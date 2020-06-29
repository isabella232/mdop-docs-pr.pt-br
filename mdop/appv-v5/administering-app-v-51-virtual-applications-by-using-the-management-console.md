---
title: Administrar aplicativos virtuais do App-V 5.1 usando o Console de Gerenciamento
description: Administrar aplicativos virtuais do App-V 5.1 usando o Console de Gerenciamento
author: dansimp
ms.assetid: a4d078aa-ec54-4fa4-9463-bfb3b971d724
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63ec965519bedef08b09c961dc5d1c90e1d8d694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796606"
---
# <span data-ttu-id="2fe4a-103">Administrar aplicativos virtuais do App-V 5.1 usando o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2fe4a-103">Administering App-V 5.1 Virtual Applications by Using the Management Console</span></span>


<span data-ttu-id="2fe4a-104">Use o servidor de gerenciamento do Microsoft Application Virtualization (App-V) 5,1 para gerenciar pacotes, grupos de conexão e acesso a pacotes em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="2fe4a-104">Use the Microsoft Application Virtualization (App-V) 5.1 management server to manage packages, connection groups, and package access in your environment.</span></span> <span data-ttu-id="2fe4a-105">O servidor publica os ícones de aplicativo, atalhos e associações de tipo de arquivo para computadores autorizados que executam o cliente App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="2fe4a-105">The server publishes application icons, shortcuts, and file type associations to authorized computers that run the App-V 5.1 client.</span></span> <span data-ttu-id="2fe4a-106">Um ou mais servidores de gerenciamento geralmente compartilham um repositório de dados comum para informações de configuração e pacote.</span><span class="sxs-lookup"><span data-stu-id="2fe4a-106">One or more management servers typically share a common data store for configuration and package information.</span></span>

<span data-ttu-id="2fe4a-107">O servidor de gerenciamento usa os grupos dos serviços de domínio Active Directory (AD DS) para gerenciar a autorização do usuário e tem o SQL Server instalado para gerenciar o banco de dados e o repositório de dados.</span><span class="sxs-lookup"><span data-stu-id="2fe4a-107">The management server uses Active Directory Domain Services (AD DS) groups to manage user authorization and has SQL Server installed to manage the database and data store.</span></span>

<span data-ttu-id="2fe4a-108">Como os servidores de gerenciamento transmitem aplicativos para usuários finais sob demanda, esses servidores são adequados para configurações de sistema que têm LANs confiáveis e de alta largura de banda.</span><span class="sxs-lookup"><span data-stu-id="2fe4a-108">Because the management servers stream applications to end users on demand, these servers are ideally suited for system configurations that have reliable, high-bandwidth LANs.</span></span> <span data-ttu-id="2fe4a-109">O servidor de gerenciamento consiste nos seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="2fe4a-109">The management server consists of the following components:</span></span>

-   <span data-ttu-id="2fe4a-110">Servidor de gerenciamento – Use o servidor de gerenciamento para gerenciar pacotes e grupos de conexão.</span><span class="sxs-lookup"><span data-stu-id="2fe4a-110">Management Server – Use the management server to manage packages and connection groups.</span></span>

-   <span data-ttu-id="2fe4a-111">Publishing Server – use o Publishing Server para implantar pacotes em computadores que executam o cliente App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="2fe4a-111">Publishing Server – Use the publishing server to deploy packages to computers that run the App-V 5.1 client.</span></span>

-   <span data-ttu-id="2fe4a-112">Banco de dados de gerenciamento – Use o banco de dados de gerenciamento para gerenciar o acesso ao pacote e publicar a sincronização do servidor com o servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="2fe4a-112">Management Database - Use the management database to manage the package access and to publish the server’s synchronization with the management server.</span></span>

## <span data-ttu-id="2fe4a-113">Tarefas do console de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2fe4a-113">Management Console tasks</span></span>


<span data-ttu-id="2fe4a-114">As tarefas mais comuns que você pode executar com o console de gerenciamento do App-V 5,1 são:</span><span class="sxs-lookup"><span data-stu-id="2fe4a-114">The most common tasks that you can perform with the App-V 5.1 Management console are:</span></span>

-   [<span data-ttu-id="2fe4a-115">Como conectar-se ao Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2fe4a-115">How to Connect to the Management Console</span></span>](how-to-connect-to-the-management-console-51.md)

-   [<span data-ttu-id="2fe4a-116">Como adicionar ou atualizar pacotes usando o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2fe4a-116">How to Add or Upgrade Packages by Using the Management Console</span></span>](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md)

-   [<span data-ttu-id="2fe4a-117">Como configurar o acesso a pacotes usando o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2fe4a-117">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

-   [<span data-ttu-id="2fe4a-118">Como publicar um pacote usando o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2fe4a-118">How to Publish a Package by Using the Management Console</span></span>](how-to-publish-a-package-by-using-the-management-console-51.md)

-   [<span data-ttu-id="2fe4a-119">Como excluir um pacote no Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2fe4a-119">How to Delete a Package in the Management Console</span></span>](how-to-delete-a-package-in-the-management-console-51.md)

-   [<span data-ttu-id="2fe4a-120">Como adicionar ou remover um administrador usando o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2fe4a-120">How to Add or Remove an Administrator by Using the Management Console</span></span>](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)

-   [<span data-ttu-id="2fe4a-121">Como registrar e cancelar o registro de um servidor publicação usando o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2fe4a-121">How to Register and Unregister a Publishing Server by Using the Management Console</span></span>](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console51.md)

-   [<span data-ttu-id="2fe4a-122">Como criar um arquivo de configuração personalizada usando o Console de Gerenciamento do App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="2fe4a-122">How to Create a Custom Configuration File by Using the App-V 5.1 Management Console</span></span>](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md)

-   [<span data-ttu-id="2fe4a-123">Como transferir configurações e acesso para outra versão de um pacote usando o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2fe4a-123">How to Transfer Access and Configurations to Another Version of a Package by Using the Management Console</span></span>](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console51.md)

-   [<span data-ttu-id="2fe4a-124">Como personalizar extensões de aplicativos virtuais para um grupo do AD específico usando o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2fe4a-124">How to Customize Virtual Applications Extensions for a Specific AD Group by Using the Management Console</span></span>](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console51.md)

-   [<span data-ttu-id="2fe4a-125">Como exibir e configurar aplicativos e extensões de aplicativos virtuais padrão usando o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2fe4a-125">How to View and Configure Applications and Default Virtual Application Extensions by Using the Management Console</span></span>](how-to-view-and-configure-applications-and-default-virtual-application-extensions-by-using-the-management-console-beta.md)

<span data-ttu-id="2fe4a-126">Os principais elementos do console de gerenciamento do App-V 5,1 são:</span><span class="sxs-lookup"><span data-stu-id="2fe4a-126">The main elements of the App-V 5.1 Management Console are:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2fe4a-127">Guia Console de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2fe4a-127">Management Console tab</span></span></th>
<th align="left"><span data-ttu-id="2fe4a-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="2fe4a-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2fe4a-129">Guia pacotes</span><span class="sxs-lookup"><span data-stu-id="2fe4a-129">Packages tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fe4a-130">Use a <strong> </strong> guia pacotes para adicionar ou atualizar pacotes.</span><span class="sxs-lookup"><span data-stu-id="2fe4a-130">Use the <strong>PACKAGES</strong> tab to add or upgrade packages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2fe4a-131">Guia grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="2fe4a-131">Connection Groups tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fe4a-132">Use a <strong> guia grupos de conexão </strong> para gerenciar grupos de conexão.</span><span class="sxs-lookup"><span data-stu-id="2fe4a-132">Use the <strong>CONNECTION GROUPS</strong> tab to manage connection groups.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2fe4a-133">Guia servidores</span><span class="sxs-lookup"><span data-stu-id="2fe4a-133">Servers tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fe4a-134">Use a <strong> </strong> guia servidores para registrar um novo servidor.</span><span class="sxs-lookup"><span data-stu-id="2fe4a-134">Use the <strong>SERVERS</strong> tab to register a new server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2fe4a-135">Guia administradores</span><span class="sxs-lookup"><span data-stu-id="2fe4a-135">Administrators tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fe4a-136">Use a <strong> </strong> guia administradores para registrar, adicionar ou remover administradores em seu ambiente do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="2fe4a-136">Use the <strong>ADMINISTRATORS</strong> tab to register, add, or remove administrators in your App-V 5.1 environment.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2fe4a-137">**Importante**  O JavaScript deve estar ativado no navegador que abre o console de gerenciamento da Web.</span><span class="sxs-lookup"><span data-stu-id="2fe4a-137">**Important** JavaScript must be enabled on the browser that opens the Web Management Console.</span></span>

 






## <a href="" id="other-resources-for-this-app-v-5-1-deployment-"></a><span data-ttu-id="2fe4a-138">Outros recursos para esta implantação do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="2fe4a-138">Other resources for this App-V 5.1 deployment</span></span>


-   [<span data-ttu-id="2fe4a-139">Guia do administrador do Microsoft Application Virtualization 5,1</span><span class="sxs-lookup"><span data-stu-id="2fe4a-139">Microsoft Application Virtualization 5.1 Administrator's Guide</span></span>](microsoft-application-virtualization-51-administrators-guide.md)

-   [<span data-ttu-id="2fe4a-140">Operações para o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="2fe4a-140">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





