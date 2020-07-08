---
title: Planejamento para contas e grupos do MBAM 2.5
description: Planejamento para contas e grupos do MBAM 2.5
author: dansimp
ms.assetid: 73bb9fe5-5900-4b6f-b271-ade62991fca1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 3431c3602685a4f96cb4c1333700107ba9c38b96
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799745"
---
# Planejamento para contas e grupos do MBAM 2.5


Este tópico lista as funções e as contas que você deve criar nos serviços de domínio Active Directory (AD DS) para fornecer direitos de segurança e acesso para os bancos de dados do Microsoft BitLocker Administration and Monitoring (MBAM), relatórios e aplicativos Web. Para cada função e conta, o campo correspondente no assistente de configuração do servidor MBAM é fornecido. Para obter uma lista dos cmdlets e parâmetros do Windows PowerShell correspondentes a essas contas, consulte [Configurando os recursos do servidor do MBAM 2,5 usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md#bkmk-reqd-posh-accts).

**Observação**  
O MBAM não dá suporte ao uso de contas de serviço gerenciadas.



## Contas de banco de dados


Crie as contas a seguir para o banco de dados de conformidade e auditoria e o banco de dados de recuperação.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da conta e finalidade</th>
<th align="left">Tipo de conta</th>
<th align="left">Campo do assistente de configuração do MBAM Server correspondente a essa conta</th>
<th align="left">Descrição do campo assistente de configuração do servidor MBAM que corresponde a essa conta</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Banco de dados de auditoria e conformidade e banco de dados de recuperação ou grupo de leitura/gravação para relatórios</p></td>
<td align="left"><p>Usuário ou grupo</p></td>
<td align="left"><p>Usuário ou grupo de domínio de acesso de leitura/gravação</p></td>
<td align="left"><p>Usuário ou grupo de domínio que tem acesso de leitura/gravação para o banco de dados de conformidade e auditoria e o banco de dados de recuperação para permitir que os aplicativos Web acessem os dados e relatórios nestes bancos de dados.</p>
<p>Se você inserir um nome de usuário nesse campo, ele deverá ser o mesmo valor do valor no <strong> campo conta de domínio do pool de aplicativos de serviço Web </strong> na <strong> página Configurar aplicativos Web </strong> .</p>
<p>Se você inserir um nome de grupo nesse campo, o valor no <strong> campo conta de domínio do pool de aplicativos do serviço Web </strong> na <strong> página Configurar aplicativos Web </strong> deve ser um membro do grupo que você inserir nesse campo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>O banco de dados de auditoria e o usuário ou grupo de auditoria somente leitura para relatórios</p></td>
<td align="left"><p>Usuário ou grupo</p></td>
<td align="left"><p>Usuário ou grupo de domínio de acesso somente leitura</p></td>
<td align="left"><p>Nome do usuário ou grupo que terá acesso somente leitura ao banco de dados de conformidade e auditoria para permitir que os relatórios acessem os dados de conformidade e auditoria neste banco de dados.</p>
<p>Se você inserir um nome de usuário nesse campo, ele deverá ser o mesmo usuário que você especificou no <strong> campo conta de domínio de banco de dados de auditoria e conformidade </strong> na <strong> página Configurar relatórios </strong> .</p>
<p>Se você inserir um nome de grupo nesse campo, o valor especificado no <strong> campo conta de domínio de banco de dados de auditoria e de auditoria </strong> na <strong> página Configurar relatórios </strong> deve ser um membro do grupo especificado nesse campo.</p></td>
</tr>
</tbody>
</table>



## Contas de relatório


Crie as contas a seguir para o recurso relatórios.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da conta/finalidade</th>
<th align="left">Tipo de conta</th>
<th align="left">Campo do assistente de configuração do MBAM Server correspondente a essa conta</th>
<th align="left">Descrição do campo assistente de configuração do servidor MBAM que corresponde a essa conta</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Grupo de acesso de domínio somente leitura de relatórios</p></td>
<td align="left"><p>Grupo</p></td>
<td align="left"><p>Grupo de domínio da função de relatório</p></td>
<td align="left"><p>Especifica o grupo de usuários do domínio que tem acesso somente leitura aos relatórios no site de administração e monitoramento. O grupo especificado deve ser o mesmo que você especificou para o parâmetro de grupo de acesso somente leitura de relatórios quando os aplicativos Web estão habilitados.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Conta de usuário do domínio de banco de dados de auditoria e conformidade</p></td>
<td align="left"><p>Usuário</p></td>
<td align="left"><p>Conta de domínio de banco de dados de auditoria e conformidade</p></td>
<td align="left"><p>Conta e senha de usuário do domínio que a instância local do SQL Server Reporting Services usa para acessar o banco de dados de auditoria e conformidade. Esta conta exige <strong> logon como direitos de lote </strong> para o servidor do SQL Server Reporting Services.</p>
<p>Se o valor que você inserir no <strong> campo usuário ou grupo de domínio somente leitura </strong> na <strong> página configurar bancos de dados </strong> for um nome de usuário, você deverá digitar esse mesmo valor neste campo.</p>
<p>Se o valor que você inserir no <strong> campo usuário ou grupo de domínio somente leitura </strong> na <strong> página configurar bancos de dados </strong> for um nome de grupo, o valor que você inserir nesse campo deve ser um membro desse grupo.</p>
<p>Configure a senha desta conta para nunca expirar. A conta de usuário deve ser capaz de acessar todos os dados que estão disponíveis para o grupo de usuários do MBAM Reports.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-helpdesk-roles"></a>Contas de site de administração e monitoramento (Help Desk)


Crie as contas a seguir para o site de administração e monitoramento.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da conta/finalidade</th>
<th align="left">Tipo de conta</th>
<th align="left">Campo do assistente de configuração do MBAM Server correspondente a essa conta</th>
<th align="left">Descrição do campo assistente de configuração do servidor MBAM que corresponde a essa conta</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Conta de domínio do pool de aplicativos do serviço Web</p></td>
<td align="left"><p>Usuário</p></td>
<td align="left"><p>Conta de domínio do pool de aplicativos do serviço Web</p></td>
<td align="left"><p>Conta de usuário do domínio a ser usada pelo pool de aplicativos para os aplicativos Web.</p>
<p>Se você inserir um nome de usuário no <strong> campo usuário ou grupo do domínio de acesso de leitura/gravação </strong> na <strong> página configurar bancos de dados </strong> , você deverá digitar esse mesmo valor neste campo.</p>
<p>Se você inserir um nome de grupo no <strong> campo usuário ou grupo do domínio de acesso de leitura/gravação </strong> na <strong> página configurar bancos de dados </strong> , o valor que você inserir nesse campo deverá ser um membro desse grupo.</p>
<p>Se você não especificar credenciais, as credenciais que foram especificadas para qualquer aplicativo da Web habilitado anteriormente serão usadas. Todos os aplicativos Web devem usar as mesmas credenciais de pool de aplicativos. Se você especificar credenciais diferentes para diferentes aplicativos da Web, o valor especificado mais recentemente será usado.</p>
<div class="alert">
<strong>Importante</strong><br/><p>Para aumentar a segurança, defina a conta especificada nas credenciais para ter direitos de usuário limitados.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Grupo de acesso de usuários avançados da assistência técnica MBAM</p></td>
<td align="left"><p>Grupo</p></td>
<td align="left"><p>Usuários avançados da assistência técnica MBAM</p></td>
<td align="left"><p>Grupo de usuários do domínio cujos membros têm acesso a todas as áreas de recuperação do site de administração e monitoramento. Os usuários que têm essa função precisam inserir apenas a chave de recuperação, e não o domínio do usuário final e o nome de usuário, ao ajudar os usuários finais a recuperarem suas unidades. Se um usuário for membro do grupo usuários da assistência técnica do MBAM e do grupo usuários avançados do MBAM helpdesk, as permissões de grupo usuários da assistência avançada do MBAM poderão substituir as permissões do grupo MBAM helpdesk.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Grupo de acesso de usuários da assistência técnica MBAM</p></td>
<td align="left"><p>Grupo</p></td>
<td align="left"><p>Usuários da assistência técnica MBAM</p></td>
<td align="left"><p>Grupo de usuários do domínio cujos membros têm acesso às áreas gerenciar TPM e unidade de recuperação do site de administração e monitoramento do MBAM. As pessoas que têm essa função devem preencher todos os campos, incluindo o nome do domínio e o nome da conta do usuário final, quando eles usam qualquer uma dessas opções.</p>
<p>Se um usuário for membro do grupo usuários da assistência técnica do MBAM e do grupo usuários avançados do MBAM helpdesk, as permissões de grupo usuários da assistência avançada do MBAM poderão substituir as permissões do grupo MBAM helpdesk.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Grupo de acesso de usuários de relatório MBAM</p></td>
<td align="left"><p>Grupo</p></td>
<td align="left"><p>Usuários do relatório MBAM</p></td>
<td align="left"><p>Grupo de usuários do domínio cujos membros têm acesso somente leitura aos relatórios na área relatórios do site Administração e monitoramento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Grupo de usuários de migração de dados MBAM</p></td>
<td align="left"><p>Grupo</p></td>
<td align="left"><p>Usuários de migração de dados do MBAM</p></td>
<td align="left"><p>Grupo de usuários de domínio opcional cujos membros têm permissões para gravar dados no MBAM usando o serviço de recuperação e hardware do MBAM em execução no servidor MBAM. Essa conta geralmente é usada com os cmdlets Write-MBAM * para gravar dados de recuperação e TPM do Active Directory no banco de dados do MBAM.</p>
<p>Para obter mais informações, consulte <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> MBAM 2,5 considerações de segurança </a> .</p></td>
</tr>
</tbody>
</table>




## Tópicos relacionados


[Preparando seu ambiente para o MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Pré-requisitos para implantação do MBAM 2.5](mbam-25-deployment-prerequisites.md)



## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





