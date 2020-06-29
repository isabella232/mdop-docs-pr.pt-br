---
title: Implantando o Cliente do MBAM 1.0
description: Implantando o Cliente do MBAM 1.0
author: dansimp
ms.assetid: f7ca233f-5035-4ff9-ab3a-f2453b4929d1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dee8c2f4a9b398c9f0797ada35e4c36610c755b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799165"
---
# <span data-ttu-id="522b1-103">Implantando o Cliente do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="522b1-103">Deploying the MBAM 1.0 Client</span></span>


<span data-ttu-id="522b1-104">O cliente Microsoft BitLocker Administration and Monitoring (MBAM) permite que os administradores imponham e monitorem a criptografia de unidade de disco BitLocker em computadores da empresa.</span><span class="sxs-lookup"><span data-stu-id="522b1-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="522b1-105">O cliente BitLocker pode ser integrado a uma organização implantando o cliente por meio de ferramentas como os serviços de domínio do Active Directory ou diretamente criptografando os computadores cliente como parte do processo de imagem inicial.</span><span class="sxs-lookup"><span data-stu-id="522b1-105">The BitLocker client can be integrated into an organization by deploying the client through tools like Active Directory Domain Services or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="522b1-106">Dependendo de quando implantar o cliente do MBAM, você pode habilitar a criptografia do BitLocker em um computador em sua organização antes ou depois que o usuário final receber o computador.</span><span class="sxs-lookup"><span data-stu-id="522b1-106">Depending on when you deploy the MBAM Client, you can enable BitLocker encryption on a computer in your organization either before or after the end user receives the computer.</span></span> <span data-ttu-id="522b1-107">Para controlar esse tempo, configure a política de grupo e implante o software cliente do MBAM usando um sistema de implantação de software corporativo.</span><span class="sxs-lookup"><span data-stu-id="522b1-107">To control this timing, you configure Group Policy and deploy the MBAM Client software by using an enterprise software deployment system.</span></span>

<span data-ttu-id="522b1-108">Você pode usar um ou ambos os métodos em sua organização.</span><span class="sxs-lookup"><span data-stu-id="522b1-108">You can use either or both of these methods in your organization.</span></span> <span data-ttu-id="522b1-109">Se você usa os dois métodos, pode melhorar a conformidade, o relatório e o suporte à recuperação de chave.</span><span class="sxs-lookup"><span data-stu-id="522b1-109">If you use both methods, you can improve compliance, reporting, and key recovery support.</span></span>

## <span data-ttu-id="522b1-110">Implantar o cliente do MBAM em computadores desktop ou laptop</span><span class="sxs-lookup"><span data-stu-id="522b1-110">Deploy the MBAM Client to desktop or laptop computers</span></span>


<span data-ttu-id="522b1-111">Depois de configurar a política de grupo, você pode implantar os arquivos do Windows Installer de instalação do cliente do MBAM em computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="522b1-111">After you have configured Group Policy, you can deploy the MBAM Client installation Windows Installer files to target computers.</span></span> <span data-ttu-id="522b1-112">Você pode fazer isso usando um produto de sistema de implantação de software corporativo, como o Gerenciador de configuração do Microsoft System Center 2012 ou os serviços de domínio do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="522b1-112">You can do this by use of an enterprise software deployment system product like Microsoft System Center 2012 Configuration Manager or Active Directory Domain Services.</span></span> <span data-ttu-id="522b1-113">Os dois arquivos disponíveis do Windows Installer da instalação do cliente MBAM são MBAMClient-64bit.msi e MBAMClient-32bit.msi.</span><span class="sxs-lookup"><span data-stu-id="522b1-113">The two available MBAM Client installation Windows Installer files are MBAMClient-64bit.msi and MBAMClient-32bit.msi.</span></span> <span data-ttu-id="522b1-114">Esses arquivos são fornecidos com o software MBAM.</span><span class="sxs-lookup"><span data-stu-id="522b1-114">These files are provided with the MBAM software.</span></span> <span data-ttu-id="522b1-115">Para obter mais informações sobre como implantar objetos de política de grupo do MBAM, consulte [implantando objetos de política de grupo do MBAM 1,0](deploying-mbam-10-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="522b1-115">For more information about how to deploy MBAM Group Policy Objects, see [Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md).</span></span>

[<span data-ttu-id="522b1-116">Como implantar o cliente do MBAM em computadores desktop ou notebooks</span><span class="sxs-lookup"><span data-stu-id="522b1-116">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-1.md)

## <span data-ttu-id="522b1-117">Implantar o cliente MBAM como parte de uma implantação do Windows</span><span class="sxs-lookup"><span data-stu-id="522b1-117">Deploy the MBAM Client as part of a Windows deployment</span></span>


<span data-ttu-id="522b1-118">Em algumas organizações, novos computadores são recebidos e configurados centralmente.</span><span class="sxs-lookup"><span data-stu-id="522b1-118">In some organizations, new computers are received and configured centrally.</span></span> <span data-ttu-id="522b1-119">Essa situação permite que os administradores instalem o cliente do MBAM para gerenciar a criptografia do BitLocker em cada computador antes que todos os dados do usuário sejam gravados no computador.</span><span class="sxs-lookup"><span data-stu-id="522b1-119">This situation enables administrators to install the MBAM Client to manage BitLocker encryption on each computer before any user data is written to the computer.</span></span> <span data-ttu-id="522b1-120">Essa abordagem ajuda a garantir que os computadores sejam criptografados corretamente porque o administrador executa a ação sem depender de uma ação do usuário final.</span><span class="sxs-lookup"><span data-stu-id="522b1-120">This approach helps to ensure that computers are properly encrypted because the administrator performs the action without reliance on end-user action.</span></span> <span data-ttu-id="522b1-121">Uma pressuposição chave para esse cenário é que a política da organização instala uma imagem corporativa do Windows antes que o computador seja entregue ao usuário.</span><span class="sxs-lookup"><span data-stu-id="522b1-121">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span>

[<span data-ttu-id="522b1-122">Como implantar o cliente do MBAM como parte de uma implantação do Windows</span><span class="sxs-lookup"><span data-stu-id="522b1-122">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-1.md)

## <span data-ttu-id="522b1-123">Outros recursos para a implantação do cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="522b1-123">Other resources for deploying the MBAM Client</span></span>


[<span data-ttu-id="522b1-124">Implantando o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="522b1-124">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

[<span data-ttu-id="522b1-125">Planejar implantação de cliente MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="522b1-125">Planning for MBAM 1.0 Client Deployment</span></span>](planning-for-mbam-10-client-deployment.md)

 

 





