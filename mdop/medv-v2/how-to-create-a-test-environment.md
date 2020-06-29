---
title: Como criar um ambiente de teste
description: Como criar um ambiente de teste
author: dansimp
ms.assetid: a0db2299-16f3-4516-8769-7d55ca4a1e98
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ee2ab131f6003b56cce7a60ffea1cd00b067fae3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800042"
---
# <span data-ttu-id="9fb0e-103">Como criar um ambiente de teste</span><span class="sxs-lookup"><span data-stu-id="9fb0e-103">How to Create a Test Environment</span></span>


<span data-ttu-id="9fb0e-104">Veja a seguir algumas etapas e instruções para ajudá-lo a criar um ambiente de teste que você pode usar para testar o pacote do espaço de trabalho do MED-V localmente antes de implantá-lo em toda a empresa.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-104">The following are some steps and instructions to help you create a test environment that you can use to test your MED-V workspace package locally before deploying it throughout your enterprise.</span></span> <span data-ttu-id="9fb0e-105">Esta seção fornece orientação sobre como criar um ambiente de teste, seja manualmente ou usando um sistema de distribuição de software eletrônico.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-105">This section provides guidance about how to create a test environment, either manually or by using an electronic software distribution system.</span></span>

**<span data-ttu-id="9fb0e-106">Para criar um ambiente de teste usando um ESD</span><span class="sxs-lookup"><span data-stu-id="9fb0e-106">To create a test environment by using an ESD</span></span>**

1.  <span data-ttu-id="9fb0e-107">Use o método de implantação de software na empresa em toda a empresa para implantar os seguintes componentes necessários em um computador de teste.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-107">Use your company’s method of deploying software throughout the enterprise to deploy the following necessary components to a test computer.</span></span> <span data-ttu-id="9fb0e-108">Instale-os na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="9fb0e-108">Install them in the following order:</span></span>

    -   <span data-ttu-id="9fb0e-109">**PC virtual do Windows** – se ainda não estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-109">**Windows Virtual PC** – if not already installed.</span></span> <span data-ttu-id="9fb0e-110">Para obter mais informações, consulte [configurar pré-requisitos de instalação](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="9fb0e-110">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="9fb0e-111">**Inclusões e atualizações do Windows Virtual PC**– se ainda não estiverem instaladas.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-111">**Windows Virtual PC Additions and Updates**– if not already installed.</span></span> <span data-ttu-id="9fb0e-112">Para obter mais informações, consulte [configurar pré-requisitos de instalação](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="9fb0e-112">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="9fb0e-113">**Arquivo de instalação do MED-v Host Agent** – instala o arquivo de instalação do Host Agent (MED-v \ _HostAgent \ _setup instalação).</span><span class="sxs-lookup"><span data-stu-id="9fb0e-113">**MED-V Host Agent Installation File** – installs the Host Agent (MED-V\_HostAgent\_Setup installation file).</span></span> <span data-ttu-id="9fb0e-114">Para obter mais informações, consulte [como instalar manualmente o agente de host do MED-V](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="9fb0e-114">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

    -   <span data-ttu-id="9fb0e-115">**Instalador do espaço de trabalho do MED-v, VHD e executável de configuração** – criado no **pacote do espaço de trabalho do MED-v**.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-115">**MED-V Workspace Installer, VHD, and Setup Executable** – created in the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="9fb0e-116">Para obter mais informações, consulte [criar um pacote de espaço de trabalho do MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="9fb0e-116">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

        <span data-ttu-id="9fb0e-117">**Importante**  O programa executável de configuração e VHD deve estar na mesma pasta que o instalador do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-117">**Important** The VHD and Setup executable program must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="9fb0e-118">Em seguida, instale o instalador do espaço de trabalho do MED-V executando setup.exe.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-118">Then, install the MED-V workspace installer by running setup.exe.</span></span>

         

2.  <span data-ttu-id="9fb0e-119">Depois que todos os componentes estiverem instalados no computador de teste, execute o MED-V Host Agent para iniciar a configuração da primeira vez.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-119">After all of the components are installed on the test computer, run the MED-V Host Agent to start first time setup.</span></span>

    <span data-ttu-id="9fb0e-120">Clique em **Iniciar**, em **todos os programas**, em **virtualização de área de trabalho do Microsoft Enterprise**e clique em **agente de host do MED-V**.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-120">Click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

    <span data-ttu-id="9fb0e-121">**Observação**  Se você não puder executar fisicamente o agente de host do MED-V no computador de teste, a configuração iniciará automaticamente na próxima vez em que o computador for reiniciado.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-121">**Note** If you cannot physically run the MED-V Host Agent on the test computer, first time setup starts automatically the next time that the computer restarts.</span></span>

     

<span data-ttu-id="9fb0e-122">Primeira vez que o programa de instalação é iniciado, pode levar dez minutos ou mais para concluir.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-122">First time setup starts and can take ten minutes or more to finish.</span></span>

<span data-ttu-id="9fb0e-123">Para obter informações sobre como testar suas configurações na primeira vez em que a configuração estiver em execução, consulte [como verificar as configurações de configuração da primeira vez](how-to-verify-first-time-setup-settings.md).</span><span class="sxs-lookup"><span data-stu-id="9fb0e-123">For information about testing your configuration settings when first time setup is running, see [How to Verify First Time Setup Settings](how-to-verify-first-time-setup-settings.md).</span></span>

**<span data-ttu-id="9fb0e-124">Para criar um ambiente de teste manualmente</span><span class="sxs-lookup"><span data-stu-id="9fb0e-124">To create a test environment manually</span></span>**

1.  <span data-ttu-id="9fb0e-125">Instale o agente de host do MED-V em um ambiente de teste local que inclua pré-requisitos do MED-V, como o Windows Virtual PC com adições e atualizações.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-125">Install the MED-V Host Agent in a local test environment that includes MED-V prerequisites, such as Windows Virtual PC with additions and updates.</span></span> <span data-ttu-id="9fb0e-126">Para obter informações, consulte [como instalar manualmente o agente de host do MED-V](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="9fb0e-126">For information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

2.  <span data-ttu-id="9fb0e-127">Copie os arquivos do espaço de trabalho do MED-V para o seu ambiente de teste.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-127">Copy the MED-V workspace files to your test environment.</span></span> <span data-ttu-id="9fb0e-128">Os arquivos do espaço de trabalho do MED-V estão localizados na pasta de destino que você especificou no **pacote do espaço de trabalho do MED-v**.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-128">The MED-V workspace files are located in the destination folder that you specified in the **MED-V Workspace Packager**.</span></span>

    <span data-ttu-id="9fb0e-129">**Importante**  O programa executável de configuração e VHD deve estar na mesma pasta em seu ambiente de teste como o instalador do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-129">**Important** The VHD and Setup executable program must be in the same folder on your test environment as the MED-V workspace installer.</span></span>

     

3.  <span data-ttu-id="9fb0e-130">Instale o espaço de trabalho do MED-V executando setup.exe.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-130">Install the MED-V workspace by running setup.exe.</span></span>

4.  <span data-ttu-id="9fb0e-131">Iniciar a configuração da primeira vez executando o agente de host MED-V.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-131">Start first time setup by running the MED-V Host Agent.</span></span>

    <span data-ttu-id="9fb0e-132">Clique em **Iniciar**, em **todos os programas**, em **virtualização de área de trabalho do Microsoft Enterprise**e clique em **agente de host do MED-V**.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-132">Click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

<span data-ttu-id="9fb0e-133">Início da primeira vez em que a configuração é iniciada e pode demorar vários minutos para ser concluída, dependendo do tamanho do VHD especificado.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-133">First time setup starts and might take several minutes to complete, depending on the size of the VHD specified.</span></span>

<span data-ttu-id="9fb0e-134">Agora você está pronto para testar as diferentes configurações de configuração, publicação de aplicativos e redirecionamento de URL que você especificou para seu espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-134">You are now ready to test the different settings for configuration, application publishing, and URL redirection that you specified for your MED-V workspace.</span></span>

<span data-ttu-id="9fb0e-135">**Observação**  Por padrão, o MED-V substitui a política de bloqueio de tela no convidado.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-135">**Note** By default, MED-V overrides the screen lock policy in the guest.</span></span> <span data-ttu-id="9fb0e-136">No entanto, isso não representa um problema de segurança porque o computador host ainda honra a política de bloqueio de tela.</span><span class="sxs-lookup"><span data-stu-id="9fb0e-136">However, this does not pose a security problem because the host computer still honors the screen lock policy.</span></span>

 

## <span data-ttu-id="9fb0e-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9fb0e-137">Related topics</span></span>


[<span data-ttu-id="9fb0e-138">Como verificar as configurações da primeira instalação</span><span class="sxs-lookup"><span data-stu-id="9fb0e-138">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

[<span data-ttu-id="9fb0e-139">Como testar a publicação de aplicativos</span><span class="sxs-lookup"><span data-stu-id="9fb0e-139">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="9fb0e-140">Como testar o redirecionamento da URL</span><span class="sxs-lookup"><span data-stu-id="9fb0e-140">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

 

 





