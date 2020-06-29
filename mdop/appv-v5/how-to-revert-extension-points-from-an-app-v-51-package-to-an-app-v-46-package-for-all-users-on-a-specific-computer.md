---
title: Como reverter pontos de extensão de um pacote do App-V 5.1 para um pacote do App-V 4.6 para todos os usuários em um computador específico
description: Como reverter pontos de extensão de um pacote do App-V 5.1 para um pacote do App-V 4.6 para todos os usuários em um computador específico
author: dansimp
ms.assetid: 64640b8e-de6b-4006-a33e-353d285af15e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: ce8d5cc0e79be46fd9680a3bea0236bbeb93ea83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796321"
---
# <span data-ttu-id="d3e57-103">Como reverter pontos de extensão de um pacote do App-V 5.1 para um pacote do App-V 4.6 para todos os usuários em um computador específico</span><span class="sxs-lookup"><span data-stu-id="d3e57-103">How to Revert Extension Points from an App-V 5.1 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>


<span data-ttu-id="d3e57-104">Use o procedimento a seguir para reverter os pontos de extensão de um pacote App-V 5,1 para o formato de arquivo App-V 4,6 usando o arquivo de configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="d3e57-104">Use the following procedure to revert extension points from an App-V 5.1 package to the App-V 4.6 file format using the deployment configuration file.</span></span>

**<span data-ttu-id="d3e57-105">Para reverter um pacote</span><span class="sxs-lookup"><span data-stu-id="d3e57-105">To revert a package</span></span>**

1.  <span data-ttu-id="d3e57-106">Certifique-se de que o pacote App-V 4,6 seja publicado para os usuários, mas que o FTAs e os atalhos tenham sido presumidos pelo pacote do App-v 5,1 usando o método de migração a seguir, [como migrar pontos de extensão de um pacote do App-v 4,6 para um pacote app-v 5,1 convertido para todos os usuários em um computador específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md).</span><span class="sxs-lookup"><span data-stu-id="d3e57-106">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.1 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md).</span></span>

    <span data-ttu-id="d3e57-107">Na seção **userconfiguration** do arquivo de configuração de implantação do pacote convertido, para definir a política, faça a seguinte atualização para a seção **Userconfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "false" PackageName = &lt; ID &gt; do pacote**</span><span class="sxs-lookup"><span data-stu-id="d3e57-107">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="d3e57-108">Em um prompt de comando elevado, digite:</span><span class="sxs-lookup"><span data-stu-id="d3e57-108">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="d3e57-109">PS &gt; **set-AppvClientPackage $pkg – DynamicDeploymentConfiguration** &lt; caminho para o arquivo de configuração de implantação&gt;</span><span class="sxs-lookup"><span data-stu-id="d3e57-109">PS&gt;**Set-AppvClientPackage $pkg –DynamicDeploymentConfiguration** &lt;path to deployment configuration file&gt;</span></span>

    <span data-ttu-id="d3e57-110">&gt;**$Pkg de publicação do PS-AppVClientPackage-DynamicUserConfigurationType useDeploymentConfiguration**</span><span class="sxs-lookup"><span data-stu-id="d3e57-110">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationType useDeploymentConfiguration**</span></span>

3.  <span data-ttu-id="d3e57-111">Realize uma atualização de publicação ou aguarde a próxima atualização de publicação agendada do pacote App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="d3e57-111">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6 package.</span></span>

    <span data-ttu-id="d3e57-112">Abra o aplicativo usando FTAs ou atalhos.</span><span class="sxs-lookup"><span data-stu-id="d3e57-112">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="d3e57-113">Agora o aplicativo deve abrir usando o App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="d3e57-113">The Application should now open using App-V 4.6.</span></span>

    **<span data-ttu-id="d3e57-114">Observação</span><span class="sxs-lookup"><span data-stu-id="d3e57-114">Note</span></span>**  
    <span data-ttu-id="d3e57-115">Se você não precisar mais do pacote App-V 5,1, poderá cancelar a publicação do pacote App-V 5,1 e os pontos de extensão serão revertidos automaticamente para o App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="d3e57-115">If you do not need the App-V 5.1 package anymore, you can unpublish the App-V 5.1 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="d3e57-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d3e57-116">Related topics</span></span>


[<span data-ttu-id="d3e57-117">Operações para o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="d3e57-117">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









