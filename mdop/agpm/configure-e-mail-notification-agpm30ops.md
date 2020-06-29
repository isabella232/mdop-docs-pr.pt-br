---
title: Configurar notificações por email
description: Configurar notificações por email
author: dansimp
ms.assetid: b32ce395-d1b9-4c5b-b765-97cdbf455f9e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0204f2bd3430fa47b785d13a73b107e311990b82
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797438"
---
# <span data-ttu-id="3fb84-103">Configurar notificações por email</span><span class="sxs-lookup"><span data-stu-id="3fb84-103">Configure E-Mail Notification</span></span>


<span data-ttu-id="3fb84-104">Quando um editor ou um revisor tenta criar, implantar ou excluir um objeto de política de grupo (GPO), uma solicitação para esta ação é enviada a um endereço de email ou a endereços designados para que um Aprovador possa avaliar a solicitação e implementá-la ou Deny-la.</span><span class="sxs-lookup"><span data-stu-id="3fb84-104">When an Editor or a Reviewer attempts to create, deploy, or delete a Group Policy Object (GPO), a request for this action is sent to a designated e-mail address or addresses so that an Approver can evaluate the request and implement or deny it.</span></span> <span data-ttu-id="3fb84-105">Você determina o endereço de email ou endereços para os quais as notificações são enviadas, bem como o alias do qual as notificações são enviadas.</span><span class="sxs-lookup"><span data-stu-id="3fb84-105">You determine the e-mail address or addresses to which notifications are sent, as well as the alias from which notifications are sent.</span></span>

<span data-ttu-id="3fb84-106">Uma conta de usuário com a função de administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="3fb84-106">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="3fb84-107">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="3fb84-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="3fb84-108">Para configurar a notificação por email para o AGPM</span><span class="sxs-lookup"><span data-stu-id="3fb84-108">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="3fb84-109">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="3fb84-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="3fb84-110">No painel de detalhes, clique na guia de **delegação de domínio** .</span><span class="sxs-lookup"><span data-stu-id="3fb84-110">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="3fb84-111">No campo **do endereço de email** , digite o alias de email do AGPM do qual as notificações devem ser enviadas.</span><span class="sxs-lookup"><span data-stu-id="3fb84-111">In the **From e-mail address** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="3fb84-112">No campo **endereço de email para** , digite uma lista delimitada por vírgulas de endereços de email de aprovadores que devem receber solicitações de aprovação.</span><span class="sxs-lookup"><span data-stu-id="3fb84-112">In the **To e-mail address** field, type a comma-delimited list of e-mail addresses of Approvers who should receive requests for approval.</span></span>

5.  <span data-ttu-id="3fb84-113">No campo **servidor SMTP** , digite um servidor de email SMTP válido.</span><span class="sxs-lookup"><span data-stu-id="3fb84-113">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="3fb84-114">Nos campos **nome de usuário** e **senha** , digite as credenciais de um usuário com acesso ao serviço SMTP.</span><span class="sxs-lookup"><span data-stu-id="3fb84-114">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span>

7.  <span data-ttu-id="3fb84-115">Clique em **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="3fb84-115">Click **Apply**.</span></span>

### <span data-ttu-id="3fb84-116">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="3fb84-116">Additional considerations</span></span>

-   <span data-ttu-id="3fb84-117">Por padrão, você deve ser um administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="3fb84-117">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="3fb84-118">Especificamente, você deve ter permissões de **lista de conteúdo** e **Opções de modificação** para o domínio.</span><span class="sxs-lookup"><span data-stu-id="3fb84-118">Specifically, you must have **List Contents** and **Modify Options** permissions for the domain.</span></span>

-   <span data-ttu-id="3fb84-119">A notificação por email para o AGPM é uma configuração no nível do domínio.</span><span class="sxs-lookup"><span data-stu-id="3fb84-119">E-mail notification for AGPM is a domain-level setting.</span></span> <span data-ttu-id="3fb84-120">Você pode fornecer diferentes endereços de email do aprovador ou aliases de email do AGPM na guia de **delegação de domínio** de cada domínio ou usar os mesmos endereços de email em todo o ambiente.</span><span class="sxs-lookup"><span data-stu-id="3fb84-120">You can provide different Approver e-mail addresses or AGPM e-mail aliases on each domain's **Domain Delegation** tab, or use the same e-mail addresses throughout your environment.</span></span>

-   <span data-ttu-id="3fb84-121">Por padrão, as mensagens de email enviadas como resultado de ações no gerenciamento avançado de política de grupo (AGPM) não são criptografadas.</span><span class="sxs-lookup"><span data-stu-id="3fb84-121">By default, e-mail messages sent as a result of actions in Advanced Group Policy Management (AGPM) are not encrypted.</span></span> <span data-ttu-id="3fb84-122">No entanto, você pode configurar a segurança de email para o AGPM usando configurações do registro para especificar se deseja usar a criptografia SSL (Secure Sockets Layer) e qual porta SMTP usar.</span><span class="sxs-lookup"><span data-stu-id="3fb84-122">However, you can configure e-mail security for AGPM using registry settings to specify whether to use Secure Sockets Layer (SSL) encryption and which SMTP port to use.</span></span> <span data-ttu-id="3fb84-123">Para obter mais informações, consulte [Configurar a segurança de email para o AGPM](configure-e-mail-security-for-agpm-agpm30ops.md)</span><span class="sxs-lookup"><span data-stu-id="3fb84-123">For more information, see [Configure E-Mail Security for AGPM](configure-e-mail-security-for-agpm-agpm30ops.md)</span></span>

### <span data-ttu-id="3fb84-124">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="3fb84-124">Additional references</span></span>

-   [<span data-ttu-id="3fb84-125">Configuração do Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="3fb84-125">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management.md)

 

 





