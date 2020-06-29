---
title: Como gerenciar pacotes do App-V 5.0 em execução em um computador autônomo usando o PowerShell
description: Como gerenciar pacotes do App-V 5.0 em execução em um computador autônomo usando o PowerShell
author: dansimp
ms.assetid: 1d6c2d25-81ec-4ff8-9262-6b4cf484a376
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b7af1781a7a443a4fcfc8e7d4a92525b34986763
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796370"
---
# <span data-ttu-id="e2979-103">Como gerenciar pacotes do App-V 5.0 em execução em um computador autônomo usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="e2979-103">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span>


<span data-ttu-id="e2979-104">As seções a seguir explicam como executar várias tarefas de gerenciamento em um computador cliente autônomo usando o PowerShell:</span><span class="sxs-lookup"><span data-stu-id="e2979-104">The following sections explain how to perform various management tasks on a stand-alone client computer by using PowerShell:</span></span>

-   [<span data-ttu-id="e2979-105">Para retornar uma lista de pacotes</span><span class="sxs-lookup"><span data-stu-id="e2979-105">To return a list of packages</span></span>](#bkmk-return-pkgs-standalone-posh)

-   [<span data-ttu-id="e2979-106">Para adicionar um pacote</span><span class="sxs-lookup"><span data-stu-id="e2979-106">To add a package</span></span>](#bkmk-add-pkgs-standalone-posh)

-   [<span data-ttu-id="e2979-107">Para publicar um pacote</span><span class="sxs-lookup"><span data-stu-id="e2979-107">To publish a package</span></span>](#bkmk-pub-pkg-standalone-posh)

-   [<span data-ttu-id="e2979-108">Para publicar um pacote para um usuário específico</span><span class="sxs-lookup"><span data-stu-id="e2979-108">To publish a package to a specific user</span></span>](#bkmk-pub-pkg-a-user-standalone-posh)

-   [<span data-ttu-id="e2979-109">Para adicionar e publicar um pacote</span><span class="sxs-lookup"><span data-stu-id="e2979-109">To add and publish a package</span></span>](#bkmk-add-pub-pkg-standalone-posh)

-   [<span data-ttu-id="e2979-110">Para cancelar a publicação de um pacote existente</span><span class="sxs-lookup"><span data-stu-id="e2979-110">To unpublish an existing package</span></span>](#bkmk-unpub-pkg-standalone-posh)

-   [<span data-ttu-id="e2979-111">Para cancelar a publicação de um pacote para um usuário específico</span><span class="sxs-lookup"><span data-stu-id="e2979-111">To unpublish a package for a specific user</span></span>](#bkmk-unpub-pkg-specfc-use)

-   [<span data-ttu-id="e2979-112">Para remover um pacote existente</span><span class="sxs-lookup"><span data-stu-id="e2979-112">To remove an existing package</span></span>](#bkmk-remove-pkg-standalone-posh)

-   [<span data-ttu-id="e2979-113">Para habilitar apenas os administradores a publicar ou cancelar a publicação de pacotes</span><span class="sxs-lookup"><span data-stu-id="e2979-113">To enable only administrators to publish or unpublish packages</span></span>](#bkmk-admins-pub-pkgs)

-   [<span data-ttu-id="e2979-114">Noções básicas sobre pacotes pendentes (userpending e GlobalPending)</span><span class="sxs-lookup"><span data-stu-id="e2979-114">Understanding pending packages (UserPending and GlobalPending)</span></span>](#bkmk-understd-pend-pkgs)

## <a href="" id="bkmk-return-pkgs-standalone-posh"></a><span data-ttu-id="e2979-115">Para retornar uma lista de pacotes</span><span class="sxs-lookup"><span data-stu-id="e2979-115">To return a list of packages</span></span>


<span data-ttu-id="e2979-116">Use as informações a seguir para retornar uma lista de pacotes que têm direito a um usuário específico:</span><span class="sxs-lookup"><span data-stu-id="e2979-116">Use the following information to return a list of packages that are entitled to a specific user:</span></span>

<span data-ttu-id="e2979-117">**Cmdlet**: Get-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="e2979-117">**Cmdlet**: Get-AppvClientPackage</span></span>

<span data-ttu-id="e2979-118">**Parâmetros**:-Name-Version-PackageID-VersionId</span><span class="sxs-lookup"><span data-stu-id="e2979-118">**Parameters**: -Name -Version -PackageID -VersionID</span></span>

<span data-ttu-id="e2979-119">**Exemplo**: Get-AppvClientPackage-Name "ContosoApplication"-versão 2</span><span class="sxs-lookup"><span data-stu-id="e2979-119">**Example**: Get-AppvClientPackage –Name “ContosoApplication” -Version 2</span></span>

## <a href="" id="bkmk-add-pkgs-standalone-posh"></a><span data-ttu-id="e2979-120">Para adicionar um pacote</span><span class="sxs-lookup"><span data-stu-id="e2979-120">To add a package</span></span>


<span data-ttu-id="e2979-121">Use as informações a seguir para adicionar um pacote a um computador.</span><span class="sxs-lookup"><span data-stu-id="e2979-121">Use the following information to add a package to a computer.</span></span>

<span data-ttu-id="e2979-122">**Importante**  Este exemplo adiciona apenas um pacote.</span><span class="sxs-lookup"><span data-stu-id="e2979-122">**Important** This example only adds a package.</span></span> <span data-ttu-id="e2979-123">Ele não publica o pacote no usuário ou no computador.</span><span class="sxs-lookup"><span data-stu-id="e2979-123">It does not publish the package to the user or the computer.</span></span>

 

<span data-ttu-id="e2979-124">**Cmdlet**: Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="e2979-124">**Cmdlet**: Add-AppvClientPackage</span></span>

<span data-ttu-id="e2979-125">**Exemplo**: $contoso = Add-AppvClientPackage \\\\path\\to\\appv\\package.AppV</span><span class="sxs-lookup"><span data-stu-id="e2979-125">**Example**: $Contoso = Add-AppvClientPackage \\\\path\\to\\appv\\package.appv</span></span>

## <a href="" id="bkmk-pub-pkg-standalone-posh"></a><span data-ttu-id="e2979-126">Para publicar um pacote</span><span class="sxs-lookup"><span data-stu-id="e2979-126">To publish a package</span></span>


<span data-ttu-id="e2979-127">Use as informações a seguir para publicar um pacote que foi adicionado a um usuário específico ou globalmente para qualquer usuário do computador.</span><span class="sxs-lookup"><span data-stu-id="e2979-127">Use the following information to publish a package that has been added to a specific user or globally to any user on the computer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e2979-128">Método de publicação</span><span class="sxs-lookup"><span data-stu-id="e2979-128">Publishing method</span></span></th>
<th align="left"><span data-ttu-id="e2979-129">Cmdlet e exemplo</span><span class="sxs-lookup"><span data-stu-id="e2979-129">Cmdlet and example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e2979-130">Publicação para o usuário</span><span class="sxs-lookup"><span data-stu-id="e2979-130">Publishing to the user</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="e2979-131">Cmdlet </strong> : publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="e2979-131">Cmdlet</strong>: Publish-AppvClientPackage</span></span></p>
<p><strong><span data-ttu-id="e2979-132">Exemplo </strong> : publish-AppvClientPackage "ContosoApplication"</span><span class="sxs-lookup"><span data-stu-id="e2979-132">Example</strong>: Publish-AppvClientPackage “ContosoApplication”</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e2979-133">Publicação global</span><span class="sxs-lookup"><span data-stu-id="e2979-133">Publishing globally</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="e2979-134">Cmdlet </strong> : publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="e2979-134">Cmdlet</strong>: Publish-AppvClientPackage</span></span></p>
<p><strong><span data-ttu-id="e2979-135">Exemplo </strong> : publish-AppvClientPackage "ContosoApplication"-global</span><span class="sxs-lookup"><span data-stu-id="e2979-135">Example</strong>: Publish-AppvClientPackage “ContosoApplication” -Global</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-pub-pkg-a-user-standalone-posh"></a><span data-ttu-id="e2979-136">Para publicar um pacote para um usuário específico</span><span class="sxs-lookup"><span data-stu-id="e2979-136">To publish a package to a specific user</span></span>


<span data-ttu-id="e2979-137">**Observação**  Você deve usar o pacote de hotfix do App-V 5,0 SP2 5 ou posterior para usar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e2979-137">**Note** You must use App-V 5.0 SP2 Hotfix Package 5 or later to use this parameter.</span></span>

 

<span data-ttu-id="e2979-138">Um administrador pode publicar um pacote para um usuário específico especificando o parâmetro opcional **– userid** com o cmdlet **Publish-AppvClientPackage** , em que **-userid** representa o Sid (identificador de segurança) do usuário final.</span><span class="sxs-lookup"><span data-stu-id="e2979-138">An administrator can publish a package to a specific user by specifying the optional **–UserSID** parameter with the **Publish-AppvClientPackage** cmdlet, where **-UserSID** represents the end user’s security identifier (SID).</span></span>

<span data-ttu-id="e2979-139">Para usar esse parâmetro:</span><span class="sxs-lookup"><span data-stu-id="e2979-139">To use this parameter:</span></span>

-   <span data-ttu-id="e2979-140">Você pode executar esse cmdlet a partir da sessão de usuário ou de administrador.</span><span class="sxs-lookup"><span data-stu-id="e2979-140">You can run this cmdlet from the user or administrator session.</span></span>

-   <span data-ttu-id="e2979-141">Você deve estar conectado com credenciais administrativas para usar o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e2979-141">You must be logged in with administrative credentials to use the parameter.</span></span>

-   <span data-ttu-id="e2979-142">O usuário final deve estar conectado.</span><span class="sxs-lookup"><span data-stu-id="e2979-142">The end user must be logged in.</span></span>

-   <span data-ttu-id="e2979-143">Você deve fornecer o SID (identificador de segurança) do usuário final.</span><span class="sxs-lookup"><span data-stu-id="e2979-143">You must provide the end user’s security identifier (SID).</span></span>

<span data-ttu-id="e2979-144">**Cmdlet**: publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="e2979-144">**Cmdlet**: Publish-AppvClientPackage</span></span>

<span data-ttu-id="e2979-145">**Exemplo**: publish-AppvClientPackage "ContosoApplication"-usuáriosid S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="e2979-145">**Example**: Publish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span>

## <a href="" id="bkmk-add-pub-pkg-standalone-posh"></a><span data-ttu-id="e2979-146">Para adicionar e publicar um pacote</span><span class="sxs-lookup"><span data-stu-id="e2979-146">To add and publish a package</span></span>


<span data-ttu-id="e2979-147">Use as informações a seguir para adicionar um pacote a um computador e publicá-lo para o usuário.</span><span class="sxs-lookup"><span data-stu-id="e2979-147">Use the following information to add a package to a computer and publish it to the user.</span></span>

<span data-ttu-id="e2979-148">**Cmdlet**: Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="e2979-148">**Cmdlet**: Add-AppvClientPackage</span></span>

<span data-ttu-id="e2979-149">**Exemplo**: Add-AppvClientPackage \\\\path\\to\\appv\\package.AppV | Publicar-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="e2979-149">**Example**: Add-AppvClientPackage \\\\path\\to\\appv\\package.appv | Publish-AppvClientPackage</span></span>

## <a href="" id="bkmk-unpub-pkg-standalone-posh"></a><span data-ttu-id="e2979-150">Para cancelar a publicação de um pacote existente</span><span class="sxs-lookup"><span data-stu-id="e2979-150">To unpublish an existing package</span></span>


<span data-ttu-id="e2979-151">Use as informações a seguir para cancelar a publicação de um pacote que tenha sido qualificado para um usuário, mas não remova o pacote do computador.</span><span class="sxs-lookup"><span data-stu-id="e2979-151">Use the following information to unpublish a package which has been entitled to a user but not remove the package from the computer.</span></span>

<span data-ttu-id="e2979-152">**Cmdlet**: cancelar publicação-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="e2979-152">**Cmdlet**: Unpublish-AppvClientPackage</span></span>

<span data-ttu-id="e2979-153">**Exemplo**: cancelar publicação-AppvClientPackage "ContosoApplication"</span><span class="sxs-lookup"><span data-stu-id="e2979-153">**Example**: Unpublish-AppvClientPackage “ContosoApplication”</span></span>

## <a href="" id="bkmk-unpub-pkg-specfc-use"></a><span data-ttu-id="e2979-154">Para cancelar a publicação de um pacote para um usuário específico</span><span class="sxs-lookup"><span data-stu-id="e2979-154">To unpublish a package for a specific user</span></span>


<span data-ttu-id="e2979-155">**Observação**  Você deve usar o pacote de hotfix do App-V 5,0 SP2 5 ou posterior para usar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e2979-155">**Note** You must use App-V 5.0 SP2 Hotfix Package 5 or later to use this parameter.</span></span>

 

<span data-ttu-id="e2979-156">Um administrador pode cancelar a publicação de um pacote para um usuário específico usando o parâmetro opcional **– userid** com o cmdlet **UNPUBLISH-AppvClientPackage** , em que **-userid** representa o Sid (identificador de segurança) do usuário final.</span><span class="sxs-lookup"><span data-stu-id="e2979-156">An administrator can unpublish a package for a specific user by using the optional **–UserSID** parameter with the **Unpublish-AppvClientPackage** cmdlet, where **-UserSID** represents the end user’s security identifier (SID).</span></span>

<span data-ttu-id="e2979-157">Para usar esse parâmetro:</span><span class="sxs-lookup"><span data-stu-id="e2979-157">To use this parameter:</span></span>

-   <span data-ttu-id="e2979-158">Você pode executar esse cmdlet a partir da sessão de usuário ou de administrador.</span><span class="sxs-lookup"><span data-stu-id="e2979-158">You can run this cmdlet from the user or administrator session.</span></span>

-   <span data-ttu-id="e2979-159">Você deve estar conectado com credenciais administrativas para usar o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e2979-159">You must be logged in with administrative credentials to use the parameter.</span></span>

-   <span data-ttu-id="e2979-160">O usuário final deve estar conectado.</span><span class="sxs-lookup"><span data-stu-id="e2979-160">The end user must be logged in.</span></span>

-   <span data-ttu-id="e2979-161">Você deve fornecer o SID (identificador de segurança) do usuário final.</span><span class="sxs-lookup"><span data-stu-id="e2979-161">You must provide the end user’s security identifier (SID).</span></span>

<span data-ttu-id="e2979-162">**Cmdlet**: cancelar publicação-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="e2979-162">**Cmdlet**: Unpublish-AppvClientPackage</span></span>

<span data-ttu-id="e2979-163">**Exemplo**: cancelar publicação-AppvClientPackage "ContosoApplication"-usuáriosid S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="e2979-163">**Example**: Unpublish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span>

## <a href="" id="bkmk-remove-pkg-standalone-posh"></a><span data-ttu-id="e2979-164">Para remover um pacote existente</span><span class="sxs-lookup"><span data-stu-id="e2979-164">To remove an existing package</span></span>


<span data-ttu-id="e2979-165">Use as informações a seguir para remover um pacote do computador.</span><span class="sxs-lookup"><span data-stu-id="e2979-165">Use the following information to remove a package from the computer.</span></span>

<span data-ttu-id="e2979-166">**Cmdlet**: Remove-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="e2979-166">**Cmdlet**: Remove-AppvClientPackage</span></span>

<span data-ttu-id="e2979-167">**Exemplo**: Remove-AppvClientPackage "ContosoApplication"</span><span class="sxs-lookup"><span data-stu-id="e2979-167">**Example**: Remove-AppvClientPackage “ContosoApplication”</span></span>

<span data-ttu-id="e2979-168">**Observação**  Cmdlets do App-V foram atribuídos a variáveis para os exemplos anteriores somente para fins de esclarecimento; a atribuição não é um requisito.</span><span class="sxs-lookup"><span data-stu-id="e2979-168">**Note** App-V cmdlets have been assigned to variables for the previous examples for clarity only; assignment is not a requirement.</span></span> <span data-ttu-id="e2979-169">A maioria dos cmdlets pode ser combinada conforme exibido em [para adicionar e publicar um pacote](#bkmk-add-pub-pkg-standalone-posh).</span><span class="sxs-lookup"><span data-stu-id="e2979-169">Most cmdlets can be combined as displayed in [To add and publish a package](#bkmk-add-pub-pkg-standalone-posh).</span></span> <span data-ttu-id="e2979-170">Para obter um tutorial detalhado, consulte o [App-V 5,0 Client do PowerShell DeepShip](https://go.microsoft.com/fwlink/?LinkId=324466).</span><span class="sxs-lookup"><span data-stu-id="e2979-170">For a detailed tutorial, see [App-V 5.0 Client PowerShell Deep Dive](https://go.microsoft.com/fwlink/?LinkId=324466).</span></span>

 

## <a href="" id="bkmk-admins-pub-pkgs"></a><span data-ttu-id="e2979-171">Para habilitar apenas os administradores a publicar ou cancelar a publicação de pacotes</span><span class="sxs-lookup"><span data-stu-id="e2979-171">To enable only administrators to publish or unpublish packages</span></span>


<span data-ttu-id="e2979-172">**Observação** 
 **Este recurso tem suporte a partir do App-V 5,0 SP3.**</span><span class="sxs-lookup"><span data-stu-id="e2979-172">**Note**
**This feature is supported starting in App-V 5.0 SP3.**</span></span>

 

<span data-ttu-id="e2979-173">Use o cmdlet e o parâmetro a seguir para habilitar somente administradores (não usuários finais) para publicar ou cancelar a publicação de pacotes:</span><span class="sxs-lookup"><span data-stu-id="e2979-173">Use the following cmdlet and parameter to enable only administrators (not end users) to publish or unpublish packages:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e2979-174">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e2979-174">Cmdlet</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e2979-175">Set-AppvClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2979-175">Set-AppvClientConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e2979-176">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2979-176">Parameter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e2979-177">-RequirePublishAsAdmin</span><span class="sxs-lookup"><span data-stu-id="e2979-177">-RequirePublishAsAdmin</span></span></p>
<p><span data-ttu-id="e2979-178">Valores de parâmetro:</span><span class="sxs-lookup"><span data-stu-id="e2979-178">Parameter values:</span></span></p>
<ul>
<li><p><span data-ttu-id="e2979-179">0-falso</span><span class="sxs-lookup"><span data-stu-id="e2979-179">0 - False</span></span></p></li>
<li><p><span data-ttu-id="e2979-180">1-verdadeiro</span><span class="sxs-lookup"><span data-stu-id="e2979-180">1 - True</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="e2979-181">Exemplo: </strong> : Set-AppvClientConfiguration – RequirePublishAsAdmin1</span><span class="sxs-lookup"><span data-stu-id="e2979-181">Example:</strong>: Set-AppvClientConfiguration –RequirePublishAsAdmin1</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e2979-182">Para usar o console de gerenciamento do App-V para definir essa configuração, consulte [como publicar um pacote usando o console de gerenciamento](how-to-publish-a-package-by-using-the-management-console-50.md).</span><span class="sxs-lookup"><span data-stu-id="e2979-182">To use the App-V Management console to set this configuration, see [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md).</span></span>

## <a href="" id="bkmk-understd-pend-pkgs"></a><span data-ttu-id="e2979-183">Noções básicas sobre pacotes pendentes (userpending e GlobalPending)</span><span class="sxs-lookup"><span data-stu-id="e2979-183">Understanding pending packages (UserPending and GlobalPending)</span></span>


<span data-ttu-id="e2979-184">A **partir do App-V 5,0 SP2**: se você executar um cmdlet do PowerShell que afeta um pacote que está em uso no momento, a tarefa que você está tentando executar é colocada em um estado pendente.</span><span class="sxs-lookup"><span data-stu-id="e2979-184">**Starting in App-V 5.0 SP2**: If you run a PowerShell cmdlet that affects a package that is currently in use, the task that you are trying to perform is placed in a pending state.</span></span> <span data-ttu-id="e2979-185">Por exemplo, se você tentar publicar um pacote quando um aplicativo nesse pacote estiver sendo usado e executar **Get-AppvClientPackage**, o status pendente será exibido na saída do cmdlet da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e2979-185">For example, if you try to publish a package when an application in that package is being used, and then run **Get-AppvClientPackage**, the pending status appears in the cmdlet output as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e2979-186">Item de saída do cmdlet</span><span class="sxs-lookup"><span data-stu-id="e2979-186">Cmdlet output item</span></span></th>
<th align="left"><span data-ttu-id="e2979-187">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2979-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e2979-188">Userpending</span><span class="sxs-lookup"><span data-stu-id="e2979-188">UserPending</span></span></p></td>
<td align="left"><p><span data-ttu-id="e2979-189">Indica se o pacote listado tem uma tarefa pendente que está sendo aplicada ao usuário:</span><span class="sxs-lookup"><span data-stu-id="e2979-189">Indicates whether the listed package has a pending task that is being applied to the user:</span></span></p>
<ul>
<li><p><span data-ttu-id="e2979-190">True</span><span class="sxs-lookup"><span data-stu-id="e2979-190">True</span></span></p></li>
<li><p><span data-ttu-id="e2979-191">False</span><span class="sxs-lookup"><span data-stu-id="e2979-191">False</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e2979-192">GlobalPending</span><span class="sxs-lookup"><span data-stu-id="e2979-192">GlobalPending</span></span></p></td>
<td align="left"><p><span data-ttu-id="e2979-193">Indica se o pacote listado tem uma tarefa pendente que está sendo aplicada globalmente ao computador:</span><span class="sxs-lookup"><span data-stu-id="e2979-193">Indicates whether the listed package has a pending task that is being applied globally to the computer:</span></span></p>
<ul>
<li><p><span data-ttu-id="e2979-194">True</span><span class="sxs-lookup"><span data-stu-id="e2979-194">True</span></span></p></li>
<li><p><span data-ttu-id="e2979-195">False</span><span class="sxs-lookup"><span data-stu-id="e2979-195">False</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e2979-196">A tarefa pendente será executada mais tarde, de acordo com as seguintes regras:</span><span class="sxs-lookup"><span data-stu-id="e2979-196">The pending task will run later, according to the following rules:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e2979-197">Tipo de tarefa</span><span class="sxs-lookup"><span data-stu-id="e2979-197">Task type</span></span></th>
<th align="left"><span data-ttu-id="e2979-198">Regra aplicável</span><span class="sxs-lookup"><span data-stu-id="e2979-198">Applicable rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e2979-199">Tarefa baseada em usuário, por exemplo, publicar um pacote para um usuário</span><span class="sxs-lookup"><span data-stu-id="e2979-199">User-based task, e.g., publishing a package to a user</span></span></p></td>
<td align="left"><p><span data-ttu-id="e2979-200">A tarefa pendente será executada após o usuário fazer logoff e, em seguida, fazer logon novamente.</span><span class="sxs-lookup"><span data-stu-id="e2979-200">The pending task will be performed after the user logs off and then logs back on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e2979-201">Tarefa com base global, por exemplo, habilitar um grupo de conexão globalmente</span><span class="sxs-lookup"><span data-stu-id="e2979-201">Globally based task, e.g., enabling a connection group globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="e2979-202">A tarefa pendente será executada quando o computador for desligado e reiniciado.</span><span class="sxs-lookup"><span data-stu-id="e2979-202">The pending task will be performed when the computer is shut down and then restarted.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e2979-203">Para obter mais informações sobre tarefas pendentes, consulte [sobre o App-V 5,0 SP2](about-app-v-50-sp2.md#bkmk-pkg-upgr-pendg-tasks).</span><span class="sxs-lookup"><span data-stu-id="e2979-203">For more information about pending tasks, see [About App-V 5.0 SP2](about-app-v-50-sp2.md#bkmk-pkg-upgr-pendg-tasks).</span></span>

<span data-ttu-id="e2979-204">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="e2979-204">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="e2979-205">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="e2979-205">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="e2979-206">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="e2979-206">Got an App-V issue?</span></span>** <span data-ttu-id="e2979-207">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="e2979-207">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="e2979-208">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2979-208">Related topics</span></span>


[<span data-ttu-id="e2979-209">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="e2979-209">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="e2979-210">Administração do App-V usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="e2979-210">Administering App-V by Using PowerShell</span></span>](administering-app-v-by-using-powershell.md)

 

 





