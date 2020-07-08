---
title: Administrar o MBAM 1.0 usando PowerShell
description: Administrar o MBAM 1.0 usando PowerShell
author: dansimp
ms.assetid: 3bf2eca5-4ab7-4e84-9e80-c0c7d709647b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3547bee9b2efc58252bb6f0a1cb0aa4c484e4e80
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799612"
---
# Administrar o MBAM 1.0 usando PowerShell


O monitoramento e administração do Microsoft BitLocker (MBAM) fornece o conjunto de cmdlets do Windows PowerShell listados a seguir. Os administradores podem usar esses cmdlets do PowerShell para executar várias tarefas do MBAM Server a partir do prompt de comando, e não do site de administração do MBAM.

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
<td align="left"><p>Add-MbamHardwareType</p></td>
<td align="left"><p>Adiciona um novo modelo de hardware ao inventário de hardware do MBAM. Esse cmdlet também pode especificar se o hardware tem ou não suporte para a criptografia de unidade de disco BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamBitLockerRecoveryKey</p></td>
<td align="left"><p>Solicita uma chave de recuperação MBAM que permitirá que um usuário Desbloqueie um computador ou unidade criptografada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Get-MbamHardwareType</p></td>
<td align="left"><p>Obtém um inventário de hardware mestre que contém dados que indicam se os modelos de hardware são compatíveis ou são incompatíveis com a criptografia de unidade de disco BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamTPMOwnerPassword</p></td>
<td align="left"><p>Fornece uma senha de proprietário do TPM para um usuário gerenciar o acesso de TPM (Trusted Platform Module). Ajuda os usuários quando o TPM os bloqueou e não aceitará mais o PIN.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Install-MBAM</p></td>
<td align="left"><p>Instala os recursos do MBAM que fornecem ferramentas avançadas de política de grupo, criptografia, recuperação de chave e relatórios de conformidade.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Remove-MbamHardwareType</p></td>
<td align="left"><p>Remove os modelos de hardware do inventário de hardware.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Set-MbamHardwareType</p></td>
<td align="left"><p>Permite o gerenciamento de um inventário de hardware mestre para designar se os modelos de hardware são compatíveis ou não podem executar a criptografia BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Desinstalar-MBAM</p></td>
<td align="left"><p>Remove os recursos MBAM instalados anteriormente que fornecem ferramentas avançadas de política, criptografia, recuperação de chave e relatórios de conformidade.</p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Operações do MBAM 1.0](operations-for-mbam-10.md)

 

 





