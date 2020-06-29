---
title: Como verificar as configurações da primeira instalação
description: Como verificar as configurações da primeira instalação
author: dansimp
ms.assetid: e8a07d4c-5786-4455-ac43-2deac4042efd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859d627ec90fbc26d18019062d5e316f907cec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796146"
---
# <span data-ttu-id="16a78-103">Como verificar as configurações da primeira instalação</span><span class="sxs-lookup"><span data-stu-id="16a78-103">How to Verify First Time Setup Settings</span></span>


<span data-ttu-id="16a78-104">Enquanto o teste da configuração inicial estiver em execução ou após a conclusão, você pode verificar as configurações que configurou em seu espaço de trabalho do MED-V executando as seguintes tarefas.</span><span class="sxs-lookup"><span data-stu-id="16a78-104">While your test of first time setup is running or after it finishes, you can verify the settings that you configured in your MED-V workspace by performing the following tasks.</span></span>

<span data-ttu-id="16a78-105">**Observação**  Para obter informações sobre como monitorar a conclusão bem-sucedida da primeira configuração da sua empresa após a implantação, consulte [monitoramento de implantações de espaço de trabalho do MED-V](monitoring-med-v-workspace-deployments.md).</span><span class="sxs-lookup"><span data-stu-id="16a78-105">**Note** For information about how to monitor the successful completion of first time setup throughout your enterprise after deployment, see [Monitoring MED-V Workspace Deployments](monitoring-med-v-workspace-deployments.md).</span></span>

 

**<span data-ttu-id="16a78-106">Para verificar as configurações durante a configuração da primeira vez</span><span class="sxs-lookup"><span data-stu-id="16a78-106">To verify settings during first time setup</span></span>**

1.  <span data-ttu-id="16a78-107">Enquanto a configuração estiver em execução pela primeira vez, verifique o seguinte:</span><span class="sxs-lookup"><span data-stu-id="16a78-107">While first time setup is running, verify the following:</span></span>

    <span data-ttu-id="16a78-108">Se você especificou o modo **autônomo** , verifique se a máquina virtual não é exibida na primeira vez em que a configuração está em execução.</span><span class="sxs-lookup"><span data-stu-id="16a78-108">If you specified **Unattended** mode, verify that the virtual machine does not appear when first time setup is running.</span></span>

    <span data-ttu-id="16a78-109">Se você especificou o modo assistido, verifique se a máquina virtual é exibida e se todos os campos que exigem entrada do usuário são exibidos.</span><span class="sxs-lookup"><span data-stu-id="16a78-109">If you specified attended mode, verify that the virtual machine appears and that all fields that require user input are displayed.</span></span>

2.  <span data-ttu-id="16a78-110">Você também pode monitorar o processo de configuração completo da primeira vez, exibindo a máquina virtual na primeira vez em que a configuração estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="16a78-110">You can also monitor the complete first time setup process by viewing the virtual machine when first time setup is running.</span></span> <span data-ttu-id="16a78-111">Para fazer isso, execute estas etapas:</span><span class="sxs-lookup"><span data-stu-id="16a78-111">To do this, follow these steps:</span></span>

    1.  <span data-ttu-id="16a78-112">Abra o console do Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="16a78-112">Open the Windows Virtual PC Console.</span></span>

        <span data-ttu-id="16a78-113">Clique em **Iniciar**, clique em **todos os programas**, clique em **PC virtual do Windows**e clique em **PC virtual do Windows**.</span><span class="sxs-lookup"><span data-stu-id="16a78-113">Click **Start**, click **All Programs**, click **Windows Virtual PC**, and then click **Windows Virtual PC**.</span></span>

    2.  <span data-ttu-id="16a78-114">Inicie o MED-V se ele ainda não estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="16a78-114">Start MED-V if it is not already running.</span></span>

        <span data-ttu-id="16a78-115">Se ainda não estiver presente, em curto período, uma máquina virtual com o nome do espaço de trabalho do MED-V implantado aparecerá na lista de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="16a78-115">If not already present, in a short time, a virtual machine with the name of the deployed MED-V workspace appears in the list of virtual machines.</span></span>

    3.  <span data-ttu-id="16a78-116">Clique duas vezes na máquina virtual do MED-V para abri-la.</span><span class="sxs-lookup"><span data-stu-id="16a78-116">Double-click the MED-V virtual machine to open it.</span></span>

        <span data-ttu-id="16a78-117">Você pode observar a máquina virtual do MED-V quando ela está sendo configurada, e você pode solucionar problemas com o procedimento de mini-configuração.</span><span class="sxs-lookup"><span data-stu-id="16a78-117">You can observe the MED-V virtual machine when it is being set up, and you can troubleshoot the Mini-Setup procedure.</span></span> <span data-ttu-id="16a78-118">Verifique as informações nas diferentes telas à medida que elas entram, como a configuração de configurações de rede, informações sobre o domínio do computador, configuração do agente convidado, configuração de configurações pessoais e desligamento.</span><span class="sxs-lookup"><span data-stu-id="16a78-118">Verify the information in the different screens as they go by, such as configuring networking settings, computer domain join information, configuring of the Guest Agent, set up of personal settings, and shutdown.</span></span>

    4.  <span data-ttu-id="16a78-119">A máquina virtual é fechada automaticamente quando a instalação for concluída pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="16a78-119">The virtual machine closes automatically when first time setup finishes.</span></span>

        <span data-ttu-id="16a78-120">**Observação**  Você pode fechar a janela da máquina virtual a qualquer momento e a configuração da primeira vez continuar.</span><span class="sxs-lookup"><span data-stu-id="16a78-120">**Note** You can close the virtual machine window at any time and first time setup continues.</span></span>

         

**<span data-ttu-id="16a78-121">Para verificar as configurações após a conclusão da instalação do programa pela primeira vez</span><span class="sxs-lookup"><span data-stu-id="16a78-121">To verify settings after first time setup finishes</span></span>**

1.  <span data-ttu-id="16a78-122">Verifique se a configuração da primeira vez foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="16a78-122">Ensure that first time setup finished successfully.</span></span>

2.  <span data-ttu-id="16a78-123">Verifique se o espaço de trabalho do MED-V está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="16a78-123">Verify that the MED-V workspace is set up correctly.</span></span>

    1.  <span data-ttu-id="16a78-124">Abra o console do Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="16a78-124">Open the Windows Virtual PC Console.</span></span>

        <span data-ttu-id="16a78-125">Clique em **Iniciar**, clique em **todos os programas**, clique em **PC virtual do Windows**e clique em **PC virtual do Windows**.</span><span class="sxs-lookup"><span data-stu-id="16a78-125">Click **Start**, click **All Programs**, click **Windows Virtual PC**, and then click **Windows Virtual PC**.</span></span>

    2.  <span data-ttu-id="16a78-126">Clique duas vezes no seu espaço de trabalho do MED-V instalado.</span><span class="sxs-lookup"><span data-stu-id="16a78-126">Double-click your installed MED-V workspace.</span></span>

        <span data-ttu-id="16a78-127">Se o espaço de trabalho do MED-V já estiver executando um aplicativo virtual, talvez você seja solicitado a fechar o aplicativo antes de poder abrir a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="16a78-127">If the MED-V workspace is already running a virtual application, you might be prompted to close the application before you can open the virtual machine.</span></span>

    3.  <span data-ttu-id="16a78-128">No espaço de trabalho do MED-V, clique com o botão direito do mouse em **meu computador**e, em seguida, clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="16a78-128">In the MED-V workspace, right-click **My Computer**, and then click **Properties**.</span></span>

    4.  <span data-ttu-id="16a78-129">Verifique se o espaço de trabalho do MED-V ingressou no domínio correto.</span><span class="sxs-lookup"><span data-stu-id="16a78-129">Verify that the MED-V workspace joined the correct domain.</span></span> <span data-ttu-id="16a78-130">Se aplicável à sua organização, teste o ingresso no domínio especificando dois domínios diferentes para verificar se o domínio de convidado é substituído pelo domínio host.</span><span class="sxs-lookup"><span data-stu-id="16a78-130">If applicable to your organization, test domain joining by specifying two different domains to verify that the guest domain is overridden by the host domain.</span></span>

    5.  <span data-ttu-id="16a78-131">Verifique se o espaço de trabalho do MED-V ingressou na unidade organizacional do domínio que você especificou.</span><span class="sxs-lookup"><span data-stu-id="16a78-131">Verify that the MED-V workspace joined the domain organizational unit that you specified.</span></span>

    6.  <span data-ttu-id="16a78-132">Se você especificou a máscara de nome do computador, verifique se o novo nome do computador corresponde ao que foi especificado.</span><span class="sxs-lookup"><span data-stu-id="16a78-132">If you specified the computer name mask, verify that the new computer name matches what was specified.</span></span>

3.  <span data-ttu-id="16a78-133">Verifique se as configurações de localidade especificadas estão corretas.</span><span class="sxs-lookup"><span data-stu-id="16a78-133">Verify that the locale settings that you specified are correct.</span></span>

    1.  <span data-ttu-id="16a78-134">No espaço de trabalho do MED-V, clique em **Iniciar** e em **painel de controle**.</span><span class="sxs-lookup"><span data-stu-id="16a78-134">In the MED-V workspace, click **Start** and then click **Control Panel**.</span></span>

    2.  <span data-ttu-id="16a78-135">Verifique as configurações especificadas, por exemplo, **data e hora** e **regionais e idioma**.</span><span class="sxs-lookup"><span data-stu-id="16a78-135">Verify your specified configuration settings, for example, **Date and Time** and **Regional and Language**.</span></span>

<span data-ttu-id="16a78-136">**Observação**  Se você tiver problemas ao verificar as configurações de configuração da primeira vez, consulte [solução de problemas de operações](operations-troubleshooting-medv2.md).</span><span class="sxs-lookup"><span data-stu-id="16a78-136">**Note** If you encounter any problems when verifying your first time setup settings, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

 

<span data-ttu-id="16a78-137">Depois de verificar se as configurações de configuração da primeira vez estão corretas, você pode testar outras configurações do espaço de trabalho do MED-V para verificar se elas funcionam conforme o esperado, como a publicação de aplicativos e o redirecionamento de URL.</span><span class="sxs-lookup"><span data-stu-id="16a78-137">After you have verified that your first time setup settings are correct, you can test other MED-V workspace configurations to verify that they function as intended, such as application publishing and URL redirection.</span></span>

<span data-ttu-id="16a78-138">Depois de concluir o teste do pacote do espaço de trabalho do MED-V e verificar se ele está funcionando conforme o esperado, você pode implantar o espaço de trabalho do MED-V na sua empresa.</span><span class="sxs-lookup"><span data-stu-id="16a78-138">After you have completed all testing of your MED-V workspace package and have verified that it is functioning as intended, you can deploy the MED-V workspace to your enterprise.</span></span>

## <span data-ttu-id="16a78-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="16a78-139">Related topics</span></span>


[<span data-ttu-id="16a78-140">Como testar a publicação de aplicativos</span><span class="sxs-lookup"><span data-stu-id="16a78-140">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="16a78-141">Como testar o redirecionamento da URL</span><span class="sxs-lookup"><span data-stu-id="16a78-141">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

[<span data-ttu-id="16a78-142">Como implantar o pacote de espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="16a78-142">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)

[<span data-ttu-id="16a78-143">Gerenciar configurações de espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="16a78-143">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





