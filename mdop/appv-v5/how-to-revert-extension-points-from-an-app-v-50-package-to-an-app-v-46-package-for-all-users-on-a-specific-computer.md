---
title: Como reverter pontos de extensão de um pacote do App-V 5.0 para um pacote do App-V 4.6 para todos os usuários em um computador específico
description: Como reverter pontos de extensão de um pacote do App-V 5.0 para um pacote do App-V 4.6 para todos os usuários em um computador específico
ms.assetid: 2a43ca1b-6847-4dd1-ade2-336ac4ac6af0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 62542e5cd0b9dcb55f6e8f3db4d4f43c011a2839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796322"
---
# <span data-ttu-id="c1855-103">Como reverter pontos de extensão de um pacote do App-V 5.0 para um pacote do App-V 4.6 para todos os usuários em um computador específico</span><span class="sxs-lookup"><span data-stu-id="c1855-103">How to Revert Extension Points from an App-V 5.0 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>

<span data-ttu-id="c1855-104">*Observação:*\* App-V 4,6 saiu do suporte básico.</span><span class="sxs-lookup"><span data-stu-id="c1855-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span> <span data-ttu-id="c1855-105">O seguinte pressupõe que o cliente App-V 4,6 SP3 já está instalado.</span><span class="sxs-lookup"><span data-stu-id="c1855-105">The following assumes that the App-V 4.6 SP3 client is already installed.</span></span>

<span data-ttu-id="c1855-106">Use o procedimento a seguir para reverter os pontos de extensão de um pacote App-V 5,0 para o formato de arquivo App-V 4,6 usando o arquivo de configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="c1855-106">Use the following procedure to revert extension points from an App-V 5.0 package to the App-V 4.6 file format using the deployment configuration file.</span></span>

**<span data-ttu-id="c1855-107">Para reverter um pacote</span><span class="sxs-lookup"><span data-stu-id="c1855-107">To revert a package</span></span>**

1.  <span data-ttu-id="c1855-108">Certifique-se de que o pacote App-V 4,6 seja publicado para os usuários, mas que o FTAs e os atalhos tenham sido presumidos pelo pacote do App-v 5,0 usando o método de migração a seguir, [como migrar pontos de extensão de um pacote do App-v 4,6 para um pacote app-v 5,0 convertido para todos os usuários em um computador específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md).</span><span class="sxs-lookup"><span data-stu-id="c1855-108">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.0 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md).</span></span>

    <span data-ttu-id="c1855-109">Na seção **userconfiguration** do arquivo de configuração de implantação do pacote convertido, para definir a política, faça a seguinte atualização para a seção **Userconfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "false" PackageName = &lt; ID &gt; do pacote**</span><span class="sxs-lookup"><span data-stu-id="c1855-109">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="c1855-110">Em um prompt de comando elevado, digite:</span><span class="sxs-lookup"><span data-stu-id="c1855-110">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="c1855-111">PS &gt; **set-AppvClientPackage $pkg – DynamicDeploymentConfiguration** &lt; caminho para o arquivo de configuração de implantação&gt;</span><span class="sxs-lookup"><span data-stu-id="c1855-111">PS&gt;**Set-AppvClientPackage $pkg –DynamicDeploymentConfiguration** &lt;path to deployment configuration file&gt;</span></span>

    <span data-ttu-id="c1855-112">&gt;**$Pkg de publicação do PS-AppVClientPackage-DynamicUserConfigurationType useDeploymentConfiguration**</span><span class="sxs-lookup"><span data-stu-id="c1855-112">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationType useDeploymentConfiguration**</span></span>

3.  <span data-ttu-id="c1855-113">Realize uma atualização de publicação ou aguarde a próxima atualização de publicação agendada do pacote App-V 4,6 SP2.</span><span class="sxs-lookup"><span data-stu-id="c1855-113">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6 SP2 package.</span></span>

    <span data-ttu-id="c1855-114">Abra o aplicativo usando FTAs ou atalhos.</span><span class="sxs-lookup"><span data-stu-id="c1855-114">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="c1855-115">Agora o aplicativo deve abrir usando o App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="c1855-115">The Application should now open using App-V 4.6.</span></span>

    **<span data-ttu-id="c1855-116">Observação</span><span class="sxs-lookup"><span data-stu-id="c1855-116">Note</span></span>**  
    <span data-ttu-id="c1855-117">Se você não precisar mais do pacote App-V 5,0, poderá cancelar a publicação do pacote App-V 5,0 e os pontos de extensão serão revertidos automaticamente para o App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="c1855-117">If you do not need the App-V 5.0 package anymore, you can unpublish the App-V 5.0 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="c1855-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c1855-118">Related topics</span></span>


[<span data-ttu-id="c1855-119">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="c1855-119">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









