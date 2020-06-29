---
title: Como instalar o servidor de gerenciamento em um computador autônomo e conectá-lo ao banco de dados
description: Como instalar o servidor de gerenciamento em um computador autônomo e conectá-lo ao banco de dados
author: dansimp
ms.assetid: 95281287-cb56-4117-befd-854268ea147c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 86f384e88b85101855287bb428e75376f7974219
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796397"
---
# <span data-ttu-id="01a01-103">Como instalar o servidor de gerenciamento em um computador autônomo e conectá-lo ao banco de dados</span><span class="sxs-lookup"><span data-stu-id="01a01-103">How to install the Management Server on a Standalone Computer and Connect it to the Database</span></span>


<span data-ttu-id="01a01-104">Use o procedimento a seguir para instalar o servidor de gerenciamento em um computador autônomo e conectá-lo ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="01a01-104">Use the following procedure to install the management server on a standalone computer and connect it to the database.</span></span>

**<span data-ttu-id="01a01-105">Para instalar o servidor de gerenciamento em um computador autônomo e conectá-lo ao banco de dados</span><span class="sxs-lookup"><span data-stu-id="01a01-105">To install the management server on a standalone computer and connect it to the database</span></span>**

1.  <span data-ttu-id="01a01-106">Copie os arquivos de instalação do App-V 5,0 Server para o computador no qual você deseja instalá-lo.</span><span class="sxs-lookup"><span data-stu-id="01a01-106">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="01a01-107">Para iniciar a instalação do App-V 5,0 Server, clique com o botão direito do mouse e execute **appv\_server\_setup.exe** como administrador.</span><span class="sxs-lookup"><span data-stu-id="01a01-107">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="01a01-108">Clique em **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="01a01-108">Click **Install**.</span></span>

2.  <span data-ttu-id="01a01-109">Na página de **introdução** , examine e aceite os termos de licença e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="01a01-109">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="01a01-110">Na página **usar o Microsoft Update para ajudar a manter seu computador seguro e atualizado** , para habilitar as atualizações da Microsoft, selecione **usar o Microsoft Update quando eu verificar se há atualizações (recomendado).**</span><span class="sxs-lookup"><span data-stu-id="01a01-110">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="01a01-111">Para desabilitar o Microsoft Updates, selecione **não quero usar o Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="01a01-111">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="01a01-112">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="01a01-112">Click **Next**.</span></span>

4.  <span data-ttu-id="01a01-113">Na página **seleção de recursos** , marque a caixa de seleção **servidor de gerenciamento** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="01a01-113">On the **Feature Selection** page, select the **Management Server** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="01a01-114">Na página **local de instalação** , aceite o local padrão e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="01a01-114">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="01a01-115">Na página **configurar banco de dados de gerenciamento existente** , selecione **usar um SQL Server remoto**e digite o nome do computador que executa o Microsoft SQL SQL, por exemplo, **SqlServerMachine**.</span><span class="sxs-lookup"><span data-stu-id="01a01-115">On the **Configure Existing Management Database** page, select **Use a remote SQL Server**, and type the machine name of the computer running Microsoft SQL SQL, for example **SqlServerMachine**.</span></span>

    **<span data-ttu-id="01a01-116">Observação</span><span class="sxs-lookup"><span data-stu-id="01a01-116">Note</span></span>**  
    <span data-ttu-id="01a01-117">Se o Microsoft SQL Server estiver implantado no mesmo servidor, selecione **usar SQL Server local**.</span><span class="sxs-lookup"><span data-stu-id="01a01-117">If the Microsoft SQL Server is deployed on the same server, select **Use local SQL Server**.</span></span>



~~~
For the SQL Server Instance, select **Use the default instance**. If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.

Specify the **SQL Server Database name** that this management server will use, for example **AppvManagement**.
~~~

7. <span data-ttu-id="01a01-118">Na página **configurar configuração do servidor de gerenciamento** , especifique o grupo de anúncios ou a conta que será conectada ao console de gerenciamento para fins administrativos, por exemplo, **MyDomain\\MyUser** ou **MyDomain\\AdminGroup**.</span><span class="sxs-lookup"><span data-stu-id="01a01-118">On the **Configure Management Server Configuration** page, specify the AD group or account that will connect to the management console for administrative purposes for example **MyDomain\\MyUser** or **MyDomain\\AdminGroup**.</span></span> <span data-ttu-id="01a01-119">A conta ou o grupo do AD especificado será habilitado para gerenciar o servidor por meio do console de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="01a01-119">The account or AD group you specify will be enabled to manage the server through the management console.</span></span> <span data-ttu-id="01a01-120">Você pode adicionar mais usuários ou grupos usando o console de gerenciamento após a instalação</span><span class="sxs-lookup"><span data-stu-id="01a01-120">You can add additional users or groups using the management console after installation</span></span>

   <span data-ttu-id="01a01-121">Especifique o **nome do site** que você deseja usar para o serviço de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="01a01-121">Specify the **Website Name** that you want to use for the management service.</span></span> <span data-ttu-id="01a01-122">Aceite o padrão se você não tiver um nome personalizado.</span><span class="sxs-lookup"><span data-stu-id="01a01-122">Accept the default if you do not have a custom name.</span></span> <span data-ttu-id="01a01-123">Para a **Associação de portabilidade**, especifique um número de porta exclusivo a ser usado, por exemplo, **12345**.</span><span class="sxs-lookup"><span data-stu-id="01a01-123">For the **Port Binding**, specify a unique port number to be used, for example **12345**.</span></span>

8. <span data-ttu-id="01a01-124">Clique em **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="01a01-124">Click **Install**.</span></span>

9. <span data-ttu-id="01a01-125">Para confirmar se a configuração foi concluída com êxito, abra um navegador da Web e digite a seguinte URL: http://managementserver:portnumber/Console.html se a instalação tiver sido bem-sucedida, você verá o **console de gerenciamento do Silverlight** aparecerá sem mensagens de erro ou avisos sendo exibidos.</span><span class="sxs-lookup"><span data-stu-id="01a01-125">To confirm that the setup has completed successfully, open a web browser, and type the following URL: http://managementserver:portnumber/Console.html if the installation was successful you should see the **Silverlight Management Console** appear without any error messages or warnings being displayed.</span></span>

   <span data-ttu-id="01a01-126">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="01a01-126">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="01a01-127">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="01a01-127">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="01a01-128">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="01a01-128">Got an App-V issue?</span></span>** <span data-ttu-id="01a01-129">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="01a01-129">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="01a01-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01a01-130">Related topics</span></span>


[<span data-ttu-id="01a01-131">Implantação do App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="01a01-131">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)









