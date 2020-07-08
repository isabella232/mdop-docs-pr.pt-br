---
title: Sobre a emissão de relatórios do App-V 5.0
description: Sobre a emissão de relatórios do App-V 5.0
author: dansimp
ms.assetid: 27c33dda-f017-41e3-8a78-1b681543ec4f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a29585886aa20233f49c85101cff570a098c69ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796642"
---
# Sobre a emissão de relatórios do App-V 5.0


O Microsoft Application Virtualization (App-V) 5,0 inclui um recurso de relatório interno que ajuda a coletar informações sobre computadores que executam o cliente App-V 5,0 e informações sobre o uso do pacote de aplicativos virtual. Você pode usar essas informações para gerar relatórios de um banco de dados centralizado.

## <a href="" id="---------app-v-5-0-reporting-overview"></a> Visão geral da emissão de relatórios do App-V 5,0


A lista a seguir exibe o fluxo de trabalho de alto nível final a fim para relatórios no App-V 5,0.

1.  O servidor de relatórios do Microsoft Application Virtualization (App-V) 5,0 tem os seguintes pré-requisitos:

    -   Função de servidor Web do serviço de informações da Internet (IIS)

    -   Função de autenticação do Windows (em **IIS/segurança**)

    -   SQL Server instalado e em execução com o SQL Server Reporting Services (SSRS)

    Para confirmar que o SQL Server Reporting Services está em execução, exiba `http://localhost/Reports` em um navegador da Web como administrador no servidor que hospedará relatórios do App-V 5,0. A home page do SQL Server Reporting Services deve ser exibida.

2.  Instale o servidor de relatórios do App-V 5,0 e o banco de dados associado. Para obter mais informações sobre como instalar o servidor de relatórios [, consulte Como instalar o servidor de relatórios em um computador autônomo e conectá-lo ao banco de dados](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md). Configure o tempo em que o computador executando o cliente App-V 5,0 deve enviar dados para o servidor de relatórios.

3.  Se você não estiver usando um sistema de distribuição de software eletrônico como o Configuration Manager para exibir relatórios, você pode definir relatórios no serviço de relatórios do SQL Server. Baixe os relatórios predefinidos do appvshort no centro de download em <https://go.microsoft.com/fwlink/?LinkId=397255> .

    **Observação**  Se você estiver usando a integração do Configuration Manager com o App-V 5,0, a maioria dos relatórios será gerada do Configuration Manager em vez do App-V 5,0.

     

4.  Após importar o módulo do PowerShell do App-V 5,0 usando `Import-Module AppvClient` o administrador, habilite o cliente App-v 5,0. Este cmdlet do PowerShell de exemplo habilita relatórios do App-V 5,0:

    ``` syntax
    Set-AppvClientConfiguration –reportingserverurl <url>:<port> -reportingenabled 1 – ReportingStartTime <0-23> - ReportingRandomDelay <#min>
    ```

    Para enviar imediatamente dados de relatório do App-V 5,0, execute `Send-AppvClientReport` no cliente do App-v 5,0.

    Para obter mais informações sobre como instalar o cliente do App-V 5,0 com relatório habilitado, consulte [sobre as configurações de cliente](about-client-configuration-settings.md). Para administrar relatórios do App-V 5,0 com o Windows PowerShell, consulte [como habilitar relatórios no cliente do App-v 5,0 usando o PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md).

5.  Depois que o servidor de relatório recebe os dados do cliente App-V 5,0, ele envia os dados para o banco de dados de relatórios. Quando o banco de dados recebe e processa os dados do cliente, uma resposta bem-sucedida é enviada ao servidor de relatórios e, em seguida, uma notificação é enviada ao cliente App-V 5,0.

6.  Quando o cliente do App-V 5,0 recebe a notificação de êxito, ele esvazia o cache de dados para conservar espaço.

    **Observação**  Por padrão, o cache é apagado depois que o servidor confirma o recebimento de dados. Você pode configurar manualmente o cliente para salvar o cache de dados.

     

~~~
If the App-V 5.0 client device does not receive a success notification from the server, it retains data in the cache and tries to resend data at the next configured interval. Clients continue to collect data and add it to the cache.
~~~

### <a href="" id="-------------app-v-5-0-reporting-server-frequently-asked-questions"></a> Perguntas frequentes sobre o aplicativo do App-V 5,0 Reporting Server

A tabela a seguir mostra as respostas a perguntas comuns sobre relatórios do App-V 5,0

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pergunta</th>
<th align="left">Mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Qual é a frequência com a qual as informações de relatório são enviadas para o banco de dados de relatórios?</p></td>
<td align="left"><p>A frequência depende de como a tarefa de relatório é configurada no computador que está executando o cliente App-V 5,0. Você deve configurar a frequência/intervalo para enviar os dados de relatório. O relatório do App-V 5,0 não é habilitado por padrão.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Quais informações são armazenadas no banco de dados do servidor de relatórios?</p></td>
<td align="left"><p>A lista a seguir exibe o que está armazenado no banco de dados de relatórios:</p>
<ul>
<li><p>O sistema operacional em execução no computador que está executando o cliente App-V 5,0: nome do host, versão, Service Pack, tipo-cliente/servidor, arquitetura do processador.</p></li>
<li><p>Informações sobre o cliente do App-V 5,0: versão.</p></li>
<li><p>Lista de pacotes publicados: GUID, GUID de versão, nome.</p></li>
<li><p>Informações de uso do aplicativo: nome, versão, servidor de streaming, usuário (DOMAIN\alias), GUID de versão do pacote, status e tempo de lançamento, hora de encerramento.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Qual é o volume médio de informações que são enviadas para o servidor de relatórios?</p></td>
<td align="left"><p>Isso depende. A lista a seguir exibe os três conjuntos de dados enviados para o servidor de relatórios:</p>
<ol>
<li><p>Informações do sistema operacional e do App-V 5,0 Client. aproximadamente 150 bytes, todas as vezes que os dados forem enviados.</p></li>
<li><p>Lista de pacotes publicados. aproximadamente 7 KB para 30 pacotes. Isso é enviado somente quando a lista de pacotes é atualizada com uma atualização de publicação, que é feita com pouca frequência; Se não houver nenhuma alteração, essas informações não serão enviadas.</p></li>
<li><p>Informações de uso do aplicativo virtual – cerca de 0,25 KB por evento. A função de abertura e fechamento de contagem como um evento se ambos ocorrerem antes de enviar as informações. Ao enviar usando uma tarefa agendada, somente os dados desde o último upload bem-sucedido são enviados ao servidor. Se enviar manualmente por meio do cmdlet do PowerShell, há um argumento opcional que controla se os dados precisam ser reenviados na próxima vez – esse argumento é <strong> DeleteOnSuccess </strong> .</p>
<p></p>
<p>Portanto, por exemplo, se vinte aplicativos forem abertos e fechados e se as informações de relatório estiverem agendadas para serem enviadas diariamente, o tráfego diário típico deve ser sobre 0.15 KB + 20 x 0,25 KB ou sobre 5KB/usuário</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>É possível agendar a emissão de relatórios?</p></td>
<td align="left"><p>Sim. Além de enviar manualmente relatórios usando cmdlets do PowerShell ( <strong> Send-AppvClientReport </strong> ), a tarefa pode ser agendada para que ela aconteça automaticamente. Há duas maneiras de agendar o relatório:</p>
<ol>
<li><p>Usando cmdlets do PowerShell- <strong> set-AppvClientConfiguration </strong> . Por exemplo:</p>
<p>Set-AppvClientConfiguration-ReportingEnabled 1-ReportingServerURL<a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</a></p>
<p></p>
<p>Para obter uma lista completa das definições de configuração do cliente <a href="about-client-configuration-settings.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings.md)"> , consulte sobre as configurações de cliente </a> e procure as seguintes entradas: <strong> ReportingEnabled </strong> , <strong> ReportingServerURL </strong> , <strong> ReportingDataCacheLimit </strong> , <strong> ReportingDataBlockSize </strong> , <strong> ReportingStartTime </strong> , <strong> ReportingRandomDelay </strong> , ReportingInterval <strong> </strong> .</p>
<p></p></li>
<li><p>Usando a política de grupo. Se for distribuído usando o controlador de domínio, as configurações serão iguais às listadas anteriormente.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Configurações de política de grupo substituir configurações locais definidas usando o PowerShell.</p>
</div>
<div>

</div></li>
</ol></td>
</tr>
</tbody>
</table>
 


## <a href="" id="---------app-v-5-0-client-reporting"></a> Relatório de cliente do App-V 5,0


Para usar os relatórios do App-V 5,0, você deve instalar e configurar o cliente App-V 5,0. Depois que o cliente tiver sido instalado, use o cmdlet **set-AppVClientConfiguration** do PowerShell ou o **modelo ADMX** para configurar o relatório. Os cmdlets do recurso de relatório estão disponíveis usando o link a seguir e são precedidas pela **geração de relatórios**. Para obter uma lista completa das configurações de cliente, consulte [sobre as definições de configuração do cliente](about-client-configuration-settings.md). A seção a seguir fornece exemplos da configuração de relatório do cliente do App-V 5,0 usando o PowerShell.

### Configurando relatórios do cliente App-V usando o PowerShell

Os exemplos a seguir mostram como os parâmetros do PowerShell podem configurar os recursos de relatório do cliente App-V 5,0.

**Observação**  
A tarefa de configuração a seguir também pode ser configurada usando configurações de política de grupo no modelo ADMX do App-V 5,0. Para obter mais informações sobre como usar o modelo ADMX, consulte [como modificar a configuração do cliente do App-V 5,0 usando o modelo ADMX e a política de grupo](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md).
 


**Para habilitar o relatório e iniciar a coleta de dados no computador que está executando o cliente App-V 5,0**:

`Set-AppVClientConfiguration –ReportingEnabled 1`

**Para configurar o cliente para enviar dados automaticamente para um servidor de relatórios específico**:

``` syntax
Set-AppVClientConfiguration –ReportingServerURL http://MyReportingServer:MyPort/ -ReportingStartTime 20 -ReportingInterval 1 -ReportingRandomDelay 30
```

`-ReportingInterval 1 -ReportingRandomDelay 30`

Este exemplo configura o cliente para enviar automaticamente os dados de relatório para a URL do servidor de relatórios <strong> http://MyReportingServer:MyPort/ </strong> . Além disso, os dados de relatório serão enviados diariamente entre o 8:00 e o 8:30 PM, dependendo do atraso aleatório gerado para a sessão.

**Para limitar o tamanho do cache de dados no cliente**:

`Set-AppvClientConfiguration –ReportingDataCacheLimit 100`

Configura o tamanho máximo do cache de relatórios no computador que está executando o cliente do App-V 5,0 para 100 MB. Se o limite do cache for atingido antes que os dados sejam enviados ao servidor, o log será regravado e os dados serão substituídos, conforme necessário.

**Para configurar o tamanho do bloco de dados transmitido na rede entre o cliente e o servidor**:

`Set-AppvClientConfiguration –ReportingDataBlockSize 10240`

Especifica o máximo de blocos de dados que o cliente envia para 10240 MB.

### Tipos de dados coletados

A tabela a seguir mostra os tipos de informações que você pode coletar usando os relatórios do App-V 5,0.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Informações do cliente</th>
<th align="left">Informações do pacote</th>
<th align="left">Uso do aplicativo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nome do host</p></td>
<td align="left"><p>Nome do pacote</p></td>
<td align="left"><p>Horários de início e término</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versão do cliente do App-V 5,0</p></td>
<td align="left"><p>Versão do pacote</p></td>
<td align="left"><p>Status da execução</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Arquitetura do processador</p></td>
<td align="left"><p>Origem do pacote</p></td>
<td align="left"><p>Estado de encerramento</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versão do sistema operacional</p></td>
<td align="left"><p>Porcentagem em cache</p></td>
<td align="left"><p>Nome do aplicativo</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nível do Service Pack</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Versão do aplicativo</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tipo de sistema operacional</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Nome de Usuário</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>Grupo de conexão</p></td>
</tr>
</tbody>
</table>
 


O cliente coleta e salva esses dados em um formato **. xml** . O cache de dados está oculto por padrão e requer direitos de administrador para abrir o arquivo XML.

### Enviar dados para o servidor

Você pode configurar o computador que está executando o cliente App-V 5,0 para enviar dados automaticamente para o servidor de relatórios especificado. Para especificar o servidor, use o cmdlet **set-AppvClientConfiguration** com as seguintes configurações:

-   ReportingEnabled

-   ReportingServerURL

-   ReportingStartTime

-   ReportingInterval

-   ReportingRandomDelay

Depois de definir as configurações anteriores, você deve criar uma tarefa agendada. A tarefa agendada vai entrar em contato com o servidor especificado pela configuração **ReportingServerURL** e iniciará a transferência. Se você quiser enviar dados manualmente para fora dos horários agendados, use o seguinte cmdlet do PowerShell:

`Send-AppVClientReport –URL http://MyReportingServer:MyPort/ -DeleteOnSuccess`

Se o servidor de relatório foi configurado anteriormente, o parâmetro **– URL** pode ser omitido. Como alternativa, se os dados devem ser enviados para um local alternativo, especifique uma URL diferente para substituir o **ReportingServerURL** configurado para essa coleta de dados.

O parâmetro **-DeleteOnSuccess** indica que, se a transferência for bem-sucedida, o cache de dados será limpo. Se não for especificado, o cache não será limpo.

### Coleta manual de dados

Você também pode usar o cmdlet **Send-AppVClientReport** para coletar dados manualmente. Esta solução é útil com ou sem um servidor de relatórios existente. A lista a seguir exibe informações sobre a coleta de dados com ou sem um servidor de relatórios.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Com um servidor de relatórios</th>
<th align="left">Sem um servidor de relatórios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Se você tiver um servidor de relatórios do App-V 5,0 existente, crie um script ou uma tarefa agendada personalizada. Especifique se o cliente envia os dados para o local especificado com a frequência desejada.</p></td>
<td align="left"><p>Se você não tiver um servidor de relatórios do App-V 5,0 existente, use o <strong> parâmetro – URL </strong> para enviar os dados para um compartilhamento especificado. Por exemplo:</p>
<p><code>Send-AppVClientReport –URL \Myshare\MyData\ -DeleteOnSuccess</code></p>
<p>O exemplo anterior enviará os dados de relatório para o <strong> &lt; local \MyShare\MyData/Strong &gt; indicado pelo <strong> parâmetro-URL </strong> . Depois que os dados forem enviados, o cache será limpo.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Se um local diferente do servidor de relatórios for especificado, os dados serão enviados usando o <strong> formato. XML </strong> sem processamento adicional.</p>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

### Criar relatórios

Para recuperar informações de relatório e criar relatórios usando o App-V 5,0, você deve usar um dos seguintes métodos:

-   **Microsoft SQL Server Reporting Services (SSRS)** -o Microsoft SQL Server Reporting Services está disponível com o Microsoft SQL Server. O SSRS não é instalado quando você instala o servidor de relatórios do App-V 5,0. Ele deve ser implantado separadamente para gerar os relatórios associados.

    Use o link a seguir para obter mais informações sobre como usar o [Microsoft SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596).

-   **Script** – você pode gerar relatórios diretamente em relação ao banco de dados de relatórios do App-V 5,0. Por exemplo:

    **Procedimento armazenado:**

    o **spProcessClientReport** está agendado para ser executado à meia-noite ou 12:00 am.

    Para executar o procedimento armazenado agendado do Microsoft SQL Server, o Microsoft SQL Server Agent deve estar em execução. Você deve certificar-se de que o Microsoft SQL Server Agent está definido como **AutoStart**. Para obter mais informações, consulte [AutoStart SQL Server Agent (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045).

    O procedimento armazenado também é criado ao usar os scripts de banco de dados do App-V 5,0.

Você também deve garantir que as **conexões simultâneas** do serviço Web do serviço Web do servidor de relatório sejam definidas com um valor que o servidor poderá gerenciar sem afetar a disponibilidade. O número recomendado de **conexões simultâneas máximas** para o **serviço Web de relatório** é **10.000**.






## Tópicos relacionados


[Implantação do servidor App-V 5.0](deploying-the-app-v-50-server.md)

[Como instalar o servidor de relatórios em um computador autônomo e conectá-lo ao banco de dados](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

 

 





