---
title: ADD SERVER
description: ADD SERVER
author: dansimp
ms.assetid: 4be2ac2e-a410-4711-9f84-f305393c8fa7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e15a5943b40e14b2f9031bf8b3ddffa693e32dea
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797615"
---
# <span data-ttu-id="4e3be-103">ADD SERVER</span><span class="sxs-lookup"><span data-stu-id="4e3be-103">ADD SERVER</span></span>


<span data-ttu-id="4e3be-104">Adiciona um servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="4e3be-104">Adds a publishing server.</span></span>

`SFTMIME ADD SERVER:server-name /HOST hostname /TYPE {HTTP|RTSP}                 /PATH path [/PORT port] [/REFRESH {ON|OFF}] [/SECURE]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4e3be-105">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="4e3be-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="4e3be-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e3be-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e3be-107">SERVIDOR: &lt; nome do servidor&gt;</span><span class="sxs-lookup"><span data-stu-id="4e3be-107">SERVER:&lt;server-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e3be-108">O nome de exibição do servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="4e3be-108">The display name for the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4e3be-109">&lt;Nome do host/host&gt;</span><span class="sxs-lookup"><span data-stu-id="4e3be-109">/HOST &lt;hostname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e3be-110">O nome do host ou o endereço IP do servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="4e3be-110">The host name or IP address for the publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e3be-111">/TYPE {HTTP | RTSP</span><span class="sxs-lookup"><span data-stu-id="4e3be-111">/TYPE {HTTP|RTSP}</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e3be-112">Indica se o servidor de publicação é um servidor Web ( &quot; http &quot; ) ou um servidor de virtualização de aplicativos ( &quot; RTSP &quot; ).</span><span class="sxs-lookup"><span data-stu-id="4e3be-112">Indicates whether the publishing server is a Web server (&quot;HTTP&quot;) or an Application Virtualization Server (&quot;RTSP&quot;).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4e3be-113">/PORT &lt; porta&gt;</span><span class="sxs-lookup"><span data-stu-id="4e3be-113">/PORT &lt;port&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e3be-114">A porta na qual o servidor de publicação escuta.</span><span class="sxs-lookup"><span data-stu-id="4e3be-114">The port on which the publishing server listens.</span></span> <span data-ttu-id="4e3be-115">O padrão é o 80 para servidores HTTP normais, 443 para servidores HTTP usando a segurança aprimorada, 554 para servidores de virtualização de aplicativos normais e 322 para servidores que usam segurança aprimorada.</span><span class="sxs-lookup"><span data-stu-id="4e3be-115">Defaults to 80 for normal HTTP servers, 443 for HTTP servers using enhanced security, 554 for normal Application Virtualization Servers, and 322 for servers using enhanced security.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e3be-116">&lt;Caminho/Path&gt;</span><span class="sxs-lookup"><span data-stu-id="4e3be-116">/PATH &lt;path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e3be-117">A parte do caminho da URL usada em uma solicitação de publicação.</span><span class="sxs-lookup"><span data-stu-id="4e3be-117">The path portion of the URL used in a publishing request.</span></span> <span data-ttu-id="4e3be-118">Se o parâmetro TYPE estiver definido como RTSP, o caminho será opcional e padrão &quot; / &quot; .</span><span class="sxs-lookup"><span data-stu-id="4e3be-118">If the TYPE parameter is set to RTSP, the path is optional and defaults to &quot;/&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4e3be-119">/REFRESH</span><span class="sxs-lookup"><span data-stu-id="4e3be-119">/REFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e3be-120">Se definido como ativado, as informações de publicação serão atualizadas quando o usuário fizer logon.</span><span class="sxs-lookup"><span data-stu-id="4e3be-120">If set to ON, publishing information will be refreshed when the user logs in.</span></span> <span data-ttu-id="4e3be-121">O padrão é ativado.</span><span class="sxs-lookup"><span data-stu-id="4e3be-121">Defaults to ON.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e3be-122">/SECURE</span><span class="sxs-lookup"><span data-stu-id="4e3be-122">/SECURE</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e3be-123">Se presente, indica que uma conexão com a segurança reforçada deve ser estabelecida com o servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="4e3be-123">If present, indicates that a connection with enhanced security should be established to the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4e3be-124">/LOG</span><span class="sxs-lookup"><span data-stu-id="4e3be-124">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e3be-125">Se especificado, a saída será registrada no nome do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="4e3be-125">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e3be-126">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="4e3be-126">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e3be-127">Se especificado, a saída será apresentada na janela ativa do console (padrão).</span><span class="sxs-lookup"><span data-stu-id="4e3be-127">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4e3be-128">/GUI</span><span class="sxs-lookup"><span data-stu-id="4e3be-128">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e3be-129">Se especificado, a saída será apresentada em uma caixa de diálogo do Windows.</span><span class="sxs-lookup"><span data-stu-id="4e3be-129">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="4e3be-130">Para a versão 4.6, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="4e3be-130">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4e3be-131">/LOGU</span><span class="sxs-lookup"><span data-stu-id="4e3be-131">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="4e3be-132">Se especificado, a saída será registrada no nome do caminho especificado no formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="4e3be-132">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4e3be-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e3be-133">Related topics</span></span>


[<span data-ttu-id="4e3be-134">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="4e3be-134">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





