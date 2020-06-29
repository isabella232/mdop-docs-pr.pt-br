---
title: Práticas recomendadas para o Application Virtualization Sequencer
description: Práticas recomendadas para o Application Virtualization Sequencer
author: dansimp
ms.assetid: 95e5e216-864f-41a1-90d4-b8d7e1eb42a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859514fb34185a339c7f2c2734f331e5a99d050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798984"
---
# <span data-ttu-id="34263-103">Práticas recomendadas para o Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="34263-103">Best Practices for the Application Virtualization Sequencer</span></span>


<span data-ttu-id="34263-104">Este tópico fornece as práticas recomendadas para executar o sequenciador do Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="34263-104">This topic provides best practices for running the Microsoft Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="34263-105">Revise e considere as seguintes recomendações ao planejar e usar o sequenciador no seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="34263-105">Review and consider the following recommendations when planning and using the Sequencer in your environment.</span></span>

## <span data-ttu-id="34263-106">Sequenciando as práticas recomendadas de configuração do computador</span><span class="sxs-lookup"><span data-stu-id="34263-106">Sequencing Computer Configuration Best Practices</span></span>


<span data-ttu-id="34263-107">As seguintes práticas recomendadas devem ser consideradas ao configurar o computador que executa o sequenciador App-V:</span><span class="sxs-lookup"><span data-stu-id="34263-107">The following best practices should be considered when configuring the computer running the App-V Sequencer:</span></span>

-   **<span data-ttu-id="34263-108">Sequência em um computador que tem uma configuração semelhante e que está executando uma versão anterior do sistema operacional do que os computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="34263-108">Sequence on a computer that has a similar configuration and that is running an earlier version of the operating system than the target computers.</span></span>**

    <span data-ttu-id="34263-109">Verifique se o computador que está executando o sequenciador está executando uma versão anterior do sistema operacional do que os computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="34263-109">Ensure that the computer that is running the Sequencer is running an earlier version of the operating system than the target computers.</span></span> <span data-ttu-id="34263-110">Isso inclui o Service Pack e as versões de atualização.</span><span class="sxs-lookup"><span data-stu-id="34263-110">This includes the service pack and update versions.</span></span> <span data-ttu-id="34263-111">Por exemplo, se os computadores de destino estiverem executando o WindowsVista e o WindowsXP, você deve sequenciar aplicativos em um computador que esteja executando o WindowsXP.</span><span class="sxs-lookup"><span data-stu-id="34263-111">For example, if the target computers are running WindowsVista and WindowsXP, you should sequence applications on a computer that is running WindowsXP.</span></span> <span data-ttu-id="34263-112">A capacidade de sequenciar em um sistema operacional e executar o aplicativo virtualizado em um sistema operacional diferente não é garantida e depende do aplicativo específico e do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="34263-112">The ability to sequence on one operating system and run the virtualized application on a different operating system is not guaranteed, and depends on the particular application and operating system.</span></span> <span data-ttu-id="34263-113">Se você encontrar problemas, talvez seja necessário sequenciar o mesmo ambiente do sistema operacional que o do aplicativo do aplicativo do App-V está em execução.</span><span class="sxs-lookup"><span data-stu-id="34263-113">If you encounter issues, you may be required to sequence on the same operating system environment as the one on which the App-V client is running.</span></span>

-   **<span data-ttu-id="34263-114">Configurar o computador que executa o sequenciador com várias partições.</span><span class="sxs-lookup"><span data-stu-id="34263-114">Configure the computer running the Sequencer with multiple partitions.</span></span>**

    <span data-ttu-id="34263-115">Você deve configurar o computador que executa o sequenciador com pelo menos duas partições primárias.</span><span class="sxs-lookup"><span data-stu-id="34263-115">You should configure the computer running the Sequencer with at least two primary partitions.</span></span> <span data-ttu-id="34263-116">A primeira partição (**C:**) deve conter o sistema operacional e deve ser formatada usando o sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="34263-116">The first partition (**C:**) should contain the operating system, and it should be formatted using the NTFS file system.</span></span> <span data-ttu-id="34263-117">A segunda partição (**Q:**) é usada como o caminho de destino para a instalação do aplicativo virtual e também deve ser formatada usando o sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="34263-117">The second partition (**Q:**) is used as the destination path for the virtual application installation and should also be formatted using the NTFS file system.</span></span>

-   **<span data-ttu-id="34263-118">Configure o diretório Temp com espaço livre suficiente em disco.</span><span class="sxs-lookup"><span data-stu-id="34263-118">Configure the temp directory with enough free disk space.</span></span>**

    <span data-ttu-id="34263-119">O sequenciador usa o diretório **% tmp%** ou **% Temp%** e o diretório de **rascunho** para armazenar arquivos temporários durante o sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="34263-119">The Sequencer uses the **%TMP%** or **%TEMP%** directory and the **Scratch** directory to store temporary files during sequencing.</span></span> <span data-ttu-id="34263-120">Você deve configurar esses diretórios no computador que executa o sequenciador com espaço livre em disco equivalente aos requisitos estimados de instalação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="34263-120">You should configure these directories on the computer running the Sequencer with free disk space equivalent to the estimated application installation requirements.</span></span> <span data-ttu-id="34263-121">Você pode verificar o local do diretório de **rascunho** abrindo o console do sequenciador e selecionando **ferramentas**, **Opções**e, em seguida, selecionando a guia **caminhos** . a configuração de diretórios temporários e o diretório de **rascunho** em partições de disco rígido diferentes podem melhorar o desempenho durante o sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="34263-121">You can verify the location of the **Scratch** directory by opening the Sequencer console and selecting **Tools**, **Options**, and then selecting the **Paths** tab. Configuring the temp directories and the **Scratch** directory on different hard drive partitions can improve performance during sequencing.</span></span>

-   **<span data-ttu-id="34263-122">Sequenciar aplicativos usando o Microsoft VirtualPC.</span><span class="sxs-lookup"><span data-stu-id="34263-122">Sequence applications by using Microsoft VirtualPC.</span></span>**

    <span data-ttu-id="34263-123">Você vai sequenciar a maioria dos aplicativos mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="34263-123">You will sequence most applications more than once.</span></span> <span data-ttu-id="34263-124">Para ajudar a facilitar isso, você deve considerar o sequenciamento em um computador executado em um ambiente virtual.</span><span class="sxs-lookup"><span data-stu-id="34263-124">To help facilitate this, you should consider sequencing on a computer running in a virtual environment.</span></span> <span data-ttu-id="34263-125">Dessa forma, você poderá sequenciar um aplicativo e reverter a um estado limpo, com a reconfiguração mínima, no computador que está executando o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="34263-125">This will allow you to sequence an application and revert to a clean state, with minimal reconfiguration, on the computer that is running the Sequencer.</span></span>

    <span data-ttu-id="34263-126">Se você estiver executando o Microsoft Hyper-V em seu ambiente, o sequenciador do App-V será executado quando o computador virtual Hyper-V em que estiver sendo executado for:</span><span class="sxs-lookup"><span data-stu-id="34263-126">If you are running Microsoft Hyper-V in your environment the App-V sequencer will run when the Hyper-V virtual computer it is running on is:</span></span>

    -   <span data-ttu-id="34263-127">pausado e retomado.</span><span class="sxs-lookup"><span data-stu-id="34263-127">paused and resumed.</span></span>

    -   <span data-ttu-id="34263-128">tem seu estado salvo e restaurado.</span><span class="sxs-lookup"><span data-stu-id="34263-128">has its state saved and restored.</span></span>

    -   <span data-ttu-id="34263-129">salvo como instantâneo e é restaurado.</span><span class="sxs-lookup"><span data-stu-id="34263-129">saved as a snapshot and is restored.</span></span>

    -   <span data-ttu-id="34263-130">migrado para hardware diferente como parte de uma migração ao vivo.</span><span class="sxs-lookup"><span data-stu-id="34263-130">migrated to different hardware as part of a live migration.</span></span>

-   **<span data-ttu-id="34263-131">Antes de sequenciar um novo aplicativo, desligue outros programas em execução.</span><span class="sxs-lookup"><span data-stu-id="34263-131">Before you sequence a new application, shut down other running programs.</span></span>**

    <span data-ttu-id="34263-132">Os processos e as tarefas agendadas que normalmente são executados no computador de sequenciamento podem retardar o processo de sequenciamento e fazer com que dados irrelevantes sejam coletados durante o sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="34263-132">Processes and scheduled tasks that normally run on the sequencing computer can slow down the sequencing process and cause irrelevant data to be gathered during sequencing.</span></span> <span data-ttu-id="34263-133">Todos os aplicativos e programas desnecessários devem ser desligados antes de você começar a sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="34263-133">All unnecessary applications and programs should be shut down before you begin sequencing.</span></span>

-   **<span data-ttu-id="34263-134">Sequência em um computador que esteja executando serviços de terminal</span><span class="sxs-lookup"><span data-stu-id="34263-134">Sequence on a computer that is running Terminal Services</span></span>**

    <span data-ttu-id="34263-135">Você não deve configurar o modo de instalação em um computador que esteja executando serviços de terminal antes de instalar o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="34263-135">You should not configure the install mode on a computer that is running Terminal Services before you install the sequencer.</span></span>

## <span data-ttu-id="34263-136">Práticas recomendadas de sequenciamento</span><span class="sxs-lookup"><span data-stu-id="34263-136">Sequencing Best Practices</span></span>


<span data-ttu-id="34263-137">As seguintes práticas recomendadas devem ser consideradas ao sequenciar um novo aplicativo:</span><span class="sxs-lookup"><span data-stu-id="34263-137">The following best practices should be considered when sequencing a new application:</span></span>

-   

    <span data-ttu-id="34263-138">**Observação**  Se estiver executando o App-V 4,6 SP1, você não precisará sequenciar para um diretório que siga a Convenção de nomenclatura do 8,3.</span><span class="sxs-lookup"><span data-stu-id="34263-138">**Note** If you are running App-V 4.6 SP1 you do not need to sequence to a directory that follows the 8.3 naming convention.</span></span>

     

-   **<span data-ttu-id="34263-139">Sequência para um diretório exclusivo que acompanha a Convenção de nomenclatura do 8,3.</span><span class="sxs-lookup"><span data-stu-id="34263-139">Sequence to a unique directory that follows the 8.3 naming convention.</span></span>**

    <span data-ttu-id="34263-140">Você deve sequenciar todos os aplicativos para um diretório que siga a Convenção de nomenclatura do 8,3.</span><span class="sxs-lookup"><span data-stu-id="34263-140">You should sequence all applications to a directory that follows the 8.3 naming convention.</span></span> <span data-ttu-id="34263-141">O nome do diretório especificado não pode conter mais de oito caracteres, seguidos por uma extensão de nome de arquivo de três caracteres — por exemplo, **Q:\\MYAPP. ABC**.</span><span class="sxs-lookup"><span data-stu-id="34263-141">The specified directory name cannot contain more than eight characters, followed by a three-character file name extension—for example, **Q:\\MYAPP.ABC**.</span></span>

-   **<span data-ttu-id="34263-142">Sequência para uma pasta de destino na raiz da unidade, não a um subdiretório.</span><span class="sxs-lookup"><span data-stu-id="34263-142">Sequence to a destination folder on the root of the drive, not to a subdirectory.</span></span>**

    <span data-ttu-id="34263-143">Se o pacote de aplicativos tiver várias partes, instale cada aplicativo em um subdiretório do diretório principal.</span><span class="sxs-lookup"><span data-stu-id="34263-143">If the application suite has multiple parts, install each application to a subdirectory of the main directory.</span></span> <span data-ttu-id="34263-144">Por exemplo, se um pacote contiver um aplicativo juntamente com um cliente, use **Q:\\AppSuite** como o diretório principal e sequenciando o aplicativo principal para **Q:\\AppSuite\\Main**e sequenciando o cliente para o **Q:\\AppSuite\\Client**.</span><span class="sxs-lookup"><span data-stu-id="34263-144">For example, if a package contains an application along with a client, use **Q:\\AppSuite** as the main directory and sequence the main application to **Q:\\AppSuite\\Main**, and sequence the client to **Q:\\AppSuite\\Client**.</span></span>

-   **<span data-ttu-id="34263-145">Configure e teste o aplicativo durante a fase de instalação.</span><span class="sxs-lookup"><span data-stu-id="34263-145">Configure and test the application during the installation phase.</span></span>**

    <span data-ttu-id="34263-146">Concluir a instalação de um aplicativo geralmente requer a execução de várias etapas manuais que não fazem parte do processo de instalação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="34263-146">Completing the installation of an application often requires performing several manual steps that are not part of the application installation process.</span></span> <span data-ttu-id="34263-147">Essas etapas podem envolver a configuração de uma conexão com um banco de dados ou a cópia de arquivos atualizados.</span><span class="sxs-lookup"><span data-stu-id="34263-147">These steps can involve configuring a connection to a database or copying updated files.</span></span> <span data-ttu-id="34263-148">Você deve executar essas configurações durante a fase de instalação e, em seguida, executar o aplicativo para garantir que ele funcione.</span><span class="sxs-lookup"><span data-stu-id="34263-148">You should perform these configurations during the installation phase and then run the application to make sure it works.</span></span>

-   **<span data-ttu-id="34263-149">Execute o aplicativo, várias vezes, se necessário, até que o programa seja estável.</span><span class="sxs-lookup"><span data-stu-id="34263-149">Run the application, multiple times if necessary, until the program is stable.</span></span>**

    <span data-ttu-id="34263-150">Você deve executar o aplicativo várias vezes durante a instalação para garantir que todas as configurações de registro e de caixa de diálogo associadas sejam concluídas.</span><span class="sxs-lookup"><span data-stu-id="34263-150">You should run the application multiple times during the installation to ensure all associated registration and dialog box configurations have been completed.</span></span> <span data-ttu-id="34263-151">Abrir o aplicativo várias vezes durante a instalação garantirá que somente os recursos relevantes do aplicativo sejam carregados no **bloco de recursos principal**.</span><span class="sxs-lookup"><span data-stu-id="34263-151">Opening the application multiple times during installation will ensure that only the relevant application features are loaded into the **primary feature block**.</span></span>

-   **<span data-ttu-id="34263-152">Desabilitar todos os recursos de atualização automática associados ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="34263-152">Disable all automatic update features associated with the application.</span></span>**

    <span data-ttu-id="34263-153">Alguns aplicativos têm a capacidade de verificar as atualizações mais recentes automaticamente durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="34263-153">Some applications have the ability to check for the latest updates automatically during installation.</span></span> <span data-ttu-id="34263-154">Para auxiliar no controle de versão dos pacotes de aplicativos virtuais, você deve desabilitar esse recurso durante o sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="34263-154">To assist with versioning of virtual application packages, you should disable this feature during sequencing.</span></span> <span data-ttu-id="34263-155">Se houver atualizações necessárias, você deve sequenciar um novo pacote de aplicativo virtual com as atualizações associadas instaladas.</span><span class="sxs-lookup"><span data-stu-id="34263-155">If there are required updates, you should sequence a new virtual application package with the associated updates installed.</span></span>

## <span data-ttu-id="34263-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="34263-156">Related topics</span></span>


[<span data-ttu-id="34263-157">Planejamento da implantação do Application Virtualization System</span><span class="sxs-lookup"><span data-stu-id="34263-157">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





