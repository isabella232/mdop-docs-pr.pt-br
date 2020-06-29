---
title: Como Carregar Arquivos e Pacotes
description: Como Carregar Arquivos e Pacotes
author: dansimp
ms.assetid: f86f5bf1-99a4-44d7-ae2f-e6049c482f68
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9427fd8089ec9c22d7d379b15ae94bf421ca2d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797085"
---
# <span data-ttu-id="c9eb6-103">Como Carregar Arquivos e Pacotes</span><span class="sxs-lookup"><span data-stu-id="c9eb6-103">How to Load Files and Packages</span></span>


<span data-ttu-id="c9eb6-104">Você pode usar o procedimento a seguir para carregar arquivos e pacotes em servidores de virtualização de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c9eb6-104">You can use the following procedure to load files and packages on Application Virtualization Servers.</span></span>

<span data-ttu-id="c9eb6-105">**Observação**  Durante o processo de instalação, você especificou o local do diretório \\Content na página **caminho do conteúdo** .</span><span class="sxs-lookup"><span data-stu-id="c9eb6-105">**Note** During the installation process, you specified the location of the \\Content directory on the **Content Path** page.</span></span> <span data-ttu-id="c9eb6-106">Esse diretório deve ser criado e configurado como um compartilhamento de arquivo padrão antes de você apontar para sua localização.</span><span class="sxs-lookup"><span data-stu-id="c9eb6-106">This directory should be created and configured as a standard file share before you point to its location.</span></span>

 

**<span data-ttu-id="c9eb6-107">Para carregar arquivos e pacotes</span><span class="sxs-lookup"><span data-stu-id="c9eb6-107">To load files and packages</span></span>**

1.  <span data-ttu-id="c9eb6-108">No computador do qual você irá transmitir aplicativos, navegue até o local que você especificou para o diretório \\Content.</span><span class="sxs-lookup"><span data-stu-id="c9eb6-108">On the computer from which you will stream applications, navigate to the location that you specified for the \\Content directory.</span></span> <span data-ttu-id="c9eb6-109">Se necessário, crie o diretório e configure-o como um compartilhamento de arquivo padrão.</span><span class="sxs-lookup"><span data-stu-id="c9eb6-109">If necessary, create the directory and configure it as a standard file share.</span></span>

2.  <span data-ttu-id="c9eb6-110">Mova os arquivos SFT dos aplicativos e pacotes virtuais para o diretório \\Content.</span><span class="sxs-lookup"><span data-stu-id="c9eb6-110">Move the SFT files for the virtual applications and packages to the \\Content directory.</span></span> <span data-ttu-id="c9eb6-111">Para manter os arquivos SFT organizados e evitar confusão, coloque aplicativos e pacotes em subpastas dedicadas.</span><span class="sxs-lookup"><span data-stu-id="c9eb6-111">To keep the SFT files organized and to avoid confusion, put applications and packages in dedicated subfolders.</span></span>

3.  <span data-ttu-id="c9eb6-112">Carregue os aplicativos e pacotes de acordo com os requisitos do seu cenário e configuração, considerando as seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="c9eb6-112">Load the applications and packages according to the requirements of your scenario and configuration, considering the following conditions:</span></span>

    -   <span data-ttu-id="c9eb6-113">Se seus aplicativos e pacotes estiverem armazenados em um servidor de gerenciamento do Application Virtualization (App-V), carregue-os pelo console de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="c9eb6-113">If your applications and packages are stored on an Application Virtualization (App-V) Management Server, load them through the Management Console.</span></span> <span data-ttu-id="c9eb6-114">Para obter mais informações, consulte [como carregar ou descarregar um aplicativo](how-to-load-or-unload-an-application.md) ou [como carregar aplicativos virtuais na área de notificação da área de trabalho](how-to-load-virtual-applications-from-the-desktop-notification-area.md).</span><span class="sxs-lookup"><span data-stu-id="c9eb6-114">For more information, see [How to Load or Unload an Application](how-to-load-or-unload-an-application.md) or [How to Load Virtual Applications from the Desktop Notification Area](how-to-load-virtual-applications-from-the-desktop-notification-area.md).</span></span>

    -   <span data-ttu-id="c9eb6-115">Se seus aplicativos estiverem armazenados em um servidor de streaming App-V, um servidor Web ou um computador configurado como um servidor de arquivos, os aplicativos poderão ser carregados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c9eb6-115">If your applications are stored on an App-V Streaming Server, a Web server, or a computer configured as a file server, the applications can be automatically loaded.</span></span>

        <span data-ttu-id="c9eb6-116">**Observação**  O servidor de streaming App-V sonda automaticamente o diretório \\Content para aplicativos e pacotes e coloca essas informações na RAM para atender às solicitações do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c9eb6-116">**Note** The App-V Streaming Server automatically polls the \\Content directory for applications and packages and puts this information in RAM to service application requests.</span></span>

        <span data-ttu-id="c9eb6-117">Os clientes do App-V devem ser configurados corretamente para recuperar aplicativos e pacotes de servidores Web e servidores de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c9eb6-117">The App-V Clients must be properly configured to retrieve applications and packages from Web servers and file servers.</span></span> <span data-ttu-id="c9eb6-118">Para obter mais informações, consulte [como configurar o cliente para a recuperação de pacotes de aplicativos](how-to-configure-the-client-for-application-package-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="c9eb6-118">For more information, see [How to Configure the Client for Application Package Retrieval](how-to-configure-the-client-for-application-package-retrieval.md).</span></span>

         

## <span data-ttu-id="c9eb6-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9eb6-119">Related topics</span></span>


[<span data-ttu-id="c9eb6-120">Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="c9eb6-120">Application Virtualization Server</span></span>](application-virtualization-server.md)

 

 





