---
title: Avaliação do MBAM 1.0
description: Avaliação do MBAM 1.0
author: dansimp
ms.assetid: a1e2b674-eda9-4e1c-9b4c-e748470c71f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f09b06af52f5738fd50bfe727987b760d98552d9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799635"
---
# <span data-ttu-id="0c13d-103">Avaliação do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="0c13d-103">Evaluating MBAM 1.0</span></span>


<span data-ttu-id="0c13d-104">Antes de implantar o Microsoft BitLocker Administration and Monitoring (MBAM) em um ambiente de produção, você deve avaliá-lo em um ambiente de laboratório.</span><span class="sxs-lookup"><span data-stu-id="0c13d-104">Before you deploy Microsoft BitLocker Administration and Monitoring (MBAM) into a production environment, you should evaluate it in a lab environment.</span></span> <span data-ttu-id="0c13d-105">Você pode usar as informações neste tópico para configurar o MBAM em um ambiente de laboratório de servidor único para fins de avaliação apenas.</span><span class="sxs-lookup"><span data-stu-id="0c13d-105">You can use the information in this topic to set up MBAM in a single server lab environment for evaluation purposes only.</span></span>

<span data-ttu-id="0c13d-106">Embora as etapas de implantação reais sejam muito semelhantes ao cenário descrito em [como instalar e configurar o MBAM em um único servidor](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md), este tópico contém informações adicionais para permitir que você configure um ambiente de avaliação do MBAM no mínimo de tempo.</span><span class="sxs-lookup"><span data-stu-id="0c13d-106">While the actual deployment steps are very similar to the scenario that is described in [How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md), this topic contains additional information to enable you to set up an MBAM evaluation environment in the least amount of time.</span></span>

## <span data-ttu-id="0c13d-107">Configurar o ambiente de laboratório</span><span class="sxs-lookup"><span data-stu-id="0c13d-107">Set up the Lab Environment</span></span>


<span data-ttu-id="0c13d-108">Mesmo quando você configura uma instância de não-produção de MBAM para avaliar em um ambiente de laboratório, você ainda deve verificar se atendeu os pré-requisitos de implantação e os requisitos de hardware e software.</span><span class="sxs-lookup"><span data-stu-id="0c13d-108">Even when you set up a non-production instance of MBAM to evaluate in a lab environment, you should still verify that you have met the deployment prerequisites and the hardware and software requirements.</span></span> <span data-ttu-id="0c13d-109">Para obter mais informações, consulte [pré-requisitos de implantação do MBAM 1,0](mbam-10-deployment-prerequisites.md) e [MBAM 1,0 configurações compatíveis](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="0c13d-109">For more information, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span> <span data-ttu-id="0c13d-110">Você também deve rever [a preparação do seu ambiente para o MBAM 1,0](preparing-your-environment-for-mbam-10.md) antes de começar a implantação de avaliação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0c13d-110">You should also review [Preparing your Environment for MBAM 1.0](preparing-your-environment-for-mbam-10.md) before you begin the MBAM evaluation deployment.</span></span>

### <span data-ttu-id="0c13d-111">Planejar uma implantação de avaliação do MBAM</span><span class="sxs-lookup"><span data-stu-id="0c13d-111">Plan for an MBAM Evaluation Deployment</span></span>

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
<th align="left"><span data-ttu-id="0c13d-112">Tarefa</span><span class="sxs-lookup"><span data-stu-id="0c13d-112">Task</span></span></th>
<th align="left"><span data-ttu-id="0c13d-113">Referências</span><span class="sxs-lookup"><span data-stu-id="0c13d-113">References</span></span></th>
<th align="left"><span data-ttu-id="0c13d-114">Observações</span><span class="sxs-lookup"><span data-stu-id="0c13d-114">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="0c13d-115">Examine as informações de introdução sobre o MBAM para obter noções básicas sobre o produto antes de começar o planejamento de implantação.</span><span class="sxs-lookup"><span data-stu-id="0c13d-115">Review the Getting Started information about MBAM to gain a basic understanding of the product before you begin your deployment planning.</span></span></p></td>
<td align="left"><p><a href="getting-started-with-mbam-10.md" data-raw-source="[Getting Started with MBAM 1.0](getting-started-with-mbam-10.md)"><span data-ttu-id="0c13d-116">Introdução ao MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="0c13d-116">Getting Started with MBAM 1.0</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p></p>
<p><span data-ttu-id="0c13d-117">Prepare o ambiente de computação para a instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0c13d-117">Prepare your computing environment for the MBAM installation.</span></span> <span data-ttu-id="0c13d-118">Para fazer isso, você deve habilitar a criptografia de dados transparente (TDE) nas instâncias do SQL Server que hospedam bancos de dados do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0c13d-118">To do so, you must enable the Transparent Data Encryption (TDE) on the SQL Server instances that will host MBAM databases.</span></span> <span data-ttu-id="0c13d-119">Para habilitar o TDE em seu ambiente de laboratório, você pode criar um arquivo. SQL para ser executado em relação ao banco de dados mestre que está hospedado na instância do SQL Server que MBAM usará.</span><span class="sxs-lookup"><span data-stu-id="0c13d-119">To enable TDE in your lab environment, you can create a .sql file to run against the master database that is hosted on the instance of the SQL Server that MBAM will use.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="0c13d-120">Observação</span><span class="sxs-lookup"><span data-stu-id="0c13d-120">Note</span></span></strong><br/><p><span data-ttu-id="0c13d-121">Você pode usar o exemplo a seguir para criar um arquivo. SQL para seu ambiente de laboratório para habilitar rapidamente o TDE na instância do SQL Server que hospedará os bancos de dados do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0c13d-121">You can use the following example to create a .sql file for your lab environment to quickly enable TDE on the SQL Server instance that will host the MBAM databases.</span></span> <span data-ttu-id="0c13d-122">Esses comandos do SQL Server habilitarão o TDE usando um certificado SQL Server assinado localmente.</span><span class="sxs-lookup"><span data-stu-id="0c13d-122">These SQL Server commands will enable TDE by using a locally signed SQL Server certificate.</span></span> <span data-ttu-id="0c13d-123">Certifique-se de fazer backup do certificado TDE e da chave de criptografia associada ao caminho de backup local do <em> C:\backup </em> .</span><span class="sxs-lookup"><span data-stu-id="0c13d-123">Make sure to back up the TDE certificate and its associated encryption key to the example local backup path of <em>C:\Backup</em>.</span></span> <span data-ttu-id="0c13d-124">O certificado e a chave do TDE são necessários ao recuperar o banco de dados ou mover o certificado e a chave para outro servidor que tenha a criptografia TDE no local.</span><span class="sxs-lookup"><span data-stu-id="0c13d-124">The TDE certificate and key are required when recover the database or move the certificate and key to another server that has TDE encryption in place.</span></span></p>
</div>
<div>

</div>
<pre class="syntax" space="preserve"><code>USE master;
GO
CREATE MASTER KEY ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;;
GO
CREATE CERTIFICATE tdeCert WITH SUBJECT = &#39;TDE Certificate&#39;;
GO
BACKUP CERTIFICATE tdeCert TO FILE = &#39;C:\Backup\TDECertificate.cer&#39;
   WITH PRIVATE KEY (
         FILE = &#39;C:\Backup\TDECertificateKey.pvk&#39;,
         ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;);
GO</code></pre></td>
<td align="left"><p><a href="mbam-10-deployment-prerequisites.md" data-raw-source="[MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md)"><span data-ttu-id="0c13d-125">Pré-requisitos para implantação do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="0c13d-125">MBAM 1.0 Deployment Prerequisites</span></span></a></p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=269703" data-raw-source="[Database Encryption in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703)"><span data-ttu-id="0c13d-126">Criptografia de banco de dados no SQL Server 2008 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="0c13d-126">Database Encryption in SQL Server 2008 Enterprise Edition</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="0c13d-127">Planeje e configure MBAM requisitos da política de grupo.</span><span class="sxs-lookup"><span data-stu-id="0c13d-127">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-group-policy-requirements.md" data-raw-source="[Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md)"><span data-ttu-id="0c13d-128">Planejar Requisitos de Política de Grupo do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="0c13d-128">Planning for MBAM 1.0 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="0c13d-129">Planeje e crie os grupos de segurança dos serviços de domínio do Active Directory necessários e planeje os requisitos de associação do grupo de segurança local do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0c13d-129">Plan for and create the necessary Active Directory Domain Services security groups and plan for MBAM local security group membership requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)"><span data-ttu-id="0c13d-130">Planejamento para Funções de Administrador do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="0c13d-130">Planning for MBAM 1.0 Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="0c13d-131">Planeje a implantação de recursos do MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="0c13d-131">Plan for MBAM Server feature deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-server-deployment.md" data-raw-source="[Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md)"><span data-ttu-id="0c13d-132">Planejar implantação de servidor MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="0c13d-132">Planning for MBAM 1.0 Server Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="0c13d-133">Plano para a implantação do cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="0c13d-133">Plan for MBAM Client deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-client-deployment.md" data-raw-source="[Planning for MBAM 1.0 Client Deployment](planning-for-mbam-10-client-deployment.md)"><span data-ttu-id="0c13d-134">Planejar implantação de cliente MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="0c13d-134">Planning for MBAM 1.0 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="0c13d-135">Executar uma implantação de avaliação do MBAM</span><span class="sxs-lookup"><span data-stu-id="0c13d-135">Perform an MBAM Evaluation Deployment</span></span>

<span data-ttu-id="0c13d-136">Depois de concluir as instalações de pré-requisitos de software e planejamento necessárias para preparar o ambiente de computação para uma instalação do MBAM, você pode começar a implantação de avaliação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0c13d-136">After you complete the necessary planning and software prerequisite installations to prepare your computing environment for an MBAM installation, you can begin the MBAM evaluation deployment.</span></span>

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
<td align="left"><p><span data-ttu-id="0c13d-137">Examine as informações de configurações compatíveis com o MBAM para garantir que os computadores cliente e servidor selecionados tenham suporte para a instalação do recurso MBAM.</span><span class="sxs-lookup"><span data-stu-id="0c13d-137">Review the MBAM supported configurations information to make sure that the selected client and server computers are supported for the MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)"><span data-ttu-id="0c13d-138">Configurações com suporte no MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="0c13d-138">MBAM 1.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="0c13d-139">Execute a instalação do MBAM para implantar recursos do MBAM Server em um único servidor para fins de avaliação.</span><span class="sxs-lookup"><span data-stu-id="0c13d-139">Run MBAM Setup to deploy MBAM Server features on a single server for evaluation purposes.</span></span></p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)"><span data-ttu-id="0c13d-140">Como instalar e configurar o MBAM em um servidor único</span><span class="sxs-lookup"><span data-stu-id="0c13d-140">How to Install and Configure MBAM on a Single Server</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="0c13d-141">Adicione os grupos de segurança dos serviços de domínio Active Directory que você criou durante a fase de planejamento para os grupos locais do recurso de servidor local MBAM no novo servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="0c13d-141">Add the Active Directory Domain Services security groups that you created during the planning phase to the appropriate local MBAM Server feature local groups on the new MBAM server.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)"><span data-ttu-id="0c13d-142">Planejando funções de administrador do MBAM 1,0 </a> e <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> como gerenciar funções de administrador do MBAM</span><span class="sxs-lookup"><span data-stu-id="0c13d-142">Planning for MBAM 1.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="0c13d-143">Criar e implantar os objetos de política de grupo MBAM necessários.</span><span class="sxs-lookup"><span data-stu-id="0c13d-143">Create and deploy the required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)"><span data-ttu-id="0c13d-144">Implantar Objetos de Política de Grupo no MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="0c13d-144">Deploying MBAM 1.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="0c13d-145">Implantar o software cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0c13d-145">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)"><span data-ttu-id="0c13d-146">Implantando o Cliente do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="0c13d-146">Deploying the MBAM 1.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="0c13d-147">Configurar computadores de laboratório para avaliação do MBAM</span><span class="sxs-lookup"><span data-stu-id="0c13d-147">Configure Lab Computers for MBAM Evaluation</span></span>


<span data-ttu-id="0c13d-148">Você pode alterar as configurações de frequência nos relatórios de status do cliente MBAM usando o editor do registro.</span><span class="sxs-lookup"><span data-stu-id="0c13d-148">You can change the frequency settings on the MBAM Client status reporting by using Registry Editor.</span></span> <span data-ttu-id="0c13d-149">No entanto, essas modificações devem ser usadas somente para fins de teste.</span><span class="sxs-lookup"><span data-stu-id="0c13d-149">However, these modifications should be used for testing purposes only.</span></span>

**<span data-ttu-id="0c13d-150">Aviso</span><span class="sxs-lookup"><span data-stu-id="0c13d-150">Warning</span></span>**  
<span data-ttu-id="0c13d-151">Este tópico descreve como alterar o registro do Windows usando o editor do registro.</span><span class="sxs-lookup"><span data-stu-id="0c13d-151">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="0c13d-152">Se você alterar o registro do Windows incorretamente, poderá causar sérios problemas que talvez exijam a reinstalação do Windows.</span><span class="sxs-lookup"><span data-stu-id="0c13d-152">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="0c13d-153">Você deve fazer uma cópia de backup dos arquivos do registro (System. dat e User. dat) antes de alterar o registro.</span><span class="sxs-lookup"><span data-stu-id="0c13d-153">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="0c13d-154">A Microsoft não pode garantir que os problemas que podem ocorrer quando você alterar o registro possam ser resolvidos.</span><span class="sxs-lookup"><span data-stu-id="0c13d-154">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="0c13d-155">Altere o registro por sua conta e risco.</span><span class="sxs-lookup"><span data-stu-id="0c13d-155">Change the registry at your own risk.</span></span>



### <a href="" id="modify-the-frequency-settings-on-mbam-client-status-reporting-"></a><span data-ttu-id="0c13d-156">Modificar as configurações de frequência no relatório de status do cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="0c13d-156">Modify the Frequency Settings on MBAM Client Status Reporting</span></span>

<span data-ttu-id="0c13d-157">As frequências de reutilização de cliente e status de ativação do cliente MBAM têm um valor mínimo de 90 minutos quando são definidas para usar a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="0c13d-157">The MBAM Client wakeup and status reporting frequencies have a minimum value of 90 minutes when they are set to use Group Policy.</span></span> <span data-ttu-id="0c13d-158">Você pode alterar essas frequências em computadores cliente do MBAM editando o registro do Windows para valores menores, o que ajudará a acelerar o teste.</span><span class="sxs-lookup"><span data-stu-id="0c13d-158">You can change these frequencies on MBAM client computers by editing the Windows registry to lower values, which will help speed up the testing.</span></span> <span data-ttu-id="0c13d-159">Para modificar as configurações de frequência em MBAM relatório de status do cliente, use um editor do registro para navegar para **HKLM\\Software\\Policies\\FVE\\MDOPBitLockerManagement**, altere os valores para **ClientWakeupFrequency** e **StatusReportingFrequency** para **1** como o valor mínimo com suporte do cliente e, em seguida, reinicie o serviço de cliente de gerenciamento de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0c13d-159">To modify the frequency settings on MBAM Client status reporting, use a registry editor to navigate to **HKLM\\Software\\Policies\\FVE\\MDOPBitLockerManagement**, change the values for **ClientWakeupFrequency** and **StatusReportingFrequency** to **1** as the minimum client supported value, and then restart BitLocker Management Client Service.</span></span> <span data-ttu-id="0c13d-160">Quando você fizer essa alteração, o cliente do MBAM se reportará a cada minuto.</span><span class="sxs-lookup"><span data-stu-id="0c13d-160">When you make this change, the MBAM Client will report every minute.</span></span> <span data-ttu-id="0c13d-161">Você pode definir valores tão baixos apenas quando faz isso manualmente no registro.</span><span class="sxs-lookup"><span data-stu-id="0c13d-161">You can set values this low only when you do so manually in the registry.</span></span>

### <a href="" id="modify-the-startup-delay-on-mbam-client-service-"></a><span data-ttu-id="0c13d-162">Modificar o atraso de inicialização no serviço de cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="0c13d-162">Modify the Startup Delay on MBAM Client Service</span></span>

<span data-ttu-id="0c13d-163">Além das frequências de reativação do cliente MBAM e status, há um atraso aleatório de até 90 minutos quando o serviço de agente cliente do MBAM é iniciado em computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="0c13d-163">In addition to the MBAM Client wakeup and status reporting frequencies, there is a random delay of up to 90 minutes when the MBAM Client agent service starts on client computers.</span></span> <span data-ttu-id="0c13d-164">Se você não quiser o atraso aleatório, crie um valor **DWORD** de **NoStartupDelay** em **HKLM\\Software\\Microsoft\\MBAM**, defina seu valor como **1**e, em seguida, reinicie o serviço de cliente de gerenciamento de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0c13d-164">If you do not want the random delay, create a **DWORD** value of **NoStartupDelay** under **HKLM\\Software\\Microsoft\\MBAM**, set its value to **1**, and then restart BitLocker Management Client Service.</span></span>

## <span data-ttu-id="0c13d-165">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0c13d-165">Related topics</span></span>


[<span data-ttu-id="0c13d-166">Introdução ao MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="0c13d-166">Getting Started with MBAM 1.0</span></span>](getting-started-with-mbam-10.md)









