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
ms.openlocfilehash: 4b2cbf333c705088d0a068521fb65e99551bb1f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799830"
---
# Como habilitar o BitLocker por meio do MBAM como parte de uma implantação do Windows


Este tópico explica como habilitar o BitLocker no computador de um usuário final usando o MBAM como parte do processo de criação e implantação do Windows. Se você vir uma tela preta na reinicialização (após concluir a fase de instalação) indicando que a unidade não pode ser desbloqueada, consulte a [etapa versões anteriores do Windows não inicia após a etapa "configurar o Windows e o Gerenciador de configurações", se o uso do BitLocker de pré-configuração for usado com o Windows 10, versão 1511](https://support.microsoft.com/en-us/help/4494799/earlier-windows-versions-don-t-start-after-you-use-pre-provision-bitlo).

**Pré-requisitos:**

-   Um processo de implantação de imagem do Windows existente – o Microsoft Deployment Toolkit (MDT), o Microsoft System Center Configuration Manager ou alguma outra ferramenta ou processo de imagem – deve estar em vigor

-   O TPM deve estar habilitado no BIOS e visível para o sistema operacional

-   A infraestrutura de servidor MBAM deve estar disponível e estar acessível

-   A partição do sistema necessária para o BitLocker deve ser criada

-   O computador deve ser associado ao domínio durante a criação de uma imagem antes que o MBAM completamente o BitLocker

**Para habilitar o BitLocker usando o MBAM 2,5 SP1 como parte de uma implantação do Windows**

1. No MBAM 2,5 SP1, a abordagem recomendada para habilitar o BitLocker durante uma implantação do Windows é usar o `Invoke-MbamClientDeployment.ps1` script do PowerShell.

   -   O `Invoke-MbamClientDeployment.ps1` script reage ao BitLocker durante o processo de criação de imagens. Quando exigido pela política do BitLocker, o agente do MBAM imediatamente solicita que o usuário do domínio crie um PIN ou uma senha quando o usuário do domínio fizer logon pela primeira vez após a criação da imagem.

   -   Fácil de usar com o MDT, o System Center Configuration Manager ou processos de imagens autônomos

   -   Compatível com o PowerShell 2,0 ou superior

   -   Criptografar volume do sistema operacional com protetor de chave TPM

   -   Suporte total ao provisionamento de BitLocker

   -   Opcionalmente, criptografe FDDs

   -   OwnerAuth TPM de caução para Windows 7, MBAM deve ter o TPM para que a caução ocorra.
   Para o Windows 8,1, Windows 10 RTM e Windows 10 versão 1511, a caução de TPM OwnerAuth é suportada.
   Para o Windows 10, versão 1607 ou posterior, somente o Windows pode apropriar-se do TPM. No addiiton, o Windows não mantém a senha de proprietário do TPM ao provisionar o TPM. Consulte a [senha de proprietário do TPM](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) para obter mais detalhes.

   -   Chaves de recuperação de caução e pacotes de chave de recuperação

   -   Relatar o status de criptografia imediatamente

   -   Novos provedores WMI

   -   Registro em log detalhado

   -   Manipulação de erros robusto

   Você pode baixar o `Invoke-MbamClientDeployment.ps1` script no [centro de download do Microsoft.com](https://www.microsoft.com/download/details.aspx?id=54439). Esse é o principal script que o sistema de implantação chamará para configurar as chaves de recuperação de unidade de disco BitLocker e de recuperação de registro com o servidor MBAM.

   **Métodos de implantação WMI para MBAM:** Os seguintes métodos WMI foram adicionados no MBAM 2,5 SP1 para dar suporte à habilitação do BitLocker usando o `Invoke-MbamClientDeployment.ps1` script do PowerShell.

   <a href="" id="mbam-machine-wmi-class"></a>Classe WMI MBAM **\ _Machine** 
    **PrepareTpmAndEscrowOwnerAuth:** Lê o TPM OwnerAuth e o envia para o banco de dados de recuperação do MBAM usando o serviço de recuperação do MBAM. Se o TPM não for proprietário e o provisionamento automático não estiver ativado, ele gerará um OwnerAuth TPM e apropriará-se. Se ele falhar, um código de erro será retornado para solução de problemas.

   **Observação** Para o Windows 10, versão 1607 ou posterior, somente o Windows pode apropriar-se do TPM. No addiiton, o Windows não mantém a senha de proprietário do TPM ao provisionar o TPM. Consulte a [senha de proprietário do TPM](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) para obter mais detalhes.

| Parâmetro | Descrição |
| -------- | ----------- |
| RecoveryServiceEndPoint | Uma cadeia de caracteres especificando o ponto de extremidade do serviço de recuperação do MBAM. |

Veja a seguir uma lista de mensagens de erro comuns:

| Valores de retorno comuns | Mensagem de erro |
| -------------------- | ------------- |
|  **S_OK**<br />0 (0x0) | O método foi bem-sucedido. |
| **MBAM_E_TPM_NOT_PRESENT**<br />2147746304 (0x80040200) | O TPM não está presente no computador ou está desabilitado na configuração do BIOS. |
| **MBAM_E_TPM_INCORRECT_STATE**<br />2147746305 (0x80040201) | O TPM não está no estado correto (habilitado, ativado e instalação do proprietário permitidos). |
| **MBAM_E_TPM_AUTO_PROVISIONING_PENDING**<br />2147746306 (0x80040202) | MBAM não pode apropriar-se do TPM porque o provisionamento automático está pendente. Tente novamente após a conclusão do provisionamento automático. |
| **MBAM_E_TPM_OWNERAUTH_READFAIL**<br />2147746307 (0x80040203) | MBAM não pode ler o valor de autorização de proprietário do TPM. O valor pode ter sido removido após uma caução com êxito. No Windows 7, o MBAM não pode ler o valor se o TPM pertencer a outras pessoas. |
| **MBAM_E_REBOOT_REQUIRED**<br />2147746308 (0x80040204) | O computador deve ser reiniciado para configurar o TPM para o estado correto. Talvez seja necessário reinicializar manualmente o computador. |
| **MBAM_E_SHUTDOWN_REQUIRED**<br />2147746309 (0x80040205) | O computador deve ser desligado e ativado novamente para definir o TPM para o estado correto. Talvez seja necessário reinicializar manualmente o computador. |
| **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | O acesso foi negado pelo ponto de extremidade remoto. |
| **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | O ponto de extremidade remoto não existe ou não foi possível localizá-lo. |
| * * WS_E_ENDPOINT_FAILURE<br />2151481357 (0x803D000F) | O ponto de extremidade remoto não pôde processar a solicitação. |
| **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | O ponto de extremidade remoto não era alcançável. |
| **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Uma mensagem contendo uma falha foi recebida do ponto de extremidade remoto. Verifique se você está se conectando ao ponto de extremidade do serviço correto. |
| **WS_E_INVALID_ENDPOINT_URL** 2151481376 (0x803D0020) | A URL do endereço do ponto de extremidade não é válida. A URL deve começar com "http" ou "https". |

   **ReportStatus:** Lê o status de conformidade do volume e o envia para o banco de dados de status de conformidade do MBAM usando o serviço de relatório de status do MBAM. O status inclui o nível de codificação, o tipo de protetor, o estado do protetor e o estado de criptografia. Se ele falhar, um código de erro será retornado para solução de problemas.

   | Parâmetro | Descrição |
   | --------- | ----------- |
   | ReportingServiceEndPoint | Uma cadeia de caracteres especificando o ponto de extremidade do serviço de relatório de status do MBAM. |

   Veja a seguir uma lista de mensagens de erro comuns:

   | Valores de retorno comuns | Mensagem de erro |
   | -------------------- | ------------- |
   | **S_OK**<br /> 0 (0x0) | O método foi bem-sucedido |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | O acesso foi negado pelo ponto de extremidade remoto.|
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | O ponto de extremidade remoto não existe ou não foi possível localizá-lo. |
   | **WS_E_ENDPOINT_FAILURE**<br /> 2151481357 (0x803D000F) | O ponto de extremidade remoto não pôde processar a solicitação. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | O ponto de extremidade remoto não era alcançável. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Uma mensagem contendo uma falha foi recebida do ponto de extremidade remoto. Verifique se você está se conectando ao ponto de extremidade do serviço correto. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0x803D0020) | A URL do endereço do ponto de extremidade não é válida. A URL deve começar com "http" ou "https". |

   <a href="" id="mbam-volume-wmi-class"></a>**MBAM \ _Volume classe WMI** **EscrowRecoveryKey:** lê a senha numérica de recuperação e o pacote de chaves do volume e as envia para o banco de dados de recuperação do MBAM usando o serviço de recuperação do MBAM. Se ele falhar, um código de erro será retornado para solução de problemas.

   | Parâmetro | Descrição |
   | --------- | ----------- |
   | RecoveryServiceEndPoint | Uma cadeia de caracteres especificando o ponto de extremidade do serviço de recuperação do MBAM. |

   Veja a seguir uma lista de mensagens de erro comuns:

   | Valores de retorno comuns | Mensagem de erro |
   | -------------------- | ------------- |
   | **S_OK**<br />0 (0x0) | O método foi bem-sucedido |
   | **FVE_E_LOCKED_VOLUME**<br />2150694912 (0x80310000) | O volume está bloqueado. |
   | **FVE_E_PROTECTOR_NOT_FOUND**<br />2150694963 (0x80310033) | Não foi encontrado um protetor de senha numérica para o volume. |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | O acesso foi negado pelo ponto de extremidade remoto. |
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | O ponto de extremidade remoto não existe ou não foi possível localizá-lo. |
   | **WS_E_ENDPOINT_FAILURE**<br />2151481357 (0x803D000F) | O ponto de extremidade remoto não pôde processar a solicitação. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | O ponto de extremidade remoto não era alcançável. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Uma mensagem contendo uma falha foi recebida do ponto de extremidade remoto. Verifique se você está se conectando ao ponto de extremidade do serviço correto. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0x803D0020) | A URL do endereço do ponto de extremidade não é válida. A URL deve começar com "http" ou "https". |
     

2. **Implantar o MBAM usando o Microsoft Deployment Toolkit (MDT) e o PowerShell**

   1.  No MDT, crie um novo compartilhamento de implantação ou abra um compartilhamento de implantação existente.

       **Observação**  
       O `Invoke-MbamClientDeployment.ps1` script do PowerShell pode ser usado com qualquer processo de imagem ou ferramenta. Esta seção mostra como integrá-lo usando o MDT, mas as etapas são semelhantes a integrá-lo a qualquer outro processo ou ferramenta.

       **Tenha**  
       Se você estiver usando o WinPE (pre-aprovisionamento) do BitLocker e quiser manter o valor de autorização de proprietário do TPM, será necessário adicionar o `SaveWinPETpmOwnerAuth.wsf` script no WinPE imediatamente antes que a instalação seja reinicializada em todo o sistema operacional. **Se você não usar esse script, perderá o valor de autorização de proprietário do TPM na reinicialização.**

   2.  Copiar `Invoke-MbamClientDeployment.ps1` para ** &lt; DeploymentShare &gt; \\Scripts**. Se você estiver usando pré-aprovisionamento, copie o `SaveWinPETpmOwnerAuth.wsf` arquivo para ** &lt; DeploymentShare &gt; \\Scripts**.

   3.  Adicione o aplicativo cliente MBAM 2,5 SP1 ao nó aplicativos no compartilhamento de implantação.

       1.  No nó **aplicativos** , clique em **novo aplicativo**.

       2.  Selecione **aplicativo com arquivos de origem**. Clique em **Avançar**.

       3.  Em **nome do aplicativo**, digite "MBAM 2,5 SP1 cliente". Clique em **Avançar**.

       4.  Navegue até o diretório que contém `MBAMClientSetup-<Version>.msi` . Clique em **Avançar**.

       5.  Digite "MBAM 2,5 SP1 Client" como o diretório a ser criado. Clique em **Avançar**.

       6.  Digite `msiexec /i MBAMClientSetup-<Version>.msi /quiet` na linha de comando. Clique em **Avançar**.

       7.  Aceite os padrões restantes para concluir o assistente de novo aplicativo.

   4.  No MDT, clique com o botão direito do mouse no nome do compartilhamento de implantação e clique em **Propriedades**. Clique na guia **regras** . Adicione as seguintes linhas:

       `SkipBitLocker=YES``BDEInstall=TPM``BDEInstallSuppress=NO``BDEWaitForEncryption=YES`

       Clique em OK para fechar a janela.

   5.  No nó sequências de tarefas, edite uma sequência de tarefas existente usada para a implantação do Windows. Se desejar, você pode criar uma nova sequência de tarefas clicando com o botão direito do mouse no nó **sequências de tarefas** , selecionando **nova sequência de tarefas**e concluindo o assistente.

       Na guia **sequência de tarefas** da sequência de tarefas selecionada, execute estas etapas:

       1.  Na pasta **pré-instalar** , habilite a tarefa opcional **habilitar BitLocker (offline)** se você quiser que o BitLocker seja habilitado no WinPE, que criptografa apenas o espaço usado.

       2.  Para persistir o TPM OwnerAuth ao usar o pre-aprovisionamento, permitindo que o MBAM faça a caução posteriormente, faça o seguinte:

           1.  Localizar a etapa **instalar sistema operacional**

           2.  Adicionar uma nova etapa de **linha de comando executar** após

           3.  Nomeie a etapa **persiste TPM OwnerAuth**

           4.  Defina a linha de comando como `cscript.exe "%SCRIPTROOT%/SaveWinPETpmOwnerAuth.wsf"`
            **Observação:** para o Windows 10, versão 1607 ou posterior, somente o Windows pode apropriar-se do TPM. No addiiton, o Windows não mantém a senha de proprietário do TPM ao provisionar o TPM. Consulte a [senha de proprietário do TPM](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) para obter mais detalhes.

       3.  Na pasta de **restauração de estado** , exclua a tarefa **habilitar BitLocker** .

       4.  Na pasta **restauração de estado** em **tarefas personalizadas**, crie uma nova tarefa de **instalar aplicativo** e nomeie-a para **instalar o MBAM Agent**. Clique no botão de opção **instalar único aplicativo** e navegue até o aplicativo cliente do MBAM 2,5 SP1 criado anteriormente.

       5.  Na pasta de **restauração de estado** em **tarefas personalizadas**, crie uma nova tarefa de **script do PowerShell executar** (após a etapa do aplicativo cliente do MBAM 2,5 SP1) com as seguintes configurações (Atualize os parâmetros conforme apropriado para o seu ambiente):

           -   Nome: configurar o BitLocker para MBAM

           -   Script do PowerShell: `Invoke-MbamClientDeployment.ps1`

           -   Os

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
               <td align="left"><p>Ponto de extremidade do serviço de recuperação MBAM</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-StatusReportingServiceEndpoint</p></td>
               <td align="left"><p>Opcional</p></td>
               <td align="left"><p>Ponto de extremidade do serviço de relatório de status MBAM</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-EncryptionMethod</p></td>
               <td align="left"><p>Opcional</p></td>
               <td align="left"><p>Método de criptografia (padrão: AES 128)</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-EncryptAndEscrowDataVolume</p></td>
               <td align="left"><p>Opção</p></td>
               <td align="left"><p>Especificar para criptografar volume (s) de dados e a (s) chave (s) de recuperação do volume de dados de caução</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-WaitForEncryptionToComplete</p></td>
               <td align="left"><p>Opção</p></td>
               <td align="left"><p>Especifique a espera pela conclusão da criptografia</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-DoNotResumeSuspendedEncryption</p></td>
               <td align="left"><p>Opção</p></td>
               <td align="left"><p>Especificar que o script de implantação não retomará a criptografia suspensa</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreEscrowOwnerAuthFailure</p></td>
               <td align="left"><p>Opção</p></td>
               <td align="left"><p>Especificar para ignorar o proprietário TPM-falha de caução de autenticação. Ele deve ser usado nos cenários em que o MBAM não consegue ler o proprietário do TPM-auth, por exemplo, se o provisionamento automático do TPM estiver habilitado</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-IgnoreEscrowRecoveryKeyFailure</p></td>
               <td align="left"><p>Opção</p></td>
               <td align="left"><p>Especificar para ignorar a falha de caução da chave de recuperação de volume</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreReportStatusFailure</p></td>
               <td align="left"><p>Opção</p></td>
               <td align="left"><p>Especificar para ignorar a falha no relatório de status</p></td>
               </tr>
               </tbody>
               </table>

                 

**Para habilitar o BitLocker usando o MBAM 2,5 ou anterior como parte de uma implantação do Windows**

1.  Instale o cliente MBAM. Para obter instruções, consulte [como implantar o cliente MBAM usando uma linha de comando](how-to-deploy-the-mbam-client-by-using-a-command-line.md).

2.  Ingressar no computador em um domínio (recomendado).

    -   Se o computador não estiver associado a um domínio, a senha de recuperação não será armazenada no serviço de recuperação de chave MBAM. Por padrão, o MBAM não permite que a criptografia ocorra, a menos que a chave de recuperação possa ser armazenada.

    -   Se um computador for iniciado no modo de recuperação antes que a chave de recuperação seja armazenada no servidor do MBAM, nenhum método de recuperação estará disponível, e o computador precisará ser renovado.

3.  Abra um prompt de comando como administrador e interrompa o serviço MBAM.

4.  Defina o serviço como **manual** ou por **demanda** digitando os seguintes comandos:

    **net stop mbamagent**

    **SC config mbamagent Start = Demand**

5.  Defina os valores do registro para que o cliente MBAM ignore as configurações de política de grupo e, em vez disso, defina a criptografia para iniciar a hora em que o Windows é implantado nesse computador cliente.

    **Cuidado**  Esta etapa descreve como modificar o registro do Windows. Usar o editor do registro incorretamente pode causar sérios problemas que podem exigir a reinstalação do Windows. Não podemos garantir que os problemas resultantes do uso incorreto do editor do registro possam ser resolvidos. Use o editor do registro por sua conta e risco.

    1.  Definir o TPM para **apenas a criptografia do sistema operacional**, executar Regedit.exe e, em seguida, importar o modelo de chave do registro de C:\\Arquivos de Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.

    2.  No Regedit.exe, vá para HKLM\\SOFTWARE\\Microsoft\\MBAM e defina as configurações listadas na tabela a seguir.

        **Observação**  Você pode definir configurações de política de grupo ou valores de registro relacionados a MBAM aqui. Essas configurações substituirão os valores definidos anteriormente.

        Definições de configuração de entrada do registro

        Deploymenttime

        0 = desativado

        1 = usar configurações de política de tempo de implantação (padrão) – Use essa configuração para habilitar a criptografia no momento em que o Windows é implantado no computador cliente.

        UseKeyRecoveryService

        0 = não usar a caução de chave (as próximas duas entradas do registro não são necessárias nesse caso)

        1 = usar a caução chave no sistema de recuperação de chave (padrão)

        Esta é a configuração recomendada, que permite que o MBAM armazene as chaves de recuperação. O computador deve ser capaz de se comunicar com o serviço de recuperação de chave MBAM. Verifique se o computador pode se comunicar com o serviço antes de prosseguir.

        Keyrecoveryoptions

        0 = carregar apenas a chave de recuperação

        1 = carregar chave de recuperação e pacote de recuperação de chave (padrão)

        KeyRecoveryServiceEndPoint

        Defina esse valor como a URL do servidor que está executando o serviço de recuperação de chave, por exemplo, http://de &lt; nome do computador &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.


6.  O cliente MBAM reiniciará o sistema durante a implantação do cliente do MBAM. Quando estiver pronto para essa reinicialização, execute o seguinte comando em um prompt de comando como administrador:

    **net start mbamagent**

7.  Quando o computador for reiniciado e o BIOS solicitar, aceite a alteração do TPM.

8.  Durante o processo de criação de imagens do sistema operacional cliente Windows, quando você estiver pronto para iniciar a criptografia, abra um prompt de comando como administrador e digite os seguintes comandos para definir o início para **automático** e reiniciar o agente cliente do MBAM:

    **SC config mbamagent Start = auto**

    **net start mbamagent**

9.  Para excluir os valores do registro de bypass, execute Regedit.exe e vá para a entrada do registro HKLM\\SOFTWARE\\Microsoft. Clique com o botão direito do mouse no nó **MBAM** e, em seguida, clique em **excluir**.

## Tópicos relacionados

[Implantando o cliente do MBAM 2.5](deploying-the-mbam-25-client.md)

[Planejando a implantação do cliente do MBAM 2.5](planning-for-mbam-25-client-deployment.md)

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
