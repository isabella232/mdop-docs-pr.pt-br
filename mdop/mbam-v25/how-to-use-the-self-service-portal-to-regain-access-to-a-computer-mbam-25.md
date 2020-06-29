---
title: Como usar o Portal de Autoatendimento para recuperar o acesso a um computador
description: Como usar o Portal de Autoatendimento para recuperar o acesso a um computador
author: dansimp
ms.assetid: 3c24b13a-d1b1-4763-8ac0-0b2db46267e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cde9c71a957a5270d69aa8388455895f1cb2432b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799925"
---
# Como usar o Portal de Autoatendimento para recuperar o acesso a um computador


O portal de autoatendimento é um site que os administradores de ti configuram como parte da implantação do Microsoft BitLocker Administration and Monitoring (MBAM) 2,5. O website permite que os usuários finais recuperem o acesso de modo independente em seus computadores se eles estiverem bloqueados do Windows. O portal de autoatendimento não requer assistência para a equipe de suporte técnico.

As instruções a seguir são escritas da perspectiva dos usuários finais, mas as informações podem ser úteis para que os administradores de ti compreendam.

**Importante**  Um usuário final deve ter conectado fisicamente ao computador (não remotamente) pelo menos uma vez com êxito para poder recuperar a chave usando o portal de autoatendimento. Caso contrário, eles devem usar o portal de helpdesk para a recuperação de chave.

 

Os usuários finais podem ter travamentos se:

-   Esquecer a senha ou o PIN

-   Alterar os arquivos do sistema operacional, o BIOS ou o Trusted Platform Module (TPM)

**Observação**  Se o administrador de ti configurou um tempo limite de estado de sessão do IIS, uma mensagem será exibida no portal de autoatendimento 60 segundos antes do tempo limite.

 

**Para usar o portal de autoatendimento para recuperar o acesso a um computador**

1.  No campo **KeyId de recuperação** , insira um mínimo de oito da ID de chave do bitlocker de 32 dígitos que é exibido na tela de recuperação do BitLocker do computador. Se os oito primeiros dígitos corresponderem a várias chaves, será exibida uma mensagem solicitando que você insira todos os dígitos do 32 da ID da chave de recuperação.

2.  No campo **motivo** , selecione um motivo para a sua solicitação para a chave de recuperação.

3.  Clique em **obter chave**. A chave de recuperação do BitLocker será exibida no campo **chave de recuperação do BitLocker** .

4.  Digite o código de 48 dígitos na tela de recuperação do BitLocker no computador para obter novamente o acesso ao computador.



## Tópicos relacionados


[Realizando o gerenciamento do BitLocker com o MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 
## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





