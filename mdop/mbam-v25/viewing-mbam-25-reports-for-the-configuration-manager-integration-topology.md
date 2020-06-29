---
title: Exibindo relatórios do MBAM 2.5 referentes à topologia de integração do Configuration Manager
description: Exibindo relatórios do MBAM 2.5 referentes à topologia de integração do Configuration Manager
author: dansimp
ms.assetid: 60d11b2f-3a76-4023-8da4-f89e9f35b790
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3384fee62d302ac47775fe106265456ef119ab47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799393"
---
# <span data-ttu-id="da997-103">Exibindo relatórios do MBAM 2.5 referentes à topologia de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="da997-103">Viewing MBAM 2.5 Reports for the Configuration Manager Integration Topology</span></span>


<span data-ttu-id="da997-104">Este tópico descreve os relatórios que estão disponíveis quando você configura o Microsoft BitLocker Administration and Monitoring (MBAM) com a topologia de integração do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="da997-104">This topic describes the reports that are available when you configure Microsoft BitLocker Administration and Monitoring (MBAM) with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="da997-105">Os relatórios mostram a compatibilidade do BitLocker para a empresa e para computadores e dispositivos individuais que o MBAM gerencia.</span><span class="sxs-lookup"><span data-stu-id="da997-105">The reports show BitLocker compliance for the enterprise and for individual computers and devices that MBAM manages.</span></span> <span data-ttu-id="da997-106">Os relatórios fornecem gráficos e informações em tabelas, e eles têm filtros que permitem que você visualize dados de diferentes perspectivas.</span><span class="sxs-lookup"><span data-stu-id="da997-106">The reports provide tabular information and charts, and they have filters that let you view data from different perspectives.</span></span>

<span data-ttu-id="da997-107">Na topologia de integração do Configuration Manager, você vê relatórios do Configuration Manager em vez de usar o site de administração e monitoramento, com exceção do **relatório de auditoria de recuperação**, que você continua a exibir no site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="da997-107">In the Configuration Manager Integration topology, you view reports from Configuration Manager rather than from the Administration and Monitoring Website, with the exception of the **Recovery Audit Report**, which you continue to view from the Administration and Monitoring Website.</span></span>

<span data-ttu-id="da997-108">Para obter informações sobre os relatórios do MBAM para a topologia autônoma, consulte [exibindo relatórios do MBAM 2,5 para a topologia](viewing-mbam-25-reports-for-the-stand-alone-topology.md)autônoma.</span><span class="sxs-lookup"><span data-stu-id="da997-108">For information about MBAM reports for the Stand-alone topology, see [Viewing MBAM 2.5 Reports for the Stand-alone Topology](viewing-mbam-25-reports-for-the-stand-alone-topology.md).</span></span>

## <span data-ttu-id="da997-109">Acessando relatórios no Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="da997-109">Accessing reports in Configuration Manager</span></span>


<span data-ttu-id="da997-110">Para acessar o recurso relatórios no Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="da997-110">To access the Reports feature in Configuration Manager:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="da997-111">Versão do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="da997-111">Version of Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="da997-112">Como exibir os relatórios</span><span class="sxs-lookup"><span data-stu-id="da997-112">How to view the reports</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-113">SystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="da997-113">SystemCenter2012 ConfigurationManager</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="da997-114">No painel esquerdo, selecione o <strong> espaço de </strong> trabalho monitoramento.</span><span class="sxs-lookup"><span data-stu-id="da997-114">In the left pane, select the <strong>Monitoring</strong> workspace.</span></span></p></li>
<li><p><span data-ttu-id="da997-115">Na árvore, expanda <strong> relatórios de relatório de visão geral </strong> &gt; <strong> </strong> &gt; <strong> </strong> &gt; <strong> MBAM </strong> .</span><span class="sxs-lookup"><span data-stu-id="da997-115">In the tree, expand <strong>Overview</strong> &gt; <strong>Reporting</strong> &gt; <strong>Reports</strong> &gt; <strong>MBAM</strong>.</span></span></p></li>
<li><p><span data-ttu-id="da997-116">Selecione a pasta que representa o idioma no qual você deseja exibir relatórios e, em seguida, selecione o relatório no painel à direita.</span><span class="sxs-lookup"><span data-stu-id="da997-116">Select the folder that represents the language in which you want to view reports, and then select the report from the right pane.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-117">Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="da997-117">Configuration Manager 2007</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="da997-118">No painel esquerdo, expanda <strong> Gerenciamento do computador relatório do Reporting </strong> &gt; <strong> </strong> &gt; <strong> Services </strong> &gt; <strong> &lt; Server &gt; </strong> &gt; <strong> Folders </strong> &gt; <strong> MBAM </strong> .</span><span class="sxs-lookup"><span data-stu-id="da997-118">In the left pane, expand <strong>Computer Management</strong> &gt; <strong>Reporting</strong> &gt; <strong>Reporting Services</strong> &gt; <strong>&lt;server name&gt;</strong> &gt; <strong>Report folders</strong> &gt; <strong>MBAM</strong>.</span></span></p></li>
<li><p><span data-ttu-id="da997-119">Selecione a pasta que representa o idioma no qual você deseja exibir relatórios e, em seguida, selecione o relatório no painel à direita.</span><span class="sxs-lookup"><span data-stu-id="da997-119">Select the folder that represents the language in which you want to view reports, and then select the report from the right pane.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="da997-120">Descrição dos relatórios no Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="da997-120">Description of reports in Configuration Manager</span></span>


<span data-ttu-id="da997-121">Há algumas diferenças mínimas nos relatórios da topologia de integração do Configuration Manager e da topologia autônoma.</span><span class="sxs-lookup"><span data-stu-id="da997-121">There are a few minor differences in the reports for the Configuration Manager Integration topology and the Stand-alone topology.</span></span> <span data-ttu-id="da997-122">As seções a seguir descrevem os dados nos relatórios do MBAM para a topologia de integração do Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="da997-122">The following sections describe the data in the MBAM reports for the Configuration Manager Integration topology:</span></span>

-   [<span data-ttu-id="da997-123">Painel de conformidade do BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="da997-123">BitLocker Enterprise Compliance Dashboard</span></span>](#bkmk-dashboard)

-   [<span data-ttu-id="da997-124">Detalhes de conformidade corporativa do BitLocker</span><span class="sxs-lookup"><span data-stu-id="da997-124">BitLocker Enterprise Compliance Details</span></span>](#bkmk-compliancedetails)

-   [<span data-ttu-id="da997-125">Resumo de conformidade empresarial do BitLocker</span><span class="sxs-lookup"><span data-stu-id="da997-125">BitLocker Enterprise Compliance Summary</span></span>](#bkmk-compliancesummary)

-   [<span data-ttu-id="da997-126">Relatório de conformidade do computador BitLocker</span><span class="sxs-lookup"><span data-stu-id="da997-126">BitLocker Computer Compliance Report</span></span>](#bkmk-compliancereport)

### <a href="" id="bkmk-dashboard"></a><span data-ttu-id="da997-127">Painel de conformidade do BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="da997-127">BitLocker Enterprise Compliance Dashboard</span></span>

<span data-ttu-id="da997-128">O painel de conformidade do BitLocker Enterprise fornece os seguintes gráficos, que mostram o status de compatibilidade do BitLocker na empresa:</span><span class="sxs-lookup"><span data-stu-id="da997-128">The BitLocker Enterprise Compliance Dashboard provides the following graphs, which show BitLocker compliance status across the enterprise:</span></span>

-   <span data-ttu-id="da997-129">Distribuição de status de conformidade</span><span class="sxs-lookup"><span data-stu-id="da997-129">Compliance Status Distribution</span></span>

-   <span data-ttu-id="da997-130">Distribuição de erros não conformes</span><span class="sxs-lookup"><span data-stu-id="da997-130">Non Compliant Errors Distribution</span></span>

-   <span data-ttu-id="da997-131">Distribuição de status de conformidade por tipo de drive</span><span class="sxs-lookup"><span data-stu-id="da997-131">Compliance Status Distribution by Drive Type</span></span>

**<span data-ttu-id="da997-132">Distribuição de status de conformidade</span><span class="sxs-lookup"><span data-stu-id="da997-132">Compliance Status Distribution</span></span>**

<span data-ttu-id="da997-133">Este gráfico de pizza mostra o status de conformidade para computadores dentro da empresa.</span><span class="sxs-lookup"><span data-stu-id="da997-133">This pie chart shows compliance status for computers within the enterprise.</span></span> <span data-ttu-id="da997-134">Ele também mostra a porcentagem de computadores, em comparação com o número total de computadores na coleção selecionada, que tem esse status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="da997-134">It also shows the percentage of computers, compared to the total number of computers in the selected collection, that has that compliance status.</span></span> <span data-ttu-id="da997-135">O número real de computadores com cada status também é mostrado.</span><span class="sxs-lookup"><span data-stu-id="da997-135">The actual number of computers with each status is also shown.</span></span> <span data-ttu-id="da997-136">O gráfico de pizza mostra os seguintes status de conformidade:</span><span class="sxs-lookup"><span data-stu-id="da997-136">The pie chart shows the following compliance statuses:</span></span>

-   <span data-ttu-id="da997-137">CLS</span><span class="sxs-lookup"><span data-stu-id="da997-137">Compliant</span></span>

-   <span data-ttu-id="da997-138">Não compatível</span><span class="sxs-lookup"><span data-stu-id="da997-138">Non Compliant</span></span>

-   <span data-ttu-id="da997-139">Isento de usuário</span><span class="sxs-lookup"><span data-stu-id="da997-139">User Exempt</span></span>

-   <span data-ttu-id="da997-140">Isento de usuário temporário</span><span class="sxs-lookup"><span data-stu-id="da997-140">Temporary User Exempt</span></span>

-   <span data-ttu-id="da997-141">Política não imposta</span><span class="sxs-lookup"><span data-stu-id="da997-141">Policy Not Enforced</span></span>

-   <span data-ttu-id="da997-142">Sabe.</span><span class="sxs-lookup"><span data-stu-id="da997-142">Unknown.</span></span> <span data-ttu-id="da997-143">Esses computadores relataram um erro de status ou fazem parte da coleção, mas nunca relataram o status da conformidade.</span><span class="sxs-lookup"><span data-stu-id="da997-143">These computers reported a status error, or they are part of the collection, but have never reported their compliance status.</span></span> <span data-ttu-id="da997-144">A falta de um status de conformidade pode ocorrer se o computador estiver desconectado da organização.</span><span class="sxs-lookup"><span data-stu-id="da997-144">The lack of a compliance status could occur if the computer is disconnected from the organization.</span></span>

**<span data-ttu-id="da997-145">Distribuição de erros não conformes</span><span class="sxs-lookup"><span data-stu-id="da997-145">Non Compliant Errors Distribution</span></span>**

<span data-ttu-id="da997-146">Este gráfico de pizza mostra as categorias de computadores na empresa que não são compatíveis com a política de criptografia de unidade de disco BitLocker e mostra o número de computadores em cada categoria.</span><span class="sxs-lookup"><span data-stu-id="da997-146">This pie chart shows the categories of computers in the enterprise that are not compliant with the BitLocker Drive Encryption policy, and shows the number of computers in each category.</span></span> <span data-ttu-id="da997-147">Cada porcentagem da categoria é calculada a partir do número total de computadores não compatíveis na coleção.</span><span class="sxs-lookup"><span data-stu-id="da997-147">Each category percentage is calculated from the total number of non-compliant computers in the collection.</span></span>

-   <span data-ttu-id="da997-148">Criptografia adiada pelo usuário</span><span class="sxs-lookup"><span data-stu-id="da997-148">User postponed encryption</span></span>

-   <span data-ttu-id="da997-149">Não é possível encontrar o TPM compatível</span><span class="sxs-lookup"><span data-stu-id="da997-149">Unable to find compatible TPM</span></span>

-   <span data-ttu-id="da997-150">A partição do sistema não está disponível ou é grande o suficiente</span><span class="sxs-lookup"><span data-stu-id="da997-150">System partition not available or large enough</span></span>

-   <span data-ttu-id="da997-151">Conflito de política</span><span class="sxs-lookup"><span data-stu-id="da997-151">Policy conflict</span></span>

-   <span data-ttu-id="da997-152">Aguardando o provisionamento automático do TPM</span><span class="sxs-lookup"><span data-stu-id="da997-152">Waiting for TPM auto provisioning</span></span>

-   <span data-ttu-id="da997-153">Ocorreu um erro desconhecido</span><span class="sxs-lookup"><span data-stu-id="da997-153">An unknown error has occurred</span></span>

-   <span data-ttu-id="da997-154">Não há informações.</span><span class="sxs-lookup"><span data-stu-id="da997-154">No information.</span></span> <span data-ttu-id="da997-155">Esses computadores não têm o cliente do MBAM instalado ou têm o cliente do MBAM instalado, mas não ativado (por exemplo, o serviço não está funcionando).</span><span class="sxs-lookup"><span data-stu-id="da997-155">These computers do not have the MBAM Client installed, or they have the MBAM Client installed but not activated (for example, the service is not working).</span></span>

**<span data-ttu-id="da997-156">Distribuição de status de conformidade por tipo de drive</span><span class="sxs-lookup"><span data-stu-id="da997-156">Compliance Status Distribution by Drive Type</span></span>**

<span data-ttu-id="da997-157">Este gráfico de barras mostra o status atual de conformidade do BitLocker por tipo de unidade.</span><span class="sxs-lookup"><span data-stu-id="da997-157">This bar chart shows the current BitLocker compliance status by drive type.</span></span> <span data-ttu-id="da997-158">Os status são **compatíveis** e **não são compatíveis**.</span><span class="sxs-lookup"><span data-stu-id="da997-158">The statuses are **Compliant** and **Non Compliant**.</span></span> <span data-ttu-id="da997-159">As barras são mostradas para unidades de dados fixas e unidades do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="da997-159">Bars are shown for fixed data drives and operating system drives.</span></span> <span data-ttu-id="da997-160">Os computadores que não têm uma unidade de dados fixa são incluídos e mostram um valor apenas na barra de **unidade do sistema operacional** .</span><span class="sxs-lookup"><span data-stu-id="da997-160">Computers that do not have a fixed data drive are included and show a value only in the **Operating System Drive** bar.</span></span> <span data-ttu-id="da997-161">O gráfico não inclui os usuários que receberam isenção da política de criptografia de unidade de disco BitLocker ou nenhuma categoria de política.</span><span class="sxs-lookup"><span data-stu-id="da997-161">The chart does not include users who have been granted an exemption from the BitLocker Drive Encryption policy or the No Policy category.</span></span>

### <a href="" id="bkmk-compliancedetails"></a><span data-ttu-id="da997-162">Detalhes de conformidade corporativa do BitLocker</span><span class="sxs-lookup"><span data-stu-id="da997-162">BitLocker Enterprise Compliance Details</span></span>

<span data-ttu-id="da997-163">Este relatório mostra informações sobre a conformidade total do BitLocker em toda a sua empresa para o conjunto de computadores direcionados para uso do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="da997-163">This report shows information about the overall BitLocker compliance across your enterprise for the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="da997-164">Campos de detalhes de conformidade corporativa do BitLocker</span><span class="sxs-lookup"><span data-stu-id="da997-164">BitLocker Enterprise Compliance Details Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="da997-165">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="da997-165">Column Name</span></span></th>
<th align="left"><span data-ttu-id="da997-166">Descrição</span><span class="sxs-lookup"><span data-stu-id="da997-166">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-167">Computadores gerenciados</span><span class="sxs-lookup"><span data-stu-id="da997-167">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-168">Número de computadores que o MBAM gerencia.</span><span class="sxs-lookup"><span data-stu-id="da997-168">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-169">% Compatível</span><span class="sxs-lookup"><span data-stu-id="da997-169">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-170">Porcentagem de computadores compatíveis na empresa.</span><span class="sxs-lookup"><span data-stu-id="da997-170">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-171">% Não compatível</span><span class="sxs-lookup"><span data-stu-id="da997-171">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-172">Porcentagem de computadores não compatíveis na empresa.</span><span class="sxs-lookup"><span data-stu-id="da997-172">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-173">% De conformidade desconhecida</span><span class="sxs-lookup"><span data-stu-id="da997-173">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-174">Porcentagem de computadores com um estado de conformidade que não é conhecido.</span><span class="sxs-lookup"><span data-stu-id="da997-174">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-175">% De isenção</span><span class="sxs-lookup"><span data-stu-id="da997-175">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-176">Porcentagem de computadores isentos do requisito de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="da997-176">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-177">% Não isenta</span><span class="sxs-lookup"><span data-stu-id="da997-177">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-178">Porcentagem de computadores que não estão isentos do requisito de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="da997-178">Percentage of computers not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-179">CLS</span><span class="sxs-lookup"><span data-stu-id="da997-179">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-180">Porcentagem de computadores compatíveis na empresa.</span><span class="sxs-lookup"><span data-stu-id="da997-180">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-181">Não compatível</span><span class="sxs-lookup"><span data-stu-id="da997-181">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-182">Porcentagem de computadores não compatíveis na empresa.</span><span class="sxs-lookup"><span data-stu-id="da997-182">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-183">Conformidade desconhecida</span><span class="sxs-lookup"><span data-stu-id="da997-183">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-184">Porcentagem de computadores com um estado de conformidade que não é conhecido.</span><span class="sxs-lookup"><span data-stu-id="da997-184">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-185">Isentos</span><span class="sxs-lookup"><span data-stu-id="da997-185">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-186">Total de computadores isentos do requisito de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="da997-186">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-187">Não isento</span><span class="sxs-lookup"><span data-stu-id="da997-187">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-188">Total de computadores que não estão isentos do requisito de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="da997-188">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="da997-189">Estados de detalhes de conformidade corporativa do BitLocker</span><span class="sxs-lookup"><span data-stu-id="da997-189">BitLocker Enterprise Compliance Details States</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="da997-190">Status de conformidade</span><span class="sxs-lookup"><span data-stu-id="da997-190">Compliance Status</span></span></th>
<th align="left"><span data-ttu-id="da997-191">Isenção</span><span class="sxs-lookup"><span data-stu-id="da997-191">Exemption</span></span></th>
<th align="left"><span data-ttu-id="da997-192">Descrição</span><span class="sxs-lookup"><span data-stu-id="da997-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-193">Não compatível</span><span class="sxs-lookup"><span data-stu-id="da997-193">Noncompliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-194">Não isento</span><span class="sxs-lookup"><span data-stu-id="da997-194">Not exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-195">O computador não é compatível, de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="da997-195">The computer is noncompliant, according to the specified policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-196">CLS</span><span class="sxs-lookup"><span data-stu-id="da997-196">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-197">Não isento</span><span class="sxs-lookup"><span data-stu-id="da997-197">Not exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-198">O computador é compatível de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="da997-198">The computer is compliant in accordance with the specified policy.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancesummary"></a><span data-ttu-id="da997-199">Resumo de conformidade empresarial do BitLocker</span><span class="sxs-lookup"><span data-stu-id="da997-199">BitLocker Enterprise Compliance Summary</span></span>

<span data-ttu-id="da997-200">Use esse tipo de relatório para mostrar informações sobre a conformidade geral do BitLocker em toda a sua empresa e para mostrar a conformidade para computadores individuais que estejam na coleção de computadores que são direcionados para uso do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="da997-200">Use this report type to show information about the overall BitLocker compliance across your enterprise and to show the compliance for individual computers that are in the collection of computers that is targeted for BitLocker use.</span></span>

**<span data-ttu-id="da997-201">Campos Resumo de conformidade empresarial do BitLocker</span><span class="sxs-lookup"><span data-stu-id="da997-201">BitLocker Enterprise Compliance Summary Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="da997-202">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="da997-202">Column Name</span></span></th>
<th align="left"><span data-ttu-id="da997-203">Descrição</span><span class="sxs-lookup"><span data-stu-id="da997-203">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-204">Computadores gerenciados</span><span class="sxs-lookup"><span data-stu-id="da997-204">Managed Computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-205">Número de computadores que o MBAM gerencia.</span><span class="sxs-lookup"><span data-stu-id="da997-205">Number of computers that MBAM manages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-206">% Compatível</span><span class="sxs-lookup"><span data-stu-id="da997-206">% Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-207">Porcentagem de computadores compatíveis na empresa.</span><span class="sxs-lookup"><span data-stu-id="da997-207">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-208">% Não compatível</span><span class="sxs-lookup"><span data-stu-id="da997-208">% Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-209">Porcentagem de computadores não compatíveis na empresa.</span><span class="sxs-lookup"><span data-stu-id="da997-209">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-210">% De conformidade desconhecida</span><span class="sxs-lookup"><span data-stu-id="da997-210">% Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-211">Porcentagem de computadores com um estado de conformidade que não é conhecido.</span><span class="sxs-lookup"><span data-stu-id="da997-211">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-212">% De isenção</span><span class="sxs-lookup"><span data-stu-id="da997-212">% Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-213">Porcentagem de computadores isentos do requisito de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="da997-213">Percentage of computers exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-214">% Não isenta</span><span class="sxs-lookup"><span data-stu-id="da997-214">% Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-215">Porcentagem de computadores que não estão isentos do requisito de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="da997-215">Percentage of computers not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-216">CLS</span><span class="sxs-lookup"><span data-stu-id="da997-216">Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-217">Porcentagem de computadores compatíveis na empresa.</span><span class="sxs-lookup"><span data-stu-id="da997-217">Percentage of compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-218">Não compatível</span><span class="sxs-lookup"><span data-stu-id="da997-218">Non-Compliant</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-219">Porcentagem de computadores não compatíveis na empresa.</span><span class="sxs-lookup"><span data-stu-id="da997-219">Percentage of non-compliant computers in the enterprise.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-220">Conformidade desconhecida</span><span class="sxs-lookup"><span data-stu-id="da997-220">Unknown Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-221">Porcentagem de computadores com um estado de conformidade que não é conhecido.</span><span class="sxs-lookup"><span data-stu-id="da997-221">Percentage of computers with a compliance state that is not known.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-222">Isentos</span><span class="sxs-lookup"><span data-stu-id="da997-222">Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-223">Total de computadores isentos do requisito de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="da997-223">Total computers that are exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-224">Não isento</span><span class="sxs-lookup"><span data-stu-id="da997-224">Non-Exempt</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-225">Total de computadores que não estão isentos do requisito de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="da997-225">Total computers that are not exempt from the BitLocker encryption requirement.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="da997-226">Detalhes do computador de Resumo de conformidade corporativa do BitLocker</span><span class="sxs-lookup"><span data-stu-id="da997-226">BitLocker Enterprise Compliance Summary Computer Details</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="da997-227">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="da997-227">Column Name</span></span></th>
<th align="left"><span data-ttu-id="da997-228">Descrição</span><span class="sxs-lookup"><span data-stu-id="da997-228">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-229">Nome do computador</span><span class="sxs-lookup"><span data-stu-id="da997-229">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-230">Nome do computador DNS especificado pelo usuário que está sendo gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="da997-230">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-231">Nome de domínio</span><span class="sxs-lookup"><span data-stu-id="da997-231">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-232">Nome de domínio totalmente qualificado, em que o computador cliente reside e é gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="da997-232">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-233">Status de conformidade</span><span class="sxs-lookup"><span data-stu-id="da997-233">Compliance Status</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-234">Status geral de conformidade do computador gerenciado pela MBAM.</span><span class="sxs-lookup"><span data-stu-id="da997-234">Overall compliance status of the computer managed by MBAM.</span></span> <span data-ttu-id="da997-235">Os Estados válidos são compatíveis e não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="da997-235">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="da997-236">Observe que o status de conformidade por unidade (veja a tabela a seguir) pode indicar estados de conformidade diferentes.</span><span class="sxs-lookup"><span data-stu-id="da997-236">Notice that the compliance status per drive (see the table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="da997-237">No entanto, esse campo representa o estado de conformidade, de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="da997-237">However, this field represents that compliance state, in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-238">Isenção</span><span class="sxs-lookup"><span data-stu-id="da997-238">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-239">Status que indica se o usuário está isento ou não isento da política BitLocker.</span><span class="sxs-lookup"><span data-stu-id="da997-239">Status that indicates whether the user is exempt or non-exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-240">Usuários do dispositivo</span><span class="sxs-lookup"><span data-stu-id="da997-240">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-241">Usuário do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da997-241">User of the device.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-242">Detalhes do status de conformidade</span><span class="sxs-lookup"><span data-stu-id="da997-242">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-243">Mensagens de erro e status sobre o estado de conformidade do computador de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="da997-243">Error and status messages about the compliance state of the computer in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-244">Último contato</span><span class="sxs-lookup"><span data-stu-id="da997-244">Last Contact</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-245">Data e hora em que o computador contatou o servidor pela última vez para informar o status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="da997-245">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="da997-246">A frequência do contato é configurável por meio das configurações da política de grupo.</span><span class="sxs-lookup"><span data-stu-id="da997-246">The contact frequency is configurable through the Group Policy settings.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancereport"></a><span data-ttu-id="da997-247">Relatório de conformidade do computador BitLocker</span><span class="sxs-lookup"><span data-stu-id="da997-247">BitLocker Computer Compliance Report</span></span>

<span data-ttu-id="da997-248">Use esse tipo de relatório para coletar informações específicas a um computador.</span><span class="sxs-lookup"><span data-stu-id="da997-248">Use this report type to collect information that is specific to a computer.</span></span> <span data-ttu-id="da997-249">O relatório de conformidade de computador BitLocker fornece informações de criptografia detalhadas sobre cada unidade em um computador (sistema operacional e unidades de dados fixas).</span><span class="sxs-lookup"><span data-stu-id="da997-249">The BitLocker Computer Compliance Report provides detailed encryption information about each drive on a computer (operating system and fixed data drives).</span></span> <span data-ttu-id="da997-250">Ele também fornece uma indicação da política aplicada a cada tipo de unidade no computador.</span><span class="sxs-lookup"><span data-stu-id="da997-250">It also provides an indication of the policy that is applied to each drive type on the computer.</span></span> <span data-ttu-id="da997-251">Para ver os detalhes de cada unidade, expanda a entrada nome do computador.</span><span class="sxs-lookup"><span data-stu-id="da997-251">To view the details of each drive, expand the Computer Name entry.</span></span>

<span data-ttu-id="da997-252">**Observação**  O status da criptografia do volume de dados removível não é mostrado neste relatório.</span><span class="sxs-lookup"><span data-stu-id="da997-252">**Note** The Removable Data Volume encryption status is not shown in this report.</span></span>

 

**<span data-ttu-id="da997-253">Relatório de conformidade do computador BitLocker: campos de detalhes do computador</span><span class="sxs-lookup"><span data-stu-id="da997-253">BitLocker Computer Compliance Report: Computer Details Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="da997-254">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="da997-254">Column Name</span></span></th>
<th align="left"><span data-ttu-id="da997-255">Descrição</span><span class="sxs-lookup"><span data-stu-id="da997-255">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-256">Nome do computador</span><span class="sxs-lookup"><span data-stu-id="da997-256">Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-257">Nome do computador DNS especificado pelo usuário que está sendo gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="da997-257">User-specified DNS computer name that is being managed by MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-258">Nome de domínio</span><span class="sxs-lookup"><span data-stu-id="da997-258">Domain Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-259">Nome de domínio totalmente qualificado, em que o computador cliente reside e é gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="da997-259">Fully qualified domain name, where the client computer resides and is managed by MBAM.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-260">Tipo de computador</span><span class="sxs-lookup"><span data-stu-id="da997-260">Computer Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-261">Tipo de computador.</span><span class="sxs-lookup"><span data-stu-id="da997-261">Type of computer.</span></span> <span data-ttu-id="da997-262">Tipos válidos são não portáteis e portáteis.</span><span class="sxs-lookup"><span data-stu-id="da997-262">Valid types are Non-Portable and Portable.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-263">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="da997-263">Operating System</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-264">Tipo de sistema operacional encontrado no computador cliente gerenciado MBAM.</span><span class="sxs-lookup"><span data-stu-id="da997-264">Operating System type found on the MBAM managed client computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-265">Conformidade geral</span><span class="sxs-lookup"><span data-stu-id="da997-265">Overall Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-266">Status geral de conformidade do computador gerenciado pela MBAM.</span><span class="sxs-lookup"><span data-stu-id="da997-266">Overall compliance status of the computer managed by MBAM.</span></span> <span data-ttu-id="da997-267">Os Estados válidos são compatíveis e não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="da997-267">Valid states are Compliant and Noncompliant.</span></span> <span data-ttu-id="da997-268">Observe que o status de conformidade por unidade (veja a tabela a seguir) pode indicar estados de conformidade diferentes.</span><span class="sxs-lookup"><span data-stu-id="da997-268">Notice that the compliance status per drive (see the table that follows) may indicate different compliance states.</span></span> <span data-ttu-id="da997-269">No entanto, esse campo representa o estado de conformidade de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="da997-269">However, this field represents that compliance state in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-270">Conformidade com o sistema operacional</span><span class="sxs-lookup"><span data-stu-id="da997-270">Operating System Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-271">Status de conformidade do sistema operacional que é gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="da997-271">Compliance status of the operating system that is managed by MBAM.</span></span> <span data-ttu-id="da997-272">Os Estados válidos são compatíveis e não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="da997-272">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-273">Conformidade de unidade de dados fixa</span><span class="sxs-lookup"><span data-stu-id="da997-273">Fixed Data Drive Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-274">Status de conformidade da unidade de dados fixa gerenciada pela MBAM.</span><span class="sxs-lookup"><span data-stu-id="da997-274">Compliance status of the fixed data drive that is managed by MBAM.</span></span> <span data-ttu-id="da997-275">Os Estados válidos são compatíveis e não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="da997-275">Valid states are Compliant and Noncompliant.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-276">Data da última atualização</span><span class="sxs-lookup"><span data-stu-id="da997-276">Last Update Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-277">Data e hora em que o computador contatou o servidor pela última vez para informar o status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="da997-277">Date and time that the computer last contacted the server to report compliance status.</span></span> <span data-ttu-id="da997-278">A frequência do contato é configurável por meio das configurações da política de grupo.</span><span class="sxs-lookup"><span data-stu-id="da997-278">The contact frequency is configurable through the Group Policy settings.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-279">Isenção</span><span class="sxs-lookup"><span data-stu-id="da997-279">Exemption</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-280">Status que indica se o usuário está isento ou não isento da política BitLocker.</span><span class="sxs-lookup"><span data-stu-id="da997-280">Status that indicates whether the user is exempt or non-exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-281">Usuário isento</span><span class="sxs-lookup"><span data-stu-id="da997-281">Exempted User</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-282">Usuário que está isento da política BitLocker.</span><span class="sxs-lookup"><span data-stu-id="da997-282">User who is exempt from the BitLocker policy.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-283">Data de isenção</span><span class="sxs-lookup"><span data-stu-id="da997-283">Exemption Date</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-284">Data em que a isenção foi concedida.</span><span class="sxs-lookup"><span data-stu-id="da997-284">Date on which the exemption was granted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-285">Detalhes do status de conformidade</span><span class="sxs-lookup"><span data-stu-id="da997-285">Compliance Status Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-286">Mensagens de erro e status sobre o estado de conformidade do computador de acordo com a política especificada.</span><span class="sxs-lookup"><span data-stu-id="da997-286">Error and status messages about the compliance state of the computer in accordance with the policy specified.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-287">Nível de codificação da política</span><span class="sxs-lookup"><span data-stu-id="da997-287">Policy Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-288">O nível de codificação selecionado pelo administrador durante a especificação da política MBAM (por exemplo, 128-bit com difusor).</span><span class="sxs-lookup"><span data-stu-id="da997-288">Cipher strength selected by the Administrator during the MBAM policy specification (for example, 128-bit with diffuser).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-289">Política: unidade do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="da997-289">Policy: Operating System Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-290">Indica se a criptografia é necessária para o sistema operacional e o tipo de protetor apropriado.</span><span class="sxs-lookup"><span data-stu-id="da997-290">Indicates if encryption is required for the operating system and the appropriate protector type.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-291">Política: unidade de dados fixa</span><span class="sxs-lookup"><span data-stu-id="da997-291">Policy: Fixed Data Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-292">Indica se a criptografia é necessária para a unidade de dados fixo.</span><span class="sxs-lookup"><span data-stu-id="da997-292">Indicates if encryption is required for the fixed data drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-293">Fabricante</span><span class="sxs-lookup"><span data-stu-id="da997-293">Manufacturer</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-294">Nome do fabricante do computador, como aparece no BIOS do computador.</span><span class="sxs-lookup"><span data-stu-id="da997-294">Computer manufacturer name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-295">Modelo</span><span class="sxs-lookup"><span data-stu-id="da997-295">Model</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-296">Nome do modelo do fabricante do computador, como aparece no BIOS do computador.</span><span class="sxs-lookup"><span data-stu-id="da997-296">Computer manufacturer model name as it appears in the computer BIOS.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-297">Usuários do dispositivo</span><span class="sxs-lookup"><span data-stu-id="da997-297">Device Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-298">Usuários conhecidos no computador que está sendo gerenciado pelo MBAM.</span><span class="sxs-lookup"><span data-stu-id="da997-298">Known users on the computer that is being managed by MBAM.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="da997-299">Relatório de conformidade do computador BitLocker: campos de volume do computador</span><span class="sxs-lookup"><span data-stu-id="da997-299">BitLocker Computer Compliance Report: Computer Volume Fields</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="da997-300">Nome da coluna</span><span class="sxs-lookup"><span data-stu-id="da997-300">Column Name</span></span></th>
<th align="left"><span data-ttu-id="da997-301">Descrição</span><span class="sxs-lookup"><span data-stu-id="da997-301">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-302">Letra da unidade</span><span class="sxs-lookup"><span data-stu-id="da997-302">Drive Letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-303">Letra da unidade do computador que foi atribuída à unidade específica pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="da997-303">Computer drive letter that was assigned to the particular drive by the user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-304">Tipo de unidade</span><span class="sxs-lookup"><span data-stu-id="da997-304">Drive Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-305">Tipo de unidade.</span><span class="sxs-lookup"><span data-stu-id="da997-305">Type of drive.</span></span> <span data-ttu-id="da997-306">Os valores válidos são unidade do sistema operacional e unidade de dados fixa.</span><span class="sxs-lookup"><span data-stu-id="da997-306">Valid values are Operating System Drive and Fixed Data Drive.</span></span> <span data-ttu-id="da997-307">Esses são drives físicos, em vez de volumes lógicos.</span><span class="sxs-lookup"><span data-stu-id="da997-307">These are physical drives rather than logical volumes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-308">Nível de codificação</span><span class="sxs-lookup"><span data-stu-id="da997-308">Cipher Strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-309">Nível de codificação selecionado pelo administrador durante a especificação da política MBAM.</span><span class="sxs-lookup"><span data-stu-id="da997-309">Cipher strength selected by the Administrator during MBAM policy specification.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-310">Tipos de protetor</span><span class="sxs-lookup"><span data-stu-id="da997-310">Protector Types</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-311">Tipo de protetor selecionado por meio da política usada para criptografar um sistema operacional ou unidade de dados fixa.</span><span class="sxs-lookup"><span data-stu-id="da997-311">Type of protector selected through the policy used to encrypt an operating system or fixed data drive.</span></span> <span data-ttu-id="da997-312">Os tipos de protetor válidos para um sistema operacional são TPM ou TPM + PIN.</span><span class="sxs-lookup"><span data-stu-id="da997-312">The valid protector types for an operating system are TPM or TPM+PIN.</span></span> <span data-ttu-id="da997-313">O tipo de protetor válido para uma unidade de dados fixa é uma senha.</span><span class="sxs-lookup"><span data-stu-id="da997-313">The valid protector type for a fixed data drive is a password.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da997-314">Estado do protetor</span><span class="sxs-lookup"><span data-stu-id="da997-314">Protector State</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-315">Indica que o computador que está sendo gerenciado pelo MBAM ativou o tipo de protetor especificado na política.</span><span class="sxs-lookup"><span data-stu-id="da997-315">Indicates that the computer being managed by MBAM has enabled the protector type specified in the policy.</span></span> <span data-ttu-id="da997-316">Os Estados válidos estão ATIVAdos ou desativados.</span><span class="sxs-lookup"><span data-stu-id="da997-316">The valid states are ON or OFF.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da997-317">Estado de criptografia</span><span class="sxs-lookup"><span data-stu-id="da997-317">Encryption State</span></span></p></td>
<td align="left"><p><span data-ttu-id="da997-318">Estado de criptografia da unidade.</span><span class="sxs-lookup"><span data-stu-id="da997-318">Encryption state of the drive.</span></span> <span data-ttu-id="da997-319">Os Estados válidos são criptografados, não criptografados e criptografados.</span><span class="sxs-lookup"><span data-stu-id="da997-319">Valid states are Encrypted, Not Encrypted, and Encrypting.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="da997-320">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="da997-320">Related topics</span></span>


[<span data-ttu-id="da997-321">Monitorando e gerando relatórios de conformidade do BitLocker com o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="da997-321">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

 

## <span data-ttu-id="da997-322">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="da997-322">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="da997-323">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="da997-323">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="da997-324">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="da997-324">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





