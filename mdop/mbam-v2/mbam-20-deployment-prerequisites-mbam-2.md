---
title: Pré-requisitos para implantação do MBAM 2.0
description: Pré-requisitos para implantação do MBAM 2.0
author: dansimp
ms.assetid: 57d1c2bb-5ea3-457e-badd-dd9206ff0f20
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ef7ee64a3661009f18e0963d738c57a59885cb20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799787"
---
# Pré-requisitos para implantação do MBAM 2.0


Antes de iniciar a instalação do Microsoft BitLocker Administration and Monitoring (MBAM), você deve certificar-se de que você atendeu aos pré-requisitos para instalar o produto. Esta seção contém informações para ajudá-lo a planejar com êxito o ambiente computacional antes de implantar os recursos e os clientes do Microsoft BitLocker Administration and Monitoring Server. Se você estiver instalando o MBAM com o Configuration Manager, consulte [planejando implantar o MBAM com o Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) para obter pré-requisitos adicionais.

## Pré-requisitos de instalação para recursos do MBAM Server


Cada um dos recursos do MBAM Server tem pré-requisitos específicos que devem ser atendidos para que os recursos do MBAM possam ser instalados com êxito. MBAM a instalação verifica se todos os pré-requisitos são atendidos antes do início da instalação.

### Pré-requisitos para o servidor de administração e monitoramento

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
<td align="left"><p><strong>Função de servidor Web do Windows Server</strong></p></td>
<td align="left"><p>Esta função deve ser adicionada a um sistema operacional de servidor com suporte para o recurso de servidor de administração e monitoramento.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Ferramentas de gerenciamento do servidor Web (IIS)</strong></p></td>
<td align="left"><p>Selecione <strong> ferramentas e scripts de gerenciamento do IIS </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Certificado SSL</strong></p></td>
<td align="left"><p>Opcional. Para proteger a comunicação entre os clientes e os serviços Web, você precisa obter e instalar um certificado assinado por uma autoridade de segurança confiável.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Serviços de função de servidor Web</strong></p></td>
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
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Recursos do Windows Server</strong></p></td>
<td align="left"><p><strong>Recursos do .NET Framework 3.5.1:</strong></p>
<ul>
<li><p>.NET Framework 3.5.1</p></li>
<li><p>Ativação do WCF</p>
<ul>
<li><p>Ativação de HTTP</p></li>
<li><p>Ativação não HTTP</p></li>
</ul></li>
</ul>
<p><strong>Serviço de ativação de processos do Windows:</strong></p>
<ul>
<li><p>Modelo de processo</p></li>
<li><p>Ambiente .NET</p></li>
<li><p>APIs de configuração</p></li>
</ul></td>
</tr>
</tbody>
</table>



**Observação**  
Para obter uma lista dos sistemas operacionais compatíveis, consulte [configurações compatíveis do MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).



### Pré-requisitos para os relatórios de conformidade e auditoria

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
<td align="left"><p>Versão com suporte do SQL Server</p>
<p>Consulte <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> configurações compatíveis do MBAM 2,0 </a> para ver as versões compatíveis.</p></td>
<td align="left"><p>Instale o SQL Server com:</p>
<ul>
<li><p>Agrupamento SQL_Latin1_General_CP1_CI_AS</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server Reporting Services (SSRS)</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Direitos de instância do SSRS – necessários para a instalação de relatórios apenas se você estiver instalando bancos de dados em um servidor separado dos relatórios.</p></td>
<td align="left"><p>Direitos de instância obrigatórios:</p>
<ul>
<li><p>Criar pastas</p></li>
<li><p>Publicar relatórios</p></li>
</ul>
<p>O SSRS deve ser instalado e executado durante a instalação do servidor do MBAM. Configurar o SSRS no modo "nativo" e não no modo não configurado ou "SharePoint".</p></td>
</tr>
</tbody>
</table>



### Pré-requisitos para o banco de dados de recuperação

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
<td align="left"><p>Versão com suporte do SQL Server</p>
<p>Consulte <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> configurações compatíveis do MBAM 2,0 </a> para ver as versões compatíveis.</p></td>
<td align="left"><p>Instale o SQL Server com:</p>
<ul>
<li><p>Agrupamento SQL_Latin1_General_CP1_CI_AS</p></li>
<li><p>Ferramentas de gerenciamento do SQL Server</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Permissões do SQL Server necessárias</p></td>
<td align="left"><p>Permissões necessárias:</p>
<ul>
<li><p>Funções de servidor de logon da instância SQL:</p>
<ul>
<li><p>dbcreator</p></li>
<li><p>processadmin</p></li>
</ul></li>
<li><p>Direitos de instância do SQL Server Reporting Services:</p>
<ul>
<li><p>Criar pastas</p></li>
<li><p>Publicar relatórios</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Opcional-instalar o recurso de criptografia transparente de dados (TDE) disponível no SQL Server</p></td>
<td align="left"><p>O recurso TDE do SQL Server executa a criptografia e a descriptografia de e/s em tempo real dos arquivos de dados e log, que podem ajudá-lo a obedecer a várias leis, regulamentações e diretrizes estabelecidas em diversos setores.</p>
<div class="alert">
<strong>Observação</strong><br/><p>O TDE executa a descriptografia em tempo real das informações do banco de dados, o que significa que, se a conta na qual você está conectado tiver permissões para o banco de dados enquanto você estiver exibindo as informações da chave de recuperação nas tabelas do SQL Server, as informações da chave de recuperação estarão visíveis.</p>
</div>
<div>

</div>
<p>Saiba mais sobre o TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> MBAM 2,0 considerações de segurança </a> .</p></td>
</tr>
</tbody>
</table>



### Pré-requisitos para o banco de dados de conformidade e auditoria

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
<td align="left"><p>Versão com suporte do SQL Server</p>
<p>Consulte <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> configurações compatíveis do MBAM 2,0 </a> para ver as versões compatíveis.</p></td>
<td align="left"><p>Instale o SQL Server com:</p>
<ul>
<li><p>Agrupamento SQL_Latin1_General_CP1_CI_AS</p></li>
<li><p>Ferramentas de gerenciamento do SQL Server</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Permissões do SQL Server necessárias</p></td>
<td align="left"><p>Permissões necessárias:</p>
<ul>
<li><p>Funções de servidor de logon da instância SQL:</p>
<ul>
<li><p>dbcreator</p></li>
<li><p>processadmin</p></li>
</ul></li>
<li><p>Direitos de instância do SQL Server Reporting Services:</p>
<ul>
<li><p>Criar pastas</p></li>
<li><p>Publicar relatórios</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Opcional – Instale o recurso de criptografia transparente de dados (TDE) no SQL Server.</p></td>
<td align="left"><p>O recurso TDE do SQL Server executa a criptografia e a descriptografia de e/s em tempo real dos arquivos de dados e log, que podem ajudá-lo a obedecer a várias leis, regulamentações e diretrizes estabelecidas em diversos setores.</p>
<div class="alert">
<strong>Observação</strong><br/><p>O TDE executa a descriptografia em tempo real das informações do banco de dados, o que significa que, se a conta na qual você está conectado tiver permissões para o banco de dados enquanto você estiver exibindo as informações da chave de recuperação nas tabelas do SQL Server, as informações da chave de recuperação estarão visíveis.</p>
</div>
<div>

</div>
<p>Saiba mais sobre o TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> MBAM 2,0 considerações de segurança</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>O SQL Server deve ter serviços de mecanismo de banco de dados instalados e em execução durante a instalação do MBAM Server.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>O serviço do SQL Server Agent deve estar em execução e definido para inicialização automática nas instâncias selecionadas do SQL Server.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### Pré-requisitos para o portal de autoatendimento

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
<td align="left"><p>Versão com suporte do Windows Server</p>
<p>Consulte <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"> configurações compatíveis do MBAM 2,0 </a> para ver as versões compatíveis.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>ASP.NET MVC 2,0</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392270" data-raw-source="[ASP.NET MVC 2 download](https://go.microsoft.com/fwlink/?LinkId=392270)">Download do ASP.NET MVC 2</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ferramentas de gerenciamento do IIS do serviço Web</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Pré-requisitos para clientes MBAM


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
<td align="left"><p><strong>Os clientes do Windows 7 </strong> - devem ter a funcionalidade TPM (Trusted Platform Module).</p></td>
<td align="left"><p>A versão do TPM deve ser 1,2 ou posterior.</p></td>
</tr>
<tr class="even">
<td align="left"><p>O chip TPM deve estar ativado no BIOS e ser redefinido do sistema operacional.</p></td>
<td align="left"><p>Para obter mais informações, consulte a documentação do BIOS.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Clientes do Windows 8 somente </strong> : para ter o MBAM Store e gerenciar as chaves de recuperação do TPM: o provisionamento automático do TPM deve ser desativado e MBAM deve ser definido como o proprietário do TPM antes de implantar o MBAM. Para desativar o provisionamento automático do TPM, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> Disable-TpmAutoProvisioning </a> .</p>
<ul>
<li><p>O provisionamento automático de TPM deve ser desativado.</p></li>
<li><p>MBAM deve ser definido como o proprietário do TPM antes de implantar o MBAM.</p></li>
</ul></td>
<td align="left"><p>Para desativar o provisionamento automático do TPM, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> Disable-TpmAutoProvisioning </a> .</p>
<div class="alert">
<strong>Observação</strong><br/><p>Verifique se o teclado, o vídeo ou o mouse estão diretamente conectados e não são gerenciados por meio de um botão de teclado, vídeo ou mouse (KVM). Um comutador KVM pode interferir na capacidade do computador de detectar a presença física do hardware.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Tópicos relacionados


[Planejar a implantação do MBAM 2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Configurações com suporte no MBAM 2.0](mbam-20-supported-configurations-mbam-2.md)









