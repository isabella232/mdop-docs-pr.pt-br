---
title: Pré-requisitos para o recurso de integração do Configuration Manager
description: Pré-requisitos para o recurso de integração do Configuration Manager
author: dansimp
ms.assetid: b318cbd3-b009-44b8-991b-f7364c1cae88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af7abd50f6218810dd6718f091512b48fee32652
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799587"
---
# <span data-ttu-id="81875-103">Pré-requisitos para o recurso de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="81875-103">Prerequisites for the Configuration Manager Integration Feature</span></span>


<span data-ttu-id="81875-104">Se você implantar o MBAM com a topologia de integração do System Center Configuration Manager, recomendamos uma arquitetura de três servidores, conforme descrito em [arquitetura de alto nível do MBAM 2,5 com a topologia de integração do Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="81875-104">If you deploy MBAM with the System Center Configuration Manager Integration topology, we recommend a three-server architecture, as described in [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span></span> <span data-ttu-id="81875-105">Essa arquitetura pode dar suporte a 500.000 computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="81875-105">This architecture can support 500,000 client computers.</span></span>

**<span data-ttu-id="81875-106">Importante</span><span class="sxs-lookup"><span data-stu-id="81875-106">Important</span></span>**  
<span data-ttu-id="81875-107">Não há suporte para o Windows to go para a instalação de topologia de integração do Configuration Manager quando você está usando o Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="81875-107">Windows To Go is not supported for the Configuration Manager Integration topology installation when you are using Configuration Manager 2007.</span></span>



## <span data-ttu-id="81875-108">Pré-requisitos gerais do recurso de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="81875-108">General prerequisites for the Configuration Manager Integration feature</span></span>


<span data-ttu-id="81875-109">Quando você instala o MBAM com o Configuration Manager, os seguintes pré-requisitos adicionais são necessários, além dos pré-requisitos para a topologia autônoma.</span><span class="sxs-lookup"><span data-stu-id="81875-109">When you install MBAM with Configuration Manager, the following additional prerequisites are required in addition to the prerequisites for the Stand-alone topology.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="81875-110">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="81875-110">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="81875-111">Informações adicionais</span><span class="sxs-lookup"><span data-stu-id="81875-111">Additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81875-112">O servidor do Configuration Manager é um site primário no sistema do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="81875-112">The Configuration Manager Server is a primary site in the Configuration Manager system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="81875-113">N/A</span><span class="sxs-lookup"><span data-stu-id="81875-113">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81875-114">O agente cliente do inventário de hardware está no servidor do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="81875-114">The Hardware Inventory Client Agent is on the Configuration Manager Server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="81875-115">Para o System Center 2012 Configuration Manager, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> como configurar o inventário de hardware no Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="81875-115">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)">How to Configure Hardware Inventory in Configuration Manager</a>.</span></span></p>
<p><span data-ttu-id="81875-116">Para o Configuration Manager 2007, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> como configurar o inventário de hardware para um site </a> .</span><span class="sxs-lookup"><span data-stu-id="81875-116">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)">How to Configure Hardware Inventory for a Site</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81875-117">Um dos seguintes itens está habilitado, dependendo da versão do Configuration Manager que você está usando:</span><span class="sxs-lookup"><span data-stu-id="81875-117">One of the following is enabled, depending on the version of Configuration Manager that you are using:</span></span></p>
<ul>
<li><p><span data-ttu-id="81875-118">Configurações de conformidade-(System Center 2012 Configuration Manager)</span><span class="sxs-lookup"><span data-stu-id="81875-118">Compliance Settings - (System Center 2012 Configuration Manager)</span></span></p></li>
<li><p><span data-ttu-id="81875-119">Agente cliente do gerenciamento de configuração desejado (DCM) – (Configuration Manager 2007)</span><span class="sxs-lookup"><span data-stu-id="81875-119">Desired Configuration Management (DCM) Client Agent – (Configuration Manager 2007)</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="81875-120">Para o System Center 2012 Configuration Manager, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> definindo configurações de conformidade no Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="81875-120">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)">Configuring Compliance Settings in Configuration Manager</a>.</span></span></p>
<p><span data-ttu-id="81875-121">Para o Configuration Manager 2007, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> as propriedades do agente cliente de gerenciamento de configuração desejadas </a> .</span><span class="sxs-lookup"><span data-stu-id="81875-121">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)">Desired Configuration Management Client Agent Properties</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81875-122">Um ponto do Reporting Services é definido no Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="81875-122">A reporting services point is defined in Configuration Manager.</span></span> <span data-ttu-id="81875-123">Obrigatório para SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="81875-123">Required for SQL Server Reporting Services (SSRS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="81875-124">Para o System Center 2012 Configuration Manager, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> pré-requisitos para relatórios no Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="81875-124">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)">Prerequisites for Reporting in Configuration Manager</a>.</span></span></p>
<p><span data-ttu-id="81875-125">Para o Configuration Manager 2007, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> como criar um ponto do Reporting Services para SQL Reporting Services </a> .</span><span class="sxs-lookup"><span data-stu-id="81875-125">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)">How to Create a Reporting Services Point for SQL Reporting Services</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81875-126">O Configuration Manager 2007 requer o Microsoft .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="81875-126">Configuration Manager 2007 requires Microsoft .NET Framework 2.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="81875-127">O agente do cliente DCM (gerenciamento de configuração desejado) no Configuration Manager 2007 requer que o .NET Framework 2,0 para denunciar a conformidade.</span><span class="sxs-lookup"><span data-stu-id="81875-127">The Desired Configuration Management (DCM) Client Agent in Configuration Manager 2007 requires .NET Framework 2.0 to report compliance.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="81875-128">Observação</span><span class="sxs-lookup"><span data-stu-id="81875-128">Note</span></span></strong><br/><p><span data-ttu-id="81875-129">A instalação do .NET Framework 3,5 instala automaticamente o .NET Framework 2,0.</span><span class="sxs-lookup"><span data-stu-id="81875-129">Installing .NET Framework 3.5 automatically installs .NET Framework 2.0.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="81875-130">Permissões necessárias para instalar o MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="81875-130">Required permissions to install MBAM with Configuration Manager</span></span>


<span data-ttu-id="81875-131">Para instalar o MBAM com o Configuration Manager, você deve ter um usuário administrativo no Configuration Manager que tenha um direito de acesso com as permissões mínimas listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="81875-131">To install MBAM with Configuration Manager, you must have an administrative user in Configuration Manager who has a security role with the minimum permissions listed in the following table.</span></span> <span data-ttu-id="81875-132">A tabela também mostra os direitos que você deve ter, além dos direitos de administrador do computador básico, para instalar o MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="81875-132">The table also shows the rights that you must have, beyond basic computer administrator rights, to install the MBAM Server.</span></span>

**<span data-ttu-id="81875-133">As permissões na tabela a seguir se aplicam a ambas as versões do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="81875-133">The permissions in the following table apply to both versions of Configuration Manager.</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="81875-134">Permissões</span><span class="sxs-lookup"><span data-stu-id="81875-134">Permissions</span></span></th>
<th align="left"><span data-ttu-id="81875-135">Recurso do servidor MBAM</span><span class="sxs-lookup"><span data-stu-id="81875-135">MBAM Server feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81875-136">Funções do servidor de logon da instância do SQL Server:-dbcreator-processadmin</span><span class="sxs-lookup"><span data-stu-id="81875-136">SQL Server instance login server roles: - dbcreator- processadmin</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="81875-137">Banco de dados de recuperação-banco de dados de auditoria</span><span class="sxs-lookup"><span data-stu-id="81875-137">Recovery Database- Audit Database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81875-138">Direitos de instância do SSRS:-criar pastas – publicar relatórios</span><span class="sxs-lookup"><span data-stu-id="81875-138">SSRS instance rights: - Create Folders- Publish Reports</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="81875-139">Integração do System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="81875-139">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="81875-140">Systems Center 2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="81875-140">System Center 2012 Configuration Manager</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="81875-141">Permissões</span><span class="sxs-lookup"><span data-stu-id="81875-141">Permissions</span></span></th>
<th align="left"><span data-ttu-id="81875-142">Recurso do servidor do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="81875-142">Configuration Manager Server feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81875-143">Direitos de site do Configuration Manager:-ler</span><span class="sxs-lookup"><span data-stu-id="81875-143">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="81875-144">Integração do System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="81875-144">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81875-145">Direitos de coleção do Configuration Manager:-criar-excluir-ler-modificar-implantar itens de configuração</span><span class="sxs-lookup"><span data-stu-id="81875-145">Configuration Manager collection rights: - Create- Delete- Read- Modify- Deploy Configuration Items</span></span></p></td>
<td align="left"><p><span data-ttu-id="81875-146">Integração do System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="81875-146">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81875-147">Direitos de item de configuração do Configuration Manager:-Create-Delete-Read</span><span class="sxs-lookup"><span data-stu-id="81875-147">Configuration Manager configuration item rights: - Create- Delete- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="81875-148">Integração do System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="81875-148">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="81875-149">Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="81875-149">Configuration Manager 2007</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="81875-150">Permissões</span><span class="sxs-lookup"><span data-stu-id="81875-150">Permissions</span></span></th>
<th align="left"><span data-ttu-id="81875-151">Recurso do servidor do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="81875-151">Configuration Manager Server feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81875-152">Direitos de site do Configuration Manager:-ler</span><span class="sxs-lookup"><span data-stu-id="81875-152">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="81875-153">Integração do System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="81875-153">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="81875-154">Direitos de coleção do Configuration Manager:-Create-Delete-Read-ReadResource</span><span class="sxs-lookup"><span data-stu-id="81875-154">Configuration Manager collection rights: - Create- Delete- Read- ReadResource</span></span></p></td>
<td align="left"><p><span data-ttu-id="81875-155">Integração do System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="81875-155">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="81875-156">Direitos de item de configuração do Configuration Manager:-criar-excluir-ler-distribuir</span><span class="sxs-lookup"><span data-stu-id="81875-156">Configuration Manager configuration item rights: - Create- Delete- Read- Distribute</span></span></p></td>
<td align="left"><p><span data-ttu-id="81875-157">Integração do System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="81875-157">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="81875-158">Alterações necessárias para os arquivos. mof</span><span class="sxs-lookup"><span data-stu-id="81875-158">Required changes for the .mof files</span></span>


<span data-ttu-id="81875-159">Para permitir que os computadores cliente relatem detalhes de conformidade do BitLocker por meio dos relatórios do Gerenciador de configuração do MBAM, você precisa editar o arquivo. mof de configuração e o arquivo SMS \ _def. MOF para o System Center 2012 Configuration Manager e o Microsoft System Center Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="81875-159">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the Configuration.mof file and Sms\_def.mof file for System Center 2012 Configuration Manager and Microsoft System Center Configuration Manager 2007.</span></span> <span data-ttu-id="81875-160">Para obter instruções, consulte [pré-requisitos do servidor do MBAM 2,5 que se aplicam apenas à topologia de integração do Configuration Manager](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="81875-160">For instructions, see [MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span></span>



## <span data-ttu-id="81875-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="81875-161">Related topics</span></span>


[<span data-ttu-id="81875-162">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="81875-162">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span>](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

[<span data-ttu-id="81875-163">Pré-requisitos do servidor MBAM 2.5 que se aplicam somente à topologia de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="81875-163">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span>](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)



## <span data-ttu-id="81875-164">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="81875-164">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="81875-165">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="81875-165">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="81875-166">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="81875-166">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





