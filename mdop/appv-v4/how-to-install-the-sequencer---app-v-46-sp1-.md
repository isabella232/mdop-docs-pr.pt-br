---
title: Como instalar o sequenciador (App-V 4,6 SP1)
description: Como instalar o sequenciador (App-V 4,6 SP1)
author: dansimp
ms.assetid: fe8eb876-28fb-46ae-b592-da055107e639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 611564e861d65dcd357c58732fb60dab21c05abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797092"
---
# <span data-ttu-id="4b8b6-103">Como instalar o sequenciador (App-V 4,6 SP1)</span><span class="sxs-lookup"><span data-stu-id="4b8b6-103">How to Install the Sequencer (App-V 4.6 SP1)</span></span>


<span data-ttu-id="4b8b6-104">O sequenciador do Microsoft Application Virtualization (App-V) monitora e registra o processo de instalação e configuração de aplicativos para que o aplicativo possa ser executado como um aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-104">The Microsoft Application Virtualization (App-V) Sequencer monitors and records the installation and setup process for applications so that the application can be run as a virtual application.</span></span> <span data-ttu-id="4b8b6-105">Você deve instalar o sequenciador do App-V em um computador que tenha somente o sistema operacional instalado.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-105">You should install the App-V Sequencer on a computer that has only the operating system installed.</span></span> <span data-ttu-id="4b8b6-106">Você também pode instalar o sequenciador em um computador executado em um ambiente virtual, por exemplo, um computador virtual.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-106">Alternatively, you can install the Sequencer on a computer running in a virtual environment, for example, a virtual computer.</span></span> <span data-ttu-id="4b8b6-107">Esse método é útil porque é mais fácil manter um ambiente de sequenciamento de limpeza que você pode reutilizar com uma configuração adicional mínima.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-107">This method is useful because it is easier to maintain a clean sequencing environment that you can reuse with minimal additional configuration.</span></span>

<span data-ttu-id="4b8b6-108">Você deve ter credenciais administrativas no computador que você está usando para sequenciar o aplicativo, e o computador não deve estar executando qualquer versão do cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-108">You must have administrative credentials on the computer you are using to sequence the application, and the computer must not be running any version of App-V client.</span></span> <span data-ttu-id="4b8b6-109">A criação de um aplicativo virtual usando o sequenciador App-V requer várias operações, portanto, é importante que você instale o sequenciador em um computador que atenda ou exceda os [requisitos de hardware e software do sequenciador do Application Virtualization](application-virtualization-sequencer-hardware-and-software-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4b8b6-109">Creating a virtual application by using the App-V Sequencer requires multiple operations, so it is important that you install the Sequencer on a computer that meets or exceeds the [Application Virtualization Sequencer Hardware and Software Requirements](application-virtualization-sequencer-hardware-and-software-requirements.md).</span></span>

**<span data-ttu-id="4b8b6-110">Observação</span><span class="sxs-lookup"><span data-stu-id="4b8b6-110">Note</span></span>**  
<span data-ttu-id="4b8b6-111">Não há suporte para a execução do sequenciador App-V no modo de segurança.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-111">Running the App-V sequencer in Safe Mode is not supported.</span></span>



**<span data-ttu-id="4b8b6-112">Para instalar o Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="4b8b6-112">To install the Microsoft Application Virtualization Sequencer</span></span>**

1.  <span data-ttu-id="4b8b6-113">Copie os arquivos de instalação do Microsoft Application Virtualization Sequencer para o computador no qual você deseja instalá-lo.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-113">Copy the Microsoft Application Virtualization Sequencer installation files to the computer on which you want to install it.</span></span>

2.  <span data-ttu-id="4b8b6-114">Para iniciar o assistente de instalação do Microsoft Application Virtualization Sequencer, clique duas vezes em **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-114">To start the Microsoft Application Virtualization Sequencer installation wizard, double-click **Setup.exe**.</span></span> <span data-ttu-id="4b8b6-115">Se o **pacote redistribuível do Microsoft Visual C++ SP1 (x86)** não for detectado antes da instalação, clique em **instalar** para instalar o pré-requisito obrigatório.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-115">If the **Microsoft Visual C++ SP1 Redistributable Package (x86)** is not detected prior to installation, click **Install** to install the required prerequisite.</span></span>

3.  <span data-ttu-id="4b8b6-116">Para continuar a instalação, na página **Bem-vindo** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-116">To continue the installation, on the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="4b8b6-117">Na página **contrato de licença** , para aceitar os termos do contrato de licença, clique em **aceito os termos do contrato de licença**e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-117">On the **License Agreement** page, to accept the terms of the license agreement, click **I accept the terms in the license agreement**, and then click **Next**.</span></span>

5.  <span data-ttu-id="4b8b6-118">Na página **pasta de destino** , para aceitar a pasta de instalação padrão, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-118">On the **Destination Folder** page, to accept the default installation folder, click **Next**.</span></span> <span data-ttu-id="4b8b6-119">Para especificar uma pasta de destino diferente, clique em **alterar** e especifique a pasta de instalação que será usada para a instalação.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-119">To specify a different destination folder, click **Change** and specify the installation folder that will be used for the installation.</span></span> <span data-ttu-id="4b8b6-120">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-120">Click **Next**.</span></span>

6.  <span data-ttu-id="4b8b6-121">Na página **unidade virtual** , para configurar o **Q:\\** de unidade padrão do Application Virtualization (padrão) como a unidade em que todos os aplicativos sequenciados serão executados, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-121">On the **Virtual Drive** page, to configure the Application Virtualization default drive **Q:\\** (default) as the drive that all sequenced applications will run from, click **Next**.</span></span> <span data-ttu-id="4b8b6-122">Se você quiser especificar uma letra de unidade diferente, use a lista e selecione a letra de unidade que deseja usar, selecionando a letra de unidade apropriada e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-122">If you want to specify a different drive letter, use the list and select the drive letter that you want to use by selecting the appropriate drive letter, and then click **Next**.</span></span>

    **<span data-ttu-id="4b8b6-123">Importante</span><span class="sxs-lookup"><span data-stu-id="4b8b6-123">Important</span></span>**  
    <span data-ttu-id="4b8b6-124">A letra da unidade de virtualização do aplicativo especificada com esta etapa é a letra da unidade na qual os aplicativos virtuais serão executados nos computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-124">The Application Virtualization drive letter specified with this step is the drive letter that virtual applications will be run from on target computers.</span></span> <span data-ttu-id="4b8b6-125">A letra da unidade especificada deve estar disponível e não está sendo usada no momento nos computadores que executam o cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-125">The drive letter specified must be available, and not currently in use on the computers running the App-V client.</span></span> <span data-ttu-id="4b8b6-126">Se a unidade especificada já estiver em uso, o aplicativo virtual falhará no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-126">If the specified drive is already in use, the virtual application fails on the target computer.</span></span>



7.  <span data-ttu-id="4b8b6-127">Na página **pronto para instalar o programa** , clique em **instalar**para iniciar a instalação.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-127">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

8.  <span data-ttu-id="4b8b6-128">Na página **Assistente InstallShield concluído** , para fechar o assistente de instalação e abrir o sequenciador do App-V, clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-128">On the **InstallShield Wizard Completed** page, to close the installation wizard and open the App-V Sequencer, click **Finish**.</span></span> <span data-ttu-id="4b8b6-129">Para fechar o assistente de instalação sem abrir o sequenciador, desmarque **iniciar o programa**e, em seguida, clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-129">To close the installation wizard without opening the Sequencer, clear **Launch the program**, and then click **Finish**.</span></span>

    **<span data-ttu-id="4b8b6-130">Observação</span><span class="sxs-lookup"><span data-stu-id="4b8b6-130">Note</span></span>**  
    <span data-ttu-id="4b8b6-131">Se você instalou o sequenciador do App-V em um computador que executa um ambiente virtual, por exemplo, um computador virtual, agora você deve fazer um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-131">If you installed the App-V Sequencer on a computer running a virtual environment, for example a virtual machine, you must now take a snapshot.</span></span> <span data-ttu-id="4b8b6-132">Depois de sequenciar um aplicativo, você pode reverter para essa imagem, para que você possa sequenciar o próximo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-132">After you sequence an application, you can revert to this image, so you can sequence the next application.</span></span>



~~~
When you uninstall the Sequencer, the following registry keys are not removed from the computer that the Sequencer was installed on. Additionally, you must restart the computer after you have uninstalled the Sequencer so that all associated drivers can be stopped and the operation can be completed.

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey**
~~~

## <span data-ttu-id="4b8b6-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4b8b6-133">Related topics</span></span>


[<span data-ttu-id="4b8b6-134">Configuração do Application Virtualization Sequencer (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="4b8b6-134">Configuring the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](configuring-the-application-virtualization-sequencer--app-v-46-sp1-.md)









