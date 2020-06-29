---
title: Configurações compatíveis do DaRT 10
description: Configurações compatíveis do DaRT 10
author: dansimp
ms.assetid: a07d6562-1fa9-499f-829c-9cc487ede0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 414b9d5cb7bf78dcfeda3fafc1c476e367709446
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796174"
---
# <span data-ttu-id="ed907-103">Configurações compatíveis do DaRT 10</span><span class="sxs-lookup"><span data-stu-id="ed907-103">DaRT 10 Supported Configurations</span></span>


<span data-ttu-id="ed907-104">Este tópico especifica o software de pré-requisito e os requisitos de configuração com suporte necessários para instalar e executar o Microsoft Diagnostic and Recovery Toolset (DaRT) 10 em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="ed907-104">This topic specifies the prerequisite software and supported configurations requirements that are necessary to install and run Microsoft Diagnostics and Recovery Toolset (DaRT) 10 in your environment.</span></span> <span data-ttu-id="ed907-105">Os requisitos do sistema operacional e os requisitos do sistema necessários para executar o DaRT 10 são especificados.</span><span class="sxs-lookup"><span data-stu-id="ed907-105">Both the operating system requirements and the system requirements that are required to run DaRT 10 are specified.</span></span> <span data-ttu-id="ed907-106">Para obter informações sobre pré-requisitos que você precisa considerar para criar a imagem de recuperação do DaRT, consulte [planejando criar a imagem de recuperação do DART 10](planning-to-create-the-dart-10-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="ed907-106">For information about prerequisites that you need to consider to create the DaRT recovery image, see [Planning to Create the DaRT 10 Recovery Image](planning-to-create-the-dart-10-recovery-image.md).</span></span>

<span data-ttu-id="ed907-107">Para configurações compatíveis que se aplicam a versões posteriores, consulte a documentação da versão aplicável.</span><span class="sxs-lookup"><span data-stu-id="ed907-107">For supported configurations that apply to later releases, see the documentation for the applicable release.</span></span>

<span data-ttu-id="ed907-108">Você pode instalar o DaRT de uma de duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="ed907-108">You can install DaRT in one of two ways.</span></span> <span data-ttu-id="ed907-109">Você pode instalar toda a funcionalidade em um computador administrador de ti, no qual executará todas as tarefas associadas à execução do DaRT.</span><span class="sxs-lookup"><span data-stu-id="ed907-109">You can install all functionality on an IT administrator computer, where you will perform all the tasks associated with running DaRT.</span></span> <span data-ttu-id="ed907-110">Você também pode instalar, no computador administrador, somente a funcionalidade DaRT que cria a imagem de recuperação e, em seguida, instalar a funcionalidade usada para executar o DaRT (ou seja, o Visualizador de conexão remota do DaRT) em um computador de suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="ed907-110">Alternatively, you can install, on the administrator computer, only the DaRT functionality that creates the recovery image, and then install the functionality used to run DaRT (that is, the DaRT Remote Connection Viewer) on a help desk computer.</span></span>

## <span data-ttu-id="ed907-111">Software de pré-requisito do DaRT 10</span><span class="sxs-lookup"><span data-stu-id="ed907-111">DaRT 10 prerequisite software</span></span>


<span data-ttu-id="ed907-112">Certifique-se de que os seguintes pré-requisitos são atendidos antes de instalar o DaRT.</span><span class="sxs-lookup"><span data-stu-id="ed907-112">Make sure that the following prerequisites are met before you install DaRT.</span></span>

### <span data-ttu-id="ed907-113">Pré-requisitos do computador administrador</span><span class="sxs-lookup"><span data-stu-id="ed907-113">Administrator computer prerequisites</span></span>

<span data-ttu-id="ed907-114">A tabela a seguir lista os pré-requisitos de instalação do computador administrador quando você está instalando o DaRT 10 e todas as ferramentas do DaRT.</span><span class="sxs-lookup"><span data-stu-id="ed907-114">The following table lists the installation prerequisites for the administrator computer when you are installing DaRT 10 and all of the DaRT tools.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ed907-115">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="ed907-115">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="ed907-116">Detalhes</span><span class="sxs-lookup"><span data-stu-id="ed907-116">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ed907-117">Kit de avaliação e desenvolvimento do Windows (ADK)</span><span class="sxs-lookup"><span data-stu-id="ed907-117">Windows Assessment and Development Kit (ADK)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ed907-118">Obrigatório para o assistente de recuperação de imagem de DaRT.</span><span class="sxs-lookup"><span data-stu-id="ed907-118">Required for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="ed907-119">Contém as ferramentas de implantação, que são usadas para personalizar, implantar e fazer a manutenção de imagens do Windows e contém o ambiente de pré-instalação do Windows (Windows PE).</span><span class="sxs-lookup"><span data-stu-id="ed907-119">Contains the Deployment Tools, which are used to customize, deploy, and service Windows images, and contains the Windows Preinstallation Environment (Windows PE).</span></span> <span data-ttu-id="ed907-120">O ADK não será necessário se você estiver instalando apenas o Visualizador de conexão remota e/ou o Crash Analyzer.</span><span class="sxs-lookup"><span data-stu-id="ed907-120">The ADK is not required if you are installing only the Remote Connection Viewer and/or Crash Analyzer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ed907-121">Kit de desenvolvimento do Windows ou kit de desenvolvimento de software (opcional)</span><span class="sxs-lookup"><span data-stu-id="ed907-121">Windows Development Kit OR Software Development Kit (optional)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ed907-122">O Crash Analyzer requer as ferramentas de depuração do Windows 10 do kit de driver do Windows para analisar os arquivos de despejo de memória.</span><span class="sxs-lookup"><span data-stu-id="ed907-122">Crash Analyzer requires the Windows 10 Debugging Tools from the Windows Driver Kit to analyze memory dump files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ed907-123">Imagem ISO do Windows 10 64-bit ou 32 bits</span><span class="sxs-lookup"><span data-stu-id="ed907-123">Windows 10 64-bit or 32-bit ISO image</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ed907-124">O DaRT requer a imagem do Windows RE (ambiente de recuperação do Windows) da mídia do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ed907-124">DaRT requires the Windows Recovery Environment (Windows RE) image from the Windows 10 media.</span></span> <span data-ttu-id="ed907-125">Baixe a versão de 32 bits ou 64 bits do Windows 10, dependendo do tipo de imagem de recuperação do DaRT que você deseja criar.</span><span class="sxs-lookup"><span data-stu-id="ed907-125">Download the 32-bit or 64-bit version of Windows 10, depending on the type of DaRT recovery image you want to create.</span></span> <span data-ttu-id="ed907-126">Se você oferecer suporte a ambos os tipos de sistema em seu ambiente, baixe ambas as versões do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ed907-126">If you support both system types in your environment, download both versions of Windows 10.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="ed907-127">Pré-requisitos do computador de suporte técnico</span><span class="sxs-lookup"><span data-stu-id="ed907-127">Help desk computer prerequisites</span></span>

<span data-ttu-id="ed907-128">A tabela a seguir lista os pré-requisitos de instalação do computador com suporte técnico quando você está executando o Visualizador de conexão remota do DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="ed907-128">The following table lists the installation prerequisites for the help desk computer when you are running the DaRT 10 Remote Connection Viewer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ed907-129">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="ed907-129">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="ed907-130">Detalhes</span><span class="sxs-lookup"><span data-stu-id="ed907-130">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ed907-131">Visualizador de conexão remota do DaRT 10</span><span class="sxs-lookup"><span data-stu-id="ed907-131">DaRT 10 Remote Connection Viewer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ed907-132">Deve ser instalado em um sistema operacional Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ed907-132">Must be installed on a Windows 10 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ed907-133">Ferramentas de depuração para Windows</span><span class="sxs-lookup"><span data-stu-id="ed907-133">Debugging Tools for Windows</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ed907-134">Obrigatório apenas se você estiver instalando a ferramenta Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="ed907-134">Required only if you are installing the Crash Analyzer tool</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="ed907-135">Pré-requisitos do computador do usuário final</span><span class="sxs-lookup"><span data-stu-id="ed907-135">End-user computer prerequisites</span></span>

<span data-ttu-id="ed907-136">Não há nenhum software obrigatório que deve ser instalado em computadores de usuário final, exceto o sistema operacional Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ed907-136">There is no prerequisite software that must be installed on end-user computers, other than the Windows 10 operating system.</span></span>

## <a href="" id="---------dart-10-operating-system-requirements"></a> <span data-ttu-id="ed907-137">Requisitos do sistema operacional DaRT 10</span><span class="sxs-lookup"><span data-stu-id="ed907-137">DaRT 10 operating system requirements</span></span>


### <span data-ttu-id="ed907-138">Requisitos do sistema de computador administrador</span><span class="sxs-lookup"><span data-stu-id="ed907-138">Administrator computer system requirements</span></span>

<span data-ttu-id="ed907-139">A tabela a seguir lista os sistemas operacionais suportados para a instalação do computador do administrador do DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="ed907-139">The following table lists the operating systems that are supported for the DaRT 10 administrator computer installation.</span></span>

<span data-ttu-id="ed907-140">**Observação**  Certifique-se de atribuir espaço suficiente para as ferramentas adicionais que você deseja instalar no computador administrador.</span><span class="sxs-lookup"><span data-stu-id="ed907-140">**Note** Make sure that you allocate enough space for any additional tools that you want to install on the administrator computer.</span></span>

 

<span data-ttu-id="ed907-141">**Observação**  A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="ed907-141">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="ed907-142">Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="ed907-142">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="ed907-143">Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)</span><span class="sxs-lookup"><span data-stu-id="ed907-143">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>

 

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
<th align="left"><span data-ttu-id="ed907-144">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="ed907-144">Operating System</span></span></th>
<th align="left"><span data-ttu-id="ed907-145">Edição</span><span class="sxs-lookup"><span data-stu-id="ed907-145">Edition</span></span></th>
<th align="left"><span data-ttu-id="ed907-146">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ed907-146">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="ed907-147">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="ed907-147">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="ed907-148">Requisitos do Sistema Operacional</span><span class="sxs-lookup"><span data-stu-id="ed907-148">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="ed907-149">Requisito de RAM para executar o DaRT</span><span class="sxs-lookup"><span data-stu-id="ed907-149">RAM Requirement for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed907-150">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ed907-150">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-151">Todas as edições</span><span class="sxs-lookup"><span data-stu-id="ed907-151">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-152">N/A</span><span class="sxs-lookup"><span data-stu-id="ed907-152">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-153">64 bits</span><span class="sxs-lookup"><span data-stu-id="ed907-153">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-154">2 GB</span><span class="sxs-lookup"><span data-stu-id="ed907-154">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-155">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="ed907-155">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ed907-156">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ed907-156">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-157">Todas as edições</span><span class="sxs-lookup"><span data-stu-id="ed907-157">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-158">N/A</span><span class="sxs-lookup"><span data-stu-id="ed907-158">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-159">32 bits</span><span class="sxs-lookup"><span data-stu-id="ed907-159">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-160">1 GB</span><span class="sxs-lookup"><span data-stu-id="ed907-160">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-161">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="ed907-161">1.5 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> <span data-ttu-id="ed907-162">Requisitos do sistema do computador de suporte técnico DaRT</span><span class="sxs-lookup"><span data-stu-id="ed907-162">DaRT help desk computer system requirements</span></span>

<span data-ttu-id="ed907-163">Se você permitir que um suporte técnico ajude a solucionar problemas com computadores remotamente, você deve ter o Visualizador de conexão remota instalado no computador de suporte.</span><span class="sxs-lookup"><span data-stu-id="ed907-163">If you allow a help desk to remotely troubleshoot computers, you must have the Remote Connection Viewer installed on the help desk computer.</span></span> <span data-ttu-id="ed907-164">Opcionalmente, você pode instalar a ferramenta Crash Analyzer no computador de suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="ed907-164">You can optionally install the Crash Analyzer tool on the help desk computer.</span></span>

<span data-ttu-id="ed907-165">O DaRT 10 permite que um trabalhador de suporte técnico se conecte a um computador DaRT 10 usando o DaRT 7,0, o DaRT 8,0, o DaRt 8,1 ou o DaRT 10 Remote Connection Viewer.</span><span class="sxs-lookup"><span data-stu-id="ed907-165">DaRT 10 enables a help desk worker to connect to a DaRT 10 computer by using either the DaRT 7.0, DaRT 8.0, DaRt 8.1, or DaRT 10 Remote Connection Viewer.</span></span> <span data-ttu-id="ed907-166">O DaRT 7,0, o DaRT 8,0 e o DaRt 8,1, os visualizadores de conexão remota exigem os sistemas operacionais Windows 7, Windows 8 ou Windows 8,1, respectivamente, enquanto o Visualizador de conexão remota do DaRT 10 requer o Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ed907-166">The DaRT 7.0, DaRT 8.0 and DaRt 8.1, Remote Connection Viewers require Windows 7, Windows 8, or Windows 8.1 operating systems respectively, while the DaRT 10 Remote Connection Viewer requires Windows 10.</span></span> <span data-ttu-id="ed907-167">O Visualizador de conexão remota do DaRT 10 e todas as outras ferramentas do DaRT 10 podem ser instaladas apenas em um computador com Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ed907-167">The DaRT 10 Remote Connection Viewer and all other DaRT 10 tools can be installed only on a computer running Windows 10.</span></span>

<span data-ttu-id="ed907-168">A tabela a seguir lista os sistemas operacionais suportados para a instalação do computador do DaRT Help Desk.</span><span class="sxs-lookup"><span data-stu-id="ed907-168">The following table lists the operating systems that are supported for the DaRT help desk computer installation.</span></span>

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
<th align="left"><span data-ttu-id="ed907-169">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="ed907-169">Operating System</span></span></th>
<th align="left"><span data-ttu-id="ed907-170">Edição</span><span class="sxs-lookup"><span data-stu-id="ed907-170">Edition</span></span></th>
<th align="left"><span data-ttu-id="ed907-171">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ed907-171">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="ed907-172">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="ed907-172">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="ed907-173">Requisitos do Sistema Operacional</span><span class="sxs-lookup"><span data-stu-id="ed907-173">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="ed907-174">Requisitos de RAM para executar o DaRT</span><span class="sxs-lookup"><span data-stu-id="ed907-174">RAM Requirements for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed907-175">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ed907-175">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-176">Todas as edições</span><span class="sxs-lookup"><span data-stu-id="ed907-176">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-177">N/A</span><span class="sxs-lookup"><span data-stu-id="ed907-177">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-178">64 bits</span><span class="sxs-lookup"><span data-stu-id="ed907-178">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-179">2 GB</span><span class="sxs-lookup"><span data-stu-id="ed907-179">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-180">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="ed907-180">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ed907-181">Windows10 (somente com o Visualizador de conexão remota 10,0)</span><span class="sxs-lookup"><span data-stu-id="ed907-181">Windows10 (with Remote Connection Viewer 10.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-182">Todas as edições</span><span class="sxs-lookup"><span data-stu-id="ed907-182">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-183">N/A</span><span class="sxs-lookup"><span data-stu-id="ed907-183">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-184">32 bits</span><span class="sxs-lookup"><span data-stu-id="ed907-184">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-185">1 GB</span><span class="sxs-lookup"><span data-stu-id="ed907-185">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-186">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="ed907-186">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed907-187">Windows8</span><span class="sxs-lookup"><span data-stu-id="ed907-187">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-188">Todas as edições</span><span class="sxs-lookup"><span data-stu-id="ed907-188">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-189">N/A</span><span class="sxs-lookup"><span data-stu-id="ed907-189">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-190">64 bits</span><span class="sxs-lookup"><span data-stu-id="ed907-190">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-191">2 GB</span><span class="sxs-lookup"><span data-stu-id="ed907-191">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-192">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="ed907-192">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ed907-193">Windows8 (somente com o Visualizador de conexão remota 8,0)</span><span class="sxs-lookup"><span data-stu-id="ed907-193">Windows8 (with Remote Connection Viewer 8.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-194">Todas as edições</span><span class="sxs-lookup"><span data-stu-id="ed907-194">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-195">N/A</span><span class="sxs-lookup"><span data-stu-id="ed907-195">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-196">32 bits</span><span class="sxs-lookup"><span data-stu-id="ed907-196">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-197">1 GB</span><span class="sxs-lookup"><span data-stu-id="ed907-197">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-198">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="ed907-198">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed907-199">Windows 7 (somente com o Visualizador de conexão remota 7,0)</span><span class="sxs-lookup"><span data-stu-id="ed907-199">Windows 7 (with Remote Connection Viewer 7.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-200">Todas as edições</span><span class="sxs-lookup"><span data-stu-id="ed907-200">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-201">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="ed907-201">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-202">64 bits ou 32 bits</span><span class="sxs-lookup"><span data-stu-id="ed907-202">64-bit or 32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-203">1 GB</span><span class="sxs-lookup"><span data-stu-id="ed907-203">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-204">N/A</span><span class="sxs-lookup"><span data-stu-id="ed907-204">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ed907-205">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ed907-205">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-206">Padrão, corporativo, Data Center</span><span class="sxs-lookup"><span data-stu-id="ed907-206">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-207">N/A</span><span class="sxs-lookup"><span data-stu-id="ed907-207">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-208">64 bits</span><span class="sxs-lookup"><span data-stu-id="ed907-208">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-209">2 GB</span><span class="sxs-lookup"><span data-stu-id="ed907-209">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-210">1,0 GB</span><span class="sxs-lookup"><span data-stu-id="ed907-210">1.0 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed907-211">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ed907-211">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-212">Padrão, corporativo, Data Center</span><span class="sxs-lookup"><span data-stu-id="ed907-212">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-213">N/A</span><span class="sxs-lookup"><span data-stu-id="ed907-213">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-214">64 bits</span><span class="sxs-lookup"><span data-stu-id="ed907-214">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-215">2 GB</span><span class="sxs-lookup"><span data-stu-id="ed907-215">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-216">1,0 GB</span><span class="sxs-lookup"><span data-stu-id="ed907-216">1.0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ed907-217">O DaRT também tem os seguintes requisitos mínimos de hardware para o computador do usuário final:</span><span class="sxs-lookup"><span data-stu-id="ed907-217">DaRT also has the following minimum hardware requirements for the end-user computer:</span></span>

<span data-ttu-id="ed907-218">Uma unidade de CD ou DVD ou uma porta USB-necessária apenas se você estiver implantando o DaRT na sua empresa usando um CD, DVD ou USB.</span><span class="sxs-lookup"><span data-stu-id="ed907-218">A CD or DVD drive or a USB port - required only if you are deploying DaRT in your enterprise by using a CD, DVD, or USB.</span></span>

<span data-ttu-id="ed907-219">Suporte do BIOS para iniciar o computador a partir de um CD ou DVD, uma unidade flash USB ou de uma partição remota ou de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ed907-219">BIOS support for starting the computer from a CD or DVD, a USB flash drive, or from a remote or recovery partition.</span></span>

### <a href="" id="-------------dart-10-end-user-computer-system-requirements"></a> <span data-ttu-id="ed907-220">Requisitos do sistema para o computador de usuário final do DaRT 10</span><span class="sxs-lookup"><span data-stu-id="ed907-220">DaRT 10 end-user computer system requirements</span></span>

<span data-ttu-id="ed907-221">A janela do conjunto de ferramentas de diagnóstico e recuperação do DaRT 10 requer que o computador do usuário final use um dos seguintes sistemas operacionais juntamente com a quantidade especificada de memória do sistema disponível para o DaRT:</span><span class="sxs-lookup"><span data-stu-id="ed907-221">The Diagnostics and Recovery Toolset window in DaRT 10 requires that the end-user computer use one of the following operating systems together with the specified amount of system memory available for DaRT:</span></span>

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
<th align="left"><span data-ttu-id="ed907-222">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="ed907-222">Operating System</span></span></th>
<th align="left"><span data-ttu-id="ed907-223">Edição</span><span class="sxs-lookup"><span data-stu-id="ed907-223">Edition</span></span></th>
<th align="left"><span data-ttu-id="ed907-224">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ed907-224">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="ed907-225">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="ed907-225">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="ed907-226">Requisitos do Sistema Operacional</span><span class="sxs-lookup"><span data-stu-id="ed907-226">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="ed907-227">Requisitos de RAM</span><span class="sxs-lookup"><span data-stu-id="ed907-227">RAM Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed907-228">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ed907-228">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-229">Todas as edições</span><span class="sxs-lookup"><span data-stu-id="ed907-229">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-230">N/A</span><span class="sxs-lookup"><span data-stu-id="ed907-230">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-231">64 bits</span><span class="sxs-lookup"><span data-stu-id="ed907-231">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-232">2 GB</span><span class="sxs-lookup"><span data-stu-id="ed907-232">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-233">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="ed907-233">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ed907-234">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ed907-234">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-235">Todas as edições</span><span class="sxs-lookup"><span data-stu-id="ed907-235">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-236">N/A</span><span class="sxs-lookup"><span data-stu-id="ed907-236">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-237">32 bits</span><span class="sxs-lookup"><span data-stu-id="ed907-237">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-238">1 GB</span><span class="sxs-lookup"><span data-stu-id="ed907-238">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed907-239">1,5 GB</span><span class="sxs-lookup"><span data-stu-id="ed907-239">1.5 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ed907-240">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ed907-240">Related topics</span></span>


[<span data-ttu-id="ed907-241">Planejamento da implantação do DaRT 10</span><span class="sxs-lookup"><span data-stu-id="ed907-241">Planning to Deploy DaRT 10</span></span>](planning-to-deploy-dart-10.md)

 

 





