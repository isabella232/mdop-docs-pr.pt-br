---
title: Planejar implantação de cliente MBAM 2.0
description: Planejar implantação de cliente MBAM 2.0
author: dansimp
ms.assetid: 3a92cf29-092f-4cad-bdfa-d5f6aafe554b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c3a7383188d4064247d8e493c8e6125fc24a1d2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796045"
---
# <span data-ttu-id="6508d-103">Planejar implantação de cliente MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="6508d-103">Planning for MBAM 2.0 Client Deployment</span></span>


<span data-ttu-id="6508d-104">Dependendo de quando você implantar o cliente Microsoft BitLocker Administration and Monitoring (MBAM), você pode habilitar a criptografia de unidade de disco BitLocker em um computador em sua organização antes de o usuário final receber o computador ou mais tarde.</span><span class="sxs-lookup"><span data-stu-id="6508d-104">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client, you can enable BitLocker drive encryption on a computer in your organization either before the end user receives the computer or afterwards.</span></span> <span data-ttu-id="6508d-105">Para as topologias autônomas do MBAM e do Configuration Manager, você precisa definir configurações de política de grupo para MBAM.</span><span class="sxs-lookup"><span data-stu-id="6508d-105">For both the MBAM Stand-alone and the Configuration Manager topologies, you have to configure Group Policy settings for MBAM.</span></span>

<span data-ttu-id="6508d-106">Se você estiver usando a topologia autônoma do MBAM, é recomendável usar um sistema de implantação de software corporativo para implantar o software cliente do MBAM em computadores de usuário final.</span><span class="sxs-lookup"><span data-stu-id="6508d-106">If you are using the MBAM Stand-alone topology, it is recommended that you use an enterprise software deployment system to deploy the MBAM Client software to end-user computers.</span></span>

<span data-ttu-id="6508d-107">Se você implantar o MBAM com a topologia do Configuration Manager, poderá usar o Configuration Manager para implantar o software cliente do MBAM em computadores de usuário final.</span><span class="sxs-lookup"><span data-stu-id="6508d-107">If you deploy MBAM with the Configuration Manager topology, you can use Configuration Manager to deploy the MBAM Client software to end-user computers.</span></span> <span data-ttu-id="6508d-108">No Configuration Manager, a instalação do MBAM cria um conjunto de computadores que MBAM pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="6508d-108">In Configuration Manager, the MBAM installation creates a collection of computers that MBAM can manage.</span></span> <span data-ttu-id="6508d-109">Esta coleção inclui estações de trabalho e dispositivos que não têm um Trusted Platform Module (TPM), mas que executam o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6508d-109">This collection includes workstations and devices that do not have a Trusted Platform Module (TPM), but that are running Windows 8.</span></span>

<span data-ttu-id="6508d-110">**Observação**  Não há suporte para o Windows to go para instalações do Gerenciador de configurações integradas do MBAM se você estiver usando o Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="6508d-110">**Note** Windows To Go is not supported for integrated Configuration Manager installations of MBAM if you are using Configuration Manager 2007.</span></span>

 

## <span data-ttu-id="6508d-111">Implantando o cliente do MBAM para habilitar a criptografia do BitLocker após a distribuição do computador para usuários finais</span><span class="sxs-lookup"><span data-stu-id="6508d-111">Deploying the MBAM Client to Enable BitLocker Encryption After Computer Distribution to End Users</span></span>


<span data-ttu-id="6508d-112">Depois de configurar a política de grupo, você pode usar um produto do sistema de implantação de software corporativo, como o Microsoft System Center Configuration Manager ou os serviços de domínio Active Directory (AD DS), para implantar os arquivos do Windows Installer da instalação do cliente do MBAM em computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="6508d-112">After you configure Group Policy, you can use an enterprise software deployment system product like Microsoft System Center Configuration Manager or Active Directory Domain Services (AD DS) to deploy the Windows Installer files of the MBAM Client installation to target computers.</span></span> <span data-ttu-id="6508d-113">Para implantar o cliente do MBAM, você pode usar os arquivos 32 de MbamClientSetup.exe bits ou 64 bits ou arquivos MBAMClient.msi, que são fornecidos com o software do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6508d-113">To deploy the MBAM Client, you can use either the 32-bit or 64-bit MbamClientSetup.exe files or MBAMClient.msi files, which are provided with the MBAM software.</span></span>

<span data-ttu-id="6508d-114">Quando você implanta o cliente MBAM após distribuir computadores para computadores cliente, os usuários finais são solicitados a criptografar o computador.</span><span class="sxs-lookup"><span data-stu-id="6508d-114">When you deploy the MBAM Client after you distribute computers to client computers, end users are prompted to encrypt their computer.</span></span> <span data-ttu-id="6508d-115">Isso permite que o MBAM colete os dados, que incluem o PIN e a senha, e, em seguida, iniciar o processo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="6508d-115">This enables MBAM to collect the data, which includes the PIN and password, and then to begin the encryption process.</span></span>

<span data-ttu-id="6508d-116">**Observação**  Nessa abordagem, os usuários que tiverem computadores com um chip TPM serão solicitados a ativar e inicializar o chip TPM se o chip não tiver sido ativado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6508d-116">**Note** In this approach, users who have computers with a TPM chip are prompted to activate and initialize the TPM chip if the chip has not been previously activated.</span></span>

 

## <span data-ttu-id="6508d-117">Usando o cliente MBAM para habilitar a criptografia do BitLocker antes da distribuição do computador para usuários finais</span><span class="sxs-lookup"><span data-stu-id="6508d-117">Using the MBAM Client to Enable BitLocker Encryption Before Computer Distribution to End Users</span></span>


<span data-ttu-id="6508d-118">Nas organizações em que os computadores são recebidos e configurados de forma centralizada, e onde os computadores têm um chip TPM compatível, você pode instalar o cliente MBAM para gerenciar a criptografia do BitLocker em cada computador antes que os dados do usuário sejam gravados nele.</span><span class="sxs-lookup"><span data-stu-id="6508d-118">In organizations where computers are received and configured centrally, and where computers have a compliant TPM chip, you can install the MBAM Client to manage BitLocker encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="6508d-119">A vantagem desse processo é que cada computador será compatível com a criptografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6508d-119">The benefit of this process is that every computer will then be BitLocker encryption-compliant.</span></span> <span data-ttu-id="6508d-120">Esse método não depende da ação do usuário porque o administrador já criptografou o computador.</span><span class="sxs-lookup"><span data-stu-id="6508d-120">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="6508d-121">Uma pressuposição chave para esse cenário é que a política da organização instala uma imagem corporativa do Windows antes que o computador seja entregue ao usuário.</span><span class="sxs-lookup"><span data-stu-id="6508d-121">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span>

<span data-ttu-id="6508d-122">Se a sua organização quiser usar o chip TPM para criptografar computadores, o administrador adicionará o protetor TPM para criptografar o volume do sistema operacional do computador.</span><span class="sxs-lookup"><span data-stu-id="6508d-122">If your organization wants to use the TPM chip to encrypt computers, the administrator adds the TPM protector to encrypt the operating system volume of the computer.</span></span> <span data-ttu-id="6508d-123">Se a sua organização quiser usar o chip TPM e um protetor de PIN, o administrador criptografará o volume do sistema operacional com o protetor TPM e os usuários selecionarão um PIN quando fizerem logon pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="6508d-123">If your organization wants to use the TPM chip and a PIN protector, the administrator encrypts the operating system volume with the TPM protector, and then users select a PIN when they log on for the first time.</span></span> <span data-ttu-id="6508d-124">Se a sua organização decidir usar apenas o protetor de PIN, o administrador não precisará criptografar o volume primeiro.</span><span class="sxs-lookup"><span data-stu-id="6508d-124">If your organization decides to use only the PIN protector, the administrator does not have to encrypt the volume first.</span></span> <span data-ttu-id="6508d-125">Quando os usuários fazem logon, o monitoramento e a administração do Microsoft BitLocker pedem que eles forneçam um PIN, ou um PIN e uma senha a serem usados em reinícios posteriores do computador.</span><span class="sxs-lookup"><span data-stu-id="6508d-125">When users log on, Microsoft BitLocker Administration and Monitoring prompts them to provide a PIN, or a PIN and password to be used on later computer restarts.</span></span>

<span data-ttu-id="6508d-126">**Observação**  A opção de protetor TPM exige que o administrador aceite o prompt do BIOS para ativar e inicializar o TPM antes que o computador seja entregue ao usuário.</span><span class="sxs-lookup"><span data-stu-id="6508d-126">**Note** The TPM protector option requires the administrator to accept the BIOS prompt to activate and initialize the TPM before the computer is delivered to the user.</span></span>

 

## <span data-ttu-id="6508d-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6508d-127">Related topics</span></span>


[<span data-ttu-id="6508d-128">Planejar a implantação do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="6508d-128">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="6508d-129">Implantando o Cliente do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="6508d-129">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)

 

 





