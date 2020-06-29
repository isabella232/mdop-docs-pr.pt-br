---
title: Como configurar atualização periódica de publicação
description: Como configurar atualização periódica de publicação
author: dansimp
ms.assetid: c358c765-cb88-4881-b4e7-0a2e87304870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5bbea1c661d6cb5a78f0bb9de29538e0222cda6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796948"
---
# <span data-ttu-id="97ad4-103">Como configurar atualização periódica de publicação</span><span class="sxs-lookup"><span data-stu-id="97ad4-103">How to Set Up Periodic Publishing Refresh</span></span>


<span data-ttu-id="97ad4-104">Você pode usar o procedimento a seguir para configurar o cliente para atualizar periodicamente as informações de publicação dos servidores App-V.</span><span class="sxs-lookup"><span data-stu-id="97ad4-104">You can use the following procedure to configure the client to periodically refresh the publishing information from the App-V servers.</span></span> <span data-ttu-id="97ad4-105">Após a configuração do cliente, a operação de atualização é automática.</span><span class="sxs-lookup"><span data-stu-id="97ad4-105">After the client is configured, the refresh operation is automatic.</span></span> <span data-ttu-id="97ad4-106">Essas configurações definem as configurações padrão do cliente para que todos os usuários deste computador vejam as mesmas configurações.</span><span class="sxs-lookup"><span data-stu-id="97ad4-106">These settings configure the default settings for the client so that all users on this computer will see the same settings.</span></span>

<span data-ttu-id="97ad4-107">**Observação**  Depois que você executar esse procedimento, as informações de publicação serão atualizadas de acordo com as novas configurações após a primeira atualização ao fazer logon.</span><span class="sxs-lookup"><span data-stu-id="97ad4-107">**Note** After you have performed this procedure, the publishing information will be refreshed according to the new settings after the first refresh at login.</span></span> <span data-ttu-id="97ad4-108">Quando essa primeira atualização ocorre, o servidor pode substituir as configurações do computador por configurações diferentes, dependendo de como ela está configurada.</span><span class="sxs-lookup"><span data-stu-id="97ad4-108">When this first refresh occurs, the server might override the computer settings with different settings, depending on how it is configured.</span></span> <span data-ttu-id="97ad4-109">A guia **Atualizar** na caixa de diálogo **Propriedades** mostra as configurações do computador cliente configurado localmente e as configurações que podem ter sido configuradas para o usuário pelo servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="97ad4-109">The **Refresh** tab in the **Properties** dialog box shows the locally configured client computer settings and any settings that might have been configured for the user by the publishing server.</span></span>

 

**<span data-ttu-id="97ad4-110">Para atualizar periodicamente as informações de publicação dos servidores de virtualização de aplicativos</span><span class="sxs-lookup"><span data-stu-id="97ad4-110">To periodically refresh the publishing information from the Application Virtualization Servers</span></span>**

1.  <span data-ttu-id="97ad4-111">Clique em **servidores de publicação** no painel **escopo** .</span><span class="sxs-lookup"><span data-stu-id="97ad4-111">Click **Publishing Servers** in the **Scope** pane.</span></span>

2.  <span data-ttu-id="97ad4-112">No painel de **resultados** , clique com o botão direito do mouse no servidor desejado e selecione **Propriedades** no menu pop-up-.</span><span class="sxs-lookup"><span data-stu-id="97ad4-112">In the **Results** pane, right-click the desired server and select **Properties** from the pop-up-menu.</span></span>

3.  <span data-ttu-id="97ad4-113">Na caixa de diálogo **Propriedades** , na guia **Atualizar** , marque a caixa de seleção **Atualizar configuração a cada** e insira um número que represente a frequência no campo.</span><span class="sxs-lookup"><span data-stu-id="97ad4-113">In the **Properties** dialog box, on the **Refresh** tab, select the **Refresh configuration every** check box and enter a number that represents the frequency in the field.</span></span> <span data-ttu-id="97ad4-114">Em seguida, selecione **minutos**, **horas**, **dias** no menu suspenso.</span><span class="sxs-lookup"><span data-stu-id="97ad4-114">Then select **Minutes**, **Hours**, **Days** from the drop-down menu.</span></span>

    <span data-ttu-id="97ad4-115">**Observação**  Essa configuração fará com que o cliente atualize as informações de publicação toda vez que o período configurado for ultrapassado.</span><span class="sxs-lookup"><span data-stu-id="97ad4-115">**Note** This setting will cause the client to refresh publishing information every time the configured period elapses.</span></span> <span data-ttu-id="97ad4-116">Se o usuário não estiver conectado quando for hora de fazer uma atualização, a atualização ocorrerá quando o usuário fizer logon.</span><span class="sxs-lookup"><span data-stu-id="97ad4-116">If the user is not logged in when it's time to do a refresh, the refresh will take place when the user next logs in.</span></span> <span data-ttu-id="97ad4-117">Em seguida, o temporizador é iniciado novamente para o próximo período.</span><span class="sxs-lookup"><span data-stu-id="97ad4-117">The timer is then started again for the next period.</span></span>

     

4.  <span data-ttu-id="97ad4-118">Clique em **aplicar** para alterar a configuração.</span><span class="sxs-lookup"><span data-stu-id="97ad4-118">Click **Apply** to change the configuration.</span></span>

5.  <span data-ttu-id="97ad4-119">Quando terminar de configurar o servidor, clique em **OK** para sair da caixa de diálogo e retornar ao console de gerenciamento de cliente do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="97ad4-119">When you finish configuring the server, click **OK** to exit the dialog box and return to the Application Virtualization Client Management Console.</span></span>

## <span data-ttu-id="97ad4-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="97ad4-120">Related topics</span></span>


[<span data-ttu-id="97ad4-121">Como configurar o Application Virtualization Client Management Console</span><span class="sxs-lookup"><span data-stu-id="97ad4-121">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

 

 





