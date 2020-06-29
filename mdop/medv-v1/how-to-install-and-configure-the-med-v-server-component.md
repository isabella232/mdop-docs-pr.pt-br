---
title: Como instalar e configurar o componente de servidor do MED-V
description: Como instalar e configurar o componente de servidor do MED-V
author: dansimp
ms.assetid: 2d3c5b15-df2c-4ab6-bf78-f47ef8ae7418
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4fb0cc5c9ffe76e987e316d0285f172dd0b76578
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799980"
---
# <span data-ttu-id="01d55-103">Como instalar e configurar o componente de servidor do MED-V</span><span class="sxs-lookup"><span data-stu-id="01d55-103">How to Install and Configure the MED-V Server Component</span></span>


<span data-ttu-id="01d55-104">Esta seção explica como [instalar](#bkmk-howtoinstallthemedvserver) e [Configurar](#bkmk-howtoconfigurethemedvserver) o servidor MED-V.</span><span class="sxs-lookup"><span data-stu-id="01d55-104">This section explains how to [install](#bkmk-howtoinstallthemedvserver) and [configure](#bkmk-howtoconfigurethemedvserver) the MED-V server.</span></span>

## <a href="" id="bkmk-howtoinstallthemedvserver"></a><span data-ttu-id="01d55-105">Como instalar o servidor MED-V</span><span class="sxs-lookup"><span data-stu-id="01d55-105">How to Install the MED-V Server</span></span>


**<span data-ttu-id="01d55-106">Para instalar o servidor MED-V</span><span class="sxs-lookup"><span data-stu-id="01d55-106">To install the MED-V server</span></span>**

1.  <span data-ttu-id="01d55-107">Instale o pacote MED-V Server. msi.</span><span class="sxs-lookup"><span data-stu-id="01d55-107">Install the MED-V Server .msi package.</span></span>

    <span data-ttu-id="01d55-108">O pacote MED-V Server. msi é chamado *MED-V\_Server\_x.msi*, em que x é o número da versão.</span><span class="sxs-lookup"><span data-stu-id="01d55-108">The MED-V Server .msi package is called *MED-V\_Server\_x.msi*, where x is the version number.</span></span>

    <span data-ttu-id="01d55-109">Por exemplo, *MED-V\_Server\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="01d55-109">For example, *MED-V\_Server\_1.0.65.msi*.</span></span>

2.  <span data-ttu-id="01d55-110">Quando a tela de **boas-vindas do Assistente InstallShield** for exibida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="01d55-110">When the **InstallShield Wizard Welcome** screen appears, click **Next**.</span></span>

3.  <span data-ttu-id="01d55-111">Na tela **contrato de licença** , leia o contrato de licença, clique em **aceito os termos do contrato de licença**e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="01d55-111">On the **License Agreement** screen, read the license agreement, click **I accept the terms in the license agreement**, and then click **Next**.</span></span>

    <span data-ttu-id="01d55-112">A tela de **pasta de destino** será exibida, com a pasta de instalação padrão exibida.</span><span class="sxs-lookup"><span data-stu-id="01d55-112">The **Destination Folder** screen appears, with the default installation folder displayed.</span></span>

    <span data-ttu-id="01d55-113">A pasta de instalação padrão é *%systemdrive%\\Program Files\\Microsoft Enterprise Desktop Virtualization\\*.</span><span class="sxs-lookup"><span data-stu-id="01d55-113">The default installation folder is *%systemdrive%\\Program Files\\Microsoft Enterprise Desktop Virtualization\\*.</span></span>

    -   <span data-ttu-id="01d55-114">Para alterar a pasta em que o MED-V deve ser instalado, clique em **alterar** e navegue até uma pasta existente.</span><span class="sxs-lookup"><span data-stu-id="01d55-114">To change the folder where MED-V should be installed, click **Change** and browse to an existing folder.</span></span>

4.  <span data-ttu-id="01d55-115">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="01d55-115">Click **Next**.</span></span>

5.  <span data-ttu-id="01d55-116">Na tela **pronto para instalar o programa** , clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="01d55-116">On the **Ready to Install the Program** screen, click **Install**.</span></span>

    <span data-ttu-id="01d55-117">A instalação do servidor MED-V é iniciada.</span><span class="sxs-lookup"><span data-stu-id="01d55-117">The MED-V server installation starts.</span></span> <span data-ttu-id="01d55-118">Isso pode levar alguns minutos, e a tela pode não exibir texto.</span><span class="sxs-lookup"><span data-stu-id="01d55-118">This can take several minutes, and the screen might not display text.</span></span> <span data-ttu-id="01d55-119">Durante a instalação, várias telas de progresso são exibidas.</span><span class="sxs-lookup"><span data-stu-id="01d55-119">During installation, several progress screens appear.</span></span> <span data-ttu-id="01d55-120">Se aparecer uma mensagem, siga as instruções fornecidas.</span><span class="sxs-lookup"><span data-stu-id="01d55-120">If a message appears, follow the instructions provided.</span></span>

6.  <span data-ttu-id="01d55-121">Quando a tela **Assistente InstallShield concluído** for exibida, clique em **concluir** para concluir o assistente.</span><span class="sxs-lookup"><span data-stu-id="01d55-121">When the **InstallShield Wizard Completed** screen appears, click **Finish** to complete the wizard.</span></span>

**<span data-ttu-id="01d55-122">Observação</span><span class="sxs-lookup"><span data-stu-id="01d55-122">Note</span></span>**  
<span data-ttu-id="01d55-123">Se você estiver instalando o servidor MED-V pela área de trabalho remota da Microsoft, use a seguinte sintaxe: **mstsc/administrador**. Certifique-se de que sua sessão RDP seja direcionada ao console.</span><span class="sxs-lookup"><span data-stu-id="01d55-123">If you are installing the MED-V server via Microsoft Remote Desktop, use the following syntax: **mstsc/admin**. Ensure that your RDP session is directed to the console.</span></span>



## <a href="" id="bkmk-howtoconfigurethemedvserver"></a><span data-ttu-id="01d55-124">Como configurar o servidor MED-V</span><span class="sxs-lookup"><span data-stu-id="01d55-124">How to Configure the MED-V Server</span></span>


<span data-ttu-id="01d55-125">As seguintes configurações do servidor podem ser configuradas:</span><span class="sxs-lookup"><span data-stu-id="01d55-125">The following server settings can be configured:</span></span>

-   [<span data-ttu-id="01d55-126">Connections</span><span class="sxs-lookup"><span data-stu-id="01d55-126">Connections</span></span>](#bkmk-configuringconnections)

-   [<span data-ttu-id="01d55-127">Images</span><span class="sxs-lookup"><span data-stu-id="01d55-127">Images</span></span>](#bkmk-configuringimages)

-   [<span data-ttu-id="01d55-128">Permissões</span><span class="sxs-lookup"><span data-stu-id="01d55-128">Permissions</span></span>](#bkmk-configuringpermissions)

-   [<span data-ttu-id="01d55-129">Relatórios</span><span class="sxs-lookup"><span data-stu-id="01d55-129">Reports</span></span>](#bkmk-configuringreports)

### <a href="" id="bkmk-configuringconnections"></a><span data-ttu-id="01d55-130">Configurar conexões</span><span class="sxs-lookup"><span data-stu-id="01d55-130">Configuring Connections</span></span>

**<span data-ttu-id="01d55-131">Para configurar conexões</span><span class="sxs-lookup"><span data-stu-id="01d55-131">To configure connections</span></span>**

1.  <span data-ttu-id="01d55-132">No menu Iniciar do Windows, selecione **todos os programas &gt; med-v &gt; med-v Server Configuration Manager**.</span><span class="sxs-lookup"><span data-stu-id="01d55-132">On the Windows Start menu, select **All Programs &gt; MED-V &gt; MED-V Server Configuration Manager**.</span></span>

    **<span data-ttu-id="01d55-133">Observação</span><span class="sxs-lookup"><span data-stu-id="01d55-133">Note</span></span>**  
    <span data-ttu-id="01d55-134">Observação: se você tiver marcado a caixa de seleção **iniciar o Gerenciador de configuração do MED-v Server** durante a instalação do servidor, o Gerenciador de configuração do MED-v Server será iniciado automaticamente após a conclusão da instalação do servidor.</span><span class="sxs-lookup"><span data-stu-id="01d55-134">Note: If you selected the **Launch MED-V Server Configuration Manager** check box during the server installation, the MED-V server configuration manager starts automatically after the server installation is complete.</span></span>



~~~
The MED-V Server Configuration Manager appears.
~~~

2. <span data-ttu-id="01d55-135">Na guia **conexões** , defina as seguintes configurações de conexões de cliente:</span><span class="sxs-lookup"><span data-stu-id="01d55-135">On the **Connections** tab, configure the following client connections settings:</span></span>

   -   <span data-ttu-id="01d55-136">**Habilitar conexões não criptografadas (http), usando a porta**— Marque esta caixa de seleção para habilitar conexões não criptografadas usando uma porta especificada.</span><span class="sxs-lookup"><span data-stu-id="01d55-136">**Enable unencrypted connections (http), using port**—Select this check box to enable unencrypted connections using a specified port.</span></span> <span data-ttu-id="01d55-137">Na caixa porta, insira a porta do servidor na qual aceitar conexões não criptografadas (http).</span><span class="sxs-lookup"><span data-stu-id="01d55-137">In the port box, enter the server port on which to accept unencrypted connections (http).</span></span>

   -   <span data-ttu-id="01d55-138">**Habilitar conexões criptografadas (https), usando porta**— Marque esta caixa de seleção para habilitar conexões criptografadas usando uma porta especificada.</span><span class="sxs-lookup"><span data-stu-id="01d55-138">**Enable encrypted connections (https), using port**—Select this check box to enable encrypted connections using a specified port.</span></span> <span data-ttu-id="01d55-139">Na caixa porta, insira a porta do servidor na qual aceitar conexões criptografadas (https).</span><span class="sxs-lookup"><span data-stu-id="01d55-139">In the port box, enter the server port on which to accept encrypted connections (https).</span></span>

       <span data-ttu-id="01d55-140">HTTPS é uma configuração opcional que pode ser definida para garantir transações seguras entre o servidor MED-V e os clientes do MED-V.</span><span class="sxs-lookup"><span data-stu-id="01d55-140">Https is an optional configuration which can be set to ensure secure transactions between the MED-V server and MED-V clients.</span></span> <span data-ttu-id="01d55-141">Para configurar o HTTPS, você deve executar os seguintes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="01d55-141">To configure https, you must perform the following procedures:</span></span>

       -   <span data-ttu-id="01d55-142">Configurar um certificado no servidor.</span><span class="sxs-lookup"><span data-stu-id="01d55-142">Configure a certificate on the server.</span></span>

       -   <span data-ttu-id="01d55-143">Associe o certificado do servidor à porta especificada usando Netsh.</span><span class="sxs-lookup"><span data-stu-id="01d55-143">Associate the server certificate with the port specified using netsh.</span></span> <span data-ttu-id="01d55-144">Para obter informações, consulte os seguintes artigos:</span><span class="sxs-lookup"><span data-stu-id="01d55-144">For information, see the following:</span></span>

           -   [<span data-ttu-id="01d55-145">Comandos netsh para HTTP (Hypertext Transfer Protocol)</span><span class="sxs-lookup"><span data-stu-id="01d55-145">Netsh Commands for Hypertext Transfer Protocol (HTTP)</span></span>](https://go.microsoft.com/fwlink/?LinkId=183314)

           -   [<span data-ttu-id="01d55-146">Como: configurar uma porta com um certificado SSL</span><span class="sxs-lookup"><span data-stu-id="01d55-146">How to: Configure a Port with an SSL Certificate</span></span>](https://go.microsoft.com/fwlink/?LinkID=183315)

           -   [<span data-ttu-id="01d55-147">Como: configurar uma porta com um certificado SSL</span><span class="sxs-lookup"><span data-stu-id="01d55-147">How to: Configure a Port with an SSL Certificate</span></span>](https://msdn.microsoft.com/library/ms733791.aspx)

3. <span data-ttu-id="01d55-148">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="01d55-148">Click **OK**.</span></span>

### <a href="" id="bkmk-configuringimages"></a><span data-ttu-id="01d55-149">Configurando imagens</span><span class="sxs-lookup"><span data-stu-id="01d55-149">Configuring Images</span></span>

**<span data-ttu-id="01d55-150">Para configurar imagens</span><span class="sxs-lookup"><span data-stu-id="01d55-150">To configure images</span></span>**

1.  <span data-ttu-id="01d55-151">Clique na guia **imagens** .</span><span class="sxs-lookup"><span data-stu-id="01d55-151">Click the **Images** tab.</span></span>

2.  <span data-ttu-id="01d55-152">Defina as seguintes configurações de gerenciamento de imagens:</span><span class="sxs-lookup"><span data-stu-id="01d55-152">Configure the following image management settings:</span></span>

    -   <span data-ttu-id="01d55-153">**Diretório VMs**— diretório da máquina virtual (o diretório onde as imagens estão armazenadas).</span><span class="sxs-lookup"><span data-stu-id="01d55-153">**VMs Directory**—The virtual machine directory (the directory where the images are stored).</span></span> <span data-ttu-id="01d55-154">Este campo contém um caminho UNC para o diretório de imagens no servidor de distribuição de imagens que deve ser acessado do servidor MED-V.</span><span class="sxs-lookup"><span data-stu-id="01d55-154">This field contains a UNC path to the image directory on the image distribution server that should be accessible from the MED-V server.</span></span>

    -   <span data-ttu-id="01d55-155">**URL de VMs**— o local do servidor onde as imagens estão armazenadas.</span><span class="sxs-lookup"><span data-stu-id="01d55-155">**VMs URL**—The location of the server where the images are stored.</span></span>

3.  <span data-ttu-id="01d55-156">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="01d55-156">Click **OK**.</span></span>

### <a href="" id="bkmk-configuringpermissions"></a><span data-ttu-id="01d55-157">Configurando permissões</span><span class="sxs-lookup"><span data-stu-id="01d55-157">Configuring Permissions</span></span>

**<span data-ttu-id="01d55-158">Para configurar permissões</span><span class="sxs-lookup"><span data-stu-id="01d55-158">To configure permissions</span></span>**

1.  <span data-ttu-id="01d55-159">Clique na guia **permissões** .</span><span class="sxs-lookup"><span data-stu-id="01d55-159">Click the **Permissions** tab.</span></span>

2.  <span data-ttu-id="01d55-160">Uma lista de todos os usuários que podem fazer logon é fornecida.</span><span class="sxs-lookup"><span data-stu-id="01d55-160">A list of all users who can log in is provided.</span></span> <span data-ttu-id="01d55-161">Para aplicar as permissões de leitura e gravação a um usuário, marque a caixa de seleção ao lado do usuário.</span><span class="sxs-lookup"><span data-stu-id="01d55-161">To apply read and write permissions to a user, select the check box next to the user.</span></span> <span data-ttu-id="01d55-162">Para aplicar permissões somente leitura a um usuário, desmarque a caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="01d55-162">To apply read-only permissions to a user, clear the check box.</span></span>

3.  <span data-ttu-id="01d55-163">Para adicionar usuários ou grupos de domínio, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="01d55-163">To add domain users or groups, click **Add**.</span></span>

    <span data-ttu-id="01d55-164">A caixa de diálogo **Inserir nomes de usuário ou grupo** é exibida.</span><span class="sxs-lookup"><span data-stu-id="01d55-164">The **Enter User or Group names** dialog box appears.</span></span>

    1.  <span data-ttu-id="01d55-165">Selecione usuários ou grupos do domínio seguindo um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="01d55-165">Select domain users or groups by doing one of the following:</span></span>

        -   <span data-ttu-id="01d55-166">No campo **Inserir nomes de usuário ou grupo** , digite um usuário ou grupo que exista no domínio ou exista como um usuário ou grupo local no computador.</span><span class="sxs-lookup"><span data-stu-id="01d55-166">In the **Enter User or Group names** field, type a user or group that exists in the domain or exists as a local user or group on the computer.</span></span> <span data-ttu-id="01d55-167">Em seguida, clique em **verificar nomes** para resolvê-lo para o nome completo existente.</span><span class="sxs-lookup"><span data-stu-id="01d55-167">Then click **Check Names** to resolve it to the full existent name.</span></span>

        -   <span data-ttu-id="01d55-168">Clique em **Localizar** para abrir a caixa de diálogo **Selecionar usuários ou grupos** padrão.</span><span class="sxs-lookup"><span data-stu-id="01d55-168">Click **Find** to open the standard **Select Users or Groups** dialog box.</span></span> <span data-ttu-id="01d55-169">Em seguida, selecione usuários ou grupos do domínio.</span><span class="sxs-lookup"><span data-stu-id="01d55-169">Then select domain users or groups.</span></span>

    2.  <span data-ttu-id="01d55-170">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="01d55-170">Click **OK**.</span></span>

4.  <span data-ttu-id="01d55-171">Para remover usuários ou grupos de domínio, selecione um usuário ou grupo e clique em **remover**.</span><span class="sxs-lookup"><span data-stu-id="01d55-171">To remove domain users or groups, select a user or group and click **Remove**.</span></span>

5.  <span data-ttu-id="01d55-172">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="01d55-172">Click **OK**.</span></span>

### <a href="" id="bkmk-configuringreports"></a><span data-ttu-id="01d55-173">Configurando relatórios</span><span class="sxs-lookup"><span data-stu-id="01d55-173">Configuring Reports</span></span>

**<span data-ttu-id="01d55-174">Para configurar relatórios</span><span class="sxs-lookup"><span data-stu-id="01d55-174">To configure reports</span></span>**

1.  <span data-ttu-id="01d55-175">Clique na guia **relatórios** .</span><span class="sxs-lookup"><span data-stu-id="01d55-175">Click the **Reports** tab.</span></span>

2.  <span data-ttu-id="01d55-176">Para dar suporte a relatórios, selecione **habilitar relatórios**.</span><span class="sxs-lookup"><span data-stu-id="01d55-176">To support reports, select **Enable reports**.</span></span>

3.  <span data-ttu-id="01d55-177">Na caixa **cadeia de conexão** , insira uma cadeia de conexão para o banco de dados MSSQL.</span><span class="sxs-lookup"><span data-stu-id="01d55-177">In the **Connection String** box, enter a connection string for the MSSQL database.</span></span>

    -   <span data-ttu-id="01d55-178">Quando o SQL Server estiver instalado em um servidor remoto, use a seguinte cadeia de conexão:</span><span class="sxs-lookup"><span data-stu-id="01d55-178">When SQL Server is installed on a remote server, use the following connection string:</span></span>

        `Data Source=<ServerName>;Initial Catalog=<DBName>;uid=sa;pwd=<Password>;`

        **<span data-ttu-id="01d55-179">Observação</span><span class="sxs-lookup"><span data-stu-id="01d55-179">Note</span></span>**  
        <span data-ttu-id="01d55-180">Observação: para se conectar ao SQL Express, use:</span><span class="sxs-lookup"><span data-stu-id="01d55-180">Note: To connect to SQL Express, use:</span></span> `Data Source=<ServerName>\sqlexpress.`



4.  <span data-ttu-id="01d55-181">Para criar o banco de dados, clique em **criar banco de dados**.</span><span class="sxs-lookup"><span data-stu-id="01d55-181">To create the database, click **Create Database**.</span></span>

5.  <span data-ttu-id="01d55-182">Para testar a conexão, clique em **testar conexão**.</span><span class="sxs-lookup"><span data-stu-id="01d55-182">To test the connection, click **Test Connection**.</span></span>

6.  <span data-ttu-id="01d55-183">Para configurar as opções de compensação do banco de dados, clique em **limpar opções**.</span><span class="sxs-lookup"><span data-stu-id="01d55-183">To configure database clearing options, click **Clear Options**.</span></span>

    <span data-ttu-id="01d55-184">A caixa de diálogo **limpar opções de banco de dados** é exibida.</span><span class="sxs-lookup"><span data-stu-id="01d55-184">The **Clear Database Options** dialog box appears.</span></span>

    1.  <span data-ttu-id="01d55-185">Escolha uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="01d55-185">Choose one of the following options:</span></span>

        -   <span data-ttu-id="01d55-186">**Limpar dados mais antigos do que**: limpar todos os dados anteriores ao número de dias especificado; na caixa número, insira um número de dias.</span><span class="sxs-lookup"><span data-stu-id="01d55-186">**Clear data older than**—Clear all data older than the number of days specified; in the number box, enter a number of days.</span></span>

        -   <span data-ttu-id="01d55-187">**Limpar todos os dados do banco de**dados — limpar todos os dados existentes no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="01d55-187">**Clear all data from database**—Clear all existent data in the database.</span></span>

        -   <span data-ttu-id="01d55-188">**Remover banco de dados**— excluir o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="01d55-188">**Drop database**—Delete the database.</span></span>

    2.  <span data-ttu-id="01d55-189">Clique em **OK** para aplicar as alterações e fechar a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="01d55-189">Click **OK** to apply changes and close the dialog box.</span></span>

7.  <span data-ttu-id="01d55-190">Clique em **OK** para salvar as alterações ou clique em **Cancelar** para fechar a caixa de diálogo sem salvar as alterações.</span><span class="sxs-lookup"><span data-stu-id="01d55-190">Click **OK** to save the changes, or click **Cancel** to close the dialog box without saving changes.</span></span>

8.  <span data-ttu-id="01d55-191">Se solicitado, reinicie o serviço do servidor MED-V para aplicar as alterações nas configurações de rede.</span><span class="sxs-lookup"><span data-stu-id="01d55-191">If prompted, restart the MED-V server service to apply changes to the network settings.</span></span>

## <span data-ttu-id="01d55-192">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01d55-192">Related topics</span></span>


[<span data-ttu-id="01d55-193">Configurações com suporte</span><span class="sxs-lookup"><span data-stu-id="01d55-193">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

[<span data-ttu-id="01d55-194">Projetar a infraestrutura de servidor do MED-V</span><span class="sxs-lookup"><span data-stu-id="01d55-194">Design the MED-V Server Infrastructure</span></span>](design-the-med-v-server-infrastructure.md)









