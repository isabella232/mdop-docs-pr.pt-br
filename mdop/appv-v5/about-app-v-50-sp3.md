---
title: Sobre o App-V 5.0 SP3
description: Sobre o App-V 5.0 SP3
author: dansimp
ms.assetid: 67b5268b-edc1-4027-98b0-b3937dd70a6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: bc72f3f72c2b06470287dfe4ba3ed22abcc6068b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796632"
---
# Sobre o App-V 5.0 SP3


Use as seções a seguir para analisar informações sobre alterações significativas que se aplicam ao Microsoft Application Virtualization (App-V) 5,0 SP3:

-   [Pré-requisitos de software do App-V 5,0 SP3 e configurações com suporte](#bkmk-sp3-prereq-configs)

-   [Migrando para o App-V 5,0 SP3](#bkmk-migrate-to-50sp3)

-   [O arquivo XML do grupo de conexão criado manualmente requer a atualização para o esquema](#bkmk-update-schema-cg)

-   [Melhorias nos grupos de conexão](#bkmk-cg-improvements)

-   [Os administradores podem publicar e cancelar a publicação de pacotes para um usuário específico](#bkmk-usersid-pub-pkgs-specf-user)

-   [Habilitar apenas administradores para publicar e cancelar a publicação de pacotes](#bkmk-admins-only-pub-unpub-pkgs)

-   [A chave do registro RunVirtual dá suporte a pacotes publicados para o usuário](#bkmk-runvirtual-reg-key)

-   [Novos cmdlets do PowerShell e ajuda do cmdlet atualizável](#bkmk-posh-cmdlets-help)

-   [O diretório de aplicativos virtual primário (PVAD) está oculto, mas pode ser ativado](#bkmk-pvad-hidden)

-   [ClientVersion é necessário para visualizar os metadados de publicação do App-V](#bkmk-pub-metadata-clientversion)

-   [Os logs de eventos do App-V foram consolidados](#bkmk-event-logs-moved)

## <a href="" id="bkmk-sp3-prereq-configs"></a>Pré-requisitos de software do App-V 5,0 SP3 e configurações com suporte


Confira os links a seguir para os pré-requisitos do software App-V 5,0 SP3 e configurações com suporte.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Links para pré-requisitos e configurações com suporte</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-50-sp3-prerequisites.md" data-raw-source="[App-V 5.0 SP3 Prerequisites](app-v-50-sp3-prerequisites.md)">Pré-requisitos do App-V 5.0 SP3</a></p></td>
<td align="left"><p>Software obrigatório que você deve instalar antes de iniciar a instalação do App-V 5,0 SP3</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)">Configurações com suporte ao App-V 5.0 SP3</a></p></td>
<td align="left"><p>Sistemas operacionais com suporte e requisitos de hardware para os componentes App-V Server, Sequencer e cliente</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-migrate-to-50sp3"></a>Migrando para o App-V 5,0 SP3


Use as informações a seguir para atualizar para o App-V 5,0 SP3 a partir de versões anteriores.

### Antes de iniciar a atualização

Revise as seguintes informações antes de iniciar a atualização:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Itens a serem revisados antes da atualização</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Componentes a serem atualizados</p></td>
<td align="left"><ol>
<li><p>Servidor do App-V</p></li>
<li><p>Sequenciador</p></li>
<li><p>Cliente App-V ou serviços de área de trabalho remota do App-V (RDS)</p></li>
<li><p>Grupos de conexão</p></li>
</ol>
<div class="alert">
<strong>Observação</strong><br/><p>Para usar a interface de usuário do aplicativo cliente do App-V, baixe a versão existente do <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Microsoft Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> aplicativo de interface do usuário do cliente do Microsoft Application Virtualization 5,0 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Atualizando do App-V 4. x</p></td>
<td align="left"><p>Primeiro você deve atualizar para o App-V 5,0. Você não pode atualizar diretamente do App-V 4. x para o App-V 5,0 SP3.</p>
<p>Para obter mais informações, consulte:</p>
<ul>
<li><p><a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)">Sobre o App-V 5.0</a> </p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)">Planejamento para a migração de uma versão anterior do App-V</a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Atualizando a partir do App-V 5,0 ou posterior</p></td>
<td align="left"><p>Você pode atualizar para o App-V 5,0 SP3 diretamente de qualquer uma das seguintes versões:</p>
<ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
</ul>
<p>Para atualizar para o App-V 5,0 SP3, siga as etapas nas seções restantes deste artigo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Alterações necessárias nos pacotes e grupos de conexão após a atualização</p></td>
<td align="left"><p>Nenhuma. Pacotes e grupos de conexão continuarão a funcionar como no momento.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a>Etapas para atualizar a infraestrutura do App-V

Conclua as etapas a seguir para atualizar cada componente da infraestrutura do App-V para o App-V 5,0 SP3.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Etapa</th>
<th align="left">Para obter mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Etapa 1: Atualize o App-V Server.</p>
<p>Se você não estiver usando o servidor App-V, pule esta etapa e vá para a próxima etapa.</p>
<div class="alert">
<strong>Observação</strong><br/><p>O cliente App-V 5,0 SP3 é compatível com o servidor App-V 5,0 SP1.</p>
</div>
<div>

</div></td>
<td align="left"><p>Siga estas etapas: </p>
<ol>
<li><p>Examine as <a href="release-notes-for-app-v-50-sp3.md" data-raw-source="[Release Notes for App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)"> notas de versão do App-V 5,0 SP3 </a> para ver os problemas que podem afetar a instalação do App-v Server.</p></li>
<li><p>Siga um destes procedimentos, dependendo do método que você está usando para atualizar o banco de dados de gerenciamento e/ou banco de dados de relatórios:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método de atualização de banco de dados</th>
<th align="left">Etapa</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Installer</p></td>
<td align="left"><p>Pule esta etapa e vá para a etapa 3, "se você estiver atualizando o App-V Server..."</p></td>
</tr>
<tr class="even">
<td align="left"><p>Scripts SQL</p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Banco de dados de gerenciamento</strong></p></td>
<td align="left"><p>Para instalar ou atualizar, consulte <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> scripts do SQL para instalar ou atualizar o aplicativo de servidor de gerenciamento do App-V 5,0 SP3 falha </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Banco de dados de relatórios</strong></p></td>
<td align="left"><p>Siga as etapas em <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)"> como implantar os bancos de dados do App-V usando scripts SQL </a> .</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>
<p> </p></li>
<li><p>Se você estiver atualizando o pacote do pacote do aplicativo App-V do App-V 5,0 SP1 3 ou posterior, conclua as etapas na seção <a href="#bkmk-check-reg-key-svr" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](#bkmk-check-reg-key-svr)"> Verifique as chaves do registro após instalar o servidor App-V 5,0 SP3 </a> .</p></li>
<li><p>Siga as etapas em <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"> como implantar o servidor do App-V 5,0 </a> .</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>Etapa 2: Atualize o sequenciador do App-V.</p></td>
<td align="left"><p>Veja <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"> como instalar o sequenciador </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Etapa 3: Atualize o cliente App-V ou o App-V RDS Client.</p></td>
<td align="left"><p>Veja <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"> como implantar o cliente App-V </a> .</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-check-reg-key-svr"></a>Verifique as chaves do registro antes de instalar o App-V 5,0 SP3 Server

Esta é a etapa 3 da tabela anterior.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Quando essa etapa é necessária</strong></p></td>
<td align="left"><p>Você está atualizando a partir do App-V SP1 com qualquer pacote de hotfix subsequente instalado usando um arquivo. msp.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Quais componentes exigem que você siga esta etapa</strong></p></td>
<td align="left"><p>Somente os componentes do App-V Server que você está atualizando.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Quando precisar fazer esta etapa</strong></p></td>
<td align="left"><p>Antes de atualizar o servidor do App-V para o App-V 5,0 SP3</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>O que você precisa fazer</strong></p></td>
<td align="left"><p>Usando as informações nas tabelas a seguir, atualize cada valor de chave do registro sob <code>HKLM\Software\Microsoft\AppV\Server</code> o valor que você forneceu na instalação do servidor original. Concluir esta etapa restaura os valores do registro que podem ter sido removidos quando os pacotes de hotfix do App-V SP1 foram instalados.</p></td>
</tr>
</tbody>
</table>



**Chave ManagementDatabase**

Se você estiver instalando o banco de dados de gerenciamento, defina essas chaves de registro em `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da chave</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</p></td>
<td align="left"><p>Descreve se uma conta de acesso público é necessária para acessar bancos de dados de gerenciamento não locais. Valor é definido como "1" se for necessário.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_NAME</p></td>
<td align="left"><p>Nome do banco de dados de gerenciamento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</p></td>
<td align="left"><p>Conta usada para acesso de leitura (pública) ao banco de dados de gerenciamento.</p>
<p>Usado quando <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> é definido como 1.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>Identificador seguro (SID) da conta usada para acesso de leitura (pública) ao banco de dados de gerenciamento.</p>
<p>Usado quando <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> é definido como 1.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Instância do SQL Server para o banco de dados de gerenciamento.</p>
<p>Se o valor estiver em branco, a instância de banco de dados padrão será usada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</p></td>
<td align="left"><p>Conta usada para acesso de gravação (administrador) ao banco de dados de gerenciamento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>Identificador seguro (SID) da conta usada para acesso de gravação (administrador) ao banco de dados de gerenciamento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
<td align="left"><p>Conta de computador remoto do servidor de gerenciamento (domínio \ conta).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
<td align="left"><p>Logon de administrador de instalação para o servidor de gerenciamento (domínio \ conta).</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></td>
<td align="left"><p>Valores válidos são:</p>
<ul>
<li><p><strong>1 </strong> – o serviço de gerenciamento está no computador local, ou seja, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT está em branco.</p></li>
<li><p><strong>0 </strong> - o serviço de gerenciamento está em um computador diferente do computador local.</p></li>
</ul></td>
</tr>
</tbody>
</table>



**Chave ManagementService**

Se você estiver instalando o servidor de gerenciamento, defina essas chaves de registro em `HKLM\Software\Microsoft\AppV\Server\ManagementService` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da chave</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MANAGEMENT_ADMINACCOUNT</p></td>
<td align="left"><p>Conta ou grupo dos serviços de domínio Active Directory (AD DS) que está autorizado a gerenciar o App-V (domínio de domínio).</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Instância do SQL Server que contém o banco de dados de gerenciamento.</p>
<p>Se o valor estiver em branco, a instância de banco de dados padrão será usada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_SQL_SERVER_NAME</p></td>
<td align="left"><p>Nome do SQL Server remoto com o banco de dados de gerenciamento.</p>
<p>Se o valor estiver em branco, o computador local será usado.</p></td>
</tr>
</tbody>
</table>



**Chave ReportingDatabase**

Se você estiver instalando o banco de dados de relatórios, defina essas chaves de registro em `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da chave</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</p></td>
<td align="left"><p>Descreve se uma conta de acesso público é necessária para acessar bancos de dados de relatório não locais. Valor é definido como "1" se for necessário.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_NAME</p></td>
<td align="left"><p>Nome do banco de dados de relatório.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</p></td>
<td align="left"><p>Conta usada para acesso de leitura (pública) ao banco de dados de relatórios.</p>
<p>Usado quando <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> é definido como 1.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>Identificador seguro (SID) da conta usada para acesso de leitura (pública) ao banco de dados de relatórios.</p>
<p>Usado quando <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> é definido como 1.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Instância do SQL Server para o banco de dados de relatórios.</p>
<p>Se o valor estiver em branco, a instância de banco de dados padrão será usada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_WRITE_ACCESS_ACCOUNT</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
<td align="left"><p>Conta de computador remoto do servidor de relatório (domínio \ conta).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
<td align="left"><p>Login de administrador de instalação para o servidor de relatórios (domínio \ conta).</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_SERVER_MACHINE_USE_LOCAL</p></td>
<td align="left"><p>Valores válidos são:</p>
<ul>
<li><p><strong>1 </strong> – o serviço de relatório está no computador local, ou seja, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT está em branco.</p></li>
<li><p><strong>0 </strong> - o serviço de relatório está em um computador diferente do computador local.</p></li>
</ul></td>
</tr>
</tbody>
</table>



**Chave ReportingService**

Se você estiver instalando o servidor de relatórios, defina essas chaves de registro em `HKLM\Software\Microsoft\AppV\Server\ReportingService` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da chave</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>REPORTING_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Instância do SQL Server para o banco de dados de relatórios.</p>
<p>Se o valor estiver em branco, a instância de banco de dados padrão será usada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_SQL_SERVER_NAME</p></td>
<td align="left"><p>Nome do SQL Server remoto com o banco de dados de relatórios.</p>
<p>Se o valor estiver em branco, o computador local será usado.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-update-schema-cg"></a>O arquivo XML do grupo de conexão criado manualmente requer a atualização para o esquema


Se você estiver criando manualmente o arquivo XML do grupo de conexão e quiser usar os novos recursos "pacotes opcionais" e "usar qualquer versão" descritos em [melhorias nos grupos de conexão](#bkmk-cg-improvements), você deve especificar o seguinte esquema no arquivo XML:

`xmlns="http://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"`

Para obter exemplos e mais informações, consulte [sobre o arquivo de grupo de conexão](about-the-connection-group-file.md).

## <a href="" id="bkmk-cg-improvements"></a>Melhorias nos grupos de conexão


Você pode gerenciar grupos de conexão com mais facilidade usando pacotes opcionais e outros aprimoramentos que foram adicionados no App-V 5,0 SP3. A tabela a seguir resume as tarefas que você pode executar usando os novos recursos de grupo de conexão e links para informações mais detalhadas sobre cada tarefa.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarefa/recurso</th>
<th align="left">Descrição</th>
<th align="left">Links para obter mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Habilitar um grupo de conexão para incluir pacotes opcionais</p></td>
<td align="left"><p>Incluir pacotes opcionais em um grupo de conexão permite que você determine dinamicamente quais aplicativos serão incluídos no ambiente virtual do grupo de conexão, com base nos aplicativos aos quais os usuários estão habilitados.</p>
<p>Você não precisa gerenciar o máximo de grupos de conexão porque pode misturar pacotes opcionais e não opcionais no mesmo grupo de conexão. A combinação de pacotes permite que diferentes grupos de usuários usem o mesmo grupo de conexão, mesmo que os usuários possam ter apenas um pacote em comum.</p>
<p><strong>Exemplo </strong> : você pode habilitar um pacote com o Microsoft Office para todos os usuários, mas habilitar diferentes pacotes opcionais, que contêm diferentes plug-ins do Office para subconjuntos diferentes de usuários.</p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)">Como usar pacotes opcionais em grupos de conexão</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Cancelar a publicação ou excluir um pacote opcional sem alterar o grupo de conexões</p></td>
<td align="left"><p>Cancele a publicação ou exclua ou cancele a publicação de um pacote opcional, que está em um grupo de conexão, sem precisar desabilitar ou habilitar novamente o grupo de conexão no cliente App-V.</p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)">Como usar pacotes opcionais em grupos de conexão</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Publicar grupos de conexão que contêm pacotes publicados pelo usuário e publicados globalmente</p></td>
<td align="left"><p>Crie um grupo de conexões publicada pelo usuário que contenha pacotes publicados pelo usuário e publicados globalmente.</p></td>
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md)">Como criar um grupo de conexão com pacotes publicados pelo usuário e globalmente publicados</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Fazer um grupo de conexão ignorar a versão do pacote</p></td>
<td align="left"><p>Configure um grupo de conexão para aceitar qualquer versão de um pacote, o que permite que você atualize um pacote sem precisar desabilitar o grupo de conexão. Além disso, se houver um pacote opcional com uma versão incorreta no grupo de conexão, o pacote será ignorado e não bloqueará a criação do ambiente virtual do grupo de conexão.</p></td>
<td align="left"><p><a href="how-to-make-a-connection-group-ignore-the-package-version.md" data-raw-source="[How to Make a Connection Group Ignore the Package Version](how-to-make-a-connection-group-ignore-the-package-version.md)">Como criar um grupo de conexão para ignorar a versão do pacote</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Limitar os recursos de publicação dos usuários finais</p></td>
<td align="left"><p>Habilite somente administradores (não usuários finais) para publicar pacotes e habilitar grupos de conexão.</p></td>
<td align="left"><p>Para obter informações sobre grupos de conexão, consulte <a href="how-to-allow-only-administrators-to-enable-connection-groups.md" data-raw-source="[How to Allow Only Administrators to Enable Connection Groups](how-to-allow-only-administrators-to-enable-connection-groups.md)"> como permitir que apenas administradores habilitem grupos de conexão</a></p>
<p>Para obter informações sobre pacotes, consulte os seguintes artigos:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Link para obter mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Console de gerenciamento</p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-50.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md)">Como publicar um pacote usando o Console de Gerenciamento</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg)">Como gerenciar grupos de conexão em um computador autônomo usando o Windows PowerShell</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sistema de distribuição de software eletrônico de terceiros</p></td>
<td align="left"><p><a href="how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md" data-raw-source="[How to Enable Only Administrators to Publish Packages by Using an ESD](how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md)">Como permitir que apenas administradores publiquem pacotes usando ESD</a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p>Habilitar ou desabilitar um grupo de conexão para um usuário específico</p></td>
<td align="left"><p>Os administradores podem habilitar ou desabilitar um grupo de conexão para um usuário específico usando o <strong> parâmetro opcional – userid </strong> com os seguintes cmdlets:</p>
<ul>
<li><p>Enable-AppVClientConnectionGroup</p></li>
<li><p>Disable-AppVClientConnectionGroup</p></li>
</ul></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic)">Como gerenciar grupos de conexão em um computador autônomo usando o Windows PowerShell</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Mesclando caminhos de pacote idênticos em um diretório virtual em grupos de conexão</p></td>
<td align="left"><p>Se dois ou mais pacotes em um grupo de conexão contiverem caminhos de diretório idênticos, os caminhos serão mesclados em um único diretório virtual dentro do ambiente virtual do grupo de conexão.</p>
<p>Essa mesclagem de caminhos permite que um aplicativo em um pacote Acesse arquivos que estão em um pacote diferente.</p></td>
<td align="left"><p><a href="about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp)">Sobre o ambiente Virtual do grupo de conexão</a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-usersid-pub-pkgs-specf-user"></a>Os administradores podem publicar e cancelar a publicação de pacotes para um usuário específico


Os administradores podem usar os seguintes cmdlets para publicar ou cancelar a publicação de pacotes para um usuário específico. Para usar os cmdlets, insira o parâmetro **– userid** , seguido do Sid (identificador de segurança) do usuário. Para obter mais informações, consulte:

-   [Como gerenciar pacotes do App-V 5.0 em execução em um computador autônomo usando o PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-pub-pkg-a-user-standalone-posh)

-   [Como gerenciar pacotes do App-V 5.0 em execução em um computador autônomo usando o PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-unpub-pkg-specfc-use)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cmdlet</th>
<th align="left">Exemplos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Publicar-AppvClientPackage</p></td>
<td align="left"><p>Publish-AppvClientPackage "ContosoApplication"-Usuáriosid S-1-2-34-56789012-3456789012-345678901-2345</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cancelar publicação-AppvClientPackage</p></td>
<td align="left"><p>Cancelar publicação-AppvClientPackage "ContosoApplication"-Usuáriosid S-1-2-34-56789012-3456789012-345678901-2345</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-admins-only-pub-unpub-pkgs"></a>Habilitar apenas administradores para publicar e cancelar a publicação de pacotes


Você pode habilitar somente administradores (não usuários finais) para publicar e cancelar a publicação de pacotes usando um dos seguintes métodos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configuração da Política de Grupo</p></td>
<td align="left"><p>Navegue até o seguinte nó de objeto de política de Grupo:</p>
<p><strong>Política de configuração do computador &gt; &gt; modelos administrativos do &gt; &gt; App-V &gt; Publishing </strong> .</p>
<p>Habilite a <strong> configuração de política exigir publicação como administrador </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)">Como gerenciar pacotes do App-V 5.0 em execução em um computador autônomo usando o PowerShell</a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-runvirtual-reg-key"></a>A chave do registro RunVirtual dá suporte a pacotes publicados para o usuário


O App-V 5,0 SP3 adiciona suporte para o uso da chave do registro **RunVirtual** com aplicativos virtualizados que estão em pacotes publicados pelo usuário. A chave do registro **RunVirtual** permite executar um aplicativo instalado localmente em um ambiente virtual, juntamente com aplicativos que foram virtualizados usando o App-V.

Anteriormente, os aplicativos virtualizados nos pacotes do App-V precisavam ser publicados globalmente. Para saber mais sobre o **RunVirtual** e sobre outros métodos de execução de aplicativos instalados localmente em um ambiente virtual com aplicativos virtualizados, consulte [executando um aplicativo instalado localmente dentro de um ambiente virtual com aplicativos virtualizados](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md).

## <a href="" id="bkmk-posh-cmdlets-help"></a>Novos cmdlets do PowerShell e ajuda do cmdlet atualizável


Novos cmdlets do PowerShell e a ajuda do cmdlet atualizável estão incluídos no App-V 5,0 SP3. Para baixar os módulos do cmdlet, consulte [como carregar os cmdlets do PowerShell e obter ajuda do cmdlet](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md#bkmk-load-cmdlets).

### Novos cmdlets do PowerShell Server do App-V 5,0 SP3

Novos cmdlets do Windows PowerShell para o App-V Server foram adicionados para ajudar você a gerenciar grupos de conexão.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cmdlet</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Add-AppvServerConnectionGroupPackage</p></td>
<td align="left"><p>Acrescenta um pacote ao final de um grupo de conexão&#39;a lista de pacotes e permite que você configure o pacote como opcional e/ou sem nenhuma versão dentro do grupo de conexão.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Set-AppvServerConnectionGroupPackage</p></td>
<td align="left"><p>Permite que você edite detalhes sobre o pacote do grupo de conexão, como se ele é opcional.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Remove-AppvServerConnectionGroupPackage</p></td>
<td align="left"><p>Remove um pacote de um grupo de conexão.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-get-cmdlet-help"></a>Obtendo ajuda para os cmdlets do PowerShell

A ajuda do cmdlet está disponível nos seguintes formatos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Formato</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Como um módulo para download</p></td>
<td align="left"><p>Para obter a ajuda mais recente após o download do módulo cmdlet:</p>
<ol>
<li><p>Abra o Windows PowerShell ou o ambiente de script integrado do Windows PowerShell (ISE).</p></li>
<li><p>Digite um dos seguintes comandos para carregar os cmdlets do módulo que você deseja:</p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente App-V</th>
<th align="left">Comando para digitar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor do App-V</p></td>
<td align="left"><p>Update-Help-AppvServer do módulo</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sequenciador App-V</p></td>
<td align="left"><p>Update-Help-AppvSequencer do módulo</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cliente App-V</p></td>
<td align="left"><p>Update-Help-AppvClient do módulo</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p>No TechNet como páginas da Web</p></td>
<td align="left"><p>Consulte o nó App-V em <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> automação do Microsoft Desktop Optimization Pack with Windows PowerShell </a> .</p></td>
</tr>
</tbody>
</table>



Para obter mais informações, consulte [como carregar cmdlets do PowerShell e obter ajuda do cmdlet](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md).

## <a href="" id="bkmk-pvad-hidden"></a>O diretório de aplicativos virtual primário (PVAD) está oculto, mas pode ser ativado


O diretório de aplicativos virtual primário (PVAD) está oculto no App-V 5,0 SP3, mas você pode ativá-lo novamente e torná-lo visível usando um dos seguintes métodos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Etapas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Usar um parâmetro de linha de comando</p></td>
<td align="left"><p>Passe o <strong> parâmetro – EnablePVADControl </strong> para a <strong>Sequencer.exe</strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Criar uma subchave do registro</p></td>
<td align="left"><ol>
<li><p>No editor do registro, navegue até: <code>HKLM\SOFTWARE\Microsoft\AppV\Sequencer\Compatibility</code></p>
<div class="alert">
<strong>Observação</strong><br/><p>Se a <code>Compatibility</code> subchave não existir, você deverá criá-la.</p>
</div>
<div>

</div></li>
<li><p>Crie um valor DWORD chamado <strong> EnablePVADControl </strong> e defina o valor como <strong> 1 </strong> .</p>
<p>O valor <strong> 0 </strong> significa que o PVAD está oculto.</p></li>
</ol></td>
</tr>
</tbody>
</table>



**Saiba mais sobre o PVAD:** Ao usar o sequenciador para criar um pacote, você pode inserir qualquer caminho de instalação para o pacote. Nas versões anteriores do App-V, você deve especificar o diretório de aplicativos virtual primário (PVAD) do aplicativo como o caminho. PVAD é o diretório no qual você normalmente instalaria um aplicativo em seu computador local se não estivesse usando o App-V. Por exemplo, se você estiver instalando o Office em um computador, o PVAD normalmente seria C:\\Arquivos de Files\\Microsoft Office\\.

## <a href="" id="bkmk-pub-metadata-clientversion"></a>ClientVersion é necessário para visualizar os metadados de publicação do App-V


No App-V 5,0 SP3, você deve fornecer os seguintes valores no endereço quando consulta o servidor de publicação App-V para metadados:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Valor</th>
<th align="left">Detalhes adicionais</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>ClientVersion</strong></p></td>
<td align="left"><p>Se você omitir <strong> o </strong> parâmetro ClientVersion da consulta, os metadados excluirão os novos recursos do App-V 5,0 SP3.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>ClientOS</strong></p></td>
<td align="left"><p>Você deve fornecer esse valor apenas se selecionar sistemas operacionais específicos do cliente quando você sequenciar o pacote. Se você selecionar o padrão (todos os sistemas operacionais), não especifique esse valor na consulta.</p>
<p>Se você omitir <strong> o </strong> parâmetro ClientOS da consulta, somente os pacotes que foram sequenciados para dar suporte a qualquer sistema operacional aparecem nos metadados.</p></td>
</tr>
</tbody>
</table>



Para ver a sintaxe e os exemplos dessa consulta, consulte [exibindo os metadados de publicação do App-V Server](viewing-app-v-server-publishing-metadata.md).

## <a href="" id="bkmk-event-logs-moved"></a>Os logs de eventos do App-V foram consolidados


Os logs de eventos a seguir, anteriormente localizados em **logs de aplicativos e serviços/Microsoft/AppV/ &lt; app &gt; -V**, foram movidos para **aplicativos e logs de serviços/Microsoft/AppV/ServiceLog**.

Para exibir os logs, selecione **Exibir** &gt; **Mostrar logs analíticos e de depuração** no aplicativo visualizador de eventos.

Cliente-cliente de catálogo-cliente de integração-cliente de orquestração-cliente PackageConfig cliente-cliente de script-cliente-serviço cliente-Vemgr cliente-VFSC FilesystemMetadataLibrary ManifestLibrary PolicyLibrary subsistemas-subsistemas do AppPath-subsistemas com FTA-

## Como obter tecnologias do MDOP


O App-V faz parte do Microsoft Desktop Optimization Pack (MDOP). O MDOP faz parte do Microsoft Software Assurance. Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte [como faço para obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).






## Tópicos relacionados


[Notas de versão do App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)









