---
title: Como habilitar o BitLocker por meio do MBAM como parte de uma implantação do Windows
description: Como habilitar o BitLocker por meio do MBAM como parte de uma implantação do Windows
author: dansimp
ms.assetid: 7609ad7a-bb06-47be-b186-0a2db787c8a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: cd4086ca6bb2ea8d253ea3b743f4efe7efbbb6c1
ms.sourcegitcommit: 325c4b77f9a9df0f3de268457fed06184623bb94
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "11626178"
---
# <a name="how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deployment"></a>Como habilitar o BitLocker por meio do MBAM como parte de uma implantação do Windows

> [!IMPORTANT]
> Essas instruções não pertencem ao Gerenciamento de BitLocker do Configuration Manager. O `Invoke-MbamClientDeployment.ps1` script do PowerShell não tem suporte para uso com o Gerenciamento do BitLocker no Configuration Manager. Isso inclui a escroção de chaves de recuperação do BitLocker durante uma sequência de tarefas do Configuration Manager. Além disso, a partir do Configuration Manager Current Branch 2103, o Gerenciamento de BitLocker do Configuration Manager não usa mais o site de serviços de recuperação de chaves do MBAM para escrow keys. Tentar usar o script do PowerShell com o `Invoke-MbamClientDeployment.ps1` Configuration Manager Current Branch 2103 ou mais novo pode resultar em sérios problemas com o site do Configuration Manager. Os problemas conhecidos incluem a criação de uma grande quantidade de política direcionada a todos os dispositivos que podem causar tempestades de política. Isso levará a uma grave degradação do desempenho no Configuration Manager principalmente SQL e com Pontos de Gerenciamento.

Este tópico explica como habilitar o BitLocker no computador de um usuário final usando o MBAM como parte do seu processo de Windows de implantação e imagens. Se você vir uma tela preta na reinicialização (após a conclusão da fase de instalação) indicando que a unidade não pode ser desbloqueada, consulte Versões anteriores do Windows não começam após a etapa ["Setup Windows and Configuration Manager" se o BitLocker](https://support.microsoft.com/en-us/help/4494799/earlier-windows-versions-don-t-start-after-you-use-pre-provision-bitlo)de pré-provisionamento for usado com o Windows 10, versão 1511 .

**Pré-requisitos:**

-   Um processo de implantação Windows imagem existente – O microsoft deployment Toolkit (MDT), o Microsoft System Center Configuration Manager ou alguma outra ferramenta ou processo de imagem - deve estar no local

-   O TPM deve ser habilitado no BIOS e visível para o sistema operacional

-   A infraestrutura do servidor MBAM deve estar no local e acessível

-   A partição do sistema exigida pelo BitLocker deve ser criada

-   O computador deve ser ingressado no domínio durante a imagem antes que o MBAM habilita totalmente o BitLocker

**Para habilitar o BitLocker usando o MBAM 2.5 SP1 como parte de uma Windows implantação**

1. No MBAM 2.5 SP1, a abordagem recomendada para habilitar o BitLocker durante uma implantação Windows é usando o `Invoke-MbamClientDeployment.ps1` script do PowerShell.

   -   O `Invoke-MbamClientDeployment.ps1` script decreta o BitLocker durante o processo de imagem. Quando necessário pela política BitLocker, o agente do MBAM solicita imediatamente que o usuário de domínio crie um PIN ou senha quando o usuário de domínio faz o primeiro logo depois da imagem.

   -   Fácil de usar com processos de imagem MDT, System Center Configuration Manager ou autônomos

   -   Compatível com o PowerShell 2.0 ou superior

   -   Criptografar o volume do sistema operacional com o protetor de teclas TPM

   -   Suporte total ao pré-provisionamento do BitLocker

   -   Opcionalmente criptografar FDDs

   -   Escrow TPM OwnerAuth For Windows 7, MBAM must own the TPM for escrow to occur.
   Para Windows 8.1, Windows 10 RTM e Windows 10 versão 1511, há suporte para a escrow do TPM OwnerAuth.
   Para Windows 10, versão 1607 ou posterior, somente Windows pode assumir a propriedade do TPM. Em addiiton, Windows manterá a senha do proprietário do TPM ao provisionar o TPM. Consulte [A senha do proprietário do TPM](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) para obter mais detalhes.

   -   Chaves de recuperação de escrow e pacotes de chaves de recuperação

   -   Relatar o status de criptografia imediatamente

   -   Novos provedores WMI

   -   Registro em log detalhado

   -   Tratamento de erros robustos

   Você pode baixar o `Invoke-MbamClientDeployment.ps1` script Microsoft.com Centro de [Download.](https://www.microsoft.com/download/details.aspx?id=54439) Este é o script principal que seu sistema de implantação chamará para configurar a criptografia de unidade bitLocker e gravar chaves de recuperação com o MBAM Server.

   **Métodos de implantação WMI para MBAM:** Os métodos WMI a seguir foram adicionados ao MBAM 2.5 SP1 para dar suporte à habilitação do BitLocker usando o `Invoke-MbamClientDeployment.ps1` script do PowerShell.

   <a href="" id="mbam-machine-wmi-class"></a>**MBAM\_Machine Classe WMI** 
    **PrepareTpmAndEscrowOwnerAuth:** Lê o TPM OwnerAuth e o envia para o banco de dados de recuperação do MBAM usando o serviço de recuperação do MBAM. Se o TPM não for de propriedade e o provisionamento automático não estiver em, ele gerará um TPM OwnerAuth e assume a propriedade. Se falhar, um código de erro será retornado para solução de problemas.

   **Observação** Para Windows 10, versão 1607 ou posterior, somente Windows pode assumir a propriedade do TPM. Em addiiton, Windows manterá a senha do proprietário do TPM ao provisionar o TPM. Consulte [A senha do proprietário do TPM](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) para obter mais detalhes.

| Parâmetro | Descrição |
| -------- | ----------- |
| RecoveryServiceEndPoint | Uma cadeia de caracteres que especifica o ponto de extremidade do serviço de recuperação do MBAM. |

Aqui estão uma lista de mensagens de erro comuns:

| Valores comuns de retorno | Mensagem de erro |
| -------------------- | ------------- |
|  **S_OK**<br />0 (0x0) | O método foi bem-sucedido. |
| **MBAM_E_TPM_NOT_PRESENT**<br />2147746304 (0x80040200) | O TPM não está presente no computador ou está desabilitado na configuração do BIOS. |
| **MBAM_E_TPM_INCORRECT_STATE**<br />2147746305 (0x80040201) | O TPM não está no estado correto (habilitada, ativada e a instalação do proprietário permitida). |
| **MBAM_E_TPM_AUTO_PROVISIONING_PENDING**<br />2147746306 (0x80040202) | O MBAM não pode assumir a propriedade do TPM porque o provisionamento automático está pendente. Tente novamente depois que o provisionamento automático for concluído. |
| **MBAM_E_TPM_OWNERAUTH_READFAIL**<br />2147746307 (0x80040203) | O MBAM não pode ler o valor de autorização do proprietário do TPM. O valor pode ter sido removido após uma escrow bem-sucedida. No Windows 7, o MBAM não poderá ler o valor se o TPM for de outras pessoas. |
| **MBAM_E_REBOOT_REQUIRED**<br />2147746308 (0x80040204) | O computador deve ser reiniciado para definir o TPM como o estado correto. Talvez seja necessário reiniciar manualmente o computador. |
| **MBAM_E_SHUTDOWN_REQUIRED**<br />2147746309 (0x80040205) | O computador deve ser desligado e ligado novamente para definir o TPM como o estado correto. Talvez seja necessário reiniciar manualmente o computador. |
| **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | O acesso foi negado pelo ponto de extremidade remoto. |
| **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | O ponto de extremidade remoto não existe ou não pôde ser localizado. |
| **WS_E_ENDPOINT_FAILURE<br />2151481357 (0x803D000F) | O ponto de extremidade remoto não pôde processar a solicitação. |
| **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | O ponto de extremidade remoto não era acessível. |
| **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Uma mensagem contendo uma falha foi recebida do ponto de extremidade remoto. Certifique-se de que você está se conectando ao ponto de extremidade de serviço correto. |
| **WS_E_INVALID_ENDPOINT_URL** 2151481376 (0x803D0020) | A URL do endereço do ponto de extremidade não é válida. A URL deve começar com "http" ou "https". |

   **ReportStatus:** Lê o status de conformidade do volume e o envia para o banco de dados de status de conformidade do MBAM usando o serviço de relatório de status do MBAM. O status inclui a força da codificação, o tipo de protetor, o estado do protetor e o estado de criptografia. Se falhar, um código de erro será retornado para solução de problemas.

   | Parâmetro | Descrição |
   | --------- | ----------- |
   | ReportingServiceEndPoint | Uma cadeia de caracteres que especifica o ponto de extremidade do serviço de relatório de status do MBAM. |

   Aqui estão uma lista de mensagens de erro comuns:

   | Valores comuns de retorno | Mensagem de erro |
   | -------------------- | ------------- |
   | **S_OK**<br /> 0 (0x0) | O método foi bem-sucedido |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | O acesso foi negado pelo ponto de extremidade remoto.|
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | O ponto de extremidade remoto não existe ou não pôde ser localizado. |
   | **WS_E_ENDPOINT_FAILURE**<br /> 2151481357 (0x803D000F) | O ponto de extremidade remoto não pôde processar a solicitação. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | O ponto de extremidade remoto não era acessível. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Uma mensagem contendo uma falha foi recebida do ponto de extremidade remoto. Certifique-se de que você está se conectando ao ponto de extremidade de serviço correto. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0x803D0020) | A URL do endereço do ponto de extremidade não é válida. A URL deve começar com "http" ou "https". |

   <a href="" id="mbam-volume-wmi-class"></a>**MBAM\_Volume WMI Class** **EscrowRecoveryKey:** lê a senha numérica de recuperação e o pacote de chaves do volume e os envia para o banco de dados de recuperação do MBAM usando o serviço de recuperação do MBAM. Se falhar, um código de erro será retornado para solução de problemas.

   | Parâmetro | Descrição |
   | --------- | ----------- |
   | RecoveryServiceEndPoint | Uma cadeia de caracteres que especifica o ponto de extremidade do serviço de recuperação do MBAM. |

   Aqui estão uma lista de mensagens de erro comuns:

   | Valores comuns de retorno | Mensagem de erro |
   | -------------------- | ------------- |
   | **S_OK**<br />0 (0x0) | O método foi bem-sucedido |
   | **FVE_E_LOCKED_VOLUME**<br />2150694912 (0x80310000) | O volume está bloqueado. |
   | **FVE_E_PROTECTOR_NOT_FOUND**<br />2150694963 (0x80310033) | Um protetor de Senha Numérica não foi encontrado para o volume. |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | O acesso foi negado pelo ponto de extremidade remoto. |
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | O ponto de extremidade remoto não existe ou não pôde ser localizado. |
   | **WS_E_ENDPOINT_FAILURE**<br />2151481357 (0x803D000F) | O ponto de extremidade remoto não pôde processar a solicitação. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | O ponto de extremidade remoto não era acessível. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Uma mensagem contendo uma falha foi recebida do ponto de extremidade remoto. Certifique-se de que você está se conectando ao ponto de extremidade de serviço correto. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0x803D0020) | A URL do endereço do ponto de extremidade não é válida. A URL deve começar com "http" ou "https". |
     

2. **Implantar o MBAM usando o Microsoft Deployment Toolkit (MDT) e o PowerShell**

   1.  No MDT, crie um novo compartilhamento de implantação ou abra um compartilhamento de implantação existente.

       **Observação**  
       O `Invoke-MbamClientDeployment.ps1` script do PowerShell pode ser usado com qualquer processo de imagem ou ferramenta. Esta seção mostra como integrá-lo usando o MDT, mas as etapas são semelhantes à integração com qualquer outro processo ou ferramenta.

       **Cuidado**  
       Se você estiver usando o pré-provisionamento do BitLocker (WinPE) e quiser manter o valor de autorização do proprietário do TPM, adicione o script no WinPE imediatamente antes que a instalação seja reiniciada no sistema operacional `SaveWinPETpmOwnerAuth.wsf` completo. **Se você não usar esse script, perderá o valor de autorização do proprietário do TPM na reinicialização.**

   2.  Copiar `Invoke-MbamClientDeployment.ps1` para ** &lt; DeploymentShare &gt; \\Scripts**. Se você estiver usando o pré-provisionamento, copie o arquivo `SaveWinPETpmOwnerAuth.wsf` em ** &lt; DeploymentShare &gt; \\Scripts**.

   3.  Adicione o aplicativo cliente MBAM 2.5 SP1 ao nó Aplicativos no compartilhamento de implantação.

       1.  No nó **Aplicativos,** clique em **Novo Aplicativo**.

       2.  Selecione **Aplicativo com Arquivos de Origem**. Clique em **Avançar**.

       3.  Em **Nome do Aplicativo,** digite "MBAM 2.5 SP1 Client". Clique em **Avançar**.

       4.  Navegue até o diretório que contém `MBAMClientSetup-<Version>.msi` . Clique em **Avançar**.

       5.  Digite "Cliente MBAM 2.5 SP1" como o diretório a ser criado. Clique em **Avançar**.

       6.  Insira `msiexec /i MBAMClientSetup-<Version>.msi /quiet` na linha de comando. Clique em **Avançar**.

       7.  Aceite os padrões restantes para concluir o assistente Novo Aplicativo.

   4.  No MDT, clique com o botão direito do mouse no nome do compartilhamento de implantação e clique em **Propriedades**. Clique na **guia Regras.** Adicione as seguintes linhas:

       `SkipBitLocker=YES``BDEInstall=TPM``BDEInstallSuppress=NO``BDEWaitForEncryption=YES`

       Clique em OK para fechar a janela.

   5.  No nó Sequências de Tarefas, edite uma sequência de tarefas existente usada para Windows Implantação. Se quiser, você pode criar uma nova sequência de tarefas clicando com o botão direito do mouse no nó **Sequências** de Tarefas, selecionando **Nova**Sequência de Tarefas e concluindo o assistente.

       Na guia **Sequência de** Tarefas da sequência de tarefas selecionada, execute estas etapas:

       1.  Na pasta **Pré-instalação,** habilita a tarefa opcional **Habilitar o BitLocker (Offline)** se você quiser o BitLocker habilitado no WinPE, que criptografa somente o espaço usado.

       2.  Para persistir o Proprietário do TPMAuth ao usar o pré-provisionamento, permitindo que o MBAM o escrow mais tarde, faça o seguinte:

           1.  Encontre a **etapa Instalar Sistema** Operacional

           2.  Adicionar uma nova **etapa de Linha de** Comando de Executar após ela

           3.  Nomeia a etapa **Persist TPM OwnerAuth**

           4.  De definir a linha de comando como `cscript.exe "%SCRIPTROOT%/SaveWinPETpmOwnerAuth.wsf"`
            **Observação:** para Windows 10, versão 1607 ou posterior, somente Windows pode assumir a propriedade do TPM. Em addiiton, Windows manterá a senha do proprietário do TPM ao provisionar o TPM. Consulte [A senha do proprietário do TPM](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) para obter mais detalhes.

       3.  Na pasta **Restauração de Estado,** exclua **a tarefa Habilitar BitLocker.**

       4.  Na pasta **Restauração de Estado** em Tarefas **Personalizadas,** crie uma nova tarefa **Instalar Aplicativo** e nomee-a Instalar o **Agente MBAM.** Clique no **botão de rádio** Instalar Aplicativo Único e navegue até o aplicativo cliente MBAM 2.5 SP1 criado anteriormente.

       5.  Na **** pasta Restauração de Estado em Tarefas Personalizadas, **** crie uma nova tarefa Executar Script do **PowerShell** (após a etapa do aplicativo cliente MBAM 2.5 SP1) com as seguintes configurações (atualize os parâmetros conforme apropriado para seu ambiente):

           -   Nome: Configurar o BitLocker para MBAM

           -   Script do PowerShell: `Invoke-MbamClientDeployment.ps1`

           -   Parâmetros:

               <table>
               <colgroup>
               <col width="33%" />
               <col width="33%" />
               <col width="33%" />
               </colgroup>
               <tbody>
               <tr class="odd">
               <td align="left"><p>-RecoveryServiceEndpoint</p></td>
               <td align="left"><p>Obrigatório</p></td>
               <td align="left"><p>Ponto de extremidade do serviço de recuperação do MBAM</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-StatusReportingServiceEndpoint</p></td>
               <td align="left"><p>Opcional</p></td>
               <td align="left"><p>Ponto de extremidade do serviço de relatório de status do MBAM</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-EncryptionMethod</p></td>
               <td align="left"><p>Opcional</p></td>
               <td align="left"><p>Método de criptografia (padrão: AES 128)</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-EncryptAndEscrowDataVolume</p></td>
               <td align="left"><p>Opção</p></td>
               <td align="left"><p>Especificar para criptografar volumes de dados e escrow data volume recovery key(s)</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-WaitForEncryptionToComplete</p></td>
               <td align="left"><p>Opção</p></td>
               <td align="left"><p>Especificar para aguardar a conclusão da criptografia</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-DoNotResumeSuspendedEncryption</p></td>
               <td align="left"><p>Opção</p></td>
               <td align="left"><p>Especificar que o script de implantação não retomará a criptografia suspensa</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreEscrowOwnerAuthFailure</p></td>
               <td align="left"><p>Opção</p></td>
               <td align="left"><p>Especifique para ignorar a falha de escrow owner-auth do TPM. Ele deve ser usado nos cenários em que o MBAM não é capaz de ler o proprietário do TPM, por exemplo, se o provisionamento automático do TPM estiver habilitado</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-IgnoreEscrowRecoveryKeyFailure</p></td>
               <td align="left"><p>Opção</p></td>
               <td align="left"><p>Especificar para ignorar a falha de escrow da chave de recuperação de volume</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreReportStatusFailure</p></td>
               <td align="left"><p>Opção</p></td>
               <td align="left"><p>Especificar para ignorar a falha de relatórios de status</p></td>
               </tr>
               </tbody>
               </table>

                 

**Para habilitar o BitLocker usando o MBAM 2.5 ou anterior como parte de uma Windows implantação**

1.  Instale o cliente MBAM. Para obter instruções, [consulte How to Deploy the MBAM Client by Using a Command Line](how-to-deploy-the-mbam-client-by-using-a-command-line.md).

2.  Associar o computador a um domínio (recomendado).

    -   Se o computador não estiver ingressado em um domínio, a senha de recuperação não será armazenada no serviço de Recuperação de Chave do MBAM. Por padrão, o MBAM não permite que a criptografia ocorra, a menos que a chave de recuperação possa ser armazenada.

    -   Se um computador for iniciado no modo de recuperação antes que a chave de recuperação seja armazenada no MBAM Server, nenhum método de recuperação estará disponível e o computador terá que ser reimaginado.

3.  Abra um prompt de comando como administrador e pare o serviço MBAM.

4.  De definir o serviço como **Manual** **ou Sob demanda** digitando os seguintes comandos:

    **net stop mbamagent**

    **sc config mbamagent start= demand**

5.  De definir os valores do Registro para que o Cliente MBAM ignore as configurações da Política de Grupo e, em vez disso, desarme a criptografia para iniciar a hora em que Windows é implantado nesse computador cliente.

    **Cuidado**  
    Esta etapa descreve como modificar o Windows registro. Usar o Editor de Registro incorretamente pode causar problemas sérios que podem exigir que você reinstale Windows. Não podemos garantir que os problemas resultantes do uso incorreto do Editor de Registro possam ser resolvidos. Use o Editor do Registro por sua conta e risco.

    1.  Dejuste o TPM para criptografia somente do sistema **operacional,** execute Regedit.exe e importe o modelo de chave do Registro de C:\\Arquivos de Programas\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.

    2.  Em Regedit.exe, vá para HKLM\\SOFTWARE\\Microsoft\\MBAM e configure as configurações listadas na tabela a seguir.

        **Observação**  
        Você pode definir configurações de Política de Grupo ou valores do Registro relacionados ao MBAM aqui. Essas configurações substituirão os valores definidos anteriormente.

        Configurações de configuração de entrada do Registro

        DeploymentTime

        0 = Desligado

        1 = Use configurações de política de tempo de implantação (padrão) – use essa configuração para habilitar a criptografia no momento em que Windows é implantado no computador cliente.

        UseKeyRecoveryService

        0 = Não use o escrow de chave (as próximas duas entradas do Registro não são necessárias neste caso)

        1 = Usar o escrow de teclas no sistema de Recuperação de Chaves (padrão)

        Essa é a configuração recomendada, que permite que o MBAM armazene as chaves de recuperação. O computador deve ser capaz de se comunicar com o serviço de Recuperação de Chave do MBAM. Verifique se o computador pode se comunicar com o serviço antes de prosseguir.

        KeyRecoveryOptions

        0 = Carrega somente Chave de Recuperação

        1 = Carrega Chave de Recuperação e Pacote de Recuperação de Chave (padrão)

        KeyRecoveryServiceEndPoint

        Dejuste esse valor para a URL do servidor que executa o serviço de Recuperação de Chave, por exemplo, http:// nome do computador &lt; &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.


6.  O Cliente MBAM reiniciará o sistema durante a implantação do Cliente MBAM. Quando você estiver pronto para essa reinicialização, execute o seguinte comando em um prompt de comando como administrador:

    **net start mbamagent**

7.  Quando os computadores reiniciarem e o BIOS solicitar, aceite a alteração do TPM.

8.  Durante o Windows de imagens do sistema operacional cliente, quando você estiver pronto para iniciar a criptografia, abra um prompt de comando como administrador e digite os seguintes comandos para definir o início como **Automático** e reiniciar o agente cliente MBAM:

    **sc config mbamagent start= auto**

    **net start mbamagent**

9.  Para excluir os valores do registro de bypass, execute Regedit.exe e vá para a entrada HKLM\\SOFTWARE\\Microsoft Registry. Clique com o botão direito do mouse no nó **MBAM** e clique em **Excluir**.

## <a name="related-topics"></a>Tópicos relacionados

[Implantando o cliente do MBAM 2.5](deploying-the-mbam-25-client.md)

[Planejando a implantação do cliente do MBAM 2.5](planning-for-mbam-25-client-deployment.md)

## <a name="got-a-suggestion-for-mbam"></a>Tem uma sugestão para MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas de MBAM, use o [Fórum technet do MBAM.](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)
