---
title: Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.0 para um usuário específico
description: Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.0 para um usuário específico
ms.assetid: dad25992-3c75-4b7d-b4c6-c2edf43baaea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: a17d9dad11092a4c8356983b70bea3c18da1be04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796359"
---
# <span data-ttu-id="fd2e7-103">Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.0 para um usuário específico</span><span class="sxs-lookup"><span data-stu-id="fd2e7-103">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User</span></span>

<span data-ttu-id="fd2e7-104">*Observação:*\* App-V 4,6 saiu do suporte básico.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="fd2e7-105">Use o procedimento a seguir para migrar os pacotes criados com o App-V usando o arquivo de configuração do usuário.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-105">Use the following procedure to migrate packages created with App-V using the user configuration file.</span></span>

**<span data-ttu-id="fd2e7-106">Para converter um pacote</span><span class="sxs-lookup"><span data-stu-id="fd2e7-106">To convert a package</span></span>**

1. <span data-ttu-id="fd2e7-107">Localize o arquivo de configuração do usuário para o pacote que você deseja converter.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-107">Locate the user configuration file for the package you want to convert.</span></span> <span data-ttu-id="fd2e7-108">Para definir a política, execute as seguintes atualizações na seção **userconfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PACKAGEname = &lt; ID &gt; do pacote**.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-108">To set the policy, perform the following updates in the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName=&lt;Package ID&gt;**.</span></span>

   <span data-ttu-id="fd2e7-109">Veja a seguir um exemplo de um arquivo de configuração do usuário:</span><span class="sxs-lookup"><span data-stu-id="fd2e7-109">The following is an example of a user configuration file:</span></span>

   <span data-ttu-id="fd2e7-110">&lt;? XML Version = "1.0"?&gt;</span><span class="sxs-lookup"><span data-stu-id="fd2e7-110">&lt;?xml version="1.0" ?&gt;</span></span>

   <span data-ttu-id="fd2e7-111">&lt;Userconfiguration PackageID = &lt; ID &gt; do pacote DisplayName = &lt; nome do pacote&gt;</span><span class="sxs-lookup"><span data-stu-id="fd2e7-111">&lt;UserConfiguration PackageId=&lt;Package ID&gt; DisplayName=&lt;Name of the Package&gt;</span></span>

   <span data-ttu-id="fd2e7-112">xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "true"</span><span class="sxs-lookup"><span data-stu-id="fd2e7-112">xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>; &lt;ManagingAuthority TakeoverExtensionPointsFrom46="true"</span></span>

   <span data-ttu-id="fd2e7-113">PackageName = &lt; ID do pacote&gt;</span><span class="sxs-lookup"><span data-stu-id="fd2e7-113">PackageName=&lt;Package ID&gt;</span></span>

   <span data-ttu-id="fd2e7-114">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="fd2e7-114">&lt;/UserConfiguration&gt;</span></span>

2. <span data-ttu-id="fd2e7-115">Para adicionar o tipo de pacote App-V 5,0 o seguinte em um prompt de comando elevado do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="fd2e7-115">To add the App-V 5.0 package type the following in an elevated PowerShell command prompt:</span></span>

   <span data-ttu-id="fd2e7-116">PS &gt; **$pkg = Add-AppvClientPackage –** caminho caminho &lt; para o local do pacote&gt;</span><span class="sxs-lookup"><span data-stu-id="fd2e7-116">PS&gt;**$pkg= Add-AppvClientPackage –Path** &lt;Path to package location&gt;</span></span>

   <span data-ttu-id="fd2e7-117">&gt;**Public Publish-AppVClientPackage $pkg-DynamicUserConfiguration** &lt; caminho para o arquivo de configuração do usuário&gt;</span><span class="sxs-lookup"><span data-stu-id="fd2e7-117">PS&gt;**Publish-AppVClientPackage $pkg -DynamicUserConfiguration** &lt;Path to the user configuration file&gt;</span></span>

3. <span data-ttu-id="fd2e7-118">Abra o aplicativo usando FTAs ou atalhos agora.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-118">Open the application using FTAs or shortcuts now.</span></span> <span data-ttu-id="fd2e7-119">O aplicativo deve ser aberto usando o App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-119">The application should open using App-V 5.0.</span></span>

   <span data-ttu-id="fd2e7-120">O pacote App-V SP2 e o pacote App-V 5,0 convertido são publicados no usuário, mas o FTAs e os atalhos para os aplicativos foram assumidos pelo pacote App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-120">The App-V SP2 package and the converted App-V 5.0 package are published to the user, but the FTAs and shortcuts for the applications have been assumed by the App-V 5.0 package.</span></span>

   <span data-ttu-id="fd2e7-121">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="fd2e7-121">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="fd2e7-122">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="fd2e7-122">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="fd2e7-123">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="fd2e7-123">Got an App-V issue?</span></span>** <span data-ttu-id="fd2e7-124">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="fd2e7-124">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="fd2e7-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd2e7-125">Related topics</span></span>


[<span data-ttu-id="fd2e7-126">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="fd2e7-126">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





