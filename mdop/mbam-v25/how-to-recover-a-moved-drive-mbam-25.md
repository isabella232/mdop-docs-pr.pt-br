---
title: Como recuperar uma unidade movida
description: Como recuperar uma unidade movida
author: dansimp
ms.assetid: 0d38ce7e-bc64-473e-ae85-99b7099ca758
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 9e7e03846e0a94902b699377043237c651939a07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799253"
---
# <span data-ttu-id="67431-103">Como recuperar uma unidade movida</span><span class="sxs-lookup"><span data-stu-id="67431-103">How to Recover a Moved Drive</span></span>
<span data-ttu-id="67431-104">Este tópico explica como usar o site de administração e monitoramento (também chamado de suporte técnico) para recuperar uma unidade do sistema operacional que foi movida após ser criptografada pelo Microsoft BitLocker Administration and Monitoring (MBAM).</span><span class="sxs-lookup"><span data-stu-id="67431-104">This topic explains how to use the Administration and Monitoring Website (also referred to as the Help Desk) to recover an operating system drive that was moved after being encrypted by Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="67431-105">Quando uma unidade é movida, ela não aceita mais o PIN usado no computador anterior porque o chip TPM (Trusted Platform Module) foi alterado.</span><span class="sxs-lookup"><span data-stu-id="67431-105">When a drive is moved, it no longer accepts the PIN that was used in the previous computer because the Trusted Platform Module (TPM) chip has changed.</span></span> <span data-ttu-id="67431-106">Para recuperar a unidade movida, você deve obter a ID da chave de recuperação para recuperar a senha de recuperação.</span><span class="sxs-lookup"><span data-stu-id="67431-106">To recover the moved drive, you must obtain the recovery key ID to retrieve the recovery password.</span></span>

<span data-ttu-id="67431-107">Para recuperar uma unidade movida, você deve usar a área de **recuperação de unidade** do site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="67431-107">To recover a moved drive, you must use the **Drive Recovery** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="67431-108">Para acessar a área de **recuperação da unidade** , você deve ser atribuído à função usuários da assistência técnica do MBAM ou à função usuários avançados da assistência técnica do MBAM.</span><span class="sxs-lookup"><span data-stu-id="67431-108">To access the **Drive Recovery** area, you must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role.</span></span> <span data-ttu-id="67431-109">Para obter mais informações sobre essas funções, confira [planejamento para contas e grupos do MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="67431-109">For more information about these roles, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>

**<span data-ttu-id="67431-110">Para recuperar uma unidade movida</span><span class="sxs-lookup"><span data-stu-id="67431-110">To recover a moved drive</span></span>**
1.  <span data-ttu-id="67431-111">No computador que contém a unidade movida, inicie o computador no modo de ambiente de recuperação do Windows (WinRE) ou inicie o computador usando o conjunto de ferramentas de diagnóstico e recuperação (DaRT) da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="67431-111">On the computer that contains the moved drive, start the computer in Windows Recovery Environment (WinRE) mode, or start the computer by using the Microsoft Diagnostic and Recovery Toolset (DaRT).</span></span>

2.  <span data-ttu-id="67431-112">Depois que o computador for iniciado com o WinRE ou o DaRT, o MBAM tratará a unidade do sistema operacional movida como uma unidade de dados fixa.</span><span class="sxs-lookup"><span data-stu-id="67431-112">After the computer has been started with WinRE or DaRT, MBAM will treat the moved operating system drive as a fixed data drive.</span></span> <span data-ttu-id="67431-113">O MBAM exibirá a identificação da senha de recuperação da unidade e solicitará a senha de recuperação.</span><span class="sxs-lookup"><span data-stu-id="67431-113">MBAM will then display the drive’s recovery password ID and ask for the recovery password.</span></span>

    <span data-ttu-id="67431-114">**Observação**  Em alguns casos, você poderá clicar em **esqueci o PIN** durante o processo de inicialização e, em seguida, inserir o modo de recuperação para exibir a ID da chave de recuperação.</span><span class="sxs-lookup"><span data-stu-id="67431-114">**Note** In some cases, you may be able to click **I forgot the PIN** during the startup process, and then enter the recovery mode to display the recovery key ID.</span></span>

     

3.  <span data-ttu-id="67431-115">Use a ID da chave de recuperação para recuperar a senha de recuperação e desbloquear a unidade no site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="67431-115">Use the recovery key ID to retrieve the recovery password and unlock the drive from the Administration and Monitoring Website.</span></span> <span data-ttu-id="67431-116">Para obter instruções, consulte [como recuperar uma unidade no modo de recuperação](how-to-recover-a-drive-in-recovery-mode-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="67431-116">For instructions, see [How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-25.md).</span></span>

    <span data-ttu-id="67431-117">Se a unidade movida tiver sido configurada para usar um chip TPM no computador original, conclua as etapas adicionais a seguir.</span><span class="sxs-lookup"><span data-stu-id="67431-117">If the moved drive was configured to use a TPM chip on the original computer, complete the following additional steps.</span></span> <span data-ttu-id="67431-118">Caso contrário, o processo de recuperação é concluído.</span><span class="sxs-lookup"><span data-stu-id="67431-118">Otherwise, the recovery process is complete.</span></span>

4.  <span data-ttu-id="67431-119">Após desbloquear a unidade e concluir o processo de inicialização, abra um prompt de comando no modo WinRE e use o `manage-bde` comando para descriptografar a unidade.</span><span class="sxs-lookup"><span data-stu-id="67431-119">After unlocking the drive and completing the start process, open a command prompt in WinRE mode and use the `manage-bde` command to decrypt the drive.</span></span> <span data-ttu-id="67431-120">Usar essa ferramenta é a única maneira de remover o TPM mais o protetor de PIN sem o chip TPM original.</span><span class="sxs-lookup"><span data-stu-id="67431-120">Using this tool is the only way to remove the TPM plus the PIN protector without the original TPM chip.</span></span> <span data-ttu-id="67431-121">Para obter informações sobre o `manage-bde` comando, consulte [Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567).</span><span class="sxs-lookup"><span data-stu-id="67431-121">For information about the `manage-bde` command, see [Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567).</span></span>

5.  <span data-ttu-id="67431-122">Quando a remoção for concluída, inicie o computador normalmente.</span><span class="sxs-lookup"><span data-stu-id="67431-122">When the removal is completed, start the computer normally.</span></span> <span data-ttu-id="67431-123">O agente MBAM irá impor a política para criptografar a unidade com o TPM do novo computador mais o PIN.</span><span class="sxs-lookup"><span data-stu-id="67431-123">The MBAM agent will now enforce the policy to encrypt the drive with the new computer’s TPM plus the PIN.</span></span>



## <span data-ttu-id="67431-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="67431-124">Related topics</span></span>


[<span data-ttu-id="67431-125">Realizando o gerenciamento do BitLocker com o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="67431-125">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 

## <span data-ttu-id="67431-126">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="67431-126">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="67431-127">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="67431-127">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="67431-128">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="67431-128">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





