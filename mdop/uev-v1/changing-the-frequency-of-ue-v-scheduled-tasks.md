---
title: Alterando a frequência das tarefas agendadas do UE-V
description: Alterando a frequência das tarefas agendadas do UE-V
author: dansimp
ms.assetid: 33c2674e-0df4-4717-9c3d-820a90b16e19
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ced608608ffae82a29fb5ca84cfca281082b8127
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799122"
---
# Alterando a frequência das tarefas agendadas do UE-V


O instalador do agente do Microsoft User Experience Virtualization (UE-V), AgentSetup.exe, cria duas tarefas agendadas durante a instalação do UE-V Agent. As duas tarefas são a tarefa de **atualização automática do modelo** e a tarefa **configuração de status do local de armazenamento** . Essas tarefas agendadas não são configuráveis com as ferramentas do UE-V. Os administradores que quiserem alterar a tarefa agendada desses itens poderão criar um script que use as opções de linha de comando do Schtasks.exe.

Para obter mais informações sobre Schtasks.exe, consulte [como usar Schtasks, exe para agendar tarefas no Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).

## Atualização automática de modelo


A tarefa de **atualização automática do modelo** verifica o catálogo de modelos de configurações para modelos novos, atualizados ou removidos. Essa tarefa só é executada se a SettingsTemplateCatalog estiver configurada. A tarefa de **atualização automática do modelo** executa o arquivo ApplySettingsCatalog.exe, localizado no diretório de instalação do UE-V Agent.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da tarefa</th>
<th align="left">Gatilho padrão</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Atualização automática do \Microsoft\UE-V\Template</p></td>
<td align="left"><p>3:30 AM todos os dias</p></td>
</tr>
</tbody>
</table>

 

**Exemplo:** O comando a seguir configura o agente para verificar a lista de catálogos de modelos de configurações a cada hora.

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

## Status do local de armazenamento de configurações


A tarefa **configuração de status do local de armazenamento** executa as seguintes ações:

1.  Verifica se as pastas do UE-V ainda estão fixadas ou registradas com o recurso arquivos offline.

2.  Verifica se o local de armazenamento de configurações está offline ou online.

3.  Força uma sincronização no intervalo especificado em vez do intervalo padrão para arquivos offline.

4.  Sincroniza qualquer pacote de configurações que está configurado para ser previamente buscado.

5.  Verifica se o caminho da pasta base do Active Directory foi alterado.

6.  Grava a configuração de armazenamento de configurações atuais no seguinte local

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Nome da tarefa</th>
    <th align="left">Gatilho padrão</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Status do local de armazenamento do \Microsoft\UE-V\Settings</p></td>
    <td align="left"><p>Ao fazer logon de qualquer usuário – após o disparo, repita a cada 30 minutos indefinidamente.</p></td>
    </tr>
    </tbody>
    </table>

     

**Exemplo:** O comando a seguir configura o agente para executar a ação acima de cada hora.

``` syntax
schtasks /change /tn "\Microsoft\UE-V\Settings Storage Location Status" /ri 60
```

## Tópicos relacionados


[Administração da UE-V 1.0](administering-ue-v-10.md)

[Operações para a UE-V 1.0](operations-for-ue-v-10.md)

 

 





