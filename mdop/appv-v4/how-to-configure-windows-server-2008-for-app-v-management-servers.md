---
title: Como configurar o Windows Server 2008 paro App-V Management Servers
description: Como configurar o Windows Server 2008 paro App-V Management Servers
author: dansimp
ms.assetid: 38b4016f-de82-4209-9159-387d20ddee25
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2d1cd7e84ffc0036c98e70a9a0ee1fd3a4ade790
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797182"
---
# <span data-ttu-id="c98ea-103">Como configurar o Windows Server 2008 paro App-V Management Servers</span><span class="sxs-lookup"><span data-stu-id="c98ea-103">How to Configure Windows Server 2008 for App-V Management Servers</span></span>


<span data-ttu-id="c98ea-104">O servidor do Windows Server 2008 no qual você instala o serviço Web de gerenciamento do Microsoft Application Virtualization (App-V) requer que os serviços de informações da Internet (IIS) sejam instalados como uma função no servidor.</span><span class="sxs-lookup"><span data-stu-id="c98ea-104">The Windows Server 2008 server on which you install the Microsoft Application Virtualization (App-V) Management Web Service requires Internet Information Services (IIS) to be installed as a role on the server.</span></span> <span data-ttu-id="c98ea-105">Use o procedimento a seguir para configurar o Windows Server 2008 para dar suporte à instalação do App-vserver.</span><span class="sxs-lookup"><span data-stu-id="c98ea-105">Use the following procedure to configure Windows Server 2008 to support App-Vserver installation.</span></span>

**<span data-ttu-id="c98ea-106">Para instalar o IIS em um computador com Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="c98ea-106">To install IIS on a Windows Server2008 computer</span></span>**

1.  <span data-ttu-id="c98ea-107">No computador Windows Server2008, clique em **Iniciar**, clique em **todos os programas**, clique em **Ferramentas administrativas**e clique em **Gerenciador de servidores** para iniciar o Gerenciador de servidores.</span><span class="sxs-lookup"><span data-stu-id="c98ea-107">On the Windows Server2008 computer, click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Server Manager** to start Server Manager.</span></span> <span data-ttu-id="c98ea-108">No Gerenciador de servidores, clique com o botão direito do mouse no nó **funções** e clique em **adicionar funções** para iniciar o **Assistente para adicionar funções**.</span><span class="sxs-lookup"><span data-stu-id="c98ea-108">In Server Manager, right-click the **Roles** node, and click **Add Roles** to start the **Add Roles Wizard**.</span></span>

2.  <span data-ttu-id="c98ea-109">No **Assistente para adicionar funções**, na página **selecionar funções do servidor** , selecione **servidor Web (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="c98ea-109">In the **Add Roles Wizard**, on the **Select Server Roles** page, select **Web Server (IIS)**.</span></span> <span data-ttu-id="c98ea-110">Quando solicitado, clique em **Adicionar recursos necessários** para adicionar os recursos dependentes.</span><span class="sxs-lookup"><span data-stu-id="c98ea-110">When prompted, click **Add Required Features** to add the dependent features.</span></span>

3.  <span data-ttu-id="c98ea-111">Na página **selecionar funções de servidor** , clique em **Avançar**e, em seguida, clique em **Avançar** novamente.</span><span class="sxs-lookup"><span data-stu-id="c98ea-111">On the **Select Server Roles** page, Click **Next**, and then click **Next** again.</span></span>

4.  <span data-ttu-id="c98ea-112">No **Assistente para adicionar funções**, na página **selecionar serviços de função** :</span><span class="sxs-lookup"><span data-stu-id="c98ea-112">In the **Add Roles Wizard**, on the **Select Role Services** page:</span></span>

    1.  <span data-ttu-id="c98ea-113">Em **desenvolvimento de aplicativos**, selecione **ASP.net** e, quando solicitado, clique em **Adicionar serviços de função necessários** para adicionar os serviços e recursos de funções dependentes.</span><span class="sxs-lookup"><span data-stu-id="c98ea-113">Under **Application Development**, select **ASP.NET** and, when prompted, click **Add Required Role Services** to add the dependent roles services and features.</span></span>

    2.  <span data-ttu-id="c98ea-114">Em **segurança**, selecione **autenticação do Windows**.</span><span class="sxs-lookup"><span data-stu-id="c98ea-114">Under **Security**, select **Windows Authentication**.</span></span>

    3.  <span data-ttu-id="c98ea-115">No nó **ferramentas de gerenciamento** , selecione **scripts e ferramentas de gerenciamento do IIS**.</span><span class="sxs-lookup"><span data-stu-id="c98ea-115">In the **Management Tools** node, select **IIS Management Scripts and Tools**.</span></span> <span data-ttu-id="c98ea-116">Em **compatibilidade com gerenciamento do IIS6**, verifique se a **compatibilidade da metabase do Iis6** e a compatibilidade do WMI do **IIS6** estão selecionadas e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="c98ea-116">Under **IIS6 Management Compatibility**, ensure that both **IIS6 Metabase Compatibility** and **IIS6 WMI Compatibility** are selected, and then click **Next**.</span></span>

5.  <span data-ttu-id="c98ea-117">Na página **confirmar seleções de instalação** , clique em **instalar**e, em seguida, conclua o restante do assistente.</span><span class="sxs-lookup"><span data-stu-id="c98ea-117">On the **Confirm Installation Selections** page, click **Install**, and then complete the rest of the wizard.</span></span>

6.  <span data-ttu-id="c98ea-118">Clique em **fechar** para sair do **Assistente para adicionar funções**e feche o Gerenciador de servidores.</span><span class="sxs-lookup"><span data-stu-id="c98ea-118">Click **Close** to exit the **Add Roles Wizard**, and then close Server Manager.</span></span>

## <span data-ttu-id="c98ea-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c98ea-119">Related topics</span></span>


[<span data-ttu-id="c98ea-120">Requisitos para implantação do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="c98ea-120">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)

[<span data-ttu-id="c98ea-121">Listas de verificação de atualização e implantação do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="c98ea-121">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





