---
title: Como instalar os bancos de dados de gerenciamento e relatórios em computadores separados dos serviços de gerenciamento e relatórios
description: Como instalar os bancos de dados de gerenciamento e relatórios em computadores separados dos serviços de gerenciamento e relatórios
author: dansimp
ms.assetid: 02afd6d6-4c33-4c0b-bd88-ae167b786fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1522045fced411164ac4fd36af41d46ab61ad6f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796396"
---
# <span data-ttu-id="f5084-103">Como instalar os bancos de dados de gerenciamento e relatórios em computadores separados dos serviços de gerenciamento e relatórios</span><span class="sxs-lookup"><span data-stu-id="f5084-103">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>


<span data-ttu-id="f5084-104">Use o procedimento a seguir para instalar o servidor de banco de dados e o servidor de gerenciamento em computadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="f5084-104">Use the following procedure to install the database server and management server on different computers.</span></span> <span data-ttu-id="f5084-105">O computador no qual você planeja instalar o servidor de banco de dados deve estar executando uma versão com suporte do Microsoft SQL ou haverá falha na instalação.</span><span class="sxs-lookup"><span data-stu-id="f5084-105">The computer you plan to install the database server on must be running a supported version of Microsoft SQL or the installation will fail.</span></span>

**<span data-ttu-id="f5084-106">Observação</span><span class="sxs-lookup"><span data-stu-id="f5084-106">Note</span></span>**  
<span data-ttu-id="f5084-107">Depois de concluir a implantação, o nome do **Microsoft SQL Server**, o **nome da instância** e o **nome do banco de dados** serão exigidos pelo administrador que está instalando o serviço para poder se conectar a esses bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="f5084-107">After you complete the deployment, the **Microsoft SQL Server name**, **instance name** and **database name** will be required by the administrator installing the service to be able to connect to these databases.</span></span>



**<span data-ttu-id="f5084-108">Para instalar o banco de dados de gerenciamento e o servidor de gerenciamento em computadores separados</span><span class="sxs-lookup"><span data-stu-id="f5084-108">To install the management database and the management server on separate computers</span></span>**

1.  <span data-ttu-id="f5084-109">Copie os arquivos de instalação do App-V 5,0 Server para o computador no qual você deseja instalá-lo.</span><span class="sxs-lookup"><span data-stu-id="f5084-109">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="f5084-110">Para iniciar a instalação do App-V 5,0 Server, clique com o botão direito do mouse e execute **appv\_server\_setup.exe** como administrador.</span><span class="sxs-lookup"><span data-stu-id="f5084-110">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="f5084-111">Clique em **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="f5084-111">Click **Install**.</span></span>

2.  <span data-ttu-id="f5084-112">Na página de **introdução** , examine e aceite os termos de licença e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="f5084-112">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="f5084-113">Na página **usar o Microsoft Update para ajudar a manter seu computador seguro e atualizado** , para habilitar as atualizações da Microsoft, selecione **usar o Microsoft Update quando eu verificar se há atualizações (recomendado).**</span><span class="sxs-lookup"><span data-stu-id="f5084-113">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="f5084-114">Para desabilitar o Microsoft Updates, selecione **não quero usar o Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="f5084-114">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="f5084-115">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="f5084-115">Click **Next**.</span></span>

4.  <span data-ttu-id="f5084-116">Na página **seleção de recursos** , selecione os componentes que você deseja instalar, marcando a caixa de seleção **banco de dados do servidor de gerenciamento** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="f5084-116">On the **Feature Selection** page, select the components you want to install by selecting the **Management Server Database** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="f5084-117">Na página **local de instalação** , aceite o local padrão e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="f5084-117">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="f5084-118">Na página inicial **criar novo banco de dados do servidor de gerenciamento**, aceite as seleções padrão, se necessário, e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="f5084-118">On the initial **Create New Management Server Database page**, accept the default selections if appropriate, and click **Next**.</span></span>

    <span data-ttu-id="f5084-119">Se você estiver usando uma instância personalizada do SQL Server, selecione **usar uma instância personalizada** e digite o nome da instância.</span><span class="sxs-lookup"><span data-stu-id="f5084-119">If you are using a custom SQL Server instance, then select **Use a custom instance** and type the name of the instance.</span></span>

    <span data-ttu-id="f5084-120">Se você estiver usando um nome de banco de dados personalizado, selecione **configuração personalizada** e digite o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f5084-120">If you are using a custom database name, then select **Custom configuration** and type the database name.</span></span>

7.  <span data-ttu-id="f5084-121">Na página **criar novo banco de dados do servidor de gerenciamento** , selecione **usar um computador remoto**e digite a conta de computador remoto usando o seguinte formato: **Domain\\MachineAccount**.</span><span class="sxs-lookup"><span data-stu-id="f5084-121">On the next **Create New Management Server Database** page, select **Use a remote computer**, and type the remote machine account using the following format: **Domain\\MachineAccount**.</span></span>

    **<span data-ttu-id="f5084-122">Observação</span><span class="sxs-lookup"><span data-stu-id="f5084-122">Note</span></span>**  
    <span data-ttu-id="f5084-123">Se você planeja implantar o servidor de gerenciamento no mesmo computador, será necessário selecionar **usar este computador local**.</span><span class="sxs-lookup"><span data-stu-id="f5084-123">If you plan to deploy the management server on the same computer you must select **Use this local computer**.</span></span>



~~~
Specify the user name for the management server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. <span data-ttu-id="f5084-124">Para iniciar a instalação, clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="f5084-124">To start the installation, click **Install**.</span></span>

**<span data-ttu-id="f5084-125">Para instalar o banco de dados de relatórios e o servidor de relatórios em computadores separados</span><span class="sxs-lookup"><span data-stu-id="f5084-125">To install the reporting database and the reporting server on separate computers</span></span>**

1.  <span data-ttu-id="f5084-126">Copie os arquivos de instalação do App-V 5,0 Server para o computador no qual você deseja instalá-lo.</span><span class="sxs-lookup"><span data-stu-id="f5084-126">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="f5084-127">Para iniciar a instalação do App-V 5,0 Server, clique com o botão direito do mouse e execute **appv\_server\_setup.exe** como administrador.</span><span class="sxs-lookup"><span data-stu-id="f5084-127">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="f5084-128">Clique em **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="f5084-128">Click **Install**.</span></span>

2.  <span data-ttu-id="f5084-129">Na página de **introdução** , examine e aceite os termos de licença e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="f5084-129">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="f5084-130">Na página **usar o Microsoft Update para ajudar a manter seu computador seguro e atualizado** , para habilitar as atualizações da Microsoft, selecione **usar o Microsoft Update quando eu verificar se há atualizações (recomendado).**</span><span class="sxs-lookup"><span data-stu-id="f5084-130">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="f5084-131">Para desabilitar o Microsoft Updates, selecione **não quero usar o Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="f5084-131">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="f5084-132">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="f5084-132">Click **Next**.</span></span>

4.  <span data-ttu-id="f5084-133">Na página **seleção de recursos** , selecione os componentes que você deseja instalar, marcando a caixa de seleção **banco de dados do servidor de relatório** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="f5084-133">On the **Feature Selection** page, select the components you want to install by selecting the **Reporting Server Database** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="f5084-134">Na página **local de instalação** , aceite o local padrão e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="f5084-134">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="f5084-135">Na página inicial **criar novo banco de dados do servidor de relatórios** , aceite as seleções padrão, se necessário, e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="f5084-135">On the initial **Create New Reporting Server Database** page, accept the default selections if appropriate, and click **Next**.</span></span>

    <span data-ttu-id="f5084-136">Se você estiver usando uma instância personalizada do SQL Server, selecione **usar uma instância personalizada** e digite o nome da instância.</span><span class="sxs-lookup"><span data-stu-id="f5084-136">If you are using a custom SQL Server instance, then select **Use a custom instance** and type the name of the instance.</span></span>

    <span data-ttu-id="f5084-137">Se você estiver usando um nome de banco de dados personalizado, selecione **configuração personalizada** e digite o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f5084-137">If you are using a custom database name, then select **Custom configuration** and type the database name.</span></span>

7.  <span data-ttu-id="f5084-138">Na página **criar novo banco de dados do servidor de relatórios** , selecione **usar um computador remoto**e digite a conta de computador remoto usando o seguinte formato: **Domain\\MachineAccount**.</span><span class="sxs-lookup"><span data-stu-id="f5084-138">On the next **Create New Reporting Server Database** page, select **Use a remote computer**, and type the remote machine account using the following format: **Domain\\MachineAccount**.</span></span>

    **<span data-ttu-id="f5084-139">Observação</span><span class="sxs-lookup"><span data-stu-id="f5084-139">Note</span></span>**  
    <span data-ttu-id="f5084-140">Se você planeja implantar o servidor de relatórios no mesmo computador, será necessário selecionar **usar este computador local**.</span><span class="sxs-lookup"><span data-stu-id="f5084-140">If you plan to deploy the reporting server on the same computer you must select **Use this local computer**.</span></span>



~~~
Specify the user name for the reporting server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. <span data-ttu-id="f5084-141">Para iniciar a instalação, clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="f5084-141">To start the installation, click **Install**.</span></span>

**<span data-ttu-id="f5084-142">Para instalar os bancos de dados de gerenciamento e relatórios usando scripts de banco de dados do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="f5084-142">To install the management and reporting databases using App-V 5.0 database scripts</span></span>**

1.  <span data-ttu-id="f5084-143">Copie os arquivos de instalação do App-V 5,0 Server para o computador no qual você deseja instalá-lo.</span><span class="sxs-lookup"><span data-stu-id="f5084-143">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span>

2.  <span data-ttu-id="f5084-144">Para extrair os scripts do banco de dados do App-V 5,0, abra um prompt de comando e especifique o local onde os arquivos de instalação são salvos e execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="f5084-144">To extract the App-V 5.0 database scripts, open a command prompt and specify the location where the installation files are saved and run the following command:</span></span>

    <span data-ttu-id="f5084-145">**appv\_server\_setup.exe** **/layout** **/LAYOUTDIR = "InstallationExtractionLocation"**.</span><span class="sxs-lookup"><span data-stu-id="f5084-145">**appv\_server\_setup.exe** **/LAYOUT** **/LAYOUTDIR=”InstallationExtractionLocation”**.</span></span>

3.  <span data-ttu-id="f5084-146">Após a extração ter sido completada, para acessar o arquivo Leiame de instruções e scripts de banco de dados do App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="f5084-146">After the extraction has been completed, to access the App-V 5.0 database scripts and instructions readme file:</span></span>

    -   <span data-ttu-id="f5084-147">O Leiame de instruções e scripts de banco de dados de gerenciamento do App-V 5,0 estão localizados na seguinte pasta: banco de dados de gerenciamento de scripts de banco de **InstallationExtractionLocation**  \\  **Database Scripts**  \\  **Management Database**.</span><span class="sxs-lookup"><span data-stu-id="f5084-147">The App-V 5.0 Management Database scripts and instructions readme are located in the following folder: **InstallationExtractionLocation** \\ **Database Scripts** \\ **Management Database**.</span></span>

    -   <span data-ttu-id="f5084-148">O Leiame de instruções e scripts do banco de dados de relatórios do App-V 5,0 estão localizados na seguinte pasta: **InstallationExtractionLocation**de relatório de  \\  **scripts de banco de dados**do aplicativo  \\  **Reporting Database**.</span><span class="sxs-lookup"><span data-stu-id="f5084-148">The App-V 5.0 Reporting Database scripts and instructions readme are located in the following folder: **InstallationExtractionLocation** \\ **Database Scripts** \\ **Reporting Database**.</span></span>

4.  <span data-ttu-id="f5084-149">Para cada banco de dados, copie os scripts para um compartilhamento e modifique-os seguindo as instruções no arquivo readme.</span><span class="sxs-lookup"><span data-stu-id="f5084-149">For each database, copy the scripts to a share and modify them following the instructions in the readme file.</span></span>

    **<span data-ttu-id="f5084-150">Observação</span><span class="sxs-lookup"><span data-stu-id="f5084-150">Note</span></span>**  
    <span data-ttu-id="f5084-151">Para obter mais informações sobre como modificar os SIDs obrigatórios contidos nos scripts, consulte [como instalar os bancos de dados do App-V e converter os identificadores de segurança associados usando o PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="f5084-151">For more information about modifying the required SIDs contained in the scripts see, [How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md).</span></span>



5.  <span data-ttu-id="f5084-152">Execute os scripts no computador que está executando o Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f5084-152">Run the scripts on the computer running Microsoft SQL Server.</span></span>

    <span data-ttu-id="f5084-153">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="f5084-153">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="f5084-154">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="f5084-154">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="f5084-155">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="f5084-155">Got an App-V issue?</span></span>** <span data-ttu-id="f5084-156">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="f5084-156">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="f5084-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5084-157">Related topics</span></span>


[<span data-ttu-id="f5084-158">Implantação do App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f5084-158">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)









