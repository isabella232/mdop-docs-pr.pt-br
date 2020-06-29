---
title: Sobre o App-V 5.1
description: Sobre o App-V 5.1
author: dansimp
ms.assetid: 35bc9908-d502-4a9c-873f-8ee17b6d9d74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4f2404dcd431b32f5d9a4ae7c49f1e376979e04e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796627"
---
# <span data-ttu-id="29433-103">Sobre o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="29433-103">About App-V 5.1</span></span>


<span data-ttu-id="29433-104">Use as seções a seguir para analisar informações sobre alterações significativas que se aplicam ao Application Virtualization (App-V) 5,1:</span><span class="sxs-lookup"><span data-stu-id="29433-104">Use the following sections to review information about significant changes that apply to Application Virtualization (App-V) 5.1:</span></span>

[<span data-ttu-id="29433-105">Pré-requisitos de software do App-V 5,1 e configurações com suporte</span><span class="sxs-lookup"><span data-stu-id="29433-105">App-V 5.1 software prerequisites and supported configurations</span></span>](#bkmk-51-prereq-configs)

[<span data-ttu-id="29433-106">Migrando para o App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="29433-106">Migrating to App-V 5.1</span></span>](#bkmk-migrate-to-51)

[<span data-ttu-id="29433-107">O que há de novo no App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="29433-107">What’s New in App-V 5.1</span></span>](#bkmk-whatsnew)

[<span data-ttu-id="29433-108">Suporte do App-V para Windows 10</span><span class="sxs-lookup"><span data-stu-id="29433-108">App-V support for Windows 10</span></span>](#bkmk-win10support)

[<span data-ttu-id="29433-109">Alterações no console de gerenciamento do App-V</span><span class="sxs-lookup"><span data-stu-id="29433-109">App-V Management Console Changes</span></span>](#bkmk-mgmtconsole)

[<span data-ttu-id="29433-110">Melhorias do sequenciador</span><span class="sxs-lookup"><span data-stu-id="29433-110">Sequencer Improvements</span></span>](#bkmk-seqimprove)

[<span data-ttu-id="29433-111">Melhorias no conversor de pacote</span><span class="sxs-lookup"><span data-stu-id="29433-111">Improvements to Package Converter</span></span>](#bkmk-pkgconvimprove)

[<span data-ttu-id="29433-112">Suporte para vários scripts em um único gatilho de evento</span><span class="sxs-lookup"><span data-stu-id="29433-112">Support for multiple scripts on a single event trigger</span></span>](#bkmk-supmultscripts)

[<span data-ttu-id="29433-113">Caminho codificado para a pasta de instalação é redirecionado para a raiz do sistema de arquivos virtual</span><span class="sxs-lookup"><span data-stu-id="29433-113">Hardcoded path to installation folder is redirected to virtual file system root</span></span>](#bkmk-hardcodepath)

## <a href="" id="bkmk-51-prereq-configs"></a><span data-ttu-id="29433-114">Pré-requisitos de software do App-V 5,1 e configurações com suporte</span><span class="sxs-lookup"><span data-stu-id="29433-114">App-V 5.1 software prerequisites and supported configurations</span></span>


<span data-ttu-id="29433-115">Confira os links a seguir para os pré-requisitos de software do App-V 5,1 e as configurações com suporte.</span><span class="sxs-lookup"><span data-stu-id="29433-115">See the following links for the App-V 5.1 software prerequisites and supported configurations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="29433-116">Links para pré-requisitos e configurações com suporte</span><span class="sxs-lookup"><span data-stu-id="29433-116">Links to prerequisites and supported configurations</span></span></th>
<th align="left"><span data-ttu-id="29433-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="29433-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-51-prerequisites.md" data-raw-source="[App-V 5.1 Prerequisites](app-v-51-prerequisites.md)"><span data-ttu-id="29433-118">Pré-requisitos do App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="29433-118">App-V 5.1 Prerequisites</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="29433-119">Software obrigatório que você deve instalar antes de iniciar a instalação do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="29433-119">Prerequisite software that you must install before starting the App-V 5.1 installation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"><span data-ttu-id="29433-120">Configurações com suporte ao App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="29433-120">App-V 5.1 Supported Configurations</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="29433-121">Sistemas operacionais com suporte e requisitos de hardware para os componentes App-V Server, Sequencer e cliente</span><span class="sxs-lookup"><span data-stu-id="29433-121">Supported operating systems and hardware requirements for the App-V Server, Sequencer, and Client components</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="29433-122">**Suporte para usar o Configuration Manager com App-V:** O App-V 5,1 dá suporte ao System Center 2012 R2 Configuration Manager SP1.</span><span class="sxs-lookup"><span data-stu-id="29433-122">**Support for using Configuration Manager with App-V:** App-V 5.1 supports System Center 2012 R2 Configuration Manager SP1.</span></span> <span data-ttu-id="29433-123">Consulte [planejando a integração do App-v com o Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx) para obter informações sobre como integrar seu ambiente app-v com o Configuration Manager e o Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="29433-123">See [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx) for information about integrating your App-V environment with Configuration Manager and Configuration Manager.</span></span>

## <a href="" id="bkmk-migrate-to-51"></a><span data-ttu-id="29433-124">Migrando para o App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="29433-124">Migrating to App-V 5.1</span></span>


<span data-ttu-id="29433-125">Use as informações a seguir para atualizar para o App-V 5,1 de versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="29433-125">Use the following information to upgrade to App-V 5.1 from earlier versions.</span></span> <span data-ttu-id="29433-126">Para obter mais informações, confira [migrar para o App-V 5,1 de uma versão anterior](migrating-to-app-v-51-from-a-previous-version.md) .</span><span class="sxs-lookup"><span data-stu-id="29433-126">See [Migrating to App-V 5.1 from a Previous Version](migrating-to-app-v-51-from-a-previous-version.md) for more information.</span></span>

### <span data-ttu-id="29433-127">Antes de iniciar a atualização</span><span class="sxs-lookup"><span data-stu-id="29433-127">Before you start the upgrade</span></span>

<span data-ttu-id="29433-128">Revise as seguintes informações antes de iniciar a atualização:</span><span class="sxs-lookup"><span data-stu-id="29433-128">Review the following information before you start the upgrade:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="29433-129">Itens a serem revisados antes da atualização</span><span class="sxs-lookup"><span data-stu-id="29433-129">Items to review before upgrading</span></span></th>
<th align="left"><span data-ttu-id="29433-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="29433-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29433-131">Componentes para atualização, em qualquer ordem</span><span class="sxs-lookup"><span data-stu-id="29433-131">Components to upgrade, in any order</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="29433-132">Servidor do App-V</span><span class="sxs-lookup"><span data-stu-id="29433-132">App-V Server</span></span></p></li>
<li><p><span data-ttu-id="29433-133">Sequenciador</span><span class="sxs-lookup"><span data-stu-id="29433-133">Sequencer</span></span></p></li>
<li><p><span data-ttu-id="29433-134">Cliente App-V ou serviços de área de trabalho remota do App-V (RDS)</span><span class="sxs-lookup"><span data-stu-id="29433-134">App-V Client or App-V Remote Desktop Services (RDS) Client</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="29433-135">Observação</span><span class="sxs-lookup"><span data-stu-id="29433-135">Note</span></span></strong><br/><p><span data-ttu-id="29433-136">Antes do App-V 5,0 SP2, a interface do usuário de gerenciamento do cliente (UI) foi fornecida com a instalação do cliente do App-V.</span><span class="sxs-lookup"><span data-stu-id="29433-136">Prior to App-V 5.0 SP2, the Client Management User Interface (UI) was provided with the App-V Client installation.</span></span> <span data-ttu-id="29433-137">Para instalações do App-V 5,0 SP2 (ou posterior), você pode usar a interface do usuário de gerenciamento de cliente ao baixar do <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> aplicativo de interface do usuário do cliente do Application Virtualization 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="29433-137">For App-V 5.0 SP2 installations (or later), you can use the Client Management UI by downloading from <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)">Application Virtualization 5.0 Client UI Application</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29433-138">Atualizando do App-V 4. x</span><span class="sxs-lookup"><span data-stu-id="29433-138">Upgrading from App-V 4.x</span></span></p></td>
<td align="left"><p><span data-ttu-id="29433-139">Primeiro você deve atualizar para o App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="29433-139">You must first upgrade to App-V 5.0.</span></span> <span data-ttu-id="29433-140">Você não pode atualizar diretamente do App-V 4. x para o App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="29433-140">You cannot upgrade directly from App-V 4.x to App-V 5.1.</span></span> <span data-ttu-id="29433-141">Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="29433-141">For more information, see:</span></span></p>
<ul>
<li><p><span data-ttu-id="29433-142">"Diferenças entre o App-V 4,6 e o App-V 5,0" em <a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)"> sobre o app-v 5,0</span><span class="sxs-lookup"><span data-stu-id="29433-142">“Differences between App-V 4.6 and App-V 5.0” in <a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)">About App-V 5.0</span></span></a></p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)"><span data-ttu-id="29433-143">Planejamento para a migração de uma versão anterior do App-V</span><span class="sxs-lookup"><span data-stu-id="29433-143">Planning for Migrating from a Previous Version of App-V</span></span></a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29433-144">Atualizando a partir do App-V 5,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="29433-144">Upgrading from App-V 5.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="29433-145">Você pode atualizar para o App-V 5,1 diretamente de qualquer uma das seguintes versões:</span><span class="sxs-lookup"><span data-stu-id="29433-145">You can upgrade to App-V 5.1 directly from any of the following versions:</span></span></p>
<ul>
<li><p><span data-ttu-id="29433-146">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="29433-146">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="29433-147">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="29433-147">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="29433-148">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="29433-148">App-V 5.0 SP2</span></span></p></li>
<li><p><span data-ttu-id="29433-149">App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="29433-149">App-V 5.0 SP3</span></span></p></li>
</ul>
<p><span data-ttu-id="29433-150">Para atualizar para o App-V 5,1, siga as etapas nas seções restantes deste tópico.</span><span class="sxs-lookup"><span data-stu-id="29433-150">To upgrade to App-V 5.1, follow the steps in the remaining sections of this topic.</span></span></p>
<p><span data-ttu-id="29433-151">Pacotes e grupos de conexão continuarão a funcionar com o App-V 5,1, como fazem no momento.</span><span class="sxs-lookup"><span data-stu-id="29433-151">Packages and connection groups will continue to work with App-V 5.1 as they currently do.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a><span data-ttu-id="29433-152">Etapas para atualizar a infraestrutura do App-V</span><span class="sxs-lookup"><span data-stu-id="29433-152">Steps to upgrade the App-V infrastructure</span></span>

<span data-ttu-id="29433-153">Conclua as etapas a seguir para atualizar cada componente da infraestrutura do App-V para o App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="29433-153">Complete the following steps to upgrade each component of the App-V infrastructure to App-V 5.1.</span></span> <span data-ttu-id="29433-154">A ordem a seguir é apenas uma sugestão; Você pode atualizar componentes em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="29433-154">The following order is only a suggestion; you may upgrade components in any order.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="29433-155">Etapa</span><span class="sxs-lookup"><span data-stu-id="29433-155">Step</span></span></th>
<th align="left"><span data-ttu-id="29433-156">Para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="29433-156">For more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29433-157">Etapa 1: Atualize o App-V Server.</span><span class="sxs-lookup"><span data-stu-id="29433-157">Step 1: Upgrade the App-V Server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="29433-158">Observação</span><span class="sxs-lookup"><span data-stu-id="29433-158">Note</span></span></strong><br/><p><span data-ttu-id="29433-159">Se você não estiver usando o servidor App-V, pule esta etapa e vá para a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="29433-159">If you are not using the App-V Server, skip this step and go to the next step.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="29433-160">Siga estas etapas: </span><span class="sxs-lookup"><span data-stu-id="29433-160">Follow these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="29433-161">Siga um destes procedimentos, dependendo do método que você está usando para atualizar o banco de dados de gerenciamento e/ou banco de dados de relatórios:</span><span class="sxs-lookup"><span data-stu-id="29433-161">Do one of the following, depending on the method you are using to upgrade the Management database and/or Reporting database:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="29433-162">Método de atualização de banco de dados</span><span class="sxs-lookup"><span data-stu-id="29433-162">Database upgrade method</span></span></th>
<th align="left"><span data-ttu-id="29433-163">Etapa</span><span class="sxs-lookup"><span data-stu-id="29433-163">Step</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29433-164">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="29433-164">Windows Installer</span></span></p></td>
<td align="left"><p><span data-ttu-id="29433-165">Pule esta etapa e vá para a etapa 2, "se você estiver atualizando o App-V Server..."</span><span class="sxs-lookup"><span data-stu-id="29433-165">Skip this step and go to step 2, “If you are upgrading the App-V Server...”</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29433-166">Scripts SQL</span><span class="sxs-lookup"><span data-stu-id="29433-166">SQL scripts</span></span></p></td>
<td align="left"><p><span data-ttu-id="29433-167">Siga as etapas em <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)"> como implantar os bancos de dados do App-V usando scripts SQL </a> .</span><span class="sxs-lookup"><span data-stu-id="29433-167">Follow the steps in <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)">How to Deploy the App-V Databases by Using SQL Scripts</a>.</span></span></p></td>
</tr>
</tbody>
</table>
<li><p><span data-ttu-id="29433-168">Se você estiver atualizando o pacote do pacote do aplicativo App-V do App-V 5,0 SP1 3 ou posterior, conclua as etapas na seção <a href="check-reg-key-svr.md" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](check-reg-key-svr.md)"> Verifique as chaves do registro após instalar o servidor App-V 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="29433-168">If you are upgrading the App-V Server from App-V 5.0 SP1 Hotfix Package 3 or later, complete the steps in section <a href="check-reg-key-svr.md" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](check-reg-key-svr.md)">Check registry keys after installing the App-V 5.0 SP3 Server</a>.</span></span></p></li>
<li><p><span data-ttu-id="29433-169">Siga as etapas em <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"> como implantar o servidor do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="29433-169">Follow the steps in <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)">How to Deploy the App-V 5.1 Server</span></span></a></p></li>
<p> </p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29433-170">Etapa 2: Atualize o sequenciador do App-V.</span><span class="sxs-lookup"><span data-stu-id="29433-170">Step 2: Upgrade the App-V Sequencer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="29433-171">Veja <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"> como instalar o sequenciador </a> .</span><span class="sxs-lookup"><span data-stu-id="29433-171">See <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)">How to Install the Sequencer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29433-172">Etapa 3: Atualize o cliente App-V ou o App-V RDS Client.</span><span class="sxs-lookup"><span data-stu-id="29433-172">Step 3: Upgrade the App-V Client or App-V RDS Client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="29433-173">Veja <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"> como implantar o cliente App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="29433-173">See <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="29433-174">Convertendo pacotes criados usando uma versão anterior do App-V</span><span class="sxs-lookup"><span data-stu-id="29433-174">Converting packages created using a prior version of App-V</span></span>

<span data-ttu-id="29433-175">Use o utilitário conversor de pacote para atualizar pacotes de aplicativos virtuais criados usando versões do App-V antes do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="29433-175">Use the package converter utility to upgrade virtual application packages created using versions of App-V prior to App-V 5.0.</span></span> <span data-ttu-id="29433-176">O conversor de pacote usa o PowerShell para converter pacotes e pode ajudar a automatizar o processo se você tiver muitos pacotes que exijam conversão.</span><span class="sxs-lookup"><span data-stu-id="29433-176">The package converter uses PowerShell to convert packages and can help automate the process if you have many packages that require conversion.</span></span>

**<span data-ttu-id="29433-177">Observação</span><span class="sxs-lookup"><span data-stu-id="29433-177">Note</span></span>**  
<span data-ttu-id="29433-178">Os pacotes do App-V 5,1 são exatamente iguais aos pacotes do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="29433-178">App-V 5.1 packages are exactly the same as App-V 5.0 packages.</span></span> <span data-ttu-id="29433-179">Não houve nenhuma alteração no formato do pacote entre as versões e, portanto, não há necessidade de converter pacotes do App-V 5,0 em pacotes do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="29433-179">There has been no change in the package format between the versions and so there is no need to convert App-V 5.0 packages to App-V 5.1 packages.</span></span>



## <a href="" id="bkmk-whatsnew"></a><span data-ttu-id="29433-180">O que há de novo no App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="29433-180">What’s New in App-V 5.1</span></span>


<span data-ttu-id="29433-181">Estas seções destinam-se aos usuários que já estão familiarizados com o App-V e querem saber o que mudou no App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="29433-181">These sections are for users who are already familiar with App-V and want to know what has changed in App-V 5.1.</span></span> <span data-ttu-id="29433-182">Se você ainda não estiver familiarizado com o App-V, comece lendo planejando o [app-v 5,1](planning-for-app-v-51.md).</span><span class="sxs-lookup"><span data-stu-id="29433-182">If you are not already familiar with App-V, you should start by reading [Planning for App-V 5.1](planning-for-app-v-51.md).</span></span>

### <a href="" id="bkmk-win10support"></a><span data-ttu-id="29433-183">Suporte do App-V para Windows 10</span><span class="sxs-lookup"><span data-stu-id="29433-183">App-V support for Windows 10</span></span>

<span data-ttu-id="29433-184">A tabela a seguir lista o suporte do Windows 10 para App-V.</span><span class="sxs-lookup"><span data-stu-id="29433-184">The following table lists the Windows 10 support for App-V.</span></span> <span data-ttu-id="29433-185">Não há suporte para o Windows 10 em versões do App-V antes do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="29433-185">Windows 10 is not supported in versions of App-V prior to App-V 5.1.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="29433-186">Componente</span><span class="sxs-lookup"><span data-stu-id="29433-186">Component</span></span></th>
<th align="left"><span data-ttu-id="29433-187">App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="29433-187">App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="29433-188">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="29433-188">App-V 5.0</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29433-189">Cliente App-V</span><span class="sxs-lookup"><span data-stu-id="29433-189">App-V Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="29433-190">Sim</span><span class="sxs-lookup"><span data-stu-id="29433-190">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="29433-191">Não</span><span class="sxs-lookup"><span data-stu-id="29433-191">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29433-192">Cliente RDS do App-V</span><span class="sxs-lookup"><span data-stu-id="29433-192">App-V RDS Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="29433-193">Sim</span><span class="sxs-lookup"><span data-stu-id="29433-193">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="29433-194">Não</span><span class="sxs-lookup"><span data-stu-id="29433-194">No</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29433-195">Sequenciador App-V</span><span class="sxs-lookup"><span data-stu-id="29433-195">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="29433-196">Sim</span><span class="sxs-lookup"><span data-stu-id="29433-196">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="29433-197">Não</span><span class="sxs-lookup"><span data-stu-id="29433-197">No</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-mgmtconsole"></a><span data-ttu-id="29433-198">Alterações no console de gerenciamento do App-V</span><span class="sxs-lookup"><span data-stu-id="29433-198">App-V Management Console Changes</span></span>

<span data-ttu-id="29433-199">Esta seção compara a funcionalidade atual e anterior do console de gerenciamento do App-V.</span><span class="sxs-lookup"><span data-stu-id="29433-199">This section compares the App-V Management Console’s current and previous functionality.</span></span>

### <span data-ttu-id="29433-200">O Silverlight não é mais necessário</span><span class="sxs-lookup"><span data-stu-id="29433-200">Silverlight is no longer required</span></span>

<span data-ttu-id="29433-201">A interface do usuário do console de gerenciamento não requer mais o Silverlight.</span><span class="sxs-lookup"><span data-stu-id="29433-201">The Management Console UI no longer requires Silverlight.</span></span> <span data-ttu-id="29433-202">O console de gerenciamento do 5,1 é criado em HTML5 e JavaScript.</span><span class="sxs-lookup"><span data-stu-id="29433-202">The 5.1 Management Console is built on HTML5 and Javascript.</span></span>

### <span data-ttu-id="29433-203">As notificações e mensagens são exibidas individualmente em uma caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="29433-203">Notifications and messages are displayed individually in a dialog box</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="29433-204">Novo no App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="29433-204">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="29433-205">Antes do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="29433-205">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="29433-206">Indicador de número de mensagens:</span><span class="sxs-lookup"><span data-stu-id="29433-206">Number of messages indicator:</span></span></strong></p>
<p><span data-ttu-id="29433-207">Na barra de título do console de gerenciamento do App-V, um número agora é exibido ao lado de um ícone de sinalizador para indicar o número de mensagens que estão aguardando para serem lidas.</span><span class="sxs-lookup"><span data-stu-id="29433-207">On the title bar of the App-V Management Console, a number is now displayed next to a flag icon to indicate the number of messages that are waiting to be read.</span></span></p></td>
<td align="left"><p><span data-ttu-id="29433-208">Você pode ver apenas uma mensagem ou um erro de cada vez, e você não pôde determinar quantas mensagens havia.</span><span class="sxs-lookup"><span data-stu-id="29433-208">You could see only one message or error at a time, and you were unable to determine how many messages there were.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="29433-209">Aparência da mensagem:</span><span class="sxs-lookup"><span data-stu-id="29433-209">Message appearance:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="29433-210">As mensagens que exigem entrada do usuário aparecem em uma caixa de diálogo separada que é exibida na parte superior da página atual que você estava exibindo e exigem uma resposta antes de poder descartá-las.</span><span class="sxs-lookup"><span data-stu-id="29433-210">Messages that require user input appear in a separate dialog box that displays on top of the current page that you were viewing, and require a response before you can dismiss them.</span></span></p></li>
<li><p><span data-ttu-id="29433-211">Mensagens e erros aparecem em uma lista, com um abaixo do outro.</span><span class="sxs-lookup"><span data-stu-id="29433-211">Messages and errors appear in a list, with one beneath the other.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="29433-212">Você pode ver apenas uma mensagem ou um erro de cada vez.</span><span class="sxs-lookup"><span data-stu-id="29433-212">You could see only one message or error at a time.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="29433-213">Ignorando mensagens:</span><span class="sxs-lookup"><span data-stu-id="29433-213">Dismissing messages:</span></span></strong></p>
<p><span data-ttu-id="29433-214">Use o <strong> link ignorar tudo </strong> para ignorar todas as mensagens e erros de uma vez ou descartá-los um de cada vez.</span><span class="sxs-lookup"><span data-stu-id="29433-214">Use the <strong>Dismiss All</strong> link to dismiss all messages and errors at one time, or dismiss them one at a time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="29433-215">Você pode ignorar mensagens e erros apenas um de cada vez.</span><span class="sxs-lookup"><span data-stu-id="29433-215">You could dismiss messages and errors only one at a time.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="29433-216">As páginas do console agora são URLs separadas</span><span class="sxs-lookup"><span data-stu-id="29433-216">Console pages are now separate URLs</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="29433-217">Novo no App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="29433-217">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="29433-218">Antes do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="29433-218">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29433-219">Cada página no console tem uma URL diferente, que permite marcar páginas específicas para acesso rápido no futuro.</span><span class="sxs-lookup"><span data-stu-id="29433-219">Each page in the console has a different URL, which enables you to bookmark specific pages for quick access in the future.</span></span></p>
<p><span data-ttu-id="29433-220">O número que aparece em algumas URLs indica o pacote específico.</span><span class="sxs-lookup"><span data-stu-id="29433-220">The number that appears in some URLs indicates the specific package.</span></span> <span data-ttu-id="29433-221">Esses números são exclusivos.</span><span class="sxs-lookup"><span data-stu-id="29433-221">These numbers are unique.</span></span></p></td>
<td align="left"><p><span data-ttu-id="29433-222">Todas as páginas de console são acessadas por meio da mesma URL.</span><span class="sxs-lookup"><span data-stu-id="29433-222">All console pages are accessed through the same URL.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="29433-223">Nova, página de grupos de conexão separados e opção de menu</span><span class="sxs-lookup"><span data-stu-id="29433-223">New, separate CONNECTION GROUPS page and menu option</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="29433-224">Novo no App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="29433-224">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="29433-225">Antes do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="29433-225">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29433-226">A página de grupos de conexão agora faz parte do menu principal, no mesmo nível da página de pacotes.</span><span class="sxs-lookup"><span data-stu-id="29433-226">The CONNECTION GROUPS page is now part of the main menu, at the same level as the PACKAGES page.</span></span></p></td>
<td align="left"><p><span data-ttu-id="29433-227">Para abrir a página grupos de conexão, navegue pela página pacotes.</span><span class="sxs-lookup"><span data-stu-id="29433-227">To open the CONNECTION GROUPS page, you navigate through the PACKAGES page.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="29433-228">As opções de menu para pacotes foram alteradas</span><span class="sxs-lookup"><span data-stu-id="29433-228">Menu options for packages have changed</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="29433-229">Novo no App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="29433-229">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="29433-230">Antes do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="29433-230">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="29433-231">As opções a seguir são botões agora que aparecem na parte inferior da página pacotes:</span><span class="sxs-lookup"><span data-stu-id="29433-231">The following options are now buttons that appear at the bottom of the PACKAGES page:</span></span></p>
<ul>
<li><p><span data-ttu-id="29433-232">Adicionar ou atualizar</span><span class="sxs-lookup"><span data-stu-id="29433-232">Add or Upgrade</span></span></p></li>
<li><p><span data-ttu-id="29433-233">Publicar</span><span class="sxs-lookup"><span data-stu-id="29433-233">Publish</span></span></p></li>
<li><p><span data-ttu-id="29433-234">Cancelar</span><span class="sxs-lookup"><span data-stu-id="29433-234">Unpublish</span></span></p></li>
<li><p><span data-ttu-id="29433-235">Excluir</span><span class="sxs-lookup"><span data-stu-id="29433-235">Delete</span></span></p></li>
</ul>
<p><span data-ttu-id="29433-236">As opções a seguir ainda serão exibidas quando você clicar com o botão direito do mouse em um pacote para abrir o menu de contexto suspenso:</span><span class="sxs-lookup"><span data-stu-id="29433-236">The following options will still appear when you right-click a package to open the drop-down context menu:</span></span></p>
<ul>
<li><p><span data-ttu-id="29433-237">Publicar</span><span class="sxs-lookup"><span data-stu-id="29433-237">Publish</span></span></p></li>
<li><p><span data-ttu-id="29433-238">Cancelar</span><span class="sxs-lookup"><span data-stu-id="29433-238">Unpublish</span></span></p></li>
<li><p><span data-ttu-id="29433-239">Editar o acesso ao anúncio</span><span class="sxs-lookup"><span data-stu-id="29433-239">Edit AD Access</span></span></p></li>
<li><p><span data-ttu-id="29433-240">Editar configuração de implantação</span><span class="sxs-lookup"><span data-stu-id="29433-240">Edit Deployment Config</span></span></p></li>
<li><p><span data-ttu-id="29433-241">Transferir configuração de implantação de...</span><span class="sxs-lookup"><span data-stu-id="29433-241">Transfer deployment configuration from…</span></span></p></li>
<li><p><span data-ttu-id="29433-242">Transferir acesso e configuração de...</span><span class="sxs-lookup"><span data-stu-id="29433-242">Transfer access and configuration from…</span></span></p></li>
<li><p><span data-ttu-id="29433-243">Excluir</span><span class="sxs-lookup"><span data-stu-id="29433-243">Delete</span></span></p></li>
</ul>
<p><span data-ttu-id="29433-244">Quando você clica em <strong> excluir </strong> para remover um pacote, uma caixa de diálogo é aberta e solicita que você confirme que deseja excluir o pacote.</span><span class="sxs-lookup"><span data-stu-id="29433-244">When you click <strong>Delete</strong> to remove a package, a dialog box opens and asks you to confirm that you want to delete the package.</span></span></p></td>
<td align="left"><p><span data-ttu-id="29433-245">A <strong> opção Adicionar ou atualizar </strong> era um botão no canto superior direito da página pacotes.</span><span class="sxs-lookup"><span data-stu-id="29433-245">The <strong>Add or Upgrade</strong> option was a button at the top right of the PACKAGES page.</span></span></p>
<p><span data-ttu-id="29433-246">As <strong> </strong> Opções publicar, <strong> Cancelar publicação </strong> e <strong> excluir </strong> estavam disponíveis somente se você clicar com o botão direito do mouse em um nome de pacote na lista pacotes.</span><span class="sxs-lookup"><span data-stu-id="29433-246">The <strong>Publish</strong>, <strong>Unpublish</strong>, and <strong>Delete</strong> options were available only if you right-clicked a package name in the packages list.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="29433-247">As seguintes operações de pacote agora são botões na página de detalhes do pacote para cada pacote:</span><span class="sxs-lookup"><span data-stu-id="29433-247">The following package operations are now buttons on the package details page for each package:</span></span></p>
<ul>
<li><p><span data-ttu-id="29433-248">Transferir (menu suspenso com as seguintes opções):</span><span class="sxs-lookup"><span data-stu-id="29433-248">Transfer (drop-down menu with the following options):</span></span></p>
<ul>
<li><p><span data-ttu-id="29433-249">Transferir configuração de implantação de...</span><span class="sxs-lookup"><span data-stu-id="29433-249">Transfer deployment configuration from…</span></span></p></li>
<li><p><span data-ttu-id="29433-250">Transferir acesso e configuração de...</span><span class="sxs-lookup"><span data-stu-id="29433-250">Transfer access and configuration from…</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="29433-251">Editar (grupos de conexão e acesso ao AD)</span><span class="sxs-lookup"><span data-stu-id="29433-251">Edit (connection groups and AD Access)</span></span></p></li>
<li><p><span data-ttu-id="29433-252">Cancelar</span><span class="sxs-lookup"><span data-stu-id="29433-252">Unpublish</span></span></p></li>
<li><p><span data-ttu-id="29433-253">Excluir</span><span class="sxs-lookup"><span data-stu-id="29433-253">Delete</span></span></p></li>
<li><p><span data-ttu-id="29433-254">Editar configuração padrão</span><span class="sxs-lookup"><span data-stu-id="29433-254">Edit Default Configuration</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="29433-255">Essas opções de pacote estavam disponíveis somente se você clicar com o botão direito do mouse em um nome de pacote na lista pacotes.</span><span class="sxs-lookup"><span data-stu-id="29433-255">These package options were available only if you right-clicked a package name in the packages list.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="29433-256">Ícones no painel esquerdo têm novas cores e texto</span><span class="sxs-lookup"><span data-stu-id="29433-256">Icons in left pane have new colors and text</span></span>

<span data-ttu-id="29433-257">As cores dos ícones no painel esquerdo foram alteradas e o texto é adicionado para tornar os ícones consistentes com outros produtos da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="29433-257">The colors of the icons in the left pane have been changed, and text added, to make the icons consistent with other Microsoft products.</span></span>

### <span data-ttu-id="29433-258">A página de visão geral foi removida</span><span class="sxs-lookup"><span data-stu-id="29433-258">Overview page has been removed</span></span>

<span data-ttu-id="29433-259">No painel esquerdo do console de gerenciamento, a opção de menu visão geral e sua página de visão geral associada foram removidas.</span><span class="sxs-lookup"><span data-stu-id="29433-259">In the left pane of the Management Console, the OVERVIEW menu option and its associated OVERVIEW page have been removed.</span></span>

### <a href="" id="bkmk-seqimprove"></a><span data-ttu-id="29433-260">Melhorias do sequenciador</span><span class="sxs-lookup"><span data-stu-id="29433-260">Sequencer Improvements</span></span>

<span data-ttu-id="29433-261">Os seguintes aprimoramentos foram feitos no editor de pacotes no sequenciador do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="29433-261">The following improvements have been made to the package editor in the App-V 5.1 Sequencer.</span></span>

### <span data-ttu-id="29433-262">Importar e exportar o arquivo de manifesto</span><span class="sxs-lookup"><span data-stu-id="29433-262">Import and export the manifest file</span></span>

<span data-ttu-id="29433-263">Você pode importar e exportar o arquivo AppxManifest.xml.</span><span class="sxs-lookup"><span data-stu-id="29433-263">You can import and export the AppxManifest.xml file.</span></span> <span data-ttu-id="29433-264">Para exportar o arquivo de manifesto, selecione a guia **avançado** e, na caixa arquivo de manifesto, clique em **Exportar..**.. Você pode fazer alterações no arquivo de manifesto, como a remoção de extensões do Shell ou a edição de associações de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="29433-264">To export the manifest file, select the **Advanced** tab and in the Manifest File box, click **Export...**. You can make changes to the manifest file, such as removing shell extensions or editing file type associations.</span></span>

<span data-ttu-id="29433-265">Depois de fazer as alterações, clique em **importar...** e selecione o arquivo editado.</span><span class="sxs-lookup"><span data-stu-id="29433-265">After you make your changes, click **Import...** and select the file you edited.</span></span> <span data-ttu-id="29433-266">Depois de importá-lo com êxito novamente, o arquivo de manifesto será atualizado imediatamente dentro do editor do pacote.</span><span class="sxs-lookup"><span data-stu-id="29433-266">After you successfully import it back in, the manifest file is immediately updated within the package editor.</span></span>

**<span data-ttu-id="29433-267">Tenha</span><span class="sxs-lookup"><span data-stu-id="29433-267">Caution</span></span>**  
<span data-ttu-id="29433-268">Quando você importa o arquivo, suas alterações são validadas em relação ao esquema XML.</span><span class="sxs-lookup"><span data-stu-id="29433-268">When you import the file, your changes are validated against the XML schema.</span></span> <span data-ttu-id="29433-269">Se o arquivo não for válido, você receberá um erro.</span><span class="sxs-lookup"><span data-stu-id="29433-269">If the file is not valid, you will receive an error.</span></span> <span data-ttu-id="29433-270">Lembre-se de que é possível importar um arquivo validado em relação ao esquema XML, mas que ainda poderá falhar para ser executado por outros motivos.</span><span class="sxs-lookup"><span data-stu-id="29433-270">Be aware that it is possible to import a file that is validated against the XML schema, but that might still fail to run for other reasons.</span></span>



### <span data-ttu-id="29433-271">Adição da lista de Windows 10 a sistemas operacionais</span><span class="sxs-lookup"><span data-stu-id="29433-271">Addition of Windows 10 to operating systems list</span></span>

<span data-ttu-id="29433-272">Na guia implantação, os bits do Windows 10 32-bit e do Windows 10-64 foram adicionados à lista de sistemas operacionais para os quais você pode sequenciar um pacote.</span><span class="sxs-lookup"><span data-stu-id="29433-272">In the Deployment tab, Windows 10 32-bit and Windows 10-64 bit have been added to the list of operating systems for which you can sequence a package.</span></span> <span data-ttu-id="29433-273">Se você selecionar **qualquer sistema operacional**, o Windows 10 será incluído automaticamente entre os sistemas operacionais aos quais o pacote sequenciado dará suporte.</span><span class="sxs-lookup"><span data-stu-id="29433-273">If you select **Any Operating System**, Windows 10 is automatically included among the operating systems that the sequenced package will support.</span></span>

### <span data-ttu-id="29433-274">O caminho atual é exibido na parte inferior do editor do registro virtual</span><span class="sxs-lookup"><span data-stu-id="29433-274">Current path displays at bottom of virtual registry editor</span></span>

<span data-ttu-id="29433-275">Na guia registro virtual, o caminho agora é exibido na parte inferior do editor do registro virtual, que permite que você determine a chave atualmente selecionada.</span><span class="sxs-lookup"><span data-stu-id="29433-275">In the Virtual Registry tab, the path now displays at the bottom of the virtual registry editor, which enables you to determine the currently selected key.</span></span> <span data-ttu-id="29433-276">Antes, era preciso rolar pela árvore do registro para localizar a chave atualmente selecionada.</span><span class="sxs-lookup"><span data-stu-id="29433-276">Previously, you had to scroll through the registry tree to find the currently selected key.</span></span>

### <a href="" id="combined--find-and-replace--dialog-box-and-shortcut-keys-added-in-virtual-registry-editor"></a><span data-ttu-id="29433-277">Caixa de diálogo "localizar e substituir" combinada e teclas de atalho adicionadas no editor do registro virtual</span><span class="sxs-lookup"><span data-stu-id="29433-277">Combined “find and replace” dialog box and shortcut keys added in virtual registry editor</span></span>

<span data-ttu-id="29433-278">No editor de registro virtual, as teclas de atalho foram adicionadas à opção Localizar (Ctrl + F) e uma caixa de diálogo que combina as tarefas "localizar" e "substituir" foi adicionada para permitir que você localize e substitua valores e dados.</span><span class="sxs-lookup"><span data-stu-id="29433-278">In the virtual registry editor, shortcut keys have been added for the Find option (Ctrl+F), and a dialog box that combines the “find” and “replace” tasks has been added to enable you to find and replace values and data.</span></span> <span data-ttu-id="29433-279">Para acessar essa caixa de diálogo combinada, selecione uma chave e siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="29433-279">To access this combined dialog box, select a key and do one of the following:</span></span>

-   <span data-ttu-id="29433-280">Pressione **Ctrl + H**</span><span class="sxs-lookup"><span data-stu-id="29433-280">Press **Ctrl+H**</span></span>

-   <span data-ttu-id="29433-281">Clique com o botão direito do mouse em uma tecla e selecione **substituir**.</span><span class="sxs-lookup"><span data-stu-id="29433-281">Right-click a key and select **Replace**.</span></span>

-   <span data-ttu-id="29433-282">Selecione **Exibir** &gt; **substituir registro virtual** &gt; **Replace**.</span><span class="sxs-lookup"><span data-stu-id="29433-282">Select **View** &gt; **Virtual Registry** &gt; **Replace**.</span></span>

<span data-ttu-id="29433-283">Anteriormente, a caixa de diálogo "substituir" não existe e você precisava fazer alterações manualmente.</span><span class="sxs-lookup"><span data-stu-id="29433-283">Previously, the “Replace” dialog box did not exist, and you had to make changes manually.</span></span>

### <span data-ttu-id="29433-284">Renomear chaves de registro e arquivos de pacote com êxito</span><span class="sxs-lookup"><span data-stu-id="29433-284">Rename registry keys and package files successfully</span></span>

<span data-ttu-id="29433-285">Você pode renomear arquivos e chaves do registro virtual sem ter problemas com o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="29433-285">You can rename virtual registry keys and files without experiencing Sequencer issues.</span></span> <span data-ttu-id="29433-286">Anteriormente, o sequenciador parou de funcionar se você tentou renomear uma chave.</span><span class="sxs-lookup"><span data-stu-id="29433-286">Previously, the Sequencer stopped working if you tried to rename a key.</span></span>

### <span data-ttu-id="29433-287">Importar e exportar chaves do registro virtual</span><span class="sxs-lookup"><span data-stu-id="29433-287">Import and export virtual registry keys</span></span>

<span data-ttu-id="29433-288">Você pode importar e exportar chaves do registro virtual.</span><span class="sxs-lookup"><span data-stu-id="29433-288">You can import and export virtual registry keys.</span></span> <span data-ttu-id="29433-289">Para importar uma chave, clique com o botão direito do mouse no nó sob o qual deseja importar a chave, navegue até a tecla que você deseja importar e clique em **importar**.</span><span class="sxs-lookup"><span data-stu-id="29433-289">To import a key, right-click the node under which to import the key, navigate to the key you want to import, and then click **Import**.</span></span> <span data-ttu-id="29433-290">Para exportar uma chave, clique com o botão direito do mouse na chave e selecione **Exportar**.</span><span class="sxs-lookup"><span data-stu-id="29433-290">To export a key, right-click the key and select **Export**.</span></span>

### <span data-ttu-id="29433-291">Importar um diretório para o sistema de arquivos virtual</span><span class="sxs-lookup"><span data-stu-id="29433-291">Import a directory into the virtual file system</span></span>

<span data-ttu-id="29433-292">Você pode importar um diretório para o VFS.</span><span class="sxs-lookup"><span data-stu-id="29433-292">You can import a directory into the VFS.</span></span> <span data-ttu-id="29433-293">Para importar um diretório, clique na guia **arquivos de pacote** e, em seguida, clique em **Exibir** &gt; diretório de importação do sistema de **arquivos virtual** &gt; **Import Directory**.</span><span class="sxs-lookup"><span data-stu-id="29433-293">To import a directory, click the **Package Files** tab, and then click **View** &gt; **Virtual File System** &gt; **Import Directory**.</span></span> <span data-ttu-id="29433-294">Se você tentar importar um diretório que contém arquivos que já estão no VFS, a importação falhará e uma mensagem explicativa será exibida.</span><span class="sxs-lookup"><span data-stu-id="29433-294">If you try to import a directory that contains files that are already in the VFS, the import fails, and an explanatory message is displayed.</span></span> <span data-ttu-id="29433-295">Antes do App-V 5,1, não foi possível importar diretórios.</span><span class="sxs-lookup"><span data-stu-id="29433-295">Prior to App-V 5.1, you could not import directories.</span></span>

### <span data-ttu-id="29433-296">Importar ou exportar um arquivo VFS sem precisar excluí-lo e adicioná-lo novamente ao pacote</span><span class="sxs-lookup"><span data-stu-id="29433-296">Import or export a VFS file without having to delete and then add it back to the package</span></span>

<span data-ttu-id="29433-297">Você pode importar arquivos ou exportar arquivos do VFS sem precisar excluir o arquivo e adicioná-lo novamente ao pacote.</span><span class="sxs-lookup"><span data-stu-id="29433-297">You can import files to or export files from the VFS without having to delete the file and then add it back to the package.</span></span> <span data-ttu-id="29433-298">Por exemplo, você pode usar esse recurso para exportar um log de alterações para uma unidade local, editar o arquivo usando um editor externo e, em seguida, importar novamente o arquivo para o VFS.</span><span class="sxs-lookup"><span data-stu-id="29433-298">For example, you might use this feature to export a change log to a local drive, edit the file using an external editor, and then re-import the file into the VFS.</span></span>

<span data-ttu-id="29433-299">Para exportar um arquivo, selecione a guia **arquivos de pacote** , clique com o botão direito do mouse no arquivo no VFS, clique em **Exportar**e escolha um local de exportação do qual você pode fazer as edições.</span><span class="sxs-lookup"><span data-stu-id="29433-299">To export a file, select the **Package Files** tab, right-click the file in the VFS, click **Export**, and choose an export location from which you can make your edits.</span></span>

<span data-ttu-id="29433-300">Para importar um arquivo, selecione a guia **arquivos de pacote** e clique com o botão direito do mouse no arquivo que você exportou.</span><span class="sxs-lookup"><span data-stu-id="29433-300">To import a file, select the **Package Files** tab and right-click the file that you had exported.</span></span> <span data-ttu-id="29433-301">Navegue até o arquivo editado e clique em **importar**.</span><span class="sxs-lookup"><span data-stu-id="29433-301">Browse to the file that you edited, and then click **Import**.</span></span> <span data-ttu-id="29433-302">O arquivo importado substituirá o arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="29433-302">The imported file will overwrite the existing file.</span></span>

<span data-ttu-id="29433-303">Depois de importar um arquivo, você deve salvar o pacote clicando em **File** &gt; **salvar**arquivo.</span><span class="sxs-lookup"><span data-stu-id="29433-303">After you import a file, you must save the package by clicking **File** &gt; **Save**.</span></span>

### <span data-ttu-id="29433-304">O menu para adicionar um arquivo de pacote foi movido</span><span class="sxs-lookup"><span data-stu-id="29433-304">Menu for adding a package file has moved</span></span>

<span data-ttu-id="29433-305">A opção de menu para adicionar um arquivo de pacote foi movida.</span><span class="sxs-lookup"><span data-stu-id="29433-305">The menu option for adding a package file has been moved.</span></span> <span data-ttu-id="29433-306">Para localizar a opção Adicionar, selecione a guia **arquivos de pacote** e, em seguida, clique em **Exibir** &gt; **sistema de arquivos virtual** &gt; **Adicionar arquivo**.</span><span class="sxs-lookup"><span data-stu-id="29433-306">To find the Add option, select the **Package Files** tab, then click **View** &gt; **Virtual File System** &gt; **Add File**.</span></span> <span data-ttu-id="29433-307">Anteriormente, você clicou com o botão direito do mouse em uma pasta no nó VFS e escolhe **Adicionar arquivo**.</span><span class="sxs-lookup"><span data-stu-id="29433-307">Previously, you right-clicked a folder under the VFS node, and chose **Add File**.</span></span>

### <span data-ttu-id="29433-308">Nó do registro virtual expande hives do computador e do usuário por padrão</span><span class="sxs-lookup"><span data-stu-id="29433-308">Virtual registry node expands MACHINE and USER hives by default</span></span>

<span data-ttu-id="29433-309">Quando você abre o registro virtual, as hives do computador e do usuário são mostradas abaixo do nó do registro de nível superior.</span><span class="sxs-lookup"><span data-stu-id="29433-309">When you open the virtual registry, the MACHINE and USER hives are shown below the top-level REGISTRY node.</span></span> <span data-ttu-id="29433-310">Antes, era preciso expandir o nó do registro para mostrar as Hives abaixo.</span><span class="sxs-lookup"><span data-stu-id="29433-310">Previously, you had to expand the REGISTRY node to show the hives beneath.</span></span>

### <span data-ttu-id="29433-311">Habilitar ou desabilitar objetos auxiliares do navegador</span><span class="sxs-lookup"><span data-stu-id="29433-311">Enable or disable Browser Helper Objects</span></span>

<span data-ttu-id="29433-312">Você pode habilitar ou desabilitar objetos auxiliares do navegador selecionando uma nova caixa de seleção, habilitar objetos auxiliares do navegador, na guia Avançado da interface de usuário do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="29433-312">You can enable or disable Browser Helper Objects by selecting a new check box, Enable Browser Helper Objects, on the Advanced tab of the Sequencer user interface.</span></span> <span data-ttu-id="29433-313">Se objetos auxiliares do navegador:</span><span class="sxs-lookup"><span data-stu-id="29433-313">If Browser Helper Objects:</span></span>

-   <span data-ttu-id="29433-314">Existir no pacote e estiver habilitada, a caixa de seleção estará marcada por padrão.</span><span class="sxs-lookup"><span data-stu-id="29433-314">Exist in the package and are enabled, the check box is selected by default.</span></span>

-   <span data-ttu-id="29433-315">Existir no pacote e estiverem desativados, a caixa de seleção estará desmarcada por padrão.</span><span class="sxs-lookup"><span data-stu-id="29433-315">Exist in the package and are disabled, the check box is clear by default.</span></span>

-   <span data-ttu-id="29433-316">Existe no pacote, com um ou mais habilitado e um ou mais desabilitado, a caixa de seleção é definida como indeterminada por padrão.</span><span class="sxs-lookup"><span data-stu-id="29433-316">Exist in the package, with one or more enabled and one or more disabled, the check box is set to indeterminate by default.</span></span>

-   <span data-ttu-id="29433-317">Não existir no pacote, a caixa de seleção estará desabilitada.</span><span class="sxs-lookup"><span data-stu-id="29433-317">Do not exist in the package, the check box is disabled.</span></span>

### <a href="" id="bkmk-pkgconvimprove"></a><span data-ttu-id="29433-318">Melhorias no conversor de pacote</span><span class="sxs-lookup"><span data-stu-id="29433-318">Improvements to Package Converter</span></span>

<span data-ttu-id="29433-319">Agora você pode usar o conversor de pacote para converter pacotes do App-V 4,6 que contêm scripts e informações do registro e scripts dos arquivos Source. OSD agora estão incluídos na saída do conversor de pacote.</span><span class="sxs-lookup"><span data-stu-id="29433-319">You can now use the package converter to convert App-V 4.6 packages that contain scripts, and registry information and scripts from source .osd files are now included in package converter output.</span></span>

<span data-ttu-id="29433-320">Para obter mais informações, incluindo exemplos, confira [migrar para o App-V 5,1 de uma versão anterior](migrating-to-app-v-51-from-a-previous-version.md).</span><span class="sxs-lookup"><span data-stu-id="29433-320">For more information including examples, see [Migrating to App-V 5.1 from a Previous Version](migrating-to-app-v-51-from-a-previous-version.md).</span></span>

### <a href="" id="bkmk-supmultscripts"></a><span data-ttu-id="29433-321">Suporte para vários scripts em um único gatilho de evento</span><span class="sxs-lookup"><span data-stu-id="29433-321">Support for multiple scripts on a single event trigger</span></span>

<span data-ttu-id="29433-322">O App-V 5,1 oferece suporte ao uso de vários scripts em um único gatilho de evento para pacotes do App-V, incluindo pacotes que você está convertendo do App-V 4,6 para o App-V 5,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="29433-322">App-V 5.1 supports the use of multiple scripts on a single event trigger for App-V packages, including packages that you are converting from App-V 4.6 to App-V 5.0 or later.</span></span> <span data-ttu-id="29433-323">Para habilitar o uso de vários scripts, o App-V 5,1 usa um aplicativo inicializador de scripts, chamado ScriptRunner.exe, que é instalado como parte da instalação do App-V Client.</span><span class="sxs-lookup"><span data-stu-id="29433-323">To enable the use of multiple scripts, App-V 5.1 uses a script launcher application, named ScriptRunner.exe, which is installed as part of the App-V client installation.</span></span>

<span data-ttu-id="29433-324">Para obter mais informações, incluindo uma lista de gatilhos de eventos e o contexto em que scripts podem ser executados, consulte a seção scripts em [sobre a configuração dinâmica do App-V 5,1](about-app-v-51-dynamic-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="29433-324">For more information, including a list of event triggers and the context under which scripts can be run, see the Scripts section in [About App-V 5.1 Dynamic Configuration](about-app-v-51-dynamic-configuration.md).</span></span>

### <a href="" id="bkmk-hardcodepath"></a><span data-ttu-id="29433-325">Caminho codificado para a pasta de instalação é redirecionado para a raiz do sistema de arquivos virtual</span><span class="sxs-lookup"><span data-stu-id="29433-325">Hardcoded path to installation folder is redirected to virtual file system root</span></span>

<span data-ttu-id="29433-326">Quando você converte pacotes do App-V 4,6 para o 5,1, o pacote App-V 5,1 pode acessar a unidade codificada que você era obrigado a usar quando criou pacotes do 4,6.</span><span class="sxs-lookup"><span data-stu-id="29433-326">When you convert packages from App-V 4.6 to 5.1, the App-V 5.1 package can access the hardcoded drive that you were required to use when you created 4.6 packages.</span></span> <span data-ttu-id="29433-327">A letra da unidade será a unidade que você selecionou como a unidade de instalação na máquina de sequenciamento de 4,6.</span><span class="sxs-lookup"><span data-stu-id="29433-327">The drive letter will be the drive you selected as the installation drive on the 4.6 sequencing machine.</span></span> <span data-ttu-id="29433-328">(A letra da unidade padrão é Q:\\.)</span><span class="sxs-lookup"><span data-stu-id="29433-328">(The default drive letter is Q:\\.)</span></span>

<span data-ttu-id="29433-329">Anteriormente, a pasta raiz do 4,6 não foi reconhecida e não pôde ser acessada pelos pacotes do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="29433-329">Previously, the 4.6 root folder was not recognized and could not be accessed by App-V 5.0 packages.</span></span> <span data-ttu-id="29433-330">Os pacotes do App-V 5,1 podem acessar arquivos codificados por seu caminho completo ou podem enumerar programaticamente arquivos na raiz de instalação do App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="29433-330">App-V 5.1 packages can access hardcoded files by their full path or can programmatically enumerate files under the App-V 4.6 installation root.</span></span>

<span data-ttu-id="29433-331">**Detalhes técnicos:** O conversor de pacotes do App-V 5,1 salvará a pasta raiz de instalação do App-V 4,6 e nomes de pastas curtas no arquivo FilesystemMetadata.xml do elemento FileSystem.</span><span class="sxs-lookup"><span data-stu-id="29433-331">**Technical Details:** The App-V 5.1 package converter will save the App-V 4.6 installation root folder and short folder names in the FilesystemMetadata.xml file in the Filesystem element.</span></span> <span data-ttu-id="29433-332">Quando o cliente App-V 5,1 cria o processo virtual, ele mapeará solicitações da raiz de instalação do App-V 4,6 para a raiz do sistema de arquivos virtual.</span><span class="sxs-lookup"><span data-stu-id="29433-332">When the App-V 5.1 client creates the virtual process, it will map requests from the App-V 4.6 installation root to the virtual file system root.</span></span>

## <span data-ttu-id="29433-333">Como obter tecnologias do MDOP</span><span class="sxs-lookup"><span data-stu-id="29433-333">How to Get MDOP Technologies</span></span>


<span data-ttu-id="29433-334">O App-V faz parte do Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="29433-334">App-V is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="29433-335">O MDOP faz parte do Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="29433-335">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="29433-336">Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte [como faço para obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="29433-336">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>






## <span data-ttu-id="29433-337">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="29433-337">Related topics</span></span>


[<span data-ttu-id="29433-338">Notas de versão do App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="29433-338">Release Notes for App-V 5.1</span></span>](release-notes-for-app-v-51.md)









