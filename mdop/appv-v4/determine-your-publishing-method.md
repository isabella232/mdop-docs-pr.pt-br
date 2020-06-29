---
title: Determinar o método de publicação
description: Determinar o método de publicação
author: dansimp
ms.assetid: 1f2d0d39-5d65-457a-b826-4f45b00c8c85
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a6b19b12c28ab67e3250909cb32ddb8419f399a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797973"
---
# <span data-ttu-id="3c4e7-103">Determinar o método de publicação</span><span class="sxs-lookup"><span data-stu-id="3c4e7-103">Determine Your Publishing Method</span></span>


<span data-ttu-id="3c4e7-104">Depois de sequenciar um aplicativo usando o sequenciador do Application Virtualization, você precisará *publicar* esse aplicativo para seus usuários.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-104">After you sequence an application by using the Application Virtualization Sequencer, you need to *publish* that application to your users.</span></span> <span data-ttu-id="3c4e7-105">Publicar o aplicativo consiste em fornecer os ícones, as informações de definição do pacote e o local da fonte de conteúdo para cada computador em que o cliente do Application Virtualization foi instalado.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-105">Publishing the application consists of delivering the icons, package definition information, and content source location to each computer where the Application Virtualization Client has been installed.</span></span> <span data-ttu-id="3c4e7-106">A tabela a seguir descreve os métodos de publicação com suporte ao implantar o Application Virtualization usando um sistema ESD (Electronic Software Distribution).</span><span class="sxs-lookup"><span data-stu-id="3c4e7-106">The following table describes publishing methods that are supported when you deploy Application Virtualization by using an electronic software distribution (ESD) system.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3c4e7-107">Método</span><span class="sxs-lookup"><span data-stu-id="3c4e7-107">Method</span></span></th>
<th align="left"><span data-ttu-id="3c4e7-108">Vantagens</span><span class="sxs-lookup"><span data-stu-id="3c4e7-108">Advantages</span></span></th>
<th align="left"><span data-ttu-id="3c4e7-109">Desvantagens</span><span class="sxs-lookup"><span data-stu-id="3c4e7-109">Disadvantages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c4e7-110">Gerar um arquivo do Windows Installer durante o sequenciamento, como uma solução autônoma.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-110">Generate a Windows Installer file during sequencing, as a stand-alone solution.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3c4e7-111">Muito simples de usar.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-111">Very simple to use.</span></span></p></li>
<li><p><span data-ttu-id="3c4e7-112">Pacote carregado no cache localmente em cada computador.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-112">Package loaded into cache locally on each computer.</span></span></p></li>
<li><p><span data-ttu-id="3c4e7-113">Ícones exibidos para o usuário.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-113">Icons displayed to user.</span></span></p></li>
<li><p><span data-ttu-id="3c4e7-114">Semelhante à implantação de software tradicional.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-114">Similar to traditional software deployment.</span></span></p></li>
<li><p><span data-ttu-id="3c4e7-115">Não é preciso ter servidores de streaming.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-115">No need for streaming servers.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3c4e7-116">Não há flexibilidade na localização do conteúdo do pacote em computadores, no mesmo local em todos os computadores.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-116">No flexibility in location of package contents on computers—same location on all computers.</span></span></p></li>
<li><p><span data-ttu-id="3c4e7-117">Deve usar somente adicionar/remover programas ou msiexec para remover aplicativos.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-117">Must use only Add/Remove Programs or msiexec to remove applications.</span></span></p></li>
<li><p><span data-ttu-id="3c4e7-118">Remoção e substituição pela nova versão necessária para atualização do pacote.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-118">Removal and replacement with new version required for package updating.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3c4e7-119">Gerar um arquivo do Windows Installer durante o sequenciamento, usado com as propriedades de linha de comando MODE, LOAD e OVERRIDEURL e o manifesto do pacote.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-119">Generate a Windows Installer file during sequencing, used with MODE, LOAD, and OVERRIDEURL command-line properties and the package manifest.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3c4e7-120">Simples de usar, mas com flexibilidade adicional.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-120">Simple to use but with added flexibility.</span></span></p></li>
<li><p><span data-ttu-id="3c4e7-121">Ícones exibidos para o usuário.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-121">Icons displayed to user.</span></span></p></li>
<li><p><span data-ttu-id="3c4e7-122">O arquivo SFT que contém os aplicativos pode ser colocado em um local de origem de streaming, com clientes configurados para usar esse local.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-122">SFT file containing the applications can be placed on a streaming source location, with clients configured to use that location.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3c4e7-123">Flexibilidade limitada — apenas o local do conteúdo do pacote pode ser controlado no tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-123">Limited flexibility—only the location of the package content can be controlled at run time.</span></span></p></li>
<li><p><span data-ttu-id="3c4e7-124">Deve usar somente adicionar/remover programas ou msiexec para remover o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-124">Must use only Add/Remove Programs or msiexec to remove the application.</span></span></p></li>
<li><p><span data-ttu-id="3c4e7-125">Remoção e substituição pela nova versão necessária para a atualização do pacote, a menos que você use o Streaming Server.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-125">Removal and replacement with new version required for package updating, unless using streaming server.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3c4e7-126">Executar comandos SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-126">Run SFTMIME commands.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3c4e7-127">Flexibilidade completa: controle total de todas as funções de gerenciamento de pacotes.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-127">Complete flexibility—full control of all package management functions.</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="3c4e7-128">Os comandos devem ser scripdos para serem usados com o sistema ESD.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-128">Commands must be scripted for use with the ESD system.</span></span></p></li>
<li><p><span data-ttu-id="3c4e7-129">Os comandos devem ser executados em cada computador na sequência correta.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-129">Commands must be run on each computer in correct sequence.</span></span></p></li>
<li><p><span data-ttu-id="3c4e7-130">Informações detalhadas sobre a linguagem de comando e o planejamento cuidadoso necessários.</span><span class="sxs-lookup"><span data-stu-id="3c4e7-130">Detailed understanding of command language and careful planning required.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="3c4e7-131">Para obter mais informações sobre como usar esses métodos de publicação, consulte [como publicar um aplicativo virtual no cliente](how-to-publish-a-virtual-application-on-the-client.md).</span><span class="sxs-lookup"><span data-stu-id="3c4e7-131">For more information about using these publishing methods, see [How to Publish a Virtual Application on the Client](how-to-publish-a-virtual-application-on-the-client.md).</span></span>

## <span data-ttu-id="3c4e7-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3c4e7-132">Related topics</span></span>


[<span data-ttu-id="3c4e7-133">Determinar o método de streaming</span><span class="sxs-lookup"><span data-stu-id="3c4e7-133">Determine Your Streaming Method</span></span>](determine-your-streaming-method.md)

[<span data-ttu-id="3c4e7-134">Cenário baseado em Distribuição Eletrônica de Software</span><span class="sxs-lookup"><span data-stu-id="3c4e7-134">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="3c4e7-135">Visão geral de cenário baseado em Distribuição Eletrônica de Software</span><span class="sxs-lookup"><span data-stu-id="3c4e7-135">Electronic Software Distribution-Based Scenario Overview</span></span>](electronic-software-distribution-based-scenario-overview.md)

[<span data-ttu-id="3c4e7-136">Como publicar um aplicativo virtual no cliente</span><span class="sxs-lookup"><span data-stu-id="3c4e7-136">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="3c4e7-137">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="3c4e7-137">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





