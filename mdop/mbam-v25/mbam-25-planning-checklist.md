---
title: Lista de verificação de planejamento para o MBAM 2.5
description: Lista de verificação de planejamento para o MBAM 2.5
author: dansimp
ms.assetid: ffe11eb8-44db-4886-8300-6dffec8bcfa4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 505f2890d67f36056ab5bb87df2a894473cd3306
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799893"
---
# <span data-ttu-id="6942a-103">Lista de verificação de planejamento para o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="6942a-103">MBAM 2.5 Planning Checklist</span></span>


<span data-ttu-id="6942a-104">Você pode usar as listas de verificação a seguir para ajudá-lo a preparar seu ambiente de computação para a implantação do Microsoft BitLocker Administration and Monitoring (MBAM).</span><span class="sxs-lookup"><span data-stu-id="6942a-104">You can use the following checklists to help you prepare your computing environment for the Microsoft BitLocker Administration and Monitoring (MBAM) deployment.</span></span> <span data-ttu-id="6942a-105">As listas de verificação fornecem uma lista de alto nível de itens que devem ser considerados ao planejar a implantação.</span><span class="sxs-lookup"><span data-stu-id="6942a-105">The checklists provide a high-level list of items to consider when planning the deployment.</span></span> <span data-ttu-id="6942a-106">Há listas de verificação separadas para a topologia autônoma e a topologia de integração do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="6942a-106">There are separate checklists for the Stand-alone topology and the Configuration Manager Integration topology.</span></span> <span data-ttu-id="6942a-107">Talvez você queira copiar a lista de verificação desejada para uma planilha e personalizá-la para seu uso.</span><span class="sxs-lookup"><span data-stu-id="6942a-107">You might want to copy the desired checklist into a spreadsheet and customize it for your use.</span></span>

**<span data-ttu-id="6942a-108">Lista de verificação de planejamento para uma implantação do MBAM</span><span class="sxs-lookup"><span data-stu-id="6942a-108">Planning checklist for an MBAM deployment</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="6942a-109">Tarefa</span><span class="sxs-lookup"><span data-stu-id="6942a-109">Task</span></span></th>
<th align="left"><span data-ttu-id="6942a-110">Referências</span><span class="sxs-lookup"><span data-stu-id="6942a-110">References</span></span></th>
<th align="left"><span data-ttu-id="6942a-111">Observações</span><span class="sxs-lookup"><span data-stu-id="6942a-111">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="6942a-112">Revise as &quot; informações de introdução &quot; para entender o produto antes de iniciar o planejamento de implantação.</span><span class="sxs-lookup"><span data-stu-id="6942a-112">Review the &quot;Getting started&quot; information to understand the product before you start deployment planning.</span></span></p></td>
<td align="left"><p><a href="getting-started-with-mbam-25.md" data-raw-source="[Getting Started with MBAM 2.5](getting-started-with-mbam-25.md)"><span data-ttu-id="6942a-113">Introdução ao MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="6942a-113">Getting Started with MBAM 2.5</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="6942a-114">Examine a arquitetura de alto nível recomendada para uma implantação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6942a-114">Review the recommended high-level architecture for an MBAM deployment.</span></span> <span data-ttu-id="6942a-115">Você também pode querer revisar uma ilustração e uma descrição das partes individuais (bancos de dados, sites, relatórios) de uma implantação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6942a-115">You might also want to review an illustration and description of the individual parts (databases, websites, Reports) of an MBAM deployment.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="6942a-116">Arquitetura de alto nível do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="6942a-116">High-Level Architecture for MBAM 2.5</span></span></a></p>
<p><a href="illustrated-features-of-an-mbam-25-deployment.md" data-raw-source="[Illustrated Features of an MBAM 2.5 Deployment](illustrated-features-of-an-mbam-25-deployment.md)"><span data-ttu-id="6942a-117">Recursos ilustrados de uma implantação do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="6942a-117">Illustrated Features of an MBAM 2.5 Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="6942a-118">Revise e conclua os pré-requisitos para as topologias de integração do Gerenciador de configurações e autônomos do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6942a-118">Review and complete the prerequisites for the MBAM Stand-alone and Configuration Manager Integration topologies.</span></span></p></td>
<td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="6942a-119">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6942a-119">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="6942a-120">Se você planeja usar a topologia de integração do Configuration Manager, complete os pré-requisitos adicionais que se aplicam somente a essa topologia.</span><span class="sxs-lookup"><span data-stu-id="6942a-120">If you plan to use the Configuration Manager Integration topology, complete the additional prerequisites that apply only to this topology.</span></span></p></td>
<td align="left"><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="6942a-121">Pré-requisitos do servidor MBAM 2.5 que se aplicam somente à topologia de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6942a-121">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="6942a-122">Examine e conheça os pré-requisitos do MBAM 2,5 para o cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6942a-122">Review and meet the MBAM 2.5 prerequisites for the MBAM Client.</span></span></p></td>
<td align="left"><p><a href="prerequisites-for-mbam-25-clients.md" data-raw-source="[Prerequisites for MBAM 2.5 Clients](prerequisites-for-mbam-25-clients.md)"><span data-ttu-id="6942a-123">Pré-requisitos para clientes do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="6942a-123">Prerequisites for MBAM 2.5 Clients</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="6942a-124">Planeje e configure MBAM requisitos da política de grupo.</span><span class="sxs-lookup"><span data-stu-id="6942a-124">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md)"><span data-ttu-id="6942a-125">Planejamento para os requisitos de Política de Grupo do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="6942a-125">Planning for MBAM 2.5 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="6942a-126">Planeje e crie os grupos de segurança do ActiveDirectoryDomainServices necessários.</span><span class="sxs-lookup"><span data-stu-id="6942a-126">Plan for and create the necessary ActiveDirectoryDomainServices security groups.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)"><span data-ttu-id="6942a-127">Planejamento para contas e grupos do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="6942a-127">Planning for MBAM 2.5 Groups and Accounts</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="6942a-128">Planeje como você vai proteger os sites do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6942a-128">Plan how you will secure the MBAM websites.</span></span></p></td>
<td align="left"><p><a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"><span data-ttu-id="6942a-129">Planejamento de formas para proteger os sites do MBAM</span><span class="sxs-lookup"><span data-stu-id="6942a-129">Planning How to Secure the MBAM Websites</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="6942a-130">Examine as configurações compatíveis com o MBAM para garantir que o seu hardware atenda aos requisitos do sistema de instalação.</span><span class="sxs-lookup"><span data-stu-id="6942a-130">Review the MBAM Supported Configurations to ensure that your hardware meets the installation system requirements.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="6942a-131">Configurações com suporte no MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="6942a-131">MBAM 2.5 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="6942a-132">Examine as considerações para a implantação dos recursos do MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="6942a-132">Review the considerations for deploying the MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-server-deployment.md" data-raw-source="[Planning for MBAM 2.5 Server Deployment](planning-for-mbam-25-server-deployment.md)"><span data-ttu-id="6942a-133">Planejando a implantação de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="6942a-133">Planning for MBAM 2.5 Server Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="6942a-134">Examine as considerações para a implantação do cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="6942a-134">Review the considerations for deploying the MBAM Client.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-client-deployment.md" data-raw-source="[Planning for MBAM 2.5 Client Deployment](planning-for-mbam-25-client-deployment.md)"><span data-ttu-id="6942a-135">Planejando a implantação do cliente do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="6942a-135">Planning for MBAM 2.5 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="6942a-136">Examine os requisitos e as etapas para implantar o MBAM em uma configuração altamente disponível.</span><span class="sxs-lookup"><span data-stu-id="6942a-136">Review the requirements and steps to deploy MBAM in a highly available configuration.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-high-availability.md" data-raw-source="[Planning for MBAM 2.5 High Availability](planning-for-mbam-25-high-availability.md)"><span data-ttu-id="6942a-137">Planejando a alta disponibilidade do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="6942a-137">Planning for MBAM 2.5 High Availability</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="6942a-138">Examine as considerações de segurança MBAM pertinentes ao módulo de plataforma confiável, arquivos de log e criptografia de dados transparente.</span><span class="sxs-lookup"><span data-stu-id="6942a-138">Review the MBAM security considerations that pertain to the Trusted Platform Module, log files, and transparent data encryption.</span></span></p></td>
<td align="left"><p><a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"><span data-ttu-id="6942a-139">Considerações sobre segurança do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="6942a-139">MBAM 2.5 Security Considerations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="6942a-140">Opcionalmente, examine as etapas para avaliar o MBAM em um ambiente de teste.</span><span class="sxs-lookup"><span data-stu-id="6942a-140">Optionally, review the steps to evaluate MBAM in a test environment.</span></span></p></td>
<td align="left"><p><a href="evaluating-mbam-25-in-a-test-environment.md" data-raw-source="[Evaluating MBAM 2.5 in a Test Environment](evaluating-mbam-25-in-a-test-environment.md)"><span data-ttu-id="6942a-141">Avaliando o MBAM 2.5 em um ambiente de teste</span><span class="sxs-lookup"><span data-stu-id="6942a-141">Evaluating MBAM 2.5 in a Test Environment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="6942a-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6942a-142">Related topics</span></span>


[<span data-ttu-id="6942a-143">Planejamento do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="6942a-143">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

 

 
## <span data-ttu-id="6942a-144">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="6942a-144">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="6942a-145">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="6942a-145">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="6942a-146">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="6942a-146">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




