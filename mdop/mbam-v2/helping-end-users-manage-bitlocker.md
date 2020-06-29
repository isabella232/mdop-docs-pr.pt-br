---
title: Ajudando os usuários finais a gerenciar o BitLocker
description: Ajudando os usuários finais a gerenciar o BitLocker
author: dansimp
ms.assetid: 47776fb3-2d94-4970-b687-c35ec3dd6c64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26ef2bc33a75ff7773b75807ab0e10e5aa67b109
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799540"
---
# <span data-ttu-id="d6dde-103">Ajudando os usuários finais a gerenciar o BitLocker</span><span class="sxs-lookup"><span data-stu-id="d6dde-103">Helping End Users Manage BitLocker</span></span>


<span data-ttu-id="d6dde-104">O conteúdo em um computador perdido ou roubado é vulnerável a acesso não autorizado, que pode representar um risco de segurança para pessoas e empresas.</span><span class="sxs-lookup"><span data-stu-id="d6dde-104">Content on a lost or stolen computer is vulnerable to unauthorized access, which can present a security risk to both people and companies.</span></span> <span data-ttu-id="d6dde-105">O monitoramento e administração do Microsoft BitLocker (MBAM) usa o BitLocker para ajudar a evitar o acesso não autorizado, bloqueando o computador para ajudar a proteger dados confidenciais de usuários mal-intencionados.</span><span class="sxs-lookup"><span data-stu-id="d6dde-105">Microsoft BitLocker Administration and Monitoring (MBAM) uses BitLocker to help prevent unauthorized access by locking your computer to help protect sensitive data from malicious users.</span></span>

## <span data-ttu-id="d6dde-106">O que é BitLocker?</span><span class="sxs-lookup"><span data-stu-id="d6dde-106">What is BitLocker?</span></span>


<span data-ttu-id="d6dde-107">A criptografia de unidade de disco BitLocker pode oferecer proteção para unidades de sistema operacionais, unidades de dados e unidades removíveis (como uma unidade USB Thumb) criptografando as unidades.</span><span class="sxs-lookup"><span data-stu-id="d6dde-107">BitLocker Drive Encryption can provide protection for operating system drives, data drives, and removable drives (such as a USB thumb drive) by encrypting the drives.</span></span> <span data-ttu-id="d6dde-108">Dependendo de como o BitLocker estiver configurado, os usuários podem precisar fornecer uma chave (uma senha ou PIN) para desbloquear as informações armazenadas nas unidades criptografadas.</span><span class="sxs-lookup"><span data-stu-id="d6dde-108">Depending on how BitLocker is configured, users may have to provide a key (a password or PIN) to unlock the information that is stored on the encrypted drives.</span></span>

<span data-ttu-id="d6dde-109">Quando você adiciona novos arquivos a uma unidade criptografada com o BitLocker, o BitLocker os criptografa automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d6dde-109">When you add new files to a drive that is encrypted with BitLocker, BitLocker encrypts them automatically.</span></span> <span data-ttu-id="d6dde-110">Os arquivos permanecem criptografados somente enquanto são armazenados na unidade criptografada.</span><span class="sxs-lookup"><span data-stu-id="d6dde-110">Files remain encrypted only while they are stored in the encrypted drive.</span></span> <span data-ttu-id="d6dde-111">Os arquivos copiados para outra unidade ou computador são descriptografados.</span><span class="sxs-lookup"><span data-stu-id="d6dde-111">Files that are copied to another drive or computer are decrypted.</span></span> <span data-ttu-id="d6dde-112">Se você compartilhar arquivos com outros usuários, por exemplo, por meio de uma rede, esses arquivos serão criptografados enquanto estiverem armazenados na unidade criptografada, mas poderão ser acessados normalmente por usuários autorizados.</span><span class="sxs-lookup"><span data-stu-id="d6dde-112">If you share files with other users, such as through a network, these files are encrypted while stored on the encrypted drive, but they can be accessed normally by authorized users.</span></span>

<span data-ttu-id="d6dde-113">Se você criptografar a unidade do sistema operacional, o BitLocker verifica o computador durante a inicialização em busca de condições que possam representar um risco de segurança (por exemplo, uma alteração no BIOS ou muda para qualquer arquivo de inicialização).</span><span class="sxs-lookup"><span data-stu-id="d6dde-113">If you encrypt the operating system drive, BitLocker checks the computer during startup for any conditions that could represent a security risk (for example, a change to the BIOS or changes to any startup files).</span></span> <span data-ttu-id="d6dde-114">Se um possível risco de segurança for detectado, o BitLocker bloqueará a unidade do sistema operacional e será necessária uma chave de recuperação do BitLocker especial para desbloqueá-la.</span><span class="sxs-lookup"><span data-stu-id="d6dde-114">If a potential security risk is detected, BitLocker will lock the operating system drive and require a special BitLocker recovery key to unlock it.</span></span> <span data-ttu-id="d6dde-115">Certifique-se de criar essa chave de recuperação ao ativar o BitLocker pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="d6dde-115">Make sure that you create this recovery key when you turn on BitLocker for the first time.</span></span> <span data-ttu-id="d6dde-116">Caso contrário, você pode perder permanentemente o acesso aos seus arquivos.</span><span class="sxs-lookup"><span data-stu-id="d6dde-116">Otherwise, you could permanently lose access to your files.</span></span>

<span data-ttu-id="d6dde-117">Se você criptografar unidades de dados (fixas ou removíveis), poderá desbloquear uma unidade criptografada com uma senha ou um cartão inteligente ou definir a unidade para desbloquear automaticamente quando você fizer logon no computador.</span><span class="sxs-lookup"><span data-stu-id="d6dde-117">If you encrypt data drives (fixed or removable), you can unlock an encrypted drive with a password or a smart card, or set the drive to automatically unlock when you log on to the computer.</span></span>

<span data-ttu-id="d6dde-118">Além de senhas e PINs, o BitLocker pode usar o chip Trusted Platform Module (TPM) fornecido em muitos computadores mais novos.</span><span class="sxs-lookup"><span data-stu-id="d6dde-118">In addition to passwords and PINs, BitLocker can use the Trusted Platform Module (TPM) chip that is provided in many newer computers.</span></span> <span data-ttu-id="d6dde-119">O chip TPM é usado para garantir que seu computador não tenha sido adulterado antes de o BitLocker desbloqueie a unidade do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d6dde-119">The TPM chip is used to ensure that your computer has not been tampered with before BitLocker will unlock the operating system drive.</span></span> <span data-ttu-id="d6dde-120">Durante o processo de criptografia, talvez seja necessário habilitar o chip TPM.</span><span class="sxs-lookup"><span data-stu-id="d6dde-120">During the encryption process, you may have to enable the TPM chip.</span></span> <span data-ttu-id="d6dde-121">Quando você inicia o computador, o BitLocker pede que o TPM entre as chaves para a unidade e a desbloqueie.</span><span class="sxs-lookup"><span data-stu-id="d6dde-121">When you start your computer, BitLocker asks the TPM for the keys to the drive and unlocks it.</span></span> <span data-ttu-id="d6dde-122">Para habilitar o chip TPM, será preciso reiniciar o computador e alterar uma configuração no BIOS, em uma camada anterior ao Windows do software do computador.</span><span class="sxs-lookup"><span data-stu-id="d6dde-122">To enable the TPM chip, you will have to restart your computer and then change a setting in the BIOS, a pre-Windows layer of your computer software.</span></span> <span data-ttu-id="d6dde-123">Para obter mais informações sobre o TPM, consulte [sobre o chip TPM do computador](about-the-computer-tpm-chip.md).</span><span class="sxs-lookup"><span data-stu-id="d6dde-123">For more information about the TPM, see [About the Computer TPM Chip](about-the-computer-tpm-chip.md).</span></span>

<span data-ttu-id="d6dde-124">Depois que seu computador estiver protegido pelo BitLocker, talvez seja necessário digitar um PIN ou uma senha sempre que o computador ativar ou iniciar a hibernação.</span><span class="sxs-lookup"><span data-stu-id="d6dde-124">Once your computer is protected by BitLocker, you may have to enter a PIN or password every time that the computer wakes from hibernation or starts.</span></span> <span data-ttu-id="d6dde-125">O suporte técnico para sua empresa ou organização pode ajudá-lo a se esquecer do seu PIN ou senha.</span><span class="sxs-lookup"><span data-stu-id="d6dde-125">The Help Desk for your company or organization can help if you ever forget your PIN or password.</span></span>

<span data-ttu-id="d6dde-126">Você pode desativar o BitLocker temporariamente, temporariamente, suspendendo-o, ou permanentemente, descriptografando a unidade.</span><span class="sxs-lookup"><span data-stu-id="d6dde-126">You can turn off BitLocker, either temporarily, by suspending it, or permanently, by decrypting the drive.</span></span>

<span data-ttu-id="d6dde-127">**Observação**  Como o BitLocker criptografa toda a unidade e não apenas os próprios arquivos individuais, tenha cuidado ao mover dados confidenciais entre unidades.</span><span class="sxs-lookup"><span data-stu-id="d6dde-127">**Note** Because BitLocker encrypts the whole drive and not just the individual files themselves, be careful when you move sensitive data between drives.</span></span> <span data-ttu-id="d6dde-128">Se você mover um arquivo de uma unidade de disco protegida pelo BitLocker para uma unidade não criptografada, o arquivo não será mais criptografado.</span><span class="sxs-lookup"><span data-stu-id="d6dde-128">If you move a file from a BitLocker-protected drive to a nonencrypted drive, the file will no longer be encrypted.</span></span>

 

## <span data-ttu-id="d6dde-129">Sobre o aplicativo opções de criptografia do BitLocker</span><span class="sxs-lookup"><span data-stu-id="d6dde-129">About the BitLocker Encryption Options Application</span></span>


<span data-ttu-id="d6dde-130">Para desbloquear as unidades de disco rígido do seu computador e gerenciar seu PIN e senhas, use o aplicativo opções de criptografia do BitLocker no painel de controle do Windows seguindo o procedimento descrito aqui.</span><span class="sxs-lookup"><span data-stu-id="d6dde-130">To unlock hard disk drives on your computer and to manage your PIN and passwords, use the BitLocker Encryption Options application in the Windows Control Panel by following the procedure outlined here.</span></span> <span data-ttu-id="d6dde-131">Você pode inserir senhas para desbloquear unidades protegidas e verificar o status do BitLocker das unidades conectadas usando este aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d6dde-131">You can enter passwords to unlock protected drives and can check the BitLocker status of attached drives by using this application.</span></span>

**<span data-ttu-id="d6dde-132">Para abrir o aplicativo opções de criptografia do BitLocker</span><span class="sxs-lookup"><span data-stu-id="d6dde-132">To open the BitLocker Encryption Options application</span></span>**

1.  <span data-ttu-id="d6dde-133">Clique em **Iniciar**e selecione **painel de controle**.</span><span class="sxs-lookup"><span data-stu-id="d6dde-133">Click **Start**, and select **Control Panel**.</span></span> <span data-ttu-id="d6dde-134">O painel de controle é aberto em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="d6dde-134">The Control Panel opens in a new window.</span></span>

2.  <span data-ttu-id="d6dde-135">No **painel de controle**, selecione **sistema e segurança**.</span><span class="sxs-lookup"><span data-stu-id="d6dde-135">In **Control Panel**, select **System and Security**.</span></span>

3.  <span data-ttu-id="d6dde-136">Selecione **Opções de criptografia do BitLocker** para abrir o aplicativo opções de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d6dde-136">Select **BitLocker Encryption Options** to open the BitLocker Encryption Options application.</span></span>

    <span data-ttu-id="d6dde-137">Para obter uma descrição das opções disponíveis, consulte a seção a seguir.</span><span class="sxs-lookup"><span data-stu-id="d6dde-137">For a description of the available options, see the following section.</span></span>

## <span data-ttu-id="d6dde-138">Opções no aplicativo opções de criptografia do BitLocker</span><span class="sxs-lookup"><span data-stu-id="d6dde-138">Options on the BitLocker Encryption Options Application</span></span>


<span data-ttu-id="d6dde-139">O aplicativo opções de criptografia do BitLocker no painel de controle permite que você gerencie seu PIN e senhas, que o BitLocker usa para proteger seu computador.</span><span class="sxs-lookup"><span data-stu-id="d6dde-139">The BitLocker Encryption Options application on Control Panel lets you manage your PIN and passwords, which BitLocker uses to protect your computer.</span></span>

**<span data-ttu-id="d6dde-140">Criptografia de unidade de disco BitLocker – drives de disco fixos:</span><span class="sxs-lookup"><span data-stu-id="d6dde-140">BitLocker Drive Encryption – Fixed Disk Drives:</span></span>**

<span data-ttu-id="d6dde-141">Nesta seção, você pode exibir informações sobre unidades de disco rígido conectadas ao seu computador e o status atual de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d6dde-141">In this section, you can view information about hard disk drives connected to your computer and their current BitLocker Encryption status.</span></span>

-   <span data-ttu-id="d6dde-142">**Gerenciar seu PIN** -altera o PIN usado pelo BitLocker para desbloquear a unidade do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d6dde-142">**Manage your PIN** - changes the PIN used by BitLocker to unlock your operating system drive.</span></span>

-   <span data-ttu-id="d6dde-143">**Gerenciar sua senha** – altera a senha que é usada pelo BitLocker para desbloquear suas outras unidades internas.</span><span class="sxs-lookup"><span data-stu-id="d6dde-143">**Manage your password** - changes the password that is used by BitLocker to unlock your other internal drives.</span></span>

**<span data-ttu-id="d6dde-144">Criptografia de unidade de disco BitLocker-unidades externas:</span><span class="sxs-lookup"><span data-stu-id="d6dde-144">BitLocker Drive Encryption - External Drives:</span></span>**

<span data-ttu-id="d6dde-145">Nesta seção, você pode exibir informações sobre unidades externas (como um pen drive) conectados ao seu computador e o status atual de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d6dde-145">In this section, you can view information about external drives (such as a USB thumb drive) connected to your computer, and their current BitLocker encryption status.</span></span>

-   <span data-ttu-id="d6dde-146">**Gerenciar sua senha** – altera a senha que é usada pelo BitLocker para desbloquear suas outras unidades internas.</span><span class="sxs-lookup"><span data-stu-id="d6dde-146">**Manage your password** - changes the password that is used by BitLocker to unlock your other internal drives.</span></span>

**<span data-ttu-id="d6dde-147">Antecipa</span><span class="sxs-lookup"><span data-stu-id="d6dde-147">Advanced:</span></span>**

-   <span data-ttu-id="d6dde-148">**Administração do TPM** -abre a ferramenta de administração do TPM em uma janela separada.</span><span class="sxs-lookup"><span data-stu-id="d6dde-148">**TPM Administration** - opens the TPM Administration tool in a separate window.</span></span> <span data-ttu-id="d6dde-149">Aqui você pode configurar tarefas comuns do TPM e obter informações sobre o chipset TPM.</span><span class="sxs-lookup"><span data-stu-id="d6dde-149">From here you can configure common TPM tasks and obtain information about the TPM chipset.</span></span> <span data-ttu-id="d6dde-150">Você deve ter permissões administrativas no seu computador para acessar essa ferramenta.</span><span class="sxs-lookup"><span data-stu-id="d6dde-150">You must have administrative permissions on your computer to access this tool.</span></span>

-   <span data-ttu-id="d6dde-151">**Gerenciamento de disco** : abrir a ferramenta de gerenciamento de disco.</span><span class="sxs-lookup"><span data-stu-id="d6dde-151">**Disk Management** -open the Disk Management tool.</span></span> <span data-ttu-id="d6dde-152">Aqui você pode ver as informações de todos os discos rígidos conectados ao computador e configurar partições e opções de unidade.</span><span class="sxs-lookup"><span data-stu-id="d6dde-152">From here you can view the information for all hard drives connected to the computer and configure partitions and drive options.</span></span> <span data-ttu-id="d6dde-153">Você deve ter direitos administrativos em seu computador para acessar essa ferramenta.</span><span class="sxs-lookup"><span data-stu-id="d6dde-153">You must have administrative rights on your computer to access this tool.</span></span>

 

 





