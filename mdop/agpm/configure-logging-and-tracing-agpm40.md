---
title: Configurar log e rastreamento
description: Configurar log e rastreamento
author: dansimp
ms.assetid: 2418cb6a-7189-4080-8fe2-9c8d47dec62c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bfc56d418ae83cbc5db24246bfac057305629df7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797431"
---
# <span data-ttu-id="2d501-103">Configurar log e rastreamento</span><span class="sxs-lookup"><span data-stu-id="2d501-103">Configure Logging and Tracing</span></span>


<span data-ttu-id="2d501-104">Você pode configurar centralmente o rastreamento e o log opcionais usando modelos administrativos.</span><span class="sxs-lookup"><span data-stu-id="2d501-104">You can centrally configure optional logging and tracing using Administrative templates.</span></span> <span data-ttu-id="2d501-105">Isso pode ser útil ao diagnosticar problemas relacionados ao gerenciamento avançado de política de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="2d501-105">This may be helpful when diagnosing any problems related to Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="2d501-106">Uma conta de usuário com a função de administrador do AGPM (controle total), a conta de usuário do aprovador que criou o objeto de política de grupo (GPO) usado nesses procedimentos ou uma conta de usuário com as permissões necessárias no AGPM é necessária para concluir esses procedimentos.</span><span class="sxs-lookup"><span data-stu-id="2d501-106">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the Group Policy Object (GPO) used in these procedures, or a user account with the necessary permissions in AGPM is required to complete these procedures.</span></span> <span data-ttu-id="2d501-107">Além disso, uma conta de usuário com acesso ao servidor do AGPM é necessária para iniciar o registro em log no servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="2d501-107">Additionally, a user account with access to the AGPM Server is required to initiate logging on the AGPM Server.</span></span> <span data-ttu-id="2d501-108">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="2d501-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="2d501-109">Para configurar o registro em log e rastreamento do AGPM</span><span class="sxs-lookup"><span data-stu-id="2d501-109">To configure logging and tracing for AGPM</span></span>**

1.  <span data-ttu-id="2d501-110">Na árvore do **console de gerenciamento de política de grupo** , edite um GPO aplicado a todos os administradores de política de grupo para os quais você deseja ativar o log e o rastreamento.</span><span class="sxs-lookup"><span data-stu-id="2d501-110">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators for which you want to turn on logging and tracing.</span></span> <span data-ttu-id="2d501-111">(Para obter mais informações, consulte [editando um GPO](editing-a-gpo-agpm40.md).)</span><span class="sxs-lookup"><span data-stu-id="2d501-111">(For more information, see [Editing a GPO](editing-a-gpo-agpm40.md).)</span></span>

2.  <span data-ttu-id="2d501-112">Na janela **Editor de gerenciamento de política de grupo** , clique em **configuração do computador**, **políticas**, **modelos administrativos**, **componentes do Windows**e **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="2d501-112">In the **Group Policy Management Editor** window, click **Computer Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

3.  <span data-ttu-id="2d501-113">No painel de detalhes, clique duas vezes em **AGPM: configurar o registro em log**.</span><span class="sxs-lookup"><span data-stu-id="2d501-113">In the details pane, double-click **AGPM: Configure logging**.</span></span>

4.  <span data-ttu-id="2d501-114">Na janela **Propriedades** , clique em **habilitado**e configure o nível de detalhes a serem registrados nos logs.</span><span class="sxs-lookup"><span data-stu-id="2d501-114">In the **Properties** window, click **Enabled**, and configure the level of detail to record in the logs.</span></span>

5.  <span data-ttu-id="2d501-115">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d501-115">Click **OK**.</span></span>

6.  <span data-ttu-id="2d501-116">Feche a janela do **Editor de gerenciamento de política de grupo** .</span><span class="sxs-lookup"><span data-stu-id="2d501-116">Close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="2d501-117">(Para obter mais informações, consulte [implantar um GPO](deploy-a-gpo-agpm40.md).) Após a atualização da política de grupo, você deve reiniciar o serviço do AGPM para iniciar, modificar ou parar o registro em log no servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="2d501-117">(For more information, see [Deploy a GPO](deploy-a-gpo-agpm40.md).) After Group Policy is updated, you must restart the AGPM Service to start, modify, or stop logging on the AGPM Server.</span></span> <span data-ttu-id="2d501-118">Os administradores de política de grupo devem fechar e reiniciar o GPMC para iniciar, modificar ou interromper o registro em seus computadores.</span><span class="sxs-lookup"><span data-stu-id="2d501-118">Group Policy administrators must close and restart the GPMC to start, modify, or stop logging on their computers.</span></span>

    <span data-ttu-id="2d501-119">**Rastrear locais de arquivos**:</span><span class="sxs-lookup"><span data-stu-id="2d501-119">**Trace file locations**:</span></span>

    -   <span data-ttu-id="2d501-120">Cliente:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="2d501-120">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

    -   <span data-ttu-id="2d501-121">Servidor:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="2d501-121">Server: %ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

### <span data-ttu-id="2d501-122">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="2d501-122">Additional considerations</span></span>

-   <span data-ttu-id="2d501-123">Você deve ser capaz de editar e implantar um GPO para configurar o rastreamento e o log do AGPM.</span><span class="sxs-lookup"><span data-stu-id="2d501-123">You must be able to edit and deploy a GPO to configure AGPM logging and tracing.</span></span> <span data-ttu-id="2d501-124">Consulte [editando um GPO](editing-a-gpo-agpm40.md) e [implante um GPO](deploy-a-gpo-agpm40.md) para obter detalhes adicionais.</span><span class="sxs-lookup"><span data-stu-id="2d501-124">See [Editing a GPO](editing-a-gpo-agpm40.md) and [Deploy a GPO](deploy-a-gpo-agpm40.md) for additional detail.</span></span>

### <span data-ttu-id="2d501-125">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="2d501-125">Additional references</span></span>

-   [<span data-ttu-id="2d501-126">Configuração do Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="2d501-126">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management-agpm40.md)

 

 





