---
title: Como testar a publicação de aplicativos
description: Como testar a publicação de aplicativos
author: dansimp
ms.assetid: 17ba2e12-50a0-4f41-8300-f61f09db9f6c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 8dffb4f79ac89c7d419b27640f4f05364bd69e5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799967"
---
# <span data-ttu-id="16ea9-103">Como testar a publicação de aplicativos</span><span class="sxs-lookup"><span data-stu-id="16ea9-103">How to Test Application Publishing</span></span>


<span data-ttu-id="16ea9-104">Depois de concluir o teste da configuração inicial, você pode verificar se a funcionalidade de publicação do aplicativo está funcionando como esperado executando as seguintes tarefas.</span><span class="sxs-lookup"><span data-stu-id="16ea9-104">After your test of first time setup finishes, you can verify that the application publishing functionality is working as expected by performing the following tasks.</span></span>

<a href="" id="bkmk-apppub"></a>**<span data-ttu-id="16ea9-105">Para testar a publicação do aplicativo</span><span class="sxs-lookup"><span data-stu-id="16ea9-105">To test application publishing</span></span>**

1.  <span data-ttu-id="16ea9-106">Verifique se os aplicativos que você especificou para publicação estão visíveis.</span><span class="sxs-lookup"><span data-stu-id="16ea9-106">Verify that the applications that you specified for publishing are visible.</span></span>

    <span data-ttu-id="16ea9-107">Clique em **Iniciar** e em **todos os programas** e procure os aplicativos especificados.</span><span class="sxs-lookup"><span data-stu-id="16ea9-107">Click **Start** and then click **All Programs** and search for the specified applications.</span></span>

    <span data-ttu-id="16ea9-108">Em alguns casos, você pode ter o mesmo aplicativo instalado duas vezes, uma vez no computador host e uma vez no convidado.</span><span class="sxs-lookup"><span data-stu-id="16ea9-108">In some cases, you might have the same application installed two times, one time on the host computer and one time on the guest.</span></span> <span data-ttu-id="16ea9-109">Se um aplicativo publicado com o mesmo nome for publicado no mesmo local no menu **Iniciar** host, ele será diferenciado do atalho do aplicativo host adicionando o nome da máquina virtual ao nome do atalho.</span><span class="sxs-lookup"><span data-stu-id="16ea9-109">If a published application that has the same name is published to the same location on the host **Start** menu, it is distinguished from the host application shortcut by adding the virtual machine name to the shortcut name.</span></span> <span data-ttu-id="16ea9-110">Por exemplo, para uma máquina virtual chamada "MEDVHost1", um aplicativo host pode ser "bloco de notas" e um aplicativo publicado pode ser "notepad (MEDVHost1)".</span><span class="sxs-lookup"><span data-stu-id="16ea9-110">For example, for a virtual machine named “MEDVHost1”, a host application might be "Notepad" and a published application might be "Notepad (MEDVHost1)".</span></span>

2.  <span data-ttu-id="16ea9-111">Verifique se os aplicativos funcionam conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="16ea9-111">Verify that the applications function as intended.</span></span>

    <span data-ttu-id="16ea9-112">No computador host, inicie os aplicativos publicados e verifique se eles abrem no Windows XP SP3 no convidado.</span><span class="sxs-lookup"><span data-stu-id="16ea9-112">On the host computer, start the applications that you published and verify that they open in Windows XP SP3 on the guest.</span></span> <span data-ttu-id="16ea9-113">O aplicativo deve aparecer em uma janela no estilo do Windows XP na área de trabalho do computador host.</span><span class="sxs-lookup"><span data-stu-id="16ea9-113">The application must appear in a Windows XP-style window on the host computer desktop.</span></span>

3.  <span data-ttu-id="16ea9-114">Se aplicável, verifique se o redirecionamento do documento funciona conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="16ea9-114">If applicable, verify that document redirection functions as intended.</span></span>

    <span data-ttu-id="16ea9-115">Se um aplicativo publicado no convidado precisa abrir uma pasta na unidade do sistema host, verifique se ela pode abrir a pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="16ea9-115">If a published application on the guest has to open a folder on the host system drive, ensure that it can open the specified folder.</span></span>

    <span data-ttu-id="16ea9-116">**Importante**  Como o Windows Virtual PC não dá suporte à criação de um compartilhamento de uma pasta que já esteja compartilhada, o redirecionamento não ocorre para documentos que se abrem em uma pasta compartilhada, como uma pasta meus documentos localizada na rede.</span><span class="sxs-lookup"><span data-stu-id="16ea9-116">**Important** Because Windows Virtual PC does not support creating a share from a folder that is already shared, redirection does not occur for any documents that open from a shared folder, such as a My Documents folder that is located on the network.</span></span> <span data-ttu-id="16ea9-117">Para obter mais informações, consulte [solução de problemas de operações](operations-troubleshooting-medv2.md).</span><span class="sxs-lookup"><span data-stu-id="16ea9-117">For more information, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

<span data-ttu-id="16ea9-118">Depois de verificar que os aplicativos publicados estão instalados e funcionando corretamente, você pode testar se os aplicativos podem ser adicionados ou removidos do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="16ea9-118">After you have verified that published applications are installed and functioning correctly, you can test whether applications can be added or removed from the MED-V workspace.</span></span>

**<span data-ttu-id="16ea9-119">Para testar se um aplicativo pode ser adicionado ou removido</span><span class="sxs-lookup"><span data-stu-id="16ea9-119">To test that an application can be added or removed</span></span>**

1.  <span data-ttu-id="16ea9-120">Adicionar ou remover um aplicativo do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="16ea9-120">Add or remove an application from the MED-V workspace.</span></span>

    <span data-ttu-id="16ea9-121">Para obter informações sobre como adicionar e remover aplicativos de um espaço de trabalho do MED-V, consulte [Gerenciando aplicativos implantados em espaços de trabalho do MED-v](managing-applications-deployed-to-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="16ea9-121">For information about how to add and remove applications from a MED-V workspace, see [Managing Applications Deployed to MED-V Workspaces](managing-applications-deployed-to-med-v-workspaces.md).</span></span>

2.  <span data-ttu-id="16ea9-122">Se você adicionou um aplicativo, repita as etapas em [para testar a publicação do aplicativo](#bkmk-apppub) para verificar se o novo aplicativo funciona conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="16ea9-122">If you added an application, repeat the steps in [To Test Application Publishing](#bkmk-apppub) to verify that the new application functions as intended.</span></span>

3.  <span data-ttu-id="16ea9-123">Se você removeu um aplicativo, clique em **Iniciar** , em **todos os programas** e verifique se qualquer aplicativo removido não está mais listado.</span><span class="sxs-lookup"><span data-stu-id="16ea9-123">If you removed an application, click **Start** and then click **All Programs** and verify that any applications that you removed are no longer listed.</span></span>

<span data-ttu-id="16ea9-124">**Observação**  Se você encontrar problemas ao verificar as configurações da publicação do aplicativo, consulte [solução de problemas de operações](operations-troubleshooting-medv2.md).</span><span class="sxs-lookup"><span data-stu-id="16ea9-124">**Note** If you encounter any problems when verifying your application publication settings, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

<span data-ttu-id="16ea9-125">Depois de concluir o teste da publicação do aplicativo, você pode testar outras configurações do espaço de trabalho do MED-V para verificar se elas funcionam conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="16ea9-125">After you have completed testing application publishing, you can test other MED-V workspace configurations to verify that they function as intended.</span></span>

<span data-ttu-id="16ea9-126">Depois de concluir o teste do pacote do espaço de trabalho do MED-V e ter confirmado que ele está funcionando conforme o esperado, você pode implantar o espaço de trabalho do MED-V na sua empresa.</span><span class="sxs-lookup"><span data-stu-id="16ea9-126">After you have completed testing your MED-V workspace package and have verified that it is functioning as intended, you can deploy the MED-V workspace to your enterprise.</span></span>

## <span data-ttu-id="16ea9-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="16ea9-127">Related topics</span></span>

[<span data-ttu-id="16ea9-128">Como testar o redirecionamento da URL</span><span class="sxs-lookup"><span data-stu-id="16ea9-128">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

[<span data-ttu-id="16ea9-129">Como verificar as configurações da primeira instalação</span><span class="sxs-lookup"><span data-stu-id="16ea9-129">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

[<span data-ttu-id="16ea9-130">Como implantar o pacote de espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="16ea9-130">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)

 

 





