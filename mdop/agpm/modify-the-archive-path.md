---
title: Modificar o caminho do arquivo morto
description: Modificar o caminho do arquivo morto
author: dansimp
ms.assetid: 6d90daf9-58db-4166-b5b3-e84bb261164a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1fc6ba2bf415d3d1bc67144d0dec1030c6173026
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797736"
---
# <span data-ttu-id="dab83-103">Modificar o caminho do arquivo morto</span><span class="sxs-lookup"><span data-stu-id="dab83-103">Modify the Archive Path</span></span>


<span data-ttu-id="dab83-104">O caminho do arquivo morto é o local do arquivo morto relativo ao servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="dab83-104">The archive path is the location of the archive relative to the AGPM Server.</span></span> <span data-ttu-id="dab83-105">O caminho de arquivo morto pode apontar para uma pasta no servidor do AGPM ou em outro servidor na mesma floresta.</span><span class="sxs-lookup"><span data-stu-id="dab83-105">The archive path can point to a folder on the AGPM Server or on another server in the same forest.</span></span>

<span data-ttu-id="dab83-106">O caminho de arquivo morto e a conta do serviço do AGPM são configurados durante a instalação do servidor do AGPM e podem ser alterados posteriormente por meio de **Adicionar ou remover programas** no servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="dab83-106">The archive path and AGPM Service Account are configured during the installation of AGPM Server and can be changed afterward through **Add or Remove Programs** on the AGPM Server.</span></span>

<span data-ttu-id="dab83-107">Uma conta de usuário que é membro do grupo Domain admins e tem acesso ao servidor do AGPM (o computador em que a Microsoft Advanced Group Policy Management-Server está instalado) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="dab83-107">A user account that is a member of the Domain Admins group and has access to the AGPM Server (the computer on which Microsoft Advanced Group Policy Management - Server is installed) is required to complete this procedure.</span></span>

**<span data-ttu-id="dab83-108">Para modificar o caminho do arquivo morto</span><span class="sxs-lookup"><span data-stu-id="dab83-108">To modify the archive path</span></span>**

1.  <span data-ttu-id="dab83-109">No computador em que o gerenciamento avançado de política de grupo da Microsoft-servidor está instalado, clique em **Iniciar**, **painel de controle**, clique em **Adicionar ou remover programas**.</span><span class="sxs-lookup"><span data-stu-id="dab83-109">On the computer on which Microsoft Advanced Group Policy Management - Server is installed, click **Start**, click **Control Panel**, click **Add or Remove Programs**.</span></span>

2.  <span data-ttu-id="dab83-110">Clique em **gerenciamento avançado de política de grupo da Microsoft-servidor**e, em seguida, clique em **alterar**.</span><span class="sxs-lookup"><span data-stu-id="dab83-110">Click **Microsoft Advanced Group Policy Management - Server**, and then click **Change**.</span></span>

3.  <span data-ttu-id="dab83-111">Clique em **Avançar**e, em seguida, clique em **Modificar**.</span><span class="sxs-lookup"><span data-stu-id="dab83-111">Click **Next**, and then click **Modify**.</span></span>

4.  <span data-ttu-id="dab83-112">Siga as instruções na tela para definir as configurações do serviço do AGPM:</span><span class="sxs-lookup"><span data-stu-id="dab83-112">Follow the instructions on screen to configure settings for the AGPM Service:</span></span>

    1.  <span data-ttu-id="dab83-113">Para o caminho do arquivo morto, insira um novo local para o arquivo morto relativo ao servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="dab83-113">For the archive path, enter a new location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="dab83-114">O caminho do arquivo morto pode apontar para uma pasta no servidor do AGPM ou em outro lugar, mas o local deve ter espaço suficiente para armazenar todos os GPOs e dados de histórico gerenciados por esse servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="dab83-114">The archive path can point to a folder on the AGPM Server or elsewhere, but the location should have sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span>

    2.  <span data-ttu-id="dab83-115">Insira as credenciais para a conta de serviço do AGPM.</span><span class="sxs-lookup"><span data-stu-id="dab83-115">Enter credentials for the AGPM Service Account.</span></span>

        <span data-ttu-id="dab83-116">**Importante**  Modificar a instalação limpa as credenciais da conta de serviço do AGPM.</span><span class="sxs-lookup"><span data-stu-id="dab83-116">**Important** Modifying the installation clears the credentials for the AGPM Service Account.</span></span> <span data-ttu-id="dab83-117">Você deve inserir as credenciais novamente, mas elas não precisam corresponder às credenciais usadas durante a instalação original.</span><span class="sxs-lookup"><span data-stu-id="dab83-117">You must re-enter credentials, but they are not required to match the credentials used during the original installation.</span></span>

        <span data-ttu-id="dab83-118">A conta de serviço do AGPM deve ter acesso total aos GPOs que ele gerenciará.</span><span class="sxs-lookup"><span data-stu-id="dab83-118">The AGPM Service Account must have full access to the GPOs that it will manage.</span></span> <span data-ttu-id="dab83-119">Se você estiver gerenciando GPOs em um único domínio, poderá tornar a conta do sistema local para o controlador de domínio primário a conta do serviço do AGPM.</span><span class="sxs-lookup"><span data-stu-id="dab83-119">If you will be managing GPOs on a single domain, you can make the Local System account for the primary domain controller the AGPM Service Account.</span></span>

        <span data-ttu-id="dab83-120">Se você estiver gerenciando GPOs em vários domínios ou se um servidor membro for o servidor do AGPM, você deve configurar uma conta diferente como a conta de serviço do AGPM porque a conta do sistema local para um controlador de domínio não pode acessar GPOs em outros domínios.</span><span class="sxs-lookup"><span data-stu-id="dab83-120">If you will be managing GPOs on multiple domains or if a member server will be the AGPM Server, you should configure a different account as the AGPM Service Account because the Local System account for one domain controller cannot access GPOs on other domains.</span></span>

         

    3.  <span data-ttu-id="dab83-121">Para o proprietário do arquivo morto, insira as credenciais de um administrador do AGPM (controle total).</span><span class="sxs-lookup"><span data-stu-id="dab83-121">For the archive owner, enter the credentials of an AGPM Administrator (Full Control).</span></span>

5.  <span data-ttu-id="dab83-122">Clique em **alterar**e, quando a instalação estiver concluída, clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="dab83-122">Click **Change**, and when the installation is complete click **Finish**.</span></span>

### <span data-ttu-id="dab83-123">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="dab83-123">Additional references</span></span>

-   [<span data-ttu-id="dab83-124">Gerenciamento do serviço AGPM</span><span class="sxs-lookup"><span data-stu-id="dab83-124">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 





