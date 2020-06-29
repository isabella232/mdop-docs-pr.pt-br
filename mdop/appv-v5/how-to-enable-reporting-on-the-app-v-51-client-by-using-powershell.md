---
title: Como habilitar relatórios no cliente do App-V 5.1 usando o PowerShell
description: Como habilitar relatórios no cliente do App-V 5.1 usando o PowerShell
author: dansimp
ms.assetid: c4c58be6-cc50-44f6-bf4f-8346fc5d0c0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1d8c0d5e1930020ed1ce354f806f8917a9644e02
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796408"
---
# <span data-ttu-id="a6eb2-103">Como habilitar relatórios no cliente do App-V 5.1 usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="a6eb2-103">How to Enable Reporting on the App-V 5.1 Client by Using PowerShell</span></span>


<span data-ttu-id="a6eb2-104">Use o procedimento a seguir para configurar o App-V 5,1 para relatórios.</span><span class="sxs-lookup"><span data-stu-id="a6eb2-104">Use the following procedure to configure the App-V 5.1 for reporting.</span></span>

**<span data-ttu-id="a6eb2-105">Para configurar o computador que executa o cliente App-V 5,1 para relatórios</span><span class="sxs-lookup"><span data-stu-id="a6eb2-105">To configure the computer running the App-V 5.1 client for reporting</span></span>**

1. <span data-ttu-id="a6eb2-106">Instale o cliente App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="a6eb2-106">Install the App-V 5.1 client.</span></span> <span data-ttu-id="a6eb2-107">Para obter mais informações sobre como instalar o cliente [, consulte como implantar o cliente App-V](how-to-deploy-the-app-v-client-51gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="a6eb2-107">For more information about installing the client see [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md).</span></span>

2. <span data-ttu-id="a6eb2-108">Depois de instalar o cliente App-V 5,1, use o PowerShell **set-AppvClientConfiguration** para configurar as definições de configuração de relatórios adequadas:</span><span class="sxs-lookup"><span data-stu-id="a6eb2-108">After you have installed the App-V 5.1 client, use the **Set-AppvClientConfiguration** PowerShell to configure appropriate Reporting Configuration settings:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="a6eb2-109">Configuração</span><span class="sxs-lookup"><span data-stu-id="a6eb2-109">Setting</span></span></th>
   <th align="left"><span data-ttu-id="a6eb2-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6eb2-110">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a6eb2-111">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="a6eb2-111">ReportingEnabled</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a6eb2-112">Permite que o cliente retorne informações para um servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="a6eb2-112">Enables the client to return information to a reporting server.</span></span> <span data-ttu-id="a6eb2-113">Essa configuração é necessária para que o cliente colete os dados de relatório no cliente.</span><span class="sxs-lookup"><span data-stu-id="a6eb2-113">This setting is required for the client to collect the reporting data on the client.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a6eb2-114">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="a6eb2-114">ReportingServerURL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a6eb2-115">Especifica o local no servidor de relatório onde as informações do cliente são salvas.</span><span class="sxs-lookup"><span data-stu-id="a6eb2-115">Specifies the location on the reporting server where client information is saved.</span></span> <span data-ttu-id="a6eb2-116">Por exemplo, http:// &lt; reportingservername &gt; : &lt; reportingportnumber &gt; .</span><span class="sxs-lookup"><span data-stu-id="a6eb2-116">For example, http://&lt;reportingservername&gt;:&lt;reportingportnumber&gt;.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="a6eb2-117">Observação</span><span class="sxs-lookup"><span data-stu-id="a6eb2-117">Note</span></span></strong><br/><p><span data-ttu-id="a6eb2-118">Este é o número da porta que foi atribuído durante a configuração do servidor de relatório</span><span class="sxs-lookup"><span data-stu-id="a6eb2-118">This is the port number that was assigned during the Reporting Server setup</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a6eb2-119">Hora de início do relatório</span><span class="sxs-lookup"><span data-stu-id="a6eb2-119">Reporting Start Time</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a6eb2-120">Isso é definido para agendar o cliente para enviar os dados automaticamente para o servidor.</span><span class="sxs-lookup"><span data-stu-id="a6eb2-120">This is set to schedule the client to automatically send the data to the server.</span></span> <span data-ttu-id="a6eb2-121">Essa configuração indicará a hora em que os dados de relatório começarão a enviar.</span><span class="sxs-lookup"><span data-stu-id="a6eb2-121">This setting will indicate the hour at which the reporting data will start to send.</span></span> <span data-ttu-id="a6eb2-122">Ele está no formato de 24 horas e aceitará um número entre o 0-23.</span><span class="sxs-lookup"><span data-stu-id="a6eb2-122">It is in the 24 hour format and will take a number between 0-23.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a6eb2-123">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="a6eb2-123">ReportingRandomDelay</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a6eb2-124">Especifica o atraso máximo (em minutos) dos dados a serem enviados para o servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="a6eb2-124">Specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="a6eb2-125">Quando a tarefa agendada for iniciada, o cliente gerará um atraso aleatório entre 0 e ReportingRandomDelay e esperará a duração especificada antes de enviar os dados.</span><span class="sxs-lookup"><span data-stu-id="a6eb2-125">When the scheduled task is started, the client generates a random delay between 0 and ReportingRandomDelay and will wait the specified duration before sending data.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a6eb2-126">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="a6eb2-126">ReportingInterval</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a6eb2-127">Especifica o intervalo de repetição que o cliente usará para reenviar dados ao servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="a6eb2-127">Specifies the retry interval that the client will use to resend data to the reporting server.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="a6eb2-128">ReportingDataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="a6eb2-128">ReportingDataCacheLimit</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a6eb2-129">Especifica o tamanho máximo em megabytes (MB) do cache XML para armazenar informações de relatório.</span><span class="sxs-lookup"><span data-stu-id="a6eb2-129">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="a6eb2-130">O tamanho se aplica ao cache na memória.</span><span class="sxs-lookup"><span data-stu-id="a6eb2-130">The size applies to the cache in memory.</span></span> <span data-ttu-id="a6eb2-131">Quando o limite for atingido, o arquivo de log será revertido.</span><span class="sxs-lookup"><span data-stu-id="a6eb2-131">When the limit is reached, the log file will roll over.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="a6eb2-132">ReportingDataBlockSize</span><span class="sxs-lookup"><span data-stu-id="a6eb2-132">ReportingDataBlockSize</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a6eb2-133">Especifica o tamanho máximo em megabytes (MB) do cache XML para armazenar informações de relatório.</span><span class="sxs-lookup"><span data-stu-id="a6eb2-133">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="a6eb2-134">O tamanho se aplica ao cache na memória.</span><span class="sxs-lookup"><span data-stu-id="a6eb2-134">The size applies to the cache in memory.</span></span> <span data-ttu-id="a6eb2-135">Quando o limite for atingido, o arquivo de log será revertido.</span><span class="sxs-lookup"><span data-stu-id="a6eb2-135">When the limit is reached, the log file will roll over.</span></span></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="a6eb2-136">Após a configuração das configurações apropriadas, o computador que executa o cliente App-V 5,1 coletará dados automaticamente e enviará os dados de volta para o servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="a6eb2-136">After the appropriate settings have been configured, the computer running the App-V 5.1 client will automatically collect data and will send the data back to the reporting server.</span></span>

   <span data-ttu-id="a6eb2-137">Além disso, os administradores podem enviar manualmente os dados de volta de uma maneira sob demanda usando o cmdlet do PowerShell **Send-AppvClientReport** .</span><span class="sxs-lookup"><span data-stu-id="a6eb2-137">Additionally, administrators can manually send the data back in an on-demand manner using the **Send-AppvClientReport** PowerShell cmdlet.</span></span>

   <span data-ttu-id="a6eb2-138">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="a6eb2-138">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="a6eb2-139">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="a6eb2-139">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="a6eb2-140">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="a6eb2-140">Got an App-V issue?</span></span>** <span data-ttu-id="a6eb2-141">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="a6eb2-141">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="a6eb2-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a6eb2-142">Related topics</span></span>


[<span data-ttu-id="a6eb2-143">Administração do App-V 5.1 usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="a6eb2-143">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)









