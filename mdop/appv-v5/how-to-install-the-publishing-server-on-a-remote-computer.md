---
title: Como instalar o servidor de publicação em um computador remoto
description: Como instalar o servidor de publicação em um computador remoto
author: dansimp
ms.assetid: 37970706-54ff-4799-9485-b9b49fd50f37
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d711fa51ade856b3ac5880ba60a19315c358734
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796389"
---
# <span data-ttu-id="6f574-103">Como instalar o servidor de publicação em um computador remoto</span><span class="sxs-lookup"><span data-stu-id="6f574-103">How to Install the Publishing Server on a Remote Computer</span></span>


<span data-ttu-id="6f574-104">Use o procedimento a seguir para instalar o Publishing Server em um computador separado.</span><span class="sxs-lookup"><span data-stu-id="6f574-104">Use the following procedure to install the publishing server on a separate computer.</span></span> <span data-ttu-id="6f574-105">Antes de executar o procedimento a seguir, verifique se o banco de dados e o servidor de gerenciamento estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6f574-105">Before you perform the following procedure, ensure the database and management server are available.</span></span>

**<span data-ttu-id="6f574-106">Para instalar o Publishing Server em um computador separado</span><span class="sxs-lookup"><span data-stu-id="6f574-106">To install the publishing server on a separate computer</span></span>**

1. <span data-ttu-id="6f574-107">Copie os arquivos de instalação do App-V 5,0 Server para o computador no qual você deseja instalá-lo.</span><span class="sxs-lookup"><span data-stu-id="6f574-107">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="6f574-108">Para iniciar a instalação do App-V 5,0 Server, clique com o botão direito do mouse e execute **appv\_server\_setup.exe** como administrador.</span><span class="sxs-lookup"><span data-stu-id="6f574-108">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="6f574-109">Clique em **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="6f574-109">Click **Install**.</span></span>

2. <span data-ttu-id="6f574-110">Na página de **introdução** , examine e aceite os termos de licença e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="6f574-110">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3. <span data-ttu-id="6f574-111">Na página **usar o Microsoft Update para ajudar a manter seu computador seguro e atualizado** , para habilitar as atualizações da Microsoft, selecione **usar o Microsoft Update quando eu verificar se há atualizações (recomendado).**</span><span class="sxs-lookup"><span data-stu-id="6f574-111">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="6f574-112">Para desabilitar o Microsoft Updates, selecione **não quero usar o Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="6f574-112">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="6f574-113">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="6f574-113">Click **Next**.</span></span>

4. <span data-ttu-id="6f574-114">Na página **seleção de recursos** , marque a caixa de seleção **servidor de publicação** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="6f574-114">On the **Feature Selection** page, select the **Publishing Server** checkbox and click **Next**.</span></span>

5. <span data-ttu-id="6f574-115">Na página **local de instalação** , aceite o local padrão e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="6f574-115">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6. <span data-ttu-id="6f574-116">Na página **Configurar o Publishing Server Configuration** , especifique os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="6f574-116">On the **Configure Publishing Server Configuration** page, specify the following items:</span></span>

   -   <span data-ttu-id="6f574-117">A URL para o serviço de gerenciamento ao qual o servidor de publicação será conectado.</span><span class="sxs-lookup"><span data-stu-id="6f574-117">The URL for the management service that the publishing server will connect to.</span></span> <span data-ttu-id="6f574-118">Por exemplo, **http://ManagementServerName:12345** .</span><span class="sxs-lookup"><span data-stu-id="6f574-118">For example, **http://ManagementServerName:12345**.</span></span>

   -   <span data-ttu-id="6f574-119">Especifique o nome do site que você deseja usar para o serviço de publicação.</span><span class="sxs-lookup"><span data-stu-id="6f574-119">Specify the website name that you want to use for the publishing service.</span></span> <span data-ttu-id="6f574-120">Aceite o padrão se você não tiver um nome personalizado.</span><span class="sxs-lookup"><span data-stu-id="6f574-120">Accept the default if you do not have a custom name.</span></span>

   -   <span data-ttu-id="6f574-121">Para a **Associação de portabilidade**, especifique um número de porta exclusivo que será usado pelo App-V 5,0, por exemplo, **54321**.</span><span class="sxs-lookup"><span data-stu-id="6f574-121">For the **Port Binding**, specify a unique port number that will be used by App-V 5.0, for example **54321**.</span></span>

7. <span data-ttu-id="6f574-122">Na página **pronto para instalar** , clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="6f574-122">On the **Ready to Install** page, click **Install**.</span></span>

8. <span data-ttu-id="6f574-123">Após a conclusão da instalação, o servidor de publicação deve ser registrado com o servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="6f574-123">After the installation is complete, the publishing server must be registered with the management server.</span></span> <span data-ttu-id="6f574-124">No console de gerenciamento do App-V 5,0, use as etapas a seguir para registrar o servidor:</span><span class="sxs-lookup"><span data-stu-id="6f574-124">In the App-V 5.0 management console, use the following steps to register the server:</span></span>

   1.  <span data-ttu-id="6f574-125">Abra o console do servidor de gerenciamento do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6f574-125">Open the App-V 5.0 management server console.</span></span>

   2.  <span data-ttu-id="6f574-126">No painel esquerdo, selecione **servidores**e, em seguida, selecione **registrar novo servidor**.</span><span class="sxs-lookup"><span data-stu-id="6f574-126">In the left pane, select **Servers**, and then select **Register New Server**.</span></span>

   3.  <span data-ttu-id="6f574-127">Digite o nome do servidor e uma descrição (se necessário) e clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="6f574-127">Type the name of this server and a description (if required) and click **Add**.</span></span>

9. <span data-ttu-id="6f574-128">Para verificar se o servidor de publicação está funcionando corretamente, você deve importar um pacote para o servidor de gerenciamento, entitle o pacote a um grupo de anúncios e publicar o pacote.</span><span class="sxs-lookup"><span data-stu-id="6f574-128">To verify if the publishing server is running correctly, you should import a package to the management server, entitle the package to an AD group, and publish the package.</span></span> <span data-ttu-id="6f574-129">Usando um navegador da Internet, abra a seguinte URL: <strong> http://publishingserver:pubport </strong> .</span><span class="sxs-lookup"><span data-stu-id="6f574-129">Using an internet browser, open the following URL: <strong>http://publishingserver:pubport</strong>.</span></span> <span data-ttu-id="6f574-130">Se o servidor estiver executando corretamente, as informações semelhantes às seguintes serão exibidas:</span><span class="sxs-lookup"><span data-stu-id="6f574-130">If the server is running correctly information similar to the following will be displayed:</span></span>

   ```xml
   <Publishing Protocol="1.0">
     <Packages>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" VersionId="5d03c08f-51dc-4026-8cf9-15ebe3d65a72" PackageUrl="\\server\share\file.appv" />
     </Packages>
     <NoGroup>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" />
     </NoGroup>
   </Publishing>
   ```

   <span data-ttu-id="6f574-131">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="6f574-131">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="6f574-132">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="6f574-132">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="6f574-133">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="6f574-133">Got an App-V issue?</span></span>** <span data-ttu-id="6f574-134">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="6f574-134">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="6f574-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6f574-135">Related topics</span></span>


[<span data-ttu-id="6f574-136">Implantação do App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="6f574-136">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

 

 





