---
title: Como configurar o suporte para espelhamento do Microsoft SQL Server para o App-V
description: Como configurar o suporte para espelhamento do Microsoft SQL Server para o App-V
author: dansimp
ms.assetid: 6d069eb5-109f-460a-836a-de49473b7035
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fb572442cd12bb32fc9406de65f05a3bf061f946
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797224"
---
# <span data-ttu-id="c10f2-103">Como configurar o suporte para espelhamento do Microsoft SQL Server para o App-V</span><span class="sxs-lookup"><span data-stu-id="c10f2-103">How to Configure Microsoft SQL Server Mirroring Support for App-V</span></span>


<span data-ttu-id="c10f2-104">Você pode usar o procedimento a seguir para configurar seu ambiente do Microsoft Application Virtualization (App-V) para usar o espelhamento de banco de dados do Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c10f2-104">You can use the following procedure to configure your Microsoft Application Virtualization (App-V) environment to use Microsoft SQL Server database mirroring.</span></span> <span data-ttu-id="c10f2-105">Configurar o espelhamento de banco de dados pode ajudar nos cenários de recuperação de desastres e failover.</span><span class="sxs-lookup"><span data-stu-id="c10f2-105">Configuring database mirroring can help with disaster recovery and failover scenarios.</span></span> <span data-ttu-id="c10f2-106">O App-V 4,5 SP2 dá suporte a todos os modos de espelhamento de banco de dados atualmente disponíveis para o Microsoft SQL Server 2005 e o SQL Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c10f2-106">App-V 4.5 SP2 supports all modes of database mirroring currently available for Microsoft SQL Server 2005 and SQL Server 2008.</span></span>

**<span data-ttu-id="c10f2-107">Observação</span><span class="sxs-lookup"><span data-stu-id="c10f2-107">Note</span></span>**  
<span data-ttu-id="c10f2-108">Esse procedimento foi escrito para administradores que estão familiarizados com a configuração e a configuração de bancos de dados e o espelhamento de banco de dados do SQL Server com o Microsoft SQL Server e, portanto, abrange apenas as configurações específicas que são exclusivas do App-V.</span><span class="sxs-lookup"><span data-stu-id="c10f2-108">This procedure is written for administrators who are familiar with setting up and configuring SQL Server databases and database mirroring with Microsoft SQL Server, and therefore covers only the specific configuration settings that are unique to App-V.</span></span>



**<span data-ttu-id="c10f2-109">Para configurar seu ambiente do App-V para usar o espelhamento de banco de dados do Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="c10f2-109">To configure your App-V environment to use Microsoft SQL Server database mirroring</span></span>**

1.  <span data-ttu-id="c10f2-110">Configure o espelhamento de banco de dados do SQL Server do banco de dados do App-V seguindo as práticas comerciais padrão para o espelhamento do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c10f2-110">Set up SQL Server database mirroring of the App-V database following your standard business practices for database mirroring.</span></span> <span data-ttu-id="c10f2-111">Use os links a seguir para obter informações gerais sobre como implementar o espelhamento de banco de dados do Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="c10f2-111">Use the following links for general information about implementing Microsoft SQL Server database mirroring:</span></span>

    -   <span data-ttu-id="c10f2-112">**Microsoft SQL 2005**–[Configurando o espelhamento do banco de dados](https://go.microsoft.com/fwlink/?LinkId=187478) (https://go.microsoft.com/fwlink/?LinkId=187478)</span><span class="sxs-lookup"><span data-stu-id="c10f2-112">**Microsoft SQL 2005**—[Setting Up Database Mirroring](https://go.microsoft.com/fwlink/?LinkId=187478) (https://go.microsoft.com/fwlink/?LinkId=187478)</span></span>

    -   <span data-ttu-id="c10f2-113">**Microsoft SQL 2008**–[Configurando o espelhamento do banco de dados](https://go.microsoft.com/fwlink/?LinkId=187477) (https://go.microsoft.com/fwlink/?LinkId=187477)</span><span class="sxs-lookup"><span data-stu-id="c10f2-113">**Microsoft SQL 2008**—[Setting Up Database Mirroring](https://go.microsoft.com/fwlink/?LinkId=187477) (https://go.microsoft.com/fwlink/?LinkId=187477)</span></span>

    <span data-ttu-id="c10f2-114">Além disso, você pode encontrar informações sobre as práticas recomendadas nas [práticas recomendadas de espelhamento de banco de dados e considerações de desempenho](https://go.microsoft.com/fwlink/?LinkId=190270) ( https://go.microsoft.com/fwlink/?LinkId=190270) .</span><span class="sxs-lookup"><span data-stu-id="c10f2-114">In addition, you can find Best Practices information in [Database Mirroring Best Practices and Performance Considerations](https://go.microsoft.com/fwlink/?LinkId=190270) (https://go.microsoft.com/fwlink/?LinkId=190270).</span></span>

2.  <span data-ttu-id="c10f2-115">Após a configuração do espelhamento, verifique se o banco de dados do App-V mostra um status de **(principal, sincronizado)** e se o banco de dados espelhado mostra um status de **(espelho, sincronizado/restauração)**.</span><span class="sxs-lookup"><span data-stu-id="c10f2-115">After mirroring has been set up, verify that the App-V database shows a status of **(Principal, Synchronized)**, and the mirrored database shows a status of **(Mirror, Synchronized / Restoring)**.</span></span> <span data-ttu-id="c10f2-116">Resolva problemas de espelhamento antes de prosseguir para a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="c10f2-116">Resolve any mirroring issues before proceeding to the next step.</span></span> <span data-ttu-id="c10f2-117">Para obter informações adicionais sobre como monitorar o status, consulte [monitorando o status do espelhamento](https://go.microsoft.com/fwlink/?LinkId=190279) ( https://go.microsoft.com/fwlink/?LinkId=190279) .</span><span class="sxs-lookup"><span data-stu-id="c10f2-117">For additional information about monitoring the status, see [Monitoring Mirroring Status](https://go.microsoft.com/fwlink/?LinkId=190279) (https://go.microsoft.com/fwlink/?LinkId=190279).</span></span>

3.  <span data-ttu-id="c10f2-118">No computador SQL Server que hospeda o espelho do banco de dados do App-v, crie o logon do SQL Server para a conta de serviço de rede do servidor de gerenciamento do App-v usando o nome de conta de \*\* &lt; domínio &gt; \\ &lt; ManagementServerHostName &gt; $ \*\*.</span><span class="sxs-lookup"><span data-stu-id="c10f2-118">On the SQL Server computer that hosts the mirror of the App-V database, create the SQL Server Login for the network service account of the App-V Management Server by using the account name **&lt;domain&gt;\\&lt;ManagementServerHostName&gt;$**.</span></span>

4.  <span data-ttu-id="c10f2-119">Instale o cliente nativo do Microsoft SQL Server no servidor de gerenciamento do App-V e no computador que executa o serviço Web de gerenciamento do App-V, se instalado em um computador diferente.</span><span class="sxs-lookup"><span data-stu-id="c10f2-119">Install the Microsoft SQL Server Native Client on the App-V Management Server, and on the computer running the App-V Management Web Service if installed on a different computer.</span></span> <span data-ttu-id="c10f2-120">Se você planeja ter servidores de gerenciamento do App-V adicionais se conectarem ao banco de dados SQL espelhado para o balanceamento de carga, você deve instalar o Microsoft SQL Server Native Client nesses computadores também.</span><span class="sxs-lookup"><span data-stu-id="c10f2-120">If you plan to have additional App-V Management Servers connect to the mirrored SQL database for load balancing, you must install the Microsoft SQL Server Native Client on those computers as well.</span></span> <span data-ttu-id="c10f2-121">Você pode baixar o Microsoft SQL Server Native Client da página [Microsoft SQL server 2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=187479) no centro de download da Microsoft ( https://go.microsoft.com/fwlink/?LinkId=187479) .</span><span class="sxs-lookup"><span data-stu-id="c10f2-121">You can download the Microsoft SQL Server Native Client from the [Microsoft SQL Server 2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=187479) page in the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=187479).</span></span>

5.  <span data-ttu-id="c10f2-122">Verifique a chave de registro **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlservername** e verifique se ela contém apenas o nome de host do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c10f2-122">Check the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLServerName** and make sure that it contains only the host name of the SQL Server.</span></span> <span data-ttu-id="c10f2-123">Se ele incluir um nome de instância, por exemplo, *serverhostname\\instancename*, o nome da instância deve ser removido.</span><span class="sxs-lookup"><span data-stu-id="c10f2-123">If it includes an instance name, for example *serverhostname\\instancename*, the instance name must be removed.</span></span>

    **<span data-ttu-id="c10f2-124">Importante</span><span class="sxs-lookup"><span data-stu-id="c10f2-124">Important</span></span>**  
    <span data-ttu-id="c10f2-125">O servidor de gerenciamento do App-V usa a biblioteca de rede TCP/IP para se comunicar com o SQL Server quando o espelhamento de banco de dados está habilitado e, portanto, os nomes de instância não podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="c10f2-125">The App-V Management Server uses the TCP/IP networking library to communicate with the SQL Server when database mirroring is enabled, and therefore instance names cannot be used.</span></span> <span data-ttu-id="c10f2-126">Em vez disso, os números das portas devem ser especificados nas chaves do registro.</span><span class="sxs-lookup"><span data-stu-id="c10f2-126">The port numbers must be specified in the registry keys instead.</span></span>



6.  <span data-ttu-id="c10f2-127">Verifique a chave de registro **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlserverport** e certifique-se de que ela contenha o número da porta usada para SQL no computador SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c10f2-127">Check the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLServerPort** and make sure that it contains the port number that is used for SQL on the SQL Server computer.</span></span> <span data-ttu-id="c10f2-128">Se você estiver usando uma instância nomeada, esse valor chave deve ser definido como a porta usada para a instância nomeada.</span><span class="sxs-lookup"><span data-stu-id="c10f2-128">If you are using a named instance this key value must be set to the port that is used for the named instance.</span></span>

7.  <span data-ttu-id="c10f2-129">Crie a chave de registro **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlfailoverservername** as REG \ _SZ e, em seguida, defina o valor para o nome do host do SQL Server que hospeda o espelho.</span><span class="sxs-lookup"><span data-stu-id="c10f2-129">Create the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLFailoverServerName** as REG\_SZ and then set the value to the host name of the SQL Server that hosts the mirror.</span></span>

8.  <span data-ttu-id="c10f2-130">Crie a chave de registro **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlfailoverserverport** como DWORD e, em seguida, defina o valor para o número da porta que é usado para SQL no computador que está executando o SQL Server para hospedar o espelho.</span><span class="sxs-lookup"><span data-stu-id="c10f2-130">Create the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLFailoverServerPort** as DWORD and then set the value to the port number that is used for SQL on the computer that is running SQL Server to host the mirror.</span></span> <span data-ttu-id="c10f2-131">Se você estiver usando uma instância nomeada para o espelho, esse valor chave deve ser definido como o número da porta que será usado para a instância nomeada.</span><span class="sxs-lookup"><span data-stu-id="c10f2-131">If you are using a named instance for the mirror this key value must be set to the port number that is used for the named instance.</span></span>

9.  <span data-ttu-id="c10f2-132">No computador que está executando o serviço Web de gerenciamento do App-V, configure o arquivo de texto do UDL (Universal Data Link).</span><span class="sxs-lookup"><span data-stu-id="c10f2-132">On the computer that is running the App-V Management Web Service, configure the Universal Data Link (UDL) text file.</span></span> <span data-ttu-id="c10f2-133">No diretório onde o App-V está instalado, clique duas vezes em **SftMgmt. udl** e especifique os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="c10f2-133">In the directory where App-V is installed, double-click **SftMgmt.udl** and specify the following values:</span></span>

    -   <span data-ttu-id="c10f2-134">Na guia **provedor** , selecione o provedor OLE DB do **SQL Server Native Client 10,0**.</span><span class="sxs-lookup"><span data-stu-id="c10f2-134">On the **Provider** tab, select the OLE DB provider **SQL Server Native Client 10.0**.</span></span>

    -   <span data-ttu-id="c10f2-135">Clique em **Avançar** para selecionar a guia **conexão** . Na caixa **nome do servidor** , digite o nome do servidor do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c10f2-135">Click **Next** to select the **Connection** tab. In the **Server Name** box, enter the server name of the SQL Server.</span></span> <span data-ttu-id="c10f2-136">Em seguida, selecione **usar a segurança integrada do Windows NT**.</span><span class="sxs-lookup"><span data-stu-id="c10f2-136">Next, select **Use Windows NT Integrated Security**.</span></span> <span data-ttu-id="c10f2-137">Por fim, clique na lista **Selecione o banco de dados**e, em seguida, selecione o nome do banco de dados App-V.</span><span class="sxs-lookup"><span data-stu-id="c10f2-137">Finally, click the list **Select the database**, and then select the App-V database name.</span></span>

    -   <span data-ttu-id="c10f2-138">Clique na guia **tudo** e selecione o **parceiro de failover**de entrada.</span><span class="sxs-lookup"><span data-stu-id="c10f2-138">Click the **All** tab, and then select the entry **Failover Partner**.</span></span> <span data-ttu-id="c10f2-139">Clique em **Editar valor**e insira o nome do servidor do SQL Server de failover.</span><span class="sxs-lookup"><span data-stu-id="c10f2-139">Click **Edit Value**, and then enter the server name of the failover SQL Server.</span></span> <span data-ttu-id="c10f2-140">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="c10f2-140">Click **OK**.</span></span>

    **<span data-ttu-id="c10f2-141">Importante</span><span class="sxs-lookup"><span data-stu-id="c10f2-141">Important</span></span>**  
    <span data-ttu-id="c10f2-142">O sistema App-V usa a autenticação Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c10f2-142">The App-V system uses Kerberos authentication.</span></span> <span data-ttu-id="c10f2-143">Portanto, quando você configura o espelhamento do SQL no qual a autenticação Kerberos está habilitada no SQL Server e o serviço do SQL Server é executado em uma conta de usuário do domínio, você deve configurar manualmente um SPN.</span><span class="sxs-lookup"><span data-stu-id="c10f2-143">Therefore, when you configure SQL mirroring where Kerberos Authentication is enabled on the SQL Server and the SQL Server service runs under a domain user account, you must manually configure an SPN.</span></span> <span data-ttu-id="c10f2-144">Para obter mais informações, consulte "quando o serviço SQL usa a conta baseada em domínio" no artigo [Configurando a administração do App-V para um ambiente distribuído](https://go.microsoft.com/fwlink/?LinkId=203186) ( https://go.microsoft.com/fwlink/?LinkId=203186) .</span><span class="sxs-lookup"><span data-stu-id="c10f2-144">For more information, see “When SQL Service Uses Domain-Based Account” in the article [Configuring App-V Administration for a Distributed Environment](https://go.microsoft.com/fwlink/?LinkId=203186) (https://go.microsoft.com/fwlink/?LinkId=203186).</span></span>



10. <span data-ttu-id="c10f2-145">Para verificar se o espelhamento do banco de dados está funcionando corretamente, teste o failover e confirme se o App-V Management Server continua funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="c10f2-145">To verify that database mirroring is running correctly, test the failover and confirm that the App-V Management Server continues to function correctly.</span></span>

    **<span data-ttu-id="c10f2-146">Importante</span><span class="sxs-lookup"><span data-stu-id="c10f2-146">Important</span></span>**  
    <span data-ttu-id="c10f2-147">Continue com cuidado e siga as práticas comerciais padrão para garantir que as operações do sistema não sejam interrompidas em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="c10f2-147">Proceed with care, and follow your standard business practices to ensure that system operations are not disrupted in the event of a failure.</span></span>



~~~
After the failover has occurred successfully, as verified by using the SQL Server status monitoring information, right-click the **Applications** node in the App-V Management Console, and then select **Refresh**. The list of applications should display normally if the system is working correctly.
~~~

## <span data-ttu-id="c10f2-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c10f2-148">Related topics</span></span>


[<span data-ttu-id="c10f2-149">Como realizar tarefas administrativas no Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="c10f2-149">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)









