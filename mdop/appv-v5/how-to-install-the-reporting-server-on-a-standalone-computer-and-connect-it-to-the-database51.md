---
title: Como instalar o servidor de relatórios em um computador autônomo e conectá-lo ao banco de dados
description: Como instalar o servidor de relatórios em um computador autônomo e conectá-lo ao banco de dados
author: dansimp
ms.assetid: 11f07750-4045-4c8d-a583-7d70c9e9aa7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67866714ff6ae60097d9b368fd0eaf361b08eec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796383"
---
# <span data-ttu-id="c02be-103">Como instalar o servidor de relatórios em um computador autônomo e conectá-lo ao banco de dados</span><span class="sxs-lookup"><span data-stu-id="c02be-103">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>

<span data-ttu-id="c02be-104">Use o procedimento a seguir para instalar o servidor de relatório em um computador autônomo e conectá-lo ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c02be-104">Use the following procedure to install the reporting server on a standalone computer and connect it to the database.</span></span>

<span data-ttu-id="c02be-105">**Importante** Antes de executar o procedimento a seguir, você deve ler e entender [sobre relatórios do App-V 5,1](about-app-v-51-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="c02be-105">**Important** Before performing the following procedure you should read and understand [About App-V 5.1 Reporting](about-app-v-51-reporting.md).</span></span>

## <span data-ttu-id="c02be-106">Para instalar o servidor de relatórios em um computador autônomo e conectá-lo ao banco de dados</span><span class="sxs-lookup"><span data-stu-id="c02be-106">To install the reporting server on a standalone computer and connect it to the database</span></span>

1. <span data-ttu-id="c02be-107">Copie os arquivos de instalação do App-V 5,1 Server para o computador no qual você deseja instalá-lo.</span><span class="sxs-lookup"><span data-stu-id="c02be-107">Copy the App-V 5.1 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="c02be-108">Para iniciar a instalação do App-V 5,1 Server, clique com o botão direito do mouse e execute **appv\_server\_setup.exe** como administrador.</span><span class="sxs-lookup"><span data-stu-id="c02be-108">To start the App-V 5.1 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="c02be-109">Clique em **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="c02be-109">Click **Install**.</span></span>

2. <span data-ttu-id="c02be-110">Na página de **introdução** , examine e aceite os termos de licença e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="c02be-110">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3. <span data-ttu-id="c02be-111">Na página **usar o Microsoft Update para ajudar a manter seu computador seguro e atualizado** , para habilitar as atualizações da Microsoft, selecione **usar o Microsoft Update quando eu verificar se há atualizações (recomendado).**</span><span class="sxs-lookup"><span data-stu-id="c02be-111">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="c02be-112">Para desabilitar o Microsoft Updates, selecione **não quero usar o Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="c02be-112">To disable Microsoft updates, select **I don't want to use Microsoft Update**.</span></span> <span data-ttu-id="c02be-113">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="c02be-113">Click **Next**.</span></span>

4. <span data-ttu-id="c02be-114">Na página **seleção de recursos** , marque a caixa de seleção **servidor de relatório** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="c02be-114">On the **Feature Selection** page, select the **Reporting Server** checkbox and click **Next**.</span></span>

5. <span data-ttu-id="c02be-115">Na página **local de instalação** , aceite o local padrão e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="c02be-115">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6. <span data-ttu-id="c02be-116">Na página **configurar banco de dados de relatórios existente** , selecione **usar um SQL Server remoto**e digite o nome do computador que executa o Microsoft SQL Server, por exemplo, **SqlServerMachine**.</span><span class="sxs-lookup"><span data-stu-id="c02be-116">On the **Configure Existing Reporting Database** page, select **Use a remote SQL Server**, and type the machine name of the computer running Microsoft SQL Server, for example **SqlServerMachine**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c02be-117">Se o Microsoft SQL Server estiver implantado no mesmo servidor, selecione **usar SQL Server local**.</span><span class="sxs-lookup"><span data-stu-id="c02be-117">If the Microsoft SQL Server is deployed on the same server, select **Use local SQL Server**.</span></span>

    <span data-ttu-id="c02be-118">Para a instância do SQL Server, selecione **usar a instância padrão**.</span><span class="sxs-lookup"><span data-stu-id="c02be-118">For the SQL Server Instance, select **Use the default instance**.</span></span> <span data-ttu-id="c02be-119">Se estiver usando uma instância personalizada do Microsoft SQL Server, você deve selecionar **usar uma instância personalizada** e digitar o nome da instância.</span><span class="sxs-lookup"><span data-stu-id="c02be-119">If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.</span></span>

    <span data-ttu-id="c02be-120">Especifique o **nome do banco de dados do SQL Server** que será usado por esse servidor de relatórios, por exemplo, **AppvReporting**.</span><span class="sxs-lookup"><span data-stu-id="c02be-120">Specify the **SQL Server Database name** that this reporting server will use, for example **AppvReporting**.</span></span>

7. <span data-ttu-id="c02be-121">Na página **Configurar servidor de relatórios** .</span><span class="sxs-lookup"><span data-stu-id="c02be-121">On the **Configure Reporting Server Configuration** page.</span></span>

   - <span data-ttu-id="c02be-122">Especifique o nome do site que você deseja usar para o serviço de relatório.</span><span class="sxs-lookup"><span data-stu-id="c02be-122">Specify the Website Name that you want to use for the Reporting Service.</span></span> <span data-ttu-id="c02be-123">Deixe o padrão inalterado se você não tiver um nome personalizado.</span><span class="sxs-lookup"><span data-stu-id="c02be-123">Leave the default unchanged if you do not have a custom name.</span></span>

   - <span data-ttu-id="c02be-124">Para a **Associação de portabilidade**, especifique um número de porta exclusivo que será usado pelo App-V 5,1, por exemplo, **55555**.</span><span class="sxs-lookup"><span data-stu-id="c02be-124">For the **Port binding**, specify a unique port number that will be used by App-V 5.1, for example **55555**.</span></span> <span data-ttu-id="c02be-125">Você também deve certificar-se de que a porta especificada não está sendo usada por outro site.</span><span class="sxs-lookup"><span data-stu-id="c02be-125">You should also ensure that the port specified is not being used by another website.</span></span>

8. <span data-ttu-id="c02be-126">Clique em **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="c02be-126">Click **Install**.</span></span>

**<span data-ttu-id="c02be-127">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="c02be-127">Got an App-V issue?</span></span>** <span data-ttu-id="c02be-128">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="c02be-128">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="c02be-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c02be-129">Related topics</span></span>

[<span data-ttu-id="c02be-130">Sobre a emissão de relatórios do App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="c02be-130">About App-V 5.1 Reporting</span></span>](about-app-v-51-reporting.md)

[<span data-ttu-id="c02be-131">Implantação do App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="c02be-131">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="c02be-132">Como habilitar relatórios no cliente do App-V 5.1 usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="c02be-132">How to Enable Reporting on the App-V 5.1 Client by Using PowerShell</span></span>](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md)
