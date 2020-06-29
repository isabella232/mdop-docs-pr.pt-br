---
title: ADD PACKAGE
description: ADD PACKAGE
author: dansimp
ms.assetid: aa83928d-a234-4395-831e-2a7ef786ff53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 925349ce5bdf041b6a8768b5413692966e1cfc1e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799064"
---
# <span data-ttu-id="42e8c-103">ADD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="42e8c-103">ADD PACKAGE</span></span>


<span data-ttu-id="42e8c-104">Adiciona um registro de pacote.</span><span class="sxs-lookup"><span data-stu-id="42e8c-104">Adds a package record.</span></span> <span data-ttu-id="42e8c-105">Se o pacote já existir, esse comando atualizará a configuração do pacote existente.</span><span class="sxs-lookup"><span data-stu-id="42e8c-105">If the package already exists, this command will update the configuration of the existing package.</span></span>

`SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                 [/OVERRIDEURL url [/AUTOLOADONREFRESH] [/AUTOLOADONLOGIN]                 [/AUTOLOADONLAUNCH] [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="42e8c-106">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="42e8c-106">Parameter</span></span></th>
<th align="left"><span data-ttu-id="42e8c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="42e8c-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42e8c-108">PACKAGE: &lt; Package-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="42e8c-108">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="42e8c-109">Nome de usuário e de usuário visível para o pacote.</span><span class="sxs-lookup"><span data-stu-id="42e8c-109">User-visible and user-friendly name for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42e8c-110">&lt;Manifesto/manifest-caminho&gt;</span><span class="sxs-lookup"><span data-stu-id="42e8c-110">/MANIFEST &lt;manifest-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="42e8c-111">O caminho do arquivo de manifesto que lista os aplicativos incluídos no pacote e todas as informações de publicação deles.</span><span class="sxs-lookup"><span data-stu-id="42e8c-111">The path of the manifest file that lists the applications included in the package and all of their publishing information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42e8c-112">URL do/OVERRIDEURL &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="42e8c-112">/OVERRIDEURL &lt;URL&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="42e8c-113">O local do arquivo SFT do pacote.</span><span class="sxs-lookup"><span data-stu-id="42e8c-113">The location of the package's SFT file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42e8c-114">/AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="42e8c-114">/AUTOLOADONREFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="42e8c-115">O carregamento em segundo plano é executado após uma atualização de publicação.</span><span class="sxs-lookup"><span data-stu-id="42e8c-115">Background loading is performed after a publishing refresh.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42e8c-116">/AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="42e8c-116">/AUTOLOADONLOGIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="42e8c-117">O carregamento em segundo plano é executado quando um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="42e8c-117">Background loading is performed when a user logs in.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42e8c-118">/AUTOLOADONLAUNCH</span><span class="sxs-lookup"><span data-stu-id="42e8c-118">/AUTOLOADONLAUNCH</span></span></p></td>
<td align="left"><p><span data-ttu-id="42e8c-119">O carregamento em segundo plano é executado após um usuário iniciar um aplicativo do pacote.</span><span class="sxs-lookup"><span data-stu-id="42e8c-119">Background loading is performed after a user starts an application from the package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42e8c-120">/AUTOLOADTARGET alvo</span><span class="sxs-lookup"><span data-stu-id="42e8c-120">/AUTOLOADTARGET target</span></span></p></td>
<td align="left"><p><span data-ttu-id="42e8c-121">Indica quais aplicativos do pacote serão carregados de forma carregada.</span><span class="sxs-lookup"><span data-stu-id="42e8c-121">Indicates which applications from the package will be autoloaded.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42e8c-122">NENHUMA</span><span class="sxs-lookup"><span data-stu-id="42e8c-122">NONE</span></span></p></td>
<td align="left"><p><span data-ttu-id="42e8c-123">Nenhuma sobrecarga será realizada, apesar da presença de qualquer sinalizador/AUTOLOADONxxx.</span><span class="sxs-lookup"><span data-stu-id="42e8c-123">No autoloading will be performed, despite the presence of any /AUTOLOADONxxx flags.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42e8c-124">TODO</span><span class="sxs-lookup"><span data-stu-id="42e8c-124">ALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="42e8c-125">Se um gatilho de autocarregamento estiver habilitado, todos os aplicativos do pacote serão carregados no cache, independentemente de terem sido iniciados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="42e8c-125">If an autoload trigger is enabled, all applications in the package will be loaded into cache whether or not they have been previously started.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42e8c-126">PREVUSED</span><span class="sxs-lookup"><span data-stu-id="42e8c-126">PREVUSED</span></span></p></td>
<td align="left"><p><span data-ttu-id="42e8c-127">Se um gatilho de autocarregamento estiver habilitado, o pacote será carregado se qualquer aplicativo deste pacote tiver sido iniciado anteriormente por um usuário.</span><span class="sxs-lookup"><span data-stu-id="42e8c-127">If an autoload trigger is enabled, the package will load if any applications in this package have previously been started by a user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42e8c-128">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="42e8c-128">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="42e8c-129">Se estiver presente, o pacote estará disponível para todos os usuários neste computador.</span><span class="sxs-lookup"><span data-stu-id="42e8c-129">If present, the package will be available for all users on this computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42e8c-130">/LOG</span><span class="sxs-lookup"><span data-stu-id="42e8c-130">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="42e8c-131">Se especificado, a saída será registrada no nome do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="42e8c-131">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42e8c-132">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="42e8c-132">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="42e8c-133">Se especificado, a saída será apresentada na janela ativa do console (padrão).</span><span class="sxs-lookup"><span data-stu-id="42e8c-133">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="42e8c-134">/GUI</span><span class="sxs-lookup"><span data-stu-id="42e8c-134">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="42e8c-135">Se especificado, a saída será apresentada em uma caixa de diálogo do Windows.</span><span class="sxs-lookup"><span data-stu-id="42e8c-135">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="42e8c-136">Para a versão 4.6, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="42e8c-136">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="42e8c-137">/LOGU</span><span class="sxs-lookup"><span data-stu-id="42e8c-137">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="42e8c-138">Se especificado, a saída será registrada no nome do caminho especificado no formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="42e8c-138">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="42e8c-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="42e8c-139">Related topics</span></span>


[<span data-ttu-id="42e8c-140">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="42e8c-140">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





