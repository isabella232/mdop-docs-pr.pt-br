---
title: Pré-requisitos do App-V 5.1
description: Pré-requisitos do App-V 5.1
author: dansimp
ms.assetid: 1bfa03c1-a4ae-45ec-8a2b-b10c2b94bfb0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 24a74d8f8d7148cdb6c32bcafa87f479d24305af
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796575"
---
# Pré-requisitos do App-V 5.1


Antes de instalar o Microsoft Application Virtualization (App-V) 5,1, verifique se você instalou todos os softwares de pré-requisito obrigatórios a seguir.

Para obter uma lista dos sistemas operacionais compatíveis e requisitos de hardware para o App-V Server, o Sequencer e o cliente, consulte [configurações compatíveis do App-v 5,1](app-v-51-supported-configurations.md).

## Resumo do software pré-instalado em cada sistema operacional


A tabela a seguir indica o software que já está instalado para diferentes sistemas operacionais.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operacional</th>
<th align="left">Descrição do pré-requisito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Todo o software obrigatório já está instalado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>Todo o software obrigatório já está instalado.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Se você estiver executando o Windows 8, atualize para o Windows 8,1 antes de usar o App-V 5,1.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>O seguinte software de pré-requisito já está instalado:</p>
<ul>
<li><p>Microsoft .NET Framework 4,5</p></li>
<li><p>Windows PowerShell 3,0</p>
<div class="alert">
<strong>Observação</strong><br/><p>A instalação do PowerShell 3,0 exige uma reinicialização.</p>
</div>
<div>

</div></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>O software de pré-requisito ainda não está instalado. Você deve instalá-lo antes de instalar o App-V.</p></td>
</tr>
</tbody>
</table>



## Software de pré-requisito do App-V Server


Instale o software obrigatório obrigatório para os componentes do servidor do App-V 5,1.

### O que saber antes de começar

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Conta para instalar o App-V Server</p></td>
<td align="left"><p>A conta que você usa para instalar os componentes do App-V Server deve ter:</p>
<ul>
<li><p>Direitos administrativos no computador no qual você está instalando os componentes.</p></li>
<li><p>A capacidade de consultar os serviços de domínio do Active Directory.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Porta e firewall</p></td>
<td align="left"><ul>
<li><p>Especifique uma porta onde cada componente será hospedado.</p></li>
<li><p>Adicione as regras de firewall associadas para permitir solicitações de entrada às portas especificadas.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>WebDAV (criação e controle de versão distribuídas na Web)</p></td>
<td align="left"><p>O WebDAV é desabilitado automaticamente para o serviço de gerenciamento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cenários de implantação com suporte</p></td>
<td align="left"><ul>
<li><p>Uma implantação autônoma, onde todos os componentes são implantados no mesmo servidor.</p></li>
<li><p>Uma implantação distribuída.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Cenários de implantação sem suporte</p></td>
<td align="left"><ul>
<li><p>Instalar instâncias lado a lado de várias versões do App-V Server no mesmo servidor.</p></li>
<li><p>Instalar os componentes do App-V Server em um computador que executa o núcleo do servidor ou controlador de domínio.</p></li>
</ul></td>
</tr>
</tbody>
</table>



### Software de pré-requisito do servidor de gerenciamento

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pré-requisitos e configurações necessárias</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Versão com suporte do SQL Server</p></td>
<td align="left"><p>Para ver as versões com suporte, consulte <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> configurações compatíveis do App-V 5,1 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (instalador da Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p></td>
<td align="left"><p>A instalação do PowerShell 3,0 exige uma reinicialização.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Baixar e instalar o <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p></td>
<td align="left"><p>Aplica-se somente ao Windows 7.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Pacotes redistribuíveis do Visual C++ para o Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>registro de ASP.NET de 64 bits</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Função de servidor Web do Windows Server</p></td>
<td align="left"><p>Esta função deve ser adicionada a um sistema operacional de servidor com suporte para o servidor de gerenciamento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ferramentas de gerenciamento do servidor Web (IIS)</p></td>
<td align="left"><p>Clique em <strong> ferramentas e scripts de gerenciamento do IIS </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Serviços de função de servidor Web</p></td>
<td align="left"><p><strong>Recursos comuns de HTTP:</strong></p>
<ul>
<li><p>Conteúdo estático</p></li>
<li><p>Documento padrão</p></li>
</ul>
<p><strong>Desenvolvimento de aplicativos:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>Extensibilidade .NET</p></li>
<li><p>Extensões ISAPI</p></li>
<li><p>Filtros ISAPI</p></li>
</ul>
<p><strong>Segurança</strong></p>
<ul>
<li><p>Autenticação do Windows</p></li>
<li><p>Filtragem de solicitações</p></li>
</ul>
<p><strong>Ferramentas de gerenciamento:</strong></p>
<ul>
<li><p>Console de gerenciamento do IIS</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Local de instalação padrão</p></td>
<td align="left"><p>Servidor%PROGRAMFILES%\Microsoft Application Virtualization</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Localização do banco de dados de gerenciamento</p></td>
<td align="left"><p>Nome do banco de dados SQL Server, nome da instância do banco de dados do SQL Server e nome do banco de dados</p></td>
</tr>
<tr class="even">
<td align="left"><p>Permissões do console de gerenciamento e do banco de dados de gerenciamento</p></td>
<td align="left"><p>Um usuário ou grupo que pode acessar o console de gerenciamento e o banco de dados após a conclusão da implantação. Somente esses usuários ou grupos terão acesso ao console de gerenciamento e ao banco de dados, a menos que administradores adicionais sejam adicionados usando o console de gerenciamento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome do site do serviço de gerenciamento</p></td>
<td align="left"><p>Nome para o site do console de gerenciamento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Associação de porta do serviço de gerenciamento</p></td>
<td align="left"><p>Número de porta exclusivo para o serviço de gerenciamento. Esta porta não pode ser usada por outro processo no computador.</p></td>
</tr>
</tbody>
</table>



**Importante**  
O JavaScript deve estar ativado no navegador que abre o console de gerenciamento da Web.



### Software de pré-requisito do banco de dados do Management Server

O banco de dados de gerenciamento só será necessário se você estiver usando o servidor de gerenciamento do App-V 5,1.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pré-requisitos e configurações necessárias</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (instalador da Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Pacotes redistribuíveis do Visual C++ para o Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Local de instalação padrão</p></td>
<td align="left"><p>Servidor%PROGRAMFILES%\Microsoft Application Virtualization</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome da instância personalizada do SQL Server (se aplicável)</p></td>
<td align="left"><p>Formato a ser usado: <strong> InstanceName</strong></p>
<p>Esse formato se baseia na pressuposição de que a instalação está no computador local.</p>
<p>Se você especificar o nome com o formato <strong> SVR\INSTANCE </strong> , a instalação não será bem-sucedida.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome do banco de dados personalizado (se aplicável)</p></td>
<td align="left"><p>Nome de banco de dados exclusivo.</p>
<p>Padrão: AppVManagement</p></td>
</tr>
<tr class="even">
<td align="left"><p>Local do servidor de gerenciamento</p></td>
<td align="left"><p>Conta da máquina na qual o servidor de gerenciamento está implantado.</p>
<p>Formato a ser usado: Domain\MachineAccount</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Administrador de instalação do servidor de gerenciamento</p></td>
<td align="left"><p>Conta usada para instalar o servidor de gerenciamento.</p>
<p>Formato a ser usado: Domain\AdministratorLoginName</p></td>
</tr>
<tr class="even">
<td align="left"><p>Agente de serviço do Microsoft SQL Server</p></td>
<td align="left"><p>Configure o computador do banco de dados de gerenciamento para que o serviço do Microsoft SQL Server Agent seja reiniciado automaticamente. Para obter instruções, consulte <a href="https://technet.microsoft.com/magazine/gg313742.aspx" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://technet.microsoft.com/magazine/gg313742.aspx)"> Configurar o agente do SQL Server para reiniciar serviços automaticamente </a> .</p></td>
</tr>
</tbody>
</table>



### Software de pré-requisito do servidor de publicação

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pré-requisitos e configurações necessárias</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (instalador da Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Pacotes redistribuíveis do Visual C++ para o Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>registro de ASP.NET de 64 bits</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Função de servidor Web do Windows Server</p></td>
<td align="left"><p>Esta função deve ser adicionada a um sistema operacional de servidor com suporte para o servidor de gerenciamento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ferramentas de gerenciamento do servidor Web (IIS)</p></td>
<td align="left"><p>Clique em <strong> ferramentas e scripts de gerenciamento do IIS </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Serviços de função de servidor Web</p></td>
<td align="left"><p><strong>Recursos comuns de HTTP:</strong></p>
<ul>
<li><p>Conteúdo estático</p></li>
<li><p>Documento padrão</p></li>
</ul>
<p><strong>Desenvolvimento de aplicativos:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>Extensibilidade .NET</p></li>
<li><p>Extensões ISAPI</p></li>
<li><p>Filtros ISAPI</p></li>
</ul>
<p><strong>Segurança</strong></p>
<ul>
<li><p>Autenticação do Windows</p></li>
<li><p>Filtragem de solicitações</p></li>
</ul>
<p><strong>Ferramentas de gerenciamento:</strong></p>
<ul>
<li><p>Console de gerenciamento do IIS</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Local de instalação padrão</p></td>
<td align="left"><p>Servidor%PROGRAMFILES%\Microsoft Application Virtualization</p></td>
</tr>
<tr class="even">
<td align="left"><p>URL do serviço de gerenciamento</p></td>
<td align="left"><p>URL do serviço de gerenciamento do App-V. Esta é a porta com a qual o servidor de publicação se comunica.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Arquitetura de instalação</th>
<th align="left">Formato a ser usado para a URL</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>O servidor de gerenciamento e o servidor de publicação são instalados no mesmo servidor</p></td>
<td align="left"><p><a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>O servidor de gerenciamento e o servidor de publicação são instalados em servidores diferentes</p></td>
<td align="left"><p><a href="http://MyAppvServer.MyDomain.com" data-raw-source="http://MyAppvServer.MyDomain.com">http://MyAppvServer.MyDomain.com</a></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome do site do serviço de publicação</p></td>
<td align="left"><p>Nome do site de publicação.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Associação de porta do serviço de publicação</p></td>
<td align="left"><p>Número de porta exclusivo para o serviço de publicação. Esta porta não pode ser usada por outro processo no computador.</p></td>
</tr>
</tbody>
</table>



### Software de pré-requisito do servidor de relatório

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pré-requisitos e configurações necessárias</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Versão com suporte do SQL Server</p></td>
<td align="left"><p>Para ver as versões com suporte, consulte <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> configurações compatíveis do App-V 5,1 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (instalador da Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Pacotes redistribuíveis do Visual C++ para o Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>registro de ASP.NET de 64 bits</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Função de servidor Web do Windows Server</p></td>
<td align="left"><p>Esta função deve ser adicionada a um sistema operacional de servidor com suporte para o servidor de gerenciamento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ferramentas de gerenciamento do servidor Web (IIS)</p></td>
<td align="left"><p>Clique em <strong> ferramentas e scripts de gerenciamento do IIS </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Serviços de função de servidor Web</p></td>
<td align="left"><p>Para reduzir o risco de envio de dados indesejados ou mal-intencionados para o servidor de relatórios, você deve restringir o acesso ao serviço Web de relatório de acordo com a política de segurança da sua empresa.</p>
<p><strong>Recursos comuns de HTTP:</strong></p>
<ul>
<li><p>Conteúdo estático</p></li>
<li><p>Documento padrão</p></li>
</ul>
<p><strong>Desenvolvimento de aplicativos:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>Extensibilidade .NET</p></li>
<li><p>Extensões ISAPI</p></li>
<li><p>Filtros ISAPI</p></li>
</ul>
<p><strong>Segurança</strong></p>
<ul>
<li><p>Autenticação do Windows</p></li>
<li><p>Filtragem de solicitações</p></li>
</ul>
<p><strong>Ferramentas de gerenciamento:</strong></p>
<ul>
<li><p>Console de gerenciamento do IIS</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Local de instalação padrão</p></td>
<td align="left"><p>Servidor%PROGRAMFILES%\Microsoft Application Virtualization</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome do site do serviço de relatório</p></td>
<td align="left"><p>Nome do site de relatório.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Associação de porta do serviço de relatório</p></td>
<td align="left"><p>Número de porta exclusivo para o serviço de relatório. Esta porta não pode ser usada por outro processo no computador.</p></td>
</tr>
</tbody>
</table>



### Software de pré-requisito do banco de dados de relatório

O banco de dados de relatórios só será necessário se você estiver usando o servidor de relatórios do App-V 5,1.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pré-requisitos e configurações necessárias</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (instalador da Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Pacotes redistribuíveis do Visual C++ para o Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Local de instalação padrão</p></td>
<td align="left"><p>Servidor%PROGRAMFILES%\Microsoft Application Virtualization</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome da instância personalizada do SQL Server (se aplicável)</p></td>
<td align="left"><p>Formato a ser usado: <strong> InstanceName</strong></p>
<p>Esse formato se baseia na pressuposição de que a instalação está no computador local.</p>
<p>Se você especificar o nome com o formato <strong> SVR\INSTANCE </strong> , a instalação não será bem-sucedida.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome do banco de dados personalizado (se aplicável)</p></td>
<td align="left"><p>Nome de banco de dados exclusivo.</p>
<p>Padrão: AppVReporting</p></td>
</tr>
<tr class="even">
<td align="left"><p>Local do servidor de relatório</p></td>
<td align="left"><p>Conta da máquina na qual o servidor de relatório está implantado.</p>
<p>Formato a ser usado: Domain\MachineAccount</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Administrador de instalação do Reporting Server</p></td>
<td align="left"><p>Conta usada para instalar o servidor de relatórios.</p>
<p>Formato a ser usado: Domain\AdministratorLoginName</p></td>
</tr>
<tr class="even">
<td align="left"><p>Serviço do Microsoft SQL Server e agente de serviço do Microsoft SQL Server</p></td>
<td align="left"><p>Configure esses serviços para serem associados às contas de usuário que têm acesso ao AD DS de consulta.</p></td>
</tr>
</tbody>
</table>



## Software de pré-requisito do cliente App-V


Instale o software de pré-requisito a seguir para o cliente App-V.

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
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (instalador da Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p></td>
<td align="left"><p>A instalação do PowerShell 3,0 exige uma reinicialização.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</a></p></td>
<td align="left"><p>Aplica-se somente ao Windows 7: baixar e instalar o KB.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Pacotes redistribuíveis do Visual C++ para o Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Software de pré-requisito do cliente dos serviços de área de trabalho remota


Instale o software de pré-requisito a seguir para o cliente dos serviços de área de trabalho remota do App-V.

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
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (instalador da Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p></td>
<td align="left"><p>A instalação do PowerShell 3,0 exige uma reinicialização.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</a></p></td>
<td align="left"><p>Aplica-se somente ao Windows 7: baixar e instalar o KB.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Pacotes redistribuíveis do Visual C++ para o Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Software de pré-requisito do sequenciador


**O que saber antes de instalar os pré-requisitos:**

-   Prática recomendada: o computador que executa o sequenciador deve ter as mesmas configurações de hardware e software dos computadores que executarão os aplicativos virtuais.

-   O processo de sequenciamento exige muitos recursos, portanto certifique-se de que o computador que executa o sequenciador tenha bastante memória, um processador rápido e um disco rígido rápido. Os requisitos do sistema dos aplicativos instalados localmente não podem exceder os do sequenciador. Para obter mais informações, consulte [configurações compatíveis do App-V 5,1](app-v-51-supported-configurations.md).

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
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (instalador da Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p></td>
<td align="left"><p>A instalação do PowerShell 3,0 exige uma reinicialização.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</a></p></td>
<td align="left"><p>Aplica-se somente ao Windows 7: baixar e instalar o KB.</p></td>
</tr>
</tbody>
</table>








## Tópicos relacionados


[Planejamento para o App-V 5.1](planning-for-app-v-51.md)

[Configurações com suporte ao App-V 5.1](app-v-51-supported-configurations.md)









