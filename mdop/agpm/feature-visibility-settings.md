---
title: Configurações de visibilidade do recurso
description: Configurações de visibilidade do recurso
author: dansimp
ms.assetid: 9db2ba03-fb75-4f95-9138-ec89b9fc8d01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26f19895d0a9163885779688ba7d89f6d16f2a17
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797799"
---
# Configurações de visibilidade do recurso


As configurações de modelo administrativo para gerenciamento avançado de política de grupo (AGPM) permitem que você configure centralmente a visibilidade do nó de **controle de alterações** e a guia **histórico** para administradores de política de grupo para os quais um objeto de política de grupo (GPO) com essas configurações é aplicado.

As configurações a seguir estão disponíveis em snap-ins do Configuration\\Administrative Templates\\Windows Components\\Microsoft console de gerenciamento \ \ restritos/permitidos Snap-ins\\Extension no **Editor de objeto de política de grupo** durante a edição de um GPO no GPMC (console de gerenciamento de política de grupo). Se esse caminho não estiver visível, clique com o botão direito do mouse em **modelos administrativos**e adicione o modelo AGPM. admx ou AGPM. adm.

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
<td align="left"><p><strong>Controle de alterações do AGPM</strong></p></td>
<td align="left"><p>Se habilitada ou não configurada, o <strong> nó de controle de alterações </strong> fica visível no GPMC.</p>
<p>Se desabilitado, o <strong> nó de controle de alterações </strong> não fica visível no GPMC.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Extensão do link do AGPM</strong></p></td>
<td align="left"><p>Se habilitada ou não configurada, uma <strong> </strong> guia histórico será exibida no GPMC para cada GPO vinculado.</p>
<p>Se desabilitado, <strong> a </strong> guia histórico não fica visível para GPOs vinculados.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Extensão do GPO do AGPM</strong></p></td>
<td align="left"><p>Se habilitada ou não configurada, uma <strong> </strong> guia histórico será exibida no GPMC para cada GPO.</p>
<p>Se desabilitado, <strong> a </strong> guia histórico não fica visível para GPOs.</p></td>
</tr>
</tbody>
</table>

 

### Referências adicionais

-   [Configurações de Modelo Administrativo](administrative-template-settings.md)

 

 





