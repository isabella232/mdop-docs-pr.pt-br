---
title: PUBLISH PACKAGE
description: PUBLISH PACKAGE
author: dansimp
ms.assetid: a33e72dd-194f-4283-8e99-4584ab13de53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00b63389986f495d9405939245a50575bae453f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796800"
---
# <span data-ttu-id="877ab-103">PUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="877ab-103">PUBLISH PACKAGE</span></span>


<span data-ttu-id="877ab-104">Publica o conteúdo de um pacote inteiro.</span><span class="sxs-lookup"><span data-stu-id="877ab-104">Publishes the contents of an entire package.</span></span>

`SFTMIME PUBLISH PACKAGE:package-name /MANIFEST manifest-path [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="877ab-105">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="877ab-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="877ab-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="877ab-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="877ab-107">PACKAGE: &lt; Package-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="877ab-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="877ab-108">Nome de usuário e de usuário visível para o pacote.</span><span class="sxs-lookup"><span data-stu-id="877ab-108">User-visible and user-friendly name for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="877ab-109">&lt;Manifesto/manifest-caminho&gt;</span><span class="sxs-lookup"><span data-stu-id="877ab-109">/MANIFEST &lt;manifest-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="877ab-110">O caminho ou a URL do arquivo de manifesto que lista os aplicativos incluídos no pacote e todas as informações de publicação deles.</span><span class="sxs-lookup"><span data-stu-id="877ab-110">The path or URL of the manifest file that lists the applications included in the package and all of their publishing information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="877ab-111">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="877ab-111">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="877ab-112">Se estiver presente, o pacote estará disponível para todos os usuários neste computador.</span><span class="sxs-lookup"><span data-stu-id="877ab-112">If present, the package will be available for all users on this computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="877ab-113">/LOG</span><span class="sxs-lookup"><span data-stu-id="877ab-113">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="877ab-114">Se especificado, a saída será registrada no nome do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="877ab-114">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="877ab-115">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="877ab-115">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="877ab-116">Se especificado, a saída será apresentada na janela ativa do console (padrão).</span><span class="sxs-lookup"><span data-stu-id="877ab-116">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="877ab-117">/GUI</span><span class="sxs-lookup"><span data-stu-id="877ab-117">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="877ab-118">Se especificado, a saída será apresentada em uma caixa de diálogo do Windows.</span><span class="sxs-lookup"><span data-stu-id="877ab-118">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="877ab-119">Para a versão 4.6, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="877ab-119">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="877ab-120">/LOGU</span><span class="sxs-lookup"><span data-stu-id="877ab-120">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="877ab-121">Se especificado, a saída será registrada no nome do caminho especificado no formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="877ab-121">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="877ab-122">**Importante**  O pacote já deve ter sido adicionado ao cliente do Application Virtualization e o arquivo de manifesto é necessário.</span><span class="sxs-lookup"><span data-stu-id="877ab-122">**Important** The package must already have been added to the Application Virtualization Client, and the manifest file is required.</span></span>

<span data-ttu-id="877ab-123">Para usar o parâmetro **global** , o comando publicar pacote deve ser executado como administrador local; caso contrário, somente as permissões **ManageTypes** e **PublishShortcut** são necessárias.</span><span class="sxs-lookup"><span data-stu-id="877ab-123">To use the **GLOBAL** parameter, the PUBLISH PACKAGE command must be run as local Administrator; otherwise, only **ManageTypes** and **PublishShortcut** permissions are needed.</span></span>

<span data-ttu-id="877ab-124">Publicar sem o parâmetro **global** concede ao usuário acesso aos aplicativos no pacote e publica os tipos de arquivo e atalhos listados no manifesto para o perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="877ab-124">Publishing without the **GLOBAL** parameter grants the user access to the applications in the package and publishes the file types and shortcuts listed in the manifest to the user’s profile.</span></span>

<span data-ttu-id="877ab-125">A publicação com o parâmetro **global** adiciona os tipos de arquivo e atalhos listados no manifesto ao perfil "todos os usuários".</span><span class="sxs-lookup"><span data-stu-id="877ab-125">Publishing with the **GLOBAL** parameter adds the file types and shortcuts listed in the manifest to the “All Users” profile.</span></span>

<span data-ttu-id="877ab-126">Se o pacote não for global antes de a chamada e o parâmetro **global** ser usado, o pacote será tornado global e estará disponível para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="877ab-126">If the package is not global before the call and the **GLOBAL** parameter is used, the package is made global and available to all users.</span></span>

 

## <span data-ttu-id="877ab-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="877ab-127">Related topics</span></span>


[<span data-ttu-id="877ab-128">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="877ab-128">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





