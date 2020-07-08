---
title: Como aplicar as configurações de rede a um espaço de trabalho do MED-V
description: Como aplicar as configurações de rede a um espaço de trabalho do MED-V
author: dansimp
ms.assetid: 641f46b3-a56f-478a-823b-1d90aa1716b3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5a13227518945e74be9e4b3772af97eadbce3fc4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799888"
---
# Como aplicar as configurações de rede a um espaço de trabalho do MED-V


Os administradores podem definir as configurações de rede para cada espaço de trabalho do MED-V.

Todas as configurações de rede são configuradas no módulo de **política** , na guia **rede** .

**Para aplicar as configurações de rede a um espaço de trabalho do MED-V**

1.  Clique no espaço de trabalho do MED-V para configurar.

2.  No painel **rede** , defina as configurações conforme descrito na tabela a seguir.

3.  No menu **política** , selecione **confirmar**.

**Propriedades da rede do espaço de trabalho do MED-V**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriedade</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Propriedades de TCP/IP</p></td>
<td align="left"><ul>
<li><p><strong>Usar o endereço IP do host (NAT) </strong> — o espaço de trabalho usará o NAT para compartilhar o IP do host para o tráfego de saída.</p></li>
<li><p><strong>Use um endereço IP diferente do host (ponte) </strong> — o espaço de trabalho do MED-V terá seu próprio endereço de rede, geralmente obtido via DHCP.</p></li>
</ul>
<p>Marque a <strong> caixa de seleção mapear vários adaptadores para espaço </strong> de trabalho quando o computador host tiver vários adaptadores. É recomendável usar essa configuração quando o host se mover entre diferentes redes usando adaptadores diferentes.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Servidor DNS</p></td>
<td align="left"><ul>
<li><p><strong>Não alterar </strong> — as configurações de DNS definidas na máquina virtual do espaço de trabalho do MED-V não serão alteradas.</p></li>
<li><p><strong>Usar o endereço DNS do host </strong> — as configurações de DNS do espaço de trabalho do MED-V serão sincronizadas para corresponder às configurações do host. A sincronização de DNS é dinâmica. Ele é sincronizado periodicamente com o host, de forma que, se ele for alterado no host, será alterado dinamicamente no espaço de trabalho do MED-V.</p></li>
<li><p><strong>Use endereços DNS específicos </strong> — o espaço de trabalho do MED-V usará um DNS específico, conforme especificado.</p>
<p>Nos <strong> campos principal </strong> e <strong> secundário </strong> , insira os endereços DNS primário e secundário.</p>
<p>Marque a <strong> caixa de seleção endereços de DNS do host de acréscimo </strong> para acrescentar o host aos endereços DNS configurados.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Atribuir sufixos DNS</p></td>
<td align="left"><ul>
<li><p><strong>Atribuir os seguintes sufixos </strong> : Marque esta caixa de seleção para atribuir sufixos DNS específicos; na caixa, insira um sufixo ou vários sufixos separados por vírgulas.</p></li>
<li><p><strong>Acrescentar sufixos </strong> de host — Marque essa caixa de seleção para acrescentar os sufixos de host ao endereço DNS.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Criando um espaço de trabalho do MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

[Usando a interface de usuário do Console de Gerenciamento do MED-V](using-the-med-v-management-console-user-interface.md)

 

 





