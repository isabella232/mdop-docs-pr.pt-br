---
title: Sobre o MBAM 2.0
description: Sobre o MBAM 2.0
author: dansimp
ms.assetid: b43a0ba9-1c83-4854-a2c5-14eea0070e36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7bdf24d1f375dd1fa8b18ac90c2fc49d2887c6c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799448"
---
# Sobre o MBAM 2.0


O Microsoft BitLockerAdministration e o Monitoring (MBAM) 2.0 fornecem uma interface administrativa simplificada para a criptografia de unidade de disco BitLocker. O BitLocker oferece proteção aprimorada contra roubo de dados ou exposição de dados para computadores perdidos ou roubados. O BitLocker criptografa todos os dados armazenados no volume do sistema operacional Windows e nos volumes de dados configurados.

## Sobre o MBAM 2.0


O BitLockerAdministration e o Monitoring 2.0 aplicam as opções de política de criptografia do BitLocker que você define para a sua empresa, monitora a conformidade dos computadores cliente com essas políticas e relatórios sobre o status de criptografia dos computadores corporativos e individuais. Além disso, o MBAM permite que você acesse as informações da chave de recuperação quando os usuários esquecem o PIN ou a senha, ou quando o registro da inicialização ou do BIOS é alterado.

**Observação**  O BitLocker não é abordado em detalhes neste guia. Para obter uma visão geral do BitLocker, consulte [visão geral da criptografia de unidade de disco BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=225013).

 

Os seguintes grupos podem estar interessados em usar o MBAM para gerenciar o BitLocker:

-   Administradores, profissionais de segurança de ti e responsáveis pela conformidade responsáveis por garantir que os dados confidenciais não sejam divulgados sem autorização

-   Administradores que são responsáveis por segurança de computador em escritórios remotos ou filiais

-   Administradores responsáveis pelos computadores cliente que executam o Windows

## <a href="" id="what-s-new-in-mbam-2-0"></a>Novidades do MBAM 2.0


O MBAM 2.0 oferece os novos recursos e funcionalidades a seguir.

### Integração do System Center Configuration Manager com o MBAM

O MBAM agora oferece suporte à integração com o System Center Configuration Manager. Essa integração move a infraestrutura de conformidade do MBAM para o ambiente nativo do Configuration Manager. Os administradores de ti que usam o Configuration Manager na empresa podem ver agora o status de conformidade da empresa no console de gerenciamento da Microsoft e analisar relatórios para exibir computadores individuais.

### A compatibilidade de hardware está disponível somente na topologia de integração do Configuration Manager

A integração do Configuration Manager com o MBAM permite que os recursos do Configuration Manager permitam ou proíbam o uso de certos tipos de hardware com o MBAM e oferece mais flexibilidade do que a compatibilidade de hardware que estava disponível no MBAM 1,0. Os administradores de ti podem criar suas próprias coleções para limitar o hardware e podem implantar a linha de base de configuração do MBAM para essas coleções. A compatibilidade de hardware do MBAM que estava presente no MBAM 1,0 agora está disponível apenas na topologia do MBAM Configuration Manager e administrada do Configuration Manager.

### Política de proteção flexível

Os computadores que já estão criptografados com um protetor (por exemplo, TPM + PIN ou desbloqueio automático e senha) e que recebem uma política MBAM que exige um subconjunto dessa criptografia (por exemplo, TPM ou desbloqueio automático) são considerados compatíveis. No exemplo acima, a opção PIN e senha não seriam removidas automaticamente, a menos que o administrador de ti defina especificamente esses recursos como não mais permitidos.

Os computadores que não estão criptografados e que recebem uma política de MBAM (por exemplo, TPM ou desbloqueio automático) são criptografados adequadamente. Os usuários que são administradores locais podem usar as ferramentas do BitLocker (item do painel de controle, criptografia de unidade de disco BitLocker ou Manage-bde) para adicionar ou modificar os protetores existentes (por exemplo, TPM + PIN ou desbloqueio automático e senha). Elas permanecem em conformidade, a menos que as políticas do MBAM a definam especificamente.

### Capacidade de atualizar o cliente MBAM

O Windows Installer do cliente MBAM 2.0 detecta a versão do cliente existente e executa as etapas necessárias para atualizar para o cliente do MBAM 2.0 a partir de versões anteriores.

### Capacidade de atualizar o servidor MBAM a partir de versões anteriores

Você pode atualizar a infraestrutura de servidor do MBAM 2.0 a partir de versões anteriores do MBAM da seguinte maneira:

**Substituição manual do servidor in-loco** – você deve desinstalar manualmente a infraestrutura do servidor do MBAM existente e instalar a infraestrutura de servidor do MBAM 2,0. Você não precisa remover os bancos de dados para fazer a atualização. Em vez disso, selecione os bancos de dados existentes, que a versão anterior do cliente MBAM criou. A instalação de atualização do MBAM 2.0 então migra os bancos de dados existentes para o MBAM 2,0.

**Atualização de cliente distribuído** – se você estiver usando a topologia MBAM autônoma, poderá atualizar os clientes do MBAM gradualmente após a instalação da infraestrutura de servidor MBAM do 2,0. O servidor MBAM 2,0 detecta a versão do cliente existente e executa as etapas necessárias para atualizar para o cliente 2,0.

Depois de atualizar a infraestrutura de servidor do MBAM 2,0, os clientes do MBAM 1,0 continuam a se comunicar com o servidor do MBAM 2,0 com êxito, dados de recuperação posteriores, mas a conformidade será baseada nas políticas do MBAM 1,0. Você deve atualizar os clientes para o MBAM 2,0 para que os computadores cliente relatem precisamente a conformidade com as políticas do MBAM 2,0. Você pode atualizar os clientes para o cliente do MBAM 2,0 sem desinstalar o cliente anterior e o cliente começará a aplicar e relatar as políticas do MBAM 2,0.

Se estiver usando o MBAM com o Configuration Manager, você deve atualizar os clientes do MBAM 1,0 para MBAM 2,0.

### <a href="" id="mbam-support-for-bitlocker-s-enterprise-scenarios-on-the-windows-8-platform"></a>Suporte MBAM para cenários corporativos do BitLocker na plataforma do Windows 8

O MBAM dá suporte ao sistema operacional Windows 8 como uma plataforma de destino para a instalação do cliente do MBAM. Esse suporte permite aos administradores de ti instalar o agente do MBAM, para criptografar as unidades do sistema operacional Windows 8 e para informar sobre a conformidade dos computadores. O MBAM aproveita os protetores de TPM e TPM + PIN para gerenciar o sistema operacional Windows 8 da mesma forma que faz com o sistema operacional Windows 7. O MBAM 2.0 também adiciona suporte para os clientes de criptografia do Windows to go.

### Adição do portal de autoatendimento

Agora, os usuários finais podem usar o portal de autoatendimento para recuperar as chaves de recuperação. O portal de autoatendimento pode ser implantado em um único servidor com os outros recursos do MBAM ou em um servidor separado que ofereça aos administradores de ti a flexibilidade de expor o portal de autoatendimento aos usuários, conforme necessário. Depois que o portal de autoatendimento autenticar usuários, os usuários precisarão inserir apenas os oito primeiros dígitos da ID da chave de recuperação para receber a chave de recuperação.

O MBAM também protege a chave permitindo que os usuários recuperem chaves somente para os computadores nos quais são usuários, o que reduz o risco de que outros usuários obtenham acesso não autorizado.

### Capacidade de retomar automaticamente a proteção BitLocker a partir de um estado suspenso

O MBAM não permite mais que os administradores de ti mantenham o BitLocker suspenso e desprotegido por períodos prolongados de tempo. Se um administrador de ti suspender o BitLocker, o MBAM o reativará automaticamente quando o computador for reinicializado, o que reduz o risco de que o computador possa ser atacado.

### Unidades de dados fixas podem ser configuradas para desbloquear automaticamente sem uma senha

Uma política de unidade de dados fixa (FDD) agora pode ser configurada para permitir o desbloqueio automático da unidade sem uma senha. Os usuários não são solicitados a fornecer uma senha antes de a FDD ser criptografada, e o FDD será protegido e desbloqueado automaticamente com a unidade do sistema operacional.

## <a href="" id="---------mbam-2-0-release-notes"></a> Notas de versão do MBAM 2.0


Para saber mais e saber mais sobre as últimas notícias que não estão incluídas na documentação, consulte as [notas de versão do MBAM 2,0](release-notes-for-mbam-20-mbam-2.md).

## Como obter o MBAM 2.0


Essa tecnologia é parte do Microsoft Desktop Optimization Pack (MDOP). Os clientes empresariais podem obter o MDOP com o Microsoft Software Assurance. Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte [como faço para obter o MDOP?](https://go.microsoft.com/fwlink/p/?LinkId=322049)

## Tópicos relacionados


[Introdução ao MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)

 

 





