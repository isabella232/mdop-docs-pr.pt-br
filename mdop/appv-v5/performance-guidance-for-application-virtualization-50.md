---
title: Guia de desempenho do Application Virtualization 5.0
description: Guia de desempenho do Application Virtualization 5.0
author: dansimp
ms.assetid: 6b3a3255-b957-4b9b-8bfc-a93fe8438a81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3b0f5ef07935fc34adce772e7b2fff85a12b01dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796274"
---
# <span data-ttu-id="dbcb3-103">Guia de desempenho do Application Virtualization 5.0</span><span class="sxs-lookup"><span data-stu-id="dbcb3-103">Performance Guidance for Application Virtualization 5.0</span></span>


<span data-ttu-id="dbcb3-104">Saiba como configurar o App-V 5,0 para obter ótimo desempenho, otimizar pacotes de aplicativos virtuais e oferecer uma experiência de usuário melhor com o RDS e o VDI.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-104">Learn how to configure App-V 5.0 for optimal performance, optimize virtual app packages, and provide a better user experience with RDS and VDI.</span></span>

<span data-ttu-id="dbcb3-105">A implementação de vários métodos pode ajudá-lo a melhorar a experiência do usuário final.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-105">Implementing multiple methods can help you improve the end-user experience.</span></span> <span data-ttu-id="dbcb3-106">No entanto, seu ambiente pode não dar suporte a todos os métodos.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-106">However, your environment may not support all methods.</span></span>

<span data-ttu-id="dbcb3-107">Você deve ler e compreender as informações a seguir antes de ler este documento.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-107">You should read and understand the following information before reading this document.</span></span>

-   [<span data-ttu-id="dbcb3-108">Guia do administrador do Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="dbcb3-108">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)

-   [<span data-ttu-id="dbcb3-109">Publicação de aplicativos e interação do cliente do App-V 5 SP2</span><span class="sxs-lookup"><span data-stu-id="dbcb3-109">App-V 5 SP2 Application Publishing and Client Interaction</span></span>](https://go.microsoft.com/fwlink/?LinkId=395206)

-   [<span data-ttu-id="dbcb3-110">Guia de sequenciamento do Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="dbcb3-110">Microsoft Application Virtualization 5.0 Sequencing Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=269953)

**<span data-ttu-id="dbcb3-111">Observação</span><span class="sxs-lookup"><span data-stu-id="dbcb3-111">Note</span></span>**  
<span data-ttu-id="dbcb3-112">Alguns termos usados neste documento podem ter significados diferentes dependendo da fonte externa e do contexto.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-112">Some terms used in this document may have different meanings depending on external source and context.</span></span> <span data-ttu-id="dbcb3-113">Para obter mais informações sobre os termos usados neste documento seguidos de um asterisco **\\** \*, consulte a seção [terminologia de orientação do desempenho do Application Virtualization](#bkmk-terms1) deste documento.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-113">For more information about terms used in this document followed by an asterisk **\\**\* review the [Application Virtualization Performance Guidance Terminology](#bkmk-terms1) section of this document.</span></span>



<span data-ttu-id="dbcb3-114">Por fim, este documento fornecerá as informações para configurar o computador que está executando o cliente do App-V 5,0 e o ambiente para obter ótimo desempenho.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-114">Finally, this document will provide you with the information to configure the computer running App-V 5.0 client and the environment for optimal performance.</span></span> <span data-ttu-id="dbcb3-115">Otimize seus pacotes de aplicativos virtuais para desempenho usando o sequenciador e saiba como usar a virtualização de experiência do usuário (UE-V) ou outras tecnologias de gerenciamento do ambiente do usuário para fornecer a melhor experiência do usuário com o App-V 5,0 nos serviços de área de trabalho remota (RDS) e infraestrutura de área de trabalho virtual (VDI) não persistente.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-115">Optimize your virtual application packages for performance using the sequencer, and to understand how to use User Experience Virtualization (UE-V) or other user environment management technologies to provide the optimal user experience with App-V 5.0 in both Remote Desktop Services (RDS) and non-persistent virtual desktop infrastructure (VDI).</span></span>

<span data-ttu-id="dbcb3-116">Para ajudar a determinar quais informações são relevantes para o seu ambiente, examine a breve visão geral e a lista de verificação de aplicabilidade de cada seção.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-116">To help determine what information is relevant to your environment you should review each section’s brief overview and applicability checklist.</span></span>

## <a href="" id="---------app-v-5-0-in-stateful--non-persistent-deployments"></a> <span data-ttu-id="dbcb3-117">App-V 5,0 em implantações de estado \ \* não persistentes</span><span class="sxs-lookup"><span data-stu-id="dbcb3-117">App-V 5.0 in stateful\* non-persistent deployments</span></span>


<span data-ttu-id="dbcb3-118">Esta seção fornece informações sobre uma abordagem que ajuda a garantir que um usuário terá acesso a todos os aplicativos virtuais em segundos após o logon.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-118">This section provides information about an approach that helps ensure a user will have access to all virtual applications within seconds after logging in.</span></span> <span data-ttu-id="dbcb3-119">Isso é conseguido com o endereçamento exclusivo da atualização de publicação do App-V 5,0 de longa execução.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-119">This is achieved by uniquely addressing the often long-running App-V 5.0 publishing refresh.</span></span> <span data-ttu-id="dbcb3-120">Como você descobrirá a base da abordagem, a atualização de publicação mais rápida é aquela que não precisa realmente fazer nada.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-120">As you will discover the basis of the approach, the fastest publishing refresh, is one that doesn’t have to actually do anything.</span></span> <span data-ttu-id="dbcb3-121">Uma série de condições deve ser satisfeita e etapas seguidas para fornecer a melhor experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-121">A number of conditions must be met and steps followed to provide the optimal user experience.</span></span>

<span data-ttu-id="dbcb3-122">Use as informações na seção a seguir para obter mais informações:</span><span class="sxs-lookup"><span data-stu-id="dbcb3-122">Use the information in the following section for more information:</span></span>

<span data-ttu-id="dbcb3-123">[Cenários de uso](#bkmk-us) – conforme você revisa os dois cenários, lembre-se de que esses são os métodos extremos.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-123">[Usage Scenarios](#bkmk-us) - As you review the two scenarios, keep in mind that these are the approach extremes.</span></span> <span data-ttu-id="dbcb3-124">Com base em seus requisitos de uso, você pode optar por aplicar essas etapas a um subconjunto de pacotes de aplicativos virtuais e/ou usuários.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-124">Based on your usage requirements, you may choose to apply these steps to a subset of users and/or virtual applications packages.</span></span>

-   <span data-ttu-id="dbcb3-125">Otimizado para desempenho – para fornecer a experiência ideal, você pode esperar que a imagem base inclua alguns dos pacotes de aplicativo virtual do App-V.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-125">Optimized for Performance – To provide the optimal experience, you can expect the base image to include some of the App-V virtual application package.</span></span> <span data-ttu-id="dbcb3-126">Esse e outros requisitos são discutidos.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-126">This and other requirements are discussed.</span></span>

-   <span data-ttu-id="dbcb3-127">Otimizado para armazenamento – se você estiver preocupado com o impacto do armazenamento, seguir este cenário irá ajudá-lo a solucionar esses problemas.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-127">Optimized for Storage – If you are concerned with the storage impact, following this scenario will help address those concerns.</span></span>

[<span data-ttu-id="dbcb3-128">Preparando seu ambiente</span><span class="sxs-lookup"><span data-stu-id="dbcb3-128">Preparing your Environment</span></span>](#bkmk-pe)

-   <span data-ttu-id="dbcb3-129">Etapas para preparar a imagem base – seja em um ambiente de VDI ou RDSH não persistente, apenas algumas etapas devem ser concluídas na imagem base para habilitar essa abordagem.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-129">Steps to Prepare the Base Image – Whether in a non-persistent VDI or RDSH environment, only a few steps must be completed in the base image to enable this approach.</span></span>

-   <span data-ttu-id="dbcb3-130">Use o UE-V 2,0 como a solução de gerenciamento de perfil do usuário (UPM) para a abordagem do App-V – a base dessa abordagem é a capacidade de uma solução UEM de persistir o conteúdo de apenas alguns locais de registro e de arquivo.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-130">Use UE-V 2.0 as the User Profile Management (UPM) solution for the App-V approach – the cornerstone of this approach is the ability of a UEM solution to persist the contents of just a few registry and file locations.</span></span> <span data-ttu-id="dbcb3-131">Esses locais constituem as integrações do usuário \ \*.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-131">These locations constitute the user integrations\*.</span></span> <span data-ttu-id="dbcb3-132">Certifique-se de analisar os requisitos específicos para a solução UPM.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-132">Be sure to review the specific requirements for the UPM solution.</span></span>

[<span data-ttu-id="dbcb3-133">Orientação de experiência do usuário</span><span class="sxs-lookup"><span data-stu-id="dbcb3-133">User Experience Walk-through</span></span>](#bkmk-uewt)

-   <span data-ttu-id="dbcb3-134">Acompanhamento-passo-a-passo é uma orientação passo a passo das operações do App-V e do UE-V e das expectativas que os usuários devem ter.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-134">Walk-through – This is a step-by-step walk-through of the App-V and UE-V operations and the expectations users should have.</span></span>

-   <span data-ttu-id="dbcb3-135">Resultado – descreve os resultados esperados.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-135">Outcome – This describes the expected results.</span></span>

[<span data-ttu-id="dbcb3-136">Impacto no ciclo de vida do pacote</span><span class="sxs-lookup"><span data-stu-id="dbcb3-136">Impact to Package Lifecycle</span></span>](#bkmk-plc)

[<span data-ttu-id="dbcb3-137">Aprimorar a experiência com VDI por meio da otimização/ajuste de desempenho</span><span class="sxs-lookup"><span data-stu-id="dbcb3-137">Enhancing the VDI Experience through Performance Optimization/Tuning</span></span>](#bkmk-evdi)

### <a href="" id="applicability-checklist-"></a><span data-ttu-id="dbcb3-138">Lista de verificação de aplicabilidade</span><span class="sxs-lookup"><span data-stu-id="dbcb3-138">Applicability Checklist</span></span>

<span data-ttu-id="dbcb3-139">Ambiente de implantação</span><span class="sxs-lookup"><span data-stu-id="dbcb3-139">Deployment Environment</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="dbcb3-140">VDI ou RDSH não persistentes.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-140">Non-Persistent VDI or RDSH.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="dbcb3-141">User Experience Virtualization (UE-V), outras soluções UPM ou discos de perfil de usuário (UPD).</span><span class="sxs-lookup"><span data-stu-id="dbcb3-141">User Experience Virtualization (UE-V), other UPM solutions or User Profile Disks (UPD).</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="dbcb3-142">Configuração esperada</span><span class="sxs-lookup"><span data-stu-id="dbcb3-142">Expected Configuration</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="dbcb3-143">User Experience Virtualization (UE-V) com o modelo de estado de usuário do App-V habilitado ou o software de gerenciamento de perfil do usuário (UPM).</span><span class="sxs-lookup"><span data-stu-id="dbcb3-143">User Experience Virtualization (UE-V) with the App-V user state template enabled or User Profile Management (UPM) software.</span></span> <span data-ttu-id="dbcb3-144">O software UPM não-UE-V deve ser capaz de disparar no início e no logoff de logon ou processo/aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-144">Non-UE-V UPM software must be capable of triggering on Login or Process/Application Start and Logoff.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="dbcb3-145">O SCS (repositório de conteúdo compartilhado) do App-V está configurado ou pode ser configurado.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-145">App-V Shared Content Store (SCS) is configured or can be configured.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="dbcb3-146">Administração de ti</span><span class="sxs-lookup"><span data-stu-id="dbcb3-146">IT Administration</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="dbcb3-147">O administrador pode precisar atualizar a imagem base da VM regularmente para garantir o desempenho ideal ou o administrador pode precisar gerenciar várias imagens para diferentes grupos de usuários.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-147">Admin may need to update the VM base image regularly to ensure optimal performance or Admin may need to manage multiple images for different user groups.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-us"></a><span data-ttu-id="dbcb3-148">Cenário de uso</span><span class="sxs-lookup"><span data-stu-id="dbcb3-148">Usage Scenario</span></span>

<span data-ttu-id="dbcb3-149">Ao revisar os dois cenários, lembre-se de que esses métodos são extremos.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-149">As you review the two scenarios, keep in mind that these approach the extremes.</span></span> <span data-ttu-id="dbcb3-150">Com base em seus requisitos de uso, você pode optar por aplicar essas etapas a um subconjunto de usuários, pacotes de aplicativos virtuais ou ambos.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-150">Based on your usage requirements, you may choose to apply these steps to a subset of users, virtual application packages, or both.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dbcb3-151">Otimizado para desempenho</span><span class="sxs-lookup"><span data-stu-id="dbcb3-151">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="dbcb3-152">Otimizado para armazenamento</span><span class="sxs-lookup"><span data-stu-id="dbcb3-152">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dbcb3-153">Para fornecer a melhor experiência do usuário, essa abordagem aproveita os recursos de uma solução UPM e requer uma preparação adicional da imagem e pode causar uma sobrecarga adicional de gerenciamento de imagens.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-153">To provide the most optimal user experience, this approach leverages the capabilities of a UPM solution and requires additional image preparation and can incur some additional image management overhead.</span></span></p>
<p><span data-ttu-id="dbcb3-154">A seguir está a descrição de vários aprimoramentos de desempenho em implantações não persistentes de estado.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-154">The following describes many performance improvements in stateful non-persistent deployments.</span></span> <span data-ttu-id="dbcb3-155">Para obter mais informações, consulte as <strong> etapas de sequenciamento para otimizar pacotes para a publicação de desempenho </strong> e referência para <strong> o guia de sequenciamento do App-V 5,0 </strong> na <strong> seção Consulte também deste documento </strong> .</span><span class="sxs-lookup"><span data-stu-id="dbcb3-155">For more information, see the <strong>Sequencing Steps to Optimize Packages for Publishing Performance</strong> and reference to <strong>App-V 5.0 Sequencing Guide</strong> in the <strong>See Also section of this document</strong>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dbcb3-156">As expectativas gerais do cenário anterior ainda se aplicam aqui.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-156">The general expectations of the previous scenario still apply here.</span></span> <span data-ttu-id="dbcb3-157">No entanto, lembre-se de que as imagens da VM são geralmente armazenadas em arrays dispendiosos; uma ligeira alteração foi feita na abordagem.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-157">However, keep in mind that VM images are typically stored in very costly arrays; a slight alteration has been made to the approach.</span></span> <span data-ttu-id="dbcb3-158">Não configure previamente pacotes de aplicativos virtuais direcionados pelo usuário na imagem base.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-158">Do not pre-configure user-targeted virtual application packages in the base image.</span></span></p>
<p><span data-ttu-id="dbcb3-159">O impacto dessas alterações é detalhado na seção do guia de experiência do usuário deste documento.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-159">The impact of this alteration is detailed in the User Experience Walkthrough section of this document.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pe"></a><span data-ttu-id="dbcb3-160">Preparando seu ambiente</span><span class="sxs-lookup"><span data-stu-id="dbcb3-160">Preparing your Environment</span></span>

<span data-ttu-id="dbcb3-161">A tabela a seguir mostra as etapas necessárias para preparar a imagem base e o UE-V ou outra solução UPM para a abordagem.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-161">The following table displays the required steps to prepare the base image and the UE-V or another UPM solution for the approach.</span></span>

**<span data-ttu-id="dbcb3-162">Preparar a imagem base</span><span class="sxs-lookup"><span data-stu-id="dbcb3-162">Prepare the Base Image</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dbcb3-163">Otimizado para desempenho</span><span class="sxs-lookup"><span data-stu-id="dbcb3-163">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="dbcb3-164">Otimizado para armazenamento</span><span class="sxs-lookup"><span data-stu-id="dbcb3-164">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="dbcb3-165">Instale o pacote de hotfix 4 para a versão do cliente do aplicativo virtualização do 5,0 SP2 do cliente.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-165">Install the Hotfix Package 4 for Application Virtualization 5.0 SP2 client version of the client.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-166">Instalar o UE-V e baixar o modelo de configurações do App-V da Galeria de modelos do UE-V, consulte as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-166">Install UE-V and download the App-V Settings Template from the UE-V template Gallery, see the following steps.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-167">Configurar para o modo SCS (repositório de conteúdo compartilhado).</span><span class="sxs-lookup"><span data-stu-id="dbcb3-167">Configure for Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="dbcb3-168">Para obter mais informações, consulte <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)"> como instalar o aplicativo App-V 5,0 para o modo de repositório de conteúdo compartilhado </a> .</span><span class="sxs-lookup"><span data-stu-id="dbcb3-168">For more information see <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)">How to Install the App-V 5.0 Client for Shared Content Store Mode</a>.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-169">Configurar preservar integrações de usuário na DWORD do registro de logon.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-169">Configure Preserve User Integrations on Login Registry DWORD.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-170">Pré-configure todos os pacotes de usuário e de destino global, por exemplo, <strong> Add-AppvClientPackage </strong> .</span><span class="sxs-lookup"><span data-stu-id="dbcb3-170">Pre-configure all user- and global-targeted packages for example, <strong>Add-AppvClientPackage</strong>.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-171">Pré-configure todos os grupos de conexões direcionadas a usuário e global, por exemplo, <strong> Add-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="dbcb3-171">Pre-configure all user- and global-targeted connection groups for example, <strong>Add-AppvClientConnectionGroup</strong>.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-172">Pré-publique todos os pacotes direcionados globalmente.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-172">Pre-publish all global-targeted packages.</span></span></p>
<p></p>
<p><span data-ttu-id="dbcb3-173">Como alternativa</span><span class="sxs-lookup"><span data-stu-id="dbcb3-173">Alternatively,</span></span></p>
<ul>
<li><p><span data-ttu-id="dbcb3-174">Executar uma publicação/atualização global.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-174">Perform a global publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-175">Executar uma publicação/atualização de usuário.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-175">Perform a user publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-176">Cancele a publicação de todos os pacotes direcionados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-176">Un-publish all user-targeted packages.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-177">Exclua as seguintes entradas de User-virtual File System (VFS).</span><span class="sxs-lookup"><span data-stu-id="dbcb3-177">Delete the following user-Virtual File System (VFS) entries.</span></span></p></li>
</ul>
<p><code>AppData\Local\Microsoft\AppV\Client\VFS</code></p>
<p><code>AppData\Roaming\Microsoft\AppV\Client\VFS</code></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="dbcb3-178">Instale o pacote de hotfix 4 para a versão do cliente do aplicativo virtualização do 5,0 SP2 do cliente.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-178">Install the Hotfix Package 4 for Application Virtualization 5.0 SP2 client version of the client.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-179">Instalar o UE-V e baixar o modelo de configurações do App-V da Galeria de modelos do UE-V, consulte as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-179">Install UE-V and download the App-V Settings Template from the UE-V template Gallery, see the following steps.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-180">Configurar para o modo SCS (repositório de conteúdo compartilhado).</span><span class="sxs-lookup"><span data-stu-id="dbcb3-180">Configure for Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="dbcb3-181">Para obter mais informações, consulte <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)"> como instalar o aplicativo App-V 5,0 para o modo de repositório de conteúdo compartilhado </a> .</span><span class="sxs-lookup"><span data-stu-id="dbcb3-181">For more information see <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)">How to Install the App-V 5.0 Client for Shared Content Store Mode</a>.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-182">Configurar preservar integrações de usuário na DWORD do registro de logon.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-182">Configure Preserve User Integrations on Login Registry DWORD.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-183">Pré-configure todos os pacotes direcionados global por exemplo, <strong> Add-AppvClientPackage </strong> .</span><span class="sxs-lookup"><span data-stu-id="dbcb3-183">Pre-configure all global-targeted packages for example, <strong>Add-AppvClientPackage</strong>.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-184">Pré-configure todos os grupos de conexão de direcionamento global, por exemplo, <strong> Add-AppvClientConnectionGroup </strong> .</span><span class="sxs-lookup"><span data-stu-id="dbcb3-184">Pre-configure all global-targeted connection groups for example, <strong>Add-AppvClientConnectionGroup</strong>.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-185">Pré-publique todos os pacotes direcionados globalmente.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-185">Pre-publish all global-targeted packages.</span></span></p>
<p></p></li>
</ul></td>
</tr>
</tbody>
</table>



<span data-ttu-id="dbcb3-186">**Configurações** -para configurações essenciais do cliente App-V e para obter um pouco mais de contexto e instruções, Confira as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="dbcb3-186">**Configurations** - For critical App-V Client configurations and for a little more context and how-to, review the following information:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dbcb3-187">Configuração</span><span class="sxs-lookup"><span data-stu-id="dbcb3-187">Configuration Setting</span></span></th>
<th align="left"><span data-ttu-id="dbcb3-188">O que isso faz?</span><span class="sxs-lookup"><span data-stu-id="dbcb3-188">What does this do?</span></span></th>
<th align="left"><span data-ttu-id="dbcb3-189">Como devo usá-lo?</span><span class="sxs-lookup"><span data-stu-id="dbcb3-189">How should I use it?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dbcb3-190">Modo SCS (Shared Content Store)</span><span class="sxs-lookup"><span data-stu-id="dbcb3-190">Shared Content Store (SCS) Mode</span></span></p>
<ul>
<li><p><span data-ttu-id="dbcb3-191">Configurável no PowerShell usando <strong> set-AppvClientConfiguration </strong> – <strong> SharedContentStoreMode </strong> ou</span><span class="sxs-lookup"><span data-stu-id="dbcb3-191">Configurable in PowerShell using <strong>Set- AppvClientConfiguration</strong> –<strong>SharedContentStoreMode</strong>, or</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-192">Durante a instalação do cliente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-192">During installation of the App-V 5.0 client.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="dbcb3-193">Ao executar o repositório de conteúdo compartilhado, somente os dados de publicação são mantidos no disco rígido; outros ativos de aplicativo virtual são mantidos na memória (RAM).</span><span class="sxs-lookup"><span data-stu-id="dbcb3-193">When running the shared content store only publishing data is maintained on hard disk; other virtual application assets are maintained in memory (RAM).</span></span></p>
<p><span data-ttu-id="dbcb3-194">Isso ajuda a conservar o armazenamento local e a minimizar a e/s de disco por segundo (IOPS).</span><span class="sxs-lookup"><span data-stu-id="dbcb3-194">This helps to conserve local storage and minimize disk I/O per second (IOPS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="dbcb3-195">Isso é recomendado quando conexões de baixa latência são disponibilizadas entre o ponto de extremidade do cliente App-V e o servidor de conteúdo do SCS, SAN.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-195">This is recommended when low-latency connections are available between the App-V Client endpoint and the SCS content server, SAN.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dbcb3-196">PreserveUserIntegrationsOnLogin</span><span class="sxs-lookup"><span data-stu-id="dbcb3-196">PreserveUserIntegrationsOnLogin</span></span></p>
<ul>
<li><p><span data-ttu-id="dbcb3-197">Configurar no registro em <strong> HKEY_LOCAL_MACHINE </strong>  \  <strong> software </strong>  \  <strong> Microsoft </strong>  \  <strong> AppV </strong>  \  <strong> Client </strong>  \  <strong> Integration </strong> .</span><span class="sxs-lookup"><span data-stu-id="dbcb3-197">Configure in the Registry under <strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>AppV</strong> \ <strong>Client</strong> \ <strong>Integration</strong>.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-198">Crie o valor DWORD <strong> PreserveUserIntegrationsOnLogin </strong> com um valor de <strong> 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="dbcb3-198">Create the DWORD value <strong>PreserveUserIntegrationsOnLogin</strong> with a value of <strong>1</strong>.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-199">Reinicie o serviço App-V Client ou reinicie o computador que executa o cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-199">Restart the App-V client service or restart the computer running the App-V Client.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="dbcb3-200">Se você não tiver pré-configurado ( <strong> Add-AppvClientPackage </strong> ) um pacote específico e essa configuração não for definida, o cliente App-V desintegrará \* as integrações de usuário persistentes e, em seguida, se reintegrará \*.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-200">If you have not pre-configured (<strong>Add-AppvClientPackage</strong>) a specific package and this setting is not configured, the App-V Client will de-integrate\* the persisted user integrations, then re-integrate\*.</span></span></p>
<p><span data-ttu-id="dbcb3-201">Para cada pacote que atenda às condições acima, o dobro do trabalho será realizado durante a publicação/atualização.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-201">For every package that meets the above conditions, effectively twice the work will be done during publishing/refresh.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dbcb3-202">Se você não planeja pré-configurar previamente cada pacote de usuário disponível na imagem base, use essa configuração.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-202">If you don’t plan to pre-configure every available user package in the base image, use this setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dbcb3-203">MaxConcurrentPublishingRefresh</span><span class="sxs-lookup"><span data-stu-id="dbcb3-203">MaxConcurrentPublishingRefresh</span></span></p>
<ul>
<li><p><span data-ttu-id="dbcb3-204">Configurar no registro em <strong> HKEY_LOCAL_MACHINE </strong> &lt; forte &gt; software </strong>  \  <strong> publicação de </strong>  \  <strong> </strong> &lt; cliente forte do Microsoft AppV &gt; </strong>  \  <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="dbcb3-204">Configure in the Registry under <strong>HKEY_LOCAL_MACHINE</strong> &lt;strong&gt;Software</strong> \ <strong>Microsoft</strong> \ <strong>AppV</strong> &lt;strong&gt;Client</strong> \ <strong>Publishing</strong>.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-205">Crie o valor DWORD <strong> MaxConcurrentPublishingrefresh </strong> com o número máximo de atualizações de publicação simultâneas desejadas.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-205">Create the DWORD value <strong>MaxConcurrentPublishingrefresh</strong> with the desired maximum number of concurrent publishing refreshes.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-206">O serviço e o computador do cliente App-V não precisam ser reiniciados.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-206">The App-V client service and computer do not need to be restarted.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="dbcb3-207">Essa configuração determina o número de usuários que podem realizar uma atualização/sincronização de publicação ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-207">This setting determines the number of users that can perform a publishing refresh/sync at the same time.</span></span> <span data-ttu-id="dbcb3-208">A configuração padrão é sem limite.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-208">The default setting is no limit.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dbcb3-209">Limitar o número de atualizações de publicação simultâneas impede o uso excessivo da CPU que pode afetar o desempenho do computador.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-209">Limiting the number of concurrent publishing refreshes prevents excessive CPU usage that could impact computer performance.</span></span> <span data-ttu-id="dbcb3-210">Esse limite é recomendado em um ambiente RDS, no qual vários usuários podem entrar no mesmo computador ao mesmo tempo e executar uma sincronização de atualização de publicação.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-210">This limit is recommended in an RDS environment, where multiple users can log in to the same computer at the same time and perform a publishing refresh sync.</span></span></p>
<p><span data-ttu-id="dbcb3-211">Se o limite de atualização de publicação simultânea for atingido, o tempo necessário para publicar novos aplicativos e disponibilizá-los para os usuários finais após o login poderá demorar um período indeterminado.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-211">If the concurrent publishing refresh threshold is reached, the time required to publish new applications and make them available to end users after they log in could take an indeterminate amount of time.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="dbcb3-212">Configurar o método de solução UE-V para App-V</span><span class="sxs-lookup"><span data-stu-id="dbcb3-212">Configure UE-V solution for App-V Approach</span></span>

<span data-ttu-id="dbcb3-213">Recomendamos usar o Microsoft User Experience Virtualization (UE-V) para capturar e centralizar as configurações do aplicativo e as configurações do sistema operacional do Windows para um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-213">We recommend using Microsoft User Experience Virtualization (UE-V) to capture and centralize application settings and Windows operating system settings for a specific user.</span></span> <span data-ttu-id="dbcb3-214">Essas configurações são aplicadas aos diferentes computadores que são acessados pelo usuário, incluindo computadores de mesa, laptops e sessões do Virtual Desktop Infrastructure (VDI).</span><span class="sxs-lookup"><span data-stu-id="dbcb3-214">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span> <span data-ttu-id="dbcb3-215">A UE-V é otimizada para cenários de RDS e VDI.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-215">UE-V is optimized for RDS and VDI scenarios.</span></span>

<span data-ttu-id="dbcb3-216">Para obter mais informações, consulte [introdução ao User Experience Virtualization 2,0](https://technet.microsoft.com/library/dn458936.aspx)</span><span class="sxs-lookup"><span data-stu-id="dbcb3-216">For more information see [Getting Started With User Experience Virtualization 2.0](https://technet.microsoft.com/library/dn458936.aspx)</span></span>

<span data-ttu-id="dbcb3-217">Em essência, tudo o que é necessário é instalar o UE-V Client e baixar o modelo de configurações do aplicativo Microsoft autod App-V da [Galeria de modelos do Microsoft User Experience Virtualization (UE-v)](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33).</span><span class="sxs-lookup"><span data-stu-id="dbcb3-217">In essence all that is required is to install the UE-V client and download the following Microsoft authored App-V settings template from the [Microsoft User Experience Virtualization (UE-V) template gallery](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33).</span></span> <span data-ttu-id="dbcb3-218">Registre o modelo.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-218">Register the template.</span></span> <span data-ttu-id="dbcb3-219">Para obter mais informações sobre os modelos do UE-V, consulte [o recurso específico do UE-v para adquirir e registrar o modelo](https://technet.microsoft.com/library/dn458936.aspx).</span><span class="sxs-lookup"><span data-stu-id="dbcb3-219">For more information around UE-V templates see [The UE-V specific resource for acquiring and registering the template](https://technet.microsoft.com/library/dn458936.aspx).</span></span>

**<span data-ttu-id="dbcb3-220">Observação</span><span class="sxs-lookup"><span data-stu-id="dbcb3-220">Note</span></span>**  
<span data-ttu-id="dbcb3-221">Sem realizar uma etapa de configuração adicional, a virtualização de ambiente de usuário da Microsoft (UE-V) não poderá sincronizar os atalhos do menu iniciar (arquivos. lnk) no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-221">Without performing an additional configuration step, the Microsoft User Environment Virtualization (UE-V) will not be able to synchronize the Start menu shortcuts (.lnk files) on the target computer.</span></span> <span data-ttu-id="dbcb3-222">O tipo de arquivo. lnk é excluído por padrão.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-222">The .lnk file type is excluded by default.</span></span>

<span data-ttu-id="dbcb3-223">O UE-V só dará suporte à remoção do tipo de arquivo. lnk da lista de exclusão nos cenários de RDS e VDI, em que cada dispositivo de usuário terá o mesmo conjunto de aplicativos instalados no mesmo local e cada arquivo. lnk será válido para todos os dispositivos dos usuários.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-223">UE-V will only support removing the .lnk file type from the exclusion list in the RDS and VDI scenarios, where every user’s device will have the same set of applications installed to the same location and every .lnk file is valid for all the users’ devices.</span></span> <span data-ttu-id="dbcb3-224">Por exemplo, o UE-V não oferece suporte aos dois cenários a seguir, porque o resultado da rede será que o atalho será válido em um, mas não em todos os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-224">For example, UE-V would not currently support the following 2 scenarios, because the net result will be that the shortcut will be valid on one but not all devices.</span></span>

-   <span data-ttu-id="dbcb3-225">Se um usuário tiver um aplicativo instalado em um dispositivo com arquivos. lnk habilitados e o mesmo aplicativo nativo instalado em outro dispositivo em uma raiz de instalação diferente com arquivos. lnk habilitados.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-225">If a user has an application installed on one device with .lnk files enabled and the same native application installed on another device to a different installation root with .lnk files enabled.</span></span>

-   <span data-ttu-id="dbcb3-226">Se um usuário tiver um aplicativo instalado em um dispositivo, mas não outro com arquivos. lnk habilitados.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-226">If a user has an application installed on one device but not another with .lnk files enabled.</span></span>



**<span data-ttu-id="dbcb3-227">Importante</span><span class="sxs-lookup"><span data-stu-id="dbcb3-227">Important</span></span>**  
<span data-ttu-id="dbcb3-228">Este tópico descreve como alterar o registro do Windows usando o editor do registro.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-228">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="dbcb3-229">Se você alterar o registro do Windows incorretamente, poderá causar sérios problemas que talvez exijam a reinstalação do Windows.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-229">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="dbcb3-230">Você deve fazer uma cópia de backup dos arquivos do registro (System. dat e User. dat) antes de alterar o registro.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-230">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="dbcb3-231">A Microsoft não pode garantir que os problemas que podem ocorrer quando você alterar o registro possam ser resolvidos.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-231">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="dbcb3-232">Altere o registro por sua conta e risco.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-232">Change the registry at your own risk.</span></span>



<span data-ttu-id="dbcb3-233">Usando o editor de registro da Microsoft (regedit.exe), navegue até **HKEY \ _LOCAL \ _MACHINE**  \\  **software**  \\  **Microsoft**  \\  **UEV**  \\  **Agent**  \\  **Configuration**  \\  **ExcludedFileTypes** e remova **. lnk** dos tipos de arquivo excluídos.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-233">Using the Microsoft Registry Editor (regedit.exe), navigate to **HKEY\_LOCAL\_MACHINE** \\ **Software** \\ **Microsoft** \\ **UEV** \\ **Agent** \\ **Configuration** \\ **ExcludedFileTypes** and remove **.lnk** from the excluded file types.</span></span>

**<span data-ttu-id="dbcb3-234">Configurar outra solução de gerenciamento de perfil do usuário (UPM) para a abordagem do App-V</span><span class="sxs-lookup"><span data-stu-id="dbcb3-234">Configure other User Profile Management (UPM) solution for App-V Approach</span></span>**

<span data-ttu-id="dbcb3-235">A expectativa em um ambiente stateful é que uma solução UPM é implementada e pode dar suporte à persistência de dados de usuário entre sessões e entre logons.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-235">The expectation in a stateful environment is that a UPM solution is implemented and can support persistence of user data across sessions and between logins.</span></span>

<span data-ttu-id="dbcb3-236">Os requisitos para a solução UPM são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-236">The requirements for the UPM solution are as follows.</span></span>

<span data-ttu-id="dbcb3-237">Para habilitar uma experiência de logon otimizada, por exemplo, a abordagem App-V 5,0 para o usuário, a solução deve ser capaz de:</span><span class="sxs-lookup"><span data-stu-id="dbcb3-237">To enable an optimized login experience, for example the App-V 5.0 approach for the user, the solution must be capable of:</span></span>

-   <span data-ttu-id="dbcb3-238">Persistir as integrações de usuário abaixo, como parte do perfil do usuário/pessoa.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-238">Persisting the below user integrations as part of the user profile/persona.</span></span>

-   <span data-ttu-id="dbcb3-239">Disparar uma sincronização de perfil de usuário no logon (ou início do aplicativo), que pode garantir que todas as integrações de usuário sejam aplicadas antes de iniciar a publicação/atualização ou,</span><span class="sxs-lookup"><span data-stu-id="dbcb3-239">Triggering a user profile sync on login (or application start), which can guarantee that all user integrations are applied before publishing/refresh begin, or,</span></span>

-   <span data-ttu-id="dbcb3-240">Anexar e desanexar um disco de perfil de usuário (UPD) ou uma tecnologia semelhante que contém as integrações do usuário.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-240">Attaching and detaching a user profile disk (UPD) or similar technology that contains the user integrations.</span></span>

-   <span data-ttu-id="dbcb3-241">Captura de alterações nos locais, que constituem as integrações do usuário antes do logoff da sessão.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-241">Capturing changes to the locations, which constitute the user integrations, prior to session logoff.</span></span>

<span data-ttu-id="dbcb3-242">Com o App-V 5,0 ao adicionar um servidor de publicação (**Add-AppvPublishingServer**), você pode configurar a sincronização, por exemplo, atualizar durante o logon e/ou depois de um intervalo de atualização especificado.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-242">With App-V 5.0 when you add a publishing server (**Add-AppvPublishingServer**) you can configure synchronization, for example refresh during log on and/or after a specified refresh interval.</span></span> <span data-ttu-id="dbcb3-243">Em ambos os casos, uma tarefa agendada é criada.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-243">In both cases a scheduled task is created.</span></span>

<span data-ttu-id="dbcb3-244">Em versões anteriores do App-V 5,0, ambas as tarefas agendadas eram configuradas usando um VBScript que iniciaria o usuário e a atualização global.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-244">In previous versions of App-V 5.0, both scheduled tasks were configured using a VBScript that would initiate the user and global refresh.</span></span> <span data-ttu-id="dbcb3-245">Com o pacote de hotfix 4 para Application Virtualization 5,0 SP2, a atualização do usuário durante o logon é iniciada pela **SyncAppvPublishingServer.exe**.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-245">With Hotfix Package 4 for Application Virtualization 5.0 SP2 the user refresh on log on is initiated by **SyncAppvPublishingServer.exe**.</span></span> <span data-ttu-id="dbcb3-246">Essa alteração foi introduzida para fornecer um processo de gatilho às soluções do UPM.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-246">This change was introduced to provide UPM solutions a trigger process.</span></span> <span data-ttu-id="dbcb3-247">Esse processo atrasará a publicação/Refresh para permitir que a solução UPM aplique as integrações do usuário.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-247">This process will delay the publish /refresh to allow the UPM solution to apply the user integrations.</span></span> <span data-ttu-id="dbcb3-248">Ele será encerrado quando a publicação/atualização for concluída.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-248">It will exit once the publishing/refresh is complete.</span></span>

**<span data-ttu-id="dbcb3-249">Integrações do usuário</span><span class="sxs-lookup"><span data-stu-id="dbcb3-249">User Integrations</span></span>**

<span data-ttu-id="dbcb3-250">Registro – HKEY \ _CURRENT \ _USER</span><span class="sxs-lookup"><span data-stu-id="dbcb3-250">Registry – HKEY\_CURRENT\_USER</span></span>

-   <span data-ttu-id="dbcb3-251">Caminho-Software\\Classes</span><span class="sxs-lookup"><span data-stu-id="dbcb3-251">Path - Software\\Classes</span></span>

    <span data-ttu-id="dbcb3-252">Exclude: configurações locais, ActivatableClasses, AppX \ \*</span><span class="sxs-lookup"><span data-stu-id="dbcb3-252">Exclude: Local Settings, ActivatableClasses, AppX\*</span></span>

-   <span data-ttu-id="dbcb3-253">Caminho-Software\\Microsoft\\AppV</span><span class="sxs-lookup"><span data-stu-id="dbcb3-253">Path - Software\\Microsoft\\AppV</span></span>

-   <span data-ttu-id="dbcb3-254">Caminhos de caminho Software\\Microsoft\\Windows\\CurrentVersion\\App</span><span class="sxs-lookup"><span data-stu-id="dbcb3-254">Path- Software\\Microsoft\\Windows\\CurrentVersion\\App Paths</span></span>

**<span data-ttu-id="dbcb3-255">Locais de arquivos</span><span class="sxs-lookup"><span data-stu-id="dbcb3-255">File Locations</span></span>**

-   <span data-ttu-id="dbcb3-256">Root – "variável de ambiente" APPDATA</span><span class="sxs-lookup"><span data-stu-id="dbcb3-256">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="dbcb3-257">Caminho – Microsoft\\AppV\\Client\\Catalog</span><span class="sxs-lookup"><span data-stu-id="dbcb3-257">Path – Microsoft\\AppV\\Client\\Catalog</span></span>

-   <span data-ttu-id="dbcb3-258">Root – "variável de ambiente" APPDATA</span><span class="sxs-lookup"><span data-stu-id="dbcb3-258">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="dbcb3-259">Caminho – Microsoft\\AppV\\Client\\Integration</span><span class="sxs-lookup"><span data-stu-id="dbcb3-259">Path – Microsoft\\AppV\\Client\\Integration</span></span>

-   <span data-ttu-id="dbcb3-260">Root – "variável de ambiente" APPDATA</span><span class="sxs-lookup"><span data-stu-id="dbcb3-260">Root – “Environment Variable” APPDATA</span></span>

    <span data-ttu-id="dbcb3-261">Path-Microsoft\\Windows\\Start Menu\\Programs</span><span class="sxs-lookup"><span data-stu-id="dbcb3-261">Path - Microsoft\\Windows\\Start Menu\\Programs</span></span>

-   <span data-ttu-id="dbcb3-262">(Para manter todos os atalhos da área de trabalho, virtuais e não virtuais)</span><span class="sxs-lookup"><span data-stu-id="dbcb3-262">(To persist all desktop shortcuts, virtual and non-virtual)</span></span>

    <span data-ttu-id="dbcb3-263">Root-"KnownFolder" {B4BFCC3A-DB2C-424C-B029-7FE99A87C641} filemask-\ \*. lnk</span><span class="sxs-lookup"><span data-stu-id="dbcb3-263">Root - “KnownFolder” {B4BFCC3A-DB2C-424C-B029-7FE99A87C641}FileMask - \*.lnk</span></span>

**<span data-ttu-id="dbcb3-264">Microsoft User Experience Virtualization (UE-V)</span><span class="sxs-lookup"><span data-stu-id="dbcb3-264">Microsoft User Experience Virtualization (UE-V)</span></span>**

<span data-ttu-id="dbcb3-265">Além disso, recomendamos usar o Microsoft User Experience Virtualization (UE-V) para capturar e centralizar as configurações do aplicativo e as configurações do sistema operacional do Windows para um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-265">Additionally, we recommend using Microsoft User Experience Virtualization (UE-V) to capture and centralize application settings and Windows operating system settings for a specific user.</span></span> <span data-ttu-id="dbcb3-266">Essas configurações são aplicadas aos diferentes computadores que são acessados pelo usuário, incluindo computadores de mesa, laptops e sessões do Virtual Desktop Infrastructure (VDI).</span><span class="sxs-lookup"><span data-stu-id="dbcb3-266">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span>

<span data-ttu-id="dbcb3-267">Para obter mais informações, consulte [introdução ao User Experience Virtualization 1,0](https://technet.microsoft.com/library/jj680015.aspx) e [compartilhamento de configurações modelos de local com a Galeria de modelos UE-V](https://technet.microsoft.com/library/jj679972.aspx).</span><span class="sxs-lookup"><span data-stu-id="dbcb3-267">For more information see [Getting Started With User Experience Virtualization 1.0](https://technet.microsoft.com/library/jj680015.aspx) and [Sharing Settings Location Templates with the UE-V Template Gallery](https://technet.microsoft.com/library/jj679972.aspx).</span></span>

### <a href="" id="bkmk-uewt"></a><span data-ttu-id="dbcb3-268">Orientação de experiência do usuário</span><span class="sxs-lookup"><span data-stu-id="dbcb3-268">User Experience Walk-through</span></span>

<span data-ttu-id="dbcb3-269">Veja a seguir uma orientação passo a passo sobre as operações do App-V e do UPM e as expectativas que os usuários devem esperar.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-269">This following is a step-by-step walk-through of the App-V and UPM operations and the expectations users should expect.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dbcb3-270">Otimizado para desempenho</span><span class="sxs-lookup"><span data-stu-id="dbcb3-270">Optimized for Performance</span></span></th>
<th align="left"><span data-ttu-id="dbcb3-271">Otimizado para armazenamento</span><span class="sxs-lookup"><span data-stu-id="dbcb3-271">Optimized for Storage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dbcb3-272">Após implementar essa abordagem no ambiente VDI/RDSH, no primeiro logon,</span><span class="sxs-lookup"><span data-stu-id="dbcb3-272">After implementing this approach in the VDI/RDSH environment, on first login,</span></span></p>
<ul>
<li><p><span data-ttu-id="dbcb3-273">Opera Uma publicação/atualização do usuário é iniciada.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-273">(Operation) A user-publishing/refresh is initiated.</span></span> <span data-ttu-id="dbcb3-274">Gestão Se esta for a primeira vez que um usuário publicou aplicativos virtuais (por exemplo, não persistente), isso vai pegar a duração normal de uma publicação/atualização.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-274">(Expectation) If this is the first time a user has published virtual applications (e.g. non-persistent), this will take the usual duration of a publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-275">Opera Após a publicação/atualização, a solução UPM captura as integrações do usuário.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-275">(Operation) After the publishing/refresh, the UPM solution captures the user integrations.</span></span> <span data-ttu-id="dbcb3-276">Gestão Dependendo de como a solução UPM está configurada, isso pode ocorrer como parte do processo de logoff.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-276">(Expectation) Depending on how the UPM solution is configured, this may occur as part of the logoff process.</span></span> <span data-ttu-id="dbcb3-277">Isso fará com que a sobrecarga e a sobrecarga semelhantes sejam mantidas no estado do usuário.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-277">This will incur the same/similar overhead as persisting the user state.</span></span></p></li>
</ul>
<p><span data-ttu-id="dbcb3-278">Em logons subsequentes:</span><span class="sxs-lookup"><span data-stu-id="dbcb3-278">On subsequent logins:</span></span></p>
<ul>
<li><p><span data-ttu-id="dbcb3-279">Opera UPM solução aplica as integrações do usuário ao sistema antes de publicação/atualização.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-279">(Operation) UPM solution applies the user integrations to the system prior to publishing/refresh.</span></span></p>
<p><span data-ttu-id="dbcb3-280">Gestão Haverá atalhos presentes na área de trabalho ou no menu Iniciar, que funcionam imediatamente.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-280">(Expectation) There will be shortcuts present on the desktop, or in the start menu, which work immediately.</span></span> <span data-ttu-id="dbcb3-281">Quando a publicação/atualização é concluída (ou seja, as titularidades do pacote são alteradas), alguns podem ficar ausentes.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-281">When the publishing/refresh completes (i.e., package entitlements change), some may go away.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-282">Opera A publicação/atualização processará operações de cancelamento e publicação de alterações nos direitos do pacote do usuário.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-282">(Operation) Publishing/refresh will process un-publish and publish operations for changes in user package entitlements.</span></span> <span data-ttu-id="dbcb3-283">Gestão Se não houver nenhuma alteração de direito, o publishing1 será concluído em segundos.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-283">(Expectation) If there are no entitlement changes, publishing1 will complete in seconds.</span></span> <span data-ttu-id="dbcb3-284">Caso contrário, a publicação/atualização será aumentada em relação ao número e à complexidade \* dos aplicativos virtuais</span><span class="sxs-lookup"><span data-stu-id="dbcb3-284">Otherwise, the publishing/refresh will increase relative to the number and complexity\* of virtual applications</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-285">Opera A solução UPM capturará as integrações do usuário novamente no logoff.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-285">(Operation) UPM solution will capture user integrations again at logoff.</span></span> <span data-ttu-id="dbcb3-286">Gestão Mesmo que a seção anterior.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-286">(Expectation) Same as previous.</span></span></p></li>
</ul>
<p><span data-ttu-id="dbcb3-287">¹ a operação de publicação ( <strong> publicar-AppVClientPackage </strong> ) adiciona entradas ao catálogo do usuário, mapeia a qualificação ao usuário, identifica o repositório local e termina ao completar qualquer etapa de integração.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-287">¹ The publishing operation (<strong>Publish-AppVClientPackage</strong>) adds entries to the user catalog, maps entitlement to the user, identifies the local store, and finishes by completing any integration steps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dbcb3-288">Após implementar essa abordagem no ambiente VDI/RDSH, no primeiro logon,</span><span class="sxs-lookup"><span data-stu-id="dbcb3-288">After implementing this approach in the VDI/RDSH environment, on first login,</span></span></p>
<ul>
<li><p><span data-ttu-id="dbcb3-289">Opera Uma publicação/atualização do usuário é iniciada.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-289">(Operation) A user-publishing/refresh is initiated.</span></span> <span data-ttu-id="dbcb3-290">Gestão</span><span class="sxs-lookup"><span data-stu-id="dbcb3-290">(Expectation)</span></span></p>
<ul>
<li><p><span data-ttu-id="dbcb3-291">Se esta for a primeira vez que um usuário publicou aplicativos virtuais (por exemplo, não persistente), isso vai pegar a duração normal de uma publicação/atualização.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-291">If this is the first time a user has published virtual applications (e.g., non-persistent), this will take the usual duration of a publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-292">Os logins iniciais e subseqüentes serão afetados pela pré-configuração dos pacotes (adicionar/atualizar).</span><span class="sxs-lookup"><span data-stu-id="dbcb3-292">First and subsequent logins will be impacted by pre-configuring of packages (add/refresh).</span></span></p>
<p></p></li>
</ul></li>
<li><p><span data-ttu-id="dbcb3-293">Opera Após a publicação/atualização, a solução UPM captura as integrações do usuário.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-293">(Operation) After the publishing/refresh, the UPM solution captures the user integrations.</span></span> <span data-ttu-id="dbcb3-294">Gestão Dependendo de como a solução UPM está configurada, isso pode ocorrer como parte do processo de logoff.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-294">(Expectation) Depending on how the UPM solution is configured, this may occur as part of the logoff process.</span></span> <span data-ttu-id="dbcb3-295">Isso fará com que a sobrecarga e a sobrecarga semelhantes sejam mantidas no estado do usuário</span><span class="sxs-lookup"><span data-stu-id="dbcb3-295">This will incur the same/similar overhead as persisting the user state</span></span></p></li>
</ul>
<p><span data-ttu-id="dbcb3-296">Em logons subsequentes:</span><span class="sxs-lookup"><span data-stu-id="dbcb3-296">On subsequent logins:</span></span></p>
<ul>
<li><p><span data-ttu-id="dbcb3-297">Opera UPM solução aplica as integrações do usuário ao sistema antes de publicação/atualização.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-297">(Operation) UPM solution applies the user integrations to the system prior to publishing/refresh.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-298">Opera Adicionar/atualizar deve pré-configurar todos os aplicativos direcionados ao usuário.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-298">(Operation) Add/refresh must pre-configure all user targeted applications.</span></span> <span data-ttu-id="dbcb3-299">Gestão</span><span class="sxs-lookup"><span data-stu-id="dbcb3-299">(Expectation)</span></span></p>
<ul>
<li><p><span data-ttu-id="dbcb3-300">Isso pode aumentar o tempo para a disponibilidade do aplicativo significativamente (na ordem de 10 de segundos).</span><span class="sxs-lookup"><span data-stu-id="dbcb3-300">This may increase the time to application availability significantly (on the order of 10’s of seconds).</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-301">Isso aumentará o tempo de atualização de publicação em relação ao número e à complexidade \* dos aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-301">This will increase the publishing refresh time relative to the number and complexity\* of virtual applications.</span></span></p>
<p></p></li>
</ul></li>
<li><p><span data-ttu-id="dbcb3-302">Opera A publicação/atualização processará operações de cancelamento e publicação para alterações nos direitos do pacote de usuários.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-302">(Operation) Publishing/refresh will process un-publish and publish operations for changes to user package entitlements.</span></span></p></li>
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
<th align="left"><span data-ttu-id="dbcb3-303">Resultado</span><span class="sxs-lookup"><span data-stu-id="dbcb3-303">Outcome</span></span></th>
<th align="left"><span data-ttu-id="dbcb3-304">Resultado</span><span class="sxs-lookup"><span data-stu-id="dbcb3-304">Outcome</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="dbcb3-305">Como as integrações do usuário são completamente preservadas, não haverá nenhum trabalho por exemplo, integração para a publicação/atualização a ser concluída.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-305">Because the user integrations are entirely preserved, there will be no work for example, integration for the publishing/refresh to complete.</span></span> <span data-ttu-id="dbcb3-306">Todos os aplicativos virtuais estarão disponíveis em segundos de login.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-306">All virtual applications will be available within seconds of login.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-307">A publicação/atualização processará as alterações dos aplicativos virtuais intitulados aos usuários, que impactam a experiência.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-307">The publishing/refresh will process changes to the users entitled virtual applications which impacts the experience.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="dbcb3-308">Como o Adicionar/atualizar deve reconfigurar todos os aplicativos virtuais para a VM, o tempo de atualização de publicação em todos os logins será estendido.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-308">Because the add/refresh must re-configure all the virtual applications to the VM, the publishing refresh time on every login will be extended.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-plc"></a><span data-ttu-id="dbcb3-309">Impacto no ciclo de vida do pacote</span><span class="sxs-lookup"><span data-stu-id="dbcb3-309">Impact to Package Life Cycle</span></span>

<span data-ttu-id="dbcb3-310">Atualizar um pacote é um aspecto crucial do ciclo de vida do pacote.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-310">Upgrading a package is a crucial aspect of the package lifecycle.</span></span> <span data-ttu-id="dbcb3-311">Para ajudar a garantir que os usuários tenham acesso aos pacotes de aplicativos virtuais atualizados (publicados) ou rebaixados (não publicados), é recomendável atualizar a imagem base para refletir essas alterações.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-311">To help guarantee users have access to the appropriate upgraded (published) or downgraded (un-published) virtual application packages, it is recommended you update the base image to reflect these changes.</span></span> <span data-ttu-id="dbcb3-312">Para entender por que examine a seção a seguir:</span><span class="sxs-lookup"><span data-stu-id="dbcb3-312">To understand why review the following section:</span></span>

<span data-ttu-id="dbcb3-313">App-V 5,0 SP2 introduziu o conceito de Estados pendentes.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-313">App-V 5.0 SP2 introduced the concept of pending states.</span></span> <span data-ttu-id="dbcb3-314">No passado,</span><span class="sxs-lookup"><span data-stu-id="dbcb3-314">In the past,</span></span>

-   <span data-ttu-id="dbcb3-315">Se um administrador tiver alterado direitos ou criado uma nova versão de um pacote (atualizado) e durante uma publicação/atualização que o pacote estava em uso, a operação de cancelamento ou publicação, respectivamente, falharia.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-315">If an administrator changed entitlements or created a new version of a package (upgraded) and during a publishing/refresh that package was in-use, the un-publish or publish operation, respectively, would fail.</span></span>

-   <span data-ttu-id="dbcb3-316">Agora, se um pacote estiver em-uso, a operação será pendente.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-316">Now, if a package is in-use the operation will be pended.</span></span> <span data-ttu-id="dbcb3-317">As operações de cancelamento de publicação e publicação pendente serão processadas na reinicialização do serviço, ou se outro comando de publicação ou cancelamento de publicação for emitido.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-317">The un-publish and publish-pend operations will be processed on service restart or if another publish or un-publish command is issued.</span></span> <span data-ttu-id="dbcb3-318">Nesse caso, se o aplicativo virtual estiver sendo usado de outra forma, o aplicativo virtual permanecerá em um estado pendente.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-318">In the latter case, if the virtual application is in-use otherwise, the virtual application will remain in a pending state.</span></span> <span data-ttu-id="dbcb3-319">Para pacotes publicados globalmente, uma reinicialização (ou reinicialização do serviço) geralmente necessária.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-319">For globally published packages, a restart (or service restart) often needed.</span></span>

<span data-ttu-id="dbcb3-320">Em um ambiente não persistente, é improvável que estas operações pendentes sejam processadas.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-320">In a non-persistent environment, it is unlikely these pended operations will be processed.</span></span> <span data-ttu-id="dbcb3-321">As operações pendentes, por exemplo, as tarefas são capturadas em **HKEY \ _CURRENT \ _USER**  \\  **software**  \\  **Microsoft**  \\  **AppV**  \\  **Client**  \\  **PendingTasks**.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-321">The pended operations, for example tasks are captured under **HKEY\_CURRENT\_USER** \\ **Software** \\ **Microsoft** \\ **AppV** \\ **Client** \\ **PendingTasks**.</span></span> <span data-ttu-id="dbcb3-322">Embora esse local seja mantido pela solução UPM, se não for aplicado ao ambiente antes do logon, ele não será processado.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-322">Although this location is persisted by the UPM solution, if it is not applied to the environment prior to log on, it will not be processed.</span></span>

### <a href="" id="bkmk-evdi"></a><span data-ttu-id="dbcb3-323">Aprimorar a experiência com VDI por meio do ajuste de otimização de desempenho</span><span class="sxs-lookup"><span data-stu-id="dbcb3-323">Enhancing the VDI Experience through Performance Optimization Tuning</span></span>

<span data-ttu-id="dbcb3-324">A seção a seguir contém listas com informações sobre documentação e downloads da Microsoft que podem ser úteis ao otimizar seu ambiente para desempenho.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-324">The following section contains lists with information about Microsoft documentation and downloads that may be useful when optimizing your environment for performance.</span></span>

**<span data-ttu-id="dbcb3-325">Blog e script do .NET NGEN (altamente recomendado)</span><span class="sxs-lookup"><span data-stu-id="dbcb3-325">.NET NGEN Blog and Script (Highly Recommended)</span></span>**

<span data-ttu-id="dbcb3-326">Sobre a tecnologia NGEN</span><span class="sxs-lookup"><span data-stu-id="dbcb3-326">About NGEN technology</span></span>

-   [<span data-ttu-id="dbcb3-327">Como acelerar a otimização do NGEN</span><span class="sxs-lookup"><span data-stu-id="dbcb3-327">How to speed up NGEN optimization</span></span>](https://blogs.msdn.com/b/dotnet/archive/2013/08/06/wondering-why-mscorsvw-exe-has-high-cpu-usage-you-can-speed-it-up.aspx)

-   [<span data-ttu-id="dbcb3-328">Script</span><span class="sxs-lookup"><span data-stu-id="dbcb3-328">Script</span></span>](https://aka.ms/DrainNGenQueue)

**<span data-ttu-id="dbcb3-329">Funções do servidor e do servidor do Windows</span><span class="sxs-lookup"><span data-stu-id="dbcb3-329">Windows Server and Server Roles</span></span>**

<span data-ttu-id="dbcb3-330">Diretrizes de ajuste de desempenho do servidor para</span><span class="sxs-lookup"><span data-stu-id="dbcb3-330">Server Performance Tuning Guidelines for</span></span>

-   [<span data-ttu-id="dbcb3-331">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="dbcb3-331">Microsoft Windows Server 2012 R2</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn529133.aspx)

-   [<span data-ttu-id="dbcb3-332">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dbcb3-332">Microsoft Windows Server 2012</span></span>](https://download.microsoft.com/download/0/0/B/00BE76AF-D340-4759-8ECD-C80BC53B6231/performance-tuning-guidelines-windows-server-2012.docx)

-   [<span data-ttu-id="dbcb3-333">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dbcb3-333">Microsoft Windows Server 2008 R2</span></span>](https://download.microsoft.com/download/6/B/2/6B2EBD3A-302E-4553-AC00-9885BBF31E21/Perf-tun-srv-R2.docx)

**<span data-ttu-id="dbcb3-334">Funções de servidor</span><span class="sxs-lookup"><span data-stu-id="dbcb3-334">Server Roles</span></span>**

-   [<span data-ttu-id="dbcb3-335">Host de virtualização de área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="dbcb3-335">Remote Desktop Virtualization Host</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567643.aspx)

-   [<span data-ttu-id="dbcb3-336">Host da sessão da área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="dbcb3-336">Remote Desktop Session Host</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567648.aspx)

-   [<span data-ttu-id="dbcb3-337">Relevância do IIS: gerenciamento de App-V, publicação, serviços Web de relatório</span><span class="sxs-lookup"><span data-stu-id="dbcb3-337">IIS Relevance: App-V Management, Publishing, Reporting Web Services</span></span>](https://msdn.microsoft.com/library/windows/hardware/dn567678.aspx)

-   [<span data-ttu-id="dbcb3-338">Relevância de servidor de arquivos (SMB): se usado para armazenamento e entrega de conteúdo do App-V no modo SCS</span><span class="sxs-lookup"><span data-stu-id="dbcb3-338">File Server (SMB) Relevance: If used for App-V Content Storage and Delivery in SCS Mode</span></span>](https://technet.microsoft.com/library/jj134210.aspx)

**<span data-ttu-id="dbcb3-339">Orientação de ajuste de desempenho do cliente Windows (SO convidado)</span><span class="sxs-lookup"><span data-stu-id="dbcb3-339">Windows Client (Guest OS) Performance Tuning Guidance</span></span>**

-   [<span data-ttu-id="dbcb3-340">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="dbcb3-340">Microsoft Windows 7</span></span>](https://download.microsoft.com/download/E/5/7/E5783D68-160B-4366-8387-114FC3E45EB4/Performance Tuning Guidelines for Windows 7 Desktop Virtualization v1.9.docx)

-   [<span data-ttu-id="dbcb3-341">Script de otimização: (fornecido pelo suporte da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dbcb3-341">Optimization Script: (Provided by Microsoft Support)</span></span>](https://blogs.technet.com/b/jeff_stokes/archive/2012/10/15/the-microsoft-premier-field-engineer-pfe-view-on-virtual-desktop-vdi-density.aspx)

-   [<span data-ttu-id="dbcb3-342">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="dbcb3-342">Microsoft Windows 8</span></span>](https://download.microsoft.com/download/6/0/1/601D7797-A063-4FA7-A2E5-74519B57C2B4/Windows_8_VDI_Image_Client_Tuning_Guide.pdf)

-   [<span data-ttu-id="dbcb3-343">Script de otimização: (fornecido pelo suporte da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dbcb3-343">Optimization Script: (Provided by Microsoft Support)</span></span>](https://blogs.technet.com/b/jeff_stokes/archive/2013/04/09/hot-off-the-presses-get-it-now-the-windows-8-vdi-optimization-script-courtesy-of-pfe.aspx)

## <span data-ttu-id="dbcb3-344">Etapas de sequenciamento para otimizar pacotes para o desempenho de publicação</span><span class="sxs-lookup"><span data-stu-id="dbcb3-344">Sequencing Steps to Optimize Packages for Publishing Performance</span></span>


<span data-ttu-id="dbcb3-345">O App-V 5,0 e o App-V 5,0 SP2 fornecem um valor significativo em suas respectivas versões.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-345">App-V 5.0 and App-V 5.0 SP2 provide significant value in their respective releases.</span></span> <span data-ttu-id="dbcb3-346">Vários recursos facilitam novos cenários ou habilitam novos cenários de implantação de cliente.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-346">Several features facilitate new scenarios or enabled new customer deployment scenarios.</span></span> <span data-ttu-id="dbcb3-347">Esses recursos seguintes podem afetar o desempenho das operações de publicação e inicialização.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-347">These following features can impact the performance of the publishing and launch operations.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dbcb3-348">Etapa</span><span class="sxs-lookup"><span data-stu-id="dbcb3-348">Step</span></span></th>
<th align="left"><span data-ttu-id="dbcb3-349">Consideração</span><span class="sxs-lookup"><span data-stu-id="dbcb3-349">Consideration</span></span></th>
<th align="left"><span data-ttu-id="dbcb3-350">Benefícios</span><span class="sxs-lookup"><span data-stu-id="dbcb3-350">Benefits</span></span></th>
<th align="left"><span data-ttu-id="dbcb3-351">Compensações</span><span class="sxs-lookup"><span data-stu-id="dbcb3-351">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dbcb3-352">Nenhum bloco de recursos 1 (FB1, também conhecido como principal FB)</span><span class="sxs-lookup"><span data-stu-id="dbcb3-352">No Feature Block 1 (FB1, also known as Primary FB)</span></span></p></td>
<td align="left"><p><span data-ttu-id="dbcb3-353">Nenhuma FB1 significa que o aplicativo será iniciado imediatamente e a falha de fluxo (o aplicativo exige arquivo, DLL e deve ser puxado pela rede) durante a inicialização. Se houver limitações de rede, o FB1 irá:</span><span class="sxs-lookup"><span data-stu-id="dbcb3-353">No FB1 means the application will launch immediately and stream fault (application requires file, DLL and must pull down over the network) during launch.If there are network limitations, FB1 will:</span></span></p>
<ul>
<li><p><span data-ttu-id="dbcb3-354">Reduza o número de falhas de fluxo e largura de banda de rede usada quando você inicia um aplicativo pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-354">Reduce the number of stream faults and network bandwidth used when you launch an application for the first time.</span></span></p></li>
<li><p><span data-ttu-id="dbcb3-355">Atrasar o lançamento até que todo o FB1 tenha sido transmitido.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-355">Delay launch until the entire FB1 has been streamed.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="dbcb3-356">A falha do fluxo diminui o tempo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-356">Stream faulting decreases the launch time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dbcb3-357">Os pacotes de aplicativos virtuais com o FB1 configurado precisarão ser novamente sequenciados.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-357">Virtual application packages with FB1 configured will need to be re-sequenced.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="dbcb3-358">Removendo FB1</span><span class="sxs-lookup"><span data-stu-id="dbcb3-358">Removing FB1</span></span>

<span data-ttu-id="dbcb3-359">Remover o FB1 não exige o instalador do aplicativo original.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-359">Removing FB1 does not require the original application installer.</span></span> <span data-ttu-id="dbcb3-360">Depois de concluir as etapas a seguir, é recomendável que você reverta o computador que executa o sequenciador para um instantâneo limpo.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-360">After completing the following steps, it is suggested that you revert the computer running the sequencer to a clean snapshot.</span></span>

<span data-ttu-id="dbcb3-361">**Interface do usuário do sequenciador** -crie um novo pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-361">**Sequencer UI** - Create a New Virtual Application Package.</span></span>

1.  <span data-ttu-id="dbcb3-362">Conclua as etapas de sequenciamento para personalizar- &gt; streaming.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-362">Complete the sequencing steps up to Customize -&gt; Streaming.</span></span>

2.  <span data-ttu-id="dbcb3-363">Na etapa de streaming, não selecione **otimizar o pacote para implantação em redes lentas ou não confiáveis**.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-363">At the Streaming step, do not select **Optimize the package for deployment over slow or unreliable network**.</span></span>

3.  <span data-ttu-id="dbcb3-364">Se desejar, vá para o **sistema operacional de destino**.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-364">If desired, move on to **Target OS**.</span></span>

**<span data-ttu-id="dbcb3-365">Modificar um pacote de aplicativo virtual existente</span><span class="sxs-lookup"><span data-stu-id="dbcb3-365">Modify an Existing Virtual Application Package</span></span>**

1.  <span data-ttu-id="dbcb3-366">Conclua as etapas de sequenciamento para transmitir.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-366">Complete the sequencing steps up to Streaming.</span></span>

2.  <span data-ttu-id="dbcb3-367">Não selecione **otimizar o pacote para implantação em uma rede lenta ou não confiável**.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-367">Do not select **Optimize the package for deployment over a slow or unreliable network**.</span></span>

3.  <span data-ttu-id="dbcb3-368">Mover para **criar pacote**.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-368">Move to **Create Package**.</span></span>

<span data-ttu-id="dbcb3-369">**PowerShell** -atualize um pacote de aplicativo virtual existente.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-369">**PowerShell** - Update an Existing Virtual Application Package.</span></span>

1.  <span data-ttu-id="dbcb3-370">Abra uma sessão do PowerShell com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-370">Open an elevated PowerShell session.</span></span>

2.  <span data-ttu-id="dbcb3-371">Import-Module **appvsequencer**.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-371">Import-module **appvsequencer**.</span></span>

3.  <span data-ttu-id="dbcb3-372">**Update-AppvSequencerPackage**  -  **AppvPackageFilePath**</span><span class="sxs-lookup"><span data-stu-id="dbcb3-372">**Update-AppvSequencerPackage** - **AppvPackageFilePath**</span></span>

    <span data-ttu-id="dbcb3-373">"C:\\Packages\\MyPackage.appv"-instalador</span><span class="sxs-lookup"><span data-stu-id="dbcb3-373">"C:\\Packages\\MyPackage.appv" -Installer</span></span>

    <span data-ttu-id="dbcb3-374">"C:\\PackageInstall\\PackageUpgrade.exe empty.exe"-OutputPath</span><span class="sxs-lookup"><span data-stu-id="dbcb3-374">"C:\\PackageInstall\\PackageUpgrade.exe empty.exe" -OutputPath</span></span>

    <span data-ttu-id="dbcb3-375">"C:\\UpgradedPackages"</span><span class="sxs-lookup"><span data-stu-id="dbcb3-375">"C:\\UpgradedPackages"</span></span>

    **<span data-ttu-id="dbcb3-376">Observação</span><span class="sxs-lookup"><span data-stu-id="dbcb3-376">Note</span></span>**  
    <span data-ttu-id="dbcb3-377">Esse cmdlet requer um arquivo executável (. exe) ou um arquivo em lotes (. bat).</span><span class="sxs-lookup"><span data-stu-id="dbcb3-377">This cmdlet requires an executable (.exe) or batch file (.bat).</span></span> <span data-ttu-id="dbcb3-378">Você deve fornecer um arquivo executável ou arquivo em lotes vazio (não há nada).</span><span class="sxs-lookup"><span data-stu-id="dbcb3-378">You must provide an empty (does nothing) executable or batch file.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dbcb3-379">Etapa</span><span class="sxs-lookup"><span data-stu-id="dbcb3-379">Step</span></span></th>
<th align="left"><span data-ttu-id="dbcb3-380">Conhecer</span><span class="sxs-lookup"><span data-stu-id="dbcb3-380">Considerations</span></span></th>
<th align="left"><span data-ttu-id="dbcb3-381">Benefícios</span><span class="sxs-lookup"><span data-stu-id="dbcb3-381">Benefits</span></span></th>
<th align="left"><span data-ttu-id="dbcb3-382">Compensações</span><span class="sxs-lookup"><span data-stu-id="dbcb3-382">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dbcb3-383">Nenhuma instalação do SXS na publicação (pré-instalação assemblies SxS)</span><span class="sxs-lookup"><span data-stu-id="dbcb3-383">No SXS Install at Publish (Pre-Install SxS assemblies)</span></span></p></td>
<td align="left"><p><span data-ttu-id="dbcb3-384">Os pacotes de aplicativos virtuais não precisam ser seqüenciados novamente.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-384">Virtual Application packages do not need to be re-sequenced.</span></span> <span data-ttu-id="dbcb3-385">Os assemblies SxS podem permanecer no pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-385">SxS Assemblies can remain in the virtual application package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dbcb3-386">As dependências do assembly SxS não serão instaladas no momento da publicação.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-386">The SxS Assembly dependencies will not install at publishing time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dbcb3-387">As dependências de assembly SxS devem ser pré-instaladas.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-387">SxS Assembly dependencies must be pre-installed.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="dbcb3-388">Criando um novo pacote de aplicativo virtual no sequenciador</span><span class="sxs-lookup"><span data-stu-id="dbcb3-388">Creating a new virtual application package on the sequencer</span></span>

<span data-ttu-id="dbcb3-389">Se, durante o monitoramento do sequenciador, um assembly SxS (como um VC + + Runtime) for instalado como parte da instalação de um aplicativo, o assembly SxS será detectado e incluído no pacote automaticamente.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-389">If, during sequencer monitoring, an SxS Assembly (such as a VC++ Runtime) is installed as part of an application’s installation, SxS Assembly will be automatically detected and included in the package.</span></span> <span data-ttu-id="dbcb3-390">O administrador será notificado e terá a opção de excluir o assembly SxS.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-390">The administrator will be notified and will have the option to exclude the SxS Assembly.</span></span>

<span data-ttu-id="dbcb3-391">**Lado do cliente**:</span><span class="sxs-lookup"><span data-stu-id="dbcb3-391">**Client Side**:</span></span>

<span data-ttu-id="dbcb3-392">Ao publicar um pacote de aplicativo virtual, o cliente do App-V 5,0 SP2 detectará se uma dependência SxS necessária já está instalada.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-392">When publishing a virtual application package, the App-V 5.0 SP2 Client will detect if a required SxS dependency is already installed.</span></span> <span data-ttu-id="dbcb3-393">Se a dependência não estiver disponível no computador e estiver incluída no pacote, um programa tradicional do Windows Installer (.\*\* MSI\*\*) a instalação do assembly SxS será iniciada.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-393">If the dependency is unavailable on the computer and it is included in the package, a traditional Windows Installer (.**msi**) installation of the SxS assembly will be initiated.</span></span> <span data-ttu-id="dbcb3-394">Conforme documentado anteriormente, basta instalar a dependência no computador que está executando o cliente para garantir que a instalação do Windows Installer (. msi) não ocorra.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-394">As previously documented, simply install the dependency on the computer running the client to ensure that the Windows Installer (.msi) installation will not occur.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dbcb3-395">Etapa</span><span class="sxs-lookup"><span data-stu-id="dbcb3-395">Step</span></span></th>
<th align="left"><span data-ttu-id="dbcb3-396">Conhecer</span><span class="sxs-lookup"><span data-stu-id="dbcb3-396">Considerations</span></span></th>
<th align="left"><span data-ttu-id="dbcb3-397">Benefícios</span><span class="sxs-lookup"><span data-stu-id="dbcb3-397">Benefits</span></span></th>
<th align="left"><span data-ttu-id="dbcb3-398">Compensações</span><span class="sxs-lookup"><span data-stu-id="dbcb3-398">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dbcb3-399">Empregar arquivos de configuração dinâmicos de forma seletiva</span><span class="sxs-lookup"><span data-stu-id="dbcb3-399">Selectively Employ Dynamic Configuration files</span></span></p></td>
<td align="left"><p><span data-ttu-id="dbcb3-400">O cliente App-V 5,0 deve analisar e processar esses arquivos de configuração dinâmica.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-400">The App-V 5.0 client must parse and process these Dynamic Configuration files.</span></span></p>
<p><span data-ttu-id="dbcb3-401">Fique atento ao tamanho e à complexidade (execução de script, inclusões de VREG/exclusões) do arquivo.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-401">Be conscious of size and complexity (script execution, VREG inclusions/exclusions) of the file.</span></span></p>
<p><span data-ttu-id="dbcb3-402">Muitos pacotes de aplicativos virtuais podem já ter arquivos de configurações dinâmicas específicos do computador ou do computador.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-402">Numerous virtual application packages may already have User- or computer–specific dynamic configurations files.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dbcb3-403">Os tempos de publicação serão aprimorados se esses arquivos forem usados seletivamente ou não.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-403">Publishing times will improve if these files are used selectively or not at all.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dbcb3-404">Os pacotes de aplicativos virtuais precisariam ser reconfigurados individualmente ou por meio do console de gerenciamento do App-V Server para remover arquivos de configuração dinâmico associados.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-404">Virtual application packages would need to be reconfigured individually or via the App-V server management console to remove associated Dynamic Configuration files.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="dbcb3-405">Desativando uma configuração dinâmica usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="dbcb3-405">Disabling a Dynamic Configuration using Powershell</span></span>

-   <span data-ttu-id="dbcb3-406">Para pacotes já publicados, você pode usar `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` sem</span><span class="sxs-lookup"><span data-stu-id="dbcb3-406">For already published packages, you can use `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` without</span></span>

    <span data-ttu-id="dbcb3-407">Parâmetro **-DynamicDeploymentConfiguration**</span><span class="sxs-lookup"><span data-stu-id="dbcb3-407">**-DynamicDeploymentConfiguration** parameter</span></span>

-   <span data-ttu-id="dbcb3-408">Da mesma forma, ao adicionar novos pacotes usando `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv` , não use o</span><span class="sxs-lookup"><span data-stu-id="dbcb3-408">Similarly, when adding new packages using `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv`, do not use the</span></span>

    <span data-ttu-id="dbcb3-409">**-Parâmetro DynamicDeploymentConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="dbcb3-409">**-DynamicDeploymentConfiguration** parameter.</span></span>

<span data-ttu-id="dbcb3-410">Para obter a documentação sobre como aplicar uma configuração dinâmica, consulte:</span><span class="sxs-lookup"><span data-stu-id="dbcb3-410">For documentation on How to Apply a Dynamic Configuration, see:</span></span>

-   [<span data-ttu-id="dbcb3-411">Como aplicar o arquivo de configuração do usuário usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="dbcb3-411">How to Apply the User Configuration File by Using PowerShell</span></span>](how-to-apply-the-user-configuration-file-by-using-powershell.md)

-   [<span data-ttu-id="dbcb3-412">Como aplicar o arquivo de configuração da implantação usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="dbcb3-412">How to Apply the Deployment Configuration File by Using PowerShell</span></span>](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="dbcb3-413">Etapa</span><span class="sxs-lookup"><span data-stu-id="dbcb3-413">Step</span></span></th>
<th align="left"><span data-ttu-id="dbcb3-414">Conhecer</span><span class="sxs-lookup"><span data-stu-id="dbcb3-414">Considerations</span></span></th>
<th align="left"><span data-ttu-id="dbcb3-415">Benefícios</span><span class="sxs-lookup"><span data-stu-id="dbcb3-415">Benefits</span></span></th>
<th align="left"><span data-ttu-id="dbcb3-416">Compensações</span><span class="sxs-lookup"><span data-stu-id="dbcb3-416">Tradeoffs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="dbcb3-417">Conta para a execução de script síncrono durante o ciclo de vida do pacote.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-417">Account for Synchronous Script Execution during Package Lifecycle.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dbcb3-418">Se o material de apoio do script estiver incorporado no pacote, o Add (PowerShell) pode ser significativamente mais lento.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-418">If script collateral is embedded in the package, Add (Powershell) may be significantly slower.</span></span></p>
<p><span data-ttu-id="dbcb3-419">A execução de scripts durante a inicialização do aplicativo virtual (StartVirtualEnvironment, StartProcess) e/ou adicionar + publicar afetará o desempenho percebido durante uma ou mais dessas operações do ciclo de vida.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-419">Running of scripts during virtual application launch (StartVirtualEnvironment, StartProcess) and/or Add+Publish will impact the perceived performance during one or more of these lifecycle operations.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dbcb3-420">O uso de scripts assíncronos (não bloqueados) garantirá que as operações do ciclo de vida sejam concluídas com eficiência.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-420">Use of Asynchronous (Non-Blocking) Scripts will ensure that the lifecycle operations complete efficiently.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dbcb3-421">Esta etapa requer o conhecimento funcional de todos os pacotes de aplicativos virtuais com o material de script incorporado, que tem arquivos de configurações dinâmicos associados e a referência e execução de scripts de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-421">This step requires working knowledge of all virtual application packages with embedded script collateral, which have associated dynamic configurations files and which reference and run scripts synchronously.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="dbcb3-422">Remover fontes virtuais estranhas do pacote.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-422">Remove Extraneous Virtual Fonts from Package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dbcb3-423">A maioria dos aplicativos investigados pela equipe do produto App-V continha um pequeno número de fontes, geralmente menor que 20.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-423">The majority of applications investigated by the App-V product team contained a small number of fonts, typically fewer than 20.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dbcb3-424">As fontes virtuais afetam o desempenho da atualização da publicação.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-424">Virtual Fonts impact publishing refresh performance.</span></span></p></td>
<td align="left"><p><span data-ttu-id="dbcb3-425">As fontes desejadas deverão ser habilitadas/instaladas nativamente.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-425">Desired fonts will need to be enabled/installed natively.</span></span> <span data-ttu-id="dbcb3-426">Para obter instruções, confira instalar ou desinstalar fontes.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-426">For instructions, see Install or uninstall fonts.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="dbcb3-427">Determinar quais fontes virtuais existem no pacote</span><span class="sxs-lookup"><span data-stu-id="dbcb3-427">Determining what virtual fonts exist in the package</span></span>

-   <span data-ttu-id="dbcb3-428">Faça uma cópia do pacote.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-428">Make a copy of the package.</span></span>

-   <span data-ttu-id="dbcb3-429">Renomear o pacote \ _copy. AppV para Package\_copy.zip</span><span class="sxs-lookup"><span data-stu-id="dbcb3-429">Rename Package\_copy.appv to Package\_copy.zip</span></span>

-   <span data-ttu-id="dbcb3-430">Abra AppxManifest.xml e localize o seguinte:</span><span class="sxs-lookup"><span data-stu-id="dbcb3-430">Open AppxManifest.xml and locate the following:</span></span>

    <span data-ttu-id="dbcb3-431">&lt;AppV: categoria de extensão = "AppV. fonts"&gt;</span><span class="sxs-lookup"><span data-stu-id="dbcb3-431">&lt;appv:Extension Category="AppV.Fonts"&gt;</span></span>

    <span data-ttu-id="dbcb3-432">&lt;AppV: fontes&gt;</span><span class="sxs-lookup"><span data-stu-id="dbcb3-432">&lt;appv:Fonts&gt;</span></span>

    <span data-ttu-id="dbcb3-433">&lt;AppV: caminho da fonte = "\ [{fonts} \] \\private\\CalibriL.ttf" DelayLoad = "true" &gt; &lt; /AppV: Font&gt;</span><span class="sxs-lookup"><span data-stu-id="dbcb3-433">&lt;appv:Font Path="\[{Fonts}\]\\private\\CalibriL.ttf" DelayLoad="true"&gt;&lt;/appv:Font&gt;</span></span>

    **<span data-ttu-id="dbcb3-434">Observação</span><span class="sxs-lookup"><span data-stu-id="dbcb3-434">Note</span></span>**  
    <span data-ttu-id="dbcb3-435">Se houver fontes marcadas como **DELAYLOAD**, elas não terão impacto na primeira inicialização.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-435">If there are fonts marked as **DelayLoad**, those will not impact first launch.</span></span>



~~~
&lt;/appv:Fonts&gt;
~~~

### <span data-ttu-id="dbcb3-436">Excluindo fontes virtuais do pacote</span><span class="sxs-lookup"><span data-stu-id="dbcb3-436">Excluding virtual fonts from the package</span></span>

<span data-ttu-id="dbcb3-437">Use o arquivo de configuração dinâmica que melhor se adapta ao escopo do usuário – configuração de implantação para todos os usuários no computador, configuração de usuário para usuários específicos ou usuários.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-437">Use the dynamic configuration file that best suits the user scope – deployment configuration for all users on computer, user configuration for specific user or users.</span></span>

-   <span data-ttu-id="dbcb3-438">Desative as fontes com a implantação ou a configuração do usuário.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-438">Disable fonts with the deployment or user configuration.</span></span>

<span data-ttu-id="dbcb3-439">Fontes</span><span class="sxs-lookup"><span data-stu-id="dbcb3-439">Fonts</span></span>

--&gt;

<span data-ttu-id="dbcb3-440">&lt;Fonts Enabled = "false"/&gt;</span><span class="sxs-lookup"><span data-stu-id="dbcb3-440">&lt;Fonts Enabled="false" /&gt;</span></span>

<span data-ttu-id="dbcb3-441">&lt;!--</span><span class="sxs-lookup"><span data-stu-id="dbcb3-441">&lt;!--</span></span>

## <a href="" id="bkmk-terms1"></a> <span data-ttu-id="dbcb3-442">Terminologia de diretrizes de desempenho do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="dbcb3-442">App-V 5.0 Performance Guidance Terminology</span></span>


<span data-ttu-id="dbcb3-443">Os termos a seguir são usados para descrever os conceitos e ações relacionados à otimização de desempenho do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-443">The following terms are used when describing concepts and actions related to App-V 5.0 performance optimization.</span></span>

-   <span data-ttu-id="dbcb3-444">**Complexidade** – refere-se a uma ou mais características do pacote que podem afetar o desempenho durante a pré-configuração (**Add-AppvClientPackage**) ou integração (**Publish-AppvClientPackage**).</span><span class="sxs-lookup"><span data-stu-id="dbcb3-444">**Complexity** – Refers to the one or more package characteristics that may impact performance during pre-configure (**Add-AppvClientPackage**) or integration (**Publish-AppvClientPackage**).</span></span> <span data-ttu-id="dbcb3-445">Alguns exemplos de características são: tamanho do manifesto, número de fontes virtuais, número de arquivos.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-445">Some example characteristics are: manifest size, number of virtual fonts, number of files.</span></span>

-   <span data-ttu-id="dbcb3-446">**Desintegrar** – remove as integrações do usuário</span><span class="sxs-lookup"><span data-stu-id="dbcb3-446">**De-Integrate** – Removes the user integrations</span></span>

-   <span data-ttu-id="dbcb3-447">**Integrar novamente** – aplica as integrações do usuário.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-447">**Re-Integrate** – Applies the user integrations.</span></span>

-   <span data-ttu-id="dbcb3-448">**Não persistente, poold** – cria um computador que executa um ambiente virtual cada vez que eles fazem logon.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-448">**Non-Persistent, Pooled** – Creates a computer running a virtual environment each time they log in.</span></span>

-   <span data-ttu-id="dbcb3-449">**Persistente, pessoal** – um computador que executa um ambiente virtual que permanece igual para cada logon.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-449">**Persistent, Personal** – A computer running a virtual environment that remains the same for every login.</span></span>

-   <span data-ttu-id="dbcb3-450">**Stateful** – para este documento, sugere que as integrações do usuário são mantidas entre sessões e uma tecnologia de gerenciamento do ambiente do usuário é usada em conjunto com RDSH não persistente ou VDI.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-450">**Stateful** - For this document, implies that user integrations are persisted between sessions and a user environment management technology is used in conjunction with non-persistent RDSH or VDI.</span></span>

-   <span data-ttu-id="dbcb3-451">**Sem monitoração** de estado – representa um cenário quando nenhum estado do usuário é mantido entre as sessões.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-451">**Stateless** – Represents a scenario when no user state is persisted between sessions.</span></span>

-   <span data-ttu-id="dbcb3-452">**Gatilho** – (ou gatilhos de ação nativa).</span><span class="sxs-lookup"><span data-stu-id="dbcb3-452">**Trigger** – (or Native Action Triggers).</span></span> <span data-ttu-id="dbcb3-453">O UPM usa esses tipos de gatilhos para iniciar operações de monitoramento ou sincronização.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-453">UPM uses these types of triggers to initiate monitoring or synchronization operations.</span></span>

-   <span data-ttu-id="dbcb3-454">**Experiência do usuário** -no contexto do App-V 5,0, a experiência do usuário, quantitativomente, é a soma das seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="dbcb3-454">**User Experience** - In the context of App-V 5.0, the user experience, quantitatively, is the sum of the following parts:</span></span>

    -   <span data-ttu-id="dbcb3-455">Do ponto em que os usuários iniciam um logon quando podem manipular a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-455">From the point that users initiate a log-in to when they are able to manipulate the desktop.</span></span>

    -   <span data-ttu-id="dbcb3-456">A partir do ponto em que a área de trabalho pode ser interagindo ao ponto em que uma atualização de publicação começa (em termos do PowerShell, sincronizar) ao usar a infraestrutura de servidor completo do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-456">From the point where the desktop can be interacted with to the point a publishing refresh begins (in PowerShell terms, sync) when using the App-V 5.0 full server infrastructure.</span></span> <span data-ttu-id="dbcb3-457">Em instâncias autônomas, é quando os comandos do PowerShell **Add-AppVClientPackage** e **Publish-AppVClientPackage** são iniciados.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-457">In standalone instances, it is when the **Add-AppVClientPackage** and **Publish-AppVClientPackage Powershell** commands are initiated.</span></span>

    -   <span data-ttu-id="dbcb3-458">Do início ao término da atualização da publicação.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-458">From start to completion of the publishing refresh.</span></span> <span data-ttu-id="dbcb3-459">Em instâncias autônomas, este é o primeiro a último aplicativo virtual publicado.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-459">In standalone instances, this is the first to last virtual application published.</span></span>

    -   <span data-ttu-id="dbcb3-460">A partir do ponto em que o aplicativo virtual está disponível para ser iniciado a partir de um atalho.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-460">From the point where the virtual application is available to launch from a shortcut.</span></span> <span data-ttu-id="dbcb3-461">Como alternativa, ele é do ponto em que a associação de tipo de arquivo está registrada e iniciará um aplicativo virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-461">Alternatively, it is from the point at which the file type association is registered and will launch a specified virtual application.</span></span>

-   <span data-ttu-id="dbcb3-462">**Gerenciamento de perfil de usuário** – a abordagem controlada e estruturada para gerenciar componentes do usuário associados ao ambiente.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-462">**User Profile Management** – The controlled and structured approach to managing user components associated with the environment.</span></span> <span data-ttu-id="dbcb3-463">Por exemplo, perfis de usuário, gerenciamento de preferências e políticas, controle de aplicativos e implantação de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-463">For example, user profiles, preference and policy management, application control and application deployment.</span></span> <span data-ttu-id="dbcb3-464">Você pode usar scripts ou soluções de terceiros para configurar o ambiente conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="dbcb3-464">You can use scripting or third-party solutions configure the environment as needed.</span></span>






## <span data-ttu-id="dbcb3-465">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dbcb3-465">Related topics</span></span>


[<span data-ttu-id="dbcb3-466">Guia do administrador do Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="dbcb3-466">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)









