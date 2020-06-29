---
title: Validando a configuração de recursos de servidor do MBAM 2.5
description: Validando a configuração de recursos de servidor do MBAM 2.5
author: dansimp
ms.assetid: f4983a33-ce18-4186-a471-dd6415940504
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f955e0b9ccb7952995574e4aa981674f7c7667fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800001"
---
# Validando a configuração de recursos de servidor do MBAM 2.5


Quando você concluir a implantação de recursos do servidor do Microsoft BitLocker Administration and Monitoring (MBAM) 2,5, recomendamos que valide a implantação para garantir que todos os recursos tenham sido configurados com êxito. Use o procedimento que corresponda à topologia (autônoma ou integração do System Center Configuration Manager) que você implantou.

## Validando a implantação do servidor MBAM com a topologia autônoma


Use as etapas a seguir para validar a implantação do MBAM Server com a topologia autônoma.

**Para validar uma implantação autônoma do servidor MBAM**

1.  Em cada servidor em que um recurso do MBAM é implantado, clique em programas **Control Panel** &gt; **Programs** &gt; **e recursos**do painel de controle. Verifique se a **Administração e o monitoramento do Microsoft BitLocker** aparecem na lista **programas e recursos** .

    **Observação**  
    Para fazer a validação, você deve usar uma conta de domínio que tenha credenciais administrativas do computador local em cada servidor.



2.  No servidor em que o banco de dados de recuperação está configurado, abra o SQL Server Management Studio e verifique se o banco de dados de **recuperação e hardware do MBAM** está configurado.

3.  No servidor em que o banco de dados de conformidade e auditoria está configurado, abra o SQL Server Management Studio e verifique se o **banco de dados de status de conformidade do MBAM** está configurado.

4.  No servidor em que o recurso relatórios está configurado, abra um navegador da Web com credenciais administrativas e navegue até a "página inicial" do site do SQL Server Reporting Services.

    O local padrão Home de uma instância do site do SQL Server Reporting Services está em:

    http (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *porta* &gt; /reports.aspx

    Para localizar a URL real, use a ferramenta Gerenciador de configuração do Reporting Services e selecione as instâncias que você especificou durante a configuração.

5.  Confirme se uma pasta de relatórios chamada **Administração e administração do Microsoft BitLocker** contém uma fonte de dados chamada **MaltaDataSource** , bem como as pastas de idiomas. A fonte de dados contém pastas com nomes que representam idiomas (por exemplo, en-US). Os relatórios estão nas pastas de idiomas.

    **Observação**  
    Se o SQL Server Reporting Services (SSRS) foi configurado como uma instância nomeada, a URL deve ser semelhante à seguinte: http (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *porta* &gt; /Reports\_ &lt; *SSRSInstanceName*&gt;



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring Website (also known as Help Desk) and select a report, the following message appears: "Only Secure Content is Displayed." To show the report, click **Show All Content**.
~~~



6. No servidor em que o recurso de site Administração e monitoramento está configurado, execute o **Gerenciador de servidores**, navegue até **funções**e, em seguida, selecione **servidor Web (IIS)** &gt; **Gerenciador de serviços de informações da Internet (IIS)**.

7. Em **conexões**, navegue até o * &lt; nome &gt; do computador* e selecione **sites** &gt; **Administração e monitoramento do Microsoft BitLocker**. Verifique se os seguintes itens estão listados:

   -   **MBAMAdministrationService**

   -   **MBAMComplianceStatusService**

   -   **MBAMRecoveryAndHardwareService**

8. No servidor em que o site de administração e monitoramento e o portal de autoatendimento estão configurados, abra um navegador da Web com credenciais administrativas.

9. Navegue até os seguintes websites para verificar se eles são carregados com êxito:

   -   https (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /helpdesk/-confirme cada um dos links para navegação e relatórios

   -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /SelfService/

   **Observação**  
   Pressupõe-se que você configurou os recursos do servidor na porta padrão sem criptografia de rede. Se você configurou os recursos de servidor em uma porta ou diretório virtual diferente, altere as URLs para incluir a porta apropriada, por exemplo:

   http (s):// &lt; *nome do host* &gt; : &lt; *porta* &gt; /helpdesk/

   http (s):// &lt; *nome do host* &gt; : &lt; *porta* &gt; / &lt; *VirtualDirectory*&gt;/

   Se os recursos do servidor foram configurados com a criptografia de rede, altere http://para https://.



10. Navegue até os serviços da Web a seguir para verificar se eles são carregados com êxito. Uma página abre para indicar que o serviço está em execução, mas a página não exibe metadados.

    -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /MBAMAdministrationService/AdministrationService.svc

    -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /MBAMUserSupportService/UserSupportService.svc

    -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /MBAMComplianceStatusService/StatusReportingService.svc

    -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /MBAMRecoveryAndHardwareService/CoreService.svc

## Validando a implantação do servidor MBAM com a topologia de integração do Configuration Manager


Use as etapas a seguir para validar a implantação do MBAM com a topologia de integração do Configuration Manager. Conclua as etapas de validação correspondentes à versão do Configuration Manager que você está usando.

### <a href="" id="validating-the-mbam-server-deployment-with-system-center-2012-configuration-manager-"></a>Validando a implantação do servidor MBAM com o System Center 2012 Configuration Manager

Use estas etapas para validar a implantação do MBAM Server quando estiver usando o MBAM com o System Center 2012 Configuration Manager.

**Para validar uma implantação do Configuration Manager MBAM implantação do servidor – System Center 2012 Configuration Manager**

1.  No servidor em que o System Center 2012 Configuration Manager é implantado, abra **programas e recursos** no **painel de controle**e verifique se a **Administração e o monitoramento do Microsoft BitLocker** são exibidos.

    **Observação**  
    Para validar a configuração, você deve usar uma conta de domínio que tenha credenciais administrativas do computador local em cada servidor.



2.  No console do Configuration Manager, clique nos conjuntos de dispositivos do espaço de trabalho de **conformidade e ativos** e &gt; **Device Collections**confirme se uma nova coleção chamada **MBAM de computadores com suporte** é exibida.

3.  No console do Configuration Manager, clique na guia relatórios de relatório do espaço de trabalho de **monitoramento** &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.

4.  Verifique se a pasta **MBAM** contém subpastas, com nomes que representam idiomas diferentes, e se os seguintes relatórios estão listados em cada subpasta de idioma:

    -   Conformidade do computador BitLocker

    -   Painel de conformidade do BitLocker Enterprise

    -   Detalhes de conformidade corporativa do BitLocker

    -   Resumo de conformidade empresarial do BitLocker

5.  No console do Configuration Manager, clique nas linhas de base de configuração de conformidade do espaço de trabalho de **ativos e ativos** &gt; **Compliance Settings** &gt; **Configuration Baselines**e confirme se a linha de base de configuração **proteção BitLocker** está listada.

6.  No console do Configuration Manager, clique nos itens de configuração de compatibilidade de espaço de trabalho de **ativos e ativos** &gt; **Compliance Settings** &gt; **Configuration Items**e confirme se os seguintes itens de configuração novos são exibidos:

    -   Proteção de unidades de dados fixas do BitLocker

    -   Proteção de unidade do sistema operacional BitLocker

### Validando a implantação do servidor MBAM com o Configuration Manager 2007

Use estas etapas para validar a implantação do MBAM Server quando estiver usando o MBAM com o Configuration Manager 2007.

**Para validar uma implantação do Configuration Manager Integration MBAM Server Deployment – Configuration Manager 2007**

1.  No servidor em que o Configuration Manager 2007 é implantado, abra **programas e recursos** no **painel de controle** e verifique se a **Administração e o monitoramento do Microsoft BitLocker** são exibidos.

    **Observação**  
    Para validar a configuração, você deve usar uma conta de domínio que tenha credenciais administrativas do computador local em cada servidor.



2.  No console do Configuration Manager, clique em **site Database &lt; Sitecom &gt;  -  &lt; nome_do_servidor &gt; , &lt; SiteName &gt; ), gerenciamento do computador**e confirme se uma nova coleção chamada **MBAM Computer Supported** é exibida.

3.  No console do Configuration Manager, clique em relatórios de pastas do relatório do **Reporting** &gt; **Services** &gt; ** \\\\ &lt; Server &gt; ** &gt; **Report Folders** &gt; **MBAM**.

    Verifique se a pasta **MBAM** contém subpastas, com nomes que representam idiomas diferentes, e se os seguintes relatórios estão listados em cada subpasta de idioma:

    -   Conformidade do computador BitLocker

    -   Painel de conformidade do BitLocker Enterprise

    -   Detalhes de conformidade corporativa do BitLocker

    -   Resumo de conformidade empresarial do BitLocker

4.  No console do Configuration Manager, clique em linhas de base de configuração do **Gerenciamento de configuração desejado** &gt; **Configuration Baselines**e confirme se a configuração **proteção do BitLocker** da linha de base de configuração está listada.

5.  No console do Configuration Manager, clique em itens de configuração de **Gerenciamento de configuração desejada** &gt; **Configuration Items**e confirme se os seguintes itens de configuração novos são exibidos:

    -   Proteção de unidades de dados fixas do BitLocker

    -   Proteção de unidade do sistema operacional BitLocker



## Tópicos relacionados


[Configurando os recursos de servidor do MBAM 2.5](configuring-the-mbam-25-server-features.md)


## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






