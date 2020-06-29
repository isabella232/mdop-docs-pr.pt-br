---
title: Como recuperar uma unidade movida
description: Como recuperar uma unidade movida
author: dansimp
ms.assetid: 697cd78d-962c-411e-901a-2e9220ba6552
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bd0d43f2eea95fe71225a50e7fa68d4fb1c35485
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799597"
---
# <span data-ttu-id="2598d-103">Como recuperar uma unidade movida</span><span class="sxs-lookup"><span data-stu-id="2598d-103">How to Recover a Moved Drive</span></span>


<span data-ttu-id="2598d-104">Quando você move uma unidade de sistema operacional criptografada usando o Microsoft BitLocker Administration and Monitoring (MBAM), a unidade não aceita o PIN que foi usado em um computador anterior devido à mudança para o chip TPM (Trusted Platform Module).</span><span class="sxs-lookup"><span data-stu-id="2598d-104">When you move an operating system drive that is encrypted by using Microsoft BitLocker Administration and Monitoring (MBAM), the drive will not accept the PIN that was used in a previous computer because of the change to the Trusted Platform Module (TPM) chip.</span></span> <span data-ttu-id="2598d-105">Para usar a unidade movida, você precisará de uma maneira de obter a ID da chave de recuperação para recuperar a senha de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2598d-105">To use the moved drive, you will need a way to obtain the recovery key ID to retrieve the recovery password.</span></span> <span data-ttu-id="2598d-106">Use o procedimento a seguir para recuperar uma unidade que foi movida.</span><span class="sxs-lookup"><span data-stu-id="2598d-106">Use the following procedure to recover a drive that has moved.</span></span>

**<span data-ttu-id="2598d-107">Para recuperar uma unidade movida</span><span class="sxs-lookup"><span data-stu-id="2598d-107">To recover a moved drive</span></span>**

1.  <span data-ttu-id="2598d-108">No computador que contém a unidade movida, inicie o computador no modo de ambiente de recuperação do Windows (WinRE) ou inicie o computador usando o conjunto de ferramentas de diagnóstico e recuperação (DaRT) da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2598d-108">On the computer that contains the moved drive, start the computer in Windows recovery environment (WinRE) mode, or start the computer by using the Microsoft Diagnostic and Recovery Toolset (DaRT).</span></span>

2.  <span data-ttu-id="2598d-109">Depois que o computador for iniciado com o WinRE ou o DaRT, a administração e o monitoramento do Microsoft BitLocker tratarão a unidade do sistema operacional movida como uma unidade de dados.</span><span class="sxs-lookup"><span data-stu-id="2598d-109">Once the computer has been started with WinRE or DaRT, Microsoft BitLocker Administration and Monitoring will treat the moved operating system drive as a data drive.</span></span> <span data-ttu-id="2598d-110">O MBAM exibirá a identificação da senha de recuperação da unidade e solicitará a senha de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2598d-110">MBAM will then display the drive’s recovery password ID and ask for the recovery password.</span></span>

    <span data-ttu-id="2598d-111">**Observação**  Em alguns casos, você poderá clicar em **esqueci o PIN** durante o processo de inicialização e, em seguida, inserir o modo de recuperação para exibir a ID da chave de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2598d-111">**Note** In some cases, you may be able to click **I forgot the PIN** during the startup process, and then enter the recovery mode to display the recovery key ID.</span></span>

     

3.  <span data-ttu-id="2598d-112">Use a ID da chave de recuperação para recuperar a senha de recuperação e desbloquear a unidade no site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="2598d-112">Use the recovery key ID to retrieve the recovery password and unlock the drive from the Administration and Monitoring website.</span></span>

4.  <span data-ttu-id="2598d-113">Se a unidade movida foi configurada para usar um chip TPM no computador original, você deve executar etapas adicionais após desbloquear a unidade e concluir o processo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="2598d-113">If the moved drive was configured to use a TPM chip on the original computer, you must take additional steps after unlocking the drive and completing the start process.</span></span> <span data-ttu-id="2598d-114">No modo WinRE, abra um prompt de comando e use a ferramenta **Manage-bde** para descriptografar a unidade.</span><span class="sxs-lookup"><span data-stu-id="2598d-114">In WinRE mode, open a command prompt and use the **manage-bde** tool to decrypt the drive.</span></span> <span data-ttu-id="2598d-115">Usar essa ferramenta é a única maneira de remover o TPM e o protetor de pino sem o chip TPM original.</span><span class="sxs-lookup"><span data-stu-id="2598d-115">Using this tool is the only way to remove the TPM plus PIN protector without the original TPM chip.</span></span>

5.  <span data-ttu-id="2598d-116">Quando a remoção for concluída, inicie o computador normalmente.</span><span class="sxs-lookup"><span data-stu-id="2598d-116">Once the removal is completed, start the computer normally.</span></span> <span data-ttu-id="2598d-117">O agente do MBAM agora irá impor a política para criptografar a unidade com o novo PIN do computador e o PIN do novo computador.</span><span class="sxs-lookup"><span data-stu-id="2598d-117">The MBAM agent will now enforce the policy to encrypt the drive with the new computer’s TPM plus PIN.</span></span>

## <span data-ttu-id="2598d-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2598d-118">Related topics</span></span>


[<span data-ttu-id="2598d-119">Realizar o Gerenciamento do BitLocker com o MBAM</span><span class="sxs-lookup"><span data-stu-id="2598d-119">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





