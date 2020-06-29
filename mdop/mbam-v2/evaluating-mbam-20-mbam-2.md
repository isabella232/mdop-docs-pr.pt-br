---
title: Avaliação do MBAM 2.0
description: Avaliação do MBAM 2.0
author: dansimp
ms.assetid: bfc77eec-0fd7-4fec-9c78-6870afa87152
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b7be883f44f5f09a904f619972ae3e7c35261d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799532"
---
# <span data-ttu-id="313cd-103">Avaliação do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="313cd-103">Evaluating MBAM 2.0</span></span>


<span data-ttu-id="313cd-104">Antes de implantar o Microsoft BitLocker Administration and Monitoring (MBAM) em um ambiente de produção, você deve avaliá-lo em um ambiente de teste.</span><span class="sxs-lookup"><span data-stu-id="313cd-104">Before deploying Microsoft BitLocker Administration and Monitoring (MBAM) into a production environment, you should evaluate it in a test environment.</span></span> <span data-ttu-id="313cd-105">As informações neste tópico podem ser usadas para configurar a administração e o monitoramento do Microsoft BitLocker com uma topologia autônoma em um ambiente de teste de servidor único para fins de avaliação apenas.</span><span class="sxs-lookup"><span data-stu-id="313cd-105">The information in this topic can be used to set up Microsoft BitLocker Administration and Monitoring with a Stand-alone topology in a single-server test environment for evaluation purposes only.</span></span> <span data-ttu-id="313cd-106">Uma topologia de servidor único não é recomendada para ambientes de produção.</span><span class="sxs-lookup"><span data-stu-id="313cd-106">A single-server topology is not recommended for production environments.</span></span>

<span data-ttu-id="313cd-107">Para obter instruções sobre como implantar o MBAM em um ambiente de teste, consulte [como instalar e configurar o MBAM em um único servidor](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="313cd-107">For instructions on deploying MBAM in a test environment, see [How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md).</span></span>

## <span data-ttu-id="313cd-108">Configurando o ambiente de teste</span><span class="sxs-lookup"><span data-stu-id="313cd-108">Setting up the Test Environment</span></span>


<span data-ttu-id="313cd-109">Mesmo que você esteja configurando uma instância de não-produção de MBAM para avaliar em um ambiente de teste, você ainda deve verificar se atendeu os pré-requisitos e requisitos de hardware e software.</span><span class="sxs-lookup"><span data-stu-id="313cd-109">Even though you are setting up a non-production instance of MBAM to evaluate in a test environment, you should still verify that you have met the prerequisites and hardware and software requirements.</span></span> <span data-ttu-id="313cd-110">Antes de iniciar a instalação, consulte [pré-requisitos de implantação do MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md), [MBAM 2,0 configurações compatíveis](mbam-20-supported-configurations-mbam-2.md)e [preparando seu ambiente para o MBAM 2,0](preparing-your-environment-for-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="313cd-110">Before you start the installation, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md), [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md), and [Preparing your Environment for MBAM 2.0](preparing-your-environment-for-mbam-20-mbam-2.md).</span></span>

### <span data-ttu-id="313cd-111">Planejar uma implantação de avaliação do MBAM</span><span class="sxs-lookup"><span data-stu-id="313cd-111">Plan for an MBAM Evaluation Deployment</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="313cd-112">Tarefa</span><span class="sxs-lookup"><span data-stu-id="313cd-112">Task</span></span></th>
<th align="left"><span data-ttu-id="313cd-113">Referências</span><span class="sxs-lookup"><span data-stu-id="313cd-113">References</span></span></th>
<th align="left"><span data-ttu-id="313cd-114">Observações</span><span class="sxs-lookup"><span data-stu-id="313cd-114">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="313cd-115">Examine as informações de introdução sobre o MBAM para obter noções básicas sobre o produto antes de começar a planejar a implantação.</span><span class="sxs-lookup"><span data-stu-id="313cd-115">Review the Getting Started information about MBAM to gain a basic understanding of the product before beginning deployment planning.</span></span></p></td>
<td align="left"><p><a href="getting-started-with-mbam-20-mbam-2.md" data-raw-source="[Getting Started with MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)"><span data-ttu-id="313cd-116">Introdução ao MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="313cd-116">Getting Started with MBAM 2.0</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="313cd-117">Planeje os pré-requisitos de implantação do MBAM 2,0 e prepare o ambiente de computação.</span><span class="sxs-lookup"><span data-stu-id="313cd-117">Plan for MBAM 2.0 Deployment Prerequisites and prepare your computing environment.</span></span></p></td>
<td align="left"><p><a href="mbam-20-deployment-prerequisites-mbam-2.md" data-raw-source="[MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md)"><span data-ttu-id="313cd-118">Pré-requisitos para implantação do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="313cd-118">MBAM 2.0 Deployment Prerequisites</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="313cd-119">Planeje e configure MBAM requisitos da política de grupo.</span><span class="sxs-lookup"><span data-stu-id="313cd-119">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)"><span data-ttu-id="313cd-120">Planejar Requisitos de Política de Grupo do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="313cd-120">Planning for MBAM 2.0 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="313cd-121">Planeje e crie os grupos de segurança do ActiveDirectoryDomainServices necessários e planeje os requisitos de associação do grupo de segurança local do MBAM.</span><span class="sxs-lookup"><span data-stu-id="313cd-121">Plan for and create necessary ActiveDirectoryDomainServices security groups, and plan for MBAM local security group membership requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="313cd-122">Planejamento para Funções de Administrador do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="313cd-122">Planning for MBAM 2.0 Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="313cd-123">Plano para a implantação de recursos do MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="313cd-123">Plan for deploying MBAM Server feature deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-server-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md)"><span data-ttu-id="313cd-124">Planejar implantação de servidor MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="313cd-124">Planning for MBAM 2.0 Server Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="313cd-125">Plano para implantar a implantação do cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="313cd-125">Plan for deploying MBAM Client deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)"><span data-ttu-id="313cd-126">Planejar implantação de cliente MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="313cd-126">Planning for MBAM 2.0 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="313cd-127">Executar uma implantação de avaliação do MBAM</span><span class="sxs-lookup"><span data-stu-id="313cd-127">Perform an MBAM Evaluation Deployment</span></span>

<span data-ttu-id="313cd-128">Depois de concluir as instalações de pré-requisitos de software e planejamento necessárias para preparar o ambiente de computação para a instalação do MBAM, você pode começar a implantação de avaliação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="313cd-128">After completing the necessary planning and software prerequisite installations to prepare your computing environment for the MBAM installation, you can begin the MBAM evaluation deployment.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="313cd-129">Examine as informações de configurações compatíveis com o MBAM para garantir que os computadores cliente e servidor selecionados tenham suporte para a instalação de recursos do MBAM.</span><span class="sxs-lookup"><span data-stu-id="313cd-129">Review the MBAM supported configurations information to make sure that selected client and server computers are supported for MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"><span data-ttu-id="313cd-130">Configurações com suporte no MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="313cd-130">MBAM 2.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="313cd-131">Execute a instalação do MBAM para implantar recursos do MBAM Server em um único servidor para fins de avaliação.</span><span class="sxs-lookup"><span data-stu-id="313cd-131">Run MBAM Setup to deploy MBAM Server features on a single server for evaluation purposes.</span></span></p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md)"><span data-ttu-id="313cd-132">Como instalar e configurar o MBAM em um servidor único</span><span class="sxs-lookup"><span data-stu-id="313cd-132">How to Install and Configure MBAM on a Single Server</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="313cd-133">Adicione os grupos de segurança do ActiveDirectoryDomainServices, que você criou durante a fase de planejamento, aos grupos locais do recurso de servidor local adequado MBAM no novo servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="313cd-133">Add ActiveDirectoryDomainServices security groups, that you created during the planning phase, to the appropriate local MBAM Server feature local groups on the new MBAM Server.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="313cd-134">Planejando funções de administrador do MBAM 2,0 </a> e <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> como gerenciar funções de administrador do MBAM</span><span class="sxs-lookup"><span data-stu-id="313cd-134">Planning for MBAM 2.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="313cd-135">Criar e implantar objetos obrigatórios de política de grupo do MBAM.</span><span class="sxs-lookup"><span data-stu-id="313cd-135">Create and deploy required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)"><span data-ttu-id="313cd-136">Implantar Objetos de Política de Grupo no MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="313cd-136">Deploying MBAM 2.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="313cd-137">Implantar o software cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="313cd-137">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)"><span data-ttu-id="313cd-138">Implantando o Cliente do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="313cd-138">Deploying the MBAM 2.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="313cd-139">Configurar computadores de laboratório para avaliação do MBAM</span><span class="sxs-lookup"><span data-stu-id="313cd-139">Configure Lab Computers for MBAM Evaluation</span></span>


<span data-ttu-id="313cd-140">Esta seção contém informações que podem ser usadas para acelerar o relatório de status do cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="313cd-140">This section contains information that can be used to speed up the MBAM Client status reporting.</span></span> <span data-ttu-id="313cd-141">No entanto, essas modificações devem ser usadas somente para fins de teste.</span><span class="sxs-lookup"><span data-stu-id="313cd-141">However, these modifications should be used for testing purposes only.</span></span>

<span data-ttu-id="313cd-142">**Observação**  As informações na seção a seguir descrevem como modificar o registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="313cd-142">**Note** The information in following section describes how to modify the Windows registry.</span></span> <span data-ttu-id="313cd-143">Usar o editor do registro incorretamente pode causar sérios problemas que podem exigir a reinstalação do Windows.</span><span class="sxs-lookup"><span data-stu-id="313cd-143">Using Registry Editor incorrectly can cause serious problems that may require you to reinstall Windows.</span></span> <span data-ttu-id="313cd-144">A Microsoft não pode garantir que os problemas resultantes do uso incorreto do editor do registro possam ser resolvidos.</span><span class="sxs-lookup"><span data-stu-id="313cd-144">Microsoft cannot guarantee that problems resulting from the incorrect use of Registry Editor can be solved.</span></span> <span data-ttu-id="313cd-145">Use o editor do registro por sua conta e risco.</span><span class="sxs-lookup"><span data-stu-id="313cd-145">Use Registry Editor at your own risk.</span></span>

 

### <span data-ttu-id="313cd-146">Modificar as configurações de frequência de relatório de status do cliente do MBAM</span><span class="sxs-lookup"><span data-stu-id="313cd-146">Modify MBAM Client Status Reporting Frequency Settings</span></span>

<span data-ttu-id="313cd-147">As frequências de reutilização de cliente e status de ativação do cliente MBAM têm um valor mínimo de 90 minutos quando são definidas usando a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="313cd-147">The MBAM Client wakeup and status reporting frequencies have a minimum value of 90 minutes when they are set using Group Policy.</span></span> <span data-ttu-id="313cd-148">Você pode usar o registro do Windows para alterar essas frequências para um valor inferior em computadores cliente do MBAM para ajudar a acelerar o teste.</span><span class="sxs-lookup"><span data-stu-id="313cd-148">You can use the Windows registry to change these frequencies to a lower value on MBAM client computers to help speed up testing.</span></span>

<span data-ttu-id="313cd-149">Para modificar as configurações de frequência de relatório de status do cliente do MBAM:</span><span class="sxs-lookup"><span data-stu-id="313cd-149">To modify the MBAM Client status reporting frequency settings:</span></span>

1.  <span data-ttu-id="313cd-150">Use um editor de registro para navegar até **HKLM\\Software\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement**.</span><span class="sxs-lookup"><span data-stu-id="313cd-150">Use a registry editor to navigate to **HKLM\\Software\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement**.</span></span>

2.  <span data-ttu-id="313cd-151">Altere os valores de **ClientWakeupFrequency** e **StatusReportingFrequency** para **1** como o valor mínimo com suporte do cliente.</span><span class="sxs-lookup"><span data-stu-id="313cd-151">Change the values for **ClientWakeupFrequency** and **StatusReportingFrequency** to **1** as the minimum client-supported value.</span></span> <span data-ttu-id="313cd-152">Essa alteração faz com que o cliente do MBAM denuncie a cada minuto.</span><span class="sxs-lookup"><span data-stu-id="313cd-152">This change causes the MBAM Client to report every minute.</span></span>

3.  <span data-ttu-id="313cd-153">Reinicie o **serviço de cliente de gerenciamento de BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="313cd-153">Restart **BitLocker Management Client Service**.</span></span>

<span data-ttu-id="313cd-154">**Observação**  Para definir valores que sejam tão baixos, você deve defini-los no registro manualmente.</span><span class="sxs-lookup"><span data-stu-id="313cd-154">**Note** To set values that are this low, you must set them in the registry manually.</span></span>

 

### <span data-ttu-id="313cd-155">Modificar o atraso de inicialização do serviço do cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="313cd-155">Modify MBAM Client Service Startup Delay</span></span>

<span data-ttu-id="313cd-156">Além das frequências de reativação do cliente MBAM e status, há um atraso aleatório de até 90 minutos quando o serviço de agente cliente do MBAM é iniciado em computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="313cd-156">In addition to the MBAM Client wakeup and status reporting frequencies, there is a random delay of up to 90 minutes when the MBAM Client agent service starts on client computers.</span></span> <span data-ttu-id="313cd-157">Se você não quiser o atraso aleatório, crie um valor **DWORD** de **NoStartupDelay** em **HKLM\\Software\\Microsoft\\MBAM**, defina seu valor como **1**e, em seguida, reinicie o serviço de cliente de **Gerenciamento de BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="313cd-157">If you do not want the random delay, create a **DWORD** value of **NoStartupDelay** under **HKLM\\Software\\Microsoft\\MBAM**, set its value to **1**, and then restart **BitLocker Management Client Service**.</span></span>

## <span data-ttu-id="313cd-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="313cd-158">Related topics</span></span>


[<span data-ttu-id="313cd-159">Introdução ao MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="313cd-159">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

 

 





