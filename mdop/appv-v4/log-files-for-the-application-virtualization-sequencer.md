---
title: Arquivos de log do Application Virtualization Sequencer
description: Arquivos de log do Application Virtualization Sequencer
author: dansimp
ms.assetid: 1a296544-eab4-46f9-82ce-3136f8b578af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8cdf9dbc78ccdd03df5903ef4d42990099a2c53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796881"
---
# <span data-ttu-id="7d136-103">Arquivos de log do Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="7d136-103">Log Files for the Application Virtualization Sequencer</span></span>


<span data-ttu-id="7d136-104">Os arquivos de log do sequenciador do Application Virtualization (App-V) fornecem informações detalhadas sobre o sequenciamento de aplicativos, e eles podem ser úteis quando você está verificando a funcionalidade ou durante a solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="7d136-104">The log files for the Application Virtualization (App-V) Sequencer provide detailed information about sequencing applications, and they can be helpful when you are verifying functionality or when you are troubleshooting issues.</span></span>

<span data-ttu-id="7d136-105">A tabela a seguir fornece informações sobre os arquivos de log e seus locais padrão, que são criados ao usar o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="7d136-105">The following table provides information about the log files and their default locations, which are created when using the Sequencer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7d136-106">Nome do arquivo de log</span><span class="sxs-lookup"><span data-stu-id="7d136-106">Log File Name</span></span></th>
<th align="left"><span data-ttu-id="7d136-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d136-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="7d136-108">sft-seq-log.txt</span><span class="sxs-lookup"><span data-stu-id="7d136-108">sft-seq-log.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7d136-109">Fornece informações gerais sobre a sequenciagem de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7d136-109">Provides general information about sequencing an application.</span></span> <span data-ttu-id="7d136-110">Use este log como ponto de partida para solucionar erros de sequenciador.</span><span class="sxs-lookup"><span data-stu-id="7d136-110">Use this log as a starting point for troubleshooting Sequencer errors.</span></span></p>
<p><span data-ttu-id="7d136-111">Local do arquivo de log: <em> %windir%\Microsoft Application Virtualization Sequencer\Logs</span><span class="sxs-lookup"><span data-stu-id="7d136-111">Log file location: <em>%windir%\Microsoft Application Virtualization Sequencer\Logs</span></span></em></p>
<p><span data-ttu-id="7d136-112">[Valor do token do modelo] Local do arquivo de log do App-V 4.6: <em> %windir%\Program Comuns\microsoft Application Virtualization Sequencer\Logs </em> [valor de token do modelo]</span><span class="sxs-lookup"><span data-stu-id="7d136-112">[Template Token Value] App-V4.6 log file location: <em>%windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs</em>[Template Token Value]</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="7d136-113">sftbt.txt</span><span class="sxs-lookup"><span data-stu-id="7d136-113">sftbt.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7d136-114">Fornece informações sobre as tarefas de reinicialização do computador que ocorrem durante a reinicialização simulada do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="7d136-114">Provides information about computer restart tasks that occur during the Sequencer’s simulated restart.</span></span></p>
<p><span data-ttu-id="7d136-115">Local do arquivo de log: <em> %windir%\Microsoft Application Virtualization Sequencer\Logs</span><span class="sxs-lookup"><span data-stu-id="7d136-115">Log file location: <em>%windir%\Microsoft Application Virtualization Sequencer\Logs</span></span></em></p>
<p><span data-ttu-id="7d136-116">[Valor do token do modelo] Local do arquivo de log do App-V 4.6: <em> %windir%\Program Comuns\microsoft Application Virtualization Sequencer\Logs </em> [valor de token do modelo]</span><span class="sxs-lookup"><span data-stu-id="7d136-116">[Template Token Value] App-V4.6 log file location: <em>%windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs</em>[Template Token Value]</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="7d136-117">SftCallBack.txt</span><span class="sxs-lookup"><span data-stu-id="7d136-117">SftCallBack.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7d136-118">Fornece informações gerais sobre os processos usados durante o sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="7d136-118">Provides general information about processes used during sequencing.</span></span></p>
<p><span data-ttu-id="7d136-119">Local do arquivo de log: <em> %windir%\Microsoft Application Virtualization Sequencer\Logs</span><span class="sxs-lookup"><span data-stu-id="7d136-119">Log file location: <em>%windir%\Microsoft Application Virtualization Sequencer\Logs</span></span></em></p>
<p><span data-ttu-id="7d136-120">[Valor do token do modelo] Local do arquivo de log do App-V 4.6: <em> %windir%\Program Comuns\microsoft Application Virtualization Sequencer\Logs </em> [valor de token do modelo]</span><span class="sxs-lookup"><span data-stu-id="7d136-120">[Template Token Value] App-V4.6 log file location: <em>%windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs</em>[Template Token Value]</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="7d136-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d136-121">Related topics</span></span>


[<span data-ttu-id="7d136-122">Referência do Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="7d136-122">Application Virtualization Sequencer Reference</span></span>](application-virtualization-sequencer-reference.md)

 

 





