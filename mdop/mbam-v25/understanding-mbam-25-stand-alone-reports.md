---
title: Noções básicas sobre relatórios autônomos do MBAM 2.5
description: Noções básicas sobre relatórios autônomos do MBAM 2.5
author: dansimp
ms.assetid: 78b5aaf4-8257-4722-8eb9-e0de48db6a11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45e84c7c3b2bcb1602890c7c5a09592324da691e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796084"
---
# <span data-ttu-id="034bd-103">Noções básicas sobre relatórios autônomos do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="034bd-103">Understanding MBAM 2.5 Stand-alone Reports</span></span>


<span data-ttu-id="034bd-104">Este tópico descreve os relatórios que estão disponíveis quando você está executando o Microsoft BitLocker Administration and Monitoring (MBAM) na topologia autônoma.</span><span class="sxs-lookup"><span data-stu-id="034bd-104">This topic describes the reports that are available when you are running Microsoft BitLocker Administration and Monitoring (MBAM) in the Stand-alone topology.</span></span>

**<span data-ttu-id="034bd-105">Observação</span><span class="sxs-lookup"><span data-stu-id="034bd-105">Note</span></span>**  
<span data-ttu-id="034bd-106">Se você estiver executando o MBAM com a topologia de integração do Configuration Manager, gere relatórios do Configuration Manager em vez de MBAM.</span><span class="sxs-lookup"><span data-stu-id="034bd-106">If you are running MBAM with the Configuration Manager Integration topology, you generate reports from Configuration Manager rather than from MBAM.</span></span> <span data-ttu-id="034bd-107">Consulte [exibindo relatórios do MBAM 2,5 para a topologia de integração do Configuration Manager](viewing-mbam-25-reports-for-the-configuration-manager-integration-topology.md) para obter mais informações sobre esses relatórios.</span><span class="sxs-lookup"><span data-stu-id="034bd-107">See [Viewing MBAM 2.5 Reports for the Configuration Manager Integration Topology](viewing-mbam-25-reports-for-the-configuration-manager-integration-topology.md) for more information about these reports.</span></span>



## <span data-ttu-id="034bd-108">Compreendendo os relatórios de topologia autônomo do MBAM</span><span class="sxs-lookup"><span data-stu-id="034bd-108">Understanding the MBAM Stand-alone topology reports</span></span>


<span data-ttu-id="034bd-109">O MBAM fornece três tipos de relatório que você pode usar para monitorar a conformidade do BitLocker com a sua organização:</span><span class="sxs-lookup"><span data-stu-id="034bd-109">MBAM provides three report types that you can use to monitor your organization for BitLocker compliance:</span></span>

-   [<span data-ttu-id="034bd-110">Relatório de conformidade empresarial</span><span class="sxs-lookup"><span data-stu-id="034bd-110">Enterprise Compliance Report</span></span>](#bkmk-enterprisecompliance)

-   [<span data-ttu-id="034bd-111">Relatório de conformidade do computador</span><span class="sxs-lookup"><span data-stu-id="034bd-111">Computer Compliance Report</span></span>](#bkmk-compliance)

-   [<span data-ttu-id="034bd-112">Relatório de auditoria de recuperação</span><span class="sxs-lookup"><span data-stu-id="034bd-112">Recovery Audit Report</span></span>](#bkmk-recovery)

<span data-ttu-id="034bd-113">Para acessar relatórios do MBAM quando você estiver executando o MBAM na topologia autônoma, abra um navegador da Web e, em seguida, abra o site Administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="034bd-113">To access MBAM reports when you are running MBAM in the Stand-alone topology, open a web browser, and then open the Administration and Monitoring Website.</span></span> <span data-ttu-id="034bd-114">Selecione **relatórios** na barra de menus à esquerda.</span><span class="sxs-lookup"><span data-stu-id="034bd-114">Select **Reports** in the left menu bar.</span></span> <span data-ttu-id="034bd-115">Na barra de menus superior, selecione o tipo de relatório que você deseja gerar.</span><span class="sxs-lookup"><span data-stu-id="034bd-115">From the top menu bar, select the kind of report that you want to generate.</span></span> <span data-ttu-id="034bd-116">Para obter mais informações sobre como gerar esses relatórios, consulte [gerando relatórios autônomos do MBAM 2,5](generating-mbam-25-stand-alone-reports.md).</span><span class="sxs-lookup"><span data-stu-id="034bd-116">For more information about generating these reports, see [Generating MBAM 2.5 Stand-alone Reports](generating-mbam-25-stand-alone-reports.md).</span></span>

### <a href="" id="bkmk-enterprisecompliance"></a><span data-ttu-id="034bd-117">Relatório de conformidade empresarial</span><span class="sxs-lookup"><span data-stu-id="034bd-117">Enterprise Compliance Report</span></span>

<span data-ttu-id="034bd-118">Use esse tipo de relatório para coletar informações sobre a conformidade geral do BitLocker em sua organização.</span><span class="sxs-lookup"><span data-stu-id="034bd-118">Use this report type to collect information about overall BitLocker compliance in your organization.</span></span> <span data-ttu-id="034bd-119">Você pode usar filtros para restringir os resultados da pesquisa para saber mais sobre o estado de conformidade e o status de erro dos computadores em sua organização.</span><span class="sxs-lookup"><span data-stu-id="034bd-119">You can use filters to narrow your search results to learn more about the compliance state and error status of computers in your organization.</span></span>

**<span data-ttu-id="034bd-120">Visão geral da conformidade corporativa</span><span class="sxs-lookup"><span data-stu-id="034bd-120">Enterprise Compliance Overview</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="034bd-121">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="034bd-121">Column Name</span></span></th>
<th align="left"><span data-ttu-id="034bd-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="034bd-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-123">Computadores gerenciados</span><span class="sxs-lookup"><span data-stu-id="034bd-123">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-124">Número de computadores que o MBAM gerencia.</span><span class="sxs-lookup"><span data-stu-id="034bd-124">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-125">% Compatível</span><span class="sxs-lookup"><span data-stu-id="034bd-125">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-126">Porcentagem de computadores compatíveis na empresa.</span><span class="sxs-lookup"><span data-stu-id="034bd-126">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-127">% Não compatível</span><span class="sxs-lookup"><span data-stu-id="034bd-127">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-128">Porcentagem de computadores não compatíveis na empresa.</span><span class="sxs-lookup"><span data-stu-id="034bd-128">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-129">% De isenção</span><span class="sxs-lookup"><span data-stu-id="034bd-129">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-130">Porcentagem de computadores isentos do requisito de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="034bd-130">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-131">% Não isenta</span><span class="sxs-lookup"><span data-stu-id="034bd-131">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-132">Porcentagem de computadores que não estão isentos do requisito de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="034bd-132">Percentage of computers not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-133">CLS</span><span class="sxs-lookup"><span data-stu-id="034bd-133">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-134">Porcentagem de computadores compatíveis na empresa.</span><span class="sxs-lookup"><span data-stu-id="034bd-134">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-135">Não compatível</span><span class="sxs-lookup"><span data-stu-id="034bd-135">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-136">Porcentagem de computadores não compatíveis na empresa.</span><span class="sxs-lookup"><span data-stu-id="034bd-136">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-137">Isentos</span><span class="sxs-lookup"><span data-stu-id="034bd-137">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-138">Total de computadores isentos do requisito de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="034bd-138">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-139">Não isento</span><span class="sxs-lookup"><span data-stu-id="034bd-139">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-140">Total de computadores que não estão isentos do requisito de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="034bd-140">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="034bd-141">Detalhes do computador de conformidade empresarial</span><span class="sxs-lookup"><span data-stu-id="034bd-141">Enterprise Compliance Computer Details</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="034bd-142">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="034bd-142">Column Name</span></span></th>
<th align="left"><span data-ttu-id="034bd-143">Descrição</span><span class="sxs-lookup"><span data-stu-id="034bd-143">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-144">Nome do computador</span><span class="sxs-lookup"><span data-stu-id="034bd-144">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-145">Nome DNS especificado pelo usuário que é gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="034bd-145">User-specified DNS name that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-146">Nome de domínio</span><span class="sxs-lookup"><span data-stu-id="034bd-146">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-147">Nome de domínio totalmente qualificado em que o computador cliente reside e é gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="034bd-147">Fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-148">Status de conformidade</span><span class="sxs-lookup"><span data-stu-id="034bd-148">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-149">Estado de conformidade do computador, de acordo com a política especificada para o computador.</span><span class="sxs-lookup"><span data-stu-id="034bd-149">State of compliance for the computer, according to the policy specified for the computer.</span></span> <span data-ttu-id="034bd-150">Os Estados são compatíveis e não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="034bd-150">The states are Noncompliant and Compliant.</span></span> <span data-ttu-id="034bd-151">Consulte a tabela Estados de conformidade de relatório de conformidade empresarial a seguir para obter mais informações sobre como interpretar Estados de conformidade.</span><span class="sxs-lookup"><span data-stu-id="034bd-151">See the following Enterprise Compliance Report Compliance States table for more information about how to interpret compliance states.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-152">Isenção</span><span class="sxs-lookup"><span data-stu-id="034bd-152">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-153">Status que indica se este computador está isento da política BitLocker.</span><span class="sxs-lookup"><span data-stu-id="034bd-153">Status that indicates whether this computer is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-154">Detalhes do status de conformidade</span><span class="sxs-lookup"><span data-stu-id="034bd-154">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-155">Mensagens de erro e status sobre o estado de conformidade do computador de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="034bd-155">Error and status messages about the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-156">Último contato</span><span class="sxs-lookup"><span data-stu-id="034bd-156">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-157">Data e hora em que o computador contatou o servidor pela última vez para informar o status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="034bd-157">Date and time when the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="034bd-158">A frequência do contato é configurável.</span><span class="sxs-lookup"><span data-stu-id="034bd-158">The contact frequency is configurable.</span></span> <span data-ttu-id="034bd-159">Para obter mais informações, consulte as configurações de política de grupo do MBAM.</span><span class="sxs-lookup"><span data-stu-id="034bd-159">For more information, see the MBAM Group Policy settings.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-compliance"></a><span data-ttu-id="034bd-160">Relatório de conformidade do computador</span><span class="sxs-lookup"><span data-stu-id="034bd-160">Computer Compliance Report</span></span>

<span data-ttu-id="034bd-161">Use esse tipo de relatório para coletar informações específicas a um computador ou usuário.</span><span class="sxs-lookup"><span data-stu-id="034bd-161">Use this report type to collect information that is specific to a computer or user.</span></span>

<span data-ttu-id="034bd-162">Exiba esse relatório clicando no nome do computador no relatório de conformidade empresarial ou digitando o nome do computador no relatório de conformidade do computador.</span><span class="sxs-lookup"><span data-stu-id="034bd-162">View this report by clicking the computer name in the Enterprise Compliance Report, or by typing the computer name in the Computer Compliance Report.</span></span> <span data-ttu-id="034bd-163">Este relatório mostra informações de criptografia detalhadas sobre cada unidade (sistema operacional e unidades de dados fixas) em um computador.</span><span class="sxs-lookup"><span data-stu-id="034bd-163">This report shows detailed encryption information about each drive (operating system and fixed data drives) on a computer.</span></span> <span data-ttu-id="034bd-164">Ele também indica a política aplicada a cada tipo de unidade no computador.</span><span class="sxs-lookup"><span data-stu-id="034bd-164">It also indicates the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="034bd-165">Para ver os detalhes de cada unidade, expanda a entrada nome do computador.</span><span class="sxs-lookup"><span data-stu-id="034bd-165">To view the details of each drive, expand the Computer Name entry.</span></span>

**<span data-ttu-id="034bd-166">Observação</span><span class="sxs-lookup"><span data-stu-id="034bd-166">Note</span></span>**  
<span data-ttu-id="034bd-167">O status da criptografia do volume de dados removível não é mostrado neste relatório.</span><span class="sxs-lookup"><span data-stu-id="034bd-167">Removable Data Volume encryption status is not shown in this report.</span></span>



**<span data-ttu-id="034bd-168">Campos de relatório de conformidade do computador</span><span class="sxs-lookup"><span data-stu-id="034bd-168">Computer Compliance Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="034bd-169">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="034bd-169">Column Name</span></span></th>
<th align="left"><span data-ttu-id="034bd-170">Descrição</span><span class="sxs-lookup"><span data-stu-id="034bd-170">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-171">Nome do computador</span><span class="sxs-lookup"><span data-stu-id="034bd-171">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-172">Nome do computador DNS especificado pelo usuário que é gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="034bd-172">User-specified DNS computer name that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-173">Nome de domínio</span><span class="sxs-lookup"><span data-stu-id="034bd-173">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-174">Nome de domínio totalmente qualificado em que o computador cliente reside e é gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="034bd-174">Fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-175">Tipo de computador</span><span class="sxs-lookup"><span data-stu-id="034bd-175">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-176">Tipo de computador.</span><span class="sxs-lookup"><span data-stu-id="034bd-176">Type of computer.</span></span> <span data-ttu-id="034bd-177">Tipos válidos são não portáteis e portáteis.</span><span class="sxs-lookup"><span data-stu-id="034bd-177">Valid types are Non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-178">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="034bd-178">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-179">Tipo de sistema operacional encontrado no computador cliente que é gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="034bd-179">Operating system type found on the client computer that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-180">Status de conformidade</span><span class="sxs-lookup"><span data-stu-id="034bd-180">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-181">Status geral de conformidade do computador gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="034bd-181">Overall compliance status of the computer that is managed by MBAM.</span></span> <span data-ttu-id="034bd-182">Os Estados válidos são compatíveis e não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="034bd-182">Valid states are Compliant and Noncompliant.</span></span></p>
<p><span data-ttu-id="034bd-183">Observe que o status de conformidade por unidade (veja a tabela a seguir) pode indicar estados de conformidade diferentes.</span><span class="sxs-lookup"><span data-stu-id="034bd-183">Notice that the compliance status per drive (see the following table) may indicate different compliance states.</span></span> <span data-ttu-id="034bd-184">No entanto, esse campo representa o estado de conformidade, de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="034bd-184">However, this field represents that compliance state, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-185">Nível de codificação da política</span><span class="sxs-lookup"><span data-stu-id="034bd-185">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-186">O nível de codificação selecionado pelo administrador durante a especificação da política MBAM (por exemplo, 128-bit com difusor).</span><span class="sxs-lookup"><span data-stu-id="034bd-186">Cipher strength selected by the administrator during MBAM policy specification (for example, 128-bit with diffuser).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-187">Unidade de sistema operacional da política</span><span class="sxs-lookup"><span data-stu-id="034bd-187">Policy Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-188">Indica se a criptografia é necessária para o sistema operacional e mostra o tipo de protetor apropriado.</span><span class="sxs-lookup"><span data-stu-id="034bd-188">Indicates if encryption is required for the operating system and shows the appropriate protector type.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-189">Unidade de dados fixos da política</span><span class="sxs-lookup"><span data-stu-id="034bd-189">Policy-Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-190">Indica se a criptografia é necessária para a unidade de dados fixo.</span><span class="sxs-lookup"><span data-stu-id="034bd-190">Indicates if encryption is required for the fixed data drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-191">Unidade de dados removível de política</span><span class="sxs-lookup"><span data-stu-id="034bd-191">Policy Removable Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-192">Indica se a criptografia é necessária para a unidade removível.</span><span class="sxs-lookup"><span data-stu-id="034bd-192">Indicates if encryption is required for the removable drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-193">Usuários do dispositivo</span><span class="sxs-lookup"><span data-stu-id="034bd-193">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-194">Usuários conhecidos no computador gerenciados pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="034bd-194">Known users on the computer that is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-195">Isenção</span><span class="sxs-lookup"><span data-stu-id="034bd-195">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-196">Status que indica se este computador está isento da política BitLocker.</span><span class="sxs-lookup"><span data-stu-id="034bd-196">Status that indicates whether this computer is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-197">Fabricante</span><span class="sxs-lookup"><span data-stu-id="034bd-197">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-198">Nome do fabricante do computador, como aparece no BIOS do computador.</span><span class="sxs-lookup"><span data-stu-id="034bd-198">Computer manufacturer name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-199">Modelo</span><span class="sxs-lookup"><span data-stu-id="034bd-199">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-200">Nome do modelo do fabricante do computador, como aparece no BIOS do computador.</span><span class="sxs-lookup"><span data-stu-id="034bd-200">Computer manufacturer model name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-201">Detalhes do status de conformidade</span><span class="sxs-lookup"><span data-stu-id="034bd-201">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-202">Mensagens de erro e status sobre o estado de conformidade do computador, de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="034bd-202">Error and status messages about the compliance state of the computer, in accordance with the specified policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-203">Último contato</span><span class="sxs-lookup"><span data-stu-id="034bd-203">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-204">Data e hora em que o computador contatou o servidor pela última vez para informar o status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="034bd-204">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="034bd-205">A frequência do contato é configurável.</span><span class="sxs-lookup"><span data-stu-id="034bd-205">The contact frequency is configurable.</span></span> <span data-ttu-id="034bd-206">Para obter mais informações, consulte as configurações de política de grupo do MBAM.</span><span class="sxs-lookup"><span data-stu-id="034bd-206">For more information, see the MBAM Group Policy settings.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="034bd-207">Campos da unidade do relatório de conformidade do computador</span><span class="sxs-lookup"><span data-stu-id="034bd-207">Computer Compliance Report Drive Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="034bd-208">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="034bd-208">Column Name</span></span></th>
<th align="left"><span data-ttu-id="034bd-209">Descrição</span><span class="sxs-lookup"><span data-stu-id="034bd-209">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-210">Letra da unidade</span><span class="sxs-lookup"><span data-stu-id="034bd-210">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-211">Letra da unidade do computador que foi atribuída à unidade específica pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="034bd-211">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-212">Tipo de unidade</span><span class="sxs-lookup"><span data-stu-id="034bd-212">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-213">Tipo de unidade.</span><span class="sxs-lookup"><span data-stu-id="034bd-213">Type of drive.</span></span> <span data-ttu-id="034bd-214">Os valores válidos são unidade do sistema operacional e unidade de dados fixa.</span><span class="sxs-lookup"><span data-stu-id="034bd-214">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="034bd-215">Esses são drives físicos, em vez de volumes lógicos.</span><span class="sxs-lookup"><span data-stu-id="034bd-215">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-216">Nível de codificação</span><span class="sxs-lookup"><span data-stu-id="034bd-216">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-217">Nível de codificação selecionado pelo administrador durante a especificação da política MBAM.</span><span class="sxs-lookup"><span data-stu-id="034bd-217">Cipher strength selected by the administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-218">Tipo de protetor</span><span class="sxs-lookup"><span data-stu-id="034bd-218">Protector Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-219">Tipo de protetor selecionado por meio da configuração de política de grupo usada para criptografar um sistema operacional ou volume de dados fixos.</span><span class="sxs-lookup"><span data-stu-id="034bd-219">Type of protector selected through the Group Policy setting used to encrypt an operating system or fixed data volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-220">Estado do protetor</span><span class="sxs-lookup"><span data-stu-id="034bd-220">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-221">Indica que o computador que está sendo gerenciado pelo MBAM ativou o tipo de protetor especificado na política.</span><span class="sxs-lookup"><span data-stu-id="034bd-221">Indicates that the computer being managed by MBAM has enabled the protector type that is specified in the policy.</span></span> <span data-ttu-id="034bd-222">Os Estados válidos estão ATIVAdos ou desativados.</span><span class="sxs-lookup"><span data-stu-id="034bd-222">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-223">Estado de criptografia</span><span class="sxs-lookup"><span data-stu-id="034bd-223">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-224">Estado de criptografia da unidade.</span><span class="sxs-lookup"><span data-stu-id="034bd-224">Encryption state of the drive.</span></span> <span data-ttu-id="034bd-225">Os Estados válidos são criptografados, não criptografados e criptografados.</span><span class="sxs-lookup"><span data-stu-id="034bd-225">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-226">Status de conformidade</span><span class="sxs-lookup"><span data-stu-id="034bd-226">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-227">Estado que indica se a unidade está de acordo com a política.</span><span class="sxs-lookup"><span data-stu-id="034bd-227">State that indicates whether the drive is in accordance with the policy.</span></span> <span data-ttu-id="034bd-228">Os Estados são compatíveis e não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="034bd-228">States are Noncompliant and Compliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-229">Detalhes do status de conformidade</span><span class="sxs-lookup"><span data-stu-id="034bd-229">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-230">Mensagens de erro e status do estado de conformidade do computador, de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="034bd-230">Error and status messages of the compliance state of the computer, according to the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-recovery"></a><span data-ttu-id="034bd-231">Relatório de auditoria de recuperação</span><span class="sxs-lookup"><span data-stu-id="034bd-231">Recovery Audit Report</span></span>

<span data-ttu-id="034bd-232">Use esse tipo de relatório para auditar os usuários que solicitaram acesso às chaves de recuperação do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="034bd-232">Use this report type to audit users who have requested access to BitLocker recovery keys.</span></span> <span data-ttu-id="034bd-233">O relatório oferece vários filtros com base nos critérios de filtragem desejados.</span><span class="sxs-lookup"><span data-stu-id="034bd-233">The report offers several filters based on the desired filtering criteria.</span></span> <span data-ttu-id="034bd-234">Você pode filtrar por um tipo específico de usuário (um usuário de suporte técnico ou um usuário final), se a solicitação foi bem-sucedida, se a solicitação foi bem-sucedida, o tipo específico de chave solicitada e um intervalo de datas durante o qual ocorreu a recuperação.</span><span class="sxs-lookup"><span data-stu-id="034bd-234">You can filter on a specific type of user (a Help Desk user or an end user), whether the request failed or was successful, the specific type of key requested, and a date range during which the retrieval occurred.</span></span>

**<span data-ttu-id="034bd-235">Campos de relatório de auditoria de recuperação</span><span class="sxs-lookup"><span data-stu-id="034bd-235">Recovery Audit Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="034bd-236">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="034bd-236">Column Name</span></span></th>
<th align="left"><span data-ttu-id="034bd-237">Descrição</span><span class="sxs-lookup"><span data-stu-id="034bd-237">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-238">Data e hora da solicitação</span><span class="sxs-lookup"><span data-stu-id="034bd-238">Request Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-239">Data e hora em que uma solicitação de recuperação de chave foi feita por um usuário final ou usuário de suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="034bd-239">Date and time that a key retrieval request was made by an end user or Help Desk user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-240">Fonte de solicitação de auditoria</span><span class="sxs-lookup"><span data-stu-id="034bd-240">Audit Request Source</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-241">O site a partir do qual a solicitação foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="034bd-241">The site from which the request was initiated.</span></span> <span data-ttu-id="034bd-242">Essa entrada terá um dos dois valores: <strong> portal de autoatendimento </strong> ou <strong> assistência técnica </strong> .</span><span class="sxs-lookup"><span data-stu-id="034bd-242">This entry will have one of two values: <strong>Self-Service Portal</strong> or <strong>Helpdesk</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-243">Status da solicitação</span><span class="sxs-lookup"><span data-stu-id="034bd-243">Request Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-244">Status da solicitação.</span><span class="sxs-lookup"><span data-stu-id="034bd-244">Status of the request.</span></span> <span data-ttu-id="034bd-245">Status válidos são bem-sucedidos (a chave foi recuperada) ou falhou (a tecla não foi recuperada).</span><span class="sxs-lookup"><span data-stu-id="034bd-245">Valid statuses are Successful (the key was retrieved), or Failed (the key was not retrieved).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-246">Usuário da assistência técnica</span><span class="sxs-lookup"><span data-stu-id="034bd-246">Helpdesk User</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-247">Usuário de suporte técnico que iniciou a solicitação de recuperação de chave.</span><span class="sxs-lookup"><span data-stu-id="034bd-247">Help Desk user who initiated the request for key retrieval.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="034bd-248">Observação</span><span class="sxs-lookup"><span data-stu-id="034bd-248">Note</span></span></strong><br/><p><span data-ttu-id="034bd-249">Se um usuário avançado da assistência técnica recuperar a chave sem especificar o usuário final, o <strong> campo usuário final </strong> estará em branco.</span><span class="sxs-lookup"><span data-stu-id="034bd-249">If an Advanced Helpdesk User recovers the key without specifying the end user, the <strong>End User</strong> field will be blank.</span></span> <span data-ttu-id="034bd-250">Um usuário da assistência técnica padrão deve especificar o usuário final, e esse usuário será exibido nesse campo.</span><span class="sxs-lookup"><span data-stu-id="034bd-250">A standard Helpdesk User must specify the end user, and that user will appear in this field.</span></span></p>
<p><span data-ttu-id="034bd-251">Uma recuperação por meio do portal de autoatendimento listará o usuário final solicitante, nesse campo e no <strong> campo usuário final </strong> .</span><span class="sxs-lookup"><span data-stu-id="034bd-251">A recovery via the Self-Service Portal will list the requesting end user both in this field and in the <strong>End User</strong> field.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-252">Usuário final</span><span class="sxs-lookup"><span data-stu-id="034bd-252">End User</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-253">Usuário final que iniciou a solicitação de recuperação de chave.</span><span class="sxs-lookup"><span data-stu-id="034bd-253">End user who initiated the request for key retrieval.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-254">Computador</span><span class="sxs-lookup"><span data-stu-id="034bd-254">Computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-255">Nome do computador que foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="034bd-255">Computer name of the computer that was recovered.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="034bd-256">Tipo de chave</span><span class="sxs-lookup"><span data-stu-id="034bd-256">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-257">Tipo de chave que foi solicitada pelo usuário de suporte técnico ou pelo usuário final.</span><span class="sxs-lookup"><span data-stu-id="034bd-257">Type of key that was requested by the Help Desk user or the end user.</span></span> <span data-ttu-id="034bd-258">Os três tipos de chaves que o MBAM coleta são:</span><span class="sxs-lookup"><span data-stu-id="034bd-258">The three types of keys that MBAM collects are:</span></span></p>
<ul>
<li><p><span data-ttu-id="034bd-259">Senha da chave de recuperação (usada para recuperar um computador no modo de recuperação)</span><span class="sxs-lookup"><span data-stu-id="034bd-259">Recovery Key Password (used to recover a computer in recovery mode)</span></span></p></li>
<li><p><span data-ttu-id="034bd-260">ID da chave de recuperação (usada para recuperar um computador no modo de recuperação em nome de outro usuário)</span><span class="sxs-lookup"><span data-stu-id="034bd-260">Recovery Key ID (used to recover a computer in recovery mode on behalf of another user)</span></span></p></li>
<li><p><span data-ttu-id="034bd-261">Hash de senha TPM (usado para recuperar um computador com um TPM bloqueado)</span><span class="sxs-lookup"><span data-stu-id="034bd-261">TPM Password Hash (used to recover a computer with a locked TPM)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="034bd-262">Descrição do motivo</span><span class="sxs-lookup"><span data-stu-id="034bd-262">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="034bd-263">Motivo pelo qual o tipo de chave especificado foi solicitado pelo usuário de suporte técnico ou pelo usuário final.</span><span class="sxs-lookup"><span data-stu-id="034bd-263">Reason the specified key type was requested by the Help Desk user or the end user.</span></span> <span data-ttu-id="034bd-264">Os motivos são especificados nos recursos de recuperação de unidade e gerenciamento de TPM do site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="034bd-264">The reasons are specified in the Drive Recovery and Manage TPM features of the Administration and Monitoring Website.</span></span> <span data-ttu-id="034bd-265">As entradas válidas são texto inserido pelo usuário ou um dos seguintes códigos de motivo:</span><span class="sxs-lookup"><span data-stu-id="034bd-265">The valid entries are user-entered text or one of the following reason codes:</span></span></p>
<ul>
<li><p><span data-ttu-id="034bd-266">Ordem de inicialização do sistema operacional alterada</span><span class="sxs-lookup"><span data-stu-id="034bd-266">Operating System Boot Order changed</span></span></p></li>
<li><p><span data-ttu-id="034bd-267">BIOS alterado</span><span class="sxs-lookup"><span data-stu-id="034bd-267">BIOS Changed</span></span></p></li>
<li><p><span data-ttu-id="034bd-268">Arquivos do sistema operacional alterados</span><span class="sxs-lookup"><span data-stu-id="034bd-268">Operating System files changed</span></span></p></li>
<li><p><span data-ttu-id="034bd-269">Chave de inicialização perdida</span><span class="sxs-lookup"><span data-stu-id="034bd-269">Lost Startup key</span></span></p></li>
<li><p><span data-ttu-id="034bd-270">Perdeu o PIN</span><span class="sxs-lookup"><span data-stu-id="034bd-270">Lost PIN</span></span></p></li>
<li><p><span data-ttu-id="034bd-271">Redefinição de TPM</span><span class="sxs-lookup"><span data-stu-id="034bd-271">TPM Reset</span></span></p></li>
<li><p><span data-ttu-id="034bd-272">Senha perdida</span><span class="sxs-lookup"><span data-stu-id="034bd-272">Lost Passphrase</span></span></p></li>
<li><p><span data-ttu-id="034bd-273">Cartão inteligente perdido</span><span class="sxs-lookup"><span data-stu-id="034bd-273">Lost Smartcard</span></span></p></li>
<li><p><span data-ttu-id="034bd-274">Redefinir o bloqueio de PIN</span><span class="sxs-lookup"><span data-stu-id="034bd-274">Reset PIN lockout</span></span></p></li>
<li><p><span data-ttu-id="034bd-275">Ativar o TPM</span><span class="sxs-lookup"><span data-stu-id="034bd-275">Turn on TPM</span></span></p></li>
<li><p><span data-ttu-id="034bd-276">Desativar o TPM</span><span class="sxs-lookup"><span data-stu-id="034bd-276">Turn off TPM</span></span></p></li>
<li><p><span data-ttu-id="034bd-277">Alterar a senha do TPM</span><span class="sxs-lookup"><span data-stu-id="034bd-277">Change TPM password</span></span></p></li>
<li><p><span data-ttu-id="034bd-278">Limpar TPM</span><span class="sxs-lookup"><span data-stu-id="034bd-278">Clear TPM</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="034bd-279">Observação</span><span class="sxs-lookup"><span data-stu-id="034bd-279">Note</span></span>**  
<span data-ttu-id="034bd-280">Os resultados do relatório podem ser salvos em um arquivo clicando no botão **Exportar** na barra de menus **relatórios** .</span><span class="sxs-lookup"><span data-stu-id="034bd-280">Report results can be saved to a file by clicking the **Export** button on the **Reports** menu bar.</span></span>




## <span data-ttu-id="034bd-281">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="034bd-281">Related topics</span></span>


[<span data-ttu-id="034bd-282">Monitorando e gerando relatórios de conformidade do BitLocker com o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="034bd-282">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[<span data-ttu-id="034bd-283">Gerando relatórios autônomos do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="034bd-283">Generating MBAM 2.5 Stand-alone Reports</span></span>](generating-mbam-25-stand-alone-reports.md)



## <span data-ttu-id="034bd-284">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="034bd-284">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="034bd-285">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="034bd-285">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="034bd-286">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="034bd-286">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





