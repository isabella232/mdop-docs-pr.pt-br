---
title: Planejamento da implantação do App-V 5.1 com um sistema de distribuição eletrônica de software
description: Planejamento da implantação do App-V 5.1 com um sistema de distribuição eletrônica de software
author: dansimp
ms.assetid: c26602c2-5e8d-44e6-90df-adacc593607e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fde3f0ea4f1dec72b97143b4b27dd0b32a503b15
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796240"
---
# Planejamento da implantação do App-V 5.1 com um sistema de distribuição eletrônica de software


Se você estiver usando um sistema de distribuição de software eletrônico para implantar pacotes do App-V, examine as considerações de planejamento a seguir. Para obter informações sobre como usar o System Center Configuration Manager para implantar o App-V, consulte [introdução ao gerenciamento de aplicativos no Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816).

Examine as seguintes opções de componentes e requisitos de arquitetura que se aplicam quando você usa um ESD para implantar pacotes do App-V:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Requisito ou opção de implantação</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>O servidor de gerenciamento do App-V, o banco de dados de gerenciamento e o servidor de publicação não são necessários.</p></td>
<td align="left"><p>Essas funções são manipuladas pela solução ESD implementada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Você pode implantar o servidor de relatórios do App-V e relatar o banco de dados lado a lado com o ESD.</p></td>
<td align="left"><p>A implantação lado a lado permite coletar dados e gerar relatórios.</p>
<p>Se você habilitar o cliente App-V para enviar informações de relatório e não estiver usando o servidor de relatórios do App-V, os dados de relatório serão armazenados em arquivos. xml associados.</p></td>
</tr>
</tbody>
</table>

 






## Tópicos relacionados


[Planejando a implantação do App-V](planning-to-deploy-app-v51.md)

 

 





