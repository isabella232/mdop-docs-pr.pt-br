---
title: Administração do App-V usando o PowerShell
description: Administração do App-V usando o PowerShell
author: dansimp
ms.assetid: 1ff4686a-1e19-4eff-b648-ada091281094
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0e7f9171e0ac5589d8f1935e715dfdb9c349192d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796605"
---
# <span data-ttu-id="f7621-103">Administração do App-V usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7621-103">Administering App-V by Using PowerShell</span></span>


<span data-ttu-id="f7621-104">O Microsoft Application Virtualization (App-V) 5,0 fornece cmdlets do Windows PowerShell, que podem ajudar os administradores a executar várias tarefas do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f7621-104">Microsoft Application Virtualization (App-V) 5.0 provides Windows PowerShell cmdlets, which can help administrators perform various App-V 5.0 tasks.</span></span> <span data-ttu-id="f7621-105">As seções a seguir fornecem mais informações sobre como usar o PowerShell com o App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f7621-105">The following sections provide more information about using PowerShell with App-V 5.0.</span></span>

## <span data-ttu-id="f7621-106">Como administrar o App-V 5,0 usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7621-106">How to administer App-V 5.0 by using PowerShell</span></span>


<span data-ttu-id="f7621-107">Use os seguintes procedimentos do PowerShell para executar várias tarefas do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f7621-107">Use the following PowerShell procedures to perform various App-V 5.0 tasks.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f7621-108">Nome</span><span class="sxs-lookup"><span data-stu-id="f7621-108">Name</span></span></th>
<th align="left"><span data-ttu-id="f7621-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7621-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md" data-raw-source="[How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md)"><span data-ttu-id="f7621-110">Como carregar os cmdlets do PowerShell e obter ajuda sobre cmdlets</span><span class="sxs-lookup"><span data-stu-id="f7621-110">How to Load the PowerShell Cmdlets and Get Cmdlet Help</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="f7621-111">Descreve como instalar os cmdlets do PowerShell e localizar exemplos e ajuda do cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7621-111">Describes how to install the PowerShell cmdlets and find cmdlet help and examples.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="f7621-112">Como gerenciar pacotes do App-V 5.0 em execução em um computador autônomo usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7621-112">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="f7621-113">Descreve como gerenciar o ciclo de vida do pacote do cliente em um computador autônomo usando o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f7621-113">Describes how to manage the client package lifecycle on a stand-alone computer using PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="f7621-114">Como gerenciar grupos de conexão em um computador autônomo usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7621-114">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="f7621-115">Descreve como gerenciar grupos de conexão usando o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f7621-115">Describes how to manage connection groups using PowerShell.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-modify-client-configuration-by-using-powershell.md" data-raw-source="[How to Modify Client Configuration by Using PowerShell](how-to-modify-client-configuration-by-using-powershell.md)"><span data-ttu-id="f7621-116">Como modificar a configuração do cliente usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7621-116">How to Modify Client Configuration by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="f7621-117">Descreve como modificar o cliente usando o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f7621-117">Describes how to modify the client using PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-apply-the-user-configuration-file-by-using-powershell.md" data-raw-source="[How to Apply the User Configuration File by Using PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell.md)"><span data-ttu-id="f7621-118">Como aplicar o arquivo de configuração do usuário usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7621-118">How to Apply the User Configuration File by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="f7621-119">Descreve como aplicar um arquivo de configuração de usuário usando o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f7621-119">Describes how to apply a user configuration file using PowerShell.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-apply-the-deployment-configuration-file-by-using-powershell.md" data-raw-source="[How to Apply the Deployment Configuration File by Using PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)"><span data-ttu-id="f7621-120">Como aplicar o arquivo de configuração da implantação usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7621-120">How to Apply the Deployment Configuration File by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="f7621-121">Descreve como aplicar um arquivo de configuração de implantação usando o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f7621-121">Describes how to apply a deployment configuration file using PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-sequence-a-package--by-using-powershell-50.md" data-raw-source="[How to Sequence a Package by Using PowerShell](how-to-sequence-a-package--by-using-powershell-50.md)"><span data-ttu-id="f7621-122">Como sequenciar um pacote usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7621-122">How to Sequence a Package by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="f7621-123">Descreve como criar um novo pacote usando o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f7621-123">Describes how to create a new package using PowerShell.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-create-a-package-accelerator-by-using-powershell.md" data-raw-source="[How to Create a Package Accelerator by Using PowerShell](how-to-create-a-package-accelerator-by-using-powershell.md)"><span data-ttu-id="f7621-124">Como criar um acelerador de pacotes usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7621-124">How to Create a Package Accelerator by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="f7621-125">Descreve como criar um acelerador de pacote usando o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f7621-125">Describes how to create a package accelerator using PowerShell.</span></span> <span data-ttu-id="f7621-126">Você pode usar aceleradores de pacote sequenciando automaticamente aplicativos grandes e complexos.</span><span class="sxs-lookup"><span data-stu-id="f7621-126">You can use package accelerators automatically sequence large, complex applications.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md" data-raw-source="[How to Enable Reporting on the App-V 5.0 Client by Using PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)"><span data-ttu-id="f7621-127">Como habilitar relatórios no cliente do App-V 5.0 usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7621-127">How to Enable Reporting on the App-V 5.0 Client by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="f7621-128">Descreve como habilitar o computador que executa a App-V 5,0 para enviar informações de relatório.</span><span class="sxs-lookup"><span data-stu-id="f7621-128">Describes how to enable the computer running the App-V 5.0 to send reporting information.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md" data-raw-source="[How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md)"><span data-ttu-id="f7621-129">Como instalar os bancos de dados do App-V e converter os identificadores de segurança associados usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7621-129">How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="f7621-130">Descreve como obter uma matriz de nomes de conta e convertê-los no SID correspondente nos formatos padrão e hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="f7621-130">Describes how to take an array of account names and to convert each of them to the corresponding SID in standard and hexadecimal formats.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f7621-131">Manipulação de erros do PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7621-131">PowerShell Error Handling</span></span>


<span data-ttu-id="f7621-132">Use a tabela a seguir para obter informações sobre a manipulação de erros do PowerShell do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f7621-132">Use the following table for information about App-V 5.0 PowerShell error handling.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f7621-133">Evento</span><span class="sxs-lookup"><span data-stu-id="f7621-133">Event</span></span></th>
<th align="left"><span data-ttu-id="f7621-134">Ação</span><span class="sxs-lookup"><span data-stu-id="f7621-134">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7621-135">Usando o atributo RollbackOnError com scripts inseridos</span><span class="sxs-lookup"><span data-stu-id="f7621-135">Using the RollbackOnError attribute with embedded scripts</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7621-136">Quando você usa o <strong> </strong> atributo RollbackOnError com scripts inseridos, o atributo é ignorado para os seguintes eventos:</span><span class="sxs-lookup"><span data-stu-id="f7621-136">When you use the <strong>RollbackOnError</strong> attribute with embedded scripts, the attribute is ignored for the following events:</span></span></p>
<ul>
<li><p><span data-ttu-id="f7621-137">Como remover um pacote</span><span class="sxs-lookup"><span data-stu-id="f7621-137">Removing a package</span></span></p></li>
<li><p><span data-ttu-id="f7621-138">Cancelando a publicação de um pacote</span><span class="sxs-lookup"><span data-stu-id="f7621-138">Unpublishing a package</span></span></p></li>
<li><p><span data-ttu-id="f7621-139">Finalizando um ambiente virtual</span><span class="sxs-lookup"><span data-stu-id="f7621-139">Terminating a virtual environment</span></span></p></li>
<li><p><span data-ttu-id="f7621-140">Finalizando um processo</span><span class="sxs-lookup"><span data-stu-id="f7621-140">Terminating a process</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f7621-141">O nome do pacote contém<strong>$</span><span class="sxs-lookup"><span data-stu-id="f7621-141">Package name contains <strong>$</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f7621-142">Se um nome de pacote contiver o caractere ( <strong> $ </strong> ), você deve usar uma aspa simples ( <strong> ' </strong> ), por exemplo,</span><span class="sxs-lookup"><span data-stu-id="f7621-142">If a package name contains the character ( <strong>$</strong> ), you must use a single-quote ( <strong>‘</strong> ), for example,</span></span></p>
<p><strong><span data-ttu-id="f7621-143">Add-AppvClientPackage ' contoso $ app. AppV '</span><span class="sxs-lookup"><span data-stu-id="f7621-143">Add-AppvClientPackage ‘Contoso$App.appv’</span></span></strong></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="f7621-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7621-144">Related topics</span></span>


[<span data-ttu-id="f7621-145">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f7621-145">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





