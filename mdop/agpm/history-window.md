---
title: Janela Histórico
description: Janela Histórico
author: dansimp
ms.assetid: f11f9ad9-bffe-4c56-8c46-fe9c0a8e55c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 02b4336409f33d6c1f2868bceb22cb95120f2198
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797795"
---
# Janela Histórico


O histórico de um objeto de política de grupo (GPO) pode ser exibido clicando duas vezes em um GPO ou clicando com o botão direito do mouse em um GPO e, em seguida, clicando em **histórico**. Ele também é exibido no GPMC ( **console de gerenciamento de política de grupo** ) como uma guia para cada GPO.

O histórico fornece uma lista de todas as versões do GPO selecionado salvas no arquivo morto. Na janela do **histórico** , você pode obter um relatório das configurações dentro de um GPO, comparar várias versões de um GPO ou retornar a uma versão anterior de um GPO.

## Filtrar eventos na janela de histórico


As guias dentro da janela do **histórico** filtram os eventos exibidos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Guias</th>
<th align="left">Filtre</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Mostrar tudo</strong></p></td>
<td align="left"><p>Exibir todas as versões do GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Check-in</strong></p></td>
<td align="left"><p>Exiba somente as versões com check-in do GPO. A versão implantada é omitida nesta lista.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Somente rótulos</strong></p></td>
<td align="left"><p>Exiba somente os GPOs que têm rótulos associados a eles.</p></td>
</tr>
</tbody>
</table>

 

## Informações do evento


As informações são fornecidas para cada evento no histórico do GPO selecionado.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Característica do GPO</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Computador</strong></p></td>
<td align="left"><p>Versão gerada automaticamente da parte de configuração do computador do GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Usuário</strong></p></td>
<td align="left"><p>Versão gerada automaticamente da parte de configuração do usuário do GPO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Hora</strong></p></td>
<td align="left"><p>Carimbo de data/hora da versão do GPO quando a ação no campo status foi executada.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Estado</strong></p></td>
<td align="left"><p>O estado da versão selecionada do GPO:</p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong>Implantada </strong> : esta versão do GPO está atualmente em tempo real no ambiente de produção.</p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong>Check-in </strong> : esta versão do GPO está disponível para editores autorizados a fazer check-out para edição ou para a implantação de um administrador de política de grupo.</p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong>Check-out </strong> : esta versão do GPO atualmente está com check-out por um editor e não está disponível para outros editores. (O estado checked out não é registrado no <strong> Histórico </strong> , exceto para indicar se um GPO está em check-out no momento.)</p>
<p><img src="images/327623bd-0842-4372-be1f-bdc4b8c3481c.gif" alt="Created GPO icon" /> <strong>Criado </strong> : identifica a data e a hora da criação inicial do GPO.</p>
<p><img src="images/8356fcdc-1279-425b-ab14-a23bcfe391da.gif" alt="Labeled GPO icon" /> <strong>Rotulado </strong> : identifica uma versão rotulada do GPO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Status do GPO</strong></p></td>
<td align="left"><p>A configuração do computador e a configuração do usuário podem ser gerenciadas separadamente umas das outras. Esse status mostra quais partes do GPO estão habilitadas.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Proprietário</strong></p></td>
<td align="left"><p>A pessoa que fez check-in ou implantou o GPO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Comentário</strong></p></td>
<td align="left"><p>Um comentário inserido pelo proprietário de um GPO no momento em que essa versão foi modificada. Útil para identificar as especificidades da versão em caso de necessidade de reverter para uma versão anterior.</p></td>
</tr>
</tbody>
</table>

 

## Relatórios


Dependendo se uma única versão do GPO ou várias versões do GPO estiverem selecionadas, os botões **configurações** e **diferenças** exibirão relatórios sobre as configurações do GPO. Clicar com o botão direito do mouse em versões do GPO fornece a opção de exibir relatórios baseados em XML também.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Botão</th>
<th align="left">Efeito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Configurações</strong></p></td>
<td align="left"><p>Gerar um relatório baseado em HTML exibindo as configurações dentro da versão selecionada do GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Existentes</strong></p></td>
<td align="left"><p>Gerar um relatório baseado em HTML que compara as configurações dentro de várias versões selecionadas do GPO.</p></td>
</tr>
</tbody>
</table>

 

### Chave para relatórios de diferença

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Símbolo</th>
<th align="left">Significado</th>
<th align="left">Cor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nenhum(a)</p></td>
<td align="left"><p>O item existe com configurações idênticas nos dois GPOs</p></td>
<td align="left"><p>Varia de acordo com o nível</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[#]</strong></p></td>
<td align="left"><p>O item existe nos dois GPOs, mas com configurações alteradas</p></td>
<td align="left"><p>Chuva</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>[-]</strong></p></td>
<td align="left"><p>O item existe somente no primeiro GPO</p></td>
<td align="left"><p>Vermelho</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[+]</strong></p></td>
<td align="left"><p>O item existe somente no segundo GPO</p></td>
<td align="left"><p>Verde</p></td>
</tr>
</tbody>
</table>

 

-   Para itens com configurações alteradas, as configurações alteradas são identificadas quando o item é expandido. O valor do atributo em cada GPO é exibido na mesma ordem em que os GPOs são exibidos no relatório.

-   Algumas alterações nas configurações podem fazer com que um item seja reportado como dois itens diferentes (um presente somente no primeiro GPO, um presente somente no segundo), em vez de um item alterado.

### Referências adicionais

-   [Guia Conteúdo](contents-tab.md)

 

 





