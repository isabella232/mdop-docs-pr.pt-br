---
title: Como executar tarefas de editor
description: Como executar tarefas de editor
author: dansimp
ms.assetid: 81976a01-2a95-4256-b703-9fb3c884ef34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b8e23bb91d8762d19eed9ae817967ba5a57505a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797719"
---
# <span data-ttu-id="eb3bb-103">Como executar tarefas de editor</span><span class="sxs-lookup"><span data-stu-id="eb3bb-103">Performing Editor Tasks</span></span>


<span data-ttu-id="eb3bb-104">No gerenciamento avançado de política de grupo (AGPM), um editor é uma pessoa autorizada por um administrador do AGPM (controle total) para alterar objetos de política de grupo (GPOs) e criar modelos de GPO.</span><span class="sxs-lookup"><span data-stu-id="eb3bb-104">In Advanced Group Policy Management (AGPM), an Editor is a person authorized by an AGPM Administrator (Full Control) to change Group Policy Objects (GPOs) and create GPO templates.</span></span> <span data-ttu-id="eb3bb-105">Além disso, um editor pode solicitar que um GPO seja criado, excluído ou restaurado.</span><span class="sxs-lookup"><span data-stu-id="eb3bb-105">Additionally, an Editor can request that a GPO be created, deleted, or restored.</span></span> <span data-ttu-id="eb3bb-106">Um Aprovador deve aprovar a solicitação para que ela seja implementada.</span><span class="sxs-lookup"><span data-stu-id="eb3bb-106">An Approver must approve the request for it to be implemented.</span></span> <span data-ttu-id="eb3bb-107">Um editor pode exportar um GPO para um arquivo para que ele possa ser copiado para um domínio em outra floresta e importar um GPO que foi copiado de outro domínio.</span><span class="sxs-lookup"><span data-stu-id="eb3bb-107">An Editor can export a GPO to a file so that it can be copied to a domain in another forest, and import a GPO that was copied from another domain.</span></span>

<span data-ttu-id="eb3bb-108">**Importante**  Certifique-se de que você esteja se conectando ao arquivo central para GPOs.</span><span class="sxs-lookup"><span data-stu-id="eb3bb-108">**Important** Make sure that you are connecting to the central archive for GPOs.</span></span> <span data-ttu-id="eb3bb-109">Para obter mais informações, consulte [Configurar uma conexão com o servidor do AGPM](configure-an-agpm-server-connection-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="eb3bb-109">For more information, see [Configure an AGPM Server Connection](configure-an-agpm-server-connection-agpm40.md).</span></span>

 

-   [<span data-ttu-id="eb3bb-110">Criar ou controlar um GPO</span><span class="sxs-lookup"><span data-stu-id="eb3bb-110">Creating or Controlling a GPO</span></span>](creating-or-controlling-a-gpo-agpm40-ed.md)

-   [<span data-ttu-id="eb3bb-111">Editando um GPO</span><span class="sxs-lookup"><span data-stu-id="eb3bb-111">Editing a GPO</span></span>](editing-a-gpo-agpm40.md)

-   [<span data-ttu-id="eb3bb-112">Como usar um ambiente de teste</span><span class="sxs-lookup"><span data-stu-id="eb3bb-112">Using a Test Environment</span></span>](using-a-test-environment.md)

-   [<span data-ttu-id="eb3bb-113">Solicitar a implantação de um GPO</span><span class="sxs-lookup"><span data-stu-id="eb3bb-113">Request Deployment of a GPO</span></span>](request-deployment-of-a-gpo-agpm40.md)

-   [<span data-ttu-id="eb3bb-114">Criação de um modelo e ajuste de um modelo padrão</span><span class="sxs-lookup"><span data-stu-id="eb3bb-114">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template-agpm40.md)

-   [<span data-ttu-id="eb3bb-115">Excluir ou restaurar um GPO</span><span class="sxs-lookup"><span data-stu-id="eb3bb-115">Deleting or Restoring a GPO</span></span>](deleting-or-restoring-a-gpo-agpm40.md)

<span data-ttu-id="eb3bb-116">**Observação**  Como a função editor inclui as permissões para a função de revisor, um editor também pode revisar as configurações e comparar os GPOs.</span><span class="sxs-lookup"><span data-stu-id="eb3bb-116">**Note** Because the Editor role includes the permissions for the Reviewer role, an Editor can also review settings and compare GPOs.</span></span> <span data-ttu-id="eb3bb-117">Confira [executar tarefas do revisor](performing-reviewer-tasks-agpm40.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="eb3bb-117">See [Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md) for more information.</span></span>

 

### <span data-ttu-id="eb3bb-118">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="eb3bb-118">Additional considerations</span></span>

<span data-ttu-id="eb3bb-119">Por padrão, as seguintes permissões são fornecidas para a função de editor:</span><span class="sxs-lookup"><span data-stu-id="eb3bb-119">By default, the following permissions are provided for the Editor role:</span></span>

-   <span data-ttu-id="eb3bb-120">Conteúdo da lista</span><span class="sxs-lookup"><span data-stu-id="eb3bb-120">List Contents</span></span>

-   <span data-ttu-id="eb3bb-121">Ler configurações</span><span class="sxs-lookup"><span data-stu-id="eb3bb-121">Read Settings</span></span>

-   <span data-ttu-id="eb3bb-122">Editar configurações</span><span class="sxs-lookup"><span data-stu-id="eb3bb-122">Edit Settings</span></span>

-   <span data-ttu-id="eb3bb-123">GPO de exportação</span><span class="sxs-lookup"><span data-stu-id="eb3bb-123">Export GPO</span></span>

-   <span data-ttu-id="eb3bb-124">Importar GPO</span><span class="sxs-lookup"><span data-stu-id="eb3bb-124">Import GPO</span></span>

-   <span data-ttu-id="eb3bb-125">Criar modelo</span><span class="sxs-lookup"><span data-stu-id="eb3bb-125">Create Template</span></span>

 

 





