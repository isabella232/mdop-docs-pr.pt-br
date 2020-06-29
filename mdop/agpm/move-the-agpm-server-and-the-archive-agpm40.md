---
title: Mover o servidor e o arquivo morto do AGPM
description: Mover o servidor e o arquivo morto do AGPM
author: dansimp
ms.assetid: 9ec48d3a-c293-45f0-8939-32ccdc062303
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 61ad2eb6e0ea46eef89379894a99469254e0fd5e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799091"
---
# <span data-ttu-id="31aec-103">Mover o servidor e o arquivo morto do AGPM</span><span class="sxs-lookup"><span data-stu-id="31aec-103">Move the AGPM Server and the Archive</span></span>


<span data-ttu-id="31aec-104">Se você estiver substituindo o servidor do AGPM e o servidor no qual o arquivo está hospedado, será necessário mover o serviço do AGPM e o arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="31aec-104">If you are replacing the AGPM Server and the server on which the archive is hosted, you must move the AGPM Service and the archive.</span></span> <span data-ttu-id="31aec-105">Se preferir, você pode mover o serviço do AGPM e o arquivamento separadamente.</span><span class="sxs-lookup"><span data-stu-id="31aec-105">If you prefer, you can move the AGPM Service and the archive separately.</span></span>

**<span data-ttu-id="31aec-106">Observação</span><span class="sxs-lookup"><span data-stu-id="31aec-106">Note</span></span>**  
-   <span data-ttu-id="31aec-107">O servidor do AGPM é o computador que hospeda o serviço do AGPM e o computador no qual o gerenciamento avançado de política de grupo da Microsoft – servidor está instalado.</span><span class="sxs-lookup"><span data-stu-id="31aec-107">The AGPM Server is the computer that hosts the AGPM Service and the computer on which Microsoft Advanced Group Policy Management – Server is installed.</span></span>

-   <span data-ttu-id="31aec-108">Por padrão, o arquivo morto é hospedado no servidor do AGPM, mas você pode especificar um caminho de arquivo morto para hospedá-lo em outro servidor em vez disso.</span><span class="sxs-lookup"><span data-stu-id="31aec-108">By default, the archive is hosted on the AGPM Server, but you can specify an archive path to host it on another server instead.</span></span>

 

<span data-ttu-id="31aec-109">Uma conta de usuário que é membro do grupo Domain admins e tem acesso aos servidores AGPM anteriores e novos necessários para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="31aec-109">A user account that is a member of the Domain Admins group and has access to the previous and new AGPM Servers is required to complete this procedure.</span></span> <span data-ttu-id="31aec-110">Além disso, você deve fornecer credenciais para que a conta de serviço do AGPM seja usada pelo novo servidor do AGPM para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="31aec-110">Additionally, you must provide credentials for the AGPM Service Account to be used by the new AGPM Server to complete this procedure.</span></span>

**<span data-ttu-id="31aec-111">Para mover o serviço do AGPM e o arquivo para um servidor ou servidores diferentes</span><span class="sxs-lookup"><span data-stu-id="31aec-111">To move the AGPM Service and the archive to a different server or servers</span></span>**

1.  <span data-ttu-id="31aec-112">Faça backup do arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="31aec-112">Back up the archive.</span></span> <span data-ttu-id="31aec-113">Para obter mais informações, consulte [fazer backup do arquivo morto](back-up-the-archive-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="31aec-113">For more information, see [Back Up the Archive](back-up-the-archive-agpm40.md).</span></span>

2.  <span data-ttu-id="31aec-114">Mover o serviço do AGPM:</span><span class="sxs-lookup"><span data-stu-id="31aec-114">Move the AGPM Service:</span></span>

    1.  <span data-ttu-id="31aec-115">Interrompa o serviço do AGPM.</span><span class="sxs-lookup"><span data-stu-id="31aec-115">Stop the AGPM Service.</span></span> <span data-ttu-id="31aec-116">Para obter mais informações, consulte [Iniciar e interromper o serviço do AGPM](start-and-stop-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="31aec-116">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

    2.  <span data-ttu-id="31aec-117">Instale o gerenciamento avançado de política de grupo da Microsoft-servidor no novo servidor que hospedará o serviço do AGPM.</span><span class="sxs-lookup"><span data-stu-id="31aec-117">Install Microsoft Advanced Group Policy Management - Server on the new server that will host the AGPM Service.</span></span> <span data-ttu-id="31aec-118">Durante esse processo, você especifica o novo caminho de arquivo morto, o local para o arquivo morto em relação ao servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="31aec-118">During this process, you specify the new archive path, the location for the archive in relation to the AGPM Server.</span></span> <span data-ttu-id="31aec-119">Para obter mais informações, consulte [o guia passo a passo para o 4,0](https://go.microsoft.com/fwlink/?LinkId=153505) (guia de planejamento e gerenciamento avançado de política de grupo https://go.microsoft.com/fwlink/?LinkId=153505) da Microsoft [para o gerenciamento avançado de política de grupo da Microsoft](https://go.microsoft.com/fwlink/?LinkId=156883) ( https://go.microsoft.com/fwlink/?LinkId=156883) .</span><span class="sxs-lookup"><span data-stu-id="31aec-119">For more information, see [Step-by-Step Guide for Microsoft Advanced Group Policy Management 4.0](https://go.microsoft.com/fwlink/?LinkId=153505) (https://go.microsoft.com/fwlink/?LinkId=153505) and [Planning Guide for Microsoft Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=156883) (https://go.microsoft.com/fwlink/?LinkId=156883).</span></span>

    3.  <span data-ttu-id="31aec-120">Um administrador do AGPM (controle total) deve configurar a conexão do servidor do AGPM para todos os administradores de política de grupo que usarão o novo servidor do AGPM e removerão a conexão do servidor do AGPM antigo, ou o administrador da política de grupo deve configurar manualmente a nova conexão do servidor do AGPM e remover a conexão do servidor do AGPM antigo para o snap-in do AGPM no computador.</span><span class="sxs-lookup"><span data-stu-id="31aec-120">Either an AGPM Administrator (Full Control) must configure the AGPM Server connection for all Group Policy administrators who will use the new AGPM Server and remove the connection for the old AGPM Server, or else each Group Policy administrator must manually configure the new AGPM Server connection and remove the old AGPM Server connection for the AGPM snap-in on their computer.</span></span> <span data-ttu-id="31aec-121">Para obter mais informações, consulte [Configurar conexões do servidor de AGPM](configure-agpm-server-connections-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="31aec-121">For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

        <span data-ttu-id="31aec-122">**Observação**  Como prática recomendada, você deve desinstalar o gerenciamento avançado de política de grupo da Microsoft – servidor do servidor do AGPM anterior.</span><span class="sxs-lookup"><span data-stu-id="31aec-122">**Note** As a best practice, you should uninstall Microsoft Advanced Group Policy Management – Server from the previous AGPM Server.</span></span> <span data-ttu-id="31aec-123">Isso garantirá que o serviço do AGPM não pode ser reiniciado acidentalmente nesse servidor e poderá causar confusão se qualquer conexão do servidor do AGPM for mantida.</span><span class="sxs-lookup"><span data-stu-id="31aec-123">This will ensure that the AGPM Service cannot be unintentionally restarted on that server and potentially cause confusion if any AGPM Server connections to it remain.</span></span>

         

3.  <span data-ttu-id="31aec-124">Copie o arquivo do backup para o novo servidor que irá hospedar o arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="31aec-124">Copy the archive from the backup to the new server that will host the archive.</span></span> <span data-ttu-id="31aec-125">Para obter mais informações, consulte [restaurar o arquivo de um backup](restore-the-archive-from-a-backup-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="31aec-125">For more information, see [Restore the Archive from a Backup](restore-the-archive-from-a-backup-agpm40.md).</span></span>

    <span data-ttu-id="31aec-126">**Importante**  Se você moveu o arquivo sem mover o serviço do AGPM ao mesmo tempo:</span><span class="sxs-lookup"><span data-stu-id="31aec-126">**Important** If you moved the archive without moving the AGPM Service at the same time:</span></span>

    1.  <span data-ttu-id="31aec-127">Você deve alterar o caminho do arquivo morto para apontar para o novo local para o arquivo morto em relação ao servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="31aec-127">You must change the archive path to point to the new location for the archive in relation to the AGPM Server.</span></span> <span data-ttu-id="31aec-128">Para obter mais informações, consulte [Modificar o serviço do AGPM](modify-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="31aec-128">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).</span></span>

    2.  <span data-ttu-id="31aec-129">Você deve digitar novamente e confirmar a senha na guia de **delegação de domínio** . Para obter mais informações, consulte [Configurar notificação por email](configure-e-mail-notification-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="31aec-129">You must re-enter and confirm the password on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification-agpm40.md).</span></span>

     

### <span data-ttu-id="31aec-130">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="31aec-130">Additional references</span></span>

-   [<span data-ttu-id="31aec-131">Fazer backup do arquivo morto</span><span class="sxs-lookup"><span data-stu-id="31aec-131">Back Up the Archive</span></span>](back-up-the-archive-agpm40.md)

-   [<span data-ttu-id="31aec-132">Restaurar o arquivo morto de um backup</span><span class="sxs-lookup"><span data-stu-id="31aec-132">Restore the Archive from a Backup</span></span>](restore-the-archive-from-a-backup-agpm40.md)

-   [<span data-ttu-id="31aec-133">Configurar conexões de servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="31aec-133">Configure AGPM Server Connections</span></span>](configure-agpm-server-connections-agpm40.md)

-   [<span data-ttu-id="31aec-134">Modificar o serviço AGPM</span><span class="sxs-lookup"><span data-stu-id="31aec-134">Modify the AGPM Service</span></span>](modify-the-agpm-service-agpm40.md)

-   <span data-ttu-id="31aec-135">[Guia passo a passo para o gerenciamento avançado de política de grupo 4,0 da Microsoft](https://go.microsoft.com/fwlink/?LinkId=153505) (https://go.microsoft.com/fwlink/?LinkId=153505)</span><span class="sxs-lookup"><span data-stu-id="31aec-135">[Step-by-Step Guide for Microsoft Advanced Group Policy Management 4.0](https://go.microsoft.com/fwlink/?LinkId=153505) (https://go.microsoft.com/fwlink/?LinkId=153505)</span></span>

-   <span data-ttu-id="31aec-136">[Guia de planejamento para o gerenciamento avançado de política de grupo da Microsoft](https://go.microsoft.com/fwlink/?LinkId=156883) (https://go.microsoft.com/fwlink/?LinkId=156883)</span><span class="sxs-lookup"><span data-stu-id="31aec-136">[Planning Guide for Microsoft Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=156883) (https://go.microsoft.com/fwlink/?LinkId=156883)</span></span>

-   [<span data-ttu-id="31aec-137">Executar tarefas de administração de AGPM</span><span class="sxs-lookup"><span data-stu-id="31aec-137">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

 

 





