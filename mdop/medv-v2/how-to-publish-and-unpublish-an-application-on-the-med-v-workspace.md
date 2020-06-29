---
title: Como publicar e cancelar a publicação de um aplicativo no espaço de trabalho da MED-V
description: Como publicar e cancelar a publicação de um aplicativo no espaço de trabalho da MED-V
author: dansimp
ms.assetid: fd5a62e9-0577-44d2-ae17-61c0aef78ce8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cc8f9579d800aa0e5da0d67e0cd71bcae5e912a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799969"
---
# <span data-ttu-id="f5fbb-103">Como publicar e cancelar a publicação de um aplicativo no espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="f5fbb-103">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>


<span data-ttu-id="f5fbb-104">Embora um aplicativo seja instalado em um espaço de trabalho do MED-V, você também pode ter que publicar o aplicativo antes que ele fique disponível para o usuário final.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-104">Even though an application is installed in a MED-V workspace, you might also have to publish the application before it becomes available to the end user.</span></span> <span data-ttu-id="f5fbb-105">Por padrão, a maioria dos aplicativos é publicada no momento em que são instalados e os atalhos são criados e habilitados.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-105">By default, most applications are published at the time that they are installed and shortcuts are created and enabled.</span></span>

<span data-ttu-id="f5fbb-106">Em alguns casos, talvez você queira instalar aplicativos no espaço de trabalho do MED-V sem disponibilizá-los para o usuário final, por exemplo, software de verificação de vírus.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-106">In some cases, you might want to install applications on the MED-V workspace without making them available to the end user, for example, virus-scanning software.</span></span> <span data-ttu-id="f5fbb-107">Da mesma forma, há ocasiões em que você deseja publicar um aplicativo instalado no espaço de trabalho do MED-V que estava indisponível anteriormente para o usuário final.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-107">Similarly, there are occasions in which you want to publish an application that is installed on the MED-V workspace that was previously unavailable to the end user.</span></span> <span data-ttu-id="f5fbb-108">Por exemplo, talvez seja necessário publicar um aplicativo instalado se a instalação não criar automaticamente um atalho no menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="f5fbb-108">For example, you might have to publish an installed application if the installation did not automatically create a shortcut on the **Start** menu.</span></span>

<span data-ttu-id="f5fbb-109">**Importante**  Se você publicar um aplicativo que não dê suporte a caminhos UNC, recomendamos mapear o aplicativo para uma unidade.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-109">**Important** If you publish an application that does not support UNC paths, we recommend that you map the application to a drive.</span></span>

 

<span data-ttu-id="f5fbb-110">Você pode publicar ou cancelar a publicação de aplicativos em um espaço de trabalho do MED-V implantado executando uma das seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="f5fbb-110">You can publish or unpublish applications to a deployed MED-V workspace by performing one of the following tasks:</span></span>

**<span data-ttu-id="f5fbb-111">Para publicar ou cancelar a publicação de um aplicativo instalado</span><span class="sxs-lookup"><span data-stu-id="f5fbb-111">To publish or unpublish an installed application</span></span>**

1.  <span data-ttu-id="f5fbb-112">Para publicar um aplicativo em um espaço de trabalho do MED-V implantado, copie um atalho para esse aplicativo para a pasta a seguir na máquina virtual:</span><span class="sxs-lookup"><span data-stu-id="f5fbb-112">To publish an application on a deployed MED-V workspace, copy a shortcut for that application to the following folder on the virtual machine:</span></span>

    <span data-ttu-id="f5fbb-113">Menu C:\\Documents e Settings\\All Users\\Start</span><span class="sxs-lookup"><span data-stu-id="f5fbb-113">C:\\Documents and Settings\\All Users\\Start Menu</span></span>

    <span data-ttu-id="f5fbb-114">Se for necessário, use a política de grupo ou um sistema ESD para implantar um script que copia o atalho do aplicativo para a pasta de menu todos os Users\\Start.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-114">If it is necessary, use Group Policy or an ESD system to deploy a script that copies the shortcut for that application to the All Users\\Start Menu folder.</span></span>

2.  <span data-ttu-id="f5fbb-115">Para cancelar a publicação de um aplicativo em um espaço de trabalho do MED-V implantado, exclua o atalho para esse aplicativo da seguinte pasta na máquina virtual:</span><span class="sxs-lookup"><span data-stu-id="f5fbb-115">To unpublish an application on a deployed MED-V workspace, delete the shortcut for that application from the following folder on the virtual machine:</span></span>

    <span data-ttu-id="f5fbb-116">Menu C:\\Documents e Settings\\All Users\\Start</span><span class="sxs-lookup"><span data-stu-id="f5fbb-116">C:\\Documents and Settings\\All Users\\Start Menu</span></span>

    <span data-ttu-id="f5fbb-117">Se for necessário, use a política de grupo ou um sistema ESD para implantar um script que exclui o atalho para esse aplicativo na pasta de menu todos os Users\\Start.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-117">If it is necessary, use Group Policy or an ESD system to deploy a script that deletes the shortcut for that application from the All Users\\Start Menu folder.</span></span>

    <span data-ttu-id="f5fbb-118">**Observação**  Freqüentemente, o atalho é excluído automaticamente do menu **Iniciar** do computador host quando você desinstala o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-118">**Note** Frequently, the shortcut is automatically deleted from the host computer **Start** menu when you uninstall the application.</span></span> <span data-ttu-id="f5fbb-119">No entanto, em alguns casos, por exemplo, para um espaço de trabalho do MED-V configurado para todos os usuários de um computador compartilhado, talvez seja necessário excluir manualmente o atalho no menu **Iniciar** após a desinstalação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-119">However, in some cases, such as for a MED-V workspace that is configured for all users of a shared computer, you might have to manually delete the shortcut on the **Start** menu after the application is uninstalled.</span></span> <span data-ttu-id="f5fbb-120">Para fazer isso, o usuário final pode clicar com o botão direito do mouse no atalho e selecionar **excluir**.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-120">The end-user can do this by right-clicking the shortcut and selecting **Delete**.</span></span>

     

<span data-ttu-id="f5fbb-121">Para testar se o aplicativo foi publicado ou cancelado, verifique no espaço de trabalho do MED-V se o atalho correspondente está disponível ou não.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-121">To test that the application was published or unpublished, verify on the MED-V workspace whether the corresponding shortcut is available or not.</span></span>

<span data-ttu-id="f5fbb-122">**Observação**  Os aplicativos incluídos no Windows XP SP3 e estão localizados na pasta do menu Iniciar da máquina virtual não são automaticamente publicados no host.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-122">**Note** Applications that are included in Windows XP SP3 and are located in the virtual machine Start Menu folder are not automatically published to the host.</span></span> <span data-ttu-id="f5fbb-123">Elas são controladas por configurações do registro que bloqueiam a publicação automática.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-123">They are controlled by registry settings that block automatic publishing.</span></span> <span data-ttu-id="f5fbb-124">Para obter mais informações, consulte [lista de exclusões de aplicativos PC virtual do Windows](windows-virtual-pc-application-exclude-list.md).</span><span class="sxs-lookup"><span data-stu-id="f5fbb-124">For more information, see [Windows Virtual PC Application Exclude List](windows-virtual-pc-application-exclude-list.md).</span></span>

 

**<span data-ttu-id="f5fbb-125">Para publicar itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="f5fbb-125">To publish Control Panel items</span></span>**

1.  <span data-ttu-id="f5fbb-126">Crie um atalho na máquina virtual em que o destino é o nome do item, como C:\\WINDOWS\\system32\\appwiz.cpl.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-126">Create a shortcut on the virtual machine where the target is the name of the item, such as C:\\WINDOWS\\system32\\appwiz.cpl.</span></span>

    <span data-ttu-id="f5fbb-127">O atalho deve ser criado ou movido para a pasta "%ALLUSERSPROFILE%\\Start Menu\\" ou uma de suas subpastas.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-127">The shortcut must be either created in or moved to the "%ALLUSERSPROFILE%\\Start Menu\\" folder or one of its subfolders.</span></span>

    <span data-ttu-id="f5fbb-128">O item será publicado no computador host no local correspondente na pasta do menu iniciar host.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-128">The item will be published to the host computer in the corresponding location in the host Start Menu folder.</span></span>

2.  <span data-ttu-id="f5fbb-129">Inicie o atalho para o item no host.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-129">Start the shortcut for the item in the host.</span></span>

<span data-ttu-id="f5fbb-130">**Cuidado**  Quando você cria o atalho, não especifique% SystemRoot% \\control.exe.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-130">**Caution** When you create the shortcut, do not specify %SystemRoot%\\control.exe.</span></span> <span data-ttu-id="f5fbb-131">Este aplicativo não será publicado porque está contido nas configurações do registro que bloqueiam a publicação automática.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-131">This application will not be published because it is contained in the registry settings that block automatic publishing.</span></span>

 

**<span data-ttu-id="f5fbb-132">Como o MED-V manipula a publicação automática de aplicativos</span><span class="sxs-lookup"><span data-stu-id="f5fbb-132">How MED-V handles automatic application publishing</span></span>**

1.  <span data-ttu-id="f5fbb-133">Durante a publicação do aplicativo, o MED-V copia os atalhos da máquina virtual convidada para o computador host tentando corresponder à hierarquia de pastas existente no convidado.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-133">During application publishing, MED-V copies the shortcuts from the guest virtual machine to the host computer by trying to match the folder hierarchy that exists in the guest.</span></span> <span data-ttu-id="f5fbb-134">Fazendo isso, o MED-V copia atalhos do convidado para o host seguindo estas etapas:</span><span class="sxs-lookup"><span data-stu-id="f5fbb-134">By doing this, MED-V copies shortcuts from the guest to the host by following these steps:</span></span>

    1.  <span data-ttu-id="f5fbb-135">O MED-V tenta localizar uma pasta em Start Menu\\Programs no computador host que tem o mesmo nome da pasta no convidado na qual o atalho reside.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-135">MED-V tries to locate a folder under Start Menu\\Programs in the host computer that is named the same as the folder in the guest where the shortcut resides.</span></span>

    2.  <span data-ttu-id="f5fbb-136">Se não houver nenhuma pasta correspondente, o MED-V tentará localizar uma pasta na pasta do menu Iniciar do host com o nome da pasta no convidado em que o atalho reside.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-136">If there is no matching folder, MED-V then tries to locate a folder in the host Start Menu folder that is named the same as the folder in the guest where the shortcut resides.</span></span>

    3.  <span data-ttu-id="f5fbb-137">Se não houver nenhuma pasta correspondente, o MED-V copiará o atalho para a pasta padrão no host, a pasta Start Menu\\Programs.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-137">If there is no matching folder, MED-V copies the shortcut to the default folder on the host, the Start Menu\\Programs folder.</span></span>

2.  <span data-ttu-id="f5fbb-138">Exemplo de processo de publicação do aplicativo:</span><span class="sxs-lookup"><span data-stu-id="f5fbb-138">Example of application publishing process:</span></span>

    1.  <span data-ttu-id="f5fbb-139">Se um atalho de aplicativo for publicado na pasta Start Menu\\Programs\\AppShortcuts no Guest, o MED-V procurará no computador host por uma pasta AppShortcuts de início do Menu\\Programs\\ e, se for encontrado, copiará o atalho para essa pasta.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-139">If an application shortcut is published to the Start Menu\\Programs\\AppShortcuts folder in the guest, then MED-V looks in the host computer for a Start Menu\\Programs\\ AppShortcuts folder and if found, copies the shortcut to that folder.</span></span>

    2.  <span data-ttu-id="f5fbb-140">Se a pasta não for encontrada, o MED-V procura no computador host por uma pasta de início Menu\\AppShortcuts e, se for encontrado, copia o atalho para essa pasta.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-140">If the folder is not found, then MED-V looks in the host computer for a Start Menu\\AppShortcuts folder and if found, copies the shortcut to that folder.</span></span>

    3.  <span data-ttu-id="f5fbb-141">Se a pasta não for encontrada, o MED-V copiará o atalho para a pasta Start Menu\\Programs.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-141">If the folder is not found, then MED-V copies the shortcut to the Start Menu\\Programs folder.</span></span>

<span data-ttu-id="f5fbb-142">**Observação**  Uma pasta já deve existir na pasta do menu Iniciar do computador host para o MED-V copiar o atalho para lá.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-142">**Note** A folder must already exist in the host computer Start Menu folder for MED-V to copy the shortcut there.</span></span> <span data-ttu-id="f5fbb-143">O MED-V não cria a pasta, se ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="f5fbb-143">MED-V does not create the folder if it does not already exist.</span></span>

 

## <span data-ttu-id="f5fbb-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5fbb-144">Related topics</span></span>


[<span data-ttu-id="f5fbb-145">Instalação e remoção de um aplicativo no espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="f5fbb-145">Installing and Removing an Application on the MED-V Workspace</span></span>](installing-and-removing-an-application-on-the-med-v-workspace.md)

[<span data-ttu-id="f5fbb-146">Gerenciamento de atualizações de software para espaços de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="f5fbb-146">Managing Software Updates for MED-V Workspaces</span></span>](managing-software-updates-for-med-v-workspaces.md)

[<span data-ttu-id="f5fbb-147">Lista de exclusão do aplicativo Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f5fbb-147">Windows Virtual PC Application Exclude List</span></span>](windows-virtual-pc-application-exclude-list.md)

 

 





