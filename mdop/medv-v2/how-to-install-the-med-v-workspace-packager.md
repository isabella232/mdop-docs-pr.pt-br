---
title: Como instalar o empacotador de espaço de trabalho da MED-V
description: Como instalar o empacotador de espaço de trabalho da MED-V
author: dansimp
ms.assetid: 627478e9-6798-4b32-9a50-7a1b72bea295
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e23492852813752f028ae2201e656162d6189642
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799554"
---
# <span data-ttu-id="3d02a-103">Como instalar o empacotador de espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="3d02a-103">How to Install the MED-V Workspace Packager</span></span>


<span data-ttu-id="3d02a-104">O Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 inclui um **pacote do espaço de trabalho do MED-v**, que o administrador da área de trabalho usa para criar os pacotes de implantação do espaço de trabalho do MED-v que são distribuídos para os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="3d02a-104">Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 includes a **MED-V Workspace Packager**, which the desktop administrator uses to create the MED-V workspace deployment packages that are distributed to the end users.</span></span> <span data-ttu-id="3d02a-105">O packager fornece uma orientação passo a passo sobre como criar espaços de trabalho do MED-V e contém assistentes que ajudam no processo.</span><span class="sxs-lookup"><span data-stu-id="3d02a-105">The packager provides step-by-step guidance on how to create MED-V workspaces and contains wizards that help in the process.</span></span>

<span data-ttu-id="3d02a-106">**Importante**  Antes de começar a executar os assistentes, certifique-se de ter um VHD preparado pronto para instalar.</span><span class="sxs-lookup"><span data-stu-id="3d02a-106">**Important** Before you start to run the wizards, make sure that you have a prepared VHD ready to install.</span></span> <span data-ttu-id="3d02a-107">Para obter mais informações, consulte [preparar uma imagem do MED-V](prepare-a-med-v-image.md).</span><span class="sxs-lookup"><span data-stu-id="3d02a-107">For more information, see [Prepare a MED-V Image](prepare-a-med-v-image.md).</span></span>

 

<span data-ttu-id="3d02a-108">Esta seção fornece instruções passo a passo para instalar ou reparar o pacote do espaço de **trabalho do MED-V**.</span><span class="sxs-lookup"><span data-stu-id="3d02a-108">This section provides step-by-step instructions for installing or repairing the **MED-V Workspace Packager**.</span></span>

**<span data-ttu-id="3d02a-109">Para instalar o pacote do espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="3d02a-109">To install the MED-V Workspace Packager</span></span>**

1.  <span data-ttu-id="3d02a-110">Localize os arquivos de instalação do MED-V recebidos como parte do download do software.</span><span class="sxs-lookup"><span data-stu-id="3d02a-110">Locate the MED-V installation files that you received as part of your software download.</span></span>

2.  <span data-ttu-id="3d02a-111">Clique duas vezes no arquivo de instalação do MED-V \ _WorkspacePackager \ _Setup.</span><span class="sxs-lookup"><span data-stu-id="3d02a-111">Double-click the MED-V\_WorkspacePackager\_Setup installation file.</span></span>

    <span data-ttu-id="3d02a-112">O assistente de **configuração do pacote do espaço de trabalho do Microsoft Enterprise Desktop Virtualization (MED-V)** é aberto.</span><span class="sxs-lookup"><span data-stu-id="3d02a-112">The **Microsoft Enterprise Desktop Virtualization (MED-V) Workspace Packager Setup** wizard opens.</span></span> <span data-ttu-id="3d02a-113">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="3d02a-113">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="3d02a-114">Aceite os termos de licença para software Microsoft e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="3d02a-114">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="3d02a-115">Selecione a pasta de destino para instalar o pacote do espaço de trabalho do MED-V e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="3d02a-115">Select the destination folder for installing the MED-V Workspace Packager, and then click **Next**.</span></span>

5.  <span data-ttu-id="3d02a-116">Para começar a instalação, clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="3d02a-116">To begin the installation, click **Install**.</span></span>

6.  <span data-ttu-id="3d02a-117">Depois que a instalação for concluída com êxito, clique em **concluir** para fechar o assistente.</span><span class="sxs-lookup"><span data-stu-id="3d02a-117">After the installation is completed successfully, click **Finish** to close the wizard.</span></span>

    <span data-ttu-id="3d02a-118">Para verificar se a instalação do packager foi bem-sucedida, clique em **Iniciar**, em **todos os programas**, em **virtualização de área de trabalho do Microsoft Enterprise**e, em seguida, clique em **empacotador do espaço de trabalho do MED-V.**</span><span class="sxs-lookup"><span data-stu-id="3d02a-118">To verify that the installation of the packager was successful, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Workspace Packager.**</span></span>

    <span data-ttu-id="3d02a-119">Para obter informações sobre como usar o **pacote de espaço de trabalho do MED-v**, consulte [criar um pacote de espaço de trabalho do MED-v](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="3d02a-119">For information about how to use the **MED-V Workspace Packager**, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

<span data-ttu-id="3d02a-120">Se o packager não abrir como esperado, você pode tentar reparar a instalação.</span><span class="sxs-lookup"><span data-stu-id="3d02a-120">If the packager does not open as expected, you can try to repair the installation.</span></span>

**<span data-ttu-id="3d02a-121">Para reparar a instalação do pacote do espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="3d02a-121">To repair the MED-V Workspace Packager installation</span></span>**

1.  <span data-ttu-id="3d02a-122">Clique duas vezes no arquivo de instalação do MED-V \ _WorkspacePackager \ _Setup.</span><span class="sxs-lookup"><span data-stu-id="3d02a-122">Double-click the MED-V\_WorkspacePackager\_Setup installation file.</span></span>

    <span data-ttu-id="3d02a-123">O assistente de **configuração do pacote do espaço de trabalho do Microsoft Enterprise Desktop Virtualization (MED-V)** é aberto.</span><span class="sxs-lookup"><span data-stu-id="3d02a-123">The **Microsoft Enterprise Desktop Virtualization (MED-V) Workspace Packager Setup** wizard opens.</span></span> <span data-ttu-id="3d02a-124">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="3d02a-124">Click **Next** to continue.</span></span>

2.  <span data-ttu-id="3d02a-125">Para reparar os erros que podem ter ocorrido na instalação, clique em **reparar**.</span><span class="sxs-lookup"><span data-stu-id="3d02a-125">To repair errors that might have occurred in the installation, click **Repair**.</span></span>

3.  <span data-ttu-id="3d02a-126">Para começar o processo de reparo, clique em **reparar** novamente.</span><span class="sxs-lookup"><span data-stu-id="3d02a-126">To begin the repair process, click **Repair** again.</span></span>

4.  <span data-ttu-id="3d02a-127">Depois que o reparo for concluído com êxito, clique em **concluir** para fechar o assistente.</span><span class="sxs-lookup"><span data-stu-id="3d02a-127">After the repair is completed successfully, click **Finish** to close the wizard.</span></span>

    <span data-ttu-id="3d02a-128">Para verificar se o reparo do packager foi bem-sucedido, clique em **Iniciar**, em **todos os programas**, em **virtualização de área de trabalho do Microsoft Enterprise**e em **empacotador de espaço de trabalho do MED-V.**</span><span class="sxs-lookup"><span data-stu-id="3d02a-128">To verify that the repair of the packager was successful, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Workspace Packager.**</span></span>

## <span data-ttu-id="3d02a-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3d02a-129">Related topics</span></span>


[<span data-ttu-id="3d02a-130">Como instalar manualmente o agente de host da MED-V</span><span class="sxs-lookup"><span data-stu-id="3d02a-130">How to Manually Install the MED-V Host Agent</span></span>](how-to-manually-install-the-med-v-host-agent.md)

[<span data-ttu-id="3d02a-131">Como desinstalar os componentes da MED-V</span><span class="sxs-lookup"><span data-stu-id="3d02a-131">How to Uninstall the MED-V Components</span></span>](how-to-uninstall-the-med-v-components.md)

 

 





