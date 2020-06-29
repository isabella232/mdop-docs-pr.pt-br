---
title: Parâmetros de linha de comando do instalador do Application Virtualization Client
description: Parâmetros de linha de comando do instalador do Application Virtualization Client
author: dansimp
ms.assetid: 508fa404-52a5-4919-8788-2a3dfb00639b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 911d333c80060c1881c96430c1d2d0516b6a4855
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797581"
---
# Parâmetros de linha de comando do instalador do Application Virtualization Client


A tabela a seguir lista todos os parâmetros de linha de comando disponíveis do instalador do cliente do Microsoft Application Virtualization, seus valores e uma breve descrição de cada parâmetro. Os parâmetros diferenciam maiúsculas de minúsculas e devem ser inseridos como letras maiúsculas. Todos os valores de parâmetro devem estar entre aspas duplas.

**Observação**  
-   Para o App-V versão 4,6, os parâmetros de linha de comando não podem ser usados durante uma atualização de cliente.

-   Os parâmetros *SWICACHESIZE* e *MINFREESPACEMB* não podem ser combinados na linha de comando. Se ambos forem usados, o parâmetro *SWICACHESIZE* será ignorado.



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parâmetro</th>
<th align="left">Valores</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em>ALLOWINDEPENDENTFILESTREAMING</em></p></td>
<td align="left"><p>TRUE</p>
<p>FALSE</p></td>
<td align="left"><p>Indica se o streaming do arquivo será habilitado independentemente de como o cliente foi configurado com o <em> parâmetro APPLICATIONSOURCEROOT </em> . Se definido como FALSE, o transporte não habilitará o streaming de arquivos, mesmo que o parâmetro OSD HREF ou <em> APPLICATIONSOURCEROOT </em> contenha um caminho de arquivo.</p>
<p>Valores possíveis:</p>
<ul>
<li><p>TRUE – o aplicativo implantado manualmente pode ser carregado do disco.</p></li>
<li><p>FALSE — todos os aplicativos devem vir do servidor de fluxo de origem.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em>APPLICATIONSOURCEROOT</em></p></td>
<td align="left"><p><em>URL RTSP:// </em> (para distribuição de pacote dinâmico)</p>
<p><em>URL file:// </em> ou <em> UNC </em> (para carga da entrega de pacotes de arquivos)</p></td>
<td align="left"><p>Para habilitar um administrador ou um sistema de distribuição de software eletrônico para garantir que o carregamento do aplicativo seja executado em conformidade com o esquema de gerenciamento de topologia, permite uma substituição da CODEBASE do OSD para o elemento HREF do aplicativo (o local de origem). Se o valor for "", que é o valor padrão, as configurações de arquivo OSD existentes serão usadas.</p>
<p>Uma URL tem várias partes:</p>
<p>&lt;protocolo &gt; :// &lt; servidor &gt; : &lt; caminho da porta &gt; / &lt; &gt; / &lt; ? consulta &gt; &lt; #fragment&gt;</p>
<p>Um caminho UNC tem três partes:</p>
<p>&amp;lt; ComputerName; ComputerName &gt; &amp; ; Share Folder &gt; &amp; lt; Resource&gt;</p>
<p>Se o <em> </em> parâmetro APPLICATIONSOURCEROOT for especificado em um cliente, o cliente irá romper a URL ou caminho UNC de um arquivo OSD em suas partes constituintes e substituir as seções OSD pelas <em> seções APPLICATIONSOURCEROOT correspondentes </em> .</p>
<div class="alert">
<strong>Importante</strong><br/><p>Certifique-se de usar o formato correto ao usar file://com um caminho UNC. O formato correto é file:// &amp; lt; Server &gt; &amp; lt; Server lt; share &gt; .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em>ICONSOURCEROOT</em></p></td>
<td align="left"><p><em>UNC</em></p>
<p>URL <em> http:// </em> ou <em> URL https://</em></p></td>
<td align="left"><p>Permite que um administrador especifique um local de origem para a recuperação de ícone para um pacote de aplicativo sequenciado durante a publicação. As raízes de origem dos ícones dão suporte a caminhos e URLs UNC (HTTP ou HTTPS). Se o valor for "", que é o valor padrão, as configurações de arquivo OSD existentes serão usadas.</p>
<p>Uma URL tem várias partes:</p>
<p>&lt;protocolo &gt; :// &lt; servidor &gt; : &lt; caminho da porta &gt; / &lt; &gt; / &lt; ? consulta &gt; &lt; #fragment&gt;</p>
<p>Um caminho UNC tem três partes:</p>
<p>&amp;lt; ComputerName; ComputerName &gt; &amp; ; Share Folder &gt; &amp; lt; Resource&gt;</p>
<div class="alert">
<strong>Importante</strong><br/><p>Certifique-se de usar o formato correto ao usar um caminho UNC. Os formatos aceitáveis são &amp; lt; Server &gt; &amp; lt; share &gt; ou &lt; Letter Drive &gt; : &amp; lt; Folder &gt; .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em>OSDSOURCEROOT</em></p></td>
<td align="left"><p><em>UNC</em></p>
<p>URL <em> http:// </em> ou <em> URL https://</em></p></td>
<td align="left"><p>Permite que um administrador especifique um local de origem para a recuperação de arquivo OSD para um pacote de aplicativo durante a publicação. As raízes de origem do OSD dão suporte a caminhos e URLs UNC (HTTP ou HTTPS). Se o valor for "", que é o valor padrão, as configurações de arquivo OSD existentes serão usadas.</p>
<p>Uma URL tem várias partes:</p>
<p>&lt;protocolo &gt; :// &lt; servidor &gt; : &lt; caminho da porta &gt; / &lt; &gt; / &lt; ? consulta &gt; &lt; #fragment&gt;</p>
<p>Um caminho UNC tem três partes:</p>
<p>&amp;lt; ComputerName; ComputerName &gt; &amp; ; Share Folder &gt; &amp; lt; Resource&gt;</p>
<div class="alert">
<strong>Importante</strong><br/><p>Certifique-se de usar o formato correto ao usar um caminho UNC. Os formatos aceitáveis são &amp; lt; Server &gt; &amp; lt; share &gt; ou &lt; Letter Drive &gt; : &amp; lt; Folder &gt; .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em>AUTOLOADONLOGIN</em></p>
<p><em>AUTOLOADONLAUNCH</em></p>
<p><em>AUTOLOADONREFRESH</em></p></td>
<td align="left"><p>[0 | 1]</p></td>
<td align="left"><p>Os gatilhos AutoLoad que definem os eventos que iniciam o carregamento automático de aplicativos. AutoLoad usa implicitamente o streaming em segundo plano para permitir que o aplicativo seja totalmente carregado no cache.</p>
<p>O bloco de recursos principal será carregado o mais rápido possível. Os blocos de recursos restantes serão carregados em segundo plano para permitir operações em primeiro plano, como interação do usuário com aplicativos, para ter prioridade e fornecer desempenho ideal.</p>
<div class="alert">
<strong>Observação</strong><br/><p>O <em> </em> parâmetro AUTOLOADTARGET determina quais aplicativos são carregados automaticamente. Por padrão, os pacotes que foram usados são carregados automaticamente, a menos que <em> AUTOLOADTARGET </em> esteja definido.</p>
</div>
<div>

</div>
<p>Cada parâmetro afeta o comportamento de carregamento da seguinte maneira:</p>
<ul>
<li><p><em>AUTOLOADONLOGIN </em> – o carregamento é iniciado quando o usuário faz logon.</p></li>
<li><p><em>AUTOLOADONLAUNCH </em> – o carregamento é iniciado quando o usuário inicia um aplicativo.</p></li>
<li><p><em>AUTOLOADONREFRESH </em> – o carregamento começa quando ocorre uma atualização de publicação.</p></li>
</ul>
<p>Os três valores podem ser combinados. No exemplo a seguir, os gatilhos de AutoLoad estão habilitados no momento da conexão do usuário e quando ocorre uma atualização de publicação:</p>
<p><em>AUTOLOADONLOGIN AUTOLOADONREFRESH</em></p>
<div class="alert">
<strong>Observação</strong><br/><p>Se o cliente estiver configurado com esses valores na primeira instalação, a função Autocarregar não será acionada até a próxima vez que o usuário fizer logoff e logon novamente.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em>AUTOLOADTARGET</em></p></td>
<td align="left"><p>NENHUMA</p>
<p>TODO</p>
<p>PREVUSED</p></td>
<td align="left"><p>Indica o que será carregado automaticamente quando um determinado disparador de autocarregamento ocorrer.</p>
<p>Valores possíveis:</p>
<ul>
<li><p>NONE — sem carregamento automático, independentemente de quais gatilhos podem ser definidos.</p></li>
<li><p>Tudo — se qualquer gatilho de autocarregamento estiver habilitado, todos os pacotes serão carregados automaticamente, independentemente de terem sido iniciados.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Essa configuração é definida para pacotes individuais usando o SFTMIME <strong> Adicionar pacote </strong> e <strong> Configurar comandos de pacote </strong> . Para obter mais informações sobre esses comandos, consulte <a href="sftmime--command-reference.md" data-raw-source="[SFTMIME Command Reference](sftmime--command-reference.md)"> referência de comandos SFTMIME </a> .</p>
</div>
<div>

</div></li>
<li><p>PREVUSED — se qualquer gatilho de AutoLoad estiver habilitado, carregue somente os pacotes nos quais pelo menos um aplicativo do pacote tenha sido usado anteriormente (ou seja, iniciado ou previamente armazenado em cache).</p></li>
</ul>
<div class="alert">
<strong>Observação</strong><br/><p>Ao instalar o cliente App-V para usar um cache somente leitura (por exemplo, como uma implementação de servidor VDI), você deve definir o <em> </em> parâmetro AUTOLOADTARGET como None para impedir que o cliente tente atualizar aplicativos no cache somente leitura.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em>DOTIMEOUTMINUTES</em></p></td>
<td align="left"><p>29600 (padrão)</p>
<p>1 – 1439998560 minutos (intervalo)</p></td>
<td align="left"><p>Indica quantos minutos um aplicativo pode ser usado em uma operação desconectada.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>INSTALLDIR</em></p></td>
<td align="left"><p>&lt;caminho&gt;</p></td>
<td align="left"><p>Especifica o diretório de instalação do cliente App-V.</p>
<p>Exemplo: INSTALLDIR = &quot; C:\Program Files\Microsoft Application Virtualization Client&quot;</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>Opti</em></p></td>
<td align="left"><p>VERDADEIRO</p>
<p>“”</p></td>
<td align="left"><p>Os componentes de cliente do Microsoft Application Virtualization serão atualizáveis por meio do Microsoft Update quando as atualizações forem disponibilizadas para o público em geral. O Microsoft Update Agent instalado em sistemas operacionais Windows exige que um usuário explicitamente opte por usar o serviço. Esse consentimento é necessário apenas uma vez para todos os aplicativos no dispositivo. Se você já tiver optado pelo Microsoft Update, os componentes do Microsoft Application Virtualization no dispositivo utilizarão automaticamente o serviço.</p>
<p>Para a instalação na linha de comando, o uso do Microsoft Update é, por padrão, recusado (a menos que um aplicativo anterior já tenha habilitado o dispositivo para ser incluído) devido ao requisito para a aceitação manual do Microsoft Update. Portanto, optar por não deve ser explícito para instalações de linha de comando. Definir o parâmetro de linha de comando <em> optid </em> como true força a aceitação da aceitação do Microsoft Update.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>REQUIREAUTHORIZATIONIFCACHED</em></p></td>
<td align="left"><p>TRUE</p>
<p>FALSE</p></td>
<td align="left"><p>Indica se a autorização é sempre necessária, se um aplicativo já está em cache.</p>
<p>Valores possíveis:</p>
<ul>
<li><p>TRUE — o aplicativo sempre deve ser autorizado na inicialização. Para aplicativos de fluxo RTSP, o token de autorização do usuário é enviado ao servidor para autorização. Para aplicativos baseados em arquivos, as ACLs de arquivo determinam se um usuário pode acessar o aplicativo.</p></li>
<li><p>FALSE — sempre tente se conectar ao servidor. Se não for possível estabelecer uma conexão com o servidor, o cliente ainda permite que o usuário inicie um aplicativo que tenha sido carregado anteriormente no cache.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWICACHESIZE</em></p></td>
<td align="left"><p>Tamanho do cache em MB</p></td>
<td align="left"><p>Especifica o tamanho em megabytes do cache do cliente. O tamanho padrão é de 4096 MB, e o tamanho máximo é 1.048.576 MB (1 TB). O sistema verifica o espaço disponível no momento da instalação, mas o espaço não é reservado.</p>
<p>Exemplo: <strong> SWICACHESIZE = &quot; 1024&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIPUBSVRDISPLAY</em></p></td>
<td align="left"><p>Nome de exibição</p></td>
<td align="left"><p>Especifica o nome exibido do servidor de publicação; obrigatório quando o <em> SWIPUBSVRHOST </em> é usado.</p>
<p>Exemplo: <strong> SWIPUBSVRDISPLAY = &quot; ambiente de produção&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIPUBSVRTYPE</em></p></td>
<td align="left"><p>[HTTP | RTSP</p></td>
<td align="left"><p>Especifica o tipo de servidor de publicação. O tipo de servidor padrão é o Application Virtualization Server. A <strong> </strong> opção/Secure não diferencia maiúsculas de minúsculas.</p>
<ul>
<li><p>HTTP – servidor HTTP padrão</p></li>
<li><p>HTTP <strong> /Secure </strong> — servidor http de segurança aprimorada</p></li>
<li><p>RTSP — servidor de virtualização de aplicativos</p></li>
<li><p>RTSP <strong> /Secure </strong> — servidor de virtualização do aplicativo de segurança aprimorado</p></li>
</ul>
<p>Exemplo: <strong> SWIPUBSVRTYPE = &quot; http/Secure&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIPUBSVRHOST</em></p></td>
<td align="left"><p>Endereço IP | nome do host</p></td>
<td align="left"><p>Especifica o endereço IP do servidor de virtualização de aplicativos ou um nome de host do servidor que é resolvido para o endereço IP&#39;s do servidor; obrigatório quando o <em> SWIPUBSVRDISPLAY </em> é usado.</p>
<p>Exemplo: <strong> SWIPUBSVRHOST = &quot; Server01&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIPUBSVRPORT</em></p></td>
<td align="left"><p>Número da porta</p></td>
<td align="left"><p>Especifica a porta lógica que é usada por este servidor de virtualização de aplicativos para ouvir solicitações do cliente (padrão = 554).</p>
<ul>
<li><p>Servidor HTTP padrão — padrão = 80.</p></li>
<li><p>Servidor HTTP de segurança aprimorada — padrão = 443.</p></li>
<li><p>Servidor de virtualização de aplicativos — padrão = 554.</p></li>
<li><p>Servidor avançado de virtualização do aplicativo de segurança — padrão = 322.</p></li>
</ul>
<p>Exemplo: <strong> SWIPUBSVRPORT = &quot; 443&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIPUBSVRPATH</em></p></td>
<td align="left"><p>Nome do caminho</p></td>
<td align="left"><p>Especifica o local no servidor de publicação do arquivo que define associações de tipo de arquivo (padrão =/); obrigatório quando o <em> </em> valor do parâmetro SWIPUBSVRTYPE é http.</p>
<p>Exemplo: <strong> SWIPUBSVRPATH = &quot; /APPVIRT/appsntypes.xml&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIPUBSVRREFRESH</em></p></td>
<td align="left"><p>[Ligado | REDONDA</p></td>
<td align="left"><p>Especifica se o cliente consulta automaticamente o servidor de publicação para aplicativos e associações de tipo de arquivo quando um usuário faz logon no cliente (padrão = ativado).</p>
<p>Exemplo: <strong> SWIPUBSVRREFRESH = &quot; desativado&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIGLOBALDATA</em></p></td>
<td align="left"><p>Diretório de dados globais</p></td>
<td align="left"><p>Especifica o diretório em que os dados serão armazenados que não são específicos de determinados usuários (padrão = C:\Documents and Settings\All Users\Documents).</p>
<p>Exemplo: <strong> SWIGLOBALDATA = &quot; D:\Microsoft Application Virtualization Client\Global&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIUSERDATA</em></p></td>
<td align="left"><p>Diretório de dados do usuário</p></td>
<td align="left"><p>Especifica o diretório onde os dados serão armazenados específicos a determinados usuários (padrão =% APPDATA%).</p>
<p>Exemplo: <strong> SWIUSERDATA = &quot; H:\Windows\Microsoft Application Virtualization Client&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIFSDRIVE</em></p></td>
<td align="left"><p>Letra de unidade preferida</p></td>
<td align="left"><p>Corresponde à letra da unidade selecionada para a unidade virtual.</p>
<p>Exemplo: <strong> SWIFSDRIVE = &quot; S&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SYSTEMEVENTLOGLEVEL</em></p></td>
<td align="left"><p>0 – 4</p></td>
<td align="left"><p>Indica o nível de log no qual as mensagens de log são gravadas no log de eventos do NT. O valor indica um limite do que é registrado, ou seja, tudo é igual a ou menor que o valor é registrado. Por exemplo, um valor de 0x3 (Warning) indica que avisos (0x3), erros (0x2) e erros críticos (0x1) são registrados.</p>
<p>Valores possíveis:</p>
<ul>
<li><p>0 = = nenhum</p></li>
<li><p>1 = = crítica</p></li>
<li><p>2 = = erro</p></li>
<li><p>3 = = aviso</p></li>
<li><p>4 = = informações</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em>MINFREESPACEMB</em></p></td>
<td align="left"><p>Em MB</p></td>
<td align="left"><p>Especifica a quantidade de espaço livre (em megabytes) que deve estar disponível no host antes que o tamanho do cache possa aumentar. O exemplo a seguir configuraria o cliente para garantir pelo menos 5 GB de espaço livre no disco antes de permitir que o tamanho do cache aumente. O padrão é 5000 MB de espaço livre disponível em disco no momento da instalação.</p>
<p>Exemplo: <strong> MINFREESPACEMB = &quot; 5000 &quot; (5 GB)</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>KEEPCURRENTSETTINGS</em></p></td>
<td align="left"><p>[0 | 1]</p></td>
<td align="left"><p>Usado quando você aplicou configurações do registro antes de implantar um cliente — por exemplo, usando a política de grupo. Quando um cliente é implantado, defina esse parâmetro como um valor de 1 para que ele não substitua as configurações do registro.</p>
<div class="alert">
<strong>Importante</strong><br/><p>Se definido com o valor 1, os seguintes parâmetros de linha de comando do instalador do cliente serão ignorados:</p>
<p><strong>SWICACHESIZE </strong> , <strong> MINFREESPACEMB </strong> , <strong> ALLOWINDEPENDENTFILESTREAMING </strong> , <strong> APPLICATIONSOURCEROOT </strong> , <strong> IconSourceRoot </strong> , <strong> OSDSourceRoot </strong> , <strong> SYSTEMEVENTLOGLEVEL </strong> , <strong> SWIGLOBALDATA </strong> , <strong> DOTIMEOUTMINUTES </strong> , <strong> SWIFSDRIVE </strong> , <strong> AUTOLOADTARGET </strong> , <strong> AUTOLOADTRIGGERS </strong> e <strong> SWIUSERDATA </strong> .</p>
<p>Para obter mais informações sobre como definir esses valores após a instalação, consulte "como definir as configurações do registro do cliente do App-V usando a linha de comando" no guia de operações do Application Virtualization (App-V) ( <a href="https://go.microsoft.com/fwlink/?LinkId=122939" data-raw-source="[https://go.microsoft.com/fwlink/?LinkId=122939](https://go.microsoft.com/fwlink/?LinkId=122939)"> https://go.microsoft.com/fwlink/?LinkId=122939 </a> ).</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Tópicos relacionados


[Como instalar manualmente o Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)

[Como fazer upgrade do Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)

[Referência de comando SFTMIME](sftmime--command-reference.md)









