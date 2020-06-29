---
title: Implantando o Microsoft Office 2010 usando o App-V
description: Implantando o Microsoft Office 2010 usando o App-V
author: dansimp
ms.assetid: ae0b0459-c0d6-4946-b62d-ff153f52d1fb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 90454373e9a1c894eba8cbf1b8642656b986bc94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796546"
---
# <span data-ttu-id="61d3d-103">Implantando o Microsoft Office 2010 usando o App-V</span><span class="sxs-lookup"><span data-stu-id="61d3d-103">Deploying Microsoft Office 2010 by Using App-V</span></span>


<span data-ttu-id="61d3d-104">Você pode criar pacotes do Office 2010 para o Microsoft Application Virtualization (App-V) 5,1 usando um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="61d3d-104">You can create Office 2010 packages for Microsoft Application Virtualization (App-V) 5.1 using one of the following methods:</span></span>

-   <span data-ttu-id="61d3d-105">Sequenciador do Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="61d3d-105">Application Virtualization (App-V) Sequencer</span></span>

-   <span data-ttu-id="61d3d-106">Acelerador de pacote do Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="61d3d-106">Application Virtualization (App-V) Package Accelerator</span></span>

## <span data-ttu-id="61d3d-107">Suporte do App-V para o Office 2010</span><span class="sxs-lookup"><span data-stu-id="61d3d-107">App-V support for Office 2010</span></span>


<span data-ttu-id="61d3d-108">A tabela a seguir mostra as versões do App-V, os métodos de criação de pacotes do Office, o licenciamento com suporte e as implantações com suporte para o Office 2010.</span><span class="sxs-lookup"><span data-stu-id="61d3d-108">The following table shows the App-V versions, methods of Office package creation, supported licensing, and supported deployments for Office 2010.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="61d3d-109">Item com suporte</span><span class="sxs-lookup"><span data-stu-id="61d3d-109">Supported item</span></span></th>
<th align="left"><span data-ttu-id="61d3d-110">Nível de suporte</span><span class="sxs-lookup"><span data-stu-id="61d3d-110">Level of support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="61d3d-111">Versões do App-V com suporte</span><span class="sxs-lookup"><span data-stu-id="61d3d-111">Supported App-V versions</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="61d3d-112">4,6</span><span class="sxs-lookup"><span data-stu-id="61d3d-112">4.6</span></span></p></li>
<li><p><span data-ttu-id="61d3d-113">5.0</span><span class="sxs-lookup"><span data-stu-id="61d3d-113">5.0</span></span></p></li>
<li><p><span data-ttu-id="61d3d-114">5,1</span><span class="sxs-lookup"><span data-stu-id="61d3d-114">5.1</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="61d3d-115">Criação de pacote</span><span class="sxs-lookup"><span data-stu-id="61d3d-115">Package creation</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="61d3d-116">Sequenciamento</span><span class="sxs-lookup"><span data-stu-id="61d3d-116">Sequencing</span></span></p></li>
<li><p><span data-ttu-id="61d3d-117">Acelerador de pacote</span><span class="sxs-lookup"><span data-stu-id="61d3d-117">Package Accelerator</span></span></p></li>
<li><p><span data-ttu-id="61d3d-118">Kit de implantação do Office</span><span class="sxs-lookup"><span data-stu-id="61d3d-118">Office Deployment Kit</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="61d3d-119">Licenciamento compatível</span><span class="sxs-lookup"><span data-stu-id="61d3d-119">Supported licensing</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-120">Licenciamento por volume</span><span class="sxs-lookup"><span data-stu-id="61d3d-120">Volume Licensing</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="61d3d-121">Implantações com suporte</span><span class="sxs-lookup"><span data-stu-id="61d3d-121">Supported deployments</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="61d3d-122">Desktop</span><span class="sxs-lookup"><span data-stu-id="61d3d-122">Desktop</span></span></p></li>
<li><p><span data-ttu-id="61d3d-123">VDI pessoal</span><span class="sxs-lookup"><span data-stu-id="61d3d-123">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="61d3d-124">AOS</span><span class="sxs-lookup"><span data-stu-id="61d3d-124">RDS</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="61d3d-125">Criando o Office 2010 App-V 5,1 usando o sequenciador</span><span class="sxs-lookup"><span data-stu-id="61d3d-125">Creating Office 2010 App-V 5.1 using the sequencer</span></span>


<span data-ttu-id="61d3d-126">O sequenciamento do Office 2010 é um dos principais métodos para criar um pacote do Office 2010 no App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="61d3d-126">Sequencing Office 2010 is one of the main methods for creating an Office 2010 package on App-V 5.1.</span></span> <span data-ttu-id="61d3d-127">A Microsoft forneceu uma receita detalhada por meio de um artigo da base de dados de conhecimento.</span><span class="sxs-lookup"><span data-stu-id="61d3d-127">Microsoft has provided a detailed recipe through a Knowledge Base article.</span></span> <span data-ttu-id="61d3d-128">Para criar um pacote do Office 2010 no App-V 5,1, consulte o link a seguir para obter instruções detalhadas:</span><span class="sxs-lookup"><span data-stu-id="61d3d-128">To create an Office 2010 package on App-V 5.1, refer to the following link for detailed instructions:</span></span>

[<span data-ttu-id="61d3d-129">Como sequenciar o Microsoft Office 2010 no Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="61d3d-129">How To Sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

## <span data-ttu-id="61d3d-130">Criando pacotes do Office 2010 App-V 5,1 usando aceleradores de pacote</span><span class="sxs-lookup"><span data-stu-id="61d3d-130">Creating Office 2010 App-V 5.1 packages using package accelerators</span></span>


<span data-ttu-id="61d3d-131">Os pacotes do Office 2010 App-V 5,1 podem ser criados por meio de aceleradores de pacote.</span><span class="sxs-lookup"><span data-stu-id="61d3d-131">Office 2010 App-V 5.1 packages can be created through package accelerators.</span></span> <span data-ttu-id="61d3d-132">A Microsoft fornece aceleradores de pacote para a criação do Office 2010 no Windows 10, no Windows 8 e no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="61d3d-132">Microsoft has provided package accelerators for creating Office 2010 on Windows 10, Windows 8 and Windows 7.</span></span> <span data-ttu-id="61d3d-133">Para criar pacotes do Office 2010 no App-V usando aceleradores de pacote, consulte as seguintes páginas para acessar o acelerador de pacote apropriado:</span><span class="sxs-lookup"><span data-stu-id="61d3d-133">To create Office 2010 packages on App-V using Package accelerators, refer to the following pages to access the appropriate package accelerator:</span></span>

-   [<span data-ttu-id="61d3d-134">Acelerador de pacote do App-V 5,0 para Office Professional Plus 2010 – Windows 8</span><span class="sxs-lookup"><span data-stu-id="61d3d-134">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 8</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330677)

-   [<span data-ttu-id="61d3d-135">Acelerador de pacote do App-V 5,0 para Office Professional Plus 2010 – Windows 7</span><span class="sxs-lookup"><span data-stu-id="61d3d-135">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 7</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330678)

<span data-ttu-id="61d3d-136">Para obter instruções detalhadas sobre como criar pacotes de aplicativos virtuais usando aceleradores de pacotes do App-V, consulte [como criar um pacote de aplicativo virtual usando um acelerador de pacote app-v](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md).</span><span class="sxs-lookup"><span data-stu-id="61d3d-136">For detailed instructions on how to create virtual application packages using App-V package accelerators, see [How to Create a Virtual Application Package Using an App-V Package Accelerator](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md).</span></span>

## <span data-ttu-id="61d3d-137">Implantando o pacote do Microsoft Office para o App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="61d3d-137">Deploying the Microsoft Office package for App-V 5.1</span></span>


<span data-ttu-id="61d3d-138">Você pode implantar pacotes do Office 2010 usando qualquer um dos seguintes métodos de implantação do App-V:</span><span class="sxs-lookup"><span data-stu-id="61d3d-138">You can deploy Office 2010 packages by using any of the following App-V deployment methods:</span></span>

-   <span data-ttu-id="61d3d-139">System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="61d3d-139">System Center Configuration Manager</span></span>

-   <span data-ttu-id="61d3d-140">Servidor do App-V</span><span class="sxs-lookup"><span data-stu-id="61d3d-140">App-V server</span></span>

-   <span data-ttu-id="61d3d-141">Autônomos por meio de comandos do PowerShell</span><span class="sxs-lookup"><span data-stu-id="61d3d-141">Stand-alone through PowerShell commands</span></span>

## <span data-ttu-id="61d3d-142">Gerenciamento e personalização do Office App-V Package</span><span class="sxs-lookup"><span data-stu-id="61d3d-142">Office App-V package management and customization</span></span>


<span data-ttu-id="61d3d-143">Os pacotes do Office 2010 podem ser gerenciados como qualquer outro pacote do App-V 5,1 por meio de mecanismos de gerenciamento de pacotes conhecidos.</span><span class="sxs-lookup"><span data-stu-id="61d3d-143">Office 2010 packages can be managed like any other App-V 5.1 packages through known package management mechanisms.</span></span> <span data-ttu-id="61d3d-144">Nenhuma instrução especial é necessária, por exemplo, para adicionar, publicar, cancelar a publicação ou remover pacotes do Office.</span><span class="sxs-lookup"><span data-stu-id="61d3d-144">No special instructions are needed, for example, to add, publish, unpublish, or remove Office packages.</span></span>

## <span data-ttu-id="61d3d-145">Integração do Microsoft Office com o Windows</span><span class="sxs-lookup"><span data-stu-id="61d3d-145">Microsoft Office integration with Windows</span></span>


<span data-ttu-id="61d3d-146">A tabela a seguir fornece uma lista completa de pontos de integração com suporte para o Office 2010.</span><span class="sxs-lookup"><span data-stu-id="61d3d-146">The following table provides a full list of supported integration points for Office 2010.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="61d3d-147">Ponto de extensão</span><span class="sxs-lookup"><span data-stu-id="61d3d-147">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="61d3d-148">Descrição</span><span class="sxs-lookup"><span data-stu-id="61d3d-148">Description</span></span></th>
<th align="left"><span data-ttu-id="61d3d-149">Office 2010</span><span class="sxs-lookup"><span data-stu-id="61d3d-149">Office 2010</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="61d3d-150">Plug-in de junção de reunião do Lync para Firefox e Chrome</span><span class="sxs-lookup"><span data-stu-id="61d3d-150">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-151">O usuário pode ingressar em reuniões do Lync a partir do Firefox e do Chrome</span><span class="sxs-lookup"><span data-stu-id="61d3d-151">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="61d3d-152">Enviado para o driver de impressão do OneNote</span><span class="sxs-lookup"><span data-stu-id="61d3d-152">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-153">O usuário pode imprimir no OneNote</span><span class="sxs-lookup"><span data-stu-id="61d3d-153">User can print to OneNote</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-154">Sim</span><span class="sxs-lookup"><span data-stu-id="61d3d-154">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="61d3d-155">Anotações vinculadas do OneNote</span><span class="sxs-lookup"><span data-stu-id="61d3d-155">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-156">Anotações vinculadas do OneNote</span><span class="sxs-lookup"><span data-stu-id="61d3d-156">OneNote Linked Notes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="61d3d-157">Enviar para o suplemento do OneNote para Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="61d3d-157">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-158">O usuário pode enviar para o OneNote do IE</span><span class="sxs-lookup"><span data-stu-id="61d3d-158">User can send to OneNote from IE</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="61d3d-159">Exceção de firewall para o Lync e o Outlook</span><span class="sxs-lookup"><span data-stu-id="61d3d-159">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-160">Exceção de firewall para o Lync e o Outlook</span><span class="sxs-lookup"><span data-stu-id="61d3d-160">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="61d3d-161">Cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="61d3d-161">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-162">Os aplicativos e suplementos nativos podem interagir com o Outlook virtual por MAPI</span><span class="sxs-lookup"><span data-stu-id="61d3d-162">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="61d3d-163">Plug-in do SharePoint para Firefox</span><span class="sxs-lookup"><span data-stu-id="61d3d-163">SharePoint Plugin for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-164">O usuário pode usar os recursos do SharePoint no Firefox</span><span class="sxs-lookup"><span data-stu-id="61d3d-164">User can use SharePoint features in Firefox</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="61d3d-165">Applet do painel de controle de email</span><span class="sxs-lookup"><span data-stu-id="61d3d-165">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-166">O usuário Obtém o applet do painel de controle de email no Outlook</span><span class="sxs-lookup"><span data-stu-id="61d3d-166">User gets the mail control panel applet in Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-167">Sim</span><span class="sxs-lookup"><span data-stu-id="61d3d-167">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="61d3d-168">Assemblies de interoperabilidade primária</span><span class="sxs-lookup"><span data-stu-id="61d3d-168">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-169">Suporte a suplementos gerenciados</span><span class="sxs-lookup"><span data-stu-id="61d3d-169">Support managed add-ins</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="61d3d-170">Manipulador do cache de documentos do Office</span><span class="sxs-lookup"><span data-stu-id="61d3d-170">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-171">Permite o cache de documentos para aplicativos do Office</span><span class="sxs-lookup"><span data-stu-id="61d3d-171">Allows Document Cache for Office applications</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="61d3d-172">Manipulador de pesquisa de protocolo do Outlook</span><span class="sxs-lookup"><span data-stu-id="61d3d-172">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-173">O usuário pode pesquisar no Outlook</span><span class="sxs-lookup"><span data-stu-id="61d3d-173">User can search in outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-174">Sim</span><span class="sxs-lookup"><span data-stu-id="61d3d-174">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="61d3d-175">Controles ActiveX:</span><span class="sxs-lookup"><span data-stu-id="61d3d-175">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-176">Para obter mais informações sobre controles ActiveX, consulte <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> referência da API do controle ActiveX </a> .</span><span class="sxs-lookup"><span data-stu-id="61d3d-176">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="61d3d-177">Groove. SiteClient</span><span class="sxs-lookup"><span data-stu-id="61d3d-177">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-178">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="61d3d-178">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="61d3d-179">PortalConnect.PersonalSite</span><span class="sxs-lookup"><span data-stu-id="61d3d-179">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-180">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="61d3d-180">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="61d3d-181">SharePoint. openDocuments</span><span class="sxs-lookup"><span data-stu-id="61d3d-181">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-182">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="61d3d-182">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="61d3d-183">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="61d3d-183">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-184">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="61d3d-184">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="61d3d-185">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="61d3d-185">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-186">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="61d3d-186">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="61d3d-187">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="61d3d-187">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-188">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="61d3d-188">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="61d3d-189">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="61d3d-189">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-190">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="61d3d-190">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="61d3d-191">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="61d3d-191">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-192">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="61d3d-192">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="61d3d-193">Sharpoint.OpenXMLDocuments</span><span class="sxs-lookup"><span data-stu-id="61d3d-193">Sharpoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-194">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="61d3d-194">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="61d3d-195">SharePoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="61d3d-195">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-196">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="61d3d-196">Active X control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="61d3d-197">WinProj. Activator</span><span class="sxs-lookup"><span data-stu-id="61d3d-197">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-198">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="61d3d-198">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="61d3d-199">Name. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="61d3d-199">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-200">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="61d3d-200">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="61d3d-201">STSUPld.CopyCtl</span><span class="sxs-lookup"><span data-stu-id="61d3d-201">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-202">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="61d3d-202">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="61d3d-203">CommunicatorMeetingJoinAx. Joinmanager</span><span class="sxs-lookup"><span data-stu-id="61d3d-203">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-204">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="61d3d-204">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="61d3d-205">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="61d3d-205">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-206">Controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="61d3d-206">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="61d3d-207">Auxiliar do navegador do OneDrive pro</span><span class="sxs-lookup"><span data-stu-id="61d3d-207">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-208">Controle ActiveX]</span><span class="sxs-lookup"><span data-stu-id="61d3d-208">Active X Control]</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="61d3d-209">Sobreposições de ícones do OneDrive pro</span><span class="sxs-lookup"><span data-stu-id="61d3d-209">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="61d3d-210">O ícone do shell do Windows Explorer se sobrepõe quando os usuários confiram pastas pastas do OneDrive pro</span><span class="sxs-lookup"><span data-stu-id="61d3d-210">Windows explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="61d3d-211">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="61d3d-211">Additional resources</span></span>


**<span data-ttu-id="61d3d-212">Recursos adicionais dos pacotes do Office 2013 App-V</span><span class="sxs-lookup"><span data-stu-id="61d3d-212">Office 2013 App-V Packages Additional Resources</span></span>**

[<span data-ttu-id="61d3d-213">Cenários suportados para a implantação do Microsoft Office como um pacote App-V sequenciado</span><span class="sxs-lookup"><span data-stu-id="61d3d-213">Supported scenarios for deploying Microsoft Office as a sequenced App-V Package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**<span data-ttu-id="61d3d-214">Pacotes do Office 2010 App-V</span><span class="sxs-lookup"><span data-stu-id="61d3d-214">Office 2010 App-V Packages</span></span>**

[<span data-ttu-id="61d3d-215">Kit de sequenciamento do Microsoft Office 2010 para Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="61d3d-215">Microsoft Office 2010 Sequencing Kit for Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[<span data-ttu-id="61d3d-216">Problemas conhecidos ao criar ou usar um pacote do App-V 5,0 do Office 2010</span><span class="sxs-lookup"><span data-stu-id="61d3d-216">Known issues when you create or use an App-V 5.0 Office 2010 package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[<span data-ttu-id="61d3d-217">Como sequenciar o Microsoft Office 2010 no Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="61d3d-217">How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**<span data-ttu-id="61d3d-218">Grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="61d3d-218">Connection Groups</span></span>**

[<span data-ttu-id="61d3d-219">Implantando grupos de conexão no Microsoft App-V V5</span><span class="sxs-lookup"><span data-stu-id="61d3d-219">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="61d3d-220">Gerenciando grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="61d3d-220">Managing Connection Groups</span></span>](managing-connection-groups51.md)

**<span data-ttu-id="61d3d-221">Configuração dinâmica</span><span class="sxs-lookup"><span data-stu-id="61d3d-221">Dynamic Configuration</span></span>**

[<span data-ttu-id="61d3d-222">Sobre a configuração dinâmica do App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="61d3d-222">About App-V 5.1 Dynamic Configuration</span></span>](about-app-v-51-dynamic-configuration.md)






 

 





