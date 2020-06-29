---
title: Sobre o chip de TPM do computador
description: Sobre o chip de TPM do computador
author: dansimp
ms.assetid: 6f1cf18c-277a-4932-886d-14202ca8d175
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f6df54dc8085c398bacc508fdbbb79a30b0e4204
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799291"
---
# <span data-ttu-id="d0057-103">Sobre o chip de TPM do computador</span><span class="sxs-lookup"><span data-stu-id="d0057-103">About the Computer TPM Chip</span></span>


<span data-ttu-id="d0057-104">O BitLocker fornece proteção adicional quando é usado com um chip TPM (Trusted Platform Module).</span><span class="sxs-lookup"><span data-stu-id="d0057-104">BitLocker provides additional protection when it is used with a Trusted Platform Module (TPM) chip.</span></span> <span data-ttu-id="d0057-105">O chip TPM é um componente de hardware que é instalado em muitos computadores mais novos pelos fabricantes de computador.</span><span class="sxs-lookup"><span data-stu-id="d0057-105">The TPM chip is a hardware component that is installed in many newer computers by the computer manufacturers.</span></span> <span data-ttu-id="d0057-106">O Microsoft BitLocker Administration and Monitoring (MBAM) usa o BitLocker, além do chip TPM, para ajudar a fornecer proteção adicional dos seus dados e garantir que seu computador não tenha sido adulterado.</span><span class="sxs-lookup"><span data-stu-id="d0057-106">Microsoft BitLocker Administration and Monitoring (MBAM) uses BitLocker, in addition to the TPM chip, to help provide additional protection of your data and to make sure that your computer has not been tampered with.</span></span>

## <span data-ttu-id="d0057-107">Como configurar seu TPM</span><span class="sxs-lookup"><span data-stu-id="d0057-107">How to Set Up Your TPM</span></span>


<span data-ttu-id="d0057-108">Quando você inicia o assistente de criptografia de unidade de disco BitLocker em seu computador, o BitLocker verifica se a sua organização configurou o BitLocker para usar um chip TPM.</span><span class="sxs-lookup"><span data-stu-id="d0057-108">When you start the BitLocker Drive Encryption wizard on your computer, BitLocker checks for a TPM chip if your organization has configured BitLocker to use a TPM chip.</span></span> <span data-ttu-id="d0057-109">Se o BitLocker encontrar um chip TPM compatível, você pode ser solicitado a reiniciar o computador para habilitar o chip TPM para uso.</span><span class="sxs-lookup"><span data-stu-id="d0057-109">If BitLocker finds a compatible TPM chip, you may be prompted to restart your computer to enable the TPM chip for use.</span></span> <span data-ttu-id="d0057-110">Assim que o computador for reiniciado, siga as instruções para configurar o chip TPM no BIOS (o BIOS é uma camada anterior ao Windows do seu software de computador).</span><span class="sxs-lookup"><span data-stu-id="d0057-110">As soon as your computer has restarted, follow the instructions to configure the TPM chip in the BIOS (the BIOS is a pre-Windows layer of your computer software).</span></span>

<span data-ttu-id="d0057-111">Após a configuração do BitLocker, você pode acessar informações adicionais sobre o chip do TPM abrindo a ferramenta opções de criptografia BitLocker no painel de controle do Windows e, em seguida, selecionando **Administração do TPM**.</span><span class="sxs-lookup"><span data-stu-id="d0057-111">After BitLocker is configured, you can access additional information about the TPM chip by opening the BitLocker Encryption Options tool in the Windows Control Panel, and then selecting **TPM Administration**.</span></span>

<span data-ttu-id="d0057-112">**Observação**  Você deve ter credenciais administrativas no seu computador para acessar essa ferramenta.</span><span class="sxs-lookup"><span data-stu-id="d0057-112">**Note** You must have administrative credentials on your computer to access this tool.</span></span>

 

<span data-ttu-id="d0057-113">Em uma falha de TPM, uma alteração no BIOS ou determinadas atualizações do Windows, o BitLocker bloqueará seu computador e exigirá que você entre em contato com o suporte técnico para desbloqueá-lo.</span><span class="sxs-lookup"><span data-stu-id="d0057-113">In a TPM failure, a change in the BIOS, or certain Windows Updates, BitLocker will lock your computer and require you to contact your Help Desk to unlock it.</span></span> <span data-ttu-id="d0057-114">Você precisa fornecer o nome do seu computador, bem como o domínio do computador.</span><span class="sxs-lookup"><span data-stu-id="d0057-114">You have to provide the name of your computer as well as your computer’s domain.</span></span> <span data-ttu-id="d0057-115">O suporte técnico pode fornecer um arquivo de senha que pode ser usado para desbloquear seu computador.</span><span class="sxs-lookup"><span data-stu-id="d0057-115">Help Desk can give you a password file that can be used to unlock your computer.</span></span>

## <span data-ttu-id="d0057-116">Solução de problemas de TPM</span><span class="sxs-lookup"><span data-stu-id="d0057-116">Troubleshooting TPM Issues</span></span>


<span data-ttu-id="d0057-117">Se ocorrer uma falha no TPM, alterar o BIOS ou algumas atualizações do Windows ocorrerem, o BitLocker bloqueará seu computador e exigirá que você entre em contato com o suporte técnico para desbloqueá-lo.</span><span class="sxs-lookup"><span data-stu-id="d0057-117">If a TPM failure, change in the BIOS, or certain Windows Updates occur, BitLocker will lock your computer and require you to contact your Help Desk to unlock it.</span></span> <span data-ttu-id="d0057-118">Você precisa fornecer o nome do seu computador, bem como o domínio do computador.</span><span class="sxs-lookup"><span data-stu-id="d0057-118">You have to provide the name of your computer as well as your computer’s domain.</span></span> <span data-ttu-id="d0057-119">O suporte técnico pode fornecer um arquivo de senha que você pode usar para desbloquear seu computador.</span><span class="sxs-lookup"><span data-stu-id="d0057-119">The Help Desk can give you a password file that you can use to unlock your computer.</span></span>

## <span data-ttu-id="d0057-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d0057-120">Related topics</span></span>


[<span data-ttu-id="d0057-121">Ajudando os usuários finais a gerenciar o BitLocker</span><span class="sxs-lookup"><span data-stu-id="d0057-121">Helping End Users Manage BitLocker</span></span>](helping-end-users-manage-bitlocker.md)

[<span data-ttu-id="d0057-122">Como usar seu PIN ou sua senha</span><span class="sxs-lookup"><span data-stu-id="d0057-122">Using Your PIN or Password</span></span>](using-your-pin-or-password.md)

 

 





