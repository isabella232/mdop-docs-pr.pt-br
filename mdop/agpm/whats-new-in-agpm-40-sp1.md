---
title: Novidades do AGPM 4.0 SP1
description: Novidades do AGPM 4.0 SP1
author: dansimp
ms.assetid: c6a3d94a-13c3-44e6-a466-c3011879999e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca1ee4a1c2eb943a25246dc31b127eaf72ff5fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797268"
---
# <span data-ttu-id="45ed4-103">Novidades do AGPM 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="45ed4-103">What's New in AGPM 4.0 SP1</span></span>


<span data-ttu-id="45ed4-104">Este conteúdo "o que há de novo" descreve melhorias e configurações com suporte para o gerenciamento avançado de política de grupo (AGPM) 4,0 SP1 da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="45ed4-104">This “What’s New” content describes enhancements and supported configurations for Microsoft Advanced Group Policy Management (AGPM) 4.0 SP1.</span></span> <span data-ttu-id="45ed4-105">Se houver uma diferença entre esse conteúdo e outra documentação do AGPM, esse conteúdo deve ser considerado autoritativo e deve substituir o conteúdo incluído neste produto.</span><span class="sxs-lookup"><span data-stu-id="45ed4-105">If there is a difference between this content and other AGPM documentation, this content should be considered authoritative and should supersede the content included with this product.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="45ed4-106">O que há de novo</span><span class="sxs-lookup"><span data-stu-id="45ed4-106">What’s new</span></span>


<span data-ttu-id="45ed4-107">O AGPM 4,0 SP1 é compatível com os seguintes aprimoramentos:</span><span class="sxs-lookup"><span data-stu-id="45ed4-107">AGPM 4.0 SP1 supports the following enhancements:</span></span>

### <span data-ttu-id="45ed4-108">Extensões novas e alteradas do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="45ed4-108">New and changed client-side extensions</span></span>

<span data-ttu-id="45ed4-109">As extensões do lado do cliente da política de grupo (CSEs) foram adicionadas ou alteradas para o AGPM dar suporte a novas políticas de grupo no Windows 8 e no Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="45ed4-109">Group Policy client-side extensions (CSEs) have been added or changed for AGPM to support new Group Policies in Windows 8 and Windows Server 2012.</span></span> <span data-ttu-id="45ed4-110">Essas políticas de grupo permitem que os administradores de política de grupo gerenciem e controlem as configurações de política de grupo específicas do Windows 8 que mudam entre dois objetos de política de grupo (GPOs) ou modelos.</span><span class="sxs-lookup"><span data-stu-id="45ed4-110">These group policies enable Group Policy administrators to manage and track Windows 8-specific Group Policy settings that change between two Group Policy Objects (GPOs) or templates.</span></span> <span data-ttu-id="45ed4-111">Você também pode criar GPOs personalizados, com configurações específicas do Windows 8, e configurar e salvar os GPOs como um modelo.</span><span class="sxs-lookup"><span data-stu-id="45ed4-111">You can also create custom GPOs, with Windows 8-specific settings, and configure and save the GPOs as a template.</span></span> <span data-ttu-id="45ed4-112">Para exibir seu CSEs, use as configurações e os relatórios de diferença disponíveis no cliente do AGPM 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="45ed4-112">To view your CSEs, use the settings and difference reports that are available in the AGPM 4.0 SP1 client.</span></span>

<span data-ttu-id="45ed4-113">As extensões nova e alterada do lado do cliente da política de grupo são:</span><span class="sxs-lookup"><span data-stu-id="45ed4-113">The new and changed Group Policy client-side extensions are:</span></span>

-   <span data-ttu-id="45ed4-114">**Política de acesso central:** Permite que os administradores de política de grupo especifiquem políticas de acesso central em servidores de política de grupo, por exemplo, servidores de arquivos.</span><span class="sxs-lookup"><span data-stu-id="45ed4-114">**Central Access Policy:** Enables Group Policy administrators to specify Central Access Policies on Group Policy servers, for example, file servers.</span></span> <span data-ttu-id="45ed4-115">A política de acesso central é uma política de autorização especificada por um item de GPO e aplicada a destinos de política para facilitar o acesso centralizado e o controle de recursos.</span><span class="sxs-lookup"><span data-stu-id="45ed4-115">Central Access Policy is an authorization policy that is specified by a GPO item and applied to policy targets to facilitate centralized access and control of resources.</span></span> <span data-ttu-id="45ed4-116">Essas políticas de acesso central devem ser configuradas em um computador cliente de política de grupo no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="45ed4-116">These Central Access Policies must be configured on a Group Policy client computer from within Active Directory.</span></span> <span data-ttu-id="45ed4-117">Uma política de grupo distribui o conhecimento de uma política de acesso central aplicável aos computadores que precisam aplicá-la.</span><span class="sxs-lookup"><span data-stu-id="45ed4-117">A Group Policy distributes the knowledge of an applicable Central Access Policy to the computers that have to enforce it.</span></span>

-   <span data-ttu-id="45ed4-118">**Alterações nas políticas de resolução de nomes:** Permite que os administradores de política de grupo definam as configurações de segurança do DNS e do DirectAccess em computadores cliente DNS.</span><span class="sxs-lookup"><span data-stu-id="45ed4-118">**Name Resolution Policy changes:** Enables Group Policy administrators to configure settings for DNS security and DirectAccess on DNS client computers.</span></span> <span data-ttu-id="45ed4-119">Novas guias para definir configurações de servidor DNS genérico e configurações de codificação foram adicionadas.</span><span class="sxs-lookup"><span data-stu-id="45ed4-119">New tabs for configuring Generic DNS Server settings and Encoding settings have been added.</span></span>

-   <span data-ttu-id="45ed4-120">**Alterações de preferência de política de Grupo:** Adiciona suporte para a configuração e o gerenciamento de configurações do Internet Explorer 10 que foram adicionadas para o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="45ed4-120">**Group Policy Preference changes:** Adds support for the configuration and management of Internet Explorer 10 settings that were added for Windows 8.</span></span>

-   <span data-ttu-id="45ed4-121">**Conexões de aplicativos remotos e da área de trabalho:** Permite que os administradores de política de grupo especifiquem a URL de conexão padrão usada para conexões de aplicativos e área de trabalho remotos.</span><span class="sxs-lookup"><span data-stu-id="45ed4-121">**Remote Application and Desktop Connections:** Lets Group Policy administrators specify the default connection URL that is used for Remote Application and Desktop Connections.</span></span>

-   <span data-ttu-id="45ed4-122">**Opções de inicialização do Windows to go:** Permite que os administradores de política de grupo configurem se o computador será inicializado no Windows to go se um dispositivo USB que contém um espaço de trabalho do Windows to go estiver conectado.</span><span class="sxs-lookup"><span data-stu-id="45ed4-122">**Windows To Go Startup Options:** Lets Group Policy administrators configure whether the computer will boot to Windows To Go if a USB device that contains a Windows To Go workspace is connected.</span></span>

-   <span data-ttu-id="45ed4-123">**Opções de hibernação do Windows to go:** Permite que os administradores de política de grupo configurem se um computador pode usar o estado de suspensão de hibernação (S4) quando o computador é iniciado a partir de um espaço de trabalho do Windows to go.</span><span class="sxs-lookup"><span data-stu-id="45ed4-123">**Windows To Go Hibernate Options:** Lets Group Policy administrators configure whether a computer can use the hibernation sleep state (S4) when the computer is started from a Windows To Go workspace.</span></span>

### <span data-ttu-id="45ed4-124">Feedback do cliente e pacote cumulativo de hotfix</span><span class="sxs-lookup"><span data-stu-id="45ed4-124">Customer feedback and hotfix rollup</span></span>

<span data-ttu-id="45ed4-125">O AGPM 4,0 SP1 inclui um pacote cumulativo de correções para solucionar problemas encontrados desde o lançamento do AGPM 4,0.</span><span class="sxs-lookup"><span data-stu-id="45ed4-125">AGPM 4.0 SP1 includes a rollup of fixes to address issues found since the AGPM 4.0 release.</span></span> <span data-ttu-id="45ed4-126">O AGPM 4,0 SP1 contém as mais recentes correções até e incluindo o gerenciamento avançado de política de grupo da Microsoft 4,0 hotfix 1.</span><span class="sxs-lookup"><span data-stu-id="45ed4-126">AGPM 4.0 SP1 contains the latest fixes up to and including Microsoft Advanced Group Policy Management 4.0 Hotfix 1.</span></span>

### <span data-ttu-id="45ed4-127">Relatórios de configurações e diferença mostram novas extensões de política de grupo</span><span class="sxs-lookup"><span data-stu-id="45ed4-127">Settings and difference reports show new Group Policy extensions</span></span>

<span data-ttu-id="45ed4-128">As novas extensões de política de grupo foram adicionadas às configurações e aos relatórios de diferença.</span><span class="sxs-lookup"><span data-stu-id="45ed4-128">The new Group Policy extensions have been added to the settings and difference reports.</span></span>

### <span data-ttu-id="45ed4-129">Mudanças e suporte do instalador</span><span class="sxs-lookup"><span data-stu-id="45ed4-129">Installer changes and support</span></span>

<span data-ttu-id="45ed4-130">As alterações e o suporte para o instalador do AGPM 4,0 SP1 são:</span><span class="sxs-lookup"><span data-stu-id="45ed4-130">The changes and support for the AGPM 4.0 SP1 installer are:</span></span>

-   <span data-ttu-id="45ed4-131">Se você instalar o AGPM 4,0 SP1 no Windows 8 ou no Windows Server 2012, o instalador do AGPM verificará se o software de pré-requisito necessário (console de gerenciamento de política de grupo e a estrutura .NET 3,5) está instalado.</span><span class="sxs-lookup"><span data-stu-id="45ed4-131">If you install AGPM 4.0 SP1 on Windows 8 or Windows Server 2012, the AGPM installer verifies that the required prerequisite software (Group Policy Management Console and the .NET 3.5 Framework) is installed.</span></span> <span data-ttu-id="45ed4-132">Se esses pré-requisitos não estiverem instalados, a instalação do AGPM 4,0 SP1 será bloqueada.</span><span class="sxs-lookup"><span data-stu-id="45ed4-132">If these prerequisites are not installed, the AGPM 4.0 SP1 installation is blocked.</span></span>

-   <span data-ttu-id="45ed4-133">Quando você instala o AGPM 4,0 SP1, a ativação do WCF, a ativação não HTTP e o serviço de ativação de processos do Windows são habilitados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="45ed4-133">When you install AGPM 4.0 SP1, WCF Activation, Non-HTTP Activation, and Windows Process Activation Service are automatically enabled.</span></span>

-   <span data-ttu-id="45ed4-134">Nos sistemas operacionais cliente Windows Vista, Windows 7 e Windows 8, baixe a versão apropriada do kit de ferramentas de administração do sistema remoto para o sistema operacional antes de instalar o AGPM 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="45ed4-134">On Windows Vista, Windows 7, and Windows 8 client operating systems, download the appropriate version of the Remote System Administration Toolkit for your operating system before you install AGPM 4.0 SP1.</span></span>

-   <span data-ttu-id="45ed4-135">Há suporte para a compatibilidade com versões anteriores com sistemas operacionais com suporte.</span><span class="sxs-lookup"><span data-stu-id="45ed4-135">Backward compatibility with older supported operating systems is supported.</span></span>

### <span data-ttu-id="45ed4-136">Capacidade de atualizar ou atualizar para o AGPM 4,0 SP1 sem digitar novamente os parâmetros de configuração</span><span class="sxs-lookup"><span data-stu-id="45ed4-136">Ability to upgrade or update to AGPM 4.0 SP1 without re-entering configuration parameters</span></span>

<span data-ttu-id="45ed4-137">Você pode atualizar o cliente do AGPM ou o servidor para o AGPM 4,0 SP1 somente do AGPM 4,0 sem ser solicitado a digitar novamente os parâmetros de configuração (chamado de "atualização inteligente"), conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="45ed4-137">You can upgrade the AGPM client or server to AGPM 4.0 SP1 only from AGPM 4.0 without being prompted to re-enter configuration parameters (called “Smart Upgrade”), as shown in the following table.</span></span> <span data-ttu-id="45ed4-138">Se você estiver atualizando para o AGPM 4,0 SP1 de outras versões do AGPM, conforme mostrado na tabela, você deve usar a "atualização clássica", que exige que você insira novamente os parâmetros de configuração.</span><span class="sxs-lookup"><span data-stu-id="45ed4-138">If you are upgrading to AGPM 4.0 SP1 from other versions of AGPM, as shown in the table, you must use the “Classic Upgrade,” which requires you to re-enter the configuration parameters.</span></span> <span data-ttu-id="45ed4-139">Como cada versão do AGPM está associada a um sistema operacional específico, consulte [escolher qual versão do AGPM instalar](https://go.microsoft.com/fwlink/?LinkId=254350)e atualizar o sistema operacional conforme apropriado antes de realizar uma atualização.</span><span class="sxs-lookup"><span data-stu-id="45ed4-139">Since each version of AGPM is associated with a particular operating system, refer to [Choosing Which Version of AGPM to Install](https://go.microsoft.com/fwlink/?LinkId=254350), and be sure to upgrade your operating system as appropriate before performing an upgrade.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="45ed4-140">Versão do AGPM a partir da qual você pode atualizar</span><span class="sxs-lookup"><span data-stu-id="45ed4-140">AGPM Version From Which You Can Upgrade</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="45ed4-141">2,5</span><span class="sxs-lookup"><span data-stu-id="45ed4-141">2.5</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="45ed4-142">3,0</span><span class="sxs-lookup"><span data-stu-id="45ed4-142">3.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="45ed4-143">4,0</span><span class="sxs-lookup"><span data-stu-id="45ed4-143">4.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="45ed4-144">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="45ed4-144">4.0 SP1</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ed4-145">2,5</span><span class="sxs-lookup"><span data-stu-id="45ed4-145">2.5</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-146">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="45ed4-146">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-147">Atualização clássica</span><span class="sxs-lookup"><span data-stu-id="45ed4-147">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-148">Atualização clássica</span><span class="sxs-lookup"><span data-stu-id="45ed4-148">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-149">A instalação está bloqueada</span><span class="sxs-lookup"><span data-stu-id="45ed4-149">Installation is blocked</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ed4-150">3,0</span><span class="sxs-lookup"><span data-stu-id="45ed4-150">3.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-151">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="45ed4-151">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-152">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="45ed4-152">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-153">Atualização clássica</span><span class="sxs-lookup"><span data-stu-id="45ed4-153">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-154">A instalação está bloqueada</span><span class="sxs-lookup"><span data-stu-id="45ed4-154">Installation is blocked</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ed4-155">4,0</span><span class="sxs-lookup"><span data-stu-id="45ed4-155">4.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-156">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="45ed4-156">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-157">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="45ed4-157">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-158">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="45ed4-158">Not Applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-159">Atualização inteligente</span><span class="sxs-lookup"><span data-stu-id="45ed4-159">Smart Upgrade</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="45ed4-160">Configurações compatíveis</span><span class="sxs-lookup"><span data-stu-id="45ed4-160">Supported configurations</span></span>


<span data-ttu-id="45ed4-161">O AGPM dá suporte às configurações na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="45ed4-161">AGPM supports the configurations in the following table.</span></span> <span data-ttu-id="45ed4-162">Embora o AGPM dê suporte a configurações mistas, é altamente recomendável que você execute o cliente e o servidor do AGPM na mesma família de sistema operacional, por exemplo, Windows 8 com Windows Server 2012, Windows 7 com Windows Server 2008 R2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="45ed4-162">Although AGPM supports mixed configurations, it is strongly recommended that you run the AGPM client and server on the same operating system family, for example, Windows 8 with Windows Server 2012, Windows 7 with Windows Server 2008 R2, and so on.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="45ed4-163">Configurações com suporte para o servidor AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="45ed4-163">Supported Configurations for AGPM 4.0 SP1 Server</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="45ed4-164">Configurações com suporte para o cliente do AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="45ed4-164">Supported Configurations for AGPM 4.0 SP1 Client</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="45ed4-165">Suporte do AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="45ed4-165">AGPM 4.0 SP1 Support</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ed4-166">Windows 8 ou Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="45ed4-166">Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-167">Windows 8 ou Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="45ed4-167">Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-168">Com suporte</span><span class="sxs-lookup"><span data-stu-id="45ed4-168">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ed4-169">Windows Server 2008 R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="45ed4-169">Windows Server 2008 R2 or Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-170">Windows Server 2008 R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="45ed4-170">Windows Server 2008 R2 or Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-171">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8</span><span class="sxs-lookup"><span data-stu-id="45ed4-171">Supported, but cannot edit policy settings or preference items that exist only in Windows 8</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ed4-172">Windows Server 2008 R2 ou Windows 7 ou Windows 8 ou Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="45ed4-172">Windows Server 2008 R2 or Windows 7 or Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-173">Windows Server 2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="45ed4-173">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-174">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server 2008 R2 ou no Windows 7 ou no Windows 8.</span><span class="sxs-lookup"><span data-stu-id="45ed4-174">Supported, but cannot edit policy settings or preference items that exist only in Windows Server 2008 R2 or Windows 7 or Windows 8.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45ed4-175">Windows Server 2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="45ed4-175">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-176">Windows Server 2008 R2 ou Windows 7 ou Windows 8 ou Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="45ed4-176">Windows Server 2008 R2 or Windows 7 or Windows 8 or Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-177">Com suporte</span><span class="sxs-lookup"><span data-stu-id="45ed4-177">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45ed4-178">Windows Server 2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="45ed4-178">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-179">Windows Server 2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="45ed4-179">Windows Server 2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="45ed4-180">Com suporte, mas não pode relatar ou editar configurações de política ou itens de preferência que existem somente no Windows Server 2008 R2 ou no Windows 7 ou no Windows 8</span><span class="sxs-lookup"><span data-stu-id="45ed4-180">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server 2008 R2 or Windows 7 or Windows 8</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="45ed4-181">Pré-requisitos para a instalação do AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="45ed4-181">Prerequisites for installing AGPM 4.0 SP1</span></span>


<span data-ttu-id="45ed4-182">A tabela a seguir descreve o comportamento no Windows 8 dos instaladores do cliente e do cliente do AGPM 4,0 SP1 quando o .NET 3,5 ou o console de gerenciamento de política de grupo (RSAT) estiver ausente.</span><span class="sxs-lookup"><span data-stu-id="45ed4-182">The following table describes the behavior on Windows 8 of AGPM 4.0 SP1 client and server installers when .NET 3.5 or the Group Policy Management Console in the Remote Server Administration Tools (RSAT) is missing.</span></span>

**<span data-ttu-id="45ed4-183">Cliente do AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="45ed4-183">AGPM Client 4.0 SP1</span></span>**

**<span data-ttu-id="45ed4-184">Servidor do AGPM 4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="45ed4-184">AGPM Server 4.0 SP1</span></span>**

**<span data-ttu-id="45ed4-185">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="45ed4-185">Operating System</span></span>**

**<span data-ttu-id="45ed4-186">.NET</span><span class="sxs-lookup"><span data-stu-id="45ed4-186">.NET</span></span>**

**<span data-ttu-id="45ed4-187">RSAT</span><span class="sxs-lookup"><span data-stu-id="45ed4-187">RSAT</span></span>**

**<span data-ttu-id="45ed4-188">.NET</span><span class="sxs-lookup"><span data-stu-id="45ed4-188">.NET</span></span>**

**<span data-ttu-id="45ed4-189">RSAT</span><span class="sxs-lookup"><span data-stu-id="45ed4-189">RSAT</span></span>**

**<span data-ttu-id="45ed4-190">Windows 8</span><span class="sxs-lookup"><span data-stu-id="45ed4-190">Windows 8</span></span>**

<span data-ttu-id="45ed4-191">Se o .NET 3,5 não estiver habilitado ou instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="45ed4-191">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="45ed4-192">Se o GPMC não estiver habilitado ou instalado no sistema, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="45ed4-192">If GPMC is not enabled or installed on the system, the installer blocks the installation.</span></span>

<span data-ttu-id="45ed4-193">Se o .NET 3,5 não estiver habilitado ou instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="45ed4-193">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="45ed4-194">Se o GPMC não estiver habilitado ou instalado no sistema, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="45ed4-194">If GPMC is not enabled or installed on the system, the installer blocks the installation.</span></span>

**<span data-ttu-id="45ed4-195">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="45ed4-195">Windows Server 2012</span></span>**

<span data-ttu-id="45ed4-196">Se o .NET 3,5 não estiver habilitado ou instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="45ed4-196">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="45ed4-197">Se o GPMC não estiver habilitado, o instalador o habilitará durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="45ed4-197">If GPMC is not enabled, the installer enables it during the installation.</span></span>

<span data-ttu-id="45ed4-198">Se o .NET 3,5 não estiver habilitado ou instalado, o instalador bloqueará a instalação.</span><span class="sxs-lookup"><span data-stu-id="45ed4-198">If .NET 3.5 is not enabled or installed, the installer blocks the installation.</span></span>

<span data-ttu-id="45ed4-199">Se o GPMC não estiver habilitado, o instalador o habilitará durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="45ed4-199">If GPMC is not enabled, the installer enables it during the installation.</span></span>

 

## <span data-ttu-id="45ed4-200">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="45ed4-200">Related topics</span></span>


[<span data-ttu-id="45ed4-201">Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="45ed4-201">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="45ed4-202">Notas de versão para o Gerenciamento Avançado de Política de Grupo 4.0 SP1 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="45ed4-202">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP1</span></span>](release-notes-for-microsoft-advanced-group-policy-management-40-sp1.md)

 

 





