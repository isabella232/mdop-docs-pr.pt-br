---
title: Atualizando de versões anteriores do MBAM
description: Atualizando de versões anteriores do MBAM
author: dansimp
ms.assetid: 73b425cf-9cd9-4ebc-a35e-1b3bf18596ce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af45d193a5e8001288e70389ff220cb5d8269918
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799346"
---
# <span data-ttu-id="1a6a1-103">Atualizando de versões anteriores do MBAM</span><span class="sxs-lookup"><span data-stu-id="1a6a1-103">Upgrading from Previous Versions of MBAM</span></span>


<span data-ttu-id="1a6a1-104">Você pode atualizar a administração e o monitoramento do Microsoft BitLocker (MBAM) para o MBAM 2.0, com a topologia autônoma ou a topologia do Configuration Manager, fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1a6a1-104">You can upgrade Microsoft BitLocker Administration and Monitoring (MBAM) to MBAM2.0, with the Stand-alone topology or Configuration Manager topology, by doing the following:</span></span>

-   <span data-ttu-id="1a6a1-105">**Substituição manual** in-loco do servidor – para atualizar o servidor do MBAM, desinstale manualmente o MBAM usando o instalador ou o painel de controle e instale a infraestrutura do MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-105">**Manual in-place server replacement** – To upgrade the MBAM Server, manually uninstall MBAM by using either the installer or Control Panel, and then install the MBAM2.0 infrastructure.</span></span> <span data-ttu-id="1a6a1-106">Não é necessário remover os bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-106">You do not have to remove the databases.</span></span> <span data-ttu-id="1a6a1-107">Desinstalar o servidor MBAM 1,0 deixa os bancos de dados do MBAM intactos.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-107">Uninstalling the MBAM 1.0 Server leaves the MBAM databases intact.</span></span> <span data-ttu-id="1a6a1-108">Se você especificar os mesmos bancos de dados que o MBAM 1,0 estava usando, a instalação do MBAM 2.0 mantém dados do MBAM 1,0 nos bancos de dados e converte os bancos de dados para trabalhar com MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-108">If you specify the same databases that MBAM 1.0 was using, the MBAM2.0 installation retains MBAM 1.0 data in the databases and converts the databases to work with MBAM2.0.</span></span>

-   <span data-ttu-id="1a6a1-109">**Atualização do cliente distribuído** -se você estiver usando a topologia MBAM autônoma, poderá atualizar os clientes do MBAM gradualmente após a instalação da infraestrutura de servidor do MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-109">**Distributed Client Upgrade** - If you are using the Stand-alone MBAM topology, you can upgrade the MBAM Clients gradually after you install the MBAM 2.0 Server infrastructure.</span></span> <span data-ttu-id="1a6a1-110">O servidor MBAM 2,0 detecta a versão do cliente existente e executa as etapas necessárias para atualizar para o cliente 2,0.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-110">The MBAM 2.0 Server detects the version of the existing Client and performs the required steps to upgrade to the 2.0 Client.</span></span>

    <span data-ttu-id="1a6a1-111">Depois de atualizar a infraestrutura de servidor do MBAM 2,0, os clientes do MBAM 1,0 continuam a se comunicar com o servidor do MBAM 2,0 com êxito, dados de recuperação posteriores, mas a conformidade será baseada nas políticas do MBAM 1,0.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-111">After you upgrade the MBAM 2.0 Server infrastructure, MBAM 1.0 Clients continue to report to the MBAM 2.0 Server successfully, escrowing recovery data, but compliance will be based on the policies in MBAM 1.0.</span></span> <span data-ttu-id="1a6a1-112">Você deve atualizar os clientes para o MBAM 2,0 para que os computadores cliente relatem precisamente a conformidade com as políticas do MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-112">You must upgrade clients to MBAM 2.0 to have client computers accurately report compliance against the MBAM 2.0 policies.</span></span> <span data-ttu-id="1a6a1-113">Você pode atualizar os clientes para o cliente do MBAM 2,0 sem desinstalar o cliente anterior e o cliente começará a aplicar e relatar as políticas do MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-113">You can upgrade the clients to the MBAM 2.0 Client without uninstalling the previous client, and the client will start to apply and report MBAM 2.0 policies.</span></span>

    <span data-ttu-id="1a6a1-114">Se estiver usando o MBAM com o Configuration Manager, você deve atualizar os clientes do MBAM 1,0 para MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-114">If you are using MBAM with Configuration Manager, you must upgrade the MBAM 1.0 clients to MBAM 2.0.</span></span>

## <span data-ttu-id="1a6a1-115">Atualizando o MBAM a partir de uma arquitetura de dois servidores</span><span class="sxs-lookup"><span data-stu-id="1a6a1-115">Upgrading MBAM from a Two-Server Architecture</span></span>


<span data-ttu-id="1a6a1-116">Use as instruções a seguir para atualizar de uma versão anterior do MBAM quando você estiver usando uma arquitetura de dois servidores, onde um servidor está hospedando os componentes do Microsoft SQL Server, e o outro servidor está hospedando os sites e serviços.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-116">Use the following instructions to upgrade from a previous version of MBAM when you are using a two-server architecture, where one server is hosting the Microsoft SQL Server components, and the other server is hosting the websites and services.</span></span>

**<span data-ttu-id="1a6a1-117">Para atualizar o MBAM a partir de uma arquitetura de dois servidores</span><span class="sxs-lookup"><span data-stu-id="1a6a1-117">To upgrade MBAM from a two-server architecture</span></span>**

1.  <span data-ttu-id="1a6a1-118">No servidor com os recursos do SQL Server, no painel de controle, selecione **programas e recursos**e, em seguida, desinstalar **o Microsoft BitLocker Administration and Monitoring**.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-118">On the server with the SQL Server features, in Control Panel, select **Programs and Features**, and then uninstall **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="1a6a1-119">O banco de dados de recuperação e a conformidade e o banco de dados de auditoria permanecem inalterados.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-119">The Recovery Database and Compliance and Audit database remain unchanged.</span></span>

2.  <span data-ttu-id="1a6a1-120">Execute **MBAMSetup.exe** para a versão MBAM 2,0, selecione opcionalmente o **programa de aperfeiçoamento da experiência do usuário**e clique em **Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-120">Run **MBAMSetup.exe** for version MBAM 2.0, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="1a6a1-121">Leia e aceite o contrato de licença de software da Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-121">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="1a6a1-122">Na página **seleção de topologia** , **Selecione a topologia autônoma ou** de **integração do System Center Configuration Manager** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-122">On the **Topology Selection** page, select the **Stand-alone** or **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="1a6a1-123">Na página **selecionar recursos para instalar** , desmarque os recursos **servidor de autoatendimento** e **Administração e monitoramento e** clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-123">On the **Select features to install** page, clear the **Self-Service Server** and **Administration and Monitoring Server** features, and then click **Next**.</span></span>

6.  <span data-ttu-id="1a6a1-124">Aguarde até que as verificações de pré-requisitos sejam concluídas e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-124">Wait for the prerequisite checks to finish, and then click **Next**.</span></span> <span data-ttu-id="1a6a1-125">Se um pré-requisito ausente for detectado, resolva os pré-requisitos ausentes e clique em **verificar pré-requisitos novamente**.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-125">If a missing prerequisite is detected, resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span>

7.  <span data-ttu-id="1a6a1-126">Na página **fornecer conta usada para acessar a página bancos de dados do MBAM** , forneça o nome do computador para o servidor que hospedará os sites e serviços e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-126">On the **Provide account used to access the MBAM databases** page, provide the computer name for the server that will host the sites and services, and then click **Next**.</span></span>

8.  <span data-ttu-id="1a6a1-127">Na página **Configurar o banco** de dados de recuperação, especifique o nome da instância do SQL Server e o nome do banco de dados que armazenará os dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-127">On the **Configure the Recovery database** page, specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="1a6a1-128">Você também deve especificar onde os arquivos do banco de dados e as informações do log serão localizados.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-128">You must also specify where the database files and log information will be located.</span></span>

9.  <span data-ttu-id="1a6a1-129">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-129">Click **Next** to continue.</span></span>

10. <span data-ttu-id="1a6a1-130">Na página **Configurar o banco de dados de conformidade e auditoria** , especifique o nome da instância do SQL Server e o nome do banco de dados que armazenará os dados de auditoria e conformidade.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-130">On the **Configure the Compliance and Audit database** page, specify the SQL Server instance name and the name of the database that will store the compliance and audit data.</span></span>

11. <span data-ttu-id="1a6a1-131">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-131">Click **Next** to continue.</span></span>

12. <span data-ttu-id="1a6a1-132">Na página **Configurar a conformidade e os relatórios de auditoria** , especifique a instância do SQL Server Reporting Services na qual os relatórios de conformidade e auditoria serão instalados e forneça uma conta de usuário e uma senha de domínio para acessar o banco de dados de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-132">On the **Configure the Compliance and Audit Reports** page, specify the SQL Server Reporting Services instance where the Compliance and Audit reports will be installed, and provide a domain user account and password to access the Compliance and Audit database.</span></span> <span data-ttu-id="1a6a1-133">Configure a senha desta conta para nunca expirar.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-133">Configure the password for this account to never expire.</span></span> <span data-ttu-id="1a6a1-134">A conta de usuário pode acessar todos os dados disponíveis para o grupo usuários do MBAM Reports.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-134">The user account can access all data available to the MBAM Reports Users group.</span></span>

13. <span data-ttu-id="1a6a1-135">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-135">Click **Next** to continue.</span></span>

14. <span data-ttu-id="1a6a1-136">Especifique se deseja usar as atualizações da Microsoft para ajudar a manter seu computador seguro e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-136">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="1a6a1-137">Isso não ativa as atualizações automáticas no Windows.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-137">This does not turn on Automatic Updates in Windows.</span></span> <span data-ttu-id="1a6a1-138">Se você anteriormente optou por usar o Microsoft Update para este produto ou outro produto, a página Microsoft Update não será exibida.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-138">If you previously chose to use Microsoft Update for this product or another product, the Microsoft Update page does not appear.</span></span>

15. <span data-ttu-id="1a6a1-139">Na página **Resumo da instalação** , examine os recursos que serão instalados e clique em **instalar** para iniciar a instalação.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-139">On the **Installation Summary** page, review the features that will be installed, and then click **Install** to start the installation.</span></span>

**<span data-ttu-id="1a6a1-140">Para desinstalar os recursos do servidor de administração e monitoramento e concluir a atualização</span><span class="sxs-lookup"><span data-stu-id="1a6a1-140">To uninstall the Administration and Monitoring Server features and to complete the upgrade</span></span>**

1.  <span data-ttu-id="1a6a1-141">No computador que hospeda os recursos do servidor de administração e monitoramento, no painel de controle, selecione **programas e recursos**e, em seguida, desinstale o MBAM para remover os sites e serviços instalados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-141">On the computer that hosts the Administration and Monitoring Server features, in Control Panel, select **Programs and Features**, and then uninstall MBAM to remove the previously installed websites and services.</span></span>

2.  <span data-ttu-id="1a6a1-142">Execute o **MBAMSetup.exe** para a versão 2,0, selecione opcionalmente o **programa de aperfeiçoamento da experiência do usuário**e clique em **Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-142">Run the **MBAMSetup.exe** for version 2.0, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="1a6a1-143">Leia e aceite o contrato de licença de software da Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-143">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="1a6a1-144">Na página **seleção de topologia** , **Selecione a topologia autônoma ou** de **integração do System Center Configuration Manager** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-144">On the **Topology Selection** page, select the **Stand-alone** or **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="1a6a1-145">Na página **selecionar recursos para instalar** , desmarque o banco de dados de **recuperação** e os recursos de **banco de dados de auditoria** e conformidade e relatórios de **auditoria** e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-145">On the **Select features to install** page, clear the **Recovery Database** and **Compliance and Audit Database** and **Compliance and Audit Reports** features, and then click **Next**.</span></span>

6.  <span data-ttu-id="1a6a1-146">Aguarde até que as verificações de pré-requisitos sejam concluídas e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-146">Wait for the prerequisite checks to finish, and then click **Next**.</span></span> <span data-ttu-id="1a6a1-147">Se um pré-requisito ausente for detectado, resolva os pré-requisitos ausentes primeiro e clique em **verificar pré-requisitos novamente**.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-147">If a missing prerequisite is detected, resolve the missing prerequisites first, and then click **Check prerequisites again**.</span></span>

7.  <span data-ttu-id="1a6a1-148">Na página **Configurar segurança de comunicação de rede** , escolha se deseja usar a criptografia SSL (Secure Socket Layer) para os sites e serviços.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-148">On the **Configure network communication security** page, choose whether to use Secure Socket Layer (SSL) encryption for the websites and services.</span></span> <span data-ttu-id="1a6a1-149">Se você decidir criptografar a comunicação, selecione o certificado de autoridade de certificação (CA) a ser usado para criptografia.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-149">If you decide to encrypt the communication, select the certification authority (CA) certificate to use for encryption.</span></span>

    <span data-ttu-id="1a6a1-150">**Observação**  O certificado deve ser criado antes desta etapa para permitir que você o selecione nessa página.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-150">**Note** The certificate must be created before this step to enable you to select it on this page.</span></span>

     

8.  <span data-ttu-id="1a6a1-151">Na página **Configurar o local do banco de dados de status de conformidade** , especifique o nome da instância do SQL Server e o nome do banco de dados que armazena os dados de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-151">On the **Configure the location of the Compliance Status database** page, specify the SQL Server instance name and the name of the database that stores the compliance and audit data.</span></span> <span data-ttu-id="1a6a1-152">Você também deve especificar onde os arquivos do banco de dados e as informações do log serão localizados.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-152">You must also specify where the database files and log information will be located.</span></span>

9.  <span data-ttu-id="1a6a1-153">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-153">Click **Next** to continue.</span></span>

10. <span data-ttu-id="1a6a1-154">Na página **Configurar o local do banco de dados de recuperação** , especifique o nome da instância do SQL Server e o nome do banco de dados que armazena os dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-154">On the **Configure the location of the Recovery Database** page, specify the SQL Server instance name and the name of the database that stores the recovery data.</span></span>

11. <span data-ttu-id="1a6a1-155">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-155">Click **Next** to continue.</span></span>

12. <span data-ttu-id="1a6a1-156">Na página **Configurar a conformidade e os relatórios de auditoria** , insira a URL da instância de relatório que você configurou no outro servidor.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-156">On the **Configure the Compliance and Audit Reports** page, enter the URL for the reporting instance that you configured on the other server.</span></span> <span data-ttu-id="1a6a1-157">Use o botão **testar** para verificar se você pode acessar o site.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-157">Use the **Test** button to verify that you can reach the site.</span></span>

13. <span data-ttu-id="1a6a1-158">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-158">Click **Next** to continue.</span></span>

14. <span data-ttu-id="1a6a1-159">Na página **Configurar o portal de autoatendimento** , insira o número da porta, o nome do host, o nome do diretório virtual e o caminho de instalação do portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-159">On the **Configure the Self-Service Portal** page, enter the port number, host name, virtual directory name, and installation path for the Self-Service Portal.</span></span>

    <span data-ttu-id="1a6a1-160">**Observação**  O número da porta que você especificar deve ser um número de porta não usado no servidor de administração e monitoramento, a menos que você especifique um nome de cabeçalho de host exclusivo.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-160">**Note** The port number that you specify must be an unused port number on the Administration and Monitoring Server unless you specify a unique host header name.</span></span>

     

15. <span data-ttu-id="1a6a1-161">Na página **Configurar o servidor de administração e monitoramento** , especifique o diretório virtual desejado para o site de suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-161">On the **Configure the Administration and Monitoring Server** page, specify the desired virtual directory for the Help Desk website.</span></span>

16. <span data-ttu-id="1a6a1-162">Especifique se deseja usar as atualizações da Microsoft para ajudar a manter seu computador seguro e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-162">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="1a6a1-163">Esta etapa não ativa as atualizações automáticas no Windows.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-163">This step does not turn on Automatic Updates in Windows.</span></span> <span data-ttu-id="1a6a1-164">Se você anteriormente optou por usar o Microsoft Update para este produto ou outro produto, a página Microsoft Update não será exibida.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-164">If you previously chose to use Microsoft Update for this product or another product, the Microsoft Update page does not appear.</span></span>

17. <span data-ttu-id="1a6a1-165">Na página **Resumo da instalação** , examine os recursos que serão instalados e clique em **instalar** para iniciar a instalação.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-165">On the **Installation Summary** page, review the features that will be installed, and then click **Install** to start the installation.</span></span>

18. <span data-ttu-id="1a6a1-166">Para validar que a atualização foi bem-sucedida, verifique se você pode entrar em contato com cada site de outro computador do domínio.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-166">To validate that the upgrade was successful, verify that you can reach each site from another computer in the domain.</span></span>

## <span data-ttu-id="1a6a1-167">Atualizando o cliente MBAM em computadores de usuários finais</span><span class="sxs-lookup"><span data-stu-id="1a6a1-167">Upgrading the MBAM Client on End-User Computers</span></span>


<span data-ttu-id="1a6a1-168">Para atualizar os computadores de usuários finais para o cliente do MBAM 2,0, execute **MbamClientSetup.exe** em cada computador cliente.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-168">To upgrade end-user computers to the MBAM 2.0 Client, run **MbamClientSetup.exe** on each client computer.</span></span> <span data-ttu-id="1a6a1-169">O instalador atualiza automaticamente o cliente para o cliente do MBAM 2,0.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-169">The installer automatically updates the Client to the MBAM 2.0 Client.</span></span> <span data-ttu-id="1a6a1-170">Você pode instalar o cliente do MBAM por meio de um sistema de distribuição de software eletrônico, ferramentas como os serviços de domínio do Active Directory ou o System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-170">You can install the MBAM Client through an electronic software distribution system, tools such as Active Directory Domain Services or System Center Configuration Manager.</span></span>

<span data-ttu-id="1a6a1-171">Para validar a atualização do cliente, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1a6a1-171">To validate the Client upgrade, do the following:</span></span>

1.  <span data-ttu-id="1a6a1-172">Aguarde até que o ciclo de relatório configurado seja concluído e, em seguida, inicie o **SQL Server Management Studio** no computador do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-172">Wait until the configured reporting cycle is finished, and then start **SQL Server Management Studio** on the SQL Server computer.</span></span>

2.  <span data-ttu-id="1a6a1-173">No computador do SQL Server, inicie o **SQL Server Management Studio**.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-173">On the SQL Server computer, start **SQL Server Management Studio**.</span></span>

3.  <span data-ttu-id="1a6a1-174">Verifique se a tabela **RecoveryAndHardwareCore. Machines** contém uma linha que mostra o nome do computador do usuário final.</span><span class="sxs-lookup"><span data-stu-id="1a6a1-174">Verify that the **RecoveryAndHardwareCore.Machines** table contains a row that shows the end-user’s computer name.</span></span>

## <span data-ttu-id="1a6a1-175">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1a6a1-175">Related topics</span></span>


[<span data-ttu-id="1a6a1-176">Implantando o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="1a6a1-176">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)

 

 





