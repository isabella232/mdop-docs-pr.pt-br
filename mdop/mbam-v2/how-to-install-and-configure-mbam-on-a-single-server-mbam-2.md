---
title: Como instalar e configurar o MBAM em um servidor único
description: Como instalar e configurar o MBAM em um servidor único
author: dansimp
ms.assetid: 45e6a012-6c8c-4d90-902c-d09de9a0cbea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 53e170f421bdce8dd6f771af3902af627a15a085
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799398"
---
# Como instalar e configurar o MBAM em um servidor único


Os procedimentos neste tópico descrevem como instalar o Microsoft BitLocker Administration and Monitoring (MBAM) na topologia autônoma em um único servidor. Use a configuração de servidor único em um ambiente de teste. Para ambientes de produção, use dois ou mais servidores. Se você estiver instalando a administração e o monitoramento do Microsoft BitLocker usando a topologia do Configuration Manager, consulte [implantando o MBAM com o Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).

O diagrama a seguir mostra um exemplo de uma arquitetura de servidor único. Para obter uma descrição dos bancos de dados e recursos, consulte [arquitetura de alto nível para MBAM 2,0](high-level-architecture-for-mbam-20-mbam-2.md).

![MBAM 2 topologia de implantação de servidor único](images/mbam2-1-server.gif)

Cada recurso do servidor tem determinados pré-requisitos. Para verificar se você atendeu aos pré-requisitos e requisitos de hardware e software, consulte [pré-requisitos de implantação do MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md) e [MBAM 2,0 configurações compatíveis](mbam-20-supported-configurations-mbam-2.md). Além disso, alguns recursos também têm informações que devem ser fornecidas durante o processo de instalação para a implantação bem-sucedida do recurso. Você também deve rever [a preparação do seu ambiente para o MBAM 2,0](preparing-your-environment-for-mbam-20-mbam-2.md) antes de iniciar a implantação do MBAM.

**Observação**  
Para obter os arquivos de log de instalação, use o pacote msiexec e a opção **/l** &lt; Location &gt; para instalar o MBAM. Os arquivos de log são criados no local que você especificar.

Arquivos de log de instalação adicionais são criados na pasta% temp% no servidor do usuário que está instalando o MBAM.



## Para instalar os recursos do MBAM Server em um único servidor


As etapas a seguir descrevem como instalar os recursos gerais do MBAM.

**Para iniciar a instalação dos recursos do servidor do MBAM**

1.  No servidor em que você deseja instalar o MBAM, execute **MBAMSetup.exe** para iniciar o assistente de instalação do MBAM.

2.  Na página de **boas-vindas** , selecione o **programa de aperfeiçoamento da experiência do usuário**e clique em **Iniciar**.

3.  Leia e aceite o contrato de licença de software da Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.

4.  Na página **seleção de topologia** , selecione a topologia **autônoma** e clique em **Avançar**.

5.  Na página **selecionar recursos para instalar** , selecione os recursos que você deseja instalar. Por padrão, todos os recursos do MBAM são selecionados para instalação. Os recursos que devem ser instalados no mesmo computador devem ser instalados juntos ao mesmo tempo. Desmarque as caixas de seleção de todos os recursos que você deseja instalar em outro lugar. Você deve instalar os recursos do MBAM na seguinte ordem:

    -   Banco de dados de recuperação

    -   Banco de dados de auditoria e conformidade

    -   Relatórios de conformidade e auditoria

    -   Servidor de autoatendimento

    -   Servidor de administração e monitoramento

    -   Modelo de política de grupo MBAM

    **Observação**  
    O assistente de instalação verifica os pré-requisitos para a sua instalação e exibe os pré-requisitos que estão faltando. Se todos os pré-requisitos forem atendidos, a instalação continuará. Se um pré-requisito ausente for detectado, você precisará resolver os pré-requisitos ausentes e, em seguida, clique em **verificar pré-requisitos novamente**. Se todos os pré-requisitos forem atendidos desta vez, a instalação será retomada.



6.  Na página **Configurar segurança de comunicação de rede** , escolha se deseja criptografar a comunicação entre os serviços Web no servidor de administração e monitoramento e nos clientes. Se você decidir criptografar a comunicação, selecione a autoridade de certificação-certificado provisionado para usar para criptografia. O certificado deve ser criado antes desta etapa para permitir que você o selecione nessa página.

    **Observação**  
    Esta página será exibida somente se você tiver selecionado o portal de autoatendimento ou o recurso de servidor de administração e monitoramento na página **selecionar recursos para instalar** .



7.  Clique em **Avançar**e, em seguida, prossiga para o próximo conjunto de etapas para configurar os recursos do MBAM Server.

**Para configurar os recursos do servidor do MBAM**

1.  Na página **Configurar o banco** de dados de recuperação, especifique o nome da instância do SQL Server e o nome do banco de dados que armazenará os dados de recuperação. Você também deve especificar onde os arquivos do banco de dados serão localizados e onde as informações do log serão localizadas.

2.  Clique em **Avançar** para continuar.

3.  Na página **Configurar o banco de dados de conformidade e auditoria** , especifique o nome da instância do SQL Server e o nome do banco de dados que armazenará os dados de auditoria e conformidade. Você também deve especificar onde os arquivos do banco de dados serão localizados e onde as informações do log serão localizadas.

4.  Clique em **Avançar** para continuar.

5.  Na página **Configurar a conformidade e os relatórios de auditoria** , especifique a instância do SQL Server Reporting Services na qual os relatórios de conformidade e auditoria serão instalados e forneça uma conta de usuário de domínio e uma senha para acessar o banco de dados de conformidade e auditoria. Configure a senha desta conta para nunca expirar. A conta de usuário deve poder acessar todos os dados disponíveis para o grupo usuários do MBAM Reports.

6.  Clique em **Avançar** para continuar.

7.  Na página **Configurar o portal de autoatendimento** , insira o número da porta, o nome do host, o nome do diretório virtual e o caminho de instalação do portal de autoatendimento.

    **Observação**  
    O número da porta que você especificar deve ser um número de porta não usado no servidor de administração e monitoramento, a menos que você especifique um nome de cabeçalho de host exclusivo. Se você estiver usando o Firewall do Windows, a porta será aberta automaticamente.



8.  Clique em **Avançar** para continuar.

9.  Especifique se deseja usar as atualizações da Microsoft para ajudar a manter seu computador seguro e clique em **Avançar**. Isso não ativa as atualizações automáticas no Windows.

10. Na página **Configurar o servidor de administração e monitoramento** , insira o número da porta, o nome do host, o nome do diretório virtual e o caminho de instalação do site de suporte técnico.

    **Observação**  
    O número da porta que você especificar deve ser um número de porta não usado no servidor de administração e monitoramento, a menos que você especifique um nome de cabeçalho de host exclusivo. Se você estiver usando o Firewall do Windows, a porta será aberta automaticamente.



11. Na página **Resumo da instalação** , examine a lista de recursos que serão instalados e clique em **instalar** para começar a instalar os recursos do MBAM. Clique em **voltar** para voltar ao assistente se precisar revisar ou alterar as configurações de instalação ou clique em **Cancelar** para sair da instalação. A instalação instala os recursos do MBAM e avisa que a instalação foi concluída.

12. Clique em **concluir** para sair do assistente. Depois que os recursos do Microsoft BitLocker Administration and Monitoring Server tiverem sido instalados, prossiga para a próxima seção e conclua as etapas necessárias para adicionar usuários às funções de administração e monitoramento do Microsoft BitLocker. Para obter mais informações sobre as funções, consulte [planejando funções de administrador do MBAM 2,0](planning-for-mbam-20-administrator-roles-mbam-2.md).

**Para executar a configuração pós-instalação**

1.  No servidor de administração e monitoramento, adicione usuários aos grupos locais a seguir para dar a eles acesso aos recursos de site do suporte técnico do MBAM:

    -   **Usuários da assistência técnica do MBAM**: os membros desse grupo local podem acessar os recursos de recuperação de unidade e gerenciamento de TPM no site de administração e monitoramento do MBAM. Todos os campos na recuperação de unidade e no gerenciamento de TPM são campos obrigatórios para um usuário da assistência técnica.

    -   **MBAM usuários avançados da assistência técnica**: os membros desse grupo local têm acesso avançado aos recursos de recuperação de unidade e gerenciamento de TPM no site de administração e monitoramento do MBAM. Para os usuários avançados da assistência técnica, somente o campo **ID da chave** é necessário na recuperação de unidade. Em gerenciar TPM, somente os campos **domínio do computador** e nome do **computador** são necessários.

2.  No servidor de administração e monitoramento, adicione usuários ao grupo local a seguir para habilitá-los a acessar o recurso relatórios no site Administração e monitoramento do MBAM:

    -   **Usuários de relatório MBAM**: os membros desse grupo local podem acessar os recursos de relatórios no site de administração e monitoramento do MBAM.

    -   Marca o portal de autoatendimento com o nome da sua empresa, o texto de aviso e outras informações específicas da empresa. Para obter instruções, consulte [como marcar o portal de autoatendimento](how-to-brand-the-self-service-portal.md).

    **Observação**  
    Associações de usuário ou de grupo idênticas do grupo local **usuários do relatório do MBAM** devem ser mantidas em todos os computadores nos quais os recursos do servidor de administração e monitoramento do MBAM, banco de dados de conformidade e auditoria, e conformidade e relatórios de auditoria estejam instalados. A maneira recomendada de fazer isso é criar um grupo de segurança de domínio e adicionar esse grupo de domínio a cada grupo de usuários de relatório MBAM local. Ao usar esse processo, gerencie as associações de grupo por meio do grupo de domínio.



## Validando a instalação de recursos do servidor MBAM


Quando a instalação do Microsoft BitLocker Administration and Monitoring for concluída, valide se a instalação configurou com êxito todos os recursos MBAM necessários para o gerenciamento do BitLocker. Use o procedimento a seguir para confirmar se o serviço MBAM está funcionando.

**Para validar a instalação de recursos do servidor do MBAM**

1. Em cada servidor em que um recurso MBAM está implantado, abra o **painel de controle**. Selecione **programas**e, em seguida, selecione **programas e recursos**. Verifique se a **Administração e o monitoramento do Microsoft BitLocker** aparecem na lista **programas e recursos** .

   **Observação**  
   Para validar a instalação, você deve usar uma conta de domínio que tenha credenciais administrativas do computador local em cada servidor.



2. No servidor em que o banco de dados de recuperação está instalado, abra o SQL Server Management Studio e verifique se o banco de dados de **recuperação e hardware do MBAM** está instalado.

3. No servidor em que o banco de dados de conformidade e auditoria está instalado, abra o SQL Server Management Studio e verifique se o **banco de dados de status de conformidade do MBAM** está instalado.

4. No servidor em que os relatórios de conformidade e auditoria estiverem instalados, abra um navegador da Web com credenciais administrativas e navegue até a "página inicial" do site do SQL Server Reporting Services.

   O local padrão Home de uma instância do site do SQL Server Reporting Services está em http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /reports. Para localizar a URL real, use a ferramenta Gerenciador de configuração do Reporting Services e selecione as instâncias especificadas durante a instalação.

   Confirme se uma pasta de relatórios denominada administração e administração do Microsoft BitLocker contém uma fonte de dados chamada **MaltaDataSource** e se uma pasta **en-US** contém quatro relatórios.

   **Observação**  
   Se o SQL Server Reporting Services foi configurado como uma instância nomeada, a URL deve ser semelhante à seguinte: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. No servidor em que o recurso administração e monitoramento estiver instalado, execute o **Gerenciador de servidores** e navegue até **funções**. Selecione **servidor Web (IIS)** e, em seguida, clique em **Gerenciador dos serviços de informações da Internet (IIS).**

6. Em **conexões,** navegue até * &lt; NomeDoComputador &gt; *, selecione **sites**e, em seguida, selecione **Administração e monitoramento do Microsoft BitLocker**. Verifique se o **MBAMAdministrationService**, o **MBAMUserSupportService**, o **MBAMComplianceStatusService**e o **MBAMRecoveryAndHardwareService** estão listados.

7. No servidor em que os recursos de administração e monitoramento e o portal de autoatendimento estão instalados, abra um navegador da Web com credenciais administrativas e navegue até os seguintes locais para verificar se eles são carregados com êxito:

   -   *http:// &lt; hostname &gt; /helpdesk/default.aspx* e confirme cada um dos links para navegação e relatórios

   -   *http:// &lt; hostname &gt; /SelfService&gt;/*

   -   *http:// &lt; nome_do_computador &gt; /MBAMAdministrationService/AdministrationService.svc*

   -   *http:// &lt; hostname &gt; /MBAMUserSupportService/UserSupportService.svc*

   -   *http:// &lt; nome_do_computador &gt; /MBAMComplianceStatusService/StatusReportingService.svc*

   -   *http:// &lt; nome_do_computador &gt; /MBAMRecoveryAndHardwareService/CoreService.svc*

   **Observação**  
   Presume-se que os recursos do servidor foram instalados na porta padrão sem criptografia de rede. Se você instalou os recursos de servidor em uma porta ou diretório virtual diferente, altere as URLs para incluir a porta apropriada, por exemplo, *http:// &lt; hostname &gt; : &lt; Port &gt; /helpdesk/default.asp*x ou*http:// &lt; hostname &gt; : &lt; Port &gt; / &lt; VirtualDirectory &gt; /Default.aspx*

   Se os recursos do servidor foram instalados com a criptografia de rede, altere http://para https://.



## Tópicos relacionados


[Implantação da infraestrutura de servidor do MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









