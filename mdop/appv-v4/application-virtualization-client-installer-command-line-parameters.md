---
title: Parâmetros de linha de comando do instalador do Application Virtualization Client
description: Parâmetros de linha de comando do instalador do Application Virtualization Client
author: dansimp
ms.assetid: 508fa404-52a5-4919-8788-2a3dfb00639b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 911d333c80060c1881c96430c1d2d0516b6a4855
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797581"
---
# <span data-ttu-id="61e1f-103">Parâmetros de linha de comando do instalador do Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="61e1f-103">Application Virtualization Client Installer Command-Line Parameters</span></span>


<span data-ttu-id="61e1f-104">A tabela a seguir lista todos os parâmetros de linha de comando disponíveis do instalador do cliente do Microsoft Application Virtualization, seus valores e uma breve descrição de cada parâmetro.</span><span class="sxs-lookup"><span data-stu-id="61e1f-104">The following table lists all available Microsoft Application Virtualization Client installer command-line parameters, their values, and a brief description of each parameter.</span></span> <span data-ttu-id="61e1f-105">Os parâmetros diferenciam maiúsculas de minúsculas e devem ser inseridos como letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="61e1f-105">Parameters are case-sensitive and must be entered as all-uppercase letters.</span></span> <span data-ttu-id="61e1f-106">Todos os valores de parâmetro devem estar entre aspas duplas.</span><span class="sxs-lookup"><span data-stu-id="61e1f-106">All parameter values must be enclosed in double quotes.</span></span>

**<span data-ttu-id="61e1f-107">Observação</span><span class="sxs-lookup"><span data-stu-id="61e1f-107">Note</span></span>**  
-   <span data-ttu-id="61e1f-108">Para o App-V versão 4,6, os parâmetros de linha de comando não podem ser usados durante uma atualização de cliente.</span><span class="sxs-lookup"><span data-stu-id="61e1f-108">For App-V version 4.6, command-line parameters cannot be used during a client upgrade.</span></span>

-   <span data-ttu-id="61e1f-109">Os parâmetros *SWICACHESIZE* e *MINFREESPACEMB* não podem ser combinados na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="61e1f-109">The *SWICACHESIZE* and *MINFREESPACEMB* parameters cannot be combined on the command line.</span></span> <span data-ttu-id="61e1f-110">Se ambos forem usados, o parâmetro *SWICACHESIZE* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="61e1f-110">If both are used, the *SWICACHESIZE* parameter will be ignored.</span></span>



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="61e1f-111">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="61e1f-111">Parameter</span></span></th>
<th align="left"><span data-ttu-id="61e1f-112">Valores</span><span class="sxs-lookup"><span data-stu-id="61e1f-112">Values</span></span></th>
<th align="left"><span data-ttu-id="61e1f-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="61e1f-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="61e1f-114">ALLOWINDEPENDENTFILESTREAMING</span><span class="sxs-lookup"><span data-stu-id="61e1f-114">ALLOWINDEPENDENTFILESTREAMING</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-115">TRUE</span><span class="sxs-lookup"><span data-stu-id="61e1f-115">TRUE</span></span></p>
<p><span data-ttu-id="61e1f-116">FALSE</span><span class="sxs-lookup"><span data-stu-id="61e1f-116">FALSE</span></span></p></td>
<td align="left"><p><span data-ttu-id="61e1f-117">Indica se o streaming do arquivo será habilitado independentemente de como o cliente foi configurado com o <em> parâmetro APPLICATIONSOURCEROOT </em> .</span><span class="sxs-lookup"><span data-stu-id="61e1f-117">Indicates whether streaming from file will be enabled regardless of how the client has been configured with the <em>APPLICATIONSOURCEROOT</em> parameter.</span></span> <span data-ttu-id="61e1f-118">Se definido como FALSE, o transporte não habilitará o streaming de arquivos, mesmo que o parâmetro OSD HREF ou <em> APPLICATIONSOURCEROOT </em> contenha um caminho de arquivo.</span><span class="sxs-lookup"><span data-stu-id="61e1f-118">If set to FALSE, the transport will not enable streaming from files even if the OSD HREF or the <em>APPLICATIONSOURCEROOT</em> parameter contains a file path.</span></span></p>
<p><span data-ttu-id="61e1f-119">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="61e1f-119">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="61e1f-120">TRUE – o aplicativo implantado manualmente pode ser carregado do disco.</span><span class="sxs-lookup"><span data-stu-id="61e1f-120">TRUE—Manually deployed application may be loaded from disk.</span></span></p></li>
<li><p><span data-ttu-id="61e1f-121">FALSE — todos os aplicativos devem vir do servidor de fluxo de origem.</span><span class="sxs-lookup"><span data-stu-id="61e1f-121">FALSE—All applications must come from source streaming server.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="61e1f-122">APPLICATIONSOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="61e1f-122">APPLICATIONSOURCEROOT</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-123"><em>URL RTSP:// </em> (para distribuição de pacote dinâmico)</span><span class="sxs-lookup"><span data-stu-id="61e1f-123">RTSP:// <em>URL</em> (for dynamic package delivery)</span></span></p>
<p><span data-ttu-id="61e1f-124"><em>URL file:// </em> ou <em> UNC </em> (para carga da entrega de pacotes de arquivos)</span><span class="sxs-lookup"><span data-stu-id="61e1f-124">File:// <em>URL</em> or <em>UNC</em> (for load from file package delivery)</span></span></p></td>
<td align="left"><p><span data-ttu-id="61e1f-125">Para habilitar um administrador ou um sistema de distribuição de software eletrônico para garantir que o carregamento do aplicativo seja executado em conformidade com o esquema de gerenciamento de topologia, permite uma substituição da CODEBASE do OSD para o elemento HREF do aplicativo (o local de origem).</span><span class="sxs-lookup"><span data-stu-id="61e1f-125">To enable an administrator or an electronic software distribution system to ensure that application loading is performed in compliance with the topology management scheme, allows an override of the OSD CODEBASE for the application HREF element (the source location).</span></span> <span data-ttu-id="61e1f-126">Se o valor for "", que é o valor padrão, as configurações de arquivo OSD existentes serão usadas.</span><span class="sxs-lookup"><span data-stu-id="61e1f-126">If the value is “”, which is the default value, the existing OSD file settings are used.</span></span></p>
<p><span data-ttu-id="61e1f-127">Uma URL tem várias partes:</span><span class="sxs-lookup"><span data-stu-id="61e1f-127">A URL has several parts:</span></span></p>
<p><span data-ttu-id="61e1f-128">&lt;protocolo &gt; :// &lt; servidor &gt; : &lt; caminho da porta &gt; / &lt; &gt; / &lt; ? consulta &gt; &lt; #fragment&gt;</span><span class="sxs-lookup"><span data-stu-id="61e1f-128">&lt;protocol&gt;://&lt;server&gt;:&lt;port&gt;/&lt;path&gt;/&lt;?query&gt;&lt;#fragment&gt;</span></span></p>
<p><span data-ttu-id="61e1f-129">Um caminho UNC tem três partes:</span><span class="sxs-lookup"><span data-stu-id="61e1f-129">A UNC path has three parts:</span></span></p>
<p><span data-ttu-id="61e1f-130">&amp;lt; ComputerName; ComputerName &gt; &amp; ; Share Folder &gt; &amp; lt; Resource&gt;</span><span class="sxs-lookup"><span data-stu-id="61e1f-130">&amp;lt;computername&gt;&amp;lt;share folder&gt;&amp;lt;resource&gt;</span></span></p>
<p><span data-ttu-id="61e1f-131">Se o <em> </em> parâmetro APPLICATIONSOURCEROOT for especificado em um cliente, o cliente irá romper a URL ou caminho UNC de um arquivo OSD em suas partes constituintes e substituir as seções OSD pelas <em> seções APPLICATIONSOURCEROOT correspondentes </em> .</span><span class="sxs-lookup"><span data-stu-id="61e1f-131">If the <em>APPLICATIONSOURCEROOT</em> parameter is specified on a client, the client will break the URL or UNC path from an OSD file into its constituent parts and replace the OSD sections with the corresponding <em>APPLICATIONSOURCEROOT</em> sections.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="61e1f-132">Importante</span><span class="sxs-lookup"><span data-stu-id="61e1f-132">Important</span></span></strong><br/><p><span data-ttu-id="61e1f-133">Certifique-se de usar o formato correto ao usar file://com um caminho UNC.</span><span class="sxs-lookup"><span data-stu-id="61e1f-133">Be sure to use the correct format when using file:// with a UNC path.</span></span> <span data-ttu-id="61e1f-134">O formato correto é file:// &amp; lt; Server &gt; &amp; lt; Server lt; share &gt; .</span><span class="sxs-lookup"><span data-stu-id="61e1f-134">The correct format is file://&amp;lt;server&gt;&amp;lt;share&gt;.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="61e1f-135">ICONSOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="61e1f-135">ICONSOURCEROOT</span></span></em></p></td>
<td align="left"><p><em><span data-ttu-id="61e1f-136">UNC</span><span class="sxs-lookup"><span data-stu-id="61e1f-136">UNC</span></span></em></p>
<p><span data-ttu-id="61e1f-137">URL <em> http:// </em> ou <em> URL https://</span><span class="sxs-lookup"><span data-stu-id="61e1f-137">HTTP://<em>URL</em> or HTTPS://<em>URL</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-138">Permite que um administrador especifique um local de origem para a recuperação de ícone para um pacote de aplicativo sequenciado durante a publicação.</span><span class="sxs-lookup"><span data-stu-id="61e1f-138">Enables an administrator to specify a source location for icon retrieval for a sequenced application package during publication.</span></span> <span data-ttu-id="61e1f-139">As raízes de origem dos ícones dão suporte a caminhos e URLs UNC (HTTP ou HTTPS).</span><span class="sxs-lookup"><span data-stu-id="61e1f-139">Icon source roots support UNC paths and URLs (HTTP or HTTPS).</span></span> <span data-ttu-id="61e1f-140">Se o valor for "", que é o valor padrão, as configurações de arquivo OSD existentes serão usadas.</span><span class="sxs-lookup"><span data-stu-id="61e1f-140">If the value is “”, which is the default value, the existing OSD file settings are used.</span></span></p>
<p><span data-ttu-id="61e1f-141">Uma URL tem várias partes:</span><span class="sxs-lookup"><span data-stu-id="61e1f-141">A URL has several parts:</span></span></p>
<p><span data-ttu-id="61e1f-142">&lt;protocolo &gt; :// &lt; servidor &gt; : &lt; caminho da porta &gt; / &lt; &gt; / &lt; ? consulta &gt; &lt; #fragment&gt;</span><span class="sxs-lookup"><span data-stu-id="61e1f-142">&lt;protocol&gt;://&lt;server&gt;:&lt;port&gt;/&lt;path&gt;/&lt;?query&gt;&lt;#fragment&gt;</span></span></p>
<p><span data-ttu-id="61e1f-143">Um caminho UNC tem três partes:</span><span class="sxs-lookup"><span data-stu-id="61e1f-143">A UNC path has three parts:</span></span></p>
<p><span data-ttu-id="61e1f-144">&amp;lt; ComputerName; ComputerName &gt; &amp; ; Share Folder &gt; &amp; lt; Resource&gt;</span><span class="sxs-lookup"><span data-stu-id="61e1f-144">&amp;lt;computername&gt;&amp;lt;share folder&gt;&amp;lt;resource&gt;</span></span></p>
<div class="alert">
<strong><span data-ttu-id="61e1f-145">Importante</span><span class="sxs-lookup"><span data-stu-id="61e1f-145">Important</span></span></strong><br/><p><span data-ttu-id="61e1f-146">Certifique-se de usar o formato correto ao usar um caminho UNC.</span><span class="sxs-lookup"><span data-stu-id="61e1f-146">Be sure to use the correct format when using a UNC path.</span></span> <span data-ttu-id="61e1f-147">Os formatos aceitáveis são &amp; lt; Server &gt; &amp; lt; share &gt; ou &lt; Letter Drive &gt; : &amp; lt; Folder &gt; .</span><span class="sxs-lookup"><span data-stu-id="61e1f-147">Acceptable formats are &amp;lt;server&gt;&amp;lt;share&gt; or &lt;drive letter&gt;:&amp;lt;folder&gt;.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="61e1f-148">OSDSOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="61e1f-148">OSDSOURCEROOT</span></span></em></p></td>
<td align="left"><p><em><span data-ttu-id="61e1f-149">UNC</span><span class="sxs-lookup"><span data-stu-id="61e1f-149">UNC</span></span></em></p>
<p><span data-ttu-id="61e1f-150">URL <em> http:// </em> ou <em> URL https://</span><span class="sxs-lookup"><span data-stu-id="61e1f-150">HTTP://<em>URL</em> or HTTPS://<em>URL</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-151">Permite que um administrador especifique um local de origem para a recuperação de arquivo OSD para um pacote de aplicativo durante a publicação.</span><span class="sxs-lookup"><span data-stu-id="61e1f-151">Enables an administrator to specify a source location for OSD file retrieval for an application package during publication.</span></span> <span data-ttu-id="61e1f-152">As raízes de origem do OSD dão suporte a caminhos e URLs UNC (HTTP ou HTTPS).</span><span class="sxs-lookup"><span data-stu-id="61e1f-152">OSD source roots support UNC paths and URLs (HTTP or HTTPS).</span></span> <span data-ttu-id="61e1f-153">Se o valor for "", que é o valor padrão, as configurações de arquivo OSD existentes serão usadas.</span><span class="sxs-lookup"><span data-stu-id="61e1f-153">If the value is “”, which is the default value, the existing OSD file settings are used.</span></span></p>
<p><span data-ttu-id="61e1f-154">Uma URL tem várias partes:</span><span class="sxs-lookup"><span data-stu-id="61e1f-154">A URL has several parts:</span></span></p>
<p><span data-ttu-id="61e1f-155">&lt;protocolo &gt; :// &lt; servidor &gt; : &lt; caminho da porta &gt; / &lt; &gt; / &lt; ? consulta &gt; &lt; #fragment&gt;</span><span class="sxs-lookup"><span data-stu-id="61e1f-155">&lt;protocol&gt;://&lt;server&gt;:&lt;port&gt;/&lt;path&gt;/&lt;?query&gt;&lt;#fragment&gt;</span></span></p>
<p><span data-ttu-id="61e1f-156">Um caminho UNC tem três partes:</span><span class="sxs-lookup"><span data-stu-id="61e1f-156">A UNC path has three parts:</span></span></p>
<p><span data-ttu-id="61e1f-157">&amp;lt; ComputerName; ComputerName &gt; &amp; ; Share Folder &gt; &amp; lt; Resource&gt;</span><span class="sxs-lookup"><span data-stu-id="61e1f-157">&amp;lt;computername&gt;&amp;lt;share folder&gt;&amp;lt;resource&gt;</span></span></p>
<div class="alert">
<strong><span data-ttu-id="61e1f-158">Importante</span><span class="sxs-lookup"><span data-stu-id="61e1f-158">Important</span></span></strong><br/><p><span data-ttu-id="61e1f-159">Certifique-se de usar o formato correto ao usar um caminho UNC.</span><span class="sxs-lookup"><span data-stu-id="61e1f-159">Be sure to use the correct format when using a UNC path.</span></span> <span data-ttu-id="61e1f-160">Os formatos aceitáveis são &amp; lt; Server &gt; &amp; lt; share &gt; ou &lt; Letter Drive &gt; : &amp; lt; Folder &gt; .</span><span class="sxs-lookup"><span data-stu-id="61e1f-160">Acceptable formats are &amp;lt;server&gt;&amp;lt;share&gt; or &lt;drive letter&gt;:&amp;lt;folder&gt;.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="61e1f-161">AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="61e1f-161">AUTOLOADONLOGIN</span></span></em></p>
<p><em><span data-ttu-id="61e1f-162">AUTOLOADONLAUNCH</span><span class="sxs-lookup"><span data-stu-id="61e1f-162">AUTOLOADONLAUNCH</span></span></em></p>
<p><em><span data-ttu-id="61e1f-163">AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="61e1f-163">AUTOLOADONREFRESH</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-164">[0 | 1]</span><span class="sxs-lookup"><span data-stu-id="61e1f-164">[0|1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="61e1f-165">Os gatilhos AutoLoad que definem os eventos que iniciam o carregamento automático de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="61e1f-165">The AutoLoad triggers that define the events that initiate auto-loading of applications.</span></span> <span data-ttu-id="61e1f-166">AutoLoad usa implicitamente o streaming em segundo plano para permitir que o aplicativo seja totalmente carregado no cache.</span><span class="sxs-lookup"><span data-stu-id="61e1f-166">AutoLoad implicitly uses background streaming to enable the application to be fully loaded into cache.</span></span></p>
<p><span data-ttu-id="61e1f-167">O bloco de recursos principal será carregado o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="61e1f-167">The primary feature block will be loaded as quickly as possible.</span></span> <span data-ttu-id="61e1f-168">Os blocos de recursos restantes serão carregados em segundo plano para permitir operações em primeiro plano, como interação do usuário com aplicativos, para ter prioridade e fornecer desempenho ideal.</span><span class="sxs-lookup"><span data-stu-id="61e1f-168">Remaining feature blocks will be loaded in the background to enable foreground operations, such as user interaction with applications, to take priority and provide optimal performance.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="61e1f-169">Observação</span><span class="sxs-lookup"><span data-stu-id="61e1f-169">Note</span></span></strong><br/><p><span data-ttu-id="61e1f-170">O <em> </em> parâmetro AUTOLOADTARGET determina quais aplicativos são carregados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="61e1f-170">The <em>AUTOLOADTARGET</em> parameter determines which applications are auto-loaded.</span></span> <span data-ttu-id="61e1f-171">Por padrão, os pacotes que foram usados são carregados automaticamente, a menos que <em> AUTOLOADTARGET </em> esteja definido.</span><span class="sxs-lookup"><span data-stu-id="61e1f-171">By default, packages that have been used are auto-loaded unless <em>AUTOLOADTARGET</em> is set.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="61e1f-172">Cada parâmetro afeta o comportamento de carregamento da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="61e1f-172">Each parameter affects loading behavior as follows:</span></span></p>
<ul>
<li><p><em><span data-ttu-id="61e1f-173">AUTOLOADONLOGIN </em> – o carregamento é iniciado quando o usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="61e1f-173">AUTOLOADONLOGIN</em>—Loading starts when the user logs in.</span></span></p></li>
<li><p><em><span data-ttu-id="61e1f-174">AUTOLOADONLAUNCH </em> – o carregamento é iniciado quando o usuário inicia um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="61e1f-174">AUTOLOADONLAUNCH</em>—Loading starts when the user starts an application.</span></span></p></li>
<li><p><em><span data-ttu-id="61e1f-175">AUTOLOADONREFRESH </em> – o carregamento começa quando ocorre uma atualização de publicação.</span><span class="sxs-lookup"><span data-stu-id="61e1f-175">AUTOLOADONREFRESH</em>—Loading starts when a publishing refresh occurs.</span></span></p></li>
</ul>
<p><span data-ttu-id="61e1f-176">Os três valores podem ser combinados.</span><span class="sxs-lookup"><span data-stu-id="61e1f-176">The three values can be combined.</span></span> <span data-ttu-id="61e1f-177">No exemplo a seguir, os gatilhos de AutoLoad estão habilitados no momento da conexão do usuário e quando ocorre uma atualização de publicação:</span><span class="sxs-lookup"><span data-stu-id="61e1f-177">In the following example, AutoLoad triggers are enabled both at user login and when publishing refresh occurs:</span></span></p>
<p><em><span data-ttu-id="61e1f-178">AUTOLOADONLOGIN AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="61e1f-178">AUTOLOADONLOGIN AUTOLOADONREFRESH</span></span></em></p>
<div class="alert">
<strong><span data-ttu-id="61e1f-179">Observação</span><span class="sxs-lookup"><span data-stu-id="61e1f-179">Note</span></span></strong><br/><p><span data-ttu-id="61e1f-180">Se o cliente estiver configurado com esses valores na primeira instalação, a função Autocarregar não será acionada até a próxima vez que o usuário fizer logoff e logon novamente.</span><span class="sxs-lookup"><span data-stu-id="61e1f-180">If the client is configured with these values at first install, Autoload will not be triggered until the next time the user logs off and logs back on.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="61e1f-181">AUTOLOADTARGET</span><span class="sxs-lookup"><span data-stu-id="61e1f-181">AUTOLOADTARGET</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-182">NENHUMA</span><span class="sxs-lookup"><span data-stu-id="61e1f-182">NONE</span></span></p>
<p><span data-ttu-id="61e1f-183">TODO</span><span class="sxs-lookup"><span data-stu-id="61e1f-183">ALL</span></span></p>
<p><span data-ttu-id="61e1f-184">PREVUSED</span><span class="sxs-lookup"><span data-stu-id="61e1f-184">PREVUSED</span></span></p></td>
<td align="left"><p><span data-ttu-id="61e1f-185">Indica o que será carregado automaticamente quando um determinado disparador de autocarregamento ocorrer.</span><span class="sxs-lookup"><span data-stu-id="61e1f-185">Indicates what will be auto-loaded when any given AutoLoad triggers occur.</span></span></p>
<p><span data-ttu-id="61e1f-186">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="61e1f-186">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="61e1f-187">NONE — sem carregamento automático, independentemente de quais gatilhos podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="61e1f-187">NONE—No auto-loading, regardless of what triggers might be set.</span></span></p></li>
<li><p><span data-ttu-id="61e1f-188">Tudo — se qualquer gatilho de autocarregamento estiver habilitado, todos os pacotes serão carregados automaticamente, independentemente de terem sido iniciados.</span><span class="sxs-lookup"><span data-stu-id="61e1f-188">ALL—If any AutoLoad trigger is enabled, all packages are automatically loaded, whether or not they have ever been launched.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="61e1f-189">Observação</span><span class="sxs-lookup"><span data-stu-id="61e1f-189">Note</span></span></strong><br/><p><span data-ttu-id="61e1f-190">Essa configuração é definida para pacotes individuais usando o SFTMIME <strong> Adicionar pacote </strong> e <strong> Configurar comandos de pacote </strong> .</span><span class="sxs-lookup"><span data-stu-id="61e1f-190">This setting is configured for individual packages by using the SFTMIME <strong>ADD PACKAGE</strong> and <strong>CONFIGURE PACKAGE</strong> commands.</span></span> <span data-ttu-id="61e1f-191">Para obter mais informações sobre esses comandos, consulte <a href="sftmime--command-reference.md" data-raw-source="[SFTMIME Command Reference](sftmime--command-reference.md)"> referência de comandos SFTMIME </a> .</span><span class="sxs-lookup"><span data-stu-id="61e1f-191">For more information about these commands, see <a href="sftmime--command-reference.md" data-raw-source="[SFTMIME Command Reference](sftmime--command-reference.md)">SFTMIME Command Reference</a>.</span></span></p>
</div>
<div>

</div></li>
<li><p><span data-ttu-id="61e1f-192">PREVUSED — se qualquer gatilho de AutoLoad estiver habilitado, carregue somente os pacotes nos quais pelo menos um aplicativo do pacote tenha sido usado anteriormente (ou seja, iniciado ou previamente armazenado em cache).</span><span class="sxs-lookup"><span data-stu-id="61e1f-192">PREVUSED—If any AutoLoad trigger is enabled, load only the packages where at least one application in the package has been previously used (that is, launched or precached).</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="61e1f-193">Observação</span><span class="sxs-lookup"><span data-stu-id="61e1f-193">Note</span></span></strong><br/><p><span data-ttu-id="61e1f-194">Ao instalar o cliente App-V para usar um cache somente leitura (por exemplo, como uma implementação de servidor VDI), você deve definir o <em> </em> parâmetro AUTOLOADTARGET como None para impedir que o cliente tente atualizar aplicativos no cache somente leitura.</span><span class="sxs-lookup"><span data-stu-id="61e1f-194">When you install the App-V client to use a read-only cache, (for example, as a VDI server implementation), you must set the <em>AUTOLOADTARGET</em> parameter to NONE to prevent the client from trying to update applications in the read-only cache.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="61e1f-195">DOTIMEOUTMINUTES</span><span class="sxs-lookup"><span data-stu-id="61e1f-195">DOTIMEOUTMINUTES</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-196">29600 (padrão)</span><span class="sxs-lookup"><span data-stu-id="61e1f-196">29600 (default)</span></span></p>
<p><span data-ttu-id="61e1f-197">1 – 1439998560 minutos (intervalo)</span><span class="sxs-lookup"><span data-stu-id="61e1f-197">1–1439998560 minutes (range)</span></span></p></td>
<td align="left"><p><span data-ttu-id="61e1f-198">Indica quantos minutos um aplicativo pode ser usado em uma operação desconectada.</span><span class="sxs-lookup"><span data-stu-id="61e1f-198">Indicates how many minutes an application may be used in disconnected operation.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="61e1f-199">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="61e1f-199">INSTALLDIR</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-200">&lt;caminho&gt;</span><span class="sxs-lookup"><span data-stu-id="61e1f-200">&lt;pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="61e1f-201">Especifica o diretório de instalação do cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="61e1f-201">Specifies the installation directory of the App-V Client.</span></span></p>
<p><span data-ttu-id="61e1f-202">Exemplo: INSTALLDIR = &quot; C:\Program Files\Microsoft Application Virtualization Client&quot;</span><span class="sxs-lookup"><span data-stu-id="61e1f-202">Example: INSTALLDIR=&quot;C:\Program Files\Microsoft Application Virtualization Client&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="61e1f-203">Opti</span><span class="sxs-lookup"><span data-stu-id="61e1f-203">OPTIN</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-204">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="61e1f-204">“TRUE”</span></span></p>
<p><span data-ttu-id="61e1f-205">“”</span><span class="sxs-lookup"><span data-stu-id="61e1f-205">“”</span></span></p></td>
<td align="left"><p><span data-ttu-id="61e1f-206">Os componentes de cliente do Microsoft Application Virtualization serão atualizáveis por meio do Microsoft Update quando as atualizações forem disponibilizadas para o público em geral.</span><span class="sxs-lookup"><span data-stu-id="61e1f-206">Microsoft Application Virtualization Client components will be upgradable through Microsoft Update when updates are made available to the general public.</span></span> <span data-ttu-id="61e1f-207">O Microsoft Update Agent instalado em sistemas operacionais Windows exige que um usuário explicitamente opte por usar o serviço.</span><span class="sxs-lookup"><span data-stu-id="61e1f-207">The Microsoft Update Agent installed on Windows operating systems requires a user to explicitly opt-in to use the service.</span></span> <span data-ttu-id="61e1f-208">Esse consentimento é necessário apenas uma vez para todos os aplicativos no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="61e1f-208">This opt-in is required only one time for all applications on the device.</span></span> <span data-ttu-id="61e1f-209">Se você já tiver optado pelo Microsoft Update, os componentes do Microsoft Application Virtualization no dispositivo utilizarão automaticamente o serviço.</span><span class="sxs-lookup"><span data-stu-id="61e1f-209">If you have already opted into Microsoft Update, the Microsoft Application Virtualization components on the device will automatically take advantage of the service.</span></span></p>
<p><span data-ttu-id="61e1f-210">Para a instalação na linha de comando, o uso do Microsoft Update é, por padrão, recusado (a menos que um aplicativo anterior já tenha habilitado o dispositivo para ser incluído) devido ao requisito para a aceitação manual do Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="61e1f-210">For command-line installation, use of Microsoft Update is by default opt-out (unless a previous application already enabled the device to be opted in) due to the requirement for manually opting into Microsoft Update.</span></span> <span data-ttu-id="61e1f-211">Portanto, optar por não deve ser explícito para instalações de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="61e1f-211">Therefore, opting in must be explicit for command-line installations.</span></span> <span data-ttu-id="61e1f-212">Definir o parâmetro de linha de comando <em> optid </em> como true força a aceitação da aceitação do Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="61e1f-212">Setting the command-line parameter <em>OPTIN</em> to TRUE forces the Microsoft Update opt-in to be set.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="61e1f-213">REQUIREAUTHORIZATIONIFCACHED</span><span class="sxs-lookup"><span data-stu-id="61e1f-213">REQUIREAUTHORIZATIONIFCACHED</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-214">TRUE</span><span class="sxs-lookup"><span data-stu-id="61e1f-214">TRUE</span></span></p>
<p><span data-ttu-id="61e1f-215">FALSE</span><span class="sxs-lookup"><span data-stu-id="61e1f-215">FALSE</span></span></p></td>
<td align="left"><p><span data-ttu-id="61e1f-216">Indica se a autorização é sempre necessária, se um aplicativo já está em cache.</span><span class="sxs-lookup"><span data-stu-id="61e1f-216">Indicates whether authorization is always required, whether or not an application is already in cache.</span></span></p>
<p><span data-ttu-id="61e1f-217">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="61e1f-217">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="61e1f-218">TRUE — o aplicativo sempre deve ser autorizado na inicialização.</span><span class="sxs-lookup"><span data-stu-id="61e1f-218">TRUE—Application always must be authorized at startup.</span></span> <span data-ttu-id="61e1f-219">Para aplicativos de fluxo RTSP, o token de autorização do usuário é enviado ao servidor para autorização.</span><span class="sxs-lookup"><span data-stu-id="61e1f-219">For RTSP streamed applications, the user authorization token is sent to the server for authorization.</span></span> <span data-ttu-id="61e1f-220">Para aplicativos baseados em arquivos, as ACLs de arquivo determinam se um usuário pode acessar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="61e1f-220">For file-based applications, file ACLs dictate whether a user may access the application.</span></span></p></li>
<li><p><span data-ttu-id="61e1f-221">FALSE — sempre tente se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="61e1f-221">FALSE—Always try to connect to the server.</span></span> <span data-ttu-id="61e1f-222">Se não for possível estabelecer uma conexão com o servidor, o cliente ainda permite que o usuário inicie um aplicativo que tenha sido carregado anteriormente no cache.</span><span class="sxs-lookup"><span data-stu-id="61e1f-222">If a connection to the server cannot be established, the client still allows the user to launch an application that has previously been loaded into cache.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="61e1f-223">SWICACHESIZE</span><span class="sxs-lookup"><span data-stu-id="61e1f-223">SWICACHESIZE</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-224">Tamanho do cache em MB</span><span class="sxs-lookup"><span data-stu-id="61e1f-224">Cache size in MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="61e1f-225">Especifica o tamanho em megabytes do cache do cliente.</span><span class="sxs-lookup"><span data-stu-id="61e1f-225">Specifies the size in megabytes of the client cache.</span></span> <span data-ttu-id="61e1f-226">O tamanho padrão é de 4096 MB, e o tamanho máximo é 1.048.576 MB (1 TB).</span><span class="sxs-lookup"><span data-stu-id="61e1f-226">The default size is 4096 MB, and the maximum size is 1,048,576 MB (1 TB).</span></span> <span data-ttu-id="61e1f-227">O sistema verifica o espaço disponível no momento da instalação, mas o espaço não é reservado.</span><span class="sxs-lookup"><span data-stu-id="61e1f-227">The system checks for the available space at installation time, but the space is not reserved.</span></span></p>
<p><span data-ttu-id="61e1f-228">Exemplo: <strong> SWICACHESIZE = &quot; 1024&quot;</span><span class="sxs-lookup"><span data-stu-id="61e1f-228">Example: <strong>SWICACHESIZE=&quot;1024&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="61e1f-229">SWIPUBSVRDISPLAY</span><span class="sxs-lookup"><span data-stu-id="61e1f-229">SWIPUBSVRDISPLAY</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-230">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="61e1f-230">Display name</span></span></p></td>
<td align="left"><p><span data-ttu-id="61e1f-231">Especifica o nome exibido do servidor de publicação; obrigatório quando o <em> SWIPUBSVRHOST </em> é usado.</span><span class="sxs-lookup"><span data-stu-id="61e1f-231">Specifies the displayed name of the publishing server; required when <em>SWIPUBSVRHOST</em> is used.</span></span></p>
<p><span data-ttu-id="61e1f-232">Exemplo: <strong> SWIPUBSVRDISPLAY = &quot; ambiente de produção&quot;</span><span class="sxs-lookup"><span data-stu-id="61e1f-232">Example: <strong>SWIPUBSVRDISPLAY=&quot;PRODUCTION ENVIRONMENT&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="61e1f-233">SWIPUBSVRTYPE</span><span class="sxs-lookup"><span data-stu-id="61e1f-233">SWIPUBSVRTYPE</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-234">[HTTP | RTSP</span><span class="sxs-lookup"><span data-stu-id="61e1f-234">[HTTP|RTSP]</span></span></p></td>
<td align="left"><p><span data-ttu-id="61e1f-235">Especifica o tipo de servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="61e1f-235">Specifies the publishing server type.</span></span> <span data-ttu-id="61e1f-236">O tipo de servidor padrão é o Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="61e1f-236">The default server type is Application Virtualization Server.</span></span> <span data-ttu-id="61e1f-237">A <strong> </strong> opção/Secure não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="61e1f-237">The <strong>/secure</strong> switch is not case sensitive.</span></span></p>
<ul>
<li><p><span data-ttu-id="61e1f-238">HTTP – servidor HTTP padrão</span><span class="sxs-lookup"><span data-stu-id="61e1f-238">HTTP—Standard HTTP Server</span></span></p></li>
<li><p><span data-ttu-id="61e1f-239">HTTP <strong> /Secure </strong> — servidor http de segurança aprimorada</span><span class="sxs-lookup"><span data-stu-id="61e1f-239">HTTP <strong>/secure</strong>—Enhanced Security HTTP Server</span></span></p></li>
<li><p><span data-ttu-id="61e1f-240">RTSP — servidor de virtualização de aplicativos</span><span class="sxs-lookup"><span data-stu-id="61e1f-240">RTSP—Application Virtualization Server</span></span></p></li>
<li><p><span data-ttu-id="61e1f-241">RTSP <strong> /Secure </strong> — servidor de virtualização do aplicativo de segurança aprimorado</span><span class="sxs-lookup"><span data-stu-id="61e1f-241">RTSP <strong>/secure</strong>—Enhanced Security Application Virtualization Server</span></span></p></li>
</ul>
<p><span data-ttu-id="61e1f-242">Exemplo: <strong> SWIPUBSVRTYPE = &quot; http/Secure&quot;</span><span class="sxs-lookup"><span data-stu-id="61e1f-242">Example: <strong>SWIPUBSVRTYPE=&quot;HTTP /secure&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="61e1f-243">SWIPUBSVRHOST</span><span class="sxs-lookup"><span data-stu-id="61e1f-243">SWIPUBSVRHOST</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-244">Endereço IP | nome do host</span><span class="sxs-lookup"><span data-stu-id="61e1f-244">IP address|host name</span></span></p></td>
<td align="left"><p><span data-ttu-id="61e1f-245">Especifica o endereço IP do servidor de virtualização de aplicativos ou um nome de host do servidor que é resolvido para o endereço IP&#39;s do servidor; obrigatório quando o <em> SWIPUBSVRDISPLAY </em> é usado.</span><span class="sxs-lookup"><span data-stu-id="61e1f-245">Specifies either the IP address of the Application Virtualization Server or a host name of the server that resolves into the server&#39;s IP address; required when <em>SWIPUBSVRDISPLAY</em> is used.</span></span></p>
<p><span data-ttu-id="61e1f-246">Exemplo: <strong> SWIPUBSVRHOST = &quot; Server01&quot;</span><span class="sxs-lookup"><span data-stu-id="61e1f-246">Example: <strong>SWIPUBSVRHOST=&quot;SERVER01&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="61e1f-247">SWIPUBSVRPORT</span><span class="sxs-lookup"><span data-stu-id="61e1f-247">SWIPUBSVRPORT</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-248">Número da porta</span><span class="sxs-lookup"><span data-stu-id="61e1f-248">Port number</span></span></p></td>
<td align="left"><p><span data-ttu-id="61e1f-249">Especifica a porta lógica que é usada por este servidor de virtualização de aplicativos para ouvir solicitações do cliente (padrão = 554).</span><span class="sxs-lookup"><span data-stu-id="61e1f-249">Specifies the logical port that is used by this Application Virtualization Server to listen for requests from the client (default = 554).</span></span></p>
<ul>
<li><p><span data-ttu-id="61e1f-250">Servidor HTTP padrão — padrão = 80.</span><span class="sxs-lookup"><span data-stu-id="61e1f-250">Standard HTTP server—Default = 80.</span></span></p></li>
<li><p><span data-ttu-id="61e1f-251">Servidor HTTP de segurança aprimorada — padrão = 443.</span><span class="sxs-lookup"><span data-stu-id="61e1f-251">Enhanced Security HTTP Server—Default = 443.</span></span></p></li>
<li><p><span data-ttu-id="61e1f-252">Servidor de virtualização de aplicativos — padrão = 554.</span><span class="sxs-lookup"><span data-stu-id="61e1f-252">Application Virtualization Server—Default = 554.</span></span></p></li>
<li><p><span data-ttu-id="61e1f-253">Servidor avançado de virtualização do aplicativo de segurança — padrão = 322.</span><span class="sxs-lookup"><span data-stu-id="61e1f-253">Enhanced Security Application Virtualization Server—Default = 322.</span></span></p></li>
</ul>
<p><span data-ttu-id="61e1f-254">Exemplo: <strong> SWIPUBSVRPORT = &quot; 443&quot;</span><span class="sxs-lookup"><span data-stu-id="61e1f-254">Example: <strong>SWIPUBSVRPORT=&quot;443&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="61e1f-255">SWIPUBSVRPATH</span><span class="sxs-lookup"><span data-stu-id="61e1f-255">SWIPUBSVRPATH</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-256">Nome do caminho</span><span class="sxs-lookup"><span data-stu-id="61e1f-256">Path name</span></span></p></td>
<td align="left"><p><span data-ttu-id="61e1f-257">Especifica o local no servidor de publicação do arquivo que define associações de tipo de arquivo (padrão =/); obrigatório quando o <em> </em> valor do parâmetro SWIPUBSVRTYPE é http.</span><span class="sxs-lookup"><span data-stu-id="61e1f-257">Specifies the location on the publishing server of the file that defines file type associations (default = /); required when the <em>SWIPUBSVRTYPE</em> parameter value is HTTP.</span></span></p>
<p><span data-ttu-id="61e1f-258">Exemplo: <strong> SWIPUBSVRPATH = &quot; /APPVIRT/appsntypes.xml&quot;</span><span class="sxs-lookup"><span data-stu-id="61e1f-258">Example: <strong>SWIPUBSVRPATH=&quot;/AppVirt/appsntypes.xml&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="61e1f-259">SWIPUBSVRREFRESH</span><span class="sxs-lookup"><span data-stu-id="61e1f-259">SWIPUBSVRREFRESH</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-260">[Ligado | REDONDA</span><span class="sxs-lookup"><span data-stu-id="61e1f-260">[ON|OFF]</span></span></p></td>
<td align="left"><p><span data-ttu-id="61e1f-261">Especifica se o cliente consulta automaticamente o servidor de publicação para aplicativos e associações de tipo de arquivo quando um usuário faz logon no cliente (padrão = ativado).</span><span class="sxs-lookup"><span data-stu-id="61e1f-261">Specifies whether the client automatically queries the publishing server for file type associations and applications when a user logs in to the client (default = ON).</span></span></p>
<p><span data-ttu-id="61e1f-262">Exemplo: <strong> SWIPUBSVRREFRESH = &quot; desativado&quot;</span><span class="sxs-lookup"><span data-stu-id="61e1f-262">Example: <strong>SWIPUBSVRREFRESH=&quot;off&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="61e1f-263">SWIGLOBALDATA</span><span class="sxs-lookup"><span data-stu-id="61e1f-263">SWIGLOBALDATA</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-264">Diretório de dados globais</span><span class="sxs-lookup"><span data-stu-id="61e1f-264">Global data directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="61e1f-265">Especifica o diretório em que os dados serão armazenados que não são específicos de determinados usuários (padrão = C:\Documents and Settings\All Users\Documents).</span><span class="sxs-lookup"><span data-stu-id="61e1f-265">Specifies the directory where data will be stored that is not specific to particular users (default = C:\Documents and Settings\All Users\Documents).</span></span></p>
<p><span data-ttu-id="61e1f-266">Exemplo: <strong> SWIGLOBALDATA = &quot; D:\Microsoft Application Virtualization Client\Global&quot;</span><span class="sxs-lookup"><span data-stu-id="61e1f-266">Example: <strong>SWIGLOBALDATA=&quot;D:\Microsoft Application Virtualization Client\Global&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="61e1f-267">SWIUSERDATA</span><span class="sxs-lookup"><span data-stu-id="61e1f-267">SWIUSERDATA</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-268">Diretório de dados do usuário</span><span class="sxs-lookup"><span data-stu-id="61e1f-268">User data directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="61e1f-269">Especifica o diretório onde os dados serão armazenados específicos a determinados usuários (padrão =% APPDATA%).</span><span class="sxs-lookup"><span data-stu-id="61e1f-269">Specifies the directory where data will be stored that is specific to particular users (default = %APPDATA%).</span></span></p>
<p><span data-ttu-id="61e1f-270">Exemplo: <strong> SWIUSERDATA = &quot; H:\Windows\Microsoft Application Virtualization Client&quot;</span><span class="sxs-lookup"><span data-stu-id="61e1f-270">Example: <strong>SWIUSERDATA=&quot;H:\Windows\Microsoft Application Virtualization Client&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="61e1f-271">SWIFSDRIVE</span><span class="sxs-lookup"><span data-stu-id="61e1f-271">SWIFSDRIVE</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-272">Letra de unidade preferida</span><span class="sxs-lookup"><span data-stu-id="61e1f-272">Preferred drive letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="61e1f-273">Corresponde à letra da unidade selecionada para a unidade virtual.</span><span class="sxs-lookup"><span data-stu-id="61e1f-273">Corresponds to the drive letter that you selected for the virtual drive.</span></span></p>
<p><span data-ttu-id="61e1f-274">Exemplo: <strong> SWIFSDRIVE = &quot; S&quot;</span><span class="sxs-lookup"><span data-stu-id="61e1f-274">Example: <strong>SWIFSDRIVE=&quot;S&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="61e1f-275">SYSTEMEVENTLOGLEVEL</span><span class="sxs-lookup"><span data-stu-id="61e1f-275">SYSTEMEVENTLOGLEVEL</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-276">0 – 4</span><span class="sxs-lookup"><span data-stu-id="61e1f-276">0–4</span></span></p></td>
<td align="left"><p><span data-ttu-id="61e1f-277">Indica o nível de log no qual as mensagens de log são gravadas no log de eventos do NT.</span><span class="sxs-lookup"><span data-stu-id="61e1f-277">Indicates the logging level at which log messages are written to the NT event Log.</span></span> <span data-ttu-id="61e1f-278">O valor indica um limite do que é registrado, ou seja, tudo é igual a ou menor que o valor é registrado.</span><span class="sxs-lookup"><span data-stu-id="61e1f-278">The value indicates a threshold of what is logged—that is, everything equal to or less than that value is logged.</span></span> <span data-ttu-id="61e1f-279">Por exemplo, um valor de 0x3 (Warning) indica que avisos (0x3), erros (0x2) e erros críticos (0x1) são registrados.</span><span class="sxs-lookup"><span data-stu-id="61e1f-279">For example, a value of 0x3 (Warning) indicates that Warnings (0x3), Errors (0x2), and Critical Errors (0x1) are logged.</span></span></p>
<p><span data-ttu-id="61e1f-280">Valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="61e1f-280">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="61e1f-281">0 = = nenhum</span><span class="sxs-lookup"><span data-stu-id="61e1f-281">0 == None</span></span></p></li>
<li><p><span data-ttu-id="61e1f-282">1 = = crítica</span><span class="sxs-lookup"><span data-stu-id="61e1f-282">1 == Critical</span></span></p></li>
<li><p><span data-ttu-id="61e1f-283">2 = = erro</span><span class="sxs-lookup"><span data-stu-id="61e1f-283">2 == Error</span></span></p></li>
<li><p><span data-ttu-id="61e1f-284">3 = = aviso</span><span class="sxs-lookup"><span data-stu-id="61e1f-284">3 == Warning</span></span></p></li>
<li><p><span data-ttu-id="61e1f-285">4 = = informações</span><span class="sxs-lookup"><span data-stu-id="61e1f-285">4 == Information</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="61e1f-286">MINFREESPACEMB</span><span class="sxs-lookup"><span data-stu-id="61e1f-286">MINFREESPACEMB</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-287">Em MB</span><span class="sxs-lookup"><span data-stu-id="61e1f-287">In MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="61e1f-288">Especifica a quantidade de espaço livre (em megabytes) que deve estar disponível no host antes que o tamanho do cache possa aumentar.</span><span class="sxs-lookup"><span data-stu-id="61e1f-288">Specifies the amount of free space (in megabytes) that must be available on the host before the cache size can increase.</span></span> <span data-ttu-id="61e1f-289">O exemplo a seguir configuraria o cliente para garantir pelo menos 5 GB de espaço livre no disco antes de permitir que o tamanho do cache aumente.</span><span class="sxs-lookup"><span data-stu-id="61e1f-289">The following example would configure the client to ensure at least 5 GB of free space on the disk before allowing the size of the cache to increase.</span></span> <span data-ttu-id="61e1f-290">O padrão é 5000 MB de espaço livre disponível em disco no momento da instalação.</span><span class="sxs-lookup"><span data-stu-id="61e1f-290">The default is 5000 MB of free space available on disk at installation time.</span></span></p>
<p><span data-ttu-id="61e1f-291">Exemplo: <strong> MINFREESPACEMB = &quot; 5000 &quot; (5 GB)</span><span class="sxs-lookup"><span data-stu-id="61e1f-291">Example: <strong>MINFREESPACEMB =&quot;5000&quot; (5 GB)</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="61e1f-292">KEEPCURRENTSETTINGS</span><span class="sxs-lookup"><span data-stu-id="61e1f-292">KEEPCURRENTSETTINGS</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="61e1f-293">[0 | 1]</span><span class="sxs-lookup"><span data-stu-id="61e1f-293">[0|1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="61e1f-294">Usado quando você aplicou configurações do registro antes de implantar um cliente — por exemplo, usando a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="61e1f-294">Used when you have applied registry settings prior to deploying a client—for example, by using Group Policy.</span></span> <span data-ttu-id="61e1f-295">Quando um cliente é implantado, defina esse parâmetro como um valor de 1 para que ele não substitua as configurações do registro.</span><span class="sxs-lookup"><span data-stu-id="61e1f-295">When a client is deployed, set this parameter to a value of 1 so that it will not overwrite the registry settings.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="61e1f-296">Importante</span><span class="sxs-lookup"><span data-stu-id="61e1f-296">Important</span></span></strong><br/><p><span data-ttu-id="61e1f-297">Se definido com o valor 1, os seguintes parâmetros de linha de comando do instalador do cliente serão ignorados:</span><span class="sxs-lookup"><span data-stu-id="61e1f-297">If set to a value of 1, the following client installer command-line parameters are ignored:</span></span></p>
<p><strong><span data-ttu-id="61e1f-298">SWICACHESIZE </strong> , <strong> MINFREESPACEMB </strong> , <strong> ALLOWINDEPENDENTFILESTREAMING </strong> , <strong> APPLICATIONSOURCEROOT </strong> , <strong> IconSourceRoot </strong> , <strong> OSDSourceRoot </strong> , <strong> SYSTEMEVENTLOGLEVEL </strong> , <strong> SWIGLOBALDATA </strong> , <strong> DOTIMEOUTMINUTES </strong> , <strong> SWIFSDRIVE </strong> , <strong> AUTOLOADTARGET </strong> , <strong> AUTOLOADTRIGGERS </strong> e <strong> SWIUSERDATA </strong> .</span><span class="sxs-lookup"><span data-stu-id="61e1f-298">SWICACHESIZE</strong>, <strong>MINFREESPACEMB</strong>, <strong>ALLOWINDEPENDENTFILESTREAMING</strong>, <strong>APPLICATIONSOURCEROOT</strong>, <strong>ICONSOURCEROOT</strong>, <strong>OSDSOURCEROOT</strong>, <strong>SYSTEMEVENTLOGLEVEL</strong>, <strong>SWIGLOBALDATA</strong>, <strong>DOTIMEOUTMINUTES</strong>, <strong>SWIFSDRIVE</strong>, <strong>AUTOLOADTARGET</strong>, <strong>AUTOLOADTRIGGERS</strong>, and <strong>SWIUSERDATA</strong>.</span></span></p>
<p><span data-ttu-id="61e1f-299">Para obter mais informações sobre como definir esses valores após a instalação, consulte "como definir as configurações do registro do cliente do App-V usando a linha de comando" no guia de operações do Application Virtualization (App-V) ( <a href="https://go.microsoft.com/fwlink/?LinkId=122939" data-raw-source="[https://go.microsoft.com/fwlink/?LinkId=122939](https://go.microsoft.com/fwlink/?LinkId=122939)"> https://go.microsoft.com/fwlink/?LinkId=122939 </a> ).</span><span class="sxs-lookup"><span data-stu-id="61e1f-299">For further information about setting these values after installation, see “How to Configure the App-V Client Registry Settings by Using the Command Line” in the Application Virtualization (App-V) Operations Guide (<a href="https://go.microsoft.com/fwlink/?LinkId=122939" data-raw-source="[https://go.microsoft.com/fwlink/?LinkId=122939](https://go.microsoft.com/fwlink/?LinkId=122939)">https://go.microsoft.com/fwlink/?LinkId=122939</a>).</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="61e1f-300">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="61e1f-300">Related topics</span></span>


[<span data-ttu-id="61e1f-301">Como instalar manualmente o Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="61e1f-301">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="61e1f-302">Como fazer upgrade do Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="61e1f-302">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)

[<span data-ttu-id="61e1f-303">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="61e1f-303">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)









