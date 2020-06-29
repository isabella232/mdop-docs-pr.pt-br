---
title: Como recuperar uma unidade no modo de recuperação
description: Como recuperar uma unidade no modo de recuperação
author: dansimp
ms.assetid: e126eaf8-9ae7-40fe-a28e-dbd78d26859e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d15f33f461e60fceeed3acbce3a0c82b02b56f98
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799258"
---
# Como recuperar uma unidade no modo de recuperação


Este tópico explica como usar o site de administração e monitoramento (também conhecido como o Help Desk) para obter uma senha de recuperação para fornecer aos usuários finais se a unidade protegida pelo BitLocker entrar no modo de recuperação. As unidades entram no modo de recuperação se os usuários perdem ou esquecem o PIN ou a senha ou se o chip TPM (Trusted Module Platform) detecta alterações nos arquivos do BIOS ou da inicialização de um computador.

Para obter uma senha de recuperação, use a área de **recuperação de unidade** do site de administração e monitoramento. Você deve receber a função usuários da assistência técnica MBAM ou a função usuários avançados da assistência técnica do MBAM para acessar esta área do site.

**Observação**  
Você pode ter atribuído a essas funções nomes diferentes quando você as criou. Para obter mais informações, consulte [planejando para contas e grupos do MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).



**Importante**  
As senhas de recuperação expiram após um único uso. Em unidades do sistema operacional e unidades de dados fixas, a regra de uso único é aplicada automaticamente. Em unidades removíveis, ele é aplicado quando a unidade é removida e, em seguida, reinserida e desbloqueada em um computador com configurações de política de grupo ativadas para gerenciar unidades removíveis.



**Para recuperar uma unidade no modo de recuperação**

1.  Abra um navegador da Web e navegue até o **site de administração e monitoramento**.

2.  No painel esquerdo, selecione **recuperação de unidade** para abrir a página **recuperar acesso a uma unidade criptografada** .

3.  Insira o domínio de logon do Windows do usuário final e o nome de usuário para exibir informações de recuperação.

    **Observação**  
    Se você estiver no grupo usuários da assistência avançada do MBAM, os campos domínio do usuário e ID do usuário não serão necessários.



4.  Insira os primeiros oito dígitos da ID da chave de recuperação para ver uma lista de possíveis chaves de recuperação correspondentes ou digite a ID da chave de recuperação inteira para obter a chave de recuperação exata.

5.  Na lista **motivo da desbloqueio de unidade** , selecione uma das opções predefinidas e, em seguida, clique em **Enviar**.

    MBAM retornará o seguinte:

    -   Uma mensagem de erro se nenhuma senha de recuperação correspondente for encontrada

    -   Várias correspondências possíveis se o usuário tiver várias senhas de recuperação correspondentes

    -   A senha de recuperação e o pacote de recuperação para o usuário enviado

        **Observação**  
        Se você estiver recuperando uma unidade danificada, a opção pacote de recuperação fornece o BitLocker com informações críticas necessárias para a recuperação da unidade.



~~~
After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

6. Para copiar a senha, clique em **copiar chave**e cole a senha de recuperação em uma mensagem de email. Ou, se preferir, clique em **salvar** para salvar a senha de recuperação em um arquivo.

   Quando o usuário digitar a senha de recuperação no sistema ou usar o pacote de recuperação, a unidade será desbloqueada.



## Tópicos relacionados


[Realizando o gerenciamento do BitLocker com o MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)



## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





