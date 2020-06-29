---
title: Como desinstalar os componentes da MED-V
description: Como desinstalar os componentes da MED-V
author: dansimp
ms.assetid: c121dd27-6b2f-4d41-a21a-c6e8608c5c41
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 514ec8227b858b34289ca2330f7cfb038bc4f00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796147"
---
# <span data-ttu-id="fafd6-103">Como desinstalar os componentes da MED-V</span><span class="sxs-lookup"><span data-stu-id="fafd6-103">How to Uninstall the MED-V Components</span></span>


<span data-ttu-id="fafd6-104">Em determinadas circunstâncias, talvez você queira desinstalar todos ou parte dos componentes do 2,0 da virtualização de área de trabalho do Microsoft Enterprise (MED-V) de sua empresa.</span><span class="sxs-lookup"><span data-stu-id="fafd6-104">Under certain circumstances, you might want to uninstall all or part of the Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 components from your enterprise.</span></span> <span data-ttu-id="fafd6-105">Por exemplo, você solucionou todos os problemas de compatibilidade do sistema operacional do aplicativo ou deseja implantar um espaço de trabalho do MED-V diferente em sua empresa.</span><span class="sxs-lookup"><span data-stu-id="fafd6-105">For example, you have resolved all application operating system compatibility issues, or you want to deploy a different MED-V workspace in your enterprise.</span></span>

<span data-ttu-id="fafd6-106">Geralmente, você pode configurar o sistema ESD (distribuição de software eletrônico) para desinstalar os componentes do MED-V usando um instalador baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="fafd6-106">Typically, you can configure your electronic software distribution (ESD) system to uninstall the MED-V components by using a Windows-based Installer.</span></span> <span data-ttu-id="fafd6-107">Como alternativa, você pode desinstalar todos ou alguns componentes do MED-V manualmente.</span><span class="sxs-lookup"><span data-stu-id="fafd6-107">Alternately, you can uninstall all or some MED-V components manually.</span></span>

<span data-ttu-id="fafd6-108">**Importante**  Antes de desinstalar o agente de host do MED-V, você deve primeiro desinstalar qualquer espaço de trabalho do MED-V instalado.</span><span class="sxs-lookup"><span data-stu-id="fafd6-108">**Important** Before you can uninstall the MED-V Host Agent, you must first uninstall any installed MED-V workspace.</span></span>

 

<span data-ttu-id="fafd6-109">Use os procedimentos a seguir para desinstalar os componentes do MED-V da sua empresa.</span><span class="sxs-lookup"><span data-stu-id="fafd6-109">Use the following procedures to uninstall the MED-V components from your enterprise.</span></span>

**<span data-ttu-id="fafd6-110">Para desinstalar o MED-V usando um sistema de distribuição de software eletrônico</span><span class="sxs-lookup"><span data-stu-id="fafd6-110">To uninstall MED-V using an electronic software distribution System</span></span>**

1.  <span data-ttu-id="fafd6-111">Use o sistema ESD para distribuir um script que invoque o uninstall.exe programa executável para cada espaço de trabalho do MED-V que você deseja desinstalar.</span><span class="sxs-lookup"><span data-stu-id="fafd6-111">Use your ESD system to distribute a script that invokes the uninstall.exe executable program for every MED-V workspace that you want to uninstall.</span></span> <span data-ttu-id="fafd6-112">O arquivo está localizado em C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span><span class="sxs-lookup"><span data-stu-id="fafd6-112">The file is located at C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span></span> <span data-ttu-id="fafd6-113">Você pode definir um sinalizador para executar o programa de desinstalação executável silenciosamente para que os usuários finais não saibam a desinstalação.</span><span class="sxs-lookup"><span data-stu-id="fafd6-113">You can set a flag to run the uninstall executable program silently so that end users are unaware of the uninstallation.</span></span>

2.  <span data-ttu-id="fafd6-114">Crie um pacote para distribuir o arquivo de instalação do MED-V Host Agent para cada computador em que um espaço de trabalho do MED-V foi desinstalado.</span><span class="sxs-lookup"><span data-stu-id="fafd6-114">Create a package to distribute the MED-V Host Agent installation file to each computer on which a MED-V workspace was uninstalled.</span></span> <span data-ttu-id="fafd6-115">Configure o pacote para executar a desinstalação em modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="fafd6-115">Configure the package to run the uninstallation in silent mode.</span></span>

<span data-ttu-id="fafd6-116">O cliente ESD reconhece quando os novos pacotes estão disponíveis e começa a desinstalar os pacotes de acordo com a definição e os requisitos.</span><span class="sxs-lookup"><span data-stu-id="fafd6-116">The ESD client recognizes when the new packages are available and starts to uninstall the packages per the definition and requirements.</span></span>

**<span data-ttu-id="fafd6-117">Para desinstalar manualmente um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="fafd6-117">To manually uninstall a MED-V workspace</span></span>**

1.  <span data-ttu-id="fafd6-118">No computador host, clique em **Iniciar**, clique em **painel de controle**e, em seguida, clique em **programas e recursos**.</span><span class="sxs-lookup"><span data-stu-id="fafd6-118">On the host computer, click **Start**, click **Control Panel**, and then click **Programs and Features**.</span></span>

2.  <span data-ttu-id="fafd6-119">Na janela **programas e recursos** , selecione o espaço de trabalho do MED-V que você deseja remover e clique em **desinstalar**.</span><span class="sxs-lookup"><span data-stu-id="fafd6-119">In the **Programs and Features** window, select the MED-V workspace that you want to remove, and then click **Uninstall**.</span></span> <span data-ttu-id="fafd6-120">(O espaço de trabalho do MED-V é chamado de "espaço de trabalho do MED-V- &lt; *espaço de trabalho \ _name* &gt; ").</span><span class="sxs-lookup"><span data-stu-id="fafd6-120">(The MED-V workspace is named "MED-V Workspace - &lt;*workspace\_name*&gt;").</span></span> <span data-ttu-id="fafd6-121">O &lt; _name assistente de configuração do *espaço de trabalho* &gt; **Setup Wizard** é aberto.</span><span class="sxs-lookup"><span data-stu-id="fafd6-121">The &lt;*workspace\_name*&gt; **Setup Wizard** opens.</span></span>

3.  <span data-ttu-id="fafd6-122">No **Assistente de configuração**, clique em **Avançar**e, em seguida, clique em **remover**.</span><span class="sxs-lookup"><span data-stu-id="fafd6-122">On the **Setup Wizard**, click **Next**, and then click **Remove**.</span></span>

4.  <span data-ttu-id="fafd6-123">Se preferir, marque a caixa de seleção para excluir o disco VHD mestre e os discos diferenciais criados pelo MED-V.</span><span class="sxs-lookup"><span data-stu-id="fafd6-123">If you prefer, select the check box to delete the master VHD disk and differencing disks created by MED-V.</span></span> <span data-ttu-id="fafd6-124">Isso não é necessário, mas libera espaço em disco após o término da desinstalação.</span><span class="sxs-lookup"><span data-stu-id="fafd6-124">This is not required, but frees disk space after the uninstallation finishes.</span></span>

5.  <span data-ttu-id="fafd6-125">Clique em **remover**.</span><span class="sxs-lookup"><span data-stu-id="fafd6-125">Click **Remove**.</span></span>

    <span data-ttu-id="fafd6-126">**Observação**  Se o MED-V estiver sendo executado no momento, será exibida uma caixa de diálogo perguntando se você deseja desligá-la.</span><span class="sxs-lookup"><span data-stu-id="fafd6-126">**Note** If MED-V is currently running, a dialog box appears and prompts you whether you want to shut it down.</span></span> <span data-ttu-id="fafd6-127">Clique em **Sim** para continuar com a desinstalação.</span><span class="sxs-lookup"><span data-stu-id="fafd6-127">Click **Yes** to continue with the uninstallation.</span></span> <span data-ttu-id="fafd6-128">Clique em **não** para cancelar a desinstalação.</span><span class="sxs-lookup"><span data-stu-id="fafd6-128">Click **No** to cancel the uninstallation.</span></span>

     

<span data-ttu-id="fafd6-129">Como alternativa, você pode remover um espaço de trabalho do MED-V executando o `uninstall.exe` arquivo, normalmente localizado em C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span><span class="sxs-lookup"><span data-stu-id="fafd6-129">Alternately, you can remove a MED-V workspace by running the `uninstall.exe` file, typically located at C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span></span>

**<span data-ttu-id="fafd6-130">Para desinstalar manualmente o agente de host do MED-V</span><span class="sxs-lookup"><span data-stu-id="fafd6-130">To manually uninstall the MED-V Host Agent</span></span>**

1.  <span data-ttu-id="fafd6-131">No computador host do Windows 7, clique em **Iniciar**, clique em **painel de controle**e, em seguida, clique em **programas e recursos**.</span><span class="sxs-lookup"><span data-stu-id="fafd6-131">On the Windows 7 host computer, click **Start**, click **Control Panel**, and then click **Programs and Features**.</span></span>

2.  <span data-ttu-id="fafd6-132">Na janela **programas e recursos** , selecione **agente de host MED-V**e clique em **desinstalar**.</span><span class="sxs-lookup"><span data-stu-id="fafd6-132">In the **Programs and Features** window, select **MED-V Host Agent**, and then click **Uninstall**.</span></span>

    <span data-ttu-id="fafd6-133">O Windows Installer remove o agente de host MED-V.</span><span class="sxs-lookup"><span data-stu-id="fafd6-133">The Windows Installer removes the MED-V Host Agent.</span></span>

    <span data-ttu-id="fafd6-134">**Observação**  Se você tentar desinstalar o agente de host do MED-V antes de desinstalar o espaço de trabalho do MED-V, será exibida uma caixa de diálogo que diz que você deve primeiro desinstalar o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="fafd6-134">**Note** If you try to uninstall the MED-V Host Agent before you uninstall the MED-V workspace, a dialog box appears that states that you must first uninstall the MED-V workspace.</span></span> <span data-ttu-id="fafd6-135">Clique em **OK** para continuar.</span><span class="sxs-lookup"><span data-stu-id="fafd6-135">Click **OK** to continue.</span></span>

     

**<span data-ttu-id="fafd6-136">Para desinstalar manualmente o pacote do espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="fafd6-136">To manually uninstall the MED-V Workspace Packager</span></span>**

1.  <span data-ttu-id="fafd6-137">No computador host, clique em **Iniciar**, clique em **painel de controle**e, em seguida, clique em **programas e recursos**.</span><span class="sxs-lookup"><span data-stu-id="fafd6-137">On the host computer, click **Start**, click **Control Panel**, and then click **Programs and Features**.</span></span>

2.  <span data-ttu-id="fafd6-138">Na janela **programas e recursos** , selecione **pacote do espaço de trabalho do MED-V**e clique em **desinstalar**.</span><span class="sxs-lookup"><span data-stu-id="fafd6-138">In the **Programs and Features** window, select **MED-V Workspace Packager**, and then click **Uninstall**.</span></span>

    <span data-ttu-id="fafd6-139">O Windows Installer remove o pacote do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="fafd6-139">The Windows Installer removes the MED-V Workspace Packager.</span></span>

    <span data-ttu-id="fafd6-140">**Observação**  Você pode desinstalar o pacote do espaço de trabalho do MED-V a qualquer momento, sem afetar qualquer espaço de trabalho do MED-V implantado.</span><span class="sxs-lookup"><span data-stu-id="fafd6-140">**Note** You can uninstall the MED-V Workspace Packager at any time without affecting any deployed MED-V workspaces.</span></span>

     

## <span data-ttu-id="fafd6-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fafd6-141">Related topics</span></span>


[<span data-ttu-id="fafd6-142">Implantar os componentes da MED-V</span><span class="sxs-lookup"><span data-stu-id="fafd6-142">Deploy the MED-V Components</span></span>](deploy-the-med-v-components.md)

 

 





