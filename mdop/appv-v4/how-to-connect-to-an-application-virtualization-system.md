---
title: Como se Conectar a um Application Virtualization System
description: Como se Conectar a um Application Virtualization System
author: dansimp
ms.assetid: ac38216c-5464-4c0b-a4d3-3949ba6358ac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 30d60e187e1b7595fd0dce6641fa027a1df68f3d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797180"
---
# <span data-ttu-id="87d53-103">Como se Conectar a um Application Virtualization System</span><span class="sxs-lookup"><span data-stu-id="87d53-103">How to Connect to an Application Virtualization System</span></span>


<span data-ttu-id="87d53-104">Você deve conectar o console de gerenciamento do servidor do Application Virtualization a um sistema de virtualização de aplicativos antes de poder usar o console de gerenciamento para gerenciar aplicativos, associações de tipo de arquivo, pacotes, licenças de aplicativos, grupos de servidores, políticas e administradores de provedor.</span><span class="sxs-lookup"><span data-stu-id="87d53-104">You must connect the Application Virtualization Server Management Console to an Application Virtualization System before you can use the management console to manage applications, file type associations, packages, application licenses, server groups, provider policies and administrators.</span></span> <span data-ttu-id="87d53-105">O procedimento a seguir descreve as etapas que devem ser seguidas para conectar o console a um sistema de virtualização de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="87d53-105">The following procedure outlines the steps you must follow to connect the console to an Application Virtualization System.</span></span>

**<span data-ttu-id="87d53-106">Para se conectar a um sistema de virtualização de aplicativos</span><span class="sxs-lookup"><span data-stu-id="87d53-106">To connect to an Application Virtualization System</span></span>**

1. <span data-ttu-id="87d53-107">Clique com o botão direito do mouse no nó do sistema do Application Virtualization no painel **escopo** e selecione **conectar ao sistema de virtualização de aplicativos** no menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="87d53-107">Right-click the Application Virtualization System node in the **Scope** pane, and select **Connect to Application Virtualization System** from the pop-up menu.</span></span>

   **<span data-ttu-id="87d53-108">Observação</span><span class="sxs-lookup"><span data-stu-id="87d53-108">Note</span></span>**  
   <span data-ttu-id="87d53-109">Há três componentes para o gerenciamento de servidor do Application Virtualization: o console de gerenciamento do Application Virtualization, o serviço de gerenciamento da Web e o SQL Datastore.</span><span class="sxs-lookup"><span data-stu-id="87d53-109">There are three components to Application Virtualization server management: the Application Virtualization Management Console, the Management Web Service, and the SQL Datastore.</span></span> <span data-ttu-id="87d53-110">Se esses componentes forem distribuídos entre máquinas físicas diferentes, você precisará configurar a segurança corretamente para que os componentes se comuniquem pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="87d53-110">If these components are distributed across different physical machines, you must configure security properly for the components to communicate across the system.</span></span> <span data-ttu-id="87d53-111">Para obter mais informações, consulte os seguintes artigos e manuais:</span><span class="sxs-lookup"><span data-stu-id="87d53-111">For more information, see the following manuals and articles:</span></span>

   <span data-ttu-id="87d53-112">[Como configurar o servidor para ser confiável para delegação](https://go.microsoft.com/fwlink/?LinkID=166682) (https://go.microsoft.com/fwlink/?LinkID=166682)</span><span class="sxs-lookup"><span data-stu-id="87d53-112">[How to Configure the Server to be Trusted for Delegation](https://go.microsoft.com/fwlink/?LinkID=166682) (https://go.microsoft.com/fwlink/?LinkID=166682)</span></span>

   <span data-ttu-id="87d53-113">[Guia de planejamento e implantação para o sistema de virtualização de aplicativos](https://go.microsoft.com/fwlink/?LinkID=122063) (https://go.microsoft.com/fwlink/?LinkID=122063)</span><span class="sxs-lookup"><span data-stu-id="87d53-113">[Planning and Deployment Guide for the Application Virtualization System](https://go.microsoft.com/fwlink/?LinkID=122063) (https://go.microsoft.com/fwlink/?LinkID=122063)</span></span>

   <span data-ttu-id="87d53-114">[Guia de operações do sistema de virtualização de aplicativos](https://go.microsoft.com/fwlink/?LinkID=133129) (https://go.microsoft.com/fwlink/?LinkID=133129)</span><span class="sxs-lookup"><span data-stu-id="87d53-114">[Operations Guide for the Application Virtualization System](https://go.microsoft.com/fwlink/?LinkID=133129) (https://go.microsoft.com/fwlink/?LinkID=133129)</span></span>

   <span data-ttu-id="87d53-115">[Artigo 930472](https://go.microsoft.com/fwlink/?LinkId=114647) na base de dados de conhecimento Microsoft (https://go.microsoft.com/fwlink/?LinkId=114647)</span><span class="sxs-lookup"><span data-stu-id="87d53-115">[Article 930472](https://go.microsoft.com/fwlink/?LinkId=114647) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=114647)</span></span>

   <span data-ttu-id="87d53-116">[Artigo 930565](https://go.microsoft.com/fwlink/?LinkId=114648) na base de dados de conhecimento Microsoft (https://go.microsoft.com/fwlink/?LinkId=114648)</span><span class="sxs-lookup"><span data-stu-id="87d53-116">[Article 930565](https://go.microsoft.com/fwlink/?LinkId=114648) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=114648)</span></span>

     

2. <span data-ttu-id="87d53-117">Preencha os campos da caixa de diálogo **conectar-se ao sistema do Application Virtualization** :</span><span class="sxs-lookup"><span data-stu-id="87d53-117">Complete the fields in the **Connect to Application Virtualization System** dialog box:</span></span>

   1. <span data-ttu-id="87d53-118">**Nome do host do serviço Web**— Insira o nome do sistema de virtualização de aplicativos ao qual você deseja se conectar ou digite **localhost** para se conectar ao servidor local.</span><span class="sxs-lookup"><span data-stu-id="87d53-118">**Web Service Host Name**—Enter the name of the Application Virtualization System to which you want to connect, or enter **localhost** to connect to the local server.</span></span>

   2. <span data-ttu-id="87d53-119">**Usar conexão segura**-Marque esta caixa de seleção se quiser se conectar ao servidor com uma conexão segura.</span><span class="sxs-lookup"><span data-stu-id="87d53-119">**Use Secure Connection**—Select this check box if you want to connect to the server with a secure connection.</span></span>

   3. <span data-ttu-id="87d53-120">**Porta**— Insira o número da porta que você deseja usar para a conexão.</span><span class="sxs-lookup"><span data-stu-id="87d53-120">**Port**—Enter the port number you want to use for the connection.</span></span> <span data-ttu-id="87d53-121">o **80** é o número de porta convencional padrão e o **443** é o número da porta segura.</span><span class="sxs-lookup"><span data-stu-id="87d53-121">**80** is the default regular port number, and **443** is the secure-port number.</span></span>

   4. <span data-ttu-id="87d53-122">**Usar conta atual do Windows**— Selecione este botão de opção para usar as credenciais atuais da conta do Windows.</span><span class="sxs-lookup"><span data-stu-id="87d53-122">**Use Current Windows Account**—Select this radio button to use the current Windows account credentials.</span></span>

   5. <span data-ttu-id="87d53-123">**Especificar conta do Windows**— Selecione este botão de opção quando quiser se conectar ao servidor como um usuário diferente.</span><span class="sxs-lookup"><span data-stu-id="87d53-123">**Specify Windows Account**—Select this radio button when you want to connect to the server as a different user.</span></span>

   6. <span data-ttu-id="87d53-124">**Nome**— Insira o nome do novo usuário usando o formato *DOMAIN\\username* ou o <em> username@domain </em> .</span><span class="sxs-lookup"><span data-stu-id="87d53-124">**Name**—Enter the name of the new user by using either the *DOMAIN\\username* or the <em>username@domain</em> format.</span></span>

   7. <span data-ttu-id="87d53-125">**Senha**— Insira a senha que corresponde ao novo usuário.</span><span class="sxs-lookup"><span data-stu-id="87d53-125">**Password**—Enter the password that corresponds to the new user.</span></span>

3. <span data-ttu-id="87d53-126">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="87d53-126">Click **OK**.</span></span>

## <span data-ttu-id="87d53-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87d53-127">Related topics</span></span>


[<span data-ttu-id="87d53-128">Como realizar tarefas administrativas no Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="87d53-128">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





