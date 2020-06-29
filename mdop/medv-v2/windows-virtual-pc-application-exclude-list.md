---
title: Lista de exclusão do aplicativo Windows Virtual PC
description: Lista de exclusão do aplicativo Windows Virtual PC
author: dansimp
ms.assetid: 7715f198-f5ed-421e-8740-0cec2ca4ece3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/28/2017
ms.openlocfilehash: 190049ce99865ef237d8d26e14a8279def7da521
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799323"
---
# <span data-ttu-id="9098e-103">Lista de exclusão do aplicativo Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9098e-103">Windows Virtual PC Application Exclude List</span></span>


<span data-ttu-id="9098e-104">Em alguns casos, talvez você não queira que os aplicativos instalados no espaço de trabalho do MED-V sejam publicados no menu **Iniciar** do computador host.</span><span class="sxs-lookup"><span data-stu-id="9098e-104">In some instances, you might not want applications that are installed in the MED-V workspace to be published to the host computer **Start** menu.</span></span> <span data-ttu-id="9098e-105">Você pode cancelar a publicação desses aplicativos seguindo as instruções em [como publicar e cancelar a publicação de um aplicativo no espaço de trabalho do MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="9098e-105">You can unpublish these applications by following the instructions at [How to Publish and Unpublish an Application on the MED-V Workspace](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).</span></span> <span data-ttu-id="9098e-106">No entanto, se o programa for atualizado automaticamente, ele também pode ser republicado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="9098e-106">However, if the program ever automatically updates, it might also be automatically republished.</span></span> <span data-ttu-id="9098e-107">Isso faz com que você tenha que cancelar a publicação do aplicativo novamente.</span><span class="sxs-lookup"><span data-stu-id="9098e-107">This causes you to have to unpublish the application again.</span></span>

<span data-ttu-id="9098e-108">O Windows Virtual PC inclui um recurso conhecido como "lista de exclusões" que permite especificar determinados aplicativos instalados que você não deseja que sejam publicados no menu **Iniciar** do host.</span><span class="sxs-lookup"><span data-stu-id="9098e-108">Windows Virtual PC includes a feature known as the "Exclude List" that lets you specify certain installed applications that you do not want published to the host **Start** menu.</span></span> <span data-ttu-id="9098e-109">A "lista de exclusões" está localizada no registro convidado da chave HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList e lista os aplicativos que não são publicados no menu **Iniciar** do host.</span><span class="sxs-lookup"><span data-stu-id="9098e-109">The "Exclude List" is located in the guest registry in the HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList key and lists those applications that are not published to the host **Start** menu.</span></span> <span data-ttu-id="9098e-110">Você pode considerar a "lista de exclusões" como cancelar permanentemente a publicação dos aplicativos especificados, pois as atualizações automáticas dos aplicativos listados não farão com que eles sejam automaticamente republicados.</span><span class="sxs-lookup"><span data-stu-id="9098e-110">You can think of the “Exclude List” as permanently unpublishing the specified applications because any automatic updates to the applications that are listed will not cause them to be automatically republished.</span></span>

## <span data-ttu-id="9098e-111">Gerenciando aplicativos usando a lista de exclusões no PC virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="9098e-111">Managing Applications by Using the Exclude List in Windows Virtual PC</span></span>


****

1.  <span data-ttu-id="9098e-112">Abra o espaço de trabalho do MED-V em tela inteira.</span><span class="sxs-lookup"><span data-stu-id="9098e-112">Open the MED-V workspace in full screen.</span></span>

    <span data-ttu-id="9098e-113">Para obter informações sobre como abrir o espaço de trabalho do MED-V no modo de tela inteira usando o kit de ferramentas de administração do MED-V, consulte [exibindo as configurações do espaço de trabalho do MED-v](viewing-med-v-workspace-configurations.md#bkmk-fullscreen).</span><span class="sxs-lookup"><span data-stu-id="9098e-113">For information about opening the MED-V workspace in full-screen mode by using the MED-V Administration Toolkit, see [Viewing MED-V Workspace Configurations](viewing-med-v-workspace-configurations.md#bkmk-fullscreen).</span></span> <span data-ttu-id="9098e-114">Ou você pode abri-lo manualmente em tela inteira clicando em **Iniciar**, em **todos os programas**, em **computador virtual do Windows**, clique em **PC virtual do Windows**e, em seguida, clique duas vezes no espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="9098e-114">Or you can manually open it in full screen by clicking **Start**, click **All Programs**, click **Windows Virtual PC**, click **Windows Virtual PC**, and then double-click the MED-V workspace.</span></span>

2.  <span data-ttu-id="9098e-115">Na janela espaço de trabalho do Windows Virtual PC do MED-V, abra o editor do registro.</span><span class="sxs-lookup"><span data-stu-id="9098e-115">In the MED-V workspace Windows Virtual PC window, open Registry Editor.</span></span>

    <span data-ttu-id="9098e-116">Clique em **Iniciar**, clique em **executar**e digite regedit.</span><span class="sxs-lookup"><span data-stu-id="9098e-116">Click **Start**, click **Run**, and then type regedit.</span></span> <span data-ttu-id="9098e-117">Em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="9098e-117">Then click **OK**.</span></span>

3.  <span data-ttu-id="9098e-118">No editor do registro, localize a chave do registro HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList</span><span class="sxs-lookup"><span data-stu-id="9098e-118">In Registry Editor, locate the HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList registry key.</span></span>

4.  <span data-ttu-id="9098e-119">Crie um novo valor do registro para o aplicativo instalado que você não deseja publicar no menu **Iniciar** do computador host.</span><span class="sxs-lookup"><span data-stu-id="9098e-119">Create a new registry value for the installed application that you do not want published to the host computer **Start** menu.</span></span> <span data-ttu-id="9098e-120">Por exemplo, se você quiser cancelar a publicação do programa publicado automaticamente do Microsoft Silverlight, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="9098e-120">For example, if you want to unpublish the automatically published program Microsoft Silverlight, follow these steps:</span></span>

    1.  <span data-ttu-id="9098e-121">Com a chave do registro VPCVAppExcludeList realçada, clique em **Editar**, clique em **novo**e, em seguida, clique em **valor da cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="9098e-121">With the VPCVAppExcludeList registry key highlighted, click **Edit**, click **New**, and then click **String Value**.</span></span>

    2.  <span data-ttu-id="9098e-122">Digite o nome do novo valor do registro.</span><span class="sxs-lookup"><span data-stu-id="9098e-122">Enter the name for the new registry value.</span></span> <span data-ttu-id="9098e-123">Por exemplo, para o Microsoft Silverlight, você pode inserir sllauncher.exe.</span><span class="sxs-lookup"><span data-stu-id="9098e-123">For example, for Microsoft Silverlight, you might enter sllauncher.exe.</span></span>

    3.  <span data-ttu-id="9098e-124">Clique duas vezes no novo valor do registro e insira os dados do valor.</span><span class="sxs-lookup"><span data-stu-id="9098e-124">Double-click the new registry value and enter the value data.</span></span>

        <span data-ttu-id="9098e-125">Os dados de valor são o caminho completo para o comando que você deseja cancelar a publicação.</span><span class="sxs-lookup"><span data-stu-id="9098e-125">The value data is the full path for the command that you want to unpublish.</span></span> <span data-ttu-id="9098e-126">Para encontrar o caminho completo, clique com o botão direito do mouse no menu **Iniciar** do aplicativo que você não deseja publicar e, em seguida, clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="9098e-126">You can find the full path by right-clicking on the shortcut on the **Start** menu for the application that you do not want published and then clicking **Properties**.</span></span> <span data-ttu-id="9098e-127">O caminho completo está listado na guia **atalho** em **destino**.</span><span class="sxs-lookup"><span data-stu-id="9098e-127">The full path is listed in the **Shortcut** tab under **Target**.</span></span>

        <span data-ttu-id="9098e-128">Por exemplo, para o programa Microsoft Silverlight, o caminho completo pode ser "C:\\Arquivos de Files\\Microsoft Silverlight\\4.0.50917.0\\Silverlight.Configuration.exe."</span><span class="sxs-lookup"><span data-stu-id="9098e-128">For example, for the program Microsoft Silverlight, the full path might be "C:\\Program Files\\Microsoft Silverlight\\4.0.50917.0\\Silverlight.Configuration.exe."</span></span>

        <span data-ttu-id="9098e-129">**Importante**  Se aplicável, remova as aspas do caminho completo ao inseri-lo no campo dados do valor.</span><span class="sxs-lookup"><span data-stu-id="9098e-129">**Important** If applicable, remove the quotation marks from the full path when you enter it into the value data field.</span></span>

         

5.  <span data-ttu-id="9098e-130">Feche o editor do registro e reinicie a máquina virtual do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="9098e-130">Close Registry Editor and restart the MED-V workspace virtual machine.</span></span>

    <span data-ttu-id="9098e-131">O aplicativo ainda está instalado no espaço de trabalho do MED-V, mas agora é removido do menu **Iniciar** do computador host.</span><span class="sxs-lookup"><span data-stu-id="9098e-131">The application is still installed in the MED-V workspace but is now removed from the host computer **Start** menu.</span></span>

<span data-ttu-id="9098e-132">Você também pode republicar um aplicativo excluído no menu **Iniciar** do host excluindo o valor correspondente da chave VPCVAppExcludeList.</span><span class="sxs-lookup"><span data-stu-id="9098e-132">You can also republish an excluded application to the host **Start** menu by deleting the corresponding value from the VPCVAppExcludeList key.</span></span> <span data-ttu-id="9098e-133">Por exemplo, para republicar o Microsoft Silverlight, clique com o botão direito do mouse no valor do registro sllauncher.exe e selecione **excluir**.</span><span class="sxs-lookup"><span data-stu-id="9098e-133">For example, to republish Microsoft Silverlight, right-click the registry value sllauncher.exe and select **Delete**.</span></span>

## <span data-ttu-id="9098e-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9098e-134">Related topics</span></span>


[<span data-ttu-id="9098e-135">Referência técnica da MED-V</span><span class="sxs-lookup"><span data-stu-id="9098e-135">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

[<span data-ttu-id="9098e-136">Como publicar e cancelar a publicação de um aplicativo no espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="9098e-136">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





