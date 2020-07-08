---
title: Como gerar relatórios
description: Como gerar relatórios
author: dansimp
ms.assetid: 9f8ba28e-1993-4c11-a28a-493718051e5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 930b7061d3e5e2fb9951d45b1422915836cbc00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799983"
---
# Como gerar relatórios


Os seguintes tipos de relatório podem ser criados por administradores no MED-V:

-   [Status](#bkmk-generatingastatusreport)— use o relatório de status para analisar o status atual de todos os usuários ativos e todos os espaços de trabalho do MED-V de cada usuário com base em um período de tempo definido. Isso inclui a visualização de computadores que estão conectados ao servidor ou, se não estiverem conectados no momento, a data e a hora da última vez em que foram conectados ao servidor, o status de cada computador e outras informações relevantes.

-   [Log de atividades](#bkmk-generatinganactivitylogreport)— Use este relatório para revisar os eventos originados de um host ou usuário específico em um intervalo de datas definido.

-   [Log de erros](#bkmk-generatinganerrorlogreport)— Use este relatório para exibir os erros originados de um host ou usuário específico em um intervalo de datas definido.

Os resultados do relatório podem ser classificados por qualquer coluna clicando no nome da coluna apropriada.

Os resultados do relatório podem ser agrupados arrastando-se um cabeçalho de coluna para a parte superior do relatório. Arraste vários cabeçalhos de coluna para agrupar uma coluna após a outra.

## <a href="" id="bkmk-generatingastatusreport"></a>Como gerar um relatório de status


**Para gerar um relatório de status**

1.  Clique no botão gerenciamento de **relatórios** .

2.  No módulo **relatórios** , no menu **tipos de relatório** , selecione **status**e clique em **gerar**.

    A caixa de diálogo parâmetros do relatório é exibida.

3.  Na caixa de diálogo **parâmetros do relatório** , no campo **número de dias** , insira um número ou use as setas para selecionar o número de dias a serem incluídos no relatório de status e clique em **OK**.

    Um relatório de status é gerado. Os parâmetros de relatório são definidos na tabela a seguir.

**Propriedades do espaço de trabalho MED-V do cliente**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriedade</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tempo</p></td>
<td align="left"><p>A data e a hora em que o evento ocorreu.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Por padrão, os eventos são exibidos em ordem decrescente de data. No entanto, é possível alterá-lo clicando na coluna tempo recebido.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Nome do usuário</p></td>
<td align="left"><p>O usuário que iniciou o evento.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Se o evento ocorreu antes de um usuário se conectar, o nome do usuário será SYSTEM.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome do host</p></td>
<td align="left"><p>O nome do computador host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome do espaço de trabalho</p></td>
<td align="left"><p>O nome do espaço de trabalho do MED-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome do computador do espaço de trabalho</p></td>
<td align="left"><p>O nome do computador no qual o espaço de trabalho do MED-V está em execução.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Online</p></td>
<td align="left"><p>O estado atual do computador cliente:</p>
<ul>
<li><p><strong>Terminou</strong></p></li>
<li><p><strong>Iniciado na &lt; data e hora em que o espaço de trabalho foi iniciado&gt;</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Versão do cliente</p></td>
<td align="left"><p>O número da versão do cliente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versão da política</p></td>
<td align="left"><p>A versão de política que o espaço de trabalho do MED-V está usando no momento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome da imagem</p></td>
<td align="left"><p>O nome da imagem.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versão da imagem</p></td>
<td align="left"><p>A versão de imagem que o espaço de trabalho do MED-V está usando no momento.</p>
<div class="alert">
<strong>Observação</strong><br/><p>A versão do espaço de trabalho do MED-V pode ser desconhecida se ainda não tiver sido baixada em um computador.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganactivitylogreport"></a>Como gerar um relatório de log de atividades


**Para gerar um relatório de log de atividades**

1.  Clique no botão gerenciamento de **relatórios** .

    O módulo relatórios é exibido.

2.  No módulo **relatórios** , no menu **tipos de relatório** , selecione **registro de atividades**e clique em **gerar**.

3.  Na caixa de diálogo **parâmetros de relatório** , configure um ou mais dos seguintes parâmetros:

    -   **Número de dias**— o número de dias a serem exibidos no relatório.

    -   O **nome de usuário contém**— qualquer evento no qual o nome de usuário contém o texto inserido está incluído no relatório.

    -   O **nome do host contém**— qualquer evento em que o nome do host contém o texto inserido está incluído no relatório.

4.  Clique em **OK**.

    Um relatório é gerado com os eventos e as datas selecionadas. Os parâmetros de relatório são definidos na tabela a seguir.

**Propriedades do relatório do log de atividades**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriedade</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ID do evento</p></td>
<td align="left"><p>A ID do evento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gravidade</p></td>
<td align="left"><p><strong>Informações, erro, aviso</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Categoria</p></td>
<td align="left"><p>O módulo ao qual o relatório se refere.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descrição</p></td>
<td align="left"><p>Uma descrição do evento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Hora de recebimento</p></td>
<td align="left"><p>A data e a hora em que o evento foi recebido no servidor.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Se o cliente estiver trabalhando offline, o servidor receberá os relatórios quando o cliente estiver online.</p>
</div>
<div>

</div>
<div class="alert">
<strong>Observação</strong><br/><p>Por padrão, os eventos são exibidos em ordem decrescente de data. No entanto, é possível alterá-lo clicando na <strong> coluna tempo recebido </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Tempo do cliente</p></td>
<td align="left"><p>A data e a hora em que o evento ocorreu de acordo com o relógio do cliente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome do host</p></td>
<td align="left"><p>O nome do computador host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome do usuário</p></td>
<td align="left"><p>O usuário que iniciou o evento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome do espaço de trabalho</p></td>
<td align="left"><p>O nome do espaço de trabalho do MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome do computador do espaço de trabalho</p></td>
<td align="left"><p>O nome do computador no qual o espaço de trabalho do MED-V está em execução.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganerrorlogreport"></a>Como gerar um relatório de log de erros


**Para gerar um relatório de log de erros**

1.  Clique no botão gerenciamento de **relatórios** .

2.  No módulo **relatórios** , no menu **tipos de relatório** , selecione **log de erros**e clique em **gerar**.

3.  Na caixa de diálogo **parâmetros de relatório** , configure um ou mais dos seguintes parâmetros:

    -   **Número de dias**— o número de dias a serem exibidos no relatório.

    -   O **nome de usuário contém**— qualquer evento no qual o nome de usuário contém o texto inserido está incluído no relatório.

    -   O **nome do host contém**— qualquer evento em que o nome do host contém o texto inserido está incluído no relatório.

4.  Clique em **OK**.

    Um relatório é gerado com os eventos e as datas selecionadas. Os parâmetros de relatório são definidos na tabela a seguir.

**Propriedades do relatório de log de erros**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriedade</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ID do evento</p></td>
<td align="left"><p>A ID do evento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Categoria</p></td>
<td align="left"><p>O módulo ao qual o relatório se refere.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Descrição</p></td>
<td align="left"><p>Uma descrição do evento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Hora de recebimento</p></td>
<td align="left"><p>A data e a hora em que o evento foi recebido no servidor.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Se o cliente estiver trabalhando offline, o servidor receberá os relatórios quando o cliente estiver online.</p>
</div>
<div>

</div>
<div class="alert">
<strong>Observação</strong><br/><p>Por padrão, os eventos são exibidos em ordem decrescente de data. No entanto, é possível alterá-lo clicando na <strong> coluna tempo recebido </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Tempo do cliente</p></td>
<td align="left"><p>A data e a hora em que o evento ocorreu de acordo com o relógio do cliente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome do host</p></td>
<td align="left"><p>O nome do computador host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome do usuário</p></td>
<td align="left"><p>O usuário que iniciou o evento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome do espaço de trabalho</p></td>
<td align="left"><p>O nome do espaço de trabalho do MED-V.</p></td>
</tr>
</tbody>
</table>











