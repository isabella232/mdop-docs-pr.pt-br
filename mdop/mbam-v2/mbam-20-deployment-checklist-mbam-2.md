---
title: Lista de verificação para implantação do MBAM 2.0
description: Lista de verificação para implantação do MBAM 2.0
author: dansimp
ms.assetid: 7905d31d-f21c-4683-b9c4-95b815e08fab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d8d0ce1a3ff48d4bf2f84e61b4a578b170264a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799872"
---
# <span data-ttu-id="767b1-103">Lista de verificação para implantação do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="767b1-103">MBAM 2.0 Deployment Checklist</span></span>


<span data-ttu-id="767b1-104">Esta lista de verificação pode ser usada para ajudá-lo durante a implantação do Microsoft BitLocker Administration and Monitoring (MBAM) com uma topologia autônoma.</span><span class="sxs-lookup"><span data-stu-id="767b1-104">This checklist can be used to help you during Microsoft BitLocker Administration and Monitoring (MBAM) deployment with a Stand-alone topology.</span></span>

**<span data-ttu-id="767b1-105">Observação</span><span class="sxs-lookup"><span data-stu-id="767b1-105">Note</span></span>**  
<span data-ttu-id="767b1-106">Esta lista de verificação descreve as etapas recomendadas e uma lista de alto nível de itens a serem considerados ao implantar recursos de administração e monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="767b1-106">This checklist outlines the recommended steps and a high-level list of items to consider when deploying Microsoft BitLocker Administration and Monitoring features.</span></span> <span data-ttu-id="767b1-107">É recomendável que você copie esta lista de verificação para um programa de planilha e personalize-a para seu uso.</span><span class="sxs-lookup"><span data-stu-id="767b1-107">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>



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
<th align="left"><span data-ttu-id="767b1-108">Tarefa</span><span class="sxs-lookup"><span data-stu-id="767b1-108">Task</span></span></th>
<th align="left"><span data-ttu-id="767b1-109">Referências</span><span class="sxs-lookup"><span data-stu-id="767b1-109">References</span></span></th>
<th align="left"><span data-ttu-id="767b1-110">Observações</span><span class="sxs-lookup"><span data-stu-id="767b1-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="767b1-111">Conclua a fase de planejamento para preparar o ambiente de computação para a implantação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="767b1-111">Complete the planning phase to prepare the computing environment for MBAM deployment.</span></span></p></td>
<td align="left"><p><a href="mbam-20-planning-checklist-mbam-2.md" data-raw-source="[MBAM 2.0 Planning Checklist](mbam-20-planning-checklist-mbam-2.md)"><span data-ttu-id="767b1-112">Lista de Verificação de Planejamento do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="767b1-112">MBAM 2.0 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="767b1-113">Examine as informações de configurações compatíveis com o MBAM para garantir que os computadores cliente e servidor selecionados tenham suporte para a instalação de recursos do MBAM.</span><span class="sxs-lookup"><span data-stu-id="767b1-113">Review the MBAM supported configurations information to make sure selected client and server computers are supported for MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"><span data-ttu-id="767b1-114">Configurações com suporte no MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="767b1-114">MBAM 2.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="767b1-115">Execute a instalação do MBAM para implantar recursos do MBAM Server na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="767b1-115">Run MBAM Setup to deploy MBAM Server features in the following order:</span></span></p>
<ol>
<li><p><span data-ttu-id="767b1-116">Banco de dados de recuperação</span><span class="sxs-lookup"><span data-stu-id="767b1-116">Recovery Database</span></span></p></li>
<li><p><span data-ttu-id="767b1-117">Banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="767b1-117">Compliance and Audit Database</span></span></p></li>
<li><p><span data-ttu-id="767b1-118">Auditoria e relatórios de conformidade</span><span class="sxs-lookup"><span data-stu-id="767b1-118">Compliance Audit and Reports</span></span></p></li>
<li><p><span data-ttu-id="767b1-119">Servidor de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="767b1-119">Self-Service Server</span></span></p></li>
<li><p><span data-ttu-id="767b1-120">Servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="767b1-120">Administration and Monitoring Server</span></span></p></li>
<li><p><span data-ttu-id="767b1-121">Modelo de política de grupo MBAM</span><span class="sxs-lookup"><span data-stu-id="767b1-121">MBAM Group Policy template</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="767b1-122">Observação</span><span class="sxs-lookup"><span data-stu-id="767b1-122">Note</span></span></strong><br/><p><span data-ttu-id="767b1-123">Mantenha o controle dos nomes dos servidores em que cada recurso está instalado.</span><span class="sxs-lookup"><span data-stu-id="767b1-123">Keep track of the names of the servers each feature is installed on.</span></span> <span data-ttu-id="767b1-124">Essas informações serão usadas em todo o processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="767b1-124">This information will be used throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-20-server-infrastructure-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Server Infrastructure](deploying-the-mbam-20-server-infrastructure-mbam-2.md)"><span data-ttu-id="767b1-125">Implantação da infraestrutura de servidor do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="767b1-125">Deploying the MBAM 2.0 Server Infrastructure</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="767b1-126">Adicione os grupos de segurança dos serviços de domínio do Active Directory criados durante a fase de planejamento ao recurso apropriado do servidor de MBAM local Administradores grupos em servidores adequados.</span><span class="sxs-lookup"><span data-stu-id="767b1-126">Add Active Directory Domain Services security groups created during the planning phase to the appropriate local MBAM Server feature administrators groups on appropriate servers.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="767b1-127">Planejando funções de administrador do MBAM 2,0 </a> e <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> como gerenciar funções de administrador do MBAM</span><span class="sxs-lookup"><span data-stu-id="767b1-127">Planning for MBAM 2.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="767b1-128">Criar e implantar objetos obrigatórios de política de grupo do MBAM.</span><span class="sxs-lookup"><span data-stu-id="767b1-128">Create and deploy required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)"><span data-ttu-id="767b1-129">Implantar Objetos de Política de Grupo no MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="767b1-129">Deploying MBAM 2.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="767b1-130">Implantar o software cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="767b1-130">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)"><span data-ttu-id="767b1-131">Implantando o Cliente do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="767b1-131">Deploying the MBAM 2.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="767b1-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="767b1-132">Related topics</span></span>


[<span data-ttu-id="767b1-133">Implantando o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="767b1-133">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)









