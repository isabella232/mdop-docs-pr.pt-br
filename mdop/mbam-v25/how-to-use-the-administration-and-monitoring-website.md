---
title: Como usar o site Administração e Monitoramento
description: Como usar o site Administração e Monitoramento
author: dansimp
ms.assetid: bb96a4e8-d4f4-4e6f-b7db-82d96998bfa6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b9597e29a5a7a6236cb351d8d6d1f682edce3cf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796151"
---
# <span data-ttu-id="1f585-103">Como usar o site Administração e Monitoramento</span><span class="sxs-lookup"><span data-stu-id="1f585-103">How to Use the Administration and Monitoring Website</span></span>


<span data-ttu-id="1f585-104">O site de administração e monitoramento, também chamado de suporte técnico, é uma interface administrativa para a criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1f585-104">The Administration and Monitoring Website, also referred to as the Help Desk, is an administrative interface for BitLocker Drive Encryption.</span></span> <span data-ttu-id="1f585-105">Use o site para analisar relatórios, recuperar as unidades de usuários finais e gerenciar os usuários finais TPMs, conforme descrito nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f585-105">Use the website to review reports, recover end users’ drives, and manage end users’ TPMs, as described in the following sections.</span></span>

<span data-ttu-id="1f585-106">**Observação**  Se você estiver usando o MBAM na topologia autônoma, Visualizar todos os relatórios do site Administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="1f585-106">**Note** If you are using MBAM in the Stand-alone topology, you view all reports from the Administration and Monitoring Website.</span></span> <span data-ttu-id="1f585-107">Se você estiver usando a topologia de integração do Configuration Manager, exiba todos os relatórios no Configuration Manager, exceto o relatório de auditoria de recuperação, que você continuará a ver no site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="1f585-107">If you are using the Configuration Manager Integration topology, you view all reports in Configuration Manager, except the Recovery Audit report, which you continue to view from the Administration and Monitoring Website.</span></span> <span data-ttu-id="1f585-108">Para obter mais informações sobre relatórios, consulte [monitoramento e relatórios de conformidade do BitLocker com o MBAM 2,5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="1f585-108">For more information about reports, see [Monitoring and Reporting BitLocker Compliance with MBAM 2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md).</span></span>

 

## <span data-ttu-id="1f585-109">Funções necessárias para usar o site de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="1f585-109">Required roles for using the Administration and Monitoring Website</span></span>


<span data-ttu-id="1f585-110">Para acessar áreas específicas do site de administração e monitoramento, você deve ter uma das funções a seguir, que são grupos que você cria no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1f585-110">To access specific areas of the Administration and Monitoring Website, you must have one of the following roles, which are groups that you create in Active Directory.</span></span> <span data-ttu-id="1f585-111">Você pode usar qualquer nome para estes grupos.</span><span class="sxs-lookup"><span data-stu-id="1f585-111">You can use any name for these groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1f585-112">Account</span><span class="sxs-lookup"><span data-stu-id="1f585-112">Account</span></span></th>
<th align="left"><span data-ttu-id="1f585-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f585-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1f585-114">Usuários avançados da assistência técnica MBAM</span><span class="sxs-lookup"><span data-stu-id="1f585-114">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f585-115">Fornece acesso a todas as áreas do site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="1f585-115">Provides access to all areas of the Administration and Monitoring Website.</span></span> <span data-ttu-id="1f585-116">Os usuários que têm essa função só inserem a chave de recuperação, e não o nome de usuário e o domínio do usuário final, ao ajudar os usuários finais a recuperarem suas unidades.</span><span class="sxs-lookup"><span data-stu-id="1f585-116">Users who have this role enter only the recovery key, and not the end user’s domain and user name, when helping end users recover their drives.</span></span> <span data-ttu-id="1f585-117">Se um usuário for membro do grupo usuários da assistência técnica do MBAM e do grupo usuários avançados do MBAM helpdesk, as permissões do grupo usuários da assistência avançada do MBAM substituirão as permissões do grupo usuários da assistência técnica do MBAM.</span><span class="sxs-lookup"><span data-stu-id="1f585-117">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Users Group permissions.</span></span></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1f585-118">Usuários da assistência técnica MBAM</span><span class="sxs-lookup"><span data-stu-id="1f585-118">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f585-119">Fornece acesso às áreas gerenciar TPM e recuperação de unidade do site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="1f585-119">Provides access to the Manage TPM and Drive Recovery areas of the Administration and Monitoring Website.</span></span> <span data-ttu-id="1f585-120">As pessoas que têm essa função devem preencher todos os campos, incluindo o nome do domínio e o nome da conta do usuário final, quando eles usam uma área.</span><span class="sxs-lookup"><span data-stu-id="1f585-120">Individuals who have this role must fill in all fields, including the end-user’s domain and account name, when they use either area.</span></span></p>
<p><span data-ttu-id="1f585-121">Se um usuário for membro do grupo usuários da assistência técnica do MBAM e do grupo usuários avançados do MBAM helpdesk, as permissões do grupo usuários da assistência avançada do MBAM substituirão as permissões do grupo usuários da assistência técnica do MBAM.</span><span class="sxs-lookup"><span data-stu-id="1f585-121">If a user is a member of both the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Users Group permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1f585-122">Usuários do relatório MBAM</span><span class="sxs-lookup"><span data-stu-id="1f585-122">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f585-123">Fornece acesso aos relatórios na <strong> </strong> área relatórios do site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="1f585-123">Provides access to the reports in the <strong>Reports</strong> area of the Administration and Monitoring Website.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1f585-124">Tarefas que você pode executar no site Administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="1f585-124">Tasks you can perform on the Administration and Monitoring Website</span></span>


<span data-ttu-id="1f585-125">A tabela a seguir resume as tarefas que você pode executar no site de administração e monitoramento e fornece links para obter mais informações sobre cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="1f585-125">The following table summarizes the tasks you can perform on the Administration and Monitoring Website and provides links to more information about each task.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1f585-126">Tarefa</span><span class="sxs-lookup"><span data-stu-id="1f585-126">Task</span></span></th>
<th align="left"><span data-ttu-id="1f585-127">Área do site na qual você acessa a tarefa</span><span class="sxs-lookup"><span data-stu-id="1f585-127">Area of the Website where you access the task</span></span></th>
<th align="left"><span data-ttu-id="1f585-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f585-128">Description</span></span></th>
<th align="left"><span data-ttu-id="1f585-129">Para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="1f585-129">For more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1f585-130">Consulte os relatórios</span><span class="sxs-lookup"><span data-stu-id="1f585-130">View reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f585-131">Relatórios</span><span class="sxs-lookup"><span data-stu-id="1f585-131">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f585-132">Permite que você execute relatórios para monitorar o uso do BitLocker, a conformidade e a atividade de recuperação de chave.</span><span class="sxs-lookup"><span data-stu-id="1f585-132">Enables you to run reports to monitor BitLocker usage, compliance, and key recovery activity.</span></span> <span data-ttu-id="1f585-133">Os relatórios fornecem dados sobre conformidade com a empresa, computadores individuais e quem solicitou as chaves de recuperação ou o pacote OwnerAuth do TPM para um computador específico.</span><span class="sxs-lookup"><span data-stu-id="1f585-133">Reports provide data about enterprise compliance, individual computers, and who requested recovery keys or the TPM OwnerAuth package for a specific computer.</span></span></p></td>
<td align="left"><p><a href="viewing-mbam-25-reports-for-the-stand-alone-topology.md" data-raw-source="[Viewing MBAM 2.5 Reports for the Stand-alone Topology](viewing-mbam-25-reports-for-the-stand-alone-topology.md)"><span data-ttu-id="1f585-134">Exibindo relatórios do MBAM 2.5 referentes à topologia autônoma</span><span class="sxs-lookup"><span data-stu-id="1f585-134">Viewing MBAM 2.5 Reports for the Stand-alone Topology</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1f585-135">Determinar o status de criptografia BitLocker de computadores perdidos ou roubados</span><span class="sxs-lookup"><span data-stu-id="1f585-135">Determine the BitLocker encryption status of lost or stolen computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f585-136">Relatórios</span><span class="sxs-lookup"><span data-stu-id="1f585-136">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f585-137">Determine se um volume foi criptografado se o computador for perdido ou roubado.</span><span class="sxs-lookup"><span data-stu-id="1f585-137">Determine if a volume was encrypted if the computer is lost or stolen.</span></span></p></td>
<td align="left"><p><a href="how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md" data-raw-source="[How to Determine BitLocker Encryption State of Lost Computers](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)"><span data-ttu-id="1f585-138">Como determinar o estado de criptografia BitLocker de computadores perdidos</span><span class="sxs-lookup"><span data-stu-id="1f585-138">How to Determine BitLocker Encryption State of Lost Computers</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1f585-139">Recuperar drives perdidos</span><span class="sxs-lookup"><span data-stu-id="1f585-139">Recover lost drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f585-140">Recuperação de unidade</span><span class="sxs-lookup"><span data-stu-id="1f585-140">Drive Recovery</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f585-141">Recuperar unidades que são:</span><span class="sxs-lookup"><span data-stu-id="1f585-141">Recover drives that are:</span></span></p>
<ul>
<li><p><span data-ttu-id="1f585-142">No modo de recuperação</span><span class="sxs-lookup"><span data-stu-id="1f585-142">In recovery mode</span></span></p></li>
<li><p><span data-ttu-id="1f585-143">Foram movidos</span><span class="sxs-lookup"><span data-stu-id="1f585-143">Have been moved</span></span></p></li>
<li><p><span data-ttu-id="1f585-144">Estão corrompidos</span><span class="sxs-lookup"><span data-stu-id="1f585-144">Are corrupted</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><a href="how-to-recover-a-drive-in-recovery-mode-mbam-25.md" data-raw-source="[How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)"><span data-ttu-id="1f585-145">Como recuperar uma unidade no modo de recuperação</span><span class="sxs-lookup"><span data-stu-id="1f585-145">How to Recover a Drive in Recovery Mode</span></span></a></p></li>
<li><p><a href="how-to-recover-a-moved-drive-mbam-25.md" data-raw-source="[How to Recover a Moved Drive](how-to-recover-a-moved-drive-mbam-25.md)"><span data-ttu-id="1f585-146">Como recuperar uma unidade movida</span><span class="sxs-lookup"><span data-stu-id="1f585-146">How to Recover a Moved Drive</span></span></a></p></li>
<li><p><a href="how-to-recover-a-corrupted-drive-mbam-25.md" data-raw-source="[How to Recover a Corrupted Drive](how-to-recover-a-corrupted-drive-mbam-25.md)"><span data-ttu-id="1f585-147">Como recuperar uma unidade corrompida</span><span class="sxs-lookup"><span data-stu-id="1f585-147">How to Recover a Corrupted Drive</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1f585-148">Redefinir um bloqueio de TPM</span><span class="sxs-lookup"><span data-stu-id="1f585-148">Reset a TPM lockout</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f585-149">Gerenciar TPM</span><span class="sxs-lookup"><span data-stu-id="1f585-149">Manage TPM</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f585-150">Fornece acesso a dados do TPM que foram coletados pelo cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="1f585-150">Provides access to TPM data that has been collected by the MBAM Client.</span></span> <span data-ttu-id="1f585-151">Em um bloqueio de TPM, use o site Administração e monitoramento para recuperar o arquivo de senha necessário para desbloquear o TPM.</span><span class="sxs-lookup"><span data-stu-id="1f585-151">In a TPM lockout, use the Administration and Monitoring Website to retrieve the necessary password file to unlock the TPM.</span></span></p></td>
<td align="left"><p><a href="how-to-reset-a-tpm-lockout-mbam-25.md" data-raw-source="[How to Reset a TPM Lockout](how-to-reset-a-tpm-lockout-mbam-25.md)"><span data-ttu-id="1f585-152">Como redefinir um bloqueio de TPM</span><span class="sxs-lookup"><span data-stu-id="1f585-152">How to Reset a TPM Lockout</span></span></a></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="1f585-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1f585-153">Related topics</span></span>


[<span data-ttu-id="1f585-154">Realizando o gerenciamento do BitLocker com o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1f585-154">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 

## <span data-ttu-id="1f585-155">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="1f585-155">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="1f585-156">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="1f585-156">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="1f585-157">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="1f585-157">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





