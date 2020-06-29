---
title: Nó Políticas de Provedor
description: Nó Políticas de Provedor
author: dansimp
ms.assetid: 89b47076-7732-4128-93cc-8e6d5b671c8e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221171b22471a4a8614b13023b24dd21fd571dd3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796804"
---
# <span data-ttu-id="b3c25-103">Nó Políticas de Provedor</span><span class="sxs-lookup"><span data-stu-id="b3c25-103">Provider Policies Node</span></span>


<span data-ttu-id="b3c25-104">O nó **políticas do provedor** é um nível abaixo do nó do sistema de virtualização do aplicativo no painel **escopo** no console de gerenciamento do servidor do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="b3c25-104">The **Provider Policies** node is one level below the Application Virtualization System node in the **Scope** pane in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="b3c25-105">Quando você seleciona esse nó, o painel de **resultados** exibe uma lista de políticas de provedor.</span><span class="sxs-lookup"><span data-stu-id="b3c25-105">When you select this node, the **Results** pane displays a list of provider policies.</span></span> <span data-ttu-id="b3c25-106">Clique com o botão direito do mouse no nó **políticas do provedor** para exibir um menu pop-up que contém os elementos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b3c25-106">Right-click the **Provider Policies** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-provider-policy"></a>**<span data-ttu-id="b3c25-107">Nova política de provedor</span><span class="sxs-lookup"><span data-stu-id="b3c25-107">New Provider Policy</span></span>**  
<span data-ttu-id="b3c25-108">Exibe o assistente de nova política de provedor.</span><span class="sxs-lookup"><span data-stu-id="b3c25-108">Displays the New Provider Policy Wizard.</span></span> <span data-ttu-id="b3c25-109">Este assistente consiste nas seguintes páginas:</span><span class="sxs-lookup"><span data-stu-id="b3c25-109">This wizard consists of the following pages:</span></span>

1.  <span data-ttu-id="b3c25-110">Digite um nome no campo **nome da política do provedor** .</span><span class="sxs-lookup"><span data-stu-id="b3c25-110">Enter a name in the **Provider Policy Name** field.</span></span> <span data-ttu-id="b3c25-111">Marque a caixa de seleção **gerenciar área de trabalho cliente usando o console de gerenciamento** , se desejar essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="b3c25-111">Select the **Manage client desktop using the Management Console** check box if you want that capability.</span></span> <span data-ttu-id="b3c25-112">Marque uma ou ambas as caixas de seleção a seguir se quiser a funcionalidade associada:</span><span class="sxs-lookup"><span data-stu-id="b3c25-112">Select one or both of the following check boxes if you want the associated functionality:</span></span>

    -   **<span data-ttu-id="b3c25-113">Atualizar a configuração de publicação quando um usuário faz logon</span><span class="sxs-lookup"><span data-stu-id="b3c25-113">Refresh publishing configuration when a user logs in</span></span>**

    -   <span data-ttu-id="b3c25-114">**Atualizar a configuração a cada**.</span><span class="sxs-lookup"><span data-stu-id="b3c25-114">**Refresh configuration every**.</span></span> <span data-ttu-id="b3c25-115">Depois de selecionar essa opção, insira um número e selecione a unidade no menu suspenso.</span><span class="sxs-lookup"><span data-stu-id="b3c25-115">After selecting this option, enter a number and select the unit from the drop-down menu.</span></span> <span data-ttu-id="b3c25-116">As entradas válidas variam de um mínimo de **30 minutos** a um máximo de **999 dias**.</span><span class="sxs-lookup"><span data-stu-id="b3c25-116">Valid entries range from a minimum of **30 minutes** to a maximum of **999 days**.</span></span>

2.  <span data-ttu-id="b3c25-117">Clique em **Adicionar** ou **remover** para adicionar ou remover uma atribuição de grupo.</span><span class="sxs-lookup"><span data-stu-id="b3c25-117">Click **Add** or **Remove** to add or remove a group assignment.</span></span> <span data-ttu-id="b3c25-118">Use a caixa de diálogo de pesquisa padrão do **Windows** para localizar um grupo de usuários.</span><span class="sxs-lookup"><span data-stu-id="b3c25-118">Use the standard **Windows Browse** dialog box to find a user group.</span></span>

3.  <span data-ttu-id="b3c25-119">Marque uma das seguintes caixas de seleção na caixa de diálogo **configuração de pipeline do provedor** para habilitar o recurso associado:</span><span class="sxs-lookup"><span data-stu-id="b3c25-119">Select one of the following check boxes on the **Provider Pipeline Configuration** dialog box to enable the associated feature:</span></span>

    -   <span data-ttu-id="b3c25-120">**Autenticação**— selecione o tipo de autenticação na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="b3c25-120">**Authentication**—Select the type of authentication from the drop-down list.</span></span>

    -   **<span data-ttu-id="b3c25-121">Impor as configurações de permissão de acesso</span><span class="sxs-lookup"><span data-stu-id="b3c25-121">Enforce Access Permission Settings</span></span>**

    -   **<span data-ttu-id="b3c25-122">Registrar informações de uso</span><span class="sxs-lookup"><span data-stu-id="b3c25-122">Log Usage Information</span></span>**

    -   <span data-ttu-id="b3c25-123">**Licenciamento**— selecione um esquema de imposição na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="b3c25-123">**Licensing**—Select an enforcement scheme from the drop-down list.</span></span>

4.  <span data-ttu-id="b3c25-124">Clique em **concluir** para adicionar a nova política de provedor.</span><span class="sxs-lookup"><span data-stu-id="b3c25-124">Click **Finish** to add the new provider policy.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="b3c25-125">Exibir</span><span class="sxs-lookup"><span data-stu-id="b3c25-125">View</span></span>**  
<span data-ttu-id="b3c25-126">Altera a aparência e o conteúdo do painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="b3c25-126">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="b3c25-127">Nova janela a partir daqui</span><span class="sxs-lookup"><span data-stu-id="b3c25-127">New Window from Here</span></span>**  
<span data-ttu-id="b3c25-128">Abre um novo console de gerenciamento com o nó selecionado como nó raiz.</span><span class="sxs-lookup"><span data-stu-id="b3c25-128">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="b3c25-129">Atualizar</span><span class="sxs-lookup"><span data-stu-id="b3c25-129">Refresh</span></span>**  
<span data-ttu-id="b3c25-130">Atualiza o modo de exibição do servidor.</span><span class="sxs-lookup"><span data-stu-id="b3c25-130">Refreshes the view of the server.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="b3c25-131">Exportar lista</span><span class="sxs-lookup"><span data-stu-id="b3c25-131">Export List</span></span>**  
<span data-ttu-id="b3c25-132">Cria um arquivo de texto delimitado por tabulação que contém o conteúdo do painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="b3c25-132">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="b3c25-133">Este item exibe uma caixa de diálogo de **salvamento de arquivo** padrão na qual você especifica o local para o arquivo de texto que está criando.</span><span class="sxs-lookup"><span data-stu-id="b3c25-133">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="b3c25-134">Ajuda</span><span class="sxs-lookup"><span data-stu-id="b3c25-134">Help</span></span>**  
<span data-ttu-id="b3c25-135">Exibe o sistema de ajuda do console de gerenciamento do servidor do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="b3c25-135">Displays the help system for the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="b3c25-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b3c25-136">Related topics</span></span>


[<span data-ttu-id="b3c25-137">Server Management Console: nó Políticas de Provedor</span><span class="sxs-lookup"><span data-stu-id="b3c25-137">Server Management Console: Provider Policies Node</span></span>](server-management-console-provider-policies-node.md)

 

 





