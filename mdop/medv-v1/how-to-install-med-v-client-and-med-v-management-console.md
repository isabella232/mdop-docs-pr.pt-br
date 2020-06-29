---
title: Como instalar o cliente MED-V e o Console de Gerenciamento do MED-V
description: Como instalar o cliente MED-V e o Console de Gerenciamento do MED-V
author: dansimp
ms.assetid: 8a5f3010-3a50-487e-99d8-e352e5cb51c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 24a486cc7cf5534171f80b08dc93742e03cd4a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799981"
---
# <span data-ttu-id="baef6-103">Como instalar o cliente MED-V e o Console de Gerenciamento do MED-V</span><span class="sxs-lookup"><span data-stu-id="baef6-103">How to Install MED-V Client and MED-V Management Console</span></span>


<span data-ttu-id="baef6-104">Os seguintes componentes do MED-V estão incluídos no pacote Client. msi:</span><span class="sxs-lookup"><span data-stu-id="baef6-104">The following MED-V components are included in the client .msi package:</span></span>

-   <span data-ttu-id="baef6-105">Cliente MED-V — o software MED-V que deve ser instalado em computadores cliente para executar os espaços de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="baef6-105">MED-V client—The MED-V software that must be installed on client computers for running MED-V workspaces.</span></span>

-   <span data-ttu-id="baef6-106">Console de gerenciamento do MED-V – a ferramenta administrativa que os administradores podem usar para criar e manter imagens, espaços de trabalho do MED-V e políticas.</span><span class="sxs-lookup"><span data-stu-id="baef6-106">MED-V management console—The administrative tool that administrators can use to create and maintain images, MED-V workspaces, and policies.</span></span>

<span data-ttu-id="baef6-107">O console de gerenciamento do MED-V e o cliente MED-V são instalados do pacote MED-V Client. msi.</span><span class="sxs-lookup"><span data-stu-id="baef6-107">The MED-V management console and the MED-V client are both installed from the MED-V client .msi package.</span></span> <span data-ttu-id="baef6-108">No entanto, o cliente MED-V pode ser instalado independentemente sem o console de gerenciamento do MED-V, desmarcando a caixa de seleção **instalar o aplicativo de gerenciamento do MED-v** durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="baef6-108">The MED-V client, however, can be installed independently without the MED-V management console by clearing the **Install the MED-V Management application** check box during installation.</span></span>

**<span data-ttu-id="baef6-109">Observação</span><span class="sxs-lookup"><span data-stu-id="baef6-109">Note</span></span>**  
<span data-ttu-id="baef6-110">O cliente do MED-V e o console de gerenciamento do MED-V só podem ser instalados em computadores com Windows 7, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="baef6-110">The MED-V client and MED-V management console can only be installed on Windows 7-, Windows Vista-, and Windows XP-based computers.</span></span> <span data-ttu-id="baef6-111">Eles não podem ser instalados em produtos de servidor.</span><span class="sxs-lookup"><span data-stu-id="baef6-111">They cannot be installed on server products.</span></span>



**<span data-ttu-id="baef6-112">Observação</span><span class="sxs-lookup"><span data-stu-id="baef6-112">Note</span></span>**  
<span data-ttu-id="baef6-113">Não instale o cliente MED-V usando o comando **runas** do Windows.</span><span class="sxs-lookup"><span data-stu-id="baef6-113">Do not install the MED-V client using the Windows **runas** command.</span></span>



**<span data-ttu-id="baef6-114">Para instalar o cliente MED-V</span><span class="sxs-lookup"><span data-stu-id="baef6-114">To install the MED-V client</span></span>**

1.  <span data-ttu-id="baef6-115">Faça logon como usuário com direitos de administrador local no computador local.</span><span class="sxs-lookup"><span data-stu-id="baef6-115">Log in as a user with local administrator rights on the local computer.</span></span>

2.  <span data-ttu-id="baef6-116">Execute o pacote MED-V. msi.</span><span class="sxs-lookup"><span data-stu-id="baef6-116">Run the MED-V .msi package.</span></span>

    <span data-ttu-id="baef6-117">O pacote MED-V. msi é chamado *MED-V\_x.msi*, em que *x* é o número da versão.</span><span class="sxs-lookup"><span data-stu-id="baef6-117">The MED-V .msi package is called *MED-V\_x.msi*, where *x* is the version number.</span></span>

    <span data-ttu-id="baef6-118">Por exemplo, *MED-V\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="baef6-118">For example, *MED-V\_1.0.65.msi*.</span></span>

3.  <span data-ttu-id="baef6-119">Quando a tela de **boas-vindas do Assistente InstallShield** for exibida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="baef6-119">When the **InstallShield Wizard Welcome** screen appears, click **Next**.</span></span>

4.  <span data-ttu-id="baef6-120">Na tela **contrato de licença** , leia o contrato de licença, clique em **aceito os termos do contrato de licença**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="baef6-120">On the **License Agreement** screen, read the license agreement, click **I accept the terms in the license agreement**, and click **Next**.</span></span>

    <span data-ttu-id="baef6-121">A tela de **pasta de destino** será exibida, com a pasta de instalação padrão exibida.</span><span class="sxs-lookup"><span data-stu-id="baef6-121">The **Destination Folder** screen appears, with the default installation folder displayed.</span></span>

    <span data-ttu-id="baef6-122">A pasta de instalação padrão é o diretório onde o sistema operacional está instalado.</span><span class="sxs-lookup"><span data-stu-id="baef6-122">The default installation folder is the directory where the operating system is installed.</span></span>

    -   <span data-ttu-id="baef6-123">Para alterar a pasta em que o MED-V deve ser instalado, clique em **alterar**e navegue até uma pasta existente.</span><span class="sxs-lookup"><span data-stu-id="baef6-123">To change the folder where MED-V should be installed, click **Change**, and browse to an existing folder.</span></span>

5.  <span data-ttu-id="baef6-124">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="baef6-124">Click **Next**.</span></span>

6.  <span data-ttu-id="baef6-125">Na tela de **configurações do MED-v** , configure a instalação do MED-v da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="baef6-125">On the **MED-V Settings** screen, configure the MED-V installation as follows:</span></span>

    -   <span data-ttu-id="baef6-126">Marque a caixa de seleção **instalar o aplicativo de gerenciamento do MED-V** para incluir o componente de gerenciamento na instalação.</span><span class="sxs-lookup"><span data-stu-id="baef6-126">Select the **Install the MED-V management application** check box to include the management component in the installation.</span></span>

        **<span data-ttu-id="baef6-127">Observação</span><span class="sxs-lookup"><span data-stu-id="baef6-127">Note</span></span>**  
        <span data-ttu-id="baef6-128">Os administradores de virtualização de área de trabalho corporativa devem instalar o aplicativo de gerenciamento do MED-V.</span><span class="sxs-lookup"><span data-stu-id="baef6-128">Enterprise Desktop Virtualization administrators should install the MED-V management application.</span></span> <span data-ttu-id="baef6-129">Este aplicativo é necessário para configurar imagens da área de trabalho e espaços de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="baef6-129">This application is required for configuring desktop images and MED-V workspaces.</span></span>



~~~
-   Select the **Load MED-V when Windows starts** check box to start MED-V automatically on startup.

-   Select the **Add a MED-V shortcut to my desktop** check box to create a MED-V shortcut on your desktop.

-   In the **Server address** field, type the server address.

-   In the **Server port** field, type the server's port.

-   Select the **Server requires encrypted connections (https)** check box to work with https.

-   The default virtual machine images folder is displayed. The default installation folder is *%systemdrive%\\MED-V Images\\*. To change the folder where MED-V should be installed, click **Change**, and browse to an existing folder.
~~~

7. <span data-ttu-id="baef6-130">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="baef6-130">Click **Next**.</span></span>

8. <span data-ttu-id="baef6-131">Na tela **pronto para instalar o programa** , clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="baef6-131">On the **Ready to Install the Program** screen, click **Install**.</span></span>

   <span data-ttu-id="baef6-132">A instalação do cliente do MED-V é iniciada.</span><span class="sxs-lookup"><span data-stu-id="baef6-132">The MED-V client installation starts.</span></span> <span data-ttu-id="baef6-133">Isso pode levar alguns minutos, e a tela pode não exibir texto.</span><span class="sxs-lookup"><span data-stu-id="baef6-133">This can take several minutes, and the screen might not display text.</span></span> <span data-ttu-id="baef6-134">Durante a instalação, várias telas de progresso são exibidas.</span><span class="sxs-lookup"><span data-stu-id="baef6-134">During installation, several progress screens appear.</span></span> <span data-ttu-id="baef6-135">Se aparecer uma mensagem, siga as instruções fornecidas.</span><span class="sxs-lookup"><span data-stu-id="baef6-135">If a message appears, follow the instructions provided.</span></span>

   <span data-ttu-id="baef6-136">Após a instalação bem-sucedida, a tela **Assistente InstallShield concluído** é exibida.</span><span class="sxs-lookup"><span data-stu-id="baef6-136">Upon successful installation, the **InstallShield Wizard Completed** screen appears.</span></span>

9. <span data-ttu-id="baef6-137">Clique em **concluir** para fechar o assistente.</span><span class="sxs-lookup"><span data-stu-id="baef6-137">Click **Finish** to close the wizard.</span></span>

## <span data-ttu-id="baef6-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="baef6-138">Related topics</span></span>


[<span data-ttu-id="baef6-139">Configurações com suporte</span><span class="sxs-lookup"><span data-stu-id="baef6-139">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

[<span data-ttu-id="baef6-140">Listas de verificação para instalação e atualização</span><span class="sxs-lookup"><span data-stu-id="baef6-140">Installation and Upgrade Checklists</span></span>](installation-and-upgrade-checklists.md)









