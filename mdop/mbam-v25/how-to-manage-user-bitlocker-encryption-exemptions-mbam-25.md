---
title: Como gerenciar isenções de criptografia BitLocker para usuários
description: Como gerenciar isenções de criptografia BitLocker para usuários
author: dansimp
ms.assetid: f582ab82-5bb5-4cd3-ad7c-483240533cf9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4224a0fb6d905c2362659efe7cf05e16756f7c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799943"
---
# Como gerenciar isenções de criptografia BitLocker para usuários


O monitoramento e a administração do Microsoft BitLocker (MBAM) permitem que você destenha usuários dos requisitos de criptografia de unidade de disco BitLocker.

Para isolar os usuários da proteção BitLocker, você precisa:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarefa</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Criar uma infraestrutura para dar suporte a usuários isentos.</p></td>
<td align="left"><p>Exemplos dessa infraestrutura incluem aos usuários um número de telefone de contato, uma página da Web ou um endereço para correspondência que eles podem usar para solicitar uma isenção.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Adicione o usuário isento a um grupo de segurança para um objeto de política de grupo configurado especificamente para usuários isentos.</p></td>
<td align="left"><p>Quando os membros desse grupo de segurança entram em um computador, a configuração de política de grupo do usuário isenta o usuário da proteção do BitLocker. A configuração de política de grupo do usuário substitui a política do computador e o computador permanecerá isento da criptografia do BitLocker.</p>
<div class="alert">
<strong>Observação</strong><br/><p>O MBAM não enact a política de criptografia se o computador já estiver protegido pelo BitLocker e se o usuário estiver isento de o usuário. No entanto, se outro usuário que não está isento da política de criptografia entrar no computador, ocorrerá a criptografia.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



As etapas a seguir descrevem o que ocorre quando os usuários finais solicitam uma isenção do processo de isenção de criptografia de unidade BitLocker por meio do cliente MBAM ou de qualquer processo que sua organização usa. Você deve definir configurações da política de grupo do MBAM para permitir que os usuários finais solicitem uma isenção da criptografia de unidade de disco BitLocker.

1.  Quando os usuários finais entram em um computador que precisa ser criptografado, eles recebem uma notificação de que o computador será criptografado. Eles podem selecionar a **isenção de solicitação** e adiar a criptografia selecionando **adiar**ou podem selecionar **Iniciar criptografia** para aceitar a criptografia do BitLocker.

    **Observação**  
    A seleção de **isenção de solicitação** adia a proteção do BitLocker até o tempo máximo definido na política de isenção do usuário.



2.  Se os usuários finais selecionarem **solicitação de isenção**, receberão uma notificação informando que eles devem contatar o grupo de administração do BitLocker da organização. Dependendo de como a configuração de **política de isenção de usuário** é configurada, os usuários recebem um ou mais dos seguintes métodos de contato:

    -   Número de telefone

    -   URL da página da Web

    -   Endereço para correspondência

3.  Depois que a solicitação de isenção é recebida, o administrador do MBAM decide se deseja adicionar o usuário ao grupo de serviços de domínio Active Directory (AD DS) de isenção BitLocker.

4.  Depois que um usuário final envia uma solicitação de isenção, o cliente MBAM relata o usuário como "isento temporariamente". Em seguida, o cliente aguarda um número especificado de dias, que os administradores de ti configuram, antes de verificar a conformidade do computador novamente. Se o administrador do MBAM rejeita a solicitação de isenção, a opção de solicitação de isenção é desativada, o que impede que o usuário solicite a isenção novamente.

O monitoramento e a administração do Microsoft BitLocker (MBAM) permitem que você destenha usuários dos requisitos de criptografia de unidade de disco BitLocker.

Para isolar os usuários da proteção BitLocker, você precisa:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarefa</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Criar uma infraestrutura para dar suporte a usuários isentos.</p></td>
<td align="left"><p>Exemplos dessa infraestrutura incluem aos usuários um número de telefone de contato, uma página da Web ou um endereço para correspondência que eles podem usar para solicitar uma isenção.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Adicione o usuário isento a um grupo de segurança para um objeto de política de grupo configurado especificamente para usuários isentos.</p></td>
<td align="left"><p>Quando os membros desse grupo de segurança entram em um computador, a configuração de política de grupo do usuário isenta o usuário da proteção do BitLocker. A configuração de política de grupo do usuário substitui a política do computador e o computador permanecerá isento da criptografia do BitLocker.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Se o computador já estiver protegido pelo BitLocker, a política de isenção de usuário não terá efeito. Além disso, se outro usuário entrar em um computador que não está isento da política de criptografia, ocorrerá a criptografia.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



As etapas a seguir descrevem o que ocorre quando os usuários finais solicitam uma isenção do processo de isenção de criptografia de unidade BitLocker por meio do cliente MBAM ou de qualquer processo que sua organização usa. Você deve definir configurações da política de grupo do MBAM para permitir que os usuários finais solicitem uma isenção da criptografia de unidade de disco BitLocker.

1.  Quando os usuários finais entram em um computador que precisa ser criptografado, eles recebem uma notificação de que o computador será criptografado. Eles podem selecionar a **isenção de solicitação** e adiar a criptografia selecionando **adiar**ou podem selecionar **Iniciar criptografia** para aceitar a criptografia do BitLocker.

    **Observação**  
    A seleção de **isenção de solicitação** adia a proteção do BitLocker até o tempo máximo definido na política de isenção do usuário.



2.  Se os usuários finais selecionarem **solicitação de isenção**, receberão uma notificação informando que eles devem contatar o grupo de administração do BitLocker da organização. Dependendo de como a configuração de **política de isenção de usuário** é configurada, os usuários recebem um ou mais dos seguintes métodos de contato:

    -   Número de telefone

    -   URL da página da Web

    -   Endereço para correspondência

3.  Depois que a solicitação de isenção é recebida, o administrador do MBAM decide se deseja adicionar o usuário ao grupo de serviços de domínio Active Directory (AD DS) de isenção BitLocker.

4.  Depois que um usuário final envia uma solicitação de isenção, o cliente MBAM relata o usuário como "isento temporariamente". Em seguida, o cliente aguarda um número especificado de dias, que os administradores de ti configuram, antes de verificar a conformidade do computador novamente. Se o administrador do MBAM rejeita a solicitação de isenção, a opção de solicitação de isenção é desativada, o que impede que o usuário solicite a isenção novamente.

**Para isentar um usuário da criptografia de unidade de disco BitLocker**

1.  Crie um grupo de segurança do AD DS que será usado para gerenciar isenções de usuário dos requisitos de criptografia do BitLocker.

2.  Crie um objeto de política de grupo usando os modelos de política de grupo Administração e monitoramento do Microsoft BitLocker.

3.  Associe o objeto de política de grupo ao grupo do AD DS que você criou na etapa anterior. As configurações de política para os usuários isentos estão localizadas em: modelos administrativos do **userconfiguration** &gt; **Administrative Templates** &gt; **componentes** &gt; **do Windows MBAM (gerenciamento de BitLocker)**.

4.  Para o grupo de segurança que você criou para usuários isentos de BitLocker, adicione os nomes dos usuários que estão solicitando uma isenção.

    Quando um usuário entra em um computador controlado pelo BitLocker, o cliente MBAM verifica a configuração da política de isenção do usuário. Se o computador já estiver criptografado, a proteção BitLocker não será suspensa. Se o computador não estiver criptografado, o MBAM não solicitará que o usuário criptografe.

    **Importante**  
    Cenários de computador compartilhado exigem consideração especial quando você estiver usando isenções de usuário BitLocker. Se um usuário não isento entrar em um computador compartilhado com um usuário isento, o computador pode estar criptografado.




## Tópicos relacionados


[Administrando os recursos do MBAM 2.5](administering-mbam-25-features.md)

[Planejamento para os requisitos de Política de Grupo do MBAM 2.5](planning-for-mbam-25-group-policy-requirements.md)




## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




