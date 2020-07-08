---
title: Usando o Windows PowerShell para administrar o MBAM 2.5
description: Usando o Windows PowerShell para administrar o MBAM 2.5
author: dansimp
ms.assetid: 64668e76-2cba-433d-8d2d-50df0a4b2997
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 8db305bfbdf79723da2b186dd5cc00406a4089cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796074"
---
# Usando o Windows PowerShell para administrar o MBAM 2.5


Este tópico descreve os cmdlets do Windows PowerShell para administração e monitoramento do Microsoft BitLocker (MBAM) relacionados à recuperação de computadores ou unidades quando os usuários são bloqueados.

Para cmdlets que você usa para configurar os recursos do MBAM Server, consulte [configurando recursos do MBAM do 2,5 usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).

## <a href="" id="cmdlets-for-recovering-computers-or-drives-that-are-managed-by-mbam-"></a>Cmdlets para recuperar computadores ou unidades que são gerenciados pelo MBAM


Use os seguintes cmdlets do Windows PowerShell para recuperar computadores ou unidades que são gerenciados pelo MBAM.

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
<td align="left"><p>Get-MbamBitLockerRecoveryKey</p></td>
<td align="left"><p>Solicita uma chave de recuperação MBAM que permite aos usuários desbloquear um computador ou unidade criptografada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamTPMOwnerPassword</p></td>
<td align="left"><p>Fornece aos usuários uma senha de proprietário do TPM que eles podem usar para desbloquear um Trusted Platform Module (TPM) quando o TPM os bloqueou e não aceitará mais o PIN.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-cmdlet-help"></a> Ajuda do cmdlet MBAM


A ajuda do Windows PowerShell para cmdlets MBAM está disponível nos seguintes formatos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Formato de ajuda do Windows PowerShell</th>
<th align="left">Mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Em um prompt de comando do Windows PowerShell, digite <strong> </strong> &lt; <em> cmdlet Get-Help</em>&gt;</p></td>
<td align="left"><p>Para carregar os cmdlets do Windows PowerShell mais recentes, siga as instruções em <a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"> Configurando os recursos do servidor do MBAM 2,5 usando o Windows PowerShell</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>No TechNet como páginas da Web</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>No centro de download como um arquivo. docx do Word</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>No centro de download como um arquivo. pdf</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 



## Tópicos relacionados


[Administrando os recursos do MBAM 2.5](administering-mbam-25-features.md)

[Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





