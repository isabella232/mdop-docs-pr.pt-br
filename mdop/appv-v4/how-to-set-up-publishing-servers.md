---
title: Como configurar servidores de publicação
description: Como configurar servidores de publicação
author: dansimp
ms.assetid: 2111f079-c202-4c49-b2a6-f4237068b2dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f060d862fd1449f5240ad495b53a1fa4e97697f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796943"
---
# <span data-ttu-id="3fd6c-103">Como configurar servidores de publicação</span><span class="sxs-lookup"><span data-stu-id="3fd6c-103">How to Set Up Publishing Servers</span></span>


<span data-ttu-id="3fd6c-104">Você pode usar os procedimentos a seguir para adicionar e configurar servidores de virtualização de aplicativos diretamente do console de gerenciamento de cliente.</span><span class="sxs-lookup"><span data-stu-id="3fd6c-104">You can use the following procedures to add and configure Application Virtualization Servers directly from the Client Management Console.</span></span>

**<span data-ttu-id="3fd6c-105">Para adicionar um servidor de publicação de aplicativos</span><span class="sxs-lookup"><span data-stu-id="3fd6c-105">To add an application publishing server</span></span>**

1.  <span data-ttu-id="3fd6c-106">No painel de **resultados** , clique com o botão direito do mouse e selecione **novo servidor** no menu pop-up-menu para iniciar o novo assistente de servidor de virtualização de aplicativos ou, como alternativa, clique com o botão direito do mouse no nó do **servidor de publicação** e selecione **novo servidor** no menu pop-up-up.</span><span class="sxs-lookup"><span data-stu-id="3fd6c-106">In the **Results** pane, right-click and select **New Server** from the pop-up-menu to start the New Application Virtualization Server Wizard, or alternatively, right-click the **Publishing Server** node and select **New Server** from the pop-up-menu.</span></span>

2.  <span data-ttu-id="3fd6c-107">Na página um do assistente, insira o nome do servidor no campo nome para **exibição** e selecione o tipo de servidor na lista suspensa **tipo** .</span><span class="sxs-lookup"><span data-stu-id="3fd6c-107">On page one of the wizard, enter the name of the server in the **Display Name** field and select the server type from the **Type** drop-down list.</span></span> <span data-ttu-id="3fd6c-108">Você pode escolher o servidor de **virtualização de aplicativos**, o **servidor de virtualização de aplicativo de segurança avançada**, o **servidor HTTP padrão**ou o **servidor http de segurança avançada** na lista suspensa de tipos de servidor.</span><span class="sxs-lookup"><span data-stu-id="3fd6c-108">You can choose **Application Virtualization Server**, **Enhanced Security Application Virtualization Server**, **Standard HTTP Server**, or **Enhanced Security HTTP Server** from the drop-down list of server types.</span></span>

3.  <span data-ttu-id="3fd6c-109">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="3fd6c-109">Click **Next**.</span></span>

4.  <span data-ttu-id="3fd6c-110">Na página 2 do assistente, digite as informações apropriadas nos campos **nome do host** e **porta** .</span><span class="sxs-lookup"><span data-stu-id="3fd6c-110">On page two of the wizard, type the appropriate information into the **Host Name** and **Port** fields.</span></span> <span data-ttu-id="3fd6c-111">O campo **caminho** não é editável para servidores do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="3fd6c-111">The **Path** field is not editable for Application Virtualization Servers.</span></span> <span data-ttu-id="3fd6c-112">Você deve digitar um caminho para o servidor HTTP padrão ou o servidor HTTP de segurança avançada.</span><span class="sxs-lookup"><span data-stu-id="3fd6c-112">You must enter a path for Standard HTTP Server or Enhanced Security HTTP Server.</span></span>

5.  <span data-ttu-id="3fd6c-113">Clique em **concluir** para adicionar o servidor.</span><span class="sxs-lookup"><span data-stu-id="3fd6c-113">Click **Finish** to add the server.</span></span>

**<span data-ttu-id="3fd6c-114">Para configurar um servidor de publicação de aplicativos</span><span class="sxs-lookup"><span data-stu-id="3fd6c-114">To set up an application publishing server</span></span>**

1.  <span data-ttu-id="3fd6c-115">No painel de **resultados** , clique com o botão direito do mouse no servidor desejado e selecione **Propriedades** no menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="3fd6c-115">In the **Results** pane, right-click the desired server and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="3fd6c-116">Clique na guia **geral** , na qual você pode alterar o nome do servidor, selecione um tipo na lista suspensa de tipos de servidor e especifique o nome e a porta do host.</span><span class="sxs-lookup"><span data-stu-id="3fd6c-116">Click the **General** tab, where you can change the server name, select a type from the drop-down list of server types, and specify the host name and port.</span></span> <span data-ttu-id="3fd6c-117">Quando o tipo de servidor é um servidor HTTP padrão ou um servidor HTTP de segurança avançada, o campo **caminho** também é editável.</span><span class="sxs-lookup"><span data-stu-id="3fd6c-117">When the server type is Standard HTTP Server or Enhanced Security HTTP Server, the **Path** field is also editable.</span></span>

3.  <span data-ttu-id="3fd6c-118">Clique na guia **Atualizar** , na qual a caixa de seleção **Atualizar publicação no logon do usuário** está marcada por padrão.</span><span class="sxs-lookup"><span data-stu-id="3fd6c-118">Click the **Refresh** tab, where the **Refresh publishing on user login** check box is selected by default.</span></span> <span data-ttu-id="3fd6c-119">Para alterar a taxa de atualização, marque a caixa de seleção **atualizar a publicação a cada** e insira um número que represente a frequência no campo.</span><span class="sxs-lookup"><span data-stu-id="3fd6c-119">To change the refresh rate, select the **Refresh publishing every** check box and enter a number that represents the frequency in the field.</span></span> <span data-ttu-id="3fd6c-120">Em seguida, selecione **minutos**, **horas**, **dias** no menu suspenso.</span><span class="sxs-lookup"><span data-stu-id="3fd6c-120">Then select **Minutes**, **Hours**, **Days** from the drop-down menu.</span></span> <span data-ttu-id="3fd6c-121">(A quantidade mínima de tempo que você pode inserir é de 30 minutos.)</span><span class="sxs-lookup"><span data-stu-id="3fd6c-121">(The minimum amount of time you can enter is 30 minutes.)</span></span>

4.  <span data-ttu-id="3fd6c-122">Clique em **aplicar** para alterar a configuração.</span><span class="sxs-lookup"><span data-stu-id="3fd6c-122">Click **Apply** to change the configuration.</span></span>

5.  <span data-ttu-id="3fd6c-123">Quando terminar de publicar, clique em **OK** para sair da caixa de diálogo e retornar ao console de gerenciamento de cliente.</span><span class="sxs-lookup"><span data-stu-id="3fd6c-123">When you are finished publishing, click **OK** to exit the dialog box and return to the Client Management Console.</span></span>

## <span data-ttu-id="3fd6c-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3fd6c-124">Related topics</span></span>


[<span data-ttu-id="3fd6c-125">Como desabilitar ou Modificar as configurações de Modo de Operação Desconectada</span><span class="sxs-lookup"><span data-stu-id="3fd6c-125">How to Disable or Modify Disconnected Operation Mode Settings</span></span>](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 





