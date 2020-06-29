---
title: ADD TYPE
description: ADD TYPE
author: dansimp
ms.assetid: 8f1d3978-9977-4851-9f46-fee6aefa3535
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d2dcfb24a32dc733aa91b5534e0011090ef12b9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799061"
---
# <span data-ttu-id="1cb3e-103">ADD TYPE</span><span class="sxs-lookup"><span data-stu-id="1cb3e-103">ADD TYPE</span></span>


<span data-ttu-id="1cb3e-104">Adiciona a associação de tipo de arquivo especificada.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-104">Adds the specified file type association.</span></span>

`SFTMIME ADD TYPE:file-extension /APP application [/ICON icon-pathname]                 [/DESCRIPTION type-desc] [/CONTENT-TYPE content-type] [/GLOBAL]                 [/PERCEIVED-TYPE perceived-type] [/PROGID progid]                 [/CONFIRMOPEN {YES|NO}] [/SHOWEXT {YES|NO}]                 [/NEWMENU {YES|NO}]  [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1cb3e-105">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="1cb3e-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="1cb3e-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="1cb3e-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1cb3e-107">TIPO: &lt; extensão de arquivo&gt;</span><span class="sxs-lookup"><span data-stu-id="1cb3e-107">TYPE:&lt;file-extension&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cb3e-108">A extensão de nome de arquivo que será associada ao aplicativo especificado.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-108">The file name extension that will be associated with the application specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1cb3e-109">&lt;Aplicativo/App&gt;</span><span class="sxs-lookup"><span data-stu-id="1cb3e-109">/APP &lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cb3e-110">O nome e a versão (opcional) do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-110">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1cb3e-111">Ícone do/ICON &lt; -PathName&gt;</span><span class="sxs-lookup"><span data-stu-id="1cb3e-111">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cb3e-112">O caminho ou a URL do arquivo de ícone.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-112">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1cb3e-113">&lt;Tipo de/Description-desc&gt;</span><span class="sxs-lookup"><span data-stu-id="1cb3e-113">/DESCRIPTION &lt;type-desc&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cb3e-114">O nome amigável do tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-114">The user-friendly name for the file type.</span></span> <span data-ttu-id="1cb3e-115">O padrão é o &quot; arquivo de extensão.&quot;</span><span class="sxs-lookup"><span data-stu-id="1cb3e-115">Defaults to &quot;EXTENSION File.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1cb3e-116">&lt;Tipo de conteúdo/Content-Type&gt;</span><span class="sxs-lookup"><span data-stu-id="1cb3e-116">/CONTENT-TYPE &lt;content-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cb3e-117">O tipo de conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-117">The content type of the file.</span></span> <span data-ttu-id="1cb3e-118">O padrão é &quot; Application/Softricity-Extension.&quot;</span><span class="sxs-lookup"><span data-stu-id="1cb3e-118">Defaults to &quot;application/softricity-extension.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1cb3e-119">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="1cb3e-119">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cb3e-120">Se estiver presente, o pacote estará disponível para todos os usuários neste computador.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-120">If present, the package will be available for all users on this computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1cb3e-121">&lt;Tipo percebido/PERCEIVED-Type&gt;</span><span class="sxs-lookup"><span data-stu-id="1cb3e-121">/PERCEIVED-TYPE &lt;perceived-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cb3e-122">O tipo percebido do arquivo.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-122">The perceived type of the file.</span></span> <span data-ttu-id="1cb3e-123">O padrão é Nothing.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-123">Defaults to nothing.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1cb3e-124">&lt;ProgID/ProgId&gt;</span><span class="sxs-lookup"><span data-stu-id="1cb3e-124">/PROGID &lt;progid&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cb3e-125">O identificador programático para o tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-125">The programmatic identifier for the file type.</span></span> <span data-ttu-id="1cb3e-126">Padrão para App Virt. Extension. File.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-126">Defaults to App Virt.extension.File.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1cb3e-127">/CONFIRMOPEN</span><span class="sxs-lookup"><span data-stu-id="1cb3e-127">/CONFIRMOPEN</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cb3e-128">Indica se os usuários que baixam um arquivo desse tipo devem ser solicitados a abrir ou salvar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-128">Indicates whether users downloading a file of this type should be asked whether to open or save the file.</span></span> <span data-ttu-id="1cb3e-129">Padrão para Sim.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-129">Defaults to YES.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1cb3e-130">/SHOWEXT</span><span class="sxs-lookup"><span data-stu-id="1cb3e-130">/SHOWEXT</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cb3e-131">Indica se a extensão do arquivo sempre deve ser mostrada, mesmo se o usuário tiver solicitado que todas as extensões fiquem ocultas.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-131">Indicates whether the file's extension should always be shown, even if the user has requested that all extensions be hidden.</span></span> <span data-ttu-id="1cb3e-132">Padrão para não.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-132">Defaults to NO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1cb3e-133">/NEWMENU</span><span class="sxs-lookup"><span data-stu-id="1cb3e-133">/NEWMENU</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cb3e-134">Indica se uma entrada deve ser adicionada ao <strong> menu novo do Shell </strong> .</span><span class="sxs-lookup"><span data-stu-id="1cb3e-134">Indicates whether an entry should be added to the shell's <strong>New</strong> menu.</span></span> <span data-ttu-id="1cb3e-135">Padrão para não.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-135">Defaults to NO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1cb3e-136">/LOG</span><span class="sxs-lookup"><span data-stu-id="1cb3e-136">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cb3e-137">Se especificado, a saída será registrada no nome do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-137">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1cb3e-138">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="1cb3e-138">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cb3e-139">Se especificado, a saída será apresentada na janela ativa do console (padrão).</span><span class="sxs-lookup"><span data-stu-id="1cb3e-139">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1cb3e-140">/GUI</span><span class="sxs-lookup"><span data-stu-id="1cb3e-140">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cb3e-141">Se especificado, a saída será apresentada em uma caixa de diálogo do Windows.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-141">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="1cb3e-142">Para a versão 4.6, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-142">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1cb3e-143">/LOGU</span><span class="sxs-lookup"><span data-stu-id="1cb3e-143">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cb3e-144">Se especificado, a saída será registrada no nome do caminho especificado no formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="1cb3e-144">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1cb3e-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1cb3e-145">Related topics</span></span>


[<span data-ttu-id="1cb3e-146">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="1cb3e-146">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





