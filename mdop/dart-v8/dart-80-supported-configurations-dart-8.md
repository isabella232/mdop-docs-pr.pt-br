---
title: Configurações compatíveis do DaRT 8.0
description: Configurações compatíveis do DaRT 8.0
author: dansimp
ms.assetid: 95d68e5c-d202-4f4a-adef-d2098328172e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 02c891555992652bf2a9b2b674ab8377536ef9d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799370"
---
# <span data-ttu-id="86328-103">Configurações compatíveis do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="86328-103">DaRT 8.0 Supported Configurations</span></span>


<span data-ttu-id="86328-104">Este tópico especifica o software de pré-requisito e os requisitos de configuração com suporte que são necessários para instalar e executar o Microsoft Diagnostic and Recovery Toolset (DaRT) 8,0 em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="86328-104">This topic specifies the prerequisite software and supported configurations requirements that are necessary to install and run Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 in your environment.</span></span> <span data-ttu-id="86328-105">Os requisitos do sistema operacional e os requisitos do sistema necessários para executar o DaRT 8,0 são especificados.</span><span class="sxs-lookup"><span data-stu-id="86328-105">Both the operating system requirements and the system requirements that are required to run DaRT 8.0 are specified.</span></span> <span data-ttu-id="86328-106">Para obter informações sobre pré-requisitos que você precisa considerar para criar a imagem de recuperação do DaRT, consulte [planejando criar a imagem de recuperação do dart 8,0](planning-to-create-the-dart-80-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="86328-106">For information about prerequisites that you need to consider to create the DaRT recovery image, see [Planning to Create the DaRT 8.0 Recovery Image](planning-to-create-the-dart-80-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="86328-107">Para configurações compatíveis que se aplicam a versões posteriores, consulte a documentação da versão aplicável.</span><span class="sxs-lookup"><span data-stu-id="86328-107">For supported configurations that apply to later releases, see the documentation for the applicable release.</span></span>

<span data-ttu-id="86328-108">Você pode instalar o DaRT de uma de duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="86328-108">You can install DaRT in one of two ways.</span></span> <span data-ttu-id="86328-109">Você pode instalar toda a funcionalidade em um computador administrador de ti, no qual executará todas as tarefas associadas à execução do DaRT.</span><span class="sxs-lookup"><span data-stu-id="86328-109">You can install all functionality on an IT administrator computer, where you will perform all the tasks associated with running DaRT.</span></span> <span data-ttu-id="86328-110">Você também pode instalar, no computador administrador, somente a funcionalidade DaRT que cria a imagem de recuperação e, em seguida, instalar a funcionalidade usada para executar o DaRT (ou seja, o Visualizador de conexão remota do DaRT) em um computador de suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="86328-110">Alternatively, you can install, on the administrator computer, only the DaRT functionality that creates the recovery image, and then install the functionality used to run DaRT (that is, the DaRT Remote Connection Viewer) on a help desk computer.</span></span>

## <a href="" id="---------dart-8-0-prerequisite-software"></a> <span data-ttu-id="86328-111">Software de pré-requisito DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="86328-111">DaRT 8.0 prerequisite software</span></span>


<span data-ttu-id="86328-112">Certifique-se de que os seguintes pré-requisitos são atendidos antes de instalar o DaRT.</span><span class="sxs-lookup"><span data-stu-id="86328-112">Make sure that the following prerequisites are met before you install DaRT.</span></span>

### <span data-ttu-id="86328-113">Pré-requisitos do computador administrador</span><span class="sxs-lookup"><span data-stu-id="86328-113">Administrator computer prerequisites</span></span>

<span data-ttu-id="86328-114">A tabela a seguir lista os pré-requisitos de instalação do computador administrador quando você está instalando o DaRT 8,0 e todas as ferramentas do DaRT.</span><span class="sxs-lookup"><span data-stu-id="86328-114">The following table lists the installation prerequisites for the administrator computer when you are installing DaRT 8.0 and all of the DaRT tools.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="86328-115">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="86328-115">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="86328-116">Detalhes</span><span class="sxs-lookup"><span data-stu-id="86328-116">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="86328-117">Kit de avaliação e desenvolvimento do Windows (ADK)</span><span class="sxs-lookup"><span data-stu-id="86328-117">Windows Assessment and Development Kit (ADK)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="86328-118">Obrigatório para o assistente de recuperação de imagem de DaRT.</span><span class="sxs-lookup"><span data-stu-id="86328-118">Required for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="86328-119">Contém as ferramentas de implantação, que são usadas para personalizar, implantar e fazer a manutenção de imagens do Windows e contém o ambiente de pré-instalação do Windows (Windows PE).</span><span class="sxs-lookup"><span data-stu-id="86328-119">Contains the Deployment Tools, which are used to customize, deploy, and service Windows images, and contains the Windows Preinstallation Environment (Windows PE).</span></span> <span data-ttu-id="86328-120">O ADK não será necessário se você estiver instalando apenas o Visualizador de conexão remota e/ou o Crash Analyzer.</span><span class="sxs-lookup"><span data-stu-id="86328-120">The ADK is not required if you are installing only the Remote Connection Viewer and/or Crash Analyzer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="86328-121">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="86328-121">.NET Framework 4.5</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="86328-122">Exigido pelo assistente de imagem de recuperação DaRT.</span><span class="sxs-lookup"><span data-stu-id="86328-122">Required by the DaRT Recovery Image wizard.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="86328-123">Kit de desenvolvimento do Windows ou kit de desenvolvimento de software (opcional)</span><span class="sxs-lookup"><span data-stu-id="86328-123">Windows Development Kit OR Software Development Kit (optional)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="86328-124">O Crash Analyzer requer as ferramentas de depuração do Windows 8 do kit de driver do Windows para analisar os arquivos de despejo de memória.</span><span class="sxs-lookup"><span data-stu-id="86328-124">Crash Analyzer requires the Windows 8 Debugging Tools from the Windows Driver Kit to analyze memory dump files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="86328-125">Imagem ISO do Windows 8 64-bit</span><span class="sxs-lookup"><span data-stu-id="86328-125">Windows 8 64-bit ISO image</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="86328-126">O DaRT requer a imagem do Windows RE (ambiente de recuperação do Windows) da mídia do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="86328-126">DaRT requires the Windows Recovery Environment (Windows RE) image from the Windows 8 media.</span></span> <span data-ttu-id="86328-127">Baixe a versão de 32 bits ou 64 bits do Windows 8, dependendo do tipo de imagem de recuperação do DaRT que você deseja criar.</span><span class="sxs-lookup"><span data-stu-id="86328-127">Download the 32-bit or 64-bit version of Windows 8, depending on the type of DaRT recovery image you want to create.</span></span> <span data-ttu-id="86328-128">Se você oferecer suporte a ambos os tipos de sistema em seu ambiente, baixe ambas as versões do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="86328-128">If you support both system types in your environment, download both versions of Windows 8.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="86328-129">Pré-requisitos do computador de suporte técnico</span><span class="sxs-lookup"><span data-stu-id="86328-129">Help desk computer prerequisites</span></span>

<span data-ttu-id="86328-130">A tabela a seguir lista os pré-requisitos de instalação do computador com suporte técnico quando você está executando o Visualizador de conexão remota DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="86328-130">The following table lists the installation prerequisites for the help desk computer when you are running the DaRT 8.0 Remote Connection Viewer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="86328-131">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="86328-131">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="86328-132">Detalhes</span><span class="sxs-lookup"><span data-stu-id="86328-132">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="86328-133">Visualizador de conexão remota DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="86328-133">DaRT 8.0 Remote Connection Viewer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="86328-134">Deve ser instalado em um sistema operacional Windows 8.</span><span class="sxs-lookup"><span data-stu-id="86328-134">Must be installed on a Windows 8 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="86328-135">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="86328-135">NET Framework 4.5</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="86328-136">Exigido pelo assistente de imagem de recuperação DaRT</span><span class="sxs-lookup"><span data-stu-id="86328-136">Required by the DaRT Recovery Image wizard</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="86328-137">Ferramentas de depuração para Windows</span><span class="sxs-lookup"><span data-stu-id="86328-137">Debugging Tools for Windows</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="86328-138">Obrigatório apenas se você estiver instalando a ferramenta Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="86328-138">Required only if you are installing the Crash Analyzer tool</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="86328-139">Pré-requisitos do computador do usuário final</span><span class="sxs-lookup"><span data-stu-id="86328-139">End-user computer prerequisites</span></span>

<span data-ttu-id="86328-140">Não há nenhum software obrigatório que deve ser instalado em computadores de usuário final, exceto o sistema operacional Windows 8.</span><span class="sxs-lookup"><span data-stu-id="86328-140">There is no prerequisite software that must be installed on end-user computers, other than the Windows 8 operating system.</span></span>

## <a href="" id="---------dart-operating-system-requirements"></a> <span data-ttu-id="86328-141">Requisitos do sistema operacional DaRT</span><span class="sxs-lookup"><span data-stu-id="86328-141">DaRT operating system requirements</span></span>


### <span data-ttu-id="86328-142">Requisitos do sistema de computador administrador</span><span class="sxs-lookup"><span data-stu-id="86328-142">Administrator computer system requirements</span></span>

<span data-ttu-id="86328-143">A tabela a seguir lista os sistemas operacionais suportados para a instalação do computador do administrador do DaRT.</span><span class="sxs-lookup"><span data-stu-id="86328-143">The following table lists the operating systems that are supported for the DaRT administrator computer installation.</span></span>

<span data-ttu-id="86328-144">**Observação**  Certifique-se de atribuir espaço suficiente para as ferramentas adicionais que você deseja instalar no computador administrador.</span><span class="sxs-lookup"><span data-stu-id="86328-144">**Note** Make sure that you allocate enough space for any additional tools that you want to install on the administrator computer.</span></span>

 

<span data-ttu-id="86328-145">**Observação**  A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="86328-145">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="86328-146">Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="86328-146">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="86328-147">Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="86328-147">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>

 

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="86328-148">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="86328-148">Operating System</span></span></th>
<th align="left"><span data-ttu-id="86328-149">Edição</span><span class="sxs-lookup"><span data-stu-id="86328-149">Edition</span></span></th>
<th align="left"><span data-ttu-id="86328-150">Service Pack</span><span class="sxs-lookup"><span data-stu-id="86328-150">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="86328-151">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="86328-151">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="86328-152">Requisitos do Sistema Operacional</span><span class="sxs-lookup"><span data-stu-id="86328-152">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="86328-153">Requisito de RAM para executar o DaRT</span><span class="sxs-lookup"><span data-stu-id="86328-153">RAM Requirement for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86328-154">Windows8</span><span class="sxs-lookup"><span data-stu-id="86328-154">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-155">Todas as edições</span><span class="sxs-lookup"><span data-stu-id="86328-155">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-156">N/A</span><span class="sxs-lookup"><span data-stu-id="86328-156">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-157">64 bits</span><span class="sxs-lookup"><span data-stu-id="86328-157">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-158">2 GB</span><span class="sxs-lookup"><span data-stu-id="86328-158">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-159">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="86328-159">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86328-160">Windows8</span><span class="sxs-lookup"><span data-stu-id="86328-160">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-161">Todas as edições</span><span class="sxs-lookup"><span data-stu-id="86328-161">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-162">N/A</span><span class="sxs-lookup"><span data-stu-id="86328-162">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-163">32 bits</span><span class="sxs-lookup"><span data-stu-id="86328-163">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-164">1 GB</span><span class="sxs-lookup"><span data-stu-id="86328-164">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-165">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="86328-165">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86328-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="86328-166">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-167">Padrão, corporativo, Data Center</span><span class="sxs-lookup"><span data-stu-id="86328-167">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-168">N/A</span><span class="sxs-lookup"><span data-stu-id="86328-168">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-169">64 bits</span><span class="sxs-lookup"><span data-stu-id="86328-169">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-170">512 MB</span><span class="sxs-lookup"><span data-stu-id="86328-170">512 MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-171">1.0 GB</span><span class="sxs-lookup"><span data-stu-id="86328-171">1 .0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> <span data-ttu-id="86328-172">Requisitos do sistema do computador de suporte técnico DaRT</span><span class="sxs-lookup"><span data-stu-id="86328-172">DaRT help desk computer system requirements</span></span>

<span data-ttu-id="86328-173">Se você permitir que um suporte técnico ajude a solucionar problemas com computadores remotamente, você deve ter o Visualizador de conexão remota instalado no computador de suporte.</span><span class="sxs-lookup"><span data-stu-id="86328-173">If you allow a help desk to remotely troubleshoot computers, you must have the Remote Connection Viewer installed on the help desk computer.</span></span> <span data-ttu-id="86328-174">Opcionalmente, você pode instalar a ferramenta Crash Analyzer no computador de suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="86328-174">You can optionally install the Crash Analyzer tool on the help desk computer.</span></span>

<span data-ttu-id="86328-175">O DaRT 8,0 permite que um trabalhador de suporte técnico se conecte a um computador DaRT 8,0 usando o DaRT 7,0 ou o DaRT 8,0 Remote Connection Viewer.</span><span class="sxs-lookup"><span data-stu-id="86328-175">DaRT 8.0 enables a help desk worker to connect to a DaRT 8.0 computer by using either the DaRT 7.0 or DaRT 8.0 Remote Connection Viewer.</span></span> <span data-ttu-id="86328-176">O Visualizador de conexão remota do DaRT 7,0 exige um sistema operacional Windows 7, enquanto o Visualizador de conexão remota do DaRT 8,0 requer o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="86328-176">The DaRT 7.0 Remote Connection Viewer requires a Windows 7 operating system, while the DaRT 8.0 Remote Connection Viewer requires Windows 8.</span></span> <span data-ttu-id="86328-177">O Visualizador de conexão remota do DaRT 8,0 e todas as outras ferramentas do DaRT 8,0 podem ser instaladas apenas em um computador com Windows 8.</span><span class="sxs-lookup"><span data-stu-id="86328-177">The DaRT 8.0 Remote Connection Viewer and all other DaRT 8.0 tools can be installed only on a computer running Windows 8.</span></span>

<span data-ttu-id="86328-178">A tabela a seguir lista os sistemas operacionais suportados para a instalação do computador do DaRT Help Desk.</span><span class="sxs-lookup"><span data-stu-id="86328-178">The following table lists the operating systems that are supported for the DaRT help desk computer installation.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="86328-179">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="86328-179">Operating System</span></span></th>
<th align="left"><span data-ttu-id="86328-180">Edição</span><span class="sxs-lookup"><span data-stu-id="86328-180">Edition</span></span></th>
<th align="left"><span data-ttu-id="86328-181">Service Pack</span><span class="sxs-lookup"><span data-stu-id="86328-181">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="86328-182">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="86328-182">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="86328-183">Requisitos do Sistema Operacional</span><span class="sxs-lookup"><span data-stu-id="86328-183">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="86328-184">Requisitos de RAM para executar o DaRT</span><span class="sxs-lookup"><span data-stu-id="86328-184">RAM Requirements for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86328-185">Windows8</span><span class="sxs-lookup"><span data-stu-id="86328-185">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-186">Todas as edições</span><span class="sxs-lookup"><span data-stu-id="86328-186">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-187">N/A</span><span class="sxs-lookup"><span data-stu-id="86328-187">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-188">64 bits</span><span class="sxs-lookup"><span data-stu-id="86328-188">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-189">2 GB</span><span class="sxs-lookup"><span data-stu-id="86328-189">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-190">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="86328-190">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86328-191">Windows8 (somente com o Visualizador de conexão remota 8,0)</span><span class="sxs-lookup"><span data-stu-id="86328-191">Windows8 (with Remote Connection Viewer 8.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-192">Todas as edições</span><span class="sxs-lookup"><span data-stu-id="86328-192">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-193">N/A</span><span class="sxs-lookup"><span data-stu-id="86328-193">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-194">32 bits</span><span class="sxs-lookup"><span data-stu-id="86328-194">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-195">1 GB</span><span class="sxs-lookup"><span data-stu-id="86328-195">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-196">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="86328-196">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86328-197">Windows 7 (somente com o Visualizador de conexão remota 7,0)</span><span class="sxs-lookup"><span data-stu-id="86328-197">Windows 7 (with Remote Connection Viewer 7.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-198">Todas as edições</span><span class="sxs-lookup"><span data-stu-id="86328-198">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-199">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="86328-199">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-200">64 bits ou 32 bits</span><span class="sxs-lookup"><span data-stu-id="86328-200">64-bit or 32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-201">1 GB</span><span class="sxs-lookup"><span data-stu-id="86328-201">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-202">N/A</span><span class="sxs-lookup"><span data-stu-id="86328-202">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86328-203">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="86328-203">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-204">Padrão, corporativo, Data Center</span><span class="sxs-lookup"><span data-stu-id="86328-204">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-205">N/A</span><span class="sxs-lookup"><span data-stu-id="86328-205">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-206">64 bits</span><span class="sxs-lookup"><span data-stu-id="86328-206">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-207">51</span><span class="sxs-lookup"><span data-stu-id="86328-207">51</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-208">1,0 GB</span><span class="sxs-lookup"><span data-stu-id="86328-208">1.0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="86328-209">O DaRT também tem os seguintes requisitos mínimos de hardware para o computador do usuário final:</span><span class="sxs-lookup"><span data-stu-id="86328-209">DaRT also has the following minimum hardware requirements for the end-user computer:</span></span>

<span data-ttu-id="86328-210">Uma unidade de CD ou DVD ou uma porta USB-necessária apenas se você estiver implantando o DaRT na sua empresa usando um CD, DVD ou USB.</span><span class="sxs-lookup"><span data-stu-id="86328-210">A CD or DVD drive or a USB port - required only if you are deploying DaRT in your enterprise by using a CD, DVD, or USB.</span></span>

<span data-ttu-id="86328-211">Suporte do BIOS para iniciar o computador a partir de um CD ou DVD, uma unidade flash USB ou de uma partição remota ou de recuperação.</span><span class="sxs-lookup"><span data-stu-id="86328-211">BIOS support for starting the computer from a CD or DVD, a USB flash drive, or from a remote or recovery partition.</span></span>

### <a href="" id="-------------dart-end-user-computer-system-requirements"></a> <span data-ttu-id="86328-212">Requisitos do sistema para o computador de usuário final do DaRT</span><span class="sxs-lookup"><span data-stu-id="86328-212">DaRT end-user computer system requirements</span></span>

<span data-ttu-id="86328-213">A janela do conjunto de ferramentas de diagnóstico e recuperação do DaRT requer que o computador do usuário final use um dos seguintes sistemas operacionais juntamente com a quantidade especificada de memória do sistema disponível para o DaRT:</span><span class="sxs-lookup"><span data-stu-id="86328-213">The Diagnostics and Recovery Toolset window in DaRT requires that the end-user computer use one of the following operating systems together with the specified amount of system memory available for DaRT:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="86328-214">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="86328-214">Operating System</span></span></th>
<th align="left"><span data-ttu-id="86328-215">Edição</span><span class="sxs-lookup"><span data-stu-id="86328-215">Edition</span></span></th>
<th align="left"><span data-ttu-id="86328-216">Service Pack</span><span class="sxs-lookup"><span data-stu-id="86328-216">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="86328-217">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="86328-217">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="86328-218">Requisitos do Sistema Operacional</span><span class="sxs-lookup"><span data-stu-id="86328-218">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="86328-219">Requisitos de RAM</span><span class="sxs-lookup"><span data-stu-id="86328-219">RAM Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86328-220">Windows8</span><span class="sxs-lookup"><span data-stu-id="86328-220">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-221">Todas as edições</span><span class="sxs-lookup"><span data-stu-id="86328-221">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-222">N/A</span><span class="sxs-lookup"><span data-stu-id="86328-222">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-223">64 bits</span><span class="sxs-lookup"><span data-stu-id="86328-223">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-224">2 GB</span><span class="sxs-lookup"><span data-stu-id="86328-224">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-225">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="86328-225">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86328-226">Windows8</span><span class="sxs-lookup"><span data-stu-id="86328-226">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-227">Todas as edições</span><span class="sxs-lookup"><span data-stu-id="86328-227">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-228">N/A</span><span class="sxs-lookup"><span data-stu-id="86328-228">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-229">32 bits</span><span class="sxs-lookup"><span data-stu-id="86328-229">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-230">1 GB</span><span class="sxs-lookup"><span data-stu-id="86328-230">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-231">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="86328-231">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86328-232">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="86328-232">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-233">Padrão, corporativo, Data Center</span><span class="sxs-lookup"><span data-stu-id="86328-233">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-234">N/A</span><span class="sxs-lookup"><span data-stu-id="86328-234">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-235">64 bits</span><span class="sxs-lookup"><span data-stu-id="86328-235">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-236">512 MB</span><span class="sxs-lookup"><span data-stu-id="86328-236">512 MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="86328-237">1,0 GB</span><span class="sxs-lookup"><span data-stu-id="86328-237">1.0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="86328-238">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="86328-238">Related topics</span></span>


[<span data-ttu-id="86328-239">Planejamento da implantação do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="86328-239">Planning to Deploy DaRT 8.0</span></span>](planning-to-deploy-dart-80-dart-8.md)

 

 





