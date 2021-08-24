---
title: Solução de problemas de instalação do MBAM 2.5
description: Apresentando como solucionar problemas de instalação do MBAM 2.5.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: 6ea152792801c630fa365f37d1668d1a4d84b3a5
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910626"
---
# <a name="troubleshooting-mbam-25-installation-problems"></a>Solução de problemas de instalação do MBAM 2.5

Este artigo apresenta como solucionar problemas de instalação do Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 em uma configuração autônoma.

## <a name="referring-mbam-log-files-for-troubleshooting"></a>Referindo-se a arquivos de log do MBAM para solução de problemas

O MBAM inclui o registro em log para instalação do servidor, instalação do cliente e eventos. Esse log deve ser chamado para solução de problemas. 
 
### <a name="mbam-server-installation-log-files"></a>Arquivos de log de instalação do servidor MBAM

MBAMServerSetup.exe gera os seguintes arquivos de log na pasta %temp% do usuário durante a instalação do MBAM:<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14 números>.log**

MBAMServerSetup.exe registra as ações que foram tomadas durante a instalação do MBAM e a instalação do recurso do servidor MBAM:<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers>_0_MBAMServer.msi.log**

MBAMServerSetup.exe registra ações adicionais que foram tomadas durante a instalação.

### <a name="mbam-client-installation-log-file"></a>Arquivo de log de instalação do cliente MBAM

A instalação do cliente é registrada no arquivo de log a seguir na pasta %temp% (ou em um local personalizado, dependendo de como o cliente foi instalado): <br />**MSI \<five random characters\> .log**

Esse log contém as ações que são tomadas durante a instalação do cliente MBAM.
 
### <a name="mbam-client-event-logging-channel"></a>Canal de registro em log de eventos do cliente MBAM

O MBAM tem canais separados de registro em log de eventos. Os arquivos de log Admin, Analytical e Operational estão localizados no Visualizador de Eventos, em **Application and Services Logs**  >  **microsoft**  >  **Windows**  >  **MBAM**.

A tabela a seguir fornece uma breve descrição de cada log de eventos.
 
|Log de eventos| Descrição|
|----------|-------|
|Microsoft-Windows-MBAM/Admin|  Contém mensagens de erro|
|Microsoft-Windows-MBAM/Analytic|   Contém informações de registro em log avançadas|
|Microsoft-Windows-MBAM/Operacional|    Contém mensagens de sucesso|

### <a name="mbam-server-event-logging-channel"></a>Canal de registro em log de eventos do servidor MBAM

Os arquivos de log estão localizados no Visualizador de Eventos, em **Application and Services Logs**  >  **Microsoft**  >  **Windows**  >  **MBAM**. A tabela a seguir inclui logs de eventos do servidor que foram introduzidos no MBAM 2.5:

|Log de eventos| Descrição|
|--------|-------------|
|Microsoft-Windows-MBAM/Admin|  Contém mensagens de erro|
|Microsoft-Windows-MBAM/Analytic|   Contém informações de registro em log avançadas|
|Microsoft-Windows-MBAM/Operacional|    Contém mensagens de sucesso|

### <a name="mbam-web-service-logs"></a>Logs de serviço Web do MBAM

Cada log de serviço Web do MBAM grava informações de registro em log em um arquivo SVCLOG. Por padrão, cada serviço Web grava o arquivo de rastreamento em uma pasta que usa seu nome na pasta C:\inetpub\Microsoft BitLocker Management Solution\Logs.

Você pode usar a ferramenta visualizador de rastreamento de serviço (parte do Microsoft Visual Studio) para analisar os rastreamentos de svclog.

## <a name="troubleshooting-encryption-and-reporting-issues"></a>Solução de problemas de criptografia e relatórios

Esta seção contém informações de solução de problemas para funcionalidade do servidor, funcionalidade do cliente, configurações e problemas conhecidos:
 
### <a name="mbam-client-installation-group-policy-settings"></a>Instalação do cliente MBAM, configurações de Política de Grupo

Determine se o agente MBAM está instalado no computador cliente. Quando o MBAM é instalado, ele cria um serviço chamado Serviço de Cliente de Gerenciamento do BitLocker. Esse serviço é configurado para iniciar automaticamente. Determine se o serviço está em execução.

Certifique-se de que as configurações da Política de Grupo do MBAM sejam aplicadas no computador cliente. A seguinte sub-chave do Registro será criada se as configurações da Política de Grupo foram aplicadas no computador cliente: **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

Verifique se essa chave existe e é preenchida usando valores por configurações de Política de Grupo.

### <a name="mbam-agent-in-the-initial-delay-period"></a>Agente MBAM no período de atraso inicial

O cliente MBAM não inicia a operação imediatamente após a instalação. Há um atraso aleatório inicial de 1 a 18 minutos antes de o Agente MBAM iniciar sua operação. Além do atraso inicial, há um atraso de pelo menos 90 minutos. (O atraso depende das configurações da Política de Grupo configuradas para a frequência de verificação do status do cliente.) Portanto, o atraso total antes de um cliente iniciar a operação é o *atraso aleatório*da verificação de frequência  +  *do cliente*.

Se os logs de eventos Operacional e Administrador estão em branco, o cliente ainda não iniciou a operação e está no período de atraso mencionado anteriormente. Se você quiser ignorar o atraso, siga estas etapas:
 
1. Pare o serviço de Serviço de Cliente de Gerenciamento do BitLocker.

2. Na ** sub-HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM** do Registro, crie o valor do Registro **NoStartupDelay,** desfize seu tipo como **REG_DWORD**e, em seguida, de definir seu valor **como 1**.

3. Em **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement, **de definir **os valores ClientWakeupFrequency** e **StatusReportingFrequency** **como 1**. Esses valores serão revertidos para suas configurações originais depois que as atualizações da Política de Grupo estão no computador.

4. Inicie o serviço de Serviço de Cliente de Gerenciamento do BitLocker.

Depois que o serviço for iniciado, se você fizer logoff localmente no computador e não houver erros, receberá uma solicitação para criptografar o computador em um minuto. Se você não receber uma solicitação, revise os logs de administrador do MBAM para ver se há entradas de erro.

### <a name="computer-does-not-have-a-tpm-device-or-the-tpm-device-is-not-enabled-in-the-bios"></a>O computador não tem um dispositivo TPM ou o dispositivo TPM não está habilitado no BIOS

Revise o log de eventos do Administrador do MBAM. Você verá uma entrada de evento que se parece com o seguinte no log de eventos administrador do MBAM:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 12:31:10 PM
    Event ID:      9
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    The TPM hardware is missing.
    TPM is needed to encrypt the operating system drive with any TPM protector.

Abra o Gerenciamento do TPM (tpm.msc) e verifique se o computador tem um dispositivo TPM. Se o tpm.msc não mostrar um dispositivo, abra o Gerenciador de Dispositivos (devmgmt.msc) e verifique se há um Módulo de Plataforma Confiável em Dispositivos de Segurança. Se você não vir um dispositivo Trusted Platform Module, isso pode ser verdadeiro por um dos seguintes motivos:

* Seu sistema não tem um dispositivo TPM/Security (Trusted Platform Module).

* O dispositivo TPM está desabilitado no BIOS.

* O dispositivo TPM está habilitado no BIOS, mas o gerenciamento do dispositivo TPM a partir da configuração do sistema operacional está desabilitado no BIOS.

* Você não está usando um driver da Microsoft para o dispositivo TPM. Revise os dispositivos listados no gerenciador de dispositivos para identificar o driver de dispositivo do Microsoft TPM.

Se o dispositivo TPM não estiver usando o driver C:\Windows\System32\tpm.sys, você deverá atualizar o driver selecionando o arquivo C:\Windows\Inf\tpm.inf.

### <a name="computer-does-not-have-a-valid-system-partition"></a>O computador não tem uma partição SYSTEM válida

Revise o log de eventos do Administrador do MBAM. Você verá uma entrada de evento que se parece com o seguinte no log de eventos administrador do MBAM:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:37 AM
    Event ID:      8
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTESTVM.xtremelabs.com
    Description:
    The system volume is missing.
    SystemVolume is needed to encrypt the operating system drive.

O BitLocker requer uma partição SYSTEM para habilitar a criptografia ( Criptografia de Unidade do BitLocker no Windows[7: Perguntas frequentes](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).

O MBAM não cria a partição do sistema automaticamente. Você pode usar o utilitário de preparação de unidade do BitLocker (bdehdcfg.exe) para criar a partição do sistema e mover os arquivos de inicialização necessários.

Por exemplo, você pode usar o comando **%windir%\system32\bdeHdCfg.exe -target padrão -size 300 –quiet** para preparar a unidade silenciosamente antes de implantar o MBAM para criptografar as unidades. Isso requer uma reinicialização. Você também pode roteá-la se isso for necessário. O documento a seguir descreve a Ferramenta de Preparação da Unidade bitLocker:

[Descrição da Ferramenta de Preparação de Unidade do BitLocker](https://support.microsoft.com/help/933246)

### <a name="drives-are-not-formatted-to-have-a-compatible-file-system"></a>As unidades não são formatadas para ter um sistema de arquivos compatível

Consulte o [artigo technet para requisitos do sistema de arquivos para BitLocker](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements).

### <a name="group-policy-conflict"></a>Conflito de Política de Grupo

Você verá uma entrada de evento que se parece com o seguinte no log de eventos administrador do MBAM:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/25/2013 9:27:58 PM
    Event ID:      22
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Detected Fixed Data Drive volume encryption policies conflict.
    Check BitLocker and MBAM policies related to FDD drive protectors.

Verifique as configurações da Política de Grupo para garantir que você não tenha uma configuração conflitante entre as configurações da Política de Grupo do MBAM.

Você deve configurar a Política de Grupo usando o modelo MDOP MBAM e não o modelo de Criptografia de Unidade do BitLocker.

Por exemplo:

Em Configurações de criptografia de unidade do sistema operacional, você selecionou o TPM como o protetor e também selecionou Permitir PINs avançados **para inicialização.** Essas são configurações conflitantes porque a proteção somente TPM não exige um PIN. Portanto, você deve desabilitar a configuração de PINs aprimorados.

### <a name="user-may-have-requested-an-exemption"></a>O usuário pode ter solicitado uma isenção

Se você habilitar a configuração do computador\Modelos Administrativos\Windows Components\MDOP MBAM (Gerenciamento do BitLocker)\Gerenciamento de Cliente\Configurar a política de grupo de isenção do usuário, os usuários terão a opção de solicitar uma isenção.

Por padrão, se o usuário solicitar uma isenção, a isenção será válida por 7 dias e o usuário não receberá prompts para criptografar durante esse período. (O valor padrão pode ser aumentado ou reduzido durante a configuração da política.) Após o fim do período de isenção, o usuário é solicitado a criptografar.

Você verá a seguinte entrada no log de eventos administrador do MBAM quando um computador estiver sob isenção do usuário:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 3:06:40 PM
    Event ID:      13
    Task Category: None
    Level:         Warning
    Keywords:      
    User:          SYSTEM
    Computer:      MBAMCLIENT.contoso.com
    Description:
    The user is exempt from encryption.

Se você deseja substituir manualmente a isenção do usuário para um computador, siga estas etapas:
 
1. De definir o valor AllowUserExemption como **0** na seguinte sub-chave do Registro: <br />
**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

2. Exclua todos os valores do Registro na seguinte sub-chave do Registro, exceto **Para AgentVersion,** **EncodedComputerName**e **Installed**:<br />
**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM**

    **Observação** Você deve reiniciar o agente MBAM para que as alterações entre em vigor.

Esteja ciente de que, depois de aplicar a Política de Grupo ao computador, esses valores poderão ser revertidos para suas configurações originais.

### <a name="wmi-issue"></a>Problema WMI

O MBAM usa métodos da classe win32_encryptablevolume para gerenciar o BitLocker. Se esse módulo estiver sem registro ou corrompido, o cliente MBAM não funcionará corretamente e você verá a seguinte entrada de evento no log de eventos do Administrador do MBAM:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/27/2013 11:18:51 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTEST.xtremelabs.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x80041016 
    Details:
    NULL

Além disso, você pode observar que as políticas de Recuperação e Hardware não se aplicam ao Código de Erro 0x8007007e. Isso se traduz em "O módulo especificado não pôde ser encontrado".

Para resolver esse problema, você deve recadastrar **a classe win32_encryptablevolume** usando o seguinte comando:

```cmd
mofcomp c:\Windows\System32\wbem\win32_encryptablevolume.mof
```

## <a name="troubleshooting-mbam-agent-communication-issues"></a>Solução de problemas de comunicação do Agente do MBAM

Esta seção contém informações de solução de problemas para os seguintes problemas relacionados à comunicação do agente MBAM:

### <a name="incorrect-mbam-service-url"></a>URL de serviço MBAM incorreta

Se o valor do Serviço de Status de Conformidade do MBAM ou do Serviço de Recuperação e Hardware estiver incorreto, você verá uma entrada de evento que se parece com o seguinte no log de eventos do Administrador do MBAM no computador cliente:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:36 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:33 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

Verifique os valores **de KeyRecoveryServiceEndPoint** e **StatusReportingServiceEndpoint** na seguinte sub-chave do Registro no computador cliente: <br />
**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

Por padrão, a URL de KeyRecoveryServiceEndPoint (ponto de extremidade de serviço de Recuperação e Hardware do MBAM) está no seguinte formato: <br />
**http:// \<servername\> : \<port\> /MBAMRecoveryAndHardwareService/CoreService.svc**

Por padrão, a URL para StatusReportingServiceEndpoint (ponto de extremidade do serviço de relatório de Status do MBAM) está no seguinte formato:<br />
**http:// : \<servername\> \<port\> /MBAMComplianceStatusService/StatusReportingService.svc**

> [!Note]
> Não deve haver espaços na URL.

Se a URL do serviço estiver incorreta, você deverá corrigir a URL do serviço na seguinte configuração de Política de Grupo:

**Configuração do computador**  >  **Políticas**  >  **Modelos Administrativos**  >  **Windows componentes**  >  **MDOP MBAM (Gerenciamento do BitLocker)**  >  **Gerenciamento de Cliente**  >  **Configurar o MBAM Services**

### <a name="connectivity-issue-that-affects-the-mbam-administration-server"></a>Problema de conectividade que afeta o servidor de administração do MBAM

O agente do MBAM não poderá postar atualizações no banco de dados se existirem problemas de conectividade entre o agente cliente e o servidor de administração do MBAM. Nesse caso, você observará entradas de falha de conectividade no log de eventos administrador do MBAM no computador cliente:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 18:21:22
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.
 
    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 23:06:48
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0006 
    Details:
    The operation did not complete within the time allotted.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          02-09-2013 02:02:04
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.

Verificações básicas:

* Verifique a conectividade básica pingando o servidor de administração do MBAM por nome e IP. Verifique se você pode se conectar ao site de administração do MBAM ou porta de serviço usando telnet ou portqry.

* Verifique se o serviço do IIS está sendo executado no servidor de administração e monitoramento do MBAM e se o serviço Web do MBAM está escutando na mesma porta configurada no computador cliente do MBAM ( `netstat –ano | find "portnumber"` ).

* Verifique se o número de porta configurado para o site do MBAM está usando o Gerenciador do IIS (inetmgr). Certifique-se de que o número da porta seja igual ao número da porta no qual o cliente está escutando. Certifique-se de que o número da porta não seja compartilhado por outro aplicativo. Por exemplo, outro aplicativo no servidor não deve usar a mesma porta.

* Se houver um firewall, certifique-se de que a porta está aberta no firewall ou no servidor proxy.

* Se a comunicação entre cliente e servidor estiver segura, certifique-se de que você está usando um certificado SSL válido.

* Verifique a conectividade de rede entre o servidor Web e o servidor de banco de dados para o qual os dados são enviados para inserção. Você pode verificar a conectividade do banco de dados do servidor Web para o servidor de banco de dados usando o Administrador de Fonte de Dados ODBC. Informações detalhadas SQL Server solução de problemas de conexão estão disponíveis em Como solucionar problemas de conexão [com o SQL Server Mecanismo de Banco de Dados](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).

#### <a name="troubleshooting-the-connectivity-issue"></a>Solução de problemas do problema de conectividade

Certifique-se de que a URL de serviço configurada no cliente está correta. Copie o valor da URL de KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**) do Registro e abra-o no Internet Explorer.

Da mesma forma, copie o valor da URL para StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**) e abra-o no Internet Explorer.

> [!Note]
> Se você não puder navegar até a URL do computador cliente, teste a conectividade de rede básica do cliente para o servidor que está executando o IIS. Consulte os pontos 1, 2, 3 e 4 na seção anterior.

Além disso, revise os logs de aplicativo no servidor de administração e monitoramento para ver se há erros.

Você pode fazer um rastreamento de rede simultâneo entre o cliente e o servidor e analisar o rastreamento para determinar a causa da falha de conexão entre o agente cliente e o servidor de administração do MBAM.

> [!Note]
> Se você puder navegar até as URLs de serviço do computador cliente e houver entradas de erro de conectividade nos logs de eventos de administrador do MBAM, isso pode ser devido a uma falha de conectividade entre o servidor de administração e o servidor de banco de dados.

Se você puder navegar com êxito para URLs de serviço e houver conectividade entre o cliente e o servidor em execução, o IIS está funcionando. No entanto, pode haver um problema na comunicação entre o servidor que está executando o IIS e o servidor de banco de dados.

Os serviços do MBAM podem não conseguir se conectar ao servidor de banco de dados devido a um problema de rede ou uma configuração incorreta de cadeia de caracteres de conexão de banco de dados. Revise os logs de aplicativo no servidor de administração e monitoramento. Você pode ver entradas de erros ou avisos da fonte ASP.NET 2.0.50727.0 que se parecem com a seguinte entrada de log:

    Log Name:      Application
    Source:        ASP.NET 2.0.50727.0
    Date:          7/11/2013 6:16:34 PM
    Event ID:      1310
    Task Category: Web Event
    Level:         Warning
    Keywords:      Classic
    User:          N/A
    Computer:      MBAM2-Admin.contoso.com
    Description:
    Event code: 100001
    Event message: SQL error occurred
    Event time: 7/11/2013 6:16:34 PM
    Event time (UTC): 7/11/2013 12:46:34 PM
    Event ID: 6615fb8eb9d54e778b933d5bb7ca91ed
    Event sequence: 2
    Event occurrence: 1
    Event detail code: 0 
    Application information:
        Application domain: /LM/W3SVC/2/ROOT/MBAMAdministrationService-1-130180202570338699
        Trust level: Full
        Application Virtual Path: /MBAMAdministrationService
        Application Path: C:\inetpub\Microsoft BitLocker Management Solution\Administration Service\
        Machine name: MBAM2-ADMIN 
    
    Process information:
        Process ID: 1940
        Process name: w3wp.exe
        Account name: NT AUTHORITY\NETWORK SERVICE 
    
    Exception information:
        Exception type: SqlException
        Exception message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server) 
    
    Request information:
        Request URL: 
        Request path: 
        User host address: 
        User: 
        Is authenticated: False
        Authentication Type: 
        Thread account name: NT AUTHORITY\NETWORK SERVICE 
    
    Thread information:
        Thread ID: 7
        Thread account name: NT AUTHORITY\NETWORK SERVICE
        Is impersonating: False
        Stack trace:    at System.Data.SqlClient.SqlInternalConnection.OnError(SqlException exception, Boolean breakConnection)
       at System.Data.SqlClient.TdsParser.ThrowExceptionAndWarning(TdsParserStateObject stateObj)
       at System.Data.SqlClient.TdsParser.Connect(ServerInfo serverInfo, SqlInternalConnectionTds connHandler, Boolean ignoreSniOpenTimeout, Int64 timerExpire, Boolean encrypt, Boolean trustServerCert, Boolean integratedSecurity, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.AttemptOneLogin(ServerInfo serverInfo, String newPassword, Boolean ignoreSniOpenTimeout, Int64 timerExpire, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.LoginNoFailover(String host, String newPassword, Boolean redirectedUserInstance, SqlConnection owningObject, SqlConnectionString connectionOptions, Int64 timerStart)
       at System.Data.SqlClient.SqlInternalConnectionTds.OpenLoginEnlist(SqlConnection owningObject, SqlConnectionString connectionOptions, String newPassword, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlInternalConnectionTds..ctor(DbConnectionPoolIdentity identity, SqlConnectionString connectionOptions, Object providerInfo, String newPassword, SqlConnection owningObject, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlConnectionFactory.CreateConnection(DbConnectionOptions options, Object poolGroupProviderInfo, DbConnectionPool pool, DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionFactory.CreatePooledConnection(DbConnection owningConnection, DbConnectionPool pool, DbConnectionOptions options)
       at System.Data.ProviderBase.DbConnectionPool.CreateObject(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.UserCreateRequest(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.GetConnection(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionFactory.GetConnection(DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionClosed.OpenConnection(DbConnection outerConnection, DbConnectionFactory connectionFactory)
       at System.Data.SqlClient.SqlConnection.Open()
       at System.Data.Linq.SqlClient.SqlConnectionManager.UseConnection(IConnectionUser user)
       at System.Data.Linq.SqlClient.SqlProvider.get_IsSqlCe()
       at System.Data.Linq.SqlClient.SqlProvider.InitializeProviderMode()
       at System.Data.Linq.SqlClient.SqlProvider.System.Data.Linq.Provider.IProvider.Execute(Expression query)
       at System.Data.Linq.DataContext.ExecuteMethodCall(Object instance, MethodInfo methodInfo, Object[] parameters)
       at Microsoft.Mbam.Server.ServiceCommon.KeyRecoveryModelDataContext.GetRecoveryKeyIds(String partialRecoveryKeyId, String reason)
       at Microsoft.Mbam.ApplicationSupportService.AdministrationService.GetRecoveryKeyIds(String partialRecoveryKeyId, String reasonCode)
    
    Custom event details:
        Application: MBAMAdministrationService
        Sql Server:
        Database: MBAM Recovery and Hardware
        Database: MBAM Compliance Status
        Sql ErrorCode: 5
        Error Message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)

#### <a name="possible-causes"></a>Possíveis causas

##### <a name="cause-1"></a>Causa 1

O administrador pode ter especificado um nome de instância de banco de dados inválido/nome do banco de dados durante a instalação dos componentes do servidor de administração e monitoramento.

Você pode verificar e corrigir as cadeias de conexão de banco de dados usando o console de Gerenciamento do IIS. Para fazer isso, abra o Gerenciador do IIS e navegue até Microsoft BitLocker Administration and Monitoring. Para cada serviço listado no lado esquerdo, siga estas etapas para alterar as cadeias de caracteres de conexão do banco de dados:

1. Em **Exibição de Recursos,** selecione duas vezes **Cadeias de Caracteres de Conexão**.

2. Na página **Cadeias de** Conexão, selecione a cadeia de caracteres de conexão que você deseja alterar.

3. No painel **Ações,** selecione **Editar**.

4. Na caixa **de diálogo Editar Cadeia de** Caracteres de Conexão, altere as propriedades que você deseja alterar e selecione **OK**.

##### <a name="cause-2"></a>Causa 2

SQL Server porta bloqueada no firewall. Verifique o número de porta para o qual SQL Server está configurado para ouvir e verifique se a porta está aberta no firewall entre o servidor de administração e o servidor de banco de dados.

##### <a name="cause-3"></a>Causa 3

Vinculações TCP/IP SQL servidor incorretos. Verifique SQL vínculos TCP/IP no SQL Server Configuration Manager no servidor de banco de dados. O MBAM exige que os protocolos TCP/IP e Pipes nomeados sejam habilitados para se conectar ao banco de dados.

##### <a name="cause-4"></a>Causa 4

A conta do NT Authority\Network Service ou a conta do computador do SERVIDOR de Administração do MBAM não têm as permissões necessárias para se conectar ao banco de dados SQL de dados.

Durante a instalação de componentes de banco de dados no servidor de banco de dados, o instalador cria dois grupos locais: MBAM Compliance Auditing DB Access e MBAM Recovery e Hardware DB Access.

A conta do NT Authority\Network Service, a conta do computador do servidor de administração do MBAM e o usuário que instala os componentes do banco de dados são adicionados automaticamente a esses grupos.

Esses grupos têm as permissões necessárias no banco de dados durante a instalação. Todos os usuários que fazem parte desse grupo recebem automaticamente as permissões necessárias no banco de dados.

O serviço Web pode não se conectar ao servidor de banco de dados devido a um problema de permissões se uma ou mais das seguintes condições são verdadeiras:

* Os grupos mencionados anteriormente são removidos dos grupos locais no servidor de banco de dados.

* A conta do NT Authority\Network Service e a conta do computador do servidor de administração do MBAM não são membros desses grupos.

* Esses grupos não têm as permissões necessárias no banco de dados.

Você observará erros relacionados a permissões nos logs de aplicativo no servidor de administração e monitoramento do MBAM se qualquer uma das condições anteriores for verdadeira. Nesse caso, você deve adicionar manualmente a conta do NT Authority\Network Service e a conta do computador do servidor de administração do MBAM e conceder a eles uma função pública em todo o servidor no servidor de banco de dados SQL que está usando SQL Server Management Studio ( https://msdn.microsoft.com/library/aa337562.aspx) .

#### <a name="review-the-web-service-logs"></a>Revisar os logs do serviço Web

Se nenhum evento for registrado nos logs de aplicativo no servidor de administração do MBAM, é hora de revisar os logs de serviço web (.svclog) do serviço Web do MBAM hospedado no servidor de administração e monitoramento do MBAM. Você terá que usar a Ferramenta do Visualizador de Rastreamento de Serviço (SvcTraceViewer.exe) para https://msdn.microsoft.com/library/ms732023.aspx exibir o arquivo de log.

Você deve investigar principalmente os logs de rastreamento de serviço de RecoveryandHardwareService e ComplianceStatusService. Por padrão, os logs de serviço web estão localizados na pasta C:\inetpub\Microsoft BitLocker Management Solution\Logs. Lá, cada serviço grava seu arquivo .svclog em sua própria pasta.

Revise a atividade no log de rastreamento de serviço para ver se há entradas de erro ou aviso. Por padrão, as entradas de erro são realçadas em vermelho. Selecione a descrição de erro no painel direito do visualizador de rastreamento para exibir informações detalhadas sobre a entrada de erro. Veja a seguir uma entrada de erro de exemplo do log de rastreamento:

    <E2ETraceEvent xmlns="http://schemas.microsoft.com/2004/06/E2ETraceEvent">
    <System xmlns="http://schemas.microsoft.com/2004/06/windows/eventlog/system">
    <EventID>15183</EventID>
    <Type>3</Type>
    <SubType Name="Error">0</SubType>
    <Level>2</Level>
    <TimeCreated SystemTime="2013-07-05T14:48:06.2821550Z" />
    <Source Name="Microsoft.Mbam.CoreService" />
    <Correlation ActivityID="{00000000-0000-0000-0000-000000000000}" />
    <Execution ProcessName="w3wp" ProcessID="4332" ThreadID="11" />
    <Channel />
    <Computer>XXXXXXXXXXX</Computer>
    </System>
    <ApplicationData>AddUpdateVolume: While executing sql transaction for add volume to store exception occurred Key Recovery Data Store processing error: Violation of UNIQUE KEY constraint 'UniqueRecoveryKeyId'. Cannot insert duplicate key in object 'RecoveryAndHardwareCore.Keys'. The duplicate key value is (8637036e-b379-4798-bd9e-5a0b36296de3).
    </ApplicationData>
    </E2ETraceEvent>

## <a name="re-installation-or-reconfiguration-of-mbam-infrastructure"></a>Nova instalação ou reconfiguração da infraestrutura do MBAM

Para instalar ou reconfigurar a infraestrutura do MBAM, você deve saber as seguintes coisas:

* Conta do Pool de Aplicativos

* Grupos MBAM (Helpdesk, Advanced, Report Users Group)

* URL de relatórios mbam

* SQL Server nome e nomes de banco de dados

* Contas ReadWrite e ReadOnly do MBAM

### <a name="application-pool-account"></a>Conta do Pool de Aplicativos

Para encontrar a conta do Pool de Aplicativos, faça logoff no Servidor Web do MBAM, abra o Gerenciador Serviços de Informações da Internet **(IIS)** e selecione **Pools de Aplicativos**:

![pools de aplicativos.](images/troubleshooting-MBAM-installation-1.png)

O Nome da Entidade de Serviço (SPN) deve ser definido nesta conta. Essa configuração é muito importante para a funcionalidade do MBAM.

### <a name="mbam-groups-helpdesk-advanced-report-users-group-and-reports-url"></a>Grupos mbam (Helpdesk, Advanced, Report Users Group and Reports URL)

![Grupos MBAM.](images/troubleshooting-MBAM-installation-2.png)

Isso fornece informações como Grupo de Ajuda, Grupo de Ajuda Avançada, Grupo de Usuários de Relatório e URL de Relatórios do MBAM. A URL de Relatórios do MBAM deve ser fornecida na configuração do MBAM e deve ser lida como: http(s)://servername/ReportServer.

### <a name="sql-server-name-and-database-db-names"></a>SQL Server nome e banco de dados (DB)

Para encontrar os SQL Server e instâncias que hospedam os DBs do MBAM, faça logoff no servidor do MBAM Web (IIS) e navegue até a subchame de registro de acesso:

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web**

![Regedit.](images/troubleshooting-MBAM-installation-3.png)

As partes realçadas são cadeias de caracteres de conexão. Eles devem ter o nome SQL Server, nomes de banco de dados e instâncias (se nomeado).

### <a name="mbam-readwrite-and-readonly-accounts"></a>Contas do MBAM ReadWrite e ReadOnly

Essas informações estarão no banco de dados SQL Server, para o qual já encontramos o nome do servidor Web.

#### <a name="readwrite-account"></a>Conta ReadWrite

1. Faça logoff no SQL Management Studio.

2. Clique com o botão direito do mouse em Recuperação e Hardware do **MBAM,** selecione **Propriedades**e selecione **Permissões**.

Por exemplo, O nome da conta de laboratório é **MBAMWrite**. As contas Pool de Aplicativos e ReadWrite são definidas como as mesmas.

![SQL DB.](images/troubleshooting-MBAM-installation-4.png)

![Propriedades DB.](images/troubleshooting-MBAM-installation-5.png)

Navegue **até Segurança** e, em seguida, faça **logon** SQL Management Studio. Navegue até a conta mostrada na captura de tela anterior.

![SQL Segurança.](images/troubleshooting-MBAM-installation-6.png)

Clique com o botão direito do mouse nas contas, acesse **Mapeamento de Usuários**de Propriedades e localize o banco de dados de Recuperação e Hardware do MBAM:

![Mapeamento de Usuário.](images/troubleshooting-MBAM-installation-7.png)

#### <a name="readonly-account"></a>Conta ReadOnly

Abra SQL Server Reporting Services Configuration Manager no Servidor SSRS. Selecione **URL do Gerenciador de Relatório**e, em seguida, navegue pelas **URLs**:

![Gerente de Relatório.](images/troubleshooting-MBAM-installation-8.png)

Selecione **Administração e Monitoramento do Microsoft Bitlocker:**

![Administração e Monitoramento do Bitlocker.](images/troubleshooting-MBAM-installation-9.png)

Selecione **MaltaDatasource**:

![DBs.](images/troubleshooting-MBAM-installation-10.png)

![MaltaDatasource.](images/troubleshooting-MBAM-installation-11.png)

Os MaltaDataSource devem ter o nome da conta ReadOnly e devem ser usados na configuração do MBAM.

## <a name="reference"></a>Referência

Para obter mais informações, consulte os seguintes artigos:

[Implantando o MBAM 2.5 em uma configuração autônoma](https://support.microsoft.com/help/3046555)

[Microsoft BitLocker Administration and Monitoring 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/)
