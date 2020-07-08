---
title: Noções básicas sobre relatórios autônomos do MBAM 2.5
description: Noções básicas sobre relatórios autônomos do MBAM 2.5
author: dansimp
ms.assetid: 78b5aaf4-8257-4722-8eb9-e0de48db6a11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45e84c7c3b2bcb1602890c7c5a09592324da691e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796084"
---
# Noções básicas sobre relatórios autônomos do MBAM 2.5


Este tópico descreve os relatórios que estão disponíveis quando você está executando o Microsoft BitLocker Administration and Monitoring (MBAM) na topologia autônoma.

**Observação**  
Se você estiver executando o MBAM com a topologia de integração do Configuration Manager, gere relatórios do Configuration Manager em vez de MBAM. Consulte [exibindo relatórios do MBAM 2,5 para a topologia de integração do Configuration Manager](viewing-mbam-25-reports-for-the-configuration-manager-integration-topology.md) para obter mais informações sobre esses relatórios.



## Compreendendo os relatórios de topologia autônomo do MBAM


O MBAM fornece três tipos de relatório que você pode usar para monitorar a conformidade do BitLocker com a sua organização:

-   [Relatório de conformidade empresarial](#bkmk-enterprisecompliance)

-   [Relatório de conformidade do computador](#bkmk-compliance)

-   [Relatório de auditoria de recuperação](#bkmk-recovery)

Para acessar relatórios do MBAM quando você estiver executando o MBAM na topologia autônoma, abra um navegador da Web e, em seguida, abra o site Administração e monitoramento. Selecione **relatórios** na barra de menus à esquerda. Na barra de menus superior, selecione o tipo de relatório que você deseja gerar. Para obter mais informações sobre como gerar esses relatórios, consulte [gerando relatórios autônomos do MBAM 2,5](generating-mbam-25-stand-alone-reports.md).

### <a href="" id="bkmk-enterprisecompliance"></a>Relatório de conformidade empresarial

Use esse tipo de relatório para coletar informações sobre a conformidade geral do BitLocker em sua organização. Você pode usar filtros para restringir os resultados da pesquisa para saber mais sobre o estado de conformidade e o status de erro dos computadores em sua organização.

**Visão geral da conformidade corporativa**

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
<td align="left"><p>% De isenção</p></td>
<td align="left"><p>Porcentagem de computadores isentos do requisito de criptografia do BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% Não isenta</p></td>
<td align="left"><p>Porcentagem de computadores que não estão isentos do requisito de criptografia do BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>CLS</p></td>
<td align="left"><p>Porcentagem de computadores compatíveis na empresa.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Não compatível</p></td>
<td align="left"><p>Porcentagem de computadores não compatíveis na empresa.</p></td>
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



**Detalhes do computador de conformidade empresarial**

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
<td align="left"><p>Nome DNS especificado pelo usuário que é gerenciado pelo MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome de domínio</p></td>
<td align="left"><p>Nome de domínio totalmente qualificado em que o computador cliente reside e é gerenciado pelo MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Status de conformidade</p></td>
<td align="left"><p>Estado de conformidade do computador, de acordo com a política especificada para o computador. Os Estados são compatíveis e não são compatíveis. Consulte a tabela Estados de conformidade de relatório de conformidade empresarial a seguir para obter mais informações sobre como interpretar Estados de conformidade.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Isenção</p></td>
<td align="left"><p>Status que indica se este computador está isento da política BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Detalhes do status de conformidade</p></td>
<td align="left"><p>Mensagens de erro e status sobre o estado de conformidade do computador de acordo com a política especificada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Último contato</p></td>
<td align="left"><p>Data e hora em que o computador contatou o servidor pela última vez para informar o status de conformidade. A frequência do contato é configurável. Para obter mais informações, consulte as configurações de política de grupo do MBAM.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-compliance"></a>Relatório de conformidade do computador

Use esse tipo de relatório para coletar informações específicas a um computador ou usuário.

Exiba esse relatório clicando no nome do computador no relatório de conformidade empresarial ou digitando o nome do computador no relatório de conformidade do computador. Este relatório mostra informações de criptografia detalhadas sobre cada unidade (sistema operacional e unidades de dados fixas) em um computador. Ele também indica a política aplicada a cada tipo de unidade no computador. Para ver os detalhes de cada unidade, expanda a entrada nome do computador.

**Observação**  
O status da criptografia do volume de dados removível não é mostrado neste relatório.



**Campos de relatório de conformidade do computador**

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
<td align="left"><p>Nome do computador DNS especificado pelo usuário que é gerenciado pelo MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome de domínio</p></td>
<td align="left"><p>Nome de domínio totalmente qualificado em que o computador cliente reside e é gerenciado pelo MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tipo de computador</p></td>
<td align="left"><p>Tipo de computador. Tipos válidos são não portáteis e portáteis.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sistema operacional</p></td>
<td align="left"><p>Tipo de sistema operacional encontrado no computador cliente que é gerenciado pelo MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Status de conformidade</p></td>
<td align="left"><p>Status geral de conformidade do computador gerenciado pelo MBAM. Os Estados válidos são compatíveis e não são compatíveis.</p>
<p>Observe que o status de conformidade por unidade (veja a tabela a seguir) pode indicar estados de conformidade diferentes. No entanto, esse campo representa o estado de conformidade, de acordo com a política especificada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nível de codificação da política</p></td>
<td align="left"><p>O nível de codificação selecionado pelo administrador durante a especificação da política MBAM (por exemplo, 128-bit com difusor).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Unidade de sistema operacional da política</p></td>
<td align="left"><p>Indica se a criptografia é necessária para o sistema operacional e mostra o tipo de protetor apropriado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Unidade de dados fixos da política</p></td>
<td align="left"><p>Indica se a criptografia é necessária para a unidade de dados fixo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Unidade de dados removível de política</p></td>
<td align="left"><p>Indica se a criptografia é necessária para a unidade removível.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuários do dispositivo</p></td>
<td align="left"><p>Usuários conhecidos no computador gerenciados pelo MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Isenção</p></td>
<td align="left"><p>Status que indica se este computador está isento da política BitLocker.</p></td>
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
<td align="left"><p>Detalhes do status de conformidade</p></td>
<td align="left"><p>Mensagens de erro e status sobre o estado de conformidade do computador, de acordo com a política especificada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Último contato</p></td>
<td align="left"><p>Data e hora em que o computador contatou o servidor pela última vez para informar o status de conformidade. A frequência do contato é configurável. Para obter mais informações, consulte as configurações de política de grupo do MBAM.</p></td>
</tr>
</tbody>
</table>



**Campos da unidade do relatório de conformidade do computador**

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
<td align="left"><p>Tipo de protetor</p></td>
<td align="left"><p>Tipo de protetor selecionado por meio da configuração de política de grupo usada para criptografar um sistema operacional ou volume de dados fixos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Estado do protetor</p></td>
<td align="left"><p>Indica que o computador que está sendo gerenciado pelo MBAM ativou o tipo de protetor especificado na política. Os Estados válidos estão ATIVAdos ou desativados.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Estado de criptografia</p></td>
<td align="left"><p>Estado de criptografia da unidade. Os Estados válidos são criptografados, não criptografados e criptografados.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Status de conformidade</p></td>
<td align="left"><p>Estado que indica se a unidade está de acordo com a política. Os Estados são compatíveis e não são compatíveis.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Detalhes do status de conformidade</p></td>
<td align="left"><p>Mensagens de erro e status do estado de conformidade do computador, de acordo com a política especificada.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-recovery"></a>Relatório de auditoria de recuperação

Use esse tipo de relatório para auditar os usuários que solicitaram acesso às chaves de recuperação do BitLocker. O relatório oferece vários filtros com base nos critérios de filtragem desejados. Você pode filtrar por um tipo específico de usuário (um usuário de suporte técnico ou um usuário final), se a solicitação foi bem-sucedida, se a solicitação foi bem-sucedida, o tipo específico de chave solicitada e um intervalo de datas durante o qual ocorreu a recuperação.

**Campos de relatório de auditoria de recuperação**

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
<td align="left"><p>Data e hora da solicitação</p></td>
<td align="left"><p>Data e hora em que uma solicitação de recuperação de chave foi feita por um usuário final ou usuário de suporte técnico.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Fonte de solicitação de auditoria</p></td>
<td align="left"><p>O site a partir do qual a solicitação foi iniciada. Essa entrada terá um dos dois valores: <strong> portal de autoatendimento </strong> ou <strong> assistência técnica </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Status da solicitação</p></td>
<td align="left"><p>Status da solicitação. Status válidos são bem-sucedidos (a chave foi recuperada) ou falhou (a tecla não foi recuperada).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuário da assistência técnica</p></td>
<td align="left"><p>Usuário de suporte técnico que iniciou a solicitação de recuperação de chave.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Se um usuário avançado da assistência técnica recuperar a chave sem especificar o usuário final, o <strong> campo usuário final </strong> estará em branco. Um usuário da assistência técnica padrão deve especificar o usuário final, e esse usuário será exibido nesse campo.</p>
<p>Uma recuperação por meio do portal de autoatendimento listará o usuário final solicitante, nesse campo e no <strong> campo usuário final </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuário final</p></td>
<td align="left"><p>Usuário final que iniciou a solicitação de recuperação de chave.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Computador</p></td>
<td align="left"><p>Nome do computador que foi recuperado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tipo de chave</p></td>
<td align="left"><p>Tipo de chave que foi solicitada pelo usuário de suporte técnico ou pelo usuário final. Os três tipos de chaves que o MBAM coleta são:</p>
<ul>
<li><p>Senha da chave de recuperação (usada para recuperar um computador no modo de recuperação)</p></li>
<li><p>ID da chave de recuperação (usada para recuperar um computador no modo de recuperação em nome de outro usuário)</p></li>
<li><p>Hash de senha TPM (usado para recuperar um computador com um TPM bloqueado)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Descrição do motivo</p></td>
<td align="left"><p>Motivo pelo qual o tipo de chave especificado foi solicitado pelo usuário de suporte técnico ou pelo usuário final. Os motivos são especificados nos recursos de recuperação de unidade e gerenciamento de TPM do site de administração e monitoramento. As entradas válidas são texto inserido pelo usuário ou um dos seguintes códigos de motivo:</p>
<ul>
<li><p>Ordem de inicialização do sistema operacional alterada</p></li>
<li><p>BIOS alterado</p></li>
<li><p>Arquivos do sistema operacional alterados</p></li>
<li><p>Chave de inicialização perdida</p></li>
<li><p>Perdeu o PIN</p></li>
<li><p>Redefinição de TPM</p></li>
<li><p>Senha perdida</p></li>
<li><p>Cartão inteligente perdido</p></li>
<li><p>Redefinir o bloqueio de PIN</p></li>
<li><p>Ativar o TPM</p></li>
<li><p>Desativar o TPM</p></li>
<li><p>Alterar a senha do TPM</p></li>
<li><p>Limpar TPM</p></li>
</ul></td>
</tr>
</tbody>
</table>



**Observação**  
Os resultados do relatório podem ser salvos em um arquivo clicando no botão **Exportar** na barra de menus **relatórios** .




## Tópicos relacionados


[Monitorando e gerando relatórios de conformidade do BitLocker com o MBAM 2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[Gerando relatórios autônomos do MBAM 2.5](generating-mbam-25-stand-alone-reports.md)



## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





