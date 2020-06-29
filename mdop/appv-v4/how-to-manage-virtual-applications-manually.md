---
title: Como gerenciar aplicativos virtuais manualmente
description: Como gerenciar aplicativos virtuais manualmente
author: dansimp
ms.assetid: 583c5255-d3f4-4197-85cd-2a59868d85de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e8dd5bb9d62950ac1a03ad0ec14802d9e0ff56e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797060"
---
# <span data-ttu-id="f1735-103">Como gerenciar aplicativos virtuais manualmente</span><span class="sxs-lookup"><span data-stu-id="f1735-103">How to Manage Virtual Applications Manually</span></span>


<span data-ttu-id="f1735-104">Você pode usar o console de gerenciamento de cliente do Application Virtualization (App-V) para gerenciar aplicativos virtuais no cliente da área de trabalho do App-V ou do App-V cliente para serviços de área de trabalho remota (anteriormente serviços de terminal).</span><span class="sxs-lookup"><span data-stu-id="f1735-104">You can use the Application Virtualization (App-V) Client Management Console to manage virtual applications in the App-V Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="f1735-105">Os administradores do App-V podem usar executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="f1735-105">App-V administrators can use perform the following tasks:</span></span>

## <span data-ttu-id="f1735-106">Como carregar ou descarregar um aplicativo App-V</span><span class="sxs-lookup"><span data-stu-id="f1735-106">How to Load or Unload an App-V Application</span></span>


<span data-ttu-id="f1735-107">Você pode usar os procedimentos a seguir para carregar ou descarregar um aplicativo a partir do cache, diretamente do painel **resultados** do nó do **aplicativo** no console de gerenciamento de cliente do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f1735-107">You can use the following procedures to load or unload an application from the cache, directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="f1735-108">Quando você seleciona esse nó, o painel de **resultados** exibe uma lista de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f1735-108">When you select this node, the **Results** pane displays a list of applications.</span></span>

<span data-ttu-id="f1735-109">**Observação**  Quando você carrega ou descarrega um pacote, todos os aplicativos no pacote são carregados em ou removidos do cache.</span><span class="sxs-lookup"><span data-stu-id="f1735-109">**Note** When you load or unload a package, all the applications in the package are loaded into or removed from cache.</span></span> <span data-ttu-id="f1735-110">Ao carregar um pacote, se você não tiver espaço suficiente em cache para carregar os aplicativos, aumente o tamanho do cache.</span><span class="sxs-lookup"><span data-stu-id="f1735-110">When loading a package, if you do not have adequate space in cache to load the applications, increase your cache size.</span></span> <span data-ttu-id="f1735-111">Para obter mais informações sobre o tamanho do cache, consulte [como alterar o tamanho do cache e a designação da letra da unidade](how-to-change-the-cache-size-and-the-drive-letter-designation.md).</span><span class="sxs-lookup"><span data-stu-id="f1735-111">For more information about cache size, see [How to Change the Cache Size and the Drive Letter Designation](how-to-change-the-cache-size-and-the-drive-letter-designation.md).</span></span>

 

**<span data-ttu-id="f1735-112">Para carregar um aplicativo App-V</span><span class="sxs-lookup"><span data-stu-id="f1735-112">To load an App-V application</span></span>**

1.  <span data-ttu-id="f1735-113">Mova o cursor para o painel de **resultados** , clique com o botão direito do mouse no aplicativo desejado e selecione **carregar** no menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="f1735-113">Move the cursor to the **Results** pane, right-click the desired application, and select **Load** from the pop-up menu.</span></span>

2.  <span data-ttu-id="f1735-114">O aplicativo é carregado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f1735-114">The application is automatically loaded.</span></span> <span data-ttu-id="f1735-115">O progresso é acompanhado na coluna rotulada **status do pacote**.</span><span class="sxs-lookup"><span data-stu-id="f1735-115">The progress is tracked in the column labeled **Package Status**.</span></span> <span data-ttu-id="f1735-116">Você deve atualizar o modo de exibição para ver se a carga está concluída ou para ver o progresso.</span><span class="sxs-lookup"><span data-stu-id="f1735-116">You must refresh the view to see that the load is complete or to see the progress.</span></span>

**<span data-ttu-id="f1735-117">Para descarregar um aplicativo App-V</span><span class="sxs-lookup"><span data-stu-id="f1735-117">To unload an App-V application</span></span>**

1.  <span data-ttu-id="f1735-118">Mova o cursor para o painel de **resultados** , clique com o botão direito do mouse no aplicativo desejado e selecione **descarregar** no menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="f1735-118">Move the cursor to the **Results** pane, right-click the desired application, and select **Unload** from the pop-up menu.</span></span>

2.  <span data-ttu-id="f1735-119">O aplicativo é descarregado automaticamente, e a coluna **status do pacote** é atualizada para refletir a alteração.</span><span class="sxs-lookup"><span data-stu-id="f1735-119">The application is automatically unloaded, and the **Package Status** column is updated to reflect the change.</span></span>

## <span data-ttu-id="f1735-120">Como limpar um aplicativo App-V</span><span class="sxs-lookup"><span data-stu-id="f1735-120">How to clear an App-V application</span></span>


<span data-ttu-id="f1735-121">Você pode limpar um aplicativo do console diretamente do painel **resultados** do nó do **aplicativo** no console de gerenciamento de cliente do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f1735-121">You can clear an application from the console directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="f1735-122">Quando você limpa um aplicativo, o sistema remove as configurações, atalhos e associações de tipo de arquivo que correspondem ao aplicativo e também remove o aplicativo da lista de aplicativos do usuário.</span><span class="sxs-lookup"><span data-stu-id="f1735-122">When you clear an application, the system removes the settings, shortcuts, and file type associations that correspond to the application and also removes the application from the user’s list of applications.</span></span>

<span data-ttu-id="f1735-123">**Observação**  Ao limpar um aplicativo do console, você não pode mais usar esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1735-123">**Note** When you clear an application from the console, you can no longer use that application.</span></span> <span data-ttu-id="f1735-124">No entanto, o aplicativo permanece em cache e ainda está disponível para outros usuários no mesmo sistema.</span><span class="sxs-lookup"><span data-stu-id="f1735-124">However, the application remains in cache and is still available to other users on the same system.</span></span> <span data-ttu-id="f1735-125">Após uma atualização de publicação, os aplicativos limpos ficarão novamente disponíveis para você.</span><span class="sxs-lookup"><span data-stu-id="f1735-125">After a publishing refresh, the cleared applications will again become available to you.</span></span> <span data-ttu-id="f1735-126">Se houver vários aplicativos em um pacote, as configurações do usuário não serão removidas até que todos os aplicativos sejam limpos.</span><span class="sxs-lookup"><span data-stu-id="f1735-126">If there are multiple applications in a package, the user's settings are not removed until all of the applications are cleared.</span></span>

 

**<span data-ttu-id="f1735-127">Para limpar um aplicativo do console</span><span class="sxs-lookup"><span data-stu-id="f1735-127">To clear an application from the console</span></span>**

1.  <span data-ttu-id="f1735-128">Mova o cursor para o painel de **resultados** , clique com o botão direito do mouse no aplicativo desejado e selecione **limpar** no menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="f1735-128">Move the cursor to the **Results** pane, right-click the desired application, and select **Clear** from the pop-up menu.</span></span>

2.  <span data-ttu-id="f1735-129">Na solicitação de confirmação, clique em **Sim** para remover o aplicativo ou clique em **não** para cancelar a operação.</span><span class="sxs-lookup"><span data-stu-id="f1735-129">At the confirmation prompt, click **Yes** to remove the application or click **No** to cancel the operation.</span></span>

## <span data-ttu-id="f1735-130">Como reparar um aplicativo App-V</span><span class="sxs-lookup"><span data-stu-id="f1735-130">How to Repair an App-V application</span></span>


<span data-ttu-id="f1735-131">Para reparar um aplicativo selecionado, você pode executar o seguinte procedimento diretamente do painel **resultados** do nó do **aplicativo** no console de gerenciamento de cliente do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f1735-131">To repair a selected application, you can perform the following procedure directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="f1735-132">Ao reparar um aplicativo, você remove qualquer configuração de usuário personalizada e restaura as configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="f1735-132">When you repair an application, you remove any custom user settings and restore the default settings.</span></span> <span data-ttu-id="f1735-133">Essa ação não altera ou exclui atalhos ou associações de tipo de arquivo, e não remove o aplicativo do cache.</span><span class="sxs-lookup"><span data-stu-id="f1735-133">This action does not change or delete shortcuts or file type associations, and it does not remove the application from cache.</span></span>

**<span data-ttu-id="f1735-134">Para reparar um aplicativo App-V</span><span class="sxs-lookup"><span data-stu-id="f1735-134">To repair an App-V application</span></span>**

1.  <span data-ttu-id="f1735-135">Mover o cursor para o painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="f1735-135">Move the cursor to the **Results** pane.</span></span>

2.  <span data-ttu-id="f1735-136">Clique com o botão direito do mouse no aplicativo desejado e selecione **reparar** no menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="f1735-136">Right-click the desired application, and select **Repair** from the pop-up menu.</span></span>

3.  <span data-ttu-id="f1735-137">Na solicitação de confirmação, clique em **Sim** para reparar o aplicativo ou em **não** para cancelar.</span><span class="sxs-lookup"><span data-stu-id="f1735-137">At the confirmation prompt, click **Yes** to repair the application or **No** to cancel.</span></span>

## <span data-ttu-id="f1735-138">Como importar um aplicativo App-V</span><span class="sxs-lookup"><span data-stu-id="f1735-138">How to import an App-V application</span></span>


<span data-ttu-id="f1735-139">Você pode usar o procedimento a seguir para importar um aplicativo para o cache diretamente do painel **resultados** do nó do **aplicativo** no console de gerenciamento de cliente do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f1735-139">You can use the following procedure to import an application into the cache directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="f1735-140">Para importar um aplicativo App-V</span><span class="sxs-lookup"><span data-stu-id="f1735-140">To import an App-V application</span></span>**

1.  <span data-ttu-id="f1735-141">Mova o cursor para o painel de **resultados** , clique com o botão direito do mouse no aplicativo desejado e selecione **importar** no menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="f1735-141">Move the cursor to the **Results** pane, right-click the desired application, and select **Import** from the pop-up menu.</span></span>

2.  <span data-ttu-id="f1735-142">Na janela **procurar** , navegue até o local do arquivo de pacote do aplicativo desejado e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1735-142">From the **Browse** window, navigate to the location of the package file for the desired application, and then click **OK**.</span></span>

    <span data-ttu-id="f1735-143">**Observação**  Se você já configurou um caminho de pesquisa de importação ou se o arquivo SFT está no mesmo caminho da última importação bem-sucedida, a etapa 2 não é necessária.</span><span class="sxs-lookup"><span data-stu-id="f1735-143">**Note** If you have already configured an import search path or if the SFT file is in the same path as the last successful import, step 2 is not required.</span></span>

     

## <span data-ttu-id="f1735-144">Como bloquear ou desbloquear um aplicativo App-V</span><span class="sxs-lookup"><span data-stu-id="f1735-144">How to lock or unlock an App-V application</span></span>


<span data-ttu-id="f1735-145">Você pode usar os procedimentos a seguir para bloquear ou desbloquear qualquer aplicativo no cache do cliente da área de trabalho do Application Virtualization ou no cache do cliente dos serviços de área de trabalho remota (anteriormente Terminal Services).</span><span class="sxs-lookup"><span data-stu-id="f1735-145">You can use the following procedures to lock or unlock any application in the Application Virtualization Desktop Client cache or the Client for Remote Desktop Services (formerly Terminal Services) cache.</span></span> <span data-ttu-id="f1735-146">Um aplicativo bloqueado não pode ser removido do cache para criar espaço para novos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f1735-146">A locked application cannot be removed from the cache to make room for new applications.</span></span> <span data-ttu-id="f1735-147">Para remover um aplicativo bloqueado do cache de cliente de desktop virtualização de aplicativos ou do cliente para o cache de serviços de área de trabalho remota, você deve primeiro desbloqueá-lo.</span><span class="sxs-lookup"><span data-stu-id="f1735-147">To remove a locked application from the Application Virtualization Desktop Client cache or the Client for Remote Desktop Services cache, you must first unlock it.</span></span>

**<span data-ttu-id="f1735-148">Para bloquear um aplicativo</span><span class="sxs-lookup"><span data-stu-id="f1735-148">To lock an application</span></span>**

1.  <span data-ttu-id="f1735-149">Mover o cursor para o painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="f1735-149">Move the cursor to the **Results** pane.</span></span>

2.  <span data-ttu-id="f1735-150">Clique com o botão direito do mouse no aplicativo desejado e selecione **Bloquear** no menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="f1735-150">Right-click the desired application, and select **Lock** from the pop-up menu.</span></span> <span data-ttu-id="f1735-151">O aplicativo selecionado está bloqueado no cache.</span><span class="sxs-lookup"><span data-stu-id="f1735-151">The selected application is locked in the cache.</span></span>

**<span data-ttu-id="f1735-152">Para desbloquear um aplicativo</span><span class="sxs-lookup"><span data-stu-id="f1735-152">To unlock an application</span></span>**

1.  <span data-ttu-id="f1735-153">Mover o cursor para o painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="f1735-153">Move the cursor to the **Results** pane.</span></span>

2.  <span data-ttu-id="f1735-154">Clique com o botão direito do mouse no aplicativo desejado e selecione **desbloquear** no menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="f1735-154">Right-click the desired application, and select **Unlock** from the pop-up menu.</span></span> <span data-ttu-id="f1735-155">O aplicativo selecionado está desbloqueado no cache e pode ser removido.</span><span class="sxs-lookup"><span data-stu-id="f1735-155">The selected application is unlocked in the cache and can be removed.</span></span>

## <span data-ttu-id="f1735-156">Como excluir um aplicativo App-V</span><span class="sxs-lookup"><span data-stu-id="f1735-156">How to delete an App-V application</span></span>


<span data-ttu-id="f1735-157">Quando você seleciona o nó do **aplicativo** no console de gerenciamento do cliente do Application Virtualization, o painel **resultados** exibe uma lista de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f1735-157">When you select the **Application** node in the Application Virtualization Client Management Console, the **Results** pane displays a list of applications.</span></span> <span data-ttu-id="f1735-158">Você pode usar o procedimento a seguir para excluir um aplicativo do painel **resultados** , que também remove o aplicativo do cache.</span><span class="sxs-lookup"><span data-stu-id="f1735-158">You can use the following procedure to delete an application from the **Results** pane, which also removes the application from the cache.</span></span>

<span data-ttu-id="f1735-159">**Observação**  Quando você exclui um aplicativo, o aplicativo selecionado não estará mais disponível para os usuários do cliente.</span><span class="sxs-lookup"><span data-stu-id="f1735-159">**Note** When you delete an application, the selected application will no longer be available to any users on that client.</span></span> <span data-ttu-id="f1735-160">Os atalhos e associações de tipo de arquivo estão ocultos e o aplicativo é excluído do cache.</span><span class="sxs-lookup"><span data-stu-id="f1735-160">Shortcuts and file type associations are hidden, and the application is deleted from cache.</span></span> <span data-ttu-id="f1735-161">No entanto, se outro aplicativo se refere a dados nos dados de cache do sistema de arquivos do aplicativo selecionado, esses itens não serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="f1735-161">However, if another application refers to data in the file system cache data for the selected application, these items will not be deleted.</span></span>

<span data-ttu-id="f1735-162">Após uma atualização de publicação, os aplicativos excluídos ficarão novamente disponíveis para você.</span><span class="sxs-lookup"><span data-stu-id="f1735-162">After a publishing refresh, the deleted applications will again become available to you.</span></span>

 

**<span data-ttu-id="f1735-163">Para excluir um aplicativo</span><span class="sxs-lookup"><span data-stu-id="f1735-163">To delete an application</span></span>**

1.  <span data-ttu-id="f1735-164">Mova o cursor para o painel de **resultados** , clique com o botão direito do mouse no aplicativo desejado e selecione **excluir** no menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="f1735-164">Move the cursor to the **Results** pane, right-click the desired application, and select **Delete** from the pop-up menu.</span></span>

2.  <span data-ttu-id="f1735-165">Na solicitação de confirmação, clique em **Sim** para remover o aplicativo ou clique em **não** para cancelar a operação.</span><span class="sxs-lookup"><span data-stu-id="f1735-165">At the confirmation prompt, click **Yes** to remove the application or click **No** to cancel the operation.</span></span>

## <span data-ttu-id="f1735-166">Como alterar um ícone do aplicativo App-V</span><span class="sxs-lookup"><span data-stu-id="f1735-166">How to change an App-V application icon</span></span>


<span data-ttu-id="f1735-167">Você pode usar o procedimento a seguir para alterar um ícone associado ao aplicativo selecionado diretamente do painel **resultados** do nó do **aplicativo** no console de gerenciamento do aplicativo virtualização de cliente.</span><span class="sxs-lookup"><span data-stu-id="f1735-167">You can use the following procedure to change an icon associated with the selected application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="f1735-168">Para alterar um ícone de aplicativo</span><span class="sxs-lookup"><span data-stu-id="f1735-168">To change an application icon</span></span>**

1.  <span data-ttu-id="f1735-169">Mova o cursor para o painel **resultados** e clique com o botão direito do mouse no aplicativo desejado.</span><span class="sxs-lookup"><span data-stu-id="f1735-169">Move the cursor to the **Results** pane, and right-click the desired application.</span></span>

2.  <span data-ttu-id="f1735-170">Selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="f1735-170">Select **Properties**.</span></span>

3.  <span data-ttu-id="f1735-171">Na guia **geral** , clique em **Alterar ícone**.</span><span class="sxs-lookup"><span data-stu-id="f1735-171">On the **General** tab, click **Change Icon**.</span></span>

4.  <span data-ttu-id="f1735-172">Selecione o ícone desejado ou navegue até outro local para selecionar o ícone.</span><span class="sxs-lookup"><span data-stu-id="f1735-172">Select the desired icon, or browse to another location to select the icon.</span></span> <span data-ttu-id="f1735-173">Depois de selecionar o ícone, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1735-173">After you've selected the icon, click **OK**.</span></span> <span data-ttu-id="f1735-174">O novo ícone aparecerá no painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="f1735-174">The new icon appears in the **Results** pane.</span></span>

## <span data-ttu-id="f1735-175">Como adicionar um aplicativo App-V</span><span class="sxs-lookup"><span data-stu-id="f1735-175">How to add an App-V application</span></span>


<span data-ttu-id="f1735-176">Você pode usar o procedimento a seguir para adicionar um aplicativo diretamente do painel **resultados** do nó do **aplicativo** no console de gerenciamento do cliente do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f1735-176">You can use the following procedure to add an application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="f1735-177">Para adicionar um aplicativo</span><span class="sxs-lookup"><span data-stu-id="f1735-177">To add an application</span></span>**

1.  <span data-ttu-id="f1735-178">No painel de **resultados** , clique com o botão direito do mouse e selecione **novo aplicativo** no menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="f1735-178">In the **Results** pane, right-click and select **New Application** from the pop-up menu.</span></span>

2.  <span data-ttu-id="f1735-179">Na página do assistente, você pode executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="f1735-179">On the wizard page, you can perform the following tasks:</span></span>

    1.  <span data-ttu-id="f1735-180">**Alterar ícone**— exibe um navegador padrão de ícones do Windows.</span><span class="sxs-lookup"><span data-stu-id="f1735-180">**Change Icon**—Displays a standard Windows icon browser.</span></span> <span data-ttu-id="f1735-181">Procure e selecione o ícone desejado.</span><span class="sxs-lookup"><span data-stu-id="f1735-181">Browse to and select the desired icon.</span></span>

    2.  <span data-ttu-id="f1735-182">**Caminho ou URL do arquivo OSD**— Insira um caminho absoluto local, um caminho UNC completo (arquivo compartilhado ou diretório em uma rede) ou uma URL http.</span><span class="sxs-lookup"><span data-stu-id="f1735-182">**OSD File Path or URL**—Enter a local absolute path, a full UNC path (shared file or directory on a network), or an HTTP URL.</span></span>

    3.  <span data-ttu-id="f1735-183">**(Botão procurar OSD)**— exibe a caixa de diálogo padrão **Abrir arquivo** do Windows.</span><span class="sxs-lookup"><span data-stu-id="f1735-183">**(OSD browse button)**—Displays the standard Windows **Open File** dialog box.</span></span> <span data-ttu-id="f1735-184">Navegue até localizar o arquivo desejado.</span><span class="sxs-lookup"><span data-stu-id="f1735-184">Browse to find the desired file.</span></span>

3.  <span data-ttu-id="f1735-185">Clique em **concluir** para adicionar o aplicativo ao painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="f1735-185">Click **Finish** to add the application to the **Results** pane.</span></span>

## <span data-ttu-id="f1735-186">Como publicar um atalho do aplicativo App-V</span><span class="sxs-lookup"><span data-stu-id="f1735-186">How to publish an App-V application shortcut</span></span>


<span data-ttu-id="f1735-187">Você pode usar o procedimento a seguir para publicar atalhos para um aplicativo diretamente do painel **resultados** do nó do **aplicativo** no console de gerenciamento de cliente do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f1735-187">You can use the following procedure to publish shortcuts to an application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="f1735-188">Para publicar atalhos de aplicativos</span><span class="sxs-lookup"><span data-stu-id="f1735-188">To publish application shortcuts</span></span>**

1.  <span data-ttu-id="f1735-189">Mova o cursor para o painel de **resultados** , clique com o botão direito do mouse no aplicativo desejado e selecione **novo atalho** no menu pop-up para exibir o assistente de novo atalho.</span><span class="sxs-lookup"><span data-stu-id="f1735-189">Move the cursor to the **Results** pane, right-click the desired application, and select **New Shortcut** from the pop-up menu to display the New Shortcut Wizard.</span></span>

2.  <span data-ttu-id="f1735-190">Na primeira página do assistente de novo atalho, selecione um ícone e especifique um nome para o atalho.</span><span class="sxs-lookup"><span data-stu-id="f1735-190">On the first page of the New Shortcut Wizard, select an icon and specify a name for the shortcut.</span></span>

    1.  <span data-ttu-id="f1735-191">**Alterar ícone**— exibe um navegador padrão de ícones do Windows.</span><span class="sxs-lookup"><span data-stu-id="f1735-191">**Change Icon**—Displays a standard Windows icon browser.</span></span> <span data-ttu-id="f1735-192">Procure e selecione o ícone desejado.</span><span class="sxs-lookup"><span data-stu-id="f1735-192">Browse to and select the desired icon.</span></span>

    2.  <span data-ttu-id="f1735-193">**Título do atalho**— Insira o nome que você deseja dar ao atalho.</span><span class="sxs-lookup"><span data-stu-id="f1735-193">**Shortcut Title**—Enter the name you want to give the shortcut.</span></span> <span data-ttu-id="f1735-194">Este campo é definido como padrão para o nome e a versão existentes do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1735-194">This field defaults to the existing name and version of the application.</span></span>

3.  <span data-ttu-id="f1735-195">Na segunda página do assistente, determine o local do atalho publicado.</span><span class="sxs-lookup"><span data-stu-id="f1735-195">On the second page of the wizard, determine the location of the published shortcut.</span></span>

    1.  <span data-ttu-id="f1735-196">**A área de trabalho**— Marque esta caixa de seleção para publicar o atalho na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f1735-196">**The Desktop**—Select this check box to publish the shortcut to the desktop.</span></span>

    2.  <span data-ttu-id="f1735-197">**A barra de ferramentas início rápido**— Marque esta caixa de seleção para publicar o atalho na barra de ferramentas início rápido.</span><span class="sxs-lookup"><span data-stu-id="f1735-197">**The Quick Launch Toolbar**—Select this check box to publish the shortcut to the Quick Launch toolbar.</span></span>

    3.  <span data-ttu-id="f1735-198">**O menu Enviar para**-Marque esta caixa de seleção para publicar o atalho no menu **Enviar para** .</span><span class="sxs-lookup"><span data-stu-id="f1735-198">**The Send To Menu**—Select this check box to publish the shortcut to the **Send To** menu.</span></span>

    4.  <span data-ttu-id="f1735-199">**Programas no menu iniciar**– quando você marca a caixa de seleção **menu iniciar** , este campo torna-se ativo.</span><span class="sxs-lookup"><span data-stu-id="f1735-199">**Programs in the Start Menu**—When you select the **Start Menu** check box, this field becomes active.</span></span> <span data-ttu-id="f1735-200">Deixe este campo em branco para publicar o atalho diretamente na raiz da pasta programas, ou insira um nome de pasta ou hierarquia — por exemplo, "meu \ _Computer aplicativos do \\Office."</span><span class="sxs-lookup"><span data-stu-id="f1735-200">Leave this field blank to publish the shortcut directly to the root of the Programs folder, or enter a folder name or hierarchy—for example, "My\_Computer\\Office Applications."</span></span> <span data-ttu-id="f1735-201">Os atalhos criados dessa maneira estão disponíveis somente para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="f1735-201">Shortcuts created this way are available only for the current user.</span></span>

    5.  <span data-ttu-id="f1735-202">**Outro local** e botão **procurar** — quando você marca a caixa de seleção **outro local** , esse campo torna-se ativo.</span><span class="sxs-lookup"><span data-stu-id="f1735-202">**Another location** and **Browse** button—When you select the **Another location** check box, this field becomes active.</span></span> <span data-ttu-id="f1735-203">Insira qualquer local válido no computador ou qualquer caminho UNC disponível (arquivo compartilhado ou diretório em uma rede).</span><span class="sxs-lookup"><span data-stu-id="f1735-203">Enter any valid location on the computer or any available UNC path (shared file or directory on a network).</span></span> <span data-ttu-id="f1735-204">O botão **procurar** exibe uma caixa de diálogo padrão **Abrir arquivo** do Windows.</span><span class="sxs-lookup"><span data-stu-id="f1735-204">The **Browse** button displays a standard Windows **File Open** dialog box.</span></span>

4.  <span data-ttu-id="f1735-205">Na terceira página do assistente, insira os parâmetros de linha de comando desejados.</span><span class="sxs-lookup"><span data-stu-id="f1735-205">On the third page of the wizard, enter desired command-line parameters.</span></span>

5.  <span data-ttu-id="f1735-206">Clique em **concluir** para publicar os atalhos e sair para o painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="f1735-206">Click **Finish** to publish the shortcuts and exit to the **Results** pane.</span></span>

## <span data-ttu-id="f1735-207">Como adicionar uma associação de tipo de arquivo para um aplicativo App-V</span><span class="sxs-lookup"><span data-stu-id="f1735-207">How to add a file type association for an App-V application</span></span>


<span data-ttu-id="f1735-208">Você pode usar o procedimento a seguir para adicionar uma associação de tipo de arquivo, usando o nó **associações de tipo de arquivo** no console de gerenciamento de cliente do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f1735-208">You can use the following procedure to add a file type association, using the **File Type Associations** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="f1735-209">Para adicionar uma associação de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="f1735-209">To add a file type association</span></span>**

1.  <span data-ttu-id="f1735-210">Clique com o botão direito do mouse no nó **associações de tipo de arquivo** e selecione **nova associação** no menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="f1735-210">Right-click the **File Type Associations** node, and select **New Association** from the pop-up menu.</span></span>

2.  <span data-ttu-id="f1735-211">Complete a primeira etapa da caixa de diálogo completando as informações a seguir e, em seguida, clique em **Avançar**:</span><span class="sxs-lookup"><span data-stu-id="f1735-211">Complete the first step of the dialog box by completing the following information, and then click **Next**:</span></span>

    1.  <span data-ttu-id="f1735-212">**Extensão**— Insira uma nova extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f1735-212">**Extension**—Enter a new file name extension.</span></span> <span data-ttu-id="f1735-213">Este campo está em branco por padrão.</span><span class="sxs-lookup"><span data-stu-id="f1735-213">This field is blank by default.</span></span>

    2.  <span data-ttu-id="f1735-214">**Crie um novo tipo de arquivo com esta descrição**: Selecione este botão de opção para inserir uma nova descrição de tipo de arquivo no campo ativo.</span><span class="sxs-lookup"><span data-stu-id="f1735-214">**Create a new file type with this description**—Select this radio button to enter a new file type description in the active field.</span></span> <span data-ttu-id="f1735-215">Esse botão está selecionado por padrão, e o campo ativo está em branco.</span><span class="sxs-lookup"><span data-stu-id="f1735-215">This button is selected by default, and the active field is blank.</span></span>

    3.  <span data-ttu-id="f1735-216">**Aplicar este tipo de arquivo a todos os usuários**— Marque essa caixa de seleção quando quiser que essa associação seja global para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="f1735-216">**Apply this file type to all users**—Select this check box when you want this association to be global for all users.</span></span> <span data-ttu-id="f1735-217">Por padrão, essa caixa está desmarcada.</span><span class="sxs-lookup"><span data-stu-id="f1735-217">By default, this box is cleared.</span></span>

    4.  <span data-ttu-id="f1735-218">**Vincular esta extensão a um tipo de arquivo existente**— Selecione este botão de opção para associar a extensão a um tipo de arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="f1735-218">**Link this extension with an existing file type**—Select this radio button to associate the extension with an existing file type.</span></span> <span data-ttu-id="f1735-219">Escolha um tipo de arquivo na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="f1735-219">Pick a file type from the drop-down list.</span></span> <span data-ttu-id="f1735-220">Quando você escolher essa opção, a **próxima** será alterada para **concluir**.</span><span class="sxs-lookup"><span data-stu-id="f1735-220">When you choose this option, **Next** is changed to **Finish**.</span></span>

3.  <span data-ttu-id="f1735-221">Complete a segunda etapa da caixa de diálogo completando as informações a seguir e, em seguida, clique em **concluir** para retornar ao console de gerenciamento de cliente:</span><span class="sxs-lookup"><span data-stu-id="f1735-221">Complete the second step of the dialog box by completing the following information, and then click **Finish** to return to the Client Management Console:</span></span>

    1.  <span data-ttu-id="f1735-222">**Alterar ícone**— clique neste botão para alterar o ícone do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1735-222">**Change Icon**—Click this button to change the application icon.</span></span> <span data-ttu-id="f1735-223">Selecione um dos ícones disponíveis ou navegue até um novo local e selecione um ícone.</span><span class="sxs-lookup"><span data-stu-id="f1735-223">Select one of the available icons, or browse to a new location and select an icon.</span></span>

    2.  <span data-ttu-id="f1735-224">**Abrir arquivos com o aplicativo selecionado**— Selecione este botão de opção para abrir o arquivo com um aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="f1735-224">**Open files with the selected application**—Select this radio button to open the file with an existing application.</span></span> <span data-ttu-id="f1735-225">Escolha um aplicativo na lista suspensa de aplicativos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f1735-225">Choose an application from the drop-down list of available applications.</span></span>

    3.  <span data-ttu-id="f1735-226">**Abrir arquivo com a associação descrita neste arquivo OSD**– Selecione este botão de opção para especificar um arquivo do descritor de software (OSD) aberto que determina o aplicativo usado para abrir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="f1735-226">**Open file with the association described in this OSD file**—Select this radio button to specify an Open Software Descriptor (OSD) file that determines the application used to open the file.</span></span> <span data-ttu-id="f1735-227">Use o botão procurar para selecionar um local existente ou digite um caminho ou uma URL formatada HTTP nesse campo.</span><span class="sxs-lookup"><span data-stu-id="f1735-227">Use the browse button to select an existing location, or enter a path or HTTP-formatted URL in this field.</span></span>

## <span data-ttu-id="f1735-228">Como excluir uma associação de tipo de arquivo para um aplicativo App-V</span><span class="sxs-lookup"><span data-stu-id="f1735-228">How to delete a file type association for an App-V application</span></span>


<span data-ttu-id="f1735-229">Você pode usar o procedimento a seguir para excluir uma associação de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f1735-229">You can use the following procedure to delete a file type association.</span></span> <span data-ttu-id="f1735-230">O nó **associações de tipo de arquivo** é um nível abaixo do nó **virtualização do aplicativo** no painel **escopo** .</span><span class="sxs-lookup"><span data-stu-id="f1735-230">The **File Type Associations** node is one level below the **Application Virtualization** node in the **Scope** pane.</span></span> <span data-ttu-id="f1735-231">Quando você seleciona esse nó, o painel de **resultados** exibe uma lista de associações de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f1735-231">When you select this node, the **Results** pane displays a list of file type associations.</span></span>

**<span data-ttu-id="f1735-232">Para remover uma associação de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="f1735-232">To remove a file type association</span></span>**

1.  <span data-ttu-id="f1735-233">No painel de **resultados** , clique com o botão direito do mouse na extensão da Associação de tipo de arquivo que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="f1735-233">In the **Results** pane, right-click the extension of the file type association you want to delete.</span></span>

2.  <span data-ttu-id="f1735-234">Selecione **excluir** no menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="f1735-234">Select **Delete** from the pop-up menu.</span></span>

3.  <span data-ttu-id="f1735-235">Clique em **Sim** para excluir a associação ou em **não** para retornar ao painel de **resultados** .</span><span class="sxs-lookup"><span data-stu-id="f1735-235">Click **Yes** to delete the association, or click **No** to return to the **Results** pane.</span></span>

## <span data-ttu-id="f1735-236">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1735-236">Related topics</span></span>


[<span data-ttu-id="f1735-237">Cliente do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f1735-237">Application Virtualization Client</span></span>](application-virtualization-client.md)

 

 





