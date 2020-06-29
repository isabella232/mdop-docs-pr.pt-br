---
title: Planejamento da migração de versões anteriores
description: Planejamento da migração de versões anteriores
author: dansimp
ms.assetid: 62967bf1-542f-41b0-838f-c62f3430ac73
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9b239e09da06270b30b401151cf12e817e2cf8d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796823"
---
# <span data-ttu-id="ebeaf-103">Planejamento da migração de versões anteriores</span><span class="sxs-lookup"><span data-stu-id="ebeaf-103">Planning for Migration from Previous Versions</span></span>


<span data-ttu-id="ebeaf-104">Antes de tentar atualizar para o Microsoft Application Virtualization 4.5 ou versões posteriores, qualquer versão anterior a 4.1 deve ser atualizada para a versão 4.1.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-104">Before attempting to upgrade to Microsoft Application Virtualization4.5 or later versions, any version prior to4.1 must be upgraded to version4.1.</span></span> <span data-ttu-id="ebeaf-105">Você deve planejar a atualização dos seus clientes primeiro e, em seguida, atualizar os componentes do servidor.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-105">You should plan to upgrade your clients first, and then upgrade the server components.</span></span> <span data-ttu-id="ebeaf-106">Os clientes que foram atualizados para o 4.5 continuarão a funcionar com os servidores do Application Virtualization que ainda não foram atualizados.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-106">Clients that have been upgraded to4.5 will continue to work with Application Virtualization servers that have not yet been upgraded.</span></span> <span data-ttu-id="ebeaf-107">Não há suporte para versões anteriores do cliente em servidores que foram atualizados para 4.5.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-107">Earlier versions of the client are not supported on servers that have been upgraded to4.5.</span></span> <span data-ttu-id="ebeaf-108">Para obter mais informações sobre a atualização dos componentes do sistema, consulte [Considerações sobre implantação e atualização do Application Virtualization](application-virtualization-deployment-and-upgrade-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="ebeaf-108">For more information about upgrading the system components, see [Application Virtualization Deployment and Upgrade Considerations](application-virtualization-deployment-and-upgrade-considerations.md).</span></span>

<span data-ttu-id="ebeaf-109">Para ajudar a garantir uma migração bem-sucedida, os componentes do sistema do Application Virtualization devem ser atualizados na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="ebeaf-109">To help ensure a successful migration, the Application Virtualization system components should be upgraded in the following order:</span></span>

1.  **<span data-ttu-id="ebeaf-110">Clientes de virtualização de aplicativos Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-110">Microsoft Application Virtualization Clients.</span></span>** <span data-ttu-id="ebeaf-111">Para obter instruções passo a passo de atualização, consulte [como atualizar o cliente do Application Virtualization](how-to-upgrade-the-application-virtualization-client.md).</span><span class="sxs-lookup"><span data-stu-id="ebeaf-111">For step-by-step upgrade instructions, see [How to Upgrade the Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md).</span></span>

2.  **<span data-ttu-id="ebeaf-112">Servidores e banco de dados de virtualização de aplicativos Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-112">Microsoft Application Virtualization Servers and Database.</span></span>** <span data-ttu-id="ebeaf-113">Para obter instruções passo a passo de atualização, consulte [como atualizar os servidores e componentes do sistema](how-to-upgrade-the-servers-and-system-components.md).</span><span class="sxs-lookup"><span data-stu-id="ebeaf-113">For step-by-step upgrade instructions, see [How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md).</span></span>

    <span data-ttu-id="ebeaf-114">**Observação**  Se você tiver mais de um servidor que compartilha o acesso ao banco de dados do Application Virtualization, todos esses servidores deverão ser colocados offline enquanto o banco de dados estiver sendo atualizado.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-114">**Note** If you have more than one server sharing access to the Application Virtualization database, all those servers must be taken offline while the database is being upgraded.</span></span> <span data-ttu-id="ebeaf-115">Você deve seguir as práticas comerciais normais para a atualização do banco de dados, mas é altamente recomendável que você teste a atualização do banco de dados usando uma cópia de backup do banco de dados primeiro em um servidor de teste.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-115">You should follow your normal business practices for the database upgrade, but it is highly advisable that you test the database upgrade by using a backup copy of the database first on a test server.</span></span> <span data-ttu-id="ebeaf-116">Em seguida, você deve selecionar um dos servidores para a primeira atualização, o que fará a atualização do esquema de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-116">Then, you should select one of the servers for the first upgrade, which will upgrade the database schema.</span></span> <span data-ttu-id="ebeaf-117">Depois que o banco de dados de produção for atualizado com êxito, você poderá atualizar os outros servidores.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-117">After the production database has been successfully upgraded, you can upgrade the other servers.</span></span>

     

3.  **<span data-ttu-id="ebeaf-118">Serviço Web de gerenciamento do aplicativo Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-118">Microsoft Application Virtualization Management Web Service.</span></span>** <span data-ttu-id="ebeaf-119">Esta etapa se aplica apenas se o serviço Web de gerenciamento estiver em um servidor separado, o que exigirá que você execute o programa de instalação do servidor nesse servidor separado para atualizar o serviço Web.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-119">This step applies only if the Management Web Service is on a separate server, which would require that you run the server installer program on that separate server to upgrade the Web service.</span></span> <span data-ttu-id="ebeaf-120">Caso contrário, a etapa anterior de atualização do servidor atualizará automaticamente o serviço Web de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-120">Otherwise, the previous server upgrade step will automatically upgrade the Management Web Service.</span></span>

4.  **<span data-ttu-id="ebeaf-121">Console de gerenciamento do Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-121">Microsoft Application Virtualization Management Console.</span></span>** <span data-ttu-id="ebeaf-122">Esta etapa se aplica apenas se o console de gerenciamento estiver em um computador separado, o que exigirá que você execute o programa de instalação do servidor nesse computador separado para atualizar o console.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-122">This step applies only if the Management Console is on a separate computer, which would require that you run the server installer program on that separate computer to upgrade the console.</span></span> <span data-ttu-id="ebeaf-123">Caso contrário, a etapa anterior de atualização do servidor atualizará o console de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-123">Otherwise, the previous server upgrade step will upgrade the Management Console.</span></span>

5.  **<span data-ttu-id="ebeaf-124">Microsoft Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-124">Microsoft Application Virtualization Sequencer.</span></span>** <span data-ttu-id="ebeaf-125">Para obter instruções passo a passo, consulte [como instalar o Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md).</span><span class="sxs-lookup"><span data-stu-id="ebeaf-125">For step-by-step instructions, see [How to Install the Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md).</span></span> <span data-ttu-id="ebeaf-126">Qualquer pacote de aplicativos virtual sequenciado na versão 4.2 não precisará ser novamente sequenciado para uso com a versão 4.5.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-126">Any virtual application packages sequenced in version4.2 will not have to be re-sequenced for use with version4.5.</span></span> <span data-ttu-id="ebeaf-127">No entanto, você deve considerar a atualização dos pacotes virtuais para o formato do Microsoft Application Virtualization 4.5 se quiser aplicar ACLs (listas de controle de acesso) padrão ou gerar um arquivo do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-127">However, you should consider upgrading the virtual packages to the Microsoft Application Virtualization4.5 format if you would like to apply default access control lists (ACLs) or generate a Windows Installer file.</span></span> <span data-ttu-id="ebeaf-128">Isso é um processo simples e requer que o pacote de aplicativo virtual existente seja aberto e salvo com o 4,5 Sequencer.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-128">This is a simple process and requires only that the existing virtual application package be opened and saved with the4.5 Sequencer.</span></span> <span data-ttu-id="ebeaf-129">Isso pode ser automatizado usando a interface de linha de comando do sequenciador do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-129">This can be automated by using the Application Virtualization Sequencer command-line interface.</span></span>

## <a href="" id="app-v-4-6-client-package-support-"></a><span data-ttu-id="ebeaf-130">Suporte ao pacote do cliente do App-V 4.6</span><span class="sxs-lookup"><span data-stu-id="ebeaf-130">App-V4.6 Client Package Support</span></span>


<span data-ttu-id="ebeaf-131">Você pode implantar pacotes criados em versões anteriores do App-V para os clientes do App-V 4.6.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-131">You can deploy packages created in previous versions of App-V to App-V4.6 Clients.</span></span> <span data-ttu-id="ebeaf-132">No entanto, você deve modificar o arquivo **. OSD** associado para que ele inclua o sistema operacional apropriado e as informações sobre a arquitetura do chip.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-132">However, you must modify the associated **.osd** file so that it includes the appropriate operating system and chip architecture information.</span></span> <span data-ttu-id="ebeaf-133">Use os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-133">Use the following values.</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ebeaf-134">Valor do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="ebeaf-134">OS Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebeaf-135">&lt;VALOR do sistema operacional = "Win2003TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="ebeaf-135">&lt;OS VALUE=”Win2003TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ebeaf-136">&lt;VALOR do sistema operacional = "Win2003TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="ebeaf-136">&lt;OS VALUE=”Win2003TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebeaf-137">&lt;VALOR do sistema operacional = "Win2008TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="ebeaf-137">&lt;OS VALUE=”Win2008TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ebeaf-138">&lt;VALOR do sistema operacional = "Win2008TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="ebeaf-138">&lt;OS VALUE=”Win2008TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebeaf-139">&lt;VALOR do sistema operacional = "Win2008R2TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="ebeaf-139">&lt;OS VALUE=”Win2008R2TS64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ebeaf-140">&lt;VALOR do sistema operacional = "Win7"/&gt;</span><span class="sxs-lookup"><span data-stu-id="ebeaf-140">&lt;OS VALUE=”Win7”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebeaf-141">&lt;VALOR do sistema operacional = "Win764"/&gt;</span><span class="sxs-lookup"><span data-stu-id="ebeaf-141">&lt;OS VALUE=”Win764”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ebeaf-142">&lt;VALOR do sistema operacional = "WinVista"/&gt;</span><span class="sxs-lookup"><span data-stu-id="ebeaf-142">&lt;OS VALUE=”WinVista”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebeaf-143">&lt;VALOR do sistema operacional = "WinVista64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="ebeaf-143">&lt;OS VALUE=”WinVista64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ebeaf-144">&lt;VALOR do sistema operacional = "WinXP"/&gt;</span><span class="sxs-lookup"><span data-stu-id="ebeaf-144">&lt;OS VALUE=”WinXP”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebeaf-145">&lt;VALOR do sistema operacional = "WinXP64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="ebeaf-145">&lt;OS VALUE=”WinXP64”/&gt;</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ebeaf-146">Para executar um pacote de 32 bits recém-criado, você deve sequenciar o aplicativo em um computador executando um sistema operacional de 32 bits com o sequenciador App-V 4.6 instalado.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-146">To run a newly created 32-bit package, you must sequence the application on a computer running a 32-bit operating system with the App-V4.6 Sequencer installed.</span></span> <span data-ttu-id="ebeaf-147">Depois de sequenciar o aplicativo, no console do sequenciador, selecione a guia **implantação** e especifique o sistema operacional e a arquitetura de chip apropriados conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-147">After you have sequenced the application, in the Sequencer console, select the **Deployment** tab and then specify the appropriate operating system and chip architecture as required.</span></span>

<span data-ttu-id="ebeaf-148">**Importante**  Aplicativos sequenciados em um computador executando um sistema operacional de 64 bits devem ser implantados em computadores que executam um sistema operacional de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-148">**Important** Applications sequenced on a computer running a 64-bit operating system must be deployed to computers running a 64-bit operating system.</span></span> <span data-ttu-id="ebeaf-149">Novos pacotes de 32 bits criados usando o App-V 4.6 Sequencer não serão executados em computadores que executam o cliente App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-149">New 32-bit packages created by using the App-V4.6 Sequencer will not run on computers running the App-V 4.5 Client.</span></span>

 

<span data-ttu-id="ebeaf-150">Para executar novos pacotes de 64 bits no cliente App-V 4.6, você deve sequenciar o aplicativo em um computador executando o sequenciador do App-V 4.6 e que esteja executando um sistema operacional de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-150">To run new 64-bit packages on the App-V4.6 Client, you must sequence the application on a computer running the App-V4.6 Sequencer and that is running a 64-bit operating system.</span></span> <span data-ttu-id="ebeaf-151">Depois de sequenciar o aplicativo, no console do sequenciador, selecione a guia **implantação** e especifique o sistema operacional e a arquitetura de chip apropriados conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-151">After you have sequenced the application, in the Sequencer console, select the **Deployment** tab and then specify the appropriate operating system and chip architecture as required.</span></span>

<span data-ttu-id="ebeaf-152">A tabela a seguir lista quais versões do cliente executarão pacotes criados usando as várias versões do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-152">The following table lists which client versions will run packages created by using the various versions of the Sequencer.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="ebeaf-153">Sequenciado usando o sequenciador do App-V 4,2</span><span class="sxs-lookup"><span data-stu-id="ebeaf-153">Sequenced by using the App-V 4.2 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="ebeaf-154">Sequenciado usando o sequenciador do App-V 4,5</span><span class="sxs-lookup"><span data-stu-id="ebeaf-154">Sequenced by using the App-V 4.5 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="ebeaf-155">Sequenciado usando o sequenciador do App-V 4,6 de 32 bits</span><span class="sxs-lookup"><span data-stu-id="ebeaf-155">Sequenced by using the 32-bit App-V 4.6 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="ebeaf-156">Sequenciado usando o sequenciador do App-V 4,6 de 64 bits</span><span class="sxs-lookup"><span data-stu-id="ebeaf-156">Sequenced by using the 64-bit App-V 4.6 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="ebeaf-157">Sequenciado usando o sequenciador do App-V 4,6 SP1 do 32-bit App-V</span><span class="sxs-lookup"><span data-stu-id="ebeaf-157">Sequenced by using the 32-bit App-V 4.6 SP1 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="ebeaf-158">Sequenciado usando o sequenciador do App-V 4,6 SP1 do 64-bit App-V</span><span class="sxs-lookup"><span data-stu-id="ebeaf-158">Sequenced by using the 64-bit App-V 4.6 SP1 Sequencer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebeaf-159">cliente do 4,2</span><span class="sxs-lookup"><span data-stu-id="ebeaf-159">4.2 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-160">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-160">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-161">Não</span><span class="sxs-lookup"><span data-stu-id="ebeaf-161">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-162">Não</span><span class="sxs-lookup"><span data-stu-id="ebeaf-162">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-163">Não</span><span class="sxs-lookup"><span data-stu-id="ebeaf-163">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-164">Não</span><span class="sxs-lookup"><span data-stu-id="ebeaf-164">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-165">Não</span><span class="sxs-lookup"><span data-stu-id="ebeaf-165">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ebeaf-166">¹ Client 4,5</span><span class="sxs-lookup"><span data-stu-id="ebeaf-166">4.5 Client ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-167">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-167">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-168">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-168">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-169">Não</span><span class="sxs-lookup"><span data-stu-id="ebeaf-169">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-170">Não</span><span class="sxs-lookup"><span data-stu-id="ebeaf-170">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-171">Não</span><span class="sxs-lookup"><span data-stu-id="ebeaf-171">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-172">Não</span><span class="sxs-lookup"><span data-stu-id="ebeaf-172">No</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebeaf-173">cliente do 4,6 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="ebeaf-173">4.6 Client (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-174">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-174">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-175">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-175">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-176">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-176">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-177">Não</span><span class="sxs-lookup"><span data-stu-id="ebeaf-177">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-178">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-178">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-179">Não</span><span class="sxs-lookup"><span data-stu-id="ebeaf-179">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ebeaf-180">cliente do 4,6 (64 bits)</span><span class="sxs-lookup"><span data-stu-id="ebeaf-180">4.6 Client (64-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-181">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-181">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-182">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-182">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-183">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-183">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-184">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-184">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-185">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-185">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-186">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-186">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebeaf-187">Cliente do 4,6 SP1</span><span class="sxs-lookup"><span data-stu-id="ebeaf-187">4.6 SP1 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-188">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-188">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-189">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-189">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-190">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-190">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-191">Não</span><span class="sxs-lookup"><span data-stu-id="ebeaf-191">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-192">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-192">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-193">Não</span><span class="sxs-lookup"><span data-stu-id="ebeaf-193">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ebeaf-194">Cliente do 4,6 SP1 (64 bits)</span><span class="sxs-lookup"><span data-stu-id="ebeaf-194">4.6 SP1 Client (64-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-195">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-195">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-196">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-196">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-197">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-197">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-198">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-198">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-199">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-199">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebeaf-200">Sim</span><span class="sxs-lookup"><span data-stu-id="ebeaf-200">Yes</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ebeaf-201">¹ aplica-se a todas as versões do cliente App-V 4.5, incluindo App-V 4.5, App-V 4.5 CU1 e App-V 4.5 SP1.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-201">¹Applies to all versions of the App-V4.5 Client, including App-V4.5, App-V4.5CU1 and App-V4.5 SP1.</span></span>

## <span data-ttu-id="ebeaf-202">Considerações adicionais sobre a migração</span><span class="sxs-lookup"><span data-stu-id="ebeaf-202">Additional Migration Considerations</span></span>


<span data-ttu-id="ebeaf-203">Um dos recursos do sequenciador App-V 4.5 é a capacidade de criar arquivos do Windows Installer (. msi) como pontos de controle para interoperabilidade do pacote de aplicativos virtual com sistemas ESD (distribuição de software eletrônico), como o Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-203">One of the features of the App-V4.5 Sequencer is the ability to create Windows Installer files (.msi) as control points for virtual application package interoperability with electronic software distribution (ESD) systems such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="ebeaf-204">Os arquivos anteriores do Windows Installer criados com a ferramenta. msi para a virtualização de aplicativos que foram instalados em um cliente App-V 4.1 ou 4.2 que, em seguida, foi atualizado para o 4.5 continuam funcionando, embora não possam ser instalados no cliente 4.5.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-204">Previous Windows Installer files created with the .msi tool for Application Virtualization that were installed on a App-V4.1 or4.2 Client that is subsequently upgraded to4.5 continue to work, although they cannot be installed on the4.5 Client.</span></span> <span data-ttu-id="ebeaf-205">No entanto, eles não podem ser removidos ou atualizados, a menos que eles sejam atualizados no sequenciador de 4,5.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-205">However, they cannot be removed or upgraded unless they are upgraded in the4.5 Sequencer.</span></span> <span data-ttu-id="ebeaf-206">O pacote de aplicativo virtual anterior ao 4,5 precisaria ser aberto no sequenciador de 4,5 e salvo como um arquivo do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-206">The original pre-4.5 virtual application package would need to be opened in the4.5 Sequencer and then saved as a Windows Installer File.</span></span>

<span data-ttu-id="ebeaf-207">**Observação**  Se o cliente App-V 4.2 já tiver sido atualizado para o 4.5, é possível usar o script como solução alternativa para preservar os pacotes 4.2 em clientes 4.5 e permitir que eles sejam gerenciados.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-207">**Note** If the App-V4.2 Client has already been upgraded to4.5, it is possible to use script as a workaround to preserve the4.2 packages on4.5 clients and allow them to be managed.</span></span> <span data-ttu-id="ebeaf-208">Esse script deve copiar dois arquivos, msvcp71.dll e msvcr71.dll, para a pasta de instalação do App-V e definir os seguintes valores de chave do registro na chave do registro \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span><span class="sxs-lookup"><span data-stu-id="ebeaf-208">This script must copy two files, msvcp71.dll and msvcr71.dll, to the App-V installation folder and set the following registry key values under the registry key \[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span></span>

<span data-ttu-id="ebeaf-209">"ClientVersion" = "4.2.1.20"</span><span class="sxs-lookup"><span data-stu-id="ebeaf-209">"ClientVersion"="4.2.1.20"</span></span>

<span data-ttu-id="ebeaf-210">"GlobalDataDirectory" = "C:\\\\Documents e Settings\\\\All Users\\\\Documents\\\\" (um local gravável globalmente)</span><span class="sxs-lookup"><span data-stu-id="ebeaf-210">"GlobalDataDirectory"="C:\\\\Documents and Settings\\\\All Users\\\\Documents\\\\" (a globally writeable location)</span></span>

 

<span data-ttu-id="ebeaf-211">Os arquivos do Windows Installer gerados pela App-V 4,5 Sequencer exibem a mensagem de erro "Este pacote requer o cliente do Microsoft Application Virtualization 4,5 ou posterior" quando você tenta executá-los em um cliente do App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-211">Windows Installer files generated by the App-V 4.5 Sequencer display the error message "This package requires Microsoft Application Virtualization Client 4.5 or later" when you try to run them on an App-V 4.6 Client.</span></span> <span data-ttu-id="ebeaf-212">Abra o pacote antigo com o sequenciador do App-V 4,5 SP1 ou o sequenciador do App-V 4,6 e gere um novo. msi para o pacote.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-212">Open the old package with either the App-V 4.5 SP1 Sequencer or the App-V 4.6 Sequencer and generate a new .msi for the package.</span></span>

<span data-ttu-id="ebeaf-213">Quaisquer relatórios do 4.2 que foram criados e salvos serão substituídos quando o servidor for atualizado para o 4.5.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-213">Any4.2 reports that were created and saved will be overwritten when the server is upgraded to4.5.</span></span> <span data-ttu-id="ebeaf-214">Se precisar manter esses relatórios, você deve salvar uma cópia de backup do arquivo SftMMC. msc localizado na pasta do console de gerenciamento do SoftGrid no servidor e usar essa cópia para substituir o novo SftMMC. msc que é instalado durante a atualização.</span><span class="sxs-lookup"><span data-stu-id="ebeaf-214">If you need to keep these reports, you must save a backup copy of the SftMMC.msc file located in the SoftGrid Management Console folder on the server and use that copy to replace the new SftMMC.msc that is installed during the upgrade.</span></span>

<span data-ttu-id="ebeaf-215">Para obter informações adicionais sobre a atualização de versões anteriores, consulte [atualização para perguntas frequentes do Microsoft Application Virtualization 4,5](https://go.microsoft.com/fwlink/?LinkId=120358) ( https://go.microsoft.com/fwlink/?LinkId=120358) .</span><span class="sxs-lookup"><span data-stu-id="ebeaf-215">For additional information about upgrading from previous versions, see [Upgrading to Microsoft Application Virtualization 4.5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) (https://go.microsoft.com/fwlink/?LinkId=120358).</span></span>

## <span data-ttu-id="ebeaf-216">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ebeaf-216">Related topics</span></span>


[<span data-ttu-id="ebeaf-217">Planejamento da implantação do Application Virtualization System</span><span class="sxs-lookup"><span data-stu-id="ebeaf-217">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





