---
title: Definir o escopo do projeto
description: Definir o escopo do projeto
author: dansimp
ms.assetid: 84637d2a-2e30-417d-b150-dc81f414b3a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4f33562452327bba9036f56d9f6f96650f00c1f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799313"
---
# <span data-ttu-id="9a827-103">Definir o escopo do projeto</span><span class="sxs-lookup"><span data-stu-id="9a827-103">Define the Project Scope</span></span>


<span data-ttu-id="9a827-104">Ao definir o escopo do projeto, determine o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9a827-104">When defining the project scope, determine the following:</span></span>

1.  <span data-ttu-id="9a827-105">Os usuários finais do MED-V – o local e o número de usuários finais são usados para determinar a localização das instalações do cliente MED-V e o número de instâncias do MED-V, bem como o número e o posicionamento de repositórios de imagens do MED-V.</span><span class="sxs-lookup"><span data-stu-id="9a827-105">The MED-V end users—the location and number of end users are used in determining the location of MED-V client installations and the number of MED-V instances, as well as the number and placement of MED-V image repositories.</span></span>

2.  <span data-ttu-id="9a827-106">As imagens da máquina virtual (VM) a serem gerenciadas pelo MED-V – para determinar o método de distribuição de imagens e posicionamento de repositórios de imagens.</span><span class="sxs-lookup"><span data-stu-id="9a827-106">The virtual machine (VM) images to be managed by MED-V—to determine the method of distributing images and placement of image repositories.</span></span>

3.  <span data-ttu-id="9a827-107">As expectativas de nível de serviço da organização — para determinar os requisitos de desempenho e tolerância a falhas para o servidor e o banco de dados do MED-V, bem como o repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="9a827-107">The organization’s service level expectations—to determine the performance and fault-tolerance requirements for the MED-V server and database as well as the image repository.</span></span>

4.  <span data-ttu-id="9a827-108">Valide-se com a empresa — Verifique se há uma compreensão completa de como a infraestrutura planejada afeta a empresa.</span><span class="sxs-lookup"><span data-stu-id="9a827-108">Validate with the business—ensure there is a complete understanding of how the planned infrastructure affects the business.</span></span>

## <span data-ttu-id="9a827-109">Definir os usuários finais do MED-V</span><span class="sxs-lookup"><span data-stu-id="9a827-109">Define the MED-V End Users</span></span>


<span data-ttu-id="9a827-110">Primeiro, determine onde os usuários finais estão localizados, bem como o número de usuários em cada local.</span><span class="sxs-lookup"><span data-stu-id="9a827-110">First, determine where the end users are located, as well as the number of users in each location.</span></span> <span data-ttu-id="9a827-111">Em seguida, obtenha um diagrama de infraestrutura de rede que exiba os locais do usuário e a largura de banda disponível para esses locais.</span><span class="sxs-lookup"><span data-stu-id="9a827-111">Second, obtain a network infrastructure diagram that displays the user locations and the available bandwidth to those locations.</span></span> <span data-ttu-id="9a827-112">Terceiro, descubra se os usuários viajam entre locais.</span><span class="sxs-lookup"><span data-stu-id="9a827-112">Third, find out if users travel between locations.</span></span> <span data-ttu-id="9a827-113">Se os usuários viajarem, talvez seja necessário capacidade adicional no design dos repositórios de infraestrutura e imagem do servidor.</span><span class="sxs-lookup"><span data-stu-id="9a827-113">If users travel, additional capacity may be required in the design of the server infrastructure and image repositories.</span></span>

## <span data-ttu-id="9a827-114">Determinar as imagens do MED-V a serem gerenciadas pelo MED-V</span><span class="sxs-lookup"><span data-stu-id="9a827-114">Determine the MED-V Images to Be Managed by MED-V</span></span>


<span data-ttu-id="9a827-115">Depois que os usuários finais do MED-V tiverem sido definidos, determine quais VMs serão gerenciadas pelo MED-V para os usuários em cada local.</span><span class="sxs-lookup"><span data-stu-id="9a827-115">After the MED-V end users have been defined, determine which VMs will be managed by MED-V for the users in each location.</span></span>

<span data-ttu-id="9a827-116">Se qualquer uma das VMs estiver armazenada em uma biblioteca centralizada, determine o local da biblioteca para que ela possa ser avaliada para uso como um repositório do MED-V.</span><span class="sxs-lookup"><span data-stu-id="9a827-116">If any of the VMs are stored in a centralized library, determine the location of the library so that it may be evaluated for use as a MED-V repository.</span></span>

## <a href="" id="determine-the-organization-s-service-level-expectations"></a><span data-ttu-id="9a827-117">Determinar as expectativas de nível de serviço da organização</span><span class="sxs-lookup"><span data-stu-id="9a827-117">Determine the Organization’s Service Level Expectations</span></span>


<span data-ttu-id="9a827-118">Para cada espaço de trabalho do MED-V, observe o tempo aceitável para uma nova imagem carregar e o período de tempo para atualizações críticas a serem implantadas.</span><span class="sxs-lookup"><span data-stu-id="9a827-118">For each MED-V workspace, note the acceptable time for a new image to load and the timeframe for critical updates to be deployed.</span></span>

<span data-ttu-id="9a827-119">Se aplicável, registre as expectativas de nível de serviço para relatórios do MED-V a serem usados no design da infraestrutura do servidor.</span><span class="sxs-lookup"><span data-stu-id="9a827-119">If applicable, record the service level expectations for MED-V reporting, to be used in the design of the server infrastructure.</span></span>

## <span data-ttu-id="9a827-120">Validar com o negócio</span><span class="sxs-lookup"><span data-stu-id="9a827-120">Validate with the Business</span></span>


<span data-ttu-id="9a827-121">Pergunte aos stakeholders de negócios e aos proprietários de aplicativos as seguintes perguntas:</span><span class="sxs-lookup"><span data-stu-id="9a827-121">Ask business stakeholders and application owners the following questions:</span></span>

-   <span data-ttu-id="9a827-122">Há imagens existentes que possam ser combinadas?</span><span class="sxs-lookup"><span data-stu-id="9a827-122">Are there any existing images that can be combined?</span></span> <span data-ttu-id="9a827-123">Por exemplo, se o aplicativo A em WindowsXP for uma imagem do VPC e o aplicativo B no WindowsXP for outra imagem do VPC, talvez uma única imagem possa conter ambos os aplicativos, reduzindo o espaço do repositório e a largura de banda necessária para o download da imagem.</span><span class="sxs-lookup"><span data-stu-id="9a827-123">For example, if application A on WindowsXP is one VPC image and application B on WindowsXP is another VPC image, perhaps a single image can contain both applications, thereby reducing repository space and bandwidth required for image download.</span></span>

-   <span data-ttu-id="9a827-124">Os aplicativos em escopo são licenciados e compatíveis, se entregues em uma VM pelo MED-V?</span><span class="sxs-lookup"><span data-stu-id="9a827-124">Are the in-scope applications licensable and supportable if delivered in a VM by MED-V?</span></span> <span data-ttu-id="9a827-125">Consulte o fornecedor do aplicativo para garantir que os termos de licenciamento e suporte não sejam violados ao entregar o aplicativo pelo MED-V.</span><span class="sxs-lookup"><span data-stu-id="9a827-125">Check with the application supplier to ensure that licensing and support terms will not be violated by delivering the application through MED-V.</span></span>

 

 





