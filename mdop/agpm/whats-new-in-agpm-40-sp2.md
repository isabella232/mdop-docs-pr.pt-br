---
title: Novidades do AGPM 4.0 SP2
description: Novidades do AGPM 4.0 SP2
author: dansimp
ms.assetid: 5c0dcab4-f27d-4153-8b8e-b280b080be51
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 56369207780cf0795f16eda91f249a26270c4b47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797267"
---
# Novidades do AGPM 4.0 SP2


Este conteúdo descreve melhorias e configurações com suporte para o serviço de gerenciamento de política de grupo avançado (AGPM) 4.0 da Microsoft Pack2 (SP2). Se houver uma diferença entre esse conteúdo e outra documentação do AGPM, considere esse conteúdo autoritativo e assuma que ele substitui a outra documentação.

## <a href="" id="what-s-new"></a>O que há de novo


O AGPM 4.0 SP2 é compatível com os recursos e funcionalidades a seguir.

### Suporte para Windows 8.1 e Windows Server2012 R2

O AGPM 4.0 SP2 adiciona suporte para os sistemas operacionais Windows 8.1 e Windows Server2012 R2.

### Extensões novas e alteradas do lado do cliente

As extensões do lado do cliente da política de grupo foram adicionadas ou alteradas para o AGPM para dar suporte a novas configurações de política no Windows 8.1. Essas configurações de política permitem que os administradores de política de grupo gerenciem e controlem as configurações de política específicas do Windows 8.1 que mudam entre dois objetos de política de grupo (GPOs) ou modelos. Para exibir as extensões do lado do cliente, use as configurações e os relatórios de diferença disponíveis no cliente do AGPM.

As extensões nova e alterada do lado do cliente da política de grupo são:

-   **Especifique as configurações de pastas de trabalho**. Se você habilitar essa configuração de política, os administradores de ti poderão configurar pastas de trabalho para serem criadas automaticamente. O recurso de pastas de trabalho permite que os usuários finais sincronizem arquivos de dispositivos da área de trabalho do Windows para outros dispositivos. Use essa configuração de política para criar a relação de sincronização em dispositivos de um usuário final e para configurar como identificar o servidor de arquivos que armazena as pastas de trabalho do usuário. Se você marcar a caixa de seleção **autoprovisionar sincronização** , a parceria de sincronização será criada sem a entrada do usuário, e os dados começarão a ser sincronizados automaticamente com o dispositivo do usuário. Se você não marcar a caixa de seleção **sincronização automática de autoprovisionar** , os usuários devem fornecer entrada para iniciar a sincronização.

-   **Forçar a configuração automática para todos os usuários**. Se você habilitar essa configuração de política, os administradores de ti poderão determinar se a parceria de pastas de trabalho será criada automaticamente em dispositivos de usuário final sem entrada de usuários finais. Se você habilitar essa configuração de política, a sincronização será configurada de acordo com o modo como você define a configuração de política **especificar configurações de pastas de trabalho** . Se você definir a configuração de política **forçar configuração automática para todos os usuários** como **desabilitada** ou **não configurada**, a parceria de pastas de trabalho será configurada de acordo com o modo como você define a opção de **provisionamento automático** na configuração de política **especificar configurações de pastas de trabalho** .

Para obter mais informações sobre o recurso de pastas de trabalho, consulte [visão geral de pastas de trabalho](https://go.microsoft.com/fwlink/?LinkId=330444).

### Feedback do cliente e pacote cumulativo de hotfix

O AGPM 4.0 SP2 inclui um pacote cumulativo de hotfixes para solucionar problemas encontrados desde o lançamento do AGPM 4.0 Service Pack1 (SP1). O AGPM 4.0 SP2 contém as mais recentes correções até e incluindo o gerenciamento avançado de política de grupo 4.0 da Microsoft 4.0 SP1 Hotfix1. Para obter mais informações, consulte o artigo [2873472](https://go.microsoft.com/fwlink/?LinkId=325400)da base de dados de conhecimento.

### Novas extensões de política de grupo nas configurações e relatórios de diferença

As novas extensões de política de grupo foram adicionadas às configurações e aos relatórios de diferença.

### Mudanças e suporte do instalador

As alterações e o suporte para o instalador do AGPM 4.0 SP2 são:

-   Se você instalar o AGPM 4.0 SP2 nos sistemas operacionais Windows 8 ou Windows Server 2012 ou posteriores, o instalador do AGPM verificará se o software de pré-requisito obrigatório (console de gerenciamento de política de grupo (GPMC) e o Microsoft .NET Framework 3.5) está instalado. Se este software obrigatório não estiver instalado, a instalação do AGPM 4.0 SP2 será bloqueada.

-   Quando você instala o servidor do AGPM, a ativação do WCF, a ativação não HTTP e o serviço de ativação de processos do Windows são habilitados automaticamente.

-   No sistema operacional do cliente WindowsVista e sistemas operacionais posteriores, baixe a versão apropriada das ferramentas de administração do sistema remoto para o sistema operacional antes de instalar o AGPM 4.0 SP2.

-   O AGPM 4.0 SP2 dá suporte à compatibilidade com versões anteriores com sistemas operacionais compatíveis.

### Capacidade de atualizar para o AGPM 4.0 SP2 sem digitar novamente os parâmetros de configuração

Você pode atualizar o cliente do AGPM ou o servidor do AGPM para o AGPM 4.0 SP2 sem ser solicitado a digitar novamente os parâmetros de configuração (chamado de atualização inteligente) somente do AGPM 4.0 em diante, conforme mostrado na tabela a seguir. Se você estiver atualizando para o AGPM 4.0 SP2 de outras versões do AGPM, conforme mostrado na tabela, você deve usar a atualização clássica, que exige que você reinsira os parâmetros de configuração. Como cada versão do AGPM está associada a um sistema operacional específico, consulte [escolhendo qual versão do AGPM instalar](https://go.microsoft.com/fwlink/?LinkId=254350) e certifique-se de atualizar o sistema operacional conforme apropriado antes de atualizar o AGPM.

**Atualizações compatíveis com o AGPM 4,0 SP2**

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Versão do AGPM a partir da qual você pode atualizar</strong></p></td>
<td align="left"><p><strong>2,5</strong></p></td>
<td align="left"><p><strong>3,0</strong></p></td>
<td align="left"><p><strong>4,0</strong></p></td>
<td align="left"><p><strong>4,0 SP1</strong></p></td>
<td align="left"><p><strong>4,0 SP2</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>2,5</p></td>
<td align="left"><p>Não Aplicável</p></td>
<td align="left"><p>Atualização clássica</p></td>
<td align="left"><p>Atualização clássica</p></td>
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
</tr>
<tr class="even">
<td align="left"><p>4,0</p></td>
<td align="left"><p>Não Aplicável</p></td>
<td align="left"><p>Não Aplicável</p></td>
<td align="left"><p>Não Aplicável</p></td>
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
</tr>
</tbody>
</table>

 

## Configurações compatíveis


O AGPM 4.0 SP2 dá suporte às configurações na tabela a seguir. Embora o AGPM dê suporte a configurações mistas, recomendamos que você execute o cliente do AGPM e o servidor do AGPM na mesma linha do sistema operacional, por exemplo, Windows 8.1 com Windows Server2012 R2, Windows 8 com Windows Server 2012 e assim por diante.

**Configurações de política e sistemas operacionais compatíveis com o AGPM 4.0 SP2**

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
<td align="left"><p>Windows Server2012 R2 ou Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 ou Windows 8.1</p></td>
<td align="left"><p>Com suporte</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012, Windows 8.1 ou Windows 8</p></td>
<td align="left"><p>Windows Server 2012 ou Windows 8</p></td>
<td align="left"><p>Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8.1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 ou Windows7</p></td>
<td align="left"><p>Windows Server2008R2 ou Windows7</p></td>
<td align="left"><p>Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8.1 ou no Windows 8</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012, Windows Server2008R2, Windows 8 ou Windows 7</p></td>
<td align="left"><p>Windows Server2008 ou WindowsVista com Service Pack 1 (SP1)</p></td>
<td align="left"><p>Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 ou Windows 7</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2, Windows 8 ou Windows 7</p></td>
<td align="left"><p>Sem suporte</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Windows Server2008 ou Windows Vista com SP1</p></td>
<td align="left"><p>Com suporte, mas não pode reportar ou editar configurações de política ou itens de preferência que existem somente no Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 ou Windows 7</p></td>
</tr>
</tbody>
</table>

 

## Pré-requisitos para a instalação do AGPM 4.0 SP2


A tabela a seguir descreve o comportamento dos instaladores do cliente e do servidor do AGPM 4.0 SP2 no Windows 8.1 quando o .NET Framework 3.5 ou o GPMC nas ferramentas de administração do servidor remoto estão ausentes.

**Cliente do AGPM**

**Servidor do AGPM**

**Sistema operacional**

**.NET Framework**

**Ferramentas de Administração de Servidor Remoto**

**.NET Framework**

**Ferramentas de Administração de Servidor Remoto**

**Windows 8.1**

Se o .NET Framework 3.5 não estiver habilitado ou instalado, o instalador bloqueará a instalação.

Se o GPMC não estiver habilitado ou instalado, o instalador bloqueará a instalação.

Se o .NET Framework 3.5 não estiver habilitado ou instalado, o instalador bloqueará a instalação.

Se o GPMC não estiver habilitado ou instalado, o instalador bloqueará a instalação.

**Windows Server2012 R2**

Se o .NET Framework 3.5 não estiver habilitado ou instalado, o instalador bloqueará a instalação.

Se o GPMC não estiver habilitado, o instalador o habilitará durante a instalação.

Se o .NET Framework 3.5 não estiver habilitado ou instalado, o instalador bloqueará a instalação.

Se o GPMC não estiver habilitado, o instalador o habilitará durante a instalação.

 

## Como obter tecnologias do MDOP


O AGPM 4,0 SP2 faz parte do Microsoft Desktop Optimization Pack (MDOP). O MDOP faz parte do Microsoft Software Assurance. Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte [como obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Tópicos relacionados


[Gerenciamento Avançado de Política de Grupo](index.md)

[Notas de versão para Microsoft Advanced Group Policy Management 4.0 SP2](release-notes-for-microsoft-advanced-group-policy-management-40-sp2.md)

[Como escolher qual versão do AGPM a ser instalada](choosing-which-version-of-agpm-to-install.md)

 

 





