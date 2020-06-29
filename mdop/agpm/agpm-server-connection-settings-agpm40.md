---
title: Configurações de conexão do servidor do AGPM
description: Configurações de conexão do servidor do AGPM
author: dansimp
ms.assetid: cc67f122-6309-4820-92c2-f6a27d897123
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 55bd5c04f573a421674068bea6fc9c6adcd29a12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796098"
---
# Configurações de conexão do servidor do AGPM


Você pode usar as configurações de modelo administrativo para o gerenciamento avançado de política de grupo (AGPM) para configurar de forma centralizada as conexões do servidor do AGPM para administradores de política de grupo para os quais um objeto de política de grupo (GPO) com essas configurações é aplicado.

As configurações a seguir estão disponíveis em User Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM ao editar um GPO.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuração</th>
<th align="left">Efeito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>AGPM: especificar o servidor do AGPM padrão (todos os domínios)</strong></p></td>
<td align="left"><p>Essa configuração de política permite especificar um servidor do AGPM padrão para todos os domínios. Isso é usado somente pelos clientes do AGPM e restringe os administradores de política de grupo a se conectarem a outro arquivo morto. Você pode substituir esse padrão para domínios individuais usando a <strong> configuração do AGPM: especificar servidores de AGPM </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>AGPM: especificar servidores de AGPM</strong></p></td>
<td align="left"><p>Essa configuração de política permite especificar os servidores do AGPM para domínios individuais. Isso é usado somente pelos clientes do AGPM e restringe os administradores de política de grupo a se conectarem a um arquivo morto diferente para o domínio especificado. Para especificar um servidor do AGPM padrão, use o <strong> AGPM: especificar o servidor do AGPM padrão (todos os domínios) </strong> e usar essa configuração de política para substituir o padrão por domínio.</p></td>
</tr>
</tbody>
</table>

 

### Referências adicionais

-   [Pasta Modelos Administrativos](administrative-templates-folder-agpm40.md)

-   [Executar tarefas de administração de AGPM](performing-agpm-administrator-tasks-agpm40.md)

 

 





