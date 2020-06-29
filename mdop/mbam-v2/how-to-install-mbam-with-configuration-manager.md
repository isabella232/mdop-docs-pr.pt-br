---
title: Como instalar o MBAM com o Configuration Manager
description: Como instalar o MBAM com o Configuration Manager
author: dansimp
ms.assetid: fd0832e4-3b79-4e56-9550-d2f396be6d09
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a556ce961e6a423caecdd0766cf8623383897b58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799610"
---
# <span data-ttu-id="0bb12-103">Como instalar o MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="0bb12-103">How to Install MBAM with Configuration Manager</span></span>


<span data-ttu-id="0bb12-104">Esta seção descreve as etapas para instalar o MBAM com o Configuration Manager usando a configuração recomendada, que é ilustrada em [introdução-usando o MBAM com o Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="0bb12-104">This section describes the steps to install MBAM with Configuration Manager by using the recommended configuration, which is illustrated in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span></span> <span data-ttu-id="0bb12-105">As etapas são divididas nas seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="0bb12-105">The steps are divided into the following tasks:</span></span>

-   <span data-ttu-id="0bb12-106">Instalar e configurar o MBAM no servidor do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="0bb12-106">Install and configure MBAM on the Configuration Manager Server</span></span>

-   <span data-ttu-id="0bb12-107">Instalar os bancos de dados de recuperação e auditoria no servidor de banco de dados</span><span class="sxs-lookup"><span data-stu-id="0bb12-107">Install the Recovery and Audit Databases on the Database Server</span></span>

-   <span data-ttu-id="0bb12-108">Instalar os recursos do servidor de administração e monitoramento no servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="0bb12-108">Install the Administration and Monitoring Server features on the Administration and Monitoring Server</span></span>

<span data-ttu-id="0bb12-109">Antes de começar a instalação, certifique-se de ter editado ou criado os arquivos MOF necessários.</span><span class="sxs-lookup"><span data-stu-id="0bb12-109">Before you begin the installation, ensure that you have edited or created the necessary mof files.</span></span> <span data-ttu-id="0bb12-110">Para obter instruções, consulte [como criar ou editar os arquivos MOF](how-to-create-or-edit-the-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="0bb12-110">For instructions, see [How to Create or Edit the mof Files](how-to-create-or-edit-the-mof-files.md).</span></span>

<span data-ttu-id="0bb12-111">**Importante**  Se você estiver usando uma instância do SQL Server Reporting Services (SSRS) não padrão, deverá iniciar a configuração do MBAM usando a seguinte linha de comando para especificar a instância do SSRS nomeado:</span><span class="sxs-lookup"><span data-stu-id="0bb12-111">**Important** If you are using a non-default SQL Server Reporting Services (SSRS) instance, you must start the MBAM Setup by using the following command line to specify the SSRS named instance:</span></span>

`MbamSetup.exe CM_SSRS_INSTANCE_NAME=<NamedInstance>`

 

**<span data-ttu-id="0bb12-112">Para instalar o MBAM no servidor do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="0bb12-112">To install MBAM on the Configuration Manager Server</span></span>**

1.  <span data-ttu-id="0bb12-113">No servidor do Configuration Manager, execute **MBAMSetup.exe** para iniciar o assistente de instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0bb12-113">On the Configuration Manager Server, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

    <span data-ttu-id="0bb12-114">**Observação**  Para obter os arquivos de log de instalação, você precisa usar o pacote msiexec e a opção **/l** &lt; Location &gt; para instalar o Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0bb12-114">**Note** To obtain the setup log files, you have to use the Msiexec package and the **/L** &lt;location&gt; option to install Configuration Manager.</span></span> <span data-ttu-id="0bb12-115">Os arquivos de log são criados no local que você especificar.</span><span class="sxs-lookup"><span data-stu-id="0bb12-115">Log files are created in the location that you specify.</span></span>

    <span data-ttu-id="0bb12-116">Arquivos de log de instalação adicionais são criados na pasta% temp% no computador do usuário que está instalando o Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0bb12-116">Additional setup log files are created in the %temp% folder on the computer of the user who is installing Configuration Manager.</span></span>

     

2.  <span data-ttu-id="0bb12-117">Na página de **boas-vindas** , selecione o **programa de aperfeiçoamento da experiência do usuário**e clique em **Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="0bb12-117">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="0bb12-118">Leia e aceite o contrato de licença de software da Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="0bb12-118">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="0bb12-119">Na página **seleção de topologia** , selecione **integração do System Center Configuration Manager**e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="0bb12-119">On the **Topology Selection** page, select **System Center Configuration Manager Integration**, and then click **Next**.</span></span>

5.  <span data-ttu-id="0bb12-120">Na página **selecionar recursos para instalar** , selecione a **integração do System Center Configuration Manager**.</span><span class="sxs-lookup"><span data-stu-id="0bb12-120">On the **Select features to install** page, select **System Center Configuration Manager Integration**.</span></span>

    <span data-ttu-id="0bb12-121">**Observação**  Na página **verificando pré-requisitos** , clique em **Avançar** depois que o assistente de instalação verifica os pré-requisitos para a sua instalação e confirma se nenhuma delas está ausente.</span><span class="sxs-lookup"><span data-stu-id="0bb12-121">**Note** On the **Checking Prerequisites** page, click **Next** after the installation wizard checks the prerequisites for your installation and confirms that none are missing.</span></span> <span data-ttu-id="0bb12-122">Se um pré-requisito ausente for detectado, você precisará resolver os pré-requisitos ausentes e, em seguida, clique em **verificar pré-requisitos novamente.**</span><span class="sxs-lookup"><span data-stu-id="0bb12-122">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again.**</span></span>

     

6.  <span data-ttu-id="0bb12-123">Especifique se deseja usar as atualizações da Microsoft para ajudar a manter seu computador seguro e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="0bb12-123">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="0bb12-124">Usar o Microsoft Updates não ativa as atualizações automáticas no Windows.</span><span class="sxs-lookup"><span data-stu-id="0bb12-124">Using Microsoft Updates does not turn on Automatic Updates in Windows.</span></span>

7.  <span data-ttu-id="0bb12-125">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="0bb12-125">Click **Next** to continue.</span></span>

8.  <span data-ttu-id="0bb12-126">Na página **Resumo da instalação** , examine a lista de recursos que serão instalados e clique em **instalar** para começar a instalar os recursos do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0bb12-126">On the **Installation Summary** page, review the list of features that will be installed, and click **Install** to start installing the MBAM features.</span></span> <span data-ttu-id="0bb12-127">Clique em **voltar** para voltar ao assistente se precisar revisar ou alterar as configurações de instalação ou clique em **Cancelar** para sair da instalação.</span><span class="sxs-lookup"><span data-stu-id="0bb12-127">Click **Back** to move back through the wizard if you have to review or change your installation settings, or click **Cancel** to exit Setup.</span></span> <span data-ttu-id="0bb12-128">A instalação instala os recursos do MBAM e avisa que a instalação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="0bb12-128">Setup installs the MBAM features and notifies you that the installation is completed.</span></span>

9.  <span data-ttu-id="0bb12-129">Clique em **concluir** para sair do assistente.</span><span class="sxs-lookup"><span data-stu-id="0bb12-129">Click **Finish** to exit the wizard.</span></span>

**<span data-ttu-id="0bb12-130">Para instalar os bancos de dados de recuperação e auditoria no servidor de banco de dados</span><span class="sxs-lookup"><span data-stu-id="0bb12-130">To install the Recovery and Audit Databases on the Database Server</span></span>**

1.  <span data-ttu-id="0bb12-131">No servidor de banco de dados, execute **MBAMSetup.exe** para iniciar o assistente de instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0bb12-131">On the Database Server, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="0bb12-132">Na página de **boas-vindas** , selecione o **programa de aperfeiçoamento da experiência do usuário**e clique em **Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="0bb12-132">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="0bb12-133">Leia e aceite o contrato de licença de software da Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="0bb12-133">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="0bb12-134">Na página **seleção de topologia** , selecione a topologia de **integração do System Center Configuration Manager** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="0bb12-134">On the **Topology Selection** page, select the **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="0bb12-135">Na lista de recursos a serem instalados, selecione **banco de dados de recuperação** e **banco de dados de auditoria**e desmarque os recursos restantes.</span><span class="sxs-lookup"><span data-stu-id="0bb12-135">From the list of features to install, select **Recovery Database** and **Audit Database**, and clear the remaining features.</span></span>

    <span data-ttu-id="0bb12-136">**Observação**  O assistente de instalação verifica os pré-requisitos para a sua instalação e exibe os pré-requisitos que estão faltando.</span><span class="sxs-lookup"><span data-stu-id="0bb12-136">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="0bb12-137">Se todos os pré-requisitos forem atendidos, a instalação continuará.</span><span class="sxs-lookup"><span data-stu-id="0bb12-137">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="0bb12-138">Se um pré-requisito ausente for detectado, você precisará resolver os pré-requisitos ausentes e, em seguida, clique em **verificar pré-requisitos novamente**.</span><span class="sxs-lookup"><span data-stu-id="0bb12-138">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="0bb12-139">Se todos os pré-requisitos forem atendidos desta vez, a instalação será retomada.</span><span class="sxs-lookup"><span data-stu-id="0bb12-139">If all prerequisites are met this time, the installation resumes.</span></span>

     

6.  <span data-ttu-id="0bb12-140">Na página **Configurar o banco de dados de recuperação** , especifique os nomes dos computadores que executarão o recurso de servidor de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="0bb12-140">On the **Configure the Recovery Database** page, specify the names of the computers that will be running the Administration and Monitoring Server feature.</span></span> <span data-ttu-id="0bb12-141">Após a implantação do recurso de servidor de administração e monitoramento, ele usa sua conta de domínio para se conectar ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0bb12-141">After the Administration and Monitoring Server feature is deployed, it uses its domain account to connect to the database.</span></span>

7.  <span data-ttu-id="0bb12-142">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="0bb12-142">Click **Next** to continue.</span></span>

8.  <span data-ttu-id="0bb12-143">Especifique o nome da instância do SQL Server e o nome do banco de dados que armazenará os dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="0bb12-143">Specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="0bb12-144">Você também deve especificar o local em que o banco de dados será localizado e onde as informações do log serão localizadas.</span><span class="sxs-lookup"><span data-stu-id="0bb12-144">You must also specify both where the database will be located and where the log information will be located.</span></span>

9.  <span data-ttu-id="0bb12-145">Clique em **Avançar** para continuar com o assistente de instalação de configuração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0bb12-145">Click **Next** to continue with the MBAM Setup installation wizard.</span></span>

10. <span data-ttu-id="0bb12-146">Na página **Configurar o banco de dados de auditoria** , especifique a conta de usuário que será usada para acessar o banco de dados para relatórios.</span><span class="sxs-lookup"><span data-stu-id="0bb12-146">On the **Configure the Audit Database** page, specify the user account that will be used to access the database for reports.</span></span>

11. <span data-ttu-id="0bb12-147">Especifique os nomes de computador dos computadores que executarão o servidor de administração e monitoramento e os relatórios de auditoria.</span><span class="sxs-lookup"><span data-stu-id="0bb12-147">Specify the computer names of the computers that will be running the Administration and Monitoring Server and the Audit Reports.</span></span> <span data-ttu-id="0bb12-148">Após a implantação e o monitoramento e os recursos de relatórios de auditoria serem implantados, as contas de domínio deles serão usadas para se conectar aos bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="0bb12-148">After the Administration and Monitoring and the Audit Reports features are deployed, their domain accounts will be used to connect to the databases.</span></span>

    <span data-ttu-id="0bb12-149">**Observação**  Se você estiver instalando o banco de dados de auditoria sem o recurso relatórios de auditoria, será necessário adicionar uma exceção no computador de banco de dados de auditoria para habilitar o tráfego de entrada na porta do Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0bb12-149">**Note** If you are installing the Audit Database without the Audit Reports feature, you must add an exception on the Audit Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="0bb12-150">O número da porta padrão é 1433.</span><span class="sxs-lookup"><span data-stu-id="0bb12-150">The default port number is 1433.</span></span>

     

12. <span data-ttu-id="0bb12-151">Especifique o nome da instância do SQL Server e o nome do banco de dados que armazenará os dados de auditoria.</span><span class="sxs-lookup"><span data-stu-id="0bb12-151">Specify the SQL Server instance name and the name of the database that will store the audit data.</span></span> <span data-ttu-id="0bb12-152">Você também deve especificar onde as informações do log e do banco de dados serão localizadas.</span><span class="sxs-lookup"><span data-stu-id="0bb12-152">You must also specify where the database and log information will be located.</span></span>

13. <span data-ttu-id="0bb12-153">Clique em **instalar** para iniciar a instalação e, em seguida, clique em **concluir** para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="0bb12-153">Click **Install** to start the installation, and then click **Finish** to complete the installation.</span></span>

**<span data-ttu-id="0bb12-154">Para instalar os recursos do servidor de administração e monitoramento no servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="0bb12-154">To install the Administration and Monitoring Server features on the Administration and Monitoring Server</span></span>**

1.  <span data-ttu-id="0bb12-155">No servidor de administração e monitoramento, execute **MBAMSetup.exe** para iniciar o assistente de instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0bb12-155">On the Administration and Monitoring Server, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="0bb12-156">Na página de **boas-vindas** , selecione o **programa de aperfeiçoamento da experiência do usuário**e clique em **Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="0bb12-156">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="0bb12-157">Leia e aceite o contrato de licença de software da Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="0bb12-157">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="0bb12-158">Na página **seleção de topologia** , selecione a topologia de **integração do System Center Configuration Manager** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="0bb12-158">On the **Topology Selection** page, select the **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="0bb12-159">Na lista de recursos a serem instalados, selecione **Administração e monitoramento do servidor** e do **portal de autoatendimento**e desmarque os recursos restantes.</span><span class="sxs-lookup"><span data-stu-id="0bb12-159">From the list of features to install, select **Administration and Monitoring Server** and **Self-Service Portal**, and clear the remaining features.</span></span>

    <span data-ttu-id="0bb12-160">**Observação**  O assistente de instalação verifica os pré-requisitos para a sua instalação e exibe os pré-requisitos que estão faltando.</span><span class="sxs-lookup"><span data-stu-id="0bb12-160">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="0bb12-161">Se todos os pré-requisitos forem atendidos, a instalação continuará.</span><span class="sxs-lookup"><span data-stu-id="0bb12-161">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="0bb12-162">Se um pré-requisito ausente for detectado, você precisará resolver os pré-requisitos ausentes e, em seguida, clique em **verificar pré-requisitos novamente**.</span><span class="sxs-lookup"><span data-stu-id="0bb12-162">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="0bb12-163">Se todos os pré-requisitos forem atendidos desta vez, a instalação será retomada.</span><span class="sxs-lookup"><span data-stu-id="0bb12-163">If all prerequisites are met this time, the installation resumes.</span></span>

     

6.  <span data-ttu-id="0bb12-164">Instale o portal de autoatendimento seguindo as etapas na seção **para instalar o portal** de autoatendimento em [como instalar e configurar o MBAM em servidores distribuídos](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="0bb12-164">Install the Self-Service Portal by following the steps in the **To install the Self-Service Portal** section in [How to Install and Configure MBAM on Distributed Servers](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span></span>

    <span data-ttu-id="0bb12-165">**Observação**  Se os computadores cliente não terão acesso à rede de distribuição de conteúdo (CDN) da Microsoft, que oferece ao portal de autoatendimento o acesso necessário a certos arquivos JavaScript, conclua as etapas na seção **para configurar o portal de autoatendimento quando os usuários finais não puderem acessar a seção de rede de distribuição de conteúdo da Microsoft** [como instalar e configurar o MBAM em servidores distribuídos](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md) para configurar o portal de autoatendimento para fazer referência aos arquivos JavaScript a partir de uma fonte acessível.</span><span class="sxs-lookup"><span data-stu-id="0bb12-165">**Note** If the client computers will not have access to the Microsoft Content Delivery Network (CDN), which gives the Self-Service Portal the required access to certain JavaScript files, complete the steps in the **To configure the Self-Service Portal when end users cannot access the Microsoft Content Delivery Network** section [How to Install and Configure MBAM on Distributed Servers](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md) to configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span>

     

7.  <span data-ttu-id="0bb12-166">Para instalar os recursos do servidor de administração e monitoramento, siga as etapas na seção **para instalar o recurso de servidor de administração e monitoramento** em [como instalar e configurar o MBAM em servidores distribuídos](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="0bb12-166">Install the Administration and Monitoring Server features by following the steps in the **To install the Administration and Monitoring Server feature** section in [How to Install and Configure MBAM on Distributed Servers](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span></span>

8.  <span data-ttu-id="0bb12-167">Clique em **concluir** para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="0bb12-167">Click **Finish** to complete the installation.</span></span>

## <span data-ttu-id="0bb12-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0bb12-168">Related topics</span></span>


[<span data-ttu-id="0bb12-169">Como validar a instalação do MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="0bb12-169">How to Validate the MBAM Installation with Configuration Manager</span></span>](how-to-validate-the-mbam-installation-with-configuration-manager.md)

[<span data-ttu-id="0bb12-170">Como implantar o MBAM com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="0bb12-170">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





