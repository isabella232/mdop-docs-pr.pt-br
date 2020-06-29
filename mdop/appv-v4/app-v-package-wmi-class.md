---
title: Classe WMI de pacote do App-V
description: Classe WMI de pacote do App-V
author: dansimp
ms.assetid: 0fc26c3b-9706-4804-be2d-645771dc33ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa452afaaeb2f490c179a928b24de47207d6dc63
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797597"
---
# <span data-ttu-id="e4bfe-103">Classe WMI de pacote do App-V</span><span class="sxs-lookup"><span data-stu-id="e4bfe-103">App-V Package WMI Class</span></span>


<span data-ttu-id="e4bfe-104">No cliente do Application Virtualization (App-V), a classe **Package** é uma classe WMI (Instrumentação de gerenciamento do Windows) que representa todos os pacotes virtuais no cliente.</span><span class="sxs-lookup"><span data-stu-id="e4bfe-104">In the Application Virtualization (App-V) Client, the **Package** class is a Windows Management Instrumentation (WMI) class that represents all the virtual packages on the client.</span></span> <span data-ttu-id="e4bfe-105">Os pacotes virtuais podem conter muitos aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="e4bfe-105">The virtual packages can contain many virtual applications.</span></span>

## <span data-ttu-id="e4bfe-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4bfe-106">Syntax</span></span>


``` syntax
class Package
{
      string Name;
      string Version;
      string PackageGUID;
      string SftPath;
      uint64 TotalSize;
      uint64 CachedSize;
      uint64 LaunchSize;
      uint64 CachedLaunchSize;
      boolean InUse;
      boolean Locked;
      uint16 CachedPercentage;
      string VersionGUID;
 };
```

## <span data-ttu-id="e4bfe-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e4bfe-107">Properties</span></span>


<a href="" id="name"></a>**<span data-ttu-id="e4bfe-108">Nome</span><span class="sxs-lookup"><span data-stu-id="e4bfe-108">Name</span></span>**  
<span data-ttu-id="e4bfe-109">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e4bfe-109">Data type: **String**</span></span>

<span data-ttu-id="e4bfe-110">Tipo de acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4bfe-110">Access type: Read-only</span></span>

<span data-ttu-id="e4bfe-111">Qualificadores: nenhum</span><span class="sxs-lookup"><span data-stu-id="e4bfe-111">Qualifiers: None</span></span>

<span data-ttu-id="e4bfe-112">O nome de usuário amigável do pacote virtual.</span><span class="sxs-lookup"><span data-stu-id="e4bfe-112">The user-friendly name of the virtual package.</span></span>

<a href="" id="version"></a>**<span data-ttu-id="e4bfe-113">Versão</span><span class="sxs-lookup"><span data-stu-id="e4bfe-113">Version</span></span>**  
<span data-ttu-id="e4bfe-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e4bfe-114">Data type: **String**</span></span>

<span data-ttu-id="e4bfe-115">Tipo de acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4bfe-115">Access type: Read-only</span></span>

<span data-ttu-id="e4bfe-116">Qualificadores: nenhum</span><span class="sxs-lookup"><span data-stu-id="e4bfe-116">Qualifiers: None</span></span>

<span data-ttu-id="e4bfe-117">A versão do pacote virtual.</span><span class="sxs-lookup"><span data-stu-id="e4bfe-117">The version of the virtual package.</span></span>

<a href="" id="packageguid"></a>**<span data-ttu-id="e4bfe-118">PackageGUID</span><span class="sxs-lookup"><span data-stu-id="e4bfe-118">PackageGUID</span></span>**  
<span data-ttu-id="e4bfe-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e4bfe-119">Data type: **String**</span></span>

<span data-ttu-id="e4bfe-120">Tipo de acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4bfe-120">Access type: Read-only</span></span>

<span data-ttu-id="e4bfe-121">Qualificadores: chave</span><span class="sxs-lookup"><span data-stu-id="e4bfe-121">Qualifiers: Key</span></span>

<span data-ttu-id="e4bfe-122">O identificador de GUID dos arquivos de origem e de configuração do pacote.</span><span class="sxs-lookup"><span data-stu-id="e4bfe-122">The GUID identifier of the package configuration and source files.</span></span>

<a href="" id="sftpath"></a>**<span data-ttu-id="e4bfe-123">SftPath</span><span class="sxs-lookup"><span data-stu-id="e4bfe-123">SftPath</span></span>**  
<span data-ttu-id="e4bfe-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e4bfe-124">Data type: **String**</span></span>

<span data-ttu-id="e4bfe-125">Tipo de acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4bfe-125">Access type: Read-only</span></span>

<span data-ttu-id="e4bfe-126">Qualificadores: nenhum</span><span class="sxs-lookup"><span data-stu-id="e4bfe-126">Qualifiers: None</span></span>

<span data-ttu-id="e4bfe-127">O caminho do arquivo SFT.</span><span class="sxs-lookup"><span data-stu-id="e4bfe-127">The file path of the SFT file.</span></span>

<a href="" id="totalsize"></a>**<span data-ttu-id="e4bfe-128">TotalSize</span><span class="sxs-lookup"><span data-stu-id="e4bfe-128">TotalSize</span></span>**  
<span data-ttu-id="e4bfe-129">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e4bfe-129">Data type: **UInt64**</span></span>

<span data-ttu-id="e4bfe-130">Tipo de acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4bfe-130">Access type: Read-only</span></span>

<span data-ttu-id="e4bfe-131">Qualificadores: nenhum</span><span class="sxs-lookup"><span data-stu-id="e4bfe-131">Qualifiers: None</span></span>

<span data-ttu-id="e4bfe-132">O tamanho total do pacote virtual, em quilobytes.</span><span class="sxs-lookup"><span data-stu-id="e4bfe-132">The total size of the virtual package, in kilobytes.</span></span>

<a href="" id="cachedsize"></a>**<span data-ttu-id="e4bfe-133">CachedSize</span><span class="sxs-lookup"><span data-stu-id="e4bfe-133">CachedSize</span></span>**  
<span data-ttu-id="e4bfe-134">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e4bfe-134">Data type: **UInt64**</span></span>

<span data-ttu-id="e4bfe-135">Tipo de acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4bfe-135">Access type: Read-only</span></span>

<span data-ttu-id="e4bfe-136">Qualificadores: nenhum</span><span class="sxs-lookup"><span data-stu-id="e4bfe-136">Qualifiers: None</span></span>

<span data-ttu-id="e4bfe-137">O tamanho total do cache do pacote virtual, em quilobytes.</span><span class="sxs-lookup"><span data-stu-id="e4bfe-137">The total size of the cache for the virtual package, in kilobytes.</span></span>

<a href="" id="launchsize"></a>**<span data-ttu-id="e4bfe-138">LaunchSize</span><span class="sxs-lookup"><span data-stu-id="e4bfe-138">LaunchSize</span></span>**  
<span data-ttu-id="e4bfe-139">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e4bfe-139">Data type: **UInt64**</span></span>

<span data-ttu-id="e4bfe-140">Tipo de acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4bfe-140">Access type: Read-only</span></span>

<span data-ttu-id="e4bfe-141">Qualificadores: nenhum</span><span class="sxs-lookup"><span data-stu-id="e4bfe-141">Qualifiers: None</span></span>

<span data-ttu-id="e4bfe-142">O tamanho total do bloco de recursos principal do pacote virtual, em quilobytes.</span><span class="sxs-lookup"><span data-stu-id="e4bfe-142">The total size of the virtual package’s primary feature block, in kilobytes.</span></span>

<a href="" id="cachedlaunchsize"></a>**<span data-ttu-id="e4bfe-143">CachedLaunchSize</span><span class="sxs-lookup"><span data-stu-id="e4bfe-143">CachedLaunchSize</span></span>**  
<span data-ttu-id="e4bfe-144">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e4bfe-144">Data type: **UInt64**</span></span>

<span data-ttu-id="e4bfe-145">Tipo de acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4bfe-145">Access type: Read-only</span></span>

<span data-ttu-id="e4bfe-146">Qualificadores: nenhum</span><span class="sxs-lookup"><span data-stu-id="e4bfe-146">Qualifiers: None</span></span>

<span data-ttu-id="e4bfe-147">O tamanho total do bloco de recursos primário do pacote virtual que foi armazenado em cache, em kilobytes.</span><span class="sxs-lookup"><span data-stu-id="e4bfe-147">Total size of the virtual package’s primary feature block that has been cached, in kilobytes.</span></span>

<a href="" id="inuse"></a>**<span data-ttu-id="e4bfe-148">InUse</span><span class="sxs-lookup"><span data-stu-id="e4bfe-148">InUse</span></span>**  
<span data-ttu-id="e4bfe-149">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e4bfe-149">Data type: **Boolean**</span></span>

<span data-ttu-id="e4bfe-150">Tipo de acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4bfe-150">Access type: Read-only</span></span>

<span data-ttu-id="e4bfe-151">Qualificadores: nenhum</span><span class="sxs-lookup"><span data-stu-id="e4bfe-151">Qualifiers: None</span></span>

<span data-ttu-id="e4bfe-152">**true** se algum aplicativo virtual do pacote virtual estiver em execução; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="e4bfe-152">**true** if any virtual application in the virtual package is running; otherwise **false**.</span></span>

<a href="" id="locked"></a>**<span data-ttu-id="e4bfe-153">Bloqueado</span><span class="sxs-lookup"><span data-stu-id="e4bfe-153">Locked</span></span>**  
<span data-ttu-id="e4bfe-154">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e4bfe-154">Data type: **Boolean**</span></span>

<span data-ttu-id="e4bfe-155">Tipo de acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4bfe-155">Access type: Read-only</span></span>

<span data-ttu-id="e4bfe-156">Qualificadores: nenhum</span><span class="sxs-lookup"><span data-stu-id="e4bfe-156">Qualifiers: None</span></span>

<span data-ttu-id="e4bfe-157">**verdadeiro** se o pacote virtual estiver bloqueado; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="e4bfe-157">**true** if the virtual package is locked; otherwise **false**.</span></span>

<a href="" id="cachedpercentage"></a>**<span data-ttu-id="e4bfe-158">CachedPercentage</span><span class="sxs-lookup"><span data-stu-id="e4bfe-158">CachedPercentage</span></span>**  
<span data-ttu-id="e4bfe-159">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4bfe-159">Data type: **UInt16**</span></span>

<span data-ttu-id="e4bfe-160">Tipo de acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4bfe-160">Access type: Read-only</span></span>

<span data-ttu-id="e4bfe-161">Qualificadores: nenhum</span><span class="sxs-lookup"><span data-stu-id="e4bfe-161">Qualifiers: None</span></span>

<span data-ttu-id="e4bfe-162">O percentual dos arquivos de cache.</span><span class="sxs-lookup"><span data-stu-id="e4bfe-162">The percentage of the cache files.</span></span> <span data-ttu-id="e4bfe-163">Com base na fórmula a seguir: CachedSize/TotalSize × 100.</span><span class="sxs-lookup"><span data-stu-id="e4bfe-163">Based on the following formula: CachedSize / TotalSize × 100.</span></span>

<a href="" id="versionguid"></a>**<span data-ttu-id="e4bfe-164">VersionGUID</span><span class="sxs-lookup"><span data-stu-id="e4bfe-164">VersionGUID</span></span>**  
<span data-ttu-id="e4bfe-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e4bfe-165">Data type: **String**</span></span>

<span data-ttu-id="e4bfe-166">Tipo de acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4bfe-166">Access type: Read-only</span></span>

<span data-ttu-id="e4bfe-167">Qualificadores: nenhum</span><span class="sxs-lookup"><span data-stu-id="e4bfe-167">Qualifiers: None</span></span>

<span data-ttu-id="e4bfe-168">O identificador de GUID da versão do pacote.</span><span class="sxs-lookup"><span data-stu-id="e4bfe-168">The GUID identifier of the package version.</span></span>

 

 





