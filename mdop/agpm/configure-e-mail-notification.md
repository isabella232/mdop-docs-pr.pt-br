---
title: Configurar notificações por email
description: Configurar notificações por email
author: dansimp
ms.assetid: 6e152de0-4376-4963-8d1a-3e7f5866d30f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 46e8d00c2446a0185de30bbd1f39a7e3eaf90080
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797433"
---
# <span data-ttu-id="33d5a-103">Configurar notificações por email</span><span class="sxs-lookup"><span data-stu-id="33d5a-103">Configure E-Mail Notification</span></span>


<span data-ttu-id="33d5a-104">Quando um editor ou um revisor tenta criar, implantar ou excluir um objeto de política de grupo (GPO), uma solicitação para esta ação é enviada a um endereço de email ou a endereços designados para que um Aprovador possa avaliar a solicitação e implementá-la ou Deny-la.</span><span class="sxs-lookup"><span data-stu-id="33d5a-104">When an Editor or a Reviewer attempts to create, deploy, or delete a Group Policy object (GPO), a request for this action is sent to a designated e-mail address or addresses so that an Approver can evaluate the request and implement or deny it.</span></span> <span data-ttu-id="33d5a-105">Você determina o endereço de email ou endereços para os quais as notificações são enviadas, bem como o alias do qual as notificações são enviadas.</span><span class="sxs-lookup"><span data-stu-id="33d5a-105">You determine the e-mail address or addresses to which notifications are sent, as well as the alias from which notifications are sent.</span></span>

<span data-ttu-id="33d5a-106">Uma conta de usuário com a função de administrador do AGPM (controle total) ou permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="33d5a-106">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="33d5a-107">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="33d5a-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="33d5a-108">Para configurar a notificação por email para o AGPM</span><span class="sxs-lookup"><span data-stu-id="33d5a-108">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="33d5a-109">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="33d5a-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="33d5a-110">No painel de detalhes, clique na guia de **delegação de domínio** .</span><span class="sxs-lookup"><span data-stu-id="33d5a-110">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="33d5a-111">No campo **de** , digite o alias de email do AGPM do qual as notificações devem ser enviadas.</span><span class="sxs-lookup"><span data-stu-id="33d5a-111">In the **From** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="33d5a-112">No campo **para** , digite uma lista delimitada por vírgulas de endereços de email de aprovadores que devem receber solicitações de aprovação.</span><span class="sxs-lookup"><span data-stu-id="33d5a-112">In the **To** field, type a comma-delimited list of e-mail addresses of Approvers who should receive requests for approval.</span></span>

5.  <span data-ttu-id="33d5a-113">No campo **servidor SMTP** , digite um servidor de email SMTP válido.</span><span class="sxs-lookup"><span data-stu-id="33d5a-113">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="33d5a-114">Nos campos **nome de usuário** e **senha** , digite as credenciais de um usuário com acesso ao serviço SMTP.</span><span class="sxs-lookup"><span data-stu-id="33d5a-114">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span>

7.  <span data-ttu-id="33d5a-115">Clique em **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="33d5a-115">Click **Apply**.</span></span>

### <span data-ttu-id="33d5a-116">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="33d5a-116">Additional considerations</span></span>

-   <span data-ttu-id="33d5a-117">Por padrão, você deve ser um administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="33d5a-117">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="33d5a-118">Especificamente, você deve ter permissões de **lista de conteúdo** e **Opções de modificação** para o domínio.</span><span class="sxs-lookup"><span data-stu-id="33d5a-118">Specifically, you must have **List Contents** and **Modify Options** permissions for the domain.</span></span>

-   <span data-ttu-id="33d5a-119">A notificação por email para o AGPM é uma configuração no nível do domínio.</span><span class="sxs-lookup"><span data-stu-id="33d5a-119">E-mail notification for AGPM is a domain-level setting.</span></span> <span data-ttu-id="33d5a-120">Você pode fornecer diferentes endereços de email do aprovador ou aliases de email do AGPM na guia de **delegação de domínio** de cada domínio ou usar os mesmos endereços de email em todo o ambiente.</span><span class="sxs-lookup"><span data-stu-id="33d5a-120">You can provide different Approver e-mail addresses or AGPM e-mail aliases on each domain's **Domain Delegation** tab, or use the same e-mail addresses throughout your environment.</span></span>

### <span data-ttu-id="33d5a-121">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="33d5a-121">Additional references</span></span>

-   [<span data-ttu-id="33d5a-122">Executar tarefas de administração de AGPM</span><span class="sxs-lookup"><span data-stu-id="33d5a-122">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





