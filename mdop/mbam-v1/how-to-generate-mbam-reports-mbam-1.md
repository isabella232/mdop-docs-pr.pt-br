---
title: Como gerar relatórios do MBAM
description: Como gerar relatórios do MBAM
author: dansimp
ms.assetid: cdf4ae76-040c-447c-8736-c9e57068d221
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f0b5a4e984d7a609eab7204e67f46042992f586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799490"
---
# <span data-ttu-id="beb2c-103">Como gerar relatórios do MBAM</span><span class="sxs-lookup"><span data-stu-id="beb2c-103">How to Generate MBAM Reports</span></span>


<span data-ttu-id="beb2c-104">O monitoramento e a administração do Microsoft BitLocker (MBAM) geram vários relatórios para monitorar o uso e a conformidade de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="beb2c-104">Microsoft BitLocker Administration and Monitoring (MBAM) generates various reports to monitor BitLocker encryption usage and compliance.</span></span> <span data-ttu-id="beb2c-105">Este tópico descreve como abrir o site de administração do MBAM e como gerar relatórios do MBAM sobre conformidade empresarial, computadores individuais, compatibilidade de hardware e atividade de recuperação de chave.</span><span class="sxs-lookup"><span data-stu-id="beb2c-105">This topic describes how to open the MBAM administration website and how to generate MBAM reports on enterprise compliance, individual computers, hardware compatibility, and key recovery activity.</span></span> <span data-ttu-id="beb2c-106">Para obter mais informações sobre os relatórios do MBAM, consulte [noções básicas sobre relatórios do MBAM](understanding-mbam-reports-mbam-1.md).</span><span class="sxs-lookup"><span data-stu-id="beb2c-106">For more information about MBAM reports, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-1.md).</span></span>

<span data-ttu-id="beb2c-107">**Observação**  Para executar os relatórios, você deve ser membro da função de **usuários de relatório** nos computadores em que você instalou os recursos de servidor de administração e monitoramento, banco de dados de auditoria e conformidade e relatórios de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="beb2c-107">**Note** To run the reports, you must be a member of the **Report Users** role on the computers where you have installed the Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports.</span></span>

 

**<span data-ttu-id="beb2c-108">Para abrir o site de administração do MBAM</span><span class="sxs-lookup"><span data-stu-id="beb2c-108">To open the MBAM Administration website</span></span>**

1.  <span data-ttu-id="beb2c-109">Abra um navegador da Web e navegue até o site do MBAM.</span><span class="sxs-lookup"><span data-stu-id="beb2c-109">Open a web browser and navigate to the MBAM website.</span></span> <span data-ttu-id="beb2c-110">A URL padrão do site é \*http:// &lt; NomeDoComputador &gt; \* do servidor de administração e monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="beb2c-110">The default URL for the website is *http://&lt;computername&gt;* of the Microsoft BitLocker Administration and Monitoring server.</span></span>

    <span data-ttu-id="beb2c-111">**Observação**  Se o site do MBAMadministration foi instalado em uma porta que não seja a porta 80, você deve especificar o número da porta na URL.</span><span class="sxs-lookup"><span data-stu-id="beb2c-111">**Note** If the MBAMadministration website was installed on a port other than port 80, you must specify that port number in the URL.</span></span> <span data-ttu-id="beb2c-112">Por exemplo, \*http:// &lt; NomeDoComputador &gt; : &lt; Port &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="beb2c-112">For example, *http://&lt;computername&gt;:&lt;port&gt;*.</span></span> <span data-ttu-id="beb2c-113">Se você especificou um nome de host para o site do MBAMadministration durante a instalação, a URL seria \*http:// &lt; hostname &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="beb2c-113">If you specified a Host Name for the MBAMadministration website during the installation, the URL would be *http://&lt;hostname&gt;*.</span></span>

     

2.  <span data-ttu-id="beb2c-114">No painel de navegação, clique em **relatórios**.</span><span class="sxs-lookup"><span data-stu-id="beb2c-114">In the navigation pane, click **Reports**.</span></span> <span data-ttu-id="beb2c-115">No painel principal, clique na guia do tipo de relatório: **relatório de conformidade empresarial**, **relatório de conformidade do computador**, relatório de auditoria de **hardware**ou relatório de **auditoria de recuperação**.</span><span class="sxs-lookup"><span data-stu-id="beb2c-115">In the main pane, click the tab for your report type: **Enterprise Compliance Report**, **Computer Compliance Report**, **Hardware Audit Report**, or **Recovery Audit Report**.</span></span>

    <span data-ttu-id="beb2c-116">**Observação**  Os dados do cliente MBAM históricos são mantidos no banco de dados de conformidade.</span><span class="sxs-lookup"><span data-stu-id="beb2c-116">**Note** Historical MBAM Client data is retained in the compliance database.</span></span> <span data-ttu-id="beb2c-117">Esses dados retidos podem ser necessários caso um computador seja perdido ou roubado.</span><span class="sxs-lookup"><span data-stu-id="beb2c-117">This retained data may be needed in case a computer is lost or stolen.</span></span> <span data-ttu-id="beb2c-118">Ao executar relatórios corporativos, você deve usar as datas de início e de término adequadas para fazer o escopo dos quadros de tempo dos relatórios de uma a duas semanas para aumentar a precisão dos dados de relatório.</span><span class="sxs-lookup"><span data-stu-id="beb2c-118">When running enterprise reports, you should use appropriate start and end dates to scope the time frames for the reports from one to two weeks to increase the reporting data accuracy.</span></span>

     

**<span data-ttu-id="beb2c-119">Para gerar um relatório de conformidade empresarial</span><span class="sxs-lookup"><span data-stu-id="beb2c-119">To generate an enterprise Compliance Report</span></span>**

1.  <span data-ttu-id="beb2c-120">No site do MBAMadministration, clique em **relatórios** no painel de navegação e, em seguida, clique na guia **relatório de conformidade empresarial** e selecione os filtros apropriados para o seu relatório.</span><span class="sxs-lookup"><span data-stu-id="beb2c-120">On the MBAMadministration website, click **Reports** in the navigation pane, then click the **Enterprise Compliance Report** tab and select the appropriate filters for your report.</span></span> <span data-ttu-id="beb2c-121">Para o relatório de conformidade empresarial, você pode definir os filtros a seguir.</span><span class="sxs-lookup"><span data-stu-id="beb2c-121">For the Enterprise Compliance Report, you can set the following filters.</span></span>

    -   <span data-ttu-id="beb2c-122">**Status de conformidade**.</span><span class="sxs-lookup"><span data-stu-id="beb2c-122">**Compliance Status**.</span></span> <span data-ttu-id="beb2c-123">Use esse filtro para especificar os tipos de status de conformidade (por exemplo, compatíveis ou não conformes) a serem incluídos no relatório.</span><span class="sxs-lookup"><span data-stu-id="beb2c-123">Use this filter to specify the compliance status types (for example, Compliant or Noncompliant) to include in the report.</span></span>

    -   <span data-ttu-id="beb2c-124">**Estado do erro**.</span><span class="sxs-lookup"><span data-stu-id="beb2c-124">**Error State**.</span></span> <span data-ttu-id="beb2c-125">Use esse filtro para especificar os tipos de estado de erro, como nenhum erro ou erro, a ser incluído no relatório.</span><span class="sxs-lookup"><span data-stu-id="beb2c-125">Use this filter to specify the Error State types, such as No Error or Error, to include in the report.</span></span>

2.  <span data-ttu-id="beb2c-126">Clique em **Exibir relatório** para exibir o relatório especificado.</span><span class="sxs-lookup"><span data-stu-id="beb2c-126">Click **View Report** to display the specified report.</span></span>

    <span data-ttu-id="beb2c-127">Os resultados do relatório podem ser salvos em qualquer um dos vários formatos de arquivo disponíveis, como HTML, Microsoft Word e Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="beb2c-127">The report results can be saved in any of several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

    <span data-ttu-id="beb2c-128">**Observação**  O relatório de conformidade empresarial é gerado por um trabalho do SQL que é executado a cada seis horas.</span><span class="sxs-lookup"><span data-stu-id="beb2c-128">**Note** The Enterprise Compliance report is generated by a SQL job that runs every six hours.</span></span> <span data-ttu-id="beb2c-129">Portanto, na primeira vez que você tentar exibir o relatório, verá que alguns dados estão ausentes.</span><span class="sxs-lookup"><span data-stu-id="beb2c-129">Therefore, the first time you try to view the report you may find that some data is missing.</span></span>

     

3.  <span data-ttu-id="beb2c-130">Para exibir informações sobre um computador no relatório de conformidade do computador, selecione o nome do computador.</span><span class="sxs-lookup"><span data-stu-id="beb2c-130">To view information about a computer in the Computer Compliance Report, select the computer name.</span></span>

4.  <span data-ttu-id="beb2c-131">Selecione o sinal de adição (+) ao lado do nome do computador para exibir informações sobre os volumes do computador.</span><span class="sxs-lookup"><span data-stu-id="beb2c-131">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

**<span data-ttu-id="beb2c-132">Para gerar o relatório de conformidade do computador</span><span class="sxs-lookup"><span data-stu-id="beb2c-132">To generate the Computer Compliance Report</span></span>**

1.  <span data-ttu-id="beb2c-133">No site do MBAMadministration, selecione o nó do **relatório** no painel de navegação e selecione o **relatório de conformidade do computador**.</span><span class="sxs-lookup"><span data-stu-id="beb2c-133">In the MBAMadministration website, select the **Report** node in the navigation pane, and then select the **Computer Compliance Report**.</span></span> <span data-ttu-id="beb2c-134">Use o relatório de conformidade do computador para pesquisar o **nome de usuário** ou o **nome do computador**.</span><span class="sxs-lookup"><span data-stu-id="beb2c-134">Use the Computer Compliance report to search for **user name** or **computer name**.</span></span>

2.  <span data-ttu-id="beb2c-135">Clique em **Exibir relatório** para ver o relatório do computador.</span><span class="sxs-lookup"><span data-stu-id="beb2c-135">Click **View Report** to view the computer report.</span></span>

    <span data-ttu-id="beb2c-136">Os resultados podem ser salvos em qualquer um dos vários formatos de arquivo disponíveis, como HTML, Microsoft Word e Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="beb2c-136">Results can be saved in any of several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

3.  <span data-ttu-id="beb2c-137">Para exibir mais informações sobre um computador no relatório de conformidade do computador, selecione o nome do computador.</span><span class="sxs-lookup"><span data-stu-id="beb2c-137">To display more information about a computer in the Computer Compliance Report, select the computer name.</span></span>

4.  <span data-ttu-id="beb2c-138">Selecione o sinal de adição (+) ao lado do nome do computador para exibir informações sobre os volumes do computador.</span><span class="sxs-lookup"><span data-stu-id="beb2c-138">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

    <span data-ttu-id="beb2c-139">**Observação**  Um computador cliente MBAM é considerado compatível se o computador atender aos requisitos das configurações da política do MBAM ou se o modelo de hardware do computador estiver definido como incompatível.</span><span class="sxs-lookup"><span data-stu-id="beb2c-139">**Note** An MBAM Client computer is considered compliant if the computer matches the requirements of the MBAM policy settings or the computer’s hardware model is set to incompatible.</span></span> <span data-ttu-id="beb2c-140">Portanto, quando você estiver exibindo informações detalhadas sobre os volumes de disco associados ao computador, os computadores isentos da criptografia do BitLocker devido à compatibilidade de hardware poderão ser exibidos como compatíveis, mesmo que o status da criptografia do volume da unidade seja exibido como não compatível.</span><span class="sxs-lookup"><span data-stu-id="beb2c-140">Therefore, when you are viewing detailed information about the disk volumes associated with the computer, computers that are exempt from BitLocker encryption due to hardware compatibility can be displayed as compliant even though their drive volume encryption status is displayed as noncompliant.</span></span>

     

**<span data-ttu-id="beb2c-141">Para gerar o relatório de auditoria de compatibilidade de hardware</span><span class="sxs-lookup"><span data-stu-id="beb2c-141">To generate the Hardware Compatibility Audit Report</span></span>**

1.  <span data-ttu-id="beb2c-142">No site do MBAMadministration, selecione o nó do **relatório** no painel de navegação e selecione o **relatório de auditoria de hardware**.</span><span class="sxs-lookup"><span data-stu-id="beb2c-142">From the MBAMadministration website, select the **Report** node from the navigation pane, and then select the **Hardware Audit Report**.</span></span> <span data-ttu-id="beb2c-143">Selecione os filtros apropriados para o seu relatório de auditoria de hardware.</span><span class="sxs-lookup"><span data-stu-id="beb2c-143">Select the appropriate filters for your Hardware Audit report.</span></span> <span data-ttu-id="beb2c-144">O relatório de auditoria de hardware oferece os seguintes filtros disponíveis:</span><span class="sxs-lookup"><span data-stu-id="beb2c-144">The Hardware Audit report offers the following available filters:</span></span>

    -   <span data-ttu-id="beb2c-145">**Usuário (Domain\\User)**.</span><span class="sxs-lookup"><span data-stu-id="beb2c-145">**User (Domain\\User)**.</span></span> <span data-ttu-id="beb2c-146">Especifica o nome do usuário que fez uma alteração.</span><span class="sxs-lookup"><span data-stu-id="beb2c-146">Specifies the name of the user who made a change.</span></span>

    -   <span data-ttu-id="beb2c-147">**Tipo de alteração**.</span><span class="sxs-lookup"><span data-stu-id="beb2c-147">**Change Type**.</span></span> <span data-ttu-id="beb2c-148">Especifica o tipo de alterações que você está procurando.</span><span class="sxs-lookup"><span data-stu-id="beb2c-148">Specifies the type of changes you are looking for.</span></span>

    -   <span data-ttu-id="beb2c-149">**Data de início**.</span><span class="sxs-lookup"><span data-stu-id="beb2c-149">**Start Date**.</span></span> <span data-ttu-id="beb2c-150">Especifica a parte de data de início do intervalo de datas que você deseja relatar.</span><span class="sxs-lookup"><span data-stu-id="beb2c-150">Specifies the Start Date part of the date range that you want to report on.</span></span>

    -   <span data-ttu-id="beb2c-151">**Data de término**.</span><span class="sxs-lookup"><span data-stu-id="beb2c-151">**End Date**.</span></span> <span data-ttu-id="beb2c-152">Especifica a parte de data de término do intervalo de datas que você deseja relatar.</span><span class="sxs-lookup"><span data-stu-id="beb2c-152">Specifies the End Date part of the date range that you want to report on.</span></span>

2.  <span data-ttu-id="beb2c-153">Clique em **Exibir relatório** para exibir o relatório.</span><span class="sxs-lookup"><span data-stu-id="beb2c-153">Click **View Report** to view the report.</span></span>

    <span data-ttu-id="beb2c-154">Os resultados podem ser salvos em vários formatos de arquivo disponíveis, como HTML, Microsoft Word e Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="beb2c-154">Results can be saved in several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

**<span data-ttu-id="beb2c-155">Para gerar o relatório de auditoria de chave de recuperação</span><span class="sxs-lookup"><span data-stu-id="beb2c-155">To generate the Recovery Key Audit Report</span></span>**

1.  <span data-ttu-id="beb2c-156">No site do MBAMadministration, selecione o nó do **relatório** no painel de navegação e, em seguida, selecione o **relatório de auditoria de recuperação**.</span><span class="sxs-lookup"><span data-stu-id="beb2c-156">From the MBAMadministration website, select the **Report** node in the navigation pane, and then select the **Recovery Audit Report**.</span></span> <span data-ttu-id="beb2c-157">Selecione os filtros para o relatório de auditoria de chave de recuperação.</span><span class="sxs-lookup"><span data-stu-id="beb2c-157">Select the filters for your Recovery Key Audit report.</span></span> <span data-ttu-id="beb2c-158">Os filtros disponíveis para auditoria de chave de recuperação são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="beb2c-158">The available filters for Recovery Key audits are as follows:</span></span>

    -   <span data-ttu-id="beb2c-159">**Solicitante**.</span><span class="sxs-lookup"><span data-stu-id="beb2c-159">**Requestor**.</span></span> <span data-ttu-id="beb2c-160">Especifica o nome de usuário do solicitante.</span><span class="sxs-lookup"><span data-stu-id="beb2c-160">Specifies the user name of the requestor.</span></span> <span data-ttu-id="beb2c-161">O solicitante é a pessoa da assistência técnica que acessou a chave em nome de um usuário.</span><span class="sxs-lookup"><span data-stu-id="beb2c-161">The requestor is the person in the help desk who accessed the key on behalf of a user.</span></span>

    -   <span data-ttu-id="beb2c-162">**Solicitante**.</span><span class="sxs-lookup"><span data-stu-id="beb2c-162">**Requestee**.</span></span> <span data-ttu-id="beb2c-163">Especifica o nome de usuário do solicitante.</span><span class="sxs-lookup"><span data-stu-id="beb2c-163">Specifies the user name of the requestee.</span></span> <span data-ttu-id="beb2c-164">O solicitante é a pessoa que chamou o suporte técnico para obter uma chave de recuperação.</span><span class="sxs-lookup"><span data-stu-id="beb2c-164">The requestee is the person who called the help desk to obtain a recovery key.</span></span>

    -   <span data-ttu-id="beb2c-165">**Resultado da solicitação** Especifica os tipos de resultado de solicitação, como: sucesso ou falha.</span><span class="sxs-lookup"><span data-stu-id="beb2c-165">**Request Result** Specifies the request result types, such as: Success or Failed.</span></span> <span data-ttu-id="beb2c-166">Por exemplo, você pode querer ver as tentativas de acesso à chave que falharam.</span><span class="sxs-lookup"><span data-stu-id="beb2c-166">For example, you may want to view failed key access attempts.</span></span>

    -   <span data-ttu-id="beb2c-167">**Tipo de chave**.</span><span class="sxs-lookup"><span data-stu-id="beb2c-167">**Key Type**.</span></span> <span data-ttu-id="beb2c-168">Especifica o tipo de chave, como: senha da chave de recuperação ou hash de senha do TPM.</span><span class="sxs-lookup"><span data-stu-id="beb2c-168">Specifies the Key Type, such as: Recovery Key Password or TPM Password Hash.</span></span>

    -   <span data-ttu-id="beb2c-169">**Data de início**.</span><span class="sxs-lookup"><span data-stu-id="beb2c-169">**Start Date**.</span></span> <span data-ttu-id="beb2c-170">Especifica a parte de data de início do intervalo de datas.</span><span class="sxs-lookup"><span data-stu-id="beb2c-170">Specifies the Start Date part of the date range.</span></span>

    -   <span data-ttu-id="beb2c-171">**Data de término**.</span><span class="sxs-lookup"><span data-stu-id="beb2c-171">**End Date**.</span></span> <span data-ttu-id="beb2c-172">Especifica a parte de data de término do intervalo de datas.</span><span class="sxs-lookup"><span data-stu-id="beb2c-172">Specifies the End Date part of the date range.</span></span>

2.  <span data-ttu-id="beb2c-173">Clique em **Exibir relatório** para exibir o relatório.</span><span class="sxs-lookup"><span data-stu-id="beb2c-173">Click **View Report** to display the report.</span></span>

    <span data-ttu-id="beb2c-174">Os resultados podem ser salvos em vários formatos de arquivo disponíveis, como HTML, Microsoft Word e Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="beb2c-174">Results can be saved in several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

## <span data-ttu-id="beb2c-175">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="beb2c-175">Related topics</span></span>


[<span data-ttu-id="beb2c-176">Monitorando e Gerando Relatórios de Conformidade do BitLocker com o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="beb2c-176">Monitoring and Reporting BitLocker Compliance with MBAM 1.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





