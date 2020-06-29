---
title: Como instalar o Console de Gerenciamento
description: Como instalar o Console de Gerenciamento
author: dansimp
ms.assetid: 586d99c8-bca6-42e2-a39c-a696053142f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 48f4f69753794cf8099df36828e0502e98414b31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797098"
---
# <span data-ttu-id="a8b43-103">Como instalar o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="a8b43-103">How to Install the Management Console</span></span>


<span data-ttu-id="a8b43-104">Você pode usar o procedimento a seguir para instalar o console de gerenciamento do Application Virtualization em um computador de destino na rede.</span><span class="sxs-lookup"><span data-stu-id="a8b43-104">You can use the following procedure to install the Application Virtualization Management Console on a target computer on the network.</span></span> <span data-ttu-id="a8b43-105">Você deve usar uma conta de rede com privilégios de administrador no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="a8b43-105">You must use a network account that has administrator privileges on the target computer.</span></span> <span data-ttu-id="a8b43-106">Você pode usar o console para configurar e gerenciar a plataforma de sistema do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="a8b43-106">You can use the console to configure and manage the Application Virtualization System Platform.</span></span>

<span data-ttu-id="a8b43-107">Antes de concluir esse procedimento, você deve instalar o serviço Web de gerenciamento do Application Virtualization nesse ou em outro computador.</span><span class="sxs-lookup"><span data-stu-id="a8b43-107">Before you can complete this procedure, you must install the Application Virtualization Management Web Service on this or a different computer.</span></span> <span data-ttu-id="a8b43-108">O serviço Web de gerenciamento permite que você acesse o repositório de dados e o controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="a8b43-108">The Management Web Service allows you to access the data store and the domain controller.</span></span> <span data-ttu-id="a8b43-109">Para obter mais informações sobre como instalar o serviço Web, consulte [como instalar o serviço Web de gerenciamento](how-to-install-the-management-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="a8b43-109">For more information about installing the Web service, see [How to Install the Management Web Service](how-to-install-the-management-web-service.md).</span></span>

**<span data-ttu-id="a8b43-110">Para instalar o console de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="a8b43-110">To install the Management Console</span></span>**

1.  <span data-ttu-id="a8b43-111">Verifique se não há versões anteriores do console de gerenciamento instaladas no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="a8b43-111">Verify that no previous versions of the Management Console are installed on the target computer.</span></span>

2.  <span data-ttu-id="a8b43-112">Navegue até o local do programa de configuração do sistema virtualização de aplicativos na rede, execute este programa da rede ou copie o diretório dele para o computador de destino e, em seguida, clique duas vezes em **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="a8b43-112">Navigate to the location of the Application Virtualization System setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click **Setup.exe**.</span></span>

3.  <span data-ttu-id="a8b43-113">Na **página de boas-vindas**, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="a8b43-113">On the **Welcome Page**, click **Next**.</span></span>

4.  <span data-ttu-id="a8b43-114">Na página **contrato de licença** , para aceitar o contrato de licença, selecione **aceito os termos e as condições da licença**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="a8b43-114">On the **License Agreement** page, to accept the license agreement, select **I accept the license terms and conditions**, and then click **Next**.</span></span>

5.  <span data-ttu-id="a8b43-115">Na página **informações de registro** , especifique o **nome de usuário** e as informações da **organização** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="a8b43-115">On the **Registration Information** page, specify the **User Name** and **Organization** information, and then click **Next**.</span></span>

6.  <span data-ttu-id="a8b43-116">Na página **tipo de instalação** , clique em **personalizado** e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="a8b43-116">On the **Setup Type** page, click **Custom** and then click **Next**.</span></span>

7.  <span data-ttu-id="a8b43-117">Na página **configuração personalizada** , desmarque todos os componentes do sistema do Application Virtualization, exceto **console de gerenciamento**, e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="a8b43-117">On the **Custom Setup** page, deselect all Application Virtualization System components except **Management Console**, and then click **Next**.</span></span>

    <span data-ttu-id="a8b43-118">**Observação**  Se um componente já estiver instalado no computador, desmarque-o na tela instalação personalizada, ele será desinstalado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a8b43-118">**Note** If a component is already installed on the computer, by deselecting it on the Custom Setup screen, it will automatically be uninstalled.</span></span>

     

8.  <span data-ttu-id="a8b43-119">Na tela **pronto para modificar o programa** , clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="a8b43-119">On the **Ready to Modify the Program** screen, click **Install**.</span></span>

    <span data-ttu-id="a8b43-120">**Observação**  Se este for o primeiro componente que você instalar, a página **pronto para instalar o programa** será exibida.</span><span class="sxs-lookup"><span data-stu-id="a8b43-120">**Note** If this is the first component you install, the **Ready to Install the Program** page is displayed.</span></span> <span data-ttu-id="a8b43-121">Para iniciar a instalação, clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="a8b43-121">To start the installation, click **Install**.</span></span>

     

9.  <span data-ttu-id="a8b43-122">Na tela **Assistente de instalação concluído** , clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="a8b43-122">On the **Installation Wizard Completed** screen, click **Finish**.</span></span> <span data-ttu-id="a8b43-123">Clique em **OK** para reiniciar o computador e concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="a8b43-123">Click **Okay** to restart the computer and complete the installation.</span></span>

10. <span data-ttu-id="a8b43-124">No painel de controle do Windows, clique duas vezes em **Ferramentas administrativas** e, em seguida, clique em **console de gerenciamento do Application Virtualization** para exibir o console de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="a8b43-124">In the Windows Control Panel, double-click **Administrative Tools** and then click **Application Virtualization Management Console** to display the Management Console.</span></span>

11. <span data-ttu-id="a8b43-125">Clique no ícone **conectar** ou clique com o botão direito do mouse no contêiner de **sistemas de virtualização de aplicativos** e clique em **conectar ao sistema do Application Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="a8b43-125">Click the **Connect** icon, or right-click the **Application Virtualization Systems** container, and then click **Connect to Application Virtualization System**.</span></span>

12. <span data-ttu-id="a8b43-126">Na tela **conectar-se ao sistema do Application Virtualization** , digite o nome e a porta do host do computador do serviço Web de gerenciamento, altere as informações de segurança e as credenciais de logon, se necessário, e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="a8b43-126">On the **Connect to Application Virtualization System** screen, enter the host name and port of the Management Web Service computer, change the security information and login credentials if necessary, and then click **OK**.</span></span>

13. <span data-ttu-id="a8b43-127">Depois de se conectar ao computador do serviço Web de gerenciamento, clique em **arquivo** no menu **console** e, em seguida, clique em **sair**.</span><span class="sxs-lookup"><span data-stu-id="a8b43-127">After connecting to the Management Web Service computer, click **File** on the **Console** menu, and then click **Exit**.</span></span> <span data-ttu-id="a8b43-128">Clique em **Sim** para salvar as configurações do console.</span><span class="sxs-lookup"><span data-stu-id="a8b43-128">Click **Yes** to save console settings.</span></span>

## <span data-ttu-id="a8b43-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a8b43-129">Related topics</span></span>


[<span data-ttu-id="a8b43-130">Como instalar os componentes de servidores e do sistema</span><span class="sxs-lookup"><span data-stu-id="a8b43-130">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





