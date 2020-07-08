---
title: Configurações com suporte ao App-V 5.0
description: Configurações com suporte ao App-V 5.0
author: dansimp
ms.assetid: 3787ff63-7ce7-45a8-8f01-81b4b6dced34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 60236743d2a6b418ca7f4705168a7bf064b82156
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796587"
---
# Configurações com suporte ao App-V 5.0


Este tópico especifica os requisitos necessários para instalar e executar o Microsoft Application Virtualization (App-V) 5,0 em seu ambiente.

**Importante**  
**As configurações com suporte neste artigo se aplicam apenas ao App-V 5,0**. Para configurações compatíveis que se aplicam aos pacotes de serviço do App-V 5,0, consulte as seguintes páginas da Web:

-   [Quais são as novidades no App-V 5.0 SP1](whats-new-in-app-v-50-sp1.md)

-   [Sobre o App-V 5.0 SP2](about-app-v-50-sp2.md)

-   [Configurações com suporte ao App-V 5.0 SP3](app-v-50-sp3-supported-configurations.md)



## <a href="" id="---------app-v-5-0-server-system-requirements"></a> Requisitos do sistema do App-V 5,0 Server


**Importante**  
O servidor do App-V 5,0 não é compatível com os seguintes cenários:



-   Implantação em um computador que executa o Microsoft Windows Server Core.

-   Implantação em um computador que executa uma versão anterior dos componentes do App-V 5,0 Server.

    **Observação**  
    Você pode instalar o App-V 5,0 lado a lado com o servidor do App-V 4,5 Lightweight Streaming Server (LWS) apenas. Não há suporte para a implantação do App-V 5,0 lado a lado com o servidor HWS do App-V 4,5 Application Virtualization Management Service (HWS).



-   Implantação em um computador que executa o Microsoft SQL Server Express Edition.

-   Implantação remota do banco de dados do servidor de gerenciamento ou do banco de dados de relatórios. O instalador deve ser executado diretamente no computador executando o Microsoft SQL para que a instalação do banco de dados seja bem-sucedida.

-   Implantação em um controlador de domínio.

-   Não há suporte para caminhos curtos. Se você pretende usar um caminho curto, você deve criar um novo volume.

### Requisitos do sistema operacional do servidor de gerenciamento

A tabela a seguir lista os sistemas operacionais suportados para a instalação do servidor de gerenciamento do App-V 5,0.

**Observação**  
A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior. Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)



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
<td align="left"><p>Microsoft Windows Server 2008 (padrão, Enterprise, Datacenter ou servidor Web)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p>SP1 e versões mais recentes</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012 (padrão, Datacenter)</p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 (padrão, Datacenter)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>



**Importante**  
Não há suporte para a implantação da função de servidor de gerenciamento em um computador com o compartilhamento de área de trabalho remota (RDS) habilitada.



### <a href="" id="management-server-hardware-requirements-"></a>Requisitos de hardware do servidor de gerenciamento

-   Processador – 1,4 GHz ou mais rápido, processador de 64 bits (x64)

-   RAM — 1 GB de RAM (64 bits)

-   Espaço em disco – 200 MB de espaço disponível no disco rígido, não incluindo o diretório de conteúdo.

### Requisitos do sistema operacional do servidor de publicação

A tabela a seguir lista os sistemas operacionais suportados para a instalação do servidor de publicação do App-V 5,0.

**Observação**  
A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior. Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)



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
<td align="left"><p>Microsoft Windows Server 2008 (padrão, Enterprise, Datacenter ou servidor Web)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012 (padrão, Datacenter)</p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 (padrão, Datacenter)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>



### <a href="" id="publishing-server-hardware-requirements-"></a>Requisitos de hardware do servidor de publicação

-   Processador – 1,4 GHz ou mais veloz. processador de 64 bits (x64)

-   RAM – 2 GB de RAM (64 bits)

-   Espaço em disco — 200 MB de espaço disponível no disco rígido. Não inclui o diretório de conteúdo

### Requisitos do sistema operacional do servidor de relatório

A tabela a seguir lista os sistemas operacionais suportados para a instalação do App-V 5,0 Reporting Server.

**Observação**  
A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior. Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)



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
<td align="left"><p>Microsoft Windows Server 2008 (padrão, Enterprise, Datacenter ou servidor Web)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012 (padrão, Datacenter)</p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 (padrão, Datacenter)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>



### <a href="" id="reporting-server-hardware-requirements-"></a>Requisitos de hardware do servidor de relatório

-   Processador – 1,4 GHz ou mais veloz. processador de 64 bits (x64)

-   RAM – 2 GB de RAM (64 bits)

-   Espaço em disco — 200 MB de espaço disponível no disco rígido

### <a href="" id="sql-server-database-requirements-"></a>Requisitos de banco de dados do SQL Server

A tabela a seguir lista as versões do SQL Server com suporte para o banco de dados do App-V 5,0 e para a instalação do servidor.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo de servidor do App-V 5,0</th>
<th align="left">Versão do SQL Server</th>
<th align="left">Edição</th>
<th align="left">Service Pack</th>
<th align="left">Arquitetura do sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Gerenciamento/relatórios</p></td>
<td align="left"><p>Microsoft SQL Server 2008</p>
<p>(Standard, Enterprise, Datacenter ou a edição para desenvolvedores com o seguinte recurso: <strong> Serviços de mecanismo de banco de dados </strong> .)</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gerenciamento/relatórios</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p>
<p>(Standard, Enterprise, Datacenter ou a edição para desenvolvedores com o seguinte recurso: <strong> Serviços de mecanismo de banco de dados </strong> .)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gerenciamento/relatórios</p></td>
<td align="left"><p>Microsoft SQL Server 2012</p>
<p>(Standard, Enterprise, Datacenter ou a edição para desenvolvedores com o seguinte recurso: <strong> Serviços de mecanismo de banco de dados </strong> .)</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-client-supp-cfgs"></a> Requisitos do sistema do cliente do App-V 5,0


A tabela a seguir lista os sistemas operacionais com suporte para a instalação do cliente do App-V 5,0.

**Observação**  
A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior. Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)



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
<td align="left"><p>Microsoft Windows 7</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong>Importante</strong><br/><p>O Windows 8,1 só tem suporte do App-V 5,0 SP2</p>
</div>
<div>

</div>
<p>Windows 8.1</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
</tbody>
</table>



Não há suporte para os seguintes cenários de instalação do cliente do App-V, exceto conforme observado:

-   Computadores que executam o Windows Server

-   Computadores que executam o App-V 4,6 SP1 ou versões anteriores

-   O cliente de serviços de área de trabalho remota do App-V 5,0 tem suporte apenas para servidores habilitados para RDS

### <a href="" id="client-hardware-requirements-"></a>Requisitos de hardware do cliente

A lista a seguir exibe a configuração de hardware com suporte para a instalação do cliente do App-V 5,0.

-   Processador — 1,4 GHz ou processador de 32 bits (x86) ou 64 bits (x64)

-   RAM – 1 GB (32 bits) ou 2 GB (64 bits)

-   Disco — 100 MB para instalação, não incluindo o espaço em disco usado por aplicativos virtualizados.

## <a href="" id="---------app-v-5-0-remote-desktop-client-system-requirements"></a> Requisitos do sistema do cliente de área de trabalho remota do App-V 5,0


A tabela a seguir lista os sistemas operacionais com suporte para a instalação de cliente de área de trabalho remota do App-V 5,0.

**Observação**  
A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior. Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)



Service Pack da edição do sistema operacional Microsoft Windows Server 2008

R2

SP1

Microsoft Windows Server 2012

**Importante**  
O Windows Server 2012 R2 só tem suporte do App-V 5,0 SP2



Microsoft Windows Server 2012 (padrão, Datacenter)

R2

64 bits



### <a href="" id="remote-desktop-client-hardware-requirements-"></a>Requisitos de hardware do cliente da área de trabalho remota

A lista a seguir exibe a configuração de hardware com suporte para a instalação do cliente do App-V 5,0.

-   Processador — 1,4 GHz ou processador de 32 bits (x86) ou 64 bits (x64)

-   RAM – 1 GB (32 bits) ou 2 GB (64 bits)

-   Disco — 100 MB para instalação, não incluindo o espaço em disco usado por aplicativos virtualizados.

## <a href="" id="---------app-v-5-0-sequencer-system-requirements"></a> Requisitos do sistema do App-V 5,0 Sequencer


A tabela a seguir lista os sistemas operacionais suportados para a instalação do sequenciador do App-V 5,0.

**Observação**  
A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack imediatamente anterior. Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obter informações adicionais sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)



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
<td align="left"><p>Microsoft Windows 7</p></td>
<td align="left"></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 bits e 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8</p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bits e 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong>Importante</strong><br/><p>O Windows 8,1 só tem suporte do App-V 5,0 SP2</p>
</div>
<div>

</div>
<p>Windows 8.1</p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2008</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 bits e 64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p>32 bits e 64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><div class="alert">
<strong>Importante</strong><br/><p>O Windows Server 2012 R2 só tem suporte do App-V 5,0 SP2</p>
</div>
<div>

</div>
<p>Microsoft Windows Server 2012</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-supp-ver-sccm"></a>Versões com suporte do System Center Configuration Manager


Você pode usar o Gerenciador de configuração do Microsoft System Center 2012 ou o Gerenciador de configuração do System Center 2012 R2 para gerenciar aplicativos virtuais do App-V, relatórios e outras funções. A tabela a seguir lista as versões com suporte do Configuration Manager para cada versão aplicável do App-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versão do Configuration Manager compatível</th>
<th align="left">Versão do App-V</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Gerenciador de configuração do Microsoft System Center 2012</p></td>
<td align="left"><ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>System Center 2012 R2 Configuration Manager</p></td>
<td align="left"><ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
</ul></td>
</tr>
</tbody>
</table>



Para obter mais informações sobre como o Configuration Manager integra-se ao App-V, consulte [planejando a integração do App-v com o Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).






## Tópicos relacionados


[Planejando a implantação do App-V](planning-to-deploy-app-v.md)

[Pré-requisitos do App-V 5.0](app-v-50-prerequisites.md)









