---
title: Como instalar e configurar o aplicativo padrão
description: Como instalar e configurar o aplicativo padrão
author: dansimp
ms.assetid: 5c5d5ad1-af40-4f83-8234-39e972f2c29a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083de7a8ebf94bce0b41c0d3c3edf350a9aff38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797111"
---
# <span data-ttu-id="fe653-103">Como instalar e configurar o aplicativo padrão</span><span class="sxs-lookup"><span data-stu-id="fe653-103">How to Install and Configure the Default Application</span></span>


<span data-ttu-id="fe653-104">O aplicativo padrão é fornecido como parte da instalação e é copiado automaticamente para o servidor de gerenciamento do aplicativo Microsoft Application Virtualization (App-V) durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="fe653-104">The default application is provided as part of the installation and is automatically copied to the Microsoft Application Virtualization (App-V) Management Server during installation.</span></span> <span data-ttu-id="fe653-105">Ele é usado para verificar se o servidor de gerenciamento foi instalado e configurado corretamente, mas deve ser publicado no cliente do Microsoft Application Virtualization (App-V) para que o usuário possa acessá-lo.</span><span class="sxs-lookup"><span data-stu-id="fe653-105">It is used to verify that the Management Server was installed and configured correctly, but it has to be published to the Microsoft Application Virtualization (App-V) Client so that the user can access it.</span></span>

<span data-ttu-id="fe653-106">Use os procedimentos a seguir para publicar o aplicativo padrão e para transmiti-lo.</span><span class="sxs-lookup"><span data-stu-id="fe653-106">Use the following procedures to publish the default application and to stream it.</span></span>

**<span data-ttu-id="fe653-107">Para publicar o aplicativo padrão</span><span class="sxs-lookup"><span data-stu-id="fe653-107">To publish the default application</span></span>**

1.  <span data-ttu-id="fe653-108">Faça logon no servidor de gerenciamento do App-V usando uma conta que seja membro do grupo de administradores do App-V especificado durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="fe653-108">Log on to the App-V Management Server by using an account that is a member of the App-V Administrators group specified during installation.</span></span>

2.  <span data-ttu-id="fe653-109">No servidor de gerenciamento App-V, clique em **Iniciar**, clique em **Ferramentas administrativas**e clique em **console de gerenciamento do Application Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="fe653-109">On the App-V Management Server, click **Start**, click **Administrative Tools**, and then click **Application Virtualization Management Console**.</span></span>

3.  <span data-ttu-id="fe653-110">No console de gerenciamento do App-V, clique em **ações**e, em seguida, clique em **conectar ao sistema do Application Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="fe653-110">In the App-V Management Console, click **Actions**, and then click **Connect to Application Virtualization System**.</span></span>

4.  <span data-ttu-id="fe653-111">Na página **Configurar conexão** , desmarque a caixa de seleção **usar conexão segura** .</span><span class="sxs-lookup"><span data-stu-id="fe653-111">On the **Configure Connection** page, clear the **Use Secure Connection** check box.</span></span>

5.  <span data-ttu-id="fe653-112">Na caixa **nome do host do serviço Web** , digite o nome de domínio totalmente qualificado (FQDN) do servidor de gerenciamento do App-V e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe653-112">In the **Web Service Host Name** box, type the fully qualified domain name (FQDN) of the App-V Management Server, and then click **OK**.</span></span>

    <span data-ttu-id="fe653-113">**Observação**  Você também pode usar o **localhost** para o nome de host do serviço Web, se ele estiver instalado no servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="fe653-113">**Note** You can also use **localhost** for the Web Service Host name if it is installed on the Management Server.</span></span>

     

6.  <span data-ttu-id="fe653-114">No console de gerenciamento do App-V, clique com o botão direito do mouse no nó do **servidor** e clique em **Opções do sistema**.</span><span class="sxs-lookup"><span data-stu-id="fe653-114">In the App-V Management Console, right-click the **Server** node, and click **System Options**.</span></span>

7.  <span data-ttu-id="fe653-115">Na guia **geral** , na caixa **caminho do conteúdo padrão** , digite o caminho UNC (Convenção Universal de nomenclatura) para a pasta de conteúdo que você criou no servidor durante a instalação; por exemplo, \ \ \ \ &lt; nome do servidor &gt; \\Content e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe653-115">On the **General** tab, in the **Default Content Path** box, enter the Universal Naming Convention (UNC) path to the Content folder you created on the server during installation; for example, \\\\&lt;Server Name&gt;\\Content, and then click **OK**.</span></span>

    <span data-ttu-id="fe653-116">**Importante**  Use o FQDN do nome do servidor para que o cliente possa resolver o nome corretamente.</span><span class="sxs-lookup"><span data-stu-id="fe653-116">**Important** Use the FQDN for the server name so that the client can resolve the name correctly.</span></span>

     

8.  <span data-ttu-id="fe653-117">No console de gerenciamento do App-V, no painel de navegação, expanda o nó do **servidor** e clique em **aplicativos**.</span><span class="sxs-lookup"><span data-stu-id="fe653-117">In the App-V Management Console, in the navigation pane, expand the **Server** node, and then click **Applications**.</span></span>

9.  <span data-ttu-id="fe653-118">No painel de tópicos, clique em **aplicativo padrão**e, em seguida, no painel **ações** , clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="fe653-118">In the topic pane, click **Default Application**, and then, in the **Actions** pane, click **Properties**.</span></span>

10. <span data-ttu-id="fe653-119">Na caixa de diálogo **Propriedades** , ao lado da caixa **caminho do OSD** , clique em **procurar**.</span><span class="sxs-lookup"><span data-stu-id="fe653-119">In the **Properties** dialog box, next to the **OSD Path** box, click **Browse**.</span></span>

11. <span data-ttu-id="fe653-120">Na caixa de diálogo **abrir** , digite o caminho UNC para a pasta de conteúdo que você criou no servidor durante a instalação; por exemplo, \ \ \ \ &lt; nome do servidor &gt; \\Content e pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="fe653-120">In the **Open** dialog box, enter the UNC path to the Content folder you created on the server during installation; for example, \\\\&lt;Server Name&gt;\\Content, and press ENTER.</span></span> <span data-ttu-id="fe653-121">Você deve usar o nome do servidor real e não pode usar o **localhost** aqui.</span><span class="sxs-lookup"><span data-stu-id="fe653-121">You must use the actual server name and cannot use the **localhost** here.</span></span>

    <span data-ttu-id="fe653-122">**Importante**  Certifique-se de que os valores nas caixas caminho do **OSD** e **caminho do ícone** estejam no formato UNC (por exemplo, \ \ \ \ &lt; nome do servidor &gt; \\Content\\DefaultApp.ico) e aponte para a pasta de conteúdo que você criou ao instalar o servidor.</span><span class="sxs-lookup"><span data-stu-id="fe653-122">**Important** Ensure that the values in both the **OSD Path** and **Icon Path** boxes are in UNC format (for example, \\\\&lt;Server Name&gt;\\Content\\DefaultApp.ico), and point to the Content folder you created when installing the server.</span></span> <span data-ttu-id="fe653-123">Não use **localhost** ou um caminho de arquivo contendo uma letra de unidade, como C:\\Arquivos de Files\\.. \\.. Disputa.</span><span class="sxs-lookup"><span data-stu-id="fe653-123">Do not use **localhost** or a file path containing a drive letter such as C:\\Program Files\\..\\..\\Content.</span></span>

     

12. <span data-ttu-id="fe653-124">Selecione o arquivo DefaultApp. OSD e clique em **abrir**.</span><span class="sxs-lookup"><span data-stu-id="fe653-124">Select the DefaultApp.osd file, and click **Open**.</span></span>

13. <span data-ttu-id="fe653-125">Repita as etapas anteriores para configurar o caminho do ícone.</span><span class="sxs-lookup"><span data-stu-id="fe653-125">Repeat the previous steps to configure the icon path.</span></span>

14. <span data-ttu-id="fe653-126">Clique na guia **permissões de acesso** e confirme se o grupo usuários do App-V tem permissões de acesso ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fe653-126">Click the **Access Permissions** tab, and confirm that the App-V Users group has access permissions to the application.</span></span>

15. <span data-ttu-id="fe653-127">Clique na guia **atalhos** e, em seguida, clique em **publicar na área de trabalho do usuário**.</span><span class="sxs-lookup"><span data-stu-id="fe653-127">Click the **Shortcuts** tab, and then click **Publish to User’s Desktop**.</span></span> <span data-ttu-id="fe653-128">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe653-128">Click **OK**.</span></span>

16. <span data-ttu-id="fe653-129">Abra o Windows Explorer e localize o diretório de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="fe653-129">Open Windows Explorer, and locate the Content directory.</span></span>

17. <span data-ttu-id="fe653-130">Clique duas vezes no arquivo DefaultApp. OSD e abra-o com o bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="fe653-130">Double-click the DefaultApp.osd file, and open it with Notepad.</span></span>

18. <span data-ttu-id="fe653-131">Localize a linha que contém a marca **href** e altere-a para o código a seguir:</span><span class="sxs-lookup"><span data-stu-id="fe653-131">Locate the line that contains the **HREF** tag, and change it to the following code:</span></span>

         `CODEBASEHREF=”RTSP://<FQDN of your server>:554/DefaultApp.sft”`

    <span data-ttu-id="fe653-132">Ou, se você estiver usando RTSPs:</span><span class="sxs-lookup"><span data-stu-id="fe653-132">Or, if you are using RTSPS:</span></span>

         `CODEBASEHREF=”RTSPS://<FQDN of your server>:322/DefaultApp.sft”`

19. <span data-ttu-id="fe653-133">Feche o arquivo DefaultApp. OSD e salve as alterações.</span><span class="sxs-lookup"><span data-stu-id="fe653-133">Close the DefaultApp.osd file, and save the changes.</span></span>

**<span data-ttu-id="fe653-134">Para transmitir o aplicativo padrão</span><span class="sxs-lookup"><span data-stu-id="fe653-134">To stream the default application</span></span>**

1.  <span data-ttu-id="fe653-135">No computador em que o cliente App-V está instalado, faça logon como um usuário que seja membro do grupo usuários da virtualização de aplicativos especificado durante a instalação do servidor.</span><span class="sxs-lookup"><span data-stu-id="fe653-135">On the computer that has the App-V Client installed, log on as a user who is a member of the Application Virtualization Users group specified during server installation.</span></span>

2.  <span data-ttu-id="fe653-136">Na área de trabalho, o atalho **aplicativo padrão do aplicativo virtualização de aplicativos** é exibido.</span><span class="sxs-lookup"><span data-stu-id="fe653-136">On the desktop, the **Default Application Virtualization Application** shortcut appears.</span></span> <span data-ttu-id="fe653-137">Clique duas vezes no atalho para iniciar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fe653-137">Double-click the shortcut to start the application.</span></span>

3.  <span data-ttu-id="fe653-138">Uma barra de status, exibida acima da área de notificação do Windows, relata que o aplicativo está iniciando.</span><span class="sxs-lookup"><span data-stu-id="fe653-138">A status bar, displayed above the Windows notification area, reports that the application is starting.</span></span> <span data-ttu-id="fe653-139">Se a inicialização do aplicativo for bem-sucedida, a tela de título do aplicativo padrão será exibida.</span><span class="sxs-lookup"><span data-stu-id="fe653-139">If the application startup is successful, the title screen for the default application is displayed.</span></span> <span data-ttu-id="fe653-140">Clique em **OK** para fechar a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fe653-140">Click **OK** to close the dialog box.</span></span> <span data-ttu-id="fe653-141">Agora você confirmou que o sistema do App-V está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="fe653-141">You have now confirmed that the App-V system is running correctly.</span></span>

## <span data-ttu-id="fe653-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fe653-142">Related topics</span></span>


[<span data-ttu-id="fe653-143">Como configurar os servidores para a implantação baseada em servidor</span><span class="sxs-lookup"><span data-stu-id="fe653-143">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

 

 





