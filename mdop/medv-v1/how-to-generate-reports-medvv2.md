---
title: Como gerar relatórios
description: Como gerar relatórios
author: dansimp
ms.assetid: 9f8ba28e-1993-4c11-a28a-493718051e5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 930b7061d3e5e2fb9951d45b1422915836cbc00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799983"
---
# <span data-ttu-id="d0396-103">Como gerar relatórios</span><span class="sxs-lookup"><span data-stu-id="d0396-103">How to Generate Reports</span></span>


<span data-ttu-id="d0396-104">Os seguintes tipos de relatório podem ser criados por administradores no MED-V:</span><span class="sxs-lookup"><span data-stu-id="d0396-104">The following report types can be created by administrators in MED-V:</span></span>

-   <span data-ttu-id="d0396-105">[Status](#bkmk-generatingastatusreport)— use o relatório de status para analisar o status atual de todos os usuários ativos e todos os espaços de trabalho do MED-V de cada usuário com base em um período de tempo definido.</span><span class="sxs-lookup"><span data-stu-id="d0396-105">[Status](#bkmk-generatingastatusreport)—Use the status report to review the current status of all active users and all MED-V workspaces of each user based on a defined period of time.</span></span> <span data-ttu-id="d0396-106">Isso inclui a visualização de computadores que estão conectados ao servidor ou, se não estiverem conectados no momento, a data e a hora da última vez em que foram conectados ao servidor, o status de cada computador e outras informações relevantes.</span><span class="sxs-lookup"><span data-stu-id="d0396-106">This includes viewing computers that are currently connected to the server or, if they are not currently connected, the date and time they were last connected to the server, the status of each computer, and other relevant information.</span></span>

-   <span data-ttu-id="d0396-107">[Log de atividades](#bkmk-generatinganactivitylogreport)— Use este relatório para revisar os eventos originados de um host ou usuário específico em um intervalo de datas definido.</span><span class="sxs-lookup"><span data-stu-id="d0396-107">[Activity Log](#bkmk-generatinganactivitylogreport)—Use this report to review events that originated from a specific host or user in a defined date range.</span></span>

-   <span data-ttu-id="d0396-108">[Log de erros](#bkmk-generatinganerrorlogreport)— Use este relatório para exibir os erros originados de um host ou usuário específico em um intervalo de datas definido.</span><span class="sxs-lookup"><span data-stu-id="d0396-108">[Error Log](#bkmk-generatinganerrorlogreport)—Use this report to view errors that originated from a specific host or user in a defined date range.</span></span>

<span data-ttu-id="d0396-109">Os resultados do relatório podem ser classificados por qualquer coluna clicando no nome da coluna apropriada.</span><span class="sxs-lookup"><span data-stu-id="d0396-109">The report results can be sorted by any column by clicking the appropriate column name.</span></span>

<span data-ttu-id="d0396-110">Os resultados do relatório podem ser agrupados arrastando-se um cabeçalho de coluna para a parte superior do relatório.</span><span class="sxs-lookup"><span data-stu-id="d0396-110">The report results can be grouped by dragging a column header to the top of the report.</span></span> <span data-ttu-id="d0396-111">Arraste vários cabeçalhos de coluna para agrupar uma coluna após a outra.</span><span class="sxs-lookup"><span data-stu-id="d0396-111">Drag multiple column headers to group one column after another.</span></span>

## <a href="" id="bkmk-generatingastatusreport"></a><span data-ttu-id="d0396-112">Como gerar um relatório de status</span><span class="sxs-lookup"><span data-stu-id="d0396-112">How to Generate a Status Report</span></span>


**<span data-ttu-id="d0396-113">Para gerar um relatório de status</span><span class="sxs-lookup"><span data-stu-id="d0396-113">To generate a status report</span></span>**

1.  <span data-ttu-id="d0396-114">Clique no botão gerenciamento de **relatórios** .</span><span class="sxs-lookup"><span data-stu-id="d0396-114">Click the **Reports** management button.</span></span>

2.  <span data-ttu-id="d0396-115">No módulo **relatórios** , no menu **tipos de relatório** , selecione **status**e clique em **gerar**.</span><span class="sxs-lookup"><span data-stu-id="d0396-115">In the **Reports** module, on the **Report Types** menu, select **Status**, and click **Generate**.</span></span>

    <span data-ttu-id="d0396-116">A caixa de diálogo parâmetros do relatório é exibida.</span><span class="sxs-lookup"><span data-stu-id="d0396-116">The Report Parameters dialog box appears.</span></span>

3.  <span data-ttu-id="d0396-117">Na caixa de diálogo **parâmetros do relatório** , no campo **número de dias** , insira um número ou use as setas para selecionar o número de dias a serem incluídos no relatório de status e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0396-117">In the **Report Parameters** dialog box, in the **Number of days** field, enter a number or use the arrows to select the number of days to include in the status report, and click **OK**.</span></span>

    <span data-ttu-id="d0396-118">Um relatório de status é gerado.</span><span class="sxs-lookup"><span data-stu-id="d0396-118">A status report is generated.</span></span> <span data-ttu-id="d0396-119">Os parâmetros de relatório são definidos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d0396-119">The report parameters are defined in the following table.</span></span>

**<span data-ttu-id="d0396-120">Propriedades do espaço de trabalho MED-V do cliente</span><span class="sxs-lookup"><span data-stu-id="d0396-120">Client MED-V Workspace Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d0396-121">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d0396-121">Property</span></span></th>
<th align="left"><span data-ttu-id="d0396-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0396-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0396-123">Tempo</span><span class="sxs-lookup"><span data-stu-id="d0396-123">Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-124">A data e a hora em que o evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="d0396-124">The date and time the event occurred.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="d0396-125">Observação</span><span class="sxs-lookup"><span data-stu-id="d0396-125">Note</span></span></strong><br/><p><span data-ttu-id="d0396-126">Por padrão, os eventos são exibidos em ordem decrescente de data.</span><span class="sxs-lookup"><span data-stu-id="d0396-126">By default, the events are displayed in descending date order.</span></span> <span data-ttu-id="d0396-127">No entanto, é possível alterá-lo clicando na coluna tempo recebido.</span><span class="sxs-lookup"><span data-stu-id="d0396-127">However, it can be changed by clicking the Time Received column.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0396-128">Nome do usuário</span><span class="sxs-lookup"><span data-stu-id="d0396-128">User Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-129">O usuário que iniciou o evento.</span><span class="sxs-lookup"><span data-stu-id="d0396-129">The user who initiated the event.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="d0396-130">Observação</span><span class="sxs-lookup"><span data-stu-id="d0396-130">Note</span></span></strong><br/><p><span data-ttu-id="d0396-131">Se o evento ocorreu antes de um usuário se conectar, o nome do usuário será SYSTEM.</span><span class="sxs-lookup"><span data-stu-id="d0396-131">If the event occurred before a user logged on, the user name is SYSTEM.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0396-132">Nome do host</span><span class="sxs-lookup"><span data-stu-id="d0396-132">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-133">O nome do computador host.</span><span class="sxs-lookup"><span data-stu-id="d0396-133">The name of the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0396-134">Nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="d0396-134">Workspace Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-135">O nome do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="d0396-135">The name of the MED-V workspace.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0396-136">Nome do computador do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="d0396-136">Workspace Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-137">O nome do computador no qual o espaço de trabalho do MED-V está em execução.</span><span class="sxs-lookup"><span data-stu-id="d0396-137">The name of the computer the MED-V workspace is running on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0396-138">Online</span><span class="sxs-lookup"><span data-stu-id="d0396-138">Online</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-139">O estado atual do computador cliente:</span><span class="sxs-lookup"><span data-stu-id="d0396-139">The current state of the client computer:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="d0396-140">Terminou</span><span class="sxs-lookup"><span data-stu-id="d0396-140">Stopped</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="d0396-141">Iniciado na &lt; data e hora em que o espaço de trabalho foi iniciado&gt;</span><span class="sxs-lookup"><span data-stu-id="d0396-141">Started at &lt;date and time the workspace was started&gt;</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0396-142">Versão do cliente</span><span class="sxs-lookup"><span data-stu-id="d0396-142">Client Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-143">O número da versão do cliente.</span><span class="sxs-lookup"><span data-stu-id="d0396-143">The version number of the client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0396-144">Versão da política</span><span class="sxs-lookup"><span data-stu-id="d0396-144">Policy Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-145">A versão de política que o espaço de trabalho do MED-V está usando no momento.</span><span class="sxs-lookup"><span data-stu-id="d0396-145">The policy version that the MED-V workspace is currently using.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0396-146">Nome da imagem</span><span class="sxs-lookup"><span data-stu-id="d0396-146">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-147">O nome da imagem.</span><span class="sxs-lookup"><span data-stu-id="d0396-147">The name of the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0396-148">Versão da imagem</span><span class="sxs-lookup"><span data-stu-id="d0396-148">Image Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-149">A versão de imagem que o espaço de trabalho do MED-V está usando no momento.</span><span class="sxs-lookup"><span data-stu-id="d0396-149">The image version that the MED-V workspace is currently using.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="d0396-150">Observação</span><span class="sxs-lookup"><span data-stu-id="d0396-150">Note</span></span></strong><br/><p><span data-ttu-id="d0396-151">A versão do espaço de trabalho do MED-V pode ser desconhecida se ainda não tiver sido baixada em um computador.</span><span class="sxs-lookup"><span data-stu-id="d0396-151">MED-V workspace version can be Unknown if it has not yet been downloaded onto a computer.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganactivitylogreport"></a><span data-ttu-id="d0396-152">Como gerar um relatório de log de atividades</span><span class="sxs-lookup"><span data-stu-id="d0396-152">How to Generate an Activity Log Report</span></span>


**<span data-ttu-id="d0396-153">Para gerar um relatório de log de atividades</span><span class="sxs-lookup"><span data-stu-id="d0396-153">To generate an activity log report</span></span>**

1.  <span data-ttu-id="d0396-154">Clique no botão gerenciamento de **relatórios** .</span><span class="sxs-lookup"><span data-stu-id="d0396-154">Click the **Reports** management button.</span></span>

    <span data-ttu-id="d0396-155">O módulo relatórios é exibido.</span><span class="sxs-lookup"><span data-stu-id="d0396-155">The Reports module appears.</span></span>

2.  <span data-ttu-id="d0396-156">No módulo **relatórios** , no menu **tipos de relatório** , selecione **registro de atividades**e clique em **gerar**.</span><span class="sxs-lookup"><span data-stu-id="d0396-156">In the **Reports** module, on the **Report Types** menu, select **Activity Log**, and click **Generate**.</span></span>

3.  <span data-ttu-id="d0396-157">Na caixa de diálogo **parâmetros de relatório** , configure um ou mais dos seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="d0396-157">In the **Report Parameters** dialog box, configure one or more of the following parameters:</span></span>

    -   <span data-ttu-id="d0396-158">**Número de dias**— o número de dias a serem exibidos no relatório.</span><span class="sxs-lookup"><span data-stu-id="d0396-158">**Number of days**—The number of days to display in the report.</span></span>

    -   <span data-ttu-id="d0396-159">O **nome de usuário contém**— qualquer evento no qual o nome de usuário contém o texto inserido está incluído no relatório.</span><span class="sxs-lookup"><span data-stu-id="d0396-159">**User name contains**—Any event where the user name contains the text entered is included in the report.</span></span>

    -   <span data-ttu-id="d0396-160">O **nome do host contém**— qualquer evento em que o nome do host contém o texto inserido está incluído no relatório.</span><span class="sxs-lookup"><span data-stu-id="d0396-160">**Host name contains**—Any event where the host name contains the text entered is included in the report.</span></span>

4.  <span data-ttu-id="d0396-161">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0396-161">Click **OK**.</span></span>

    <span data-ttu-id="d0396-162">Um relatório é gerado com os eventos e as datas selecionadas.</span><span class="sxs-lookup"><span data-stu-id="d0396-162">A report is generated with the events and dates selected.</span></span> <span data-ttu-id="d0396-163">Os parâmetros de relatório são definidos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d0396-163">The report parameters are defined in the following table.</span></span>

**<span data-ttu-id="d0396-164">Propriedades do relatório do log de atividades</span><span class="sxs-lookup"><span data-stu-id="d0396-164">Activity Log Report Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d0396-165">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d0396-165">Property</span></span></th>
<th align="left"><span data-ttu-id="d0396-166">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0396-166">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0396-167">ID do evento</span><span class="sxs-lookup"><span data-stu-id="d0396-167">Event ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-168">A ID do evento.</span><span class="sxs-lookup"><span data-stu-id="d0396-168">The event ID.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0396-169">Gravidade</span><span class="sxs-lookup"><span data-stu-id="d0396-169">Severity</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="d0396-170">Informações, erro, aviso</span><span class="sxs-lookup"><span data-stu-id="d0396-170">Information, Error, Warning</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0396-171">Categoria</span><span class="sxs-lookup"><span data-stu-id="d0396-171">Category</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-172">O módulo ao qual o relatório se refere.</span><span class="sxs-lookup"><span data-stu-id="d0396-172">The module that the report is referring to.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0396-173">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0396-173">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-174">Uma descrição do evento.</span><span class="sxs-lookup"><span data-stu-id="d0396-174">A description of the event.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0396-175">Hora de recebimento</span><span class="sxs-lookup"><span data-stu-id="d0396-175">Time Received</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-176">A data e a hora em que o evento foi recebido no servidor.</span><span class="sxs-lookup"><span data-stu-id="d0396-176">The date and time the event was received on the server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="d0396-177">Observação</span><span class="sxs-lookup"><span data-stu-id="d0396-177">Note</span></span></strong><br/><p><span data-ttu-id="d0396-178">Se o cliente estiver trabalhando offline, o servidor receberá os relatórios quando o cliente estiver online.</span><span class="sxs-lookup"><span data-stu-id="d0396-178">If the client is working offline, the server receives the reports when the client is online.</span></span></p>
</div>
<div>

</div>
<div class="alert">
<strong><span data-ttu-id="d0396-179">Observação</span><span class="sxs-lookup"><span data-stu-id="d0396-179">Note</span></span></strong><br/><p><span data-ttu-id="d0396-180">Por padrão, os eventos são exibidos em ordem decrescente de data.</span><span class="sxs-lookup"><span data-stu-id="d0396-180">By default, the events are displayed in descending date order.</span></span> <span data-ttu-id="d0396-181">No entanto, é possível alterá-lo clicando na <strong> coluna tempo recebido </strong> .</span><span class="sxs-lookup"><span data-stu-id="d0396-181">However, it can be changed by clicking the <strong>Time Received</strong> column.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0396-182">Tempo do cliente</span><span class="sxs-lookup"><span data-stu-id="d0396-182">Client Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-183">A data e a hora em que o evento ocorreu de acordo com o relógio do cliente.</span><span class="sxs-lookup"><span data-stu-id="d0396-183">The date and time the event occurred according to the client clock.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0396-184">Nome do host</span><span class="sxs-lookup"><span data-stu-id="d0396-184">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-185">O nome do computador host.</span><span class="sxs-lookup"><span data-stu-id="d0396-185">The name of the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0396-186">Nome do usuário</span><span class="sxs-lookup"><span data-stu-id="d0396-186">User Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-187">O usuário que iniciou o evento.</span><span class="sxs-lookup"><span data-stu-id="d0396-187">The user who initiated the event.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0396-188">Nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="d0396-188">Workspace Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-189">O nome do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="d0396-189">The name of the MED-V workspace.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0396-190">Nome do computador do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="d0396-190">Workspace Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-191">O nome do computador no qual o espaço de trabalho do MED-V está em execução.</span><span class="sxs-lookup"><span data-stu-id="d0396-191">The name of the computer the MED-V workspace is running on.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganerrorlogreport"></a><span data-ttu-id="d0396-192">Como gerar um relatório de log de erros</span><span class="sxs-lookup"><span data-stu-id="d0396-192">How to Generate an Error Log Report</span></span>


**<span data-ttu-id="d0396-193">Para gerar um relatório de log de erros</span><span class="sxs-lookup"><span data-stu-id="d0396-193">To generate an error log report</span></span>**

1.  <span data-ttu-id="d0396-194">Clique no botão gerenciamento de **relatórios** .</span><span class="sxs-lookup"><span data-stu-id="d0396-194">Click the **Reports** management button.</span></span>

2.  <span data-ttu-id="d0396-195">No módulo **relatórios** , no menu **tipos de relatório** , selecione **log de erros**e clique em **gerar**.</span><span class="sxs-lookup"><span data-stu-id="d0396-195">In the **Reports** module, on the **Report Types** menu, select **Error Log**, and click **Generate**.</span></span>

3.  <span data-ttu-id="d0396-196">Na caixa de diálogo **parâmetros de relatório** , configure um ou mais dos seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="d0396-196">In the **Report Parameters** dialog box, configure one or more of the following parameters:</span></span>

    -   <span data-ttu-id="d0396-197">**Número de dias**— o número de dias a serem exibidos no relatório.</span><span class="sxs-lookup"><span data-stu-id="d0396-197">**Number of days**—The number of days to display in the report.</span></span>

    -   <span data-ttu-id="d0396-198">O **nome de usuário contém**— qualquer evento no qual o nome de usuário contém o texto inserido está incluído no relatório.</span><span class="sxs-lookup"><span data-stu-id="d0396-198">**User name contains**—Any event where the user name contains the text entered is included in the report.</span></span>

    -   <span data-ttu-id="d0396-199">O **nome do host contém**— qualquer evento em que o nome do host contém o texto inserido está incluído no relatório.</span><span class="sxs-lookup"><span data-stu-id="d0396-199">**Host name contains**—Any event where the host name contains the text entered is included in the report.</span></span>

4.  <span data-ttu-id="d0396-200">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0396-200">Click **OK**.</span></span>

    <span data-ttu-id="d0396-201">Um relatório é gerado com os eventos e as datas selecionadas.</span><span class="sxs-lookup"><span data-stu-id="d0396-201">A report is generated with the events and dates selected.</span></span> <span data-ttu-id="d0396-202">Os parâmetros de relatório são definidos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d0396-202">The report parameters are defined in the following table.</span></span>

**<span data-ttu-id="d0396-203">Propriedades do relatório de log de erros</span><span class="sxs-lookup"><span data-stu-id="d0396-203">Error Log Report Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d0396-204">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d0396-204">Property</span></span></th>
<th align="left"><span data-ttu-id="d0396-205">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0396-205">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0396-206">ID do evento</span><span class="sxs-lookup"><span data-stu-id="d0396-206">Event ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-207">A ID do evento.</span><span class="sxs-lookup"><span data-stu-id="d0396-207">The event ID.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0396-208">Categoria</span><span class="sxs-lookup"><span data-stu-id="d0396-208">Category</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-209">O módulo ao qual o relatório se refere.</span><span class="sxs-lookup"><span data-stu-id="d0396-209">The module that the report is referring to.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0396-210">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0396-210">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-211">Uma descrição do evento.</span><span class="sxs-lookup"><span data-stu-id="d0396-211">A description of the event.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0396-212">Hora de recebimento</span><span class="sxs-lookup"><span data-stu-id="d0396-212">Time Received</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-213">A data e a hora em que o evento foi recebido no servidor.</span><span class="sxs-lookup"><span data-stu-id="d0396-213">The date and time the event was received on the server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="d0396-214">Observação</span><span class="sxs-lookup"><span data-stu-id="d0396-214">Note</span></span></strong><br/><p><span data-ttu-id="d0396-215">Se o cliente estiver trabalhando offline, o servidor receberá os relatórios quando o cliente estiver online.</span><span class="sxs-lookup"><span data-stu-id="d0396-215">If the client is working offline, the server receives the reports when the client is online.</span></span></p>
</div>
<div>

</div>
<div class="alert">
<strong><span data-ttu-id="d0396-216">Observação</span><span class="sxs-lookup"><span data-stu-id="d0396-216">Note</span></span></strong><br/><p><span data-ttu-id="d0396-217">Por padrão, os eventos são exibidos em ordem decrescente de data.</span><span class="sxs-lookup"><span data-stu-id="d0396-217">By default, the events are displayed in descending date order.</span></span> <span data-ttu-id="d0396-218">No entanto, é possível alterá-lo clicando na <strong> coluna tempo recebido </strong> .</span><span class="sxs-lookup"><span data-stu-id="d0396-218">However, it can be changed by clicking the <strong>Time Received</strong> column.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0396-219">Tempo do cliente</span><span class="sxs-lookup"><span data-stu-id="d0396-219">Client Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-220">A data e a hora em que o evento ocorreu de acordo com o relógio do cliente.</span><span class="sxs-lookup"><span data-stu-id="d0396-220">The date and time the event occurred according to the client clock.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0396-221">Nome do host</span><span class="sxs-lookup"><span data-stu-id="d0396-221">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-222">O nome do computador host.</span><span class="sxs-lookup"><span data-stu-id="d0396-222">The name of the host computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0396-223">Nome do usuário</span><span class="sxs-lookup"><span data-stu-id="d0396-223">User Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-224">O usuário que iniciou o evento.</span><span class="sxs-lookup"><span data-stu-id="d0396-224">The user who initiated the event.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0396-225">Nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="d0396-225">Workspace Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="d0396-226">O nome do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="d0396-226">The name of the MED-V workspace.</span></span></p></td>
</tr>
</tbody>
</table>











