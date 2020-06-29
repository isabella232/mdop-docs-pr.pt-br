---
title: Como trabalhar com modelos personalizados da UE-V e com o gerador da UE-V
description: Como trabalhar com modelos personalizados da UE-V e com o gerador da UE-V
author: dansimp
ms.assetid: 7bb2583a-b032-4800-9bf9-eb33528e1d0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: db5387254842bfdcf3898089bc12a8e929e3813a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799380"
---
# <span data-ttu-id="72903-103">Como trabalhar com modelos personalizados da UE-V e com o gerador da UE-V</span><span class="sxs-lookup"><span data-stu-id="72903-103">Working with Custom UE-V Templates and the UE-V Generator</span></span>


<span data-ttu-id="72903-104">Para fazer roaming de aplicativos entre computadores de usuário, o Microsoft User Experience Virtualization (UE-V it Virtualization) usa *modelos de local de configurações*.</span><span class="sxs-lookup"><span data-stu-id="72903-104">In order to roam applications between user computers, Microsoft User Experience Virtualization (UE-V) uses *settings location templates*.</span></span> <span data-ttu-id="72903-105">Alguns modelos de local de configurações estão incluídos na virtualização da experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="72903-105">Some settings location templates are included with User Experience Virtualization.</span></span> <span data-ttu-id="72903-106">Você também pode criar, editar ou validar modelos de local de configurações personalizadas com o UE-V Generator.</span><span class="sxs-lookup"><span data-stu-id="72903-106">You can also create, edit, or validate custom settings location templates with the UE-V Generator.</span></span>

<span data-ttu-id="72903-107">O UE-V Generator monitora um aplicativo para descobrir e capturar os locais onde o aplicativo armazena suas configurações.</span><span class="sxs-lookup"><span data-stu-id="72903-107">The UE-V Generator monitors an application to discover and capture the locations where the application stores its settings.</span></span> <span data-ttu-id="72903-108">O aplicativo que está sendo monitorado deve ser um aplicativo tradicional.</span><span class="sxs-lookup"><span data-stu-id="72903-108">The application being monitored must be a traditional application.</span></span> <span data-ttu-id="72903-109">O UE-V Generator não pode criar um modelo de local de configurações para os seguintes tipos de aplicativos:</span><span class="sxs-lookup"><span data-stu-id="72903-109">The UE-V Generator cannot create a settings location template for the following application types:</span></span>

-   <span data-ttu-id="72903-110">Aplicativos virtualizados</span><span class="sxs-lookup"><span data-stu-id="72903-110">Virtualized applications</span></span>

-   <span data-ttu-id="72903-111">Aplicativo oferecido por meio dos serviços de terminal</span><span class="sxs-lookup"><span data-stu-id="72903-111">Application offered through terminal services</span></span>

-   <span data-ttu-id="72903-112">Aplicativos Java</span><span class="sxs-lookup"><span data-stu-id="72903-112">Java applications</span></span>

-   <span data-ttu-id="72903-113">Aplicativos do Windows 8</span><span class="sxs-lookup"><span data-stu-id="72903-113">Windows 8 applications</span></span>

## <span data-ttu-id="72903-114">Criar modelos de localização de configurações da UE-V com o gerador da UE-V</span><span class="sxs-lookup"><span data-stu-id="72903-114">Create UE-V Settings Location Templates with the UE-V Generator</span></span>


<span data-ttu-id="72903-115">Como usar o UE-V Generator para criar modelos de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="72903-115">How to use the UE-V Generator to create settings location templates.</span></span>

[<span data-ttu-id="72903-116">Criar modelos de localização de configurações da UE-V com o gerador da UE-V</span><span class="sxs-lookup"><span data-stu-id="72903-116">Create UE-V Settings Location Templates with the UE-V Generator</span></span>](create-ue-v-settings-location-templates-with-the-ue-v-generator.md)

## <span data-ttu-id="72903-117">Editar modelos de localização de configurações da UE-V com o gerador da UE-V</span><span class="sxs-lookup"><span data-stu-id="72903-117">Edit UE-V Settings Location Templates with the UE-V Generator</span></span>


<span data-ttu-id="72903-118">Como usar o UE-V Generator para editar modelos de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="72903-118">How to use the UE-V Generator to edit settings location templates.</span></span>

[<span data-ttu-id="72903-119">Editar modelos de localização de configurações da UE-V com o gerador da UE-V</span><span class="sxs-lookup"><span data-stu-id="72903-119">Edit UE-V Settings Location Templates with the UE-V Generator</span></span>](edit-ue-v-settings-location-templates-with-the-ue-v-generator.md)

## <span data-ttu-id="72903-120">Validar modelos de localização de configurações da UE-V com o gerador da UE-V</span><span class="sxs-lookup"><span data-stu-id="72903-120">Validate UE-V Settings Location Templates with UE-V Generator</span></span>


<span data-ttu-id="72903-121">Como usar o UE-V Generator para validar modelos de local de configurações modificados fora do gerador do UE-V.</span><span class="sxs-lookup"><span data-stu-id="72903-121">How to use the UE-V Generator to validate settings location templates modified outside the UE-V Generator.</span></span>

[<span data-ttu-id="72903-122">Validar modelos de localização de configurações da UE-V com o gerador da UE-V</span><span class="sxs-lookup"><span data-stu-id="72903-122">Validate UE-V Settings Location Templates with UE-V Generator</span></span>](validate-ue-v-settings-location-templates-with-ue-v-generator.md)

## <a href="" id="bkmk-standardnonstandardsettingslocations"></a><span data-ttu-id="72903-123">Locais de configurações padrão e não padrão</span><span class="sxs-lookup"><span data-stu-id="72903-123">Standard and Nonstandard settings locations</span></span>


<span data-ttu-id="72903-124">O UE-V Generator ajuda você a identificar onde os aplicativos procuram arquivos de configurações e configurações do registro que os aplicativos usam para armazenar as informações das configurações.</span><span class="sxs-lookup"><span data-stu-id="72903-124">The UE-V Generator helps you identify where applications look for settings files and registry settings that applications use to store settings information.</span></span> <span data-ttu-id="72903-125">Você pode usar o UE-V Generator para abrir o aplicativo como parte do processo de descoberta para capturar as configurações em locais padrão.</span><span class="sxs-lookup"><span data-stu-id="72903-125">You can use the UE-V Generator to open the application as part of the discovery process to capture settings in standard locations.</span></span> <span data-ttu-id="72903-126">Os locais padrão incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="72903-126">Standard locations include the following:</span></span>

-   <span data-ttu-id="72903-127">**Configurações do registro** – locais do registro em **HKEY \ _CURRENT \ _USER**</span><span class="sxs-lookup"><span data-stu-id="72903-127">**Registry Settings** – Registry locations under **HKEY\_CURRENT\_USER**</span></span>

-   <span data-ttu-id="72903-128">**Arquivos de configurações do aplicativo** – arquivos armazenados em \ \ **usuários** \ \ [nome de usuário \] \ \ **AppData**em  \\  **roaming**</span><span class="sxs-lookup"><span data-stu-id="72903-128">**Application Settings Files** – Files stored under \\ **Users** \\ \[User name\] \\ **AppData** \\ **Roaming**</span></span>

<span data-ttu-id="72903-129">O gerador do UE-V exclui locais que normalmente armazenam arquivos de software do aplicativo, não se movimente bem entre computadores ou ambientes do usuário.</span><span class="sxs-lookup"><span data-stu-id="72903-129">The UE-V Generator excludes locations which commonly store application software files do not roam well between user computers or environments.</span></span> <span data-ttu-id="72903-130">O gerador do UE-V exclui estes locais.</span><span class="sxs-lookup"><span data-stu-id="72903-130">The UE-V Generator excludes these locations.</span></span> <span data-ttu-id="72903-131">Locais excluídos são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="72903-131">Excluded locations are as follows:</span></span>

-   <span data-ttu-id="72903-132">HKEY \ _CURRENT \ _USER chaves do registro e arquivos para os quais o usuário conectado não pode gravar valores</span><span class="sxs-lookup"><span data-stu-id="72903-132">HKEY\_CURRENT\_USER registry keys and files to which the logged-on user cannot write values</span></span>

-   <span data-ttu-id="72903-133">HKEY \ _CURRENT \ _USER chaves do registro e arquivos associados à funcionalidade central do sistema operacional Windows</span><span class="sxs-lookup"><span data-stu-id="72903-133">HKEY\_CURRENT\_USER registry keys and files that are associated with the core functionality of the Windows operating system</span></span>

-   <span data-ttu-id="72903-134">Todas as chaves do registro localizadas no hive \ _LOCAL \ _MACHINE Hive (requer direitos de administrador e exija que o contrato de UAC seja definido)</span><span class="sxs-lookup"><span data-stu-id="72903-134">All registry keys that are located in the HKEY\_LOCAL\_MACHINE hive (Requires Administrator rights and might require UAC agreement to set)</span></span>

-   <span data-ttu-id="72903-135">Arquivos localizados em diretórios de arquivos de programas (exige direitos de administrador e podem exigir um contrato de UAC para definir)</span><span class="sxs-lookup"><span data-stu-id="72903-135">Files that are located in Program Files directories (Requires Administrator rights and might require UAC agreement to set)</span></span>

-   <span data-ttu-id="72903-136">Arquivos localizados em Usuários \ \ \ [nome de usuário \] \ \ AppData \ \ LocalLow</span><span class="sxs-lookup"><span data-stu-id="72903-136">Files located in Users \\ \[User name\] \\ AppData \\ LocalLow</span></span>

-   <span data-ttu-id="72903-137">Arquivos do sistema operacional do Windows localizados em% SystemRoot% (exige direitos de administrador e podem exigir um contrato de UAC para definir)</span><span class="sxs-lookup"><span data-stu-id="72903-137">Windows operating system files that are located in %systemroot% (Requires Administrator rights and might require UAC agreement to set)</span></span>

<span data-ttu-id="72903-138">Se as chaves do registro e os arquivos armazenados nesses locais forem necessários para fazer roaming das configurações do aplicativo, você pode adicionar manualmente os locais excluídos ao modelo de local de configurações durante o processo de criação de modelos.</span><span class="sxs-lookup"><span data-stu-id="72903-138">If registry keys and files stored in these locations are required in order to roam application settings, you can manually add the excluded locations to the settings location template during the template creation process.</span></span>

## <span data-ttu-id="72903-139">Outros recursos para este produto</span><span class="sxs-lookup"><span data-stu-id="72903-139">Other resources for this product</span></span>


[<span data-ttu-id="72903-140">Operações para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="72903-140">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

[<span data-ttu-id="72903-141">Administração da UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="72903-141">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

 

 





