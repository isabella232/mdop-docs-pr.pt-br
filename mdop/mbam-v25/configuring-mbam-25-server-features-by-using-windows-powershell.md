---
title: Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell
description: Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell
author: dansimp
ms.assetid: 826429fd-29bb-44be-b47e-5f5c7d20dd1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f350a9eb96a20f50644cfdc1965b7f72741a2c29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799152"
---
# Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell


Depois de instalar o software de servidor MBAM 2,5, você pode usar os recursos de servidor configurar MBAM 2,5 usando cmdlets do Windows PowerShell ou o assistente de configuração do servidor MBAM. Este tópico descreve como configurar o MBAM 2,5 usando os cmdlets do Windows PowerShell. Para usar o assistente em vez disso, consulte [Configurando os recursos do servidor do MBAM 2,5](configuring-the-mbam-25-server-features.md).

## Neste tópico


Este tópico inclui as seguintes informações sobre como usar o Windows PowerShell para configurar o MBAM:

-   [Como carregar a ajuda do Windows PowerShell para MBAM 2,5](#bkmk-load-posh-help)

-   [Como obter ajuda sobre um cmdlet MBAM do Windows PowerShell](#bkmk-help-specific-cmdlet)

-   [Configurações que você pode fazer somente com o Windows PowerShell, mas não com o assistente de configuração do servidor do MBAM](#bkmk-config-only-posh)

-   [Pré-requisitos e requisitos para usar o Windows PowerShell para configurar recursos do MBAM Server](#bkmk-prereqs-posh-mbamsvr)

-   [Usar o Windows PowerShell para configurar o MBAM em um computador remoto](#bkmk-remote-config)

-   [Contas necessárias e parâmetros do cmdlet do Windows PowerShell correspondentes](#bkmk-reqd-posh-accts)

Para obter informações sobre os cmdlets **Get-MbamBitLockerRecoveryKey** e **Get-MbamTPMOwnerPassword** do Windows PowerShell, que são usados para administrar o MBAM, consulte [usando o Windows PowerShell para administrar MBAM o 2,5](using-windows-powershell-to-administer-mbam-25.md).

## <a href="" id="bkmk-load-posh-help"></a>Como carregar a ajuda do Windows PowerShell para MBAM 2,5


Para obter uma lista dos cmdlets do Windows PowerShell no TechNet, consulte [automação do Microsoft Desktop Optimization Pack with Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=392816).

**Para carregar a ajuda do MBAM 2,5 para cmdlets do Windows PowerShell após instalar o software do MBAM Server**

1.  Abra o Windows PowerShell ou o ambiente de script integrado do Windows PowerShell (ISE).

2.  Digite **Update-Help – módulo Microsoft. MBAM**.

## <a href="" id="bkmk-help-specific-cmdlet"></a>Como obter ajuda sobre um cmdlet MBAM do Windows PowerShell


A ajuda do Windows PowerShell para MBAM está disponível nos seguintes formatos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Formato de ajuda do Windows PowerShell</th>
<th align="left">Mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Em um prompt de comando do Windows PowerShell, digite <strong> </strong> &lt; <em> cmdlet Get-Help</em>&gt;</p></td>
<td align="left"><p>Para carregar os cmdlets do Windows PowerShell mais recentes, siga as instruções na seção anterior sobre como carregar a ajuda do Windows PowerShell para MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>No TechNet como páginas da Web</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>No centro de download como um arquivo. docx do Word</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>No centro de download como um arquivo. pdf</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-config-only-posh"></a>Configurações que você pode fazer somente com o Windows PowerShell, mas não com o assistente de configuração do servidor do MBAM


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configurações que você pode fazer somente usando o Windows PowerShell</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Instale os serviços Web em um computador separado dos aplicativos da Web.</p></td>
<td align="left"><p>Usando o assistente, você deve instalar os serviços Web e aplicativos Web no mesmo computador.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Habilite relatórios em um ponto separado do Reporting Services sem instalar todos os objetos do Configuration Manager.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Exclua todos os objetos do Configuration Manager.</p></td>
<td align="left"><p>Excluir os objetos por sua vez exclui todos os dados de conformidade do Configuration Manager.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Insira uma cadeia de conexão personalizada para os bancos de dados.</p></td>
<td align="left"><p>Exemplo: para configurar os aplicativos Web para trabalhar com o espelhamento, você deve usar o <strong> cmdlet Enable-MbamWebApplication </strong> para especificar a sintaxe apropriada do parceiro de failover na cadeia de conexão.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ignorar a validação e configurar um recurso, mesmo que a verificação de pré-requisito tenha falhado.</p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 

**Observação**  Você não pode desabilitar os bancos de dados do MBAM com um cmdlet do Windows PowerShell ou com o assistente de configuração do servidor do MBAM. Para impedir a remoção acidental dos dados de auditoria e conformidade, os administradores de banco de dados devem remover os bancos de dados manualmente.

 

## <a href="" id="bkmk-prereqs-posh-mbamsvr"></a>Pré-requisitos e requisitos para usar o Windows PowerShell para configurar recursos do MBAM Server


Antes de iniciar a configuração, complete os pré-requisitos a seguir.

**Pré-requisitos relacionados à conta**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pré-requisito</th>
<th align="left">Detalhes ou informações adicionais</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Crie as contas necessárias.</p></td>
<td align="left"><p>Consulte <strong> a seção contas necessárias e os parâmetros de cmdlet correspondentes do Windows PowerShell </strong> mais adiante neste tópico.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Contas de usuário e grupos que você passa como parâmetros para os cmdlets do Windows PowerShell devem ser contas válidas no domínio.</p></td>
<td align="left"><p>Você não pode usar contas locais.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Especifique contas no formato de nível inferior.</p></td>
<td align="left"><p>Exemplos:</p>
<p>domainNetBiosName\userdomainNetBiosName\group</p></td>
</tr>
</tbody>
</table>

 

**Pré-requisitos relacionados à permissão**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pré-requisito</th>
<th align="left">Detalhes ou informações adicionais</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Você deve ser um administrador no computador local no qual está configurando o recurso MBAM.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Use um prompt de comando elevado do Windows PowerShell para executar todos os cmdlets do Windows PowerShell.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Somente para o <strong> cmdlet Enable-MbamDatabase </strong> :</p>
<p>Você deve ter &quot; permissões criar qualquer banco de dados &quot; na instância do banco de dados de destino do Microsoft SQL Server.</p>
<p>Essa conta de usuário deve fazer parte do grupo Administradores local ou do grupo operadores de backup para registrar o gravador do serviço de cópias de sombra de volume (VSS) do MBAM.</p></td>
<td align="left"><p>Por padrão, o administrador do banco de dados ou o administrador do sistema tem as &quot; permissões CREATE ANY DATABASE necessárias &quot; .</p>
<p></p>
<p>Para obter mais informações sobre o gravador VSS, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=392814" data-raw-source="[Volume Shadow Copy Service](https://go.microsoft.com/fwlink/?LinkId=392814)"> serviço de cópias de sombra de volume </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Somente para o <strong> recurso de integração do System Center Configuration Manager </strong> :</p>
<p>O usuário que habilita esse recurso deve ter estes direitos no Configuration Manager:</p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo de direitos no Configuration Manager</th>
<th align="left">Direitos obrigatórios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Direitos de site do Configuration Manager:</p></td>
<td align="left"><p>- Leitura</p></td>
</tr>
<tr class="even">
<td align="left"><p>Direitos de coleção do Configuration Manager:</p></td>
<td align="left"><p>- Criar-excluir-ler-modificar-implantar itens de configuração</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Direitos de item de configuração do Configuration Manager:</p></td>
<td align="left"><p>- Criar-excluir-ler</p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-remote-config"></a>Usar o Windows PowerShell para configurar o MBAM em um computador remoto


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Quando usar esse recurso</strong></p></td>
<td align="left"><p>Quando você quiser configurar os recursos do servidor do MBAM 2,5 em um computador remoto. Os cmdlets do Windows PowerShell estão em execução em um computador, e você está configurando os recursos em um computador diferente e remoto.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>O que você precisa fazer</strong></p></td>
<td align="left"><p>Para usar o Windows PowerShell para configurar os recursos do MBAM 2,5 Server em um computador remoto, você deve:</p>
<ul>
<li><p>Verifique se o software do servidor MBAM 2,5 foi instalado no computador remoto.</p></li>
<li><p>Use o protocolo Credential Security Support Provider (CredSSP) para abrir a sessão do Windows PowerShell.</p></li>
<li><p>Habilite o gerenciamento remoto do Windows (WinRM). Se você não conseguir habilitar o WinRM e configurá-lo corretamente, o <strong> cmdlet New-PSSession </strong> descrito nesta tabela exibirá um erro e descreverá como corrigir o problema. Para obter mais informações sobre o WinRM, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=393064" data-raw-source="[Using Windows Remote Management](https://go.microsoft.com/fwlink/?LinkId=393064)"> usando o gerenciamento remoto do Windows </a> .</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Por que você precisa fazer isso</strong></p></td>
<td align="left"><p>Esse protocolo permite que os cmdlets do Windows PowerShell se conectem aos serviços de domínio do Active Directory usando as credenciais administrativas do usuário. Você pode receber um erro de validação se iniciar a sessão do Windows PowerShell sem esse protocolo.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Como iniciar uma sessão do Windows PowerShell com o protocolo CredSSP</strong></p></td>
<td align="left"><p>Digite o seguinte código no prompt do Windows PowerShell:</p>
<p><code>$s = New-PSSession -ComputerName xxx -Authentication Credssp -Credential xxx</code></p>
<p>O código a seguir mostra um exemplo.</p>
<p><code>$session = New-PSSession -ComputerName &lt;MBAM_server_name&gt; -Authentication Credssp -Credential (Get-Credential)</code></p>
<p><code>Enter-PSSession $session</code></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqd-posh-accts"></a>Contas necessárias e parâmetros do cmdlet do Windows PowerShell correspondentes


A tabela a seguir descreve as contas necessárias para configurar os recursos do MBAM 2,5 Server. Ele também lista o cmdlet e o parâmetro do Windows PowerShell correspondente para o qual você precisa especificar a conta durante a configuração.

Tipo de parâmetro cmdlet (usuário ou grupo) Descrição Enable-MBAMDatabase

AccessAccount

Usuário ou grupo

Especifique um usuário ou grupo de domínio que tenha permissão de leitura/gravação para esse banco de dados para dar aos aplicativos Web acesso a dados e relatórios nesse banco de dados. Se o valor for um usuário de domínio, o parâmetro **WebServiceApplicationPoolCredential** usado ao executar o cmdlet **Enable-MbamWebApplication** deve usar a mesma conta de usuário. Se o valor for um grupo usuários do domínio, a conta de domínio que é usada pelo parâmetro **WebServiceApplicationPoolCredential** deve ser um membro desse grupo.

ReportAccount

Usuário ou grupo

Especifique um grupo de usuários de domínio ou de usuário com permissão somente leitura para esse banco de dados para fornecer ao MBAM relatórios acesso aos dados de conformidade e auditoria. Se o valor for um usuário de domínio, o parâmetro **ComplianceAndAuditDBCredential** do cmdlet **Enable-MbamReport** deve usar a mesma conta de usuário. Se o valor for um grupo usuários do domínio, a conta de domínio que é usada pelo parâmetro **ComplianceAndAuditDBCredential** deve ser um membro desse grupo.

Enable-MbamReport

ComplianceAndAuditDBCredential

Usuário

Especifica as credenciais administrativas que a instância do SSRS local usa para se conectar ao banco de dados de auditoria e conformidade do MBAM. O usuário do domínio na credencial administrativa deve ser o mesmo que a conta de usuário que é usada para o parâmetro **ReportAccount** , que é usado durante a execução do cmdlet **Enable-MbamDatabase** . Se um grupo de usuários de domínio foi usado com o parâmetro **ReportAccount** , essa conta deve ser membro desse grupo.

**Importante**  A conta especificada nas credenciais administrativas deve ter direitos de usuário limitados para melhorar a segurança. Além disso, a senha da conta deve ser definida como não expirar.

 

ReportsReadOnlyAccessGroup

Grupo

Especifica o grupo de usuários do domínio que tem permissões de leitura para os relatórios. O grupo especificado deve ser o mesmo grupo usado para o parâmetro **ReportsReadOnlyAccessGroup** no cmdlet **Enable-MbamWebApplication** .

Enable-MBAMWebApplication

AdvancedHelpdeskAccessGroup

Grupo

Especifica o grupo usuários do domínio que tem acesso a todas as áreas do site de administração e monitoramento, exceto à área relatórios.

HelpdeskAccessGroup

Grupo

Especifica o grupo usuários do domínio que tem acesso às áreas **gerenciar TPM** e **unidade de recuperação** do site de administração e monitoramento.

ReportsReadOnlyAccessGroup

Grupo

Especifica o grupo usuários do domínio que tem permissão de leitura para a área **relatórios** do site de administração e monitoramento. O grupo especificado deve ser o mesmo grupo usado para o parâmetro **ReportsReadOnlyAccessGroup** no cmdlet **Enable-MbamReport** .

WebServiceApplicationPoolCredential

Usuário

Especifica o usuário do domínio a ser usado pelo pool de aplicativos para os aplicativos Web do MBAM. Ele deve ser a mesma conta de usuário de domínio especificada no parâmetro **AccessAccount** do cmdlet **Enable-MbamDatabase** . Se um grupo de usuários do domínio foi usado pelo parâmetro **AccessAccount** ao executar o cmdlet **Enable-MbamDatabase** , o usuário do domínio especificado aqui deve ser um membro desse grupo. Se você não especificar as credenciais administrativas, as credenciais administrativas que foram especificadas por qualquer aplicativo da Web habilitado anteriormente serão usadas. Todos os aplicativos da Web usam a mesma identidade do pool de aplicativos. Se for especificado várias vezes, o valor especificado mais recentemente será usado.

**Importante**  Para aumentar a segurança, defina a conta especificada nas credenciais administrativas para direitos de usuário limitados. Além disso, defina a senha da conta para nunca expirar. Verifique se a conta interna do IIS \ _IUSRS ou a conta que é usada para o parâmetro **WebServiceApplicationPoolCredential** foi adicionada à configuração de segurança **representar um cliente após autenticação** local.

Para exibir a configuração de segurança local, abra o **Editor de política de segurança local**, expanda o nó **políticas locais** , selecione o nó **atribuição de direitos de usuário** e, em seguida, clique duas vezes na opção **representar um cliente após autenticação** e **fazer logon como um trabalho em lotes** em configurações de política de grupo no painel detalhes.

 

 




## Tópicos relacionados


[Configurando os recursos de servidor do MBAM 2.5](configuring-the-mbam-25-server-features.md)

[Validando a configuração de recursos de servidor do MBAM 2.5](validating-the-mbam-25-server-feature-configuration.md)

[Usando o Windows PowerShell para administrar o MBAM 2.5](using-windows-powershell-to-administer-mbam-25.md)

 
## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





