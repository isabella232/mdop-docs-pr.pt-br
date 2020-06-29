---
title: Identificar o número de instâncias do MED-V
description: Identificar o número de instâncias do MED-V
author: dansimp
ms.assetid: edea9bdf-a28c-4d24-9298-7bd6536c3a94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22f7d54318d2dc489461474e5531c5162d8c087d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799436"
---
# <span data-ttu-id="1fcc7-103">Identificar o número de instâncias do MED-V</span><span class="sxs-lookup"><span data-stu-id="1fcc7-103">Identify the Number of MED-V Instances</span></span>


<span data-ttu-id="1fcc7-104">Você precisa determinar o número de instâncias do MED-V, além de definir o escopo para cada instância para que você possa projetar a infraestrutura do servidor.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-104">You need to determine the number of MED-V instances, as well as define the scope for each instance so that you can design the server infrastructure.</span></span> <span data-ttu-id="1fcc7-105">Uma instância do MED-V inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1fcc7-105">A MED-V instance includes the following:</span></span>

-   <span data-ttu-id="1fcc7-106">O servidor MED-V e os espaços de trabalho do MED-V armazenados no servidor, incluindo permissões do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-106">The MED-V server and the MED-V workspaces stored on the server, including Active Directory permissions.</span></span>

-   <span data-ttu-id="1fcc7-107">Um banco de dados do SQL Server que armazena eventos do cliente.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-107">A SQL Server database that stores client events.</span></span> <span data-ttu-id="1fcc7-108">O banco de dados pode ser compartilhado por várias instâncias do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-108">The database may be shared by multiple MED-V instances.</span></span>

-   <span data-ttu-id="1fcc7-109">O repositório de imagens para as imagens do MED-V empacotadas.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-109">The image repository for the packed MED-V images.</span></span> <span data-ttu-id="1fcc7-110">O repositório pode ser compartilhado por várias instâncias do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-110">The repository may be shared by multiple MED-V instances.</span></span>

-   <span data-ttu-id="1fcc7-111">O console de gerenciamento usado para criar e compactar imagens e criar espaços de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-111">The management console used to create and pack images and to create MED-V workspaces.</span></span> <span data-ttu-id="1fcc7-112">O console não pode ser usado simultaneamente por várias instâncias do MED-V, mas pode ser desconectado de um servidor MED-V e, em seguida, conectado a um servidor MED-V diferente.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-112">The console cannot be used simultaneously by multiple MED-V instances, but it can be disconnected from one MED-V server and then connected to a different MED-V server.</span></span>

-   <span data-ttu-id="1fcc7-113">Os clientes do MED-V que recebem os espaços de trabalho do MED-V e a autorização para usá-los do servidor.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-113">MED-V clients that receive MED-V workspaces, and authorization to use them, from the server.</span></span>

<span data-ttu-id="1fcc7-114">Instâncias do MED-V separadas não podem ser integradas ou compartilhar espaços de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-114">Separate MED-V instances cannot be integrated or share MED-V workspaces.</span></span> <span data-ttu-id="1fcc7-115">Portanto, cada instância adicional descentraliza o gerenciamento de virtualização.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-115">Therefore, each additional instance decentralizes the virtualization management.</span></span>

## <span data-ttu-id="1fcc7-116">Determine o número de instâncias do MED-V necessárias</span><span class="sxs-lookup"><span data-stu-id="1fcc7-116">Determine the Number of MED-V Instances Required</span></span>


<span data-ttu-id="1fcc7-117">Comece pressupondo que você esteja usando uma instância do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-117">Start by assuming you are using one MED-V instance.</span></span> <span data-ttu-id="1fcc7-118">Em seguida, considere as seguintes condições e adicione mais instâncias para cada condição que se aplica à sua infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-118">Then, consider the following conditions, and add additional instances for each condition that applies to your infrastructure.</span></span>

-   <span data-ttu-id="1fcc7-119">Número de usuários com suporte — cada instância do MED-V pode oferecer suporte a até 5.000 clientes ativos simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-119">Number of supported users—Each MED-V instance can support up to 5,000 concurrently active clients.</span></span> <span data-ttu-id="1fcc7-120">Simultaneamente ativo significa que o cliente está online com o servidor MED-V e envia Polls para o servidor para obter atualizações de políticas e imagens, bem como eventos.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-120">Concurrently active means the client is online with the MED-V server and sending polls to the server for policy and image updates, as well as events.</span></span> <span data-ttu-id="1fcc7-121">Se sua infraestrutura incluir mais de 5.000 usuários ativos, adicione uma instância para cada 5.000 usuários.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-121">If your infrastructure will include more than 5,000 active users, add one instance for every 5,000 users.</span></span>

-   <span data-ttu-id="1fcc7-122">Usuários em domínios não confiáveis – as permissões do espaço de trabalho do MED-v Server associa o espaço de trabalho do MED-V do Active Directory com usuários e/ou grupos do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-122">Users in untrusted domains—The MED-V server associates MED-V workspace permissions with Active Directory users and/or groups.</span></span> <span data-ttu-id="1fcc7-123">Isso exige que os usuários do MED-V existam dentro do limite de confiança do servidor MED-V.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-123">This requires MED-V users to exist within the trust boundary of the MED-V server.</span></span> <span data-ttu-id="1fcc7-124">Adicione uma instância do MED-V para cada grupo de usuários do MED-V que está em um domínio separado e não confiável.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-124">Add one MED-V instance for each group of MED-V users that is in a separate, untrusted domain.</span></span>

-   <span data-ttu-id="1fcc7-125">Clientes em redes isoladas — determine se todos os clientes residem em redes isoladas e, portanto, exigem uma instância do MED-V separada.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-125">Clients in isolated networks—Determine whether any clients reside in networks that are isolated and therefore require a separate MED-V instance.</span></span> <span data-ttu-id="1fcc7-126">Por exemplo, as organizações muitas vezes isolam redes de laboratório de redes de produção.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-126">For example, organizations often isolate lab networks from production networks.</span></span> <span data-ttu-id="1fcc7-127">Adicione uma instância do MED-V a cada rede isolada que conterá clientes MED-V.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-127">Add a MED-V instance for each isolated network that will contain MED-V clients.</span></span>

-   <span data-ttu-id="1fcc7-128">Requisitos organizacionais — a organização pode exigir que um grupo de clientes seja gerenciado por uma instância do MED-V separada por motivos de segurança, como quando aplicativos confidenciais são entregues somente a um conjunto restrito de usuários em um domínio.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-128">Organizational requirements—The organization may require that a group of clients be managed by a separate MED-V instance for security reasons, such as when sensitive applications are delivered only to a restricted set of users within a domain.</span></span> <span data-ttu-id="1fcc7-129">Por exemplo, o departamento de folha de pagamento pode negar aos usuários de outros departamentos acesso à instância do MED-V que armazena a política para processamento de folha de pagamento.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-129">For example, the payroll department may deny users from other departments access to the MED-V instance that stores policy for payroll processing.</span></span> <span data-ttu-id="1fcc7-130">Além disso, se a organização usa um modelo de gerenciamento distribuído, uma instância do MED-V separada pode ser necessária para cada grupo de negócios com clientes MED-V a fim de permitir que o grupo Gerencie seu próprio ambiente virtualizado.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-130">Additionally, if the organization uses a distributed management model, a separate MED-V instance may be required for each business group having MED-V clients in order to enable the group to manage its own virtualized environment.</span></span> <span data-ttu-id="1fcc7-131">Adicione uma instância do MED-V para cada requisito organizacional individual.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-131">Add one MED-V instance for each separate organizational requirement.</span></span>

-   <span data-ttu-id="1fcc7-132">Considerações legais: problemas nacionais de segurança ou privacidade e leis fiduciárias podem exigir a separação de certos dados ou impedir que outros dados ultrapassem as bordas nacionais.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-132">Legal considerations—National security or privacy issues and fiduciary laws could require the separation of certain data or prevent other data from crossing national borders.</span></span> <span data-ttu-id="1fcc7-133">Se necessário, adicione mais instâncias do MED-V para atender a essa necessidade.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-133">If necessary, add additional MED-V instances to address this need.</span></span>

<span data-ttu-id="1fcc7-134">Depois de determinar o número de instâncias do MED-V necessárias para sua infraestrutura, bem como o raciocínio para cada uma, forneça um nome para cada instância.</span><span class="sxs-lookup"><span data-stu-id="1fcc7-134">After you determine the number of MED-V instances required for your infrastructure, as well as the reasoning for each one, provide a name for each instance.</span></span>

 

 





