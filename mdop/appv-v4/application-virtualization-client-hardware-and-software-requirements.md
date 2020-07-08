---
title: Requisitos de Hardware e Software do Application Virtualization Client
description: Requisitos de Hardware e Software do Application Virtualization Client
author: dansimp
ms.assetid: 8b877a2c-5721-4b22-a47f-e2838d58ab12
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5b828f59ba36099b4f6a545cd5bbcb3c72d24e3e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797584"
---
# Requisitos de Hardware e Software do Application Virtualization Client


Este tópico descreve a configuração mínima de hardware e software recomendada para a instalação do cliente de desktop do Application Virtualization e do cliente do Application Virtualization para serviços de área de trabalho remota (antes serviços de terminal).

## Cliente de desktop do Application Virtualization


A lista a seguir inclui os requisitos mínimos de hardware e software para o cliente da área de trabalho do Application Virtualization. Os requisitos são listados primeiro para Microsoft Application Virtualization (App-V) 4.6 SP2, seguido pelos requisitos para versões que precedem o App-V 4.6 SP2.

**Observação**  O cliente da área de trabalho do Application Virtualization (App-V) não exige nenhum processador adicional ou recursos de RAM além dos requisitos do sistema operacional do host.

 

### Requisitos de Hardware

Os requisitos de hardware são aplicáveis a todas as versões.

-   Processador — Veja os requisitos de sistema recomendados para o sistema operacional que você está usando.

-   RAM — Veja os requisitos de sistema recomendados para o sistema operacional que você está usando.

-   Disco — 30MB para instalação e 6GB para o cache.

### Requisitos de software para o App-V 4,6 SP2

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
<th align="left">SKU da arquitetura</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Pacote</p></td>
<td align="left"><p>Edição Professional</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Business, Enterprise ou Ultimate Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>7</p></td>
<td align="left"><p>Professional, Enterprise ou Ultimate Edition</p></td>
<td align="left"><p>Sem Service Pack ou SP1</p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>Edição pro ou Enterprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
</tbody>
</table>

Os seguintes pré-requisitos de software são instalados automaticamente se você estiver usando o método Setup.exe. Se você estiver usando o programa de instalação do Setup.msi, os seguintes produtos devem ser instalados primeiro.
- **Microsoft Visual c++ 2005 SP1 Redistributable Package (x86)**— para obter mais informações sobre como instalar o Microsoft visual C++ 2005 SP1 Redistributable Package (x86), consulte [microsoft Visual c++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) ( https://go.microsoft.com/fwlink/?LinkId=119961) . Para a versão 4,5 SP2 do aplicativo App-V, baixe Vcredist\_x86.exe do [pacote redistribuível da atualização de segurança do Microsoft Visual C++ 2005 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360) .
  -   **Microsoft Core XML Services (MSXML) 6,0 SP1 (x86)**— para obter mais informações sobre como instalar o Microsoft Core XML Services (msxml) 6,0 SP1 (x86), consulte [Microsoft Core XML Services (MSXML) 6,0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) ( https://go.microsoft.com/fwlink/?LinkId=63266) .

Para o cliente da área de trabalho do Application Virtualization (App-V) 4,6, o seguinte pré-requisito de software adicional será instalado automaticamente se você estiver usando o método Setup.exe. Se você estiver usando o programa de instalação do Setup.msi, também deverá instalar com os outros pré-requisitos listados.

-   **Pacote redistribuível do Microsoft VisualC + + 2008SP1 (x86)**-para obter mais informações sobre como instalar o Microsoft VisualC + + 2008 SP1 Redistributable Package (x86), consulte [Microsoft VisualC + + 2008 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=150700) ( https://go.microsoft.com/fwlink/?LinkId=150700) .

### Requisitos de software para versões que precedem o App-V 4,6 SP2

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
<th align="left">SKU da arquitetura</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Pacote</p></td>
<td align="left"><p>Edição Professional</p></td>
<td align="left"><p>SP2 ou SP3</p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Business, Enterprise ou Ultimate Edition</p></td>
<td align="left"><p>Sem Service Pack, SP1 ou SP2</p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>¹ do Windows7</p></td>
<td align="left"><p>Professional, Enterprise ou Ultimate Edition</p></td>
<td align="left"><p>Sem Service Pack ou SP1</p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
</tbody>
</table>
¹ com suporte para App-V 4,5 SP1 e SP2, App-V 4,6 e 4,6 SP1 somente

O cliente da área de trabalho do Application Virtualization (App-V) 4,6 dá suporte a SKUs x86 e x64 desses sistemas operacionais.

Os seguintes pré-requisitos de software são instalados automaticamente se você estiver usando o método Setup.exe. Se você estiver usando o programa de instalação do Setup.msi, os seguintes produtos devem ser instalados primeiro.

-   <strong>Microsoft Visual C++ 2005 SP1 Redistributable Package (x86) </strong> — para obter mais informações sobre como instalar o Microsoft Visual c++ 2005 SP1 Redistributable Package (x86), consulte <a href="https://go.microsoft.com/fwlink/?LinkId=119961" data-raw-source="[Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961)"> Microsoft visual C++ 2005 SP1 Redistributable Package (x86) </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=119961" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=119961"> https://go.microsoft.com/fwlink/?LinkId=119961 </a> ). Para a versão 4,5 SP2 do aplicativo App-V, baixe o Vcredist_x86.exe da <a href="https://go.microsoft.com/fwlink/?LinkId=169360" data-raw-source="[Microsoft Visual C++ 2005 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=169360)"> atualização de segurança ATL do pacote redistribuível do Microsoft Visual C++ 2005 Service Pack 1 </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=169360" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=169360"> https://go.microsoft.com/fwlink/?LinkId=169360 </a> ).

-   <strong>Microsoft Core XML Services (MSXML) 6,0 SP1 (x86) </strong> — para obter mais informações sobre como instalar o Microsoft Core XML Services (MSXML) 6,0 SP1 (x86), consulte <a href="https://go.microsoft.com/fwlink/?LinkId=63266" data-raw-source="[Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266)"> Microsoft Core XML Services (msxml) 6,0 SP1 (x86) </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=63266" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=63266"> https://go.microsoft.com/fwlink/?LinkId=63266 </a> ).

-   <strong>Relatório de erros do aplicativo Microsoft </strong> – o programa de instalação deste software está incluído <strong> na </strong> pasta Support\Watson no arquivo compactado de auto-extração.

Para o cliente da área de trabalho do Application Virtualization (App-V) 4,6, o seguinte pré-requisito de software adicional será instalado automaticamente se você estiver usando o método Setup.exe. Se você estiver usando o programa de instalação do Setup.msi, também deverá instalar com os outros pré-requisitos listados.

-   <strong>Microsoft Visual C++ 2008 SP1 Redistributable Package (x86) </strong> — para obter mais informações sobre como instalar o Microsoft Visual c++ 2008 SP1 Redistributable Package (x86), consulte <a href="https://go.microsoft.com/fwlink/?LinkId=150700" data-raw-source="[Microsoft Visual C++ 2008 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=150700)"> Microsoft visual C++ 2008 SP1 Redistributable Package (x86) </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=150700" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=150700"> https://go.microsoft.com/fwlink/?LinkId=150700 </a> ).

## Cliente do Application Virtualization para serviços de área de trabalho remota

Veja a seguir os requisitos de hardware e software recomendados para o cliente do Application Virtualization para serviços de área de trabalho remota. Os requisitos são listados primeiro para appv461_3 e, em seguida, os requisitos para versões que antecedem o App-V 4,6 SP2.

O cliente do Application Virtualization (App-V) para serviços de área de trabalho remota não requer nenhum processador adicional ou recursos de RAM além dos requisitos do sistema operacional do host.

### Requisitos de Hardware

Os requisitos de hardware são aplicáveis a todas as versões.

-   Processador — Veja os requisitos de sistema recomendados para o sistema operacional que você está usando.

-   RAM — Veja os requisitos de sistema recomendados para o sistema operacional que você está usando. Esses requisitos também dependem do número de usuários e aplicativos.

-   Disco — 30MB para instalação e 6GB para o cache.

### Requisitos de software para o App-V 4,6 SP2

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
<th align="left">SKU da arquitetura</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Edição Standard, Enterprise Edition ou Datacenter Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter Edition</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter Edition</p></td>
<td align="left"><p>Sem Service Pack ou SP1</p></td>
<td align="left"><p>x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

Os seguintes pré-requisitos de software são instalados automaticamente se você estiver usando o método Setup.exe. Se você estiver usando o programa de instalação do Setup.msi, os seguintes produtos devem ser instalados primeiro.

-   **Pacote redistribuível do Microsoft VisualC + + 2005SP1 (x86)**-para obter mais informações sobre como instalar o Microsoft VisualC + + 2005 SP1 Redistributable Package (x86), consulte [Microsoft VisualC + + 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) ( https://go.microsoft.com/fwlink/?LinkId=119961) . Para a versão 4.5 SP2 do aplicativo App-V, baixe Vcredist\_x86.exe do [Microsoft Visual C++ 2005 Service Pack 1 pacote redistribuível pacote de segurança ATL Update](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360) .

-   **Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)**— para obter mais informações sobre como instalar o Microsoft Core XML Services (MSXML) 6.0 SP1 (x86), consulte [Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) ( https://go.microsoft.com/fwlink/?LinkId=63266) .

-   **Relatório de erros do aplicativo Microsoft**– o programa de instalação deste software está incluído na pasta **Support\\Watson** no arquivo compactado de auto-extração.

Para o cliente da área de trabalho do Application Virtualization (App-V) 4,6, o seguinte pré-requisito de software adicional será instalado automaticamente se você estiver usando o método Setup.exe. Se você estiver usando o programa de instalação do Setup.msi, também deverá instalar com os outros pré-requisitos listados.

-   **Pacote redistribuível do Microsoft VisualC + + 2008SP1 (x86)**-para obter mais informações sobre como instalar o Microsoft VisualC + + 2008 SP1 Redistributable Package (x86), consulte [Microsoft VisualC + + 2008 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=150700) ( https://go.microsoft.com/fwlink/?LinkId=150700) .

### Requisitos de software para versões que precedem o App-V 4,6 SP2

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
<th align="left">SKU da arquitetura</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Edição Standard, Enterprise Edition ou Datacenter Edition</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Edição Standard, Enterprise Edition ou Datacenter Edition</p></td>
<td align="left"><p>Sem Service Pack ou SP2</p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter Edition</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 e x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter Edition</p></td>
<td align="left"><p>Sem Service Pack ou SP1</p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

O cliente do Application Virtualization (App-V) 4,6 para serviços de área de trabalho remota dá suporte a SKUs x86 e x64 desses sistemas operacionais.

## Tópicos relacionados
- [Requisitos de Hardware e Software do Application Virtualization Sequencer](application-virtualization-sequencer-hardware-and-software-requirements.md)
- [Requisitos de Sistema do Application Virtualization](application-virtualization-system-requirements.md)
- [Como instalar o cliente usando a linha de comando](how-to-install-the-client-by-using-the-command-line-new.md)
- [Como instalar manualmente o Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)
- [Como fazer upgrade do Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)
