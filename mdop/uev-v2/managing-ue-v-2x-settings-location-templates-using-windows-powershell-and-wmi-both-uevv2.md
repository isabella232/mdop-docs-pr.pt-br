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
# Gerenciando modelos de localização de configurações do UE-V 2. x usando o Windows PowerShell e o WMI


Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 usam modelos de localização de configurações XML para definir as configurações que a virtualização da experiência do usuário captura e aplica. O UE-V inclui um conjunto de modelos de localização de configurações padrão. Ele também inclui a ferramenta de gerador do UE-V que permite criar modelos de local de configurações personalizadas. Depois de criar e implantar modelos de local de configurações, você pode gerenciar esses modelos usando o Windows PowerShell e a instrumentação de gerenciamento do Windows (WMI). Para obter uma lista completa dos cmdlets do PowerShell do UE-V, consulte [referência do cmdlet do UE-v 2](https://go.microsoft.com/fwlink/p/?LinkId=393495) ( https://go.microsoft.com/fwlink/p/?LinkId=393495) .

## Gerenciar modelos de locais de configurações do UE-V 2 usando o Windows PowerShell


Os recursos do WMI e do Windows PowerShell do UE-V incluem a capacidade de habilitar, desabilitar, registrar, atualizar e cancelar o registro de modelos de localização de configurações. Ao usar esses recursos, você pode automatizar o processo de registro, atualização ou cancelamento de registro de modelos com o UE-V Agent. Você também pode registrar modelos manualmente usando os comandos WMI e Windows PowerShell. Ao usar esses recursos em conjunto com uma solução de distribuição de software eletrônico, política de grupo ou outro método de implantação automatizado, como um script, você pode automatizar ainda mais o processo.

Você deve ter permissões de administrador para atualizar, registrar ou cancelar o registro de um modelo de local de configurações. Não é necessário ter permissões de administrador para habilitar, desabilitar ou listar modelos.

***<em>Para gerenciar modelos de local de configurações usando o Windows PowerShellell</em>***

1.  Use uma conta com direitos de administrador para abrir um prompt de comando do Windows PowerShell.

2.  Use os seguintes cmdlets do Windows PowerShell para registrar e gerenciar os modelos de local das configurações do UE-V.

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
    <td align="left"><p><code>Get-UevTemplate</code></p></td>
    <td align="left"><p>Lista todos os modelos de local de configurações que estão registrados no computador.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate –Application &lt;string&gt;</code></p></td>
    <td align="left"><p>Lista todos os modelos de local de configurações que são registrados no computador em que o nome do aplicativo ou o nome do modelo contém &lt; cadeia de caracteres &gt; .</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate –TemplateID &lt;string&gt;</code></p></td>
    <td align="left"><p>Lista todos os modelos de local de configurações que são registrados no computador em que a ID do modelo contém a &lt; cadeia de caracteres &gt; .</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate [-ApplicationOrTemplateID] &lt;string&gt;</code></p></td>
    <td align="left"><p>Lista todos os modelos de local de configurações que são registrados no computador onde o nome do aplicativo ou do modelo ou a ID do modelo contém &lt; cadeia de caracteres &gt; .</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplateProgram [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Obtém o nome das informações do programa e da versão, que dependem da ID do modelo.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage</code></p></td>
    <td align="left"><p>Obtém a lista de aplicativos do Windows em vigor.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevAppXPackage -Computer</code></p></td>
    <td align="left"><p>Obtém a lista de aplicativos do Windows que estão configurados para o computador.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p>Obtém a lista de aplicativos do Windows que são configurados para o usuário atual.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Register-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Registra um ou mais modelos de local de configurações com UE-V usando caminhos relativos e/ou caracteres curinga em caminhos de arquivo. Após o registro de um modelo, o UE-V sincroniza as configurações definidas no modelo entre computadores que têm o modelo registrado.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Register-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Registra um ou mais modelos de local de configurações com UE-V usando caminhos literais, onde nenhum caractere pode ser interpretado como caracteres curinga. Após o registro de um modelo, o UE-V sincroniza as configurações definidas no modelo entre computadores que têm o modelo registrado.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Unregister-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Cancela o registro de um modelo de local de configurações com UE-V. Quando um modelo é cancelado, o UE-V não sincroniza mais as configurações definidas no modelo entre computadores.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Unregister-UevTemplate -All</code></p></td>
    <td align="left"><p>Cancela o registro de todos os modelos de locais de configurações com UE-V. Quando um modelo é cancelado, o UE-V não sincroniza mais as configurações definidas no modelo entre computadores.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Update-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Atualiza um ou mais modelos de local de configurações com uma versão mais recente do modelo. Use caminhos relativos e/ou caracteres curinga nos caminhos do arquivo. O novo modelo deve ser uma versão mais recente do que o modelo existente.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Update-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Atualiza um ou mais modelos de local de configurações com uma versão mais recente do modelo. Use caminhos completos para arquivos de modelo, onde nenhum caractere pode ser interpretado como caracteres curinga. O novo modelo deve ser uma versão mais recente do que o modelo existente.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Remove um ou mais aplicativos do Windows da lista de aplicativos do Windows do computador.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p>Remove o aplicativo do Windows da lista de aplicativos do usuário do Windows atual.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer -All</code></p></td>
    <td align="left"><p>Remove todos os aplicativos do Windows da lista de aplicativos do Windows do computador.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Remove um ou mais aplicativos do Windows da lista de aplicativos do usuário do Windows atual.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] -All</code></p></td>
    <td align="left"><p>Remove todos os aplicativos do Windows da lista de aplicativos do Windows do usuário atual.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Desabilita um modelo de local de configurações para o usuário atual do computador.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Disable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Desabilita um ou mais aplicativos do Windows na lista de aplicativos do Windows do computador.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Desabilita um ou mais aplicativos do Windows na lista de aplicativos do usuário do Windows atual.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Habilita um modelo de local de configurações para o usuário atual do computador.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Enable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Habilita um ou mais aplicativos do Windows na lista de aplicativos do Windows do computador.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Habilita um ou mais aplicativos do Windows na lista de aplicativos do usuário do Windows atual.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Test-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Determina se um ou mais modelos de localização de configurações estão em conformidade com o esquema XML. Pode usar caminhos relativos e caracteres curinga.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Test-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Determina se um ou mais modelos de localização de configurações estão em conformidade com o esquema XML. O caminho deve ser um caminho completo para o arquivo de modelo, mas não inclui caracteres curinga.</p></td>
    </tr>
    </tbody>
    </table>



Os recursos do UE-V Windows PowerShell permitem que você gerencie um grupo de modelos de configurações implantados em sua empresa. Use o procedimento a seguir para gerenciar um grupo de modelos usando o Windows PowerShell.

**Para gerenciar um grupo de modelos de local de configurações usando o Windows PowerShell**

1.  Modifique ou atualize os modelos de local de configurações desejadas.

2.  Se você quiser modificar ou atualizar os modelos de local de configurações, implante esses modelos de local de configurações para uma pasta acessível ao computador local.

3.  No computador local, abra uma janela do Windows PowerShell com direitos de administrador.

4.  Cancele o registro de todas as versões registradas anteriormente dos modelos digitando o comando a seguir.

    ``` syntax
    Unregister-UevTemplate -All
    ```

    Esse comando cancela o registro de todos os modelos ativos no computador.

5.  Registre os modelos atualizados digitando o seguinte comando.

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    Esse comando registra todos os modelos de local de configurações localizados na pasta de modelos especificada.

### <a href="" id="win8applist"></a>Lista de aplicativos do Windows

Ao listar um aplicativo do Windows na lista de aplicativos do Windows, você especifica se esse aplicativo está habilitado ou desabilitado para a sincronização das configurações. Os aplicativos são identificados na lista pelo nome da família de pacotes e se a sincronização das configurações deve ser habilitada ou desabilitada para esse aplicativo. Ao usar essas configurações juntamente com a configuração de comportamento de sincronização padrão não listada, você pode controlar se os aplicativos do Windows serão sincronizados.

Para exibir o nome da família de pacotes de aplicativos do Windows instalados, em um prompt de comando do Windows PowerShell, digite:

``` syntax
Get-AppxPackage | Sort-Object PackageFamilyName | Format-Table PackageFamilyName
```

Para exibir uma lista de aplicativos do Windows que podem sincronizar as configurações em um computador com o nome da família de pacotes, status habilitado e fonte habilitada, em um prompt de comando do Windows PowerShell, digite: `Get-UevAppxPackage`

**Definições das propriedades Get-UevAppxPackage**

<a href="" id="displayname"></a>**DisplayName**  
O nome que é exibido para o usuário no aplicativo da central de configurações da empresa. A `DisplayName` propriedade é derivada da `PackageFamilyName` propriedade.

<a href="" id="packagefamilyname"></a>**PackageFamilyName**  
O nome do pacote que é instalado para o usuário atual.

<a href="" id="enabled"></a>**Habilitado**  
Define se as configurações do aplicativo estão configuradas para sincronização.

<a href="" id="enabledsource"></a>**Habilitou**  
O local em que a configuração que habilita ou desabilita o aplicativo está definida. Os valores possíveis são: *NotSet*, *LocalMachine*, *LocalUser*, *PolicyMachine*e *PolicyUser*.

<a href="" id="notset"></a>**NotSet**  
A política não está configurada para sincronizar este aplicativo.

<a href="" id="localmachine"></a>**LocalMachine**  
O estado habilitado é definido na seção computador local do registro.

<a href="" id="localuser"></a>**Conta**  
O estado habilitado é definido na seção usuário atual do registro.

<a href="" id="policymachine"></a>**PolicyMachine**  
O estado habilitado é definido na seção política da seção computador local do registro.

Para obter a lista de aplicativos do Windows configurado pelo usuário, no prompt de comando do Windows PowerShell, digite: `Get-UevAppxPackage –CurrentComputerUser`

Para obter a lista configurada do computador de aplicativos do Windows, no prompt de comando do Windows PowerShell, digite: `Get-UevAppxPackage –Computer`

Para qualquer um dos parâmetros, CurrentComputerUser ou computador, o cmdlet retorna uma lista dos aplicativos do Windows que são configurados no nível do usuário ou do computador.

**Definições de propriedades**

<a href="" id="displayname"></a>**DisplayName**  
O nome que é exibido para o usuário no aplicativo da central de configurações da empresa. A `DisplayName` propriedade é derivada da `PackageFamilyName` propriedade.

<a href="" id="packagefamilyname"></a>**PackageFamilyName**  
O nome do pacote que é instalado para o usuário atual.

<a href="" id="enabled"></a>**Habilitado**  
Define se as configurações do aplicativo estão configuradas para serem sincronizadas para a opção especificada, ou seja, **usuário** ou **computador**.

<a href="" id="installed"></a>**Instalado**  
True se o aplicativo, ou seja, o PackageFamilyName estiver instalado para o usuário atual.

### Gerenciar modelos de locais de configurações do UE-V 2 usando WMI

A virtualização da experiência do usuário fornece o seguinte conjunto de comandos WMI. Os administradores podem usar essas interfaces para gerenciar modelos de local de configurações do Windows PowerShell e automatizar tarefas administrativas de modelos.

**Para gerenciar modelos de local de configurações usando WMI**

1.  Use uma conta com direitos de administrador para abrir uma janela do Windows PowerShell.

2.  Use os seguintes comandos WMI para registrar e gerenciar os modelos de local das configurações do UE-V.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>                         Windows PowerShell command</code></th>
    <th align="left">Descrição</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId,TemplateName, TemplateVersion,Enabled | Format-Table -Autosize</code></p></td>
    <td align="left"><p>Lista todos os modelos de local de configurações que são registrados para o computador.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod –Namespace root\Microsoft\UEV –Class SettingsLocationTemplate –Name GetProcessInfoByTemplateId &lt;template Id&gt;</code></p></td>
    <td align="left"><p>Obtém o nome das informações do programa e da versão, o que depende do nome do modelo.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV EffectiveWindows8App</code></p></td>
    <td align="left"><p>Obtém a lista de aplicativos do Windows em vigor.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-WmiObject-namespace root\Microsoft\UEV MachineConfiguredWindows8App</p></td>
    <td align="left"><p>Obtém a lista de aplicativos do Windows que estão configurados para o computador.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguredWindows8App</code></p></td>
    <td align="left"><p>Obtém a lista de aplicativos do Windows que são configurados para o usuário atual.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Register -ArgumentList &lt;template path &gt;</code></p></td>
    <td align="left"><p>Registra um modelo de local de configurações com UE-V.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name UnregisterByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Cancela o registro de um modelo de local de configurações com UE-V. Assim que um modelo é cancelado, o UE-V não sincroniza mais as configurações definidas no modelo entre computadores.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Update -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p>Atualiza um modelo de local de configurações com UE-V. O novo modelo deve ser uma versão mais recente do que a existente.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Remove um ou mais aplicativos do Windows da lista de aplicativos do Windows do computador.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Remove um ou mais aplicativos do Windows da lista de aplicativos do usuário do Windows atual.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name DisableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Desabilita um ou mais modelos de local de configurações com UE-V.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Desabilita um ou mais aplicativos do Windows na lista de aplicativos do Windows do computador.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Desabilita um ou mais aplicativos do Windows na lista de aplicativos do usuário do Windows atual.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name EnableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Habilita um modelo de local de configurações com UE-V.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Habilita os aplicativos do Windows na lista de aplicativos do Windows do computador.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Habilita os aplicativos do Windows na lista de aplicativos do usuário do Windows atual.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Validate -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p>Determina se um modelo de local de configurações especificado está em conformidade com o esquema XML.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
Where a list of Package Family Names is called by the WMI command, the list must be in quotes and separated by a pipe symbol, for example, `"<package family name | package family name>"`.
~~~



### Implantando o UE-V Agent usando o Windows PowerShell

**Como implantar o UE-V Agent usando o Windows PowerShell**

1.  Testar o pacote de instalação do UE-V Agent em um compartilhamento de rede acessível.

    **Observação**  
    Use AgentSetup.exe para implantar as versões de 32 bits e de 64 bits do UE-V Agent. Os pacotes do Windows Installer, AgentSetupx86.msi e AgentSetupx64.msi, estão disponíveis para cada arquitetura. Para desinstalar o UE-V Agent posteriormente, usando o arquivo de instalação, você deve usar o mesmo tipo de arquivo.



2.  Use um dos seguintes comandos do Windows PowerShell para instalar o UE-V Agent.

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**Tem uma sugestão para UE-V**? Adicione ou vote em sugestões [aqui](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **Tem um problema de UE-V**? Use o [Fórum do TechNet para UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).

## Tópicos relacionados


[Administração do UE-V 2. x com o Windows PowerShell e o WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[Administração do UE-V 2. x](administering-ue-v-2x-new-uevv2.md)









