---
title: Implantando o Microsoft Office 2013 usando o App-V
description: Implantando o Microsoft Office 2013 usando o App-V
author: dansimp
ms.assetid: 9a7be05e-2a7a-4874-af25-09c0f5037876
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: f6a54cadce79ff3680fd69206eba8ac3fbe83a68
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796547"
---
# <span data-ttu-id="f593a-103">Implantando o Microsoft Office 2013 usando o App-V</span><span class="sxs-lookup"><span data-stu-id="f593a-103">Deploying Microsoft Office 2013 by Using App-V</span></span>


<span data-ttu-id="f593a-104">Use as informações neste artigo para usar o Microsoft Application Virtualization (App-V) 5,1 ou versões posteriores para fornecer o Microsoft Office 2013 como um aplicativo virtualizado para computadores em sua organização.</span><span class="sxs-lookup"><span data-stu-id="f593a-104">Use the information in this article to use Microsoft Application Virtualization (App-V) 5.1, or later versions, to deliver Microsoft Office 2013 as a virtualized application to computers in your organization.</span></span> <span data-ttu-id="f593a-105">Para obter informações sobre como usar o App-V para fornecer o Office 2010, consulte [implantando o Microsoft Office 2010 usando o app-v](deploying-microsoft-office-2010-by-using-app-v51.md).</span><span class="sxs-lookup"><span data-stu-id="f593a-105">For information about using App-V to deliver Office 2010, see [Deploying Microsoft Office 2010 by Using App-V](deploying-microsoft-office-2010-by-using-app-v51.md).</span></span> <span data-ttu-id="f593a-106">Para implantar com êxito o Office 2013 com o App-V, você precisa estar familiarizado com o Office 2013 e o App-V.</span><span class="sxs-lookup"><span data-stu-id="f593a-106">To successfully deploy Office 2013 with App-V, you need to be familiar with Office 2013 and App-V.</span></span>

<span data-ttu-id="f593a-107">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="f593a-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="f593a-108">O que saber antes de começar</span><span class="sxs-lookup"><span data-stu-id="f593a-108">What to know before you start</span></span>](#bkmk-before-you-start)

-   [<span data-ttu-id="f593a-109">Criando um pacote do Office 2013 para o App-V com a ferramenta de implantação do Office</span><span class="sxs-lookup"><span data-stu-id="f593a-109">Creating an Office 2013 package for App-V with the Office Deployment Tool</span></span>](#bkmk-create-office-pkg)

-   [<span data-ttu-id="f593a-110">Publicando o pacote do Office para o App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="f593a-110">Publishing the Office package for App-V 5.1</span></span>](#bkmk-pub-pkg-office)

-   [<span data-ttu-id="f593a-111">Personalizando e gerenciando pacotes do Office App-V</span><span class="sxs-lookup"><span data-stu-id="f593a-111">Customizing and managing Office App-V packages</span></span>](#bkmk-custmz-manage-office-pkgs)

## <a href="" id="bkmk-before-you-start"></a><span data-ttu-id="f593a-112">O que saber antes de começar</span><span class="sxs-lookup"><span data-stu-id="f593a-112">What to know before you start</span></span>


<span data-ttu-id="f593a-113">Antes de implantar o Office 2013 usando o App-V, examine as informações de planejamento a seguir.</span><span class="sxs-lookup"><span data-stu-id="f593a-113">Before you deploy Office 2013 by using App-V, review the following planning information.</span></span>

### <a href="" id="bkmk-supp-vers-coexist"></a><span data-ttu-id="f593a-114">Versões do Office com suporte e coexistência do Office</span><span class="sxs-lookup"><span data-stu-id="f593a-114">Supported Office versions and Office coexistence</span></span>

<span data-ttu-id="f593a-115">Use a tabela a seguir para obter informações sobre as versões compatíveis do Office e sobre como executar versões coexistentes do Office.</span><span class="sxs-lookup"><span data-stu-id="f593a-115">Use the following table to get information about supported versions of Office and about running coexisting versions of Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f593a-116">Informações a serem revisadas</span><span class="sxs-lookup"><span data-stu-id="f593a-116">Information to review</span></span></th>
<th align="left"><span data-ttu-id="f593a-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="f593a-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="planning-for-using-app-v-with-office51.md#bkmk-office-vers-supp-appv" data-raw-source="[Planning for Using App-V with Office](planning-for-using-app-v-with-office51.md#bkmk-office-vers-supp-appv)"><span data-ttu-id="f593a-118">Planejando o uso do App-V com o Office</span><span class="sxs-lookup"><span data-stu-id="f593a-118">Planning for Using App-V with Office</span></span></a></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f593a-119">Versões com suporte do Office</span><span class="sxs-lookup"><span data-stu-id="f593a-119">Supported versions of Office</span></span></p></li>
<li><p><span data-ttu-id="f593a-120">Tipos de implantação com suporte (por exemplo, área de trabalho, infraestrutura de área de trabalho virtual pessoal (VDI), VDI em pool)</span><span class="sxs-lookup"><span data-stu-id="f593a-120">Supported deployment types (for example, desktop, personal Virtual Desktop Infrastructure (VDI), pooled VDI)</span></span></p></li>
<li><p><span data-ttu-id="f593a-121">Opções de licenciamento do Office</span><span class="sxs-lookup"><span data-stu-id="f593a-121">Office licensing options</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><a href="planning-for-using-app-v-with-office51.md#bkmk-plan-coexisting" data-raw-source="[Planning for Using App-V with Office](planning-for-using-app-v-with-office51.md#bkmk-plan-coexisting)"><span data-ttu-id="f593a-122">Planejando o uso do App-V com o Office</span><span class="sxs-lookup"><span data-stu-id="f593a-122">Planning for Using App-V with Office</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="f593a-123">Considerações para a instalação de diferentes versões do Office no mesmo computador</span><span class="sxs-lookup"><span data-stu-id="f593a-123">Considerations for installing different versions of Office on the same computer</span></span></p></td>
</tr>
</tbody>
</table>


### <a href="" id="bkmk-pkg-pub-reqs"></a><span data-ttu-id="f593a-124">Requisitos de empacotamento, publicação e implantação</span><span class="sxs-lookup"><span data-stu-id="f593a-124">Packaging, publishing, and deployment requirements</span></span>

<span data-ttu-id="f593a-125">Antes de implantar o Office usando o App-V, examine os seguintes requisitos.</span><span class="sxs-lookup"><span data-stu-id="f593a-125">Before you deploy Office by using App-V, review the following requirements.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f593a-126">Tarefa</span><span class="sxs-lookup"><span data-stu-id="f593a-126">Task</span></span></th>
<th align="left"><span data-ttu-id="f593a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f593a-127">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f593a-128">Embalagem</span><span class="sxs-lookup"><span data-stu-id="f593a-128">Packaging</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f593a-129">Todos os aplicativos do Office que você deseja implantar para os usuários devem estar em um único pacote.</span><span class="sxs-lookup"><span data-stu-id="f593a-129">All of the Office applications that you want to deploy to users must be in a single package.</span></span></p></li>
<li><p><span data-ttu-id="f593a-130">No App-V 5,1 e posterior, você deve usar a ferramenta de implantação do Office para criar pacotes.</span><span class="sxs-lookup"><span data-stu-id="f593a-130">In App-V 5.1 and later, you must use the Office Deployment Tool to create packages.</span></span> <span data-ttu-id="f593a-131">Não é possível usar o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="f593a-131">You cannot use the Sequencer.</span></span></p></li>
<li><p><span data-ttu-id="f593a-132">Se você estiver implantando o Microsoft Visio 2013 e o Microsoft Project 2013 juntamente com o Office, deverá incluí-los no mesmo pacote com o Office.</span><span class="sxs-lookup"><span data-stu-id="f593a-132">If you are deploying Microsoft Visio 2013 and Microsoft Project 2013 along with Office, you must include them in the same package with Office.</span></span> <span data-ttu-id="f593a-133">Para obter mais informações, consulte <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2013 and Project 2013 with Office](#bkmk-deploy-visio-project)"> implantação do Visio 2013 e do Project 2013 com o Office </a> .</span><span class="sxs-lookup"><span data-stu-id="f593a-133">For more information, see <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2013 and Project 2013 with Office](#bkmk-deploy-visio-project)">Deploying Visio 2013 and Project 2013 with Office</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f593a-134">Publicação</span><span class="sxs-lookup"><span data-stu-id="f593a-134">Publishing</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f593a-135">Você pode publicar apenas um pacote do Office em cada computador cliente.</span><span class="sxs-lookup"><span data-stu-id="f593a-135">You can publish only one Office package to each client computer.</span></span></p></li>
<li><p><span data-ttu-id="f593a-136">Você deve publicar o pacote do Office globalmente.</span><span class="sxs-lookup"><span data-stu-id="f593a-136">You must publish the Office package globally.</span></span> <span data-ttu-id="f593a-137">Você não pode publicar para o usuário.</span><span class="sxs-lookup"><span data-stu-id="f593a-137">You cannot publish to the user.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f593a-138">Implantando qualquer um dos seguintes produtos em um computador compartilhado, por exemplo, usando serviços de área de trabalho remota:</span><span class="sxs-lookup"><span data-stu-id="f593a-138">Deploying any of the following products to a shared computer, for example, by using Remote Desktop Services:</span></span></p>
<ul>
<li><p><span data-ttu-id="f593a-139">Aplicativos do Microsoft 365 para empresas</span><span class="sxs-lookup"><span data-stu-id="f593a-139">Microsoft 365 Apps for enterprise</span></span></p></li>
<li><p><span data-ttu-id="f593a-140">Visio pro para Office 365</span><span class="sxs-lookup"><span data-stu-id="f593a-140">Visio Pro for Office 365</span></span></p></li>
<li><p><span data-ttu-id="f593a-141">Project pro para Office 365</span><span class="sxs-lookup"><span data-stu-id="f593a-141">Project Pro for Office 365</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="f593a-142">Você deve habilitar a <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)"> ativação de computador compartilhado </a> .</span><span class="sxs-lookup"><span data-stu-id="f593a-142">You must enable <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)">shared computer activation</a>.</span></span></p>
<p><span data-ttu-id="f593a-143">Você não usará a ativação de computador compartilhado se estiver implantando um produto licenciado por volume, como:</span><span class="sxs-lookup"><span data-stu-id="f593a-143">You don’t use shared computer activation if you’re deploying a volume licensed product, such as:</span></span></p>
<ul>
<li><p><span data-ttu-id="f593a-144">Office Professional Plus 2013</span><span class="sxs-lookup"><span data-stu-id="f593a-144">Office Professional Plus 2013</span></span></p></li>
<li><p><span data-ttu-id="f593a-145">Visio Professional 2013</span><span class="sxs-lookup"><span data-stu-id="f593a-145">Visio Professional 2013</span></span></p></li>
<li><p><span data-ttu-id="f593a-146">Project Professional 2013</span><span class="sxs-lookup"><span data-stu-id="f593a-146">Project Professional 2013</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="f593a-147">Excluindo aplicativos do Office de um pacote</span><span class="sxs-lookup"><span data-stu-id="f593a-147">Excluding Office applications from a package</span></span>

<span data-ttu-id="f593a-148">A tabela a seguir descreve os métodos recomendados para excluir aplicativos específicos do Office de um pacote.</span><span class="sxs-lookup"><span data-stu-id="f593a-148">The following table describes the recommended methods for excluding specific Office applications from a package.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f593a-149">Tarefa</span><span class="sxs-lookup"><span data-stu-id="f593a-149">Task</span></span></th>
<th align="left"><span data-ttu-id="f593a-150">Detalhes</span><span class="sxs-lookup"><span data-stu-id="f593a-150">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f593a-151">Use a <strong> </strong> configuração ExcludeApp quando você cria o pacote usando a ferramenta de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="f593a-151">Use the <strong>ExcludeApp</strong> setting when you create the package by using the Office Deployment Tool.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f593a-152">Permite que você exclua aplicativos específicos do Office do pacote quando a ferramenta de implantação do Office cria o pacote.</span><span class="sxs-lookup"><span data-stu-id="f593a-152">Enables you to exclude specific Office applications from the package when the Office Deployment Tool creates the package.</span></span> <span data-ttu-id="f593a-153">Por exemplo, você pode usar essa configuração para criar um pacote que contenha apenas o Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="f593a-153">For example, you can use this setting to create a package that contains only Microsoft Word.</span></span></p></li>
<li><p><span data-ttu-id="f593a-154">Para obter mais informações, consulte o <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)"> elemento ExcludeApp </a> .</span><span class="sxs-lookup"><span data-stu-id="f593a-154">For more information, see <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)">ExcludeApp element</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f593a-155">Modificar o arquivo DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="f593a-155">Modify the DeploymentConfig.xml file</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f593a-156">Modifique o arquivo DeploymentConfig.xml após a criação do pacote.</span><span class="sxs-lookup"><span data-stu-id="f593a-156">Modify the DeploymentConfig.xml file after the package has been created.</span></span> <span data-ttu-id="f593a-157">Esse arquivo contém as configurações padrão do pacote para todos os usuários em um computador que esteja executando o cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="f593a-157">This file contains the default package settings for all users on a computer that is running the App-V Client.</span></span></p></li>
<li><p><span data-ttu-id="f593a-158">Para obter mais informações, consulte <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2013 applications](#bkmk-disable-office-apps)"> desabilitando aplicativos do Office 2013 </a> .</span><span class="sxs-lookup"><span data-stu-id="f593a-158">For more information, see <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2013 applications](#bkmk-disable-office-apps)">Disabling Office 2013 applications</a>.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-create-office-pkg"></a><span data-ttu-id="f593a-159">Criando um pacote do Office 2013 para o App-V com a ferramenta de implantação do Office</span><span class="sxs-lookup"><span data-stu-id="f593a-159">Creating an Office 2013 package for App-V with the Office Deployment Tool</span></span>


<span data-ttu-id="f593a-160">Conclua as etapas a seguir para criar um pacote do Office 2013 para o App-V 5,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="f593a-160">Complete the following steps to create an Office 2013 package for App-V 5.1 or later.</span></span>

**<span data-ttu-id="f593a-161">Importante</span><span class="sxs-lookup"><span data-stu-id="f593a-161">Important</span></span>**  
<span data-ttu-id="f593a-162">No App-V 5,1 e posterior, você deve ter a ferramenta de implantação do Office para criar um pacote.</span><span class="sxs-lookup"><span data-stu-id="f593a-162">In App-V 5.1 and later, you must the Office Deployment Tool to create a package.</span></span> <span data-ttu-id="f593a-163">Você não pode usar o sequenciador para criar pacotes.</span><span class="sxs-lookup"><span data-stu-id="f593a-163">You cannot use the Sequencer to create packages.</span></span>



### <span data-ttu-id="f593a-164">Revisar os pré-requisitos para usar a ferramenta de implantação do Office</span><span class="sxs-lookup"><span data-stu-id="f593a-164">Review prerequisites for using the Office Deployment Tool</span></span>

<span data-ttu-id="f593a-165">O computador no qual você está instalando a ferramenta de implantação do Office deve ter:</span><span class="sxs-lookup"><span data-stu-id="f593a-165">The computer on which you are installing the Office Deployment Tool must have:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f593a-166">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="f593a-166">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="f593a-167">Descrição</span><span class="sxs-lookup"><span data-stu-id="f593a-167">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f593a-168">Software de pré-requisito</span><span class="sxs-lookup"><span data-stu-id="f593a-168">Prerequisite software</span></span></p></td>
<td align="left"><p><span data-ttu-id="f593a-169">.NET Framework 4</span><span class="sxs-lookup"><span data-stu-id="f593a-169">.Net Framework 4</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f593a-170">Sistemas operacionais compatíveis</span><span class="sxs-lookup"><span data-stu-id="f593a-170">Supported operating systems</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f593a-171">versão de 64 bits do Windows 8 ou posterior</span><span class="sxs-lookup"><span data-stu-id="f593a-171">64-bit version of Windows 8 or later</span></span></p></li>
<li><p><span data-ttu-id="f593a-172">versão de 64 bits do Windows 7</span><span class="sxs-lookup"><span data-stu-id="f593a-172">64-bit version of Windows 7</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="f593a-173">Observação</span><span class="sxs-lookup"><span data-stu-id="f593a-173">Note</span></span>**  
<span data-ttu-id="f593a-174">Neste tópico, o termo "Office 2013 App-V Package" refere-se ao licenciamento de assinatura e licenciamento por volume.</span><span class="sxs-lookup"><span data-stu-id="f593a-174">In this topic, the term “Office 2013 App-V package” refers to subscription licensing and volume licensing.</span></span>



### <span data-ttu-id="f593a-175">Criar pacotes do Office 2013 App-V usando a ferramenta de implantação do Office</span><span class="sxs-lookup"><span data-stu-id="f593a-175">Create Office 2013 App-V Packages Using Office Deployment Tool</span></span>

<span data-ttu-id="f593a-176">Você cria pacotes do Office 2013 App-V usando a ferramenta de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="f593a-176">You create Office 2013 App-V packages by using the Office Deployment Tool.</span></span> <span data-ttu-id="f593a-177">As instruções a seguir explicam como criar um pacote do Office 2013 App-V com licenciamento por volume ou licenciamento de assinatura.</span><span class="sxs-lookup"><span data-stu-id="f593a-177">The following instructions explain how to create an Office 2013 App-V package with Volume Licensing or Subscription Licensing.</span></span>

<span data-ttu-id="f593a-178">Crie pacotes do Office 2013 App-V em computadores com Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f593a-178">Create Office 2013 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="f593a-179">Uma vez criado, o pacote do Office 2013 App-V será executado em computadores com o Windows 7, o Windows 8,1 e o Windows 10 com 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f593a-179">Once created, the Office 2013 App-V package will run on 32-bit and 64-bit Windows 7, Windows 8.1, and Windows 10 computers.</span></span>

### <span data-ttu-id="f593a-180">Baixar a ferramenta de implantação do Office</span><span class="sxs-lookup"><span data-stu-id="f593a-180">Download the Office Deployment Tool</span></span>

<span data-ttu-id="f593a-181">Os pacotes do Office 2013 App-V são criados usando a ferramenta de implantação do Office, que gera um pacote do Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="f593a-181">Office 2013 App-V Packages are created using the Office Deployment Tool, which generates an Office 2013 App-V Package.</span></span> <span data-ttu-id="f593a-182">O pacote não pode ser criado ou modificado por meio do sequenciador App-V.</span><span class="sxs-lookup"><span data-stu-id="f593a-182">The package cannot be created or modified through the App-V sequencer.</span></span> <span data-ttu-id="f593a-183">Para começar a criação de pacotes:</span><span class="sxs-lookup"><span data-stu-id="f593a-183">To begin package creation:</span></span>

1.  <span data-ttu-id="f593a-184">Baixe a [ferramenta de implantação do Office para clique para executar](https://www.microsoft.com/download/details.aspx?id=36778).</span><span class="sxs-lookup"><span data-stu-id="f593a-184">Download the [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/download/details.aspx?id=36778).</span></span>

2.  <span data-ttu-id="f593a-185">Execute o arquivo. exe e extraia seus recursos para o local desejado.</span><span class="sxs-lookup"><span data-stu-id="f593a-185">Run the .exe file and extract its features into the desired location.</span></span> <span data-ttu-id="f593a-186">Para facilitar esse processo, você pode criar uma pasta de rede compartilhada na qual os recursos serão salvos.</span><span class="sxs-lookup"><span data-stu-id="f593a-186">To make this process easier, you can create a shared network folder where the features will be saved.</span></span>

    <span data-ttu-id="f593a-187">Exemplo: \\\\Server\\Office2013</span><span class="sxs-lookup"><span data-stu-id="f593a-187">Example: \\\\Server\\Office2013</span></span>

3.  <span data-ttu-id="f593a-188">Verifique se há um setup.exe e um arquivo configuration.xml e se estão no local especificado.</span><span class="sxs-lookup"><span data-stu-id="f593a-188">Check that a setup.exe and a configuration.xml file exist and are in the location you specified.</span></span>

### <span data-ttu-id="f593a-189">Baixar aplicativos do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f593a-189">Download Office 2013 applications</span></span>

<span data-ttu-id="f593a-190">Depois de baixar a ferramenta de implantação do Office, você pode usá-la para obter os aplicativos mais recentes do Office 2013.</span><span class="sxs-lookup"><span data-stu-id="f593a-190">After you download the Office Deployment Tool, you can use it to get the latest Office 2013 applications.</span></span> <span data-ttu-id="f593a-191">Depois de obter os aplicativos do Office, crie o pacote do Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="f593a-191">After getting the Office applications, you create the Office 2013 App-V package.</span></span>

<span data-ttu-id="f593a-192">O arquivo XML que está incluído na ferramenta de implantação do Office especifica os detalhes do produto, como os idiomas e os aplicativos do Office incluídos.</span><span class="sxs-lookup"><span data-stu-id="f593a-192">The XML file that is included in the Office Deployment Tool specifies the product details, such as the languages and Office applications included.</span></span>

1.  <span data-ttu-id="f593a-193">**Personalize o arquivo de configuração XML de exemplo:** Use o arquivo de configuração XML de exemplo que você baixou com a ferramenta de implantação do Office para personalizar os aplicativos do Office:</span><span class="sxs-lookup"><span data-stu-id="f593a-193">**Customize the sample XML configuration file:** Use the sample XML configuration file that you downloaded with the Office Deployment Tool to customize the Office applications:</span></span>

    1.  <span data-ttu-id="f593a-194">Abra o arquivo XML de exemplo no bloco de notas ou no seu editor de texto favorito.</span><span class="sxs-lookup"><span data-stu-id="f593a-194">Open the sample XML file in Notepad or your favorite text editor.</span></span>

    2.  <span data-ttu-id="f593a-195">Com o exemplo configuration.xml arquivo aberto e pronto para edição, você pode especificar produtos, idiomas e o caminho para o qual você salva os aplicativos do Office 2013.</span><span class="sxs-lookup"><span data-stu-id="f593a-195">With the sample configuration.xml file open and ready for editing, you can specify products, languages, and the path to which you save the Office 2013 applications.</span></span> <span data-ttu-id="f593a-196">Veja a seguir um exemplo básico do arquivo configuration.xml:</span><span class="sxs-lookup"><span data-stu-id="f593a-196">The following is a basic example of the configuration.xml file:</span></span>

        ```xml
        <Configuration>
           <Add SourcePath= ”\\Server\Office2013” OfficeClientEdition="32" >
            <Product ID="O365ProPlusRetail ">
              <Language ID="en-us" />
            </Product>
            <Product ID="VisioProRetail">
              <Language ID="en-us" />
            </Product>
          </Add>
        </Configuration>
        ```

        **<span data-ttu-id="f593a-197">Observação</span><span class="sxs-lookup"><span data-stu-id="f593a-197">Note</span></span>**  
        <span data-ttu-id="f593a-198">O XML de configuração é um arquivo XML de exemplo.</span><span class="sxs-lookup"><span data-stu-id="f593a-198">The configuration XML is a sample XML file.</span></span> <span data-ttu-id="f593a-199">O arquivo inclui linhas que foram comentadas. Você pode "remover o comentário" dessas linhas para personalizar as configurações adicionais com o arquivo.</span><span class="sxs-lookup"><span data-stu-id="f593a-199">The file includes lines that are commented out. You can “uncomment” these lines to customize additional settings with the file.</span></span>



~~~
    The above XML configuration file specifies that Office 2013 ProPlus 32-bit edition, including Visio ProPlus, will be downloaded in English to the \\\\server\\Office 2013, which is the location where Office applications will be saved to. Note that the Product ID of the applications will not affect the final licensing of Office. Office 2013 App-V packages with various licensing can be created from the same applications through specifying licensing in a later stage. The table below summarizes the customizable attributes and elements of XML file:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Input</th>
    <th align="left">Description</th>
    <th align="left">Example</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Add element</p></td>
    <td align="left"><p>Specifies the products and languages to include in the package.</p></td>
    <td align="left"><p>N/A</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>OfficeClientEdition (attribute of Add element)</p></td>
    <td align="left"><p>Specifies the edition of Office 2013 product to use: 32-bit or 64-bit. The operation fails if <strong>OfficeClientEdition</strong> is not set to a valid value.</p></td>
    <td align="left"><p><strong>OfficeClientEdition</strong>=&quot;32&quot;</p>
    <p><strong>OfficeClientEdition</strong>=&quot;64&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Product element</p></td>
    <td align="left"><p>Specifies the application. Project 2013 and Visio 2013 must be specified here as an added product to be included in the applications.</p></td>
    <td align="left"><p><code>Product ID =&quot;O365ProPlusRetail &quot;</code></p>
    <p><code>Product ID =&quot;VisioProRetail&quot;</code></p>
    <p><code>Product ID =&quot;ProjectProRetail&quot;</code></p>
    <p><code>Product ID =&quot;ProPlusVolume&quot;</code></p>
    <p><code>Product ID =&quot;VisioProVolume&quot;</code></p>
    <p><code>Product ID = &quot;ProjectProVolume&quot;</code></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Language element</p></td>
    <td align="left"><p>Specifies the language supported in the applications</p></td>
    <td align="left"><p><code>Language ID=&quot;en-us&quot;</code></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Version (attribute of Add element)</p></td>
    <td align="left"><p>Optional. Specifies a build to use for the package</p>
    <p>Defaults to latest advertised build (as defined in v32.CAB at the Office source).</p></td>
    <td align="left"><p><code>15.1.2.3</code></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>SourcePath (attribute of Add element)</p></td>
    <td align="left"><p>Specifies the location in which the applications will be saved to.</p></td>
    <td align="left"><p><code>Sourcepath = &quot;\\Server\Office2013”</code></p></td>
    </tr>
    </tbody>
    </table>



    After editing the configuration.xml file to specify the desired product, languages, and also the location which the Office 2013 applications will be saved onto, you can save the configuration file, for example, as Customconfig.xml.
~~~

2. <span data-ttu-id="f593a-200">**Baixe os aplicativos para o local especificado:** Use um prompt de comando elevado e um sistema operacional de 64 bits para baixar os aplicativos do Office 2013 que serão convertidos posteriormente em um pacote do App-V.</span><span class="sxs-lookup"><span data-stu-id="f593a-200">**Download the applications into the specified location:** Use an elevated command prompt and a 64 bit operating system to download the Office 2013 applications that will later be converted into an App-V package.</span></span> <span data-ttu-id="f593a-201">Veja a seguir um exemplo de comando com a descrição de detalhes:</span><span class="sxs-lookup"><span data-stu-id="f593a-201">Below is an example command with description of details:</span></span>

   ``` syntax
   \\server\Office2013\setup.exe /download \\server\Office2013\Customconfig.xml
   ```

   <span data-ttu-id="f593a-202">No exemplo:</span><span class="sxs-lookup"><span data-stu-id="f593a-202">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f593a-203">\server\Office2013</span><span class="sxs-lookup"><span data-stu-id="f593a-203">\server\Office2013</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f593a-204">é o local de compartilhamento de rede que contém a ferramenta de implantação do Office e o arquivo de Configuration.xml personalizado Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="f593a-204">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="f593a-205">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="f593a-205">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f593a-206">é a ferramenta de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="f593a-206">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f593a-207">/Download</span><span class="sxs-lookup"><span data-stu-id="f593a-207">/download</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f593a-208">baixa os aplicativos do Office 2013 que você especificar no arquivo customConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="f593a-208">downloads the Office 2013 applications that you specify in the customConfig.xml file.</span></span> <span data-ttu-id="f593a-209">Esses bits podem ser convertidos posteriormente em um pacote do Office 2013 App-V com licenciamento por volume.</span><span class="sxs-lookup"><span data-stu-id="f593a-209">These bits can be later converted in an Office 2013 App-V package with Volume Licensing.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="f593a-210">\server\Office2013\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="f593a-210">\server\Office2013\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f593a-211">passa o arquivo de configuração XML necessário para concluir o processo de download, neste exemplo, customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="f593a-211">passes the XML configuration file required to complete the download process, in this example, customconfig.xml.</span></span> <span data-ttu-id="f593a-212">Depois de usar o comando download, os aplicativos do Office devem ser encontrados no local especificado no arquivo XML de configuração, neste exemplo \Server\Office2013.</span><span class="sxs-lookup"><span data-stu-id="f593a-212">After using the download command, Office applications should be found in the location specified in the configuration xml file, in this example \Server\Office2013.</span></span></p></td>
   </tr>
   </tbody>
   </table>



### <span data-ttu-id="f593a-213">Converter os aplicativos do Office em um pacote do App-V</span><span class="sxs-lookup"><span data-stu-id="f593a-213">Convert the Office applications into an App-V package</span></span>

<span data-ttu-id="f593a-214">Depois de baixar os aplicativos do Office 2013 por meio da ferramenta de implantação do Office, use a ferramenta de implantação do Office para convertê-los em um pacote do Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="f593a-214">After you download the Office 2013 applications through the Office Deployment Tool, use the Office Deployment Tool to convert them into an Office 2013 App-V package.</span></span> <span data-ttu-id="f593a-215">Conclua as etapas que correspondem ao seu modelo de licenciamento.</span><span class="sxs-lookup"><span data-stu-id="f593a-215">Complete the steps that correspond to your licensing model.</span></span>

**<span data-ttu-id="f593a-216">Resumo do que você precisará fazer:</span><span class="sxs-lookup"><span data-stu-id="f593a-216">Summary of what you’ll need to do:</span></span>**

-   <span data-ttu-id="f593a-217">Crie os pacotes do Office 2013 App-V em computadores com Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f593a-217">Create the Office 2013 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="f593a-218">No entanto, o pacote será executado em computadores 64 com o Windows 7, Windows 8 e Windows 10 em 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f593a-218">However, the package will run on 32-bit and 64-bit Windows 7, Windows 8, and Windows 10 computers.</span></span>

-   <span data-ttu-id="f593a-219">Crie um pacote do Office App-V para o pacote de licenciamento de assinatura ou o licenciamento por volume usando a ferramenta de implantação do Office e modifique o arquivo de configuração do CustomConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="f593a-219">Create an Office App-V package for either Subscription Licensing package or Volume Licensing by using the Office Deployment Tool, and then modify the CustomConfig.xml configuration file.</span></span>

    <span data-ttu-id="f593a-220">A tabela a seguir resume os valores que você precisa inserir no arquivo CustomConfig.xml para o modelo de licenciamento que você está usando.</span><span class="sxs-lookup"><span data-stu-id="f593a-220">The following table summarizes the values you need to enter in the CustomConfig.xml file for the licensing model you’re using.</span></span> <span data-ttu-id="f593a-221">As etapas nas seções que seguem a tabela especificarão as entradas exatas que você precisa fazer.</span><span class="sxs-lookup"><span data-stu-id="f593a-221">The steps in the sections that follow the table will specify the exact entries you need to make.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f593a-222">ID do Produto (Product ID)</span><span class="sxs-lookup"><span data-stu-id="f593a-222">Product ID</span></span></th>
<th align="left"><span data-ttu-id="f593a-223">Licenciamento por volume</span><span class="sxs-lookup"><span data-stu-id="f593a-223">Volume Licensing</span></span></th>
<th align="left"><span data-ttu-id="f593a-224">Licenciamento de assinatura</span><span class="sxs-lookup"><span data-stu-id="f593a-224">Subscription Licensing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f593a-225">Office 2013</span><span class="sxs-lookup"><span data-stu-id="f593a-225">Office 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f593a-226">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="f593a-226">ProPlusVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="f593a-227">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="f593a-227">O365ProPlusRetail</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f593a-228">Office 2013 com Visio 2013</span><span class="sxs-lookup"><span data-stu-id="f593a-228">Office 2013 with Visio 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f593a-229">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="f593a-229">ProPlusVolume</span></span></p>
<p><span data-ttu-id="f593a-230">VisioProVolume</span><span class="sxs-lookup"><span data-stu-id="f593a-230">VisioProVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="f593a-231">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="f593a-231">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="f593a-232">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="f593a-232">VisioProRetail</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f593a-233">Office 2013 com Visio 2013 e Project 2013</span><span class="sxs-lookup"><span data-stu-id="f593a-233">Office 2013 with Visio 2013 and Project 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f593a-234">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="f593a-234">ProPlusVolume</span></span></p>
<p><span data-ttu-id="f593a-235">VisioProVolume</span><span class="sxs-lookup"><span data-stu-id="f593a-235">VisioProVolume</span></span></p>
<p><span data-ttu-id="f593a-236">ProjectProVolume</span><span class="sxs-lookup"><span data-stu-id="f593a-236">ProjectProVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="f593a-237">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="f593a-237">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="f593a-238">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="f593a-238">VisioProRetail</span></span></p>
<p><span data-ttu-id="f593a-239">ProjectProRetail</span><span class="sxs-lookup"><span data-stu-id="f593a-239">ProjectProRetail</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="f593a-240">Como converter os aplicativos do Office em um pacote do App-V</span><span class="sxs-lookup"><span data-stu-id="f593a-240">How to convert the Office applications into an App-V package</span></span>**

1. <span data-ttu-id="f593a-241">No bloco de notas, abra novamente o arquivo CustomConfig.xml e faça as seguintes alterações no arquivo:</span><span class="sxs-lookup"><span data-stu-id="f593a-241">In Notepad, reopen the CustomConfig.xml file, and make the following changes to the file:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f593a-242">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="f593a-242">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="f593a-243">O que alterar o valor para</span><span class="sxs-lookup"><span data-stu-id="f593a-243">What to change the value to</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f593a-244">SourcePath</span><span class="sxs-lookup"><span data-stu-id="f593a-244">SourcePath</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f593a-245">Aponte para os aplicativos do Office baixados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f593a-245">Point to the Office applications downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f593a-246">ProductID</span><span class="sxs-lookup"><span data-stu-id="f593a-246">ProductID</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f593a-247">Especifique o tipo de licenciamento, conforme mostrado nos exemplos a seguir:</span><span class="sxs-lookup"><span data-stu-id="f593a-247">Specify the type of licensing, as shown in the following examples:</span></span></p>
   <ul>
   <li><p><span data-ttu-id="f593a-248">Licenciamento de assinatura</span><span class="sxs-lookup"><span data-stu-id="f593a-248">Subscription Licensing</span></span></p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\server\Office 2013&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;O365ProPlusRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt; </code></pre>
   <p><span data-ttu-id="f593a-249">Neste exemplo, foram feitas as seguintes alterações para criar um pacote com licenciamento de assinatura:</span><span class="sxs-lookup"><span data-stu-id="f593a-249">In this example, the following changes were made to create a package with Subscription licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f593a-250">SourcePath</span><span class="sxs-lookup"><span data-stu-id="f593a-250">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f593a-251">é o caminho, que foi alterado para apontar para os aplicativos do Office que foram baixados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f593a-251">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="f593a-252">ID do Produto (Product ID)</span><span class="sxs-lookup"><span data-stu-id="f593a-252">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f593a-253">para o Office foi alterado para <code>O365ProPlusRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="f593a-253">for Office was changed to <code>O365ProPlusRetail</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f593a-254">ID do Produto (Product ID)</span><span class="sxs-lookup"><span data-stu-id="f593a-254">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f593a-255">para o Visio foi alterado para <code>VisioProRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="f593a-255">for Visio was changed to <code>VisioProRetail</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p>
   <p></p></li>
   <li><p><span data-ttu-id="f593a-256">Licenciamento por volume</span><span class="sxs-lookup"><span data-stu-id="f593a-256">Volume Licensing</span></span></p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\Server\Office2013&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;ProPlusVolume&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProVolume&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt;</code></pre>
   <p><span data-ttu-id="f593a-257">Neste exemplo, foram feitas as seguintes alterações para criar um pacote com licenciamento por volume:</span><span class="sxs-lookup"><span data-stu-id="f593a-257">In this example, the following changes were made to create a package with Volume licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f593a-258">SourcePath</span><span class="sxs-lookup"><span data-stu-id="f593a-258">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f593a-259">é o caminho, que foi alterado para apontar para os aplicativos do Office que foram baixados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f593a-259">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="f593a-260">ID do Produto (Product ID)</span><span class="sxs-lookup"><span data-stu-id="f593a-260">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f593a-261">para o Office foi alterado para <code>ProPlusVolume</code> .</span><span class="sxs-lookup"><span data-stu-id="f593a-261">for Office was changed to <code>ProPlusVolume</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f593a-262">ID do Produto (Product ID)</span><span class="sxs-lookup"><span data-stu-id="f593a-262">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f593a-263">para o Visio foi alterado para <code>VisioProVolume</code> .</span><span class="sxs-lookup"><span data-stu-id="f593a-263">for Visio was changed to <code>VisioProVolume</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p>
   <p></p></li>
   </ul></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f593a-264">ExcludeApp (opcional)</span><span class="sxs-lookup"><span data-stu-id="f593a-264">ExcludeApp (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f593a-265">Permite especificar os programas do Office que você não deseja incluir no pacote do App-V que a ferramenta de implantação do Office cria.</span><span class="sxs-lookup"><span data-stu-id="f593a-265">Lets you specify Office programs that you don’t want included in the App-V package that the Office Deployment Tool creates.</span></span> <span data-ttu-id="f593a-266">Por exemplo, você pode excluir o Access e o InfoPath.</span><span class="sxs-lookup"><span data-stu-id="f593a-266">For example, you can exclude Access and InfoPath.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f593a-267">PACKAGEGUID (opcional)</span><span class="sxs-lookup"><span data-stu-id="f593a-267">PACKAGEGUID (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f593a-268">Por padrão, todos os pacotes do App-V criados pela ferramenta de implantação do Office compartilham a mesma ID de pacote do App-V.</span><span class="sxs-lookup"><span data-stu-id="f593a-268">By default, all App-V packages created by the Office Deployment Tool share the same App-V Package ID.</span></span> <span data-ttu-id="f593a-269">Você pode usar PACKAGEGUID para especificar uma ID de pacote diferente para cada pacote, que permite publicar vários pacotes do App-V, criados pela ferramenta de implantação do Office e gerenciá-los usando o servidor App-V.</span><span class="sxs-lookup"><span data-stu-id="f593a-269">You can use PACKAGEGUID to specify a different package ID for each package, which allows you to publish multiple App-V packages, created by the Office Deployment Tool, and manage them by using the App-V Server.</span></span></p>
   <p><span data-ttu-id="f593a-270">Um exemplo de quando usar esse parâmetro é se você cria pacotes diferentes para usuários diferentes.</span><span class="sxs-lookup"><span data-stu-id="f593a-270">An example of when to use this parameter is if you create different packages for different users.</span></span> <span data-ttu-id="f593a-271">Por exemplo, você pode criar um pacote com apenas o Office 2013 para alguns usuários e criar outro pacote com o Office 2013 e o Visio 2013 para outro conjunto de usuários.</span><span class="sxs-lookup"><span data-stu-id="f593a-271">For example, you can create a package with just Office 2013 for some users, and create another package with Office 2013 and Visio 2013 for another set of users.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="f593a-272">Observação</span><span class="sxs-lookup"><span data-stu-id="f593a-272">Note</span></span></strong><br/><p><span data-ttu-id="f593a-273">Mesmo que você use IDs de pacote exclusivas, ainda é possível implantar apenas um pacote do App-V para um único dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f593a-273">Even if you use unique package IDs, you can still deploy only one App-V package to a single device.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="f593a-274">Use o comando/Packager para converter os aplicativos do Office em um pacote do Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="f593a-274">Use the /packager command to convert the Office applications to an Office 2013 App-V package.</span></span>

   <span data-ttu-id="f593a-275">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f593a-275">For example:</span></span>

   ``` syntax
   \\server\Office2013\setup.exe /packager \\server\Office2013\Customconfig.xml  \\server\share\Office2013AppV
   ```

   <span data-ttu-id="f593a-276">No exemplo:</span><span class="sxs-lookup"><span data-stu-id="f593a-276">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f593a-277">\server\Office2013</span><span class="sxs-lookup"><span data-stu-id="f593a-277">\server\Office2013</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f593a-278">é o local de compartilhamento de rede que contém a ferramenta de implantação do Office e o arquivo de Configuration.xml personalizado Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="f593a-278">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="f593a-279">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="f593a-279">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f593a-280">é a ferramenta de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="f593a-280">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f593a-281">/packager</span><span class="sxs-lookup"><span data-stu-id="f593a-281">/packager</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f593a-282">cria o pacote do Office 2013 App-V com licenciamento por volume conforme especificado no arquivo customConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="f593a-282">creates the Office 2013 App-V package with Volume Licensing as specified in the customConfig.xml file.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="f593a-283">\server\Office2013\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="f593a-283">\server\Office2013\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f593a-284">passa o arquivo XML de configuração (neste caso, customConfig) que foi preparado para o estágio de empacotamento.</span><span class="sxs-lookup"><span data-stu-id="f593a-284">passes the configuration XML file (in this case customConfig) that has been prepared for the packaging stage.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f593a-285">\server\share\Office 2013AppV</span><span class="sxs-lookup"><span data-stu-id="f593a-285">\server\share\Office 2013AppV</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f593a-286">Especifica o local do pacote do Office App-V recém-criado.</span><span class="sxs-lookup"><span data-stu-id="f593a-286">specifies the location of the newly created Office App-V package.</span></span></p></td>
   </tr>
   </tbody>
   </table>



~~~
After you run the **/packager** command, the following folders appear up in the directory where you specified the package should be saved:

-   **App-V Packages** – contains an Office 2013 App-V package and two deployment configuration files.

-   **WorkingDir**

**Note**  
To troubleshoot any issues, see the log files in the %temp% directory (default).
~~~



3. <span data-ttu-id="f593a-287">Verifique se o pacote do Office 2013 App-V funciona corretamente:</span><span class="sxs-lookup"><span data-stu-id="f593a-287">Verify that the Office 2013 App-V package works correctly:</span></span>

   1.  <span data-ttu-id="f593a-288">Publique o pacote do Office 2013 App-V, que você criou globalmente, em um computador de teste e verifique se os atalhos do Office 2013 são exibidos.</span><span class="sxs-lookup"><span data-stu-id="f593a-288">Publish the Office 2013 App-V package, which you created globally, to a test computer, and verify that the Office 2013 shortcuts appear.</span></span>

   2.  <span data-ttu-id="f593a-289">Inicie alguns aplicativos do Office 2013, como o Excel ou o Word, para garantir que o pacote esteja funcionando conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="f593a-289">Start a few Office 2013 applications, such as Excel or Word, to ensure that your package is working as expected.</span></span>

## <a href="" id="bkmk-pub-pkg-office"></a><span data-ttu-id="f593a-290">Publicando o pacote do Office para o App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="f593a-290">Publishing the Office package for App-V 5.1</span></span>


<span data-ttu-id="f593a-291">Use as informações a seguir para publicar um pacote do Office.</span><span class="sxs-lookup"><span data-stu-id="f593a-291">Use the following information to publish an Office package.</span></span>

### <span data-ttu-id="f593a-292">Métodos para publicar pacotes do Office App-V</span><span class="sxs-lookup"><span data-stu-id="f593a-292">Methods for publishing Office App-V packages</span></span>

<span data-ttu-id="f593a-293">Implante o pacote do App-V para o Office 2013 usando os mesmos métodos que você usa para qualquer outro pacote:</span><span class="sxs-lookup"><span data-stu-id="f593a-293">Deploy the App-V package for Office 2013 by using the same methods you use for any other package:</span></span>

-   <span data-ttu-id="f593a-294">System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f593a-294">System Center Configuration Manager</span></span>

-   <span data-ttu-id="f593a-295">Servidor do App-V</span><span class="sxs-lookup"><span data-stu-id="f593a-295">App-V Server</span></span>

-   <span data-ttu-id="f593a-296">Autônomos por meio de comandos do PowerShell</span><span class="sxs-lookup"><span data-stu-id="f593a-296">Stand-alone through PowerShell commands</span></span>

### <span data-ttu-id="f593a-297">Como publicar pré-requisitos e requisitos</span><span class="sxs-lookup"><span data-stu-id="f593a-297">Publishing prerequisites and requirements</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f593a-298">Pré-requisito ou requisito</span><span class="sxs-lookup"><span data-stu-id="f593a-298">Prerequisite or requirement</span></span></th>
<th align="left"><span data-ttu-id="f593a-299">Detalhes</span><span class="sxs-lookup"><span data-stu-id="f593a-299">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f593a-300">Habilitar o script do PowerShell nos clientes do App-V</span><span class="sxs-lookup"><span data-stu-id="f593a-300">Enable PowerShell scripting on the App-V clients</span></span></p></td>
<td align="left"><p><span data-ttu-id="f593a-301">Para publicar pacotes do Office 2013, você deve executar um script.</span><span class="sxs-lookup"><span data-stu-id="f593a-301">To publish Office 2013 packages, you must run a script.</span></span></p>
<p><span data-ttu-id="f593a-302">Os scripts de pacote são desativados por padrão em clientes App-V.</span><span class="sxs-lookup"><span data-stu-id="f593a-302">Package scripts are disabled by default on App-V clients.</span></span> <span data-ttu-id="f593a-303">Para habilitar o script, execute o seguinte comando do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="f593a-303">To enable scripting, run the following PowerShell command:</span></span></p>
<pre class="syntax" space="preserve"><code>Set-AppvClientConfiguration –EnablePackageScripts 1</code></pre></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f593a-304">Publicar o pacote do Office 2013 globalmente</span><span class="sxs-lookup"><span data-stu-id="f593a-304">Publish the Office 2013 package globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="f593a-305">Os pontos de extensão no pacote App-V do Office exigem instalação no nível do computador.</span><span class="sxs-lookup"><span data-stu-id="f593a-305">Extension points in the Office App-V package require installation at the computer level.</span></span></p>
<p><span data-ttu-id="f593a-306">Quando você publica no nível do computador, não são necessárias ações de pré-requisito ou redistribuíveis, e o pacote do Office 2013 permite que seus aplicativos funcionem como o Office instalado nativamente, eliminando a necessidade de os administradores personalizarem pacotes.</span><span class="sxs-lookup"><span data-stu-id="f593a-306">When you publish at the computer level, no prerequisite actions or redistributables are needed, and the Office 2013 package globally enables its applications to work like natively installed Office, eliminating the need for administrators to customize packages.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="f593a-307">Como publicar um pacote do Office</span><span class="sxs-lookup"><span data-stu-id="f593a-307">How to publish an Office package</span></span>

<span data-ttu-id="f593a-308">Execute o seguinte comando para publicar um pacote do Office globalmente:</span><span class="sxs-lookup"><span data-stu-id="f593a-308">Run the following command to publish an Office package globally:</span></span>

-   `Add-AppvClientPackage <Path_to_AppV_Package> | Publish-AppvClientPackage –global`

-   <span data-ttu-id="f593a-309">No console de gerenciamento da Web no App-V Server, você pode adicionar permissões a um grupo de computadores em vez de a um grupo de usuários para permitir que os pacotes sejam publicados globalmente nos computadores do grupo correspondente.</span><span class="sxs-lookup"><span data-stu-id="f593a-309">From the Web Management Console on the App-V Server, you can add permissions to a group of computers instead of to a user group to enable packages to be published globally to the computers in the corresponding group.</span></span>

## <a href="" id="bkmk-custmz-manage-office-pkgs"></a><span data-ttu-id="f593a-310">Personalizando e gerenciando pacotes do Office App-V</span><span class="sxs-lookup"><span data-stu-id="f593a-310">Customizing and managing Office App-V packages</span></span>


<span data-ttu-id="f593a-311">Para gerenciar seus pacotes do Office App-V, use as mesmas operações que faria para qualquer outro pacote, mas há algumas exceções, como descrito nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="f593a-311">To manage your Office App-V packages, use the same operations as you would for any other package, but there are a few exceptions, as outlined in the following sections.</span></span>

-   [<span data-ttu-id="f593a-312">Habilitando plug-ins do Office usando grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="f593a-312">Enabling Office plug-ins by using connection groups</span></span>](#bkmk-enable-office-plugins)

-   [<span data-ttu-id="f593a-313">Desativando aplicativos do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f593a-313">Disabling Office 2013 applications</span></span>](#bkmk-disable-office-apps)

-   [<span data-ttu-id="f593a-314">Desativando atalhos do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f593a-314">Disabling Office 2013 shortcuts</span></span>](#bkmk-disable-shortcuts)

-   [<span data-ttu-id="f593a-315">Gerenciando atualizações de pacote do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f593a-315">Managing Office 2013 package upgrades</span></span>](#bkmk-manage-office-pkg-upgrd)

-   [<span data-ttu-id="f593a-316">Gerenciando atualizações de licenciamento do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f593a-316">Managing Office 2013 licensing upgrades</span></span>](#bkmk-manage-office-lic-upgrd)

-   [<span data-ttu-id="f593a-317">Implantação do Visio 2013 e do Project 2013 com o Office</span><span class="sxs-lookup"><span data-stu-id="f593a-317">Deploying Visio 2013 and Project 2013 with Office</span></span>](#bkmk-deploy-visio-project)

### <a href="" id="bkmk-enable-office-plugins"></a><span data-ttu-id="f593a-318">Habilitando plug-ins do Office usando grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="f593a-318">Enabling Office plug-ins by using connection groups</span></span>

<span data-ttu-id="f593a-319">Use as etapas desta seção para habilitar os plug-ins do Office com o pacote do Office.</span><span class="sxs-lookup"><span data-stu-id="f593a-319">Use the steps in this section to enable Office plug-ins with your Office package.</span></span> <span data-ttu-id="f593a-320">Para usar os plug-ins do Office, você deve usar o sequenciador do App-V para criar um pacote separado que contenha apenas os plug-ins. Não é possível usar a ferramenta de implantação do Office para criar o pacote de plug-ins.</span><span class="sxs-lookup"><span data-stu-id="f593a-320">To use Office plug-ins, you must use the App-V Sequencer to create a separate package that contains just the plug-ins. You cannot use the Office Deployment Tool to create the plug-ins package.</span></span> <span data-ttu-id="f593a-321">Em seguida, crie um grupo de conexão que contenha o pacote de plug-ins e o pacote do Office, conforme descrito nas etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="f593a-321">You then create a connection group that contains the Office package and the plug-ins package, as described in the following steps.</span></span>

**<span data-ttu-id="f593a-322">Para habilitar plug-ins para pacotes do Office App-V</span><span class="sxs-lookup"><span data-stu-id="f593a-322">To enable plug-ins for Office App-V packages</span></span>**

1.  <span data-ttu-id="f593a-323">Adicione um grupo de conexão por meio do App-V Server, do System Center Configuration Manager ou de um cmdlet do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f593a-323">Add a Connection Group through App-V Server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

2.  <span data-ttu-id="f593a-324">Sequenciar seus plug-ins usando o sequenciador do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="f593a-324">Sequence your plug-ins using the App-V 5.1 Sequencer.</span></span> <span data-ttu-id="f593a-325">Verifique se o Office 2013 está instalado no computador que está sendo usado para sequenciar o plug-in.</span><span class="sxs-lookup"><span data-stu-id="f593a-325">Ensure that Office 2013 is installed on the computer being used to sequence the plug-in.</span></span> <span data-ttu-id="f593a-326">É recomendável usar os aplicativos do Microsoft 365 para empresas (não virtuais) no computador de sequenciamento quando você sequenciar plug-ins do Office 2013.</span><span class="sxs-lookup"><span data-stu-id="f593a-326">It is recommended you use Microsoft 365 Apps for enterprise(non-virtual) on the sequencing computer when you sequence Office 2013 plug-ins.</span></span>

3.  <span data-ttu-id="f593a-327">Crie um pacote do App-V 5,1 que inclua os plug-ins desejados.</span><span class="sxs-lookup"><span data-stu-id="f593a-327">Create an App-V 5.1 package that includes the desired plug-ins.</span></span>

4.  <span data-ttu-id="f593a-328">Adicione um grupo de conexão por meio do App-V Server, do System Center Configuration Manager ou de um cmdlet do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f593a-328">Add a Connection Group through App-V server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

5.  <span data-ttu-id="f593a-329">Adicione o pacote do Office 2013 App-V e o pacote de plug-ins que você sequenciaou ao grupo de conexão que você criou.</span><span class="sxs-lookup"><span data-stu-id="f593a-329">Add the Office 2013 App-V package and the plug-ins package you sequenced to the Connection Group you created.</span></span>

    **<span data-ttu-id="f593a-330">Importante</span><span class="sxs-lookup"><span data-stu-id="f593a-330">Important</span></span>**  
    <span data-ttu-id="f593a-331">A ordem dos pacotes no grupo de conexão determina a ordem em que o conteúdo do pacote é mesclado.</span><span class="sxs-lookup"><span data-stu-id="f593a-331">The order of the packages in the Connection Group determines the order in which the package contents are merged.</span></span> <span data-ttu-id="f593a-332">No arquivo do descritor de grupo de conexão, adicione o pacote do Office 2013 App-V primeiro e, em seguida, adicione o pacote do plug-in App-V.</span><span class="sxs-lookup"><span data-stu-id="f593a-332">In your Connection group descriptor file, add the Office 2013 App-V package first, and then add the plug-in App-V package.</span></span>



6.  <span data-ttu-id="f593a-333">Certifique-se de que os dois pacotes sejam publicados no computador de destino e que o pacote de plug-in seja publicado globalmente para corresponder às configurações globais do pacote do Office 2013 App-V publicado.</span><span class="sxs-lookup"><span data-stu-id="f593a-333">Ensure that both packages are published to the target computer and that the plug-in package is published globally to match the global settings of the published Office 2013 App-V package.</span></span>

7.  <span data-ttu-id="f593a-334">Verifique se o arquivo de configuração de implantação do pacote de plug-in tem as mesmas configurações que o pacote do Office 2013 App-V tem.</span><span class="sxs-lookup"><span data-stu-id="f593a-334">Verify that the Deployment Configuration File of the plug-in package has the same settings that the Office 2013 App-V package has.</span></span>

    <span data-ttu-id="f593a-335">Como o pacote do Office 2013 App-V está integrado ao sistema operacional, as configurações do pacote de plug-in devem coincidir.</span><span class="sxs-lookup"><span data-stu-id="f593a-335">Since the Office 2013 App-V package is integrated with the operating system, the plug-in package settings should match.</span></span> <span data-ttu-id="f593a-336">Você pode pesquisar o arquivo de configuração de implantação para "modo COM" e garantir que o pacote de plug-ins tenha esse valor definido como "integrado" e que "InProcessEnabled" e "OutOfProcessEnabled" correspondam às configurações do pacote do Office 2013 App-V que você publicou.</span><span class="sxs-lookup"><span data-stu-id="f593a-336">You can search the Deployment Configuration File for “COM Mode” and ensure that your plug-ins package has that value set as “Integrated” and that both "InProcessEnabled" and "OutOfProcessEnabled" match the settings of the Office 2013 App-V package you published.</span></span>

8.  <span data-ttu-id="f593a-337">Abra o arquivo de configuração de implantação e defina o valor de **objetos habilitados** como **falso**.</span><span class="sxs-lookup"><span data-stu-id="f593a-337">Open the Deployment Configuration File and set the value for **Objects Enabled** to **false**.</span></span>

9.  <span data-ttu-id="f593a-338">Se você fez qualquer alteração no arquivo de configuração de implantação após o sequenciamento, verifique se o pacote de plug-in é publicado com o arquivo.</span><span class="sxs-lookup"><span data-stu-id="f593a-338">If you made any changes to the Deployment Configuration file after sequencing, ensure that the plug-in package is published with the file.</span></span>

10. <span data-ttu-id="f593a-339">Verifique se o grupo de conexão que você criou está habilitado no computador desejado.</span><span class="sxs-lookup"><span data-stu-id="f593a-339">Ensure that the Connection Group you created is enabled onto your desired computer.</span></span> <span data-ttu-id="f593a-340">O grupo de conexão criado provavelmente será "pendente" se o pacote do Office 2013 App-V estiver em uso quando o grupo de conexão estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="f593a-340">The Connection Group created will likely “pend” if the Office 2013 App-V package is in use when the Connection Group is enabled.</span></span> <span data-ttu-id="f593a-341">Se isso acontecer, será necessário reinicializar para habilitar o grupo de conexão com êxito.</span><span class="sxs-lookup"><span data-stu-id="f593a-341">If that happens, you have to reboot to successfully enable the Connection Group.</span></span>

11. <span data-ttu-id="f593a-342">Depois de publicar com êxito os dois pacotes e habilitar o grupo de conexão, inicie o aplicativo de destino do Office 2013 e verifique se o plug-in que você publicou e adicionado ao grupo de conexão funciona como esperado.</span><span class="sxs-lookup"><span data-stu-id="f593a-342">After you successfully publish both packages and enable the Connection Group, start the target Office 2013 application and verify that the plug-in you published and added to the connection group works as expected.</span></span>

### <a href="" id="bkmk-disable-office-apps"></a><span data-ttu-id="f593a-343">Desativando aplicativos do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f593a-343">Disabling Office 2013 applications</span></span>

<span data-ttu-id="f593a-344">Você pode querer desabilitar aplicativos específicos em seu pacote do Office App-V.</span><span class="sxs-lookup"><span data-stu-id="f593a-344">You may want to disable specific applications in your Office App-V package.</span></span> <span data-ttu-id="f593a-345">Por exemplo, você pode desabilitar o Access, mas deixar todos os outros aplicativos principais do Office disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f593a-345">For instance, you can disable Access, but leave all other Office application main available.</span></span> <span data-ttu-id="f593a-346">Quando você desabilitar um aplicativo, o usuário final não verá mais o atalho para esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f593a-346">When you disable an application, the end user will no longer see the shortcut for that application.</span></span> <span data-ttu-id="f593a-347">Não é necessário sequenciar novamente o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f593a-347">You do not have to re-sequence the application.</span></span> <span data-ttu-id="f593a-348">Quando você altera o arquivo de configuração de implantação após a publicação do pacote do Office 2013 App-V, você salvará as alterações, adicionará o pacote do Office 2013 app-v e a publicará novamente com o novo arquivo de configuração de implantação para aplicar as novas configurações aos aplicativos do pacote do Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="f593a-348">When you change the Deployment Configuration File after the Office 2013 App-V package has been published, you will save the changes, add the Office 2013 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2013 App-V Package applications.</span></span>

**<span data-ttu-id="f593a-349">Observação</span><span class="sxs-lookup"><span data-stu-id="f593a-349">Note</span></span>**  
<span data-ttu-id="f593a-350">Para excluir aplicativos específicos do Office (por exemplo, o Access e o InfoPath) quando você cria o pacote do App-V com a ferramenta de implantação do Office, use a configuração **ExcludeApp** .</span><span class="sxs-lookup"><span data-stu-id="f593a-350">To exclude specific Office applications (for example, Access and InfoPath) when you create the App-V package with the Office Deployment Tool, use the **ExcludeApp** setting.</span></span> <span data-ttu-id="f593a-351">Para obter mais informações, consulte [referência para o arquivo de configuration.xml clique para executar](https://technet.microsoft.com/library/jj219426.aspx).</span><span class="sxs-lookup"><span data-stu-id="f593a-351">For more information, see [Reference for Click-to-Run configuration.xml file](https://technet.microsoft.com/library/jj219426.aspx).</span></span>



**<span data-ttu-id="f593a-352">Para desabilitar um aplicativo do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f593a-352">To disable an Office 2013 application</span></span>**

1.  <span data-ttu-id="f593a-353">Abra um arquivo de configuração de implantação com um editor de texto, como o **bloco de notas** , e procure por "aplicativos".</span><span class="sxs-lookup"><span data-stu-id="f593a-353">Open a Deployment Configuration File with a text editor such as **Notepad** and search for “Applications."</span></span>

2.  <span data-ttu-id="f593a-354">Procure o aplicativo do Office que você deseja desabilitar, por exemplo, Access 2013.</span><span class="sxs-lookup"><span data-stu-id="f593a-354">Search for the Office application you want to disable, for example, Access 2013.</span></span>

3.  <span data-ttu-id="f593a-355">Altere o valor de "Enabled" de "true" para "false".</span><span class="sxs-lookup"><span data-stu-id="f593a-355">Change the value of "Enabled" from "true" to "false."</span></span>

4.  <span data-ttu-id="f593a-356">Salve o arquivo de configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="f593a-356">Save the Deployment Configuration File.</span></span>

5.  <span data-ttu-id="f593a-357">Adicione o pacote do Office 2013 App-V com o novo arquivo de configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="f593a-357">Add the Office 2013 App-V Package with the new Deployment Configuration File.</span></span>

    ```xml
    <Application Id="[{AppVPackageRoot)]\officefl5\INFOPATH.EXE" Enabled="true">
      <VisualElements>
        <Name>InfoPath Filler 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[{AppVPackageRoot}]\office15\lync.exe" Enabled="true">
      <VisualElements>
        <Name>Lync 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[(AppVPackageRoot}]\office15\MSACCESS.EXE" Enabled="true">
      <VisualElements>
        <Name>Access 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    ```

6.  <span data-ttu-id="f593a-358">Adicione novamente o pacote do Office 2013 App-V e Republique-o com o novo arquivo de configuração de implantação para aplicar as novas configurações aos aplicativos do pacote do App-V do Office 2013.</span><span class="sxs-lookup"><span data-stu-id="f593a-358">Re-add the Office 2013 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2013 App-V Package applications.</span></span>

### <a href="" id="bkmk-disable-shortcuts"></a><span data-ttu-id="f593a-359">Desativando atalhos do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f593a-359">Disabling Office 2013 shortcuts</span></span>

<span data-ttu-id="f593a-360">Você pode querer desativar atalhos para determinados aplicativos do Office em vez de cancelar a publicação ou remoção do pacote.</span><span class="sxs-lookup"><span data-stu-id="f593a-360">You may want to disable shortcuts for certain Office applications instead of unpublishing or removing the package.</span></span> <span data-ttu-id="f593a-361">O exemplo a seguir mostra como desabilitar atalhos para o Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f593a-361">The following example shows how to disable shortcuts for Microsoft Access.</span></span>

**<span data-ttu-id="f593a-362">Para desativar atalhos para aplicativos do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f593a-362">To disable shortcuts for Office 2013 applications</span></span>**

1.  <span data-ttu-id="f593a-363">Abra um arquivo de configuração de implantação no bloco de notas e procure por "atalhos".</span><span class="sxs-lookup"><span data-stu-id="f593a-363">Open a Deployment Configuration File in Notepad and search for “Shortcuts”.</span></span>

2.  <span data-ttu-id="f593a-364">Para desabilitar certos atalhos, exclua ou comente os atalhos específicos que você não quer.</span><span class="sxs-lookup"><span data-stu-id="f593a-364">To disable certain shortcuts, delete or comment out the specific shortcuts you don’t want.</span></span> <span data-ttu-id="f593a-365">Você deve manter o subsistema presente e habilitado.</span><span class="sxs-lookup"><span data-stu-id="f593a-365">You must keep the subsystem present and enabled.</span></span> <span data-ttu-id="f593a-366">Por exemplo, no exemplo a seguir, exclua os atalhos do Microsoft Access, enquanto mantém os subsistemas de &lt; atalho &gt; &lt; /Shortcut &gt; intactos para desabilitar o atalho do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f593a-366">For example, in the example below, delete the Microsoft Access shortcuts, while keeping the subsystems &lt;shortcut&gt; &lt;/shortcut&gt; intact to disable the Microsoft Access shortcut.</span></span>

    ``` syntax
    Shortcuts

    -->
     <Shortcuts Enabled="true">
      <Extensions>
        <Extension Category="AppV.Shortcut">
          <Shortcut>
           <File>[{Common Programs}]\Microsoft Office 2013\Access 2013.lnk</File>
           <Target>[{AppvPackageRoot}])office15\MSACCESS.EXE</Target>
           <Icon>[{Windows}]\Installer\{90150000-000F-0000-0000-000000FF1CE)\accicons.exe.Ø.ico</Icon>
           <Arguments />
           <WorkingDirectory />
           <AppuserModelId>Microsoft.Office.MSACCESS.EXE.15</AppUserModelId>
           <AppUserModelExcludeFromShowInNewInstall>true</AppUserModelExcludeFromShowInNewInstall>
           <Description>Build a professional app quickly to manage data.</Description>
           <ShowCommand>l</ShowCommand>
           <ApplicationId>[{AppVPackageRoot}]\office15\MSACCESS.EXE</ApplicationId>
        </Shortcut>
    ```

3.  <span data-ttu-id="f593a-367">Salve o arquivo de configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="f593a-367">Save the Deployment Configuration File.</span></span>

4.  <span data-ttu-id="f593a-368">Republicar o pacote do Office 2013 App-V com novo arquivo de configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="f593a-368">Republish Office 2013 App-V Package with new Deployment Configuration File.</span></span>

<span data-ttu-id="f593a-369">Muitas configurações adicionais podem ser alteradas por meio da modificação da configuração de implantação para pacotes do App-V, por exemplo, associações de tipo de arquivo, sistema de arquivos virtual e muito mais.</span><span class="sxs-lookup"><span data-stu-id="f593a-369">Many additional settings can be changed through modifying the Deployment Configuration for App-V packages, for example, file type associations, Virtual File System, and more.</span></span> <span data-ttu-id="f593a-370">Para obter informações adicionais sobre como usar arquivos de configuração de implantação para alterar as configurações do pacote do App-V, consulte a seção recursos adicionais no final deste documento.</span><span class="sxs-lookup"><span data-stu-id="f593a-370">For additional information on how to use Deployment Configuration Files to change App-V package settings, refer to the additional resources section at the end of this document.</span></span>

### <a href="" id="bkmk-manage-office-pkg-upgrd"></a><span data-ttu-id="f593a-371">Gerenciando atualizações de pacote do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f593a-371">Managing Office 2013 package upgrades</span></span>

<span data-ttu-id="f593a-372">Para atualizar um pacote do Office 2013, use a ferramenta de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="f593a-372">To upgrade an Office 2013 package, use the Office Deployment Tool.</span></span> <span data-ttu-id="f593a-373">Para atualizar um pacote do Office 2013 implantado anteriormente, siga as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="f593a-373">To upgrade a previously deployed Office 2013 package, perform the following steps.</span></span>

**<span data-ttu-id="f593a-374">Como atualizar um pacote do Office 2013 implantado anteriormente</span><span class="sxs-lookup"><span data-stu-id="f593a-374">How to upgrade a previously deployed Office 2013 package</span></span>**

1.  <span data-ttu-id="f593a-375">Crie um novo pacote do Office 2013 por meio da ferramenta de implantação do Office que usa o software aplicativo mais recente do Office 2013.</span><span class="sxs-lookup"><span data-stu-id="f593a-375">Create a new Office 2013 package through the Office Deployment Tool that uses the most recent Office 2013 application software.</span></span> <span data-ttu-id="f593a-376">Os bits mais recentes do Office 2013 sempre podem ser obtidos por meio do estágio de download da criação de um pacote do Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="f593a-376">The most recent Office 2013 bits can always be obtained through the download stage of creating an Office 2013 App-V Package.</span></span> <span data-ttu-id="f593a-377">O pacote do Office 2013 recém-criado terá as atualizações mais recentes e uma nova ID de versão.</span><span class="sxs-lookup"><span data-stu-id="f593a-377">The newly created Office 2013 package will have the most recent updates and a new Version ID.</span></span> <span data-ttu-id="f593a-378">Todos os pacotes criados usando a ferramenta de implantação do Office têm a mesma linhagem.</span><span class="sxs-lookup"><span data-stu-id="f593a-378">All packages created using the Office Deployment Tool have the same lineage.</span></span>

    **<span data-ttu-id="f593a-379">Observação</span><span class="sxs-lookup"><span data-stu-id="f593a-379">Note</span></span>**  
    <span data-ttu-id="f593a-380">Os pacotes do Office App-V têm duas IDs de versão:</span><span class="sxs-lookup"><span data-stu-id="f593a-380">Office App-V packages have two Version IDs:</span></span>

    -   <span data-ttu-id="f593a-381">Uma ID de versão do pacote do Office 2013 App-V que é exclusiva em todos os pacotes criados usando a ferramenta de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="f593a-381">An Office 2013 App-V Package Version ID that is unique across all packages created using the Office Deployment Tool.</span></span>

    -   <span data-ttu-id="f593a-382">Uma segunda ID de versão do pacote do App-V, x. x. x. x por exemplo, no manifesto AppX que só será alterado se houver uma nova versão do Office.</span><span class="sxs-lookup"><span data-stu-id="f593a-382">A second App-V Package Version ID, x.x.x.x for example, in the AppX manifest that will only change if there is a new version of Office itself.</span></span> <span data-ttu-id="f593a-383">Por exemplo, se uma nova versão do Office 2013 com atualizações estiver disponível e um pacote for criado por meio da ferramenta de implantação do Office para incorporar essas atualizações, a ID da versão X. x. x. X será alterada para refletir que a própria versão do Office mudou.</span><span class="sxs-lookup"><span data-stu-id="f593a-383">For example, if a new Office 2013 release with upgrades is available, and a package is created through the Office Deployment Tool to incorporate these upgrades, the X.X.X.X version ID will change to reflect that the Office version itself has changed.</span></span> <span data-ttu-id="f593a-384">O servidor App-V usará a ID da versão x. x. x para diferenciar esse pacote e reconhecer que ele contém novas atualizações para o pacote publicado anteriormente e, como resultado, publicá-lo como uma atualização para o pacote existente do Office 2013.</span><span class="sxs-lookup"><span data-stu-id="f593a-384">The App-V server will use the X.X.X.X version ID to differentiate this package and recognize that it contains new upgrades to the previously published package, and as a result, publish it as an upgrade to the existing Office 2013 package.</span></span>



2.  <span data-ttu-id="f593a-385">Publique globalmente os pacotes do Office 2013 App-V recém-criados em computadores onde você deseja aplicar as novas atualizações.</span><span class="sxs-lookup"><span data-stu-id="f593a-385">Globally publish the newly created Office 2013 App-V Packages onto computers where you would like to apply the new updates.</span></span> <span data-ttu-id="f593a-386">Como o novo pacote tem a mesma linhagem do pacote mais antigo do Office 2013 App-V, publicar o novo pacote com as atualizações só aplicará as novas alterações ao pacote antigo e, portanto, será rápido.</span><span class="sxs-lookup"><span data-stu-id="f593a-386">Since the new package has the same lineage of the older Office 2013 App-V Package, publishing the new package with the updates will only apply the new changes to the old package, and thus will be fast.</span></span>

3.  <span data-ttu-id="f593a-387">As atualizações serão aplicadas da mesma maneira em qualquer pacote App-V publicado globalmente.</span><span class="sxs-lookup"><span data-stu-id="f593a-387">Upgrades will be applied in the same manner of any globally published App-V Packages.</span></span> <span data-ttu-id="f593a-388">Como os aplicativos provavelmente estarão em uso, as atualizações podem ser adiadas até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="f593a-388">Because applications will probably be in use, upgrades might be delayed until the computer is rebooted.</span></span>

### <a href="" id="bkmk-manage-office-lic-upgrd"></a><span data-ttu-id="f593a-389">Gerenciando atualizações de licenciamento do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f593a-389">Managing Office 2013 licensing upgrades</span></span>

<span data-ttu-id="f593a-390">Se um novo pacote do Office 2013 App-V tiver uma licença diferente do pacote do Office 2013 App-V implantado no momento.</span><span class="sxs-lookup"><span data-stu-id="f593a-390">If a new Office 2013 App-V Package has a different license than the Office 2013 App-V Package currently deployed.</span></span> <span data-ttu-id="f593a-391">Por exemplo, o pacote do Office 2013 implantado é uma assinatura do Office 2013 e o novo pacote do Office 2013 é baseado em licenciamento por volume, as instruções a seguir devem ser seguidas para garantir uma atualização de licenciamento suave:</span><span class="sxs-lookup"><span data-stu-id="f593a-391">For instance, the Office 2013 package deployed is a subscription based Office 2013 and the new Office 2013 package is Volume Licensing based, the following instructions must be followed to ensure smooth licensing upgrade:</span></span>

**<span data-ttu-id="f593a-392">Como atualizar uma licença do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f593a-392">How to upgrade an Office 2013 License</span></span>**

1.  <span data-ttu-id="f593a-393">Cancele a publicação do pacote App-V de licenciamento de assinatura do Office 2013 já implementado.</span><span class="sxs-lookup"><span data-stu-id="f593a-393">Unpublish the already deployed Office 2013 Subscription Licensing App-V package.</span></span>

2.  <span data-ttu-id="f593a-394">Remova o pacote App-V de licenciamento de assinatura do Office 2013 cancelado.</span><span class="sxs-lookup"><span data-stu-id="f593a-394">Remove the unpublished Office 2013 Subscription Licensing App-V package.</span></span>

3.  <span data-ttu-id="f593a-395">Reinicie o computador.</span><span class="sxs-lookup"><span data-stu-id="f593a-395">Restart the computer.</span></span>

4.  <span data-ttu-id="f593a-396">Adicione o novo licenciamento de volume do pacote do Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="f593a-396">Add the new Office 2013 App-V Package Volume Licensing.</span></span>

5.  <span data-ttu-id="f593a-397">Publicar o pacote do Office 2013 App-V adicionado com licenciamento por volume.</span><span class="sxs-lookup"><span data-stu-id="f593a-397">Publish the added Office 2013 App-V Package with Volume Licensing.</span></span>

<span data-ttu-id="f593a-398">Um pacote do Office 2013 App-V com seu licenciamento escolhido será implantado com êxito.</span><span class="sxs-lookup"><span data-stu-id="f593a-398">An Office 2013 App-V Package with your chosen licensing will be successfully deployed.</span></span>

### <a href="" id="bkmk-deploy-visio-project"></a><span data-ttu-id="f593a-399">Implantação do Visio 2013 e do Project 2013 com o Office</span><span class="sxs-lookup"><span data-stu-id="f593a-399">Deploying Visio 2013 and Project 2013 with Office</span></span>

<span data-ttu-id="f593a-400">A tabela a seguir descreve os requisitos e as opções para a implantação do Visio 2013 e do Project 2013 com o Office.</span><span class="sxs-lookup"><span data-stu-id="f593a-400">The following table describes the requirements and options for deploying Visio 2013 and Project 2013 with Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f593a-401">Tarefa</span><span class="sxs-lookup"><span data-stu-id="f593a-401">Task</span></span></th>
<th align="left"><span data-ttu-id="f593a-402">Detalhes</span><span class="sxs-lookup"><span data-stu-id="f593a-402">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f593a-403">Como faço para empacotar e publicar o Visio 2013 e o Project 2013 com o Office?</span><span class="sxs-lookup"><span data-stu-id="f593a-403">How do I package and publish Visio 2013 and Project 2013 with Office?</span></span></p></td>
<td align="left"><p><span data-ttu-id="f593a-404">Você deve incluir o Visio 2013 e o Project 2013 no mesmo pacote com o Office.</span><span class="sxs-lookup"><span data-stu-id="f593a-404">You must include Visio 2013 and Project 2013 in the same package with Office.</span></span></p>
<p><span data-ttu-id="f593a-405">Se você não estiver implantando o Office, poderá criar um pacote que contenha o Visio e/ou Project, desde que siga a <a href="../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md" data-raw-source="[Deploying Microsoft Office 2010 by Using App-V](../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md)"> implantação do Microsoft Office 2010 usando o App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="f593a-405">If you aren’t deploying Office, you can create a package that contains Visio and/or Project, as long as you follow <a href="../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md" data-raw-source="[Deploying Microsoft Office 2010 by Using App-V](../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md)">Deploying Microsoft Office 2010 by Using App-V</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f593a-406">Como eu posso implantar o Visio 2013 e o Project 2013 para usuários específicos?</span><span class="sxs-lookup"><span data-stu-id="f593a-406">How can I deploy Visio 2013 and Project 2013 to specific users?</span></span></p></td>
<td align="left"><p><span data-ttu-id="f593a-407">Use um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="f593a-407">Use one of the following methods:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f593a-408">Se quiser...</span><span class="sxs-lookup"><span data-stu-id="f593a-408">If you want to...</span></span></th>
<th align="left"><span data-ttu-id="f593a-409">... em seguida, use esse método</span><span class="sxs-lookup"><span data-stu-id="f593a-409">...then use this method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f593a-410">Crie dois pacotes diferentes e implante cada um deles em um grupo diferente de usuários</span><span class="sxs-lookup"><span data-stu-id="f593a-410">Create two different packages and deploy each one to a different group of users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f593a-411">Crie e implante os seguintes pacotes:</span><span class="sxs-lookup"><span data-stu-id="f593a-411">Create and deploy the following packages:</span></span></p>
<ul>
<li><p><span data-ttu-id="f593a-412">Um pacote que contém apenas o Office-implantação em computadores cujos usuários precisam apenas do Office.</span><span class="sxs-lookup"><span data-stu-id="f593a-412">A package that contains only Office - deploy to computers whose users need only Office.</span></span></p></li>
<li><p><span data-ttu-id="f593a-413">Um pacote que contém o Office, o Visio e o Project-implantação para computadores cujos usuários precisam de todos os três aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f593a-413">A package that contains Office, Visio, and Project - deploy to computers whose users need all three applications.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f593a-414">Se você quiser apenas um pacote para a organização inteira, ou se tiver usuários que compartilham computadores:</span><span class="sxs-lookup"><span data-stu-id="f593a-414">If you want only one package for the whole organization, or if you have users who share computers:</span></span></p></td>
<td align="left"><p><span data-ttu-id="f593a-415">Siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="f593a-415">Follows these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="f593a-416">Crie um pacote que contenha o Office, o Visio e o Project.</span><span class="sxs-lookup"><span data-stu-id="f593a-416">Create a package that contains Office, Visio, and Project.</span></span></p></li>
<li><p><span data-ttu-id="f593a-417">Implante o pacote para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="f593a-417">Deploy the package to all users.</span></span></p></li>
<li><p><span data-ttu-id="f593a-418">Use <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)"> o Microsoft AppLocker </a> para impedir que usuários específicos usem o Visio e o Project.</span><span class="sxs-lookup"><span data-stu-id="f593a-418">Use <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)">Microsoft AppLocker</a> to prevent specific users from using Visio and Project.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f593a-419">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="f593a-419">Additional resources</span></span>


**<span data-ttu-id="f593a-420">Recursos adicionais dos pacotes do Office 2013 App-V</span><span class="sxs-lookup"><span data-stu-id="f593a-420">Office 2013 App-V Packages Additional Resources</span></span>**

[<span data-ttu-id="f593a-421">Ferramenta de implantação do Office para clique para executar</span><span class="sxs-lookup"><span data-stu-id="f593a-421">Office Deployment Tool for Click-to-Run</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=330672)

[<span data-ttu-id="f593a-422">Cenários suportados para a implantação do Microsoft Office como um pacote App-V sequenciado</span><span class="sxs-lookup"><span data-stu-id="f593a-422">Supported scenarios for deploying Microsoft Office as a sequenced App-V Package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**<span data-ttu-id="f593a-423">Pacotes do Office 2010 App-V</span><span class="sxs-lookup"><span data-stu-id="f593a-423">Office 2010 App-V Packages</span></span>**

[<span data-ttu-id="f593a-424">Kit de sequenciamento do Microsoft Office 2010 para Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="f593a-424">Microsoft Office 2010 Sequencing Kit for Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[<span data-ttu-id="f593a-425">Problemas conhecidos ao criar ou usar um pacote do App-V 5,0 do Office 2010</span><span class="sxs-lookup"><span data-stu-id="f593a-425">Known issues when you create or use an App-V 5.0 Office 2010 package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[<span data-ttu-id="f593a-426">Como sequenciar o Microsoft Office 2010 no Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="f593a-426">How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**<span data-ttu-id="f593a-427">Grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="f593a-427">Connection Groups</span></span>**

[<span data-ttu-id="f593a-428">Implantando grupos de conexão no Microsoft App-V V5</span><span class="sxs-lookup"><span data-stu-id="f593a-428">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="f593a-429">Gerenciando grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="f593a-429">Managing Connection Groups</span></span>](managing-connection-groups51.md)

**<span data-ttu-id="f593a-430">Configuração dinâmica</span><span class="sxs-lookup"><span data-stu-id="f593a-430">Dynamic Configuration</span></span>**

[<span data-ttu-id="f593a-431">Sobre a configuração dinâmica do App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="f593a-431">About App-V 5.1 Dynamic Configuration</span></span>](about-app-v-51-dynamic-configuration.md)














