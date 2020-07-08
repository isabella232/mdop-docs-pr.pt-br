---
title: Gerenciamento de configurações do espaço de trabalho da MED-V
description: Gerenciamento de configurações do espaço de trabalho da MED-V
author: dansimp
ms.assetid: 517d04de-c31f-4b50-b2b3-5f8c312ed37b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97add695f605b71547b564789cce07a1d58763f2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799816"
---
# Gerenciamento de configurações do espaço de trabalho da MED-V


A virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0 armazena suas configurações de configuração no registro. As informações incluídas aqui sobre o registro podem ajudá-lo a gerenciar melhor seus serviços do MED-V.

O MED-V usa o seguinte caminho de pesquisa ao procurar os valores de configurações resultantes:

O MED-V procura primeiro na política do computador.

Se o valor não for encontrado, o MED-V pesquisará na política de usuário.

Se o valor não for encontrado, o MED-V procura na seção HKEY \ _LOCAL \ _MACHINE \\System.

Se o valor não for encontrado, o MED-V pesquisará no hive do registro do usuário HKEY \ _CURRENT.

Se o valor ainda não for encontrado, o MED-V usará o padrão.

Uma prática recomendada geral é definir o valor na seção HKEY \ _LOCAL \ _MACHINE \\System ou na política do computador. Mas se você quiser que o usuário final seja capaz de definir uma determinada configuração, você deve deixá-la.

**Observação**  
Antes de implantar seus espaços de trabalho do MED-V, você pode usar um editor de script para alterar o script do Windows PowerShell (arquivo. ps1) criado pelo pacote do espaço de trabalho do MED-V. Para obter mais informações, consulte [definindo as configurações avançadas usando o Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).

Depois de implantar seus espaços de trabalho do MED-V, você pode alterar determinadas configurações de configuração do MED-V editando as entradas do registro.



Esta seção lista todas as chaves de registro do MED-V configuráveis e explica seus usos.

## Chave de diagnóstico


A tabela a seguir fornece informações sobre os valores do registro associados à chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Diagnostics.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome </th>
<th align="left">Tipo </th>
<th align="left">Dados/padrão </th>
<th align="left">Descrição </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>EventLogLevel </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Padrão = 3</p></td>
<td align="left"><p>O tipo de informação que está registrada no log de eventos. Os níveis incluem o seguinte: 0 (nenhum), 1 (erro), 2 (aviso), 3 (informações), 4 (Depurar).</p></td>
</tr>
</tbody>
</table>



## Chave FTS


A tabela a seguir fornece informações sobre os valores do registro associados à chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Fts.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome</th>
<th align="left">Tipo</th>
<th align="left">Dados/padrão</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AddUserToAdminGroupEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 0</p></td>
<td align="left"><p>Configura se a primeira vez que o programa de instalação adiciona automaticamente o usuário final ao grupo administrador&#39;s. 0 = falso; 1 = verdadeiro.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: o programa de instalação da primeira vez não adiciona automaticamente o usuário final ao grupo administrador&#39;s.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadeiro: o programa de instalação da primeira vez adiciona automaticamente o usuário final ao grupo administrador&#39;s.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ComputerNameMask </p></td>
<td align="left"><p>St</p></td>
<td align="left"><p>MEDV* </p></td>
<td align="left"><p>A máscara de nome do computador que é usada para criar o nome do computador&#39;s da máquina virtual convidada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>A máscara pode conter uma marca% username% para inserir o nome de usuário como parte do nome do computador. Da mesma forma, a marca% hostname% insere o nome do computador host.</p>
<p>Cada &quot; # &quot; caractere na máscara é substituído por um dígito aleatório. Um caractere de asterisco (*) no final da máscara é substituído por caracteres alfanuméricos aleatórios.</p>
<p>Um número específico de caracteres de% hostname% e% username% pode ser capturado usando colchetes. Por exemplo, &quot; % username% [3] &quot; usaria os três primeiros caracteres do nome de usuário.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeleteVMStateTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 90</p></td>
<td align="left"><p>O valor de tempo limite, em segundos, quando a configuração tenta excluir a máquina virtual pela primeira vez. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DetachVfdTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 120</p></td>
<td align="left"><p>O valor de tempo limite, em segundos, quando a configuração da primeira vez tenta desanexar o disquete virtual da máquina virtual. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DialogUrl </p></td>
<td align="left"><p>St</p></td>
<td align="left"><p></p></td>
<td align="left"><p>URL personalizável que se vincula à página da Web interna e é exibida pela primeira vez que você configurar as mensagens de diálogo. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>ExplorerTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 900</p></td>
<td align="left"><p>O valor de tempo limite, em segundos, que a configuração de primeira vez aguarda para o Windows Explorer. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FailureDialogMsg </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>Mensagem encontrada no arquivo de recurso </p></td>
<td align="left"><p>Mensagem personalizável que é exibida para o usuário final quando a configuração não pode ser concluída pela primeira vez.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GiveUserGroupRightsMaxRetryCount </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Padrão = 3</p></td>
<td align="left"><p>O número máximo de vezes que o MED-V tenta conceder a um usuário final direitos de grupo. Exceder o valor de repetição especificado sem ser capaz de conceder com êxito a um grupo de usuários finais os direitos provavelmente causam uma falha de preparação da máquina virtual que, em seguida, está sujeito ao valor MaxRetryCount. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>GiveUserGroupRightsTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 300</p></td>
<td align="left"><p>O valor de tempo limite, em segundos, ao conceder direitos a um grupo de usuários. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LogFilePaths </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Uma lista dos caminhos do arquivo de log que o MED-V coleta durante a primeira configuração. </p></td>
</tr>
<tr class="even">
<td align="left"><p>MaxPostponeTime </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 120</p></td>
<td align="left"><p>O número máximo de horas em que a configuração da primeira vez pode ser adiada pelo usuário final. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxRetryCount </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 3</p></td>
<td align="left"><p>O número máximo de vezes que o MED-V tenta preparar uma máquina virtual se cada tentativa terminar em uma falha diferente de um erro de software. Quando a preparação da máquina virtual falha e o número da primeira tentativa de configuração é excedido, o MED-V informa o usuário final sobre a falha e não dá a opção de tentar novamente. A contagem é reativada sempre que o MED-V é iniciado. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Modo </p></td>
<td align="left"><p>St</p></td>
<td align="left"><p>Padrão = autônomo</p></td>
<td align="left"><p>Configura a primeira vez que a configuração interage com o usuário. Os valores possíveis são os seguintes:</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Compromissos.</strong> O usuário final deve inserir informações durante a primeira configuração.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Se você criou o arquivo Sysprep. inf para que a mini-instalação exija que a entrada do usuário seja concluída, você deve <strong> selecionar </strong> modo assistido ou problemas podem ocorrer durante a configuração inicial.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Autônomo </strong> . A máquina virtual não é mostrada para o usuário final durante a primeira instalação, mas o usuário final é solicitado antes do início da configuração da primeira vez.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Silencioso </strong> . A máquina virtual não é mostrada para o usuário final durante a primeira configuração.</p></td>
</tr>
<tr class="even">
<td align="left"><p>NonInteractiveRetryTimeoutInc </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 15</p></td>
<td align="left"><p>O valor de tempo limite, em minutos, que a configuração inicial deve ser completada na primeira vez que a instalação é feita ao tentar novamente a instalação. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>NonInteractiveTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 45</p></td>
<td align="left"><p>O valor de tempo limite, em minutos, que a configuração inicial deve ser completada na primeira vez em que você configurar o modo interativo. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PostponeUtcDateTimeLimit </p></td>
<td align="left"><p>St</p></td>
<td align="left"><p></p></td>
<td align="left"><p>A data e a hora, no formato DateTime UTC, que pode ser adiada pela primeira vez. Insira no formato &quot; aaaa-mm-dd hh: mm &quot; com horas especificadas usando o padrão de relógio de 24 horas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RetryDialogMsg </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>Mensagem encontrada no arquivo de recurso </p></td>
<td align="left"><p>Mensagem personalizável que é exibida para o usuário final quando a configuração da primeira vez precisa ser feita novamente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SetComputerNameEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 0</p></td>
<td align="left"><p>Configura se a entrada ComputerName na seção [UserData] do arquivo Sysprep. inf no convidado deve ser atualizada de acordo com a ComputerNameMask especificada.   0 = falso; 1 = verdadeiro.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: a entrada ComputerName no arquivo Sysprep. inf não é atualizada de acordo com o ComputerNameMask.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadeiro: a entrada ComputerName no arquivo Sysprep. inf é atualizada de acordo com o ComputerNameMask.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SetJoinDomainEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 0</p></td>
<td align="left"><p>Configura se a configuração JoinDomain na seção [identificação] do arquivo Sysprep. inf no convidado deve ser atualizada para corresponder às configurações no host.  0 = falso; 1 = verdadeiro.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: a configuração JoinDomain no arquivo Sysprep. inf não é atualizada para corresponder às configurações no host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadeiro: a configuração JoinDomain no arquivo Sysprep. inf é atualizada para corresponder às configurações no host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SetMachineObjectOUEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 0</p></td>
<td align="left"><p>Configura se a configuração MachineObjectOU na seção [identificação] do arquivo Sysprep. inf no convidado é atualizada para corresponder ao host.  0 = falso; 1 = verdadeiro.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: a configuração MachineObjectOU no arquivo Sysprep. inf não é atualizada para corresponder às configurações no host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadeiro: a configuração MachineObjectOU no arquivo Sysprep. inf é atualizada para corresponder às configurações no host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SetRegionalSettingsEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 0</p></td>
<td align="left"><p>Configura se as configurações na seção [RegionalSettings] do arquivo Sysprep. inf no convidado são atualizadas para corresponderem ao host.  0 = falso; 1 = verdadeiro.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Por padrão, a configuração de fuso horário no convidado sempre é sincronizada com a configuração de fuso horário no host.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: as configurações na seção [RegionalSettings] do arquivo Sysprep. inf no convidado não são atualizadas para corresponderem ao host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadeiro: as configurações na seção [RegionalSettings] do arquivo Sysprep. inf no convidado são atualizadas para corresponderem ao host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SetUserDataEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 0</p></td>
<td align="left"><p>Configura se as configurações FullName e OrgName na seção [UserData] do arquivo Sysprep. inf no convidado são atualizadas para corresponder às configurações no host.  0 = falso; 1 = verdadeiro.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: as configurações FullName e OrgName no arquivo Sysprep. inf não são atualizadas para corresponder às configurações no host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadeiro: as configurações FullName e OrgName no arquivo Sysprep. inf são atualizadas para corresponder às configurações no host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>StartDialogMsg </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>Mensagem encontrada no arquivo de recurso </p></td>
<td align="left"><p>Mensagem personalizável que é exibida para o usuário final quando a configuração está pronta para começar. </p></td>
</tr>
<tr class="even">
<td align="left"><p>TaskCancelTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 30</p></td>
<td align="left"><p>O valor de tempo limite, em segundos, que a configuração inicial aguarda pela primeira vez para obter uma resposta da máquina virtual para uma operação de cancelamento. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TaskVMTurnOffTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 60</p></td>
<td align="left"><p>O valor de tempo limite, em segundos, que a configuração da primeira vez aguarda para que a máquina virtual seja encerrada. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>UpgradeTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 600</p></td>
<td align="left"><p>O tempo, em segundos, antes que uma tentativa de atualização do software do agente de convidado do MED-V expire. Intervalo = 0 a 2147483647.</p></td>
</tr>
</tbody>
</table>



## Chave userexperience


A tabela a seguir fornece informações sobre os valores do registro associados à chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\UserExperience e a tecla HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\UserExperience.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome</th>
<th align="left">Tipo</th>
<th align="left">Dados/padrão</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AppPublishingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 1</p></td>
<td align="left"><p>Configura se a publicação do aplicativo do convidado para o host está habilitada.  0 = falso; 1 = verdadeiro.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: desabilita a publicação de aplicativos do convidado para o host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadeiro: habilita a publicação de aplicativos do convidado para o host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AudioSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 1</p></td>
<td align="left"><p>Configura se o compartilhamento do dispositivo de e/s de áudio entre o convidado e o host está habilitado.  0 = falso; 1 = verdadeiro.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: desabilita o compartilhamento do dispositivo de e/s de áudio entre o convidado e o host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadeiro: habilita o compartilhamento do dispositivo de e/s de áudio entre o convidado e o host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ClipboardSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 1</p></td>
<td align="left"><p>Configura se o compartilhamento da área de transferência entre o convidado e o host está habilitado.  0 = falso; 1 = verdadeiro.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: desabilita o compartilhamento da área de transferência entre o convidado e o host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadeiro: permite o compartilhamento da área de transferência entre o convidado e o host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DialogTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 300</p></td>
<td align="left"><p>O tempo, em segundos, antes da primeira vez em que a configuração iniciar a caixa de diálogo Iniciar. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HideVmTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 30</p></td>
<td align="left"><p>O valor de tempo limite, em minutos, que a janela da máquina virtual de tela inteira está oculta do usuário final durante uma tentativa de logon longa.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LogonStartEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 1</p></td>
<td align="left"><p>Configura se o convidado deve ser iniciado quando o usuário final se conecta à área de trabalho ou quando o primeiro aplicativo convidado é iniciado.  0 = falso; 1 = verdadeiro.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: o convidado é iniciado quando o primeiro aplicativo convidado é iniciado.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadeiro: o convidado é iniciado quando o usuário final faz logon na área de trabalho.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PrinterSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 1</p></td>
<td align="left"><p>Configura se o compartilhamento de impressoras entre o convidado e o host está habilitado.  0 = falso; 1 = verdadeiro.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: desabilita o compartilhamento de impressoras entre o convidado e o host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadeiro: habilita o compartilhamento de impressoras entre o convidado e o host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>RebootAbsoluteDelayTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 1440</p></td>
<td align="left"><p>O valor de tempo limite, em minutos, que a configuração inicial aguarda durante uma reinicialização. Intervalo = 0 a 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RedirectUrls </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>Lista de URLs especificada</p></td>
<td align="left"><p>Especifica uma lista de URLs a serem redirecionadas do host para o convidado. </p></td>
</tr>
<tr class="even">
<td align="left"><p>SmartCardLogonEnabled</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 0</p></td>
<td align="left"><p>Configura se os cartões inteligentes podem ser usados para autenticar usuários no MED-V. 0 = falso; 1 = verdadeiro.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: não permite que os cartões inteligentes autentiquem usuários finais para o MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadeiro: permite que os cartões inteligentes autentiquem os usuários finais para o MED-V.</p>
<div class="alert">
<strong>Importante</strong><br/><p>Se SmartCardLogonEnabled e CredentialCacheEnabled estiverem habilitados, SmartCardLogonEnabled substituirá CredentialCacheEnabled.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>SmartCardSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 1</p></td>
<td align="left"><p>Configura se o compartilhamento de cartões inteligentes entre o convidado e o host está habilitado.  0 = falso; 1 = verdadeiro.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: desabilita o compartilhamento de cartões inteligentes entre o convidado e o host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadeiro: habilita o compartilhamento de cartões inteligentes entre o convidado e o host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>USBDeviceSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 1</p></td>
<td align="left"><p>Configura se o compartilhamento de dispositivos USB entre o convidado e o host está habilitado.  0 = falso; 1 = verdadeiro.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: desabilita o compartilhamento de dispositivos USB entre o convidado e o host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadeiro: habilita o compartilhamento de dispositivos USB entre o convidado e o host.</p></td>
</tr>
</tbody>
</table>



## Chave de VM


A tabela a seguir fornece informações sobre os valores do registro associados à chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\VM e a tecla HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\VM.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome</th>
<th align="left">Tipo</th>
<th align="left">Dados/padrão</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Fecharaction </p></td>
<td align="left"><p>St</p></td>
<td align="left"><p>Padrão = HIBERNAr</p></td>
<td align="left"><p>A ação que a máquina virtual executa após o último aplicativo em execução é fechada. Essa configuração será ignorada se o valor LogonStartEnabled estiver habilitado. As opções possíveis são as seguintes:</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>HIBERNAr </strong> . Esta opção libera todos os recursos físicos que a máquina virtual está usando, como memória e CPU, e salva o estado de todos os aplicativos e operações em execução.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>DESLIGAR </strong> . Esta opção desliga o sistema operacional convidado com segurança e, em seguida, libera todos os recursos físicos que a máquina virtual está usando, como memória e CPU.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>desativar </strong> . Essa opção pode causar perda de dados porque é o mesmo que desativar o botão de energia ou retirar o cabo de alimentação em um computador físico. Use essa opção somente se não for possível usar uma das outras duas opções.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GuestMemFromHostMem </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>378, 512, 1024, 1536, 2048 </p></td>
<td align="left"><p>Uma lista de valores de memória (MB) para o convidado. Esse valor é usado para determinar a quantidade de RAM disponível para o convidado. Combinado com HostMemToGuestMem, uma tabela de pesquisa é criada para determinar a quantidade de memória RAM a ser alocada na máquina virtual convidada. Os valores possíveis podem ser de 128 a 3712.</p></td>
</tr>
<tr class="even">
<td align="left"><p>GuestUpdateDuration </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 240</p></td>
<td align="left"><p>O número de minutos que o MED-V deve manter o convidado ativo para a atualização automática, a partir do momento especificado no valor GuestUpdateTime. Intervalo = 0 a 1440. Definir esse valor como zero (0) desabilita a funcionalidade de correção de convidado.</p>
<p>Para obter mais informações sobre o patch de convidado para atualizações automáticas, consulte <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> gerenciando atualizações automáticas para espaços de trabalho do MED-V </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GuestUpdateTime </p></td>
<td align="left"><p>St</p></td>
<td align="left"><p>Padrão = 00:00</p></td>
<td align="left"><p>A hora e os minutos todos os dias em que o MED-V deve ativar o convidado para atualizações automáticas usando o padrão de relógio de 24 horas. Especificar a hora no formato HH: MM  </p>
<p>Para obter mais informações sobre o patch de convidado para atualizações automáticas, consulte <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> gerenciando atualizações automáticas para espaços de trabalho do MED-V </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>HostMemToGuestMem </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>1024, 2048, 4096, 8192, 16384 </p></td>
<td align="left"><p>Uma lista de valores de memória (MB) para o convidado, determinada pela RAM disponível no host. Combinado com GuestMemFromHostMem, uma tabela de pesquisa é criada para determinar a quantidade de memória RAM a ser alocada na máquina virtual convidada. Os valores possíveis podem ser de 1024 a 16384.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HostMemToGuestMemCalcEnabled</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 1</p></td>
<td align="left"><p>Configura se a memória alocada para o convidado é calculada a partir da memória presente no host.  0 = falso; 1 = verdadeiro.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: a memória alocada para o convidado não é calculada a partir da memória presente no host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadeiro: a memória alocada para o convidado é calculada a partir da memória presente no host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Memória </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 512</p></td>
<td align="left"><p>A RAM (MB) que deve ser alocada para a máquina virtual convidada. Essa configuração será ignorada se a configuração HostMemToGuestMemEnabled estiver habilitada. Intervalo = de 128 a 2048.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MultiUserEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 0</p></td>
<td align="left"><p>Configura se vários usuários compartilham o mesmo espaço de trabalho do MED-V.  0 = falso; 1 = verdadeiro.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = falso: vários usuários não compartilham o mesmo espaço de trabalho do MED-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = verdadeiro: vários usuários compartilham o mesmo espaço de trabalho do MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Networkingmode </p></td>
<td align="left"><p>St</p></td>
<td align="left"><p>Padrão = NAT</p></td>
<td align="left"><p>O tipo de conexão de rede usado no convidado. Os valores possíveis são os seguintes:</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Com ponte </strong> . O MED-V tem seu próprio endereço de rede, normalmente obtido por meio de DHCP.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>NAT </strong> . O MED-V usa a NAT (conversão de endereços de rede) para compartilhar o host&#39;s de IP para o tráfego de saída.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TaskTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 600</p></td>
<td align="left"><p>Um valor de tempo limite geral, em segundos, em que o MED-V aguarda a conclusão de uma tarefa, como reinício e desligamento. Intervalo = 0 a 2147483647.</p></td>
</tr>
</tbody>
</table>



## Configurações do registro de convidado


Esta seção lista as chaves configuráveis do registro de convidado do MED-V e explica seus usos.

### v2

A tabela a seguir fornece informações sobre o valor do registro Guest associado à chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome </th>
<th align="left">Tipo </th>
<th align="left">Dados/padrão </th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>EnableGPWorkarounds</p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Padrão = 1 </p></td>
<td align="left"><p>Configura como o MED-V manipula as chaves BufferPolicyReads e GroupPolicyMinTransferRate.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>Por padrão, o MED-V define estas chaves da seguinte maneira:</p>
<p>BufferPolicyReads = 1 e GroupPolicyMinTransferRate = 0.</p>
<p>Crie a chave EnableGPWorkarounds, se for necessário, e defina a chave como zero se você não quiser que o MED-V altere as configurações padrão de BufferPolicyReads e GroupPolicyMinTransferRate.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Se o seu espaço de trabalho do MED-V estiver em execução no modo NAT, o EnableGPWorkarounds afetará as chaves do registro BufferPolicyReads e GroupPolicyMinTransferRate. Se o seu espaço de trabalho do MED-V estiver em execução no modo de ponte, o EnableGPWorkarounds afetará apenas a chave do registro BufferPolicyReads.</p>
</div>
<div>

</div>
<p>1 = verdadeiro: o MED-V define as chaves BufferPolicyReads = 1 e GroupPolicyMinTransferRate = 0 (se estiver em execução no modo NAT) ou apenas BufferPolicyReads = 1 (se estiver em execução no modo de ponte).</p>
<p>0 = falso: o MED-V não faz nenhuma alteração nas chaves BufferPolicyReads e GroupPolicyMinTransferRate.</p></td>
</tr>
</tbody>
</table>



## Tópicos relacionados


[Gerenciar aplicativos de área de trabalho da MED-V](manage-med-v-workspace-applications.md)

[Gerenciar o redirecionamento da URL da MED-V](manage-med-v-url-redirection.md)

[Gerenciar configurações de espaço de trabalho da MED-V](manage-med-v-workspace-settings.md)









