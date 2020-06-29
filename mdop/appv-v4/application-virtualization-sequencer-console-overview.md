---
title: Visão geral do console do Application Virtualization Sequencer
description: Visão geral do console do Application Virtualization Sequencer
author: dansimp
ms.assetid: 681bb40d-2937-4645-82aa-4a44775232d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2f977fccaaded0309181a1d74c16b749498abb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799023"
---
# <span data-ttu-id="70ab5-103">Visão geral do console do Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="70ab5-103">Application Virtualization Sequencer Console Overview</span></span>


<span data-ttu-id="70ab5-104">O sequenciador do Application Virtualization (App-V) cria aplicativos para que possam ser executados em um ambiente virtual, como aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="70ab5-104">The Application Virtualization (App-V) Sequencer creates applications so that they can be run in a virtual environment, as virtual applications.</span></span> <span data-ttu-id="70ab5-105">Depois que um aplicativo é sequenciado, ele pode ser executado em um servidor App-V para computadores de destino que executam o cliente da área de trabalho do App-V ou o cliente App-V para serviços de área de trabalho remota (anteriormente serviços de terminal) usando um processo chamado streaming.</span><span class="sxs-lookup"><span data-stu-id="70ab5-105">After an application has been sequenced, it can run from an App-V Server to target computers that are running the App-V Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services) by using a process called streaming.</span></span> <span data-ttu-id="70ab5-106">O sequenciador App-V monitora o processo de instalação e configuração para aplicativos e registra todas as informações necessárias para que o aplicativo seja executado no ambiente virtual.</span><span class="sxs-lookup"><span data-stu-id="70ab5-106">The App-V Sequencer monitors the installation and setup process for applications, and it records all the information necessary for the application to run in the virtual environment.</span></span> <span data-ttu-id="70ab5-107">Esse processo também determina quais arquivos e configurações são aplicáveis a todos os usuários e quais configurações os usuários podem personalizar.</span><span class="sxs-lookup"><span data-stu-id="70ab5-107">This process also determines which files and configurations are applicable to all users and which configurations users can customize.</span></span> <span data-ttu-id="70ab5-108">Os aplicativos virtuais são executados em computadores de destino e não afetam o sistema operacional em execução no computador de destino ou em todos os aplicativos instalados no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="70ab5-108">Virtual applications run on target computers and have no effect on the operating system running on the target computer or on any applications that are installed on the target computer.</span></span>

## <span data-ttu-id="70ab5-109">Considerações de segurança do sequenciador do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="70ab5-109">Application Virtualization Sequencer Security Considerations</span></span>


<span data-ttu-id="70ab5-110">O sequenciador App-V executa todos os serviços detectados no tempo de sequenciamento usando a conta do sistema local e não aplica os descritores de segurança nas solicitações de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="70ab5-110">The App-V Sequencer runs all services detected at sequencing time using the Local System account and does not enforce security descriptors on service control requests.</span></span> <span data-ttu-id="70ab5-111">Se o serviço foi instalado usando uma conta de usuário diferente ou se os descritores de segurança destinam-se a conceder permissões de serviço específicas a grupos de usuários diferentes, considere cuidadosamente se o serviço deve ser virtualizado.</span><span class="sxs-lookup"><span data-stu-id="70ab5-111">If the service was installed using a different user account or if the security descriptors are intended to grant different user groups specific service permissions, consider carefully whether the service should be virtualized.</span></span> <span data-ttu-id="70ab5-112">Em alguns casos, você deve instalar o serviço localmente para garantir que a segurança do serviço pretendida seja preservada.</span><span class="sxs-lookup"><span data-stu-id="70ab5-112">In some cases, you should install the service locally to ensure that the intended service security is preserved.</span></span>

## <span data-ttu-id="70ab5-113">Opções do menu do console do sequenciador do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="70ab5-113">Application Virtualization Sequencer Console Menu Options</span></span>


<span data-ttu-id="70ab5-114">Os itens de menu a seguir estão disponíveis no console do App-V Sequencer:</span><span class="sxs-lookup"><span data-stu-id="70ab5-114">The following menu items are available in the App-V Sequencer Console:</span></span>

-   <span data-ttu-id="70ab5-115">**Arquivo**— contém vários comandos para ajudar a criar, abrir, modificar e salvar aplicativos sequenciados.</span><span class="sxs-lookup"><span data-stu-id="70ab5-115">**File**—Contains various commands to help create, open, modify, and save sequenced applications.</span></span>

-   <span data-ttu-id="70ab5-116">**Editar**— contém vários comandos para a edição de aplicativos virtuais existentes.</span><span class="sxs-lookup"><span data-stu-id="70ab5-116">**Edit**—Contains various commands for editing existing virtual applications.</span></span>

-   <span data-ttu-id="70ab5-117">**Modo de exibição**— contém vários comandos para exibir as propriedades de um aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="70ab5-117">**View**—Contains various commands for viewing properties of a virtual application.</span></span>

-   <span data-ttu-id="70ab5-118">**Ferramentas**— contém várias ferramentas e diagnósticos para a configuração de aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="70ab5-118">**Tools**—Contains various tools and diagnostics for configuring virtual applications.</span></span>

## <span data-ttu-id="70ab5-119">Opções da barra de ferramentas do console do sequenciador do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="70ab5-119">Application Virtualization Sequencer Console Toolbar Options</span></span>


<span data-ttu-id="70ab5-120">Os botões da barra de ferramentas a seguir estão disponíveis no console do App-V Sequencer:</span><span class="sxs-lookup"><span data-stu-id="70ab5-120">The following toolbar buttons are available in the App-V Sequencer Console:</span></span>

-   <span data-ttu-id="70ab5-121">**Novo pacote**— clique para criar um novo aplicativo sequenciado.</span><span class="sxs-lookup"><span data-stu-id="70ab5-121">**New Package**—Click to create a new sequenced application.</span></span>

-   <span data-ttu-id="70ab5-122">**Abrir**— clique para abrir um pacote de aplicativo sequenciado no console do App-V Sequencer.</span><span class="sxs-lookup"><span data-stu-id="70ab5-122">**Open**—Click to open a sequenced application package in the App-V Sequencer Console.</span></span>

-   <span data-ttu-id="70ab5-123">**Abrir para atualização**— clique para abrir um aplicativo sequenciado para atualizar ou aplicar uma atualização.</span><span class="sxs-lookup"><span data-stu-id="70ab5-123">**Open for Upgrade**—Click to open a sequenced application to upgrade or apply an update.</span></span>

-   <span data-ttu-id="70ab5-124">**Salvar**— clique para salvar um aplicativo virtual sequenciado.</span><span class="sxs-lookup"><span data-stu-id="70ab5-124">**Save**—Click to save a sequenced virtual application.</span></span>

-   <span data-ttu-id="70ab5-125">**Assistente de sequenciamento**— clique para abrir o assistente de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="70ab5-125">**Sequencing Wizard**—Click to open the Sequencing Wizard.</span></span> <span data-ttu-id="70ab5-126">Você deve usar esse botão para iniciar o assistente de sequenciamento se fizer alterações na guia **geral** em **ferramentas**  /  **Opções**.</span><span class="sxs-lookup"><span data-stu-id="70ab5-126">You should use this button to start the Sequencing Wizard if you make any changes on the **General** tab under **Tools** / **Options**.</span></span>

## <span data-ttu-id="70ab5-127">Guias do aplicativo virtual</span><span class="sxs-lookup"><span data-stu-id="70ab5-127">Virtual Application Tabs</span></span>


<span data-ttu-id="70ab5-128">As guias a seguir são exibidas quando você vê um aplicativo virtual no console do sequenciador App-V:</span><span class="sxs-lookup"><span data-stu-id="70ab5-128">The following tabs are displayed when you view a virtual application in the App-V Sequencer Console:</span></span>

-   <span data-ttu-id="70ab5-129">**Propriedades**— exibe informações sobre o aplicativo virtual selecionado.</span><span class="sxs-lookup"><span data-stu-id="70ab5-129">**Properties**—Displays information about the selected virtual application.</span></span> <span data-ttu-id="70ab5-130">Você pode atualizar o **nome** e os **comentários** do pacote associados ao aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="70ab5-130">You can update the **Package Name** and **Comments** associated with the virtual application.</span></span>

-   <span data-ttu-id="70ab5-131">**Implantação**– exibe informações sobre como o aplicativo virtual será acessado por computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="70ab5-131">**Deployment**—Displays information about how the virtual application will be accessed by target computers.</span></span> <span data-ttu-id="70ab5-132">Você pode configurar o método de entrega do aplicativo virtual, e pode configurar quais sistemas operacionais devem estar em execução no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="70ab5-132">You can configure the virtual application delivery method, and you can configure which operating systems must be running on the target computer.</span></span> <span data-ttu-id="70ab5-133">Você também pode configurar as opções de saída associadas.</span><span class="sxs-lookup"><span data-stu-id="70ab5-133">You can also configure the associated output options.</span></span> <span data-ttu-id="70ab5-134">Se você planeja ter clientes acessarem um aplicativo virtual de um arquivo, use o seguinte formato ao especificar o caminho: **file://Server/share/Path/.sft**.</span><span class="sxs-lookup"><span data-stu-id="70ab5-134">If you plan to have clients access a virtual application from a file, use the following format when specifying the path: **File://server/share/path/.sft**.</span></span> <span data-ttu-id="70ab5-135">Selecione **aplicar descritores de segurança** para preservar a segurança associada ao pacote durante uma atualização, ou as permissões serão redefinidas durante a atualização.</span><span class="sxs-lookup"><span data-stu-id="70ab5-135">Select **Enforce Security Descriptors** to preserve security associated with the package during an upgrade, or the permissions will be reset during the upgrade.</span></span>

-   <span data-ttu-id="70ab5-136">**Histórico de alterações**— exibe informações sobre atualizações feitas no aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="70ab5-136">**Change History**—Displays information about updates that have been made to the virtual application.</span></span>

-   <span data-ttu-id="70ab5-137">**Arquivos**— exibe os arquivos associados ao aplicativo virtual selecionado.</span><span class="sxs-lookup"><span data-stu-id="70ab5-137">**Files**—Displays the files associated with the selected virtual application.</span></span> <span data-ttu-id="70ab5-138">Você pode fazer revisões secundárias nas propriedades de arquivo associadas usando os campos apropriados.</span><span class="sxs-lookup"><span data-stu-id="70ab5-138">You can make minor revisions to the associated file properties by using the appropriate fields.</span></span>

-   <span data-ttu-id="70ab5-139">**Registro virtual**— exibe o registro virtual associado ao aplicativo virtual selecionado.</span><span class="sxs-lookup"><span data-stu-id="70ab5-139">**Virtual Registry**—Displays the virtual registry associated with the selected virtual application.</span></span> <span data-ttu-id="70ab5-140">Você pode adicionar ou excluir as chaves do registro clicando com o botão direito do mouse na entrada apropriada.</span><span class="sxs-lookup"><span data-stu-id="70ab5-140">You can add or delete registry keys by right-clicking the appropriate entry.</span></span>

-   <span data-ttu-id="70ab5-141">**Sistema de arquivos virtual**— exibe os sistemas de arquivos virtuais associados ao aplicativo virtual selecionado.</span><span class="sxs-lookup"><span data-stu-id="70ab5-141">**Virtual File System**—Displays the virtual file systems associated with the selected virtual application.</span></span> <span data-ttu-id="70ab5-142">Você pode adicionar, excluir ou editar entradas do sistema de arquivos nesta guia clicando com o botão direito do mouse na entrada apropriada e selecionando a opção.</span><span class="sxs-lookup"><span data-stu-id="70ab5-142">You can add, delete, or edit file system entries on this tab by right-clicking the appropriate entry and selecting the option.</span></span>

-   <span data-ttu-id="70ab5-143">**Serviços virtuais**— exibe os serviços associados ao aplicativo virtual selecionado.</span><span class="sxs-lookup"><span data-stu-id="70ab5-143">**Virtual Services**—Displays the services associated with the selected virtual application.</span></span>

-   <span data-ttu-id="70ab5-144">**OSD**— exibe informações sobre o descritor de software aberto (OSD) associado ao aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="70ab5-144">**OSD**—Displays information about the Open Software Descriptor (OSD) associated with the virtual application.</span></span> <span data-ttu-id="70ab5-145">Você pode atualizar os arquivos associados ao arquivo OSD clicando com o botão direito do mouse na entrada apropriada e selecionando a ação desejada.</span><span class="sxs-lookup"><span data-stu-id="70ab5-145">You can update the files associated with the OSD file by right-clicking the appropriate entry and selecting the action that you want.</span></span>

## <span data-ttu-id="70ab5-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70ab5-146">Related topics</span></span>


[<span data-ttu-id="70ab5-147">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="70ab5-147">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





