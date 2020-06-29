---
title: Implantando o Microsoft Office 2010 usando o App-V
description: Implantando o Microsoft Office 2010 usando o App-V
author: dansimp
ms.assetid: 0a9e496e-82a1-4dc0-a496-7b21eaa00f53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 303a44d921e40a411a4c4ea4622f06a76b8ed9c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796549"
---
# <span data-ttu-id="1c772-103">Implantando o Microsoft Office 2010 usando o App-V</span><span class="sxs-lookup"><span data-stu-id="1c772-103">Deploying Microsoft Office 2010 by Using App-V</span></span>


<span data-ttu-id="1c772-104">Você pode criar pacotes do Office 2010 para o Application Virtualization 5,0 usando um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="1c772-104">You can create Office 2010 packages for Application Virtualization 5.0 using one of the following methods:</span></span>

-   <span data-ttu-id="1c772-105">Sequenciador do Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="1c772-105">Application Virtualization (App-V) Sequencer</span></span>

-   <span data-ttu-id="1c772-106">Acelerador de pacote do Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="1c772-106">Application Virtualization (App-V) Package Accelerator</span></span>

## <span data-ttu-id="1c772-107">Suporte do App-V para o Office 2010</span><span class="sxs-lookup"><span data-stu-id="1c772-107">App-V support for Office 2010</span></span>


<span data-ttu-id="1c772-108">A tabela a seguir mostra as versões do App-V, os métodos de criação de pacotes do Office, o licenciamento com suporte e as implantações com suporte para o Office 2010.</span><span class="sxs-lookup"><span data-stu-id="1c772-108">The following table shows the App-V versions, methods of Office package creation, supported licensing, and supported deployments for Office 2010.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1c772-109">Item com suporte</span><span class="sxs-lookup"><span data-stu-id="1c772-109">Supported item</span></span></th>
<th align="left"><span data-ttu-id="1c772-110">Nível de suporte</span><span class="sxs-lookup"><span data-stu-id="1c772-110">Level of support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1c772-111">Versões do App-V com suporte</span><span class="sxs-lookup"><span data-stu-id="1c772-111">Supported App-V versions</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1c772-112">4,6</span><span class="sxs-lookup"><span data-stu-id="1c772-112">4.6</span></span></p></li>
<li><p><span data-ttu-id="1c772-113">5.0</span><span class="sxs-lookup"><span data-stu-id="1c772-113">5.0</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1c772-114">Criação de pacote</span><span class="sxs-lookup"><span data-stu-id="1c772-114">Package creation</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1c772-115">Sequenciamento</span><span class="sxs-lookup"><span data-stu-id="1c772-115">Sequencing</span></span></p></li>
<li><p><span data-ttu-id="1c772-116">Acelerador de pacote</span><span class="sxs-lookup"><span data-stu-id="1c772-116">Package Accelerator</span></span></p></li>
<li><p><span data-ttu-id="1c772-117">Kit de implantação do Office</span><span class="sxs-lookup"><span data-stu-id="1c772-117">Office Deployment Kit</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1c772-118">Licenciamento compatível</span><span class="sxs-lookup"><span data-stu-id="1c772-118">Supported licensing</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-119">Licenciamento por volume</span><span class="sxs-lookup"><span data-stu-id="1c772-119">Volume Licensing</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1c772-120">Implantações com suporte</span><span class="sxs-lookup"><span data-stu-id="1c772-120">Supported deployments</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="1c772-121">Desktop</span><span class="sxs-lookup"><span data-stu-id="1c772-121">Desktop</span></span></p></li>
<li><p><span data-ttu-id="1c772-122">VDI pessoal</span><span class="sxs-lookup"><span data-stu-id="1c772-122">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="1c772-123">AOS</span><span class="sxs-lookup"><span data-stu-id="1c772-123">RDS</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1c772-124">Criando o Office 2010 App-V 5,0 usando o sequenciador</span><span class="sxs-lookup"><span data-stu-id="1c772-124">Creating Office 2010 App-V 5.0 using the sequencer</span></span>


<span data-ttu-id="1c772-125">O sequenciamento do Office 2010 é um dos principais métodos para criar um pacote do Office 2010 no App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1c772-125">Sequencing Office 2010 is one of the main methods for creating an Office 2010 package on App-V 5.0.</span></span> <span data-ttu-id="1c772-126">A Microsoft forneceu uma receita detalhada por meio de um artigo da base de dados de conhecimento.</span><span class="sxs-lookup"><span data-stu-id="1c772-126">Microsoft has provided a detailed recipe through a Knowledge Base article.</span></span> <span data-ttu-id="1c772-127">Para criar um pacote do Office 2010 no App-V 5,0, consulte o link a seguir para obter instruções detalhadas:</span><span class="sxs-lookup"><span data-stu-id="1c772-127">To create an Office 2010 package on App-V 5.0, refer to the following link for detailed instructions:</span></span>

[<span data-ttu-id="1c772-128">Como sequenciar o Microsoft Office 2010 no Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="1c772-128">How To Sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

## <span data-ttu-id="1c772-129">Criando pacotes do Office 2010 App-V 5,0 usando aceleradores de pacote</span><span class="sxs-lookup"><span data-stu-id="1c772-129">Creating Office 2010 App-V 5.0 packages using package accelerators</span></span>


<span data-ttu-id="1c772-130">Os pacotes do Office 2010 App-V 5,0 podem ser criados por meio de aceleradores de pacote.</span><span class="sxs-lookup"><span data-stu-id="1c772-130">Office 2010 App-V 5.0 packages can be created through package accelerators.</span></span> <span data-ttu-id="1c772-131">A Microsoft fornece aceleradores de pacote para a criação do Office 2010 no Windows 8 e no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1c772-131">Microsoft has provided package accelerators for creating Office 2010 on Windows 8 and Windows 7.</span></span> <span data-ttu-id="1c772-132">Para criar pacotes do Office 2010 no App-V usando aceleradores de pacote, consulte as seguintes páginas para acessar o acelerador de pacote apropriado:</span><span class="sxs-lookup"><span data-stu-id="1c772-132">To create Office 2010 packages on App-V using Package accelerators, refer to the following pages to access the appropriate package accelerator:</span></span>

-   [<span data-ttu-id="1c772-133">Acelerador de pacote do App-V 5,0 para Office Professional Plus 2010 – Windows 8</span><span class="sxs-lookup"><span data-stu-id="1c772-133">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 8</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330677)

-   [<span data-ttu-id="1c772-134">Acelerador de pacote do App-V 5,0 para Office Professional Plus 2010 – Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c772-134">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 7</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330678)

<span data-ttu-id="1c772-135">Para obter instruções detalhadas sobre como criar pacotes de aplicativos virtuais usando aceleradores de pacotes do App-V, consulte [como criar um pacote de aplicativo virtual usando um acelerador de pacote app-v](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md).</span><span class="sxs-lookup"><span data-stu-id="1c772-135">For detailed instructions on how to create virtual application packages using App-V package accelerators, see [How to Create a Virtual Application Package Using an App-V Package Accelerator](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md).</span></span>

## <span data-ttu-id="1c772-136">Implantando o pacote do Microsoft Office para o App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="1c772-136">Deploying the Microsoft Office package for App-V 5.0</span></span>


<span data-ttu-id="1c772-137">Você pode implantar pacotes do Office 2010 usando qualquer um dos seguintes métodos de implantação do App-V:</span><span class="sxs-lookup"><span data-stu-id="1c772-137">You can deploy Office 2010 packages by using any of the following App-V deployment methods:</span></span>

-   <span data-ttu-id="1c772-138">System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="1c772-138">System Center Configuration Manager</span></span>

-   <span data-ttu-id="1c772-139">Servidor do App-V</span><span class="sxs-lookup"><span data-stu-id="1c772-139">App-V server</span></span>

-   <span data-ttu-id="1c772-140">Autônomos por meio de comandos do PowerShell</span><span class="sxs-lookup"><span data-stu-id="1c772-140">Stand-alone through PowerShell commands</span></span>

## <span data-ttu-id="1c772-141">Gerenciamento e personalização do Office App-V Package</span><span class="sxs-lookup"><span data-stu-id="1c772-141">Office App-V package management and customization</span></span>


<span data-ttu-id="1c772-142">Os pacotes do Office 2010 podem ser gerenciados como qualquer outro pacote do App-V 5,0 por meio de mecanismos de gerenciamento de pacotes conhecidos.</span><span class="sxs-lookup"><span data-stu-id="1c772-142">Office 2010 packages can be managed like any other App-V 5.0 packages through known package management mechanisms.</span></span> <span data-ttu-id="1c772-143">Nenhuma instrução especial é necessária, por exemplo, para adicionar, publicar, cancelar a publicação ou remover pacotes do Office.</span><span class="sxs-lookup"><span data-stu-id="1c772-143">No special instructions are needed, for example, to add, publish, unpublish, or remove Office packages.</span></span>

## <span data-ttu-id="1c772-144">Integração do Microsoft Office com o Windows</span><span class="sxs-lookup"><span data-stu-id="1c772-144">Microsoft Office integration with Windows</span></span>


<span data-ttu-id="1c772-145">A tabela a seguir fornece uma lista completa de pontos de integração com suporte para o Office 2010.</span><span class="sxs-lookup"><span data-stu-id="1c772-145">The following table provides a full list of supported integration points for Office 2010.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1c772-146">Ponto de extensão</span><span class="sxs-lookup"><span data-stu-id="1c772-146">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="1c772-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c772-147">Description</span></span></th>
<th align="left"><span data-ttu-id="1c772-148">Office 2010</span><span class="sxs-lookup"><span data-stu-id="1c772-148">Office 2010</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1c772-149">Plug-in de junção de reunião do Lync para Firefox e Chrome</span><span class="sxs-lookup"><span data-stu-id="1c772-149">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-150">O usuário pode ingressar em reuniões do Lync a partir do Firefox e do Chrome</span><span class="sxs-lookup"><span data-stu-id="1c772-150">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1c772-151">Enviado para o driver de impressão do OneNote</span><span class="sxs-lookup"><span data-stu-id="1c772-151">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-152">O usuário pode imprimir no OneNote</span><span class="sxs-lookup"><span data-stu-id="1c772-152">User can print to OneNote</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-153">Sim</span><span class="sxs-lookup"><span data-stu-id="1c772-153">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1c772-154">Anotações vinculadas do OneNote</span><span class="sxs-lookup"><span data-stu-id="1c772-154">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-155">Anotações vinculadas do OneNote</span><span class="sxs-lookup"><span data-stu-id="1c772-155">OneNote Linked Notes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1c772-156">Enviar para o suplemento do OneNote para Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="1c772-156">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-157">O usuário pode enviar para o OneNote do IE</span><span class="sxs-lookup"><span data-stu-id="1c772-157">User can send to OneNote from IE</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1c772-158">Exceção de firewall para o Lync e o Outlook</span><span class="sxs-lookup"><span data-stu-id="1c772-158">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-159">Exceção de firewall para o Lync e o Outlook</span><span class="sxs-lookup"><span data-stu-id="1c772-159">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1c772-160">Cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="1c772-160">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-161">Os aplicativos e suplementos nativos podem interagir com o Outlook virtual por MAPI</span><span class="sxs-lookup"><span data-stu-id="1c772-161">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1c772-162">Plug-in do SharePoint para Firefox</span><span class="sxs-lookup"><span data-stu-id="1c772-162">SharePoint Plugin for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-163">O usuário pode usar os recursos do SharePoint no Firefox</span><span class="sxs-lookup"><span data-stu-id="1c772-163">User can use SharePoint features in Firefox</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1c772-164">Applet do painel de controle de email</span><span class="sxs-lookup"><span data-stu-id="1c772-164">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-165">O usuário Obtém o applet do painel de controle de email no Outlook</span><span class="sxs-lookup"><span data-stu-id="1c772-165">User gets the mail control panel applet in Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-166">Sim</span><span class="sxs-lookup"><span data-stu-id="1c772-166">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1c772-167">Assemblies de interoperabilidade primária</span><span class="sxs-lookup"><span data-stu-id="1c772-167">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-168">Suporte a suplementos gerenciados</span><span class="sxs-lookup"><span data-stu-id="1c772-168">Support managed add-ins</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1c772-169">Manipulador do cache de documentos do Office</span><span class="sxs-lookup"><span data-stu-id="1c772-169">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-170">Permite o cache de documentos para aplicativos do Office</span><span class="sxs-lookup"><span data-stu-id="1c772-170">Allows Document Cache for Office applications</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1c772-171">Manipulador de pesquisa de protocolo do Outlook</span><span class="sxs-lookup"><span data-stu-id="1c772-171">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-172">O usuário pode pesquisar no Outlook</span><span class="sxs-lookup"><span data-stu-id="1c772-172">User can search in outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-173">Sim</span><span class="sxs-lookup"><span data-stu-id="1c772-173">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1c772-174">Controles ActiveX:</span><span class="sxs-lookup"><span data-stu-id="1c772-174">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-175">Para obter mais informações sobre controles ActiveX, consulte <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> referência da API do controle ActiveX </a> .</span><span class="sxs-lookup"><span data-stu-id="1c772-175">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1c772-176">Groove. SiteClient</span><span class="sxs-lookup"><span data-stu-id="1c772-176">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-177">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1c772-177">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1c772-178">PortalConnect.PersonalSite</span><span class="sxs-lookup"><span data-stu-id="1c772-178">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-179">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1c772-179">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1c772-180">SharePoint. openDocuments</span><span class="sxs-lookup"><span data-stu-id="1c772-180">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-181">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1c772-181">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1c772-182">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="1c772-182">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-183">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1c772-183">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1c772-184">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="1c772-184">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-185">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1c772-185">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1c772-186">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="1c772-186">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-187">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1c772-187">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1c772-188">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="1c772-188">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-189">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1c772-189">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1c772-190">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="1c772-190">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-191">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1c772-191">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1c772-192">Sharpoint.OpenXMLDocuments</span><span class="sxs-lookup"><span data-stu-id="1c772-192">Sharpoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-193">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1c772-193">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1c772-194">SharePoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="1c772-194">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-195">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1c772-195">Active X control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1c772-196">WinProj. Activator</span><span class="sxs-lookup"><span data-stu-id="1c772-196">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-197">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1c772-197">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1c772-198">Name. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="1c772-198">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-199">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1c772-199">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1c772-200">STSUPld.CopyCtl</span><span class="sxs-lookup"><span data-stu-id="1c772-200">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-201">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1c772-201">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1c772-202">CommunicatorMeetingJoinAx. Joinmanager</span><span class="sxs-lookup"><span data-stu-id="1c772-202">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-203">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1c772-203">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="1c772-204">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="1c772-204">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-205">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="1c772-205">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="1c772-206">Auxiliar do navegador do OneDrive pro</span><span class="sxs-lookup"><span data-stu-id="1c772-206">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-207">Controle ActiveX]</span><span class="sxs-lookup"><span data-stu-id="1c772-207">Active X Control]</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1c772-208">Sobreposições de ícones do OneDrive pro</span><span class="sxs-lookup"><span data-stu-id="1c772-208">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="1c772-209">O ícone do shell do Windows Explorer se sobrepõe quando os usuários confiram pastas pastas do OneDrive pro</span><span class="sxs-lookup"><span data-stu-id="1c772-209">Windows explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1c772-210">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="1c772-210">Additional resources</span></span>


**<span data-ttu-id="1c772-211">Pacotes do Office 2013 App-V 5,0 5,0 recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="1c772-211">Office 2013 App-V 5.0 Packages 5.0 Additional Resources</span></span>**

[<span data-ttu-id="1c772-212">Cenários suportados para a implantação do Microsoft Office como um pacote App-V sequenciado</span><span class="sxs-lookup"><span data-stu-id="1c772-212">Supported scenarios for deploying Microsoft Office as a sequenced App-V Package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**<span data-ttu-id="1c772-213">Pacotes do Office 2010 App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="1c772-213">Office 2010 App-V 5.0 Packages</span></span>**

[<span data-ttu-id="1c772-214">Kit de sequenciamento do Microsoft Office 2010 para Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="1c772-214">Microsoft Office 2010 Sequencing Kit for Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[<span data-ttu-id="1c772-215">Problemas conhecidos ao criar ou usar um pacote do App-V 5,0 do Office 2010</span><span class="sxs-lookup"><span data-stu-id="1c772-215">Known issues when you create or use an App-V 5.0 Office 2010 package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[<span data-ttu-id="1c772-216">Como sequenciar o Microsoft Office 2010 no Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="1c772-216">How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**<span data-ttu-id="1c772-217">Grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="1c772-217">Connection Groups</span></span>**

[<span data-ttu-id="1c772-218">Implantando grupos de conexão no Microsoft App-V V5</span><span class="sxs-lookup"><span data-stu-id="1c772-218">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="1c772-219">Gerenciando grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="1c772-219">Managing Connection Groups</span></span>](managing-connection-groups.md)

**<span data-ttu-id="1c772-220">Configuração dinâmica</span><span class="sxs-lookup"><span data-stu-id="1c772-220">Dynamic Configuration</span></span>**

[<span data-ttu-id="1c772-221">Sobre a configuração dinâmica do App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="1c772-221">About App-V 5.0 Dynamic Configuration</span></span>](about-app-v-50-dynamic-configuration.md)






 

 





