---
title: Administrando os Recursos do MBAM 1.0
description: Administrando os Recursos do MBAM 1.0
author: dansimp
ms.assetid: dd9a9eff-f1ad-4af3-85d9-c19131a4ad22
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a99ac556227c0f113fb20f3aca32d21c204877b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797882"
---
# Administrando os Recursos do MBAM 1.0


Depois de concluir todo o planejamento e a implantação necessários do Microsoft BitLocker Administration and Monitoring (MBAM), você poderá configurar e usar o MBAM para gerenciar a criptografia do BitLocker corporativo. As informações nesta seção descrevem tarefas de operações do recurso pós-instalação do dia-a-dia após a instalação MBAM.

## Gerenciar funções de administrador do MBAM


Após a conclusão da instalação do MBAM para todos os recursos do servidor, os usuários administrativos devem ter acesso a esses recursos de servidor. Como prática recomendada, os administradores que gerenciam ou usam recursos do MBAM Server devem ser atribuídos aos grupos de segurança do Active Directory e esses grupos devem ser adicionados ao grupo local administrativo apropriado do MBAM.

[Como gerenciar funções de administrador do MBAM](how-to-manage-mbam-administrator-roles-mbam-1.md)

## Gerenciar a compatibilidade de hardware


O recurso de compatibilidade de hardware do MBAM pode ajudá-lo a garantir que somente o hardware do computador especificado como suporte para BitLocker será criptografado. Quando esse recurso estiver ativado, bit \ _admmontla criptografará apenas computadores marcados como compatíveis.

**Importante**  Quando esse recurso estiver desativado, todos os computadores nos quais a política MBAM é implantada serão criptografados.

 

O MBAM pode coletar informações sobre o fabricante e o modelo de computadores cliente se você implantar a política de grupo "permitir verificação de compatibilidade de hardware". Se você configurar essa política, o agente MBAM relata as informações do modelo e do modelo do computador ao servidor MBAM quando o cliente MBAM é implantado em um computador cliente.

[Como gerenciar a compatibilidade de hardware](how-to-manage-hardware-compatibility-mbam-1.md)

[Como gerenciar isenções de criptografia BitLocker para usuários](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)

## Gerenciar isenções de criptografia do BitLocker


MBAM pode conceder duas formas de isenção de criptografia BitLocker: isenção de computador e isenção de usuário. A isenção de computador geralmente é usada quando uma empresa tem computadores que não precisam ser criptografados, como computadores usados em desenvolvimento ou testes ou computadores mais antigos que não dão suporte ao BitLocker. Em alguns casos, a lei local também pode exigir que determinados computadores não sejam criptografados. Você também pode optar por não ter certeza de que os usuários que não precisam ou querem que suas unidades sejam criptografadas.

[Como gerenciar isenções de criptografia BitLocker para computadores](how-to-manage-computer-bitlocker-encryption-exemptions.md)

## Gerenciar as opções de criptografia do BitLocker do cliente MBAM usando o painel de controle


Se habilitado por meio de um GPO (objetos de política de grupo), um painel de controle do MBAM personalizado chamado opções de criptografia BitLocker estará disponível em **sistema e segurança**. Este painel de controle personalizado substitui o painel de controle padrão do Windows BitLocker. O painel de controle do MBAM permite desbloquear unidades criptografadas (fixas e removíveis) e também ajuda você a gerenciar seu PIN ou senha.

[Como gerenciar opções de criptografia BitLocker do Cliente do MBAM utilizando o Painel de Controle](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-1.md)

## Outros recursos para administrar recursos do MBAM


[Operações do MBAM 1.0](operations-for-mbam-10.md)

 

 





