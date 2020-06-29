---
title: Configurações com suporte no MED-V 1.0 SP1
description: Configurações com suporte no MED-V 1.0 SP1
author: dansimp
ms.assetid: 4dcf37c4-a061-43d2-878c-28efc87c3cdd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5a707e8a3d59a423308f9f735ff38df9e235fbf5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799418"
---
# Configurações com suporte no MED-V 1.0 SP1


Este tópico especifica os requisitos necessários para instalar e executar o Microsoft Enterprise Desktop Virtualization (MED-V) 1,0 Service Pack 1 (SP1) no seu ambiente.

## Requisitos do sistema do cliente do MED-V 1,0 SP1


### Requisitos do sistema operacional do cliente MED-V

A tabela a seguir lista os sistemas operacionais suportados para a instalação do cliente do MED-V 1,0 SP1.

**Observação**  
A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior. Para encontrar os cronogramas de suporte para o seu produto, consulte o [ciclo de vida dos pacotes de serviços compatíveis do ciclo de vida](https://go.microsoft.com/fwlink/?LinkId=31975) ( https://go.microsoft.com/fwlink/?LinkId=31975) . Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [política de suporte do ciclo de vida do suporte Microsoft Support](https://go.microsoft.com/fwlink/?LinkId=31976) https://go.microsoft.com/fwlink/?LinkId=31976)



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operacional</th>
<th align="left">Edição</th>
<th align="left">Service Pack</th>
<th align="left">Arquitetura do sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows XP</p></td>
<td align="left"><p>Edição Professional</p></td>
<td align="left"><p>SP2 ou SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Business, Enterprise ou Ultimate</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Professional, Enterprise ou Ultimate</p></td>
<td align="left"><p>Nenhum(a)</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
</tbody>
</table>



**Observação**  
O cliente MED-V não é executado no modo x64 nativo. Em vez disso, o MED-V funciona no modo WOW64 (Windows 64-bit) em computadores de 64 bits.



A tabela a seguir lista a RAM mínima necessária para cada sistema operacional compatível com o MED-V 1,0 SP1.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operacional</th>
<th align="left">RAM mínima necessária</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows XP Professional</p></td>
<td align="left"><p>1 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>2 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7 x86</p></td>
<td align="left"><p>2 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 7 x64</p></td>
<td align="left"><p>3 GB</p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-sp1-client-configuration-"></a>Configuração do cliente do MED-V 1,0 SP1

**Versão do .NET Framework**

As seguintes versões do Microsoft .NET Framework têm suporte para a instalação do cliente do MED-V 1,0 SP1:

-   .NET Framework 2,0 ou .NET Framework 2,0 SP1

-   .NET Framework 3,0 ou .NET Framework 3,0 SP1

-   .NET Framework 3,5 ou .NET Framework 3,5 SP1

**Mecanismo de virtualização**

Microsoft Virtual PC 2007 SP1 com o hotfix descrito no artigo da base de dados de conhecimento Microsoft 974918 tem suporte para a instalação do cliente MED-V 1,0 SP1 nas seguintes configurações:

-   Arquivo de disco rígido virtual estático (VHD)

-   Vários arquivos VHD localizados no mesmo diretório

-   Arquivo VHD dinâmico

**Navegador da Internet**

O Windows Internet Explorer 7 e o Windows Internet Explorer 8 têm suporte para a instalação do cliente do MED-V 1,0 SP1.

**Microsoft Hyper-V Server**

O cliente MED-V não é compatível com um ambiente do Microsoft Hyper-V Server.

## Requisitos do sistema do espaço de trabalho do MED-V 1,0 SP1


O MED-V 1,0 SP1 introduz mudanças nos requisitos do sistema daqueles do MED-V 1,0.

### Requisitos do sistema operacional do espaço de trabalho do MED-V

A tabela a seguir lista os sistemas operacionais suportados para os espaços de trabalho do MED-V 1,0 SP1.

**Observação**  
A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior. Para encontrar os cronogramas de suporte para o seu produto, consulte o [ciclo de vida dos pacotes de serviços compatíveis do ciclo de vida](https://go.microsoft.com/fwlink/?LinkId=31975) ( https://go.microsoft.com/fwlink/?LinkId=31975) . Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [política de suporte do ciclo de vida do suporte Microsoft Support](https://go.microsoft.com/fwlink/?LinkId=31976) https://go.microsoft.com/fwlink/?LinkId=31976)



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operacional</th>
<th align="left">Edição</th>
<th align="left">Service Pack</th>
<th align="left">Arquitetura do sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 2000</p></td>
<td align="left"><p>Professional</p></td>
<td align="left"><p>4</p></td>
<td align="left"><p>X86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows XP</p></td>
<td align="left"><p>Edição Professional</p></td>
<td align="left"><p>SP2 ou SP3</p>
<div class="alert">
<strong>Observação</strong><br/><p>O SP3 é recomendado para garantir que o espaço de trabalho do MED-V seja compatível com futuras versões do MED-V.</p>
</div>
<div>

</div></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-sp1-workspace-configuration-"></a>Configuração do espaço de trabalho do MED-V 1,0 SP1

**Versão do .NET Framework**

O MED-V requer uma das seguintes versões compatíveis do Microsoft .NET Framework para a instalação do espaço de trabalho do MED-V 1,0 SP1:

-   .NET Framework 2,0 SP1

-   .NET Framework 3,0 SP1

-   .NET Framework 3,5 ou .NET Framework 3,5 SP1

**Observação**  
Recomendamos o .NET Framework 3,5 SP1 para garantir que o espaço de trabalho do MED-V seja compatível com futuras versões do MED-V.



**Navegador da Internet**

O Windows Internet Explorer 6 SP2 e o Windows Internet Explorer 7 têm suporte para a instalação do espaço de trabalho do MED-V 1,0 SP1.

### <a href="" id="med-v-workspace-images-"></a>Imagens do espaço de trabalho do MED-V

As imagens do espaço de trabalho do MED-V devem ser criadas usando o Virtual PC 2007 SP1.

## Requisitos do sistema do servidor MED-V 1,0 SP1


O MED-V 1,0 SP1 introduz mudanças nos requisitos do sistema daqueles do MED-V 1,0.

### Requisitos do sistema operacional do MED-V 1,0 Server

A tabela a seguir lista os sistemas operacionais suportados para instalações do servidor MED-V 1,0 SP1.

**Observação**  
A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior. Para encontrar os cronogramas de suporte para o seu produto, consulte o [ciclo de vida dos pacotes de serviços compatíveis do ciclo de vida](https://go.microsoft.com/fwlink/?LinkId=31975) ( https://go.microsoft.com/fwlink/?LinkId=31975) . Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [política de suporte do ciclo de vida do suporte Microsoft Support](https://go.microsoft.com/fwlink/?LinkId=31976) https://go.microsoft.com/fwlink/?LinkId=31976)



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operacional</th>
<th align="left">Edição</th>
<th align="left">Service Pack</th>
<th align="left">Arquitetura do sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server 2008</p></td>
<td align="left"><p>Standard ou Enterprise</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>X86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Standard ou Enterprise</p></td>
<td align="left"><p>Nenhum(a)</p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-sp1-server-configuration-"></a>Configuração do servidor do MED-V 1,0 SP1

**Versão do .NET Framework**

O MED-V requer uma das seguintes versões compatíveis do Microsoft .NET Framework para a instalação do espaço de trabalho do MED-V 1,0 SP1:

-   .NET Framework 2,0 ou .NET Framework 2,0 SP1

-   .NET Framework 3,0 ou .NET Framework 3,0 SP1

-   .NET Framework 3,5 ou .NET Framework 3,5 SP1

**Microsoft SQL Server versão**

As seguintes versões do Microsoft SQL Server são compatíveis com o MED-V 1,0 SP1 quando o SQL Server é instalado localmente ou remotamente do servidor MED-V 1,0 SP1:

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versão do SQL Server</th>
<th align="left">Edição</th>
<th align="left">Service Pack</th>
<th align="left">Arquitetura do sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SQL Server 2005</p></td>
<td align="left"><p>Edição expressa, padrão ou Enterprise</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>X86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server 2008</p></td>
<td align="left"><p>Express, Standard ou Enterprise</p></td>
<td align="left"><p>Nenhum(a)</p></td>
<td align="left"><p>X86 ou x64</p></td>
</tr>
</tbody>
</table>



**Microsoft Hyper-V Server**

O servidor MED-V é compatível com um ambiente do Microsoft Hyper-V Server.

## Informações de globalização do MED-V 1,0 SP1


Embora o MED-V não seja liberado em idiomas diferentes do inglês, as seguintes versões do idioma do sistema operacional Windows são compatíveis com o cliente do MED-V 1,0 SP1, o espaço de trabalho e as instalações do servidor:

-   Inglês

-   Francês

-   Alemão

-   Italiano

-   Espanhol

-   Português (Brasil)

-   Holandês (Países Baixos)

-   Japonês









