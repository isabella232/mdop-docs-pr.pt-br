---
title: Como configurar os Application Virtualization Streaming Servers
description: Como configurar os Application Virtualization Streaming Servers
author: dansimp
ms.assetid: 3e2dde35-9d72-40ba-9fdf-d0338bd4d561
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0ec5497b010d18bcba60e81e96cbe6334c27fb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797202"
---
# <span data-ttu-id="13a1d-103">Como configurar os Application Virtualization Streaming Servers</span><span class="sxs-lookup"><span data-stu-id="13a1d-103">How to Configure the Application Virtualization Streaming Servers</span></span>


<span data-ttu-id="13a1d-104">Antes que os aplicativos virtuais possam ser transmitidos para o cliente da área de trabalho do Application Virtualization ou o cliente para serviços de área de trabalho remota (antes serviços de terminal), os servidores de streaming do Application Virtualization devem ser configurados.</span><span class="sxs-lookup"><span data-stu-id="13a1d-104">Before virtual applications can be streamed to the Application Virtualization Desktop Client or the Client for Remote Desktop Services (formerly Terminal Services), the Application Virtualization Streaming Servers must be configured.</span></span> <span data-ttu-id="13a1d-105">Ao configurar os servidores, você está configurando o *diretório de conteúdo* em que os arquivos SFT são carregados e armazenados.</span><span class="sxs-lookup"><span data-stu-id="13a1d-105">When you configure the servers, you are setting up the *content directory* where the SFT files are loaded and stored.</span></span> <span data-ttu-id="13a1d-106">Os arquivos SFT contêm o aplicativo virtual (ou aplicativos).</span><span class="sxs-lookup"><span data-stu-id="13a1d-106">The SFT files contain the virtual application (or applications).</span></span>

<span data-ttu-id="13a1d-107">**Importante**  Os servidores de virtualização de aplicativos transmitem arquivos SFT para o cliente da área de trabalho e o cliente para serviços de área de trabalho remota usando somente protocolos RTSP ou RTSP.</span><span class="sxs-lookup"><span data-stu-id="13a1d-107">**Important** Application Virtualization Servers stream SFT files to the Desktop Client and the Client for Remote Desktop Services using only RTSP or RTSPS protocols.</span></span> <span data-ttu-id="13a1d-108">O arquivo ICO (ícone) e o arquivo OSD (Open Software Descriptor) podem ser configurados para transmitir de um arquivo ou servidor HTTP diferente.</span><span class="sxs-lookup"><span data-stu-id="13a1d-108">The ICO (icon) file and the OSD (open software descriptor) file can be configured to stream from a different file or HTTP server.</span></span>

 

**<span data-ttu-id="13a1d-109">Para configurar os servidores de streaming do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="13a1d-109">To configure the Application Virtualization Streaming Servers</span></span>**

1.  <span data-ttu-id="13a1d-110">Conclua o procedimento de instalação do servidor de streaming do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="13a1d-110">Complete the installation procedure for the Application Virtualization Streaming Server.</span></span> <span data-ttu-id="13a1d-111">Durante o procedimento de instalação, especifique o local do diretório \\Content na tela **caminho do conteúdo** .</span><span class="sxs-lookup"><span data-stu-id="13a1d-111">During the installation procedure, you specify the location of the \\Content directory on the **Content Path** screen.</span></span>

2.  <span data-ttu-id="13a1d-112">Navegue até o local que você especificou para o diretório \\Content e, se necessário, crie o diretório.</span><span class="sxs-lookup"><span data-stu-id="13a1d-112">Navigate to the location that you specified for the \\Content directory, and if you have to, create the directory.</span></span>

3.  <span data-ttu-id="13a1d-113">Quando o diretório de conteúdo é criado, configure esse diretório como um compartilhamento de arquivo padrão.</span><span class="sxs-lookup"><span data-stu-id="13a1d-113">When the Content directory is created, configure this directory as a standard file share.</span></span>

4.  <span data-ttu-id="13a1d-114">Configure as permissões do sistema de arquivos NTFS para o diretório de conteúdo e as pastas do pacote no diretório de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="13a1d-114">Configure the NTFS file system permissions to the Content directory and the package folders under the Content directory.</span></span> <span data-ttu-id="13a1d-115">Você deve usar grupos de segurança nos serviços de domínio Active Directory que definem quais usuários podem acessar cada aplicativo.</span><span class="sxs-lookup"><span data-stu-id="13a1d-115">You should use Security Groups in Active Directory Domain Services that define which users can access each application.</span></span>

## <span data-ttu-id="13a1d-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="13a1d-116">Related topics</span></span>


[<span data-ttu-id="13a1d-117">Cenário baseado no Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="13a1d-117">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="13a1d-118">Cenário baseado em Distribuição Eletrônica de Software</span><span class="sxs-lookup"><span data-stu-id="13a1d-118">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="13a1d-119">Como configurar os Application Virtualization Management Servers</span><span class="sxs-lookup"><span data-stu-id="13a1d-119">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)

[<span data-ttu-id="13a1d-120">Como configurar o Servidor de Arquivos</span><span class="sxs-lookup"><span data-stu-id="13a1d-120">How to Configure the File Server</span></span>](how-to-configure-the-file-server.md)

[<span data-ttu-id="13a1d-121">Como configurar o servidor para o IIS</span><span class="sxs-lookup"><span data-stu-id="13a1d-121">How to Configure the Server for IIS</span></span>](how-to-configure-the-server-for-iis.md)

 

 





