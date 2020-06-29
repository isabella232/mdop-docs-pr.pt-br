---
title: Avaliação do MBAM 1.0
description: Avaliação do MBAM 1.0
author: dansimp
ms.assetid: a1e2b674-eda9-4e1c-9b4c-e748470c71f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f09b06af52f5738fd50bfe727987b760d98552d9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799635"
---
# Avaliação do MBAM 1.0


Antes de implantar o Microsoft BitLocker Administration and Monitoring (MBAM) em um ambiente de produção, você deve avaliá-lo em um ambiente de laboratório. Você pode usar as informações neste tópico para configurar o MBAM em um ambiente de laboratório de servidor único para fins de avaliação apenas.

Embora as etapas de implantação reais sejam muito semelhantes ao cenário descrito em [como instalar e configurar o MBAM em um único servidor](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md), este tópico contém informações adicionais para permitir que você configure um ambiente de avaliação do MBAM no mínimo de tempo.

## Configurar o ambiente de laboratório


Mesmo quando você configura uma instância de não-produção de MBAM para avaliar em um ambiente de laboratório, você ainda deve verificar se atendeu os pré-requisitos de implantação e os requisitos de hardware e software. Para obter mais informações, consulte [pré-requisitos de implantação do MBAM 1,0](mbam-10-deployment-prerequisites.md) e [MBAM 1,0 configurações compatíveis](mbam-10-supported-configurations.md). Você também deve rever [a preparação do seu ambiente para o MBAM 1,0](preparing-your-environment-for-mbam-10.md) antes de começar a implantação de avaliação do MBAM.

### Planejar uma implantação de avaliação do MBAM

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Tarefa</th>
<th align="left">Referências</th>
<th align="left">Observações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Examine as informações de introdução sobre o MBAM para obter noções básicas sobre o produto antes de começar o planejamento de implantação.</p></td>
<td align="left"><p><a href="getting-started-with-mbam-10.md" data-raw-source="[Getting Started with MBAM 1.0](getting-started-with-mbam-10.md)">Introdução ao MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p></p>
<p>Prepare o ambiente de computação para a instalação do MBAM. Para fazer isso, você deve habilitar a criptografia de dados transparente (TDE) nas instâncias do SQL Server que hospedam bancos de dados do MBAM. Para habilitar o TDE em seu ambiente de laboratório, você pode criar um arquivo. SQL para ser executado em relação ao banco de dados mestre que está hospedado na instância do SQL Server que MBAM usará.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Você pode usar o exemplo a seguir para criar um arquivo. SQL para seu ambiente de laboratório para habilitar rapidamente o TDE na instância do SQL Server que hospedará os bancos de dados do MBAM. Esses comandos do SQL Server habilitarão o TDE usando um certificado SQL Server assinado localmente. Certifique-se de fazer backup do certificado TDE e da chave de criptografia associada ao caminho de backup local do <em> C:\backup </em> . O certificado e a chave do TDE são necessários ao recuperar o banco de dados ou mover o certificado e a chave para outro servidor que tenha a criptografia TDE no local.</p>
</div>
<div>

</div>
<pre class="syntax" space="preserve"><code>USE master;
GO
CREATE MASTER KEY ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;;
GO
CREATE CERTIFICATE tdeCert WITH SUBJECT = &#39;TDE Certificate&#39;;
GO
BACKUP CERTIFICATE tdeCert TO FILE = &#39;C:\Backup\TDECertificate.cer&#39;
   WITH PRIVATE KEY (
         FILE = &#39;C:\Backup\TDECertificateKey.pvk&#39;,
         ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;);
GO</code></pre></td>
<td align="left"><p><a href="mbam-10-deployment-prerequisites.md" data-raw-source="[MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md)">Pré-requisitos para implantação do MBAM 1.0</a></p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=269703" data-raw-source="[Database Encryption in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703)">Criptografia de banco de dados no SQL Server 2008 Enterprise Edition</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planeje e configure MBAM requisitos da política de grupo.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-group-policy-requirements.md" data-raw-source="[Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md)">Planejar Requisitos de Política de Grupo do MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planeje e crie os grupos de segurança dos serviços de domínio do Active Directory necessários e planeje os requisitos de associação do grupo de segurança local do MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)">Planejamento para Funções de Administrador do MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planeje a implantação de recursos do MBAM Server.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-server-deployment.md" data-raw-source="[Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md)">Planejar implantação de servidor MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Plano para a implantação do cliente MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-client-deployment.md" data-raw-source="[Planning for MBAM 1.0 Client Deployment](planning-for-mbam-10-client-deployment.md)">Planejar implantação de cliente MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### Executar uma implantação de avaliação do MBAM

Depois de concluir as instalações de pré-requisitos de software e planejamento necessárias para preparar o ambiente de computação para uma instalação do MBAM, você pode começar a implantação de avaliação do MBAM.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Examine as informações de configurações compatíveis com o MBAM para garantir que os computadores cliente e servidor selecionados tenham suporte para a instalação do recurso MBAM.</p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)">Configurações com suporte no MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Execute a instalação do MBAM para implantar recursos do MBAM Server em um único servidor para fins de avaliação.</p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)">Como instalar e configurar o MBAM em um servidor único</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Adicione os grupos de segurança dos serviços de domínio Active Directory que você criou durante a fase de planejamento para os grupos locais do recurso de servidor local MBAM no novo servidor MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)">Planejando funções de administrador do MBAM 1,0 </a> e <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> como gerenciar funções de administrador do MBAM</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Criar e implantar os objetos de política de grupo MBAM necessários.</p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)">Implantar Objetos de Política de Grupo no MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Implantar o software cliente do MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)">Implantando o Cliente do MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Configurar computadores de laboratório para avaliação do MBAM


Você pode alterar as configurações de frequência nos relatórios de status do cliente MBAM usando o editor do registro. No entanto, essas modificações devem ser usadas somente para fins de teste.

**Aviso**  
Este tópico descreve como alterar o registro do Windows usando o editor do registro. Se você alterar o registro do Windows incorretamente, poderá causar sérios problemas que talvez exijam a reinstalação do Windows. Você deve fazer uma cópia de backup dos arquivos do registro (System. dat e User. dat) antes de alterar o registro. A Microsoft não pode garantir que os problemas que podem ocorrer quando você alterar o registro possam ser resolvidos. Altere o registro por sua conta e risco.



### <a href="" id="modify-the-frequency-settings-on-mbam-client-status-reporting-"></a>Modificar as configurações de frequência no relatório de status do cliente MBAM

As frequências de reutilização de cliente e status de ativação do cliente MBAM têm um valor mínimo de 90 minutos quando são definidas para usar a política de grupo. Você pode alterar essas frequências em computadores cliente do MBAM editando o registro do Windows para valores menores, o que ajudará a acelerar o teste. Para modificar as configurações de frequência em MBAM relatório de status do cliente, use um editor do registro para navegar para **HKLM\\Software\\Policies\\FVE\\MDOPBitLockerManagement**, altere os valores para **ClientWakeupFrequency** e **StatusReportingFrequency** para **1** como o valor mínimo com suporte do cliente e, em seguida, reinicie o serviço de cliente de gerenciamento de BitLocker. Quando você fizer essa alteração, o cliente do MBAM se reportará a cada minuto. Você pode definir valores tão baixos apenas quando faz isso manualmente no registro.

### <a href="" id="modify-the-startup-delay-on-mbam-client-service-"></a>Modificar o atraso de inicialização no serviço de cliente MBAM

Além das frequências de reativação do cliente MBAM e status, há um atraso aleatório de até 90 minutos quando o serviço de agente cliente do MBAM é iniciado em computadores cliente. Se você não quiser o atraso aleatório, crie um valor **DWORD** de **NoStartupDelay** em **HKLM\\Software\\Microsoft\\MBAM**, defina seu valor como **1**e, em seguida, reinicie o serviço de cliente de gerenciamento de BitLocker.

## Tópicos relacionados


[Introdução ao MBAM 1.0](getting-started-with-mbam-10.md)









