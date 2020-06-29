---
title: Sobre o App-V 5.0 SP3
description: Sobre o App-V 5.0 SP3
author: dansimp
ms.assetid: 67b5268b-edc1-4027-98b0-b3937dd70a6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: bc72f3f72c2b06470287dfe4ba3ed22abcc6068b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796632"
---
# <span data-ttu-id="bc712-103">Sobre o App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="bc712-103">About App-V 5.0 SP3</span></span>


<span data-ttu-id="bc712-104">Use as seções a seguir para analisar informações sobre alterações significativas que se aplicam ao Microsoft Application Virtualization (App-V) 5,0 SP3:</span><span class="sxs-lookup"><span data-stu-id="bc712-104">Use the following sections to review information about significant changes that apply to Microsoft Application Virtualization (App-V) 5.0 SP3:</span></span>

-   [<span data-ttu-id="bc712-105">Pré-requisitos de software do App-V 5,0 SP3 e configurações com suporte</span><span class="sxs-lookup"><span data-stu-id="bc712-105">App-V 5.0 SP3 software prerequisites and supported configurations</span></span>](#bkmk-sp3-prereq-configs)

-   [<span data-ttu-id="bc712-106">Migrando para o App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="bc712-106">Migrating to App-V 5.0 SP3</span></span>](#bkmk-migrate-to-50sp3)

-   [<span data-ttu-id="bc712-107">O arquivo XML do grupo de conexão criado manualmente requer a atualização para o esquema</span><span class="sxs-lookup"><span data-stu-id="bc712-107">Manually created connection group xml file requires update to schema</span></span>](#bkmk-update-schema-cg)

-   [<span data-ttu-id="bc712-108">Melhorias nos grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="bc712-108">Improvements to connection groups</span></span>](#bkmk-cg-improvements)

-   [<span data-ttu-id="bc712-109">Os administradores podem publicar e cancelar a publicação de pacotes para um usuário específico</span><span class="sxs-lookup"><span data-stu-id="bc712-109">Administrators can publish and unpublish packages for a specific user</span></span>](#bkmk-usersid-pub-pkgs-specf-user)

-   [<span data-ttu-id="bc712-110">Habilitar apenas administradores para publicar e cancelar a publicação de pacotes</span><span class="sxs-lookup"><span data-stu-id="bc712-110">Enable only administrators to publish and unpublish packages</span></span>](#bkmk-admins-only-pub-unpub-pkgs)

-   [<span data-ttu-id="bc712-111">A chave do registro RunVirtual dá suporte a pacotes publicados para o usuário</span><span class="sxs-lookup"><span data-stu-id="bc712-111">RunVirtual registry key supports packages that are published to the user</span></span>](#bkmk-runvirtual-reg-key)

-   [<span data-ttu-id="bc712-112">Novos cmdlets do PowerShell e ajuda do cmdlet atualizável</span><span class="sxs-lookup"><span data-stu-id="bc712-112">New PowerShell cmdlets and updateable cmdlet help</span></span>](#bkmk-posh-cmdlets-help)

-   [<span data-ttu-id="bc712-113">O diretório de aplicativos virtual primário (PVAD) está oculto, mas pode ser ativado</span><span class="sxs-lookup"><span data-stu-id="bc712-113">Primary virtual application directory (PVAD) is hidden but can be turned on</span></span>](#bkmk-pvad-hidden)

-   [<span data-ttu-id="bc712-114">ClientVersion é necessário para visualizar os metadados de publicação do App-V</span><span class="sxs-lookup"><span data-stu-id="bc712-114">ClientVersion is required to view App-V publishing metadata</span></span>](#bkmk-pub-metadata-clientversion)

-   [<span data-ttu-id="bc712-115">Os logs de eventos do App-V foram consolidados</span><span class="sxs-lookup"><span data-stu-id="bc712-115">App-V event logs have been consolidated</span></span>](#bkmk-event-logs-moved)

## <a href="" id="bkmk-sp3-prereq-configs"></a><span data-ttu-id="bc712-116">Pré-requisitos de software do App-V 5,0 SP3 e configurações com suporte</span><span class="sxs-lookup"><span data-stu-id="bc712-116">App-V 5.0 SP3 software prerequisites and supported configurations</span></span>


<span data-ttu-id="bc712-117">Confira os links a seguir para os pré-requisitos do software App-V 5,0 SP3 e configurações com suporte.</span><span class="sxs-lookup"><span data-stu-id="bc712-117">See the following links for the App-V 5.0 SP3 software prerequisites and supported configurations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc712-118">Links para pré-requisitos e configurações com suporte</span><span class="sxs-lookup"><span data-stu-id="bc712-118">Links to prerequisites and supported configurations</span></span></th>
<th align="left"><span data-ttu-id="bc712-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc712-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-50-sp3-prerequisites.md" data-raw-source="[App-V 5.0 SP3 Prerequisites](app-v-50-sp3-prerequisites.md)"><span data-ttu-id="bc712-120">Pré-requisitos do App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="bc712-120">App-V 5.0 SP3 Prerequisites</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="bc712-121">Software obrigatório que você deve instalar antes de iniciar a instalação do App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="bc712-121">Prerequisite software that you must install before starting the App-V 5.0 SP3 installation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)"><span data-ttu-id="bc712-122">Configurações com suporte ao App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="bc712-122">App-V 5.0 SP3 Supported Configurations</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="bc712-123">Sistemas operacionais com suporte e requisitos de hardware para os componentes App-V Server, Sequencer e cliente</span><span class="sxs-lookup"><span data-stu-id="bc712-123">Supported operating systems and hardware requirements for the App-V Server, Sequencer, and Client components</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-migrate-to-50sp3"></a><span data-ttu-id="bc712-124">Migrando para o App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="bc712-124">Migrating to App-V 5.0 SP3</span></span>


<span data-ttu-id="bc712-125">Use as informações a seguir para atualizar para o App-V 5,0 SP3 a partir de versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="bc712-125">Use the following information to upgrade to App-V 5.0 SP3 from earlier versions.</span></span>

### <span data-ttu-id="bc712-126">Antes de iniciar a atualização</span><span class="sxs-lookup"><span data-stu-id="bc712-126">Before you start the upgrade</span></span>

<span data-ttu-id="bc712-127">Revise as seguintes informações antes de iniciar a atualização:</span><span class="sxs-lookup"><span data-stu-id="bc712-127">Review the following information before you start the upgrade:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc712-128">Itens a serem revisados antes da atualização</span><span class="sxs-lookup"><span data-stu-id="bc712-128">Items to review before upgrading</span></span></th>
<th align="left"><span data-ttu-id="bc712-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc712-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-130">Componentes a serem atualizados</span><span class="sxs-lookup"><span data-stu-id="bc712-130">Components to upgrade</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="bc712-131">Servidor do App-V</span><span class="sxs-lookup"><span data-stu-id="bc712-131">App-V Server</span></span></p></li>
<li><p><span data-ttu-id="bc712-132">Sequenciador</span><span class="sxs-lookup"><span data-stu-id="bc712-132">Sequencer</span></span></p></li>
<li><p><span data-ttu-id="bc712-133">Cliente App-V ou serviços de área de trabalho remota do App-V (RDS)</span><span class="sxs-lookup"><span data-stu-id="bc712-133">App-V client or App-V Remote Desktop Services (RDS) client</span></span></p></li>
<li><p><span data-ttu-id="bc712-134">Grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="bc712-134">Connection groups</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="bc712-135">Observação</span><span class="sxs-lookup"><span data-stu-id="bc712-135">Note</span></span></strong><br/><p><span data-ttu-id="bc712-136">Para usar a interface de usuário do aplicativo cliente do App-V, baixe a versão existente do <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Microsoft Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> aplicativo de interface do usuário do cliente do Microsoft Application Virtualization 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="bc712-136">To use the App-V client user interface, download the existing version from <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Microsoft Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)">Microsoft Application Virtualization 5.0 Client UI Application</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-137">Atualizando do App-V 4. x</span><span class="sxs-lookup"><span data-stu-id="bc712-137">Upgrading from App-V 4.x</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-138">Primeiro você deve atualizar para o App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="bc712-138">You must first upgrade to App-V 5.0.</span></span> <span data-ttu-id="bc712-139">Você não pode atualizar diretamente do App-V 4. x para o App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="bc712-139">You cannot upgrade directly from App-V 4.x to App-V 5.0 SP3.</span></span></p>
<p><span data-ttu-id="bc712-140">Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="bc712-140">For more information, see:</span></span></p>
<ul>
<li><p><a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)"><span data-ttu-id="bc712-141">Sobre o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="bc712-141">About App-V 5.0</span></span></a> </p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)"><span data-ttu-id="bc712-142">Planejamento para a migração de uma versão anterior do App-V</span><span class="sxs-lookup"><span data-stu-id="bc712-142">Planning for Migrating from a Previous Version of App-V</span></span></a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-143">Atualizando a partir do App-V 5,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="bc712-143">Upgrading from App-V 5.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-144">Você pode atualizar para o App-V 5,0 SP3 diretamente de qualquer uma das seguintes versões:</span><span class="sxs-lookup"><span data-stu-id="bc712-144">You can upgrade to App-V 5.0 SP3 directly from any of the following versions:</span></span></p>
<ul>
<li><p><span data-ttu-id="bc712-145">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="bc712-145">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="bc712-146">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="bc712-146">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="bc712-147">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="bc712-147">App-V 5.0 SP2</span></span></p></li>
</ul>
<p><span data-ttu-id="bc712-148">Para atualizar para o App-V 5,0 SP3, siga as etapas nas seções restantes deste artigo.</span><span class="sxs-lookup"><span data-stu-id="bc712-148">To upgrade to App-V 5.0 SP3, follow the steps in the remaining sections of this article.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-149">Alterações necessárias nos pacotes e grupos de conexão após a atualização</span><span class="sxs-lookup"><span data-stu-id="bc712-149">Required changes to packages and connection groups after upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-150">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="bc712-150">None.</span></span> <span data-ttu-id="bc712-151">Pacotes e grupos de conexão continuarão a funcionar como no momento.</span><span class="sxs-lookup"><span data-stu-id="bc712-151">Packages and connection groups will continue to work as they currently do.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a><span data-ttu-id="bc712-152">Etapas para atualizar a infraestrutura do App-V</span><span class="sxs-lookup"><span data-stu-id="bc712-152">Steps to upgrade the App-V infrastructure</span></span>

<span data-ttu-id="bc712-153">Conclua as etapas a seguir para atualizar cada componente da infraestrutura do App-V para o App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="bc712-153">Complete the following steps to upgrade each component of the App-V infrastructure to App-V 5.0 SP3.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc712-154">Etapa</span><span class="sxs-lookup"><span data-stu-id="bc712-154">Step</span></span></th>
<th align="left"><span data-ttu-id="bc712-155">Para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="bc712-155">For more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-156">Etapa 1: Atualize o App-V Server.</span><span class="sxs-lookup"><span data-stu-id="bc712-156">Step 1: Upgrade the App-V Server.</span></span></p>
<p><span data-ttu-id="bc712-157">Se você não estiver usando o servidor App-V, pule esta etapa e vá para a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="bc712-157">If you are not using the App-V Server, skip this step and go to the next step.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="bc712-158">Observação</span><span class="sxs-lookup"><span data-stu-id="bc712-158">Note</span></span></strong><br/><p><span data-ttu-id="bc712-159">O cliente App-V 5,0 SP3 é compatível com o servidor App-V 5,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="bc712-159">The App-V 5.0 SP3 client is compatible with the App-V 5.0 SP1 Server.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="bc712-160">Siga estas etapas: </span><span class="sxs-lookup"><span data-stu-id="bc712-160">Follow these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="bc712-161">Examine as <a href="release-notes-for-app-v-50-sp3.md" data-raw-source="[Release Notes for App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)"> notas de versão do App-V 5,0 SP3 </a> para ver os problemas que podem afetar a instalação do App-v Server.</span><span class="sxs-lookup"><span data-stu-id="bc712-161">Review the <a href="release-notes-for-app-v-50-sp3.md" data-raw-source="[Release Notes for App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)">Release Notes for App-V 5.0 SP3</a> for issues that may affect the App-V Server installation.</span></span></p></li>
<li><p><span data-ttu-id="bc712-162">Siga um destes procedimentos, dependendo do método que você está usando para atualizar o banco de dados de gerenciamento e/ou banco de dados de relatórios:</span><span class="sxs-lookup"><span data-stu-id="bc712-162">Do one of the following, depending on the method you are using to upgrade the Management database and/or Reporting database:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc712-163">Método de atualização de banco de dados</span><span class="sxs-lookup"><span data-stu-id="bc712-163">Database upgrade method</span></span></th>
<th align="left"><span data-ttu-id="bc712-164">Etapa</span><span class="sxs-lookup"><span data-stu-id="bc712-164">Step</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-165">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="bc712-165">Windows Installer</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-166">Pule esta etapa e vá para a etapa 3, "se você estiver atualizando o App-V Server..."</span><span class="sxs-lookup"><span data-stu-id="bc712-166">Skip this step and go to step 3, “If you are upgrading the App-V Server...”</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-167">Scripts SQL</span><span class="sxs-lookup"><span data-stu-id="bc712-167">SQL scripts</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bc712-168">Banco de dados de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="bc712-168">Management database</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bc712-169">Para instalar ou atualizar, consulte <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> scripts do SQL para instalar ou atualizar o aplicativo de servidor de gerenciamento do App-V 5,0 SP3 falha </a> .</span><span class="sxs-lookup"><span data-stu-id="bc712-169">To install or upgrade, see <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)">SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bc712-170">Banco de dados de relatórios</span><span class="sxs-lookup"><span data-stu-id="bc712-170">Reporting database</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bc712-171">Siga as etapas em <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)"> como implantar os bancos de dados do App-V usando scripts SQL </a> .</span><span class="sxs-lookup"><span data-stu-id="bc712-171">Follow the steps in <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)">How to Deploy the App-V Databases by Using SQL Scripts</a>.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>
<p> </p></li>
<li><p><span data-ttu-id="bc712-172">Se você estiver atualizando o pacote do pacote do aplicativo App-V do App-V 5,0 SP1 3 ou posterior, conclua as etapas na seção <a href="#bkmk-check-reg-key-svr" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](#bkmk-check-reg-key-svr)"> Verifique as chaves do registro após instalar o servidor App-V 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="bc712-172">If you are upgrading the App-V Server from App-V 5.0 SP1 Hotfix Package 3 or later, complete the steps in section <a href="#bkmk-check-reg-key-svr" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](#bkmk-check-reg-key-svr)">Check registry keys after installing the App-V 5.0 SP3 Server</a>.</span></span></p></li>
<li><p><span data-ttu-id="bc712-173">Siga as etapas em <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"> como implantar o servidor do App-V 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="bc712-173">Follow the steps in <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)">How to Deploy the App-V 5.0 Server</a>.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-174">Etapa 2: Atualize o sequenciador do App-V.</span><span class="sxs-lookup"><span data-stu-id="bc712-174">Step 2: Upgrade the App-V Sequencer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-175">Veja <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"> como instalar o sequenciador </a> .</span><span class="sxs-lookup"><span data-stu-id="bc712-175">See <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)">How to Install the Sequencer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-176">Etapa 3: Atualize o cliente App-V ou o App-V RDS Client.</span><span class="sxs-lookup"><span data-stu-id="bc712-176">Step 3: Upgrade the App-V client or App-V RDS client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-177">Veja <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"> como implantar o cliente App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="bc712-177">See <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-check-reg-key-svr"></a><span data-ttu-id="bc712-178">Verifique as chaves do registro antes de instalar o App-V 5,0 SP3 Server</span><span class="sxs-lookup"><span data-stu-id="bc712-178">Check registry keys before installing the App-V 5.0 SP3 Server</span></span>

<span data-ttu-id="bc712-179">Esta é a etapa 3 da tabela anterior.</span><span class="sxs-lookup"><span data-stu-id="bc712-179">This is step 3 from the previous table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bc712-180">Quando essa etapa é necessária</span><span class="sxs-lookup"><span data-stu-id="bc712-180">When this step is required</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bc712-181">Você está atualizando a partir do App-V SP1 com qualquer pacote de hotfix subsequente instalado usando um arquivo. msp.</span><span class="sxs-lookup"><span data-stu-id="bc712-181">You are upgrading from App-V SP1 with any subsequent Hotfix Packages that you installed by using an .msp file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bc712-182">Quais componentes exigem que você siga esta etapa</span><span class="sxs-lookup"><span data-stu-id="bc712-182">Which components require that you do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bc712-183">Somente os componentes do App-V Server que você está atualizando.</span><span class="sxs-lookup"><span data-stu-id="bc712-183">Only the App-V Server components that you are upgrading.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bc712-184">Quando precisar fazer esta etapa</span><span class="sxs-lookup"><span data-stu-id="bc712-184">When you need to do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bc712-185">Antes de atualizar o servidor do App-V para o App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="bc712-185">Before you upgrade the App-V Server to App-V 5.0 SP3</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bc712-186">O que você precisa fazer</span><span class="sxs-lookup"><span data-stu-id="bc712-186">What you need to do</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bc712-187">Usando as informações nas tabelas a seguir, atualize cada valor de chave do registro sob <code>HKLM\Software\Microsoft\AppV\Server</code> o valor que você forneceu na instalação do servidor original.</span><span class="sxs-lookup"><span data-stu-id="bc712-187">Using the information in the following tables, update each registry key value under <code>HKLM\Software\Microsoft\AppV\Server</code> with the value that you provided in your original server installation.</span></span> <span data-ttu-id="bc712-188">Concluir esta etapa restaura os valores do registro que podem ter sido removidos quando os pacotes de hotfix do App-V SP1 foram instalados.</span><span class="sxs-lookup"><span data-stu-id="bc712-188">Completing this step restores registry values that may have been removed when App-V SP1 Hotfix Packages were installed.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="bc712-189">Chave ManagementDatabase</span><span class="sxs-lookup"><span data-stu-id="bc712-189">ManagementDatabase key</span></span>**

<span data-ttu-id="bc712-190">Se você estiver instalando o banco de dados de gerenciamento, defina essas chaves de registro em `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` .</span><span class="sxs-lookup"><span data-stu-id="bc712-190">If you are installing the Management database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc712-191">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="bc712-191">Key name</span></span></th>
<th align="left"><span data-ttu-id="bc712-192">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc712-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-193">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="bc712-193">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-194">Descreve se uma conta de acesso público é necessária para acessar bancos de dados de gerenciamento não locais.</span><span class="sxs-lookup"><span data-stu-id="bc712-194">Describes whether a public access account is required to access non-local management databases.</span></span> <span data-ttu-id="bc712-195">Valor é definido como "1" se for necessário.</span><span class="sxs-lookup"><span data-stu-id="bc712-195">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-196">MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="bc712-196">MANAGEMENT_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-197">Nome do banco de dados de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="bc712-197">Name of the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-198">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="bc712-198">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-199">Conta usada para acesso de leitura (pública) ao banco de dados de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="bc712-199">Account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="bc712-200">Usado quando <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> é definido como 1.</span><span class="sxs-lookup"><span data-stu-id="bc712-200">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-201">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="bc712-201">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-202">Identificador seguro (SID) da conta usada para acesso de leitura (pública) ao banco de dados de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="bc712-202">Secure identifier (SID) of the account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="bc712-203">Usado quando <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> é definido como 1.</span><span class="sxs-lookup"><span data-stu-id="bc712-203">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-204">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="bc712-204">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-205">Instância do SQL Server para o banco de dados de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="bc712-205">SQL Server instance for the Management database.</span></span></p>
<p><span data-ttu-id="bc712-206">Se o valor estiver em branco, a instância de banco de dados padrão será usada.</span><span class="sxs-lookup"><span data-stu-id="bc712-206">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-207">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="bc712-207">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-208">Conta usada para acesso de gravação (administrador) ao banco de dados de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="bc712-208">Account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-209">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="bc712-209">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-210">Identificador seguro (SID) da conta usada para acesso de gravação (administrador) ao banco de dados de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="bc712-210">Secure identifier (SID) of the account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-211">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="bc712-211">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-212">Conta de computador remoto do servidor de gerenciamento (domínio \ conta).</span><span class="sxs-lookup"><span data-stu-id="bc712-212">Management server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-213">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="bc712-213">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-214">Logon de administrador de instalação para o servidor de gerenciamento (domínio \ conta).</span><span class="sxs-lookup"><span data-stu-id="bc712-214">Installation administrator login for the Management server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-215">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="bc712-215">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-216">Valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="bc712-216">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="bc712-217">1 </strong> – o serviço de gerenciamento está no computador local, ou seja, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT está em branco.</span><span class="sxs-lookup"><span data-stu-id="bc712-217">1</strong> – the Management service is on the local computer, that is, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="bc712-218">0 </strong> - o serviço de gerenciamento está em um computador diferente do computador local.</span><span class="sxs-lookup"><span data-stu-id="bc712-218">0</strong> - the Management service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="bc712-219">Chave ManagementService</span><span class="sxs-lookup"><span data-stu-id="bc712-219">ManagementService key</span></span>**

<span data-ttu-id="bc712-220">Se você estiver instalando o servidor de gerenciamento, defina essas chaves de registro em `HKLM\Software\Microsoft\AppV\Server\ManagementService` .</span><span class="sxs-lookup"><span data-stu-id="bc712-220">If you are installing the Management server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc712-221">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="bc712-221">Key name</span></span></th>
<th align="left"><span data-ttu-id="bc712-222">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc712-222">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-223">MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="bc712-223">MANAGEMENT_ADMINACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-224">Conta ou grupo dos serviços de domínio Active Directory (AD DS) que está autorizado a gerenciar o App-V (domínio de domínio).</span><span class="sxs-lookup"><span data-stu-id="bc712-224">Active Directory Domain Services (AD DS) group or account that is authorized to manage App-V (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-225">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="bc712-225">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-226">Instância do SQL Server que contém o banco de dados de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="bc712-226">SQL server instance that contains the Management database.</span></span></p>
<p><span data-ttu-id="bc712-227">Se o valor estiver em branco, a instância de banco de dados padrão será usada.</span><span class="sxs-lookup"><span data-stu-id="bc712-227">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-228">MANAGEMENT_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="bc712-228">MANAGEMENT_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-229">Nome do SQL Server remoto com o banco de dados de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="bc712-229">Name of the remote SQL server with the Management database.</span></span></p>
<p><span data-ttu-id="bc712-230">Se o valor estiver em branco, o computador local será usado.</span><span class="sxs-lookup"><span data-stu-id="bc712-230">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="bc712-231">Chave ReportingDatabase</span><span class="sxs-lookup"><span data-stu-id="bc712-231">ReportingDatabase key</span></span>**

<span data-ttu-id="bc712-232">Se você estiver instalando o banco de dados de relatórios, defina essas chaves de registro em `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` .</span><span class="sxs-lookup"><span data-stu-id="bc712-232">If you are installing the Reporting database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc712-233">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="bc712-233">Key name</span></span></th>
<th align="left"><span data-ttu-id="bc712-234">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc712-234">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-235">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="bc712-235">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-236">Descreve se uma conta de acesso público é necessária para acessar bancos de dados de relatório não locais.</span><span class="sxs-lookup"><span data-stu-id="bc712-236">Describes whether a public access account is required to access non-local reporting databases.</span></span> <span data-ttu-id="bc712-237">Valor é definido como "1" se for necessário.</span><span class="sxs-lookup"><span data-stu-id="bc712-237">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-238">REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="bc712-238">REPORTING_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-239">Nome do banco de dados de relatório.</span><span class="sxs-lookup"><span data-stu-id="bc712-239">Name of the Reporting database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-240">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="bc712-240">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-241">Conta usada para acesso de leitura (pública) ao banco de dados de relatórios.</span><span class="sxs-lookup"><span data-stu-id="bc712-241">Account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="bc712-242">Usado quando <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> é definido como 1.</span><span class="sxs-lookup"><span data-stu-id="bc712-242">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-243">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="bc712-243">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-244">Identificador seguro (SID) da conta usada para acesso de leitura (pública) ao banco de dados de relatórios.</span><span class="sxs-lookup"><span data-stu-id="bc712-244">Secure identifier (SID) of the account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="bc712-245">Usado quando <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> é definido como 1.</span><span class="sxs-lookup"><span data-stu-id="bc712-245">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-246">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="bc712-246">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-247">Instância do SQL Server para o banco de dados de relatórios.</span><span class="sxs-lookup"><span data-stu-id="bc712-247">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="bc712-248">Se o valor estiver em branco, a instância de banco de dados padrão será usada.</span><span class="sxs-lookup"><span data-stu-id="bc712-248">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-249">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="bc712-249">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-250">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="bc712-250">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-251">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="bc712-251">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-252">Conta de computador remoto do servidor de relatório (domínio \ conta).</span><span class="sxs-lookup"><span data-stu-id="bc712-252">Reporting server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-253">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="bc712-253">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-254">Login de administrador de instalação para o servidor de relatórios (domínio \ conta).</span><span class="sxs-lookup"><span data-stu-id="bc712-254">Installation administrator login for the Reporting server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-255">REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="bc712-255">REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-256">Valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="bc712-256">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="bc712-257">1 </strong> – o serviço de relatório está no computador local, ou seja, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT está em branco.</span><span class="sxs-lookup"><span data-stu-id="bc712-257">1</strong> – the Reporting service is on the local computer, that is, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="bc712-258">0 </strong> - o serviço de relatório está em um computador diferente do computador local.</span><span class="sxs-lookup"><span data-stu-id="bc712-258">0</strong> - the Reporting service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="bc712-259">Chave ReportingService</span><span class="sxs-lookup"><span data-stu-id="bc712-259">ReportingService key</span></span>**

<span data-ttu-id="bc712-260">Se você estiver instalando o servidor de relatórios, defina essas chaves de registro em `HKLM\Software\Microsoft\AppV\Server\ReportingService` .</span><span class="sxs-lookup"><span data-stu-id="bc712-260">If you are installing the Reporting server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc712-261">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="bc712-261">Key name</span></span></th>
<th align="left"><span data-ttu-id="bc712-262">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc712-262">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-263">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="bc712-263">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-264">Instância do SQL Server para o banco de dados de relatórios.</span><span class="sxs-lookup"><span data-stu-id="bc712-264">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="bc712-265">Se o valor estiver em branco, a instância de banco de dados padrão será usada.</span><span class="sxs-lookup"><span data-stu-id="bc712-265">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-266">REPORTING_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="bc712-266">REPORTING_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-267">Nome do SQL Server remoto com o banco de dados de relatórios.</span><span class="sxs-lookup"><span data-stu-id="bc712-267">Name of the remote SQL server with the Reporting database.</span></span></p>
<p><span data-ttu-id="bc712-268">Se o valor estiver em branco, o computador local será usado.</span><span class="sxs-lookup"><span data-stu-id="bc712-268">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-update-schema-cg"></a><span data-ttu-id="bc712-269">O arquivo XML do grupo de conexão criado manualmente requer a atualização para o esquema</span><span class="sxs-lookup"><span data-stu-id="bc712-269">Manually created connection group xml file requires update to schema</span></span>


<span data-ttu-id="bc712-270">Se você estiver criando manualmente o arquivo XML do grupo de conexão e quiser usar os novos recursos "pacotes opcionais" e "usar qualquer versão" descritos em [melhorias nos grupos de conexão](#bkmk-cg-improvements), você deve especificar o seguinte esquema no arquivo XML:</span><span class="sxs-lookup"><span data-stu-id="bc712-270">If you are manually creating the connection group XML file, and want to use the new “optional packages” and “use any version” features that are described in [Improvements to connection groups](#bkmk-cg-improvements), you must specify the following schema in the XML file:</span></span>

`xmlns="http://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"`

<span data-ttu-id="bc712-271">Para obter exemplos e mais informações, consulte [sobre o arquivo de grupo de conexão](about-the-connection-group-file.md).</span><span class="sxs-lookup"><span data-stu-id="bc712-271">For examples and more information, see [About the Connection Group File](about-the-connection-group-file.md).</span></span>

## <a href="" id="bkmk-cg-improvements"></a><span data-ttu-id="bc712-272">Melhorias nos grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="bc712-272">Improvements to connection groups</span></span>


<span data-ttu-id="bc712-273">Você pode gerenciar grupos de conexão com mais facilidade usando pacotes opcionais e outros aprimoramentos que foram adicionados no App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="bc712-273">You can manage connection groups more easily by using optional packages and other improvements that have been added in App-V 5.0 SP3.</span></span> <span data-ttu-id="bc712-274">A tabela a seguir resume as tarefas que você pode executar usando os novos recursos de grupo de conexão e links para informações mais detalhadas sobre cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="bc712-274">The following table summarizes the tasks that you can perform by using the new connection group features, and links to more detailed information about each task.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc712-275">Tarefa/recurso</span><span class="sxs-lookup"><span data-stu-id="bc712-275">Task/feature</span></span></th>
<th align="left"><span data-ttu-id="bc712-276">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc712-276">Description</span></span></th>
<th align="left"><span data-ttu-id="bc712-277">Links para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="bc712-277">Links to more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-278">Habilitar um grupo de conexão para incluir pacotes opcionais</span><span class="sxs-lookup"><span data-stu-id="bc712-278">Enable a connection group to include optional packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-279">Incluir pacotes opcionais em um grupo de conexão permite que você determine dinamicamente quais aplicativos serão incluídos no ambiente virtual do grupo de conexão, com base nos aplicativos aos quais os usuários estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="bc712-279">Including optional packages in a connection group enables you to dynamically determine which applications will be included in the connection group’s virtual environment, based on the applications that users are entitled to.</span></span></p>
<p><span data-ttu-id="bc712-280">Você não precisa gerenciar o máximo de grupos de conexão porque pode misturar pacotes opcionais e não opcionais no mesmo grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="bc712-280">You don’t need to manage as many connection groups because you can mix optional and non-optional packages in the same connection group.</span></span> <span data-ttu-id="bc712-281">A combinação de pacotes permite que diferentes grupos de usuários usem o mesmo grupo de conexão, mesmo que os usuários possam ter apenas um pacote em comum.</span><span class="sxs-lookup"><span data-stu-id="bc712-281">Mixing packages allows different groups of users to use the same connection group, even though users might have only one package in common.</span></span></p>
<p><strong><span data-ttu-id="bc712-282">Exemplo </strong> : você pode habilitar um pacote com o Microsoft Office para todos os usuários, mas habilitar diferentes pacotes opcionais, que contêm diferentes plug-ins do Office para subconjuntos diferentes de usuários.</span><span class="sxs-lookup"><span data-stu-id="bc712-282">Example</strong>: You can enable a package with Microsoft Office for all users, but enable different optional packages, which contain different Office plug-ins, to different subsets of users.</span></span></p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"><span data-ttu-id="bc712-283">Como usar pacotes opcionais em grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="bc712-283">How to Use Optional Packages in Connection Groups</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-284">Cancelar a publicação ou excluir um pacote opcional sem alterar o grupo de conexões</span><span class="sxs-lookup"><span data-stu-id="bc712-284">Unpublish or delete an optional package without changing the connection group</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-285">Cancele a publicação ou exclua ou cancele a publicação de um pacote opcional, que está em um grupo de conexão, sem precisar desabilitar ou habilitar novamente o grupo de conexão no cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="bc712-285">Unpublish or delete, or unpublish and republish an optional package, which is in a connection group, without having to disable or re-enable the connection group on the App-V client.</span></span></p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"><span data-ttu-id="bc712-286">Como usar pacotes opcionais em grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="bc712-286">How to Use Optional Packages in Connection Groups</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-287">Publicar grupos de conexão que contêm pacotes publicados pelo usuário e publicados globalmente</span><span class="sxs-lookup"><span data-stu-id="bc712-287">Publish connection groups that contain user-published and globally published packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-288">Crie um grupo de conexões publicada pelo usuário que contenha pacotes publicados pelo usuário e publicados globalmente.</span><span class="sxs-lookup"><span data-stu-id="bc712-288">Create a user-published connection group that contains user-published and globally published packages.</span></span></p></td>
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md)"><span data-ttu-id="bc712-289">Como criar um grupo de conexão com pacotes publicados pelo usuário e globalmente publicados</span><span class="sxs-lookup"><span data-stu-id="bc712-289">How to Create a Connection Group with User-Published and Globally Published Packages</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-290">Fazer um grupo de conexão ignorar a versão do pacote</span><span class="sxs-lookup"><span data-stu-id="bc712-290">Make a connection group ignore the package version</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-291">Configure um grupo de conexão para aceitar qualquer versão de um pacote, o que permite que você atualize um pacote sem precisar desabilitar o grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="bc712-291">Configure a connection group to accept any version of a package, which enables you to upgrade a package without having to disable the connection group.</span></span> <span data-ttu-id="bc712-292">Além disso, se houver um pacote opcional com uma versão incorreta no grupo de conexão, o pacote será ignorado e não bloqueará a criação do ambiente virtual do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="bc712-292">In addition, if there is an optional package with an incorrect version in the connection group, the package is ignored and won’t block the connection group’s virtual environment from being created.</span></span></p></td>
<td align="left"><p><a href="how-to-make-a-connection-group-ignore-the-package-version.md" data-raw-source="[How to Make a Connection Group Ignore the Package Version](how-to-make-a-connection-group-ignore-the-package-version.md)"><span data-ttu-id="bc712-293">Como criar um grupo de conexão para ignorar a versão do pacote</span><span class="sxs-lookup"><span data-stu-id="bc712-293">How to Make a Connection Group Ignore the Package Version</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-294">Limitar os recursos de publicação dos usuários finais</span><span class="sxs-lookup"><span data-stu-id="bc712-294">Limit end users’ publishing capabilities</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-295">Habilite somente administradores (não usuários finais) para publicar pacotes e habilitar grupos de conexão.</span><span class="sxs-lookup"><span data-stu-id="bc712-295">Enable only administrators (not end users) to publish packages and to enable connection groups.</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-296">Para obter informações sobre grupos de conexão, consulte <a href="how-to-allow-only-administrators-to-enable-connection-groups.md" data-raw-source="[How to Allow Only Administrators to Enable Connection Groups](how-to-allow-only-administrators-to-enable-connection-groups.md)"> como permitir que apenas administradores habilitem grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="bc712-296">For information about connection groups, see <a href="how-to-allow-only-administrators-to-enable-connection-groups.md" data-raw-source="[How to Allow Only Administrators to Enable Connection Groups](how-to-allow-only-administrators-to-enable-connection-groups.md)">How to Allow Only Administrators to Enable Connection Groups</span></span></a></p>
<p><span data-ttu-id="bc712-297">Para obter informações sobre pacotes, consulte os seguintes artigos:</span><span class="sxs-lookup"><span data-stu-id="bc712-297">For information about packages, see the following articles:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc712-298">Método</span><span class="sxs-lookup"><span data-stu-id="bc712-298">Method</span></span></th>
<th align="left"><span data-ttu-id="bc712-299">Link para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="bc712-299">Link to more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-300">Console de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="bc712-300">Management console</span></span></p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-50.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md)"><span data-ttu-id="bc712-301">Como publicar um pacote usando o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="bc712-301">How to Publish a Package by Using the Management Console</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-302">PowerShell</span><span class="sxs-lookup"><span data-stu-id="bc712-302">PowerShell</span></span></p></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg)"><span data-ttu-id="bc712-303">Como gerenciar grupos de conexão em um computador autônomo usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bc712-303">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-304">Sistema de distribuição de software eletrônico de terceiros</span><span class="sxs-lookup"><span data-stu-id="bc712-304">Third-party electronic software delivery system</span></span></p></td>
<td align="left"><p><a href="how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md" data-raw-source="[How to Enable Only Administrators to Publish Packages by Using an ESD](how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md)"><span data-ttu-id="bc712-305">Como permitir que apenas administradores publiquem pacotes usando ESD</span><span class="sxs-lookup"><span data-stu-id="bc712-305">How to Enable Only Administrators to Publish Packages by Using an ESD</span></span></a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-306">Habilitar ou desabilitar um grupo de conexão para um usuário específico</span><span class="sxs-lookup"><span data-stu-id="bc712-306">Enable or disable a connection group for a specific user</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-307">Os administradores podem habilitar ou desabilitar um grupo de conexão para um usuário específico usando o <strong> parâmetro opcional – userid </strong> com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bc712-307">Administrators can enable or disable a connection group for a specific user by using the optional <strong>–UserSID</strong> parameter with the following cmdlets:</span></span></p>
<ul>
<li><p><span data-ttu-id="bc712-308">Enable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="bc712-308">Enable-AppVClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="bc712-309">Disable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="bc712-309">Disable-AppVClientConnectionGroup</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic)"><span data-ttu-id="bc712-310">Como gerenciar grupos de conexão em um computador autônomo usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bc712-310">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-311">Mesclando caminhos de pacote idênticos em um diretório virtual em grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="bc712-311">Merging identical package paths into one virtual directory in connection groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-312">Se dois ou mais pacotes em um grupo de conexão contiverem caminhos de diretório idênticos, os caminhos serão mesclados em um único diretório virtual dentro do ambiente virtual do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="bc712-312">If two or more packages in a connection group contain identical directory paths, the paths are merged into a single virtual directory inside the connection group virtual environment.</span></span></p>
<p><span data-ttu-id="bc712-313">Essa mesclagem de caminhos permite que um aplicativo em um pacote Acesse arquivos que estão em um pacote diferente.</span><span class="sxs-lookup"><span data-stu-id="bc712-313">This merging of paths allows an application in one package to access files that are in a different package.</span></span></p></td>
<td align="left"><p><a href="about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp)"><span data-ttu-id="bc712-314">Sobre o ambiente Virtual do grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="bc712-314">About the Connection Group Virtual Environment</span></span></a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-usersid-pub-pkgs-specf-user"></a><span data-ttu-id="bc712-315">Os administradores podem publicar e cancelar a publicação de pacotes para um usuário específico</span><span class="sxs-lookup"><span data-stu-id="bc712-315">Administrators can publish and unpublish packages for a specific user</span></span>


<span data-ttu-id="bc712-316">Os administradores podem usar os seguintes cmdlets para publicar ou cancelar a publicação de pacotes para um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="bc712-316">Administrators can use the following cmdlets to publish or unpublish packages for a specific user.</span></span> <span data-ttu-id="bc712-317">Para usar os cmdlets, insira o parâmetro **– userid** , seguido do Sid (identificador de segurança) do usuário.</span><span class="sxs-lookup"><span data-stu-id="bc712-317">To use the cmdlets, enter the **–UserSID** parameter, followed by the user’s security identifier (SID).</span></span> <span data-ttu-id="bc712-318">Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="bc712-318">For more information, see:</span></span>

-   [<span data-ttu-id="bc712-319">Como gerenciar pacotes do App-V 5.0 em execução em um computador autônomo usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="bc712-319">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span>](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-pub-pkg-a-user-standalone-posh)

-   [<span data-ttu-id="bc712-320">Como gerenciar pacotes do App-V 5.0 em execução em um computador autônomo usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="bc712-320">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span>](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-unpub-pkg-specfc-use)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc712-321">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bc712-321">Cmdlet</span></span></th>
<th align="left"><span data-ttu-id="bc712-322">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bc712-322">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-323">Publicar-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="bc712-323">Publish-AppvClientPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-324">Publish-AppvClientPackage "ContosoApplication"-Usuáriosid S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="bc712-324">Publish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-325">Cancelar publicação-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="bc712-325">Unpublish-AppvClientPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-326">Cancelar publicação-AppvClientPackage "ContosoApplication"-Usuáriosid S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="bc712-326">Unpublish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-admins-only-pub-unpub-pkgs"></a><span data-ttu-id="bc712-327">Habilitar apenas administradores para publicar e cancelar a publicação de pacotes</span><span class="sxs-lookup"><span data-stu-id="bc712-327">Enable only administrators to publish and unpublish packages</span></span>


<span data-ttu-id="bc712-328">Você pode habilitar somente administradores (não usuários finais) para publicar e cancelar a publicação de pacotes usando um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="bc712-328">You can enable only administrators (not end users) to publish and unpublish packages by using one of the following methods:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc712-329">Método</span><span class="sxs-lookup"><span data-stu-id="bc712-329">Method</span></span></th>
<th align="left"><span data-ttu-id="bc712-330">Mais informações</span><span class="sxs-lookup"><span data-stu-id="bc712-330">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-331">Configuração da Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="bc712-331">Group Policy setting</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-332">Navegue até o seguinte nó de objeto de política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="bc712-332">Navigate to the following Group Policy Object node:</span></span></p>
<p><strong><span data-ttu-id="bc712-333">Política de configuração do computador &gt; &gt; modelos administrativos do &gt; &gt; App-V &gt; Publishing </strong> .</span><span class="sxs-lookup"><span data-stu-id="bc712-333">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing</strong>.</span></span></p>
<p><span data-ttu-id="bc712-334">Habilite a <strong> configuração de política exigir publicação como administrador </strong> .</span><span class="sxs-lookup"><span data-stu-id="bc712-334">Enable the <strong>Require publish as administrator</strong> Group Policy setting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-335">PowerShell</span><span class="sxs-lookup"><span data-stu-id="bc712-335">PowerShell</span></span></p></td>
<td align="left"><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)"><span data-ttu-id="bc712-336">Como gerenciar pacotes do App-V 5.0 em execução em um computador autônomo usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="bc712-336">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-runvirtual-reg-key"></a><span data-ttu-id="bc712-337">A chave do registro RunVirtual dá suporte a pacotes publicados para o usuário</span><span class="sxs-lookup"><span data-stu-id="bc712-337">RunVirtual registry key supports packages that are published to the user</span></span>


<span data-ttu-id="bc712-338">O App-V 5,0 SP3 adiciona suporte para o uso da chave do registro **RunVirtual** com aplicativos virtualizados que estão em pacotes publicados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="bc712-338">App-V 5.0 SP3 adds support for using the **RunVirtual** registry key with virtualized applications that are in user-published packages.</span></span> <span data-ttu-id="bc712-339">A chave do registro **RunVirtual** permite executar um aplicativo instalado localmente em um ambiente virtual, juntamente com aplicativos que foram virtualizados usando o App-V.</span><span class="sxs-lookup"><span data-stu-id="bc712-339">The **RunVirtual** registry key lets you run a locally installed application in a virtual environment, along with applications that have been virtualized by using App-V.</span></span>

<span data-ttu-id="bc712-340">Anteriormente, os aplicativos virtualizados nos pacotes do App-V precisavam ser publicados globalmente.</span><span class="sxs-lookup"><span data-stu-id="bc712-340">Previously, the virtualized applications in App-V packages had to be published globally.</span></span> <span data-ttu-id="bc712-341">Para saber mais sobre o **RunVirtual** e sobre outros métodos de execução de aplicativos instalados localmente em um ambiente virtual com aplicativos virtualizados, consulte [executando um aplicativo instalado localmente dentro de um ambiente virtual com aplicativos virtualizados](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md).</span><span class="sxs-lookup"><span data-stu-id="bc712-341">For more about **RunVirtual** and about other methods of running locally installed applications in a virtual environment with virtualized applications, see [Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md).</span></span>

## <a href="" id="bkmk-posh-cmdlets-help"></a><span data-ttu-id="bc712-342">Novos cmdlets do PowerShell e ajuda do cmdlet atualizável</span><span class="sxs-lookup"><span data-stu-id="bc712-342">New PowerShell cmdlets and updateable cmdlet help</span></span>


<span data-ttu-id="bc712-343">Novos cmdlets do PowerShell e a ajuda do cmdlet atualizável estão incluídos no App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="bc712-343">New PowerShell cmdlets and updateable cmdlet help are included in App-V 5.0 SP3.</span></span> <span data-ttu-id="bc712-344">Para baixar os módulos do cmdlet, consulte [como carregar os cmdlets do PowerShell e obter ajuda do cmdlet](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md#bkmk-load-cmdlets).</span><span class="sxs-lookup"><span data-stu-id="bc712-344">To download the cmdlet modules, see [How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md#bkmk-load-cmdlets).</span></span>

### <span data-ttu-id="bc712-345">Novos cmdlets do PowerShell Server do App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="bc712-345">New App-V 5.0 SP3 Server PowerShell cmdlets</span></span>

<span data-ttu-id="bc712-346">Novos cmdlets do Windows PowerShell para o App-V Server foram adicionados para ajudar você a gerenciar grupos de conexão.</span><span class="sxs-lookup"><span data-stu-id="bc712-346">New Windows PowerShell cmdlets for the App-V Server have been added to help you manage connection groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc712-347">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bc712-347">Cmdlet</span></span></th>
<th align="left"><span data-ttu-id="bc712-348">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc712-348">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-349">Add-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="bc712-349">Add-AppvServerConnectionGroupPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-350">Acrescenta um pacote ao final de um grupo de conexão&#39;a lista de pacotes e permite que você configure o pacote como opcional e/ou sem nenhuma versão dentro do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="bc712-350">Appends a package to the end of a connection group&#39;s package list and enables you to configure the package as optional and/or with no version within the connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-351">Set-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="bc712-351">Set-AppvServerConnectionGroupPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-352">Permite que você edite detalhes sobre o pacote do grupo de conexão, como se ele é opcional.</span><span class="sxs-lookup"><span data-stu-id="bc712-352">Enables you to edit details about the connection group package, such as whether it is optional.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-353">Remove-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="bc712-353">Remove-AppvServerConnectionGroupPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-354">Remove um pacote de um grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="bc712-354">Removes a package from a connection group.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-get-cmdlet-help"></a><span data-ttu-id="bc712-355">Obtendo ajuda para os cmdlets do PowerShell</span><span class="sxs-lookup"><span data-stu-id="bc712-355">Getting help for the PowerShell cmdlets</span></span>

<span data-ttu-id="bc712-356">A ajuda do cmdlet está disponível nos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="bc712-356">Cmdlet help is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc712-357">Formato</span><span class="sxs-lookup"><span data-stu-id="bc712-357">Format</span></span></th>
<th align="left"><span data-ttu-id="bc712-358">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc712-358">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-359">Como um módulo para download</span><span class="sxs-lookup"><span data-stu-id="bc712-359">As a downloadable module</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-360">Para obter a ajuda mais recente após o download do módulo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="bc712-360">To get the latest help after downloading the cmdlet module:</span></span></p>
<ol>
<li><p><span data-ttu-id="bc712-361">Abra o Windows PowerShell ou o ambiente de script integrado do Windows PowerShell (ISE).</span><span class="sxs-lookup"><span data-stu-id="bc712-361">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span></p></li>
<li><p><span data-ttu-id="bc712-362">Digite um dos seguintes comandos para carregar os cmdlets do módulo que você deseja:</span><span class="sxs-lookup"><span data-stu-id="bc712-362">Type one of the following commands to load the cmdlets for the module you want:</span></span></p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc712-363">Componente App-V</span><span class="sxs-lookup"><span data-stu-id="bc712-363">App-V component</span></span></th>
<th align="left"><span data-ttu-id="bc712-364">Comando para digitar</span><span class="sxs-lookup"><span data-stu-id="bc712-364">Command to type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-365">Servidor do App-V</span><span class="sxs-lookup"><span data-stu-id="bc712-365">App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-366">Update-Help-AppvServer do módulo</span><span class="sxs-lookup"><span data-stu-id="bc712-366">Update-Help-Module AppvServer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-367">Sequenciador App-V</span><span class="sxs-lookup"><span data-stu-id="bc712-367">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-368">Update-Help-AppvSequencer do módulo</span><span class="sxs-lookup"><span data-stu-id="bc712-368">Update-Help-Module AppvSequencer</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-369">Cliente App-V</span><span class="sxs-lookup"><span data-stu-id="bc712-369">App-V client</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-370">Update-Help-AppvClient do módulo</span><span class="sxs-lookup"><span data-stu-id="bc712-370">Update-Help-Module AppvClient</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-371">No TechNet como páginas da Web</span><span class="sxs-lookup"><span data-stu-id="bc712-371">On TechNet as web pages</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-372">Consulte o nó App-V em <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> automação do Microsoft Desktop Optimization Pack with Windows PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="bc712-372">See the App-V node under <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)">Microsoft Desktop Optimization Pack Automation with Windows PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="bc712-373">Para obter mais informações, consulte [como carregar cmdlets do PowerShell e obter ajuda do cmdlet](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md).</span><span class="sxs-lookup"><span data-stu-id="bc712-373">For more information, see [How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md).</span></span>

## <a href="" id="bkmk-pvad-hidden"></a><span data-ttu-id="bc712-374">O diretório de aplicativos virtual primário (PVAD) está oculto, mas pode ser ativado</span><span class="sxs-lookup"><span data-stu-id="bc712-374">Primary virtual application directory (PVAD) is hidden but can be turned on</span></span>


<span data-ttu-id="bc712-375">O diretório de aplicativos virtual primário (PVAD) está oculto no App-V 5,0 SP3, mas você pode ativá-lo novamente e torná-lo visível usando um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="bc712-375">The primary virtual application directory (PVAD) is hidden in App-V 5.0 SP3, but you can turn it back on and make it visible by using one of the following methods:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc712-376">Método</span><span class="sxs-lookup"><span data-stu-id="bc712-376">Method</span></span></th>
<th align="left"><span data-ttu-id="bc712-377">Etapas</span><span class="sxs-lookup"><span data-stu-id="bc712-377">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc712-378">Usar um parâmetro de linha de comando</span><span class="sxs-lookup"><span data-stu-id="bc712-378">Use a command line parameter</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc712-379">Passe o <strong> parâmetro – EnablePVADControl </strong> para a <strong>Sequencer.exe</strong> .</span><span class="sxs-lookup"><span data-stu-id="bc712-379">Pass the <strong>–EnablePVADControl</strong> parameter to the <strong>Sequencer.exe</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc712-380">Criar uma subchave do registro</span><span class="sxs-lookup"><span data-stu-id="bc712-380">Create a registry subkey</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="bc712-381">No editor do registro, navegue até:</span><span class="sxs-lookup"><span data-stu-id="bc712-381">In the Registry Editor, navigate to:</span></span> <code>HKLM\SOFTWARE\Microsoft\AppV\Sequencer\Compatibility</code></p>
<div class="alert">
<strong><span data-ttu-id="bc712-382">Observação</span><span class="sxs-lookup"><span data-stu-id="bc712-382">Note</span></span></strong><br/><p><span data-ttu-id="bc712-383">Se a <code>Compatibility</code> subchave não existir, você deverá criá-la.</span><span class="sxs-lookup"><span data-stu-id="bc712-383">If the <code>Compatibility</code> subkey doesn’t exist, you must create it.</span></span></p>
</div>
<div>

</div></li>
<li><p><span data-ttu-id="bc712-384">Crie um valor DWORD chamado <strong> EnablePVADControl </strong> e defina o valor como <strong> 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="bc712-384">Create a DWORD Value named <strong>EnablePVADControl</strong>, and set the value to <strong>1</strong>.</span></span></p>
<p><span data-ttu-id="bc712-385">O valor <strong> 0 </strong> significa que o PVAD está oculto.</span><span class="sxs-lookup"><span data-stu-id="bc712-385">A value of <strong>0</strong> means that PVAD is hidden.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>



<span data-ttu-id="bc712-386">**Saiba mais sobre o PVAD:** Ao usar o sequenciador para criar um pacote, você pode inserir qualquer caminho de instalação para o pacote.</span><span class="sxs-lookup"><span data-stu-id="bc712-386">**More about PVAD:** When you use the Sequencer to create a package, you can enter any installation path for the package.</span></span> <span data-ttu-id="bc712-387">Nas versões anteriores do App-V, você deve especificar o diretório de aplicativos virtual primário (PVAD) do aplicativo como o caminho.</span><span class="sxs-lookup"><span data-stu-id="bc712-387">In past versions of App-V, you were required to specify the primary virtual application directory (PVAD) of the application as the path.</span></span> <span data-ttu-id="bc712-388">PVAD é o diretório no qual você normalmente instalaria um aplicativo em seu computador local se não estivesse usando o App-V.</span><span class="sxs-lookup"><span data-stu-id="bc712-388">PVAD is the directory to which you would typically install an application on your local computer if you weren’t using App-V.</span></span> <span data-ttu-id="bc712-389">Por exemplo, se você estiver instalando o Office em um computador, o PVAD normalmente seria C:\\Arquivos de Files\\Microsoft Office\\.</span><span class="sxs-lookup"><span data-stu-id="bc712-389">For example, if you were installing Office on a computer, the PVAD typically would be C:\\Program Files\\Microsoft Office\\.</span></span>

## <a href="" id="bkmk-pub-metadata-clientversion"></a><span data-ttu-id="bc712-390">ClientVersion é necessário para visualizar os metadados de publicação do App-V</span><span class="sxs-lookup"><span data-stu-id="bc712-390">ClientVersion is required to view App-V publishing metadata</span></span>


<span data-ttu-id="bc712-391">No App-V 5,0 SP3, você deve fornecer os seguintes valores no endereço quando consulta o servidor de publicação App-V para metadados:</span><span class="sxs-lookup"><span data-stu-id="bc712-391">In App-V 5.0 SP3, you must provide the following values in the address when you query the App-V Publishing server for metadata:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc712-392">Valor</span><span class="sxs-lookup"><span data-stu-id="bc712-392">Value</span></span></th>
<th align="left"><span data-ttu-id="bc712-393">Detalhes adicionais</span><span class="sxs-lookup"><span data-stu-id="bc712-393">Additional details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bc712-394">ClientVersion</span><span class="sxs-lookup"><span data-stu-id="bc712-394">ClientVersion</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bc712-395">Se você omitir <strong> o </strong> parâmetro ClientVersion da consulta, os metadados excluirão os novos recursos do App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="bc712-395">If you omit the <strong>ClientVersion</strong> parameter from the query, the metadata excludes the new App-V 5.0 SP3 features.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bc712-396">ClientOS</span><span class="sxs-lookup"><span data-stu-id="bc712-396">ClientOS</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bc712-397">Você deve fornecer esse valor apenas se selecionar sistemas operacionais específicos do cliente quando você sequenciar o pacote.</span><span class="sxs-lookup"><span data-stu-id="bc712-397">You have to provide this value only if you select specific client operating systems when you sequence the package.</span></span> <span data-ttu-id="bc712-398">Se você selecionar o padrão (todos os sistemas operacionais), não especifique esse valor na consulta.</span><span class="sxs-lookup"><span data-stu-id="bc712-398">If you select the default (all operating systems), do not specify this value in the query.</span></span></p>
<p><span data-ttu-id="bc712-399">Se você omitir <strong> o </strong> parâmetro ClientOS da consulta, somente os pacotes que foram sequenciados para dar suporte a qualquer sistema operacional aparecem nos metadados.</span><span class="sxs-lookup"><span data-stu-id="bc712-399">If you omit the <strong>ClientOS</strong> parameter from the query, only the packages that were sequenced to support any operating system appear in the metadata.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="bc712-400">Para ver a sintaxe e os exemplos dessa consulta, consulte [exibindo os metadados de publicação do App-V Server](viewing-app-v-server-publishing-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="bc712-400">For syntax and examples of this query, see [Viewing App-V Server Publishing Metadata](viewing-app-v-server-publishing-metadata.md).</span></span>

## <a href="" id="bkmk-event-logs-moved"></a><span data-ttu-id="bc712-401">Os logs de eventos do App-V foram consolidados</span><span class="sxs-lookup"><span data-stu-id="bc712-401">App-V event logs have been consolidated</span></span>


<span data-ttu-id="bc712-402">Os logs de eventos a seguir, anteriormente localizados em **logs de aplicativos e serviços/Microsoft/AppV/ &lt; app &gt; -V**, foram movidos para **aplicativos e logs de serviços/Microsoft/AppV/ServiceLog**.</span><span class="sxs-lookup"><span data-stu-id="bc712-402">The following event logs, previously located at **Applications and Services Logs/Microsoft/AppV/&lt;App-V component&gt;**, have been moved to **Applications and Services Logs/Microsoft/AppV/ServiceLog**.</span></span>

<span data-ttu-id="bc712-403">Para exibir os logs, selecione **Exibir** &gt; **Mostrar logs analíticos e de depuração** no aplicativo visualizador de eventos.</span><span class="sxs-lookup"><span data-stu-id="bc712-403">To view the logs, select **View** &gt; **Show Analytic and Debug Logs** in the Event Viewer application.</span></span>

<span data-ttu-id="bc712-404">Cliente-cliente de catálogo-cliente de integração-cliente de orquestração-cliente PackageConfig cliente-cliente de script-cliente-serviço cliente-Vemgr cliente-VFSC FilesystemMetadataLibrary ManifestLibrary PolicyLibrary subsistemas-subsistemas do AppPath-subsistemas com FTA-</span><span class="sxs-lookup"><span data-stu-id="bc712-404">Client-Catalog Client-Integration Client-Orchestration Client-PackageConfig Client-Scripting Client-Service Client-Vemgr Client-VFSC FilesystemMetadataLibrary ManifestLibrary PolicyLibrary Subsystems-ActiveX Subsystems-AppPath Subsystems-Com Subsystems-fta</span></span>

## <span data-ttu-id="bc712-405">Como obter tecnologias do MDOP</span><span class="sxs-lookup"><span data-stu-id="bc712-405">How to Get MDOP Technologies</span></span>


<span data-ttu-id="bc712-406">O App-V faz parte do Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="bc712-406">App-V is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="bc712-407">O MDOP faz parte do Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="bc712-407">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="bc712-408">Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte [como faço para obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="bc712-408">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>






## <span data-ttu-id="bc712-409">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc712-409">Related topics</span></span>


[<span data-ttu-id="bc712-410">Notas de versão do App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="bc712-410">Release Notes for App-V 5.0 SP3</span></span>](release-notes-for-app-v-50-sp3.md)









