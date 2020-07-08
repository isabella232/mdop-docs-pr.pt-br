---
title: Novidades no AGPM 4.0
description: Novidades no AGPM 4.0
author: dansimp
ms.assetid: 31775f7f-a59c-4e64-a875-0adc9f5bc835
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 82b4445a7d22fb7c1ef4f42d896f11908a22f2f5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797658"
---
# Novidades no AGPM 4.0


O gerenciamento avançado de política de grupo (AGPM) 4.0 da Microsoft oferece novos recursos que permitem pesquisar objetos de política de grupo (GPOs), filtrar a lista de GPOs exibidos, exportar e importar um GPO para uma floresta diferente e instalar o AGPM em computadores que executam o Windows e o Windows Server2008R2.

## Pesquisar e filtrar GPOs


No AGPM 4,0, você pode pesquisar a lista de GPOs em busca de atributos específicos para filtrar a lista de GPOs exibida. Por exemplo, você pode pesquisar GPOs com um nome, estado ou comentário específico. Você também pode pesquisar os GPOs que foram alterados pela última vez por um determinado administrador de política de grupo ou em uma data específica.

Você pode criar uma cadeia de pesquisa complexa usando o *atributo Format GPO 1: Pesquisar texto 1 atributo do GPO 2: Pesquisar texto 2..*., onde um atributo GPO é qualquer título de coluna na lista de GPOs do AGPM. Por exemplo, para pesquisar todos os GPOs com nomes, incluindo o texto "MyGPO" que está com check-in e alterados pela última vez pela Editor03 do usuário, você deve digitar o seguinte na caixa de pesquisa: **nome: MyGPO Estado:****check-in****alterado por: Editor03**. A pesquisa retorna correspondências parciais para que você possa inserir parte de um nome de GPO ou nome de usuário e exibir uma lista de todos os GPOs que incluem esse texto no nome.

Além disso, você pode usar os mesmos termos especiais disponíveis ao pesquisar no Windows para pesquisar os GPOs alterados em uma data específica ou em um intervalo de datas. Por exemplo, **alterar Data:****lastmonth** ou **alterar Data:****thisweek**.

## Exportar e importar GPOs para florestas diferentes


Usando o AGPM 4,0, você pode copiar um GPO controlado de um domínio em uma floresta para um domínio em uma segunda floresta. Por exemplo, você pode exportar um GPO de um domínio em uma floresta para um arquivo CAB usando o AGPM, copiar esse arquivo CAB para uma unidade USB, conectar a unidade USB a um computador em um domínio em uma segunda floresta e importar o GPO para o AGPM em um domínio na segunda floresta. Você pode importar o GPO como um novo GPO controlado ou importá-lo para substituir as configurações de um GPO existente que está com check-out.

## Suporte para Windows Server 2008 R2 e Windows 7


O AGPM 4,0 tem suporte para Windows Server2008R2 e Windows e ainda oferece suporte ao Windows Server2008 e WindowsVista® com Service Pack1 (SP1). No entanto, há limitações em um ambiente misto que inclui os sistemas operacionais mais recentes e mais antigos, conforme indicado na tabela a seguir.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operacional no qual o servidor do AGPM 4,0 é executado</th>
<th align="left">Sistema operacional no qual o cliente do AGPM 4,0 é executado</th>
<th align="left">Status do suporte do AGPM 4,0</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 ou Windows7</p></td>
<td align="left"><p>Windows Server2008R2 ou Windows7</p></td>
<td align="left"><p>Com suporte</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 ou Windows7</p></td>
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server2008R2 ou no Windows7</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Windows Server2008R2 ou Windows7</p></td>
<td align="left"><p>Sem Suporte</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Com suporte, mas não pode reportar ou editar configurações de política ou itens de preferência que existem somente no Windows Server2008R2 ou no Windows7</p></td>
</tr>
</tbody>
</table>

 

 

 





