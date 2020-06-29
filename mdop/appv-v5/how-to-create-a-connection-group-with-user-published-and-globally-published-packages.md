---
title: Como criar um grupo de conexão com pacotes publicados pelo usuário e globalmente publicados
description: Como criar um grupo de conexão com pacotes publicados pelo usuário e globalmente publicados
author: dansimp
ms.assetid: 82f7ea7f-7b14-4506-8940-fdcd6c3e117f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: c98981180133881909db17d19cb42771f94bd66a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796478"
---
# <span data-ttu-id="416dd-103">Como criar um grupo de conexão com pacotes publicados pelo usuário e globalmente publicados</span><span class="sxs-lookup"><span data-stu-id="416dd-103">How to Create a Connection Group with User-Published and Globally Published Packages</span></span>
<span data-ttu-id="416dd-104">Você pode criar grupos de conexão intitulados pelo usuário que contenham pacotes publicados pelo usuário e publicados globalmente, usando um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="416dd-104">You can create user-entitled connection groups that contain both user-published and globally published packages, using either of the following methods:</span></span>

-   [<span data-ttu-id="416dd-105">Como usar cmdlets do PowerShell para criar grupos de conexão qualificados pelo usuário</span><span class="sxs-lookup"><span data-stu-id="416dd-105">How to use PowerShell cmdlets to create the user-entitled connection groups</span></span>](#bkmk-posh-userentitled-cg)

-   [<span data-ttu-id="416dd-106">Como usar o servidor do App-V para criar grupos de conexão qualificados pelo usuário</span><span class="sxs-lookup"><span data-stu-id="416dd-106">How to use the App-V Server to create the user-entitled connection groups</span></span>](#bkmk-appvserver-userentitled-cg)

**<span data-ttu-id="416dd-107">O que saber antes de começar:</span><span class="sxs-lookup"><span data-stu-id="416dd-107">What to know before you start:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="416dd-108">Cenários sem suporte e possíveis problemas</span><span class="sxs-lookup"><span data-stu-id="416dd-108">Unsupported scenarios and potential issues</span></span></th>
<th align="left"><span data-ttu-id="416dd-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="416dd-109">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="416dd-110">Você não pode incluir pacotes publicados pelo usuário em grupos de conexão habilitados globalmente.</span><span class="sxs-lookup"><span data-stu-id="416dd-110">You cannot include user-published packages in globally entitled connection groups.</span></span></p></td>
<td align="left"><p><span data-ttu-id="416dd-111">O grupo de conexão falhará.</span><span class="sxs-lookup"><span data-stu-id="416dd-111">The connection group will fail.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="416dd-112">Se você publicar um pacote globalmente e, em seguida, criar um grupo de conexões publicada pelo usuário no qual você fez esse pacote não opcional, ainda poderá executar <strong> &lt; o AppvClientPackage Package &gt; -global </strong> para cancelar a publicação do pacote, mesmo quando esse pacote estiver sendo usado em outro grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="416dd-112">If you publish a package globally and then create a user-published connection group in which you’ve made that package non-optional, you can still run <strong>Unpublish-AppvClientPackage &lt;package&gt; -global</strong> to unpublish the package, even when that package is being used in another connection group.</span></span></p></td>
<td align="left"><p><span data-ttu-id="416dd-113">Se qualquer outro grupo de conexão estiver usando esse pacote, o pacote irá falhar nesses grupos de conexão.</span><span class="sxs-lookup"><span data-stu-id="416dd-113">If any other connection groups are using that package, the package will fail in those connection groups.</span></span></p>
<p><span data-ttu-id="416dd-114">Para evitar a publicação inadvertida de um pacote não opcional que está sendo usado em outro grupo de conexão, recomendamos que você acompanhe os grupos de conexão em que usou um pacote não opcional.</span><span class="sxs-lookup"><span data-stu-id="416dd-114">To avoid inadvertently unpublishing a non-optional package that is being used in another connection group, we recommend that you track the connection groups in which you’ve used a non-optional package.</span></span></p></td>
</tr>
</tbody>
</table>

 
<a href="" id="bkmk-posh-userentitled-cg"></a>**<span data-ttu-id="416dd-115">Como usar cmdlets do PowerShell para criar grupos de conexão intitulados pelo usuário</span><span class="sxs-lookup"><span data-stu-id="416dd-115">How to use PowerShell cmdlets to create user-entitled connection groups</span></span>**

1.  <span data-ttu-id="416dd-116">Para adicionar e publicar pacotes, use os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="416dd-116">Add and publish packages by using the following commands:</span></span>

    **<span data-ttu-id="416dd-117">Add-AppvClientPackage package1 \ _AppV \ _file \ _Path</span><span class="sxs-lookup"><span data-stu-id="416dd-117">Add-AppvClientPackage Package1\_AppV\_file\_Path</span></span>**

    **<span data-ttu-id="416dd-118">Add-AppvClientPackage Package2 \ _AppV \ _file \ _Path</span><span class="sxs-lookup"><span data-stu-id="416dd-118">Add-AppvClientPackage Package2\_AppV\_file\_Path</span></span>**

    **<span data-ttu-id="416dd-119">Publish-AppvClientPackage-PackageID package1 \ _ID-VersionId package1 \ _Version ID-global</span><span class="sxs-lookup"><span data-stu-id="416dd-119">Publish-AppvClientPackage -PackageId Package1\_ID-VersionId Package1\_Version ID -Global</span></span>**

    **<span data-ttu-id="416dd-120">Publish-AppvClientPackage-PackageID Package2 \ _ID-VersionIdPackage2-\ _ID</span><span class="sxs-lookup"><span data-stu-id="416dd-120">Publish-AppvClientPackage -PackageId Package2\_ID -VersionIdPackage2\_ID</span></span>**

2.  <span data-ttu-id="416dd-121">Crie o arquivo XML do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="416dd-121">Create the connection group XML file.</span></span> <span data-ttu-id="416dd-122">Para obter mais informações, consulte [sobre o arquivo de grupo de conexão](about-the-connection-group-file.md).</span><span class="sxs-lookup"><span data-stu-id="416dd-122">For more information, see [About the Connection Group File](about-the-connection-group-file.md).</span></span>

3.  <span data-ttu-id="416dd-123">Adicione e publique o grupo de conexão usando os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="416dd-123">Add and publish the connection group by using the following commands:</span></span>

    **<span data-ttu-id="416dd-124">Conexão Add-AppvClientConnectionGroup \ _Group \ _XML \ _file \ _Path</span><span class="sxs-lookup"><span data-stu-id="416dd-124">Add-AppvClientConnectionGroup Connection\_Group\_XML\_file\_Path</span></span>**

    **<span data-ttu-id="416dd-125">Enable-AppvClientConnectionGroup-GroupId CG \ _Group \ _ID-VersionId CG \ _Version \ _ID</span><span class="sxs-lookup"><span data-stu-id="416dd-125">Enable-AppvClientConnectionGroup -GroupId CG\_Group\_ID-VersionId CG\_Version\_ID</span></span>**

<a href="" id="bkmk-appvserver-userentitled-cg"></a>**<span data-ttu-id="416dd-126">Como usar o servidor do App-V para criar grupos de conexão intitulados pelo usuário</span><span class="sxs-lookup"><span data-stu-id="416dd-126">How to use the App-V Server to create user-entitled connection groups</span></span>**

1.  <span data-ttu-id="416dd-127">Abra o console de gerenciamento do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="416dd-127">Open the App-V 5.0 Management Console.</span></span>

2.  <span data-ttu-id="416dd-128">Siga as instruções em [como publicar um pacote usando o console de gerenciamento](how-to-publish-a-package-by-using-the-management-console-50.md) para publicar pacotes globalmente e para o usuário.</span><span class="sxs-lookup"><span data-stu-id="416dd-128">Follow the instructions in [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md) to publish packages globally and to the user.</span></span>

3.  <span data-ttu-id="416dd-129">Siga as instruções em [como criar um grupo de conexão](how-to-create-a-connection-group.md) para criar o grupo de conexões e adicionar os pacotes publicados pelo usuário e publicados globalmente.</span><span class="sxs-lookup"><span data-stu-id="416dd-129">Follow the instructions in [How to Create a Connection Group](how-to-create-a-connection-group.md) to create the connection group, and add the user-published and globally published packages.</span></span>

    <span data-ttu-id="416dd-130">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="416dd-130">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="416dd-131">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="416dd-131">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="416dd-132">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="416dd-132">Got an App-V issue?</span></span>** <span data-ttu-id="416dd-133">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="416dd-133">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="416dd-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="416dd-134">Related topics</span></span>


[<span data-ttu-id="416dd-135">Gerenciando grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="416dd-135">Managing Connection Groups</span></span>](managing-connection-groups.md)

[<span data-ttu-id="416dd-136">Como usar pacotes opcionais em grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="416dd-136">How to Use Optional Packages in Connection Groups</span></span>](how-to-use-optional-packages-in-connection-groups.md)

 

 





