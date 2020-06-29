---
title: Implantando o Microsoft Office 2013 usando o App-V
description: Implantando o Microsoft Office 2013 usando o App-V
author: dansimp
ms.assetid: 02df5dc8-79e2-4c5c-8398-dbfb23344ab3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: c57227d531c61949f9160c27fc249db72dbc6523
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796548"
---
# <span data-ttu-id="f158c-103">Implantando o Microsoft Office 2013 usando o App-V</span><span class="sxs-lookup"><span data-stu-id="f158c-103">Deploying Microsoft Office 2013 by Using App-V</span></span>


<span data-ttu-id="f158c-104">Use as informações neste artigo para usar o Microsoft Application Virtualization 5,0 ou versões posteriores para fornecer o Microsoft Office 2013 como um aplicativo virtualizado para computadores em sua organização.</span><span class="sxs-lookup"><span data-stu-id="f158c-104">Use the information in this article to use Microsoft Application Virtualization 5.0, or later versions, to deliver Microsoft Office 2013 as a virtualized application to computers in your organization.</span></span> <span data-ttu-id="f158c-105">Para obter informações sobre como usar o App-V para fornecer o Office 2010, consulte [implantando o Microsoft Office 2010 usando o app-v](deploying-microsoft-office-2010-by-using-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="f158c-105">For information about using App-V to deliver Office 2010, see [Deploying Microsoft Office 2010 by Using App-V](deploying-microsoft-office-2010-by-using-app-v.md).</span></span> <span data-ttu-id="f158c-106">Para implantar com êxito o Office 2013 com o App-V, você precisa estar familiarizado com o Office 2013 e PP-V.</span><span class="sxs-lookup"><span data-stu-id="f158c-106">To successfully deploy Office 2013 with App-V, you need to be familiar with Office 2013 and pp-V.</span></span>

<span data-ttu-id="f158c-107">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="f158c-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="f158c-108">O que saber antes de começar</span><span class="sxs-lookup"><span data-stu-id="f158c-108">What to know before you start</span></span>](#bkmk-before-you-start)

-   [<span data-ttu-id="f158c-109">Criando um pacote do Office 2013 para o App-V com a ferramenta de implantação do Office</span><span class="sxs-lookup"><span data-stu-id="f158c-109">Creating an Office 2013 package for App-V with the Office Deployment Tool</span></span>](#bkmk-create-office-pkg)

-   [<span data-ttu-id="f158c-110">Publicando o pacote do Office para o App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="f158c-110">Publishing the Office package for App-V 5.0</span></span>](#bkmk-pub-pkg-office)

-   [<span data-ttu-id="f158c-111">Personalizando e gerenciando pacotes do Office App-V</span><span class="sxs-lookup"><span data-stu-id="f158c-111">Customizing and managing Office App-V packages</span></span>](#bkmk-custmz-manage-office-pkgs)

## <a href="" id="bkmk-before-you-start"></a><span data-ttu-id="f158c-112">O que saber antes de começar</span><span class="sxs-lookup"><span data-stu-id="f158c-112">What to know before you start</span></span>


<span data-ttu-id="f158c-113">Antes de implantar o Office 2013 usando o App-V, examine as informações de planejamento a seguir.</span><span class="sxs-lookup"><span data-stu-id="f158c-113">Before you deploy Office 2013 by using App-V, review the following planning information.</span></span>

### <a href="" id="bkmk-supp-vers-coexist"></a><span data-ttu-id="f158c-114">Versões do Office com suporte e coexistência do Office</span><span class="sxs-lookup"><span data-stu-id="f158c-114">Supported Office versions and Office coexistence</span></span>

<span data-ttu-id="f158c-115">Use a tabela a seguir para obter informações sobre as versões compatíveis do Office e sobre como executar versões coexistentes do Office.</span><span class="sxs-lookup"><span data-stu-id="f158c-115">Use the following table to get information about supported versions of Office and about running coexisting versions of Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f158c-116">Informações a serem revisadas</span><span class="sxs-lookup"><span data-stu-id="f158c-116">Information to review</span></span></th>
<th align="left"><span data-ttu-id="f158c-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="f158c-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv" data-raw-source="[Planning for Using App-V with Office](planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv)"><span data-ttu-id="f158c-118">Planejando o uso do App-V com o Office</span><span class="sxs-lookup"><span data-stu-id="f158c-118">Planning for Using App-V with Office</span></span></a></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f158c-119">Versões com suporte do Office</span><span class="sxs-lookup"><span data-stu-id="f158c-119">Supported versions of Office</span></span></p></li>
<li><p><span data-ttu-id="f158c-120">Tipos de implantação com suporte (por exemplo, área de trabalho, infraestrutura de área de trabalho virtual pessoal (VDI), VDI em pool)</span><span class="sxs-lookup"><span data-stu-id="f158c-120">Supported deployment types (for example, desktop, personal Virtual Desktop Infrastructure (VDI), pooled VDI)</span></span></p></li>
<li><p><span data-ttu-id="f158c-121">Opções de licenciamento do Office</span><span class="sxs-lookup"><span data-stu-id="f158c-121">Office licensing options</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-plan-coexisting" data-raw-source="[Planning for Using App-V with Office](planning-for-using-app-v-with-office.md#bkmk-plan-coexisting)"><span data-ttu-id="f158c-122">Planejando o uso do App-V com o Office</span><span class="sxs-lookup"><span data-stu-id="f158c-122">Planning for Using App-V with Office</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="f158c-123">Considerações para a instalação de diferentes versões do Office no mesmo computador</span><span class="sxs-lookup"><span data-stu-id="f158c-123">Considerations for installing different versions of Office on the same computer</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pkg-pub-reqs"></a><span data-ttu-id="f158c-124">Requisitos de empacotamento, publicação e implantação</span><span class="sxs-lookup"><span data-stu-id="f158c-124">Packaging, publishing, and deployment requirements</span></span>

<span data-ttu-id="f158c-125">Antes de implantar o Office usando o App-V, examine os seguintes requisitos.</span><span class="sxs-lookup"><span data-stu-id="f158c-125">Before you deploy Office by using App-V, review the following requirements.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f158c-126">Tarefa</span><span class="sxs-lookup"><span data-stu-id="f158c-126">Task</span></span></th>
<th align="left"><span data-ttu-id="f158c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f158c-127">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f158c-128">Embalagem</span><span class="sxs-lookup"><span data-stu-id="f158c-128">Packaging</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f158c-129">Todos os aplicativos do Office que você deseja implantar para os usuários devem estar em um único pacote.</span><span class="sxs-lookup"><span data-stu-id="f158c-129">All of the Office applications that you want to deploy to users must be in a single package.</span></span></p></li>
<li><p><span data-ttu-id="f158c-130">No App-V 5,0 e posterior, você deve usar a ferramenta de implantação do Office para criar pacotes.</span><span class="sxs-lookup"><span data-stu-id="f158c-130">In App-V 5.0 and later, you must use the Office Deployment Tool to create packages.</span></span> <span data-ttu-id="f158c-131">Não é possível usar o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="f158c-131">You cannot use the Sequencer.</span></span></p></li>
<li><p><span data-ttu-id="f158c-132">Se você estiver implantando o Microsoft Visio 2013 e o Microsoft Project 2013 juntamente com o Office, deverá incluí-los no mesmo pacote com o Office.</span><span class="sxs-lookup"><span data-stu-id="f158c-132">If you are deploying Microsoft Visio 2013 and Microsoft Project 2013 along with Office, you must include them in the same package with Office.</span></span> <span data-ttu-id="f158c-133">Para obter mais informações, consulte <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2013 and Project 2013 with Office](#bkmk-deploy-visio-project)"> implantação do Visio 2013 e do Project 2013 com o Office </a> .</span><span class="sxs-lookup"><span data-stu-id="f158c-133">For more information, see <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2013 and Project 2013 with Office](#bkmk-deploy-visio-project)">Deploying Visio 2013 and Project 2013 with Office</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f158c-134">Publicação</span><span class="sxs-lookup"><span data-stu-id="f158c-134">Publishing</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f158c-135">Você pode publicar apenas um pacote do Office em cada computador cliente.</span><span class="sxs-lookup"><span data-stu-id="f158c-135">You can publish only one Office package to each client computer.</span></span></p></li>
<li><p><span data-ttu-id="f158c-136">Você deve publicar o pacote do Office globalmente.</span><span class="sxs-lookup"><span data-stu-id="f158c-136">You must publish the Office package globally.</span></span> <span data-ttu-id="f158c-137">Você não pode publicar para o usuário.</span><span class="sxs-lookup"><span data-stu-id="f158c-137">You cannot publish to the user.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f158c-138">Implantando qualquer um dos seguintes produtos em um computador compartilhado, por exemplo, usando serviços de área de trabalho remota:</span><span class="sxs-lookup"><span data-stu-id="f158c-138">Deploying any of the following products to a shared computer, for example, by using Remote Desktop Services:</span></span></p>
<ul>
<li><p><span data-ttu-id="f158c-139">Aplicativos do Microsoft 365 para empresas</span><span class="sxs-lookup"><span data-stu-id="f158c-139">Microsoft 365 Apps for enterprise</span></span></p></li>
<li><p><span data-ttu-id="f158c-140">Visio pro para Office 365</span><span class="sxs-lookup"><span data-stu-id="f158c-140">Visio Pro for Office 365</span></span></p></li>
<li><p><span data-ttu-id="f158c-141">Project pro para Office 365</span><span class="sxs-lookup"><span data-stu-id="f158c-141">Project Pro for Office 365</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="f158c-142">Você deve habilitar a <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)"> ativação de computador compartilhado </a> .</span><span class="sxs-lookup"><span data-stu-id="f158c-142">You must enable <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)">shared computer activation</a>.</span></span></p>
<p><span data-ttu-id="f158c-143">Você não usará a ativação de computador compartilhado se estiver implantando um produto licenciado por volume, como:</span><span class="sxs-lookup"><span data-stu-id="f158c-143">You don’t use shared computer activation if you’re deploying a volume licensed product, such as:</span></span></p>
<ul>
<li><p><span data-ttu-id="f158c-144">Office Professional Plus 2013</span><span class="sxs-lookup"><span data-stu-id="f158c-144">Office Professional Plus 2013</span></span></p></li>
<li><p><span data-ttu-id="f158c-145">Visio Professional 2013</span><span class="sxs-lookup"><span data-stu-id="f158c-145">Visio Professional 2013</span></span></p></li>
<li><p><span data-ttu-id="f158c-146">Project Professional 2013</span><span class="sxs-lookup"><span data-stu-id="f158c-146">Project Professional 2013</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="f158c-147">Excluindo aplicativos do Office de um pacote</span><span class="sxs-lookup"><span data-stu-id="f158c-147">Excluding Office applications from a package</span></span>

<span data-ttu-id="f158c-148">A tabela a seguir descreve os métodos recomendados para excluir aplicativos específicos do Office de um pacote.</span><span class="sxs-lookup"><span data-stu-id="f158c-148">The following table describes the recommended methods for excluding specific Office applications from a package.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f158c-149">Tarefa</span><span class="sxs-lookup"><span data-stu-id="f158c-149">Task</span></span></th>
<th align="left"><span data-ttu-id="f158c-150">Detalhes</span><span class="sxs-lookup"><span data-stu-id="f158c-150">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f158c-151">Use a <strong> </strong> configuração ExcludeApp quando você cria o pacote usando a ferramenta de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="f158c-151">Use the <strong>ExcludeApp</strong> setting when you create the package by using the Office Deployment Tool.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f158c-152">Permite que você exclua aplicativos específicos do Office do pacote quando a ferramenta de implantação do Office cria o pacote.</span><span class="sxs-lookup"><span data-stu-id="f158c-152">Enables you to exclude specific Office applications from the package when the Office Deployment Tool creates the package.</span></span> <span data-ttu-id="f158c-153">Por exemplo, você pode usar essa configuração para criar um pacote que contenha apenas o Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="f158c-153">For example, you can use this setting to create a package that contains only Microsoft Word.</span></span></p></li>
<li><p><span data-ttu-id="f158c-154">Para obter mais informações, consulte o <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)"> elemento ExcludeApp </a> .</span><span class="sxs-lookup"><span data-stu-id="f158c-154">For more information, see <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)">ExcludeApp element</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f158c-155">Modificar o arquivo DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="f158c-155">Modify the DeploymentConfig.xml file</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f158c-156">Modifique o arquivo DeploymentConfig.xml após a criação do pacote.</span><span class="sxs-lookup"><span data-stu-id="f158c-156">Modify the DeploymentConfig.xml file after the package has been created.</span></span> <span data-ttu-id="f158c-157">Esse arquivo contém as configurações padrão do pacote para todos os usuários em um computador que esteja executando o cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="f158c-157">This file contains the default package settings for all users on a computer that is running the App-V Client.</span></span></p></li>
<li><p><span data-ttu-id="f158c-158">Para obter mais informações, consulte <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2013 applications](#bkmk-disable-office-apps)"> desabilitando aplicativos do Office 2013 </a> .</span><span class="sxs-lookup"><span data-stu-id="f158c-158">For more information, see <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2013 applications](#bkmk-disable-office-apps)">Disabling Office 2013 applications</a>.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-create-office-pkg"></a><span data-ttu-id="f158c-159">Criando um pacote do Office 2013 para o App-V com a ferramenta de implantação do Office</span><span class="sxs-lookup"><span data-stu-id="f158c-159">Creating an Office 2013 package for App-V with the Office Deployment Tool</span></span>


<span data-ttu-id="f158c-160">Conclua as etapas a seguir para criar um pacote do Office 2013 para o App-V 5,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="f158c-160">Complete the following steps to create an Office 2013 package for App-V 5.0 or later.</span></span>

**<span data-ttu-id="f158c-161">Importante</span><span class="sxs-lookup"><span data-stu-id="f158c-161">Important</span></span>**  
<span data-ttu-id="f158c-162">No App-V 5,0 e posterior, você deve ter a ferramenta de implantação do Office para criar um pacote.</span><span class="sxs-lookup"><span data-stu-id="f158c-162">In App-V 5.0 and later, you must the Office Deployment Tool to create a package.</span></span> <span data-ttu-id="f158c-163">Você não pode usar o sequenciador para criar pacotes.</span><span class="sxs-lookup"><span data-stu-id="f158c-163">You cannot use the Sequencer to create packages.</span></span>


### <span data-ttu-id="f158c-164">Revisar os pré-requisitos para usar a ferramenta de implantação do Office</span><span class="sxs-lookup"><span data-stu-id="f158c-164">Review prerequisites for using the Office Deployment Tool</span></span>

<span data-ttu-id="f158c-165">O computador no qual você está instalando a ferramenta de implantação do Office deve ter:</span><span class="sxs-lookup"><span data-stu-id="f158c-165">The computer on which you are installing the Office Deployment Tool must have:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f158c-166">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="f158c-166">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="f158c-167">Descrição</span><span class="sxs-lookup"><span data-stu-id="f158c-167">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f158c-168">Software de pré-requisito</span><span class="sxs-lookup"><span data-stu-id="f158c-168">Prerequisite software</span></span></p></td>
<td align="left"><p><span data-ttu-id="f158c-169">.NET Framework 4</span><span class="sxs-lookup"><span data-stu-id="f158c-169">.Net Framework 4</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f158c-170">Sistemas operacionais compatíveis</span><span class="sxs-lookup"><span data-stu-id="f158c-170">Supported operating systems</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f158c-171">versão de 64 bits do Windows 8</span><span class="sxs-lookup"><span data-stu-id="f158c-171">64-bit version of Windows 8</span></span></p></li>
<li><p><span data-ttu-id="f158c-172">versão de 64 bits do Windows 7</span><span class="sxs-lookup"><span data-stu-id="f158c-172">64-bit version of Windows 7</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


**<span data-ttu-id="f158c-173">Observação</span><span class="sxs-lookup"><span data-stu-id="f158c-173">Note</span></span>**  
<span data-ttu-id="f158c-174">Neste tópico, o termo "Office 2013 App-V Package" refere-se ao licenciamento de assinatura e licenciamento por volume.</span><span class="sxs-lookup"><span data-stu-id="f158c-174">In this topic, the term “Office 2013 App-V package” refers to subscription licensing and volume licensing.</span></span>


### <span data-ttu-id="f158c-175">Criar pacotes do Office 2013 App-V usando a ferramenta de implantação do Office</span><span class="sxs-lookup"><span data-stu-id="f158c-175">Create Office 2013 App-V Packages Using Office Deployment Tool</span></span>

<span data-ttu-id="f158c-176">Você cria pacotes do Office 2013 App-V usando a ferramenta de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="f158c-176">You create Office 2013 App-V packages by using the Office Deployment Tool.</span></span> <span data-ttu-id="f158c-177">As instruções a seguir explicam como criar um pacote do Office 2013 App-V com licenciamento por volume ou licenciamento de assinatura.</span><span class="sxs-lookup"><span data-stu-id="f158c-177">The following instructions explain how to create an Office 2013 App-V package with Volume Licensing or Subscription Licensing.</span></span>

<span data-ttu-id="f158c-178">Crie pacotes do Office 2013 App-V em computadores com Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f158c-178">Create Office 2013 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="f158c-179">Uma vez criado, o pacote do Office 2013 App-V será executado em computadores com o Windows 7 e o Windows 7 e o Windows 8 bit 32 e 64.</span><span class="sxs-lookup"><span data-stu-id="f158c-179">Once created, the Office 2013 App-V package will run on 32-bit and 64-bit Windows 7 and Windows 8 computers.</span></span>

### <span data-ttu-id="f158c-180">Baixar a ferramenta de implantação do Office</span><span class="sxs-lookup"><span data-stu-id="f158c-180">Download the Office Deployment Tool</span></span>

<span data-ttu-id="f158c-181">Os pacotes do Office 2013 App-V são criados usando a ferramenta de implantação do Office, que gera um pacote do Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="f158c-181">Office 2013 App-V Packages are created using the Office Deployment Tool, which generates an Office 2013 App-V Package.</span></span> <span data-ttu-id="f158c-182">O pacote não pode ser criado ou modificado por meio do sequenciador App-V.</span><span class="sxs-lookup"><span data-stu-id="f158c-182">The package cannot be created or modified through the App-V sequencer.</span></span> <span data-ttu-id="f158c-183">Para começar a criação de pacotes:</span><span class="sxs-lookup"><span data-stu-id="f158c-183">To begin package creation:</span></span>

1.  <span data-ttu-id="f158c-184">Baixe a [ferramenta de implantação do Office para clique para executar](https://www.microsoft.com/download/details.aspx?id=36778).</span><span class="sxs-lookup"><span data-stu-id="f158c-184">Download the [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/download/details.aspx?id=36778).</span></span>

2.  <span data-ttu-id="f158c-185">Execute o arquivo. exe e extraia seus recursos para o local desejado.</span><span class="sxs-lookup"><span data-stu-id="f158c-185">Run the .exe file and extract its features into the desired location.</span></span> <span data-ttu-id="f158c-186">Para facilitar esse processo, você pode criar uma pasta de rede compartilhada na qual os recursos serão salvos.</span><span class="sxs-lookup"><span data-stu-id="f158c-186">To make this process easier, you can create a shared network folder where the features will be saved.</span></span>

    <span data-ttu-id="f158c-187">Exemplo: \\\\Server\\Office2013</span><span class="sxs-lookup"><span data-stu-id="f158c-187">Example: \\\\Server\\Office2013</span></span>

3.  <span data-ttu-id="f158c-188">Verifique se há um setup.exe e um arquivo configuration.xml e se estão no local especificado.</span><span class="sxs-lookup"><span data-stu-id="f158c-188">Check that a setup.exe and a configuration.xml file exist and are in the location you specified.</span></span>

### <span data-ttu-id="f158c-189">Baixar aplicativos do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f158c-189">Download Office 2013 applications</span></span>

<span data-ttu-id="f158c-190">Depois de baixar a ferramenta de implantação do Office, você pode usá-la para obter os aplicativos mais recentes do Office 2013.</span><span class="sxs-lookup"><span data-stu-id="f158c-190">After you download the Office Deployment Tool, you can use it to get the latest Office 2013 applications.</span></span> <span data-ttu-id="f158c-191">Depois de obter os aplicativos do Office, crie o pacote do Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="f158c-191">After getting the Office applications, you create the Office 2013 App-V package.</span></span>

<span data-ttu-id="f158c-192">O arquivo XML que está incluído na ferramenta de implantação do Office especifica os detalhes do produto, como os idiomas e os aplicativos do Office incluídos.</span><span class="sxs-lookup"><span data-stu-id="f158c-192">The XML file that is included in the Office Deployment Tool specifies the product details, such as the languages and Office applications included.</span></span>

1. <span data-ttu-id="f158c-193">**Personalize o arquivo de configuração XML de exemplo:** Use o arquivo de configuração XML de exemplo que você baixou com a ferramenta de implantação do Office para personalizar os aplicativos do Office:</span><span class="sxs-lookup"><span data-stu-id="f158c-193">**Customize the sample XML configuration file:** Use the sample XML configuration file that you downloaded with the Office Deployment Tool to customize the Office applications:</span></span>

   1. <span data-ttu-id="f158c-194">Abra o arquivo XML de exemplo no bloco de notas ou no seu editor de texto favorito.</span><span class="sxs-lookup"><span data-stu-id="f158c-194">Open the sample XML file in Notepad or your favorite text editor.</span></span>

   2. <span data-ttu-id="f158c-195">Com o exemplo configuration.xml arquivo aberto e pronto para edição, você pode especificar produtos, idiomas e o caminho para o qual você salva os aplicativos do Office 2013.</span><span class="sxs-lookup"><span data-stu-id="f158c-195">With the sample configuration.xml file open and ready for editing, you can specify products, languages, and the path to which you save the Office 2013 applications.</span></span> <span data-ttu-id="f158c-196">Veja a seguir um exemplo básico do arquivo configuration.xml:</span><span class="sxs-lookup"><span data-stu-id="f158c-196">The following is a basic example of the configuration.xml file:</span></span>

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

      **<span data-ttu-id="f158c-197">Observação</span><span class="sxs-lookup"><span data-stu-id="f158c-197">Note</span></span>**  
      <span data-ttu-id="f158c-198">O XML de configuração é um arquivo XML de exemplo.</span><span class="sxs-lookup"><span data-stu-id="f158c-198">The configuration XML is a sample XML file.</span></span> <span data-ttu-id="f158c-199">O arquivo inclui linhas que foram comentadas. Você pode "remover o comentário" dessas linhas para personalizar as configurações adicionais com o arquivo.</span><span class="sxs-lookup"><span data-stu-id="f158c-199">The file includes lines that are commented out. You can “uncomment” these lines to customize additional settings with the file.</span></span>

      <span data-ttu-id="f158c-200">O arquivo de configuração XML acima Especifica que o Office 2013 ProPlus 32-bit Edition, incluindo o Visio ProPlus, será baixado em inglês para o \\\\server\\Office 2013, que é o local onde os aplicativos do Office serão salvos.</span><span class="sxs-lookup"><span data-stu-id="f158c-200">The above XML configuration file specifies that Office 2013 ProPlus 32-bit edition, including Visio ProPlus, will be downloaded in English to the \\\\server\\Office 2013, which is the location where Office applications will be saved to.</span></span> <span data-ttu-id="f158c-201">Observe que a ID do produto dos aplicativos não afetará o licenciamento final do Office.</span><span class="sxs-lookup"><span data-stu-id="f158c-201">Note that the Product ID of the applications will not affect the final licensing of Office.</span></span> <span data-ttu-id="f158c-202">Os pacotes do Office 2013 App-V com várias licenças podem ser criados a partir dos mesmos aplicativos por meio da especificação de licenciamento em um estágio posterior.</span><span class="sxs-lookup"><span data-stu-id="f158c-202">Office 2013 App-V packages with various licensing can be created from the same applications through specifying licensing in a later stage.</span></span> <span data-ttu-id="f158c-203">A tabela a seguir resume os atributos e elementos personalizáveis do arquivo XML:</span><span class="sxs-lookup"><span data-stu-id="f158c-203">The table below summarizes the customizable attributes and elements of XML file:</span></span>

      <table>
      <colgroup>
      <col width="33%" />
      <col width="33%" />
      <col width="33%" />
      </colgroup>
      <thead>
      <tr class="header">
      <th align="left"><span data-ttu-id="f158c-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="f158c-204">Input</span></span></th>
      <th align="left"><span data-ttu-id="f158c-205">Descrição</span><span class="sxs-lookup"><span data-stu-id="f158c-205">Description</span></span></th>
      <th align="left"><span data-ttu-id="f158c-206">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f158c-206">Example</span></span></th>
      </tr>
      </thead>
      <tbody>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="f158c-207">Adicionar elemento</span><span class="sxs-lookup"><span data-stu-id="f158c-207">Add element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="f158c-208">Especifica os produtos e idiomas a serem incluídos no pacote.</span><span class="sxs-lookup"><span data-stu-id="f158c-208">Specifies the products and languages to include in the package.</span></span></p></td>
      <td align="left"><p><span data-ttu-id="f158c-209">N/A</span><span class="sxs-lookup"><span data-stu-id="f158c-209">N/A</span></span></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="f158c-210">OfficeClientEdition (atributo do elemento add)</span><span class="sxs-lookup"><span data-stu-id="f158c-210">OfficeClientEdition (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="f158c-211">Especifica a edição do produto do Office 2013 a ser usado: 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f158c-211">Specifies the edition of Office 2013 product to use: 32-bit or 64-bit.</span></span> <span data-ttu-id="f158c-212">A operação falhará se <strong> OfficeClientEdition </strong> não estiver definido como um valor válido.</span><span class="sxs-lookup"><span data-stu-id="f158c-212">The operation fails if <strong>OfficeClientEdition</strong> is not set to a valid value.</span></span></p></td>
      <td align="left"><p><strong><span data-ttu-id="f158c-213">OfficeClientEdition </strong> = &quot; 32&quot;</span><span class="sxs-lookup"><span data-stu-id="f158c-213">OfficeClientEdition</strong>=&quot;32&quot;</span></span></p>
      <p><strong><span data-ttu-id="f158c-214">OfficeClientEdition </strong> = &quot; 64&quot;</span><span class="sxs-lookup"><span data-stu-id="f158c-214">OfficeClientEdition</strong>=&quot;64&quot;</span></span></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="f158c-215">Elemento Product</span><span class="sxs-lookup"><span data-stu-id="f158c-215">Product element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="f158c-216">Especifica o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f158c-216">Specifies the application.</span></span> <span data-ttu-id="f158c-217">O Project 2013 e o Visio 2013 devem ser especificados aqui como um produto adicionado a ser incluído nos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f158c-217">Project 2013 and Visio 2013 must be specified here as an added product to be included in the applications.</span></span></p></td>
      <td align="left"><p><code>Product ID =&quot;O365ProPlusRetail &quot;</code></p>
      <p><code>Product ID =&quot;VisioProRetail&quot;</code></p>
      <p><code>Product ID =&quot;ProjectProRetail&quot;</code></p>
      <p><code>Product ID =&quot;ProPlusVolume&quot;</code></p>
      <p><code>Product ID =&quot;VisioProVolume&quot;</code></p>
      <p><code>Product ID = &quot;ProjectProVolume&quot;</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="f158c-218">Elemento de linguagem</span><span class="sxs-lookup"><span data-stu-id="f158c-218">Language element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="f158c-219">Especifica o idioma com suporte nos aplicativos</span><span class="sxs-lookup"><span data-stu-id="f158c-219">Specifies the language supported in the applications</span></span></p></td>
      <td align="left"><p><code>Language ID=&quot;en-us&quot;</code></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="f158c-220">Versão (atributo do elemento add)</span><span class="sxs-lookup"><span data-stu-id="f158c-220">Version (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="f158c-221">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f158c-221">Optional.</span></span> <span data-ttu-id="f158c-222">Especifica uma compilação a ser usada para o pacote</span><span class="sxs-lookup"><span data-stu-id="f158c-222">Specifies a build to use for the package</span></span></p>
      <p><span data-ttu-id="f158c-223">O padrão é a compilação anunciada mais recente (conforme definido no v32.CAB na origem do Office).</span><span class="sxs-lookup"><span data-stu-id="f158c-223">Defaults to latest advertised build (as defined in v32.CAB at the Office source).</span></span></p></td>
      <td align="left"><p><code>15.1.2.3</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="f158c-224">Caminho_de_origem (atributo do elemento add)</span><span class="sxs-lookup"><span data-stu-id="f158c-224">SourcePath (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="f158c-225">Especifica o local em que os aplicativos serão salvos.</span><span class="sxs-lookup"><span data-stu-id="f158c-225">Specifies the location in which the applications will be saved to.</span></span></p></td>
      <td align="left"><p><code>Sourcepath = &quot;\Server\Office2013”</code></p></td>
      </tr>
      </tbody>
      </table>

      <span data-ttu-id="f158c-226">Depois de editar o arquivo configuration.xml para especificar o produto desejado, os idiomas e também o local em que os aplicativos do Office 2013 serão salvos, você poderá salvar o arquivo de configuração, por exemplo, como Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="f158c-226">After editing the configuration.xml file to specify the desired product, languages, and also the location which the Office 2013 applications will be saved onto, you can save the configuration file, for example, as Customconfig.xml.</span></span>

2. <span data-ttu-id="f158c-227">**Baixe os aplicativos para o local especificado:** Use um prompt de comando elevado e um sistema operacional de 64 bits para baixar os aplicativos do Office 2013 que serão convertidos posteriormente em um pacote do App-V.</span><span class="sxs-lookup"><span data-stu-id="f158c-227">**Download the applications into the specified location:** Use an elevated command prompt and a 64 bit operating system to download the Office 2013 applications that will later be converted into an App-V package.</span></span> <span data-ttu-id="f158c-228">Veja a seguir um exemplo de comando com a descrição de detalhes:</span><span class="sxs-lookup"><span data-stu-id="f158c-228">Below is an example command with description of details:</span></span>

   ``` syntax
   \\server\Office2013\setup.exe /download \\server\Office2013\Customconfig.xml
   ```

   <span data-ttu-id="f158c-229">No exemplo:</span><span class="sxs-lookup"><span data-stu-id="f158c-229">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f158c-230">\server\Office2013</span><span class="sxs-lookup"><span data-stu-id="f158c-230">\server\Office2013</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f158c-231">é o local de compartilhamento de rede que contém a ferramenta de implantação do Office e o arquivo de Configuration.xml personalizado Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="f158c-231">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="f158c-232">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="f158c-232">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f158c-233">é a ferramenta de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="f158c-233">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f158c-234">/Download</span><span class="sxs-lookup"><span data-stu-id="f158c-234">/download</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f158c-235">baixa os aplicativos do Office 2013 que você especificar no arquivo customConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="f158c-235">downloads the Office 2013 applications that you specify in the customConfig.xml file.</span></span> <span data-ttu-id="f158c-236">Esses bits podem ser convertidos posteriormente em um pacote do Office 2013 App-V com licenciamento por volume.</span><span class="sxs-lookup"><span data-stu-id="f158c-236">These bits can be later converted in an Office 2013 App-V package with Volume Licensing.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="f158c-237">\server\Office2013\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="f158c-237">\server\Office2013\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f158c-238">passa o arquivo de configuração XML necessário para concluir o processo de download, neste exemplo, customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="f158c-238">passes the XML configuration file required to complete the download process, in this example, customconfig.xml.</span></span> <span data-ttu-id="f158c-239">Depois de usar o comando download, os aplicativos do Office devem ser encontrados no local especificado no arquivo XML de configuração, neste exemplo \Server\Office2013.</span><span class="sxs-lookup"><span data-stu-id="f158c-239">After using the download command, Office applications should be found in the location specified in the configuration xml file, in this example \Server\Office2013.</span></span></p></td>
   </tr>
   </tbody>
   </table>



### <span data-ttu-id="f158c-240">Converter os aplicativos do Office em um pacote do App-V</span><span class="sxs-lookup"><span data-stu-id="f158c-240">Convert the Office applications into an App-V package</span></span>

<span data-ttu-id="f158c-241">Depois de baixar os aplicativos do Office 2013 por meio da ferramenta de implantação do Office, use a ferramenta de implantação do Office para convertê-los em um pacote do Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="f158c-241">After you download the Office 2013 applications through the Office Deployment Tool, use the Office Deployment Tool to convert them into an Office 2013 App-V package.</span></span> <span data-ttu-id="f158c-242">Conclua as etapas que correspondem ao seu modelo de licenciamento.</span><span class="sxs-lookup"><span data-stu-id="f158c-242">Complete the steps that correspond to your licensing model.</span></span>

**<span data-ttu-id="f158c-243">Resumo do que você precisará fazer:</span><span class="sxs-lookup"><span data-stu-id="f158c-243">Summary of what you’ll need to do:</span></span>**

-   <span data-ttu-id="f158c-244">Crie os pacotes do Office 2013 App-V em computadores com Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f158c-244">Create the Office 2013 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="f158c-245">No entanto, o pacote será executado 32 em computadores 64 com o Windows 7 e o Windows 8-bit Windows 7 e Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f158c-245">However, the package will run on 32-bit and 64-bit Windows 7 and Windows 8 computers.</span></span>

-   <span data-ttu-id="f158c-246">Crie um pacote do Office App-V para o pacote de licenciamento de assinatura ou o licenciamento por volume usando a ferramenta de implantação do Office e modifique o arquivo de configuração do CustomConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="f158c-246">Create an Office App-V package for either Subscription Licensing package or Volume Licensing by using the Office Deployment Tool, and then modify the CustomConfig.xml configuration file.</span></span>

    <span data-ttu-id="f158c-247">A tabela a seguir resume os valores que você precisa inserir no arquivo CustomConfig.xml para o modelo de licenciamento que você está usando.</span><span class="sxs-lookup"><span data-stu-id="f158c-247">The following table summarizes the values you need to enter in the CustomConfig.xml file for the licensing model you’re using.</span></span> <span data-ttu-id="f158c-248">As etapas nas seções que seguem a tabela especificarão as entradas exatas que você precisa fazer.</span><span class="sxs-lookup"><span data-stu-id="f158c-248">The steps in the sections that follow the table will specify the exact entries you need to make.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f158c-249">ID do Produto (Product ID)</span><span class="sxs-lookup"><span data-stu-id="f158c-249">Product ID</span></span></th>
<th align="left"><span data-ttu-id="f158c-250">Licenciamento por volume</span><span class="sxs-lookup"><span data-stu-id="f158c-250">Volume Licensing</span></span></th>
<th align="left"><span data-ttu-id="f158c-251">Licenciamento de assinatura</span><span class="sxs-lookup"><span data-stu-id="f158c-251">Subscription Licensing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f158c-252">Office 2013</span><span class="sxs-lookup"><span data-stu-id="f158c-252">Office 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f158c-253">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="f158c-253">ProPlusVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="f158c-254">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="f158c-254">O365ProPlusRetail</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f158c-255">Office 2013 com Visio 2013</span><span class="sxs-lookup"><span data-stu-id="f158c-255">Office 2013 with Visio 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f158c-256">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="f158c-256">ProPlusVolume</span></span></p>
<p><span data-ttu-id="f158c-257">VisioProVolume</span><span class="sxs-lookup"><span data-stu-id="f158c-257">VisioProVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="f158c-258">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="f158c-258">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="f158c-259">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="f158c-259">VisioProRetail</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f158c-260">Office 2013 com Visio 2013 e Project 2013</span><span class="sxs-lookup"><span data-stu-id="f158c-260">Office 2013 with Visio 2013 and Project 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f158c-261">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="f158c-261">ProPlusVolume</span></span></p>
<p><span data-ttu-id="f158c-262">VisioProVolume</span><span class="sxs-lookup"><span data-stu-id="f158c-262">VisioProVolume</span></span></p>
<p><span data-ttu-id="f158c-263">ProjectProVolume</span><span class="sxs-lookup"><span data-stu-id="f158c-263">ProjectProVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="f158c-264">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="f158c-264">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="f158c-265">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="f158c-265">VisioProRetail</span></span></p>
<p><span data-ttu-id="f158c-266">ProjectProRetail</span><span class="sxs-lookup"><span data-stu-id="f158c-266">ProjectProRetail</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="f158c-267">Como converter os aplicativos do Office em um pacote do App-V</span><span class="sxs-lookup"><span data-stu-id="f158c-267">How to convert the Office applications into an App-V package</span></span>**

1. <span data-ttu-id="f158c-268">No bloco de notas, abra novamente o arquivo CustomConfig.xml e faça as seguintes alterações no arquivo:</span><span class="sxs-lookup"><span data-stu-id="f158c-268">In Notepad, reopen the CustomConfig.xml file, and make the following changes to the file:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f158c-269">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="f158c-269">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="f158c-270">O que alterar o valor para</span><span class="sxs-lookup"><span data-stu-id="f158c-270">What to change the value to</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f158c-271">SourcePath</span><span class="sxs-lookup"><span data-stu-id="f158c-271">SourcePath</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f158c-272">Aponte para os aplicativos do Office baixados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f158c-272">Point to the Office applications downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f158c-273">ProductID</span><span class="sxs-lookup"><span data-stu-id="f158c-273">ProductID</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f158c-274">Especifique o tipo de licenciamento, conforme mostrado nos exemplos a seguir:</span><span class="sxs-lookup"><span data-stu-id="f158c-274">Specify the type of licensing, as shown in the following examples:</span></span></p>
   <ul>
   <li><p><span data-ttu-id="f158c-275">Licenciamento de assinatura</span><span class="sxs-lookup"><span data-stu-id="f158c-275">Subscription Licensing</span></span></p>
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
   <p><span data-ttu-id="f158c-276">Neste exemplo, foram feitas as seguintes alterações para criar um pacote com licenciamento de assinatura:</span><span class="sxs-lookup"><span data-stu-id="f158c-276">In this example, the following changes were made to create a package with Subscription licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f158c-277">SourcePath</span><span class="sxs-lookup"><span data-stu-id="f158c-277">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f158c-278">é o caminho, que foi alterado para apontar para os aplicativos do Office que foram baixados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f158c-278">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="f158c-279">ID do Produto (Product ID)</span><span class="sxs-lookup"><span data-stu-id="f158c-279">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f158c-280">para o Office foi alterado para <code>O365ProPlusRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="f158c-280">for Office was changed to <code>O365ProPlusRetail</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f158c-281">ID do Produto (Product ID)</span><span class="sxs-lookup"><span data-stu-id="f158c-281">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f158c-282">para o Visio foi alterado para <code>VisioProRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="f158c-282">for Visio was changed to <code>VisioProRetail</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p>
   <p></p></li>
   <li><p><span data-ttu-id="f158c-283">Licenciamento por volume</span><span class="sxs-lookup"><span data-stu-id="f158c-283">Volume Licensing</span></span></p>
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
   <p><span data-ttu-id="f158c-284">Neste exemplo, foram feitas as seguintes alterações para criar um pacote com licenciamento por volume:</span><span class="sxs-lookup"><span data-stu-id="f158c-284">In this example, the following changes were made to create a package with Volume licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f158c-285">SourcePath</span><span class="sxs-lookup"><span data-stu-id="f158c-285">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f158c-286">é o caminho, que foi alterado para apontar para os aplicativos do Office que foram baixados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f158c-286">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="f158c-287">ID do Produto (Product ID)</span><span class="sxs-lookup"><span data-stu-id="f158c-287">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f158c-288">para o Office foi alterado para <code>ProPlusVolume</code> .</span><span class="sxs-lookup"><span data-stu-id="f158c-288">for Office was changed to <code>ProPlusVolume</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f158c-289">ID do Produto (Product ID)</span><span class="sxs-lookup"><span data-stu-id="f158c-289">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f158c-290">para o Visio foi alterado para <code>VisioProVolume</code> .</span><span class="sxs-lookup"><span data-stu-id="f158c-290">for Visio was changed to <code>VisioProVolume</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p>
   <p></p></li>
   </ul></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f158c-291">ExcludeApp (opcional)</span><span class="sxs-lookup"><span data-stu-id="f158c-291">ExcludeApp (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f158c-292">Permite especificar os programas do Office que você não deseja incluir no pacote do App-V que a ferramenta de implantação do Office cria.</span><span class="sxs-lookup"><span data-stu-id="f158c-292">Lets you specify Office programs that you don’t want included in the App-V package that the Office Deployment Tool creates.</span></span> <span data-ttu-id="f158c-293">Por exemplo, você pode excluir o Access e o InfoPath.</span><span class="sxs-lookup"><span data-stu-id="f158c-293">For example, you can exclude Access and InfoPath.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f158c-294">PACKAGEGUID (opcional)</span><span class="sxs-lookup"><span data-stu-id="f158c-294">PACKAGEGUID (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f158c-295">Por padrão, todos os pacotes do App-V criados pela ferramenta de implantação do Office compartilham a mesma ID de pacote do App-V.</span><span class="sxs-lookup"><span data-stu-id="f158c-295">By default, all App-V packages created by the Office Deployment Tool share the same App-V Package ID.</span></span> <span data-ttu-id="f158c-296">Você pode usar PACKAGEGUID para especificar uma ID de pacote diferente para cada pacote, que permite publicar vários pacotes do App-V, criados pela ferramenta de implantação do Office e gerenciá-los usando o servidor App-V.</span><span class="sxs-lookup"><span data-stu-id="f158c-296">You can use PACKAGEGUID to specify a different package ID for each package, which allows you to publish multiple App-V packages, created by the Office Deployment Tool, and manage them by using the App-V Server.</span></span></p>
   <p><span data-ttu-id="f158c-297">Um exemplo de quando usar esse parâmetro é se você cria pacotes diferentes para usuários diferentes.</span><span class="sxs-lookup"><span data-stu-id="f158c-297">An example of when to use this parameter is if you create different packages for different users.</span></span> <span data-ttu-id="f158c-298">Por exemplo, você pode criar um pacote com apenas o Office 2013 para alguns usuários e criar outro pacote com o Office 2013 e o Visio 2013 para outro conjunto de usuários.</span><span class="sxs-lookup"><span data-stu-id="f158c-298">For example, you can create a package with just Office 2013 for some users, and create another package with Office 2013 and Visio 2013 for another set of users.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="f158c-299">Observação</span><span class="sxs-lookup"><span data-stu-id="f158c-299">Note</span></span></strong><br/><p><span data-ttu-id="f158c-300">Mesmo que você use IDs de pacote exclusivas, ainda é possível implantar apenas um pacote do App-V para um único dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f158c-300">Even if you use unique package IDs, you can still deploy only one App-V package to a single device.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="f158c-301">Use o comando/Packager para converter os aplicativos do Office em um pacote do Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="f158c-301">Use the /packager command to convert the Office applications to an Office 2013 App-V package.</span></span>

   <span data-ttu-id="f158c-302">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f158c-302">For example:</span></span>

   ``` syntax
   \\server\Office2013\setup.exe /packager \\server\Office2013\Customconfig.xml  \\server\share\Office2013AppV
   ```

   <span data-ttu-id="f158c-303">No exemplo:</span><span class="sxs-lookup"><span data-stu-id="f158c-303">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f158c-304">\server\Office2013</span><span class="sxs-lookup"><span data-stu-id="f158c-304">\server\Office2013</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f158c-305">é o local de compartilhamento de rede que contém a ferramenta de implantação do Office e o arquivo de Configuration.xml personalizado Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="f158c-305">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="f158c-306">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="f158c-306">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f158c-307">é a ferramenta de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="f158c-307">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f158c-308">/packager</span><span class="sxs-lookup"><span data-stu-id="f158c-308">/packager</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f158c-309">cria o pacote do Office 2013 App-V com licenciamento por volume conforme especificado no arquivo customConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="f158c-309">creates the Office 2013 App-V package with Volume Licensing as specified in the customConfig.xml file.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="f158c-310">\server\Office2013\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="f158c-310">\server\Office2013\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f158c-311">passa o arquivo XML de configuração (neste caso, customConfig) que foi preparado para o estágio de empacotamento.</span><span class="sxs-lookup"><span data-stu-id="f158c-311">passes the configuration XML file (in this case customConfig) that has been prepared for the packaging stage.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f158c-312">\server\share\Office 2013AppV</span><span class="sxs-lookup"><span data-stu-id="f158c-312">\server\share\Office 2013AppV</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f158c-313">Especifica o local do pacote do Office App-V recém-criado.</span><span class="sxs-lookup"><span data-stu-id="f158c-313">specifies the location of the newly created Office App-V package.</span></span></p></td>
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



3. <span data-ttu-id="f158c-314">Verifique se o pacote do Office 2013 App-V funciona corretamente:</span><span class="sxs-lookup"><span data-stu-id="f158c-314">Verify that the Office 2013 App-V package works correctly:</span></span>

   1.  <span data-ttu-id="f158c-315">Publique o pacote do Office 2013 App-V, que você criou globalmente, em um computador de teste e verifique se os atalhos do Office 2013 são exibidos.</span><span class="sxs-lookup"><span data-stu-id="f158c-315">Publish the Office 2013 App-V package, which you created globally, to a test computer, and verify that the Office 2013 shortcuts appear.</span></span>

   2.  <span data-ttu-id="f158c-316">Inicie alguns aplicativos do Office 2013, como o Excel ou o Word, para garantir que o pacote esteja funcionando conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="f158c-316">Start a few Office 2013 applications, such as Excel or Word, to ensure that your package is working as expected.</span></span>

## <a href="" id="bkmk-pub-pkg-office"></a><span data-ttu-id="f158c-317">Publicando o pacote do Office para o App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="f158c-317">Publishing the Office package for App-V 5.0</span></span>


<span data-ttu-id="f158c-318">Use as informações a seguir para publicar um pacote do Office.</span><span class="sxs-lookup"><span data-stu-id="f158c-318">Use the following information to publish an Office package.</span></span>

### <span data-ttu-id="f158c-319">Métodos para publicar pacotes do Office App-V</span><span class="sxs-lookup"><span data-stu-id="f158c-319">Methods for publishing Office App-V packages</span></span>

<span data-ttu-id="f158c-320">Implante o pacote do App-V para o Office 2013 usando os mesmos métodos que você usa para qualquer outro pacote:</span><span class="sxs-lookup"><span data-stu-id="f158c-320">Deploy the App-V package for Office 2013 by using the same methods you use for any other package:</span></span>

-   <span data-ttu-id="f158c-321">System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f158c-321">System Center Configuration Manager</span></span>

-   <span data-ttu-id="f158c-322">Servidor do App-V</span><span class="sxs-lookup"><span data-stu-id="f158c-322">App-V Server</span></span>

-   <span data-ttu-id="f158c-323">Autônomos por meio de comandos do PowerShell</span><span class="sxs-lookup"><span data-stu-id="f158c-323">Stand-alone through PowerShell commands</span></span>

### <span data-ttu-id="f158c-324">Como publicar pré-requisitos e requisitos</span><span class="sxs-lookup"><span data-stu-id="f158c-324">Publishing prerequisites and requirements</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f158c-325">Pré-requisito ou requisito</span><span class="sxs-lookup"><span data-stu-id="f158c-325">Prerequisite or requirement</span></span></th>
<th align="left"><span data-ttu-id="f158c-326">Detalhes</span><span class="sxs-lookup"><span data-stu-id="f158c-326">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f158c-327">Habilitar o script do PowerShell nos clientes do App-V</span><span class="sxs-lookup"><span data-stu-id="f158c-327">Enable PowerShell scripting on the App-V clients</span></span></p></td>
<td align="left"><p><span data-ttu-id="f158c-328">Para publicar pacotes do Office 2013, você deve executar um script.</span><span class="sxs-lookup"><span data-stu-id="f158c-328">To publish Office 2013 packages, you must run a script.</span></span></p>
<p><span data-ttu-id="f158c-329">Os scripts de pacote são desativados por padrão em clientes App-V.</span><span class="sxs-lookup"><span data-stu-id="f158c-329">Package scripts are disabled by default on App-V clients.</span></span> <span data-ttu-id="f158c-330">Para habilitar o script, execute o seguinte comando do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="f158c-330">To enable scripting, run the following PowerShell command:</span></span></p>
<pre class="syntax" space="preserve"><code>Set-AppvClientConfiguration –EnablePackageScripts 1</code></pre></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f158c-331">Publicar o pacote do Office 2013 globalmente</span><span class="sxs-lookup"><span data-stu-id="f158c-331">Publish the Office 2013 package globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="f158c-332">Os pontos de extensão no pacote App-V do Office exigem instalação no nível do computador.</span><span class="sxs-lookup"><span data-stu-id="f158c-332">Extension points in the Office App-V package require installation at the computer level.</span></span></p>
<p><span data-ttu-id="f158c-333">Quando você publica no nível do computador, não são necessárias ações de pré-requisito ou redistribuíveis, e o pacote do Office 2013 permite que seus aplicativos funcionem como o Office instalado nativamente, eliminando a necessidade de os administradores personalizarem pacotes.</span><span class="sxs-lookup"><span data-stu-id="f158c-333">When you publish at the computer level, no prerequisite actions or redistributables are needed, and the Office 2013 package globally enables its applications to work like natively installed Office, eliminating the need for administrators to customize packages.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="f158c-334">Como publicar um pacote do Office</span><span class="sxs-lookup"><span data-stu-id="f158c-334">How to publish an Office package</span></span>

<span data-ttu-id="f158c-335">Execute o seguinte comando para publicar um pacote do Office globalmente:</span><span class="sxs-lookup"><span data-stu-id="f158c-335">Run the following command to publish an Office package globally:</span></span>

-   `Add-AppvClientPackage <Path_to_AppV_Package> | Publish-AppvClientPackage –global`

-   <span data-ttu-id="f158c-336">No console de gerenciamento da Web no App-V Server, você pode adicionar permissões a um grupo de computadores em vez de a um grupo de usuários para permitir que os pacotes sejam publicados globalmente nos computadores do grupo correspondente.</span><span class="sxs-lookup"><span data-stu-id="f158c-336">From the Web Management Console on the App-V Server, you can add permissions to a group of computers instead of to a user group to enable packages to be published globally to the computers in the corresponding group.</span></span>

## <a href="" id="bkmk-custmz-manage-office-pkgs"></a><span data-ttu-id="f158c-337">Personalizando e gerenciando pacotes do Office App-V</span><span class="sxs-lookup"><span data-stu-id="f158c-337">Customizing and managing Office App-V packages</span></span>


<span data-ttu-id="f158c-338">Para gerenciar seus pacotes do Office App-V, use as mesmas operações que faria para qualquer outro pacote, mas há algumas exceções, como descrito nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="f158c-338">To manage your Office App-V packages, use the same operations as you would for any other package, but there are a few exceptions, as outlined in the following sections.</span></span>

-   [<span data-ttu-id="f158c-339">Habilitando plug-ins do Office usando grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="f158c-339">Enabling Office plug-ins by using connection groups</span></span>](#bkmk-enable-office-plugins)

-   [<span data-ttu-id="f158c-340">Desativando aplicativos do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f158c-340">Disabling Office 2013 applications</span></span>](#bkmk-disable-office-apps)

-   [<span data-ttu-id="f158c-341">Desativando atalhos do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f158c-341">Disabling Office 2013 shortcuts</span></span>](#bkmk-disable-shortcuts)

-   [<span data-ttu-id="f158c-342">Gerenciando atualizações de pacote do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f158c-342">Managing Office 2013 package upgrades</span></span>](#bkmk-manage-office-pkg-upgrd)

-   [<span data-ttu-id="f158c-343">Gerenciando atualizações de licenciamento do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f158c-343">Managing Office 2013 licensing upgrades</span></span>](#bkmk-manage-office-lic-upgrd)

-   [<span data-ttu-id="f158c-344">Implantação do Visio 2013 e do Project 2013 com o Office</span><span class="sxs-lookup"><span data-stu-id="f158c-344">Deploying Visio 2013 and Project 2013 with Office</span></span>](#bkmk-deploy-visio-project)

### <a href="" id="bkmk-enable-office-plugins"></a><span data-ttu-id="f158c-345">Habilitando plug-ins do Office usando grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="f158c-345">Enabling Office plug-ins by using connection groups</span></span>

<span data-ttu-id="f158c-346">Use as etapas desta seção para habilitar os plug-ins do Office com o pacote do Office.</span><span class="sxs-lookup"><span data-stu-id="f158c-346">Use the steps in this section to enable Office plug-ins with your Office package.</span></span> <span data-ttu-id="f158c-347">Para usar os plug-ins do Office, você deve usar o sequenciador do App-V para criar um pacote separado que contenha apenas os plug-ins. Não é possível usar a ferramenta de implantação do Office para criar o pacote de plug-ins.</span><span class="sxs-lookup"><span data-stu-id="f158c-347">To use Office plug-ins, you must use the App-V Sequencer to create a separate package that contains just the plug-ins. You cannot use the Office Deployment Tool to create the plug-ins package.</span></span> <span data-ttu-id="f158c-348">Em seguida, crie um grupo de conexão que contenha o pacote de plug-ins e o pacote do Office, conforme descrito nas etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="f158c-348">You then create a connection group that contains the Office package and the plug-ins package, as described in the following steps.</span></span>

**<span data-ttu-id="f158c-349">Para habilitar plug-ins para pacotes do Office App-V</span><span class="sxs-lookup"><span data-stu-id="f158c-349">To enable plug-ins for Office App-V packages</span></span>**

1.  <span data-ttu-id="f158c-350">Adicione um grupo de conexão por meio do App-V Server, do System Center Configuration Manager ou de um cmdlet do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f158c-350">Add a Connection Group through App-V Server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

2.  <span data-ttu-id="f158c-351">Sequenciar seus plug-ins usando o sequenciador do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f158c-351">Sequence your plug-ins using the App-V 5.0 Sequencer.</span></span> <span data-ttu-id="f158c-352">Verifique se o Office 2013 está instalado no computador que está sendo usado para sequenciar o plug-in.</span><span class="sxs-lookup"><span data-stu-id="f158c-352">Ensure that Office 2013 is installed on the computer being used to sequence the plug-in.</span></span> <span data-ttu-id="f158c-353">É recomendável usar os aplicativos do Microsoft 365 para empresas (não virtuais) no computador de sequenciamento quando você sequenciar plug-ins do Office 2013.</span><span class="sxs-lookup"><span data-stu-id="f158c-353">It is recommended you use Microsoft 365 Apps for enterprise(non-virtual) on the sequencing computer when you sequence Office 2013 plug-ins.</span></span>

3.  <span data-ttu-id="f158c-354">Crie um pacote do App-V 5,0 que inclua os plug-ins desejados.</span><span class="sxs-lookup"><span data-stu-id="f158c-354">Create an App-V 5.0 package that includes the desired plug-ins.</span></span>

4.  <span data-ttu-id="f158c-355">Adicione um grupo de conexão por meio do App-V Server, do System Center Configuration Manager ou de um cmdlet do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f158c-355">Add a Connection Group through App-V server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

5.  <span data-ttu-id="f158c-356">Adicione o pacote do Office 2013 App-V e o pacote de plug-ins que você sequenciaou ao grupo de conexão que você criou.</span><span class="sxs-lookup"><span data-stu-id="f158c-356">Add the Office 2013 App-V package and the plug-ins package you sequenced to the Connection Group you created.</span></span>

    **<span data-ttu-id="f158c-357">Importante</span><span class="sxs-lookup"><span data-stu-id="f158c-357">Important</span></span>**  
    <span data-ttu-id="f158c-358">A ordem dos pacotes no grupo de conexão determina a ordem em que o conteúdo do pacote é mesclado.</span><span class="sxs-lookup"><span data-stu-id="f158c-358">The order of the packages in the Connection Group determines the order in which the package contents are merged.</span></span> <span data-ttu-id="f158c-359">No arquivo do descritor de grupo de conexão, adicione o pacote do Office 2013 App-V primeiro e, em seguida, adicione o pacote do plug-in App-V.</span><span class="sxs-lookup"><span data-stu-id="f158c-359">In your Connection group descriptor file, add the Office 2013 App-V package first, and then add the plug-in App-V package.</span></span>



6.  <span data-ttu-id="f158c-360">Certifique-se de que os dois pacotes sejam publicados no computador de destino e que o pacote de plug-in seja publicado globalmente para corresponder às configurações globais do pacote do Office 2013 App-V publicado.</span><span class="sxs-lookup"><span data-stu-id="f158c-360">Ensure that both packages are published to the target computer and that the plug-in package is published globally to match the global settings of the published Office 2013 App-V package.</span></span>

7.  <span data-ttu-id="f158c-361">Verifique se o arquivo de configuração de implantação do pacote de plug-in tem as mesmas configurações que o pacote do Office 2013 App-V tem.</span><span class="sxs-lookup"><span data-stu-id="f158c-361">Verify that the Deployment Configuration File of the plug-in package has the same settings that the Office 2013 App-V package has.</span></span>

    <span data-ttu-id="f158c-362">Como o pacote do Office 2013 App-V está integrado ao sistema operacional, as configurações do pacote de plug-in devem coincidir.</span><span class="sxs-lookup"><span data-stu-id="f158c-362">Since the Office 2013 App-V package is integrated with the operating system, the plug-in package settings should match.</span></span> <span data-ttu-id="f158c-363">Você pode pesquisar o arquivo de configuração de implantação para "modo COM" e garantir que o pacote de plug-ins tenha esse valor definido como "integrado" e que "InProcessEnabled" e "OutOfProcessEnabled" correspondam às configurações do pacote do Office 2013 App-V que você publicou.</span><span class="sxs-lookup"><span data-stu-id="f158c-363">You can search the Deployment Configuration File for “COM Mode” and ensure that your plug-ins package has that value set as “Integrated” and that both "InProcessEnabled" and "OutOfProcessEnabled" match the settings of the Office 2013 App-V package you published.</span></span>

8.  <span data-ttu-id="f158c-364">Abra o arquivo de configuração de implantação e defina o valor de **objetos habilitados** como **falso**.</span><span class="sxs-lookup"><span data-stu-id="f158c-364">Open the Deployment Configuration File and set the value for **Objects Enabled** to **false**.</span></span>

9.  <span data-ttu-id="f158c-365">Se você fez qualquer alteração no arquivo de configuração de implantação após o sequenciamento, verifique se o pacote de plug-in é publicado com o arquivo.</span><span class="sxs-lookup"><span data-stu-id="f158c-365">If you made any changes to the Deployment Configuration file after sequencing, ensure that the plug-in package is published with the file.</span></span>

10. <span data-ttu-id="f158c-366">Verifique se o grupo de conexão que você criou está habilitado no computador desejado.</span><span class="sxs-lookup"><span data-stu-id="f158c-366">Ensure that the Connection Group you created is enabled onto your desired computer.</span></span> <span data-ttu-id="f158c-367">O grupo de conexão criado provavelmente será "pendente" se o pacote do Office 2013 App-V estiver em uso quando o grupo de conexão estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="f158c-367">The Connection Group created will likely “pend” if the Office 2013 App-V package is in use when the Connection Group is enabled.</span></span> <span data-ttu-id="f158c-368">Se isso acontecer, será necessário reinicializar para habilitar o grupo de conexão com êxito.</span><span class="sxs-lookup"><span data-stu-id="f158c-368">If that happens, you have to reboot to successfully enable the Connection Group.</span></span>

11. <span data-ttu-id="f158c-369">Depois de publicar com êxito os dois pacotes e habilitar o grupo de conexão, inicie o aplicativo de destino do Office 2013 e verifique se o plug-in que você publicou e adicionado ao grupo de conexão funciona como esperado.</span><span class="sxs-lookup"><span data-stu-id="f158c-369">After you successfully publish both packages and enable the Connection Group, start the target Office 2013 application and verify that the plug-in you published and added to the connection group works as expected.</span></span>

### <a href="" id="bkmk-disable-office-apps"></a><span data-ttu-id="f158c-370">Desativando aplicativos do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f158c-370">Disabling Office 2013 applications</span></span>

<span data-ttu-id="f158c-371">Você pode querer desabilitar aplicativos específicos em seu pacote do Office App-V.</span><span class="sxs-lookup"><span data-stu-id="f158c-371">You may want to disable specific applications in your Office App-V package.</span></span> <span data-ttu-id="f158c-372">Por exemplo, você pode desabilitar o Access, mas deixar todos os outros aplicativos principais do Office disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f158c-372">For instance, you can disable Access, but leave all other Office application main available.</span></span> <span data-ttu-id="f158c-373">Quando você desabilitar um aplicativo, o usuário final não verá mais o atalho para esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f158c-373">When you disable an application, the end user will no longer see the shortcut for that application.</span></span> <span data-ttu-id="f158c-374">Não é necessário sequenciar novamente o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f158c-374">You do not have to re-sequence the application.</span></span> <span data-ttu-id="f158c-375">Quando você altera o arquivo de configuração de implantação após a publicação do pacote do Office 2013 App-V, você salvará as alterações, adicionará o pacote do Office 2013 app-v e a publicará novamente com o novo arquivo de configuração de implantação para aplicar as novas configurações aos aplicativos do pacote do Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="f158c-375">When you change the Deployment Configuration File after the Office 2013 App-V package has been published, you will save the changes, add the Office 2013 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2013 App-V Package applications.</span></span>

**<span data-ttu-id="f158c-376">Observação</span><span class="sxs-lookup"><span data-stu-id="f158c-376">Note</span></span>**  
<span data-ttu-id="f158c-377">Para excluir aplicativos específicos do Office (por exemplo, o Access e o InfoPath) quando você cria o pacote do App-V com a ferramenta de implantação do Office, use a configuração **ExcludeApp** .</span><span class="sxs-lookup"><span data-stu-id="f158c-377">To exclude specific Office applications (for example, Access and InfoPath) when you create the App-V package with the Office Deployment Tool, use the **ExcludeApp** setting.</span></span> <span data-ttu-id="f158c-378">Para obter mais informações, consulte [referência para o arquivo de configuration.xml clique para executar](https://technet.microsoft.com/library/jj219426.aspx).</span><span class="sxs-lookup"><span data-stu-id="f158c-378">For more information, see [Reference for Click-to-Run configuration.xml file](https://technet.microsoft.com/library/jj219426.aspx).</span></span>



**<span data-ttu-id="f158c-379">Para desabilitar um aplicativo do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f158c-379">To disable an Office 2013 application</span></span>**

1.  <span data-ttu-id="f158c-380">Abra um arquivo de configuração de implantação com um editor de texto, como o **bloco de notas** , e procure por "aplicativos".</span><span class="sxs-lookup"><span data-stu-id="f158c-380">Open a Deployment Configuration File with a text editor such as **Notepad** and search for “Applications."</span></span>

2.  <span data-ttu-id="f158c-381">Procure o aplicativo do Office que você deseja desabilitar, por exemplo, Access 2013.</span><span class="sxs-lookup"><span data-stu-id="f158c-381">Search for the Office application you want to disable, for example, Access 2013.</span></span>

3.  <span data-ttu-id="f158c-382">Altere o valor de "Enabled" de "true" para "false".</span><span class="sxs-lookup"><span data-stu-id="f158c-382">Change the value of "Enabled" from "true" to "false."</span></span>

4.  <span data-ttu-id="f158c-383">Salve o arquivo de configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="f158c-383">Save the Deployment Configuration File.</span></span>

5.  <span data-ttu-id="f158c-384">Adicione o pacote do Office 2013 App-V com o novo arquivo de configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="f158c-384">Add the Office 2013 App-V Package with the new Deployment Configuration File.</span></span>

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

6.  <span data-ttu-id="f158c-385">Adicione novamente o pacote do Office 2013 App-V e Republique-o com o novo arquivo de configuração de implantação para aplicar as novas configurações aos aplicativos do pacote do App-V do Office 2013.</span><span class="sxs-lookup"><span data-stu-id="f158c-385">Re-add the Office 2013 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2013 App-V Package applications.</span></span>

### <a href="" id="bkmk-disable-shortcuts"></a><span data-ttu-id="f158c-386">Desativando atalhos do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f158c-386">Disabling Office 2013 shortcuts</span></span>

<span data-ttu-id="f158c-387">Você pode querer desativar atalhos para determinados aplicativos do Office em vez de cancelar a publicação ou remoção do pacote.</span><span class="sxs-lookup"><span data-stu-id="f158c-387">You may want to disable shortcuts for certain Office applications instead of unpublishing or removing the package.</span></span> <span data-ttu-id="f158c-388">O exemplo a seguir mostra como desabilitar atalhos para o Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f158c-388">The following example shows how to disable shortcuts for Microsoft Access.</span></span>

**<span data-ttu-id="f158c-389">Para desativar atalhos para aplicativos do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f158c-389">To disable shortcuts for Office 2013 applications</span></span>**

1.  <span data-ttu-id="f158c-390">Abra um arquivo de configuração de implantação no bloco de notas e procure por "atalhos".</span><span class="sxs-lookup"><span data-stu-id="f158c-390">Open a Deployment Configuration File in Notepad and search for “Shortcuts”.</span></span>

2.  <span data-ttu-id="f158c-391">Para desabilitar certos atalhos, exclua ou comente os atalhos específicos que você não quer.</span><span class="sxs-lookup"><span data-stu-id="f158c-391">To disable certain shortcuts, delete or comment out the specific shortcuts you don’t want.</span></span> <span data-ttu-id="f158c-392">Você deve manter o subsistema presente e habilitado.</span><span class="sxs-lookup"><span data-stu-id="f158c-392">You must keep the subsystem present and enabled.</span></span> <span data-ttu-id="f158c-393">Por exemplo, no exemplo a seguir, exclua os atalhos do Microsoft Access, enquanto mantém os subsistemas de &lt; atalho &gt; &lt; /Shortcut &gt; intactos para desabilitar o atalho do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f158c-393">For example, in the example below, delete the Microsoft Access shortcuts, while keeping the subsystems &lt;shortcut&gt; &lt;/shortcut&gt; intact to disable the Microsoft Access shortcut.</span></span>

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

3.  <span data-ttu-id="f158c-394">Salve o arquivo de configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="f158c-394">Save the Deployment Configuration File.</span></span>

4.  <span data-ttu-id="f158c-395">Republicar o pacote do Office 2013 App-V com novo arquivo de configuração de implantação.</span><span class="sxs-lookup"><span data-stu-id="f158c-395">Republish Office 2013 App-V Package with new Deployment Configuration File.</span></span>

<span data-ttu-id="f158c-396">Muitas configurações adicionais podem ser alteradas por meio da modificação da configuração de implantação para pacotes do App-V, por exemplo, associações de tipo de arquivo, sistema de arquivos virtual e muito mais.</span><span class="sxs-lookup"><span data-stu-id="f158c-396">Many additional settings can be changed through modifying the Deployment Configuration for App-V packages, for example, file type associations, Virtual File System, and more.</span></span> <span data-ttu-id="f158c-397">Para obter informações adicionais sobre como usar arquivos de configuração de implantação para alterar as configurações do pacote do App-V, consulte a seção recursos adicionais no final deste documento.</span><span class="sxs-lookup"><span data-stu-id="f158c-397">For additional information on how to use Deployment Configuration Files to change App-V package settings, refer to the additional resources section at the end of this document.</span></span>

### <a href="" id="bkmk-manage-office-pkg-upgrd"></a><span data-ttu-id="f158c-398">Gerenciando atualizações de pacote do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f158c-398">Managing Office 2013 package upgrades</span></span>

<span data-ttu-id="f158c-399">Para atualizar um pacote do Office 2013, use a ferramenta de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="f158c-399">To upgrade an Office 2013 package, use the Office Deployment Tool.</span></span> <span data-ttu-id="f158c-400">Para atualizar um pacote do Office 2013 implantado anteriormente, siga as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="f158c-400">To upgrade a previously deployed Office 2013 package, perform the following steps.</span></span>

**<span data-ttu-id="f158c-401">Como atualizar um pacote do Office 2013 implantado anteriormente</span><span class="sxs-lookup"><span data-stu-id="f158c-401">How to upgrade a previously deployed Office 2013 package</span></span>**

1.  <span data-ttu-id="f158c-402">Crie um novo pacote do Office 2013 por meio da ferramenta de implantação do Office que usa o software aplicativo mais recente do Office 2013.</span><span class="sxs-lookup"><span data-stu-id="f158c-402">Create a new Office 2013 package through the Office Deployment Tool that uses the most recent Office 2013 application software.</span></span> <span data-ttu-id="f158c-403">Os bits mais recentes do Office 2013 sempre podem ser obtidos por meio do estágio de download da criação de um pacote do Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="f158c-403">The most recent Office 2013 bits can always be obtained through the download stage of creating an Office 2013 App-V Package.</span></span> <span data-ttu-id="f158c-404">O pacote do Office 2013 recém-criado terá as atualizações mais recentes e uma nova ID de versão.</span><span class="sxs-lookup"><span data-stu-id="f158c-404">The newly created Office 2013 package will have the most recent updates and a new Version ID.</span></span> <span data-ttu-id="f158c-405">Todos os pacotes criados usando a ferramenta de implantação do Office têm a mesma linhagem.</span><span class="sxs-lookup"><span data-stu-id="f158c-405">All packages created using the Office Deployment Tool have the same lineage.</span></span>

    **<span data-ttu-id="f158c-406">Observação</span><span class="sxs-lookup"><span data-stu-id="f158c-406">Note</span></span>**  
    <span data-ttu-id="f158c-407">Os pacotes do Office App-V têm duas IDs de versão:</span><span class="sxs-lookup"><span data-stu-id="f158c-407">Office App-V packages have two Version IDs:</span></span>

    -   <span data-ttu-id="f158c-408">Uma ID de versão do pacote do Office 2013 App-V que é exclusiva em todos os pacotes criados usando a ferramenta de implantação do Office.</span><span class="sxs-lookup"><span data-stu-id="f158c-408">An Office 2013 App-V Package Version ID that is unique across all packages created using the Office Deployment Tool.</span></span>

    -   <span data-ttu-id="f158c-409">Uma segunda ID de versão do pacote do App-V, x. x. x. x por exemplo, no manifesto AppX que só será alterado se houver uma nova versão do Office.</span><span class="sxs-lookup"><span data-stu-id="f158c-409">A second App-V Package Version ID, x.x.x.x for example, in the AppX manifest that will only change if there is a new version of Office itself.</span></span> <span data-ttu-id="f158c-410">Por exemplo, se uma nova versão do Office 2013 com atualizações estiver disponível e um pacote for criado por meio da ferramenta de implantação do Office para incorporar essas atualizações, a ID da versão X. x. x. X será alterada para refletir que a própria versão do Office mudou.</span><span class="sxs-lookup"><span data-stu-id="f158c-410">For example, if a new Office 2013 release with upgrades is available, and a package is created through the Office Deployment Tool to incorporate these upgrades, the X.X.X.X version ID will change to reflect that the Office version itself has changed.</span></span> <span data-ttu-id="f158c-411">O servidor App-V usará a ID da versão x. x. x para diferenciar esse pacote e reconhecer que ele contém novas atualizações para o pacote publicado anteriormente e, como resultado, publicá-lo como uma atualização para o pacote existente do Office 2013.</span><span class="sxs-lookup"><span data-stu-id="f158c-411">The App-V server will use the X.X.X.X version ID to differentiate this package and recognize that it contains new upgrades to the previously published package, and as a result, publish it as an upgrade to the existing Office 2013 package.</span></span>



2.  <span data-ttu-id="f158c-412">Publique globalmente os pacotes do Office 2013 App-V recém-criados em computadores onde você deseja aplicar as novas atualizações.</span><span class="sxs-lookup"><span data-stu-id="f158c-412">Globally publish the newly created Office 2013 App-V Packages onto computers where you would like to apply the new updates.</span></span> <span data-ttu-id="f158c-413">Como o novo pacote tem a mesma linhagem do pacote mais antigo do Office 2013 App-V, publicar o novo pacote com as atualizações só aplicará as novas alterações ao pacote antigo e, portanto, será rápido.</span><span class="sxs-lookup"><span data-stu-id="f158c-413">Since the new package has the same lineage of the older Office 2013 App-V Package, publishing the new package with the updates will only apply the new changes to the old package, and thus will be fast.</span></span>

3.  <span data-ttu-id="f158c-414">As atualizações serão aplicadas da mesma maneira em qualquer pacote App-V publicado globalmente.</span><span class="sxs-lookup"><span data-stu-id="f158c-414">Upgrades will be applied in the same manner of any globally published App-V Packages.</span></span> <span data-ttu-id="f158c-415">Como os aplicativos provavelmente estarão em uso, as atualizações podem ser adiadas até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="f158c-415">Because applications will probably be in use, upgrades might be delayed until the computer is rebooted.</span></span>

### <a href="" id="bkmk-manage-office-lic-upgrd"></a><span data-ttu-id="f158c-416">Gerenciando atualizações de licenciamento do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f158c-416">Managing Office 2013 licensing upgrades</span></span>

<span data-ttu-id="f158c-417">Se um novo pacote do Office 2013 App-V tiver uma licença diferente do pacote do Office 2013 App-V implantado no momento.</span><span class="sxs-lookup"><span data-stu-id="f158c-417">If a new Office 2013 App-V Package has a different license than the Office 2013 App-V Package currently deployed.</span></span> <span data-ttu-id="f158c-418">Por exemplo, o pacote do Office 2013 implantado é uma assinatura do Office 2013 e o novo pacote do Office 2013 é baseado em licenciamento por volume, as instruções a seguir devem ser seguidas para garantir uma atualização de licenciamento suave:</span><span class="sxs-lookup"><span data-stu-id="f158c-418">For instance, the Office 2013 package deployed is a subscription based Office 2013 and the new Office 2013 package is Volume Licensing based, the following instructions must be followed to ensure smooth licensing upgrade:</span></span>

**<span data-ttu-id="f158c-419">Como atualizar uma licença do Office 2013</span><span class="sxs-lookup"><span data-stu-id="f158c-419">How to upgrade an Office 2013 License</span></span>**

1.  <span data-ttu-id="f158c-420">Cancele a publicação do pacote App-V de licenciamento de assinatura do Office 2013 já implementado.</span><span class="sxs-lookup"><span data-stu-id="f158c-420">Unpublish the already deployed Office 2013 Subscription Licensing App-V package.</span></span>

2.  <span data-ttu-id="f158c-421">Remova o pacote App-V de licenciamento de assinatura do Office 2013 cancelado.</span><span class="sxs-lookup"><span data-stu-id="f158c-421">Remove the unpublished Office 2013 Subscription Licensing App-V package.</span></span>

3.  <span data-ttu-id="f158c-422">Reinicie o computador.</span><span class="sxs-lookup"><span data-stu-id="f158c-422">Restart the computer.</span></span>

4.  <span data-ttu-id="f158c-423">Adicione o novo licenciamento de volume do pacote do Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="f158c-423">Add the new Office 2013 App-V Package Volume Licensing.</span></span>

5.  <span data-ttu-id="f158c-424">Publicar o pacote do Office 2013 App-V adicionado com licenciamento por volume.</span><span class="sxs-lookup"><span data-stu-id="f158c-424">Publish the added Office 2013 App-V Package with Volume Licensing.</span></span>

<span data-ttu-id="f158c-425">Um pacote do Office 2013 App-V com seu licenciamento escolhido será implantado com êxito.</span><span class="sxs-lookup"><span data-stu-id="f158c-425">An Office 2013 App-V Package with your chosen licensing will be successfully deployed.</span></span>

### <a href="" id="bkmk-deploy-visio-project"></a><span data-ttu-id="f158c-426">Implantação do Visio 2013 e do Project 2013 com o Office</span><span class="sxs-lookup"><span data-stu-id="f158c-426">Deploying Visio 2013 and Project 2013 with Office</span></span>

<span data-ttu-id="f158c-427">A tabela a seguir descreve os requisitos e as opções para a implantação do Visio 2013 e do Project 2013 com o Office.</span><span class="sxs-lookup"><span data-stu-id="f158c-427">The following table describes the requirements and options for deploying Visio 2013 and Project 2013 with Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f158c-428">Tarefa</span><span class="sxs-lookup"><span data-stu-id="f158c-428">Task</span></span></th>
<th align="left"><span data-ttu-id="f158c-429">Detalhes</span><span class="sxs-lookup"><span data-stu-id="f158c-429">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f158c-430">Como faço para empacotar e publicar o Visio 2013 e o Project 2013 com o Office?</span><span class="sxs-lookup"><span data-stu-id="f158c-430">How do I package and publish Visio 2013 and Project 2013 with Office?</span></span></p></td>
<td align="left"><p><span data-ttu-id="f158c-431">Você deve incluir o Visio 2013 e o Project 2013 no mesmo pacote com o Office.</span><span class="sxs-lookup"><span data-stu-id="f158c-431">You must include Visio 2013 and Project 2013 in the same package with Office.</span></span></p>
<p><span data-ttu-id="f158c-432">Se você não estiver implantando o Office, poderá criar um pacote que contenha o Visio e/ou Project, desde que siga a <a href="../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md" data-raw-source="[Deploying Microsoft Office 2010 by Using App-V](../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md)"> implantação do Microsoft Office 2010 usando o App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="f158c-432">If you aren’t deploying Office, you can create a package that contains Visio and/or Project, as long as you follow <a href="../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md" data-raw-source="[Deploying Microsoft Office 2010 by Using App-V](../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md)">Deploying Microsoft Office 2010 by Using App-V</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f158c-433">Como eu posso implantar o Visio 2013 e o Project 2013 para usuários específicos?</span><span class="sxs-lookup"><span data-stu-id="f158c-433">How can I deploy Visio 2013 and Project 2013 to specific users?</span></span></p></td>
<td align="left"><p><span data-ttu-id="f158c-434">Use um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="f158c-434">Use one of the following methods:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f158c-435">Se quiser...</span><span class="sxs-lookup"><span data-stu-id="f158c-435">If you want to...</span></span></th>
<th align="left"><span data-ttu-id="f158c-436">... em seguida, use esse método</span><span class="sxs-lookup"><span data-stu-id="f158c-436">...then use this method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f158c-437">Crie dois pacotes diferentes e implante cada um deles em um grupo diferente de usuários</span><span class="sxs-lookup"><span data-stu-id="f158c-437">Create two different packages and deploy each one to a different group of users</span></span></p></td>
<td align="left"><p><span data-ttu-id="f158c-438">Crie e implante os seguintes pacotes:</span><span class="sxs-lookup"><span data-stu-id="f158c-438">Create and deploy the following packages:</span></span></p>
<ul>
<li><p><span data-ttu-id="f158c-439">Um pacote que contém apenas o Office-implantação em computadores cujos usuários precisam apenas do Office.</span><span class="sxs-lookup"><span data-stu-id="f158c-439">A package that contains only Office - deploy to computers whose users need only Office.</span></span></p></li>
<li><p><span data-ttu-id="f158c-440">Um pacote que contém o Office, o Visio e o Project-implantação para computadores cujos usuários precisam de todos os três aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f158c-440">A package that contains Office, Visio, and Project - deploy to computers whose users need all three applications.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f158c-441">Se você quiser apenas um pacote para a organização inteira, ou se tiver usuários que compartilham computadores:</span><span class="sxs-lookup"><span data-stu-id="f158c-441">If you want only one package for the whole organization, or if you have users who share computers:</span></span></p></td>
<td align="left"><p><span data-ttu-id="f158c-442">Siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="f158c-442">Follows these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="f158c-443">Crie um pacote que contenha o Office, o Visio e o Project.</span><span class="sxs-lookup"><span data-stu-id="f158c-443">Create a package that contains Office, Visio, and Project.</span></span></p></li>
<li><p><span data-ttu-id="f158c-444">Implante o pacote para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="f158c-444">Deploy the package to all users.</span></span></p></li>
<li><p><span data-ttu-id="f158c-445">Use <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)"> o Microsoft AppLocker </a> para impedir que usuários específicos usem o Visio e o Project.</span><span class="sxs-lookup"><span data-stu-id="f158c-445">Use <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)">Microsoft AppLocker</a> to prevent specific users from using Visio and Project.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="f158c-446">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="f158c-446">Additional resources</span></span>


**<span data-ttu-id="f158c-447">Pacotes do Office 2013 App-V 5,0 5,0 recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="f158c-447">Office 2013 App-V 5.0 Packages 5.0 Additional Resources</span></span>**

[<span data-ttu-id="f158c-448">Ferramenta de implantação do Office para clique para executar</span><span class="sxs-lookup"><span data-stu-id="f158c-448">Office Deployment Tool for Click-to-Run</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=330672)

[<span data-ttu-id="f158c-449">Cenários suportados para a implantação do Microsoft Office como um pacote App-V sequenciado</span><span class="sxs-lookup"><span data-stu-id="f158c-449">Supported scenarios for deploying Microsoft Office as a sequenced App-V Package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**<span data-ttu-id="f158c-450">Pacotes do Office 2010 App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="f158c-450">Office 2010 App-V 5.0 Packages</span></span>**

[<span data-ttu-id="f158c-451">Kit de sequenciamento do Microsoft Office 2010 para Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="f158c-451">Microsoft Office 2010 Sequencing Kit for Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[<span data-ttu-id="f158c-452">Problemas conhecidos ao criar ou usar um pacote do App-V 5,0 do Office 2010</span><span class="sxs-lookup"><span data-stu-id="f158c-452">Known issues when you create or use an App-V 5.0 Office 2010 package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[<span data-ttu-id="f158c-453">Como sequenciar o Microsoft Office 2010 no Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="f158c-453">How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**<span data-ttu-id="f158c-454">Grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="f158c-454">Connection Groups</span></span>**

[<span data-ttu-id="f158c-455">Implantando grupos de conexão no Microsoft App-V V5</span><span class="sxs-lookup"><span data-stu-id="f158c-455">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="f158c-456">Gerenciando grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="f158c-456">Managing Connection Groups</span></span>](managing-connection-groups.md)

**<span data-ttu-id="f158c-457">Configuração dinâmica</span><span class="sxs-lookup"><span data-stu-id="f158c-457">Dynamic Configuration</span></span>**

[<span data-ttu-id="f158c-458">Sobre a configuração dinâmica do App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f158c-458">About App-V 5.0 Dynamic Configuration</span></span>](about-app-v-50-dynamic-configuration.md)














