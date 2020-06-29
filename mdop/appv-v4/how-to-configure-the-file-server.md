---
title: Como configurar o Servidor de Arquivos
description: Como configurar o Servidor de Arquivos
author: dansimp
ms.assetid: 0977554c-1741-411b-85e7-7e1cd017542f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a8971ad5c9f83dec4d0c77a16f1093ef7026b5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797194"
---
# <span data-ttu-id="aacf6-103">Como configurar o Servidor de Arquivos</span><span class="sxs-lookup"><span data-stu-id="aacf6-103">How to Configure the File Server</span></span>


<span data-ttu-id="aacf6-104">Você pode usar o procedimento a seguir para configurar um computador local que é usado como um compartilhamento de arquivos e transmite aplicativos para o cliente da área de trabalho do Application Virtualization e para o cliente para serviços de área de trabalho remota (anteriormente serviços de terminal).</span><span class="sxs-lookup"><span data-stu-id="aacf6-104">You can use the following procedure to configure a local computer that is used as a file share and streams applications to the Application Virtualization Desktop Client and the Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="aacf6-105">Esse cenário é usado quando você não deseja adicionar uma infraestrutura de servidor adicional ao seu ambiente de hardware existente.</span><span class="sxs-lookup"><span data-stu-id="aacf6-105">This scenario is used when you do not want to add an additional server infrastructure to your existing hardware environment.</span></span>

<span data-ttu-id="aacf6-106">Se você estiver usando um servidor de gerenciamento do Application Virtualization como um ponto de distribuição para o compartilhamento de arquivos instalado em escritórios locais, você deve configurar esse servidor para que os aplicativos virtuais possam ser transmitidos para os computadores que são usados como compartilhamentos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="aacf6-106">If you are using an Application Virtualization Management Server as a distribution point to the file share installed in local offices, you must configure this server before virtual applications can be streamed to the computers that are used as file shares.</span></span> <span data-ttu-id="aacf6-107">Ao configurar os servidores e os compartilhamentos de arquivos, você está configurando o diretório de conteúdo em que os arquivos SFT são carregados e armazenados.</span><span class="sxs-lookup"><span data-stu-id="aacf6-107">When you configure the servers and the file shares, you are setting up the content directory where the SFT files are loaded and stored.</span></span> <span data-ttu-id="aacf6-108">Os arquivos SFT contêm o aplicativo virtual (ou aplicativos).</span><span class="sxs-lookup"><span data-stu-id="aacf6-108">The SFT files contain the virtual application (or applications).</span></span>

<span data-ttu-id="aacf6-109">**Importante**  Para que os aplicativos sejam transmitidos corretamente para o cliente da área de trabalho de virtualização do aplicativo e para os serviços de área de trabalho remota, o arquivo SFT flui do diretório de conteúdo no servidor em que você armazena o aplicativo virtual; o arquivo ICO (ícone) e o arquivo OSD (Open Software Descriptor) podem ser configurados para transmitir de um servidor diferente.</span><span class="sxs-lookup"><span data-stu-id="aacf6-109">**Important** For applications to stream properly to the Application Virtualization Desktop Client and the Client for Remote Desktop Services, the SFT file streams from the content directory on the server where you store the virtual application; the ICO (icon) file and the OSD (open software descriptor) file can be configured to stream from a different server.</span></span>

 

**<span data-ttu-id="aacf6-110">Para configurar o servidor de arquivos do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="aacf6-110">To configure the Application Virtualization file server</span></span>**

1.  <span data-ttu-id="aacf6-111">Conclua o procedimento de instalação a seguir para configurar o servidor que é usado como o ponto de distribuição:</span><span class="sxs-lookup"><span data-stu-id="aacf6-111">Complete the following installation procedure to configure the server that is used as the distribution point:</span></span>

    [<span data-ttu-id="aacf6-112">Como instalar o Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="aacf6-112">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

    <span data-ttu-id="aacf6-113">**Observação**  Durante o procedimento de instalação, especifique o local do diretório \\Content na tela **caminho do conteúdo** .</span><span class="sxs-lookup"><span data-stu-id="aacf6-113">**Note** During the installation procedure, you specify the location of the \\Content directory on the **Content Path** screen.</span></span>

     

2.  <span data-ttu-id="aacf6-114">Crie um diretório \\Content, que corresponde ao diretório especificado ao instalar o servidor, em cada computador que você está usando como um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="aacf6-114">Create a \\Content directory, which corresponds to the directory you specified when you installed the server, on each computer that you are using as a file share.</span></span>

    <span data-ttu-id="aacf6-115">**Importante**  Configure os clientes da área de trabalho do Application Virtualization para transmitir aplicativos do computador que você está usando como um compartilhamento de arquivos, em vez de um servidor do Application Virtualization ou servidor IIS.</span><span class="sxs-lookup"><span data-stu-id="aacf6-115">**Important** Configure the Application Virtualization Desktop Clients to stream applications from the computer you are using as a file share rather than from an Application Virtualization Server or IIS server.</span></span>

     

3.  <span data-ttu-id="aacf6-116">Quando o diretório \\Content é criado, configure esse diretório como um compartilhamento de arquivo padrão.</span><span class="sxs-lookup"><span data-stu-id="aacf6-116">When the \\Content directory is created, configure this directory as a standard file share.</span></span>

## <span data-ttu-id="aacf6-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aacf6-117">Related topics</span></span>


[<span data-ttu-id="aacf6-118">Cenário baseado no Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="aacf6-118">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="aacf6-119">Cenário baseado em Distribuição Eletrônica de Software</span><span class="sxs-lookup"><span data-stu-id="aacf6-119">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="aacf6-120">Como configurar os Application Virtualization Management Servers</span><span class="sxs-lookup"><span data-stu-id="aacf6-120">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)

[<span data-ttu-id="aacf6-121">Como configurar os Application Virtualization Streaming Servers</span><span class="sxs-lookup"><span data-stu-id="aacf6-121">How to Configure the Application Virtualization Streaming Servers</span></span>](how-to-configure-the-application-virtualization-streaming-servers.md)

[<span data-ttu-id="aacf6-122">Como configurar o servidor para o IIS</span><span class="sxs-lookup"><span data-stu-id="aacf6-122">How to Configure the Server for IIS</span></span>](how-to-configure-the-server-for-iis.md)

 

 





