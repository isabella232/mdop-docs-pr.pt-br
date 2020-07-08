---
title: Alterar a frequência das tarefas agendadas do UE-V 2. x
description: Alterar a frequência das tarefas agendadas do UE-V 2. x
author: dansimp
ms.assetid: ee486570-c6cf-4fd9-ba48-0059ba877c10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/29/2016
ms.openlocfilehash: 1c1e3c091431dc56068dcd1fe0e849b0df1f6aa0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799470"
---
# Alterar a frequência das tarefas agendadas do UE-V 2. x


O instalador do agente do Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 ou 2,1 SP1, AgentSetup.exe, cria as seguintes tarefas agendadas durante a instalação do agente do UE-V:

-   **Monitorar configurações de aplicativo**

-   **Aplicativo de controlador de sincronização**

-   **Sincronizar configurações durante logoff**

-   **Atualização automática de modelo**

-   **Coletar dados do CEIP**

-   **Carregar dados CEIP**

**Observação**  Com exceção da coleta de dados CEIP, essas tarefas devem permanecer habilitadas, pois o UE-V não pode funcionar sem elas.

 

Essas tarefas agendadas não são configuráveis com as ferramentas do UE-V. Os administradores que desejam alterar a tarefa agendada desses itens podem criar um script que use as opções de linha de comando do Schtasks.exe.

Para obter mais informações sobre Schtasks.exe, consulte [como usar Schtasks, exe para agendar tarefas no Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).

Para obter mais informações sobre

## Tarefas agendadas de UE-V


As seguintes tarefas agendadas estão incluídas no UE-V 2 com comandos de configuração agendada de exemplo.

### Coletar dados do CEIP

Se, durante a instalação, o usuário ou o administrador tiver optado por participar do programa de aperfeiçoamento da experiência do usuário (CEIP), o UE-V coleta dados para ajudar a melhorar o produto em lançamentos futuros. Esta tarefa agendada só é executada no logon. A tarefa **coletar dados CEIP** executa a UevSqmSession.exe, localizada no diretório de instalação do UE-V Agent.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da tarefa</th>
<th align="left">Evento padrão</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Dados do CEIP do \Microsoft\UE-V\Collect</p></td>
<td align="left"><p>Sessão</p></td>
</tr>
</tbody>
</table>

 

### Monitorar configurações de aplicativo

A tarefa **monitorar configurações do aplicativo** é usada para sincronizar as configurações para aplicativos do Windows. Ele é executado no momento do logon, mas atrasado em 30 segundos para não afetar o logon de acordo. A tarefa monitorar status do aplicativo executa o arquivo UevAppMonitor.exe, localizado no diretório de instalação do UE-V Agent.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da tarefa</th>
<th align="left">Evento padrão</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Status do aplicativo \Microsoft\UE-V\Monitor</p></td>
<td align="left"><p>Sessão</p></td>
</tr>
</tbody>
</table>

 

### Aplicativo de controlador de sincronização

A tarefa de **aplicativo do controlador de sincronização** é usada para iniciar o controlador de sincronização para sincronizar as configurações do computador com o local de armazenamento de configurações. Por padrão, a tarefa é executada a cada 30 minutos. Nesse momento, as configurações locais são sincronizadas com o local de armazenamento de configurações e as configurações atualizadas no local de armazenamento de configurações são sincronizadas com o computador. O aplicativo de controlador de sincronização executa o Microsoft.Uev.SyncController.exe, localizado no diretório de instalação do UE-V Agent.
**Observação:** De acordo com a tarefa **monitorar configurações do aplicativo** , essa tarefa é executada no momento do logon, mas demora 30 segundos para não afetar o logon de forma prejudicial.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da tarefa</th>
<th align="left">Evento padrão</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aplicativo de controlador \Microsoft\UE-V\Sync</p></td>
<td align="left"><p>Faça logon e a cada 30 minutos depois</p></td>
</tr>
</tbody>
</table>

 

Por exemplo, o comando a seguir configura o agente para sincronizar as configurações a cada 15 minutos, em vez do padrão de 30 minutos.

``` syntax
Schtasks /change /tn “Microsoft\UE-V\Sync Controller Application” /ri 15
```

### Sincronizar configurações durante logoff

A tarefa **sincronizar configurações em logoff** é usada para iniciar um aplicativo no logon que controla a sincronização de aplicativos durante o logoff para UE-V. A tarefa sincronizar configurações em logoff executa o arquivo Microsoft.Uev.SyncController.exe, localizado no diretório de instalação do UE-V Agent.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da tarefa</th>
<th align="left">Evento padrão</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configurações do \Microsoft\UE-V\Synchronize ao fazer logoff</p></td>
<td align="left"><p>Sessão</p></td>
</tr>
</tbody>
</table>

 

### Atualização automática de modelo

A tarefa de **atualização automática do modelo** verifica o catálogo de modelos de configurações para modelos novos, atualizados ou removidos. Essa tarefa só é executada se a SettingsTemplateCatalog estiver configurada. A tarefa de **atualização automática do modelo** executa o arquivo ApplySettingsCatalog.exe, localizado no diretório de instalação do UE-V Agent.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da tarefa</th>
<th align="left">Evento padrão</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Atualização automática do \Microsoft\UE-V\Template</p></td>
<td align="left"><p>Inicialização do sistema e em 3:30 AM todos os dias, em um tempo aleatório em uma janela de 1 hora</p></td>
</tr>
</tbody>
</table>

 

**Exemplo:** O comando a seguir configura o UE-V Agent para verificar a lista de catálogos de modelos de configurações a cada hora.

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

### Carregar dados CEIP

A tarefa **carregar dados do CEIP** será executada durante a instalação se o usuário ou o administrador optar por participar do programa de aperfeiçoamento da experiência do usuário (CEIP). Essa tarefa carrega os dados nos servidores CEIP nos quais os dados são usados para ajudar a melhorar o produto para futuras versões do UE-V. Esta tarefa agendada é executada no momento do logon e a cada 4 horas depois. A tarefa **carregar dados do CEIP** executa o arquivo UevSqmUploader.exe, localizado no diretório de instalação do UE-V Agent.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da tarefa</th>
<th align="left">Evento padrão</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Dados do CEIP do \Microsoft\UE-V\Upload</p></td>
<td align="left"><p>Durante o logon e a cada 4 horas</p></td>
</tr>
</tbody>
</table>

 

## Detalhes da tarefa agendada do UE-V 2


O gráfico a seguir fornece informações adicionais sobre as tarefas agendadas para o UE-V 2:

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Nome da tarefa </strong> (nome do arquivo)</p></td>
<td align="left"><p><strong>Frequência padrão</strong></p></td>
<td align="left"><p><strong>Alternância de energia</strong></p></td>
<td align="left"><p><strong>Somente ocioso</strong></p></td>
<td align="left"><p><strong>Conexão de rede</strong></p></td>
<td align="left"><p><strong>Descrição</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Monitorar configurações </strong> do aplicativo (UevAppMonitor.exe)</p></td>
<td align="left"><p>Inicia 30 segundos após o logon e continua até que o logoff seja efetuado.</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>Sincroniza as configurações para aplicativos do Windows (AppX).</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Aplicativo de controlador </strong> de sincronização (Microsoft.Uev.SyncController.exe)</p></td>
<td align="left"><p>Durante o logon e a cada 30 min em diante.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Somente se a rede estiver conectada</p></td>
<td align="left"><p>Inicia o controlador de sincronização que sincroniza as configurações locais com o local de armazenamento de configurações.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Sincronizar configurações ao fazer logoff </strong> (Microsoft.Uev.SyncController.exe)</p></td>
<td align="left"><p>Executa no logon e, em seguida, aguarda o logoff para sincronizar as configurações.</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>Inicie um aplicativo no logon que controla a sincronização de aplicativos durante o logoff.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Atualização automática </strong> de modelo (ApplySettingsCatalog.exe)</p></td>
<td align="left"><p>É executado no logon inicial e em 3:30 AM todos os dias daí em diante.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>Verifica o catálogo de modelos de configurações para modelos novos, atualizados ou removidos. Esta tarefa só será executada se SettingsTemplateCatalog estiver configurada.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Coletar dados CEIP </strong> (UevSqmSession.exe)</p></td>
<td align="left"><p>No logon iniciado pelo serviço</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>N/A</p></td>
<td align="left"><p>Se o usuário ou o administrador optar pelo programa de aperfeiçoamento da experiência do usuário (CEIP), essa tarefa coletará dados que ajudarão a aprimorar futuras versões do UE-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Carregar dados CEIP </strong> (UevSqmUploader.exe)</p></td>
<td align="left"><p>É executado no momento da conexão e às 4:00 fica todos os dias depois disso.</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Somente se a rede estiver conectada</p></td>
<td align="left"><p>Se o usuário ou o administrador optar pelo programa de aperfeiçoamento da experiência do usuário (CEIP), essa tarefa carregará os dados nos servidores CEIP.</p></td>
</tr>
</tbody>
</table>

 

**Da**

-   Botão de **alternância de energia** – o Agendador de tarefas otimizará o consumo de energia quando não estiver conectado à alimentação de CA. A tarefa pode parar de funcionar se o computador mudar para energia da bateria.

-   **Somente ocioso** – a tarefa será interrompida se o computador deixar de ficar ocioso. Por padrão, a tarefa não será reiniciada quando o computador ficar ocioso novamente. Em vez disso, a tarefa será iniciada novamente no próximo gatilho de tarefa.

-   **Conexão de rede** – tarefas marcadas como "Sim" só são executadas se o computador tiver uma conexão de rede disponível. As tarefas marcadas como "N/d" são executadas independentemente da conectividade de rede.

### Como gerenciar tarefas agendadas

Para localizar tarefas agendadas, faça o seguinte:

1.  Abra "agendar tarefas" no computador do usuário.

2.  Navegue até: Agendador de tarefas – &gt; biblioteca do Agendador de tarefas- &gt; Microsoft- &gt; UE-V

3.  Selecione a tarefa agendada que você deseja gerenciar e configurar no painel detalhes.

### Informações adicionais

As seguintes informações adicionais se aplicam às tarefas agendadas do UE-V:

-   ll a sequência de tarefas programas estão localizados na pasta de instalação do UE-V Agent, `%programFiles%\Microsoft User Experience Virtualization\Agent\[architecture]\` por padrão.

-   A tarefa agendada do aplicativo de controlador de sincronização é o componente crucial quando o UE-V SyncMethod é definido como "SyncProvider" (a configuração padrão do UE-V 2). Esta tarefa agendada mantém o SettingsSToragePath sincronizado com as versões armazenadas em cache localmente dos arquivos de pacote de configurações. Se os usuários reclamarem de que as configurações não sincronizam com frequência suficiente, você poderá reduzir a configuração de tarefa agendada para apenas 1 minuto.Você também pode aumentar o padrão de 30 min para um valor mais alto, se necessário. Se os usuários reclamarem de que as configurações não sincronizam rápido o suficiente no logon, você poderá remover a configuração de atraso para a tarefa agendada. (Você pode encontrar a configuração atraso na caixa de diálogo **Editar gatilho** )

-   Você não precisa desabilitar a tarefa agendada de atualização automática de modelo se usar outro método para manter os modelos dos clientes em sincronia (ou seja, política de grupo ou linhas de base do Configuration Manager). Deixar o valor da propriedade SettingsTemplateCatalog em branco impede que o UE-V Verifique o catálogo de configurações para ver os modelos personalizados. Esta tarefa agendada executa ApplySettingsCatalog.exe e, essencialmente, retornará imediatamente.

-   A tarefa monitorar configurações do aplicativo agendada atualizará as configurações do aplicativo do Windows (AppX) em tempo real, com base nos gatilhos de configuração do programa de aplicativos do Windows, criados em cada aplicativo.






## Tópicos relacionados


[Administração do UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

[Implantar o UE-V 2. x para aplicativos personalizados](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#deploycatalogue)

 

 





