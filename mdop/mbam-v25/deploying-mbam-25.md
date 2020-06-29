---
title: Implantando o MBAM 2.5
description: Implantando o MBAM 2.5
author: dansimp
ms.assetid: 45403607-1f4d-42fe-8413-0d4da01808a6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0cfa0a190530186211cd96884b2e32e9c65881f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799841"
---
# <span data-ttu-id="be508-103">Implantando o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="be508-103">Deploying MBAM 2.5</span></span>


<span data-ttu-id="be508-104">Use essas informações para identificar os procedimentos que você pode seguir para implantar e configurar os recursos de servidor do Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 para atualizar para o MBAM 2,5 de versões anteriores ou para remover recursos do MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="be508-104">Use this information to identify the procedures you can follow to deploy and configure Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server features to upgrade to MBAM 2.5 from previous versions, or to remove MBAM Server features.</span></span>

## <span data-ttu-id="be508-105">Informações de implantação</span><span class="sxs-lookup"><span data-stu-id="be508-105">Deployment information</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="be508-106">Descrição do tópico</span><span class="sxs-lookup"><span data-stu-id="be508-106">Topic description</span></span></th>
<th align="left"><span data-ttu-id="be508-107">Links para tópicos</span><span class="sxs-lookup"><span data-stu-id="be508-107">Links to topics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="be508-108">Opções de topologia de implantação.</span><span class="sxs-lookup"><span data-stu-id="be508-108">Deployment topology options.</span></span></p></li>
<li><p><span data-ttu-id="be508-109">Como instalar o software MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="be508-109">How to install the MBAM Server software.</span></span></p></li>
<li><p><span data-ttu-id="be508-110">Como configurar os recursos do servidor do MBAM.</span><span class="sxs-lookup"><span data-stu-id="be508-110">How to configure the MBAM Server features.</span></span></p></li>
</ul></td>
<td align="left"><p><a href="deploying-the-mbam-25-server-infrastructure.md" data-raw-source="[Deploying the MBAM 2.5 Server Infrastructure](deploying-the-mbam-25-server-infrastructure.md)"><span data-ttu-id="be508-111">Implantando a infraestrutura de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="be508-111">Deploying the MBAM 2.5 Server Infrastructure</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be508-112">Como baixar e implantar os modelos de política de grupo do MBAM, que são necessários para gerenciar clientes do MBAM e políticas de criptografia do BitLocker na empresa.</span><span class="sxs-lookup"><span data-stu-id="be508-112">How to download and deploy the MBAM Group Policy Templates, which are required to manage MBAM Clients and BitLocker encryption policies in the enterprise.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-25-group-policy-objects.md" data-raw-source="[Deploying MBAM 2.5 Group Policy Objects](deploying-mbam-25-group-policy-objects.md)"><span data-ttu-id="be508-113">Implantando objetos de Política de Grupo do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="be508-113">Deploying MBAM 2.5 Group Policy Objects</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be508-114">Como usar os arquivos do Windows Installer do cliente MBAM para implantar o software cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="be508-114">How to use the MBAM Client Windows Installer files to deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-25-client.md" data-raw-source="[Deploying the MBAM 2.5 Client](deploying-the-mbam-25-client.md)"><span data-ttu-id="be508-115">Implantando o cliente do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="be508-115">Deploying the MBAM 2.5 Client</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be508-116">Lista de verificação que pode ajudá-lo a implantar os recursos do MBAM Server e o cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="be508-116">Checklist that can assist you in deploying the MBAM Server features and MBAM Client.</span></span></p></td>
<td align="left"><p><a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)"><span data-ttu-id="be508-117">Lista de verificação para implantação do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="be508-117">MBAM 2.5 Deployment Checklist</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="be508-118">Como atualizar o MBAM a partir de versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="be508-118">How to upgrade MBAM from previous versions.</span></span></p></td>
<td align="left"><p><a href="upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions.md" data-raw-source="[Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions](upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions.md)"><span data-ttu-id="be508-119">Atualizando para o MBAM 2.5 ou MBAM 2.5 SP1 de versões anteriores</span><span class="sxs-lookup"><span data-stu-id="be508-119">Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="be508-120">Como remover o software ou os recursos do MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="be508-120">How to remove MBAM Server features or software.</span></span></p></td>
<td align="left"><p><a href="removing-mbam-server-features-or-software.md" data-raw-source="[Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md)"><span data-ttu-id="be508-121">Removendo os recursos de servidor ou o software do MBAM</span><span class="sxs-lookup"><span data-stu-id="be508-121">Removing MBAM Server Features or Software</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="be508-122">Outros recursos para a implantação do MBAM</span><span class="sxs-lookup"><span data-stu-id="be508-122">Other resources for deploying MBAM</span></span>


[<span data-ttu-id="be508-123">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="be508-123">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](index.md)

[<span data-ttu-id="be508-124">Introdução ao MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="be508-124">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

[<span data-ttu-id="be508-125">Planejamento do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="be508-125">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

[<span data-ttu-id="be508-126">Operações do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="be508-126">Operations for MBAM 2.5</span></span>](operations-for-mbam-25.md)

[<span data-ttu-id="be508-127">Solução de problemas do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="be508-127">Troubleshooting MBAM 2.5</span></span>](troubleshooting-mbam-25.md)

[<span data-ttu-id="be508-128">Referência técnica do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="be508-128">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)

[<span data-ttu-id="be508-129">Implantação do MBAM 2.5 em uma configuração autônoma</span><span class="sxs-lookup"><span data-stu-id="be508-129">Deploying MBAM 2.5 in a stand-alone configuration</span></span>](https://support.microsoft.com/kb/3046555)

## <span data-ttu-id="be508-130">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="be508-130">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="be508-131">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="be508-131">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="be508-132">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="be508-132">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





