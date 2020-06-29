---
title: Como gerenciar isenções de criptografia BitLocker para usuários
description: Como gerenciar isenções de criptografia BitLocker para usuários
author: dansimp
ms.assetid: 48d69721-504f-4524-8a04-b9ce213ac9b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c3d70558a65c3288174413d6c36cc9c77bc9eaa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796131"
---
# Como gerenciar isenções de criptografia BitLocker para usuários


O Microsoft BitLocker Administration and Monitoring (MBAM) pode ser usado para gerenciar a proteção do BitLocker, isentando os usuários que não precisam ou querem que suas unidades sejam criptografadas.

Para isolar os usuários da proteção BitLocker, uma organização deve primeiro criar uma infraestrutura para dar suporte a tais isenções. A infraestrutura de suporte pode incluir um número de telefone de contato, uma página da Web ou um endereço para correspondência para solicitar a isenção. Além disso, qualquer usuário isento precisará ser adicionado a um grupo de segurança para a política de grupo criada especificamente para usuários isentos. Quando os membros desse grupo de segurança fizerem logon em um computador, a política de grupo de usuários mostrará que o usuário está isento da proteção do BitLocker. A política do usuário substitui a política do computador e o computador permanecerá isento da criptografia do BitLocker.

**Observação**  Se o computador já estiver protegido pelo BitLocker, a política de isenção de usuário não terá efeito.

 

A tabela a seguir mostra como a proteção do BitLocker é aplicada com base na maneira como as isenções são definidas.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Status do usuário</th>
<th align="left">Computador não isento</th>
<th align="left">Isento de computador</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>O usuário não está isento</strong></p></td>
<td align="left"><p>A proteção do BitLocker é imposta no computador.</p></td>
<td align="left"><p>A proteção do BitLocker não é imposta no computador.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Isento de usuário</strong></p></td>
<td align="left"><p>A proteção do BitLocker não é imposta no computador.</p></td>
<td align="left"><p>A proteção do BitLocker não é imposta no computador.</p></td>
</tr>
</tbody>
</table>

 

**Para isentar um usuário da criptografia do BitLocker**

1.  Crie um grupo de segurança ActiveDirectoryDomainServices que será usado para gerenciar isenções de usuário da criptografia do BitLocker.

2.  Crie uma configuração de objeto de política de grupo usando o modelo de política de grupo do MBAM. Associe o objeto de política de grupo ao grupo do Active Directory que você criou na etapa anterior. Para obter mais informações sobre as configurações de política necessárias para permitir que os usuários solicitem a isenção da criptografia BitLocker, consulte a seção configurar política de isenção de usuário em [planejamento para requisitos de política de grupo do MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md).

3.  Depois de criar um grupo de segurança para usuários isentos do BitLocker, adicione a este grupo os nomes dos usuários que estão solicitando isenção. Quando um usuário faz logon em um computador controlado pelo BitLocker, o cliente MBAM verifica a configuração da política de isenção do usuário e suspende a proteção de acordo com a forma como o usuário faz parte do grupo de segurança de isenção de BitLocker.

    **Observação**  Cenários de computador compartilhado exigem uma consideração especial sobre isenção de usuário. Se um usuário não isento fizer logon em um computador compartilhado com um usuário isento, o computador pode estar criptografado.

     

**Para permitir que os usuários solicitem a isenção da criptografia BitLocker**

1.  Depois de configurar políticas de isenção de usuários pela usingwith modelo de política MBAM, um usuário pode solicitar isenção de proteção BitLocker por meio do cliente MBAM.

2.  Quando um usuário faz logon em um computador marcado como **compatível** na lista de compatibilidade de hardware do MBAM, o sistema apresenta ao usuário uma notificação de que o computador está sendo criptografado. O usuário pode selecionar **solicitação de isenção** e adiar a criptografia selecionando **mais tarde**ou selecionar **Iniciar** para aceitar a criptografia do BitLocker.

    **Observação**  Selecionar a **isenção de solicitação** adiará a proteção do BitLocker até o tempo máximo definido na política de isenção do usuário.

     

3.  Quando um usuário seleciona a **isenção de solicitação**, o usuário é notificado a contatar o grupo de administração do BitLocker da organização. Dependendo de como a configuração de política de isenção de usuário é configurada, os usuários recebem um ou mais dos seguintes métodos de contato:

    -   Número de telefone

    -   URL da página da Web

    -   Endereço para correspondência

    Depois de enviar a solicitação, o administrador do MBAM pode decidir se é apropriado adicionar o usuário ao grupo do Active Directory de isenção do BitLocker.

    **Observação**  Quando o limite de tempo adiado da política de isenção do usuário tiver expirado, os usuários não verão a opção de solicitar isenção à política de criptografia. Nesse momento, os usuários devem entrar em contato com o administrador do MBAM diretamente para receber a isenção da proteção do BitLocker.

     

## Tópicos relacionados


[Administrando os Recursos do MBAM 1.0](administering-mbam-10-features.md)

 

 





