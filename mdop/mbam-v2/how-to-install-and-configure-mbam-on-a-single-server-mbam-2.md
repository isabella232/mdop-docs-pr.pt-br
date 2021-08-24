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
ms.openlocfilehash: 4dffe2e2dcb82866b86a3ac281aca8a0dcaab686
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910656"
---
# <a name="how-to-install-and-configure-mbam-on-a-single-server"></a>Como instalar e configurar o MBAM em um servidor único


Os procedimentos neste tópico descrevem como instalar o Microsoft BitLocker Administration and Monitoring (MBAM) na topologia autônomo em um único servidor. Use a configuração de servidor único somente em um ambiente de teste. Para ambientes de produção, use dois ou mais servidores. Se você estiver instalando a Administração e o Monitoramento do Microsoft BitLocker usando a topologia do Configuration Manager, consulte [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).

O diagrama a seguir mostra um exemplo de uma arquitetura de servidor único. Para uma descrição dos bancos de dados e recursos, consulte [High-Level Architecture for MBAM 2.0](high-level-architecture-for-mbam-20-mbam-2.md).

![topologia de implantação de servidor único do mbam 2.](images/mbam2-1-server.gif)

Cada recurso de servidor tem determinados pré-requisitos. Para verificar se você atendeu aos pré-requisitos e requisitos de hardware e software, consulte [MbaM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) e CONFIGURAções com suporte do [MBAM 2.0](mbam-20-supported-configurations-mbam-2.md). Além disso, alguns recursos também têm informações que devem ser fornecidas durante o processo de instalação para implantar o recurso com êxito. Você também deve revisar [Preparando seu Ambiente para o MBAM 2.0](preparing-your-environment-for-mbam-20-mbam-2.md) antes de iniciar a implantação do MBAM.

**Observação**  
Para obter os arquivos de log de instalação, use o pacote Msiexec e a opção de local **/L** &lt; para instalar o &gt; MBAM. Os arquivos de log são criados no local especificado.

Arquivos de log de instalação adicionais são criados na pasta %temp% no servidor do usuário que está instalando o MBAM.



## <a name="to-install-mbam-server-features-on-a-single-server"></a>Para instalar recursos do MBAM Server em um único servidor


As etapas a seguir descrevem como instalar recursos gerais do MBAM.

**Para iniciar a instalação de recursos do MBAM Server**

1.  No servidor onde você deseja instalar o MBAM, executeMBAMSetup.exe** iniciar ** o assistente de instalação do MBAM.

2.  Na página **Bem-vindo,** selecione opcionalmente o Programa de Aperfeiçoamento da Experiência **do Cliente**e clique em **Iniciar**.

3.  Leia e aceite o Contrato de Licença de Software da Microsoft e clique em **Próximo** para continuar a instalação.

4.  Na página **Seleção de Topologia,** selecione **a** topologia autônomo e clique em **Próximo**.

5.  Na página **Selecionar recursos para instalar,** selecione os recursos que você deseja instalar. Por padrão, todos os recursos do MBAM são selecionados para instalação. Os recursos que devem ser instalados no mesmo computador devem ser instalados juntos ao mesmo tempo. Limpe as caixas de seleção de todos os recursos que você deseja instalar em outro lugar. Você deve instalar os recursos do MBAM na seguinte ordem:

    -   Banco de Dados de Recuperação

    -   Banco de dados de conformidade e auditoria

    -   Relatórios de conformidade e auditoria

    -   Self-Service Server

    -   Servidor de Administração e Monitoramento

    -   Modelo de Política de Grupo do MBAM

    **Observação**  
    O assistente de instalação verifica os pré-requisitos de sua instalação e exibe os pré-requisitos que estão faltando. Se todos os pré-requisitos são atendidos, a instalação continua. Se um pré-requisito ausente for detectado, você terá que resolver os pré-requisitos ausentes e, em seguida, clique em Verificar **pré-requisitos novamente**. Se todos os pré-requisitos são atendidos desta vez, a instalação é retomada.



6.  Na página **Configurar segurança de** comunicação de rede, escolha se deve criptografar a comunicação entre os Serviços Web no Servidor de Administração e Monitoramento e os clientes. Se você decidir criptografar a comunicação, selecione o certificado provisionado pela autoridade de certificação a ser usado para criptografia. O certificado deve ser criado antes desta etapa para permitir que você o selecione nesta página.

    **Observação**  
    Esta página será exibida somente se você tiver selecionado o portal Self-Service ou o recurso Servidor de Administração e Monitoramento na página Selecionar **recursos para** instalar.



7.  Clique **em**Próximo e continue para o próximo conjunto de etapas para configurar os recursos do MBAM Server.

**Para configurar os recursos do MBAM Server**

1.  Na página **Configurar o banco de** dados de recuperação, especifique o nome da instância SQL Server e o nome do banco de dados que armazenará os dados de recuperação. Você também deve especificar onde os arquivos de banco de dados estarão localizados e onde as informações de log estarão localizadas.

2.  Clique em **Avançar** para continuar.

3.  Na página **Configurar o banco** de dados de Conformidade e Auditoria, especifique o nome da instância SQL Server e o nome do banco de dados que armazenará os dados de conformidade e auditoria. Você também deve especificar onde os arquivos de banco de dados estarão localizados e onde as informações de log estarão localizadas.

4.  Clique em **Avançar** para continuar.

5.  Na página **Configurar** relatórios de conformidade e auditoria, especifique a SQL Server Reporting Services em que os relatórios de Conformidade e Auditoria serão instalados e forneça uma conta de usuário de domínio e senha para acessar o banco de dados de Conformidade e Auditoria. Configure a senha dessa conta para nunca expirar. A conta de usuário deve ser capaz de acessar todos os dados disponíveis para o grupo Usuários de Relatórios do MBAM.

6.  Clique em **Avançar** para continuar.

7.  Na página **Configurar o Self-Service Portal,** insira o número da porta, o nome do host, o nome do diretório virtual e o caminho de instalação do portal Self-Service.

    **Observação**  
    O número da porta que você especificar deve ser um número de porta não usada no Servidor de Administração e Monitoramento, a menos que você especifique um nome de header de host exclusivo. Se você estiver usando Windows Firewall, a porta será aberta automaticamente.



8.  Clique em **Avançar** para continuar.

9.  Especifique se deve usar as Atualizações da Microsoft para ajudar a manter seu computador seguro e clique em **Próximo**. Isso não ativará Atualizações Automáticas no Windows.

10. Na página **Configurar o Servidor** de Administração e Monitoramento, insira o número da porta, o nome do host, o nome do diretório virtual e o caminho de instalação para o site do Help Desk.

    **Observação**  
    O número da porta que você especificar deve ser um número de porta não usada no Servidor de Administração e Monitoramento, a menos que você especifique um nome de header de host exclusivo. Se você estiver usando Windows Firewall, a porta será aberta automaticamente.



11. Na página **Resumo da** Instalação, revise a lista de recursos que serão instalados e clique em **Instalar** para começar a instalar os recursos do MBAM. Clique **em Voltar** para voltar ao assistente se você tiver que revisar ou alterar suas configurações de instalação ou clicar em **Cancelar** para sair da Instalação. A instalação instala os recursos do MBAM e notifica que a instalação está concluída.

12. Clique **em Concluir** para sair do assistente. Depois que os recursos do Microsoft BitLocker Administration and Monitoring Server foram instalados, continue até a próxima seção e conclua as etapas para adicionar usuários às funções de Administração e Monitoramento do Microsoft BitLocker. Para obter mais informações sobre funções, consulte [Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md).

**Para executar a configuração pós-instalação**

1.  No Servidor de Administração e Monitoramento, adicione usuários aos seguintes grupos locais para lhes dar acesso aos recursos do site do MbaM Help Desk:

    -   **Usuários do MbaM Helpdesk**: Membros desse grupo local podem acessar os recursos de Recuperação de Unidade e Gerenciar TPM no site de Administração e Monitoramento do MBAM. Todos os campos em Recuperação de Unidade e Gerenciar TPM são campos necessários para um Usuário do Helpdesk.

    -   **Usuários avançados do MbaM Helpdesk**: Membros desse grupo local têm acesso avançado aos recursos de Recuperação de Unidade e Gerenciar TPM no site de Administração e Monitoramento do MBAM. Para Usuários Avançados do Helpdesk, somente o campo **ID** de chave é necessário na Recuperação de Unidade. Em Gerenciar TPM, apenas **o** campo Domínio do Computador e o campo **Nome** do Computador são necessários.

2.  No Servidor de Administração e Monitoramento, adicione usuários ao grupo local a seguir para permitir que eles acessem o recurso Relatórios no site de Administração e Monitoramento do MBAM:

    -   **Usuários de Relatório do MBAM**: Membros desse grupo local podem acessar os recursos relatórios no site de Administração e Monitoramento do MBAM.

    -   Brand the Self-Service Portal with your company name, notice text, and other company-specific information. Para obter instruções, [consulte How to Brand the Self-Service Portal](how-to-brand-the-self-service-portal.md).

    **Observação**  
    Associação de usuário ou grupo idêntica ao grupo local de Usuários de Relatório do **MBAM** deve ser mantida em todos os computadores em que os recursos do MbaM Administration and Monitoring Server, o Banco de Dados de Conformidade e Auditoria e Os Relatórios de Conformidade e Auditoria estão instalados. A maneira recomendada de fazer isso é criar um grupo de segurança de domínio e adicionar esse grupo de domínio a cada grupo local de Usuários de Relatório do MBAM. Ao usar esse processo, gerencie as associações de grupo por meio do grupo de domínios.



## <a name="validating-the-mbam-server-feature-installation"></a>Validando a instalação do recurso do MBAM Server


Quando a instalação de Administração e Monitoramento do Microsoft BitLocker for concluída, valide que a instalação tenha sido configurada com êxito todos os recursos de MBAM necessários para o gerenciamento do BitLocker. Use o procedimento a seguir para confirmar se o serviço MBAM está funcional.

**Para validar a instalação do recurso do MBAM Server**

1. Em cada servidor em que um recurso MBAM é implantado, abra **Painel de Controle**. Selecione **Programas**e, em seguida, selecione **Programas e Recursos.** Verifique se a Administração e o Monitoramento do **Microsoft BitLocker** aparecem na lista **Programas e Recursos.**

   **Observação**  
   Para validar a instalação, você deve usar uma conta de domínio que tenha credenciais administrativas de computador local em cada servidor.



2. No servidor onde o Banco de Dados de Recuperação está instalado, abra o SQL Server Management Studio e verifique se o banco de dados de Recuperação e Hardware do **MBAM** está instalado.

3. No servidor onde o Banco de Dados de Conformidade e Auditoria está instalado, abra o SQL Server Management Studio e verifique se o Banco de Dados de Status de Conformidade do **MBAM** está instalado.

4. No servidor onde os Relatórios de Conformidade e Auditoria estão instalados, abra um navegador da Web com credenciais administrativas e navegue até a "Home" do site SQL Server Reporting Services site.

   O local de início padrão de uma SQL Server Reporting Services site está http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports. Para encontrar a URL real, use a ferramenta Reporting Services Configuration Manager e selecione as instâncias especificadas durante a instalação.

   Confirme se uma pasta Relatórios chamada Administração e Monitoramento do Microsoft BitLocker contém uma fonte de dados chamada **MaltaDataSource** e se uma pasta **en-us** contém quatro relatórios.

   **Observação**  
   Se SQL Server Reporting Services foi configurada como uma instância nomeada, a URL deve se parecer com o seguinte:* &lt; http:// NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. No servidor onde o recurso Administração e Monitoramento está instalado, execute **o Gerenciador de** Servidores e navegue até **Funções**. Selecione **Servidor Web (IIS)** e clique **Serviços de Informações da Internet Gerenciador (IIS).**

6. Em **Conexões,** navegue até * &lt; nome do &gt; *computador, selecione **Sites**e selecione Administração e Monitoramento do **Microsoft BitLocker.** Verifique se **MBAMAdministrationService**, **MBAMUserSupportService**, **MBAMComplianceStatusService**e **MBAMRecoveryAndHardwareService** estão listados.

7. No servidor onde os recursos de Administração e Monitoramento e o Portal Self-Service estão instalados, abra um navegador da Web com credenciais administrativas e navegue até os seguintes locais para verificar se eles carregam com êxito:

   -   *http:// &lt; hostname &gt; /HelpDesk/default.aspx* e confirme cada um dos links para navegação e relatórios

   -   *http:// &lt; hostname &gt; /SelfService&gt;/*

   -   *http:// nome &lt; do &gt; computador /MBAMAdministrationService/AdministrationService.svc*

   -   *http:// &lt; hostname &gt; /MBAMUserSupportService/UserSupportService.svc*

   -   *http:// &lt; &gt; nomedocomputador /MBAMComplianceStatusService/StatusReportingService.svc*

   -   *http:// nome &lt; do &gt; computador /MBAMRecoveryAndHardwareService/CoreService.svc*

   **Observação**  
   Presume-se que os recursos do servidor foram instalados na porta padrão sem criptografia de rede. Se você instalou os recursos do servidor em uma porta ou diretório virtual diferente, altere as URLs para incluir a porta apropriada, por exemplo, http:// nome do * &lt; host : porta &gt; &lt; &gt; /HelpDesk/default.asp*x ou http:// nome do*host : porta &lt; &gt; &lt; &gt; / &lt; virtualdirectory &gt; /default.aspx*

   Se os recursos do servidor foram instalados com criptografia de rede, altere http:// para https://.



## <a name="related-topics"></a>Tópicos relacionados


[Implantação da infraestrutura de servidor do MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









