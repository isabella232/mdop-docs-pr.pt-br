---
title: Como configurar os Application Virtualization Management Servers
description: Como configurar os Application Virtualization Management Servers
author: dansimp
ms.assetid: a9f96148-bf2d-486f-98c2-23409bfb0935
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d6d54dd213efb8d5cbff5d0e730e6dc08c8d19b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797206"
---
# <span data-ttu-id="b2d8c-103">Como configurar os Application Virtualization Management Servers</span><span class="sxs-lookup"><span data-stu-id="b2d8c-103">How to Configure the Application Virtualization Management Servers</span></span>


<span data-ttu-id="b2d8c-104">Antes que aplicativos virtualizados possam ser transmitidos para o cliente da área de trabalho do Application Virtualization ou o cliente para serviços de área de trabalho remota (antes serviços de terminal), o servidor de gerenciamento do Application Virtualization deve ser configurado.</span><span class="sxs-lookup"><span data-stu-id="b2d8c-104">Before virtualized applications can be streamed to the Application Virtualization Desktop Client or the Client for Remote Desktop Services (formerly Terminal Services), the Application Virtualization Management Server must be configured.</span></span> <span data-ttu-id="b2d8c-105">Ao configurar o servidor, você está configurando o *diretório de conteúdo* em que os arquivos SFT são carregados e armazenados.</span><span class="sxs-lookup"><span data-stu-id="b2d8c-105">When you configure the server, you are setting up the *content directory* where the SFT files are loaded and stored.</span></span> <span data-ttu-id="b2d8c-106">Os arquivos SFT contêm o aplicativo virtualizado (ou aplicativos).</span><span class="sxs-lookup"><span data-stu-id="b2d8c-106">The SFT files contain the virtualized application (or applications).</span></span>

<span data-ttu-id="b2d8c-107">**Importante**  Os servidores de virtualização de aplicativos transmitem arquivos SFT para o cliente da área de trabalho e o cliente para serviços de área de trabalho remota usando somente protocolos RTSP ou RTSP.</span><span class="sxs-lookup"><span data-stu-id="b2d8c-107">**Important** Application Virtualization Servers stream SFT files to the Desktop Client and the Client for Remote Desktop Services using only RTSP or RTSPS protocols.</span></span> <span data-ttu-id="b2d8c-108">O arquivo ICO (ícone) e o arquivo OSD (Open Software Descriptor) podem ser configurados para transmitir de um arquivo ou servidor HTTP diferente.</span><span class="sxs-lookup"><span data-stu-id="b2d8c-108">The ICO (icon) file and the OSD (open software descriptor) file can be configured to stream from a different file or HTTP server.</span></span>

 

**<span data-ttu-id="b2d8c-109">Para configurar o servidor de gerenciamento do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="b2d8c-109">To configure the Application Virtualization Management Server</span></span>**

1.  <span data-ttu-id="b2d8c-110">Conclua o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="b2d8c-110">Complete the following procedure:</span></span>

    [<span data-ttu-id="b2d8c-111">Como instalar o Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="b2d8c-111">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

    <span data-ttu-id="b2d8c-112">**Observação**  Durante o procedimento de instalação, especifique o local do diretório \\Content na tela **caminho do conteúdo** .</span><span class="sxs-lookup"><span data-stu-id="b2d8c-112">**Note** During the installation procedure, you specify the location of the \\Content directory on the **Content Path** screen.</span></span>

     

2.  <span data-ttu-id="b2d8c-113">Navegue até o local que você especificou para o diretório \\Content e, se necessário, crie o diretório.</span><span class="sxs-lookup"><span data-stu-id="b2d8c-113">Navigate to the location that you specified for the \\Content directory, and if necessary, create the directory.</span></span>

3.  <span data-ttu-id="b2d8c-114">Quando o diretório de conteúdo é criado, configure esse diretório como um compartilhamento de arquivo padrão.</span><span class="sxs-lookup"><span data-stu-id="b2d8c-114">When the content directory is created, configure this directory as a standard file share.</span></span>

## <span data-ttu-id="b2d8c-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b2d8c-115">Related topics</span></span>


[<span data-ttu-id="b2d8c-116">Cenário baseado no Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="b2d8c-116">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="b2d8c-117">Requisitos de Sistema do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="b2d8c-117">Application Virtualization System Requirements</span></span>](application-virtualization-system-requirements.md)

[<span data-ttu-id="b2d8c-118">Cenário baseado em Distribuição Eletrônica de Software</span><span class="sxs-lookup"><span data-stu-id="b2d8c-118">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="b2d8c-119">Como configurar os servidores para a implantação baseada em servidor</span><span class="sxs-lookup"><span data-stu-id="b2d8c-119">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

 

 





