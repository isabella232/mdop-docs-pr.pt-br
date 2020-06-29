---
title: Realizando o gerenciamento do BitLocker com o MBAM 2.5
description: Realizando o gerenciamento do BitLocker com o MBAM 2.5
author: dansimp
ms.assetid: 068f3ee0-300c-4083-ba18-7065eef997ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a0ee5802f945176914c56659e0ff7e34e93a969
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799786"
---
# <span data-ttu-id="172c5-103">Realizando o gerenciamento do BitLocker com o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="172c5-103">Performing BitLocker Management with MBAM 2.5</span></span>


<span data-ttu-id="172c5-104">Depois de planejar e implantar o Microsoft BitLocker Administration and Monitoring (MBAM), você pode configurá-lo e usá-lo para gerenciar a criptografia de unidade de disco BitLocker na sua empresa.</span><span class="sxs-lookup"><span data-stu-id="172c5-104">After planning and then deploying Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use it to manage BitLocker Drive Encryption across your enterprise.</span></span> <span data-ttu-id="172c5-105">As informações nesta seção descrevem tarefas de gerenciamento de criptografia do BitLocker do dia a dia após a instalação que são realizadas usando a administração e o monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="172c5-105">The information in this section describes post-installation, day-to-day BitLocker encryption management tasks that are accomplished by using Microsoft BitLocker Administration and Monitoring.</span></span>

## <span data-ttu-id="172c5-106">Redefinir um bloqueio de TPM</span><span class="sxs-lookup"><span data-stu-id="172c5-106">Reset a TPM lockout</span></span>


<span data-ttu-id="172c5-107">Um TPM (Trusted Platform Module) é um microchip projetado para fornecer funções básicas relacionadas à segurança, principalmente envolvendo chaves de criptografia.</span><span class="sxs-lookup"><span data-stu-id="172c5-107">A Trusted Platform Module (TPM) is a microchip that is designed to provide basic security-related functions, primarily involving encryption keys.</span></span> <span data-ttu-id="172c5-108">O TPM geralmente é instalado na placa-mãe de um computador e comunica-se com o restante do sistema usando um adaptador de barramento do host.</span><span class="sxs-lookup"><span data-stu-id="172c5-108">The TPM is usually installed on the motherboard of a computer, and it communicates with the rest of the system by using a host bus adapter.</span></span> <span data-ttu-id="172c5-109">Em computadores que incorporam um TPM, você pode criar chaves criptográficas e criptografá-las para que elas possam ser descriptografadas apenas pelo TPM.</span><span class="sxs-lookup"><span data-stu-id="172c5-109">On computers that incorporate a TPM, you can create cryptographic keys and encrypt them so that they can be decrypted only by the TPM.</span></span>

<span data-ttu-id="172c5-110">Um bloqueio de TPM pode ocorrer se um usuário inserir o PIN incorreto muitas vezes.</span><span class="sxs-lookup"><span data-stu-id="172c5-110">A TPM lockout can occur if a user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="172c5-111">O número de vezes que um usuário pode inserir um PIN incorreto antes que os bloqueios do TPM variem de acordo com o fabricante.</span><span class="sxs-lookup"><span data-stu-id="172c5-111">The number of times that a user can enter an incorrect PIN before the TPM locks varies by manufacturer.</span></span> <span data-ttu-id="172c5-112">Você pode usar o MBAM para acessar o sistema de dados de recuperação de chave centralizada no site de administração e monitoramento, onde você pode recuperar um arquivo de senha de proprietário do TPM quando fornecer uma ID de computador e um identificador de usuário associado.</span><span class="sxs-lookup"><span data-stu-id="172c5-112">You can use MBAM to access the centralized key recovery data system on the Administration and Monitoring Website, where you can retrieve a TPM owner password file when you supply a computer ID and an associated user identifier.</span></span>

[<span data-ttu-id="172c5-113">Como redefinir um bloqueio de TPM</span><span class="sxs-lookup"><span data-stu-id="172c5-113">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-25.md)

## <span data-ttu-id="172c5-114">Recuperar unidades</span><span class="sxs-lookup"><span data-stu-id="172c5-114">Recover drives</span></span>


<span data-ttu-id="172c5-115">Quando você estiver lidando com a criptografia de dados, especialmente em um ambiente corporativo, considere como esses dados podem ser recuperados em caso de falha de hardware, mudanças na equipe ou outras situações nas quais as chaves de criptografia podem ser perdidas.</span><span class="sxs-lookup"><span data-stu-id="172c5-115">When you are dealing with the encryption of data, especially in an enterprise environment, consider how that data can be recovered in the event of a hardware failure, changes in personnel, or other situations in which encryption keys can be lost.</span></span>

<span data-ttu-id="172c5-116">Os recursos de recuperação de unidade criptografada no MBAM garantem que os dados possam ser capturados e armazenados e que as ferramentas necessárias estejam disponíveis para acessar um volume protegido pelo BitLocker quando o BitLocker entra no modo de recuperação, é movido ou é corrompido.</span><span class="sxs-lookup"><span data-stu-id="172c5-116">The encrypted drive recovery features in MBAM ensure that data can be captured and stored and that the required tools are available to access a BitLocker-protected volume when BitLocker goes into recovery mode, is moved, or becomes corrupted.</span></span>

[<span data-ttu-id="172c5-117">Como recuperar uma unidade no modo de recuperação</span><span class="sxs-lookup"><span data-stu-id="172c5-117">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)

[<span data-ttu-id="172c5-118">Como recuperar uma unidade movida</span><span class="sxs-lookup"><span data-stu-id="172c5-118">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-25.md)

[<span data-ttu-id="172c5-119">Como recuperar uma unidade corrompida</span><span class="sxs-lookup"><span data-stu-id="172c5-119">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-25.md)

## <span data-ttu-id="172c5-120">Determinar o estado de criptografia BitLocker dos computadores perdidos</span><span class="sxs-lookup"><span data-stu-id="172c5-120">Determine BitLocker encryption state of lost computers</span></span>


<span data-ttu-id="172c5-121">Ao usar o MBAM, você pode determinar o último status de criptografia do BitLocker conhecido de computadores que foram perdidos ou roubados.</span><span class="sxs-lookup"><span data-stu-id="172c5-121">By using MBAM, you can determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span>

[<span data-ttu-id="172c5-122">Como determinar o estado de criptografia BitLocker de computadores perdidos</span><span class="sxs-lookup"><span data-stu-id="172c5-122">How to Determine BitLocker Encryption State of Lost Computers</span></span>](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)

## <span data-ttu-id="172c5-123">Usar o portal de autoatendimento para recuperar o acesso a um computador</span><span class="sxs-lookup"><span data-stu-id="172c5-123">Use the Self-Service Portal to regain access to a computer</span></span>


<span data-ttu-id="172c5-124">Se os usuários finais forem bloqueados pelo BitLocker, eles poderão usar as instruções desta seção para obter uma chave de recuperação do BitLocker e obter novamente o acesso ao computador.</span><span class="sxs-lookup"><span data-stu-id="172c5-124">If end users get locked out of Windows by BitLocker, they can use the instructions in this section to get a BitLocker recovery key to regain access to their computer.</span></span>

[<span data-ttu-id="172c5-125">Como usar o Portal de Autoatendimento para recuperar o acesso a um computador</span><span class="sxs-lookup"><span data-stu-id="172c5-125">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>](how-to-use-the-self-service-portal-to-regain-access-to-a-computer-mbam-25.md)



## <span data-ttu-id="172c5-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="172c5-126">Related topics</span></span>


[<span data-ttu-id="172c5-127">Operações do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="172c5-127">Operations for MBAM 2.5</span></span>](operations-for-mbam-25.md)

 

## <span data-ttu-id="172c5-128">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="172c5-128">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="172c5-129">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="172c5-129">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="172c5-130">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="172c5-130">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





