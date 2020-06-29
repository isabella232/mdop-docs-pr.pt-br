---
title: CONFIGURE PACKAGE
description: CONFIGURE PACKAGE
author: dansimp
ms.assetid: acc7eaa8-6ada-47b9-a655-2ca2537605b9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc8b315b68349cc9834316786b0bf15d4ac3c5cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797507"
---
# <span data-ttu-id="11165-103">CONFIGURE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="11165-103">CONFIGURE PACKAGE</span></span>


<span data-ttu-id="11165-104">Permite que o usuário altere um arquivo de manifesto de pacote, origem do pacote, tipos de gatilho de carga ou destino de carga para um pacote.</span><span class="sxs-lookup"><span data-stu-id="11165-104">Enables the user to change a package manifest file, package source, load trigger types, or load target for a package.</span></span>

`SFTMIME CONFIGURE PACKAGE:package-name [/MANIFEST manifest-path]                 [/OVERRIDEURL url] [/AUTOLOADNEVER] [/AUTOLOADONREFRESH]                 [/AUTOLOADONLOGIN] [/AUTOLOADONLAUNCH]                 [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/LOG log-pathname | /CONSOLE | /GUI]                 [/NO-UPDATE-FTA-SHORTCUT {TRUE|FALSE} {/GLOBAL}]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="11165-105">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="11165-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="11165-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="11165-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11165-107">PACKAGE: &lt; Package-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="11165-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="11165-108">Nome de usuário e de usuário visível para o pacote.</span><span class="sxs-lookup"><span data-stu-id="11165-108">User-visible and user-friendly name for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11165-109">&lt;Manifesto/manifest-caminho&gt;</span><span class="sxs-lookup"><span data-stu-id="11165-109">/MANIFEST &lt;manifest-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="11165-110">O caminho ou a URL do arquivo de manifesto que lista os aplicativos incluídos no pacote e todas as informações de publicação deles.</span><span class="sxs-lookup"><span data-stu-id="11165-110">The path or URL of the manifest file that lists the applications included in the package and all of their publishing information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11165-111">URL do/OVERRIDEURL &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="11165-111">/OVERRIDEURL &lt;URL&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="11165-112">O local do arquivo SFT do pacote.</span><span class="sxs-lookup"><span data-stu-id="11165-112">The location of the package's SFT file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11165-113">/AUTOLOADNEVER</span><span class="sxs-lookup"><span data-stu-id="11165-113">/AUTOLOADNEVER</span></span></p></td>
<td align="left"><p><span data-ttu-id="11165-114">O carregamento em segundo plano está desativado para o pacote.</span><span class="sxs-lookup"><span data-stu-id="11165-114">Background loading is turned off for the package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11165-115">/AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="11165-115">/AUTOLOADONREFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="11165-116">O carregamento em segundo plano é executado após uma atualização de publicação.</span><span class="sxs-lookup"><span data-stu-id="11165-116">Background loading is performed after a publishing refresh.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11165-117">/AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="11165-117">/AUTOLOADONLOGIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="11165-118">O carregamento em segundo plano é executado quando um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="11165-118">Background loading is performed when a user logs in.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11165-119">/AUTOLOADONLAUNCH</span><span class="sxs-lookup"><span data-stu-id="11165-119">/AUTOLOADONLAUNCH</span></span></p></td>
<td align="left"><p><span data-ttu-id="11165-120">O carregamento em segundo plano é executado após um usuário iniciar um aplicativo do pacote.</span><span class="sxs-lookup"><span data-stu-id="11165-120">Background loading is performed after a user starts an application from the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11165-121">/AUTOLOADTARGET &lt; alvo&gt;</span><span class="sxs-lookup"><span data-stu-id="11165-121">/AUTOLOADTARGET &lt;target&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="11165-122">Indica quais aplicativos do pacote serão carregados de forma carregada.</span><span class="sxs-lookup"><span data-stu-id="11165-122">Indicates which applications from the package will be autoloaded.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11165-123">NENHUMA</span><span class="sxs-lookup"><span data-stu-id="11165-123">NONE</span></span></p></td>
<td align="left"><p><span data-ttu-id="11165-124">Nenhuma sobrecarga será realizada, apesar da presença de qualquer sinalizador/AUTOLOADONxxx.</span><span class="sxs-lookup"><span data-stu-id="11165-124">No autoloading will be performed despite the presence of any /AUTOLOADONxxx flags.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11165-125">TODO</span><span class="sxs-lookup"><span data-stu-id="11165-125">ALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="11165-126">Se um gatilho de autocarregamento estiver habilitado, todos os aplicativos do pacote serão carregados no cache independentemente de terem sido iniciados.</span><span class="sxs-lookup"><span data-stu-id="11165-126">If an autoload trigger is enabled, all applications in the package will be loaded into cache regardless of whether they have ever been launched.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11165-127">PREVUSED</span><span class="sxs-lookup"><span data-stu-id="11165-127">PREVUSED</span></span></p></td>
<td align="left"><p><span data-ttu-id="11165-128">Se um gatilho de autocarregamento estiver habilitado, o pacote será carregado se qualquer aplicativo deste pacote tiver sido iniciado anteriormente por um usuário.</span><span class="sxs-lookup"><span data-stu-id="11165-128">If an autoload trigger is enabled, the package will load if any applications in this package have previously been started by a user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11165-129">/LOG</span><span class="sxs-lookup"><span data-stu-id="11165-129">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="11165-130">Se especificado, a saída será registrada no nome do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="11165-130">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11165-131">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="11165-131">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="11165-132">Se especificado, a saída será apresentada na janela ativa do console (padrão).</span><span class="sxs-lookup"><span data-stu-id="11165-132">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11165-133">/GUI</span><span class="sxs-lookup"><span data-stu-id="11165-133">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="11165-134">Se especificado, a saída será apresentada em uma caixa de diálogo do Windows.</span><span class="sxs-lookup"><span data-stu-id="11165-134">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="11165-135">Para a versão 4.6, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="11165-135">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11165-136">/LOGU</span><span class="sxs-lookup"><span data-stu-id="11165-136">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="11165-137">Se especificado, a saída será registrada no nome do caminho especificado no formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="11165-137">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="11165-138">Para a versão 4.6 SP2, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="11165-138">For version4.6 SP2, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="11165-139">[/NO-UPDATE-FTA-SHORTCUT {TRUE | FALSE} {/GLOBAL}]</span><span class="sxs-lookup"><span data-stu-id="11165-139">[/NO-UPDATE-FTA-SHORTCUT {TRUE|FALSE} {/GLOBAL}]</span></span></p></td>
<td align="left"><p><span data-ttu-id="11165-140">Se definido como TRUE, um valor do registro será criado para o pacote, seja por usuário ou globalmente se o sinalizador/GLOBAL for especificado.</span><span class="sxs-lookup"><span data-stu-id="11165-140">If set to TRUE, a registry value is created for the package, either per user, or globally if the /GLOBAL flag is specified.</span></span></p>
<p><span data-ttu-id="11165-141">Se definido como FALSE, o valor do registro será removido e as associações de tipo de arquivo (FTA) do pacote serão reinstaladas.</span><span class="sxs-lookup"><span data-stu-id="11165-141">If set to FALSE, the registry value is removed and the file type associations (FTA) for the package are reinstalled.</span></span></p>
<p><span data-ttu-id="11165-142">Se não for especificado, ocorrerá a FTA normal e o comportamento de publicação de atalhos.</span><span class="sxs-lookup"><span data-stu-id="11165-142">If not specified, normal FTA and shortcut publishing behavior occurs.</span></span> <span data-ttu-id="11165-143">Se você executar qualquer operação de atualização de publicação subsequente no cliente do App-V 4,6 SP2, os atalhos e FTAs para pacotes que possuem esse valor de registro definido não serão alterados, e os atalhos e FTAs não serão registrados na inicialização do sistema ou no logon do usuário, a menos que você redefina o sinalizador.</span><span class="sxs-lookup"><span data-stu-id="11165-143">If you perform any subsequent publishing refresh operations on the App-V 4.6 SP2 client, the shortcuts and FTAs for packages that have this registry value set will not be changed, and the shortcuts and FTAs will not be registered at system startup or user login unless you reset the flag.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="11165-144">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="11165-144">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="11165-145">Funciona em conjunto com o sinalizador/NO-UPDATE-FTA-SHORTCUT.</span><span class="sxs-lookup"><span data-stu-id="11165-145">Works in conjunction with the /NO-UPDATE-FTA-SHORTCUT flag.</span></span> <span data-ttu-id="11165-146">Se o sinalizador/GLOBAL estiver presente, isso indicará que um valor do registro será criado para esse pacote para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="11165-146">If the /GLOBAL flag is present, it indicates that a registry value will be created for that package for all users.</span></span> <span data-ttu-id="11165-147">Por padrão, o valor do registro é criado apenas para esse usuário.</span><span class="sxs-lookup"><span data-stu-id="11165-147">By default, the registry value is created only for this user.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="11165-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="11165-148">Related topics</span></span>


[<span data-ttu-id="11165-149">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="11165-149">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





