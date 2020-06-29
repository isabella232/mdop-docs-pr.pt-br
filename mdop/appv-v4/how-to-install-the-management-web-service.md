---
title: Como instalar o Management Web Service
description: Como instalar o Management Web Service
author: dansimp
ms.assetid: cac296f5-8ca0-4ce7-afdb-859ae207d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b8cc1b4821cb4041d75003cf7e6ff592e1c5039
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797093"
---
# <span data-ttu-id="4ba85-103">Como instalar o Management Web Service</span><span class="sxs-lookup"><span data-stu-id="4ba85-103">How to Install the Management Web Service</span></span>


<span data-ttu-id="4ba85-104">Use o procedimento a seguir para instalar o serviço Web de gerenciamento do Application Virtualization em um computador de destino na rede, com uma conta de logon com privilégios administrativos locais.</span><span class="sxs-lookup"><span data-stu-id="4ba85-104">Use the following procedure to install the Application Virtualization Management Web Service on a target computer on the network, with a logon account having local administrative privileges.</span></span> <span data-ttu-id="4ba85-105">Embora não seja necessário, recomendamos que você instale esse componente em seu servidor Web.</span><span class="sxs-lookup"><span data-stu-id="4ba85-105">Although it is not required, we recommended that you install this component on your Web server.</span></span>

**<span data-ttu-id="4ba85-106">Para instalar o serviço Web de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4ba85-106">To install the Management Web Service</span></span>**

1.  <span data-ttu-id="4ba85-107">Verifique se nenhuma versão anterior do serviço Web do Application Virtualization está instalada em seu computador de destino.</span><span class="sxs-lookup"><span data-stu-id="4ba85-107">Verify that no previous versions of the Application Virtualization Web Service are installed on your target computer.</span></span>

2.  <span data-ttu-id="4ba85-108">Navegue até o local do programa de configuração do sistema virtualização de aplicativos na rede, execute este programa da rede ou copie o diretório dele para o computador de destino e, em seguida, clique duas vezes em **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="4ba85-108">Navigate to the location of the Application Virtualization System setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click **Setup.exe**.</span></span>

3.  <span data-ttu-id="4ba85-109">Depois que o assistente de instalação abrir, na página de **boas-vindas** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4ba85-109">After the Installation Wizard opens, on the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="4ba85-110">Na página **contrato de licença** , para aceitar o contrato de licença, selecione **aceito os termos e as condições da licença**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4ba85-110">On the **License Agreement** page, to accept the license agreement, select **I accept the license terms and conditions**, and then click **Next**.</span></span>

5.  <span data-ttu-id="4ba85-111">Na página **informações de registro** , especifique o **nome de usuário** e as informações da organização e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4ba85-111">On the **Registration Information** page, specify the **User Name** and organization information, and then click **Next**.</span></span>

6.  <span data-ttu-id="4ba85-112">Na página **tipo de instalação** , clique em **personalizado**e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4ba85-112">On the **Setup Type** page, click **Custom**, and then click **Next**.</span></span>

    <span data-ttu-id="4ba85-113">**Observação**  Se esse não for o primeiro componente que você instalou neste computador, a página **manutenção do programa** será exibida.</span><span class="sxs-lookup"><span data-stu-id="4ba85-113">**Note** If this is not the first component you installed on this computer, the **Program Maintenance** page is displayed.</span></span> <span data-ttu-id="4ba85-114">Na página **manutenção do programa** , clique em **Modificar**.</span><span class="sxs-lookup"><span data-stu-id="4ba85-114">On the **Program Maintenance** page, click **Modify**.</span></span>

     

7.  <span data-ttu-id="4ba85-115">Na página **configuração personalizada** , desmarque todos os componentes do sistema do Application Virtualization, exceto o **serviço de gerenciamento do App Virt**, e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4ba85-115">On the **Custom Setup** page, clear all Application Virtualization System components except **App Virt Management Service**, and then click **Next**.</span></span>

    <span data-ttu-id="4ba85-116">**Observação**  Se um componente já estiver instalado no computador, desmarcá-lo na página de **instalação personalizada** , ele será desinstalado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="4ba85-116">**Note** If a component is already installed on the computer, by clearing it on the **Custom Setup** page, you will automatically uninstall it.</span></span>

     

8.  <span data-ttu-id="4ba85-117">Na página **servidor de banco de dados** , clique em **conectar a um banco de dados disponível**e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4ba85-117">On the **Database Server** page, click **Connect to available database**, and then click **Next**.</span></span>

    <span data-ttu-id="4ba85-118">**Observação**  Em um ambiente de produção, a Microsoft pressupõe que você se conectará a um banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="4ba85-118">**Note** In a production environment, Microsoft assumes that you will connect to an existing database.</span></span> <span data-ttu-id="4ba85-119">Se você quiser instalar um banco de dados, consulte [como instalar um banco de dados](how-to-install-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="4ba85-119">If you want to install a database, see [How to Install a Database](how-to-install-a-database.md).</span></span> <span data-ttu-id="4ba85-120">Após instalar o banco de dados, continue com a etapa 13.</span><span class="sxs-lookup"><span data-stu-id="4ba85-120">After installing the database, continue with step 13.</span></span>

     

9.  <span data-ttu-id="4ba85-121">Na página **tipo de servidor de banco de dados** , selecione um tipo de banco de dados na lista e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4ba85-121">On the **Database Server Type** page, select a database type from the list, and then click **Next**.</span></span>

10. <span data-ttu-id="4ba85-122">Na página **local do servidor de banco de dados** , selecione um servidor de banco de dados na lista de servidores disponíveis ou adicione um servidor marcando a caixa de seleção **usar o seguinte nome de host** e inserindo informações nas caixas nome do **servidor** e **número da porta** e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4ba85-122">On the **Database Server Location** page, select a database server from the list of available servers or add a server by selecting the **Use the following host name** check box and entering information in the **Server Name** and **Port Number** boxes, and then click **Next**.</span></span>

11. <span data-ttu-id="4ba85-123">Na página **Selecionar Banco de dados** , selecione o banco de dados desejado e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4ba85-123">On the **Select Database** page, select the database you want, and then click **Next**.</span></span>

12. <span data-ttu-id="4ba85-124">Na página **configuração do usuário do banco** de dados, insira as credenciais que o serviço Web de gerenciamento usará para acessar o repositório de dados e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4ba85-124">On the **Database User Configuration** page, enter the credentials that the Management Web Service will use to access the data store, and then click **Next**.</span></span>

13. <span data-ttu-id="4ba85-125">Na página **pronto para modificar o programa** , clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="4ba85-125">On the **Ready to Modify the Program** page, click **Install**.</span></span>

    <span data-ttu-id="4ba85-126">**Observação**  Se este for o primeiro componente que você instalar, a página **pronto para instalar o programa** será exibida.</span><span class="sxs-lookup"><span data-stu-id="4ba85-126">**Note** If this is the first component you install, the **Ready to Install the Program** page is displayed.</span></span> <span data-ttu-id="4ba85-127">Na página, clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="4ba85-127">On the page, click **Install**.</span></span>

     

14. <span data-ttu-id="4ba85-128">Na página **Assistente de instalação concluído** , clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="4ba85-128">On the **Installation Wizard Completed** page, click **Finish**.</span></span>

## <span data-ttu-id="4ba85-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4ba85-129">Related topics</span></span>


[<span data-ttu-id="4ba85-130">Como instalar os componentes de servidores e do sistema</span><span class="sxs-lookup"><span data-stu-id="4ba85-130">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





