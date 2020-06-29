---
title: Gerenciando modelos de localização de configurações do UE-V 2. x usando o Windows PowerShell e o WMI
description: Gerenciando modelos de localização de configurações do UE-V 2. x usando o Windows PowerShell e o WMI
author: dansimp
ms.assetid: b5253050-acc3-4274-90d0-1fa4c480331d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9788ff1a11f1c70e52b75dd2187a198f5472f77f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796110"
---
# <span data-ttu-id="0e65d-103">Gerenciando modelos de localização de configurações do UE-V 2. x usando o Windows PowerShell e o WMI</span><span class="sxs-lookup"><span data-stu-id="0e65d-103">Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI</span></span>


<span data-ttu-id="0e65d-104">Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 usam modelos de localização de configurações XML para definir as configurações que a virtualização da experiência do usuário captura e aplica.</span><span class="sxs-lookup"><span data-stu-id="0e65d-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 use XML settings location templates to define the settings that User Experience Virtualization captures and applies.</span></span> <span data-ttu-id="0e65d-105">O UE-V inclui um conjunto de modelos de localização de configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="0e65d-105">UE-V includes a set of standard settings location templates.</span></span> <span data-ttu-id="0e65d-106">Ele também inclui a ferramenta de gerador do UE-V que permite criar modelos de local de configurações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="0e65d-106">It also includes the UE-V Generator tool that enables you to create custom settings location templates.</span></span> <span data-ttu-id="0e65d-107">Depois de criar e implantar modelos de local de configurações, você pode gerenciar esses modelos usando o Windows PowerShell e a instrumentação de gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0e65d-107">After you create and deploy settings location templates, you can manage those templates by using Windows PowerShell and the Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="0e65d-108">Para obter uma lista completa dos cmdlets do PowerShell do UE-V, consulte [referência do cmdlet do UE-v 2](https://go.microsoft.com/fwlink/p/?LinkId=393495) ( https://go.microsoft.com/fwlink/p/?LinkId=393495) .</span><span class="sxs-lookup"><span data-stu-id="0e65d-108">For a complete list of UE-V PowerShell cmdlets, see [UE-V 2 Cmdlet Reference](https://go.microsoft.com/fwlink/p/?LinkId=393495) (https://go.microsoft.com/fwlink/p/?LinkId=393495).</span></span>

## <span data-ttu-id="0e65d-109">Gerenciar modelos de locais de configurações do UE-V 2 usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0e65d-109">Manage UE-V 2 settings location templates by using Windows PowerShell</span></span>


<span data-ttu-id="0e65d-110">Os recursos do WMI e do Windows PowerShell do UE-V incluem a capacidade de habilitar, desabilitar, registrar, atualizar e cancelar o registro de modelos de localização de configurações.</span><span class="sxs-lookup"><span data-stu-id="0e65d-110">The WMI and Windows PowerShell features of UE-V include the ability to enable, disable, register, update, and unregister settings location templates.</span></span> <span data-ttu-id="0e65d-111">Ao usar esses recursos, você pode automatizar o processo de registro, atualização ou cancelamento de registro de modelos com o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="0e65d-111">By using these features, you can automate the process of registering, updating, or unregistering templates with the UE-V Agent.</span></span> <span data-ttu-id="0e65d-112">Você também pode registrar modelos manualmente usando os comandos WMI e Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0e65d-112">You can also manually register templates by using WMI and Windows PowerShell commands.</span></span> <span data-ttu-id="0e65d-113">Ao usar esses recursos em conjunto com uma solução de distribuição de software eletrônico, política de grupo ou outro método de implantação automatizado, como um script, você pode automatizar ainda mais o processo.</span><span class="sxs-lookup"><span data-stu-id="0e65d-113">By using these features in conjunction with an electronic software distribution solution, Group Policy, or another automated deployment method such as a script, you can further automate that process.</span></span>

<span data-ttu-id="0e65d-114">Você deve ter permissões de administrador para atualizar, registrar ou cancelar o registro de um modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="0e65d-114">You must have administrator permissions to update, register, or unregister a settings location template.</span></span> <span data-ttu-id="0e65d-115">Não é necessário ter permissões de administrador para habilitar, desabilitar ou listar modelos.</span><span class="sxs-lookup"><span data-stu-id="0e65d-115">Administrator permissions are not required to enable, disable, or list templates.</span></span>

***<em><span data-ttu-id="0e65d-116">Para gerenciar modelos de local de configurações usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0e65d-116">To manage settings location templates by using Windows PowerShell</span></span>ell</em>***

1.  <span data-ttu-id="0e65d-117">Use uma conta com direitos de administrador para abrir um prompt de comando do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0e65d-117">Use an account with administrator rights to open a Windows PowerShell command prompt.</span></span>

2.  <span data-ttu-id="0e65d-118">Use os seguintes cmdlets do Windows PowerShell para registrar e gerenciar os modelos de local das configurações do UE-V.</span><span class="sxs-lookup"><span data-stu-id="0e65d-118">Use the following Windows PowerShell cmdlets to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="0e65d-119">comando do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0e65d-119">Windows PowerShell command</span></span></th>
    <th align="left"><span data-ttu-id="0e65d-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e65d-120">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-121">Lista todos os modelos de local de configurações que estão registrados no computador.</span><span class="sxs-lookup"><span data-stu-id="0e65d-121">Lists all the settings location templates that are registered on the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate –Application &lt;string&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-122">Lista todos os modelos de local de configurações que são registrados no computador em que o nome do aplicativo ou o nome do modelo contém &lt; cadeia de caracteres &gt; .</span><span class="sxs-lookup"><span data-stu-id="0e65d-122">Lists all the settings location templates that are registered on the computer where the application name or template name contains &lt;string&gt;.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate –TemplateID &lt;string&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-123">Lista todos os modelos de local de configurações que são registrados no computador em que a ID do modelo contém a &lt; cadeia de caracteres &gt; .</span><span class="sxs-lookup"><span data-stu-id="0e65d-123">Lists all the settings location templates that are registered on the computer where the template ID contains &lt;string&gt;.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate [-ApplicationOrTemplateID] &lt;string&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-124">Lista todos os modelos de local de configurações que são registrados no computador onde o nome do aplicativo ou do modelo ou a ID do modelo contém &lt; cadeia de caracteres &gt; .</span><span class="sxs-lookup"><span data-stu-id="0e65d-124">Lists all the settings location templates that are registered on the computer where the application or template name, or template ID contains &lt;string&gt;.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplateProgram [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-125">Obtém o nome das informações do programa e da versão, que dependem da ID do modelo.</span><span class="sxs-lookup"><span data-stu-id="0e65d-125">Gets the name of the program and version information, which depend on the template ID.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-126">Obtém a lista de aplicativos do Windows em vigor.</span><span class="sxs-lookup"><span data-stu-id="0e65d-126">Gets the effective list of Windows apps.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevAppXPackage -Computer</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-127">Obtém a lista de aplicativos do Windows que estão configurados para o computador.</span><span class="sxs-lookup"><span data-stu-id="0e65d-127">Gets the list of Windows apps that are configured for the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-128">Obtém a lista de aplicativos do Windows que são configurados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="0e65d-128">Gets the list of Windows apps that are configured for the current user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Register-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-129">Registra um ou mais modelos de local de configurações com UE-V usando caminhos relativos e/ou caracteres curinga em caminhos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="0e65d-129">Registers one or more settings location template with UE-V by using relative paths and/or wildcard characters in file paths.</span></span> <span data-ttu-id="0e65d-130">Após o registro de um modelo, o UE-V sincroniza as configurações definidas no modelo entre computadores que têm o modelo registrado.</span><span class="sxs-lookup"><span data-stu-id="0e65d-130">After a template is registered, UE-V synchronizes the settings that are defined in the template between computers that have the template registered.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Register-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-131">Registra um ou mais modelos de local de configurações com UE-V usando caminhos literais, onde nenhum caractere pode ser interpretado como caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="0e65d-131">Registers one or more settings location template with UE-V by using literal paths, where no characters can be interpreted as wildcard characters.</span></span> <span data-ttu-id="0e65d-132">Após o registro de um modelo, o UE-V sincroniza as configurações definidas no modelo entre computadores que têm o modelo registrado.</span><span class="sxs-lookup"><span data-stu-id="0e65d-132">After a template is registered, UE-V synchronizes the settings that are defined in the template between computers that have the template registered.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Unregister-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-133">Cancela o registro de um modelo de local de configurações com UE-V.</span><span class="sxs-lookup"><span data-stu-id="0e65d-133">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="0e65d-134">Quando um modelo é cancelado, o UE-V não sincroniza mais as configurações definidas no modelo entre computadores.</span><span class="sxs-lookup"><span data-stu-id="0e65d-134">When a template is unregistered, UE-V no longer synchronizes the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Unregister-UevTemplate -All</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-135">Cancela o registro de todos os modelos de locais de configurações com UE-V.</span><span class="sxs-lookup"><span data-stu-id="0e65d-135">Unregisters all settings location templates with UE-V.</span></span> <span data-ttu-id="0e65d-136">Quando um modelo é cancelado, o UE-V não sincroniza mais as configurações definidas no modelo entre computadores.</span><span class="sxs-lookup"><span data-stu-id="0e65d-136">When a template is unregistered, UE-V no longer synchronizes the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Update-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-137">Atualiza um ou mais modelos de local de configurações com uma versão mais recente do modelo.</span><span class="sxs-lookup"><span data-stu-id="0e65d-137">Updates one or more settings location templates with a more recent version of the template.</span></span> <span data-ttu-id="0e65d-138">Use caminhos relativos e/ou caracteres curinga nos caminhos do arquivo.</span><span class="sxs-lookup"><span data-stu-id="0e65d-138">Use relative paths and/or wildcard characters in the file paths.</span></span> <span data-ttu-id="0e65d-139">O novo modelo deve ser uma versão mais recente do que o modelo existente.</span><span class="sxs-lookup"><span data-stu-id="0e65d-139">The new template should be a newer version than the existing template.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Update-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-140">Atualiza um ou mais modelos de local de configurações com uma versão mais recente do modelo.</span><span class="sxs-lookup"><span data-stu-id="0e65d-140">Updates one or more settings location templates with a more recent version of the template.</span></span> <span data-ttu-id="0e65d-141">Use caminhos completos para arquivos de modelo, onde nenhum caractere pode ser interpretado como caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="0e65d-141">Use full paths to template files, where no characters can be interpreted as wildcard characters.</span></span> <span data-ttu-id="0e65d-142">O novo modelo deve ser uma versão mais recente do que o modelo existente.</span><span class="sxs-lookup"><span data-stu-id="0e65d-142">The new template should be a newer version than the existing template.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-143">Remove um ou mais aplicativos do Windows da lista de aplicativos do Windows do computador.</span><span class="sxs-lookup"><span data-stu-id="0e65d-143">Removes one or more Windows apps from the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-144">Remove o aplicativo do Windows da lista de aplicativos do usuário do Windows atual.</span><span class="sxs-lookup"><span data-stu-id="0e65d-144">Removes Windows app from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer -All</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-145">Remove todos os aplicativos do Windows da lista de aplicativos do Windows do computador.</span><span class="sxs-lookup"><span data-stu-id="0e65d-145">Removes all Windows apps from the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-146">Remove um ou mais aplicativos do Windows da lista de aplicativos do usuário do Windows atual.</span><span class="sxs-lookup"><span data-stu-id="0e65d-146">Removes one or more Windows apps from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] -All</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-147">Remove todos os aplicativos do Windows da lista de aplicativos do Windows do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="0e65d-147">Removes all Windows apps from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-148">Desabilita um modelo de local de configurações para o usuário atual do computador.</span><span class="sxs-lookup"><span data-stu-id="0e65d-148">Disables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Disable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-149">Desabilita um ou mais aplicativos do Windows na lista de aplicativos do Windows do computador.</span><span class="sxs-lookup"><span data-stu-id="0e65d-149">Disables one or more Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-150">Desabilita um ou mais aplicativos do Windows na lista de aplicativos do usuário do Windows atual.</span><span class="sxs-lookup"><span data-stu-id="0e65d-150">Disables one or more Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-151">Habilita um modelo de local de configurações para o usuário atual do computador.</span><span class="sxs-lookup"><span data-stu-id="0e65d-151">Enables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Enable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-152">Habilita um ou mais aplicativos do Windows na lista de aplicativos do Windows do computador.</span><span class="sxs-lookup"><span data-stu-id="0e65d-152">Enables one or more Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-153">Habilita um ou mais aplicativos do Windows na lista de aplicativos do usuário do Windows atual.</span><span class="sxs-lookup"><span data-stu-id="0e65d-153">Enables one or more Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Test-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-154">Determina se um ou mais modelos de localização de configurações estão em conformidade com o esquema XML.</span><span class="sxs-lookup"><span data-stu-id="0e65d-154">Determines whether one or more settings location templates comply with its XML schema.</span></span> <span data-ttu-id="0e65d-155">Pode usar caminhos relativos e caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="0e65d-155">Can use relative paths and wildcard characters.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Test-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-156">Determina se um ou mais modelos de localização de configurações estão em conformidade com o esquema XML.</span><span class="sxs-lookup"><span data-stu-id="0e65d-156">Determines whether one or more settings location templates comply with its XML schema.</span></span> <span data-ttu-id="0e65d-157">O caminho deve ser um caminho completo para o arquivo de modelo, mas não inclui caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="0e65d-157">The path must be a full path to the template file, but does not include wildcard characters.</span></span></p></td>
    </tr>
    </tbody>
    </table>



<span data-ttu-id="0e65d-158">Os recursos do UE-V Windows PowerShell permitem que você gerencie um grupo de modelos de configurações implantados em sua empresa.</span><span class="sxs-lookup"><span data-stu-id="0e65d-158">The UE-V Windows PowerShell features enable you to manage a group of settings templates that are deployed in your enterprise.</span></span> <span data-ttu-id="0e65d-159">Use o procedimento a seguir para gerenciar um grupo de modelos usando o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0e65d-159">Use the following procedure to manage a group of templates by using Windows PowerShell.</span></span>

**<span data-ttu-id="0e65d-160">Para gerenciar um grupo de modelos de local de configurações usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0e65d-160">To manage a group of settings location templates by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="0e65d-161">Modifique ou atualize os modelos de local de configurações desejadas.</span><span class="sxs-lookup"><span data-stu-id="0e65d-161">Modify or update the desired settings location templates.</span></span>

2.  <span data-ttu-id="0e65d-162">Se você quiser modificar ou atualizar os modelos de local de configurações, implante esses modelos de local de configurações para uma pasta acessível ao computador local.</span><span class="sxs-lookup"><span data-stu-id="0e65d-162">If you want to modify or update the settings location templates, deploy those settings location templates to a folder that is accessible to the local computer.</span></span>

3.  <span data-ttu-id="0e65d-163">No computador local, abra uma janela do Windows PowerShell com direitos de administrador.</span><span class="sxs-lookup"><span data-stu-id="0e65d-163">On the local computer, open a Windows PowerShell window with administrator rights.</span></span>

4.  <span data-ttu-id="0e65d-164">Cancele o registro de todas as versões registradas anteriormente dos modelos digitando o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="0e65d-164">Unregister all the previously registered versions of the templates by typing the following command.</span></span>

    ``` syntax
    Unregister-UevTemplate -All
    ```

    <span data-ttu-id="0e65d-165">Esse comando cancela o registro de todos os modelos ativos no computador.</span><span class="sxs-lookup"><span data-stu-id="0e65d-165">This command unregisters all active templates on the computer.</span></span>

5.  <span data-ttu-id="0e65d-166">Registre os modelos atualizados digitando o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="0e65d-166">Register the updated templates by typing the following command.</span></span>

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    <span data-ttu-id="0e65d-167">Esse comando registra todos os modelos de local de configurações localizados na pasta de modelos especificada.</span><span class="sxs-lookup"><span data-stu-id="0e65d-167">This command registers all of the settings location templates that are located in the specified template folder.</span></span>

### <a href="" id="win8applist"></a><span data-ttu-id="0e65d-168">Lista de aplicativos do Windows</span><span class="sxs-lookup"><span data-stu-id="0e65d-168">Windows app list</span></span>

<span data-ttu-id="0e65d-169">Ao listar um aplicativo do Windows na lista de aplicativos do Windows, você especifica se esse aplicativo está habilitado ou desabilitado para a sincronização das configurações.</span><span class="sxs-lookup"><span data-stu-id="0e65d-169">By listing a Windows app in the Windows app list, you specify whether that app is enabled or disabled for settings synchronization.</span></span> <span data-ttu-id="0e65d-170">Os aplicativos são identificados na lista pelo nome da família de pacotes e se a sincronização das configurações deve ser habilitada ou desabilitada para esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0e65d-170">Apps are identified in the list by their Package Family name and whether settings synchronization should be enabled or disabled for that app.</span></span> <span data-ttu-id="0e65d-171">Ao usar essas configurações juntamente com a configuração de comportamento de sincronização padrão não listada, você pode controlar se os aplicativos do Windows serão sincronizados.</span><span class="sxs-lookup"><span data-stu-id="0e65d-171">When you use these settings along with the Unlisted Default Sync Behavior setting, you can control whether Windows apps are synchronized.</span></span>

<span data-ttu-id="0e65d-172">Para exibir o nome da família de pacotes de aplicativos do Windows instalados, em um prompt de comando do Windows PowerShell, digite:</span><span class="sxs-lookup"><span data-stu-id="0e65d-172">To display the Package Family Name of installed Windows apps, at a Windows PowerShell command prompt, enter:</span></span>

``` syntax
Get-AppxPackage | Sort-Object PackageFamilyName | Format-Table PackageFamilyName
```

<span data-ttu-id="0e65d-173">Para exibir uma lista de aplicativos do Windows que podem sincronizar as configurações em um computador com o nome da família de pacotes, status habilitado e fonte habilitada, em um prompt de comando do Windows PowerShell, digite:</span><span class="sxs-lookup"><span data-stu-id="0e65d-173">To display a list of Windows apps that can synchronize settings on a computer with their package family name, enabled status, and enabled source, at a Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage`

**<span data-ttu-id="0e65d-174">Definições das propriedades Get-UevAppxPackage</span><span class="sxs-lookup"><span data-stu-id="0e65d-174">Definitions of Get-UevAppxPackage properties</span></span>**

<a href="" id="displayname"></a>**<span data-ttu-id="0e65d-175">DisplayName</span><span class="sxs-lookup"><span data-stu-id="0e65d-175">DisplayName</span></span>**  
<span data-ttu-id="0e65d-176">O nome que é exibido para o usuário no aplicativo da central de configurações da empresa.</span><span class="sxs-lookup"><span data-stu-id="0e65d-176">The name that is displayed to the user in the Company Settings Center application.</span></span> <span data-ttu-id="0e65d-177">A `DisplayName` propriedade é derivada da `PackageFamilyName` propriedade.</span><span class="sxs-lookup"><span data-stu-id="0e65d-177">The `DisplayName` property is derived from the `PackageFamilyName` property.</span></span>

<a href="" id="packagefamilyname"></a>**<span data-ttu-id="0e65d-178">PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="0e65d-178">PackageFamilyName</span></span>**  
<span data-ttu-id="0e65d-179">O nome do pacote que é instalado para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="0e65d-179">The name of the package that is installed for the current user.</span></span>

<a href="" id="enabled"></a>**<span data-ttu-id="0e65d-180">Habilitado</span><span class="sxs-lookup"><span data-stu-id="0e65d-180">Enabled</span></span>**  
<span data-ttu-id="0e65d-181">Define se as configurações do aplicativo estão configuradas para sincronização.</span><span class="sxs-lookup"><span data-stu-id="0e65d-181">Defines whether the settings for the app are configured to synchronize.</span></span>

<a href="" id="enabledsource"></a>**<span data-ttu-id="0e65d-182">Habilitou</span><span class="sxs-lookup"><span data-stu-id="0e65d-182">EnabledSource</span></span>**  
<span data-ttu-id="0e65d-183">O local em que a configuração que habilita ou desabilita o aplicativo está definida.</span><span class="sxs-lookup"><span data-stu-id="0e65d-183">The location where the configuration that enables or disables the app is set.</span></span> <span data-ttu-id="0e65d-184">Os valores possíveis são: *NotSet*, *LocalMachine*, *LocalUser*, *PolicyMachine*e *PolicyUser*.</span><span class="sxs-lookup"><span data-stu-id="0e65d-184">Possible values are: *NotSet*, *LocalMachine*, *LocalUser*, *PolicyMachine*, and *PolicyUser*.</span></span>

<a href="" id="notset"></a>**<span data-ttu-id="0e65d-185">NotSet</span><span class="sxs-lookup"><span data-stu-id="0e65d-185">NotSet</span></span>**  
<span data-ttu-id="0e65d-186">A política não está configurada para sincronizar este aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0e65d-186">The policy is not configured to synchronize this app.</span></span>

<a href="" id="localmachine"></a>**<span data-ttu-id="0e65d-187">LocalMachine</span><span class="sxs-lookup"><span data-stu-id="0e65d-187">LocalMachine</span></span>**  
<span data-ttu-id="0e65d-188">O estado habilitado é definido na seção computador local do registro.</span><span class="sxs-lookup"><span data-stu-id="0e65d-188">The enabled state is set in the local computer section of the registry.</span></span>

<a href="" id="localuser"></a>**<span data-ttu-id="0e65d-189">Conta</span><span class="sxs-lookup"><span data-stu-id="0e65d-189">LocalUser</span></span>**  
<span data-ttu-id="0e65d-190">O estado habilitado é definido na seção usuário atual do registro.</span><span class="sxs-lookup"><span data-stu-id="0e65d-190">The enabled state is set in the current user section of the registry.</span></span>

<a href="" id="policymachine"></a>**<span data-ttu-id="0e65d-191">PolicyMachine</span><span class="sxs-lookup"><span data-stu-id="0e65d-191">PolicyMachine</span></span>**  
<span data-ttu-id="0e65d-192">O estado habilitado é definido na seção política da seção computador local do registro.</span><span class="sxs-lookup"><span data-stu-id="0e65d-192">The enabled state is set in the policy section of the local computer section of the registry.</span></span>

<span data-ttu-id="0e65d-193">Para obter a lista de aplicativos do Windows configurado pelo usuário, no prompt de comando do Windows PowerShell, digite:</span><span class="sxs-lookup"><span data-stu-id="0e65d-193">To get the user-configured list of Windows apps, at the Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage –CurrentComputerUser`

<span data-ttu-id="0e65d-194">Para obter a lista configurada do computador de aplicativos do Windows, no prompt de comando do Windows PowerShell, digite:</span><span class="sxs-lookup"><span data-stu-id="0e65d-194">To get the computer-configured list of Windows apps, at the Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage –Computer`

<span data-ttu-id="0e65d-195">Para qualquer um dos parâmetros, CurrentComputerUser ou computador, o cmdlet retorna uma lista dos aplicativos do Windows que são configurados no nível do usuário ou do computador.</span><span class="sxs-lookup"><span data-stu-id="0e65d-195">For either parameter, CurrentComputerUser or Computer, the cmdlet returns a list of the Windows apps that are configured at the user or at the computer level.</span></span>

**<span data-ttu-id="0e65d-196">Definições de propriedades</span><span class="sxs-lookup"><span data-stu-id="0e65d-196">Definitions of properties</span></span>**

<a href="" id="displayname"></a>**<span data-ttu-id="0e65d-197">DisplayName</span><span class="sxs-lookup"><span data-stu-id="0e65d-197">DisplayName</span></span>**  
<span data-ttu-id="0e65d-198">O nome que é exibido para o usuário no aplicativo da central de configurações da empresa.</span><span class="sxs-lookup"><span data-stu-id="0e65d-198">The name that is displayed to the user in the Company Settings Center application.</span></span> <span data-ttu-id="0e65d-199">A `DisplayName` propriedade é derivada da `PackageFamilyName` propriedade.</span><span class="sxs-lookup"><span data-stu-id="0e65d-199">The `DisplayName` property is derived from the `PackageFamilyName` property.</span></span>

<a href="" id="packagefamilyname"></a>**<span data-ttu-id="0e65d-200">PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="0e65d-200">PackageFamilyName</span></span>**  
<span data-ttu-id="0e65d-201">O nome do pacote que é instalado para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="0e65d-201">The name of the package that is installed for the current user.</span></span>

<a href="" id="enabled"></a>**<span data-ttu-id="0e65d-202">Habilitado</span><span class="sxs-lookup"><span data-stu-id="0e65d-202">Enabled</span></span>**  
<span data-ttu-id="0e65d-203">Define se as configurações do aplicativo estão configuradas para serem sincronizadas para a opção especificada, ou seja, **usuário** ou **computador**.</span><span class="sxs-lookup"><span data-stu-id="0e65d-203">Defines whether the settings for the app are configured to synchronize for the specified switch, that is, **user** or **computer**.</span></span>

<a href="" id="installed"></a>**<span data-ttu-id="0e65d-204">Instalado</span><span class="sxs-lookup"><span data-stu-id="0e65d-204">Installed</span></span>**  
<span data-ttu-id="0e65d-205">True se o aplicativo, ou seja, o PackageFamilyName estiver instalado para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="0e65d-205">True if the app, that is, the PackageFamilyName is installed for the current user.</span></span>

### <span data-ttu-id="0e65d-206">Gerenciar modelos de locais de configurações do UE-V 2 usando WMI</span><span class="sxs-lookup"><span data-stu-id="0e65d-206">Manage UE-V 2 settings location templates by using WMI</span></span>

<span data-ttu-id="0e65d-207">A virtualização da experiência do usuário fornece o seguinte conjunto de comandos WMI.</span><span class="sxs-lookup"><span data-stu-id="0e65d-207">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="0e65d-208">Os administradores podem usar essas interfaces para gerenciar modelos de local de configurações do Windows PowerShell e automatizar tarefas administrativas de modelos.</span><span class="sxs-lookup"><span data-stu-id="0e65d-208">Administrators can use these interfaces to manage settings location templates from Windows PowerShell and automate template administrative tasks.</span></span>

**<span data-ttu-id="0e65d-209">Para gerenciar modelos de local de configurações usando WMI</span><span class="sxs-lookup"><span data-stu-id="0e65d-209">To manage settings location templates by using WMI</span></span>**

1.  <span data-ttu-id="0e65d-210">Use uma conta com direitos de administrador para abrir uma janela do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0e65d-210">Use an account with administrator rights to open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="0e65d-211">Use os seguintes comandos WMI para registrar e gerenciar os modelos de local das configurações do UE-V.</span><span class="sxs-lookup"><span data-stu-id="0e65d-211">Use the following WMI commands to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>                         Windows PowerShell command</code></th>
    <th align="left"><span data-ttu-id="0e65d-212">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e65d-212">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId,TemplateName, TemplateVersion,Enabled | Format-Table -Autosize</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-213">Lista todos os modelos de local de configurações que são registrados para o computador.</span><span class="sxs-lookup"><span data-stu-id="0e65d-213">Lists all the settings location templates that are registered for the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod –Namespace root\Microsoft\UEV –Class SettingsLocationTemplate –Name GetProcessInfoByTemplateId &lt;template Id&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-214">Obtém o nome das informações do programa e da versão, o que depende do nome do modelo.</span><span class="sxs-lookup"><span data-stu-id="0e65d-214">Gets the name of the program and version information, which depends on the template name.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV EffectiveWindows8App</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-215">Obtém a lista de aplicativos do Windows em vigor.</span><span class="sxs-lookup"><span data-stu-id="0e65d-215">Gets the effective list of Windows apps.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="0e65d-216">Get-WmiObject-namespace root\Microsoft\UEV MachineConfiguredWindows8App</span><span class="sxs-lookup"><span data-stu-id="0e65d-216">Get-WmiObject -Namespace root\Microsoft\UEV MachineConfiguredWindows8App</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-217">Obtém a lista de aplicativos do Windows que estão configurados para o computador.</span><span class="sxs-lookup"><span data-stu-id="0e65d-217">Gets the list of Windows apps that are configured for the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguredWindows8App</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-218">Obtém a lista de aplicativos do Windows que são configurados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="0e65d-218">Gets the list of Windows apps that are configured for the current user.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Register -ArgumentList &lt;template path &gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-219">Registra um modelo de local de configurações com UE-V.</span><span class="sxs-lookup"><span data-stu-id="0e65d-219">Registers a settings location template with UE-V.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name UnregisterByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-220">Cancela o registro de um modelo de local de configurações com UE-V.</span><span class="sxs-lookup"><span data-stu-id="0e65d-220">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="0e65d-221">Assim que um modelo é cancelado, o UE-V não sincroniza mais as configurações definidas no modelo entre computadores.</span><span class="sxs-lookup"><span data-stu-id="0e65d-221">As soon as a template is unregistered, UE-V no longer synchronizes the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Update -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-222">Atualiza um modelo de local de configurações com UE-V.</span><span class="sxs-lookup"><span data-stu-id="0e65d-222">Updates a settings location template with UE-V.</span></span> <span data-ttu-id="0e65d-223">O novo modelo deve ser uma versão mais recente do que a existente.</span><span class="sxs-lookup"><span data-stu-id="0e65d-223">The new template should be a newer version than the existing one.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-224">Remove um ou mais aplicativos do Windows da lista de aplicativos do Windows do computador.</span><span class="sxs-lookup"><span data-stu-id="0e65d-224">Removes one or more Windows apps from the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-225">Remove um ou mais aplicativos do Windows da lista de aplicativos do usuário do Windows atual.</span><span class="sxs-lookup"><span data-stu-id="0e65d-225">Removes one or more Windows apps from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name DisableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-226">Desabilita um ou mais modelos de local de configurações com UE-V.</span><span class="sxs-lookup"><span data-stu-id="0e65d-226">Disables one or more settings location templates with UE-V.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-227">Desabilita um ou mais aplicativos do Windows na lista de aplicativos do Windows do computador.</span><span class="sxs-lookup"><span data-stu-id="0e65d-227">Disables one or more Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-228">Desabilita um ou mais aplicativos do Windows na lista de aplicativos do usuário do Windows atual.</span><span class="sxs-lookup"><span data-stu-id="0e65d-228">Disables one or more Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name EnableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-229">Habilita um modelo de local de configurações com UE-V.</span><span class="sxs-lookup"><span data-stu-id="0e65d-229">Enables a settings location template with UE-V.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-230">Habilita os aplicativos do Windows na lista de aplicativos do Windows do computador.</span><span class="sxs-lookup"><span data-stu-id="0e65d-230">Enables Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-231">Habilita os aplicativos do Windows na lista de aplicativos do usuário do Windows atual.</span><span class="sxs-lookup"><span data-stu-id="0e65d-231">Enables Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Validate -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="0e65d-232">Determina se um modelo de local de configurações especificado está em conformidade com o esquema XML.</span><span class="sxs-lookup"><span data-stu-id="0e65d-232">Determines whether a given settings location template complies with its XML schema.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
Where a list of Package Family Names is called by the WMI command, the list must be in quotes and separated by a pipe symbol, for example, `"<package family name | package family name>"`.
~~~



### <span data-ttu-id="0e65d-233">Implantando o UE-V Agent usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0e65d-233">Deploying the UE-V Agent using Windows PowerShell</span></span>

**<span data-ttu-id="0e65d-234">Como implantar o UE-V Agent usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0e65d-234">How to deploy the UE-V Agent by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="0e65d-235">Testar o pacote de instalação do UE-V Agent em um compartilhamento de rede acessível.</span><span class="sxs-lookup"><span data-stu-id="0e65d-235">Stage the UE-V Agent installation package in an accessible network share.</span></span>

    **<span data-ttu-id="0e65d-236">Observação</span><span class="sxs-lookup"><span data-stu-id="0e65d-236">Note</span></span>**  
    <span data-ttu-id="0e65d-237">Use AgentSetup.exe para implantar as versões de 32 bits e de 64 bits do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="0e65d-237">Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="0e65d-238">Os pacotes do Windows Installer, AgentSetupx86.msi e AgentSetupx64.msi, estão disponíveis para cada arquitetura.</span><span class="sxs-lookup"><span data-stu-id="0e65d-238">The Windows Installer packages, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="0e65d-239">Para desinstalar o UE-V Agent posteriormente, usando o arquivo de instalação, você deve usar o mesmo tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="0e65d-239">To uninstall the UE-V Agent at a later time by using the installation file, you must use the same file type.</span></span>



2.  <span data-ttu-id="0e65d-240">Use um dos seguintes comandos do Windows PowerShell para instalar o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="0e65d-240">Use one of the following Windows PowerShell commands to install the UE-V Agent.</span></span>

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

<span data-ttu-id="0e65d-241">**Tem uma sugestão para UE-V**?</span><span class="sxs-lookup"><span data-stu-id="0e65d-241">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="0e65d-242">Adicione ou vote em sugestões [aqui](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span><span class="sxs-lookup"><span data-stu-id="0e65d-242">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="0e65d-243">**Tem um problema de UE-V**?</span><span class="sxs-lookup"><span data-stu-id="0e65d-243">**Got a UE-V issue**?</span></span> <span data-ttu-id="0e65d-244">Use o [Fórum do TechNet para UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span><span class="sxs-lookup"><span data-stu-id="0e65d-244">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <span data-ttu-id="0e65d-245">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e65d-245">Related topics</span></span>


[<span data-ttu-id="0e65d-246">Administração do UE-V 2. x com o Windows PowerShell e o WMI</span><span class="sxs-lookup"><span data-stu-id="0e65d-246">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[<span data-ttu-id="0e65d-247">Administração do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="0e65d-247">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)









