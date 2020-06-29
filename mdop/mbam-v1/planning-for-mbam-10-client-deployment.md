---
title: Planejar implantação de cliente MBAM 1.0
description: Planejar implantação de cliente MBAM 1.0
author: dansimp
ms.assetid: 3af2e7f3-134b-4ab9-9847-b07474ca6ac3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d58d6420febd2da9ee9cd4074fc8b5870285b0b4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799760"
---
# <span data-ttu-id="33ccf-103">Planejar implantação de cliente MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="33ccf-103">Planning for MBAM 1.0 Client Deployment</span></span>


<span data-ttu-id="33ccf-104">Dependendo de quando você implantar o cliente Microsoft BitLocker Administration and Monitoring (MBAM), você pode habilitar a criptografia do BitLocker em um computador em sua organização antes de o usuário final receber o computador ou depois.</span><span class="sxs-lookup"><span data-stu-id="33ccf-104">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client, you can enable BitLocker encryption on a computer in your organization either before the end user receives the computer or afterwards.</span></span> <span data-ttu-id="33ccf-105">Para habilitar a criptografia BitLocker após o usuário final receber o computador, configure a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="33ccf-105">To enable BitLocker encryption after the end user receives the computer, configure Group Policy.</span></span> <span data-ttu-id="33ccf-106">Para habilitar a criptografia do BitLocker antes de o usuário final receber o computador, implante o software cliente do MBAM usando um sistema de implantação de software corporativo.</span><span class="sxs-lookup"><span data-stu-id="33ccf-106">To enable BitLocker encryption before the end user receives the computer, deploy the MBAM Client software by using an enterprise software deployment system.</span></span>

<span data-ttu-id="33ccf-107">Você pode usar um ou os dois métodos em sua organização.</span><span class="sxs-lookup"><span data-stu-id="33ccf-107">You can use one or both methods in your organization.</span></span> <span data-ttu-id="33ccf-108">Se você usa os dois métodos, pode melhorar a conformidade, o relatório e o suporte à recuperação de chave.</span><span class="sxs-lookup"><span data-stu-id="33ccf-108">If you use both methods, you can improve compliance, reporting, and key recovery support.</span></span>

<span data-ttu-id="33ccf-109">**Observação**  Para verificar os requisitos do sistema do cliente do MBAM, consulte [configurações compatíveis do MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="33ccf-109">**Note** To review the MBAM Client system requirements, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

## <span data-ttu-id="33ccf-110">Implantando o cliente do MBAM para habilitar a criptografia do BitLocker após a distribuição do computador para usuários finais</span><span class="sxs-lookup"><span data-stu-id="33ccf-110">Deploying the MBAM Client to enable BitLocker encryption after computer distribution to end users</span></span>


<span data-ttu-id="33ccf-111">Depois de configurar a política de grupo, você pode usar um produto do sistema de implantação de software corporativo, como o Microsoft System Center Configuration Manager 2012 ou os serviços de domínio do Active Directory, para implantar os arquivos do Windows Installer da instalação do cliente do MBAM para os computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="33ccf-111">After you configure the Group Policy, you can use an enterprise software deployment system product, such as Microsoft System Center Configuration Manager 2012 or Active Directory Domain Services, to deploy the MBAM Client installation Windows Installer files to the target computers.</span></span> <span data-ttu-id="33ccf-112">Os dois arquivos de instalação do cliente MBAM do Windows Installer são MBAMClient-64bit.msi e MBAMClient-32bit.msi, que são fornecidos com o software do MBAM.</span><span class="sxs-lookup"><span data-stu-id="33ccf-112">The two MBAM Client installation Windows Installer files are MBAMClient-64bit.msi and MBAMClient-32bit.msi, which are provided with the MBAM software.</span></span> <span data-ttu-id="33ccf-113">Para obter mais informações sobre como implantar objetos de política de grupo do MBAM, consulte [implantando objetos de política de grupo do MBAM 1,0](deploying-mbam-10-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="33ccf-113">For more information about how to deploy MBAM Group Policy Objects, see [Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md).</span></span>

<span data-ttu-id="33ccf-114">Quando você implanta o cliente MBAM, depois de distribuir os computadores para os usuários finais, os usuários finais são solicitados a criptografar seus computadores.</span><span class="sxs-lookup"><span data-stu-id="33ccf-114">When you deploy the MBAM Client, after you distribute the computers to end users, the end users are prompted to encrypt their computers.</span></span> <span data-ttu-id="33ccf-115">Isso permite que o MBAM colete os dados para incluir o PIN e a senha e, em seguida, iniciar o processo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="33ccf-115">This lets MBAM collect the data, to include the PIN and password, and then begin the encryption process.</span></span>

<span data-ttu-id="33ccf-116">**Observação**  Nessa abordagem, os usuários são solicitados a ativar e inicializar o chip Trusted Platform Module (TPM), se ele não tiver sido ativado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="33ccf-116">**Note** In this approach, users are prompted to activate and initialize the Trusted Platform Module (TPM) chip, if it has not been previously activated.</span></span>

 

## <span data-ttu-id="33ccf-117">Usando o cliente MBAM para habilitar a criptografia do BitLocker antes da distribuição do computador para usuários finais</span><span class="sxs-lookup"><span data-stu-id="33ccf-117">Using the MBAM Client to enable BitLocker encryption before computer distribution to end users</span></span>


<span data-ttu-id="33ccf-118">Nas organizações em que os computadores são recebidos e configurados centralmente, você pode instalar o cliente MBAM para gerenciar a criptografia do BitLocker em cada computador antes que os dados do usuário sejam gravados nele.</span><span class="sxs-lookup"><span data-stu-id="33ccf-118">In organizations where computers are received and configured centrally, you can install the MBAM Client to manage BitLocker encryption on each computer before any user data is written on it.</span></span> <span data-ttu-id="33ccf-119">A vantagem desse processo é que cada computador será compatível com a criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="33ccf-119">The benefit of this process is that every computer will then be compliant with the BitLocker encryption.</span></span> <span data-ttu-id="33ccf-120">Esse método não depende da ação do usuário porque o administrador já criptografou o computador.</span><span class="sxs-lookup"><span data-stu-id="33ccf-120">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="33ccf-121">Uma pressuposição chave para esse cenário é que a política da organização instala uma imagem corporativa do Windows antes que o computador seja entregue ao usuário.</span><span class="sxs-lookup"><span data-stu-id="33ccf-121">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span>

<span data-ttu-id="33ccf-122">Se a sua organização deseja usar (TPM) para criptografar computadores, o administrador deve criptografar o volume do sistema operacional do computador com o protetor TPM.</span><span class="sxs-lookup"><span data-stu-id="33ccf-122">If your organization wants to use (TPM) to encrypt computers, the administrator must encrypt the operating system volume of the computer with TPM protector.</span></span> <span data-ttu-id="33ccf-123">Se a sua organização quiser usar o chip TPM e um protetor de PIN, o administrador deve criptografar o volume do sistema com o protetor TPM e, em seguida, os usuários selecionam um PIN na primeira vez em que fazem logon.</span><span class="sxs-lookup"><span data-stu-id="33ccf-123">If your organization wants to use the TPM chip and a PIN protector, the administrator must encrypt the system volume with the TPM protector, and then the users select a PIN the first time they log on.</span></span> <span data-ttu-id="33ccf-124">Se a sua organização decidir usar apenas o protetor de PIN, o administrador não precisará criptografar o volume primeiro.</span><span class="sxs-lookup"><span data-stu-id="33ccf-124">If your organization decides to use only the PIN protector, the administrator does not have to encrypt the volume first.</span></span> <span data-ttu-id="33ccf-125">Quando os usuários fazem logon em seus computadores, o MBAM solicita que forneçam um PIN ou um PIN e uma senha que eles usarão quando reinicializarem o computador mais tarde.</span><span class="sxs-lookup"><span data-stu-id="33ccf-125">When users log on their computers, MBAM prompts them to provide a PIN or a PIN and a password that they will use when they restart their computer later.</span></span>

<span data-ttu-id="33ccf-126">**Observação**  A opção de protetor TPM exige que o administrador aceite o prompt do BIOS para ativar e inicializar o TPM antes de entregar o computador ao usuário.</span><span class="sxs-lookup"><span data-stu-id="33ccf-126">**Note** The TPM protector option requires for the administrator to accept the BIOS prompt to activate and initialize the TPM before delivering the computer to the user.</span></span>

 

## <span data-ttu-id="33ccf-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="33ccf-127">Related topics</span></span>


[<span data-ttu-id="33ccf-128">Planejar a implantação do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="33ccf-128">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="33ccf-129">Implantando o Cliente do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="33ccf-129">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)

 

 





