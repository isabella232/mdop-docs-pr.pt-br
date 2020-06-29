---
title: Como configurar o comportamento de atalhos e de associações de tipo de arquivo
description: Como configurar o comportamento de atalhos e de associações de tipo de arquivo
author: dansimp
ms.assetid: d6fd1728-4de6-4066-b36b-d4837d593d40
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84e3e0cdd43cfc26cf56f1b5ac72560b1c702ae6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797220"
---
# Como configurar o comportamento de atalhos e de associações de tipo de arquivo


A política de publicação de atalho e de associação de tipo de arquivo (FTA) é definida e controlada pelo arquivo XML de publicação, que é enviado aos clientes por um servidor de publicação durante uma operação de atualização de publicação. Quando o cliente recebe essas informações, adiciona quaisquer dados publicados recentemente sobre aplicativos como os ícones e FTAs. Em seguida, ele remove todos os dados de publicação desatualizados.

Na versão 4,6 do App-V, dois valores da chave do registro foram definidos para permitir que os administradores controlem esse comportamento. Por padrão, os atalhos criados localmente usando o console cliente agora são mantidos.

## Como alterar o comportamento do atalho e do FTA


Dois novos valores do Registro DWORD foram definidos para a chave do registro de configuração do cliente, "FileTypePolicy" e "ShortcutPolicy". Esses valores do Registro DWORD não estão presentes por padrão, mas podem ser adicionados manualmente. A chave do registro de configuração está localizada em HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\ [Wow6432Node\\\] Microsoft\\SoftGrid\\4.5\\Client\\Configuration.

Há quatro valores de política definidos na tabela a seguir, que se aplicam a ambos os valores de chave do registro. A lista a seguir mostra os valores numéricos das configurações do registro e o comportamento aplicado a tipos de arquivo ou atalhos em uma operação de atualização de publicação.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Nome</p></td>
<td align="left"><p>Tipo</p></td>
<td align="left"><p>Dados (exemplos)</p></td>
<td align="left"><p>Descrição</p></td>
</tr>
<tr class="even">
<td align="left"><p>FileTypePolicy</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 0x2 (App-V 4,6)</p></td>
<td align="left"><p>(0x0) – "ClientOnly"-remover itens existentes da mesma fonte de informações de publicação e manter somente os itens que são adicionados localmente</p>
<p>(0x1) – "ServerOnly"-Remova os itens desatualizados da mesma fonte de informações de publicação e os itens que são adicionados localmente e adicione os novos itens</p>
<p>(0x2) – "ClientAndServer"-Remova todos os itens desatualizados da mesma fonte de informações de publicação, mantenha os itens adicionados localmente e adicione os novos itens (padrão se não estiverem presentes para o App-V 4,6)</p>
<p>(0x3) – "NoChange"-não fazer alterações em tipos de arquivo ou atalhos</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ShortcutPolicy</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Padrão = 0x2</p></td>
<td align="left"><p>(0x0) – "ClientOnly"-remover itens existentes da mesma fonte de informações de publicação e manter somente os itens adicionados localmente</p>
<p>(0x1) – "ServerOnly"-Remova todos os itens desatualizados da mesma fonte de informações de publicação e itens adicionados localmente e adicione os novos itens</p>
<p>(0x2) – "ClientAndServer"-Remova todos os itens desatualizados da mesma fonte de informações de publicação, mantenha os itens adicionados localmente e adicione os novos itens (padrão, se não estiverem presentes)</p>
<p>(0x3) – "NoChange"-não fazer alterações em tipos de arquivo ou atalhos</p></td>
</tr>
</tbody>
</table>

 

**Observação**  Os valores de texto referem-se aos valores dos atributos XML no arquivo XML de publicação.Você pode definir esses valores manualmente se tiver implementado uma solução de publicação HTTP personalizada.

 

 

 





