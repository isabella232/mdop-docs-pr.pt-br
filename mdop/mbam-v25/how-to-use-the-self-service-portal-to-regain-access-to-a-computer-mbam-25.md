---
title: Como usar o Portal de Autoatendimento para recuperar o acesso a um computador
description: Como usar o Portal de Autoatendimento para recuperar o acesso a um computador
author: dansimp
ms.assetid: 3c24b13a-d1b1-4763-8ac0-0b2db46267e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cde9c71a957a5270d69aa8388455895f1cb2432b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799925"
---
# <span data-ttu-id="ef875-103">Como usar o Portal de Autoatendimento para recuperar o acesso a um computador</span><span class="sxs-lookup"><span data-stu-id="ef875-103">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>


<span data-ttu-id="ef875-104">O portal de autoatendimento é um site que os administradores de ti configuram como parte da implantação do Microsoft BitLocker Administration and Monitoring (MBAM) 2,5.</span><span class="sxs-lookup"><span data-stu-id="ef875-104">The Self-Service Portal is a website that IT administrators configure as part of their Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 deployment.</span></span> <span data-ttu-id="ef875-105">O website permite que os usuários finais recuperem o acesso de modo independente em seus computadores se eles estiverem bloqueados do Windows.</span><span class="sxs-lookup"><span data-stu-id="ef875-105">The website enables end users to independently regain access to their computers if they get locked out of Windows.</span></span> <span data-ttu-id="ef875-106">O portal de autoatendimento não requer assistência para a equipe de suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="ef875-106">The Self-Service Portal requires no assistance from Help Desk staff.</span></span>

<span data-ttu-id="ef875-107">As instruções a seguir são escritas da perspectiva dos usuários finais, mas as informações podem ser úteis para que os administradores de ti compreendam.</span><span class="sxs-lookup"><span data-stu-id="ef875-107">The following instructions are written from the perspective of end users, but the information may be useful for IT administrators to understand.</span></span>

<span data-ttu-id="ef875-108">**Importante**  Um usuário final deve ter conectado fisicamente ao computador (não remotamente) pelo menos uma vez com êxito para poder recuperar a chave usando o portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="ef875-108">**Important** An end user must have physically logged on to the computer (not remotely) at least one time successfully to be able to recover their key using the Self-Service Portal.</span></span> <span data-ttu-id="ef875-109">Caso contrário, eles devem usar o portal de helpdesk para a recuperação de chave.</span><span class="sxs-lookup"><span data-stu-id="ef875-109">Otherwise, they must use the Helpdesk Portal for key recovery.</span></span>

 

<span data-ttu-id="ef875-110">Os usuários finais podem ter travamentos se:</span><span class="sxs-lookup"><span data-stu-id="ef875-110">End users may experience lockouts if they:</span></span>

-   <span data-ttu-id="ef875-111">Esquecer a senha ou o PIN</span><span class="sxs-lookup"><span data-stu-id="ef875-111">Forget their password or PIN</span></span>

-   <span data-ttu-id="ef875-112">Alterar os arquivos do sistema operacional, o BIOS ou o Trusted Platform Module (TPM)</span><span class="sxs-lookup"><span data-stu-id="ef875-112">Change operating system files, the BIOS, or the Trusted Platform Module (TPM)</span></span>

<span data-ttu-id="ef875-113">**Observação**  Se o administrador de ti configurou um tempo limite de estado de sessão do IIS, uma mensagem será exibida no portal de autoatendimento 60 segundos antes do tempo limite.</span><span class="sxs-lookup"><span data-stu-id="ef875-113">**Note** If the IT administrator configured an IIS Session State time-out, a message is displayed in the Self-Service Portal 60 seconds prior to the time-out.</span></span>

 

**<span data-ttu-id="ef875-114">Para usar o portal de autoatendimento para recuperar o acesso a um computador</span><span class="sxs-lookup"><span data-stu-id="ef875-114">To use the Self-Service Portal to regain access to a computer</span></span>**

1.  <span data-ttu-id="ef875-115">No campo **KeyId de recuperação** , insira um mínimo de oito da ID de chave do bitlocker de 32 dígitos que é exibido na tela de recuperação do BitLocker do computador.</span><span class="sxs-lookup"><span data-stu-id="ef875-115">In the **Recovery KeyId** field, enter a minimum of eight of the 32-digit BitLocker Key ID that is displayed on the BitLocker recovery screen of your computer.</span></span> <span data-ttu-id="ef875-116">Se os oito primeiros dígitos corresponderem a várias chaves, será exibida uma mensagem solicitando que você insira todos os dígitos do 32 da ID da chave de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ef875-116">If the first eight digits match multiple keys, a message displays that requires you to enter all 32 digits of the recovery key ID.</span></span>

2.  <span data-ttu-id="ef875-117">No campo **motivo** , selecione um motivo para a sua solicitação para a chave de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ef875-117">In the **Reason** field, select a reason for your request for the recovery key.</span></span>

3.  <span data-ttu-id="ef875-118">Clique em **obter chave**.</span><span class="sxs-lookup"><span data-stu-id="ef875-118">Click **Get Key**.</span></span> <span data-ttu-id="ef875-119">A chave de recuperação do BitLocker será exibida no campo **chave de recuperação do BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="ef875-119">Your BitLocker recovery key is displayed in the **Your BitLocker Recovery Key** field.</span></span>

4.  <span data-ttu-id="ef875-120">Digite o código de 48 dígitos na tela de recuperação do BitLocker no computador para obter novamente o acesso ao computador.</span><span class="sxs-lookup"><span data-stu-id="ef875-120">Enter the 48-digit code into the BitLocker recovery screen on your computer to regain access to the computer.</span></span>



## <span data-ttu-id="ef875-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ef875-121">Related topics</span></span>


[<span data-ttu-id="ef875-122">Realizando o gerenciamento do BitLocker com o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ef875-122">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 
## <span data-ttu-id="ef875-123">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="ef875-123">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="ef875-124">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="ef875-124">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="ef875-125">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="ef875-125">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





