---
title: Como mover os relatórios do MBAM 2.5
description: Como mover os relatórios do MBAM 2.5
author: dansimp
ms.assetid: c8223656-ca9d-41c8-94a3-64d07a6b99e9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1cdef260b4381671a1b9de66565ece0b70876200
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795988"
---
# <span data-ttu-id="f6805-103">Como mover os relatórios do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f6805-103">How to Move the MBAM 2.5 Reports</span></span>


<span data-ttu-id="f6805-104">Use estes procedimentos para mover o recurso relatórios de um computador para outro, ou seja, para mover o recurso relatórios do servidor a para o servidor B.</span><span class="sxs-lookup"><span data-stu-id="f6805-104">Use these procedures to move the Reports feature from one computer to another, that is, to move the Reports feature from Server A to Server B.</span></span>

<span data-ttu-id="f6805-105">As etapas de alto nível para mover o recurso relatórios são:</span><span class="sxs-lookup"><span data-stu-id="f6805-105">The high-level steps for moving the Reports feature are:</span></span>

1.  <span data-ttu-id="f6805-106">Interrompa todas as instâncias do site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="f6805-106">Stop all instances of the MBAM Administration and Monitoring Website.</span></span>

2.  <span data-ttu-id="f6805-107">Instale o software de servidor MBAM 2,5 no servidor B e configure o recurso relatórios no servidor B.</span><span class="sxs-lookup"><span data-stu-id="f6805-107">Install the MBAM 2.5 Server software on Server B and configure the Reports feature on Server B.</span></span>

3.  <span data-ttu-id="f6805-108">Atualize os dados de conexão dos relatórios nos servidores de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="f6805-108">Update the reports connection data on the MBAM Administration and Monitoring servers.</span></span>

4.  <span data-ttu-id="f6805-109">Retome a instância do site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="f6805-109">Resume the instance of the MBAM Administration and Monitoring Website.</span></span>

<span data-ttu-id="f6805-110">**Observação**  Para executar os scripts de exemplo do Windows PowerShell neste tópico, você deve atualizar a política de execução do Windows PowerShell para permitir que os scripts sejam executados.</span><span class="sxs-lookup"><span data-stu-id="f6805-110">**Note** To run the example Windows PowerShell scripts in this topic, you must update the Windows PowerShell execution policy to enable scripts to be run.</span></span> <span data-ttu-id="f6805-111">Consulte [executando scripts do Windows PowerShell](https://technet.microsoft.com/library/ee176949.aspx) para obter instruções.</span><span class="sxs-lookup"><span data-stu-id="f6805-111">See [Running Windows PowerShell Scripts](https://technet.microsoft.com/library/ee176949.aspx) for instructions.</span></span>

 

**<span data-ttu-id="f6805-112">Parar o site de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="f6805-112">Stop the MBAM Administration and Monitoring Website</span></span>**

-   <span data-ttu-id="f6805-113">No servidor que está executando o site de administração e monitoramento, use o console do Gerenciador de serviços de informações da Internet (IIS) para interromper o site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="f6805-113">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to stop the Administration and Monitoring Website.</span></span>

    <span data-ttu-id="f6805-114">Para automatizar esse procedimento, você pode usar o Windows PowerShell para inserir um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="f6805-114">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

    ``` syntax
    PS C:\> Stop-Website "Microsoft BitLocker Administration and Monitoring"
    ```

**<span data-ttu-id="f6805-115">Instale o software MBAM Server e execute o assistente de configuração do servidor do MBAM no servidor B</span><span class="sxs-lookup"><span data-stu-id="f6805-115">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>**

1.  <span data-ttu-id="f6805-116">Instale o software MBAM Server no servidor B. Para obter instruções, confira [instalar o software de servidor MBAM 2,5](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="f6805-116">Install the MBAM Server software on Server B. For instructions, see [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span>

2.  <span data-ttu-id="f6805-117">No servidor B, inicie o assistente de configuração do servidor do MBAM, clique em **Adicionar novos recursos**e selecione apenas o recurso **relatórios** .</span><span class="sxs-lookup"><span data-stu-id="f6805-117">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Reports** feature.</span></span>

    <span data-ttu-id="f6805-118">Você também pode usar o cmdlet **Enable-MbamReport** do Windows PowerShell para configurar os relatórios.</span><span class="sxs-lookup"><span data-stu-id="f6805-118">Alternatively, you can use the **Enable-MbamReport** Windows PowerShell cmdlet to configure the Reports.</span></span>

    <span data-ttu-id="f6805-119">Para obter instruções sobre como configurar os relatórios, consulte [como configurar os relatórios do MBAM 2,5](how-to-configure-the-mbam-25-reports.md).</span><span class="sxs-lookup"><span data-stu-id="f6805-119">For instructions on how to configure the Reports, see [How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md).</span></span>

**<span data-ttu-id="f6805-120">Atualizar os dados de conexão dos relatórios no servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="f6805-120">Update the reports connection data on the Administration and Monitoring Server</span></span>**

1.  <span data-ttu-id="f6805-121">No servidor que está executando o recurso relatórios, use o console do Gerenciador dos serviços de informações da Internet (IIS) para atualizar a URL dos relatórios.</span><span class="sxs-lookup"><span data-stu-id="f6805-121">On the server that is running the Reports feature, use the Internet Information Services (IIS) Manager console to update the Reports URL.</span></span>

2.  <span data-ttu-id="f6805-122">Expanda **Administração e monitoramento do Microsoft BitLocker**e selecione o nó da **assistência técnica** .</span><span class="sxs-lookup"><span data-stu-id="f6805-122">Expand **Microsoft BitLocker Administration and Monitoring**, and then select the **HelpDesk** node.</span></span>

3.  <span data-ttu-id="f6805-123">Na seção **Gerenciamento** do modo de **exibição recursos**, selecione **Editor de configuração**.</span><span class="sxs-lookup"><span data-stu-id="f6805-123">In the **Management** section of the **Features View**, select **Configuration Editor**.</span></span>

4.  <span data-ttu-id="f6805-124">No campo **seção** , selecione **appSettings**.</span><span class="sxs-lookup"><span data-stu-id="f6805-124">In the **Section** field, select **appSettings**.</span></span>

5.  <span data-ttu-id="f6805-125">Selecione a linha de **coleção** e, em seguida, clique no botão "reticências" **(...)** na extremidade direita do painel para abrir o **Editor de coleção**.</span><span class="sxs-lookup"><span data-stu-id="f6805-125">Select the **Collection** row, and then click the "ellipses" button **(…)** at the far right of the pane to open the **Collection Editor**.</span></span>

6.  <span data-ttu-id="f6805-126">No **Editor de coleção**, selecione a linha que contém **Microsoft. MBAM. Reports. URL**e atualize o valor de **Microsoft. MBAM. Reports. URL** para refletir o nome do servidor para o servidor B.</span><span class="sxs-lookup"><span data-stu-id="f6805-126">In the **Collection Editor**, select the row that contains **Microsoft.Mbam.Reports.Url**, and update the value for **Microsoft.Mbam.Reports.Url** to reflect the server name for Server B.</span></span>

    <span data-ttu-id="f6805-127">Se você configurou anteriormente o recurso relatórios em uma instância nomeada do SQL Server Reporting Services, adicione ou atualize o nome da instância para a URL, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f6805-127">If you previously configured the Reports feature on a named instance of SQL Server Reporting Services, add or update the name of the instance to the URL, for example:</span></span>

    `http://$SERVERNAME$/ReportServer_$SQLSRSINSTANCENAME$/Pages....)`

7.  <span data-ttu-id="f6805-128">Para automatizar esse procedimento, você pode usar o Windows PowerShell para executar um comando no servidor de administração e monitoramento semelhante ao exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="f6805-128">To automate this procedure, you can use Windows PowerShell to run a command on the Administration and Monitoring Server that is similar to the following code example.</span></span>

    ``` syntax
    PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\\sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value "http://$SERVERNAME$/ReportServer[_$SRSINSTANCENAME$]/Pages/ReportViewer.aspx?/Microsoft+BitLocker+Administration+and+Monitoring/"
    ```

    <span data-ttu-id="f6805-129">Usando as descrições na tabela a seguir, substitua os valores no exemplo de código por valores que correspondam ao seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="f6805-129">Using the descriptions in the following table, replace the values in the code example with values that match your environment.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="f6805-130">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="f6805-130">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="f6805-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6805-131">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f6805-132">$SERVERNAME $</span><span class="sxs-lookup"><span data-stu-id="f6805-132">$SERVERNAME$</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f6805-133">Nome do servidor para o qual os relatórios foram movidos.</span><span class="sxs-lookup"><span data-stu-id="f6805-133">Name of the server to which the Reports were moved.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="f6805-134">$SRSINSTANCENAME $</span><span class="sxs-lookup"><span data-stu-id="f6805-134">$SRSINSTANCENAME$</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f6805-135">Nome da instância do SQL Server Reporting Services para a qual os relatórios foram movidos.</span><span class="sxs-lookup"><span data-stu-id="f6805-135">Name of the instance of SQL Server Reporting Services to which the Reports were moved.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="f6805-136">Retomar a instância do site de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="f6805-136">Resume the instance of the Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="f6805-137">No servidor que está executando o site de administração e monitoramento, use o console do Gerenciador de serviços de informações da Internet (IIS) para iniciar o site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="f6805-137">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to start the Administration and Monitoring Website.</span></span>

2.  <span data-ttu-id="f6805-138">Para automatizar esse procedimento, você pode usar o Windows PowerShell para executar um comando semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="f6805-138">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

    ``` syntax
    PS C:\> Start-Website "Microsoft BitLocker Administration and Monitoring"
    ```

    <span data-ttu-id="f6805-139">**Observação**  Para executar esse comando, você deve adicionar o módulo do IIS para Windows PowerShell à instância atual do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f6805-139">**Note** To run this command, you must add the IIS module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

     



## <span data-ttu-id="f6805-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f6805-140">Related topics</span></span>


[<span data-ttu-id="f6805-141">Como configurar os relatórios do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f6805-141">How to Configure the MBAM 2.5 Reports</span></span>](how-to-configure-the-mbam-25-reports.md)

[<span data-ttu-id="f6805-142">Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f6805-142">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[<span data-ttu-id="f6805-143">Movendo os recursos do MBAM 2.5 para outro servidor</span><span class="sxs-lookup"><span data-stu-id="f6805-143">Moving MBAM 2.5 Features to Another Server</span></span>](moving-mbam-25-features-to-another-server.md)

 
## <span data-ttu-id="f6805-144">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="f6805-144">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="f6805-145">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="f6805-145">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="f6805-146">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="f6805-146">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





