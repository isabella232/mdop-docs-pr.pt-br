---
title: Quais são as novidades no App-V 5.0
description: Quais são as novidades no App-V 5.0
author: dansimp
ms.assetid: 79ff6e02-e926-4803-87d8-248a6b28099d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dabe264f033bd5c9897f07d931f799a42e6b72e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796195"
---
# <span data-ttu-id="5e127-103">Quais são as novidades no App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="5e127-103">What's New in App-V 5.0</span></span>


<span data-ttu-id="5e127-104">Esta seção é para os usuários que já estão familiarizados com o App-V e querem saber o que mudou no App-V 5,0 se você ainda não estiver familiarizado com o App-V, deve começar por meio [de leitura de planejamento para o app-v 5,0](planning-for-app-v-50-rc.md).</span><span class="sxs-lookup"><span data-stu-id="5e127-104">This section is for users who are already familiar with App-V and want to know what has changed in App-V 5.0 If you are not already familiar with App-V, you should start by reading [Planning for App-V 5.0](planning-for-app-v-50-rc.md).</span></span>

## <span data-ttu-id="5e127-105">Alterações na funcionalidade padrão</span><span class="sxs-lookup"><span data-stu-id="5e127-105">Changes in Standard Functionality</span></span>


<span data-ttu-id="5e127-106">As seções a seguir contêm informações sobre as alterações na funcionalidade padrão do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="5e127-106">The following sections contain information about the changes in standard functionality for App-V 5.0.</span></span>

### <span data-ttu-id="5e127-107">Alterações em sistemas operacionais com suporte</span><span class="sxs-lookup"><span data-stu-id="5e127-107">Changes to Supported Operating Systems</span></span>

<span data-ttu-id="5e127-108">Para obter mais informações, consulte [configurações compatíveis do App-V 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="5e127-108">For more information, see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

## <span data-ttu-id="5e127-109">Alterações no sequenciador</span><span class="sxs-lookup"><span data-stu-id="5e127-109">Changes to the sequencer</span></span>


<span data-ttu-id="5e127-110">As seções a seguir contêm informações sobre as alterações no sequenciador do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="5e127-110">The following sections contain information about the changes in the App-V 5.0 sequencer.</span></span>

### <span data-ttu-id="5e127-111">Alteração específica no sequenciador</span><span class="sxs-lookup"><span data-stu-id="5e127-111">Specific change to the sequencer</span></span>

<span data-ttu-id="5e127-112">A tabela a seguir exibe informações sobre o que mudou com o sequenciador do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="5e127-112">The following table displays information about what has changed with the App-V 5.0 sequencer</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5e127-113">Recurso sequenciador</span><span class="sxs-lookup"><span data-stu-id="5e127-113">Sequencer Feature</span></span></th>
<th align="left"><span data-ttu-id="5e127-114">Funcionalidade do sequenciador do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="5e127-114">App-V 5.0 Sequencer Functionality</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5e127-115">Processamento de reinicialização</span><span class="sxs-lookup"><span data-stu-id="5e127-115">Reboot processing</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e127-116">Quando um aplicativo solicita uma reinicialização, você deve permitir que o aplicativo reinicie o computador que executa o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="5e127-116">When an application prompts for a restart, you should allow the application to restart the computer running the sequencer.</span></span> <span data-ttu-id="5e127-117">O computador executando o sequenciador será reiniciado e o sequenciador será retomado no modo de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="5e127-117">The computer running the sequencer will restart and the sequencer will resume in monitoring mode.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5e127-118">Especificando o diretório de aplicativos virtual</span><span class="sxs-lookup"><span data-stu-id="5e127-118">Specifying the virtual application directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e127-119">Diretório de aplicativos virtual é um parâmetro obrigatório.</span><span class="sxs-lookup"><span data-stu-id="5e127-119">Virtual Application Directory is a mandatory parameter.</span></span> <span data-ttu-id="5e127-120">Para obter os melhores resultados, ele deve corresponder ao diretório de instalação do instalador do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5e127-120">For best results, it should match the installation directory of the application installer.</span></span> <span data-ttu-id="5e127-121">Isso resulta em desempenho e compatibilidade de aplicativos mais ótimos.</span><span class="sxs-lookup"><span data-stu-id="5e127-121">This results in more optimal performance and application compatibility.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5e127-122">Editando atalhos/FTAs</span><span class="sxs-lookup"><span data-stu-id="5e127-122">Editing shortcuts/FTAs</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e127-123">A página atalhos/FTA está na <strong> </strong> página edição avançada após a conclusão do assistente de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="5e127-123">The Shortcuts/FTA page is on the <strong>Advanced</strong> editing page after the sequencing wizard has completed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5e127-124">Guia Histórico de Alterações</span><span class="sxs-lookup"><span data-stu-id="5e127-124">Change History Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e127-125">A guia alterar histórico foi removida para o App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="5e127-125">The Change History tab has been removed for App-V 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5e127-126">Guia OSD</span><span class="sxs-lookup"><span data-stu-id="5e127-126">OSD Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e127-127">A guia OSD foi removida para o App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="5e127-127">The OSD tab has been removed for App-V 5.0.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5e127-128">Guia Serviços virtuais</span><span class="sxs-lookup"><span data-stu-id="5e127-128">Virtual Services Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e127-129">A guia de serviços virtuais foi removida para o App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="5e127-129">The virtual services tab has been removed for App-V 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5e127-130">Guia arquivos/sistema de arquivos virtual</span><span class="sxs-lookup"><span data-stu-id="5e127-130">Files/Virtual File System Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e127-131">Essas guias são combinadas e permitem que você modifique arquivos de pacote.</span><span class="sxs-lookup"><span data-stu-id="5e127-131">These tabs are combined and allow you to modify package files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5e127-132">Guia Implantação</span><span class="sxs-lookup"><span data-stu-id="5e127-132">Deployment Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e127-133">Não há mais opções para configurar a URL do servidor nos pacotes.</span><span class="sxs-lookup"><span data-stu-id="5e127-133">There are no longer options to configure the server URL in the packages.</span></span> <span data-ttu-id="5e127-134">Você deve configurá-lo agora usando a configuração de implantação ou o servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="5e127-134">You should configure this now using deployment configuration, or the management server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5e127-135">Ferramenta conversor de pacote</span><span class="sxs-lookup"><span data-stu-id="5e127-135">Package Converter Tool</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e127-136">Agora você pode usar o PowerShell para converter os pacotes criados em versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="5e127-136">You can now use PowerShell to convert packages created in previous versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5e127-137">Complemento/middleware</span><span class="sxs-lookup"><span data-stu-id="5e127-137">Add-on/Middleware</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e127-138">Você pode expandir pacotes pai ao sequenciar um aplicativo complementar ou middleware.</span><span class="sxs-lookup"><span data-stu-id="5e127-138">You can expand parent packages when you are sequencing an Add-On or Middleware application.</span></span> <span data-ttu-id="5e127-139">Complementos e pacotes middleware devem ser conectados usando grupos de conexão no App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="5e127-139">Add-ons and Middleware packages must be connected using connection groups in App-V 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5e127-140">Saída de arquivos</span><span class="sxs-lookup"><span data-stu-id="5e127-140">Files output</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e127-141">Os arquivos a seguir são criados com o App-V 5,0, o Windows Installer (. msi),. AppV, a configuração de implantação, a configuração do usuário e o Report.XML.</span><span class="sxs-lookup"><span data-stu-id="5e127-141">The following files are created with App-V 5.0, Windows Installer (.msi), .appv, deployment configuration, user configuration, and the Report.XML.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5e127-142">Pacotes de compactação/descritores de segurança/MSI</span><span class="sxs-lookup"><span data-stu-id="5e127-142">Compression/Security descriptors/MSI packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e127-143">A compactação e a criação de um arquivo do Windows Installer (. msi) são automáticas para todos os pacotes, e você não pode mais substituir descritores de segurança.</span><span class="sxs-lookup"><span data-stu-id="5e127-143">Compression and the creation of a Windows Installer (.msi) file are automatic for all packages and you can no longer override security descriptors.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5e127-144">Ferramentas/opções</span><span class="sxs-lookup"><span data-stu-id="5e127-144">Tools / Options</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e127-145">A janela diagnóstico foi removida e várias outras configurações.</span><span class="sxs-lookup"><span data-stu-id="5e127-145">The Diagnostics window has been removed as well as several other settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5e127-146">Unidade de instalação</span><span class="sxs-lookup"><span data-stu-id="5e127-146">Installation Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e127-147">Uma unidade de instalação não é mais necessária quando você instala um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5e127-147">An installation drive is no longer required when you install an application.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5e127-148">Transmissão de OOS</span><span class="sxs-lookup"><span data-stu-id="5e127-148">OOS Streaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="5e127-149">Se nenhuma otimização de fluxo for executada, os pacotes serão transportados com falha quando forem solicitados por computadores que executam o cliente App-V 5,0 até que possam ser iniciados.</span><span class="sxs-lookup"><span data-stu-id="5e127-149">If no stream optimization is performed, packages are stream faulted when they are requested by computers running the App-V 5.0 client until they can launch.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5e127-150">P: &lt; /p&gt;</span><span class="sxs-lookup"><span data-stu-id="5e127-150">Q:&lt;/p&gt;</span></span></td>
<td align="left"><p><span data-ttu-id="5e127-151">O App-V 5,0 usa o sistema de arquivos nativo e não requer mais um Q:.</span><span class="sxs-lookup"><span data-stu-id="5e127-151">App-V 5.0 uses the native file system and no longer requires a Q:.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5e127-152">Detecção de erros de sequenciamento</span><span class="sxs-lookup"><span data-stu-id="5e127-152">Sequencing error detection</span></span>


<span data-ttu-id="5e127-153">O sequenciador do App-V 5,0 pode detectar problemas de sequenciamento comuns durante o sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="5e127-153">The App-V 5.0 sequencer can detect common sequencing issues during sequencing.</span></span> <span data-ttu-id="5e127-154">A página **relatório de instalação** no final do assistente de sequenciamento exibe as mensagens de diagnóstico categorizadas em **erros**, **avisos**e **informações** dependendo da gravidade do problema.</span><span class="sxs-lookup"><span data-stu-id="5e127-154">The **Installation Report** page at the end of the sequencing wizard displays diagnostic messages categorized into **Errors**, **Warnings**, and **Info** depending on the severity of the issue.</span></span>

<span data-ttu-id="5e127-155">Para exibir informações mais detalhadas sobre um evento, clique duas vezes no item que você deseja revisar no relatório.</span><span class="sxs-lookup"><span data-stu-id="5e127-155">To display more detailed information about an event, double-click the item you want to review in the report.</span></span> <span data-ttu-id="5e127-156">Os problemas de sequenciamento, bem como sugestões sobre como resolver os problemas são exibidos.</span><span class="sxs-lookup"><span data-stu-id="5e127-156">The sequencing issues, as well as suggestions about how to resolve the issues are displayed.</span></span> <span data-ttu-id="5e127-157">As informações do relatório de preparação do sistema e do relatório de instalação serão resumidas quando você terminar de criar um pacote.</span><span class="sxs-lookup"><span data-stu-id="5e127-157">Information from the system preparation report and the installation report are summarized when you have finished creating a package.</span></span> <span data-ttu-id="5e127-158">A lista a seguir mostra os tipos de problemas disponíveis no relatório:</span><span class="sxs-lookup"><span data-stu-id="5e127-158">The following list displays the types of issues available in the report:</span></span>

-   <span data-ttu-id="5e127-159">Arquivos excluídos.</span><span class="sxs-lookup"><span data-stu-id="5e127-159">Excluded files.</span></span>

-   <span data-ttu-id="5e127-160">Informações do driver.</span><span class="sxs-lookup"><span data-stu-id="5e127-160">Driver information.</span></span>

-   <span data-ttu-id="5e127-161">Diferenças do sistema COM+.</span><span class="sxs-lookup"><span data-stu-id="5e127-161">COM+ system differences.</span></span>

-   <span data-ttu-id="5e127-162">Conflitos lado a lado (SxS).</span><span class="sxs-lookup"><span data-stu-id="5e127-162">Side-by-side (SxS) conflicts.</span></span>

-   <span data-ttu-id="5e127-163">Extensões do Shell.</span><span class="sxs-lookup"><span data-stu-id="5e127-163">Shell Extensions.</span></span>

-   <span data-ttu-id="5e127-164">Informações sobre serviços sem suporte.</span><span class="sxs-lookup"><span data-stu-id="5e127-164">Information about unsupported services.</span></span>

-   <span data-ttu-id="5e127-165">Protocolo.</span><span class="sxs-lookup"><span data-stu-id="5e127-165">DCOM.</span></span>

## <span data-ttu-id="5e127-166">Grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="5e127-166">Connection Groups</span></span>


<span data-ttu-id="5e127-167">O recurso App-V anteriormente conhecido como **composição do pacote dinâmico** agora é conhecido como **grupos de conexão** no App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="5e127-167">The App-V feature formerly known as **Dynamic Suite Composition** is now referred to as **Connection Groups** in App-V 5.0.</span></span> <span data-ttu-id="5e127-168">Para obter mais informações sobre como usar grupos de conexão, consulte [Gerenciando grupos de conexão](managing-connection-groups.md).</span><span class="sxs-lookup"><span data-stu-id="5e127-168">For more information about using Connection Groups see [Managing Connection Groups](managing-connection-groups.md).</span></span>

## <span data-ttu-id="5e127-169">Funcionalidade de licenciamento e medição</span><span class="sxs-lookup"><span data-stu-id="5e127-169">Licensing and Metering Functionality</span></span>


<span data-ttu-id="5e127-170">A funcionalidade de aplicativo e licenciamento foi removida no App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="5e127-170">The application and licensing functionality has been removed in App-V 5.0.</span></span> <span data-ttu-id="5e127-171">As posições de licença reais em seu ambiente dependem da licença de título de software específica e dos direitos de uso concedidos pelos termos de licença associados.</span><span class="sxs-lookup"><span data-stu-id="5e127-171">The actual license positions in your environment depend on the specific software title license and usage rights granted by the associated license terms.</span></span>

## <span data-ttu-id="5e127-172">Cache de arquivos e aplicativos</span><span class="sxs-lookup"><span data-stu-id="5e127-172">File and Application Cache</span></span>


<span data-ttu-id="5e127-173">Não há arquivo ou cache de aplicativos disponível com o App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="5e127-173">There is no file or application cache available with App-V 5.0.</span></span>






## <span data-ttu-id="5e127-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5e127-174">Related topics</span></span>


[<span data-ttu-id="5e127-175">Sobre o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="5e127-175">About App-V 5.0</span></span>](about-app-v-50.md)

 

 





