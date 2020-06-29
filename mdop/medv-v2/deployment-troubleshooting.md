---
title: Solução de problemas de implantação
description: Solução de problemas de implantação
author: dansimp
ms.assetid: 9ee980f2-4e77-4020-9f0e-8c2ffdc390ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe9677175c9538bc070d2adea17a96351397d9a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799164"
---
# <span data-ttu-id="2adb7-103">Solução de problemas de implantação</span><span class="sxs-lookup"><span data-stu-id="2adb7-103">Deployment Troubleshooting</span></span>


<span data-ttu-id="2adb7-104">Este tópico inclui informações para ajudá-lo a solucionar problemas de implantação na virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="2adb7-104">This topic includes information to help you troubleshoot deployment issues in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="2adb7-105">Solucionando problemas na implantação do MED-V</span><span class="sxs-lookup"><span data-stu-id="2adb7-105">Troubleshooting Issues in MED-V Deployment</span></span>


<span data-ttu-id="2adb7-106">O seguinte problema pode ocorrer ao implantar o MED-V.</span><span class="sxs-lookup"><span data-stu-id="2adb7-106">The following issue might occur when you deploy MED-V.</span></span> <span data-ttu-id="2adb7-107">A solução ajuda a solucionar esse problema.</span><span class="sxs-lookup"><span data-stu-id="2adb7-107">The solution helps troubleshoot this issue.</span></span>

**<span data-ttu-id="2adb7-108">Ocorrerão problemas se você estiver instalando o MED-V somente para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="2adb7-108">Problems Occur if Installing MED-V for Current User Only.</span></span>** <span data-ttu-id="2adb7-109">O MED-V só oferece suporte à instalação do pacote do espaço de trabalho do MED-V, ao agente de host do MED-V e ao espaço de trabalho do MED-v para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="2adb7-109">MED-V only supports the installation of the MED-V Workspace Packager, the MED-V Host Agent, and the MED-V workspace for all users.</span></span> <span data-ttu-id="2adb7-110">A instalação para o usuário atual só causa falhas na instalação dos componentes e na configuração do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="2adb7-110">Installing for the current user only causes failures in the installation of the components and in the setup of the MED-V workspace.</span></span>

**<span data-ttu-id="2adb7-111">Solução</span><span class="sxs-lookup"><span data-stu-id="2adb7-111">Solution</span></span>**

<span data-ttu-id="2adb7-112">Nunca use a opção **ALLUSERS = ""** ao instalar os componentes do MED-V.</span><span class="sxs-lookup"><span data-stu-id="2adb7-112">Never use the option **ALLUSERS=””** when installing the MED-V components.</span></span>

**<span data-ttu-id="2adb7-113">O MED-V requer o uso exclusivo da pilha de virtualização.</span><span class="sxs-lookup"><span data-stu-id="2adb7-113">MED-V Requires Exclusive Use of the Virtualization Stack.</span></span>** <span data-ttu-id="2adb7-114">Somente uma pilha de virtualização pode ser executada por vez em um computador.</span><span class="sxs-lookup"><span data-stu-id="2adb7-114">Only one virtualization stack can be run at a time on a computer.</span></span> <span data-ttu-id="2adb7-115">O computador virtual do Windows deve usar a pilha virtual e o MED-V depende do PC virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="2adb7-115">Windows Virtual PC must use the virtual stack, and MED-V depends on Windows Virtual PC.</span></span> <span data-ttu-id="2adb7-116">Portanto, se você tentar implantar ou usar o MED-V quando outros aplicativos estiverem em execução que usam a pilha virtual, o MED-V não pode ser executado ou ser instalado com êxito.</span><span class="sxs-lookup"><span data-stu-id="2adb7-116">Therefore, if you try to deploy or use MED-V when other applications are running that use the virtual stack, MED-V cannot run or be successfully installed.</span></span>

**<span data-ttu-id="2adb7-117">Solução</span><span class="sxs-lookup"><span data-stu-id="2adb7-117">Solution</span></span>**

<span data-ttu-id="2adb7-118">Feche todos os aplicativos que estejam sendo executados que usem a pilha de virtualização antes de instalar ou executar o MED-V.</span><span class="sxs-lookup"><span data-stu-id="2adb7-118">Close any application that is running that uses the virtualization stack before you install or run MED-V.</span></span>

**<span data-ttu-id="2adb7-119">Os atalhos permanecem após a desinstalação.</span><span class="sxs-lookup"><span data-stu-id="2adb7-119">Shortcuts Remain after Uninstall.</span></span>** <span data-ttu-id="2adb7-120">Por padrão, quando você desinstala o MED-V, os atalhos do menu **Iniciar** do usuário final são removidos.</span><span class="sxs-lookup"><span data-stu-id="2adb7-120">By default, when you uninstall MED-V, shortcuts in the end user’s **Start** menu are removed.</span></span> <span data-ttu-id="2adb7-121">No entanto, em determinadas situações, por exemplo, para usuários finais que estiverem executando perfis móveis, os atalhos para aplicativos publicados do MED-V permanecem no menu **Iniciar** do usuário final.</span><span class="sxs-lookup"><span data-stu-id="2adb7-121">However, in certain situations, such as for end users who are running roaming profiles, shortcuts to MED-V published applications remain in the end user’s **Start** menu.</span></span>

**<span data-ttu-id="2adb7-122">Solução</span><span class="sxs-lookup"><span data-stu-id="2adb7-122">Solution</span></span>**

<span data-ttu-id="2adb7-123">Para excluir manualmente os atalhos restantes no menu **Iniciar** , clique com o botão direito do mouse nos atalhos e, em seguida, clique em **remover**.</span><span class="sxs-lookup"><span data-stu-id="2adb7-123">To manually delete the remaining shortcuts on the **Start** menu, right-click the shortcuts, and then click **Remove**.</span></span>

**<span data-ttu-id="2adb7-124">Desabilitar a configuração da política de grupo da mensagem de logon no espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="2adb7-124">Disable Logon Message Group Policy Setting in the MED-V Workspace.</span></span>** <span data-ttu-id="2adb7-125">Se a mensagem de logon do Windows XP estiver habilitada no espaço de trabalho do MED-V, o usuário final deverá fazer logon toda vez que quiser abrir um aplicativo virtual do MED-V.</span><span class="sxs-lookup"><span data-stu-id="2adb7-125">If the Windows XP logon message is enabled in the MED-V workspace, the end user must log on every time they want to open a MED-V virtual application.</span></span> <span data-ttu-id="2adb7-126">Isso cria uma experiência de usuário ruim.</span><span class="sxs-lookup"><span data-stu-id="2adb7-126">This creates a poor user experience.</span></span>

**<span data-ttu-id="2adb7-127">Solução</span><span class="sxs-lookup"><span data-stu-id="2adb7-127">Solution</span></span>**

<span data-ttu-id="2adb7-128">Desabilite as seguintes configurações de política de grupo na máquina virtual do MED-V:</span><span class="sxs-lookup"><span data-stu-id="2adb7-128">Disable the following Group Policy settings in the MED-V virtual machine:</span></span>

**<span data-ttu-id="2adb7-129">Logon interativo: texto de mensagem para usuários tentando fazer logon</span><span class="sxs-lookup"><span data-stu-id="2adb7-129">Interactive logon: Message text for users attempting to log on</span></span>**

**<span data-ttu-id="2adb7-130">Logon interativo: Título da mensagem para usuários tentando fazer logon</span><span class="sxs-lookup"><span data-stu-id="2adb7-130">Interactive logon: Message title for users attempting to log on</span></span>**

## <span data-ttu-id="2adb7-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2adb7-131">Related topics</span></span>


[<span data-ttu-id="2adb7-132">Solução de problemas de operações</span><span class="sxs-lookup"><span data-stu-id="2adb7-132">Operations Troubleshooting</span></span>](operations-troubleshooting-medv2.md)

 

 





