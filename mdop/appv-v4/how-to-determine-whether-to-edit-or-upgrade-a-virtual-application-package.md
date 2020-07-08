---
title: Como determinar se um pacote de aplicativo virtual deve ser editado ou atualizado
description: Como determinar se um pacote de aplicativo virtual deve ser editado ou atualizado
author: dansimp
ms.assetid: 33dd5332-6802-46e0-9748-43fcc8f80aa3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b256a4927231613b6f2e688b5951adf57c9cb89a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797138"
---
# Como determinar se um pacote de aplicativo virtual deve ser editado ou atualizado


Use a tabela a seguir para ajudar a determinar se um pacote de aplicativo virtual pode ser aberto para edição, se você precisa criar uma nova versão do pacote, ou se qualquer uma dessas opções está disponível, usando o sequenciador do App-V.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Ação</th>
<th align="left">Abrir para edição</th>
<th align="left">Abrir para atualização</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Exiba as propriedades do pacote.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="even">
<td align="left"><p>Exiba o histórico de alterações do pacote.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Exibir arquivos de pacote associados.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="even">
<td align="left"><p>Editar configurações do registro.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Revisar configurações de pacote adicionais (exceto propriedades de arquivos do sistema operacional).</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="even">
<td align="left"><p>Crie um MSI (Windows Installer) associado.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modifique o arquivo OSD.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="even">
<td align="left"><p>Compactar e descompactar pacote.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Adicionar associações de tipo de arquivo.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="even">
<td align="left"><p>Renomear atalhos.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Definir o estado virtualizado da chave do registro (override/Merge).</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="even">
<td align="left"><p>Definir o estado da pasta virtualizada.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Editar mapeamentos do sistema de arquivos virtual.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="even">
<td align="left"><p>Revise Todas as propriedades de arquivo de sistema operacional associadas para um pacote.</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Adicionar mais serviços.</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="even">
<td align="left"><p>Adicionar mais arquivos.</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Coletar e configurar descritores de segurança associados.</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="even">
<td align="left"><p>Aplicar atualizações de segurança ou atualizar para uma nova versão.</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Adicionar um aplicativo adicional.</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="even">
<td align="left"><p>Aplique atualizações que exijam que o aplicativo seja aberto.</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Aplique atualizações que exijam que o computador seja reiniciado.</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>Sim</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Como editar um aplicativo virtual existente](how-to-edit-an-existing-virtual-application.md)

[Como fazer upgrade de um aplicativo virtual existente](how-to-upgrade-an-existing-virtual-application.md)

 

 





