---
title: Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell
description: Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell
author: dansimp
ms.assetid: 826429fd-29bb-44be-b47e-5f5c7d20dd1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f350a9eb96a20f50644cfdc1965b7f72741a2c29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799152"
---
# <span data-ttu-id="79158-103">Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="79158-103">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>


<span data-ttu-id="79158-104">Depois de instalar o software de servidor MBAM 2,5, você pode usar os recursos de servidor configurar MBAM 2,5 usando cmdlets do Windows PowerShell ou o assistente de configuração do servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="79158-104">After you install the MBAM 2.5 Server software, you can use configure MBAM 2.5 Server features by using Windows PowerShell cmdlets or the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="79158-105">Este tópico descreve como configurar o MBAM 2,5 usando os cmdlets do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="79158-105">This topic describes how to configure MBAM 2.5 by using the Windows PowerShell cmdlets.</span></span> <span data-ttu-id="79158-106">Para usar o assistente em vez disso, consulte [Configurando os recursos do servidor do MBAM 2,5](configuring-the-mbam-25-server-features.md).</span><span class="sxs-lookup"><span data-stu-id="79158-106">To use the wizard instead, see [Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md).</span></span>

## <span data-ttu-id="79158-107">Neste tópico</span><span class="sxs-lookup"><span data-stu-id="79158-107">In this topic</span></span>


<span data-ttu-id="79158-108">Este tópico inclui as seguintes informações sobre como usar o Windows PowerShell para configurar o MBAM:</span><span class="sxs-lookup"><span data-stu-id="79158-108">This topic includes the following information about using Windows PowerShell to configure MBAM:</span></span>

-   [<span data-ttu-id="79158-109">Como carregar a ajuda do Windows PowerShell para MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="79158-109">How to load Windows PowerShell Help for MBAM 2.5</span></span>](#bkmk-load-posh-help)

-   [<span data-ttu-id="79158-110">Como obter ajuda sobre um cmdlet MBAM do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="79158-110">How to get Help about an MBAM Windows PowerShell cmdlet</span></span>](#bkmk-help-specific-cmdlet)

-   [<span data-ttu-id="79158-111">Configurações que você pode fazer somente com o Windows PowerShell, mas não com o assistente de configuração do servidor do MBAM</span><span class="sxs-lookup"><span data-stu-id="79158-111">Configurations that you can do only with Windows PowerShell but not with the MBAM Server Configuration wizard</span></span>](#bkmk-config-only-posh)

-   [<span data-ttu-id="79158-112">Pré-requisitos e requisitos para usar o Windows PowerShell para configurar recursos do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="79158-112">Prerequisites and requirements for using Windows PowerShell to configure MBAM Server features</span></span>](#bkmk-prereqs-posh-mbamsvr)

-   [<span data-ttu-id="79158-113">Usar o Windows PowerShell para configurar o MBAM em um computador remoto</span><span class="sxs-lookup"><span data-stu-id="79158-113">Using Windows PowerShell to configure MBAM on a remote computer</span></span>](#bkmk-remote-config)

-   [<span data-ttu-id="79158-114">Contas necessárias e parâmetros do cmdlet do Windows PowerShell correspondentes</span><span class="sxs-lookup"><span data-stu-id="79158-114">Required accounts and corresponding Windows PowerShell cmdlet parameters</span></span>](#bkmk-reqd-posh-accts)

<span data-ttu-id="79158-115">Para obter informações sobre os cmdlets **Get-MbamBitLockerRecoveryKey** e **Get-MbamTPMOwnerPassword** do Windows PowerShell, que são usados para administrar o MBAM, consulte [usando o Windows PowerShell para administrar MBAM o 2,5](using-windows-powershell-to-administer-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="79158-115">For information about the **Get-MbamBitLockerRecoveryKey** and **Get-MbamTPMOwnerPassword** Windows PowerShell cmdlets, which are used to administer MBAM, see [Using Windows PowerShell to Administer MBAM 2.5](using-windows-powershell-to-administer-mbam-25.md).</span></span>

## <a href="" id="bkmk-load-posh-help"></a><span data-ttu-id="79158-116">Como carregar a ajuda do Windows PowerShell para MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="79158-116">How to load Windows PowerShell Help for MBAM 2.5</span></span>


<span data-ttu-id="79158-117">Para obter uma lista dos cmdlets do Windows PowerShell no TechNet, consulte [automação do Microsoft Desktop Optimization Pack with Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=392816).</span><span class="sxs-lookup"><span data-stu-id="79158-117">For a list of the Windows PowerShell cmdlets on TechNet, see [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=392816).</span></span>

**<span data-ttu-id="79158-118">Para carregar a ajuda do MBAM 2,5 para cmdlets do Windows PowerShell após instalar o software do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="79158-118">To load the MBAM 2.5 Help for Windows PowerShell cmdlets after installing the MBAM Server software</span></span>**

1.  <span data-ttu-id="79158-119">Abra o Windows PowerShell ou o ambiente de script integrado do Windows PowerShell (ISE).</span><span class="sxs-lookup"><span data-stu-id="79158-119">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="79158-120">Digite **Update-Help – módulo Microsoft. MBAM**.</span><span class="sxs-lookup"><span data-stu-id="79158-120">Type **Update-Help –Module Microsoft.MBAM**.</span></span>

## <a href="" id="bkmk-help-specific-cmdlet"></a><span data-ttu-id="79158-121">Como obter ajuda sobre um cmdlet MBAM do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="79158-121">How to get Help about an MBAM Windows PowerShell cmdlet</span></span>


<span data-ttu-id="79158-122">A ajuda do Windows PowerShell para MBAM está disponível nos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="79158-122">Windows PowerShell Help for MBAM is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="79158-123">Formato de ajuda do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="79158-123">Windows PowerShell Help format</span></span></th>
<th align="left"><span data-ttu-id="79158-124">Mais informações</span><span class="sxs-lookup"><span data-stu-id="79158-124">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79158-125">Em um prompt de comando do Windows PowerShell, digite <strong> </strong> &lt; <em> cmdlet Get-Help</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="79158-125">At a Windows PowerShell command prompt, type <strong>Get-Help</strong> &lt;<em>cmdlet</em>&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="79158-126">Para carregar os cmdlets do Windows PowerShell mais recentes, siga as instruções na seção anterior sobre como carregar a ajuda do Windows PowerShell para MBAM.</span><span class="sxs-lookup"><span data-stu-id="79158-126">To upload the latest Windows PowerShell cmdlets, follow the instructions in the previous section on how to load Windows PowerShell Help for MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79158-127">No TechNet como páginas da Web</span><span class="sxs-lookup"><span data-stu-id="79158-127">On TechNet as webpages</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79158-128">No centro de download como um arquivo. docx do Word</span><span class="sxs-lookup"><span data-stu-id="79158-128">On the Download Center as a Word .docx file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79158-129">No centro de download como um arquivo. pdf</span><span class="sxs-lookup"><span data-stu-id="79158-129">On the Download Center as a .pdf file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-config-only-posh"></a><span data-ttu-id="79158-130">Configurações que você pode fazer somente com o Windows PowerShell, mas não com o assistente de configuração do servidor do MBAM</span><span class="sxs-lookup"><span data-stu-id="79158-130">Configurations that you can do only with Windows PowerShell but not with the MBAM Server Configuration wizard</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="79158-131">Configurações que você pode fazer somente usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="79158-131">Configurations that you can do only by using Windows PowerShell</span></span></th>
<th align="left"><span data-ttu-id="79158-132">Detalhes</span><span class="sxs-lookup"><span data-stu-id="79158-132">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79158-133">Instale os serviços Web em um computador separado dos aplicativos da Web.</span><span class="sxs-lookup"><span data-stu-id="79158-133">Install the web services on a separate computer from the web applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="79158-134">Usando o assistente, você deve instalar os serviços Web e aplicativos Web no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="79158-134">Using the wizard, you must install the web services and web applications on the same computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79158-135">Habilite relatórios em um ponto separado do Reporting Services sem instalar todos os objetos do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="79158-135">Enable reports on a separate reporting services point without installing all of the Configuration Manager objects.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79158-136">Exclua todos os objetos do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="79158-136">Delete all of the objects from Configuration Manager.</span></span></p></td>
<td align="left"><p><span data-ttu-id="79158-137">Excluir os objetos por sua vez exclui todos os dados de conformidade do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="79158-137">Deleting the objects in turn deletes all of the compliance data from Configuration Manager.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79158-138">Insira uma cadeia de conexão personalizada para os bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="79158-138">Enter a custom connection string for the databases.</span></span></p></td>
<td align="left"><p><span data-ttu-id="79158-139">Exemplo: para configurar os aplicativos Web para trabalhar com o espelhamento, você deve usar o <strong> cmdlet Enable-MbamWebApplication </strong> para especificar a sintaxe apropriada do parceiro de failover na cadeia de conexão.</span><span class="sxs-lookup"><span data-stu-id="79158-139">Example: To configure the web applications to work with mirroring, you must use the <strong>Enable-MbamWebApplication</strong> cmdlet to specify the appropriate failover partner syntax in the connection string.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79158-140">Ignorar a validação e configurar um recurso, mesmo que a verificação de pré-requisito tenha falhado.</span><span class="sxs-lookup"><span data-stu-id="79158-140">Skip validation and configure a feature even though the prerequisite check failed.</span></span></p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="79158-141">**Observação**  Você não pode desabilitar os bancos de dados do MBAM com um cmdlet do Windows PowerShell ou com o assistente de configuração do servidor do MBAM.</span><span class="sxs-lookup"><span data-stu-id="79158-141">**Note** You cannot disable the MBAM databases with a Windows PowerShell cmdlet or the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="79158-142">Para impedir a remoção acidental dos dados de auditoria e conformidade, os administradores de banco de dados devem remover os bancos de dados manualmente.</span><span class="sxs-lookup"><span data-stu-id="79158-142">To prevent the accidental removal of your compliance and audit data, database administrators must remove databases manually.</span></span>

 

## <a href="" id="bkmk-prereqs-posh-mbamsvr"></a><span data-ttu-id="79158-143">Pré-requisitos e requisitos para usar o Windows PowerShell para configurar recursos do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="79158-143">Prerequisites and requirements for using Windows PowerShell to configure MBAM Server features</span></span>


<span data-ttu-id="79158-144">Antes de iniciar a configuração, complete os pré-requisitos a seguir.</span><span class="sxs-lookup"><span data-stu-id="79158-144">Before starting the configuration, complete the following prerequisites.</span></span>

**<span data-ttu-id="79158-145">Pré-requisitos relacionados à conta</span><span class="sxs-lookup"><span data-stu-id="79158-145">Account-related prerequisites</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="79158-146">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="79158-146">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="79158-147">Detalhes ou informações adicionais</span><span class="sxs-lookup"><span data-stu-id="79158-147">Details or additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79158-148">Crie as contas necessárias.</span><span class="sxs-lookup"><span data-stu-id="79158-148">Create the required accounts.</span></span></p></td>
<td align="left"><p><span data-ttu-id="79158-149">Consulte <strong> a seção contas necessárias e os parâmetros de cmdlet correspondentes do Windows PowerShell </strong> mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="79158-149">See section <strong>Required accounts and corresponding Windows PowerShell cmdlet parameters</strong> later in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79158-150">Contas de usuário e grupos que você passa como parâmetros para os cmdlets do Windows PowerShell devem ser contas válidas no domínio.</span><span class="sxs-lookup"><span data-stu-id="79158-150">User accounts and groups that you pass as parameters to the Windows PowerShell cmdlets must be valid accounts in the domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="79158-151">Você não pode usar contas locais.</span><span class="sxs-lookup"><span data-stu-id="79158-151">You cannot use local accounts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79158-152">Especifique contas no formato de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="79158-152">Specify accounts in the down-level format.</span></span></p></td>
<td align="left"><p><span data-ttu-id="79158-153">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="79158-153">Examples:</span></span></p>
<p><span data-ttu-id="79158-154">domainNetBiosName\userdomainNetBiosName\group</span><span class="sxs-lookup"><span data-stu-id="79158-154">domainNetBiosName\userdomainNetBiosName\group</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="79158-155">Pré-requisitos relacionados à permissão</span><span class="sxs-lookup"><span data-stu-id="79158-155">Permission-related prerequisites</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="79158-156">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="79158-156">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="79158-157">Detalhes ou informações adicionais</span><span class="sxs-lookup"><span data-stu-id="79158-157">Details or additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79158-158">Você deve ser um administrador no computador local no qual está configurando o recurso MBAM.</span><span class="sxs-lookup"><span data-stu-id="79158-158">You must be an administrator on the local computer where you are configuring the MBAM feature.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79158-159">Use um prompt de comando elevado do Windows PowerShell para executar todos os cmdlets do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="79158-159">Use an elevated Windows PowerShell command prompt to run all Windows PowerShell cmdlets.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79158-160">Somente para o <strong> cmdlet Enable-MbamDatabase </strong> :</span><span class="sxs-lookup"><span data-stu-id="79158-160">For the <strong>Enable-MbamDatabase</strong> cmdlet only:</span></span></p>
<p><span data-ttu-id="79158-161">Você deve ter &quot; permissões criar qualquer banco de dados &quot; na instância do banco de dados de destino do Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="79158-161">You must have &quot;create any database&quot; permissions on the instance of the target Microsoft SQL Server database.</span></span></p>
<p><span data-ttu-id="79158-162">Essa conta de usuário deve fazer parte do grupo Administradores local ou do grupo operadores de backup para registrar o gravador do serviço de cópias de sombra de volume (VSS) do MBAM.</span><span class="sxs-lookup"><span data-stu-id="79158-162">This user account must be a part of the local administrators group or the Backup Operators group to register the MBAM Volume Shadow Copy Service (VSS) Writer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="79158-163">Por padrão, o administrador do banco de dados ou o administrador do sistema tem as &quot; permissões CREATE ANY DATABASE necessárias &quot; .</span><span class="sxs-lookup"><span data-stu-id="79158-163">By default, the database administrator or system administrator has the required &quot;create any database&quot; permissions.</span></span></p>
<p></p>
<p><span data-ttu-id="79158-164">Para obter mais informações sobre o gravador VSS, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=392814" data-raw-source="[Volume Shadow Copy Service](https://go.microsoft.com/fwlink/?LinkId=392814)"> serviço de cópias de sombra de volume </a> .</span><span class="sxs-lookup"><span data-stu-id="79158-164">For more information about VSS Writer, see <a href="https://go.microsoft.com/fwlink/?LinkId=392814" data-raw-source="[Volume Shadow Copy Service](https://go.microsoft.com/fwlink/?LinkId=392814)">Volume Shadow Copy Service</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79158-165">Somente para o <strong> recurso de integração do System Center Configuration Manager </strong> :</span><span class="sxs-lookup"><span data-stu-id="79158-165">For the <strong>System Center Configuration Manager Integration</strong> feature only:</span></span></p>
<p><span data-ttu-id="79158-166">O usuário que habilita esse recurso deve ter estes direitos no Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="79158-166">The user who enables this feature must have these rights in Configuration Manager:</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="79158-167">Tipo de direitos no Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="79158-167">Type of rights in Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="79158-168">Direitos obrigatórios</span><span class="sxs-lookup"><span data-stu-id="79158-168">Required rights</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79158-169">Direitos de site do Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="79158-169">Configuration Manager Site rights:</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="79158-170">Leitura</span><span class="sxs-lookup"><span data-stu-id="79158-170">Read</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="79158-171">Direitos de coleção do Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="79158-171">Configuration Manager Collection rights:</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="79158-172">Criar-excluir-ler-modificar-implantar itens de configuração</span><span class="sxs-lookup"><span data-stu-id="79158-172">Create- Delete- Read- Modify- Deploy Configuration Items</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="79158-173">Direitos de item de configuração do Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="79158-173">Configuration Manager Configuration item rights:</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="79158-174">Criar-excluir-ler</span><span class="sxs-lookup"><span data-stu-id="79158-174">Create- Delete- Read</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-remote-config"></a><span data-ttu-id="79158-175">Usar o Windows PowerShell para configurar o MBAM em um computador remoto</span><span class="sxs-lookup"><span data-stu-id="79158-175">Using Windows PowerShell to configure MBAM on a remote computer</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="79158-176">Quando usar esse recurso</span><span class="sxs-lookup"><span data-stu-id="79158-176">When to use this capability</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="79158-177">Quando você quiser configurar os recursos do servidor do MBAM 2,5 em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="79158-177">When you want to configure the MBAM 2.5 Server features on a remote computer.</span></span> <span data-ttu-id="79158-178">Os cmdlets do Windows PowerShell estão em execução em um computador, e você está configurando os recursos em um computador diferente e remoto.</span><span class="sxs-lookup"><span data-stu-id="79158-178">The Windows PowerShell cmdlets are running on one computer, and you are configuring the features on a different, remote computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="79158-179">O que você precisa fazer</span><span class="sxs-lookup"><span data-stu-id="79158-179">What you have to do</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="79158-180">Para usar o Windows PowerShell para configurar os recursos do MBAM 2,5 Server em um computador remoto, você deve:</span><span class="sxs-lookup"><span data-stu-id="79158-180">To use Windows PowerShell to configure MBAM 2.5 Server features on a remote computer, you must:</span></span></p>
<ul>
<li><p><span data-ttu-id="79158-181">Verifique se o software do servidor MBAM 2,5 foi instalado no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="79158-181">Ensure that the MBAM 2.5 Server software has been installed on the remote computer.</span></span></p></li>
<li><p><span data-ttu-id="79158-182">Use o protocolo Credential Security Support Provider (CredSSP) para abrir a sessão do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="79158-182">Use the Credential Security Support Provider (CredSSP) Protocol to open the Windows PowerShell session.</span></span></p></li>
<li><p><span data-ttu-id="79158-183">Habilite o gerenciamento remoto do Windows (WinRM).</span><span class="sxs-lookup"><span data-stu-id="79158-183">Enable Windows Remote Management (WinRM).</span></span> <span data-ttu-id="79158-184">Se você não conseguir habilitar o WinRM e configurá-lo corretamente, o <strong> cmdlet New-PSSession </strong> descrito nesta tabela exibirá um erro e descreverá como corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="79158-184">If you fail to enable WinRM and to configure it correctly, the <strong>New-PSSession</strong> cmdlet that is described in this table displays an error and describes how to fix the issue.</span></span> <span data-ttu-id="79158-185">Para obter mais informações sobre o WinRM, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=393064" data-raw-source="[Using Windows Remote Management](https://go.microsoft.com/fwlink/?LinkId=393064)"> usando o gerenciamento remoto do Windows </a> .</span><span class="sxs-lookup"><span data-stu-id="79158-185">For more information about WinRM, see <a href="https://go.microsoft.com/fwlink/?LinkId=393064" data-raw-source="[Using Windows Remote Management](https://go.microsoft.com/fwlink/?LinkId=393064)">Using Windows Remote Management</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="79158-186">Por que você precisa fazer isso</span><span class="sxs-lookup"><span data-stu-id="79158-186">Why you have to do it</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="79158-187">Esse protocolo permite que os cmdlets do Windows PowerShell se conectem aos serviços de domínio do Active Directory usando as credenciais administrativas do usuário.</span><span class="sxs-lookup"><span data-stu-id="79158-187">This protocol enables the Windows PowerShell cmdlets to connect to Active Directory Domain Services by using the user’s administrative credentials.</span></span> <span data-ttu-id="79158-188">Você pode receber um erro de validação se iniciar a sessão do Windows PowerShell sem esse protocolo.</span><span class="sxs-lookup"><span data-stu-id="79158-188">You might get a validation error if you start the Windows PowerShell session without this protocol.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="79158-189">Como iniciar uma sessão do Windows PowerShell com o protocolo CredSSP</span><span class="sxs-lookup"><span data-stu-id="79158-189">How to start a Windows PowerShell session with the CredSSP protocol</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="79158-190">Digite o seguinte código no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="79158-190">Type the following code at the Windows PowerShell prompt:</span></span></p>
<p><code>$s = New-PSSession -ComputerName xxx -Authentication Credssp -Credential xxx</code></p>
<p><span data-ttu-id="79158-191">O código a seguir mostra um exemplo.</span><span class="sxs-lookup"><span data-stu-id="79158-191">The following code shows an example.</span></span></p>
<p><code>$session = New-PSSession -ComputerName &lt;MBAM_server_name&gt; -Authentication Credssp -Credential (Get-Credential)</code></p>
<p><code>Enter-PSSession $session</code></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqd-posh-accts"></a><span data-ttu-id="79158-192">Contas necessárias e parâmetros do cmdlet do Windows PowerShell correspondentes</span><span class="sxs-lookup"><span data-stu-id="79158-192">Required accounts and corresponding Windows PowerShell cmdlet parameters</span></span>


<span data-ttu-id="79158-193">A tabela a seguir descreve as contas necessárias para configurar os recursos do MBAM 2,5 Server.</span><span class="sxs-lookup"><span data-stu-id="79158-193">The following table describes the accounts that are required to configure MBAM 2.5 Server features.</span></span> <span data-ttu-id="79158-194">Ele também lista o cmdlet e o parâmetro do Windows PowerShell correspondente para o qual você precisa especificar a conta durante a configuração.</span><span class="sxs-lookup"><span data-stu-id="79158-194">It also lists the corresponding Windows PowerShell cmdlet and parameter for which you have to specify the account during configuration.</span></span>

<span data-ttu-id="79158-195">Tipo de parâmetro cmdlet (usuário ou grupo) Descrição Enable-MBAMDatabase</span><span class="sxs-lookup"><span data-stu-id="79158-195">Cmdlet Parameter Type (User or Group) Description Enable-MBAMDatabase</span></span>

<span data-ttu-id="79158-196">AccessAccount</span><span class="sxs-lookup"><span data-stu-id="79158-196">AccessAccount</span></span>

<span data-ttu-id="79158-197">Usuário ou grupo</span><span class="sxs-lookup"><span data-stu-id="79158-197">User or Group</span></span>

<span data-ttu-id="79158-198">Especifique um usuário ou grupo de domínio que tenha permissão de leitura/gravação para esse banco de dados para dar aos aplicativos Web acesso a dados e relatórios nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="79158-198">Specify a domain user or group that has read/write permission to this database to give the web applications access to data and reports in this database.</span></span> <span data-ttu-id="79158-199">Se o valor for um usuário de domínio, o parâmetro **WebServiceApplicationPoolCredential** usado ao executar o cmdlet **Enable-MbamWebApplication** deve usar a mesma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="79158-199">If the value is a domain user, then the **WebServiceApplicationPoolCredential** parameter that is used when running the **Enable-MbamWebApplication** cmdlet must use the same user account.</span></span> <span data-ttu-id="79158-200">Se o valor for um grupo usuários do domínio, a conta de domínio que é usada pelo parâmetro **WebServiceApplicationPoolCredential** deve ser um membro desse grupo.</span><span class="sxs-lookup"><span data-stu-id="79158-200">If the value is a domain Users group, then the domain account that is used by the **WebServiceApplicationPoolCredential** parameter must be a member of this group.</span></span>

<span data-ttu-id="79158-201">ReportAccount</span><span class="sxs-lookup"><span data-stu-id="79158-201">ReportAccount</span></span>

<span data-ttu-id="79158-202">Usuário ou grupo</span><span class="sxs-lookup"><span data-stu-id="79158-202">User or Group</span></span>

<span data-ttu-id="79158-203">Especifique um grupo de usuários de domínio ou de usuário com permissão somente leitura para esse banco de dados para fornecer ao MBAM relatórios acesso aos dados de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="79158-203">Specify a domain user or Users group that has read-only permission to this database to provide the MBAM reports access to the compliance and audit data.</span></span> <span data-ttu-id="79158-204">Se o valor for um usuário de domínio, o parâmetro **ComplianceAndAuditDBCredential** do cmdlet **Enable-MbamReport** deve usar a mesma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="79158-204">If the value is a domain user, then the **ComplianceAndAuditDBCredential** parameter of the **Enable-MbamReport** cmdlet must use the same user account.</span></span> <span data-ttu-id="79158-205">Se o valor for um grupo usuários do domínio, a conta de domínio que é usada pelo parâmetro **ComplianceAndAuditDBCredential** deve ser um membro desse grupo.</span><span class="sxs-lookup"><span data-stu-id="79158-205">If the value is a domain Users group, then the domain account that is used by the **ComplianceAndAuditDBCredential** parameter must be a member of this group.</span></span>

<span data-ttu-id="79158-206">Enable-MbamReport</span><span class="sxs-lookup"><span data-stu-id="79158-206">Enable-MbamReport</span></span>

<span data-ttu-id="79158-207">ComplianceAndAuditDBCredential</span><span class="sxs-lookup"><span data-stu-id="79158-207">ComplianceAndAuditDBCredential</span></span>

<span data-ttu-id="79158-208">Usuário</span><span class="sxs-lookup"><span data-stu-id="79158-208">User</span></span>

<span data-ttu-id="79158-209">Especifica as credenciais administrativas que a instância do SSRS local usa para se conectar ao banco de dados de auditoria e conformidade do MBAM.</span><span class="sxs-lookup"><span data-stu-id="79158-209">Specifies the administrative credential that the local SSRS instance uses to connect to the MBAM Compliance and Audit Database.</span></span> <span data-ttu-id="79158-210">O usuário do domínio na credencial administrativa deve ser o mesmo que a conta de usuário que é usada para o parâmetro **ReportAccount** , que é usado durante a execução do cmdlet **Enable-MbamDatabase** .</span><span class="sxs-lookup"><span data-stu-id="79158-210">The domain user in the administrative credential must be the same as the user account that is used for the **ReportAccount** parameter, which is used while running the **Enable-MbamDatabase** cmdlet.</span></span> <span data-ttu-id="79158-211">Se um grupo de usuários de domínio foi usado com o parâmetro **ReportAccount** , essa conta deve ser membro desse grupo.</span><span class="sxs-lookup"><span data-stu-id="79158-211">If a domain Users group was used with the **ReportAccount** parameter, this account should be a member of that group.</span></span>

<span data-ttu-id="79158-212">**Importante**  A conta especificada nas credenciais administrativas deve ter direitos de usuário limitados para melhorar a segurança.</span><span class="sxs-lookup"><span data-stu-id="79158-212">**Important** The account specified in the administrative credentials should have limited user rights for improved security.</span></span> <span data-ttu-id="79158-213">Além disso, a senha da conta deve ser definida como não expirar.</span><span class="sxs-lookup"><span data-stu-id="79158-213">Also, the password of the account should be set to not expire.</span></span>

 

<span data-ttu-id="79158-214">ReportsReadOnlyAccessGroup</span><span class="sxs-lookup"><span data-stu-id="79158-214">ReportsReadOnlyAccessGroup</span></span>

<span data-ttu-id="79158-215">Grupo</span><span class="sxs-lookup"><span data-stu-id="79158-215">Group</span></span>

<span data-ttu-id="79158-216">Especifica o grupo de usuários do domínio que tem permissões de leitura para os relatórios.</span><span class="sxs-lookup"><span data-stu-id="79158-216">Specifies the domain user group that has read permissions to the reports.</span></span> <span data-ttu-id="79158-217">O grupo especificado deve ser o mesmo grupo usado para o parâmetro **ReportsReadOnlyAccessGroup** no cmdlet **Enable-MbamWebApplication** .</span><span class="sxs-lookup"><span data-stu-id="79158-217">The specified group must be the same group that is used for the **ReportsReadOnlyAccessGroup** parameter in the **Enable-MbamWebApplication** cmdlet.</span></span>

<span data-ttu-id="79158-218">Enable-MBAMWebApplication</span><span class="sxs-lookup"><span data-stu-id="79158-218">Enable-MBAMWebApplication</span></span>

<span data-ttu-id="79158-219">AdvancedHelpdeskAccessGroup</span><span class="sxs-lookup"><span data-stu-id="79158-219">AdvancedHelpdeskAccessGroup</span></span>

<span data-ttu-id="79158-220">Grupo</span><span class="sxs-lookup"><span data-stu-id="79158-220">Group</span></span>

<span data-ttu-id="79158-221">Especifica o grupo usuários do domínio que tem acesso a todas as áreas do site de administração e monitoramento, exceto à área relatórios.</span><span class="sxs-lookup"><span data-stu-id="79158-221">Specifies the domain Users group that has access to all areas of the Administration and Monitoring Website except the Reports area.</span></span>

<span data-ttu-id="79158-222">HelpdeskAccessGroup</span><span class="sxs-lookup"><span data-stu-id="79158-222">HelpdeskAccessGroup</span></span>

<span data-ttu-id="79158-223">Grupo</span><span class="sxs-lookup"><span data-stu-id="79158-223">Group</span></span>

<span data-ttu-id="79158-224">Especifica o grupo usuários do domínio que tem acesso às áreas **gerenciar TPM** e **unidade de recuperação** do site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="79158-224">Specifies the domain Users group that has access to the **Manage TPM** and **Drive Recovery** areas of the Administration and Monitoring Website.</span></span>

<span data-ttu-id="79158-225">ReportsReadOnlyAccessGroup</span><span class="sxs-lookup"><span data-stu-id="79158-225">ReportsReadOnlyAccessGroup</span></span>

<span data-ttu-id="79158-226">Grupo</span><span class="sxs-lookup"><span data-stu-id="79158-226">Group</span></span>

<span data-ttu-id="79158-227">Especifica o grupo usuários do domínio que tem permissão de leitura para a área **relatórios** do site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="79158-227">Specifies the domain Users group that has read permission to the **Reports** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="79158-228">O grupo especificado deve ser o mesmo grupo usado para o parâmetro **ReportsReadOnlyAccessGroup** no cmdlet **Enable-MbamReport** .</span><span class="sxs-lookup"><span data-stu-id="79158-228">The specified group must be the same group that is used for the **ReportsReadOnlyAccessGroup** parameter in the **Enable-MbamReport** cmdlet.</span></span>

<span data-ttu-id="79158-229">WebServiceApplicationPoolCredential</span><span class="sxs-lookup"><span data-stu-id="79158-229">WebServiceApplicationPoolCredential</span></span>

<span data-ttu-id="79158-230">Usuário</span><span class="sxs-lookup"><span data-stu-id="79158-230">User</span></span>

<span data-ttu-id="79158-231">Especifica o usuário do domínio a ser usado pelo pool de aplicativos para os aplicativos Web do MBAM.</span><span class="sxs-lookup"><span data-stu-id="79158-231">Specifies the domain user to be used by the application pool for the MBAM web applications.</span></span> <span data-ttu-id="79158-232">Ele deve ser a mesma conta de usuário de domínio especificada no parâmetro **AccessAccount** do cmdlet **Enable-MbamDatabase** .</span><span class="sxs-lookup"><span data-stu-id="79158-232">It must be the same domain user account that is specified in the **AccessAccount** parameter of the **Enable-MbamDatabase** cmdlet.</span></span> <span data-ttu-id="79158-233">Se um grupo de usuários do domínio foi usado pelo parâmetro **AccessAccount** ao executar o cmdlet **Enable-MbamDatabase** , o usuário do domínio especificado aqui deve ser um membro desse grupo.</span><span class="sxs-lookup"><span data-stu-id="79158-233">If a domain Users group was used by the **AccessAccount** parameter when running the **Enable-MbamDatabase** cmdlet, the domain user that is specified here must be a member of that group.</span></span> <span data-ttu-id="79158-234">Se você não especificar as credenciais administrativas, as credenciais administrativas que foram especificadas por qualquer aplicativo da Web habilitado anteriormente serão usadas.</span><span class="sxs-lookup"><span data-stu-id="79158-234">If you do not specify the administrative credentials, the administrative credentials that were specified by any previously enabled web application are used.</span></span> <span data-ttu-id="79158-235">Todos os aplicativos da Web usam a mesma identidade do pool de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="79158-235">All of the web applications use the same application pool identity.</span></span> <span data-ttu-id="79158-236">Se for especificado várias vezes, o valor especificado mais recentemente será usado.</span><span class="sxs-lookup"><span data-stu-id="79158-236">If it is specified multiple times, the most recently specified value is used.</span></span>

<span data-ttu-id="79158-237">**Importante**  Para aumentar a segurança, defina a conta especificada nas credenciais administrativas para direitos de usuário limitados.</span><span class="sxs-lookup"><span data-stu-id="79158-237">**Important** For improved security, set the account that is specified in the administrative credentials to limited user rights.</span></span> <span data-ttu-id="79158-238">Além disso, defina a senha da conta para nunca expirar.</span><span class="sxs-lookup"><span data-stu-id="79158-238">Also, set the password of the account to never expire.</span></span> <span data-ttu-id="79158-239">Verifique se a conta interna do IIS \ _IUSRS ou a conta que é usada para o parâmetro **WebServiceApplicationPoolCredential** foi adicionada à configuração de segurança **representar um cliente após autenticação** local.</span><span class="sxs-lookup"><span data-stu-id="79158-239">Ensure that either the built-in IIS\_IUSRS account or the account that is used for the **WebServiceApplicationPoolCredential** parameter has been added to the **Impersonate a client after authentication** local security setting.</span></span>

<span data-ttu-id="79158-240">Para exibir a configuração de segurança local, abra o **Editor de política de segurança local**, expanda o nó **políticas locais** , selecione o nó **atribuição de direitos de usuário** e, em seguida, clique duas vezes na opção **representar um cliente após autenticação** e **fazer logon como um trabalho em lotes** em configurações de política de grupo no painel detalhes.</span><span class="sxs-lookup"><span data-stu-id="79158-240">To view the local security setting, open the **Local Security Policy editor**, expand the **Local Policies** node, select the **User Rights Assignment** node, and then double-click the **Impersonate a client after authentication** and **Log on as a batch job** Group Policy settings in the details pane.</span></span>

 

 




## <span data-ttu-id="79158-241">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="79158-241">Related topics</span></span>


[<span data-ttu-id="79158-242">Configurando os recursos de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="79158-242">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="79158-243">Validando a configuração de recursos de servidor do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="79158-243">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)

[<span data-ttu-id="79158-244">Usando o Windows PowerShell para administrar o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="79158-244">Using Windows PowerShell to Administer MBAM 2.5</span></span>](using-windows-powershell-to-administer-mbam-25.md)

 
## <span data-ttu-id="79158-245">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="79158-245">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="79158-246">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="79158-246">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="79158-247">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="79158-247">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





