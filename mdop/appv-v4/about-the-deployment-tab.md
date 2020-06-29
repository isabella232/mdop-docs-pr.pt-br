---
title: Sobre a guia Implantação
description: Sobre a guia Implantação
author: dansimp
ms.assetid: 12891798-baa4-45a5-b845-b9505ab95633
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 147e8b1057c789d97087461a585fa3f365089784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797630"
---
# <span data-ttu-id="513b1-103">Sobre a guia Implantação</span><span class="sxs-lookup"><span data-stu-id="513b1-103">About the Deployment Tab</span></span>


<span data-ttu-id="513b1-104">Use a guia **implantação** no console do sequenciador do Application Virtualization para alterar as informações de um aplicativo que você está prestes a sequenciar.</span><span class="sxs-lookup"><span data-stu-id="513b1-104">Use the **Deployment** tab in the Application Virtualization Sequencer Console to change the information for an application you are about to sequence.</span></span> <span data-ttu-id="513b1-105">Esta guia contém os elementos a seguir.</span><span class="sxs-lookup"><span data-stu-id="513b1-105">This tab contains the following elements.</span></span>

## <span data-ttu-id="513b1-106">URL do servidor</span><span class="sxs-lookup"><span data-stu-id="513b1-106">Server URL</span></span>


<span data-ttu-id="513b1-107">Use os controles de **URL do servidor** para especificar as definições de configuração do servidor de aplicativos virtual.</span><span class="sxs-lookup"><span data-stu-id="513b1-107">Use the **Server URL** controls to specify the virtual application server configuration settings.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="513b1-108">Controle</span><span class="sxs-lookup"><span data-stu-id="513b1-108">Control</span></span></th>
<th align="left"><span data-ttu-id="513b1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="513b1-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="513b1-110">Protocolo</span><span class="sxs-lookup"><span data-stu-id="513b1-110">Protocol</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="513b1-111">Permite que você selecione o protocolo que irá transmitir o pacote do aplicativo sequenciado de um servidor de aplicativos virtual a um cliente de desktop do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="513b1-111">Enables you to select the protocol that will stream the sequenced application package from a virtual application server to an Application Virtualization Desktop Client.</span></span> <span data-ttu-id="513b1-112">Os seguintes protocolos estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="513b1-112">The following protocols are available:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="513b1-113">RTSP </strong> — o padrão, especifica que o protocolo de streaming em tempo real controla a troca de aplicativos habilitados para virtualização.</span><span class="sxs-lookup"><span data-stu-id="513b1-113">RTSP</strong>—The default, it specifies that the Real-Time Streaming Protocol controls the exchange of virtualization-enabled applications.</span></span></p></li>
<li><p><strong><span data-ttu-id="513b1-114">RTSPs </strong> — especifica que o protocolo de streaming em tempo real com segurança da camada de transporte controla a troca de um pacote de aplicativo sequenciado.</span><span class="sxs-lookup"><span data-stu-id="513b1-114">RTSPS</strong>—Specifies that the Real-Time Streaming Protocol with Transport Layer Security controls the exchange of a sequenced application package.</span></span></p></li>
<li><p><strong><span data-ttu-id="513b1-115">Arquivo </strong> — especifica que o aplicativo sequenciado será transmitido de um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="513b1-115">File</strong>—Specifies that the sequenced application will be streamed from a file share.</span></span></p></li>
<li><p><strong><span data-ttu-id="513b1-116">HTTPS </strong> — especifica que o protocolo de transporte de hipertexto seguro controla a troca de um pacote.</span><span class="sxs-lookup"><span data-stu-id="513b1-116">HTTPS</strong>—Specifies that Secure Hypertext Transport Protocol controls the exchange of a package.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="513b1-117">Hostname</span><span class="sxs-lookup"><span data-stu-id="513b1-117">Hostname</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="513b1-118">Permite que você selecione o servidor de aplicativos virtual ou o balanceador de carga na frente de um grupo de servidores de aplicativos virtuais que transmitirá o pacote de software a um cliente de desktop de virtualização de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="513b1-118">Enables you to select the virtual application server or the load balancer in front of a group of virtual application servers that will stream the software package to an Application Virtualization Desktop Client.</span></span> <span data-ttu-id="513b1-119">Você deve concluir esse item para criar um pacote de aplicativo sequenciado, mas você pode alterar a variável de ambiente% SFT_SOFTGRIDSERVER% padrão para o nome de host ou endereço IP real de um servidor de aplicativos virtual.</span><span class="sxs-lookup"><span data-stu-id="513b1-119">You must complete this item to create a sequenced application package, but you can change from the default %SFT_SOFTGRIDSERVER% environment variable to the actual hostname or IP address of a virtual application server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="513b1-120">Observação</span><span class="sxs-lookup"><span data-stu-id="513b1-120">Note</span></span></strong><br/><p><span data-ttu-id="513b1-121">Se você optar por não especificar um nome de host estático ou endereço IP, em cada cliente de desktop virtualização de aplicativos, será necessário configurar uma variável de ambiente chamada SFT_SOFTGRIDSERVER.</span><span class="sxs-lookup"><span data-stu-id="513b1-121">If you choose not to specify a static hostname or IP address, on each Application Virtualization Desktop Client you must set up an environment variable called SFT_SOFTGRIDSERVER.</span></span> <span data-ttu-id="513b1-122">O valor deve ser o nome do host ou endereço IP do servidor de aplicativos virtual ou o balanceador de carga que é este cliente&#39;s fonte de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="513b1-122">Its value must be the hostname or IP address of the virtual application server or load balancer that is this client&#39;s source of applications.</span></span> <span data-ttu-id="513b1-123">Você deve transformar essa variável de ambiente em uma variável de sistema, em vez de uma variável de usuário.</span><span class="sxs-lookup"><span data-stu-id="513b1-123">You should make this environment variable a system variable rather than a user variable.</span></span> <span data-ttu-id="513b1-124">Qualquer sessão de cliente da área de trabalho do Application Virtualization que esteja em execução neste computador durante a atribuição dessa variável deve ser fechada e, em seguida, aberta para que a sessão retomada saiba qual é a sua nova fonte de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="513b1-124">Any Application Virtualization Desktop Client session that is running on this computer during your assignment of this variable must be closed and then opened so that the resumed session will be aware of its new application source.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="513b1-125">Port</span><span class="sxs-lookup"><span data-stu-id="513b1-125">Port</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="513b1-126">Permite que você especifique a porta na qual o servidor de aplicativos virtual ou o balanceador de carga escutará uma solicitação de cliente de desktop virtualização de aplicativos&#39;s para o pacote.</span><span class="sxs-lookup"><span data-stu-id="513b1-126">Enables you to specify the port on which the virtual application server or the load balancer will listen for an Application Virtualization Desktop Client&#39;s request for the package.</span></span> <span data-ttu-id="513b1-127">Essas informações são necessárias para criar um pacote, mas você pode alterá-lo.</span><span class="sxs-lookup"><span data-stu-id="513b1-127">This information is required to create a package, but you can change it.</span></span> <span data-ttu-id="513b1-128">A porta padrão é 554.</span><span class="sxs-lookup"><span data-stu-id="513b1-128">The default port is 554.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="513b1-129">Caminho</span><span class="sxs-lookup"><span data-stu-id="513b1-129">Path</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="513b1-130">Permite que você especifique o caminho relativo no servidor de aplicativos virtual em que o pacote do software está armazenado e do qual ele será transmitido.</span><span class="sxs-lookup"><span data-stu-id="513b1-130">Enables you to specify the relative path on the virtual application server where the software package is stored and from which it will be streamed.</span></span> <span data-ttu-id="513b1-131">Essas informações são necessárias para criar um pacote se o arquivo SFT for armazenado em um subdiretório de conteúdo; caso contrário, essas informações não são necessárias.</span><span class="sxs-lookup"><span data-stu-id="513b1-131">This information is required to create a package if the SFT file will be stored in a subdirectory of CONTENT; otherwise, this information is not required.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="513b1-132">Sistemas operacionais</span><span class="sxs-lookup"><span data-stu-id="513b1-132">Operating Systems</span></span>


<span data-ttu-id="513b1-133">Use os controles de **sistemas operacionais** para especificar os requisitos do sistema operacional do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="513b1-133">Use the **Operating Systems** controls to specify the application's operating system requirements.</span></span> <span data-ttu-id="513b1-134">Se um cliente da área de trabalho do Application Virtualization não puder dar suporte a nenhum dos sistemas operacionais selecionados, o aplicativo não será iniciado.</span><span class="sxs-lookup"><span data-stu-id="513b1-134">If an Application Virtualization Desktop Client cannot support any of the selected operating systems, the application will not start.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="513b1-135">Controles</span><span class="sxs-lookup"><span data-stu-id="513b1-135">Controls</span></span></th>
<th align="left"><span data-ttu-id="513b1-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="513b1-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="513b1-137">Sistemas operacionais disponíveis</span><span class="sxs-lookup"><span data-stu-id="513b1-137">Available Operating Systems</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="513b1-138">Exibe uma lista de sistemas operacionais que podem dar suporte aos aplicativos no pacote.</span><span class="sxs-lookup"><span data-stu-id="513b1-138">Displays a list of operating systems that can support the applications in the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="513b1-139">Sistemas operacionais selecionados</span><span class="sxs-lookup"><span data-stu-id="513b1-139">Selected Operating Systems</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="513b1-140">Exibe uma lista de sistemas operacionais selecionados que dão suporte aos aplicativos no pacote.</span><span class="sxs-lookup"><span data-stu-id="513b1-140">Displays a list of selected operating systems that support the applications in the package.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="513b1-141">Opções de saída</span><span class="sxs-lookup"><span data-stu-id="513b1-141">Output Options</span></span>


<span data-ttu-id="513b1-142">Use os controles de **Opções de saída** para especificar as opções de saída para o aplicativo a ser instalado.</span><span class="sxs-lookup"><span data-stu-id="513b1-142">Use the **Output Options** controls to specify the output options for the application to be installed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="513b1-143">Controle</span><span class="sxs-lookup"><span data-stu-id="513b1-143">Control</span></span></th>
<th align="left"><span data-ttu-id="513b1-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="513b1-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="513b1-145">Algoritmo de compactação</span><span class="sxs-lookup"><span data-stu-id="513b1-145">Compression Algorithm</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="513b1-146">Use para selecionar o método para compactar o arquivo SFT para streaming em uma rede.</span><span class="sxs-lookup"><span data-stu-id="513b1-146">Use to select the method for compressing the SFT file for streaming across a network.</span></span> <span data-ttu-id="513b1-147">Selecione um dos seguintes métodos de compactação:</span><span class="sxs-lookup"><span data-stu-id="513b1-147">Select one of the following compression methods:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="513b1-148">Compactado </strong> — especifica que o arquivo SFT seja compactado <a href="https://go.microsoft.com/fwlink/?LinkId=111475" data-raw-source="[ZLIB](https://go.microsoft.com/fwlink/?LinkId=111475)"> no </a> formato zlib.</span><span class="sxs-lookup"><span data-stu-id="513b1-148">Compressed</strong>—Specifies that the SFT file be compressed in the <a href="https://go.microsoft.com/fwlink/?LinkId=111475" data-raw-source="[ZLIB](https://go.microsoft.com/fwlink/?LinkId=111475)">ZLIB</a> format.</span></span></p></li>
<li><p><strong><span data-ttu-id="513b1-149">Não compactado </strong> — o padrão; especifica que o arquivo SFT não seja compactado.</span><span class="sxs-lookup"><span data-stu-id="513b1-149">Not Compressed</strong>—The default; specifies that the SFT file not be compressed.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="513b1-150">Impor descritores de segurança</span><span class="sxs-lookup"><span data-stu-id="513b1-150">Enforce Security Descriptors</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="513b1-151">Selecione para impor os descritores de segurança dos aplicativos no pacote após a implantação no cliente.</span><span class="sxs-lookup"><span data-stu-id="513b1-151">Select to enforce security descriptors of the applications in the package after it is deployed to the client.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="513b1-152">Gerar pacote MSI (Microsoft Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="513b1-152">Generate Microsoft Windows Installer (MSI) Package</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="513b1-153">Selecione para instalar ou implantar um pacote de aplicativo sequenciado com o Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="513b1-153">Select to install or deploy a sequenced application package with the Windows Installer.</span></span> <span data-ttu-id="513b1-154">Se você tiver feito alterações usando o sequenciador, as alterações não serão incluídas com o arquivo do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="513b1-154">If you have made any changes using the sequencer the changes will not be included with the Windows Installer file.</span></span> <span data-ttu-id="513b1-155">O arquivo do Windows Installer sempre será criado usando o arquivo. sft salvo no disco rígido.</span><span class="sxs-lookup"><span data-stu-id="513b1-155">The Windows Installer file will always be created using the .sft file saved on the hard disk.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="513b1-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="513b1-156">Related topics</span></span>


[<span data-ttu-id="513b1-157">Como alterar as propriedades da implantação</span><span class="sxs-lookup"><span data-stu-id="513b1-157">How to Change Deployment Properties</span></span>](how-to-change-deployment-properties.md)

[<span data-ttu-id="513b1-158">Console do Sequencer</span><span class="sxs-lookup"><span data-stu-id="513b1-158">Sequencer Console</span></span>](sequencer-console.md)









