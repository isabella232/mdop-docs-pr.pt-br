---
title: Administrando os Recursos do MBAM 2.0
description: Administrando os Recursos do MBAM 2.0
author: dansimp
ms.assetid: 065e0704-069e-4372-9b86-0b57dd7638dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 35bb855e185ad8e3fa6880853938074cf6185a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799286"
---
# Administrando os Recursos do MBAM 2.0


Depois de concluir o planejamento necessário e a implantação do Microsoft BitLocker Administration and Monitoring (MBAM), você pode configurá-lo e usá-lo para gerenciar a criptografia do BitLocker na empresa as informações nesta seção descrevem as tarefas de operações do recurso de administração e monitoramento do Microsoft BitLocker do dia-a-dia após a instalação.

## Gerenciar funções de administrador do MBAM


Após a conclusão da instalação do MBAM para todos os recursos do servidor, os usuários administrativos devem receber acesso a eles. Como prática recomendada, os administradores que gerenciam ou usam os recursos do MBAM Server devem ser atribuídos aos grupos de segurança dos serviços de domínio Active Directory e esses grupos devem ser adicionados ao grupo local administrativo MBAM apropriado.

[Como gerenciar funções de administrador do MBAM](how-to-manage-mbam-administrator-roles-mbam-2.md)

## Gerenciar isenções de criptografia do BitLocker


O MBAM permite que você conceda isenções de criptografia a usuários específicos que não precisam ou querem que suas unidades sejam criptografadas. A isenção de computador geralmente é usada quando uma empresa tem computadores que não precisam ser criptografados, como computadores usados em desenvolvimento ou testes ou computadores mais antigos que não dão suporte ao BitLocker. Em alguns casos, a lei local também pode exigir que determinados computadores não sejam criptografados.

[Como gerenciar isenções de criptografia BitLocker para usuários](how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md)

## Gerenciar as opções de criptografia do BitLocker do cliente MBAM usando o painel de controle


O MBAM fornece um painel de controle personalizado, chamado opções de criptografia do BitLocker, que aparecerá em **sistema e segurança**. O painel de controle do MBAM pode ser usado para desbloquear unidades fixas e removíveis criptografadas e também gerenciar seu PIN ou senha.

**Observação**  Este painel de controle personalizado não substitui o painel de controle padrão do Windows BitLocker.

 

[Como gerenciar opções de criptografia BitLocker do Cliente do MBAM utilizando o Painel de Controle](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-2.md)

## Outros recursos para administrar recursos do MBAM


[Operações do MBAM 2.0](operations-for-mbam-20-mbam-2.md)

 

 





