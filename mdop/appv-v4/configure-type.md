---
title: CONFIGURE TYPE
description: CONFIGURE TYPE
author: dansimp
ms.assetid: 2caf9433-5449-486f-ab94-83ee8e44d7f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b70cdd1b27eba0109183f1eb9cfb42f08b3f341
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798025"
---
# <span data-ttu-id="f78c3-103">CONFIGURE TYPE</span><span class="sxs-lookup"><span data-stu-id="f78c3-103">CONFIGURE TYPE</span></span>


<span data-ttu-id="f78c3-104">Permite que o usuário altere as configurações de uma associação de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f78c3-104">Enables the user to change settings for a file type association.</span></span>

`SFTMIME CONFIGURE TYPE:file-extension [/GLOBAL] [/APP application]                 [/ICON icon-pathname] [/DESCRIPTION type-desc]                 [/CONTENT-TYPE content-type] [/PERCEIVED-TYPE perceived-type]                 [/PROGID progid] [/CONFIRMOPEN {YES|NO}]                 [/SHOWEXT {YES|NO}] [/NEWMENU {YES|NO}]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f78c3-105">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="f78c3-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="f78c3-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f78c3-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f78c3-107">TIPO: &lt; extensão de arquivo&gt;</span><span class="sxs-lookup"><span data-stu-id="f78c3-107">TYPE:&lt;file-extension&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f78c3-108">A extensão de nome de arquivo a ser configurada.</span><span class="sxs-lookup"><span data-stu-id="f78c3-108">The file name extension to be configured.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f78c3-109">&lt;Aplicativo/App&gt;</span><span class="sxs-lookup"><span data-stu-id="f78c3-109">/APP &lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f78c3-110">O nome e a versão (opcional) do aplicativo ao qual associar esse tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f78c3-110">The name and version (optional) of the application to associate this file type with.</span></span> <span data-ttu-id="f78c3-111">Não pode ser especificado com PROGID.</span><span class="sxs-lookup"><span data-stu-id="f78c3-111">Cannot be specified with PROGID.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f78c3-112">Ícone do/ICON &lt; -PathName&gt;</span><span class="sxs-lookup"><span data-stu-id="f78c3-112">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f78c3-113">O caminho ou a URL do arquivo de ícone.</span><span class="sxs-lookup"><span data-stu-id="f78c3-113">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f78c3-114">&lt;Tipo de/Description-desc&gt;</span><span class="sxs-lookup"><span data-stu-id="f78c3-114">/DESCRIPTION &lt;type-desc&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f78c3-115">O nome amigável do tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f78c3-115">The user-friendly name for the file type.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f78c3-116">&lt;Tipo de conteúdo/Content-Type&gt;</span><span class="sxs-lookup"><span data-stu-id="f78c3-116">/CONTENT-TYPE &lt;content-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f78c3-117">O tipo de conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f78c3-117">The content type of the file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f78c3-118">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="f78c3-118">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="f78c3-119">Se presente, indica que a associação que se aplica a todos os usuários deve ser editada, não a específica do usuário.</span><span class="sxs-lookup"><span data-stu-id="f78c3-119">If present, indicates that the association that applies to all users should be edited, not the user-specific one.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f78c3-120">&lt;Tipo percebido/PERCEIVED-Type&gt;</span><span class="sxs-lookup"><span data-stu-id="f78c3-120">/PERCEIVED-TYPE &lt;perceived-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f78c3-121">O tipo percebido do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f78c3-121">The perceived type of the file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f78c3-122">&lt;ProgID/ProgId&gt;</span><span class="sxs-lookup"><span data-stu-id="f78c3-122">/PROGID &lt;progid&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f78c3-123">Indica que a extensão deve ser associada a um tipo de arquivo diferente.</span><span class="sxs-lookup"><span data-stu-id="f78c3-123">Indicates that the extension should be associated with a different file type.</span></span> <span data-ttu-id="f78c3-124">O tipo de arquivo anterior não é excluído.</span><span class="sxs-lookup"><span data-stu-id="f78c3-124">The previous file type is not deleted.</span></span> <span data-ttu-id="f78c3-125">Não pode ser especificado com APP, ICON, DESCRIPTION, CONFIRMOPEN ou SHOWEXT.</span><span class="sxs-lookup"><span data-stu-id="f78c3-125">Cannot be specified with APP, ICON, DESCRIPTION, CONFIRMOPEN, or SHOWEXT.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f78c3-126">/CONFIRMOPEN</span><span class="sxs-lookup"><span data-stu-id="f78c3-126">/CONFIRMOPEN</span></span></p></td>
<td align="left"><p><span data-ttu-id="f78c3-127">Indica se os usuários que baixam um arquivo desse tipo devem ser solicitados a abrir ou salvar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="f78c3-127">Indicates whether users downloading a file of this type should be asked whether to open or save the file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f78c3-128">/SHOWEXT</span><span class="sxs-lookup"><span data-stu-id="f78c3-128">/SHOWEXT</span></span></p></td>
<td align="left"><p><span data-ttu-id="f78c3-129">Indica se a extensão do arquivo sempre deve ser mostrada, mesmo se o usuário tiver solicitado que todas as extensões fiquem ocultas.</span><span class="sxs-lookup"><span data-stu-id="f78c3-129">Indicates whether the file's extension should always be shown, even if the user has requested that all extensions be hidden.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f78c3-130">/NEWMENU</span><span class="sxs-lookup"><span data-stu-id="f78c3-130">/NEWMENU</span></span></p></td>
<td align="left"><p><span data-ttu-id="f78c3-131">Indica se uma entrada deve ser adicionada ao <strong> menu novo do Shell </strong> .</span><span class="sxs-lookup"><span data-stu-id="f78c3-131">Indicates whether an entry should be added to the shell's <strong>New</strong> menu.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f78c3-132">/LOG</span><span class="sxs-lookup"><span data-stu-id="f78c3-132">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="f78c3-133">Se especificado, a saída será registrada no nome do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="f78c3-133">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f78c3-134">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="f78c3-134">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="f78c3-135">Se especificado, a saída será apresentada na janela ativa do console (padrão).</span><span class="sxs-lookup"><span data-stu-id="f78c3-135">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f78c3-136">/GUI</span><span class="sxs-lookup"><span data-stu-id="f78c3-136">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="f78c3-137">Se especificado, a saída será apresentada em uma caixa de diálogo do Windows.</span><span class="sxs-lookup"><span data-stu-id="f78c3-137">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f78c3-138">Para a versão 4.6, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="f78c3-138">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f78c3-139">/LOGU</span><span class="sxs-lookup"><span data-stu-id="f78c3-139">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="f78c3-140">Se especificado, a saída será registrada no nome do caminho especificado no formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="f78c3-140">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f78c3-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f78c3-141">Related topics</span></span>


[<span data-ttu-id="f78c3-142">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="f78c3-142">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





