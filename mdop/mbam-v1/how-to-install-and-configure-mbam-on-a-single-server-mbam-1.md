---
title: Como instalar e configurar o MBAM em um servidor único
description: Como instalar e configurar o MBAM em um servidor único
author: dansimp
ms.assetid: 55841c63-bad9-44e7-b7fd-ea7037febbd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 225f66493ceafce5461df3fcc6f701e9a2922a5f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799404"
---
# Como instalar e configurar o MBAM em um servidor único


Os procedimentos neste tópico descrevem a instalação completa dos recursos do Microsoft BitLocker Administration and Monitoring (MBAM) em um único servidor.

Cada recurso do servidor tem determinados pré-requisitos. Para verificar se você cumpriu os pré-requisitos e os requisitos de hardware e software, consulte [pré-requisitos de implantação do MBAM 1,0](mbam-10-deployment-prerequisites.md) e [MBAM 1,0 configurações compatíveis](mbam-10-supported-configurations.md). Além disso, alguns recursos também têm informações que devem ser fornecidas durante o processo de instalação para a implantação bem-sucedida do recurso. Você também deve rever [a preparação do seu ambiente para o MBAM 1,0](preparing-your-environment-for-mbam-10.md) antes de começar a implantação do MBAM.

**Observação**  Para obter os arquivos de log de instalação, você deve instalar o MBAM usando o pacote **msiexec** e a opção **/l** &lt; Location &gt; . Os arquivos de log são criados no local que você especificar.

Arquivos de log de instalação adicionais são criados na pasta% Temp% do usuário que está instalando o MBAM.

 

## Para instalar os recursos do MBAM Server em um único servidor


As etapas a seguir descrevem como instalar os recursos gerais do MBAM.

**Observação**  Certifique-se de usar a configuração de 32 bits em servidores de 32 bits e a configuração de 64 bits em servidores de 64 bits.

 

**Para iniciar a instalação dos recursos do MBAM Server**

1.  Inicie o assistente de instalação do MBAM. Clique em **instalar** na página de boas-vindas.

2.  Leia e aceite os termos de licença para software Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.

3.  Por padrão, todos os recursos do MBAM são selecionados para instalação. Os recursos que serão instalados no mesmo computador deverão ser instalados juntos ao mesmo tempo. Desmarque os recursos que você deseja instalar em outro lugar. Você deve instalar os recursos do MBAM na seguinte ordem:

    -   Recuperação e banco de dados de hardware

    -   Banco de dados de auditoria e conformidade

    -   Auditoria e relatórios de conformidade

    -   Servidor de administração e monitoramento

    -   Modelo de política de grupo MBAM

    **Observação**  O assistente de instalação verifica os pré-requisitos para a sua instalação e exibe os pré-requisitos que estão faltando. Se todos os pré-requisitos forem atendidos, a instalação continuará. Se um pré-requisito ausente for detectado, você deve resolver os pré-requisitos ausentes e clique em **verificar pré-requisitos novamente**. Depois que todos os pré-requisitos forem atendidos, a instalação será retomada.

     

4.  Você será solicitado a configurar a segurança de comunicação de rede. O MBAM pode criptografar a comunicação entre o banco de dados de recuperação e do hardware, o servidor de administração e monitoramento e os clientes. Se você decidir criptografar a comunicação, será solicitado a selecionar o certificado provisionado pela autoridade que será usado para criptografia.

5.  Clique em **Avançar** para continuar.

6.  O assistente de configuração do MBAM exibirá as páginas de instalação dos recursos selecionados.

**Para implantar recursos do MBAM Server**

1.  Na janela **Configurar o banco de dados de recuperação e de hardware** , especifique a instância do SQL Server e o nome do banco de dados que armazenará os dados de recuperação e hardware. Você também deve especificar o local dos arquivos de banco de dados e o local das informações de log.

2.  Clique em **Avançar** para continuar.

3.  Na janela **Configurar o banco de dados de conformidade e auditoria** , especifique a instância do SQL Server e o nome do banco de dados que armazenará os dados de auditoria e conformidade. Em seguida, especifique o local dos arquivos de banco de dados e o local das informações de log.

4.  Clique em **Avançar** para continuar.

5.  Na janela **relatórios de conformidade e auditoria** , especifique a instância do serviço de relatório que será usada e forneça uma conta de usuário de domínio para acessar o banco de dados. Deve ser uma conta de usuário que seja provisionada especificamente para esse uso. A conta de usuário deve poder acessar todos os dados disponíveis para o grupo usuários do MBAM Reports.

6.  Clique em **Avançar** para continuar.

7.  Na janela **Configurar o servidor de administração e monitoração** , insira a **Associação de porta**, o nome do **host** (opcional) e o **caminho de instalação** do servidor de administração e monitoramento do MBAM.

    **Aviso**  O número da porta que você especificar deve ser um número de porta não usado no servidor de administração e monitoramento, a menos que um nome de cabeçalho de host exclusivo seja especificado.

     

8.  Clique em **Avançar** para continuar.

9.  Especifique se deseja usar as atualizações da Microsoft para ajudar a manter seu computador seguro e clique em **Avançar**. A opção atualizações da Microsoft não ativa as atualizações automáticas no Windows.

10. Quando o assistente de configuração coletou as informações de recurso necessárias, a instalação do MBAM está pronta para começar. Clique em **voltar** para voltar ao assistente se desejar revisar ou alterar as configurações de instalação. Clique em **instalar** para começar a instalação. Clique em **Cancelar** para sair da instalação. A instalação instala os recursos do MBAM e avisa que a instalação foi concluída.

11. Clique em **concluir** para sair do assistente.

12. Depois de instalar os recursos do MBAM Server, você deve adicionar usuários às funções MBAM. Para obter mais informações, consulte [planejando funções de administrador do MBAM 1,0](planning-for-mbam-10-administrator-roles.md).

**Para executar a configuração pós-instalação**

1.  Após a conclusão da instalação, você deve adicionar funções de usuário para que você possa conceder aos usuários acesso aos recursos do site de administração do MBAM. No servidor de administração e monitoramento, adicione usuários aos seguintes grupos locais:

    -   **Usuários de hardware do MBAM**: os membros desse grupo local podem acessar o recurso de hardware no site de administração do MBAM.

    -   **Usuários da assistência técnica do MBAM**: os membros desse grupo local podem acessar os recursos de recuperação de unidade e gerenciamento de TPM no site de administração do MBAM. Todos os campos na recuperação de unidade e no gerenciamento de TPM são campos obrigatórios para um usuário da assistência técnica.

    -   **Usuários de helpdesk avançados do MBAM**: os membros desse grupo local têm acesso avançado aos recursos de recuperação de unidade e gerenciamento de TPM no site de administração do MBAM. Para os usuários avançados da assistência técnica, somente o campo ID da chave é necessário na recuperação de unidade. Para gerenciar usuários do TPM, somente os campos domínio do computador e nome do computador são obrigatórios.

2.  No servidor de administração e monitoramento, no banco de dados de conformidade e auditoria e no computador que hospeda os relatórios de conformidade e auditoria, adicione usuários ao grupo local a seguir para permitir que eles acessem o recurso relatórios no site de administração do MBAM:

    -   **Usuários de relatório MBAM**: os membros desse grupo local podem acessar os recursos de relatórios no site de administração do MBAM.

    **Observação**  Associação de usuários idênticas ou associação de grupo do grupo local **usuários de relatórios MBAM** devem ser mantidas em todos os computadores nos quais os recursos de servidor de administração e monitoramento, o banco de dados de conformidade e auditoria e os relatórios de conformidade e auditoria estão instalados.

    Para manter associações idênticas em todos os computadores, você deve criar um grupo de segurança de domínio e adicionar esse grupo de domínio a cada grupo de usuários MBAM de relatório local. Ao fazer isso, você pode gerenciar as associações de grupo usando o grupo de domínio.

     

## Validando a instalação de recursos do servidor MBAM


Quando a instalação do MBAM estiver concluída, valide se a instalação configurou com êxito todos os recursos de MBAM necessários para o gerenciamento do BitLocker. Use o procedimento a seguir para confirmar se o serviço MBAM está funcionando:

**Para validar a instalação de recursos do MBAM Server**

1. Em cada servidor em que um recurso MBAM está implantado, abra o **painel de controle**. Clique em **programas**e, em seguida, clique em **programas e recursos**. Verifique se a **Administração e o monitoramento do Microsoft BitLocker** aparecem na lista **programas e recursos** .

   **Observação**  
   Para validar a instalação, você deve usar uma conta de domínio que tenha credenciais administrativas do computador local em cada servidor.

     

2. No servidor em que o banco de dados de recuperação e de hardware está instalado, abra o SQL Server Management Studio e verifique se o banco de dados de **recuperação e hardware do MBAM** está instalado.

3. No servidor em que o banco de dados de conformidade e auditoria está instalado, abra o SQL Server Management Studio e verifique se o **banco de dados de auditoria e conformidade** com o MBAM está instalado.

4. No servidor em que os relatórios de conformidade e auditoria estiverem instalados, abra um navegador da Web com privilégios administrativos e navegue até a "página inicial" do site do SQL Server Reporting Services.

   O local padrão Home de uma instância do site do SQL Server Reporting Services está em http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /reports. Para localizar a URL real, use a ferramenta Gerenciador de configuração do Reporting Services e selecione as instâncias especificadas durante a instalação.

   Confirme se uma pasta denominada **relatórios de conformidade de Malta** está listada e se contém cinco relatórios e uma fonte de dados.

   **Observação**  
   Se o SQL Server Reporting Services foi configurado como uma instância nomeada, a URL deve ser semelhante à seguinte: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *

     

5. No servidor em que o recurso administração e monitoramento estiver instalado, execute **o Gerenciador de servidores** e navegue até **funções**, selecione **servidor Web (IIS)** e clique em **Gerenciador dos serviços de informações da Internet (IIS)**

6. Em **conexões**, navegue até * &lt; NomeDoComputador &gt; *, selecione **sites**e selecione **Administração e monitoramento do Microsoft BitLocker**. Verifique se **MBAMAdministrationService**, **MBAMComplianceStatusService**e **MBAMRecoveryAndHardwareService** estão listados.

7. No servidor em que o recurso administração e monitoramento estiver instalado, abra um navegador da Web com privilégios administrativos e navegue até os seguintes locais no site do MBAM para verificar se eles são carregados com êxito:

   -   *http:// &lt; NomeDoComputador &gt; /Default.aspx* e confirme cada um dos links para navegação e relatórios

   -   *http:// &lt; nome_do_computador &gt; /MBAMAdministrationService/AdministrationService.svc*

   -   *http:// &lt; nome_do_computador &gt; /MBAMComplianceStatusService/StatusReportingService.svc*

   -   *http:// &lt; nome_do_computador &gt; /MBAMRecoveryAndHardwareService/CoreService.svc*

   **Observação**  
   Normalmente, os serviços são instalados na porta padrão 80 sem criptografia de rede. Se os serviços estiverem instalados em uma porta diferente, altere as URLs para incluir a porta apropriada. Por exemplo, http://* &lt; ComputerName &gt; : &lt; Port &gt; */default.aspx ou http:// <em> &lt; hostheadername &gt; / </em> Default. aspx.

   Se os serviços estiverem instalados com a criptografia de rede, altere http://para https://.

     

## Tópicos relacionados


[Implantando a infraestrutura do Servidor do MBAM 1.0](deploying-the-mbam-10-server-infrastructure.md)

 

 





