---
title: Fazer backup do arquivo morto
description: Fazer backup do arquivo morto
author: dansimp
ms.assetid: 538d85eb-3596-4c1d-bbd7-26bc28857c28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c6888d61e126d603aefa4e818f1070c5a493ea6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797480"
---
# <span data-ttu-id="051d2-103">Fazer backup do arquivo morto</span><span class="sxs-lookup"><span data-stu-id="051d2-103">Back Up the Archive</span></span>


<span data-ttu-id="051d2-104">Para ajudar na recuperação do arquivo para o gerenciamento avançado de política de grupo (AGPM) se houver um desastre, um administrador do AGPM (controle total) deve fazer o backup do arquivamento com frequência.</span><span class="sxs-lookup"><span data-stu-id="051d2-104">To help in the recovery of the archive for Advanced Group Policy Management (AGPM) if there is a disaster, an AGPM Administrator (Full Control) should back up the archive frequently.</span></span> <span data-ttu-id="051d2-105">Por padrão, o arquivo morto é criado no%ProgramData%\\Microsoft\\AGPM.</span><span class="sxs-lookup"><span data-stu-id="051d2-105">By default, the archive is created in %ProgramData%\\Microsoft\\AGPM.</span></span> <span data-ttu-id="051d2-106">No entanto, você pode especificar um caminho diferente durante a configuração do gerenciamento avançado de política de grupo da Microsoft-servidor.</span><span class="sxs-lookup"><span data-stu-id="051d2-106">However, you can specify a different path during the setup of Microsoft Advanced Group Policy Management - Server.</span></span>

<span data-ttu-id="051d2-107">Uma conta de usuário que tem acesso ao servidor do AGPM – o computador no qual o serviço do AGPM está instalado — e para a pasta que contém o arquivo morto é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="051d2-107">A user account that has access to both the AGPM Server—the computer on which the AGPM Service is installed—and to the folder that contains the archive is required to complete this procedure.</span></span>

**<span data-ttu-id="051d2-108">Para fazer backup do arquivo morto</span><span class="sxs-lookup"><span data-stu-id="051d2-108">To back up the archive</span></span>**

1.  <span data-ttu-id="051d2-109">Interrompa o serviço do AGPM.</span><span class="sxs-lookup"><span data-stu-id="051d2-109">Stop the AGPM Service.</span></span> <span data-ttu-id="051d2-110">Para obter mais informações, consulte [Iniciar e interromper o serviço do AGPM](start-and-stop-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="051d2-110">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

2.  <span data-ttu-id="051d2-111">Faça backup da pasta arquivo morto usando o Windows Explorer, xcopy, Windows Server® backup ou outra ferramenta de backup.</span><span class="sxs-lookup"><span data-stu-id="051d2-111">Back up the archive folder by using Windows Explorer, Xcopy, Windows Server® Backup, or another backup tool.</span></span> <span data-ttu-id="051d2-112">Certifique-se de fazer backup dos arquivos ocultos, do sistema e somente leitura.</span><span class="sxs-lookup"><span data-stu-id="051d2-112">Make sure that you back up hidden, system, and read-only files.</span></span>

3.  <span data-ttu-id="051d2-113">Armazene o backup do arquivo morto em um local seguro.</span><span class="sxs-lookup"><span data-stu-id="051d2-113">Store the archive backup in a secure location.</span></span>

4.  <span data-ttu-id="051d2-114">Reinicie o serviço do AGPM.</span><span class="sxs-lookup"><span data-stu-id="051d2-114">Restart the AGPM Service.</span></span> <span data-ttu-id="051d2-115">Para obter mais informações, consulte [Iniciar e interromper o serviço do AGPM](start-and-stop-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="051d2-115">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

<span data-ttu-id="051d2-116">**Observação**  Se um administrador do AGPM faz o backup do arquivo raramente, os objetos de política de grupo (GPOs) no backup do arquivo morto não serão atuais.</span><span class="sxs-lookup"><span data-stu-id="051d2-116">**Note** If an AGPM Administrator backs up the archive infrequently, the Group Policy Objects (GPOs) in the archive backup will not be current.</span></span> <span data-ttu-id="051d2-117">Para garantir que o backup do arquivo morto esteja atualizado, faça backup do arquivamento como parte da estratégia de backup diário da sua organização.</span><span class="sxs-lookup"><span data-stu-id="051d2-117">To better ensure that the archive backup is current, back up the archive as part of your organization’s daily backup strategy.</span></span>

 

### <span data-ttu-id="051d2-118">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="051d2-118">Additional references</span></span>

-   [<span data-ttu-id="051d2-119">Restaurar o arquivo morto de um backup</span><span class="sxs-lookup"><span data-stu-id="051d2-119">Restore the Archive from a Backup</span></span>](restore-the-archive-from-a-backup-agpm40.md)

-   [<span data-ttu-id="051d2-120">Mover o servidor e o arquivo morto do AGPM</span><span class="sxs-lookup"><span data-stu-id="051d2-120">Move the AGPM Server and the Archive</span></span>](move-the-agpm-server-and-the-archive-agpm40.md)

-   [<span data-ttu-id="051d2-121">Gerenciamento do arquivo morto</span><span class="sxs-lookup"><span data-stu-id="051d2-121">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





