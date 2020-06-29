---
title: Guia de desempenho do Application Virtualization 5.1
description: Guia de desempenho do Application Virtualization 5.1
author: dansimp
ms.assetid: 5f2643c7-5cf7-4a29-adb7-45bf9f5b0364
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3382a7958e12cc28b8101a6d5b7384a6975e6e82
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796270"
---
# <span data-ttu-id="14cb1-103">Guia de desempenho do Application Virtualization 5.1</span><span class="sxs-lookup"><span data-stu-id="14cb1-103">Performance Guidance for Application Virtualization 5.1</span></span>


<span data-ttu-id="14cb1-104">Saiba como configurar o App-V 5,1 para obter ótimo desempenho, otimizar pacotes de aplicativos virtuais e oferecer uma experiência de usuário melhor com o RDS e o VDI.</span><span class="sxs-lookup"><span data-stu-id="14cb1-104">Learn how to configure App-V 5.1 for optimal performance, optimize virtual app packages, and provide a better user experience with RDS and VDI.</span></span>

<span data-ttu-id="14cb1-105">A implementação de vários métodos pode ajudá-lo a melhorar a experiência do usuário final.</span><span class="sxs-lookup"><span data-stu-id="14cb1-105">Implementing multiple methods can help you improve the end-user experience.</span></span> <span data-ttu-id="14cb1-106">No entanto, seu ambiente pode não dar suporte a todos os métodos.</span><span class="sxs-lookup"><span data-stu-id="14cb1-106">However, your environment may not support all methods.</span></span>

<span data-ttu-id="14cb1-107">Você deve ler e compreender as informações a seguir antes de ler este documento.</span><span class="sxs-lookup"><span data-stu-id="14cb1-107">You should read and understand the following information before reading this document.</span></span>

-   [<span data-ttu-id="14cb1-108">Guia do administrador do Microsoft Application Virtualization 5,1</span><span class="sxs-lookup"><span data-stu-id="14cb1-108">Microsoft Application Virtualization 5.1 Administrator's Guide</span></span>](microsoft-application-virtualization-51-administrators-guide.md)

-   [<span data-ttu-id="14cb1-109">Publicação de aplicativos e interação do cliente do App-V 5 SP2</span><span class="sxs-lookup"><span data-stu-id="14cb1-109">App-V 5 SP2 Application Publishing and Client Interaction</span></span>](https://go.microsoft.com/fwlink/?LinkId=395206)

-   [<span data-ttu-id="14cb1-110">Guia de sequenciamento do Microsoft Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="14cb1-110">Microsoft Application Virtualization Sequencing Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=269953)

**<span data-ttu-id="14cb1-111">Observação</span><span class="sxs-lookup"><span data-stu-id="14cb1-111">Note</span></span>**  
<span data-ttu-id="14cb1-112">Alguns termos usados neste documento podem ter significados diferentes dependendo da fonte externa e do contexto.</span><span class="sxs-lookup"><span data-stu-id="14cb1-112">Some terms used in this document may have different meanings depending on external source and context.</span></span> <span data-ttu-id="14cb1-113">Para obter mais informações sobre os termos usados neste documento seguidos de um asterisco **\\** \*, consulte a seção [terminologia de orientação do desempenho do Application Virtualization](#bkmk-terms1) deste documento.</span><span class="sxs-lookup"><span data-stu-id="14cb1-113">For more information about terms used in this document followed by an asterisk **\\**\* review the [Application Virtualization Performance Guidance Terminology](#bkmk-terms1) section of this document.</span></span>



<span data-ttu-id="14cb1-114">Por fim, este documento fornecerá as informações para configurar o computador que está executando o cliente do App-V 5,1 e o ambiente para obter ótimo desempenho.</span><span class="sxs-lookup"><span data-stu-id="14cb1-114">Finally, this document will provide you with the information to configure the computer running App-V 5.1 client and the environment for optimal performance.</span></span> <span data-ttu-id="14cb1-115">Otimize seus pacotes de aplicativos virtuais para desempenho usando o sequenciador e saiba como usar a virtualização de experiência do usuário (UE-V) ou outras tecnologias de gerenciamento do ambiente do usuário para fornecer a melhor experiência do usuário com o App-V 5,1 nos serviços de área de trabalho remota (RDS) e infraestrutura de área de trabalho virtual (VDI) não persistente.</span><span class="sxs-lookup"><span data-stu-id="14cb1-115">Optimize your virtual application packages for performance using the sequencer, and to understand how to use User Experience Virtualization (UE-V) or other user environment management technologies to provide the optimal user experience with App-V 5.1 in both Remote Desktop Services (RDS) and non-persistent virtual desktop infrastructure (VDI).</span></span>

<span data-ttu-id="14cb1-116">Para ajudar a determinar quais informações são relevantes para o seu ambiente, examine a breve visão geral e a lista de verificação de aplicabilidade de cada seção.</span><span class="sxs-lookup"><span data-stu-id="14cb1-116">To help determine what information is relevant to your environment you should review each section’s brief overview and applicability checklist.</span></span>

## <a href="" id="---------app-v-5-1-in-stateful--non-persistent-deployments"></a> <span data-ttu-id="14cb1-117">App-V 5,1 em implantações de estado \ \* não persistentes</span><span class="sxs-lookup"><span data-stu-id="14cb1-117">App-V 5.1 in stateful\* non-persistent deployments</span></span>


<span data-ttu-id="14cb1-118">Esta seção fornece informações sobre uma abordagem que ajuda a garantir que um usuário terá acesso a todos os aplicativos virtuais em segundos após o logon.</span><span class="sxs-lookup"><span data-stu-id="14cb1-118">This section provides information about an approach that helps ensure a user will have access to all virtual applications within seconds after logging in.</span></span> <span data-ttu-id="14cb1-119">Isso é conseguido com o endereçamento exclusivo da atualização de publicação do App-V 5,1 de longa execução.</span><span class="sxs-lookup"><span data-stu-id="14cb1-119">This is achieved by uniquely addressing the often long-running App-V 5.1 publishing refresh.</span></span> <span data-ttu-id="14cb1-120">Como você descobrirá a base da abordagem, a atualização de publicação mais rápida é aquela que não precisa realmente fazer nada.</span><span class="sxs-lookup"><span data-stu-id="14cb1-120">As you will discover the basis of the approach, the fastest publishing refresh, is one that doesn’t have to actually do anything.</span></span> <span data-ttu-id="14cb1-121">Uma série de condições deve ser satisfeita e etapas seguidas para fornecer a melhor experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="14cb1-121">A number of conditions must be met and steps followed to provide the optimal user experience.</span></span>

<span data-ttu-id="14cb1-122">Use as informações na seção a seguir para obter mais informações:</span><span class="sxs-lookup"><span data-stu-id="14cb1-122">Use the information in the following section for more information:</span></span>

<span data-ttu-id="14cb1-123">[Cenários de uso](#bkmk-us) – conforme você revisa os dois cenários, lembre-se de que esses são os métodos extremos.</span><span class="sxs-lookup"><span data-stu-id="14cb1-123">[Usage Scenarios](#bkmk-us) - As you review the two scenarios, keep in mind that these are the approach extremes.</span></span> <span data-ttu-id="14cb1-124">Com base em seus requisitos de uso, você pode optar por aplicar essas etapas a um subconjunto de pacotes de aplicativos virtuais e/ou usuários.</span><span class="sxs-lookup"><span data-stu-id="14cb1-124">Based on your usage requirements, you may choose to apply these steps to a subset of users and/or virtual applications packages.</span></span>

-   <span data-ttu-id="14cb1-125">Otimizado para desempenho – para fornecer a experiência ideal, você pode esperar que a imagem base inclua alguns dos pacotes de aplicativo virtual do App-V.</span><span class="sxs-lookup"><span data-stu-id="14cb1-125">Optimized for Performance – To provide the optimal experience, you can expect the base image to include some of the App-V virtual application package.</span></span> <span data-ttu-id="14cb1-126">Esse e outros requisitos são discutidos.</span><span class="sxs-lookup"><span data-stu-id="14cb1-126">This and other requirements are discussed.</span></span>

-   <span data-ttu-id="14cb1-127">Otimizado para armazenamento – se você estiver preocupado com o impacto do armazenamento, seguir este cenário irá ajudá-lo a solucionar esses problemas.</span><span class="sxs-lookup"><span data-stu-id="14cb1-127">Optimized for Storage – If you are concerned with the storage impact, following this scenario will help address those concerns.</span></span>

[<span data-ttu-id="14cb1-128">Preparando seu ambiente</span><span class="sxs-lookup"><span data-stu-id="14cb1-128">Preparing your Environment</span></span>](#bkmk-pe)

-   <span data-ttu-id="14cb1-129">Etapas para preparar a imagem base – seja em um ambiente de VDI ou RDSH não persistente, apenas algumas etapas devem ser concluídas na imagem base para habilitar essa abordagem.</span><span class="sxs-lookup"><span data-stu-id="14cb1-129">Steps to Prepare the Base Image – Whether in a non-persistent VDI or RDSH environment, only a few steps must be completed in the base image to enable this approach.</span></span>

-   <span data-ttu-id="14cb1-130">Use o UE-V 2,1 como a solução de gerenciamento de perfil do usuário (UPM) para a abordagem do App-V – a base dessa abordagem é a capacidade de uma solução UEM de persistir o conteúdo de apenas alguns locais de registro e de arquivo.</span><span class="sxs-lookup"><span data-stu-id="14cb1-130">Use UE-V 2.1 as the User Profile Management (UPM) solution for the App-V approach – the cornerstone of this approach is the ability of a UEM solution to persist the contents of just a few registry and file locations.</span></span> <span data-ttu-id="14cb1-131">Esses locais constituem as integrações do usuário \ \*.</span><span class="sxs-lookup"><span data-stu-id="14cb1-131">These locations constitute the user integrations\*.</span></span> <span data-ttu-id="14cb1-132">Certifique-se de analisar os requisitos específicos para a solução UPM.</span><span class="sxs-lookup"><span data-stu-id="14cb1-132">Be sure to review the specific requirements for the UPM solution.</span></span>

[<span data-ttu-id="14cb1-133">Orientação de experiência do usuário</span><span class="sxs-lookup"><span data-stu-id="14cb1-133">User Experience Walk-through</span></span>](#bkmk-uewt)

-   <span data-ttu-id="14cb1-134">Acompanhamento-passo-a-passo é uma orientação passo a passo das operações do App-V e do UE-V e das expectativas que os usuários devem ter.</span><span class="sxs-lookup"><span data-stu-id="14cb1-134">Walk-through – This is a step-by-step walk-through of the App-V and UE-V operations and the expectations users should have.</span></span>

-   <span data-ttu-id="14cb1-135">Resultado – descreve os resultados esperados.</span><span class="sxs-lookup"><span data-stu-id="14cb1-135">Outcome – This describes the expected results.</span></span>

[<span data-ttu-id="14cb1-136">Impacto no ciclo de vida do pacote</span><span class="sxs-lookup"><span data-stu-id="14cb1-136">Impact to Package Lifecycle</span></span>](#bkmk-plc)

[<span data-ttu-id="14cb1-137">Aprimorar a experiência com VDI por meio da otimização/ajuste de desempenho</span><span class="sxs-lookup"><span data-stu-id="14cb1-137">Enhancing the VDI Experience through Performance Optimization/Tuning</span></span>](#bkmk-evdi)

### <a href="" id="applicability-checklist-"></a><span data-ttu-id="14cb1-138">Lista de verificação de aplicabilidade</span><span class="sxs-lookup"><span data-stu-id="14cb1-138">Applicability Checklist</span></span>

<span data-ttu-id="14cb1-139">Ambiente de implantação</span><span class="sxs-lookup"><span data-stu-id="14cb1-139">Deployment Environment</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="14cb1-140">VDI ou RDSH não persistentes.</span><span class="sxs-lookup"><span data-stu-id="14cb1-140">Non-Persistent VDI or RDSH.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="14cb1-141">User Experience Virtualization (UE-V), outras soluções UPM ou discos de perfil de usuário (UPD).</span><span class="sxs-lookup"><span data-stu-id="14cb1-141">User Experience Virtualization (UE-V), other UPM solutions or User Profile Disks (UPD).</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="14cb1-142">Configuração esperada</span><span class="sxs-lookup"><span data-stu-id="14cb1-142">Expected Configuration</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="14cb1-143">User Experience Virtualization (UE-V) com o modelo de estado de usuário do App-V habilitado ou o software de gerenciamento de perfil do usuário (UPM).</span><span class="sxs-lookup"><span data-stu-id="14cb1-143">User Experience Virtualization (UE-V) with the App-V user state template enabled or User Profile Management (UPM) software.</span></span> <span data-ttu-id="14cb1-144">O software UPM não-UE-V deve ser capaz de disparar no início e no logoff de logon ou processo/aplicativo.</span><span class="sxs-lookup"><span data-stu-id="14cb1-144">Non-UE-V UPM software must be capable of triggering on Login or Process/Application Start and Logoff.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="14cb1-145">O SCS (repositório de conteúdo compartilhado) do App-V está configurado ou pode ser configurado.</span><span class="sxs-lookup"><span data-stu-id="14cb1-145">App-V Shared Content Store (SCS) is configured or can be configured.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="14cb1-146">Administração de ti</span><span class="sxs-lookup"><span data-stu-id="14cb1-146">IT Administration</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="14cb1-147">O administrador pode precisar atualizar a imagem base da VM regularmente para garantir o desempenho ideal ou o administrador pode precisar gerenciar várias imagens para diferentes grupos de usuários.</span><span class="sxs-lookup"><span data-stu-id="14cb1-147">Admin may need to update the VM base image regularly to ensure optimal performance or Admin may need to manage multiple images for different user groups.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-us"></a><span data-ttu-id="14cb1-148">Cenário de uso</span><span class="sxs-lookup"><span data-stu-id="14cb1-148">Usage Scenario</span></span>

<span data-ttu-id="14cb1-149">Ao revisar os dois cenários, lembre-se de que esses métodos são extremos.</span><span class="sxs-lookup"><span data-stu-id="14cb1-149">As you review the two scenarios, keep in mind that these approach the extremes.</span></span> <span data-ttu-id="14cb1-150">Com base em seus requisitos de uso, você pode optar por aplicar essas etapas a um subconjunto de usuários, pacotes de aplicativos virtuais ou ambos.</span><span class="sxs-lookup"><span data-stu-id="14cb1-150">Based on your usage requirements, you may choose to apply these steps to a subset of users, virtual application packages, or both.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14cb1-151">Otimizado para desempenho</span><span class="sxs-lookup"><span data-stu-id="14cb1-151">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="14cb1-152">Otimizado para armazenamento</span><span class="sxs-lookup"><span data-stu-id="14cb1-152">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14cb1-153">Para fornecer a melhor experiência do usuário, essa abordagem aproveita os recursos de uma solução UPM e requer uma preparação adicional da imagem e pode causar uma sobrecarga adicional de gerenciamento de imagens.</span><span class="sxs-lookup"><span data-stu-id="14cb1-153">To provide the most optimal user experience, this approach leverages the capabilities of a UPM solution and requires additional image preparation and can incur some additional image management overhead.</span></span></p>
<p><span data-ttu-id="14cb1-154">A seguir está a descrição de vários aprimoramentos de desempenho em implantações não persistentes de estado.</span><span class="sxs-lookup"><span data-stu-id="14cb1-154">The following describes many performance improvements in stateful non-persistent deployments.</span></span> <span data-ttu-id="14cb1-155">Para obter mais informações, consulte as <strong> etapas de sequenciamento para otimizar pacotes para a publicação de desempenho </strong> e referência para <strong> o guia de sequenciamento do App-V </strong> na <strong> seção Consulte também deste documento </strong> .</span><span class="sxs-lookup"><span data-stu-id="14cb1-155">For more information, see the <strong>Sequencing Steps to Optimize Packages for Publishing Performance</strong> and reference to <strong>App-V Sequencing Guide</strong> in the <strong>See Also section of this document</strong>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="14cb1-156">As expectativas gerais do cenário anterior ainda se aplicam aqui.</span><span class="sxs-lookup"><span data-stu-id="14cb1-156">The general expectations of the previous scenario still apply here.</span></span> <span data-ttu-id="14cb1-157">No entanto, lembre-se de que as imagens da VM são geralmente armazenadas em arrays dispendiosos; uma ligeira alteração foi feita na abordagem.</span><span class="sxs-lookup"><span data-stu-id="14cb1-157">However, keep in mind that VM images are typically stored in very costly arrays; a slight alteration has been made to the approach.</span></span> <span data-ttu-id="14cb1-158">Não configure previamente pacotes de aplicativos virtuais direcionados pelo usuário na imagem base.</span><span class="sxs-lookup"><span data-stu-id="14cb1-158">Do not pre-configure user-targeted virtual application packages in the base image.</span></span></p>
<p><span data-ttu-id="14cb1-159">O impacto dessas alterações é detalhado na seção do guia de experiência do usuário deste documento.</span><span class="sxs-lookup"><span data-stu-id="14cb1-159">The impact of this alteration is detailed in the User Experience Walkthrough section of this document.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pe"></a><span data-ttu-id="14cb1-160">Preparando seu ambiente</span><span class="sxs-lookup"><span data-stu-id="14cb1-160">Preparing your Environment</span></span>

<span data-ttu-id="14cb1-161">A tabela a seguir mostra as etapas necessárias para preparar a imagem base e o UE-V ou outra solução UPM para a abordagem.</span><span class="sxs-lookup"><span data-stu-id="14cb1-161">The following table displays the required steps to prepare the base image and the UE-V or another UPM solution for the approach.</span></span>

**<span data-ttu-id="14cb1-162">Preparar a imagem base</span><span class="sxs-lookup"><span data-stu-id="14cb1-162">Prepare the Base Image</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14cb1-163">Otimizado para desempenho</span><span class="sxs-lookup"><span data-stu-id="14cb1-163">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="14cb1-164">Otimizado para armazenamento</span><span class="sxs-lookup"><span data-stu-id="14cb1-164">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="14cb1-165">Instale a versão do cliente do App-V 5,1 do cliente.</span><span class="sxs-lookup"><span data-stu-id="14cb1-165">Install the App-V 5.1 client version of the client.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-166">Instalar o UE-V e baixar o modelo de configurações do App-V da Galeria de modelos do UE-V, consulte as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="14cb1-166">Install UE-V and download the App-V Settings Template from the UE-V template Gallery, see the following steps.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-167">Configurar para o modo SCS (repositório de conteúdo compartilhado).</span><span class="sxs-lookup"><span data-stu-id="14cb1-167">Configure for Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="14cb1-168">Para obter mais informações, consulte <a href="how-to-install-the-app-v-51-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)"> como instalar o aplicativo App-V 5,1 para o modo de repositório de conteúdo compartilhado </a> .</span><span class="sxs-lookup"><span data-stu-id="14cb1-168">For more information see <a href="how-to-install-the-app-v-51-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)">How to Install the App-V 5.1 Client for Shared Content Store Mode</a>.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-169">Configurar preservar integrações de usuário na DWORD do registro de logon.</span><span class="sxs-lookup"><span data-stu-id="14cb1-169">Configure Preserve User Integrations on Login Registry DWORD.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-170">Pré-configure todos os pacotes de usuário e de destino global, por exemplo, <strong> Add-AppvClientPackage </strong> .</span><span class="sxs-lookup"><span data-stu-id="14cb1-170">Pre-configure all user- and global-targeted packages for example, <strong>Add-AppvClientPackage</strong>.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-171">Pré-configure todos os grupos de conexões direcionadas a usuário e global, por exemplo, <strong> Add-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="14cb1-171">Pre-configure all user- and global-targeted connection groups for example, <strong>Add-AppvClientConnectionGroup</strong>.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-172">Pré-publique todos os pacotes direcionados globalmente.</span><span class="sxs-lookup"><span data-stu-id="14cb1-172">Pre-publish all global-targeted packages.</span></span></p>
<p></p>
<p><span data-ttu-id="14cb1-173">Como alternativa</span><span class="sxs-lookup"><span data-stu-id="14cb1-173">Alternatively,</span></span></p>
<ul>
<li><p><span data-ttu-id="14cb1-174">Executar uma publicação/atualização global.</span><span class="sxs-lookup"><span data-stu-id="14cb1-174">Perform a global publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-175">Executar uma publicação/atualização de usuário.</span><span class="sxs-lookup"><span data-stu-id="14cb1-175">Perform a user publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-176">Cancele a publicação de todos os pacotes direcionados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="14cb1-176">Un-publish all user-targeted packages.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-177">Exclua as seguintes entradas de User-virtual File System (VFS).</span><span class="sxs-lookup"><span data-stu-id="14cb1-177">Delete the following user-Virtual File System (VFS) entries.</span></span></p></li>
</ul>
<p><code>AppData\Local\Microsoft\AppV\Client\VFS</code></p>
<p><code>AppData\Roaming\Microsoft\AppV\Client\VFS</code></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="14cb1-178">Instale a versão do cliente do App-V 5,1 do cliente.</span><span class="sxs-lookup"><span data-stu-id="14cb1-178">Install the App-V 5.1 client version of the client.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-179">Instalar o UE-V e baixar o modelo de configurações do App-V da Galeria de modelos do UE-V, consulte as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="14cb1-179">Install UE-V and download the App-V Settings Template from the UE-V template Gallery, see the following steps.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-180">Configurar para o modo SCS (repositório de conteúdo compartilhado).</span><span class="sxs-lookup"><span data-stu-id="14cb1-180">Configure for Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="14cb1-181">Para obter mais informações, consulte <a href="how-to-install-the-app-v-51-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)"> como instalar o aplicativo App-V 5,1 para o modo de repositório de conteúdo compartilhado </a> .</span><span class="sxs-lookup"><span data-stu-id="14cb1-181">For more information see <a href="how-to-install-the-app-v-51-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)">How to Install the App-V 5.1 Client for Shared Content Store Mode</a>.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-182">Configurar preservar integrações de usuário na DWORD do registro de logon.</span><span class="sxs-lookup"><span data-stu-id="14cb1-182">Configure Preserve User Integrations on Login Registry DWORD.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-183">Pré-configure todos os pacotes direcionados global por exemplo, <strong> Add-AppvClientPackage </strong> .</span><span class="sxs-lookup"><span data-stu-id="14cb1-183">Pre-configure all global-targeted packages for example, <strong>Add-AppvClientPackage</strong>.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-184">Pré-configure todos os grupos de conexão de direcionamento global, por exemplo, <strong> Add-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="14cb1-184">Pre-configure all global-targeted connection groups for example, <strong>Add-AppvClientConnectionGroup</strong>.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-185">Pré-publique todos os pacotes direcionados globalmente.</span><span class="sxs-lookup"><span data-stu-id="14cb1-185">Pre-publish all global-targeted packages.</span></span></p>
<p></p></li>
</ul></td>
</tr>
</tbody>
</table>



<span data-ttu-id="14cb1-186">**Configurações** -para configurações essenciais do cliente App-V e para obter um pouco mais de contexto e instruções, Confira as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="14cb1-186">**Configurations** - For critical App-V Client configurations and for a little more context and how-to, review the following information:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14cb1-187">Configuração</span><span class="sxs-lookup"><span data-stu-id="14cb1-187">Configuration Setting</span></span></th>
<th align="left"><span data-ttu-id="14cb1-188">O que isso faz?</span><span class="sxs-lookup"><span data-stu-id="14cb1-188">What does this do?</span></span></th>
<th align="left"><span data-ttu-id="14cb1-189">Como devo usá-lo?</span><span class="sxs-lookup"><span data-stu-id="14cb1-189">How should I use it?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14cb1-190">Modo SCS (Shared Content Store)</span><span class="sxs-lookup"><span data-stu-id="14cb1-190">Shared Content Store (SCS) Mode</span></span></p>
<ul>
<li><p><span data-ttu-id="14cb1-191">Configurável no PowerShell usando <strong> set-AppvClientConfiguration </strong> – <strong> SharedContentStoreMode </strong> ou</span><span class="sxs-lookup"><span data-stu-id="14cb1-191">Configurable in PowerShell using <strong>Set- AppvClientConfiguration</strong> –<strong>SharedContentStoreMode</strong>, or</span></span></p></li>
<li><p><span data-ttu-id="14cb1-192">Durante a instalação do cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="14cb1-192">During installation of the App-V client.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="14cb1-193">Ao executar o repositório de conteúdo compartilhado, somente os dados de publicação são mantidos no disco rígido; outros ativos de aplicativo virtual são mantidos na memória (RAM).</span><span class="sxs-lookup"><span data-stu-id="14cb1-193">When running the shared content store only publishing data is maintained on hard disk; other virtual application assets are maintained in memory (RAM).</span></span></p>
<p><span data-ttu-id="14cb1-194">Isso ajuda a conservar o armazenamento local e a minimizar a e/s de disco por segundo (IOPS).</span><span class="sxs-lookup"><span data-stu-id="14cb1-194">This helps to conserve local storage and minimize disk I/O per second (IOPS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="14cb1-195">Isso é recomendado quando conexões de baixa latência são disponibilizadas entre o ponto de extremidade do cliente App-V e o servidor de conteúdo do SCS, SAN.</span><span class="sxs-lookup"><span data-stu-id="14cb1-195">This is recommended when low-latency connections are available between the App-V Client endpoint and the SCS content server, SAN.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14cb1-196">PreserveUserIntegrationsOnLogin</span><span class="sxs-lookup"><span data-stu-id="14cb1-196">PreserveUserIntegrationsOnLogin</span></span></p>
<ul>
<li><p><span data-ttu-id="14cb1-197">Configurar no registro em <strong> HKEY_LOCAL_MACHINE </strong>  \  <strong> software </strong>  \  <strong> Microsoft </strong>  \  <strong> AppV </strong>  \  <strong> Client </strong>  \  <strong> Integration </strong> .</span><span class="sxs-lookup"><span data-stu-id="14cb1-197">Configure in the Registry under <strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>AppV</strong> \ <strong>Client</strong> \ <strong>Integration</strong>.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-198">Crie o valor DWORD <strong> PreserveUserIntegrationsOnLogin </strong> com um valor de <strong> 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="14cb1-198">Create the DWORD value <strong>PreserveUserIntegrationsOnLogin</strong> with a value of <strong>1</strong>.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-199">Reinicie o serviço App-V Client ou reinicie o computador que executa o cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="14cb1-199">Restart the App-V client service or restart the computer running the App-V Client.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="14cb1-200">Se você não tiver pré-configurado ( <strong> Add-AppvClientPackage </strong> ) um pacote específico e essa configuração não for definida, o cliente App-V desintegrará \* as integrações de usuário persistentes e, em seguida, se reintegrará \*.</span><span class="sxs-lookup"><span data-stu-id="14cb1-200">If you have not pre-configured (<strong>Add-AppvClientPackage</strong>) a specific package and this setting is not configured, the App-V Client will de-integrate\* the persisted user integrations, then re-integrate\*.</span></span></p>
<p><span data-ttu-id="14cb1-201">Para cada pacote que atenda às condições acima, o dobro do trabalho será realizado durante a publicação/atualização.</span><span class="sxs-lookup"><span data-stu-id="14cb1-201">For every package that meets the above conditions, effectively twice the work will be done during publishing/refresh.</span></span></p></td>
<td align="left"><p><span data-ttu-id="14cb1-202">Se você não planeja pré-configurar previamente cada pacote de usuário disponível na imagem base, use essa configuração.</span><span class="sxs-lookup"><span data-stu-id="14cb1-202">If you don’t plan to pre-configure every available user package in the base image, use this setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14cb1-203">MaxConcurrentPublishingRefresh</span><span class="sxs-lookup"><span data-stu-id="14cb1-203">MaxConcurrentPublishingRefresh</span></span></p>
<ul>
<li><p><span data-ttu-id="14cb1-204">Configurar no registro em <strong> HKEY_LOCAL_MACHINE </strong> &lt; forte &gt; software </strong>  \  <strong> publicação de </strong>  \  <strong> </strong> &lt; cliente forte do Microsoft AppV &gt; </strong>  \  <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="14cb1-204">Configure in the Registry under <strong>HKEY_LOCAL_MACHINE</strong> &lt;strong&gt;Software</strong> \ <strong>Microsoft</strong> \ <strong>AppV</strong> &lt;strong&gt;Client</strong> \ <strong>Publishing</strong>.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-205">Crie o valor DWORD <strong> MaxConcurrentPublishingrefresh </strong> com o número máximo de atualizações de publicação simultâneas desejadas.</span><span class="sxs-lookup"><span data-stu-id="14cb1-205">Create the DWORD value <strong>MaxConcurrentPublishingrefresh</strong> with the desired maximum number of concurrent publishing refreshes.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-206">O serviço e o computador do cliente App-V não precisam ser reiniciados.</span><span class="sxs-lookup"><span data-stu-id="14cb1-206">The App-V client service and computer do not need to be restarted.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="14cb1-207">Essa configuração determina o número de usuários que podem realizar uma atualização/sincronização de publicação ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="14cb1-207">This setting determines the number of users that can perform a publishing refresh/sync at the same time.</span></span> <span data-ttu-id="14cb1-208">A configuração padrão é sem limite.</span><span class="sxs-lookup"><span data-stu-id="14cb1-208">The default setting is no limit.</span></span></p></td>
<td align="left"><p><span data-ttu-id="14cb1-209">Limitar o número de atualizações de publicação simultâneas impede o uso excessivo da CPU que pode afetar o desempenho do computador.</span><span class="sxs-lookup"><span data-stu-id="14cb1-209">Limiting the number of concurrent publishing refreshes prevents excessive CPU usage that could impact computer performance.</span></span> <span data-ttu-id="14cb1-210">Esse limite é recomendado em um ambiente RDS, no qual vários usuários podem entrar no mesmo computador ao mesmo tempo e executar uma sincronização de atualização de publicação.</span><span class="sxs-lookup"><span data-stu-id="14cb1-210">This limit is recommended in an RDS environment, where multiple users can log in to the same computer at the same time and perform a publishing refresh sync.</span></span></p>
<p><span data-ttu-id="14cb1-211">Se o limite de atualização de publicação simultânea for atingido, o tempo necessário para publicar novos aplicativos e disponibilizá-los para os usuários finais após o login poderá demorar um período indeterminado.</span><span class="sxs-lookup"><span data-stu-id="14cb1-211">If the concurrent publishing refresh threshold is reached, the time required to publish new applications and make them available to end users after they log in could take an indeterminate amount of time.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="14cb1-212">Configurar o método de solução UE-V para App-V</span><span class="sxs-lookup"><span data-stu-id="14cb1-212">Configure UE-V solution for App-V Approach</span></span>

<span data-ttu-id="14cb1-213">Recomendamos usar o Microsoft User Experience Virtualization (UE-V) para capturar e centralizar as configurações do aplicativo e as configurações do sistema operacional do Windows para um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="14cb1-213">We recommend using Microsoft User Experience Virtualization (UE-V) to capture and centralize application settings and Windows operating system settings for a specific user.</span></span> <span data-ttu-id="14cb1-214">Essas configurações são aplicadas aos diferentes computadores que são acessados pelo usuário, incluindo computadores de mesa, laptops e sessões do Virtual Desktop Infrastructure (VDI).</span><span class="sxs-lookup"><span data-stu-id="14cb1-214">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span> <span data-ttu-id="14cb1-215">A UE-V é otimizada para cenários de RDS e VDI.</span><span class="sxs-lookup"><span data-stu-id="14cb1-215">UE-V is optimized for RDS and VDI scenarios.</span></span>

<span data-ttu-id="14cb1-216">Para obter mais informações, consulte [introdução ao User Experience Virtualization 2,0](https://technet.microsoft.com/library/dn458926.aspx)</span><span class="sxs-lookup"><span data-stu-id="14cb1-216">For more information see [Getting Started With User Experience Virtualization 2.0](https://technet.microsoft.com/library/dn458926.aspx)</span></span>

<span data-ttu-id="14cb1-217">Em essência, tudo o que é necessário é instalar o UE-V Client e baixar o modelo de configurações do aplicativo Microsoft autod App-V da [Galeria de modelos do Microsoft User Experience Virtualization (UE-v)](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33).</span><span class="sxs-lookup"><span data-stu-id="14cb1-217">In essence all that is required is to install the UE-V client and download the following Microsoft authored App-V settings template from the [Microsoft User Experience Virtualization (UE-V) template gallery](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33).</span></span> <span data-ttu-id="14cb1-218">Registre o modelo.</span><span class="sxs-lookup"><span data-stu-id="14cb1-218">Register the template.</span></span> <span data-ttu-id="14cb1-219">Para obter mais informações sobre os modelos do UE-V, consulte [o recurso específico do UE-v para adquirir e registrar o modelo](https://technet.microsoft.com/library/dn458926.aspx).</span><span class="sxs-lookup"><span data-stu-id="14cb1-219">For more information around UE-V templates see [The UE-V specific resource for acquiring and registering the template](https://technet.microsoft.com/library/dn458926.aspx).</span></span>

**<span data-ttu-id="14cb1-220">Observação</span><span class="sxs-lookup"><span data-stu-id="14cb1-220">Note</span></span>**  
<span data-ttu-id="14cb1-221">Sem realizar uma etapa de configuração adicional, a virtualização de ambiente de usuário da Microsoft (UE-V) não poderá sincronizar os atalhos do menu iniciar (arquivos. lnk) no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="14cb1-221">Without performing an additional configuration step, the Microsoft User Environment Virtualization (UE-V) will not be able to synchronize the Start menu shortcuts (.lnk files) on the target computer.</span></span> <span data-ttu-id="14cb1-222">O tipo de arquivo. lnk é excluído por padrão.</span><span class="sxs-lookup"><span data-stu-id="14cb1-222">The .lnk file type is excluded by default.</span></span>

<span data-ttu-id="14cb1-223">O UE-V só dará suporte à remoção do tipo de arquivo. lnk da lista de exclusão nos cenários de RDS e VDI, em que cada dispositivo de usuário terá o mesmo conjunto de aplicativos instalados no mesmo local e cada arquivo. lnk será válido para todos os dispositivos dos usuários.</span><span class="sxs-lookup"><span data-stu-id="14cb1-223">UE-V will only support removing the .lnk file type from the exclusion list in the RDS and VDI scenarios, where every user’s device will have the same set of applications installed to the same location and every .lnk file is valid for all the users’ devices.</span></span> <span data-ttu-id="14cb1-224">Por exemplo, o UE-V não oferece suporte aos dois cenários a seguir, porque o resultado da rede será que o atalho será válido em um, mas não em todos os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="14cb1-224">For example, UE-V would not currently support the following 2 scenarios, because the net result will be that the shortcut will be valid on one but not all devices.</span></span>

-   <span data-ttu-id="14cb1-225">Se um usuário tiver um aplicativo instalado em um dispositivo com arquivos. lnk habilitados e o mesmo aplicativo nativo instalado em outro dispositivo em uma raiz de instalação diferente com arquivos. lnk habilitados.</span><span class="sxs-lookup"><span data-stu-id="14cb1-225">If a user has an application installed on one device with .lnk files enabled and the same native application installed on another device to a different installation root with .lnk files enabled.</span></span>

-   <span data-ttu-id="14cb1-226">Se um usuário tiver um aplicativo instalado em um dispositivo, mas não outro com arquivos. lnk habilitados.</span><span class="sxs-lookup"><span data-stu-id="14cb1-226">If a user has an application installed on one device but not another with .lnk files enabled.</span></span>



**<span data-ttu-id="14cb1-227">Importante</span><span class="sxs-lookup"><span data-stu-id="14cb1-227">Important</span></span>**  
<span data-ttu-id="14cb1-228">Este tópico descreve como alterar o registro do Windows usando o editor do registro.</span><span class="sxs-lookup"><span data-stu-id="14cb1-228">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="14cb1-229">Se você alterar o registro do Windows incorretamente, poderá causar sérios problemas que talvez exijam a reinstalação do Windows.</span><span class="sxs-lookup"><span data-stu-id="14cb1-229">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="14cb1-230">Você deve fazer uma cópia de backup dos arquivos do registro (System. dat e User. dat) antes de alterar o registro.</span><span class="sxs-lookup"><span data-stu-id="14cb1-230">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="14cb1-231">A Microsoft não pode garantir que os problemas que podem ocorrer quando você alterar o registro possam ser resolvidos.</span><span class="sxs-lookup"><span data-stu-id="14cb1-231">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="14cb1-232">Altere o registro por sua conta e risco.</span><span class="sxs-lookup"><span data-stu-id="14cb1-232">Change the registry at your own risk.</span></span>



<span data-ttu-id="14cb1-233">Usando o editor de registro da Microsoft (regedit.exe), navegue até **HKEY \ _LOCAL \ _MACHINE**  \\  **software**  \\  **Microsoft**  \\  **UEV**  \\  **Agent**  \\  **Configuration**  \\  **ExcludedFileTypes** e remova **. lnk** dos tipos de arquivo excluídos.</span><span class="sxs-lookup"><span data-stu-id="14cb1-233">Using the Microsoft Registry Editor (regedit.exe), navigate to **HKEY\_LOCAL\_MACHINE** \\ **Software** \\ **Microsoft** \\ **UEV** \\ **Agent** \\ **Configuration** \\ **ExcludedFileTypes** and remove **.lnk** from the excluded file types.</span></span>

**<span data-ttu-id="14cb1-234">Configurar outra solução de gerenciamento de perfil do usuário (UPM) para a abordagem do App-V</span><span class="sxs-lookup"><span data-stu-id="14cb1-234">Configure other User Profile Management (UPM) solution for App-V Approach</span></span>**

<span data-ttu-id="14cb1-235">A expectativa em um ambiente stateful é que uma solução UPM é implementada e pode dar suporte à persistência de dados de usuário entre sessões e entre logons.</span><span class="sxs-lookup"><span data-stu-id="14cb1-235">The expectation in a stateful environment is that a UPM solution is implemented and can support persistence of user data across sessions and between logins.</span></span>

<span data-ttu-id="14cb1-236">Os requisitos para a solução UPM são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="14cb1-236">The requirements for the UPM solution are as follows.</span></span>

<span data-ttu-id="14cb1-237">Para habilitar uma experiência de logon otimizada, por exemplo, a abordagem App-V 5,1 para o usuário, a solução deve ser capaz de:</span><span class="sxs-lookup"><span data-stu-id="14cb1-237">To enable an optimized login experience, for example the App-V 5.1 approach for the user, the solution must be capable of:</span></span>

-   <span data-ttu-id="14cb1-238">Persistir as integrações de usuário abaixo, como parte do perfil do usuário/pessoa.</span><span class="sxs-lookup"><span data-stu-id="14cb1-238">Persisting the below user integrations as part of the user profile/persona.</span></span>

-   <span data-ttu-id="14cb1-239">Disparar uma sincronização de perfil de usuário no logon (ou início do aplicativo), que pode garantir que todas as integrações de usuário sejam aplicadas antes de iniciar a publicação/atualização ou,</span><span class="sxs-lookup"><span data-stu-id="14cb1-239">Triggering a user profile sync on login (or application start), which can guarantee that all user integrations are applied before publishing/refresh begin, or,</span></span>

-   <span data-ttu-id="14cb1-240">Anexar e desanexar um disco de perfil de usuário (UPD) ou uma tecnologia semelhante que contém as integrações do usuário.</span><span class="sxs-lookup"><span data-stu-id="14cb1-240">Attaching and detaching a user profile disk (UPD) or similar technology that contains the user integrations.</span></span>

    **<span data-ttu-id="14cb1-241">Observação</span><span class="sxs-lookup"><span data-stu-id="14cb1-241">Note</span></span>**  
    <span data-ttu-id="14cb1-242">O App-V tem suporte ao usar a UPD somente quando o perfil inteiro é armazenado no disco de perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="14cb1-242">App-V is supported when using UPD only when the entire profile is stored on the user profile disk.</span></span>

    <span data-ttu-id="14cb1-243">Não há suporte para pacotes do App-V ao usar a UPD com pastas selecionadas armazenadas no disco de perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="14cb1-243">App-V packages are not supported when using UPD with selected folders stored in the user profile disk.</span></span> <span data-ttu-id="14cb1-244">O driver copiar no write não manipula as pastas selecionadas UPD.</span><span class="sxs-lookup"><span data-stu-id="14cb1-244">The Copy on Write driver does not handle UPD selected folders.</span></span>



-   <span data-ttu-id="14cb1-245">Captura de alterações nos locais, que constituem as integrações do usuário antes do logoff da sessão.</span><span class="sxs-lookup"><span data-stu-id="14cb1-245">Capturing changes to the locations, which constitute the user integrations, prior to session logoff.</span></span>

<span data-ttu-id="14cb1-246">Com o App-V 5,1 ao adicionar um servidor de publicação (**Add-AppvPublishingServer**), você pode configurar a sincronização, por exemplo, atualizar durante o logon e/ou depois de um intervalo de atualização especificado.</span><span class="sxs-lookup"><span data-stu-id="14cb1-246">With App-V 5.1 when you add a publishing server (**Add-AppvPublishingServer**) you can configure synchronization, for example refresh during log on and/or after a specified refresh interval.</span></span> <span data-ttu-id="14cb1-247">Em ambos os casos, uma tarefa agendada é criada.</span><span class="sxs-lookup"><span data-stu-id="14cb1-247">In both cases a scheduled task is created.</span></span>

<span data-ttu-id="14cb1-248">Em versões anteriores do App-V 5,1, ambas as tarefas agendadas eram configuradas usando um VBScript que iniciaria o usuário e a atualização global.</span><span class="sxs-lookup"><span data-stu-id="14cb1-248">In previous versions of App-V 5.1, both scheduled tasks were configured using a VBScript that would initiate the user and global refresh.</span></span> <span data-ttu-id="14cb1-249">Com o pacote de hotfix 4 para Application Virtualization 5,0 SP2, a atualização do usuário durante o logon foi iniciada por **SyncAppvPublishingServer.exe**.</span><span class="sxs-lookup"><span data-stu-id="14cb1-249">With Hotfix Package 4 for Application Virtualization 5.0 SP2 the user refresh on log on was initiated by **SyncAppvPublishingServer.exe**.</span></span> <span data-ttu-id="14cb1-250">Essa alteração foi introduzida para fornecer um processo de gatilho às soluções do UPM.</span><span class="sxs-lookup"><span data-stu-id="14cb1-250">This change was introduced to provide UPM solutions a trigger process.</span></span> <span data-ttu-id="14cb1-251">Esse processo atrasa a publicação/Refresh para permitir que a solução UPM aplique as integrações do usuário.</span><span class="sxs-lookup"><span data-stu-id="14cb1-251">This process delays the publish /refresh to allow the UPM solution to apply the user integrations.</span></span> <span data-ttu-id="14cb1-252">Ele será encerrado quando a publicação/atualização for concluída.</span><span class="sxs-lookup"><span data-stu-id="14cb1-252">It will exit once the publishing/refresh is complete.</span></span>

**<span data-ttu-id="14cb1-253">Integrações do usuário</span><span class="sxs-lookup"><span data-stu-id="14cb1-253">User Integrations</span></span>**

<span data-ttu-id="14cb1-254">Registro – HKEY \ _CURRENT \ _USER</span><span class="sxs-lookup"><span data-stu-id="14cb1-254">Registry – HKEY\_CURRENT\_USER</span></span>

-   <span data-ttu-id="14cb1-255">Caminho-Software\\Classes</span><span class="sxs-lookup"><span data-stu-id="14cb1-255">Path - Software\\Classes</span></span>

    <span data-ttu-id="14cb1-256">Exclude: configurações locais, ActivatableClasses, AppX \ \*</span><span class="sxs-lookup"><span data-stu-id="14cb1-256">Exclude: Local Settings, ActivatableClasses, AppX\*</span></span>

-   <span data-ttu-id="14cb1-257">Caminho-Software\\Microsoft\\AppV</span><span class="sxs-lookup"><span data-stu-id="14cb1-257">Path - Software\\Microsoft\\AppV</span></span>

-   <span data-ttu-id="14cb1-258">Caminhos de caminho Software\\Microsoft\\Windows\\CurrentVersion\\App</span><span class="sxs-lookup"><span data-stu-id="14cb1-258">Path- Software\\Microsoft\\Windows\\CurrentVersion\\App Paths</span></span>

**<span data-ttu-id="14cb1-259">Locais de arquivos</span><span class="sxs-lookup"><span data-stu-id="14cb1-259">File Locations</span></span>**

-   <span data-ttu-id="14cb1-260">Root – "variável de ambiente" APPDATA</span><span class="sxs-lookup"><span data-stu-id="14cb1-260">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="14cb1-261">Caminho – Microsoft\\AppV\\Client\\Catalog</span><span class="sxs-lookup"><span data-stu-id="14cb1-261">Path – Microsoft\\AppV\\Client\\Catalog</span></span>

-   <span data-ttu-id="14cb1-262">Root – "variável de ambiente" APPDATA</span><span class="sxs-lookup"><span data-stu-id="14cb1-262">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="14cb1-263">Caminho – Microsoft\\AppV\\Client\\Integration</span><span class="sxs-lookup"><span data-stu-id="14cb1-263">Path – Microsoft\\AppV\\Client\\Integration</span></span>

-   <span data-ttu-id="14cb1-264">Root – "variável de ambiente" APPDATA</span><span class="sxs-lookup"><span data-stu-id="14cb1-264">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="14cb1-265">Path-Microsoft\\Windows\\Start Menu\\Programs</span><span class="sxs-lookup"><span data-stu-id="14cb1-265">Path - Microsoft\\Windows\\Start Menu\\Programs</span></span>

-   <span data-ttu-id="14cb1-266">(Para manter todos os atalhos da área de trabalho, virtuais e não virtuais)</span><span class="sxs-lookup"><span data-stu-id="14cb1-266">(To persist all desktop shortcuts, virtual and non-virtual)</span></span>

    <span data-ttu-id="14cb1-267">Root-"KnownFolder" {B4BFCC3A-DB2C-424C-B029-7FE99A87C641} filemask-\ \*. lnk</span><span class="sxs-lookup"><span data-stu-id="14cb1-267">Root - “KnownFolder” {B4BFCC3A-DB2C-424C-B029-7FE99A87C641}FileMask - \*.lnk</span></span>

**<span data-ttu-id="14cb1-268">Microsoft User Experience Virtualization (UE-V)</span><span class="sxs-lookup"><span data-stu-id="14cb1-268">Microsoft User Experience Virtualization (UE-V)</span></span>**

<span data-ttu-id="14cb1-269">Além disso, recomendamos usar o Microsoft User Experience Virtualization (UE-V) para capturar e centralizar as configurações do aplicativo e as configurações do sistema operacional do Windows para um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="14cb1-269">Additionally, we recommend using Microsoft User Experience Virtualization (UE-V) to capture and centralize application settings and Windows operating system settings for a specific user.</span></span> <span data-ttu-id="14cb1-270">Essas configurações são aplicadas aos diferentes computadores que são acessados pelo usuário, incluindo computadores de mesa, laptops e sessões do Virtual Desktop Infrastructure (VDI).</span><span class="sxs-lookup"><span data-stu-id="14cb1-270">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span>

<span data-ttu-id="14cb1-271">Para obter mais informações, consulte [introdução ao User Experience Virtualization 1,0](https://technet.microsoft.com/library/jj680015.aspx) e [compartilhamento de configurações modelos de local com a Galeria de modelos UE-V](https://technet.microsoft.com/library/jj679972.aspx).</span><span class="sxs-lookup"><span data-stu-id="14cb1-271">For more information see [Getting Started With User Experience Virtualization 1.0](https://technet.microsoft.com/library/jj680015.aspx) and [Sharing Settings Location Templates with the UE-V Template Gallery](https://technet.microsoft.com/library/jj679972.aspx).</span></span>

### <a href="" id="bkmk-uewt"></a><span data-ttu-id="14cb1-272">Orientação de experiência do usuário</span><span class="sxs-lookup"><span data-stu-id="14cb1-272">User Experience Walk-through</span></span>

<span data-ttu-id="14cb1-273">Veja a seguir uma orientação passo a passo sobre as operações do App-V e do UPM e as expectativas que os usuários devem esperar.</span><span class="sxs-lookup"><span data-stu-id="14cb1-273">This following is a step-by-step walk-through of the App-V and UPM operations and the expectations users should expect.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14cb1-274">Otimizado para desempenho</span><span class="sxs-lookup"><span data-stu-id="14cb1-274">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="14cb1-275">Otimizado para armazenamento</span><span class="sxs-lookup"><span data-stu-id="14cb1-275">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14cb1-276">Após implementar essa abordagem no ambiente VDI/RDSH, no primeiro logon,</span><span class="sxs-lookup"><span data-stu-id="14cb1-276">After implementing this approach in the VDI/RDSH environment, on first login,</span></span></p>
<ul>
<li><p><span data-ttu-id="14cb1-277">Opera Uma publicação/atualização do usuário é iniciada.</span><span class="sxs-lookup"><span data-stu-id="14cb1-277">(Operation) A user-publishing/refresh is initiated.</span></span> <span data-ttu-id="14cb1-278">Gestão Se esta for a primeira vez que um usuário publicou aplicativos virtuais (por exemplo, não persistente), isso vai pegar a duração normal de uma publicação/atualização.</span><span class="sxs-lookup"><span data-stu-id="14cb1-278">(Expectation) If this is the first time a user has published virtual applications (e.g. non-persistent), this will take the usual duration of a publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-279">Opera Após a publicação/atualização, a solução UPM captura as integrações do usuário.</span><span class="sxs-lookup"><span data-stu-id="14cb1-279">(Operation) After the publishing/refresh, the UPM solution captures the user integrations.</span></span> <span data-ttu-id="14cb1-280">Gestão Dependendo de como a solução UPM está configurada, isso pode ocorrer como parte do processo de logoff.</span><span class="sxs-lookup"><span data-stu-id="14cb1-280">(Expectation) Depending on how the UPM solution is configured, this may occur as part of the logoff process.</span></span> <span data-ttu-id="14cb1-281">Isso fará com que a sobrecarga e a sobrecarga semelhantes sejam mantidas no estado do usuário.</span><span class="sxs-lookup"><span data-stu-id="14cb1-281">This will incur the same/similar overhead as persisting the user state.</span></span></p></li>
</ul>
<p><span data-ttu-id="14cb1-282">Em logons subsequentes:</span><span class="sxs-lookup"><span data-stu-id="14cb1-282">On subsequent logins:</span></span></p>
<ul>
<li><p><span data-ttu-id="14cb1-283">Opera UPM solução aplica as integrações do usuário ao sistema antes de publicação/atualização.</span><span class="sxs-lookup"><span data-stu-id="14cb1-283">(Operation) UPM solution applies the user integrations to the system prior to publishing/refresh.</span></span></p>
<p><span data-ttu-id="14cb1-284">Gestão Haverá atalhos presentes na área de trabalho ou no menu Iniciar, que funcionam imediatamente.</span><span class="sxs-lookup"><span data-stu-id="14cb1-284">(Expectation) There will be shortcuts present on the desktop, or in the start menu, which work immediately.</span></span> <span data-ttu-id="14cb1-285">Quando a publicação/atualização é concluída (ou seja, as titularidades do pacote são alteradas), alguns podem ficar ausentes.</span><span class="sxs-lookup"><span data-stu-id="14cb1-285">When the publishing/refresh completes (i.e., package entitlements change), some may go away.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-286">Opera A publicação/atualização processará operações de cancelamento e publicação de alterações nos direitos do pacote do usuário.</span><span class="sxs-lookup"><span data-stu-id="14cb1-286">(Operation) Publishing/refresh will process un-publish and publish operations for changes in user package entitlements.</span></span> <span data-ttu-id="14cb1-287">Gestão Se não houver nenhuma alteração de direito, o publishing1 será concluído em segundos.</span><span class="sxs-lookup"><span data-stu-id="14cb1-287">(Expectation) If there are no entitlement changes, publishing1 will complete in seconds.</span></span> <span data-ttu-id="14cb1-288">Caso contrário, a publicação/atualização será aumentada em relação ao número e à complexidade \* dos aplicativos virtuais</span><span class="sxs-lookup"><span data-stu-id="14cb1-288">Otherwise, the publishing/refresh will increase relative to the number and complexity\* of virtual applications</span></span></p></li>
<li><p><span data-ttu-id="14cb1-289">Opera A solução UPM capturará as integrações do usuário novamente no logoff.</span><span class="sxs-lookup"><span data-stu-id="14cb1-289">(Operation) UPM solution will capture user integrations again at logoff.</span></span> <span data-ttu-id="14cb1-290">Gestão Mesmo que a seção anterior.</span><span class="sxs-lookup"><span data-stu-id="14cb1-290">(Expectation) Same as previous.</span></span></p></li>
</ul>
<p><span data-ttu-id="14cb1-291">¹ a operação de publicação ( <strong> publicar-AppVClientPackage </strong> ) adiciona entradas ao catálogo do usuário, mapeia a qualificação ao usuário, identifica o repositório local e termina ao completar qualquer etapa de integração.</span><span class="sxs-lookup"><span data-stu-id="14cb1-291">¹ The publishing operation (<strong>Publish-AppVClientPackage</strong>) adds entries to the user catalog, maps entitlement to the user, identifies the local store, and finishes by completing any integration steps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="14cb1-292">Após implementar essa abordagem no ambiente VDI/RDSH, no primeiro logon,</span><span class="sxs-lookup"><span data-stu-id="14cb1-292">After implementing this approach in the VDI/RDSH environment, on first login,</span></span></p>
<ul>
<li><p><span data-ttu-id="14cb1-293">Opera Uma publicação/atualização do usuário é iniciada.</span><span class="sxs-lookup"><span data-stu-id="14cb1-293">(Operation) A user-publishing/refresh is initiated.</span></span> <span data-ttu-id="14cb1-294">Gestão</span><span class="sxs-lookup"><span data-stu-id="14cb1-294">(Expectation)</span></span></p>
<ul>
<li><p><span data-ttu-id="14cb1-295">Se esta for a primeira vez que um usuário publicou aplicativos virtuais (por exemplo, não persistente), isso vai pegar a duração normal de uma publicação/atualização.</span><span class="sxs-lookup"><span data-stu-id="14cb1-295">If this is the first time a user has published virtual applications (e.g., non-persistent), this will take the usual duration of a publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-296">Os logins iniciais e subseqüentes serão afetados pela pré-configuração dos pacotes (adicionar/atualizar).</span><span class="sxs-lookup"><span data-stu-id="14cb1-296">First and subsequent logins will be impacted by pre-configuring of packages (add/refresh).</span></span></p>
<p></p></li>
</ul></li>
<li><p><span data-ttu-id="14cb1-297">Opera Após a publicação/atualização, a solução UPM captura as integrações do usuário.</span><span class="sxs-lookup"><span data-stu-id="14cb1-297">(Operation) After the publishing/refresh, the UPM solution captures the user integrations.</span></span> <span data-ttu-id="14cb1-298">Gestão Dependendo de como a solução UPM está configurada, isso pode ocorrer como parte do processo de logoff.</span><span class="sxs-lookup"><span data-stu-id="14cb1-298">(Expectation) Depending on how the UPM solution is configured, this may occur as part of the logoff process.</span></span> <span data-ttu-id="14cb1-299">Isso fará com que a sobrecarga e a sobrecarga semelhantes sejam mantidas no estado do usuário</span><span class="sxs-lookup"><span data-stu-id="14cb1-299">This will incur the same/similar overhead as persisting the user state</span></span></p></li>
</ul>
<p><span data-ttu-id="14cb1-300">Em logons subsequentes:</span><span class="sxs-lookup"><span data-stu-id="14cb1-300">On subsequent logins:</span></span></p>
<ul>
<li><p><span data-ttu-id="14cb1-301">Opera UPM solução aplica as integrações do usuário ao sistema antes de publicação/atualização.</span><span class="sxs-lookup"><span data-stu-id="14cb1-301">(Operation) UPM solution applies the user integrations to the system prior to publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-302">Opera Adicionar/atualizar deve pré-configurar todos os aplicativos direcionados ao usuário.</span><span class="sxs-lookup"><span data-stu-id="14cb1-302">(Operation) Add/refresh must pre-configure all user targeted applications.</span></span> <span data-ttu-id="14cb1-303">Gestão</span><span class="sxs-lookup"><span data-stu-id="14cb1-303">(Expectation)</span></span></p>
<ul>
<li><p><span data-ttu-id="14cb1-304">Isso pode aumentar o tempo para a disponibilidade do aplicativo significativamente (na ordem de 10 de segundos).</span><span class="sxs-lookup"><span data-stu-id="14cb1-304">This may increase the time to application availability significantly (on the order of 10’s of seconds).</span></span></p></li>
<li><p><span data-ttu-id="14cb1-305">Isso aumentará o tempo de atualização de publicação em relação ao número e à complexidade \* dos aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="14cb1-305">This will increase the publishing refresh time relative to the number and complexity\* of virtual applications.</span></span></p>
<p></p></li>
</ul></li>
<li><p><span data-ttu-id="14cb1-306">Opera A publicação/atualização processará operações de cancelamento e publicação para alterações nos direitos do pacote de usuários.</span><span class="sxs-lookup"><span data-stu-id="14cb1-306">(Operation) Publishing/refresh will process un-publish and publish operations for changes to user package entitlements.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14cb1-307">Resultado</span><span class="sxs-lookup"><span data-stu-id="14cb1-307">Outcome</span></span></th>
<th align="left"><span data-ttu-id="14cb1-308">Resultado</span><span class="sxs-lookup"><span data-stu-id="14cb1-308">Outcome</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="14cb1-309">Como as integrações do usuário são completamente preservadas, não haverá nenhum trabalho por exemplo, integração para a publicação/atualização a ser concluída.</span><span class="sxs-lookup"><span data-stu-id="14cb1-309">Because the user integrations are entirely preserved, there will be no work for example, integration for the publishing/refresh to complete.</span></span> <span data-ttu-id="14cb1-310">Todos os aplicativos virtuais estarão disponíveis em segundos de login.</span><span class="sxs-lookup"><span data-stu-id="14cb1-310">All virtual applications will be available within seconds of login.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-311">A publicação/atualização processará as alterações dos aplicativos virtuais intitulados aos usuários, que impactam a experiência.</span><span class="sxs-lookup"><span data-stu-id="14cb1-311">The publishing/refresh will process changes to the users entitled virtual applications which impacts the experience.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="14cb1-312">Como o Adicionar/atualizar deve reconfigurar todos os aplicativos virtuais para a VM, o tempo de atualização de publicação em todos os logins será estendido.</span><span class="sxs-lookup"><span data-stu-id="14cb1-312">Because the add/refresh must re-configure all the virtual applications to the VM, the publishing refresh time on every login will be extended.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-plc"></a><span data-ttu-id="14cb1-313">Impacto no ciclo de vida do pacote</span><span class="sxs-lookup"><span data-stu-id="14cb1-313">Impact to Package Life Cycle</span></span>

<span data-ttu-id="14cb1-314">Atualizar um pacote é um aspecto crucial do ciclo de vida do pacote.</span><span class="sxs-lookup"><span data-stu-id="14cb1-314">Upgrading a package is a crucial aspect of the package lifecycle.</span></span> <span data-ttu-id="14cb1-315">Para ajudar a garantir que os usuários tenham acesso aos pacotes de aplicativos virtuais atualizados (publicados) ou rebaixados (não publicados), é recomendável atualizar a imagem base para refletir essas alterações.</span><span class="sxs-lookup"><span data-stu-id="14cb1-315">To help guarantee users have access to the appropriate upgraded (published) or downgraded (un-published) virtual application packages, it is recommended you update the base image to reflect these changes.</span></span> <span data-ttu-id="14cb1-316">Para entender por que examine a seção a seguir:</span><span class="sxs-lookup"><span data-stu-id="14cb1-316">To understand why review the following section:</span></span>

<span data-ttu-id="14cb1-317">App-V 5,0 SP2 introduziu o conceito de Estados pendentes.</span><span class="sxs-lookup"><span data-stu-id="14cb1-317">App-V 5.0 SP2 introduced the concept of pending states.</span></span> <span data-ttu-id="14cb1-318">No passado,</span><span class="sxs-lookup"><span data-stu-id="14cb1-318">In the past,</span></span>

-   <span data-ttu-id="14cb1-319">Se um administrador tiver alterado direitos ou criado uma nova versão de um pacote (atualizado) e durante uma publicação/atualização que o pacote estava em uso, a operação de cancelamento ou publicação, respectivamente, falharia.</span><span class="sxs-lookup"><span data-stu-id="14cb1-319">If an administrator changed entitlements or created a new version of a package (upgraded) and during a publishing/refresh that package was in-use, the un-publish or publish operation, respectively, would fail.</span></span>

-   <span data-ttu-id="14cb1-320">Agora, se um pacote estiver em-uso, a operação será pendente.</span><span class="sxs-lookup"><span data-stu-id="14cb1-320">Now, if a package is in-use the operation will be pended.</span></span> <span data-ttu-id="14cb1-321">As operações de cancelamento de publicação e publicação pendente serão processadas na reinicialização do serviço, ou se outro comando de publicação ou cancelamento de publicação for emitido.</span><span class="sxs-lookup"><span data-stu-id="14cb1-321">The un-publish and publish-pend operations will be processed on service restart or if another publish or un-publish command is issued.</span></span> <span data-ttu-id="14cb1-322">Nesse caso, se o aplicativo virtual estiver sendo usado de outra forma, o aplicativo virtual permanecerá em um estado pendente.</span><span class="sxs-lookup"><span data-stu-id="14cb1-322">In the latter case, if the virtual application is in-use otherwise, the virtual application will remain in a pending state.</span></span> <span data-ttu-id="14cb1-323">Para pacotes publicados globalmente, uma reinicialização (ou reinicialização do serviço) geralmente necessária.</span><span class="sxs-lookup"><span data-stu-id="14cb1-323">For globally published packages, a restart (or service restart) often needed.</span></span>

<span data-ttu-id="14cb1-324">Em um ambiente não persistente, é improvável que estas operações pendentes sejam processadas.</span><span class="sxs-lookup"><span data-stu-id="14cb1-324">In a non-persistent environment, it is unlikely these pended operations will be processed.</span></span> <span data-ttu-id="14cb1-325">As operações pendentes, por exemplo, as tarefas são capturadas em **HKEY \ _CURRENT \ _USER**  \\  **software**  \\  **Microsoft**  \\  **AppV**  \\  **Client**  \\  **PendingTasks**.</span><span class="sxs-lookup"><span data-stu-id="14cb1-325">The pended operations, for example tasks are captured under **HKEY\_CURRENT\_USER** \\ **Software** \\ **Microsoft** \\ **AppV** \\ **Client** \\ **PendingTasks**.</span></span> <span data-ttu-id="14cb1-326">Embora esse local seja mantido pela solução UPM, se não for aplicado ao ambiente antes do logon, ele não será processado.</span><span class="sxs-lookup"><span data-stu-id="14cb1-326">Although this location is persisted by the UPM solution, if it is not applied to the environment prior to log on, it will not be processed.</span></span>

### <a href="" id="bkmk-evdi"></a><span data-ttu-id="14cb1-327">Aprimorar a experiência com VDI por meio do ajuste de otimização de desempenho</span><span class="sxs-lookup"><span data-stu-id="14cb1-327">Enhancing the VDI Experience through Performance Optimization Tuning</span></span>

<span data-ttu-id="14cb1-328">A seção a seguir contém listas com informações sobre documentação e downloads da Microsoft que podem ser úteis ao otimizar seu ambiente para desempenho.</span><span class="sxs-lookup"><span data-stu-id="14cb1-328">The following section contains lists with information about Microsoft documentation and downloads that may be useful when optimizing your environment for performance.</span></span>

**<span data-ttu-id="14cb1-329">Blog e script do .NET NGEN (altamente recomendado)</span><span class="sxs-lookup"><span data-stu-id="14cb1-329">.NET NGEN Blog and Script (Highly Recommended)</span></span>**

<span data-ttu-id="14cb1-330">Sobre a tecnologia NGEN</span><span class="sxs-lookup"><span data-stu-id="14cb1-330">About NGEN technology</span></span>

-   [<span data-ttu-id="14cb1-331">Como acelerar a otimização do NGEN</span><span class="sxs-lookup"><span data-stu-id="14cb1-331">How to speed up NGEN optimization</span></span>](https://blogs.msdn.com/b/dotnet/archive/2013/08/06/wondering-why-mscorsvw-exe-has-high-cpu-usage-you-can-speed-it-up.aspx)

-   [<span data-ttu-id="14cb1-332">Script</span><span class="sxs-lookup"><span data-stu-id="14cb1-332">Script</span></span>](https://aka.ms/DrainNGenQueue)

**<span data-ttu-id="14cb1-333">Funções do servidor e do servidor do Windows</span><span class="sxs-lookup"><span data-stu-id="14cb1-333">Windows Server and Server Roles</span></span>**

<span data-ttu-id="14cb1-334">Diretrizes de ajuste de desempenho do servidor para</span><span class="sxs-lookup"><span data-stu-id="14cb1-334">Server Performance Tuning Guidelines for</span></span>

-   [<span data-ttu-id="14cb1-335">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="14cb1-335">Microsoft Windows Server 2012 R2</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn529133.aspx)

-   [<span data-ttu-id="14cb1-336">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14cb1-336">Microsoft Windows Server 2012</span></span>](https://download.microsoft.com/download/0/0/B/00BE76AF-D340-4759-8ECD-C80BC53B6231/performance-tuning-guidelines-windows-server-2012.docx)

-   [<span data-ttu-id="14cb1-337">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="14cb1-337">Microsoft Windows Server 2008 R2</span></span>](https://download.microsoft.com/download/6/B/2/6B2EBD3A-302E-4553-AC00-9885BBF31E21/Perf-tun-srv-R2.docx)

**<span data-ttu-id="14cb1-338">Funções de servidor</span><span class="sxs-lookup"><span data-stu-id="14cb1-338">Server Roles</span></span>**

-   [<span data-ttu-id="14cb1-339">Host de virtualização de área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="14cb1-339">Remote Desktop Virtualization Host</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567643.aspx)

-   [<span data-ttu-id="14cb1-340">Host da sessão da área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="14cb1-340">Remote Desktop Session Host</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567648.aspx)

-   [<span data-ttu-id="14cb1-341">Relevância do IIS: gerenciamento de App-V, publicação, serviços Web de relatório</span><span class="sxs-lookup"><span data-stu-id="14cb1-341">IIS Relevance: App-V Management, Publishing, Reporting Web Services</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567678.aspx)

-   [<span data-ttu-id="14cb1-342">Relevância de servidor de arquivos (SMB): se usado para armazenamento e entrega de conteúdo do App-V no modo SCS</span><span class="sxs-lookup"><span data-stu-id="14cb1-342">File Server (SMB) Relevance: If used for App-V Content Storage and Delivery in SCS Mode</span></span>](https://technet.microsoft.com/library/jj134210.aspx)

**<span data-ttu-id="14cb1-343">Orientação de ajuste de desempenho do cliente Windows (SO convidado)</span><span class="sxs-lookup"><span data-stu-id="14cb1-343">Windows Client (Guest OS) Performance Tuning Guidance</span></span>**

-   [<span data-ttu-id="14cb1-344">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="14cb1-344">Microsoft Windows 7</span></span>](https://download.microsoft.com/download/E/5/7/E5783D68-160B-4366-8387-114FC3E45EB4/Performance Tuning Guidelines for Windows 7 Desktop Virtualization v1.9.docx)

-   [<span data-ttu-id="14cb1-345">Script de otimização: (fornecido pelo suporte da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="14cb1-345">Optimization Script: (Provided by Microsoft Support)</span></span>](https://blogs.technet.com/b/jeff_stokes/archive/2012/10/15/the-microsoft-premier-field-engineer-pfe-view-on-virtual-desktop-vdi-density.aspx)

-   [<span data-ttu-id="14cb1-346">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="14cb1-346">Microsoft Windows 8</span></span>](https://download.microsoft.com/download/6/0/1/601D7797-A063-4FA7-A2E5-74519B57C2B4/Windows_8_VDI_Image_Client_Tuning_Guide.pdf)

-   [<span data-ttu-id="14cb1-347">Script de otimização: (fornecido pelo suporte da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="14cb1-347">Optimization Script: (Provided by Microsoft Support)</span></span>](https://blogs.technet.com/b/jeff_stokes/archive/2013/04/09/hot-off-the-presses-get-it-now-the-windows-8-vdi-optimization-script-courtesy-of-pfe.aspx)

## <span data-ttu-id="14cb1-348">Etapas de sequenciamento para otimizar pacotes para o desempenho de publicação</span><span class="sxs-lookup"><span data-stu-id="14cb1-348">Sequencing Steps to Optimize Packages for Publishing Performance</span></span>


<span data-ttu-id="14cb1-349">Vários recursos do App-V facilitam novos cenários ou permitem novos cenários de implantação de cliente.</span><span class="sxs-lookup"><span data-stu-id="14cb1-349">Several App-V features facilitate new scenarios or enable new customer deployment scenarios.</span></span> <span data-ttu-id="14cb1-350">Esses recursos seguintes podem afetar o desempenho das operações de publicação e inicialização.</span><span class="sxs-lookup"><span data-stu-id="14cb1-350">These following features can impact the performance of the publishing and launch operations.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14cb1-351">Etapa</span><span class="sxs-lookup"><span data-stu-id="14cb1-351">Step</span></span></th>
<th align="left"><span data-ttu-id="14cb1-352">Consideração</span><span class="sxs-lookup"><span data-stu-id="14cb1-352">Consideration</span></span></th>
<th align="left"><span data-ttu-id="14cb1-353">Benefícios</span><span class="sxs-lookup"><span data-stu-id="14cb1-353">Benefits</span></span></th>
<th align="left"><span data-ttu-id="14cb1-354">Compensações</span><span class="sxs-lookup"><span data-stu-id="14cb1-354">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14cb1-355">Nenhum bloco de recursos 1 (FB1, também conhecido como principal FB)</span><span class="sxs-lookup"><span data-stu-id="14cb1-355">No Feature Block 1 (FB1, also known as Primary FB)</span></span></p></td>
<td align="left"><p><span data-ttu-id="14cb1-356">Nenhuma FB1 significa que o aplicativo será iniciado imediatamente e a falha de fluxo (o aplicativo exige arquivo, DLL e deve ser puxado pela rede) durante a inicialização. Se houver limitações de rede, o FB1 irá:</span><span class="sxs-lookup"><span data-stu-id="14cb1-356">No FB1 means the application will launch immediately and stream fault (application requires file, DLL and must pull down over the network) during launch.If there are network limitations, FB1 will:</span></span></p>
<ul>
<li><p><span data-ttu-id="14cb1-357">Reduza o número de falhas de fluxo e largura de banda de rede usada quando você inicia um aplicativo pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="14cb1-357">Reduce the number of stream faults and network bandwidth used when you launch an application for the first time.</span></span></p></li>
<li><p><span data-ttu-id="14cb1-358">Atrasar o lançamento até que todo o FB1 tenha sido transmitido.</span><span class="sxs-lookup"><span data-stu-id="14cb1-358">Delay launch until the entire FB1 has been streamed.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="14cb1-359">A falha do fluxo diminui o tempo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="14cb1-359">Stream faulting decreases the launch time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="14cb1-360">Os pacotes de aplicativos virtuais com o FB1 configurado precisarão ser novamente sequenciados.</span><span class="sxs-lookup"><span data-stu-id="14cb1-360">Virtual application packages with FB1 configured will need to be re-sequenced.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="14cb1-361">Removendo FB1</span><span class="sxs-lookup"><span data-stu-id="14cb1-361">Removing FB1</span></span>

<span data-ttu-id="14cb1-362">Remover o FB1 não exige o instalador do aplicativo original.</span><span class="sxs-lookup"><span data-stu-id="14cb1-362">Removing FB1 does not require the original application installer.</span></span> <span data-ttu-id="14cb1-363">Depois de concluir as etapas a seguir, é recomendável que você reverta o computador que executa o sequenciador para um instantâneo limpo.</span><span class="sxs-lookup"><span data-stu-id="14cb1-363">After completing the following steps, it is suggested that you revert the computer running the sequencer to a clean snapshot.</span></span>

<span data-ttu-id="14cb1-364">**Interface do usuário do sequenciador** -crie um novo pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="14cb1-364">**Sequencer UI** - Create a New Virtual Application Package.</span></span>

1.  <span data-ttu-id="14cb1-365">Conclua as etapas de sequenciamento para personalizar- &gt; streaming.</span><span class="sxs-lookup"><span data-stu-id="14cb1-365">Complete the sequencing steps up to Customize -&gt; Streaming.</span></span>

2.  <span data-ttu-id="14cb1-366">Na etapa de streaming, não selecione **otimizar o pacote para implantação em redes lentas ou não confiáveis**.</span><span class="sxs-lookup"><span data-stu-id="14cb1-366">At the Streaming step, do not select **Optimize the package for deployment over slow or unreliable network**.</span></span>

3.  <span data-ttu-id="14cb1-367">Se desejar, vá para o **sistema operacional de destino**.</span><span class="sxs-lookup"><span data-stu-id="14cb1-367">If desired, move on to **Target OS**.</span></span>

**<span data-ttu-id="14cb1-368">Modificar um pacote de aplicativo virtual existente</span><span class="sxs-lookup"><span data-stu-id="14cb1-368">Modify an Existing Virtual Application Package</span></span>**

1.  <span data-ttu-id="14cb1-369">Conclua as etapas de sequenciamento para transmitir.</span><span class="sxs-lookup"><span data-stu-id="14cb1-369">Complete the sequencing steps up to Streaming.</span></span>

2.  <span data-ttu-id="14cb1-370">Não selecione **otimizar o pacote para implantação em uma rede lenta ou não confiável**.</span><span class="sxs-lookup"><span data-stu-id="14cb1-370">Do not select **Optimize the package for deployment over a slow or unreliable network**.</span></span>

3.  <span data-ttu-id="14cb1-371">Mover para **criar pacote**.</span><span class="sxs-lookup"><span data-stu-id="14cb1-371">Move to **Create Package**.</span></span>

<span data-ttu-id="14cb1-372">**PowerShell** -atualize um pacote de aplicativo virtual existente.</span><span class="sxs-lookup"><span data-stu-id="14cb1-372">**PowerShell** - Update an Existing Virtual Application Package.</span></span>

1.  <span data-ttu-id="14cb1-373">Abra uma sessão do PowerShell com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="14cb1-373">Open an elevated PowerShell session.</span></span>

2.  <span data-ttu-id="14cb1-374">Import-Module **appvsequencer**.</span><span class="sxs-lookup"><span data-stu-id="14cb1-374">Import-module **appvsequencer**.</span></span>

3.  <span data-ttu-id="14cb1-375">**Update-AppvSequencerPackage**  -  **AppvPackageFilePath**</span><span class="sxs-lookup"><span data-stu-id="14cb1-375">**Update-AppvSequencerPackage** - **AppvPackageFilePath**</span></span>

    <span data-ttu-id="14cb1-376">"C:\\Packages\\MyPackage.appv"-instalador</span><span class="sxs-lookup"><span data-stu-id="14cb1-376">"C:\\Packages\\MyPackage.appv" -Installer</span></span>

    <span data-ttu-id="14cb1-377">"C:\\PackageInstall\\PackageUpgrade.exe empty.exe"-OutputPath</span><span class="sxs-lookup"><span data-stu-id="14cb1-377">"C:\\PackageInstall\\PackageUpgrade.exe empty.exe" -OutputPath</span></span>

    <span data-ttu-id="14cb1-378">"C:\\UpgradedPackages"</span><span class="sxs-lookup"><span data-stu-id="14cb1-378">"C:\\UpgradedPackages"</span></span>

    **<span data-ttu-id="14cb1-379">Observação</span><span class="sxs-lookup"><span data-stu-id="14cb1-379">Note</span></span>**  
    <span data-ttu-id="14cb1-380">Esse cmdlet requer um arquivo executável (. exe) ou um arquivo em lotes (. bat).</span><span class="sxs-lookup"><span data-stu-id="14cb1-380">This cmdlet requires an executable (.exe) or batch file (.bat).</span></span> <span data-ttu-id="14cb1-381">Você deve fornecer um arquivo executável ou arquivo em lotes vazio (não há nada).</span><span class="sxs-lookup"><span data-stu-id="14cb1-381">You must provide an empty (does nothing) executable or batch file.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14cb1-382">Etapa</span><span class="sxs-lookup"><span data-stu-id="14cb1-382">Step</span></span></th>
<th align="left"><span data-ttu-id="14cb1-383">Conhecer</span><span class="sxs-lookup"><span data-stu-id="14cb1-383">Considerations</span></span></th>
<th align="left"><span data-ttu-id="14cb1-384">Benefícios</span><span class="sxs-lookup"><span data-stu-id="14cb1-384">Benefits</span></span></th>
<th align="left"><span data-ttu-id="14cb1-385">Compensações</span><span class="sxs-lookup"><span data-stu-id="14cb1-385">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14cb1-386">Nenhuma instalação do SXS na publicação (pré-instalação assemblies SxS)</span><span class="sxs-lookup"><span data-stu-id="14cb1-386">No SXS Install at Publish (Pre-Install SxS assemblies)</span></span></p></td>
<td align="left"><p><span data-ttu-id="14cb1-387">Os pacotes de aplicativos virtuais não precisam ser seqüenciados novamente.</span><span class="sxs-lookup"><span data-stu-id="14cb1-387">Virtual Application packages do not need to be re-sequenced.</span></span> <span data-ttu-id="14cb1-388">Os assemblies SxS podem permanecer no pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="14cb1-388">SxS Assemblies can remain in the virtual application package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="14cb1-389">As dependências do assembly SxS não serão instaladas no momento da publicação.</span><span class="sxs-lookup"><span data-stu-id="14cb1-389">The SxS Assembly dependencies will not install at publishing time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="14cb1-390">As dependências de assembly SxS devem ser pré-instaladas.</span><span class="sxs-lookup"><span data-stu-id="14cb1-390">SxS Assembly dependencies must be pre-installed.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="14cb1-391">Criando um novo pacote de aplicativo virtual no sequenciador</span><span class="sxs-lookup"><span data-stu-id="14cb1-391">Creating a new virtual application package on the sequencer</span></span>

<span data-ttu-id="14cb1-392">Se, durante o monitoramento do sequenciador, um assembly SxS (como um VC + + Runtime) for instalado como parte da instalação de um aplicativo, o assembly SxS será detectado e incluído no pacote automaticamente.</span><span class="sxs-lookup"><span data-stu-id="14cb1-392">If, during sequencer monitoring, an SxS Assembly (such as a VC++ Runtime) is installed as part of an application’s installation, SxS Assembly will be automatically detected and included in the package.</span></span> <span data-ttu-id="14cb1-393">O administrador será notificado e terá a opção de excluir o assembly SxS.</span><span class="sxs-lookup"><span data-stu-id="14cb1-393">The administrator will be notified and will have the option to exclude the SxS Assembly.</span></span>

<span data-ttu-id="14cb1-394">**Lado do cliente**:</span><span class="sxs-lookup"><span data-stu-id="14cb1-394">**Client Side**:</span></span>

<span data-ttu-id="14cb1-395">Ao publicar um pacote de aplicativo virtual, o cliente App-V detectará se uma dependência SxS obrigatória já está instalada.</span><span class="sxs-lookup"><span data-stu-id="14cb1-395">When publishing a virtual application package, the App-V Client will detect if a required SxS dependency is already installed.</span></span> <span data-ttu-id="14cb1-396">Se a dependência não estiver disponível no computador e estiver incluída no pacote, um programa tradicional do Windows Installer (.\*\* MSI\*\*) a instalação do assembly SxS será iniciada.</span><span class="sxs-lookup"><span data-stu-id="14cb1-396">If the dependency is unavailable on the computer and it is included in the package, a traditional Windows Installer (.**msi**) installation of the SxS assembly will be initiated.</span></span> <span data-ttu-id="14cb1-397">Conforme documentado anteriormente, basta instalar a dependência no computador que está executando o cliente para garantir que a instalação do Windows Installer (. msi) não ocorra.</span><span class="sxs-lookup"><span data-stu-id="14cb1-397">As previously documented, simply install the dependency on the computer running the client to ensure that the Windows Installer (.msi) installation will not occur.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14cb1-398">Etapa</span><span class="sxs-lookup"><span data-stu-id="14cb1-398">Step</span></span></th>
<th align="left"><span data-ttu-id="14cb1-399">Conhecer</span><span class="sxs-lookup"><span data-stu-id="14cb1-399">Considerations</span></span></th>
<th align="left"><span data-ttu-id="14cb1-400">Benefícios</span><span class="sxs-lookup"><span data-stu-id="14cb1-400">Benefits</span></span></th>
<th align="left"><span data-ttu-id="14cb1-401">Compensações</span><span class="sxs-lookup"><span data-stu-id="14cb1-401">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14cb1-402">Empregar arquivos de configuração dinâmicos de forma seletiva</span><span class="sxs-lookup"><span data-stu-id="14cb1-402">Selectively Employ Dynamic Configuration files</span></span></p></td>
<td align="left"><p><span data-ttu-id="14cb1-403">O cliente App-V 5,1 deve analisar e processar esses arquivos de configuração dinâmica.</span><span class="sxs-lookup"><span data-stu-id="14cb1-403">The App-V 5.1 client must parse and process these Dynamic Configuration files.</span></span></p>
<p><span data-ttu-id="14cb1-404">Fique atento ao tamanho e à complexidade (execução de script, inclusões de VREG/exclusões) do arquivo.</span><span class="sxs-lookup"><span data-stu-id="14cb1-404">Be conscious of size and complexity (script execution, VREG inclusions/exclusions) of the file.</span></span></p>
<p><span data-ttu-id="14cb1-405">Muitos pacotes de aplicativos virtuais podem já ter arquivos de configurações dinâmicas específicos do computador ou do computador.</span><span class="sxs-lookup"><span data-stu-id="14cb1-405">Numerous virtual application packages may already have User- or computer–specific dynamic configurations files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="14cb1-406">Os tempos de publicação serão aprimorados se esses arquivos forem usados seletivamente ou não.</span><span class="sxs-lookup"><span data-stu-id="14cb1-406">Publishing times will improve if these files are used selectively or not at all.</span></span></p></td>
<td align="left"><p><span data-ttu-id="14cb1-407">Os pacotes de aplicativos virtuais precisariam ser reconfigurados individualmente ou por meio do console de gerenciamento do App-V Server para remover arquivos de configuração dinâmico associados.</span><span class="sxs-lookup"><span data-stu-id="14cb1-407">Virtual application packages would need to be reconfigured individually or via the App-V server management console to remove associated Dynamic Configuration files.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="14cb1-408">Desativando uma configuração dinâmica usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="14cb1-408">Disabling a Dynamic Configuration using Powershell</span></span>

-   <span data-ttu-id="14cb1-409">Para pacotes já publicados, você pode usar `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` sem</span><span class="sxs-lookup"><span data-stu-id="14cb1-409">For already published packages, you can use `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` without</span></span>

    <span data-ttu-id="14cb1-410">Parâmetro **-DynamicDeploymentConfiguration**</span><span class="sxs-lookup"><span data-stu-id="14cb1-410">**-DynamicDeploymentConfiguration** parameter</span></span>

-   <span data-ttu-id="14cb1-411">Da mesma forma, ao adicionar novos pacotes usando `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv` , não use o</span><span class="sxs-lookup"><span data-stu-id="14cb1-411">Similarly, when adding new packages using `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv`, do not use the</span></span>

    <span data-ttu-id="14cb1-412">**-Parâmetro DynamicDeploymentConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="14cb1-412">**-DynamicDeploymentConfiguration** parameter.</span></span>

<span data-ttu-id="14cb1-413">Para obter a documentação sobre como aplicar uma configuração dinâmica, consulte:</span><span class="sxs-lookup"><span data-stu-id="14cb1-413">For documentation on How to Apply a Dynamic Configuration, see:</span></span>

-   [<span data-ttu-id="14cb1-414">Como aplicar o arquivo de configuração do usuário usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="14cb1-414">How to Apply the User Configuration File by Using PowerShell</span></span>](how-to-apply-the-user-configuration-file-by-using-powershell51.md)

-   [<span data-ttu-id="14cb1-415">Como aplicar o arquivo de configuração da implantação usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="14cb1-415">How to Apply the Deployment Configuration File by Using PowerShell</span></span>](how-to-apply-the-deployment-configuration-file-by-using-powershell51.md)

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="14cb1-416">Etapa</span><span class="sxs-lookup"><span data-stu-id="14cb1-416">Step</span></span></th>
<th align="left"><span data-ttu-id="14cb1-417">Conhecer</span><span class="sxs-lookup"><span data-stu-id="14cb1-417">Considerations</span></span></th>
<th align="left"><span data-ttu-id="14cb1-418">Benefícios</span><span class="sxs-lookup"><span data-stu-id="14cb1-418">Benefits</span></span></th>
<th align="left"><span data-ttu-id="14cb1-419">Compensações</span><span class="sxs-lookup"><span data-stu-id="14cb1-419">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="14cb1-420">Conta para a execução de script síncrono durante o ciclo de vida do pacote.</span><span class="sxs-lookup"><span data-stu-id="14cb1-420">Account for Synchronous Script Execution during Package Lifecycle.</span></span></p></td>
<td align="left"><p><span data-ttu-id="14cb1-421">Se o material de apoio do script estiver incorporado no pacote, o Add (PowerShell) pode ser significativamente mais lento.</span><span class="sxs-lookup"><span data-stu-id="14cb1-421">If script collateral is embedded in the package, Add (Powershell) may be significantly slower.</span></span></p>
<p><span data-ttu-id="14cb1-422">A execução de scripts durante a inicialização do aplicativo virtual (StartVirtualEnvironment, StartProcess) e/ou adicionar + publicar afetará o desempenho percebido durante uma ou mais dessas operações do ciclo de vida.</span><span class="sxs-lookup"><span data-stu-id="14cb1-422">Running of scripts during virtual application launch (StartVirtualEnvironment, StartProcess) and/or Add+Publish will impact the perceived performance during one or more of these lifecycle operations.</span></span></p></td>
<td align="left"><p><span data-ttu-id="14cb1-423">O uso de scripts assíncronos (não bloqueados) garantirá que as operações do ciclo de vida sejam concluídas com eficiência.</span><span class="sxs-lookup"><span data-stu-id="14cb1-423">Use of Asynchronous (Non-Blocking) Scripts will ensure that the lifecycle operations complete efficiently.</span></span></p></td>
<td align="left"><p><span data-ttu-id="14cb1-424">Esta etapa requer o conhecimento funcional de todos os pacotes de aplicativos virtuais com o material de script incorporado, que tem arquivos de configurações dinâmicos associados e a referência e execução de scripts de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="14cb1-424">This step requires working knowledge of all virtual application packages with embedded script collateral, which have associated dynamic configurations files and which reference and run scripts synchronously.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="14cb1-425">Remover fontes virtuais estranhas do pacote.</span><span class="sxs-lookup"><span data-stu-id="14cb1-425">Remove Extraneous Virtual Fonts from Package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="14cb1-426">A maioria dos aplicativos investigados pela equipe do produto App-V continha um pequeno número de fontes, geralmente menor que 20.</span><span class="sxs-lookup"><span data-stu-id="14cb1-426">The majority of applications investigated by the App-V product team contained a small number of fonts, typically fewer than 20.</span></span></p></td>
<td align="left"><p><span data-ttu-id="14cb1-427">As fontes virtuais afetam o desempenho da atualização da publicação.</span><span class="sxs-lookup"><span data-stu-id="14cb1-427">Virtual Fonts impact publishing refresh performance.</span></span></p></td>
<td align="left"><p><span data-ttu-id="14cb1-428">As fontes desejadas deverão ser habilitadas/instaladas nativamente.</span><span class="sxs-lookup"><span data-stu-id="14cb1-428">Desired fonts will need to be enabled/installed natively.</span></span> <span data-ttu-id="14cb1-429">Para obter instruções, confira instalar ou desinstalar fontes.</span><span class="sxs-lookup"><span data-stu-id="14cb1-429">For instructions, see Install or uninstall fonts.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="14cb1-430">Determinar quais fontes virtuais existem no pacote</span><span class="sxs-lookup"><span data-stu-id="14cb1-430">Determining what virtual fonts exist in the package</span></span>

-   <span data-ttu-id="14cb1-431">Faça uma cópia do pacote.</span><span class="sxs-lookup"><span data-stu-id="14cb1-431">Make a copy of the package.</span></span>

-   <span data-ttu-id="14cb1-432">Renomear o pacote \ _copy. AppV para Package\_copy.zip</span><span class="sxs-lookup"><span data-stu-id="14cb1-432">Rename Package\_copy.appv to Package\_copy.zip</span></span>

-   <span data-ttu-id="14cb1-433">Abra AppxManifest.xml e localize o seguinte:</span><span class="sxs-lookup"><span data-stu-id="14cb1-433">Open AppxManifest.xml and locate the following:</span></span>

    <span data-ttu-id="14cb1-434">&lt;AppV: categoria de extensão = "AppV. fonts"&gt;</span><span class="sxs-lookup"><span data-stu-id="14cb1-434">&lt;appv:Extension Category="AppV.Fonts"&gt;</span></span>

    <span data-ttu-id="14cb1-435">&lt;AppV: fontes&gt;</span><span class="sxs-lookup"><span data-stu-id="14cb1-435">&lt;appv:Fonts&gt;</span></span>

    <span data-ttu-id="14cb1-436">&lt;AppV: caminho da fonte = "\ [{fonts} \] \\private\\CalibriL.ttf" DelayLoad = "true" &gt; &lt; /AppV: Font&gt;</span><span class="sxs-lookup"><span data-stu-id="14cb1-436">&lt;appv:Font Path="\[{Fonts}\]\\private\\CalibriL.ttf" DelayLoad="true"&gt;&lt;/appv:Font&gt;</span></span>

    **<span data-ttu-id="14cb1-437">Observação</span><span class="sxs-lookup"><span data-stu-id="14cb1-437">Note</span></span>**  
    <span data-ttu-id="14cb1-438">Se houver fontes marcadas como **DELAYLOAD**, elas não terão impacto na primeira inicialização.</span><span class="sxs-lookup"><span data-stu-id="14cb1-438">If there are fonts marked as **DelayLoad**, those will not impact first launch.</span></span>



~~~
&lt;/appv:Fonts&gt;
~~~

### <span data-ttu-id="14cb1-439">Excluindo fontes virtuais do pacote</span><span class="sxs-lookup"><span data-stu-id="14cb1-439">Excluding virtual fonts from the package</span></span>

<span data-ttu-id="14cb1-440">Use o arquivo de configuração dinâmica que melhor se adapta ao escopo do usuário – configuração de implantação para todos os usuários no computador, configuração de usuário para usuários específicos ou usuários.</span><span class="sxs-lookup"><span data-stu-id="14cb1-440">Use the dynamic configuration file that best suits the user scope – deployment configuration for all users on computer, user configuration for specific user or users.</span></span>

-   <span data-ttu-id="14cb1-441">Desative as fontes com a implantação ou a configuração do usuário.</span><span class="sxs-lookup"><span data-stu-id="14cb1-441">Disable fonts with the deployment or user configuration.</span></span>

<span data-ttu-id="14cb1-442">Fontes</span><span class="sxs-lookup"><span data-stu-id="14cb1-442">Fonts</span></span>

--&gt;

<span data-ttu-id="14cb1-443">&lt;Fonts Enabled = "false"/&gt;</span><span class="sxs-lookup"><span data-stu-id="14cb1-443">&lt;Fonts Enabled="false" /&gt;</span></span>

<span data-ttu-id="14cb1-444">&lt;!--</span><span class="sxs-lookup"><span data-stu-id="14cb1-444">&lt;!--</span></span>

## <a href="" id="bkmk-terms1"></a> <span data-ttu-id="14cb1-445">Terminologia de diretrizes de desempenho do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="14cb1-445">App-V 5.1 Performance Guidance Terminology</span></span>


<span data-ttu-id="14cb1-446">Os termos a seguir são usados para descrever os conceitos e ações relacionados à otimização de desempenho do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="14cb1-446">The following terms are used when describing concepts and actions related to App-V 5.1 performance optimization.</span></span>

-   <span data-ttu-id="14cb1-447">**Complexidade** – refere-se a uma ou mais características do pacote que podem afetar o desempenho durante a pré-configuração (**Add-AppvClientPackage**) ou integração (**Publish-AppvClientPackage**).</span><span class="sxs-lookup"><span data-stu-id="14cb1-447">**Complexity** – Refers to the one or more package characteristics that may impact performance during pre-configure (**Add-AppvClientPackage**) or integration (**Publish-AppvClientPackage**).</span></span> <span data-ttu-id="14cb1-448">Alguns exemplos de características são: tamanho do manifesto, número de fontes virtuais, número de arquivos.</span><span class="sxs-lookup"><span data-stu-id="14cb1-448">Some example characteristics are: manifest size, number of virtual fonts, number of files.</span></span>

-   <span data-ttu-id="14cb1-449">**Desintegrar** – remove as integrações do usuário</span><span class="sxs-lookup"><span data-stu-id="14cb1-449">**De-Integrate** – Removes the user integrations</span></span>

-   <span data-ttu-id="14cb1-450">**Integrar novamente** – aplica as integrações do usuário.</span><span class="sxs-lookup"><span data-stu-id="14cb1-450">**Re-Integrate** – Applies the user integrations.</span></span>

-   <span data-ttu-id="14cb1-451">**Não persistente, poold** – cria um computador que executa um ambiente virtual cada vez que eles fazem logon.</span><span class="sxs-lookup"><span data-stu-id="14cb1-451">**Non-Persistent, Pooled** – Creates a computer running a virtual environment each time they log in.</span></span>

-   <span data-ttu-id="14cb1-452">**Persistente, pessoal** – um computador que executa um ambiente virtual que permanece igual para cada logon.</span><span class="sxs-lookup"><span data-stu-id="14cb1-452">**Persistent, Personal** – A computer running a virtual environment that remains the same for every login.</span></span>

-   <span data-ttu-id="14cb1-453">**Stateful** – para este documento, sugere que as integrações do usuário são mantidas entre sessões e uma tecnologia de gerenciamento do ambiente do usuário é usada em conjunto com RDSH não persistente ou VDI.</span><span class="sxs-lookup"><span data-stu-id="14cb1-453">**Stateful** - For this document, implies that user integrations are persisted between sessions and a user environment management technology is used in conjunction with non-persistent RDSH or VDI.</span></span>

-   <span data-ttu-id="14cb1-454">**Sem monitoração** de estado – representa um cenário quando nenhum estado do usuário é mantido entre as sessões.</span><span class="sxs-lookup"><span data-stu-id="14cb1-454">**Stateless** – Represents a scenario when no user state is persisted between sessions.</span></span>

-   <span data-ttu-id="14cb1-455">**Gatilho** – (ou gatilhos de ação nativa).</span><span class="sxs-lookup"><span data-stu-id="14cb1-455">**Trigger** – (or Native Action Triggers).</span></span> <span data-ttu-id="14cb1-456">O UPM usa esses tipos de gatilhos para iniciar operações de monitoramento ou sincronização.</span><span class="sxs-lookup"><span data-stu-id="14cb1-456">UPM uses these types of triggers to initiate monitoring or synchronization operations.</span></span>

-   <span data-ttu-id="14cb1-457">**Experiência do usuário** -no contexto do App-V 5,1, a experiência do usuário, quantitativomente, é a soma das seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="14cb1-457">**User Experience** - In the context of App-V 5.1, the user experience, quantitatively, is the sum of the following parts:</span></span>

    -   <span data-ttu-id="14cb1-458">Do ponto em que os usuários iniciam um logon quando podem manipular a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="14cb1-458">From the point that users initiate a log-in to when they are able to manipulate the desktop.</span></span>

    -   <span data-ttu-id="14cb1-459">A partir do ponto em que a área de trabalho pode ser interagindo ao ponto em que uma atualização de publicação começa (em termos do PowerShell, sincronizar) ao usar a infraestrutura de servidor completo do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="14cb1-459">From the point where the desktop can be interacted with to the point a publishing refresh begins (in PowerShell terms, sync) when using the App-V 5.1 full server infrastructure.</span></span> <span data-ttu-id="14cb1-460">Em instâncias autônomas, é quando os comandos do PowerShell **Add-AppVClientPackage** e **Publish-AppVClientPackage** são iniciados.</span><span class="sxs-lookup"><span data-stu-id="14cb1-460">In standalone instances, it is when the **Add-AppVClientPackage** and **Publish-AppVClientPackage Powershell** commands are initiated.</span></span>

    -   <span data-ttu-id="14cb1-461">Do início ao término da atualização da publicação.</span><span class="sxs-lookup"><span data-stu-id="14cb1-461">From start to completion of the publishing refresh.</span></span> <span data-ttu-id="14cb1-462">Em instâncias autônomas, este é o primeiro a último aplicativo virtual publicado.</span><span class="sxs-lookup"><span data-stu-id="14cb1-462">In standalone instances, this is the first to last virtual application published.</span></span>

    -   <span data-ttu-id="14cb1-463">A partir do ponto em que o aplicativo virtual está disponível para ser iniciado a partir de um atalho.</span><span class="sxs-lookup"><span data-stu-id="14cb1-463">From the point where the virtual application is available to launch from a shortcut.</span></span> <span data-ttu-id="14cb1-464">Como alternativa, ele é do ponto em que a associação de tipo de arquivo está registrada e iniciará um aplicativo virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="14cb1-464">Alternatively, it is from the point at which the file type association is registered and will launch a specified virtual application.</span></span>

-   <span data-ttu-id="14cb1-465">**Gerenciamento de perfil de usuário** – a abordagem controlada e estruturada para gerenciar componentes do usuário associados ao ambiente.</span><span class="sxs-lookup"><span data-stu-id="14cb1-465">**User Profile Management** – The controlled and structured approach to managing user components associated with the environment.</span></span> <span data-ttu-id="14cb1-466">Por exemplo, perfis de usuário, gerenciamento de preferências e políticas, controle de aplicativos e implantação de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="14cb1-466">For example, user profiles, preference and policy management, application control and application deployment.</span></span> <span data-ttu-id="14cb1-467">Você pode usar scripts ou soluções de terceiros para configurar o ambiente conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="14cb1-467">You can use scripting or third-party solutions configure the environment as needed.</span></span>






## <span data-ttu-id="14cb1-468">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="14cb1-468">Related topics</span></span>


[<span data-ttu-id="14cb1-469">Guia do administrador do Microsoft Application Virtualization 5,1</span><span class="sxs-lookup"><span data-stu-id="14cb1-469">Microsoft Application Virtualization 5.1 Administrator's Guide</span></span>](microsoft-application-virtualization-51-administrators-guide.md)









