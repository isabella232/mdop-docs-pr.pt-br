---
title: Configurando o firewall para os App-V Servers
description: Configurando o firewall para os App-V Servers
author: dansimp
ms.assetid: f779c450-6c6f-46a8-ac66-5e82e0689d55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92db727eb060546ab71f2c647f2d89b662be5c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798001"
---
# <span data-ttu-id="80999-103">Configurando o firewall para os App-V Servers</span><span class="sxs-lookup"><span data-stu-id="80999-103">Configuring the Firewall for the App-V Servers</span></span>


<span data-ttu-id="80999-104">Depois de instalar o servidor de gerenciamento do Microsoft Application Virtualization (App-V) ou o servidor de streaming e configurá-lo para usar o protocolo RTSP ou RTSPs, você deve criar exceções de firewall para os programas App-V.</span><span class="sxs-lookup"><span data-stu-id="80999-104">After you install the Microsoft Application Virtualization (App-V) Management Server or Streaming Server and configure it to use the RTSP or RTSPS protocol, you must create firewall exceptions for the App-V programs.</span></span>

## <span data-ttu-id="80999-105">Configurando exceções de firewall para o servidor de gerenciamento do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="80999-105">Configuring Firewall Exceptions for Application Virtualization Management Server</span></span>


<span data-ttu-id="80999-106">Crie uma exceção de firewall para **sghwdsptr.exe** e **sghwsvr.exe**.</span><span class="sxs-lookup"><span data-stu-id="80999-106">Create a firewall exception for **sghwdsptr.exe** and **sghwsvr.exe**.</span></span> <span data-ttu-id="80999-107">Esses programas são encontrados na pasta C:\\Arquivos de Files\\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin em um sistema operacional de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="80999-107">These programs are found in the folder C:\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin on a 32-bit operating system.</span></span> <span data-ttu-id="80999-108">Se você estiver usando uma versão do sistema operacional de 64 bits, a pasta estará localizada em C:\\Arquivos de programas (x86) \\Microsoft System Center App Center Virt Management Server\\App virt gerenciamento Server\\bin.</span><span class="sxs-lookup"><span data-stu-id="80999-108">If you are using a 64-bit operating system version, the folder is located under C:\\Program Files (x86)\\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin.</span></span>

## <span data-ttu-id="80999-109">Configurando exceções de firewall para o servidor de streaming do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="80999-109">Configuring Firewall Exceptions for Application Virtualization Streaming Server</span></span>


<span data-ttu-id="80999-110">Crie uma exceção de firewall para **sglwdsptr.exe** e **sglwsvr.exe**.</span><span class="sxs-lookup"><span data-stu-id="80999-110">Create a firewall exception for **sglwdsptr.exe** and **sglwsvr.exe**.</span></span> <span data-ttu-id="80999-111">Esses programas são encontrados na pasta C:\\Arquivos de Files\\Microsoft System Center virt streaming Server\\App virt streaming Server\\bin em um sistema operacional de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="80999-111">These programs are found in the folder C:\\Program Files\\Microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin on a 32-bit operating system.</span></span> <span data-ttu-id="80999-112">Se você estiver usando uma versão do sistema operacional de 64 bits, a pasta estará localizada em C:\\Arquivos de programas (x86) \\Microsoft System Center App Virt streaming Server\\App virt streaming Server\\bin.</span><span class="sxs-lookup"><span data-stu-id="80999-112">If you are using a 64-bit operating system version, the folder is located under C:\\Program Files (x86)\\Microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin.</span></span>

## <span data-ttu-id="80999-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="80999-113">Related topics</span></span>


[<span data-ttu-id="80999-114">Como configurar os servidores para a implantação baseada em servidor</span><span class="sxs-lookup"><span data-stu-id="80999-114">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

[<span data-ttu-id="80999-115">Como instalar e configurar o aplicativo padrão</span><span class="sxs-lookup"><span data-stu-id="80999-115">How to Install and Configure the Default Application</span></span>](how-to-install-and-configure-the-default-application.md)

 

 





