---
title: UNLOAD APP
description: UNLOAD APP
author: dansimp
ms.assetid: f0d729ae-8772-498b-be11-1a4b35499c53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f1ae30f5b8c788f8763c2c2b9d1c1956182750d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796668"
---
# <span data-ttu-id="4aa34-103">UNLOAD APP</span><span class="sxs-lookup"><span data-stu-id="4aa34-103">UNLOAD APP</span></span>


<span data-ttu-id="4aa34-104">Descarrega o aplicativo e todos os outros aplicativos do pacote no cache do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="4aa34-104">Unloads the application and all other applications in the package from the file system cache.</span></span>

`SFTMIME UNLOAD APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4aa34-105">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="4aa34-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="4aa34-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="4aa34-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4aa34-107">Aplicativo: &lt; aplicativo&gt;</span><span class="sxs-lookup"><span data-stu-id="4aa34-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4aa34-108">O nome e a versão (opcional) do aplicativo a ser descarregado.</span><span class="sxs-lookup"><span data-stu-id="4aa34-108">The name and version (optional) of the application to unload.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4aa34-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="4aa34-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="4aa34-110">Se especificado, a saída será registrada no nome do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="4aa34-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4aa34-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="4aa34-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="4aa34-112">Se especificado, a saída será apresentada na janela ativa do console (padrão).</span><span class="sxs-lookup"><span data-stu-id="4aa34-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4aa34-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="4aa34-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="4aa34-114">Se especificado, a saída será apresentada em uma caixa de diálogo do Windows.</span><span class="sxs-lookup"><span data-stu-id="4aa34-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="4aa34-115">Para a versão 4.6, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="4aa34-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4aa34-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="4aa34-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="4aa34-117">Se especificado, a saída será registrada no nome do caminho especificado no formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="4aa34-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4aa34-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4aa34-118">Related topics</span></span>


[<span data-ttu-id="4aa34-119">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="4aa34-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





