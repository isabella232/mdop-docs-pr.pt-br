---
title: Gerenciamento de agente e pacotes da UE-V 1.0 com o PowerShell e o WMI
description: Gerenciamento de agente e pacotes da UE-V 1.0 com o PowerShell e o WMI
author: dansimp
ms.assetid: c8989b01-1769-4e69-82b1-4aadb261d2d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 79268e3384aaaf08bdd4e9b92d74b039ce96596a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797497"
---
# <span data-ttu-id="d31b0-103">Gerenciamento de agente e pacotes da UE-V 1.0 com o PowerShell e o WMI</span><span class="sxs-lookup"><span data-stu-id="d31b0-103">Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI</span></span>


<span data-ttu-id="d31b0-104">Você pode usar o WMI e o PowerShell para gerenciar a configuração e o comportamento de sincronização do agente do Microsoft User Experience Virtualization (UE-V).</span><span class="sxs-lookup"><span data-stu-id="d31b0-104">You can use WMI and PowerShell to manage Microsoft User Experience Virtualization (UE-V) Agent configuration and synchronization behavior.</span></span>

**<span data-ttu-id="d31b0-105">Como implantar o UE-V Agent com o PowerShell</span><span class="sxs-lookup"><span data-stu-id="d31b0-105">How to deploy the UE-V agent with PowerShell</span></span>**

1.  <span data-ttu-id="d31b0-106">Testar o arquivo do instalador do UE-V em um compartilhamento de rede acessível.</span><span class="sxs-lookup"><span data-stu-id="d31b0-106">Stage the UE-V installer file in an accessible network share.</span></span>

    **<span data-ttu-id="d31b0-107">Observação</span><span class="sxs-lookup"><span data-stu-id="d31b0-107">Note</span></span>**  
    <span data-ttu-id="d31b0-108">Use AgentSetup.exe para implantar as versões de 32 bits e de 64 bits do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="d31b0-108">Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="d31b0-109">Os arquivos do Windows Installer versões, AgentSetupx86.msi e AgentSetupx64.msi, estão disponíveis para cada arquitetura.</span><span class="sxs-lookup"><span data-stu-id="d31b0-109">Windows Installer Files versions, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="d31b0-110">Para desinstalar o UE-V Agent posteriormente usando o arquivo de instalação, você deve usar o mesmo tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="d31b0-110">To uninstall the UE-V Agent at a later time using the installation file, you must use the same file type.</span></span>



2.  <span data-ttu-id="d31b0-111">Use um dos seguintes comandos do PowerShell para instalar o agente.</span><span class="sxs-lookup"><span data-stu-id="d31b0-111">Use one of the following PowerShell commands to install the agent.</span></span>

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**<span data-ttu-id="d31b0-112">Como configurar o UE-V Agent com o PowerShell</span><span class="sxs-lookup"><span data-stu-id="d31b0-112">How to configure the UE-V Agent with PowerShell</span></span>**

1.  <span data-ttu-id="d31b0-113">Use uma conta com direitos de administrador para abrir uma janela do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d31b0-113">Use an account with administrator rights to open a PowerShell window.</span></span> <span data-ttu-id="d31b0-114">Importe o módulo do PowerShell do UE-V usando o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="d31b0-114">Import the UE-V PowerShell module by using the following command.</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="d31b0-115">Use os comandos do PowerShell a seguir para configurar o agente.</span><span class="sxs-lookup"><span data-stu-id="d31b0-115">Use the following PowerShell commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="d31b0-116">Comando do PowerShell</span><span class="sxs-lookup"><span data-stu-id="d31b0-116">PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="d31b0-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="d31b0-117">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="d31b0-118">Get-UevConfiguration</span><span class="sxs-lookup"><span data-stu-id="d31b0-118">Get-UevConfiguration</span></span></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-119">Veja as configurações efetivas do agente do UE-V.</span><span class="sxs-lookup"><span data-stu-id="d31b0-119">View the effective UE-V agent settings.</span></span> <span data-ttu-id="d31b0-120">As configurações específicas do usuário têm precedência sobre as configurações do computador.</span><span class="sxs-lookup"><span data-stu-id="d31b0-120">User-specific settings have precedence over the computer settings.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d31b0-121">Get-UevConfiguration-CurrentComputerUser</span><span class="sxs-lookup"><span data-stu-id="d31b0-121">Get-UevConfiguration - CurrentComputerUser</span></span></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-122">Exiba os valores das configurações do UE-V Agent somente para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="d31b0-122">View the UE-V agent settings values for the current user only.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="d31b0-123">Get-UevConfiguration-computador</span><span class="sxs-lookup"><span data-stu-id="d31b0-123">Get-UevConfiguration -Computer</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-124">Exiba os valores das configurações de configuração do UE-V Agent para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="d31b0-124">View the UE-V agent configuration settings values for all users on the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d31b0-125">Set-UevConfiguration-caminho SettingsStoragePath do computador &lt; para _settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="d31b0-125">Set-UevConfiguration -Computer -SettingsStoragePath &lt;path to _settings_storage_location&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-126">Definir um local de armazenamento de configurações por computador.</span><span class="sxs-lookup"><span data-stu-id="d31b0-126">Define a per-computer settings storage location.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="d31b0-127">Set-UevConfiguration-CurrentComputerUser-SettingsStoragePath &lt; caminho para _settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="d31b0-127">Set-UevConfiguration -CurrentComputerUser -SettingsStoragePath &lt;path to _settings_storage_location&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-128">Definir um local de armazenamento de configurações por usuário.</span><span class="sxs-lookup"><span data-stu-id="d31b0-128">Define a per-user settings storage location.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d31b0-129">Set-UevConfiguration-computador-SyncTimeoutInMilliseconds &lt; Timeout em milissegundos&gt;</span><span class="sxs-lookup"><span data-stu-id="d31b0-129">Set-UevConfiguration -Computer -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-130">Definir o tempo limite de sincronização em milissegundos</span><span class="sxs-lookup"><span data-stu-id="d31b0-130">Set the synchronization timeout in milliseconds</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="d31b0-131">Set-UevConfiguration-CurrentComputerUser-SyncTimeoutInMilliseconds &lt; Timeout em milissegundos&gt;</span><span class="sxs-lookup"><span data-stu-id="d31b0-131">Set-UevConfiguration -CurrentComputerUser -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-132">Definir o tempo limite de sincronização do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="d31b0-132">Set the synchronization timeout for the current user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d31b0-133">Set-UevConfiguration-Computer-MaxPackageSizeInBytes &lt; size in bytes&gt;</span><span class="sxs-lookup"><span data-stu-id="d31b0-133">Set-UevConfiguration -Computer -MaxPackageSizeInBytes &lt;size in bytes&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-134">Configurar o UE-V Agent para denunciar quando um tamanho de arquivo de pacote de configurações atingir um limite definido.</span><span class="sxs-lookup"><span data-stu-id="d31b0-134">Configure the UE-V agent to report when a settings package file size reaches a defined threshold.</span></span> <span data-ttu-id="d31b0-135">Defina o tamanho do pacote de limite em bytes.</span><span class="sxs-lookup"><span data-stu-id="d31b0-135">Set the threshold package size in bytes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="d31b0-136">Set-UevConfiguration-CurrentComputerUser-MaxPackageSizeInBytes &lt; tamanho em bytes&gt;</span><span class="sxs-lookup"><span data-stu-id="d31b0-136">Set-UevConfiguration -CurrentComputerUser -MaxPackageSizeInBytes &lt;size in bytes&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-137">Defina o limite de aviso do tamanho do pacote para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="d31b0-137">Set the package size warning threshold for the current user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d31b0-138">Set-UevConfiguration – computador – SettingsTemplateCatalogPath &lt; caminho para catálogo&gt;</span><span class="sxs-lookup"><span data-stu-id="d31b0-138">Set-UevConfiguration –Computer –SettingsTemplateCatalogPath &lt;path to catalog&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-139">Defina o caminho do catálogo de modelos de configurações.</span><span class="sxs-lookup"><span data-stu-id="d31b0-139">Set the settings template catalog path.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="d31b0-140">Set-UevConfiguration-método de sincronização de computador-SyncMethod &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="d31b0-140">Set-UevConfiguration -Computer -SyncMethod &lt;sync method&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-141">Defina o método de sincronização: OfflineFiles ou None.</span><span class="sxs-lookup"><span data-stu-id="d31b0-141">Set the synchronization method: OfflineFiles or None.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d31b0-142">Set-UevConfiguration-CurrentComputerUser-SyncMethod &lt; método de sincronização&gt;</span><span class="sxs-lookup"><span data-stu-id="d31b0-142">Set-UevConfiguration -CurrentComputerUser -SyncMethod &lt;sync method&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-143">Defina o método de sincronização para o usuário atual: OfflineFiles ou None.</span><span class="sxs-lookup"><span data-stu-id="d31b0-143">Set the synchronization method for the current user: OfflineFiles or None.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="d31b0-144">Set-UEVConfiguration-computador – EnableSettingsImportNotify</span><span class="sxs-lookup"><span data-stu-id="d31b0-144">Set-UEVConfiguration -Computer –EnableSettingsImportNotify</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-145">Permitir que a notificação ocorra quando a importação das configurações do usuário for adiada.</span><span class="sxs-lookup"><span data-stu-id="d31b0-145">Enable notification to occur when the import of user settings is delayed.</span></span></p>
    <p><span data-ttu-id="d31b0-146">Use – DisableSettingsImportNotify para desabilitar a notificação.</span><span class="sxs-lookup"><span data-stu-id="d31b0-146">Use –DisableSettingsImportNotify to disable notification.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d31b0-147">Set-UEVConfiguration-CurrentComputerUser-EnableSettingsImportNotify</span><span class="sxs-lookup"><span data-stu-id="d31b0-147">Set-UEVConfiguration - CurrentComputerUser -EnableSettingsImportNotify</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-148">Habilite a notificação para o usuário atual quando a importação das configurações do usuário for adiada.</span><span class="sxs-lookup"><span data-stu-id="d31b0-148">Enable notification for the current user when the import of user settings is delayed.</span></span></p>
    <p><span data-ttu-id="d31b0-149">Use – DisableSettingsImportNotify para desabilitar a notificação.</span><span class="sxs-lookup"><span data-stu-id="d31b0-149">Use –DisableSettingsImportNotify to disable notification.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="d31b0-150">Set-UEVConfiguration-computador-SettingsImportNotifyDelayInSeconds</span><span class="sxs-lookup"><span data-stu-id="d31b0-150">Set-UEVConfiguration -Computer -SettingsImportNotifyDelayInSeconds</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-151">Especificar o tempo em segundos antes de o usuário ser notificado</span><span class="sxs-lookup"><span data-stu-id="d31b0-151">Specify the time in seconds before the user is notified</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d31b0-152">Set-UEVConfiguration-CurrentComputerUser-SettingsImportNotifyDelayInSeconds</span><span class="sxs-lookup"><span data-stu-id="d31b0-152">Set-UEVConfiguration - CurrentComputerUser -SettingsImportNotifyDelayInSeconds</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-153">Especifique o tempo em segundos antes da notificação para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="d31b0-153">Specify the time in seconds before notification for the current user.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="d31b0-154">Set-UevConfiguration – computador – DisableSync</span><span class="sxs-lookup"><span data-stu-id="d31b0-154">Set-UevConfiguration –Computer –DisableSync</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-155">Desative o UE-V para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="d31b0-155">Disable UE-V for all the users on the computer.</span></span></p>
    <p><span data-ttu-id="d31b0-156">Use – EnableSync para habilitar ou desabilitar novamente.</span><span class="sxs-lookup"><span data-stu-id="d31b0-156">Use –EnableSync to enable or re-enable.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d31b0-157">Set-UevConfiguration – CurrentComputerUser-DisableSync</span><span class="sxs-lookup"><span data-stu-id="d31b0-157">Set-UevConfiguration –CurrentComputerUser -DisableSync</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-158">Desative o UE-V para o usuário atual no computador.</span><span class="sxs-lookup"><span data-stu-id="d31b0-158">Disable UE-V for the current user on the computer.</span></span></p>
    <p><span data-ttu-id="d31b0-159">Use – EnableSync para habilitar ou desabilitar novamente.</span><span class="sxs-lookup"><span data-stu-id="d31b0-159">Use –EnableSync to enable or re-enable.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="d31b0-160">Clear-UevConfiguration – nome da &lt; configuração do computador&gt;</span><span class="sxs-lookup"><span data-stu-id="d31b0-160">Clear-UevConfiguration –Computer -&lt;setting name&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-161">Desmarque uma configuração específica para todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="d31b0-161">Clear a specific setting for all users on the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d31b0-162">Clear-UevConfiguration – CurrentComputerUser- &lt; nome de configuração&gt;</span><span class="sxs-lookup"><span data-stu-id="d31b0-162">Clear-UevConfiguration –CurrentComputerUser -&lt;setting name&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-163">Limpar uma configuração específica somente para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="d31b0-163">Clear a specific setting for the current user only.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="d31b0-164">Export-UevConfiguration &lt; arquivo de migração de configurações&gt;</span><span class="sxs-lookup"><span data-stu-id="d31b0-164">Export-UevConfiguration &lt;settings migration file&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-165">Exporte a configuração do computador UE-V para um arquivo de migração de configurações.</span><span class="sxs-lookup"><span data-stu-id="d31b0-165">Export the UE-V computer configuration to a settings migration file.</span></span> <span data-ttu-id="d31b0-166">A extensão do arquivo deve ser ". UEV".</span><span class="sxs-lookup"><span data-stu-id="d31b0-166">The extension of the file must be “.uev”.</span></span></p>
    <p><span data-ttu-id="d31b0-167">O cmdlet Export exporta todas as configurações do agente do UE-V que são configuráveis com o parâmetro-Computer.</span><span class="sxs-lookup"><span data-stu-id="d31b0-167">The export cmdlet exports all UE-V agent settings that are configurable with the -computer parameter.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d31b0-168">Importar-arquivo de migração de configurações do UevConfiguration &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="d31b0-168">Import-UevConfiguration &lt;settings migration file&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-169">Importar a configuração do computador UE-V de um arquivo de migração de configurações (arquivo. UEV).</span><span class="sxs-lookup"><span data-stu-id="d31b0-169">Import the UE-V computer configuration from a settings migration file (.uev file).</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="d31b0-170">Como exportar as configurações do pacote do UE-V e reparar modelos do UE-V com o PowerShell</span><span class="sxs-lookup"><span data-stu-id="d31b0-170">How to export UE-V package settings and repair UE-V templates with PowerShell</span></span>**

1.  <span data-ttu-id="d31b0-171">Abra uma janela do PowerShell como administrador.</span><span class="sxs-lookup"><span data-stu-id="d31b0-171">Open a PowerShell window as an Administrator.</span></span> <span data-ttu-id="d31b0-172">Importe o módulo do PowerShell do UE-V com o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="d31b0-172">Import the UE-V PowerShell module with the following command.</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="d31b0-173">Use os comandos do PowerShell a seguir para configurar o agente.</span><span class="sxs-lookup"><span data-stu-id="d31b0-173">Use the following PowerShell commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="d31b0-174">Comando do PowerShell</span><span class="sxs-lookup"><span data-stu-id="d31b0-174">PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="d31b0-175">Descrição</span><span class="sxs-lookup"><span data-stu-id="d31b0-175">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="d31b0-176">Export-UevPackage MicrosoftCalculator6. pkgx</span><span class="sxs-lookup"><span data-stu-id="d31b0-176">Export-UevPackage MicrosoftCalculator6.pkgx</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-177">Extrai as configurações de um arquivo de pacote calculadora da Microsoft e converte-as em um formato legível por pessoas em XML.</span><span class="sxs-lookup"><span data-stu-id="d31b0-177">Extracts the settings from a Microsoft Calculator package file and converts them into a human-readable format in XML.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d31b0-178">Reparar-UevTemplateIndex</span><span class="sxs-lookup"><span data-stu-id="d31b0-178">Repair-UevTemplateIndex</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-179">Repara o índice dos modelos de local de configurações do UE-V.</span><span class="sxs-lookup"><span data-stu-id="d31b0-179">Repairs the index of the UE-V settings location templates.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="d31b0-180">Como configurar o UE-V Agent com WMI</span><span class="sxs-lookup"><span data-stu-id="d31b0-180">How to configure the UE-V Agent with WMI</span></span>**

1.  <span data-ttu-id="d31b0-181">A virtualização da experiência do usuário fornece o seguinte conjunto de comandos WMI.</span><span class="sxs-lookup"><span data-stu-id="d31b0-181">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="d31b0-182">Os administradores podem usar essa interface para configurar o UE-V Agent a partir da linha de comando e automatizar tarefas típicas de configuração.</span><span class="sxs-lookup"><span data-stu-id="d31b0-182">Administrators can use this interface to configure the UE-V agent from the command line and automate typical configuration tasks.</span></span>

    <span data-ttu-id="d31b0-183">Use uma conta com direitos de administrador para abrir uma janela do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d31b0-183">Use an account with administrator rights to open a PowerShell window.</span></span>

2.  <span data-ttu-id="d31b0-184">Use os seguintes comandos WMI para configurar o agente.</span><span class="sxs-lookup"><span data-stu-id="d31b0-184">Use the following WMI commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="d31b0-185">Comando do PowerShell</span><span class="sxs-lookup"><span data-stu-id="d31b0-185">PowerShell command</span></span></th>
    <th align="left"><span data-ttu-id="d31b0-186">Descrição</span><span class="sxs-lookup"><span data-stu-id="d31b0-186">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d31b0-187">Get-WmiObject-configuração do root\Microsoft\UEV de namespace</span><span class="sxs-lookup"><span data-stu-id="d31b0-187">Get-WmiObject -Namespace root\Microsoft\UEV Configuration</span></span></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-188">Exibir as configurações ativas do agente do UE-V.</span><span class="sxs-lookup"><span data-stu-id="d31b0-188">View the active UE-V agent settings.</span></span> <span data-ttu-id="d31b0-189">As configurações específicas do usuário têm precedência sobre as configurações do computador.</span><span class="sxs-lookup"><span data-stu-id="d31b0-189">User-specific settings have precedence over the computer settings.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="d31b0-190">Get-WmiObject-namespace root\Microsoft\UEV userconfiguration</span><span class="sxs-lookup"><span data-stu-id="d31b0-190">Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-191">Veja a configuração do UE-V Agent definida para o usuário.</span><span class="sxs-lookup"><span data-stu-id="d31b0-191">View the UE-V agent configuration that is defined for user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d31b0-192">Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d31b0-192">Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-193">Veja a configuração do UE-V Agent definida para o computador.</span><span class="sxs-lookup"><span data-stu-id="d31b0-193">View the UE-V agent configuration that is defined for computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="d31b0-194">$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d31b0-194">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="d31b0-195">$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="d31b0-195">$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</span></span></p>
    <p><span data-ttu-id="d31b0-196">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="d31b0-196">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-197">Definir um local de armazenamento de configurações por computador.</span><span class="sxs-lookup"><span data-stu-id="d31b0-197">Define a per-computer settings storage location.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d31b0-198">$config = Get-WmiObject-namespace root\Microsoft\UEV userconfiguration</span><span class="sxs-lookup"><span data-stu-id="d31b0-198">$config = Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</span></span></p>
    <p><span data-ttu-id="d31b0-199">$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="d31b0-199">$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</span></span></p>
    <p><span data-ttu-id="d31b0-200">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="d31b0-200">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-201">Definir um local de armazenamento de configurações por usuário.</span><span class="sxs-lookup"><span data-stu-id="d31b0-201">Define a per-user settings storage location.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="d31b0-202">$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d31b0-202">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="d31b0-203">$config. SyncTimeoutInMilliseconds = &lt; timeout_in_milliseconds&gt;</span><span class="sxs-lookup"><span data-stu-id="d31b0-203">$config.SyncTimeoutInMilliseconds = &lt;timeout_in_milliseconds&gt;</span></span></p>
    <p><span data-ttu-id="d31b0-204">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="d31b0-204">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-205">Defina o tempo limite de sincronização em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="d31b0-205">Set the synchronization timeout in milliseconds.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d31b0-206">$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d31b0-206">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="d31b0-207">$config. MaxPackageSizeInBytes = &lt; size_in_bytes&gt;</span><span class="sxs-lookup"><span data-stu-id="d31b0-207">$config.MaxPackageSizeInBytes = &lt;size_in_bytes&gt;</span></span></p>
    <p><span data-ttu-id="d31b0-208">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="d31b0-208">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-209">Configurar o UE-V Agent para denunciar quando um tamanho de arquivo de pacote de configurações atingir um limite definido.</span><span class="sxs-lookup"><span data-stu-id="d31b0-209">Configure the UE-V agent to report when a settings package file size reaches a defined threshold.</span></span> <span data-ttu-id="d31b0-210">Defina o tamanho do arquivo do pacote de limite em bytes.</span><span class="sxs-lookup"><span data-stu-id="d31b0-210">Set the threshold package file size in bytes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="d31b0-211">$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d31b0-211">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="d31b0-212">$config. SyncMethod = &lt; sync_method&gt;</span><span class="sxs-lookup"><span data-stu-id="d31b0-212">$config.SyncMethod = &lt;sync_method&gt;</span></span></p>
    <p><span data-ttu-id="d31b0-213">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="d31b0-213">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-214">Defina o método de sincronização: OfflineFiles ou None.</span><span class="sxs-lookup"><span data-stu-id="d31b0-214">Set the synchronization method: OfflineFiles or None.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d31b0-215">$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d31b0-215">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="d31b0-216">$config. &lt; definindo o &gt;  =  &lt; valor da configuração de nome&gt;</span><span class="sxs-lookup"><span data-stu-id="d31b0-216">$config.&lt;setting name&gt; = &lt;setting value&gt;</span></span></p>
    <p><span data-ttu-id="d31b0-217">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="d31b0-217">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-218">Atualize uma configuração específica por computador.</span><span class="sxs-lookup"><span data-stu-id="d31b0-218">Update a specific per-computer setting.</span></span> <span data-ttu-id="d31b0-219">Para limpar a configuração, use $null como o valor de configuração.</span><span class="sxs-lookup"><span data-stu-id="d31b0-219">To clear the setting, use $null as the setting value.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="d31b0-220">$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d31b0-220">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="d31b0-221">$config. &lt; definindo o &gt;  =  &lt; valor da configuração de nome&gt;</span><span class="sxs-lookup"><span data-stu-id="d31b0-221">$config.&lt;setting name&gt; = &lt;setting value&gt;</span></span></p>
    <p><span data-ttu-id="d31b0-222">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="d31b0-222">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d31b0-223">Atualize uma configuração específica por usuário.</span><span class="sxs-lookup"><span data-stu-id="d31b0-223">Update a specific per-user setting.</span></span> <span data-ttu-id="d31b0-224">Para limpar a configuração, use $null como o valor de configuração.</span><span class="sxs-lookup"><span data-stu-id="d31b0-224">To clear the setting, use $null as the setting value.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and PowerShell, the defined configuration is stored in the registry in the following locations:

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

## <span data-ttu-id="d31b0-225">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d31b0-225">Related topics</span></span>


[<span data-ttu-id="d31b0-226">Administração da UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="d31b0-226">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="d31b0-227">Operações para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="d31b0-227">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)









