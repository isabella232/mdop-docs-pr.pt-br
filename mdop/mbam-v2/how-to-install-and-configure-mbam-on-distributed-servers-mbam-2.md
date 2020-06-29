---
title: Como instalar e configurar o MBAM em servidores distribuídos
description: Como instalar e configurar o MBAM em servidores distribuídos
author: dansimp
ms.assetid: 67b91e6b-ae2e-4e47-9ef2-6819aba95976
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 841b894430d14604f0fd923703708d7a3f588c07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799396"
---
# Como instalar e configurar o MBAM em servidores distribuídos


Os procedimentos neste tópico descrevem como instalar o Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 na topologia autônoma em servidores distribuídos. Para ver um diagrama da arquitetura recomendada, juntamente com uma descrição dos bancos de dados e recursos, consulte [implantando a infraestrutura de servidor MBAM 2,0](deploying-the-mbam-20-server-infrastructure-mbam-2.md). Para instalar a administração e o monitoramento do Microsoft BitLocker com a topologia do Configuration Manager, consulte [implantando o MBAM com o Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).

Cada recurso do servidor tem determinados pré-requisitos. Para verificar se você atendeu aos pré-requisitos e requisitos de hardware e software, consulte [pré-requisitos de implantação do MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md) e [MBAM 2,0 configurações compatíveis](mbam-20-supported-configurations-mbam-2.md). Além disso, alguns recursos exigem que você forneça determinadas informações durante o processo de instalação para implantar o recurso com êxito. Você também deve analisar o [planejamento para a implantação do MBAM 2,0 Server](planning-for-mbam-20-server-deployment-mbam-2.md) antes de iniciar a implantação do MBAM.

**Observação**  
Para obter os arquivos de log de instalação, você precisa usar o pacote msiexec e a opção **/l** &lt; Location &gt; para instalar o MBAM. Os arquivos de log são criados no local que você especificar.

Arquivos de log de instalação adicionais são criados na pasta% temp% no servidor do usuário que está instalando o MBAM.



## <a href="" id="deploying-mbam-server-features-"></a>Implantando recursos do MBAM Server


As etapas a seguir descrevem como instalar os recursos gerais do MBAM.

**Para iniciar o assistente de instalação do MBAM Server**

1.  No servidor em que você deseja instalar a administração e o monitoramento do Microsoft BitLocker, execute **MBAMSetup.exe** para iniciar o assistente de instalação do MBAM.

2.  Na página de **boas-vindas** , selecione o **programa de aperfeiçoamento da experiência do usuário**e clique em **Iniciar**.

3.  Leia e aceite o contrato de licença de software da Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.

4.  Na página **seleção de topologia** , selecione a topologia **autônoma** e clique em **Avançar**.

    **Observação**  
    Se você quiser instalar o MBAM com a topologia integrada do Configuration Manager, consulte [implantando o MBAM com o Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).



5.  Selecione os recursos que você deseja instalar. Por padrão, todos os recursos do MBAM são selecionados para instalação. Desmarque os recursos que você deseja instalar em outro lugar. Os recursos que serão instalados no mesmo computador deverão ser instalados juntos ao mesmo tempo. Você deve instalar os recursos do MBAM na seguinte ordem:

    -   Banco de dados de recuperação

    -   Banco de dados de auditoria e conformidade

    -   Relatórios de conformidade e auditoria

    -   Portal de autoatendimento

    -   Servidor de administração e monitoramento

    -   Modelo de política de grupo MBAM

    **Observação**  
    O assistente de instalação verifica os pré-requisitos para a sua instalação e exibe os pré-requisitos que estão faltando. Se todos os pré-requisitos forem atendidos, a instalação continuará. Se um pré-requisito ausente for detectado, você precisará resolver os pré-requisitos ausentes e, em seguida, clique em **verificar pré-requisitos novamente**. Se todos os pré-requisitos forem atendidos desta vez, a instalação será retomada.



~~~
The MBAM Setup wizard displays installation pages for the features that you select. The following sections describe the installation procedures for each feature.

**Note**  
For the following instructions, it is assumed that each feature is to be installed on a separate server. If you install multiple features on a single server, you can change or eliminate some steps.
~~~



**Para instalar o banco de dados de recuperação**

1.  Na página **Configurar o banco de dados de recuperação** , especifique os nomes dos computadores que executarão o recurso de servidor de administração e monitoramento. Após a implantação do recurso de servidor de administração e monitoramento, ele usa sua conta de domínio para se conectar ao banco de dados.

2.  Clique em **Avançar** para continuar.

3.  Especifique o nome da instância do SQL Server e o nome do banco de dados que armazenará os dados de recuperação. Você também deve especificar o local em que o banco de dados será localizado e onde as informações do log serão localizadas.

4.  Clique em **Avançar** para continuar com o assistente de configuração do MBAM.

**Para instalar o banco de dados de auditoria e conformidade**

1.  Na página **Configurar o banco de dados de conformidade e auditoria** , especifique a conta de usuário que será usada para acessar o banco de dados para relatórios.

2.  Especifique os nomes de computador dos computadores que executarão o servidor de administração e monitoramento e os relatórios de conformidade e auditoria. Após a implantação da administração e do monitoramento e do servidor de relatórios de auditoria e conformidade, eles usam suas contas de domínio para se conectar aos bancos de dados.

    **Observação**  
    Se você estiver instalando o banco de dados de auditoria e conformidade sem o recurso de relatórios de auditoria e conformidade, será necessário adicionar uma exceção no computador de banco de dados de conformidade e auditoria para habilitar o tráfego de entrada na porta do Microsoft SQL Server. O número da porta padrão é 1433.



3.  Especifique o nome da instância do SQL Server e o nome do banco de dados que armazenará os dados de auditoria e conformidade. Você também deve especificar onde as informações do log e do banco de dados serão localizadas.

4.  Clique em **Avançar** para continuar com o assistente de configuração de monitoramento e administração do Microsoft BitLocker.

**Para instalar os relatórios de conformidade e auditoria**

1.  Na página **configurar os relatórios de conformidade e auditoria** , especifique o nome da instância remota do SQL Server (por exemplo, &lt; ServerName &gt; ) em que o banco de dados de auditoria e conformidade foi instalado.

    **Observação**  
    Se você estiver instalando os relatórios de conformidade e auditoria sem o servidor de administração e monitoramento, será necessário adicionar uma exceção no computador de relatório de conformidade e auditoria para habilitar o tráfego de entrada na porta do servidor de relatório (a porta padrão é 80).



2.  Especifique o nome do banco de dados de auditoria e conformidade. Por padrão, o nome do banco de dados é MBAM status de conformidade, embora você possa alterar o nome ao instalar o banco de dados de conformidade e auditoria.

3.  Clique em **Avançar** para continuar.

4.  Selecione a instância do SQL Server Reporting Services na qual os relatórios de conformidade e auditoria serão instalados. Forneça uma conta de usuário de domínio e senha para acessar o banco de dados de auditoria e conformidade. Configure a senha desta conta para nunca expirar. A conta de usuário deve ser capaz de acessar todos os dados que estão disponíveis para o grupo de usuários do MBAM Reports.

5.  Clique em **Avançar** para continuar com o assistente de configuração de monitoramento e administração do Microsoft BitLocker.

**Para instalar o portal de autoatendimento**

1.  Na página **Configurar o portal de autoatendimento** , você pode, opcionalmente, criptografar a comunicação entre o portal de autoatendimento e os servidores de administração e monitoramento. Se você escolher a opção de criptografar a comunicação, será solicitado a selecionar o certificado provisionado para a autoridade de certificação a ser usado para criptografia.

2.  Clique em **Avançar** para continuar.

3.  Especifique a instância remota do SQL Server (por exemplo, * &lt; ServerName &gt; *) em que o banco de dados de auditoria e conformidade foi instalado.

4.  Especifique o nome do banco de dados de auditoria e conformidade. Por padrão, o nome do banco de dados é MBAM status de conformidade. No entanto, você pode alterar o nome ao instalar o banco de dados de auditoria e conformidade.

5.  Clique em **Avançar** para continuar.

6.  Especifique a instância remota do SQL Server (por exemplo, * &lt; ServerName &gt; *) em que o banco de dados de recuperação foi instalado.

7.  Especifique o nome do banco de dados de recuperação. Por padrão, o nome do banco de dados é **MBAM recuperação e hardware**. No entanto, você pode alterar o nome ao instalar o recurso de banco de dados de recuperação.

8.  Clique em **Avançar** para continuar.

9.  Digite o **número da porta**, o **nome do host** (opcional) e o caminho de **instalação** do MBAM Administration and Monitoring Server.

    **Observação**  
    O número da porta que você especificar deve ser um número de porta não usado no servidor de administração e monitoramento, a menos que você especifique um nome de cabeçalho de host exclusivo. Se você estiver usando o Firewall do Windows, a porta será aberta automaticamente.



10. Para registrar opcionalmente um SPN (nome da entidade de serviço) para o portal de autoatendimento, selecione **registrar os nomes principais de serviço (SPN) da máquina com o Active Directory (necessário para a autenticação do Windows)**. Se você marcar esta caixa de seleção, a instalação do MBAM não tentará registrar os SPNs existentes, e você poderá registrar manualmente o SPN antes ou depois da instalação do MBAM. Para obter instruções sobre como registrar o SPN manualmente, consulte [registro manual de SPN](https://go.microsoft.com/fwlink/?LinkId=286758).

11. Clique em **Avançar** para continuar com o assistente de configuração de monitoramento e administração do Microsoft BitLocker.

12. Especifique se deseja usar as atualizações da Microsoft para ajudar a manter seu computador seguro e clique em **Avançar**.

13. Quando as informações do recurso MBAM selecionado forem concluídas, você estará pronto para iniciar a instalação do MBAM usando o assistente de configuração. Clique em **voltar** para mover-se pelo assistente se precisar revisar ou alterar as configurações de instalação. Clique em **instalar** para iniciar a instalação. Clique em **Cancelar** para sair do assistente. A instalação instala os recursos do MBAM que você selecionou e avisa que a instalação foi concluída.

14. Clique em **concluir** para sair do assistente.

    **Observação**  
    Para configurar o portal de autoatendimento depois de instalá-lo, confira o portal de autoatendimento com o nome da sua empresa e outras informações específicas da empresa em [como marcar o portal de autoatendimento](how-to-brand-the-self-service-portal.md) para obter instruções.



15. Se os computadores cliente tiverem acesso à rede de distribuição de conteúdo (CDN) da Microsoft, que fornece ao portal de autoatendimento o acesso necessário a certos arquivos JavaScript, você concluiu a instalação do portal de autoatendimento. Se os computadores cliente não tiverem acesso à CDN da Microsoft, conclua as etapas na próxima seção para configurar o portal de autoatendimento para fazer referência aos arquivos JavaScript a partir de uma fonte acessível.

**Para configurar o portal de autoatendimento quando os usuários finais não conseguem acessar a Microsoft Content Delivery Network**

1. Se os computadores cliente tiverem acesso à rede de distribuição de conteúdo (CDN) da Microsoft, que fornece ao portal de autoatendimento o acesso necessário a certos arquivos JavaScript, a instalação do portal de autoatendimento está concluída. Se os computadores cliente não tiverem acesso à CDN da Microsoft, conclua as etapas restantes desta seção para configurar o portal de autoatendimento para fazer referência aos arquivos JavaScript a partir de uma fonte acessível.

2. Baixe os quatro arquivos JavaScript da CDN da Microsoft:

   -   jQuery-1.7.2.min.js-[https://go.microsoft.com/p/fwlink/?LinkID=271736](https://go.microsoft.com/fwlink/p/?LinkID=271736)

   -   MicrosoftAjax.js –[https://go.microsoft.com/p/fwlink/?LinkId=272283](https://go.microsoft.com/fwlink/p/?LinkId=272283)

   -   MicrosoftMvcAjax.js-[https://go.microsoft.com/p/fwlink/?LinkId=272284](https://go.microsoft.com/fwlink/p/?LinkId=272284)

   -   MicrosoftMvcValidation.js- <https://go.microsoft.com/fwlink/p/?LinkId=272285>

3. Copie os arquivos JavaScript para o diretório **scripts** do portal de autoatendimento. Esse diretório está localizado no <em> &lt; MBAM Self-Service &gt; \\ </em> Website\\Scripts. Self-Service Directory

4. Abra o **Gerenciador dos serviços de informações da Internet (IIS)**.

5. Expanda **sites** &gt; **Administração e monitoramento do Microsoft BitLocker**e realce **SelfService**.

   **Observação**  
   *SelfService* é o nome do diretório virtual padrão. Se você tiver escolhido um nome diferente para esse diretório durante a instalação, lembre-se de substituir *SelfService* no restante dessas instruções com o nome escolhido.



6. No painel do meio, clique duas vezes em **configurações do aplicativo**.

7. Para cada item na lista a seguir, edite as configurações do aplicativo para referenciar o novo local substituindo o &lt; diretório virtual &gt; por/SelfService/(ou o nome escolhido durante a instalação). Por exemplo, o caminho do diretório virtual será semelhante a jquery-1.7.2.min.js/selfservice/scripts/.

   -   jQueryPath:/ &lt; diretório virtual &gt; /scripts/jQuery-1.7.2.min.js

   -   MicrosoftAjaxPath:/ &lt; diretório virtual &gt; /scripts/MicrosoftAjax.js

   -   MicrosoftMvcAjaxPath:/ &lt; diretório virtual &gt; /scripts/MicrosoftMvcAjax.js

   -   MicrosoftMvcValidationPath:/ &lt; diretório virtual &gt; /scripts/MicrosoftMvcValidation.js

**Para instalar o recurso do servidor de administração e monitoramento**

1. O MBAM pode criptografar a comunicação entre os serviços Web e os servidores de administração e monitoramento. Se você escolher a opção de criptografar a comunicação, será solicitado a selecionar o certificado provisionado para a autoridade de certificação a ser usado para criptografia.

2. Clique em **Avançar** para continuar.

3. Especifique a instância remota do SQL Server (por exemplo: * &lt; ServerName &gt; *) em que o banco de dados de auditoria e conformidade foi instalado.

4. Especifique o nome do banco de dados de auditoria e conformidade. Por padrão, o nome do banco de dados é MBAM status de conformidade. No entanto, você pode alterar o nome ao instalar o banco de dados de auditoria e conformidade.

5. Clique em **Avançar** para continuar.

6. Especifique a instância remota do SQL Server (por exemplo: * &lt; nomedoservidor &gt; *) em que o banco de dados de recuperação foi instalado.

7. Especifique o nome do banco de dados de recuperação. Por padrão, o nome do banco de dados é **MBAM recuperação e hardware**. No entanto, você pode alterar o nome ao instalar o recurso de banco de dados de recuperação.

8. Clique em **Avançar** para continuar.

9. Especifique a URL para a "página inicial" do site do SQL Server Reporting Services (SRS). O local padrão Home de uma instância do site do SQL Server Reporting Services está em:

   http:// <em> &lt; NameofMBAMReportsServer &gt; / </em> ReportServer

   **Observação**  
   Se o SQL Server Reporting Services foi configurado como uma instância nomeada, a URL é semelhante à seguinte: http://* &lt; NameofMBAMReportsServer &gt; */ReportServer\_* &lt; SRSInstanceName &gt; *.



10. Clique em **Avançar** para continuar.

11. Digite o **número da porta**, o **nome do host** (opcional) e o caminho de **instalação** do MBAM Administration and Monitoring Server.

    **Observação**  
    O número da porta que você especificar deve ser um número de porta não usado no servidor de administração e monitoramento, a menos que você especifique um nome de cabeçalho de host exclusivo. Se você estiver usando o Firewall do Windows, a porta será aberta automaticamente.



12. Para registrar opcionalmente um SPN (nome da entidade de serviço) para o portal de autoatendimento, selecione **registrar os nomes principais de serviço (SPN) da máquina com o Active Directory (necessário para a autenticação do Windows)**. Se você marcar esta caixa de seleção, a instalação do MBAM não tentará registrar os SPNs existentes, e você poderá registrar manualmente o SPN antes ou depois da instalação do MBAM. Para obter instruções sobre como registrar o SPN manualmente, consulte [registro manual de SPN](https://go.microsoft.com/fwlink/?LinkId=286758).

13. Clique em **Avançar** para continuar com o assistente de configuração de monitoramento e administração do Microsoft BitLocker.

14. Especifique se deseja usar as atualizações da Microsoft para ajudar a manter seu computador seguro e clique em **Avançar**.

15. Quando as informações do recurso MBAM selecionado forem concluídas, você estará pronto para iniciar a instalação do MBAM usando o assistente de configuração. Clique em **voltar** para mover-se pelo assistente se precisar revisar ou alterar as configurações de instalação. Clique em **instalar** para a instalação. Clique em **Cancelar** para sair do assistente. A instalação instala os recursos do MBAM que você selecionou e avisa que a instalação foi concluída.

16. Clique em **concluir** para sair do assistente.

**Para executar a configuração pós-instalação**

1.  No servidor de administração e monitoramento, adicione usuários aos grupos locais a seguir para dar a eles acesso aos recursos no site Administração e monitoramento do MBAM.

    -   **Usuários da assistência técnica do MBAM**: os membros desse grupo local podem acessar os recursos de recuperação de unidade e gerenciamento de TPM no site de administração e monitoramento do MBAM. Todos os campos na recuperação de unidade e no gerenciamento de TPM são campos obrigatórios para um usuário da assistência técnica.

    -   **MBAM usuários avançados da assistência técnica**: os membros desse grupo local têm acesso avançado aos recursos de recuperação de unidade e gerenciamento de TPM no site de administração e monitoramento do MBAM. Para os usuários avançados da assistência técnica, somente o campo ID da chave é necessário na recuperação de unidade. Em **gerenciar TPM**, somente os campos **domínio do computador** e nome do **computador** são necessários.

2.  No servidor que hospeda o servidor de administração e monitoramento e o banco de dados de conformidade e auditoria e no servidor que hospeda os relatórios de conformidade e auditoria, adicione usuários ao grupo local a seguir para dar a eles acesso ao recurso relatórios no site Administração e monitoramento do MBAM.

    -   **Usuários de relatório MBAM**: os membros desse grupo local podem acessar os relatórios no site de administração e monitoramento do MBAM.

    **Observação**  
    Associações de usuário ou de grupo idênticas do grupo local **usuários do relatório MBAM** devem ser mantidas em todos os computadores nos quais os recursos de servidor administração e monitoramento do MBAM, banco de dados de conformidade e auditoria e os relatórios de conformidade e auditoria estejam instalados.



## Validando a instalação de recursos do servidor MBAM


Quando a instalação do recurso Microsoft BitLocker Administration and Monitoring Server estiver concluída, recomendamos que você valide se a instalação configurou com êxito todos os recursos necessários para o MBAM. Use o procedimento a seguir para confirmar se o serviço de administração e monitoramento do Microsoft BitLocker está funcionando.

**Para validar uma instalação do MBAM Server**

1. Em cada servidor em que um recurso MBAM é implantado, abra o **painel de controle**, selecione **programas**e **programas e recursos**. Verifique se a **Administração e o monitoramento do Microsoft BitLocker** aparecem na lista **programas e recursos** .

   **Observação**  
   Para validar a instalação do MBAM, você deve usar uma conta de domínio que tenha credenciais administrativas do computador local em cada servidor.



2. No servidor em que o banco de dados de recuperação está instalado, abra o SQL Server Management Studio e verifique se o banco de dados de **recuperação e hardware do MBAM** está instalado.

3. No servidor em que o banco de dados de conformidade e auditoria está instalado, abra o SQL Server Management Studio e verifique se o **banco de dados de status de conformidade do MBAM** está instalado.

4. No servidor em que os relatórios de conformidade e auditoria estiverem instalados, abra um navegador da Web com credenciais administrativas e navegue até a "página inicial" do site do SQL Server Reporting Services.

   O local Home padrão de uma instância de site do SQL Server Reporting Services pode ser encontrado em http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /reports.aspx. Para localizar a URL real, use a ferramenta Gerenciador de configuração do Reporting Services e selecione as instâncias que foram especificadas durante a instalação.

   Confirme se uma pasta de relatórios denominada **Administração e administração do Microsoft BitLocker** contém uma fonte de dados chamada **MaltaDataSource** e se uma pasta **en-US** contém quatro relatórios.

   **Observação**  
   Se o SQL Server Reporting Services foi configurado como uma instância nomeada, a URL deve ser semelhante à seguinte: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. No servidor em que o recurso administração e monitoramento estiver instalado, execute o **Gerenciador de servidores** e navegue até **funções**. Selecione **servidor Web (IIS)** e, em seguida, clique em **Gerenciador dos serviços de informações da Internet (IIS)**.

6. Em **conexões**, navegue até * &lt; NomeDoComputador &gt; *, selecione **sites**e selecione **Administração e monitoramento do Microsoft BitLocker**. Verifique se **MBAMAdministrationService**, **MBAMComplianceStatusService**e **MBAMRecoveryAndHardwareService** estão listados.

7. No servidor em que os recursos de administração e monitoramento e o portal de autoatendimento estão instalados, abra um navegador da Web com credenciais administrativas e navegue até os seguintes locais para verificar se eles são carregados com êxito.

   **Observação**  
   As URLs terminadas em ". svc" não exibem um site. O sucesso é indicado pela mensagem "a publicação de metadados para este serviço está atualmente desabilitada" ou por informações semelhantes a um código. Se você vir outra mensagem de erro ou se não for possível encontrar a página, a página não será carregada com êxito.



~~~
-   *http://&lt;hostname&gt;/HelpDesk/default.aspx* and confirm each of the links for navigation and reports

-   *http://&lt;hostname&gt;/SelfService&gt;/*

-   *http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc*

-   *http://&lt;hostname&gt;/MBAMUserSupportService/UserSupportService.svc*

-   *http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc*

-   *http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc*

**Note**  
It is assumed that the server features were installed on the default port without network encryption. If you installed the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example, *http://&lt;hostname&gt;:&lt;port&gt;/HelpDesk/default.aspx* or*http://&lt;hostname&gt;:&lt;port&gt;/&lt;virtualdirectory&gt;/default.aspx*

If the server features were installed with network encryption, change http:// to https://.
~~~



8. Verifique se cada página da Web foi carregada com êxito.

## Tópicos relacionados


[Implantação da infraestrutura de servidor do MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









