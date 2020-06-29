---
title: Configuração do App-V para administração segura
description: Configuração do App-V para administração segura
author: dansimp
ms.assetid: 4543fa81-c8cc-4b10-83b7-060778eb1349
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de70c1df734bbf1168fd7dacf9410d3451a8a3c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798018"
---
# <span data-ttu-id="8a3b5-103">Configuração do App-V para administração segura</span><span class="sxs-lookup"><span data-stu-id="8a3b5-103">Configuring App-V for Secure Administration</span></span>


<span data-ttu-id="8a3b5-104">Em um ambiente em que a proteção de operações administrativas é importante, o App-V permite a comunicação segura entre o serviço de gerenciamento da Web do App-V e o console de gerenciamento do App-V.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-104">In an environment where securing administrative operations is important, App-V allows for secure communication between the App-V Web Management Service and the App-V Management Console.</span></span> <span data-ttu-id="8a3b5-105">Como o serviço de gerenciamento é um aplicativo baseado na Web, ele exige a proteção do aplicativo do servidor de gerenciamento do App-V no servidor Web que hospeda o serviço de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-105">Because the Management Service is a Web-based application, it requires securing the App-V Management Server application on the Web server that hosts the Management Service.</span></span> <span data-ttu-id="8a3b5-106">Conforme mostrado na ilustração a seguir, esse processo inclui o uso de HTTPS para comunicação e a configuração do servidor IIS para permitir somente a autenticação integrada do Windows.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-106">As shown in the following illustration, this process includes using HTTPS for communication and configuring the IIS server to allow only Windows Integrated Authentication.</span></span>

![configuração de rede do serviço Web App-v](images/appvmgmtwebservice.gif)

<span data-ttu-id="8a3b5-108">O serviço de gerenciamento da Web App-V é instalado como um aplicativo baseado na Web no IIS.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-108">The App-V Web Management Service is installed as a Web-based application on IIS.</span></span> <span data-ttu-id="8a3b5-109">Para que o serviço de gerenciamento da Web ofereça suporte a conexões seguras (SSL) entre o console de gerenciamento do App-V e o serviço de gerenciamento da Web, você precisará configurar o servidor IIS onde o serviço de gerenciamento da Web está instalado e configurar o console de gerenciamento do App-V.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-109">For the Web Management Service to support secure (SSL) connections between the App-V Management Console and the Web Management Service, you will need to configure the IIS server where the Web Management Service is installed and configure the App-V Management Console.</span></span>

## <span data-ttu-id="8a3b5-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="8a3b5-110">In This Section</span></span>


<a href="" id="configuring-certificates-to-support-the-app-v-web-management-service"></a>[<span data-ttu-id="8a3b5-111">Configuração de certificados para dar suporte ao Serviço de Gerenciamento da Web do App-V</span><span class="sxs-lookup"><span data-stu-id="8a3b5-111">Configuring Certificates to Support the App-V Web Management Service</span></span>](configuring-certificates-to-support-the-app-v-web-management-service.md)  
<span data-ttu-id="8a3b5-112">Fornece informações úteis sobre como configurar certificados para dar suporte a conexões baseadas em SSL, para ajudar a proteger a comunicação do serviço de gerenciamento da Web do App-V.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-112">Provides helpful information about configuring certificates to support SSL-based connections, to help secure communication for the App-V Web Management Service.</span></span>

<a href="" id="how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment"></a>[<span data-ttu-id="8a3b5-113">Como instalar e configurar o Console de Gerenciamento do App-V para um ambiente mais seguro</span><span class="sxs-lookup"><span data-stu-id="8a3b5-113">How to Install and Configure the App-V Management Console for a More Secure Environment</span></span>](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)  
<span data-ttu-id="8a3b5-114">Fornece um procedimento passo a passo para se conectar a um serviço de gerenciamento da Web do App-V usando uma conexão segura.</span><span class="sxs-lookup"><span data-stu-id="8a3b5-114">Provides a step-by-step procedure for connecting to an App-V Web Management Service by using a secure connection.</span></span>

 

 





