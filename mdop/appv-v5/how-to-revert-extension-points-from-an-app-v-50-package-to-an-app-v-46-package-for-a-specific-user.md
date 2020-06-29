---
ms.reviewer: ''
title: Como reverter pontos de extensão de um pacote do App-V 5.0 para um pacote do App-V 4.6 para um usuário específico
description: Como reverter pontos de extensão de um pacote do App-V 5.0 para um pacote do App-V 4.6 para um usuário específico
ms.assetid: f1d2ab1f-0831-4976-b49f-169511d3382a
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 2a0660024734806c508043cc2db030c96cfd16a2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796325"
---
# <span data-ttu-id="79be6-103">Como reverter pontos de extensão de um pacote do App-V 5.0 para um pacote do App-V 4.6 para um usuário específico</span><span class="sxs-lookup"><span data-stu-id="79be6-103">How to Revert Extension Points From an App-V 5.0 Package to an App-V 4.6 Package for a Specific User</span></span>

<span data-ttu-id="79be6-104">*Observação:*\* App-V 4,6 saiu do suporte básico.</span><span class="sxs-lookup"><span data-stu-id="79be6-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="79be6-105">Use o procedimento a seguir para reverter um pacote App-V 5,0 para o formato de arquivo App-V usando o arquivo de configuração do usuário.</span><span class="sxs-lookup"><span data-stu-id="79be6-105">Use the following procedure to revert an App-V 5.0 package to the App-V file format using the user configuration file.</span></span>

**<span data-ttu-id="79be6-106">Para reverter um pacote</span><span class="sxs-lookup"><span data-stu-id="79be6-106">To revert a package</span></span>**

1.  <span data-ttu-id="79be6-107">Certifique-se de que o pacote App-V 4,6 seja publicado para os usuários, mas que o FTAs e os atalhos tenham sido presumidos pelo pacote do App-v 5,0 usando o método de migração a seguir, [como migrar pontos de extensão de um pacote app-v 4,6 para o app-v 5,0 para um usuário específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).</span><span class="sxs-lookup"><span data-stu-id="79be6-107">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.0 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).</span></span>

    <span data-ttu-id="79be6-108">Na seção **userconfiguration** do arquivo de configuração de implantação do pacote convertido, para definir a política, faça a seguinte atualização para a seção **Userconfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "false" PackageName = &lt; ID &gt; do pacote**</span><span class="sxs-lookup"><span data-stu-id="79be6-108">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="79be6-109">Em um prompt de comando elevado, digite:</span><span class="sxs-lookup"><span data-stu-id="79be6-109">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="79be6-110">&gt;**$Pkg de publicação PS-AppVClientPackage-DynamicUserConfigurationPath** &lt; caminho para o arquivo de configuração do usuário&gt;</span><span class="sxs-lookup"><span data-stu-id="79be6-110">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationPath** &lt;path to user configuration file&gt;</span></span>

3.  <span data-ttu-id="79be6-111">Realize uma atualização de publicação ou aguarde a próxima atualização de publicação agendada para o App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="79be6-111">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6.</span></span> <span data-ttu-id="79be6-112">Abra o aplicativo usando FTAs ou atalhos.</span><span class="sxs-lookup"><span data-stu-id="79be6-112">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="79be6-113">Agora o aplicativo deve abrir usando o App-V 4,6 SP2.</span><span class="sxs-lookup"><span data-stu-id="79be6-113">The Application should now open using App-V 4.6 SP2.</span></span>

    **<span data-ttu-id="79be6-114">Observação</span><span class="sxs-lookup"><span data-stu-id="79be6-114">Note</span></span>**  
    <span data-ttu-id="79be6-115">Se você não precisar mais do pacote App-V 5,0, poderá cancelar a publicação do pacote App-V 5,0 e os pontos de extensão serão revertidos automaticamente para o App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="79be6-115">If you do not need the App-V 5.0 package anymore, you can unpublish the App-V 5.0 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="79be6-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="79be6-116">Related topics</span></span>


[<span data-ttu-id="79be6-117">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="79be6-117">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)












