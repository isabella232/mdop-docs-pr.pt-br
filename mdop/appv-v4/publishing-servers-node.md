---
title: Nó Servidores de Publicação
description: Nó Servidores de Publicação
author: dansimp
ms.assetid: b5823c6c-15bc-4e8d-aeeb-acc366ffedd1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c001e246c63919773d29a2317d5a43937c0813f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796797"
---
# <span data-ttu-id="aa59f-103">Nó Servidores de Publicação</span><span class="sxs-lookup"><span data-stu-id="aa59f-103">Publishing Servers Node</span></span>


<span data-ttu-id="aa59f-104">O nó **servidores de publicação** é um nível abaixo do nó **virtualização do aplicativo** no painel **escopo** do console de gerenciamento de cliente do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="aa59f-104">The **Publishing Servers** node is one level below the **Application Virtualization** node in the **Scope** pane of the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="aa59f-105">Quando você seleciona esse nó, o painel de **resultados** exibe uma lista de servidores de publicação.</span><span class="sxs-lookup"><span data-stu-id="aa59f-105">When you select this node, the **Results** pane displays a list of publishing servers.</span></span>

<span data-ttu-id="aa59f-106">Clique com o botão direito do mouse no nó **servidores de publicação** para exibir um menu pop-up que contém os elementos a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa59f-106">Right-click the **Publishing Servers** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-server"></a>**<span data-ttu-id="aa59f-107">Novo servidor</span><span class="sxs-lookup"><span data-stu-id="aa59f-107">New Server</span></span>**  
<span data-ttu-id="aa59f-108">Este item de menu exibe o assistente para novo servidor.</span><span class="sxs-lookup"><span data-stu-id="aa59f-108">This menu item displays the New Server Wizard.</span></span> <span data-ttu-id="aa59f-109">Este assistente consiste em duas páginas:</span><span class="sxs-lookup"><span data-stu-id="aa59f-109">This wizard consists of two pages:</span></span>

1.  <span data-ttu-id="aa59f-110">Insira um nome de exibição do servidor e um tipo de servidor:</span><span class="sxs-lookup"><span data-stu-id="aa59f-110">Enter a server display name and server type:</span></span>

    -   <span data-ttu-id="aa59f-111">**Nome para exibição**— Insira um nome que você deseja exibir para o servidor.</span><span class="sxs-lookup"><span data-stu-id="aa59f-111">**Display Name**—Enter a name that you want displayed for the server.</span></span> <span data-ttu-id="aa59f-112">Este campo está em branco por padrão.</span><span class="sxs-lookup"><span data-stu-id="aa59f-112">This field is blank by default.</span></span>

    -   <span data-ttu-id="aa59f-113">**Tipo**— escolha o tipo de servidor na lista suspensa de tipos de servidor.</span><span class="sxs-lookup"><span data-stu-id="aa59f-113">**Type**—Choose the server type from the drop-down list of server types.</span></span>

2.  <span data-ttu-id="aa59f-114">Especifique as configurações de conexão para o servidor:</span><span class="sxs-lookup"><span data-stu-id="aa59f-114">Specify the connection settings for the server:</span></span>

    -   <span data-ttu-id="aa59f-115">**Nome do host**— Insira o nome ou o endereço IP do servidor.</span><span class="sxs-lookup"><span data-stu-id="aa59f-115">**Host Name**—Enter the name or IP address for the server.</span></span>

    -   <span data-ttu-id="aa59f-116">**Porta**— Insira um valor numérico que corresponda ao número da porta.</span><span class="sxs-lookup"><span data-stu-id="aa59f-116">**Port**—Enter a numeric value that corresponds to the port number.</span></span> <span data-ttu-id="aa59f-117">O valor padrão é 554 se o tipo de servidor for "servidor de virtualização de aplicativos" e 80 se o tipo de servidor for "servidor HTTP padrão".</span><span class="sxs-lookup"><span data-stu-id="aa59f-117">The default value is 554 if the server type is "Application Virtualization Server" and 80 if the server type is "Standard HTTP Server."</span></span>

    -   <span data-ttu-id="aa59f-118">**Path**— este campo é definido como padrão "/" e é somente leitura quando o tipo de servidor é "servidor de virtualização de aplicativos" ou "servidor de virtualização de aplicativo de segurança aprimorada".</span><span class="sxs-lookup"><span data-stu-id="aa59f-118">**Path**—This field defaults to "/" and is read-only when the server type is "Application Virtualization Server" or “Enhanced Security Application Virtualization Server”.</span></span> <span data-ttu-id="aa59f-119">Quando o tipo de servidor é "servidor HTTP padrão" ou "servidor HTTP de segurança aprimorada", o campo **caminho** também pode ser editado.</span><span class="sxs-lookup"><span data-stu-id="aa59f-119">When the server type is “Standard HTTP Server” or “Enhanced Security HTTP Server”, the **Path** field is also editable.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="aa59f-120">Nova janela a partir daqui</span><span class="sxs-lookup"><span data-stu-id="aa59f-120">New Window from Here</span></span>**  
<span data-ttu-id="aa59f-121">Selecione este item de menu para abrir um novo console de gerenciamento com o nó selecionado como nó raiz.</span><span class="sxs-lookup"><span data-stu-id="aa59f-121">Select this menu item to open a new management console with the selected node as the root node.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="aa59f-122">Exportar lista</span><span class="sxs-lookup"><span data-stu-id="aa59f-122">Export List</span></span>**  
<span data-ttu-id="aa59f-123">Você pode usar esse item de menu para criar um arquivo de texto delimitado por tabulação que contenha o conteúdo do painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="aa59f-123">You can use this menu item to create a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="aa59f-124">Este item exibe uma caixa de diálogo de **salvamento de arquivo** padrão na qual você especifica o local para o arquivo de texto que está criando.</span><span class="sxs-lookup"><span data-stu-id="aa59f-124">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="aa59f-125">Exibir</span><span class="sxs-lookup"><span data-stu-id="aa59f-125">View</span></span>**  
<span data-ttu-id="aa59f-126">Esta lista pop-up de itens de menu permite que você altere a aparência e o conteúdo do painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="aa59f-126">This pop-up list of menu items enables you to change the appearance and content of the **Results** pane.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="aa59f-127">Atualizar</span><span class="sxs-lookup"><span data-stu-id="aa59f-127">Refresh</span></span>**  
<span data-ttu-id="aa59f-128">Selecione este item para atualizar o console de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="aa59f-128">Select this item to refresh the management console.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="aa59f-129">Ajuda</span><span class="sxs-lookup"><span data-stu-id="aa59f-129">Help</span></span>**  
<span data-ttu-id="aa59f-130">Este item exibe o sistema de ajuda do console de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="aa59f-130">This item displays the help system for the management console.</span></span>

## <span data-ttu-id="aa59f-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa59f-131">Related topics</span></span>


[<span data-ttu-id="aa59f-132">Painel Resultados de Servidores de Publicação</span><span class="sxs-lookup"><span data-stu-id="aa59f-132">Publishing Servers Results Pane</span></span>](publishing-servers-results-pane.md)

[<span data-ttu-id="aa59f-133">Colunas do painel Resultados de Servidores de Publicação</span><span class="sxs-lookup"><span data-stu-id="aa59f-133">Publishing Servers Results Pane Columns</span></span>](publishing-servers-results-pane-columns.md)

 

 





