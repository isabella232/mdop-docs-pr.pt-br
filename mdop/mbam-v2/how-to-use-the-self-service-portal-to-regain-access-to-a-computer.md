---
title: Como usar o Portal de Autoatendimento para recuperar o acesso a um computador
description: Como usar o Portal de Autoatendimento para recuperar o acesso a um computador
author: dansimp
ms.assetid: bcf095de-0237-4bb0-b450-da8fb6d6f3d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4abcffcf35e09bd5e24f4715a38dca74518ba29e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799800"
---
# Como usar o Portal de Autoatendimento para recuperar o acesso a um computador


Se os usuários finais se tornarem desbloqueados pelo BitLocker porque esquecim a senha ou o PIN, ou porque mudaram arquivos do sistema operacional ou alteraram o BIOS ou o TPM (Trusted Platform Module), eles podem usar o portal de autoatendimento para obter acesso ao Windows sem precisar solicitar assistência técnica para obter ajuda.

**Observação**  Se o administrador de ti configurou um tempo limite de estado de sessão IIS, uma mensagem será exibida 60 segundos antes do tempo limite.

 

**Observação**  Essas instruções são escritas para e da perspectiva de usuários finais.

 

**Para usar o portal de autoatendimento para recuperar o acesso a um computador**

1.  No campo **KeyId de recuperação** , insira um mínimo de oito da ID de chave do bitlocker de 32 dígitos que é exibido na tela de recuperação do BitLocker do computador.

    **Observação**  Se os oito primeiros dígitos corresponderem a várias chaves, será exibida uma mensagem solicitando que você insira todos os dígitos do 32 da ID da chave de recuperação.

     

2.  No campo **motivo** , selecione um motivo para a sua solicitação para a chave de recuperação.

3.  Clique em **obter chave**. A chave de recuperação do BitLocker será exibida no campo "a chave de recuperação do BitLocker".

4.  Digite o código de 48 dígitos na tela de recuperação do BitLocker no computador para obter novamente o acesso ao computador.

## Tópicos relacionados


[Realizar o Gerenciamento do BitLocker com o MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





