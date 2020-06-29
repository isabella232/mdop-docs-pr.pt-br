---
title: Como gerenciar grupos de conexão em um computador autônomo usando o Windows PowerShell
description: Como gerenciar grupos de conexão em um computador autônomo usando o Windows PowerShell
author: dansimp
ms.assetid: e1589eff-d306-40fb-a0ae-727190dafe26
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ab120f7089619fa01885d5182313dc33fc47f827
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796362"
---
# <span data-ttu-id="da0e3-103">Como gerenciar grupos de conexão em um computador autônomo usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="da0e3-103">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span>


<span data-ttu-id="da0e3-104">Um grupo de conexões App-V permite que você execute todos os aplicativos virtuais como um conjunto definido de pacotes em um único ambiente virtual.</span><span class="sxs-lookup"><span data-stu-id="da0e3-104">An App-V connection group allows you to run all the virtual applications as a defined set of packages in a single virtual environment.</span></span> <span data-ttu-id="da0e3-105">Por exemplo, você pode virtualizar um aplicativo e seus plug-ins usando pacotes separados, mas executá-los juntos em um único grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="da0e3-105">For example, you can virtualize an application and its plug-ins by using separate packages, but run them together in a single connection group.</span></span>

<span data-ttu-id="da0e3-106">Um arquivo XML de grupo de conexão define o grupo de conexão que é executado no computador em que você instalou o cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="da0e3-106">A connection group XML file defines the connection group that runs on the computer where you’ve installed the App-V client.</span></span> <span data-ttu-id="da0e3-107">Para obter informações sobre o arquivo XML do grupo de conexão e como configurá-lo, consulte [sobre o arquivo do grupo de conexão](about-the-connection-group-file51.md).</span><span class="sxs-lookup"><span data-stu-id="da0e3-107">For information about the connection group XML file and how to configure it, see [About the Connection Group File](about-the-connection-group-file51.md).</span></span>

<span data-ttu-id="da0e3-108">Este tópico explica os seguintes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="da0e3-108">This topic explains the following procedures:</span></span>

-   [<span data-ttu-id="da0e3-109">Para adicionar e publicar os pacotes do App-V no grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="da0e3-109">To add and publish the App-V packages in the connection group</span></span>](#bkmk-add-pub-pkgs-in-cg)

-   [<span data-ttu-id="da0e3-110">Para adicionar e habilitar o grupo de conexão no cliente App-V</span><span class="sxs-lookup"><span data-stu-id="da0e3-110">To add and enable the connection group on the App-V client</span></span>](#bkmk-add-enable-cg-on-clt)

-   [<span data-ttu-id="da0e3-111">Para habilitar ou desabilitar um grupo de conexões para um usuário específico</span><span class="sxs-lookup"><span data-stu-id="da0e3-111">To enable or disable a connection group for a specific user</span></span>](#bkmk-enable-cg-for-user-poshtopic)

-   [<span data-ttu-id="da0e3-112">Para permitir que somente administradores habilitem grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="da0e3-112">To allow only administrators to enable connection groups</span></span>](#bkmk-admin-only-posh-topic-cg)

<a href="" id="bkmk-add-pub-pkgs-in-cg"></a><span data-ttu-id="da0e3-113">*Para adicionar e publicar os pacotes do App-V no grupo de conexão*\*</span><span class="sxs-lookup"><span data-stu-id="da0e3-113">*To add and publish the App-V packages in the connection group*\*</span></span>

1.  <span data-ttu-id="da0e3-114">Para adicionar e publicar os pacotes do App-V 5,1 no computador que está executando o cliente App-V, digite o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="da0e3-114">To add and publish the App-V 5.1 packages to the computer running the App-V client, type the following command:</span></span>

    <span data-ttu-id="da0e3-115">Add-AppvClientPackage – path c:\\tmpstore\\quartfin.AppV | Publicar-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="da0e3-115">Add-AppvClientPackage –path c:\\tmpstore\\quartfin.appv | Publish-AppvClientPackage</span></span>

2.  <span data-ttu-id="da0e3-116">Repita a **etapa 1** deste procedimento para cada pacote no grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="da0e3-116">Repeat **step 1** of this procedure for each package in the connection group.</span></span>

<a href="" id="bkmk-add-enable-cg-on-clt"></a>**<span data-ttu-id="da0e3-117">Para adicionar e habilitar o grupo de conexão no cliente App-V</span><span class="sxs-lookup"><span data-stu-id="da0e3-117">To add and enable the connection group on the App-V client</span></span>**

1.  <span data-ttu-id="da0e3-118">Adicione o grupo de conexão digitando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="da0e3-118">Add the connection group by typing the following command:</span></span>

    <span data-ttu-id="da0e3-119">Add-AppvClientConnectionGroup – caminho c:\\tmpstore\\financ.xml</span><span class="sxs-lookup"><span data-stu-id="da0e3-119">Add-AppvClientConnectionGroup –path c:\\tmpstore\\financ.xml</span></span>

2.  <span data-ttu-id="da0e3-120">Habilite o grupo de conexão digitando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="da0e3-120">Enable the connection group by typing the following command:</span></span>

    <span data-ttu-id="da0e3-121">Enable-AppvClientConnectionGroup – nome "aplicativos financeiros"</span><span class="sxs-lookup"><span data-stu-id="da0e3-121">Enable-AppvClientConnectionGroup –name “Financial Applications”</span></span>

    <span data-ttu-id="da0e3-122">Quando qualquer aplicativo virtual que esteja nos pacotes de membros são executados no computador de destino, eles serão executados dentro do ambiente virtual do grupo de conexão e estarão disponíveis para todos os aplicativos virtuais nos outros pacotes do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="da0e3-122">When any virtual applications that are in the member packages are run on the target computer, they will run inside the connection group’s virtual environment and will be available to all the virtual applications in the other packages in the connection group.</span></span>

<a href="" id="bkmk-enable-cg-for-user-poshtopic"></a>**<span data-ttu-id="da0e3-123">Para habilitar ou desabilitar um grupo de conexões para um usuário específico</span><span class="sxs-lookup"><span data-stu-id="da0e3-123">To enable or disable a connection group for a specific user</span></span>**

1.  <span data-ttu-id="da0e3-124">Examine a descrição e os requisitos do parâmetro:</span><span class="sxs-lookup"><span data-stu-id="da0e3-124">Review the parameter description and requirements:</span></span>

    -   <span data-ttu-id="da0e3-125">O parâmetro permite que um administrador habilite ou desabilite um grupo de conexão para um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="da0e3-125">The parameter enables an administrator to enable or disable a connection group for a specific user.</span></span>

    -   <span data-ttu-id="da0e3-126">Você deve usar o pacote de hotfix do App-V 5,0 SP2 5 ou posterior para usar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="da0e3-126">You must use App-V 5.0 SP2 Hotfix Package 5 or later to use this parameter.</span></span>

    -   <span data-ttu-id="da0e3-127">Você pode executar esse cmdlet a partir da sessão de usuário ou de administrador.</span><span class="sxs-lookup"><span data-stu-id="da0e3-127">You can run this cmdlet from the user or administrator session.</span></span>

    -   <span data-ttu-id="da0e3-128">Você deve estar conectado com credenciais administrativas para usar o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="da0e3-128">You must be logged in with administrative credentials to use the parameter.</span></span>

    -   <span data-ttu-id="da0e3-129">O usuário final deve estar conectado.</span><span class="sxs-lookup"><span data-stu-id="da0e3-129">The end user must be logged in.</span></span>

    -   <span data-ttu-id="da0e3-130">Você deve fornecer o SID (identificador de segurança) do usuário final.</span><span class="sxs-lookup"><span data-stu-id="da0e3-130">You must provide the end user’s security identifier (SID).</span></span>

2.  <span data-ttu-id="da0e3-131">Use os seguintes cmdlets e adicione o parâmetro Optional **– userid** , em que **-deusers** representa o Sid (identificador de segurança) do usuário final:</span><span class="sxs-lookup"><span data-stu-id="da0e3-131">Use the following cmdlets, and add the optional **–UserSID** parameter, where **-UserSID** represents the end user’s security identifier (SID):</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="da0e3-132">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="da0e3-132">Cmdlet</span></span></th>
    <th align="left"><span data-ttu-id="da0e3-133">Exemplos</span><span class="sxs-lookup"><span data-stu-id="da0e3-133">Examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="da0e3-134">Enable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="da0e3-134">Enable-AppVClientConnectionGroup</span></span></p></td>
    <td align="left"><p><span data-ttu-id="da0e3-135">Enable-AppVClientConnectionGroup "ConnectionGroupA"-Usuáriosid S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="da0e3-135">Enable-AppVClientConnectionGroup “ConnectionGroupA” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="da0e3-136">Disable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="da0e3-136">Disable -AppVClientConnectionGroup</span></span></p></td>
    <td align="left"><p><span data-ttu-id="da0e3-137">Disable-AppVClientConnectionGroup "ConnectionGroupA"-Usuáriosid S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="da0e3-137">Disable -AppVClientConnectionGroup “ConnectionGroupA” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
    </tr>
    </tbody>
    </table>

<a href="" id="bkmk-admin-only-posh-topic-cg"></a>**<span data-ttu-id="da0e3-138">Para permitir que somente administradores habilitem grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="da0e3-138">To allow only administrators to enable connection groups</span></span>**

1.  <span data-ttu-id="da0e3-139">Examine a descrição e a necessidade de usar este cmdlet:</span><span class="sxs-lookup"><span data-stu-id="da0e3-139">Review the description and requirement for using this cmdlet:</span></span>

    -   <span data-ttu-id="da0e3-140">Use este cmdlet e parâmetro para configurar o cliente App-V para permitir que somente administradores (não usuários finais) habilitem ou desabilitem grupos de conexão.</span><span class="sxs-lookup"><span data-stu-id="da0e3-140">Use this cmdlet and parameter to configure the App-V client to allow only administrators (not end users) to enable or disable connection groups.</span></span>

    -   <span data-ttu-id="da0e3-141">Você deve estar usando pelo menos o App-V 5,0 SP3 para usar este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da0e3-141">You must be using at least App-V 5.0 SP3 to use this cmdlet.</span></span>

2.  <span data-ttu-id="da0e3-142">Execute o seguinte cmdlet e parâmetro:</span><span class="sxs-lookup"><span data-stu-id="da0e3-142">Run the following cmdlet and parameter:</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="da0e3-143">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="da0e3-143">Cmdlet</span></span></th>
    <th align="left"><span data-ttu-id="da0e3-144">Parâmetro e valores</span><span class="sxs-lookup"><span data-stu-id="da0e3-144">Parameter and values</span></span></th>
    <th align="left"><span data-ttu-id="da0e3-145">Exemplo</span><span class="sxs-lookup"><span data-stu-id="da0e3-145">Example</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="da0e3-146">Set-AppvClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="da0e3-146">Set-AppvClientConfiguration</span></span></p></td>
    <td align="left"><p><span data-ttu-id="da0e3-147">–RequirePublishAsAdmin</span><span class="sxs-lookup"><span data-stu-id="da0e3-147">–RequirePublishAsAdmin</span></span></p>
    <ul>
    <li><p><span data-ttu-id="da0e3-148">0-falso</span><span class="sxs-lookup"><span data-stu-id="da0e3-148">0 - False</span></span></p></li>
    <li><p><span data-ttu-id="da0e3-149">1-verdadeiro</span><span class="sxs-lookup"><span data-stu-id="da0e3-149">1 - True</span></span></p></li>
    </ul></td>
    <td align="left"><p><span data-ttu-id="da0e3-150">Set-AppvClientConfiguration – RequirePublishAsAdmin1</span><span class="sxs-lookup"><span data-stu-id="da0e3-150">Set-AppvClientConfiguration –RequirePublishAsAdmin1</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="da0e3-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="da0e3-151">Related topics</span></span>


[<span data-ttu-id="da0e3-152">Operações para o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="da0e3-152">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="da0e3-153">Administração do App-V 5.1 usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="da0e3-153">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)









