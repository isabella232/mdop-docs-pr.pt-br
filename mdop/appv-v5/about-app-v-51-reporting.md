---
title: Sobre a emissão de relatórios do App-V 5.1
description: Sobre a emissão de relatórios do App-V 5.1
author: dansimp
ms.assetid: 385dca00-7178-4e35-8d86-c58867ebd65c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 827343d538238ca638b57a74ae5d2d74bc6c5968
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796628"
---
# <span data-ttu-id="8a696-103">Sobre a emissão de relatórios do App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="8a696-103">About App-V 5.1 Reporting</span></span>

<span data-ttu-id="8a696-104">O Microsoft Application Virtualization (App-V) 5,1 inclui um recurso de relatório interno que ajuda a coletar informações sobre computadores que executam o cliente App-V 5,1 e informações sobre o uso do pacote de aplicativos virtual.</span><span class="sxs-lookup"><span data-stu-id="8a696-104">Microsoft Application Virtualization (App-V) 5.1 includes a built-in reporting feature that helps you collect information about computers running the App-V 5.1 client as well as information about virtual application package usage.</span></span> <span data-ttu-id="8a696-105">Você pode usar essas informações para gerar relatórios de um banco de dados centralizado.</span><span class="sxs-lookup"><span data-stu-id="8a696-105">You can use this information to generate reports from a centralized database.</span></span>

## <a href="" id="---------app-v-5-1-reporting-overview"></a> <span data-ttu-id="8a696-106">Visão geral da emissão de relatórios do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="8a696-106">App-V 5.1 Reporting Overview</span></span>

<span data-ttu-id="8a696-107">A lista a seguir exibe o fluxo de trabalho de alto nível final a fim para relatórios no App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8a696-107">The following list displays the end–to-end high-level workflow for reporting in App-V 5.1.</span></span>

1. <span data-ttu-id="8a696-108">O servidor de relatórios do App-V 5,1 tem os seguintes pré-requisitos:</span><span class="sxs-lookup"><span data-stu-id="8a696-108">The App-V 5.1 Reporting server has the following prerequisites:</span></span>

    - <span data-ttu-id="8a696-109">Função de servidor Web do serviço de informações da Internet (IIS)</span><span class="sxs-lookup"><span data-stu-id="8a696-109">Internet Information Service (IIS) web server role</span></span>

    - <span data-ttu-id="8a696-110">Função de autenticação do Windows (em **IIS/segurança**)</span><span class="sxs-lookup"><span data-stu-id="8a696-110">Windows Authentication role (under **IIS / Security**)</span></span>

    - <span data-ttu-id="8a696-111">SQL Server instalado e em execução com o SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="8a696-111">SQL Server installed and running with SQL Server Reporting Services (SSRS)</span></span>

    <span data-ttu-id="8a696-112">Para confirmar que o SQL Server Reporting Services está em execução, exiba `http://localhost/Reports` em um navegador da Web como administrador no servidor que hospedará relatórios do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8a696-112">To confirm SQL Server Reporting Services is running, view `http://localhost/Reports` in a web browser as administrator on the server that will host App-V 5.1 Reporting.</span></span> <span data-ttu-id="8a696-113">A home page do SQL Server Reporting Services deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="8a696-113">The SQL Server Reporting Services Home page should display.</span></span>

2. <span data-ttu-id="8a696-114">Instale o servidor de relatórios do App-V 5,1 e o banco de dados associado.</span><span class="sxs-lookup"><span data-stu-id="8a696-114">Install the App-V 5.1 reporting server and associated database.</span></span> <span data-ttu-id="8a696-115">Para obter mais informações sobre como instalar o servidor de relatórios [, consulte Como instalar o servidor de relatórios em um computador autônomo e conectá-lo ao banco de dados](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database51.md).</span><span class="sxs-lookup"><span data-stu-id="8a696-115">For more information about installing the reporting server see [How to install the Reporting Server on a Standalone Computer and Connect it to the Database](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database51.md).</span></span> <span data-ttu-id="8a696-116">Configure o tempo em que o computador executando o cliente App-V 5,1 deve enviar dados para o servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="8a696-116">Configure the time when the computer running the App-V 5.1 client should send data to the reporting server.</span></span>

3. <span data-ttu-id="8a696-117">Se você não estiver usando um sistema de distribuição de software eletrônico como o Configuration Manager para exibir relatórios, você pode definir relatórios no serviço de relatórios do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8a696-117">If you are not using an electronic software distribution system such as Configuration Manager to view reports then you can define reports in SQL Server Reporting Service.</span></span> <span data-ttu-id="8a696-118">Baixe relatórios SSRS predefinidos do [centro de download](https://go.microsoft.com/fwlink/?LinkId=397255).</span><span class="sxs-lookup"><span data-stu-id="8a696-118">Download predefined SSRS Reports from the [Download Center](https://go.microsoft.com/fwlink/?LinkId=397255).</span></span>

    > [!NOTE]
    > <span data-ttu-id="8a696-119">Se você estiver usando a integração do Configuration Manager com o App-V 5,1, a maioria dos relatórios será gerada do Configuration Manager em vez do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8a696-119">If you are using the Configuration Manager integration with App-V 5.1, most reports are generated from Configuration Manager rather than from App-V 5.1.</span></span>

4. <span data-ttu-id="8a696-120">Após importar o módulo do PowerShell do App-V 5,1 usando `Import-Module AppvClient` o administrador, habilite o cliente App-v 5,1.</span><span class="sxs-lookup"><span data-stu-id="8a696-120">After importing the App-V 5.1 PowerShell module using `Import-Module AppvClient` as administrator, enable the App-V 5.1 client.</span></span> <span data-ttu-id="8a696-121">Este cmdlet do PowerShell de exemplo habilita relatórios do App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="8a696-121">This sample PowerShell cmdlet enables App-V 5.1 reporting:</span></span>

    ```powershell
    Set-AppvClientConfiguration –reportingserverurl <url>:<port> -reportingenabled 1 – ReportingStartTime <0-23> - ReportingRandomDelay <#min>
    ```

    <span data-ttu-id="8a696-122">Para enviar imediatamente dados de relatório do App-V 5,1, execute `Send-AppvClientReport` no cliente do App-v 5,1.</span><span class="sxs-lookup"><span data-stu-id="8a696-122">To immediately send App-V 5.1 report data, run `Send-AppvClientReport` on the App-V 5.1 client.</span></span>

    <span data-ttu-id="8a696-123">Para obter mais informações sobre como instalar o cliente do App-V 5,1 com relatório habilitado, consulte [sobre as configurações de cliente](about-client-configuration-settings51.md).</span><span class="sxs-lookup"><span data-stu-id="8a696-123">For more information about installing the App-V 5.1 client with reporting enabled see [About Client Configuration Settings](about-client-configuration-settings51.md).</span></span> <span data-ttu-id="8a696-124">Para administrar relatórios do App-V 5,1 com o Windows PowerShell, consulte [como habilitar relatórios no cliente do App-v 5,1 usando o PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="8a696-124">To administer App-V 5.1 Reporting with Windows PowerShell, see [How to Enable Reporting on the App-V 5.1 Client by Using PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md).</span></span>

5. <span data-ttu-id="8a696-125">Depois que o servidor de relatório recebe os dados do cliente App-V 5,1, ele envia os dados para o banco de dados de relatórios.</span><span class="sxs-lookup"><span data-stu-id="8a696-125">After the reporting server receives the data from the App-V 5.1 client it sends the data to the reporting database.</span></span> <span data-ttu-id="8a696-126">Quando o banco de dados recebe e processa os dados do cliente, uma resposta bem-sucedida é enviada ao servidor de relatórios e, em seguida, uma notificação é enviada ao cliente App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8a696-126">When the database receives and processes the client data, a successful reply is sent to the reporting server and then a notification is sent to the App-V 5.1 client.</span></span>

6. <span data-ttu-id="8a696-127">Quando o cliente do App-V 5,1 recebe a notificação de êxito, ele esvazia o cache de dados para conservar espaço.</span><span class="sxs-lookup"><span data-stu-id="8a696-127">When the App-V 5.1 client receives the success notification, it empties the data cache to conserve space.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8a696-128">Por padrão, o cache é apagado depois que o servidor confirma o recebimento de dados.</span><span class="sxs-lookup"><span data-stu-id="8a696-128">By default the cache is cleared after the server confirms receipt of data.</span></span> <span data-ttu-id="8a696-129">Você pode configurar manualmente o cliente para salvar o cache de dados.</span><span class="sxs-lookup"><span data-stu-id="8a696-129">You can manually configure the client to save the data cache.</span></span>

<span data-ttu-id="8a696-130">Se o dispositivo cliente do App-V 5,1 não receber uma notificação de êxito do servidor, ele manterá os dados no cache e tentará reenviar os dados no próximo intervalo configurado.</span><span class="sxs-lookup"><span data-stu-id="8a696-130">If the App-V 5.1 client device does not receive a success notification from the server, it retains data in the cache and tries to resend data at the next configured interval.</span></span> <span data-ttu-id="8a696-131">Os clientes continuam a coletar dados e adicioná-los ao cache.</span><span class="sxs-lookup"><span data-stu-id="8a696-131">Clients continue to collect data and add it to the cache.</span></span>

### <a href="" id="-------------app-v-5-1-reporting-server-frequently-asked-questions"></a> <span data-ttu-id="8a696-132">Perguntas frequentes sobre o aplicativo do App-V 5,1 Reporting Server</span><span class="sxs-lookup"><span data-stu-id="8a696-132">App-V 5.1 reporting server frequently asked questions</span></span>

<span data-ttu-id="8a696-133">A tabela a seguir mostra as respostas a perguntas comuns sobre relatórios do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="8a696-133">The following table displays answers to common questions about App-V 5.1 reporting</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8a696-134">Pergunta</span><span class="sxs-lookup"><span data-stu-id="8a696-134">Question</span></span></th>
<th align="left"><span data-ttu-id="8a696-135">Mais informações</span><span class="sxs-lookup"><span data-stu-id="8a696-135">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a696-136">Qual é a frequência com a qual as informações de relatório são enviadas para o banco de dados de relatórios?</span><span class="sxs-lookup"><span data-stu-id="8a696-136">What is the frequency that reporting information is sent to the reporting database?</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a696-137">A frequência depende de como a tarefa de relatório é configurada no computador que está executando o cliente App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8a696-137">The frequency depends on how the reporting task is configured on the computer running the App-V 5.1 client.</span></span> <span data-ttu-id="8a696-138">Você deve configurar a frequência/intervalo para enviar os dados de relatório.</span><span class="sxs-lookup"><span data-stu-id="8a696-138">You must configure the frequency / interval for sending the reporting data.</span></span> <span data-ttu-id="8a696-139">O relatório do App-V 5,1 não é habilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="8a696-139">App-V 5.1 Reporting is not enabled by default.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8a696-140">Quais informações são armazenadas no banco de dados do servidor de relatórios?</span><span class="sxs-lookup"><span data-stu-id="8a696-140">What information is stored in the reporting server database?</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a696-141">A lista a seguir exibe o que está armazenado no banco de dados de relatórios:</span><span class="sxs-lookup"><span data-stu-id="8a696-141">The following list displays what is stored in the reporting database:</span></span></p>
<ul>
<li><p><span data-ttu-id="8a696-142">O sistema operacional em execução no computador que está executando o cliente App-V 5,1: nome do host, versão, Service Pack, tipo-cliente/servidor, arquitetura do processador.</span><span class="sxs-lookup"><span data-stu-id="8a696-142">The operating system running on the computer running the App-V 5.1 client: host name, version, service pack, type - client/server, processor architecture.</span></span></p></li>
<li><p><span data-ttu-id="8a696-143">Informações sobre o cliente do App-V 5,1: versão.</span><span class="sxs-lookup"><span data-stu-id="8a696-143">App-V 5.1 Client information: version.</span></span></p></li>
<li><p><span data-ttu-id="8a696-144">Lista de pacotes publicados: GUID, GUID de versão, nome.</span><span class="sxs-lookup"><span data-stu-id="8a696-144">Published package list: GUID, version GUID, name.</span></span></p></li>
<li><p><span data-ttu-id="8a696-145">Informações de uso do aplicativo: nome, versão, servidor de streaming, usuário (DOMAIN\alias), GUID de versão do pacote, status e tempo de lançamento, hora de encerramento.</span><span class="sxs-lookup"><span data-stu-id="8a696-145">Application usage information: name, version, streaming server, user (domain\alias), package version GUID, launch status and time, shutdown time.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a696-146">Qual é o volume médio de informações que são enviadas para o servidor de relatórios?</span><span class="sxs-lookup"><span data-stu-id="8a696-146">What is the average volume of information that is sent to the reporting server?</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a696-147">Isso depende.</span><span class="sxs-lookup"><span data-stu-id="8a696-147">It depends.</span></span> <span data-ttu-id="8a696-148">A lista a seguir exibe os três conjuntos de dados enviados para o servidor de relatórios:</span><span class="sxs-lookup"><span data-stu-id="8a696-148">The following list displays the three sets of the data sent to the reporting server:</span></span></p>
<ol>
<li><p><span data-ttu-id="8a696-149">Informações do sistema operacional e do App-V 5,1 Client.</span><span class="sxs-lookup"><span data-stu-id="8a696-149">Operating system, and App-V 5.1 client information.</span></span> <span data-ttu-id="8a696-150">aproximadamente 150 bytes, todas as vezes que os dados forem enviados.</span><span class="sxs-lookup"><span data-stu-id="8a696-150">~150 Bytes, every time this data is sent.</span></span></p></li>
<li><p><span data-ttu-id="8a696-151">Lista de pacotes publicados.</span><span class="sxs-lookup"><span data-stu-id="8a696-151">Published package list.</span></span> <span data-ttu-id="8a696-152">aproximadamente 7 KB para 30 pacotes.</span><span class="sxs-lookup"><span data-stu-id="8a696-152">~7 KB for 30 packages.</span></span> <span data-ttu-id="8a696-153">Isso é enviado somente quando a lista de pacotes é atualizada com uma atualização de publicação, que é feita com pouca frequência; Se não houver nenhuma alteração, essas informações não serão enviadas.</span><span class="sxs-lookup"><span data-stu-id="8a696-153">This is sent only when the package list is updated with a publishing refresh, which is done infrequently; if there is no change, this information is not sent.</span></span></p></li>
<li><p><span data-ttu-id="8a696-154">Informações de uso do aplicativo virtual – cerca de 0,25 KB por evento.</span><span class="sxs-lookup"><span data-stu-id="8a696-154">Virtual application usage information – about 0.25KB per event.</span></span> <span data-ttu-id="8a696-155">A função de abertura e fechamento de contagem como um evento se ambos ocorrerem antes de enviar as informações.</span><span class="sxs-lookup"><span data-stu-id="8a696-155">Opening and closing count as one event if both occur before sending the information.</span></span> <span data-ttu-id="8a696-156">Ao enviar usando uma tarefa agendada, somente os dados desde o último upload bem-sucedido são enviados ao servidor.</span><span class="sxs-lookup"><span data-stu-id="8a696-156">When sending using a scheduled task, only the data since the last successful upload is sent to the server.</span></span> <span data-ttu-id="8a696-157">Se enviar manualmente por meio do cmdlet do PowerShell, há um argumento opcional que controla se os dados precisam ser reenviados na próxima vez – esse argumento é <strong> DeleteOnSuccess </strong> .</span><span class="sxs-lookup"><span data-stu-id="8a696-157">If sending manually through the PowerShell cmdlet, there is an optional argument that controls if the data needs to be re-sent next time around – that argument is <strong>DeleteOnSuccess</strong>.</span></span></p>
<p></p>
<p><span data-ttu-id="8a696-158">Portanto, por exemplo, se vinte aplicativos forem abertos e fechados e se as informações de relatório estiverem agendadas para serem enviadas diariamente, o tráfego diário típico deve ser sobre 0.15 KB + 20 x 0,25 KB ou sobre 5KB/usuário</span><span class="sxs-lookup"><span data-stu-id="8a696-158">So for example, if twenty applications are opened and closed and reporting information is scheduled to be sent daily, the typical daily traffic should be about 0.15KB + 20 x 0.25KB, or about 5KB/user</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8a696-159">É possível agendar a emissão de relatórios?</span><span class="sxs-lookup"><span data-stu-id="8a696-159">Can reporting be scheduled?</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a696-160">Sim.</span><span class="sxs-lookup"><span data-stu-id="8a696-160">Yes.</span></span> <span data-ttu-id="8a696-161">Além de enviar manualmente relatórios usando cmdlets do PowerShell ( <strong> Send-AppvClientReport </strong> ), a tarefa pode ser agendada para que ela aconteça automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8a696-161">Besides manually sending reporting using PowerShell Cmdlets (<strong>Send-AppvClientReport</strong>), the task can be scheduled so it will happen automatically.</span></span> <span data-ttu-id="8a696-162">Há duas maneiras de agendar o relatório:</span><span class="sxs-lookup"><span data-stu-id="8a696-162">There are two ways to schedule the reporting:</span></span></p>
<ol>
<li><p><span data-ttu-id="8a696-163">Usando cmdlets do PowerShell- <strong> set-AppvClientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="8a696-163">Using PowerShell cmdlets - <strong>Set-AppvClientConfiguration</strong>.</span></span> <span data-ttu-id="8a696-164">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="8a696-164">For example:</span></span></p>
<p><span data-ttu-id="8a696-165">Set-AppvClientConfiguration-ReportingEnabled 1-ReportingServerURL<a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</span><span class="sxs-lookup"><span data-stu-id="8a696-165">Set-AppvClientConfiguration -ReportingEnabled 1 - ReportingServerURL <a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</span></span></a></p>
<p></p>
<p><span data-ttu-id="8a696-166">Para obter uma lista completa das definições de configuração do cliente <a href="about-client-configuration-settings51.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings51.md)"> , consulte sobre as configurações de cliente </a> e procure as seguintes entradas: <strong> ReportingEnabled </strong> , <strong> ReportingServerURL </strong> , <strong> ReportingDataCacheLimit </strong> , <strong> ReportingDataBlockSize </strong> , <strong> ReportingStartTime </strong> , <strong> ReportingRandomDelay </strong> , ReportingInterval <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="8a696-166">For a complete list of client configuration settings see <a href="about-client-configuration-settings51.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings51.md)">About Client Configuration Settings</a> and look for the following entries: <strong>ReportingEnabled</strong>, <strong>ReportingServerURL</strong>, <strong>ReportingDataCacheLimit</strong>, <strong>ReportingDataBlockSize</strong>, <strong>ReportingStartTime</strong>, <strong>ReportingRandomDelay</strong>, <strong>ReportingInterval</strong>.</span></span></p>
<p></p></li>
<li><p><span data-ttu-id="8a696-167">Usando a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="8a696-167">By using Group Policy.</span></span> <span data-ttu-id="8a696-168">Se for distribuído usando o controlador de domínio, as configurações serão iguais às listadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="8a696-168">If distributed using the domain controller, the settings are the same as previously listed.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="8a696-169">Observação</span><span class="sxs-lookup"><span data-stu-id="8a696-169">Note</span></span></strong><br/><p><span data-ttu-id="8a696-170">Configurações de política de grupo substituir configurações locais definidas usando o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8a696-170">Group Policy settings override local settings configured using PowerShell.</span></span></p>
</div>
<div>
</div></li>
</ol></td>
</tr>
</tbody>
</table>

## <a href="" id="---------app-v-5-1-client-reporting"></a> <span data-ttu-id="8a696-171">Relatório de cliente do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="8a696-171">App-V 5.1 Client Reporting</span></span>

<span data-ttu-id="8a696-172">Para usar os relatórios do App-V 5,1, você deve instalar e configurar o cliente App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8a696-172">To use App-V 5.1 reporting you must install and configure the App-V 5.1 client.</span></span> <span data-ttu-id="8a696-173">Depois que o cliente tiver sido instalado, use o cmdlet **set-AppVClientConfiguration** do PowerShell ou o **modelo ADMX** para configurar o relatório.</span><span class="sxs-lookup"><span data-stu-id="8a696-173">After the client has been installed, use the **Set-AppVClientConfiguration** PowerShell cmdlet or the **ADMX Template** to configure reporting.</span></span> <span data-ttu-id="8a696-174">Os cmdlets do recurso de relatório estão disponíveis usando o link a seguir e são precedidas pela **geração de relatórios**.</span><span class="sxs-lookup"><span data-stu-id="8a696-174">The reporting feature cmdlets are available by using the following link and are prefaced by **Reporting**.</span></span> <span data-ttu-id="8a696-175">Para obter uma lista completa das configurações de cliente, consulte [sobre as definições de configuração do cliente](about-client-configuration-settings51.md).</span><span class="sxs-lookup"><span data-stu-id="8a696-175">For a complete list of client configuration settings see [About Client Configuration Settings](about-client-configuration-settings51.md).</span></span> <span data-ttu-id="8a696-176">A seção a seguir fornece exemplos da configuração de relatório do cliente do App-V 5,1 usando o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8a696-176">The following section provides examples of App-V 5.1 client reporting configuration using PowerShell.</span></span>

### <span data-ttu-id="8a696-177">Configurando relatórios do cliente App-V usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="8a696-177">Configuring App-V Client reporting using PowerShell</span></span>

<span data-ttu-id="8a696-178">Os exemplos a seguir mostram como os parâmetros do PowerShell podem configurar os recursos de relatório do cliente App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8a696-178">The following examples show how PowerShell parameters can configure the reporting features of the App-V 5.1 client.</span></span>

> [!NOTE]
> <span data-ttu-id="8a696-179">A tarefa de configuração a seguir também pode ser configurada usando configurações de política de grupo no modelo ADMX do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8a696-179">The following configuration task can also be configured using Group Policy settings in the App-V 5.1 ADMX template.</span></span> <span data-ttu-id="8a696-180">Para obter mais informações sobre como usar o modelo ADMX, consulte [como modificar a configuração do cliente do App-V 5,1 usando o modelo ADMX e a política de grupo](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md).</span><span class="sxs-lookup"><span data-stu-id="8a696-180">For more information about using the ADMX template, see [How to Modify App-V 5.1 Client Configuration Using the ADMX Template and Group Policy](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md).</span></span>

<span data-ttu-id="8a696-181">**Para habilitar o relatório e iniciar a coleta de dados no computador que está executando o cliente App-V 5,1**:</span><span class="sxs-lookup"><span data-stu-id="8a696-181">**To enable reporting and to initiate data collection on the computer running the App-V 5.1 client**:</span></span>

```powershell
Set-AppVClientConfiguration –ReportingEnabled 1
```

<span data-ttu-id="8a696-182">**Para configurar o cliente para enviar dados automaticamente para um servidor de relatórios específico**:</span><span class="sxs-lookup"><span data-stu-id="8a696-182">**To configure the client to automatically send data to a specific reporting server**:</span></span>

```powershell
Set-AppVClientConfiguration –ReportingServerURL http://MyReportingServer:MyPort/ -ReportingStartTime 20 -ReportingInterval 1 -ReportingRandomDelay 30 -ReportingInterval 1 -ReportingRandomDelay 30
```

<span data-ttu-id="8a696-183">Este exemplo configura o cliente para enviar automaticamente os dados de relatório para a URL do servidor de relatórios **http://MyReportingServer:MyPort/** .</span><span class="sxs-lookup"><span data-stu-id="8a696-183">This example configures the client to automatically send the reporting data to the reporting server URL **http://MyReportingServer:MyPort/**.</span></span> <span data-ttu-id="8a696-184">Além disso, os dados de relatório serão enviados diariamente entre o 8:00 e o 8:30 PM, dependendo do atraso aleatório gerado para a sessão.</span><span class="sxs-lookup"><span data-stu-id="8a696-184">Additionally, the reporting data will be sent daily between 8:00 and 8:30 PM, depending on the random delay generated for the session.</span></span>

<span data-ttu-id="8a696-185">**Para limitar o tamanho do cache de dados no cliente**:</span><span class="sxs-lookup"><span data-stu-id="8a696-185">**To limit the size of the data cache on the client**:</span></span>

```powershell
Set-AppvClientConfiguration –ReportingDataCacheLimit 100
```

<span data-ttu-id="8a696-186">Configura o tamanho máximo do cache de relatórios no computador que está executando o cliente do App-V 5,1 para 100 MB.</span><span class="sxs-lookup"><span data-stu-id="8a696-186">Configures the maximum size of the reporting cache on the computer running the App-V 5.1 client to 100 MB.</span></span> <span data-ttu-id="8a696-187">Se o limite do cache for atingido antes que os dados sejam enviados ao servidor, o log será regravado e os dados serão substituídos, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="8a696-187">If the cache limit is reached before the data is sent to the server, then the log rolls over and data will be overwritten as necessary.</span></span>

<span data-ttu-id="8a696-188">**Para configurar o tamanho do bloco de dados transmitido na rede entre o cliente e o servidor**:</span><span class="sxs-lookup"><span data-stu-id="8a696-188">**To configure the data block size transmitted across the network between the client and the server**:</span></span>

```powershell
Set-AppvClientConfiguration –ReportingDataBlockSize 10240
```

<span data-ttu-id="8a696-189">Especifica o máximo de blocos de dados que o cliente envia para 10240 MB.</span><span class="sxs-lookup"><span data-stu-id="8a696-189">Specifies the maximum data block that the client sends to 10240 MB.</span></span>

### <span data-ttu-id="8a696-190">Tipos de dados coletados</span><span class="sxs-lookup"><span data-stu-id="8a696-190">Types of data collected</span></span>

<span data-ttu-id="8a696-191">A tabela a seguir mostra os tipos de informações que você pode coletar usando os relatórios do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8a696-191">The following table displays the types of information you can collect by using App-V 5.1 reporting.</span></span>

|<span data-ttu-id="8a696-192">Informações do cliente</span><span class="sxs-lookup"><span data-stu-id="8a696-192">Client Information</span></span>  |<span data-ttu-id="8a696-193">Informações do pacote</span><span class="sxs-lookup"><span data-stu-id="8a696-193">Package Information</span></span>  |<span data-ttu-id="8a696-194">Uso do aplicativo</span><span class="sxs-lookup"><span data-stu-id="8a696-194">Application Usage</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="8a696-195">Nome do host</span><span class="sxs-lookup"><span data-stu-id="8a696-195">Host Name</span></span> |<span data-ttu-id="8a696-196">Nome do pacote</span><span class="sxs-lookup"><span data-stu-id="8a696-196">Package Name</span></span>|<span data-ttu-id="8a696-197">Horários de início e término</span><span class="sxs-lookup"><span data-stu-id="8a696-197">Start and End Times</span></span>|
|<span data-ttu-id="8a696-198">Versão do cliente do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="8a696-198">App-V 5.1 Client Version</span></span> |<span data-ttu-id="8a696-199">Versão do pacote</span><span class="sxs-lookup"><span data-stu-id="8a696-199">Package Version</span></span>|<span data-ttu-id="8a696-200">Status da execução</span><span class="sxs-lookup"><span data-stu-id="8a696-200">Run Status</span></span>|
|<span data-ttu-id="8a696-201">Arquitetura do processador</span><span class="sxs-lookup"><span data-stu-id="8a696-201">Processor Architecture</span></span> |<span data-ttu-id="8a696-202">Origem do pacote</span><span class="sxs-lookup"><span data-stu-id="8a696-202">Package Source</span></span>|<span data-ttu-id="8a696-203">Estado de encerramento</span><span class="sxs-lookup"><span data-stu-id="8a696-203">Shutdown State</span></span>|
|<span data-ttu-id="8a696-204">Versão do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="8a696-204">Operating System Version</span></span>|<span data-ttu-id="8a696-205">Porcentagem em cache</span><span class="sxs-lookup"><span data-stu-id="8a696-205">Percent Cached</span></span>|<span data-ttu-id="8a696-206">Nome do aplicativo</span><span class="sxs-lookup"><span data-stu-id="8a696-206">Application Name</span></span>|
|<span data-ttu-id="8a696-207">Nível do Service Pack</span><span class="sxs-lookup"><span data-stu-id="8a696-207">Service Pack Level</span></span>| |<span data-ttu-id="8a696-208">Versão do aplicativo</span><span class="sxs-lookup"><span data-stu-id="8a696-208">Application Version</span></span>|
|<span data-ttu-id="8a696-209">Tipo de sistema operacional</span><span class="sxs-lookup"><span data-stu-id="8a696-209">Operating System Type</span></span>| |<span data-ttu-id="8a696-210">Nome de Usuário</span><span class="sxs-lookup"><span data-stu-id="8a696-210">Username</span></span>|
| | |<span data-ttu-id="8a696-211">Grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="8a696-211">Connection Group</span></span>|

<span data-ttu-id="8a696-212">O cliente coleta e salva esses dados em um formato **. xml** .</span><span class="sxs-lookup"><span data-stu-id="8a696-212">The client collects and saves this data in an **.xml** format.</span></span> <span data-ttu-id="8a696-213">O cache de dados está oculto por padrão e requer direitos de administrador para abrir o arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="8a696-213">The data cache is hidden by default and requires administrator rights to open the XML file.</span></span>

### <span data-ttu-id="8a696-214">Enviar dados para o servidor</span><span class="sxs-lookup"><span data-stu-id="8a696-214">Sending data to the server</span></span>

<span data-ttu-id="8a696-215">Você pode configurar o computador que está executando o cliente App-V 5,1 para enviar dados automaticamente para o servidor de relatórios especificado.</span><span class="sxs-lookup"><span data-stu-id="8a696-215">You can configure the computer that is running the App-V 5.1 client to automatically send data to the specified reporting server.</span></span> <span data-ttu-id="8a696-216">Para especificar o servidor, use o cmdlet **set-AppvClientConfiguration** com as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="8a696-216">To specify the server use the **Set-AppvClientConfiguration** cmdlet with the following settings:</span></span>

- <span data-ttu-id="8a696-217">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="8a696-217">ReportingEnabled</span></span>
- <span data-ttu-id="8a696-218">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="8a696-218">ReportingServerURL</span></span>
- <span data-ttu-id="8a696-219">ReportingStartTime</span><span class="sxs-lookup"><span data-stu-id="8a696-219">ReportingStartTime</span></span>
- <span data-ttu-id="8a696-220">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="8a696-220">ReportingInterval</span></span>
- <span data-ttu-id="8a696-221">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="8a696-221">ReportingRandomDelay</span></span>

<span data-ttu-id="8a696-222">Depois de definir as configurações anteriores, você deve criar uma tarefa agendada.</span><span class="sxs-lookup"><span data-stu-id="8a696-222">After you configure the previous settings, you must create a scheduled task.</span></span> <span data-ttu-id="8a696-223">A tarefa agendada vai entrar em contato com o servidor especificado pela configuração **ReportingServerURL** e iniciará a transferência.</span><span class="sxs-lookup"><span data-stu-id="8a696-223">The scheduled task will contact the server specified by the **ReportingServerURL** setting and will initiate the transfer.</span></span> <span data-ttu-id="8a696-224">Se você quiser enviar dados manualmente para fora dos horários agendados, use o seguinte cmdlet do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="8a696-224">If you want to manually send data outside of the scheduled times, use the following PowerShell cmdlet:</span></span>

```powershell
Send-AppVClientReport –URL http://MyReportingServer:MyPort/ -DeleteOnSuccess
```

<span data-ttu-id="8a696-225">Se o servidor de relatório foi configurado anteriormente, o parâmetro **– URL** pode ser omitido.</span><span class="sxs-lookup"><span data-stu-id="8a696-225">If the reporting server has been previously configured, then the **–URL** parameter can be omitted.</span></span> <span data-ttu-id="8a696-226">Como alternativa, se os dados devem ser enviados para um local alternativo, especifique uma URL diferente para substituir o **ReportingServerURL** configurado para essa coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="8a696-226">Alternatively, if the data should be sent to an alternate location, specify a different URL to override the configured **ReportingServerURL** for this data collection.</span></span>

<span data-ttu-id="8a696-227">O parâmetro **-DeleteOnSuccess** indica que, se a transferência for bem-sucedida, o cache de dados será limpo.</span><span class="sxs-lookup"><span data-stu-id="8a696-227">The **-DeleteOnSuccess** parameter indicates that if the transfer is successful, then the data cache is cleared.</span></span> <span data-ttu-id="8a696-228">Se não for especificado, o cache não será limpo.</span><span class="sxs-lookup"><span data-stu-id="8a696-228">If this is not specified, then the cache will not be cleared.</span></span>

### <span data-ttu-id="8a696-229">Coleta manual de dados</span><span class="sxs-lookup"><span data-stu-id="8a696-229">Manual Data Collection</span></span>

<span data-ttu-id="8a696-230">Você também pode usar o cmdlet **Send-AppVClientReport** para coletar dados manualmente.</span><span class="sxs-lookup"><span data-stu-id="8a696-230">You can also use the **Send-AppVClientReport** cmdlet to manually collect data.</span></span> <span data-ttu-id="8a696-231">Esta solução é útil com ou sem um servidor de relatórios existente.</span><span class="sxs-lookup"><span data-stu-id="8a696-231">This solution is helpful with or without an existing reporting server.</span></span> <span data-ttu-id="8a696-232">A lista a seguir exibe informações sobre a coleta de dados com ou sem um servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="8a696-232">The following list displays information about collecting data with or without a reporting server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8a696-233">Com um servidor de relatórios</span><span class="sxs-lookup"><span data-stu-id="8a696-233">With a Reporting Server</span></span></th>
<th align="left"><span data-ttu-id="8a696-234">Sem um servidor de relatórios</span><span class="sxs-lookup"><span data-stu-id="8a696-234">Without a Reporting Server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8a696-235">Se você tiver um servidor de relatórios do App-V 5,1 existente, crie um script ou uma tarefa agendada personalizada.</span><span class="sxs-lookup"><span data-stu-id="8a696-235">If you have an existing App-V 5.1 reporting Server, create a customized scheduled task or script.</span></span> <span data-ttu-id="8a696-236">Especifique se o cliente envia os dados para o local especificado com a frequência desejada.</span><span class="sxs-lookup"><span data-stu-id="8a696-236">Specify that the client send the data to the specified location with the desired frequency.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8a696-237">Se você não tiver um servidor de relatórios do App-V 5,1 existente, use o <strong> parâmetro – URL </strong> para enviar os dados para um compartilhamento especificado.</span><span class="sxs-lookup"><span data-stu-id="8a696-237">If you do not have an existing App-V 5.1 reporting Server, use the <strong>–URL</strong> parameter to send the data to a specified share.</span></span> <span data-ttu-id="8a696-238">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="8a696-238">For example:</span></span></p>
<p><code>Send-AppVClientReport –URL \Myshare\MyData\ -DeleteOnSuccess</code></p>
<p><span data-ttu-id="8a696-239">O exemplo anterior enviará os dados de relatório para o <strong> &lt; local \MyShare\MyData/Strong &gt; indicado pelo <strong> parâmetro-URL </strong> .</span><span class="sxs-lookup"><span data-stu-id="8a696-239">The previous example will send the reporting data to <strong>\MyShare\MyData&lt;/strong&gt; location indicated by the <strong>-URL</strong> parameter.</span></span> <span data-ttu-id="8a696-240">Depois que os dados forem enviados, o cache será limpo.</span><span class="sxs-lookup"><span data-stu-id="8a696-240">After the data has been sent, the cache is cleared.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="8a696-241">Observação</span><span class="sxs-lookup"><span data-stu-id="8a696-241">Note</span></span></strong><br/><p><span data-ttu-id="8a696-242">Se um local diferente do servidor de relatórios for especificado, os dados serão enviados usando o <strong> formato. XML </strong> sem processamento adicional.</span><span class="sxs-lookup"><span data-stu-id="8a696-242">If a location other than the Reporting Server is specified, the data is sent using <strong>.xml</strong> format with no additional processing.</span></span></p>
</div>
<div>
</div></td>
</tr>
</tbody>
</table>

### <span data-ttu-id="8a696-243">Criar relatórios</span><span class="sxs-lookup"><span data-stu-id="8a696-243">Creating Reports</span></span>

<span data-ttu-id="8a696-244">Para recuperar informações de relatório e criar relatórios usando o App-V 5,1, você deve usar um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="8a696-244">To retrieve report information and create reports using App-V 5.1 you must use one of the following methods:</span></span>

- <span data-ttu-id="8a696-245">**Microsoft SQL Server Reporting Services (SSRS)** -o Microsoft SQL Server Reporting Services está disponível com o Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8a696-245">**Microsoft SQL Server Reporting Services (SSRS)** - Microsoft SQL Server Reporting Services is available with Microsoft SQL Server.</span></span> <span data-ttu-id="8a696-246">O SSRS não é instalado quando você instala o servidor de relatórios do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8a696-246">SSRS is not installed when you install the App-V 5.1 reporting server.</span></span> <span data-ttu-id="8a696-247">Ele deve ser implantado separadamente para gerar os relatórios associados.</span><span class="sxs-lookup"><span data-stu-id="8a696-247">It must be deployed separately to generate the associated reports.</span></span>

    <span data-ttu-id="8a696-248">Use o link a seguir para obter mais informações sobre como usar o [Microsoft SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596).</span><span class="sxs-lookup"><span data-stu-id="8a696-248">Use the following link for more information about using [Microsoft SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596).</span></span>

- <span data-ttu-id="8a696-249">**Script** – você pode gerar relatórios diretamente em relação ao banco de dados de relatórios do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8a696-249">**Scripting** – You can generate reports by scripting directly against the App-V 5.1 reporting database.</span></span> <span data-ttu-id="8a696-250">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="8a696-250">For example:</span></span>

    **<span data-ttu-id="8a696-251">Procedimento armazenado:</span><span class="sxs-lookup"><span data-stu-id="8a696-251">Stored Procedure:</span></span>**

    <span data-ttu-id="8a696-252">o **spProcessClientReport** está agendado para ser executado à meia-noite ou 12:00 am.</span><span class="sxs-lookup"><span data-stu-id="8a696-252">**spProcessClientReport** is scheduled to run at midnight or 12:00 AM.</span></span>

    <span data-ttu-id="8a696-253">Para executar o procedimento armazenado agendado do Microsoft SQL Server, o Microsoft SQL Server Agent deve estar em execução.</span><span class="sxs-lookup"><span data-stu-id="8a696-253">To run the Microsoft SQL Server Scheduled Stored procedure, the Microsoft SQL Server Agent must be running.</span></span> <span data-ttu-id="8a696-254">Você deve certificar-se de que o Microsoft SQL Server Agent está definido como **AutoStart**.</span><span class="sxs-lookup"><span data-stu-id="8a696-254">You should ensure that the Microsoft SQL Server Agent is set to **AutoStart**.</span></span> <span data-ttu-id="8a696-255">Para obter mais informações, consulte [AutoStart SQL Server Agent (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045).</span><span class="sxs-lookup"><span data-stu-id="8a696-255">For more information see [Autostart SQL Server Agent (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045).</span></span>

    <span data-ttu-id="8a696-256">O procedimento armazenado também é criado ao usar os scripts de banco de dados do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8a696-256">The stored procedure is also created when using the App-V 5.1 database scripts.</span></span>

<span data-ttu-id="8a696-257">Você também deve garantir que as **conexões simultâneas** do serviço Web do serviço Web do servidor de relatório sejam definidas com um valor que o servidor poderá gerenciar sem afetar a disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="8a696-257">You should also ensure that the reporting server web service's **Maximum Concurrent Connections** is set to a value that the server will be able to manage without impacting availability.</span></span> <span data-ttu-id="8a696-258">O número recomendado de **conexões simultâneas máximas** para o **serviço Web de relatório** é **10.000**.</span><span class="sxs-lookup"><span data-stu-id="8a696-258">The recommended number of **Maximum Concurrent Connections** for the **Reporting Web Service** is **10,000**.</span></span>

## <span data-ttu-id="8a696-259">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8a696-259">Related topics</span></span>

[<span data-ttu-id="8a696-260">Implantação do servidor App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="8a696-260">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)

[<span data-ttu-id="8a696-261">Como instalar o servidor de relatórios em um computador autônomo e conectá-lo ao banco de dados</span><span class="sxs-lookup"><span data-stu-id="8a696-261">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database51.md)
