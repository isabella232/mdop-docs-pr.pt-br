---
title: Como adicionar um aplicativo manualmente
description: Como adicionar um aplicativo manualmente
author: dansimp
ms.assetid: c635b07a-5c7f-4ab2-ba18-366457146cb9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 868939553fae6172ccca549ddc3f08aa76ee3c56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797057"
---
# <span data-ttu-id="8fb1f-103">Como adicionar um aplicativo manualmente</span><span class="sxs-lookup"><span data-stu-id="8fb1f-103">How to Manually Add an Application</span></span>


<span data-ttu-id="8fb1f-104">Ao adicionar um aplicativo ao servidor de gerenciamento do Application Virtualization, é recomendável importá-lo.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-104">When adding an application to the Application Virtualization Management Server, it is recommended that you import it.</span></span> <span data-ttu-id="8fb1f-105">Você pode adicionar um aplicativo manualmente, mas deve fornecer as informações exatas e detalhadas sobre o aplicativo chamado para nesta seção.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-105">You can add an application manually, but you must provide the precise, detailed information about the application called for in this section.</span></span>

**<span data-ttu-id="8fb1f-106">Para adicionar manualmente um novo aplicativo</span><span class="sxs-lookup"><span data-stu-id="8fb1f-106">To manually add a new application</span></span>**

1.  <span data-ttu-id="8fb1f-107">No painel esquerdo, clique com o botão direito do mouse no nó **aplicativos** e escolha **novo aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-107">In the left pane, right-click the **Applications** node and choose **New Application**.</span></span>

2.  <span data-ttu-id="8fb1f-108">No **Assistente novo aplicativo**, preencha a caixa de diálogo **informações gerais** :</span><span class="sxs-lookup"><span data-stu-id="8fb1f-108">In the **New Application Wizard**, complete the **General Information** dialog box:</span></span>

    1.  <span data-ttu-id="8fb1f-109">**Nome do aplicativo**— digite o nome que você deseja que os usuários vejam.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-109">**Application Name**—Type the name you want the users to see.</span></span>

    2.  <span data-ttu-id="8fb1f-110">**Versão**— digite a versão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-110">**Version**—Type the application version.</span></span>

    3.  <span data-ttu-id="8fb1f-111">**Habilitado**– essa caixa deve ser selecionada para transmitir o aplicativo após criá-lo.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-111">**Enabled**—This box must be selected to stream the application after you create it.</span></span>

    4.  <span data-ttu-id="8fb1f-112">**Descrição**— digite uma descrição opcional para o uso administrativo.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-112">**Description**—Type an optional description for administrative use.</span></span>

    5.  <span data-ttu-id="8fb1f-113">**Caminho OSD**— procure a rede no arquivo Open Software DESCRIPTOR (OSD) do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-113">**OSD Path**—Browse the network to the application's Open Software Descriptor (OSD) file.</span></span> <span data-ttu-id="8fb1f-114">Esse arquivo deve estar em uma pasta de rede compartilhada.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-114">This file must be in a shared network folder.</span></span>

    6.  <span data-ttu-id="8fb1f-115">**Caminho do ícone**— navegue até o arquivo ico do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-115">**Icon Path**—Browse to the application's ICO file.</span></span>

    7.  <span data-ttu-id="8fb1f-116">**Grupo de licenças de aplicativos**— se você tiver configurado grupos de licenças, poderá atribuir o aplicativo a um selecionando-o na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-116">**Application License Group**—If you have set up license groups, you can assign the application to one by selecting it in the pull-down list.</span></span>

    8.  <span data-ttu-id="8fb1f-117">**Grupo de servidores**— se você tiver vários servidores de virtualização de aplicativos, poderá atribuir o aplicativo a um selecionando-o na lista pull-down.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-117">**Server Group**—If you have multiple Application Virtualization Servers, you can assign the application to one by selecting it in the pull-down list.</span></span>

3.  <span data-ttu-id="8fb1f-118">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-118">Click **Next**.</span></span>

4.  <span data-ttu-id="8fb1f-119">Na caixa de diálogo **selecionar pacote** , selecione o pacote relacionado e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-119">In the **Select Package** dialog box, select the related package and click **Next**.</span></span>

5.  <span data-ttu-id="8fb1f-120">Na tela **atalhos publicados** , marque as caixas dos locais em que você deseja que os atalhos do aplicativo apareçam nos computadores cliente e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-120">On the **Published Shortcuts** screen, select the boxes for the locations where you would like the application shortcuts to appear on the client computers and click **Next**.</span></span>

6.  <span data-ttu-id="8fb1f-121">Na tela **associações de arquivo** , você pode adicionar novas associações de arquivo de tipo a esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-121">In the **File Associations** screen, you can add new type file associations to this application.</span></span> <span data-ttu-id="8fb1f-122">Para fazer isso, clique em **Adicionar**, insira a extensão (sem um ponto precedente), insira uma descrição e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-122">To do so, click **Add**, enter the extension (without a preceding dot), enter a description, and click **OK**.</span></span>

7.  <span data-ttu-id="8fb1f-123">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-123">Click **Next**.</span></span>

8.  <span data-ttu-id="8fb1f-124">Na caixa de diálogo **permissões de acesso** , clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-124">In the **Access Permissions** dialog box, click **Add**.</span></span>

9.  <span data-ttu-id="8fb1f-125">Na caixa de diálogo **Adicionar/editar grupo de usuários** , navegue até o grupo usuário.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-125">In the **Add/Edit User Group** dialog box, navigate to the user group.</span></span> <span data-ttu-id="8fb1f-126">Você também pode inserir o domínio e o grupo digitando as informações nos respectivos campos.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-126">You can also enter the domain and group by typing the information in the respective fields.</span></span> <span data-ttu-id="8fb1f-127">Quando terminar, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-127">When you finish, click **OK**.</span></span> <span data-ttu-id="8fb1f-128">Você pode adicionar outros grupos com as mesmas páginas.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-128">You can add other groups with the same pages.</span></span>

10. <span data-ttu-id="8fb1f-129">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-129">Click **Next**.</span></span>

11. <span data-ttu-id="8fb1f-130">Na tela **Resumo** , você pode revisar as configurações de importação.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-130">On the **Summary** screen, you can review the import settings.</span></span> <span data-ttu-id="8fb1f-131">Clique em **concluir** para adicionar o aplicativo, clique em **retornar** para alterar as informações ou clique em **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="8fb1f-131">Click **Finish** to add the application, click **Back** to change the information, or click **Cancel**.</span></span>

## <span data-ttu-id="8fb1f-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8fb1f-132">Related topics</span></span>


[<span data-ttu-id="8fb1f-133">Como gerenciar aplicativos no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="8fb1f-133">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





