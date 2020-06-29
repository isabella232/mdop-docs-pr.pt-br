---
title: Implantando o cliente do MBAM 2.5
description: Implantando o cliente do MBAM 2.5
author: dansimp
ms.assetid: 0a96a0ee-f280-49d9-a244-88f4147fe9fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 375af8966c8e66a58baec5065d065891187899fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799840"
---
# <span data-ttu-id="b8d3f-103">Implantando o cliente do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="b8d3f-103">Deploying the MBAM 2.5 Client</span></span>


<span data-ttu-id="b8d3f-104">O software cliente de administração e monitoramento do Microsoft BitLocker (MBAM) permite que os administradores imponham e monitorem a criptografia de unidade de disco BitLocker em computadores da empresa.</span><span class="sxs-lookup"><span data-stu-id="b8d3f-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client software enables administrators to enforce and monitor BitLocker Drive Encryption on computers in the enterprise.</span></span> <span data-ttu-id="b8d3f-105">O cliente BitLocker pode ser integrado a uma organização implantando o cliente por meio de um sistema de distribuição de software eletrônico, como os serviços de domínio Active Directory, ou diretamente criptografando os computadores cliente como parte do processo de imagem inicial.</span><span class="sxs-lookup"><span data-stu-id="b8d3f-105">The BitLocker client can be integrated into an organization by deploying the client through an electronic software distribution system, such as Active Directory Domain Services, or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="b8d3f-106">Dependendo de quando você implantar o software cliente de administração e monitoramento do Microsoft BitLocker, é possível habilitar a criptografia de unidade de disco BitLocker em um computador em sua organização antes de o usuário final receber o computador ou depois de configurar a política de grupo e implantar o software cliente do MBAM usando um sistema de implantação de software corporativo.</span><span class="sxs-lookup"><span data-stu-id="b8d3f-106">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring Client software, you can enable BitLocker Drive Encryption on a computer in your organization either before the end user receives the computer or afterwards by configuring Group Policy and deploying the MBAM Client software by using an enterprise software deployment system.</span></span>

## <span data-ttu-id="b8d3f-107">Implantar o cliente do MBAM em computadores desktop ou laptop</span><span class="sxs-lookup"><span data-stu-id="b8d3f-107">Deploy the MBAM Client to desktop or laptop computers</span></span>


<span data-ttu-id="b8d3f-108">Depois de definir as configurações da política de grupo, você pode usar um produto do sistema de implantação de software corporativo, como o MicrosoftSystemCenter2012 ConfigurationManager ou os serviços de domínio do Active Directory, para implantar os arquivos de instalação do cliente do MBAM no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="b8d3f-108">After configuring Group Policy settings, you can use an enterprise software deployment system product like MicrosoftSystemCenter2012 ConfigurationManager or Active Directory Domain Services to deploy the MBAM Client installation Windows Installer files to target computers.</span></span> <span data-ttu-id="b8d3f-109">Você pode usar os arquivos 32 de MbamClientSetup.exe bits ou 64 bits ou os arquivos de 32 bits ou 64 bits MBAMClient.msi, que são fornecidos com o software cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="b8d3f-109">You can use either the 32-bit or 64-bit MbamClientSetup.exe files or the 32-bit or 64-bit MBAMClient.msi files, which are provided with the MBAM Client software.</span></span> <span data-ttu-id="b8d3f-110">Para obter mais informações sobre a implantação de configurações de política de grupo do MBAM, consulte [implantando objetos de política de grupo do MBAM 2,5](deploying-mbam-25-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b8d3f-110">For more information about deploying MBAM Group Policy settings, see [Deploying MBAM 2.5 Group Policy Objects](deploying-mbam-25-group-policy-objects.md).</span></span>

<span data-ttu-id="b8d3f-111">**Observação**  A partir do MBAM 2,5 SP1, um MSI separado não está mais incluído no produto MBAM.</span><span class="sxs-lookup"><span data-stu-id="b8d3f-111">**Note** Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="b8d3f-112">No entanto, você pode extrair o MSI do arquivo executável (. exe) que está incluído no produto.</span><span class="sxs-lookup"><span data-stu-id="b8d3f-112">However, you can extract the MSI from the executable file (.exe) that is included with the product.</span></span>

 

[<span data-ttu-id="b8d3f-113">Como implantar o cliente do MBAM em computadores desktop ou notebooks</span><span class="sxs-lookup"><span data-stu-id="b8d3f-113">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25.md)

## <span data-ttu-id="b8d3f-114">Implantar o cliente MBAM como parte de uma implantação do Windows</span><span class="sxs-lookup"><span data-stu-id="b8d3f-114">Deploy the MBAM Client as part of a Windows deployment</span></span>


<span data-ttu-id="b8d3f-115">Nas organizações em que os computadores são recebidos e configurados centralmente, você pode instalar o cliente MBAM para gerenciar a criptografia de unidade de disco BitLocker em cada computador antes que os dados do usuário sejam gravados nele.</span><span class="sxs-lookup"><span data-stu-id="b8d3f-115">In organizations where computers are received and configured centrally, you can install the MBAM Client to manage BitLocker Drive Encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="b8d3f-116">A vantagem desse processo é que todos os computadores, em conformidade com a criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b8d3f-116">The benefit of this process is that every computer is then BitLocker Drive Encryption-compliant.</span></span> <span data-ttu-id="b8d3f-117">Esse método não depende da ação do usuário porque o administrador já criptografou o computador.</span><span class="sxs-lookup"><span data-stu-id="b8d3f-117">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="b8d3f-118">Uma pressuposição chave para esse cenário é que a política da organização instala uma imagem corporativa do Windows antes que o computador seja entregue ao usuário.</span><span class="sxs-lookup"><span data-stu-id="b8d3f-118">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span> <span data-ttu-id="b8d3f-119">Se as configurações de política de grupo tiverem sido configuradas para exigir um PIN, os usuários serão solicitados a definir um PIN depois de receberem a política.</span><span class="sxs-lookup"><span data-stu-id="b8d3f-119">If the Group Policy settings has been configured to require a PIN, users are prompted to set a PIN after they receive the policy.</span></span>

[<span data-ttu-id="b8d3f-120">Como habilitar o BitLocker por meio do MBAM como parte de uma implantação do Windows</span><span class="sxs-lookup"><span data-stu-id="b8d3f-120">How to Enable BitLocker by Using MBAM as Part of a Windows Deployment</span></span>](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)

## <span data-ttu-id="b8d3f-121">Como implantar o cliente MBAM usando uma linha de comando</span><span class="sxs-lookup"><span data-stu-id="b8d3f-121">How to deploy the MBAM Client by using a command line</span></span>


<span data-ttu-id="b8d3f-122">Esta seção explica como instalar o cliente MBAM usando uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="b8d3f-122">This section explains how to install the MBAM Client by using a command line.</span></span>

[<span data-ttu-id="b8d3f-123">Como implantar o cliente do MBAM usando uma linha de comando</span><span class="sxs-lookup"><span data-stu-id="b8d3f-123">How to Deploy the MBAM Client by Using a Command Line</span></span>](how-to-deploy-the-mbam-client-by-using-a-command-line.md)

## <span data-ttu-id="b8d3f-124">Outros recursos para a implantação do cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="b8d3f-124">Other resources for deploying the MBAM Client</span></span>


[<span data-ttu-id="b8d3f-125">Implantando o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="b8d3f-125">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)



## <span data-ttu-id="b8d3f-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b8d3f-126">Related topics</span></span>


[<span data-ttu-id="b8d3f-127">Implantando o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="b8d3f-127">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

[<span data-ttu-id="b8d3f-128">Planejamento do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="b8d3f-128">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

 
## <span data-ttu-id="b8d3f-129">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="b8d3f-129">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="b8d3f-130">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="b8d3f-130">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="b8d3f-131">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="b8d3f-131">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





