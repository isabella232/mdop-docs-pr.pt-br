---
title: Usando a interface de usuário do Console de Gerenciamento do MED-V
description: Usando a interface de usuário do Console de Gerenciamento do MED-V
author: dansimp
ms.assetid: f42714d7-6f0c-4995-ab31-d4ef0845a22c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22fc98c3edbea48847e1a00369bea21a470e66b7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799754"
---
# <span data-ttu-id="0de5f-103">Usando a interface de usuário do Console de Gerenciamento do MED-V</span><span class="sxs-lookup"><span data-stu-id="0de5f-103">Using the MED-V Management Console User Interface</span></span>


<span data-ttu-id="0de5f-104">A interface do usuário do console está dividida nas seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="0de5f-104">The console user interface is divided into the following sections:</span></span>

-   <span data-ttu-id="0de5f-105">Os seguintes **botões de gerenciamento do MED-V**, que correspondem aos três módulos:</span><span class="sxs-lookup"><span data-stu-id="0de5f-105">The following **MED-V management buttons**, which correspond to the three modules:</span></span>

    -   <span data-ttu-id="0de5f-106">**Política**– o módulo de **política** é usado para definir os espaços de trabalho do MED-V e suas configurações e permissões relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0de5f-106">**Policy**—The **Policy** module is used to define the MED-V workspaces and their related settings and permissions.</span></span>

    -   <span data-ttu-id="0de5f-107">**Images**— o módulo **images** é usado para gerenciar imagens do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="0de5f-107">**Images**—The **Images** module is used to manage MED-V workspace images.</span></span>

    -   <span data-ttu-id="0de5f-108">**Relatórios**— o módulo **relatórios** é usado para gerar e exibir relatórios do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="0de5f-108">**Reports**—The **Reports** module is used for generating and viewing MED-V workspace reports.</span></span>

-   <span data-ttu-id="0de5f-109">A **barra de ferramentas** exibe atalhos relevantes para o botão selecionado.</span><span class="sxs-lookup"><span data-stu-id="0de5f-109">The **toolbar** displays shortcuts relevant to the button selected.</span></span>

-   <span data-ttu-id="0de5f-110">O **painel display** exibe um módulo correspondente ao botão que está selecionado.</span><span class="sxs-lookup"><span data-stu-id="0de5f-110">The **display pane** displays a module corresponding to the button that is selected.</span></span>

![](images/medv-ui-console-general.gif)

## <span data-ttu-id="0de5f-111">Como fazer logon no console de gerenciamento do MED-V</span><span class="sxs-lookup"><span data-stu-id="0de5f-111">How to Log In to the MED-V Management Console</span></span>


**<span data-ttu-id="0de5f-112">Para abrir o console de gerenciamento do MED-V</span><span class="sxs-lookup"><span data-stu-id="0de5f-112">To open the MED-V management console</span></span>**

-   <span data-ttu-id="0de5f-113">No menu **Iniciar** do Windows, selecione **todos os programas &gt; Gerenciamento med &gt; -v**do MED-v ou na área de trabalho, clique duas vezes no ícone de gerenciamento do MED-v.</span><span class="sxs-lookup"><span data-stu-id="0de5f-113">On the Windows **Start** menu, select **All Programs &gt; MED-V &gt; MED-V Management**, or on the desktop, double-click the MED-V Management icon.</span></span>

    <span data-ttu-id="0de5f-114">A janela de **logon do MED-V Management** será exibida.</span><span class="sxs-lookup"><span data-stu-id="0de5f-114">The **MED-V Management Login** window appears.</span></span>

<span data-ttu-id="0de5f-115">**Observação**  Por motivos de segurança, o primeiro usuário para se conectar ao console de gerenciamento do MED-V se tornará o único usuário nesse computador que tenha permissão para acessar o console de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="0de5f-115">**Note** For security reasons, the first user to log in to the MED-V management console will become the only user on that computer allowed to access the management console.</span></span>

 

**<span data-ttu-id="0de5f-116">Para entrar</span><span class="sxs-lookup"><span data-stu-id="0de5f-116">To log in</span></span>**

1.  <span data-ttu-id="0de5f-117">Digite suas credenciais de usuário do domínio no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="0de5f-117">Type in your domain user credentials in the following format:</span></span>

    <span data-ttu-id="0de5f-118">"domínio \ _name \\user\ _name", "senha"</span><span class="sxs-lookup"><span data-stu-id="0de5f-118">"domain\_name\\user\_name", "password"</span></span>

    <span data-ttu-id="0de5f-119">**Observação**  Ao configurar o servidor, os usuários com acesso total e usuários com acesso somente leitura são definidos.</span><span class="sxs-lookup"><span data-stu-id="0de5f-119">**Note** When configuring the server, users with full access as well as users with read-only access are defined.</span></span> <span data-ttu-id="0de5f-120">Todos os usuários devem ser usuários do domínio.</span><span class="sxs-lookup"><span data-stu-id="0de5f-120">All users must be domain users.</span></span> <span data-ttu-id="0de5f-121">O nome de usuário e a senha do domínio são usados para o logon de gerenciamento do MED-V.</span><span class="sxs-lookup"><span data-stu-id="0de5f-121">The domain user name and password is used for MED-V management login.</span></span>

     

2.  <span data-ttu-id="0de5f-122">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="0de5f-122">Click **OK**.</span></span>

    <span data-ttu-id="0de5f-123">O console de **Gerenciamento do MED-V** é exibido.</span><span class="sxs-lookup"><span data-stu-id="0de5f-123">The **MED-V Management** console appears.</span></span>

## <span data-ttu-id="0de5f-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0de5f-124">Related topics</span></span>


[<span data-ttu-id="0de5f-125">Como instalar o cliente MED-V e o Console de Gerenciamento do MED-V</span><span class="sxs-lookup"><span data-stu-id="0de5f-125">How to Install MED-V Client and MED-V Management Console</span></span>](how-to-install-med-v-client-and-med-v-management-console.md)

 

 





