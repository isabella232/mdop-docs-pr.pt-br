---
title: Requisitos de Sistema do Application Virtualization
description: Requisitos de Sistema do Application Virtualization
author: dansimp
ms.assetid: a2798dd9-168e-45eb-8103-e12e128fae7c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c160a7532b521bb41570b419b22b9e7daaec2987
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797541"
---
# Requisitos de Sistema do Application Virtualization


Este tópico descreve os requisitos mínimos de hardware e software para o servidor de gerenciamento do Microsoft Application Virtualization (App-V) e o Streaming Server.

## Servidores de gerenciamento e streaming do Application Virtualization


A lista a seguir inclui os requisitos mínimos de hardware e software para o servidor de gerenciamento do App-V e do App-V Streaming Server.

### Requisitos de Hardware

-   Processador — Intel Pentium III, 1 GHz

-   RAM — 512 MB

-   Espaço em disco — 200 MB de espaço disponível no disco rígido, não incluindo o diretório de conteúdo

### Requisitos de software

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
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Edição padrão</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Edição Enterprise ou Datacenter Edition</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Edição padrão</p></td>
<td align="left"><p>Sem Service Pack ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Edição Enterprise ou Datacenter Edition</p></td>
<td align="left"><p>Sem Service Pack ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter Edition</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ aplica-se somente ao App-V 4,5 SP1 e SP2.

## Repositório de dados


A lista a seguir inclui os requisitos mínimos de hardware e software para o computador que é usado quando você instala o repositório de dados em um servidor separado. O repositório de dados é necessário apenas para o servidor de gerenciamento do Application Virtualization.

### Requisitos de Hardware

-   Processador — Intel Pentium III, 850 MHz

-   RAM — 512 MB

-   Espaço em disco — 200 MB de espaço disponível no disco rígido

### Requisitos de software

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
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Edição padrão</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Edição Enterprise ou Datacenter Edition</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Edição padrão</p></td>
<td align="left"><p>Sem Service Pack ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Edição Enterprise ou Datacenter Edition</p></td>
<td align="left"><p>Sem Service Pack ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter Edition</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ aplica-se somente ao App-V 4,5 SP1 e SP2.

-   Banco de dados — Microsoft SQL Server2000 SP3a ou SP4, SQL Server2005 SP1, SP2 ou SP3, ou SQL Server2008, sem Service Pack ou SP1 ou SQL Server2008 R2 (32 bits ou 64 bits)

-   Componentes do Microsoft Data Access – MDAC 2,7

-   Controlador de domínio — Active Directory Domain Services ou Primary Domain Controller (PDC) baseado em Windows NT 4.0 como a autoridade de autenticação central

## Serviço Web de gerenciamento


A lista a seguir inclui os requisitos mínimos de hardware e software para o serviço Web de gerenciamento do Application Virtualization quando ele é instalado em um computador separado.

### Requisitos de Hardware

-   Processador — Intel Pentium III, 800 MHz

-   RAM — 256 MB

-   Espaço em disco – 50 MB de espaço disponível no disco rígido

### Requisitos de software

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
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Edição padrão</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Edição Enterprise ou Datacenter Edition</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Edição padrão</p></td>
<td align="left"><p>Sem Service Pack ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Edição Enterprise ou Datacenter Edition</p></td>
<td align="left"><p>Sem Service Pack ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter Edition</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ aplica-se somente ao App-V 4,5 SP1 e SP2.

-   Serviços de informações da Internet (IIS) 6,0 configurado com o Microsoft ASP.NET, IIS 7

-   Microsoft .NET Framework 2.0

## Console de gerenciamento


A lista a seguir inclui os requisitos mínimos de hardware e software recomendados para o console de gerenciamento do Application Virtualization quando ele é instalado em um computador separado.

### Requisitos de Hardware

-   Processador — Intel Pentium III, 450 MHz

-   RAM — 256 MB

-   Espaço em disco — 200 MB de espaço disponível no disco rígido

### Requisitos de software

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
<td align="left"><p>Pacote</p></td>
<td align="left"><p>Edição Professional</p></td>
<td align="left"><p>SP2 ou SP3</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Business, Enterprise ou Ultimate Edition</p></td>
<td align="left"><p>Sem Service Pack, SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>7</p></td>
<td align="left"><p>Professional, Enterprise ou Ultimate Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Edição Standard, Enterprise Edition ou Datacenter Edition</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Edição Standard, Enterprise Edition ou Datacenter Edition</p></td>
<td align="left"><p>Sem Service Pack ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter Edition</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 R2 ¹</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ aplica-se somente ao App-V 4,5 SP1 e SP2.

-   Console de gerenciamento Microsoft — MMC 3.0 ou posterior

-   Microsoft .NET Framework 2.0 SP2 (mínimo)

    **Importante**  O requisito mínimo é o .NET Framework 2,0 SP2 se você precisar instalar o hotfix do App-V KB980850 ou hotfixes do App-V subsequentes no computador que está executando o console de gerenciamento do App-V.

     

## Tópicos relacionados


[Requisitos de Hardware e Software do Application Virtualization Client](application-virtualization-client-hardware-and-software-requirements.md)

[Requisitos de Hardware e Software do Application Virtualization Sequencer](application-virtualization-sequencer-hardware-and-software-requirements.md)

[Como configurar os servidores para a implantação baseada em servidor](how-to-configure-servers-for-server-based-deployment.md)

[Como instalar os componentes de servidores e do sistema](how-to-install-the-servers-and-system-components.md)

[Como fazer upgrade dos componentes de servidores e do sistema](how-to-upgrade-the-servers-and-system-components.md)

 

 





