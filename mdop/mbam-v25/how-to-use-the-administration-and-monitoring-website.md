---
title: Como usar o site Administração e Monitoramento
description: Como usar o site Administração e Monitoramento
author: dansimp
ms.assetid: bb96a4e8-d4f4-4e6f-b7db-82d96998bfa6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b9597e29a5a7a6236cb351d8d6d1f682edce3cf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796151"
---
# Como usar o site Administração e Monitoramento


O site de administração e monitoramento, também chamado de suporte técnico, é uma interface administrativa para a criptografia de unidade de disco BitLocker. Use o site para analisar relatórios, recuperar as unidades de usuários finais e gerenciar os usuários finais TPMs, conforme descrito nas seções a seguir.

**Observação**  Se você estiver usando o MBAM na topologia autônoma, Visualizar todos os relatórios do site Administração e monitoramento. Se você estiver usando a topologia de integração do Configuration Manager, exiba todos os relatórios no Configuration Manager, exceto o relatório de auditoria de recuperação, que você continuará a ver no site de administração e monitoramento. Para obter mais informações sobre relatórios, consulte [monitoramento e relatórios de conformidade do BitLocker com o MBAM 2,5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md).

 

## Funções necessárias para usar o site de administração e monitoramento


Para acessar áreas específicas do site de administração e monitoramento, você deve ter uma das funções a seguir, que são grupos que você cria no Active Directory. Você pode usar qualquer nome para estes grupos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Account</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Usuários avançados da assistência técnica MBAM</p></td>
<td align="left"><p>Fornece acesso a todas as áreas do site de administração e monitoramento. Os usuários que têm essa função só inserem a chave de recuperação, e não o nome de usuário e o domínio do usuário final, ao ajudar os usuários finais a recuperarem suas unidades. Se um usuário for membro do grupo usuários da assistência técnica do MBAM e do grupo usuários avançados do MBAM helpdesk, as permissões do grupo usuários da assistência avançada do MBAM substituirão as permissões do grupo usuários da assistência técnica do MBAM.</p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuários da assistência técnica MBAM</p></td>
<td align="left"><p>Fornece acesso às áreas gerenciar TPM e recuperação de unidade do site de administração e monitoramento. As pessoas que têm essa função devem preencher todos os campos, incluindo o nome do domínio e o nome da conta do usuário final, quando eles usam uma área.</p>
<p>Se um usuário for membro do grupo usuários da assistência técnica do MBAM e do grupo usuários avançados do MBAM helpdesk, as permissões do grupo usuários da assistência avançada do MBAM substituirão as permissões do grupo usuários da assistência técnica do MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuários do relatório MBAM</p></td>
<td align="left"><p>Fornece acesso aos relatórios na <strong> </strong> área relatórios do site de administração e monitoramento.</p></td>
</tr>
</tbody>
</table>

 

## Tarefas que você pode executar no site Administração e monitoramento


A tabela a seguir resume as tarefas que você pode executar no site de administração e monitoramento e fornece links para obter mais informações sobre cada tarefa.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarefa</th>
<th align="left">Área do site na qual você acessa a tarefa</th>
<th align="left">Descrição</th>
<th align="left">Para obter mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Consulte os relatórios</p></td>
<td align="left"><p>Relatórios</p></td>
<td align="left"><p>Permite que você execute relatórios para monitorar o uso do BitLocker, a conformidade e a atividade de recuperação de chave. Os relatórios fornecem dados sobre conformidade com a empresa, computadores individuais e quem solicitou as chaves de recuperação ou o pacote OwnerAuth do TPM para um computador específico.</p></td>
<td align="left"><p><a href="viewing-mbam-25-reports-for-the-stand-alone-topology.md" data-raw-source="[Viewing MBAM 2.5 Reports for the Stand-alone Topology](viewing-mbam-25-reports-for-the-stand-alone-topology.md)">Exibindo relatórios do MBAM 2.5 referentes à topologia autônoma</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Determinar o status de criptografia BitLocker de computadores perdidos ou roubados</p></td>
<td align="left"><p>Relatórios</p></td>
<td align="left"><p>Determine se um volume foi criptografado se o computador for perdido ou roubado.</p></td>
<td align="left"><p><a href="how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md" data-raw-source="[How to Determine BitLocker Encryption State of Lost Computers](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)">Como determinar o estado de criptografia BitLocker de computadores perdidos</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Recuperar drives perdidos</p></td>
<td align="left"><p>Recuperação de unidade</p></td>
<td align="left"><p>Recuperar unidades que são:</p>
<ul>
<li><p>No modo de recuperação</p></li>
<li><p>Foram movidos</p></li>
<li><p>Estão corrompidos</p></li>
</ul></td>
<td align="left"><ul>
<li><p><a href="how-to-recover-a-drive-in-recovery-mode-mbam-25.md" data-raw-source="[How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)">Como recuperar uma unidade no modo de recuperação</a></p></li>
<li><p><a href="how-to-recover-a-moved-drive-mbam-25.md" data-raw-source="[How to Recover a Moved Drive](how-to-recover-a-moved-drive-mbam-25.md)">Como recuperar uma unidade movida</a></p></li>
<li><p><a href="how-to-recover-a-corrupted-drive-mbam-25.md" data-raw-source="[How to Recover a Corrupted Drive](how-to-recover-a-corrupted-drive-mbam-25.md)">Como recuperar uma unidade corrompida</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Redefinir um bloqueio de TPM</p></td>
<td align="left"><p>Gerenciar TPM</p></td>
<td align="left"><p>Fornece acesso a dados do TPM que foram coletados pelo cliente MBAM. Em um bloqueio de TPM, use o site Administração e monitoramento para recuperar o arquivo de senha necessário para desbloquear o TPM.</p></td>
<td align="left"><p><a href="how-to-reset-a-tpm-lockout-mbam-25.md" data-raw-source="[How to Reset a TPM Lockout](how-to-reset-a-tpm-lockout-mbam-25.md)">Como redefinir um bloqueio de TPM</a></p></td>
</tr>
</tbody>
</table>

 


## Tópicos relacionados


[Realizando o gerenciamento do BitLocker com o MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





