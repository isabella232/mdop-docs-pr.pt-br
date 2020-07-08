---
title: Noções básicas sobre relatórios do MBAM
description: Noções básicas sobre relatórios do MBAM
author: dansimp
ms.assetid: 8778f333-760e-4f26-acb4-4e73b6fbb536
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c3ca5e4da4cbcea80c87520f0ecd05e1e7d6be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799347"
---
# Noções básicas sobre relatórios do MBAM


Se você escolheu a topologia autônoma ao instalar o Microsoft BitLocker Administration and Monitoring (MBAM), é possível executar diferentes relatórios no MBAM para monitorar o uso e a conformidade do BitLocker. O MBAM relata a conformidade e outras informações sobre todos os computadores e dispositivos que ele gerencia. As informações neste tópico podem ser usadas para ajudar você a entender os relatórios de administração e monitoramento do Microsoft BitLocker para empresas e para conformidade de computador individual e para a atividade de recuperação de chave.

**Observação**  Se você escolheu a topologia do Configuration Manager quando instalou o Microsoft BitLocker Administration and Monitoring (MBAM), os relatórios são gerados do Configuration Manager em vez de MBAM. Para obter mais informações sobre os relatórios executados a partir do Configuration Manager, consulte [noções básicas sobre relatórios do MBAM no Configuration Manager](understanding-mbam-reports-in-configuration-manager.md).

 

## Noções básicas sobre relatórios


Para acessar o recurso relatórios da administração e do monitoramento do Microsoft BitLocker, abra um navegador da Web e abra o site Administração e monitoramento. Selecione **relatórios** na barra de menus à esquerda e, em seguida, selecione na barra de menus superior o tipo de relatório que você deseja gerar.

### Relatório de conformidade empresarial

Use esse tipo de relatório para coletar informações sobre a conformidade geral do BitLocker em sua organização. Você pode usar filtros diferentes para restringir os resultados da pesquisa ao estado de conformidade e status de erro. As informações do relatório são atualizadas a cada seis horas.

**Campos relatório de conformidade para empresas**

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
<td align="left"><p>Nome DNS especificado pelo usuário que está sendo gerenciado pelo MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome de domínio</p></td>
<td align="left"><p>Nome de domínio totalmente qualificado em que o computador cliente reside e é gerenciado pelo MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Status de conformidade</p></td>
<td align="left"><p>Estado de conformidade do computador, de acordo com a política especificada para o computador. Os Estados são compatíveis e não são compatíveis. Consulte a tabela Estados de conformidade para relatórios corporativos de conformidade para obter mais informações sobre como interpretar Estados de conformidade.</p></td>
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

 

**Estados de conformidade para relatórios de conformidade empresarial**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Status de conformidade</th>
<th align="left">Isenção</th>
<th align="left">Descrição</th>
<th align="left">Ação do usuário</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Não compatível</p></td>
<td align="left"><p>Não isento</p></td>
<td align="left"><p>O computador não é compatível, de acordo com a política especificada.</p></td>
<td align="left"><p>Expanda os detalhes do relatório de conformidade do computador clicando em <strong> nome </strong> do computador e determine se o estado de cada unidade está em conformidade com a política especificada. Se o estado de criptografia indicar que o computador não está criptografado, a criptografia pode estar em processo, ou há um erro no computador. Se não houver nenhum erro, a causa provável é que o computador ainda está em processo de conexão ou estabelecimento do status de criptografia. Verifique novamente mais tarde para determinar se o estado muda.</p></td>
</tr>
<tr class="even">
<td align="left"><p>CLS</p></td>
<td align="left"><p>Não isento</p></td>
<td align="left"><p>O computador é compatível, de acordo com a política especificada.</p></td>
<td align="left"><p>Nenhuma ação necessária; o estado do computador pode ser confirmado exibindo o relatório de conformidade do computador.</p></td>
</tr>
</tbody>
</table>

 

### Relatório de conformidade do computador

Use esse tipo de relatório para coletar informações específicas a um computador ou usuário.

Este relatório pode ser visualizado clicando no nome do computador no relatório de conformidade empresarial ou digitando o nome do computador no relatório de conformidade do computador. O relatório de conformidade do computador fornece informações de criptografia detalhadas sobre cada unidade (sistema operacional e unidades de dados fixas) em um computador, além de uma indicação da política aplicada a cada tipo de unidade no computador. Para ver os detalhes de cada unidade, expanda a entrada nome do computador.

**Observação**  O status da criptografia do volume de dados removível não será exibido no relatório.

 

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
<td align="left"><p>Tipo de sistema operacional encontrado no computador cliente MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Status de conformidade</p></td>
<td align="left"><p>Status geral de conformidade do computador gerenciado pela MBAM. Os Estados válidos são compatíveis e não são compatíveis. Observe que o status de conformidade por unidade (veja a tabela a seguir) pode indicar estados de conformidade diferentes. No entanto, esse campo representa o estado de conformidade, de acordo com a política especificada.</p></td>
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
<td align="left"><p>Usuários conhecidos no computador que está sendo gerenciado pelo MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Fabricante</p></td>
<td align="left"><p>Nome do fabricante do computador, como aparece no BIOS do computador.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Modelo</p></td>
<td align="left"><p>Nome do modelo do fabricante do computador, como aparece no BIOS do computador.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Detalhes do status de conformidade</p></td>
<td align="left"><p>Mensagens de erro e status do estado de conformidade do computador, de acordo com a política especificada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Último contato</p></td>
<td align="left"><p>Data e hora em que o computador contatou o servidor pela última vez para informar o status de conformidade. A frequência do contato é configurável (consulte Configurações de política de MBAM).</p></td>
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
<td align="left"><p>Tipo de protetor selecionado por meio da política usada para criptografar um sistema operacional ou volume de dados fixos.</p></td>
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

 

### Relatório de auditoria de recuperação

Use esse tipo de relatório para auditar os usuários que solicitaram acesso às chaves de recuperação. O relatório oferece vários filtros com base nos critérios de filtragem desejados. Os usuários podem filtrar em um tipo específico de usuário, um usuário de suporte técnico ou um usuário final, se a solicitação falhou ou foi bem-sucedida, o tipo específico de chave solicitada e um intervalo de datas durante o qual ocorreu a recuperação. O administrador pode produzir relatórios contextuais de acordo com a necessidade.

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
<td align="left"><p>Status da solicitação</p></td>
<td align="left"><p>Status da solicitação. Os status válidos são bem-sucedidos (a chave foi recuperada) ou falha (a tecla não foi recuperada).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuário da assistência técnica</p></td>
<td align="left"><p>Usuário de suporte técnico que iniciou a solicitação de recuperação de chave. Observação: se o usuário de suporte técnico recuperar a chave em um usuário final, o campo usuário final estará em branco.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuário</p></td>
<td align="left"><p>Usuário final que iniciou a solicitação de recuperação de chave.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tipo de chave</p></td>
<td align="left"><p>Tipo de chave que foi solicitada pelo usuário de suporte técnico ou pelo usuário final. Os três tipos de chaves que o MBAM coleta são: senha da chave de recuperação (usada para recuperar um computador no modo de recuperação), ID da chave de recuperação (usada para recuperar um computador no modo de recuperação em nome de outro usuário) e hash de senha do TPM (usado para recuperar um computador com um TPM bloqueado).</p></td>
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

 

**Observação**  Os resultados do relatório podem ser salvos em um arquivo clicando no botão **Exportar** na barra de menus relatórios. Para obter mais informações sobre como executar relatórios do MBAM, consulte [como gerar relatórios do MBAM](how-to-generate-mbam-reports-mbam-2.md).

 

## Tópicos relacionados


[Monitorando e Gerando Relatórios de Conformidade do BitLocker com o MBAM 2.0](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





