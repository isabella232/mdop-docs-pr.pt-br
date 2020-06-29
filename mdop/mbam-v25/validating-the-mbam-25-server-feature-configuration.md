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
# <span data-ttu-id="f9f66-103">Validando a configuração de recursos de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f9f66-103">Validating the MBAM 2.5 Server Feature Configuration</span></span>


<span data-ttu-id="f9f66-104">Quando você concluir a implantação de recursos do servidor do Microsoft BitLocker Administration and Monitoring (MBAM) 2,5, recomendamos que valide a implantação para garantir que todos os recursos tenham sido configurados com êxito.</span><span class="sxs-lookup"><span data-stu-id="f9f66-104">When you finish the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server feature deployment, we recommend that you validate the deployment to ensure that all features have been successfully configured.</span></span> <span data-ttu-id="f9f66-105">Use o procedimento que corresponda à topologia (autônoma ou integração do System Center Configuration Manager) que você implantou.</span><span class="sxs-lookup"><span data-stu-id="f9f66-105">Use the procedure that matches the topology (Stand-alone or System Center Configuration Manager Integration) that you deployed.</span></span>

## <span data-ttu-id="f9f66-106">Validando a implantação do servidor MBAM com a topologia autônoma</span><span class="sxs-lookup"><span data-stu-id="f9f66-106">Validating the MBAM Server deployment with the Stand-alone topology</span></span>


<span data-ttu-id="f9f66-107">Use as etapas a seguir para validar a implantação do MBAM Server com a topologia autônoma.</span><span class="sxs-lookup"><span data-stu-id="f9f66-107">Use the following steps to validate your MBAM Server deployment with the Stand-alone topology.</span></span>

**<span data-ttu-id="f9f66-108">Para validar uma implantação autônoma do servidor MBAM</span><span class="sxs-lookup"><span data-stu-id="f9f66-108">To validate a Stand-alone MBAM Server deployment</span></span>**

1.  <span data-ttu-id="f9f66-109">Em cada servidor em que um recurso do MBAM é implantado, clique em programas **Control Panel** &gt; **Programs** &gt; **e recursos**do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="f9f66-109">On each server where an MBAM feature is deployed, click **Control Panel** &gt; **Programs** &gt; **Programs and Features**.</span></span> <span data-ttu-id="f9f66-110">Verifique se a **Administração e o monitoramento do Microsoft BitLocker** aparecem na lista **programas e recursos** .</span><span class="sxs-lookup"><span data-stu-id="f9f66-110">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

    **<span data-ttu-id="f9f66-111">Observação</span><span class="sxs-lookup"><span data-stu-id="f9f66-111">Note</span></span>**  
    <span data-ttu-id="f9f66-112">Para fazer a validação, você deve usar uma conta de domínio que tenha credenciais administrativas do computador local em cada servidor.</span><span class="sxs-lookup"><span data-stu-id="f9f66-112">To do the validation, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2.  <span data-ttu-id="f9f66-113">No servidor em que o banco de dados de recuperação está configurado, abra o SQL Server Management Studio e verifique se o banco de dados de **recuperação e hardware do MBAM** está configurado.</span><span class="sxs-lookup"><span data-stu-id="f9f66-113">On the server where the Recovery Database is configured, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is configured.</span></span>

3.  <span data-ttu-id="f9f66-114">No servidor em que o banco de dados de conformidade e auditoria está configurado, abra o SQL Server Management Studio e verifique se o **banco de dados de status de conformidade do MBAM** está configurado.</span><span class="sxs-lookup"><span data-stu-id="f9f66-114">On the server where the Compliance and Audit Database is configured, open SQL Server Management Studio and verify that the **MBAM Compliance Status Database** is configured.</span></span>

4.  <span data-ttu-id="f9f66-115">No servidor em que o recurso relatórios está configurado, abra um navegador da Web com credenciais administrativas e navegue até a "página inicial" do site do SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="f9f66-115">On the server where the Reports feature is configured, open a web browser with administrative credentials and browse to the "Home" of the SQL Server Reporting Services site.</span></span>

    <span data-ttu-id="f9f66-116">O local padrão Home de uma instância do site do SQL Server Reporting Services está em:</span><span class="sxs-lookup"><span data-stu-id="f9f66-116">The default Home location of a SQL Server Reporting Services site instance is at:</span></span>

    <span data-ttu-id="f9f66-117">http (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *porta* &gt; /reports.aspx</span><span class="sxs-lookup"><span data-stu-id="f9f66-117">http(s)://&lt; *MBAMReportsServerName*&gt;:&lt;*port*&gt;/Reports.aspx</span></span>

    <span data-ttu-id="f9f66-118">Para localizar a URL real, use a ferramenta Gerenciador de configuração do Reporting Services e selecione as instâncias que você especificou durante a configuração.</span><span class="sxs-lookup"><span data-stu-id="f9f66-118">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances that you specified during setup.</span></span>

5.  <span data-ttu-id="f9f66-119">Confirme se uma pasta de relatórios chamada **Administração e administração do Microsoft BitLocker** contém uma fonte de dados chamada **MaltaDataSource** , bem como as pastas de idiomas.</span><span class="sxs-lookup"><span data-stu-id="f9f66-119">Confirm that a reports folder named **Microsoft BitLocker Administration and Monitoring** contains a data source called **MaltaDataSource** as well as the language folders.</span></span> <span data-ttu-id="f9f66-120">A fonte de dados contém pastas com nomes que representam idiomas (por exemplo, en-US).</span><span class="sxs-lookup"><span data-stu-id="f9f66-120">The data source contains folders with names that represent languages (for example, en-us).</span></span> <span data-ttu-id="f9f66-121">Os relatórios estão nas pastas de idiomas.</span><span class="sxs-lookup"><span data-stu-id="f9f66-121">The reports are in the language folders.</span></span>

    **<span data-ttu-id="f9f66-122">Observação</span><span class="sxs-lookup"><span data-stu-id="f9f66-122">Note</span></span>**  
    <span data-ttu-id="f9f66-123">Se o SQL Server Reporting Services (SSRS) foi configurado como uma instância nomeada, a URL deve ser semelhante à seguinte: http (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *porta* &gt; /Reports\_ &lt; *SSRSInstanceName*&gt;</span><span class="sxs-lookup"><span data-stu-id="f9f66-123">If SQL Server Reporting Services (SSRS) was configured as a named instance, the URL should resemble the following: http(s)://&lt; *MBAMReportsServerName*&gt;:&lt;*port*&gt;/Reports\_&lt;*SSRSInstanceName*&gt;</span></span>



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring Website (also known as Help Desk) and select a report, the following message appears: "Only Secure Content is Displayed." To show the report, click **Show All Content**.
~~~



6. <span data-ttu-id="f9f66-124">No servidor em que o recurso de site Administração e monitoramento está configurado, execute o **Gerenciador de servidores**, navegue até **funções**e, em seguida, selecione **servidor Web (IIS)** &gt; **Gerenciador de serviços de informações da Internet (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="f9f66-124">On the server where the Administration and Monitoring Website feature is configured, run **Server Manager**, browse to **Roles**, and then select **Web Server (IIS)** &gt; **Internet Information Services (IIS) Manager**.</span></span>

7. <span data-ttu-id="f9f66-125">Em **conexões**, navegue até o \* &lt; nome &gt; do computador\* e selecione **sites** &gt; **Administração e monitoramento do Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="f9f66-125">In **Connections**, browse to *&lt;computer name&gt;* and select **Sites** &gt; **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="f9f66-126">Verifique se os seguintes itens estão listados:</span><span class="sxs-lookup"><span data-stu-id="f9f66-126">Verify that the following are listed:</span></span>

   -   **<span data-ttu-id="f9f66-127">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="f9f66-127">MBAMAdministrationService</span></span>**

   -   **<span data-ttu-id="f9f66-128">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="f9f66-128">MBAMComplianceStatusService</span></span>**

   -   **<span data-ttu-id="f9f66-129">MBAMRecoveryAndHardwareService</span><span class="sxs-lookup"><span data-stu-id="f9f66-129">MBAMRecoveryAndHardwareService</span></span>**

8. <span data-ttu-id="f9f66-130">No servidor em que o site de administração e monitoramento e o portal de autoatendimento estão configurados, abra um navegador da Web com credenciais administrativas.</span><span class="sxs-lookup"><span data-stu-id="f9f66-130">On the server where the Administration and Monitoring Website and Self-Service Portal are configured, open a web browser with administrative credentials.</span></span>

9. <span data-ttu-id="f9f66-131">Navegue até os seguintes websites para verificar se eles são carregados com êxito:</span><span class="sxs-lookup"><span data-stu-id="f9f66-131">Browse to the following websites to verify that they load successfully:</span></span>

   -   <span data-ttu-id="f9f66-132">https (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /helpdesk/-confirme cada um dos links para navegação e relatórios</span><span class="sxs-lookup"><span data-stu-id="f9f66-132">https(s)://&lt;*MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/HelpDesk/ - confirm each of the links for navigation and reports</span></span>

   -   <span data-ttu-id="f9f66-133">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /SelfService/</span><span class="sxs-lookup"><span data-stu-id="f9f66-133">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/SelfService/</span></span>

   **<span data-ttu-id="f9f66-134">Observação</span><span class="sxs-lookup"><span data-stu-id="f9f66-134">Note</span></span>**  
   <span data-ttu-id="f9f66-135">Pressupõe-se que você configurou os recursos do servidor na porta padrão sem criptografia de rede.</span><span class="sxs-lookup"><span data-stu-id="f9f66-135">It is assumed that you configured the server features on the default port without network encryption.</span></span> <span data-ttu-id="f9f66-136">Se você configurou os recursos de servidor em uma porta ou diretório virtual diferente, altere as URLs para incluir a porta apropriada, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f9f66-136">If you configured the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example:</span></span>

   <span data-ttu-id="f9f66-137">http (s):// &lt; *nome do host* &gt; : &lt; *porta* &gt; /helpdesk/</span><span class="sxs-lookup"><span data-stu-id="f9f66-137">http(s)://&lt; *host name*&gt;:&lt;*port*&gt;/HelpDesk/</span></span>

   <span data-ttu-id="f9f66-138">http (s):// &lt; *nome do host* &gt; : &lt; *porta* &gt; / &lt; *VirtualDirectory*&gt;/</span><span class="sxs-lookup"><span data-stu-id="f9f66-138">http(s)://&lt; *host name*&gt;:&lt;*port*&gt;/&lt;*virtualdirectory*&gt;/</span></span>

   <span data-ttu-id="f9f66-139">Se os recursos do servidor foram configurados com a criptografia de rede, altere http://para https://.</span><span class="sxs-lookup"><span data-stu-id="f9f66-139">If the server features were configured with network encryption, change http:// to https://.</span></span>



10. <span data-ttu-id="f9f66-140">Navegue até os serviços da Web a seguir para verificar se eles são carregados com êxito.</span><span class="sxs-lookup"><span data-stu-id="f9f66-140">Browse to the following web services to verify that they load successfully.</span></span> <span data-ttu-id="f9f66-141">Uma página abre para indicar que o serviço está em execução, mas a página não exibe metadados.</span><span class="sxs-lookup"><span data-stu-id="f9f66-141">A page opens to indicate that the service is running, but the page does not display any metadata.</span></span>

    -   <span data-ttu-id="f9f66-142">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="f9f66-142">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>

    -   <span data-ttu-id="f9f66-143">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /MBAMUserSupportService/UserSupportService.svc</span><span class="sxs-lookup"><span data-stu-id="f9f66-143">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMUserSupportService/UserSupportService.svc</span></span>

    -   <span data-ttu-id="f9f66-144">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="f9f66-144">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>

    -   <span data-ttu-id="f9f66-145">http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="f9f66-145">http(s)://&lt; *MBAMAdministrationServerName*&gt;:&lt;*port*&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>

## <span data-ttu-id="f9f66-146">Validando a implantação do servidor MBAM com a topologia de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f9f66-146">Validating the MBAM Server deployment with the Configuration Manager Integration topology</span></span>


<span data-ttu-id="f9f66-147">Use as etapas a seguir para validar a implantação do MBAM com a topologia de integração do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f9f66-147">Use the following steps to validate your MBAM deployment with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="f9f66-148">Conclua as etapas de validação correspondentes à versão do Configuration Manager que você está usando.</span><span class="sxs-lookup"><span data-stu-id="f9f66-148">Complete the validation steps that match the version of Configuration Manager that you are using.</span></span>

### <a href="" id="validating-the-mbam-server-deployment-with-system-center-2012-configuration-manager-"></a><span data-ttu-id="f9f66-149">Validando a implantação do servidor MBAM com o System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f9f66-149">Validating the MBAM Server deployment with System Center 2012 Configuration Manager</span></span>

<span data-ttu-id="f9f66-150">Use estas etapas para validar a implantação do MBAM Server quando estiver usando o MBAM com o System Center 2012 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f9f66-150">Use these steps to validate your MBAM Server deployment when you are using MBAM with System Center 2012 Configuration Manager.</span></span>

**<span data-ttu-id="f9f66-151">Para validar uma implantação do Configuration Manager MBAM implantação do servidor – System Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f9f66-151">To validate a Configuration Manager Integration MBAM Server deployment – System Center 2012 Configuration Manager</span></span>**

1.  <span data-ttu-id="f9f66-152">No servidor em que o System Center 2012 Configuration Manager é implantado, abra **programas e recursos** no **painel de controle**e verifique se a **Administração e o monitoramento do Microsoft BitLocker** são exibidos.</span><span class="sxs-lookup"><span data-stu-id="f9f66-152">On the server where System Center 2012 Configuration Manager is deployed, open **Programs and Features** in **Control Panel**, and verify that **Microsoft BitLocker Administration and Monitoring** appears.</span></span>

    **<span data-ttu-id="f9f66-153">Observação</span><span class="sxs-lookup"><span data-stu-id="f9f66-153">Note</span></span>**  
    <span data-ttu-id="f9f66-154">Para validar a configuração, você deve usar uma conta de domínio que tenha credenciais administrativas do computador local em cada servidor.</span><span class="sxs-lookup"><span data-stu-id="f9f66-154">To validate the configuration, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2.  <span data-ttu-id="f9f66-155">No console do Configuration Manager, clique nos conjuntos de dispositivos do espaço de trabalho de **conformidade e ativos** e &gt; **Device Collections**confirme se uma nova coleção chamada **MBAM de computadores com suporte** é exibida.</span><span class="sxs-lookup"><span data-stu-id="f9f66-155">In the Configuration Manager console, click the **Assets and Compliance** workspace &gt; **Device Collections**, and confirm that a new collection called **MBAM Supported Computers** is displayed.</span></span>

3.  <span data-ttu-id="f9f66-156">No console do Configuration Manager, clique na guia relatórios de relatório do espaço de trabalho de **monitoramento** &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="f9f66-156">In the Configuration Manager console, click the **Monitoring** workspace &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.</span></span>

4.  <span data-ttu-id="f9f66-157">Verifique se a pasta **MBAM** contém subpastas, com nomes que representam idiomas diferentes, e se os seguintes relatórios estão listados em cada subpasta de idioma:</span><span class="sxs-lookup"><span data-stu-id="f9f66-157">Verify that the **MBAM** folder contains subfolders, with names that represent different languages, and that the following reports are listed in each language subfolder:</span></span>

    -   <span data-ttu-id="f9f66-158">Conformidade do computador BitLocker</span><span class="sxs-lookup"><span data-stu-id="f9f66-158">BitLocker Computer Compliance</span></span>

    -   <span data-ttu-id="f9f66-159">Painel de conformidade do BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="f9f66-159">BitLocker Enterprise Compliance Dashboard</span></span>

    -   <span data-ttu-id="f9f66-160">Detalhes de conformidade corporativa do BitLocker</span><span class="sxs-lookup"><span data-stu-id="f9f66-160">BitLocker Enterprise Compliance Details</span></span>

    -   <span data-ttu-id="f9f66-161">Resumo de conformidade empresarial do BitLocker</span><span class="sxs-lookup"><span data-stu-id="f9f66-161">BitLocker Enterprise Compliance Summary</span></span>

5.  <span data-ttu-id="f9f66-162">No console do Configuration Manager, clique nas linhas de base de configuração de conformidade do espaço de trabalho de **ativos e ativos** &gt; **Compliance Settings** &gt; **Configuration Baselines**e confirme se a linha de base de configuração **proteção BitLocker** está listada.</span><span class="sxs-lookup"><span data-stu-id="f9f66-162">In the Configuration Manager console, click the **Assets and Compliance** workspace &gt; **Compliance Settings** &gt; **Configuration Baselines**, and confirm that the configuration baseline **BitLocker Protection** is listed.</span></span>

6.  <span data-ttu-id="f9f66-163">No console do Configuration Manager, clique nos itens de configuração de compatibilidade de espaço de trabalho de **ativos e ativos** &gt; **Compliance Settings** &gt; **Configuration Items**e confirme se os seguintes itens de configuração novos são exibidos:</span><span class="sxs-lookup"><span data-stu-id="f9f66-163">In the Configuration Manager console, click the **Assets and Compliance** workspace &gt; **Compliance Settings** &gt; **Configuration Items**, and confirm that the following new configuration items are displayed:</span></span>

    -   <span data-ttu-id="f9f66-164">Proteção de unidades de dados fixas do BitLocker</span><span class="sxs-lookup"><span data-stu-id="f9f66-164">BitLocker Fixed Data Drives Protection</span></span>

    -   <span data-ttu-id="f9f66-165">Proteção de unidade do sistema operacional BitLocker</span><span class="sxs-lookup"><span data-stu-id="f9f66-165">BitLocker Operating System Drive Protection</span></span>

### <span data-ttu-id="f9f66-166">Validando a implantação do servidor MBAM com o Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="f9f66-166">Validating the MBAM Server deployment with Configuration Manager 2007</span></span>

<span data-ttu-id="f9f66-167">Use estas etapas para validar a implantação do MBAM Server quando estiver usando o MBAM com o Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="f9f66-167">Use these steps to validate your MBAM Server deployment when you are using MBAM with Configuration Manager 2007.</span></span>

**<span data-ttu-id="f9f66-168">Para validar uma implantação do Configuration Manager Integration MBAM Server Deployment – Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="f9f66-168">To validate a Configuration Manager Integration MBAM Server deployment – Configuration Manager 2007</span></span>**

1.  <span data-ttu-id="f9f66-169">No servidor em que o Configuration Manager 2007 é implantado, abra **programas e recursos** no **painel de controle** e verifique se a **Administração e o monitoramento do Microsoft BitLocker** são exibidos.</span><span class="sxs-lookup"><span data-stu-id="f9f66-169">On the server where Configuration Manager 2007 is deployed, open **Programs and Features** on **Control Panel** , and verify that **Microsoft BitLocker Administration and Monitoring** appears.</span></span>

    **<span data-ttu-id="f9f66-170">Observação</span><span class="sxs-lookup"><span data-stu-id="f9f66-170">Note</span></span>**  
    <span data-ttu-id="f9f66-171">Para validar a configuração, você deve usar uma conta de domínio que tenha credenciais administrativas do computador local em cada servidor.</span><span class="sxs-lookup"><span data-stu-id="f9f66-171">To validate the configuration, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2.  <span data-ttu-id="f9f66-172">No console do Configuration Manager, clique em **site Database &lt; Sitecom &gt;  -  &lt; nome_do_servidor &gt; , &lt; SiteName &gt; ), gerenciamento do computador**e confirme se uma nova coleção chamada **MBAM Computer Supported** é exibida.</span><span class="sxs-lookup"><span data-stu-id="f9f66-172">In the Configuration Manager console, click **Site Database &lt;SiteCode&gt; - &lt;ServerName&gt;, &lt;SiteName&gt;), Computer Management**, and confirm that a new collection called **MBAM Supported Computers** is displayed.</span></span>

3.  <span data-ttu-id="f9f66-173">No console do Configuration Manager, clique em relatórios de pastas do relatório do **Reporting** &gt; **Services** &gt; \*\* \\\\ &lt; Server &gt; \*\* &gt; **Report Folders** &gt; **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="f9f66-173">In the Configuration Manager console, click **Reporting** &gt; **Reporting Services** &gt; **\\\\&lt;ServerName&gt;** &gt; **Report Folders** &gt; **MBAM**.</span></span>

    <span data-ttu-id="f9f66-174">Verifique se a pasta **MBAM** contém subpastas, com nomes que representam idiomas diferentes, e se os seguintes relatórios estão listados em cada subpasta de idioma:</span><span class="sxs-lookup"><span data-stu-id="f9f66-174">Verify that the **MBAM** folder contains subfolders, with names that represent different languages, and that the following reports are listed in each language subfolder:</span></span>

    -   <span data-ttu-id="f9f66-175">Conformidade do computador BitLocker</span><span class="sxs-lookup"><span data-stu-id="f9f66-175">BitLocker Computer Compliance</span></span>

    -   <span data-ttu-id="f9f66-176">Painel de conformidade do BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="f9f66-176">BitLocker Enterprise Compliance Dashboard</span></span>

    -   <span data-ttu-id="f9f66-177">Detalhes de conformidade corporativa do BitLocker</span><span class="sxs-lookup"><span data-stu-id="f9f66-177">BitLocker Enterprise Compliance Details</span></span>

    -   <span data-ttu-id="f9f66-178">Resumo de conformidade empresarial do BitLocker</span><span class="sxs-lookup"><span data-stu-id="f9f66-178">BitLocker Enterprise Compliance Summary</span></span>

4.  <span data-ttu-id="f9f66-179">No console do Configuration Manager, clique em linhas de base de configuração do **Gerenciamento de configuração desejado** &gt; **Configuration Baselines**e confirme se a configuração **proteção do BitLocker** da linha de base de configuração está listada.</span><span class="sxs-lookup"><span data-stu-id="f9f66-179">In the Configuration Manager console, click **Desired Configuration Management** &gt; **Configuration Baselines**, and confirm that the configuration baseline **BitLocker Protection** is listed.</span></span>

5.  <span data-ttu-id="f9f66-180">No console do Configuration Manager, clique em itens de configuração de **Gerenciamento de configuração desejada** &gt; **Configuration Items**e confirme se os seguintes itens de configuração novos são exibidos:</span><span class="sxs-lookup"><span data-stu-id="f9f66-180">In the Configuration Manager console, click **Desired Configuration Management** &gt; **Configuration Items**, and confirm that the following new configuration items are displayed:</span></span>

    -   <span data-ttu-id="f9f66-181">Proteção de unidades de dados fixas do BitLocker</span><span class="sxs-lookup"><span data-stu-id="f9f66-181">BitLocker Fixed Data Drives Protection</span></span>

    -   <span data-ttu-id="f9f66-182">Proteção de unidade do sistema operacional BitLocker</span><span class="sxs-lookup"><span data-stu-id="f9f66-182">BitLocker Operating System Drive Protection</span></span>



## <span data-ttu-id="f9f66-183">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9f66-183">Related topics</span></span>


[<span data-ttu-id="f9f66-184">Configurando os recursos de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f9f66-184">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)


## <span data-ttu-id="f9f66-185">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="f9f66-185">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="f9f66-186">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="f9f66-186">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="f9f66-187">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="f9f66-187">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






