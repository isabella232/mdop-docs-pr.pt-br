---
title: Gerenciamento do serviço AGPM
description: Gerenciamento do serviço AGPM
author: dansimp
ms.assetid: a522b1f1-c57b-43aa-9d75-acc6f9bedbf9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 08749b1b698ff2ec560a5922c5e71138ad31068b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797754"
---
# <span data-ttu-id="a24c7-103">Gerenciamento do serviço AGPM</span><span class="sxs-lookup"><span data-stu-id="a24c7-103">Managing the AGPM Service</span></span>


<span data-ttu-id="a24c7-104">O serviço do AGPM é um serviço do Windows que atua como um proxy de segurança, gerenciando o acesso do cliente a objetos de política de grupo (GPOs) no ambiente de arquivamento e produção.</span><span class="sxs-lookup"><span data-stu-id="a24c7-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy Objects (GPOs) in the archive and production environment.</span></span> <span data-ttu-id="a24c7-105">Ele impõe a delegação de gerenciamento de política de grupo (AGPM) avançada e fornece um nível avançado de segurança.</span><span class="sxs-lookup"><span data-stu-id="a24c7-105">It enforces Advanced Group Policy Management (AGPM) delegation and provides an enhanced level of security.</span></span> <span data-ttu-id="a24c7-106">O serviço do AGPM está hospedado no servidor em que o Microsoft Advanced Group Policy Management-Server está instalado.</span><span class="sxs-lookup"><span data-stu-id="a24c7-106">The AGPM Service is hosted on the server on which the Microsoft Advanced Group Policy Management - Server is installed.</span></span>

<span data-ttu-id="a24c7-107">**Cuidado**  Não modifique as configurações do serviço do AGPM por meio de ferramentas e **Serviços** **administrativos** no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a24c7-107">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="a24c7-108">Isso pode impedir que o serviço do AGPM seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="a24c7-108">Doing so can prevent the AGPM Service from starting.</span></span>

 

-   [<span data-ttu-id="a24c7-109">Iniciar e parar o serviço AGPM</span><span class="sxs-lookup"><span data-stu-id="a24c7-109">Start and Stop the AGPM Service</span></span>](start-and-stop-the-agpm-service-agpm30ops.md)

-   [<span data-ttu-id="a24c7-110">Modificar o serviço AGPM</span><span class="sxs-lookup"><span data-stu-id="a24c7-110">Modify the AGPM Service</span></span>](modify-the-agpm-service-agpm30ops.md)

### <span data-ttu-id="a24c7-111">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="a24c7-111">Additional references</span></span>

-   [<span data-ttu-id="a24c7-112">Mover o servidor e o arquivo morto do AGPM</span><span class="sxs-lookup"><span data-stu-id="a24c7-112">Move the AGPM Server and the Archive</span></span>](move-the-agpm-server-and-the-archive.md)

-   [<span data-ttu-id="a24c7-113">Executar tarefas de administração de AGPM</span><span class="sxs-lookup"><span data-stu-id="a24c7-113">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm30ops.md)

 

 





