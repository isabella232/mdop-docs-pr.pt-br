---
title: Configurações com suporte ao App-V 5.1
description: Configurações com suporte ao App-V 5.1
author: dansimp
ms.assetid: 8b8db63b-f71c-4ae9-80e7-a6752334e1f6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/02/2020
ms.openlocfilehash: fbda364de66b1f7b8730dca38f864a84f7848e58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796571"
---
# Configurações com suporte ao App-V 5.1

>Aplica-se a: Windows 10, versão 1607; Servidor de janelas 2019; Windows Server 2016; Windows Server 2012 R2; Windows Server 2012; Windows Server 2008 R2 (atualização de segurança estendida)

Este tópico especifica os requisitos para instalar e executar o Microsoft Application Virtualization (App-V) 5,1 em seu ambiente.

## Requisitos do sistema do App-V Server

Esta seção lista os requisitos de sistema operacional e de hardware para todos os componentes do App-V Server.

### Cenários de servidor sem suporte do 5,1 do App-V

O servidor do App-V 5,1 não é compatível com os seguintes cenários:

-   Implantação em um computador que executa o Microsoft Windows Server Core.

-   Implantação em um computador que executa uma versão anterior dos componentes do App-V 5,1 Server. Você pode instalar o App-V 5,1 lado a lado com o servidor do App-V 4.5 Lightweight Streaming Server (LWS) apenas. A implantação do App-V lado a lado com o serviço de gerenciamento de virtualização do aplicativo (HWS) do App-V 4,5 não é suportada.

-   Implantação em um computador que executa o Microsoft SQL Server Express Edition.

-   Implantação em um controlador de domínio.

-   Caminhos curtos. Se você pretende usar um caminho curto, deve criar um novo volume.

### Requisitos do sistema operacional do servidor de gerenciamento

A tabela a seguir lista os sistemas operacionais suportados para a instalação do servidor de gerenciamento do App-V 5,1.

> [!NOTE]
> A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior. Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Consulte [perguntas frequentes sobre política de suporte do ciclo de vida do suporte Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976) para obter mais informações

 | Sistema operacional                 | Service Pack | Arquitetura do sistema |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64 bits       |
| Microsoft Windows Server 2016    |              |        64 bits       |
| Microsoft Windows Server 2012 R2 |              |        64 bits       |
| Microsoft Windows Server 2012    |              |        64 bits       |
| [Atualização de segurança estendida](https://www.microsoft.com/windows-server/extended-security-updates) do Microsoft Windows Server 2008 R2|      SP1     |        64 bits       |
 

**Importante**  Não há suporte para a implantação da função de servidor de gerenciamento em um computador com o compartilhamento de área de trabalho remota (RDS) habilitada.

 

### <a href="" id="management-server-hardware-requirements-"></a>Requisitos de hardware do servidor de gerenciamento

-   Processador – 1,4 GHz ou mais rápido, processador de 64 bits (x64)

-   RAM — 1 GB de RAM (64 bits)

-   Espaço em disco — 200 MB de espaço disponível no disco rígido, não incluindo o diretório de conteúdo

### Requisitos de banco de dados do servidor de gerenciamento

A tabela a seguir lista as versões do SQL Server que têm suporte para a instalação do banco de dados de gerenciamento do App-V 5,1.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versão do SQL Server</th>
<th align="left">Service Pack</th>
<th align="left">Arquitetura do sistema</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2019</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>

<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2017</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2016</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2012</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2008 R2</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
</tbody>
</table>

Para obter mais informações sobre arquivos de configuração do usuário com o SQL Server 2016 ou posterior, consulte o [artigo de suporte](https://support.microsoft.com/help/4548751/app-v-server-publishing-might-fail-when-you-apply-user-configuration-f).

### Requisitos do sistema operacional do servidor de publicação

A tabela a seguir lista os sistemas operacionais suportados para a instalação do servidor de publicação do App-V 5,1.

| Sistema operacional                 | Service Pack | Arquitetura do sistema |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64 bits       |
| Microsoft Windows Server 2016    |              |        64 bits       |
| Microsoft Windows Server 2012 R2 |              |        64 bits       |
| Microsoft Windows Server 2012    |              |        64 bits       |
| [Atualização de segurança estendida](https://www.microsoft.com/windows-server/extended-security-updates) do Microsoft Windows Server 2008 R2 |      SP1     |        64 bits       |

### <a href="" id="publishing-server-hardware-requirements-"></a>Requisitos de hardware do servidor de publicação

O App-V adiciona nenhuma outra necessidade além daquelas do Windows Server.

-   Processador – 1,4 GHz ou mais rápido, processador de 64 bits (x64)

-   RAM – 2 GB de RAM (64 bits)

-   Espaço em disco — 200 MB de espaço disponível no disco rígido, não incluindo o diretório de conteúdo

### Requisitos do sistema operacional do servidor de relatório

A tabela a seguir lista os sistemas operacionais suportados para a instalação do App-V 5,1 Reporting Server.

| Sistema operacional                 | Service Pack | Arquitetura do sistema |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64 bits       |
| Microsoft Windows Server 2016    |              |        64 bits       |
| Microsoft Windows Server 2012 R2 |              |        64 bits       |
| Microsoft Windows Server 2012    |              |        64 bits       |
| [Atualização de segurança estendida](https://www.microsoft.com/windows-server/extended-security-updates) do Microsoft Windows Server 2008 R2 |      SP1     |        64 bits       |

### <a href="" id="reporting-server-hardware-requirements-"></a>Requisitos de hardware do servidor de relatório

O App-V adiciona nenhuma outra necessidade além daquelas do Windows Server.

-   Processador – 1,4 GHz ou mais rápido, processador de 64 bits (x64)

-   RAM – 2 GB de RAM (64 bits)

-   Espaço em disco — 200 MB de espaço disponível no disco rígido

### Requisitos de banco de dados do servidor de relatório

A tabela a seguir lista as versões do SQL Server que têm suporte para a instalação do banco de dados de relatórios do App-V 5,1.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versão do SQL Server</th>
<th align="left">Service Pack</th>
<th align="left">Arquitetura do sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2017</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2016</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2014</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2012</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2008 R2</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-client-supp-cfgs"></a>Requisitos do sistema do cliente App-V

A tabela a seguir lista os sistemas operacionais com suporte para a instalação do cliente do App-V 5,1.

> [!NOTE]
> Com a versão de aniversário do Windows 10 (aka versão 1607), o cliente App-V está em uma caixa e bloqueará a instalação de qualquer versão anterior do cliente App-V

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operacional</th>
<th align="left">Service Pack</th>
<th align="left">Arquitetura do sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows10 (versão anterior ao 1607)</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8.1</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>7</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
</tbody>
</table>

 

Não há suporte para os seguintes cenários de instalação do cliente do App-V, exceto conforme observado:

-   Computadores que executam o Windows Server

-   Computadores que executam o App-V 4.6 SP1 ou versões anteriores

-   O cliente de serviços de área de trabalho remota do App-V 5,1 tem suporte apenas para servidores habilitados para RDS

### <a href="" id="app-v-client-hardware-requirements-"></a>Requisitos de hardware do aplicativo cliente do App-V

A lista a seguir exibe a configuração de hardware com suporte para a instalação do cliente do App-V 5,1.

-   Processador — 1,4 GHz ou processador de 32 bits (x86) ou 64 bits (x64)

-   RAM – 1 GB (32 bits) ou 2 GB (64 bits)

-   Disco — 100 MB para instalação, não incluindo o espaço em disco usado por aplicativos virtualizados.

## Requisitos do sistema do cliente dos serviços de área de trabalho remota


A tabela a seguir lista os sistemas operacionais com suporte para a instalação do cliente do App-V 5,1 Remote Desktop Services (RDS).

| Sistema operacional                 | Service Pack | Arquitetura do sistema |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64 bits       |
| Microsoft Windows Server 2016    |              |        64 bits       |
| Microsoft Windows Server 2012 R2 |              |        64 bits       |
| Microsoft Windows Server 2012    |              |        64 bits       |
| [Atualização de segurança estendida](https://www.microsoft.com/windows-server/extended-security-updates) do Microsoft Windows Server 2008 R2 |      SP1     |        64 bits       |

### Requisitos de hardware do cliente dos serviços de área de trabalho remota

O App-V adiciona nenhuma outra necessidade além daquelas do Windows Server.

-   Processador – 1,4 GHz ou mais rápido, processador de 64 bits (x64)

-   RAM – 2 GB de RAM (64 bits)

-   Espaço em disco — 200 MB de espaço disponível no disco rígido

## Requisitos do sistema do sequenciador

A tabela a seguir lista os sistemas operacionais suportados para a instalação do sequenciador do App-V 5,1.

| Sistema operacional                 | Service Pack | Arquitetura do sistema |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64 bits       |
| Microsoft Windows Server 2016    |              |        64 bits       |
| Microsoft Windows Server 2012 R2 |              |        64 bits       |
| Microsoft Windows Server 2012    |              |        64 bits       |
| [Atualização de segurança estendida](https://www.microsoft.com/windows-server/extended-security-updates) do Microsoft Windows Server 2008 R2 |      SP1     |        64 bits       |
| Microsoft Windows 10             |              | 32 bits e 64 bits   |
| Microsoft Windows 8,1            |              | 32 bits e 64 bits   |
| Microsoft Windows 7              |      SP1     | 32 bits e 64 bits   |

### Requisitos de hardware do sequenciador

Consulte a documentação do Windows ou Windows Server para saber quais são os requisitos de hardware. O App-V adiciona nenhum requisito de hardware adicional.

## <a href="" id="bkmk-supp-ver-sccm"></a>Versões com suporte do System Center Configuration Manager

O cliente App-V dá suporte às seguintes versões do System Center Configuration Manager:

-   MicrosoftSystemCenter2012 ConfigurationManager

-   System Center 2012 R2 Configuration Manager

-   System Center 2012 R2 Configuration Manager SP1

A seguinte matriz de versão do App-V e do System Center Configuration Manager mostra todas as combinações suportadas oficialmente do App-V e do Configuration Manager.

> [!NOTE]
> O App-V 4,5 e o 4,6 saíram do suporte básico.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versão do App-V</th>
<th align="left">System Center Configuration Manager 2007</th>
<th align="left">Systems Center 2012 Configuration Manager</th>
<th align="left">System Center 2012 Configuration Manager SP1</th>
<th align="left">System Center 2012 R2 Configuration Manager</th>
<th align="left">System Center 2012 R2 Configuration Manager SP1</th>
<th align="left">System Center 2012 Configuration Manager SP2</th>
<th align="left">System Center Configuration Manager versão 1511</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,0 SP3</p></td>
<td align="left"><p>MSI-wrapper somente</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>2012 SP1 CU4</p></td>
<td align="left"><p>2012 R2 CU1</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 5.1</p></td>
<td align="left"><p>MSI-wrapper somente</p></td>
<td align="left"><p>Não</p></td>
<td align="left"><p>2012 SP1 CU4</p></td>
<td align="left"><p>2012 R2 CU1</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
</tr>
</tbody>
</table>

 

Para obter mais informações sobre como o Configuration Manager integra-se ao App-V, consulte [planejando a integração do App-v com o Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).

## Tópicos relacionados

[Planejando a implantação do App-V](planning-to-deploy-app-v51.md)

[Pré-requisitos do App-V 5.1](app-v-51-prerequisites.md)
