---
title: Como instalar um banco de dados
description: Como instalar um banco de dados
author: dansimp
ms.assetid: 52e3a19d-b7cf-4f2c-8268-0f8361cc9766
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c5f42673c08744d17e1d2e0ef955ebed2848de18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797113"
---
# <span data-ttu-id="b2504-103">Como instalar um banco de dados</span><span class="sxs-lookup"><span data-stu-id="b2504-103">How to Install a Database</span></span>


<span data-ttu-id="b2504-104">Você pode usar o procedimento a seguir para instalar um banco de dados para a implantação baseada em servidor da virtualização de aplicativos se um banco de dados ainda não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="b2504-104">You can use the following procedure to install a database for your server-based deployment of Application Virtualization if a database is not already available.</span></span> <span data-ttu-id="b2504-105">Em geral, em um ambiente de produção, você se conectará a um banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="b2504-105">Typically, in a production environment, you will connect to an existing database.</span></span>

<span data-ttu-id="b2504-106">**Importante**  Para instalar o banco de dados, você deve usar uma conta de rede com as permissões apropriadas.</span><span class="sxs-lookup"><span data-stu-id="b2504-106">**Important** To install the database, you must use a network account with the appropriate permissions.</span></span> <span data-ttu-id="b2504-107">Se a sua organização exigir que apenas administradores de banco de dados possam criar e conduzir atualizações de banco de dados, os scripts estarão disponíveis para permitir que essa tarefa seja realizada.</span><span class="sxs-lookup"><span data-stu-id="b2504-107">If your organization requires that only database administrators are allowed to create and conduct database upgrades, scripts are available that allow this task to be performed.</span></span>

 

**<span data-ttu-id="b2504-108">Para instalar um banco de dados</span><span class="sxs-lookup"><span data-stu-id="b2504-108">To install a database</span></span>**

1.  <span data-ttu-id="b2504-109">Navegue até o local do programa de configuração do sistema virtualização de aplicativos na rede, execute este programa da rede ou copie o diretório dele para o computador de destino e, em seguida, clique duas vezes em **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="b2504-109">Navigate to the location of the Application Virtualization System setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click **Setup.exe**.</span></span>

2.  <span data-ttu-id="b2504-110">Na **página de boas-vindas**, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b2504-110">On the **Welcome Page**, click **Next**.</span></span>

3.  <span data-ttu-id="b2504-111">Na página **contrato de licença** , para aceitar o contrato de licença, selecione **aceito os termos e as condições da licença**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b2504-111">On the **License Agreement** page, to accept the license agreement, select **I accept the license terms and conditions**, and click **Next**.</span></span>

4.  <span data-ttu-id="b2504-112">Na página **informações de registro** , especifique o **nome de usuário** e as informações da **organização** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b2504-112">On the **Registering Information** page, specify the **User Name** and **Organization** information, and then click **Next**.</span></span>

5.  <span data-ttu-id="b2504-113">Na página **tipo de instalação** , selecione **personalizado** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b2504-113">On the **Setup Type** page, select **Custom** and then click **Next**.</span></span>

6.  <span data-ttu-id="b2504-114">Na página **configuração personalizada** , desmarque todos os componentes do sistema do Application Virtualization, exceto o **servidor do Application Virtualization**, e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b2504-114">On the **Custom Setup** page, deselect all Application Virtualization System components except **Application Virtualization Server**, and then click **Next**.</span></span>

    <span data-ttu-id="b2504-115">**Observação**  Se um componente já estiver instalado no computador, desmarque-o na tela de **instalação personalizada** , ele será desinstalado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b2504-115">**Note** If a component is already installed on the computer, by deselecting it on the **Custom Setup** screen it will automatically be uninstalled.</span></span>

     

7.  <span data-ttu-id="b2504-116">Na página **servidor de banco de dados** , digite as senhas, atribua um caminho de instalação, salve as informações e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b2504-116">On the **Database Server** page, type the passwords, assign an installation path, save the information, and click **Next**.</span></span>

8.  <span data-ttu-id="b2504-117">Selecione um nome para o banco de dados e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b2504-117">Select a name for the database, and then click **Next**.</span></span>

    <span data-ttu-id="b2504-118">**Observação**  Se o erro 25109 for exibido quando você tentar concluir esta etapa, você terá configurado incorretamente as permissões necessárias para instalar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b2504-118">**Note** If error 25109 is displayed when you try to complete this step, you have incorrectly set up the permissions necessary to install the database.</span></span> <span data-ttu-id="b2504-119">Para obter detalhes sobre como configurar as permissões SQL necessárias, consulte <https://go.microsoft.com/fwlink/?LinkId=132144> .</span><span class="sxs-lookup"><span data-stu-id="b2504-119">For details on setting up the necessary SQL permissions, please see <https://go.microsoft.com/fwlink/?LinkId=132144>.</span></span>

     

9.  <span data-ttu-id="b2504-120">Na tela **servidor de diretório** , insira um nome de domínio e credenciais que os servidores de virtualização de aplicativos e o serviço Web de gerenciamento usarão para acessar seu controlador de domínio, salvar essas informações e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b2504-120">On the **Directory Server** screen, enter a domain name and credentials that Application Virtualization Servers and the Management Web Service will use to access your domain controller, save this information, and then click **Next**.</span></span>

    <span data-ttu-id="b2504-121">**Observação**  A instalação usará como padrão o domínio do computador atual.</span><span class="sxs-lookup"><span data-stu-id="b2504-121">**Note** The installation will default to the domain of the current computer.</span></span>

     

10. <span data-ttu-id="b2504-122">Na página **grupo de administradores** , digite o nome de um grupo que terá privilégios de administrador, salve essas informações e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b2504-122">On the **Administrator Group** page, enter the name of a group that will have Administrator privileges, save this information, and then click **Next**.</span></span>

    <span data-ttu-id="b2504-123">**Observação**  Você também pode inserir os primeiros caracteres do nome de um grupo que terão privilégios de administração, clicar em **Avançar**e, na tela **selecionar grupo administrador** , selecione o grupo na lista resultante.</span><span class="sxs-lookup"><span data-stu-id="b2504-123">**Note** You can also enter the first few characters of the name of a group that will have Administration privileges, click **Next**, and on the **Select Administrator Group** screen, select the group from the resulting list.</span></span> <span data-ttu-id="b2504-124">Em seguida, salve essas informações e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b2504-124">Then save this information and click **Next**.</span></span>

     

11. <span data-ttu-id="b2504-125">Na página **grupo de provedores padrão** , insira o nome completo de um grupo que controlará o acesso aos aplicativos, salve essas informações e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b2504-125">On the **Default Provider Group** page, enter the complete name of a group that will control access to applications, save this information, and then click **Next**.</span></span>

    <span data-ttu-id="b2504-126">**Observação**  Você também pode inserir os primeiros caracteres do nome de um grupo que controlará o acesso aos aplicativos, clique em **Avançar**e, na tela **selecionar grupo de provedor padrão** , selecione o grupo na lista.</span><span class="sxs-lookup"><span data-stu-id="b2504-126">**Note** You can also enter the first few characters of the name of a group that will control access to applications, click **Next**, and on the **Select Default Provider Group** screen, select the group in the list.</span></span> <span data-ttu-id="b2504-127">Em seguida, salve essas informações e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b2504-127">Then save this information and click **Next**.</span></span>

     

12. <span data-ttu-id="b2504-128">Na página **Assistente de instalação concluído** , para fechar o assistente, clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="b2504-128">On the **Installation Wizard Completed** page, to close the wizard, click **Finish**.</span></span>

    <span data-ttu-id="b2504-129">**Importante**  A instalação pode demorar alguns minutos para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="b2504-129">**Important** The installation can take a few minutes to finish.</span></span> <span data-ttu-id="b2504-130">Uma mensagem de status piscará acima da área de notificação da área de trabalho do Windows, indicando se a instalação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b2504-130">A status message will flash above the Windows desktop notification area, indicating whether the installation succeeded.</span></span>

     

## <span data-ttu-id="b2504-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b2504-131">Related topics</span></span>


[<span data-ttu-id="b2504-132">Como instalar os componentes de servidores e do sistema</span><span class="sxs-lookup"><span data-stu-id="b2504-132">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





