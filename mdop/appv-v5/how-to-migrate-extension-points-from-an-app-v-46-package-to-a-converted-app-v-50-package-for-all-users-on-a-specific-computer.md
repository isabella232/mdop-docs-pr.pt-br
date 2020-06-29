---
title: Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.0 convertido para todos os usuários em um computador específico
description: Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.0 convertido para todos os usuários em um computador específico
ms.assetid: 3ae9996f-71d9-4ca1-9aab-25b599158e55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 3c53104907448edeb894cf4eb9dbb0a24d3229e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796361"
---
# <span data-ttu-id="c2c89-103">Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.0 convertido para todos os usuários em um computador específico</span><span class="sxs-lookup"><span data-stu-id="c2c89-103">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer</span></span>

<span data-ttu-id="c2c89-104">**Observação:** O App-V 4,6 tem saído do suporte básico.</span><span class="sxs-lookup"><span data-stu-id="c2c89-104">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="c2c89-105">Use o procedimento a seguir para migrar os pontos de extensão de um pacote App-V 4.6 para um pacote App-V 5,0 usando o arquivo de configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="c2c89-105">Use the following procedure to migrate extension points from an App-V4.6package to a App-V 5.0 package using the deployment configuration file.</span></span>

<span data-ttu-id="c2c89-106">**Observação**  O procedimento a seguir não requer um servidor de gerenciamento do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c2c89-106">**Note** The following procedure does not require an App-V 5.0 management server.</span></span>

 

**<span data-ttu-id="c2c89-107">Para migrar os pontos de extensão de um pacote de um pacote App-V 4.6 para um pacote App-V 5,0 convertido usando o arquivo de configuração de implantação</span><span class="sxs-lookup"><span data-stu-id="c2c89-107">To migrate extension points from a package from an App-V4.6 package to a converted App-V 5.0 package using the deployment configuration file</span></span>**

1. <span data-ttu-id="c2c89-108">Localize o diretório que contém o arquivo de configuração de implantação do pacote que você deseja migrar.</span><span class="sxs-lookup"><span data-stu-id="c2c89-108">Locate the directory that contains the deployment configuration file for the package you want to migrate.</span></span> <span data-ttu-id="c2c89-109">Para definir a política, faça a seguinte atualização para a seção **userconfiguration** :</span><span class="sxs-lookup"><span data-stu-id="c2c89-109">To set the policy, make the following update to the **userConfiguration** section:</span></span>

   **<span data-ttu-id="c2c89-110">ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; ID do pacote&gt;</span><span class="sxs-lookup"><span data-stu-id="c2c89-110">ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName=&lt;Package ID&gt;</span></span>**

   <span data-ttu-id="c2c89-111">Veja a seguir um exemplo de conteúdo de um arquivo de configuração de implantação:</span><span class="sxs-lookup"><span data-stu-id="c2c89-111">The following is an example of content from a deployment configuration file:</span></span>

   <span data-ttu-id="c2c89-112">&lt;? XML Version = "1.0"?&gt;</span><span class="sxs-lookup"><span data-stu-id="c2c89-112">&lt;?xml version="1.0" ?&gt;</span></span>

   <span data-ttu-id="c2c89-113">&lt;DeploymentConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2c89-113">&lt;DeploymentConfiguration</span></span>

   <span data-ttu-id="c2c89-114">xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration> " PackageID = &lt; ID do pacote &gt; DisplayName = &lt; Display Name&gt;</span><span class="sxs-lookup"><span data-stu-id="c2c89-114">xmlns="<https://schemas.microsoft.com/appv/2010/deploymentconfiguration>" PackageId=&lt;Package ID&gt; DisplayName=&lt;Display Name&gt;</span></span>

   <span data-ttu-id="c2c89-115">&lt;MachineConfiguration/&gt;</span><span class="sxs-lookup"><span data-stu-id="c2c89-115">&lt;MachineConfiguration/&gt;</span></span>

   <span data-ttu-id="c2c89-116">&lt;Userconfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="c2c89-116">&lt;UserConfiguration&gt;</span></span>

   <span data-ttu-id="c2c89-117">&lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true"</span><span class="sxs-lookup"><span data-stu-id="c2c89-117">&lt;ManagingAuthority TakeoverExtensionPointsFrom46="true"</span></span>

   <span data-ttu-id="c2c89-118">PackageName = &lt; ID do pacote&gt;</span><span class="sxs-lookup"><span data-stu-id="c2c89-118">PackageName=&lt;Package ID&gt;</span></span>

   <span data-ttu-id="c2c89-119">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="c2c89-119">&lt;/UserConfiguration&gt;</span></span>

   <span data-ttu-id="c2c89-120">&lt;/DeploymentConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="c2c89-120">&lt;/DeploymentConfiguration&gt;</span></span>

2. <span data-ttu-id="c2c89-121">Para adicionar o pacote App-V 5,0 em um prompt de comando do PowerShell com privilégios elevados, digite:</span><span class="sxs-lookup"><span data-stu-id="c2c89-121">To add the App-V 5.0 package, in an elevated PowerShell command prompt type:</span></span>

   <span data-ttu-id="c2c89-122">PS &gt; **$pkg = Add-AppvClientPackage** **–** caminho caminho &lt; para o local &gt;  - do pacote**DynamicDeploymentConfiguration** &lt; caminho para o arquivo de configuração de implantação&gt;</span><span class="sxs-lookup"><span data-stu-id="c2c89-122">PS&gt;**$pkg= Add-AppvClientPackage** **–Path** &lt;Path to package location&gt; -**DynamicDeploymentConfiguration** &lt;Path to the deployment configuration file&gt;</span></span>

   <span data-ttu-id="c2c89-123">&gt;**$Pkg de publicação PS-AppVClientPackage**</span><span class="sxs-lookup"><span data-stu-id="c2c89-123">PS&gt;**Publish-AppVClientPackage $pkg**</span></span>

3. <span data-ttu-id="c2c89-124">Para testar a migração, abra o aplicativo virtual usando o FTAs ou atalhos associados.</span><span class="sxs-lookup"><span data-stu-id="c2c89-124">To test the migration, open the virtual application using associated FTAs or shortcuts.</span></span> <span data-ttu-id="c2c89-125">O aplicativo é aberto com o App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c2c89-125">The application opens with App-V 5.0.</span></span> <span data-ttu-id="c2c89-126">Ambos, o pacote App-V 4,6 e o pacote App-V 5,0 convertido são publicados no usuário, mas o FTAs e os atalhos para os aplicativos foram considerados pelo pacote App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c2c89-126">Both, the App-V 4.6 package and the converted App-V 5.0 package are published to the user, but the FTAs and shortcuts for the applications have been assumed by the App-V 5.0 package.</span></span>

   <span data-ttu-id="c2c89-127">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="c2c89-127">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="c2c89-128">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="c2c89-128">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="c2c89-129">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="c2c89-129">Got an App-V issue?</span></span>** <span data-ttu-id="c2c89-130">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="c2c89-130">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="c2c89-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2c89-131">Related topics</span></span>


[<span data-ttu-id="c2c89-132">Como reverter pontos de extensão de um pacote do App-V 5.0 para um pacote do App-V 4.6 para todos os usuários em um computador específico</span><span class="sxs-lookup"><span data-stu-id="c2c89-132">How to Revert Extension Points from an App-V 5.0 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="c2c89-133">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="c2c89-133">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





