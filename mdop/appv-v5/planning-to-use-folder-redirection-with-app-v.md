---
title: Planejando o uso do redirecionamento de pastas com o App-V
description: Planejando o uso do redirecionamento de pastas com o App-V
author: dansimp
ms.assetid: 2a4deeed-fdc0-465c-b88a-3a2fbbf27436
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b25b3531faa495275bf4e478389f44790d8eed9a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796235"
---
# <span data-ttu-id="4b600-103">Planejando o uso do redirecionamento de pastas com o App-V</span><span class="sxs-lookup"><span data-stu-id="4b600-103">Planning to Use Folder Redirection with App-V</span></span>


<span data-ttu-id="4b600-104">O App-V 5,0 SP2 permite o uso do redirecionamento de pastas, um recurso que permite aos usuários e administradores redirecionar o caminho de uma pasta para um novo local.</span><span class="sxs-lookup"><span data-stu-id="4b600-104">App-V 5.0 SP2 supports the use of folder redirection, a feature that enables users and administrators to redirect the path of a folder to a new location.</span></span>

<span data-ttu-id="4b600-105">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="4b600-105">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="4b600-106">Requisitos para usar o redirecionamento de pastas</span><span class="sxs-lookup"><span data-stu-id="4b600-106">Requirements for using folder redirection</span></span>](#bkmk-folder-redir-reqs)

-   [<span data-ttu-id="4b600-107">Como configurar o redirecionamento de pastas para uso com o App-V</span><span class="sxs-lookup"><span data-stu-id="4b600-107">How to configure folder redirection for use with App-V</span></span>](#bkmk-folder-redir-cfg)

-   [<span data-ttu-id="4b600-108">Como o redirecionamento de pastas funciona com o App-V</span><span class="sxs-lookup"><span data-stu-id="4b600-108">How folder redirection works with App-V</span></span>](#bkmk-folder-redir-works)

-   [<span data-ttu-id="4b600-109">Visão geral do redirecionamento de pastas</span><span class="sxs-lookup"><span data-stu-id="4b600-109">Overview of folder redirection</span></span>](#bkmk-folder-redir-overview)

## <a href="" id="bkmk-folder-redir-reqs"></a><span data-ttu-id="4b600-110">Requisitos e cenários sem suporte para o uso do redirecionamento de pastas</span><span class="sxs-lookup"><span data-stu-id="4b600-110">Requirements and unsupported scenarios for using folder redirection</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b600-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b600-111">Requirements</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b600-112">Para usar o redirecionamento de pastas% AppData%, você deve:</span><span class="sxs-lookup"><span data-stu-id="4b600-112">To use %AppData% folder redirection, you must:</span></span></p>
<ul>
<li><p><span data-ttu-id="4b600-113">Ter um pacote App-V que tenha uma pasta de sistema de arquivos virtual do AppData (VFS).</span><span class="sxs-lookup"><span data-stu-id="4b600-113">Have an App-V package that has an AppData virtual file system (VFS) folder.</span></span></p></li>
<li><p><span data-ttu-id="4b600-114">Habilite o redirecionamento de pastas e redirecione as pastas dos usuários para uma pasta compartilhada, geralmente uma pasta de rede.</span><span class="sxs-lookup"><span data-stu-id="4b600-114">Enable folder redirection and redirect users’ folders to a shared folder, typically a network folder.</span></span></p></li>
<li><p><span data-ttu-id="4b600-115">Faça o roaming ou nenhum dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="4b600-115">Roam both or neither of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="4b600-116">Arquivos em%appdata%\Microsoft\AppV\Client\Catalog</span><span class="sxs-lookup"><span data-stu-id="4b600-116">Files under %appdata%\Microsoft\AppV\Client\Catalog</span></span></p></li>
<li><p><span data-ttu-id="4b600-117">Configurações do registro em HKEY_CURRENT_USER \Software\Microsoft\AppV\Client\Packages</span><span class="sxs-lookup"><span data-stu-id="4b600-117">Registry settings under HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages</span></span></p>
<p><span data-ttu-id="4b600-118">Para obter mais detalhes, consulte <a href="application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs" data-raw-source="[Application Publishing and Client Interaction](application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs)"> publicação de aplicativos e interação do cliente </a> .</span><span class="sxs-lookup"><span data-stu-id="4b600-118">For more detail, see <a href="application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs" data-raw-source="[Application Publishing and Client Interaction](application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs)">Application Publishing and Client Interaction</a>.</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="4b600-119">Verifique se as seguintes pastas estão disponíveis para cada usuário que faz logon no computador que está executando o aplicativo App-V 5,0 SP2 ou posterior:</span><span class="sxs-lookup"><span data-stu-id="4b600-119">Ensure that the following folders are available to each user who logs into the computer that is running the App-V 5.0 SP2 or later client:</span></span></p>
<ul>
<li><p><span data-ttu-id="4b600-120">% AppData% está configurado para o local de rede desejado (com ou sem <a href="https://technet.microsoft.com/library/cc780552.aspx" data-raw-source="[Offline Files](https://technet.microsoft.com/library/cc780552.aspx)"> suporte a arquivos offline </a> ).</span><span class="sxs-lookup"><span data-stu-id="4b600-120">%AppData% is configured to the desired network location (with or without <a href="https://technet.microsoft.com/library/cc780552.aspx" data-raw-source="[Offline Files](https://technet.microsoft.com/library/cc780552.aspx)">Offline Files</a> support).</span></span></p></li>
<li><p><span data-ttu-id="4b600-121">% LocalAppData% está configurado para a pasta local desejada.</span><span class="sxs-lookup"><span data-stu-id="4b600-121">%LocalAppData% is configured to the desired local folder.</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4b600-122">Cenários sem suporte</span><span class="sxs-lookup"><span data-stu-id="4b600-122">Unsupported scenarios</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="4b600-123">Configurando o% LocalAppData% como uma unidade de rede.</span><span class="sxs-lookup"><span data-stu-id="4b600-123">Configuring %LocalAppData% as a network drive.</span></span></p></li>
<li><p><span data-ttu-id="4b600-124">Redirecionar o menu Iniciar para uma única pasta para vários usuários.</span><span class="sxs-lookup"><span data-stu-id="4b600-124">Redirecting the Start menu to a single folder for multiple users.</span></span></p></li>
<li><p><span data-ttu-id="4b600-125">Se o roaming AppData (% AppData%) for Redirecionado para um compartilhamento de rede que não está disponível, aplicativos App-V falharão ao iniciarão da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="4b600-125">If roaming AppData (%AppData%) is redirected to a network share that is not available, App-V applications will fail to launch as follows:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4b600-126">Versão do App-V</span><span class="sxs-lookup"><span data-stu-id="4b600-126">App-V version</span></span></th>
<th align="left"><span data-ttu-id="4b600-127">Descrição do cenário</span><span class="sxs-lookup"><span data-stu-id="4b600-127">Scenario description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b600-128">Nos hotfixes do App-V 5,0 a App-V 5,0 SP2 Plus</span><span class="sxs-lookup"><span data-stu-id="4b600-128">In App-V 5.0 through App-V 5.0 SP2 plus hotfixes</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b600-129">Essa falha ocorrerá independentemente de os arquivos offline estarem habilitados.</span><span class="sxs-lookup"><span data-stu-id="4b600-129">This failure will occur regardless of whether Offline Files is enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4b600-130">No App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="4b600-130">In App-V 5.0 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b600-131">Se o compartilhamento de rede não disponível tiver sido habilitado para arquivos offline, o aplicativo App-V será iniciado com êxito.</span><span class="sxs-lookup"><span data-stu-id="4b600-131">If the unavailable network share has been enabled for Offline Files, the App-V application will start successfully.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-cfg"></a><span data-ttu-id="4b600-132">Como configurar o redirecionamento de pastas para uso com o App-V</span><span class="sxs-lookup"><span data-stu-id="4b600-132">How to configure folder redirection for use with App-V</span></span>


<span data-ttu-id="4b600-133">O redirecionamento de pastas pode ser aplicado a diferentes pastas, como área de trabalho, meus documentos, minhas imagens, etc. No entanto, a única pasta que impacta o uso de aplicativos App-V é a pasta Roaming do usuário do usuário (% AppData%).</span><span class="sxs-lookup"><span data-stu-id="4b600-133">Folder redirection can be applied to different folders, such as Desktop, My Documents, My Pictures, etc. However, the only folder that impacts the use of App-V applications is the user’s roaming AppData folder (%AppData%).</span></span> <span data-ttu-id="4b600-134">Você pode aplicar o redirecionamento de pastas a qualquer outra pasta com suporte sem afetar o App-V.</span><span class="sxs-lookup"><span data-stu-id="4b600-134">You can apply folder redirection to any other supported folders without impacting App-V.</span></span>

## <a href="" id="bkmk-folder-redir-works"></a><span data-ttu-id="4b600-135">Como o redirecionamento de pastas funciona com o App-V</span><span class="sxs-lookup"><span data-stu-id="4b600-135">How folder redirection works with App-V</span></span>


<span data-ttu-id="4b600-136">A tabela a seguir descreve como o redirecionamento de pastas funciona quando% AppData% é redirecionado para uma rede e quando você atende aos requisitos listados anteriormente neste artigo.</span><span class="sxs-lookup"><span data-stu-id="4b600-136">The following table describes how folder redirection works when %AppData% is redirected to a network and when you have met the requirements listed earlier in this article.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4b600-137">Estado do ambiente virtual</span><span class="sxs-lookup"><span data-stu-id="4b600-137">Virtual environment state</span></span></th>
<th align="left"><span data-ttu-id="4b600-138">Ação que ocorre</span><span class="sxs-lookup"><span data-stu-id="4b600-138">Action that occurs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b600-139">Quando o ambiente virtual é iniciado</span><span class="sxs-lookup"><span data-stu-id="4b600-139">When the virtual environment starts</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b600-140">A pasta de AppData do sistema de arquivos virtual (VFS) é mapeada para a pasta local AppData (% LocalAppData%) em vez de na pasta Roaming AppData do usuário (% AppData%).</span><span class="sxs-lookup"><span data-stu-id="4b600-140">The virtual file system (VFS) AppData folder is mapped to the local AppData folder (%LocalAppData%) instead of to the user’s roaming AppData folder (%AppData%).</span></span></p>
<ul>
<li><p><span data-ttu-id="4b600-141">LocalAppData contém um cache local da pasta de AppData do roaming do usuário para o pacote em uso.</span><span class="sxs-lookup"><span data-stu-id="4b600-141">LocalAppData contains a local cache of the user’s roaming AppData folder for the package in use.</span></span> <span data-ttu-id="4b600-142">O cache local está localizado em:</span><span class="sxs-lookup"><span data-stu-id="4b600-142">The local cache is located under:</span></span></p>
<p><code>%LocalAppData%\Microsoft\AppV\Client\VFS\PackageGUID\AppData</code></p></li>
<li><p><span data-ttu-id="4b600-143">Os dados mais recentes da pasta roaming de AppData do usuário são copiados para e substituem os dados atualmente no cache local.</span><span class="sxs-lookup"><span data-stu-id="4b600-143">The latest data from the user’s roaming AppData folder is copied to and replaces the data currently in the local cache.</span></span></p></li>
<li><p><span data-ttu-id="4b600-144">Enquanto o ambiente virtual está em execução, os dados continuam a ser salvos no cache local.</span><span class="sxs-lookup"><span data-stu-id="4b600-144">While the virtual environment is running, data continues to be saved to the local cache.</span></span> <span data-ttu-id="4b600-145">Os dados são servidos somente a partir de% LocalAppData% e não são movidos ou sincronizados com% AppData% até o usuário final desligar o computador.</span><span class="sxs-lookup"><span data-stu-id="4b600-145">Data is served only out of %LocalAppData% and is not moved or synchronized with %AppData% until the end user shuts down the computer.</span></span></p></li>
<li><p><span data-ttu-id="4b600-146">As entradas na pasta AppData são feitas usando o contexto do usuário, e não o contexto do sistema.</span><span class="sxs-lookup"><span data-stu-id="4b600-146">Entries to the AppData folder are made using the user context, not the system context.</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="4b600-147">Observação</span><span class="sxs-lookup"><span data-stu-id="4b600-147">Note</span></span></strong><br/><p><span data-ttu-id="4b600-148">Às vezes, o redirecionamento de pastas do cliente App-V falha ao mover arquivos de% AppData% para% LocalAppData%.</span><span class="sxs-lookup"><span data-stu-id="4b600-148">The App-V client folder redirection sometimes fails to move files from %AppData% to %LocalAppData%.</span></span> <span data-ttu-id="4b600-149">Confira <a href="release-notes-for-app-v-50-sp2.md#bkmk-folderredirection" data-raw-source="[Release Notes for App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md#bkmk-folderredirection)"> notas de versão do App-V 5,0 SP2 </a> .</span><span class="sxs-lookup"><span data-stu-id="4b600-149">See <a href="release-notes-for-app-v-50-sp2.md#bkmk-folderredirection" data-raw-source="[Release Notes for App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md#bkmk-folderredirection)">Release Notes for App-V 5.0 SP2</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4b600-150">Quando o ambiente virtual é encerrado</span><span class="sxs-lookup"><span data-stu-id="4b600-150">When the virtual environment shuts down</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b600-151">Os dados armazenados em cache locais em AppData (roaming) são compactados e copiados para a pasta "real" de AppData em roaming em% AppData%.</span><span class="sxs-lookup"><span data-stu-id="4b600-151">The local cached data in AppData (roaming) is zipped up and copied to the “real” roaming AppData folder in %AppData%.</span></span> <span data-ttu-id="4b600-152">Um carimbo de data/hora, que indica o último carregamento conhecido, é salvo simultaneamente como uma chave do registro em:</span><span class="sxs-lookup"><span data-stu-id="4b600-152">A time stamp, which indicates the last known upload, is simultaneously saved as a registry key under:</span></span></p>
<p><code>HKCU\Software\Microsoft\AppV\Client\Packages&amp;lt;PACKAGE_GUID&gt;\AppDataTime</code></p>
<p><span data-ttu-id="4b600-153">Para fornecer redundância, o App-V 5,0 mantém as três cópias mais recentes dos dados compactados em% AppData%.</span><span class="sxs-lookup"><span data-stu-id="4b600-153">To provide redundancy, App-V 5.0 keeps the three most recent copies of the compressed data under %AppData%.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-overview"></a><span data-ttu-id="4b600-154">Visão geral do redirecionamento de pastas</span><span class="sxs-lookup"><span data-stu-id="4b600-154">Overview of folder redirection</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b600-155">Finalidade</span><span class="sxs-lookup"><span data-stu-id="4b600-155">Purpose</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b600-156">Permite que os usuários finais trabalhem com arquivos, que foram redirecionados para outra pasta, como se os arquivos ainda existissem na unidade local.</span><span class="sxs-lookup"><span data-stu-id="4b600-156">Enables end users to work with files, which have been redirected to another folder, as if the files still existed on the local drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4b600-157">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b600-157">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b600-158">O redirecionamento de pastas permite aos usuários e administradores redirecionar o caminho de uma pasta para um local de rede.</span><span class="sxs-lookup"><span data-stu-id="4b600-158">Folder redirection allows users and administrators to redirect the path of a folder to a network location.</span></span> <span data-ttu-id="4b600-159">Os documentos na pasta estão disponíveis para o usuário em qualquer computador na rede.</span><span class="sxs-lookup"><span data-stu-id="4b600-159">The documents in the folder are available to the user from any computer on the network.</span></span></p>
<ul>
<li><p><span data-ttu-id="4b600-160">O redirecionamento de pastas permite aos usuários e administradores redirecionar o caminho de uma pasta para um local de rede.</span><span class="sxs-lookup"><span data-stu-id="4b600-160">Folder redirection allows users and administrators to redirect the path of a folder to a network location.</span></span> <span data-ttu-id="4b600-161">Os documentos na pasta estão disponíveis para o usuário em qualquer computador na rede.</span><span class="sxs-lookup"><span data-stu-id="4b600-161">The documents in the folder are available to the user from any computer on the network.</span></span></p></li>
<li><p><span data-ttu-id="4b600-162">O novo local pode ser uma pasta no computador local ou em uma pasta em uma rede compartilhada.</span><span class="sxs-lookup"><span data-stu-id="4b600-162">The new location can be a folder on the local computer or a folder on a shared network.</span></span></p></li>
<li><p><span data-ttu-id="4b600-163">O redirecionamento de pastas atualiza os arquivos imediatamente, enquanto os dados de roaming geralmente são sincronizados quando o usuário faz logon ou logoff.</span><span class="sxs-lookup"><span data-stu-id="4b600-163">Folder redirection updates the files immediately, whereas roaming data is typically synchronized when the user logs in or logs off.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4b600-164">Exemplo de uso</span><span class="sxs-lookup"><span data-stu-id="4b600-164">Usage example</span></span></p></td>
<td align="left"><p><span data-ttu-id="4b600-165">Você pode redirecionar a pasta documentos, que geralmente é armazenada no computador&#39;s local disco rígido, em um local de rede.</span><span class="sxs-lookup"><span data-stu-id="4b600-165">You can redirect the Documents folder, which is usually stored on the computer&#39;s local hard disk, to a network location.</span></span> <span data-ttu-id="4b600-166">O usuário pode acessar os documentos na pasta de qualquer computador na rede.</span><span class="sxs-lookup"><span data-stu-id="4b600-166">The user can access the documents in the folder from any computer on the network.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4b600-167">Mais recursos</span><span class="sxs-lookup"><span data-stu-id="4b600-167">More resources</span></span></p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/cc778976.aspx" data-raw-source="[Folder redirection overview](https://technet.microsoft.com/library/cc778976.aspx)"><span data-ttu-id="4b600-168">Visão geral do redirecionamento de pasta</span><span class="sxs-lookup"><span data-stu-id="4b600-168">Folder redirection overview</span></span></a></p></td>
</tr>
</tbody>
</table>
















