---
title: Sobre o Application Virtualization Sequencer
description: Sobre o Application Virtualization Sequencer
author: dansimp
ms.assetid: bee193ca-58bd-40c9-b41a-310435633895
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 83709bcceabe3312fba34512b47d28a24b4dc52c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797637"
---
# <span data-ttu-id="3cbf5-103">Sobre o Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="3cbf5-103">About the Application Virtualization Sequencer</span></span>


<span data-ttu-id="3cbf5-104">O sequenciador do Microsoft Application Virtualization (App-V) monitora e registra todos os processos de instalação e configuração de um aplicativo e cria os seguintes arquivos: **ico**, **OSD**, **SFT**e **SPRJ**.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-104">The Microsoft Application Virtualization (App-V) Sequencer monitors and records all installation and setup processes for an application and creates the following files: **ICO**, **OSD**, **SFT**, and **SPRJ**.</span></span> <span data-ttu-id="3cbf5-105">Esses arquivos contêm todas as informações necessárias sobre um aplicativo para que o aplicativo possa ser executado em um ambiente virtual em computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-105">These files contain all the necessary information about an application so the application can run in a virtual environment on target computers.</span></span> <span data-ttu-id="3cbf5-106">Você pode usar o sequenciador do Microsoft Application Virtualization (App-V) para criar aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-106">You can use the Microsoft Application Virtualization (App-V) Sequencer to create virtual applications.</span></span> <span data-ttu-id="3cbf5-107">Depois de sequenciar um aplicativo, ele pode ser transmitido para computadores de destino ou os computadores de destino podem executar o aplicativo virtual baixando o conteúdo do pacote de aplicativo virtual e executando o aplicativo localmente.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-107">After you sequence an application, it can be streamed to target computers, or target computers can run the virtual application by downloading the contents of the virtual application package and running the application locally.</span></span>

<span data-ttu-id="3cbf5-108">**Importante**  Para executar um pacote de aplicativo virtual, o computador de destino deve estar executando a versão adequada do cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-108">**Important** To run a virtual application package the target computer must be running the appropriate version of the App-V client.</span></span>

 

<span data-ttu-id="3cbf5-109">Os pacotes de aplicativos virtuais são executados em computadores de destino sem interagir com o sistema operacional subjacente no computador de destino porque cada aplicativo é executado em um ambiente virtual e é isolado de outros aplicativos instalados ou em execução no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-109">Virtual application packages run on target computers without interacting with the underlying operating system on the target computer because each application runs in a virtual environment and is isolated from other applications that are installed or running on the target computer.</span></span> <span data-ttu-id="3cbf5-110">Esse isolamento pode reduzir conflitos de aplicativos e pode ajudar a diminuir a quantidade necessária de testes de pré-implantação de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-110">This isolation can reduce application conflicts and can help decrease the required amount of application pre-deployment testing.</span></span>

## <span data-ttu-id="3cbf5-111">Terminologia do sequenciador</span><span class="sxs-lookup"><span data-stu-id="3cbf5-111">Sequencer Terminology</span></span>


<a href="" id="application-virtualization-drive"></a><span data-ttu-id="3cbf5-112">Unidade de virtualização do aplicativo</span><span class="sxs-lookup"><span data-stu-id="3cbf5-112">Application Virtualization drive</span></span>  
<span data-ttu-id="3cbf5-113">A unidade virtualização de aplicativo é a unidade padrão (Q:\) no computador de destino a partir do qual os aplicativos sequenciados são executados.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-113">The application virtualization drive is the default drive (Q:\) on the target computer from which sequenced applications are run.</span></span>

<a href="" id="ico-file"></a><span data-ttu-id="3cbf5-114">Arquivo ICO</span><span class="sxs-lookup"><span data-stu-id="3cbf5-114">ICO file</span></span>  
<span data-ttu-id="3cbf5-115">O arquivo de ícone na área de trabalho do cliente que é usado para iniciar um aplicativo sequenciado.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-115">The icon file on the client desktop which is used to launch a sequenced application.</span></span>

<a href="" id="installation-directory"></a><span data-ttu-id="3cbf5-116">Diretório de instalação</span><span class="sxs-lookup"><span data-stu-id="3cbf5-116">Installation directory</span></span>  
<span data-ttu-id="3cbf5-117">O diretório usado pelo sequenciador para colocar os arquivos de instalação durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-117">The directory used by the sequencer to place installation files during setup.</span></span>

<a href="" id="open-software-descriptor--osd--file"></a><span data-ttu-id="3cbf5-118">Abrir arquivo descritor de software (OSD)</span><span class="sxs-lookup"><span data-stu-id="3cbf5-118">Open Software Descriptor (OSD) file</span></span>  
<span data-ttu-id="3cbf5-119">Um arquivo baseado em XML que instrui o cliente App-V a recuperar o aplicativo sequenciado do servidor de streaming App-V e como executar o aplicativo sequenciado no ambiente virtual.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-119">An XML-based file that instructs the App-V client how to retrieve the sequenced application from the App-V streaming server and how to run the sequenced application in the virtual environment.</span></span>

<a href="" id="package-root-directory"></a><span data-ttu-id="3cbf5-120">Diretório raiz do pacote</span><span class="sxs-lookup"><span data-stu-id="3cbf5-120">Package root directory</span></span>  
<span data-ttu-id="3cbf5-121">O diretório no computador de sequenciamento em que os arquivos do pacote do aplicativo sequenciado são instalados.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-121">The directory on the sequencing computer on which files for the sequenced application package are installed.</span></span> <span data-ttu-id="3cbf5-122">Esse diretório também existe virtualmente no computador para o qual um aplicativo sequenciado será transmitido.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-122">This directory also exists virtually on the computer to which a sequenced application will be streamed.</span></span>

<a href="" id="sequenced-application"></a><span data-ttu-id="3cbf5-123">Aplicativo sequenciado</span><span class="sxs-lookup"><span data-stu-id="3cbf5-123">Sequenced application</span></span>  
<span data-ttu-id="3cbf5-124">Um aplicativo que foi monitorado pelo sequenciador, dividido em blocos de recursos primário e secundário, transmitido para um computador de destino que executa o cliente App-V t e executa um ambiente virtual.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-124">An application that has been monitored by the sequencer, broken up into primary and secondary feature blocks, streamed to a target computer running the App-V client t, and runs a virtual environment.</span></span>

<a href="" id="sequenced-application-package"></a><span data-ttu-id="3cbf5-125">Pacote de aplicativo sequenciado</span><span class="sxs-lookup"><span data-stu-id="3cbf5-125">Sequenced application package</span></span>  
<span data-ttu-id="3cbf5-126">Os arquivos que compõem um aplicativo virtual e permitem que um aplicativo virtual seja executado.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-126">The files that comprise a virtual application and allow a virtual application to run.</span></span> <span data-ttu-id="3cbf5-127">Esses arquivos são criados após o sequenciamento e incluirão os arquivos. **OSD**, **. sft**, **. sprj**e **. ico** de maneira específica.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-127">These files are created after sequencing and specifically include **.osd**, **.sft**, **.sprj**, and **.ico** files.</span></span>

<a href="" id="sequencing"></a><span data-ttu-id="3cbf5-128">Sequenciamento</span><span class="sxs-lookup"><span data-stu-id="3cbf5-128">Sequencing</span></span>  
<span data-ttu-id="3cbf5-129">O processo de criação de um pacote de aplicativo usando o sequenciador App-V.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-129">The process of creating an application package using the App-V Sequencer.</span></span> <span data-ttu-id="3cbf5-130">Nesse processo, um aplicativo é monitorado, seus atalhos são configurados e um pacote de aplicativo sequenciado é criado.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-130">In this process, an application is monitored, its shortcuts are configured, and a sequenced application package is created.</span></span>

<a href="" id="sequencing-computer"></a><span data-ttu-id="3cbf5-131">Sequenciando computador</span><span class="sxs-lookup"><span data-stu-id="3cbf5-131">Sequencing computer</span></span>  
<span data-ttu-id="3cbf5-132">O computador usado para sequenciar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-132">The computer used to sequence an application.</span></span>

<a href="" id="virtual-application"></a><span data-ttu-id="3cbf5-133">Aplicativo virtual</span><span class="sxs-lookup"><span data-stu-id="3cbf5-133">Virtual application</span></span>  
<span data-ttu-id="3cbf5-134">Um aplicativo empacotado pelo sequenciador para ser executado em um ambiente virtual autônomo.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-134">An application packaged by the Sequencer to run in a self-contained, virtual environment.</span></span> <span data-ttu-id="3cbf5-135">O ambiente virtual contém as informações necessárias para executar o aplicativo no cliente sem instalar o aplicativo localmente.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-135">The virtual environment contains the information necessary to run the application on the client without installing the application locally.</span></span>

<a href="" id="primary-feature-block"></a><span data-ttu-id="3cbf5-136">Bloco de recursos primário</span><span class="sxs-lookup"><span data-stu-id="3cbf5-136">Primary feature block</span></span>  
<span data-ttu-id="3cbf5-137">O conteúdo mínimo em um pacote de aplicativo virtual que é necessário para que um aplicativo seja executado em um computador de destino.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-137">The minimum content in a virtual application package that is necessary for an application to run on a target computer.</span></span> <span data-ttu-id="3cbf5-138">O conteúdo no bloco de recursos principal é identificado durante a fase de aplicação do sequenciamento e normalmente consiste no conteúdo dos recursos de aplicativo mais usados.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-138">The content in the primary feature block is identified during the application phase of sequencing and typically consists of the content for the most used application features.</span></span>

## <a href="" id="sequencing-applications-"></a><span data-ttu-id="3cbf5-139">Sequenciando aplicativos</span><span class="sxs-lookup"><span data-stu-id="3cbf5-139">Sequencing Applications</span></span>


<span data-ttu-id="3cbf5-140">Há dois métodos para criar e modificar pacotes de aplicativos virtuais em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-140">There are two methods to create and modify virtual application packages in your environment.</span></span> <span data-ttu-id="3cbf5-141">O primeiro método é usar o assistente de **sequenciamento** .</span><span class="sxs-lookup"><span data-stu-id="3cbf5-141">The first method is by using the **Sequencing** wizard.</span></span> <span data-ttu-id="3cbf5-142">O assistente de **sequenciamento** permite que você crie novos ou modifique pacotes de aplicativos virtuais existentes.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-142">The **Sequencing** wizard allows you to create new, or modify existing virtual application packages.</span></span> <span data-ttu-id="3cbf5-143">Para obter mais informações sobre como usar o assistente de **sequenciamento** , consulte [como sequenciar um novo aplicativo](how-to-sequence-a-new-application.md).</span><span class="sxs-lookup"><span data-stu-id="3cbf5-143">For more information about using the **Sequencing** wizard see, [How to Sequence a New Application](how-to-sequence-a-new-application.md).</span></span> <span data-ttu-id="3cbf5-144">O segundo método é usando a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-144">The second method is by using the command-line.</span></span> <span data-ttu-id="3cbf5-145">A linha de comando permite que você crie novos ou modifique pacotes de aplicativos virtuais existentes usando o prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-145">The command-line allows you to create new, or modify existing virtual application packages using the command prompt.</span></span> <span data-ttu-id="3cbf5-146">Para obter mais informações sobre como usar a linha de comando, consulte [como gerenciar aplicativos virtuais usando a linha de comando](how-to-manage-virtual-applications-using-the-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="3cbf5-146">For more information about using the command line see, [How to Manage Virtual Applications Using the Command Line](how-to-manage-virtual-applications-using-the-command-line.md).</span></span>

<span data-ttu-id="3cbf5-147">O assistente de **sequenciamento** fornece as seguintes funções para a criação de pacotes de aplicativos virtuais:</span><span class="sxs-lookup"><span data-stu-id="3cbf5-147">The **Sequencing** wizard provides the following functions for creating virtual application packages:</span></span>

1.  <span data-ttu-id="3cbf5-148">**Configuração do pacote**: o assistente de **sequenciamento** solicita informações de configuração do pacote necessárias para concluir o arquivo do descritor de software aberto (OSD), que é um arquivo obrigatório para iniciar um pacote de aplicativo sequenciado.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-148">**Package Configuration**: The **Sequencing** Wizard prompts for package configuration information necessary to complete the Open Software Descriptor (OSD) file, which is a required file for starting a sequenced application package.</span></span>

2.  <span data-ttu-id="3cbf5-149">**Instalação do aplicativo**: o assistente de **sequenciamento** coleta informações sobre as configurações de instalação e inicialização de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-149">**Application Installation**: The **Sequencing** Wizard gathers information about an application’s installation and startup configurations.</span></span> <span data-ttu-id="3cbf5-150">Ele monitora e registra as informações de instalação e inicialização associadas ao aplicativo para criar os arquivos necessários para um pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-150">It monitors and records the installation and startup information associated with the application to create the files necessary for a virtual application package.</span></span>

3.  <span data-ttu-id="3cbf5-151">**Inicialização do aplicativo**: o assistente de **sequenciamento** coleta informações para compilar e ordenar os blocos de código necessários para executar a inicialização inicial do pacote do aplicativo sequenciado no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-151">**Application Startup**: The **Sequencing** Wizard gathers information for compiling and ordering the blocks of code necessary to perform the initial startup of the sequenced application package on the target computer.</span></span> <span data-ttu-id="3cbf5-152">A compilação do bloco de código é referida como o bloco de recursos principal.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-152">The compilation of the code block is referred to as the primary feature block.</span></span>

## <span data-ttu-id="3cbf5-153">Considerações de segurança do sequenciador do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="3cbf5-153">Application Virtualization Sequencer Security Considerations</span></span>


<span data-ttu-id="3cbf5-154">O sequenciador App-V executa todos os serviços detectados no tempo de sequenciamento usando a conta do sistema local e não aplica os descritores de segurança nas solicitações de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-154">The App-V Sequencer runs all services detected at sequencing time using the Local System account and does not enforce security descriptors on service control requests.</span></span> <span data-ttu-id="3cbf5-155">Se o serviço foi instalado usando uma conta de usuário diferente ou se os descritores de segurança destinam-se a conceder permissões de serviço específicas a grupos de usuários diferentes, considere cuidadosamente se o serviço deve ser virtualizado.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-155">If the service was installed using a different user account or if the security descriptors are intended to grant different user groups specific service permissions, consider carefully whether the service should be virtualized.</span></span> <span data-ttu-id="3cbf5-156">Em alguns casos, você deve instalar o serviço localmente para garantir que a segurança do serviço pretendida seja preservada.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-156">In some cases, you should install the service locally to ensure that the intended service security is preserved.</span></span>

<span data-ttu-id="3cbf5-157">**Importante**  Você deve sempre salvar pacotes de aplicativos virtuais em um local seguro.</span><span class="sxs-lookup"><span data-stu-id="3cbf5-157">**Important** You should always save virtual application packages in a secure location.</span></span>

 

## <span data-ttu-id="3cbf5-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3cbf5-158">Related topics</span></span>


[<span data-ttu-id="3cbf5-159">Visão geral do Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="3cbf5-159">Application Virtualization Sequencer Overview</span></span>](application-virtualization-sequencer-overview.md)

 

 





