---
title: Avaliando o MBAM 2.5 em um ambiente de teste
description: Avaliando o MBAM 2.5 em um ambiente de teste
author: dansimp
ms.assetid: 72959b7a-e55f-4797-91b3-5be23c8c2844
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d7ba8a62f5ddecf85fe56e04fc16a6bae374ba9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799215"
---
# <span data-ttu-id="465d3-103">Avaliando o MBAM 2.5 em um ambiente de teste</span><span class="sxs-lookup"><span data-stu-id="465d3-103">Evaluating MBAM 2.5 in a Test Environment</span></span>


<span data-ttu-id="465d3-104">Este tópico descreve como você pode configurar um ambiente de teste para avaliar a administração e o monitoramento do Microsoft BitLocker (MBAM) 2,5 na topologia autônoma ou de integração do System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="465d3-104">This topic describes how you can set up a test environment to evaluate Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in the Stand-alone or System Center Configuration Manager Integration topology.</span></span>

## <span data-ttu-id="465d3-105">Avaliando o MBAM 2,5 usando a topologia autônoma</span><span class="sxs-lookup"><span data-stu-id="465d3-105">Evaluating MBAM 2.5 by using the Stand-alone topology</span></span>


<span data-ttu-id="465d3-106">Para avaliar o MBAM usando a topologia autônoma, use as informações contidas nas tabelas a seguir para instalar o software do servidor do MBAM e configure os recursos do servidor MBAM em seu ambiente de teste.</span><span class="sxs-lookup"><span data-stu-id="465d3-106">To evaluate MBAM by using the Stand-alone topology, use the information in the following tables to install the MBAM Server software, and then configure the MBAM Server features in your test environment.</span></span>

**<span data-ttu-id="465d3-107">Para avaliar o MBAM 2,5 usando a topologia autônoma</span><span class="sxs-lookup"><span data-stu-id="465d3-107">To evaluate MBAM 2.5 by using the Stand-alone topology</span></span>**

1. <span data-ttu-id="465d3-108">Antes de instalar o MBAM, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="465d3-108">Before installing MBAM, do the following:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="465d3-109">Tarefa</span><span class="sxs-lookup"><span data-stu-id="465d3-109">Task</span></span></th>
   <th align="left"><span data-ttu-id="465d3-110">Onde obter instruções</span><span class="sxs-lookup"><span data-stu-id="465d3-110">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="465d3-111">Verifique se você instalou todo o software de pré-requisito.</span><span class="sxs-lookup"><span data-stu-id="465d3-111">Ensure that you have installed all of the prerequisite software.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="465d3-112">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="465d3-112">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="465d3-113">Verifique o hardware, a RAM e outras especificações necessárias.</span><span class="sxs-lookup"><span data-stu-id="465d3-113">Check the required hardware, RAM, and other specifications.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="465d3-114">Configurações com suporte no MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="465d3-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="465d3-115">Examine os pré-requisitos para usar o Windows PowerShell se você planeja usar os cmdlets para configurar o MBAM.</span><span class="sxs-lookup"><span data-stu-id="465d3-115">Review the prerequisites for using Windows PowerShell if you plan to use the cmdlets to configure MBAM.</span></span></p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="465d3-116">Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="465d3-116">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="465d3-117">Instale o software do servidor do MBAM e configure os recursos desejados.</span><span class="sxs-lookup"><span data-stu-id="465d3-117">Install the MBAM Server software, and then configure the features you want.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="465d3-118">Tarefa</span><span class="sxs-lookup"><span data-stu-id="465d3-118">Task</span></span></th>
   <th align="left"><span data-ttu-id="465d3-119">Onde obter instruções</span><span class="sxs-lookup"><span data-stu-id="465d3-119">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="465d3-120">Instale o software do servidor MBAM em cada servidor no qual você deseja configurar um recurso do servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="465d3-120">Install the MBAM Server software on each server where you want to configure an MBAM Server feature.</span></span></p></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="465d3-121">Instalando o software de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="465d3-121">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="465d3-122">Configurar o banco de dados de conformidade e auditoria e o banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="465d3-122">Configure the Compliance and Audit Database and the Recovery Database.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="465d3-123">Como configurar os bancos de dados do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="465d3-123">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="465d3-124">Configurar o recurso relatórios.</span><span class="sxs-lookup"><span data-stu-id="465d3-124">Configure the Reports feature.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="465d3-125">Como configurar os relatórios do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="465d3-125">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="465d3-126">Configurar os aplicativos Web.</span><span class="sxs-lookup"><span data-stu-id="465d3-126">Configure the web applications.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="465d3-127">Como configurar os aplicativos Web do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="465d3-127">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="465d3-128">Em um computador cliente, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="465d3-128">On a client computer, do the following:</span></span>

   1.  <span data-ttu-id="465d3-129">Instale o cliente MBAM em um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="465d3-129">Install the MBAM Client on a client computer.</span></span>

   2.  <span data-ttu-id="465d3-130">Aplique os objetos de política de grupo do MBAM (GPOs) ao computador.</span><span class="sxs-lookup"><span data-stu-id="465d3-130">Apply the MBAM Group Policy Objects (GPOs) to the computer.</span></span>

   3.  <span data-ttu-id="465d3-131">Defina as seguintes chaves do registro para forçar o cliente MBAM a despertar mais rápido e em intervalos regulares:</span><span class="sxs-lookup"><span data-stu-id="465d3-131">Set the following registry keys to force the MBAM Client to wake up faster and at regular intervals:</span></span>

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **<span data-ttu-id="465d3-132">Observação</span><span class="sxs-lookup"><span data-stu-id="465d3-132">Note</span></span>**  
       <span data-ttu-id="465d3-133">Como essas chaves ativam o cliente MBAM a cada minuto, recomendamos que você use essas configurações da chave do registro somente em um ambiente de teste.</span><span class="sxs-lookup"><span data-stu-id="465d3-133">Because these keys wake up the MBAM Client every minute, we recommend that you use these registry key settings only in a test environment.</span></span>



   4.  <span data-ttu-id="465d3-134">Reinicie o **serviço de cliente de gerenciamento BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="465d3-134">Restart the **BitLocker Management Client Service**.</span></span>

## <span data-ttu-id="465d3-135">Avaliando o MBAM 2,5 usando a topologia de integração do Configuration Manager do System Center 2012</span><span class="sxs-lookup"><span data-stu-id="465d3-135">Evaluating MBAM 2.5 by using the System Center 2012 Configuration Manager Integration topology</span></span>


<span data-ttu-id="465d3-136">Para avaliar o MBAM usando a topologia de integração do Configuration Manager, use as informações nas tabelas a seguir para instalar o software do servidor do MBAM e configure os recursos do servidor MBAM em seu ambiente de teste.</span><span class="sxs-lookup"><span data-stu-id="465d3-136">To evaluate MBAM by using the Configuration Manager Integration topology, use the information in the following tables to install the MBAM Server software, and then configure the MBAM Server features in your test environment.</span></span> <span data-ttu-id="465d3-137">Depois de instalar o cliente MBAM em um computador cliente, você executará etapas adicionais para forçar o cliente MBAM a reportar o status do computador para o MBAM mais rápido.</span><span class="sxs-lookup"><span data-stu-id="465d3-137">After installing the MBAM Client on a client computer, you will complete additional steps to force the MBAM Client to report the computer’s status to MBAM more quickly.</span></span>

**<span data-ttu-id="465d3-138">Para avaliar o MBAM 2,5 usando a topologia de integração do Configuration Manager do System Center 2012</span><span class="sxs-lookup"><span data-stu-id="465d3-138">To evaluate MBAM 2.5 by using the System Center 2012 Configuration Manager Integration topology</span></span>**

1. <span data-ttu-id="465d3-139">Antes de instalar o MBAM, confira o software de pré-requisito e a configuração com suporte.</span><span class="sxs-lookup"><span data-stu-id="465d3-139">Before installing MBAM, review the prerequisite software and supported configuration.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="465d3-140">Tarefa</span><span class="sxs-lookup"><span data-stu-id="465d3-140">Task</span></span></th>
   <th align="left"><span data-ttu-id="465d3-141">Onde obter instruções</span><span class="sxs-lookup"><span data-stu-id="465d3-141">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="465d3-142">Verifique se você instalou todo o software de pré-requisito.</span><span class="sxs-lookup"><span data-stu-id="465d3-142">Ensure that you have installed all of the prerequisite software.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="465d3-143">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="465d3-143">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="465d3-144">Pré-requisitos do servidor MBAM 2.5 que se aplicam somente à topologia de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="465d3-144">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="465d3-145">Verifique o hardware, a RAM e outras especificações necessárias.</span><span class="sxs-lookup"><span data-stu-id="465d3-145">Check the required hardware, RAM, and other specifications.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="465d3-146">Configurações com suporte no MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="465d3-146">MBAM 2.5 Supported Configurations</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="465d3-147">Examine os pré-requisitos para usar o Windows PowerShell se você planeja usar os cmdlets para configurar o MBAM.</span><span class="sxs-lookup"><span data-stu-id="465d3-147">Review the prerequisites for using Windows PowerShell if you plan to use the cmdlets to configure MBAM.</span></span></p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="465d3-148">Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="465d3-148">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="465d3-149">Criar ou editar os arquivos. mof.</span><span class="sxs-lookup"><span data-stu-id="465d3-149">Create or edit the .mof files.</span></span></p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)"><span data-ttu-id="465d3-150">Edite o arquivo Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="465d3-150">Edit the Configuration.mof File</span></span></a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)"><span data-ttu-id="465d3-151">Criar ou editar o arquivo Sms_def.mof</span><span class="sxs-lookup"><span data-stu-id="465d3-151">Create or Edit the Sms_def.mof File</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="465d3-152">Instale o software do servidor do MBAM e configure os recursos desejados.</span><span class="sxs-lookup"><span data-stu-id="465d3-152">Install the MBAM Server software, and then configure the features you want.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="465d3-153">Tarefa</span><span class="sxs-lookup"><span data-stu-id="465d3-153">Task</span></span></th>
   <th align="left"><span data-ttu-id="465d3-154">Onde obter instruções</span><span class="sxs-lookup"><span data-stu-id="465d3-154">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="465d3-155">Instale o software do servidor MBAM em cada servidor no qual você deseja configurar um recurso do servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="465d3-155">Install the MBAM Server software on each server where you want to configure an MBAM Server feature.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="465d3-156">Observação</span><span class="sxs-lookup"><span data-stu-id="465d3-156">Note</span></span></strong><br/><p><span data-ttu-id="465d3-157">Você pode instalar os bancos de dados em um computador remoto do SQL Server usando o Windows PowerShell ou um pacote de aplicativo da camada de dados (DAC) exportado.</span><span class="sxs-lookup"><span data-stu-id="465d3-157">You can install the databases to a remote SQL Server computer by using Windows PowerShell or an exported data-tier application (DAC) package.</span></span> <span data-ttu-id="465d3-158">Para obter mais informações sobre pacotes DAC, consulte <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> aplicativos da camada de dados </a> .</span><span class="sxs-lookup"><span data-stu-id="465d3-158">For more information about DAC packages, see <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)">Data-tier Applications</a>.</span></span></p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="465d3-159">Instalando o software de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="465d3-159">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="465d3-160">Configurar o banco de dados de conformidade e auditoria e o banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="465d3-160">Configure the Compliance and Audit Database and the Recovery Database.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="465d3-161">Como configurar os bancos de dados do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="465d3-161">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="465d3-162">Configurar o recurso relatórios.</span><span class="sxs-lookup"><span data-stu-id="465d3-162">Configure the Reports feature.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="465d3-163">Como configurar os relatórios do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="465d3-163">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="465d3-164">Configurar os aplicativos Web.</span><span class="sxs-lookup"><span data-stu-id="465d3-164">Configure the web applications.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="465d3-165">Como configurar os aplicativos Web do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="465d3-165">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="465d3-166">Configurar o System Center Configuration Manager para instalar os objetos do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="465d3-166">Configure the System Center Configuration Manager to install the Configuration Manager objects.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)"><span data-ttu-id="465d3-167">Como configurar a integração do System Center Configuration Manager do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="465d3-167">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="465d3-168">Em um computador cliente, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="465d3-168">On a client computer, do the following:</span></span>

   1.  <span data-ttu-id="465d3-169">Instale o cliente do MBAM e o cliente do Configuration Manager em um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="465d3-169">Install the MBAM Client and the Configuration Manager Client on a client computer.</span></span>

   2.  <span data-ttu-id="465d3-170">Aplicar os objetos de política de grupo do MBAM ao computador.</span><span class="sxs-lookup"><span data-stu-id="465d3-170">Apply the MBAM Group Policy Objects to the computer.</span></span>

   3.  <span data-ttu-id="465d3-171">Defina as seguintes chaves do registro para forçar o cliente MBAM a despertar mais rápido e em intervalos regulares:</span><span class="sxs-lookup"><span data-stu-id="465d3-171">Set the following registry keys to force the MBAM Client to wake up faster and at regular intervals:</span></span>

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **<span data-ttu-id="465d3-172">Observação</span><span class="sxs-lookup"><span data-stu-id="465d3-172">Note</span></span>**  
       <span data-ttu-id="465d3-173">Como essas chaves ativam o cliente MBAM a cada minuto, recomendamos que você use essas configurações da chave do registro somente em um ambiente de teste.</span><span class="sxs-lookup"><span data-stu-id="465d3-173">Because these keys wake up the MBAM Client every minute, we recommend that you use these registry key settings only in a test environment.</span></span>



   4.  <span data-ttu-id="465d3-174">Reinicie o **serviço de cliente de gerenciamento BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="465d3-174">Restart the **BitLocker Management Client Service**.</span></span>

   5.  <span data-ttu-id="465d3-175">No painel de controle, abra o **Gerenciador de configurações**e, em seguida, clique na guia **ações** .</span><span class="sxs-lookup"><span data-stu-id="465d3-175">In Control Panel, open **Configuration Manager**, and then click the **Actions** tab.</span></span>

   6.  <span data-ttu-id="465d3-176">Selecione **ciclo de inventário de hardware**e clique em **executar agora**.</span><span class="sxs-lookup"><span data-stu-id="465d3-176">Select **Hardware Inventory Cycle**, and then click **Run Now**.</span></span> <span data-ttu-id="465d3-177">Esta etapa executa o inventário de hardware usando as novas classes importadas para seus arquivos. mof e, em seguida, envia os dados ao servidor do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="465d3-177">This step runs the hardware inventory by using the new classes that you imported to your .mof files, and then sends the data to the Configuration Manager server.</span></span>

   7.  <span data-ttu-id="465d3-178">Selecione **recuperação de política de máquina & ciclo de avaliação**e, em seguida, clique em **executar agora** para aplicar os objetos de política de grupo relevantes para esse computador cliente.</span><span class="sxs-lookup"><span data-stu-id="465d3-178">Select **Machine Policy Retrieval & Evaluation Cycle**, and then click **Run Now** to apply the Group Policy Objects that are relevant to that client computer.</span></span>



4. <span data-ttu-id="465d3-179">No console do Configuration Manager, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="465d3-179">In the Configuration Manager console, do the following:</span></span>

   1.  <span data-ttu-id="465d3-180">No painel de navegação, clique com o botão direito do mouse em **computadores com suporte do MBAM**, clique em **Atualizar Associação**e em **Sim** para forçar o computador cliente a denunciar sua associação imediatamente.</span><span class="sxs-lookup"><span data-stu-id="465d3-180">In the navigation pane, right-click **MBAM Supported Computers**, click **Update Membership**, and then click **Yes** to force the client computer to report its membership immediately.</span></span>

   2.  <span data-ttu-id="465d3-181">No painel de navegação, clique em **computadores com suporte MBAM** para verificar se o computador cliente aparece na coleção.</span><span class="sxs-lookup"><span data-stu-id="465d3-181">In the navigation pane, click **MBAM Supported Computers** to verify that the client computer appears in the collection.</span></span>

5. <span data-ttu-id="465d3-182">No computador cliente, no painel de controle, abra novamente o **Gerenciador de configuração** e faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="465d3-182">On the client computer, in Control Panel, reopen **Configuration Manager** again, and do the following:</span></span>

   1.  <span data-ttu-id="465d3-183">Clique na guia **ações** e, em seguida, execute novamente a **recuperação da política do computador & ciclo de avaliação**.</span><span class="sxs-lookup"><span data-stu-id="465d3-183">Click the **Actions** tab, and then rerun **Machine Policy Retrieval & Evaluation Cycle**.</span></span>

   2.  <span data-ttu-id="465d3-184">Clique na guia **configurações** , selecione a linha de base do BitLocker e, em seguida, clique em **avaliar**.</span><span class="sxs-lookup"><span data-stu-id="465d3-184">Click the **Configurations** tab, select the BitLocker baseline, and then click **Evaluate**.</span></span>

6. <span data-ttu-id="465d3-185">No console do Configuration Manager, verifique se o computador cliente é exibido no relatório de conformidade para empresas: da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="465d3-185">In the Configuration Manager console, verify that the client computer appears on the Enterprise Compliance Report: as follows:</span></span>

   1.  <span data-ttu-id="465d3-186">No painel de navegação, selecione o espaço de trabalho **monitoramento** .</span><span class="sxs-lookup"><span data-stu-id="465d3-186">In the navigation pane, select the **Monitoring** workspace.</span></span>

   2.  <span data-ttu-id="465d3-187">Na árvore de console, expanda relatórios de relatório de **visão geral** &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="465d3-187">In the console tree, expand **Overview** &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.</span></span>

   3.  <span data-ttu-id="465d3-188">Selecione a pasta que representa o idioma no qual você deseja exibir relatórios e, em seguida, selecione o relatório no painel de resultados.</span><span class="sxs-lookup"><span data-stu-id="465d3-188">Select the folder that represents the language in which you want to view reports, and then select the report in the results pane.</span></span>

## <span data-ttu-id="465d3-189">Avaliando o MBAM 2,5 usando a topologia de integração do System Center Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="465d3-189">Evaluating MBAM 2.5 by using the System Center Configuration Manager 2007 Integration topology</span></span>


<span data-ttu-id="465d3-190">Para avaliar o MBAM usando a topologia de integração do Configuration Manager, siga as mesmas etapas para instalar e configurar o MBAM em seu ambiente de teste conforme você usa em um ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="465d3-190">To evaluate MBAM by using the Configuration Manager Integration topology, follow the same steps to install and configure MBAM in your test environment as you use in a production environment.</span></span> <span data-ttu-id="465d3-191">Depois de instalar o cliente MBAM em um computador cliente, conclua as etapas adicionais neste tópico para permitir que o cliente do MBAM comece a reportar o status do computador para o MBAM mais rápido.</span><span class="sxs-lookup"><span data-stu-id="465d3-191">After installing the MBAM Client on a client computer, complete the additional steps in this topic to enable the MBAM Client to start reporting the computer’s status to MBAM more quickly.</span></span>

**<span data-ttu-id="465d3-192">Para avaliar o MBAM usando a topologia de integração do Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="465d3-192">To evaluate MBAM by using the Configuration Manager 2007 Integration topology</span></span>**

1. <span data-ttu-id="465d3-193">Antes de instalar o MBAM, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="465d3-193">Before you install MBAM, do the following:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="465d3-194">Tarefa</span><span class="sxs-lookup"><span data-stu-id="465d3-194">Task</span></span></th>
   <th align="left"><span data-ttu-id="465d3-195">Onde obter instruções</span><span class="sxs-lookup"><span data-stu-id="465d3-195">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="465d3-196">Verifique se você instalou todo o software de pré-requisito.</span><span class="sxs-lookup"><span data-stu-id="465d3-196">Ensure that you have installed all of the prerequisite software.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="465d3-197">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="465d3-197">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="465d3-198">Pré-requisitos do servidor MBAM 2.5 que se aplicam somente à topologia de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="465d3-198">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="465d3-199">Verifique o hardware, a RAM e outras especificações necessárias.</span><span class="sxs-lookup"><span data-stu-id="465d3-199">Check the required hardware, RAM, and other specifications.</span></span></p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="465d3-200">Configurações com suporte no MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="465d3-200">MBAM 2.5 Supported Configurations</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="465d3-201">Criar ou editar os arquivos. mof.</span><span class="sxs-lookup"><span data-stu-id="465d3-201">Create or edit the .mof files.</span></span></p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)"><span data-ttu-id="465d3-202">Edite o arquivo Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="465d3-202">Edit the Configuration.mof File</span></span></a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)"><span data-ttu-id="465d3-203">Criar ou editar o arquivo Sms_def.mof</span><span class="sxs-lookup"><span data-stu-id="465d3-203">Create or Edit the Sms_def.mof File</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="465d3-204">Instale o software do servidor do MBAM e configure os recursos desejados.</span><span class="sxs-lookup"><span data-stu-id="465d3-204">Install the MBAM Server software, and then configure the features you want.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="465d3-205">Tarefa</span><span class="sxs-lookup"><span data-stu-id="465d3-205">Task</span></span></th>
   <th align="left"><span data-ttu-id="465d3-206">Onde obter instruções</span><span class="sxs-lookup"><span data-stu-id="465d3-206">Where to get instructions</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="465d3-207">Instale o software do servidor MBAM em cada servidor no qual você deseja configurar um recurso do servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="465d3-207">Install the MBAM Server software on each server where you want to configure an MBAM Server feature.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="465d3-208">Observação</span><span class="sxs-lookup"><span data-stu-id="465d3-208">Note</span></span></strong><br/><p><span data-ttu-id="465d3-209">Você pode instalar os bancos de dados em um computador remoto do SQL Server usando o Windows PowerShell ou um pacote de aplicativo da camada de dados (DAC) exportado.</span><span class="sxs-lookup"><span data-stu-id="465d3-209">You can install the databases to a remote SQL Server computer by using Windows PowerShell or an exported data-tier application (DAC) package.</span></span> <span data-ttu-id="465d3-210">Para obter mais informações sobre pacotes DAC, consulte <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> aplicativos da camada de dados </a> .</span><span class="sxs-lookup"><span data-stu-id="465d3-210">For more information about DAC packages, see <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)">Data-tier Applications</a>.</span></span></p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="465d3-211">Instalando o software de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="465d3-211">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="465d3-212">Configurar o banco de dados de conformidade e auditoria e o banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="465d3-212">Configure the Compliance and Audit Database and the Recovery Database.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="465d3-213">Como configurar os bancos de dados do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="465d3-213">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="465d3-214">Configurar o recurso relatórios.</span><span class="sxs-lookup"><span data-stu-id="465d3-214">Configure the Reports feature.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="465d3-215">Como configurar os relatórios do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="465d3-215">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="465d3-216">Configurar os aplicativos Web.</span><span class="sxs-lookup"><span data-stu-id="465d3-216">Configure the web applications.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="465d3-217">Como configurar os aplicativos Web do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="465d3-217">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="465d3-218">Configurar o System Center Configuration Manager para instalar os objetos do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="465d3-218">Configure the System Center Configuration Manager to install the Configuration Manager objects.</span></span></p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)"><span data-ttu-id="465d3-219">Como configurar a integração do System Center Configuration Manager do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="465d3-219">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="465d3-220">Em um computador cliente, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="465d3-220">On a client computer, do the following:</span></span>

   1.  <span data-ttu-id="465d3-221">Instale o cliente MBAM em um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="465d3-221">Install the MBAM Client on a client computer.</span></span>

   2.  <span data-ttu-id="465d3-222">Aplicar os objetos de política de grupo do MBAM ao computador.</span><span class="sxs-lookup"><span data-stu-id="465d3-222">Apply the MBAM Group Policy Objects to the computer.</span></span>

   3.  <span data-ttu-id="465d3-223">Defina as seguintes chaves do registro para forçar o cliente MBAM a despertar mais rapidamente e em intervalos mais rápidos:</span><span class="sxs-lookup"><span data-stu-id="465d3-223">Set the following registry keys to force the MBAM Client to wake up more quickly and at faster intervals:</span></span>

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **<span data-ttu-id="465d3-224">Observação</span><span class="sxs-lookup"><span data-stu-id="465d3-224">Note</span></span>**  
       <span data-ttu-id="465d3-225">Como essas chaves ativam o cliente MBAM a cada minuto, recomendamos que você use essas configurações da chave do registro somente em um ambiente de avaliação.</span><span class="sxs-lookup"><span data-stu-id="465d3-225">Because these keys wake up the MBAM Client every minute, we recommend that you use these registry key settings only in an evaluation environment.</span></span>



   4.  <span data-ttu-id="465d3-226">Reinicie o **serviço de cliente de gerenciamento BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="465d3-226">Restart the **BitLocker Management Client Service**.</span></span>

   5.  <span data-ttu-id="465d3-227">No painel de controle, abra o **Gerenciador de configurações**e, em seguida, clique na guia **ações** .</span><span class="sxs-lookup"><span data-stu-id="465d3-227">In Control Panel, open **Configuration Manager**, and then click the **Actions** tab.</span></span>

   6.  <span data-ttu-id="465d3-228">Selecione **recuperação de política de máquina & ciclo de avaliação**e, em seguida, clique em **executar agora** para aplicar os objetos de política de grupo relevantes para esse computador cliente.</span><span class="sxs-lookup"><span data-stu-id="465d3-228">Select **Machine Policy Retrieval & Evaluation Cycle**, and then click **Run Now** to apply the Group Policy Objects that are relevant to that client computer.</span></span>

   7.  <span data-ttu-id="465d3-229">Selecione **ciclo de inventário de hardware**e clique em **executar agora**.</span><span class="sxs-lookup"><span data-stu-id="465d3-229">Select **Hardware Inventory Cycle**, and then click **Run Now**.</span></span> <span data-ttu-id="465d3-230">Esta etapa executa o inventário de hardware usando as novas classes que você importou para seus arquivos. mof e, em seguida, envia os dados ao servidor do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="465d3-230">This step runs the hardware inventory by using the new classes that you imported to your .mof files and then sends the data to the Configuration Manager server.</span></span>

4. <span data-ttu-id="465d3-231">No console do Configuration Manager, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="465d3-231">In the Configuration Manager console, do the following:</span></span>

   1.  <span data-ttu-id="465d3-232">No painel de navegação, clique com o botão direito do mouse em **computadores com suporte do MBAM**, clique em **Atualizar Associação**e em **Sim** para forçar o computador cliente a denunciar sua associação imediatamente.</span><span class="sxs-lookup"><span data-stu-id="465d3-232">In the navigation pane, right-click **MBAM Supported Computers**, click **Update Membership**, and then click **Yes** to force the client computer to report its membership immediately.</span></span>

   2.  <span data-ttu-id="465d3-233">No painel de navegação, clique em **computadores com suporte MBAM** para verificar se o computador cliente aparece na coleção.</span><span class="sxs-lookup"><span data-stu-id="465d3-233">In the navigation pane, click **MBAM Supported Computers** to verify that the client computer appears in the collection.</span></span>

5. <span data-ttu-id="465d3-234">No computador cliente, no painel de controle, abra novamente o **Gerenciador de configuração** e faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="465d3-234">On the client computer, in Control Panel, reopen **Configuration Manager** again, and do the following:</span></span>

   1.  <span data-ttu-id="465d3-235">Clique na guia **ações** e, em seguida, execute novamente a **recuperação da política do computador & ciclo de avaliação**.</span><span class="sxs-lookup"><span data-stu-id="465d3-235">Click the **Actions** tab, and then rerun **Machine Policy Retrieval & Evaluation Cycle**.</span></span>

   2.  <span data-ttu-id="465d3-236">Clique na guia **configurações** , selecione a linha de base do BitLocker e clique em **avaliar**.</span><span class="sxs-lookup"><span data-stu-id="465d3-236">Click the **Configurations** tab, select the BitLocker baseline, and click **Evaluate**.</span></span>

6. <span data-ttu-id="465d3-237">No console do Configuration Manager, verifique se o computador cliente é exibido no relatório de conformidade empresarial, da seguinte maneira</span><span class="sxs-lookup"><span data-stu-id="465d3-237">In the Configuration Manager console, verify that the client computer appears on the Enterprise Compliance Report, as follows</span></span>

   1.  <span data-ttu-id="465d3-238">No painel de navegação, expanda **Gerenciamento de computador** &gt; **relatório** &gt; do **Reporting Services** &gt; \*\* &lt; Server Name &gt; MBAM\*\*.</span><span class="sxs-lookup"><span data-stu-id="465d3-238">In the navigation pane, expand **Computer Management** &gt; **Reporting** &gt; **Reporting Services** &gt; **&lt;server name&gt;MBAM**.</span></span>

   2.  <span data-ttu-id="465d3-239">No nó **MBAM** , selecione a pasta que representa o idioma no qual você deseja exibir relatórios e, em seguida, selecione o relatório no painel de resultados.</span><span class="sxs-lookup"><span data-stu-id="465d3-239">Within the **MBAM** node, select the folder that represents the language in which you want to view reports, and then select the report from the results pane.</span></span>


## <span data-ttu-id="465d3-240">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="465d3-240">Related topics</span></span>


[<span data-ttu-id="465d3-241">Introdução ao MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="465d3-241">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)


## <span data-ttu-id="465d3-242">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="465d3-242">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="465d3-243">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="465d3-243">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="465d3-244">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="465d3-244">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>





