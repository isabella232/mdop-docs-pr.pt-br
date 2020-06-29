---
title: Noções básicas sobre relatórios do MBAM
description: Noções básicas sobre relatórios do MBAM
author: dansimp
ms.assetid: 8778f333-760e-4f26-acb4-4e73b6fbb536
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c3ca5e4da4cbcea80c87520f0ecd05e1e7d6be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799347"
---
# <span data-ttu-id="d4bc6-103">Noções básicas sobre relatórios do MBAM</span><span class="sxs-lookup"><span data-stu-id="d4bc6-103">Understanding MBAM Reports</span></span>


<span data-ttu-id="d4bc6-104">Se você escolheu a topologia autônoma ao instalar o Microsoft BitLocker Administration and Monitoring (MBAM), é possível executar diferentes relatórios no MBAM para monitorar o uso e a conformidade do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-104">If you chose the Stand-alone topology when you installed Microsoft BitLocker Administration and Monitoring (MBAM), you can run different reports in MBAM to monitor BitLocker usage and compliance.</span></span> <span data-ttu-id="d4bc6-105">O MBAM relata a conformidade e outras informações sobre todos os computadores e dispositivos que ele gerencia.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-105">MBAM reports compliance and other information about all of the computers and devices it manages.</span></span> <span data-ttu-id="d4bc6-106">As informações neste tópico podem ser usadas para ajudar você a entender os relatórios de administração e monitoramento do Microsoft BitLocker para empresas e para conformidade de computador individual e para a atividade de recuperação de chave.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-106">The information in this topic can be used to help you understand the Microsoft BitLocker Administration and Monitoring reports for enterprise and individual computer compliance and for key recovery activity.</span></span>

<span data-ttu-id="d4bc6-107">**Observação**  Se você escolheu a topologia do Configuration Manager quando instalou o Microsoft BitLocker Administration and Monitoring (MBAM), os relatórios são gerados do Configuration Manager em vez de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-107">**Note** If you chose the Configuration Manager topology when you installed Microsoft BitLocker Administration and Monitoring (MBAM), reports are generated from Configuration Manager rather than from MBAM.</span></span> <span data-ttu-id="d4bc6-108">Para obter mais informações sobre os relatórios executados a partir do Configuration Manager, consulte [noções básicas sobre relatórios do MBAM no Configuration Manager](understanding-mbam-reports-in-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="d4bc6-108">For more information about reports that are run from Configuration Manager, see [Understanding MBAM Reports in Configuration Manager](understanding-mbam-reports-in-configuration-manager.md).</span></span>

 

## <span data-ttu-id="d4bc6-109">Noções básicas sobre relatórios</span><span class="sxs-lookup"><span data-stu-id="d4bc6-109">Understanding Reports</span></span>


<span data-ttu-id="d4bc6-110">Para acessar o recurso relatórios da administração e do monitoramento do Microsoft BitLocker, abra um navegador da Web e abra o site Administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-110">To access the Reports feature of Microsoft BitLocker Administration and Monitoring, open a web browser and open the Administration and Monitoring website.</span></span> <span data-ttu-id="d4bc6-111">Selecione **relatórios** na barra de menus à esquerda e, em seguida, selecione na barra de menus superior o tipo de relatório que você deseja gerar.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-111">Select **Reports** in the left menu bar and then select from the top menu bar the kind of report that you want to generate.</span></span>

### <span data-ttu-id="d4bc6-112">Relatório de conformidade empresarial</span><span class="sxs-lookup"><span data-stu-id="d4bc6-112">Enterprise Compliance Report</span></span>

<span data-ttu-id="d4bc6-113">Use esse tipo de relatório para coletar informações sobre a conformidade geral do BitLocker em sua organização.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-113">Use this report type to collect information on overall BitLocker compliance in your organization.</span></span> <span data-ttu-id="d4bc6-114">Você pode usar filtros diferentes para restringir os resultados da pesquisa ao estado de conformidade e status de erro.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-114">You can use different filters to narrow your search results to Compliance state and Error status.</span></span> <span data-ttu-id="d4bc6-115">As informações do relatório são atualizadas a cada seis horas.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-115">The report information is updated every six hours.</span></span>

**<span data-ttu-id="d4bc6-116">Campos relatório de conformidade para empresas</span><span class="sxs-lookup"><span data-stu-id="d4bc6-116">Enterprise Compliance Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d4bc6-117">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="d4bc6-117">Column Name</span></span></th>
<th align="left"><span data-ttu-id="d4bc6-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4bc6-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4bc6-119">Nome do computador</span><span class="sxs-lookup"><span data-stu-id="d4bc6-119">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-120">Nome DNS especificado pelo usuário que está sendo gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-120">User-specified DNS name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4bc6-121">Nome de domínio</span><span class="sxs-lookup"><span data-stu-id="d4bc6-121">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-122">Nome de domínio totalmente qualificado em que o computador cliente reside e é gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-122">Fully qualified domain name where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4bc6-123">Status de conformidade</span><span class="sxs-lookup"><span data-stu-id="d4bc6-123">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-124">Estado de conformidade do computador, de acordo com a política especificada para o computador.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-124">State of compliance for the computer, according to the policy specified for the computer.</span></span> <span data-ttu-id="d4bc6-125">Os Estados são compatíveis e não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-125">The states are Noncompliant and Compliant.</span></span> <span data-ttu-id="d4bc6-126">Consulte a tabela Estados de conformidade para relatórios corporativos de conformidade para obter mais informações sobre como interpretar Estados de conformidade.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-126">See the Enterprise Compliance Report Compliance States table for more information about how to interpret compliance states.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4bc6-127">Detalhes do status de conformidade</span><span class="sxs-lookup"><span data-stu-id="d4bc6-127">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-128">Mensagens de erro e status do estado de conformidade do computador de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-128">Error and status messages of the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4bc6-129">Último contato</span><span class="sxs-lookup"><span data-stu-id="d4bc6-129">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-130">Data e hora em que o computador contatou o servidor pela última vez para informar o status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-130">Date and time when the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="d4bc6-131">A frequência do contato é configurável (consulte Configurações de política de MBAM).</span><span class="sxs-lookup"><span data-stu-id="d4bc6-131">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="d4bc6-132">Estados de conformidade para relatórios de conformidade empresarial</span><span class="sxs-lookup"><span data-stu-id="d4bc6-132">Enterprise Compliance Report Compliance States</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d4bc6-133">Status de conformidade</span><span class="sxs-lookup"><span data-stu-id="d4bc6-133">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="d4bc6-134">Isenção</span><span class="sxs-lookup"><span data-stu-id="d4bc6-134">Exemption</span></span></th>
<th align="left"><span data-ttu-id="d4bc6-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4bc6-135">Description</span></span></th>
<th align="left"><span data-ttu-id="d4bc6-136">Ação do usuário</span><span class="sxs-lookup"><span data-stu-id="d4bc6-136">User Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4bc6-137">Não compatível</span><span class="sxs-lookup"><span data-stu-id="d4bc6-137">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-138">Não isento</span><span class="sxs-lookup"><span data-stu-id="d4bc6-138">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-139">O computador não é compatível, de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-139">The computer is noncompliant, according to the specified policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-140">Expanda os detalhes do relatório de conformidade do computador clicando em <strong> nome </strong> do computador e determine se o estado de cada unidade está em conformidade com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-140">Expand the Computer Compliance Report details by clicking <strong>Computer Name</strong>, and determine whether the state of each drive complies with the specified policy.</span></span> <span data-ttu-id="d4bc6-141">Se o estado de criptografia indicar que o computador não está criptografado, a criptografia pode estar em processo, ou há um erro no computador.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-141">If the encryption state indicates that the computer is not encrypted, encryption may be in process, or there is an error on the computer.</span></span> <span data-ttu-id="d4bc6-142">Se não houver nenhum erro, a causa provável é que o computador ainda está em processo de conexão ou estabelecimento do status de criptografia.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-142">If there is no error, the likely cause is that the computer is still in the process of connecting or establishing the encryption status.</span></span> <span data-ttu-id="d4bc6-143">Verifique novamente mais tarde para determinar se o estado muda.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-143">Check back later to determine if the state changes.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4bc6-144">CLS</span><span class="sxs-lookup"><span data-stu-id="d4bc6-144">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-145">Não isento</span><span class="sxs-lookup"><span data-stu-id="d4bc6-145">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-146">O computador é compatível, de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-146">The computer is compliant, according to the specified policy.</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-147">Nenhuma ação necessária; o estado do computador pode ser confirmado exibindo o relatório de conformidade do computador.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-147">No action needed; the state of the computer can be confirmed by viewing the Computer Compliance Report.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="d4bc6-148">Relatório de conformidade do computador</span><span class="sxs-lookup"><span data-stu-id="d4bc6-148">Computer Compliance Report</span></span>

<span data-ttu-id="d4bc6-149">Use esse tipo de relatório para coletar informações específicas a um computador ou usuário.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-149">Use this report type to collect information that is specific to a computer or user.</span></span>

<span data-ttu-id="d4bc6-150">Este relatório pode ser visualizado clicando no nome do computador no relatório de conformidade empresarial ou digitando o nome do computador no relatório de conformidade do computador.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-150">This report can be viewed by clicking the computer name in the Enterprise Compliance Report, or by typing the computer name in the Computer Compliance Report.</span></span> <span data-ttu-id="d4bc6-151">O relatório de conformidade do computador fornece informações de criptografia detalhadas sobre cada unidade (sistema operacional e unidades de dados fixas) em um computador, além de uma indicação da política aplicada a cada tipo de unidade no computador.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-151">The Computer Compliance Report provides detailed encryption information about each drive (operating system and fixed data drives) on a computer, and also an indication of the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="d4bc6-152">Para ver os detalhes de cada unidade, expanda a entrada nome do computador.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-152">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="d4bc6-153">**Observação**  O status da criptografia do volume de dados removível não será exibido no relatório.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-153">**Note** Removable Data Volume encryption status will not be shown in the report.</span></span>

 

**<span data-ttu-id="d4bc6-154">Campos de relatório de conformidade do computador</span><span class="sxs-lookup"><span data-stu-id="d4bc6-154">Computer Compliance Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d4bc6-155">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="d4bc6-155">Column Name</span></span></th>
<th align="left"><span data-ttu-id="d4bc6-156">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4bc6-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4bc6-157">Nome do computador</span><span class="sxs-lookup"><span data-stu-id="d4bc6-157">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-158">Nome do computador DNS especificado pelo usuário que está sendo gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-158">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4bc6-159">Nome de domínio</span><span class="sxs-lookup"><span data-stu-id="d4bc6-159">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-160">Nome de domínio totalmente qualificado, em que o computador cliente reside e é gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-160">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4bc6-161">Tipo de computador</span><span class="sxs-lookup"><span data-stu-id="d4bc6-161">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-162">Tipo de computador.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-162">Type of computer.</span></span> <span data-ttu-id="d4bc6-163">Tipos válidos são não portáteis e portáteis.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-163">Valid types are non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4bc6-164">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="d4bc6-164">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-165">Tipo de sistema operacional encontrado no computador cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-165">Operating system type found on the MBAM-managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4bc6-166">Status de conformidade</span><span class="sxs-lookup"><span data-stu-id="d4bc6-166">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-167">Status geral de conformidade do computador gerenciado pela MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-167">Overall compliance status of the computer managed by MBAM.</span></span> <span data-ttu-id="d4bc6-168">Os Estados válidos são compatíveis e não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-168">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="d4bc6-169">Observe que o status de conformidade por unidade (veja a tabela a seguir) pode indicar estados de conformidade diferentes.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-169">Notice that the compliance status per drive (see the following table) may indicate different compliance states.</span></span> <span data-ttu-id="d4bc6-170">No entanto, esse campo representa o estado de conformidade, de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-170">However, this field represents that compliance state, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4bc6-171">Nível de codificação da política</span><span class="sxs-lookup"><span data-stu-id="d4bc6-171">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-172">O nível de codificação selecionado pelo administrador durante a especificação da política MBAM (por exemplo, 128-bit com difusor).</span><span class="sxs-lookup"><span data-stu-id="d4bc6-172">Cipher strength selected by the administrator during MBAM policy specification (for example, 128-bit with Diffuser).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4bc6-173">Unidade de sistema operacional da política</span><span class="sxs-lookup"><span data-stu-id="d4bc6-173">Policy Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-174">Indica se a criptografia é necessária para o sistema operacional e mostra o tipo de protetor apropriado.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-174">Indicates if encryption is required for the operating system and shows the appropriate protector type.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4bc6-175">Unidade de dados fixos da política</span><span class="sxs-lookup"><span data-stu-id="d4bc6-175">Policy-Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-176">Indica se a criptografia é necessária para a unidade de dados fixo.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-176">Indicates if encryption is required for the fixed data drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4bc6-177">Unidade de dados removível de política</span><span class="sxs-lookup"><span data-stu-id="d4bc6-177">Policy Removable Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-178">Indica se a criptografia é necessária para a unidade removível.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-178">Indicates if encryption is required for the removable drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4bc6-179">Usuários do dispositivo</span><span class="sxs-lookup"><span data-stu-id="d4bc6-179">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-180">Usuários conhecidos no computador que está sendo gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-180">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4bc6-181">Fabricante</span><span class="sxs-lookup"><span data-stu-id="d4bc6-181">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-182">Nome do fabricante do computador, como aparece no BIOS do computador.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-182">Computer manufacturer name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4bc6-183">Modelo</span><span class="sxs-lookup"><span data-stu-id="d4bc6-183">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-184">Nome do modelo do fabricante do computador, como aparece no BIOS do computador.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-184">Computer manufacturer model name, as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4bc6-185">Detalhes do status de conformidade</span><span class="sxs-lookup"><span data-stu-id="d4bc6-185">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-186">Mensagens de erro e status do estado de conformidade do computador, de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-186">Error and status messages of the compliance state of the computer, in accordance with the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4bc6-187">Último contato</span><span class="sxs-lookup"><span data-stu-id="d4bc6-187">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-188">Data e hora em que o computador contatou o servidor pela última vez para informar o status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-188">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="d4bc6-189">A frequência do contato é configurável (consulte Configurações de política de MBAM).</span><span class="sxs-lookup"><span data-stu-id="d4bc6-189">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="d4bc6-190">Campos da unidade do relatório de conformidade do computador</span><span class="sxs-lookup"><span data-stu-id="d4bc6-190">Computer Compliance Report Drive Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d4bc6-191">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="d4bc6-191">Column Name</span></span></th>
<th align="left"><span data-ttu-id="d4bc6-192">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4bc6-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4bc6-193">Letra da unidade</span><span class="sxs-lookup"><span data-stu-id="d4bc6-193">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-194">Letra da unidade do computador que foi atribuída à unidade específica pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-194">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4bc6-195">Tipo de unidade</span><span class="sxs-lookup"><span data-stu-id="d4bc6-195">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-196">Tipo de unidade.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-196">Type of drive.</span></span> <span data-ttu-id="d4bc6-197">Os valores válidos são unidade do sistema operacional e unidade de dados fixa.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-197">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="d4bc6-198">Esses são drives físicos, em vez de volumes lógicos.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-198">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4bc6-199">Nível de codificação</span><span class="sxs-lookup"><span data-stu-id="d4bc6-199">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-200">Nível de codificação selecionado pelo administrador durante a especificação da política MBAM.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-200">Cipher strength selected by the administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4bc6-201">Tipo de protetor</span><span class="sxs-lookup"><span data-stu-id="d4bc6-201">Protector Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-202">Tipo de protetor selecionado por meio da política usada para criptografar um sistema operacional ou volume de dados fixos.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-202">Type of protector selected via the policy used to encrypt an operating system or fixed data volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4bc6-203">Estado do protetor</span><span class="sxs-lookup"><span data-stu-id="d4bc6-203">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-204">Indica que o computador que está sendo gerenciado pelo MBAM ativou o tipo de protetor especificado na política.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-204">Indicates that the computer being managed by MBAM has enabled the protector type that is specified in the policy.</span></span> <span data-ttu-id="d4bc6-205">Os Estados válidos estão ATIVAdos ou desativados.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-205">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4bc6-206">Estado de criptografia</span><span class="sxs-lookup"><span data-stu-id="d4bc6-206">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-207">Estado de criptografia da unidade.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-207">Encryption state of the drive.</span></span> <span data-ttu-id="d4bc6-208">Os Estados válidos são criptografados, não criptografados e criptografados.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-208">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4bc6-209">Status de conformidade</span><span class="sxs-lookup"><span data-stu-id="d4bc6-209">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-210">Estado que indica se a unidade está de acordo com a política.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-210">State that indicates whether the drive is in accordance with the policy.</span></span> <span data-ttu-id="d4bc6-211">Os Estados são compatíveis e não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-211">States are Noncompliant and Compliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4bc6-212">Detalhes do status de conformidade</span><span class="sxs-lookup"><span data-stu-id="d4bc6-212">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-213">Mensagens de erro e status do estado de conformidade do computador, de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-213">Error and status messages of the compliance state of the computer, according to the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="d4bc6-214">Relatório de auditoria de recuperação</span><span class="sxs-lookup"><span data-stu-id="d4bc6-214">Recovery Audit Report</span></span>

<span data-ttu-id="d4bc6-215">Use esse tipo de relatório para auditar os usuários que solicitaram acesso às chaves de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-215">Use this report type to audit users who have requested access to recovery keys.</span></span> <span data-ttu-id="d4bc6-216">O relatório oferece vários filtros com base nos critérios de filtragem desejados.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-216">The report offers several filters based on the desired filtering criteria.</span></span> <span data-ttu-id="d4bc6-217">Os usuários podem filtrar em um tipo específico de usuário, um usuário de suporte técnico ou um usuário final, se a solicitação falhou ou foi bem-sucedida, o tipo específico de chave solicitada e um intervalo de datas durante o qual ocorreu a recuperação.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-217">Users can filter on a specific type of user, either a Help Desk user or an end user, whether the request failed or was successful, the specific type of key requested, and a date range during which the retrieval occurred.</span></span> <span data-ttu-id="d4bc6-218">O administrador pode produzir relatórios contextuais de acordo com a necessidade.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-218">The administrator can produce contextual reports based on need.</span></span>

**<span data-ttu-id="d4bc6-219">Campos de relatório de auditoria de recuperação</span><span class="sxs-lookup"><span data-stu-id="d4bc6-219">Recovery Audit Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d4bc6-220">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="d4bc6-220">Column Name</span></span></th>
<th align="left"><span data-ttu-id="d4bc6-221">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4bc6-221">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4bc6-222">Data e hora da solicitação</span><span class="sxs-lookup"><span data-stu-id="d4bc6-222">Request Date and Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-223">Data e hora em que uma solicitação de recuperação de chave foi feita por um usuário final ou usuário de suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-223">Date and time that a key retrieval request was made by an end user or Help Desk user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4bc6-224">Status da solicitação</span><span class="sxs-lookup"><span data-stu-id="d4bc6-224">Request Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-225">Status da solicitação.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-225">Status of the request.</span></span> <span data-ttu-id="d4bc6-226">Os status válidos são bem-sucedidos (a chave foi recuperada) ou falha (a tecla não foi recuperada).</span><span class="sxs-lookup"><span data-stu-id="d4bc6-226">Valid statuses are either Successful (the key was retrieved), or Failed (the key was not retrieved).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4bc6-227">Usuário da assistência técnica</span><span class="sxs-lookup"><span data-stu-id="d4bc6-227">Helpdesk User</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-228">Usuário de suporte técnico que iniciou a solicitação de recuperação de chave.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-228">Help Desk user that initiated the request for key retrieval.</span></span> <span data-ttu-id="d4bc6-229">Observação: se o usuário de suporte técnico recuperar a chave em um usuário final, o campo usuário final estará em branco.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-229">Note: If the Help Desk user retrieves the key on behalf on an end-user, the End User field will be blank.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4bc6-230">Usuário</span><span class="sxs-lookup"><span data-stu-id="d4bc6-230">User</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-231">Usuário final que iniciou a solicitação de recuperação de chave.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-231">End user who initiated the request for key retrieval.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d4bc6-232">Tipo de chave</span><span class="sxs-lookup"><span data-stu-id="d4bc6-232">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-233">Tipo de chave que foi solicitada pelo usuário de suporte técnico ou pelo usuário final.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-233">Type of key that was requested by either the Help Desk user or the end user.</span></span> <span data-ttu-id="d4bc6-234">Os três tipos de chaves que o MBAM coleta são: senha da chave de recuperação (usada para recuperar um computador no modo de recuperação), ID da chave de recuperação (usada para recuperar um computador no modo de recuperação em nome de outro usuário) e hash de senha do TPM (usado para recuperar um computador com um TPM bloqueado).</span><span class="sxs-lookup"><span data-stu-id="d4bc6-234">The three types of keys that MBAM collects are: Recovery Key Password (used to recovery a computer in recovery mode), Recovery Key ID (used to recover a computer in recovery mode on behalf of another user), and TPM Password Hash (used to recover a computer with a locked TPM).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d4bc6-235">Descrição do motivo</span><span class="sxs-lookup"><span data-stu-id="d4bc6-235">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="d4bc6-236">Motivo pelo qual o tipo de chave especificado foi solicitado pelo usuário de suporte técnico ou pelo usuário final.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-236">Reason the specified Key Type was requested by the Help Desk user or the end user.</span></span> <span data-ttu-id="d4bc6-237">Os motivos são especificados nos recursos de recuperação de unidade e gerenciamento de TPM do site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-237">The reasons are specified in the Drive Recovery and Manage TPM features of the Administration and Monitoring website.</span></span> <span data-ttu-id="d4bc6-238">As entradas válidas são texto inserido pelo usuário ou um dos seguintes códigos de motivo:</span><span class="sxs-lookup"><span data-stu-id="d4bc6-238">The valid entries are either user-entered text, or one of the following reason codes:</span></span></p>
<ul>
<li><p><span data-ttu-id="d4bc6-239">Ordem de inicialização do sistema operacional alterada</span><span class="sxs-lookup"><span data-stu-id="d4bc6-239">Operating System Boot Order changed</span></span></p></li>
<li><p><span data-ttu-id="d4bc6-240">BIOS alterado</span><span class="sxs-lookup"><span data-stu-id="d4bc6-240">BIOS Changed</span></span></p></li>
<li><p><span data-ttu-id="d4bc6-241">Arquivos do sistema operacional alterados</span><span class="sxs-lookup"><span data-stu-id="d4bc6-241">Operating System files changed</span></span></p></li>
<li><p><span data-ttu-id="d4bc6-242">Chave de inicialização perdida</span><span class="sxs-lookup"><span data-stu-id="d4bc6-242">Lost Startup key</span></span></p></li>
<li><p><span data-ttu-id="d4bc6-243">Perdeu o PIN</span><span class="sxs-lookup"><span data-stu-id="d4bc6-243">Lost PIN</span></span></p></li>
<li><p><span data-ttu-id="d4bc6-244">Redefinição de TPM</span><span class="sxs-lookup"><span data-stu-id="d4bc6-244">TPM Reset</span></span></p></li>
<li><p><span data-ttu-id="d4bc6-245">Senha perdida</span><span class="sxs-lookup"><span data-stu-id="d4bc6-245">Lost Passphrase</span></span></p></li>
<li><p><span data-ttu-id="d4bc6-246">Cartão inteligente perdido</span><span class="sxs-lookup"><span data-stu-id="d4bc6-246">Lost Smartcard</span></span></p></li>
<li><p><span data-ttu-id="d4bc6-247">Redefinir o bloqueio de PIN</span><span class="sxs-lookup"><span data-stu-id="d4bc6-247">Reset PIN lockout</span></span></p></li>
<li><p><span data-ttu-id="d4bc6-248">Ativar o TPM</span><span class="sxs-lookup"><span data-stu-id="d4bc6-248">Turn on TPM</span></span></p></li>
<li><p><span data-ttu-id="d4bc6-249">Desativar o TPM</span><span class="sxs-lookup"><span data-stu-id="d4bc6-249">Turn off TPM</span></span></p></li>
<li><p><span data-ttu-id="d4bc6-250">Alterar a senha do TPM</span><span class="sxs-lookup"><span data-stu-id="d4bc6-250">Change TPM password</span></span></p></li>
<li><p><span data-ttu-id="d4bc6-251">Limpar TPM</span><span class="sxs-lookup"><span data-stu-id="d4bc6-251">Clear TPM</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="d4bc6-252">**Observação**  Os resultados do relatório podem ser salvos em um arquivo clicando no botão **Exportar** na barra de menus relatórios.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-252">**Note** Report results can be saved to a file by clicking the **Export** button on the reports menu bar.</span></span> <span data-ttu-id="d4bc6-253">Para obter mais informações sobre como executar relatórios do MBAM, consulte [como gerar relatórios do MBAM](how-to-generate-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="d4bc6-253">For more information about how to run MBAM reports, see [How to Generate MBAM Reports](how-to-generate-mbam-reports-mbam-2.md).</span></span>

 

## <span data-ttu-id="d4bc6-254">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4bc6-254">Related topics</span></span>


[<span data-ttu-id="d4bc6-255">Monitorando e Gerando Relatórios de Conformidade do BitLocker com o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d4bc6-255">Monitoring and Reporting BitLocker Compliance with MBAM 2.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





