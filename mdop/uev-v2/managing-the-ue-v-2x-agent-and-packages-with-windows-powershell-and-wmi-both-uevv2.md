---
title: Gerenciando o agente e os pacotes do UE-V 2. x com o Windows PowerShell e o WMI
description: Gerenciando o agente e os pacotes do UE-V 2. x com o Windows PowerShell e o WMI
author: dansimp
ms.assetid: 56e6780b-8b2c-4717-91c8-2af63062ab75
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6a709d2c66266cf33b8e89ddd905aa0f21eb7dfe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799945"
---
# Gerenciando o agente e os pacotes do UE-V 2. x com o Windows PowerShell e o WMI


Você pode usar a instrumentação de gerenciamento do Windows (WMI) e o Windows PowerShell para gerenciar a configuração e o comportamento de sincronização do agente do Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1. Para obter uma lista completa dos cmdlets do PowerShell do UE-V, consulte [referência do cmdlet do UE-v 2](https://go.microsoft.com/fwlink/?LinkId=393495) ( https://go.microsoft.com/fwlink/?LinkId=393495) .

**Para implantar o UE-V Agent usando o Windows PowerShell**

1.  Testar o arquivo do instalador do UE-V em um compartilhamento de rede acessível.

    **Observação**  
    Use AgentSetup.exe para implantar as versões de 32 bits e de 64 bits do UE-V Agent. Os pacotes do Windows Installer, AgentSetupx86.msi e AgentSetupx64.msi, estão disponíveis para cada arquitetura. Para desinstalar o UE-V Agent posteriormente, usando o arquivo de instalação, você deve usar o mesmo tipo de arquivo.



2.  Use um dos seguintes comandos do Windows PowerShell para instalar o UE-V Agent.

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**Para configurar o UE-V Agent usando o Windows PowerShell**

1. Abra uma janela do Windows PowerShell. Para gerenciar as configurações do computador que afetam todos os usuários do computador usando o parâmetro *computador* , abra a janela com uma conta com direitos de administrador.

2. Use os seguintes comandos do Windows PowerShell para configurar o agente.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">comando do Windows PowerShell</th>
   <th align="left">Descrição</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration</code></p>
   <p></p></td>
   <td align="left"><p>Obtém as configurações efetivas do agente do UE-V. As configurações específicas do usuário têm precedência sobre as configurações do computador.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration - CurrentComputerUser</code></p>
   <p></p></td>
   <td align="left"><p>Obtém os valores das configurações do UE-V Agent somente para o usuário atual.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration -Computer</code></p></td>
   <td align="left"><p>Obtém os valores das configurações de configuração do UE-V Agent para todos os usuários do computador.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration -Details</code></p></td>
   <td align="left"><p>Obtém os detalhes para cada configuração. Exibe onde a configuração está configurada ou se usa o valor padrão. Será exibido se a configuração atual for válida.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –ContactITDescription &lt;IT description&gt;</code></p></td>
   <td align="left"><p>Define o texto que é exibido no centro de configurações da empresa para o link ajuda.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -ContactITUrl &lt;string&gt;</code></p></td>
   <td align="left"><p>Define a URL do link no centro de configurações da empresa para o link ajuda. Qualquer protocolo de URL pode ser usado.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p>Configura o UE-V Agent para não sincronizar nenhum aplicativo do Windows para todos os usuários do computador.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser – EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p>Configura o UE-V Agent para não sincronizar nenhum aplicativo do Windows para o usuário atual do computador.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableFirstUseNotification</code></p></td>
   <td align="left"><p>Configura o UE-V Agent para exibir a notificação na primeira vez que o agente é executado para todos os usuários do computador.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer –DisableFirstUseNotification</code></p></td>
   <td align="left"><p>Configura o UE-V Agent para não exibir a notificação na primeira vez que o agente é executado para todos os usuários do computador.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSettingsImportNotify</code></p></td>
   <td align="left"><p>Configura o UE-V Agent para notificar todos os usuários do computador quando a sincronização de configurações é atrasada.</p>
   <p>Use o <em> </em> parâmetro DisableSettingsImportNotify para desabilitar a notificação.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -EnableSettingsImportNotify</code></p></td>
   <td align="left"><p>Configura o UE-V Agent para notificar o usuário atual quando a sincronização de configurações é adiada.</p>
   <p>Use o <em> </em> parâmetro DisableSettingsImportNotify para desabilitar a notificação.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p>Configura o UE-V Agent para sincronizar todos os aplicativos do Windows que não são explicitamente desabilitados pela lista de aplicativos do Windows para todos os usuários do computador. Para obter mais informações, consulte &quot; Get-UevAppxPackage &quot; em <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> Gerenciando modelos de localização de configurações do UE-V 2. x usando o Windows PowerShell e o WMI </a> .</p>
   <p>Use o <em> </em> parâmetro DisableSyncUnlistedWindows8Apps para configurar o UE-V Agent para sincronizar apenas aplicativos do Windows que são explicitamente habilitados pela lista de aplicativos do Windows.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser - EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p>Configura o UE-V Agent para sincronizar todos os aplicativos do Windows que não são explicitamente desabilitados pela lista de aplicativos do Windows para o usuário atual no computador. Para obter mais informações, consulte &quot; Get-UevAppxPackage &quot; em <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> Gerenciando modelos de localização de configurações do UE-V 2. x usando o Windows PowerShell e o WMI </a> .</p>
   <p>Use o <em> </em> parâmetro DisableSyncUnlistedWindows8Apps para configurar o UE-V Agent para sincronizar apenas aplicativos do Windows que são explicitamente habilitados pela lista de aplicativos do Windows.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration –Computer –DisableSync</code></p></td>
   <td align="left"><p>Desabilita o UE-V para todos os usuários do computador.</p>
   <p>Use o <em> </em> parâmetro EnableSync para habilitar ou desabilitar novamente.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –CurrentComputerUser -DisableSync</code></p></td>
   <td align="left"><p>Desabilita o UE-V para o usuário atual no computador.</p>
   <p>Use o <em> </em> parâmetro EnableSync para habilitar ou desabilitar novamente.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableTrayIcon</code></p></td>
   <td align="left"><p>Habilita o ícone do UE-V na área de notificação para todos os usuários do computador.</p>
   <p>Use o <em> </em> parâmetro DisableTrayIcon para desabilitar o ícone.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p>Configura o UE-V Agent para relatar quando um tamanho de arquivo de pacote de configurações atinge o limite definido para todos os usuários do computador. Define o tamanho do pacote de limite em bytes.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p>Configura o UE-V Agent para relatar quando um tamanho de arquivo de pacote de configurações atinge o limite definido. Define o limite de aviso do tamanho do pacote para o usuário atual.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p>Especifica o tempo em segundos antes de o usuário ser notificado para todos os usuários do computador</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p>Especifica o tempo em segundos antes de a notificação para o usuário atual ser enviada.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p>Define um local de armazenamento de configurações por computador para todos os usuários do computador.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p>Define um local de armazenamento de configurações por usuário.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –Computer –SettingsTemplateCatalogPath &lt;path to catalog&gt;</code></p></td>
   <td align="left"><p>Define o caminho do catálogo de modelos de configurações para todos os usuários do computador.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p>Define o método de sincronização para todos os usuários do computador: SyncProvider ou None.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser  -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p>Define o método de sincronização para o usuário atual: SyncProvider ou None.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p>Define o tempo limite de sincronização em milissegundos para todos os usuários do computador</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set- UevConfiguration -CurrentComputerUser -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p>Definir o tempo limite de sincronização para o usuário atual.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Clear-UevConfiguration –Computer -&lt;setting name&gt;</code></p></td>
   <td align="left"><p>Limpa a configuração especificada para todos os usuários do computador.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Clear-UevConfiguration –CurrentComputerUser -&lt;setting name&gt;</code></p></td>
   <td align="left"><p>Limpa a configuração especificada somente para o usuário atual.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Export-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p>Exporta a configuração do computador UE-V para um arquivo de migração de configurações. A extensão de nome de arquivo deve ser. UEV.</p>
   <p>O <code>Export</code> cmdlet exporta todas as configurações do UE-V Agent que são configuráveis com o <em> </em> parâmetro Computer.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Import-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p>Importa a configuração do computador UE-V de um arquivo de migração de configurações. A extensão de nome de arquivo deve ser. UEV.</p></td>
   </tr>
   </tbody>
   </table>



**Para exportar as configurações do pacote do UE-V e reparar os modelos do UE-V usando o Windows PowerShell**

1.  Abra uma janela do Windows PowerShell como administrador.

2.  Use os seguintes comandos do Windows PowerShell para configurar o agente.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>comando do Windows PowerShell</strong></p></td>
    <td align="left"><p><strong>Descrição</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Export-UevPackage MicrosoftCalculator6. pkgx</p></td>
    <td align="left"><p>Extrai as configurações de um arquivo de pacote calculadora da Microsoft e converte-as em um formato legível por pessoas em XML.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Reparar-UevTemplateIndex</p></td>
    <td align="left"><p>Repara o índice dos modelos de local de configurações do UE-V.</p></td>
    </tr>
    </tbody>
    </table>



**Para configurar o UE-V Agent usando WMI**

1.  A virtualização da experiência do usuário fornece o seguinte conjunto de comandos WMI. Os administradores podem usar essa interface para configurar o UE-V Agent na linha de comando e automatizar tarefas típicas de configuração.

    Use uma conta com direitos de administrador para abrir uma janela do Windows PowerShell.

2.  Use os seguintes comandos WMI para configurar o agente.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>Windows PowerShell command</code></th>
    <th align="left">Descrição</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV Configuration</code></p>
    <p></p></td>
    <td align="left"><p>Exibe as configurações ativas do agente do UE-V. As configurações específicas do usuário têm precedência sobre as configurações do computador.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p></td>
    <td align="left"><p>Exibe a configuração do UE-V Agent definida para um usuário.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p></td>
    <td align="left"><p>Exibe a configuração do UE-V Agent definida para um computador.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject –Namespace root\Microsoft\Uev ConfigurationItem</code></p></td>
    <td align="left"><p>Exibe os detalhes de cada item de configuração.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Define um local de armazenamento de configurações por computador.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Define um local de armazenamento de configurações por usuário.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncTimeoutInMilliseconds = &lt;timeout_in_milliseconds&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Define o tempo limite de sincronização em milissegundos para todos os usuários do computador.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.MaxPackageSizeInBytes = &lt;size_in_bytes&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Configura o UE-V Agent para relatar quando um tamanho de arquivo de pacote de configurações atinge um limite definido. Defina o tamanho do arquivo do pacote de limite em bytes para todos os usuários do computador.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncMethod = &lt;sync_method&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Define o método de sincronização para todos os usuários do computador: SyncProvider ou None.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $true</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Para habilitar uma configuração específica por computador, desmarque a configuração e use <em> $NULL </em> como o valor de configuração. Use userconfiguration para configurações por usuário.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $false</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Para desabilitar uma configuração específica por computador, desmarque a configuração e use <em> $NULL </em> como o valor de configuração. Use a configuração do usuário para configurações por usuário.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = &lt;setting value&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Atualiza uma configuração específica por computador. Para limpar a configuração, use <em> $NULL </em> como o valor de configuração.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code></code>$config. &lt; definindo o &gt;  =  &lt; valor da configuração de nome&gt;</p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Atualiza uma configuração específica por usuário para todos os usuários do computador. Para limpar a configuração, use <em> $NULL </em> como o valor de configuração.</p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and Windows PowerShell, the defined configuration is stored in the registry in the following locations.

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

**Para exportar as configurações do pacote do UE-V e reparar os modelos do UE-V usando o WMI**

1.  O UE-V fornece o seguinte conjunto de comandos WMI. Os administradores podem usar essa interface para exportar um pacote ou reparar modelos do UE-V.

2.  Use os comandos WMI a seguir.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Comando WMI</th>
    <th align="left">Descrição</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name ExportPackage -ArgumentList &lt;package name&gt;</code></p></td>
    <td align="left"><p>Extrai as configurações de um arquivo de pacote e converte-as em um formato legível por pessoas em XML.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name RebuildIndex</code></p></td>
    <td align="left"><p>Repara o índice dos modelos de local de configurações do UE-V. Deve ser executado como administrador.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for UE-V**? Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **Got a UE-V issue**? Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).
~~~

## Tópicos relacionados


[Administração do UE-V 2. x com o Windows PowerShell e o WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[Administração do UE-V 2. x](administering-ue-v-2x-new-uevv2.md)









