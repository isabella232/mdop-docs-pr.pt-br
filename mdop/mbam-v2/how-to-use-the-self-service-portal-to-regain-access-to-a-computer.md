---
title: Como usar o Portal de Autoatendimento para recuperar o acesso a um computador
description: Como usar o Portal de Autoatendimento para recuperar o acesso a um computador
author: dansimp
ms.assetid: bcf095de-0237-4bb0-b450-da8fb6d6f3d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4abcffcf35e09bd5e24f4715a38dca74518ba29e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799800"
---
# <span data-ttu-id="11c1b-103">Como usar o Portal de Autoatendimento para recuperar o acesso a um computador</span><span class="sxs-lookup"><span data-stu-id="11c1b-103">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>


<span data-ttu-id="11c1b-104">Se os usuários finais se tornarem desbloqueados pelo BitLocker porque esquecim a senha ou o PIN, ou porque mudaram arquivos do sistema operacional ou alteraram o BIOS ou o TPM (Trusted Platform Module), eles podem usar o portal de autoatendimento para obter acesso ao Windows sem precisar solicitar assistência técnica para obter ajuda.</span><span class="sxs-lookup"><span data-stu-id="11c1b-104">If end users get locked out of Windows by BitLocker because they forgot their password or PIN, or because they changed operating system files or changed the BIOS or the Trusted Platform Module (TPM), they can use the Self-Service Portal to regain access to Windows without having to ask their Help Desk for assistance.</span></span>

<span data-ttu-id="11c1b-105">**Observação**  Se o administrador de ti configurou um tempo limite de estado de sessão IIS, uma mensagem será exibida 60 segundos antes do tempo limite.</span><span class="sxs-lookup"><span data-stu-id="11c1b-105">**Note** If the IT administrator configured an IIS Session State time-out, a message is displayed 60 seconds prior to the time-out.</span></span>

 

<span data-ttu-id="11c1b-106">**Observação**  Essas instruções são escritas para e da perspectiva de usuários finais.</span><span class="sxs-lookup"><span data-stu-id="11c1b-106">**Note** These instructions are written for and from the perspective of end users.</span></span>

 

**<span data-ttu-id="11c1b-107">Para usar o portal de autoatendimento para recuperar o acesso a um computador</span><span class="sxs-lookup"><span data-stu-id="11c1b-107">To use the Self-Service Portal to regain access to a computer</span></span>**

1.  <span data-ttu-id="11c1b-108">No campo **KeyId de recuperação** , insira um mínimo de oito da ID de chave do bitlocker de 32 dígitos que é exibido na tela de recuperação do BitLocker do computador.</span><span class="sxs-lookup"><span data-stu-id="11c1b-108">In the **Recovery KeyId** field, enter a minimum of eight of the 32-digit BitLocker Key ID that is displayed on the BitLocker recovery screen of your computer.</span></span>

    <span data-ttu-id="11c1b-109">**Observação**  Se os oito primeiros dígitos corresponderem a várias chaves, será exibida uma mensagem solicitando que você insira todos os dígitos do 32 da ID da chave de recuperação.</span><span class="sxs-lookup"><span data-stu-id="11c1b-109">**Note** If the first eight digits match multiple keys, a message displays that requires you to enter all 32 digits of the recovery key ID.</span></span>

     

2.  <span data-ttu-id="11c1b-110">No campo **motivo** , selecione um motivo para a sua solicitação para a chave de recuperação.</span><span class="sxs-lookup"><span data-stu-id="11c1b-110">In the **Reason** field, select a reason for your request for the recovery key.</span></span>

3.  <span data-ttu-id="11c1b-111">Clique em **obter chave**.</span><span class="sxs-lookup"><span data-stu-id="11c1b-111">Click **Get Key**.</span></span> <span data-ttu-id="11c1b-112">A chave de recuperação do BitLocker será exibida no campo "a chave de recuperação do BitLocker".</span><span class="sxs-lookup"><span data-stu-id="11c1b-112">Your BitLocker recovery key is displayed in the “Your BitLocker Recovery Key” field.</span></span>

4.  <span data-ttu-id="11c1b-113">Digite o código de 48 dígitos na tela de recuperação do BitLocker no computador para obter novamente o acesso ao computador.</span><span class="sxs-lookup"><span data-stu-id="11c1b-113">Enter the 48-digit code into the BitLocker recovery screen on your computer to regain access to the computer.</span></span>

## <span data-ttu-id="11c1b-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="11c1b-114">Related topics</span></span>


[<span data-ttu-id="11c1b-115">Realizar o Gerenciamento do BitLocker com o MBAM</span><span class="sxs-lookup"><span data-stu-id="11c1b-115">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





