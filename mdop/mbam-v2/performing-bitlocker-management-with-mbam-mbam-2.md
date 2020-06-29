---
title: Realizar o Gerenciamento do BitLocker com o MBAM
description: Realizar o Gerenciamento do BitLocker com o MBAM
author: dansimp
ms.assetid: 9bfc6c67-f12c-4daa-8f08-5884fb47443c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d261ec4fa789cd331209afe1c2f1858d627209a3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799884"
---
# Realizar o Gerenciamento do BitLocker com o MBAM


Depois de planejar e implantar o Microsoft BitLocker Administration and Monitoring (MBAM), você pode configurá-lo e usá-lo para gerenciar a criptografia do BitLocker corporativo. As informações nesta seção descrevem tarefas de gerenciamento de criptografia do BitLocker do dia a pós-instalação que são realizadas usando a administração e o monitoramento do Microsoft BitLocker.

## Redefinir um bloqueio de TPM usando MBAM


Um TPM (Trusted Platform Module) é um microchip projetado para fornecer funções básicas relacionadas à segurança, principalmente envolvendo chaves de criptografia. O TPM geralmente é instalado na placa-mãe de um computador ou laptop e comunica-se com o restante do sistema usando um barramento de hardware. Os computadores que incorporam um TPM têm a capacidade de criar chaves criptográficas e criptografá-las para que possam ser descriptografadas apenas pelo TPM.

Um bloqueio de TPM pode ocorrer se um usuário inserir o PIN incorreto muitas vezes. O número de vezes que um usuário pode inserir um PIN incorreto antes que os bloqueios do TPM variem do fabricante para o fabricante. Você pode usar o MBAM para acessar o sistema de dados de recuperação de chave centralizada no site de administração e monitoramento, onde você pode recuperar um arquivo de senha de proprietário do TPM quando fornecer uma ID de computador e um identificador de usuário associado.

[Como redefinir um bloqueio de TPM](how-to-reset-a-tpm-lockout-mbam-2.md)

## Recuperar unidades com o MBAM


Quando você estiver lidando com a criptografia de dados, especialmente em um ambiente corporativo, considere como esses dados podem ser recuperados em caso de falha de hardware, mudanças na equipe ou outras situações nas quais as chaves de criptografia podem ser perdidas.

Os recursos de recuperação de unidade criptografada do MBAM garantem que os dados possam ser capturados e armazenados e que as ferramentas necessárias estejam disponíveis para acessar um volume protegido pelo BitLocker quando o BitLocker entra no modo de recuperação, é movido ou é corrompido.

[Como recuperar uma unidade no modo de recuperação](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

[Como recuperar uma unidade movida](how-to-recover-a-moved-drive-mbam-2.md)

[Como recuperar uma unidade corrompida](how-to-recover-a-corrupted-drive-mbam-2.md)

## Determinar o estado de criptografia do BitLocker dos computadores perdidos usando MBAM


Usando o MBAM, você pode determinar o último status de criptografia do BitLocker conhecido de computadores que foram perdidos ou roubados.

[Como determinar o estado de criptografia BitLocker de computadores perdidos](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

## Usar o portal de autoatendimento para recuperar o acesso a um computador


Se os usuários finais forem bloqueados pelo BitLocker, eles poderão usar as instruções desta seção para obter uma chave de recuperação do BitLocker e obter novamente o acesso ao computador.

[Como usar o Portal de Autoatendimento para recuperar o acesso a um computador](how-to-use-the-self-service-portal-to-regain-access-to-a-computer.md)

## Outros recursos para executar o gerenciamento do BitLocker com o MBAM


[Operações do MBAM 2.0](operations-for-mbam-20-mbam-2.md)

 

 





