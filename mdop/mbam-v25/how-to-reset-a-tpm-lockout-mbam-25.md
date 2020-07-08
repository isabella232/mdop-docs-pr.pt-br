---
title: Como redefinir um bloqueio de TPM
description: Como redefinir um bloqueio de TPM
author: dansimp
ms.assetid: dd20a728-c52e-48e6-9f6c-1311c71dee74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5aea277e80c54fb01d1a6c00b62f0c617d1ad12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799249"
---
# Como redefinir um bloqueio de TPM


Este tópico explica como usar o site de administração e monitoramento (também chamado de suporte técnico) para redefinir um bloqueio do TPM. Os bloqueios do TPM podem ocorrer se um usuário final digitar o PIN incorreto muitas vezes. O número de vezes que um usuário pode inserir um PIN incorreto antes que os bloqueios do TPM variem do fabricante para o fabricante.

Na área **gerenciar TPM** do site de administração e monitoramento, você pode acessar o sistema de dados de recuperação de chave centralizada, que fornece um arquivo de senha de proprietário do TPM quando você fornecer uma ID de computador e um identificador de usuário associado.

Para acessar a área gerenciar TPM do site de administração e monitoramento, você deve receber a função usuários da assistência técnica MBAM ou a função usuários avançados da assistência técnica do MBAM. Essas funções são grupos que os administradores criam no Active Directory. Você pode usar qualquer nome para estes grupos. Para obter mais informações, consulte [planejando para contas e grupos do MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).

Para obter informações sobre a propriedade MBAM e TPM, consulte [considerações de segurança do MBAM 2,5](mbam-25-security-considerations.md#bkmk-tpm).

**Para redefinir um bloqueio de TPM**

1.  Abra um navegador da Web e navegue até o **site de administração e monitoramento**.

2.  No painel esquerdo, clique em **gerenciar TPM** para abrir a página **gerenciar TPM** .

3.  Digite o nome de domínio totalmente qualificado para o computador e o nome do computador.

4.  Insira o domínio de logon do Windows do usuário final e o nome de usuário para recuperar o arquivo de senha de proprietário do TPM.

    **Observação**  Se você estiver no grupo usuários da assistência avançada do MBAM, os campos domínio do usuário e ID do usuário não serão necessários.

     

5.  Na lista o motivo da solicitação **de arquivo de senha de proprietário do TPM** , selecione um motivo para a solicitação e clique em **Enviar**.

    MBAM retorna um dos seguintes:

    -   Uma mensagem de erro se não for encontrado um arquivo de senha de proprietário do TPM correspondente

    -   O arquivo de senha de proprietário do TPM para o computador enviado

    Depois que a senha de proprietário do TPM for recuperada, a senha de proprietário será exibida.

6.  Para salvar a senha em um arquivo. TPM, clique no botão **salvar** .

7.  Na área **gerenciar TPM** do site de **Administração e monitoramento**, selecione a opção **Redefinir bloqueio do TPM** e forneça o arquivo de senha de proprietário do TPM.

    O bloqueio do TPM é redefinido e o acesso do usuário final é restaurado.

    **Importante**  Não forneça o valor de hash TPM ou o arquivo de senha de proprietário do TPM aos usuários finais. Como as informações do TPM não são alteradas, a atribuição de um arquivo aos usuários finais cria um risco de segurança.

     



## Tópicos relacionados


[Realizando o gerenciamento do BitLocker com o MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 

## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





