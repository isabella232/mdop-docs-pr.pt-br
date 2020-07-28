---
title: Novidades do AGPM 4.0 SP3
description: Novidades do AGPM 4.0 SP3
author: dansimp
ms.assetid: df495d55-9fbf-4f7e-a7af-3905f4f8790e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 44e7dc6c5de75ae3a5e5def638974bae20ad2a1e
ms.sourcegitcommit: 594b6e431af98562e0b806e224d2c5c7e07d2c77
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/27/2020
ms.locfileid: "10895761"
---
# Novidades do AGPM 4.0 SP3


Este conteúdo descreve melhorias e configurações com suporte para o serviço de gerenciamento de política de grupo avançado (AGPM) 4.0 da Microsoft Pack3 (SP3). Se houver uma diferença entre esse conteúdo e outra documentação do AGPM, considere esse conteúdo autoritativo e assuma que ele substitui a outra documentação.

## <a href="" id="what-s-new"></a>O que há de novo


O AGPM 4.0 SP3 é compatível com os recursos e funcionalidades a seguir.

### Suporte para Windows10

O AGPM 4.0 SP3 adiciona suporte para os sistemas operacionais Windows10 e Windows Server 2016.

### Suporte para o PowerShell

O AGPM 4.0 SP3 adiciona suporte para cmdlets do PowerShell. Para obter uma lista dos cmdlets disponíveis no AGPM 4.0 SP3, incluindo descrições e sintaxe, consulte [automação do Microsoft Desktop Optimization Pack with Windows PowerShell](https://docs.microsoft.com/powershell/mdop/get-started?view=win-mdop2-ps).

### Feedback do cliente e pacote cumulativo de hotfix

O AGPM 4,0 SP3 inclui um ROLLUP de todas as correções até e incluindo o gerenciamento avançado de política de grupo da Microsoft 4,0 SP2 e quaisquer correções para problemas encontrados desde o AGPM 4,0 SP2.

### Capacidade de atualizar para o AGPM 4.0 SP3 sem digitar novamente os parâmetros de configuração

Você pode atualizar o cliente do AGPM ou o servidor do AGPM para o AGPM 4.0 SP3 sem ser solicitado a digitar novamente os parâmetros de configuração (chamado de atualização inteligente) apenas do AGPM 4.0 e posterior, conforme mostrado na tabela a seguir. Se você estiver atualizando para o AGPM 4.0 SP3 de outras versões do AGPM, conforme mostrado na tabela, você deve usar a atualização clássica, que exige que você insira novamente os parâmetros de configuração. Como cada versão do AGPM está associada a um sistema operacional específico, consulte [escolhendo qual versão do AGPM instalar](https://go.microsoft.com/fwlink/?LinkId=254350) e certifique-se de atualizar o sistema operacional conforme apropriado antes de atualizar o AGPM.

**Atualizações compatíveis com o AGPM 4,0 SP3**

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Versão do AGPM a partir da qual você pode atualizar</strong></p></td>
<td align="left"><p><strong>2,5</strong></p></td>
<td align="left"><p><strong>3,0</strong></p></td>
<td align="left"><p><strong>4,0</strong></p></td>
<td align="left"><p><strong>4,0 SP1</strong></p></td>
<td align="left"><p><strong>4,0 SP2</strong></p></td>
<td align="left"><p><strong>4,0 SP3</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>2,5</p></td>
<td align="left"><p>Não Aplicável</p></td>
<td align="left"><p>Atualização clássica</p></td>
<td align="left"><p>Atualização clássica</p></td>
<td align="left"><p>A instalação está bloqueada</p></td>
<td align="left"><p>A instalação está bloqueada</p></td>
<td align="left"><p>A instalação está bloqueada</p></td>
</tr>
<tr class="odd">
<td align="left"><p>3,0</p></td>
<td align="left"><p>Não Aplicável</p></td>
<td align="left"><p>Não Aplicável</p></td>
<td align="left"><p>Atualização clássica</p></td>
<td align="left"><p>A instalação está bloqueada</p></td>
<td align="left"><p>A instalação está bloqueada</p></td>
<td align="left"><p>A instalação está bloqueada</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,0</p></td>
<td align="left"><p>Não Aplicável</p></td>
<td align="left"><p>Não Aplicável</p></td>
<td align="left"><p>Não Aplicável</p></td>
<td align="left"><p>Atualização inteligente</p></td>
<td align="left"><p>Atualização inteligente</p></td>
<td align="left"><p>Atualização inteligente</p></td>
</tr>
<tr class="odd">
<td align="left"><p>4,0 SP1</p></td>
<td align="left"><p>Não Aplicável</p></td>
<td align="left"><p>Não Aplicável</p></td>
<td align="left"><p>Não Aplicável</p></td>
<td align="left"><p>Não Aplicável</p></td>
<td align="left"><p>Atualização inteligente</p></td>
<td align="left"><p>Atualização inteligente</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,0 SP2</p></td>
<td align="left"><p>Não Aplicável</p></td>
<td align="left"><p>Não Aplicável</p></td>
<td align="left"><p>Não Aplicável</p></td>
<td align="left"><p>Não Aplicável</p></td>
<td align="left"><p>Não Aplicável</p></td>
<td align="left"><p>Atualização inteligente</p></td>
</tr>
</tbody>
</table>

 

## Configurações compatíveis


O AGPM 4.0 SP3 dá suporte às configurações da tabela a seguir. Embora o AGPM dê suporte a configurações mistas, recomendamos que você execute o cliente do AGPM e o servidor do AGPM na mesma linha do sistema operacional, por exemplo, Windows10 com Windows Server 2016, Windows 8,1 com Windows Server 2012 R2 e assim por diante.

**Configurações de política e sistemas operacionais compatíveis com o AGPM 4.0 SP3**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Configurações com suporte para o servidor do AGPM</strong></th>
<th align="left"><strong>Configurações com suporte para o cliente do AGPM</strong></th>
<th align="left"><strong>Suporte do AGPM</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server 2019 ou Windows 10</p></td>
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Suportado</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2016 ou Windows 10</p></td>
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Suportado</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2 ou Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 ou Windows 8.1</p></td>
<td align="left"><p>Com suporte</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012 ou Windows 8.1</p></td>
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8.1</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 ou Windows7</p></td>
<td align="left"><p>Windows Server2008R2 ou Windows7</p></td>
<td align="left"><p>Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8.1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 ou Windows 7</p></td>
<td align="left"><p>Windows Server2008 ou WindowsVista com Service Pack 1 (SP1)</p></td>
<td align="left"><p>Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server2012 R2, no Windows Server 2012, no Windows Server2008R2, no Windows 8.1 ou no Windows7</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2 ou Windows 7</p></td>
<td align="left"><p>Sem suporte</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Com suporte, mas não pode relatar ou editar configurações de política ou itens de preferência que existem somente no Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows 8.1</p></td>
</tr>
</tbody>
</table>

 

## Pré-requisitos para a instalação do AGPM 4.0 SP3

A tabela a seguir descreve o comportamento dos instaladores do cliente e do servidor do AGPM 4.0 SP3 quando o .NET Framework 4.5.1, o PowerShell 3,0 ou o GPMC nas ferramentas de administração do servidor remoto estão ausentes.

| Cliente do AGPM            |                                                                                                 |                                                                            | Servidor do AGPM                                                                     |                                                                                                 |                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Sistema operacional       | .NET Framework                                                                                  | PowerShell                                                                 | Ferramentas de Administração de Servidor Remoto                                              | .NET Framework                                                                                  | Ferramentas de Administração de Servidor Remoto                                              |
| Windows 10             | Se o .NET Framework 4.5.1 não estiver habilitado ou instalado, o instalador bloqueará a instalação. | Se o PowerShell 3,0 não estiver instalado, o instalador bloqueará a instalação. | Se o GPMC não estiver habilitado ou instalado, o instalador bloqueará a instalação. | Se o .NET Framework 4.5.1 não estiver habilitado ou instalado, o instalador bloqueará a instalação. | Se o GPMC não estiver habilitado ou instalado, o instalador bloqueará a instalação. |
| Windows 8.1            | Se o .NET Framework 4.5.1 não estiver habilitado ou instalado, o instalador bloqueará a instalação. | Se o PowerShell 3,0 não estiver instalado, o instalador bloqueará a instalação. | Se o GPMC não estiver habilitado ou instalado, o instalador bloqueará a instalação. | Se o .NET Framework 4.5.1 não estiver habilitado ou instalado, o instalador bloqueará a instalação. | Se o GPMC não estiver habilitado ou instalado, o instalador bloqueará a instalação. |
| Windows Server 2012 R2 | Se o .NET Framework 4.5.1 não estiver habilitado ou instalado, o instalador bloqueará a instalação. | Se o PowerShell 3,0 não estiver instalado, o instalador bloqueará a instalação. | Se o GPMC não estiver habilitado, o instalador o habilitará durante a instalação.   | Se o .NET Framework 4.5.1 não estiver habilitado ou instalado, o instalador bloqueará a instalação. | Se o GPMC não estiver habilitado, o instalador o habilitará durante a instalação.   |

 

## Como obter tecnologias do MDOP


O AGPM 4,0 SP3 faz parte do Microsoft Desktop Optimization Pack (MDOP) desde o MDOP 2015. O MDOP faz parte do Microsoft Software Assurance. Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte [como obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Tópicos relacionados


[Gerenciamento Avançado de Política de Grupo](index.md)

[Notas de versão para Microsoft Advanced Group Policy Management 4.0 SP3](release-notes-for-microsoft-advanced-group-policy-management-40-sp3.md)

[Como escolher qual versão do AGPM a ser instalada](choosing-which-version-of-agpm-to-install.md)

 

 





