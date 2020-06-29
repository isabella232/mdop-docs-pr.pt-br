---
title: Lista de verificação para implantação do MBAM 2.5
description: Lista de verificação para implantação do MBAM 2.5
author: dansimp
ms.assetid: 2ba7de17-e3a4-4798-99e0-cd1dc28c5b76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11609b3d6d44d62b032e35005e5d967ca6d4e83b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799151"
---
# <span data-ttu-id="717e5-103">Lista de verificação para implantação do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="717e5-103">MBAM 2.5 Deployment Checklist</span></span>


<span data-ttu-id="717e5-104">Você pode usar esta lista de verificação para ajudá-lo durante a implantação do Microsoft BitLocker Administration and Monitoring (MBAM) com uma topologia autônoma.</span><span class="sxs-lookup"><span data-stu-id="717e5-104">You can use this checklist to help you during Microsoft BitLocker Administration and Monitoring (MBAM) deployment with a Stand-alone topology.</span></span>

**<span data-ttu-id="717e5-105">Observação</span><span class="sxs-lookup"><span data-stu-id="717e5-105">Note</span></span>**  
<span data-ttu-id="717e5-106">Esta lista de verificação descreve as etapas recomendadas e uma lista de alto nível de itens que devem ser considerados ao implantar os recursos de administração e monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="717e5-106">This checklist outlines the recommended steps and a high-level list of items to consider when you deploy Microsoft BitLocker Administration and Monitoring features.</span></span> <span data-ttu-id="717e5-107">Recomendamos que você copie esta lista de verificação para um programa de planilha e personalize-a para seu uso.</span><span class="sxs-lookup"><span data-stu-id="717e5-107">We recommend that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>



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
<th align="left"><span data-ttu-id="717e5-108">Tarefa</span><span class="sxs-lookup"><span data-stu-id="717e5-108">Task</span></span></th>
<th align="left"><span data-ttu-id="717e5-109">Referências</span><span class="sxs-lookup"><span data-stu-id="717e5-109">References</span></span></th>
<th align="left"><span data-ttu-id="717e5-110">Observações</span><span class="sxs-lookup"><span data-stu-id="717e5-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="717e5-111">Revise e conclua todas as etapas de planejamento para preparar seu ambiente para a implantação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="717e5-111">Review and complete all planning steps to prepare your environment for MBAM deployment.</span></span></p></td>
<td align="left"><p><a href="mbam-25-planning-checklist.md" data-raw-source="[MBAM 2.5 Planning Checklist](mbam-25-planning-checklist.md)"><span data-ttu-id="717e5-112">Lista de verificação de planejamento para o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="717e5-112">MBAM 2.5 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="717e5-113">Examine as informações de configurações compatíveis para garantir que o MBAM suporte os computadores cliente e servidor selecionados.</span><span class="sxs-lookup"><span data-stu-id="717e5-113">Review the supported configurations information to ensure that MBAM supports the selected client and server computers.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="717e5-114">Configurações com suporte no MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="717e5-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="717e5-115">Instale o software MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="717e5-115">Install the MBAM Server software.</span></span></p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="717e5-116">Instalando o software de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="717e5-116">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="717e5-117">Configurar os recursos do servidor do MBAM:</span><span class="sxs-lookup"><span data-stu-id="717e5-117">Configure the MBAM Server features:</span></span></p>
<ul>
<li><p><span data-ttu-id="717e5-118">Banco de dados de conformidade e auditoria e banco de dados de recuperação</span><span class="sxs-lookup"><span data-stu-id="717e5-118">Compliance and Audit Database and Recovery Database</span></span></p></li>
<li><p><span data-ttu-id="717e5-119">Relatórios</span><span class="sxs-lookup"><span data-stu-id="717e5-119">Reports</span></span></p></li>
<li><p><span data-ttu-id="717e5-120">Aplicativos Web</span><span class="sxs-lookup"><span data-stu-id="717e5-120">Web applications</span></span></p></li>
<li><p><span data-ttu-id="717e5-121">A topologia de integração do Configuration Manager (necessária somente se você estiver executando o MBAM com essa topologia)</span><span class="sxs-lookup"><span data-stu-id="717e5-121">Configuration Manager Integration topology (needed only if you are running MBAM with this topology)</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="717e5-122">Observação</span><span class="sxs-lookup"><span data-stu-id="717e5-122">Note</span></span></strong><br/><p><span data-ttu-id="717e5-123">Observe os nomes dos servidores nos quais você configura cada recurso.</span><span class="sxs-lookup"><span data-stu-id="717e5-123">Note the names of the servers on which you configure each feature.</span></span> <span data-ttu-id="717e5-124">Você usará essas informações em todo o processo de configuração.</span><span class="sxs-lookup"><span data-stu-id="717e5-124">You will use this information throughout the configuration process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="configuring-the-mbam-25-server-features.md" data-raw-source="[Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md)"><span data-ttu-id="717e5-125">Configurando os recursos de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="717e5-125">Configuring the MBAM 2.5 Server Features</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="717e5-126">Valide a configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="717e5-126">Validate the MBAM configuration.</span></span></p></td>
<td align="left"><p><a href="validating-the-mbam-25-server-feature-configuration.md" data-raw-source="[Validating the MBAM 2.5 Server Feature Configuration](validating-the-mbam-25-server-feature-configuration.md)"><span data-ttu-id="717e5-127">Validando a configuração de recursos de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="717e5-127">Validating the MBAM 2.5 Server Feature Configuration</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="717e5-128">Copie o modelo de política de grupo do MBAM e edite as configurações de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="717e5-128">Copy the MBAM Group Policy Template and edit the Group Policy settings.</span></span></p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)"><span data-ttu-id="717e5-129">Copiando os modelos de política de grupo do MBAM 2,5 </a> e <a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)"> editando as configurações de política de grupo do MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="717e5-129">Copying the MBAM 2.5 Group Policy Templates</a> and <a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)">Editing the MBAM 2.5 Group Policy Settings</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="717e5-130">Implantar o software cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="717e5-130">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-25-client.md" data-raw-source="[Deploying the MBAM 2.5 Client](deploying-the-mbam-25-client.md)"><span data-ttu-id="717e5-131">Implantando o cliente do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="717e5-131">Deploying the MBAM 2.5 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>




## <span data-ttu-id="717e5-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="717e5-132">Related topics</span></span>


[<span data-ttu-id="717e5-133">Implantando o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="717e5-133">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)




## <span data-ttu-id="717e5-134">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="717e5-134">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="717e5-135">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="717e5-135">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="717e5-136">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="717e5-136">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




