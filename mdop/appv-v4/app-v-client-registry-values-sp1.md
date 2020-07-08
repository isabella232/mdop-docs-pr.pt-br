---
title: Valores de Registro do cliente do App-V
description: Valores de Registro do cliente do App-V
author: dansimp
ms.assetid: 46af5209-9762-47b9-afdb-9a2947e013f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 05cd807ff9882bc478aca07abc4a28cdea83086a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797599"
---
# Valores de Registro do cliente do App-V


O cliente do Microsoft Application Virtualization (App-V) armazena sua configuração no registro. Você pode coletar algumas informações úteis sobre o cliente se compreender o formato dos dados no registro. Você também pode configurar várias ações do cliente alterando as entradas do registro. Este tópico lista todas as chaves do registro do cliente do Application Virtualization (App-V) e explica seus usos.

**Importante**  
Em um computador que executa um sistema operacional de 64 bits, as chaves e os valores descritos nas seções a seguir estarão em HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.



## Chave de configuração


A tabela a seguir fornece informações sobre os valores do registro associados à chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration.

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
<th align="left">Dados (exemplos)</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProductName</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Cliente de desktop do Microsoft Application Virtualization</p></td>
<td align="left"><p>Não modifique.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versão </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>4.5.0.xxx </p></td>
<td align="left"><p>Não modifique. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>Drivers </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>Sftfs.sys </p></td>
<td align="left"><p>Se esse valor da chave estiver presente, ele conterá o nome do driver que causou um erro de parada na última vez que o núcleo foi iniciado. Depois de corrigir o erro de parada, você deve excluir esse valor de chave para que o sftlist possa começar.</p></td>
</tr>
<tr class="even">
<td align="left"><p>InstallPath </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>Padrão = C:\Arquivos de Programas\microsoft Application Virtualization Client</p></td>
<td align="left"><p>O local onde o cliente está instalado. Não modifique. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>LogFilename </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>Padrão = CSIDL_COMMON_APPDATA a virtualização do \Microsoft\Application Client\sftlog.txt</p></td>
<td align="left"><p>O caminho e o nome do arquivo de log do cliente.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Se você estiver executando uma versão anterior do App-V 4,6, SP1 e modificar o nome ou o local do arquivo de log, será necessário reiniciar o serviço sftlist para que a alteração entre em vigor.</p>
</div>
<div>

</div>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>LogMinSeverity </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Padrão = 4, informativo</p></td>
<td align="left"><p>Controla quais mensagens são gravadas no log. O valor indica um limite do que é registrado – tudo que é menor ou igual a esse valor é registrado. Por exemplo, um valor de 0x3 (Warning) indica que avisos (0x3), erros (0x2) e erros críticos (0x1) são registrados.</p>
<p>Intervalo de valores: 0x0 = nenhum, 0x1 = crítica, 0x2 = erro, 0x3 = aviso, 0x4 = informações (padrão), 0x5 = Verbose.</p>
<p>O nível de log é configurável do console do cliente do Application Virtualization (App-V) e do prompt de comando. Em um prompt de comando, o comando sftlist.exe/verboselog irá aumentar o nível de log para Verbose. Para obter mais informações sobre os detalhes da linha de comando, consulte</p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467">https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467</a></p>
<p>.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LogRolloverCount</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 4</p></td>
<td align="left"><p>Define o número de cópias de backup do arquivo de log que são mantidas quando ele é redefinido. O intervalo válido é de 0 a 9999. O padrão é 4. Um valor 0 significa que nenhuma cópia será mantida.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LogMaxSize</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 256</p></td>
<td align="left"><p>Define o tamanho máximo em megabytes (MB) que o arquivo de log pode aumentar antes de ser redefinido. O tamanho padrão é de 256 MB. Quando esse tamanho for atingido, uma redefinição de log será forçada na próxima tentativa de gravação.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SystemEventLogLevel</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 0x4 (App-V 4,5)</p>
<p>Padrão = 0x3 (App-V 4,6)</p></td>
<td align="left"><p>Indica o nível de log no qual as mensagens de log são gravadas no log de eventos do NT. O valor indica um limite do que é registrado, ou seja, tudo é igual a ou menor que o valor é registrado. Por exemplo, um valor de 0x3 (Warning) indica que avisos (0x3), erros (0x2) e erros críticos (0x1) são registrados.</p>
<p>Intervalo de valores</p>
<p>0x0 = nenhum</p>
<p>0x1 = crítica</p>
<p>0x2 = erro</p>
<p>0x3 = aviso</p>
<p>0x4 = informações (padrão)</p>
<p>0x5 = Verbose</p></td>
</tr>
<tr class="even">
<td align="left"><p>AllowIndependentFileStreaming</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 0</p></td>
<td align="left"><p>Indica se o streaming do arquivo será habilitado independentemente de como o cliente foi configurado com o parâmetro APPLICATIONSOURCEROOT. Se definido como FALSE, o transporte não habilitará o streaming de arquivos, mesmo que o parâmetro OSD HREF ou APPLICATIONSOURCEROOT contenha um caminho de arquivo.</p>
<p>0x0 = falso (padrão)</p>
<p>0x1 = verdadeiro</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ApplicationSourceRoot</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps</p>
<p><a href="https://mainserver:443/prodapps" data-raw-source="https://mainserver:443/prodapps">https://mainserver:443/prodapps</a></p>
<p>arquivo://\uncserver\share\prodapps</p>
<p>arquivo://\uncserver\share</p></td>
<td align="left"><p>Habilita um administrador ou um sistema ESD (Electronic Software Distribution) para garantir que o carregamento do aplicativo seja executado de acordo com o esquema de gerenciamento de topologia. Use esse valor de chave para substituir a base de código do OSD do elemento HREF (por exemplo, o local de origem) de um aplicativo. A raiz de origem do aplicativo suporta URLs e formatos de caminho UNC (Convenção Universal de nomenclatura).</p>
<p>O formato correto para o caminho da URL é protocolo: URL do pedido: [porta] [/Path] [/], em que a porta e o caminho são opcionais. Se uma porta não for especificada, a porta padrão para o protocolo será usada. Somente a porção Protocol://Server: Port da URL OSD é substituída. </p>
<p>O formato correto para o caminho UNC é \computername\sharefolder [pasta] [], em que a pasta é opcional. O nome do computador pode ser um FQDN (nome de domínio totalmente qualificado) ou um endereço IP, e ShareFolder pode ser uma letra de unidade. Somente a parte \computername\sharefolder ou letra da unidade do caminho OSD é substituída. </p></td>
</tr>
<tr class="even">
<td align="left"><p>OSDSourceRoot</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>\computername\sharefolder\resource</p>
<p>\computername\content</p>
<p>C:\foldername</p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p>Permite que um administrador especifique um local de origem para a recuperação de arquivo OSD para um pacote de aplicativo sequenciado durante a publicação. Formatos aceitáveis para o OSDSourceRoot incluem caminhos e URLs UNC (http ou HTTPS).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IconSourceRoot</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>\computername\sharefolder\resource</p>
<p>\computername\content</p>
<p>C:\foldername</p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p>Permite que um administrador especifique um local de origem para a recuperação de arquivo de ícone para um pacote de aplicativo sequenciado durante a publicação. Formatos aceitáveis para o IconSourceRoot incluem caminhos e URLs UNC (http ou HTTPS).</p></td>
</tr>
<tr class="even">
<td align="left"><p>AutoLoadTriggers</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 5</p></td>
<td align="left"><p>AutoLoad é um parâmetro de configuração da política de tempo de execução do cliente que permite que o bloco de recursos secundário de um aplicativo virtualizado seja transmitido para o cliente automaticamente em segundo plano. Os gatilhos AutoLoad são sinalizadores para indicar eventos que iniciam o carregamento automático de aplicativos. AutoLoad usa implicitamente o streaming em segundo plano para permitir que o aplicativo seja totalmente carregado no cache. O bloco de recursos principal será carregado primeiro, e os blocos de recursos restantes serão carregados em segundo plano para permitir operações em primeiro plano, como interação do usuário com aplicativos, para ocorrer e fornecer desempenho percebido otimizado.</p>
<p>Valores de máscara de bits:</p>
<p>(0) nunca: não há bits definidos (valor é 0), nenhum carregamento automático será executado porque não há gatilhos definidos.</p>
<p>(1) OnLaunch: o carregamento será iniciado quando um usuário iniciar um aplicativo.</p>
<p>(2) OnRefresh: o carregamento será iniciado quando o aplicativo for publicado. Isso ocorre sempre que o registro do pacote é adicionado ou atualizado, por exemplo, quando ocorre uma atualização de publicação.</p>
<p>(4) OnLogin: o carregamento começa quando um usuário faz logon.</p>
<p>(5) OnLaunch e OnLogin: default.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AutoLoadTarget</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 1</p></td>
<td align="left"><p>Indica o que será carregado automaticamente quando um determinado disparador de autocarregamento ocorrer. Valores de máscara de bits:</p>
<p>(0) nenhum: não é possível carregar automaticamente, independentemente de quais gatilhos podem ser definidos.</p>
<p>(1) PreviouslyUsed (padrão): se qualquer gatilho de AutoLoad estiver habilitado, carregue somente os pacotes nos quais pelo menos um aplicativo do pacote tenha sido usado anteriormente, ou seja, iniciado ou previamente armazenado em cache.</p>
<p>(2) All: se qualquer gatilho de AutoLoad estiver habilitado, todos os aplicativos no pacote (por pacote) ou todos os pacotes (definidos para o cliente) serão carregados automaticamente, independentemente de terem sido iniciados.</p></td>
</tr>
<tr class="even">
<td align="left"><p>RequireAuthorizationIfCached</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 1</p></td>
<td align="left"><p>Indica que a autorização sempre é necessária, seja ou não um aplicativo que já esteja em cache. Valores possíveis:</p>
<p>0 = falso: sempre tente se conectar ao servidor. Se não for possível estabelecer uma conexão com o servidor, o cliente ainda permite que o usuário inicie um aplicativo que tenha sido carregado anteriormente no cache.</p>
<p>1 = verdadeiro (padrão): o aplicativo sempre deve ser autorizado na inicialização. Para aplicativos de fluxo RTSP, o token de autorização do usuário é enviado ao servidor para autorização. Para aplicativos baseados em arquivos, as ACLs de arquivo controlam se um usuário pode acessar o aplicativo.</p>
<p>Reinicie o serviço sftlist para que a alteração entre em vigor.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UserDataDirectory </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>AppData</p></td>
<td align="left"><p>Local onde o cache de ícone e as configurações de usuário são armazenados.</p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalDataDirectory </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>C:\Users\Public\Documents </p></td>
<td align="left"><p>Diretório a ser usado para dados global App-V, incluindo caches de arquivos OSD, arquivos de ícone, informações de atalho e recursos de SystemGuard, como arquivos. ini.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AllowCrashes </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>0 ou 1 </p></td>
<td align="left"><p>Padrão = 0: um valor de 0 significa que o cliente tenta capturar exceções de programa internas para que outros aplicativos do usuário possam recuperar e continuar quando ocorrer uma falha. Um valor 1 significa que o cliente permite que as exceções de programa internas ocorram para que possam ser capturadas em um depurador.</p></td>
</tr>
<tr class="even">
<td align="left"><p>CoreInternalTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>60</p></td>
<td align="left"><p>Tempo limite em segundos para solicitações de IPC internas entre núcleo e front-end. Não modifique. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>DefaultSuiteCombineTime </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>254</p></td>
<td align="left"><p>Esse valor é usado para indicar quanto tempo após ter sido iniciado que um programa pode desligar e não gerar nenhuma mensagem de erro quando outro aplicativo no mesmo pacote estiver em execução. </p></td>
</tr>
<tr class="even">
<td align="left"><p>SerializedSuiteLaunchTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Padrão = 60000</p></td>
<td align="left"><p>Define por quanto tempo em milissegundos o cliente esperará à medida que tenta serializar o programa começa no mesmo pacote. Se o cliente expirar, o programa será iniciado, mas não será serializado. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>ScriptTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>300</p></td>
<td align="left"><p>Tempo limite padrão em segundos para scripts no arquivo OSD se WAIT = TRUE. Você pode especificar o tempo limite de cada script com o tempo limite em vez de AGUARDAr. Um valor 0 significa que não há espera, e 0xFFFFFFFF significa esperar para sempre. </p></td>
</tr>
<tr class="even">
<td align="left"><p>LaunchRecordLogPath </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p></p></td>
<td align="left"><p>Se, em HKLM ou HKCU, esse valor contiver um caminho válido para um arquivo de log, o SFTTray será gravado nesse log quando os programas iniciarem, desligar, falham ao iniciar e entrarem ou saírem do modo desconectado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LaunchRecordMask </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>0x1A (26) erros de início de log e atividades de entrada e saída no modo desconectado.</p>
<p>0x1F (31) registra tudo.</p>
<p>0x0 (0) registra nada. </p></td>
<td align="left"><p>Especifica quais são os cinco eventos registrados (valores de bitmask):</p>
<p>1 para o programa é iniciado</p>
<p>2 para erros de falha na inicialização</p>
<p>4 para desligamentos</p>
<p>8 para entrar no modo desconectado</p>
<p>16 para sair do modo desconectado para se reconectar a um servidor</p>
<p>Adicione qualquer combinação desses números para ativar as respectivas mensagens. O padrão é 0x1F, se não estiver no registro. </p></td>
</tr>
<tr class="even">
<td align="left"><p>LaunchRecordWriteTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Padrão = 3000</p></td>
<td align="left"><p>Especifica em milissegundos quanto tempo a bandeja esperará ao tentar gravar no log de lançamento de lançamento se outro processo estiver usando.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ImportSearchPath </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>d:\files; C:\Documents and settings\user1\SFTs </p></td>
<td align="left"><p>Uma lista delimitada por ponto-e-vírgula com até cinco pastas para pesquisar arquivos SFT portáteis antes de solicitar que o usuário selecione um diretório. A barra invertida no caminho é opcional. Esse valor não está presente por padrão e deve ser definido manualmente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>UserImportPath</p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>D:\SFTs\ </p></td>
<td align="left"><p>Válido somente em HKCU. O último local para o qual o usuário navegou durante a localização de um arquivo SFT para a importação de pacote. Definido automaticamente se o SFT for encontrado com êxito. Isso é usado em importações sucessivas ao tentar localizar arquivos SFT automaticamente.</p></td>
</tr>
</tbody>
</table>



## Chave compartilhada


A chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Shared controla os valores compartilhados entre componentes do App-V. A tabela a seguir fornece informações sobre os valores do registro associados à chave compartilhada.

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
<th align="left">Dados (exemplos) </th>
<th align="left">Descrição </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>DumpPath </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>Padrão = C:\ </p></td>
<td align="left"><p>Caminho padrão para criar arquivos de despejo ao gerar um minidespejo em uma exceção. Usa como padrão C:\ Se não especificado. O instalador do cliente define essa chave para o &lt; diretório de dados globais do App Virtualization &gt; \Dumps. O instalador do sequenciador define essa chave para o diretório de instalação. </p></td>
</tr>
<tr class="even">
<td align="left"><p>DumpPathSizeLimit </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>1000</p></td>
<td align="left"><p>Especifica a quantidade total máxima de espaço em disco em megabytes que pode ser usada para armazenar minidespejos. Padrão = 1000 MB.</p></td>
</tr>
</tbody>
</table>



## Chave de rede


A chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network controla uma variedade de parâmetros relacionados à rede. Essa chave é usada principalmente pelo agente de transporte de rede. A tabela a seguir fornece informações sobre os valores do registro associados à chave de rede.

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
<th align="left">Dados (exemplos) </th>
<th align="left">Descrição </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Online</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 1</p></td>
<td align="left"><p>Habilita ou desabilita o modo offline. Se definido como 0, o cliente não se comunicará com os servidores de gerenciamento do App-V ou servidores de publicação. Em operações desconectadas, o cliente pode iniciar um aplicativo carregado mesmo quando não estiver conectado a um servidor de gerenciamento do App-V. No modo offline, o cliente não tenta se conectar a um servidor de gerenciamento do App-V ou ao servidor de publicação. Você deve permitir que operações desconectadas possam funcionar offline. O valor padrão é 1 habilitado (online) e 0 está desabilitado (offline).</p></td>
</tr>
<tr class="even">
<td align="left"><p>AllowDisconnectedOperation </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Padrão = 1</p></td>
<td align="left"><p>Habilita ou desabilita a operação desconectada. O valor padrão é 1 habilitado e 0 está desabilitado. Quando operações desconectadas estão habilitadas, o cliente App-V pode iniciar um aplicativo carregado mesmo quando não estiver conectado a um servidor de gerenciamento do App-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FastConnectTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 1000</p></td>
<td align="left"><p>Esse valor especifica o tempo limite de conexão TCP em milissegundos para determinar quando acessar o modo de operações desconectadas. Esse valor pode ser usado para substituir o ConnectTimeout padrão de 20 segundos (App-V Connect time out para transações de rede) ou o tempo limite TCP do sistema de aproximadamente 25 segundos. Isso leva o cliente para o modo de operações desconectadas rapidamente. Aplicado à próxima conexão.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LimitDisconnectedOperation</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 1 </p></td>
<td align="left"><p>Aplicável somente se AllowDisconnectedOperation for 1, habilitado. Esse valor determina se haverá um limite de tempo para o tempo que o cliente terá permissão para operar em operações desconectadas. 1 = limitado. 0 = ilimitado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DOTimeoutMinutes</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 129600</p></td>
<td align="left"><p>Indica por quantos minutos um aplicativo pode ser usado no modo de operação desconectado.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>Os valores válidos são 1 – 999999 em dias expressos em minutos (1 – 1439998560 minutos). O valor padrão é 90 dias ou 129.600 minutos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Protocolo</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 8</p></td>
<td align="left"><p>Protocolo padrão a ser usado (TCP versus SSL). Configurar na caixa de diálogo opções.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReadTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>cedido</p></td>
<td align="left"><p>Leia o tempo limite para transações de rede em segundos. Não modifique.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>WriteTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>cedido</p></td>
<td align="left"><p>Tempo limite de gravação para transações de rede em segundos. Não modifique.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ConnectTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>cedido</p></td>
<td align="left"><p>Tempo limite de conexão para transações de rede em segundos. Não modifique.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReestablishmentRetries</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>3D</p></td>
<td align="left"><p>O número de vezes para tentar restabelecer uma sessão interrompida.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReestablishmentInterval</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>15</p></td>
<td align="left"><p>O número de segundos de espera entre as tentativas para restabelecer uma sessão interrompida.</p></td>
</tr>
</tbody>
</table>



## Tecla http


A chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\Http controla os parâmetros relacionados ao streaming http. Essa chave é usada principalmente pelo agente de transporte de rede. A tabela a seguir fornece informações sobre os valores do registro associados à tecla http.

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
<th align="left">Dados (exemplos) </th>
<th align="left">Descrição </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>LaunchIfNotFound</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 0</p></td>
<td align="left"><p>Controla o comportamento do streaming HTTP quando uma conexão com o servidor HTTP pode ser estabelecida e o arquivo de pacote não existe mais no servidor HTTP. Se o valor não existir ou se não for definido como 1, o cliente App-V não permitirá que você inicie um aplicativo que tenha sido carregado anteriormente no cache.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>um</p></td>
<td align="left"><p>Se esse valor for definido como 1, o cliente App-V permitirá que você inicie um aplicativo que tenha sido carregado anteriormente no cache.</p></td>
</tr>
</tbody>
</table>



## Chave do sistema de arquivos


Os valores contidos na chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS controlam os parâmetros do sistema de arquivos para App-V. A tabela a seguir fornece informações sobre os valores do registro associados à chave AppFS.

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
<th align="left">Dados (exemplos) </th>
<th align="left">Descrição </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>FileSize </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>4096</p></td>
<td align="left"><p>Tamanho máximo em megabytes do arquivo de cache do sistema de arquivos. Se você alterar esse valor no registro, deverá definir o estado como 0 e reinicializar. </p></td>
</tr>
<tr class="even">
<td align="left"><p>FileName </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>C:\Users\Public\Documents\SoftGrid Client\sftfs.fsd </p></td>
<td align="left"><p>Local do arquivo de cache do sistema de arquivos. Se você alterar esse valor no registro, deverá deixar o tamanho do registro igual e reinicializar ou definir o estado como 0 e reiniciar. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>DriveLetter </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>P: </p></td>
<td align="left"><p>Unidade onde o sistema de arquivos App-V será montado, se estiver disponível. Esse valor é definido pelo ouvinte ou pelo instalador, e ele é lido pelo sistema de arquivos. </p></td>
</tr>
<tr class="even">
<td align="left"><p>Estado </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>0x100 </p></td>
<td align="left"><p>Estado do sistema de arquivos. Definido como 0 e reinicializar para limpar completamente o cache do sistema de arquivos. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>FileSystemStorage </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>C:\Profiles\Joe\SG </p></td>
<td align="left"><p>Caminho para symlinks, definido em HKCU. Não modifique (use o diretório de dados em configuração para alterar). </p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalFileSystemStorage </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>Armazenamento Client\AppFS C:\Users\Public\Documents\SoftGrid </p></td>
<td align="left"><p>Caminho para dados do sistema de arquivos globais. Não modifique. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxPercentToLockInCache </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Padrão = 90 </p></td>
<td align="left"><p>Especifica a porcentagem máxima do arquivo de cache do sistema de arquivos que pode ser bloqueada. Não modifique.</p></td>
</tr>
<tr class="even">
<td align="left"><p>UnloadLeastRecentlyUsed</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 1</p></td>
<td align="left"><p>O recurso gerenciamento de espaço em cache do sistema de arquivos usa um algoritmo menos recentemente usado (LRU) e é habilitado por padrão. Se o espaço necessário para um novo pacote exceder o espaço livre disponível no cache, o cliente App-V usará esse recurso para determinar quais pacotes existentes, que podem ser excluídos do cache, podem ser excluídos do cache para liberar espaço para o novo pacote. O cliente exclui o pacote com a data mais recente acessada se for anterior ao valor especificado no valor do registro MinPkgAge. Os valores são 0 (desabilitados) e 1 (padrão, habilitado).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MinPackageAge</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>um</p></td>
<td align="left"><p>Para determinar quando o pacote pode ser selecionado para descarte, defina esse valor do registro como igual ao número mínimo de dias que você deseja que decorra desde o último pacote ter sido acessado. Os pacotes que foram usados mais recentemente não são descartados.</p></td>
</tr>
</tbody>
</table>



## Chave de permissões


Para ajudar a evitar erros, os administradores podem usar a chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions para controlar o acesso a algumas ações para usuários não administrativos, por exemplo, para impedir que os usuários descarreguem acidentalmente programas. Os usuários com direitos administrativos podem dar a si qualquer uma dessas permissões. Em sistemas compartilhados, como um sistema de host de sessão de área de trabalho remota (host de sessão de RD) (antigo Terminal Server), tenha cuidado ao conceder permissões adicionais a usuários, pois algumas dessas permissões permitem que os usuários controlem os aplicativos usados por todos os usuários do sistema. Os valores possíveis para essas configurações são 1 (Allow) e 0 (não permite).

As configurações da chave Permissions controlam todas as interfaces que permitem as ações nomeadas. Isso inclui a caixa de diálogo opções, SFTTray e SFTMime. Essas configurações não afetam os administradores. A tabela a seguir fornece informações sobre os valores do registro associados à chave de permissões.

Dados de tipo de nome (exemplos) Descrição ChangeFSDrive

DWORD

Padrão = 0

Um valor de 1 permite que os usuários selecionem uma letra de unidade diferente para ser usada como unidade do sistema de arquivos.

ChangeCacheSize

DWORD

Padrão = 0

Um valor de 1 permite que os usuários alterem o tamanho do cache.

ChangeLogSettings

DWORD

Padrão = 0

Um valor 1 permite aos usuários modificar o nível de log, alterar sua localização e redefini-lo por meio da interface do usuário.

AddApp

DWORD

Padrão = 0

Um valor 1 permite que os usuários adicionem aplicativos explicitamente. Isso não afeta os aplicativos que são adicionados por meio da atualização de publicação nem impede os usuários de iniciar (e, portanto, adicionar implicitamente) aplicativos que ainda não foram adicionados. Valores são 0 ou 1.

LoadApp 

DWORD 

0

Não permite que um usuário carregue um aplicativo. Esse é o padrão para os hosts da sessão da área de trabalho remota. Se você for um usuário móvel, talvez queira carregar completamente seus aplicativos no cache para usá-los durante a operação desconectada ou o modo offline. Para transmitir aplicativos do servidor de gerenciamento do App-V ou do App-V Streaming Server, você deve estar conectado a um servidor para carregar aplicativos.

um

Permite que um usuário carregue um aplicativo. Este é o padrão para áreas de trabalho do Windows. 

UnloadApp 

DWORD 

0

Não permite que um usuário descarregue um aplicativo. Quando você carrega ou descarrega um pacote, todos os aplicativos no pacote são carregados em ou removidos do cache.

um

Permite que um usuário descarregue um aplicativo. 

LockApp 

DWORD 

0

Não permite que um usuário bloqueie e desbloqueie um aplicativo. Esse é o padrão para os hosts da sessão da área de trabalho remota. Um aplicativo bloqueado não pode ser removido do cache para criar espaço para novos aplicativos. Para remover um aplicativo bloqueado do cache da área de trabalho do App-V ou do cliente para serviços de área de trabalho remota (anteriormente Terminal Services), você deve desbloqueá-lo.

um

Permite que um usuário bloqueie e desbloqueie um aplicativo. Este é o padrão para áreas de trabalho do Windows. 

ManageTypes 

DWORD 

0

Não permite que um usuário adicione, edite ou remova associações de tipo de arquivo para aquele usuário sozinha. Esse é o padrão para os hosts da sessão da área de trabalho remota. 

um

Permite que um usuário adicione, edite e remova associações de tipo de arquivo somente para esse usuário e não globalmente. Este é o padrão para áreas de trabalho do Windows. 

RefreshServer 

DWORD 

0

Não permite que um usuário Acione uma atualização de configurações MIME. Esse é o padrão para os hosts da sessão da área de trabalho remota. 

um

Permite que um usuário Acione uma atualização de configurações MIME. Este é o padrão para áreas de trabalho do Windows. 

UpdateOSDFile

DWORD

Padrão = 0

Um valor de 1 permite que um usuário use um arquivo OSD modificado.

ImportApp 

DWORD 

0

Não permite que um usuário importe aplicativos para o cache. A diferença entre Load e Import é que, quando uma carga é disparada, o cliente obtém o pacote do local configurado atualmente contido na URL OSD, ASR ou override. Ao usar a importação, um local para obter o pacote deve ser especificado. 

um

Permite que um usuário importe aplicativos para o cache. 

ChangeRefreshSettings

DWORD

Padrão = 0

Um valor de 1 permite que os usuários modifiquem as configurações de atualização para os servidores (atualizar ao fazer logon e atualização periódica). Isso não significa que o usuário pode modificar outras configurações do servidor (caminho, host e assim por diante).

ManageServers

DWORD

Padrão = 0

Um valor 1 permite que o usuário adicione, edite e remova servidores, exceto para editar as configurações de atualização, que são controladas pela permissão ChangeRefreshSettings.

PublishShortcut

DWORD

Padrão = 0

Um valor 1 permite que os usuários publiquem atalhos por meio da interface do usuário. Isso não afeta os atalhos que são publicados durante uma atualização de publicação.

ViewAllApplications

DWORD

Padrão = 0

Um valor 1 exibe todos os aplicativos por meio da interface do usuário; caso contrário, somente os aplicativos do usuário são exibidos.

RepairApp

DWORD

Padrão = 1

Um valor de 1 permite que o usuário use a ação de reparo em aplicativos no SFTMime ou no console de gerenciamento de cliente. Ao reparar um aplicativo, você remove qualquer configuração de usuário personalizada e restaura as configurações padrão. Essa ação não altera ou exclui atalhos ou associações de tipo de arquivo, e não remove o aplicativo do cache.

ClearApp

DWORD

Padrão = 1

Um valor 1 permite que o usuário use a ação limpar em aplicativos no SFTMime ou o console de gerenciamento de cliente. Ao limpar um aplicativo do console, você não pode mais usar esse aplicativo. No entanto, o aplicativo permanece em cache e ainda está disponível para outros usuários no mesmo sistema. Após uma atualização de publicação, os aplicativos limpos ficarão novamente disponíveis para você.

DeleteApp

DWORD

Padrão = 0

Um valor de 1 permite que o usuário use a ação de exclusão em aplicativos no SFTMime ou o console de gerenciamento de cliente. Quando você exclui um aplicativo, o aplicativo selecionado não estará mais disponível para os usuários do cliente. Os atalhos e associações de tipo de arquivo são excluídos e o aplicativo é excluído do cache. No entanto, se outro aplicativo se refere a dados no cache do sistema de arquivos ou dados de configurações para o aplicativo selecionado, esses itens não serão excluídos.

Após uma atualização de publicação, os aplicativos excluídos ficarão novamente disponíveis para você.

ToggleOfflineMode

DWORD

Um valor 1 permite que os usuários selecionem executar o cliente no modo offline. No modo offline, o cliente de virtualização de aplicativo pode iniciar um aplicativo carregado mesmo quando ele não está conectado a um servidor de virtualização de aplicativo.



## Configurações personalizadas


A chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\CustomSettings contém valores específicos para componentes de front-end. Todas as configurações personalizadas são armazenadas como cadeias de caracteres. A tabela a seguir fornece informações sobre os valores do registro associados à chave CustomSettings.

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
<th align="left">Dados (exemplos) </th>
<th align="left">Descrição </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>TrayErrorDelay </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Padrão = 30 </p></td>
<td align="left"><p>Tempo em segundos durante os quais a área de notificação do Application Virtualization exibirá mensagens de erro, como &quot; falha na inicialização &quot; . Valor mínimo de 1. </p></td>
</tr>
<tr class="even">
<td align="left"><p>TraySuccessDelay </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Padrão = 10 </p></td>
<td align="left"><p>Tempo em segundos que a área de notificação do appvmed exibirá mensagens de sucesso como o &quot; Word foi iniciado &quot; ou o Excel será &quot; desligado &quot; . Se 0, essas mensagens serão suprimidas. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>TrayVisibility</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 0</p></td>
<td align="left"><p>0 = mostrar bandeja quando aplicativos virtualizados estiverem em uso.</p>
<p>1 = mostrar bandeja sempre.</p>
<p>2 = nunca mostrar a bandeja.</p></td>
</tr>
<tr class="even">
<td align="left"><p>TrayShowRefresh</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Quando apresentar e definido como um valor de 1, permite que os aplicativos de atualização de item de menu sejam exibidos no menu de bandeja e podem ser acessados pelo usuário.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TrayShowLoad</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Quando apresentar e definido como um valor de 1, permite que os aplicativos de carregamento de item de menu sejam exibidos no menu de bandeja e são acessíveis pelo usuário.</p></td>
</tr>
</tbody>
</table>



## Configurações de relatório


A chave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Reporting contém valores específicos para relatório para um servidor de gerenciamento App-V. A tabela a seguir fornece informações sobre os valores do registro associados à chave de relatório.

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
<th align="left">Dados (exemplos) </th>
<th align="left">Descrição </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>DataCacheLimit</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 20</p></td>
<td align="left"><p>Esse valor especifica o tamanho máximo em megabytes (MB) do cache XML para armazenar informações de relatório. O tamanho se aplica ao cache na memória. Quando o limite for atingido, o arquivo de log será revertido. Quando um novo registro for adicionado (na parte inferior da lista), um ou mais dos registros mais antigos (topo da lista) serão excluídos para liberar espaço. Um aviso será registrado no log do cliente e no log de eventos na primeira vez que isso ocorrer, e ele não será registrado novamente até que o cache seja limpo com êxito na transmissão e o log tenha sido preenchido novamente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Datablockize</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 65536</p></td>
<td align="left"><p>Esse valor especifica o tamanho máximo em bytes a ser transmitido ao servidor ao mesmo tempo na atualização de publicação, para evitar falhas de transmissão permanente quando o log atingir um tamanho significativo. O valor padrão é 65536. Ao transmitir dados de relatório para o servidor, um bloco de registros de aplicativo — menor ou igual ao tamanho do bloco em bytes de dados XML — será removido do cache e enviado ao servidor. Cada bloco terá os dados de cliente gerais e os dados da lista de pacotes globais preparados, e esses dados não serão fatorados nos cálculos de tamanho do bloco; o potencial existe para uma lista de pacotes extremamente grandes resultar em falhas de transmissão com largura de banda baixa ou conexões não confiáveis.</p></td>
</tr>
</tbody>
</table>



## Tópicos relacionados


[Referência do Application Virtualization Client](application-virtualization-client-reference.md)









