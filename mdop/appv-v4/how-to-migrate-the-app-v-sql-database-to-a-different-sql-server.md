---
title: Como migrar o banco de dados SQL do App-V para um SQL Server diferente
description: Como migrar o banco de dados SQL do App-V para um SQL Server diferente
author: dansimp
ms.assetid: 353892a1-9327-4489-a19c-4ec7bd1b736f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e3d84b0cb328873db3722ad3eb9af6a2b442fdcf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797052"
---
# <span data-ttu-id="a7e1f-103">Como migrar o banco de dados SQL do App-V para um SQL Server diferente</span><span class="sxs-lookup"><span data-stu-id="a7e1f-103">How to Migrate the App-V SQL Database to a Different SQL Server</span></span>


<span data-ttu-id="a7e1f-104">Os procedimentos a seguir descrevem em detalhes como migrar o banco de dados SQL do servidor de gerenciamento do Microsoft Application Virtualization (App-V) para um SQL Server diferente.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-104">The following procedures describe in detail how to migrate the SQL database of the Microsoft Application Virtualization (App-V) Management Server to a different SQL Server.</span></span>

<span data-ttu-id="a7e1f-105">**Importante**  Esse procedimento requer que o serviço App-V Server seja interrompido e isso impedirá que os usuários finais usem seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-105">**Important** This procedure requires that the App-V server service is stopped and this will prevent end-users from using their applications.</span></span>

 

**<span data-ttu-id="a7e1f-106">Para fazer backup do banco de dados SQL do App-V</span><span class="sxs-lookup"><span data-stu-id="a7e1f-106">To back up the App-V SQL database</span></span>**

1.  <span data-ttu-id="a7e1f-107">Abra o programa Services. msc e pare o serviço App-V Management Server em todos os servidores de gerenciamento que usam o banco de dados para ser migrado.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-107">Open the Services.msc program and stop the App-V Management Server service on all Management Servers that use the database to be migrated.</span></span>

2.  <span data-ttu-id="a7e1f-108">No computador em que o banco de dados do App-V está localizado, abra o SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-108">On the computer where the App-V database is located, open SQL Server Management Studio.</span></span>

3.  <span data-ttu-id="a7e1f-109">Expanda o nó **bancos** de dados e localize o banco de dados App-V (o nome padrão é APPVIRT).</span><span class="sxs-lookup"><span data-stu-id="a7e1f-109">Expand the **Databases** node and locate the App-V database (default name is APPVIRT).</span></span>

4.  <span data-ttu-id="a7e1f-110">Clique com o botão direito do mouse no banco de dados e selecione **tarefas** e, em seguida, selecione **fazer backup**.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-110">Right-click the database and select **Tasks** and then select **Back Up**.</span></span>

5.  <span data-ttu-id="a7e1f-111">Verifique se o **modelo de recuperação** está definido como **simples** e se o **tipo de backup** está definido como **completo**.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-111">Verify that **Recovery model** is set to **SIMPLE** and the **Backup type** is set to **Full**.</span></span> <span data-ttu-id="a7e1f-112">Altere as configurações do **conjunto de backup** e do **destino** se for necessário.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-112">Change the **Backup set** and **Destination** settings if it is necessary.</span></span>

6.  <span data-ttu-id="a7e1f-113">Clique em **OK** para fazer backup do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-113">Click **OK** to back up the database.</span></span> <span data-ttu-id="a7e1f-114">Depois que o backup for concluído com êxito, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-114">After the backup has completed successfully, click **OK**.</span></span>

7.  <span data-ttu-id="a7e1f-115">Abra o Windows Explorer e navegue até a pasta que contém o arquivo de backup do banco de dados, por exemplo, APPVIRT. Bak.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-115">Open Windows Explorer and browse to the folder that contains the database backup file, for example APPVIRT.BAK.</span></span> <span data-ttu-id="a7e1f-116">Copie o arquivo de backup do banco de dados para o computador de destino que está executando o SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-116">Copy the database backup file to the destination computer that is running SQL Server.</span></span>

**<span data-ttu-id="a7e1f-117">Para restaurar o banco de dados SQL do App-V para o computador de destino</span><span class="sxs-lookup"><span data-stu-id="a7e1f-117">To restore the App-V SQL database to the destination computer</span></span>**

1.  <span data-ttu-id="a7e1f-118">No computador de destino, abra o SQL Server Management Studio, clique com o botão direito do mouse no nó **bancos** de dados e selecione **restaurar banco de dados**.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-118">On the destination computer, open SQL Server Management Studio, right-click the **Databases** node and select **Restore Database**.</span></span>

2.  <span data-ttu-id="a7e1f-119">Em **origem para restauração**, escolha **do dispositivo** e, em seguida, clique no botão "**...**"</span><span class="sxs-lookup"><span data-stu-id="a7e1f-119">Under **Source for Restore**, choose **From device** and then click the “**…**”</span></span> <span data-ttu-id="a7e1f-120">.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-120">button.</span></span>

3.  <span data-ttu-id="a7e1f-121">Na caixa de diálogo **especificar backup** , verifique se a **mídia de backup** está definida como **arquivo** e clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-121">In the **Specify Backup** dialog box, make sure that the **Backup Media** is set to **File** and then click **Add**.</span></span>

4.  <span data-ttu-id="a7e1f-122">Selecione o arquivo de backup que você copiou do computador original que está executando o SQL Server e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-122">Select the backup file that you copied from the original computer that is running SQL Server, and then click **OK**.</span></span>

5.  <span data-ttu-id="a7e1f-123">Clique em **OK** e, em seguida, clique para selecionar o conjunto de backup a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-123">Click **OK** and then click to select the backup set to restore.</span></span>

6.  <span data-ttu-id="a7e1f-124">Em **destino para restauração**, clique na lista suspensa para o **banco de dados** e selecione o nome do banco de dados App-V, por exemplo, APPVIRT.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-124">Under **Destination for restore**, click the drop-down for **To database** and select the App-V database name, for example APPVIRT.</span></span>

7.  <span data-ttu-id="a7e1f-125">Clique em **OK** para iniciar a restauração.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-125">Click **OK** to start the restore.</span></span> <span data-ttu-id="a7e1f-126">Depois que a restauração for concluída com êxito, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-126">After the restore has completed successfully, click **OK**.</span></span>

8.  <span data-ttu-id="a7e1f-127">Expanda o nó **segurança** , clique com o botão direito do mouse em **logons** e selecione **novo logon**.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-127">Expand the **Security** node, right-click **Logins** and select **New Login**.</span></span>

9.  <span data-ttu-id="a7e1f-128">No campo **nome de logon** , insira os detalhes da conta de serviço de rede para o servidor de gerenciamento App-V no formato de DOMAIN\\SERVERNAME $.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-128">In the **Login Name** field, enter the Network Service account details for the App-V Management Server in the format of DOMAIN\\SERVERNAME$.</span></span>

10. <span data-ttu-id="a7e1f-129">Na página **geral** , em **banco de dados padrão** , selecione o nome do banco de dados App-V, por exemplo, APPVIRT, e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-129">On the **General** page under **Default database** select the App-V database name, for example, APPVIRT, and then click **OK**.</span></span>

11. <span data-ttu-id="a7e1f-130">Em **Selecione uma página**, clique para selecionar a página de **mapeamento de usuários** .</span><span class="sxs-lookup"><span data-stu-id="a7e1f-130">Under **Select a page**, click to select the **User Mapping** page.</span></span> <span data-ttu-id="a7e1f-131">Em **Usuários mapeados para este logon**, clique na caixa de seleção na coluna **mapa** para selecionar o banco de dados App-V.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-131">Under **Users mapped to this login**, click the check box in the **Map** column to select the App-V database.</span></span>

12. <span data-ttu-id="a7e1f-132">Em **Associação de função de banco de dados para: &lt; &gt; appvdatabasename**, clique para selecionar **SFTEveryone** e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-132">Under **Database role membership for: &lt;appvdatabasename&gt;**, click to select **SFTEveryone** and then click **OK**.</span></span>

13. <span data-ttu-id="a7e1f-133">Verifique se o Firewall do Windows no novo computador que está executando o SQL Server está configurado para permitir que o servidor de gerenciamento do App-V acesse o sistema.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-133">Make sure that the Windows Firewall on the new computer that is running SQL Server is configured to allow the App-V Management Server to access the system.</span></span> <span data-ttu-id="a7e1f-134">Em **Ferramentas administrativas**, use o programa **Firewall do Windows com segurança avançada** para criar uma **regra de entrada** para a porta usada pelo SQL Server (o padrão é a porta 1433).</span><span class="sxs-lookup"><span data-stu-id="a7e1f-134">Under **Administrative Tools**, use the **Windows Firewall with Advanced Security** program to create an **Inbound Rule** for the port that is used by SQL Server (default is port 1433).</span></span>

**<span data-ttu-id="a7e1f-135">Para migrar trabalhos do agente do SQL Server do App-V</span><span class="sxs-lookup"><span data-stu-id="a7e1f-135">To migrate the App-V SQL Server Agent jobs</span></span>**

1.  <span data-ttu-id="a7e1f-136">No computador original que está executando o SQL Server, no SQL Server Management Studio, expanda o nó do **agente do SQL Server** e, em seguida, expanda o nó **Jobs** .</span><span class="sxs-lookup"><span data-stu-id="a7e1f-136">On the original computer that is running SQL Server, in SQL Server Management Studio, expand the **SQL Server Agent** node, and then expand the **Jobs** node.</span></span>

2.  <span data-ttu-id="a7e1f-137">Clique com o botão direito do mouse nos quatro trabalhos do App-V a seguir e selecione **trabalho de script como | CRIAR para | Arquivo**e salve cada script em uma pasta e dê um nome descritivo a cada script.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-137">Right-click the following four App-V jobs and select **Script Job as | CREATE to | File**, and save each script to a folder and give each script a descriptive name.</span></span>

    -   **<span data-ttu-id="a7e1f-138">Banco de dados do SoftGrid (appvdbname) verificar histórico de uso</span><span class="sxs-lookup"><span data-stu-id="a7e1f-138">Softgrid Database (appvdbname) Check Usage History</span></span>**

    -   **<span data-ttu-id="a7e1f-139">Banco de dados do SoftGrid (appvdbname) fechar sessões órfãs</span><span class="sxs-lookup"><span data-stu-id="a7e1f-139">Softgrid Database (appvdbname) Close Orphaned Sessions</span></span>**

    -   **<span data-ttu-id="a7e1f-140">Banco de dados do SoftGrid (appvdbname) reforçar o limite de tamanho</span><span class="sxs-lookup"><span data-stu-id="a7e1f-140">Softgrid Database (appvdbname) Enforce Size Limit</span></span>**

    -   **<span data-ttu-id="a7e1f-141">Banco de dados do SoftGrid (appvdbname) monitorar o status do trabalho/alerta</span><span class="sxs-lookup"><span data-stu-id="a7e1f-141">Softgrid Database (appvdbname) Monitor Alert/Job Status</span></span>**

3.  <span data-ttu-id="a7e1f-142">Copie os quatro arquivos de script (. Sql) para o computador de destino que está executando o SQL Server e abra o SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-142">Copy the four script files (.sql) to the destination computer that is running SQL Server and open SQL Server Management Studio.</span></span>

4.  <span data-ttu-id="a7e1f-143">No Windows Explorer, clique com o botão direito do mouse em cada arquivo. SQL e clique em **executar**.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-143">In Windows Explorer, right-click each .sql file and then click **Run**.</span></span> <span data-ttu-id="a7e1f-144">Cada script será aberto em uma janela de consulta no SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-144">Each script will open in a query window in SQL Server Management Studio.</span></span> <span data-ttu-id="a7e1f-145">Clique em **executar** para cada script e verifique se cada um deles foi concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-145">Click **Execute** for each script and verify that each is completed successfully.</span></span>

5.  <span data-ttu-id="a7e1f-146">Atualize o nó **Jobs** no nó do **SQL Server Agent** e confirme se os quatro trabalhos foram criados com êxito.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-146">Refresh the **Jobs** node under the **SQL Server Agent** node and confirm that the four jobs are created successfully.</span></span>

**<span data-ttu-id="a7e1f-147">Para atualizar a configuração do servidor de gerenciamento do App-V</span><span class="sxs-lookup"><span data-stu-id="a7e1f-147">To update the configuration of the App-V Management Server</span></span>**

1.  <span data-ttu-id="a7e1f-148">No servidor de gerenciamento App-V, modifique as seguintes chaves do registro:</span><span class="sxs-lookup"><span data-stu-id="a7e1f-148">On the App-V Management Server, modify the following registry keys:</span></span>

    -   <span data-ttu-id="a7e1f-149">**SqlServerName**  =  &lt; newservername&gt;</span><span class="sxs-lookup"><span data-stu-id="a7e1f-149">**SQLServerName** = &lt;newservername&gt;</span></span>

    -   <span data-ttu-id="a7e1f-150">**SQLServerPort**  =  SQLServerPort &lt; newserverport&gt;</span><span class="sxs-lookup"><span data-stu-id="a7e1f-150">**SQLServerPort** = &lt;newserverport&gt;</span></span>

    <span data-ttu-id="a7e1f-151">Em seguida, reinicie o serviço App-V Server.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-151">Then restart the App-V server service.</span></span>

2.  <span data-ttu-id="a7e1f-152">Navegue até localizar o arquivo SftMgmt. udl no diretório de instalação do App-V Management Server (o padrão é C:\\Arquivos de Files\\Microsoft System Center App Virt Management Server\\App Virt Management Service).</span><span class="sxs-lookup"><span data-stu-id="a7e1f-152">Browse to find the file SftMgmt.udl under the App-V Management Server installation directory (default is C:\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt Management Service).</span></span> <span data-ttu-id="a7e1f-153">Clique com o botão direito do mouse no arquivo e selecione **abrir**.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-153">Right-click the file and select **Open**.</span></span>

3.  <span data-ttu-id="a7e1f-154">Na guia **conexão** , insira o nome do computador de destino que está executando o SQL Server e clique em **testar conexão**.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-154">On the **Connection** tab, enter the name of the destination computer that is running SQL Server, and then click **Test Connection**.</span></span> <span data-ttu-id="a7e1f-155">Quando o teste for bem-sucedido, clique em **OK** e em **OK** novamente.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-155">When the test is successful, click **OK** and then click **OK** again.</span></span>

4.  <span data-ttu-id="a7e1f-156">Para versões do App-V Management Server anteriores ao 4,5 SP2, você deve atualizar as configurações de log de SQL.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-156">For App-V Management Server versions before 4.5 SP2, you must update the SQL Logging settings.</span></span> <span data-ttu-id="a7e1f-157">Em **grupos de servidores**, clique com o botão direito do mouse no grupo do servidor do qual o servidor é membro e selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-157">Under **Server Groups**, right-click the server group the server is a member of and select **Properties**.</span></span>

5.  <span data-ttu-id="a7e1f-158">Na guia **log** , clique para selecionar a entrada do **banco de dados SQL** e, em seguida, clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-158">On the **Logging** tab click to select the **SQL Database** entry and then click **Edit**.</span></span>

6.  <span data-ttu-id="a7e1f-159">Altere o **nome do host DNS** para o nome do host do novo computador que está executando o SQL Server e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-159">Change the **DNS Host Name** to the host name of the new computer that is running SQL Server and then click **OK**.</span></span> <span data-ttu-id="a7e1f-160">Clique em **OK** duas vezes mais e reinicie o serviço App-V Server.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-160">Click **OK** two times more, and then restart the App-V server service.</span></span>

7.  <span data-ttu-id="a7e1f-161">Abra o console de gerenciamento do App-V, clique com o botão direito do mouse no nó **aplicativos** e selecione **Atualizar**.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-161">Open the App-V Management Console, right-click the **Applications** node and select **Refresh**.</span></span> <span data-ttu-id="a7e1f-162">A lista de aplicativos deve ser exibida como antes.</span><span class="sxs-lookup"><span data-stu-id="a7e1f-162">The list of applications should be displayed as before.</span></span>

 

 





