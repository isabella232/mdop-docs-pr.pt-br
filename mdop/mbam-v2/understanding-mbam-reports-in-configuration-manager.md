---
title: Noções básicas sobre relatórios do MBAM no Configuration Manager
description: Noções básicas sobre relatórios do MBAM no Configuration Manager
author: dansimp
ms.assetid: b2582190-c9de-4e64-bd5a-f31ac1916f53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 995d628cafd03c8bdd209e467c9d22169b7e03c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799349"
---
# Noções básicas sobre relatórios do MBAM no Configuration Manager


Quando a administração e o monitoramento do Microsoft BitLocker (MBAM) são instalados com a topologia integrada do Configuration Manager, os recursos de relatórios e conformidade de hardware são movidos para a infraestrutura do Configuration Manager e de MBAM. Ao usar a topologia do Configuration Manager, você executa relatórios do Configuration Manager em vez de MBAM, exceto para o relatório de auditoria de recuperação, que você continua a acessar usando o site de administração e monitoramento.

Os relatórios da topologia integrada do Configuration Manager mostram a compatibilidade do BitLocker para a empresa e para computadores e dispositivos individuais que o MBAM gerencia. Os relatórios fornecem gráficos e informações em tabelas, e permitem filtrar relatórios para exibir dados de diferentes perspectivas.

As informações neste tópico descrevem os relatórios do MBAM executados a partir do Configuration Manager. Para obter informações sobre os relatórios do MBAM para a topologia autônoma, consulte [noções básicas sobre relatórios do MBAM](understanding-mbam-reports-mbam-2.md).

## Acessando relatórios no Configuration Manager


Para acessar o recurso relatórios no Configuration Manager, abra o **console do Configuration Manager**. Para exibir a lista de relatórios disponíveis:

-   No Configuration Manager 2007, expanda o nó **Gerenciamento do computador** e, em seguida, expanda o nó **relatório** .

-   No SystemCenter2012 ConfigurationManager, no espaço de trabalho monitoramento em **visão geral**, expanda o nó **relatório** e clique em **relatórios**.

### Painel de conformidade do BitLocker Enterprise

O painel de conformidade do BitLocker Enterprise fornece os seguintes gráficos, que mostram o status de compatibilidade do BitLocker na empresa:

-   Distribuição de status de conformidade

-   Distribuição de erros não conformes

-   Distribuição de status de conformidade por tipo de drive

**Distribuição de status de conformidade**

Este gráfico de pizza mostra status de conformidade do computador dentro da empresa e mostra a porcentagem de computadores, em comparação com o número total de computadores na coleção selecionada, que tem esse status de conformidade. O número real de computadores com cada status também é mostrado. O gráfico de pizza mostra os seguintes status de conformidade:

-   CLS

-   Não compatível

-   Isento de usuário

-   Isento de usuário temporário

-   Política não imposta

-   Desconhecido – computadores cujo status foi reportado como um erro, ou dispositivos que fazem parte da coleção, mas nunca relataram o status da conformidade, por exemplo, se estiverem desconectados da organização

**Distribuição de erros não conformes**

Este gráfico de pizza mostra as categorias de computadores na empresa que não são compatíveis com a política de criptografia de unidade de disco BitLocker e mostra o número de computadores em cada categoria. Cada porcentagem da categoria é calculada a partir do número total de computadores não compatíveis na coleção.

-   Criptografia adiada pelo usuário

-   Não é possível encontrar o TPM compatível

-   A partição do sistema não está disponível ou é grande o suficiente

-   Conflito de política

-   Aguardando o provisionamento automático do TPM

-   Ocorreu um erro desconhecido

-   Nenhuma informação – computadores que não têm o cliente do MBAM instalado, ou que têm o cliente MBAM instalado, mas não foram ativados, por exemplo, o serviço não está funcionando

**Distribuição de status de conformidade por tipo de drive**

Este gráfico de barras mostra o status atual de conformidade do BitLocker por tipo de unidade. Os status são "compatíveis" e "não compatíveis". As barras são mostradas para unidades de dados fixas e unidades do sistema operacional. Os computadores que não têm uma unidade de dados fixa são incluídos e mostram um valor apenas na barra de unidade do sistema operacional. O gráfico não inclui os usuários que receberam isenção da política de criptografia de unidade de disco BitLocker ou da categoria "sem política".

### Relatório de detalhes de conformidade corporativa do BitLocker

Este relatório mostra informações sobre a conformidade total do BitLocker em toda a sua empresa para o conjunto de computadores direcionados para uso do BitLocker.

**Campos de relatório de detalhes de conformidade corporativa do BitLocker**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da coluna</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Computadores gerenciados</p></td>
<td align="left"><p>Número de computadores que o MBAM gerencia.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% Compatível</p></td>
<td align="left"><p>Porcentagem de computadores compatíveis na empresa.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% Não compatível</p></td>
<td align="left"><p>Porcentagem de computadores não compatíveis na empresa.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% De conformidade desconhecida</p></td>
<td align="left"><p>Porcentagem de computadores cujo estado de conformidade não é conhecido.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% De isenção</p></td>
<td align="left"><p>Porcentagem de computadores isentos do requisito de criptografia do BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% Não isenta</p></td>
<td align="left"><p>Porcentagem de computadores isentos do requisito de criptografia do BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CLS</p></td>
<td align="left"><p>Porcentagem de computadores compatíveis na empresa.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Não compatível</p></td>
<td align="left"><p>Porcentagem de computadores não compatíveis na empresa.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformidade desconhecida</p></td>
<td align="left"><p>Porcentagem de computadores cujo estado de conformidade não é conhecido.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Isentos</p></td>
<td align="left"><p>Total de computadores isentos do requisito de criptografia do BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Não isento</p></td>
<td align="left"><p>Total de computadores que não estão isentos do requisito de criptografia do BitLocker.</p></td>
</tr>
</tbody>
</table>

 

**Relatório de detalhes de conformidade corporativa do BitLocker-Estados de conformidade**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Status de conformidade</th>
<th align="left">Isenção</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Não compatível</p></td>
<td align="left"><p>Não isento</p></td>
<td align="left"><p>O computador não é compatível, de acordo com a política especificada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>CLS</p></td>
<td align="left"><p>Não isento</p></td>
<td align="left"><p>O computador é compatível de acordo com a política especificada.</p></td>
</tr>
</tbody>
</table>

 

### Relatório de Resumo de conformidade empresarial do BitLocker

Use esse tipo de relatório para mostrar informações sobre a conformidade geral do BitLocker em toda a sua empresa e para mostrar a conformidade para computadores individuais que estejam na coleção de computadores que são direcionados para uso do BitLocker.

**Campos relatório de Resumo de conformidade empresarial do BitLocker**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da coluna</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Computadores gerenciados</p></td>
<td align="left"><p>Número de computadores que o MBAM gerencia.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% Compatível</p></td>
<td align="left"><p>Porcentagem de computadores compatíveis na empresa.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% Não compatível</p></td>
<td align="left"><p>Porcentagem de computadores não compatíveis na empresa.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% De conformidade desconhecida</p></td>
<td align="left"><p>Porcentagem de computadores cujo estado de conformidade não é conhecido.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% De isenção</p></td>
<td align="left"><p>Porcentagem de computadores isentos do requisito de criptografia do BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% Não isenta</p></td>
<td align="left"><p>Porcentagem de computadores isentos do requisito de criptografia do BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CLS</p></td>
<td align="left"><p>Porcentagem de computadores compatíveis na empresa.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Não compatível</p></td>
<td align="left"><p>Porcentagem de computadores não compatíveis na empresa.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformidade desconhecida</p></td>
<td align="left"><p>Porcentagem de computadores cujo estado de conformidade não é conhecido.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Isentos</p></td>
<td align="left"><p>Total de computadores isentos do requisito de criptografia do BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Não isento</p></td>
<td align="left"><p>Total de computadores que não estão isentos do requisito de criptografia do BitLocker.</p></td>
</tr>
</tbody>
</table>

 

**Relatório de Resumo de conformidade empresarial do BitLocker-detalhes do computador**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da coluna</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nome do computador</p></td>
<td align="left"><p>Nome do computador DNS especificado pelo usuário que está sendo gerenciado pelo MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome de domínio</p></td>
<td align="left"><p>Nome de domínio totalmente qualificado, em que o computador cliente reside e é gerenciado pelo MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Status de conformidade</p></td>
<td align="left"><p>Status geral de conformidade do computador gerenciado pela MBAM. Os Estados válidos são compatíveis e não são compatíveis. Observe que o status de conformidade por unidade (veja a tabela a seguir) pode indicar estados de conformidade diferentes. No entanto, esse campo representa o estado de conformidade, de acordo com a política especificada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Isenção</p></td>
<td align="left"><p>Status que indica se o usuário está isento ou não isento da política BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuários do dispositivo</p></td>
<td align="left"><p>Usuário do dispositivo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Detalhes do status de conformidade</p></td>
<td align="left"><p>Mensagens de erro e status do estado de conformidade do computador de acordo com a política especificada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Último contato</p></td>
<td align="left"><p>Data e hora em que o computador contatou o servidor pela última vez para informar o status de conformidade. A frequência do contato é configurável (consulte Configurações de política de MBAM).</p></td>
</tr>
</tbody>
</table>

 

### Relatório de conformidade do computador BitLocker

Use esse tipo de relatório para coletar informações específicas a um computador. O relatório de conformidade do computador fornece informações de criptografia detalhadas sobre cada unidade (sistema operacional e unidades de dados fixas) em um computador, além de uma indicação da política aplicada a cada tipo de unidade no computador. Para ver os detalhes de cada unidade, expanda a entrada nome do computador.

**Observação**  O status da criptografia do volume de dados removível não é mostrado no relatório.

 

**Relatório de conformidade do computador BitLocker – campos de detalhes do computador**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da coluna</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nome do computador</p></td>
<td align="left"><p>Nome do computador DNS especificado pelo usuário que está sendo gerenciado pelo MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome de domínio</p></td>
<td align="left"><p>Nome de domínio totalmente qualificado, em que o computador cliente reside e é gerenciado pelo MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tipo de computador</p></td>
<td align="left"><p>Tipo de computador. Tipos válidos são não portáteis e portáteis.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sistema operacional</p></td>
<td align="left"><p>Tipo de sistema operacional encontrado no computador cliente gerenciado MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformidade geral</p></td>
<td align="left"><p>Status geral de conformidade do computador gerenciado pela MBAM. Os Estados válidos são compatíveis e não são compatíveis. Observe que o status de conformidade por unidade (veja a tabela a seguir) pode indicar estados de conformidade diferentes. No entanto, esse campo representa o estado de conformidade, de acordo com a política especificada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Conformidade com o sistema operacional</p></td>
<td align="left"><p>Status de conformidade do sistema operacional que é gerenciado pelo MBAM. Os Estados válidos são compatíveis e não são compatíveis.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformidade de unidade de dados fixa</p></td>
<td align="left"><p>Status de conformidade da unidade de dados fixa gerenciada pela MBAM. Os Estados válidos são compatíveis e não são compatíveis.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Data da última atualização</p></td>
<td align="left"><p>Data e hora em que o computador contatou o servidor pela última vez para informar o status de conformidade. A frequência do contato é configurável (consulte Configurações de política de MBAM).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Isenção</p></td>
<td align="left"><p>Status que indica se o usuário está isento ou não isento da política BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuário isento</p></td>
<td align="left"><p>Usuário que está isento da política BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Data de isenção</p></td>
<td align="left"><p>Data em que a isenção foi concedida.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Detalhes do status de conformidade</p></td>
<td align="left"><p>Mensagens de erro e status do estado de conformidade do computador de acordo com a política especificada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nível de codificação da política</p></td>
<td align="left"><p>Nível de codificação selecionado pelo administrador durante a especificação da política MBAM. (por exemplo, 128-bit com difusor).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Política: unidade do sistema operacional</p></td>
<td align="left"><p>Indica se a criptografia é necessária para o o/S e o tipo de protetor apropriado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Política: unidade de dados fixa</p></td>
<td align="left"><p>Indica se a criptografia é necessária para a unidade fixa.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Fabricante</p></td>
<td align="left"><p>Nome do fabricante do computador, como aparece no BIOS do computador.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modelo</p></td>
<td align="left"><p>Nome do modelo do fabricante do computador, como aparece no BIOS do computador.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuários do dispositivo</p></td>
<td align="left"><p>Usuários conhecidos no computador que está sendo gerenciado pelo MBAM.</p></td>
</tr>
</tbody>
</table>

 

**Relatório de conformidade do computador BitLocker – campos volume do computador**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da coluna</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Letra da unidade</p></td>
<td align="left"><p>Letra da unidade do computador que foi atribuída à unidade específica pelo usuário.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tipo de unidade</p></td>
<td align="left"><p>Tipo de unidade. Os valores válidos são unidade do sistema operacional e unidade de dados fixa. Esses são drives físicos, em vez de volumes lógicos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nível de codificação</p></td>
<td align="left"><p>Nível de codificação selecionado pelo administrador durante a especificação da política MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tipos de protetor</p></td>
<td align="left"><p>Tipo de protetor selecionado pela política usada para criptografar um sistema operacional ou volume fixo. Os tipos de protetor válidos em um sistema operacional são TPM ou TPM + PIN e para um volume de dados fixo é senha.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Estado do protetor</p></td>
<td align="left"><p>Indica que o computador que está sendo gerenciado pelo MBAM ativou o tipo de protetor especificado na política. Os Estados válidos estão ATIVAdos ou desativados.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Estado de criptografia</p></td>
<td align="left"><p>Estado de criptografia da unidade. Os Estados válidos são criptografados, não criptografados e criptografados.</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Usando o MBAM com o Configuration Manager](using-mbam-with-configuration-manager.md)

 

 





