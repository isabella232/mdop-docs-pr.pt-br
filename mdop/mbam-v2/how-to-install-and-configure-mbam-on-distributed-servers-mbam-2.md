---
title: Como instalar e configurar o MBAM em servidores distribuídos
description: Como instalar e configurar o MBAM em servidores distribuídos
author: dansimp
ms.assetid: 67b91e6b-ae2e-4e47-9ef2-6819aba95976
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 841b894430d14604f0fd923703708d7a3f588c07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799396"
---
# <span data-ttu-id="d8793-103">Como instalar e configurar o MBAM em servidores distribuídos</span><span class="sxs-lookup"><span data-stu-id="d8793-103">How to Install and Configure MBAM on Distributed Servers</span></span>


<span data-ttu-id="d8793-104">Os procedimentos neste tópico descrevem como instalar o Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 na topologia autônoma em servidores distribuídos.</span><span class="sxs-lookup"><span data-stu-id="d8793-104">The procedures in this topic describe how to install Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 in the Stand-alone topology on distributed servers.</span></span> <span data-ttu-id="d8793-105">Para ver um diagrama da arquitetura recomendada, juntamente com uma descrição dos bancos de dados e recursos, consulte [implantando a infraestrutura de servidor MBAM 2,0](deploying-the-mbam-20-server-infrastructure-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="d8793-105">To see a diagram of the recommended architecture, along with a description of the databases and features, see [Deploying the MBAM 2.0 Server Infrastructure](deploying-the-mbam-20-server-infrastructure-mbam-2.md).</span></span> <span data-ttu-id="d8793-106">Para instalar a administração e o monitoramento do Microsoft BitLocker com a topologia do Configuration Manager, consulte [implantando o MBAM com o Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span><span class="sxs-lookup"><span data-stu-id="d8793-106">To install Microsoft BitLocker Administration and Monitoring with the Configuration Manager topology, see [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span></span>

<span data-ttu-id="d8793-107">Cada recurso do servidor tem determinados pré-requisitos.</span><span class="sxs-lookup"><span data-stu-id="d8793-107">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="d8793-108">Para verificar se você atendeu aos pré-requisitos e requisitos de hardware e software, consulte [pré-requisitos de implantação do MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md) e [MBAM 2,0 configurações compatíveis](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="d8793-108">To verify that you have met the prerequisites and hardware and software requirements, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) and [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span> <span data-ttu-id="d8793-109">Além disso, alguns recursos exigem que você forneça determinadas informações durante o processo de instalação para implantar o recurso com êxito.</span><span class="sxs-lookup"><span data-stu-id="d8793-109">In addition, some features require that you provide certain information during the installation process to successfully deploy the feature.</span></span> <span data-ttu-id="d8793-110">Você também deve analisar o [planejamento para a implantação do MBAM 2,0 Server](planning-for-mbam-20-server-deployment-mbam-2.md) antes de iniciar a implantação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8793-110">You should also review [Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md) before you start the MBAM deployment.</span></span>

**<span data-ttu-id="d8793-111">Observação</span><span class="sxs-lookup"><span data-stu-id="d8793-111">Note</span></span>**  
<span data-ttu-id="d8793-112">Para obter os arquivos de log de instalação, você precisa usar o pacote msiexec e a opção **/l** &lt; Location &gt; para instalar o MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8793-112">To obtain the setup log files, you have to use the Msiexec package and the **/L** &lt;location&gt; option to install MBAM.</span></span> <span data-ttu-id="d8793-113">Os arquivos de log são criados no local que você especificar.</span><span class="sxs-lookup"><span data-stu-id="d8793-113">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="d8793-114">Arquivos de log de instalação adicionais são criados na pasta% temp% no servidor do usuário que está instalando o MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8793-114">Additional setup log files are created in the %temp% folder on the server of the user who is installing MBAM.</span></span>



## <a href="" id="deploying-mbam-server-features-"></a><span data-ttu-id="d8793-115">Implantando recursos do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="d8793-115">Deploying MBAM Server Features</span></span>


<span data-ttu-id="d8793-116">As etapas a seguir descrevem como instalar os recursos gerais do MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8793-116">The following steps describe how to install general MBAM features.</span></span>

**<span data-ttu-id="d8793-117">Para iniciar o assistente de instalação do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="d8793-117">To start the MBAM Server installation wizard</span></span>**

1.  <span data-ttu-id="d8793-118">No servidor em que você deseja instalar a administração e o monitoramento do Microsoft BitLocker, execute **MBAMSetup.exe** para iniciar o assistente de instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8793-118">On the server where you want to install Microsoft BitLocker Administration and Monitoring, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="d8793-119">Na página de **boas-vindas** , selecione o **programa de aperfeiçoamento da experiência do usuário**e clique em **Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="d8793-119">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="d8793-120">Leia e aceite o contrato de licença de software da Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="d8793-120">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="d8793-121">Na página **seleção de topologia** , selecione a topologia **autônoma** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d8793-121">On the **Topology Selection** page, select the **Stand-alone** topology, and then click **Next**.</span></span>

    **<span data-ttu-id="d8793-122">Observação</span><span class="sxs-lookup"><span data-stu-id="d8793-122">Note</span></span>**  
    <span data-ttu-id="d8793-123">Se você quiser instalar o MBAM com a topologia integrada do Configuration Manager, consulte [implantando o MBAM com o Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span><span class="sxs-lookup"><span data-stu-id="d8793-123">If you want to install MBAM with the Configuration Manager integrated topology, see [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span></span>



5.  <span data-ttu-id="d8793-124">Selecione os recursos que você deseja instalar.</span><span class="sxs-lookup"><span data-stu-id="d8793-124">Select the features that you want to install.</span></span> <span data-ttu-id="d8793-125">Por padrão, todos os recursos do MBAM são selecionados para instalação.</span><span class="sxs-lookup"><span data-stu-id="d8793-125">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="d8793-126">Desmarque os recursos que você deseja instalar em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="d8793-126">Clear the features that you want to install elsewhere.</span></span> <span data-ttu-id="d8793-127">Os recursos que serão instalados no mesmo computador deverão ser instalados juntos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="d8793-127">Features that will be installed on the same computer must be installed together at the same time.</span></span> <span data-ttu-id="d8793-128">Você deve instalar os recursos do MBAM na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="d8793-128">You must install MBAM features in the following order:</span></span>

    -   <span data-ttu-id="d8793-129">Banco de dados de recuperação</span><span class="sxs-lookup"><span data-stu-id="d8793-129">Recovery Database</span></span>

    -   <span data-ttu-id="d8793-130">Banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="d8793-130">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="d8793-131">Relatórios de conformidade e auditoria</span><span class="sxs-lookup"><span data-stu-id="d8793-131">Compliance and Audit Reports</span></span>

    -   <span data-ttu-id="d8793-132">Portal de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="d8793-132">Self-Service Portal</span></span>

    -   <span data-ttu-id="d8793-133">Servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="d8793-133">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="d8793-134">Modelo de política de grupo MBAM</span><span class="sxs-lookup"><span data-stu-id="d8793-134">MBAM Group Policy template</span></span>

    **<span data-ttu-id="d8793-135">Observação</span><span class="sxs-lookup"><span data-stu-id="d8793-135">Note</span></span>**  
    <span data-ttu-id="d8793-136">O assistente de instalação verifica os pré-requisitos para a sua instalação e exibe os pré-requisitos que estão faltando.</span><span class="sxs-lookup"><span data-stu-id="d8793-136">The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="d8793-137">Se todos os pré-requisitos forem atendidos, a instalação continuará.</span><span class="sxs-lookup"><span data-stu-id="d8793-137">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="d8793-138">Se um pré-requisito ausente for detectado, você precisará resolver os pré-requisitos ausentes e, em seguida, clique em **verificar pré-requisitos novamente**.</span><span class="sxs-lookup"><span data-stu-id="d8793-138">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="d8793-139">Se todos os pré-requisitos forem atendidos desta vez, a instalação será retomada.</span><span class="sxs-lookup"><span data-stu-id="d8793-139">If all prerequisites are met this time, the installation resumes.</span></span>



~~~
The MBAM Setup wizard displays installation pages for the features that you select. The following sections describe the installation procedures for each feature.

**Note**  
For the following instructions, it is assumed that each feature is to be installed on a separate server. If you install multiple features on a single server, you can change or eliminate some steps.
~~~



**<span data-ttu-id="d8793-140">Para instalar o banco de dados de recuperação</span><span class="sxs-lookup"><span data-stu-id="d8793-140">To install the Recovery Database</span></span>**

1.  <span data-ttu-id="d8793-141">Na página **Configurar o banco de dados de recuperação** , especifique os nomes dos computadores que executarão o recurso de servidor de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="d8793-141">On the **Configure the Recovery database** page, specify the names of the computers that will be running the Administration and Monitoring Server feature.</span></span> <span data-ttu-id="d8793-142">Após a implantação do recurso de servidor de administração e monitoramento, ele usa sua conta de domínio para se conectar ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d8793-142">After the Administration and Monitoring Server feature is deployed, it uses its domain account to connect to the database.</span></span>

2.  <span data-ttu-id="d8793-143">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="d8793-143">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="d8793-144">Especifique o nome da instância do SQL Server e o nome do banco de dados que armazenará os dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d8793-144">Specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="d8793-145">Você também deve especificar o local em que o banco de dados será localizado e onde as informações do log serão localizadas.</span><span class="sxs-lookup"><span data-stu-id="d8793-145">You must also specify both where the database will be located and where the log information will be located.</span></span>

4.  <span data-ttu-id="d8793-146">Clique em **Avançar** para continuar com o assistente de configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8793-146">Click **Next** to continue with the MBAM Setup wizard.</span></span>

**<span data-ttu-id="d8793-147">Para instalar o banco de dados de auditoria e conformidade</span><span class="sxs-lookup"><span data-stu-id="d8793-147">To install the Compliance and Audit Database</span></span>**

1.  <span data-ttu-id="d8793-148">Na página **Configurar o banco de dados de conformidade e auditoria** , especifique a conta de usuário que será usada para acessar o banco de dados para relatórios.</span><span class="sxs-lookup"><span data-stu-id="d8793-148">On the **Configure the Compliance and Audit Database** page, specify the user account that will be used to access the database for reports.</span></span>

2.  <span data-ttu-id="d8793-149">Especifique os nomes de computador dos computadores que executarão o servidor de administração e monitoramento e os relatórios de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="d8793-149">Specify the computer names of the computers that will be running the Administration and Monitoring Server and the Compliance and Audit Reports.</span></span> <span data-ttu-id="d8793-150">Após a implantação da administração e do monitoramento e do servidor de relatórios de auditoria e conformidade, eles usam suas contas de domínio para se conectar aos bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="d8793-150">After the Administration and Monitoring and the Compliance and Audit Reports Server are deployed, they use their domain accounts to connect to the databases.</span></span>

    **<span data-ttu-id="d8793-151">Observação</span><span class="sxs-lookup"><span data-stu-id="d8793-151">Note</span></span>**  
    <span data-ttu-id="d8793-152">Se você estiver instalando o banco de dados de auditoria e conformidade sem o recurso de relatórios de auditoria e conformidade, será necessário adicionar uma exceção no computador de banco de dados de conformidade e auditoria para habilitar o tráfego de entrada na porta do Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d8793-152">If you are installing the Compliance and Audit Database without the Compliance and Audit Reports feature, you must add an exception on the Compliance and Audit Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="d8793-153">O número da porta padrão é 1433.</span><span class="sxs-lookup"><span data-stu-id="d8793-153">The default port number is 1433.</span></span>



3.  <span data-ttu-id="d8793-154">Especifique o nome da instância do SQL Server e o nome do banco de dados que armazenará os dados de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="d8793-154">Specify the SQL Server instance name and the name of the database that will store the compliance and audit data.</span></span> <span data-ttu-id="d8793-155">Você também deve especificar onde as informações do log e do banco de dados serão localizadas.</span><span class="sxs-lookup"><span data-stu-id="d8793-155">You must also specify where the database and log information will be located.</span></span>

4.  <span data-ttu-id="d8793-156">Clique em **Avançar** para continuar com o assistente de configuração de monitoramento e administração do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d8793-156">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

**<span data-ttu-id="d8793-157">Para instalar os relatórios de conformidade e auditoria</span><span class="sxs-lookup"><span data-stu-id="d8793-157">To install the Compliance and Audit Reports</span></span>**

1.  <span data-ttu-id="d8793-158">Na página **configurar os relatórios de conformidade e auditoria** , especifique o nome da instância remota do SQL Server (por exemplo, &lt; ServerName &gt; ) em que o banco de dados de auditoria e conformidade foi instalado.</span><span class="sxs-lookup"><span data-stu-id="d8793-158">On the **Configure the Compliance and Audit Reports** page, specify the remote SQL Server instance name (for example, &lt;ServerName&gt;) where the Compliance and Audit Database was installed.</span></span>

    **<span data-ttu-id="d8793-159">Observação</span><span class="sxs-lookup"><span data-stu-id="d8793-159">Note</span></span>**  
    <span data-ttu-id="d8793-160">Se você estiver instalando os relatórios de conformidade e auditoria sem o servidor de administração e monitoramento, será necessário adicionar uma exceção no computador de relatório de conformidade e auditoria para habilitar o tráfego de entrada na porta do servidor de relatório (a porta padrão é 80).</span><span class="sxs-lookup"><span data-stu-id="d8793-160">If you are installing the Compliance and Audit Reports without the Administration and Monitoring Server, you must add an exception on the Compliance and Audit Report computer to enable inbound traffic on the Reporting Server port (the default port is 80).</span></span>



2.  <span data-ttu-id="d8793-161">Especifique o nome do banco de dados de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="d8793-161">Specify the name of the Compliance and Audit Database.</span></span> <span data-ttu-id="d8793-162">Por padrão, o nome do banco de dados é MBAM status de conformidade, embora você possa alterar o nome ao instalar o banco de dados de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="d8793-162">By default, the database name is MBAM Compliance Status, although you can change the name when you install the Compliance and Audit Database.</span></span>

3.  <span data-ttu-id="d8793-163">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="d8793-163">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="d8793-164">Selecione a instância do SQL Server Reporting Services na qual os relatórios de conformidade e auditoria serão instalados.</span><span class="sxs-lookup"><span data-stu-id="d8793-164">Select the instance of SQL Server Reporting Services where the Compliance and Audit Reports will be installed.</span></span> <span data-ttu-id="d8793-165">Forneça uma conta de usuário de domínio e senha para acessar o banco de dados de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="d8793-165">Provide a domain user account and password to access the Compliance and Audit Database.</span></span> <span data-ttu-id="d8793-166">Configure a senha desta conta para nunca expirar.</span><span class="sxs-lookup"><span data-stu-id="d8793-166">Configure the password for this account to never expire.</span></span> <span data-ttu-id="d8793-167">A conta de usuário deve ser capaz de acessar todos os dados que estão disponíveis para o grupo de usuários do MBAM Reports.</span><span class="sxs-lookup"><span data-stu-id="d8793-167">The user account should be able to access all data that is available to the MBAM Reports Users group.</span></span>

5.  <span data-ttu-id="d8793-168">Clique em **Avançar** para continuar com o assistente de configuração de monitoramento e administração do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d8793-168">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

**<span data-ttu-id="d8793-169">Para instalar o portal de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="d8793-169">To install the Self-Service Portal</span></span>**

1.  <span data-ttu-id="d8793-170">Na página **Configurar o portal de autoatendimento** , você pode, opcionalmente, criptografar a comunicação entre o portal de autoatendimento e os servidores de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="d8793-170">On the **Configure the Self-Service Portal** page, you can optionally encrypt the communication between the Self-Service Portal and the Administration and Monitoring servers.</span></span> <span data-ttu-id="d8793-171">Se você escolher a opção de criptografar a comunicação, será solicitado a selecionar o certificado provisionado para a autoridade de certificação a ser usado para criptografia.</span><span class="sxs-lookup"><span data-stu-id="d8793-171">If you choose the option to encrypt the communication, you are prompted to select the certification authority-provisioned certificate to use for encryption.</span></span>

2.  <span data-ttu-id="d8793-172">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="d8793-172">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="d8793-173">Especifique a instância remota do SQL Server (por exemplo, \* &lt; ServerName &gt; \*) em que o banco de dados de auditoria e conformidade foi instalado.</span><span class="sxs-lookup"><span data-stu-id="d8793-173">Specify the remote instance of SQL Server (for example, *&lt;ServerName&gt;*) where the Compliance and Audit Database was installed.</span></span>

4.  <span data-ttu-id="d8793-174">Especifique o nome do banco de dados de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="d8793-174">Specify the name of the Compliance and Audit Database.</span></span> <span data-ttu-id="d8793-175">Por padrão, o nome do banco de dados é MBAM status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="d8793-175">By default, the database name is MBAM Compliance Status.</span></span> <span data-ttu-id="d8793-176">No entanto, você pode alterar o nome ao instalar o banco de dados de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="d8793-176">However, you can change the name when you install the Compliance and Audit Database.</span></span>

5.  <span data-ttu-id="d8793-177">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="d8793-177">Click **Next** to continue.</span></span>

6.  <span data-ttu-id="d8793-178">Especifique a instância remota do SQL Server (por exemplo, \* &lt; ServerName &gt; \*) em que o banco de dados de recuperação foi instalado.</span><span class="sxs-lookup"><span data-stu-id="d8793-178">Specify the remote instance of SQL Server (for example, *&lt;ServerName&gt;*) where the Recovery Database was installed.</span></span>

7.  <span data-ttu-id="d8793-179">Especifique o nome do banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d8793-179">Specify the name of the Recovery Database.</span></span> <span data-ttu-id="d8793-180">Por padrão, o nome do banco de dados é **MBAM recuperação e hardware**.</span><span class="sxs-lookup"><span data-stu-id="d8793-180">By default, the database name is **MBAM Recovery and Hardware**.</span></span> <span data-ttu-id="d8793-181">No entanto, você pode alterar o nome ao instalar o recurso de banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d8793-181">However, you can change the name when you install the Recovery Database feature.</span></span>

8.  <span data-ttu-id="d8793-182">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="d8793-182">Click **Next** to continue.</span></span>

9.  <span data-ttu-id="d8793-183">Digite o **número da porta**, o **nome do host** (opcional) e o caminho de **instalação** do MBAM Administration and Monitoring Server.</span><span class="sxs-lookup"><span data-stu-id="d8793-183">Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring Server.</span></span>

    **<span data-ttu-id="d8793-184">Observação</span><span class="sxs-lookup"><span data-stu-id="d8793-184">Note</span></span>**  
    <span data-ttu-id="d8793-185">O número da porta que você especificar deve ser um número de porta não usado no servidor de administração e monitoramento, a menos que você especifique um nome de cabeçalho de host exclusivo.</span><span class="sxs-lookup"><span data-stu-id="d8793-185">The port number that you specify must be an unused port number on the Administration and Monitoring server unless you specify a unique host header name.</span></span> <span data-ttu-id="d8793-186">Se você estiver usando o Firewall do Windows, a porta será aberta automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d8793-186">If you are using Windows Firewall, the port will be opened automatically.</span></span>



10. <span data-ttu-id="d8793-187">Para registrar opcionalmente um SPN (nome da entidade de serviço) para o portal de autoatendimento, selecione **registrar os nomes principais de serviço (SPN) da máquina com o Active Directory (necessário para a autenticação do Windows)**.</span><span class="sxs-lookup"><span data-stu-id="d8793-187">To optionally register a Service Principal Name (SPN) for the Self-Service Portal, select **Register this machine’s Service Principal Names (SPN) with Active Directory (Required for Windows Authentication)**.</span></span> <span data-ttu-id="d8793-188">Se você marcar esta caixa de seleção, a instalação do MBAM não tentará registrar os SPNs existentes, e você poderá registrar manualmente o SPN antes ou depois da instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8793-188">If you select this check box, MBAM Setup will not try to register the existing SPNs, and you can manually register the SPN before or after the MBAM installation.</span></span> <span data-ttu-id="d8793-189">Para obter instruções sobre como registrar o SPN manualmente, consulte [registro manual de SPN](https://go.microsoft.com/fwlink/?LinkId=286758).</span><span class="sxs-lookup"><span data-stu-id="d8793-189">For instructions on registering the SPN manually, see [Manual SPN Registration](https://go.microsoft.com/fwlink/?LinkId=286758).</span></span>

11. <span data-ttu-id="d8793-190">Clique em **Avançar** para continuar com o assistente de configuração de monitoramento e administração do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d8793-190">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

12. <span data-ttu-id="d8793-191">Especifique se deseja usar as atualizações da Microsoft para ajudar a manter seu computador seguro e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d8793-191">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span>

13. <span data-ttu-id="d8793-192">Quando as informações do recurso MBAM selecionado forem concluídas, você estará pronto para iniciar a instalação do MBAM usando o assistente de configuração.</span><span class="sxs-lookup"><span data-stu-id="d8793-192">When the selected MBAM feature information is completed, you are ready to start the MBAM installation by using the Setup wizard.</span></span> <span data-ttu-id="d8793-193">Clique em **voltar** para mover-se pelo assistente se precisar revisar ou alterar as configurações de instalação.</span><span class="sxs-lookup"><span data-stu-id="d8793-193">Click **Back** to move through the wizard if you have to review or change your installation settings.</span></span> <span data-ttu-id="d8793-194">Clique em **instalar** para iniciar a instalação.</span><span class="sxs-lookup"><span data-stu-id="d8793-194">Click **Install** to start the installation.</span></span> <span data-ttu-id="d8793-195">Clique em **Cancelar** para sair do assistente.</span><span class="sxs-lookup"><span data-stu-id="d8793-195">Click **Cancel** to exit the wizard.</span></span> <span data-ttu-id="d8793-196">A instalação instala os recursos do MBAM que você selecionou e avisa que a instalação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="d8793-196">Setup installs the MBAM features that you selected and notifies you that the installation is finished.</span></span>

14. <span data-ttu-id="d8793-197">Clique em **concluir** para sair do assistente.</span><span class="sxs-lookup"><span data-stu-id="d8793-197">Click **Finish** to exit the wizard.</span></span>

    **<span data-ttu-id="d8793-198">Observação</span><span class="sxs-lookup"><span data-stu-id="d8793-198">Note</span></span>**  
    <span data-ttu-id="d8793-199">Para configurar o portal de autoatendimento depois de instalá-lo, confira o portal de autoatendimento com o nome da sua empresa e outras informações específicas da empresa em [como marcar o portal de autoatendimento](how-to-brand-the-self-service-portal.md) para obter instruções.</span><span class="sxs-lookup"><span data-stu-id="d8793-199">To configure the Self-Service Portal after you installed it, brand the Self-Service Portal with your company name and other company-specific information, see [How to Brand the Self-Service Portal](how-to-brand-the-self-service-portal.md) for instructions.</span></span>



15. <span data-ttu-id="d8793-200">Se os computadores cliente tiverem acesso à rede de distribuição de conteúdo (CDN) da Microsoft, que fornece ao portal de autoatendimento o acesso necessário a certos arquivos JavaScript, você concluiu a instalação do portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="d8793-200">If the client computers have access to the Microsoft Content Delivery Network (CDN), which gives the Self-Service Portal the required access to certain JavaScript files, you are finished with the Self-Service Portal installation.</span></span> <span data-ttu-id="d8793-201">Se os computadores cliente não tiverem acesso à CDN da Microsoft, conclua as etapas na próxima seção para configurar o portal de autoatendimento para fazer referência aos arquivos JavaScript a partir de uma fonte acessível.</span><span class="sxs-lookup"><span data-stu-id="d8793-201">If the client computers does not have access to the Microsoft CDN, complete the steps in the next section to configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span>

**<span data-ttu-id="d8793-202">Para configurar o portal de autoatendimento quando os usuários finais não conseguem acessar a Microsoft Content Delivery Network</span><span class="sxs-lookup"><span data-stu-id="d8793-202">To configure the Self-Service Portal when end users cannot access the Microsoft Content Delivery Network</span></span>**

1. <span data-ttu-id="d8793-203">Se os computadores cliente tiverem acesso à rede de distribuição de conteúdo (CDN) da Microsoft, que fornece ao portal de autoatendimento o acesso necessário a certos arquivos JavaScript, a instalação do portal de autoatendimento está concluída.</span><span class="sxs-lookup"><span data-stu-id="d8793-203">If the client computers have access to the Microsoft Content Delivery Network (CDN), which gives the Self-Service Portal the required access to certain JavaScript files, the Self-Service Portal installation is completed.</span></span> <span data-ttu-id="d8793-204">Se os computadores cliente não tiverem acesso à CDN da Microsoft, conclua as etapas restantes desta seção para configurar o portal de autoatendimento para fazer referência aos arquivos JavaScript a partir de uma fonte acessível.</span><span class="sxs-lookup"><span data-stu-id="d8793-204">If the client computers do not have access to the Microsoft CDN, complete the remaining steps in this section to configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span>

2. <span data-ttu-id="d8793-205">Baixe os quatro arquivos JavaScript da CDN da Microsoft:</span><span class="sxs-lookup"><span data-stu-id="d8793-205">Download the four JavaScript files from the Microsoft CDN:</span></span>

   -   <span data-ttu-id="d8793-206">jQuery-1.7.2.min.js-[https://go.microsoft.com/p/fwlink/?LinkID=271736](https://go.microsoft.com/fwlink/p/?LinkID=271736)</span><span class="sxs-lookup"><span data-stu-id="d8793-206">jQuery-1.7.2.min.js - [https://go.microsoft.com/p/fwlink/?LinkID=271736](https://go.microsoft.com/fwlink/p/?LinkID=271736)</span></span>

   -   <span data-ttu-id="d8793-207">MicrosoftAjax.js –[https://go.microsoft.com/p/fwlink/?LinkId=272283](https://go.microsoft.com/fwlink/p/?LinkId=272283)</span><span class="sxs-lookup"><span data-stu-id="d8793-207">MicrosoftAjax.js –[https://go.microsoft.com/p/fwlink/?LinkId=272283](https://go.microsoft.com/fwlink/p/?LinkId=272283)</span></span>

   -   <span data-ttu-id="d8793-208">MicrosoftMvcAjax.js-[https://go.microsoft.com/p/fwlink/?LinkId=272284](https://go.microsoft.com/fwlink/p/?LinkId=272284)</span><span class="sxs-lookup"><span data-stu-id="d8793-208">MicrosoftMvcAjax.js - [https://go.microsoft.com/p/fwlink/?LinkId=272284](https://go.microsoft.com/fwlink/p/?LinkId=272284)</span></span>

   -   <span data-ttu-id="d8793-209">MicrosoftMvcValidation.js-</span><span class="sxs-lookup"><span data-stu-id="d8793-209">MicrosoftMvcValidation.js -</span></span> <https://go.microsoft.com/fwlink/p/?LinkId=272285>

3. <span data-ttu-id="d8793-210">Copie os arquivos JavaScript para o diretório **scripts** do portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="d8793-210">Copy the JavaScript files to the **Scripts** directory of the Self-Service Portal.</span></span> <span data-ttu-id="d8793-211">Esse diretório está localizado no <em> &lt; MBAM Self-Service &gt; \\ </em> Website\\Scripts. Self-Service Directory</span><span class="sxs-lookup"><span data-stu-id="d8793-211">This directory is located in <em>&lt;MBAM Self-Service Install Directory&gt;\\</em>Self Service Website\\Scripts.</span></span>

4. <span data-ttu-id="d8793-212">Abra o **Gerenciador dos serviços de informações da Internet (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="d8793-212">Open **Internet Information Services (IIS) Manager**.</span></span>

5. <span data-ttu-id="d8793-213">Expanda **sites** &gt; **Administração e monitoramento do Microsoft BitLocker**e realce **SelfService**.</span><span class="sxs-lookup"><span data-stu-id="d8793-213">Expand **Sites** &gt; **Microsoft BitLocker Administration and Monitoring**, and highlight **SelfService**.</span></span>

   **<span data-ttu-id="d8793-214">Observação</span><span class="sxs-lookup"><span data-stu-id="d8793-214">Note</span></span>**  
   <span data-ttu-id="d8793-215">*SelfService* é o nome do diretório virtual padrão.</span><span class="sxs-lookup"><span data-stu-id="d8793-215">*SelfService* is the default virtual directory name.</span></span> <span data-ttu-id="d8793-216">Se você tiver escolhido um nome diferente para esse diretório durante a instalação, lembre-se de substituir *SelfService* no restante dessas instruções com o nome escolhido.</span><span class="sxs-lookup"><span data-stu-id="d8793-216">If you chose a different name for this directory during installation, remember to replace *SelfService* in the rest of these instructions with the name you chose.</span></span>



6. <span data-ttu-id="d8793-217">No painel do meio, clique duas vezes em **configurações do aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="d8793-217">In the middle pane, double-click **Application Settings**.</span></span>

7. <span data-ttu-id="d8793-218">Para cada item na lista a seguir, edite as configurações do aplicativo para referenciar o novo local substituindo o &lt; diretório virtual &gt; por/SelfService/(ou o nome escolhido durante a instalação).</span><span class="sxs-lookup"><span data-stu-id="d8793-218">For each item in the following list, edit the application settings to reference the new location by replacing &lt;virtual directory&gt; with /SelfService/ (or the name you chose during installation).</span></span> <span data-ttu-id="d8793-219">Por exemplo, o caminho do diretório virtual será semelhante a jquery-1.7.2.min.js/selfservice/scripts/.</span><span class="sxs-lookup"><span data-stu-id="d8793-219">For example, the virtual directory path will be similar to /selfservice/scripts/jquery-1.7.2.min.js.</span></span>

   -   <span data-ttu-id="d8793-220">jQueryPath:/ &lt; diretório virtual &gt; /scripts/jQuery-1.7.2.min.js</span><span class="sxs-lookup"><span data-stu-id="d8793-220">jQueryPath: /&lt;virtual directory&gt;/Scripts/ jQuery-1.7.2.min.js</span></span>

   -   <span data-ttu-id="d8793-221">MicrosoftAjaxPath:/ &lt; diretório virtual &gt; /scripts/MicrosoftAjax.js</span><span class="sxs-lookup"><span data-stu-id="d8793-221">MicrosoftAjaxPath: /&lt;virtual directory&gt;/Scripts/ MicrosoftAjax.js</span></span>

   -   <span data-ttu-id="d8793-222">MicrosoftMvcAjaxPath:/ &lt; diretório virtual &gt; /scripts/MicrosoftMvcAjax.js</span><span class="sxs-lookup"><span data-stu-id="d8793-222">MicrosoftMvcAjaxPath: /&lt;virtual directory&gt;/Scripts/ MicrosoftMvcAjax.js</span></span>

   -   <span data-ttu-id="d8793-223">MicrosoftMvcValidationPath:/ &lt; diretório virtual &gt; /scripts/MicrosoftMvcValidation.js</span><span class="sxs-lookup"><span data-stu-id="d8793-223">MicrosoftMvcValidationPath: /&lt;virtual directory&gt;/Scripts/ MicrosoftMvcValidation.js</span></span>

**<span data-ttu-id="d8793-224">Para instalar o recurso do servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="d8793-224">To install the Administration and Monitoring Server feature</span></span>**

1. <span data-ttu-id="d8793-225">O MBAM pode criptografar a comunicação entre os serviços Web e os servidores de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="d8793-225">MBAM can encrypt the communication between the Web Services and the Administration and Monitoring servers.</span></span> <span data-ttu-id="d8793-226">Se você escolher a opção de criptografar a comunicação, será solicitado a selecionar o certificado provisionado para a autoridade de certificação a ser usado para criptografia.</span><span class="sxs-lookup"><span data-stu-id="d8793-226">If you choose the option to encrypt the communication, you are prompted to select the certification authority-provisioned certificate to use for encryption.</span></span>

2. <span data-ttu-id="d8793-227">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="d8793-227">Click **Next** to continue.</span></span>

3. <span data-ttu-id="d8793-228">Especifique a instância remota do SQL Server (por exemplo: \* &lt; ServerName &gt; \*) em que o banco de dados de auditoria e conformidade foi instalado.</span><span class="sxs-lookup"><span data-stu-id="d8793-228">Specify the remote instance of SQL Server (for example: *&lt;ServerName&gt;*) where the Compliance and Audit Database was installed.</span></span>

4. <span data-ttu-id="d8793-229">Especifique o nome do banco de dados de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="d8793-229">Specify the name of the Compliance and Audit Database.</span></span> <span data-ttu-id="d8793-230">Por padrão, o nome do banco de dados é MBAM status de conformidade.</span><span class="sxs-lookup"><span data-stu-id="d8793-230">By default, the database name is MBAM Compliance Status.</span></span> <span data-ttu-id="d8793-231">No entanto, você pode alterar o nome ao instalar o banco de dados de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="d8793-231">However, you can change the name when you install the Compliance and Audit Database.</span></span>

5. <span data-ttu-id="d8793-232">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="d8793-232">Click **Next** to continue.</span></span>

6. <span data-ttu-id="d8793-233">Especifique a instância remota do SQL Server (por exemplo: \* &lt; nomedoservidor &gt; \*) em que o banco de dados de recuperação foi instalado.</span><span class="sxs-lookup"><span data-stu-id="d8793-233">Specify the remote instance of SQL Server (for example: *&lt;ServerName&gt;*) where the Recovery Database was installed.</span></span>

7. <span data-ttu-id="d8793-234">Especifique o nome do banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d8793-234">Specify the name of the Recovery Database.</span></span> <span data-ttu-id="d8793-235">Por padrão, o nome do banco de dados é **MBAM recuperação e hardware**.</span><span class="sxs-lookup"><span data-stu-id="d8793-235">By default, the database name is **MBAM Recovery and Hardware**.</span></span> <span data-ttu-id="d8793-236">No entanto, você pode alterar o nome ao instalar o recurso de banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d8793-236">However, you can change the name when you install the Recovery Database feature.</span></span>

8. <span data-ttu-id="d8793-237">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="d8793-237">Click **Next** to continue.</span></span>

9. <span data-ttu-id="d8793-238">Especifique a URL para a "página inicial" do site do SQL Server Reporting Services (SRS).</span><span class="sxs-lookup"><span data-stu-id="d8793-238">Specify the URL for the “Home” of the SQL Server Reporting Services (SRS) site.</span></span> <span data-ttu-id="d8793-239">O local padrão Home de uma instância do site do SQL Server Reporting Services está em:</span><span class="sxs-lookup"><span data-stu-id="d8793-239">The default Home location of a SQL Server Reporting Services site instance is at:</span></span>

   <span data-ttu-id="d8793-240">http:// <em> &lt; NameofMBAMReportsServer &gt; / </em> ReportServer</span><span class="sxs-lookup"><span data-stu-id="d8793-240">http://<em>&lt;NameofMBAMReportsServer&gt;/</em>ReportServer</span></span>

   **<span data-ttu-id="d8793-241">Observação</span><span class="sxs-lookup"><span data-stu-id="d8793-241">Note</span></span>**  
   <span data-ttu-id="d8793-242">Se o SQL Server Reporting Services foi configurado como uma instância nomeada, a URL é semelhante à seguinte: http://\* &lt; NameofMBAMReportsServer &gt; */ReportServer\_* &lt; SRSInstanceName &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="d8793-242">If SQL Server Reporting Services was configured as a named instance, the URL resembles the following: http://*&lt;NameofMBAMReportsServer&gt;*/ReportServer\_*&lt;SRSInstanceName&gt;*.</span></span>



10. <span data-ttu-id="d8793-243">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="d8793-243">Click **Next** to continue.</span></span>

11. <span data-ttu-id="d8793-244">Digite o **número da porta**, o **nome do host** (opcional) e o caminho de **instalação** do MBAM Administration and Monitoring Server.</span><span class="sxs-lookup"><span data-stu-id="d8793-244">Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring Server.</span></span>

    **<span data-ttu-id="d8793-245">Observação</span><span class="sxs-lookup"><span data-stu-id="d8793-245">Note</span></span>**  
    <span data-ttu-id="d8793-246">O número da porta que você especificar deve ser um número de porta não usado no servidor de administração e monitoramento, a menos que você especifique um nome de cabeçalho de host exclusivo.</span><span class="sxs-lookup"><span data-stu-id="d8793-246">The port number that you specify must be an unused port number on the Administration and Monitoring server unless you specify a unique host header name.</span></span> <span data-ttu-id="d8793-247">Se você estiver usando o Firewall do Windows, a porta será aberta automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d8793-247">If you are using Windows Firewall, the port will be opened automatically.</span></span>



12. <span data-ttu-id="d8793-248">Para registrar opcionalmente um SPN (nome da entidade de serviço) para o portal de autoatendimento, selecione **registrar os nomes principais de serviço (SPN) da máquina com o Active Directory (necessário para a autenticação do Windows)**.</span><span class="sxs-lookup"><span data-stu-id="d8793-248">To optionally register a Service Principal Name (SPN) for the Self-Service Portal, select **Register this machine’s Service Principal Names (SPN) with Active Directory (Required for Windows Authentication)**.</span></span> <span data-ttu-id="d8793-249">Se você marcar esta caixa de seleção, a instalação do MBAM não tentará registrar os SPNs existentes, e você poderá registrar manualmente o SPN antes ou depois da instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8793-249">If you select this check box, MBAM Setup will not try to register the existing SPNs, and you can manually register the SPN before or after the MBAM installation.</span></span> <span data-ttu-id="d8793-250">Para obter instruções sobre como registrar o SPN manualmente, consulte [registro manual de SPN](https://go.microsoft.com/fwlink/?LinkId=286758).</span><span class="sxs-lookup"><span data-stu-id="d8793-250">For instructions on registering the SPN manually, see [Manual SPN Registration](https://go.microsoft.com/fwlink/?LinkId=286758).</span></span>

13. <span data-ttu-id="d8793-251">Clique em **Avançar** para continuar com o assistente de configuração de monitoramento e administração do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d8793-251">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

14. <span data-ttu-id="d8793-252">Especifique se deseja usar as atualizações da Microsoft para ajudar a manter seu computador seguro e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d8793-252">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span>

15. <span data-ttu-id="d8793-253">Quando as informações do recurso MBAM selecionado forem concluídas, você estará pronto para iniciar a instalação do MBAM usando o assistente de configuração.</span><span class="sxs-lookup"><span data-stu-id="d8793-253">When the selected MBAM feature information is completed, you are ready to start the MBAM installation by using the Setup wizard.</span></span> <span data-ttu-id="d8793-254">Clique em **voltar** para mover-se pelo assistente se precisar revisar ou alterar as configurações de instalação.</span><span class="sxs-lookup"><span data-stu-id="d8793-254">Click **Back** to move through the wizard if you have to review or change your installation settings.</span></span> <span data-ttu-id="d8793-255">Clique em **instalar** para a instalação.</span><span class="sxs-lookup"><span data-stu-id="d8793-255">Click **Install** to being the installation.</span></span> <span data-ttu-id="d8793-256">Clique em **Cancelar** para sair do assistente.</span><span class="sxs-lookup"><span data-stu-id="d8793-256">Click **Cancel** to exit the wizard.</span></span> <span data-ttu-id="d8793-257">A instalação instala os recursos do MBAM que você selecionou e avisa que a instalação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="d8793-257">Setup installs the MBAM features that you selected and notifies you that the installation is finished.</span></span>

16. <span data-ttu-id="d8793-258">Clique em **concluir** para sair do assistente.</span><span class="sxs-lookup"><span data-stu-id="d8793-258">Click **Finish** to exit the wizard.</span></span>

**<span data-ttu-id="d8793-259">Para executar a configuração pós-instalação</span><span class="sxs-lookup"><span data-stu-id="d8793-259">To perform post-installation configuration</span></span>**

1.  <span data-ttu-id="d8793-260">No servidor de administração e monitoramento, adicione usuários aos grupos locais a seguir para dar a eles acesso aos recursos no site Administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8793-260">On the Administration and Monitoring Server, add users to the following local groups to give them access to the features on the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="d8793-261">**Usuários da assistência técnica do MBAM**: os membros desse grupo local podem acessar os recursos de recuperação de unidade e gerenciamento de TPM no site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8793-261">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="d8793-262">Todos os campos na recuperação de unidade e no gerenciamento de TPM são campos obrigatórios para um usuário da assistência técnica.</span><span class="sxs-lookup"><span data-stu-id="d8793-262">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="d8793-263">**MBAM usuários avançados da assistência técnica**: os membros desse grupo local têm acesso avançado aos recursos de recuperação de unidade e gerenciamento de TPM no site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8793-263">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="d8793-264">Para os usuários avançados da assistência técnica, somente o campo ID da chave é necessário na recuperação de unidade.</span><span class="sxs-lookup"><span data-stu-id="d8793-264">For Advanced Helpdesk Users, only the Key ID field is required in Drive Recovery.</span></span> <span data-ttu-id="d8793-265">Em **gerenciar TPM**, somente os campos **domínio do computador** e nome do **computador** são necessários.</span><span class="sxs-lookup"><span data-stu-id="d8793-265">In **Manage TPM**, only the **Computer Domain** field and **Computer Name** field are required.</span></span>

2.  <span data-ttu-id="d8793-266">No servidor que hospeda o servidor de administração e monitoramento e o banco de dados de conformidade e auditoria e no servidor que hospeda os relatórios de conformidade e auditoria, adicione usuários ao grupo local a seguir para dar a eles acesso ao recurso relatórios no site Administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8793-266">On the server that hosts Administration and Monitoring Server and the Compliance and Audit Database and on the server that hosts the Compliance and Audit Reports, add users to the following local group to give them access to the Reports feature on the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="d8793-267">**Usuários de relatório MBAM**: os membros desse grupo local podem acessar os relatórios no site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8793-267">**MBAM Report Users**: Members of this local group can access the reports on the MBAM Administration and Monitoring website.</span></span>

    **<span data-ttu-id="d8793-268">Observação</span><span class="sxs-lookup"><span data-stu-id="d8793-268">Note</span></span>**  
    <span data-ttu-id="d8793-269">Associações de usuário ou de grupo idênticas do grupo local **usuários do relatório MBAM** devem ser mantidas em todos os computadores nos quais os recursos de servidor administração e monitoramento do MBAM, banco de dados de conformidade e auditoria e os relatórios de conformidade e auditoria estejam instalados.</span><span class="sxs-lookup"><span data-stu-id="d8793-269">Identical user or group membership of the **MBAM Report Users** local group must be maintained on all computers where the MBAM Administration and Monitoring Server features, Compliance and Audit Database, and the Compliance and Audit Reports are installed.</span></span>



## <span data-ttu-id="d8793-270">Validando a instalação de recursos do servidor MBAM</span><span class="sxs-lookup"><span data-stu-id="d8793-270">Validating the MBAM Server Feature Installation</span></span>


<span data-ttu-id="d8793-271">Quando a instalação do recurso Microsoft BitLocker Administration and Monitoring Server estiver concluída, recomendamos que você valide se a instalação configurou com êxito todos os recursos necessários para o MBAM.</span><span class="sxs-lookup"><span data-stu-id="d8793-271">When Microsoft BitLocker Administration and Monitoring Server feature installation is completed, we recommend that you validate that the installation has successfully set up all the necessary features for MBAM.</span></span> <span data-ttu-id="d8793-272">Use o procedimento a seguir para confirmar se o serviço de administração e monitoramento do Microsoft BitLocker está funcionando.</span><span class="sxs-lookup"><span data-stu-id="d8793-272">Use the following procedure to confirm that the Microsoft BitLocker Administration and Monitoring service is functional.</span></span>

**<span data-ttu-id="d8793-273">Para validar uma instalação do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="d8793-273">To validate an MBAM Server installation</span></span>**

1. <span data-ttu-id="d8793-274">Em cada servidor em que um recurso MBAM é implantado, abra o **painel de controle**, selecione **programas**e **programas e recursos**.</span><span class="sxs-lookup"><span data-stu-id="d8793-274">On each server where an MBAM feature is deployed, open **Control Panel**, select **Programs**, and then select **Programs and Features**.</span></span> <span data-ttu-id="d8793-275">Verifique se a **Administração e o monitoramento do Microsoft BitLocker** aparecem na lista **programas e recursos** .</span><span class="sxs-lookup"><span data-stu-id="d8793-275">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="d8793-276">Observação</span><span class="sxs-lookup"><span data-stu-id="d8793-276">Note</span></span>**  
   <span data-ttu-id="d8793-277">Para validar a instalação do MBAM, você deve usar uma conta de domínio que tenha credenciais administrativas do computador local em cada servidor.</span><span class="sxs-lookup"><span data-stu-id="d8793-277">To validate the MBAM installation, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2. <span data-ttu-id="d8793-278">No servidor em que o banco de dados de recuperação está instalado, abra o SQL Server Management Studio e verifique se o banco de dados de **recuperação e hardware do MBAM** está instalado.</span><span class="sxs-lookup"><span data-stu-id="d8793-278">On the server where the Recovery Database is installed, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="d8793-279">No servidor em que o banco de dados de conformidade e auditoria está instalado, abra o SQL Server Management Studio e verifique se o **banco de dados de status de conformidade do MBAM** está instalado.</span><span class="sxs-lookup"><span data-stu-id="d8793-279">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio and verify that the **MBAM Compliance Status Database** is installed.</span></span>

4. <span data-ttu-id="d8793-280">No servidor em que os relatórios de conformidade e auditoria estiverem instalados, abra um navegador da Web com credenciais administrativas e navegue até a "página inicial" do site do SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="d8793-280">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative credentials and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="d8793-281">O local Home padrão de uma instância de site do SQL Server Reporting Services pode ser encontrado em http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /reports.aspx.</span><span class="sxs-lookup"><span data-stu-id="d8793-281">The default Home location of a SQL Server Reporting Services site instance can be found is at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.aspx.</span></span> <span data-ttu-id="d8793-282">Para localizar a URL real, use a ferramenta Gerenciador de configuração do Reporting Services e selecione as instâncias que foram especificadas durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="d8793-282">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances that were specified during setup.</span></span>

   <span data-ttu-id="d8793-283">Confirme se uma pasta de relatórios denominada **Administração e administração do Microsoft BitLocker** contém uma fonte de dados chamada **MaltaDataSource** e se uma pasta **en-US** contém quatro relatórios.</span><span class="sxs-lookup"><span data-stu-id="d8793-283">Confirm that a reports folder named **Microsoft BitLocker Administration and Monitoring** contains a data source called **MaltaDataSource** and that an **en-us** folder contains four reports.</span></span>

   **<span data-ttu-id="d8793-284">Observação</span><span class="sxs-lookup"><span data-stu-id="d8793-284">Note</span></span>**  
   <span data-ttu-id="d8793-285">Se o SQL Server Reporting Services foi configurado como uma instância nomeada, a URL deve ser semelhante à seguinte: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="d8793-285">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following:http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. <span data-ttu-id="d8793-286">No servidor em que o recurso administração e monitoramento estiver instalado, execute o **Gerenciador de servidores** e navegue até **funções**.</span><span class="sxs-lookup"><span data-stu-id="d8793-286">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**.</span></span> <span data-ttu-id="d8793-287">Selecione **servidor Web (IIS)** e, em seguida, clique em **Gerenciador dos serviços de informações da Internet (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="d8793-287">Select **Web Server (IIS)**, and then click **Internet Information Services (IIS) Manager**.</span></span>

6. <span data-ttu-id="d8793-288">Em **conexões**, navegue até \* &lt; NomeDoComputador &gt; \*, selecione **sites**e selecione **Administração e monitoramento do Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="d8793-288">In **Connections**, browse to *&lt;computername&gt;*, select **Sites**, and select **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="d8793-289">Verifique se **MBAMAdministrationService**, **MBAMComplianceStatusService**e **MBAMRecoveryAndHardwareService** estão listados.</span><span class="sxs-lookup"><span data-stu-id="d8793-289">Verify that **MBAMAdministrationService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

7. <span data-ttu-id="d8793-290">No servidor em que os recursos de administração e monitoramento e o portal de autoatendimento estão instalados, abra um navegador da Web com credenciais administrativas e navegue até os seguintes locais para verificar se eles são carregados com êxito.</span><span class="sxs-lookup"><span data-stu-id="d8793-290">On the server where the Administration and Monitoring features and Self-Service Portal are installed, open a web browser with administrative credentials and browse to the following locations to verify that they load successfully.</span></span>

   **<span data-ttu-id="d8793-291">Observação</span><span class="sxs-lookup"><span data-stu-id="d8793-291">Note</span></span>**  
   <span data-ttu-id="d8793-292">As URLs terminadas em ". svc" não exibem um site.</span><span class="sxs-lookup"><span data-stu-id="d8793-292">The URLs ending in “.svc” do not display a website.</span></span> <span data-ttu-id="d8793-293">O sucesso é indicado pela mensagem "a publicação de metadados para este serviço está atualmente desabilitada" ou por informações semelhantes a um código.</span><span class="sxs-lookup"><span data-stu-id="d8793-293">Success is indicated by the message “Metadata publishing for this service is currently disabled” or by information resembling code.</span></span> <span data-ttu-id="d8793-294">Se você vir outra mensagem de erro ou se não for possível encontrar a página, a página não será carregada com êxito.</span><span class="sxs-lookup"><span data-stu-id="d8793-294">If you see some other error message or if the page cannot be found, the page has not loaded successfully.</span></span>



~~~
-   *http://&lt;hostname&gt;/HelpDesk/default.aspx* and confirm each of the links for navigation and reports

-   *http://&lt;hostname&gt;/SelfService&gt;/*

-   *http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc*

-   *http://&lt;hostname&gt;/MBAMUserSupportService/UserSupportService.svc*

-   *http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc*

-   *http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc*

**Note**  
It is assumed that the server features were installed on the default port without network encryption. If you installed the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example, *http://&lt;hostname&gt;:&lt;port&gt;/HelpDesk/default.aspx* or*http://&lt;hostname&gt;:&lt;port&gt;/&lt;virtualdirectory&gt;/default.aspx*

If the server features were installed with network encryption, change http:// to https://.
~~~



8. <span data-ttu-id="d8793-295">Verifique se cada página da Web foi carregada com êxito.</span><span class="sxs-lookup"><span data-stu-id="d8793-295">Verify that each webpage loads successfully.</span></span>

## <span data-ttu-id="d8793-296">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d8793-296">Related topics</span></span>


[<span data-ttu-id="d8793-297">Implantação da infraestrutura de servidor do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="d8793-297">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









