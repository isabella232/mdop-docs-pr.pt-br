---
title: SFTTRAY Referência de comandos
description: SFTTRAY Referência de comandos
author: dansimp
ms.assetid: 6fa3a939-b047-4d6c-bd1d-dfb93e065eb2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a664b91ff7edd5f8536f035417cc3b0f52d7ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796708"
---
# SFTTRAY Referência de comandos


O aplicativo da bandeja do cliente do Microsoft Application Virtualization (App-V), sfttray.exe, é o principal elemento de interface do usuário do cliente App-V com o qual os usuários irão interagir durante o uso normal. Este programa controla o streaming e a inicialização de todos os aplicativos virtuais e é acessado clicando com o botão direito do mouse no ícone exibido na área de notificação para exibir o menu de funções do cliente. O menu permite que o usuário carregue aplicativos, inicie uma atualização de publicação, cancele uma solicitação ou altere o cliente para o modo offline. O usuário também pode fechar o aplicativo da bandeja cliente do aplicativo virtualização e todos os aplicativos ativos clicando em **sair**.

Por padrão, o ícone é exibido sempre que um aplicativo virtual é iniciado, embora você possa controlar esse comportamento usando comandos SFTTRAY. O aplicativo de bandeja do cliente do Application Virtualization também exibe uma barra de progresso para cada aplicativo que é iniciado, bem como mensagens de status sobre aplicativos ativos. Clicar na barra de progresso exibe uma mensagem que permite que você cancele o carregamento ou o início de um aplicativo.

## Comandos SFTTRAY


A lista de comandos e opções de linha de comando pode ser exibida executando o seguinte comando em uma janela de comando.

**Observação**  
Há apenas uma instância de bandeja de cliente do aplicativo virtualização para cada contexto de usuário, portanto, se você iniciar um novo comando SFTTRAY, ele será passado para o programa que já está em execução.



`Sfttray.exe /?`

### Uso de comandos

`Sfttray.exe [/HIDE | /SHOW]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] [/EXE alternate-exe] /LAUNCH app [args]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOAD app [/SFTFILE sft]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOADALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /REFRESHALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LAUNCHRESULT <UNIQUE ID>  /LAUNCH app [args]`

`Sfttray.exe /EXIT`

### Opções de linha de comando

As opções de linha de comando SFTTRAY estão descritas na tabela a seguir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Opção</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/HIDE</p></td>
<td align="left"><p>Oculta o ícone do SFTTRAY na área de notificação do Windows.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SHOW</p></td>
<td align="left"><p>Exibe o ícone do SFTTRAY na área de notificação do Windows.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/QUIET</p></td>
<td align="left"><p>Oferece suporte ao uso autônomo impedindo que erros exibam caixas de mensagens que exijam confirmação de usuário.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/EXE &lt; alternativo-exe&gt;</p></td>
<td align="left"><p>Usado com/LAUNCH para especificar que um programa executável deve ser iniciado no ambiente virtual quando um aplicativo virtual é iniciado no lugar do arquivo de destino especificado no OSD.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Por exemplo, use "SFTTRAY.EXE/EXE REGEDIT.EXE aplicativo de/LAUNCH &lt; &gt; " para permitir que você examine o registro do ambiente virtual no qual o aplicativo está sendo executado.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Aplicativo/Launch &gt; [ &lt; args &gt; ]</p></td>
<td align="left"><p>Inicia um aplicativo virtual. Especifique o nome e a versão de um aplicativo ou o caminho para um arquivo OSD. Opcionalmente, argumentos de linha de comando podem ser passados para o aplicativo virtual.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Use o comando "SFTMIME.EXE/QUERY OBJ: APP/SHORT" para obter uma lista dos nomes e versões dos aplicativos virtuais disponíveis.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>/LOAD</p></td>
<td align="left"><p>Carrega ou importa um aplicativo virtual.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LOADALL</p></td>
<td align="left"><p>Carrega todos os aplicativos no cache.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/REFRESHALL</p></td>
<td align="left"><p>Inicia uma atualização de publicação para todos os aplicativos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;ID exclusiva do/LAUNCHRESULT&gt;</p></td>
<td align="left"><p>Retorna o código do resultado do lançamento para o processo que inicia sfttray.exe usando um evento global e um arquivo mapeado na memória que se baseia no nome raiz especificado para o ID exclusivo. ¹</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;SFT/SFTFILE&gt;</p></td>
<td align="left"><p>Opção opcional usada com/LOAD para especificar o caminho para o arquivo SFT do aplicativo. Se especificado, o aplicativo será importado em vez de ser carregado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/EXIT</p></td>
<td align="left"><p>Fecha o programa SFTTRAY e todos os aplicativos virtuais ativos e remove o ícone da área de notificação do Windows.</p></td>
</tr>
</tbody>
</table>



**Observação**  
¹ o parâmetro de linha de comando */LAUNCHRESULT* fornece um meio para o processo que inicia sfttray.exe para especificar o nome raiz para um evento global e um arquivo de memória mapeada que são usados para retornar o código do resultado do lançamento para o processo. O nome do identificador exclusivo deve começar com "SFT-" para impedir que o nome do evento seja virtualizado quando o processo de inicialização for invocado dentro de um ambiente virtual. A região mapeada na memória terá 64 bits em tamanho.

Para usar esse parâmetro, o processo de inicialização cria um evento com o nome " &lt; identificação exclusiva &gt; -resultado \ _event", um arquivo mapeado na memória com o nome " &lt; identificação exclusiva &gt; -resultado \ _value" e, opcionalmente, um evento com o nome " &lt; identificação exclusiva &gt; -Shutdown \ _event" e, em seguida, o processo de inicialização inicia sfttray.exe e aguarda o evento ser sinalizado. Após o evento " &lt; ID exclusivo &gt; -resultado \ _event" ser sinalizado, o processo de inicialização recupera o código de retorno de 64 bits da região mapeada na memória.

Se o evento opcional " &lt; ID exclusiva &gt; -shutdown \ _event" existir quando o aplicativo virtual sair, sfttray.exe abrir e sinalizar o evento. O processo de inicialização aguardará nesse evento de desligamento se precisar determinar quando o aplicativo virtual será encerrado.











