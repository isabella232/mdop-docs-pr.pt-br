---
title: Requisitos de hardware e software do Sequencer
description: Requisitos de hardware e software do Sequencer
author: dansimp
ms.assetid: 36084e12-831d-452f-a4a4-45f07f9ce471
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d4e12a5803a3c9033513424826b49bc0bca5885
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796744"
---
# Requisitos de hardware e software do Sequencer


Este tópico descreve os requisitos mínimos de hardware e software para o computador que executa o sequenciador do Microsoft Application Virtualization (App-V).

Antes de instalar o sequenciador e depois de sequenciar cada aplicativo, você deve restaurar uma imagem limpa do sistema operacional para o computador de sequenciamento. Você pode usar um dos seguintes métodos para restaurar o computador que executa o sequenciador:

-   Reformate o disco rígido e reinstale o sistema operacional.

-   Restaure o disco rígido no computador que executa a imagem do sequenciador usando outro software de criação de imagem de disco.

A lista a seguir descreve os requisitos de hardware recomendados para executar o sequenciador do App-V.

### <a href="" id="hardware-requirements-"></a>Requisitos de Hardware

-   Processador — Intel Pentium III, 1 GHz (32 bits ou 64 bits). O processo de sequenciamento é um processo de thread único e não aproveita os dois processadores.

-   Memória: 1GB ou mais, 2 GB recomendado.

-   Disco rígido – 40 gigabytes (GB) de espaço em disco rígido com no mínimo 15 GB de espaço disponível no disco rígido. Recomendamos que você tenha pelo menos três vezes o espaço do disco rígido que o aplicativo que você está sequenciando requer.

    **Observação**  O sequenciamento requer uso intenso do disco. Uma velocidade de disco rápido pode diminuir o tempo de sequenciamento.

     

### Requisitos de software

A lista a seguir descreve os sistemas operacionais com suporte para executar o sequenciador.

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
<td align="left"><p>Professional</p></td>
<td align="left"><p>SP2 ou SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Business, Enterprise ou Ultimate</p></td>
<td align="left"><p>Sem Service Pack, SP1 ou SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>¹ do Windows7</p></td>
<td align="left"><p>Professional, Enterprise ou Ultimate</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>

 

¹ com suporte para App-V 4,5 com SP1 ou SP2 e App-V 4,6 somente

**Observação**  O sequenciador do Application Virtualization (App-V) 4,6 dá suporte a versões de 32 bits e 64 bits desses sistemas operacionais.

 

Você deve configurar os computadores que executam o sequenciador com os mesmos aplicativos instalados nos computadores de destino.

### Requisitos de software para serviços de área de trabalho remota

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
<td align="left"><p>Edição Standard, Enterprise Edition ou Datacenter Edition</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Edição Standard, Enterprise Edition ou Datacenter Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>Standard, Enterprise ou Datacenter</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>

 

**Observação**  O Application Virtualization (App-V) 4,6 para serviços de área de trabalho remota é compatível com as versões de 32 bits e de 64 bits desses sistemas operacionais.

 

## Tópicos relacionados


[Visão geral do Application Virtualization Sequencer](application-virtualization-sequencer-overview.md)

 

 





