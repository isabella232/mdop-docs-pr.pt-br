---
title: Configurar log e rastreamento
description: Configurar log e rastreamento
author: dansimp
ms.assetid: 419231f9-e9db-4f91-a7cf-a0a73db25256
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa3dfa71edb25f6641ade595cd4469e846410ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797432"
---
# <span data-ttu-id="c0e97-103">Configurar log e rastreamento</span><span class="sxs-lookup"><span data-stu-id="c0e97-103">Configure Logging and Tracing</span></span>


<span data-ttu-id="c0e97-104">Você pode configurar centralmente o log e o rastreamento opcionais para gerenciamento avançado de política de grupo (AGPM) usando modelos administrativos.</span><span class="sxs-lookup"><span data-stu-id="c0e97-104">You can centrally configure optional logging and tracing for Advanced Group Policy Management (AGPM) using Administrative templates.</span></span>

<span data-ttu-id="c0e97-105">Uma conta de usuário com a função de administrador do AGPM (controle total), a conta de usuário do aprovador que criou o GPO usado nesses procedimentos ou uma conta de usuário com as permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir esses procedimentos.</span><span class="sxs-lookup"><span data-stu-id="c0e97-105">A user account with the AGPM Administrator (Full Control) role, the user account of the Approver who created the GPO used in these procedures, or a user account with the necessary permissions in Advanced Group Policy Management is required to complete these procedures.</span></span> <span data-ttu-id="c0e97-106">Além disso, uma conta de usuário com acesso ao servidor do AGPM é necessária para iniciar o registro em log no servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="c0e97-106">Additionally, a user account with access to the AGPM Server is required to initiate logging on the AGPM Server.</span></span> <span data-ttu-id="c0e97-107">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="c0e97-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="c0e97-108">Para configurar o registro em log e rastreamento do AGPM</span><span class="sxs-lookup"><span data-stu-id="c0e97-108">To configure logging and tracing for AGPM</span></span>**

1.  <span data-ttu-id="c0e97-109">Na árvore do **console de gerenciamento de política de grupo** , edite um GPO aplicado a todos os administradores de política de grupo para os quais você deseja ativar o log e o rastreamento.</span><span class="sxs-lookup"><span data-stu-id="c0e97-109">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators for which you want to turn on logging and tracing.</span></span> <span data-ttu-id="c0e97-110">(Para obter mais informações, consulte [editando um GPO](editing-a-gpo.md).)</span><span class="sxs-lookup"><span data-stu-id="c0e97-110">(For more information, see [Editing a GPO](editing-a-gpo.md).)</span></span>

2.  <span data-ttu-id="c0e97-111">No **Editor de objeto de política de grupo**, clique em configuração do **computador**, **modelos administrativos**e **componentes do Windows**.</span><span class="sxs-lookup"><span data-stu-id="c0e97-111">In the **Group Policy Object Editor**, click **Computer Configuration**, **Administrative Templates**, and **Windows Components**.</span></span>

3.  <span data-ttu-id="c0e97-112">Se o **AGPM** não estiver listado em **componentes do Windows**:</span><span class="sxs-lookup"><span data-stu-id="c0e97-112">If **AGPM** is not listed under **Windows Components**:</span></span>

    1.  <span data-ttu-id="c0e97-113">Clique com o botão direito do mouse em **modelos administrativos** e clique em **Adicionar/remover modelos**.</span><span class="sxs-lookup"><span data-stu-id="c0e97-113">Right-click **Administrative Templates** and click **Add/Remove Templates**.</span></span>

    2.  <span data-ttu-id="c0e97-114">Clique **em Adicionar**, selecione **AGPM. admx** ou **AGPM. adm**, clique em **abrir**e, em seguida, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="c0e97-114">Click **Add**, select **agpm.admx** or **agpm.adm**, click **Open**, and then click **Close**.</span></span>

4.  <span data-ttu-id="c0e97-115">Em **componentes do Windows**, clique duas vezes em **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="c0e97-115">Under **Windows Components**, double-click **AGPM**.</span></span>

5.  <span data-ttu-id="c0e97-116">No painel de detalhes, clique duas vezes em **log do AGPM**.</span><span class="sxs-lookup"><span data-stu-id="c0e97-116">In the details pane, double-click **AGPM Logging**.</span></span>

6.  <span data-ttu-id="c0e97-117">Na janela **Propriedades de log do AGPM** , clique em **habilitado**e configure o nível de detalhes a serem registrados nos logs.</span><span class="sxs-lookup"><span data-stu-id="c0e97-117">In the **AGPM Logging Properties** window, click **Enabled**, and configure the level of detail to record in the logs.</span></span>

7.  <span data-ttu-id="c0e97-118">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="c0e97-118">Click **OK**.</span></span>

8.  <span data-ttu-id="c0e97-119">Feche o **Editor de objeto de política de grupo**.</span><span class="sxs-lookup"><span data-stu-id="c0e97-119">Close the **Group Policy Object Editor**.</span></span> <span data-ttu-id="c0e97-120">(Para obter mais informações, consulte [implantar um GPO](deploy-a-gpo.md).) Após a atualização da política de grupo, você deve reiniciar o serviço do AGPM para começar a fazer logon no servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="c0e97-120">(For more information, see [Deploy a GPO](deploy-a-gpo.md).) After Group Policy is updated, you must restart the AGPM Service to begin logging on the AGPM Server.</span></span> <span data-ttu-id="c0e97-121">Os administradores de política de grupo devem fechar e reiniciar o GPMC para começar a fazer logon em seus computadores.</span><span class="sxs-lookup"><span data-stu-id="c0e97-121">Group Policy administrators must close and restart the GPMC to begin logging on their computers.</span></span>

    <span data-ttu-id="c0e97-122">**Rastrear locais de arquivos**:</span><span class="sxs-lookup"><span data-stu-id="c0e97-122">**Trace file locations**:</span></span>

    -   <span data-ttu-id="c0e97-123">Cliente:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="c0e97-123">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

    -   <span data-ttu-id="c0e97-124">Servidor:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="c0e97-124">Server: %ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

### <span data-ttu-id="c0e97-125">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="c0e97-125">Additional considerations</span></span>

-   <span data-ttu-id="c0e97-126">Você deve ser capaz de editar e implantar um GPO para configurar o rastreamento e o log do AGPM.</span><span class="sxs-lookup"><span data-stu-id="c0e97-126">You must be able to edit and deploy a GPO to configure AGPM logging and tracing.</span></span> <span data-ttu-id="c0e97-127">Consulte [editando um GPO](editing-a-gpo.md) e [implante um GPO](deploy-a-gpo.md) para obter detalhes adicionais.</span><span class="sxs-lookup"><span data-stu-id="c0e97-127">See [Editing a GPO](editing-a-gpo.md) and [Deploy a GPO](deploy-a-gpo.md) for additional detail.</span></span>

### <span data-ttu-id="c0e97-128">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="c0e97-128">Additional references</span></span>

-   [<span data-ttu-id="c0e97-129">Executar tarefas de administração de AGPM</span><span class="sxs-lookup"><span data-stu-id="c0e97-129">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





