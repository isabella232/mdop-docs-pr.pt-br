---
title: DELETE TYPE
description: DELETE TYPE
author: dansimp
ms.assetid: f2852723-c894-49f3-a3c5-56f9648bb9ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0df68c0a0efcd0e269410d1580f7b0a82301c46d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797975"
---
# <span data-ttu-id="f0ec3-103">DELETE TYPE</span><span class="sxs-lookup"><span data-stu-id="f0ec3-103">DELETE TYPE</span></span>


<span data-ttu-id="f0ec3-104">Remove a associação de tipo de arquivo especificada.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-104">Removes the specified file type association.</span></span>

`SFTMIME DELETE TYPE:file-extension [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f0ec3-105">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0ec3-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="f0ec3-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f0ec3-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ec3-107">TIPO: &lt; extensão de arquivo&gt;</span><span class="sxs-lookup"><span data-stu-id="f0ec3-107">TYPE:&lt;file-extension&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ec3-108">A extensão de nome de arquivo a ser removida.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-108">The file name extension to be removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ec3-109">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="f0ec3-109">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ec3-110">Se especificado, indica que a associação global para a extensão de nome de arquivo deve ser removida.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-110">If specified, indicates that the global association for the file name extension should be removed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ec3-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="f0ec3-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ec3-112">Se especificado, a saída será registrada no nome do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f0ec3-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="f0ec3-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ec3-114">Se especificado, a saída será apresentada na janela ativa do console (padrão).</span><span class="sxs-lookup"><span data-stu-id="f0ec3-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ec3-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="f0ec3-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ec3-116">Se especificado, a saída será apresentada em uma caixa de diálogo do Windows.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f0ec3-117">Para a versão 4.6, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f0ec3-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="f0ec3-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="f0ec3-119">Se especificado, a saída será registrada no nome do caminho especificado no formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="f0ec3-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f0ec3-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f0ec3-120">Related topics</span></span>


[<span data-ttu-id="f0ec3-121">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="f0ec3-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





