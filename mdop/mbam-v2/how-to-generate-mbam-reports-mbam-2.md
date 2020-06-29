---
title: Como gerar relatórios do MBAM
description: Como gerar relatórios do MBAM
author: dansimp
ms.assetid: 083550cb-8c3f-49b3-a30e-97d85374d2f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ccdc1a2cd69d8cc2e2c2823827f5ea43ad867a78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799403"
---
# <span data-ttu-id="ee66c-103">Como gerar relatórios do MBAM</span><span class="sxs-lookup"><span data-stu-id="ee66c-103">How to Generate MBAM Reports</span></span>


<span data-ttu-id="ee66c-104">Ao instalar o Microsoft BitLocker Administration and Monitoring (MBAM) with the autônomo Topology, você pode gerar relatórios diferentes para monitorar o uso e a conformidade de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ee66c-104">When you install Microsoft BitLocker Administration and Monitoring (MBAM) with the Stand-alone topology, you can generate different reports to monitor BitLocker encryption usage and compliance.</span></span> <span data-ttu-id="ee66c-105">Os procedimentos neste tópico descrevem como abrir o site de administração e monitoramento e as etapas necessárias para gerar relatórios de administração e monitoramento do Microsoft BitLocker em conformidade com a empresa, computadores individuais e atividades de recuperação de chave.</span><span class="sxs-lookup"><span data-stu-id="ee66c-105">The procedures in this topic describe how to open the Administration and Monitoring website and the steps that are needed to generate Microsoft BitLocker Administration and Monitoring reports on enterprise compliance, individual computers, and key recovery activity.</span></span> <span data-ttu-id="ee66c-106">Para obter informações detalhadas sobre como entender os relatórios do MBAM, consulte [noções básicas sobre relatórios do MBAM](understanding-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="ee66c-106">For detailed information to help understand MBAM reports, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span></span>

<span data-ttu-id="ee66c-107">**Observação**  Para executar os relatórios, você deve ser membro da função de **usuários de relatório** nos computadores em que os recursos de servidor de administração e monitoramento, o banco de dados de conformidade e auditoria e os relatórios de conformidade e auditoria estão instalados.</span><span class="sxs-lookup"><span data-stu-id="ee66c-107">**Note** To run the reports, you must be a member of the **Report Users Role** on the computers where the Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports are installed.</span></span>

 

**<span data-ttu-id="ee66c-108">Para abrir o site de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="ee66c-108">To open the Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="ee66c-109">Abra um navegador da Web e navegue até o site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="ee66c-109">Open a web browser and navigate to the Administration and Monitoring website.</span></span> <span data-ttu-id="ee66c-110">A URL padrão para o site de administração e monitoramento é \*http:// &lt; ComputerName &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="ee66c-110">The default URL for the Administration and Monitoring website is *http://&lt;computername&gt;*.</span></span>

    <span data-ttu-id="ee66c-111">**Observação**  Se o site de administração e monitoramento tiver sido instalado em uma porta diferente da 80, você precisará especificar a porta na URL (por exemplo, \*http:// &lt; ComputerName &gt; : &lt; Port &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="ee66c-111">**Note** If theAdministration and Monitoring website was installed on a port other than 80, you have to specify the port in the URL (for example, *http://&lt;computername&gt;:&lt;port&gt;*.</span></span> <span data-ttu-id="ee66c-112">Se você tiver especificado um nome de host para o site de administração e monitoramento durante a instalação, a URL será \*http:// &lt; hostname &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="ee66c-112">If you specified a host name for theAdministration and Monitoring website during the installation, the URL is *http://&lt;hostname&gt;*.</span></span>

     

2.  <span data-ttu-id="ee66c-113">No painel esquerdo, clique em **relatórios** e selecione o relatório que você deseja executar a partir da barra de menus superior.</span><span class="sxs-lookup"><span data-stu-id="ee66c-113">In the left pane, click **Reports** and then select the report you want to run from the top menu bar.</span></span>

    <span data-ttu-id="ee66c-114">Os dados do cliente MBAM históricos são mantidos no banco de dados de conformidade para referência histórica, caso um computador seja perdido ou roubado.</span><span class="sxs-lookup"><span data-stu-id="ee66c-114">Historical MBAM client data is retained in the compliance database for historical reference in case a computer is lost or stolen.</span></span> <span data-ttu-id="ee66c-115">Ao executar relatórios corporativos, recomendamos que você use as datas de início e de término adequadas para fazer o escopo dos quadros de tempo dos relatórios de uma a duas semanas para aumentar a precisão dos dados de relatório.</span><span class="sxs-lookup"><span data-stu-id="ee66c-115">When running enterprise reports, we recommend that you use appropriate start and end dates to scope the time frames for the reports from one to two weeks to increase reporting data accuracy.</span></span>

    <span data-ttu-id="ee66c-116">**Observação**  Se o SSRS não tiver sido configurado para usar o Secure Socket Layer, a URL dos relatórios será definida como HTTP em vez de HTTPS quando você instalar o servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="ee66c-116">**Note** If SSRS was not configured to use Secure Socket Layer, the URL for the reports will be set to HTTP instead of to HTTPS when you install the MBAM Server.</span></span> <span data-ttu-id="ee66c-117">Se, em seguida, você acessar o portal de suporte técnico e selecionar um relatório, a seguinte mensagem será exibida: "somente conteúdo seguro é exibido".</span><span class="sxs-lookup"><span data-stu-id="ee66c-117">If you then go to the Help Desk portal and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span> <span data-ttu-id="ee66c-118">Para mostrar o relatório, clique em **mostrar todo o conteúdo**.</span><span class="sxs-lookup"><span data-stu-id="ee66c-118">To show the report, click **Show All Content**.</span></span>

     

**<span data-ttu-id="ee66c-119">Para gerar um relatório de conformidade empresarial</span><span class="sxs-lookup"><span data-stu-id="ee66c-119">To generate an Enterprise Compliance Report</span></span>**

1.  <span data-ttu-id="ee66c-120">No site Administração e monitoramento, selecione o nó **relatórios** no painel de navegação à esquerda, selecione **relatório de conformidade empresarial**e selecione os filtros que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="ee66c-120">From the Administration and Monitoring website, select the **Reports** node from the left navigation pane, select **Enterprise Compliance Report**, and select the filters that you want to use.</span></span> <span data-ttu-id="ee66c-121">Os filtros disponíveis para o relatório de conformidade empresarial são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="ee66c-121">The available filters for the Enterprise Compliance Report are the following:</span></span>

    -   <span data-ttu-id="ee66c-122">**Status de conformidade**.</span><span class="sxs-lookup"><span data-stu-id="ee66c-122">**Compliance Status**.</span></span> <span data-ttu-id="ee66c-123">Use esse filtro para especificar os tipos de status de conformidade (por exemplo, em conformidade ou não conforme) do relatório.</span><span class="sxs-lookup"><span data-stu-id="ee66c-123">Use this filter to specify the compliance status types (for example, Compliant, or Noncompliant) of the report.</span></span>

    -   <span data-ttu-id="ee66c-124">**Estado do erro**.</span><span class="sxs-lookup"><span data-stu-id="ee66c-124">**Error State**.</span></span> <span data-ttu-id="ee66c-125">Use esse filtro para especificar os tipos de estado de erro (por exemplo, nenhum erro ou erro) do relatório.</span><span class="sxs-lookup"><span data-stu-id="ee66c-125">Use this filter to specify the error state types (for example, No Error, or Error) of the report.</span></span>

2.  <span data-ttu-id="ee66c-126">Clique em **Exibir relatório** para exibir o relatório selecionado.</span><span class="sxs-lookup"><span data-stu-id="ee66c-126">Click **View Report** to display the selected report.</span></span>

    <span data-ttu-id="ee66c-127">Os resultados podem ser salvos em formatos diferentes, como HTML, Microsoft Word e Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="ee66c-127">Results can be saved in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

    <span data-ttu-id="ee66c-128">**Observação**  O relatório de conformidade empresarial é gerado por um trabalho do SQL que é executado a cada seis horas.</span><span class="sxs-lookup"><span data-stu-id="ee66c-128">**Note** The Enterprise Compliance report is generated by a SQL job that runs every six hours.</span></span> <span data-ttu-id="ee66c-129">Portanto, na primeira vez que você exibir o relatório, você pode descobrir que alguns dados estão ausentes.</span><span class="sxs-lookup"><span data-stu-id="ee66c-129">Therefore, the first time you view the report, you may find that some data is missing.</span></span> <span data-ttu-id="ee66c-130">Você pode gerar dados de relatório atualizados manualmente usando o SQL Management Studio.</span><span class="sxs-lookup"><span data-stu-id="ee66c-130">You can generate updated report data manually by using SQL Management Studio.</span></span> <span data-ttu-id="ee66c-131">Na janela **Gerenciador de objetos** , expanda **agente do SQL Server**, expanda **trabalhos**, clique com o botão direito do mouse no trabalho **CreateCache** e selecione **Iniciar trabalho na etapa..** ..</span><span class="sxs-lookup"><span data-stu-id="ee66c-131">From the **Object Explorer** window, expand **SQL Server Agent**, expand **Jobs**, right-click the **CreateCache** job, and select **Start Job at Step….**</span></span>

     

3.  <span data-ttu-id="ee66c-132">Selecione um nome de computador para exibir informações sobre o computador no relatório de conformidade do computador.</span><span class="sxs-lookup"><span data-stu-id="ee66c-132">Select a computer name to view information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="ee66c-133">Selecione o sinal de adição (+) ao lado do nome do computador para exibir informações sobre os volumes do computador.</span><span class="sxs-lookup"><span data-stu-id="ee66c-133">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

**<span data-ttu-id="ee66c-134">Para gerar o relatório de conformidade do computador</span><span class="sxs-lookup"><span data-stu-id="ee66c-134">To generate the Computer Compliance Report</span></span>**

1.  <span data-ttu-id="ee66c-135">No site Administração e monitoramento, selecione o nó do **relatório** no painel de navegação à esquerda e selecione o **relatório de conformidade do computador**.</span><span class="sxs-lookup"><span data-stu-id="ee66c-135">In the Administration and Monitoring website, select the **Report** node from the left navigation pane, and then select the **Computer Compliance Report**.</span></span> <span data-ttu-id="ee66c-136">Use o relatório de conformidade do computador para pesquisar o **nome de usuário** ou o **nome do computador**.</span><span class="sxs-lookup"><span data-stu-id="ee66c-136">Use the Computer Compliance report to search for **user name** or **computer name**.</span></span>

2.  <span data-ttu-id="ee66c-137">Clique em **Exibir relatório** para ver o relatório do computador.</span><span class="sxs-lookup"><span data-stu-id="ee66c-137">Click **View Report** to view the computer report.</span></span>

    <span data-ttu-id="ee66c-138">Os resultados podem ser salvos em formatos diferentes, como HTML, Microsoft Word e Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="ee66c-138">Results can be saved in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

3.  <span data-ttu-id="ee66c-139">Selecione um nome de computador para exibir mais informações sobre o computador no relatório de conformidade do computador.</span><span class="sxs-lookup"><span data-stu-id="ee66c-139">Select a computer name to display more information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="ee66c-140">Selecione o sinal de adição (+) ao lado do nome do computador para exibir informações sobre os volumes do computador.</span><span class="sxs-lookup"><span data-stu-id="ee66c-140">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

    <span data-ttu-id="ee66c-141">**Observação**  Um computador cliente MBAM é considerado compatível se o computador atender aos requisitos das configurações da política do MBAM.</span><span class="sxs-lookup"><span data-stu-id="ee66c-141">**Note** An MBAM client computer is considered compliant if the computer matches the requirements of the MBAM policy settings.</span></span>

     

**<span data-ttu-id="ee66c-142">Para gerar o relatório de auditoria de chave de recuperação</span><span class="sxs-lookup"><span data-stu-id="ee66c-142">To generate the Recovery Key Audit Report</span></span>**

1.  <span data-ttu-id="ee66c-143">No site Administração e monitoramento, selecione o nó do **relatório** no painel de navegação à esquerda e, em seguida, selecione o **relatório de auditoria de recuperação**.</span><span class="sxs-lookup"><span data-stu-id="ee66c-143">From the Administration and Monitoring website, select the **Report** node in the left navigation pane, and then select the **Recovery Audit Report**.</span></span> <span data-ttu-id="ee66c-144">Selecione os filtros para o relatório de auditoria de chave de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ee66c-144">Select the filters for your Recovery Key Audit report.</span></span> <span data-ttu-id="ee66c-145">Os filtros disponíveis para auditoria de chave de recuperação são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="ee66c-145">The available filters for Recovery Key audits are as follows:</span></span>

    -   <span data-ttu-id="ee66c-146">**Solicitante**.</span><span class="sxs-lookup"><span data-stu-id="ee66c-146">**Requestor**.</span></span> <span data-ttu-id="ee66c-147">Esse filtro permite que os usuários especifiquem o nome de usuário do solicitante.</span><span class="sxs-lookup"><span data-stu-id="ee66c-147">This filter enables users to specify the user name of the requester.</span></span> <span data-ttu-id="ee66c-148">O solicitante é a pessoa da assistência técnica que acessou a chave em nome de um usuário.</span><span class="sxs-lookup"><span data-stu-id="ee66c-148">The requester is the person in the Help Desk who accessed the key on behalf of a user.</span></span>

    -   <span data-ttu-id="ee66c-149">**Solicitante**.</span><span class="sxs-lookup"><span data-stu-id="ee66c-149">**Requestee**.</span></span> <span data-ttu-id="ee66c-150">Esse filtro permite que os usuários especifiquem o nome de usuário do solicitante.</span><span class="sxs-lookup"><span data-stu-id="ee66c-150">This filter enables users to specify the user name of the requestee.</span></span> <span data-ttu-id="ee66c-151">O solicitante é a pessoa que chamou o suporte técnico para obter uma chave de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ee66c-151">The requestee is the person who called the Help Desk to obtain a recovery key.</span></span>

    -   <span data-ttu-id="ee66c-152">**Resultado da solicitação**.</span><span class="sxs-lookup"><span data-stu-id="ee66c-152">**Request Result**.</span></span> <span data-ttu-id="ee66c-153">Esse filtro permite que os usuários especifiquem os tipos de resultados de solicitação (por exemplo, sucesso ou falha) em que desejam basear o relatório.</span><span class="sxs-lookup"><span data-stu-id="ee66c-153">This filter enables users to specify the request result types (for example, Success or Failed) that they want to base the report on.</span></span> <span data-ttu-id="ee66c-154">Por exemplo, os usuários podem querer ver as tentativas de acesso à chave que falharam.</span><span class="sxs-lookup"><span data-stu-id="ee66c-154">For example, users may want to view failed key access attempts.</span></span>

    -   <span data-ttu-id="ee66c-155">**Tipo de chave**.</span><span class="sxs-lookup"><span data-stu-id="ee66c-155">**Key Type**.</span></span> <span data-ttu-id="ee66c-156">Esse filtro permite que os usuários especifiquem o tipo de chave (por exemplo: senha da chave de recuperação ou hash de senha do TPM) em que desejam basear o relatório.</span><span class="sxs-lookup"><span data-stu-id="ee66c-156">This filter enables users to specify the Key Type (for example: Recovery Key Password or TPM Password Hash) that they want to base the report on.</span></span>

    -   <span data-ttu-id="ee66c-157">**Data de início**.</span><span class="sxs-lookup"><span data-stu-id="ee66c-157">**Start Date**.</span></span> <span data-ttu-id="ee66c-158">Esse filtro é usado para definir a parte de data de início do intervalo de datas que o usuário quer relatar.</span><span class="sxs-lookup"><span data-stu-id="ee66c-158">This filter is used to define the Start Date part of the date range that the user wants to report on.</span></span>

    -   <span data-ttu-id="ee66c-159">**Data de término**.</span><span class="sxs-lookup"><span data-stu-id="ee66c-159">**End Date**.</span></span> <span data-ttu-id="ee66c-160">Esse filtro é usado para definir a parte de data de término do intervalo de datas que os usuários desejam relatar.</span><span class="sxs-lookup"><span data-stu-id="ee66c-160">This filter is used to define the End Date part of the date range that the users want to report on.</span></span>

2.  <span data-ttu-id="ee66c-161">Clique em **Exibir relatório** para exibir o relatório.</span><span class="sxs-lookup"><span data-stu-id="ee66c-161">Click **View Report** to view the report.</span></span>

    <span data-ttu-id="ee66c-162">Os resultados podem ser salvos em formatos diferentes, como HTML, Microsoft Word e Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="ee66c-162">Results can be saved in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

## <span data-ttu-id="ee66c-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ee66c-163">Related topics</span></span>


[<span data-ttu-id="ee66c-164">Monitorando e Gerando Relatórios de Conformidade do BitLocker com o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ee66c-164">Monitoring and Reporting BitLocker Compliance with MBAM 2.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





