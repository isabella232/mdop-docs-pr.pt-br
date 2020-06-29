---
title: Como realizar tarefas do DaRT usando comandos do PowerShell
description: Como realizar tarefas do DaRT usando comandos do PowerShell
author: dansimp
ms.assetid: bc788b00-38c7-4f57-a832-916b68264d89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f8ff87aa09555b93ca04a6ec7fa5dd4ba8504514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799445"
---
# <span data-ttu-id="08702-103">Como realizar tarefas do DaRT usando comandos do PowerShell</span><span class="sxs-lookup"><span data-stu-id="08702-103">How to Perform DaRT Tasks by Using PowerShell Commands</span></span>


<span data-ttu-id="08702-104">O conjunto de ferramentas de diagnóstico e recuperação (DaRT) da Microsoft 8,0 fornece o conjunto de cmdlets do Windows PowerShell listados a seguir.</span><span class="sxs-lookup"><span data-stu-id="08702-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="08702-105">Os administradores podem usar esses cmdlets do PowerShell para executar várias tarefas do DaRT 8,0 Server a partir do prompt de comando, e não do assistente de imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="08702-105">Administrators can use these PowerShell cmdlets to perform various DaRT 8.0 server tasks from the command prompt rather than from the DaRT Recovery Image wizard.</span></span>

## <span data-ttu-id="08702-106">Para administrar o DaRT usando comandos do PowerShell</span><span class="sxs-lookup"><span data-stu-id="08702-106">To administer DaRT by using PowerShell commands</span></span>


<span data-ttu-id="08702-107">Use os cmdlets do PowerShell descritos aqui para administrar o DaRT.</span><span class="sxs-lookup"><span data-stu-id="08702-107">Use the PowerShell cmdlets described here to administer DaRT.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="08702-108">Nome</span><span class="sxs-lookup"><span data-stu-id="08702-108">Name</span></span></th>
<th align="left"><span data-ttu-id="08702-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="08702-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08702-110">Copy-DartImage</span><span class="sxs-lookup"><span data-stu-id="08702-110">Copy-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="08702-111">Grava uma ISO em um CD, DVD ou unidade USB.</span><span class="sxs-lookup"><span data-stu-id="08702-111">Burns an ISO to a CD, DVD, or USB drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08702-112">Export-DartImage</span><span class="sxs-lookup"><span data-stu-id="08702-112">Export-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="08702-113">Permite que o arquivo WIM de origem, que contém uma imagem DaRT, seja convertido em um arquivo ISO.</span><span class="sxs-lookup"><span data-stu-id="08702-113">Allows the source WIM file, which contains a DaRT image, to be converted into an ISO file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="08702-114">New-DartConfiguration</span><span class="sxs-lookup"><span data-stu-id="08702-114">New-DartConfiguration</span></span></p></td>
<td align="left"><p><span data-ttu-id="08702-115">Cria um objeto de configuração DaRT que é necessário para aplicar um conjunto de ferramentas DaRT a uma imagem do Windows.</span><span class="sxs-lookup"><span data-stu-id="08702-115">Creates a DaRT configuration object that is needed to apply a DaRT toolset to a Windows Image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="08702-116">Set-DartImage</span><span class="sxs-lookup"><span data-stu-id="08702-116">Set-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="08702-117">Aplica um objeto DartConfiguration a uma imagem montada do Windows.</span><span class="sxs-lookup"><span data-stu-id="08702-117">Applies a DartConfiguration object to a mounted Windows Image.</span></span> <span data-ttu-id="08702-118">Isso inclui a adição de todos os arquivos, configuração e dependências do pacote.</span><span class="sxs-lookup"><span data-stu-id="08702-118">This includes adding all files, configuration, and package dependencies.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="08702-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="08702-119">Related topics</span></span>


[<span data-ttu-id="08702-120">Administrar o DaRT 8.0 usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="08702-120">Administering DaRT 8.0 Using PowerShell</span></span>](administering-dart-80-using-powershell-dart-8.md)

 

 





