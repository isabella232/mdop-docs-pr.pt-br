---
title: Arquitetura de alto nível do MBAM 2.5 com topologia de integração do Configuration Manager
description: Arquitetura de alto nível do MBAM 2.5 com topologia de integração do Configuration Manager
author: dansimp
ms.assetid: 075bafa1-792b-4c24-9d8e-5d3153e2112c
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/23/2018
ms.author: dansimp
ms.openlocfilehash: 75af2e22981d76568916c36acadbbb25648b1f1d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799737"
---
# <span data-ttu-id="fdabc-103">Arquitetura de alto nível do MBAM 2,5 com a topologia de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="fdabc-103">High-level architecture of MBAM 2.5 with Configuration Manager Integration topology</span></span>

<span data-ttu-id="fdabc-104">Este tópico descreve a arquitetura recomendada para a implantação do Microsoft BitLocker Administration and Monitoring (MBAM) com a topologia de integração do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="fdabc-104">This topic describes the recommended architecture for deploying Microsoft BitLocker Administration and Monitoring (MBAM) with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="fdabc-105">Essa topologia integra o MBAM com o System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="fdabc-105">This topology integrates MBAM with System Center Configuration Manager.</span></span> <span data-ttu-id="fdabc-106">Para implantar o MBAM com a topologia autônoma, consulte [arquitetura de alto nível do MBAM 2,5 com topologia](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)autônoma.</span><span class="sxs-lookup"><span data-stu-id="fdabc-106">To deploy MBAM with the Stand-alone topology, see [High-Level Architecture of MBAM 2.5 with Stand-alone Topology](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span></span>

<span data-ttu-id="fdabc-107">Para obter uma lista das versões com suporte do software mencionadas neste tópico, consulte [configurações compatíveis do MBAM 2,5](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="fdabc-107">For a list of the supported versions of the software mentioned in this topic, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

<span data-ttu-id="fdabc-108">**Importante**  Não há suporte para o Windows to go para a instalação de topologia de integração do Configuration Manager quando você está usando o Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="fdabc-108">**Important** Windows To Go is not supported for the Configuration Manager Integration topology installation when you are using Configuration Manager 2007.</span></span>

 

## <span data-ttu-id="fdabc-109">Número recomendado de servidores e número de clientes com suporte</span><span class="sxs-lookup"><span data-stu-id="fdabc-109">Recommended number of servers and supported number of clients</span></span>


<span data-ttu-id="fdabc-110">O número recomendado de servidores e o número de clientes com suporte em um ambiente de produção é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fdabc-110">The recommended number of servers and supported number of clients in a production environment is as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fdabc-111">Arquitetura recomendada</span><span class="sxs-lookup"><span data-stu-id="fdabc-111">Recommended architecture</span></span></th>
<th align="left"><span data-ttu-id="fdabc-112">Detalhes</span><span class="sxs-lookup"><span data-stu-id="fdabc-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdabc-113">Número de servidores e outros computadores</span><span class="sxs-lookup"><span data-stu-id="fdabc-113">Number of servers and other computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdabc-114">Três servidores</span><span class="sxs-lookup"><span data-stu-id="fdabc-114">Three servers</span></span></p>
<p><span data-ttu-id="fdabc-115">Uma estação de trabalho</span><span class="sxs-lookup"><span data-stu-id="fdabc-115">One workstation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdabc-116">Número de computadores cliente com suporte</span><span class="sxs-lookup"><span data-stu-id="fdabc-116">Number of client computers supported</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdabc-117">500.000</span><span class="sxs-lookup"><span data-stu-id="fdabc-117">500,000</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="fdabc-118">Diferenças entre a integração do Configuration Manager e as topologias autônomas</span><span class="sxs-lookup"><span data-stu-id="fdabc-118">Differences between Configuration Manager Integration and stand-alone topologies</span></span>


<span data-ttu-id="fdabc-119">As principais diferenças entre as topologias são:</span><span class="sxs-lookup"><span data-stu-id="fdabc-119">The main differences between the topologies are:</span></span>

-   <span data-ttu-id="fdabc-120">Os recursos de conformidade e relatório são removidos do MBAM e são acessados do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="fdabc-120">The compliance and reporting features are removed from MBAM and are accessed from Configuration Manager.</span></span>

-   <span data-ttu-id="fdabc-121">Os relatórios são exibidos no console de gerenciamento do Configuration Manager, com exceção do relatório de auditoria de recuperação, que você continua a exibir no site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="fdabc-121">Reports are viewed from the Configuration Manager Management Console, with the exception of the Recovery Audit Report, which you continue to view from the MBAM Administration and Monitoring Website.</span></span>

## <span data-ttu-id="fdabc-122">Arquitetura de alto nível MBAM recomendada com a topologia de integração do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="fdabc-122">Recommended MBAM high-level architecture with the Configuration Manager Integration topology</span></span>


<span data-ttu-id="fdabc-123">O diagrama e a tabela a seguir descrevem a arquitetura de alto nível recomendada para o MBAM com a topologia de integração do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="fdabc-123">The following diagram and table describe the recommended high-level architecture for MBAM with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="fdabc-124">MBAM implantações de várias florestas exigem confiança unidirecional ou bidirecional.</span><span class="sxs-lookup"><span data-stu-id="fdabc-124">MBAM multi-forest deployments require a one-way or two-way trust.</span></span> <span data-ttu-id="fdabc-125">As relações de confiança unidirecionais exigem que o domínio do servidor confie no domínio do cliente.</span><span class="sxs-lookup"><span data-stu-id="fdabc-125">One-way trusts require that the server domain trusts the client domain.</span></span>

![mbam2\-5](images/mbam2-5-cmserver.png)

### <span data-ttu-id="fdabc-127">Servidor de banco de dados</span><span class="sxs-lookup"><span data-stu-id="fdabc-127">Database server</span></span>

#### <span data-ttu-id="fdabc-128">Banco de dados de recuperação</span><span class="sxs-lookup"><span data-stu-id="fdabc-128">Recovery database</span></span>

<span data-ttu-id="fdabc-129">Esse recurso é configurado em um computador com o Windows Server e com suporte para a instância do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fdabc-129">This feature is configured on a computer running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="fdabc-130">O **banco** de dados de recuperação armazena dados de recuperação coletados de computadores cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="fdabc-130">The **Recovery Database** stores recovery data that is collected from MBAM Client computers.</span></span>

#### <span data-ttu-id="fdabc-131">Banco de dados de auditoria</span><span class="sxs-lookup"><span data-stu-id="fdabc-131">Audit database</span></span>

<span data-ttu-id="fdabc-132">Esse recurso é configurado em um computador com o Windows Server e com suporte para a instância do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fdabc-132">This feature is configured on a computer running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="fdabc-133">O **banco** de dados de auditoria armazena dados de atividades de auditoria coletados de computadores cliente que acessam dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fdabc-133">The **Audit Database** stores audit activity data that is collected from client computers that have accessed recovery data.</span></span>

#### <span data-ttu-id="fdabc-134">Relatórios</span><span class="sxs-lookup"><span data-stu-id="fdabc-134">Reports</span></span>

<span data-ttu-id="fdabc-135">Esse recurso é configurado em um computador com o Windows Server e com suporte para a instância do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fdabc-135">This feature is configured on a computer running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="fdabc-136">Os **relatórios** fornecem dados de auditoria de recuperação para os computadores cliente da sua empresa.</span><span class="sxs-lookup"><span data-stu-id="fdabc-136">The **Reports** provide recovery audit data for the client computers in your enterprise.</span></span> <span data-ttu-id="fdabc-137">Você pode exibir relatórios do console do Configuration Manager ou diretamente do SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="fdabc-137">You can view reports from the Configuration Manager console or directly from SQL Server Reporting Services.</span></span>

### <span data-ttu-id="fdabc-138">Servidor de site primário do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="fdabc-138">Configuration Manager primary site server</span></span>

<span data-ttu-id="fdabc-139">Recurso de integração do System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="fdabc-139">System Center Configuration Manager Integration feature</span></span>

-   <span data-ttu-id="fdabc-140">Esse recurso está configurado no servidor de site primário do Configuration Manager, que é o servidor de nível superior na infraestrutura do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="fdabc-140">This feature is configured on the Configuration Manager Primary Site Server, which is the top-tier server in your Configuration Manager infrastructure.</span></span>

-   <span data-ttu-id="fdabc-141">O **servidor do Configuration Manager** coleta as informações do inventário de hardware dos computadores cliente e é usada para denunciar a compatibilidade do BitLocker em computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="fdabc-141">The **Configuration Manager Server** collects the hardware inventory information from client computers and is used to report BitLocker compliance of client computers.</span></span>

-   <span data-ttu-id="fdabc-142">Quando você executa o assistente de configuração de administração e administração do Microsoft BitLocker para instalar o software do servidor, o conjunto de computadores com suporte MBAM, a linha de base de configuração e os relatórios são configurados no servidor de site primário do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="fdabc-142">When you run the Microsoft BitLocker Administration and Monitoring Setup wizard to install the server software, the MBAM Supported Computers collection, configuration baseline, and reports are configured on the Configuration Manager Primary Site Server.</span></span>

-   <span data-ttu-id="fdabc-143">O **console do Configuration Manager** deve ser instalado no mesmo computador em que você instala o software MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="fdabc-143">The **Configuration Manager console** must be installed on the same computer on which you install the MBAM Server software.</span></span>

### <span data-ttu-id="fdabc-144">Servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="fdabc-144">Administration and monitoring server</span></span>

#### <span data-ttu-id="fdabc-145">Site de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="fdabc-145">Administration and monitoring website</span></span>

<span data-ttu-id="fdabc-146">Esse recurso é configurado em um computador que executa o Windows Server.</span><span class="sxs-lookup"><span data-stu-id="fdabc-146">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="fdabc-147">O **site de administração e monitoramento** é usado para:</span><span class="sxs-lookup"><span data-stu-id="fdabc-147">The **Administration and monitoring website** is used to:</span></span>

-   <span data-ttu-id="fdabc-148">Ajude os usuários finais a recuperarem o acesso aos seus computadores quando estiverem bloqueados. (Essa área do site geralmente é chamada de suporte técnico).</span><span class="sxs-lookup"><span data-stu-id="fdabc-148">Help end users regain access to their computers when they are locked out. (This area of the Website is commonly called the Help Desk.)</span></span>

-   <span data-ttu-id="fdabc-149">Exibir o relatório de auditoria de recuperação, que mostra a atividade de recuperação para computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="fdabc-149">View the Recovery Audit Report, which shows recovery activity for client computers.</span></span> <span data-ttu-id="fdabc-150">Outros relatórios são exibidos no console do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="fdabc-150">Other reports are viewed from the Configuration Manager console.</span></span>

#### <span data-ttu-id="fdabc-151">Portal de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="fdabc-151">Self-service portal</span></span>

<span data-ttu-id="fdabc-152">Esse recurso é configurado em um computador que executa o Windows Server.</span><span class="sxs-lookup"><span data-stu-id="fdabc-152">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="fdabc-153">O **portal de autoatendimento** é um site que permite aos usuários finais nos computadores cliente fazerem logon independentemente em um site para obter uma chave de recuperação caso percam ou esqueçam a senha do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fdabc-153">The **Self-Service Portal** is a website that enables end users on client computers to independently log on to a website to get a recovery key if they lose or forget their BitLocker password.</span></span>

#### <span data-ttu-id="fdabc-154">Monitorando serviços Web para este site</span><span class="sxs-lookup"><span data-stu-id="fdabc-154">Monitoring web services for this website</span></span>

<span data-ttu-id="fdabc-155">Esse recurso é instalado em um computador que executa o Windows Server.</span><span class="sxs-lookup"><span data-stu-id="fdabc-155">This feature is installed on a computer running Windows Server.</span></span>

<span data-ttu-id="fdabc-156">Os **Serviços Web de monitoramento** são usados pelo cliente MBAM e pelos websites para se comunicar ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fdabc-156">The **monitoring web services** are used by the MBAM Client and the websites to communicate to the database.</span></span>

**<span data-ttu-id="fdabc-157">Importante</span><span class="sxs-lookup"><span data-stu-id="fdabc-157">Important</span></span>**<br><span data-ttu-id="fdabc-158">O serviço Web de monitoramento não está mais disponível no Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1, pois os sites do MBAM se comunicam diretamente com o banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fdabc-158">The Monitoring Web Service is no longer available in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 since the MBAM websites communicate directly with the Recovery Database.</span></span> 

 

### <span data-ttu-id="fdabc-159">Estação de trabalho de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="fdabc-159">Management workstation</span></span>

#### <span data-ttu-id="fdabc-160">Modelos de política de grupo MBAM</span><span class="sxs-lookup"><span data-stu-id="fdabc-160">MBAM group policy templates</span></span>

-   <span data-ttu-id="fdabc-161">Os **modelos de política de grupo do MBAM** são configurações de política de grupo que definem configurações de implementação para MBAM, que permitem que você gerencie a criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fdabc-161">The **MBAM Group Policy Templates** are Group Policy settings that define implementation settings for MBAM, which enable you to manage BitLocker drive encryption.</span></span>

-   <span data-ttu-id="fdabc-162">Antes de executar o MBAM, você deve baixar os modelos de política de grupo de [como obter modelos de política de grupo do MDOP (. admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) e copiá-los para um servidor ou estação de trabalho que esteja executando um servidor Windows ou sistema operacional Windows com suporte.</span><span class="sxs-lookup"><span data-stu-id="fdabc-162">Before you run MBAM, you must download the Group Policy Templates from [How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941) and copy them to a server or workstation that is running a supported Windows Server or Windows operating system.</span></span>

    **<span data-ttu-id="fdabc-163">OBSERVAÇÃO</span><span class="sxs-lookup"><span data-stu-id="fdabc-163">NOTE</span></span>**<br><span data-ttu-id="fdabc-164">A estação de trabalho não precisa ser um computador dedicado.</span><span class="sxs-lookup"><span data-stu-id="fdabc-164">The workstation does not have to be a dedicated computer.</span></span>

     

### <span data-ttu-id="fdabc-165">Cliente MBAM e computador cliente do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="fdabc-165">MBAM Client and Configuration Manager Client computer</span></span>

#### <span data-ttu-id="fdabc-166">Software cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="fdabc-166">MBAM Client software</span></span>

<span data-ttu-id="fdabc-167">O **cliente MBAM**:</span><span class="sxs-lookup"><span data-stu-id="fdabc-167">The **MBAM Client**:</span></span>

-   <span data-ttu-id="fdabc-168">Usa objetos de política de grupo para impor a criptografia de unidade de disco BitLocker em computadores cliente da empresa.</span><span class="sxs-lookup"><span data-stu-id="fdabc-168">Uses Group Policy Objects to enforce BitLocker drive encryption on client computers in the enterprise.</span></span>

-   <span data-ttu-id="fdabc-169">Coleta a chave de recuperação do BitLocker para três tipos de unidade de dados: unidades do sistema operacional, unidades de dados fixas e unidades de dados removíveis (USB).</span><span class="sxs-lookup"><span data-stu-id="fdabc-169">Collects the BitLocker recovery key for three data drive types: operating system drives, fixed data drives, and removable (USB) data drives.</span></span>

-   <span data-ttu-id="fdabc-170">Coleta informações de recuperação e informações do computador dos computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="fdabc-170">Collects recovery information and computer information about the client computers.</span></span>

#### <span data-ttu-id="fdabc-171">Cliente do Gerenciador de Configurações</span><span class="sxs-lookup"><span data-stu-id="fdabc-171">Configuration Manager Client</span></span>

<span data-ttu-id="fdabc-172">O **cliente do Configuration Manager** permite que o Configuration Manager colete dados de compatibilidade de hardware sobre os computadores cliente e informe as informações de conformidade.</span><span class="sxs-lookup"><span data-stu-id="fdabc-172">The **Configuration Manager Client** enables Configuration Manager to collect hardware compatibility data about the client computers and report compliance information.</span></span>

 

## <span data-ttu-id="fdabc-173">Diferenças na implantação do MBAM para versões do Gerenciador de configurações com suporte</span><span class="sxs-lookup"><span data-stu-id="fdabc-173">Differences in MBAM deployment for supported Configuration Manager versions</span></span>


<span data-ttu-id="fdabc-174">Ao implantar o MBAM com a topologia de integração do Configuration Manager, você pode instalar o MBAM em um servidor de site primário.</span><span class="sxs-lookup"><span data-stu-id="fdabc-174">When you deploy MBAM with the Configuration Manager Integration topology, you can install MBAM on a primary site server.</span></span> <span data-ttu-id="fdabc-175">No entanto, a instalação do MBAM funciona de forma diferente para o Gerenciador de configuração do Center2012 e Manager2007 de configuração do sistema.</span><span class="sxs-lookup"><span data-stu-id="fdabc-175">However, the MBAM installation works differently for System Center2012 Configuration Manager and Configuration Manager2007.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fdabc-176">Versão do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="fdabc-176">Configuration Manager version</span></span></th>
<th align="left"><span data-ttu-id="fdabc-177">Descrição</span><span class="sxs-lookup"><span data-stu-id="fdabc-177">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdabc-178">Gerenciador de configuração do sistema Center2012 R2</span><span class="sxs-lookup"><span data-stu-id="fdabc-178">System Center2012 R2 Configuration Manager</span></span></p>
<p><span data-ttu-id="fdabc-179">Gerenciador de configuração do Center2012 do sistema</span><span class="sxs-lookup"><span data-stu-id="fdabc-179">System Center2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdabc-180">Se você instalar o MBAM em um servidor de site primário ou em um servidor de administração central, o MBAM executará todas as ações de instalação nesse servidor de site.</span><span class="sxs-lookup"><span data-stu-id="fdabc-180">If you install MBAM on a primary site server or on a central administration server, MBAM performs all of the installation actions on that site server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdabc-181">Manager2007 de configuração R2</span><span class="sxs-lookup"><span data-stu-id="fdabc-181">Configuration Manager2007 R2</span></span></p>
<p><span data-ttu-id="fdabc-182">Manager2007 de configuração</span><span class="sxs-lookup"><span data-stu-id="fdabc-182">Configuration Manager2007</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdabc-183">Se você instalar o MBAM em um servidor de site primário que faz parte de uma hierarquia do Configuration Manager maior com um servidor pai do site central, MBAM identificará o servidor pai do site central e executará todas as ações de instalação nesse servidor pai.</span><span class="sxs-lookup"><span data-stu-id="fdabc-183">If you install MBAM on a primary site server that is part of a larger Configuration Manager hierarchy with a central site parent server, MBAM identifies the central site parent server and performs all of the installation actions on that parent server.</span></span> <span data-ttu-id="fdabc-184">A instalação inclui verificar pré-requisitos e instalar objetos e relatórios do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="fdabc-184">The installation includes checking prerequisites and installing the Configuration Manager objects and reports.</span></span></p>
<p><span data-ttu-id="fdabc-185">Por exemplo, se você instalar o MBAM em um servidor de site primário que seja filho de um servidor pai de site central, o MBAM instalará todos os objetos e relatórios do Configuration Manager no servidor pai.</span><span class="sxs-lookup"><span data-stu-id="fdabc-185">For example, if you install MBAM on a primary site server that is a child of a central site parent server, MBAM installs all of the Configuration Manager objects and reports on the parent server.</span></span> <span data-ttu-id="fdabc-186">Se você instalar o MBAM no servidor pai, o MBAM executará todas as ações de instalação nesse servidor pai.</span><span class="sxs-lookup"><span data-stu-id="fdabc-186">If you install MBAM on the parent server, MBAM performs all of the installation actions on that parent server.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="fdabc-187">Como o MBAM funciona com o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="fdabc-187">How MBAM works with Configuration Manager</span></span>


<span data-ttu-id="fdabc-188">A integração do MBAM com o Configuration Manager se baseia em um pacote de configuração que instala os itens descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fdabc-188">The integration of MBAM with Configuration Manager is based on a configuration pack that installs the items described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fdabc-189">Itens instalados no Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="fdabc-189">Items installed into Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="fdabc-190">Descrição</span><span class="sxs-lookup"><span data-stu-id="fdabc-190">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdabc-191">Dados de configuração</span><span class="sxs-lookup"><span data-stu-id="fdabc-191">Configuration data</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdabc-192">Os dados de configuração instalam uma linha de base de configuração, chamada "proteção BitLocker", que contém dois itens de configuração:</span><span class="sxs-lookup"><span data-stu-id="fdabc-192">The configuration data installs a configuration baseline, called “BitLocker Protection,” which contains two configuration items:</span></span></p>
<ul>
<li><p><span data-ttu-id="fdabc-193">Proteção de unidade do sistema operacional BitLocker</span><span class="sxs-lookup"><span data-stu-id="fdabc-193">BitLocker Operating System Drive Protection</span></span></p></li>
<li><p><span data-ttu-id="fdabc-194">Proteção de unidades de dados fixas do BitLocker</span><span class="sxs-lookup"><span data-stu-id="fdabc-194">BitLocker Fixed Data Drives Protection</span></span></p></li>
</ul>
<p><span data-ttu-id="fdabc-195">A linha de base de configuração é implantada no conjunto de computadores com suporte MBAM, que também é criado quando o MBAM está instalado.</span><span class="sxs-lookup"><span data-stu-id="fdabc-195">The configuration baseline is deployed to the MBAM Supported Computers collection, which is also created when MBAM is installed.</span></span></p>
<p><span data-ttu-id="fdabc-196">Os dois itens de configuração fornecem a base para avaliar o status de conformidade dos computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="fdabc-196">The two configuration items provide the basis for evaluating the compliance status of the client computers.</span></span> <span data-ttu-id="fdabc-197">Essas informações são capturadas, armazenadas e avaliadas no Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="fdabc-197">This information is captured, stored, and evaluated in Configuration Manager.</span></span></p>
<p><span data-ttu-id="fdabc-198">Os itens de configuração se baseiam nos requisitos de conformidade para unidades do sistema operacional e unidades de dados fixas.</span><span class="sxs-lookup"><span data-stu-id="fdabc-198">The configuration items are based on the compliance requirements for operating system drives and fixed data drives.</span></span> <span data-ttu-id="fdabc-199">Os detalhes necessários para os computadores implantados são coletados para que a conformidade desses tipos de unidade possa ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="fdabc-199">The required details for the deployed computers are collected so that the compliance for those drive types can be evaluated.</span></span></p>
<p><span data-ttu-id="fdabc-200">Por padrão, a linha de base de configuração avalia o status de conformidade every12 horas e envia os dados de conformidade para o Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="fdabc-200">By default, the configuration baseline evaluates the compliance status every12 hours and sends the compliance data to Configuration Manager.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdabc-201">Conjunto de computadores com suporte MBAM</span><span class="sxs-lookup"><span data-stu-id="fdabc-201">MBAM Supported Computers collection</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdabc-202">MBAM cria uma coleção chamada MBAM computadores com suporte.</span><span class="sxs-lookup"><span data-stu-id="fdabc-202">MBAM creates a collection that is called MBAM Supported Computers.</span></span> <span data-ttu-id="fdabc-203">A linha de base de configuração é direcionada para computadores cliente que estão nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="fdabc-203">The configuration baseline is targeted to client computers that are in this collection.</span></span></p>
<p><span data-ttu-id="fdabc-204">Esta é uma coleção dinâmica.</span><span class="sxs-lookup"><span data-stu-id="fdabc-204">This is a dynamic collection.</span></span> <span data-ttu-id="fdabc-205">Por padrão, ele executa every12 horas e avalia a associação, com base em três critérios:</span><span class="sxs-lookup"><span data-stu-id="fdabc-205">By default, it runs every12 hours and evaluates membership, based on three criteria:</span></span></p>
<ul>
<li><p><span data-ttu-id="fdabc-206">O computador é uma versão com suporte do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="fdabc-206">The computer is a supported version of the Windows operating system.</span></span></p></li>
<li><p><span data-ttu-id="fdabc-207">O computador é um computador físico.</span><span class="sxs-lookup"><span data-stu-id="fdabc-207">The computer is a physical computer.</span></span> <span data-ttu-id="fdabc-208">Não há suporte para máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="fdabc-208">Virtual machines are not supported.</span></span></p></li>
<li><p><span data-ttu-id="fdabc-209">O computador tem um TPM (Trusted Platform Module) que está disponível.</span><span class="sxs-lookup"><span data-stu-id="fdabc-209">The computer has a Trusted Platform Module (TPM) that is available.</span></span> <span data-ttu-id="fdabc-210">Uma versão compatível do TPM 1.2 ou posterior é necessária para o Windows7.</span><span class="sxs-lookup"><span data-stu-id="fdabc-210">A compatible version of TPM1.2 or later is required for Windows7.</span></span> <span data-ttu-id="fdabc-211">O Windows10, o Windows 8.1, o Windows8 e o Windows to go não exigem um TPM.</span><span class="sxs-lookup"><span data-stu-id="fdabc-211">Windows10, Windows8.1, Windows8, and Windows To Go do not require a TPM.</span></span></p></li>
</ul>
<p><span data-ttu-id="fdabc-212">A coleção é avaliada em todos os computadores e um subconjunto de computadores compatíveis é criado, o que fornece a base para a avaliação de conformidade e a geração de relatórios para a integração com o MBAM.</span><span class="sxs-lookup"><span data-stu-id="fdabc-212">The collection is evaluated against all computers and a subset of compatible computers is created, which provides the basis for compliance evaluation and reporting for the MBAM integration.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdabc-213">Relatórios</span><span class="sxs-lookup"><span data-stu-id="fdabc-213">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdabc-214">Quando você configura o MBAM com a topologia de integração do Configuration Manager, você vê todos os relatórios no Configuration Manager, exceto o relatório de auditoria de recuperação, o último que você continua a exibir no site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="fdabc-214">When you configure MBAM with the Configuration Manager Integration topology, you view all reports in Configuration Manager, except the Recovery Audit Report, the latter of which you continue to view in the MBAM Administration and Monitoring Website.</span></span> <span data-ttu-id="fdabc-215">Os relatórios disponíveis no Configuration Manager são:</span><span class="sxs-lookup"><span data-stu-id="fdabc-215">The reports available in Configuration Manager are:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fdabc-216">Relatório</span><span class="sxs-lookup"><span data-stu-id="fdabc-216">Report</span></span></th>
<th align="left"><span data-ttu-id="fdabc-217">Descrição</span><span class="sxs-lookup"><span data-stu-id="fdabc-217">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdabc-218">Painel de conformidade do BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="fdabc-218">BitLocker Enterprise Compliance Dashboard</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdabc-219">Fornece aos administradores de ti três exibições de informações em um único relatório: distribuição de status de conformidade, não compatível – distribuição de erros e distribuição de status de conformidade por tipo de unidade.</span><span class="sxs-lookup"><span data-stu-id="fdabc-219">Gives IT administrators three views of information in a single report: Compliance Status Distribution, Non Compliant – Errors Distribution, and Compliance Status Distribution By Drive Type.</span></span> <span data-ttu-id="fdabc-220">As opções de busca detalhada no relatório permitem que os administradores de ti cliquem nos dados e exibam uma lista de computadores que correspondem ao estado selecionado.</span><span class="sxs-lookup"><span data-stu-id="fdabc-220">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the selected state.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdabc-221">Detalhes de conformidade corporativa do BitLocker</span><span class="sxs-lookup"><span data-stu-id="fdabc-221">BitLocker Enterprise Compliance Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdabc-222">Permite que os administradores de ti exibam informações sobre o status de conformidade de criptografia do BitLocker da empresa e inclui o status de conformidade de cada computador.</span><span class="sxs-lookup"><span data-stu-id="fdabc-222">Lets IT administrators view information about the BitLocker encryption compliance status of the enterprise and includes the compliance status for each computer.</span></span> <span data-ttu-id="fdabc-223">As opções de busca detalhada no relatório permitem que os administradores de ti cliquem nos dados e exibam uma lista de computadores que correspondem ao estado selecionado.</span><span class="sxs-lookup"><span data-stu-id="fdabc-223">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the selected state.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fdabc-224">Conformidade do computador BitLocker</span><span class="sxs-lookup"><span data-stu-id="fdabc-224">BitLocker Computer Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdabc-225">Permite que os administradores de ti visualizem um computador individual e determine por que ele foi reportado com um status de conformidade ou não compatível.</span><span class="sxs-lookup"><span data-stu-id="fdabc-225">Lets IT administrators view an individual computer and determine why it was reported with a status of compliant or not compliant.</span></span> <span data-ttu-id="fdabc-226">O relatório também exibe o estado de criptografia das unidades de sistema operacional e unidades de dados fixas.</span><span class="sxs-lookup"><span data-stu-id="fdabc-226">The report also displays the encryption state of the operating system drives and fixed data drives.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fdabc-227">Resumo de conformidade empresarial do BitLocker</span><span class="sxs-lookup"><span data-stu-id="fdabc-227">BitLocker Enterprise Compliance Summary</span></span></p></td>
<td align="left"><p><span data-ttu-id="fdabc-228">Permite que os administradores de ti exibam o status da conformidade da política do MBAM na empresa.</span><span class="sxs-lookup"><span data-stu-id="fdabc-228">Lets IT administrators view the status of MBAM policy compliance in the enterprise.</span></span> <span data-ttu-id="fdabc-229">O estado de cada computador é avaliado, e o relatório mostra um resumo da conformidade de todos os computadores na empresa em relação à política.</span><span class="sxs-lookup"><span data-stu-id="fdabc-229">Each computer’s state is evaluated, and the report shows a summary of the compliance of all computers in the enterprise against the policy.</span></span> <span data-ttu-id="fdabc-230">As opções de busca detalhada no relatório permitem que os administradores de ti cliquem nos dados e exibam uma lista de computadores que correspondem ao estado selecionado.</span><span class="sxs-lookup"><span data-stu-id="fdabc-230">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the selected state.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="fdabc-231">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fdabc-231">Related topics</span></span>


[<span data-ttu-id="fdabc-232">Introdução ao MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="fdabc-232">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

[<span data-ttu-id="fdabc-233">Arquitetura de alto nível do MBAM 2.5 com topologia autônoma</span><span class="sxs-lookup"><span data-stu-id="fdabc-233">High-Level Architecture of MBAM 2.5 with Stand-alone Topology</span></span>](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)

[<span data-ttu-id="fdabc-234">Recursos ilustrados de uma implantação do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="fdabc-234">Illustrated Features of an MBAM 2.5 Deployment</span></span>](illustrated-features-of-an-mbam-25-deployment.md)

 

 
## <span data-ttu-id="fdabc-235">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="fdabc-235">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="fdabc-236">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="fdabc-236">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="fdabc-237">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="fdabc-237">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




