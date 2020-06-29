---
title: Implantando o Cliente do MBAM 2.0
description: Implantando o Cliente do MBAM 2.0
author: dansimp
ms.assetid: 3dd584fe-2a54-40f0-9bab-13ea74040b01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa42c8ab3adc273f0e00ba56a59f487deba89c6f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799274"
---
# <span data-ttu-id="245ba-103">Implantando o Cliente do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="245ba-103">Deploying the MBAM 2.0 Client</span></span>


<span data-ttu-id="245ba-104">O cliente Microsoft BitLocker Administration and Monitoring (MBAM) permite que os administradores imponham e monitorem a criptografia de unidade de disco BitLocker em computadores da empresa.</span><span class="sxs-lookup"><span data-stu-id="245ba-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="245ba-105">O cliente BitLocker pode ser integrado a uma organização implantando o cliente por meio de um sistema de distribuição de software eletrônico, como os serviços de domínio Active Directory, ou diretamente criptografando os computadores cliente como parte do processo de imagem inicial.</span><span class="sxs-lookup"><span data-stu-id="245ba-105">The BitLocker client can be integrated into an organization by deploying the client through an electronic software distribution system, such as Active Directory Domain Services, or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="245ba-106">Dependendo de quando implantar o cliente de administração e monitoramento do Microsoft BitLocker, você pode habilitar a criptografia do BitLocker em um computador em sua organização antes de o usuário final receber o computador ou depois de configurar a política de grupo e implantar o software cliente do MBAM usando um sistema de implantação de software corporativo.</span><span class="sxs-lookup"><span data-stu-id="245ba-106">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring Client, you can enable BitLocker encryption on a computer in your organization either before the end user receives the computer or afterwards by configuring Group Policy and deploying the MBAM Client software by using an enterprise software deployment system.</span></span>

## <span data-ttu-id="245ba-107">Implantar o cliente do MBAM em computadores desktop ou laptop</span><span class="sxs-lookup"><span data-stu-id="245ba-107">Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="245ba-108">Depois de configurar a política de grupo, você pode usar um produto do sistema de implantação de software corporativo, como o Microsoft System Center Configuration Manager 2012 ou os serviços de domínio do Active Directory, para implantar os arquivos do Windows Installer da instalação do cliente MBAM em computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="245ba-108">After configuring Group Policy, you can use an enterprise software deployment system product like Microsoft System Center Configuration Manager 2012 or Active Directory Domain Services to deploy the MBAM Client installation Windows Installer files to target computers.</span></span> <span data-ttu-id="245ba-109">Você pode implantar o cliente usando os arquivos de 32 bits ou 64 bits MbamClientSetup.exe, ou os arquivos de 32 bits ou 64 bits MBAMClient.msi, que são fornecidos com o software MBAM.</span><span class="sxs-lookup"><span data-stu-id="245ba-109">You can deploy the client by using either the 32-bit or 64-bit MbamClientSetup.exe files, or the 32-bit or 64-bit MBAMClient.msi files, which are provided with the MBAM software.</span></span> <span data-ttu-id="245ba-110">Para obter mais informações sobre a implantação de objetos de política de grupo do MBAM, consulte [implantando objetos de política de grupo do MBAM 2,0](deploying-mbam-20-group-policy-objects-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="245ba-110">For more information about deploying MBAM Group Policy Objects, see [Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md).</span></span>

[<span data-ttu-id="245ba-111">Como implantar o cliente do MBAM em computadores desktop ou notebooks</span><span class="sxs-lookup"><span data-stu-id="245ba-111">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-2.md)

## <span data-ttu-id="245ba-112">Implantar o cliente MBAM como parte de uma implantação do Windows</span><span class="sxs-lookup"><span data-stu-id="245ba-112">Deploy the MBAM Client as Part of a Windows Deployment</span></span>


<span data-ttu-id="245ba-113">Nas organizações em que os computadores são recebidos e configurados centralmente, você pode instalar o cliente MBAM para gerenciar a criptografia do BitLocker em cada computador antes que os dados do usuário sejam gravados nele.</span><span class="sxs-lookup"><span data-stu-id="245ba-113">In organizations where computers are received and configured centrally, you can install the MBAM Client to manage BitLocker encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="245ba-114">A vantagem desse processo é que cada computador está compatível com a criptografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="245ba-114">The benefit of this process is that every computer is then BitLocker encryption compliant.</span></span> <span data-ttu-id="245ba-115">Esse método não depende da ação do usuário porque o administrador já criptografou o computador.</span><span class="sxs-lookup"><span data-stu-id="245ba-115">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="245ba-116">Uma pressuposição chave para esse cenário é que a política da organização instala uma imagem corporativa do Windows antes que o computador seja entregue ao usuário.</span><span class="sxs-lookup"><span data-stu-id="245ba-116">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span> <span data-ttu-id="245ba-117">Se a política de grupo foi configurada para exigir um PIN, os usuários são solicitados a definir um PIN depois de receberem a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="245ba-117">If the Group Policy has been configured to require a PIN, users are prompted to set a PIN after they receive the Group Policy.</span></span>

[<span data-ttu-id="245ba-118">Como implantar o cliente do MBAM como parte de uma implantação do Windows</span><span class="sxs-lookup"><span data-stu-id="245ba-118">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-2.md)

## <span data-ttu-id="245ba-119">Como usar uma linha de comando para instalar o Cliente do MBAM</span><span class="sxs-lookup"><span data-stu-id="245ba-119">How to Use a Command Line to Install the MBAM Client</span></span>


<span data-ttu-id="245ba-120">Esta seção explica como instalar o cliente MBAM usando uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="245ba-120">This section explains how to install the MBAM Client by using a command line.</span></span>

[<span data-ttu-id="245ba-121">Como usar uma linha de comando para instalar o Cliente do MBAM</span><span class="sxs-lookup"><span data-stu-id="245ba-121">How to Use a Command Line to Install the MBAM Client</span></span>](how-to-use-a-command-line-to-install-the-mbam-client.md)

## <span data-ttu-id="245ba-122">Outros recursos para a implantação do cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="245ba-122">Other Resources for Deploying the MBAM Client</span></span>


<span data-ttu-id="245ba-123">[Implantando o MBAM 2,0](deploying-mbam-20-mbam-2.md)[planejando a implantação do MBAM 2,0 Client](planning-for-mbam-20-client-deployment-mbam-2.md)</span><span class="sxs-lookup"><span data-stu-id="245ba-123">[Deploying MBAM 2.0](deploying-mbam-20-mbam-2.md)[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)</span></span>

 

 





