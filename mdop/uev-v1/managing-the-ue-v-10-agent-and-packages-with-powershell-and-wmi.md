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
# Gerenciamento de agente e pacotes da UE-V 1.0 com o PowerShell e o WMI


Você pode usar o WMI e o PowerShell para gerenciar a configuração e o comportamento de sincronização do agente do Microsoft User Experience Virtualization (UE-V).

**Como implantar o UE-V Agent com o PowerShell**

1.  Testar o arquivo do instalador do UE-V em um compartilhamento de rede acessível.

    **Observação**  
    Use AgentSetup.exe para implantar as versões de 32 bits e de 64 bits do UE-V Agent. Os arquivos do Windows Installer versões, AgentSetupx86.msi e AgentSetupx64.msi, estão disponíveis para cada arquitetura. Para desinstalar o UE-V Agent posteriormente usando o arquivo de instalação, você deve usar o mesmo tipo de arquivo.



2.  Use um dos seguintes comandos do PowerShell para instalar o agente.

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**Como configurar o UE-V Agent com o PowerShell**

1.  Use uma conta com direitos de administrador para abrir uma janela do PowerShell. Importe o módulo do PowerShell do UE-V usando o comando a seguir.

    ``` syntax
    Import-module UEV
    ```

2.  Use os comandos do PowerShell a seguir para configurar o agente.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Comando do PowerShell</strong></p></td>
    <td align="left"><p><strong>Descrição</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-UevConfiguration</p>
    <p></p></td>
    <td align="left"><p>Veja as configurações efetivas do agente do UE-V. As configurações específicas do usuário têm precedência sobre as configurações do computador.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Get-UevConfiguration-CurrentComputerUser</p>
    <p></p></td>
    <td align="left"><p>Exiba os valores das configurações do UE-V Agent somente para o usuário atual.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-UevConfiguration-computador</p></td>
    <td align="left"><p>Exiba os valores das configurações de configuração do UE-V Agent para todos os usuários do computador.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-caminho SettingsStoragePath do computador &lt; para _settings_storage_location&gt;</p></td>
    <td align="left"><p>Definir um local de armazenamento de configurações por computador.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser-SettingsStoragePath &lt; caminho para _settings_storage_location&gt;</p></td>
    <td align="left"><p>Definir um local de armazenamento de configurações por usuário.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-computador-SyncTimeoutInMilliseconds &lt; Timeout em milissegundos&gt;</p></td>
    <td align="left"><p>Definir o tempo limite de sincronização em milissegundos</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser-SyncTimeoutInMilliseconds &lt; Timeout em milissegundos&gt;</p></td>
    <td align="left"><p>Definir o tempo limite de sincronização do usuário atual.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-Computer-MaxPackageSizeInBytes &lt; size in bytes&gt;</p></td>
    <td align="left"><p>Configurar o UE-V Agent para denunciar quando um tamanho de arquivo de pacote de configurações atingir um limite definido. Defina o tamanho do pacote de limite em bytes.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser-MaxPackageSizeInBytes &lt; tamanho em bytes&gt;</p></td>
    <td align="left"><p>Defina o limite de aviso do tamanho do pacote para o usuário atual.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration – computador – SettingsTemplateCatalogPath &lt; caminho para catálogo&gt;</p></td>
    <td align="left"><p>Defina o caminho do catálogo de modelos de configurações.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration-método de sincronização de computador-SyncMethod &lt;&gt;</p></td>
    <td align="left"><p>Defina o método de sincronização: OfflineFiles ou None.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser-SyncMethod &lt; método de sincronização&gt;</p></td>
    <td align="left"><p>Defina o método de sincronização para o usuário atual: OfflineFiles ou None.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UEVConfiguration-computador – EnableSettingsImportNotify</p></td>
    <td align="left"><p>Permitir que a notificação ocorra quando a importação das configurações do usuário for adiada.</p>
    <p>Use – DisableSettingsImportNotify para desabilitar a notificação.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UEVConfiguration-CurrentComputerUser-EnableSettingsImportNotify</p></td>
    <td align="left"><p>Habilite a notificação para o usuário atual quando a importação das configurações do usuário for adiada.</p>
    <p>Use – DisableSettingsImportNotify para desabilitar a notificação.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UEVConfiguration-computador-SettingsImportNotifyDelayInSeconds</p></td>
    <td align="left"><p>Especificar o tempo em segundos antes de o usuário ser notificado</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UEVConfiguration-CurrentComputerUser-SettingsImportNotifyDelayInSeconds</p></td>
    <td align="left"><p>Especifique o tempo em segundos antes da notificação para o usuário atual.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration – computador – DisableSync</p></td>
    <td align="left"><p>Desative o UE-V para todos os usuários do computador.</p>
    <p>Use – EnableSync para habilitar ou desabilitar novamente.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration – CurrentComputerUser-DisableSync</p></td>
    <td align="left"><p>Desative o UE-V para o usuário atual no computador.</p>
    <p>Use – EnableSync para habilitar ou desabilitar novamente.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Clear-UevConfiguration – nome da &lt; configuração do computador&gt;</p></td>
    <td align="left"><p>Desmarque uma configuração específica para todos os usuários do computador.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Clear-UevConfiguration – CurrentComputerUser- &lt; nome de configuração&gt;</p></td>
    <td align="left"><p>Limpar uma configuração específica somente para o usuário atual.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Export-UevConfiguration &lt; arquivo de migração de configurações&gt;</p></td>
    <td align="left"><p>Exporte a configuração do computador UE-V para um arquivo de migração de configurações. A extensão do arquivo deve ser ". UEV".</p>
    <p>O cmdlet Export exporta todas as configurações do agente do UE-V que são configuráveis com o parâmetro-Computer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Importar-arquivo de migração de configurações do UevConfiguration &lt;&gt;</p></td>
    <td align="left"><p>Importar a configuração do computador UE-V de um arquivo de migração de configurações (arquivo. UEV).</p></td>
    </tr>
    </tbody>
    </table>



**Como exportar as configurações do pacote do UE-V e reparar modelos do UE-V com o PowerShell**

1.  Abra uma janela do PowerShell como administrador. Importe o módulo do PowerShell do UE-V com o seguinte comando.

    ``` syntax
    Import-module UEV
    ```

2.  Use os comandos do PowerShell a seguir para configurar o agente.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Comando do PowerShell</strong></p></td>
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



**Como configurar o UE-V Agent com WMI**

1.  A virtualização da experiência do usuário fornece o seguinte conjunto de comandos WMI. Os administradores podem usar essa interface para configurar o UE-V Agent a partir da linha de comando e automatizar tarefas típicas de configuração.

    Use uma conta com direitos de administrador para abrir uma janela do PowerShell.

2.  Use os seguintes comandos WMI para configurar o agente.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Comando do PowerShell</th>
    <th align="left">Descrição</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Get-WmiObject-configuração do root\Microsoft\UEV de namespace</p>
    <p></p></td>
    <td align="left"><p>Exibir as configurações ativas do agente do UE-V. As configurações específicas do usuário têm precedência sobre as configurações do computador.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-WmiObject-namespace root\Microsoft\UEV userconfiguration</p></td>
    <td align="left"><p>Veja a configuração do UE-V Agent definida para o usuário.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</p></td>
    <td align="left"><p>Veja a configuração do UE-V Agent definida para o computador.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Definir um local de armazenamento de configurações por computador.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>$config = Get-WmiObject-namespace root\Microsoft\UEV userconfiguration</p>
    <p>$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Definir um local de armazenamento de configurações por usuário.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. SyncTimeoutInMilliseconds = &lt; timeout_in_milliseconds&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Defina o tempo limite de sincronização em milissegundos.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. MaxPackageSizeInBytes = &lt; size_in_bytes&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Configurar o UE-V Agent para denunciar quando um tamanho de arquivo de pacote de configurações atingir um limite definido. Defina o tamanho do arquivo do pacote de limite em bytes.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. SyncMethod = &lt; sync_method&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Defina o método de sincronização: OfflineFiles ou None.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. &lt; definindo o &gt;  =  &lt; valor da configuração de nome&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Atualize uma configuração específica por computador. Para limpar a configuração, use $null como o valor de configuração.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. &lt; definindo o &gt;  =  &lt; valor da configuração de nome&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Atualize uma configuração específica por usuário. Para limpar a configuração, use $null como o valor de configuração.</p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and PowerShell, the defined configuration is stored in the registry in the following locations:

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

## Tópicos relacionados


[Administração da UE-V 1.0](administering-ue-v-10.md)

[Operações para a UE-V 1.0](operations-for-ue-v-10.md)









