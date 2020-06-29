---
title: Como permitir que apenas administradores habilitem grupos de conexão
description: Como permitir que apenas administradores habilitem grupos de conexão
author: dansimp
ms.assetid: 42ca3157-5d85-467b-a148-09404f8f737a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 083d6386f02996d35255f90958705798f2cd5fb9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796503"
---
# Como permitir que apenas administradores habilitem grupos de conexão


Você pode configurar o cliente App-V para que somente administradores (não usuários finais) possam habilitar ou desabilitar grupos de conexão. Em versões anteriores do App-V, você não pode impedir que os usuários finais executem essas tarefas.

**Observação** 
 **Este recurso tem suporte a partir do App-V 5,0 SP3.**

 

Use um dos seguintes métodos para permitir que apenas administradores habilitem ou desabilitem grupos de conexão.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Etapas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configuração da Política de Grupo</p></td>
<td align="left"><p>Habilite a configuração da política de grupo "exigir publicação como administrador", localizada no seguinte nó de objeto de política de Grupo:</p>
<p><strong>Política de configuração do computador &gt; &gt; modelos administrativos do &gt; &gt; App-V &gt; Publishing</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Cmdlet do PowerShell</p></td>
<td align="left"><p>Execute o <strong> cmdlet Set-AppvClientConfiguration </strong> com o <strong> parâmetro – RequirePublishAsAdmin </strong> .</p>
<p>Valores de parâmetro:</p>
<ul>
<li><p>0-falso</p></li>
<li><p>1-verdadeiro</p></li>
</ul>
<p><strong>Exemplo: </strong> : Set-AppvClientConfiguration – RequirePublishAsAdmin1</p></td>
</tr>
</tbody>
</table>

 

**Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Gerenciando grupos de conexão](managing-connection-groups51.md)

 

 





