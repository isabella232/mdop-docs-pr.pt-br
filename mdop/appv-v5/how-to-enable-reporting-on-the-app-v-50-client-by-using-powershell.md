---
title: Como habilitar relatórios no cliente do App-V 5.0 usando o PowerShell
description: Como habilitar relatórios no cliente do App-V 5.0 usando o PowerShell
author: dansimp
ms.assetid: a7aaf553-0f83-4cd0-8df8-93a5f1ebe497
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c004b4900a9814a11cb2706659a2edb99de6cc1b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796412"
---
# Como habilitar relatórios no cliente do App-V 5.0 usando o PowerShell


Use o procedimento a seguir para configurar o App-V 5,0 para relatórios.

**Para configurar o computador que executa o cliente App-V 5,0 para relatórios**

1. Instale o cliente App-V 5,0. Para obter mais informações sobre como instalar o cliente [, consulte como implantar o cliente App-V](how-to-deploy-the-app-v-client-gb18030.md).

2. Depois de instalar o cliente App-V 5,0, use o PowerShell **set-AppvClientConfiguration** para configurar as definições de configuração de relatórios adequadas:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Configuração</th>
   <th align="left">Descrição</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>ReportingEnabled</p></td>
   <td align="left"><p>Permite que o cliente retorne informações para um servidor de relatórios. Essa configuração é necessária para que o cliente colete os dados de relatório no cliente.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReportingServerURL</p></td>
   <td align="left"><p>Especifica o local no servidor de relatório onde as informações do cliente são salvas. Por exemplo, http:// &lt; reportingservername &gt; : &lt; reportingportnumber &gt; .</p>
   <div class="alert">
   <strong>Observação</strong><br/><p>Este é o número da porta que foi atribuído durante a configuração do servidor de relatório</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Hora de início do relatório</p></td>
   <td align="left"><p>Isso é definido para agendar o cliente para enviar os dados automaticamente para o servidor. Essa configuração indicará a hora em que os dados de relatório começarão a enviar. Ele está no formato de 24 horas e aceitará um número entre o 0-23.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReportingRandomDelay</p></td>
   <td align="left"><p>Especifica o atraso máximo (em minutos) dos dados a serem enviados para o servidor de relatórios. Quando a tarefa agendada for iniciada, o cliente gerará um atraso aleatório entre 0 e ReportingRandomDelay e esperará a duração especificada antes de enviar os dados.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ReportingInterval</p></td>
   <td align="left"><p>Especifica o intervalo de repetição que o cliente usará para reenviar dados ao servidor de relatórios.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReportingDataCacheLimit</p></td>
   <td align="left"><p>Especifica o tamanho máximo em megabytes (MB) do cache XML para armazenar informações de relatório. O tamanho se aplica ao cache na memória. Quando o limite for atingido, o arquivo de log será revertido.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ReportingDataBlockSize</p></td>
   <td align="left"><p>Especifica o tamanho máximo em megabytes (MB) do cache XML para armazenar informações de relatório. O tamanho se aplica ao cache na memória. Quando o limite for atingido, o arquivo de log será revertido.</p></td>
   </tr>
   </tbody>
   </table>



3. Após a configuração das configurações apropriadas, o computador que executa o cliente App-V 5,0 coletará dados automaticamente e enviará os dados de volta para o servidor de relatórios.

   Além disso, os administradores podem enviar manualmente os dados de volta de uma maneira sob demanda usando o cmdlet do PowerShell **Send-AppvClientReport** .

   **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Administração do App-V usando o PowerShell](administering-app-v-by-using-powershell.md)









