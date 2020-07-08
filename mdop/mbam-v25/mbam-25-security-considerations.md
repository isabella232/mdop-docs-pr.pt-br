---
title: Considerações sobre segurança do MBAM 2.5
description: Considerações sobre segurança do MBAM 2.5
author: dansimp
ms.assetid: f6613c63-b32b-45fb-a6e8-673d6dae7d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: 86a756ab6f983fa1f22de6835b5993e1215d1dbe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799952"
---
# Considerações sobre segurança do MBAM 2.5


Este tópico contém as seguintes informações sobre como proteger a administração e o monitoramento do Microsoft BitLocker (MBAM):

-   [Configurar o MBAM para fazer a caução do TPM e armazenar senhas do OwnerAuth](#bkmk-tpm)

-   [Configurar o MBAM para desbloquear automaticamente o TPM após um bloqueio](#bkmk-autounlock)

-   [Conexões seguras com o SQL Server](#bkmk-secure-databases)

-   [Criar contas e grupos](#bkmk-accts-groups)

-   [Usar arquivos de log do MBAM](#bkmk-logfiles)

-   [Analisar considerações do TDE de banco de dados MBAM](#bkmk-tde)

-   [Entender as considerações gerais de segurança](#bkmk-general-security)

## <a href="" id="bkmk-tpm"></a>Configurar o MBAM para fazer a caução do TPM e armazenar senhas do OwnerAuth

**Observação** Para o Windows 10, versão 1607 ou posterior, somente o Windows pode apropriar-se do TPM. Além disso, o Windows não mantém a senha de proprietário do TPM ao provisionar o TPM. Consulte a [senha de proprietário do TPM](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) para obter mais detalhes.

Dependendo da configuração, o Trusted Platform Module (TPM) será bloqueado em determinadas situações ─ como quando muitas senhas incorretas são inseridas ─ e podem permanecer bloqueadas por um período de tempo. Durante o bloqueio do TPM, o BitLocker não pode acessar as chaves de criptografia para executar operações de desbloqueio ou descriptografia, exigindo que o usuário insira sua chave de recuperação do BitLocker para acessar a unidade do sistema operacional. Para redefinir o bloqueio de TPM, você deve fornecer a senha de OwnerAuth do TPM.

MBAM pode armazenar a senha do OwnerAuth do TPM no banco de dados do MBAM se ele possuir o TPM ou se ele tiver a senha em caução. As senhas do OwnerAuth podem ser facilmente acessadas no site de administração e monitoramento quando você deve se recuperar de um bloqueio de TPM, eliminando a necessidade de aguardar que o bloqueio seja resolvido por conta própria.

### OwnerAuth TPM de caução no Windows 8 e em versões mais recentes

**Observação** Para o Windows 10, versão 1607 ou posterior, somente o Windows pode apropriar-se do TPM. No addiiton, o Windows não mantém a senha de proprietário do TPM ao provisionar o TPM. Consulte a [senha de proprietário do TPM](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) para obter mais detalhes.

No Windows 8 ou superior, o MBAM não deve mais possuir o TPM para armazenar a senha do OwnerAuth, desde que o OwnerAuth esteja disponível no computador local.

Para habilitar o MBAM para caução e, em seguida, armazenar senhas de OwnerAuth do TPM, você deve definir essas configurações de política de grupo.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuração da política de grupo</th>
<th align="left">Configuração</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ativar o backup do TPM nos serviços de domínio do Active Directory</p></td>
<td align="left"><p>Desabilitado ou não configurado</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurar o nível de informações de autorização de proprietário do TPM disponíveis para o sistema operacional</p></td>
<td align="left"><p>Delegado/nenhum ou não configurado</p></td>
</tr>
</tbody>
</table>

 

O local dessas configurações de política de grupo é o sistema de modelos administrativos de **configuração do computador** &gt; **Administrative Templates** &gt; **System** &gt; **serviços de módulo de plataforma confiável**.

**Observação**  O Windows remove o OwnerAuth localmente após o MBAM ter a caução com êxito com essas configurações.

 

### OwnerAuth TPM de caução no Windows 7

No Windows 7, MBAM deve possuir o TPM para fazer automaticamente a caução do TPM OwnerAuth informações no banco de dados do MBAM. Se o MBAM não for proprietário do TPM, você deverá usar os cmdlets de importação de dados do Active Directory do MBAM (AD) para copiar OwnerAuth do TPM do Active Directory para o banco de dados do MBAM.

### Cmdlets de importação de dados do Active MBAM do Active Directory

Os cmdlets de importação de dados do Active Directory do MBAM permitem que você recupere pacotes de chave de recuperação e senhas do OwnerAuth armazenadas no Active Directory.

O MBAM 2,5 SP1 Server é fornecido com quatro cmdlets do PowerShell que preenchem bancos de dados do MBAM com as informações de recuperação de volume e de proprietário do TPM armazenadas no Active Directory.

Para pacotes e chaves de recuperação de volume:

-   Leitura-ADRecoveryInformation

-   Write-MbamRecoveryInformation

Para obter informações de proprietário do TPM:

-   Leitura-ADTpmInformation

-   Write-MbamTpmInformation

Para associar usuários a computadores:

-   Write-MbamComputerUser

Os cmdlets Read-AD \ * lêem informações do Active Directory. Os cmdlets Write-MBAM \ * empurram os dados para os bancos de dados do MBAM. Consulte [a referência de cmdlet para administração e monitoramento do Microsoft Bitlocker 2,5](https://technet.microsoft.com/library/dn459018.aspx) para obter informações detalhadas sobre esses cmdlets, incluindo sintaxe, parâmetros e exemplos.

**Criar associações de usuário para computador:** Os cmdlets de importação de dados do Active Directory do MBAM coletam informações do Active Directory e inserem os dados no banco de dados do MBAM. No entanto, eles não associam usuários a volumes. Você pode baixar o Add-ComputerUser.ps1 script do PowerShell para criar associações de usuário para computador, que permitem que os usuários obtenham acesso a um computador por meio do site de administração e monitoramento ou usando o portal de autoatendimento para recuperação. O script Add-ComputerUser.ps1 coleta dados do atributo **gerenciado por** no Active Directory (AD), o proprietário do objeto no AD ou de um arquivo CSV personalizado. Em seguida, o script adiciona os usuários descobertos ao objeto de pipeline de informações de recuperação, que deve ser passado para Write-MbamRecoveryInformation para inserir os dados no banco de dados de recuperação.

Baixe o Add-ComputerUser.ps1 script do PowerShell no [centro de download da Microsoft](https://go.microsoft.com/fwlink/?LinkId=613122).

Você pode especificar **ajuda Add-ComputerUser.ps1** para obter ajuda para o script, incluindo exemplos de como usar os cmdlets e o script.

Para criar associações entre computadores após a instalação do servidor do MBAM, use o cmdlet do PowerShell Write-MbamComputerUser. Semelhante ao Add-ComputerUser.ps1 script do PowerShell, esse cmdlet permite que você especifique os usuários que podem usar o portal de autoatendimento para obter informações de OwnerAuth de TPM ou senhas de recuperação de volume do computador especificado.

**Observação**  O agente MBAM substituirá as associações de usuário para computador quando esse computador começar a se reportar até o servidor.

 

**Pré-requisitos:** Os cmdlets Read-AD \ * podem recuperar informações do AD apenas se eles forem executados como uma conta de usuário altamente privilegiada, como um administrador de domínio, ou executar como uma conta em um grupo de segurança personalizado com acesso de leitura às informações (recomendado).

[Guia de operações de criptografia de unidade de disco BitLocker: recuperar volumes criptografados com o AD DS](https://technet.microsoft.com/library/cc771778(WS.10).aspx) fornece detalhes sobre como criar um grupo de segurança personalizado (ou vários grupos) com acesso de leitura às informações do anúncio.

**Permissões de gravação do serviço Web de hardware e recuperação do MBAM:** Os cmdlets Write-MBAM \ * aceitam a URL do serviço de recuperação e hardware do MBAM, usados para publicar as informações de recuperação ou TPM. Geralmente, apenas uma conta de serviço do computador do domínio pode se comunicar com o serviço de recuperação e hardware do MBAM. No MBAM 2,5 SP1, você pode configurar o serviço de recuperação e de hardware do MBAM com um grupo de segurança chamado DataMigrationAccessGroup cujos membros podem ignorar a verificação da conta do serviço de computador do domínio. Os cmdlets Write-MBAM \ * devem ser executados como um usuário pertencente a esse grupo configurado. (Se preferir, as credenciais de um usuário individual no grupo configurado podem ser especificadas usando o parâmetro – Credential nos cmdlets Write-MBAM \ *.)

Você pode configurar o serviço de recuperação e de hardware do MBAM com o nome desse grupo de segurança de uma destas maneiras:

-   Forneça o nome do grupo de segurança (ou individual) no parâmetro-DataMigrationAccessGroup do cmdlet Enable-MbamWebApplication – AgentService do PowerShell.

-   Configure o grupo após a instalação do serviço de hardware e recuperação do MBAM, editando o arquivo web.config &lt; na &gt; pasta \\Microsoft Solution\\Recovery de gerenciamento do BitLocker e Service\\.

    ```xml
    <add key="DataMigrationUsersGroupName" value="<groupName>|<empty>" />
    ```

    onde &lt; nome_do_grupo &gt; é substituído pelo domínio e o nome do grupo (ou o usuário individual) que será usado para permitir a migração de dados do Active Directory.

-   Use o editor de configuração no Gerenciador do IIS para editar esse appSetting.

No exemplo a seguir, o comando, quando executado como membro do grupo ADRecoveryInformation e do grupo usuários de migração de dados, extrai as informações de recuperação de volume de computadores na unidade organizacional WORKSTATIONs (OU) no domínio contoso.com e os grava no MBAM usando o serviço de recuperação e de hardware do MBAM em execução no servidor mbam.contoso.com.

``` syntax
PS C:\> Read-ADRecoveryInformation -Server contoso.com -SearchBase "OU=WORKSTATIONS,DC=CONTOSO,DC=COM" | Write-MbamRecoveryInformation -RecoveryServiceEndPoint "https://mbam.contoso.com/MBAMRecoveryAndHardwareService/CoreService.svc"
```

**Ler-os cmdlets de leitura \ *** aceitam o nome ou o endereço IP de um computador servidor host do Active Directory para consultar informações de recuperação ou TPM. Recomendamos fornecer os nomes distintos dos contêineres de anúncios nos quais o objeto de computador reside como o valor do parâmetro SearchBase. Se os computadores estiverem armazenados em várias UOs, os cmdlets poderão aceitar a entrada de pipeline para serem executados uma vez para cada contêiner. O nome diferenciado de um contêiner de anúncios terá uma aparência semelhante a OU = máquinas, CC = contoso, DC = com. Executar uma pesquisa direcionada para contêineres específicos oferece os seguintes benefícios:

-   Reduz o risco de tempo limite enquanto consulta um grande conjunto de um conjunto de grandes objetos de computador.

-   Pode omitir UOs que contenham servidores Datacenter ou outras classes de computadores para as quais o backup pode não ser desejado ou necessário.

Outra opção é fornecer o sinalizador-recurse com ou sem o SearchBase opcional para pesquisar objetos de computador em todos os contêineres sob o SearchBase especificado ou o domínio inteiro, respectivamente. Ao usar o sinalizador-recurse, você também pode usar o parâmetro-MaxPageSize para controlar a quantidade de memória local e remota necessária para atender a consulta.

Esses cmdlets gravam nos objetos de pipeline do tipo PsObject. Cada ocorrência de PsObject contém uma única chave de recuperação de volume ou uma cadeia de caracteres de proprietário TPM com seu nome de computador associado, carimbo de data/hora e outras informações necessárias para publicá-lo no repositório de dados MBAM.

Os **cmdlets Write-MBAM \ *** aceitam valores de parâmetro de informações de recuperação do pipeline por nome da propriedade. Isso permite que os cmdlets Write-MBAM \ * aceitem a saída do pipeline dos cmdlets Read-AD \ * (por exemplo, Read-ADRecoveryInformation – Server contoso.com-recurse | Write-MbamRecoveryInformation – RecoveryServiceEndpoint mbam.contoso.com).

Os **cmdlets Write-MBAM \ *** incluem parâmetros opcionais que fornecem opções para tolerância a falhas, registro em log detalhado e preferências para a WhatIf e confirmar.

Os **cmdlets Write-MBAM \ *** também incluem um parâmetro de *tempo* opcional cujo valor é um objeto **DateTime** . Esse objeto inclui um atributo *Kind* que pode ser definido como `Local` , `UTC` , ou `Unspecified` . Quando o parâmetro *tempo* é preenchido a partir de dados obtidos do Active Directory, o tempo é convertido em UTC e esse atributo *Kind* é definido automaticamente como `UTC` . No entanto, ao preencher o parâmetro *time* usando outra fonte, como um arquivo de texto, você deve explicitamente definir o atributo *Kind* para o valor apropriado.

**Observação**  Os cmdlets Read-AD \ * não têm a capacidade de descobrir as contas de usuário que representam os usuários do computador. As associações de conta de usuário são necessárias para o seguinte:

-   Os usuários recuperem senhas/pacotes de volume usando o portal de autoatendimento

-   Usuários que não estão no grupo de segurança usuários da assistência técnica avançada do MBAM conforme definidos durante a instalação, recuperando em nome de outros usuários

 

## <a href="" id="bkmk-autounlock"></a>Configurar o MBAM para desbloquear automaticamente o TPM após um bloqueio


Você pode configurar o MBAM 2,5 SP1 para desbloquear automaticamente o TPM em caso de bloqueio. Se a reinicialização automática do bloqueio do TPM estiver habilitada, o MBAM pode detectar que um usuário está bloqueado e obter a senha do OwnerAuth do banco de dados do MBAM para desbloquear automaticamente o TPM para o usuário. A redefinição automática do bloqueio do TPM só estará disponível se a chave de recuperação do sistema operacional desse computador foi recuperada usando o portal de autoatendimento ou o site de administração e monitoramento.

**Importante**  Para habilitar a redefinição automática do bloqueio do TPM, você deve configurar esse recurso tanto no lado do servidor quanto na política de grupo do lado do cliente.

 

-   Para habilitar a redefinição automática do bloqueio do TPM no lado do cliente, defina a configuração da política de grupo "configurar redefinição automática do bloqueio do TPM", localizada em modelos administrativos de **configuração do computador** &gt; **Administrative Templates** &gt; **componentes do Windows** &gt; **MBAM** &gt; **Gerenciamento de cliente**.

-   Para habilitar a redefinição automática do bloqueio do TPM no lado do servidor, você pode verificar "habilitar a redefinição automática do bloqueio do TPM" no assistente de configuração do servidor do MBAM durante a instalação.

    Você também pode habilitar a redefinição automática do bloqueio do TPM no PowerShell especificando a opção "-reinício automático do bloqueio do TPM" ao habilitar o componente Web do serviço de agente.

Depois que um usuário inserir a chave de recuperação do BitLocker que obteve no portal de autoatendimento ou o site de administração e monitoramento, o agente do MBAM determinará se o TPM está bloqueado. Se estiver bloqueado, ele tentará recuperar o TPM OwnerAuth para o computador do banco de dados do MBAM. Se o TPM OwnerAuth for recuperado com êxito, ele será usado para desbloquear o TPM. Desbloquear o TPM torna o TPM totalmente funcional e o usuário não será forçado a inserir a senha de recuperação durante reinicializações subsequentes a partir de um bloqueio de TPM.

A redefinição automática do bloqueio do TPM está desabilitada por padrão.

**Observação**  A redefinição automática do bloqueio do TPM só tem suporte em computadores que executam o TPM versão 1,2. O TPM 2,0 fornece funcionalidade interna de redefinição automática de bloqueio.

 

**O relatório de auditoria de recuperação** inclui eventos relacionados à redefinição automática do bloqueio do TPM. Se for feita uma solicitação do cliente MBAM para recuperar uma senha do OwnerAuth TPM, um evento será registrado para indicar a recuperação. As entradas de auditoria incluirão os seguintes eventos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Entradas</th>
<th align="left">Valor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Fonte de solicitação de auditoria</p></td>
<td align="left"><p>Desbloquear TPM de agente</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tipo de chave</p></td>
<td align="left"><p>Hash de senha TPM</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Descrição do motivo</p></td>
<td align="left"><p>Redefinição de TPM</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-secure-databases"></a>Conexões seguras com o SQL Server


No MBAM, o SQL Server se comunica com o SQL Server Reporting Services e com os serviços Web para o site de administração e monitoramento e o portal de autoatendimento. Recomendamos que você proteja a comunicação com o SQL Server. Para obter mais informações, consulte [criptografar conexões com o SQL Server](https://technet.microsoft.com/library/ms189067.aspx).

Para obter mais informações sobre como proteger os sites do MBAM, consulte [planejando como proteger os sites do MBAM](planning-how-to-secure-the-mbam-websites.md).

## <a href="" id="bkmk-accts-groups"></a>Criar contas e grupos


A prática recomendada para gerenciar contas de usuário é criar grupos globais de domínio e adicionar contas de usuário a eles. Para obter uma descrição das contas e dos grupos recomendados, consulte [planejando para MBAM 2,5 grupos e contas](planning-for-mbam-25-groups-and-accounts.md).

## <a href="" id="bkmk-logfiles"></a>Usar arquivos de log do MBAM


Esta seção descreve os arquivos de log do servidor MBAM e do cliente MBAM.

**Arquivos de log de instalação do MBAM Server**

O arquivo **MBAMServerSetup.exe** gera os seguintes arquivos de log na pasta **% Temp%** do usuário durante a instalação do MBAM:

-   **Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 Numbers &gt; . log**

    Registra as ações executadas durante a configuração do MBAM e a configuração do recurso do servidor MBAM.

-   **Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 \ _numbers &gt;\_0\_MBAMServer.msi. log**

    Registra a ação adicional tomada durante a instalação.

**Arquivos de log de configuração do MBAM Server**

-   **Logs de aplicativos e serviços/Microsoft Windows/MBAM-configuração**

    Registra os erros que ocorrem quando você está usando cmdlets do Windows PowerShell ou o assistente de configuração do servidor do MBAM para configurar os recursos do MBAM Server.

**Arquivos de log de configuração do cliente MBAM**

-   **MSI &lt; cinco caracteres aleatórios &gt; . log**

    Registra as ações executadas durante a instalação do cliente MBAM.

**MBAM-arquivos de log da Web**

-   Mostra a atividade nos serviços e portais da Web.

## <a href="" id="bkmk-tde"></a>Analisar considerações do TDE de banco de dados MBAM


O recurso de criptografia transparente de dados (TDE) que está disponível no SQL Server é uma instalação opcional para as instâncias de banco de dados que hospedam os recursos de banco de dados do MBAM.

Com o TDE, você pode executar a criptografia em nível de banco de dados completa em tempo real. O TDE é a melhor opção para a criptografia em massa para atender aos padrões de segurança de dados corporativos ou conformidade normativa. O TDE funciona no nível de arquivo, que é semelhante a dois recursos do Windows: o sistema de arquivos com criptografia (EFS) e a criptografia de unidade de disco BitLocker. Os dois recursos também criptografam dados no disco rígido. O TDE não substitui a criptografia, o EFS ou o BitLocker no nível da célula.

Quando o TDE está habilitado em um banco de dados, todos os backups são criptografados. Portanto, deve-se tomar cuidado especial para garantir que o certificado que foi usado para proteger a chave de criptografia do banco de dados tenha backup e seja mantido com o backup do banco de dados. Se esse certificado (ou certificados) for perdido, os dados serão ilegíveis.

Faça backup do certificado com o banco de dados. Cada backup de certificado deve ter dois arquivos. Esses dois arquivos devem ser arquivados. Idealmente para segurança, o backup deve ser feito separadamente do arquivo de backup do banco de dados. Você também pode considerar o uso do recurso EKM (gerenciamento de chaves extensível) (consulte gerenciamento extensível de chaves) para armazenamento e manutenção de chaves usadas para o TDE.

Para obter um exemplo de como habilitar o TDE para instâncias de banco de dados do MBAM, consulte [noções básicas sobre criptografia de dados transparente (TDE)](https://technet.microsoft.com/library/bb934049.aspx).

## <a href="" id="bkmk-general-security"></a>Entender as considerações gerais de segurança


**Compreender os riscos de segurança.** O risco mais sério quando você usa a administração e o monitoramento do Microsoft BitLocker é que sua funcionalidade pode ser comprometida por um usuário não autorizado que poderia reconfigurar a criptografia de unidade de disco BitLocker e obter dados de chave de criptografia BitLocker em clientes do MBAM. No entanto, a perda de funcionalidade do MBAM por um curto período de tempo, devido a um ataque de negação de serviço, geralmente não tem um impacto catastrófico, ao contrário, por exemplo, perda de comunicação de emails ou de rede ou de energia.

**Proteja seus computadores fisicamente**. Não há segurança sem segurança física. Um invasor que obtém acesso físico a um servidor MBAM pode usá-lo para atacar toda a base de clientes. Todos os possíveis ataques físicos devem ser considerados de alto risco e diminuídos adequadamente. Os servidores MBAM devem ser armazenados em uma sala de servidor seguro com acesso controlado. Proteja esses computadores quando os administradores não estiverem fisicamente presentes fazendo com que o sistema operacional trave o computador ou usando um protetor de tela seguro.

**Aplicar as atualizações de segurança mais recentes a todos os computadores**. Mantenha-se informado sobre novas atualizações para sistemas operacionais Windows, SQL Server e MBAM assinando o serviço de notificação de segurança no [TechCenter de segurança](https://go.microsoft.com/fwlink/?LinkId=28819).

**Use senhas fortes ou frases secretas**. Sempre use senhas fortes com 15 caracteres ou mais para todas as contas de administrador do MBAM. Nunca use senhas em branco. Para obter mais informações sobre os conceitos de senha, consulte [política de senha](https://technet.microsoft.com/library/hh994572.aspx).



## Tópicos relacionados


[Planejando a implantação do MBAM 2.5](planning-to-deploy-mbam-25.md)

 
## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





