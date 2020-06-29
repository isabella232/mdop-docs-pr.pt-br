---
title: Como configurar os Balanceamento de Carga de Rede para o MBAM
description: Como configurar os Balanceamento de Carga de Rede para o MBAM
author: dansimp
ms.assetid: df2208c3-352b-4a48-9722-237b0c8cd6a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a04bc74a9dab7bfe18eed8e5a3c1b6ca64d88b5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799687"
---
# <span data-ttu-id="9cb96-103">Como configurar os Balanceamento de Carga de Rede para o MBAM</span><span class="sxs-lookup"><span data-stu-id="9cb96-103">How to Configure Network Load Balancing for MBAM</span></span>


<span data-ttu-id="9cb96-104">Para verificar se você atendeu os pré-requisitos e requisitos de hardware e software para instalar o recurso de servidor de administração e monitoramento, consulte [pré-requisitos de implantação do MBAM 1,0](mbam-10-deployment-prerequisites.md) e [MBAM 1,0 configurações compatíveis](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="9cb96-104">To verify that you have met the prerequisites and hardware and software requirements to install the Administration and Monitoring Server feature, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

<span data-ttu-id="9cb96-105">**Observação**  Para obter os arquivos de log de instalação, você deve instalar o Microsoft BitLocker Administration and Monitoring (MBAM) usando o pacote **msiexec** e a opção de localização **/l** &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="9cb96-105">**Note** To obtain the setup log files, you must install Microsoft BitLocker Administration and Monitoring (MBAM) by using the **msiexec** package and the **/l** &lt;location&gt; option.</span></span> <span data-ttu-id="9cb96-106">Os arquivos de log são criados no local que você especificar.</span><span class="sxs-lookup"><span data-stu-id="9cb96-106">The Log files are created in the location that you specify.</span></span>

<span data-ttu-id="9cb96-107">Arquivos de log de instalação adicionais são criados na pasta% Temp% do usuário que instala o MBAM.</span><span class="sxs-lookup"><span data-stu-id="9cb96-107">Additional setup log files are created in the %temp% folder of the user who installs MBAM.</span></span>

 

<span data-ttu-id="9cb96-108">Os clusters de balanceamento de carga de rede (NLB) do recurso de servidor de administração e monitoramento fornecem escalabilidade no MBAM e devem oferecer suporte a mais de 55.000 computadores cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="9cb96-108">The Network Load Balancing (NLB) clusters for the Administration and Monitoring Server feature provides scalability in MBAM and it should support more than 55,000 MBAM client computers.</span></span>

<span data-ttu-id="9cb96-109">**Observação**  O balanceamento de carga de rede do Windows Server distribui solicitações de cliente em um conjunto de servidores que são configurados em um cluster de servidor único.</span><span class="sxs-lookup"><span data-stu-id="9cb96-109">**Note** Windows Server Network Load Balancing distributes client requests across a set of servers that are configured into a single server cluster.</span></span> <span data-ttu-id="9cb96-110">Quando o balanceamento de carga de rede é instalado em cada um dos servidores (hosts) em um cluster, o cluster apresenta um endereço IP virtual ou FQDN (nome de domínio totalmente qualificado) para solicitações do cliente.</span><span class="sxs-lookup"><span data-stu-id="9cb96-110">When Network Load Balancing is installed on each of the servers (hosts) in a cluster, the cluster presents a virtual IP address or fully qualified domain name (FQDN) to client requests.</span></span> <span data-ttu-id="9cb96-111">As solicitações iniciais do cliente vão para todos os hosts do cluster, mas apenas um host aceita e manipula a solicitação.</span><span class="sxs-lookup"><span data-stu-id="9cb96-111">The initial client requests go to all the hosts in the cluster, but only one host accepts and handles the request.</span></span>

<span data-ttu-id="9cb96-112">Todos os computadores que farão parte de um cluster NLB terão os seguintes requisitos:</span><span class="sxs-lookup"><span data-stu-id="9cb96-112">All computers that will be part of a NLB cluster have the following requirements:</span></span>

-   <span data-ttu-id="9cb96-113">Todos os computadores no cluster NLB devem estar no mesmo domínio.</span><span class="sxs-lookup"><span data-stu-id="9cb96-113">All computers in the NLB cluster must be in the same domain.</span></span>

-   <span data-ttu-id="9cb96-114">Cada computador no cluster NLB deve usar um endereço IP estático.</span><span class="sxs-lookup"><span data-stu-id="9cb96-114">Each computer in the NLB cluster must use a static IP address.</span></span>

-   <span data-ttu-id="9cb96-115">Cada computador do cluster NLB deve ter o balanceamento de carga de rede habilitado.</span><span class="sxs-lookup"><span data-stu-id="9cb96-115">Each computer in the NLB cluster must have Network Load Balancing enabled.</span></span>

-   <span data-ttu-id="9cb96-116">O cluster NLB requer um endereço IP estático, e um registro de host deve ser criado manualmente no sistema de nomes de domínio (DNS).</span><span class="sxs-lookup"><span data-stu-id="9cb96-116">The NLB cluster requires a static IP address, and a host record must be manually created in the domain name system (DNS).</span></span>

 

## <span data-ttu-id="9cb96-117">Configurando o balanceamento de carga de rede para servidores de administração e monitoramento MBAM</span><span class="sxs-lookup"><span data-stu-id="9cb96-117">Configuring Network Load Balancing for MBAM Administration and Monitoring Servers</span></span>


<span data-ttu-id="9cb96-118">As etapas a seguir descrevem como configurar um nome virtual e um endereço IP do cluster NLB para dois servidores de administração e monitoramento do MBAM e como configurar clientes do MBAM para usar o cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="9cb96-118">The following steps describe how to configure an NLB cluster virtual name and IP address for two MBAM Administration and Monitoring servers, and how to configure MBAM Clients to use the NLB Cluster.</span></span>

<span data-ttu-id="9cb96-119">Antes de começar os procedimentos descritos neste tópico, você deve ter o recurso de servidor de monitoramento e administração do MBAM instalado com êxito usando a mesma associação de porta do IIS em dois computadores de servidor separados que atendam aos pré-requisitos para a instalação de recursos do MBAM Server e a configuração de cluster de NLB.</span><span class="sxs-lookup"><span data-stu-id="9cb96-119">Before you begin the procedures described in this topic, you must have the MBAM Administration and Monitoring Server feature successfully installed by using the same IIS port binding on two separate server computers that meet the prerequisites for both MBAM Server feature installation and NLB Cluster configuration.</span></span>

<span data-ttu-id="9cb96-120">**Observação**  Este tópico descreve o processo básico de uso do Gerenciador de balanceamento de carga de rede para criar um cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="9cb96-120">**Note** This topic describes the basic process of using Network Load Balancing Manager to create an NLB Cluster.</span></span> <span data-ttu-id="9cb96-121">As etapas exatas para configurar um servidor Windows como parte de um cluster NLB dependem da versão do Windows Server em uso...</span><span class="sxs-lookup"><span data-stu-id="9cb96-121">The exact steps to configure a Windows Server as part of an NLB cluster depend on the Windows Server version in use..</span></span> <span data-ttu-id="9cb96-122">Para obter mais informações sobre como criar NLBs em WindowsServer2008, consulte [criando clusters de balanceamento de carga de rede](https://go.microsoft.com/fwlink/?LinkId=197176) na biblioteca do Windows Server2008 technet.</span><span class="sxs-lookup"><span data-stu-id="9cb96-122">For more information about how to create NLBs on WindowsServer2008, see [Creating Network Load Balancing Clusters](https://go.microsoft.com/fwlink/?LinkId=197176) in the Windows Server2008 TechNet library.</span></span>

 

**<span data-ttu-id="9cb96-123">Para configurar um nome virtual e um endereço IP do cluster NLB para dois servidores de administração e monitoramento do MBAM</span><span class="sxs-lookup"><span data-stu-id="9cb96-123">To configure an NLB Cluster Virtual Name and IP address for two MBAM Administration and Monitoring Servers</span></span>**

1.  <span data-ttu-id="9cb96-124">Clique em **Iniciar**, em **todos os programas**, em **Ferramentas administrativas**e, em seguida, clique em **Gerenciador de balanceamento de carga de rede**.</span><span class="sxs-lookup"><span data-stu-id="9cb96-124">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Network Load Balancing Manager**.</span></span>

    <span data-ttu-id="9cb96-125">**Observação**  Se o Gerenciador de NLB não estiver presente, você poderá instalá-lo como um recurso do WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="9cb96-125">**Note** If the NLB Manager is not present, you can install it as a WindowsServer feature.</span></span> <span data-ttu-id="9cb96-126">Você deve instalar esse recurso em servidores de administração e monitoramento do MBAM se quiser configurá-lo para o cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="9cb96-126">You must install this feature on both MBAM Administration and Monitoring servers if you want to configure it into the NLB cluster.</span></span>

     

2.  <span data-ttu-id="9cb96-127">Na barra de menus, clique em **cluster**e, em seguida, clique em **novo** para abrir a caixa de diálogo **parâmetros de cluster** .</span><span class="sxs-lookup"><span data-stu-id="9cb96-127">On the menu bar, click **Cluster**, and then click **New** to open the **Cluster Parameters** dialog box.</span></span>

3.  <span data-ttu-id="9cb96-128">Na caixa de diálogo **parâmetros de cluster** , insira as informações para a configuração de IP do cluster NLB:</span><span class="sxs-lookup"><span data-stu-id="9cb96-128">In the **Cluster Parameters** dialog box, enter the information for the NLB cluster IP configuration:</span></span>

    -   <span data-ttu-id="9cb96-129">**Endereço IP:** Endereço IP do cluster NLB registrado no DNS</span><span class="sxs-lookup"><span data-stu-id="9cb96-129">**IP address:** NLB cluster IP address registered in DNS</span></span>

    -   <span data-ttu-id="9cb96-130">**Máscara de sub-rede:** Máscara de sub-rede do endereço IP do cluster NLB registrada no DNS</span><span class="sxs-lookup"><span data-stu-id="9cb96-130">**Subnet mask:** NLB cluster IP address subnet mask registered in DNS</span></span>

    -   <span data-ttu-id="9cb96-131">**Nome de Internet completo:** FQDN do nome do cluster NLB registrado no DNS</span><span class="sxs-lookup"><span data-stu-id="9cb96-131">**Full Internet name:** FQDN of NLB cluster name registered in DNS</span></span>

4.  <span data-ttu-id="9cb96-132">Verifique se **a difusão ponto a ponto** está selecionada no **modo de operação do cluster**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="9cb96-132">Ensure that **Unicast** is selected in **Cluster operation mode**, and then click **Next**.</span></span>

5.  <span data-ttu-id="9cb96-133">Na página **endereços IP do cluster** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="9cb96-133">On the **Cluster IP Addresses** page, click **Next**.</span></span>

6.  <span data-ttu-id="9cb96-134">Na página **regras de porta** , clique em **Editar** para definir as portas para as quais o cluster NLB responderá e configurar as portas usadas para a comunicação de sistema de cliente para site conforme elas são definidas para o site ou clique em **Avançar** para habilitar o endereço IP do cluster NLB para responder a todas as portas TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="9cb96-134">On the **Port Rules** page, click **Edit** to define the ports that the NLB cluster will respond to and configure the ports that are used for client-to-site system communication as they are defined for the site, or click **Next** to enable the NLB cluster IP address to respond to all TCP/IP ports.</span></span>

    <span data-ttu-id="9cb96-135">**Observação**  Assegure-se de que a **afinidade** esteja definida como **single**.</span><span class="sxs-lookup"><span data-stu-id="9cb96-135">**Note** Ensure that **Affinity** is set to **Single**.</span></span>

     

7.  <span data-ttu-id="9cb96-136">Na página **conectar** , insira um nome de host da instância do MBAM Administration and Monitoring Server que fará parte do cluster NLB no **host**e, em seguida, clique em **conectar**.</span><span class="sxs-lookup"><span data-stu-id="9cb96-136">On the **Connect** page, enter an MBAM Administration and Monitoring server instance host name that will be part of the NLB cluster in **Host**, and then click **Connect**.</span></span>

8.  <span data-ttu-id="9cb96-137">Em **interfaces disponíveis para configurar um novo cluster**, selecione a interface de rede que será configurada para responder à comunicação do cluster NLB e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="9cb96-137">In **Interfaces available for configuring a new cluster**, select the networking interface that will be configured to respond to NLB cluster communication, and then click **Next**.</span></span>

9.  <span data-ttu-id="9cb96-138">Na página **parâmetros do host** , revise as informações exibidas para garantir que as configurações de **configuração de IP dedicado** exibam a configuração de IP de host dedicada para o host de cluster NLB correto, verifique se o estado inicial do host do estado **padrão:** é **iniciado**e clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="9cb96-138">On the **Host Parameters** page, review the information displayed to ensure that the **Dedicated IP configuration** settings display the dedicated host IP configuration for the correct NLB cluster host, check that the Initial host state **Default state:** is **Started**, and then click **Finish**.</span></span>

    <span data-ttu-id="9cb96-139">**Observação**  A página **parâmetros do host** também exibe a prioridade do host do cluster NLB, que é de 1 a 32.</span><span class="sxs-lookup"><span data-stu-id="9cb96-139">**Note** The **Host Parameters** page also displays the NLB cluster host priority, which is 1 through 32.</span></span> <span data-ttu-id="9cb96-140">À medida que novos hosts são adicionados ao cluster NLB, a prioridade do host deve ser diferente dos hosts adicionados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9cb96-140">As new hosts are added to the NLB cluster, the host priority must differ from the previously added hosts.</span></span> <span data-ttu-id="9cb96-141">A prioridade é incrementada automaticamente quando você usa o Gerenciador de balanceamento de carga de rede.</span><span class="sxs-lookup"><span data-stu-id="9cb96-141">The priority is automatically incremented when you use the Network Load Balancing Manager.</span></span>

     

10. <span data-ttu-id="9cb96-142">Clique em \*\* &lt; &gt; nome do cluster NLB\*\* e certifique-se de que o **status** da interface do host NLB seja exibido **convergido** antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="9cb96-142">Click **&lt;NLB cluster name&gt;** and ensure that the NLB host interface **Status** displays **Converged** before you continue.</span></span> <span data-ttu-id="9cb96-143">Esta etapa pode exigir que você atualize a exibição do cluster NLB como a configuração de TCP/IP do host que está sendo modificada pelo Gerenciador de NLB.</span><span class="sxs-lookup"><span data-stu-id="9cb96-143">This step might require that you refresh the NLB cluster display as the host TCP/IP configuration that is being modified by the NLB Manager.</span></span>

11. <span data-ttu-id="9cb96-144">Para adicionar mais hosts ao cluster NLB, clique com o botão direito do mouse em \*\* &lt; nome &gt; do cluster NLB\*\*, clique em **Adicionar host ao cluster** e repita as etapas 7 a 10 para cada sistema de site que fará parte do cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="9cb96-144">To add additional hosts to the NLB cluster, right-click **&lt;NLB cluster name&gt;**, click **Add Host to Cluster,** and then repeat steps 7 through 10 for each site system that will be part of the NLB cluster.</span></span>

12. <span data-ttu-id="9cb96-145">Em um computador que tenha o modelo de política de grupo do MBAM instalado, modifique as configurações da política de grupo do MBAM para configurar os pontos de extremidade dos serviços do MBAM para usar o nome do cluster NLB e a associação de porta do IIS apropriada para acessar os recursos do MBAM de administração e do servidor de monitoramento instalados nos computadores do cluster NLB.</span><span class="sxs-lookup"><span data-stu-id="9cb96-145">On a computer that has MBAM Group Policy template installed, modify the MBAM Group Policy settings to configure the MBAM services endpoints to use the NLB Cluster name and the appropriate IIS port binding to access the MBAM Administration and Monitoring Server features that are installed on the NLB Cluster computers.</span></span> <span data-ttu-id="9cb96-146">Para obter mais informações sobre como editar configurações do GPO MBAM, consulte [como editar configurações de GPO do MBAM 1,0](how-to-edit-mbam-10-gpo-settings.md).</span><span class="sxs-lookup"><span data-stu-id="9cb96-146">For more information about how to edit MBAM GPO settings, see [How to Edit MBAM 1.0 GPO Settings](how-to-edit-mbam-10-gpo-settings.md).</span></span> <span data-ttu-id="9cb96-147">Se os servidores de administração e administração do MBAM são novos no seu ambiente, verifique se as associações de grupo de segurança local necessárias foram configuradas corretamente.</span><span class="sxs-lookup"><span data-stu-id="9cb96-147">If the MBAM Administration and Monitoring servers are new to your environment, ensure that the required local security group memberships have been properly configured.</span></span> <span data-ttu-id="9cb96-148">Para obter mais informações sobre os requisitos de grupo de segurança, consulte [planejando funções de administrador do MBAM 1,0](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="9cb96-148">For more information about security group requirements, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

13. <span data-ttu-id="9cb96-149">Quando a configuração do cluster NLB estiver concluída, recomendamos que você valide se a administração do MBAM e o monitoramento do cluster NLB funcionam.</span><span class="sxs-lookup"><span data-stu-id="9cb96-149">When the NLB Cluster configuration is complete, we recommend that you validate that the MBAM Administration and Monitoring NLB Cluster is functional.</span></span> <span data-ttu-id="9cb96-150">Para fazer isso, abra um navegador da Web em um computador que não seja o servidor que está configurado no NLB e certifique-se de que você possa acessar o site de administração e monitoramento do MBAM usando o FQDN do NLB.</span><span class="sxs-lookup"><span data-stu-id="9cb96-150">To do this, open a web browser on a computer other than the servers that are configured in the NLB, and ensure that you can access the MBAM Administration and Monitoring web site by using the NLB FQDN.</span></span>

## <span data-ttu-id="9cb96-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9cb96-151">Related topics</span></span>


[<span data-ttu-id="9cb96-152">Implantando a infraestrutura do Servidor do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="9cb96-152">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)

 

 





