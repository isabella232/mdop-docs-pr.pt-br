---
title: DELETE SERVER
description: DELETE SERVER
author: dansimp
ms.assetid: 4c929639-1c1d-47c3-9225-cc4d7a8736f0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92af31a818174fb4b0e82a11c918af2484ac2bce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797976"
---
# <span data-ttu-id="8ec41-103">DELETE SERVER</span><span class="sxs-lookup"><span data-stu-id="8ec41-103">DELETE SERVER</span></span>


<span data-ttu-id="8ec41-104">Remove um servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="8ec41-104">Removes a publishing server.</span></span>

<span data-ttu-id="8ec41-105">**Observação**  Esse comando não remove quaisquer aplicativos ou pacotes publicados do cliente pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="8ec41-105">**Note** This command does not remove any applications or packages published to the client by the server.</span></span> <span data-ttu-id="8ec41-106">Para cada aplicativo, use o comando **limpar aplicativo** SFTMIME seguido do comando **excluir pacote** para remover completamente esses aplicativos e pacotes do cliente.</span><span class="sxs-lookup"><span data-stu-id="8ec41-106">For each application, use the SFTMIME **CLEAR APP** command followed by the **DELETE PACKAGE** command to completely remove those applications and packages from the client.</span></span>

 

`SFTMIME DELETE SERVER:server-name [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8ec41-107">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ec41-107">Parameter</span></span></th>
<th align="left"><span data-ttu-id="8ec41-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ec41-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8ec41-109">SERVIDOR: &lt; nome do servidor&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec41-109">SERVER:&lt;server-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ec41-110">O nome de exibição do servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="8ec41-110">The display name of the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8ec41-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="8ec41-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ec41-112">Se especificado, a saída será registrada no nome do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="8ec41-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8ec41-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="8ec41-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ec41-114">Se especificado, a saída será apresentada na janela ativa do console (padrão).</span><span class="sxs-lookup"><span data-stu-id="8ec41-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8ec41-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="8ec41-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ec41-116">Se especificado, a saída será apresentada em uma caixa de diálogo do Windows.</span><span class="sxs-lookup"><span data-stu-id="8ec41-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="8ec41-117">Para a versão 4.6, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="8ec41-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8ec41-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="8ec41-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ec41-119">Se especificado, a saída será registrada no nome do caminho especificado no formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="8ec41-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8ec41-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8ec41-120">Related topics</span></span>


[<span data-ttu-id="8ec41-121">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="8ec41-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





