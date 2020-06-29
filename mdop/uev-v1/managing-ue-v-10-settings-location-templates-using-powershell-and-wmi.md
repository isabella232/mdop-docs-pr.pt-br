---
title: Gerenciamento dos modelos de localização de configurações da UE-V 1.0 usando o PowerShell e o WMI
description: Gerenciamento dos modelos de localização de configurações da UE-V 1.0 usando o PowerShell e o WMI
author: dansimp
ms.assetid: 4b911c78-a5e9-4199-bfeb-72ab764d47c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8dab0997cdfaf7c96862fcce4bc012c3edfe0c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796013"
---
# <span data-ttu-id="14f6a-103">Gerenciamento dos modelos de localização de configurações da UE-V 1.0 usando o PowerShell e o WMI</span><span class="sxs-lookup"><span data-stu-id="14f6a-103">Managing UE-V 1.0 Settings Location Templates Using PowerShell and WMI</span></span>


<span data-ttu-id="14f6a-104">O Microsoft User Experience Virtualization (UE-V Experience Virtualization) usa modelos de local de configurações (arquivos XML) que definem as configurações capturadas e aplicadas pela virtualização da experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="14f6a-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings captured and applied by User Experience Virtualization.</span></span> <span data-ttu-id="14f6a-105">O UE-V inclui um conjunto de modelos de localização de configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="14f6a-105">UE-V includes a set of standard settings location templates.</span></span> <span data-ttu-id="14f6a-106">Ele também inclui a ferramenta de gerador do UE-V que permite criar modelos de local de configurações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="14f6a-106">It also includes the UE-V Generator tool that enables you to create custom settings location templates.</span></span> <span data-ttu-id="14f6a-107">Depois de criar e implantar modelos de local de configurações, você pode gerenciar esses modelos usando o PowerShell ou o WMI.</span><span class="sxs-lookup"><span data-stu-id="14f6a-107">After you create and deploy settings location templates you can manage those templates using PowerShell or WMI.</span></span>

## <span data-ttu-id="14f6a-108">Gerenciar modelos de local de configurações com WMI e PowerShell</span><span class="sxs-lookup"><span data-stu-id="14f6a-108">Manage settings location templates with WMI and PowerShell</span></span>


<span data-ttu-id="14f6a-109">Os recursos do WMI e do PowerShell do UE-V incluem a capacidade de habilitar, desabilitar, registrar, atualizar e cancelar o registro de modelos de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="14f6a-109">The WMI and PowerShell features of UE-V include the ability to enable, disable, register, update, and unregister settings location templates.</span></span> <span data-ttu-id="14f6a-110">Ao usar esses recursos, você pode automatizar o processo de registro, atualização ou cancelamento de registro de modelos com o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="14f6a-110">By using these features, you can automate the process of registering, updating, or unregistering templates with the UE-V agent.</span></span> <span data-ttu-id="14f6a-111">Você também pode registrar modelos manualmente usando os comandos WMI e PowerShell.</span><span class="sxs-lookup"><span data-stu-id="14f6a-111">You can also manually register templates using WMI and PowerShell commands.</span></span> <span data-ttu-id="14f6a-112">Ao usar esses recursos em conjunto com uma solução de distribuição de software eletrônico, política de grupo ou outro método de implantação automatizado, como um script, você pode automatizar ainda mais o processo.</span><span class="sxs-lookup"><span data-stu-id="14f6a-112">By using these features in conjunction with an electronic software distribution solution, Group Policy, or another automated deployment method such as a script, you can further automate that process.</span></span>

<span data-ttu-id="14f6a-113">Você deve ter permissões de administrador para atualizar, registrar ou cancelar o registro de um modelo de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="14f6a-113">You must have administrator permissions to update, register, or unregister a settings location template.</span></span> <span data-ttu-id="14f6a-114">Não é necessário ter permissões de administrador para habilitar ou desabilitar modelos.</span><span class="sxs-lookup"><span data-stu-id="14f6a-114">Administrator permissions are not required to enable or disable templates.</span></span>

**<span data-ttu-id="14f6a-115">Para gerenciar modelos de local de configurações com o PowerShell</span><span class="sxs-lookup"><span data-stu-id="14f6a-115">To manage settings location templates with PowerShell</span></span>**

1.  <span data-ttu-id="14f6a-116">Use uma conta com direitos de administrador para abrir uma janela do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="14f6a-116">Use an account with administrator rights to open a Windows PowerShell window.</span></span> <span data-ttu-id="14f6a-117">Para importar o módulo **Microsoft UE-V PowerShell** , digite o seguinte comando no prompt de comando do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="14f6a-117">To import the **Microsoft UE-V PowerShell** module, type the following command at the PowerShell command prompt.</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="14f6a-118">Use os cmdlets do PowerShell a seguir para registrar e gerenciar os modelos de local das configurações do UE-V.</span><span class="sxs-lookup"><span data-stu-id="14f6a-118">Use the following PowerShell cmdlets to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="14f6a-119">Comando do PowerShell</span><span class="sxs-lookup"><span data-stu-id="14f6a-119">PowerShell command</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="14f6a-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="14f6a-120">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="14f6a-121">Get-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="14f6a-121">Get-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="14f6a-122">Lista todos os modelos de locais de configurações registrados no computador.</span><span class="sxs-lookup"><span data-stu-id="14f6a-122">Lists all the settings location templates registered on the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="14f6a-123">Register-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="14f6a-123">Register-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="14f6a-124">Registra um modelo de local de configurações com UE-V.</span><span class="sxs-lookup"><span data-stu-id="14f6a-124">Registers a settings location template with UE-V.</span></span> <span data-ttu-id="14f6a-125">Depois que um modelo é registrado, o UE-V sincronizará as configurações definidas no modelo entre computadores que têm o modelo registrado.</span><span class="sxs-lookup"><span data-stu-id="14f6a-125">Once a template is registered, UE-V will synchronize the settings that are defined in the template between computers that have the template registered.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="14f6a-126">Cancelar registro-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="14f6a-126">Unregister-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="14f6a-127">Cancela o registro de um modelo de local de configurações com UE-V.</span><span class="sxs-lookup"><span data-stu-id="14f6a-127">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="14f6a-128">Assim que um modelo é cancelado, o UE-V não sincronizará mais as configurações definidas no modelo entre computadores.</span><span class="sxs-lookup"><span data-stu-id="14f6a-128">As soon as a template is unregistered, UE-V will no longer synchronize the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="14f6a-129">Update-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="14f6a-129">Update-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="14f6a-130">Atualiza um modelo de local de configurações com uma versão mais recente do modelo.</span><span class="sxs-lookup"><span data-stu-id="14f6a-130">Updates a settings location template with a more recent version of the template.</span></span> <span data-ttu-id="14f6a-131">O novo modelo deve ter uma versão posterior a uma existente.</span><span class="sxs-lookup"><span data-stu-id="14f6a-131">The new template should have a version that is later than the existing one.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="14f6a-132">Disable-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="14f6a-132">Disable-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="14f6a-133">Desabilita um modelo de local de configurações para o usuário atual do computador.</span><span class="sxs-lookup"><span data-stu-id="14f6a-133">Disables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="14f6a-134">Enable-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="14f6a-134">Enable-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="14f6a-135">Habilita um modelo de local de configurações para o usuário atual do computador.</span><span class="sxs-lookup"><span data-stu-id="14f6a-135">Enables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="14f6a-136">Test-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="14f6a-136">Test-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="14f6a-137">Determina se um modelo de local de configurações especificado está em conformidade com o esquema XML.</span><span class="sxs-lookup"><span data-stu-id="14f6a-137">Determines whether a given settings location template complies with its XML schema.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

<span data-ttu-id="14f6a-138">Os recursos do PowerShell do UE-V permitem que você gerencie um grupo de modelos de configurações implantados em sua empresa.</span><span class="sxs-lookup"><span data-stu-id="14f6a-138">The UE-V PowerShell features allow you to manage a group of settings templates deployed in your enterprise.</span></span> <span data-ttu-id="14f6a-139">Para gerenciar um grupo de modelos usando o PowerShell, faça o seguinte.</span><span class="sxs-lookup"><span data-stu-id="14f6a-139">To manage a group of templates using PowerShell, do the following.</span></span>

**<span data-ttu-id="14f6a-140">Para gerenciar um grupo de modelos de local de configurações com o PowerShell</span><span class="sxs-lookup"><span data-stu-id="14f6a-140">To manage a group of settings location templates with PowerShell</span></span>**

1.  <span data-ttu-id="14f6a-141">Modifique ou atualize os modelos de local de configurações desejadas.</span><span class="sxs-lookup"><span data-stu-id="14f6a-141">Modify or update the desired settings location templates.</span></span>

2.  <span data-ttu-id="14f6a-142">Implante os modelos de localização de configurações desejadas para uma pasta acessível ao computador local.</span><span class="sxs-lookup"><span data-stu-id="14f6a-142">Deploy the desired settings location templates to a folder accessible to the local computer.</span></span>

3.  <span data-ttu-id="14f6a-143">No computador local, abra uma janela do Windows PowerShell com direitos de administrador.</span><span class="sxs-lookup"><span data-stu-id="14f6a-143">On the local computer, open a Windows PowerShell window with administrator rights.</span></span>

4.  <span data-ttu-id="14f6a-144">Importe o módulo Microsoft UE-V PowerShell, digitando o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="14f6a-144">Import the Microsoft UE-V PowerShell module, by typing the following command.</span></span>

    ``` syntax
    Import-module UEV
    ```

5.  <span data-ttu-id="14f6a-145">Cancele o registro de todas as versões registradas anteriormente dos modelos digitando o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="14f6a-145">Unregister all the previously registered versions of the templates by typing the following command.</span></span>

    ``` syntax
    Get-UevTemplate | Unregister-UevTemplate
    ```

    <span data-ttu-id="14f6a-146">Isso cancelará o registro de todos os modelos ativos no computador.</span><span class="sxs-lookup"><span data-stu-id="14f6a-146">This will unregister all active templates on the computer.</span></span>

6.  <span data-ttu-id="14f6a-147">Registre os modelos atualizados digitando o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="14f6a-147">Register the updated templates by typing the following command.</span></span>

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    <span data-ttu-id="14f6a-148">Isso registrará todos os modelos de locais de configurações localizados na pasta de modelos especificada.</span><span class="sxs-lookup"><span data-stu-id="14f6a-148">This will register all of the settings location templates located in the specified template folder.</span></span>

<span data-ttu-id="14f6a-149">A virtualização da experiência do usuário fornece o seguinte conjunto de comandos WMI.</span><span class="sxs-lookup"><span data-stu-id="14f6a-149">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="14f6a-150">Os administradores podem usar essas interfaces para gerenciar modelos de local de configurações do Windows PowerShell e automatizar tarefas administrativas de modelos.</span><span class="sxs-lookup"><span data-stu-id="14f6a-150">Administrators can use these interfaces to manage settings location templates from Windows PowerShell and automate template administrative tasks.</span></span>

**<span data-ttu-id="14f6a-151">Para gerenciar modelos de local de configurações com WMI</span><span class="sxs-lookup"><span data-stu-id="14f6a-151">To manage settings location templates with WMI</span></span>**

1.  <span data-ttu-id="14f6a-152">Use uma conta com direitos de administrador para abrir uma janela do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="14f6a-152">Use an account with administrator rights to open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="14f6a-153">Use os seguintes comandos WMI para registrar e gerenciar os modelos de local das configurações do UE-V.</span><span class="sxs-lookup"><span data-stu-id="14f6a-153">Use the following WMI commands to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="14f6a-154">Comando do PowerShell</span><span class="sxs-lookup"><span data-stu-id="14f6a-154">PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="14f6a-155">Descrição</span><span class="sxs-lookup"><span data-stu-id="14f6a-155">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="14f6a-156">Get-WmiObject-namespace root\Microsoft\UEV SettingsLocationTemplate | Select-TemplateID do objeto, TemplateName, TemplateVersion, Enabled | Format-Table-AutoSize</span><span class="sxs-lookup"><span data-stu-id="14f6a-156">Get-WmiObject -Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId,TemplateName, TemplateVersion,Enabled | Format-Table -Autosize</span></span></p></td>
    <td align="left"><p><span data-ttu-id="14f6a-157">Lista todos os modelos de locais de configurações registrados para o computador.</span><span class="sxs-lookup"><span data-stu-id="14f6a-157">Lists all the settings location templates registered for the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="14f6a-158">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Registerlist caminho do modelo de argumento &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="14f6a-158">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Register -ArgumentList &lt;template path &gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="14f6a-159">Registra um modelo de local de configurações com UE-V.</span><span class="sxs-lookup"><span data-stu-id="14f6a-159">Registers a settings location template with UE-V.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="14f6a-160">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name UnregisterByTemplateId-ArgumentList &lt; ID do modelo&gt;</span><span class="sxs-lookup"><span data-stu-id="14f6a-160">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name UnregisterByTemplateId -ArgumentList &lt;template ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="14f6a-161">Cancela o registro de um modelo de local de configurações com UE-V.</span><span class="sxs-lookup"><span data-stu-id="14f6a-161">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="14f6a-162">Assim que um modelo é cancelado, o UE-V não sincronizará mais as configurações definidas no modelo entre computadores.</span><span class="sxs-lookup"><span data-stu-id="14f6a-162">As soon as a template is unregistered, UE-V will no longer synchronize the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="14f6a-163">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name EnableByTemplateId-ArgumentList &lt; ID do modelo&gt;</span><span class="sxs-lookup"><span data-stu-id="14f6a-163">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name EnableByTemplateId -ArgumentList &lt;template ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="14f6a-164">Habilita um modelo de local de configurações com UE-V</span><span class="sxs-lookup"><span data-stu-id="14f6a-164">Enables a settings location template with UE-V</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="14f6a-165">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name DisableByTemplateId-ArgumentList &lt; ID do modelo&gt;</span><span class="sxs-lookup"><span data-stu-id="14f6a-165">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name DisableByTemplateId -ArgumentList &lt;template ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="14f6a-166">Desabilita um modelo de local de configurações com UE-V</span><span class="sxs-lookup"><span data-stu-id="14f6a-166">Disables a settings location template with UE-V</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="14f6a-167">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Update-caminho do &lt; modelo de argumento&gt;</span><span class="sxs-lookup"><span data-stu-id="14f6a-167">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Update -ArgumentList &lt;template path&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="14f6a-168">Atualiza um modelo de local de configurações com UE-V.</span><span class="sxs-lookup"><span data-stu-id="14f6a-168">Updates a settings location template with UE-V.</span></span> <span data-ttu-id="14f6a-169">O novo modelo deve ter uma versão superior à existente.</span><span class="sxs-lookup"><span data-stu-id="14f6a-169">The new template should have a version that is higher than the existing one.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="14f6a-170">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Validate-ArgumentList &lt; caminho do modelo&gt;</span><span class="sxs-lookup"><span data-stu-id="14f6a-170">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Validate -ArgumentList &lt;template path&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="14f6a-171">Determina se um modelo de local de configurações especificado está em conformidade com o esquema XML.</span><span class="sxs-lookup"><span data-stu-id="14f6a-171">Determines whether a given settings location template complies with its XML schema.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="14f6a-172">Como implantar o UE-V Agent com o PowerShell</span><span class="sxs-lookup"><span data-stu-id="14f6a-172">How to deploy the UE-V agent with PowerShell</span></span>**

1.  <span data-ttu-id="14f6a-173">Testar o arquivo do instalador do UE-V em um compartilhamento de rede acessível.</span><span class="sxs-lookup"><span data-stu-id="14f6a-173">Stage the UE-V installer file in an accessible network share.</span></span>

    <span data-ttu-id="14f6a-174">**Observação**  Use AgentSetup.exe para implantar as versões de 32 bits e de 64 bits do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="14f6a-174">**Note** Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="14f6a-175">Os arquivos do Windows Installer versões, AgentSetupx86.msi e AgentSetupx64.msi, estão disponíveis para cada arquitetura.</span><span class="sxs-lookup"><span data-stu-id="14f6a-175">Windows Installer Files versions, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="14f6a-176">Para desinstalar o UE-V Agent posteriormente usando o arquivo de instalação, você deve usar o mesmo tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="14f6a-176">To uninstall the UE-V Agent at a later time using the installation file, you must use the same file type.</span></span>

     

2.  <span data-ttu-id="14f6a-177">Use um dos seguintes comandos do PowerShell para instalar o agente.</span><span class="sxs-lookup"><span data-stu-id="14f6a-177">Use one of the following PowerShell commands to install the agent.</span></span>

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

## <span data-ttu-id="14f6a-178">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="14f6a-178">Related topics</span></span>


[<span data-ttu-id="14f6a-179">Gerenciamento de agente e pacotes da UE-V 1.0 com o PowerShell e o WMI</span><span class="sxs-lookup"><span data-stu-id="14f6a-179">Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI</span></span>](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

[<span data-ttu-id="14f6a-180">Administração da UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="14f6a-180">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="14f6a-181">Operações para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="14f6a-181">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





