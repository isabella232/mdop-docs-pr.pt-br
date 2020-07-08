---
title: Considerações de segurança do MBAM 2.0
description: Considerações de segurança do MBAM 2.0
author: dansimp
ms.assetid: 0aa5c6e2-d92c-4e30-9f6a-b48abb667ae5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 04dc9b667faddecab629b50f4c5d909fd7b2829e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799367"
---
# Considerações de segurança do MBAM 2.0


Este tópico contém uma breve visão geral sobre as contas e grupos, arquivos de log e outras considerações relacionadas à segurança para administração e monitoramento do Microsoft BitLocker (MBAM). Para obter mais informações, siga os links neste artigo.

## Considerações gerais sobre segurança


**Compreender os riscos de segurança.** O risco mais sério da administração e do monitoramento do Microsoft BitLocker é que sua funcionalidade pode ser seqüestrada por um usuário não autorizado que poderia então reconfigurar a criptografia do BitLocker e obter dados da chave de criptografia do BitLocker em clientes do MBAM. No entanto, a perda de funcionalidade do MBAM por um curto período de tempo, devido a um ataque de negação de serviço, geralmente não tem um impacto catastrófico, ao contrário, por exemplo, e-mail, comunicações de rede, luz e energia.

**Proteja seus computadores fisicamente**. Não há segurança sem segurança física. Um invasor que obtém acesso físico a um servidor MBAM pode usá-lo para atacar toda a base de clientes. Todos os possíveis ataques físicos devem ser considerados de alto risco e diminuídos adequadamente. Os servidores MBAM devem ser armazenados em uma sala de servidor seguro com acesso controlado. Proteja esses computadores quando os administradores não estiverem fisicamente presentes fazendo com que o sistema operacional trave o computador ou usando um protetor de tela seguro.

**Aplicar as atualizações de segurança mais recentes a todos os computadores**. Mantenha-se informado sobre novas atualizações para sistemas operacionais, Microsoft SQL Server e MBAM ao assinar o serviço de notificação de segurança ( <https://go.microsoft.com/fwlink/?LinkId=28819> ).

**Use senhas fortes ou frases secretas**. Sempre use senhas fortes com 15 caracteres ou mais para todas as contas de administrador do MBAM e do MBAM. Nunca use senhas em branco. Para obter mais informações sobre os conceitos de senha, consulte o White Paper "senhas de conta e políticas" no TechNet ( <https://go.microsoft.com/fwlink/?LinkId=30009> ).

## Contas e grupos no MBAM


A prática recomendada para gerenciar contas de usuário é criar grupos globais de domínio e adicionar contas de usuário a eles. Em seguida, adicione as contas globais do domínio aos grupos locais MBAM necessários nos servidores MBAM.

### Grupos do ActiveDirectoryDomainServices

Nenhum grupo do Active Directory é criado automaticamente durante o processo de configuração do MBAM. No entanto, é recomendável que você crie os seguintes grupos globais do ActiveDirectoryDomainServices para gerenciar as operações do MBAM.

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
<td align="left"><p>Crie esse grupo para gerenciar os membros do grupo local de usuários da assistência técnica avançada do MBAM criados durante a configuração do MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Acesso ao banco de dados de auditoria de conformidade MBAM</p></td>
<td align="left"><p>Crie esse grupo para gerenciar os membros do grupo local de acesso ao banco de dados de auditoria de conformidade do MBAM criado durante a configuração do MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuários da assistência técnica MBAM</p></td>
<td align="left"><p>Crie esse grupo para gerenciar os membros do grupo local usuários da assistência técnica do MBAM, criados durante a configuração do MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Recuperação do MBAM e acesso ao banco de dados de hardware</p></td>
<td align="left"><p>Crie esse grupo para gerenciar os membros do grupo local de MBAM de acesso ao banco de dados de recuperação e de dados de hardware criado durante a instalação do MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuários do relatório MBAM</p></td>
<td align="left"><p>Crie esse grupo para gerenciar os membros do grupo local usuários do relatório do MBAM criado durante a configuração do MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Administradores do sistema do MBAM</p></td>
<td align="left"><p>Crie esse grupo para gerenciar os membros do grupo local Administradores do sistema MBAM criados durante a instalação do MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Isenções de criptografia BitLocker</p></td>
<td align="left"><p>Crie esse grupo para gerenciar contas de usuário que devem ser isentadas da criptografia do BitLocker a partir de computadores nos quais eles fazem logon.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------mbam-server-local-groups"></a> Grupos locais do MBAM Server

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
<td align="left"><p>Os membros deste grupo melhoraram o acesso aos recursos de suporte técnico do MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Acesso ao banco de dados de auditoria de conformidade MBAM</p></td>
<td align="left"><p>Contém as máquinas que têm acesso ao banco de dados de auditoria e conformidade do MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuários da assistência técnica MBAM</p></td>
<td align="left"><p>Os membros desse grupo têm acesso a alguns dos recursos de suporte técnico da MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Recuperação do MBAM e acesso ao banco de dados de hardware</p></td>
<td align="left"><p>Contém as máquinas que têm acesso ao banco de dados de recuperação do MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuários do relatório MBAM</p></td>
<td align="left"><p>Os membros desse grupo têm acesso aos relatórios de conformidade e auditoria do MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Administradores do sistema do MBAM</p></td>
<td align="left"><p>Os membros desse grupo têm acesso a todos os recursos do MBAM.</p></td>
</tr>
</tbody>
</table>

 

### Conta de serviço de relatórios SSRS

A conta de serviço relatórios SSRS fornece o contexto de segurança para executar os relatórios do MBAM disponíveis por meio do SSRS. Ele é configurado durante a configuração do MBAM.

Ao configurar a conta de serviço relatórios SSRS, especifique uma conta de usuário de domínio e configure a senha para nunca expirar.

**Observação**  Se você alterar o nome da conta de serviço após a implantação do MBAM, será necessário reconfigurar a fonte de dados de relatório para usar as novas credenciais da conta de serviço. Caso contrário, você não será capaz de acessar o portal de suporte técnico.

 

## <a href="" id="---------mbam-log-files"></a> Arquivos de log do MBAM


Os seguintes arquivos de log de instalação do MBAM são criados na pasta% Temp% do usuário de instalação durante a configuração do MBAM:

**Arquivos de log de instalação do MBAM Server**

<a href="" id="msi-five-random-characters--log"></a>MSI <em> &lt; cinco caracteres aleatórios &gt; </em> . log  
Registra as ações executadas durante a instalação do MBAM e a instalação do recurso MBAM Server.

<a href="" id="installcompliancedatabase-log"></a>InstallComplianceDatabase. log  
Registra as ações executadas para criar a configuração de banco de dados de auditoria e conformidade com o MBAM.

<a href="" id="installkeycompliancedatabase-log"></a>InstallKeyComplianceDatabase. log  
Registra ações executadas para criar o banco de dados de recuperação do MBAM.

<a href="" id="addhelpdeskdbauditusers-log"></a>AddHelpDeskDbAuditUsers. log  
Registra ações executadas para criar os logons do SQL Server no banco de dados de conformidade e conformidade do MBAM e autorizar o serviço Web do HelpDesk ao banco de dados para relatórios.

<a href="" id="addhelpdeskdbusers-log"></a>AddHelpDeskDbUsers. log  
Registra as ações executadas para autorizar serviços Web para o banco de dados para recuperação de chave e criar logons para o banco de dados de recuperação do MBAM.

<a href="" id="addkeycompliancedbusers-log"></a>AddKeyComplianceDbUsers. log  
Registra as ações executadas para autorizar os serviços Web a MBAM banco de dados de auditoria e conformidade para relatórios de conformidade.

<a href="" id="addrecoveryandhardwaredbusers-log"></a>AddRecoveryAndHardwareDbUsers. log  
Registra ações executadas para autorizar serviços Web ao banco de dados de recuperação do MBAM para recuperação de chave.

**Observação**  Para obter arquivos de log de instalação do MBAM adicionais, você precisa instalar o MBAM usando o pacote msiexec e a &lt; opção/l Location &gt; . Os arquivos de log são criados no local especificado.

 

**Arquivos de log de configuração do cliente MBAM**

<a href="" id="msi-five-random-characters--log"></a>MSI <em> &lt; cinco caracteres aleatórios &gt; </em> . log  
Registra as ações executadas durante a instalação do cliente MBAM.

## <a href="" id="---------mbam-database-tde-considerations"></a> Considerações sobre o TDE do banco de dados MBAM


O recurso de criptografia de dados transparente (TDE) que está disponível no SQL Server é uma instalação opcional para as instâncias de banco de dados que hospedam os recursos de banco de dados do MBAM.

Com o TDE, você pode executar a criptografia em nível de banco de dados completa em tempo real. O TDE é a melhor opção para a criptografia em massa para atender aos padrões de segurança de dados corporativos ou conformidade normativa. O TDE funciona no nível de arquivo, que é semelhante a dois recursos do Windows: o sistema de arquivos com criptografia (EFS) e a criptografia de unidade de disco BitLocker, ambos também criptografam dados no disco rígido. O TDE não substitui a criptografia, o EFS ou o BitLocker no nível da célula.

Quando o TDE está habilitado em um banco de dados, todos os backups são criptografados. Portanto, deve-se tomar cuidado especial para garantir que o certificado que foi usado para proteger a chave de criptografia do banco de dados tenha backup e seja mantido com o backup do banco de dados. Se esse certificado (ou certificados) for perdido, os dados serão ilegíveis. Faça backup do certificado juntamente com o banco de dados. Cada backup de certificado deve ter dois arquivos. Esses dois arquivos devem ser arquivados (idealmente separadamente do arquivo de backup de banco de dados para segurança). Você também pode considerar o uso do recurso EKM (gerenciamento de chaves extensível) (consulte gerenciamento extensível de chaves) para armazenamento e manutenção de chaves usadas para TDE.

Para obter um exemplo de como habilitar o TDE para instâncias de banco de dados do MBAM, consulte [avaliando MBAM 2,0](evaluating-mbam-20-mbam-2.md).

Para obter mais informações sobre o TDE no SQLServer 2008, consulte [criptografia do SQL Server]( https://go.microsoft.com/fwlink/?LinkId=299883).

## Tópicos relacionados


[Segurança e privacidade para o MBAM 2.0](security-and-privacy-for-mbam-20-mbam-2.md)

 

 





