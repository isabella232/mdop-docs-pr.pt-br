---
title: Sobre o chip de TPM do computador
description: Sobre o chip de TPM do computador
author: dansimp
ms.assetid: 6f1cf18c-277a-4932-886d-14202ca8d175
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f6df54dc8085c398bacc508fdbbb79a30b0e4204
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799291"
---
# Sobre o chip de TPM do computador


O BitLocker fornece proteção adicional quando é usado com um chip TPM (Trusted Platform Module). O chip TPM é um componente de hardware que é instalado em muitos computadores mais novos pelos fabricantes de computador. O Microsoft BitLocker Administration and Monitoring (MBAM) usa o BitLocker, além do chip TPM, para ajudar a fornecer proteção adicional dos seus dados e garantir que seu computador não tenha sido adulterado.

## Como configurar seu TPM


Quando você inicia o assistente de criptografia de unidade de disco BitLocker em seu computador, o BitLocker verifica se a sua organização configurou o BitLocker para usar um chip TPM. Se o BitLocker encontrar um chip TPM compatível, você pode ser solicitado a reiniciar o computador para habilitar o chip TPM para uso. Assim que o computador for reiniciado, siga as instruções para configurar o chip TPM no BIOS (o BIOS é uma camada anterior ao Windows do seu software de computador).

Após a configuração do BitLocker, você pode acessar informações adicionais sobre o chip do TPM abrindo a ferramenta opções de criptografia BitLocker no painel de controle do Windows e, em seguida, selecionando **Administração do TPM**.

**Observação**  Você deve ter credenciais administrativas no seu computador para acessar essa ferramenta.

 

Em uma falha de TPM, uma alteração no BIOS ou determinadas atualizações do Windows, o BitLocker bloqueará seu computador e exigirá que você entre em contato com o suporte técnico para desbloqueá-lo. Você precisa fornecer o nome do seu computador, bem como o domínio do computador. O suporte técnico pode fornecer um arquivo de senha que pode ser usado para desbloquear seu computador.

## Solução de problemas de TPM


Se ocorrer uma falha no TPM, alterar o BIOS ou algumas atualizações do Windows ocorrerem, o BitLocker bloqueará seu computador e exigirá que você entre em contato com o suporte técnico para desbloqueá-lo. Você precisa fornecer o nome do seu computador, bem como o domínio do computador. O suporte técnico pode fornecer um arquivo de senha que você pode usar para desbloquear seu computador.

## Tópicos relacionados


[Ajudando os usuários finais a gerenciar o BitLocker](helping-end-users-manage-bitlocker.md)

[Como usar seu PIN ou sua senha](using-your-pin-or-password.md)

 

 





