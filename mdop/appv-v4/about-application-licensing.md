---
title: Sobre licenciamento de aplicativos
description: Sobre licenciamento de aplicativos
author: dansimp
ms.assetid: 6b487641-1627-4e91-b829-04f001008176
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546bc630b95fe52f960c7bdfb771d3e2561f9318
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797657"
---
# <span data-ttu-id="4f740-103">Sobre licenciamento de aplicativos</span><span class="sxs-lookup"><span data-stu-id="4f740-103">About Application Licensing</span></span>


<span data-ttu-id="4f740-104">Você pode gerenciar licenças de aplicativos diretamente do console de gerenciamento do servidor do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="4f740-104">You can manage application licenses directly from the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="4f740-105">Tipos de licença</span><span class="sxs-lookup"><span data-stu-id="4f740-105">License Types</span></span>


<span data-ttu-id="4f740-106">No momento, o sistema do System Center Application Virtualization oferece suporte aos seguintes tipos de licença:</span><span class="sxs-lookup"><span data-stu-id="4f740-106">The System Center Application Virtualization System currently supports the following license types:</span></span>

-   <span data-ttu-id="4f740-107">**Licença ilimitada**— permite o acesso ao aplicativo por qualquer número de usuários simultâneos.</span><span class="sxs-lookup"><span data-stu-id="4f740-107">**Unlimited License**—Allows access to the application by any number of simultaneous users.</span></span> <span data-ttu-id="4f740-108">Esse método de licenciamento é apropriado quando você deseja associar uma licença de toda a empresa a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4f740-108">This method of licensing is appropriate when you want to associate an enterprise-wide license with an application.</span></span>

-   <span data-ttu-id="4f740-109">**Licença simultânea**— permite que você defina o número máximo de usuários simultâneos que têm permissão para usar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4f740-109">**Concurrent License**—Enables you to define the maximum number of concurrent users who are allowed to use the application.</span></span>

-   <span data-ttu-id="4f740-110">**Licença nomeada**— permite atribuir uma licença a um usuário individual.</span><span class="sxs-lookup"><span data-stu-id="4f740-110">**Named License**—Enables you to assign a license to an individual user.</span></span> <span data-ttu-id="4f740-111">Uma licença nomeada pode ser usada para garantir que um usuário em particular sempre será capaz de executar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4f740-111">A named license can be used to ensure that a particular user will always be able to run the application.</span></span>

<span data-ttu-id="4f740-112">Você pode combinar licenças simultâneas e nomeadas para o mesmo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4f740-112">You can combine concurrent and named licenses for the same application.</span></span>

<span data-ttu-id="4f740-113">O licenciamento está desabilitado por padrão, mas você pode habilitá-lo na guia **pipeline do provedor** da caixa de diálogo **Propriedades do provedor** .</span><span class="sxs-lookup"><span data-stu-id="4f740-113">Licensing is disabled by default, but you can enable it from the **Provider Pipeline** tab of the **Provider Properties** dialog.</span></span> <span data-ttu-id="4f740-114">Para obter detalhes sobre como habilitar e desabilitar o licenciamento, consulte [como configurar ou desabilitar o licenciamento de aplicativos](how-to-set-up-or-disable-application-licensing.md).</span><span class="sxs-lookup"><span data-stu-id="4f740-114">For details about enabling and disabling licensing, see [How to Set Up or Disable Application Licensing](how-to-set-up-or-disable-application-licensing.md).</span></span>

## <span data-ttu-id="4f740-115">Políticas de provedor</span><span class="sxs-lookup"><span data-stu-id="4f740-115">Provider Policies</span></span>


<span data-ttu-id="4f740-116">Políticas de provedor foram desenvolvidas para o modelo de provedor de serviços de aplicativo (ASP).</span><span class="sxs-lookup"><span data-stu-id="4f740-116">Provider policies were developed for the Application Service Provider (ASP) model.</span></span> <span data-ttu-id="4f740-117">Nesse modelo, um único ASP pode hospedar um sistema de virtualização de aplicativo único para vários clientes, em que cada cliente precisa permanecer isolado.</span><span class="sxs-lookup"><span data-stu-id="4f740-117">In this model, a single ASP can host a single Application Virtualization System for multiple clients, where each client needs to remain isolated.</span></span> <span data-ttu-id="4f740-118">Os clientes podem ter requisitos drasticamente diferentes — por exemplo, um cliente pode exigir autenticação enquanto outro não.</span><span class="sxs-lookup"><span data-stu-id="4f740-118">Clients might have dramatically different requirements—for example, one client might require authentication while another does not.</span></span> <span data-ttu-id="4f740-119">Você pode usar políticas de provedor para associar permissões a clientes para que somente os usuários aprovados possam acessar cada aplicativo virtual ou pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="4f740-119">You can use provider policies to associate permissions with clients so that only the approved users can access each virtual application or virtual application package.</span></span>

<span data-ttu-id="4f740-120">Para o cliente empresarial, você pode usar esse recurso quando tiver requisitos de licenciamento estritos para um ou mais aplicativos.</span><span class="sxs-lookup"><span data-stu-id="4f740-120">For the enterprise customer, you can use this feature when you have strict licensing requirements for one or more applications.</span></span> <span data-ttu-id="4f740-121">Nessa situação, o componente de licenciamento está desabilitado na guia **pipeline do provedor** da caixa de diálogo **Propriedades do provedor** .</span><span class="sxs-lookup"><span data-stu-id="4f740-121">Under this situation, the licensing component is disabled on the **Provider Pipeline** tab of the **Provider Properties** dialog.</span></span>

<span data-ttu-id="4f740-122">A guia **pipeline do provedor** também tem caixas de seleção para habilitar autenticação, autorização (**reforçar as configurações de permissão de acesso**) e medição (**registrar informações de uso**).</span><span class="sxs-lookup"><span data-stu-id="4f740-122">The **Provider Pipeline** tab also has check boxes to enable authentication, authorization (**Enforce Access Permission Settings**), and metering (**Log Usage Information**).</span></span> <span data-ttu-id="4f740-123">Se a sua configuração tiver requisitos especiais, você poderá escrever seus próprios componentes de pipeline e adicioná-los ao sistema clicando no botão **avançado** .</span><span class="sxs-lookup"><span data-stu-id="4f740-123">If your configuration has special requirements, you can write your own pipeline components and add them to the system by clicking the **Advanced** button.</span></span>

## <span data-ttu-id="4f740-124">Autoridades da conta</span><span class="sxs-lookup"><span data-stu-id="4f740-124">Account Authorities</span></span>


<span data-ttu-id="4f740-125">A autoridade da conta é o domínio no qual o servidor do Application Virtualization está instalado.</span><span class="sxs-lookup"><span data-stu-id="4f740-125">The account authority is the domain in which the Application Virtualization Server is installed.</span></span> <span data-ttu-id="4f740-126">Ao passar pela instalação do servidor, você será solicitado a fornecer um nome de domínio; o domínio no qual o computador está instalado é detectado e usado por padrão.</span><span class="sxs-lookup"><span data-stu-id="4f740-126">As you proceed through the server installation, you are prompted to supply a domain name; the domain in which the computer is installed is detected and used by default.</span></span> <span data-ttu-id="4f740-127">Quando os usuários tentam entrar no sistema, eles são solicitados a fornecer suas credenciais antes de poderem acessar o domínio.</span><span class="sxs-lookup"><span data-stu-id="4f740-127">When users attempt to log in to the system, they are prompted for their credentials before they can access that domain.</span></span>

<span data-ttu-id="4f740-128">O sistema de virtualização de aplicativos dá suporte a vários domínios.</span><span class="sxs-lookup"><span data-stu-id="4f740-128">The Application Virtualization System supports multiple domains.</span></span> <span data-ttu-id="4f740-129">Você pode conceder acesso a aplicativos a grupos de usuários em outros domínios se uma relação de confiança for estabelecida entre domínios.</span><span class="sxs-lookup"><span data-stu-id="4f740-129">You can grant application access to user groups in other domains if a trust relationship is established between domains.</span></span> <span data-ttu-id="4f740-130">Os usuários devem fornecer credenciais que são reconhecidas por cada domínio.</span><span class="sxs-lookup"><span data-stu-id="4f740-130">Users must supply credentials that are recognized by each domain.</span></span>

<span data-ttu-id="4f740-131">No console de gerenciamento do servidor do Application Virtualization, você pode alterar o domínio primário (autoridade da conta) e as credenciais que são usadas para acessá-lo.</span><span class="sxs-lookup"><span data-stu-id="4f740-131">In the Application Virtualization Server Management Console, you can change the primary domain (account authority) and the credentials that are used to access it.</span></span>

## <span data-ttu-id="4f740-132">Autenticação</span><span class="sxs-lookup"><span data-stu-id="4f740-132">Authentication</span></span>


<span data-ttu-id="4f740-133">Autenticação é o mecanismo usado para confirmar a identidade do usuário.</span><span class="sxs-lookup"><span data-stu-id="4f740-133">Authentication is the mechanism used to confirm a user's identity.</span></span> <span data-ttu-id="4f740-134">Qualquer usuário com um nome de usuário e senha reconhecidos tem acesso.</span><span class="sxs-lookup"><span data-stu-id="4f740-134">Any user with a recognized user name and password has access.</span></span>

<span data-ttu-id="4f740-135">No sistema de virtualização de aplicativos, você pode habilitar ou desabilitar a autenticação por meio de uma caixa de seleção na guia **pipeline do provedor** . Por padrão, a autenticação do Windows está habilitada.</span><span class="sxs-lookup"><span data-stu-id="4f740-135">In the Application Virtualization System, you can enable or disable authentication through a check box on the **Provider Pipeline** tab. By default, Windows Authentication is enabled.</span></span>

## <span data-ttu-id="4f740-136">Autorização</span><span class="sxs-lookup"><span data-stu-id="4f740-136">Authorization</span></span>


<span data-ttu-id="4f740-137">Autorização é o processo usado para confirmar a identidade do usuário.</span><span class="sxs-lookup"><span data-stu-id="4f740-137">Authorization is the process used to confirm a user’s identity.</span></span> <span data-ttu-id="4f740-138">Depois de confirmar a identidade do usuário, o sistema determina se o usuário recebeu acesso ao sistema e para quais aplicativos o usuário recebeu acesso.</span><span class="sxs-lookup"><span data-stu-id="4f740-138">After confirming the user's identity, the system determines whether the user was granted access to the system and to which applications the user was granted access.</span></span> <span data-ttu-id="4f740-139">O console de gerenciamento de servidor do Application Virtualization tem uma caixa de seleção **impor configurações de permissão de acesso** na guia **pipeline do provedor** para habilitar ou desabilitar a autorização.</span><span class="sxs-lookup"><span data-stu-id="4f740-139">The Application Virtualization Server Management Console has an **Enforce Access Permission Settings** check box on the **Provider Pipeline** tab to enable or disable authorization.</span></span>

<span data-ttu-id="4f740-140">No sistema de virtualização de aplicativos, o acesso é concedido apenas a um grupo de usuários, e não a usuários individuais.</span><span class="sxs-lookup"><span data-stu-id="4f740-140">In the Application Virtualization System, access is granted to a user group only, not to individual users.</span></span>

## <span data-ttu-id="4f740-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f740-141">Related topics</span></span>


[<span data-ttu-id="4f740-142">Como gerenciar licenças de aplicativos no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="4f740-142">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="4f740-143">Como configurar ou desabilitar o licenciamento de aplicativo</span><span class="sxs-lookup"><span data-stu-id="4f740-143">How to Set Up or Disable Application Licensing</span></span>](how-to-set-up-or-disable-application-licensing.md)

[<span data-ttu-id="4f740-144">Server Management Console: nó Políticas de Provedor</span><span class="sxs-lookup"><span data-stu-id="4f740-144">Server Management Console: Provider Policies Node</span></span>](server-management-console-provider-policies-node.md)

 

 





