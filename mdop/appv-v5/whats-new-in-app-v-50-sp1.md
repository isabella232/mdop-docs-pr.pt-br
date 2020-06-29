---
title: Quais são as novidades no App-V 5.0 SP1
description: Quais são as novidades no App-V 5.0 SP1
author: dansimp
ms.assetid: e97c2dbb-7b40-46a0-8137-9ee4fc2bd071
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2542d0cc5a544d26b3279b24063cf3ef428b9f39
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796194"
---
# <span data-ttu-id="e3045-103">Quais são as novidades no App-V 5.0 SP1</span><span class="sxs-lookup"><span data-stu-id="e3045-103">What's new in App-V 5.0 SP1</span></span>


<span data-ttu-id="e3045-104">Esta seção é para os usuários que já estão familiarizados com o App-V e querem saber o que mudou no App-V 5,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="e3045-104">This section is for users who are already familiar with App-V and want to know what has changed in App-V 5.0 SP1.</span></span> <span data-ttu-id="e3045-105">Se você ainda não estiver familiarizado com o App-V, comece lendo planejando o [app-v 5,0](planning-for-app-v-50-rc.md).</span><span class="sxs-lookup"><span data-stu-id="e3045-105">If you are not already familiar with App-V, you should start by reading [Planning for App-V 5.0](planning-for-app-v-50-rc.md).</span></span>

## <span data-ttu-id="e3045-106">Alterações na funcionalidade padrão</span><span class="sxs-lookup"><span data-stu-id="e3045-106">Changes in Standard Functionality</span></span>


<span data-ttu-id="e3045-107">As seções a seguir contêm informações sobre as alterações na funcionalidade padrão do App-V 5,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="e3045-107">The following sections contain information about the changes in standard functionality for App-V 5.0 SP1.</span></span>

### <span data-ttu-id="e3045-108">Alterações em idiomas com suporte</span><span class="sxs-lookup"><span data-stu-id="e3045-108">Changes to Supported Languages</span></span>

<span data-ttu-id="e3045-109">Para obter mais informações, consulte [sobre o App-V 5,0 SP1](about-app-v-50-sp1.md).</span><span class="sxs-lookup"><span data-stu-id="e3045-109">For more information, see [About App-V 5.0 SP1](about-app-v-50-sp1.md).</span></span>

<span data-ttu-id="e3045-110">A lista a seguir contém mais informações sobre os novos pacotes de idiomas:</span><span class="sxs-lookup"><span data-stu-id="e3045-110">The following list contains more information about the new Language Packs:</span></span>

-   <span data-ttu-id="e3045-111">Os pacotes de idiomas do App-V 5.0 SP1 são incluídos no instalador **appv\_xxx\_setup.exe** para todos os componentes do App-v 5,0.</span><span class="sxs-lookup"><span data-stu-id="e3045-111">The App-V 5.0SP1 language packs are bundled into the **appv\_xxx\_setup.exe** installer for all the App-V 5.0 Components.</span></span>

-   <span data-ttu-id="e3045-112">Quando você executar o instalador, ele instalará automaticamente o pacote de idiomas mais apropriado com base na localidade do sistema operacional associado em execução no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="e3045-112">When you run the installer it will automatically install the most appropriate language pack based on the locale of the associated operating system running on the target computer.</span></span>

-   <span data-ttu-id="e3045-113">Se forem necessários pacotes de idiomas adicionais, você deverá extrair esses pacotes de idiomas do instalador executando o seguinte `appv_xxx_setup.exe /Layout /LayoutDir=”<path>”` comando:</span><span class="sxs-lookup"><span data-stu-id="e3045-113">If additional language packs are required, you must extract these language packs from the installer by running the following command: `appv_xxx_setup.exe /Layout /LayoutDir=”<path>”`.</span></span> <span data-ttu-id="e3045-114">Depois que isso tiver sido executado, o conteúdo do instalador será extraído para o local especificado.</span><span class="sxs-lookup"><span data-stu-id="e3045-114">After this has been run, the contents of the installer are extracted to the specified location.</span></span>

-   <span data-ttu-id="e3045-115">Você deve instalar o pacote de idiomas desejado aplicando o arquivo de instalação do pacote de idiomas apropriado.</span><span class="sxs-lookup"><span data-stu-id="e3045-115">You must install the desired language pack by applying the appropriate Language pack Windows Installation file.</span></span> <span data-ttu-id="e3045-116">Por exemplo, **appv\_hib\_LP\_jmmb\_x86.msi** ou **appv\_hib\_LP\_jmmb\_x64.msi**, onde **Hib** refere-se ao componente e **jmmb** refere-se à localidade.</span><span class="sxs-lookup"><span data-stu-id="e3045-116">For example, **appv\_hib\_LP\_jmmb\_x86.msi** or **appv\_hib\_LP\_jmmb\_x64.msi**, where **hib** refers to the component and **jmmb** refers to the locale.</span></span>

## <span data-ttu-id="e3045-117">Suporte aprimorado para o Microsoft office2010</span><span class="sxs-lookup"><span data-stu-id="e3045-117">Enhanced Support for Microsoft Office2010</span></span>


<span data-ttu-id="e3045-118">**O kit de sequenciamento do Microsoft Office 2010 para o Application Virtualization 5,0** – ajuda a oferecer aos usuários uma experiência consistente ao usar uma versão virtualizada do Microsoft office2010.</span><span class="sxs-lookup"><span data-stu-id="e3045-118">**Microsoft Office 2010 Sequencing Kit for Application Virtualization 5.0** – helps provide users with a consistent experience using a virtualized version of Microsoft Office2010.</span></span> <span data-ttu-id="e3045-119">O **Kit de sequenciamento do Microsoft office 2010 para o Application Virtualization 5,0** é usado em conjunto com o **Kit de implantação do Microsoft Office 2010 para o App-V** e também fornece o serviço de licenciamento do Microsoft office2010 necessário.</span><span class="sxs-lookup"><span data-stu-id="e3045-119">The **Microsoft Office 2010 Sequencing Kit for Application Virtualization 5.0** is used in conjunction with the **Microsoft Office 2010 Deployment Kit for App-V** and also provides the required Microsoft Office2010 licensing service.</span></span>






## <span data-ttu-id="e3045-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e3045-120">Related topics</span></span>


[<span data-ttu-id="e3045-121">Sobre o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="e3045-121">About App-V 5.0</span></span>](about-app-v-50.md)

 

 





