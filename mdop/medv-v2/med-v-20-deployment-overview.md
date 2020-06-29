---
title: Visão geral da implantação da MED-V 2.0
description: Visão geral da implantação da MED-V 2.0
author: dansimp
ms.assetid: 0b8998ea-c46f-4c81-a304-f380b2ed7cf8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ec2a5f86ac7d63295bd7c550bcb0a90004987e42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799806"
---
# <span data-ttu-id="7e282-103">Visão geral da implantação da MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="7e282-103">MED-V 2.0 Deployment Overview</span></span>


<span data-ttu-id="7e282-104">Esta seção fornece informações gerais e instruções sobre como instalar e implantar o Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="7e282-104">This section provides general information and instructions about how to install and deploy Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="7e282-105">Visão geral</span><span class="sxs-lookup"><span data-stu-id="7e282-105">Overview</span></span>


<span data-ttu-id="7e282-106">O MED-V 2,0 se baseia em um modelo de aplicativo, em que os mesmos métodos usados para implantar aplicativos podem ser usados para implantar e gerenciar o MED-V.</span><span class="sxs-lookup"><span data-stu-id="7e282-106">MED-V 2.0 is based on an application model, where the same methods that you use to deploy applications can be used to deploy and manage MED-V.</span></span> <span data-ttu-id="7e282-107">Uma solução MED-V implantada inclui dois componentes: o agente de host e o agente de convidado do MED-V.</span><span class="sxs-lookup"><span data-stu-id="7e282-107">A deployed MED-V solution includes two components: the MED-V Host Agent and Guest Agent.</span></span> <span data-ttu-id="7e282-108">O agente de host do MED-V está instalado na área de trabalho do Windows 7 e o agente de convidado do MED-V está instalado no Windows XP dentro do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="7e282-108">The MED-V Host Agent is installed on the Windows 7 desktop and the MED-V Guest Agent is installed on Windows XP inside the MED-V workspace.</span></span> <span data-ttu-id="7e282-109">O MED-V também inclui um pacote do espaço de trabalho do MED-V que fornece as informações e as ferramentas necessárias para criar e configurar os espaços de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="7e282-109">MED-V also includes a MED-V Workspace Packager that provides the information and tools necessary for creating and configuring MED-V workspaces.</span></span>

**<span data-ttu-id="7e282-110">Importante</span><span class="sxs-lookup"><span data-stu-id="7e282-110">Important</span></span>**  
<span data-ttu-id="7e282-111">O MED-V só oferece suporte à instalação do pacote do espaço de trabalho do MED-V, ao agente de host do MED-V e ao espaço de trabalho do MED-v para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="7e282-111">MED-V only supports the installation of the MED-V Workspace Packager, the MED-V Host Agent, and the MED-V workspace for all users.</span></span> <span data-ttu-id="7e282-112">A instalação do MED-V para o usuário atual somente selecionando **ALLUSERS = ""** causa falhas na instalação dos componentes e na configuração do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="7e282-112">Installing MED-V for the current user only by selecting **ALLUSERS=””** causes failures in the installation of the components and in the setup of the MED-V workspace.</span></span>



### <span data-ttu-id="7e282-113">Os arquivos de instalação do MED-V</span><span class="sxs-lookup"><span data-stu-id="7e282-113">The MED-V Installation Files</span></span>

<span data-ttu-id="7e282-114">O MED-V inclui os seguintes arquivos de instalação, necessários para executar o MED-V:</span><span class="sxs-lookup"><span data-stu-id="7e282-114">MED-V includes the following installation files, required for running MED-V:</span></span>

**<span data-ttu-id="7e282-115">O arquivo de instalação do MED-V Host Agent</span><span class="sxs-lookup"><span data-stu-id="7e282-115">The MED-V Host Agent Installation File</span></span>**

<span data-ttu-id="7e282-116">O arquivo de instalação do Host Agent é chamado de MED-V\_HostAgent\_Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="7e282-116">The Host Agent installation file is named MED-V\_HostAgent\_Setup.exe.</span></span> <span data-ttu-id="7e282-117">Esse arquivo é distribuído e instalado em cada computador de usuário final relevante como parte de sua implantação de toda a empresa do MED-V.</span><span class="sxs-lookup"><span data-stu-id="7e282-117">This file is distributed and installed on each relevant end-user computer as part of your enterprise-wide deployment of MED-V.</span></span>

**<span data-ttu-id="7e282-118">O arquivo de instalação do pacote do espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="7e282-118">The MED-V Workspace Packager Installation File</span></span>**

<span data-ttu-id="7e282-119">O arquivo de instalação do pacote do espaço de trabalho do MED-V é chamado MED-V\_WorkspacePackager\_Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="7e282-119">The MED-V Workspace Packager installation file is named MED-V\_WorkspacePackager\_Setup.exe.</span></span> <span data-ttu-id="7e282-120">Use esse arquivo para instalar o pacote do espaço de trabalho do MED-V em um computador no qual você tenha direitos e permissões de administrador.</span><span class="sxs-lookup"><span data-stu-id="7e282-120">Use this file to install the MED-V Workspace Packager on a computer where you have administrator rights and permissions.</span></span> <span data-ttu-id="7e282-121">O administrador da área de trabalho usa o pacote do espaço de trabalho do MED-V para criar e gerenciar os espaços de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="7e282-121">The desktop administrator uses the MED-V Workspace Packager to create and manage MED-V workspaces.</span></span>

**<span data-ttu-id="7e282-122">Observação</span><span class="sxs-lookup"><span data-stu-id="7e282-122">Note</span></span>**  
<span data-ttu-id="7e282-123">O agente de convidado do MED-V é instalado automaticamente durante a primeira configuração.</span><span class="sxs-lookup"><span data-stu-id="7e282-123">The MED-V Guest Agent is installed automatically during first time setup.</span></span>



### <span data-ttu-id="7e282-124">O processo de implantação do MED-V</span><span class="sxs-lookup"><span data-stu-id="7e282-124">The MED-V Deployment Process</span></span>

<span data-ttu-id="7e282-125">Veja a seguir uma visão geral de alto nível do processo de instalação e implantação do MED-V:</span><span class="sxs-lookup"><span data-stu-id="7e282-125">The following is a high-level overview of the MED-V installation and deployment process:</span></span>

1.  <span data-ttu-id="7e282-126">Instale o pacote do espaço de trabalho do MED-V no computador em que você tem credenciais administrativas e que você usará para construir os pacotes do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="7e282-126">Install the MED-V Workspace Packager on the computer where you have administrative credentials and that you will be using to build the MED-V workspace packages.</span></span> <span data-ttu-id="7e282-127">Para obter mais informações, consulte [como instalar o pacote do espaço de trabalho do MED-V](how-to-install-the-med-v-workspace-packager.md).</span><span class="sxs-lookup"><span data-stu-id="7e282-127">For more information, see [How to Install the MED-V Workspace Packager](how-to-install-the-med-v-workspace-packager.md).</span></span>

2.  <span data-ttu-id="7e282-128">Prepare sua imagem do MED-V e crie seus pacotes de espaço de trabalho do MED-V usando o pacote do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="7e282-128">Prepare your MED-V image and create your MED-V workspace packages by using the MED-V Workspace Packager.</span></span> <span data-ttu-id="7e282-129">Para obter mais informações, consulte [operações do MED-V](operations-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="7e282-129">For more information, see [Operations for MED-V](operations-for-med-v.md).</span></span>

3.  <span data-ttu-id="7e282-130">Implante os componentes do MED-V necessários em toda a sua empresa.</span><span class="sxs-lookup"><span data-stu-id="7e282-130">Deploy the required MED-V components throughout your enterprise.</span></span> <span data-ttu-id="7e282-131">Os componentes obrigatórios do MED-V são do Windows Virtual PC, do MED-V Host Agent e do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="7e282-131">The required components of MED-V are Windows Virtual PC, the MED-V Host Agent, and the MED-V workspace.</span></span>

**<span data-ttu-id="7e282-132">Importante</span><span class="sxs-lookup"><span data-stu-id="7e282-132">Important</span></span>**  
<span data-ttu-id="7e282-133">A instalação dos componentes do MED-V requer credenciais administrativas.</span><span class="sxs-lookup"><span data-stu-id="7e282-133">Installation of the MED-V components requires administrative credentials.</span></span> <span data-ttu-id="7e282-134">Se um usuário final estiver instalando o MED-V, ele será solicitado a inserir credenciais administrativas.</span><span class="sxs-lookup"><span data-stu-id="7e282-134">If an end user is installing MED-V, they are prompted to enter administrative credentials.</span></span> <span data-ttu-id="7e282-135">Como alternativa, as credenciais administrativas podem ser fornecidas no contexto se você estiver instalando usando um sistema ESD (Electronic Software Distribution).</span><span class="sxs-lookup"><span data-stu-id="7e282-135">Alternately, administrative credentials can be provided in context if you are installing by using an electronic software distribution (ESD) system.</span></span>



### <span data-ttu-id="7e282-136">Componentes do MED-V</span><span class="sxs-lookup"><span data-stu-id="7e282-136">The MED-V Components</span></span>

<span data-ttu-id="7e282-137">Os componentes do MED-V que você implanta em toda a sua empresa consistem nos seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="7e282-137">The MED-V components that you deploy throughout your enterprise consist of the following:</span></span>

**<span data-ttu-id="7e282-138">PC virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="7e282-138">Windows Virtual PC</span></span>**

<span data-ttu-id="7e282-139">Funções do MED-V nas imagens do PC virtual do Windows para sua solução de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="7e282-139">MED-V functions inside Windows Virtual PC images for its compatibility solution.</span></span> <span data-ttu-id="7e282-140">O PC virtual do Windows e a atualização para Windows 7 (KB977206) são necessários.</span><span class="sxs-lookup"><span data-stu-id="7e282-140">Windows Virtual PC and the update for Windows 7 (KB977206) are required.</span></span> <span data-ttu-id="7e282-141">Para obter mais informações, consulte [configurar pré-requisitos de instalação](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="7e282-141">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

**<span data-ttu-id="7e282-142">O arquivo de instalação do MED-V Host Agent</span><span class="sxs-lookup"><span data-stu-id="7e282-142">The MED-V Host Agent Installation File</span></span>**

<span data-ttu-id="7e282-143">MED-V\_HostAgent\_Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="7e282-143">MED-V\_HostAgent\_Setup.exe.</span></span>

**<span data-ttu-id="7e282-144">Os arquivos de instalação do espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="7e282-144">The MED-V Workspace Installation Files</span></span>**

<span data-ttu-id="7e282-145">Os arquivos de instalação do espaço de trabalho do MED-V são criados quando você cria o pacote do espaço de trabalho do MED-v que consiste no seguinte:</span><span class="sxs-lookup"><span data-stu-id="7e282-145">The MED-V workspace installation files are created when you build your MED-V workspace package that consists of the following:</span></span>

<span data-ttu-id="7e282-146">Um programa executável setup.exe que executa a instalação do espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="7e282-146">A setup.exe executable program that executes the MED-V workspace installation</span></span>

<span data-ttu-id="7e282-147">Um &lt; instalador do MED-V \ _workspace \ _name &gt; . msi</span><span class="sxs-lookup"><span data-stu-id="7e282-147">A &lt;MED-V\_workspace\_name&gt;.msi installer</span></span>

<span data-ttu-id="7e282-148">Um &lt; arquivo VHD \ _filename &gt; . medv, que é o disco rígido virtual compactado</span><span class="sxs-lookup"><span data-stu-id="7e282-148">A &lt;VHD\_filename&gt;.medv file, which is the compressed virtual hard disk</span></span>

<span data-ttu-id="7e282-149">Os arquivos para configurações de configuração ( &lt; espaço de trabalho \ _name &gt; . reg e &lt; espaço de trabalho \ _name &gt; . ps1)</span><span class="sxs-lookup"><span data-stu-id="7e282-149">The files for configuration settings (&lt;workspace\_name&gt;.reg and &lt;workspace\_name&gt;.ps1)</span></span>

<span data-ttu-id="7e282-150">Para implantar o MED-V, copie todos os arquivos de instalação necessários para o computador host ou para um compartilhamento que possa ser acessado pelo computador host.</span><span class="sxs-lookup"><span data-stu-id="7e282-150">To deploy MED-V, copy all the required installation files to the host computer or to a share that can be accessed by the host computer.</span></span> <span data-ttu-id="7e282-151">Execute os arquivos de instalação do componente para o PC virtual do Windows, o agente do host do MED-V e o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="7e282-151">Run the component installation files for Windows Virtual PC, the MED-V Host Agent, and the MED-V workspace.</span></span> <span data-ttu-id="7e282-152">Em seguida, inicie o agente do host do MED-V para concluir a configuração inicial do MED-V.</span><span class="sxs-lookup"><span data-stu-id="7e282-152">Then start the MED-V Host Agent to complete the first time setup of MED-V.</span></span>

<span data-ttu-id="7e282-153">Você pode executar a instalação manualmente.</span><span class="sxs-lookup"><span data-stu-id="7e282-153">You can perform the installation manually.</span></span> <span data-ttu-id="7e282-154">No entanto, recomendamos que você use um método de distribuição de software eletrônico para automatizar a implantação dos componentes.</span><span class="sxs-lookup"><span data-stu-id="7e282-154">However, we recommend that you use an electronic software distribution method to automate the deployment of the components.</span></span> <span data-ttu-id="7e282-155">Para obter mais informações, consulte [como implantar um espaço de trabalho do MED-V por meio de um sistema de distribuição de software eletrônico](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md).</span><span class="sxs-lookup"><span data-stu-id="7e282-155">For more information, see [How to Deploy a MED-V Workspace Through an Electronic Software Distribution System](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md).</span></span>

**<span data-ttu-id="7e282-156">Observação</span><span class="sxs-lookup"><span data-stu-id="7e282-156">Note</span></span>**  
<span data-ttu-id="7e282-157">Para obter informações sobre argumentos de linha de comando disponíveis para controlar as opções de instalação, consulte [Opções de linha de comando para arquivos de instalação do MED-V](command-line-options-for-med-v-installation-files.md).</span><span class="sxs-lookup"><span data-stu-id="7e282-157">For information about available command-line arguments to control install options, see [Command-Line Options for MED-V Installation Files](command-line-options-for-med-v-installation-files.md).</span></span>



## <span data-ttu-id="7e282-158">Etapas de implantação</span><span class="sxs-lookup"><span data-stu-id="7e282-158">Deployment Steps</span></span>


<span data-ttu-id="7e282-159">Ao implantar o MED-V em toda a sua empresa, há duas considerações principais: instalação e configuração da primeira vez.</span><span class="sxs-lookup"><span data-stu-id="7e282-159">When you deploy MED-V throughout your enterprise, there are two main considerations: installation and first time setup.</span></span>

### <span data-ttu-id="7e282-160">Instalação</span><span class="sxs-lookup"><span data-stu-id="7e282-160">Installation</span></span>

1.  <span data-ttu-id="7e282-161">**PC virtual do Windows** -durante a instalação, o MED-V verifica o computador virtual do Windows e a atualização necessária para o Windows 7 (KB977206).</span><span class="sxs-lookup"><span data-stu-id="7e282-161">**Windows Virtual PC** - During installation, MED-V checks for Windows Virtual PC and its required update for Windows 7 (KB977206).</span></span> <span data-ttu-id="7e282-162">Para obter mais informações, consulte [configurar pré-requisitos de instalação](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="7e282-162">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    <span data-ttu-id="7e282-163">Você pode instalá-los como parte das instalações do Windows 7 antes de instalar o MED-V ou pode instalá-los como parte da distribuição do MED-V.</span><span class="sxs-lookup"><span data-stu-id="7e282-163">You can install these as part of the Windows 7 installations before you install MED-V, or you can install them as part of the MED-V distribution.</span></span> <span data-ttu-id="7e282-164">No entanto, o MED-V não inclui um mecanismo para a implantação; Elas devem ser implantadas usando um sistema ESD (Electronic Software Distribution) ou parte da imagem do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7e282-164">However, MED-V does not include a mechanism for their deployment; they must be deployed by using an electronic software distribution (ESD) system or as part of the Windows 7 image.</span></span>

    **<span data-ttu-id="7e282-165">Importante</span><span class="sxs-lookup"><span data-stu-id="7e282-165">Important</span></span>**  
    <span data-ttu-id="7e282-166">Ao instalar os componentes do MED-V usando um arquivo em lotes, uma prática recomendada é especificar que o Windows Virtual PC e o hotfix do Windows Virtual PC são instalados após o pacote de host do MED-V e os arquivos de pacote do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="7e282-166">When you install the MED-V components by using a batch file, a best practice is to specify that Windows Virtual PC and the Windows Virtual PC hotfix are installed after the MED-V Host Agent and the MED-V workspace package files.</span></span> <span data-ttu-id="7e282-167">Isso significa que o Windows Update não causará interferência com o processo de instalação exigindo uma reinicialização.</span><span class="sxs-lookup"><span data-stu-id="7e282-167">This means that Windows Update will not cause any interference with the installation process by requiring a restart.</span></span>



~~~
**Note**  
After you install Windows Virtual PC, the computer must be restarted.
~~~



2. <span data-ttu-id="7e282-168">**Agente de host do MED-v** – instale o agente de host do MED-v no computador com Windows 7 em que o MED-v será executado.</span><span class="sxs-lookup"><span data-stu-id="7e282-168">**MED-V Host Agent** – Install the MED-V Host Agent on the Windows 7 computer where MED-V will be run.</span></span> <span data-ttu-id="7e282-169">Isso deve ser instalado antes da instalação do espaço de trabalho do MED-V e verifica se o computador virtual do Windows está instalado.</span><span class="sxs-lookup"><span data-stu-id="7e282-169">This must be installed before installing the MED-V workspace and checks to make sure that Windows Virtual PC is installed.</span></span>

3. <span data-ttu-id="7e282-170">**Espaço de trabalho do MED-v** – você cria os arquivos necessários nesta instalação usando o pacote do espaço de trabalho do MED-v: os arquivos setup.exe,. medv e. msi.</span><span class="sxs-lookup"><span data-stu-id="7e282-170">**MED-V workspace** – You create the files that are required in this installation by using the MED-V Workspace Packager: the setup.exe, .medv, and .msi files.</span></span> <span data-ttu-id="7e282-171">Para instalar o espaço de trabalho do MED-V, execute setup.exe; Isso aciona os outros arquivos conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="7e282-171">To install the MED-V workspace, run setup.exe; this triggers the other files as required.</span></span> <span data-ttu-id="7e282-172">A instalação coloca uma entrada no registro sob a chave de execução do computador local para iniciar o agente de host do MED-V, que sempre executa o MED-V quando o Windows for iniciado.</span><span class="sxs-lookup"><span data-stu-id="7e282-172">The installation places an entry in the registry under the local machine run key to start the MED-V Host Agent, which always runs MED-V when Windows is started.</span></span>

   **<span data-ttu-id="7e282-173">Importante</span><span class="sxs-lookup"><span data-stu-id="7e282-173">Important</span></span>**  
   <span data-ttu-id="7e282-174">A instalação do espaço de trabalho do MED-V pode ser executada interativamente pelo usuário final ou silenciosamente por meio de um sistema de distribuição de software eletrônico.</span><span class="sxs-lookup"><span data-stu-id="7e282-174">The installation of the MED-V workspace can be run interactively by the end user or silently through an electronic software distribution system.</span></span> <span data-ttu-id="7e282-175">A instalação do espaço de trabalho do MED-V requer credenciais administrativas, portanto, os usuários finais devem ser administradores de seus computadores para instalar o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="7e282-175">Installation of the MED-V workspace requires administrative credentials, so end users must be administrators of their computers to install the MED-V workspace.</span></span> <span data-ttu-id="7e282-176">Como alternativa, um sistema de distribuição de software eletrônico geralmente é executado no contexto do sistema e tem permissões suficientes.</span><span class="sxs-lookup"><span data-stu-id="7e282-176">Alternately, an electronic software distribution system typically runs in the system context and has sufficient permissions.</span></span>



~~~
**Tip**  
Because of problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.
~~~



### <span data-ttu-id="7e282-177">Configuração da primeira vez</span><span class="sxs-lookup"><span data-stu-id="7e282-177">First Time Setup</span></span>

<span data-ttu-id="7e282-178">Após a instalação do MED-V e dos componentes obrigatórios, o MED-V deve ser configurado.</span><span class="sxs-lookup"><span data-stu-id="7e282-178">After MED-V and its required components are installed, MED-V must be configured.</span></span> <span data-ttu-id="7e282-179">A configuração do MED-V é conhecida como configuração pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="7e282-179">The configuration of MED-V is known as first time setup.</span></span> <span data-ttu-id="7e282-180">Usando o **pacote do espaço de trabalho do MED-V**, você pode configurar a primeira vez que a configuração seja executada silenciosa ou interativamente.</span><span class="sxs-lookup"><span data-stu-id="7e282-180">By using the **MED-V Workspace Packager**, you can configure first time setup to run silently or interactively.</span></span> <span data-ttu-id="7e282-181">A configuração da primeira vez do MED-V exige que os usuários finais insiram a senha para se autenticarem no espaço de trabalho do MED-V, mas, caso contrário, podem ser praticamente invisíveis ao usuário.</span><span class="sxs-lookup"><span data-stu-id="7e282-181">First time setup of MED-V requires end users to enter their password to authenticate to the MED-V workspace, but otherwise can be almost invisible to the user.</span></span> <span data-ttu-id="7e282-182">As notificações são mostradas na área de notificação, como quando a instalação é concluída pela primeira vez e os aplicativos estão prontos.</span><span class="sxs-lookup"><span data-stu-id="7e282-182">Notifications are shown in the notification area, such as when first time setup is complete and applications are ready.</span></span> <span data-ttu-id="7e282-183">Veja a seguir as ações que ocorrem durante a configuração do MED-V na primeira vez:</span><span class="sxs-lookup"><span data-stu-id="7e282-183">The following are the actions that occur during first time setup of MED-V:</span></span>

1.  <span data-ttu-id="7e282-184">O disco rígido virtual deve ser configurado.</span><span class="sxs-lookup"><span data-stu-id="7e282-184">The virtual hard disk must be configured.</span></span> <span data-ttu-id="7e282-185">A mini-instalação é executada e expande a imagem do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7e282-185">Mini-Setup runs and expands the Windows XP image.</span></span> <span data-ttu-id="7e282-186">Geralmente, isso ocorre em uma janela oculta, mas o MED-V pode ser configurado para ser exibido durante essa configuração.</span><span class="sxs-lookup"><span data-stu-id="7e282-186">Typically, this occurs in a hidden window, but MED-V can be configured to display during this configuration.</span></span>

2.  <span data-ttu-id="7e282-187">Após a conclusão da mini-instalação, você pode executar comandos que devem ter para configuração adicional, como a instalação do software ESD ou de outros aplicativos ou a configuração da imagem.</span><span class="sxs-lookup"><span data-stu-id="7e282-187">After Mini-Setup finishes, you can run commands that you must have for additional configuration, such as installing ESD software or other applications, or configuring the image.</span></span> <span data-ttu-id="7e282-188">Elas podem ser chamadas no arquivo Sysprep. inf, mas não são necessárias.</span><span class="sxs-lookup"><span data-stu-id="7e282-188">These can be called in the Sysprep.inf file, but are not required there.</span></span> <span data-ttu-id="7e282-189">Para obter mais informações, consulte [Configurando uma imagem do Windows Virtual PC para MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="7e282-189">For more information, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

3.  <span data-ttu-id="7e282-190">Ftscompletion.exe é executado como a última etapa na configuração.</span><span class="sxs-lookup"><span data-stu-id="7e282-190">Ftscompletion.exe is run as the last step in configuration.</span></span> <span data-ttu-id="7e282-191">Esse processo conclui a configuração do MED-V, adiciona o usuário ao grupo RDP para permitir que eles acessem o espaço de trabalho do MED-V, copie os logs, sinalizem o MED-V de que o espaço de trabalho do MED-V está pronto e, em seguida, reinicia o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="7e282-191">This process completes the MED-V configuration, adds the user to the RDP group to let them access the MED-V workspace, copies logs, signals MED-V that the MED-V workspace is ready, and then restarts the MED-V workspace.</span></span> <span data-ttu-id="7e282-192">Esse processo também pode adicionar o usuário como administrador do espaço de trabalho do MED-V se ele tiver sido configurado quando o espaço de trabalho do MED-V foi criado.</span><span class="sxs-lookup"><span data-stu-id="7e282-192">This process can also add the user as an administrator of the MED-V workspace if this was configured when the MED-V workspace was created.</span></span> <span data-ttu-id="7e282-193">Ftscompletion.exe geralmente é chamado pelo arquivo Sysprep, inf, mas também pode ser executado por meio de outro método, como um script.</span><span class="sxs-lookup"><span data-stu-id="7e282-193">Ftscompletion.exe is typically called through the Sysprep,inf file but can also be run through another method, such as a script.</span></span> <span data-ttu-id="7e282-194">No entanto, Ftscompletion.exe deve ser a última ação que é executada quando a estação de trabalho está configurada.</span><span class="sxs-lookup"><span data-stu-id="7e282-194">However, Ftscompletion.exe must be the last action that is performed when the workstation is configured.</span></span> <span data-ttu-id="7e282-195">Para obter mais informações, consulte [Configurando uma imagem do Windows Virtual PC para MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="7e282-195">For more information, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

4.  <span data-ttu-id="7e282-196">Após a reinicialização do espaço de trabalho do MED-V pela Ftscompletion.exe, o usuário final está conectado.</span><span class="sxs-lookup"><span data-stu-id="7e282-196">After the MED-V workspace is restarted by Ftscompletion.exe, the end user is logged on.</span></span> <span data-ttu-id="7e282-197">Se ele não tiver salvo a senha durante a primeira instalação, ele será solicitado a fazê-lo novamente.</span><span class="sxs-lookup"><span data-stu-id="7e282-197">If they did not save their password during first time setup, they are prompted for it again.</span></span> <span data-ttu-id="7e282-198">O espaço de trabalho do MED-V é iniciado e configurado para o usuário.</span><span class="sxs-lookup"><span data-stu-id="7e282-198">The MED-V workspace is then started and configured for the user.</span></span> <span data-ttu-id="7e282-199">A configuração inclui a aplicação da política de grupo.</span><span class="sxs-lookup"><span data-stu-id="7e282-199">Configuration includes applying Group Policy.</span></span>

    <span data-ttu-id="7e282-200">Recomendamos que você aplique apenas as políticas que fazem sentido em um ambiente de compatibilidade do aplicativo para Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7e282-200">We recommend that you apply only those policies that make sense in an application compatibility environment for Windows XP.</span></span> <span data-ttu-id="7e282-201">Por exemplo, as políticas de personalização da área de trabalho normalmente não precisam ser aplicadas e devem ser desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="7e282-201">For example, desktop personalization policies do not typically need to be applied and should be disabled.</span></span> <span data-ttu-id="7e282-202">Para obter mais informações sobre como permitir somente perfis locais, consulte [configurações de política de grupo para perfis de usuário móvel](https://go.microsoft.com/fwlink/?LinkId=205072) ( https://go.microsoft.com/fwlink/?LinkId=205072) .</span><span class="sxs-lookup"><span data-stu-id="7e282-202">For more information about how to allow only local profiles, see [Group Policy Settings for Roaming User Profiles](https://go.microsoft.com/fwlink/?LinkId=205072) (https://go.microsoft.com/fwlink/?LinkId=205072).</span></span>

<span data-ttu-id="7e282-203">Depois que a configuração for concluída pela primeira vez, o usuário final será notificado de que os aplicativos publicados estão prontos.</span><span class="sxs-lookup"><span data-stu-id="7e282-203">After first time setup is complete, the end user is notified that the published applications are ready.</span></span> <span data-ttu-id="7e282-204">Eles poderão, então, acessar os aplicativos instalados no espaço de trabalho do MED-V a partir do menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="7e282-204">They are then able to access the applications installed in the MED-V workspace from their **Start** menu.</span></span>

## <span data-ttu-id="7e282-205">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7e282-205">Related topics</span></span>


[<span data-ttu-id="7e282-206">Preparar o ambiente de implantação para a MED-V</span><span class="sxs-lookup"><span data-stu-id="7e282-206">Prepare the Deployment Environment for MED-V</span></span>](prepare-the-deployment-environment-for-med-v.md)

[<span data-ttu-id="7e282-207">Implantação da MED-V</span><span class="sxs-lookup"><span data-stu-id="7e282-207">Deployment of MED-V</span></span>](deployment-of-med-v.md)









