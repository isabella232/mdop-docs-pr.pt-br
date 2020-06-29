---
title: Preparar uma implantação do UE-V 2. x
description: Preparar uma implantação do UE-V 2. x
author: dansimp
ms.assetid: c429fd06-13ff-48c5-b9c9-fa1ec01ab800
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: e6b2de407990536e1a08532632dcea19ea0d0ee9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799869"
---
# <span data-ttu-id="169b7-103">Preparar uma implantação do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="169b7-103">Prepare a UE-V 2.x Deployment</span></span>


<span data-ttu-id="169b7-104">Há algum planejamento e preparação antes de implantar o Microsoft User Experience Virtualization (UE-V) 2,0 ou 2,1 como uma solução para sincronizar as configurações entre dispositivos que os usuários acessam na sua empresa.</span><span class="sxs-lookup"><span data-stu-id="169b7-104">There is some planning and preparation to do before you deploy Microsoft User Experience Virtualization (UE-V) 2.0 or 2.1 as a solution for synchronizing settings between devices that users access in your enterprise.</span></span> <span data-ttu-id="169b7-105">Este tópico ajuda você a determinar o tipo de implantação que fará e qual será a preparação que você pode fazer de antemão para que sua implantação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="169b7-105">This topic helps you determine what type of deployment you'll be doing and what preparation you can make beforehand so that your deployment is successful.</span></span>

<span data-ttu-id="169b7-106">Primeiro, vamos dar uma olhada nas tarefas que você vai fazer para implantar o UE-V:</span><span class="sxs-lookup"><span data-stu-id="169b7-106">First, let’s look at the tasks you’ll do to deploy UE-V:</span></span>

-   <span data-ttu-id="169b7-107">Planejar a implantação do UE-V</span><span class="sxs-lookup"><span data-stu-id="169b7-107">Plan your UE-V Deployment</span></span>

    <span data-ttu-id="169b7-108">Antes de implantar qualquer coisa, uma boa primeira etapa é fazer um pouco de planejamento para que você possa determinar quais recursos do UE-V você vai implantar.</span><span class="sxs-lookup"><span data-stu-id="169b7-108">Before you deploy anything, a good first step is to do a little bit of planning so that you can determine which UE-V features you’ll deploy.</span></span> <span data-ttu-id="169b7-109">Portanto, se você sair desta página, verifique se voltou e leu as informações de planejamento abaixo.</span><span class="sxs-lookup"><span data-stu-id="169b7-109">So if you leave this page, make sure you come back and read through the planning information below.</span></span>

-   [<span data-ttu-id="169b7-110">Implantar os recursos necessários na UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="169b7-110">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md)

    <span data-ttu-id="169b7-111">Toda a implantação do UE-V requer estas atividades:</span><span class="sxs-lookup"><span data-stu-id="169b7-111">Every UE-V deployment requires these activities:</span></span>

    -   [<span data-ttu-id="169b7-112">Definir um local de armazenamento de configurações</span><span class="sxs-lookup"><span data-stu-id="169b7-112">Define a settings storage location</span></span>](https://technet.microsoft.com/library/dn458891.aspx#ssl)

    -   [<span data-ttu-id="169b7-113">Decidir como implantar o UE-V Agent e gerenciar as configurações de UE-V</span><span class="sxs-lookup"><span data-stu-id="169b7-113">Decide how to deploy the UE-V Agent and manage UE-V configurations</span></span>](https://technet.microsoft.com/library/dn458891.aspx#config)

    -   <span data-ttu-id="169b7-114">[Instalar o UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) em cada computador do usuário que precisa de configurações sincronizadas</span><span class="sxs-lookup"><span data-stu-id="169b7-114">[Install the UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) on every user computer that needs settings synchronized</span></span>

-   <span data-ttu-id="169b7-115">Opcionalmente, você pode [implantar o UE-V 2. x para aplicativos personalizados](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)</span><span class="sxs-lookup"><span data-stu-id="169b7-115">Optionally, you can [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)</span></span>

    <span data-ttu-id="169b7-116">O planejamento vai ajudá-lo a descobrir se você deseja que o UE-V ofereça suporte à sincronização de configurações para aplicativos personalizados (de terceiros ou de linha de negócios), o que exige estes recursos de UE-V:</span><span class="sxs-lookup"><span data-stu-id="169b7-116">Planning will help you figure out whether you want UE-V to support the synchronization of settings for custom applications (third-party or line-of-business), which requires these UE-V features:</span></span>

    -   <span data-ttu-id="169b7-117">[Instale o gerador UEV](https://technet.microsoft.com/library/dn458942.aspx#uevgen) para que você possa criar, editar e validar os modelos de local de configurações personalizadas necessários para sincronizar as configurações de aplicativo personalizadas</span><span class="sxs-lookup"><span data-stu-id="169b7-117">[Install the UEV Generator](https://technet.microsoft.com/library/dn458942.aspx#uevgen) so you can create, edit, and validate the custom settings location templates required to synchronize custom application settings</span></span>

    -   <span data-ttu-id="169b7-118">[Criar modelos de local de configurações personalizadas](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) usando o UE-V Generator</span><span class="sxs-lookup"><span data-stu-id="169b7-118">[Create custom settings location templates](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) by using the UE-V Generator</span></span>

    -   <span data-ttu-id="169b7-119">[Implantar um catálogo de modelos de configurações do UE-V](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) que você usa para armazenar seus modelos de local de configurações personalizadas</span><span class="sxs-lookup"><span data-stu-id="169b7-119">[Deploy a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) that you use to store your custom settings location templates</span></span>

<span data-ttu-id="169b7-120">Este diagrama de fluxo de trabalho fornece uma compreensão de alto nível de uma implantação do UE-V e das decisões que determinam como você implanta o UE-V na sua empresa.</span><span class="sxs-lookup"><span data-stu-id="169b7-120">This workflow diagram provides a high-level understanding of a UE-V deployment and the decisions that determine how you deploy UE-V in your enterprise.</span></span>

![deploymentworkflow](images/deploymentworkflow.png)

<span data-ttu-id="169b7-122">**Planejando uma implantação do UE-V:** Primeiro, você deseja fazer um pouco de planejamento para poder determinar quais componentes do UE-V você vai implantar.</span><span class="sxs-lookup"><span data-stu-id="169b7-122">**Planning a UE-V deployment:** First, you want to do a little bit of planning so that you can determine which UE-V components you’ll be deploying.</span></span> <span data-ttu-id="169b7-123">Planejar uma implantação do UE-V envolve estas coisas:</span><span class="sxs-lookup"><span data-stu-id="169b7-123">Planning a UE-V deployment involves these things:</span></span>

-   [<span data-ttu-id="169b7-124">Decida se deseja sincronizar as configurações para aplicativos personalizados</span><span class="sxs-lookup"><span data-stu-id="169b7-124">Decide whether to synchronize settings for custom applications</span></span>](#deciding)

    <span data-ttu-id="169b7-125">Isso determina se você vai instalar o UE-V Generator durante a implantação, o que permite criar modelos de local de configurações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="169b7-125">This determines whether you will install the UE-V Generator during deployment, which lets you create custom settings location templates.</span></span> <span data-ttu-id="169b7-126">Ele envolve o seguinte:</span><span class="sxs-lookup"><span data-stu-id="169b7-126">It involves the following:</span></span>

    <span data-ttu-id="169b7-127">Examine as [configurações que são sincronizadas automaticamente em uma implantação de UE-V](#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="169b7-127">Review the [settings that are synchronized automatically in a UE-V deployment](#autosyncsettings).</span></span>

    <span data-ttu-id="169b7-128">[Determine se você precisa de configurações sincronizadas para outros aplicativos](#determinesettingssync).</span><span class="sxs-lookup"><span data-stu-id="169b7-128">[Determine whether you need settings synchronized for other applications](#determinesettingssync).</span></span>

-   <span data-ttu-id="169b7-129">Revise [outras considerações para a implantação do UE-V](#considerations), como alta disponibilidade e planejamento de capacidade.</span><span class="sxs-lookup"><span data-stu-id="169b7-129">Review [other considerations for deploying UE-V](#considerations), such as high availability and capacity planning.</span></span>

-   [<span data-ttu-id="169b7-130">Confirme pré-requisitos e configurações com suporte para UE-V</span><span class="sxs-lookup"><span data-stu-id="169b7-130">Confirm prerequisites and supported configurations for UE-V</span></span>](#prereqs)

## <a href="" id="deciding"></a><span data-ttu-id="169b7-131">Decida se deseja sincronizar as configurações para aplicativos personalizados</span><span class="sxs-lookup"><span data-stu-id="169b7-131">Decide Whether to Synchronize Settings for Custom Applications</span></span>


<span data-ttu-id="169b7-132">Em uma implantação do UE-V, muitas configurações são sincronizadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="169b7-132">In a UE-V deployment, many settings are automatically synchronized.</span></span> <span data-ttu-id="169b7-133">Mas você também pode personalizar o UE-V para sincronizar as configurações de outros aplicativos, como linha de negócios e aplicativos de terceiros.</span><span class="sxs-lookup"><span data-stu-id="169b7-133">But you can also customize UE-V to synchronize settings for other applications, such as line-of-business and third-party apps.</span></span>

<span data-ttu-id="169b7-134">Decidir se você deseja que o UE-V sincronize as configurações para aplicativos personalizados é provavelmente a parte mais importante de planejar sua implantação do UE-V.</span><span class="sxs-lookup"><span data-stu-id="169b7-134">Deciding if you want UE-V to synchronize settings for custom applications is probably the most important part of planning your UE-V deployment.</span></span> <span data-ttu-id="169b7-135">Os tópicos desta seção ajudarão você a tomar essa decisão.</span><span class="sxs-lookup"><span data-stu-id="169b7-135">The topics in this section will help you make that decision.</span></span>

### <a href="" id="autosyncsettings"></a><span data-ttu-id="169b7-136">Configurações que são sincronizadas automaticamente em uma implantação do UE-V</span><span class="sxs-lookup"><span data-stu-id="169b7-136">Settings that are automatically synchronized in a UE-V deployment</span></span>

<span data-ttu-id="169b7-137">Esta seção fornece informações sobre as configurações que são sincronizadas por padrão no UE-V, incluindo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="169b7-137">This section provides information about the settings that are synchronized by default in UE-V, including the following:</span></span>

<span data-ttu-id="169b7-138">Aplicativos da área de trabalho cujas configurações são sincronizadas por padrão</span><span class="sxs-lookup"><span data-stu-id="169b7-138">Desktop applications whose settings are synchronized by default</span></span>

<span data-ttu-id="169b7-139">Configurações da área de trabalho do Windows que são sincronizadas por padrão</span><span class="sxs-lookup"><span data-stu-id="169b7-139">Windows desktop settings that are synchronized by default</span></span>

<span data-ttu-id="169b7-140">Uma declaração de suporte para a sincronização de configuração do aplicativo Windows</span><span class="sxs-lookup"><span data-stu-id="169b7-140">A statement of support for Windows app setting synchronization</span></span>

<span data-ttu-id="169b7-141">Consulte [modelos de configurações do User Experience Virtualization (UE-V) para que o Microsoft Office](https://www.microsoft.com/download/details.aspx?id=46367) Baixe uma lista completa das configurações específicas do microsoft Office 2013, do microsoft Office 2010 e do microsoft Office 2007 que são sincronizadas por UE-V.</span><span class="sxs-lookup"><span data-stu-id="169b7-141">See [User Experience Virtualization (UE-V) settings templates for Microsoft Office](https://www.microsoft.com/download/details.aspx?id=46367) to download a complete list of the specific Microsoft Office 2013, Microsoft Office 2010, and Microsoft Office 2007 settings that are synchronized by UE-V.</span></span>

### <span data-ttu-id="169b7-142">Aplicativos da área de trabalho sincronizados por padrão no UE-V 2,1 e no UE-V 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="169b7-142">Desktop applications synchronized by default in UE-V 2.1 and UE-V 2.1 SP1</span></span>

<span data-ttu-id="169b7-143">Quando você instala o agente do UE-V 2,1 ou do 2,1 SP1, ele registra um grupo padrão de modelos de local de configurações que capturam valores de configurações para esses aplicativos comuns da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="169b7-143">When you install the UE-V 2.1 or 2.1 SP1 Agent, it registers a default group of settings location templates that capture settings values for these common Microsoft applications.</span></span>

**<span data-ttu-id="169b7-144">Dica</span><span class="sxs-lookup"><span data-stu-id="169b7-144">Tip</span></span>**  
<span data-ttu-id="169b7-145">**Sincronização de configurações do Microsoft Office 2007** – no UE-V 2,1 e no 2,1 SP1, um modelo de local de configurações não é mais incluído por padrão para aplicativos do Office 2007.</span><span class="sxs-lookup"><span data-stu-id="169b7-145">**Microsoft Office 2007 Settings Synchronization** – In UE-V 2.1 and 2.1 SP1, a settings location template is no longer included by default for Office 2007 applications.</span></span> <span data-ttu-id="169b7-146">No entanto, você ainda pode usar os modelos do Office 2007 do UE-V 2,0 ou anterior e pode obter os modelos da [Galeria de modelos do UE-v](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span><span class="sxs-lookup"><span data-stu-id="169b7-146">However, you can still use Office 2007 templates from UE-V 2.0 or earlier and can get the templates from the [UE-V template gallery](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="169b7-147">Categoria do aplicativo</span><span class="sxs-lookup"><span data-stu-id="169b7-147">Application category</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="169b7-148">Descrição</span><span class="sxs-lookup"><span data-stu-id="169b7-148">Description</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="169b7-149">Aplicativos do Microsoft Office 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-149">Microsoft Office 2010 applications</span></span></p>
<p><span data-ttu-id="169b7-150">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Baixar uma lista de todas as configurações sincronizadas </a> )</span><span class="sxs-lookup"><span data-stu-id="169b7-150">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-151">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-151">Microsoft Word 2010</span></span></p>
<p><span data-ttu-id="169b7-152">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-152">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="169b7-153">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-153">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="169b7-154">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-154">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="169b7-155">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-155">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="169b7-156">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-156">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="169b7-157">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-157">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="169b7-158">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-158">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="169b7-159">Microsoft SharePoint Workspace 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-159">Microsoft SharePoint Workspace 2010</span></span></p>
<p><span data-ttu-id="169b7-160">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-160">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="169b7-161">Microsoft Lync 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-161">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="169b7-162">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-162">Microsoft OneNote 2010</span></span></p>
<p><span data-ttu-id="169b7-163">Microsoft SharePoint Designer 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-163">Microsoft SharePoint Designer 2010</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="169b7-164">Aplicativos do Microsoft Office 2013</span><span class="sxs-lookup"><span data-stu-id="169b7-164">Microsoft Office 2013 applications</span></span></p>
<p><span data-ttu-id="169b7-165">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Baixar uma lista de todas as configurações sincronizadas </a> )</span><span class="sxs-lookup"><span data-stu-id="169b7-165">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-166">Microsoft Word 2013</span><span class="sxs-lookup"><span data-stu-id="169b7-166">Microsoft Word 2013</span></span></p>
<p><span data-ttu-id="169b7-167">Microsoft Excel 2013</span><span class="sxs-lookup"><span data-stu-id="169b7-167">Microsoft Excel 2013</span></span></p>
<p><span data-ttu-id="169b7-168">Microsoft Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="169b7-168">Microsoft Outlook 2013</span></span></p>
<p><span data-ttu-id="169b7-169">Microsoft Access 2013</span><span class="sxs-lookup"><span data-stu-id="169b7-169">Microsoft Access 2013</span></span></p>
<p><span data-ttu-id="169b7-170">Microsoft Project 2013</span><span class="sxs-lookup"><span data-stu-id="169b7-170">Microsoft Project 2013</span></span></p>
<p><span data-ttu-id="169b7-171">Microsoft PowerPoint 2013</span><span class="sxs-lookup"><span data-stu-id="169b7-171">Microsoft PowerPoint 2013</span></span></p>
<p><span data-ttu-id="169b7-172">Microsoft Publisher 2013</span><span class="sxs-lookup"><span data-stu-id="169b7-172">Microsoft Publisher 2013</span></span></p>
<p><span data-ttu-id="169b7-173">Microsoft Visio 2013</span><span class="sxs-lookup"><span data-stu-id="169b7-173">Microsoft Visio 2013</span></span></p>
<p><span data-ttu-id="169b7-174">Microsoft InfoPath 2013</span><span class="sxs-lookup"><span data-stu-id="169b7-174">Microsoft InfoPath 2013</span></span></p>
<p><span data-ttu-id="169b7-175">Microsoft Lync 2013</span><span class="sxs-lookup"><span data-stu-id="169b7-175">Microsoft Lync 2013</span></span></p>
<p><span data-ttu-id="169b7-176">Microsoft OneNote 2013</span><span class="sxs-lookup"><span data-stu-id="169b7-176">Microsoft OneNote 2013</span></span></p>
<p><span data-ttu-id="169b7-177">Microsoft SharePoint Designer 2013</span><span class="sxs-lookup"><span data-stu-id="169b7-177">Microsoft SharePoint Designer 2013</span></span></p>
<p><span data-ttu-id="169b7-178">Centro de carregamento do Microsoft Office 2013</span><span class="sxs-lookup"><span data-stu-id="169b7-178">Microsoft Office 2013 Upload Center</span></span></p>
<p><span data-ttu-id="169b7-179">Microsoft OneDrive for Business 2013</span><span class="sxs-lookup"><span data-stu-id="169b7-179">Microsoft OneDrive for Business 2013</span></span></p>
<p><span data-ttu-id="169b7-180">Os modelos de local de configurações do UE-V 2,1 e do 2,1 SP1 do Microsoft Office 2013 incluem suporte à assinatura aprimorada do Outlook.</span><span class="sxs-lookup"><span data-stu-id="169b7-180">The UE-V 2.1 and 2.1 SP1 Microsoft Office 2013 settings location templates include improved Outlook signature support.</span></span> <span data-ttu-id="169b7-181">Adicionamos a sincronização das configurações de assinatura padrão para emails novos, de resposta e encaminhados.</span><span class="sxs-lookup"><span data-stu-id="169b7-181">We’ve added synchronization of default signature settings for new, reply, and forwarded emails.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="169b7-182">Observação</span><span class="sxs-lookup"><span data-stu-id="169b7-182">Note</span></span></strong><br/><p><span data-ttu-id="169b7-183">Um perfil do Outlook deve ser criado para qualquer dispositivo no qual o usuário deseja sincronizar a assinatura do Outlook.</span><span class="sxs-lookup"><span data-stu-id="169b7-183">An Outlook profile must be created for any device on which a user wants to sync their Outlook signature.</span></span> <span data-ttu-id="169b7-184">Se o perfil ainda não tiver sido criado, o usuário poderá criar um e, em seguida, reiniciar o Outlook nesse dispositivo para habilitar a sincronização de assinatura.</span><span class="sxs-lookup"><span data-stu-id="169b7-184">If the profile is not already created, the user can create one and then restart Outlook on that device to enable signature synchronization.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="169b7-185">Opções do navegador: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10 e Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="169b7-185">Browser options: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10, and Internet Explorer 11</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-186">Favoritos, página inicial, guias e barras de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="169b7-186">Favorites, home page, tabs, and toolbars.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="169b7-187">Observação</span><span class="sxs-lookup"><span data-stu-id="169b7-187">Note</span></span></strong><br/><p><span data-ttu-id="169b7-188">O UE-V não faz o roaming de configurações para cookies do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="169b7-188">UE-V does not roam settings for Internet Explorer cookies.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="169b7-189">Acessórios do Windows</span><span class="sxs-lookup"><span data-stu-id="169b7-189">Windows accessories</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-190">Calculadora da Microsoft, bloco de notas, WordPad.</span><span class="sxs-lookup"><span data-stu-id="169b7-190">Microsoft Calculator, Notepad, WordPad.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="169b7-191">Observação</span><span class="sxs-lookup"><span data-stu-id="169b7-191">Note</span></span>**  
<span data-ttu-id="169b7-192">O UE-V 2,1 SP1 não sincroniza as configurações entre a calculadora da Microsoft no Windows 10 e a calculadora da Microsoft em sistemas operacionais anteriores.</span><span class="sxs-lookup"><span data-stu-id="169b7-192">UE-V 2.1 SP1 does not synchronize settings between the Microsoft Calculator in Windows 10 and the Microsoft Calculator in previous operating systems.</span></span>



### <span data-ttu-id="169b7-193">Aplicativos da área de trabalho sincronizados por padrão no UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="169b7-193">Desktop applications synchronized by default in UE-V 2.0</span></span>

<span data-ttu-id="169b7-194">Quando você instala o agente do UE-V 2,0, ele registra um grupo padrão de modelos de local de configurações que capturam valores de configurações para esses aplicativos comuns da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="169b7-194">When you install the UE-V 2.0 Agent, it registers a default group of settings location templates that capture settings values for these common Microsoft applications.</span></span>

**<span data-ttu-id="169b7-195">Dica</span><span class="sxs-lookup"><span data-stu-id="169b7-195">Tip</span></span>**  
<span data-ttu-id="169b7-196">**Sincronização de configurações do Microsoft Office 2013** – em UE-V 2,0, um modelo de local de configurações não é incluído por padrão para aplicativos do Office 2013, mas está disponível para download na [Galeria de modelos do UE-V](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span><span class="sxs-lookup"><span data-stu-id="169b7-196">**Microsoft Office 2013 Settings Synchronization** – In UE-V 2.0, a settings location template is not included by default for Office 2013 applications, but is available for download from the [UE-V template gallery](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span> <span data-ttu-id="169b7-197">A [sincronização do Office 2013 com o UE-V 2,0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) fornece detalhes sobre os modelos com suporte que sincronizam as configurações do Office 2013.</span><span class="sxs-lookup"><span data-stu-id="169b7-197">[Synchronizing Office 2013 with UE-V 2.0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) provides details about the supported templates that synchronize Office 2013 settings.</span></span>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="169b7-198">Categoria do aplicativo</span><span class="sxs-lookup"><span data-stu-id="169b7-198">Application category</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="169b7-199">Descrição</span><span class="sxs-lookup"><span data-stu-id="169b7-199">Description</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="169b7-200">Aplicativos do Microsoft Office 2007</span><span class="sxs-lookup"><span data-stu-id="169b7-200">Microsoft Office 2007 applications</span></span></p>
<p><span data-ttu-id="169b7-201">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Baixar uma lista de todas as configurações sincronizadas </a> )</span><span class="sxs-lookup"><span data-stu-id="169b7-201">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-202">Microsoft Access 2007</span><span class="sxs-lookup"><span data-stu-id="169b7-202">Microsoft Access 2007</span></span></p>
<p><span data-ttu-id="169b7-203">Microsoft Communicator 2007</span><span class="sxs-lookup"><span data-stu-id="169b7-203">Microsoft Communicator 2007</span></span></p>
<p><span data-ttu-id="169b7-204">Microsoft Excel 2007</span><span class="sxs-lookup"><span data-stu-id="169b7-204">Microsoft Excel 2007</span></span></p>
<p><span data-ttu-id="169b7-205">Microsoft InfoPath 2007</span><span class="sxs-lookup"><span data-stu-id="169b7-205">Microsoft InfoPath 2007</span></span></p>
<p><span data-ttu-id="169b7-206">Microsoft OneNote 2007</span><span class="sxs-lookup"><span data-stu-id="169b7-206">Microsoft OneNote 2007</span></span></p>
<p><span data-ttu-id="169b7-207">Microsoft Outlook 2007</span><span class="sxs-lookup"><span data-stu-id="169b7-207">Microsoft Outlook 2007</span></span></p>
<p><span data-ttu-id="169b7-208">Microsoft PowerPoint 2007</span><span class="sxs-lookup"><span data-stu-id="169b7-208">Microsoft PowerPoint 2007</span></span></p>
<p><span data-ttu-id="169b7-209">Microsoft Project 2007</span><span class="sxs-lookup"><span data-stu-id="169b7-209">Microsoft Project 2007</span></span></p>
<p><span data-ttu-id="169b7-210">Microsoft Publisher 2007</span><span class="sxs-lookup"><span data-stu-id="169b7-210">Microsoft Publisher 2007</span></span></p>
<p><span data-ttu-id="169b7-211">Microsoft SharePoint Designer 2007</span><span class="sxs-lookup"><span data-stu-id="169b7-211">Microsoft SharePoint Designer 2007</span></span></p>
<p><span data-ttu-id="169b7-212">Microsoft Visio 2007</span><span class="sxs-lookup"><span data-stu-id="169b7-212">Microsoft Visio 2007</span></span></p>
<p><span data-ttu-id="169b7-213">Microsoft Word 2007</span><span class="sxs-lookup"><span data-stu-id="169b7-213">Microsoft Word 2007</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="169b7-214">Aplicativos do Microsoft Office 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-214">Microsoft Office 2010 applications</span></span></p>
<p><span data-ttu-id="169b7-215">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Baixar uma lista de todas as configurações sincronizadas </a> )</span><span class="sxs-lookup"><span data-stu-id="169b7-215">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-216">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-216">Microsoft Word 2010</span></span></p>
<p><span data-ttu-id="169b7-217">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-217">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="169b7-218">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-218">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="169b7-219">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-219">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="169b7-220">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-220">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="169b7-221">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-221">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="169b7-222">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-222">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="169b7-223">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-223">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="169b7-224">Microsoft SharePoint Workspace 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-224">Microsoft SharePoint Workspace 2010</span></span></p>
<p><span data-ttu-id="169b7-225">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-225">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="169b7-226">Microsoft Lync 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-226">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="169b7-227">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-227">Microsoft OneNote 2010</span></span></p>
<p><span data-ttu-id="169b7-228">Microsoft SharePoint Designer 2010</span><span class="sxs-lookup"><span data-stu-id="169b7-228">Microsoft SharePoint Designer 2010</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="169b7-229">Opções do navegador: Internet Explorer 8, Internet Explorer 9 e Internet Explorer 10</span><span class="sxs-lookup"><span data-stu-id="169b7-229">Browser options: Internet Explorer 8, Internet Explorer 9, and Internet Explorer 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-230">Favoritos, página inicial, guias e barras de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="169b7-230">Favorites, home page, tabs, and toolbars.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="169b7-231">Observação</span><span class="sxs-lookup"><span data-stu-id="169b7-231">Note</span></span></strong><br/><p><span data-ttu-id="169b7-232">O UE-V não faz o roaming de configurações para cookies do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="169b7-232">UE-V does not roam settings for Internet Explorer cookies.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="169b7-233">Acessórios do Windows</span><span class="sxs-lookup"><span data-stu-id="169b7-233">Windows accessories</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-234">Calculadora da Microsoft, bloco de notas, WordPad.</span><span class="sxs-lookup"><span data-stu-id="169b7-234">Microsoft Calculator, Notepad, WordPad.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="autosyncsettings2"></a><span data-ttu-id="169b7-235">Configurações do Windows sincronizadas por padrão</span><span class="sxs-lookup"><span data-stu-id="169b7-235">Windows settings synchronized by default</span></span>

<span data-ttu-id="169b7-236">O UE-V inclui modelos de local de configurações que capturam os valores das configurações do Windows.</span><span class="sxs-lookup"><span data-stu-id="169b7-236">UE-V includes settings location templates that capture settings values for these Windows settings.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="169b7-237">configurações do Windows</span><span class="sxs-lookup"><span data-stu-id="169b7-237">Windows settings</span></span></th>
<th align="left"><span data-ttu-id="169b7-238">Descrição</span><span class="sxs-lookup"><span data-stu-id="169b7-238">Description</span></span></th>
<th align="left"><span data-ttu-id="169b7-239">Aplicar em</span><span class="sxs-lookup"><span data-stu-id="169b7-239">Apply on</span></span></th>
<th align="left"><span data-ttu-id="169b7-240">Exportar em</span><span class="sxs-lookup"><span data-stu-id="169b7-240">Export on</span></span></th>
<th align="left"><span data-ttu-id="169b7-241">Estado padrão</span><span class="sxs-lookup"><span data-stu-id="169b7-241">Default state</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="169b7-242">Tela de fundo da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="169b7-242">Desktop background</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-243">Segundo plano ou papel de parede da área de trabalho ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="169b7-243">Currently active desktop background or wallpaper.</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-244">Logon, desbloqueio, conexão remota, eventos de tarefa agendada.</span><span class="sxs-lookup"><span data-stu-id="169b7-244">Logon, unlock, remote connect, Scheduled Task events.</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-245">Logoff, bloqueio, desconexão remota, usuário clicando em <strong> sincronizar agora </strong> no centro de configurações da empresa ou intervalo de tarefas agendadas</span><span class="sxs-lookup"><span data-stu-id="169b7-245">Logoff, lock, remote disconnect, user clicking <strong>Sync Now</strong> in Company Settings Center, or scheduled task interval</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-246">Habilitado</span><span class="sxs-lookup"><span data-stu-id="169b7-246">Enabled</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="169b7-247">Facilidade de Acesso</span><span class="sxs-lookup"><span data-stu-id="169b7-247">Ease of Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-248">Configurações de acessibilidade e de entrada, lente de opções da Microsoft, narrador e teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="169b7-248">Accessibility and input settings, Microsoft Magnifier, Narrator, and on-Screen Keyboard.</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-249">Somente logon.</span><span class="sxs-lookup"><span data-stu-id="169b7-249">Logon only.</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-250">Logoff, o usuário clica em <strong> sincronizar agora </strong> no centro de configurações da empresa ou no intervalo de tarefas agendadas</span><span class="sxs-lookup"><span data-stu-id="169b7-250">Logoff, user clicking <strong>Sync Now</strong> in Company Settings Center, or scheduled task interval</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-251">Habilitado</span><span class="sxs-lookup"><span data-stu-id="169b7-251">Enabled</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="169b7-252">Configurações da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="169b7-252">Desktop settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-253">Menu iniciar e configurações da barra de tarefas, opções de pasta, ícones da área de trabalho padrão, relógios adicionais e configurações de região e idioma.</span><span class="sxs-lookup"><span data-stu-id="169b7-253">Start menu and Taskbar settings, Folder options, Default desktop icons, Additional clocks, and Region and Language settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-254">Somente logon.</span><span class="sxs-lookup"><span data-stu-id="169b7-254">Logon only.</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-255">Logoff, o usuário clica em <strong> sincronizar agora </strong> no centro de configurações da empresa ou em tarefa agendada</span><span class="sxs-lookup"><span data-stu-id="169b7-255">Logoff, user clicking <strong>Sync Now</strong> in Company Settings Center, or scheduled task</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-256">Habilitado</span><span class="sxs-lookup"><span data-stu-id="169b7-256">Enabled</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="169b7-257">Observação</span><span class="sxs-lookup"><span data-stu-id="169b7-257">Note</span></span>**  
<span data-ttu-id="169b7-258">A partir do Windows 8, o UE-V não faz a roaming de configurações relacionadas à tela inicial, como itens e locais.</span><span class="sxs-lookup"><span data-stu-id="169b7-258">Starting in Windows 8, UE-V does not roam settings related to the Start screen, such as items and locations.</span></span> <span data-ttu-id="169b7-259">Além disso, o UE-V não dá suporte à sincronização de itens da barra de tarefas fixas ou atalhos de arquivos do Windows.</span><span class="sxs-lookup"><span data-stu-id="169b7-259">In addition, UE-V does not support synchronization of pinned taskbar items or Windows file shortcuts.</span></span>



**<span data-ttu-id="169b7-260">Importante</span><span class="sxs-lookup"><span data-stu-id="169b7-260">Important</span></span>**  
<span data-ttu-id="169b7-261">As configurações de barra de tarefas de roaming do UE-V 2,1 SP1 entre dispositivos Windows 10.</span><span class="sxs-lookup"><span data-stu-id="169b7-261">UE-V 2.1 SP1 roams taskbar settings between Windows 10 devices.</span></span> <span data-ttu-id="169b7-262">No entanto, o UE-V não sincroniza as configurações da barra de tarefas entre dispositivos Windows 10 e dispositivos que executam sistemas operacionais anteriores.</span><span class="sxs-lookup"><span data-stu-id="169b7-262">However, UE-V does not synchronize taskbar settings between Windows 10 devices and devices running previous operating systems.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="169b7-263">Grupo de configurações</span><span class="sxs-lookup"><span data-stu-id="169b7-263">Settings group</span></span></th>
<th align="left"><span data-ttu-id="169b7-264">Categoria</span><span class="sxs-lookup"><span data-stu-id="169b7-264">Category</span></span></th>
<th align="left"><span data-ttu-id="169b7-265">Chama</span><span class="sxs-lookup"><span data-stu-id="169b7-265">Capture</span></span></th>
<th align="left"><span data-ttu-id="169b7-266">Aplicar</span><span class="sxs-lookup"><span data-stu-id="169b7-266">Apply</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="169b7-267">Configurações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="169b7-267">Application Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="169b7-268">Aplicativos do Windows  </span><span class="sxs-lookup"><span data-stu-id="169b7-268">Windows apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-269">Fechar aplicativo</span><span class="sxs-lookup"><span data-stu-id="169b7-269">Close app</span></span></p>
<p><span data-ttu-id="169b7-270">Evento de alteração das configurações do aplicativo do Windows</span><span class="sxs-lookup"><span data-stu-id="169b7-270">Windows app settings change event</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-271">Iniciar o monitor do aplicativo UE-V na inicialização</span><span class="sxs-lookup"><span data-stu-id="169b7-271">Start the UE-V App Monitor at startup</span></span></p>
<p><span data-ttu-id="169b7-272">Abrir o aplicativo</span><span class="sxs-lookup"><span data-stu-id="169b7-272">Open app</span></span></p>
<p><span data-ttu-id="169b7-273">Evento de alteração das configurações do aplicativo do Windows</span><span class="sxs-lookup"><span data-stu-id="169b7-273">Windows App Settings change event</span></span></p>
<p><span data-ttu-id="169b7-274">Chegada de um pacote de configurações</span><span class="sxs-lookup"><span data-stu-id="169b7-274">Arrival of a settings package</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="169b7-275">Aplicativos da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="169b7-275">Desktop applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-276">Aplicativo é fechado</span><span class="sxs-lookup"><span data-stu-id="169b7-276">Application closes</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-277">O aplicativo abre e fecha</span><span class="sxs-lookup"><span data-stu-id="169b7-277">Application opens and closes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="169b7-278">Configurações da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="169b7-278">Desktop settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="169b7-279">Tela de fundo da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="169b7-279">Desktop background</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-280">Bloquear ou fazer logoff</span><span class="sxs-lookup"><span data-stu-id="169b7-280">Lock or logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-281">Logon, desbloqueio, conexão remota, notificação de Nova chegada de pacote, o usuário clica <strong> em sincronizar agora </strong> no centro de configurações da empresa ou quando a tarefa agendada é executada.</span><span class="sxs-lookup"><span data-stu-id="169b7-281">Logon, unlock, remote connect, notification of new package arrival, user clicks <strong>Sync Now</strong> in Company Settings Center, or scheduled task runs.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="169b7-282">Facilidade de acesso (comum – acessibilidade, narrador, lupa, na tela-teclado)</span><span class="sxs-lookup"><span data-stu-id="169b7-282">Ease of Access (Common – Accessibility, Narrator, Magnifier, On-Screen-Keyboard)</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-283">Bloquear ou fazer logoff</span><span class="sxs-lookup"><span data-stu-id="169b7-283">Lock or Logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-284">Sessão</span><span class="sxs-lookup"><span data-stu-id="169b7-284">Logon</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="169b7-285">Facilidade de acesso (shell-áudio, acessibilidade, teclado, mouse)</span><span class="sxs-lookup"><span data-stu-id="169b7-285">Ease of Access (Shell - Audio, Accessibility, Keyboard, Mouse)</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-286">Bloquear ou fazer logoff</span><span class="sxs-lookup"><span data-stu-id="169b7-286">Lock or logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-287">Logon, desbloqueio, conexão remota, notificação de Nova chegada de pacote, clicar em <strong> sincronizar agora </strong> no centro de configurações da empresa ou executar tarefas agendadas</span><span class="sxs-lookup"><span data-stu-id="169b7-287">Logon, unlock, remote connect, notification of new package arrival, user clicks <strong>Sync Now</strong> in Company Settings Center, or scheduled task runs</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="169b7-288">Configurações da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="169b7-288">Desktop settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-289">Bloquear ou fazer logoff</span><span class="sxs-lookup"><span data-stu-id="169b7-289">Lock or logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-290">Sessão</span><span class="sxs-lookup"><span data-stu-id="169b7-290">Logon</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="169b7-291">UE-V-suporte para aplicativos do Windows</span><span class="sxs-lookup"><span data-stu-id="169b7-291">UE-V-support for Windows Apps</span></span>

<span data-ttu-id="169b7-292">Para aplicativos do Windows, o desenvolvedor do aplicativo especifica as configurações que são sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="169b7-292">For Windows apps, the app developer specifies the settings that are synchronized.</span></span> <span data-ttu-id="169b7-293">Você pode especificar quais aplicativos do Windows estão habilitados para a sincronização de configurações.</span><span class="sxs-lookup"><span data-stu-id="169b7-293">You can specify which Windows apps are enabled for settings synchronization.</span></span>

<span data-ttu-id="169b7-294">Para exibir uma lista de aplicativos do Windows que podem sincronizar as configurações em um computador com o nome da família de pacotes, status habilitado e fonte habilitada, em um prompt de comando do Windows PowerShell, digite:</span><span class="sxs-lookup"><span data-stu-id="169b7-294">To display a list of Windows apps that can synchronize settings on a computer with their package family name, enabled status, and enabled source, at a Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage`

**<span data-ttu-id="169b7-295">Observação</span><span class="sxs-lookup"><span data-stu-id="169b7-295">Note</span></span>**  
<span data-ttu-id="169b7-296">A partir do Windows 8, o UE-V não sincroniza as configurações do aplicativo do Windows se o usuário do domínio vincular suas credenciais de entrada à conta da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="169b7-296">As of Windows 8, UE-V does not synchronize Windows app settings if the domain user links their sign-in credentials to their Microsoft Account.</span></span> <span data-ttu-id="169b7-297">Essa vinculação sincroniza as configurações do Microsoft OneDrive para UE-V, que desabilita a sincronização das configurações de aplicativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="169b7-297">This linking synchronizes settings to Microsoft OneDrive so UE-V, which disables synchronization of Windows app settings.</span></span>



### <span data-ttu-id="169b7-298">UE-V-suporte para impressoras móveis</span><span class="sxs-lookup"><span data-stu-id="169b7-298">UE-V-support for Roaming Printers</span></span>

<span data-ttu-id="169b7-299">O UE-V 2,1 SP1 permite que impressoras de rede sejam movidas entre dispositivos para que um usuário tenha acesso às suas impressoras de rede quando estiver conectado a qualquer dispositivo na rede.</span><span class="sxs-lookup"><span data-stu-id="169b7-299">UE-V 2.1 SP1 lets network printers roam between devices so that a user has access to their network printers when logged on to any device on the network.</span></span> <span data-ttu-id="169b7-300">Isso inclui o roaming da impressora definida como padrão.</span><span class="sxs-lookup"><span data-stu-id="169b7-300">This includes roaming the printer that they set as the default.</span></span>

<span data-ttu-id="169b7-301">O roaming da impressora no UE-V exige um dos seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="169b7-301">Printer roaming in UE-V requires one of these scenarios:</span></span>

-   <span data-ttu-id="169b7-302">O servidor de impressão pode baixar o driver necessário quando ele está em roaming para um novo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="169b7-302">The print server can download the required driver when it roams to a new device.</span></span>

-   <span data-ttu-id="169b7-303">O driver para a impressora de rede de roaming está pré-instalado em qualquer dispositivo que precise acessar a impressora de rede.</span><span class="sxs-lookup"><span data-stu-id="169b7-303">The driver for the roaming network printer is pre-installed on any device that needs to access that network printer.</span></span>

-   <span data-ttu-id="169b7-304">O driver da impressora pode ser obtido no Windows Update.</span><span class="sxs-lookup"><span data-stu-id="169b7-304">The printer driver can be obtained from Windows Update.</span></span>

**<span data-ttu-id="169b7-305">Observação</span><span class="sxs-lookup"><span data-stu-id="169b7-305">Note</span></span>**  
<span data-ttu-id="169b7-306">O recurso de roaming da impressora UE-V **não transfere** preferências ou configurações de impressora, como impressão em frente e verso.</span><span class="sxs-lookup"><span data-stu-id="169b7-306">The UE-V printer roaming feature does **not** roam printer settings or preferences, such as printing double-sided.</span></span>



### <a href="" id="determinesettingssync"></a><span data-ttu-id="169b7-307">Determinar se você precisa de configurações sincronizadas para outros aplicativos</span><span class="sxs-lookup"><span data-stu-id="169b7-307">Determine whether you need settings synchronized for other applications</span></span>

<span data-ttu-id="169b7-308">Depois de revisar as configurações que são sincronizadas automaticamente em uma implantação do UE-V, você deseja decidir se sincronizará as configurações de outros aplicativos, pois determina como implantar o UE-V em toda a empresa.</span><span class="sxs-lookup"><span data-stu-id="169b7-308">After you have reviewed the settings that are synchronized automatically in a UE-V deployment, you want to decide whether you will synchronize settings for other applications since this determines how you deploy UE-V throughout your enterprise.</span></span>

<span data-ttu-id="169b7-309">Como administrador, quando você considera quais aplicativos da área de trabalho serão incluídos na sua solução UE-V, considere quais configurações podem ser personalizadas pelos usuários e como e onde o aplicativo armazena suas configurações.</span><span class="sxs-lookup"><span data-stu-id="169b7-309">As an administrator, when you consider which desktop applications to include in your UE-V solution, consider which settings can be customized by users, and how and where the application stores its settings.</span></span> <span data-ttu-id="169b7-310">Nem todos os aplicativos da área de trabalho têm configurações que podem ser personalizadas ou que são rotineiramente personalizadas pelos usuários.</span><span class="sxs-lookup"><span data-stu-id="169b7-310">Not all desktop applications have settings that can be customized or that are routinely customized by users.</span></span> <span data-ttu-id="169b7-311">Além disso, nem todas as configurações de aplicativos da área de trabalho podem ser sincronizadas com segurança em vários computadores ou ambientes.</span><span class="sxs-lookup"><span data-stu-id="169b7-311">In addition, not all desktop applications settings can safely be synchronized across multiple computers or environments.</span></span>

<span data-ttu-id="169b7-312">Em geral, você pode sincronizar as configurações que atendem aos seguintes critérios:</span><span class="sxs-lookup"><span data-stu-id="169b7-312">In general, you can synchronize settings that meet the following criteria:</span></span>

-   <span data-ttu-id="169b7-313">Configurações armazenadas em locais acessíveis pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="169b7-313">Settings that are stored in user-accessible locations.</span></span> <span data-ttu-id="169b7-314">Por exemplo, não sincronize as configurações armazenadas em system32 ou fora da seção HKEY \ _CURRENT \ _USER (HKCU) do registro.</span><span class="sxs-lookup"><span data-stu-id="169b7-314">For example, do not synchronize settings that are stored in System32 or outside the HKEY\_CURRENT\_USER (HKCU) section of the registry.</span></span>

-   <span data-ttu-id="169b7-315">Configurações que não são específicas do computador específico.</span><span class="sxs-lookup"><span data-stu-id="169b7-315">Settings that are not specific to the particular computer.</span></span> <span data-ttu-id="169b7-316">Por exemplo, exclua configurações de rede ou de hardware.</span><span class="sxs-lookup"><span data-stu-id="169b7-316">For example, exclude network or hardware configurations.</span></span>

-   <span data-ttu-id="169b7-317">Configurações que podem ser sincronizadas entre computadores sem risco de dados corrompidos.</span><span class="sxs-lookup"><span data-stu-id="169b7-317">Settings that can be synchronized between computers without risk of corrupted data.</span></span> <span data-ttu-id="169b7-318">Por exemplo, não use configurações armazenadas em um arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="169b7-318">For example, do not use settings that are stored in a database file.</span></span>

### <a href="" id="checklistsettingssync"></a><span data-ttu-id="169b7-319">Lista de verificação para avaliação de aplicativos personalizados</span><span class="sxs-lookup"><span data-stu-id="169b7-319">Checklist for evaluating custom applications</span></span>

<span data-ttu-id="169b7-320">Se você tiver decidido que precisa de configurações sincronizadas para outros aplicativos, poderá usar esta lista de verificação para ajudar a descobrir quais aplicativos serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="169b7-320">If you’ve decided that you need settings synchronized for other applications, you can use this checklist to help figure out which applications you’ll include.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="169b7-321">Descrição</span><span class="sxs-lookup"><span data-stu-id="169b7-321">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="169b7-322">Este aplicativo contém configurações que o usuário pode personalizar?</span><span class="sxs-lookup"><span data-stu-id="169b7-322">Does this application contain settings that the user can customize?</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="169b7-323">É importante para o usuário que essas configurações são sincronizadas?</span><span class="sxs-lookup"><span data-stu-id="169b7-323">Is it important for the user that these settings are synchronized?</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="169b7-324">Essas configurações de usuário já são gerenciadas por uma solução de política de gerenciamento ou configurações de aplicativo?</span><span class="sxs-lookup"><span data-stu-id="169b7-324">Are these user settings already managed by an application management or settings policy solution?</span></span> <span data-ttu-id="169b7-325">O UE-V aplica as configurações do aplicativo nas configurações de inicialização do aplicativo e do Windows durante eventos de logon, desbloqueio ou conexão remota.</span><span class="sxs-lookup"><span data-stu-id="169b7-325">UE-V applies application settings at application startup and Windows settings at logon, unlock, or remote connect events.</span></span> <span data-ttu-id="169b7-326">Se você usa o UE-V com outras soluções de compartilhamento de configurações, os usuários podem ter inconsistência nas configurações sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="169b7-326">If you use UE-V with other settings sharing solutions, users might experience inconsistency across synchronized settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="169b7-327">As configurações do aplicativo são específicas do computador?</span><span class="sxs-lookup"><span data-stu-id="169b7-327">Are the application settings specific to the computer?</span></span> <span data-ttu-id="169b7-328">Preferências de aplicativo e personalizações associadas a hardware ou configurações de computador específicas não sincronizam consistentemente entre as sessões e podem causar uma experiência de aplicativo ruim.</span><span class="sxs-lookup"><span data-stu-id="169b7-328">Application preferences and customizations that are associated with hardware or specific computer configurations do not consistently synchronize across sessions and can cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="169b7-329">As configurações da loja de aplicativos são encontradas no diretório arquivos de programas ou no diretório de arquivos localizado no diretório <strong> usuários </strong> [nome de usuário] &lt; Strong &gt; AppData </strong> &lt; Strong &gt; LocalLow </strong> ?</span><span class="sxs-lookup"><span data-stu-id="169b7-329">Does the application store settings in the Program Files directory or in the file directory that is located in the <strong>Users</strong>[User name]&lt;strong&gt;AppData</strong>&lt;strong&gt;LocalLow</strong> directory?</span></span> <span data-ttu-id="169b7-330">Os dados de aplicativo armazenados em qualquer um desses locais normalmente não devem ser sincronizados com o usuário, pois esses dados são específicos do computador ou porque os dados são muito grandes para serem sincronizados.</span><span class="sxs-lookup"><span data-stu-id="169b7-330">Application data that is stored in either of these locations usually should not synchronize with the user, because this data is specific to the computer or because the data is too large to synchronize.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="169b7-331">O aplicativo armazena todas as configurações em um arquivo que contém outros dados de aplicativo que não devem ser sincronizados?</span><span class="sxs-lookup"><span data-stu-id="169b7-331">Does the application store any settings in a file that contains other application data that should not synchronize?</span></span> <span data-ttu-id="169b7-332">O UE-V sincroniza arquivos como uma unidade única.</span><span class="sxs-lookup"><span data-stu-id="169b7-332">UE-V synchronizes files as a single unit.</span></span> <span data-ttu-id="169b7-333">Se as configurações forem armazenadas em arquivos que incluam dados do aplicativo além das configurações, a sincronização desses dados adicionais poderá causar uma experiência de aplicativo deficiente.</span><span class="sxs-lookup"><span data-stu-id="169b7-333">If settings are stored in files that include application data other than settings, then synchronizing this additional data can cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="169b7-334">Qual é o tamanho dos arquivos que contêm as configurações?</span><span class="sxs-lookup"><span data-stu-id="169b7-334">How large are the files that contain the settings?</span></span> <span data-ttu-id="169b7-335">O desempenho da sincronização de configurações pode ser afetado por arquivos grandes.</span><span class="sxs-lookup"><span data-stu-id="169b7-335">The performance of the settings synchronization can be affected by large files.</span></span> <span data-ttu-id="169b7-336">Incluir arquivos grandes pode afetar o desempenho da sincronização das configurações.</span><span class="sxs-lookup"><span data-stu-id="169b7-336">Including large files can affect the performance of settings synchronization.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="considerations"></a><span data-ttu-id="169b7-337">Outras considerações ao preparar uma implantação de UE-V</span><span class="sxs-lookup"><span data-stu-id="169b7-337">Other Considerations when Preparing a UE-V Deployment</span></span>


<span data-ttu-id="169b7-338">Você também deve considerar essas coisas quando estiver se preparando para implantar o UE-V:</span><span class="sxs-lookup"><span data-stu-id="169b7-338">You should also consider these things when you are preparing to deploy UE-V:</span></span>

-   [<span data-ttu-id="169b7-339">Gerenciando a sincronização de credenciais</span><span class="sxs-lookup"><span data-stu-id="169b7-339">Managing credentials synchronization</span></span>](#creds)

-   [<span data-ttu-id="169b7-340">Sincronização de configurações do aplicativo do Windows</span><span class="sxs-lookup"><span data-stu-id="169b7-340">Windows app settings synchronization</span></span>](#appxsettings)

-   [<span data-ttu-id="169b7-341">Modelos de localização de configurações personalizadas de UE-V</span><span class="sxs-lookup"><span data-stu-id="169b7-341">Custom UE-V settings location templates</span></span>](#custom)

-   [<span data-ttu-id="169b7-342">Configurações de configurações do usuário não intencional</span><span class="sxs-lookup"><span data-stu-id="169b7-342">Unintentional user settings configurations</span></span>](#prevent)

-   [<span data-ttu-id="169b7-343">Desempenho e capacidade</span><span class="sxs-lookup"><span data-stu-id="169b7-343">Performance and capacity</span></span>](#capacity)

-   [<span data-ttu-id="169b7-344">Alta disponibilidade</span><span class="sxs-lookup"><span data-stu-id="169b7-344">High availability</span></span>](#high)

-   [<span data-ttu-id="169b7-345">Sincronização do relógio do computador</span><span class="sxs-lookup"><span data-stu-id="169b7-345">Computer clock synchronization</span></span>](#clocksync)

### <a href="" id="creds"></a><span data-ttu-id="169b7-346">Gerenciando a sincronização de credenciais no UE-V 2,1 e no UE-V 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="169b7-346">Managing credentials synchronization in UE-V 2.1 and UE-V 2.1 SP1</span></span>

<span data-ttu-id="169b7-347">Muitos aplicativos corporativos, incluindo o Microsoft Outlook e o Lync, solicitam aos usuários suas credenciais de domínio ao fazer logon.</span><span class="sxs-lookup"><span data-stu-id="169b7-347">Many enterprise applications, including Microsoft Outlook and Lync, prompt users for their domain credentials at login.</span></span> <span data-ttu-id="169b7-348">Os usuários têm a opção de salvar as credenciais em disco para evitar que você precise digitá-las toda vez que abrirem esses aplicativos.</span><span class="sxs-lookup"><span data-stu-id="169b7-348">Users have the option of saving their credentials to disk to prevent having to enter them every time they open these applications.</span></span> <span data-ttu-id="169b7-349">Habilitar a sincronização de credenciais de roaming permite que os usuários salvem suas credenciais em um computador e evite digitá-las novamente em cada computador usado em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="169b7-349">Enabling roaming credentials synchronization lets users save their credentials on one computer and avoid re-entering them on every computer they use in their environment.</span></span> <span data-ttu-id="169b7-350">Os usuários podem sincronizar algumas credenciais de domínio com o UE-V 2,1 e o 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="169b7-350">Users can synchronize some domain credentials with UE-V 2.1 and 2.1 SP1.</span></span>

**<span data-ttu-id="169b7-351">Importante</span><span class="sxs-lookup"><span data-stu-id="169b7-351">Important</span></span>**  
<span data-ttu-id="169b7-352">A sincronização de credenciais é desativada por padrão.</span><span class="sxs-lookup"><span data-stu-id="169b7-352">Credentials synchronization is disabled by default.</span></span> <span data-ttu-id="169b7-353">Você deve habilitar explicitamente a sincronização de credenciais durante a implantação para implementar esse recurso.</span><span class="sxs-lookup"><span data-stu-id="169b7-353">You must explicitly enable credentials synchronization during deployment to implement this feature.</span></span>



<span data-ttu-id="169b7-354">O UE-V 2,1 e o 2,1 SP1 podem sincronizar as credenciais da empresa, mas não use o roaming de credenciais somente para uso no computador local.</span><span class="sxs-lookup"><span data-stu-id="169b7-354">UE-V 2.1 and 2.1 SP1 can synchronize enterprise credentials, but do not roam credentials intended only for use on the local computer.</span></span>

<span data-ttu-id="169b7-355">As credenciais são configurações síncronas, o que significa que elas são aplicadas ao seu perfil na primeira vez que você se conecta ao computador após a sincronização do UE-V.</span><span class="sxs-lookup"><span data-stu-id="169b7-355">Credentials are synchronous settings, meaning they are applied to your profile the first time you log in to your computer after UE-V synchronizes.</span></span>

<span data-ttu-id="169b7-356">A sincronização de credenciais é gerenciada por seu próprio modelo de local de configurações, que é desabilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="169b7-356">Credentials synchronization is managed by its own settings location template, which is disabled by default.</span></span> <span data-ttu-id="169b7-357">Você pode habilitar ou desabilitar esse modelo por meio dos mesmos métodos usados para outros modelos.</span><span class="sxs-lookup"><span data-stu-id="169b7-357">You can enable or disable this template through the same methods used for other templates.</span></span> <span data-ttu-id="169b7-358">O identificador de modelo para esse recurso é RoamingCredentialSettings.</span><span class="sxs-lookup"><span data-stu-id="169b7-358">The template identifier for this feature is RoamingCredentialSettings.</span></span>

**<span data-ttu-id="169b7-359">Importante</span><span class="sxs-lookup"><span data-stu-id="169b7-359">Important</span></span>**  
<span data-ttu-id="169b7-360">Se você estiver usando o roaming de credenciais do Active Directory em seu ambiente, recomendamos que você não habilite o modelo de roaming de credenciais do UE-V.</span><span class="sxs-lookup"><span data-stu-id="169b7-360">If you are using Active Directory Credential Roaming in your environment, we recommend that you don’t enable the UE-V credential roaming template.</span></span>



<span data-ttu-id="169b7-361">Use um destes métodos para habilitar a sincronização de credenciais:</span><span class="sxs-lookup"><span data-stu-id="169b7-361">Use one of these methods to enable credentials synchronization:</span></span>

-   <span data-ttu-id="169b7-362">Centro de configurações da empresa</span><span class="sxs-lookup"><span data-stu-id="169b7-362">Company Settings Center</span></span>

-   <span data-ttu-id="169b7-363">PowerShell</span><span class="sxs-lookup"><span data-stu-id="169b7-363">PowerShell</span></span>

-   <span data-ttu-id="169b7-364">Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="169b7-364">Group Policy</span></span>

**<span data-ttu-id="169b7-365">Observação</span><span class="sxs-lookup"><span data-stu-id="169b7-365">Note</span></span>**  
<span data-ttu-id="169b7-366">As credenciais são criptografadas durante a sincronização.</span><span class="sxs-lookup"><span data-stu-id="169b7-366">Credentials are encrypted during synchronization.</span></span>



<span data-ttu-id="169b7-367">[Centro de configurações da empresa](https://technet.microsoft.com/library/dn458903.aspx)**:** marque a caixa de seleção configurações de credenciais de roaming em configurações do Windows para habilitar a sincronização de credenciais.</span><span class="sxs-lookup"><span data-stu-id="169b7-367">[Company Settings Center](https://technet.microsoft.com/library/dn458903.aspx)**:** Check the Roaming Credential Settings check box under Windows Settings to enable credential synchronization.</span></span> <span data-ttu-id="169b7-368">Desmarque a caixa para desabilitá-la.</span><span class="sxs-lookup"><span data-stu-id="169b7-368">Uncheck the box to disable it.</span></span> <span data-ttu-id="169b7-369">Essa caixa de seleção aparecerá apenas na central de configurações da empresa se a sua conta não estiver configurada para sincronizar as configurações usando uma conta da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="169b7-369">This check box only appears in Company Settings Center if your account is not configured to synchronize settings using a Microsoft Account.</span></span>

<span data-ttu-id="169b7-370">[PowerShell](https://technet.microsoft.com/library/dn458937.aspx)**:** este cmdlet do PowerShell permite a sincronização de credenciais:</span><span class="sxs-lookup"><span data-stu-id="169b7-370">[PowerShell](https://technet.microsoft.com/library/dn458937.aspx)**:** This PowerShell cmdlet enables credential synchronization:</span></span>

``` syntax
Enable-UevTemplate RoamingCredentialSettings
```

<span data-ttu-id="169b7-371">Este cmdlet do PowerShell desabilita a sincronização de credenciais:</span><span class="sxs-lookup"><span data-stu-id="169b7-371">This PowerShell cmdlet disables credential synchronization:</span></span>

``` syntax
Disable-UevTemplate RoamingCredentialSettings
```

<span data-ttu-id="169b7-372">[Política de grupo](https://technet.microsoft.com/library/dn458893.aspx)**:** você deve [implantar o modelo ADMX mais recente do MDOP](https://go.microsoft.com/fwlink/p/?LinkId=393944) para habilitar a sincronização de credenciais por meio da política de grupo.</span><span class="sxs-lookup"><span data-stu-id="169b7-372">[Group Policy](https://technet.microsoft.com/library/dn458893.aspx)**:** You must [deploy the latest MDOP ADMX template](https://go.microsoft.com/fwlink/p/?LinkId=393944) to enable credential synchronization through group policy.</span></span> <span data-ttu-id="169b7-373">A sincronização de credenciais é gerenciada com as configurações do Windows.</span><span class="sxs-lookup"><span data-stu-id="169b7-373">Credentials synchronization is managed with the Windows settings.</span></span> <span data-ttu-id="169b7-374">Para gerenciar esse recurso com a política de grupo, habilite a política sincronizar configurações do Windows.</span><span class="sxs-lookup"><span data-stu-id="169b7-374">To manage this feature with Group Policy, enable the Synchronize Windows settings policy.</span></span>

1.  <span data-ttu-id="169b7-375">Abra o editor de política de grupo e navegue até **configuração do usuário – modelos administrativos – componentes do Windows – virtualização da experiência do usuário da Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="169b7-375">Open Group Policy Editor and navigate to **User Configuration – Administrative Templates – Windows Components – Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="169b7-376">Clique duas vezes em **sincronizar configurações do Windows**.</span><span class="sxs-lookup"><span data-stu-id="169b7-376">Double-click on **Synchronize Windows settings**.</span></span>

3.  <span data-ttu-id="169b7-377">Se essa política estiver habilitada, você poderá habilitar a sincronização de credenciais marcando a caixa de seleção **credenciais de roaming** ou desabilitar a sincronização de credenciais desmarcando-a.</span><span class="sxs-lookup"><span data-stu-id="169b7-377">If this policy is enabled, you can enable credentials synchronization by checking the **Roaming Credentials** check box, or disable credentials synchronization by unchecking it.</span></span>

4.  <span data-ttu-id="169b7-378">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="169b7-378">Click **OK**.</span></span>

### <span data-ttu-id="169b7-379">Locais de credenciais sincronizados pela UE-V</span><span class="sxs-lookup"><span data-stu-id="169b7-379">Credential locations synchronized by UE-V</span></span>

<span data-ttu-id="169b7-380">Os arquivos de credenciais salvos por aplicativos nos seguintes locais são sincronizados:</span><span class="sxs-lookup"><span data-stu-id="169b7-380">Credential files saved by applications into the following locations are synchronized:</span></span>

-   <span data-ttu-id="169b7-381">%UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials</span><span class="sxs-lookup"><span data-stu-id="169b7-381">%UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials</span></span>\\

-   <span data-ttu-id="169b7-382">%UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto</span><span class="sxs-lookup"><span data-stu-id="169b7-382">%UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto</span></span>\\

-   <span data-ttu-id="169b7-383">%UserProfile%\\AppData\\Roaming\\Microsoft\\Protect</span><span class="sxs-lookup"><span data-stu-id="169b7-383">%UserProfile%\\AppData\\Roaming\\Microsoft\\Protect</span></span>\\

-   <span data-ttu-id="169b7-384">%UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates</span><span class="sxs-lookup"><span data-stu-id="169b7-384">%UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates</span></span>\\

<span data-ttu-id="169b7-385">As credenciais salvas em outros locais não são sincronizadas pela UE-V.</span><span class="sxs-lookup"><span data-stu-id="169b7-385">Credentials saved to other locations are not synchronized by UE-V.</span></span>

### <a href="" id="appxsettings"></a><span data-ttu-id="169b7-386">Sincronização de configurações do aplicativo do Windows</span><span class="sxs-lookup"><span data-stu-id="169b7-386">Windows app settings synchronization</span></span>

<span data-ttu-id="169b7-387">O UE-V gerencia a sincronização das configurações do aplicativo Windows de três maneiras:</span><span class="sxs-lookup"><span data-stu-id="169b7-387">UE-V manages Windows app settings synchronization in three ways:</span></span>

-   <span data-ttu-id="169b7-388">**Sincronizar aplicativos do Windows:** Permitir ou negar a sincronização de qualquer aplicativo do Windows</span><span class="sxs-lookup"><span data-stu-id="169b7-388">**Sync Windows Apps:** Allow or deny any Windows app synchronization</span></span>

-   <span data-ttu-id="169b7-389">**Lista de aplicativos do Windows:** Sincronizar uma lista de aplicativos do Windows</span><span class="sxs-lookup"><span data-stu-id="169b7-389">**Windows App List:** Synchronize a list of Windows apps</span></span>

-   <span data-ttu-id="169b7-390">**Comportamento de sincronização padrão não listado:** Determine o comportamento de sincronização dos aplicativos do Windows que não estão na lista de aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="169b7-390">**Unlisted Default Sync Behavior:** Determine the synchronization behavior of Windows apps that are not in the Windows app list.</span></span>

<span data-ttu-id="169b7-391">Para obter mais informações, consulte a [lista de aplicativos do Windows](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span><span class="sxs-lookup"><span data-stu-id="169b7-391">For more information, see the [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span></span>

### <a href="" id="custom"></a><span data-ttu-id="169b7-392">Modelos de localização de configurações personalizadas de UE-V</span><span class="sxs-lookup"><span data-stu-id="169b7-392">Custom UE-V settings location templates</span></span>

<span data-ttu-id="169b7-393">Se você estiver implantando o UE-V para sincronizar as configurações de aplicativos personalizados, usará o UE-V Generator para criar modelos de localização de configurações personalizadas para esses aplicativos da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="169b7-393">If you are deploying UE-V to synchronize settings for custom applications, you will use the UE-V Generator to create custom settings location templates for those desktop applications.</span></span> <span data-ttu-id="169b7-394">Depois de criar e testar um modelo de local de configurações personalizado em um ambiente de teste, você pode implantar os modelos de local de configurações em computadores na empresa.</span><span class="sxs-lookup"><span data-stu-id="169b7-394">After you create and test a custom settings location template in a test environment, you can deploy the settings location templates to computers in the enterprise.</span></span>

<span data-ttu-id="169b7-395">Modelos de localização de configurações personalizadas devem ser implantados com uma infraestrutura de implantação existente, como um método ESD (Enterprise Software Distribution), como o System Center Configuration Manager, com preferências ou configurando um catálogo de modelos de configurações do UE-V.</span><span class="sxs-lookup"><span data-stu-id="169b7-395">Custom settings location templates must be deployed with an existing deployment infrastructure, like an enterprise software distribution (ESD) method such as System Center Configuration Manager, with preferences, or by configuring an UE-V settings template catalog.</span></span> <span data-ttu-id="169b7-396">Os modelos implantados com o Configuration Manager ou a política de grupo devem ser registrados usando o UE-V WMI ou o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="169b7-396">Templates that are deployed with Configuration Manager or Group Policy must be registered by using UE-V WMI or Windows PowerShell.</span></span>

<span data-ttu-id="169b7-397">Para obter mais informações sobre modelos de localização de configurações personalizadas, consulte [implantar o UE-V 2. x para aplicativos personalizados](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="169b7-397">For more information about custom settings location templates, see [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span></span> <span data-ttu-id="169b7-398">Para obter mais informações sobre como usar o UE-V com o Configuration Manager, consulte [Configurando o UE-v 2. x com o System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="169b7-398">For more information about using UE-V with Configuration Manager, see [Configuring UE-V 2.x with System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span></span>

### <a href="" id="prevent"></a><span data-ttu-id="169b7-399">Impedir a configuração de configurações do usuário não intencional</span><span class="sxs-lookup"><span data-stu-id="169b7-399">Prevent unintentional user settings configuration</span></span>

<span data-ttu-id="169b7-400">O UE-V baixa as informações de novas configurações de usuário de um local de armazenamento de configurações e aplica as configurações ao computador local nestes casos:</span><span class="sxs-lookup"><span data-stu-id="169b7-400">UE-V downloads new user settings information from a settings storage location and applies the settings to the local computer in these instances:</span></span>

-   <span data-ttu-id="169b7-401">Toda vez que um aplicativo é iniciado com um modelo UE-V registrado.</span><span class="sxs-lookup"><span data-stu-id="169b7-401">Every time an application is started that has a registered UE-V template.</span></span>

-   <span data-ttu-id="169b7-402">Quando um usuário faz logon em um computador.</span><span class="sxs-lookup"><span data-stu-id="169b7-402">When a user logs on to a computer.</span></span>

-   <span data-ttu-id="169b7-403">Quando um usuário desbloqueia um computador.</span><span class="sxs-lookup"><span data-stu-id="169b7-403">When a user unlocks a computer.</span></span>

-   <span data-ttu-id="169b7-404">Quando é feita uma conexão com um computador de área de trabalho remota com UE-V instalado.</span><span class="sxs-lookup"><span data-stu-id="169b7-404">When a connection is made to a remote desktop computer that has UE-V installed.</span></span>

-   <span data-ttu-id="169b7-405">Quando a tarefa agendada do aplicativo de controlador de sincronização estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="169b7-405">When the Sync Controller Application scheduled task is run.</span></span>

<span data-ttu-id="169b7-406">Se o UE-V estiver instalado no computador A e no computador B e as configurações desejadas para o aplicativo estiverem no computador A, o computador A deve abrir e fechar o aplicativo primeiro.</span><span class="sxs-lookup"><span data-stu-id="169b7-406">If UE-V is installed on computer A and computer B, and the settings that you want for the application are on computer A, then computer A should open and close the application first.</span></span> <span data-ttu-id="169b7-407">Se o aplicativo for aberto e fechado no computador B primeiro, as configurações do aplicativo no computador A serão configuradas para as configurações do aplicativo no computador B. as configurações são sincronizadas entre computadores em cada aplicativo.</span><span class="sxs-lookup"><span data-stu-id="169b7-407">If the application is opened and closed on computer B first, then the application settings on computer A are configured to the application settings on computer B. Settings are synchronized between computers on per-application basis.</span></span> <span data-ttu-id="169b7-408">Com o passar do tempo, as configurações ficam consistentes entre computadores à medida que eles são abertos e fechados com configurações preferenciais.</span><span class="sxs-lookup"><span data-stu-id="169b7-408">Over time, settings become consistent between computers as they are opened and closed with preferred settings.</span></span>

<span data-ttu-id="169b7-409">Esse cenário também se aplica às configurações do Windows.</span><span class="sxs-lookup"><span data-stu-id="169b7-409">This scenario also applies to Windows settings.</span></span> <span data-ttu-id="169b7-410">Se as configurações do Windows no computador B devem ser iguais às do Windows no computador A, o usuário deve fazer logon e fazer logoff do computador A primeiro.</span><span class="sxs-lookup"><span data-stu-id="169b7-410">If the Windows settings on computer B should be the same as the Windows settings on computer A, then the user should log on and log off computer A first.</span></span>

<span data-ttu-id="169b7-411">Se as configurações do usuário que o usuário quer forem aplicadas na ordem errada, elas poderão ser recuperadas ao executar uma operação de restauração para o aplicativo específico ou a configuração do Windows no computador em que as configurações foram sobrescritas.</span><span class="sxs-lookup"><span data-stu-id="169b7-411">If the user settings that the user wants are applied in the wrong order, they can be recovered by performing a restore operation for the specific application or Windows configuration on the computer on which the settings were overwritten.</span></span> <span data-ttu-id="169b7-412">Para obter mais informações, consulte [gerenciar backup e restauração administrativos no UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).</span><span class="sxs-lookup"><span data-stu-id="169b7-412">For more information, see [Manage Administrative Backup and Restore in UE-V 2.x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).</span></span>

### <a href="" id="capacity"></a><span data-ttu-id="169b7-413">Desempenho e planejamento de capacidade</span><span class="sxs-lookup"><span data-stu-id="169b7-413">Performance and capacity planning</span></span>

<span data-ttu-id="169b7-414">Especifique seus requisitos para UE-V com capacidade de disco padrão e monitoramento da integridade da rede.</span><span class="sxs-lookup"><span data-stu-id="169b7-414">Specify your requirements for UE-V with standard disk capacity and network health monitoring.</span></span>

<span data-ttu-id="169b7-415">O UE-V usa um compartilhamento SMB (Server Message Block) para o armazenamento de pacotes de configurações.</span><span class="sxs-lookup"><span data-stu-id="169b7-415">UE-V uses a Server Message Block (SMB) share for the storage of settings packages.</span></span> <span data-ttu-id="169b7-416">O tamanho dos pacotes de configurações varia de acordo com as informações de configuração de cada aplicativo.</span><span class="sxs-lookup"><span data-stu-id="169b7-416">The size of settings packages varies depending on the settings information for each application.</span></span> <span data-ttu-id="169b7-417">Embora a maioria dos pacotes de configurações seja pequena, a sincronização de arquivos potencialmente grandes, como imagens da área de trabalho, pode resultar em desempenho ruim, principalmente em redes mais lentas.</span><span class="sxs-lookup"><span data-stu-id="169b7-417">While most settings packages are small, the synchronization of potentially large files, such as desktop images, can result in poor performance, particularly on slower networks.</span></span>

<span data-ttu-id="169b7-418">Para reduzir problemas com a latência da rede, crie locais de armazenamento de configurações nas mesmas redes locais em que os computadores dos usuários residem.</span><span class="sxs-lookup"><span data-stu-id="169b7-418">To reduce problems with network latency, create settings storage locations on the same local networks where the users’ computers reside.</span></span> <span data-ttu-id="169b7-419">Recomendamos 20 MB de espaço em disco por usuário para o local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="169b7-419">We recommend 20 MB of disk space per user for the settings storage location.</span></span>

<span data-ttu-id="169b7-420">Por padrão, a sincronização do UE-V expira após 2 segundos para evitar retardo excessivo devido a um pacote de configurações grande.</span><span class="sxs-lookup"><span data-stu-id="169b7-420">By default, UE-V synchronization times out after 2 seconds to prevent excessive lag due to a large settings package.</span></span> <span data-ttu-id="169b7-421">Você pode configurar a configuração SyncMethod = SyncProvider usando [objetos de política de grupo](https://technet.microsoft.com/library/dn458893.aspx).</span><span class="sxs-lookup"><span data-stu-id="169b7-421">You can configure the SyncMethod=SyncProvider setting by using [Group Policy Objects](https://technet.microsoft.com/library/dn458893.aspx).</span></span>

### <a href="" id="high"></a><span data-ttu-id="169b7-422">Alta disponibilidade para UE-V</span><span class="sxs-lookup"><span data-stu-id="169b7-422">High Availability for UE-V</span></span>

<span data-ttu-id="169b7-423">O catálogo de modelos de configurações e local de armazenamento de configurações do UE-V dão suporte ao armazenamento de dados do usuário em qualquer compartilhamento gravável.</span><span class="sxs-lookup"><span data-stu-id="169b7-423">The UE-V settings storage location and settings template catalog support storing user data on any writable share.</span></span> <span data-ttu-id="169b7-424">Para garantir alta disponibilidade, siga estes critérios:</span><span class="sxs-lookup"><span data-stu-id="169b7-424">To ensure high availability, follow these criteria:</span></span>

-   <span data-ttu-id="169b7-425">Formate o volume de armazenamento com um sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="169b7-425">Format the storage volume with an NTFS file system.</span></span>

-   <span data-ttu-id="169b7-426">O compartilhamento pode usar o sistema de arquivos distribuídos (DFS), mas há restrições.</span><span class="sxs-lookup"><span data-stu-id="169b7-426">The share can use Distributed File System (DFS) but there are restrictions.</span></span>
<span data-ttu-id="169b7-427">Especificamente, não há suporte para a configuração de destino único DFS-R (DFS – Distributed File System Replication) com ou sem um namespace do sistema de arquivos distribuído (DFS-N).</span><span class="sxs-lookup"><span data-stu-id="169b7-427">Specifically, Distributed File System Replication (DFS-R) single target configuration with or without a Distributed File System Namespace (DFS-N) is supported.</span></span>
<span data-ttu-id="169b7-428">Da mesma forma, somente a configuração de destino única é compatível com o DFS-N.</span><span class="sxs-lookup"><span data-stu-id="169b7-428">Likewise, only single target configuration is supported with DFS-N.</span></span>
<span data-ttu-id="169b7-429">Para obter informações detalhadas, consulte a [declaração de suporte da Microsoft em torno de dados de perfil de usuário replicado](https://go.microsoft.com/fwlink/p/?LinkId=313991) e também [informações sobre a política de suporte da Microsoft para um cenário de implantação DFS-R e DFS-N](https://support.microsoft.com/kb/2533009).</span><span class="sxs-lookup"><span data-stu-id="169b7-429">For detailed information, see [Microsoft’s Support Statement Around Replicated User Profile Data](https://go.microsoft.com/fwlink/p/?LinkId=313991) and also [Information about Microsoft support policy for a DFS-R and DFS-N deployment scenario](https://support.microsoft.com/kb/2533009).</span></span>

    <span data-ttu-id="169b7-430">Além disso, como o SYSVOL usa o DFS-R para replicação, o SYSVOL não pode ser usado para a replicação de arquivos de dados do UE-V.</span><span class="sxs-lookup"><span data-stu-id="169b7-430">In addition, because SYSVOL uses DFS-R for replication, SYSVOL cannot be used for UE-V data file replication.</span></span>

-   <span data-ttu-id="169b7-431">Configure as permissões de compartilhamento e as listas de controle de acesso NTFS (ACLs) conforme especificado em [implantando o local de armazenamento de configurações para UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#ssl).</span><span class="sxs-lookup"><span data-stu-id="169b7-431">Configure the share permissions and NTFS access control lists (ACLs) as specified in [Deploying the Settings Storage Location for UE-V 2.x](https://technet.microsoft.com/library/dn458891.aspx#ssl).</span></span>

-   <span data-ttu-id="169b7-432">Use o agrupamento de servidor de arquivos juntamente com o UE-V Agent para fornecer acesso a cópias de dados de estado do usuário no caso de falhas de comunicação.</span><span class="sxs-lookup"><span data-stu-id="169b7-432">Use file server clustering along with the UE-V Agent to provide access to copies of user state data in the event of communications failures.</span></span>

-   <span data-ttu-id="169b7-433">Você pode armazenar os dados de caminho de armazenamento de configurações (dados do usuário) e modelos de catálogo de modelos de configurações em compartilhamentos de cluster, em compartilhamentos DFS-N ou em ambos.</span><span class="sxs-lookup"><span data-stu-id="169b7-433">You can store the settings storage path data (user data) and settings template catalog templates on clustered shares, on DFS-N shares, or on both.</span></span>

### <a href="" id="clocksync"></a><span data-ttu-id="169b7-434">Sincronizar os relógios do computador para a sincronização de configurações do UE-V</span><span class="sxs-lookup"><span data-stu-id="169b7-434">Synchronize computer clocks for UE-V settings synchronization</span></span>

<span data-ttu-id="169b7-435">Os computadores que executam o UE-V Agent devem usar um servidor de horário para manter uma experiência de configuração consistente.</span><span class="sxs-lookup"><span data-stu-id="169b7-435">Computers that run the UE-V Agent must use a time server to maintain a consistent settings experience.</span></span> <span data-ttu-id="169b7-436">O UE-V usa carimbos de data/hora para determinar se as configurações devem ser sincronizadas do local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="169b7-436">UE-V uses time stamps to determine if settings must be synchronized from the settings storage location.</span></span> <span data-ttu-id="169b7-437">Se o relógio do computador não for exato, as configurações mais antigas podem substituir as configurações mais recentes, ou as novas configurações podem não ser salvas no local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="169b7-437">If the computer clock is inaccurate, older settings can overwrite newer settings, or the new settings might not be saved to the settings storage location.</span></span>

## <a href="" id="prereqs"></a><span data-ttu-id="169b7-438">Confirme pré-requisitos e configurações com suporte para UE-V</span><span class="sxs-lookup"><span data-stu-id="169b7-438">Confirm Prerequisites and Supported Configurations for UE-V</span></span>


<span data-ttu-id="169b7-439">Antes de prosseguir, verifique se o seu ambiente inclui estes requisitos para executar o UE-V.</span><span class="sxs-lookup"><span data-stu-id="169b7-439">Before you proceed, make sure your environment includes these requirements for running UE-V.</span></span>

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
<th align="left"><strong><span data-ttu-id="169b7-440">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="169b7-440">Operating system</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="169b7-441">Edição</span><span class="sxs-lookup"><span data-stu-id="169b7-441">Edition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="169b7-442">Service Pack</span><span class="sxs-lookup"><span data-stu-id="169b7-442">Service pack</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="169b7-443">Arquitetura do sistema</span><span class="sxs-lookup"><span data-stu-id="169b7-443">System architecture</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="169b7-444">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="169b7-444">Windows PowerShell</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="169b7-445">Microsoft .NET Framework</span><span class="sxs-lookup"><span data-stu-id="169b7-445">Microsoft .NET Framework</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="169b7-446">Windows 7</span><span class="sxs-lookup"><span data-stu-id="169b7-446">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-447">Ultimate, Enterprise ou Professional Edition</span><span class="sxs-lookup"><span data-stu-id="169b7-447">Ultimate, Enterprise, or Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-448">SP1</span><span class="sxs-lookup"><span data-stu-id="169b7-448">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-449">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="169b7-449">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-450">Windows PowerShell 3,0 ou superior</span><span class="sxs-lookup"><span data-stu-id="169b7-450">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-451">.NET Framework 4,5 ou superior para UE-V 2,1.</span><span class="sxs-lookup"><span data-stu-id="169b7-451">.NET Framework 4.5 or higher for UE-V 2.1.</span></span></p>
<p><span data-ttu-id="169b7-452">.NET Framework 4 ou superior para UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="169b7-452">.NET Framework 4 or higher for UE-V 2.0.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="169b7-453">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="169b7-453">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-454">Standard, Enterprise, Datacenter ou servidor Web</span><span class="sxs-lookup"><span data-stu-id="169b7-454">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-455">SP1</span><span class="sxs-lookup"><span data-stu-id="169b7-455">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-456">64 bits</span><span class="sxs-lookup"><span data-stu-id="169b7-456">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-457">Windows PowerShell 3,0 ou superior</span><span class="sxs-lookup"><span data-stu-id="169b7-457">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-458">.NET Framework 4,5 ou superior para UE-V 2,1.</span><span class="sxs-lookup"><span data-stu-id="169b7-458">.NET Framework 4.5 or higher for UE-V 2.1.</span></span></p>
<p><span data-ttu-id="169b7-459">.NET Framework 4 ou superior para UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="169b7-459">.NET Framework 4 or higher for UE-V 2.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="169b7-460">Windows 8 e Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="169b7-460">Windows 8 and Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-461">Enterprise ou pro</span><span class="sxs-lookup"><span data-stu-id="169b7-461">Enterprise or Pro</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-462">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="169b7-462">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-463">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="169b7-463">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-464">Windows PowerShell 3,0 ou superior</span><span class="sxs-lookup"><span data-stu-id="169b7-464">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-465">.NET Framework 4,5 ou superior</span><span class="sxs-lookup"><span data-stu-id="169b7-465">.NET Framework 4.5 or higher</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="169b7-466">Windows 10, versão anterior ao 1607</span><span class="sxs-lookup"><span data-stu-id="169b7-466">Windows 10, pre-1607 version</span></span></p>
<div class="alert">
<strong><span data-ttu-id="169b7-467">Observação</span><span class="sxs-lookup"><span data-stu-id="169b7-467">Note</span></span></strong><br/><p><span data-ttu-id="169b7-468">Somente o UE-V 2,1 SP1 é compatível com o Windows 10, versão anterior ao 1607</span><span class="sxs-lookup"><span data-stu-id="169b7-468">Only UE-V 2.1 SP1 supports Windows 10, pre-1607 version</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="169b7-469">Enterprise ou pro</span><span class="sxs-lookup"><span data-stu-id="169b7-469">Enterprise or Pro</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-470">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="169b7-470">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-471">32 bits ou 64 bits</span><span class="sxs-lookup"><span data-stu-id="169b7-471">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-472">Windows PowerShell 3,0 ou superior</span><span class="sxs-lookup"><span data-stu-id="169b7-472">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-473">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="169b7-473">.NET Framework 4.6</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="169b7-474">Windows Server 2012 e Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="169b7-474">Windows Server 2012 and Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-475">Padrão ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="169b7-475">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-476">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="169b7-476">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-477">64 bits</span><span class="sxs-lookup"><span data-stu-id="169b7-477">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-478">Windows PowerShell 3,0 ou superior</span><span class="sxs-lookup"><span data-stu-id="169b7-478">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-479">.NET Framework 4,5 ou superior</span><span class="sxs-lookup"><span data-stu-id="169b7-479">.NET Framework 4.5 or higher</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="169b7-480">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="169b7-480">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-481">Padrão ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="169b7-481">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-482">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="169b7-482">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-483">64 bits</span><span class="sxs-lookup"><span data-stu-id="169b7-483">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-484">Windows PowerShell 3,0 ou superior</span><span class="sxs-lookup"><span data-stu-id="169b7-484">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="169b7-485">.NET Framework 4,6 ou superior</span><span class="sxs-lookup"><span data-stu-id="169b7-485">.NET Framework 4.6 or higher</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="169b7-486">Também...</span><span class="sxs-lookup"><span data-stu-id="169b7-486">Also…</span></span>

-   <span data-ttu-id="169b7-487">**Licença do MDOP:** Essa tecnologia é parte do Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="169b7-487">**MDOP License:** This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="169b7-488">Os clientes empresariais podem obter o MDOP com o Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="169b7-488">Enterprise customers can get MDOP with Microsoft Software Assurance.</span></span> <span data-ttu-id="169b7-489">Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte como obter o MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="169b7-489">For more information about Microsoft Software Assurance and acquiring MDOP, see How Do I Get MDOP (https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span>

-   <span data-ttu-id="169b7-490">**Credenciais administrativas** para qualquer computador no qual você irá instalar</span><span class="sxs-lookup"><span data-stu-id="169b7-490">**Administrative Credentials** for any computer on which you’ll be installing</span></span>

**<span data-ttu-id="169b7-491">Observação</span><span class="sxs-lookup"><span data-stu-id="169b7-491">Note</span></span>**  

-   <span data-ttu-id="169b7-492">A partir do WIndows 10, versão 1607, o UE-V está incluído no [Windows 10 para empresas](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) e não faz mais parte do Microsoft Desktop Optimization Pack.</span><span class="sxs-lookup"><span data-stu-id="169b7-492">Starting with WIndows 10, version 1607, UE-V is included with [Windows 10 for Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) and is no longer part of the Microsoft Desktop Optimization Pack.</span></span>

-   <span data-ttu-id="169b7-493">O recurso do UE-V Windows PowerShell do UE-V Agent requer o .NET Framework 4 ou superior, e o Windows PowerShell 3,0 ou superior esteja habilitado.</span><span class="sxs-lookup"><span data-stu-id="169b7-493">The UE-V Windows PowerShell feature of the UE-V Agent requires .NET Framework 4 or higher and Windows PowerShell 3.0 or higher to be enabled.</span></span> <span data-ttu-id="169b7-494">Baixe o Windows PowerShell 3,0 [aqui](https://go.microsoft.com/fwlink/?LinkId=309609).</span><span class="sxs-lookup"><span data-stu-id="169b7-494">Download Windows PowerShell 3.0 [here](https://go.microsoft.com/fwlink/?LinkId=309609).</span></span>

-   <span data-ttu-id="169b7-495">Instale o .NET Framework 4 ou o .NET Framework 4,5 em computadores que executam o sistema operacional Windows 7 ou Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="169b7-495">Install .NET Framework 4 or .NET Framework 4.5 on computers that run the Windows 7 or the Windows Server 2008 R2 operating system.</span></span> <span data-ttu-id="169b7-496">Os sistemas operacionais Windows 8, Windows 8,1 e Windows Server 2012 vêm com o .NET Framework 4,5 instalado.</span><span class="sxs-lookup"><span data-stu-id="169b7-496">The Windows 8, Windows 8.1, and Windows Server 2012 operating systems come with .NET Framework 4.5 installed.</span></span> <span data-ttu-id="169b7-497">O sistema operacional Windows 10 vem com o .NET Framework 4,6 instalado.</span><span class="sxs-lookup"><span data-stu-id="169b7-497">The Windows 10 operating system comes with .NET Framework 4.6 installed.</span></span>
-   <span data-ttu-id="169b7-498">A política "Excluir cache de roaming" para perfis obrigatórios não é compatível com UE-V e não deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="169b7-498">The “Delete Roaming Cache” policy for Mandatory profiles is not supported with UE-V and should not be used.</span></span>



<span data-ttu-id="169b7-499">Não há requisitos especiais de memória de acesso aleatório (RAM) específicos para o UE-V.</span><span class="sxs-lookup"><span data-stu-id="169b7-499">There are no special random access memory (RAM) requirements specific to UE-V.</span></span>

### <span data-ttu-id="169b7-500">Sincronização de configurações por meio do provedor de sincronização</span><span class="sxs-lookup"><span data-stu-id="169b7-500">Synchronization of Settings through the Sync Provider</span></span>

<span data-ttu-id="169b7-501">O provedor de sincronização é a configuração padrão para os usuários, que sincroniza um cache local com o local de armazenamento de configurações nestes casos:</span><span class="sxs-lookup"><span data-stu-id="169b7-501">Sync Provider is the default setting for users, which synchronizes a local cache with the settings storage location in these instances:</span></span>

-   <span data-ttu-id="169b7-502">Logon/logoff</span><span class="sxs-lookup"><span data-stu-id="169b7-502">Logon/logoff</span></span>

-   <span data-ttu-id="169b7-503">Bloquear/desbloquear</span><span class="sxs-lookup"><span data-stu-id="169b7-503">Lock/unlock</span></span>

-   <span data-ttu-id="169b7-504">Conexão/desconexão da área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="169b7-504">Remote desktop connect/disconnect</span></span>

-   <span data-ttu-id="169b7-505">Abrir/fechar aplicativo</span><span class="sxs-lookup"><span data-stu-id="169b7-505">Application open/close</span></span>

<span data-ttu-id="169b7-506">Uma tarefa agendada gerencia essa sincronização de configurações a cada 30 minutos ou por meio de certos eventos de gatilho para determinados aplicativos.</span><span class="sxs-lookup"><span data-stu-id="169b7-506">A scheduled task manages this synchronization of settings every 30 minutes or through certain trigger events for certain applications.</span></span> <span data-ttu-id="169b7-507">Para obter mais informações, consulte [alterando a frequência das tarefas agendadas de UE-V 2. x](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="169b7-507">For more information, see [Changing the Frequency of UE-V 2.x Scheduled Tasks](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span></span>

<span data-ttu-id="169b7-508">O UE-V Agent sincroniza as configurações do usuário para computadores que não estão sempre conectados à rede corporativa (computadores remotos e laptops) e computadores que estão sempre conectados à rede (computadores que executam o Windows Server e hospedam sessões da interface de área de trabalho virtual (VDI)).</span><span class="sxs-lookup"><span data-stu-id="169b7-508">The UE-V Agent synchronizes user settings for computers that are not always connected to the enterprise network (remote computers and laptops) and computers that are always connected to the network (computers that run Windows Server and host virtual desktop interface (VDI) sessions).</span></span>

<span data-ttu-id="169b7-509">**Sincronização para computadores com conexões sempre disponíveis:** Quando você usa o UE-V em computadores que estão sempre conectados à rede, você deve configurar o UE-V Agent para sincronizar as configurações usando o parâmetro *SyncMethod = None* , que trata o servidor de armazenamento de configurações como um compartilhamento de rede padrão.</span><span class="sxs-lookup"><span data-stu-id="169b7-509">**Synchronization for computers with always-available connections:** When you use UE-V on computers that are always connected to the network, you must configure the UE-V Agent to synchronize settings by using the *SyncMethod=None* parameter, which treats the settings storage server as a standard network share.</span></span> <span data-ttu-id="169b7-510">Nesta configuração, o UE-V Agent pode ser configurado para notificar se a importação das configurações do aplicativo for adiada.</span><span class="sxs-lookup"><span data-stu-id="169b7-510">In this configuration, the UE-V Agent can be configured to notify if the import of the application settings is delayed.</span></span>

<span data-ttu-id="169b7-511">Habilite essa configuração por meio de um destes métodos:</span><span class="sxs-lookup"><span data-stu-id="169b7-511">Enable this configuration through one of these methods:</span></span>

-   <span data-ttu-id="169b7-512">Durante a instalação do UE-V, no prompt de comando ou em um arquivo em lotes, defina o parâmetro AgentSetup.exe *SyncMethod = None*.</span><span class="sxs-lookup"><span data-stu-id="169b7-512">During UE-V installation, at the command prompt or in a batch file, set the AgentSetup.exe parameter *SyncMethod = None*.</span></span> <span data-ttu-id="169b7-513">[A implantação do agente do UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#agent) fornece mais informações.</span><span class="sxs-lookup"><span data-stu-id="169b7-513">[Deploying the UE-V 2.x Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) provides more information.</span></span>

-   <span data-ttu-id="169b7-514">Após a instalação do UE-V, use o recurso de gerenciamento de configurações no System Center 2012 Configuration Manager ou os modelos ADMX do MDOP para empurrar a configuração *SyncMethod = None* .</span><span class="sxs-lookup"><span data-stu-id="169b7-514">After the UE-V installation, use the Settings Management feature in System Center 2012 Configuration Manager or the MDOP ADMX templates to push the *SyncMethod = None* configuration.</span></span>

-   <span data-ttu-id="169b7-515">Use o Windows PowerShell ou WMI (Instrumentação de gerenciamento do Windows) para definir a configuração *SyncMethod = None* .</span><span class="sxs-lookup"><span data-stu-id="169b7-515">Use Windows PowerShell or Windows Management Instrumentation (WMI) to set the *SyncMethod = None* configuration.</span></span>

    **<span data-ttu-id="169b7-516">Observação</span><span class="sxs-lookup"><span data-stu-id="169b7-516">Note</span></span>**  
    <span data-ttu-id="169b7-517">Esses dois últimos métodos não funcionam para ambientes de infraestrutura de área de trabalho virtual (VDI) em pool.</span><span class="sxs-lookup"><span data-stu-id="169b7-517">These last two methods do not work for pooled virtual desktop infrastructure (VDI) environments.</span></span>



<span data-ttu-id="169b7-518">Você deve reiniciar o computador para que as configurações comecem a sincronizar.</span><span class="sxs-lookup"><span data-stu-id="169b7-518">You must restart the computer before the settings start to synchronize.</span></span>

**<span data-ttu-id="169b7-519">Observação</span><span class="sxs-lookup"><span data-stu-id="169b7-519">Note</span></span>**  
<span data-ttu-id="169b7-520">Se você definir *SyncMethod = None*, todas as alterações de configurações serão salvas diretamente no servidor.</span><span class="sxs-lookup"><span data-stu-id="169b7-520">If you set *SyncMethod = None*, any settings changes are saved directly to the server.</span></span> <span data-ttu-id="169b7-521">Se a conexão de rede com o caminho de armazenamento de configurações não for encontrada, as alterações de configurações serão armazenadas em cache no dispositivo e sincronizadas na próxima vez que o provedor de sincronização for executado.</span><span class="sxs-lookup"><span data-stu-id="169b7-521">If the network connection to the settings storage path is not found, then the settings changes are cached on the device and are synchronized the next time that the sync provider runs.</span></span> <span data-ttu-id="169b7-522">Se o caminho de armazenamento de configurações não for encontrado e o perfil do usuário for removido de um ambiente de VDI em pool no logoff, as alterações de configurações serão perdidas e o usuário deverá reaplicar a alteração quando o computador for reconectado ao caminho de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="169b7-522">If the settings storage path is not found and the user profile is removed from a pooled VDI environment on logoff, settings changes are lost and the user must reapply the change when the computer is reconnected to the settings storage path.</span></span>



<span data-ttu-id="169b7-523">**Sincronização para mecanismos de sincronização externos:** O parâmetro *SyncMethod = external* especifica que se as configurações de UE-V forem gravadas em uma pasta local no computador do usuário, qualquer mecanismo de sincronização externo (como o onedrive for Business, as pastas de trabalho, o SharePoint ou o Dropbox) pode ser usado para aplicar essas configurações aos diferentes computadores que os usuários acessam.</span><span class="sxs-lookup"><span data-stu-id="169b7-523">**Synchronization for external sync engines:** The *SyncMethod=External* parameter specifies that if UE-V settings are written to a local folder on the user computer, then any external sync engine (such as OneDrive for Business, Work Folders, Sharepoint, or Dropbox) can be used to apply these settings to the different computers that users access.</span></span>

<span data-ttu-id="169b7-524">**Suporte para sessões de VDI compartilhadas:** O UE-V 2,1 e o 2,1 SP1 oferecem suporte a sessões do VDI compartilhadas entre os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="169b7-524">**Support for shared VDI sessions:** UE-V 2.1 and 2.1 SP1 provide support for VDI sessions that are shared among end users.</span></span> <span data-ttu-id="169b7-525">Você pode registrar e configurar um modelo VDI especial, o que garante que o UE-V mantém toda a funcionalidade intacta em sessões de VDI não persistentes.</span><span class="sxs-lookup"><span data-stu-id="169b7-525">You can register and configure a special VDI template, which ensures that UE-V keeps all of its functionality intact for non-persistent VDI sessions.</span></span>

**<span data-ttu-id="169b7-526">Observação</span><span class="sxs-lookup"><span data-stu-id="169b7-526">Note</span></span>**  
<span data-ttu-id="169b7-527">Se você não habilitar o modo VDI para sessões de VDI não persistentes, alguns recursos não funcionarão, como [backup/restauração e última configuração válida (LKG)](https://technet.microsoft.com/library/dn878331.aspx).</span><span class="sxs-lookup"><span data-stu-id="169b7-527">If you do not enable VDI mode for non-persistent VDI sessions, certain features do not work, such as [back-up/restore and last known good (LKG)](https://technet.microsoft.com/library/dn878331.aspx).</span></span>



<span data-ttu-id="169b7-528">O modelo VDI é fornecido com o UE-V 2,1 e o 2,1 SP1 e geralmente está disponível aqui após a instalação: C:\\Arquivos de experiência do usuário do Files\\Microsoft Virtualization\\Templates\\VdiState.xml</span><span class="sxs-lookup"><span data-stu-id="169b7-528">The VDI template is provided with UE-V 2.1 and 2.1 SP1 and is typically available here after installation: C:\\Program Files\\Microsoft User Experience Virtualization\\Templates\\VdiState.xml</span></span>

### <span data-ttu-id="169b7-529">Pré-requisitos para suporte ao gerador do UE-V</span><span class="sxs-lookup"><span data-stu-id="169b7-529">Prerequisites for UE-V Generator support</span></span>

<span data-ttu-id="169b7-530">Instale o UE-V Generator no computador que é usado para criar modelos de local de configurações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="169b7-530">Install the UE-V Generator on the computer that is used to create custom settings location templates.</span></span> <span data-ttu-id="169b7-531">Este computador deve poder executar os aplicativos cujas configurações são sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="169b7-531">This computer should be able to run the applications whose settings are synchronized.</span></span> <span data-ttu-id="169b7-532">Você deve ser membro do grupo Administradores no computador que executa o software do gerador do UE-V.</span><span class="sxs-lookup"><span data-stu-id="169b7-532">You must be a member of the Administrators group on the computer that runs the UE-V Generator software.</span></span>

<span data-ttu-id="169b7-533">O UE-V Generator deve ser instalado em um computador que usa um sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="169b7-533">The UE-V Generator must be installed on a computer that uses an NTFS file system.</span></span> <span data-ttu-id="169b7-534">O software do gerador do UE-V requer o .NET Framework 4.</span><span class="sxs-lookup"><span data-stu-id="169b7-534">The UE-V Generator software requires .NET Framework 4.</span></span> <span data-ttu-id="169b7-535">Para obter mais informações, consulte [implantar o UE-V 2. x para aplicativos personalizados](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="169b7-535">For more information, see [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span></span>

## <span data-ttu-id="169b7-536">Outros recursos para este produto</span><span class="sxs-lookup"><span data-stu-id="169b7-536">Other resources for this product</span></span>


-   [<span data-ttu-id="169b7-537">Microsoft User Experience Virtualization (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="169b7-537">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>](index.md)

-   [<span data-ttu-id="169b7-538">Introdução ao UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="169b7-538">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="169b7-539">Administração do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="169b7-539">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="169b7-540">Solução de problemas do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="169b7-540">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="169b7-541">Referência técnica da UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="169b7-541">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)














