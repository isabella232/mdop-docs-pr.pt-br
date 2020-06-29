---
title: Como aplicar configurações de máquina virtual a um espaço de trabalho do MED-V
description: Como aplicar configurações de máquina virtual a um espaço de trabalho do MED-V
author: dansimp
ms.assetid: b50d0dfb-8d61-4543-9607-a29bbb1ed45f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9662bb8202285d51971eeea8beaef938b98ed6b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799779"
---
# <span data-ttu-id="ba6dc-103">Como aplicar configurações de máquina virtual a um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="ba6dc-103">How to Apply Virtual Machine Settings to a MED-V Workspace</span></span>


<span data-ttu-id="ba6dc-104">Todos os espaços de trabalho do MED-V devem ter uma imagem do Microsoft Virtual PC associada a ele.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-104">Every MED-V workspace must have a Microsoft Virtual PC image associated with it.</span></span> <span data-ttu-id="ba6dc-105">As configurações da máquina virtual permitem atribuir uma imagem do Virtual PC e definir outras propriedades da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-105">The virtual machine settings enable you to assign a Virtual PC image as well as set other virtual machine properties.</span></span>

<span data-ttu-id="ba6dc-106">Todas as configurações da máquina virtual são configuradas no módulo de **política** , na guia **configurações de máquina virtual** .</span><span class="sxs-lookup"><span data-stu-id="ba6dc-106">All virtual machine settings are configured in the **Policy** module, on the **Virtual Machine Settings** tab.</span></span>

**<span data-ttu-id="ba6dc-107">Para aplicar as configurações da máquina virtual a um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="ba6dc-107">To apply virtual machine settings to a MED-V workspace</span></span>**

1.  <span data-ttu-id="ba6dc-108">Clique no espaço de trabalho do MED-V para configurar.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-108">Click the MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="ba6dc-109">Configure as propriedades da máquina virtual conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-109">Configure the virtual machine properties as described in the following table.</span></span>

3.  <span data-ttu-id="ba6dc-110">No menu **política** , selecione **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-110">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="ba6dc-111">Propriedades da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="ba6dc-111">Virtual Machine Properties</span></span>**

<span data-ttu-id="ba6dc-112">Descrição da propriedade *configurações da máquina virtual*</span><span class="sxs-lookup"><span data-stu-id="ba6dc-112">Property Description *Virtual Machine Settings*</span></span>

<span data-ttu-id="ba6dc-113">Imagem atribuída</span><span class="sxs-lookup"><span data-stu-id="ba6dc-113">Assigned Image</span></span>

<span data-ttu-id="ba6dc-114">A imagem real do Microsoft Virtual PC atribuída ao espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-114">The actual Microsoft Virtual PC image assigned to the MED-V workspace.</span></span> <span data-ttu-id="ba6dc-115">O menu fornece uma lista de todas as imagens disponíveis do Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-115">The menu provides a list of all available Virtual PC images.</span></span> <span data-ttu-id="ba6dc-116">Os seguintes tipos de imagem estão na lista de imagens **ativas** :</span><span class="sxs-lookup"><span data-stu-id="ba6dc-116">The following image types are in the **Active** image list:</span></span>

-   <span data-ttu-id="ba6dc-117">**Imagens de teste locais**— imagens no computador local que ainda não foram compactadas.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-117">**Local test images**—Images on the local computer that are not yet packed.</span></span> <span data-ttu-id="ba6dc-118">Esses nomes de imagens são seguidos pela palavra "Test" entre parênteses (teste) e só para fins de teste.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-118">These image names are followed by the word “test” in parentheses (test) and are for testing purposes only.</span></span>

-   <span data-ttu-id="ba6dc-119">**Imagens compactadas locais**— imagens compactadas no computador local.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-119">**Local packed images**—Packed images on the local computer.</span></span> <span data-ttu-id="ba6dc-120">Essas imagens são seguidas pela palavra "local" entre parênteses (local) e não podem ser baixadas pelos clientes até que o administrador os carregue para o servidor.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-120">These images are followed by the word “local” in parentheses (local) and cannot be downloaded by clients until the administrator uploads them to the server.</span></span>

    <span data-ttu-id="ba6dc-121">Uma imagem local pode ser selecionada se você estiver criando um pacote que será distribuído para o cliente via mídia removível (como USB ou DVD).</span><span class="sxs-lookup"><span data-stu-id="ba6dc-121">A local image can be selected if you are creating a package that will be distributed to the client via removable media (such as USB or DVD).</span></span>

-   <span data-ttu-id="ba6dc-122">**Imagens compactadas no servidor**— imagens que estão no servidor e estão disponíveis para download por clientes.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-122">**Packed images on server**—Images that are on the server and are available for download by clients.</span></span> <span data-ttu-id="ba6dc-123">Clique em atualizar para atualizar a lista imagens.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-123">Click Refresh to refresh the images list.</span></span>

    <span data-ttu-id="ba6dc-124">**Observação**  Cada imagem do espaço de trabalho do MED-V só pode ser usada por um usuário do Windows.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-124">**Note** Each MED-V workspace image can only be used by one Windows user.</span></span>

     

<span data-ttu-id="ba6dc-125">O espaço de trabalho é persistente</span><span class="sxs-lookup"><span data-stu-id="ba6dc-125">Workspace is persistent</span></span>

<span data-ttu-id="ba6dc-126">Marque esta caixa de seleção para configurar o espaço de trabalho do MED-V como persistente.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-126">Select this check box to configure the MED-V workspace as persistent.</span></span> <span data-ttu-id="ba6dc-127">Em um espaço de trabalho do MED-V persistente, quando o espaço de trabalho do MED-V é interrompido, as alterações e inclusões no espaço de trabalho do MED-v são salvas no espaço de trabalho do MED-v.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-127">In a persistent MED-V workspace, when the MED-V workspace is stopped, changes and additions to the MED-V workspace are saved in the MED-V workspace.</span></span>

<span data-ttu-id="ba6dc-128">Para um espaço de trabalho do MED-V de domínio, essa opção deve ser selecionada.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-128">For a Domain MED-V workspace, this option must be selected.</span></span>

<span data-ttu-id="ba6dc-129">**Observação**  Essa configuração não deve ser alterada após a implantação de um espaço de trabalho do MED-V para os usuários.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-129">**Note** This setting should not be changed after a MED-V workspace is deployed to users.</span></span>

 

<span data-ttu-id="ba6dc-130">Desligar a VM ao interromper o espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="ba6dc-130">Shut down the VM when stopping the Workspace</span></span>

<span data-ttu-id="ba6dc-131">Marque esta caixa de seleção para desligar a máquina virtual ao parar o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-131">Select this check box to shut down the virtual machine when stopping the MED-V workspace.</span></span> <span data-ttu-id="ba6dc-132">Se essa caixa de seleção estiver desmarcada, na conclusão de cada sessão, a máquina virtual não será desligada, mas, em vez disso, usará um instantâneo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-132">If this check box is cleared, at the completion of each session, the virtual machine is not shut down but instead takes a snapshot of the virtual machine.</span></span> <span data-ttu-id="ba6dc-133">Durante a inicialização de uma nova sessão, o Windows é iniciado a partir do instantâneo (ou seja, o Windows não é reiniciado e não é necessário fazer logon).</span><span class="sxs-lookup"><span data-stu-id="ba6dc-133">Upon the initiation of a new session, Windows starts from the snapshot (that is, Windows does not restart and no login is required).</span></span>

<span data-ttu-id="ba6dc-134">**Observação**  Essa propriedade será habilitada somente se o **espaço de trabalho for persistente** estiver selecionado.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-134">**Note** This property is enabled only if **Workspace is persistent** is selected.</span></span>

 

<span data-ttu-id="ba6dc-135">Logon no Windows na VM usando credenciais do MED-V (SSO)</span><span class="sxs-lookup"><span data-stu-id="ba6dc-135">Logon to Windows in VM using MED-V credentials (SSO)</span></span>

<span data-ttu-id="ba6dc-136">Marque esta caixa de seleção para entrar no Windows na máquina virtual usando as credenciais do MED-V inseridas ao fazer logon no cliente MED-V.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-136">Select this check box to log in to Windows on the virtual machine by using the MED-V credentials entered when logging in to MED-V client.</span></span>

<span data-ttu-id="ba6dc-137">**Observação**  Essa propriedade é habilitada somente quando o **espaço de trabalho é persistente** é selecionado.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-137">**Note** This property is enabled only when **Workspace is persistent** is selected.</span></span>

 

<span data-ttu-id="ba6dc-138">O espaço de trabalho é reversível</span><span class="sxs-lookup"><span data-stu-id="ba6dc-138">Workspace is revertible</span></span>

<span data-ttu-id="ba6dc-139">Marque esta caixa de seleção para configurar o espaço de trabalho do MED-V como reversível.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-139">Select this check box to configure the MED-V workspace as revertible.</span></span> <span data-ttu-id="ba6dc-140">Em um espaço de trabalho do MED-V reversível, na conclusão de cada sessão (ou seja, quando o usuário pára o espaço de trabalho do MED-V), o espaço de trabalho do MED-V é revertido para o estado original que estava durante a implantação.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-140">In a revertible MED-V workspace, at the completion of each session (that is, when the user stops the MED-V workspace), the MED-V workspace reverts to the original state it was in during deployment.</span></span> <span data-ttu-id="ba6dc-141">Nenhuma alteração ou acréscimo feita pelo usuário é salva no espaço de trabalho do MED-V entre as sessões.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-141">No changes or additions that the user made are saved on the MED-V workspace between sessions.</span></span>

<span data-ttu-id="ba6dc-142">**Observação**  Essa configuração não deve ser alterada após a implantação de um espaço de trabalho do MED-V para os usuários.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-142">**Note** This setting should not be changed after a MED-V workspace is deployed to users.</span></span>

 

<span data-ttu-id="ba6dc-143">Sincronizar o fuso horário do espaço de trabalho com o host</span><span class="sxs-lookup"><span data-stu-id="ba6dc-143">Synchronize Workspace time zone with host</span></span>

<span data-ttu-id="ba6dc-144">Marque esta caixa de seleção para sincronizar o fuso horário no espaço de trabalho do MED-V com o host.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-144">Select this check box to synchronize the time zone in the MED-V workspace with the host.</span></span>

<span data-ttu-id="ba6dc-145">A sincronização funciona de forma diferente, dependendo se o espaço de trabalho do MED-V é persistente ou reversível, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ba6dc-145">The synchronization works differently depending on whether the MED-V workspace is persistent or revertible, as follows:</span></span>

-   <span data-ttu-id="ba6dc-146">Em um espaço de trabalho do MED-V persistente, o fuso horário primeiro tenta sincronizar com o servidor.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-146">In a persistent MED-V workspace, the time zone first tries to synchronize with the server.</span></span> <span data-ttu-id="ba6dc-147">Se isso falhar, ele será sincronizado com o host.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-147">If that fails, it synchronizes with the host.</span></span>

-   <span data-ttu-id="ba6dc-148">Em um espaço de trabalho do MED-V reversível, o fuso horário é sincronizado com o host.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-148">In a revertible MED-V workspace, the time zone synchronizes with the host.</span></span>

*<span data-ttu-id="ba6dc-149">Configurações de bloqueio</span><span class="sxs-lookup"><span data-stu-id="ba6dc-149">Lock Settings</span></span>*

<span data-ttu-id="ba6dc-150">Bloquear o espaço de trabalho no evento de hibernação/espera do host</span><span class="sxs-lookup"><span data-stu-id="ba6dc-150">Lock the Workspace on host standby/hibernate event</span></span>

<span data-ttu-id="ba6dc-151">Marque esta caixa de seleção para bloquear automaticamente o espaço de trabalho do MED-V quando o computador host entrar no modo de espera ou hibernação.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-151">Select this check box to automatically lock the MED-V workspace when the host computer goes into standby or hibernate.</span></span>

<span data-ttu-id="ba6dc-152">Bloquear o espaço de trabalho após</span><span class="sxs-lookup"><span data-stu-id="ba6dc-152">Lock the Workspace after</span></span>

<span data-ttu-id="ba6dc-153">Marque esta caixa de seleção para bloquear o espaço de trabalho do MED-V quando o espaço de trabalho do MED-V estiver ocioso por um período de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-153">Select this check box to lock the MED-V workspace when the MED-V workspace is idle for a specified period of time.</span></span> <span data-ttu-id="ba6dc-154">Quando selecionada, a caixa número está habilitada.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-154">When selected, the number box is enabled.</span></span> <span data-ttu-id="ba6dc-155">Digite o número de minutos de tempo ocioso antes de bloquear o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-155">Enter the number of minutes of idle time before locking the MED-V workspace.</span></span>

<span data-ttu-id="ba6dc-156">**Observação**  O tempo ocioso refere-se aos aplicativos do espaço de trabalho do MED-V (não aos aplicativos host).</span><span class="sxs-lookup"><span data-stu-id="ba6dc-156">**Note** The idle time refers to the MED-V workspace applications (not the host applications).</span></span>

 

*<span data-ttu-id="ba6dc-157">Configurações de atualização de imagem</span><span class="sxs-lookup"><span data-stu-id="ba6dc-157">Image Update Settings</span></span>*

<span data-ttu-id="ba6dc-158">Manter somente</span><span class="sxs-lookup"><span data-stu-id="ba6dc-158">Keep only</span></span>

<span data-ttu-id="ba6dc-159">Marque esta caixa de seleção para limitar o número de versões de imagem antigas a serem mantidas.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-159">Select this check box to limit the number of old image versions to keep.</span></span>

<span data-ttu-id="ba6dc-160">Quando selecionada, a caixa número está habilitada.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-160">When selected, the number box is enabled.</span></span> <span data-ttu-id="ba6dc-161">Digite o número de versões antigas a serem mantidas.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-161">Enter the number of old versions to keep.</span></span>

<span data-ttu-id="ba6dc-162">Sugerir atualização quando uma nova versão estiver disponível</span><span class="sxs-lookup"><span data-stu-id="ba6dc-162">Suggest update when a new version is available</span></span>

<span data-ttu-id="ba6dc-163">Marque esta caixa de seleção para sugerir (mas não forçar) uma atualização quando uma nova versão da imagem estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-163">Select this check box to suggest (but not force) an update when a new version of the image is available.</span></span>

<span data-ttu-id="ba6dc-164">Os clientes devem usar a transferência de corte ao baixar imagens para este espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="ba6dc-164">Clients should use Trim Transfer when downloading images for this Workspace</span></span>

<span data-ttu-id="ba6dc-165">Marque esta caixa de seleção para habilitar a transferência de corte (para obter mais informações, consulte [tecnologia de transferência de corte do MED-V](med-v-trim-transfer-technology-medvv2.md)) ao baixar imagens associadas a este espaço de trabalho do MED-v.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-165">Select this check box to enable Trim Transfer (for more information, see [MED-V Trim Transfer Technology](med-v-trim-transfer-technology-medvv2.md)) when downloading images associated with this MED-V workspace.</span></span> <span data-ttu-id="ba6dc-166">Se essa caixa de seleção estiver desmarcada, a imagem inteira será baixada.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-166">If this check box is cleared, the full image will be downloaded.</span></span>

<span data-ttu-id="ba6dc-167">**Observação**  A transferência de corte exige o índice da unidade de disco rígido, o que pode demorar um tempo considerável.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-167">**Note** Trim Transfer requires indexing the hard drive, which might take a considerable amount of time.</span></span> <span data-ttu-id="ba6dc-168">É recomendável usar a transferência de corte ao indexar o disco rígido é mais eficiente do que baixar a nova versão da imagem, por exemplo, ao baixar uma versão de imagem semelhante à existente.</span><span class="sxs-lookup"><span data-stu-id="ba6dc-168">It is recommended to use Trim Transfer when indexing the hard drive is more efficient than downloading the new image version, such as when downloading an image version that is similar to the existing version.</span></span>

 

 

## <span data-ttu-id="ba6dc-169">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba6dc-169">Related topics</span></span>


[<span data-ttu-id="ba6dc-170">Criando uma imagem do MED-V</span><span class="sxs-lookup"><span data-stu-id="ba6dc-170">Creating a MED-V Image</span></span>](creating-a-med-v-image.md)

[<span data-ttu-id="ba6dc-171">Usando a interface de usuário do Console de Gerenciamento do MED-V</span><span class="sxs-lookup"><span data-stu-id="ba6dc-171">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="ba6dc-172">Criando um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="ba6dc-172">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

 

 





