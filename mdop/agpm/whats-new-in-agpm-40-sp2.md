---
title: Novidades do AGPM 4.0 SP2
description: Novidades do AGPM 4.0 SP2
author: dansimp
ms.assetid: 5c0dcab4-f27d-4153-8b8e-b280b080be51
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 56369207780cf0795f16eda91f249a26270c4b47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797267"
---
# <span data-ttu-id="6e3e9-103">Novidades do AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="6e3e9-103">What's New in AGPM 4.0 SP2</span></span>


<span data-ttu-id="6e3e9-104">Este conteúdo descreve melhorias e configurações com suporte para o serviço de gerenciamento de política de grupo avançado (AGPM) 4.0 da Microsoft Pack2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="6e3e9-104">This content describes enhancements and supported configurations for Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack2 (SP2).</span></span> <span data-ttu-id="6e3e9-105">Se houver uma diferença entre esse conteúdo e outra documentação do AGPM, considere esse conteúdo autoritativo e assuma que ele substitui a outra documentação.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-105">If there is a difference between this content and other AGPM documentation, consider this content authoritative and assume that it supersedes the other documentation.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="6e3e9-106">O que há de novo</span><span class="sxs-lookup"><span data-stu-id="6e3e9-106">What’s new</span></span>


<span data-ttu-id="6e3e9-107">O AGPM 4.0 SP2 é compatível com os recursos e funcionalidades a seguir.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-107">AGPM4.0 SP2 supports the following features and functionality.</span></span>

### <span data-ttu-id="6e3e9-108">Suporte para Windows 8.1 e Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="6e3e9-108">Support for Windows8.1 and Windows Server2012 R2</span></span>

<span data-ttu-id="6e3e9-109">O AGPM 4.0 SP2 adiciona suporte para os sistemas operacionais Windows 8.1 e Windows Server2012 R2.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-109">AGPM4.0 SP2 adds support for the Windows8.1 and Windows Server2012 R2 operating systems.</span></span>

### <span data-ttu-id="6e3e9-110">Extensões novas e alteradas do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="6e3e9-110">New and changed client-side extensions</span></span>

<span data-ttu-id="6e3e9-111">As extensões do lado do cliente da política de grupo foram adicionadas ou alteradas para o AGPM para dar suporte a novas configurações de política no Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-111">Group Policy client-side extensions have been added or changed for AGPM to support new policy settings in Windows8.1.</span></span> <span data-ttu-id="6e3e9-112">Essas configurações de política permitem que os administradores de política de grupo gerenciem e controlem as configurações de política específicas do Windows 8.1 que mudam entre dois objetos de política de grupo (GPOs) ou modelos.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-112">These policy settings enable Group Policy administrators to manage and track Windows8.1–specific policy settings that change between two Group Policy Objects (GPOs) or templates.</span></span> <span data-ttu-id="6e3e9-113">Para exibir as extensões do lado do cliente, use as configurações e os relatórios de diferença disponíveis no cliente do AGPM.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-113">To view your client-side extensions, use the settings and difference reports that are available in the AGPM Client.</span></span>

<span data-ttu-id="6e3e9-114">As extensões nova e alterada do lado do cliente da política de grupo são:</span><span class="sxs-lookup"><span data-stu-id="6e3e9-114">The new and changed Group Policy client-side extensions are:</span></span>

-   <span data-ttu-id="6e3e9-115">**Especifique as configurações de pastas de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-115">**Specify Work Folders settings**.</span></span> <span data-ttu-id="6e3e9-116">Se você habilitar essa configuração de política, os administradores de ti poderão configurar pastas de trabalho para serem criadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-116">If you enable this policy setting, IT administrators can configure Work Folders to be created automatically.</span></span> <span data-ttu-id="6e3e9-117">O recurso de pastas de trabalho permite que os usuários finais sincronizem arquivos de dispositivos da área de trabalho do Windows para outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-117">The Work Folders feature enables end users to synchronize files from their Windows desktop devices to their other devices.</span></span> <span data-ttu-id="6e3e9-118">Use essa configuração de política para criar a relação de sincronização em dispositivos de um usuário final e para configurar como identificar o servidor de arquivos que armazena as pastas de trabalho do usuário.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-118">Use this policy setting to create the synchronization relationship on an end user’s devices and to configure how to identify the file server that stores the user’s Work Folders.</span></span> <span data-ttu-id="6e3e9-119">Se você marcar a caixa de seleção **autoprovisionar sincronização** , a parceria de sincronização será criada sem a entrada do usuário, e os dados começarão a ser sincronizados automaticamente com o dispositivo do usuário.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-119">If you select the **Auto provision synchronization** check box, the synchronization partnership will be created without user input, and data will automatically start synchronizing to the user’s device.</span></span> <span data-ttu-id="6e3e9-120">Se você não marcar a caixa de seleção **sincronização automática de autoprovisionar** , os usuários devem fornecer entrada para iniciar a sincronização.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-120">If you do not select the **Auto provision synchronization** check box, users must provide input to start the synchronization.</span></span>

-   <span data-ttu-id="6e3e9-121">**Forçar a configuração automática para todos os usuários**.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-121">**Force automatic setup for all users**.</span></span> <span data-ttu-id="6e3e9-122">Se você habilitar essa configuração de política, os administradores de ti poderão determinar se a parceria de pastas de trabalho será criada automaticamente em dispositivos de usuário final sem entrada de usuários finais.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-122">If you enable this policy setting, IT administrators can determine whether to create the Work Folders partnership automatically on end-user devices without input from end users.</span></span> <span data-ttu-id="6e3e9-123">Se você habilitar essa configuração de política, a sincronização será configurada de acordo com o modo como você define a configuração de política **especificar configurações de pastas de trabalho** .</span><span class="sxs-lookup"><span data-stu-id="6e3e9-123">If you enable this policy setting, the synchronization will be set up according to how you configure the **Specify Work Folders settings** policy setting.</span></span> <span data-ttu-id="6e3e9-124">Se você definir a configuração de política **forçar configuração automática para todos os usuários** como **desabilitada** ou **não configurada**, a parceria de pastas de trabalho será configurada de acordo com o modo como você define a opção de **provisionamento automático** na configuração de política **especificar configurações de pastas de trabalho** .</span><span class="sxs-lookup"><span data-stu-id="6e3e9-124">If you set the **Force automatic setup for all users** policy setting to **Disabled** or **Not configured**, the Work Folders partnership will be configured according to how you set the **Automatic Provisioning** option in the **Specify Work Folders settings** policy setting.</span></span>

<span data-ttu-id="6e3e9-125">Para obter mais informações sobre o recurso de pastas de trabalho, consulte [visão geral de pastas de trabalho](https://go.microsoft.com/fwlink/?LinkId=330444).</span><span class="sxs-lookup"><span data-stu-id="6e3e9-125">For more information about the Work Folders feature, see [Work Folders Overview](https://go.microsoft.com/fwlink/?LinkId=330444).</span></span>

### <span data-ttu-id="6e3e9-126">Feedback do cliente e pacote cumulativo de hotfix</span><span class="sxs-lookup"><span data-stu-id="6e3e9-126">Customer feedback and hotfix rollup</span></span>

<span data-ttu-id="6e3e9-127">O AGPM 4.0 SP2 inclui um pacote cumulativo de hotfixes para solucionar problemas encontrados desde o lançamento do AGPM 4.0 Service Pack1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="6e3e9-127">AGPM4.0 SP2 includes a rollup of hotfixes to address issues found since the AGPM4.0 Service Pack1 (SP1) release.</span></span> <span data-ttu-id="6e3e9-128">O AGPM 4.0 SP2 contém as mais recentes correções até e incluindo o gerenciamento avançado de política de grupo 4.0 da Microsoft 4.0 SP1 Hotfix1.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-128">AGPM4.0 SP2 contains the latest fixes up to and including Microsoft Advanced Group Policy Management4.0 SP1 Hotfix1.</span></span> <span data-ttu-id="6e3e9-129">Para obter mais informações, consulte o artigo [2873472](https://go.microsoft.com/fwlink/?LinkId=325400)da base de dados de conhecimento.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-129">For more information, see Knowledge Base article [2873472](https://go.microsoft.com/fwlink/?LinkId=325400)).</span></span>

### <span data-ttu-id="6e3e9-130">Novas extensões de política de grupo nas configurações e relatórios de diferença</span><span class="sxs-lookup"><span data-stu-id="6e3e9-130">New Group Policy extensions in settings and difference reports</span></span>

<span data-ttu-id="6e3e9-131">As novas extensões de política de grupo foram adicionadas às configurações e aos relatórios de diferença.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-131">The new Group Policy extensions have been added to the settings and difference reports.</span></span>

### <span data-ttu-id="6e3e9-132">Mudanças e suporte do instalador</span><span class="sxs-lookup"><span data-stu-id="6e3e9-132">Installer changes and support</span></span>

<span data-ttu-id="6e3e9-133">As alterações e o suporte para o instalador do AGPM 4.0 SP2 são:</span><span class="sxs-lookup"><span data-stu-id="6e3e9-133">The changes and support for the AGPM4.0 SP2 installer are:</span></span>

-   <span data-ttu-id="6e3e9-134">Se você instalar o AGPM 4.0 SP2 nos sistemas operacionais Windows 8 ou Windows Server 2012 ou posteriores, o instalador do AGPM verificará se o software de pré-requisito obrigatório (console de gerenciamento de política de grupo (GPMC) e o Microsoft .NET Framework 3.5) está instalado.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-134">If you install AGPM4.0 SP2 on the Windows 8 or Windows Server 2012 operating system or later operating systems, the AGPM installer verifies that the required prerequisite software (the Group Policy Management Console (GPMC) and the Microsoft .NET Framework3.5) is installed.</span></span> <span data-ttu-id="6e3e9-135">Se este software obrigatório não estiver instalado, a instalação do AGPM 4.0 SP2 será bloqueada.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-135">If this prerequisite software is not installed, the AGPM4.0 SP2 installation is blocked.</span></span>

-   <span data-ttu-id="6e3e9-136">Quando você instala o servidor do AGPM, a ativação do WCF, a ativação não HTTP e o serviço de ativação de processos do Windows são habilitados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-136">When you install the AGPM Server, WCF Activation, Non-HTTP Activation, and Windows Process Activation Service are automatically enabled.</span></span>

-   <span data-ttu-id="6e3e9-137">No sistema operacional do cliente WindowsVista e sistemas operacionais posteriores, baixe a versão apropriada das ferramentas de administração do sistema remoto para o sistema operacional antes de instalar o AGPM 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-137">On the WindowsVista client operating system and later operating systems, download the appropriate version of the Remote System Administration Tools for your operating system before you install AGPM4.0 SP2.</span></span>

-   <span data-ttu-id="6e3e9-138">O AGPM 4.0 SP2 dá suporte à compatibilidade com versões anteriores com sistemas operacionais compatíveis.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-138">AGPM4.0 SP2 supports backward compatibility with older supported operating systems.</span></span>

### <span data-ttu-id="6e3e9-139">Capacidade de atualizar para o AGPM 4.0 SP2 sem digitar novamente os parâmetros de configuração</span><span class="sxs-lookup"><span data-stu-id="6e3e9-139">Ability to upgrade to AGPM4.0 SP2 without reentering configuration parameters</span></span>

<span data-ttu-id="6e3e9-140">Você pode atualizar o cliente do AGPM ou o servidor do AGPM para o AGPM 4.0 SP2 sem ser solicitado a digitar novamente os parâmetros de configuração (chamado de atualização inteligente) somente do AGPM 4.0 em diante, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-140">You can upgrade the AGPM Client or AGPM Server to AGPM4.0 SP2 without being prompted to reenter configuration parameters (called the Smart Upgrade) only from AGPM4.0 onward, as shown in the following table.</span></span> <span data-ttu-id="6e3e9-141">Se você estiver atualizando para o AGPM 4.0 SP2 de outras versões do AGPM, conforme mostrado na tabela, você deve usar a atualização clássica, que exige que você reinsira os parâmetros de configuração.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-141">If you are upgrading to AGPM4.0 SP2 from other versions of AGPM, as shown in the table, you must use the Classic Upgrade, which requires you to reenter the configuration parameters.</span></span> <span data-ttu-id="6e3e9-142">Como cada versão do AGPM está associada a um sistema operacional específico, consulte [escolhendo qual versão do AGPM instalar](https://go.microsoft.com/fwlink/?LinkId=254350) e certifique-se de atualizar o sistema operacional conforme apropriado antes de atualizar o AGPM.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-142">Because each version of AGPM is associated with a particular operating system, see [Choosing Which Version of AGPM to Install](https://go.microsoft.com/fwlink/?LinkId=254350) and make sure that you upgrade your operating system as appropriate before you upgrade AGPM.</span></span>

**<span data-ttu-id="6e3e9-143">Atualizações compatíveis com o AGPM 4,0 SP2</span><span class="sxs-lookup"><span data-stu-id="6e3e9-143">AGPM 4.0 SP2 supported upgrades</span></span>**

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6e3e9-144">Versão do AGPM a partir da qual você pode atualizar</span><span class="sxs-lookup"><span data-stu-id="6e3e9-144">AGPM version from which you can upgrade</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="6e3e9-145">2,5</span><span class="sxs-lookup"><span data-stu-id="6e3e9-145">2.5</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="6e3e9-146">3,0</span><span class="sxs-lookup"><span data-stu-id="6e3e9-146">3.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="6e3e9-147">4,0</span><span class="sxs-lookup"><span data-stu-id="6e3e9-147">4.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="6e3e9-148">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="6e3e9-148">4.0 SP1</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="6e3e9-149">4,0 SP2</span><span class="sxs-lookup"><span data-stu-id="6e3e9-149">4.0 SP2</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6e3e9-150">2,5</span><span class="sxs-lookup"><span data-stu-id="6e3e9-150">2.5</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-151">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="6e3e9-151">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-152">Atualização clássica</span><span class="sxs-lookup"><span data-stu-id="6e3e9-152">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-153">Atualização clássica</span><span class="sxs-lookup"><span data-stu-id="6e3e9-153">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-154">A instalação está bloqueada</span><span class="sxs-lookup"><span data-stu-id="6e3e9-154">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-155">A instalação está bloqueada</span><span class="sxs-lookup"><span data-stu-id="6e3e9-155">Installation is blocked</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6e3e9-156">3,0</span><span class="sxs-lookup"><span data-stu-id="6e3e9-156">3.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-157">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="6e3e9-157">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-158">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="6e3e9-158">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-159">Atualização clássica</span><span class="sxs-lookup"><span data-stu-id="6e3e9-159">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-160">A instalação está bloqueada</span><span class="sxs-lookup"><span data-stu-id="6e3e9-160">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-161">A instalação está bloqueada</span><span class="sxs-lookup"><span data-stu-id="6e3e9-161">Installation is blocked</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6e3e9-162">4,0</span><span class="sxs-lookup"><span data-stu-id="6e3e9-162">4.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-163">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="6e3e9-163">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-164">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="6e3e9-164">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-165">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="6e3e9-165">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-166">Atualização inteligente</span><span class="sxs-lookup"><span data-stu-id="6e3e9-166">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-167">Atualização inteligente</span><span class="sxs-lookup"><span data-stu-id="6e3e9-167">Smart Upgrade</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6e3e9-168">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="6e3e9-168">4.0 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-169">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="6e3e9-169">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-170">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="6e3e9-170">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-171">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="6e3e9-171">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-172">Não Aplicável</span><span class="sxs-lookup"><span data-stu-id="6e3e9-172">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-173">Atualização inteligente</span><span class="sxs-lookup"><span data-stu-id="6e3e9-173">Smart Upgrade</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="6e3e9-174">Configurações compatíveis</span><span class="sxs-lookup"><span data-stu-id="6e3e9-174">Supported configurations</span></span>


<span data-ttu-id="6e3e9-175">O AGPM 4.0 SP2 dá suporte às configurações na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-175">AGPM4.0 SP2 supports the configurations in the following table.</span></span> <span data-ttu-id="6e3e9-176">Embora o AGPM dê suporte a configurações mistas, recomendamos que você execute o cliente do AGPM e o servidor do AGPM na mesma linha do sistema operacional, por exemplo, Windows 8.1 com Windows Server2012 R2, Windows 8 com Windows Server 2012 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-176">Although AGPM supports mixed configurations, we strongly recommend that you run the AGPM Client and AGPM Server on the same operating system line—for example, Windows8.1 with Windows Server2012 R2, Windows 8 with Windows Server 2012, and so on.</span></span>

**<span data-ttu-id="6e3e9-177">Configurações de política e sistemas operacionais compatíveis com o AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="6e3e9-177">AGPM4.0 SP2 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="6e3e9-178">Configurações com suporte para o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="6e3e9-178">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="6e3e9-179">Configurações com suporte para o cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="6e3e9-179">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="6e3e9-180">Suporte do AGPM</span><span class="sxs-lookup"><span data-stu-id="6e3e9-180">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6e3e9-181">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6e3e9-181">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-182">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6e3e9-182">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-183">Com suporte</span><span class="sxs-lookup"><span data-stu-id="6e3e9-183">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6e3e9-184">Windows Server2012 R2, Windows Server 2012, Windows 8.1 ou Windows 8</span><span class="sxs-lookup"><span data-stu-id="6e3e9-184">Windows Server2012 R2, Windows Server 2012, Windows8.1, or Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-185">Windows Server 2012 ou Windows 8</span><span class="sxs-lookup"><span data-stu-id="6e3e9-185">Windows Server 2012 or Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-186">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6e3e9-186">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6e3e9-187">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="6e3e9-187">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-188">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="6e3e9-188">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-189">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8.1 ou no Windows 8</span><span class="sxs-lookup"><span data-stu-id="6e3e9-189">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1 or Windows 8</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6e3e9-190">Windows Server 2012, Windows Server2008R2, Windows 8 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="6e3e9-190">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-191">Windows Server2008 ou WindowsVista com Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="6e3e9-191">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-192">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="6e3e9-192">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, Windows 8, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6e3e9-193">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="6e3e9-193">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-194">Windows Server 2012, Windows Server2008R2, Windows 8 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="6e3e9-194">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-195">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="6e3e9-195">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6e3e9-196">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="6e3e9-196">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-197">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="6e3e9-197">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3e9-198">Com suporte, mas não pode reportar ou editar configurações de política ou itens de preferência que existem somente no Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="6e3e9-198">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, Windows 8, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="6e3e9-199">Pré-requisitos para a instalação do AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="6e3e9-199">Prerequisites for installing AGPM4.0 SP2</span></span>


<span data-ttu-id="6e3e9-200">A tabela a seguir descreve o comportamento dos instaladores do cliente e do servidor do AGPM 4.0 SP2 no Windows 8.1 quando o .NET Framework 3.5 ou o GPMC nas ferramentas de administração do servidor remoto estão ausentes.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-200">The following table describes the behavior of AGPM4.0 SP2 Client and Server installers on Windows8.1 when the .NET Framework3.5 or the GPMC in the Remote Server Administration Tools is missing.</span></span>

**<span data-ttu-id="6e3e9-201">Cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="6e3e9-201">AGPM Client</span></span>**

**<span data-ttu-id="6e3e9-202">Servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="6e3e9-202">AGPM Server</span></span>**

**<span data-ttu-id="6e3e9-203">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="6e3e9-203">Operating system</span></span>**

**<span data-ttu-id="6e3e9-204">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="6e3e9-204">.NET Framework</span></span>**

**<span data-ttu-id="6e3e9-205">Ferramentas de Administração de Servidor Remoto</span><span class="sxs-lookup"><span data-stu-id="6e3e9-205">Remote Server Administration Tools</span></span>**

**<span data-ttu-id="6e3e9-206">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="6e3e9-206">.NET Framework</span></span>**

**<span data-ttu-id="6e3e9-207">Ferramentas de Administração de Servidor Remoto</span><span class="sxs-lookup"><span data-stu-id="6e3e9-207">Remote Server Administration Tools</span></span>**

**<span data-ttu-id="6e3e9-208">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6e3e9-208">Windows8.1</span></span>**

<span data-ttu-id="6e3e9-209">Se o .NET Framework 3.5 não estiver habilitado ou instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-209">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="6e3e9-210">Se o GPMC não estiver habilitado ou instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-210">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="6e3e9-211">Se o .NET Framework 3.5 não estiver habilitado ou instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-211">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="6e3e9-212">Se o GPMC não estiver habilitado ou instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-212">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span>

**<span data-ttu-id="6e3e9-213">Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="6e3e9-213">Windows Server2012 R2</span></span>**

<span data-ttu-id="6e3e9-214">Se o .NET Framework 3.5 não estiver habilitado ou instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-214">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="6e3e9-215">Se o GPMC não estiver habilitado, o instalador o habilitará durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-215">If the GPMC is not enabled, the installer enables it during the installation.</span></span>

<span data-ttu-id="6e3e9-216">Se o .NET Framework 3.5 não estiver habilitado ou instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-216">If the .NET Framework3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="6e3e9-217">Se o GPMC não estiver habilitado, o instalador o habilitará durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-217">If the GPMC is not enabled, the installer enables it during the installation.</span></span>

 

## <span data-ttu-id="6e3e9-218">Como obter tecnologias do MDOP</span><span class="sxs-lookup"><span data-stu-id="6e3e9-218">How to Get MDOP Technologies</span></span>


<span data-ttu-id="6e3e9-219">O AGPM 4,0 SP2 faz parte do Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="6e3e9-219">AGPM 4.0 SP2 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="6e3e9-220">O MDOP faz parte do Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="6e3e9-220">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="6e3e9-221">Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte [como obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="6e3e9-221">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="6e3e9-222">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6e3e9-222">Related topics</span></span>


[<span data-ttu-id="6e3e9-223">Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="6e3e9-223">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="6e3e9-224">Notas de versão para Microsoft Advanced Group Policy Management 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="6e3e9-224">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP2</span></span>](release-notes-for-microsoft-advanced-group-policy-management-40-sp2.md)

[<span data-ttu-id="6e3e9-225">Como escolher qual versão do AGPM a ser instalada</span><span class="sxs-lookup"><span data-stu-id="6e3e9-225">Choosing Which Version of AGPM to Install</span></span>](choosing-which-version-of-agpm-to-install.md)

 

 





