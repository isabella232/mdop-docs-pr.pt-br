---
title: Realizar o Gerenciamento do BitLocker com o MBAM
description: Realizar o Gerenciamento do BitLocker com o MBAM
author: dansimp
ms.assetid: 2d24390a-87bf-48b3-96a9-3882d6f2a15c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d0de3711d5b7c3696783a054ee7c7f8220b5356
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799763"
---
# <span data-ttu-id="60568-103">Realizar o Gerenciamento do BitLocker com o MBAM</span><span class="sxs-lookup"><span data-stu-id="60568-103">Performing BitLocker Management with MBAM</span></span>


<span data-ttu-id="60568-104">Depois de implantar o Microsoft BitLocker Administration and Monitoring (MBAM), você pode configurar e usar o MBAM para gerenciar a criptografia do BitLocker corporativo.</span><span class="sxs-lookup"><span data-stu-id="60568-104">After you deploy Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use MBAM to manage enterprise BitLocker encryption.</span></span> <span data-ttu-id="60568-105">Esta seção descreve as tarefas de gerenciamento de criptografia do BitLocker do dia a dia após a instalação que podem ser realizadas usando o MBAM.</span><span class="sxs-lookup"><span data-stu-id="60568-105">This section describes post-installation, day-to-day BitLocker encryption management tasks that can be accomplished by using MBAM.</span></span>

## <span data-ttu-id="60568-106">Redefinir um bloqueio de TPM com MBAM</span><span class="sxs-lookup"><span data-stu-id="60568-106">Reset a TPM Lockout with MBAM</span></span>


<span data-ttu-id="60568-107">Um microchip do Trusted Platform Module (TPM) fornece funções básicas relacionadas à segurança.</span><span class="sxs-lookup"><span data-stu-id="60568-107">A Trusted Platform Module (TPM) microchip provides basic security-related functions.</span></span> <span data-ttu-id="60568-108">Essas funções são executadas principalmente pelo uso de chaves de criptografia.</span><span class="sxs-lookup"><span data-stu-id="60568-108">These functions are accomplished primarily by the use of encryption keys.</span></span> <span data-ttu-id="60568-109">O TPM geralmente é instalado na placa-mãe de um computador ou laptop e se comunica com o restante do sistema usando um barramento de hardware.</span><span class="sxs-lookup"><span data-stu-id="60568-109">The TPM is typically installed on the motherboard of a computer or laptop and communicates with the rest of the system by using a hardware bus.</span></span> <span data-ttu-id="60568-110">Os computadores que incorporam um TPM podem criar chaves criptográficas que podem ser descriptografadas apenas pelo TPM.</span><span class="sxs-lookup"><span data-stu-id="60568-110">Computers that incorporate a TPM can create cryptographic keys that can be decrypted only by the TPM.</span></span> <span data-ttu-id="60568-111">Um bloqueio de TPM pode ocorrer se um usuário inserir um PIN incorreto muitas vezes.</span><span class="sxs-lookup"><span data-stu-id="60568-111">A TPM lockout can occur if a user enters an incorrect PIN too many times.</span></span> <span data-ttu-id="60568-112">O número de vezes que um usuário pode inserir um PIN incorreto antes que os bloqueios do TPM variem do fabricante para o fabricante.</span><span class="sxs-lookup"><span data-stu-id="60568-112">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span> <span data-ttu-id="60568-113">O sistema de dados de recuperação de chave no site de administração do MBAM permite que você obtenha um arquivo Redefinir senha de proprietário do TPM.</span><span class="sxs-lookup"><span data-stu-id="60568-113">The Key Recovery data system on the MBAM administration website enables you to obtain a reset TPM owner password file.</span></span>

[<span data-ttu-id="60568-114">Como redefinir um bloqueio de TPM</span><span class="sxs-lookup"><span data-stu-id="60568-114">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-1.md)

## <span data-ttu-id="60568-115">Recuperar unidades com o MBAM</span><span class="sxs-lookup"><span data-stu-id="60568-115">Recover drives with MBAM</span></span>


<span data-ttu-id="60568-116">Verifique se você sabe como tentar a recuperação de dados de unidades criptografadas em caso de falha de hardware, alterações de pessoal ou outras situações em que as chaves de criptografia são perdidas.</span><span class="sxs-lookup"><span data-stu-id="60568-116">Make sure that you know how to attempt data recovery from encrypted drives in the event of hardware failure, changes in personnel, or other situations in which encryption keys are lost.</span></span> <span data-ttu-id="60568-117">Os recursos de recuperação de unidade criptografada do MBAM fornecem a captura e o armazenamento de dados e a disponibilidade de ferramentas necessárias para acessar um volume protegido pelo BitLocker quando o volume entra no modo de recuperação, é movido ou é corrompido.</span><span class="sxs-lookup"><span data-stu-id="60568-117">The Encrypted Drive Recovery features of MBAM provide the capture and storage of data and availability of tools required to access a BitLocker-protected volume when the volume goes into recovery mode, is moved, or becomes corrupted.</span></span>

[<span data-ttu-id="60568-118">Como recuperar uma unidade no modo de recuperação</span><span class="sxs-lookup"><span data-stu-id="60568-118">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-1.md)

[<span data-ttu-id="60568-119">Como recuperar uma unidade movida</span><span class="sxs-lookup"><span data-stu-id="60568-119">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-1.md)

[<span data-ttu-id="60568-120">Como recuperar uma unidade corrompida</span><span class="sxs-lookup"><span data-stu-id="60568-120">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-1.md)

## <span data-ttu-id="60568-121">Determinar o estado de criptografia do BitLocker dos computadores perdidos usando MBAM</span><span class="sxs-lookup"><span data-stu-id="60568-121">Determine BitLocker Encryption State of lost computers by Using MBAM</span></span>


<span data-ttu-id="60568-122">Ao usar o MBAM, você pode determinar o último status de criptografia do BitLocker conhecido de computadores que foram perdidos ou roubados.</span><span class="sxs-lookup"><span data-stu-id="60568-122">When you use MBAM, you can determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span>

[<span data-ttu-id="60568-123">Como determinar o estado de criptografia BitLocker de computadores perdidos</span><span class="sxs-lookup"><span data-stu-id="60568-123">How to Determine the BitLocker Encryption State of a Lost Computers</span></span>](how-to-determine-the-bitlocker-encryption-state-of-a-lost-computers-mbam-1.md)

## <span data-ttu-id="60568-124">Outros recursos para executar o gerenciamento do BitLocker com o MBAM</span><span class="sxs-lookup"><span data-stu-id="60568-124">Other resources for performing BitLocker Management with MBAM</span></span>


[<span data-ttu-id="60568-125">Operações do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="60568-125">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





