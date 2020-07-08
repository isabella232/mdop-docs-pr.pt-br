---
title: Como gerenciar isenções de criptografia BitLocker para usuários
description: Como gerenciar isenções de criptografia BitLocker para usuários
author: dansimp
ms.assetid: 1bfd9d66-6a9a-4d0e-b54a-e5a6627f5ada
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d5530701fd208d42dc1f6774fac11ee9ca2036b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799599"
---
# Como gerenciar isenções de criptografia BitLocker para usuários


O Microsoft BitLocker Administration and Monitoring (MBAM) pode ser usado para gerenciar a proteção do BitLocker isentando os usuários se houver usuários que não precisam ou querem que suas unidades sejam criptografadas.

Para isolar os usuários da proteção BitLocker, uma organização precisará criar uma infraestrutura para dar suporte a usuários isentos, como conceder ao usuário um número de telefone, uma página da Web ou endereço para correspondência a ser usado para solicitar uma isenção. Além disso, um usuário isento precisará ser adicionado a um grupo de segurança para um objeto de política de grupo criado especificamente para usuários isentos. Quando os membros desse grupo de segurança fazem logon em um computador, a configuração de política de grupo do usuário mostra que o usuário está isento da proteção do BitLocker. A configuração de política de grupo do usuário substitui a política do computador e o computador permanecerá isento da criptografia do BitLocker.

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
<td align="left"><p>A proteção do BitLocker é imposta no computador</p></td>
<td align="left"><p>A proteção BitLocker não é imposta no computador</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Isento de usuário</strong></p></td>
<td align="left"><p>A proteção BitLocker não é imposta no computador</p></td>
<td align="left"><p>A proteção BitLocker não é imposta no computador</p></td>
</tr>
</tbody>
</table>

 

**Para isentar um usuário da criptografia do BitLocker**

1.  Crie um grupo de segurança ActiveDirectoryDomainServices que será usado para gerenciar isenções de usuário dos requisitos de criptografia do BitLocker.

2.  Crie uma configuração de objeto de política de grupo usando o modelo de política de grupo Administração e monitoramento do Microsoft BitLocker e associe-o ao grupo do Active Directory que você criou na etapa anterior. As configurações de política para usuários isentos podem ser encontradas em **UserConfiguration\\Administrative Templates\\Windows COMPONENTS\\MDOP MBAM (gerenciamento de BitLocker)**.

3.  Depois de criar um grupo de segurança para usuários isentos do BitLocker, adicione a este grupo os nomes dos usuários que estão solicitando uma isenção. Quando os usuários fizerem logon em um computador controlado pelo BitLocker, o cliente MBAM verificará a configuração de política de isenção de usuário e suspenderá a proteção dependendo se o usuário fizer parte do grupo de segurança de isenção de BitLocker.

    **Importante**  Cenários de computador compartilhado exigem consideração especial ao usar isenções de usuário. Se um usuário não isento fizer logon em um computador compartilhado com um usuário isento, o computador pode estar criptografado.

     

**Para permitir que os usuários solicitem uma isenção da criptografia do BitLocker**

1.  Se você configurou políticas de isenção de usuário usando o modelo de política MBAM, um usuário pode solicitar uma isenção da proteção BitLocker por meio do cliente MBAM.

2.  Quando os usuários fazem logon em um computador que precisa ser criptografado, eles recebem uma notificação de que o computador está sendo criptografado. Eles podem selecionar a **isenção de solicitação** e adiar a criptografia selecionando **mais tarde**ou selecionar **Iniciar** para aceitar a criptografia do BitLocker.

    **Observação**  A seleção de **isenção de solicitação** adia a proteção do BitLocker até o tempo máximo definido na política de isenção do usuário.

     

3.  Se os usuários selecionarem **solicitar isenção**, receberão uma notificação solicitando que entrem em contato com o grupo de administração do BitLocker da sua organização. Dependendo de como a configuração de política de isenção de usuário é configurada, os usuários recebem um ou mais dos seguintes métodos de contato:

    -   Número de telefone

    -   URL da página da Web

    -   Endereço para correspondência

    Depois que a solicitação de isenção for recebida, o administrador do MBAM poderá decidir se é adequado para adicionar o usuário ao grupo do Active Directory de isenção de BitLocker.

    **Observação**  Depois que um usuário envia uma solicitação de isenção, o agente MBAM relata o usuário como "isento temporariamente" e, em seguida, aguarda um número de dias configurável antes de verificar a conformidade do computador novamente. Se o administrador do MBAM rejeita a solicitação de isenção, a opção de solicitação de isenção é desativada, o que impede que o usuário possa solicitar a isenção novamente.

     

## Tópicos relacionados


[Administrando os Recursos do MBAM 2.0](administering-mbam-20-features-mbam-2.md)

 

 





