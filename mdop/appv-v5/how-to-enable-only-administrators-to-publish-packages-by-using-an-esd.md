---
title: Como permitir que apenas administradores publiquem pacotes usando ESD
description: Como permitir que apenas administradores publiquem pacotes usando ESD
author: dansimp
ms.assetid: 03367b26-83d5-4299-ad52-b9177b9cf9a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 341e86ca806c5acc736c78cf8072aab6fb4286df
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796417"
---
# <span data-ttu-id="5bfc7-103">Como permitir que apenas administradores publiquem pacotes usando ESD</span><span class="sxs-lookup"><span data-stu-id="5bfc7-103">How to Enable Only Administrators to Publish Packages by Using an ESD</span></span>


<span data-ttu-id="5bfc7-104">A partir do App-V 5,0 SP3, você pode configurar o cliente App-V para que somente administradores (não usuários finais) possam publicar ou cancelar a publicação de pacotes.</span><span class="sxs-lookup"><span data-stu-id="5bfc7-104">Starting in App-V 5.0 SP3, you can configure the App-V client so that only administrators (not end users) can publish or unpublish packages.</span></span> <span data-ttu-id="5bfc7-105">Em versões anteriores do App-V, você não pode impedir que os usuários finais executem essas tarefas.</span><span class="sxs-lookup"><span data-stu-id="5bfc7-105">In earlier versions of App-V, you could not prevent end users from performing these tasks.</span></span>

**<span data-ttu-id="5bfc7-106">Para habilitar apenas os administradores a publicar ou cancelar a publicação de pacotes</span><span class="sxs-lookup"><span data-stu-id="5bfc7-106">To enable only administrators to publish or unpublish packages</span></span>**

1.  <span data-ttu-id="5bfc7-107">Navegue até o seguinte nó de objeto de política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="5bfc7-107">Navigate to the following Group Policy Object node:</span></span>

    <span data-ttu-id="5bfc7-108">**Configuração &gt; do computador Política &gt; modelos administrativos &gt; do &gt; App-V &gt; Publishing**.</span><span class="sxs-lookup"><span data-stu-id="5bfc7-108">**Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing**.</span></span>

2.  <span data-ttu-id="5bfc7-109">Habilite a configuração de política **exigir publicação como administrador** .</span><span class="sxs-lookup"><span data-stu-id="5bfc7-109">Enable the **Require publish as administrator** Group Policy setting.</span></span>

    <span data-ttu-id="5bfc7-110">Para usar opcionalmente o PowerShell para definir esse item, consulte [como gerenciar pacotes do App-V 5,0 em execução em um computador autônomo usando o PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span><span class="sxs-lookup"><span data-stu-id="5bfc7-110">To alternatively use PowerShell to set this item, see [How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span></span>

    <span data-ttu-id="5bfc7-111">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="5bfc7-111">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="5bfc7-112">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="5bfc7-112">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="5bfc7-113">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="5bfc7-113">Got an App-V issue?</span></span>** <span data-ttu-id="5bfc7-114">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="5bfc7-114">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

 

 





