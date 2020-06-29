---
title: Noções básicas sobre relatórios do MBAM no Configuration Manager
description: Noções básicas sobre relatórios do MBAM no Configuration Manager
author: dansimp
ms.assetid: b2582190-c9de-4e64-bd5a-f31ac1916f53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 995d628cafd03c8bdd209e467c9d22169b7e03c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799349"
---
# <span data-ttu-id="9facd-103">Noções básicas sobre relatórios do MBAM no Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="9facd-103">Understanding MBAM Reports in Configuration Manager</span></span>


<span data-ttu-id="9facd-104">Quando a administração e o monitoramento do Microsoft BitLocker (MBAM) são instalados com a topologia integrada do Configuration Manager, os recursos de relatórios e conformidade de hardware são movidos para a infraestrutura do Configuration Manager e de MBAM.</span><span class="sxs-lookup"><span data-stu-id="9facd-104">When Microsoft BitLocker Administration and Monitoring (MBAM) is installed with the Configuration Manager Integrated topology, the hardware compliance and reporting features are moved into the Configuration Manager infrastructure and out of MBAM.</span></span> <span data-ttu-id="9facd-105">Ao usar a topologia do Configuration Manager, você executa relatórios do Configuration Manager em vez de MBAM, exceto para o relatório de auditoria de recuperação, que você continua a acessar usando o site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="9facd-105">When you use the Configuration Manager topology, you run reports from Configuration Manager rather than from MBAM, except for the Recovery Audit Report, which you continue to access by using the Administration and Monitoring Website.</span></span>

<span data-ttu-id="9facd-106">Os relatórios da topologia integrada do Configuration Manager mostram a compatibilidade do BitLocker para a empresa e para computadores e dispositivos individuais que o MBAM gerencia.</span><span class="sxs-lookup"><span data-stu-id="9facd-106">The reports for the Configuration Manager Integrated topology show BitLocker compliance for the enterprise and for individual computers and devices that MBAM manages.</span></span> <span data-ttu-id="9facd-107">Os relatórios fornecem gráficos e informações em tabelas, e permitem filtrar relatórios para exibir dados de diferentes perspectivas.</span><span class="sxs-lookup"><span data-stu-id="9facd-107">The reports provide both tabular information and charts, and enable you to filter reports to view data from different perspectives.</span></span>

<span data-ttu-id="9facd-108">As informações neste tópico descrevem os relatórios do MBAM executados a partir do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9facd-108">The information in this topic describes the MBAM reports that you run from Configuration Manager.</span></span> <span data-ttu-id="9facd-109">Para obter informações sobre os relatórios do MBAM para a topologia autônoma, consulte [noções básicas sobre relatórios do MBAM](understanding-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="9facd-109">For information about MBAM reports for the Stand-alone topology, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span></span>

## <span data-ttu-id="9facd-110">Acessando relatórios no Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="9facd-110">Accessing Reports in Configuration Manager</span></span>


<span data-ttu-id="9facd-111">Para acessar o recurso relatórios no Configuration Manager, abra o **console do Configuration Manager**.</span><span class="sxs-lookup"><span data-stu-id="9facd-111">To access the Reports feature in Configuration Manager, open the **Configuration Manager console**.</span></span> <span data-ttu-id="9facd-112">Para exibir a lista de relatórios disponíveis:</span><span class="sxs-lookup"><span data-stu-id="9facd-112">To display the list of available reports:</span></span>

-   <span data-ttu-id="9facd-113">No Configuration Manager 2007, expanda o nó **Gerenciamento do computador** e, em seguida, expanda o nó **relatório** .</span><span class="sxs-lookup"><span data-stu-id="9facd-113">In Configuration Manager 2007, expand the **Computer Management** node, and then expand the **Reporting** node.</span></span>

-   <span data-ttu-id="9facd-114">No SystemCenter2012 ConfigurationManager, no espaço de trabalho monitoramento em **visão geral**, expanda o nó **relatório** e clique em **relatórios**.</span><span class="sxs-lookup"><span data-stu-id="9facd-114">In SystemCenter2012 ConfigurationManager, in the Monitoring workspace under **Overview**, expand the **Reporting** node and then click **Reports**.</span></span>

### <span data-ttu-id="9facd-115">Painel de conformidade do BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="9facd-115">BitLocker Enterprise Compliance Dashboard</span></span>

<span data-ttu-id="9facd-116">O painel de conformidade do BitLocker Enterprise fornece os seguintes gráficos, que mostram o status de compatibilidade do BitLocker na empresa:</span><span class="sxs-lookup"><span data-stu-id="9facd-116">The BitLocker Enterprise Compliance Dashboard provides the following graphs, which show BitLocker compliance status across the enterprise:</span></span>

-   <span data-ttu-id="9facd-117">Distribuição de status de conformidade</span><span class="sxs-lookup"><span data-stu-id="9facd-117">Compliance Status Distribution</span></span>

-   <span data-ttu-id="9facd-118">Distribuição de erros não conformes</span><span class="sxs-lookup"><span data-stu-id="9facd-118">Non Compliant Errors Distribution</span></span>

-   <span data-ttu-id="9facd-119">Distribuição de status de conformidade por tipo de drive</span><span class="sxs-lookup"><span data-stu-id="9facd-119">Compliance Status Distribution by Drive Type</span></span>

**<span data-ttu-id="9facd-120">Distribuição de status de conformidade</span><span class="sxs-lookup"><span data-stu-id="9facd-120">Compliance Status Distribution</span></span>**

<span data-ttu-id="9facd-121">Este gráfico de pizza mostra status de conformidade do computador dentro da empresa e mostra a porcentagem de computadores, em comparação com o número total de computadores na coleção selecionada, que tem esse status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="9facd-121">This pie chart shows computer compliance statuses within the enterprise, and shows the percentage of computers, compared to the total number of computers in the selected collection, that have that compliance status.</span></span> <span data-ttu-id="9facd-122">O número real de computadores com cada status também é mostrado.</span><span class="sxs-lookup"><span data-stu-id="9facd-122">The actual number of computers with each status is also shown.</span></span> <span data-ttu-id="9facd-123">O gráfico de pizza mostra os seguintes status de conformidade:</span><span class="sxs-lookup"><span data-stu-id="9facd-123">The pie chart shows the following compliance statuses:</span></span>

-   <span data-ttu-id="9facd-124">CLS</span><span class="sxs-lookup"><span data-stu-id="9facd-124">Compliant</span></span>

-   <span data-ttu-id="9facd-125">Não compatível</span><span class="sxs-lookup"><span data-stu-id="9facd-125">Non Compliant</span></span>

-   <span data-ttu-id="9facd-126">Isento de usuário</span><span class="sxs-lookup"><span data-stu-id="9facd-126">User Exempt</span></span>

-   <span data-ttu-id="9facd-127">Isento de usuário temporário</span><span class="sxs-lookup"><span data-stu-id="9facd-127">Temporary User Exempt</span></span>

-   <span data-ttu-id="9facd-128">Política não imposta</span><span class="sxs-lookup"><span data-stu-id="9facd-128">Policy Not Enforced</span></span>

-   <span data-ttu-id="9facd-129">Desconhecido – computadores cujo status foi reportado como um erro, ou dispositivos que fazem parte da coleção, mas nunca relataram o status da conformidade, por exemplo, se estiverem desconectados da organização</span><span class="sxs-lookup"><span data-stu-id="9facd-129">Unknown -computers whose status was reported as an error, or devices that are part of the collection but have never reported their compliance status, for example, if they are disconnected from the organization</span></span>

**<span data-ttu-id="9facd-130">Distribuição de erros não conformes</span><span class="sxs-lookup"><span data-stu-id="9facd-130">Non Compliant Errors Distribution</span></span>**

<span data-ttu-id="9facd-131">Este gráfico de pizza mostra as categorias de computadores na empresa que não são compatíveis com a política de criptografia de unidade de disco BitLocker e mostra o número de computadores em cada categoria.</span><span class="sxs-lookup"><span data-stu-id="9facd-131">This pie chart shows the categories of computers in the enterprise that are not compliant with the BitLocker drive encryption policy, and shows the number of computers in each category.</span></span> <span data-ttu-id="9facd-132">Cada porcentagem da categoria é calculada a partir do número total de computadores não compatíveis na coleção.</span><span class="sxs-lookup"><span data-stu-id="9facd-132">Each category percentage is calculated from the total number of non-compliant computers in the collection.</span></span>

-   <span data-ttu-id="9facd-133">Criptografia adiada pelo usuário</span><span class="sxs-lookup"><span data-stu-id="9facd-133">User postponed encryption</span></span>

-   <span data-ttu-id="9facd-134">Não é possível encontrar o TPM compatível</span><span class="sxs-lookup"><span data-stu-id="9facd-134">Unable to find compatible TPM</span></span>

-   <span data-ttu-id="9facd-135">A partição do sistema não está disponível ou é grande o suficiente</span><span class="sxs-lookup"><span data-stu-id="9facd-135">System Partition not available or large enough</span></span>

-   <span data-ttu-id="9facd-136">Conflito de política</span><span class="sxs-lookup"><span data-stu-id="9facd-136">Policy conflict</span></span>

-   <span data-ttu-id="9facd-137">Aguardando o provisionamento automático do TPM</span><span class="sxs-lookup"><span data-stu-id="9facd-137">Waiting for TPM auto provisioning</span></span>

-   <span data-ttu-id="9facd-138">Ocorreu um erro desconhecido</span><span class="sxs-lookup"><span data-stu-id="9facd-138">An unknown error has occurred</span></span>

-   <span data-ttu-id="9facd-139">Nenhuma informação – computadores que não têm o cliente do MBAM instalado, ou que têm o cliente MBAM instalado, mas não foram ativados, por exemplo, o serviço não está funcionando</span><span class="sxs-lookup"><span data-stu-id="9facd-139">No information – computers that do not have the MBAM Client installed, or that have the MBAM Client installed but not activated, for example, the service is not working</span></span>

**<span data-ttu-id="9facd-140">Distribuição de status de conformidade por tipo de drive</span><span class="sxs-lookup"><span data-stu-id="9facd-140">Compliance Status Distribution by Drive Type</span></span>**

<span data-ttu-id="9facd-141">Este gráfico de barras mostra o status atual de conformidade do BitLocker por tipo de unidade.</span><span class="sxs-lookup"><span data-stu-id="9facd-141">This bar chart shows the current BitLocker compliance status by drive type.</span></span> <span data-ttu-id="9facd-142">Os status são "compatíveis" e "não compatíveis".</span><span class="sxs-lookup"><span data-stu-id="9facd-142">The statuses are “Compliant” and “Non Compliant.”</span></span> <span data-ttu-id="9facd-143">As barras são mostradas para unidades de dados fixas e unidades do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9facd-143">Bars are shown for fixed data drives and operating system drives.</span></span> <span data-ttu-id="9facd-144">Os computadores que não têm uma unidade de dados fixa são incluídos e mostram um valor apenas na barra de unidade do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9facd-144">Computers that do not have a fixed data drive are included and show a value only in the Operating System Drive bar.</span></span> <span data-ttu-id="9facd-145">O gráfico não inclui os usuários que receberam isenção da política de criptografia de unidade de disco BitLocker ou da categoria "sem política".</span><span class="sxs-lookup"><span data-stu-id="9facd-145">The chart does not include users who have been granted an exemption from the BitLocker drive encryption policy or the “No Policy” category.</span></span>

### <span data-ttu-id="9facd-146">Relatório de detalhes de conformidade corporativa do BitLocker</span><span class="sxs-lookup"><span data-stu-id="9facd-146">BitLocker Enterprise Compliance Details Report</span></span>

<span data-ttu-id="9facd-147">Este relatório mostra informações sobre a conformidade total do BitLocker em toda a sua empresa para o conjunto de computadores direcionados para uso do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9facd-147">This report shows information about the overall BitLocker compliance across your enterprise for the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="9facd-148">Campos de relatório de detalhes de conformidade corporativa do BitLocker</span><span class="sxs-lookup"><span data-stu-id="9facd-148">BitLocker Enterprise Compliance Details Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9facd-149">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="9facd-149">Column Name</span></span></th>
<th align="left"><span data-ttu-id="9facd-150">Descrição</span><span class="sxs-lookup"><span data-stu-id="9facd-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-151">Computadores gerenciados</span><span class="sxs-lookup"><span data-stu-id="9facd-151">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-152">Número de computadores que o MBAM gerencia.</span><span class="sxs-lookup"><span data-stu-id="9facd-152">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-153">% Compatível</span><span class="sxs-lookup"><span data-stu-id="9facd-153">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-154">Porcentagem de computadores compatíveis na empresa.</span><span class="sxs-lookup"><span data-stu-id="9facd-154">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-155">% Não compatível</span><span class="sxs-lookup"><span data-stu-id="9facd-155">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-156">Porcentagem de computadores não compatíveis na empresa.</span><span class="sxs-lookup"><span data-stu-id="9facd-156">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-157">% De conformidade desconhecida</span><span class="sxs-lookup"><span data-stu-id="9facd-157">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-158">Porcentagem de computadores cujo estado de conformidade não é conhecido.</span><span class="sxs-lookup"><span data-stu-id="9facd-158">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-159">% De isenção</span><span class="sxs-lookup"><span data-stu-id="9facd-159">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-160">Porcentagem de computadores isentos do requisito de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9facd-160">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-161">% Não isenta</span><span class="sxs-lookup"><span data-stu-id="9facd-161">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-162">Porcentagem de computadores isentos do requisito de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9facd-162">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-163">CLS</span><span class="sxs-lookup"><span data-stu-id="9facd-163">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-164">Porcentagem de computadores compatíveis na empresa.</span><span class="sxs-lookup"><span data-stu-id="9facd-164">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-165">Não compatível</span><span class="sxs-lookup"><span data-stu-id="9facd-165">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-166">Porcentagem de computadores não compatíveis na empresa.</span><span class="sxs-lookup"><span data-stu-id="9facd-166">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-167">Conformidade desconhecida</span><span class="sxs-lookup"><span data-stu-id="9facd-167">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-168">Porcentagem de computadores cujo estado de conformidade não é conhecido.</span><span class="sxs-lookup"><span data-stu-id="9facd-168">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-169">Isentos</span><span class="sxs-lookup"><span data-stu-id="9facd-169">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-170">Total de computadores isentos do requisito de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9facd-170">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-171">Não isento</span><span class="sxs-lookup"><span data-stu-id="9facd-171">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-172">Total de computadores que não estão isentos do requisito de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9facd-172">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="9facd-173">Relatório de detalhes de conformidade corporativa do BitLocker-Estados de conformidade</span><span class="sxs-lookup"><span data-stu-id="9facd-173">BitLocker Enterprise Compliance Details Report - Compliance States</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9facd-174">Status de conformidade</span><span class="sxs-lookup"><span data-stu-id="9facd-174">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="9facd-175">Isenção</span><span class="sxs-lookup"><span data-stu-id="9facd-175">Exemption</span></span></th>
<th align="left"><span data-ttu-id="9facd-176">Descrição</span><span class="sxs-lookup"><span data-stu-id="9facd-176">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-177">Não compatível</span><span class="sxs-lookup"><span data-stu-id="9facd-177">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-178">Não isento</span><span class="sxs-lookup"><span data-stu-id="9facd-178">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-179">O computador não é compatível, de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="9facd-179">The computer is noncompliant, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-180">CLS</span><span class="sxs-lookup"><span data-stu-id="9facd-180">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-181">Não isento</span><span class="sxs-lookup"><span data-stu-id="9facd-181">Not Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-182">O computador é compatível de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="9facd-182">The computer is compliant in accordance with the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="9facd-183">Relatório de Resumo de conformidade empresarial do BitLocker</span><span class="sxs-lookup"><span data-stu-id="9facd-183">BitLocker Enterprise Compliance Summary Report</span></span>

<span data-ttu-id="9facd-184">Use esse tipo de relatório para mostrar informações sobre a conformidade geral do BitLocker em toda a sua empresa e para mostrar a conformidade para computadores individuais que estejam na coleção de computadores que são direcionados para uso do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9facd-184">Use this report type to show information about the overall BitLocker compliance across your enterprise and to show the compliance for individual computers that are in the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="9facd-185">Campos relatório de Resumo de conformidade empresarial do BitLocker</span><span class="sxs-lookup"><span data-stu-id="9facd-185">BitLocker Enterprise Compliance Summary Report Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9facd-186">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="9facd-186">Column Name</span></span></th>
<th align="left"><span data-ttu-id="9facd-187">Descrição</span><span class="sxs-lookup"><span data-stu-id="9facd-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-188">Computadores gerenciados</span><span class="sxs-lookup"><span data-stu-id="9facd-188">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-189">Número de computadores que o MBAM gerencia.</span><span class="sxs-lookup"><span data-stu-id="9facd-189">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-190">% Compatível</span><span class="sxs-lookup"><span data-stu-id="9facd-190">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-191">Porcentagem de computadores compatíveis na empresa.</span><span class="sxs-lookup"><span data-stu-id="9facd-191">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-192">% Não compatível</span><span class="sxs-lookup"><span data-stu-id="9facd-192">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-193">Porcentagem de computadores não compatíveis na empresa.</span><span class="sxs-lookup"><span data-stu-id="9facd-193">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-194">% De conformidade desconhecida</span><span class="sxs-lookup"><span data-stu-id="9facd-194">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-195">Porcentagem de computadores cujo estado de conformidade não é conhecido.</span><span class="sxs-lookup"><span data-stu-id="9facd-195">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-196">% De isenção</span><span class="sxs-lookup"><span data-stu-id="9facd-196">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-197">Porcentagem de computadores isentos do requisito de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9facd-197">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-198">% Não isenta</span><span class="sxs-lookup"><span data-stu-id="9facd-198">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-199">Porcentagem de computadores isentos do requisito de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9facd-199">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-200">CLS</span><span class="sxs-lookup"><span data-stu-id="9facd-200">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-201">Porcentagem de computadores compatíveis na empresa.</span><span class="sxs-lookup"><span data-stu-id="9facd-201">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-202">Não compatível</span><span class="sxs-lookup"><span data-stu-id="9facd-202">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-203">Porcentagem de computadores não compatíveis na empresa.</span><span class="sxs-lookup"><span data-stu-id="9facd-203">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-204">Conformidade desconhecida</span><span class="sxs-lookup"><span data-stu-id="9facd-204">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-205">Porcentagem de computadores cujo estado de conformidade não é conhecido.</span><span class="sxs-lookup"><span data-stu-id="9facd-205">Percentage of computers whose compliance state is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-206">Isentos</span><span class="sxs-lookup"><span data-stu-id="9facd-206">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-207">Total de computadores isentos do requisito de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9facd-207">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-208">Não isento</span><span class="sxs-lookup"><span data-stu-id="9facd-208">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-209">Total de computadores que não estão isentos do requisito de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9facd-209">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="9facd-210">Relatório de Resumo de conformidade empresarial do BitLocker-detalhes do computador</span><span class="sxs-lookup"><span data-stu-id="9facd-210">BitLocker Enterprise Compliance Summary Report - Computer Details</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9facd-211">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="9facd-211">Column Name</span></span></th>
<th align="left"><span data-ttu-id="9facd-212">Descrição</span><span class="sxs-lookup"><span data-stu-id="9facd-212">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-213">Nome do computador</span><span class="sxs-lookup"><span data-stu-id="9facd-213">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-214">Nome do computador DNS especificado pelo usuário que está sendo gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="9facd-214">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-215">Nome de domínio</span><span class="sxs-lookup"><span data-stu-id="9facd-215">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-216">Nome de domínio totalmente qualificado, em que o computador cliente reside e é gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="9facd-216">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-217">Status de conformidade</span><span class="sxs-lookup"><span data-stu-id="9facd-217">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-218">Status geral de conformidade do computador gerenciado pela MBAM.</span><span class="sxs-lookup"><span data-stu-id="9facd-218">Overall Compliance Status of the computer managed by MBAM.</span></span> <span data-ttu-id="9facd-219">Os Estados válidos são compatíveis e não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="9facd-219">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="9facd-220">Observe que o status de conformidade por unidade (veja a tabela a seguir) pode indicar estados de conformidade diferentes.</span><span class="sxs-lookup"><span data-stu-id="9facd-220">Notice that the compliance status per drive (see table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="9facd-221">No entanto, esse campo representa o estado de conformidade, de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="9facd-221">However, this field represents that compliance state, in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-222">Isenção</span><span class="sxs-lookup"><span data-stu-id="9facd-222">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-223">Status que indica se o usuário está isento ou não isento da política BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9facd-223">Status that indicates whether the user is exempt or non-exemption from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-224">Usuários do dispositivo</span><span class="sxs-lookup"><span data-stu-id="9facd-224">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-225">Usuário do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9facd-225">User of the device.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-226">Detalhes do status de conformidade</span><span class="sxs-lookup"><span data-stu-id="9facd-226">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-227">Mensagens de erro e status do estado de conformidade do computador de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="9facd-227">Error and status messages of the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-228">Último contato</span><span class="sxs-lookup"><span data-stu-id="9facd-228">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-229">Data e hora em que o computador contatou o servidor pela última vez para informar o status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="9facd-229">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="9facd-230">A frequência do contato é configurável (consulte Configurações de política de MBAM).</span><span class="sxs-lookup"><span data-stu-id="9facd-230">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="9facd-231">Relatório de conformidade do computador BitLocker</span><span class="sxs-lookup"><span data-stu-id="9facd-231">BitLocker Computer Compliance Report</span></span>

<span data-ttu-id="9facd-232">Use esse tipo de relatório para coletar informações específicas a um computador.</span><span class="sxs-lookup"><span data-stu-id="9facd-232">Use this report type to collect information that is specific to a computer.</span></span> <span data-ttu-id="9facd-233">O relatório de conformidade do computador fornece informações de criptografia detalhadas sobre cada unidade (sistema operacional e unidades de dados fixas) em um computador, além de uma indicação da política aplicada a cada tipo de unidade no computador.</span><span class="sxs-lookup"><span data-stu-id="9facd-233">The Computer Compliance Report provides detailed encryption information about each drive (Operating System and Fixed data drives) on a computer, and also an indication of the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="9facd-234">Para ver os detalhes de cada unidade, expanda a entrada nome do computador.</span><span class="sxs-lookup"><span data-stu-id="9facd-234">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="9facd-235">**Observação**  O status da criptografia do volume de dados removível não é mostrado no relatório.</span><span class="sxs-lookup"><span data-stu-id="9facd-235">**Note** Removable Data Volume encryption status is not shown in the report.</span></span>

 

**<span data-ttu-id="9facd-236">Relatório de conformidade do computador BitLocker – campos de detalhes do computador</span><span class="sxs-lookup"><span data-stu-id="9facd-236">BitLocker Computer Compliance Report – Computer Details Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9facd-237">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="9facd-237">Column Name</span></span></th>
<th align="left"><span data-ttu-id="9facd-238">Descrição</span><span class="sxs-lookup"><span data-stu-id="9facd-238">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-239">Nome do computador</span><span class="sxs-lookup"><span data-stu-id="9facd-239">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-240">Nome do computador DNS especificado pelo usuário que está sendo gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="9facd-240">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-241">Nome de domínio</span><span class="sxs-lookup"><span data-stu-id="9facd-241">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-242">Nome de domínio totalmente qualificado, em que o computador cliente reside e é gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="9facd-242">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-243">Tipo de computador</span><span class="sxs-lookup"><span data-stu-id="9facd-243">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-244">Tipo de computador.</span><span class="sxs-lookup"><span data-stu-id="9facd-244">Type of computer.</span></span> <span data-ttu-id="9facd-245">Tipos válidos são não portáteis e portáteis.</span><span class="sxs-lookup"><span data-stu-id="9facd-245">Valid types are non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-246">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="9facd-246">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-247">Tipo de sistema operacional encontrado no computador cliente gerenciado MBAM.</span><span class="sxs-lookup"><span data-stu-id="9facd-247">Operating System type found on the MBAM managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-248">Conformidade geral</span><span class="sxs-lookup"><span data-stu-id="9facd-248">Overall Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-249">Status geral de conformidade do computador gerenciado pela MBAM.</span><span class="sxs-lookup"><span data-stu-id="9facd-249">Overall Compliance Status of the computer managed by MBAM.</span></span> <span data-ttu-id="9facd-250">Os Estados válidos são compatíveis e não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="9facd-250">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="9facd-251">Observe que o status de conformidade por unidade (veja a tabela a seguir) pode indicar estados de conformidade diferentes.</span><span class="sxs-lookup"><span data-stu-id="9facd-251">Notice that the compliance status per drive (see table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="9facd-252">No entanto, esse campo representa o estado de conformidade, de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="9facd-252">However, this field represents that compliance state, in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-253">Conformidade com o sistema operacional</span><span class="sxs-lookup"><span data-stu-id="9facd-253">Operating System Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-254">Status de conformidade do sistema operacional que é gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="9facd-254">Compliance status of the operating system that is managed by MBAM.</span></span> <span data-ttu-id="9facd-255">Os Estados válidos são compatíveis e não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="9facd-255">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-256">Conformidade de unidade de dados fixa</span><span class="sxs-lookup"><span data-stu-id="9facd-256">Fixed Data Drive Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-257">Status de conformidade da unidade de dados fixa gerenciada pela MBAM.</span><span class="sxs-lookup"><span data-stu-id="9facd-257">Compliance status of the Fixed Data Drive that is managed by MBAM.</span></span> <span data-ttu-id="9facd-258">Os Estados válidos são compatíveis e não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="9facd-258">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-259">Data da última atualização</span><span class="sxs-lookup"><span data-stu-id="9facd-259">Last Update Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-260">Data e hora em que o computador contatou o servidor pela última vez para informar o status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="9facd-260">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="9facd-261">A frequência do contato é configurável (consulte Configurações de política de MBAM).</span><span class="sxs-lookup"><span data-stu-id="9facd-261">The contact frequency is configurable (see MBAM policy settings).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-262">Isenção</span><span class="sxs-lookup"><span data-stu-id="9facd-262">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-263">Status que indica se o usuário está isento ou não isento da política BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9facd-263">Status that indicates whether the user is exempt or non-exemption from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-264">Usuário isento</span><span class="sxs-lookup"><span data-stu-id="9facd-264">Exempted User</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-265">Usuário que está isento da política BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9facd-265">User who is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-266">Data de isenção</span><span class="sxs-lookup"><span data-stu-id="9facd-266">Exemption Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-267">Data em que a isenção foi concedida.</span><span class="sxs-lookup"><span data-stu-id="9facd-267">Date on which the exemption was granted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-268">Detalhes do status de conformidade</span><span class="sxs-lookup"><span data-stu-id="9facd-268">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-269">Mensagens de erro e status do estado de conformidade do computador de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="9facd-269">Error and status messages of the compliance state of the computer in accordance to the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-270">Nível de codificação da política</span><span class="sxs-lookup"><span data-stu-id="9facd-270">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-271">Nível de codificação selecionado pelo administrador durante a especificação da política MBAM.</span><span class="sxs-lookup"><span data-stu-id="9facd-271">Cipher Strength selected by the Administrator during MBAM policy specification.</span></span> <span data-ttu-id="9facd-272">(por exemplo, 128-bit com difusor).</span><span class="sxs-lookup"><span data-stu-id="9facd-272">(for example, 128-bit with Diffuser).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-273">Política: unidade do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="9facd-273">Policy: Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-274">Indica se a criptografia é necessária para o o/S e o tipo de protetor apropriado.</span><span class="sxs-lookup"><span data-stu-id="9facd-274">Indicates if encryption is required for the O/S and the appropriate protector type.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-275">Política: unidade de dados fixa</span><span class="sxs-lookup"><span data-stu-id="9facd-275">Policy:Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-276">Indica se a criptografia é necessária para a unidade fixa.</span><span class="sxs-lookup"><span data-stu-id="9facd-276">Indicates if encryption is required for the Fixed Drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-277">Fabricante</span><span class="sxs-lookup"><span data-stu-id="9facd-277">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-278">Nome do fabricante do computador, como aparece no BIOS do computador.</span><span class="sxs-lookup"><span data-stu-id="9facd-278">Computer manufacturer name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-279">Modelo</span><span class="sxs-lookup"><span data-stu-id="9facd-279">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-280">Nome do modelo do fabricante do computador, como aparece no BIOS do computador.</span><span class="sxs-lookup"><span data-stu-id="9facd-280">Computer manufacturer model name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-281">Usuários do dispositivo</span><span class="sxs-lookup"><span data-stu-id="9facd-281">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-282">Usuários conhecidos no computador que está sendo gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="9facd-282">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="9facd-283">Relatório de conformidade do computador BitLocker – campos volume do computador</span><span class="sxs-lookup"><span data-stu-id="9facd-283">BitLocker Computer Compliance Report – Computer Volume Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9facd-284">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="9facd-284">Column Name</span></span></th>
<th align="left"><span data-ttu-id="9facd-285">Descrição</span><span class="sxs-lookup"><span data-stu-id="9facd-285">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-286">Letra da unidade</span><span class="sxs-lookup"><span data-stu-id="9facd-286">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-287">Letra da unidade do computador que foi atribuída à unidade específica pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="9facd-287">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-288">Tipo de unidade</span><span class="sxs-lookup"><span data-stu-id="9facd-288">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-289">Tipo de unidade.</span><span class="sxs-lookup"><span data-stu-id="9facd-289">Type of drive.</span></span> <span data-ttu-id="9facd-290">Os valores válidos são unidade do sistema operacional e unidade de dados fixa.</span><span class="sxs-lookup"><span data-stu-id="9facd-290">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="9facd-291">Esses são drives físicos, em vez de volumes lógicos.</span><span class="sxs-lookup"><span data-stu-id="9facd-291">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-292">Nível de codificação</span><span class="sxs-lookup"><span data-stu-id="9facd-292">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-293">Nível de codificação selecionado pelo administrador durante a especificação da política MBAM.</span><span class="sxs-lookup"><span data-stu-id="9facd-293">Cipher Strength selected by the Administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-294">Tipos de protetor</span><span class="sxs-lookup"><span data-stu-id="9facd-294">Protector Types</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-295">Tipo de protetor selecionado pela política usada para criptografar um sistema operacional ou volume fixo.</span><span class="sxs-lookup"><span data-stu-id="9facd-295">Type of protector selected via policy used to encrypt an operating system or Fixed volume.</span></span> <span data-ttu-id="9facd-296">Os tipos de protetor válidos em um sistema operacional são TPM ou TPM + PIN e para um volume de dados fixo é senha.</span><span class="sxs-lookup"><span data-stu-id="9facd-296">The valid protector types on an operating system are TPM or TPM+PIN and for a Fixed Data Volume is Password.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9facd-297">Estado do protetor</span><span class="sxs-lookup"><span data-stu-id="9facd-297">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-298">Indica que o computador que está sendo gerenciado pelo MBAM ativou o tipo de protetor especificado na política.</span><span class="sxs-lookup"><span data-stu-id="9facd-298">Indicates that the computer being managed by MBAM has enabled the protector type specified in the policy.</span></span> <span data-ttu-id="9facd-299">Os Estados válidos estão ATIVAdos ou desativados.</span><span class="sxs-lookup"><span data-stu-id="9facd-299">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9facd-300">Estado de criptografia</span><span class="sxs-lookup"><span data-stu-id="9facd-300">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="9facd-301">Estado de criptografia da unidade.</span><span class="sxs-lookup"><span data-stu-id="9facd-301">Encryption state of the drive.</span></span> <span data-ttu-id="9facd-302">Os Estados válidos são criptografados, não criptografados e criptografados.</span><span class="sxs-lookup"><span data-stu-id="9facd-302">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="9facd-303">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9facd-303">Related topics</span></span>


[<span data-ttu-id="9facd-304">Usando o MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="9facd-304">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)

 

 





