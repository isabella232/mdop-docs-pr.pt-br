---
title: Administrar o MBAM 2.0 usando o PowerShell
description: Administrar o MBAM 2.0 usando o PowerShell
author: dansimp
ms.assetid: d785a8df-0a8c-4d70-abd2-93a762b4f3de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 736943e707b5d033b8ba6c26641393f02f0cdaf8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799285"
---
# Administrar o MBAM 2.0 usando o PowerShell


O monitoramento e administração do Microsoft BitLocker (MBAM) fornece o conjunto de cmdlets do Windows PowerShell listados a seguir. Os administradores podem usar estes cmdlets do PowerShell para executar várias tarefas de administração e monitoramento do Microsoft BitLocker da linha de comando, em vez de no site de administração do MBAM.

## Como administrar o MBAM usando o PowerShell


Use os cmdlets do PowerShell descritos aqui para administrar o MBAM.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Install-MBAM</p></td>
<td align="left"><p>Instala os recursos do MBAM que fornecem relatórios avançados de política, criptografia, recuperação de chave e conformidade.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Desinstalar-MBAM</p></td>
<td align="left"><p>Remove os recursos do MBAM que fornecem ferramentas avançadas de política, criptografia, recuperação de chave e relatórios de conformidade.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Get-MbamBitLockerRecoveryKey</p></td>
<td align="left"><p>Solicita uma chave de recuperação MBAM que permitirá aos usuários desbloquear um computador ou unidade criptografada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamTPMOwnerPassword</p></td>
<td align="left"><p>Fornece aos usuários uma senha de proprietário do TPM que eles podem usar para desbloquear um Trusted Platform Module (TPM) quando o TPM os bloqueou e não aceitará mais o PIN.</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Operações do MBAM 2.0](operations-for-mbam-20-mbam-2.md)

 

 





