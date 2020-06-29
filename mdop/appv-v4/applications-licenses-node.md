---
title: Nó Licenças de Aplicativos
description: Nó Licenças de Aplicativos
author: dansimp
ms.assetid: 2b8752ff-aa56-483e-b844-966941af2d94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 720de1860e72ae2c71298f93e9b346afd66da569
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797540"
---
# <span data-ttu-id="2f818-103">Nó Licenças de Aplicativos</span><span class="sxs-lookup"><span data-stu-id="2f818-103">Applications Licenses Node</span></span>


<span data-ttu-id="2f818-104">O nó de **licenças de aplicativos** é um nível abaixo do nó do sistema virtualização de aplicativos no painel **escopo** no console de gerenciamento do servidor do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="2f818-104">The **Applications Licenses** node is one level below the Application Virtualization System node in the **Scope** pane in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="2f818-105">Quando você seleciona esse nó, o painel de **resultados** exibe uma lista de licenças e grupos de licenças.</span><span class="sxs-lookup"><span data-stu-id="2f818-105">When you select this node, the **Results** pane displays a list of licenses and license groups.</span></span> <span data-ttu-id="2f818-106">Os seguintes tipos de licença estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="2f818-106">The following license types are available:</span></span>

-   <span data-ttu-id="2f818-107">**Licença ilimitada**— fornece acesso a qualquer número de usuários simultâneos.</span><span class="sxs-lookup"><span data-stu-id="2f818-107">**Unlimited License**—Provides access for any number of simultaneous users.</span></span> <span data-ttu-id="2f818-108">Esse método de licenciamento é apropriado quando você deseja associar uma licença de toda a empresa a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2f818-108">This method of licensing is appropriate when you want to associate an enterprise-wide license with an application.</span></span>

-   <span data-ttu-id="2f818-109">**Licença simultânea**— permite que você defina o número máximo de usuários simultâneos que têm permissão para usar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2f818-109">**Concurrent License**—Enables you to define the maximum number of concurrent users who are allowed to use the application.</span></span>

-   <span data-ttu-id="2f818-110">**Licença nomeada**— permite atribuir uma licença a um usuário individual.</span><span class="sxs-lookup"><span data-stu-id="2f818-110">**Named License**—Enables you to assign a license to an individual user.</span></span> <span data-ttu-id="2f818-111">Uma licença nomeada pode ser usada para garantir que um usuário em particular sempre será capaz de executar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2f818-111">A named license can be used to ensure that a particular user will always be able to run the application.</span></span>

<span data-ttu-id="2f818-112">**Observação**  Você pode combinar licenças simultâneas e nomeadas para o mesmo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2f818-112">**Note** You can combine concurrent and named licenses for the same application.</span></span>

 

<span data-ttu-id="2f818-113">Clique com o botão direito do mouse no nó **licenças de aplicativos** para exibir um menu pop-up que contém os elementos a seguir.</span><span class="sxs-lookup"><span data-stu-id="2f818-113">Right-click the **Applications Licenses** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-unlimited-license"></a>**<span data-ttu-id="2f818-114">Nova licença ilimitada</span><span class="sxs-lookup"><span data-stu-id="2f818-114">New Unlimited License</span></span>**  
<span data-ttu-id="2f818-115">Exibe o assistente de nova licença ilimitada.</span><span class="sxs-lookup"><span data-stu-id="2f818-115">Displays the New Unlimited License Wizard.</span></span> <span data-ttu-id="2f818-116">Este assistente consiste nas seguintes páginas:</span><span class="sxs-lookup"><span data-stu-id="2f818-116">This wizard consists of the following pages:</span></span>

1.  <span data-ttu-id="2f818-117">Digite o nome do grupo de licenças no campo **nome do grupo de licenças do aplicativo** e insira um valor (em minutos) no campo de **aviso de expiração da licença** .</span><span class="sxs-lookup"><span data-stu-id="2f818-117">Enter the name of the license group in the **Applications License Group Name** field, and enter a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="2f818-118">(Você pode inserir qualquer valor de 0 a 100.) Você também pode usar as setas para cima e para baixo para selecionar o número de minutos.</span><span class="sxs-lookup"><span data-stu-id="2f818-118">(You can enter any value from 0 through 100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="2f818-119">Insira um breve texto descritivo no campo **Descrição da licença** e marque a caixa de seleção **habilitada** para habilitar a licença.</span><span class="sxs-lookup"><span data-stu-id="2f818-119">Enter brief descriptive text in the **License Description** field, and select the **Enabled** check box to enable the license.</span></span>

    <span data-ttu-id="2f818-120">Opcionalmente, você pode usar o campo **data de expiração** para especificar uma data de expiração para a licença.</span><span class="sxs-lookup"><span data-stu-id="2f818-120">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="2f818-121">Você pode marcar a caixa de seleção para usar a data de expiração exibida ou pode usar o utilitário de calendário para navegar até a data de expiração desejada.</span><span class="sxs-lookup"><span data-stu-id="2f818-121">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="2f818-122">Clique em **concluir** para adicionar a nova licença.</span><span class="sxs-lookup"><span data-stu-id="2f818-122">Click **Finish** to add the new license.</span></span>

<a href="" id="new-concurrent-license"></a>**<span data-ttu-id="2f818-123">Nova licença simultânea</span><span class="sxs-lookup"><span data-stu-id="2f818-123">New Concurrent License</span></span>**  
<span data-ttu-id="2f818-124">Exibe o assistente de nova licença simultânea.</span><span class="sxs-lookup"><span data-stu-id="2f818-124">Displays the New Concurrent License Wizard.</span></span> <span data-ttu-id="2f818-125">Este assistente consiste nas três páginas a seguir e é quase idêntico ao assistente de nova licença ilimitada:</span><span class="sxs-lookup"><span data-stu-id="2f818-125">This wizard consists of the following three pages and is almost identical to the New Unlimited License Wizard:</span></span>

1.  <span data-ttu-id="2f818-126">Digite o nome do grupo de licenças no campo **nome do grupo de licenças do aplicativo** e insira um valor (em minutos) no campo de **aviso de expiração da licença** .</span><span class="sxs-lookup"><span data-stu-id="2f818-126">Enter the name of the license group in the **Applications License Group Name** field, and enter a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="2f818-127">(Você pode inserir qualquer valor de 0 a 100.) Você também pode usar as setas para cima e para baixo para selecionar o número de minutos.</span><span class="sxs-lookup"><span data-stu-id="2f818-127">(You can enter any value from 0 through 100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="2f818-128">Insira um breve texto descritivo no campo **Descrição da licença** e insira um valor no campo **quantidade da licença simultânea** .</span><span class="sxs-lookup"><span data-stu-id="2f818-128">Enter brief descriptive text in the **License Description** field, and enter a value in the **Concurrent License Quantity** field.</span></span>

    <span data-ttu-id="2f818-129">Você também pode usar as setas para cima e para baixo para especificar o número de licenças simultâneas.</span><span class="sxs-lookup"><span data-stu-id="2f818-129">You can also use the up and down arrows to specify the number of concurrent licenses.</span></span> <span data-ttu-id="2f818-130">Marque a caixa de seleção **habilitado** para habilitar a licença.</span><span class="sxs-lookup"><span data-stu-id="2f818-130">Select the **Enabled** check box to enable the license.</span></span>

    <span data-ttu-id="2f818-131">Opcionalmente, você pode usar o campo **data de expiração** para especificar uma data de expiração para a licença.</span><span class="sxs-lookup"><span data-stu-id="2f818-131">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="2f818-132">Você pode marcar a caixa de seleção para usar a data de expiração exibida ou pode usar o utilitário de calendário para navegar até a data de expiração desejada.</span><span class="sxs-lookup"><span data-stu-id="2f818-132">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="2f818-133">Clique em **concluir** para adicionar as novas licenças.</span><span class="sxs-lookup"><span data-stu-id="2f818-133">Click **Finish** to add the new licenses.</span></span>

<a href="" id="new-named-license"></a>**<span data-ttu-id="2f818-134">Nova licença nomeada</span><span class="sxs-lookup"><span data-stu-id="2f818-134">New Named License</span></span>**  
<span data-ttu-id="2f818-135">Exibe o novo assistente de licença nomeada.</span><span class="sxs-lookup"><span data-stu-id="2f818-135">Displays the New Named License Wizard.</span></span> <span data-ttu-id="2f818-136">Este assistente consiste nas quatro páginas a seguir:</span><span class="sxs-lookup"><span data-stu-id="2f818-136">This wizard consists of the following four pages:</span></span>

1.  <span data-ttu-id="2f818-137">Digite o nome do grupo de licenças no campo **nome do grupo de licenças do aplicativo** e insira um valor (em minutos) no campo de **aviso de expiração da licença** .</span><span class="sxs-lookup"><span data-stu-id="2f818-137">Enter the name of the license group in the **Applications License Group Name** field, and enter a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="2f818-138">(Você pode inserir qualquer valor de 0 a 100).</span><span class="sxs-lookup"><span data-stu-id="2f818-138">(You can enter any value from 0 through 100).</span></span> <span data-ttu-id="2f818-139">Você também pode usar as setas para cima e para baixo para selecionar o número de minutos.</span><span class="sxs-lookup"><span data-stu-id="2f818-139">You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="2f818-140">Insira um breve texto descritivo no campo **Descrição da licença** e marque a caixa de seleção **habilitada** para habilitar a licença.</span><span class="sxs-lookup"><span data-stu-id="2f818-140">Enter brief descriptive text in the **License Description** field, and select the **Enabled** check box to enable the license.</span></span>

    <span data-ttu-id="2f818-141">Opcionalmente, você pode usar o campo **data de expiração** para especificar uma data de expiração para a licença.</span><span class="sxs-lookup"><span data-stu-id="2f818-141">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="2f818-142">Você pode marcar a caixa de seleção para usar a data de expiração exibida ou pode usar o utilitário de calendário para navegar até a data de expiração desejada.</span><span class="sxs-lookup"><span data-stu-id="2f818-142">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="2f818-143">Clique em **Adicionar**, **Editar**ou **remover** usuários nomeados.</span><span class="sxs-lookup"><span data-stu-id="2f818-143">Click **Add**, **Edit**, or **Remove** named users.</span></span>

4.  <span data-ttu-id="2f818-144">Clique em **concluir** para adicionar a nova licença.</span><span class="sxs-lookup"><span data-stu-id="2f818-144">Click **Finish** to add the new license.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="2f818-145">Exibir</span><span class="sxs-lookup"><span data-stu-id="2f818-145">View</span></span>**  
<span data-ttu-id="2f818-146">Altera a aparência e o conteúdo do painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="2f818-146">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="2f818-147">Nova janela a partir daqui</span><span class="sxs-lookup"><span data-stu-id="2f818-147">New Window from Here</span></span>**  
<span data-ttu-id="2f818-148">Abre um novo console de gerenciamento com o nó selecionado como nó raiz.</span><span class="sxs-lookup"><span data-stu-id="2f818-148">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="2f818-149">Atualizar</span><span class="sxs-lookup"><span data-stu-id="2f818-149">Refresh</span></span>**  
<span data-ttu-id="2f818-150">Atualiza o modo de exibição do servidor.</span><span class="sxs-lookup"><span data-stu-id="2f818-150">Refreshes the view of the server.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="2f818-151">Exportar lista</span><span class="sxs-lookup"><span data-stu-id="2f818-151">Export List</span></span>**  
<span data-ttu-id="2f818-152">Cria um arquivo de texto delimitado por tabulação que contém o conteúdo do painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="2f818-152">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="2f818-153">Este item exibe uma caixa de diálogo de **salvamento de arquivo** padrão na qual você especifica o local para o arquivo de texto que está criando.</span><span class="sxs-lookup"><span data-stu-id="2f818-153">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="2f818-154">Ajuda</span><span class="sxs-lookup"><span data-stu-id="2f818-154">Help</span></span>**  
<span data-ttu-id="2f818-155">Exibe o sistema de ajuda do console de gerenciamento do servidor do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="2f818-155">Displays the help system for the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="2f818-156">Se você clicar em um grupo de licenças ou licença que aparece no nó **licenças do aplicativo** no painel **escopo** , os seguintes elementos estarão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2f818-156">If you click a license group or license that appears under the **Application Licenses** node in the **Scope** pane, the following elements are available.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="2f818-157">Exibir</span><span class="sxs-lookup"><span data-stu-id="2f818-157">View</span></span>**  
<span data-ttu-id="2f818-158">Altera a aparência e o conteúdo do painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="2f818-158">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="2f818-159">Nova janela a partir daqui</span><span class="sxs-lookup"><span data-stu-id="2f818-159">New Window from Here</span></span>**  
<span data-ttu-id="2f818-160">Abre um novo console de gerenciamento com o nó selecionado como nó raiz.</span><span class="sxs-lookup"><span data-stu-id="2f818-160">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="2f818-161">Excluir</span><span class="sxs-lookup"><span data-stu-id="2f818-161">Delete</span></span>**  
<span data-ttu-id="2f818-162">Exclui um pacote do painel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="2f818-162">Deletes a package from the **Results** pane.</span></span>

<a href="" id="rename"></a>**<span data-ttu-id="2f818-163">Renomear</span><span class="sxs-lookup"><span data-stu-id="2f818-163">Rename</span></span>**  
<span data-ttu-id="2f818-164">Altera o nome de um pacote no painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="2f818-164">Changes the name of a package in the **Results** pane.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="2f818-165">Exportar lista</span><span class="sxs-lookup"><span data-stu-id="2f818-165">Export List</span></span>**  
<span data-ttu-id="2f818-166">Cria um arquivo de texto delimitado por tabulação que contém o conteúdo do painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="2f818-166">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="2f818-167">Este item exibe uma caixa de diálogo de **salvamento de arquivo** padrão na qual você especifica o local para o arquivo de texto que está criando.</span><span class="sxs-lookup"><span data-stu-id="2f818-167">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="2f818-168">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2f818-168">Properties</span></span>**  
<span data-ttu-id="2f818-169">Exibe a caixa de diálogo **Propriedades** do grupo de licenças selecionado.</span><span class="sxs-lookup"><span data-stu-id="2f818-169">Displays the **Properties** dialog box for the selected license group.</span></span> <span data-ttu-id="2f818-170">A guia **geral** da caixa de diálogo **Propriedades** exibe informações sobre o grupo de licenças e permite que você altere o valor de tempo no campo de **aviso de expiração da licença** .</span><span class="sxs-lookup"><span data-stu-id="2f818-170">The **General** tab of the **Properties** dialog box displays information about the license group and lets you change the time value in the **License Expiration Warning** field.</span></span> <span data-ttu-id="2f818-171">A guia **aplicativos** exibe a lista de aplicativos associados ao grupo de licenças.</span><span class="sxs-lookup"><span data-stu-id="2f818-171">The **Applications** tab displays the list of applications associated with the license group.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="2f818-172">Ajuda</span><span class="sxs-lookup"><span data-stu-id="2f818-172">Help</span></span>**  
<span data-ttu-id="2f818-173">Exibe o sistema de ajuda do console de gerenciamento do servidor do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="2f818-173">Displays the help system for the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="2f818-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2f818-174">Related topics</span></span>


[<span data-ttu-id="2f818-175">Sobre licenciamento de aplicativos</span><span class="sxs-lookup"><span data-stu-id="2f818-175">About Application Licensing</span></span>](about-application-licensing.md)

[<span data-ttu-id="2f818-176">Como gerenciar licenças de aplicativos no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="2f818-176">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="2f818-177">Server Management Console: nó Licenças de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="2f818-177">Server Management Console: Application Licenses Node</span></span>](server-management-console-application-licenses-node.md)

 

 





