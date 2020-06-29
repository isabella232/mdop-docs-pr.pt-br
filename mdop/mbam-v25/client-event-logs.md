---
title: Logs de eventos do cliente
description: Logs de eventos do cliente
author: dansimp
ms.assetid: d5c2f270-db6a-45f1-8557-8c6fb28fd568
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7324d07bf018944fcbe24168bba2e9abea9cea41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799423"
---
# <span data-ttu-id="ac60e-103">Logs de eventos do cliente</span><span class="sxs-lookup"><span data-stu-id="ac60e-103">Client Event Logs</span></span>

<span data-ttu-id="ac60e-104">Os logs de eventos do cliente MBAM estão localizados em Visualizador de eventos – logs de aplicativos e serviços – Microsoft – Windows – MBAM-caminho operacional.</span><span class="sxs-lookup"><span data-stu-id="ac60e-104">MBAM Client event logs are located in Event Viewer – Applications and Services Logs – Microsoft – Windows – MBAM - Operational path.</span></span>
<span data-ttu-id="ac60e-105">A tabela a seguir contém as identificações de eventos que podem ocorrer no cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="ac60e-105">The following table contains event IDs that can occur on the MBAM Client.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ac60e-106">ID do evento</span><span class="sxs-lookup"><span data-stu-id="ac60e-106">Event ID</span></span></th>
<th align="left"><span data-ttu-id="ac60e-107">Canal</span><span class="sxs-lookup"><span data-stu-id="ac60e-107">Channel</span></span></th>
<th align="left"><span data-ttu-id="ac60e-108">Símbolo de evento</span><span class="sxs-lookup"><span data-stu-id="ac60e-108">Event symbol</span></span></th>
<th align="left"><span data-ttu-id="ac60e-109">Mensagem</span><span class="sxs-lookup"><span data-stu-id="ac60e-109">Message</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac60e-110">um</span><span class="sxs-lookup"><span data-stu-id="ac60e-110">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-111">Operacionais</span><span class="sxs-lookup"><span data-stu-id="ac60e-111">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-112">VolumeEnactmentSuccessful</span><span class="sxs-lookup"><span data-stu-id="ac60e-112">VolumeEnactmentSuccessful</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-113">As políticas de MBAM foram aplicadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="ac60e-113">The MBAM policies were applied successfully.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac60e-114">2</span><span class="sxs-lookup"><span data-stu-id="ac60e-114">2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-115">Administrador</span><span class="sxs-lookup"><span data-stu-id="ac60e-115">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-116">VolumeEnactmentFailed</span><span class="sxs-lookup"><span data-stu-id="ac60e-116">VolumeEnactmentFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-117">Ocorreu um erro ao aplicar políticas de MBAM.</span><span class="sxs-lookup"><span data-stu-id="ac60e-117">An error occurred while applying MBAM policies.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac60e-118">3D</span><span class="sxs-lookup"><span data-stu-id="ac60e-118">3</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-119">Operacionais</span><span class="sxs-lookup"><span data-stu-id="ac60e-119">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-120">TransferStatusDataSuccessful</span><span class="sxs-lookup"><span data-stu-id="ac60e-120">TransferStatusDataSuccessful</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-121">Os dados do status de criptografia foram enviados com êxito.</span><span class="sxs-lookup"><span data-stu-id="ac60e-121">The encryption status data was sent successfully.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac60e-122">4</span><span class="sxs-lookup"><span data-stu-id="ac60e-122">4</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-123">Administrador</span><span class="sxs-lookup"><span data-stu-id="ac60e-123">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-124">TransferStatusDataFailed</span><span class="sxs-lookup"><span data-stu-id="ac60e-124">TransferStatusDataFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-125">Ocorreu um erro ao enviar dados de status de criptografia.</span><span class="sxs-lookup"><span data-stu-id="ac60e-125">An error occurred while sending encryption status data.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac60e-126">08</span><span class="sxs-lookup"><span data-stu-id="ac60e-126">8</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-127">Administrador</span><span class="sxs-lookup"><span data-stu-id="ac60e-127">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-128">SystemVolumeNotFound</span><span class="sxs-lookup"><span data-stu-id="ac60e-128">SystemVolumeNotFound</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-129">O volume do sistema está ausente.</span><span class="sxs-lookup"><span data-stu-id="ac60e-129">The system volume is missing.</span></span> <span data-ttu-id="ac60e-130">SystemVolume é necessário para criptografar a unidade do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ac60e-130">SystemVolume is needed to encrypt the operating system drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac60e-131">222</span><span class="sxs-lookup"><span data-stu-id="ac60e-131">9</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-132">Administrador</span><span class="sxs-lookup"><span data-stu-id="ac60e-132">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-133">TPMNotFound</span><span class="sxs-lookup"><span data-stu-id="ac60e-133">TPMNotFound</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-134">O hardware TPM está ausente.</span><span class="sxs-lookup"><span data-stu-id="ac60e-134">The TPM hardware is missing.</span></span> <span data-ttu-id="ac60e-135">É necessário que o TPM criptografe a unidade do sistema operacional com qualquer protetor TPM.</span><span class="sxs-lookup"><span data-stu-id="ac60e-135">TPM is needed to encrypt the operating system drive with any TPM protector.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac60e-136">254</span><span class="sxs-lookup"><span data-stu-id="ac60e-136">10</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-137">Administrador</span><span class="sxs-lookup"><span data-stu-id="ac60e-137">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-138">MachineHWExempted</span><span class="sxs-lookup"><span data-stu-id="ac60e-138">MachineHWExempted</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-139">O computador está isento da criptografia.</span><span class="sxs-lookup"><span data-stu-id="ac60e-139">The computer is exempted from Encryption.</span></span> <span data-ttu-id="ac60e-140">Status de hardware da máquina: isento</span><span class="sxs-lookup"><span data-stu-id="ac60e-140">Machine’s hardware status: Exempted</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac60e-141">11:00</span><span class="sxs-lookup"><span data-stu-id="ac60e-141">11</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-142">Administrador</span><span class="sxs-lookup"><span data-stu-id="ac60e-142">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-143">MachineHWUnknown</span><span class="sxs-lookup"><span data-stu-id="ac60e-143">MachineHWUnknown</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-144">O computador está isento da criptografia.</span><span class="sxs-lookup"><span data-stu-id="ac60e-144">The computer is exempted from encryption.</span></span> <span data-ttu-id="ac60e-145">Status de hardware da máquina: desconhecido</span><span class="sxs-lookup"><span data-stu-id="ac60e-145">Machine’s hardware status: Unknown</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac60e-146">12</span><span class="sxs-lookup"><span data-stu-id="ac60e-146">12</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-147">Administrador</span><span class="sxs-lookup"><span data-stu-id="ac60e-147">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-148">HWCheckFailed</span><span class="sxs-lookup"><span data-stu-id="ac60e-148">HWCheckFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-149">Falha na verificação de isenção de hardware.</span><span class="sxs-lookup"><span data-stu-id="ac60e-149">Hardware exemption check failed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac60e-150">0,13</span><span class="sxs-lookup"><span data-stu-id="ac60e-150">13</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-151">Administrador</span><span class="sxs-lookup"><span data-stu-id="ac60e-151">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-152">UserIsExempted</span><span class="sxs-lookup"><span data-stu-id="ac60e-152">UserIsExempted</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-153">O usuário está isento de criptografia.</span><span class="sxs-lookup"><span data-stu-id="ac60e-153">The user is exempt from encryption.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac60e-154">quatorze</span><span class="sxs-lookup"><span data-stu-id="ac60e-154">14</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-155">Administrador</span><span class="sxs-lookup"><span data-stu-id="ac60e-155">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-156">UserIsWaiting</span><span class="sxs-lookup"><span data-stu-id="ac60e-156">UserIsWaiting</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-157">O usuário solicitou uma isenção.</span><span class="sxs-lookup"><span data-stu-id="ac60e-157">The user requested an exemption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac60e-158">15</span><span class="sxs-lookup"><span data-stu-id="ac60e-158">15</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-159">Administrador</span><span class="sxs-lookup"><span data-stu-id="ac60e-159">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-160">UserExemptionCheckFailed</span><span class="sxs-lookup"><span data-stu-id="ac60e-160">UserExemptionCheckFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-161">Falha na verificação de isenção de usuário.</span><span class="sxs-lookup"><span data-stu-id="ac60e-161">User exemption check failed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac60e-162">16</span><span class="sxs-lookup"><span data-stu-id="ac60e-162">16</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-163">Administrador</span><span class="sxs-lookup"><span data-stu-id="ac60e-163">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-164">Useradiamento</span><span class="sxs-lookup"><span data-stu-id="ac60e-164">UserPostponed</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-165">O usuário adie o processo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="ac60e-165">The user postponed the encryption process.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac60e-166">16</span><span class="sxs-lookup"><span data-stu-id="ac60e-166">17</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-167">Administrador</span><span class="sxs-lookup"><span data-stu-id="ac60e-167">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-168">TPMInitializationFailed</span><span class="sxs-lookup"><span data-stu-id="ac60e-168">TPMInitializationFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-169">Falha na inicialização do TPM.</span><span class="sxs-lookup"><span data-stu-id="ac60e-169">TPM initialization failed.</span></span> <span data-ttu-id="ac60e-170">O usuário rejeitou as mudanças do BIOS.</span><span class="sxs-lookup"><span data-stu-id="ac60e-170">The user rejected the BIOS changes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac60e-171">dezoito</span><span class="sxs-lookup"><span data-stu-id="ac60e-171">18</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-172">Administrador</span><span class="sxs-lookup"><span data-stu-id="ac60e-172">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-173">CoreServiceDown</span><span class="sxs-lookup"><span data-stu-id="ac60e-173">CoreServiceDown</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-174">Não é possível se conectar ao serviço de recuperação e hardware do MBAM.</span><span class="sxs-lookup"><span data-stu-id="ac60e-174">Unable to connect to the MBAM Recovery and Hardware service.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac60e-175">pol</span><span class="sxs-lookup"><span data-stu-id="ac60e-175">19</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-176">Operacionais</span><span class="sxs-lookup"><span data-stu-id="ac60e-176">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-177">CoreServiceUp</span><span class="sxs-lookup"><span data-stu-id="ac60e-177">CoreServiceUp</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-178">Conectado com êxito ao serviço de recuperação e hardware do MBAM.</span><span class="sxs-lookup"><span data-stu-id="ac60e-178">Successfully connected to the MBAM Recovery and Hardware service.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac60e-179">cedido</span><span class="sxs-lookup"><span data-stu-id="ac60e-179">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-180">Administrador</span><span class="sxs-lookup"><span data-stu-id="ac60e-180">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-181">PolicyMismatch</span><span class="sxs-lookup"><span data-stu-id="ac60e-181">PolicyMismatch</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-182">A política MBAM está em conflito ou está corrompida.</span><span class="sxs-lookup"><span data-stu-id="ac60e-182">The MBAM policy is in conflict or corrupt.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac60e-183">21</span><span class="sxs-lookup"><span data-stu-id="ac60e-183">21</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-184">Administrador</span><span class="sxs-lookup"><span data-stu-id="ac60e-184">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-185">ConflictingOSVolumePolicies</span><span class="sxs-lookup"><span data-stu-id="ac60e-185">ConflictingOSVolumePolicies</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-186">Conflito nas políticas de criptografia de volume do so detectado.</span><span class="sxs-lookup"><span data-stu-id="ac60e-186">Detected OS volume encryption policies conflict.</span></span> <span data-ttu-id="ac60e-187">Verifique as políticas de BitLocker e MBAM relacionadas aos protetores de unidade do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ac60e-187">Check BitLocker and MBAM policies related to OS drive protectors.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac60e-188">22</span><span class="sxs-lookup"><span data-stu-id="ac60e-188">22</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-189">Administrador</span><span class="sxs-lookup"><span data-stu-id="ac60e-189">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-190">ConflictingFDDVolumePolicies</span><span class="sxs-lookup"><span data-stu-id="ac60e-190">ConflictingFDDVolumePolicies</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-191">Conflito detectados nas políticas de criptografia de volume da unidade de dados fixas.</span><span class="sxs-lookup"><span data-stu-id="ac60e-191">Detected Fixed Data Drive volume encryption policies conflict.</span></span> <span data-ttu-id="ac60e-192">Verifique as políticas de BitLocker e MBAM relacionadas a protetores de unidade de FDD.</span><span class="sxs-lookup"><span data-stu-id="ac60e-192">Check BitLocker and MBAM policies related to FDD drive protectors.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac60e-193">27</span><span class="sxs-lookup"><span data-stu-id="ac60e-193">27</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-194">Administrador</span><span class="sxs-lookup"><span data-stu-id="ac60e-194">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-195">EncryptionFailedNoDra</span><span class="sxs-lookup"><span data-stu-id="ac60e-195">EncryptionFailedNoDra</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-196">Ocorreu um erro durante a criptografia.</span><span class="sxs-lookup"><span data-stu-id="ac60e-196">An error occurred while encrypting.</span></span> <span data-ttu-id="ac60e-197">Um protetor de agente de recuperação de dados (DRA) é necessário no modo FIPS para máquinas anteriores ao Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="ac60e-197">A Data Recovery Agent (DRA) protector is required in FIPS mode for pre-Windows 8.1 machines.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac60e-198">28</span><span class="sxs-lookup"><span data-stu-id="ac60e-198">28</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-199">Operacionais</span><span class="sxs-lookup"><span data-stu-id="ac60e-199">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-200">TpmOwnerAuthEscrowed</span><span class="sxs-lookup"><span data-stu-id="ac60e-200">TpmOwnerAuthEscrowed</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-201">O TPM OwnerAuth foi reapresentado.</span><span class="sxs-lookup"><span data-stu-id="ac60e-201">The TPM OwnerAuth has been escrowed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac60e-202">anos</span><span class="sxs-lookup"><span data-stu-id="ac60e-202">29</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-203">Operacionais</span><span class="sxs-lookup"><span data-stu-id="ac60e-203">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-204">RecoveryKeyEscrowed</span><span class="sxs-lookup"><span data-stu-id="ac60e-204">RecoveryKeyEscrowed</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-205">A chave de recuperação do BitLocker do volume foi em caução.</span><span class="sxs-lookup"><span data-stu-id="ac60e-205">The BitLocker recovery key for the volume has been escrowed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac60e-206">30</span><span class="sxs-lookup"><span data-stu-id="ac60e-206">30</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-207">Operacionais</span><span class="sxs-lookup"><span data-stu-id="ac60e-207">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-208">RecoveryKeyReset</span><span class="sxs-lookup"><span data-stu-id="ac60e-208">RecoveryKeyReset</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-209">A chave de recuperação do BitLocker do volume foi atualizada.</span><span class="sxs-lookup"><span data-stu-id="ac60e-209">The BitLocker recovery key for the volume has been updated.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac60e-210">31</span><span class="sxs-lookup"><span data-stu-id="ac60e-210">31</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-211">Operacionais</span><span class="sxs-lookup"><span data-stu-id="ac60e-211">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-212">EnforcePolicyDateSet</span><span class="sxs-lookup"><span data-stu-id="ac60e-212">EnforcePolicyDateSet</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-213">A data da política de aplicação, <em> &lt; Data &gt; </em> , foi definida para o volume</span><span class="sxs-lookup"><span data-stu-id="ac60e-213">The enforce policy date, <em>&lt;date&gt;</em>, has been set for the volume</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac60e-214">32</span><span class="sxs-lookup"><span data-stu-id="ac60e-214">32</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-215">Operacionais</span><span class="sxs-lookup"><span data-stu-id="ac60e-215">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-216">EnforcePolicyDateCleared</span><span class="sxs-lookup"><span data-stu-id="ac60e-216">EnforcePolicyDateCleared</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-217">A data da política de aplicação, <em> &lt; Data &gt; </em> , foi limpa para o volume.</span><span class="sxs-lookup"><span data-stu-id="ac60e-217">The enforce policy date, <em>&lt;date&gt;</em>, has been cleared for the volume.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac60e-218">33</span><span class="sxs-lookup"><span data-stu-id="ac60e-218">33</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-219">Operacionais</span><span class="sxs-lookup"><span data-stu-id="ac60e-219">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-220">TpmLockOutResetSucceeded</span><span class="sxs-lookup"><span data-stu-id="ac60e-220">TpmLockOutResetSucceeded</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-221">O bloqueio do TPM foi redefinido com êxito.</span><span class="sxs-lookup"><span data-stu-id="ac60e-221">Successfully reset TPM lockout.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac60e-222">34</span><span class="sxs-lookup"><span data-stu-id="ac60e-222">34</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-223">Administrador</span><span class="sxs-lookup"><span data-stu-id="ac60e-223">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-224">TpmLockOutResetFailed</span><span class="sxs-lookup"><span data-stu-id="ac60e-224">TpmLockOutResetFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-225">Falha ao redefinir o bloqueio do TPM.</span><span class="sxs-lookup"><span data-stu-id="ac60e-225">Failed to reset TPM lockout.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac60e-226">35</span><span class="sxs-lookup"><span data-stu-id="ac60e-226">35</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-227">Operacionais</span><span class="sxs-lookup"><span data-stu-id="ac60e-227">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-228">TpmOwnerAuthRetrievalSucceeded</span><span class="sxs-lookup"><span data-stu-id="ac60e-228">TpmOwnerAuthRetrievalSucceeded</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-229">OwnerAuth de TPM recuperados com êxito dos serviços do MBAM.</span><span class="sxs-lookup"><span data-stu-id="ac60e-229">Successfully retrieved TPM OwnerAuth from MBAM services.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac60e-230">36</span><span class="sxs-lookup"><span data-stu-id="ac60e-230">36</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-231">Administrador</span><span class="sxs-lookup"><span data-stu-id="ac60e-231">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-232">TpmOwnerAuthRetrievalFailed</span><span class="sxs-lookup"><span data-stu-id="ac60e-232">TpmOwnerAuthRetrievalFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-233">Falha ao recuperar o TPM OwnerAuth dos serviços do MBAM.</span><span class="sxs-lookup"><span data-stu-id="ac60e-233">Failed to retrieve TPM OwnerAuth from MBAM services.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac60e-234">37</span><span class="sxs-lookup"><span data-stu-id="ac60e-234">37</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-235">Administrador</span><span class="sxs-lookup"><span data-stu-id="ac60e-235">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-236">WmiProviderDllSearchPathUpdateFailed</span><span class="sxs-lookup"><span data-stu-id="ac60e-236">WmiProviderDllSearchPathUpdateFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-237">Falha ao atualizar o caminho de pesquisa de DLL para o provedor WMI.</span><span class="sxs-lookup"><span data-stu-id="ac60e-237">Failed to update the DLL search path for WMI provider.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac60e-238">38</span><span class="sxs-lookup"><span data-stu-id="ac60e-238">38</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-239">Administrador</span><span class="sxs-lookup"><span data-stu-id="ac60e-239">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-240">TimedOutWaitingForWmiProvider</span><span class="sxs-lookup"><span data-stu-id="ac60e-240">TimedOutWaitingForWmiProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-241">Agente interrompido-tempo limite esgotado ao aguardar a instância do provedor WMI MBAM.</span><span class="sxs-lookup"><span data-stu-id="ac60e-241">Agent Stopping - Timed-out waiting for MBAM WMI Provider Instance.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac60e-242">39</span><span class="sxs-lookup"><span data-stu-id="ac60e-242">39</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-243">Operacionais</span><span class="sxs-lookup"><span data-stu-id="ac60e-243">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-244">RemovableDriveMounted</span><span class="sxs-lookup"><span data-stu-id="ac60e-244">RemovableDriveMounted</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-245">A unidade removível foi montada.</span><span class="sxs-lookup"><span data-stu-id="ac60e-245">Removable drive was mounted.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac60e-246">40</span><span class="sxs-lookup"><span data-stu-id="ac60e-246">40</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-247">Operacionais</span><span class="sxs-lookup"><span data-stu-id="ac60e-247">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-248">RemovableDriveDismounted</span><span class="sxs-lookup"><span data-stu-id="ac60e-248">RemovableDriveDismounted</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-249">A unidade removível foi desmontada.</span><span class="sxs-lookup"><span data-stu-id="ac60e-249">Removable drive was unmounted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac60e-250">41</span><span class="sxs-lookup"><span data-stu-id="ac60e-250">41</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-251">Operacionais</span><span class="sxs-lookup"><span data-stu-id="ac60e-251">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-252">FailedToEnactEndpointUnreachable</span><span class="sxs-lookup"><span data-stu-id="ac60e-252">FailedToEnactEndpointUnreachable</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-253">Falha na conexão com o serviço de recuperação e recuperação do MBAM impedia a aplicação bem-sucedida das políticas do MBAM ao volume.</span><span class="sxs-lookup"><span data-stu-id="ac60e-253">Failure to connect to the MBAM Recovery and Hardware service prevented MBAM policies from being applied successfully to the volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ac60e-254">42</span><span class="sxs-lookup"><span data-stu-id="ac60e-254">42</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-255">Operacionais</span><span class="sxs-lookup"><span data-stu-id="ac60e-255">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-256">FailedToEnactLockedVolume</span><span class="sxs-lookup"><span data-stu-id="ac60e-256">FailedToEnactLockedVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-257">Estado do volume bloqueado impedia a aplicação bem-sucedida das políticas de MBAM ao volume.</span><span class="sxs-lookup"><span data-stu-id="ac60e-257">Locked volume state prevented MBAM policies from being applied successfully to the volume.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ac60e-258">43</span><span class="sxs-lookup"><span data-stu-id="ac60e-258">43</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-259">Operacionais</span><span class="sxs-lookup"><span data-stu-id="ac60e-259">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-260">TransferStatusDataFailedEndpointUnreachable</span><span class="sxs-lookup"><span data-stu-id="ac60e-260">TransferStatusDataFailedEndpointUnreachable</span></span></p></td>
<td align="left"><p><span data-ttu-id="ac60e-261">Falha ao se conectar ao serviço de conformidade e status da MBAM impedia a transferência de dados de status de criptografia.</span><span class="sxs-lookup"><span data-stu-id="ac60e-261">Failure to connect to the MBAM Compliance and Status service prevented the transfer of encryption status data.</span></span></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="ac60e-262">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac60e-262">Related topics</span></span>
[<span data-ttu-id="ac60e-263">Referência técnica do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ac60e-263">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)

[<span data-ttu-id="ac60e-264">Logs de eventos do servidor</span><span class="sxs-lookup"><span data-stu-id="ac60e-264">Server Event Logs</span></span>](server-event-logs.md)

 


## <span data-ttu-id="ac60e-265">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="ac60e-265">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="ac60e-266">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="ac60e-266">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="ac60e-267">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="ac60e-267">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





