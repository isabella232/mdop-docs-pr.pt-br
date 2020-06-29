---
title: Planejamento de alta disponibilidade com o App-V 5.1
description: Planejamento de alta disponibilidade com o App-V 5.1
author: dansimp
ms.assetid: 1f190a0e-10ee-4fbe-a602-7e807e943033
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5c8e0e684051859a4caa2c4ef983c040295bc6d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796260"
---
# <span data-ttu-id="50d83-103">Planejamento de alta disponibilidade com o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="50d83-103">Planning for High Availability with App-V 5.1</span></span>


<span data-ttu-id="50d83-104">As configurações de sistema do Microsoft Application Virtualization (App-V) 5,1 podem aproveitar as opções que mantêm um alto nível de serviço disponível.</span><span class="sxs-lookup"><span data-stu-id="50d83-104">Microsoft Application Virtualization (App-V) 5.1 system configurations can take advantage of options that maintain a high level of available service.</span></span>

<span data-ttu-id="50d83-105">Use as informações das seções a seguir para ajudá-lo a entender as opções de implantação do App-V 5,1 em uma configuração altamente disponível.</span><span class="sxs-lookup"><span data-stu-id="50d83-105">Use the information in the following sections to help you understand the options to deploy App-V 5.1 in a highly available configuration.</span></span>

-   [<span data-ttu-id="50d83-106">Suporte para clustering do Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="50d83-106">Support for Microsoft SQL Server clustering</span></span>](#bkmk-sqlcluster)

-   [<span data-ttu-id="50d83-107">Suporte para balanceamento de carga de rede do IIS</span><span class="sxs-lookup"><span data-stu-id="50d83-107">Support for IIS Network Load Balancing</span></span>](#bkmk-iisloadbal)

-   [<span data-ttu-id="50d83-108">Suporte a servidores de arquivos em cluster ao executar o modo (SCS)</span><span class="sxs-lookup"><span data-stu-id="50d83-108">Support for clustered file servers when running (SCS) mode</span></span>](#bkmk-clusterscsmode)

-   [<span data-ttu-id="50d83-109">Suporte para espelhamento do Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="50d83-109">Support for Microsoft SQL Server Mirroring</span></span>](#bkmk-sqlmirroring)

-   [<span data-ttu-id="50d83-110">Suporte para o Microsoft SQL Server sempre ligado</span><span class="sxs-lookup"><span data-stu-id="50d83-110">Support for Microsoft SQL Server Always On</span></span>](#bkmk-sqlalwayson)

## <a href="" id="bkmk-sqlcluster"></a><span data-ttu-id="50d83-111">Suporte para clustering do Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="50d83-111">Support for Microsoft SQL Server clustering</span></span>


<span data-ttu-id="50d83-112">Você pode executar o banco de dados de gerenciamento do App-V e o banco de dados de relatórios em computadores que executam clusters do Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="50d83-112">You can run the App-V Management database and Reporting database on computers that are running Microsoft SQL Server clusters.</span></span> <span data-ttu-id="50d83-113">No entanto, você deve instalar os bancos de dados usando scripts.</span><span class="sxs-lookup"><span data-stu-id="50d83-113">However, you must install the databases using scripts.</span></span>

<span data-ttu-id="50d83-114">Para obter instruções, consulte [como implantar os bancos de dados do App-V usando scripts SQL](how-to-deploy-the-app-v-databases-by-using-sql-scripts51.md).</span><span class="sxs-lookup"><span data-stu-id="50d83-114">For instructions, see [How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts51.md).</span></span>

## <a href="" id="bkmk-iisloadbal"></a><span data-ttu-id="50d83-115">Suporte para balanceamento de carga de rede do IIS</span><span class="sxs-lookup"><span data-stu-id="50d83-115">Support for IIS Network Load Balancing</span></span>


<span data-ttu-id="50d83-116">Você pode usar o balanceamento de carga de rede dos serviços de informações da Internet (IIS) para configurar um ambiente altamente disponível para computadores que executam os serviços de gerenciamento, publicação e relatórios do App-V 5. x que são implantados pelo IIS.</span><span class="sxs-lookup"><span data-stu-id="50d83-116">You can use Internet Information Services (IIS) Network Load Balancing to configure a highly available environment for computers running the App-V 5.x Management, Publishing, and Reporting services which are deployed through IIS.</span></span>

<span data-ttu-id="50d83-117">Revise as informações a seguir para obter mais informações sobre como configurar o IIS e o balanceamento de carga de rede para computadores que executam sistemas operacionais Windows Server:</span><span class="sxs-lookup"><span data-stu-id="50d83-117">Review the following for more information about configuring IIS and Network Load Balancing for computers running Windows Server operating systems:</span></span>

-   <span data-ttu-id="50d83-118">Fornece informações sobre como configurar os serviços de informações da Internet (IIS) 7,0.</span><span class="sxs-lookup"><span data-stu-id="50d83-118">Provides information about configuring Internet Information Services (IIS) 7.0.</span></span>

    <span data-ttu-id="50d83-119">[Obtendo alta disponibilidade e escalabilidade-ARR e NLB](https://go.microsoft.com/fwlink/?LinkId=316369) (https://go.microsoft.com/fwlink/?LinkId=316369)</span><span class="sxs-lookup"><span data-stu-id="50d83-119">[Achieving High Availability and Scalability - ARR and NLB](https://go.microsoft.com/fwlink/?LinkId=316369) (https://go.microsoft.com/fwlink/?LinkId=316369)</span></span>

-   <span data-ttu-id="50d83-120">Configurando o Microsoft Windows Server</span><span class="sxs-lookup"><span data-stu-id="50d83-120">Configuring Microsoft Windows Server</span></span>

    <span data-ttu-id="50d83-121">[Balanceamento de carga de rede](https://go.microsoft.com/fwlink/?LinkId=316370) ( https://go.microsoft.com/fwlink/?LinkId=316370) .</span><span class="sxs-lookup"><span data-stu-id="50d83-121">[Network Load Balancing](https://go.microsoft.com/fwlink/?LinkId=316370) (https://go.microsoft.com/fwlink/?LinkId=316370).</span></span>

    <span data-ttu-id="50d83-122">Essas informações também se aplicam aos clusters de balanceamento de carga de rede (NLB) do IIS no Windows Server2008, no Windows Server2008R2 ou no Windows Server2012.</span><span class="sxs-lookup"><span data-stu-id="50d83-122">This information also applies to IIS Network Load Balancing (NLB) clusters in Windows Server2008, Windows Server2008R2, or Windows Server2012.</span></span>

    <span data-ttu-id="50d83-123">**Observação**  A funcionalidade de balanceamento de carga de rede do IIS no Windows Server2012 geralmente é a mesma que no Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="50d83-123">**Note** The IIS Network Load Balancing functionality in Windows Server2012 is generally the same as in Windows Server2008R2.</span></span> <span data-ttu-id="50d83-124">No entanto, alguns detalhes da tarefa são alterados no Windows Server2012.</span><span class="sxs-lookup"><span data-stu-id="50d83-124">However, some task details are changed in Windows Server2012.</span></span> <span data-ttu-id="50d83-125">Para obter informações sobre novas maneiras de executar tarefas, consulte [tarefas comuns de gerenciamento e navegação no Windows server 2012 R2 Preview e no Windows server 2012](https://go.microsoft.com/fwlink/?LinkId=316371) ( https://go.microsoft.com/fwlink/?LinkId=316371) .</span><span class="sxs-lookup"><span data-stu-id="50d83-125">For information on new ways to do tasks, see [Common Management Tasks and Navigation in Windows Server 2012 R2 Preview and Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316371) (https://go.microsoft.com/fwlink/?LinkId=316371).</span></span>

     

## <a href="" id="bkmk-clusterscsmode"></a><span data-ttu-id="50d83-126">Suporte a servidores de arquivos em cluster ao executar o modo (SCS)</span><span class="sxs-lookup"><span data-stu-id="50d83-126">Support for clustered file servers when running (SCS) mode</span></span>


<span data-ttu-id="50d83-127">A execução do App-V 5,1 no modo de armazenamento de conteúdo de compartilhamento (SCS) com servidores de arquivos clusterizados é compatível.</span><span class="sxs-lookup"><span data-stu-id="50d83-127">Running App-V 5.1 in Share Content Store (SCS) mode with clustered file servers is supported.</span></span>

<span data-ttu-id="50d83-128">As etapas a seguir podem ser usadas para habilitar essa configuração:</span><span class="sxs-lookup"><span data-stu-id="50d83-128">The following steps can be used to enable this configuration:</span></span>

-   <span data-ttu-id="50d83-129">Configurar o App-V 5,1 para ser executado no modo SCS do cliente.</span><span class="sxs-lookup"><span data-stu-id="50d83-129">Configure App-V 5.1 to run in client SCS mode.</span></span> <span data-ttu-id="50d83-130">Para obter mais informações sobre a configuração do modo SCS do App-V 5,1, consulte [como instalar o app-v 5,1 cliente para o modo de repositório de conteúdo compartilhado](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md).</span><span class="sxs-lookup"><span data-stu-id="50d83-130">For more information about configuring App-V 5.1 SCS mode, see [How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md).</span></span>

-   <span data-ttu-id="50d83-131">Configure o cluster de servidor de arquivos configurado no modo de dimensionamento do Microsoft Server2012 e no modo pré **2012** com uma rede SAN virtual.</span><span class="sxs-lookup"><span data-stu-id="50d83-131">Configure the file server cluster configured in both the Microsoft Server2012 scale out mode and pre **2012** mode with a virtual SAN.</span></span>

<span data-ttu-id="50d83-132">As etapas a seguir podem ser usadas para validar a configuração:</span><span class="sxs-lookup"><span data-stu-id="50d83-132">The following steps can be used to validate the configuration:</span></span>

1.  <span data-ttu-id="50d83-133">Adicione um pacote no servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="50d83-133">Add a package on the publishing server.</span></span> <span data-ttu-id="50d83-134">Para obter mais informações sobre como adicionar um pacote, consulte [como adicionar ou atualizar pacotes usando o console de gerenciamento](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="50d83-134">For more information about adding a package, see [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md).</span></span>

2.  <span data-ttu-id="50d83-135">Realize uma atualização de publicação no computador que executa o cliente App-V 5,1 e abra um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="50d83-135">Perform a publishing refresh on the computer running the App-V 5.1 client and open an application.</span></span>

3.  <span data-ttu-id="50d83-136">Alternar os nós de cluster de opções de atualização de publicação mid e de fluxo contínuo para garantir que o failover funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="50d83-136">Switch cluster nodes mid-publishing refresh and mid-streaming to ensure fail-over works correctly.</span></span>

<span data-ttu-id="50d83-137">Revise as informações a seguir para obter mais informações sobre como configurar clusters de failover do Windows Server:</span><span class="sxs-lookup"><span data-stu-id="50d83-137">Review the following for more information about configuring Windows Server Failover clusters:</span></span>

-   <span data-ttu-id="50d83-138">[Lista de verificação: criar um servidor de arquivos em cluster](https://go.microsoft.com/fwlink/?LinkId=316372) ( https://go.microsoft.com/fwlink/?LinkId=316372) .</span><span class="sxs-lookup"><span data-stu-id="50d83-138">[Checklist: Create a Clustered File Server](https://go.microsoft.com/fwlink/?LinkId=316372) (https://go.microsoft.com/fwlink/?LinkId=316372).</span></span>

-   <span data-ttu-id="50d83-139">[Use volumes compartilhados de cluster em um cluster de failover do Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316373) ( https://go.microsoft.com/fwlink/?LinkId=316373) .</span><span class="sxs-lookup"><span data-stu-id="50d83-139">[Use Cluster Shared Volumes in a Windows Server 2012 Failover Cluster](https://go.microsoft.com/fwlink/?LinkId=316373) (https://go.microsoft.com/fwlink/?LinkId=316373).</span></span>

## <a href="" id="bkmk-sqlmirroring"></a><span data-ttu-id="50d83-140">Suporte para espelhamento do Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="50d83-140">Support for Microsoft SQL Server Mirroring</span></span>


<span data-ttu-id="50d83-141">Usando o espelhamento do Microsoft SQL Server, no qual o banco de dados do servidor de gerenciamento do App-V 5,1 é espelhado usando duas instâncias do SQL Server, há suporte para bancos de dados do App-V 5,1 Management Server.</span><span class="sxs-lookup"><span data-stu-id="50d83-141">Using Microsoft SQL Server mirroring, where the App-V 5.1 management server database is mirrored utilizing two SQL Server instances, for App-V 5.1 management server databases is supported.</span></span>

<span data-ttu-id="50d83-142">Revise as informações a seguir para obter mais informações sobre como configurar o espelhamento do Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="50d83-142">Review the following for more information about configuring Microsoft SQL Server Mirroring:</span></span>

-   <span data-ttu-id="50d83-143">[Como: preparar um banco de dados espelho para espelhamento (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375) (https://go.microsoft.com/fwlink/?LinkId=316375)</span><span class="sxs-lookup"><span data-stu-id="50d83-143">[How to: Prepare a Mirror Database for Mirroring (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375) (https://go.microsoft.com/fwlink/?LinkId=316375)</span></span>

-   <span data-ttu-id="50d83-144">[Estabeleça uma sessão de espelhamento de banco de dados usando a autenticação do Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377) (https://go.microsoft.com/fwlink/?LinkId=316377)</span><span class="sxs-lookup"><span data-stu-id="50d83-144">[Establish a Database Mirroring Session Using Windows Authentication (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377) (https://go.microsoft.com/fwlink/?LinkId=316377)</span></span>

<span data-ttu-id="50d83-145">As etapas a seguir podem ser usadas para validar a configuração:</span><span class="sxs-lookup"><span data-stu-id="50d83-145">The following steps can be used to validate the configuration:</span></span>

1.  <span data-ttu-id="50d83-146">Inicie uma sessão de espelhamento do Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="50d83-146">Initiate a Microsoft SQL Server Mirroring session.</span></span>

2.  <span data-ttu-id="50d83-147">Selecione **failover** para designar uma nova instância mestra do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="50d83-147">Select **Failover** to designate a new master Microsoft SQL Server instance.</span></span>

3.  <span data-ttu-id="50d83-148">Verifique se o servidor de gerenciamento do App-V 5,1 continua funcionando como esperado após o failover.</span><span class="sxs-lookup"><span data-stu-id="50d83-148">Verify that the App-V 5.1 management server continues to function as expected after the failover.</span></span>

<span data-ttu-id="50d83-149">A cadeia de conexão no servidor de gerenciamento pode ser modificada para incluir o **parceiro de failover = &lt; &gt; Server2**.</span><span class="sxs-lookup"><span data-stu-id="50d83-149">The connection string on the management server can be modified to include **failover partner = &lt;server2&gt;**.</span></span> <span data-ttu-id="50d83-150">Isso só ajudará quando o principal no espelho tiver reprovado para o secundário e o computador executando o cliente App-V 5,1 estiver fazendo uma conexão nova (Diga após a reinicialização).</span><span class="sxs-lookup"><span data-stu-id="50d83-150">This will only help when the primary on the mirror has failed over to the secondary and the computer running the App-V 5.1 client is doing a fresh connection (say after reboot).</span></span>

<span data-ttu-id="50d83-151">Use as etapas a seguir para modificar a cadeia de conexão para incluir o **parceiro de failover = &lt; &gt; Server2**:</span><span class="sxs-lookup"><span data-stu-id="50d83-151">Use the following steps to modify the connection string to include **failover partner = &lt;server2&gt;**:</span></span>

<span data-ttu-id="50d83-152">**Importante**  Este tópico descreve como alterar o registro do Windows usando o editor do registro.</span><span class="sxs-lookup"><span data-stu-id="50d83-152">**Important** This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="50d83-153">Se você alterar o registro do Windows incorretamente, poderá causar sérios problemas que talvez exijam a reinstalação do Windows.</span><span class="sxs-lookup"><span data-stu-id="50d83-153">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="50d83-154">Você deve fazer uma cópia de backup dos arquivos do registro (System. dat e User. dat) antes de alterar o registro.</span><span class="sxs-lookup"><span data-stu-id="50d83-154">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="50d83-155">A Microsoft não pode garantir que os problemas que podem ocorrer quando você alterar o registro possam ser resolvidos.</span><span class="sxs-lookup"><span data-stu-id="50d83-155">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="50d83-156">Altere o registro por sua conta e risco.</span><span class="sxs-lookup"><span data-stu-id="50d83-156">Change the registry at your own risk.</span></span>

 

1.  <span data-ttu-id="50d83-157">Faça logon no servidor de gerenciamento e abra **regedit**.</span><span class="sxs-lookup"><span data-stu-id="50d83-157">Login to the management server and open **regedit**.</span></span>

2.  <span data-ttu-id="50d83-158">Navegue até **HKEY \ _LOCAL \ _MACHINE**  \\  **software**  \\  **Microsoft**  \\  **AppV**  \\  **Server**  \\  **ManagementService**.</span><span class="sxs-lookup"><span data-stu-id="50d83-158">Navigate to **HKEY\_LOCAL\_MACHINE** \\ **Software** \\ **Microsoft** \\ **AppV** \\ **Server** \\ **ManagementService**.</span></span>

3.  <span data-ttu-id="50d83-159">Modifique o valor de **Gerenciamento \ _SQL \ _CONNECTION \ _STRING** com o \*\*parceiro de failover = &lt; Server2 &gt; \*\*.</span><span class="sxs-lookup"><span data-stu-id="50d83-159">Modify the **MANAGEMENT\_SQL\_CONNECTION\_STRING** value with the **failover partner = &lt;server2&gt;**.</span></span>

4.  <span data-ttu-id="50d83-160">Reinicie o serviço de gerenciamento usando o console do IIS.</span><span class="sxs-lookup"><span data-stu-id="50d83-160">Restart management service using the IIS console.</span></span>

    <span data-ttu-id="50d83-161">**Observação**  O espelhamento de banco de dados está na lista de recursos de mecanismo de banco de dados substituídos do Microsoft SQL Server2012 devido ao recurso **AlwaysOn** disponível com o Microsoft SQL Server 2012.</span><span class="sxs-lookup"><span data-stu-id="50d83-161">**Note** Database Mirroring is on the list of Deprecated Database Engine Features for Microsoft SQL Server2012 due to the **AlwaysOn** feature available with Microsoft SQL Server 2012.</span></span>

     

<span data-ttu-id="50d83-162">Clique em qualquer um dos links a seguir para obter mais informações:</span><span class="sxs-lookup"><span data-stu-id="50d83-162">Click any of the following links for more information:</span></span>

-   <span data-ttu-id="50d83-163">[Como: preparar um banco de dados espelho para espelhamento (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=394235) ( https://go.microsoft.com/fwlink/?LinkId=394235) .</span><span class="sxs-lookup"><span data-stu-id="50d83-163">[How to: Prepare a Mirror Database for Mirroring (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=394235) (https://go.microsoft.com/fwlink/?LinkId=394235).</span></span>

-   <span data-ttu-id="50d83-164">[Como: configurar uma sessão de espelhamento de banco de dados (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394236) ( https://go.microsoft.com/fwlink/?LinkId=394236) .</span><span class="sxs-lookup"><span data-stu-id="50d83-164">[How to: Configure a Database Mirroring Session (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394236) (https://go.microsoft.com/fwlink/?LinkId=394236).</span></span>

-   <span data-ttu-id="50d83-165">[Estabeleça uma sessão de espelhamento de banco de dados usando a autenticação do Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394237) ( https://go.microsoft.com/fwlink/?LinkId=394237) .</span><span class="sxs-lookup"><span data-stu-id="50d83-165">[Establish a Database Mirroring Session Using Windows Authentication (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394237) (https://go.microsoft.com/fwlink/?LinkId=394237).</span></span>

-   <span data-ttu-id="50d83-166">[Recursos de mecanismo de banco de dados preteridos no SQL Server 2012](https://go.microsoft.com/fwlink/?LinkId=394238) ( https://go.microsoft.com/fwlink/?LinkId=394238) .</span><span class="sxs-lookup"><span data-stu-id="50d83-166">[Deprecated Database Engine Features in SQL Server 2012](https://go.microsoft.com/fwlink/?LinkId=394238) (https://go.microsoft.com/fwlink/?LinkId=394238).</span></span>

## <a href="" id="bkmk-sqlalwayson"></a><span data-ttu-id="50d83-167">Suporte para a configuração AlwaysOn do Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="50d83-167">Support for Microsoft SQL Server Always On configuration</span></span>


<span data-ttu-id="50d83-168">O banco de dados do aplicativo de gerenciamento do App-V 5,1 dá suporte a implantações em computadores que executam o Microsoft SQL Server com a configuração **sempre ativa** .</span><span class="sxs-lookup"><span data-stu-id="50d83-168">The App-V 5.1 management server database supports deployments to computers running Microsoft SQL Server with the **Always On** configuration.</span></span>






## <span data-ttu-id="50d83-169">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="50d83-169">Related topics</span></span>


[<span data-ttu-id="50d83-170">Planejando a implantação do App-V</span><span class="sxs-lookup"><span data-stu-id="50d83-170">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

 

 





