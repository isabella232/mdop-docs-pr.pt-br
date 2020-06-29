---
title: Como habilitar relatórios no cliente do App-V 5.0 usando o PowerShell
description: Como habilitar relatórios no cliente do App-V 5.0 usando o PowerShell
author: dansimp
ms.assetid: a7aaf553-0f83-4cd0-8df8-93a5f1ebe497
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c004b4900a9814a11cb2706659a2edb99de6cc1b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796412"
---
# <span data-ttu-id="14892-103">Como habilitar relatórios no cliente do App-V 5.0 usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="14892-103">How to Enable Reporting on the App-V 5.0 Client by Using PowerShell</span></span>


<span data-ttu-id="14892-104">Use o procedimento a seguir para configurar o App-V 5,0 para relatórios.</span><span class="sxs-lookup"><span data-stu-id="14892-104">Use the following procedure to configure the App-V 5.0 for reporting.</span></span>

**<span data-ttu-id="14892-105">Para configurar o computador que executa o cliente App-V 5,0 para relatórios</span><span class="sxs-lookup"><span data-stu-id="14892-105">To configure the computer running the App-V 5.0 client for reporting</span></span>**

1. <span data-ttu-id="14892-106">Instale o cliente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="14892-106">Install the App-V 5.0 client.</span></span> <span data-ttu-id="14892-107">Para obter mais informações sobre como instalar o cliente [, consulte como implantar o cliente App-V](how-to-deploy-the-app-v-client-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="14892-107">For more information about installing the client see [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md).</span></span>

2. <span data-ttu-id="14892-108">Depois de instalar o cliente App-V 5,0, use o PowerShell **set-AppvClientConfiguration** para configurar as definições de configuração de relatórios adequadas:</span><span class="sxs-lookup"><span data-stu-id="14892-108">After you have installed the App-V 5.0 client, use the **Set-AppvClientConfiguration** PowerShell to configure appropriate Reporting Configuration settings:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="14892-109">Configuração</span><span class="sxs-lookup"><span data-stu-id="14892-109">Setting</span></span></th>
   <th align="left"><span data-ttu-id="14892-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="14892-110">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="14892-111">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="14892-111">ReportingEnabled</span></span></p></td>
   <td align="left"><p><span data-ttu-id="14892-112">Permite que o cliente retorne informações para um servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="14892-112">Enables the client to return information to a reporting server.</span></span> <span data-ttu-id="14892-113">Essa configuração é necessária para que o cliente colete os dados de relatório no cliente.</span><span class="sxs-lookup"><span data-stu-id="14892-113">This setting is required for the client to collect the reporting data on the client.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="14892-114">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="14892-114">ReportingServerURL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="14892-115">Especifica o local no servidor de relatório onde as informações do cliente são salvas.</span><span class="sxs-lookup"><span data-stu-id="14892-115">Specifies the location on the reporting server where client information is saved.</span></span> <span data-ttu-id="14892-116">Por exemplo, http:// &lt; reportingservername &gt; : &lt; reportingportnumber &gt; .</span><span class="sxs-lookup"><span data-stu-id="14892-116">For example, http://&lt;reportingservername&gt;:&lt;reportingportnumber&gt;.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="14892-117">Observação</span><span class="sxs-lookup"><span data-stu-id="14892-117">Note</span></span></strong><br/><p><span data-ttu-id="14892-118">Este é o número da porta que foi atribuído durante a configuração do servidor de relatório</span><span class="sxs-lookup"><span data-stu-id="14892-118">This is the port number that was assigned during the Reporting Server setup</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="14892-119">Hora de início do relatório</span><span class="sxs-lookup"><span data-stu-id="14892-119">Reporting Start Time</span></span></p></td>
   <td align="left"><p><span data-ttu-id="14892-120">Isso é definido para agendar o cliente para enviar os dados automaticamente para o servidor.</span><span class="sxs-lookup"><span data-stu-id="14892-120">This is set to schedule the client to automatically send the data to the server.</span></span> <span data-ttu-id="14892-121">Essa configuração indicará a hora em que os dados de relatório começarão a enviar.</span><span class="sxs-lookup"><span data-stu-id="14892-121">This setting will indicate the hour at which the reporting data will start to send.</span></span> <span data-ttu-id="14892-122">Ele está no formato de 24 horas e aceitará um número entre o 0-23.</span><span class="sxs-lookup"><span data-stu-id="14892-122">It is in the 24 hour format and will take a number between 0-23.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="14892-123">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="14892-123">ReportingRandomDelay</span></span></p></td>
   <td align="left"><p><span data-ttu-id="14892-124">Especifica o atraso máximo (em minutos) dos dados a serem enviados para o servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="14892-124">Specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="14892-125">Quando a tarefa agendada for iniciada, o cliente gerará um atraso aleatório entre 0 e ReportingRandomDelay e esperará a duração especificada antes de enviar os dados.</span><span class="sxs-lookup"><span data-stu-id="14892-125">When the scheduled task is started, the client generates a random delay between 0 and ReportingRandomDelay and will wait the specified duration before sending data.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="14892-126">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="14892-126">ReportingInterval</span></span></p></td>
   <td align="left"><p><span data-ttu-id="14892-127">Especifica o intervalo de repetição que o cliente usará para reenviar dados ao servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="14892-127">Specifies the retry interval that the client will use to resend data to the reporting server.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="14892-128">ReportingDataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="14892-128">ReportingDataCacheLimit</span></span></p></td>
   <td align="left"><p><span data-ttu-id="14892-129">Especifica o tamanho máximo em megabytes (MB) do cache XML para armazenar informações de relatório.</span><span class="sxs-lookup"><span data-stu-id="14892-129">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="14892-130">O tamanho se aplica ao cache na memória.</span><span class="sxs-lookup"><span data-stu-id="14892-130">The size applies to the cache in memory.</span></span> <span data-ttu-id="14892-131">Quando o limite for atingido, o arquivo de log será revertido.</span><span class="sxs-lookup"><span data-stu-id="14892-131">When the limit is reached, the log file will roll over.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="14892-132">ReportingDataBlockSize</span><span class="sxs-lookup"><span data-stu-id="14892-132">ReportingDataBlockSize</span></span></p></td>
   <td align="left"><p><span data-ttu-id="14892-133">Especifica o tamanho máximo em megabytes (MB) do cache XML para armazenar informações de relatório.</span><span class="sxs-lookup"><span data-stu-id="14892-133">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="14892-134">O tamanho se aplica ao cache na memória.</span><span class="sxs-lookup"><span data-stu-id="14892-134">The size applies to the cache in memory.</span></span> <span data-ttu-id="14892-135">Quando o limite for atingido, o arquivo de log será revertido.</span><span class="sxs-lookup"><span data-stu-id="14892-135">When the limit is reached, the log file will roll over.</span></span></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="14892-136">Após a configuração das configurações apropriadas, o computador que executa o cliente App-V 5,0 coletará dados automaticamente e enviará os dados de volta para o servidor de relatórios.</span><span class="sxs-lookup"><span data-stu-id="14892-136">After the appropriate settings have been configured, the computer running the App-V 5.0 client will automatically collect data and will send the data back to the reporting server.</span></span>

   <span data-ttu-id="14892-137">Além disso, os administradores podem enviar manualmente os dados de volta de uma maneira sob demanda usando o cmdlet do PowerShell **Send-AppvClientReport** .</span><span class="sxs-lookup"><span data-stu-id="14892-137">Additionally, administrators can manually send the data back in an on-demand manner using the **Send-AppvClientReport** PowerShell cmdlet.</span></span>

   <span data-ttu-id="14892-138">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="14892-138">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="14892-139">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="14892-139">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="14892-140">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="14892-140">Got an App-V issue?</span></span>** <span data-ttu-id="14892-141">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="14892-141">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="14892-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="14892-142">Related topics</span></span>


[<span data-ttu-id="14892-143">Administração do App-V usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="14892-143">Administering App-V by Using PowerShell</span></span>](administering-app-v-by-using-powershell.md)









