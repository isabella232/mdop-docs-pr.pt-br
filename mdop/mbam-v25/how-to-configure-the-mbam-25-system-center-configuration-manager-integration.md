---
title: Como configurar a integração do System Center Configuration Manager do MBAM 2.5
description: Como configurar a integração do System Center Configuration Manager do MBAM 2.5
author: dansimp
ms.assetid: 2b8a4c13-1dad-41e8-89ac-6889c5f7e051
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c6fb0a0b06399baf1dc6493a40d17e76a51741f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796001"
---
# <span data-ttu-id="37821-103">Como configurar a integração do System Center Configuration Manager do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="37821-103">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span>


<span data-ttu-id="37821-104">Este tópico explica como configurar o Microsoft BitLocker Administration and Monitoring (MBAM) para usar a topologia de integração do System Center Configuration Manager, que integra o MBAM com o Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="37821-104">This topic explains how to configure Microsoft BitLocker Administration and Monitoring (MBAM) to use the System Center Configuration Manager Integration topology, which integrates MBAM with Configuration Manager.</span></span>

<span data-ttu-id="37821-105">As instruções explicam como configurar a integração do Configuration Manager usando:</span><span class="sxs-lookup"><span data-stu-id="37821-105">The instructions explain how to configure Configuration Manager Integration by using:</span></span>

-   <span data-ttu-id="37821-106">Um cmdlet do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="37821-106">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="37821-107">O assistente de configuração do servidor do MBAM</span><span class="sxs-lookup"><span data-stu-id="37821-107">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="37821-108">As instruções se baseiam na arquitetura recomendada na [arquitetura de alto nível do MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="37821-108">The instructions are based on the recommended architecture in [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

**<span data-ttu-id="37821-109">Antes de iniciar a configuração:</span><span class="sxs-lookup"><span data-stu-id="37821-109">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="37821-110">Etapa</span><span class="sxs-lookup"><span data-stu-id="37821-110">Step</span></span></th>
<th align="left"><span data-ttu-id="37821-111">Onde obter instruções</span><span class="sxs-lookup"><span data-stu-id="37821-111">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="37821-112">Examine a arquitetura recomendada para MBAM.</span><span class="sxs-lookup"><span data-stu-id="37821-112">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md" data-raw-source="[High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)"><span data-ttu-id="37821-113">Arquitetura de alto nível do MBAM 2.5 com topologia de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="37821-113">High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="37821-114">Examine as configurações com suporte para MBAM.</span><span class="sxs-lookup"><span data-stu-id="37821-114">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="37821-115">Configurações com suporte no MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="37821-115">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="37821-116">Complete os pré-requisitos obrigatórios em cada servidor.</span><span class="sxs-lookup"><span data-stu-id="37821-116">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="37821-117">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="37821-117">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="37821-118">Pré-requisitos do servidor MBAM 2.5 que se aplicam somente à topologia de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="37821-118">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="37821-119">Instale o software do servidor MBAM em cada servidor em que você irá configurar um recurso do servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="37821-119">Install the MBAM Server software on each server where you will configure an MBAM Server feature.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="37821-120">Observação</span><span class="sxs-lookup"><span data-stu-id="37821-120">Note</span></span></strong><br/><p><span data-ttu-id="37821-121">Para essa topologia, você deve instalar o console do Configuration Manager no computador em que está instalando o software MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="37821-121">For this topology, you must install the Configuration Manager console on the computer where you are installing the MBAM Server software.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="37821-122">Instalando o software de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="37821-122">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="37821-123">Examine os pré-requisitos do Windows PowerShell (aplicável somente se você pretende usar cmdlets do Windows PowerShell para configurar o MBAM).</span><span class="sxs-lookup"><span data-stu-id="37821-123">Review Windows PowerShell prerequisites (applicable only if you are going to use Windows PowerShell cmdlets to configure MBAM).</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="37821-124">Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="37821-124">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="37821-125">Para configurar a integração do Configuration Manager usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="37821-125">To configure Configuration Manager Integration by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="37821-126">Antes de iniciar a configuração, confira [Configurando os recursos do servidor do MBAM 2,5 usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) para revisar os pré-requisitos para usar o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="37821-126">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="37821-127">Use o cmdlet **Enable-MbamCMIntegration** do Windows PowerShell para configurar os relatórios.</span><span class="sxs-lookup"><span data-stu-id="37821-127">Use the **Enable-MbamCMIntegration** Windows PowerShell cmdlet to configure the Reports.</span></span> <span data-ttu-id="37821-128">Para obter informações sobre esse cmdlet, digite **Get-Help Enable-MbamCMIntegration**.</span><span class="sxs-lookup"><span data-stu-id="37821-128">To get information about this cmdlet, type **Get-Help Enable-MbamCMIntegration**.</span></span>

**<span data-ttu-id="37821-129">Para configurar a integração do System Center Configuration Manager usando o assistente</span><span class="sxs-lookup"><span data-stu-id="37821-129">To configure the System Center Configuration Manager Integration by using the wizard</span></span>**

1.  <span data-ttu-id="37821-130">No servidor em que você deseja configurar o recurso de integração do System Center Configuration Manager, inicie o assistente de configuração do MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="37821-130">On the server where you want to configure the System Center Configuration Manager Integration feature, start the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="37821-131">Você pode selecionar **configuração do servidor MBAM** no menu **Iniciar** para abrir o assistente.</span><span class="sxs-lookup"><span data-stu-id="37821-131">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2.  <span data-ttu-id="37821-132">Clique em **Adicionar novos recursos**, selecione **integração com o System Center Configuration Manager**e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="37821-132">Click **Add New Features**, select **System Center Configuration Manager Integration**, and then click **Next**.</span></span>

    <span data-ttu-id="37821-133">O assistente verifica se todos os pré-requisitos para a integração do Configuration Manager foram atendidos.</span><span class="sxs-lookup"><span data-stu-id="37821-133">The wizard checks that all prerequisites for the Configuration Manager Integration have been met.</span></span>

3.  <span data-ttu-id="37821-134">Se a verificação de pré-requisito for bem-sucedida, clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="37821-134">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="37821-135">Caso contrário, resolva todos os pré-requisitos ausentes e clique em **verificar pré-requisitos novamente**.</span><span class="sxs-lookup"><span data-stu-id="37821-135">Otherwise, resolve any missing prerequisites, and then click **Check prerequisites again**.</span></span>

4.  <span data-ttu-id="37821-136">Use as descrições a seguir para inserir os valores de campo no assistente:</span><span class="sxs-lookup"><span data-stu-id="37821-136">Use the following descriptions to enter the field values in the wizard:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="37821-137">Campo</span><span class="sxs-lookup"><span data-stu-id="37821-137">Field</span></span></th>
    <th align="left"><span data-ttu-id="37821-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="37821-138">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="37821-139">Servidor do SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="37821-139">SQL Server Reporting Services server</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="37821-140">FQDN (nome de domínio totalmente qualificado) do servidor com a função de ponto de serviço de relatório.</span><span class="sxs-lookup"><span data-stu-id="37821-140">Fully qualified domain name (FQDN) of the server with the Reporting Service point role.</span></span> <span data-ttu-id="37821-141">Esse é o servidor ao qual os relatórios do Gerenciador de configuração do MBAM são implantados.</span><span class="sxs-lookup"><span data-stu-id="37821-141">This is the server to which the MBAM Configuration Manager Reports are deployed.</span></span></p>
    <p><span data-ttu-id="37821-142">Se você não especificar um servidor, os relatórios do Configuration Manager serão implantados no servidor local.</span><span class="sxs-lookup"><span data-stu-id="37821-142">If you don’t specify a server, the Configuration Manager Reports will be deployed to the local server.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="37821-143">Instância do SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="37821-143">SQL Server Reporting Services instance</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="37821-144">Nome da instância do SQL Server Reporting Services (SSRS) em que os relatórios do Configuration Manager são implantados.</span><span class="sxs-lookup"><span data-stu-id="37821-144">Name of the SQL Server Reporting Services (SSRS) instance where the Configuration Manager Reports are deployed.</span></span></p>
    <p><span data-ttu-id="37821-145">Se você não especificar uma instância, os relatórios do Configuration Manager serão implantados para o nome da instância padrão do SSRS.</span><span class="sxs-lookup"><span data-stu-id="37821-145">If you don’t specify an instance, the Configuration Manager Reports will be deployed to the default SSRS instance name.</span></span> <span data-ttu-id="37821-146">O valor que você inserir será ignorado se o servidor tiver o System Center 2012 Configuration Manager instalado.</span><span class="sxs-lookup"><span data-stu-id="37821-146">The value you enter is ignored if the server has System Center 2012 Configuration Manager installed.</span></span></p></td>
    </tr>
    </tbody>
    </table>



5.  <span data-ttu-id="37821-147">Na página **Resumo** , examine os recursos que serão adicionados.</span><span class="sxs-lookup"><span data-stu-id="37821-147">On the **Summary** page, review the features that will be added.</span></span>

    **<span data-ttu-id="37821-148">Observação</span><span class="sxs-lookup"><span data-stu-id="37821-148">Note</span></span>**  
    <span data-ttu-id="37821-149">Para criar um script do Windows PowerShell das entradas que você acabou de fazer, clique em **Exportar script do PowerShell** e salve o script.</span><span class="sxs-lookup"><span data-stu-id="37821-149">To create a Windows PowerShell script of the entries you just made, click **Export PowerShell Script** and save the script.</span></span>



6.  <span data-ttu-id="37821-150">Clique em **Adicionar** para adicionar o recurso integração com o Gerenciador de configurações ao servidor e, em seguida, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="37821-150">Click **Add** to add the Configuration Manager Integration feature to the server, and then click **Close**.</span></span>



## <span data-ttu-id="37821-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="37821-151">Related topics</span></span>


[<span data-ttu-id="37821-152">Configurando os recursos de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="37821-152">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="37821-153">Validando a configuração de recursos de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="37821-153">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)


## <span data-ttu-id="37821-154">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="37821-154">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="37821-155">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="37821-155">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="37821-156">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="37821-156">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






