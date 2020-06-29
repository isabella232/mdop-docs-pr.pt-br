---
title: LOAD APP
description: LOAD APP
author: dansimp
ms.assetid: 7b727d0c-5423-419d-92ef-7ebbc6343e79
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 02bd6e35da898f5b34f7efc21cbc01a72d555b8d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796887"
---
# <span data-ttu-id="92318-103">LOAD APP</span><span class="sxs-lookup"><span data-stu-id="92318-103">LOAD APP</span></span>


<span data-ttu-id="92318-104">Carrega o aplicativo especificado e todos os outros aplicativos do pacote no cache do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="92318-104">Loads the specified application and all other applications in the package into the file system cache.</span></span>

<span data-ttu-id="92318-105">**Observação**  O comando **carregar aplicativo** inicia o processo de carregamento e uma barra de progresso é exibida na área de notificação da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="92318-105">**Note** The **LOAD APP** command starts the load process and a progress bar is displayed in the Desktop Notification Area.</span></span> <span data-ttu-id="92318-106">O comando sai imediatamente após iniciar esse processo, portanto, os erros de carregamento são exibidos no mesmo local.</span><span class="sxs-lookup"><span data-stu-id="92318-106">The command exits immediately after starting this process, so any load errors are displayed in the same location.</span></span> <span data-ttu-id="92318-107">Use o comando **carregar pacote** se desejar iniciar o processo de carregamento a partir da linha de comando sem usar a área de notificação da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="92318-107">Use the **LOAD PACKAGE** command if you want to start the load process from the command line without using the Desktop Notification Area.</span></span>

 

`SFTMIME LOAD APP:application [/LOG log-pathname | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="92318-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="92318-108">Parameter</span></span></th>
<th align="left"><span data-ttu-id="92318-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="92318-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="92318-110">Aplicativo: &lt; aplicativo&gt;</span><span class="sxs-lookup"><span data-stu-id="92318-110">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="92318-111">O nome e a versão (opcional) do aplicativo a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="92318-111">The name and version (optional) of the application to load.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="92318-112">/LOG</span><span class="sxs-lookup"><span data-stu-id="92318-112">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="92318-113">Se especificado, a saída será registrada no nome do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="92318-113">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="92318-114">/GUI</span><span class="sxs-lookup"><span data-stu-id="92318-114">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="92318-115">Se especificado, a saída será apresentada em uma caixa de diálogo do Windows.</span><span class="sxs-lookup"><span data-stu-id="92318-115">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="92318-116">Para a versão 4.6, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="92318-116">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="92318-117">/LOGU</span><span class="sxs-lookup"><span data-stu-id="92318-117">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="92318-118">Se especificado, a saída será registrada no nome do caminho especificado no formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="92318-118">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="92318-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="92318-119">Related topics</span></span>


[<span data-ttu-id="92318-120">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="92318-120">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





