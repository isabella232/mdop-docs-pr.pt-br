---
title: Noções básicas sobre relatórios do MBAM
description: Noções básicas sobre relatórios do MBAM
author: dansimp
ms.assetid: 34e4aaeb-7f89-41a1-b816-c6fe8397b060
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa64a4724c87a42774e569b556013bfec2ed5514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799158"
---
# Noções básicas sobre relatórios do MBAM


O monitoramento e a administração do Microsoft BitLocker (MBAM) geram vários relatórios para monitorar o uso e a conformidade do BitLocker. Este tópico descreve os relatórios do MBAM para conformidade empresarial, computadores individuais, compatibilidade de hardware e atividade de recuperação de chave.

## Noções básicas sobre relatórios


Para acessar o recurso relatórios do MBAM, abra o site de administração do MBAM. Selecione **relatórios** no painel de navegação. Em seguida, no painel de conteúdo principal, clique na guia do tipo de relatório: **relatório de conformidade empresarial**, **relatório de conformidade do computador**, relatório de auditoria de **hardware**ou relatório de **auditoria de recuperação**.

### Relatório de conformidade empresarial

Um relatório de conformidade empresarial fornece informações sobre a conformidade geral do BitLocker em sua organização. Os filtros disponíveis para este relatório permitem restringir os resultados da pesquisa de acordo com o estado de conformidade e o status do erro. Este relatório é executado a cada seis horas.

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
<td align="left"><p>O nome DNS especificado pelo usuário que está sendo gerenciado pelo MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome de domínio</p></td>
<td align="left"><p>O nome de domínio totalmente qualificado em que o computador cliente reside e é gerenciado pelo MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Status de conformidade</p></td>
<td align="left"><p>O estado de conformidade do computador, de acordo com a política especificada para o computador. Os Estados possíveis são incompatíveis e em conformidade. Para obter mais informações, consulte Estados de conformidade do relatório de conformidade empresarial neste tópico.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Isenção</p></td>
<td align="left"><p>O estado do hardware do computador para determinar a identificação do tipo de hardware e se o computador está isento da política. Há três estados possíveis: hardware desconhecido (o tipo de hardware não foi identificado pela MBAM), isenta de hardware (o tipo de hardware foi identificado e foi marcado como isento da política de MBAM) e não está isento (o hardware foi identificado e não está isento da política).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuários do dispositivo</p></td>
<td align="left"><p>Usuários conhecidos no computador que está sendo gerenciado pelo MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Detalhes do status de conformidade</p></td>
<td align="left"><p>Mensagens de erro e status sobre o estado de conformidade do computador de acordo com a política especificada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Último contato</p></td>
<td align="left"><p>Data e hora em que o computador contatou o servidor pela última vez para informar o status de conformidade. Esse horário é configurável. Consulte Configurações de política de MBAM.</p></td>
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
<td align="left"><p>O computador não é compatível, de acordo com a política especificada, e o tipo de hardware não foi indicado como isento da política.</p></td>
<td align="left"><p>Clique em <strong> nome </strong> do computador para expandir o relatório de conformidade do computador e determinar se o estado de cada unidade está em conformidade com a política especificada. Se o estado de criptografia indicar que o computador não está criptografado, talvez a criptografia ainda esteja em andamento ou talvez haja um erro no computador. Se não houver nenhum erro, a causa provável é que o computador ainda está em processo de conexão ou estabelecimento do status de criptografia. Verifique novamente mais tarde para determinar se o estado muda.</p></td>
</tr>
<tr class="even">
<td align="left"><p>CLS</p></td>
<td align="left"><p>Não isento</p></td>
<td align="left"><p>O computador é compatível de acordo com a política especificada.</p></td>
<td align="left"><p>Nenhuma ação necessária. Opcionalmente, você pode exibir o relatório de conformidade do computador para confirmar o estado do computador.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CLS</p></td>
<td align="left"><p>Isento de hardware</p></td>
<td align="left"><p>Se o tipo de hardware estiver isento. Independentemente de como a política é definida ou o status individual de cada unidade de disco rígido, o estado geral é considerado compatível.</p></td>
<td align="left"><p>Nenhuma ação necessária.</p></td>
</tr>
<tr class="even">
<td align="left"><p>CLS</p></td>
<td align="left"><p>Hardware desconhecido</p></td>
<td align="left"><p>O MBAM reconhece o tipo de hardware, mas o MBAM não sabe se está isento ou isento de isenção. Isso ocorrerá se o administrador não tiver definido o status de compatibilidade do hardware. Portanto, o MBAM é revertido para o status compatível por padrão.</p></td>
<td align="left"><p>Esse é o estado inicial de um cliente MBAM recém implantado. Geralmente, é apenas um estado transitório. Mesmo que o administrador tenha marcado o hardware como compatível, pode haver um atraso significativo ou tempo de espera configurável antes de o computador cliente retornar a relatórios. Anote a hora do último contato e faça check-in novamente após o intervalo especificado para ver se o estado mudou. Se o estado não mudar, pode haver um erro para este computador ou tipo de hardware.</p></td>
</tr>
</tbody>
</table>

 

### Relatório de conformidade do computador

O relatório de conformidade do computador exibe informações específicas para um computador ou usuário.

O relatório de conformidade do computador fornece informações de criptografia detalhadas e políticas aplicáveis para cada unidade em um computador, incluindo unidades do sistema operacional e unidades de dados fixos. Para exibir esse tipo de relatório, clique no nome do computador no relatório de conformidade empresarial ou digite o nome do computador no relatório de conformidade do computador. Para ver os detalhes de cada unidade, expanda a entrada nome do computador.

**Observação**  Esse relatório não fornece o status de criptografia para volumes de dados removíveis.

 

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
<td align="left"><p>O nome do computador DNS especificado pelo usuário que está sendo gerenciado pelo MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome de domínio</p></td>
<td align="left"><p>O nome de domínio totalmente qualificado em que o computador cliente reside e é gerenciado pelo MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tipo de computador</p></td>
<td align="left"><p>O tipo de portabilidade do computador. Tipos válidos são não portáteis e portáteis.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sistema operacional</p></td>
<td align="left"><p>Tipo de sistema operacional instalado no computador cliente gerenciado MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Status de conformidade</p></td>
<td align="left"><p>O status geral de conformidade do computador gerenciado pela MBAM. Os Estados válidos são compatíveis e não são compatíveis. Embora seja possível ter unidades de conformidade e de não conformidade no mesmo computador, esse campo indica a conformidade geral do computador por política especificada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Força da política de Cypher</p></td>
<td align="left"><p>A intensidade de codificação selecionada pelo administrador durante a especificação da política MBAM. Por exemplo, 128-bit com difusor</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Unidade de sistema operacional da política</p></td>
<td align="left"><p>Indica se a criptografia é necessária para o o/S e o tipo de protetor conforme aplicável.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Unidade de dados fixos da política</p></td>
<td align="left"><p>Indica se a criptografia é necessária para a unidade fixa.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Unidade de dados removível de política</p></td>
<td align="left"><p>Indica se a criptografia é necessária para a unidade removível.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuários do dispositivo</p></td>
<td align="left"><p>Fornece a identidade de usuários conhecidos no computador.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Isenção</p></td>
<td align="left"><p>Indica se o tipo de hardware do computador é reconhecido pela MBAM e, se for conhecido, se o computador foi indicado como isento da política. Há três Estados: hardware desconhecido (o tipo de hardware não foi identificado pela MBAM); Isento de hardware (o tipo de hardware foi identificado e foi marcado como isento da política MBAM); e não isento (o hardware foi identificado e não está isento da política).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Fabricante</p></td>
<td align="left"><p>O nome do fabricante do computador exibido no BIOS do computador.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modelo</p></td>
<td align="left"><p>O nome do modelo do fabricante do computador, como aparece no BIOS do computador.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Detalhes do status de conformidade</p></td>
<td align="left"><p>Mensagens de erro e status do estado de conformidade do computador de acordo com a política especificada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Último contato</p></td>
<td align="left"><p>Data e hora em que o computador contatou o servidor pela última vez para informar o status de conformidade. T</p></td>
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
<td align="left"><p>Letra da unidade de computador que foi atribuída a essa determinada unidade pelo usuário.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tipo de unidade</p></td>
<td align="left"><p>Tipo de unidade. Os valores válidos são unidade do sistema operacional e unidade de dados fixa. Esses são drives físicos, em vez de volumes lógicos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Força Cypher</p></td>
<td align="left"><p>Nível de codificação selecionado pelo administrador durante a especificação da política MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tipo de protetor</p></td>
<td align="left"><p>Tipo de protetor selecionado pela política usada para criptografar um sistema operacional ou volume fixo. Os tipos de protetor válidos em uma unidade de sistema operacional são TPM ou TPM + PIN. O único tipo de protetor válido para um volume de dados fixo é a senha.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Estado do protetor</p></td>
<td align="left"><p>Este campo indica se o computador ativou o tipo de protetor especificado na política. Os Estados válidos estão ATIVAdos ou desativados.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Estado de criptografia</p></td>
<td align="left"><p>Esse é o estado atual de criptografia da unidade. Os Estados válidos são criptografados, não criptografados e criptografados.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Status de conformidade</p></td>
<td align="left"><p>Indica se a unidade está de acordo com a política. Os Estados são compatíveis e não são compatíveis.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Detalhes do status de conformidade</p></td>
<td align="left"><p>Contém mensagens de erro e status sobre o estado de conformidade do computador.</p></td>
</tr>
</tbody>
</table>

 

### Relatório de auditoria de hardware

Este relatório pode ajudá-lo a auditar alterações no status de compatibilidade de hardware de modelos e modelos de computador específicos. Para ajudá-lo a restringir os resultados da pesquisa, esse relatório inclui a filtragem de critérios, como tipo de alteração e hora de ocorrência. Cada alteração de estado é controlada por usuário e data e hora. O tipo de hardware é automaticamente preenchido pelo agente do MBAM que é executado no computador cliente. Esse relatório controla as alterações do usuário nas informações coletadas diretamente do computador gerenciado pelo MBAM. Uma alteração administrativa típica está mudando de compatível para incompatível. No entanto, o administrador também pode revisar qualquer campo.

**Campos de relatório de auditoria de hardware**

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
<td align="left"><p>Data e hora</p></td>
<td align="left"><p>Data e hora em que uma alteração foi feita para o tipo de hardware. Observe que cada tipo de hardware exclusivo é atribuído a pelo menos uma entrada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuário</p></td>
<td align="left"><p>Usuário administrativo que fez a alteração para a entrada específica.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tipo de alteração</p></td>
<td align="left"><p>Tipo de alteração feita nas informações de tipo de hardware. Os valores válidos são soma (nova entrada), atualizar (alterar entrada existente) ou exclusão (remover entrada existente).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Valor original</p></td>
<td align="left"><p>Valor da especificação do tipo de hardware antes da alteração ser feita.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Valor atual</p></td>
<td align="left"><p>Valor da especificação do tipo de hardware após a alteração ter sido feita.</p></td>
</tr>
</tbody>
</table>

 

### Relatório de auditoria de recuperação

O relatório de auditoria de recuperação pode ajudá-lo a auditar os usuários que solicitaram acesso às chaves de recuperação. Os critérios de filtro deste relatório incluem o tipo de usuário que está realizando a solicitação, o tipo de chave solicitada, o tempo de ocorrência, êxito ou falha, hora de ocorrência e tipo de usuário solicitando (suporte técnico, usuário final). Esse relatório permite que os administradores produzam relatórios contextuais de acordo com a necessidade.

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
<td align="left"><p>A data e a hora em que uma solicitação de recuperação de chave foi feita por um usuário final ou usuário de suporte técnico.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Status da solicitação</p></td>
<td align="left"><p>Status da solicitação. Os status válidos são bem-sucedidos (a chave foi recuperada) ou falha (a tecla não foi recuperada).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuário da assistência técnica</p></td>
<td align="left"><p>O usuário de suporte técnico que iniciou a solicitação de recuperação de chave. Se o usuário do suporte técnico recuperar a chave em nome de um usuário final, o campo usuário final estará em branco.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuário</p></td>
<td align="left"><p>O usuário final que iniciou a solicitação de recuperação de chave.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tipo de chave</p></td>
<td align="left"><p>O tipo de chave que foi solicitada. O MBAM coleta três tipos de chave: senha da chave de recuperação (para a recuperação de um computador no modo de recuperação); ID da chave de recuperação (para recuperar um computador no modo de recuperação em nome de outro usuário); e hash de senha do Trusted Platform Module (TPM) (para recuperar um computador com um TPM bloqueado).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descrição do motivo</p></td>
<td align="left"><p>O motivo pelo qual o tipo de chave especificado foi solicitado. Os motivos são especificados nos recursos de recuperação de unidade e gerenciamento de TPM do site administrativo. As entradas válidas incluem texto inserido pelo usuário ou um dos seguintes códigos de motivo:</p>
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
</ul>
<p></p></td>
</tr>
</tbody>
</table>

 

**Observação**  Para salvar os resultados do relatório em um arquivo, clique no botão **Exportar** na barra de menus relatórios.

 

## Tópicos relacionados


[Monitorando e Gerando Relatórios de Conformidade do BitLocker com o MBAM 1.0](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





