---
title: Configurações de registro em log e rastreamento
description: Configurações de registro em log e rastreamento
author: dansimp
ms.assetid: 858b6fbf-65b4-42fa-95a9-69b04e5734d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 078bda16b5fcf968d45e0c4890487471105e8c44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797756"
---
# Configurações de registro em log e rastreamento


As configurações de modelo administrativo para gerenciamento avançado de política de grupo (AGPM) permitem que você configure centralmente as opções de log e rastreamento para servidores de AGPM e clientes para os quais um objeto de política de grupo (GPO) com essas configurações é aplicado.

A configuração a seguir está disponível em Computer Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM ao editar um GPO.

**Rastrear locais de arquivos**:

-   Cliente:%LocalAppData%\\Microsoft\\AGPM\\agpm.log

-   Servidor:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log

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
<td align="left"><p><strong>AGPM: configurar o log</strong></p></td>
<td align="left"><p>Essa configuração de política permite ativar e configurar o registro em log para AGPM. Essa configuração afeta os componentes cliente e servidor do AGPM.</p></td>
</tr>
</tbody>
</table>

 

### Referências adicionais

-   [Pasta Modelos Administrativos](administrative-templates-folder-agpm30ops.md)

 

 





