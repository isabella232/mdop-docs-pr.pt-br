---
title: Configurações de registro em log e rastreamento
description: Configurações de registro em log e rastreamento
author: dansimp
ms.assetid: db6b43c7-fdde-4d11-b5ab-a81346e56940
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bef0f8367647aad688c2aec7586ecdaae2e22143
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797755"
---
# Configurações de registro em log e rastreamento


As configurações de modelo administrativo para gerenciamento avançado de política de grupo (AGPM) permitem que você configure centralmente as opções de log e rastreamento para servidores de AGPM e clientes para os quais um objeto de política de grupo (GPO) com essas configurações é aplicado.

A configuração a seguir está disponível em Computer Configuration\\Administrative Templates\\Windows Components\\AGPM no **Editor de objeto de política de grupo** durante a edição de um GPO no GPMC (console de gerenciamento de política de grupo). Se esse caminho não estiver visível, clique com o botão direito do mouse em **modelos administrativos**e adicione o modelo AGPM. admx ou AGPM. adm.

**Rastrear locais de arquivos**:

-   Cliente:%LocalAppData%\\Microsoft\\AGPM\\agpm.log

-   Servidor:%CommonAppData%\\Microsoft\\AGPM\\agpmserv.log

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
<td align="left"><p><strong>Log do AGPM</strong></p></td>
<td align="left"><p>Se habilitada, essa configuração define se o rastreamento está ativado e o nível de detalhes. Essa configuração afeta os componentes cliente e servidor do AGPM.</p>
<p>Se desabilitada ou não configurada, essa configuração não terá efeito.</p></td>
</tr>
</tbody>
</table>

 

### Referências adicionais

-   [Configurações de Modelo Administrativo](administrative-template-settings.md)

 

 





