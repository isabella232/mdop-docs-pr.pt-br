---
title: Planejando a implantação do cliente do MBAM 2.5
description: Planejando a implantação do cliente do MBAM 2.5
author: dansimp
ms.assetid: 23c89976-af24-4753-9412-ce0ea42d1964
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ff03b58da0985b2f57308c99a9bc15f4a0554623
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799783"
---
# <span data-ttu-id="6eeb2-103">Planejando a implantação do cliente do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="6eeb2-103">Planning for MBAM 2.5 Client Deployment</span></span>


<span data-ttu-id="6eeb2-104">Dependendo de quando você implantar o software cliente do Microsoft BitLocker Administration and Monitoring (MBAM), você pode habilitar a criptografia de unidade de disco BitLocker em um computador em sua organização antes de o usuário final receber o computador ou mais tarde.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-104">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client software, you can enable BitLocker Drive Encryption on a computer in your organization either before the end user receives the computer or afterwards.</span></span> <span data-ttu-id="6eeb2-105">Para as topologias de integração do MBAM autônomo e do System Center Configuration Manager, você precisa definir configurações de política de grupo para MBAM.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-105">For both the MBAM Stand-alone and the System Center Configuration Manager Integration topologies, you have to configure Group Policy settings for MBAM.</span></span>

<span data-ttu-id="6eeb2-106">Se você estiver usando a topologia autônoma do MBAM, recomendamos que use um sistema de implantação de software corporativo para implantar o software cliente do MBAM em computadores de usuário final.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-106">If you are using the MBAM Stand-alone topology, we recommend that you use an enterprise software deployment system to deploy the MBAM Client software to end-user computers.</span></span>

<span data-ttu-id="6eeb2-107">Se você implantar o MBAM com a topologia de integração do Configuration Manager, poderá usar o Configuration Manager para implantar o software cliente do MBAM em computadores de usuário final.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-107">If you deploy MBAM with the Configuration Manager Integration topology, you can use Configuration Manager to deploy the MBAM Client software to end-user computers.</span></span> <span data-ttu-id="6eeb2-108">No Configuration Manager, a instalação do MBAM cria um conjunto de computadores que MBAM pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-108">In Configuration Manager, the MBAM installation creates a collection of computers that MBAM can manage.</span></span> <span data-ttu-id="6eeb2-109">Esta coleção inclui estações de trabalho e dispositivos que não têm um Trusted Platform Module (TPM), mas que estão executando o Windows 8, o Windows 8,1 ou o Windows 10.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-109">This collection includes workstations and devices that do not have a Trusted Platform Module (TPM), but that are running Windows 8, Windows 8.1, or Windows 10.</span></span>

<span data-ttu-id="6eeb2-110">**Observação**  Não há suporte para o Windows to go para a instalação de topologia de integração do Configuration Manager quando você está usando o Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-110">**Note** Windows To Go is not supported for the Configuration Manager Integration topology installation when you are using Configuration Manager 2007.</span></span>

 

## <span data-ttu-id="6eeb2-111">Implantando o cliente MBAM para habilitar a criptografia de unidade de disco BitLocker após a distribuição de computador para usuários finais</span><span class="sxs-lookup"><span data-stu-id="6eeb2-111">Deploying the MBAM Client to enable BitLocker Drive Encryption after computer distribution to end users</span></span>


<span data-ttu-id="6eeb2-112">Depois de configurar a política de grupo, você pode usar um produto do sistema de implantação de software corporativo, como o Microsoft System Center Configuration Manager ou os serviços de domínio Active Directory (AD DS), para implantar os arquivos do Windows Installer da instalação do cliente do MBAM em computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-112">After you configure Group Policy, you can use an enterprise software deployment system product like Microsoft System Center Configuration Manager or Active Directory Domain Services (AD DS) to deploy the Windows Installer files of the MBAM Client installation to target computers.</span></span> <span data-ttu-id="6eeb2-113">Para implantar o cliente do MBAM, você pode usar os arquivos 32 de MbamClientSetup.exe bits ou 64 bits ou arquivos MBAMClient.msi, que são fornecidos com o software cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-113">To deploy the MBAM Client, you can use either the 32-bit or 64-bit MbamClientSetup.exe files or MBAMClient.msi files, which are provided with the MBAM Client software.</span></span>

<span data-ttu-id="6eeb2-114">**Observação**  A partir do MBAM 2,5 SP1, um MSI separado não está mais incluído no produto MBAM.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-114">**Note** Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="6eeb2-115">No entanto, você pode extrair o MSI do arquivo executável (. exe) que está incluído no produto.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-115">However, you can extract the MSI from the executable file (.exe) that is included with the product.</span></span>

 

<span data-ttu-id="6eeb2-116">Quando você implanta o cliente MBAM após distribuir computadores para computadores cliente, os usuários finais são solicitados a criptografar o computador.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-116">When you deploy the MBAM Client after you distribute computers to client computers, end users are prompted to encrypt their computer.</span></span> <span data-ttu-id="6eeb2-117">Essa ação permite que o MBAM colete os dados, que inclui o PIN e a senha (se necessário pela política) e, em seguida, iniciar o processo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-117">This action enables MBAM to collect the data, which includes the PIN and password (if required by policy), and then to begin the encryption process.</span></span>

<span data-ttu-id="6eeb2-118">**Observação**  Nessa abordagem, os usuários finais que tiverem computadores com um chip TPM serão solicitados a ativar e inicializar o chip TPM se o chip não tiver sido ativado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-118">**Note** In this approach, end users who have computers with a TPM chip are prompted to activate and initialize the TPM chip if the chip has not been previously activated.</span></span>

 

## <span data-ttu-id="6eeb2-119">Usando o cliente MBAM para habilitar a criptografia de unidade de disco BitLocker antes da distribuição de computador para usuários finais</span><span class="sxs-lookup"><span data-stu-id="6eeb2-119">Using the MBAM Client to enable BitLocker Drive Encryption before computer distribution to end users</span></span>


<span data-ttu-id="6eeb2-120">Nas organizações em que os computadores são recebidos e configurados de forma centralizada, e onde os computadores têm um chip TPM compatível, você pode usar o cliente MBAM para gerenciar a criptografia de unidade de disco BitLocker em cada computador antes que os dados do usuário sejam gravados nele.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-120">In organizations where computers are received and configured centrally, and where computers have a compliant TPM chip, you can use the MBAM Client to manage BitLocker Drive Encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="6eeb2-121">A vantagem desse processo é que todos os computadores são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-121">The benefit of this process is that every computer is then compliant.</span></span> <span data-ttu-id="6eeb2-122">Esse método não depende da ação do usuário final porque o administrador já criptografou o computador.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-122">This method does not rely on end-user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="6eeb2-123">Uma pressuposição chave para esse cenário é que a política da organização instala uma imagem corporativa do Windows antes que o computador seja entregue ao usuário final.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-123">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the end user.</span></span>

<span data-ttu-id="6eeb2-124">Se a sua organização quiser usar o chip TPM para criptografar computadores, o administrador adicionará o protetor TPM para criptografar o volume do sistema operacional do computador.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-124">If your organization wants to use the TPM chip to encrypt computers, the administrator adds the TPM protector to encrypt the operating system volume of the computer.</span></span> <span data-ttu-id="6eeb2-125">Se a sua organização quiser usar o chip TPM e um protetor de PIN, o administrador criptografará o volume do sistema operacional com o protetor TPM e, em seguida, os usuários finais selecionarão um PIN quando fizerem logon pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-125">If your organization wants to use the TPM chip and a PIN protector, the administrator encrypts the operating system volume with the TPM protector, and then end users select a PIN when they log on for the first time.</span></span> <span data-ttu-id="6eeb2-126">Se a sua organização decidir usar apenas o protetor de PIN, o administrador não precisará criptografar o volume primeiro.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-126">If your organization decides to use only the PIN protector, the administrator does not have to encrypt the volume first.</span></span> <span data-ttu-id="6eeb2-127">Quando os usuários finais se conectam, o monitoramento e a administração do Microsoft BitLocker pedem que eles forneçam um PIN, ou um PIN e uma senha a serem usados em reinícios posteriores do computador.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-127">When end users log on, Microsoft BitLocker Administration and Monitoring prompts them to provide a PIN, or a PIN and password to be used on later computer restarts.</span></span>

<span data-ttu-id="6eeb2-128">**Observação**  A opção de protetor TPM exige que o administrador aceite o prompt do BIOS para ativar e inicializar o TPM antes que o computador seja entregue ao usuário final.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-128">**Note** The TPM protector option requires the administrator to accept the BIOS prompt to activate and initialize the TPM before the computer is delivered to the end user.</span></span>

 

## <span data-ttu-id="6eeb2-129">Suporte do cliente MBAM para discos rígidos criptografados</span><span class="sxs-lookup"><span data-stu-id="6eeb2-129">MBAM Client support for Encrypted Hard Drives</span></span>


<span data-ttu-id="6eeb2-130">O MBAM dá suporte ao BitLocker em discos rígidos criptografados que atendem aos requisitos de especificação do TCG para o Opal e com os padrões IEEE 1667.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-130">MBAM supports BitLocker on Encrypted Hard Drives that meet TCG specification requirements for Opal as well as IEEE 1667 standards.</span></span> <span data-ttu-id="6eeb2-131">Quando o BitLocker estiver habilitado nesses dispositivos, ele irá gerar chaves e executar funções de gerenciamento na unidade criptografada.</span><span class="sxs-lookup"><span data-stu-id="6eeb2-131">When BitLocker is enabled on these devices, it will generate keys and perform management functions on the encrypted drive.</span></span> <span data-ttu-id="6eeb2-132">Para obter mais informações, consulte [unidade de disco rígido criptografado](https://technet.microsoft.com/library/hh831627.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6eeb2-132">See [Encrypted Hard Drive](https://technet.microsoft.com/library/hh831627.aspx) for more information.</span></span>


## <span data-ttu-id="6eeb2-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6eeb2-133">Related topics</span></span>


[<span data-ttu-id="6eeb2-134">Planejando a implantação do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="6eeb2-134">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="6eeb2-135">Implantando o cliente do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="6eeb2-135">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

 

 
## <span data-ttu-id="6eeb2-136">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="6eeb2-136">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="6eeb2-137">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="6eeb2-137">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="6eeb2-138">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="6eeb2-138">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




