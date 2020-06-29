---
title: Gerenciar o backup e a restauração administrativos no UE-V 2. x
description: Gerenciar o backup e a restauração administrativos no UE-V 2. x
author: dansimp
ms.assetid: 2eb5ae75-65e5-4afc-adb6-4e83cf4364ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11c168b54b71731c51417b2b7c4737c85f42035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800062"
---
# Gerenciar o backup e a restauração administrativos no UE-V 2. x


Como administrador do Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 ou 2,1 SP1, você pode restaurar as configurações do aplicativo e do Windows ao seu estado original. E novo no UE-V 2,1, você também pode restaurar configurações adicionais quando um usuário adotar um novo dispositivo.

## Restaurar as configurações no UE-V 2,1 ou no UE-V 2,1 SP1 quando um usuário adotar um novo dispositivo


Para restaurar as configurações quando um usuário adotar um novo dispositivo, você poderá colocar um modelo de local de configurações no perfil **backup** ou **roaming (padrão)** usando o cmdlet Set-UevTemplateProfile do PowerShell. Isso permite que as configurações do computador sejam sincronizadas com o novo computador, além das configurações do usuário. Os modelos atribuídos ao perfil de backup são incluídos em backup para esse dispositivo e configurados em cada dispositivo. Para fazer backup das configurações de um modelo, use o seguinte cmdlet no Windows PowerShell:

``` syntax
Set-UevTemplateProfile -ID <TemplateID> -Profile <backup>
```

-   &lt;TemplateID &gt; é a ID do modelo UE-V

-   &lt;&gt;o backup pode ser backup ou roaming

Ao substituir o dispositivo de um usuário, o UE-V restaura automaticamente as configurações se o domínio do usuário, o nome de usuário e o nome do dispositivo corresponderem. Todos os dados sincronizados e todos os dados de backup são restaurados automaticamente no dispositivo.

Você também pode usar o novo cmdlet do PowerShell, Restore-UevBackup, para restaurar as configurações de um dispositivo diferente. Para clonar os pacotes de configurações para o novo dispositivo, use o cmdlet a seguir no Windows PowerShell:

``` syntax
Restore-UevBackup –Machine <MachineName>
```

onde &lt; MachineName &gt; é o nome do computador do dispositivo.

Modelos como o modelo do Office 2013 que incluem muitos aplicativos podem ser incluídos no perfil móvel (padrão) ou de backup. Os aplicativos individuais em um pacote de modelos seguem o grupo. Os modelos in-box do Office 2013 incluem configurações de roaming e somente de backup. As configurações somente de backup não podem ser incluídas em um perfil móvel.

Como parte do recurso de backup/restauração, o UE-V adicionou a **última mercadoria conhecida (LKG)** às opções para reverter as configurações. Nesta versão, você pode reverter para as configurações originais ou configurações LKG. As configurações do LKG permitem que os usuários voltem a um ponto intermediário e estável antes do estado anterior ao UE-V das configurações.

### Como fazer backup/restaurar modelos com UE-V

Estes são os principais componentes de backup e restauração da UE-V:

-   Perfis de modelo

-   Local dos pacotes de configurações no modelo de local de armazenamento configurações

-   Gatilho de backup

-   Como as configurações são restauradas

**Perfis de modelo**

Um perfil de modelo UE-V é definido quando o modelo é registrado no dispositivo ou após o registro de postagem por meio do utilitário de configuração do PowerShell/WMI. Os tipos de perfil incluem:

-   Roaming (padrão)

-   Backup

-   Independemente

Todos os modelos são incluídos no perfil móvel quando registrados, a menos que especificado de outra forma. Esses modelos sincronizam as configurações para todos os dispositivos habilitados para UE-V com o modelo correspondente habilitado.

Os modelos podem ser adicionados ao perfil de backup com o PowerShell ou WMI usando o cmdlet Set-UevTemplateProfile. Os modelos no perfil de backup reservam essas configurações para o local de armazenamento de configurações em um diretório de nome de dispositivo especial. O backup das configurações especificadas é feito neste local.

Modelos designados incorretamente incluem configurações específicas do dispositivo que não devem ser sincronizadas, a menos que explicitamente restaurados. Essas configurações são armazenadas no mesmo local do pacote de configurações específicas do dispositivo no local de armazenamento de configurações como as configurações do Backedup. Esses modelos têm um identificador especial inserido no modelo que especifica que eles devem fazer parte desse perfil.

**Local dos pacotes de configurações no modelo de local de armazenamento configurações**

As configurações do perfil de roaming são armazenadas no local de armazenamento de configurações. Os modelos atribuídos ao backup ou ao perfil indesejado armazenam suas configurações no local de armazenamento de configurações em um diretório de nome de dispositivo especial. Cada dispositivo com modelos nesses perfis tem seu próprio nome de dispositivo. O UE-V não limpa esses diretórios.

**Gatilho de backup**

O backup é acionado pelos mesmos eventos que disparam uma sincronização de UE-V.

**Como as configurações são restauradas**

Restaurar o dispositivo de um usuário restaura as configurações do modelo atualmente registadas da pasta de backup de outro dispositivo e todas as configurações sincronizadas para o computador atual. As configurações são restauradas destas duas maneiras:

-   **Restauração automática**

    Se o caminho de armazenamento, o domínio e o nome do computador do usuário do UE-V são compatíveis com o usuário atual, todas as configurações do usuário serão sincronizadas, com apenas as configurações mais recentes aplicadas. Se um usuário fizer logon em um novo dispositivo pela primeira vez e esses critérios forem atendidos, os dados de configurações serão aplicados a esse dispositivo.

    **Observação**  
    As configurações de acessibilidade e de área de trabalho do Windows exigem que o usuário faça logon novamente no Windows para ser aplicado.



-   **Restauração manual**

    Se quiser ajudar os usuários restaurando um dispositivo durante uma atualização, você pode optar por usar o cmdlet Restore-UevBackup. Esse comando faz com que as configurações do usuário sejam baixadas do local de armazenamento de configurações.

## Restaurar o aplicativo e as configurações do Windows para o estado original


Os comandos do WMI e do Windows PowerShell permitem restaurar as configurações do aplicativo e do Windows para os valores de configurações que estavam no computador na primeira vez que o aplicativo foi iniciado após a instalação do UE-V Agent. Essa ação de restauração é realizada em uma base de configurações por aplicativo ou Windows. As configurações serão restauradas na próxima vez que o aplicativo for executado, ou as configurações serão restauradas quando o usuário fizer logon no sistema operacional.

**Para restaurar as configurações do aplicativo e as configurações do Windows com o Windows PowerShell para UE-V 2. x**

1.  Abra a janela do Windows PowerShell.

2.  Digite o seguinte cmdlet do Windows PowerShell para restaurar as configurações do aplicativo e as configurações do Windows.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Cmdlet do Windows PowerShell</strong></th>
    <th align="left"><strong>Descrição</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Restore-UevUserSetting -&lt;TemplateID&gt;</code></p></td>
    <td align="left"><p>Restaura as configurações de usuário para um aplicativo ou restaura um grupo de configurações do Windows.</p></td>
    </tr>
    </tbody>
    </table>



**Para restaurar as configurações do aplicativo e as configurações do Windows com WMI**

1.  Abra uma janela do Windows PowerShell.

2.  Digite o seguinte comando WMI para restaurar as configurações do aplicativo e as configurações do Windows.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Comando WMI</strong></th>
    <th align="left"><strong>Descrição</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name RestoreByTemplateId -ArgumentList &lt;template_ID&gt;</code></p></td>
    <td align="left"><p>Restaura as configurações de usuário para um aplicativo ou restaura um grupo de configurações do Windows.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
UE-V does not provide a settings rollback for Windows apps.
~~~








## Tópicos relacionados


[Administração do UE-V 2. x com o Windows PowerShell e o WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[Administração do UE-V 2. x](administering-ue-v-2x-new-uevv2.md)









