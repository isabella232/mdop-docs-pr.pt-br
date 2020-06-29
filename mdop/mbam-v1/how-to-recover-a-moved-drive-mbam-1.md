---
title: Como recuperar uma unidade movida
description: Como recuperar uma unidade movida
author: dansimp
ms.assetid: 0c7199d8-9463-4f44-9af3-b70eceeaff1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e73e0878a3102d56494feb33efa69182029988c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796122"
---
# <span data-ttu-id="bcc4c-103">Como recuperar uma unidade movida</span><span class="sxs-lookup"><span data-stu-id="bcc4c-103">How to Recover a Moved Drive</span></span>


<span data-ttu-id="bcc4c-104">Ao mover uma unidade de sistema operacional anteriormente criptografada usando o Microsoft BitLocker Administration and Monitoring (MBAM), você deve resolver certos problemas.</span><span class="sxs-lookup"><span data-stu-id="bcc4c-104">When you move an operating system drive that has been previously encrypted by using Microsoft BitLocker Administration and Monitoring (MBAM), you must resolve certain issues.</span></span> <span data-ttu-id="bcc4c-105">Depois que um PIN é anexado ao novo computador, a unidade não aceita o PIN de inicialização que foi usado no computador anterior.</span><span class="sxs-lookup"><span data-stu-id="bcc4c-105">After a PIN is attached to the new computer, the drive will not accept the start-up PIN that was used in previous computer.</span></span> <span data-ttu-id="bcc4c-106">O sistema considera o PIN como inválido devido à mudança para o chip TPM (Trusted Platform Module).</span><span class="sxs-lookup"><span data-stu-id="bcc4c-106">The system considers the PIN to be invalid because of the change to the Trusted Platform Module (TPM) chip.</span></span> <span data-ttu-id="bcc4c-107">Você deve obter uma ID da chave de recuperação para recuperar a senha de recuperação a fim de usar a unidade movida.</span><span class="sxs-lookup"><span data-stu-id="bcc4c-107">You must obtain a recovery key ID to retrieve the recovery password in order to use the moved drive.</span></span> <span data-ttu-id="bcc4c-108">Para fazer isso, use o procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="bcc4c-108">To do this, use the following procedure.</span></span>

**<span data-ttu-id="bcc4c-109">Para recuperar uma unidade movida</span><span class="sxs-lookup"><span data-stu-id="bcc4c-109">To recover a moved drive</span></span>**

1.  <span data-ttu-id="bcc4c-110">No computador que contém a unidade movida, inicie no modo de ambiente de recuperação do Windows (WinRE) ou inicie o computador usando o diagnóstico e o conjunto de ferramentas de recuperação (DaRT) da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bcc4c-110">On the computer that contains the moved drive, start in Windows Recovery Environment (WinRE) mode, or start the computer by using the Microsoft Diagnostics and Recovery Toolset (DaRT).</span></span>

2.  <span data-ttu-id="bcc4c-111">Depois que o computador for iniciado com o WinRE ou o DaRT, o MBAM tratará a unidade do sistema operacional movida como uma unidade de dados.</span><span class="sxs-lookup"><span data-stu-id="bcc4c-111">Once the computer has been started with WinRE or DaRT, MBAM will treat the moved operating system drive as a data drive.</span></span> <span data-ttu-id="bcc4c-112">O MBAM exibirá a identificação da senha de recuperação da unidade e solicitará a senha de recuperação.</span><span class="sxs-lookup"><span data-stu-id="bcc4c-112">MBAM will then display the drive’s recovery password ID and ask for the recovery password.</span></span>

    <span data-ttu-id="bcc4c-113">**Observação**  Em alguns casos, você poderá clicar em **eu esquecer o PIN** durante o processo de inicialização para entrar no modo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="bcc4c-113">**Note** In some cases, you might be able to click **I forget the PIN** during the startup process to enter the recovery mode.</span></span> <span data-ttu-id="bcc4c-114">Isso também exibe a ID da chave de recuperação.</span><span class="sxs-lookup"><span data-stu-id="bcc4c-114">This also displays the recovery key ID.</span></span>

     

3.  <span data-ttu-id="bcc4c-115">No site de administração do MBAM, use a ID da chave de recuperação para recuperar a senha de recuperação e desbloquear a unidade.</span><span class="sxs-lookup"><span data-stu-id="bcc4c-115">On the MBAM administration website, use the recovery key ID to retrieve the recovery password and unlock the drive.</span></span>

4.  <span data-ttu-id="bcc4c-116">Se a unidade movida foi configurada para usar um chip TPM no computador original, você deve executar etapas adicionais após desbloquear a unidade e concluir o processo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="bcc4c-116">If the moved drive was configured to use a TPM chip on the original computer, you must take additional steps after you unlock the drive and complete the start process.</span></span> <span data-ttu-id="bcc4c-117">No modo WinRE, abra um prompt de comando e use a ferramenta **Manage-bde** para descriptografar a unidade.</span><span class="sxs-lookup"><span data-stu-id="bcc4c-117">In WinRE mode, open a command prompt and use the **manage-bde** tool to decrypt the drive.</span></span> <span data-ttu-id="bcc4c-118">O uso dessa ferramenta é a única maneira de remover a proteção TPM-mais-PIN sem o chip TPM original.</span><span class="sxs-lookup"><span data-stu-id="bcc4c-118">The use of this tool is the only way to remove the TPM-plus-PIN protection without the original TPM chip.</span></span>

5.  <span data-ttu-id="bcc4c-119">Após a conclusão da remoção, inicie o sistema normalmente.</span><span class="sxs-lookup"><span data-stu-id="bcc4c-119">After the removal is complete, start the system normally.</span></span> <span data-ttu-id="bcc4c-120">O agente do MBAM continuará importando a política para criptografar a unidade com o novo PIN do computador e o PIN.</span><span class="sxs-lookup"><span data-stu-id="bcc4c-120">The MBAM agent will proceed to enforce the policy to encrypt the drive with the new computer’s TPM plus PIN.</span></span>

## <span data-ttu-id="bcc4c-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bcc4c-121">Related topics</span></span>


[<span data-ttu-id="bcc4c-122">Realizar o Gerenciamento do BitLocker com o MBAM</span><span class="sxs-lookup"><span data-stu-id="bcc4c-122">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





