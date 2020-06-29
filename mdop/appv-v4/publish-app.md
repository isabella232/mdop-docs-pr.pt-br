---
title: PUBLISH APP
description: PUBLISH APP
author: dansimp
ms.assetid: f25f06a8-ca23-435b-a0c2-16a5f39b6b97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2ccb19255786ee47a8356feef14be1c4d9b4fb2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796801"
---
# <span data-ttu-id="01a88-103">PUBLISH APP</span><span class="sxs-lookup"><span data-stu-id="01a88-103">PUBLISH APP</span></span>


<span data-ttu-id="01a88-104">Publica um atalho de aplicativo no menu Iniciar, na área de trabalho ou em outro local especificado do usuário.</span><span class="sxs-lookup"><span data-stu-id="01a88-104">Publishes an application shortcut to the user's Start menu, desktop, or other specified location.</span></span>

`SFTMIME PUBLISH APP:application                 {/DESKTOP | /START | /TARGET target-path} [/ICON icon-pathname]                 [/DISPLAY display-name] [/ARGS command-args...]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="01a88-105">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="01a88-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="01a88-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="01a88-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="01a88-107">APLICATIVO: &lt; aplicativo&gt;</span><span class="sxs-lookup"><span data-stu-id="01a88-107">APPLICATION:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="01a88-108">O nome e a versão (opcional) do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="01a88-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="01a88-109">/DESKTOP</span><span class="sxs-lookup"><span data-stu-id="01a88-109">/DESKTOP</span></span></p></td>
<td align="left"><p><span data-ttu-id="01a88-110">Publica um atalho para a área de trabalho do usuário.</span><span class="sxs-lookup"><span data-stu-id="01a88-110">Publishes a shortcut to the user's desktop.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="01a88-111">/START</span><span class="sxs-lookup"><span data-stu-id="01a88-111">/START</span></span></p></td>
<td align="left"><p><span data-ttu-id="01a88-112">Publica um atalho para a pasta aplicativos de virtualização de aplicativos na pasta programas do menu iniciar.</span><span class="sxs-lookup"><span data-stu-id="01a88-112">Publishes a shortcut to the Application Virtualization Applications folder in the Programs folder of the Start menu.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="01a88-113">/TARGET &lt; target-Path&gt;</span><span class="sxs-lookup"><span data-stu-id="01a88-113">/TARGET &lt;target-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="01a88-114">O caminho absoluto onde o atalho deve ser publicado.</span><span class="sxs-lookup"><span data-stu-id="01a88-114">The absolute path where the shortcut should be published.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="01a88-115">Ícone do/ICON &lt; -PathName&gt;</span><span class="sxs-lookup"><span data-stu-id="01a88-115">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="01a88-116">O caminho ou a URL do arquivo de ícone.</span><span class="sxs-lookup"><span data-stu-id="01a88-116">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="01a88-117">&lt;Nome de exibição de/display&gt;</span><span class="sxs-lookup"><span data-stu-id="01a88-117">/DISPLAY &lt;display-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="01a88-118">O nome de exibição do atalho.</span><span class="sxs-lookup"><span data-stu-id="01a88-118">The display name for the shortcut.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="01a88-119">/ARGS &lt; Command-args&gt;</span><span class="sxs-lookup"><span data-stu-id="01a88-119">/ARGS &lt;command-args&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="01a88-120">Parâmetros a serem passados para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="01a88-120">Parameters to be passed to the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="01a88-121">/LOG</span><span class="sxs-lookup"><span data-stu-id="01a88-121">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="01a88-122">Se especificado, a saída será registrada no nome do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="01a88-122">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="01a88-123">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="01a88-123">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="01a88-124">Se especificado, a saída será apresentada na janela ativa do console (padrão).</span><span class="sxs-lookup"><span data-stu-id="01a88-124">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="01a88-125">/GUI</span><span class="sxs-lookup"><span data-stu-id="01a88-125">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="01a88-126">Se especificado, a saída será apresentada em uma caixa de diálogo do Windows.</span><span class="sxs-lookup"><span data-stu-id="01a88-126">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="01a88-127">Para a versão 4.6, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="01a88-127">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="01a88-128">/LOGU</span><span class="sxs-lookup"><span data-stu-id="01a88-128">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="01a88-129">Se especificado, a saída será registrada no nome do caminho especificado no formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="01a88-129">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="01a88-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01a88-130">Related topics</span></span>


[<span data-ttu-id="01a88-131">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="01a88-131">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





