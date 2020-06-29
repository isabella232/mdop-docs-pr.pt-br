---
title: Como determinar se um pacote de aplicativo virtual deve ser editado ou atualizado
description: Como determinar se um pacote de aplicativo virtual deve ser editado ou atualizado
author: dansimp
ms.assetid: 33dd5332-6802-46e0-9748-43fcc8f80aa3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b256a4927231613b6f2e688b5951adf57c9cb89a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797138"
---
# <span data-ttu-id="189e7-103">Como determinar se um pacote de aplicativo virtual deve ser editado ou atualizado</span><span class="sxs-lookup"><span data-stu-id="189e7-103">How to Determine Whether to Edit or Upgrade a Virtual Application Package</span></span>


<span data-ttu-id="189e7-104">Use a tabela a seguir para ajudar a determinar se um pacote de aplicativo virtual pode ser aberto para edição, se você precisa criar uma nova versão do pacote, ou se qualquer uma dessas opções está disponível, usando o sequenciador do App-V.</span><span class="sxs-lookup"><span data-stu-id="189e7-104">Use the following table to help determine whether a virtual application package can be opened for edit, whether you need to create a new version of the package, or whether either option is available, using the App-V Sequencer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="189e7-105">Ação</span><span class="sxs-lookup"><span data-stu-id="189e7-105">Action</span></span></th>
<th align="left"><span data-ttu-id="189e7-106">Abrir para edição</span><span class="sxs-lookup"><span data-stu-id="189e7-106">Open for edit</span></span></th>
<th align="left"><span data-ttu-id="189e7-107">Abrir para atualização</span><span class="sxs-lookup"><span data-stu-id="189e7-107">Open for upgrade</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="189e7-108">Exiba as propriedades do pacote.</span><span class="sxs-lookup"><span data-stu-id="189e7-108">View package properties.</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-109">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-109">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-110">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-110">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="189e7-111">Exiba o histórico de alterações do pacote.</span><span class="sxs-lookup"><span data-stu-id="189e7-111">View package change history.</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-112">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-112">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-113">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-113">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="189e7-114">Exibir arquivos de pacote associados.</span><span class="sxs-lookup"><span data-stu-id="189e7-114">View associated package files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-115">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-115">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-116">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-116">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="189e7-117">Editar configurações do registro.</span><span class="sxs-lookup"><span data-stu-id="189e7-117">Edit registry settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-118">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-118">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-119">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-119">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="189e7-120">Revisar configurações de pacote adicionais (exceto propriedades de arquivos do sistema operacional).</span><span class="sxs-lookup"><span data-stu-id="189e7-120">Review additional package settings (except operating system file properties).</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-121">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-121">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-122">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-122">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="189e7-123">Crie um MSI (Windows Installer) associado.</span><span class="sxs-lookup"><span data-stu-id="189e7-123">Create associated Windows Installer (MSI).</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-124">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-124">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-125">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-125">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="189e7-126">Modifique o arquivo OSD.</span><span class="sxs-lookup"><span data-stu-id="189e7-126">Modify OSD file.</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-127">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-127">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-128">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-128">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="189e7-129">Compactar e descompactar pacote.</span><span class="sxs-lookup"><span data-stu-id="189e7-129">Compress and uncompress package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-130">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-130">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-131">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-131">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="189e7-132">Adicionar associações de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="189e7-132">Add file type associations.</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-133">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-133">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-134">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-134">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="189e7-135">Renomear atalhos.</span><span class="sxs-lookup"><span data-stu-id="189e7-135">Rename shortcuts.</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-136">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-136">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-137">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-137">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="189e7-138">Definir o estado virtualizado da chave do registro (override/Merge).</span><span class="sxs-lookup"><span data-stu-id="189e7-138">Set virtualized registry key state (override / merge).</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-139">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-139">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-140">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-140">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="189e7-141">Definir o estado da pasta virtualizada.</span><span class="sxs-lookup"><span data-stu-id="189e7-141">Set virtualized folder state.</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-142">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-142">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-143">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-143">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="189e7-144">Editar mapeamentos do sistema de arquivos virtual.</span><span class="sxs-lookup"><span data-stu-id="189e7-144">Edit virtual file system mappings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-145">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-145">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-146">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-146">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="189e7-147">Revise Todas as propriedades de arquivo de sistema operacional associadas para um pacote.</span><span class="sxs-lookup"><span data-stu-id="189e7-147">Review all associated operating system file properties for a package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-148">Não</span><span class="sxs-lookup"><span data-stu-id="189e7-148">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-149">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-149">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="189e7-150">Adicionar mais serviços.</span><span class="sxs-lookup"><span data-stu-id="189e7-150">Add additional services.</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-151">Não</span><span class="sxs-lookup"><span data-stu-id="189e7-151">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-152">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="189e7-153">Adicionar mais arquivos.</span><span class="sxs-lookup"><span data-stu-id="189e7-153">Add additional files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-154">Não</span><span class="sxs-lookup"><span data-stu-id="189e7-154">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-155">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-155">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="189e7-156">Coletar e configurar descritores de segurança associados.</span><span class="sxs-lookup"><span data-stu-id="189e7-156">Collect and configure associated security descriptors.</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-157">Não</span><span class="sxs-lookup"><span data-stu-id="189e7-157">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-158">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-158">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="189e7-159">Aplicar atualizações de segurança ou atualizar para uma nova versão.</span><span class="sxs-lookup"><span data-stu-id="189e7-159">Apply security updates or upgrade to a new version.</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-160">Não</span><span class="sxs-lookup"><span data-stu-id="189e7-160">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-161">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-161">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="189e7-162">Adicionar um aplicativo adicional.</span><span class="sxs-lookup"><span data-stu-id="189e7-162">Add an additional application.</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-163">Não</span><span class="sxs-lookup"><span data-stu-id="189e7-163">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-164">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-164">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="189e7-165">Aplique atualizações que exijam que o aplicativo seja aberto.</span><span class="sxs-lookup"><span data-stu-id="189e7-165">Apply updates that require the application to open.</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-166">Não</span><span class="sxs-lookup"><span data-stu-id="189e7-166">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-167">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-167">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="189e7-168">Aplique atualizações que exijam que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="189e7-168">Apply updates that require the computer to restart.</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-169">Não</span><span class="sxs-lookup"><span data-stu-id="189e7-169">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="189e7-170">Sim</span><span class="sxs-lookup"><span data-stu-id="189e7-170">Yes</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="189e7-171">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="189e7-171">Related topics</span></span>


[<span data-ttu-id="189e7-172">Como editar um aplicativo virtual existente</span><span class="sxs-lookup"><span data-stu-id="189e7-172">How to Edit an Existing Virtual Application</span></span>](how-to-edit-an-existing-virtual-application.md)

[<span data-ttu-id="189e7-173">Como fazer upgrade de um aplicativo virtual existente</span><span class="sxs-lookup"><span data-stu-id="189e7-173">How to Upgrade an Existing Virtual Application</span></span>](how-to-upgrade-an-existing-virtual-application.md)

 

 





