---
title: Realizar o Gerenciamento do BitLocker com o MBAM
description: Realizar o Gerenciamento do BitLocker com o MBAM
author: dansimp
ms.assetid: 2d24390a-87bf-48b3-96a9-3882d6f2a15c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d0de3711d5b7c3696783a054ee7c7f8220b5356
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799763"
---
# Realizar o Gerenciamento do BitLocker com o MBAM


Depois de implantar o Microsoft BitLocker Administration and Monitoring (MBAM), você pode configurar e usar o MBAM para gerenciar a criptografia do BitLocker corporativo. Esta seção descreve as tarefas de gerenciamento de criptografia do BitLocker do dia a dia após a instalação que podem ser realizadas usando o MBAM.

## Redefinir um bloqueio de TPM com MBAM


Um microchip do Trusted Platform Module (TPM) fornece funções básicas relacionadas à segurança. Essas funções são executadas principalmente pelo uso de chaves de criptografia. O TPM geralmente é instalado na placa-mãe de um computador ou laptop e se comunica com o restante do sistema usando um barramento de hardware. Os computadores que incorporam um TPM podem criar chaves criptográficas que podem ser descriptografadas apenas pelo TPM. Um bloqueio de TPM pode ocorrer se um usuário inserir um PIN incorreto muitas vezes. O número de vezes que um usuário pode inserir um PIN incorreto antes que os bloqueios do TPM variem do fabricante para o fabricante. O sistema de dados de recuperação de chave no site de administração do MBAM permite que você obtenha um arquivo Redefinir senha de proprietário do TPM.

[Como redefinir um bloqueio de TPM](how-to-reset-a-tpm-lockout-mbam-1.md)

## Recuperar unidades com o MBAM


Verifique se você sabe como tentar a recuperação de dados de unidades criptografadas em caso de falha de hardware, alterações de pessoal ou outras situações em que as chaves de criptografia são perdidas. Os recursos de recuperação de unidade criptografada do MBAM fornecem a captura e o armazenamento de dados e a disponibilidade de ferramentas necessárias para acessar um volume protegido pelo BitLocker quando o volume entra no modo de recuperação, é movido ou é corrompido.

[Como recuperar uma unidade no modo de recuperação](how-to-recover-a-drive-in-recovery-mode-mbam-1.md)

[Como recuperar uma unidade movida](how-to-recover-a-moved-drive-mbam-1.md)

[Como recuperar uma unidade corrompida](how-to-recover-a-corrupted-drive-mbam-1.md)

## Determinar o estado de criptografia do BitLocker dos computadores perdidos usando MBAM


Ao usar o MBAM, você pode determinar o último status de criptografia do BitLocker conhecido de computadores que foram perdidos ou roubados.

[Como determinar o estado de criptografia BitLocker de computadores perdidos](how-to-determine-the-bitlocker-encryption-state-of-a-lost-computers-mbam-1.md)

## Outros recursos para executar o gerenciamento do BitLocker com o MBAM


[Operações do MBAM 1.0](operations-for-mbam-10.md)

 

 





