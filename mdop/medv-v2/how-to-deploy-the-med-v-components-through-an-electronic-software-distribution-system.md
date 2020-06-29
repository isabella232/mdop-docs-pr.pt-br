---
title: Como implantar os componentes da MED-V por meio de um sistema de distribuição eletrônica de software
description: Como implantar os componentes da MED-V por meio de um sistema de distribuição eletrônica de software
author: dansimp
ms.assetid: 8a800bdf-6fa4-47b4-b417-df053289d4e8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d772702c770340796fe770273146bd0308617a69
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799555"
---
# <span data-ttu-id="ca274-103">Como implantar os componentes da MED-V por meio de um sistema de distribuição eletrônica de software</span><span class="sxs-lookup"><span data-stu-id="ca274-103">How to Deploy the MED-V Components Through an Electronic Software Distribution System</span></span>


<span data-ttu-id="ca274-104">Um sistema de distribuição de software eletrônico pode ajudá-lo a migrar com eficiência software para muitos computadores por meio de conexões de rede rápidas ou lentas.</span><span class="sxs-lookup"><span data-stu-id="ca274-104">An electronic software distribution system can help you efficiently move software to many computers over slow or fast network connections.</span></span> <span data-ttu-id="ca274-105">A seção a seguir fornece informações e instruções para ajudá-lo a implantar os componentes do MED-V (virtualização de área de trabalho do Microsoft Enterprise) 2,0 em toda a sua empresa usando um sistema de distribuição de software.</span><span class="sxs-lookup"><span data-stu-id="ca274-105">The following section provides information and instructions to help you deploy the Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 components throughout your enterprise by using a software distribution system.</span></span>

**<span data-ttu-id="ca274-106">Observação</span><span class="sxs-lookup"><span data-stu-id="ca274-106">Note</span></span>**  
<span data-ttu-id="ca274-107">Seja qual for a solução de distribuição de software que você usa, você deve estar familiarizado com os requisitos de sua solução específica.</span><span class="sxs-lookup"><span data-stu-id="ca274-107">Whichever software distribution solution that you use, you must be familiar with the requirements of your particular solution.</span></span> <span data-ttu-id="ca274-108">Se você estiver usando o System Center Configuration Manager 2007 R2 ou uma versão posterior, consulte a [biblioteca de documentação do Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=66999) na biblioteca técnica da Microsoft ( https://go.microsoft.com/fwlink/?LinkId=66999) .</span><span class="sxs-lookup"><span data-stu-id="ca274-108">If you are using System Center Configuration Manager 2007 R2 or a later version, see the [Configuration Manager Documentation Library](https://go.microsoft.com/fwlink/?LinkId=66999) in the Microsoft Technical Library (https://go.microsoft.com/fwlink/?LinkId=66999).</span></span>



**<span data-ttu-id="ca274-109">Importante</span><span class="sxs-lookup"><span data-stu-id="ca274-109">Important</span></span>**  
<span data-ttu-id="ca274-110">Se você estiver usando o System Center Configuration Manager 2007 SP2 e seus espaços de trabalho do MED-V estiverem configurados para operar no modo **NAT** , as máquinas virtuais serão classificadas como clientes baseados na Internet e não poderão encontrar os pontos de distribuição mais próximos a partir dos quais baixar conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ca274-110">If you are using System Center Configuration Manager 2007 SP2 and your MED-V workspaces are configured to operate in **NAT** mode, the virtual machines are classified as Internet-based clients and cannot find the closest distribution points from which to download content.</span></span>

<span data-ttu-id="ca274-111">O [hotfix para melhorar a funcionalidade para VMs gerenciadas pelo med-v](https://go.microsoft.com/fwlink/?LinkId=201088) ( https://go.microsoft.com/fwlink/?LinkId=201088) adiciona Nova funcionalidade a máquinas virtuais que são gerenciadas pelo med-v e que são configuradas para operar no modo **NAT** .</span><span class="sxs-lookup"><span data-stu-id="ca274-111">The [hotfix to improve the functionality for VMs that are managed by MED-V](https://go.microsoft.com/fwlink/?LinkId=201088) (https://go.microsoft.com/fwlink/?LinkId=201088) adds new functionality to virtual machines that are managed by MED-V and that are configured to operate in **NAT** mode.</span></span> <span data-ttu-id="ca274-112">A nova funcionalidade permite às máquinas virtuais acessar os pontos de distribuição mais próximos.</span><span class="sxs-lookup"><span data-stu-id="ca274-112">The new functionality lets virtual machines access the closest distribution points.</span></span> <span data-ttu-id="ca274-113">Portanto, o administrador pode gerenciar a máquina virtual e o computador host da mesma maneira.</span><span class="sxs-lookup"><span data-stu-id="ca274-113">Therefore, the administrator can manage the virtual machine and the host computer in the same manner.</span></span> <span data-ttu-id="ca274-114">Esse hotfix deve ser instalado primeiro no servidor do site e, em seguida, no cliente.</span><span class="sxs-lookup"><span data-stu-id="ca274-114">This hotfix must be installed first on the site server and then on the client.</span></span>

<span data-ttu-id="ca274-115">A atualização está disponível publicamente.</span><span class="sxs-lookup"><span data-stu-id="ca274-115">The update is publicly available.</span></span> <span data-ttu-id="ca274-116">No entanto, você pode ser solicitado a aceitar um contrato de serviços da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ca274-116">However, you might be prompted to accept an agreement for Microsoft Services.</span></span> <span data-ttu-id="ca274-117">Siga os prompts nas páginas da Web sucessivas para recuperar este hotfix.</span><span class="sxs-lookup"><span data-stu-id="ca274-117">Follow the prompts on the successive webpages to retrieve this hotfix.</span></span>



**<span data-ttu-id="ca274-118">Observação</span><span class="sxs-lookup"><span data-stu-id="ca274-118">Note</span></span>**  
<span data-ttu-id="ca274-119">Você deve instalar o pacote do espaço de trabalho do MED-V e compilar seus espaços de trabalho do MED-V antes de poder implantar os componentes do MED-v por meio do sistema de distribuição de software.</span><span class="sxs-lookup"><span data-stu-id="ca274-119">You must install the MED-V workspace packager and build your MED-V workspaces before you can deploy the MED-V components through your software distribution system.</span></span> <span data-ttu-id="ca274-120">Para obter mais informações sobre como preparar uma imagem e criar seus espaços de trabalho do MED-V, consulte [operações do MED-v](operations-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="ca274-120">For more information about how to prepare an image and to build your MED-V workspaces, see [Operations for MED-V](operations-for-med-v.md).</span></span>



**<span data-ttu-id="ca274-121">Para implantar os componentes do MED-V usando um sistema de distribuição de software</span><span class="sxs-lookup"><span data-stu-id="ca274-121">To deploy the MED-V components by using a software distribution system</span></span>**

1.  <span data-ttu-id="ca274-122">Defina um grupo de computadores e usuários no sistema de distribuição de software eletrônico como o conjunto de destino de computadores/usuários.</span><span class="sxs-lookup"><span data-stu-id="ca274-122">Define a group of computers and users in the electronic software distribution system as the target set of computers/users.</span></span>

2.  <span data-ttu-id="ca274-123">Crie pacotes para cada arquivo de instalação da Microsoft que precisa ser distribuído.</span><span class="sxs-lookup"><span data-stu-id="ca274-123">Create packages for each Microsoft installation file that needs to be distributed.</span></span> <span data-ttu-id="ca274-124">Estes são os arquivos necessários e a ordem em que devem ser instalados:</span><span class="sxs-lookup"><span data-stu-id="ca274-124">The following are the required files and the order in which they must be installed:</span></span>

    1.  <span data-ttu-id="ca274-125">**PC virtual do Windows** – se ainda não estiver instalado (é preciso reiniciar o computador).</span><span class="sxs-lookup"><span data-stu-id="ca274-125">**Windows Virtual PC** – if not already installed (a computer restart is required).</span></span> <span data-ttu-id="ca274-126">Para obter mais informações, consulte [configurar pré-requisitos de instalação](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="ca274-126">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    2.  <span data-ttu-id="ca274-127">**Inclusões e atualizações do Windows Virtual PC** – se ainda não estiverem instaladas.</span><span class="sxs-lookup"><span data-stu-id="ca274-127">**Windows Virtual PC Additions and Updates** – if not already installed.</span></span> <span data-ttu-id="ca274-128">Para obter mais informações, consulte [configurar pré-requisitos de instalação](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="ca274-128">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    3.  <span data-ttu-id="ca274-129">**Arquivo de instalação do MED-v Host Agent** – instala o arquivo de instalação do Host Agent (MED-v \ _HostAgent \ _setup instalação).</span><span class="sxs-lookup"><span data-stu-id="ca274-129">**MED-V Host Agent Installation File** – installs the Host Agent (MED-V\_HostAgent\_Setup installation file).</span></span> <span data-ttu-id="ca274-130">Para obter mais informações, consulte [como instalar manualmente o agente de host do MED-V](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="ca274-130">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

        **<span data-ttu-id="ca274-131">Aviso</span><span class="sxs-lookup"><span data-stu-id="ca274-131">Warning</span></span>**  
        <span data-ttu-id="ca274-132">Feche o Internet Explorer antes de instalar o agente de host do MED-V, caso contrário, pode ocorrer conflitos mais tarde com o redirecionamento de URL.</span><span class="sxs-lookup"><span data-stu-id="ca274-132">Close Internet Explorer before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="ca274-133">Você também pode fazer isso especificando uma reinicialização do computador durante uma distribuição.</span><span class="sxs-lookup"><span data-stu-id="ca274-133">You can also do this by specifying a computer restart during a distribution.</span></span>   

    4.  <span data-ttu-id="ca274-134">**Instalador do espaço de trabalho do MED-v, VHD e executável de configuração** – criado no **pacote do espaço de trabalho do MED-v**.</span><span class="sxs-lookup"><span data-stu-id="ca274-134">**MED-V Workspace Installer, VHD, and Setup Executable** – created in the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="ca274-135">Para obter mais informações, consulte [criar um pacote de espaço de trabalho do MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="ca274-135">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

        **<span data-ttu-id="ca274-136">Importante</span><span class="sxs-lookup"><span data-stu-id="ca274-136">Important</span></span>**  
        <span data-ttu-id="ca274-137">O arquivo de disco rígido virtual compactado (. medv) e o programa de instalação executável (setup.exe) devem estar na mesma pasta que o instalador do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="ca274-137">The compressed virtual hard disk file (.medv) and the Setup executable program (setup.exe) must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="ca274-138">Em seguida, instale o instalador do espaço de trabalho do MED-V executando setup.exe.</span><span class="sxs-lookup"><span data-stu-id="ca274-138">Then, install the MED-V workspace installer by running setup.exe.</span></span>

        **<span data-ttu-id="ca274-139">Dica</span><span class="sxs-lookup"><span data-stu-id="ca274-139">Tip</span></span>**  
        <span data-ttu-id="ca274-140">Como os problemas que podem ocorrer ao instalar o MED-V a partir de um local de rede, recomendamos que você copie os arquivos de instalação do espaço de trabalho do MED-V localmente e, em seguida, execute setup.exe.</span><span class="sxs-lookup"><span data-stu-id="ca274-140">Because problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.</span></span>       

3.  <span data-ttu-id="ca274-141">Configure os pacotes para serem executados em modo silencioso (não é necessária interação do usuário).</span><span class="sxs-lookup"><span data-stu-id="ca274-141">Configure the packages to run in silent mode (no user interaction is required).</span></span>

    <span data-ttu-id="ca274-142">Executar em modo silencioso elimina a solicitação para fechar o Internet Explorer se estiver em execução e a solicitação para iniciar o agente de host do MED-V.</span><span class="sxs-lookup"><span data-stu-id="ca274-142">Running in silent mode eliminates the prompt to close Internet Explorer if it is running and the prompt to start the MED-V Host Agent.</span></span> <span data-ttu-id="ca274-143">Ambas as ações são executadas quando o computador é reiniciado.</span><span class="sxs-lookup"><span data-stu-id="ca274-143">Both actions are performed when the computer is restarted.</span></span>

    **<span data-ttu-id="ca274-144">Observação</span><span class="sxs-lookup"><span data-stu-id="ca274-144">Note</span></span>**  
    <span data-ttu-id="ca274-145">A instalação do Windows Virtual PC exige que você reinicie o computador.</span><span class="sxs-lookup"><span data-stu-id="ca274-145">Installation of Windows Virtual PC requires you to restart the computer.</span></span> <span data-ttu-id="ca274-146">Você pode criar um único processo de instalação e instalar todos os componentes ao mesmo tempo se suprimir a reinicialização e ignorar os pré-requisitos necessários para a instalação do MED-V.</span><span class="sxs-lookup"><span data-stu-id="ca274-146">You can create a single installation process and install all the components at the same time if you suppress the restart and ignore the prerequisites necessary for MED-V to install.</span></span> <span data-ttu-id="ca274-147">Você também pode fazer isso usando argumentos de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="ca274-147">You can also do this by using command-line arguments.</span></span> <span data-ttu-id="ca274-148">Para obter um exemplo desses argumentos, consulte [para instalar os componentes do MED-V usando um arquivo em lotes](#bkmk-batch).</span><span class="sxs-lookup"><span data-stu-id="ca274-148">For an example of these arguments, see [To install the MED-V components by using a batch file](#bkmk-batch).</span></span> <span data-ttu-id="ca274-149">O MED-V é iniciado automaticamente quando o computador é reiniciado.</span><span class="sxs-lookup"><span data-stu-id="ca274-149">MED-V automatically starts when the computer is restarted.</span></span>

4.  <span data-ttu-id="ca274-150">Instale o MED-V e seus componentes antes de instalar o Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="ca274-150">Install MED-V and its components before installing Windows Virtual PC.</span></span> <span data-ttu-id="ca274-151">Consulte o arquivo em lotes de exemplo mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="ca274-151">See the example batch file later in this topic.</span></span>

    **<span data-ttu-id="ca274-152">Importante</span><span class="sxs-lookup"><span data-stu-id="ca274-152">Important</span></span>**  
    <span data-ttu-id="ca274-153">Selecione a opção **ignorar \ _PREREQUISITES** , conforme mostrado no arquivo em lotes de exemplo, de modo que os componentes do MED-V possam ser instalados antes dos componentes obrigatórios do VPC.</span><span class="sxs-lookup"><span data-stu-id="ca274-153">Select the **IGNORE\_PREREQUISITES** option as shown in the example batch file so that the MED-V components can be installed prior to the required VPC components.</span></span> <span data-ttu-id="ca274-154">Instale os componentes do MED-V nesta ordem para permitir a reinicialização única.</span><span class="sxs-lookup"><span data-stu-id="ca274-154">Install the MED-V components in this order to allow for the single restart.</span></span>

5.  <span data-ttu-id="ca274-155">Identifique outros requisitos necessários para a instalação e para o seu sistema de distribuição de software, como plataformas de destino e o espaço livre em disco.</span><span class="sxs-lookup"><span data-stu-id="ca274-155">Identify any other requirements necessary for the installation and for your software distribution system, such as target platforms and the free disk space.</span></span>

6.  <span data-ttu-id="ca274-156">Atribua os pacotes ao conjunto de destino de computadores/usuários.</span><span class="sxs-lookup"><span data-stu-id="ca274-156">Assign the packages to the target set of computers/users.</span></span>

    <span data-ttu-id="ca274-157">À medida que os computadores estão em execução, o cliente do sistema de distribuição de software reconhece que novos pacotes estão disponíveis e começa a instalar os pacotes de acordo com a definição e os requisitos.</span><span class="sxs-lookup"><span data-stu-id="ca274-157">As computers are running, the software distribution system client recognizes that new packages are available and begins to install the packages per the definition and requirements.</span></span> <span data-ttu-id="ca274-158">As instalações devem funcionar sequencialmente no modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="ca274-158">The installations should run sequentially in silent mode.</span></span> <span data-ttu-id="ca274-159">Recomendamos que isso seja executado como um único processo que não exija uma reinicialização até que todos os pacotes sejam instalados.</span><span class="sxs-lookup"><span data-stu-id="ca274-159">We recommend that this is performed as a single process that does not require a restart until all the packages are installed.</span></span>

7.  <span data-ttu-id="ca274-160">Depois que as instalações forem concluídas, reinicie os computadores atualizados.</span><span class="sxs-lookup"><span data-stu-id="ca274-160">After the installations are complete, restart the updated computers.</span></span>

    <span data-ttu-id="ca274-161">Dependendo do sistema de distribuição de software, você pode agendar uma reinicialização do computador ou os usuários finais podem reiniciar os computadores manualmente durante o trabalho normal.</span><span class="sxs-lookup"><span data-stu-id="ca274-161">Depending on the software distribution system, you can schedule a restart of the computer or the end users can restart the computers manually during their regular work.</span></span> <span data-ttu-id="ca274-162">Depois que o computador for reiniciado, o MED-V iniciará automaticamente após o logon de um usuário final.</span><span class="sxs-lookup"><span data-stu-id="ca274-162">After the computer is restarted, MED-V automatically starts after an end user logs on.</span></span> <span data-ttu-id="ca274-163">Quando o MED-V é iniciado pela primeira vez, ele é executado na primeira vez em que está configurado.</span><span class="sxs-lookup"><span data-stu-id="ca274-163">When MED-V starts for the first time, it runs first time setup.</span></span>

<span data-ttu-id="ca274-164">A configuração inicial do programa será iniciada e poderá demorar vários minutos para ser concluída, dependendo do tamanho do disco rígido virtual especificado e do número de políticas aplicado ao espaço de trabalho do MED-V na inicialização.</span><span class="sxs-lookup"><span data-stu-id="ca274-164">First time setup starts and might take several minutes to finish, depending on the size of the virtual hard disk that you specified and the number of policies applied to the MED-V workspace on startup.</span></span> <span data-ttu-id="ca274-165">O usuário final pode acompanhar o progresso observando o ícone do MED-V na área de notificação.</span><span class="sxs-lookup"><span data-stu-id="ca274-165">The end user can track the progress by watching the MED-V icon in the notification area.</span></span> <span data-ttu-id="ca274-166">Para obter mais informações sobre a configuração da primeira vez, consulte [visão geral de implantação do MED-V 2,0](med-v-20-deployment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ca274-166">For more information about first time setup, see [MED-V 2.0 Deployment Overview](med-v-20-deployment-overview.md).</span></span>

<a href="" id="bkmk-batch"></a>**<span data-ttu-id="ca274-167">Para instalar os componentes do MED-V usando um arquivo em lote</span><span class="sxs-lookup"><span data-stu-id="ca274-167">To install the MED-V components by using a batch file</span></span>**

1.  <span data-ttu-id="ca274-168">Execute a instalação em um prompt de comando com credenciais administrativas.</span><span class="sxs-lookup"><span data-stu-id="ca274-168">Run the installation at a command prompt with administrative credentials.</span></span>

2.  <span data-ttu-id="ca274-169">Implantar cada componente em um único diretório.</span><span class="sxs-lookup"><span data-stu-id="ca274-169">Deploy each component to a single directory.</span></span> <span data-ttu-id="ca274-170">Se executado de um compartilhamento de rede, um tempo maior será necessário para descompactar o arquivo. medv.</span><span class="sxs-lookup"><span data-stu-id="ca274-170">If run from a network share, a longer time is required to decompress the .medv file.</span></span>

3.  <span data-ttu-id="ca274-171">Como prática recomendada, especifique se o Windows Virtual PC e o hotfix do Windows Virtual PC estão instalados após o pacote do host do MED-V e os arquivos de pacote do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="ca274-171">As a best practice, specify that Windows Virtual PC and the Windows Virtual PC hotfix are installed after the MED-V Host Agent and the MED-V workspace package files.</span></span> <span data-ttu-id="ca274-172">Isso significa que o Windows Update não causará interferência com o processo de instalação exigindo uma reinicialização.</span><span class="sxs-lookup"><span data-stu-id="ca274-172">This means that Windows Update will not cause any interference with the installation process by requiring a restart.</span></span>

4.  <span data-ttu-id="ca274-173">Reinicie o computador após o término do arquivo em lote.</span><span class="sxs-lookup"><span data-stu-id="ca274-173">Restart the computer after the batch file is finished.</span></span>

<span data-ttu-id="ca274-174">Após a reinicialização, o usuário será solicitado a executar a configuração da primeira vez e concluir a configuração do MED-V.</span><span class="sxs-lookup"><span data-stu-id="ca274-174">After the restart, the user is prompted to run first time setup and complete the configuration of MED-V.</span></span>

<span data-ttu-id="ca274-175">O exemplo a seguir, com os argumentos especificados, mostra como instalar os componentes do 64 bits MED-V em um único processo:</span><span class="sxs-lookup"><span data-stu-id="ca274-175">The following example, with the specified arguments, shows how to install 64-bit MED-V components in a single process:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ca274-176">Argumento</span><span class="sxs-lookup"><span data-stu-id="ca274-176">Argument</span></span></th>
<th align="left"><span data-ttu-id="ca274-177">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca274-177">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ca274-178">/norestart</span><span class="sxs-lookup"><span data-stu-id="ca274-178">/norestart</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca274-179">Impede que a instalação do Windows Virtual PC e da atualização do Windows Virtual PC reinicie o computador host.</span><span class="sxs-lookup"><span data-stu-id="ca274-179">Prevents the installation of Windows Virtual PC and the Windows Virtual PC update from restarting the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ca274-180">/Quiet</span><span class="sxs-lookup"><span data-stu-id="ca274-180">/quiet</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca274-181">Instala os componentes do MED-V no modo silencioso sem a interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="ca274-181">Installs the MED-V components in quiet mode without user interaction.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ca274-182">/qn</span><span class="sxs-lookup"><span data-stu-id="ca274-182">/qn</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca274-183">Instala os componentes do MED-V sem uma interface de usuário.</span><span class="sxs-lookup"><span data-stu-id="ca274-183">Installs the MED-V components without a user interface.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ca274-184">IGNORE_PREREQUISITES</span><span class="sxs-lookup"><span data-stu-id="ca274-184">IGNORE_PREREQUISITES</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca274-185">Instala sem verificar o computador virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="ca274-185">Installs without checking for Windows Virtual PC.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="ca274-186">Observação</span><span class="sxs-lookup"><span data-stu-id="ca274-186">Note</span></span></strong><br/><p><span data-ttu-id="ca274-187">Especifique esse argumento apenas se você estiver instalando o Windows Virtual PC como parte desta instalação.</span><span class="sxs-lookup"><span data-stu-id="ca274-187">Only specify this argument if you are installing Windows Virtual PC as part of this installation.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ca274-188">OVERWRITEVHD</span><span class="sxs-lookup"><span data-stu-id="ca274-188">OVERWRITEVHD</span></span></p></td>
<td align="left"><p><span data-ttu-id="ca274-189">Força a instalação do espaço de trabalho do MED-V e impede que qualquer prompt seja gerado.</span><span class="sxs-lookup"><span data-stu-id="ca274-189">Forces the installation of the MED-V workspace and prevents any prompts that it might generate.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="ca274-190">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ca274-190">Example</span></span>


``` syntax
:: Install MED-V and the Pre-requisites

:: Install the MED-V Host Agent: install in quiet mode, ignore that Windows Virtual PC is not installed completely, and log results
start /WAIT .\MED-V_HostAgent_Setup.exe /qn IGNORE_PREREQUISITES=1 /l* %TEMP%\MEDVhost.log

:: Install the MED-V Workspace: install in quiet mode, Overwrite the VHD if it already exists, and log results
start /WAIT .\setup.exe /qn OVERWRITEVHD=1 /l* %TEMP%\MEDVworkspace.log

:: Install Windows Virtual PC: install in quiet mode and do not reboot
start /WAIT wusa.exe Windows6.1-KB958559-x64.msu /norestart /quiet

:: Install Windows Virtual PC patch to support non-HAV: install in quiet mode and do not reboot
wusa.exe Windows6.1-KB977206-x64.msu /norestart /quiet

:: After successful installation of the above components, a reboot of the host computer is required to complete installation.
```

## <span data-ttu-id="ca274-191">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ca274-191">Related topics</span></span>


[<span data-ttu-id="ca274-192">Visão geral da implantação da MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="ca274-192">MED-V 2.0 Deployment Overview</span></span>](med-v-20-deployment-overview.md)

[<span data-ttu-id="ca274-193">Implantar os componentes da MED-V</span><span class="sxs-lookup"><span data-stu-id="ca274-193">Deploy the MED-V Components</span></span>](deploy-the-med-v-components.md)









