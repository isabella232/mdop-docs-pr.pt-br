---
title: Como usar o Console de Gerenciamento de Clientes do App-V 5.0
description: Como usar o Console de Gerenciamento de Clientes do App-V 5.0
author: dansimp
ms.assetid: 36398307-57dd-40f3-9d4f-b09f44fd37c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8541e5bc59334b9074a3940dad7cdf0114205d4c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796205"
---
# <span data-ttu-id="fe403-103">Como usar o Console de Gerenciamento de Clientes do App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="fe403-103">Using the App-V 5.0 Client Management Console</span></span>


<span data-ttu-id="fe403-104">Este tópico fornece informações sobre como você pode configurar e gerenciar o cliente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="fe403-104">This topic provides information about how you can configure and manage the App-V 5.0 client.</span></span>

## <span data-ttu-id="fe403-105">Modificar a configuração do cliente do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="fe403-105">Modify App-V 5.0 client configuration</span></span>


<span data-ttu-id="fe403-106">O cliente App-V 5,0 tem configurações associadas que podem ser configuradas para determinar como o cliente será executado em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="fe403-106">The App-V 5.0 client has associated settings that can be configured to determine how the client will run in your environment.</span></span> <span data-ttu-id="fe403-107">Você pode gerenciar essas configurações no computador que executa o cliente ou usando o PowerShell ou a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="fe403-107">You can manage these settings on the computer that runs the client or by using PowerShell or Group Policy.</span></span> <span data-ttu-id="fe403-108">Para obter mais informações sobre como modificar o cliente usando a configuração do PowerShell ou da política de grupo, consulte [como modificar a configuração do cliente usando o PowerShell](how-to-modify-client-configuration-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="fe403-108">For more information about how to modify the client using PowerShell or Group Policy configuration see, [How to Modify Client Configuration by Using PowerShell](how-to-modify-client-configuration-by-using-powershell.md).</span></span>

## <a href="" id="the-app-v-5-0-client-management-console-"></a><span data-ttu-id="fe403-109">O console de gerenciamento do cliente do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="fe403-109">The App-V 5.0 client management console</span></span>


<span data-ttu-id="fe403-110">Você pode obter informações sobre o cliente App-V 5,0 ou executar tarefas específicas usando o console de gerenciamento do App-V 5,0 Client.</span><span class="sxs-lookup"><span data-stu-id="fe403-110">You can obtain information about the App-V 5.0 client or perform specific tasks by using the App-V 5.0 client management console.</span></span> <span data-ttu-id="fe403-111">Muitas das tarefas que você pode executar no console de gerenciamento de cliente também pode executar usando o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fe403-111">Many of the tasks that you can perform in the client management console you can also perform by using PowerShell.</span></span> <span data-ttu-id="fe403-112">Os cmdlets associados do PowerShell para cada ação também são exibidos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fe403-112">The associated PowerShell cmdlets for each action are also displayed in the following table.</span></span> <span data-ttu-id="fe403-113">Para obter mais informações sobre como usar o PowerShell, consulte [administrando o App-V usando o PowerShell](administering-app-v-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="fe403-113">For more information about how to use PowerShell, see [Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md).</span></span>

<span data-ttu-id="fe403-114">O console de gerenciamento de cliente contém as guias principais descritas a seguir.</span><span class="sxs-lookup"><span data-stu-id="fe403-114">The client management console contains the following described main tabs.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fe403-115">Tab</span><span class="sxs-lookup"><span data-stu-id="fe403-115">Tab</span></span></th>
<th align="left"><span data-ttu-id="fe403-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe403-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe403-117">Visão geral</span><span class="sxs-lookup"><span data-stu-id="fe403-117">Overview</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe403-118">A <strong> guia Visão geral </strong> contém os seguintes elementos:</span><span class="sxs-lookup"><span data-stu-id="fe403-118">The <strong>Overview</strong> tab contains the following elements:</span></span></p>
<ul>
<li><p><span data-ttu-id="fe403-119">Update – use o <strong> </strong> bloco Update para atualizar um aplicativo virtualizado ou receber um novo pacote virtualizado.</span><span class="sxs-lookup"><span data-stu-id="fe403-119">Update – Use the <strong>Update</strong> tile to refresh a virtualized application or to receive a new virtualized package.</span></span></p>
<p><span data-ttu-id="fe403-120">A <strong> última atualização </strong> exibe a versão atual do pacote virtualizado.</span><span class="sxs-lookup"><span data-stu-id="fe403-120">The <strong>Last Refresh</strong> displays the current version of the virtualized package.</span></span></p></li>
<li><p><span data-ttu-id="fe403-121">Baixar todos os aplicativos virtuais – use <strong> o </strong> bloco de download para baixar todos os pacotes provisionados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="fe403-121">Download all virtual applications – Use the <strong>Download</strong> tile to download all of the packages provisioned to the current user.</span></span></p>
<p><span data-ttu-id="fe403-122">(Cmdlet associado do PowerShell: <strong> Mount-AppvClientPackage </strong> )</span><span class="sxs-lookup"><span data-stu-id="fe403-122">(Associated PowerShell cmdlet: <strong>Mount-AppvClientPackage</strong>)</span></span></p>
<p></p></li>
<li><p><span data-ttu-id="fe403-123">Trabalhar offline – Use este bloco para impedir todas as atualizações automáticas e manuais do aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="fe403-123">Work Offline – Use this tile to disallow all automatic and manual virtual application updates.</span></span></p>
<p><span data-ttu-id="fe403-124">(Cmdlet associado do PowerShell: <strong> Set-AppvPublishServer – UserRefreshEnabled – GlobalRefreshEnabled </strong> )</span><span class="sxs-lookup"><span data-stu-id="fe403-124">(Associated PowerShell cmdlet: <strong>Set-AppvPublishServer –UserRefreshEnabled –GlobalRefreshEnabled</strong>)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fe403-125">Aplicativos virtuais</span><span class="sxs-lookup"><span data-stu-id="fe403-125">Virtual Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe403-126">A <strong> guia aplicativos virtuais </strong> exibe todos os pacotes que foram publicados para o usuário.</span><span class="sxs-lookup"><span data-stu-id="fe403-126">The <strong>VIRTUAL APPS</strong> tab displays all of the packages that have been published to the user.</span></span> <span data-ttu-id="fe403-127">Você também pode clicar em um pacote específico e ver todos os aplicativos que fazem parte do pacote.</span><span class="sxs-lookup"><span data-stu-id="fe403-127">You can also click a specific package and see all of the applications that are part of that package.</span></span> <span data-ttu-id="fe403-128">Isso exibe informações sobre pacotes que estão sendo usados no momento e quanto de cada pacote foi baixado para o computador.</span><span class="sxs-lookup"><span data-stu-id="fe403-128">This displays information about packages that are currently in use and how much of each package has been downloaded to the computer.</span></span> <span data-ttu-id="fe403-129">Você também pode iniciar e parar downloads de pacotes.</span><span class="sxs-lookup"><span data-stu-id="fe403-129">You can also start and stop package downloads.</span></span> <span data-ttu-id="fe403-130">Além disso, você pode reparar o estado do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe403-130">Additionally, you can repair the user state.</span></span> <span data-ttu-id="fe403-131">Um reparo excluirá todos os dados do usuário associados a um pacote.</span><span class="sxs-lookup"><span data-stu-id="fe403-131">A repair will delete all user data that is associated with a package.</span></span></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe403-132">Grupos de conexão do aplicativo</span><span class="sxs-lookup"><span data-stu-id="fe403-132">App Connection Groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe403-133">A <strong> guia grupos de conexão de aplicativos </strong> exibe todos os grupos de conexão que estão disponíveis para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="fe403-133">The <strong>APP CONNECTION GROUPS</strong> tab displays all of the connection groups that are available to the current user.</span></span> <span data-ttu-id="fe403-134">Clique em um grupo de conexão específico para ver todos os pacotes que fazem parte do grupo selecionado.</span><span class="sxs-lookup"><span data-stu-id="fe403-134">Click a specific connection group to see all of the packages that are part of the selected group.</span></span> <span data-ttu-id="fe403-135">Isso exibe informações sobre grupos de conexão que já estão em uso e quanto do conteúdo do grupo de conexão foram baixados para o computador.</span><span class="sxs-lookup"><span data-stu-id="fe403-135">This displays information about connection groups that are already in use and how much of the connection group contents have been downloaded to the computer.</span></span> <span data-ttu-id="fe403-136">Além disso, você pode iniciar e parar downloads do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="fe403-136">Additionally, you can start and stop connection group downloads.</span></span> <span data-ttu-id="fe403-137">Você pode usar esta seção para iniciar um reparo.</span><span class="sxs-lookup"><span data-stu-id="fe403-137">You can use this section to initiate a repair.</span></span> <span data-ttu-id="fe403-138">Um reparo removerá todo o estado do usuário associado a um grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="fe403-138">A repair will remove all of the user state that is associated a connection group.</span></span></p>
<p><span data-ttu-id="fe403-139">(Cmdlets associados do PowerShell: Download- <strong> Mount-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="fe403-139">(Associated PowerShell cmdlets: Download - <strong>Mount-AppvClientConnectionGroup</strong>.</span></span> <span data-ttu-id="fe403-140">Repair- <strong> AppvClientConnectionGroup </strong> .)</span><span class="sxs-lookup"><span data-stu-id="fe403-140">Repair -<strong>AppvClientConnectionGroup</strong>.)</span></span></p>
<p></p></td>
</tr>
</tbody>
</table>

 

[<span data-ttu-id="fe403-141">Como acessar o Console de Gerenciamento do cliente</span><span class="sxs-lookup"><span data-stu-id="fe403-141">How to Access the Client Management Console</span></span>](how-to-access-the-client-management-console.md)

[<span data-ttu-id="fe403-142">Como configurar o cliente para receber atualizações de pacotes e grupos de conexão do servidor de publicação</span><span class="sxs-lookup"><span data-stu-id="fe403-142">How to Configure the Client to Receive Package and Connection Groups Updates From the Publishing Server</span></span>](how-to-configure-the-client-to-receive-package-and-connection-groups-updates-from-the-publishing-server-beta.md)






## <span data-ttu-id="fe403-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fe403-143">Related topics</span></span>


[<span data-ttu-id="fe403-144">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="fe403-144">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





