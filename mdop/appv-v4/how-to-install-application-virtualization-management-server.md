---
title: Como instalar o Application Virtualization Management Server
description: Como instalar o Application Virtualization Management Server
author: dansimp
ms.assetid: 8184be79-8c27-4328-a3c1-183791b5556c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfd06ee1d2448990d5a740f3d59b0e5e4b45be4d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797110"
---
# <span data-ttu-id="fb959-103">Como instalar o Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="fb959-103">How to Install Application Virtualization Management Server</span></span>


<span data-ttu-id="fb959-104">O servidor de gerenciamento do Application Virtualization publica seus aplicativos para os clientes.</span><span class="sxs-lookup"><span data-stu-id="fb959-104">The Application Virtualization Management Server publishes its applications to clients.</span></span> <span data-ttu-id="fb959-105">Em um ambiente de carga balanceada, que é típico de implantações grandes, todos os servidores em um grupo de servidores devem transmitir os mesmos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="fb959-105">In a load-balanced environment, which is typical of large deployments, all servers in a server group should stream the same applications.</span></span> <span data-ttu-id="fb959-106">Se os servidores de gerenciamento do Application Virtualization forem publicar diferentes aplicativos, atribua-os a grupos de servidores diferentes.</span><span class="sxs-lookup"><span data-stu-id="fb959-106">If Application Virtualization Management Servers are to publish different applications, assign the servers to different server groups.</span></span> <span data-ttu-id="fb959-107">Nesse caso, você também pode precisar aumentar a capacidade de um grupo de servidores.</span><span class="sxs-lookup"><span data-stu-id="fb959-107">In this case, you also might need to increase a server group's capacity.</span></span>

<span data-ttu-id="fb959-108">Se você designou um computador de destino na rede, com uma conta de logon com privilégios de administrador local, você pode usar o procedimento a seguir para instalar o servidor de gerenciamento do Application Virtualization e atribuí-lo ao grupo de servidores apropriado.</span><span class="sxs-lookup"><span data-stu-id="fb959-108">If you have designated a target computer on the network, with a login account having local Administrator privileges, you can use the following procedure to install the Application Virtualization Management Server and assign it to the appropriate server group.</span></span>

**<span data-ttu-id="fb959-109">Observação</span><span class="sxs-lookup"><span data-stu-id="fb959-109">Note</span></span>**  
<span data-ttu-id="fb959-110">O assistente de instalação pode criar um registro de grupo do servidor, se ele não existir, bem como um registro das associações do servidor de gerenciamento do Application Virtualization nesse grupo.</span><span class="sxs-lookup"><span data-stu-id="fb959-110">The Installation Wizard can create a server group record, if one does not exist, as well as a record of the Application Virtualization Management Server's membership in this group.</span></span>



<span data-ttu-id="fb959-111">Depois de concluir o processo de instalação, reinicialize o servidor.</span><span class="sxs-lookup"><span data-stu-id="fb959-111">After you complete the installation process, reboot the server.</span></span>

**<span data-ttu-id="fb959-112">Para instalar um servidor de gerenciamento do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="fb959-112">To install an Application Virtualization Management Server</span></span>**

1.  <span data-ttu-id="fb959-113">Verifique e, se necessário, desinstale as versões anteriores do servidor de gerenciamento do Application Virtualization instalada no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="fb959-113">Verify and, if necessary, uninstall previous versions of the Application Virtualization Management Server that are installed on the target computer.</span></span>

2.  <span data-ttu-id="fb959-114">Para abrir o assistente de **instalação do Microsoft Application Virtualization Management Server** , navegue até o local do programa do sistema de virtualização de aplicativos **setup.exe** na rede, execute este programa da rede ou copie o diretório dele para o computador de destino e, em seguida, clique duas vezes no arquivo **Setup.exe** .</span><span class="sxs-lookup"><span data-stu-id="fb959-114">To open the **Microsoft Application Virtualization Management Server installation** wizard, navigate to the location of the Application Virtualization System **setup.exe** program on the network, either run this program from the network or copy its directory to the target computer, and then double-click the **Setup.exe** file.</span></span>

3.  <span data-ttu-id="fb959-115">Na página de **boas-vindas** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="fb959-115">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="fb959-116">Na página **contrato de licença** , leia o contrato de licença e, para aceitar o contrato de licença, selecione **aceito os termos e as condições da licença**.</span><span class="sxs-lookup"><span data-stu-id="fb959-116">On the **License Agreement** page, read the license agreement and, to accept the license agreement, select **I accept the license terms and conditions**.</span></span> <span data-ttu-id="fb959-117">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="fb959-117">Click **Next**.</span></span>

5.  <span data-ttu-id="fb959-118">Na página **informações de registro** , você deve inserir o nome de usuário e a **organização**.</span><span class="sxs-lookup"><span data-stu-id="fb959-118">On the **Registering Information** page, you must enter the user name and the **Organization**.</span></span> <span data-ttu-id="fb959-119">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="fb959-119">Click **Next**.</span></span>

6.  <span data-ttu-id="fb959-120">Na página **tipo de instalação** , selecione **personalizado**.</span><span class="sxs-lookup"><span data-stu-id="fb959-120">On the **Setup Type** page, select **Custom**.</span></span> <span data-ttu-id="fb959-121">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="fb959-121">Click **Next**.</span></span> <span data-ttu-id="fb959-122">Na página **configuração personalizada** , desmarque todos os componentes do sistema do Application Virtualization, exceto o **servidor do Application Virtualization**, e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="fb959-122">On the **Custom Setup** page, deselect all Application Virtualization System components except **Application Virtualization Server**, and then click **Next**.</span></span>

    **<span data-ttu-id="fb959-123">Tenha</span><span class="sxs-lookup"><span data-stu-id="fb959-123">Caution</span></span>**  
    <span data-ttu-id="fb959-124">Se um componente já estiver instalado no computador, quando você desmarcar-o na janela de **instalação personalizada** , o componente será desinstalado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="fb959-124">If a component is already installed on the computer, when you deselect it in the **Custom Setup** window, the component is automatically uninstalled.</span></span>



7.  <span data-ttu-id="fb959-125">Na página **banco de dados de configuração** , selecione um servidor de banco de dados na lista de servidores disponíveis ou adicione um servidor selecionando **usar o nome de host a seguir** e especificando o **nome do servidor** e os dados do **número da porta** .</span><span class="sxs-lookup"><span data-stu-id="fb959-125">On the **Configuration Database** page, select a database server from the list of available servers or add a server by selecting **Use the following host name** and specifying the **Server Name** and **Port Number** data.</span></span> <span data-ttu-id="fb959-126">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="fb959-126">Click **Next**.</span></span>

    **<span data-ttu-id="fb959-127">Observação</span><span class="sxs-lookup"><span data-stu-id="fb959-127">Note</span></span>**  
    <span data-ttu-id="fb959-128">O servidor de gerenciamento do Application Virtualization não dá suporte a SQL que diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fb959-128">The Application Virtualization Management Server does not support case sensitive SQL.</span></span>



~~~
If a database is available, click the radio button, select the database from the list, and then click **Next**. Setup will upgrade it to this newer version. If the name does not appear in the list, enter the name in the space provided.

**Note**  
When naming a server, do not use the backslash character (/) in the server name.

If you need to install a database, see [How to Install a Database](how-to-install-a-database.md). If you would like to create a new database for this version, select **Create a new database** and specify the name that will be assigned to the new database. You can also specify a new location for the database by selecting the check box and entering the path.
~~~



8. <span data-ttu-id="fb959-129">Na página **modo de segurança de conexão** , selecione o certificado desejado na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="fb959-129">On the **Connection Security Mode** page, select the desired certificate from the drop-down list.</span></span> <span data-ttu-id="fb959-130">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="fb959-130">Click **Next**.</span></span>

   **<span data-ttu-id="fb959-131">Observação</span><span class="sxs-lookup"><span data-stu-id="fb959-131">Note</span></span>**  
   <span data-ttu-id="fb959-132">A configuração do **modo de conexão segura** exige que o servidor tenha um certificado do servidor provisionado para ele de uma infraestrutura de chave pública.</span><span class="sxs-lookup"><span data-stu-id="fb959-132">The **Secure Connection Mode** setting requires the server to have a server certificate provisioned to it from a public key infrastructure.</span></span> <span data-ttu-id="fb959-133">Se um certificado do servidor não estiver instalado no servidor, essa opção não estará disponível e não poderá ser selecionada.</span><span class="sxs-lookup"><span data-stu-id="fb959-133">If a server certificate is not installed on the server, this option is unavailable and cannot be selected.</span></span> <span data-ttu-id="fb959-134">Você deve conceder acesso de leitura à conta de serviço de rede para o certificado que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="fb959-134">You must grant the Network Service account read access to the certificate being used.</span></span>



9. <span data-ttu-id="fb959-135">Na página **configuração de porta TCP** , para usar a porta padrão (554), selecione **usar porta padrão (554)**.</span><span class="sxs-lookup"><span data-stu-id="fb959-135">On the **TCP Port Configuration** page, to use the default port (554), select **Use default port (554)**.</span></span> <span data-ttu-id="fb959-136">Para especificar uma porta personalizada, selecione **usar porta personalizada** e especifique o número da porta que será usado.</span><span class="sxs-lookup"><span data-stu-id="fb959-136">To specify a custom port, select **Use custom port** and specify the port number that will be used.</span></span> <span data-ttu-id="fb959-137">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="fb959-137">Click **Next**.</span></span>

   **<span data-ttu-id="fb959-138">Observação</span><span class="sxs-lookup"><span data-stu-id="fb959-138">Note</span></span>**  
   <span data-ttu-id="fb959-139">Ao instalar o servidor em um ambiente não seguro, você pode usar a porta padrão (554) ou pode definir uma porta personalizada.</span><span class="sxs-lookup"><span data-stu-id="fb959-139">When you install the server in a nonsecure environment, you can use the default port (554) or you can define a custom port.</span></span>



10. <span data-ttu-id="fb959-140">Na página **grupo de administradores** , especifique o nome do grupo de segurança autorizado para gerenciar esse servidor no **nome do grupo**.</span><span class="sxs-lookup"><span data-stu-id="fb959-140">On the **Administrator Group** page, specify the name of the security group authorized to manage this server in **Group Name**.</span></span> <span data-ttu-id="fb959-141">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="fb959-141">Click **Next**.</span></span> <span data-ttu-id="fb959-142">Confirme o grupo especificado e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="fb959-142">Confirm the group specified and click **Next**.</span></span>

11. <span data-ttu-id="fb959-143">Na página **grupo do provedor padrão** , especifique o nome do grupo do provedor padrão e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="fb959-143">On the **Default Provider Group** page, specify the name of the default provider group, and then click **Next**.</span></span>

12. <span data-ttu-id="fb959-144">Na página **caminho do conteúdo** , especifique o local no computador de destino em que os arquivos SFT serão salvos e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="fb959-144">On the **Content Path** page, specify the location on the target computer where SFT files will be saved, and then click **Next**.</span></span>

   **<span data-ttu-id="fb959-145">Observação</span><span class="sxs-lookup"><span data-stu-id="fb959-145">Note</span></span>**  
   <span data-ttu-id="fb959-146">Se a porta HTTP ou RTSP do servidor de gerenciamento já estiver alocada, você será solicitado a escolher uma nova porta.</span><span class="sxs-lookup"><span data-stu-id="fb959-146">If the HTTP or RTSP port for the Management Server is already allocated, you will be prompted to choose a new port.</span></span> <span data-ttu-id="fb959-147">Selecione a porta desejada e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="fb959-147">Select the desired port, and then click **Next**.</span></span>



13. <span data-ttu-id="fb959-148">Na página **pronto para instalar o programa** , para instalar o servidor de gerenciamento do Application Virtualization, clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="fb959-148">On the **Ready to Install the Program** page, to install the Application Virtualization Management Server, click **Install**.</span></span>

   **<span data-ttu-id="fb959-149">Observação</span><span class="sxs-lookup"><span data-stu-id="fb959-149">Note</span></span>**  
   <span data-ttu-id="fb959-150">Se o erro 25120 for exibido quando você tentar concluir esta etapa, será necessário habilitar os **scripts e ferramentas de gerenciamento**do IIS.</span><span class="sxs-lookup"><span data-stu-id="fb959-150">If error 25120 is displayed when you try to complete this step, you need to enable IIS **Management Scripts and Tools**.</span></span> <span data-ttu-id="fb959-151">Para habilitar esse recurso do Windows, abra o painel de controle **programas e recursos** , selecione **Ativar ou desativar recursos do Windows**e navegue até **serviços de informações da Internet.**</span><span class="sxs-lookup"><span data-stu-id="fb959-151">To enable this Windows feature, open the **Programs and Features** control panel, select **Turn Windows features on or off**, and navigate to **Internet Information Services.**</span></span>

   <span data-ttu-id="fb959-152">Em **ferramentas de gerenciamento da Web**, habilite **scripts e ferramentas de gerenciamento do IIS**.</span><span class="sxs-lookup"><span data-stu-id="fb959-152">Under **Web Management Tools**, enable **IIS Management Scripts and Tools**.</span></span>



14. <span data-ttu-id="fb959-153">Na tela **Assistente de instalação concluído** , para fechar o assistente, clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="fb959-153">On the **Installation Wizard Completed** screen, to close the wizard, click **Finish**.</span></span>

   **<span data-ttu-id="fb959-154">Importante</span><span class="sxs-lookup"><span data-stu-id="fb959-154">Important</span></span>**  
   <span data-ttu-id="fb959-155">A instalação pode demorar alguns minutos para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="fb959-155">The installation can take a few minutes to finish.</span></span> <span data-ttu-id="fb959-156">Uma mensagem de status piscará acima da área de notificação da área de trabalho do Windows, indicando que a instalação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fb959-156">A status message will flash above the Windows desktop notification area, indicating that the installation succeeded.</span></span>

   <span data-ttu-id="fb959-157">Não é necessário reinicializar o computador quando solicitado.</span><span class="sxs-lookup"><span data-stu-id="fb959-157">It is not necessary to reboot the computer when prompted.</span></span> <span data-ttu-id="fb959-158">No entanto, para otimizar o desempenho do sistema, é recomendável reinicializar.</span><span class="sxs-lookup"><span data-stu-id="fb959-158">However, to optimize system performance, a reboot is recommended.</span></span>



## <span data-ttu-id="fb959-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fb959-159">Related topics</span></span>


[<span data-ttu-id="fb959-160">Como instalar os componentes de servidores e do sistema</span><span class="sxs-lookup"><span data-stu-id="fb959-160">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)









