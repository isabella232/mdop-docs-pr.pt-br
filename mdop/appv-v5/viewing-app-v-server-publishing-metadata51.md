---
title: Exibindo os metadados de publicação do servidor do App-V
description: Exibindo os metadados de publicação do servidor do App-V
author: dansimp
ms.assetid: d5fa9eb5-647c-478d-8a4d-0ecda018bce6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97c59301678280febe23b8061c08033a88ae49c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796198"
---
# <span data-ttu-id="df858-103">Exibindo os metadados de publicação do servidor do App-V</span><span class="sxs-lookup"><span data-stu-id="df858-103">Viewing App-V Server Publishing Metadata</span></span>


<span data-ttu-id="df858-104">Use este procedimento para exibir metadados de publicação, que podem ajudar você a solucionar problemas relacionados à publicação.</span><span class="sxs-lookup"><span data-stu-id="df858-104">Use this procedure to view publishing metadata, which can help you resolve publishing-related issues.</span></span> <span data-ttu-id="df858-105">Você deve usar o servidor de gerenciamento do App-V para usar este procedimento.</span><span class="sxs-lookup"><span data-stu-id="df858-105">You must be using the App-V Management server to use this procedure.</span></span>

<span data-ttu-id="df858-106">Este artigo contém as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="df858-106">This article contains the following information:</span></span>

-   [<span data-ttu-id="df858-107">Requisitos do App-V 5,1 para visualização de metadados de publicação</span><span class="sxs-lookup"><span data-stu-id="df858-107">App-V 5.1 requirements for viewing publishing metadata</span></span>](#bkmk-51-reqs-pub-meta)

-   [<span data-ttu-id="df858-108">Sintaxe a ser usada para exibir metadados de publicação</span><span class="sxs-lookup"><span data-stu-id="df858-108">Syntax to use for viewing publishing metadata</span></span>](#bkmk-syntax-view-pub-meta)

-   [<span data-ttu-id="df858-109">Consultar valores para a versão e o sistema operacional do cliente</span><span class="sxs-lookup"><span data-stu-id="df858-109">Query values for client operating system and version</span></span>](#bkmk-values-query-pub-meta)

-   [<span data-ttu-id="df858-110">Definição de metadados de publicação</span><span class="sxs-lookup"><span data-stu-id="df858-110">Definition of publishing metadata</span></span>](#bkmk-whatis-pub-metadata)

## <a href="" id="bkmk-51-reqs-pub-meta"></a><span data-ttu-id="df858-111">Requisitos do App-V 5,1 para visualização de metadados de publicação</span><span class="sxs-lookup"><span data-stu-id="df858-111">App-V 5.1 requirements for viewing publishing metadata</span></span>


<span data-ttu-id="df858-112">No App-V 5,1, você deve fornecer os seguintes valores no endereço quando consulta o servidor de publicação App-V para metadados:</span><span class="sxs-lookup"><span data-stu-id="df858-112">In App-V 5.1, you must provide the following values in the address when you query the App-V Publishing server for metadata:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="df858-113">Valor</span><span class="sxs-lookup"><span data-stu-id="df858-113">Value</span></span></th>
<th align="left"><span data-ttu-id="df858-114">Detalhes adicionais</span><span class="sxs-lookup"><span data-stu-id="df858-114">Additional details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="df858-115">ClientVersion</span><span class="sxs-lookup"><span data-stu-id="df858-115">ClientVersion</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="df858-116">Se você omitir <strong> o </strong> parâmetro ClientVersion da consulta, os metadados excluirão os recursos que foram novos no App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="df858-116">If you omit the <strong>ClientVersion</strong> parameter from the query, the metadata excludes the features that were new in App-V 5.0 SP3.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="df858-117">ClientOS</span><span class="sxs-lookup"><span data-stu-id="df858-117">ClientOS</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="df858-118">Você deve fornecer esse valor apenas se selecionar sistemas operacionais específicos do cliente quando você sequenciar o pacote.</span><span class="sxs-lookup"><span data-stu-id="df858-118">You have to provide this value only if you select specific client operating systems when you sequence the package.</span></span> <span data-ttu-id="df858-119">Se você selecionar o padrão (todos os sistemas operacionais), não especifique esse valor na consulta.</span><span class="sxs-lookup"><span data-stu-id="df858-119">If you select the default (all operating systems), do not specify this value in the query.</span></span></p>
<p><span data-ttu-id="df858-120">Se você omitir <strong> o </strong> parâmetro ClientOS da consulta, somente os pacotes que foram sequenciados para dar suporte a qualquer sistema operacional aparecem nos metadados.</span><span class="sxs-lookup"><span data-stu-id="df858-120">If you omit the <strong>ClientOS</strong> parameter from the query, only the packages that were sequenced to support any operating system appear in the metadata.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-syntax-view-pub-meta"></a><span data-ttu-id="df858-121">Sintaxe de consulta para exibir metadados de publicação</span><span class="sxs-lookup"><span data-stu-id="df858-121">Query syntax for viewing publishing metadata</span></span>


<span data-ttu-id="df858-122">A tabela a seguir fornece os exemplos de sintaxe e consulta.</span><span class="sxs-lookup"><span data-stu-id="df858-122">The following table provides the syntax and query examples.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="df858-123">Versão do App-V</span><span class="sxs-lookup"><span data-stu-id="df858-123">Version of App-V</span></span></th>
<th align="left"><span data-ttu-id="df858-124">Sintaxe da consulta</span><span class="sxs-lookup"><span data-stu-id="df858-124">Query syntax</span></span></th>
<th align="left"><span data-ttu-id="df858-125">Descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="df858-125">Parameter descriptions</span></span></th>
<th align="left"><span data-ttu-id="df858-126">Exemplo</span><span class="sxs-lookup"><span data-stu-id="df858-126">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df858-127">App-V 5,0 SP3 e App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="df858-127">App-V 5.0 SP3 and App-V 5.1</span></span></p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/?ClientVersion=&lt;AppvClientVersion&gt;&amp;ClientOS=&lt;OSStringValue&gt;</code></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="df858-128">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="df858-128">Parameter</span></span></th>
<th align="left"><span data-ttu-id="df858-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="df858-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df858-130">&lt;PubServer&gt;</span><span class="sxs-lookup"><span data-stu-id="df858-130">&lt;PubServer&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-131">Nome do servidor de publicação App-V.</span><span class="sxs-lookup"><span data-stu-id="df858-131">Name of the App-V Publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df858-132">&lt;Porta de publicação #&gt;</span><span class="sxs-lookup"><span data-stu-id="df858-132">&lt;Publishing Port#&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-133">Porta para o servidor de publicação App-V, que você definiu quando configurou o Publishing Server.</span><span class="sxs-lookup"><span data-stu-id="df858-133">Port to the App-V Publishing server, which you defined when you configured the Publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df858-134">ClientVersion = &lt; AppvClientVersion&gt;</span><span class="sxs-lookup"><span data-stu-id="df858-134">ClientVersion=&lt;AppvClientVersion&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-135">Versão do cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="df858-135">Version of the App-V client.</span></span> <span data-ttu-id="df858-136">Veja a tabela a seguir para obter o valor correto a ser usado.</span><span class="sxs-lookup"><span data-stu-id="df858-136">Refer to the following table for the correct value to use.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df858-137">ClientOS = &lt; OSStringValue&gt;</span><span class="sxs-lookup"><span data-stu-id="df858-137">ClientOS=&lt;OSStringValue&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-138">Sistema operacional do computador que está executando o cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="df858-138">Operating system of the computer that is running the App-V client.</span></span> <span data-ttu-id="df858-139">Veja a tabela a seguir para obter o valor correto a ser usado.</span><span class="sxs-lookup"><span data-stu-id="df858-139">Refer to the following table for the correct value to use.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p><span data-ttu-id="df858-140">Para obter o nome do servidor de publicação e o número da porta (http:// &lt; PubServer &gt; : &lt; Publishing Port # &gt; ) do cliente App-V, examine a configuração de URL do <strong> cmdlet Get-AppvPublishingServer do </strong> PowerShell.</span><span class="sxs-lookup"><span data-stu-id="df858-140">To get the name of the Publishing server and the port number (http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;) from the App-V Client, look at the URL configuration of the <strong>Get-AppvPublishingServer</strong> PowerShell cmdlet.</span></span></p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64" data-raw-source="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;amp;clientos=WindowsClient_6.2_x64">http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64</a></code></p>
<p><span data-ttu-id="df858-141">No exemplo:</span><span class="sxs-lookup"><span data-stu-id="df858-141">In the example:</span></span></p>
<ul>
<li><p><span data-ttu-id="df858-142">Um Windows Server 2012 R2 chamado "pubsvr01" hospeda o serviço de publicação.</span><span class="sxs-lookup"><span data-stu-id="df858-142">A Windows Server 2012 R2 named “pubsvr01” hosts the Publishing service.</span></span></p></li>
<li><p><span data-ttu-id="df858-143">O cliente Windows é o Windows 8,1 64 bits.</span><span class="sxs-lookup"><span data-stu-id="df858-143">The Windows client is Windows 8.1 64-bit.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df858-144">App-V 5,0 até App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="df858-144">App-V 5.0 through App-V 5.0 SP2</span></span></p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/ </code></p>
<div class="alert">
<strong><span data-ttu-id="df858-145">Observação</span><span class="sxs-lookup"><span data-stu-id="df858-145">Note</span></span></strong><br/><p><strong><span data-ttu-id="df858-146"></strong> <strong> </strong> Só há suporte para ClientVersion e ClientOS no app-v 5,0 SP3 e no app-v 5,1.</span><span class="sxs-lookup"><span data-stu-id="df858-146">ClientVersion</strong> and <strong>ClientOS</strong> are supported only in App-V 5.0 SP3 and App-V 5.1.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="df858-147">Consulte as informações para o App-V 5,0 SP3 e o App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="df858-147">See the information for App-V 5.0 SP3 and App-V 5.1.</span></span></p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718" data-raw-source="http://pubsvr01:2718">http://pubsvr01:2718</a></code></p>
<p><span data-ttu-id="df858-148">No exemplo, um Windows Server 2012 R2 chamado "pubsvr01" hospeda os serviços de gerenciamento e publicação.</span><span class="sxs-lookup"><span data-stu-id="df858-148">In the example, A Windows Server 2012 R2 named “pubsvr01” hosts the Management and Publishing services.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-values-query-pub-meta"></a><span data-ttu-id="df858-149">Consultar valores para a versão e o sistema operacional do cliente</span><span class="sxs-lookup"><span data-stu-id="df858-149">Query values for client operating system and version</span></span>


<span data-ttu-id="df858-150">Na consulta de metadados de publicação, insira os valores de cadeia de caracteres que correspondem ao sistema operacional do cliente e à versão que você está usando.</span><span class="sxs-lookup"><span data-stu-id="df858-150">In your publishing metadata query, enter the string values that correspond to the client operating system and version that you’re using.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="df858-151">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="df858-151">Operating system</span></span></th>
<th align="left"><span data-ttu-id="df858-152">Arquitetura</span><span class="sxs-lookup"><span data-stu-id="df858-152">Architecture</span></span></th>
<th align="left"><span data-ttu-id="df858-153">Valor String da cadeia de caracteres operacional</span><span class="sxs-lookup"><span data-stu-id="df858-153">Operating string string value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df858-154">Windows 10</span><span class="sxs-lookup"><span data-stu-id="df858-154">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-155">64 bits</span><span class="sxs-lookup"><span data-stu-id="df858-155">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-156">WindowsClient_10.0_x64</span><span class="sxs-lookup"><span data-stu-id="df858-156">WindowsClient_10.0_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df858-157">Windows 10</span><span class="sxs-lookup"><span data-stu-id="df858-157">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-158">32 bits</span><span class="sxs-lookup"><span data-stu-id="df858-158">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-159">WindowsClient_10.0_x86</span><span class="sxs-lookup"><span data-stu-id="df858-159">WindowsClient_10.0_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df858-160">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="df858-160">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-161">64 bits</span><span class="sxs-lookup"><span data-stu-id="df858-161">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-162">WindowsClient_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="df858-162">WindowsClient_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df858-163">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="df858-163">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-164">32 bits</span><span class="sxs-lookup"><span data-stu-id="df858-164">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-165">WindowsClient_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="df858-165">WindowsClient_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df858-166">Windows 8</span><span class="sxs-lookup"><span data-stu-id="df858-166">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-167">64 bits</span><span class="sxs-lookup"><span data-stu-id="df858-167">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-168">WindowsClient_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="df858-168">WindowsClient_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df858-169">Windows 8</span><span class="sxs-lookup"><span data-stu-id="df858-169">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-170">32 bits</span><span class="sxs-lookup"><span data-stu-id="df858-170">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-171">WindowsClient_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="df858-171">WindowsClient_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df858-172">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="df858-172">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-173">64 bits</span><span class="sxs-lookup"><span data-stu-id="df858-173">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-174">WindowsServer_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="df858-174">WindowsServer_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df858-175">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="df858-175">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-176">32 bits</span><span class="sxs-lookup"><span data-stu-id="df858-176">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-177">WindowsServer_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="df858-177">WindowsServer_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df858-178">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="df858-178">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-179">64 bits</span><span class="sxs-lookup"><span data-stu-id="df858-179">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-180">WindowsServer_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="df858-180">WindowsServer_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df858-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="df858-181">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-182">32 bits</span><span class="sxs-lookup"><span data-stu-id="df858-182">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-183">WindowsServer_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="df858-183">WindowsServer_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df858-184">Windows 7</span><span class="sxs-lookup"><span data-stu-id="df858-184">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-185">64 bits</span><span class="sxs-lookup"><span data-stu-id="df858-185">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-186">WindowsClient_6.1_x64</span><span class="sxs-lookup"><span data-stu-id="df858-186">WindowsClient_6.1_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df858-187">Windows 7</span><span class="sxs-lookup"><span data-stu-id="df858-187">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-188">32 bits</span><span class="sxs-lookup"><span data-stu-id="df858-188">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-189">WindowsClient_6.1_x86</span><span class="sxs-lookup"><span data-stu-id="df858-189">WindowsClient_6.1_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="df858-190">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="df858-190">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-191">64 bits</span><span class="sxs-lookup"><span data-stu-id="df858-191">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-192">WindowsServer_6.1_x64</span><span class="sxs-lookup"><span data-stu-id="df858-192">WindowsServer_6.1_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="df858-193">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="df858-193">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-194">32 bits</span><span class="sxs-lookup"><span data-stu-id="df858-194">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="df858-195">WindowsServer_6.1_x86</span><span class="sxs-lookup"><span data-stu-id="df858-195">WindowsServer_6.1_x86</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-whatis-pub-metadata"></a><span data-ttu-id="df858-196">Definição de metadados de publicação</span><span class="sxs-lookup"><span data-stu-id="df858-196">Definition of publishing metadata</span></span>


<span data-ttu-id="df858-197">Quando pacotes são publicados em um computador que está executando o cliente App-V, os metadados são enviados para esse computador indicando quais pacotes e grupos de conexão estão sendo publicados.</span><span class="sxs-lookup"><span data-stu-id="df858-197">When packages are published to a computer that is running the App-V client, metadata is sent to that computer indicating which packages and connection groups are being published.</span></span> <span data-ttu-id="df858-198">O cliente App-V faz duas solicitações separadas para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="df858-198">The App-V Client makes two separate requests for the following:</span></span>

-   <span data-ttu-id="df858-199">Pacotes e grupos de conexão que são habilitados para o computador cliente.</span><span class="sxs-lookup"><span data-stu-id="df858-199">Packages and connection groups that are entitled to the client computer.</span></span>

-   <span data-ttu-id="df858-200">Pacotes e grupos de conexão que são habilitados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="df858-200">Packages and connection groups that are entitled to the current user.</span></span>

<span data-ttu-id="df858-201">O servidor de publicação se comunica com o servidor de gerenciamento para determinar quais pacotes e grupos de conexão estão disponíveis para o solicitante.</span><span class="sxs-lookup"><span data-stu-id="df858-201">The Publishing server communicates with the Management server to determine which packages and connection groups are available to the requester.</span></span> <span data-ttu-id="df858-202">O servidor de publicação deve ser registrado com o servidor de gerenciamento para que os metadados sejam gerados.</span><span class="sxs-lookup"><span data-stu-id="df858-202">The Publishing server must be registered with the Management server in order for the metadata to be generated.</span></span>

<span data-ttu-id="df858-203">Você pode exibir os metadados de cada solicitação em um navegador da Internet usando uma consulta que se encontra no contexto do usuário ou computador específico.</span><span class="sxs-lookup"><span data-stu-id="df858-203">You can view the metadata for each request in an Internet browser by using a query that is in the context of the specific user or computer.</span></span>






## <span data-ttu-id="df858-204">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="df858-204">Related topics</span></span>


[<span data-ttu-id="df858-205">Referência técnica para o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="df858-205">Technical Reference for App-V 5.1</span></span>](technical-reference-for-app-v-51.md)









