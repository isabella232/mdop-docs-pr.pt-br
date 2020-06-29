---
title: Implantando o Microsoft Office 2016 usando o App-V
description: Implantando o Microsoft Office 2016 usando o App-V
author: dansimp
ms.assetid: cc675cde-cb8d-4b7c-a700-6104b78f1d89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 07/25/2017
ms.openlocfilehash: dfedab98e0bdf0a0d5f5e407d9bedadbbf56ad69
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796545"
---
# <span data-ttu-id="5ceb9-103">Implantando o Microsoft Office 2016 usando o App-V</span><span class="sxs-lookup"><span data-stu-id="5ceb9-103">Deploying Microsoft Office 2016 by Using App-V</span></span>


<span data-ttu-id="5ceb9-104">Use as informações neste artigo para usar o Microsoft Application Virtualization 5,0 ou versões posteriores para fornecer o Microsoft Office 2016 como um aplicativo virtualizado para computadores em sua organização.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-104">Use the information in this article to use Microsoft Application Virtualization 5.0, or later versions, to deliver Microsoft Office 2016 as a virtualized application to computers in your organization.</span></span> <span data-ttu-id="5ceb9-105">Para obter informações sobre como usar o App-V para fornecer o Office 2013, consulte [implantando o Microsoft Office 2013 usando o app-v](deploying-microsoft-office-2013-by-using-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="5ceb9-105">For information about using App-V to deliver Office 2013, see [Deploying Microsoft Office 2013 by Using App-V](deploying-microsoft-office-2013-by-using-app-v.md).</span></span> <span data-ttu-id="5ceb9-106">Para obter informações sobre como usar o App-V para fornecer o Office 2010, consulte [implantando o Microsoft Office 2010 usando o app-v](deploying-microsoft-office-2010-by-using-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="5ceb9-106">For information about using App-V to deliver Office 2010, see [Deploying Microsoft Office 2010 by Using App-V](deploying-microsoft-office-2010-by-using-app-v.md).</span></span>

<span data-ttu-id="5ceb9-107">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="5ceb9-108">O que saber antes de começar</span><span class="sxs-lookup"><span data-stu-id="5ceb9-108">What to know before you start</span></span>](#bkmk-before-you-start)

-   [<span data-ttu-id="5ceb9-109">Criando um pacote do Office 2016 para o App-V com a ferramenta de implantação do Office</span><span class="sxs-lookup"><span data-stu-id="5ceb9-109">Creating an Office 2016 package for App-V with the Office Deployment Tool</span></span>](#bkmk-create-office-pkg)

-   [<span data-ttu-id="5ceb9-110">Publicando o pacote do Office para o App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="5ceb9-110">Publishing the Office package for App-V 5.0</span></span>](#bkmk-pub-pkg-office)

-   [<span data-ttu-id="5ceb9-111">Personalizando e gerenciando pacotes do Office App-V</span><span class="sxs-lookup"><span data-stu-id="5ceb9-111">Customizing and managing Office App-V packages</span></span>](#bkmk-custmz-manage-office-pkgs)

## <a href="" id="bkmk-before-you-start"></a><span data-ttu-id="5ceb9-112">O que saber antes de começar</span><span class="sxs-lookup"><span data-stu-id="5ceb9-112">What to know before you start</span></span>


<span data-ttu-id="5ceb9-113">Antes de implantar o Office 2016 usando o App-V, examine as informações de planejamento a seguir.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-113">Before you deploy Office 2016 by using App-V, review the following planning information.</span></span>

### <a href="" id="bkmk-supp-vers-coexist"></a><span data-ttu-id="5ceb9-114">Versões do Office com suporte e coexistência do Office</span><span class="sxs-lookup"><span data-stu-id="5ceb9-114">Supported Office versions and Office coexistence</span></span>

<span data-ttu-id="5ceb9-115">Use a tabela a seguir para obter informações sobre as versões compatíveis do Office e sobre como executar versões coexistentes do Office.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-115">Use the following table to get information about supported versions of Office and about running coexisting versions of Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ceb9-116">Informações a serem revisadas</span><span class="sxs-lookup"><span data-stu-id="5ceb9-116">Information to review</span></span></th>
<th align="left"><span data-ttu-id="5ceb9-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ceb9-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv" data-raw-source="[Supported versions of Microsoft Office](planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv)"><span data-ttu-id="5ceb9-118">Versões com suporte do Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="5ceb9-118">Supported versions of Microsoft Office</span></span></a></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="5ceb9-119">Versões com suporte do Office</span><span class="sxs-lookup"><span data-stu-id="5ceb9-119">Supported versions of Office</span></span></p></li>
<li><p><span data-ttu-id="5ceb9-120">Tipos de implantação com suporte (por exemplo, área de trabalho, infraestrutura de área de trabalho virtual pessoal (VDI), VDI em pool)</span><span class="sxs-lookup"><span data-stu-id="5ceb9-120">Supported deployment types (for example, desktop, personal Virtual Desktop Infrastructure (VDI), pooled VDI)</span></span></p></li>
<li><p><span data-ttu-id="5ceb9-121">Opções de licenciamento do Office</span><span class="sxs-lookup"><span data-stu-id="5ceb9-121">Office licensing options</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-plan-coexisting" data-raw-source="[Planning for Using App-V with coexisting versions of Office](planning-for-using-app-v-with-office.md#bkmk-plan-coexisting)"><span data-ttu-id="5ceb9-122">Planejando o uso do App-V com versões coexistentes do Office</span><span class="sxs-lookup"><span data-stu-id="5ceb9-122">Planning for Using App-V with coexisting versions of Office</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="5ceb9-123">Considerações para a instalação de diferentes versões do Office no mesmo computador</span><span class="sxs-lookup"><span data-stu-id="5ceb9-123">Considerations for installing different versions of Office on the same computer</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pkg-pub-reqs"></a><span data-ttu-id="5ceb9-124">Requisitos de empacotamento, publicação e implantação</span><span class="sxs-lookup"><span data-stu-id="5ceb9-124">Packaging, publishing, and deployment requirements</span></span>

<span data-ttu-id="5ceb9-125">Antes de implantar o Office usando o App-V, examine os seguintes requisitos.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-125">Before you deploy Office by using App-V, review the following requirements.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ceb9-126">Tarefa</span><span class="sxs-lookup"><span data-stu-id="5ceb9-126">Task</span></span></th>
<th align="left"><span data-ttu-id="5ceb9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ceb9-127">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ceb9-128">Embalagem</span><span class="sxs-lookup"><span data-stu-id="5ceb9-128">Packaging</span></span></p></td>
<td align="left">
<ul>
<li><p><span data-ttu-id="5ceb9-129">Todos os aplicativos do Office que você deseja implantar para os usuários devem estar em um único pacote.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-129">All of the Office applications that you want to deploy to users must be in a single package.</span></span></p></li>
<li><p><span data-ttu-id="5ceb9-130">No App-V 5,0 e posterior, você deve usar a ferramenta de implantação do Office para criar pacotes.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-130">In App-V 5.0 and later, you must use the Office Deployment Tool to create packages.</span></span> <span data-ttu-id="5ceb9-131">Não é possível usar o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-131">You cannot use the Sequencer.</span></span></p></li>
<li><p><span data-ttu-id="5ceb9-132">Se você estiver implantando o Microsoft Visio 2016 e o Microsoft Project 2016 juntamente com o Office, deverá incluí-los no mesmo pacote com o Office.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-132">If you are deploying Microsoft Visio 2016 and Microsoft Project 2016 along with Office, you must include them in the same package with Office.</span></span> <span data-ttu-id="5ceb9-133">Para obter mais informações, consulte <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2016 and Project 2016 with Office](#bkmk-deploy-visio-project)"> implantação do Visio 2016 e do Project 2016 com o Office </a> .</span><span class="sxs-lookup"><span data-stu-id="5ceb9-133">For more information, see <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2016 and Project 2016 with Office](#bkmk-deploy-visio-project)">Deploying Visio 2016 and Project 2016 with Office</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ceb9-134">Publicação</span><span class="sxs-lookup"><span data-stu-id="5ceb9-134">Publishing</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="5ceb9-135">Você pode publicar apenas um pacote do Office em cada computador cliente.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-135">You can publish only one Office package to each client computer.</span></span></p></li>
<li><p><span data-ttu-id="5ceb9-136">Você deve publicar o pacote do Office globalmente.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-136">You must publish the Office package globally.</span></span> <span data-ttu-id="5ceb9-137">Você não pode publicar para o usuário.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-137">You cannot publish to the user.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ceb9-138">Implantando qualquer um dos seguintes produtos em um computador compartilhado, por exemplo, usando serviços de área de trabalho remota:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-138">Deploying any of the following products to a shared computer, for example, by using Remote Desktop Services:</span></span></p>
<ul>
<li><p><span data-ttu-id="5ceb9-139">Aplicativos do Microsoft 365 para empresas</span><span class="sxs-lookup"><span data-stu-id="5ceb9-139">Microsoft 365 Apps for enterprise</span></span></p></li>
<li><p><span data-ttu-id="5ceb9-140">Visio pro para Office 365</span><span class="sxs-lookup"><span data-stu-id="5ceb9-140">Visio Pro for Office 365</span></span></p></li>
<li><p><span data-ttu-id="5ceb9-141">Project pro para Office 365</span><span class="sxs-lookup"><span data-stu-id="5ceb9-141">Project Pro for Office 365</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="5ceb9-142">Você deve habilitar a <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)"> ativação de computador compartilhado </a> .</span><span class="sxs-lookup"><span data-stu-id="5ceb9-142">You must enable <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)">shared computer activation</a>.</span></span></p>
</td>
</tr>
</tbody>
</table>



### <span data-ttu-id="5ceb9-143">Excluindo aplicativos do Office de um pacote</span><span class="sxs-lookup"><span data-stu-id="5ceb9-143">Excluding Office applications from a package</span></span>

<span data-ttu-id="5ceb9-144">A tabela a seguir descreve os métodos recomendados para excluir aplicativos específicos do Office de um pacote.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-144">The following table describes the recommended methods for excluding specific Office applications from a package.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ceb9-145">Tarefa</span><span class="sxs-lookup"><span data-stu-id="5ceb9-145">Task</span></span></th>
<th align="left"><span data-ttu-id="5ceb9-146">Detalhes</span><span class="sxs-lookup"><span data-stu-id="5ceb9-146">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ceb9-147">Use a <strong> </strong> configuração ExcludeApp quando você cria o pacote usando a ferramenta de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-147">Use the <strong>ExcludeApp</strong> setting when you create the package by using the Office Deployment Tool.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="5ceb9-148">Permite que você exclua aplicativos específicos do Office do pacote quando a ferramenta de implantação do Office cria o pacote.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-148">Enables you to exclude specific Office applications from the package when the Office Deployment Tool creates the package.</span></span> <span data-ttu-id="5ceb9-149">Por exemplo, você pode usar essa configuração para criar um pacote que contenha apenas o Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-149">For example, you can use this setting to create a package that contains only Microsoft Word.</span></span></p></li>
<li><p><span data-ttu-id="5ceb9-150">Para obter mais informações, consulte o <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)"> elemento ExcludeApp </a> .</span><span class="sxs-lookup"><span data-stu-id="5ceb9-150">For more information, see <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)">ExcludeApp element</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ceb9-151">Modificar o arquivo DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="5ceb9-151">Modify the DeploymentConfig.xml file</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="5ceb9-152">Modifique o arquivo DeploymentConfig.xml após a criação do pacote.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-152">Modify the DeploymentConfig.xml file after the package has been created.</span></span> <span data-ttu-id="5ceb9-153">Esse arquivo contém as configurações padrão do pacote para todos os usuários em um computador que esteja executando o cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-153">This file contains the default package settings for all users on a computer that is running the App-V Client.</span></span></p></li>
<li><p><span data-ttu-id="5ceb9-154">Para obter mais informações, consulte <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2016 applications](#bkmk-disable-office-apps)"> desabilitando aplicativos do Office 2016 </a> .</span><span class="sxs-lookup"><span data-stu-id="5ceb9-154">For more information, see <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2016 applications](#bkmk-disable-office-apps)">Disabling Office 2016 applications</a>.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-create-office-pkg"></a><span data-ttu-id="5ceb9-155">Criando um pacote do Office 2016 para o App-V com a ferramenta de implantação do Office</span><span class="sxs-lookup"><span data-stu-id="5ceb9-155">Creating an Office 2016 package for App-V with the Office Deployment Tool</span></span>


<span data-ttu-id="5ceb9-156">Conclua as etapas a seguir para criar um pacote do Office 2016 para o App-V 5,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-156">Complete the following steps to create an Office 2016 package for App-V 5.0 or later.</span></span>

><span data-ttu-id="5ceb9-157">**Important** &nbsp; Importante &nbsp; No App-V 5,0 e posterior, você deve usar a ferramenta de implantação do Office para criar um pacote.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-157">**Important**&nbsp;&nbsp;In App-V 5.0 and later, you must use the Office Deployment Tool to create a package.</span></span> <span data-ttu-id="5ceb9-158">Você não pode usar o sequenciador para criar pacotes.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-158">You cannot use the Sequencer to create packages.</span></span>

### <span data-ttu-id="5ceb9-159">Revisar os pré-requisitos para usar a ferramenta de implantação do Office</span><span class="sxs-lookup"><span data-stu-id="5ceb9-159">Review prerequisites for using the Office Deployment Tool</span></span>

<span data-ttu-id="5ceb9-160">O computador no qual você está instalando a ferramenta de implantação do Office deve ter:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-160">The computer on which you are installing the Office Deployment Tool must have:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ceb9-161">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="5ceb9-161">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="5ceb9-162">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ceb9-162">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ceb9-163">Software de pré-requisito</span><span class="sxs-lookup"><span data-stu-id="5ceb9-163">Prerequisite software</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ceb9-164">.NET Framework 4</span><span class="sxs-lookup"><span data-stu-id="5ceb9-164">.Net Framework 4</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ceb9-165">Sistemas operacionais compatíveis</span><span class="sxs-lookup"><span data-stu-id="5ceb9-165">Supported operating systems</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="5ceb9-166">versão de 64 bits do Windows 10</span><span class="sxs-lookup"><span data-stu-id="5ceb9-166">64-bit version of Windows 10</span></span></p></li>
<li><p><span data-ttu-id="5ceb9-167">versão de 64 bits do Windows 8 ou 8,1</span><span class="sxs-lookup"><span data-stu-id="5ceb9-167">64-bit version of Windows 8 or 8.1</span></span></p></li>
<li><p><span data-ttu-id="5ceb9-168">versão de 64 bits do Windows 7</span><span class="sxs-lookup"><span data-stu-id="5ceb9-168">64-bit version of Windows 7</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


><span data-ttu-id="5ceb9-169">**Observação**  Neste tópico, o termo "Office 2016 App-V Package" refere-se ao licenciamento de assinatura.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-169">**Note**  In this topic, the term “Office 2016 App-V package” refers to subscription licensing.</span></span>


### <span data-ttu-id="5ceb9-170">Criar pacotes do Office 2016 App-V usando a ferramenta de implantação do Office</span><span class="sxs-lookup"><span data-stu-id="5ceb9-170">Create Office 2016 App-V Packages Using Office Deployment Tool</span></span>

<span data-ttu-id="5ceb9-171">Você cria pacotes do Office 2016 App-V usando a ferramenta de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-171">You create Office 2016 App-V packages by using the Office Deployment Tool.</span></span> <span data-ttu-id="5ceb9-172">As instruções a seguir explicam como criar um pacote do Office 2016 App-V com licenciamento de assinatura.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-172">The following instructions explain how to create an Office 2016 App-V package with Subscription Licensing.</span></span>

<span data-ttu-id="5ceb9-173">Crie pacotes do Office 2016 App-V em computadores com Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-173">Create Office 2016 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="5ceb9-174">Uma vez criado, o pacote do Office 2016 App-V será executado em computadores com o Windows 7, o Windows 8,1 e o Windows 10 com 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-174">Once created, the Office 2016 App-V package will run on 32-bit and 64-bit Windows 7, Windows 8.1, and Windows 10 computers.</span></span>

### <span data-ttu-id="5ceb9-175">Baixar a ferramenta de implantação do Office</span><span class="sxs-lookup"><span data-stu-id="5ceb9-175">Download the Office Deployment Tool</span></span>

<span data-ttu-id="5ceb9-176">Os pacotes do Office 2016 App-V são criados usando a ferramenta de implantação do Office, que gera um pacote do Office 2016 App-V.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-176">Office 2016 App-V Packages are created using the Office Deployment Tool, which generates an Office 2016 App-V Package.</span></span> <span data-ttu-id="5ceb9-177">O pacote não pode ser criado ou modificado por meio do sequenciador App-V.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-177">The package cannot be created or modified through the App-V sequencer.</span></span> <span data-ttu-id="5ceb9-178">Para começar a criação de pacotes:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-178">To begin package creation:</span></span>

1.  <span data-ttu-id="5ceb9-179">Baixe a [ferramenta de implantação do Office 2016 para clique para executar](https://www.microsoft.com/download/details.aspx?id=49117).</span><span class="sxs-lookup"><span data-stu-id="5ceb9-179">Download the [Office 2016 Deployment Tool for Click-to-Run](https://www.microsoft.com/download/details.aspx?id=49117).</span></span>

> <span data-ttu-id="5ceb9-180">**Importante** Você deve usar a ferramenta de implantação do Office 2016 para criar pacotes do Office 2016 App-V.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-180">**Important** You must use the Office 2016 Deployment Tool to create Office 2016 App-V Packages.</span></span>
> 2. <span data-ttu-id="5ceb9-181">Execute o arquivo. exe e extraia seus recursos para o local desejado.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-181">Run the .exe file and extract its features into the desired location.</span></span> <span data-ttu-id="5ceb9-182">Para facilitar esse processo, você pode criar uma pasta de rede compartilhada na qual os recursos serão salvos.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-182">To make this process easier, you can create a shared network folder where the features will be saved.</span></span>

    Example: \\\\Server\\Office2016

3. <span data-ttu-id="5ceb9-183">Verifique se há um setup.exe e um arquivo configuration.xml e se estão no local especificado.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-183">Check that a setup.exe and a configuration.xml file exist and are in the location you specified.</span></span>

### <span data-ttu-id="5ceb9-184">Baixar aplicativos do Office 2016</span><span class="sxs-lookup"><span data-stu-id="5ceb9-184">Download Office 2016 applications</span></span>

<span data-ttu-id="5ceb9-185">Depois de baixar a ferramenta de implantação do Office, você pode usá-la para obter os aplicativos mais recentes do Office 2016.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-185">After you download the Office Deployment Tool, you can use it to get the latest Office 2016 applications.</span></span> <span data-ttu-id="5ceb9-186">Depois de obter os aplicativos do Office, crie o pacote do Office 2016 App-V.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-186">After getting the Office applications, you create the Office 2016 App-V package.</span></span>

<span data-ttu-id="5ceb9-187">O arquivo XML que está incluído na ferramenta de implantação do Office especifica os detalhes do produto, como os idiomas e os aplicativos do Office incluídos.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-187">The XML file that is included in the Office Deployment Tool specifies the product details, such as the languages and Office applications included.</span></span>

1. <span data-ttu-id="5ceb9-188">**Personalize o arquivo de configuração XML de exemplo:** Use o arquivo de configuração XML de exemplo que você baixou com a ferramenta de implantação do Office para personalizar os aplicativos do Office:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-188">**Customize the sample XML configuration file:** Use the sample XML configuration file that you downloaded with the Office Deployment Tool to customize the Office applications:</span></span>

   1. <span data-ttu-id="5ceb9-189">Abra o arquivo XML de exemplo no bloco de notas ou no seu editor de texto favorito.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-189">Open the sample XML file in Notepad or your favorite text editor.</span></span>

   2. <span data-ttu-id="5ceb9-190">Com o exemplo configuration.xml arquivo aberto e pronto para edição, você pode especificar produtos, idiomas e o caminho para o qual você salva os aplicativos do Office 2016.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-190">With the sample configuration.xml file open and ready for editing, you can specify products, languages, and the path to which you save the Office 2016 applications.</span></span> <span data-ttu-id="5ceb9-191">Veja a seguir um exemplo básico do arquivo configuration.xml:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-191">The following is a basic example of the configuration.xml file:</span></span>

      ```xml
      <Configuration>
         <Add SourcePath= "\\Server\Office2016” OfficeClientEdition="32" >
          <Product ID="O365ProPlusRetail ">
            <Language ID="en-us" />
          </Product>
          <Product ID="VisioProRetail">
            <Language ID="en-us" />
          </Product>
        </Add>
      </Configuration>
      ```

      ><span data-ttu-id="5ceb9-192">**Observação**  O XML de configuração é um arquivo XML de exemplo.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-192">**Note**  The configuration XML is a sample XML file.</span></span> <span data-ttu-id="5ceb9-193">O arquivo inclui linhas que foram comentadas. Você pode "remover o comentário" dessas linhas para personalizar as configurações adicionais com o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-193">The file includes lines that are commented out. You can “uncomment” these lines to customize additional settings with the file.</span></span> <span data-ttu-id="5ceb9-194">Para "remover o comentário" dessas linhas, remova a "<!</span><span class="sxs-lookup"><span data-stu-id="5ceb9-194">To “uncomment” these lines, remove the "<!</span></span> <span data-ttu-id="5ceb9-195">--"do início da linha e"--> "do final da linha.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-195">- -" from the beginning of the line, and the "-- >" from the end of the line.</span></span>

      <span data-ttu-id="5ceb9-196">O arquivo de configuração XML acima Especifica que o Office 2016 ProPlus 32-bit Edition, incluindo o Visio ProPlus, será baixado em inglês para o \\\\server\\Office 2016, que é o local onde os aplicativos do Office serão salvos.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-196">The above XML configuration file specifies that Office 2016 ProPlus 32-bit edition, including Visio ProPlus, will be downloaded in English to the \\\\server\\Office 2016, which is the location where Office applications will be saved to.</span></span> <span data-ttu-id="5ceb9-197">Observe que a ID do produto dos aplicativos não afetará o licenciamento final do Office.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-197">Note that the Product ID of the applications will not affect the final licensing of Office.</span></span> <span data-ttu-id="5ceb9-198">Os pacotes do Office 2016 App-V com várias licenças podem ser criados a partir dos mesmos aplicativos por meio da especificação de licenciamento em um estágio posterior.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-198">Office 2016 App-V packages with various licensing can be created from the same applications through specifying licensing in a later stage.</span></span> <span data-ttu-id="5ceb9-199">A tabela a seguir resume os atributos e elementos personalizáveis do arquivo XML:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-199">The table below summarizes the customizable attributes and elements of XML file:</span></span>

      <table>
      <colgroup>
      <col width="33%" />
      <col width="33%" />
      <col width="33%" />
      </colgroup>
      <thead>
      <tr class="header">
      <th align="left"><span data-ttu-id="5ceb9-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="5ceb9-200">Input</span></span></th>
      <th align="left"><span data-ttu-id="5ceb9-201">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ceb9-201">Description</span></span></th>
      <th align="left"><span data-ttu-id="5ceb9-202">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5ceb9-202">Example</span></span></th>
      </tr>
      </thead>
      <tbody>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="5ceb9-203">Adicionar elemento</span><span class="sxs-lookup"><span data-stu-id="5ceb9-203">Add element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="5ceb9-204">Especifica os produtos e idiomas a serem incluídos no pacote.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-204">Specifies the products and languages to include in the package.</span></span></p></td>
      <td align="left"><p><span data-ttu-id="5ceb9-205">N/A</span><span class="sxs-lookup"><span data-stu-id="5ceb9-205">N/A</span></span></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="5ceb9-206">OfficeClientEdition (atributo do elemento add)</span><span class="sxs-lookup"><span data-stu-id="5ceb9-206">OfficeClientEdition (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="5ceb9-207">Especifica a edição do produto do Office 2016 a ser usado: 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-207">Specifies the edition of Office 2016 product to use: 32-bit or 64-bit.</span></span> <span data-ttu-id="5ceb9-208">A operação falhará se <strong> OfficeClientEdition </strong> não estiver definido como um valor válido.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-208">The operation fails if <strong>OfficeClientEdition</strong> is not set to a valid value.</span></span></p></td>
      <td align="left"><p><strong><span data-ttu-id="5ceb9-209">OfficeClientEdition </strong> = &quot; 32&quot;</span><span class="sxs-lookup"><span data-stu-id="5ceb9-209">OfficeClientEdition</strong>=&quot;32&quot;</span></span></p>
      <p><strong><span data-ttu-id="5ceb9-210">OfficeClientEdition </strong> = &quot; 64&quot;</span><span class="sxs-lookup"><span data-stu-id="5ceb9-210">OfficeClientEdition</strong>=&quot;64&quot;</span></span></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="5ceb9-211">Elemento Product</span><span class="sxs-lookup"><span data-stu-id="5ceb9-211">Product element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="5ceb9-212">Especifica o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-212">Specifies the application.</span></span> <span data-ttu-id="5ceb9-213">O Project 2016 e o Visio 2016 devem ser especificados aqui como um produto adicionado a ser incluído nos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-213">Project 2016 and Visio 2016 must be specified here as an added product to be included in the applications.</span></span>

      <span data-ttu-id="5ceb9-214">Para obter mais informações sobre os IDs de produto, consulte <a href="https://support.microsoft.com/kb/2842297" data-raw-source="[Product IDs that are supported by the Office Deployment Tool for Click-to-Run](https://support.microsoft.com/kb/2842297)"> IDs de produto que são suportados pela ferramenta de implantação do Office para clique para executar</span><span class="sxs-lookup"><span data-stu-id="5ceb9-214">For more information about the product IDs, see <a href="https://support.microsoft.com/kb/2842297" data-raw-source="[Product IDs that are supported by the Office Deployment Tool for Click-to-Run](https://support.microsoft.com/kb/2842297)">Product IDs that are supported by the Office Deployment Tool for Click-to-Run</span></span></a>
      </p></td>
      <td align="left"><p><code>Product ID =&quot;O365ProPlusRetail &quot;</code></p>
      <p><code>Product ID =&quot;VisioProRetail&quot;</code></p>
      <p><code>Product ID =&quot;ProjectProRetail&quot;</code></p>
      </td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="5ceb9-215">Elemento de linguagem</span><span class="sxs-lookup"><span data-stu-id="5ceb9-215">Language element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="5ceb9-216">Especifica o idioma com suporte nos aplicativos</span><span class="sxs-lookup"><span data-stu-id="5ceb9-216">Specifies the language supported in the applications</span></span></p></td>
      <td align="left"><p><code>Language ID=&quot;en-us&quot;</code></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="5ceb9-217">Versão (atributo do elemento add)</span><span class="sxs-lookup"><span data-stu-id="5ceb9-217">Version (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="5ceb9-218">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-218">Optional.</span></span> <span data-ttu-id="5ceb9-219">Especifica uma compilação a ser usada para o pacote</span><span class="sxs-lookup"><span data-stu-id="5ceb9-219">Specifies a build to use for the package</span></span></p>
      <p><span data-ttu-id="5ceb9-220">O padrão é a compilação anunciada mais recente (conforme definido no v32.CAB na origem do Office).</span><span class="sxs-lookup"><span data-stu-id="5ceb9-220">Defaults to latest advertised build (as defined in v32.CAB at the Office source).</span></span></p></td>
      <td align="left"><p><code>16.1.2.3</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="5ceb9-221">Caminho_de_origem (atributo do elemento add)</span><span class="sxs-lookup"><span data-stu-id="5ceb9-221">SourcePath (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="5ceb9-222">Especifica o local em que os aplicativos serão salvos.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-222">Specifies the location in which the applications will be saved to.</span></span></p></td>
      <td align="left"><p><code>Sourcepath = &quot;\Server\Office2016”</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="5ceb9-223">Canal (atributo do elemento add)</span><span class="sxs-lookup"><span data-stu-id="5ceb9-223">Channel (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="5ceb9-224">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-224">Optional.</span></span> <span data-ttu-id="5ceb9-225">Especifica o canal de atualização do produto que você deseja baixar ou instalar.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-225">Specifies the update channel for the product that you want to download or install.</span></span> </p><p><span data-ttu-id="5ceb9-226">Para obter mais informações sobre os canais de atualização, consulte Visão geral de canais de atualização para aplicativos do Microsoft 365 para empresas.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-226">For more information about update channels, see Overview of update channels for Microsoft 365 Apps for enterprise.</span></span></p></td>
      <td align="left"><p><code>Channel=&quot;Deferred&quot;</code></p></td>
      </tr>
      </tbody>
      </table>

      <span data-ttu-id="5ceb9-227">Depois de editar o arquivo configuration.xml para especificar o produto desejado, os idiomas e também o local em que os aplicativos do Office 2016 serão salvos, você poderá salvar o arquivo de configuração, por exemplo, como Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-227">After editing the configuration.xml file to specify the desired product, languages, and also the location which the Office 2016 applications will be saved onto, you can save the configuration file, for example, as Customconfig.xml.</span></span>

2. <span data-ttu-id="5ceb9-228">**Baixe os aplicativos para o local especificado:** Use um prompt de comando elevado e um sistema operacional de 64 bits para baixar os aplicativos do Office 2016 que serão convertidos posteriormente em um pacote do App-V.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-228">**Download the applications into the specified location:** Use an elevated command prompt and a 64 bit operating system to download the Office 2016 applications that will later be converted into an App-V package.</span></span> <span data-ttu-id="5ceb9-229">Veja a seguir um exemplo de comando com uma descrição de detalhes:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-229">Below is an example command with a description of details:</span></span>

   ``` syntax
   \\server\Office2016\setup.exe /download \\server\Office2016\Customconfig.xml
   ```

   <span data-ttu-id="5ceb9-230">No exemplo:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-230">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="5ceb9-231">\server\Office2016</span><span class="sxs-lookup"><span data-stu-id="5ceb9-231">\server\Office2016</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5ceb9-232">é o local de compartilhamento de rede que contém a ferramenta de implantação do Office e o arquivo de Configuration.xml personalizado Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-232">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="5ceb9-233">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="5ceb9-233">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5ceb9-234">é a ferramenta de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-234">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="5ceb9-235">/Download</span><span class="sxs-lookup"><span data-stu-id="5ceb9-235">/download</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5ceb9-236">baixa os aplicativos do Office 2016 que você especificar no arquivo customConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-236">downloads the Office 2016 applications that you specify in the customConfig.xml file.</span></span> <span data-ttu-id="5ceb9-237">Esses bits podem ser convertidos posteriormente em um pacote do Office 2016 App-V com licenciamento por volume.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-237">These bits can be later converted in an Office 2016 App-V package with Volume Licensing.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="5ceb9-238">\server\Office2016\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="5ceb9-238">\server\Office2016\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5ceb9-239">passa o arquivo de configuração XML necessário para concluir o processo de download, neste exemplo, customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-239">passes the XML configuration file required to complete the download process, in this example, customconfig.xml.</span></span> <span data-ttu-id="5ceb9-240">Depois de usar o comando download, os aplicativos do Office devem ser encontrados no local especificado no arquivo XML de configuração, neste exemplo \Server\Office2016.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-240">After using the download command, Office applications should be found in the location specified in the configuration xml file, in this example \Server\Office2016.</span></span></p></td>
   </tr>
   </tbody>
   </table>



### <span data-ttu-id="5ceb9-241">Converter os aplicativos do Office em um pacote do App-V</span><span class="sxs-lookup"><span data-stu-id="5ceb9-241">Convert the Office applications into an App-V package</span></span>

<span data-ttu-id="5ceb9-242">Depois de baixar os aplicativos do Office 2016 por meio da ferramenta de implantação do Office, use a ferramenta de implantação do Office para convertê-los em um pacote do Office 2016 App-V.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-242">After you download the Office 2016 applications through the Office Deployment Tool, use the Office Deployment Tool to convert them into an Office 2016 App-V package.</span></span> <span data-ttu-id="5ceb9-243">Conclua as etapas que correspondem ao seu modelo de licenciamento.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-243">Complete the steps that correspond to your licensing model.</span></span>

**<span data-ttu-id="5ceb9-244">Resumo do que você precisará fazer:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-244">Summary of what you’ll need to do:</span></span>**

-   <span data-ttu-id="5ceb9-245">Crie os pacotes do Office 2016 App-V em computadores com Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-245">Create the Office 2016 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="5ceb9-246">No entanto, o pacote será executado em computadores de 32 bits 64 e no Windows 7, no Windows 8 ou 8,1 e no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-246">However, the package will run on 32-bit and 64-bit Windows 7, Windows 8 or 8.1, and Windows 10 computers.</span></span>

-   <span data-ttu-id="5ceb9-247">Crie um pacote do Office App-V para pacote de licenciamento de assinatura usando a ferramenta de implantação do Office e modifique o arquivo de configuração do CustomConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-247">Create an Office App-V package for Subscription Licensing package by using the Office Deployment Tool, and then modify the CustomConfig.xml configuration file.</span></span>

    <span data-ttu-id="5ceb9-248">A tabela a seguir resume os valores que você precisa inserir no arquivo CustomConfig.xml para o modelo de licenciamento que você está usando.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-248">The following table summarizes the values you need to enter in the CustomConfig.xml file for the licensing model you’re using.</span></span> <span data-ttu-id="5ceb9-249">As etapas nas seções que seguem a tabela especificarão as entradas exatas que você precisa fazer.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-249">The steps in the sections that follow the table will specify the exact entries you need to make.</span></span>

><span data-ttu-id="5ceb9-250">**Note** &nbsp; Observação &nbsp; Você pode usar a ferramenta de implantação do Office para criar pacotes do App-V para aplicativos do Microsoft 365 para empresas.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-250">**Note**&nbsp;&nbsp;You can use the Office Deployment Tool to create App-V packages for Microsoft 365 Apps for enterprise.</span></span> <span data-ttu-id="5ceb9-251">Não há suporte para a criação de pacotes para versões de licença de volume do Office Professional Plus ou do Office Standard.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-251">Creating packages for the volume-licensed versions of Office Professional Plus or Office Standard is not supported.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ceb9-252">ID do Produto (Product ID)</span><span class="sxs-lookup"><span data-stu-id="5ceb9-252">Product ID</span></span></th>
<th align="left"><span data-ttu-id="5ceb9-253">Licenciamento de assinatura</span><span class="sxs-lookup"><span data-stu-id="5ceb9-253">Subscription Licensing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5ceb9-254">Office 2016</span><span class="sxs-lookup"><span data-stu-id="5ceb9-254">Office 2016</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5ceb9-255">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="5ceb9-255">O365ProPlusRetail</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5ceb9-256">Office 2016 com Visio 2016</span><span class="sxs-lookup"><span data-stu-id="5ceb9-256">Office 2016 with Visio 2016</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5ceb9-257">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="5ceb9-257">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="5ceb9-258">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="5ceb9-258">VisioProRetail</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5ceb9-259">Office 2016 com Visio 2016 e Project 2016</span><span class="sxs-lookup"><span data-stu-id="5ceb9-259">Office 2016 with Visio 2016 and Project 2016</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5ceb9-260">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="5ceb9-260">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="5ceb9-261">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="5ceb9-261">VisioProRetail</span></span></p>
<p><span data-ttu-id="5ceb9-262">ProjectProRetail</span><span class="sxs-lookup"><span data-stu-id="5ceb9-262">ProjectProRetail</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="5ceb9-263">Como converter os aplicativos do Office em um pacote do App-V</span><span class="sxs-lookup"><span data-stu-id="5ceb9-263">How to convert the Office applications into an App-V package</span></span>**

1. <span data-ttu-id="5ceb9-264">No bloco de notas, abra novamente o arquivo CustomConfig.xml e faça as seguintes alterações no arquivo:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-264">In Notepad, reopen the CustomConfig.xml file, and make the following changes to the file:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="5ceb9-265">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ceb9-265">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="5ceb9-266">O que alterar o valor para</span><span class="sxs-lookup"><span data-stu-id="5ceb9-266">What to change the value to</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5ceb9-267">SourcePath</span><span class="sxs-lookup"><span data-stu-id="5ceb9-267">SourcePath</span></span></p></td>
   <td align="left"><p><span data-ttu-id="5ceb9-268">Aponte para os aplicativos do Office baixados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-268">Point to the Office applications downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="5ceb9-269">ProductID</span><span class="sxs-lookup"><span data-stu-id="5ceb9-269">ProductID</span></span></p></td>
   <td align="left"><p><span data-ttu-id="5ceb9-270">Especifique o licenciamento de assinatura, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-270">Specify Subscription licensing, as shown in the following example:</span></span></p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\server\Office 2016&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;O365ProPlusRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt; </code></pre>
   <p><span data-ttu-id="5ceb9-271">Neste exemplo, foram feitas as seguintes alterações para criar um pacote com licenciamento de assinatura:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-271">In this example, the following changes were made to create a package with Subscription licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="5ceb9-272">SourcePath</span><span class="sxs-lookup"><span data-stu-id="5ceb9-272">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5ceb9-273">é o caminho, que foi alterado para apontar para os aplicativos do Office que foram baixados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-273">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="5ceb9-274">ID do Produto (Product ID)</span><span class="sxs-lookup"><span data-stu-id="5ceb9-274">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5ceb9-275">para o Office foi alterado para <code>O365ProPlusRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="5ceb9-275">for Office was changed to <code>O365ProPlusRetail</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="5ceb9-276">ID do Produto (Product ID)</span><span class="sxs-lookup"><span data-stu-id="5ceb9-276">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5ceb9-277">para o Visio foi alterado para <code>VisioProRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="5ceb9-277">for Visio was changed to <code>VisioProRetail</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p></p>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="5ceb9-278">ExcludeApp (opcional)</span><span class="sxs-lookup"><span data-stu-id="5ceb9-278">ExcludeApp (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="5ceb9-279">Permite especificar os programas do Office que você não deseja incluir no pacote do App-V que a ferramenta de implantação do Office cria.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-279">Lets you specify Office programs that you don’t want included in the App-V package that the Office Deployment Tool creates.</span></span> <span data-ttu-id="5ceb9-280">Por exemplo, você pode excluir o Access e o InfoPath.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-280">For example, you can exclude Access and InfoPath.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="5ceb9-281">PACKAGEGUID (opcional)</span><span class="sxs-lookup"><span data-stu-id="5ceb9-281">PACKAGEGUID (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="5ceb9-282">Por padrão, todos os pacotes do App-V criados pela ferramenta de implantação do Office compartilham a mesma ID de pacote do App-V.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-282">By default, all App-V packages created by the Office Deployment Tool share the same App-V Package ID.</span></span> <span data-ttu-id="5ceb9-283">Você pode usar PACKAGEGUID para especificar uma ID de pacote diferente para cada pacote, que permite publicar vários pacotes do App-V, criados pela ferramenta de implantação do Office e gerenciá-los usando o servidor App-V.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-283">You can use PACKAGEGUID to specify a different package ID for each package, which allows you to publish multiple App-V packages, created by the Office Deployment Tool, and manage them by using the App-V Server.</span></span></p>
   <p><span data-ttu-id="5ceb9-284">Um exemplo de quando usar esse parâmetro é se você cria pacotes diferentes para usuários diferentes.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-284">An example of when to use this parameter is if you create different packages for different users.</span></span> <span data-ttu-id="5ceb9-285">Por exemplo, você pode criar um pacote com apenas o Office 2016 para alguns usuários e criar outro pacote com o Office 2016 e o Visio 2016 para outro conjunto de usuários.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-285">For example, you can create a package with just Office 2016 for some users, and create another package with Office 2016 and Visio 2016 for another set of users.</span></span></p>
<span data-ttu-id="5ceb9-286">&gt;<strong>Observação </strong> mesmo que você use IDs de pacote exclusivas, ainda é possível implantar apenas um pacote do App-V para um único dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-286">&gt;<strong>Note</strong> Even if you use unique package IDs, you can still deploy only one App-V package to a single device.</span></span>
   </td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="5ceb9-287">Use o comando/Packager para converter os aplicativos do Office em um pacote do Office 2016 App-V.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-287">Use the /packager command to convert the Office applications to an Office 2016 App-V package.</span></span>

   <span data-ttu-id="5ceb9-288">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-288">For example:</span></span>

   ``` syntax
   \\server\Office2016\setup.exe /packager \\server\Office2016\Customconfig.xml  \\server\share\Office2016AppV
   ```

   <span data-ttu-id="5ceb9-289">No exemplo:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-289">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="5ceb9-290">\server\Office2016</span><span class="sxs-lookup"><span data-stu-id="5ceb9-290">\server\Office2016</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5ceb9-291">é o local de compartilhamento de rede que contém a ferramenta de implantação do Office e o arquivo de Configuration.xml personalizado Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-291">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="5ceb9-292">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="5ceb9-292">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5ceb9-293">é a ferramenta de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-293">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="5ceb9-294">/packager</span><span class="sxs-lookup"><span data-stu-id="5ceb9-294">/packager</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5ceb9-295">cria o pacote App-V do Office 2016 com o tipo de licenciamento especificado no arquivo customConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-295">creates the Office 2016 App-V package with the type of licensing specified in the customConfig.xml file.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="5ceb9-296">\server\Office2016\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="5ceb9-296">\server\Office2016\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5ceb9-297">passa o arquivo XML de configuração (neste caso, customConfig) que foi preparado para o estágio de empacotamento.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-297">passes the configuration XML file (in this case customConfig) that has been prepared for the packaging stage.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="5ceb9-298">\server\share\Office 2016AppV</span><span class="sxs-lookup"><span data-stu-id="5ceb9-298">\server\share\Office 2016AppV</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5ceb9-299">Especifica o local do pacote do Office App-V recém-criado.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-299">specifies the location of the newly created Office App-V package.</span></span></p></td>
   </tr>
   </tbody>
   </table>



~~~
After you run the **/packager** command, the following folders appear up in the directory where you specified the package should be saved:

-   **App-V Packages** – contains an Office 2016 App-V package and two deployment configuration files.

-   **WorkingDir**

**Note** To troubleshoot any issues, see the log files in the %temp% directory (default).
~~~



3. <span data-ttu-id="5ceb9-300">Verifique se o pacote do Office 2016 App-V funciona corretamente:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-300">Verify that the Office 2016 App-V package works correctly:</span></span>

   1.  <span data-ttu-id="5ceb9-301">Publique o pacote do Office 2016 App-V, que você criou globalmente, em um computador de teste e verifique se os atalhos do Office 2016 são exibidos.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-301">Publish the Office 2016 App-V package, which you created globally, to a test computer, and verify that the Office 2016 shortcuts appear.</span></span>

   2.  <span data-ttu-id="5ceb9-302">Inicie alguns aplicativos do Office 2016, como o Excel ou o Word, para garantir que o pacote esteja funcionando conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-302">Start a few Office 2016 applications, such as Excel or Word, to ensure that your package is working as expected.</span></span>

## <a href="" id="bkmk-pub-pkg-office"></a><span data-ttu-id="5ceb9-303">Publicando o pacote do Office para App-V</span><span class="sxs-lookup"><span data-stu-id="5ceb9-303">Publishing the Office package for App-V</span></span>


<span data-ttu-id="5ceb9-304">Use as informações a seguir para publicar um pacote do Office.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-304">Use the following information to publish an Office package.</span></span>

### <span data-ttu-id="5ceb9-305">Métodos para publicar pacotes do Office App-V</span><span class="sxs-lookup"><span data-stu-id="5ceb9-305">Methods for publishing Office App-V packages</span></span>

<span data-ttu-id="5ceb9-306">Implante o pacote do App-V para o Office 2016 usando os mesmos métodos que você usa para qualquer outro pacote:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-306">Deploy the App-V package for Office 2016 by using the same methods you use for any other package:</span></span>

-   <span data-ttu-id="5ceb9-307">System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="5ceb9-307">System Center Configuration Manager</span></span>

-   <span data-ttu-id="5ceb9-308">Servidor do App-V</span><span class="sxs-lookup"><span data-stu-id="5ceb9-308">App-V Server</span></span>

-   <span data-ttu-id="5ceb9-309">Autônomos por meio de comandos do PowerShell</span><span class="sxs-lookup"><span data-stu-id="5ceb9-309">Stand-alone through PowerShell commands</span></span>

### <span data-ttu-id="5ceb9-310">Como publicar pré-requisitos e requisitos</span><span class="sxs-lookup"><span data-stu-id="5ceb9-310">Publishing prerequisites and requirements</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ceb9-311">Pré-requisito ou requisito</span><span class="sxs-lookup"><span data-stu-id="5ceb9-311">Prerequisite or requirement</span></span></th>
<th align="left"><span data-ttu-id="5ceb9-312">Detalhes</span><span class="sxs-lookup"><span data-stu-id="5ceb9-312">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ceb9-313">Habilitar o script do PowerShell nos clientes do App-V</span><span class="sxs-lookup"><span data-stu-id="5ceb9-313">Enable PowerShell scripting on the App-V clients</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ceb9-314">Para publicar pacotes do Office 2016, você deve executar um script.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-314">To publish Office 2016 packages, you must run a script.</span></span></p>
<p><span data-ttu-id="5ceb9-315">Os scripts de pacote são desativados por padrão em clientes App-V.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-315">Package scripts are disabled by default on App-V clients.</span></span> <span data-ttu-id="5ceb9-316">Para habilitar o script, execute o seguinte comando do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-316">To enable scripting, run the following PowerShell command:</span></span></p>
<pre class="syntax" space="preserve"><code>Set-AppvClientConfiguration –EnablePackageScripts 1</code></pre></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ceb9-317">Publicar o pacote do Office 2016 globalmente</span><span class="sxs-lookup"><span data-stu-id="5ceb9-317">Publish the Office 2016 package globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ceb9-318">Os pontos de extensão no pacote App-V do Office exigem instalação no nível do computador.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-318">Extension points in the Office App-V package require installation at the computer level.</span></span></p>
<p><span data-ttu-id="5ceb9-319">Quando você publica no nível do computador, não são necessárias ações de pré-requisito ou redistribuíveis, e o pacote do Office 2016 permite que seus aplicativos funcionem como o Office instalado nativamente, eliminando a necessidade de os administradores personalizarem pacotes.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-319">When you publish at the computer level, no prerequisite actions or redistributables are needed, and the Office 2016 package globally enables its applications to work like natively installed Office, eliminating the need for administrators to customize packages.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="5ceb9-320">Como publicar um pacote do Office</span><span class="sxs-lookup"><span data-stu-id="5ceb9-320">How to publish an Office package</span></span>

<span data-ttu-id="5ceb9-321">Execute o seguinte comando para publicar um pacote do Office globalmente:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-321">Run the following command to publish an Office package globally:</span></span>

-   `Add-AppvClientPackage <Path_to_AppV_Package> | Publish-AppvClientPackage –global`

-   <span data-ttu-id="5ceb9-322">No console de gerenciamento da Web no App-V Server, você pode adicionar permissões a um grupo de computadores em vez de a um grupo de usuários para permitir que os pacotes sejam publicados globalmente nos computadores do grupo correspondente.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-322">From the Web Management Console on the App-V Server, you can add permissions to a group of computers instead of to a user group to enable packages to be published globally to the computers in the corresponding group.</span></span>

## <a href="" id="bkmk-custmz-manage-office-pkgs"></a><span data-ttu-id="5ceb9-323">Personalizando e gerenciando pacotes do Office App-V</span><span class="sxs-lookup"><span data-stu-id="5ceb9-323">Customizing and managing Office App-V packages</span></span>


<span data-ttu-id="5ceb9-324">Para gerenciar seus pacotes do Office App-V, use as mesmas operações que faria para qualquer outro pacote, mas há algumas exceções, como descrito nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-324">To manage your Office App-V packages, use the same operations as you would for any other package, but there are a few exceptions, as outlined in the following sections.</span></span>

-   [<span data-ttu-id="5ceb9-325">Habilitando plug-ins do Office usando grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="5ceb9-325">Enabling Office plug-ins by using connection groups</span></span>](#bkmk-enable-office-plugins)

-   [<span data-ttu-id="5ceb9-326">Desativando aplicativos do Office 2016</span><span class="sxs-lookup"><span data-stu-id="5ceb9-326">Disabling Office 2016 applications</span></span>](#bkmk-disable-office-apps)

-   [<span data-ttu-id="5ceb9-327">Desativando atalhos do Office 2016</span><span class="sxs-lookup"><span data-stu-id="5ceb9-327">Disabling Office 2016 shortcuts</span></span>](#bkmk-disable-shortcuts)

-   [<span data-ttu-id="5ceb9-328">Gerenciando atualizações de pacote do Office 2016</span><span class="sxs-lookup"><span data-stu-id="5ceb9-328">Managing Office 2016 package upgrades</span></span>](#bkmk-manage-office-pkg-upgrd)

-   [<span data-ttu-id="5ceb9-329">Implantação do Visio 2016 e do Project 2016 com o Office</span><span class="sxs-lookup"><span data-stu-id="5ceb9-329">Deploying Visio 2016 and Project 2016 with Office</span></span>](#bkmk-deploy-visio-project)

### <a href="" id="bkmk-enable-office-plugins"></a><span data-ttu-id="5ceb9-330">Habilitando plug-ins do Office usando grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="5ceb9-330">Enabling Office plug-ins by using connection groups</span></span>

<span data-ttu-id="5ceb9-331">Use as etapas desta seção para habilitar os plug-ins do Office com o pacote do Office.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-331">Use the steps in this section to enable Office plug-ins with your Office package.</span></span> <span data-ttu-id="5ceb9-332">Para usar os plug-ins do Office, você deve usar o sequenciador do App-V para criar um pacote separado que contenha apenas os plug-ins. Não é possível usar a ferramenta de implantação do Office para criar o pacote de plug-ins.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-332">To use Office plug-ins, you must use the App-V Sequencer to create a separate package that contains just the plug-ins. You cannot use the Office Deployment Tool to create the plug-ins package.</span></span> <span data-ttu-id="5ceb9-333">Em seguida, crie um grupo de conexão que contenha o pacote de plug-ins e o pacote do Office, conforme descrito nas etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-333">You then create a connection group that contains the Office package and the plug-ins package, as described in the following steps.</span></span>

**<span data-ttu-id="5ceb9-334">Para habilitar plug-ins para pacotes do Office App-V</span><span class="sxs-lookup"><span data-stu-id="5ceb9-334">To enable plug-ins for Office App-V packages</span></span>**

1.  <span data-ttu-id="5ceb9-335">Adicione um grupo de conexão por meio do App-V Server, do System Center Configuration Manager ou de um cmdlet do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-335">Add a Connection Group through App-V Server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

2.  <span data-ttu-id="5ceb9-336">Sequenciar seus plug-ins usando o sequenciador do App-V.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-336">Sequence your plug-ins using the App-V Sequencer.</span></span> <span data-ttu-id="5ceb9-337">Verifique se o Office 2016 está instalado no computador que está sendo usado para sequenciar o plug-in.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-337">Ensure that Office 2016 is installed on the computer being used to sequence the plug-in.</span></span> <span data-ttu-id="5ceb9-338">É recomendável usar os aplicativos do Microsoft 365 para empresas (não virtuais) no computador de sequenciamento quando você sequenciar plug-ins do Office 2016.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-338">It is recommended you use Microsoft 365 Apps for enterprise(non-virtual) on the sequencing computer when you sequence Office 2016 plug-ins.</span></span>

3.  <span data-ttu-id="5ceb9-339">Crie um pacote do App-V que inclua os plug-ins desejados.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-339">Create an App-V package that includes the desired plug-ins.</span></span>

4.  <span data-ttu-id="5ceb9-340">Adicione um grupo de conexão por meio do App-V Server, do System Center Configuration Manager ou de um cmdlet do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-340">Add a Connection Group through App-V server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

5.  <span data-ttu-id="5ceb9-341">Adicione o pacote do Office 2016 App-V e o pacote de plug-ins que você sequenciaou ao grupo de conexão que você criou.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-341">Add the Office 2016 App-V package and the plug-ins package you sequenced to the Connection Group you created.</span></span>

    ><span data-ttu-id="5ceb9-342">**Importante** A ordem dos pacotes no grupo de conexão determina a ordem em que o conteúdo do pacote é mesclado.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-342">**Important** The order of the packages in the Connection Group determines the order in which the package contents are merged.</span></span> <span data-ttu-id="5ceb9-343">No arquivo do descritor de grupo de conexão, adicione o pacote do Office 2016 App-V primeiro e, em seguida, adicione o pacote do plug-in App-V.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-343">In your Connection group descriptor file, add the Office 2016 App-V package first, and then add the plug-in App-V package.</span></span>



6.  <span data-ttu-id="5ceb9-344">Certifique-se de que os dois pacotes sejam publicados no computador de destino e que o pacote de plug-in seja publicado globalmente para corresponder às configurações globais do pacote do Office 2016 App-V publicado.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-344">Ensure that both packages are published to the target computer and that the plug-in package is published globally to match the global settings of the published Office 2016 App-V package.</span></span>

7.  <span data-ttu-id="5ceb9-345">Verifique se o arquivo de configuração de implantação do pacote de plug-in tem as mesmas configurações que o pacote do Office 2016 App-V tem.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-345">Verify that the Deployment Configuration File of the plug-in package has the same settings that the Office 2016 App-V package has.</span></span>

    <span data-ttu-id="5ceb9-346">Como o pacote do Office 2016 App-V está integrado ao sistema operacional, as configurações do pacote de plug-in devem coincidir.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-346">Since the Office 2016 App-V package is integrated with the operating system, the plug-in package settings should match.</span></span> <span data-ttu-id="5ceb9-347">Você pode pesquisar o arquivo de configuração de implantação para "modo COM" e garantir que o pacote de plug-ins tenha esse valor definido como "integrado" e que "InProcessEnabled" e "OutOfProcessEnabled" correspondam às configurações do pacote do Office 2016 App-V que você publicou.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-347">You can search the Deployment Configuration File for “COM Mode” and ensure that your plug-ins package has that value set as “Integrated” and that both "InProcessEnabled" and "OutOfProcessEnabled" match the settings of the Office 2016 App-V package you published.</span></span>

8.  <span data-ttu-id="5ceb9-348">Abra o arquivo de configuração de implantação e defina o valor de **objetos habilitados** como **falso**.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-348">Open the Deployment Configuration File and set the value for **Objects Enabled** to **false**.</span></span>

9.  <span data-ttu-id="5ceb9-349">Se você fez qualquer alteração no arquivo de configuração de implantação após o sequenciamento, verifique se o pacote de plug-in é publicado com o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-349">If you made any changes to the Deployment Configuration file after sequencing, ensure that the plug-in package is published with the file.</span></span>

10. <span data-ttu-id="5ceb9-350">Verifique se o grupo de conexão que você criou está habilitado no computador desejado.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-350">Ensure that the Connection Group you created is enabled onto your desired computer.</span></span> <span data-ttu-id="5ceb9-351">O grupo de conexão criado provavelmente será "pendente" se o pacote do Office 2016 App-V estiver em uso quando o grupo de conexão estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-351">The Connection Group created will likely “pend” if the Office 2016 App-V package is in use when the Connection Group is enabled.</span></span> <span data-ttu-id="5ceb9-352">Se isso acontecer, será necessário reinicializar para habilitar o grupo de conexão com êxito.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-352">If that happens, you have to reboot to successfully enable the Connection Group.</span></span>

11. <span data-ttu-id="5ceb9-353">Depois de publicar com êxito os dois pacotes e habilitar o grupo de conexão, inicie o aplicativo de destino do Office 2016 e verifique se o plug-in que você publicou e adicionado ao grupo de conexão funciona como esperado.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-353">After you successfully publish both packages and enable the Connection Group, start the target Office 2016 application and verify that the plug-in you published and added to the connection group works as expected.</span></span>

### <a href="" id="bkmk-disable-office-apps"></a><span data-ttu-id="5ceb9-354">Desativando aplicativos do Office 2016</span><span class="sxs-lookup"><span data-stu-id="5ceb9-354">Disabling Office 2016 applications</span></span>

<span data-ttu-id="5ceb9-355">Você pode querer desabilitar aplicativos específicos em seu pacote do Office App-V.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-355">You may want to disable specific applications in your Office App-V package.</span></span> <span data-ttu-id="5ceb9-356">Por exemplo, você pode desabilitar o Access, mas deixar todos os outros aplicativos principais do Office disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-356">For instance, you can disable Access, but leave all other Office application main available.</span></span> <span data-ttu-id="5ceb9-357">Quando você desabilitar um aplicativo, o usuário final não verá mais o atalho para esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-357">When you disable an application, the end user will no longer see the shortcut for that application.</span></span> <span data-ttu-id="5ceb9-358">Não é necessário sequenciar novamente o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-358">You do not have to re-sequence the application.</span></span> <span data-ttu-id="5ceb9-359">Quando você altera o arquivo de configuração de implantação após a publicação do pacote do Office 2016 App-V, você salvará as alterações, adicionará o pacote do Office 2016 app-v e a publicará novamente com o novo arquivo de configuração de implantação para aplicar as novas configurações aos aplicativos do pacote do Office 2016 App-V.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-359">When you change the Deployment Configuration File after the Office 2016 App-V package has been published, you will save the changes, add the Office 2016 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2016 App-V Package applications.</span></span>

><span data-ttu-id="5ceb9-360">**Observação** Para excluir aplicativos específicos do Office (por exemplo, o Access e o InfoPath) quando você cria o pacote do App-V com a ferramenta de implantação do Office, use a configuração **ExcludeApp** .</span><span class="sxs-lookup"><span data-stu-id="5ceb9-360">**Note** To exclude specific Office applications (for example, Access and InfoPath) when you create the App-V package with the Office Deployment Tool, use the **ExcludeApp** setting.</span></span>


**<span data-ttu-id="5ceb9-361">Para desabilitar um aplicativo do Office 2016</span><span class="sxs-lookup"><span data-stu-id="5ceb9-361">To disable an Office 2016 application</span></span>**

1.  <span data-ttu-id="5ceb9-362">Abra um arquivo de configuração de implantação com um editor de texto, como o **bloco de notas** , e procure por "aplicativos".</span><span class="sxs-lookup"><span data-stu-id="5ceb9-362">Open a Deployment Configuration File with a text editor such as **Notepad** and search for “Applications."</span></span>

2.  <span data-ttu-id="5ceb9-363">Procure o aplicativo do Office que você deseja desabilitar, por exemplo, Access 2016.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-363">Search for the Office application you want to disable, for example, Access 2016.</span></span>

3.  <span data-ttu-id="5ceb9-364">Altere o valor de "Enabled" de "true" para "false".</span><span class="sxs-lookup"><span data-stu-id="5ceb9-364">Change the value of "Enabled" from "true" to "false."</span></span>

4.  <span data-ttu-id="5ceb9-365">Salve o arquivo de configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-365">Save the Deployment Configuration File.</span></span>

5.  <span data-ttu-id="5ceb9-366">Adicione o pacote do Office 2016 App-V com o novo arquivo de configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-366">Add the Office 2016 App-V Package with the new Deployment Configuration File.</span></span>

    ```xml
    <Application Id="[{AppVPackageRoot}]\office16\lync.exe" Enabled="true">
      <VisualElements>
        <Name>Lync 2016</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[(AppVPackageRoot}]\office16\MSACCESS.EXE" Enabled="true">
      <VisualElements>
        <Name>Access 2016</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    ```

6.  <span data-ttu-id="5ceb9-367">Adicione novamente o pacote do Office 2016 App-V e Republique-o com o novo arquivo de configuração de implantação para aplicar as novas configurações aos aplicativos do pacote do App-V do Office 2016.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-367">Re-add the Office 2016 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2016 App-V Package applications.</span></span>

### <a href="" id="bkmk-disable-shortcuts"></a><span data-ttu-id="5ceb9-368">Desativando atalhos do Office 2016</span><span class="sxs-lookup"><span data-stu-id="5ceb9-368">Disabling Office 2016 shortcuts</span></span>

<span data-ttu-id="5ceb9-369">Você pode querer desativar atalhos para determinados aplicativos do Office em vez de cancelar a publicação ou remoção do pacote.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-369">You may want to disable shortcuts for certain Office applications instead of unpublishing or removing the package.</span></span> <span data-ttu-id="5ceb9-370">O exemplo a seguir mostra como desabilitar atalhos para o Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-370">The following example shows how to disable shortcuts for Microsoft Access.</span></span>

**<span data-ttu-id="5ceb9-371">Para desativar atalhos para aplicativos do Office 2016</span><span class="sxs-lookup"><span data-stu-id="5ceb9-371">To disable shortcuts for Office 2016 applications</span></span>**

1.  <span data-ttu-id="5ceb9-372">Abra um arquivo de configuração de implantação no bloco de notas e procure por "atalhos".</span><span class="sxs-lookup"><span data-stu-id="5ceb9-372">Open a Deployment Configuration File in Notepad and search for “Shortcuts”.</span></span>

2.  <span data-ttu-id="5ceb9-373">Para desabilitar certos atalhos, exclua ou comente os atalhos específicos que você não quer.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-373">To disable certain shortcuts, delete or comment out the specific shortcuts you don’t want.</span></span> <span data-ttu-id="5ceb9-374">Você deve manter o subsistema presente e habilitado.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-374">You must keep the subsystem present and enabled.</span></span> <span data-ttu-id="5ceb9-375">Por exemplo, no exemplo a seguir, exclua os atalhos do Microsoft Access, enquanto mantém os subsistemas de &lt; atalho &gt; &lt; /Shortcut &gt; intactos para desabilitar o atalho do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-375">For example, in the example below, delete the Microsoft Access shortcuts, while keeping the subsystems &lt;shortcut&gt; &lt;/shortcut&gt; intact to disable the Microsoft Access shortcut.</span></span>

    ``` syntax
    Shortcuts

    -->
     <Shortcuts Enabled="true">
      <Extensions>
        <Extension Category="AppV.Shortcut">
          <Shortcut>
           <File>[{Common Programs}]\Microsoft Office 2016\Access 2016.lnk</File>
           <Target>[{AppvPackageRoot}])office16\MSACCESS.EXE</Target>
           <Icon>[{Windows}]\Installer\{90150000-000F-0000-0000-000000FF1CE)\accicons.exe.Ø.ico</Icon>
           <Arguments />
           <WorkingDirectory />
           <AppuserModelId>Microsoft.Office.MSACCESS.EXE.15</AppUserModelId>
           <AppUserModelExcludeFromShowInNewInstall>true</AppUserModelExcludeFromShowInNewInstall>
           <Description>Build a professional app quickly to manage data.</Description>
           <ShowCommand>l</ShowCommand>
           <ApplicationId>[{AppVPackageRoot}]\office16\MSACCESS.EXE</ApplicationId>
        </Shortcut>
    ```

3.  <span data-ttu-id="5ceb9-376">Salve o arquivo de configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-376">Save the Deployment Configuration File.</span></span>

4.  <span data-ttu-id="5ceb9-377">Republicar o pacote do Office 2016 App-V com novo arquivo de configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-377">Republish Office 2016 App-V Package with new Deployment Configuration File.</span></span>

<span data-ttu-id="5ceb9-378">Muitas configurações adicionais podem ser alteradas por meio da modificação da configuração de implantação para pacotes do App-V, por exemplo, associações de tipo de arquivo, sistema de arquivos virtual e muito mais.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-378">Many additional settings can be changed through modifying the Deployment Configuration for App-V packages, for example, file type associations, Virtual File System, and more.</span></span> <span data-ttu-id="5ceb9-379">Para obter informações adicionais sobre como usar arquivos de configuração de implantação para alterar as configurações do pacote do App-V, consulte a seção recursos adicionais no final deste documento.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-379">For additional information on how to use Deployment Configuration Files to change App-V package settings, refer to the additional resources section at the end of this document.</span></span>

### <a href="" id="bkmk-manage-office-pkg-upgrd"></a><span data-ttu-id="5ceb9-380">Gerenciando atualizações de pacote do Office 2016</span><span class="sxs-lookup"><span data-stu-id="5ceb9-380">Managing Office 2016 package upgrades</span></span>

<span data-ttu-id="5ceb9-381">Para atualizar um pacote do Office 2016, use a ferramenta de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-381">To upgrade an Office 2016 package, use the Office Deployment Tool.</span></span> <span data-ttu-id="5ceb9-382">Para atualizar um pacote do Office 2016 implantado anteriormente, siga as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-382">To upgrade a previously deployed Office 2016 package, perform the following steps.</span></span>

**<span data-ttu-id="5ceb9-383">Como atualizar um pacote do Office 2016 implantado anteriormente</span><span class="sxs-lookup"><span data-stu-id="5ceb9-383">How to upgrade a previously deployed Office 2016 package</span></span>**

1. <span data-ttu-id="5ceb9-384">Crie um novo pacote do Office 2016 por meio da ferramenta de implantação do Office que usa o software aplicativo mais recente do Office 2016.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-384">Create a new Office 2016 package through the Office Deployment Tool that uses the most recent Office 2016 application software.</span></span> <span data-ttu-id="5ceb9-385">Os bits mais recentes do Office 2016 sempre podem ser obtidos por meio do estágio de download da criação de um pacote do Office 2016 App-V.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-385">The most recent Office 2016 bits can always be obtained through the download stage of creating an Office 2016 App-V Package.</span></span> <span data-ttu-id="5ceb9-386">O pacote do Office 2016 recém-criado terá as atualizações mais recentes e uma nova ID de versão.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-386">The newly created Office 2016 package will have the most recent updates and a new Version ID.</span></span> <span data-ttu-id="5ceb9-387">Todos os pacotes criados usando a ferramenta de implantação do Office têm a mesma linhagem.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-387">All packages created using the Office Deployment Tool have the same lineage.</span></span>

   > <span data-ttu-id="5ceb9-388">**Observação** Os pacotes do Office App-V têm duas IDs de versão:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-388">**Note** Office App-V packages have two Version IDs:</span></span>
   > <ul>
   > <li><span data-ttu-id="5ceb9-389">Uma ID de versão do pacote do Office 2016 App-V que é exclusiva em todos os pacotes criados usando a ferramenta de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-389">An Office 2016 App-V Package Version ID that is unique across all packages created using the Office Deployment Tool.</span></span></li>
   > <li><span data-ttu-id="5ceb9-390">Uma segunda ID de versão do pacote do App-V, x. x. x. x por exemplo, no manifesto AppX que só será alterado se houver uma nova versão do Office.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-390">A second App-V Package Version ID, x.x.x.x for example, in the AppX manifest that will only change if there is a new version of Office itself.</span></span> <span data-ttu-id="5ceb9-391">Por exemplo, se uma nova versão do Office 2016 com atualizações estiver disponível e um pacote for criado por meio da ferramenta de implantação do Office para incorporar essas atualizações, a ID da versão X. x. x. X será alterada para refletir que a própria versão do Office mudou.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-391">For example, if a new Office 2016 release with upgrades is available, and a package is created through the Office Deployment Tool to incorporate these upgrades, the X.X.X.X version ID will change to reflect that the Office version itself has changed.</span></span> <span data-ttu-id="5ceb9-392">O servidor App-V usará a ID da versão x. x. x para diferenciar esse pacote e reconhecer que ele contém novas atualizações para o pacote publicado anteriormente e, como resultado, publicá-lo como uma atualização para o pacote existente do Office 2016.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-392">The App-V server will use the X.X.X.X version ID to differentiate this package and recognize that it contains new upgrades to the previously published package, and as a result, publish it as an upgrade to the existing Office 2016 package.</span></span></li>
   > </ul>


2. <span data-ttu-id="5ceb9-393">Publique globalmente os pacotes do Office 2016 App-V recém-criados em computadores onde você deseja aplicar as novas atualizações.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-393">Globally publish the newly created Office 2016 App-V Packages onto computers where you would like to apply the new updates.</span></span> <span data-ttu-id="5ceb9-394">Como o novo pacote tem a mesma linhagem do pacote mais antigo do Office 2016 App-V, publicar o novo pacote com as atualizações só aplicará as novas alterações ao pacote antigo e, portanto, será rápido.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-394">Since the new package has the same lineage of the older Office 2016 App-V Package, publishing the new package with the updates will only apply the new changes to the old package, and thus will be fast.</span></span>

3. <span data-ttu-id="5ceb9-395">As atualizações serão aplicadas da mesma maneira em qualquer pacote App-V publicado globalmente.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-395">Upgrades will be applied in the same manner of any globally published App-V Packages.</span></span> <span data-ttu-id="5ceb9-396">Como os aplicativos provavelmente estarão em uso, as atualizações podem ser adiadas até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-396">Because applications will probably be in use, upgrades might be delayed until the computer is rebooted.</span></span>


### <a href="" id="bkmk-deploy-visio-project"></a><span data-ttu-id="5ceb9-397">Implantação do Visio 2016 e do Project 2016 com o Office</span><span class="sxs-lookup"><span data-stu-id="5ceb9-397">Deploying Visio 2016 and Project 2016 with Office</span></span>

<span data-ttu-id="5ceb9-398">A tabela a seguir descreve os requisitos e as opções para a implantação do Visio 2016 e do Project 2016 com o Office.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-398">The following table describes the requirements and options for deploying Visio 2016 and Project 2016 with Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ceb9-399">Tarefa</span><span class="sxs-lookup"><span data-stu-id="5ceb9-399">Task</span></span></th>
<th align="left"><span data-ttu-id="5ceb9-400">Detalhes</span><span class="sxs-lookup"><span data-stu-id="5ceb9-400">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ceb9-401">Como faço para empacotar e publicar o Visio 2016 e o Project 2016 com o Office?</span><span class="sxs-lookup"><span data-stu-id="5ceb9-401">How do I package and publish Visio 2016 and Project 2016 with Office?</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ceb9-402">Você deve incluir o Visio 2016 e o Project 2016 no mesmo pacote com o Office.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-402">You must include Visio 2016 and Project 2016 in the same package with Office.</span></span></p>
<p><span data-ttu-id="5ceb9-403">Se você não estiver implantando o Office, poderá criar um pacote que contenha o Visio e/ou o Project, desde que siga os requisitos de empacotamento, publicação e implantação descritos neste tópico.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-403">If you aren’t deploying Office, you can create a package that contains Visio and/or Project, as long as you follow the packaging, publishing, and deployment requirements described in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ceb9-404">Como eu posso implantar o Visio 2016 e o Project 2016 para usuários específicos?</span><span class="sxs-lookup"><span data-stu-id="5ceb9-404">How can I deploy Visio 2016 and Project 2016 to specific users?</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ceb9-405">Use um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-405">Use one of the following methods:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ceb9-406">Se quiser...</span><span class="sxs-lookup"><span data-stu-id="5ceb9-406">If you want to...</span></span></th>
<th align="left"><span data-ttu-id="5ceb9-407">... em seguida, use esse método</span><span class="sxs-lookup"><span data-stu-id="5ceb9-407">...then use this method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ceb9-408">Crie dois pacotes diferentes e implante cada um deles em um grupo diferente de usuários</span><span class="sxs-lookup"><span data-stu-id="5ceb9-408">Create two different packages and deploy each one to a different group of users</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ceb9-409">Crie e implante os seguintes pacotes:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-409">Create and deploy the following packages:</span></span></p>
<ul>
<li><p><span data-ttu-id="5ceb9-410">Um pacote que contém apenas o Office-implantação em computadores cujos usuários precisam apenas do Office.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-410">A package that contains only Office - deploy to computers whose users need only Office.</span></span></p></li>
<li><p><span data-ttu-id="5ceb9-411">Um pacote que contém o Office, o Visio e o Project-implantação para computadores cujos usuários precisam de todos os três aplicativos.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-411">A package that contains Office, Visio, and Project - deploy to computers whose users need all three applications.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ceb9-412">Se você quiser apenas um pacote para a organização inteira, ou se tiver usuários que compartilham computadores:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-412">If you want only one package for the whole organization, or if you have users who share computers:</span></span></p></td>
<td align="left"><p><span data-ttu-id="5ceb9-413">Siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="5ceb9-413">Follows these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="5ceb9-414">Crie um pacote que contenha o Office, o Visio e o Project.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-414">Create a package that contains Office, Visio, and Project.</span></span></p></li>
<li><p><span data-ttu-id="5ceb9-415">Implante o pacote para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-415">Deploy the package to all users.</span></span></p></li>
<li><p><span data-ttu-id="5ceb9-416">Use <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)"> o Microsoft AppLocker </a> para impedir que usuários específicos usem o Visio e o Project.</span><span class="sxs-lookup"><span data-stu-id="5ceb9-416">Use <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)">Microsoft AppLocker</a> to prevent specific users from using Visio and Project.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="5ceb9-417">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="5ceb9-417">Additional resources</span></span>


[<span data-ttu-id="5ceb9-418">Implantando o Microsoft Office 2013 usando o App-V</span><span class="sxs-lookup"><span data-stu-id="5ceb9-418">Deploying Microsoft Office 2013 by Using App-V</span></span>](deploying-microsoft-office-2013-by-using-app-v.md)

[<span data-ttu-id="5ceb9-419">Implantando o Microsoft Office 2010 usando o App-V</span><span class="sxs-lookup"><span data-stu-id="5ceb9-419">Deploying Microsoft Office 2010 by Using App-V</span></span>](deploying-microsoft-office-2010-by-using-app-v.md)

[<span data-ttu-id="5ceb9-420">Ferramenta de implantação do Office 2016 para clique para executar</span><span class="sxs-lookup"><span data-stu-id="5ceb9-420">Office 2016 Deployment Tool for Click-to-Run</span></span>](https://www.microsoft.com/download/details.aspx?id=49117)

**<span data-ttu-id="5ceb9-421">Grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="5ceb9-421">Connection Groups</span></span>**

[<span data-ttu-id="5ceb9-422">Implantando grupos de conexão no Microsoft App-V V5</span><span class="sxs-lookup"><span data-stu-id="5ceb9-422">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="5ceb9-423">Gerenciando grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="5ceb9-423">Managing Connection Groups</span></span>](managing-connection-groups.md)

**<span data-ttu-id="5ceb9-424">Configuração dinâmica</span><span class="sxs-lookup"><span data-stu-id="5ceb9-424">Dynamic Configuration</span></span>**

[<span data-ttu-id="5ceb9-425">Sobre a configuração dinâmica do App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="5ceb9-425">About App-V 5.1 Dynamic Configuration</span></span>](about-app-v-51-dynamic-configuration.md)





