---
title: CONFIGURE SERVER
description: CONFIGURE SERVER
author: dansimp
ms.assetid: c916eddd-74f2-46e4-953d-120b23284e37
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7757f281ec57645d20367056ba0013ef476a91a1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798979"
---
# <span data-ttu-id="63972-103">CONFIGURE SERVER</span><span class="sxs-lookup"><span data-stu-id="63972-103">CONFIGURE SERVER</span></span>


<span data-ttu-id="63972-104">Permite que um usuário altere a configuração de um servidor; qualquer configuração não especificada não será modificada.</span><span class="sxs-lookup"><span data-stu-id="63972-104">Enables a user to change the setup of a server; any settings not specified will not be modified.</span></span>

`SFTMIME CONFIGURE SERVER:server-name [/NAME display-name] [/HOST hostname]                 [/PORT port] [/PATH path] [/TYPE {HTTP|RTSP}]                 [/REFRESH {ON|OFF}] [/SECURE]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="63972-105">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="63972-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="63972-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="63972-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63972-107">SERVIDOR: &lt; nome do servidor&gt;</span><span class="sxs-lookup"><span data-stu-id="63972-107">SERVER:&lt;server-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="63972-108">O nome de exibição do servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="63972-108">The display name for the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63972-109">&lt;Nome de exibição/Name&gt;</span><span class="sxs-lookup"><span data-stu-id="63972-109">/NAME &lt;display-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="63972-110">Novo nome para exibição do servidor.</span><span class="sxs-lookup"><span data-stu-id="63972-110">New display name for the server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63972-111">&lt;Nome do host/host&gt;</span><span class="sxs-lookup"><span data-stu-id="63972-111">/HOST &lt;hostname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="63972-112">O nome do host ou o endereço IP do servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="63972-112">The host name or IP address for the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63972-113">/PORT &lt; porta&gt;</span><span class="sxs-lookup"><span data-stu-id="63972-113">/PORT &lt;port&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="63972-114">A porta na qual o servidor de publicação escuta.</span><span class="sxs-lookup"><span data-stu-id="63972-114">The port on which the publishing server listens.</span></span> <span data-ttu-id="63972-115">O padrão é o 80 para servidores HTTP normais, 443 para servidores HTTP usando a segurança aprimorada, 554 para servidores de virtualização de aplicativos normais e 322 para servidores que usam segurança aprimorada.</span><span class="sxs-lookup"><span data-stu-id="63972-115">Defaults to 80 for normal HTTP servers, 443 for HTTP servers using enhanced security, 554 for normal Application Virtualization Servers, and 322 for servers using enhanced security.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63972-116">&lt;Caminho/Path&gt;</span><span class="sxs-lookup"><span data-stu-id="63972-116">/PATH &lt;path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="63972-117">A parte do caminho da URL usada em uma solicitação de publicação.</span><span class="sxs-lookup"><span data-stu-id="63972-117">The path portion of the URL used in a publishing request.</span></span> <span data-ttu-id="63972-118">Se o parâmetro TYPE estiver definido como RTSP, o caminho será opcional e padrão &quot; / &quot; .</span><span class="sxs-lookup"><span data-stu-id="63972-118">If the TYPE parameter is set to RTSP, the path is optional and defaults to &quot;/&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63972-119">/TYPE</span><span class="sxs-lookup"><span data-stu-id="63972-119">/TYPE</span></span></p></td>
<td align="left"><p><span data-ttu-id="63972-120">Indica se o servidor de publicação é um servidor Web ( &quot; http &quot; ) ou um servidor de virtualização de aplicativos ( &quot; RTSP &quot; ).</span><span class="sxs-lookup"><span data-stu-id="63972-120">Indicates whether the publishing server is a Web server (&quot;HTTP&quot;) or an Application Virtualization Server (&quot;RTSP&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63972-121">/REFRESH</span><span class="sxs-lookup"><span data-stu-id="63972-121">/REFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="63972-122">Se definido como ativado, as informações de publicação serão atualizadas quando o usuário fizer logon.</span><span class="sxs-lookup"><span data-stu-id="63972-122">If set to ON, publishing information will be refreshed when the user logs in.</span></span> <span data-ttu-id="63972-123">O padrão é ativado.</span><span class="sxs-lookup"><span data-stu-id="63972-123">Defaults to ON.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63972-124">/SECURE</span><span class="sxs-lookup"><span data-stu-id="63972-124">/SECURE</span></span></p></td>
<td align="left"><p><span data-ttu-id="63972-125">Se presente, indica que uma conexão com a segurança reforçada deve ser estabelecida com o servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="63972-125">If present, indicates that a connection with enhanced security should be established to the publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63972-126">/LOG</span><span class="sxs-lookup"><span data-stu-id="63972-126">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="63972-127">Se especificado, a saída será registrada no nome do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="63972-127">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="63972-128">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="63972-128">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="63972-129">Se especificado, a saída será apresentada na janela ativa do console (padrão).</span><span class="sxs-lookup"><span data-stu-id="63972-129">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63972-130">/GUI</span><span class="sxs-lookup"><span data-stu-id="63972-130">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="63972-131">Se especificado, a saída será apresentada em uma caixa de diálogo do Windows.</span><span class="sxs-lookup"><span data-stu-id="63972-131">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="63972-132">Para a versão 4.6, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="63972-132">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="63972-133">/LOGU</span><span class="sxs-lookup"><span data-stu-id="63972-133">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="63972-134">Se especificado, a saída será registrada no nome do caminho especificado no formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="63972-134">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="63972-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="63972-135">Related topics</span></span>


[<span data-ttu-id="63972-136">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="63972-136">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





