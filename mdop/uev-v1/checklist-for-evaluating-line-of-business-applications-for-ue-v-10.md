---
title: Lista de verificação para avaliar os aplicativos de linha de negócios para a UE-V 1.0
description: Lista de verificação para avaliar os aplicativos de linha de negócios para a UE-V 1.0
author: dansimp
ms.assetid: 3bfaab30-59f7-4099-abb1-d248ce0086b8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 133bc5d195763b7281fd8d152e153231ac4c4d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799876"
---
# Lista de verificação para avaliar os aplicativos de linha de negócios para a UE-V 1.0


Para avaliar quais aplicativos de linha de negócios devem ser incluídos na sua implantação do UE-V, considere o seguinte:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Este aplicativo contém configurações que o usuário pode personalizar?</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>É importante para o usuário que essas configurações são de roaming?</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Essas configurações de usuário já são gerenciadas por uma solução de política de gerenciamento ou configurações de aplicativo? O UE-V aplica as configurações do aplicativo nas configurações de inicialização do aplicativo e do Windows durante os eventos de logon, desbloqueio ou conexão remota. Se você usa o UE-V com outras soluções de política de configurações, os usuários podem enfrentar inconsistência nas configurações de roaming.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>As configurações do aplicativo são específicas do computador? Preferências de aplicativo e personalizações associadas a hardware ou configurações de computador específicas não fazem roaming consistente entre as sessões e podem causar uma experiência de aplicativo ruim.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>As configurações da loja de aplicativos são encontradas no diretório arquivos de programas ou no diretório de arquivos localizado no diretório <strong> usuários </strong> \ [nome de usuário] \ <strong> AppData </strong>  \  <strong> LocalLow </strong> ? Os dados de aplicativo armazenados em qualquer um desses locais geralmente não devem ser movidos com o usuário, pois esses dados são específicos do computador ou porque os dados são muito grandes para o roaming.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>O aplicativo armazena todas as configurações em um arquivo que contém outros dados de aplicativo que não devem ser movidos? O UE-V sincroniza arquivos como uma unidade única. Se as configurações forem armazenadas em arquivos que incluam dados do aplicativo além das configurações, a sincronização desses dados adicionais poderá causar uma experiência de aplicativo ruim.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Qual é o tamanho dos arquivos que contêm as configurações? O desempenho da sincronização de configurações pode ser afetado por arquivos grandes. Incluir arquivos grandes pode afetar o desempenho da sincronização das configurações.</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Planejamento para os métodos de configuração da UE-V](planning-for-ue-v-configuration-methods.md)

[Planejamento para a UE-V 1.0](planning-for-ue-v-10.md)

 

 





