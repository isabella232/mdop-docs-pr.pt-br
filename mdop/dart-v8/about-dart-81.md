---
title: Sobre o DaRT 8.1
description: Sobre o DaRT 8.1
author: dansimp
ms.assetid: dcaddc57-0111-4a9d-8be9-f5ada0eefa7d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 29c7522b4f5a5da3b451b23f2fd200db44bb9481
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797890"
---
# <span data-ttu-id="407a5-103">Sobre o DaRT 8.1</span><span class="sxs-lookup"><span data-stu-id="407a5-103">About DaRT 8.1</span></span>


<span data-ttu-id="407a5-104">O conjunto de ferramentas de diagnóstico e recuperação (DaRT) da Microsoft 8,1 fornece os seguintes aprimoramentos, que estão descritos neste tópico.</span><span class="sxs-lookup"><span data-stu-id="407a5-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.1 provides the following enhancements, which are described in this topic.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="407a5-105">O que há de novo</span><span class="sxs-lookup"><span data-stu-id="407a5-105">What’s new</span></span>


-   **<span data-ttu-id="407a5-106">Suporte para o WIMBoot</span><span class="sxs-lookup"><span data-stu-id="407a5-106">Support for WIMBoot</span></span>**

    <span data-ttu-id="407a5-107">O conjunto de ferramentas de diagnóstico e recuperação 8,1 dá suporte ao ambiente do Windows Image File boot (WIMBoot) se essas condições forem atendidas:</span><span class="sxs-lookup"><span data-stu-id="407a5-107">Diagnostics and Recovery Toolset 8.1 supports the Windows image file boot (WIMBoot) environment if these conditions are met:</span></span>

    -   <span data-ttu-id="407a5-108">O WIMBoot se baseia na atualização 1 do Windows 8,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="407a5-108">WIMBoot is based on Windows 8.1 Update 1 or later.</span></span>

    -   <span data-ttu-id="407a5-109">A imagem do DaRT 8,1 é criada no Windows 8,1 atualização 1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="407a5-109">The DaRT 8.1 image is built on Windows 8.1 Update 1 or later.</span></span>

    <span data-ttu-id="407a5-110">Para obter mais informações sobre o WIMBoot, consulte [visão geral do Windows Image File boot (WIMBoot)](https://go.microsoft.com/fwlink/?LinkId=517536).</span><span class="sxs-lookup"><span data-stu-id="407a5-110">For more information about WIMBoot, see [Windows Image File Boot (WIMBoot) Overview](https://go.microsoft.com/fwlink/?LinkId=517536).</span></span>

-   **<span data-ttu-id="407a5-111">Suporte para Windows Server 2012 R2 e Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="407a5-111">Support for Windows Server 2012 R2 and Windows 8.1</span></span>**

    <span data-ttu-id="407a5-112">Você pode criar imagens DaRT usando o Windows Server 2012 R2 ou o Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="407a5-112">You can create DaRT images by using Windows Server 2012 R2 or Windows 8.1.</span></span>

    **<span data-ttu-id="407a5-113">Observação</span><span class="sxs-lookup"><span data-stu-id="407a5-113">Note</span></span>**  
    <span data-ttu-id="407a5-114">Para versões anteriores do Windows Server e sistemas operacionais Windows, continue a usar as versões anteriores do DaRT.</span><span class="sxs-lookup"><span data-stu-id="407a5-114">For earlier versions of the Windows Server and Windows operating systems, continue to use the earlier versions of DaRT.</span></span>



-   **<span data-ttu-id="407a5-115">Comentários do cliente</span><span class="sxs-lookup"><span data-stu-id="407a5-115">Customer feedback</span></span>**

    <span data-ttu-id="407a5-116">O DaRT 8,1 inclui atualizações que abordam problemas encontrados desde a versão DaRT 8,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="407a5-116">DaRT 8.1 includes updates that address issues found since the DaRT 8.0 SP1 release.</span></span>

-   **<span data-ttu-id="407a5-117">Windows Defender</span><span class="sxs-lookup"><span data-stu-id="407a5-117">Windows Defender</span></span>**

    <span data-ttu-id="407a5-118">O Windows Defender no Windows 8,1 inclui proteção aprimorada.</span><span class="sxs-lookup"><span data-stu-id="407a5-118">Windows Defender in Windows 8.1 includes improved protection.</span></span> <span data-ttu-id="407a5-119">As alterações não afetam a maneira como você usa o DaRT com o Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="407a5-119">The changes do not impact how you use DaRT with Windows Defender.</span></span>

## <span data-ttu-id="407a5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="407a5-120">Requirements</span></span>


-   **<span data-ttu-id="407a5-121">Kit de avaliação e desenvolvimento do Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="407a5-121">Windows Assessment and Development Kit 8.1</span></span>**

    <span data-ttu-id="407a5-122">O kit de avaliação e desenvolvimento do Windows (ADK) 8,1 é um pré-requisito obrigatório para o assistente de imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="407a5-122">Windows Assessment and Development Kit (ADK) 8.1 is a required prerequisite for the DaRT Recovery Image Wizard.</span></span> <span data-ttu-id="407a5-123">O Windows ADK 8,1 contém ferramentas de implantação usadas para personalizar, implantar e fazer a manutenção de imagens do Windows.</span><span class="sxs-lookup"><span data-stu-id="407a5-123">Windows ADK 8.1 contains deployment tools that are used to customize, deploy, and service Windows images.</span></span> <span data-ttu-id="407a5-124">Ele também contém o ambiente de pré-instalação do Windows (Windows PE).</span><span class="sxs-lookup"><span data-stu-id="407a5-124">It also contains the Windows Preinstallation Environment (Windows PE).</span></span>

    **<span data-ttu-id="407a5-125">Observação</span><span class="sxs-lookup"><span data-stu-id="407a5-125">Note</span></span>**  
    <span data-ttu-id="407a5-126">O Windows ADK 8,1 não será necessário se você estiver instalando apenas o Visualizador de conexão remota ou o Crash Analyzer.</span><span class="sxs-lookup"><span data-stu-id="407a5-126">Windows ADK 8.1 is not required if you are installing only Remote Connection Viewer or Crash Analyzer.</span></span>



~~~
To download Windows ADK 8.1, see [Windows Assessment and Deployment Kit (Windows ADK) for Windows 8.1](https://www.microsoft.com/download/details.aspx?id=39982) in the Microsoft Download Center.
~~~

-   **<span data-ttu-id="407a5-127">Microsoft .NET Framework 4.5.1</span><span class="sxs-lookup"><span data-stu-id="407a5-127">Microsoft .NET Framework 4.5.1</span></span>**

    <span data-ttu-id="407a5-128">O DaRT 8,1 requer que o .NET Framework 4.5.1 esteja instalado.</span><span class="sxs-lookup"><span data-stu-id="407a5-128">DaRT 8.1 requires that .NET Framework 4.5.1 is installed.</span></span> <span data-ttu-id="407a5-129">Para baixar, consulte [Microsoft.NET Framework 4.5.1](https://go.microsoft.com/fwlink/?LinkId=329038) no centro de download da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="407a5-129">To download, see [Microsoft.NET Framework 4.5.1](https://go.microsoft.com/fwlink/?LinkId=329038) in the Microsoft Download Center.</span></span>

-   **<span data-ttu-id="407a5-130">Ferramentas de depuração do Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="407a5-130">Windows 8.1 Debugging Tools</span></span>**

    <span data-ttu-id="407a5-131">Para usar a ferramenta Crash Analyzer no DaRT 8,1, você precisa das ferramentas de depuração necessárias, que estão disponíveis no kit de desenvolvimento de software para Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="407a5-131">To use the Crash Analyzer tool in DaRT 8.1, you need the required debugging tools, which are available in the Software Development Kit for Windows 8.1.</span></span>

    <span data-ttu-id="407a5-132">Para baixar, consulte o [Software Development Kit do Windows (SDK) para windows 8,1](https://msdn.microsoft.com/library/windows/desktop/bg162891.aspx) no centro de download da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="407a5-132">To download, see [Windows Software Development Kit (SDK) for Windows 8.1](https://msdn.microsoft.com/library/windows/desktop/bg162891.aspx) in the Microsoft Download Center.</span></span>

## <span data-ttu-id="407a5-133">Disponibilidade do idioma</span><span class="sxs-lookup"><span data-stu-id="407a5-133">Language availability</span></span>


<span data-ttu-id="407a5-134">O DaRT 8,1 está disponível nos seguintes idiomas:</span><span class="sxs-lookup"><span data-stu-id="407a5-134">DaRT 8.1 is available in the following languages:</span></span>

-   <span data-ttu-id="407a5-135">Inglês (Estados Unidos) en-US</span><span class="sxs-lookup"><span data-stu-id="407a5-135">English (United States) en-US</span></span>

-   <span data-ttu-id="407a5-136">Francês (França) fr-FR</span><span class="sxs-lookup"><span data-stu-id="407a5-136">French (France) fr-FR</span></span>

-   <span data-ttu-id="407a5-137">Italiano (Itália) it-IT</span><span class="sxs-lookup"><span data-stu-id="407a5-137">Italian (Italy) it-IT</span></span>

-   <span data-ttu-id="407a5-138">Alemão (Alemanha) de-DE</span><span class="sxs-lookup"><span data-stu-id="407a5-138">German (Germany) de-DE</span></span>

-   <span data-ttu-id="407a5-139">Espanhol, classificação internacional (Espanha) es-ES</span><span class="sxs-lookup"><span data-stu-id="407a5-139">Spanish, International Sort (Spain) es-ES</span></span>

-   <span data-ttu-id="407a5-140">Coreano (Coréia) ko-KR</span><span class="sxs-lookup"><span data-stu-id="407a5-140">Korean (Korea) ko-KR</span></span>

-   <span data-ttu-id="407a5-141">Japonês (Japão) ja-JP</span><span class="sxs-lookup"><span data-stu-id="407a5-141">Japanese (Japan) ja-JP</span></span>

-   <span data-ttu-id="407a5-142">Português (Brasil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="407a5-142">Portuguese (Brazil) pt-BR</span></span>

-   <span data-ttu-id="407a5-143">Russo (Rússia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="407a5-143">Russian (Russia) ru-RU</span></span>

-   <span data-ttu-id="407a5-144">Chinês tradicional zh-TW</span><span class="sxs-lookup"><span data-stu-id="407a5-144">Chinese Traditional zh-TW</span></span>

-   <span data-ttu-id="407a5-145">Chinês simplificado zh-CN</span><span class="sxs-lookup"><span data-stu-id="407a5-145">Chinese Simplified zh-CN</span></span>

## <span data-ttu-id="407a5-146">Como obter tecnologias do MDOP</span><span class="sxs-lookup"><span data-stu-id="407a5-146">How to Get MDOP Technologies</span></span>


<span data-ttu-id="407a5-147">O DaRT 8,1 é parte do Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="407a5-147">DaRT 8.1 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="407a5-148">O MDOP faz parte do Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="407a5-148">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="407a5-149">Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte [como obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="407a5-149">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="407a5-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="407a5-150">Related topics</span></span>


[<span data-ttu-id="407a5-151">Notas de versão do DaRT 8.1</span><span class="sxs-lookup"><span data-stu-id="407a5-151">Release Notes for DaRT 8.1</span></span>](release-notes-for-dart-81.md)









