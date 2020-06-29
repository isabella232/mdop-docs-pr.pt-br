---
title: DELETE PACKAGE
description: DELETE PACKAGE
author: dansimp
ms.assetid: 8f7a4598-610d-490e-a224-426acce01a9f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0051967ca308e88d143b8116330f5d770d6086d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797977"
---
# <span data-ttu-id="18064-103">DELETE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="18064-103">DELETE PACKAGE</span></span>


<span data-ttu-id="18064-104">Remove um registro de pacote e os aplicativos associados a ele.</span><span class="sxs-lookup"><span data-stu-id="18064-104">Removes a package record and the applications associated with it.</span></span>

`SFTMIME DELETE PACKAGE:package-name                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="18064-105">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="18064-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="18064-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="18064-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18064-107">PACKAGE: &lt; Package-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="18064-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="18064-108">O nome do pacote a ser removido.</span><span class="sxs-lookup"><span data-stu-id="18064-108">The name of the package to be removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18064-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="18064-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="18064-110">Se especificado, a saída será registrada no nome do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="18064-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18064-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="18064-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="18064-112">Se especificado, a saída será apresentada na janela ativa do console (padrão).</span><span class="sxs-lookup"><span data-stu-id="18064-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="18064-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="18064-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="18064-114">Se especificado, a saída será apresentada em uma caixa de diálogo do Windows.</span><span class="sxs-lookup"><span data-stu-id="18064-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="18064-115">Para a versão 4.6, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="18064-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="18064-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="18064-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="18064-117">Se especificado, a saída será registrada no nome do caminho especificado no formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="18064-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="18064-118">**Importante**  O comando excluir pacote sempre executa uma exclusão global do pacote e exclui somente os tipos de arquivos globais e atalhos.</span><span class="sxs-lookup"><span data-stu-id="18064-118">**Important** The DELETE PACKAGE command always performs a global delete of the package and deletes only global file types and shortcuts.</span></span>

<span data-ttu-id="18064-119">Se o pacote for global, esse comando deve ser executado como administrador local; caso contrário, somente a permissão **DeleteApp** é necessária.</span><span class="sxs-lookup"><span data-stu-id="18064-119">If the package is global, this command must be run as local Administrator; otherwise, only **DeleteApp** permission is needed.</span></span>

 

## <span data-ttu-id="18064-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="18064-120">Related topics</span></span>


[<span data-ttu-id="18064-121">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="18064-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





