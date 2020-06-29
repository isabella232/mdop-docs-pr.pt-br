---
title: Iniciar e parar o serviço AGPM
description: Iniciar e parar o serviço AGPM
author: dansimp
ms.assetid: b9d26920-c439-4992-9a78-73e4fba8309d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2be1c2386bedd5888c0ed032479bf1237ce8289c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797681"
---
# <span data-ttu-id="43343-103">Iniciar e parar o serviço AGPM</span><span class="sxs-lookup"><span data-stu-id="43343-103">Start and Stop the AGPM Service</span></span>


<span data-ttu-id="43343-104">O serviço do AGPM é um serviço do Windows que atua como um proxy de segurança, gerenciando o acesso do cliente a objetos de política de grupo (GPOs) no ambiente de arquivamento e produção.</span><span class="sxs-lookup"><span data-stu-id="43343-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy Objects (GPOs) in the archive and production environment.</span></span>

<span data-ttu-id="43343-105">**Importante**  Parar ou desabilitar o serviço do AGPM impedirá que os clientes do AGPM realizem operações (como listagem ou edição de GPOs) pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="43343-105">**Important** Stopping or disabling the AGPM Service will prevent AGPM Clients from performing any operations (such as listing or editing GPOs) through the server.</span></span>

 

<span data-ttu-id="43343-106">Uma conta de usuário com acesso ao servidor do AGPM (o computador no qual o serviço do AGPM está instalado) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="43343-106">A user account with access to the AGPM Server (the computer on which the AGPM Service is installed) is required to complete this procedure.</span></span>

**<span data-ttu-id="43343-107">Para iniciar ou parar o serviço do AGPM</span><span class="sxs-lookup"><span data-stu-id="43343-107">To start or stop the AGPM Service</span></span>**

1.  <span data-ttu-id="43343-108">No computador em que o gerenciamento avançado de política de grupo da Microsoft-servidor (e, portanto, o serviço do AGPM) estiver instalado, clique em **Iniciar**, clique em **painel de controle**, clique em **Ferramentas administrativas**e clique em **Serviços**.</span><span class="sxs-lookup"><span data-stu-id="43343-108">On the computer on which Microsoft Advanced Group Policy Management - Server (and therefore the AGPM Service) is installed, click **Start**, click **Control Panel**, click **Administrative Tools**, and then click **Services**.</span></span>

2.  <span data-ttu-id="43343-109">Na lista de serviços, clique com o botão direito do mouse em **serviço do AGPM** e selecione **Iniciar**, **reiniciar**ou **parar**.</span><span class="sxs-lookup"><span data-stu-id="43343-109">In the list of services, right-click **AGPM Service** and select **Start**, **Restart**, or **Stop**.</span></span>

    <span data-ttu-id="43343-110">**Cuidado**  Não modifique as configurações do serviço do AGPM por meio de ferramentas e **Serviços** **administrativos** no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="43343-110">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="43343-111">Isso pode impedir que o serviço do AGPM seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="43343-111">Doing so can prevent the AGPM Service from starting.</span></span>

     

### <span data-ttu-id="43343-112">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="43343-112">Additional references</span></span>

-   [<span data-ttu-id="43343-113">Gerenciamento do serviço AGPM</span><span class="sxs-lookup"><span data-stu-id="43343-113">Managing the AGPM Service</span></span>](managing-the-agpm-service-agpm30ops.md)

 

 





