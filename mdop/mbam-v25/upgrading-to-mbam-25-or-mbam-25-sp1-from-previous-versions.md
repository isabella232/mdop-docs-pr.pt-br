---
title: Atualizando para o MBAM 2.5 ou MBAM 2.5 SP1 de versões anteriores
description: Atualizando para o MBAM 2.5 ou MBAM 2.5 SP1 de versões anteriores
author: dansimp
ms.assetid: a9edb4b8-5d5e-42ab-8db6-619db2878e50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 07a03ebbbfce45f7f69a85000e18ddf1a58e53ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796078"
---
# <span data-ttu-id="70ff1-103">Atualizando para o MBAM 2.5 ou MBAM 2.5 SP1 de versões anteriores</span><span class="sxs-lookup"><span data-stu-id="70ff1-103">Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions</span></span>


<span data-ttu-id="70ff1-104">Este tópico descreve o processo de atualização do servidor do Microsoft BitLocker Administration and Monitoring (MBAM) e do cliente MBAM de versões anteriores do MBAM.</span><span class="sxs-lookup"><span data-stu-id="70ff1-104">This topic describes the process for upgrading the Microsoft BitLocker Administration and Monitoring (MBAM) Server and the MBAM Client from earlier versions of MBAM.</span></span>

<span data-ttu-id="70ff1-105">**Observação**  Você pode atualizar diretamente para o MBAM 2,5 ou o MBAM 2,5 SP1 a partir de qualquer versão anterior do MBAM.</span><span class="sxs-lookup"><span data-stu-id="70ff1-105">**Note** You can upgrade directly to MBAM 2.5 or MBAM 2.5 SP1 from any previous version of MBAM.</span></span>

 

## <span data-ttu-id="70ff1-106">Antes de iniciar a atualização</span><span class="sxs-lookup"><span data-stu-id="70ff1-106">Before you start the upgrade</span></span>


<span data-ttu-id="70ff1-107">Revise as informações a seguir antes de iniciar a atualização.</span><span class="sxs-lookup"><span data-stu-id="70ff1-107">Review the following information before you start the upgrade.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="70ff1-108">O que saber antes de começar</span><span class="sxs-lookup"><span data-stu-id="70ff1-108">What to know before you start</span></span></th>
<th align="left"><span data-ttu-id="70ff1-109">Detalhes</span><span class="sxs-lookup"><span data-stu-id="70ff1-109">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="70ff1-110">Se você estiver instalando os sites do MBAM em um servidor e os serviços Web em outro servidor, será necessário usar cmdlets do Windows PowerShell para configurá-los.</span><span class="sxs-lookup"><span data-stu-id="70ff1-110">If you are installing the MBAM websites on one server and the web services on another server, you have to use Windows PowerShell cmdlets to configure them.</span></span></p></td>
<td align="left"><p><span data-ttu-id="70ff1-111">O assistente de configuração do servidor do MBAM não dá suporte à configuração dos sites em um servidor e nos serviços Web em um servidor diferente.</span><span class="sxs-lookup"><span data-stu-id="70ff1-111">The MBAM Server Configuration wizard does not support configuring the websites on one server and the web services on a different server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="70ff1-112">Se você estiver atualizando para o MBAM 2.5 ou o 2,5 SP1 do MBAM 2.0 ou do 2,0 SP1 no Windows Server2008 R2:</span><span class="sxs-lookup"><span data-stu-id="70ff1-112">If you are upgrading to MBAM2.5 or 2.5 SP1 from MBAM2.0 or 2.0 SP1 in Windows Server2008 R2:</span></span></p>
<p><span data-ttu-id="70ff1-113">O site de administração e monitoramento e o portal de autoatendimento não funcionarão se você instalar o software .NET Framework 4.5 necessário após a instalação dos serviços de informações da Internet (IIS).</span><span class="sxs-lookup"><span data-stu-id="70ff1-113">The Administration and Monitoring Website and the Self-Service Portal will not work if you install the required .NET Framework4.5 software after Internet Information Services (IIS) is already installed.</span></span></p>
<p><span data-ttu-id="70ff1-114">Esse problema ocorre porque o ASP.NET não pode ser registrado corretamente com o IIS se o .NET Framework estiver instalado depois que o IIS já estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="70ff1-114">This issue occurs because ASP.NET cannot be registered correctly with IIS if the .NET Framework is installed after IIS has already been installed.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="70ff1-115">Para resolver este problema:</span><span class="sxs-lookup"><span data-stu-id="70ff1-115">To resolve this issue:</span></span></strong></p>
<p><span data-ttu-id="70ff1-116">Execute <strong> aspnet_regiis – i </strong> do seguinte local:</span><span class="sxs-lookup"><span data-stu-id="70ff1-116">Run <strong>aspnet_regiis –i</strong> from the following location:</span></span></p>
<p><span data-ttu-id="70ff1-117">C:\windows\microsoft.net\Framework\v4.0.30319</span><span class="sxs-lookup"><span data-stu-id="70ff1-117">C:\windows\microsoft.net\Framework\v4.0.30319</span></span></p>
<p><span data-ttu-id="70ff1-118">Para obter mais informações, consulte: <a href="https://go.microsoft.com/fwlink/?LinkId=393272" data-raw-source="[ASP.NET IIS Registration Tool](https://go.microsoft.com/fwlink/?LinkId=393272)"> ASP.net a ferramenta de registro do IIS </a> .</span><span class="sxs-lookup"><span data-stu-id="70ff1-118">For more information, see: <a href="https://go.microsoft.com/fwlink/?LinkId=393272" data-raw-source="[ASP.NET IIS Registration Tool](https://go.microsoft.com/fwlink/?LinkId=393272)">ASP.NET IIS Registration Tool</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="70ff1-119">Registre um SPN na conta do pool de aplicativos se todas as seguintes opções forem verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="70ff1-119">Register an SPN on the application pool account if all of the following are true:</span></span></p>
<ul>
<li><p><span data-ttu-id="70ff1-120">Você estiver atualizando de uma versão anterior do MBAM.</span><span class="sxs-lookup"><span data-stu-id="70ff1-120">You are upgrading from a previous version of MBAM.</span></span></p></li>
<li><p><span data-ttu-id="70ff1-121">Atualmente, você não está executando os sites do MBAM em uma configuração de carga balanceada ou distribuída, mas quer fazer isso quando atualizar para o MBAM 2.5 ou 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="70ff1-121">Currently, you are not running the MBAM websites in a load-balanced or distributed configuration, but you would like to do so when you upgrade to MBAM2.5 or 2.5 SP1.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="70ff1-122">Para obter instruções, consulte <a href="planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn)"> planejando como proteger os sites do MBAM </a> .</span><span class="sxs-lookup"><span data-stu-id="70ff1-122">For instructions, see <a href="planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn)">Planning How to Secure the MBAM Websites</a>.</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="70ff1-123">O que recomendamos</span><span class="sxs-lookup"><span data-stu-id="70ff1-123">What we recommend</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="70ff1-124">Registre um SPN (nome da entidade de serviço) para a conta do pool de aplicativos, mesmo que você já tenha registrado SPNs para a conta do computador.</span><span class="sxs-lookup"><span data-stu-id="70ff1-124">Register a service principal name (SPN) for the application pool account, even though you may already have registered SPNs for the machine account.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="70ff1-125">Por que recomendamos</span><span class="sxs-lookup"><span data-stu-id="70ff1-125">Why we recommend it</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="70ff1-126">O registro de um SPN na conta do pool de aplicativos é necessário para configurar os sites em uma configuração balanceada ou de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="70ff1-126">Registering an SPN on the application pool account is required to configure the websites in a load-balanced or distributed configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="70ff1-127">O que acontece se os SPNs já estiverem configurados em uma conta de máquina?</span><span class="sxs-lookup"><span data-stu-id="70ff1-127">What happens if SPNs are already configured on a machine account?</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="70ff1-128">O MBAM usará os SPNs que você já registrou e não precisará configurar SPNs adicionais, mas não é possível configurar os websites em uma configuração balanceada ou distribuída.</span><span class="sxs-lookup"><span data-stu-id="70ff1-128">MBAM will use the SPNs that you have already registered, and you don’t need to configure additional SPNs, but you are not able to configure the websites in a load-balanced or distributed configuration.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="70ff1-129">Etapas para atualizar a infraestrutura do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="70ff1-129">Steps to upgrade the MBAM Server infrastructure</span></span>


<span data-ttu-id="70ff1-130">Use as etapas das seções a seguir para atualizar o MBAM para a topologia autônoma ou a topologia de integração do System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="70ff1-130">Use the steps in the following sections to upgrade MBAM for the Stand-alone topology or the System Center Configuration Manager Integration topology.</span></span>

**<span data-ttu-id="70ff1-131">Para atualizar a infraestrutura do MBAM Server para topologia autônoma</span><span class="sxs-lookup"><span data-stu-id="70ff1-131">To upgrade the MBAM Server infrastructure for Stand-alone topology</span></span>**

1.  <span data-ttu-id="70ff1-132">Desinstale as versões anteriores do MBAM em **programas e recursos** e em servidores Web para garantir que as informações não sejam gravadas de clientes do MBAM na infraestrutura MBAM.</span><span class="sxs-lookup"><span data-stu-id="70ff1-132">Uninstall previous versions of MBAM from **Programs and Features** and from web servers to make sure that information is not being written from MBAM clients to the MBAM infrastructure.</span></span> <span data-ttu-id="70ff1-133">Para obter instruções, consulte [removendo recursos ou software do MBAM Server](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span><span class="sxs-lookup"><span data-stu-id="70ff1-133">For instructions, see [Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span></span>

2.  <span data-ttu-id="70ff1-134">Faça backup de seus bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="70ff1-134">Back up your databases.</span></span>

3.  <span data-ttu-id="70ff1-135">Desinstale as versões anteriores do MBAM a partir do SQL Server usando **programas e recursos**, incluindo SQL Servers que hospedam os relatórios do MBAM por meio do SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="70ff1-135">Uninstall previous versions of MBAM from SQL Server by using **Programs and Features**, including SQL Servers hosting the MBAM reports via SQL Server Reporting Services.</span></span> <span data-ttu-id="70ff1-136">Remova todas as pastas ou arquivos temporários restantes do servidor do MBAM do servidor de banco de dados e do Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="70ff1-136">Remove any remaining MBAM server temporary files or folders from the database server and reporting services.</span></span>

    <span data-ttu-id="70ff1-137">**Observação**  Os bancos de dados não serão removidos, e todos os dados de conformidade e recuperação serão mantidos no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="70ff1-137">**Note** The databases will not be removed, and all compliance and recovery data is maintained in the database.</span></span>

     

4.  <span data-ttu-id="70ff1-138">Instale e configure os bancos de dados, relatórios e aplicativos Web do MBAM 2.5 ou do 2,5 SP1, nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="70ff1-138">Install and configure the MBAM2.5 or 2.5 SP1 databases, reports, and web applications, in that order.</span></span> <span data-ttu-id="70ff1-139">Os bancos de dados estão atualizados no local.</span><span class="sxs-lookup"><span data-stu-id="70ff1-139">The databases are upgraded in place.</span></span>

5.  <span data-ttu-id="70ff1-140">Atualize os objetos de política de grupo (GPOs) usando os modelos do MBAM 2,5 para aproveitar os novos recursos do MBAM, como a criptografia imposta.</span><span class="sxs-lookup"><span data-stu-id="70ff1-140">Update the Group Policy Objects (GPOs) using the MBAM 2.5 Templates to leverage the new features in MBAM, such as enforced encryption.</span></span> <span data-ttu-id="70ff1-141">Se você não atualizar os GPOs e o cliente do MBAM para o MBAM 2,5, as versões anteriores dos clientes MBAM continuarão a se comunicar com seus GPOs atuais com funcionalidade reduzida.</span><span class="sxs-lookup"><span data-stu-id="70ff1-141">If you do not update the GPOs and the MBAM client to MBAM 2.5, earlier versions of MBAM clients will continue to report against your current GPOs with reduced functionality.</span></span> <span data-ttu-id="70ff1-142">Veja [como obter modelos de política de grupo do MDOP (. admx)](https://www.microsoft.com/download/details.aspx?id=41183) para baixar os modelos ADMX mais recentes.</span><span class="sxs-lookup"><span data-stu-id="70ff1-142">See [How to Get MDOP Group Policy (.admx) Templates](https://www.microsoft.com/download/details.aspx?id=41183) to download the latest ADMX templates.</span></span>

    <span data-ttu-id="70ff1-143">Depois de atualizar a infraestrutura do MBAM Server, os computadores cliente existentes continuam a ser reportados com êxito para o servidor MBAM 2.5 ou 2,5 SP1, e os dados de recuperação continuam a ser armazenados.</span><span class="sxs-lookup"><span data-stu-id="70ff1-143">After you upgrade the MBAM Server infrastructure, the existing client computers continue to successfully report to the MBAM2.5 or 2.5 SP1 Server, and recovery data continues to be stored.</span></span>

6.  <span data-ttu-id="70ff1-144">Instale o cliente mais recente do MBAM 2.5 ou do 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="70ff1-144">Install the latest MBAM2.5 or 2.5 SP1 Client.</span></span> <span data-ttu-id="70ff1-145">Os computadores cliente não precisam ser reiniciados após a implantação.</span><span class="sxs-lookup"><span data-stu-id="70ff1-145">Client computers do not need to be rebooted after the deployment.</span></span>

**<span data-ttu-id="70ff1-146">Para atualizar a infraestrutura do MBAM para a topologia de integração do System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="70ff1-146">To upgrade the MBAM infrastructure for System Center Configuration Manager Integration topology</span></span>**

1.  <span data-ttu-id="70ff1-147">Desinstale as versões anteriores do MBAM em **programas e recursos** e em servidores Web para garantir que as informações não sejam gravadas de clientes do MBAM na infraestrutura MBAM.</span><span class="sxs-lookup"><span data-stu-id="70ff1-147">Uninstall previous versions of MBAM from **Programs and Features** and from web servers to make sure that information is not being written from MBAM clients to the MBAM infrastructure.</span></span> <span data-ttu-id="70ff1-148">Para obter instruções, consulte [removendo recursos ou software do MBAM Server](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span><span class="sxs-lookup"><span data-stu-id="70ff1-148">For instructions, see [Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).</span></span>

2.  <span data-ttu-id="70ff1-149">Faça backup de seus bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="70ff1-149">Back up your databases.</span></span>

3.  <span data-ttu-id="70ff1-150">Desinstale as versões anteriores do MBAM a partir do SQL Server usando **programas e recursos**, incluindo SQL Servers que hospedam os relatórios do MBAM por meio do SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="70ff1-150">Uninstall previous versions of MBAM from SQL Server by using **Programs and Features**, including SQL Servers hosting the MBAM reports via SQL Server Reporting Services.</span></span> <span data-ttu-id="70ff1-151">Remova todas as pastas ou arquivos temporários restantes do servidor do MBAM do servidor de banco de dados e do Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="70ff1-151">Remove any remaining MBAM server temporary files or folders from the database server and reporting services.</span></span>

4.  <span data-ttu-id="70ff1-152">Desinstale o MBAM do servidor do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="70ff1-152">Uninstall MBAM from the Configuration Manager server.</span></span>

    <span data-ttu-id="70ff1-153">**Observação**  Os bancos de dados e os objetos do Configuration Manager (linha de base, coleção de computadores com suporte MBAM e relatórios) não serão removidos, e todos os dados de conformidade e recuperação serão mantidos no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="70ff1-153">**Note** The databases and the Configuration Manager objects (baseline, MBAM supported computers collection, and Reports) will not be removed, and all compliance and recovery data is maintained in the database.</span></span>

     

5.  <span data-ttu-id="70ff1-154">Atualize os arquivos. mof.</span><span class="sxs-lookup"><span data-stu-id="70ff1-154">Update the .mof files.</span></span>

6.  <span data-ttu-id="70ff1-155">Instale e configure os bancos de dados do MBAM 2.5 ou do 2,5 SP1, relatórios, aplicativos Web e a integração do Configuration Manager nesta ordem.</span><span class="sxs-lookup"><span data-stu-id="70ff1-155">Install and configure the MBAM2.5 or 2.5 SP1 databases, reports, web applications, and Configuration Manager integration, in that order.</span></span> <span data-ttu-id="70ff1-156">Os objetos de bancos de dados e do Configuration Manager são atualizados em vigor.</span><span class="sxs-lookup"><span data-stu-id="70ff1-156">The databases and Configuration Manager objects are upgraded in place.</span></span>

7.  <span data-ttu-id="70ff1-157">Opcionalmente, atualize os objetos de política de grupo (GPOs) e edite as configurações se desejar implementar novos recursos no MBAM, como a criptografia imposta.</span><span class="sxs-lookup"><span data-stu-id="70ff1-157">Optionally, update the Group Policy Objects (GPOs), and edit the settings if you want to implement new features in MBAM, such as enforced encryption.</span></span> <span data-ttu-id="70ff1-158">Se você não atualizar os GPOs, o MBAM continuará a se comunicar com seus GPOs atuais.</span><span class="sxs-lookup"><span data-stu-id="70ff1-158">If you do not update the GPOs, MBAM will continue to report against your current GPOs.</span></span> <span data-ttu-id="70ff1-159">Veja [como obter modelos de política de grupo do MDOP (. admx)](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates) para baixar os modelos ADMX mais recentes.</span><span class="sxs-lookup"><span data-stu-id="70ff1-159">See [How to Get MDOP Group Policy (.admx) Templates](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates) to download the latest ADMX templates.</span></span>

    <span data-ttu-id="70ff1-160">Depois de atualizar a infraestrutura do MBAM Server, os computadores cliente existentes continuam a ser reportados com êxito para o servidor MBAM 2.5 ou 2,5 SP1, e os dados de recuperação continuam a ser armazenados.</span><span class="sxs-lookup"><span data-stu-id="70ff1-160">After you upgrade the MBAM Server infrastructure, the existing client computers continue to successfully report to the MBAM2.5 or 2.5 SP1 Server, and recovery data continues to be stored.</span></span>

8.  <span data-ttu-id="70ff1-161">Instale o cliente mais recente do MBAM 2.5 ou do 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="70ff1-161">Install the latest MBAM2.5 or 2.5 SP1 Client.</span></span> <span data-ttu-id="70ff1-162">Os computadores cliente não precisam ser reiniciados após a implantação.</span><span class="sxs-lookup"><span data-stu-id="70ff1-162">Client computers do not need to be rebooted after the deployment.</span></span>

## <span data-ttu-id="70ff1-163">Suporte de atualização para o cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="70ff1-163">Upgrade support for the MBAM Client</span></span>


<span data-ttu-id="70ff1-164">O MBAM dá suporte a atualizações para o cliente do MBAM 2.5 de qualquer versão anterior do cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="70ff1-164">MBAM supports upgrades to the MBAM2.5 Client from any earlier version of the MBAM Client.</span></span>

**<span data-ttu-id="70ff1-165">Maneiras de instalar o cliente MBAM:</span><span class="sxs-lookup"><span data-stu-id="70ff1-165">Ways to install the MBAM Client:</span></span>**

-   <span data-ttu-id="70ff1-166">Atualize os computadores que executam o cliente do MBAM de uma vez ou gradualmente após a instalação da infraestrutura de servidor do MBAM 2.5.</span><span class="sxs-lookup"><span data-stu-id="70ff1-166">Upgrade the computers running MBAM Client all at once or gradually after you install the MBAM2.5 Server infrastructure.</span></span>

-   <span data-ttu-id="70ff1-167">Instale o cliente do MBAM por meio de um sistema de distribuição de software eletrônico ou de ferramentas, como os serviços de domínio do Active Directory ou o System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="70ff1-167">Install the MBAM Client through an electronic software distribution system or through tools such as Active Directory Domain Services or System Center Configuration Manager.</span></span>



## <span data-ttu-id="70ff1-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70ff1-168">Related topics</span></span>


[<span data-ttu-id="70ff1-169">Implantando o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="70ff1-169">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

[<span data-ttu-id="70ff1-170">Implantando o cliente do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="70ff1-170">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

[<span data-ttu-id="70ff1-171">Configurando os recursos de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="70ff1-171">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

 

## <span data-ttu-id="70ff1-172">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="70ff1-172">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="70ff1-173">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="70ff1-173">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="70ff1-174">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="70ff1-174">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





