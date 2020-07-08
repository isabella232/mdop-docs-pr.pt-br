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
# Gerenciamento dos modelos de localização de configurações da UE-V 1.0 usando o PowerShell e o WMI


O Microsoft User Experience Virtualization (UE-V Experience Virtualization) usa modelos de local de configurações (arquivos XML) que definem as configurações capturadas e aplicadas pela virtualização da experiência do usuário. O UE-V inclui um conjunto de modelos de localização de configurações padrão. Ele também inclui a ferramenta de gerador do UE-V que permite criar modelos de local de configurações personalizadas. Depois de criar e implantar modelos de local de configurações, você pode gerenciar esses modelos usando o PowerShell ou o WMI.

## Gerenciar modelos de local de configurações com WMI e PowerShell


Os recursos do WMI e do PowerShell do UE-V incluem a capacidade de habilitar, desabilitar, registrar, atualizar e cancelar o registro de modelos de local de configurações. Ao usar esses recursos, você pode automatizar o processo de registro, atualização ou cancelamento de registro de modelos com o UE-V Agent. Você também pode registrar modelos manualmente usando os comandos WMI e PowerShell. Ao usar esses recursos em conjunto com uma solução de distribuição de software eletrônico, política de grupo ou outro método de implantação automatizado, como um script, você pode automatizar ainda mais o processo.

Você deve ter permissões de administrador para atualizar, registrar ou cancelar o registro de um modelo de local de configurações. Não é necessário ter permissões de administrador para habilitar ou desabilitar modelos.

**Para gerenciar modelos de local de configurações com o PowerShell**

1.  Use uma conta com direitos de administrador para abrir uma janela do Windows PowerShell. Para importar o módulo **Microsoft UE-V PowerShell** , digite o seguinte comando no prompt de comando do PowerShell.

    ``` syntax
    Import-module UEV
    ```

2.  Use os cmdlets do PowerShell a seguir para registrar e gerenciar os modelos de local das configurações do UE-V.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Comando do PowerShell</strong></th>
    <th align="left"><strong>Descrição</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Get-UevTemplate</p></td>
    <td align="left"><p>Lista todos os modelos de locais de configurações registrados no computador.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Register-UevTemplate</p></td>
    <td align="left"><p>Registra um modelo de local de configurações com UE-V. Depois que um modelo é registrado, o UE-V sincronizará as configurações definidas no modelo entre computadores que têm o modelo registrado.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Cancelar registro-UevTemplate</p></td>
    <td align="left"><p>Cancela o registro de um modelo de local de configurações com UE-V. Assim que um modelo é cancelado, o UE-V não sincronizará mais as configurações definidas no modelo entre computadores.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Update-UevTemplate</p></td>
    <td align="left"><p>Atualiza um modelo de local de configurações com uma versão mais recente do modelo. O novo modelo deve ter uma versão posterior a uma existente.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Disable-UevTemplate</p></td>
    <td align="left"><p>Desabilita um modelo de local de configurações para o usuário atual do computador.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Enable-UevTemplate</p></td>
    <td align="left"><p>Habilita um modelo de local de configurações para o usuário atual do computador.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Test-UevTemplate</p></td>
    <td align="left"><p>Determina se um modelo de local de configurações especificado está em conformidade com o esquema XML.</p></td>
    </tr>
    </tbody>
    </table>

     

Os recursos do PowerShell do UE-V permitem que você gerencie um grupo de modelos de configurações implantados em sua empresa. Para gerenciar um grupo de modelos usando o PowerShell, faça o seguinte.

**Para gerenciar um grupo de modelos de local de configurações com o PowerShell**

1.  Modifique ou atualize os modelos de local de configurações desejadas.

2.  Implante os modelos de localização de configurações desejadas para uma pasta acessível ao computador local.

3.  No computador local, abra uma janela do Windows PowerShell com direitos de administrador.

4.  Importe o módulo Microsoft UE-V PowerShell, digitando o seguinte comando.

    ``` syntax
    Import-module UEV
    ```

5.  Cancele o registro de todas as versões registradas anteriormente dos modelos digitando o comando a seguir.

    ``` syntax
    Get-UevTemplate | Unregister-UevTemplate
    ```

    Isso cancelará o registro de todos os modelos ativos no computador.

6.  Registre os modelos atualizados digitando o seguinte comando.

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    Isso registrará todos os modelos de locais de configurações localizados na pasta de modelos especificada.

A virtualização da experiência do usuário fornece o seguinte conjunto de comandos WMI. Os administradores podem usar essas interfaces para gerenciar modelos de local de configurações do Windows PowerShell e automatizar tarefas administrativas de modelos.

**Para gerenciar modelos de local de configurações com WMI**

1.  Use uma conta com direitos de administrador para abrir uma janela do Windows PowerShell.

2.  Use os seguintes comandos WMI para registrar e gerenciar os modelos de local das configurações do UE-V.

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
    <td align="left"><p>Get-WmiObject-namespace root\Microsoft\UEV SettingsLocationTemplate | Select-TemplateID do objeto, TemplateName, TemplateVersion, Enabled | Format-Table-AutoSize</p></td>
    <td align="left"><p>Lista todos os modelos de locais de configurações registrados para o computador.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Registerlist caminho do modelo de argumento &lt;&gt;</p></td>
    <td align="left"><p>Registra um modelo de local de configurações com UE-V.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name UnregisterByTemplateId-ArgumentList &lt; ID do modelo&gt;</p></td>
    <td align="left"><p>Cancela o registro de um modelo de local de configurações com UE-V. Assim que um modelo é cancelado, o UE-V não sincronizará mais as configurações definidas no modelo entre computadores.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name EnableByTemplateId-ArgumentList &lt; ID do modelo&gt;</p></td>
    <td align="left"><p>Habilita um modelo de local de configurações com UE-V</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name DisableByTemplateId-ArgumentList &lt; ID do modelo&gt;</p></td>
    <td align="left"><p>Desabilita um modelo de local de configurações com UE-V</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Update-caminho do &lt; modelo de argumento&gt;</p></td>
    <td align="left"><p>Atualiza um modelo de local de configurações com UE-V. O novo modelo deve ter uma versão superior à existente.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-Name Validate-ArgumentList &lt; caminho do modelo&gt;</p></td>
    <td align="left"><p>Determina se um modelo de local de configurações especificado está em conformidade com o esquema XML.</p></td>
    </tr>
    </tbody>
    </table>

     

**Como implantar o UE-V Agent com o PowerShell**

1.  Testar o arquivo do instalador do UE-V em um compartilhamento de rede acessível.

    **Observação**  Use AgentSetup.exe para implantar as versões de 32 bits e de 64 bits do UE-V Agent. Os arquivos do Windows Installer versões, AgentSetupx86.msi e AgentSetupx64.msi, estão disponíveis para cada arquitetura. Para desinstalar o UE-V Agent posteriormente usando o arquivo de instalação, você deve usar o mesmo tipo de arquivo.

     

2.  Use um dos seguintes comandos do PowerShell para instalar o agente.

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

## Tópicos relacionados


[Gerenciamento de agente e pacotes da UE-V 1.0 com o PowerShell e o WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

[Administração da UE-V 1.0](administering-ue-v-10.md)

[Operações para a UE-V 1.0](operations-for-ue-v-10.md)

 

 





