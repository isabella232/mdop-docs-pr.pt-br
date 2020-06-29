---
title: Modificar o serviço AGPM
description: Modificar o serviço AGPM
author: dansimp
ms.assetid: 3239d088-bb86-4ec4-bc56-dbe8f1c710f5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: be39b170ef4cdc14c0f447bb6bd09a4ea92c82fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797737"
---
# <span data-ttu-id="9e0d2-103">Modificar o serviço AGPM</span><span class="sxs-lookup"><span data-stu-id="9e0d2-103">Modify the AGPM Service</span></span>


<span data-ttu-id="9e0d2-104">O serviço do AGPM é um serviço do Windows que atua como um proxy de segurança, gerenciando o acesso do cliente a objetos de política de grupo (GPOs) no ambiente de arquivamento e produção do domínio.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy Objects (GPOs) in the archive and production environment of the domain.</span></span> <span data-ttu-id="9e0d2-105">Se esse serviço for interrompido ou desabilitado, os clientes do AGPM não poderão realizar operações por meio do servidor.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-105">If this service is stopped or disabled, AGPM Clients cannot perform operations through the server.</span></span> <span data-ttu-id="9e0d2-106">Você pode modificar o caminho de arquivo morto, a conta de serviço do AGPM e a porta que o serviço do AGPM escuta.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-106">You can modify the archive path, the AGPM Service Account, and the port on which the AGPM Service listens.</span></span>

<span data-ttu-id="9e0d2-107">**Cuidado**  Não modifique as configurações do serviço do AGPM por meio de ferramentas e **Serviços** **administrativos** no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-107">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="9e0d2-108">Isso pode impedir que o serviço do AGPM seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-108">Doing so can prevent the AGPM Service from starting.</span></span>

 

<span data-ttu-id="9e0d2-109">Uma conta de usuário que é membro do grupo Domain admins e tem acesso ao servidor do AGPM (o computador em que a Microsoft Advanced Group Policy Management-Server está instalado) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-109">A user account that is a member of the Domain Admins group and has access to the AGPM Server (the computer on which Microsoft Advanced Group Policy Management - Server is installed) is required to complete this procedure.</span></span> <span data-ttu-id="9e0d2-110">Além disso, você deve fornecer credenciais para a conta de serviço do AGPM para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-110">Additionally, you must provide credentials for the AGPM Service Account to complete this procedure.</span></span>

**<span data-ttu-id="9e0d2-111">Para modificar o serviço do AGPM</span><span class="sxs-lookup"><span data-stu-id="9e0d2-111">To modify the AGPM Service</span></span>**

1.  <span data-ttu-id="9e0d2-112">No computador em que o gerenciamento avançado de política de grupo da Microsoft-servidor está instalado, clique em **Iniciar**, **painel de controle**, **programas**e **programas e recursos**.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-112">On the computer on which Microsoft Advanced Group Policy Management - Server is installed, click **Start**, **Control Panel**, **Programs**, and **Programs and Features**.</span></span>

2.  <span data-ttu-id="9e0d2-113">Clique com o botão direito do mouse em **gerenciamento avançado de política de grupo da Microsoft-servidor**e clique em **alterar**.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-113">Right-click **Microsoft Advanced Group Policy Management - Server**, and then click **Change**.</span></span>

3.  <span data-ttu-id="9e0d2-114">Clique em **Avançar**e, em seguida, clique em **Modificar**.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-114">Click **Next**, and then click **Modify**.</span></span>

4.  <span data-ttu-id="9e0d2-115">Siga as instruções para configurar o serviço do AGPM:</span><span class="sxs-lookup"><span data-stu-id="9e0d2-115">Follow the instructions to configure the AGPM Service:</span></span>

    1.  <span data-ttu-id="9e0d2-116">Na caixa de diálogo **caminho do arquivo morto** , insira um novo local para o arquivo morto relativo ao servidor do AGPM ou confirme o caminho do arquivo morto atual e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-116">In the **Archive Path** dialog box, enter a new location for the archive relative to the AGPM Server, or confirm the current archive path, and then click **Next**.</span></span>

        <span data-ttu-id="9e0d2-117">**Importante**  O caminho do arquivo morto pode apontar para uma pasta no servidor do AGPM ou em outro lugar, mas o local deve ter espaço suficiente para armazenar todos os GPOs e dados de histórico gerenciados por esse servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-117">**Important** The archive path can point to a folder on the AGPM Server or elsewhere, but the location should have sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span>

         

    2.  <span data-ttu-id="9e0d2-118">Na caixa de diálogo **conta de serviço do AGPM** , insira as credenciais de uma conta de serviço sob a qual o serviço do AGPM será executado e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-118">In the **AGPM Service Account** dialog box, enter credentials for a service account under which the AGPM Service will run, and click **Next**.</span></span>

        <span data-ttu-id="9e0d2-119">**Importante**  Modificar a instalação limpa as credenciais da conta de serviço do AGPM.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-119">**Important** Modifying the installation clears the credentials for the AGPM Service Account.</span></span> <span data-ttu-id="9e0d2-120">Você deve inserir as credenciais novamente, mas elas não precisam corresponder às credenciais usadas durante a instalação original.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-120">You must re-enter credentials, but they are not required to match the credentials used during the original installation.</span></span>

        <span data-ttu-id="9e0d2-121">A conta de serviço do AGPM deve ter acesso total aos GPOs que ele gerenciará e receberá a concessão de **logon como permissão de serviço** .</span><span class="sxs-lookup"><span data-stu-id="9e0d2-121">The AGPM Service Account must have full access to the GPOs that it will manage and will be granted **Log On As A Service** permission.</span></span> <span data-ttu-id="9e0d2-122">Se você estiver gerenciando GPOs em um único domínio, poderá tornar a conta do sistema local para o controlador de domínio primário a conta do serviço do AGPM.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-122">If you will be managing GPOs on a single domain, you can make the Local System account for the primary domain controller the AGPM Service Account.</span></span>

        <span data-ttu-id="9e0d2-123">Se você estiver gerenciando GPOs em vários domínios ou se um servidor membro for o servidor do AGPM, você deve configurar uma conta diferente como a conta de serviço do AGPM porque a conta do sistema local para um controlador de domínio não pode acessar GPOs em outros domínios.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-123">If you will be managing GPOs on multiple domains or if a member server will be the AGPM Server, you should configure a different account as the AGPM Service Account because the Local System account for one domain controller cannot access GPOs on other domains.</span></span>

         

    3.  <span data-ttu-id="9e0d2-124">Na caixa de diálogo **proprietário do arquivo morto** , insira o nome de usuário de um administrador do AGPM (controle total) ou grupo de administradores do AGPM e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-124">In the **Archive Owner** dialog box, enter the user name of an AGPM Administrator (Full Control) or group of AGPM Administrators, and click **Next**.</span></span>

        <span data-ttu-id="9e0d2-125">**Observação**  Modificar a instalação limpa as credenciais do proprietário do arquivo.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-125">**Note** Modifying the installation clears the credentials for the Archive Owner.</span></span> <span data-ttu-id="9e0d2-126">Você deve inserir as credenciais novamente, mas elas não precisam corresponder às credenciais usadas durante a instalação original.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-126">You must re-enter credentials, but they are not required to match the credentials used during the original installation.</span></span>

         

    4.  <span data-ttu-id="9e0d2-127">Na caixa de diálogo **configuração de porta** , digite uma nova porta na qual o serviço do AGPM deve ouvir ou confirmar a porta selecionada no momento e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-127">In the **Port Configuration** dialog box, type a new port on which the AGPM Service should listen or confirm the port currently selected, and click **Next**.</span></span>

        <span data-ttu-id="9e0d2-128">**Observação**  Por padrão, o serviço do AGPM escuta na porta 4600.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-128">**Note** By default, the AGPM Service listens on port 4600.</span></span>

        <span data-ttu-id="9e0d2-129">Se você configurar exceções de porta manualmente ou tiver regras Configurando exceções de porta, você pode desmarcar a caixa de seleção **Adicionar exceção de porta ao firewall** .</span><span class="sxs-lookup"><span data-stu-id="9e0d2-129">If you manually configure port exceptions or have rules configuring port exceptions, you can clear the **Add port exception to firewall** check box.</span></span>

         

5.  <span data-ttu-id="9e0d2-130">Clique em **alterar**e, quando a instalação estiver concluída, clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-130">Click **Change**, and when the installation is complete click **Finish**.</span></span>

6.  <span data-ttu-id="9e0d2-131">Se você tiver alterado a porta na qual o serviço do AGPM escuta, modifique a porta na conexão do servidor do AGPM para cada administrador de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-131">If you have changed the port on which the AGPM Service listens, modify the port in the AGPM Server connection for each Group Policy administrator.</span></span> <span data-ttu-id="9e0d2-132">(Para obter mais informações, consulte [Configurar conexões do servidor de AGPM](configure-agpm-server-connections-agpm40.md).)</span><span class="sxs-lookup"><span data-stu-id="9e0d2-132">(For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).)</span></span>

7.  <span data-ttu-id="9e0d2-133">Repita para cada servidor do AGPM ao qual as alterações de configuração devem ser aplicadas.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-133">Repeat for each AGPM Server to which the configuration changes should be applied.</span></span>

### <span data-ttu-id="9e0d2-134">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="9e0d2-134">Additional references</span></span>

-   [<span data-ttu-id="9e0d2-135">Gerenciamento do serviço AGPM</span><span class="sxs-lookup"><span data-stu-id="9e0d2-135">Managing the AGPM Service</span></span>](managing-the-agpm-service-agpm40.md)

 

 





