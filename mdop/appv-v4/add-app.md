---
title: ADD APP
description: ADD APP
author: dansimp
ms.assetid: 329fd0c8-a795-49be-b0fd-1367c5b4a34b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac83c0cf130e8de1d34d42d74e946716e4503246
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797617"
---
# <span data-ttu-id="c7fc8-103">ADD APP</span><span class="sxs-lookup"><span data-stu-id="c7fc8-103">ADD APP</span></span>


<span data-ttu-id="c7fc8-104">Adiciona um registro de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7fc8-104">Adds an application record.</span></span>

`SFTMIME ADD APP:application /OSD osd-pathname [/ICON icon-pathname] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c7fc8-105">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7fc8-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="c7fc8-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="c7fc8-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7fc8-107">Aplicativo: &lt; aplicativo&gt;</span><span class="sxs-lookup"><span data-stu-id="c7fc8-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7fc8-108">O nome e a versão (opcional) do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7fc8-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c7fc8-109">/OSD &lt; OSD-PathName&gt;</span><span class="sxs-lookup"><span data-stu-id="c7fc8-109">/OSD &lt;osd-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7fc8-110">O caminho ou a URL do arquivo OSD.</span><span class="sxs-lookup"><span data-stu-id="c7fc8-110">The path or URL for the OSD file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7fc8-111">Ícone do/ICON &lt; -PathName&gt;</span><span class="sxs-lookup"><span data-stu-id="c7fc8-111">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7fc8-112">O caminho ou a URL do arquivo de ícone.</span><span class="sxs-lookup"><span data-stu-id="c7fc8-112">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c7fc8-113">/LOG</span><span class="sxs-lookup"><span data-stu-id="c7fc8-113">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7fc8-114">Se especificado, a saída será registrada no nome do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="c7fc8-114">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7fc8-115">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="c7fc8-115">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7fc8-116">Se especificado, a saída será apresentada na janela ativa do console (padrão).</span><span class="sxs-lookup"><span data-stu-id="c7fc8-116">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c7fc8-117">/GUI</span><span class="sxs-lookup"><span data-stu-id="c7fc8-117">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7fc8-118">Se especificado, a saída será apresentada em uma caixa de diálogo do Windows.</span><span class="sxs-lookup"><span data-stu-id="c7fc8-118">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c7fc8-119">Para a versão 4.6, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="c7fc8-119">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7fc8-120">/LOGU</span><span class="sxs-lookup"><span data-stu-id="c7fc8-120">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7fc8-121">Se especificado, a saída será registrada no nome do caminho especificado no formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="c7fc8-121">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c7fc8-122">**Observação**  O nome resultante do aplicativo será retirado do arquivo OSD e não do nome fornecido no aplicativo: APP &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="c7fc8-122">**Note** The resulting name of the application will be taken from the OSD file and not from the name provided in APP:&lt;application&gt;.</span></span>

 

## <span data-ttu-id="c7fc8-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7fc8-123">Related topics</span></span>


[<span data-ttu-id="c7fc8-124">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="c7fc8-124">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





