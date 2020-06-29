---
title: DELETE APP
description: DELETE APP
author: dansimp
ms.assetid: 2f89c0c0-373b-4389-a26d-67b3f9712957
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c27c70ef3227ebaf6b16bcb1fbb4b4e65b7cb7f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797981"
---
# <span data-ttu-id="6a0d2-103">DELETE APP</span><span class="sxs-lookup"><span data-stu-id="6a0d2-103">DELETE APP</span></span>


<span data-ttu-id="6a0d2-104">Remove um registro de aplicativo do cache do sistema de arquivos para que ele não fique mais visível.</span><span class="sxs-lookup"><span data-stu-id="6a0d2-104">Removes an application record from the file system cache to make it no longer visible.</span></span> <span data-ttu-id="6a0d2-105">Os atalhos e associações de tipo de arquivo dos usuários estão ocultos, mas não excluídos.</span><span class="sxs-lookup"><span data-stu-id="6a0d2-105">Users’ shortcuts and file type associations are hidden but not deleted.</span></span> <span data-ttu-id="6a0d2-106">Nenhuma configuração de usuário é removida.</span><span class="sxs-lookup"><span data-stu-id="6a0d2-106">No user settings are removed.</span></span>

`SFTMIME DELETE APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a0d2-107">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="6a0d2-107">Parameter</span></span></th>
<th align="left"><span data-ttu-id="6a0d2-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a0d2-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a0d2-109">Aplicativo: &lt; aplicativo&gt;</span><span class="sxs-lookup"><span data-stu-id="6a0d2-109">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a0d2-110">O nome e a versão (opcional) do aplicativo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="6a0d2-110">The name and version (optional) of the application to be removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a0d2-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="6a0d2-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a0d2-112">Se especificado, a saída será registrada no nome do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="6a0d2-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a0d2-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="6a0d2-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a0d2-114">Se especificado, a saída será apresentada na janela ativa do console (padrão).</span><span class="sxs-lookup"><span data-stu-id="6a0d2-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a0d2-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="6a0d2-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a0d2-116">Se especificado, a saída será apresentada em uma caixa de diálogo do Windows.</span><span class="sxs-lookup"><span data-stu-id="6a0d2-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6a0d2-117">Para a versão 4.6, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="6a0d2-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a0d2-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="6a0d2-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a0d2-119">Se especificado, a saída será registrada no nome do caminho especificado no formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="6a0d2-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="6a0d2-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a0d2-120">Related topics</span></span>


[<span data-ttu-id="6a0d2-121">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="6a0d2-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





