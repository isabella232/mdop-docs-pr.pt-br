---
title: Determinando por que um dispositivo recebe uma mensagem de não conformidade
description: Determinando por que um dispositivo recebe uma mensagem de não conformidade
author: dansimp
ms.assetid: 793df330-a0ee-4759-b53a-95618ac74428
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/22/2017
ms.openlocfilehash: ce1d344676ebf4328506228f1bfa87c76e8036f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799499"
---
# Determinando por que um dispositivo recebe uma mensagem de não conformidade


Os seguintes códigos de não conformidade são fornecidos pela WMI e descrevem os motivos pelos quais um determinado dispositivo é reportado pela MBAM como não compatível.

Você pode usar o método preferencial para exibir o WMI. Se você usar o PowerShell, execute `gwmi -class mbam_volume -Namespace root\microsoft\mbam` a partir de um prompt do PowerShell e procure ReasonsForNoncompliance.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Código não compatível</th>
<th align="left">Motivo da não conformidade</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>0</p></td>
<td align="left"><p>O nível de codificação não é AES 256.</p></td>
</tr>
<tr class="even">
<td align="left"><p>um</p></td>
<td align="left"><p>A política MBAM exige que esse volume seja criptografado, mas não é.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>2</p></td>
<td align="left"><p>A política MBAM exige que esse volume não seja criptografado, mas está.</p></td>
</tr>
<tr class="even">
<td align="left"><p>3D</p></td>
<td align="left"><p>A política MBAM exige que esse volume use um protetor TPM, mas ele não faz isso.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>4</p></td>
<td align="left"><p>A política MBAM exige que esse volume use um protetor TPM + PIN, mas ele não faz isso.</p></td>
</tr>
<tr class="even">
<td align="left"><p>5</p></td>
<td align="left"><p>A política MBAM não permite que máquinas não TPM relatem como compatíveis.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>5</p></td>
<td align="left"><p>Volume tem um protetor TPM, mas o TPM não está visível (inicializado com a chave de recuperação após a desabilitação do TPM no BIOS?).</p></td>
</tr>
<tr class="even">
<td align="left"><p>7</p></td>
<td align="left"><p>A política MBAM exige que esse volume use um protetor de senha, mas ele não tem um.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>08</p></td>
<td align="left"><p>A política MBAM exige que esse volume não use um protetor de senha, mas ele tem um.</p></td>
</tr>
<tr class="even">
<td align="left"><p>222</p></td>
<td align="left"><p>A política MBAM exige que este volume use um protetor de desbloqueio automático, mas ele não tem um.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>254</p></td>
<td align="left"><p>A política MBAM requer que esse volume não use um protetor de desbloqueio automático, mas tenha um.</p></td>
</tr>
<tr class="even">
<td align="left"><p>11:00</p></td>
<td align="left"><p>Conflito de política detectado impedindo que o MBAM relate esse volume como compatível.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>12</p></td>
<td align="left"><p>Um volume do sistema é necessário para criptografar o volume do sistema operacional, mas ele não está presente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>0,13</p></td>
<td align="left"><p>Proteção suspensa para o volume.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>quatorze</p></td>
<td align="left"><p>Autodesbloquear não seguro, a menos que o volume do sistema operacional seja criptografado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>15</p></td>
<td align="left"><p>A política requer força mínima de Cypher é XTS-AES-128 bit, o nível real de Cypher é mais fraco do que isso.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>16</p></td>
<td align="left"><p>A política requer força mínima de Cypher é XTS-AES-256 bit, o nível real de Cypher é mais fraco do que isso.</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Referência técnica do MBAM 2.5](technical-reference-for-mbam-25.md)

[Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 
## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





