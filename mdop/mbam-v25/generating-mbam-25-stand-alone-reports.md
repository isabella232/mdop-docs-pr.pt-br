---
title: Gerando relatórios autônomos do MBAM 2.5
description: Gerando relatórios autônomos do MBAM 2.5
author: dansimp
ms.assetid: 0ec623ff-5155-4906-aef2-20cdc0f84667
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: e1c6b33de26cce5d9ad8d20461dbe0ea0f138c78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799209"
---
# <span data-ttu-id="1e651-103">Gerando relatórios autônomos do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1e651-103">Generating MBAM 2.5 Stand-alone Reports</span></span>


<span data-ttu-id="1e651-104">Ao configurar o Microsoft BitLocker Administration and Monitoring (MBAM) with the autônomo Topology, você pode gerar relatórios para monitorar o uso e a conformidade de criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1e651-104">When you configure Microsoft BitLocker Administration and Monitoring (MBAM) with the Stand-alone topology, you can generate reports to monitor BitLocker drive encryption usage and compliance.</span></span> <span data-ttu-id="1e651-105">Este tópico contém os seguintes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="1e651-105">This topic contains the following procedures:</span></span>

-   [<span data-ttu-id="1e651-106">Para abrir o site de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="1e651-106">To open the Administration and Monitoring Website</span></span>](#bkmk-openadmin)

-   [<span data-ttu-id="1e651-107">Para gerar um relatório de conformidade empresarial</span><span class="sxs-lookup"><span data-stu-id="1e651-107">To generate an Enterprise Compliance Report</span></span>](#bkmk-enterprise)

-   [<span data-ttu-id="1e651-108">Para gerar um relatório de conformidade do computador</span><span class="sxs-lookup"><span data-stu-id="1e651-108">To generate a Computer Compliance Report</span></span>](#bkmk-computercomp)

-   [<span data-ttu-id="1e651-109">Para gerar um relatório de auditoria de chave de recuperação</span><span class="sxs-lookup"><span data-stu-id="1e651-109">To generate a Recovery Key Audit Report</span></span>](#bkmk-recoverykey)

<span data-ttu-id="1e651-110">Para obter descrições dos relatórios autônomos, consulte [compreendendo os relatórios](understanding-mbam-25-stand-alone-reports.md)autônomos do MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="1e651-110">For descriptions of the Stand-alone reports, see [Understanding MBAM 2.5 Stand-alone Reports](understanding-mbam-25-stand-alone-reports.md).</span></span>

<span data-ttu-id="1e651-111">**Observação**  Para executar os relatórios, você deve ser membro do grupo **usuários de relatório do MBAM** , que você pode configurar nos serviços de domínio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1e651-111">**Note** To run the reports, you must be a member of the **MBAM Report Users** group, which you configure in Active Directory Domain Services.</span></span> <span data-ttu-id="1e651-112">Para obter mais informações, consulte [planejando para contas e grupos do MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="1e651-112">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md).</span></span>

 

<a href="" id="bkmk-openadmin"></a>**<span data-ttu-id="1e651-113">Para abrir o site de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="1e651-113">To open the Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="1e651-114">Abra um navegador da Web e navegue até o site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="1e651-114">Open a web browser and navigate to the Administration and Monitoring Website.</span></span> <span data-ttu-id="1e651-115">A URL padrão para o site de administração e monitoramento é:</span><span class="sxs-lookup"><span data-stu-id="1e651-115">The default URL for the Administration and Monitoring Website is:</span></span>

    *<span data-ttu-id="1e651-116">http (s):// &lt; MBAMAdministrationServerName &gt; : &lt; porta &gt; /helpdesk</span><span class="sxs-lookup"><span data-stu-id="1e651-116">http(s)://&lt;MBAMAdministrationServerName&gt;:&lt;port&gt;/Helpdesk</span></span>*

2.  <span data-ttu-id="1e651-117">No painel esquerdo, clique em **relatórios**.</span><span class="sxs-lookup"><span data-stu-id="1e651-117">In the left pane, click **Reports**.</span></span> <span data-ttu-id="1e651-118">Na barra de menus superior, selecione o relatório que você deseja executar.</span><span class="sxs-lookup"><span data-stu-id="1e651-118">From the top menu bar, select the report you want to run.</span></span>

    <span data-ttu-id="1e651-119">Os dados do cliente MBAM são mantidos no banco de dados de conformidade e auditoria para referência histórica, caso um computador seja perdido ou roubado.</span><span class="sxs-lookup"><span data-stu-id="1e651-119">MBAM client data is retained in the Compliance and Audit Database for historical reference in case a computer is lost or stolen.</span></span> <span data-ttu-id="1e651-120">Ao executar relatórios corporativos, recomendamos que você use as datas de início e de término adequadas para fazer o escopo dos quadros de tempo dos relatórios de uma a duas semanas para aumentar a precisão dos dados de relatório.</span><span class="sxs-lookup"><span data-stu-id="1e651-120">When running enterprise reports, we recommend that you use appropriate start and end dates to scope the time frames for the reports from one to two weeks to increase reporting data accuracy.</span></span>

    <span data-ttu-id="1e651-121">Depois de gerar um relatório, você pode salvar os resultados em formatos diferentes, como HTML, Microsoft Word e Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="1e651-121">After you generate a report, you can save the results in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

    <span data-ttu-id="1e651-122">**Observação**  Configure o SQL Server Reporting Services (SSRS) para usar SSL (Secure Sockets Layer) antes de configurar o site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="1e651-122">**Note** Configure SQL Server Reporting Services (SSRS) to use Secure Sockets Layer (SSL) before configuring the Administration and Monitoring Website.</span></span> <span data-ttu-id="1e651-123">Se, por algum motivo, o SSRS não estiver configurado para usar SSL, a URL dos relatórios será definida como HTTP em vez de HTTPS quando você configurar o site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="1e651-123">If, for any reason, SSRS is not configured to use SSL, the URL for the Reports will be set to HTTP instead of to HTTPS when you configure the Administration and Monitoring Website.</span></span> <span data-ttu-id="1e651-124">Se, em seguida, você acessar o site de administração e monitoramento e selecionar um relatório, a seguinte mensagem será exibida: "somente conteúdo seguro é exibido".</span><span class="sxs-lookup"><span data-stu-id="1e651-124">If you then go to the Administration and Monitoring Website and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span> <span data-ttu-id="1e651-125">Para mostrar o relatório, clique em **mostrar todo o conteúdo**.</span><span class="sxs-lookup"><span data-stu-id="1e651-125">To show the report, click **Show All Content**.</span></span>

     

<a href="" id="bkmk-enterprise"></a>**<span data-ttu-id="1e651-126">Para gerar um relatório de conformidade empresarial</span><span class="sxs-lookup"><span data-stu-id="1e651-126">To generate an Enterprise Compliance Report</span></span>**

1.  <span data-ttu-id="1e651-127">No site Administração e monitoramento, selecione o nó **relatórios** no painel de navegação à esquerda, selecione **relatório de conformidade empresarial**e selecione os filtros que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="1e651-127">From the Administration and Monitoring Website, select the **Reports** node from the left navigation pane, select **Enterprise Compliance Report**, and select the filters that you want to use.</span></span> <span data-ttu-id="1e651-128">Os filtros disponíveis para o relatório de conformidade empresarial são:</span><span class="sxs-lookup"><span data-stu-id="1e651-128">The available filters for the Enterprise Compliance Report are:</span></span>

    -   <span data-ttu-id="1e651-129">**Status de conformidade**.</span><span class="sxs-lookup"><span data-stu-id="1e651-129">**Compliance Status**.</span></span> <span data-ttu-id="1e651-130">Use esse filtro para especificar os tipos de status de conformidade do relatório (por exemplo, compatível ou não conforme).</span><span class="sxs-lookup"><span data-stu-id="1e651-130">Use this filter to specify the compliance status types of the report (for example, Compliant or Noncompliant).</span></span>

    -   <span data-ttu-id="1e651-131">**Estado do erro**.</span><span class="sxs-lookup"><span data-stu-id="1e651-131">**Error State**.</span></span> <span data-ttu-id="1e651-132">Use esse filtro para especificar os tipos de estado de erro do relatório (por exemplo, nenhum erro ou erro).</span><span class="sxs-lookup"><span data-stu-id="1e651-132">Use this filter to specify the error state types of the report (for example, No Error or Error).</span></span>

2.  <span data-ttu-id="1e651-133">Clique em **Exibir relatório** para exibir o relatório selecionado.</span><span class="sxs-lookup"><span data-stu-id="1e651-133">Click **View Report** to display the selected report.</span></span>

3.  <span data-ttu-id="1e651-134">Selecione um nome de computador para exibir informações sobre o computador no relatório de conformidade do computador.</span><span class="sxs-lookup"><span data-stu-id="1e651-134">Select a computer name to view information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="1e651-135">Selecione o sinal de adição (+) ao lado do nome do computador para exibir informações sobre os volumes do computador.</span><span class="sxs-lookup"><span data-stu-id="1e651-135">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

<a href="" id="bkmk-computercomp"></a>**<span data-ttu-id="1e651-136">Para gerar um relatório de conformidade do computador</span><span class="sxs-lookup"><span data-stu-id="1e651-136">To generate a Computer Compliance Report</span></span>**

1.  <span data-ttu-id="1e651-137">No site Administração e monitoramento, selecione o nó do **relatório** no painel de navegação à esquerda e selecione **relatório de conformidade do computador**.</span><span class="sxs-lookup"><span data-stu-id="1e651-137">From the Administration and Monitoring Website, select the **Report** node from the left navigation pane, and then select **Computer Compliance Report**.</span></span> <span data-ttu-id="1e651-138">Use o relatório de conformidade do computador para pesquisar o **nome de usuário** ou o **nome do computador**.</span><span class="sxs-lookup"><span data-stu-id="1e651-138">Use the Computer Compliance Report to search for **User name** or **Computer name**.</span></span>

2.  <span data-ttu-id="1e651-139">Clique em **Exibir relatório** para ver o relatório de conformidade do computador.</span><span class="sxs-lookup"><span data-stu-id="1e651-139">Click **View Report** to view the Computer Compliance Report.</span></span>

3.  <span data-ttu-id="1e651-140">Selecione um nome de computador para exibir mais informações sobre o computador no relatório de conformidade do computador.</span><span class="sxs-lookup"><span data-stu-id="1e651-140">Select a computer name to display more information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="1e651-141">Selecione o sinal de adição (+) ao lado do nome do computador para exibir informações sobre os volumes do computador.</span><span class="sxs-lookup"><span data-stu-id="1e651-141">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

    <span data-ttu-id="1e651-142">**Observação**  Um computador cliente MBAM é considerado compatível se o computador corresponder ou exceder os requisitos das configurações da política de grupo do MBAM.</span><span class="sxs-lookup"><span data-stu-id="1e651-142">**Note** An MBAM client computer is considered compliant if the computer matches or exceeds the requirements of the MBAM Group Policy settings.</span></span>

<a href="" id="bkmk-recoverykey"></a>**<span data-ttu-id="1e651-143">Para gerar um relatório de auditoria de chave de recuperação</span><span class="sxs-lookup"><span data-stu-id="1e651-143">To generate a Recovery Key Audit Report</span></span>**

1.  <span data-ttu-id="1e651-144">No site Administração e monitoramento, selecione o nó do **relatório** no painel de navegação à esquerda e selecione **relatório de auditoria de recuperação**.</span><span class="sxs-lookup"><span data-stu-id="1e651-144">From the Administration and Monitoring Website, select the **Report** node in the left navigation pane, and then select **Recovery Audit Report**.</span></span> <span data-ttu-id="1e651-145">Selecione os filtros para o relatório de auditoria de chave de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1e651-145">Select the filters for your Recovery Key Audit Report.</span></span> <span data-ttu-id="1e651-146">Os filtros disponíveis para auditoria de chave de recuperação são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="1e651-146">The available filters for recovery key audits are as follows:</span></span>

    -   <span data-ttu-id="1e651-147">**Usuário da assistência técnica**.</span><span class="sxs-lookup"><span data-stu-id="1e651-147">**Helpdesk User**.</span></span> <span data-ttu-id="1e651-148">Esse filtro permite que os usuários especifiquem o nome de usuário do solicitante.</span><span class="sxs-lookup"><span data-stu-id="1e651-148">This filter enables users to specify the user name of the requester.</span></span> <span data-ttu-id="1e651-149">O solicitante é a pessoa da assistência técnica que acessou a chave em nome de um usuário final.</span><span class="sxs-lookup"><span data-stu-id="1e651-149">The requester is the person in the Help Desk who accessed the key on behalf of an end user.</span></span>

    -   <span data-ttu-id="1e651-150">**Usuário final**.</span><span class="sxs-lookup"><span data-stu-id="1e651-150">**End User**.</span></span> <span data-ttu-id="1e651-151">Esse filtro permite que os usuários especifiquem o nome de usuário do solicitante.</span><span class="sxs-lookup"><span data-stu-id="1e651-151">This filter enables users to specify the user name of the requestee.</span></span> <span data-ttu-id="1e651-152">O solicitante é o usuário final que chamou o suporte técnico para obter uma chave de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1e651-152">The requestee is the end user who called the Help Desk to obtain a recovery key.</span></span>

    -   <span data-ttu-id="1e651-153">**Resultado da solicitação**.</span><span class="sxs-lookup"><span data-stu-id="1e651-153">**Request Result**.</span></span> <span data-ttu-id="1e651-154">Esse filtro permite que os usuários especifiquem os tipos de resultados de solicitação (por exemplo, sucesso ou falha) em que desejam basear o relatório.</span><span class="sxs-lookup"><span data-stu-id="1e651-154">This filter enables users to specify the request result types (for example, Success or Failed) that they want to base the report on.</span></span> <span data-ttu-id="1e651-155">Por exemplo, os usuários podem querer ver as tentativas de acesso à chave que falharam.</span><span class="sxs-lookup"><span data-stu-id="1e651-155">For example, users may want to view failed key access attempts.</span></span>

    -   <span data-ttu-id="1e651-156">**Tipo de chave**.</span><span class="sxs-lookup"><span data-stu-id="1e651-156">**Key Type**.</span></span> <span data-ttu-id="1e651-157">Esse filtro permite que os usuários especifiquem o tipo de chave (por exemplo, a senha da chave de recuperação ou o hash de senha do TPM) em que desejam basear o relatório.</span><span class="sxs-lookup"><span data-stu-id="1e651-157">This filter enables users to specify the key type (for example, Recovery Key Password or TPM Password Hash) that they want to base the report on.</span></span>

    -   <span data-ttu-id="1e651-158">**Data de início**.</span><span class="sxs-lookup"><span data-stu-id="1e651-158">**Start Date**.</span></span> <span data-ttu-id="1e651-159">Esse filtro é usado para definir a parte de data de início do intervalo de datas que o usuário quer relatar.</span><span class="sxs-lookup"><span data-stu-id="1e651-159">This filter is used to define the Start Date part of the date range that the user wants to report on.</span></span>

    -   <span data-ttu-id="1e651-160">**Data de término**.</span><span class="sxs-lookup"><span data-stu-id="1e651-160">**End Date**.</span></span> <span data-ttu-id="1e651-161">Esse filtro é usado para definir a parte de data de término do intervalo de datas que os usuários desejam relatar.</span><span class="sxs-lookup"><span data-stu-id="1e651-161">This filter is used to define the End Date part of the date range that the users want to report on.</span></span>

2.  <span data-ttu-id="1e651-162">Clique em **Exibir relatório** para exibir o relatório.</span><span class="sxs-lookup"><span data-stu-id="1e651-162">Click **View Report** to view the report.</span></span>



## <span data-ttu-id="1e651-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e651-163">Related topics</span></span>


[<span data-ttu-id="1e651-164">Monitorando e gerando relatórios de conformidade do BitLocker com o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1e651-164">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[<span data-ttu-id="1e651-165">Noções básicas sobre relatórios autônomos do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1e651-165">Understanding MBAM 2.5 Stand-alone Reports</span></span>](understanding-mbam-25-stand-alone-reports.md)

 

## <span data-ttu-id="1e651-166">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="1e651-166">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="1e651-167">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="1e651-167">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="1e651-168">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="1e651-168">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





