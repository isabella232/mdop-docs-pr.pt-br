---
title: Configurações de conexão do servidor do AGPM
description: Configurações de conexão do servidor do AGPM
author: dansimp
ms.assetid: faf78e5b-2b0d-4069-9b8c-910add892200
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63163de0a1adf744e6d442b8073e5b32352ed67
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796145"
---
# Configurações de conexão do servidor do AGPM


Você pode usar as configurações de modelo administrativo para o gerenciamento avançado de política de grupo (AGPM) para configurar de forma centralizada as conexões do servidor do AGPM para administradores de política de grupo para os quais um objeto de política de grupo (GPO) com essas configurações é aplicado.

As configurações a seguir estão disponíveis em User Configuration\\Administrative Templates\\Windows Components\\AGPM ao editar um GPO. Se esse caminho não estiver visível, clique com o botão direito do mouse em **modelos administrativos**e adicione o modelo AGPM. admx ou AGPM. adm.

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
<td align="left"><p><strong>Servidor do AGPM (todos os domínios)</strong></p></td>
<td align="left"><p>Se habilitada, essa configuração configura centralmente uma conexão do servidor do AGPM para ser usada por todos os domínios e desabilita as configurações na <strong> Guia do servidor </strong> do AGPM para administradores de política de grupo. Para vários servidores de AGPM, defina essa configuração com um servidor padrão e, em seguida, defina a <strong> configuração do servidor do AGPM </strong> no modelo administrativo para substituir esse servidor para outros domínios.</p>
<p>Se desabilitada ou não configurada, cada administrador de política de grupo deve selecionar o servidor do AGPM a ser exibido para cada domínio na <strong> guia servidor do AGPM </strong> no AGPM.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Servidor do AGPM</strong></p></td>
<td align="left"><p>Se habilitada, essa configuração configura centralmente vários servidores de AGPM específicos do domínio, substituindo a <strong> configuração do servidor do AGPM (todos os domínios) </strong> no modelo administrativo. Se o seu ambiente exigir apenas um único servidor do AGPM, use apenas a <strong> configuração servidor do AGPM (todos os domínios) </strong> no modelo administrativo.</p>
<p>Se desabilitada ou não configurada, a <strong> configuração do servidor do AGPM (todos os domínios) </strong> no modelo administrativo configura a conexão do servidor do AGPM.</p></td>
</tr>
</tbody>
</table>

 

### Referências adicionais

-   [Configurações de Modelo Administrativo](administrative-template-settings.md)

-   [Executar tarefas de administração de AGPM](performing-agpm-administrator-tasks.md)

 

 





