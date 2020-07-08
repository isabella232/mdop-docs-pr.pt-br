---
title: Como instalar e configurar o MBAM em servidores distribuídos
description: Como instalar e configurar o MBAM em servidores distribuídos
author: dansimp
ms.assetid: 9ee766aa-6339-422a-8d00-4f58e4646a5e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51f56a12d4e59226f834c7e474af0f1e96c1e8e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799716"
---
# Como instalar e configurar o MBAM em servidores distribuídos


Os procedimentos neste tópico descrevem a instalação completa dos recursos do Microsoft BitLocker Administration and Monitoring (MBAM) em servidores distribuídos.

Cada recurso do servidor tem determinados pré-requisitos. Para verificar se você atendeu aos pré-requisitos e requisitos de hardware e software, consulte [pré-requisitos de implantação do MBAM 1,0](mbam-10-deployment-prerequisites.md) e [MBAM 1,0 configurações compatíveis](mbam-10-supported-configurations.md). Além disso, alguns recursos exigem que você forneça determinadas informações durante o processo de instalação para implantar o recurso com êxito.

**Observação**  
Para obter os arquivos de log de instalação, você precisa instalar o MBAM usando o pacote **msiexec** e a opção **/l &lt; Location &gt; ** . Os arquivos de log são criados no local que você especificar.

Arquivos de log de instalação adicionais são criados na pasta% Temp% do usuário que executa a instalação do MBAM.



## <a href="" id="deploy-the-mbam-server-features-"></a>Implantar os recursos do MBAM Server


As etapas a seguir descrevem como instalar os recursos gerais do MBAM.

**Observação**  
Certifique-se de usar a configuração de 32 bits em servidores de 32 bits e a configuração de 64 bits em servidores de 64 bits.



**Para implantar recursos do MBAM Server**

1.  Inicie o assistente de instalação do MBAM e clique em **instalar** na página de boas-vindas.

2.  Leia e aceite os termos de licença para software Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.

3.  Por padrão, todos os recursos do MBAM são selecionados para instalação. Desmarque os recursos que você deseja instalar em outro lugar. Os recursos que você deseja instalar no mesmo computador devem ser instalados todos ao mesmo tempo. Os recursos do MBAM devem ser instalados na seguinte ordem:

    -   Recuperação e banco de dados de hardware

    -   Banco de dados de auditoria e conformidade

    -   Auditoria e relatórios de conformidade

    -   Servidor de administração e monitoramento

    -   Modelo de política de grupo MBAM

    **Observação**  
    O assistente de instalação verifica os pré-requisitos para a sua instalação e exibe os pré-requisitos que estão faltando. Se todos os pré-requisitos forem atendidos, a instalação continuará. Se um pré-requisito ausente for detectado, você precisará resolver os pré-requisitos ausentes e, em seguida, clique em **verificar pré-requisitos novamente**. Se todos os pré-requisitos forem atendidos desta vez, a instalação será retomada.



4.  O assistente de configuração do MBAM exibirá as páginas de instalação dos recursos selecionados. As seções a seguir descrevem os procedimentos de instalação para cada recurso.

    **Observação**  
    Geralmente, cada recurso é instalado em um servidor separado. Se você quiser instalar vários recursos em um único servidor, poderá alterar ou eliminar algumas das etapas a seguir.



~~~
**To install the Recovery and Hardware Database**

1.  Choose an option for MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the names of the computers that will be running the Administration and Monitoring Server feature, to configure access to the Recovery and Hardware Database.. Once the Administration and Monitoring Server feature is deployed, it connects to the database by using its domain account.

4.  Click **Next** to continue.

5.  Specify the **Database Configuration** for the SQL Server instance that stores the recovery and hardware data. You must also specify where the database will be located and where the log information will be located.

6.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Database**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Compliance and Audit Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that will be used for encryption.

2.  Click **Next** to continue.

3.  Specify the user account that will be used to access the database for reports.

4.  Click **Next** to continue.

5.  Specify the computer names of the computers that you want to run the Administration and Monitoring Server and the Compliance and Audit Reports, to configure the access to the Compliance and Audit Database.. After the Administration and Monitoring and the Compliance and Audit Reports Server are deployed, they will connect to the databases by using their domain accounts.

6.  Specify the **Database Configuration** for the SQL Server instance that will store the compliance and audit data. You must also specify where the database will be located and where the log information will be located.

7.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Reports**

1.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Compliance and Audit Database are installed.

2.  Specify the name of the Compliance and Audit Database. By default, the database name is “MBAM Compliance Status”, but you can change the name when you install the Compliance and Audit Database.

3.  Click **Next** to continue.

4.  Select the SQL Server Reporting Services instance where the Compliance and Audit Reports will be installed. Provide the username and password used to access the compliance database.

5.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Administration and Monitoring Server feature**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the remote SQL Server instance, For example, *&lt;ServerName&gt;*, where the Compliance and Audit Database are installed.

4.  Specify the name of the Compliance and Audit Database. By default, the database name is MBAM Compliance Status, but, you can change the name when you install the Compliance and Audit Database.

5.  Click **Next** to continue.

6.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Recovery and Hardware Database are installed.

7.  Specify the name of the Recovery and Hardware Database. By default, the database name is **MBAM Recovery and Hardware**, but you can change the name when you install the Recovery and Hardware Database feature.

8.  Click **Next** to continue.

9.  Specify the URL for the “Home” of the SQL Server Reporting Services (SRS) site. The default Home location of a SQL Server Reporting Services site instance is at:

    http://*&lt;NameofMBAMReportsServer&gt;/*ReportServer

    **Note**  
    If you configured the SQL Server Reporting Services as a named instance, the URL resembles the following:http://*&lt;NameofMBAMReportsServer&gt;*/ReportServer\_*&lt;SRSInstanceName&gt;*



10. Click **Next** to continue.

11. Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring server

    **Warning**  
    The port number that you specify must be an unused port number on the Administration and Monitoring server, unless you specify a unique host header name.



12. Click **Next** to continue with the MBAM Setup wizard.
~~~

5. 

   Especifique se deseja usar as atualizações da Microsoft para ajudar a manter seu computador seguro e clique em **Avançar**.

6. Quando as informações do recurso MBAM selecionado estiverem completas, você estará pronto para iniciar a instalação do MBAM usando o assistente de configuração. Clique em **voltar** para mover-se pelo assistente se precisar revisar ou alterar as configurações de instalação. Clique em **instalar** para começar a instalação. Clique em **Cancelar** para sair do assistente. A instalação instala os recursos do MBAM que você selecionou e avisa que a instalação foi concluída.

7. Clique em **concluir** para sair do assistente.

8. Adicione usuários às funções MBAM apropriadas, após a instalação dos recursos do servidor do MBAM.. Para obter mais informações, consulte [planejando funções de administrador do MBAM 1,0](planning-for-mbam-10-administrator-roles.md).

**Configuração pós-instalação**

1.  Após a conclusão da instalação do MBAM, você deve adicionar funções de usuário para que os usuários possam acessar os recursos no site de administração do MBAM. No servidor de administração e monitoramento, adicione usuários aos grupos locais a seguir.

    -   **Usuários de hardware do MBAM**: os membros desse grupo local podem acessar o recurso de hardware no site de administração do MBAM.

    -   **Usuários da assistência técnica do MBAM**: os membros desse grupo local podem acessar os recursos de recuperação de unidade e gerenciamento de módulos de plataforma confiáveis (TPM) no site de administração do MBAM. Todos os campos na recuperação de unidade e no gerenciamento de TPM são campos obrigatórios para um usuário da assistência técnica.

    -   **Usuários de helpdesk avançados do MBAM**: os membros desse grupo local têm acesso avançado aos recursos de recuperação de unidade e gerenciamento de TPM no site de administração do MBAM. Para os usuários avançados da assistência técnica, somente o campo ID da chave é necessário na recuperação de unidade. Em gerenciar TPM, somente os campos domínio do computador e nome do computador são necessários.

2.  No servidor de administração e monitoramento, no banco de dados de conformidade e auditoria e no servidor que hospeda os relatórios de conformidade e auditoria, adicione usuários ao grupo local a seguir para dar a eles acesso ao recurso relatórios no site de administração do MBAM.

    -   **Usuários de relatório MBAM**: os membros desse grupo local podem acessar os relatórios no site de administração do MBAM.

    **Observação**  
    Associações de usuário ou de grupo idênticas do grupo local **usuários do relatório MBAM** devem ser mantidas em todos os computadores nos quais os recursos de servidor administração e monitoramento do MBAM, banco de dados de conformidade e auditoria e os relatórios de conformidade e auditoria estejam instalados.



## Validar a instalação de recursos do servidor do MBAM


Quando a instalação do recurso MBAM Server estiver concluída, você deve validar se a instalação configurou com êxito todos os recursos necessários para o MBAM. Use o procedimento a seguir para confirmar se o serviço MBAM está funcionando.

**Para validar uma instalação do MBAM**

1. Em cada servidor, onde um recurso do MBAM é implantado, abra o **painel de controle**, clique em **programas**e clique em **programas e recursos**. Verifique se a **Administração e o monitoramento do Microsoft BitLocker** aparecem na lista **programas e recursos** .

   **Observação**  
   Para validar a instalação do MBAM, você deve usar uma conta de domínio que tenha credenciais administrativas do computador local em cada servidor.



2. No servidor em que o banco de dados de recuperação e de hardware está instalado, abra o SQL Server Management Studio e verifique se o banco de dados de **recuperação e hardware do MBAM** está instalado.

3. No servidor em que o banco de dados de conformidade e auditoria está instalado, abra o SQL Server Management Studio e verifique se o banco de dados de **status de conformidade do MBAM** está instalado.

4. No servidor em que os relatórios de conformidade e auditoria estiverem instalados, abra um navegador da Web com privilégios administrativos e navegue até a "página inicial" do site do SQL Server Reporting Services.

   O local padrão Home de uma instância do site do SQL Server Reporting Services pode ser encontrado em http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /reports.aspx. Para localizar a URL real, use a ferramenta Gerenciador de configuração do Reporting Services e selecione as instâncias especificadas durante a instalação.

   Confirme se uma pasta denominada **relatórios de conformidade de Malta** está listada e se contém cinco relatórios e uma fonte de dados.

   **Observação**  
   Se o SQL Server Reporting Services foi configurado como uma instância nomeada, a URL deve ser semelhante à seguinte: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *



5. No servidor em que o recurso administração e monitoramento estiver instalado, execute **o Gerenciador de servidores** e navegue até **funções**, selecione **servidor Web (IIS)** e clique em **Gerenciador dos serviços de informações da Internet (IIS)**. Em **conexões** , navegue até * &lt; NomeDoComputador &gt; *, clique em **sites**e clique em **Administração e monitoramento do Microsoft BitLocker**. Verifique se **MBAMAdministrationService**, **MBAMComplianceStatusService**e **MBAMRecoveryAndHardwareService** estão listados.

6. No servidor em que o recurso administração e monitoramento estiver instalado, abra um navegador da Web com privilégios administrativos e navegue até os seguintes locais no site da MBAM para verificar se eles são carregados com êxito:

   -   *http:// &lt; NomeDoComputador &gt; /Default.aspx* e confirme cada um dos links para navegação e relatórios

   -   *http:// &lt; nome_do_computador &gt; /MBAMAdministrationService/AdministrationService.svc*

   -   *http:// &lt; nome_do_computador &gt; /MBAMComplianceStatusService/StatusReportingService.svc*

   -   *http:// &lt; nome_do_computador &gt; /MBAMRecoveryAndHardwareService/CoreService.svc*

   **Observação**  
   Normalmente, os serviços são instalados na porta padrão 80 sem criptografia de rede. Se os serviços estiverem instalados em uma porta diferente, altere as URLs para incluir a porta apropriada. Por exemplo, http://* &lt; ComputerName &gt; : &lt; Port &gt; */default.aspx ou http:// <em> &lt; hostheadername &gt; / </em> Default. aspx

   Se os serviços foram instalados com a criptografia de rede, altere http://para https://.



~~~
Verify that each web page loads successfully.
~~~

## Tópicos relacionados


[Implantando a infraestrutura do Servidor do MBAM 1.0](deploying-the-mbam-10-server-infrastructure.md)









