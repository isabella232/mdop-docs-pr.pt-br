---
title: Painel Resultados de Licenças de Aplicativos
description: Painel Resultados de Licenças de Aplicativos
author: dansimp
ms.assetid: 8b519715-b2fe-451e-ad9b-e9b73f454961
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e5a86c22e67e061ec873317c455958536fae75b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797539"
---
# <span data-ttu-id="ce576-103">Painel Resultados de Licenças de Aplicativos</span><span class="sxs-lookup"><span data-stu-id="ce576-103">Applications Licenses Results Pane</span></span>


<span data-ttu-id="ce576-104">O painel **resultados de licenças** do aplicativo no console de gerenciamento do aplicativo virtualização de aplicativos exibe uma lista dos grupos de licenças de aplicativos e licenças de aplicativos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ce576-104">The **Applications Licenses Results** pane in the Application Virtualization Server Management Console displays a list of the available application license groups and application licenses.</span></span>

<span data-ttu-id="ce576-105">Clique com o botão direito do mouse em qualquer grupo de licenças do aplicativo para exibir um menu pop-up que contém os elementos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ce576-105">Right-click any application license group to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-unlimited-license"></a>**<span data-ttu-id="ce576-106">Nova licença ilimitada</span><span class="sxs-lookup"><span data-stu-id="ce576-106">New Unlimited License</span></span>**  
<span data-ttu-id="ce576-107">Exibe o assistente de nova licença ilimitada.</span><span class="sxs-lookup"><span data-stu-id="ce576-107">Displays the New Unlimited License Wizard.</span></span> <span data-ttu-id="ce576-108">Essa opção está disponível somente quando o grupo de licenças não tem licenças.</span><span class="sxs-lookup"><span data-stu-id="ce576-108">This option is available only when the license group has no licenses.</span></span> <span data-ttu-id="ce576-109">Este assistente consiste em três páginas:</span><span class="sxs-lookup"><span data-stu-id="ce576-109">This wizard consists of three pages:</span></span>

1.  <span data-ttu-id="ce576-110">Insira um nome de grupo no campo **nome do grupo de licenças de aplicativos** e um valor (em minutos) no campo de aviso de **expiração da licença** .</span><span class="sxs-lookup"><span data-stu-id="ce576-110">Enter a group name in the **Applications License Group Name** field and a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="ce576-111">(Você pode inserir qualquer valor de 0 a 100.) Você também pode usar as setas para cima e para baixo para selecionar o número de minutos.</span><span class="sxs-lookup"><span data-stu-id="ce576-111">(You can enter any value from 0–100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="ce576-112">Insira um breve texto descritivo no campo **Descrição da licença** e marque a caixa de seleção **habilitado** .</span><span class="sxs-lookup"><span data-stu-id="ce576-112">Enter brief descriptive text in the **License Description** field, and select the **Enabled** check box.</span></span> <span data-ttu-id="ce576-113">Opcionalmente, você pode usar o campo **data de expiração** para especificar uma data de expiração para a licença.</span><span class="sxs-lookup"><span data-stu-id="ce576-113">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="ce576-114">Você pode marcar a caixa de seleção padrão ou usar o utilitário de calendário para navegar até a data de expiração desejada.</span><span class="sxs-lookup"><span data-stu-id="ce576-114">You can select the default check box or use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="ce576-115">Clique em **concluir** para adicionar a nova licença.</span><span class="sxs-lookup"><span data-stu-id="ce576-115">Click **Finish** to add the new license.</span></span>

<a href="" id="new-concurrent-license"></a>**<span data-ttu-id="ce576-116">Nova licença simultânea</span><span class="sxs-lookup"><span data-stu-id="ce576-116">New Concurrent License</span></span>**  
<span data-ttu-id="ce576-117">Exibe o assistente de nova licença simultânea.</span><span class="sxs-lookup"><span data-stu-id="ce576-117">Displays the New Concurrent License Wizard.</span></span> <span data-ttu-id="ce576-118">Essa opção está disponível somente quando o grupo de licenças não tem licenças ilimitadas.</span><span class="sxs-lookup"><span data-stu-id="ce576-118">This option is available only when the license group has no unlimited licenses.</span></span> <span data-ttu-id="ce576-119">Este assistente consiste nas páginas a seguir e é quase idêntico ao novo assistente de licença ilimitada:</span><span class="sxs-lookup"><span data-stu-id="ce576-119">This wizard consists of the following pages and is almost identical to the New Unlimited License Wizard:</span></span>

1.  <span data-ttu-id="ce576-120">Insira um nome de grupo no campo **nome do grupo de licenças de aplicativos** e um valor (em minutos) no campo de aviso de **expiração da licença** .</span><span class="sxs-lookup"><span data-stu-id="ce576-120">Enter a group name in the **Applications License Group Name** field and a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="ce576-121">(Você pode inserir qualquer valor de 0 a 100.) Você também pode usar as setas para cima e para baixo para selecionar o número de minutos.</span><span class="sxs-lookup"><span data-stu-id="ce576-121">(You can enter any value from 0–100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="ce576-122">Insira um breve texto descritivo no campo **Descrição da licença** e insira um valor no campo **quantidade da licença simultânea** .</span><span class="sxs-lookup"><span data-stu-id="ce576-122">Enter brief descriptive text in the **License Description** field, and enter a value in the **Concurrent License Quantity** field.</span></span> <span data-ttu-id="ce576-123">Você também pode usar as setas para cima e para baixo para especificar o número de licenças simultâneas.</span><span class="sxs-lookup"><span data-stu-id="ce576-123">You can also use the up and down arrows to specify the number of concurrent licenses.</span></span> <span data-ttu-id="ce576-124">Marque a caixa de seleção **habilitado** para habilitar a licença.</span><span class="sxs-lookup"><span data-stu-id="ce576-124">Select the **Enabled** check box to enable the license.</span></span> <span data-ttu-id="ce576-125">Opcionalmente, você pode usar o campo **data de expiração** para selecionar uma data de expiração para a licença.</span><span class="sxs-lookup"><span data-stu-id="ce576-125">Optionally, you can use the **Expiration Date** field to select an expiration date for the license.</span></span> <span data-ttu-id="ce576-126">Você pode marcar a caixa de seleção para usar a data de expiração exibida ou pode usar o utilitário de calendário para navegar até a data de expiração desejada.</span><span class="sxs-lookup"><span data-stu-id="ce576-126">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="ce576-127">Clique em **concluir** para adicionar as novas licenças.</span><span class="sxs-lookup"><span data-stu-id="ce576-127">Click **Finish** to add the new licenses.</span></span>

<a href="" id="new-named-license"></a>**<span data-ttu-id="ce576-128">Nova licença nomeada</span><span class="sxs-lookup"><span data-stu-id="ce576-128">New Named License</span></span>**  
<span data-ttu-id="ce576-129">Exibe o novo assistente de licença nomeada.</span><span class="sxs-lookup"><span data-stu-id="ce576-129">Displays the New Named License Wizard.</span></span> <span data-ttu-id="ce576-130">Essa opção está disponível somente quando o grupo de licenças não tem licenças ilimitadas.</span><span class="sxs-lookup"><span data-stu-id="ce576-130">This option is available only when the license group has no unlimited licenses.</span></span> <span data-ttu-id="ce576-131">Este assistente consiste nas seguintes páginas:</span><span class="sxs-lookup"><span data-stu-id="ce576-131">This wizard consists of the following pages:</span></span>

1.  <span data-ttu-id="ce576-132">Insira um nome de grupo no campo **nome do grupo de licenças de aplicativos** e um valor (em minutos) no campo de aviso de **expiração da licença** .</span><span class="sxs-lookup"><span data-stu-id="ce576-132">Enter a group name in the **Applications License Group Name** field and a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="ce576-133">(Você pode inserir qualquer valor de 0 a 100.) Você também pode usar as setas para cima e para baixo para selecionar o número de minutos.</span><span class="sxs-lookup"><span data-stu-id="ce576-133">(You can enter any value from 0–100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="ce576-134">Insira um breve texto descritivo na **Descrição da licença**e marque a caixa de seleção **habilitado** .</span><span class="sxs-lookup"><span data-stu-id="ce576-134">Enter brief descriptive text in the **License Description**, and select the **Enabled** check box.</span></span> <span data-ttu-id="ce576-135">Opcionalmente, você pode usar o campo **data de expiração** para especificar uma data de expiração para a licença.</span><span class="sxs-lookup"><span data-stu-id="ce576-135">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="ce576-136">Você pode marcar a caixa de seleção para usar a data de expiração exibida ou usar o utilitário de calendário para navegar até a data de expiração desejada.</span><span class="sxs-lookup"><span data-stu-id="ce576-136">You can select the check box to use the displayed expiration date, or use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="ce576-137">Clique em **Adicionar**, **Editar**ou **remover** usuários nomeados.</span><span class="sxs-lookup"><span data-stu-id="ce576-137">Click **Add**, **Edit**, or **Remove** named users.</span></span>

4.  <span data-ttu-id="ce576-138">Clique em **concluir** para adicionar a nova licença.</span><span class="sxs-lookup"><span data-stu-id="ce576-138">Click **Finish** to add the new license.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="ce576-139">Nova janela a partir daqui</span><span class="sxs-lookup"><span data-stu-id="ce576-139">New Window from Here</span></span>**  
<span data-ttu-id="ce576-140">Abre um novo console de gerenciamento com o nó selecionado como nó raiz.</span><span class="sxs-lookup"><span data-stu-id="ce576-140">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="ce576-141">Excluir</span><span class="sxs-lookup"><span data-stu-id="ce576-141">Delete</span></span>**  
<span data-ttu-id="ce576-142">Exclui o grupo licença da lista.</span><span class="sxs-lookup"><span data-stu-id="ce576-142">Deletes the license group from the list.</span></span>

<a href="" id="rename"></a>**<span data-ttu-id="ce576-143">Renomear</span><span class="sxs-lookup"><span data-stu-id="ce576-143">Rename</span></span>**  
<span data-ttu-id="ce576-144">Altera o nome do grupo de licenças aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ce576-144">Changes the name of the applications license group.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="ce576-145">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ce576-145">Properties</span></span>**  
<span data-ttu-id="ce576-146">Exibe a caixa de diálogo **Propriedades** dos grupos de licenças de aplicativos selecionados.</span><span class="sxs-lookup"><span data-stu-id="ce576-146">Displays the **Properties** dialog box for the selected application license groups.</span></span> <span data-ttu-id="ce576-147">Esta caixa de diálogo tem as seguintes guias:</span><span class="sxs-lookup"><span data-stu-id="ce576-147">This dialog box has the following tabs:</span></span>

-   <span data-ttu-id="ce576-148">Guia **geral** — mostra as informações gerais sobre o grupo de licenças.</span><span class="sxs-lookup"><span data-stu-id="ce576-148">**General** tab—Displays general information about the license group.</span></span> <span data-ttu-id="ce576-149">Nessa guia, você pode alterar o valor de tempo (em minutos) no campo de **aviso de expiração da licença** .</span><span class="sxs-lookup"><span data-stu-id="ce576-149">From this tab, you can change the time value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="ce576-150">Você pode inserir qualquer valor de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="ce576-150">You can enter any value from 0–100.</span></span>

-   <span data-ttu-id="ce576-151">Guia **aplicativos** — exibe a lista de aplicativos associados ao grupo de licenças.</span><span class="sxs-lookup"><span data-stu-id="ce576-151">**Applications** tab—Displays the list of applications associated with the license group.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="ce576-152">Ajuda</span><span class="sxs-lookup"><span data-stu-id="ce576-152">Help</span></span>**  
<span data-ttu-id="ce576-153">Exibe o sistema de ajuda do console de gerenciamento do servidor do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="ce576-153">Displays the Application Virtualization Server Management Console help system.</span></span>

<span data-ttu-id="ce576-154">Quando o painel de **resultados** exibe os grupos de licenças do aplicativo, clique com o botão direito do mouse em qualquer lugar no painel de **resultados** , exceto em um grupo de licenças, para exibir um menu pop-up que contém os elementos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ce576-154">When the **Results** pane displays application license groups, right-click anywhere in the **Results** pane, except on a license group, to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="ce576-155">Atualizar</span><span class="sxs-lookup"><span data-stu-id="ce576-155">Refresh</span></span>**  
<span data-ttu-id="ce576-156">Atualiza o modo de exibição do servidor.</span><span class="sxs-lookup"><span data-stu-id="ce576-156">Refreshes the view of the server.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="ce576-157">Exportar lista</span><span class="sxs-lookup"><span data-stu-id="ce576-157">Export List</span></span>**  
<span data-ttu-id="ce576-158">Cria um arquivo de texto delimitado por tabulação que contém o conteúdo do painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="ce576-158">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="ce576-159">Este item exibe uma caixa de diálogo de **salvamento de arquivo** padrão na qual você especifica o local para o arquivo de texto que está criando.</span><span class="sxs-lookup"><span data-stu-id="ce576-159">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="ce576-160">Exibir</span><span class="sxs-lookup"><span data-stu-id="ce576-160">View</span></span>**  
<span data-ttu-id="ce576-161">Altera a aparência e o conteúdo do painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="ce576-161">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="arrange-line-up-icons"></a>**<span data-ttu-id="ce576-162">Ícones organizar/alinhar</span><span class="sxs-lookup"><span data-stu-id="ce576-162">Arrange/Line Up Icons</span></span>**  
<span data-ttu-id="ce576-163">Altera o modo como os ícones são exibidos no painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="ce576-163">Changes how the icons are displayed in the **Results** pane.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="ce576-164">Ajuda</span><span class="sxs-lookup"><span data-stu-id="ce576-164">Help</span></span>**  
<span data-ttu-id="ce576-165">Exibe o sistema de ajuda do console de gerenciamento do servidor do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="ce576-165">Displays the help system for the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="ce576-166">Quando o painel de **resultados** exibir licenças, clique com o botão direito do mouse em qualquer licença do aplicativo para exibir um menu pop-up que contém os seguintes elementos.</span><span class="sxs-lookup"><span data-stu-id="ce576-166">When the **Results** pane displays licenses, right-click any application license to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="ce576-167">Excluir</span><span class="sxs-lookup"><span data-stu-id="ce576-167">Delete</span></span>**  
<span data-ttu-id="ce576-168">Exclui a licença da lista.</span><span class="sxs-lookup"><span data-stu-id="ce576-168">Deletes the license from the list.</span></span>

<a href="" id="rename"></a>**<span data-ttu-id="ce576-169">Renomear</span><span class="sxs-lookup"><span data-stu-id="ce576-169">Rename</span></span>**  
<span data-ttu-id="ce576-170">Altera o nome da licença.</span><span class="sxs-lookup"><span data-stu-id="ce576-170">Changes the name of the license.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="ce576-171">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ce576-171">Properties</span></span>**  
<span data-ttu-id="ce576-172">Exibe a caixa de diálogo **Propriedades** para a licença do aplicativo selecionada.</span><span class="sxs-lookup"><span data-stu-id="ce576-172">Displays the **Properties** dialog box for the selected application license.</span></span>

<span data-ttu-id="ce576-173">A guia **geral** da caixa de diálogo **Propriedades** exibe informações sobre a licença e permite alterar o status habilitado, a data de validade da licença e as informações da chave da licença.</span><span class="sxs-lookup"><span data-stu-id="ce576-173">The **General** tab of the **Properties** dialog box displays information about the license and lets you change the enabled status, license expiration date, and license key information.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="ce576-174">Ajuda</span><span class="sxs-lookup"><span data-stu-id="ce576-174">Help</span></span>**  
<span data-ttu-id="ce576-175">Exibe o sistema de ajuda do console de gerenciamento do servidor.</span><span class="sxs-lookup"><span data-stu-id="ce576-175">Displays the server management console help system.</span></span>

<span data-ttu-id="ce576-176">Quando o painel de **resultados** exibe licenças, clique com o botão direito do mouse em qualquer lugar no painel **resultados** , exceto em uma licença, para exibir um menu pop-up que contém os elementos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ce576-176">When the **Results** pane displays licenses, right-click anywhere in the **Results** pane, except on a license, to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="ce576-177">Exportar lista</span><span class="sxs-lookup"><span data-stu-id="ce576-177">Export List</span></span>**  
<span data-ttu-id="ce576-178">Cria um arquivo de texto delimitado por tabulação que contém o conteúdo do painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="ce576-178">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="ce576-179">Este item exibe uma caixa de diálogo de **salvamento de arquivo** padrão na qual você especifica o local para o arquivo de texto que está criando.</span><span class="sxs-lookup"><span data-stu-id="ce576-179">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="ce576-180">Exibir</span><span class="sxs-lookup"><span data-stu-id="ce576-180">View</span></span>**  
<span data-ttu-id="ce576-181">Altera a aparência e o conteúdo do painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="ce576-181">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="arrange-line-up-icons"></a>**<span data-ttu-id="ce576-182">Ícones organizar/alinhar</span><span class="sxs-lookup"><span data-stu-id="ce576-182">Arrange/Line Up Icons</span></span>**  
<span data-ttu-id="ce576-183">Altera o modo como os ícones são exibidos no painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="ce576-183">Changes how the icons are displayed in the **Results** pane.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="ce576-184">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ce576-184">Properties</span></span>**  
<span data-ttu-id="ce576-185">Exibe a caixa de diálogo **Propriedades** para a licença selecionada.</span><span class="sxs-lookup"><span data-stu-id="ce576-185">Displays the **Properties** dialog box for the selected license.</span></span>

<span data-ttu-id="ce576-186">A guia **geral** da caixa de diálogo **Propriedades** exibe informações sobre a licença e permite alterar o status habilitado, a data de validade da licença e as informações da chave da licença.</span><span class="sxs-lookup"><span data-stu-id="ce576-186">The **General** tab of the **Properties** dialog box displays information about the license and lets you change the enabled status, license expiration date, and license key information.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="ce576-187">Ajuda</span><span class="sxs-lookup"><span data-stu-id="ce576-187">Help</span></span>**  
<span data-ttu-id="ce576-188">Exibe o sistema de ajuda do console de gerenciamento do servidor do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="ce576-188">Displays the help system for the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="ce576-189">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ce576-189">Related topics</span></span>


[<span data-ttu-id="ce576-190">Sobre licenciamento de aplicativos</span><span class="sxs-lookup"><span data-stu-id="ce576-190">About Application Licensing</span></span>](about-application-licensing.md)

[<span data-ttu-id="ce576-191">Como gerenciar licenças de aplicativos no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="ce576-191">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="ce576-192">Server Management Console: nó Licenças de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="ce576-192">Server Management Console: Application Licenses Node</span></span>](server-management-console-application-licenses-node.md)

 

 





