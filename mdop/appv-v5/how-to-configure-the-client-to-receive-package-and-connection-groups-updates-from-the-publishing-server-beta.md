---
title: Como configurar o cliente para receber atualizações de pacotes e grupos de conexão do servidor de publicação
description: Como configurar o cliente para receber atualizações de pacotes e grupos de conexão do servidor de publicação
author: dansimp
ms.assetid: f5dfd96d-4b63-468c-8d93-9dfdf47c28fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e9df1f8b324430449d8d1dd3624d9f1157968a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796487"
---
# <span data-ttu-id="9306a-103">Como configurar o cliente para receber atualizações de pacotes e grupos de conexão do servidor de publicação</span><span class="sxs-lookup"><span data-stu-id="9306a-103">How to Configure the Client to Receive Package and Connection Groups Updates From the Publishing Server</span></span>


<span data-ttu-id="9306a-104">Implantar pacotes e grupos de conexão usando o servidor de publicação App-V 5,0 é útil porque oferece gerenciamento de ponto único e alta escalabilidade.</span><span class="sxs-lookup"><span data-stu-id="9306a-104">Deploying packages and connection groups using the App-V 5.0 publishing server is helpful because it offers single-point management and high scalability.</span></span>

<span data-ttu-id="9306a-105">Use as etapas a seguir para configurar o cliente App-V 5,0 para receber atualizações do servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="9306a-105">Use the following steps to configure the App-V 5.0 client to receive updates from the publishing server.</span></span>

<span data-ttu-id="9306a-106">**Observação**  Para os procedimentos a seguir, o servidor de gerenciamento foi instalado em um computador chamado **MyMgmtSrv**, e o servidor de publicação foi instalado em um computador chamado **MyPubSrv**.</span><span class="sxs-lookup"><span data-stu-id="9306a-106">**Note** For the following procedures the management server was installed on a computer named **MyMgmtSrv**, and the publishing server was installed on a computer named **MyPubSrv**.</span></span>

 

**<span data-ttu-id="9306a-107">Para configurar o cliente do App-V 5,0 para receber atualizações do servidor de publicação</span><span class="sxs-lookup"><span data-stu-id="9306a-107">To configure the App-V 5.0 client to receive updates from the publishing server</span></span>**

1.  <span data-ttu-id="9306a-108">Implante os servidores de gerenciamento do App-V 5,0 e de publicação e adicione os pacotes e os grupos de conexão necessários.</span><span class="sxs-lookup"><span data-stu-id="9306a-108">Deploy the App-V 5.0 management and publishing servers, and add the required packages and connection groups.</span></span> <span data-ttu-id="9306a-109">Para obter mais informações sobre como adicionar pacotes e grupos de conexão, consulte [como adicionar ou atualizar pacotes usando o console de gerenciamento](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) e [como criar um grupo de conexão](how-to-create-a-connection-group.md).</span><span class="sxs-lookup"><span data-stu-id="9306a-109">For more information about adding packages and connection groups, see [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) and [How to Create a Connection Group](how-to-create-a-connection-group.md).</span></span>

2.  <span data-ttu-id="9306a-110">Para abrir o console de gerenciamento, clique no link a seguir, abra um navegador e digite o seguinte: http://MyMgmtSrv/AppvManagement/Console.html em um navegador da Web e importe, publique e entitle todos os pacotes e grupos de conexão que serão necessários para um conjunto específico de usuários.</span><span class="sxs-lookup"><span data-stu-id="9306a-110">To open the management console click the following link, open a browser and type the following: http://MyMgmtSrv/AppvManagement/Console.html in a web browser, and import, publish, and entitle all the packages and connection groups which will be necessary for a particular set of users.</span></span>

3.  <span data-ttu-id="9306a-111">No computador que executa o cliente App-V 5,0, abra um prompt de comando elevado do PowerShell, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="9306a-111">On the computer running the App-V 5.0 client, open an elevated PowerShell command prompt, run the following command:</span></span>

    **<span data-ttu-id="9306a-112">Add-AppvPublishingServer-Name ABC-URL http://MyPubSrv/AppvPublishing</span><span class="sxs-lookup"><span data-stu-id="9306a-112">Add-AppvPublishingServer -Name ABC -URL http:// MyPubSrv/AppvPublishing</span></span>**

    <span data-ttu-id="9306a-113">Esse comando irá configurar o servidor de publicação especificado.</span><span class="sxs-lookup"><span data-stu-id="9306a-113">This command will configure the specified publishing server.</span></span> <span data-ttu-id="9306a-114">Você deve ver uma saída semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="9306a-114">You should see output similar to the following:</span></span>

    <span data-ttu-id="9306a-115">ID: 1</span><span class="sxs-lookup"><span data-stu-id="9306a-115">Id : 1</span></span>

    <span data-ttu-id="9306a-116">SetByGroupPolicy: false</span><span class="sxs-lookup"><span data-stu-id="9306a-116">SetByGroupPolicy : False</span></span>

    <span data-ttu-id="9306a-117">Nome: ABC</span><span class="sxs-lookup"><span data-stu-id="9306a-117">Name : ABC</span></span>

    <span data-ttu-id="9306a-118">URL: http://MyPubSrv/AppvPublishing</span><span class="sxs-lookup"><span data-stu-id="9306a-118">URL : http:// MyPubSrv/AppvPublishing</span></span>

    <span data-ttu-id="9306a-119">GlobalRefreshEnabled: false</span><span class="sxs-lookup"><span data-stu-id="9306a-119">GlobalRefreshEnabled : False</span></span>

    <span data-ttu-id="9306a-120">GlobalRefreshOnLogon: false</span><span class="sxs-lookup"><span data-stu-id="9306a-120">GlobalRefreshOnLogon : False</span></span>

    <span data-ttu-id="9306a-121">GlobalRefreshInterval: 0</span><span class="sxs-lookup"><span data-stu-id="9306a-121">GlobalRefreshInterval : 0</span></span>

    <span data-ttu-id="9306a-122">GlobalRefreshIntervalUnit: dia</span><span class="sxs-lookup"><span data-stu-id="9306a-122">GlobalRefreshIntervalUnit : Day</span></span>

    <span data-ttu-id="9306a-123">UserRefreshEnabled: true</span><span class="sxs-lookup"><span data-stu-id="9306a-123">UserRefreshEnabled : True</span></span>

    <span data-ttu-id="9306a-124">UserRefreshOnLogon: true</span><span class="sxs-lookup"><span data-stu-id="9306a-124">UserRefreshOnLogon : True</span></span>

    <span data-ttu-id="9306a-125">UserRefreshInterval: 0</span><span class="sxs-lookup"><span data-stu-id="9306a-125">UserRefreshInterval : 0</span></span>

    <span data-ttu-id="9306a-126">UserRefreshIntervalUnit: dia</span><span class="sxs-lookup"><span data-stu-id="9306a-126">UserRefreshIntervalUnit : Day</span></span>

    <span data-ttu-id="9306a-127">A ID retornada – nesse caso 1</span><span class="sxs-lookup"><span data-stu-id="9306a-127">The returned Id – in this case 1</span></span>

4.  <span data-ttu-id="9306a-128">No computador que executa o cliente App-V 5,0, abra um prompt de comando do PowerShell e digite o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="9306a-128">On the computer running the App-V 5.0 client, open a PowerShell command prompt, and type the following command:</span></span>

    **<span data-ttu-id="9306a-129">Sync-AppvPublishingServer-serverID 1</span><span class="sxs-lookup"><span data-stu-id="9306a-129">Sync-AppvPublishingServer -ServerId 1</span></span>**

    <span data-ttu-id="9306a-130">O comando consultará o servidor de publicação para os pacotes e grupos de conexão que precisam ser adicionados ou removidos para esse cliente específico com base nos direitos dos pacotes e grupos de conexão conforme configurados no servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="9306a-130">The command will query the publishing server for the packages and connection groups that need to be added or removed for this particular client based on the entitlements for the packages and connection groups as configured on the management server.</span></span>

    <span data-ttu-id="9306a-131">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="9306a-131">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="9306a-132">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="9306a-132">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="9306a-133">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="9306a-133">Got an App-V issue?</span></span>** <span data-ttu-id="9306a-134">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="9306a-134">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="9306a-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9306a-135">Related topics</span></span>


[<span data-ttu-id="9306a-136">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="9306a-136">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





