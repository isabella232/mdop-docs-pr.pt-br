---
title: Visão geral do Application Virtualization
description: Visão geral do Application Virtualization
author: dansimp
ms.assetid: 80545ef4-cf4c-420c-88d6-48e9f226051f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f3719a817137edfd76b1b972e966c685581c58e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796850"
---
# <span data-ttu-id="f65dc-103">Visão geral do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f65dc-103">Overview of Application Virtualization</span></span>


<span data-ttu-id="f65dc-104">O Microsoft Application Virtualization (App-V) pode disponibilizar aplicativos para os computadores dos usuários finais sem precisar instalar os aplicativos diretamente nesses computadores.</span><span class="sxs-lookup"><span data-stu-id="f65dc-104">Microsoft Application Virtualization (App-V) can make applications available to end user computers without having to install the applications directly on those computers.</span></span> <span data-ttu-id="f65dc-105">Isso se tornou possível por meio de um processo conhecido como *sequenciamento do aplicativo, o*que permite que cada aplicativo seja executado em seu próprio ambiente virtual autocontido no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="f65dc-105">This is made possible through a process known as *sequencing the application*, which enables each application to run in its own self-contained virtual environment on the client computer.</span></span> <span data-ttu-id="f65dc-106">Os aplicativos sequenciados são isolados uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="f65dc-106">The sequenced applications are isolated from each other.</span></span> <span data-ttu-id="f65dc-107">Isso elimina conflitos de aplicativos, mas os aplicativos ainda podem interagir com o computador cliente.</span><span class="sxs-lookup"><span data-stu-id="f65dc-107">This eliminates application conflicts, but the applications can still interact with the client computer.</span></span>

<span data-ttu-id="f65dc-108">O cliente App-V é o recurso que permite que o usuário final interaja com os aplicativos após eles terem sido publicados no computador.</span><span class="sxs-lookup"><span data-stu-id="f65dc-108">The App-V client is the feature that lets the end user interact with the applications after they have been published to the computer.</span></span> <span data-ttu-id="f65dc-109">O cliente gerencia o ambiente virtual no qual os aplicativos virtualizados são executados em cada computador.</span><span class="sxs-lookup"><span data-stu-id="f65dc-109">The client manages the virtual environment in which the virtualized applications run on each computer.</span></span> <span data-ttu-id="f65dc-110">Após a instalação do cliente em um computador, os aplicativos devem ser disponibilizados para o computador por meio de um processo conhecido como *publicação*, o que permite que o usuário final execute os aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="f65dc-110">After the client has been installed on a computer, the applications must be made available to the computer through a process known as *publishing*, which enables the end user to run the virtual applications.</span></span> <span data-ttu-id="f65dc-111">O processo de publicação copia os ícones do aplicativo virtual e os atalhos para o computador, geralmente na área de trabalho do Windows ou no menu **Iniciar** , e também copia as informações de definição do pacote e Associação de tipo de arquivo para o computador.</span><span class="sxs-lookup"><span data-stu-id="f65dc-111">The publishing process copies the virtual application icons and shortcuts to the computer—typically on the Windows desktop or on the **Start** menu—and also copies the package definition and file type association information to the computer.</span></span> <span data-ttu-id="f65dc-112">A publicação também torna o conteúdo do pacote do aplicativo disponível para o computador do usuário final.</span><span class="sxs-lookup"><span data-stu-id="f65dc-112">Publishing also makes the application package content available to the end user’s computer.</span></span>

<span data-ttu-id="f65dc-113">O conteúdo do pacote do aplicativo virtual pode ser copiado para um ou mais servidores de virtualização de aplicativos para que ele possa ser transmitido para os clientes sob demanda e armazenado localmente em cache.</span><span class="sxs-lookup"><span data-stu-id="f65dc-113">The virtual application package content can be copied onto one or more Application Virtualization servers so that it can be streamed down to the clients on demand and cached locally.</span></span> <span data-ttu-id="f65dc-114">Os servidores de arquivos e os servidores Web também podem ser usados como servidores de streaming ou o conteúdo pode ser copiado diretamente para o computador do usuário final, por exemplo, se você estiver usando um sistema de distribuição de software eletrônico, como o Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f65dc-114">File servers and Web servers can also be used as streaming servers, or the content can be copied directly to the end user’s computer—for example, if you are using an electronic software distribution system, such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="f65dc-115">Em uma implementação de vários servidores, manter o conteúdo do pacote e mantê-lo atualizado em todos os servidores de streaming requer uma solução de gerenciamento de pacotes abrangente.</span><span class="sxs-lookup"><span data-stu-id="f65dc-115">In a multi-server implementation, maintaining the package content and keeping it up to date on all the streaming servers requires a comprehensive package management solution.</span></span> <span data-ttu-id="f65dc-116">Dependendo do tamanho da sua organização, talvez seja necessário ter muitos aplicativos virtuais disponíveis para os usuários finais localizados em todo o mundo.</span><span class="sxs-lookup"><span data-stu-id="f65dc-116">Depending on the size of your organization, you might need to have many virtual applications available to end users located all over the world.</span></span> <span data-ttu-id="f65dc-117">Gerenciar os pacotes para garantir que os aplicativos apropriados estejam disponíveis para todos os usuários onde e quando precisarem acessá-los é, portanto, um requisito importante.</span><span class="sxs-lookup"><span data-stu-id="f65dc-117">Managing the packages to ensure that the appropriate applications are available to all users where and when they need access to them is therefore an important requirement.</span></span>

## <span data-ttu-id="f65dc-118">Recursos do sistema do Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f65dc-118">Microsoft Application Virtualization System Features</span></span>


<span data-ttu-id="f65dc-119">A tabela a seguir descreve os principais recursos do sistema de gerenciamento do Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f65dc-119">The following table describes the primary features of the Microsoft Application Virtualization Management System.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f65dc-120">Recurso</span><span class="sxs-lookup"><span data-stu-id="f65dc-120">Feature</span></span></th>
<th align="left"><span data-ttu-id="f65dc-121">Função</span><span class="sxs-lookup"><span data-stu-id="f65dc-121">Function</span></span></th>
<th align="left"><span data-ttu-id="f65dc-122">Informações adicionais</span><span class="sxs-lookup"><span data-stu-id="f65dc-122">Additional Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f65dc-123">Servidor de gerenciamento do Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f65dc-123">Microsoft Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="f65dc-124">Responsável por transmitir o conteúdo do pacote e publicar os atalhos e associações de tipo de arquivo para o cliente do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f65dc-124">Responsible for streaming the package content and publishing the shortcuts and file type associations to the Application Virtualization client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f65dc-125">O servidor de gerenciamento do Application Virtualization dá suporte à atualização ativa, ao gerenciamento de licenças e a um banco de dados que pode ser usado para relatórios.</span><span class="sxs-lookup"><span data-stu-id="f65dc-125">The Application Virtualization Management Server supports active upgrade, License Management, and a database that can be used for reporting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f65dc-126">Pasta de conteúdo </strong></span><span class="sxs-lookup"><span data-stu-id="f65dc-126">Content</strong> folder</span></span></p></td>
<td align="left"><p><span data-ttu-id="f65dc-127">Indica o local dos pacotes do Application Virtualization para streaming.</span><span class="sxs-lookup"><span data-stu-id="f65dc-127">Indicates the location of the Application Virtualization packages for streaming.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f65dc-128">Essa pasta pode ser localizada em um compartilhamento ou em um servidor de gerenciamento do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f65dc-128">This folder can be located on a share on or off the Application Virtualization Management Server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f65dc-129">Console de gerenciamento do Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f65dc-129">Microsoft Application Virtualization Management Console</span></span></p></td>
<td align="left"><p><span data-ttu-id="f65dc-130">Este console é uma ferramenta de gerenciamento de snap-in do MMC 3,0 usada para administração do Microsoft Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="f65dc-130">This console is an MMC 3.0 snap-in management tool used for Microsoft Application Virtualization Server administration.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f65dc-131">Essa ferramenta pode ser instalada no servidor do Microsoft Application Virtualization ou em uma estação de trabalho separada que tenha o Microsoft Management Console (MMC) 3.0 e a Microsoft. NETFramework 2,0 instalado.</span><span class="sxs-lookup"><span data-stu-id="f65dc-131">This tool can be installed on the Microsoft Application Virtualization server or located on a separate workstation that has Microsoft Management Console (MMC)3.0 and Microsoft .NETFramework 2.0 installed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f65dc-132">Serviço Web de gerenciamento do aplicativo Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f65dc-132">Microsoft Application Virtualization Management Web Service</span></span></p></td>
<td align="left"><p><span data-ttu-id="f65dc-133">Responsável por comunicar qualquer solicitação de leitura e gravação ao repositório de dados do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f65dc-133">Responsible for communicating any read and write requests to the Application Virtualization data store.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f65dc-134">O serviço Web de gerenciamento pode ser instalado no servidor de gerenciamento do Microsoft Application Virtualization ou em um computador separado que tenha o Microsoft ISS (serviços de informações da Internet) instalado.</span><span class="sxs-lookup"><span data-stu-id="f65dc-134">The Management Web Service can be installed on the Microsoft Application Virtualization Management server or on a separate computer that has Microsoft Internet Information Services (IIS) installed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f65dc-135">Repositório de dados do Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f65dc-135">Microsoft Application Virtualization Data Store</span></span></p></td>
<td align="left"><p><span data-ttu-id="f65dc-136">O banco de dados do aplicativo do SQL Server do App-V responsável por armazenar todas as informações relacionadas à infraestrutura de virtualização do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f65dc-136">The App-V SQL Server database responsible for storing all information related to the Application Virtualization infrastructure.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f65dc-137">Essas informações incluem todos os registros de aplicativos, atribuições de aplicativos e quais grupos têm responsabilidade por gerenciar o ambiente de virtualização de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f65dc-137">This information includes all application records, application assignments, and which groups have responsibility for managing the Application Virtualization environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f65dc-138">Servidor de streaming do Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f65dc-138">Microsoft Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="f65dc-139">Responsável pela hospedagem dos pacotes do Application Virtualization para transmitir para clientes em uma filial, em que o link de volta para o servidor de gerenciamento do Application Virtualization é considerado uma conexão de rede de longa distância.</span><span class="sxs-lookup"><span data-stu-id="f65dc-139">Responsible for hosting the Application Virtualization packages for streaming to clients in a branch office, where the link back to the Application Virtualization Management Server is considered a wide area networks (WAN) connection.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f65dc-140">Esse servidor contém somente a funcionalidade de streaming e não fornece o console de gerenciamento do Application Virtualization nem o serviço Web de gerenciamento da virtualização de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f65dc-140">This server contains streaming functionality only and provides neither the Application Virtualization Management Console nor the Application Virtualization Management Web Service.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f65dc-141">Sequenciador do Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f65dc-141">Microsoft Application Virtualization Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="f65dc-142">O sequenciador é usado para monitorar e capturar a instalação de aplicativos para criar pacotes de aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="f65dc-142">The sequencer is used to monitor and capture the installation of applications to create virtual application packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f65dc-143">A saída consiste nos ícones do aplicativo, um arquivo. OSD que contém informações de definição do pacote, um arquivo de manifesto do pacote e o arquivo. sft que contém os arquivos de conteúdo do programa aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f65dc-143">The output consists of the application’s icons, an .osd file that contains package definition information, a package manifest file, and the .sft file that contains the application program’s content files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f65dc-144">Cliente do Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f65dc-144">Microsoft Application Virtualization Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="f65dc-145">O cliente da área de trabalho do Application Virtualization e o cliente do Application Virtualization para serviços de área de trabalho remota fornecem e gerenciam o ambiente virtual para aplicativos virtualizados.</span><span class="sxs-lookup"><span data-stu-id="f65dc-145">The Application Virtualization Desktop Client and the Application Virtualization Client for Remote Desktop Services provide and manage the virtual environment for the virtualized applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="f65dc-146">O cliente do Microsoft Application Virtualization gerencia o fluxo de pacote no cache, a atualização de publicação, o transporte e todas as interações com os servidores do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f65dc-146">The Microsoft Application Virtualization client manages the package streaming into cache, publishing refresh, transport, and all interaction with the Application Virtualization servers.</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 





