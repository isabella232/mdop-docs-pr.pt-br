---
title: LOAD PACKAGE
description: LOAD PACKAGE
author: dansimp
ms.assetid: eb19116d-e5d0-445c-b2f0-3116a09384d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 938aa92696c8530c91d9a7acaac42408de534edc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796885"
---
# <span data-ttu-id="294a5-103">LOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="294a5-103">LOAD PACKAGE</span></span>


<span data-ttu-id="294a5-104">Carrega o pacote especificado no cache do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="294a5-104">Loads the specified package into the file system cache.</span></span>

`SFTMIME LOAD PACKAGE:package-name [/SFTPATH sft-pathname]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="294a5-105">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="294a5-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="294a5-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="294a5-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="294a5-107">PACKAGE: &lt; Package-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="294a5-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="294a5-108">O nome do pacote a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="294a5-108">The name of the package to load.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="294a5-109">/SFTPATH &lt; SFT-PathName&gt;</span><span class="sxs-lookup"><span data-stu-id="294a5-109">/SFTPATH &lt;sft-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="294a5-110">Se especificado, o caminho para um arquivo SFT para carregar.</span><span class="sxs-lookup"><span data-stu-id="294a5-110">If specified, the path to an SFT file to load from.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="294a5-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="294a5-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="294a5-112">Se especificado, a saída será registrada no nome do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="294a5-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="294a5-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="294a5-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="294a5-114">Se especificado, a saída será apresentada na janela ativa do console (padrão).</span><span class="sxs-lookup"><span data-stu-id="294a5-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="294a5-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="294a5-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="294a5-116">Se especificado, a saída será apresentada em uma caixa de diálogo do Windows.</span><span class="sxs-lookup"><span data-stu-id="294a5-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="294a5-117">Para a versão 4.6, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="294a5-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="294a5-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="294a5-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="294a5-119">Se especificado, a saída será registrada no nome do caminho especificado no formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="294a5-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="294a5-120">**Observação**  Se nenhum SFTPATH for especificado, o cliente carregará o pacote usando o caminho que foi configurado para usar, com base no arquivo OSD, o valor da chave do registro ApplicationSourceRoot ou na configuração OverrideURL.</span><span class="sxs-lookup"><span data-stu-id="294a5-120">**Note** If no SFTPATH is specified, the client will load the package by using the path it has been configured to use, based on the OSD file, the ApplicationSourceRoot registry key value, or the OverrideURL setting.</span></span>

<span data-ttu-id="294a5-121">O comando **carregar pacote** executa uma carga síncrona e não será completa até que o pacote seja totalmente carregado ou até encontrar uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="294a5-121">The **LOAD PACKAGE** command performs a synchronous load and will not be complete until the package is fully loaded or until it encounters an error condition.</span></span>

 

## <span data-ttu-id="294a5-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="294a5-122">Related topics</span></span>


[<span data-ttu-id="294a5-123">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="294a5-123">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





