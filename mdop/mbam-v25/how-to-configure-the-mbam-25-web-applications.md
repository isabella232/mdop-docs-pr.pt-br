---
title: Como configurar os aplicativos Web do MBAM 2.5
description: Como configurar os aplicativos Web do MBAM 2.5
author: dansimp
ms.assetid: 909bf2d3-028c-4ac1-9247-171532a1eeae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0336d24f51167a00c8565ccd081f4bc5dfb2c4cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799484"
---
# <span data-ttu-id="f073b-103">Como configurar os aplicativos Web do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f073b-103">How to Configure the MBAM 2.5 Web Applications</span></span>


<span data-ttu-id="f073b-104">Este tópico explica como configurar os aplicativos da Web do Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 para a [arquitetura de alto nível recomendada para o MBAM 2,5](high-level-architecture-for-mbam-25.md) usando um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="f073b-104">This topic explains how to configure the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 web applications for the recommended [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md) by using one of the following methods:</span></span>

-   <span data-ttu-id="f073b-105">Um cmdlet do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f073b-105">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="f073b-106">O assistente de configuração do servidor do MBAM</span><span class="sxs-lookup"><span data-stu-id="f073b-106">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="f073b-107">Os aplicativos Web incluem os seguintes websites e seus serviços Web correspondentes:</span><span class="sxs-lookup"><span data-stu-id="f073b-107">The web applications comprise the following websites and their corresponding web services:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f073b-108">Website</span><span class="sxs-lookup"><span data-stu-id="f073b-108">Website</span></span></th>
<th align="left"><span data-ttu-id="f073b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f073b-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f073b-110">Site de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="f073b-110">Administration and Monitoring Website</span></span></p></td>
<td align="left"><p><span data-ttu-id="f073b-111">Site em que os usuários especificados podem exibir relatórios e ajudar os usuários finais a recuperarem seus computadores quando eles esquecem seu PIN ou senha</span><span class="sxs-lookup"><span data-stu-id="f073b-111">Website where specified users can view reports and help end users recover their computers when they forget their PIN or password</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f073b-112">Portal de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="f073b-112">Self-Service Portal</span></span></p></td>
<td align="left"><p><span data-ttu-id="f073b-113">O website que os usuários finais podem acessar para restabelecer o acesso de forma independente a seus computadores se eles esquecerem do PIN ou da senha</span><span class="sxs-lookup"><span data-stu-id="f073b-113">Website that end users can access to independently regain access to their computers if they forget their PIN or password</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="f073b-114">Antes de iniciar a configuração:</span><span class="sxs-lookup"><span data-stu-id="f073b-114">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f073b-115">Etapa</span><span class="sxs-lookup"><span data-stu-id="f073b-115">Step</span></span></th>
<th align="left"><span data-ttu-id="f073b-116">Onde obter instruções</span><span class="sxs-lookup"><span data-stu-id="f073b-116">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f073b-117">Examine a arquitetura recomendada para MBAM.</span><span class="sxs-lookup"><span data-stu-id="f073b-117">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="f073b-118">Arquitetura de alto nível do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f073b-118">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f073b-119">Examine as configurações com suporte para MBAM.</span><span class="sxs-lookup"><span data-stu-id="f073b-119">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="f073b-120">Configurações com suporte no MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f073b-120">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f073b-121">Complete os pré-requisitos obrigatórios em cada servidor.</span><span class="sxs-lookup"><span data-stu-id="f073b-121">Complete the required prerequisites on each server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="f073b-122">Observação</span><span class="sxs-lookup"><span data-stu-id="f073b-122">Note</span></span></strong><br/><p><span data-ttu-id="f073b-123">Certifique-se de configurar o SSRS (serviços do SQL ServerReporting) para usar a SSL (Secure Sockets Layer) antes de configurar o site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="f073b-123">Ensure that you configure SQL ServerReporting Services (SSRS) to use the Secure Sockets Layer (SSL) before you configure the Administration and Monitoring Website.</span></span> <span data-ttu-id="f073b-124">Caso contrário, o recurso relatórios irá usar HTTP em vez de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f073b-124">Otherwise, the Reports feature will use HTTP instead of HTTPS.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="f073b-125">Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f073b-125">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="f073b-126">MBAM 2,5-pré-requisitos do servidor que se aplicam somente à topologia de integração do Configuration Manager </a> (se aplicável)</span><span class="sxs-lookup"><span data-stu-id="f073b-126">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</a> (if applicable)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f073b-127">Registre os SPNs (nomes de entidade de serviço) da conta do pool de aplicativos para os sites.</span><span class="sxs-lookup"><span data-stu-id="f073b-127">Register service principal names (SPNs) for the application pool account for the websites.</span></span> <span data-ttu-id="f073b-128">Você só precisará fazer esta etapa se não tiver direitos de domínio administrativo nos serviços de domínio Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="f073b-128">You need to do this step only if you do not have administrative domain rights in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="f073b-129">Se você tiver esses direitos no AD DS, o MBAM criará os SPNs para você.</span><span class="sxs-lookup"><span data-stu-id="f073b-129">If you do have these rights in AD DS, MBAM will create the SPNs for you.</span></span></p></td>
<td align="left"><p><a href="planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn)"><span data-ttu-id="f073b-130">Planejamento de formas para proteger os sites do MBAM</span><span class="sxs-lookup"><span data-stu-id="f073b-130">Planning How to Secure the MBAM Websites</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f073b-131">Instale o software do servidor MBAM em cada servidor em que você irá configurar um recurso do servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="f073b-131">Install the MBAM Server software on each server where you will configure an MBAM Server feature.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="f073b-132">Observação</span><span class="sxs-lookup"><span data-stu-id="f073b-132">Note</span></span></strong><br/><p><span data-ttu-id="f073b-133">Se você planeja instalar os sites em um servidor e nos serviços Web em outro, poderá configurá-los somente usando o <strong> cmdlet Enable-MbamWebApplication do </strong> Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f073b-133">If you plan to install the websites on one server and the web services on another, you will be able to configure them only by using the <strong>Enable-MbamWebApplication</strong> Windows PowerShell cmdlet.</span></span> <span data-ttu-id="f073b-134">O assistente de configuração do servidor do MBAM não dá suporte à configuração desses itens em servidores separados.</span><span class="sxs-lookup"><span data-stu-id="f073b-134">The MBAM Server Configuration wizard does not support configuring these items on separate servers.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="f073b-135">Instalando o software de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f073b-135">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f073b-136">Examine os pré-requisitos para usar o Windows PowerShell se você planeja usar cmdlets para configurar os recursos do MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="f073b-136">Review the prerequisites for using Windows PowerShell if you plan to use cmdlets to configure MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="f073b-137">Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f073b-137">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="f073b-138">Para configurar os aplicativos Web usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f073b-138">To configure the web applications by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="f073b-139">Antes de iniciar a configuração, confira [Configurando os recursos do servidor do MBAM 2,5 usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) para revisar os pré-requisitos para usar o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f073b-139">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="f073b-140">Use o cmdlet **Enable-MbamWebApplication** para configurar os aplicativos Web usando o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f073b-140">Use the **Enable-MbamWebApplication** cmdlet to configure the web applications using Windows PowerShell.</span></span> <span data-ttu-id="f073b-141">Para obter informações sobre esse cmdlet, digite **Get-Help Enable-MbamWebApplication**.</span><span class="sxs-lookup"><span data-stu-id="f073b-141">To get information about this cmdlet, type **Get-Help Enable-MbamWebApplication**.</span></span>

**<span data-ttu-id="f073b-142">Para definir as configurações de todos os aplicativos Web usando o assistente</span><span class="sxs-lookup"><span data-stu-id="f073b-142">To configure the settings for all web applications using the wizard</span></span>**

1. <span data-ttu-id="f073b-143">No servidor em que você deseja configurar os aplicativos Web, inicie o assistente de configuração do MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="f073b-143">On the server where you want to configure the web applications, start the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="f073b-144">Você pode selecionar **configuração do servidor MBAM** no menu **Iniciar** para abrir o assistente.</span><span class="sxs-lookup"><span data-stu-id="f073b-144">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="f073b-145">Clique em **Adicionar novos recursos**, selecione **site de administração e monitoramento** e portal de **autoatendimento**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="f073b-145">Click **Add New Features**, select **Administration and Monitoring Website** and **Self-Service Portal**, and then click **Next**.</span></span> <span data-ttu-id="f073b-146">O assistente verifica se todos os pré-requisitos para os aplicativos da Web foram atendidos.</span><span class="sxs-lookup"><span data-stu-id="f073b-146">The wizard checks that all prerequisites for the web applications have been met.</span></span>

3. <span data-ttu-id="f073b-147">Se a verificação de pré-requisito for bem-sucedida, clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="f073b-147">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="f073b-148">Caso contrário, resolva todos os pré-requisitos ausentes e clique em **verificar pré-requisitos novamente**.</span><span class="sxs-lookup"><span data-stu-id="f073b-148">Otherwise, resolve any missing prerequisites, and then click **Check prerequisites again**.</span></span>

4. <span data-ttu-id="f073b-149">Use as descrições a seguir para inserir os valores de campo no assistente.</span><span class="sxs-lookup"><span data-stu-id="f073b-149">Use the following descriptions to enter the field values in the wizard.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><strong><span data-ttu-id="f073b-150">Campo</span><span class="sxs-lookup"><span data-stu-id="f073b-150">Field</span></span></strong></th>
   <th align="left"><span data-ttu-id="f073b-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="f073b-151">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f073b-152">Certificado de segurança</span><span class="sxs-lookup"><span data-stu-id="f073b-152">Security certificate</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f073b-153">Selecione um certificado criado anteriormente para criptografar opcionalmente a comunicação entre os serviços Web e o servidor no qual você está configurando os sites.</span><span class="sxs-lookup"><span data-stu-id="f073b-153">Select a previously created certificate to optionally encrypt the communication between the web services and the server on which you are configuring the websites.</span></span> <span data-ttu-id="f073b-154">Se você optar <strong> por não usar um certificado </strong> , talvez sua comunicação à Web não seja segura.</span><span class="sxs-lookup"><span data-stu-id="f073b-154">If you choose <strong>Do not use a certificate</strong>, your web communication may not be secure.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="f073b-155">Nome do host</span><span class="sxs-lookup"><span data-stu-id="f073b-155">Host name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f073b-156">Nome do computador host em que você está configurando os sites.</span><span class="sxs-lookup"><span data-stu-id="f073b-156">Name of the host computer where you are configuring the websites.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f073b-157">Caminho de instalação</span><span class="sxs-lookup"><span data-stu-id="f073b-157">Installation path</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f073b-158">Caminho onde você está instalando os sites.</span><span class="sxs-lookup"><span data-stu-id="f073b-158">Path where you are installing the websites.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="f073b-159">Port</span><span class="sxs-lookup"><span data-stu-id="f073b-159">Port</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f073b-160">Número da porta a ser usado para a comunicação de site e serviço.</span><span class="sxs-lookup"><span data-stu-id="f073b-160">Port number to use for website and service communication.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="f073b-161">Observação</span><span class="sxs-lookup"><span data-stu-id="f073b-161">Note</span></span></strong><br/><p><span data-ttu-id="f073b-162">Você deve definir uma exceção de firewall para permitir a comunicação por meio da porta especificada.</span><span class="sxs-lookup"><span data-stu-id="f073b-162">You must set a firewall exception to enable communication through the specified port.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f073b-163">Conta e senha de domínio do pool de aplicativos do serviço Web</span><span class="sxs-lookup"><span data-stu-id="f073b-163">Web service application pool domain account and password</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f073b-164">Conta de usuário do domínio e senha para o pool de aplicativos de serviço Web.</span><span class="sxs-lookup"><span data-stu-id="f073b-164">Domain user account and password for the web service application pool.</span></span></p>
   <p><span data-ttu-id="f073b-165">Se você inserir um nome de usuário no <strong> campo usuário ou grupo do domínio de acesso de leitura/gravação </strong> na <strong> página configurar bancos de dados </strong> , você deverá digitar esse mesmo valor neste campo.</span><span class="sxs-lookup"><span data-stu-id="f073b-165">If you enter a user name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, you must enter that same value in this field.</span></span></p>
   <p><span data-ttu-id="f073b-166">Se você inserir um nome de grupo no <strong> campo usuário ou grupo do domínio de acesso de leitura/gravação </strong> na <strong> página configurar bancos de dados </strong> , o valor que você inserir nesse campo deverá ser um membro desse grupo.</span><span class="sxs-lookup"><span data-stu-id="f073b-166">If you enter a group name in the <strong>Read/write access domain user or group</strong> field on the <strong>Configure Databases</strong> page, the value you enter in this field must be a member of that group.</span></span></p>
   <p><span data-ttu-id="f073b-167">Se você não especificar credenciais, as credenciais que foram especificadas para qualquer aplicativo da Web habilitado anteriormente serão usadas.</span><span class="sxs-lookup"><span data-stu-id="f073b-167">If you do not specify credentials, the credentials that were specified for any previously enabled web application will be used.</span></span> <span data-ttu-id="f073b-168">Todos os aplicativos Web devem usar as mesmas credenciais de pool de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f073b-168">All web applications must use the same application pool credentials.</span></span> <span data-ttu-id="f073b-169">Se você especificar credenciais diferentes para diferentes aplicativos da Web, o valor especificado mais recentemente será usado.</span><span class="sxs-lookup"><span data-stu-id="f073b-169">If you specify different credentials for different web applications, the most recently specified value will be used.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="f073b-170">Importante</span><span class="sxs-lookup"><span data-stu-id="f073b-170">Important</span></span></strong><br/><p><span data-ttu-id="f073b-171">Para aumentar a segurança, defina a conta especificada nas credenciais para ter direitos de usuário limitados.</span><span class="sxs-lookup"><span data-stu-id="f073b-171">For improved security, set the account that is specified in the credentials to have limited user rights.</span></span> <span data-ttu-id="f073b-172">Além disso, defina a senha da conta para nunca expirar.</span><span class="sxs-lookup"><span data-stu-id="f073b-172">Also, set the password of the account to never expire.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



5. <span data-ttu-id="f073b-173">Verifique se a conta interna do IIS \ _IUSRS ou a conta do pool de aplicativos foi adicionada às configurações de segurança local de **um cliente após autenticação** e **logon como um trabalho em lotes** .</span><span class="sxs-lookup"><span data-stu-id="f073b-173">Verify that the built-in IIS\_IUSRS account or the application pool account has been added to the **Impersonate a client after authentication** and the **Log on as a batch job** local security settings.</span></span>

   <span data-ttu-id="f073b-174">Para verificar se ela foi adicionada às configurações de segurança locais, abra o **Editor de política de segurança local**, expanda o nó **políticas locais** , clique no nó **atribuição de direitos de usuário** e clique duas vezes em **representar um cliente após autenticação** e **faça logon como uma** política de trabalho em lotes no painel direito.</span><span class="sxs-lookup"><span data-stu-id="f073b-174">To check whether it has been added to the local security settings, open the **Local Security Policy editor**, expand the **Local Policies** node, click the **User Rights Assignment** node, and double-click **Impersonate a client after authentication** and **Log on as a batch job** policies in the right pane.</span></span>

**<span data-ttu-id="f073b-175">Para configurar informações de conexão para bancos de dados usando o assistente</span><span class="sxs-lookup"><span data-stu-id="f073b-175">To configure connection information for the databases by using the wizard</span></span>**

1.  <span data-ttu-id="f073b-176">Use as descrições de campo a seguir para configurar as informações de conexão no Assistente para o banco de dados de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="f073b-176">Use the following field descriptions to configure the connection information in the wizard for the Compliance and Audit Database.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="f073b-177">Campo</span><span class="sxs-lookup"><span data-stu-id="f073b-177">Field</span></span></th>
    <th align="left"><span data-ttu-id="f073b-178">Descrição</span><span class="sxs-lookup"><span data-stu-id="f073b-178">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="f073b-179">Nome do SQL Server</span><span class="sxs-lookup"><span data-stu-id="f073b-179">SQL Server name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="f073b-180">Nome do servidor em que o banco de dados de conformidade e auditoria está configurado.</span><span class="sxs-lookup"><span data-stu-id="f073b-180">Name of the server where the Compliance and Audit Database is configured.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="f073b-181">Instância de banco de dados do SQL Server</span><span class="sxs-lookup"><span data-stu-id="f073b-181">SQL Server database instance</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="f073b-182">Nome da instância do SQL Server na qual o banco de dados de conformidade e auditoria está configurado.</span><span class="sxs-lookup"><span data-stu-id="f073b-182">SQL Server instance name where the Compliance and Audit Database is configured.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="f073b-183">Nome do banco de dados</span><span class="sxs-lookup"><span data-stu-id="f073b-183">Database name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="f073b-184">Nome do banco de dados de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="f073b-184">Name of the Compliance and Audit Database.</span></span></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="f073b-185">Use as descrições de campo a seguir para configurar as informações de conexão no assistente do banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="f073b-185">Use the following field descriptions to configure the connection information in the wizard for the Recovery Database.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="f073b-186">Campo</span><span class="sxs-lookup"><span data-stu-id="f073b-186">Field</span></span></th>
    <th align="left"><span data-ttu-id="f073b-187">Descrição</span><span class="sxs-lookup"><span data-stu-id="f073b-187">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="f073b-188">Nome do SQL Server</span><span class="sxs-lookup"><span data-stu-id="f073b-188">SQL Server name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="f073b-189">Nome do servidor em que o banco de dados de recuperação está configurado.</span><span class="sxs-lookup"><span data-stu-id="f073b-189">Name of the server where the Recovery Database is configured.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="f073b-190">Instância de banco de dados do SQL Server</span><span class="sxs-lookup"><span data-stu-id="f073b-190">SQL Server database instance</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="f073b-191">Nome da instância do SQL Server na qual o banco de dados de recuperação está configurado.</span><span class="sxs-lookup"><span data-stu-id="f073b-191">SQL Server instance name where the Recovery Database is configured.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="f073b-192">Nome do banco de dados</span><span class="sxs-lookup"><span data-stu-id="f073b-192">Database name</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="f073b-193">Nome do banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="f073b-193">Name of the Recovery Database.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="f073b-194">Para configurar os aplicativos Web usando o assistente</span><span class="sxs-lookup"><span data-stu-id="f073b-194">To configure the web applications by using the wizard</span></span>**

1. <span data-ttu-id="f073b-195">Use as descrições a seguir para inserir os valores de campo no Assistente para configurar o site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="f073b-195">Use the following descriptions to enter the field values in the wizard to configure the Administration and Monitoring Website.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f073b-196">Campo</span><span class="sxs-lookup"><span data-stu-id="f073b-196">Field</span></span></th>
   <th align="left"><span data-ttu-id="f073b-197">Descrição</span><span class="sxs-lookup"><span data-stu-id="f073b-197">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f073b-198">Grupo de domínio da função helpdesk avançado</span><span class="sxs-lookup"><span data-stu-id="f073b-198">Advanced Helpdesk role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f073b-199">Grupo de usuários do domínio cujos membros têm acesso a todas as áreas do site Administração e monitoramento, exceto a área relatórios.</span><span class="sxs-lookup"><span data-stu-id="f073b-199">Domain user group whose members have access to all areas of the Administration and Monitoring Website except the Reports area.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="f073b-200">Grupo de domínio da função helpdesk</span><span class="sxs-lookup"><span data-stu-id="f073b-200">Helpdesk role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f073b-201">Grupo de usuários do domínio cujos membros têm acesso às <strong> áreas gerenciar TPM </strong> e <strong> unidade </strong> de recuperação do site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="f073b-201">Domain user group whose members have access to the <strong>Manage TPM</strong> and <strong>Drive Recovery</strong> areas of the Administration and Monitoring Website.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f073b-202">Usar a integração do System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f073b-202">Use System Center Configuration Manager Integration</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f073b-203">Marque esta caixa de seleção se você estiver configurando o MBAM com a topologia de integração do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f073b-203">Select this check box if you are configuring MBAM with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="f073b-204">Marcar essa caixa de seleção faz com que todos os relatórios, exceto o relatório de auditoria de recuperação, sejam exibidos no Configuration Manager em vez de no site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="f073b-204">Selecting this check box makes all reports, except the Recovery Audit report, appear in Configuration Manager instead of in the Administration and Monitoring Website.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="f073b-205">Grupo de domínio da função de relatório</span><span class="sxs-lookup"><span data-stu-id="f073b-205">Reporting role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f073b-206">Grupo de usuários do domínio cujos membros têm acesso somente leitura à área relatórios do site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="f073b-206">Domain user group whose members have read-only access to the Reports area of the Administration and Monitoring Website.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f073b-207">URL do SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="f073b-207">SQL Server Reporting Services URL</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f073b-208">URL para o servidor SSRS em que os relatórios do MBAM são configurados.</span><span class="sxs-lookup"><span data-stu-id="f073b-208">URL for the SSRS server where the MBAM Reports are configured.</span></span></p>
   <p><span data-ttu-id="f073b-209">Exemplos de URLs de relatório:</span><span class="sxs-lookup"><span data-stu-id="f073b-209">Examples of report URLs:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f073b-210">Tipo de nome do host</span><span class="sxs-lookup"><span data-stu-id="f073b-210">Type of host name</span></span></th>
   <th align="left"><span data-ttu-id="f073b-211">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f073b-211">Example</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f073b-212">Exemplo com um nome de domínio totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="f073b-212">Example with a fully qualified domain name</span></span></p></td>
   <td align="left"><p><a href="https://MyReportServer.Contoso.com/ReportServer" data-raw-source="https://MyReportServer.Contoso.com/ReportServer">https://MyReportServer.Contoso.com/ReportServer</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f073b-213">Exemplo com um nome de host personalizado</span><span class="sxs-lookup"><span data-stu-id="f073b-213">Example with a custom host name</span></span></p></td>
   <td align="left"><p><a href="https://MyReportServer/ReportServer" data-raw-source="https://MyReportServer/ReportServer">https://MyReportServer/ReportServer</a></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="f073b-214">Diretório virtual</span><span class="sxs-lookup"><span data-stu-id="f073b-214">Virtual directory</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f073b-215">Diretório virtual do site Administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="f073b-215">Virtual directory of the Administration and Monitoring Website.</span></span> <span data-ttu-id="f073b-216">Esse nome corresponde ao diretório físico do site no servidor e é acrescentado ao nome do host do site, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f073b-216">This name corresponds to the website’s physical directory on the server and is appended to the website’s host name, for example:</span></span></p>
   <p><span data-ttu-id="f073b-217">http (s):// &lt; <em> nome do host </em> &gt; : &lt; <em> porta </em> &gt; /helpdesk/</span><span class="sxs-lookup"><span data-stu-id="f073b-217">http(s)://&lt;<em>hostname</em>&gt;:&lt;<em>port</em>&gt;/HelpDesk/</span></span></p>
   <p><span data-ttu-id="f073b-218">Se você não especificar um diretório virtual, o valor da <strong> assistência técnica </strong> será usado.</span><span class="sxs-lookup"><span data-stu-id="f073b-218">If you do not specify a virtual directory, the value <strong>HelpDesk</strong> will be used.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f073b-219">Grupo de domínio da função </strong> de migração de dados (opcional)</span><span class="sxs-lookup"><span data-stu-id="f073b-219">Data Migration role domain group</strong> (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f073b-220">Grupo de usuários do domínio cujos membros têm acesso para usar os cmdlets Write-MBAM \* para gravar informações de recuperação via este ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f073b-220">Domain user group whose members have access to use the Write-Mbam\*Information Cmdlets to write recovery information via this endpoint.</span></span></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="f073b-221">Use a seguinte descrição para inserir os valores de campo no Assistente para configurar o portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="f073b-221">Use the following description to enter the field values in the wizard to configure the Self-Service Portal.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="f073b-222">Campo</span><span class="sxs-lookup"><span data-stu-id="f073b-222">Field</span></span></th>
   <th align="left"><span data-ttu-id="f073b-223">Descrição</span><span class="sxs-lookup"><span data-stu-id="f073b-223">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="f073b-224">Diretório virtual</span><span class="sxs-lookup"><span data-stu-id="f073b-224">Virtual directory</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="f073b-225">Diretório virtual do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="f073b-225">Virtual directory of the web application.</span></span> <span data-ttu-id="f073b-226">Esse nome corresponde ao diretório físico do site no servidor e é acrescentado ao nome do host do site, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f073b-226">This name corresponds to the website’s physical directory on the server, and is appended to the website’s host name, for example:</span></span></p>
   <p><span data-ttu-id="f073b-227">http (s):// &lt; <em> nome do host </em> &gt; : &lt; <em> porta </em> &gt; /SelfService/</span><span class="sxs-lookup"><span data-stu-id="f073b-227">http(s)://&lt;<em>hostname</em>&gt;:&lt;<em>port</em>&gt;/SelfService/</span></span></p>
   <p><span data-ttu-id="f073b-228">Se você não especificar um diretório virtual, o valor <strong> SelfService </strong> será usado.</span><span class="sxs-lookup"><span data-stu-id="f073b-228">If you do not specify a virtual directory, the value <strong>SelfService</strong> will be used.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f073b-229">Nome da empresa</span><span class="sxs-lookup"><span data-stu-id="f073b-229">Company name</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f073b-230">Especifique um nome de empresa para o portal de autoatendimento, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f073b-230">Specify a company name for the Self-Service Portal, for example:</span></span></p>
   <p><span data-ttu-id="f073b-231">Contoso IT</span><span class="sxs-lookup"><span data-stu-id="f073b-231">Contoso IT</span></span></p>
   <p><span data-ttu-id="f073b-232">O nome da empresa é exibido por todos os usuários do portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="f073b-232">This company name is viewed by all Self-Service Portal users.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f073b-233">Texto da URL do helpdesk</span><span class="sxs-lookup"><span data-stu-id="f073b-233">Helpdesk URL text</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f073b-234">Especifique uma instrução de texto que direcione os usuários para o website do helpdesk da sua organização, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f073b-234">Specify a text statement that directs users to your organization's Helpdesk website, for example:</span></span></p>
   <p><span data-ttu-id="f073b-235">Assistência técnica ou departamento de ti do contato</span><span class="sxs-lookup"><span data-stu-id="f073b-235">Contact Helpdesk or IT department</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f073b-236">URL do helpdesk</span><span class="sxs-lookup"><span data-stu-id="f073b-236">Helpdesk URL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f073b-237">Especifique a URL do site do helpdesk da sua organização, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f073b-237">Specify the URL for your organization's Helpdesk website, for example:</span></span></p>
   <p><span data-ttu-id="f073b-238">http (s):// &lt; <em> companyHelpdeskURL</em>&gt;/</span><span class="sxs-lookup"><span data-stu-id="f073b-238">http(s)://&lt;<em>companyHelpdeskURL</em>&gt;/</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="f073b-239">Aviso de arquivo de texto</span><span class="sxs-lookup"><span data-stu-id="f073b-239">Notice text file</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f073b-240">Selecione um arquivo que contenha o aviso que você deseja que seja exibido aos usuários na página inicial do portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="f073b-240">Select a file that contains the notice you want displayed to users on the Self-Service Portal landing page.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="f073b-241">Não exibir texto de aviso para usuários</span><span class="sxs-lookup"><span data-stu-id="f073b-241">Do not display notice text to users</span></span></p></td>
   <td align="left"><p><span data-ttu-id="f073b-242">Marque esta caixa de seleção para especificar que o texto de aviso não será exibido para os usuários.</span><span class="sxs-lookup"><span data-stu-id="f073b-242">Select this check box to specify that the notice text is not displayed to users.</span></span></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="f073b-243">Quando terminar as entradas, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="f073b-243">When you finish your entries, click **Next**.</span></span>

   <span data-ttu-id="f073b-244">O assistente verifica se todos os pré-requisitos para os aplicativos da Web foram atendidos.</span><span class="sxs-lookup"><span data-stu-id="f073b-244">The wizard checks that all prerequisites for the web applications have been met.</span></span>

4. <span data-ttu-id="f073b-245">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="f073b-245">Click **Next** to continue.</span></span>

5. <span data-ttu-id="f073b-246">Na página **Resumo** , examine os recursos que serão adicionados.</span><span class="sxs-lookup"><span data-stu-id="f073b-246">On the **Summary** page, review the features that will be added.</span></span>

   **<span data-ttu-id="f073b-247">Observação</span><span class="sxs-lookup"><span data-stu-id="f073b-247">Note</span></span>**  
   <span data-ttu-id="f073b-248">Para criar um script do Windows PowerShell para as entradas feitas, clique em **Exportar script do PowerShell** e salve o script.</span><span class="sxs-lookup"><span data-stu-id="f073b-248">To create a Windows PowerShell script for the entries you made, click **Export PowerShell Script** and save the script.</span></span>



6. <span data-ttu-id="f073b-249">Clique em **Adicionar** para adicionar os aplicativos Web ao servidor e, em seguida, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="f073b-249">Click **Add** to add the web applications to the server, and then click **Close**.</span></span>

   <span data-ttu-id="f073b-250">Para personalizar o portal de autoatendimento adicionando texto de aviso personalizado, o nome da sua empresa, os ponteiros para obter mais informações e assim por diante, consulte [Personalizando o portal de autoatendimento da sua organização](customizing-the-self-service-portal-for-your-organization.md).</span><span class="sxs-lookup"><span data-stu-id="f073b-250">To customize the Self-Service Portal by adding custom notice text, your company name, pointers to more information, and so on, see [Customizing the Self-Service Portal for Your Organization](customizing-the-self-service-portal-for-your-organization.md).</span></span>

**<span data-ttu-id="f073b-251">Para configurar o portal de autoatendimento se os computadores cliente não puderem acessar a CDN</span><span class="sxs-lookup"><span data-stu-id="f073b-251">To configure the Self-Service Portal if client computers cannot access the CDN</span></span>**

1.  <span data-ttu-id="f073b-252">Determine se você está executando o Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="f073b-252">Determine whether you are running Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1.</span></span> <span data-ttu-id="f073b-253">Em caso afirmativo, não faça nada.</span><span class="sxs-lookup"><span data-stu-id="f073b-253">If so, do nothing.</span></span> <span data-ttu-id="f073b-254">Sua configuração do portal de autoatendimento está completa.</span><span class="sxs-lookup"><span data-stu-id="f073b-254">Your Self-Service Portal configuration is complete.</span></span>

    **<span data-ttu-id="f073b-255">Observação</span><span class="sxs-lookup"><span data-stu-id="f073b-255">Note</span></span>**  
    <span data-ttu-id="f073b-256">O monitoramento e administração do Microsoft BitLocker (MBAM) 2,5 SP1 instala os arquivos JavaScript na configuração e, portanto, não precisa estar conectado à rede de entrega de conteúdo do Microsoft Ajax para configurar o portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="f073b-256">Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 installs the JavaScript files in setup, and so does not need to be connected to the Microsoft Ajax Content Delivery Network in order to configure the Self-Service Portal.</span></span> <span data-ttu-id="f073b-257">As etapas a seguir serão necessárias somente se você estiver usando uma versão do Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 anterior ao SP1.</span><span class="sxs-lookup"><span data-stu-id="f073b-257">The following steps are necessary only if you are using a version of Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 previous to SP1.</span></span>



2.  <span data-ttu-id="f073b-258">Determine se seus computadores cliente têm acesso à rede de distribuição de conteúdo (CDN) do Microsoft Ajax.</span><span class="sxs-lookup"><span data-stu-id="f073b-258">Determine if your client computers have access to the Microsoft Ajax Content Delivery Network (CDN).</span></span>

    <span data-ttu-id="f073b-259">A CDN oferece ao portal de autoatendimento o acesso necessário a certos arquivos JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f073b-259">The CDN gives the Self-Service Portal the access it requires to certain JavaScript files.</span></span> <span data-ttu-id="f073b-260">Se você não configurar o portal de autoatendimento quando os computadores cliente não puderem acessar a CDN, apenas o nome da empresa e a conta sob a qual o usuário final se conectou serão exibidos.</span><span class="sxs-lookup"><span data-stu-id="f073b-260">If you don’t configure the Self-Service Portal when client computers cannot access the CDN, only the company name and the account under which the end user signed in will be displayed.</span></span> <span data-ttu-id="f073b-261">Nenhuma mensagem de erro será mostrada.</span><span class="sxs-lookup"><span data-stu-id="f073b-261">No error message will be shown.</span></span>

3.  <span data-ttu-id="f073b-262">Siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="f073b-262">Do one of the following:</span></span>

    -   <span data-ttu-id="f073b-263">Se seus computadores cliente tiverem acesso à CDN, não faça nada.</span><span class="sxs-lookup"><span data-stu-id="f073b-263">If your client computers have access to the CDN, do nothing.</span></span> <span data-ttu-id="f073b-264">Sua configuração do portal de autoatendimento está completa.</span><span class="sxs-lookup"><span data-stu-id="f073b-264">Your Self-Service Portal configuration is complete.</span></span>

    -   <span data-ttu-id="f073b-265">Se seus computadores cliente não tiverem acesso à CDN, conclua as etapas em [como configurar o portal de autoatendimento quando os computadores cliente não puderem acessar a rede de distribuição de conteúdo da Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span><span class="sxs-lookup"><span data-stu-id="f073b-265">If your client computers do not have access to the CDN, complete the steps in [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span></span>


## <span data-ttu-id="f073b-266">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f073b-266">Related topics</span></span>


[<span data-ttu-id="f073b-267">Logs de eventos do servidor</span><span class="sxs-lookup"><span data-stu-id="f073b-267">Server Event Logs</span></span>](server-event-logs.md)

[<span data-ttu-id="f073b-268">Configurando os recursos de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f073b-268">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="f073b-269">Como configurar o Portal de Autoatendimento quando os computadores cliente não puderem acessar a Rede de Distribuição de Conteúdo da Microsoft</span><span class="sxs-lookup"><span data-stu-id="f073b-269">How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network</span></span>](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md)

[<span data-ttu-id="f073b-270">Personalizando o Portal de Autoatendimento para sua organização</span><span class="sxs-lookup"><span data-stu-id="f073b-270">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

[<span data-ttu-id="f073b-271">Validando a configuração de recursos de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f073b-271">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)



## <span data-ttu-id="f073b-272">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="f073b-272">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="f073b-273">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="f073b-273">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="f073b-274">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="f073b-274">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





