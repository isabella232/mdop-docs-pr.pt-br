---
title: Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager
description: Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager
author: dansimp
ms.assetid: 76a6047a-5c6e-42ff-af09-a6f382a69537
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9af551b1d867f61912bbf3b759574a840b0645c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799784"
---
# Pré-requisitos de servidor do MBAM 2.5 para as topologias de integração autônoma e do Configuration Manager


Antes de iniciar a instalação do Microsoft BitLocker Administration and Monitoring (MBAM), você deve concluir os pré-requisitos listados neste tópico. Esses pré-requisitos se aplicam à topologia autônoma do MBAM e à topologia de integração do System Center Configuration Manager.

Se você estiver implantando o MBAM com o System Center Configuration Manager, será necessário concluir pré-requisitos adicionais, listados em [pré-requisitos de servidor MBAM 2,5 que se aplicam somente à topologia de integração do Configuration Manager](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).

Para obter uma lista dos hardwares e sistemas operacionais compatíveis com o MBAM, consulte [configurações compatíveis do MBAM 2,5](mbam-25-supported-configurations.md).

**Importante**  
Se o BitLocker tiver sido usado sem MBAM, você deverá descriptografar a unidade e limpar o TPM usando TPM. msc. MBAM não pode apropriar-se do TPM se o computador cliente já estiver criptografado e a senha de proprietário do TPM criada.



## Funções e contas MBAM necessárias


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
<td align="left"><p>Grupos criados nos serviços de domínio Active Directory (AD DS)</p></td>
<td align="left"><p>Consulte <a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)"> planejando os grupos e contas do MBAM 2,5 </a> para obter uma descrição desses grupos e contas.</p></td>
</tr>
</tbody>
</table>



## Pré-requisitos para o banco de dados de recuperação


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
<td align="left"><p>Versão com suporte do SQL Server</p></td>
<td align="left"><p>Instale o Microsoft SQL Server com SQL_Latin1_General_CP1_CI_AS agrupamento.</p>
<p>Consulte <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> configurações compatíveis do MBAM 2,5 </a> para ver as versões compatíveis.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Permissões do SQL Server necessárias</p></td>
<td align="left"><p>Permissões necessárias:</p>
<ul>
<li><p>Funções do servidor de logon da instância do SQL Server:</p>
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
<td align="left"><p>Opcional – Instale o recurso de criptografia de dados transparente (TDE) disponível no SQL Server</p></td>
<td align="left"><p>O recurso TDE do SQL Server executa a criptografia e a descriptografia de e/s em tempo real dos arquivos de dados e log, que podem ajudá-lo a obedecer a leis, regulamentos e diretrizes aplicáveis a diversos setores.</p>
<div class="alert">
<strong>Observação</strong><br/><p>O TDE executa a descriptografia em tempo real das informações do banco de dados. Isso significa que, se você estiver exibindo as informações da chave de recuperação no banco de dados do SQL Server e estiver conectado em uma conta que tenha permissões para o banco de dados, as informações da chave de recuperação serão visíveis. Para ler mais sobre o TDE, consulte <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> considerações de segurança do MBAM 2,5 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Serviços de mecanismo de banco de dados do SQL Server</p></td>
<td align="left"><p>Os serviços de mecanismo de banco de dados do SQL Server devem ser instalados e executados durante a instalação do MBAM Server.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows PowerShell 3,0 ou posterior</p></td>
<td align="left"><p>O Windows PowerShell não precisa ser instalado no servidor de banco de dados de recuperação se você estiver usando o Windows PowerShell para configurar o banco de dados de um computador remoto.</p></td>
</tr>
</tbody>
</table>



## Pré-requisitos para o banco de dados de conformidade e auditoria


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
<td align="left"><p>Versão com suporte do SQL Server</p></td>
<td align="left"><p>Instale o SQL Server com SQL_Latin1_General_CP1_CI_AS agrupamento.</p>
<p>Consulte <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> configurações compatíveis do MBAM 2,5 </a> para ver as versões compatíveis.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Permissões do SQL Server necessárias</p></td>
<td align="left"><p>Permissões necessárias:</p>
<ul>
<li><p>Funções do servidor de logon da instância do SQL Server:</p>
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
<td align="left"><p>Opcional-instalar o recurso de criptografia de dados transparente (TDE) no SQL Server</p></td>
<td align="left"><p>O recurso TDE do SQL Server executa a criptografia e a descriptografia de e/s em tempo real dos arquivos de dados e log, que podem ajudá-lo a obedecer a leis, regulamentos e diretrizes aplicáveis a diversos setores.</p>
<p>O TDE executa a descriptografia em tempo real das informações do banco de dados. Isso significa que, se você estiver exibindo as informações da chave de recuperação no banco de dados do SQL Server e estiver conectado em uma conta que tenha permissões para o banco de dados, as informações da chave de recuperação serão visíveis. Para ler mais sobre o TDE, consulte <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> considerações de segurança do MBAM 2,5 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Serviços de mecanismo de banco de dados do SQL Server</p></td>
<td align="left"><p>Os serviços de mecanismo de banco de dados do SQL Server devem ser instalados e executados durante a instalação do MBAM Server. No entanto, o SQL Server pode ser executado remotamente; Não precisa estar no mesmo servidor em que você está instalando o software MBAM Server.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows PowerShell 3,0 ou posterior</p></td>
<td align="left"><p>O Windows PowerShell não precisa ser instalado no servidor de banco de dados de conformidade e auditoria se você estiver usando o Windows PowerShell para configurar o banco de dados de um computador remoto.</p></td>
</tr>
</tbody>
</table>



## Pré-requisitos dos relatórios


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
<td align="left"><p>Versão com suporte do SQL Server</p></td>
<td align="left"><p>Instale o SQL Server com SQL_Latin1_General_CP1_CI_AS agrupamento.</p>
<p>Consulte <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> configurações compatíveis do MBAM 2,5 </a> para ver as versões compatíveis.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server Reporting Services (SSRS)</p></td>
<td align="left"><p>O SSRS deve ser instalado e executado durante a instalação do servidor do MBAM.</p>
<p>Configurar o SSRS &quot; no &quot; modo nativo e não no modo não configurado ou &quot; SharePoint &quot; .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Direitos de instância do SSRS – necessários para configurar relatórios apenas se você estiver instalando bancos de dados em um servidor separado do servidor em que os relatórios estiverem configurados.</p></td>
<td align="left"><p>Direitos de instância obrigatórios:</p>
<ul>
<li><p>Criar pastas</p></li>
<li><p>Publicar relatórios</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Windows PowerShell 3,0 ou posterior</p></td>
<td align="left"><p>O Windows PowerShell não precisa ser instalado neste servidor de banco de dados se você estiver usando o Windows PowerShell para configurar o banco de dados de um computador remoto.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-prereqsams"></a>Pré-requisitos para o servidor de administração e monitoramento


A tabela a seguir lista os pré-requisitos de instalação do MBAM Administration and Monitoring Server.

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
<td align="left"><p>Função de servidor Web do Windows Server</p></td>
<td align="left"><p>Esta função deve ser adicionada a um sistema operacional de servidor com suporte para o recurso de servidor de administração e monitoramento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ferramentas de gerenciamento do servidor Web (IIS)</p></td>
<td align="left"><p>Clique em <strong> ferramentas e scripts de gerenciamento do IIS </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Certificado SSL</strong></p></td>
<td align="left"><p>Opcional. Para proteger a comunicação entre os computadores cliente e os serviços Web, você deve obter e instalar um certificado assinado por uma autoridade de segurança confiável.</p></td>
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
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Recursos do Windows Server</p></td>
<td align="left"><p><strong>Recursos do .NET Framework 4,5:</strong></p>
<ul>
<li><p><strong>.NET Framework 4,5 ou 4,6</strong></p>
<ul>
<li><p><strong>O Windows Server 2016 </strong> - .net Framework 4,6 já está instalado para essas versões do Windows Server, mas você deve habilitá-la.</p></li>  
<li><p><strong>O Windows Server 2012 ou o Windows Server 2012 R2 </strong> - .net Framework 4,5 já está instalado para essas versões do Windows Server, mas você deve habilitá-la.</p></li>
<li><p><strong>O Windows Server 2008 R2 </strong> - .net Framework 4,5 não está incluído no windows Server 2008 R2, portanto, você deve <a href="https://go.microsoft.com/fwlink/?LinkId=392318" data-raw-source="[download Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?LinkId=392318)"> baixar o Microsoft .NET Framework 4,5 </a> e instalá-lo separadamente.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Se você estiver atualizando do MBAM 2,0 ou do MBAM 2,0 SP1 e precisar instalar o .NET Framework 4,5, consulte as <a href="release-notes-for-mbam-25.md" data-raw-source="[Release Notes for MBAM 2.5](release-notes-for-mbam-25.md)"> notas de versão do MBAM 2,5 </a> para obter uma etapa adicional necessária para fazer com que os sites funcionem.</p>
</div>
<div>

</div></li>
</ul></li>
<li><p><strong>Ativação do WCF</strong></p>
<ul>
<li><p>Ativação de HTTP</p></li>
<li><p>Ativação não HTTP (somente para Windows Server 2008, 2012 e 2012 R2)</p>
<p></p></li>
</ul></li>
<li><p><strong>Ativação de TCP</strong></p></li>
</ul>
<p><strong>Serviço de ativação de processos do Windows:</strong></p>
<ul>
<li><p>Modelo de processo</p></li>
<li><p>Ambiente do .NET Framework</p></li>
<li><p>APIs de configuração</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>ASP.NET MVC 4,0</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)">Download do ASP.NET MVC 4</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>SPN (nome da entidade de serviço)</p></td>
<td align="left"><p>Os aplicativos Web exigem um SPN para o nome do host virtual na conta de domínio que você usa para os pools de aplicativos Web.</p>
<p>Se seus direitos administrativos permitirem que você crie SPNs nos serviços de domínio Active Directory, o MBAM criará o SPN para você. Consulte <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)"> setspn </a> para obter informações sobre os direitos necessários para criar SPNs.</p>
<p>Se você não tiver direitos administrativos para criar SPNs, você deve solicitar que os administradores do Active Directory em sua organização criem o SPN para você usando o comando a seguir.</p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p>No exemplo de código, o nome do host virtual é mbamvirtual.contoso.com e a conta de domínio usada para os pools de aplicativos Web é contoso\mbamapppooluser.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Se você estiver configurando o balanceamento de carga, use a mesma conta de pool de aplicativos em todos os servidores.</p>
</div>
<div>

</div>
<p>Para obter mais informações sobre como registrar SPNs para nomes de host totalmente qualificados, NetBIOS e nomes de host, consulte <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> planejando como proteger os sites do MBAM </a> .</p></td>
</tr>
</tbody>
</table>



## Pré-requisitos para o portal de autoatendimento


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
<td align="left"><p>Versão com suporte do Windows Server</p></td>
<td align="left"><p>Consulte <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"> configurações compatíveis do MBAM 2,5 </a> para ver as versões compatíveis.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ASP.NET MVC 4,0</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)">Download do ASP.NET MVC 4</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ferramentas de gerenciamento do IIS do serviço Web</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>SPN (nome da entidade de serviço)</p></td>
<td align="left"><p>Os aplicativos Web exigem um SPN para o nome do host virtual na conta de domínio que você usa para os pools de aplicativos Web.</p>
<p>Se seus direitos administrativos permitirem que você crie SPNs nos serviços de domínio Active Directory, o MBAM criará o SPN para você. Consulte <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)"> setspn </a> para obter informações sobre os direitos necessários para criar SPNs.</p>
<p>Se você não tiver direitos administrativos para criar SPNs, você deve perguntar aos administradores do Active Directory em seus administradores de organização em sua organização para criar o SPN para você usando o comando a seguir.</p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p>No exemplo de código, o nome do host virtual é mbamvirtual.contoso.com e a conta de domínio usada para os pools de aplicativos Web é contoso\mbamapppooluser.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Se você estiver configurando o balanceamento de carga, use a mesma conta de pool de aplicativos em todos os servidores.</p>
</div>
<div>

</div>
<p>Para obter mais informações sobre como registrar SPNs para nomes de host totalmente qualificados, NetBIOS e nomes de host, consulte <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> planejando como proteger os sites do MBAM </a> .</p></td>
</tr>
</tbody>
</table>



## Pré-requisitos para a estação de trabalho de gerenciamento


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
<td align="left"><p>Antes de instalar o cliente do MBAM, baixe os modelos de política de grupo do MBAM em <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)"> como obter modelos de política de grupo do MDOP (. admx) </a> e configure-os com as configurações que você deseja implementar na sua empresa para a criptografia de unidade de disco BitLocker.</p></td>
<td align="left"><p>Antes de instalar o cliente do MBAM, faça o seguinte:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">O que fazer</th>
<th align="left">Onde obter instruções</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Copiar os modelos de política de grupo do MBAM</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Copiando os modelos de Política de Grupo do MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Editar as configurações de política de grupo</p></td>
<td align="left"><p><a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)">Editando as configurações de Política de Grupo do MBAM 2.5</a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>





## Tópicos relacionados


[Preparando seu ambiente para o MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Planejando a implantação do MBAM 2.5](planning-to-deploy-mbam-25.md)

[Configurações com suporte no MBAM 2.5](mbam-25-supported-configurations.md)




## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




