---
title: Solução de problemas de instalação do MBAM 2.5
description: Apresentando como solucionar problemas de instalação do MBAM 2,5.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: ed56a87496e09601c44028b7f948eda39143e8c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796106"
---
# Solução de problemas de instalação do MBAM 2.5

Este artigo apresenta como solucionar problemas de instalação do Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 em uma configuração autônoma.

## Fazendo referência a arquivos de log do MBAM para solução de problemas

O MBAM inclui log para instalação do servidor, instalação do cliente e eventos. Este registro em log deve ser consultado para solução de problemas. 
 
### Arquivos de log de instalação do MBAM Server

MBAMServerSetup.exe gera os seguintes arquivos de log na pasta% Temp% do usuário durante a instalação do MBAM:<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14 números>. log**

MBAMServerSetup.exe registra as ações que foram feitas durante a instalação do MBAM e o recurso MBAM Server Feature:<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers # C1_0_MBAMServer.msi. log**

MBAMServerSetup.exe registra ações adicionais que foram executadas durante a instalação.

### Arquivo de log de instalação do cliente MBAM

A instalação do cliente é gravada no seguinte arquivo de log na pasta% temp% (ou em um local personalizado, dependendo de como o cliente foi instalado): <br />**MSI \<five random characters\> . log**

Esse log contém as ações que são executadas durante a instalação do cliente do MBAM.
 
### Canal de log de eventos do cliente MBAM

O MBAM tem canais de log de eventos separados. Os arquivos de log do administrador, analítico e operacional estão localizados no Visualizador de eventos, em **logs de aplicativos e serviços**  >  **Microsoft**  >  **Windows**  >  **MBAM**.

A tabela a seguir fornece uma breve descrição de cada log de eventos.
 
|Log de eventos| Descrição|
|----------|-------|
|Microsoft-Windows-MBAM/administrador|  Contém mensagens de erro|
|Microsoft-Windows-MBAM/analítica|   Contém informações de registro avançado|
|Microsoft-Windows-MBAM/operacional|    Contém mensagens de êxito|

### Canal de log de eventos do MBAM Server

Os arquivos de log estão localizados em Visualizador de eventos, em **logs de aplicativos e serviços**  >  **Microsoft**  >  **Windows**  >  **MBAM**. A tabela a seguir inclui logs de eventos do servidor que foram introduzidos no MBAM 2,5:

|Log de eventos| Descrição|
|--------|-------------|
|Microsoft-Windows-MBAM/administrador|  Contém mensagens de erro|
|Microsoft-Windows-MBAM/analítica|   Contém informações de registro avançado|
|Microsoft-Windows-MBAM/operacional|    Contém mensagens de êxito|

### Logs de serviços Web do MBAM

Cada log de serviço Web do MBAM grava as informações de registro em um arquivo SVCLOG. Por padrão, cada serviço Web grava o arquivo de rastreamento em uma pasta que usa seu nome na pasta C:\inetpub\Microsoft BitLocker Management Solution\Logs.

Você pode usar a ferramenta Visualizador de rastreamento de serviço (parte do Microsoft Visual Studio) para analisar os rastreamentos do svclog.

## Solução de problemas de criptografia e emissão de relatórios

Esta seção contém informações de solução de problemas para funcionalidade do servidor, funcionalidade do cliente, configurações e problemas conhecidos:
 
### Instalação do cliente do MBAM, configurações da política de grupo

Determine se o agente do MBAM está instalado no computador cliente. Quando o MBAM é instalado, ele cria um serviço denominado serviço de cliente de gerenciamento BitLocker. Este serviço é configurado para iniciar automaticamente. Determine se o serviço está em execução.

Verifique se as configurações de política de grupo do MBAM são aplicadas no computador cliente. A seguinte subchave do registro será criada se as configurações de política de grupo tiverem sido aplicadas no computador cliente: **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**

Verifique se essa chave existe e se está preenchida usando valores por configurações de política de grupo.

### Agente MBAM no período de atraso inicial

O cliente MBAM não inicia a operação imediatamente após a instalação. Há um atraso inicial aleatório de 1 – 18 minutos antes de o agente MBAM iniciar a operação. Além do atraso inicial, há um atraso de pelo menos 90 minutos. (O atraso depende das configurações de política de grupo que estão definidas para a frequência de verificação do status do cliente.) Portanto, o atraso total antes da operação de início do cliente é a demora de *inicialização aleatória*atraso da  +  *frequência de verificação do cliente*.

Se os logs de eventos de administração e operacionais estiverem em branco, o cliente ainda não iniciou a operação e estará no período de atraso mencionado anteriormente. Se você quiser ignorar o atraso, siga estas etapas:
 
1. Parar o serviço de serviço de cliente de gerenciamento BitLocker.

2. Na subchave do registro do **HKEY_LOCAL_MACHINE \software\microsoft\mbam** , crie o valor do registro **NoStartupDelay** , defina seu tipo como **REG_DWORD**e, em seguida, defina seu valor como **1**.

3. Em **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**, defina os valores **ClientWakeupFrequency** e **StatusReportingFrequency** como **1**. Esses valores retornarão às configurações originais depois que as atualizações de política de grupo estiverem no computador.

4. Inicie o serviço de serviço de cliente de gerenciamento BitLocker.

Depois que o serviço for iniciado, se você fizer logon localmente no computador e não houver erros, você deve receber uma solicitação para criptografar o computador dentro de um minuto. Se você não receber uma solicitação, analise os logs de administração do MBAM para obter as entradas de erro.

### O computador não tem um dispositivo TPM ou o dispositivo TPM não está habilitado no BIOS

Examine o log de eventos de administrador do MBAM. Você verá uma entrada de evento semelhante à seguinte no log de eventos de administração do MBAM:

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

Abra o gerenciamento TPM (TPM. msc) e verifique se o computador tem um dispositivo TPM. Se o TPM. msc não mostrar um dispositivo, abra o Gerenciador de dispositivos (devmgmt. msc) e verifique se há um módulo de plataforma confiável em dispositivos de segurança. Se você não vir um dispositivo de módulo de plataforma confiável, isso pode ser verdade por um dos seguintes motivos:

* Seu sistema não tem um dispositivo TPM/segurança (Trusted Platform Module).

* O dispositivo TPM está desabilitado no BIOS.

* O dispositivo TPM está habilitado no BIOS, mas o gerenciamento do dispositivo TPM da configuração do sistema operacional está desabilitado no BIOS.

* Você não está usando um driver da Microsoft para o dispositivo TPM. Examine os dispositivos listados no Gerenciador de dispositivos para identificar o driver de dispositivo TPM da Microsoft.

Se o dispositivo TPM não estiver usando o driver C:\Windows\System32\tpm.sys, você deverá atualizar o driver selecionando o arquivo C:\Windows\Inf\tpm.inf.

### O computador não tem uma partição de sistema válida

Examine o log de eventos de administrador do MBAM. Você verá uma entrada de evento semelhante à seguinte no log de eventos de administração do MBAM:

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

O BitLocker exige uma partição de sistema para habilitar a criptografia ([criptografia de unidade de disco BitLocker no Windows 7: perguntas frequentes](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).

O MBAM não cria a partição do sistema automaticamente. Você pode usar o utilitário de preparação de unidade BitLocker (bdehdcfg.exe) para criar a partição do sistema e mover os arquivos de inicialização necessários.

Por exemplo, você pode usar o comando **% windir% \system32\bdeHdCfg.exe-Target default-size 300 – Quiet** para preparar a unidade silenciosamente antes de implantar o MBAM para criptografar as unidades. Isso requer uma reinicialização. Você também pode criar um script para a ação caso isso seja necessário. O documento a seguir descreve a ferramenta de preparação de unidade de disco BitLocker:

[Descrição da ferramenta de preparação de unidade de disco BitLocker](https://support.microsoft.com/help/933246)

### As unidades não estão formatadas para ter um sistema de arquivos compatível

Consulte o [artigo do TechNet para requisitos do sistema de arquivos para o BitLocker](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements).

### Conflito de política de grupo

Você verá uma entrada de evento semelhante à seguinte no log de eventos de administração do MBAM:

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

Verifique as configurações da política de grupo para garantir que você não tenha uma configuração conflitante entre as configurações da política de grupo do MBAM.

Você deve configurar a política de grupo usando o modelo de MBAM do MDOP e não o modelo de criptografia de unidade de disco BitLocker.

Por exemplo:

Em configurações de criptografia de unidade de sistema operacional, você selecionou TPM como protetor e também **permite pinos aprimorados para inicialização**. Essas são configurações conflitantes porque a proteção somente TPM não requer um PIN. Portanto, você deve desabilitar a configuração de pinos aprimorados.

### O usuário pode ter solicitado uma isenção

Se você ativou a configuração do Computador\modelos Administrativos\Componentes do Components\MDOP MBAM (gerenciamento de BitLocker) \Client Management\Configure política de grupo da política de isenção de usuário, os usuários terão a opção de solicitar uma isenção.

Por padrão, se o usuário solicitar uma isenção, a isenção será válida por 7 dias e o usuário não receberá prompts para criptografar durante esse período. (O valor padrão pode ser aumentado ou diminuído durante a configuração da política.) Quando o período de isenção termina, o usuário é solicitado a criptografar.

Você verá a seguinte entrada no log de eventos de administrador do MBAM quando um computador estiver em isenção de usuário:

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

Se você quiser substituir manualmente a isenção do usuário de um computador, siga estas etapas:
 
1. Defina o valor AllowUserExemption como **0** na seguinte subchave do registro: <br />
**HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

2. Exclua todos os valores do registro na seguinte subchave do registro, exceto para **AgentVersion**, **EncodedComputerName**e **instalado**:<br />
**HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM**

    **Observação** Você deve reiniciar o agente MBAM para que as alterações entrem em vigor.

Lembre-se de que depois de aplicar a política de grupo ao computador, esses valores podem reverter às configurações originais.

### Problema do WMI

MBAM usa métodos da classe win32_encryptablevolume para gerenciar o BitLocker. Se esse módulo estiver cancelado ou corrompido, o cliente MBAM não funcionará corretamente, e você verá a seguinte entrada de evento no log de eventos de administração do MBAM:

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

Além disso, você pode observar que as políticas de recuperação e de hardware não se aplicam com o código de erro 0x8007007E. Isso é convertido em "o módulo especificado não foi encontrado".

Para resolver esse problema, você deve registrar novamente a classe **Win32_EncryptableVolume** usando o seguinte comando:

```cmd
mofcomp c:\Windows\System32\wbem\win32_encryptablevolume.mof
```

## Solução de problemas de comunicação do agente MBAM

Esta seção contém informações de solução de problemas para os seguintes problemas relacionados à comunicação do agente do MBAM:

### URL do serviço de MBAM incorreta

Se o valor do serviço de status de conformidade do MBAM ou do serviço de recuperação e de hardware estiver incorreto, você verá uma entrada de evento semelhante à seguinte no log de eventos de administração do MBAM no computador cliente:

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

Verifique os valores de **KeyRecoveryServiceEndPoint** e **StatusReportingServiceEndpoint** sob a seguinte subchave do registro no computador cliente: <br />
**HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

Por padrão, a URL para o KeyRecoveryServiceEndPoint (recuperação do MBAM e o ponto de extremidade do serviço de hardware) está no seguinte formato: <br />
**http:// \<servername\> : \<port\> /MBAMRecoveryAndHardwareService/CoreService.svc**

Por padrão, a URL para o ponto de extremidade do serviço de relatório de status do StatusReportingServiceEndpoint (MBAM status) está no seguinte formato:<br />
**http:// \<servername\> : \<port\> /MBAMComplianceStatusService/StatusReportingService.svc**

> [!Note]
> Não deve haver espaços na URL.

Se a URL do serviço estiver incorreta, você deverá corrigir a URL do serviço na seguinte configuração de política de Grupo:

**Configuração**  >  do computador **Regras**  >  de **Modelos administrativos**  >  **Componentes**  >  do Windows **MDOP MBAM (gerenciamento de BitLocker)**  >  **Gerenciamento**  >  de cliente **Configurar os serviços do MBAM**

### Problema de conectividade que afeta o servidor de administração do MBAM

O agente MBAM não poderá postar atualizações para o banco de dados se houver problemas de conectividade entre o agente cliente e o servidor de administração do MBAM. Nesse caso, você observará entradas de falha de conectividade no log de eventos de administrador do MBAM no computador cliente:

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

* Verifique a conectividade básica fazendo ping no servidor de administração do MBAM por nome e IP. Verifique se você pode se conectar ao site de administração do MBAM ou à porta de serviço usando o Telnet ou o Portqry.

* Verifique se o serviço IIS está em execução no servidor de administração e monitoramento do MBAM e se o serviço Web do MBAM está ouvindo na mesma porta que está configurada no computador cliente do MBAM ( `netstat –ano | find "portnumber"` ).

* Verifique se o número da porta que está configurado para o site do MBAM está usando o Gerenciador do IIS (inetmgr). Certifique-se de que o número da porta seja igual ao número da porta na qual o cliente está ouvindo. Certifique-se de que o número da porta não seja compartilhado por outro aplicativo. Por exemplo, outro aplicativo no servidor não deve estar usando a mesma porta.

* Se houver um firewall, certifique-se de que a porta esteja aberta no firewall ou servidor proxy.

* Se a comunicação entre o cliente e o servidor for segura, certifique-se de que você esteja usando um certificado SSL válido.

* Verifique a conectividade de rede entre o servidor Web e o servidor de banco de dados para o qual os dados são enviados para inserção. Você pode verificar a conectividade do banco de dados do servidor Web para o servidor de banco de dados usando o administrador de fonte de dados ODBC. As informações detalhadas de solução de problemas de conexão do SQL Server estão disponíveis em [como solucionar problemas de conexão com o mecanismo de banco de dados do SQL Server](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).

#### Solução de problemas do problema de conectividade

Verifique se a URL do serviço que está configurada no cliente está correta. Copie o valor da URL para KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**) a partir do registro e abra-o no Internet Explorer.

Da mesma forma, copie o valor da URL para StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**) e abra-o no Internet Explorer.

> [!Note]
> Se não conseguir navegar até a URL do computador cliente, você deve testar a conectividade de rede básica do cliente para o servidor que está executando o IIS. Veja os pontos 1, 2, 3 e 4 na seção anterior.

Além disso, examine os logs do aplicativo no servidor de administração e monitoramento em busca de erros.

Você pode fazer um rastreamento de rede simultânea entre o cliente e o servidor e examinar o rastreamento para determinar a causa da falha de conexão entre o agente cliente e o servidor de administração do MBAM.

> [!Note]
> Se você puder navegar para as URLs de serviço do computador cliente e houver entradas de erro de conectividade nos logs de eventos de administrador do MBAM, isso pode ser devido a uma falha de conectividade entre o servidor de administração e o servidor de banco de dados.

Se você conseguir navegar para as duas URLs de serviço e houver conectividade entre o cliente e o servidor que está em execução, o IIS está funcionando. No entanto, pode haver um problema em comunicação entre o servidor que está executando o IIS e o servidor de banco de dados.

Os serviços do MBAM podem não conseguir se conectar ao servidor de banco de dados devido a um problema de rede ou uma configuração de cadeia de conexão de banco de dados incorreta. Examine os logs do aplicativo no servidor de administração e monitoramento. Você pode ver erros de entrada ou avisos do 2.0.50727.0 de origem ASP.NET que se assemelham à seguinte entrada de log:

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

#### Possíveis causas

##### Causa 1

O administrador pode ter especificado um nome de instância de banco de dados/nome de banco de dados inválido durante a instalação dos componentes de servidor de administração e monitoramento.

Você pode verificar e corrigir as cadeias de conexão de banco de dados usando o console de gerenciamento do IIS. Para fazer isso, abra o Gerenciador do IIS e navegue até Administração e monitoramento do Microsoft BitLocker. Para cada serviço listado no lado esquerdo, siga estas etapas para alterar as cadeias de conexão do banco de dados:

1. No **modo de exibição recursos**, selecione duas **cadeias de conexão**.

2. Na página **cadeias de conexão** , selecione a cadeia de conexão que você deseja alterar.

3. No painel **ações** , selecione **Editar**.

4. Na caixa de diálogo **Editar Cadeia de conexão** , altere as propriedades que você deseja alterar e, em seguida, selecione **OK**.

##### Causa 2

Porta do SQL Server bloqueada no firewall. Verifique o número da porta para a qual o SQL Server está configurado para escuta e certifique-se de que a porta esteja aberta no firewall entre o servidor de administração e o servidor de banco de dados.

##### Causa 3

Associações TCP/IP do SQL Server incorretas. Verifique as associações de TCP/IP do SQL no Gerenciador de configuração do SQL Server no servidor de banco de dados. MBAM requer que os protocolos TCP/IP e pipes nomeados estejam habilitados para se conectar ao banco de dados.

##### Causa 4

A conta NT Authority\Network Service ou a conta de computador do servidor de administração do MBAM não tem as permissões necessárias para se conectar ao banco de dados SQL.

Durante a instalação dos componentes de banco de dados no servidor de banco de dados, o instalador cria dois grupos locais: MBAM conformidade auditando o acesso ao banco de dados e recuperação do MBAM e acesso ao banco de dados de hardware.

A conta NT Authority\Network Service, a conta de computador do servidor de administração do MBAM e o usuário que instala os componentes do banco de dados são automaticamente adicionados a esses grupos.

Esses grupos recebem as permissões necessárias no banco de dados durante a instalação. Todos os usuários que fazem parte deste grupo recebem automaticamente as permissões necessárias no banco de dados.

O serviço Web pode não se conectar ao servidor de banco de dados devido a um problema de permissões se uma ou mais das seguintes condições forem verdadeiras:

* Os grupos mencionados anteriormente são removidos dos grupos locais do servidor de banco de dados.

* A conta NT Authority\Network Service e a conta do computador do servidor de administração do MBAM não são membros desses grupos.

* Esses grupos não têm as permissões necessárias no banco de dados.

Você notará erros relacionados a permissões nos logs do aplicativo na administração do MBAM e no servidor de monitoramento se qualquer uma das condições anteriores forem verdadeiras. Nesse caso, você deve adicionar manualmente a conta NT Authority\Network Service e a conta de computador do servidor de administração do MBAM e conceder a elas uma função pública em todo o servidor no servidor de banco de dados SQL que está usando o SQL Server Management Studio ( https://msdn.microsoft.com/library/aa337562.aspx) .

#### Examine os logs do serviço Web

Se nenhum evento for registrado nos logs do aplicativo no servidor de administração do MBAM, é hora de analisar os logs do serviço Web (. svclog) do serviço Web MBAM hospedado no servidor de administração e monitoramento do MBAM. Você precisará usar a ferramenta Visualizador de rastreamento de serviço (SvcTraceViewer.exe) https://msdn.microsoft.com/library/ms732023.aspx para exibir o arquivo de log.

Você deve investigar principalmente os logs de rastreamento de serviço do RecoveryandHardwareService e do ComplianceStatusService. Por padrão, os logs do serviço Web estão localizados na pasta Solution\Logs C:\inetpub\Microsoft de gerenciamento do BitLocker. Nesse caso, cada serviço grava o arquivo. svclog em sua própria pasta.

Examine a atividade no log de rastreamento do serviço em busca de erros ou entradas de aviso. Por padrão, as entradas de erro são realçadas em vermelho. Selecione a descrição do erro no painel direito do Visualizador de rastreamento para ver informações detalhadas sobre a entrada de erro. Veja a seguir um exemplo de entrada de erro do log de rastreamento:

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

## Reinstalação ou reconfiguração da infraestrutura do MBAM

Para reinstalar ou reconfigurar a infraestrutura do MBAM, você deve conhecer os seguintes itens:

* Conta do pool de aplicativos

* Grupos do MBAM (assistência técnica, avançado, grupo de usuários de relatório)

* URL de relatórios do MBAM

* Nome do SQL Server e nomes de bancos de dados

* MBAM ReadWrite e ReadOnly

### Conta do pool de aplicativos

Para localizar a conta do pool de aplicativos, faça logon no servidor Web MBAM, abra o **Gerenciador dos serviços de informações da Internet (IIS)** e selecione **pools de aplicativos**:

![pools de aplicativos](images/troubleshooting-MBAM-installation-1.png)

O SPN (nome da entidade de serviço) deve ser definido nesta conta. Essa configuração é muito importante para a funcionalidade do MBAM.

### Grupos do MBAM (assistência técnica, avançado, grupo de usuários relatórios e URL de relatórios)

![Grupos do MBAM](images/troubleshooting-MBAM-installation-2.png)

Isso fornece informações como grupo de helpdesk, grupo avançado de assistência técnica, grupo de usuários de relatório e URL de relatórios do MBAM. A URL de relatórios do MBAM deve ser fornecida na configuração do MBAM e deve ser lida como: http (s)://servername/ReportServer.

### Nome do SQL Server e nomes de banco de dados (DB)

Para localizar os nomes e instâncias do SQL Server que hospedam os bancos de MBAM, faça logon no servidor Web do MBAM (IIS) e navegue até a subchave do registro do folowing:

**HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM Server\Web**

![Regedit](images/troubleshooting-MBAM-installation-3.png)

As partes realçadas são cadeias de conexão. Eles devem ter o nome do SQL Server, os nomes de banco de dados e as instâncias (se nomeados).

### MBAM ReadWrite e ReadOnly

Essas informações estarão no banco de dados do SQL Server, para a qual já encontramos o nome do servidor Web.

#### Conta ReadWrite

1. Conecte-se ao SQL Management Studio.

2. Clique com o botão direito do mouse em **MBAM recuperação e hardware**, selecione **Propriedades**e, em seguida, selecione **permissões**.

Por exemplo, o nome da conta do laboratório é **MBAMWrite**. As contas pool de aplicativos e ReadWrite são definidas para serem iguais.

![SQL DB](images/troubleshooting-MBAM-installation-4.png)

![Propriedades de banco de BD](images/troubleshooting-MBAM-installation-5.png)

Navegue até **segurança** e, em seguida, **logins** no SQL Management Studio. Navegue até a conta mostrada na captura de tela anterior.

![Segurança do SQL](images/troubleshooting-MBAM-installation-6.png)

Clique com o botão direito do mouse nas contas, vá para **Propriedades mapeamento de usuários**e localize o banco de dados de recuperação e hardware do MBAM:

![Mapeamento de usuários](images/troubleshooting-MBAM-installation-7.png)

#### Conta somente leitura

Abra o Gerenciador de configuração do SQL Server Reporting Services no servidor SSRS. Selecione a **URL do Gerenciador de relatórios**e, em seguida, navegue pelas **URLs**:

![Gerenciador de relatórios](images/troubleshooting-MBAM-installation-8.png)

Selecione **Administração e monitoramento do Microsoft BitLocker**:

![Administração e monitoramento do BitLocker](images/troubleshooting-MBAM-installation-9.png)

Selecione **MaltaDatasource**:

![Bancos](images/troubleshooting-MBAM-installation-10.png)

![MaltaDatasource](images/troubleshooting-MBAM-installation-11.png)

MaltaDataSource deve ter o nome da conta ReadOnly e deve ser usado na instalação do MBAM.

## Referência

Para obter mais informações, consulte os seguintes artigos:

[Implantando o MBAM 2,5 em uma configuração autônoma](https://support.microsoft.com/help/3046555)

[Microsoft BitLocker Administration and Monitoring 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/)
