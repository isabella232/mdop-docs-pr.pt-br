---
title: Janela Histórico
description: Janela Histórico
author: dansimp
ms.assetid: 5bea62e7-d267-40b2-a66d-fb1be7373a1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81f19e3834e945a45238856e23f6ee4a86407c4a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797796"
---
# Janela Histórico


O histórico de um objeto de política de grupo (GPO) pode ser exibido clicando duas vezes em um GPO ou clicando com o botão direito do mouse em um GPO e, em seguida, clicando em **histórico**. Ele também é exibido no GPMC (console de gerenciamento de política de grupo) como uma guia para cada GPO.

O histórico fornece um registro de eventos durante o tempo de vida do GPO selecionado. Na janela do **histórico** , você pode obter um relatório das configurações em uma versão do GPO, comparar várias versões de um GPO ou retornar a uma versão anterior de um GPO.

## Filtrar eventos na janela de histórico


As guias dentro da janela do **histórico** filtram os Estados no histórico do GPO.

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
<td align="left"><p><strong>Todos os Estados</strong></p></td>
<td align="left"><p>Exibir todos os Estados no histórico do GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Versões exclusivas</strong></p></td>
<td align="left"><p>Exiba somente as versões exclusivas do GPO verificado no arquivo. A versão implantada no ambiente de produção, atalhos para versões exclusivas e Estados informativos são omitidos nesta lista.</p></td>
</tr>
</tbody>
</table>



## Informações do evento


As informações são fornecidas para cada Estado no histórico do GPO.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Atributo GPO</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Alterar Data</strong></p></td>
<td align="left"><p>Carimbo de data/hora em que a ação da <strong> </strong> coluna Estado foi realizada.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Estado</strong></p></td>
<td align="left"><p>Um estado no histórico do GPO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Alterado por</strong></p></td>
<td align="left"><p>A pessoa que fez check-in ou implantou o GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Comentário</strong></p></td>
<td align="left"><p>Um comentário inserido pela pessoa que fez check-in ou implantou um GPO no momento em que essa versão foi alterada, útil para identificar as especificidades da versão em caso de necessidade de reverter para uma versão anterior.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Excluídos</strong></p></td>
<td align="left"><p>Se essa versão do GPO pode ser excluída se o número de versões exclusivas de cada GPO retido no arquivo for limitado.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Você pode alterar se uma versão de um GPO pode ser excluída clicando com o botão direito do mouse no GPO e clicando em não <strong> Permitir exclusão </strong> ou <strong> Permitir exclusão </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Versão do computador</strong></p></td>
<td align="left"><p>Versão gerada automaticamente da parte de configuração do computador do GPO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Versão do usuário</strong></p></td>
<td align="left"><p>Versão gerada automaticamente da parte de configuração do usuário do GPO.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Status do GPO</strong></p></td>
<td align="left"><p>A configuração do computador e a configuração do usuário podem ser gerenciadas separadamente umas das outras. Esse status mostra quais partes do GPO estão habilitadas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Informações do GPO de origem</strong></p></td>
<td align="left"><p>Para um GPO que tenha sido importado de outra floresta, o nome do GPO original, o domínio e o usuário e a data associados à última alteração.</p></td>
</tr>
</tbody>
</table>



## Relatórios


Os botões **configurações** e **diferenças** exibem relatórios sobre as configurações do GPO para a versão do GPO ou versões selecionadas. Além disso, clicar com o botão direito do mouse em uma versão de GPO ou em versões fornece a opção para exibir relatórios baseados em XML.

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

-   Algumas alterações nas configurações podem fazer com que um item seja reportado como dois itens (um presente somente no primeiro GPO, um presente somente no segundo), em vez de um item alterado.

### Referências adicionais

-   [Guia Conteúdo](contents-tab-agpm40.md)









