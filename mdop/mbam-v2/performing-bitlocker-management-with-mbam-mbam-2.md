---
title: Realizar o Gerenciamento do BitLocker com o MBAM
description: Realizar o Gerenciamento do BitLocker com o MBAM
author: dansimp
ms.assetid: 9bfc6c67-f12c-4daa-8f08-5884fb47443c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d261ec4fa789cd331209afe1c2f1858d627209a3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799884"
---
# <span data-ttu-id="d1de4-103">Realizar o Gerenciamento do BitLocker com o MBAM</span><span class="sxs-lookup"><span data-stu-id="d1de4-103">Performing BitLocker Management with MBAM</span></span>


<span data-ttu-id="d1de4-104">Depois de planejar e implantar o Microsoft BitLocker Administration and Monitoring (MBAM), você pode configurá-lo e usá-lo para gerenciar a criptografia do BitLocker corporativo.</span><span class="sxs-lookup"><span data-stu-id="d1de4-104">After planning and then deploying Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use it to manage enterprise BitLocker encryption.</span></span> <span data-ttu-id="d1de4-105">As informações nesta seção descrevem tarefas de gerenciamento de criptografia do BitLocker do dia a pós-instalação que são realizadas usando a administração e o monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d1de4-105">The information in this section describes post-installation day-to-day BitLocker encryption management tasks that are accomplished by using Microsoft BitLocker Administration and Monitoring.</span></span>

## <span data-ttu-id="d1de4-106">Redefinir um bloqueio de TPM usando MBAM</span><span class="sxs-lookup"><span data-stu-id="d1de4-106">Reset a TPM Lockout by Using MBAM</span></span>


<span data-ttu-id="d1de4-107">Um TPM (Trusted Platform Module) é um microchip projetado para fornecer funções básicas relacionadas à segurança, principalmente envolvendo chaves de criptografia.</span><span class="sxs-lookup"><span data-stu-id="d1de4-107">A Trusted Platform Module (TPM) is a microchip that is designed to provide basic security-related functions, primarily involving encryption keys.</span></span> <span data-ttu-id="d1de4-108">O TPM geralmente é instalado na placa-mãe de um computador ou laptop e comunica-se com o restante do sistema usando um barramento de hardware.</span><span class="sxs-lookup"><span data-stu-id="d1de4-108">The TPM is usually installed on the motherboard of a computer or laptop, and communicates with the rest of the system by using a hardware bus.</span></span> <span data-ttu-id="d1de4-109">Os computadores que incorporam um TPM têm a capacidade de criar chaves criptográficas e criptografá-las para que possam ser descriptografadas apenas pelo TPM.</span><span class="sxs-lookup"><span data-stu-id="d1de4-109">Computers that incorporate a TPM have the ability to create cryptographic keys and encrypt them so that they can be decrypted only by the TPM.</span></span>

<span data-ttu-id="d1de4-110">Um bloqueio de TPM pode ocorrer se um usuário inserir o PIN incorreto muitas vezes.</span><span class="sxs-lookup"><span data-stu-id="d1de4-110">A TPM lockout can occur if a user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="d1de4-111">O número de vezes que um usuário pode inserir um PIN incorreto antes que os bloqueios do TPM variem do fabricante para o fabricante.</span><span class="sxs-lookup"><span data-stu-id="d1de4-111">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span> <span data-ttu-id="d1de4-112">Você pode usar o MBAM para acessar o sistema de dados de recuperação de chave centralizada no site de administração e monitoramento, onde você pode recuperar um arquivo de senha de proprietário do TPM quando fornecer uma ID de computador e um identificador de usuário associado.</span><span class="sxs-lookup"><span data-stu-id="d1de4-112">You can use MBAM to access the centralized Key Recovery data system in the Administration and Monitoring website, where you can retrieve a TPM owner password file when you supply a computer ID and associated user identifier.</span></span>

[<span data-ttu-id="d1de4-113">Como redefinir um bloqueio de TPM</span><span class="sxs-lookup"><span data-stu-id="d1de4-113">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-2.md)

## <span data-ttu-id="d1de4-114">Recuperar unidades com o MBAM</span><span class="sxs-lookup"><span data-stu-id="d1de4-114">Recover Drives with MBAM</span></span>


<span data-ttu-id="d1de4-115">Quando você estiver lidando com a criptografia de dados, especialmente em um ambiente corporativo, considere como esses dados podem ser recuperados em caso de falha de hardware, mudanças na equipe ou outras situações nas quais as chaves de criptografia podem ser perdidas.</span><span class="sxs-lookup"><span data-stu-id="d1de4-115">When you are dealing with the encryption of data, especially in an enterprise environment, consider how that data can be recovered in the event of a hardware failure, changes in personnel, or other situations in which encryption keys can be lost.</span></span>

<span data-ttu-id="d1de4-116">Os recursos de recuperação de unidade criptografada do MBAM garantem que os dados possam ser capturados e armazenados e que as ferramentas necessárias estejam disponíveis para acessar um volume protegido pelo BitLocker quando o BitLocker entra no modo de recuperação, é movido ou é corrompido.</span><span class="sxs-lookup"><span data-stu-id="d1de4-116">The encrypted drive recovery features of MBAM ensure that data can be captured and stored and that the required tools are available to access a BitLocker-protected volume when BitLocker goes into recovery mode, is moved, or becomes corrupted.</span></span>

[<span data-ttu-id="d1de4-117">Como recuperar uma unidade no modo de recuperação</span><span class="sxs-lookup"><span data-stu-id="d1de4-117">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

[<span data-ttu-id="d1de4-118">Como recuperar uma unidade movida</span><span class="sxs-lookup"><span data-stu-id="d1de4-118">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-2.md)

[<span data-ttu-id="d1de4-119">Como recuperar uma unidade corrompida</span><span class="sxs-lookup"><span data-stu-id="d1de4-119">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-2.md)

## <span data-ttu-id="d1de4-120">Determinar o estado de criptografia do BitLocker dos computadores perdidos usando MBAM</span><span class="sxs-lookup"><span data-stu-id="d1de4-120">Determine BitLocker Encryption State of Lost Computers by Using MBAM</span></span>


<span data-ttu-id="d1de4-121">Usando o MBAM, você pode determinar o último status de criptografia do BitLocker conhecido de computadores que foram perdidos ou roubados.</span><span class="sxs-lookup"><span data-stu-id="d1de4-121">Using MBAM, you can determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span>

[<span data-ttu-id="d1de4-122">Como determinar o estado de criptografia BitLocker de computadores perdidos</span><span class="sxs-lookup"><span data-stu-id="d1de4-122">How to Determine BitLocker Encryption State of Lost Computers</span></span>](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

## <span data-ttu-id="d1de4-123">Usar o portal de autoatendimento para recuperar o acesso a um computador</span><span class="sxs-lookup"><span data-stu-id="d1de4-123">Use the Self-Service Portal to Regain Access to a Computer</span></span>


<span data-ttu-id="d1de4-124">Se os usuários finais forem bloqueados pelo BitLocker, eles poderão usar as instruções desta seção para obter uma chave de recuperação do BitLocker e obter novamente o acesso ao computador.</span><span class="sxs-lookup"><span data-stu-id="d1de4-124">If end users get locked out of Windows by BitLocker, they can use the instructions in this section to get a BitLocker recovery key to regain access to their computer.</span></span>

[<span data-ttu-id="d1de4-125">Como usar o Portal de Autoatendimento para recuperar o acesso a um computador</span><span class="sxs-lookup"><span data-stu-id="d1de4-125">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>](how-to-use-the-self-service-portal-to-regain-access-to-a-computer.md)

## <span data-ttu-id="d1de4-126">Outros recursos para executar o gerenciamento do BitLocker com o MBAM</span><span class="sxs-lookup"><span data-stu-id="d1de4-126">Other Resources for Performing BitLocker Management with MBAM</span></span>


[<span data-ttu-id="d1de4-127">Operações do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d1de4-127">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





