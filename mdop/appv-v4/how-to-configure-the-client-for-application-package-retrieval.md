---
title: Como configurar o cliente para recuperação de pacote de aplicativo
description: Como configurar o cliente para recuperação de pacote de aplicativo
author: dansimp
ms.assetid: 891f2739-da7a-46da-b452-b8c0af075525
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5eeb0b977c6ecd44947d5d1c42d25d47b9e2530
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797203"
---
# <span data-ttu-id="a8e5c-103">Como configurar o cliente para recuperação de pacote de aplicativo</span><span class="sxs-lookup"><span data-stu-id="a8e5c-103">How to Configure the Client for Application Package Retrieval</span></span>


<span data-ttu-id="a8e5c-104">Quando o cliente está configurado com um servidor de gerenciamento do App-V (App-V) como seu servidor de publicação, por padrão no próximo ciclo de atualização de publicação, o cliente recupera do servidor o descritor de software aberto (OSD) e os arquivos de manifesto do pacote para cada pacote que o usuário está autorizado a usar.</span><span class="sxs-lookup"><span data-stu-id="a8e5c-104">When the client is configured with an Application Virtualization (App-V) Management Server as its publishing server, by default at the next publishing refresh cycle, the client retrieves from the server the Open Software Descriptor (OSD) and package manifest files for each package that the user is authorized to use.</span></span> <span data-ttu-id="a8e5c-105">O cliente usa as informações de origem do pacote definidas nesses arquivos para determinar onde encontrar o conteúdo do pacote, os ícones e associações de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="a8e5c-105">The client uses the package source information that is defined in these files to determine where to find the package content, icons, and file type associations.</span></span>

<span data-ttu-id="a8e5c-106">Se você quiser que o cliente obtenha o conteúdo do pacote (arquivo SFT) de um servidor de streaming do App-V local ou outra fonte alternativa, como um servidor da Web ou um servidor de arquivos, em vez do servidor de gerenciamento do App-V, você pode configurar o valor da chave do registro ApplicationSourceRoot no computador para apontar para o compartilhamento de conteúdo local no outro servidor.</span><span class="sxs-lookup"><span data-stu-id="a8e5c-106">If you want the client to obtain the package content (SFT file) from a local App-V Streaming Server or other alternate source such as a Web server or file server, instead of from the App-V Management Server, you can configure the ApplicationSourceRoot registry key value on the computer to point to the local content share on the other server.</span></span> <span data-ttu-id="a8e5c-107">O arquivo OSD ainda define o caminho de origem original para o conteúdo do pacote.</span><span class="sxs-lookup"><span data-stu-id="a8e5c-107">The OSD file still defines the original source path for the package content.</span></span> <span data-ttu-id="a8e5c-108">No entanto, o cliente usa o valor da configuração ApplicationSourceRoot no lugar do servidor e do compartilhamento especificados no caminho do conteúdo no arquivo OSD.</span><span class="sxs-lookup"><span data-stu-id="a8e5c-108">However the client uses the value of the ApplicationSourceRoot setting in place of the server and share that are specified in the content path in the OSD file.</span></span> <span data-ttu-id="a8e5c-109">Isso redireciona o cliente para recuperar o conteúdo do outro servidor.</span><span class="sxs-lookup"><span data-stu-id="a8e5c-109">This redirects the client to retrieve the content from the other server.</span></span>

<span data-ttu-id="a8e5c-110">Você também pode configurar os valores da chave do registro OSDSourceRoot e IconSourceRoot se quiser substituir essas configurações no arquivo de manifesto do pacote ou nos caminhos enviados por um servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="a8e5c-110">You can also configure the OSDSourceRoot and IconSourceRoot registry key values if you want to override those settings in the package manifest file or in the paths sent by a publishing server.</span></span> <span data-ttu-id="a8e5c-111">O OSDSourceRoot especifica um local de origem para a recuperação de arquivo OSD para um pacote de aplicativo durante a publicação.</span><span class="sxs-lookup"><span data-stu-id="a8e5c-111">The OSDSourceRoot specifies a source location for OSD file retrieval for an application package during publication.</span></span> <span data-ttu-id="a8e5c-112">O IconSourceRoot especifica um local de origem para a recuperação de ícone para um pacote de aplicativo durante a publicação.</span><span class="sxs-lookup"><span data-stu-id="a8e5c-112">The IconSourceRoot specifies a source location for icon retrieval for an application package during publication.</span></span>

**<span data-ttu-id="a8e5c-113">Observação</span><span class="sxs-lookup"><span data-stu-id="a8e5c-113">Note</span></span>**  
-   <span data-ttu-id="a8e5c-114">As configurações de IconSourceRoot e OSDSourceRoot substituem os valores no arquivo de manifesto do pacote, portanto, se você tentar implantar um pacote usando o método de arquivo do Windows Installer (. msi), ele também substituirá os valores no arquivo de manifesto do pacote contido nesse arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="a8e5c-114">The IconSourceRoot and OSDSourceRoot settings override the values in the package manifest file, so if you try to deploy a package by using the Windows Installer (.msi) file method, it will also override the values in the package manifest file that is contained within that .msi file.</span></span>

-   <span data-ttu-id="a8e5c-115">Durante as operações de streaming e de transmissão HTTP (S), os clientes do App-V 4,5 SP1 usam as configurações de servidor proxy configuradas no Internet Explorer no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="a8e5c-115">During both the publishing and HTTP(S) streaming operations,App-V 4.5 SP1 clients use the proxy server settings that are configured in Internet Explorer on the user’s computer.</span></span>



**<span data-ttu-id="a8e5c-116">Para configurar o valor da chave do registro ApplicationSourceRoot</span><span class="sxs-lookup"><span data-stu-id="a8e5c-116">To configure the ApplicationSourceRoot registry key value</span></span>**

-   <span data-ttu-id="a8e5c-117">Configure o ApplicationSourceRoot no seguinte valor da chave do registro com um caminho UNC ou uma URL:</span><span class="sxs-lookup"><span data-stu-id="a8e5c-117">Configure the ApplicationSourceRoot in the following registry key value with either a UNC path or a URL:</span></span>

    <span data-ttu-id="a8e5c-118">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\ApplicationSourceRoot</span><span class="sxs-lookup"><span data-stu-id="a8e5c-118">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\ApplicationSourceRoot</span></span>

    <span data-ttu-id="a8e5c-119">O formato correto para o caminho UNC (Convenção de nomenclatura universal) é **\\\\computername\\sharefolder\\\ [pasta \] \ [\ \ \]**, em que a **pasta** é opcional.</span><span class="sxs-lookup"><span data-stu-id="a8e5c-119">The correct format for the Universal Naming Convention (UNC) path is **\\\\computername\\sharefolder\\\[folder\]\[\\\]**, where **folder** is optional.</span></span> <span data-ttu-id="a8e5c-120">O **ComputerName** pode ser um FQDN (nome de domínio totalmente qualificado) ou um endereço IP, e **ShareFolder** pode ser uma letra de unidade.</span><span class="sxs-lookup"><span data-stu-id="a8e5c-120">The **computername** can be a Fully Qualified Domain Name (FQDN) or an IP address, and **sharefolder** can be a drive letter.</span></span> <span data-ttu-id="a8e5c-121">Somente a parte **\\\\computername\\sharedfolder** ou letra da unidade do caminho OSD é substituída.</span><span class="sxs-lookup"><span data-stu-id="a8e5c-121">Only the **\\\\computername\\sharedfolder** or drive letter portion of the OSD path is replaced.</span></span>

    <span data-ttu-id="a8e5c-122">O formato correto para o caminho da URL é protocolo: a partir de **: \ [porta \] \ [/path\] \ [/\]**, em que a **porta** e o **caminho** são opcionais.</span><span class="sxs-lookup"><span data-stu-id="a8e5c-122">The correct format for the URL path is **protocol://servername:\[port\]\[/path\]\[/\]**, where **port** and **path** are optional.</span></span> <span data-ttu-id="a8e5c-123">Se **porta** não for especificada, será usada a porta padrão do protocolo.</span><span class="sxs-lookup"><span data-stu-id="a8e5c-123">If **port** is not specified, the default port for the protocol is used.</span></span> <span data-ttu-id="a8e5c-124">Somente a porção **Protocol://Server: Port** da URL OSD é substituída.</span><span class="sxs-lookup"><span data-stu-id="a8e5c-124">Only the **protocol://server:port** portion of the OSD URL is replaced.</span></span>

    **<span data-ttu-id="a8e5c-125">Importante</span><span class="sxs-lookup"><span data-stu-id="a8e5c-125">Important</span></span>**  
    <span data-ttu-id="a8e5c-126">Não há suporte para variáveis de ambiente na definição ApplicationSourceRoot.</span><span class="sxs-lookup"><span data-stu-id="a8e5c-126">Environment variables are not supported in the ApplicationSourceRoot definition.</span></span>



~~~
The following table lists examples of acceptable URL and UNC path formats.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ApplicationSourceRoot</th>
<th align="left">OSD File HREF Path</th>
<th align="left">Result</th>
<th align="left">Comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>https://mainserver:443/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>https://mainserver:443/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://%SFT_APPVSERVER%:554/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>file://\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="odd">
<td align="left"><p>\\uncserver\share</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="even">
<td align="left"><p>\\uncserver\share\prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="odd">
<td align="left"><p>M:</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>M:\prodapps</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>
~~~



**<span data-ttu-id="a8e5c-127">Para configurar o valor de OSDSourceRoot</span><span class="sxs-lookup"><span data-stu-id="a8e5c-127">To configure the OSDSourceRoot value</span></span>**

-   <span data-ttu-id="a8e5c-128">Configure o OSDSourceRoot no seguinte valor da chave do registro com um caminho UNC ou uma URL:</span><span class="sxs-lookup"><span data-stu-id="a8e5c-128">Configure the OSDSourceRoot in the following registry key value with either a UNC path or a URL:</span></span>

    <span data-ttu-id="a8e5c-129">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\OSDSourceRoot</span><span class="sxs-lookup"><span data-stu-id="a8e5c-129">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\OSDSourceRoot</span></span>

    <span data-ttu-id="a8e5c-130">Os formatos aceitáveis para o OSDSourceRoot incluem caminhos e URLs UNC, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="a8e5c-130">Acceptable formats for the OSDSourceRoot include UNC paths and URLs, as in the following example:</span></span>

    <span data-ttu-id="a8e5c-131">**\\\\computername\\sharefolder\\resource** ou **\\\\computername\\content** ou \*\* &lt; unidade &gt; : \\foldername\*\*</span><span class="sxs-lookup"><span data-stu-id="a8e5c-131">**\\\\computername\\sharefolder\\resource** or **\\\\computername\\content** or **&lt;drive&gt;:\\foldername**</span></span>

    <span data-ttu-id="a8e5c-132">**http://computername/productivity/** or**https://computername/productivity/**</span><span class="sxs-lookup"><span data-stu-id="a8e5c-132">**http://computername/productivity/** or **https://computername/productivity/**</span></span>

**<span data-ttu-id="a8e5c-133">Para configurar o valor de IconSourceRoot</span><span class="sxs-lookup"><span data-stu-id="a8e5c-133">To configure the IconSourceRoot value</span></span>**

-   <span data-ttu-id="a8e5c-134">Configure o IconSourceRoot no seguinte valor da chave do registro com um caminho UNC ou uma URL:</span><span class="sxs-lookup"><span data-stu-id="a8e5c-134">Configure the IconSourceRoot in the following registry key value with either a UNC path or a URL:</span></span>

    <span data-ttu-id="a8e5c-135">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\IconSourceRoot</span><span class="sxs-lookup"><span data-stu-id="a8e5c-135">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\IconSourceRoot</span></span>

    <span data-ttu-id="a8e5c-136">Os formatos aceitáveis para o IconSourceRoot incluem caminhos e URLs UNC, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="a8e5c-136">Acceptable formats for the IconSourceRoot include UNC paths and URLs, as in the following example:</span></span>

    <span data-ttu-id="a8e5c-137">**\\\\computername\\sharefolder\\resource** ou **\\\\computername\\content** ou \*\* &lt; unidade &gt; : \\foldername\*\*</span><span class="sxs-lookup"><span data-stu-id="a8e5c-137">**\\\\computername\\sharefolder\\resource** or **\\\\computername\\content** or **&lt;drive&gt;:\\foldername**</span></span>

    <span data-ttu-id="a8e5c-138">**http://computername/productivity/** or**https://computername/productivity/**</span><span class="sxs-lookup"><span data-stu-id="a8e5c-138">**http://computername/productivity/** or **https://computername/productivity/**</span></span>

## <span data-ttu-id="a8e5c-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a8e5c-139">Related topics</span></span>


[<span data-ttu-id="a8e5c-140">Como definir as configurações de Registro do cliente do App-V usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="a8e5c-140">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)









