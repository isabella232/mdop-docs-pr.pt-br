---
title: Implantação do catálogo de modelos de configurações para a UE-V 1.0
description: Implantação do catálogo de modelos de configurações para a UE-V 1.0
author: dansimp
ms.assetid: 0e6ab5ef-8eeb-40b4-be7b-a841bd83be96
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f342daa958607a077fa5eb2a27ec705c8d99e67f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799911"
---
# <span data-ttu-id="17129-103">Implantação do catálogo de modelos de configurações para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="17129-103">Deploying the Settings Template Catalog for UE-V 1.0</span></span>


<span data-ttu-id="17129-104">Modelos de local de configurações personalizadas podem ser armazenados em um caminho de pasta nos computadores Microsoft User Experience Virtualization (UE-V) ou em um compartilhamento de rede SMB (bloco de mensagens de servidor).</span><span class="sxs-lookup"><span data-stu-id="17129-104">Custom settings location templates can be stored on a folder path on Microsoft User Experience Virtualization (UE-V) computers or on a Server Message Block (SMB) network share.</span></span> <span data-ttu-id="17129-105">Uma tarefa agendada do computador verifica se há modelos novos ou atualizados deste local.</span><span class="sxs-lookup"><span data-stu-id="17129-105">A scheduled task on the computer checks for new or updated templates from this location.</span></span> <span data-ttu-id="17129-106">A tarefa verifica esse local uma vez por dia e atualiza seu comportamento de sincronização com base nos modelos desta pasta.</span><span class="sxs-lookup"><span data-stu-id="17129-106">The task checks this location once each day and updates its synchronization behavior based on the templates in this folder.</span></span> <span data-ttu-id="17129-107">Os modelos adicionados ou atualizados nesta pasta desde a última verificação são registrados pelo UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="17129-107">Templates that are added or updated in this folder since the last check are registered by the UE-V agent.</span></span> <span data-ttu-id="17129-108">O UE-V Agent cancela o registro de modelos que foram removidos desta pasta.</span><span class="sxs-lookup"><span data-stu-id="17129-108">The UE-V agent deregisters templates that were removed from this folder.</span></span> <span data-ttu-id="17129-109">A tarefa agendada é executada como sistema.</span><span class="sxs-lookup"><span data-stu-id="17129-109">The scheduled task runs as SYSTEM.</span></span> <span data-ttu-id="17129-110">No mínimo, o compartilhamento de rede deve conceder permissões para o grupo computadores do domínio.</span><span class="sxs-lookup"><span data-stu-id="17129-110">At a minimum, the network share must grant permissions for the Domain Computers group.</span></span> <span data-ttu-id="17129-111">Além disso, conceda permissões de acesso à pasta de compartilhamento de rede para administradores que gerenciam os modelos armazenados.</span><span class="sxs-lookup"><span data-stu-id="17129-111">In addition, grant access permissions for the network share folder to administrators who will manage the stored templates.</span></span> <span data-ttu-id="17129-112">Para obter mais informações sobre modelos de localização de configuração personalizada, consulte [planejando a implantação de modelos personalizados para UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="17129-112">For more information about custom setting location templates, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

**<span data-ttu-id="17129-113">Para configurar o catálogo de modelos de configurações para UE-V</span><span class="sxs-lookup"><span data-stu-id="17129-113">To configure the settings template catalog for UE-V</span></span>**

1.  <span data-ttu-id="17129-114">Crie uma nova pasta no computador que irá armazenar o catálogo de modelos de configurações do UE-V.</span><span class="sxs-lookup"><span data-stu-id="17129-114">Create a new folder on the computer that will store the UE-V settings template catalog.</span></span>

2.  <span data-ttu-id="17129-115">Defina as seguintes permissões de nível de compartilhamento (SMB) para a pasta catálogo de modelos de configurações.</span><span class="sxs-lookup"><span data-stu-id="17129-115">Set the following share-level (SMB) permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="17129-116">Conta de usuário</span><span class="sxs-lookup"><span data-stu-id="17129-116">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="17129-117">Permissões recomendadas</span><span class="sxs-lookup"><span data-stu-id="17129-117">Recommend permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="17129-118">Todos</span><span class="sxs-lookup"><span data-stu-id="17129-118">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="17129-119">Nenhuma permissão</span><span class="sxs-lookup"><span data-stu-id="17129-119">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="17129-120">Computadores do domínio</span><span class="sxs-lookup"><span data-stu-id="17129-120">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="17129-121">Ler níveis de permissão</span><span class="sxs-lookup"><span data-stu-id="17129-121">Read Permission Levels</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="17129-122">Administradores</span><span class="sxs-lookup"><span data-stu-id="17129-122">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="17129-123">Níveis de permissão de leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="17129-123">Read/Write Permission Levels</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

3.  <span data-ttu-id="17129-124">Defina as seguintes permissões de NTFS para a pasta catálogo de modelos de configurações.</span><span class="sxs-lookup"><span data-stu-id="17129-124">Set the following NTFS permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="17129-125">Conta de usuário</span><span class="sxs-lookup"><span data-stu-id="17129-125">User Account</span></span></th>
    <th align="left"><span data-ttu-id="17129-126">Permissões recomendadas</span><span class="sxs-lookup"><span data-stu-id="17129-126">Recommended Permissions</span></span></th>
    <th align="left"><span data-ttu-id="17129-127">Aplicar a</span><span class="sxs-lookup"><span data-stu-id="17129-127">Apply To</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="17129-128">Criador/proprietário</span><span class="sxs-lookup"><span data-stu-id="17129-128">Creator/Owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="17129-129">Controle total</span><span class="sxs-lookup"><span data-stu-id="17129-129">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="17129-130">Esta pasta, subpastas e arquivos</span><span class="sxs-lookup"><span data-stu-id="17129-130">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="17129-131">Computadores do domínio</span><span class="sxs-lookup"><span data-stu-id="17129-131">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="17129-132">Listar conteúdo da pasta e ler</span><span class="sxs-lookup"><span data-stu-id="17129-132">List Folder Contents and Read</span></span></p></td>
    <td align="left"><p><span data-ttu-id="17129-133">Esta pasta, subpastas e arquivos</span><span class="sxs-lookup"><span data-stu-id="17129-133">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="17129-134">Todos</span><span class="sxs-lookup"><span data-stu-id="17129-134">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="17129-135">Nenhuma permissão</span><span class="sxs-lookup"><span data-stu-id="17129-135">No Permissions</span></span></p></td>
    <td align="left"><p><span data-ttu-id="17129-136">Nenhuma permissão</span><span class="sxs-lookup"><span data-stu-id="17129-136">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="17129-137">Administradores</span><span class="sxs-lookup"><span data-stu-id="17129-137">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="17129-138">Controle total</span><span class="sxs-lookup"><span data-stu-id="17129-138">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="17129-139">Esta pasta, subpastas e arquivos</span><span class="sxs-lookup"><span data-stu-id="17129-139">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

4.  <span data-ttu-id="17129-140">Clique em **OK** para fechar as caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="17129-140">Click **OK** to close the dialog boxes.</span></span>

## <span data-ttu-id="17129-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="17129-141">Related topics</span></span>


[<span data-ttu-id="17129-142">Implantação da UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="17129-142">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="17129-143">Planejar a implantação de modelo personalizado para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="17129-143">Planning for Custom Template Deployment for UE-V 1.0</span></span>](planning-for-custom-template-deployment-for-ue-v-10.md)

 

 





