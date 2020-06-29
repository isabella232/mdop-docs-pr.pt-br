---
title: Visão geral dos Componentes do Application Virtualization System
description: Visão geral dos Componentes do Application Virtualization System
author: dansimp
ms.assetid: 75d88ef7-44d8-4fa7-b7f5-9153f37e570d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cab0065b9966094da687cce2f5e94069922189fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796848"
---
# <span data-ttu-id="97c14-103">Visão geral dos Componentes do Application Virtualization System</span><span class="sxs-lookup"><span data-stu-id="97c14-103">Overview of the Application Virtualization System Components</span></span>


<span data-ttu-id="97c14-104">A tabela a seguir descreve os componentes principais do sistema de gerenciamento do Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="97c14-104">The following table describes the primary components of the Microsoft Application Virtualization Management System.</span></span> <span data-ttu-id="97c14-105">Para obter mais informações sobre como implantar esses componentes do sistema, consulte [cenário baseado em servidor do Application Virtualization](application-virtualization-server-based-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="97c14-105">For more information about deploying these system components, see [Application Virtualization Server-Based Scenario](application-virtualization-server-based-scenario.md).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="97c14-106">Componente</span><span class="sxs-lookup"><span data-stu-id="97c14-106">Component</span></span></th>
<th align="left"><span data-ttu-id="97c14-107">Função</span><span class="sxs-lookup"><span data-stu-id="97c14-107">Function</span></span></th>
<th align="left"><span data-ttu-id="97c14-108">Informações adicionais</span><span class="sxs-lookup"><span data-stu-id="97c14-108">Additional Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="97c14-109">Servidor de gerenciamento do Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="97c14-109">Microsoft Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="97c14-110">O componente responsável por transmitir o conteúdo do pacote e publicar os atalhos e associações de tipo de arquivo para o cliente do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="97c14-110">The component responsible for streaming the package content and publishing the shortcuts and file type associations to the Application Virtualization Client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="97c14-111">O servidor de gerenciamento do Application Virtualization dá suporte à atualização ativa, ao gerenciamento de licenças e a um banco de dados que pode ser usado para relatórios.</span><span class="sxs-lookup"><span data-stu-id="97c14-111">The Application Virtualization Management Server supports active upgrade, License Management, and a database that can be used for reporting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="97c14-112">Pasta de conteúdo </strong></span><span class="sxs-lookup"><span data-stu-id="97c14-112">Content</strong> folder</span></span></p></td>
<td align="left"><p><span data-ttu-id="97c14-113">O local dos pacotes do Application Virtualization para streaming.</span><span class="sxs-lookup"><span data-stu-id="97c14-113">The location of the Application Virtualization packages for streaming.</span></span></p></td>
<td align="left"><p><span data-ttu-id="97c14-114">Essa pasta pode ser localizada em um compartilhamento ou em um servidor de gerenciamento do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="97c14-114">This folder can be located on a share on or off the Application Virtualization Management Server.</span></span> <span data-ttu-id="97c14-115">A pasta também pode estar localizada em uma rede de área de armazenamento (SAN).</span><span class="sxs-lookup"><span data-stu-id="97c14-115">The folder can also be located on a Storage Area Network (SAN).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="97c14-116">Console de gerenciamento do Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="97c14-116">Microsoft Application Virtualization Management Console</span></span></p></td>
<td align="left"><p><span data-ttu-id="97c14-117">Um utilitário de gerenciamento de snap-in do MMC 3,0 para administração do Microsoft Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="97c14-117">An MMC 3.0 snap-in management utility for Microsoft Application Virtualization Server administration.</span></span></p></td>
<td align="left"><p><span data-ttu-id="97c14-118">Esse componente pode ser instalado no servidor do Microsoft Application Virtualization ou localizado em uma estação de trabalho separada que tenha o MMC 3.0 e. .NET 2.0 instalado.</span><span class="sxs-lookup"><span data-stu-id="97c14-118">This component can be installed on the Microsoft Application Virtualization server or located on a separate workstation that has MMC3.0 and .NET2.0 installed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="97c14-119">Serviço Web de gerenciamento do aplicativo Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="97c14-119">Microsoft Application Virtualization Management Web Service</span></span></p></td>
<td align="left"><p><span data-ttu-id="97c14-120">O componente responsável pela comunicação de qualquer solicitação de leitura/gravação ao repositório de dados do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="97c14-120">The component responsible for communicating any read/write requests to the Application Virtualization data store.</span></span></p></td>
<td align="left"><p><span data-ttu-id="97c14-121">Esse componente pode ser instalado no servidor do Microsoft Application Virtualization ou em um computador separado com o IIS instalado.</span><span class="sxs-lookup"><span data-stu-id="97c14-121">This component can installed on the Microsoft Application Virtualization Server or on a separate computer with IIS installed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="97c14-122">Repositório de dados do Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="97c14-122">Microsoft Application Virtualization Data Store</span></span></p></td>
<td align="left"><p><span data-ttu-id="97c14-123">O componente armazenado no banco de dados SQL e responsável por armazenar todas as informações relacionadas à infraestrutura de virtualização de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97c14-123">The component stored in the SQL database and responsible for storing all information related to the Application Virtualization infrastructure.</span></span></p></td>
<td align="left"><p><span data-ttu-id="97c14-124">Essas informações incluem todos os registros de aplicativos, atribuições de aplicativos e quais grupos têm responsabilidade por gerenciar o ambiente de virtualização de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97c14-124">This information includes all application records, application assignments, and which groups have responsibility for managing the Application Virtualization environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="97c14-125">Servidor de streaming do Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="97c14-125">Microsoft Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="97c14-126">O componente responsável pela hospedagem dos pacotes do Application Virtualization para o streaming para clientes em uma filial, em que o link de volta para o servidor de gerenciamento do Application Virtualization é considerado uma WAN.</span><span class="sxs-lookup"><span data-stu-id="97c14-126">The component responsible for hosting the Application Virtualization packages for streaming to clients in a branch office, where the link back to the Application Virtualization Management Server is considered a WAN.</span></span></p></td>
<td align="left"><p><span data-ttu-id="97c14-127">Esse servidor contém somente a funcionalidade de streaming e não fornece o console de gerenciamento do Application Virtualization nem o serviço Web de gerenciamento da virtualização de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="97c14-127">This server contains streaming functionality only and provides neither the Application Virtualization Management Console nor the Application Virtualization Management Web Service.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="97c14-128">Sequenciador do Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="97c14-128">Microsoft Application Virtualization Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="97c14-129">O componente usado para monitorar e capturar a instalação de aplicativos para criar pacotes de aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="97c14-129">The component used to monitor and capture the installation of applications to create virtual application packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="97c14-130">A saída consiste nos ícones do aplicativo, um arquivo OSD contendo informações de definição do pacote, um arquivo de manifesto do pacote e o arquivo SFT que contém os arquivos de conteúdo do programa aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97c14-130">Output consists of the application’s icons, an OSD file containing package definition information, a package manifest file, and the SFT file containing the application program’s content files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="97c14-131">Cliente do Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="97c14-131">Microsoft Application Virtualization Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="97c14-132">O componente instalado no cliente da área de trabalho do Application Virtualization ou no cliente do Application Virtualization para serviços de área de trabalho remota (anteriormente conhecido como serviços de terminal) e que fornece o ambiente virtual para aplicativos virtualizados.</span><span class="sxs-lookup"><span data-stu-id="97c14-132">The component installed on the Application Virtualization Desktop Client or on the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services) and that provides the virtual environment for the virtualized applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="97c14-133">O cliente do Microsoft Application Virtualization gerencia o fluxo de pacote no cache, a atualização de publicação, o transporte e todas as interações com os servidores do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="97c14-133">The Microsoft Application Virtualization Client manages the package streaming into cache, publishing refresh, transport, and all interaction with the Application Virtualization Servers.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="97c14-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="97c14-134">Related topics</span></span>


[<span data-ttu-id="97c14-135">Cenário baseado no Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="97c14-135">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="97c14-136">Planejamento da sua solução de streaming em uma implementação baseada em Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="97c14-136">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

[<span data-ttu-id="97c14-137">Publicação de aplicativos virtuais usando os Application Virtualization Management Servers</span><span class="sxs-lookup"><span data-stu-id="97c14-137">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





