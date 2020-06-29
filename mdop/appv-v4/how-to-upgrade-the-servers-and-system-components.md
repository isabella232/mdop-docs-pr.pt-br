---
title: Como fazer upgrade dos componentes de servidores e do sistema
description: Como fazer upgrade dos componentes de servidores e do sistema
author: dansimp
ms.assetid: 7d8374fe-5897-452e-923e-556a854b2024
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 61f8742a2f5e3c17083a77b839dfbee85ea00e24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796922"
---
# <span data-ttu-id="bb641-103">Como fazer upgrade dos componentes de servidores e do sistema</span><span class="sxs-lookup"><span data-stu-id="bb641-103">How to Upgrade the Servers and System Components</span></span>


<span data-ttu-id="bb641-104">Use o procedimento a seguir para atualizar componentes de software instalados em todos os computadores do sistema do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="bb641-104">Use the following procedure to upgrade software components installed on all Application Virtualization System computers.</span></span> <span data-ttu-id="bb641-105">Os serviços do sistema do Application Virtualization serão reiniciados automaticamente em cada computador após a atualização.</span><span class="sxs-lookup"><span data-stu-id="bb641-105">Application Virtualization System services will be restarted automatically on each computer after it has been upgraded.</span></span>

**<span data-ttu-id="bb641-106">Observação</span><span class="sxs-lookup"><span data-stu-id="bb641-106">Note</span></span>**  
-   <span data-ttu-id="bb641-107">O processo de atualização interrompe todos os serviços do sistema do Application Virtualization, tirando o sistema de fora do serviço.</span><span class="sxs-lookup"><span data-stu-id="bb641-107">The upgrade process stops all Application Virtualization System services, thereby taking the system out of service.</span></span> <span data-ttu-id="bb641-108">As sessões de usuário devem ser desligadas antes do início do processo de atualização, e você deve parar todos os serviços de servidor de virtualização de aplicativos no seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="bb641-108">User sessions should be shut down before you begin the upgrade process, and you should stop all Application Virtualization Server services in your environment.</span></span>

-   <span data-ttu-id="bb641-109">Se você tiver mais de um servidor que está compartilhando o acesso ao banco de dados do Application Virtualization, todos esses servidores deverão ser colocados offline enquanto o banco de dados estiver sendo atualizado.</span><span class="sxs-lookup"><span data-stu-id="bb641-109">If you have more than one server that is sharing access to the Application Virtualization database, all those servers must be taken offline while the database is being upgraded.</span></span> <span data-ttu-id="bb641-110">Você deve seguir as práticas comerciais normais para a atualização do banco de dados, mas é altamente recomendável que você teste a atualização do banco de dados usando uma cópia de backup do banco de dados primeiro em um servidor de teste.</span><span class="sxs-lookup"><span data-stu-id="bb641-110">You should follow your normal business practices for the database upgrade, but it is highly advisable that you test the database upgrade by using a backup copy of the database first on a test server.</span></span> <span data-ttu-id="bb641-111">Em seguida, você deve selecionar um dos servidores para a primeira atualização, o que fará a atualização do esquema de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bb641-111">Then, you should select one of the servers for the first upgrade, which will upgrade the database schema.</span></span> <span data-ttu-id="bb641-112">Depois que o banco de dados de produção for atualizado com êxito, você poderá atualizar os outros servidores.</span><span class="sxs-lookup"><span data-stu-id="bb641-112">After the production database has been successfully upgraded, you can upgrade the other servers.</span></span>

-   <span data-ttu-id="bb641-113">Você pode atualizar para o Microsoft Application Virtualization (App-V) 4.5 somente a partir do Microsoft Application Virtualization (App-V) 4.1 ou 4.1 SP1.</span><span class="sxs-lookup"><span data-stu-id="bb641-113">You can upgrade to Microsoft Application Virtualization (App-V)4.5 only from Microsoft Application Virtualization (App-V)4.1 or4.1 SP1.</span></span> <span data-ttu-id="bb641-114">O App-V 4.0 e versões anteriores devem ser desinstalados ou atualizados para o 4.1 ou 4.1 SP1 antes da atualização para o App-V 4.5.</span><span class="sxs-lookup"><span data-stu-id="bb641-114">App-V4.0 and earlier must be uninstalled or upgraded to4.1 or4.1 SP1 before upgrading to App-V4.5.</span></span>

 

**<span data-ttu-id="bb641-115">Para atualizar componentes de software em computadores sistema do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="bb641-115">To upgrade software components on Application Virtualization System computers</span></span>**

1.  <span data-ttu-id="bb641-116">Navegue até o local do programa de instalação na rede, execute este programa da rede ou copie o diretório dele para o computador de destino e, em seguida, clique duas vezes no arquivo Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="bb641-116">Navigate to the location of the Setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click the Setup.exe file.</span></span>

2.  <span data-ttu-id="bb641-117">Na página de **boas-vindas** do assistente de instalação, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="bb641-117">On the **Welcome** page of the Installation Wizard, click **Next**.</span></span>

3.  <span data-ttu-id="bb641-118">Na página **contrato de licença** , leia o contrato de licença, marque aceito **os termos do contrato de licença**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="bb641-118">On the **License Agreement** page, read the license agreement, check **I accept the terms in the license agreement**, and click **Next**.</span></span>

4.  <span data-ttu-id="bb641-119">Quando a página **software instalado** abrir e exibir uma lista dos componentes de sistema instalados do aplicativo Virtualization e a versão de cada componente, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="bb641-119">When the **Installed Software** page opens and displays a list of the installed Application Virtualization System components and the version of each component, click **Next**.</span></span>

5.  <span data-ttu-id="bb641-120">Na página **aviso de perda de sessão** , leia a mensagem exibida e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="bb641-120">On the **Session Loss Warning** page, read the displayed message and click **Next**.</span></span>

6.  <span data-ttu-id="bb641-121">Na página **conectar-se ao banco de dados de configuração** , examine o conteúdo na página e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="bb641-121">On the **Connect to Configuration Database** page, review the content on the page and click **Next**.</span></span>

7.  <span data-ttu-id="bb641-122">Se a página de **atualização de banco de dados necessária** for exibida, será necessária uma atualização de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bb641-122">If the **Database Upgrade Required** page is displayed, a database upgrade is required.</span></span> <span data-ttu-id="bb641-123">Insira as credenciais administrativas do banco de dados e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="bb641-123">Enter the database administrative credentials, and then click **Next**.</span></span> <span data-ttu-id="bb641-124">Se essa página não for exibida, pule para a etapa 9.</span><span class="sxs-lookup"><span data-stu-id="bb641-124">If this page is not displayed, skip to Step 9.</span></span>

8.  <span data-ttu-id="bb641-125">Na página **banco de dados de configuração de backup** , marque as caixas apropriadas para executar o backup e exportá-las para um local existente e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="bb641-125">On the **Backup Configuration Database** page, check the appropriate boxes to perform the backup and export it to an existing location, and then click **Next**.</span></span>

    <span data-ttu-id="bb641-126">**Importante**  Se você quiser ser capaz de reverter para a versão anterior no caso de uma falha de atualização, verifique se você verificou a caixa **executar um backup do banco de dados de configuração** ou perderá os dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="bb641-126">**Important** If you want to be able to roll back to the previous version in the event of an upgrade failure, make sure you check the **Perform a backup of the configuration database** box, or you will lose the configuration data.</span></span>

    <span data-ttu-id="bb641-127">Quando desejar restaurar um banco de dados com o VSS, primeiro você deve parar o serviço App-V Server no servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="bb641-127">When you want to restore a database with VSS, you must first stop the App-V Server Service on the Management Server.</span></span> <span data-ttu-id="bb641-128">Isso deve ser feito em todos os servidores de gerenciamento se houver mais de um servidor conectado ao mesmo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bb641-128">This should be done on every Management server if there is more than one server connected to the same database.</span></span>

     

9.  <span data-ttu-id="bb641-129">Na primeira página de **validação do pacote** , leia o conteúdo e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="bb641-129">On the first **Package Validation** page, read the content and then click **Next**.</span></span>

10. <span data-ttu-id="bb641-130">Na segunda página de **validação do pacote** , você tem a opção de exibir os detalhes da validação do pacote em uma janela do bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="bb641-130">On the second **Package Validation** page, you have the option of displaying the details of the package validation in a Notepad window.</span></span> <span data-ttu-id="bb641-131">Para ver os detalhes, clique em **detalhes**; caso contrário, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="bb641-131">To see the details, click **Details**; otherwise, click **Next**.</span></span>

11. <span data-ttu-id="bb641-132">Na página **pronto para atualizar o programa** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="bb641-132">On the **Ready to Upgrade the Program** page, click **Next**.</span></span>

12. <span data-ttu-id="bb641-133">Na página **Assistente de instalação concluído** , clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="bb641-133">On the **Installation Wizard Completed** page, click **Finish**.</span></span>

13. <span data-ttu-id="bb641-134">Repita as etapas de 1 a 12 em todos os outros computadores em que você instalou o console de gerenciamento do Application Virtualization ou o componente do software do servidor do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="bb641-134">Repeat steps 1–12 on all other computers where you installed the Application Virtualization Management Console or the Application Virtualization Server software component.</span></span>

    <span data-ttu-id="bb641-135">Após a atualização do repositório de dados, você pode retomar a operação normal.</span><span class="sxs-lookup"><span data-stu-id="bb641-135">After upgrading the data store, you can resume normal operation.</span></span> <span data-ttu-id="bb641-136">(O repositório de dados é atualizado quando você atualiza qualquer servidor ou o serviço Web de gerenciamento do App-V.)</span><span class="sxs-lookup"><span data-stu-id="bb641-136">(The data store is upgraded when you upgrade any server or the App-V Management Web Service.)</span></span>

## <span data-ttu-id="bb641-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb641-137">Related topics</span></span>


[<span data-ttu-id="bb641-138">Considerações de atualização e implantação do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="bb641-138">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

 

 





