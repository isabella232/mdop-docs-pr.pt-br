---
title: Projetar os repositórios de imagens do MED-V
description: Projetar os repositórios de imagens do MED-V
author: dansimp
ms.assetid: e153154d-2751-4990-b94d-a2d76242c15f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0c59a0dd2d1b3a78bd211c6a6353a86c77d8fc2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799307"
---
# <span data-ttu-id="25be1-103">Projetar os repositórios de imagens do MED-V</span><span class="sxs-lookup"><span data-stu-id="25be1-103">Design the MED-V Image Repositories</span></span>


<span data-ttu-id="25be1-104">Após a criação e a compactação de imagens do MED-V, elas podem ser armazenadas em um servidor de arquivos em qualquer local.</span><span class="sxs-lookup"><span data-stu-id="25be1-104">After MED-V images are created and packed, they can be stored on a file server in any location.</span></span> <span data-ttu-id="25be1-105">Os arquivos podem ser enviados por HTTP ou HTTPS por um ou mais servidores IIS.</span><span class="sxs-lookup"><span data-stu-id="25be1-105">The files may be sent over HTTP or HTTPS by one or more IIS servers.</span></span> <span data-ttu-id="25be1-106">O repositório de imagens pode ser compartilhado por várias instâncias do MED-V.</span><span class="sxs-lookup"><span data-stu-id="25be1-106">The image repository can be shared by multiple MED-V instances.</span></span>

<span data-ttu-id="25be1-107">Para projetar os repositórios de imagens, primeiro você deve decidir como as imagens serão implantadas em cada cliente e, se o cliente exigir um repositório de imagens local.</span><span class="sxs-lookup"><span data-stu-id="25be1-107">To design the image repositories, you must first decide how the images will be deployed to each client and then whether that client requires a local image repository.</span></span> <span data-ttu-id="25be1-108">Em seguida, cada repositório é projetado e colocado, juntamente com seu servidor IIS correspondente.</span><span class="sxs-lookup"><span data-stu-id="25be1-108">Each repository is then designed and placed, along with its accompanying IIS server.</span></span>

## <span data-ttu-id="25be1-109">Determinar como as imagens serão implantadas</span><span class="sxs-lookup"><span data-stu-id="25be1-109">Determine How Images Will Be Deployed</span></span>


<span data-ttu-id="25be1-110">Para cada espaço de trabalho do MED-V, decida como você planeja implantar imagens do MED-V no cliente.</span><span class="sxs-lookup"><span data-stu-id="25be1-110">For each MED-V workspace, decide how you plan to deploy MED-V images to the client.</span></span> <span data-ttu-id="25be1-111">Isso é importante na determinação de quantos repositórios são necessários para armazenar as imagens compactadas, onde esses repositórios serão colocados e, em seguida, projetar esses repositórios.</span><span class="sxs-lookup"><span data-stu-id="25be1-111">This is important in determining how many repositories are necessary to store the packed images, where those repositories will be placed, and then to design those repositories.</span></span>

<span data-ttu-id="25be1-112">Imagens compactadas podem ser implantadas das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="25be1-112">Packed images can be deployed in the following ways:</span></span>

-   <span data-ttu-id="25be1-113">Baixado pela rede a partir de um servidor de distribuição de imagens, que inclui um servidor de arquivos e um servidor IIS.</span><span class="sxs-lookup"><span data-stu-id="25be1-113">Downloaded over the network from an image distribution server, which comprises a file server and IIS server.</span></span>

-   <span data-ttu-id="25be1-114">Em mídia removível, como uma unidade USB ou DVD.</span><span class="sxs-lookup"><span data-stu-id="25be1-114">On removable media, such as a USB drive or DVD.</span></span>

-   <span data-ttu-id="25be1-115">Pré-preparado para um diretório de repositório de imagens no computador cliente usando um centro de distribuição de software corporativo.</span><span class="sxs-lookup"><span data-stu-id="25be1-115">Pre-staged to an image store directory on the client computer using an enterprise software distribution center.</span></span>

<span data-ttu-id="25be1-116">Decida qual método, ou métodos, será usado para implantar imagens do MED-V em cada um dos clientes e se o local exigirá um repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="25be1-116">Decide which method, or methods, will be used to deploy MED-V images to each of the clients and whether the location will require an image repository.</span></span>

## <span data-ttu-id="25be1-117">Determinar o número de repositórios de imagens</span><span class="sxs-lookup"><span data-stu-id="25be1-117">Determine the Number of Image Repositories</span></span>


<span data-ttu-id="25be1-118">Agora que você determinou o número mínimo de repositórios necessários, adicione mais se qualquer um dos seguintes critérios se aplicar:</span><span class="sxs-lookup"><span data-stu-id="25be1-118">Now that you have determined the minimum number of repositories you need, add more if any of the following criteria apply:</span></span>

-   <span data-ttu-id="25be1-119">Razões organizacionais ou normativas para separar as imagens do MED-V – algumas imagens do MED-V podem não ser capazes de coexistir no mesmo repositório.</span><span class="sxs-lookup"><span data-stu-id="25be1-119">Organizational or regulatory reasons to separate the MED-V images—some MED-V images may not be able to coexist in the same repository.</span></span> <span data-ttu-id="25be1-120">Por exemplo, dados pessoais confidenciais podem exigir armazenamento em um servidor que só esteja disponível para um conjunto limitado de funcionários que precisem de acesso aos dados.</span><span class="sxs-lookup"><span data-stu-id="25be1-120">For example, sensitive personal data may require storage on a server that is only available to a limited set of employees who need access to the data.</span></span>

-   <span data-ttu-id="25be1-121">Clientes em redes isoladas — se as imagens forem implantadas na rede, determine se qualquer rede está isolada e exija um repositório separado.</span><span class="sxs-lookup"><span data-stu-id="25be1-121">Clients in isolated networks—if images will be deployed over the network, determine whether any networks are isolated and require a separate repository.</span></span> <span data-ttu-id="25be1-122">Por exemplo, as organizações muitas vezes isolam redes de laboratório de redes de produção.</span><span class="sxs-lookup"><span data-stu-id="25be1-122">For example, organizations often isolate lab networks from production networks.</span></span>

-   <span data-ttu-id="25be1-123">Clientes em redes remotas — se as imagens forem implantadas na rede, algumas máquinas cliente poderão ser separadas do repositório por links de rede com largura de banda insuficiente para fornecer uma experiência adequada quando um cliente carregar um espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="25be1-123">Clients in remote networks—if images will be deployed over the network, some client machines may be separated from the repository by network links that have insufficient bandwidth to provide an adequate experience when a client loads a MED-V workspace.</span></span> <span data-ttu-id="25be1-124">Se necessário, crie instâncias do MED-V adicionais para atender a essa necessidade.</span><span class="sxs-lookup"><span data-stu-id="25be1-124">If necessary, design additional MED-V instances to address this need.</span></span>

<span data-ttu-id="25be1-125">Adicione esses repositórios ao design.</span><span class="sxs-lookup"><span data-stu-id="25be1-125">Add these repositories to the design.</span></span> <span data-ttu-id="25be1-126">Escolha um nome para cada repositório e o motivo para criá-lo.</span><span class="sxs-lookup"><span data-stu-id="25be1-126">Decide on a name for each repository and the reason for designing it.</span></span> <span data-ttu-id="25be1-127">Decida quais imagens do MED-V serão mantidas pelos repositórios e quais clientes do MED-V carregará os espaços de trabalho do MED-V com imagens do repositório.</span><span class="sxs-lookup"><span data-stu-id="25be1-127">Decide which MED-V images the repositories will hold and which MED-V clients will load MED-V workspaces with images from the repository.</span></span>

## <span data-ttu-id="25be1-128">Criar e colocar os repositórios de imagens</span><span class="sxs-lookup"><span data-stu-id="25be1-128">Design and Place the Image Repositories</span></span>


<span data-ttu-id="25be1-129">Quando uma nova imagem está disponível para clientes, os clientes começam a baixar a imagem, possivelmente simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="25be1-129">When a new image is available to clients, clients begin downloading the image, possibly simultaneously.</span></span> <span data-ttu-id="25be1-130">Isso cria uma demanda alta no repositório e deve ser levado em conta durante a criação do repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="25be1-130">This creates a high demand on the repository and must be taken into account when designing the image repository.</span></span>

<span data-ttu-id="25be1-131">Para cada repositório, determine a quantidade de dados que será armazenada.</span><span class="sxs-lookup"><span data-stu-id="25be1-131">For each repository, determine the amount of data it will store.</span></span> <span data-ttu-id="25be1-132">Somar os tamanhos das imagens que serão armazenadas no repositório.</span><span class="sxs-lookup"><span data-stu-id="25be1-132">Sum the sizes of images that will be stored in the repository.</span></span> <span data-ttu-id="25be1-133">Esse é o valor do espaço em disco necessário no servidor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="25be1-133">This is the value of the disk space required on the file server.</span></span>

<span data-ttu-id="25be1-134">Em seguida, adicione o número de clientes que podem baixar imagens do MED-V do repositório.</span><span class="sxs-lookup"><span data-stu-id="25be1-134">Next, add up the number of clients that may download MED-V images from the repository.</span></span> <span data-ttu-id="25be1-135">Este é o número máximo de downloads simultâneos que podem ocorrer quando uma nova imagem do MED-V é carregada no repositório.</span><span class="sxs-lookup"><span data-stu-id="25be1-135">This is the maximum number of concurrent downloads that can occur when a new MED-V image is loaded into the repository.</span></span> <span data-ttu-id="25be1-136">O servidor de arquivos deve ser projetado com um subsistema de disco que pode atender às demandas de e/s que isso criará.</span><span class="sxs-lookup"><span data-stu-id="25be1-136">The file server must be designed with a disk subsystem that can meet the IO demands this will create.</span></span>

<span data-ttu-id="25be1-137">O repositório de imagens pode residir no mesmo sistema do servidor MED-V e do servidor que executa o SQL Server, ou em um compartilhamento de arquivos remoto.</span><span class="sxs-lookup"><span data-stu-id="25be1-137">The image repository can reside on the same system as the MED-V server and the server running SQL Server, or on a remote file share.</span></span> <span data-ttu-id="25be1-138">Você também pode executá-lo em uma VM do Windows Server2008 Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="25be1-138">You can also run it in a Windows Server2008 Hyper-V VM.</span></span> <span data-ttu-id="25be1-139">Verifique o local de rede dos clientes que o repositório de imagens vai atender e coloque o repositório em um local de rede onde ele terá largura de banda suficiente para atender às expectativas de nível de serviço desses clientes.</span><span class="sxs-lookup"><span data-stu-id="25be1-139">Check the network location of the clients that the image repository will service, and place the repository in a network location where it will have sufficient bandwidth to meet the service level expectations of those clients.</span></span>

### <span data-ttu-id="25be1-140">Tolerância a falhas</span><span class="sxs-lookup"><span data-stu-id="25be1-140">Fault Tolerance</span></span>

<span data-ttu-id="25be1-141">Se o repositório de imagens não estiver disponível, os clientes não poderão baixar imagens do MED-V novas ou atualizadas.</span><span class="sxs-lookup"><span data-stu-id="25be1-141">If the image repository is unavailable, clients will not be able to download new or updated MED-V images.</span></span> <span data-ttu-id="25be1-142">Para criar opções de tolerância a falhas para o servidor de arquivos e discos tolerantes a falhas, consulte o guia [planejamento e design de infraestrutura Microsoft SQL server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) .</span><span class="sxs-lookup"><span data-stu-id="25be1-142">To design fault-tolerance options for the file server and fault-tolerant disks, see the [Infrastructure Planning and Design Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) guide.</span></span>

## <span data-ttu-id="25be1-143">Projetar e colocar os servidores IIS</span><span class="sxs-lookup"><span data-stu-id="25be1-143">Design and Place the IIS Servers</span></span>


<span data-ttu-id="25be1-144">Esta seção só será relevante se os clientes baixarem arquivos de imagem pela rede usando HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="25be1-144">This section is only relevant if clients will download image files over the network using HTTP or HTTPS.</span></span>

<span data-ttu-id="25be1-145">O servidor IIS pode coexistir no mesmo sistema que o servidor MED-V e o servidor que executa o SQL Server.</span><span class="sxs-lookup"><span data-stu-id="25be1-145">The IIS server can coexist on the same system as the MED-V server and the server running SQL Server.</span></span> <span data-ttu-id="25be1-146">Ele também pode ser executado em uma VM do Windows Server2008 Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="25be1-146">It can also run in a Windows Server2008 Hyper-V VM.</span></span> <span data-ttu-id="25be1-147">A infraestrutura do servidor IIS deve ter throughput suficiente para fornecer imagens aos clientes nas expectativas do nível de serviço da organização.</span><span class="sxs-lookup"><span data-stu-id="25be1-147">The IIS server infrastructure must have sufficient throughput to deliver images to clients within the service level expectations of the organization.</span></span> <span data-ttu-id="25be1-148">Ele deve ser projetado com um subsistema de disco que possa atender às demandas de e/s que isso cria.</span><span class="sxs-lookup"><span data-stu-id="25be1-148">It must be designed with a disk subsystem that can meet the IO demands this creates.</span></span>

<span data-ttu-id="25be1-149">Para cada repositório de imagens, some o número de clientes que podem baixar imagens do MED-V usando o IIS.</span><span class="sxs-lookup"><span data-stu-id="25be1-149">For each image repository, sum the number of clients that may download MED-V images using IIS.</span></span> <span data-ttu-id="25be1-150">Este é o número máximo de downloads simultâneos que podem ocorrer quando uma imagem é carregada no repositório.</span><span class="sxs-lookup"><span data-stu-id="25be1-150">This is the maximum number of concurrent downloads that can occur when an image is loaded into the repository.</span></span> <span data-ttu-id="25be1-151">Use a soma da taxa de serviço e as expectativas de nível de serviço determinadas em [definir o escopo do projeto](define-the-project-scope.md) para planejar o design da infraestrutura do servidor IIS e para determinar a quantidade apropriada de largura de banda a ser alocada para o repositório.</span><span class="sxs-lookup"><span data-stu-id="25be1-151">Use the throughput sum and the service level expectations determined in [Define the Project Scope](define-the-project-scope.md) to plan the design of the IIS server infrastructure and to determine the appropriate amount of bandwidth to allocate for the repository.</span></span>

<span data-ttu-id="25be1-152">Para projetar a infraestrutura do IIS, consulte o guia [planejamento de infraestrutura e design do Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) .</span><span class="sxs-lookup"><span data-stu-id="25be1-152">To design the IIS infrastructure, see the [Infrastructure Planning and Design Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) guide.</span></span>

### <span data-ttu-id="25be1-153">Tolerância a falhas</span><span class="sxs-lookup"><span data-stu-id="25be1-153">Fault Tolerance</span></span>

<span data-ttu-id="25be1-154">Se a infraestrutura do servidor IIS não estiver disponível, os clientes não poderão baixar imagens novas ou atualizadas.</span><span class="sxs-lookup"><span data-stu-id="25be1-154">If the IIS server infrastructure is unavailable, clients will not be able to download new or updated images.</span></span> <span data-ttu-id="25be1-155">Para configurar a tolerância a falhas, o servidor IIS baseado no Windows Server2008 pode ser colocado em um cluster de failover.</span><span class="sxs-lookup"><span data-stu-id="25be1-155">To configure fault tolerance, the Windows Server2008-based IIS server can be placed in a failover cluster.</span></span> <span data-ttu-id="25be1-156">Para projetar a tolerância a falhas para a infraestrutura do servidor IIS, consulte o guia [planejamento de infraestrutura e design do Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) .</span><span class="sxs-lookup"><span data-stu-id="25be1-156">To design the fault tolerance for the IIS server infrastructure, see the [Infrastructure Planning and Design Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) guide.</span></span>

## <span data-ttu-id="25be1-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="25be1-157">Related topics</span></span>


[<span data-ttu-id="25be1-158">Implantando um espaço de trabalho do MED-V usando um sistema de distribuição de software empresarial</span><span class="sxs-lookup"><span data-stu-id="25be1-158">Deploying a MED-V Workspace Using an Enterprise Software Distribution System</span></span>](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md)

[<span data-ttu-id="25be1-159">Implantando um espaço de trabalho do MED-V usando um pacote de implantação</span><span class="sxs-lookup"><span data-stu-id="25be1-159">Deploying a MED-V Workspace Using a Deployment Package</span></span>](deploying-a-med-v-workspace-using-a-deployment-package.md)

 

 





