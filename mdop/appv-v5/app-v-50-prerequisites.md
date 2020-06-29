---
title: Pré-requisitos do App-V 5.0
description: Pré-requisitos do App-V 5.0
author: dansimp
ms.assetid: 9756b571-c785-4ce6-a95c-d4e134e89429
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 176c9729d8c909325c6d6694e024938d9ce9df53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796593"
---
# Pré-requisitos do App-V 5.0

Antes de começar a instalação do Microsoft Application Virtualization (App-V) 5,0, você deve verificar se atendeu os pré-requisitos para instalar o produto. Este tópico contém informações para ajudá-lo a planejar com êxito a preparação do ambiente de computação antes de implantar os recursos do App-V 5,0.

> [!Important]
> **Os pré-requisitos neste artigo se aplicam apenas ao App-V 5,0**. Para obter pré-requisitos adicionais que se aplicam a pacotes de serviço do App-V 5,0, consulte as seguintes páginas da Web:

-   [Quais são as novidades no App-V 5.0 SP1](whats-new-in-app-v-50-sp1.md)

-   [Sobre o App-V 5.0 SP2](about-app-v-50-sp2.md)

-   [Pré-requisitos do App-V 5.0 SP3](app-v-50-sp3-prerequisites.md)

A tabela a seguir lista as informações de pré-requisito pertinentes a sistemas operacionais específicos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistemas operacionais</th>
<th align="left">Descrição do pré-requisito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Computadores executando:</p>
<ul>
<li><p>Windows 8</p></li>
<li><p>Windows Server 2012</p></li>
</ul></td>
<td align="left"><p>Os seguintes pré-requisitos já estão instalados:</p>
<ul>
<li><p>Microsoft .NET Framework 4,5 – você não precisa do Microsoft .NET Framework 4</p></li>
<li><p>Windows PowerShell 3,0</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Computadores executando:</p>
<ul>
<li><p>Windows 7</p></li>
<li><p>Windows Server 2008</p></li>
</ul></td>
<td align="left"><p>Talvez você queira baixar o seguinte KB:</p>
<p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[Microsoft Security Advisory: Insecure library loading could allow remote code execution](https://support.microsoft.com/kb/2533623)">Comunicado de segurança da Microsoft: o carregamento da biblioteca inseguro pode permitir a execução remota de código</a></p>
<p>Verifique se há KBs subsequentes que substituiram este e observe que alguns KBs podem exigir que você desinstale as atualizações anteriores.</p></td>
</tr>
</tbody>
</table>

## Pré-requisitos de instalação do App-V 5,0

> [!Note]  
> Os pré-requisitos a seguir já estão instalados para computadores que executam o Windows 8.

Cada um dos recursos do App-V 5,0 tem pré-requisitos específicos que devem ser atendidos antes que os recursos do App-V 5,0 possam ser instalados com êxito.

### Pré-requisitos para o cliente do App-V 5,0

A tabela a seguir lista os pré-requisitos de instalação do cliente App-V 5,0:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pré-requisito</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Requisitos de software</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (pacote completo)</p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p>
<div class="alert">
<strong>Observação</strong><br/><p>A instalação do PowerShell 3,0 exige uma reinicialização.</p>
</div>
<div>

</div></li>
<li><p>Baixar e instalar o <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Importante</strong><br/><p>Você pode baixar e instalar o artigo da base de conhecimento anterior. No entanto, ele pode ter sido substituído por uma versão mais recente.</p>
</div>
<div>

</div></li>
<li><p>O instalador do cliente (. exe) detectará se é necessário instalar os seguintes pré-requisitos, e isso o fará de acordo com isso:</p>
<p></p>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Pacotes redistribuíveis do Visual C++ para o Visual Studio 2013</a></p>
<p>Esse pré-requisito só será necessário se você tiver instalado o pacote de hotfix 4 para Application Virtualization 5,0 SP2 ou posterior.</p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=26999" data-raw-source="[The Microsoft Visual C++ 2010 Redistributable](https://www.microsoft.com/download/details.aspx?id=26999)">O Microsoft Visual C++ 2010 Redistributable</a></p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=5638" data-raw-source="[Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://www.microsoft.com/download/details.aspx?id=5638)">Pacote redistribuível do Microsoft Visual C++ 2005 SP1 (x86)</a></p></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

### Pré-requisitos para o cliente de serviços de área de trabalho remota do App-V 5,0

> [!Note]  
> Os seguintes pré-requisitos já estão instalados para computadores que executam o Windows Server 2012.

A tabela a seguir lista os pré-requisitos de instalação para o cliente dos serviços de área de trabalho remota do App-V 5,0:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pré-requisito</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Requisitos de software</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft.NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft.NET Framework 4 (pacote completo)</a></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p>
<div class="alert">
<strong>Observação</strong><br/><p>A instalação do PowerShell 3,0 exige uma reinicialização.</p>
</div>
<div>

</div></li>
<li><p>Baixar e instalar o <a href="https://go.microsoft.com/fwlink/?LinkId=286102" data-raw-source="[KB2533623](https://go.microsoft.com/fwlink/?LinkId=286102 )"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Importante</strong><br/><p>Você pode baixar e instalar o artigo da base de conhecimento anterior. No entanto, ele pode ter sido substituído por uma versão mais recente.</p>
</div>
<div>

</div></li>
<li><p>O instalador do cliente (. exe) detectará se é necessário instalar os seguintes pré-requisitos, e isso o fará de acordo com isso:</p>
<p></p>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Pacotes redistribuíveis do Visual C++ para o Visual Studio 2013</a></p>
<p>Esse pré-requisito só será necessário se você tiver instalado o pacote de hotfix 4 para Application Virtualization 5,0 SP2 ou posterior.</p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=26999" data-raw-source="[The Microsoft Visual C++ 2010 Redistributable](https://www.microsoft.com/download/details.aspx?id=26999)">O Microsoft Visual C++ 2010 Redistributable</a></p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=5638" data-raw-source="[Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://www.microsoft.com/download/details.aspx?id=5638)">Pacote redistribuível do Microsoft Visual C++ 2005 SP1 (x86)</a></p></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

### Pré-requisitos para o sequenciador do App-V 5,0

> [!Note]
> Os pré-requisitos a seguir já estão instalados para computadores que executam o Windows 8 e o Windows Server 2012.

A tabela a seguir lista os pré-requisitos para a instalação do sequenciador do App-V 5,0. Se possível, o computador que executa o sequenciador deve ter as mesmas configurações de hardware e software que os computadores que executarão os aplicativos virtuais.

> [!Note]  
> Se os requisitos do sistema de um aplicativo instalado localmente excederem os requisitos do sequenciador, você deve atender aos requisitos do aplicativo. Além disso, como o processo de sequenciamento é intensivo em recursos do sistema, recomendamos que o computador que executa o sequenciador tenha bastante memória, um processador rápido e um disco rígido rápido. Para obter mais informações, consulte [configurações compatíveis com o App-V 5,0](app-v-50-supported-configurations.md).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pré-requisito</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Requisitos de software</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Pacotes redistribuíveis do Visual C++ para o Visual Studio 2013</a></p>
<p>Esse pré-requisito só será necessário se você tiver instalado o pacote de hotfix 4 para Application Virtualization 5,0 SP2.</p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (pacote completo)</a></p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p></li>
<li><p>Baixar e instalar o <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p>
<p></p></li>
<li><p>Para computadores que executam o Microsoft Windows Server 2008 R2 SP1, baixe e instale o <a href="https://go.microsoft.com/fwlink/?LinkId=286102" data-raw-source="[KB2533623](https://go.microsoft.com/fwlink/?LinkId=286102 )"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Importante</strong><br/><p>Você pode baixar e instalar um dos artigos da base de conhecimento anteriores. No entanto, eles podem ter sido substituídos por uma versão mais recente.</p>
</div>
<div>

</div></li>
</ul></td>
</tr>
</tbody>
</table>

### Pré-requisitos para o servidor do App-V 5,0

> [!Note]
> Os seguintes pré-requisitos já estão instalados para computadores que executam o Windows Server 2012:

-   Microsoft .NET Framework 4,5. Isso elimina o requisito do Microsoft .NET Framework 4.

-   Windows PowerShell 3,0

-   Baixar e instalar o [KB2533623](https://support.microsoft.com/kb/2533623) (https://support.microsoft.com/kb/2533623)

    > [!Important]
    > Ainda é possível baixar instalar o KB anterior. No entanto, ele pode ter sido substituído por uma versão mais recente.

A tabela a seguir lista os pré-requisitos de instalação do servidor App-V 5,0. A conta que você usa para instalar os componentes do servidor deve ter direitos administrativos no computador em que você está instalando. Essa conta também deve ter a capacidade de consultar os serviços de diretório do Active Directory. Antes de instalar e configurar os servidores do App-V 5,0, você deve especificar uma porta onde cada componente será hospedado. Você também deve adicionar as regras de firewall associadas para permitir solicitações de entrada às portas especificadas.

> [!Note]
> O WebDAV (criação e controle de versão distribuídas na Web) é automaticamente desabilitado para o serviço de gerenciamento.

O servidor do App-V 5,0 tem suporte para uma implantação autônoma, onde todos os componentes são implantados no mesmo servidor e uma implantação distribuída. Dependendo da topologia que você usa para implantar o servidor do App-V 5,0, os dados necessários para cada componente sofrerão alterações ligeiramente.

> [!Important]
> Não há suporte para a instalação do servidor do App-V 5,0 em um computador que executa qualquer versão ou componente anterior do App-V. Além disso, também não há suporte para a instalação dos componentes do servidor em um computador que executa núcleo do servidor ou controlador de domínio.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pré-requisito</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Servidor de gerenciamento</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (pacote completo)</a></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<div class="alert">
<strong>Observação</strong><br/><p>A instalação do PowerShell 3,0 exige uma reinicialização.</p>
</div>
<div>

</div></li>
<li><p>Servidor Web do Windows com a função IIS habilitada e os seguintes recursos: <strong> recursos http comuns </strong> (conteúdo estático e documento padrão), <strong> desenvolvimento de aplicativos </strong> (ASP.net, EXTENSIBILIDADE .net, extensões ISAPI e filtros ISAPI), <strong> segurança </strong> (autenticação do Windows, filtragem de solicitações), <strong> ferramentas de gerenciamento </strong> (console de gerenciamento do IIS).</p></li>
<li><p>Baixar e instalar o <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Importante</strong><br/><p>Ainda é possível baixar instalar o KB anterior. No entanto, ele pode ter sido substituído por uma versão mais recente.</p>
</div>
<div>

</div></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=13523" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x64)](https://www.microsoft.com/download/details.aspx?id=13523)">Pacote redistribuível do Microsoft Visual C++ 2010 SP1 (x64)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Pacote redistribuível do Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
<li><p>registro de ASP.NET de 64 bits</p></li>
</ul>
<p>Os componentes do servidor do App-V 5,0 são dependentes, mas têm requisitos e opções de instalação variáveis que devem ser implantados. Use as informações a seguir para preparar seu ambiente para executar o servidor de gerenciamento do App-V 5,0.</p>
<ul>
<li><p>Local de instalação – por padrão, esse componente será instalado em: <strong> %ProgramFiles%\Microsoft Application Virtualization Server </strong> .</p></li>
<li><p>Local do banco de dados de gerenciamento do App-V 5,0-nome do SQL Server, nome da instância SQL, nome do banco de dados.</p></li>
<li><p>Direitos de acesso para o console de gerenciamento do App-V 5,0-esse é o usuário ou o grupo que deve receber acesso ao console de gerenciamento no final da implantação. Após a implantação, somente esses usuários terão acesso ao console de gerenciamento até que administradores adicionais sejam adicionados pelo console de gerenciamento.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Não há suporte para grupos de segurança e usuários individuais. Você deve especificar um grupo do AD DS.</p>
</div>
<div>

</div></li>
<li><p>Nome do site do serviço de gerenciamento do App-V 5,0 – especifique um nome para o site ou use o nome padrão.</p></li>
<li><p>Associação de porta do serviço de gerenciamento do App-V 5,0 – deve ser um número de porta exclusivo que não é usado por outro site no computador.</p></li>
<li><p>Suporte para Microsoft Silverlight – o Microsoft Silverlight deve ser instalado antes de o console de gerenciamento estar disponível. Embora isso não seja um requisito para a implantação, o servidor deve ser capaz de dar suporte ao Microsoft Silverlight.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Banco de dados de gerenciamento</strong></p></td>
<td align="left"><p></p>
<div class="alert">
<strong>Observação</strong><br/><p>O banco de dados só é necessário ao usar o servidor de gerenciamento do App-V 5,0.</p>
</div>
<div>

</div>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (pacote completo)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Pacote redistribuível do Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
</ul>
<p>Os componentes do servidor do App-V 5,0 são dependentes, mas têm requisitos e opções de instalação variáveis que devem ser implantados. Use as informações a seguir para preparar seu ambiente para executar o banco de dados de gerenciamento do App-V 5,0.</p>
<ul>
<li><p>Local de instalação – por padrão, esse componente será instalado em <strong> %ProgramFiles%\Microsoft Application Virtualization Server </strong> .</p></li>
<li><p>Nome da instância do SQL Server personalizado (se aplicável) – o formato deve ser <strong> InstanceName </strong> , porque a instalação pressupõe que ela esteja no computador local. Se você especificar o nome com o formato a seguir, o <strong> SVR\INSTANCE </strong> irá falhar.</p></li>
<li><p>Nome do banco de dados personalizado do App-V 5,0 (se aplicável) – você deve especificar um nome de banco de dados exclusivo. O valor padrão para o banco de dados de gerenciamento é <strong> AppVManagement </strong> .</p></li>
<li><p>Local do servidor de gerenciamento do App-V 5,0 – especifica a conta da máquina na qual o servidor de gerenciamento é implantado. Isso deve ser especificado no seguinte formato <strong> Domain\MachineAccount </strong> .</p></li>
<li><p>Aplicativo de instalação do servidor de gerenciamento do App-V 5,0 – especifica a conta que será usada para instalar o servidor de gerenciamento do App-V 5,0. Você deve usar o seguinte formato: <strong> Domain\AdministratorLoginName </strong> .</p></li>
<li><p>Agente de serviço do Microsoft SQL Server-configure o computador que executa o banco de dados de gerenciamento do App-V 5,0 para que o serviço do Microsoft SQL Server Agent seja reiniciado automaticamente. Para obter mais informações, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=273725" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://go.microsoft.com/fwlink/?LinkId=273725)"> Configurar o agente do SQL Server para reiniciar os serviços automaticamente</a></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Servidor de relatórios</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (pacote completo)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Pacote redistribuível do Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
<li><div class="alert">
<strong>Observação</strong><br/><p>Para ajudar a reduzir o risco de envio de dados indesejados ou mal-intencionados para o servidor de relatórios, você deve restringir o acesso ao serviço Web de relatório de acordo com a política de segurança da sua empresa.</p>
</div>
<div>

</div>
<p>Servidor Web do Windows com a função IIS com os seguintes recursos: <strong> recursos http comuns </strong> (conteúdo estático e documento padrão), <strong> desenvolvimento de aplicativos </strong> (ASP.net, EXTENSIBILIDADE .net, extensões ISAPI e filtros ISAPI), <strong> segurança </strong> (autenticação do Windows, filtragem de solicitações), <strong> segurança </strong> (autenticação do Windows, filtragem de solicitações), <strong> ferramentas de gerenciamento </strong> (console de gerenciamento do IIS)</p></li>
<li><p>registro de ASP.NET de 64 bits</p></li>
<li><p>Local de instalação – por padrão, esse componente é instalado em <strong> %ProgramFiles%\Microsoft Application Virtualization Server </strong> .</p></li>
<li><p>Nome do site do serviço de relatório do App-V 5,0 – especifica o nome do site ou o nome padrão que será usado.</p></li>
<li><p>Associação de porta do serviço de relatórios do App-V 5,0 – deve ser um número de porta exclusivo que ainda não esteja sendo usado por outro site que seja executado no computador.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Banco de dados de relatórios</strong></p></td>
<td align="left"><p></p>
<div class="alert">
<strong>Observação</strong><br/><p>O banco de dados só é necessário ao usar o servidor de relatórios do App-V 5,0.</p>
</div>
<div>

</div>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (pacote completo)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Pacote redistribuível do Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
</ul>
<p>Os componentes do servidor do App-V 5,0 são dependentes, mas têm requisitos e opções de instalação variáveis que devem ser implantados. Use as informações a seguir para preparar seu ambiente para executar o banco de dados de relatórios do App-V 5,0.</p>
<ul>
<li><p>Local de instalação – por padrão, esse componente será instalado em <strong> %ProgramFiles%\Microsoft Application Virtualization Server </strong> .</p></li>
<li><p>Nome da instância do SQL Server personalizado (se aplicável) – o formato deve ser <strong> InstanceName </strong> , porque a instalação pressupõe que ela esteja no computador local. Se você especificar o nome com o formato a seguir, o <strong> SVR\INSTANCE </strong> irá falhar.</p></li>
<li><p>Nome do banco de dados personalizado do App-V 5,0 (se aplicável) – você deve especificar um nome de banco de dados exclusivo. O valor padrão para o banco de dados de relatórios é <strong> AppVReporting </strong> .</p></li>
<li><p>Local do servidor de relatórios do App-V 5,0 – especifica a conta da máquina na qual o servidor de relatórios é implantado. Isso deve ser especificado no seguinte formato <strong> Domain\MachineAccount </strong> .</p></li>
<li><p>Aplicativo de instalação do App-V 5,0 Reporting Server-especifica a conta que será usada para instalar o servidor de relatórios do App-V 5,0. Você deve usar o seguinte formato: <strong> Domain\AdministratorLoginName </strong> .</p></li>
<li><p>Serviço do Microsoft SQL Server e o serviço do Microsoft SQL Server Agent – esses serviços devem estar associados a contas de usuário que têm acesso ao anúncio de consulta.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Publishing Server</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (pacote completo)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Pacote redistribuível do Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
<li><p>Servidor Web do Windows com a função IIS com os seguintes recursos: <strong> recursos http comuns </strong> (conteúdo estático e documento padrão), <strong> desenvolvimento de aplicativos </strong> (ASP.net, EXTENSIBILIDADE .net, extensões ISAPI e filtros ISAPI), <strong> segurança </strong> (autenticação do Windows, filtragem de solicitações), <strong> segurança </strong> (autenticação do Windows, filtragem de solicitações), <strong> ferramentas de gerenciamento </strong> (console de gerenciamento do IIS)</p></li>
<li><p>registro de ASP.NET de 64 bits</p></li>
</ul>
<p>Os componentes do servidor do App-V 5,0 são dependentes, mas têm requisitos e opções de instalação variáveis que devem ser implantados. Use as informações a seguir para preparar seu ambiente para executar o servidor de publicação App-V 5,0.</p>
<ul>
<li><p>Local de instalação – por padrão, esse componente é instalado em <strong> %ProgramFiles%\Microsoft Application Virtualization Server </strong> .</p></li>
<li><p>URL do serviço de gerenciamento do App-V 5,0 – especifica a URL do serviço de gerenciamento do App-V 5,0. Essa é a porta com a qual o servidor de publicação se comunica e deve ser especificada usando o seguinte formato: <strong><a href="http://localhost:12345" data-raw-source="http://localhost:12345"> http://localhost:12345 </a></strong> .</p></li>
<li><p>Nome do site do serviço de publicação do App-V 5,0 – especifica o nome do site ou o nome padrão que será usado.</p></li>
<li><p>Associação de porta do serviço de publicação do App-V 5,0 – deve ser um número de porta exclusivo que ainda não esteja sendo usado por outro site que seja executado no computador.</p></li>
</ul></td>
</tr>
</tbody>
</table>

## Tópicos relacionados

[Planejando a implantação do App-V](planning-to-deploy-app-v.md)

[Configurações com suporte ao App-V 5.0](app-v-50-supported-configurations.md)
