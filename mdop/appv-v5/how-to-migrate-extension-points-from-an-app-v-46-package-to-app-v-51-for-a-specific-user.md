---
title: Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.1 para um usuário específico
description: Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.1 para um usuário específico
author: dansimp
ms.assetid: 19da3776-5ebe-41e1-9890-12b84ef3c1c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: e2166b0f280153ad62709b21bb3477d0c4277fcd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796357"
---
# <span data-ttu-id="4c626-103">Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.1 para um usuário específico</span><span class="sxs-lookup"><span data-stu-id="4c626-103">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User</span></span>


<span data-ttu-id="4c626-104">Use o procedimento a seguir para migrar os pacotes criados com o App-V usando o arquivo de configuração do usuário.</span><span class="sxs-lookup"><span data-stu-id="4c626-104">Use the following procedure to migrate packages created with App-V using the user configuration file.</span></span>

<span data-ttu-id="4c626-105">**Observação**  Este procedimento pressupõe que você esteja executando a versão mais recente do App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="4c626-105">**Note** This procedure assumes that you are running the latest version of App-V 4.6.</span></span>

**<span data-ttu-id="4c626-106">Para converter um pacote</span><span class="sxs-lookup"><span data-stu-id="4c626-106">To convert a package</span></span>**

1. <span data-ttu-id="4c626-107">Localize o arquivo de configuração do usuário para o pacote que você deseja converter.</span><span class="sxs-lookup"><span data-stu-id="4c626-107">Locate the user configuration file for the package you want to convert.</span></span> <span data-ttu-id="4c626-108">Para definir a política, execute as seguintes atualizações na seção **userconfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PACKAGEname = &lt; ID &gt; do pacote**.</span><span class="sxs-lookup"><span data-stu-id="4c626-108">To set the policy, perform the following updates in the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName=&lt;Package ID&gt;**.</span></span>

   <span data-ttu-id="4c626-109">Veja a seguir um exemplo de um arquivo de configuração do usuário:</span><span class="sxs-lookup"><span data-stu-id="4c626-109">The following is an example of a user configuration file:</span></span>

   <span data-ttu-id="4c626-110">&lt;? XML Version = "1.0"?&gt;</span><span class="sxs-lookup"><span data-stu-id="4c626-110">&lt;?xml version="1.0" ?&gt;</span></span>

   <span data-ttu-id="4c626-111">&lt;Userconfiguration PackageID = &lt; ID &gt; do pacote DisplayName = &lt; nome do pacote&gt;</span><span class="sxs-lookup"><span data-stu-id="4c626-111">&lt;UserConfiguration PackageId=&lt;Package ID&gt; DisplayName=&lt;Name of the Package&gt;</span></span>

   <span data-ttu-id="4c626-112">xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "true"</span><span class="sxs-lookup"><span data-stu-id="4c626-112">xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>; &lt;ManagingAuthority TakeoverExtensionPointsFrom46="true"</span></span>

   <span data-ttu-id="4c626-113">PackageName = &lt; ID do pacote&gt;</span><span class="sxs-lookup"><span data-stu-id="4c626-113">PackageName=&lt;Package ID&gt;</span></span>

   <span data-ttu-id="4c626-114">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="4c626-114">&lt;/UserConfiguration&gt;</span></span>

2. <span data-ttu-id="4c626-115">Para adicionar o pacote App-V 5,1, digite o seguinte em uma janela do prompt de comando do PowerShell com privilégios elevados:</span><span class="sxs-lookup"><span data-stu-id="4c626-115">To add the App-V 5.1 package, type the following in an elevated PowerShell command prompt window:</span></span>

   <span data-ttu-id="4c626-116">PS &gt; **$pkg = Add-AppvClientPackage –** caminho caminho &lt; para o local do pacote&gt;</span><span class="sxs-lookup"><span data-stu-id="4c626-116">PS&gt;**$pkg= Add-AppvClientPackage –Path** &lt;Path to package location&gt;</span></span>

   <span data-ttu-id="4c626-117">&gt;**Public Publish-AppVClientPackage $pkg-DynamicUserConfiguration** &lt; caminho para o arquivo de configuração do usuário&gt;</span><span class="sxs-lookup"><span data-stu-id="4c626-117">PS&gt;**Publish-AppVClientPackage $pkg -DynamicUserConfiguration** &lt;Path to the user configuration file&gt;</span></span>

3. <span data-ttu-id="4c626-118">Abra o aplicativo usando FTAs ou atalhos agora.</span><span class="sxs-lookup"><span data-stu-id="4c626-118">Open the application using FTAs or shortcuts now.</span></span> <span data-ttu-id="4c626-119">O aplicativo deve ser aberto usando o App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4c626-119">The application should open using App-V 5.1.</span></span>

   <span data-ttu-id="4c626-120">O pacote App-V 4,6 e o pacote App-V 5,1 convertido são publicados no usuário, mas o FTAs e os atalhos para os aplicativos foram considerados pelo pacote App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="4c626-120">The App-V 4.6 package and the converted App-V 5.1 package are published to the user, but the FTAs and shortcuts for the applications have been assumed by the App-V 5.1 package.</span></span>

   <span data-ttu-id="4c626-121">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="4c626-121">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="4c626-122">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="4c626-122">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="4c626-123">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="4c626-123">Got an App-V issue?</span></span>** <span data-ttu-id="4c626-124">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="4c626-124">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="4c626-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4c626-125">Related topics</span></span>


[<span data-ttu-id="4c626-126">Operações para o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="4c626-126">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="4c626-127">Como reverter pontos de extensão de um pacote do App-V 5.1 para um pacote do App-V 4.6 para um usuário específico</span><span class="sxs-lookup"><span data-stu-id="4c626-127">How to Revert Extension Points From an App-V 5.1 Package to an App-V 4.6 Package for a Specific User</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)

 

 





