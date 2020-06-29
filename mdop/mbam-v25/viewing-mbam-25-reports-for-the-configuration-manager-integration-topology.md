---
title: Exibindo relatórios do MBAM 2.5 referentes à topologia de integração do Configuration Manager
description: Exibindo relatórios do MBAM 2.5 referentes à topologia de integração do Configuration Manager
author: dansimp
ms.assetid: 60d11b2f-3a76-4023-8da4-f89e9f35b790
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3384fee62d302ac47775fe106265456ef119ab47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799393"
---
# Exibindo relatórios do MBAM 2.5 referentes à topologia de integração do Configuration Manager


Este tópico descreve os relatórios que estão disponíveis quando você configura o Microsoft BitLocker Administration and Monitoring (MBAM) com a topologia de integração do Configuration Manager. Os relatórios mostram a compatibilidade do BitLocker para a empresa e para computadores e dispositivos individuais que o MBAM gerencia. Os relatórios fornecem gráficos e informações em tabelas, e eles têm filtros que permitem que você visualize dados de diferentes perspectivas.

Na topologia de integração do Configuration Manager, você vê relatórios do Configuration Manager em vez de usar o site de administração e monitoramento, com exceção do **relatório de auditoria de recuperação**, que você continua a exibir no site de administração e monitoramento.

Para obter informações sobre os relatórios do MBAM para a topologia autônoma, consulte [exibindo relatórios do MBAM 2,5 para a topologia](viewing-mbam-25-reports-for-the-stand-alone-topology.md)autônoma.

## Acessando relatórios no Configuration Manager


Para acessar o recurso relatórios no Configuration Manager:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versão do Configuration Manager</th>
<th align="left">Como exibir os relatórios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SystemCenter2012 ConfigurationManager</p></td>
<td align="left"><ol>
<li><p>No painel esquerdo, selecione o <strong> espaço de </strong> trabalho monitoramento.</p></li>
<li><p>Na árvore, expanda <strong> relatórios de relatório de visão geral </strong> &gt; <strong> </strong> &gt; <strong> </strong> &gt; <strong> MBAM </strong> .</p></li>
<li><p>Selecione a pasta que representa o idioma no qual você deseja exibir relatórios e, em seguida, selecione o relatório no painel à direita.</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>Configuration Manager 2007</p></td>
<td align="left"><ol>
<li><p>No painel esquerdo, expanda <strong> Gerenciamento do computador relatório do Reporting </strong> &gt; <strong> </strong> &gt; <strong> Services </strong> &gt; <strong> &lt; Server &gt; </strong> &gt; <strong> Folders </strong> &gt; <strong> MBAM </strong> .</p></li>
<li><p>Selecione a pasta que representa o idioma no qual você deseja exibir relatórios e, em seguida, selecione o relatório no painel à direita.</p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## Descrição dos relatórios no Configuration Manager


Há algumas diferenças mínimas nos relatórios da topologia de integração do Configuration Manager e da topologia autônoma. As seções a seguir descrevem os dados nos relatórios do MBAM para a topologia de integração do Configuration Manager:

-   [Painel de conformidade do BitLocker Enterprise](#bkmk-dashboard)

-   [Detalhes de conformidade corporativa do BitLocker](#bkmk-compliancedetails)

-   [Resumo de conformidade empresarial do BitLocker](#bkmk-compliancesummary)

-   [Relatório de conformidade do computador BitLocker](#bkmk-compliancereport)

### <a href="" id="bkmk-dashboard"></a>Painel de conformidade do BitLocker Enterprise

O painel de conformidade do BitLocker Enterprise fornece os seguintes gráficos, que mostram o status de compatibilidade do BitLocker na empresa:

-   Distribuição de status de conformidade

-   Distribuição de erros não conformes

-   Distribuição de status de conformidade por tipo de drive

**Distribuição de status de conformidade**

Este gráfico de pizza mostra o status de conformidade para computadores dentro da empresa. Ele também mostra a porcentagem de computadores, em comparação com o número total de computadores na coleção selecionada, que tem esse status de conformidade. O número real de computadores com cada status também é mostrado. O gráfico de pizza mostra os seguintes status de conformidade:

-   CLS

-   Não compatível

-   Isento de usuário

-   Isento de usuário temporário

-   Política não imposta

-   Sabe. Esses computadores relataram um erro de status ou fazem parte da coleção, mas nunca relataram o status da conformidade. A falta de um status de conformidade pode ocorrer se o computador estiver desconectado da organização.

**Distribuição de erros não conformes**

Este gráfico de pizza mostra as categorias de computadores na empresa que não são compatíveis com a política de criptografia de unidade de disco BitLocker e mostra o número de computadores em cada categoria. Cada porcentagem da categoria é calculada a partir do número total de computadores não compatíveis na coleção.

-   Criptografia adiada pelo usuário

-   Não é possível encontrar o TPM compatível

-   A partição do sistema não está disponível ou é grande o suficiente

-   Conflito de política

-   Aguardando o provisionamento automático do TPM

-   Ocorreu um erro desconhecido

-   Não há informações. Esses computadores não têm o cliente do MBAM instalado ou têm o cliente do MBAM instalado, mas não ativado (por exemplo, o serviço não está funcionando).

**Distribuição de status de conformidade por tipo de drive**

Este gráfico de barras mostra o status atual de conformidade do BitLocker por tipo de unidade. Os status são **compatíveis** e **não são compatíveis**. As barras são mostradas para unidades de dados fixas e unidades do sistema operacional. Os computadores que não têm uma unidade de dados fixa são incluídos e mostram um valor apenas na barra de **unidade do sistema operacional** . O gráfico não inclui os usuários que receberam isenção da política de criptografia de unidade de disco BitLocker ou nenhuma categoria de política.

### <a href="" id="bkmk-compliancedetails"></a>Detalhes de conformidade corporativa do BitLocker

Este relatório mostra informações sobre a conformidade total do BitLocker em toda a sua empresa para o conjunto de computadores direcionados para uso do BitLocker.

**Campos de detalhes de conformidade corporativa do BitLocker**

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
<td align="left"><p>Porcentagem de computadores com um estado de conformidade que não é conhecido.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% De isenção</p></td>
<td align="left"><p>Porcentagem de computadores isentos do requisito de criptografia do BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% Não isenta</p></td>
<td align="left"><p>Porcentagem de computadores que não estão isentos do requisito de criptografia do BitLocker.</p></td>
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
<td align="left"><p>Porcentagem de computadores com um estado de conformidade que não é conhecido.</p></td>
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

 

**Estados de detalhes de conformidade corporativa do BitLocker**

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

 

### <a href="" id="bkmk-compliancesummary"></a>Resumo de conformidade empresarial do BitLocker

Use esse tipo de relatório para mostrar informações sobre a conformidade geral do BitLocker em toda a sua empresa e para mostrar a conformidade para computadores individuais que estejam na coleção de computadores que são direcionados para uso do BitLocker.

**Campos Resumo de conformidade empresarial do BitLocker**

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
<td align="left"><p>Porcentagem de computadores com um estado de conformidade que não é conhecido.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% De isenção</p></td>
<td align="left"><p>Porcentagem de computadores isentos do requisito de criptografia do BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% Não isenta</p></td>
<td align="left"><p>Porcentagem de computadores que não estão isentos do requisito de criptografia do BitLocker.</p></td>
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
<td align="left"><p>Porcentagem de computadores com um estado de conformidade que não é conhecido.</p></td>
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

 

**Detalhes do computador de Resumo de conformidade corporativa do BitLocker**

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
<td align="left"><p>Mensagens de erro e status sobre o estado de conformidade do computador de acordo com a política especificada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Último contato</p></td>
<td align="left"><p>Data e hora em que o computador contatou o servidor pela última vez para informar o status de conformidade. A frequência do contato é configurável por meio das configurações da política de grupo.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancereport"></a>Relatório de conformidade do computador BitLocker

Use esse tipo de relatório para coletar informações específicas a um computador. O relatório de conformidade de computador BitLocker fornece informações de criptografia detalhadas sobre cada unidade em um computador (sistema operacional e unidades de dados fixas). Ele também fornece uma indicação da política aplicada a cada tipo de unidade no computador. Para ver os detalhes de cada unidade, expanda a entrada nome do computador.

**Observação**  O status da criptografia do volume de dados removível não é mostrado neste relatório.

 

**Relatório de conformidade do computador BitLocker: campos de detalhes do computador**

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
<td align="left"><p>Status geral de conformidade do computador gerenciado pela MBAM. Os Estados válidos são compatíveis e não são compatíveis. Observe que o status de conformidade por unidade (veja a tabela a seguir) pode indicar estados de conformidade diferentes. No entanto, esse campo representa o estado de conformidade de acordo com a política especificada.</p></td>
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
<td align="left"><p>Data e hora em que o computador contatou o servidor pela última vez para informar o status de conformidade. A frequência do contato é configurável por meio das configurações da política de grupo.</p></td>
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
<td align="left"><p>Mensagens de erro e status sobre o estado de conformidade do computador de acordo com a política especificada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nível de codificação da política</p></td>
<td align="left"><p>O nível de codificação selecionado pelo administrador durante a especificação da política MBAM (por exemplo, 128-bit com difusor).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Política: unidade do sistema operacional</p></td>
<td align="left"><p>Indica se a criptografia é necessária para o sistema operacional e o tipo de protetor apropriado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Política: unidade de dados fixa</p></td>
<td align="left"><p>Indica se a criptografia é necessária para a unidade de dados fixo.</p></td>
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

 

**Relatório de conformidade do computador BitLocker: campos de volume do computador**

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
<td align="left"><p>Tipo de protetor selecionado por meio da política usada para criptografar um sistema operacional ou unidade de dados fixa. Os tipos de protetor válidos para um sistema operacional são TPM ou TPM + PIN. O tipo de protetor válido para uma unidade de dados fixa é uma senha.</p></td>
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


[Monitorando e gerando relatórios de conformidade do BitLocker com o MBAM 2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

 

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





