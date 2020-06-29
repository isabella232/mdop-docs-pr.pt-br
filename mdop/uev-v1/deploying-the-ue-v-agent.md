---
title: Implantação do agente da UE-V
description: Implantação do agente da UE-V
author: dansimp
ms.assetid: ec1c16c4-4be0-41ff-93bc-3e2b1afb5832
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 19f3b798ad7d3a43b0a274a25dd97b651435de51
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800021"
---
# <span data-ttu-id="6f79a-103">Implantação do agente da UE-V</span><span class="sxs-lookup"><span data-stu-id="6f79a-103">Deploying the UE-V Agent</span></span>


<span data-ttu-id="6f79a-104">O Microsoft User Experience Virtualization (UE-V) Agent deve ser executado em cada computador que usa o UE-V para transferir o aplicativo e as configurações do Windows.</span><span class="sxs-lookup"><span data-stu-id="6f79a-104">The Microsoft User Experience Virtualization (UE-V) agent must run on each computer that uses UE-V to roam application and Windows settings.</span></span> <span data-ttu-id="6f79a-105">Um único arquivo de instalação, AgentSetup.exe, instala o UE-V Agent nos sistemas operacionais de 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="6f79a-105">A single installer file, AgentSetup.exe, installs the UE-V agent on both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="6f79a-106">Os parâmetros de linha de comando do UE-V Agent são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="6f79a-106">The command-line parameters of the UE-V Agent are the following:</span></span>

**<span data-ttu-id="6f79a-107">Parâmetros de linha de comando AgentSetup.exe</span><span class="sxs-lookup"><span data-stu-id="6f79a-107">AgentSetup.exe command-line parameters</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="6f79a-108">Parâmetro de linha de comando</span><span class="sxs-lookup"><span data-stu-id="6f79a-108">Command-line parameter</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="6f79a-109">Definição</span><span class="sxs-lookup"><span data-stu-id="6f79a-109">Definition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="6f79a-110">Observações</span><span class="sxs-lookup"><span data-stu-id="6f79a-110">Notes</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6f79a-111">/Help ou/h ou/?</span><span class="sxs-lookup"><span data-stu-id="6f79a-111">/help or /h or /?</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f79a-112">Exibe a caixa de diálogo AgentSetup.exe uso.</span><span class="sxs-lookup"><span data-stu-id="6f79a-112">Displays the AgentSetup.exe usage dialog.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6f79a-113">SettingsStoragePath</span><span class="sxs-lookup"><span data-stu-id="6f79a-113">SettingsStoragePath</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f79a-114">Indica o caminho UNC (Convenção Universal de nomenclatura) que define onde as configurações são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="6f79a-114">Indicates the Universal Naming Convention (UNC) path that defines where settings are stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f79a-115">as variáveis de ambiente% username% ou% computernamename% são aceitas.</span><span class="sxs-lookup"><span data-stu-id="6f79a-115">%username% or %computername% environment variables are accepted.</span></span> <span data-ttu-id="6f79a-116">O script pode exigir variáveis de escape.</span><span class="sxs-lookup"><span data-stu-id="6f79a-116">Scripting may require escaped variables.</span></span></p>
<p><strong><span data-ttu-id="6f79a-117">Padrão </strong> : &lt; nenhum &gt; (Active Directory User Home)</span><span class="sxs-lookup"><span data-stu-id="6f79a-117">Default</strong>: &lt;none&gt; (Active Directory user home)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6f79a-118">SettingsTemplateCatalogPath</span><span class="sxs-lookup"><span data-stu-id="6f79a-118">SettingsTemplateCatalogPath</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f79a-119">Indica o caminho UNC (Convenção Universal de nomenclatura) que define o local verificado para novos modelos de local de configurações.</span><span class="sxs-lookup"><span data-stu-id="6f79a-119">Indicates the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f79a-120">Só é necessário para modelos de local de configurações personalizadas</span><span class="sxs-lookup"><span data-stu-id="6f79a-120">Only required for custom settings location templates</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6f79a-121">RegisterMSTemplates</span><span class="sxs-lookup"><span data-stu-id="6f79a-121">RegisterMSTemplates</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f79a-122">Especifica se os modelos padrão da Microsoft devem ser registrados durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="6f79a-122">Specifies whether the default Microsoft templates should be registered during installation.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f79a-123">Verdadeiro | Falsas</span><span class="sxs-lookup"><span data-stu-id="6f79a-123">True | False</span></span></p>
<p><strong><span data-ttu-id="6f79a-124">Padrão </strong> : verdadeiro</span><span class="sxs-lookup"><span data-stu-id="6f79a-124">Default</strong>: True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6f79a-125">SyncMethod</span><span class="sxs-lookup"><span data-stu-id="6f79a-125">SyncMethod</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f79a-126">Especifica qual método de sincronização deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="6f79a-126">Specifies which synchronization method should be used.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f79a-127">OfflineFiles | Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6f79a-127">OfflineFiles | None</span></span></p>
<p><strong><span data-ttu-id="6f79a-128">Padrão </strong> : OfflineFiles</span><span class="sxs-lookup"><span data-stu-id="6f79a-128">Default</strong>: OfflineFiles</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6f79a-129">SyncTimeoutInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="6f79a-129">SyncTimeoutInMilliseconds</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f79a-130">Especifica o número de milissegundos que o computador aguarda antes do tempo limite quando ele recupera as configurações de usuário do local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="6f79a-130">Specifies the number of milliseconds that the computer waits before timeout when it retrieves user settings from the settings storage location.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="6f79a-131">Padrão </strong> : 2000 milissegundos</span><span class="sxs-lookup"><span data-stu-id="6f79a-131">Default</strong>: 2000 milliseconds</span></span></p>
<p><span data-ttu-id="6f79a-132">(Aguarde até 2 segundos)</span><span class="sxs-lookup"><span data-stu-id="6f79a-132">(wait up to 2 seconds)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6f79a-133">SyncEnabled</span><span class="sxs-lookup"><span data-stu-id="6f79a-133">SyncEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f79a-134">Especifica se a sincronização de UE-V está habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="6f79a-134">Specifies whether UE-V synchronization is enabled or disabled.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f79a-135">Verdadeiro | Falsas</span><span class="sxs-lookup"><span data-stu-id="6f79a-135">True | False</span></span></p>
<p><strong><span data-ttu-id="6f79a-136">Padrão </strong> : verdadeiro</span><span class="sxs-lookup"><span data-stu-id="6f79a-136">Default</strong>: True</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6f79a-137">MaxPackageSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="6f79a-137">MaxPackageSizeInBytes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f79a-138">Especifica um tamanho de arquivo de pacote de configurações em bytes quando o UE-V Agent informa que os arquivos excedem o limite.</span><span class="sxs-lookup"><span data-stu-id="6f79a-138">Specifies a settings package file size in bytes when the UE-V agent reports that files exceed the threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f79a-139">&lt;tamanho&gt;</span><span class="sxs-lookup"><span data-stu-id="6f79a-139">&lt;size&gt;</span></span></p>
<p><strong><span data-ttu-id="6f79a-140">Padrão </strong> : nenhum (sem limite de aviso)</span><span class="sxs-lookup"><span data-stu-id="6f79a-140">Default</strong>: none (no warning threshold)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6f79a-141">CEIPEnabled</span><span class="sxs-lookup"><span data-stu-id="6f79a-141">CEIPEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f79a-142">Especifica a configuração de participação no programa de aperfeiçoamento da experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="6f79a-142">Specifies the setting for participation in the Customer Experience Improvement program.</span></span> <span data-ttu-id="6f79a-143">Se definido como true, as informações do instalador serão carregadas no site do programa de aperfeiçoamento da experiência do usuário da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6f79a-143">If set to true, then installer information is uploaded to the Microsoft Customer Experience Improvement Program site.</span></span> <span data-ttu-id="6f79a-144">Se definido como false, nenhuma informação será carregada.</span><span class="sxs-lookup"><span data-stu-id="6f79a-144">If set to false, then no information is uploaded.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f79a-145">Verdadeiro | Falsas</span><span class="sxs-lookup"><span data-stu-id="6f79a-145">True | False</span></span></p>
<p><strong><span data-ttu-id="6f79a-146">Padrão </strong> : falso</span><span class="sxs-lookup"><span data-stu-id="6f79a-146">Default</strong>: False</span></span></p>
<p><strong><span data-ttu-id="6f79a-147">No Windows 7 </strong> : verdadeiro</span><span class="sxs-lookup"><span data-stu-id="6f79a-147">On Windows 7</strong>: True</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6f79a-148">Durante a instalação, o parâmetro de linha de comando SettingsStoragePath especifica o local de armazenamento de configurações para os valores de configurações.</span><span class="sxs-lookup"><span data-stu-id="6f79a-148">During installation, the SettingsStoragePath command-line parameter specifies the settings storage location for the settings values.</span></span> <span data-ttu-id="6f79a-149">Um local de armazenamento de configurações pode ser definido antes da implantação do UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="6f79a-149">A settings storage location can be defined before deploying the UE-V Agent.</span></span> <span data-ttu-id="6f79a-150">Se nenhuma localização de armazenamento de configurações estiver definida, o UE-V usará o diretório inicial de usuário do Active Directory como o local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="6f79a-150">If no settings storage location is defined, then UE-V uses the Active Directory user Home Directory as the settings storage location.</span></span> <span data-ttu-id="6f79a-151">Ao especificar a configuração SettingsStoragePath durante a configuração e usar o% username% como parte do valor, isso fará o roaming da mesma experiência de configurações do usuário em todos os computadores ou sessões nos quais um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="6f79a-151">When you specify the SettingsStoragePath configuration during setup and use the %username% as part of the value, this will roam the same user settings experience on all computers or sessions that a user logs into.</span></span> <span data-ttu-id="6f79a-152">Se você especificar as variáveis%username%\\%ComputerName% como parte do valor SettingsStoragePath, isso irá preservar a experiência de configurações para cada computador.</span><span class="sxs-lookup"><span data-stu-id="6f79a-152">If you specify the %username%\\%computername% variables as part of the SettingsStoragePath value, this will preserve the settings experience for each computer.</span></span>

<span data-ttu-id="6f79a-153">Os arquivos do Windows Installer (. msi) específicos da arquitetura são fornecidos para a instalação do UE-V Agent, além do instalador combinado de 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="6f79a-153">Architecture-specific Windows Installer (.msi) files are provided for the UE-V agent installation in addition to the combined 32-bit and 64-bit installer.</span></span> <span data-ttu-id="6f79a-154">Os arquivos de instalação do AgentSetupx86.msi ou AgentSetupx64.msi são menores do que o arquivo AgentSetup.exe e podem simplificar as implantações do agente.</span><span class="sxs-lookup"><span data-stu-id="6f79a-154">The AgentSetupx86.msi or AgentSetupx64.msi install files are smaller than the AgentSetup.exe file and might streamline the agent deployments.</span></span> <span data-ttu-id="6f79a-155">Os parâmetros de linha de comando para o instalador do AgentSetup.exe são suportados para a instalação do Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="6f79a-155">The command-line parameters for the AgentSetup.exe installer are supported for the Windows Installer (.msi) installation.</span></span>

<span data-ttu-id="6f79a-156">**Observação**  Durante a instalação ou desinstalação do agente do UE-V, você pode usar o arquivo AgentSetup.exe ou &lt; o &gt; arquivo AgentSetup Arch. msi, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="6f79a-156">**Note** During UE-V agent installation or uninstallation you can either use the AgentSetup.exe file or the AgentSetup&lt;arch&gt;.msi file, but not both.</span></span> <span data-ttu-id="6f79a-157">O mesmo arquivo deve ser usado para desinstalar o UE-V Agent, pois foi usado para instalar o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="6f79a-157">The same file must be used to uninstall the UE-V Agent as it was used to install the UE-V Agent.</span></span>

 

<span data-ttu-id="6f79a-158">Certifique-se de usar o formato de variável correto ao instalar o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="6f79a-158">Be sure to use the correct variable format when you install the UE-V agent.</span></span> <span data-ttu-id="6f79a-159">A tabela a seguir fornece exemplos de opções de implantação para usar os arquivos de instalação do AgentSetup.exe ou do Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="6f79a-159">The following table provides examples of deployment options for using the AgentSetup.exe or the Windows Installer (.msi) installation files.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="6f79a-160">Tipo de implementação</span><span class="sxs-lookup"><span data-stu-id="6f79a-160">Deployment type</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="6f79a-161">Descrição da implantação</span><span class="sxs-lookup"><span data-stu-id="6f79a-161">Deployment description</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="6f79a-162">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6f79a-162">Example</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6f79a-163">Prompt de comando</span><span class="sxs-lookup"><span data-stu-id="6f79a-163">Command prompt</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f79a-164">Ao instalar o UE-V Agent a partir de um prompt de comando, use o formato de variável% ^ username%.</span><span class="sxs-lookup"><span data-stu-id="6f79a-164">When you install the UE-V agent from a command prompt, use the %^username% variable format.</span></span> <span data-ttu-id="6f79a-165">Se forem necessárias aspas por causa de espaços no caminho de armazenamento de configurações, use um arquivo de script em lotes para implantação.</span><span class="sxs-lookup"><span data-stu-id="6f79a-165">If quotation marks are needed because of spaces in the settings storage path, use a batch script file for deployment.</span></span></p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6f79a-166">Script em lotes</span><span class="sxs-lookup"><span data-stu-id="6f79a-166">Batch script</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f79a-167">Ao instalar o UE-V Agent a partir de um arquivo de script em lotes, use o formato de variável%% username%%.</span><span class="sxs-lookup"><span data-stu-id="6f79a-167">When you install the UE-V Agent from a batch script file, use the %%username%% variable format.</span></span> <span data-ttu-id="6f79a-168">Se você usar esse método de instalação, deverá escapar a variável com os caracteres%%.</span><span class="sxs-lookup"><span data-stu-id="6f79a-168">If you use this install method, you must escape the variable with the %% characters.</span></span> <span data-ttu-id="6f79a-169">Sem esse caractere, o script expande a variável username no tempo de instalação, em vez do tempo de execução, fazendo com que o UE-V use um único local de armazenamento de configurações para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="6f79a-169">Without this character, the script expands the username variable at install time, rather than at run time, causing UE-V to use a single settings storage location for all users.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6f79a-170">PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f79a-170">PowerShell</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f79a-171">Ao instalar o UE-V Agent a partir de um prompt do PowerShell ou de um script do PowerShell, use o formato de variável% username%.</span><span class="sxs-lookup"><span data-stu-id="6f79a-171">When you install the UE-V agent from a PowerShell prompt or PowerShell script, use the %username% variable format.</span></span></p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6f79a-172">Distribuição de software eletrônico, como a implantação da implantação de software do Configuration Manager)</span><span class="sxs-lookup"><span data-stu-id="6f79a-172">Electronic software distribution, such as deployment of Configuration Manager Software Deployment)</span></span></p></td>
<td align="left"><p><span data-ttu-id="6f79a-173">Ao instalar o UE-V Agent com o Configuration Manager, use o formato de variável ^% username ^%.</span><span class="sxs-lookup"><span data-stu-id="6f79a-173">When you install the UE-V Agent with Configuration Manager, use the ^%username^% variable format.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6f79a-174">**Observação**  A instalação do agente U-VA exige direitos de administrador, e o computador exigirá uma reinicialização antes que o UE-V Agent possa ser executado.</span><span class="sxs-lookup"><span data-stu-id="6f79a-174">**Note** The installation of the U-EV Agent requires Administrator rights and the computer will require a restart before the UE-V agent can run.</span></span>

 

## <span data-ttu-id="6f79a-175">Métodos de implantação do agente do UE-V em um compartilhamento de rede</span><span class="sxs-lookup"><span data-stu-id="6f79a-175">UE-V Agent deployment methods from a network share</span></span>


<span data-ttu-id="6f79a-176">Você pode usar os seguintes métodos para implantar o UE-V Agent:</span><span class="sxs-lookup"><span data-stu-id="6f79a-176">You can use the following methods to deploy the UE-V agent:</span></span>

-   <span data-ttu-id="6f79a-177">Uma solução ESD (Electronic Software Distribution) que pode instalar um arquivo Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="6f79a-177">An electronic software distribution (ESD) solution that can install a Windows Installer (.msi) file.</span></span>

-   <span data-ttu-id="6f79a-178">Um script de instalação que faz referência ao arquivo do Windows Installer (. msi) que está armazenado centralmente em um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="6f79a-178">An installation script that references the Windows Installer (.msi) file that is stored centrally on a share.</span></span>

-   <span data-ttu-id="6f79a-179">Executar manualmente o programa de instalação no computador.</span><span class="sxs-lookup"><span data-stu-id="6f79a-179">Manually running the installation program on the computer.</span></span>

<span data-ttu-id="6f79a-180">Para implantar o UE-V Agent a partir de um compartilhamento de rede, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="6f79a-180">To deploy the UE-V agent from a network share, use the following steps:</span></span>

**<span data-ttu-id="6f79a-181">Para instalar e configurar o UE-V Agent a partir de um compartilhamento de rede</span><span class="sxs-lookup"><span data-stu-id="6f79a-181">To install and configure the UE-V Agent from a network share</span></span>**

1.  <span data-ttu-id="6f79a-182">Testar o arquivo de instalação do agente do UE-V (AgentSetup.exe) em um compartilhamento de rede ao qual os usuários têm permissão "ler".</span><span class="sxs-lookup"><span data-stu-id="6f79a-182">Stage the UE-V agent installation file (AgentSetup.exe) on a network share to which users have “read” permission.</span></span>

2.  <span data-ttu-id="6f79a-183">Implante um script para os computadores dos usuários que instalam o UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="6f79a-183">Deploy a script to user computers that installs the UE-V agent.</span></span> <span data-ttu-id="6f79a-184">O script deve especificar o local de armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="6f79a-184">The script should specify the settings storage location.</span></span>

**<span data-ttu-id="6f79a-185">Atualize o UE-V Agent</span><span class="sxs-lookup"><span data-stu-id="6f79a-185">Update the UE-V Agent</span></span>**

<span data-ttu-id="6f79a-186">As atualizações do software de agente UE-V serão fornecidas por meio do Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="6f79a-186">Updates for the UE-V agent software will be provided through Microsoft Update.</span></span> <span data-ttu-id="6f79a-187">Durante uma atualização do UE-V Agent, o grupo padrão de modelos de localização de configurações para aplicativos e configurações do Windows comuns podem ser atualizados.</span><span class="sxs-lookup"><span data-stu-id="6f79a-187">During a UE-V agent upgrade, the default group of settings location templates for common Microsoft applications and Windows settings may be updated.</span></span> <span data-ttu-id="6f79a-188">As atualizações do UE-V Agent podem ser implantadas usando a infraestrutura ESD (Enterprise Software Distribution).</span><span class="sxs-lookup"><span data-stu-id="6f79a-188">UE-V agent updates can be deployed by using Enterprise Software Distribution (ESD) infrastructure.</span></span>

## <span data-ttu-id="6f79a-189">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6f79a-189">Related topics</span></span>


[<span data-ttu-id="6f79a-190">Implantação da UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="6f79a-190">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="6f79a-191">Configurações com suporte para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="6f79a-191">Supported Configurations for UE-V 1.0</span></span>](supported-configurations-for-ue-v-10.md)

[<span data-ttu-id="6f79a-192">Implantação da localização do armazenamento de configurações para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="6f79a-192">Deploying the Settings Storage Location for UE-V 1.0</span></span>](deploying-the-settings-storage-location-for-ue-v-10.md)

[<span data-ttu-id="6f79a-193">Instalação do gerador da UE-V</span><span class="sxs-lookup"><span data-stu-id="6f79a-193">Installing the UE-V Generator</span></span>](installing-the-ue-v-generator.md)

<span data-ttu-id="6f79a-194">Implantar o agente de virtualização da experiência do usuário</span><span class="sxs-lookup"><span data-stu-id="6f79a-194">Deploy the User Experience Virtualization Agent</span></span>
 

 





