---
title: Classe WMI de aplicativo do App-V
description: Classe WMI de aplicativo do App-V
author: dansimp
ms.assetid: b79b0d5a-ba57-442f-8bb4-d7154fc056f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a4e1e49e35b231ddb2a480a06c46e364121ac2d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799049"
---
# <span data-ttu-id="90de0-103">Classe WMI de aplicativo do App-V</span><span class="sxs-lookup"><span data-stu-id="90de0-103">App-V Application WMI Class</span></span>


<span data-ttu-id="90de0-104">No cliente do Application Virtualization (App-V), a classe **Application** é uma classe WMI (Instrumentação de gerenciamento do Windows) que representa todos os aplicativos virtuais do cliente.</span><span class="sxs-lookup"><span data-stu-id="90de0-104">In the Application Virtualization (App-V) Client, the **Application** class is a Windows Management Instrumentation (WMI) class that represents all the virtual applications on the client.</span></span>

<span data-ttu-id="90de0-105">A sintaxe a seguir é simplificada do código MOF (formato de objeto gerenciado).</span><span class="sxs-lookup"><span data-stu-id="90de0-105">The following syntax is simplified from Managed Object Format (MOF) code.</span></span> <span data-ttu-id="90de0-106">O código inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="90de0-106">The code includes all the inherited properties.</span></span>

## <span data-ttu-id="90de0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90de0-107">Syntax</span></span>


``` syntax
class Application
{
      string Name;
      string Version;
      string PackageGUID;
      datetime LastLaunchOnSystem;
      uint32 GlobalRunningCount;
      boolean Loading;
      string OriginalOsdPath;
      string CachedOsdPath;
};
```

## <span data-ttu-id="90de0-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90de0-108">Requirements</span></span>


## <span data-ttu-id="90de0-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="90de0-109">Properties</span></span>


<a href="" id="name"></a>**<span data-ttu-id="90de0-110">Nome</span><span class="sxs-lookup"><span data-stu-id="90de0-110">Name</span></span>**  
<span data-ttu-id="90de0-111">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90de0-111">Data type: **String**</span></span>

<span data-ttu-id="90de0-112">Tipo de acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="90de0-112">Access type: Read-only</span></span>

<span data-ttu-id="90de0-113">Qualificadores: chave</span><span class="sxs-lookup"><span data-stu-id="90de0-113">Qualifiers: Key</span></span>

<span data-ttu-id="90de0-114">O nome de exibição do aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="90de0-114">The display name of the virtual application.</span></span>

<a href="" id="version"></a>**<span data-ttu-id="90de0-115">Versão</span><span class="sxs-lookup"><span data-stu-id="90de0-115">Version</span></span>**  
<span data-ttu-id="90de0-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90de0-116">Data type: **String**</span></span>

<span data-ttu-id="90de0-117">Tipo de acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="90de0-117">Access type: Read-only</span></span>

<span data-ttu-id="90de0-118">Qualificadores: chave</span><span class="sxs-lookup"><span data-stu-id="90de0-118">Qualifiers: Key</span></span>

<span data-ttu-id="90de0-119">A versão do aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="90de0-119">The version of the virtual application.</span></span>

<a href="" id="packageguid"></a>**<span data-ttu-id="90de0-120">PackageGUID</span><span class="sxs-lookup"><span data-stu-id="90de0-120">PackageGUID</span></span>**  
<span data-ttu-id="90de0-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90de0-121">Data type: **String**</span></span>

<span data-ttu-id="90de0-122">Tipo de acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="90de0-122">Access type: Read-only</span></span>

<span data-ttu-id="90de0-123">Qualificadores: nenhum</span><span class="sxs-lookup"><span data-stu-id="90de0-123">Qualifiers: None</span></span>

<span data-ttu-id="90de0-124">O GUID do pacote ao qual o aplicativo virtual está associado.</span><span class="sxs-lookup"><span data-stu-id="90de0-124">The GUID of the package that the virtual application is associated with.</span></span>

<a href="" id="lastlaunchonsystem"></a>**<span data-ttu-id="90de0-125">LastLaunchOnSystem</span><span class="sxs-lookup"><span data-stu-id="90de0-125">LastLaunchOnSystem</span></span>**  
<span data-ttu-id="90de0-126">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="90de0-126">Data type: **DateTime**</span></span>

<span data-ttu-id="90de0-127">Tipo de acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="90de0-127">Access type: Read-only</span></span>

<span data-ttu-id="90de0-128">Qualificadores: nenhum</span><span class="sxs-lookup"><span data-stu-id="90de0-128">Qualifiers: None</span></span>

<span data-ttu-id="90de0-129">A última data e hora em que o aplicativo virtual foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="90de0-129">The last date and time that the virtual application was launched.</span></span>

<a href="" id="globalrunningcount"></a>**<span data-ttu-id="90de0-130">GlobalRunningCount</span><span class="sxs-lookup"><span data-stu-id="90de0-130">GlobalRunningCount</span></span>**  
<span data-ttu-id="90de0-131">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="90de0-131">Data type: **UInt32**</span></span>

<span data-ttu-id="90de0-132">Tipo de acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="90de0-132">Access type: Read-only</span></span>

<span data-ttu-id="90de0-133">Qualificadores: nenhum</span><span class="sxs-lookup"><span data-stu-id="90de0-133">Qualifiers: None</span></span>

<span data-ttu-id="90de0-134">Uma contagem das instâncias em execução do aplicativo virtual que foram iniciadas diretamente.</span><span class="sxs-lookup"><span data-stu-id="90de0-134">A count of the running instances of the virtual application that were started directly.</span></span>

<a href="" id="loading"></a>**<span data-ttu-id="90de0-135">Carregando</span><span class="sxs-lookup"><span data-stu-id="90de0-135">Loading</span></span>**  
<span data-ttu-id="90de0-136">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="90de0-136">Data type: **Boolean**</span></span>

<span data-ttu-id="90de0-137">Tipo de acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="90de0-137">Access type: Read-only</span></span>

<span data-ttu-id="90de0-138">Qualificadores: nenhum</span><span class="sxs-lookup"><span data-stu-id="90de0-138">Qualifiers: None</span></span>

<span data-ttu-id="90de0-139">**verdadeiro** se o aplicativo virtual estiver sendo iniciado; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="90de0-139">**true** if the virtual application is being started; otherwise **false**.</span></span>

<a href="" id="originalosdpath"></a>**<span data-ttu-id="90de0-140">OriginalOsdPath</span><span class="sxs-lookup"><span data-stu-id="90de0-140">OriginalOsdPath</span></span>**  
<span data-ttu-id="90de0-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90de0-141">Data type: **String**</span></span>

<span data-ttu-id="90de0-142">Tipo de acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="90de0-142">Access type: Read-only</span></span>

<span data-ttu-id="90de0-143">Qualificadores: nenhum</span><span class="sxs-lookup"><span data-stu-id="90de0-143">Qualifiers: None</span></span>

<span data-ttu-id="90de0-144">O caminho de arquivo original do arquivo OSD que foi registrado com o cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="90de0-144">The original file path of the OSD file that was registered with the App-V Client.</span></span>

<a href="" id="cachedosdpath"></a>**<span data-ttu-id="90de0-145">CachedOsdPath</span><span class="sxs-lookup"><span data-stu-id="90de0-145">CachedOsdPath</span></span>**  
<span data-ttu-id="90de0-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90de0-146">Data type: **String**</span></span>

<span data-ttu-id="90de0-147">Tipo de acesso: somente leitura</span><span class="sxs-lookup"><span data-stu-id="90de0-147">Access type: Read-only</span></span>

<span data-ttu-id="90de0-148">Qualificadores: nenhum</span><span class="sxs-lookup"><span data-stu-id="90de0-148">Qualifiers: None</span></span>

<span data-ttu-id="90de0-149">O caminho do arquivo OSD se o cliente App-V tiver armazenado em cache o arquivo OSD localmente.</span><span class="sxs-lookup"><span data-stu-id="90de0-149">The file path of the OSD file if the App-V Client has cached the OSD file locally.</span></span>

 

 





