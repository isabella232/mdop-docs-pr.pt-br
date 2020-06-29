---
title: Planejando a implantação de servidor do MBAM 2.5
description: Planejando a implantação de servidor do MBAM 2.5
author: dansimp
ms.assetid: 88774c89-31c8-4eb8-a845-a00bbec8c870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2ecb510fab821118ce210577f9ffb83c39be050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799827"
---
# <span data-ttu-id="b60a0-103">Planejando a implantação de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="b60a0-103">Planning for MBAM 2.5 Server Deployment</span></span>


<span data-ttu-id="b60a0-104">Este tópico lista os recursos que você implanta para as topologias autônomas e do Configuration Manager do MBAM e lista a ordem em que você precisa implementá-las.</span><span class="sxs-lookup"><span data-stu-id="b60a0-104">This topic lists the features that you deploy for the MBAM Stand-alone and Configuration Manager topologies and lists the order in which you need to deploy them.</span></span> <span data-ttu-id="b60a0-105">Há uma configuração recomendada para cada topologia.</span><span class="sxs-lookup"><span data-stu-id="b60a0-105">There is a recommended configuration for each topology.</span></span> <span data-ttu-id="b60a0-106">No entanto, você pode configurar bancos de dados e recursos do MBAM Server em configurações diferentes e entre vários servidores, dependendo dos requisitos de escalabilidade.</span><span class="sxs-lookup"><span data-stu-id="b60a0-106">However, you can configure MBAM server databases and features in different configurations and across multiple servers, depending on your scalability requirements.</span></span>

## <span data-ttu-id="b60a0-107">Considerações importantes de planejamento para ambas as topologias</span><span class="sxs-lookup"><span data-stu-id="b60a0-107">Important planning considerations for both topologies</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b60a0-108">Conhecer</span><span class="sxs-lookup"><span data-stu-id="b60a0-108">Considerations</span></span></th>
<th align="left"><span data-ttu-id="b60a0-109">Detalhes ou finalidade</span><span class="sxs-lookup"><span data-stu-id="b60a0-109">Details or purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b60a0-110">Antes de iniciar a implantação, examine o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b60a0-110">Review the following before you start the deployment:</span></span></p>
<ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="b60a0-111">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="b60a0-111">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="b60a0-112">Configurações com suporte no MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="b60a0-112">MBAM 2.5 Supported Configurations</span></span></a></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="b60a0-113">Cada recurso MBAM tem pré-requisitos específicos que devem ser atendidos antes de iniciar a instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="b60a0-113">Each MBAM feature has specific prerequisites that must be met before you start the MBAM installation.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b60a0-114">As chaves de recuperação do BitLocker no MBAM expiram após um único uso.</span><span class="sxs-lookup"><span data-stu-id="b60a0-114">BitLocker recovery keys in MBAM expire after a single use.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b60a0-115">Um único uso significa que a chave de recuperação foi recuperada por meio do site de administração e monitoramento (também conhecido como Help Desk), do portal de autoatendimento ou do cmdlet Get- <strong> MbamBitLockerRecoveryKey do </strong> Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b60a0-115">A single use means that the recovery key has been retrieved through the Administration and Monitoring Website (also known as Help Desk), Self-Service Portal, or by using the Get-<strong>MbamBitLockerRecoveryKey</strong> Windows PowerShell cmdlet.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b60a0-116">Mantenha o controle dos nomes dos computadores nos quais você configura cada recurso.</span><span class="sxs-lookup"><span data-stu-id="b60a0-116">Keep track of the names of the computers on which you configure each feature.</span></span> <span data-ttu-id="b60a0-117">Você usará essas informações em todo o processo de configuração.</span><span class="sxs-lookup"><span data-stu-id="b60a0-117">You will use this information throughout the configuration process.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b60a0-118">Talvez você queira usar a <a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)"> lista de verificação de implantação do MBAM 2,5 </a> para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="b60a0-118">You may want to use the <a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)">MBAM 2.5 Deployment Checklist</a> for this purpose.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b60a0-119">Configurar apenas as configurações de política de grupo no nó MDOP MBAM (gerenciamento de BitLocker).</span><span class="sxs-lookup"><span data-stu-id="b60a0-119">Configure only the Group Policy settings in the MDOP MBAM (BitLocker Management) node.</span></span> <span data-ttu-id="b60a0-120">Não altere as configurações de política de grupo no nó criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b60a0-120">Do not change the Group Policy settings in the BitLocker Drive Encryption node.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b60a0-121">Se você alterar as configurações de política de grupo no nó de criptografia de unidade de disco BitLocker, o MBAM não funcionará.</span><span class="sxs-lookup"><span data-stu-id="b60a0-121">If you change the Group Policy settings in the BitLocker Drive Encryption node, MBAM will not work.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="planning-for-mbam-server-deployment---stand-alone-topology"></a><span data-ttu-id="b60a0-122">Planejando a implantação do MBAM Server – topologia autônoma</span><span class="sxs-lookup"><span data-stu-id="b60a0-122">Planning for MBAM Server deployment – Stand-alone topology</span></span>


<span data-ttu-id="b60a0-123">Para a topologia autônoma, uma configuração de dois servidores é recomendada para ambientes de produção, embora configurações de três a quatro servidores possam ser usadas.</span><span class="sxs-lookup"><span data-stu-id="b60a0-123">For the Stand-alone topology, a two-server configuration is recommended for production environments, although configurations of three to four servers can be used.</span></span>

<span data-ttu-id="b60a0-124">A infraestrutura de servidor para a topologia autônoma do MBAM contém os seguintes recursos, que devem ser configurados na ordem listada:</span><span class="sxs-lookup"><span data-stu-id="b60a0-124">The Server infrastructure for the MBAM Stand-alone topology contains the following features, which must be configured in the order listed:</span></span>

1.  <span data-ttu-id="b60a0-125">Bancos de dados (banco de dados de conformidade e auditoria e banco de dados de recuperação)</span><span class="sxs-lookup"><span data-stu-id="b60a0-125">Databases (Compliance and Audit Database and Recovery Database)</span></span>

2.  <span data-ttu-id="b60a0-126">Relatórios</span><span class="sxs-lookup"><span data-stu-id="b60a0-126">Reports</span></span>

3.  <span data-ttu-id="b60a0-127">Aplicativos Web (e seus serviços Web correspondentes)</span><span class="sxs-lookup"><span data-stu-id="b60a0-127">Web applications (and their corresponding web services)</span></span>

    -   <span data-ttu-id="b60a0-128">Site de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="b60a0-128">Administration and Monitoring Website</span></span>

    -   <span data-ttu-id="b60a0-129">Portal de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="b60a0-129">Self-Service Portal</span></span>

<span data-ttu-id="b60a0-130">Para obter uma descrição desses recursos, consulte [arquitetura de alto nível do MBAM 2,5 com topologia](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)autônoma.</span><span class="sxs-lookup"><span data-stu-id="b60a0-130">For a description of these features, see [High-Level Architecture of MBAM 2.5 with Stand-alone Topology](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span></span>

## <a href="" id="planning-for-mbam-server-deployment---configuration-manager-topology"></a><span data-ttu-id="b60a0-131">Planejando a implantação do MBAM Server – topologia do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="b60a0-131">Planning for MBAM Server deployment – Configuration Manager topology</span></span>


<span data-ttu-id="b60a0-132">Para a topologia de integração do Configuration Manager, uma configuração de três servidores é recomendada para ambientes de produção, embora as configurações de servidores adicionais possam ser usadas.</span><span class="sxs-lookup"><span data-stu-id="b60a0-132">For the Configuration Manager Integration topology, a three-server configuration is recommended for production environments, although configurations of additional servers can be used.</span></span>

<span data-ttu-id="b60a0-133">A infraestrutura de servidor para a topologia do Gerenciador de configuração do MBAM contém os seguintes recursos, que devem ser configurados ou executados na ordem listada:</span><span class="sxs-lookup"><span data-stu-id="b60a0-133">The Server infrastructure for the MBAM Configuration Manager topology contains the following features, which must be configured or performed in the order listed:</span></span>

1.  <span data-ttu-id="b60a0-134">Bancos de dados (banco de dados de conformidade e auditoria e banco de dados de recuperação)</span><span class="sxs-lookup"><span data-stu-id="b60a0-134">Databases (Compliance and Audit Database and Recovery Database)</span></span>

2.  <span data-ttu-id="b60a0-135">Relatórios</span><span class="sxs-lookup"><span data-stu-id="b60a0-135">Reports</span></span>

3.  <span data-ttu-id="b60a0-136">Aplicativos Web (e seus serviços Web correspondentes)</span><span class="sxs-lookup"><span data-stu-id="b60a0-136">Web applications (and their corresponding web services)</span></span>

    -   <span data-ttu-id="b60a0-137">Site de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="b60a0-137">Administration and Monitoring Website</span></span>

    -   <span data-ttu-id="b60a0-138">Portal de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="b60a0-138">Self-Service Portal</span></span>

4.  <span data-ttu-id="b60a0-139">Integração do System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="b60a0-139">System Center Configuration Manager Integration</span></span>

<span data-ttu-id="b60a0-140">Para obter uma descrição desses recursos, consulte [arquitetura de alto nível do MBAM 2,5 com a topologia de integração do Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="b60a0-140">For a description of these features, see [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span></span>



## <span data-ttu-id="b60a0-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b60a0-141">Related topics</span></span>


[<span data-ttu-id="b60a0-142">Planejando a implantação do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="b60a0-142">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="b60a0-143">Implantando a infraestrutura de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="b60a0-143">Deploying the MBAM 2.5 Server Infrastructure</span></span>](deploying-the-mbam-25-server-infrastructure.md)

 

## <span data-ttu-id="b60a0-144">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="b60a0-144">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="b60a0-145">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="b60a0-145">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="b60a0-146">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="b60a0-146">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





