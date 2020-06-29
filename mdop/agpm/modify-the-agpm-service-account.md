---
title: Modificar a conta de serviço do AGPM
description: Modificar a conta de serviço do AGPM
author: dansimp
ms.assetid: 0d8d8c7b-f299-4fee-8414-406492156942
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0672ceed2fba17060e17d2ffcfa264da458b9897
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797742"
---
# <span data-ttu-id="8cbdc-103">Modificar a conta de serviço do AGPM</span><span class="sxs-lookup"><span data-stu-id="8cbdc-103">Modify the AGPM Service Account</span></span>


<span data-ttu-id="8cbdc-104">O serviço do AGPM é um serviço do Windows que atua como um proxy de segurança, gerenciando o acesso do cliente a objetos de política de grupo (GPOs) no ambiente de arquivamento e produção.</span><span class="sxs-lookup"><span data-stu-id="8cbdc-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy objects (GPOs) in the archive and production environment.</span></span> <span data-ttu-id="8cbdc-105">Se esse serviço for interrompido ou desabilitado, os clientes do AGPM não poderão realizar operações por meio do servidor.</span><span class="sxs-lookup"><span data-stu-id="8cbdc-105">If this service is stopped or disabled, AGPM clients cannot perform operations through the server.</span></span>

<span data-ttu-id="8cbdc-106">O caminho de arquivo morto e a conta do serviço do AGPM são configurados durante a instalação do servidor do AGPM e podem ser alterados posteriormente por meio de **Adicionar ou remover programas** no servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="8cbdc-106">The archive path and AGPM Service Account are configured during the installation of AGPM Server and can be changed afterward through **Add or Remove Programs** on the AGPM Server.</span></span>

<span data-ttu-id="8cbdc-107">**Cuidado**  Não modifique as configurações do serviço do AGPM por meio de ferramentas e **Serviços** **administrativos** no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8cbdc-107">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="8cbdc-108">Isso pode impedir que o serviço do AGPM seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="8cbdc-108">Doing so can prevent the AGPM Service from starting.</span></span>

 

<span data-ttu-id="8cbdc-109">Uma conta de usuário que é membro do grupo Domain admins e tem acesso ao servidor do AGPM (o computador em que a Microsoft Advanced Group Policy Management-Server está instalado) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="8cbdc-109">A user account that is a member of the Domain Admins group and has access to the AGPM Server (the computer on which Microsoft Advanced Group Policy Management - Server is installed) is required to complete this procedure.</span></span>

<span data-ttu-id="8cbdc-110">**Importante**  A conta de serviço do AGPM deve ter acesso total aos GPOs que ele gerenciará e receberá a concessão de **logon como permissão de serviço** .</span><span class="sxs-lookup"><span data-stu-id="8cbdc-110">**Important** The AGPM Service Account must have full access to the GPOs that it will manage and will be granted **Log On As A Service** permission.</span></span> <span data-ttu-id="8cbdc-111">Se você estiver gerenciando GPOs em um único domínio, poderá tornar a conta do sistema local para o controlador de domínio primário a conta do serviço do AGPM.</span><span class="sxs-lookup"><span data-stu-id="8cbdc-111">If you will be managing GPOs on a single domain, you can make the Local System account for the primary domain controller the AGPM Service Account.</span></span>

<span data-ttu-id="8cbdc-112">Se você estiver gerenciando GPOs em vários domínios ou se um servidor membro for o servidor do AGPM, você deve configurar uma conta diferente como a conta de serviço do AGPM porque a conta do sistema local para um controlador de domínio não pode acessar GPOs em outros domínios.</span><span class="sxs-lookup"><span data-stu-id="8cbdc-112">If you will be managing GPOs on multiple domains or if a member server will be the AGPM Server, you should configure a different account as the AGPM Service Account because the Local System account for one domain controller cannot access GPOs on other domains.</span></span>

 

**<span data-ttu-id="8cbdc-113">Para modificar a conta de serviço do AGPM</span><span class="sxs-lookup"><span data-stu-id="8cbdc-113">To modify the AGPM Service Account</span></span>**

1.  <span data-ttu-id="8cbdc-114">No computador em que o gerenciamento avançado de política de grupo da Microsoft-servidor está instalado, clique em **Iniciar**, **painel de controle**, clique em **Adicionar ou remover programas**.</span><span class="sxs-lookup"><span data-stu-id="8cbdc-114">On the computer on which Microsoft Advanced Group Policy Management - Server is installed, click **Start**, click **Control Panel**, click **Add or Remove Programs**.</span></span>

2.  <span data-ttu-id="8cbdc-115">Clique em **gerenciamento avançado de política de grupo da Microsoft-servidor**e, em seguida, clique em **alterar**.</span><span class="sxs-lookup"><span data-stu-id="8cbdc-115">Click **Microsoft Advanced Group Policy Management - Server**, and then click **Change**.</span></span>

3.  <span data-ttu-id="8cbdc-116">Clique em **Avançar**e, em seguida, clique em **Modificar**.</span><span class="sxs-lookup"><span data-stu-id="8cbdc-116">Click **Next**, and then click **Modify**.</span></span>

4.  <span data-ttu-id="8cbdc-117">Siga as instruções na tela para definir as configurações do serviço do AGPM:</span><span class="sxs-lookup"><span data-stu-id="8cbdc-117">Follow the instructions on screen to configure settings for the AGPM Service:</span></span>

    1.  <span data-ttu-id="8cbdc-118">Para o caminho do arquivo morto, confirme ou altere a localização do arquivo relativo ao servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="8cbdc-118">For the archive path, confirm or change the location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="8cbdc-119">O caminho do arquivo morto pode apontar para uma pasta no servidor do AGPM ou em outro lugar, mas o local deve ter espaço suficiente para armazenar todos os GPOs e dados de histórico gerenciados por esse servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="8cbdc-119">The archive path can point to a folder on the AGPM Server or elsewhere, but the location should have sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span>

    2.  <span data-ttu-id="8cbdc-120">Insira novas credenciais para a conta de serviço do AGPM.</span><span class="sxs-lookup"><span data-stu-id="8cbdc-120">Enter new credentials for the AGPM Service Account.</span></span>

    3.  <span data-ttu-id="8cbdc-121">Para o proprietário do arquivo morto, insira as credenciais de um administrador do AGPM (controle total).</span><span class="sxs-lookup"><span data-stu-id="8cbdc-121">For the archive owner, enter the credentials of an AGPM Administrator (Full Control).</span></span>

5.  <span data-ttu-id="8cbdc-122">Clique em **alterar**e, quando a instalação estiver concluída, clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="8cbdc-122">Click **Change**, and when the installation is complete click **Finish**.</span></span>

### <span data-ttu-id="8cbdc-123">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="8cbdc-123">Additional references</span></span>

-   [<span data-ttu-id="8cbdc-124">Gerenciamento do serviço AGPM</span><span class="sxs-lookup"><span data-stu-id="8cbdc-124">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 





