---
title: CONFIGURE APP
description: CONFIGURE APP
author: dansimp
ms.assetid: fcfb4f86-8b7c-4208-bca3-955fd067079f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 42ff17e180df262deed3fe79674ad6fda6f0be4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797513"
---
# <span data-ttu-id="925fa-103">CONFIGURE APP</span><span class="sxs-lookup"><span data-stu-id="925fa-103">CONFIGURE APP</span></span>


<span data-ttu-id="925fa-104">Permite que o usuário altere o ícone associado a um aplicativo, mas não atualiza o ícone em atalhos existentes ou associações de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="925fa-104">Enables the user to change the icon associated with an application but does not update the icon on existing shortcuts or file type associations.</span></span>

`SFTMIME CONFIGURE APP:application /ICON icon-pathname                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="925fa-105">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="925fa-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="925fa-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="925fa-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="925fa-107">Aplicativo: &lt; aplicativo&gt;</span><span class="sxs-lookup"><span data-stu-id="925fa-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="925fa-108">O nome e a versão (opcional) do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="925fa-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="925fa-109">Ícone do/ICON &lt; -PathName&gt;</span><span class="sxs-lookup"><span data-stu-id="925fa-109">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="925fa-110">O caminho ou a URL do arquivo de ícone.</span><span class="sxs-lookup"><span data-stu-id="925fa-110">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="925fa-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="925fa-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="925fa-112">Se especificado, a saída será registrada no nome do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="925fa-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="925fa-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="925fa-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="925fa-114">Se especificado, a saída será apresentada na janela ativa do console (padrão).</span><span class="sxs-lookup"><span data-stu-id="925fa-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="925fa-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="925fa-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="925fa-116">Se especificado, a saída será apresentada em uma caixa de diálogo do Windows.</span><span class="sxs-lookup"><span data-stu-id="925fa-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="925fa-117">Para a versão 4.6, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="925fa-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="925fa-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="925fa-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="925fa-119">Se especificado, a saída será registrada no nome do caminho especificado no formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="925fa-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="925fa-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="925fa-120">Related topics</span></span>


[<span data-ttu-id="925fa-121">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="925fa-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





