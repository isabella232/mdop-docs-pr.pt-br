---
title: Como determinar o tipo de aplicativo a ser sequenciado (App-V 4,6 SP1)
description: Como determinar o tipo de aplicativo a ser sequenciado (App-V 4,6 SP1)
author: dansimp
ms.assetid: 936abee2-98f1-45fb-9f0d-786e1d7464b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 001f6afa36ca28eb1b8e0cc2ccc161cef4194d24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797135"
---
# Como determinar o tipo de aplicativo a ser sequenciado (App-V 4,6 SP1)


Você pode sequenciar três tipos básicos de aplicativos usando o Microsoft Application Virtualization (App-V) Sequencer.

## Para determinar o tipo de aplicativo a ser sequenciado


Use a tabela a seguir para determinar qual tipo de aplicativo você deve sequenciar e para obter mais informações sobre como sequenciar o aplicativo.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo de aplicativo</th>
<th align="left">Descrição</th>
<th align="left">Mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Standard</p></td>
<td align="left"><p>Selecione esta opção para criar um pacote que contenha um aplicativo ou um pacote de aplicativos. Você deve selecionar essa opção para a maioria dos aplicativos que você planeja sequenciar.</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-standard-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Standard Application (App-V 4.6 SP1)](how-to-sequence-a-new-standard-application--app-v-46-sp1-.md)">Como sequenciar um novo aplicativo padrão (App-V 4.6 SP1)</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Complemento ou plug-in</p></td>
<td align="left"><p>Selecione esta opção para criar um pacote que estenda a funcionalidade de um aplicativo padrão, por exemplo, um plug-in para o Microsoft Excel. Além disso, você pode usar plug-ins para aplicativos instalados nativamente ou outro pacote vinculado usando a composição do pacote dinâmico. Para obter mais informações sobre a composição do pacote dinâmico, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> como usar a composição do conjunto dinâmico </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> ).</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Add-on or Plug-in Application (App-V 4.6 SP1)](how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md)">Como sequenciar um novo complemento ou plug-in de aplicativo (App-V 4.6 SP1)</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Middleware</p></td>
<td align="left"><p>Selecione esta opção para criar um pacote que é necessário para um aplicativo padrão, por exemplo, o Microsoft .NET Framework. Os pacotes middleware são usados para a vinculação a outros pacotes usando a composição do pacote dinâmico. Para obter mais informações sobre a composição do pacote dinâmico, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> como usar a composição do conjunto dinâmico </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> ).</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Middleware Application (App-V 4.6 SP1)](how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md)">Como sequenciar um novo Aplicativo middleware (App-V 4.6 SP1)</a></p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Tarefas do Application Virtualization Sequencer (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

 

 





