---
title: Lista de verificação para implantação do MBAM 1.0
description: Lista de verificação para implantação do MBAM 1.0
author: dansimp
ms.assetid: 7e00be23-36a0-4b0f-8663-3c4f2c71546d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 96725183af2cb4e3d86d3f42973452c598497773
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796024"
---
# <span data-ttu-id="74063-103">Lista de verificação para implantação do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="74063-103">MBAM 1.0 Deployment Checklist</span></span>


<span data-ttu-id="74063-104">Esta lista de verificação foi projetada para facilitar a implantação do Microsoft BitLocker Administration and Monitoring (MBAM).</span><span class="sxs-lookup"><span data-stu-id="74063-104">This checklist is designed to facilitate your deployment of Microsoft BitLocker Administration and Monitoring (MBAM).</span></span>

**<span data-ttu-id="74063-105">Observação</span><span class="sxs-lookup"><span data-stu-id="74063-105">Note</span></span>**  
<span data-ttu-id="74063-106">Esta lista de verificação descreve as etapas recomendadas e fornece uma lista de alto nível de itens que devem ser considerados ao implantar os recursos do MBAM.</span><span class="sxs-lookup"><span data-stu-id="74063-106">This checklist outlines the recommended steps and provides a high-level list of items to consider when you deploy the MBAM features.</span></span> <span data-ttu-id="74063-107">Recomendamos que você copie esta lista de verificação para um programa de planilha e personalize-a para atender às suas necessidades específicas.</span><span class="sxs-lookup"><span data-stu-id="74063-107">We recommend that you copy this checklist into a spreadsheet program and customize it for your specific needs.</span></span>



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
<th align="left"><span data-ttu-id="74063-108">Tarefa</span><span class="sxs-lookup"><span data-stu-id="74063-108">Task</span></span></th>
<th align="left"><span data-ttu-id="74063-109">Referências</span><span class="sxs-lookup"><span data-stu-id="74063-109">References</span></span></th>
<th align="left"><span data-ttu-id="74063-110">Observações</span><span class="sxs-lookup"><span data-stu-id="74063-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="74063-111">Conclua a fase de planejamento para preparar o ambiente de computação para a implantação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="74063-111">Complete the planning phase to prepare the computing environment for MBAM deployment.</span></span></p></td>
<td align="left"><p><a href="mbam-10-planning-checklist.md" data-raw-source="[MBAM 1.0 Planning Checklist](mbam-10-planning-checklist.md)"><span data-ttu-id="74063-112">Lista de Verificação de Planejamento do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="74063-112">MBAM 1.0 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="74063-113">Revise as informações sobre as configurações compatíveis com o MBAM para garantir que os computadores cliente e servidor selecionados tenham suporte para a instalação do recurso MBAM.</span><span class="sxs-lookup"><span data-stu-id="74063-113">Review the information on MBAM supported configurations to make sure that your selected client and server computers are supported for MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)"><span data-ttu-id="74063-114">Configurações com suporte no MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="74063-114">MBAM 1.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="74063-115">Execute a instalação do MBAM para implantar recursos do MBAM Server na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="74063-115">Run MBAM Setup to deploy MBAM Server features in the following order:</span></span></p>
<ol>
<li><p><span data-ttu-id="74063-116">Recuperação e banco de dados de hardware</span><span class="sxs-lookup"><span data-stu-id="74063-116">Recovery and Hardware Database</span></span></p></li>
<li><p><span data-ttu-id="74063-117">Banco de dados de status de conformidade</span><span class="sxs-lookup"><span data-stu-id="74063-117">Compliance Status Database</span></span></p></li>
<li><p><span data-ttu-id="74063-118">Auditoria e relatórios de conformidade</span><span class="sxs-lookup"><span data-stu-id="74063-118">Compliance Audit and Reports</span></span></p></li>
<li><p><span data-ttu-id="74063-119">Servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="74063-119">Administration and Monitoring Server</span></span></p></li>
<li><p><span data-ttu-id="74063-120">Modelo de política de grupo MBAM</span><span class="sxs-lookup"><span data-stu-id="74063-120">MBAM Group Policy Template</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="74063-121">Observação</span><span class="sxs-lookup"><span data-stu-id="74063-121">Note</span></span></strong><br/><p><span data-ttu-id="74063-122">Mantenha o controle dos nomes dos servidores em que cada recurso está instalado.</span><span class="sxs-lookup"><span data-stu-id="74063-122">Keep track of the names of the servers each feature is installed on.</span></span> <span data-ttu-id="74063-123">Você usará essas informações durante todo o processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="74063-123">You will use this information throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-10-server-infrastructure.md" data-raw-source="[Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md)"><span data-ttu-id="74063-124">Implantando a infraestrutura do Servidor do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="74063-124">Deploying the MBAM 1.0 Server Infrastructure</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="74063-125">Adicione os grupos de segurança dos serviços de domínio Active Directory criados durante a fase de planejamento para os grupos de administradores de recursos de servidor de MBAM locais adequados nos servidores adequados.</span><span class="sxs-lookup"><span data-stu-id="74063-125">Add Active Directory Domain Services security groups created during the planning phase to the appropriate local MBAM Server feature administrators groups on the appropriate servers.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)"><span data-ttu-id="74063-126">Planejando funções de administrador do MBAM 1,0 </a> e <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> como gerenciar funções de administrador do MBAM</span><span class="sxs-lookup"><span data-stu-id="74063-126">Planning for MBAM 1.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="74063-127">Criar e implantar os objetos de política de grupo MBAM necessários.</span><span class="sxs-lookup"><span data-stu-id="74063-127">Create and deploy the required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)"><span data-ttu-id="74063-128">Implantar Objetos de Política de Grupo no MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="74063-128">Deploying MBAM 1.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="74063-129">Implantar o software cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="74063-129">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)"><span data-ttu-id="74063-130">Implantando o Cliente do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="74063-130">Deploying the MBAM 1.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="74063-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="74063-131">Related topics</span></span>


[<span data-ttu-id="74063-132">Implantando o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="74063-132">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)









