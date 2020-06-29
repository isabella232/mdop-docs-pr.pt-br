---
title: Como implantar manualmente um espaço de trabalho da MED-V
description: Como implantar manualmente um espaço de trabalho da MED-V
author: dansimp
ms.assetid: 94bfb209-2230-49b6-bb40-9c6ab088dbf4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f13d06e2232681f87df7a71b9a3ef3269b4f9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800040"
---
# <span data-ttu-id="4d5f5-103">Como implantar manualmente um espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="4d5f5-103">How to Deploy a MED-V Workspace Manually</span></span>


<span data-ttu-id="4d5f5-104">Em alguns casos, talvez você queira implantar seu espaço de trabalho do MED-V manualmente, por exemplo, se a sua empresa não usar um sistema de distribuição de software eletrônico para implantar aplicativos.</span><span class="sxs-lookup"><span data-stu-id="4d5f5-104">In some instances, you might want to deploy your MED-V workspace manually, for example, if your company does not use an electronic software distribution system to deploy applications.</span></span>

<span data-ttu-id="4d5f5-105">Esta seção fornece instruções sobre como implantar manualmente um espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="4d5f5-105">This section provides instruction about how to manually deploy a MED-V workspace.</span></span>

**<span data-ttu-id="4d5f5-106">Para implantar um espaço de trabalho do MED-V manualmente</span><span class="sxs-lookup"><span data-stu-id="4d5f5-106">To deploy a MED-V workspace manually</span></span>**

1.  <span data-ttu-id="4d5f5-107">Copie todos os aplicativos de pré-requisito e os arquivos de pacote do espaço de trabalho do MED-V para uma unidade compartilhada ou um DVD.</span><span class="sxs-lookup"><span data-stu-id="4d5f5-107">Copy all prerequisite applications and the MED-V workspace package files to a shared drive or to a DVD.</span></span> <span data-ttu-id="4d5f5-108">Veja a seguir uma lista dos aplicativos e arquivos necessários.</span><span class="sxs-lookup"><span data-stu-id="4d5f5-108">The following is a list of the required applications and files.</span></span>

    -   <span data-ttu-id="4d5f5-109">**PC virtual do Windows**.</span><span class="sxs-lookup"><span data-stu-id="4d5f5-109">**Windows Virtual PC**.</span></span> <span data-ttu-id="4d5f5-110">Para obter mais informações, consulte [configurar pré-requisitos de instalação](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="4d5f5-110">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="4d5f5-111">**Adições e atualizações do Windows Virtual PC**.</span><span class="sxs-lookup"><span data-stu-id="4d5f5-111">**Windows Virtual PC Additions and Updates**.</span></span> <span data-ttu-id="4d5f5-112">Para obter mais informações, consulte [configurar pré-requisitos de instalação](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="4d5f5-112">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="4d5f5-113">**Arquivo de instalação do MED-v Host Agent** – instala o arquivo de instalação do Host Agent (MED-v \ _HostAgent \ _setup instalação).</span><span class="sxs-lookup"><span data-stu-id="4d5f5-113">**MED-V Host Agent Installation File** – installs the Host Agent (MED-V\_HostAgent\_Setup installation file).</span></span>

        **<span data-ttu-id="4d5f5-114">Aviso</span><span class="sxs-lookup"><span data-stu-id="4d5f5-114">Warning</span></span>**  
        <span data-ttu-id="4d5f5-115">Feche o Internet Explorer antes de instalar o agente de host do MED-V, caso contrário, pode ocorrer conflitos mais tarde com o redirecionamento de URL.</span><span class="sxs-lookup"><span data-stu-id="4d5f5-115">Close Internet Explorer before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="4d5f5-116">Você também pode fazer isso especificando uma reinicialização do computador durante uma distribuição.</span><span class="sxs-lookup"><span data-stu-id="4d5f5-116">You can also do this by specifying a computer restart during a distribution.</span></span>



~~~
-   **MED-V Workspace Installer, VHD, and Setup Executable** – created with the **MED-V Workspace Packager**. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    **Important**  
    The compressed VHD file (.medv) and the Setup executable program (setup.exe) must be in the same folder as the MED-V workspace installer.
~~~



2. <span data-ttu-id="4d5f5-117">Instale o seguinte na ordem listada.</span><span class="sxs-lookup"><span data-stu-id="4d5f5-117">Install the following in the order listed.</span></span> <span data-ttu-id="4d5f5-118">O usuário final pode executar essa tarefa manualmente ou você pode criar um script para instalar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="4d5f5-118">The end user can perform this task manually or you can create a script to install the following:</span></span>

   -   <span data-ttu-id="4d5f5-119">O Windows Virtual PC e o Windows Virtual PC Additions e atualizações.</span><span class="sxs-lookup"><span data-stu-id="4d5f5-119">Windows Virtual PC and the Windows Virtual PC additions and updates.</span></span> <span data-ttu-id="4d5f5-120">É preciso reiniciar o computador.</span><span class="sxs-lookup"><span data-stu-id="4d5f5-120">A computer restart is required.</span></span>

   -   <span data-ttu-id="4d5f5-121">O agente de host do MED-V.</span><span class="sxs-lookup"><span data-stu-id="4d5f5-121">The MED-V Host Agent.</span></span>

       **<span data-ttu-id="4d5f5-122">Observação</span><span class="sxs-lookup"><span data-stu-id="4d5f5-122">Note</span></span>**  
       <span data-ttu-id="4d5f5-123">Se estiver em execução, o Internet Explorer deve ser reiniciado para que a instalação do agente de host MED-V possa ser concluída.</span><span class="sxs-lookup"><span data-stu-id="4d5f5-123">If it is running, Internet Explorer must be restarted before the installation of the MED-V Host Agent can finish.</span></span>



~~~
-   The MED-V workspace package.

    Install the MED-V workspace by running the setup.exe program that is included in the MED-V workspace package files.
~~~

3. <span data-ttu-id="4d5f5-124">Conclua a configuração da primeira vez.</span><span class="sxs-lookup"><span data-stu-id="4d5f5-124">Complete first time setup.</span></span>

   <span data-ttu-id="4d5f5-125">Após a instalação do espaço de trabalho do MED-V, você tem a opção de iniciar o MED-V.</span><span class="sxs-lookup"><span data-stu-id="4d5f5-125">After the MED-V workspace is installed, you have the option of starting MED-V.</span></span> <span data-ttu-id="4d5f5-126">Isso inicia o agente do host MED-V.</span><span class="sxs-lookup"><span data-stu-id="4d5f5-126">This starts the MED-V Host Agent.</span></span> <span data-ttu-id="4d5f5-127">Você pode iniciar MED-V nesse momento ou iniciar o agente de host do MED-V mais tarde para concluir a configuração do primeiro horário.</span><span class="sxs-lookup"><span data-stu-id="4d5f5-127">You can either start MED-V at that time, or start the MED-V Host Agent later to complete first time setup.</span></span>

   <span data-ttu-id="4d5f5-128">Para iniciar o agente de host do MED-V, clique em **Iniciar**, em **todos os programas**, em **virtualização de área de trabalho do Microsoft Enterprise**e clique em **agente de host do MED-v**.</span><span class="sxs-lookup"><span data-stu-id="4d5f5-128">To start the MED-V Host Agent, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

## <span data-ttu-id="4d5f5-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d5f5-129">Related topics</span></span>


[<span data-ttu-id="4d5f5-130">Como implantar um espaço de trabalho da MED-V por meio de um sistema de distribuição eletrônica de software</span><span class="sxs-lookup"><span data-stu-id="4d5f5-130">How to Deploy a MED-V Workspace Through an Electronic Software Distribution System</span></span>](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

[<span data-ttu-id="4d5f5-131">Como implantar um espaço de trabalho da MED-V em uma imagem do Windows 7</span><span class="sxs-lookup"><span data-stu-id="4d5f5-131">How to Deploy a MED-V Workspace in a Windows 7 Image</span></span>](how-to-deploy-a-med-v-workspace-in-a-windows-7-image.md)

[<span data-ttu-id="4d5f5-132">Como implantar o pacote de espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="4d5f5-132">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)









