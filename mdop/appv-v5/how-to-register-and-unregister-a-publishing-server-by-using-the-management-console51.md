---
title: Como registrar e cancelar o registro de um servidor publicação usando o Console de Gerenciamento
description: Como registrar e cancelar o registro de um servidor publicação usando o Console de Gerenciamento
author: dansimp
ms.assetid: 69cef0a8-8102-4697-b1ba-f16e0f25216b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b63922ff03ea19326e395e57236fcd079711bd43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796329"
---
# <span data-ttu-id="9fed5-103">Como registrar e cancelar o registro de um servidor publicação usando o Console de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="9fed5-103">How to Register and Unregister a Publishing Server by Using the Management Console</span></span>


<span data-ttu-id="9fed5-104">Você pode registrar e cancelar o registro de servidores de publicação que serão sincronizados com o servidor de gerenciamento do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="9fed5-104">You can register and unregister publishing servers that will synchronize with the App-V 5.1 management server.</span></span> <span data-ttu-id="9fed5-105">Você também pode ver a última tentativa que o servidor de publicação fez para sincronizar as informações com o servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="9fed5-105">You can also see the last attempt that the publishing server made to synchronize the information with the management server.</span></span>

<span data-ttu-id="9fed5-106">Use o procedimento a seguir para registrar ou cancelar o registro de um servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="9fed5-106">Use the following procedure to register or unregister a publishing server.</span></span>

**<span data-ttu-id="9fed5-107">Para registrar um servidor de publicação usando o console de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="9fed5-107">To register a publishing server using the Management Console</span></span>**

1.  <span data-ttu-id="9fed5-108">Conecte-se ao console de gerenciamento e selecione **servidores**.</span><span class="sxs-lookup"><span data-stu-id="9fed5-108">Connect to the Management Console and select **Servers**.</span></span> <span data-ttu-id="9fed5-109">Para obter mais informações sobre como se conectar ao console de gerenciamento, consulte [como se conectar ao console de gerenciamento](how-to-connect-to-the-management-console-51.md).</span><span class="sxs-lookup"><span data-stu-id="9fed5-109">For more information about how to connect to the Management Console, see [How to Connect to the Management Console](how-to-connect-to-the-management-console-51.md).</span></span>

2.  <span data-ttu-id="9fed5-110">Uma lista de servidores de publicação que já sincronizamos com o servidor de gerenciamento é exibida.</span><span class="sxs-lookup"><span data-stu-id="9fed5-110">A list of publishing servers that already synchronize with the management server is displayed.</span></span> <span data-ttu-id="9fed5-111">Clique em registrar novo servidor para registrar um novo servidor.</span><span class="sxs-lookup"><span data-stu-id="9fed5-111">Click Register New Server to register a new server.</span></span>

3.  <span data-ttu-id="9fed5-112">Digite um nome de computador de um computador associado a um domínio na linha **nome do servidor** para especificar um nome para o servidor.</span><span class="sxs-lookup"><span data-stu-id="9fed5-112">Type a computer name of a domain joined computer on the **Server Name** line, to specify a name for the server.</span></span> <span data-ttu-id="9fed5-113">Você também deve incluir um nome de domínio, por exemplo, **MyDomain\\TestServer**.</span><span class="sxs-lookup"><span data-stu-id="9fed5-113">You should also include a domain name, for example, **MyDomain\\TestServer**.</span></span> <span data-ttu-id="9fed5-114">Clique em **verificar**.</span><span class="sxs-lookup"><span data-stu-id="9fed5-114">Click **Check**.</span></span>

4.  <span data-ttu-id="9fed5-115">Selecione o computador e clique em **Adicionar** para adicionar o computador à lista de servidores.</span><span class="sxs-lookup"><span data-stu-id="9fed5-115">Select the computer and click **Add** to add the computer to the list of servers.</span></span> <span data-ttu-id="9fed5-116">O novo servidor será exibido na lista.</span><span class="sxs-lookup"><span data-stu-id="9fed5-116">The new server will be displayed in the list.</span></span>

**<span data-ttu-id="9fed5-117">Para cancelar o registro de um servidor de publicação usando o console de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="9fed5-117">To unregister a publishing server using the Management Console</span></span>**

1.  <span data-ttu-id="9fed5-118">Conecte-se ao console de gerenciamento e selecione **servidores**.</span><span class="sxs-lookup"><span data-stu-id="9fed5-118">Connect to the Management Console and select **Servers**.</span></span> <span data-ttu-id="9fed5-119">Para obter mais informações sobre como se conectar ao console de gerenciamento, consulte [como se conectar ao console de gerenciamento](how-to-connect-to-the-management-console-51.md).</span><span class="sxs-lookup"><span data-stu-id="9fed5-119">For more information about how to connect to the Management Console, see [How to Connect to the Management Console](how-to-connect-to-the-management-console-51.md).</span></span>

2.  <span data-ttu-id="9fed5-120">Será exibida uma lista de servidores de publicação que são sincronizados com o servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="9fed5-120">A list of publishing servers that synchronize with the management server is displayed.</span></span>

3.  <span data-ttu-id="9fed5-121">Para cancelar o registro do servidor, clique com o botão direito do mouse no nome do computador e selecione o nome do computador e selecione **Cancelar registro do servidor**.</span><span class="sxs-lookup"><span data-stu-id="9fed5-121">To unregister the server, right-click the computer name and select the computer name and select **unregister server**.</span></span>

    <span data-ttu-id="9fed5-122">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="9fed5-122">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="9fed5-123">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="9fed5-123">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="9fed5-124">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="9fed5-124">Got an App-V issue?</span></span>** <span data-ttu-id="9fed5-125">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="9fed5-125">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="9fed5-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9fed5-126">Related topics</span></span>


[<span data-ttu-id="9fed5-127">Operações para o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="9fed5-127">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





