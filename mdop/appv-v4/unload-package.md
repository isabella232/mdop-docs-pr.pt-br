---
title: UNLOAD PACKAGE
description: UNLOAD PACKAGE
author: dansimp
ms.assetid: a076eb5a-ce3d-49e4-ac7a-4d4df10e3477
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fbee040f97bf5675ace7e873741a4270a993a911
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796667"
---
# <span data-ttu-id="8e649-103">UNLOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="8e649-103">UNLOAD PACKAGE</span></span>


<span data-ttu-id="8e649-104">Descarrega o pacote do cache do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="8e649-104">Unloads the package from the file system cache.</span></span>

`SFTMIME UNLOAD PACKAGE:package-name [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8e649-105">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="8e649-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="8e649-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e649-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8e649-107">PACKAGE: &lt; Package-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="8e649-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e649-108">O nome do pacote a ser descarregado.</span><span class="sxs-lookup"><span data-stu-id="8e649-108">The name of the package to unload.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8e649-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="8e649-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e649-110">Se especificado, a saída será registrada no nome do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="8e649-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8e649-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="8e649-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e649-112">Se especificado, a saída será apresentada na janela ativa do console (padrão).</span><span class="sxs-lookup"><span data-stu-id="8e649-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8e649-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="8e649-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e649-114">Se especificado, a saída será apresentada em uma caixa de diálogo do Windows.</span><span class="sxs-lookup"><span data-stu-id="8e649-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="8e649-115">Para a versão 4.6, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="8e649-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8e649-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="8e649-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e649-117">Se especificado, a saída será registrada no nome do caminho especificado no formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="8e649-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8e649-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e649-118">Related topics</span></span>


[<span data-ttu-id="8e649-119">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="8e649-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





