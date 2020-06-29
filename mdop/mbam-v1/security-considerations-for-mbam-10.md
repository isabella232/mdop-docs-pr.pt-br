---
title: Considerações de segurança para o MBAM 1.0
description: Considerações de segurança para o MBAM 1.0
author: dansimp
ms.assetid: 5e1c8b8c-235b-4a92-8b0b-da50dca17353
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b06c343c8193293dde91bc7af2541f35f332d261
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799823"
---
# Considerações de segurança para o MBAM 1.0


Este tópico contém uma breve visão geral das contas e dos grupos, dos arquivos de log e outras considerações relacionadas à segurança do Microsoft BitLocker Administration and Monitoring (MBAM). Para obter mais informações, siga os links deste artigo.

## Considerações gerais sobre segurança


**Compreender os riscos de segurança.** O risco mais sério para o MBAM é que sua funcionalidade pode ser seqüestrada por um usuário não autorizado que poderia reconfigurar a criptografia do BitLocker e obter dados da chave de criptografia BitLocker em clientes do MBAM. No entanto, a perda de funcionalidade do MBAM por um curto período de tempo devido a um ataque de negação de serviço geralmente não teria um impacto catastrófico.

**Proteja seus computadores fisicamente**. A segurança está incompleta sem segurança física. Qualquer pessoa com acesso físico a um servidor MBAM pode atacar potencialmente toda a base de clientes. Qualquer ataque físico potencial deve ser considerado de alto risco e diminuído apropriadamente. Os servidores MBAM devem ser armazenados em uma sala de servidor fisicamente seguro com acesso controlado. Proteja esses computadores quando os administradores não estiverem fisicamente presentes fazendo com que o sistema operacional trave o computador ou usando um protetor de tela seguro.

**Aplicar as atualizações de segurança mais recentes a todos os computadores**. Mantenha-se informado sobre novas atualizações para sistemas operacionais, Microsoft SQL Server e MBAM ao assinar o serviço de notificação de segurança ( <https://go.microsoft.com/fwlink/p/?LinkId=28819> ).

**Use senhas fortes ou frases secretas**. Sempre use senhas fortes com 15 caracteres ou mais para todas as contas de administrador do MBAM e do MBAM. Nunca use senhas em branco. Para obter mais informações sobre os conceitos de senha, consulte o White Paper "senhas de conta e políticas" no TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).

## Contas e grupos no MBAM


Uma prática recomendada para o gerenciamento de contas de usuários é criar grupos globais de domínio e adicionar contas de usuário a eles. Em seguida, adicione as contas globais do domínio aos grupos locais MBAM necessários nos servidores MBAM.

### Grupos do ActiveDirectoryDomainServices

Nenhum grupo é criado automaticamente durante a configuração do MBAM. No entanto, você deve criar os seguintes grupos globais do ActiveDirectoryDomainServices para gerenciar as operações do MBAM.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome do Grupo</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Usuários avançados da assistência técnica MBAM</p></td>
<td align="left"><p>Crie esse grupo para gerenciar os membros do grupo local de usuários da assistência técnica avançada do MBAM que foram criados durante a configuração do MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Acesso ao banco de dados de auditoria de conformidade MBAM</p></td>
<td align="left"><p>Crie esse grupo para gerenciar os membros do grupo local de acesso ao banco de dados de auditoria de conformidade do MBAM criado durante a configuração do MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuários de hardware MBAM</p></td>
<td align="left"><p>Crie esse grupo para gerenciar os membros do grupo local usuários de hardware do MBAM que foi criado durante a configuração do MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuários da assistência técnica MBAM</p></td>
<td align="left"><p>Crie esse grupo para gerenciar os membros do grupo local usuários da assistência técnica do MBAM que foi criado durante a configuração do MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Recuperação do MBAM e acesso ao banco de dados de hardware</p></td>
<td align="left"><p>Crie esse grupo para gerenciar os membros do grupo local de recuperação de banco de dados de MBAM de dados de recuperação e de hardware criado durante a configuração do MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuários do relatório MBAM</p></td>
<td align="left"><p>Crie esse grupo para gerenciar os membros do grupo local usuários do relatório do MBAM que foi criado durante a configuração do MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Administradores do sistema do MBAM</p></td>
<td align="left"><p>Crie esse grupo para gerenciar os membros do grupo local de administradores do sistema MBAM criados durante a instalação do MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Isenções de criptografia BitLocker</p></td>
<td align="left"><p>Crie esse grupo para gerenciar contas de usuário que devem ser isentadas da criptografia do BitLocker a partir de computadores nos quais eles fazem logon.</p></td>
</tr>
</tbody>
</table>

 

### Grupos locais do MBAM Server

A instalação do MBAM cria grupos locais para dar suporte às operações do MBAM. Você deve adicionar os grupos globais do ActiveDirectoryDomainServices aos grupos locais MBAM apropriados para configurar as permissões de segurança MBAM e acesso a dados.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome do Grupo</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Usuários avançados da assistência técnica MBAM</p></td>
<td align="left"><p>Os membros deste grupo têm acesso expandido aos recursos de assistência técnica do Microsoft BitLocker Administration and Monitoring.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Acesso ao banco de dados de auditoria de conformidade MBAM</p></td>
<td align="left"><p>Esse grupo contém as máquinas que têm acesso ao banco de dados de auditoria de conformidade do MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuários de hardware MBAM</p></td>
<td align="left"><p>Os membros desse grupo têm acesso a alguns dos recursos de recursos de hardware da administração e do monitoramento do Microsoft BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuários da assistência técnica MBAM</p></td>
<td align="left"><p>Os membros desse grupo têm acesso a alguns dos recursos de helpdesk da administração e do monitoramento do BitLocker da Microsoft.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Recuperação do MBAM e acesso ao banco de dados de hardware</p></td>
<td align="left"><p>Esse grupo contém os computadores que têm acesso ao banco de dados de recuperação e hardware do MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuários do relatório MBAM</p></td>
<td align="left"><p>Os membros desse grupo têm acesso aos relatórios de conformidade e auditoria do Microsoft BitLocker Administration and Monitoring.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Administradores do sistema do MBAM</p></td>
<td align="left"><p>Os membros desse grupo têm acesso a todos os recursos da administração e do monitoramento do Microsoft BitLocker.</p></td>
</tr>
</tbody>
</table>

 

### Conta de acesso a relatórios do SSRS

A conta de serviço relatórios do SQL Server Reporting Services (SSRS) fornece o contexto de segurança para executar os relatórios do MBAM disponíveis por meio do SSRS. Esta conta é configurada durante a configuração do MBAM.

## Arquivos de log do MBAM


Durante a configuração do MBAM, os seguintes arquivos de log de instalação do MBAM são criados na pasta% Temp% do usuário que instala o

**Arquivos de log de instalação do MBAM Server**

<a href="" id="msi-five-random-characters--log"></a>MSI <em> &lt; cinco caracteres aleatórios &gt; </em> . log  
Registra as ações executadas durante a instalação do MBAM e a instalação do recurso MBAM Server.

<a href="" id="installcompliancedatabase-log"></a>InstallComplianceDatabase. log  
Registra as ações executadas para criar a configuração do banco de dados de status de conformidade do MBAM.

<a href="" id="installkeycompliancedatabase-log"></a>InstallKeyComplianceDatabase. log  
Registra as ações executadas para criar a recuperação do MBAM e o banco de dados de hardware.

<a href="" id="addhelpdeskdbauditusers-log"></a>AddHelpDeskDbAuditUsers. log  
Registra as ações executadas para criar os logons do SQL Server no banco de dados de status de conformidade do MBAM e autorizar o serviço Web de helpdesk ao banco de dados para relatórios.

<a href="" id="addhelpdeskdbusers-log"></a>AddHelpDeskDbUsers. log  
Registra as ações executadas para autorizar serviços Web para o banco de dados para recuperação de chave e criar logons para o banco de dados de recuperação e hardware do MBAM.

<a href="" id="addkeycompliancedbusers-log"></a>AddKeyComplianceDbUsers. log  
Registra as ações executadas para autorizar os serviços Web a MBAM banco de dados de status de conformidade para relatórios de conformidade.

<a href="" id="addrecoveryandhardwaredbusers-log"></a>AddRecoveryAndHardwareDbUsers. log  
Registra as ações executadas para autorizar serviços Web a recuperar e MBAM o banco de dados de hardware para a recuperação de chave.

**Observação**  Para obter arquivos de log de instalação do MBAM adicionais, você deve instalar a administração e o monitoramento do Microsoft BitLocker usando o pacote **msiexec** e a opção de localização **/l** &lt; &gt; . Os arquivos de log são criados no local especificado.

 

**Arquivos de log de configuração do cliente MBAM**

<a href="" id="msi-five-random-characters--log"></a>MSI <em> &lt; cinco caracteres aleatórios &gt; </em> . log  
Registra as ações executadas durante a instalação do cliente MBAM.

## Considerações sobre o TDE do banco de dados MBAM


O recurso de criptografia de dados transparente (TDE) disponível no SQL Server 2008 é um pré-requisito de instalação obrigatório para as instâncias de banco de dados que hospedarão os recursos de banco de dados do MBAM.

Com o TDE, você pode executar a criptografia em nível de banco de dados completa em tempo real. TDE é uma opção bem adequada para a criptografia em massa para atender aos padrões de segurança de dados corporativos ou conformidade normativa. O TDE funciona no nível de arquivo, que é semelhante a dois recursos do Windows: o sistema de arquivos com criptografia (EFS) e a criptografia de unidade de disco BitLocker, ambos também criptografam dados no disco rígido. O TDE não substitui a criptografia, o EFS ou o BitLocker no nível da célula.

Quando o TDE está habilitado em um banco de dados, todos os backups são criptografados. Portanto, deve-se tomar cuidado especial para garantir que o certificado que foi usado para proteger a chave de criptografia do banco de dados (DEK) seja backup e mantido com o backup do banco de dados. Sem um certificado, os dados serão ilegíveis. Faça backup do certificado juntamente com o banco de dados. Cada backup de certificado deve ter dois arquivos; esses dois arquivos devem ser arquivados. É melhor arquivá-los separadamente do arquivo de backup do banco de dados para segurança.

Para obter um exemplo de como habilitar o TDE para instâncias de banco de dados do MBAM, consulte [avaliando MBAM 1,0](evaluating-mbam-10.md).

Para obter mais informações sobre o TDE no SQLServer 2008, consulte [criptografia de banco de dados no SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703).

## Tópicos relacionados


[Segurança e Privacidade para o MBAM 1.0](security-and-privacy-for-mbam-10.md)

 

 





