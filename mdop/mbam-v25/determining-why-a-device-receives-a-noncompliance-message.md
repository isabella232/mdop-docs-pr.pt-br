---
title: Determinando por que um dispositivo recebe uma mensagem de não conformidade
description: Determinando por que um dispositivo recebe uma mensagem de não conformidade
author: dansimp
ms.assetid: 793df330-a0ee-4759-b53a-95618ac74428
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/22/2017
ms.openlocfilehash: ce1d344676ebf4328506228f1bfa87c76e8036f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799499"
---
# <span data-ttu-id="fe96d-103">Determinando por que um dispositivo recebe uma mensagem de não conformidade</span><span class="sxs-lookup"><span data-stu-id="fe96d-103">Determining why a Device Receives a Noncompliance Message</span></span>


<span data-ttu-id="fe96d-104">Os seguintes códigos de não conformidade são fornecidos pela WMI e descrevem os motivos pelos quais um determinado dispositivo é reportado pela MBAM como não compatível.</span><span class="sxs-lookup"><span data-stu-id="fe96d-104">The following noncompliance codes are provided by WMI and describe the reasons why a particular device is reported by MBAM as noncompliant.</span></span>

<span data-ttu-id="fe96d-105">Você pode usar o método preferencial para exibir o WMI.</span><span class="sxs-lookup"><span data-stu-id="fe96d-105">You can use your preferred method to view WMI.</span></span> <span data-ttu-id="fe96d-106">Se você usar o PowerShell, execute `gwmi -class mbam_volume -Namespace root\microsoft\mbam` a partir de um prompt do PowerShell e procure ReasonsForNoncompliance.</span><span class="sxs-lookup"><span data-stu-id="fe96d-106">If you use PowerShell, run `gwmi -class mbam_volume -Namespace root\microsoft\mbam` from a PowerShell prompt and search for ReasonsForNoncompliance.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fe96d-107">Código não compatível</span><span class="sxs-lookup"><span data-stu-id="fe96d-107">Non-Compliance Code</span></span></th>
<th align="left"><span data-ttu-id="fe96d-108">Motivo da não conformidade</span><span class="sxs-lookup"><span data-stu-id="fe96d-108">Reason for Non-Compliance</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe96d-109">0</span><span class="sxs-lookup"><span data-stu-id="fe96d-109">0</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe96d-110">O nível de codificação não é AES 256.</span><span class="sxs-lookup"><span data-stu-id="fe96d-110">Cipher strength not AES 256.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fe96d-111">um</span><span class="sxs-lookup"><span data-stu-id="fe96d-111">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe96d-112">A política MBAM exige que esse volume seja criptografado, mas não é.</span><span class="sxs-lookup"><span data-stu-id="fe96d-112">MBAM Policy requires this volume to be encrypted but it is not.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe96d-113">2</span><span class="sxs-lookup"><span data-stu-id="fe96d-113">2</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe96d-114">A política MBAM exige que esse volume não seja criptografado, mas está.</span><span class="sxs-lookup"><span data-stu-id="fe96d-114">MBAM Policy requires this volume to NOT be encrypted, but it is.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fe96d-115">3D</span><span class="sxs-lookup"><span data-stu-id="fe96d-115">3</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe96d-116">A política MBAM exige que esse volume use um protetor TPM, mas ele não faz isso.</span><span class="sxs-lookup"><span data-stu-id="fe96d-116">MBAM Policy requires this volume use a TPM protector, but it does not.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe96d-117">4</span><span class="sxs-lookup"><span data-stu-id="fe96d-117">4</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe96d-118">A política MBAM exige que esse volume use um protetor TPM + PIN, mas ele não faz isso.</span><span class="sxs-lookup"><span data-stu-id="fe96d-118">MBAM Policy requires this volume use a TPM+PIN protector, but it does not.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fe96d-119">5</span><span class="sxs-lookup"><span data-stu-id="fe96d-119">5</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe96d-120">A política MBAM não permite que máquinas não TPM relatem como compatíveis.</span><span class="sxs-lookup"><span data-stu-id="fe96d-120">MBAM Policy does not allow non TPM machines to report as compliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe96d-121">5</span><span class="sxs-lookup"><span data-stu-id="fe96d-121">6</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe96d-122">Volume tem um protetor TPM, mas o TPM não está visível (inicializado com a chave de recuperação após a desabilitação do TPM no BIOS?).</span><span class="sxs-lookup"><span data-stu-id="fe96d-122">Volume has a TPM protector but the TPM is not visible (booted with recover key after disabling TPM in BIOS?).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fe96d-123">7</span><span class="sxs-lookup"><span data-stu-id="fe96d-123">7</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe96d-124">A política MBAM exige que esse volume use um protetor de senha, mas ele não tem um.</span><span class="sxs-lookup"><span data-stu-id="fe96d-124">MBAM Policy requires this volume use a password protector, but it does not have one.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe96d-125">08</span><span class="sxs-lookup"><span data-stu-id="fe96d-125">8</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe96d-126">A política MBAM exige que esse volume não use um protetor de senha, mas ele tem um.</span><span class="sxs-lookup"><span data-stu-id="fe96d-126">MBAM Policy requires this volume NOT use a password protector, but it has one.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fe96d-127">222</span><span class="sxs-lookup"><span data-stu-id="fe96d-127">9</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe96d-128">A política MBAM exige que este volume use um protetor de desbloqueio automático, mas ele não tem um.</span><span class="sxs-lookup"><span data-stu-id="fe96d-128">MBAM Policy requires this volume use an auto-unlock protector, but it does not have one.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe96d-129">254</span><span class="sxs-lookup"><span data-stu-id="fe96d-129">10</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe96d-130">A política MBAM requer que esse volume não use um protetor de desbloqueio automático, mas tenha um.</span><span class="sxs-lookup"><span data-stu-id="fe96d-130">MBAM Policy requires this volume NOT use an auto-unlock protector, but it has one.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fe96d-131">11:00</span><span class="sxs-lookup"><span data-stu-id="fe96d-131">11</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe96d-132">Conflito de política detectado impedindo que o MBAM relate esse volume como compatível.</span><span class="sxs-lookup"><span data-stu-id="fe96d-132">Policy conflict detected preventing MBAM from reporting this volume as compliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe96d-133">12</span><span class="sxs-lookup"><span data-stu-id="fe96d-133">12</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe96d-134">Um volume do sistema é necessário para criptografar o volume do sistema operacional, mas ele não está presente.</span><span class="sxs-lookup"><span data-stu-id="fe96d-134">A system volume is needed to encrypt the OS volume but it is not present.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fe96d-135">0,13</span><span class="sxs-lookup"><span data-stu-id="fe96d-135">13</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe96d-136">Proteção suspensa para o volume.</span><span class="sxs-lookup"><span data-stu-id="fe96d-136">Protection is suspended for the volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe96d-137">quatorze</span><span class="sxs-lookup"><span data-stu-id="fe96d-137">14</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe96d-138">Autodesbloquear não seguro, a menos que o volume do sistema operacional seja criptografado.</span><span class="sxs-lookup"><span data-stu-id="fe96d-138">AutoUnlock unsafe unless the OS volume is encrypted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fe96d-139">15</span><span class="sxs-lookup"><span data-stu-id="fe96d-139">15</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe96d-140">A política requer força mínima de Cypher é XTS-AES-128 bit, o nível real de Cypher é mais fraco do que isso.</span><span class="sxs-lookup"><span data-stu-id="fe96d-140">Policy requires minimum cypher strength is XTS-AES-128 bit, actual cypher strength is weaker than that.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe96d-141">16</span><span class="sxs-lookup"><span data-stu-id="fe96d-141">16</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe96d-142">A política requer força mínima de Cypher é XTS-AES-256 bit, o nível real de Cypher é mais fraco do que isso.</span><span class="sxs-lookup"><span data-stu-id="fe96d-142">Policy requires minimum cypher strength is XTS-AES-256 bit, actual cypher strength is weaker than that.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="fe96d-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fe96d-143">Related topics</span></span>


[<span data-ttu-id="fe96d-144">Referência técnica do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="fe96d-144">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)

[<span data-ttu-id="fe96d-145">Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="fe96d-145">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 
## <span data-ttu-id="fe96d-146">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="fe96d-146">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="fe96d-147">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="fe96d-147">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="fe96d-148">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="fe96d-148">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





