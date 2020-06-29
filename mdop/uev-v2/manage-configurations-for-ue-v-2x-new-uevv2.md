---
title: Gerenciar as configurações da UE-V 2.x
description: Gerenciar as configurações da UE-V 2.x
author: dansimp
ms.assetid: e2332eca-a9cd-4446-8f7c-d17058b03466
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 20d5d2942dbd805a4054a9431b237c821cbb70fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800061"
---
# Gerenciar as configurações da UE-V 2.x


No curso do ciclo de vida do Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 ou 2,1 SP1, você precisa gerenciar a configuração do UE-V Agent e também gerenciar locais de armazenamento para recursos como arquivos de pacote de configurações. Talvez seja necessário executar outras tarefas, por exemplo, configurar o centro de configurações da empresa para definir como os usuários interagem com a UE-V. Os tópicos a seguir fornecem orientação para o gerenciamento desses recursos de UE-V.

## Configurando o UE-V 2. x usando objetos de política de grupo


Você pode usar objetos de política de grupo para modificar as configurações que definem como o UE-V sincroniza as configurações em computadores.

[Configurando o UE-V 2. x com objetos de política de grupo](configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)

## Configurando o UE-V 2. x com o System Center Configuration Manager 2012


Você pode usar o SystemCenter2012 ConfigurationManager para gerenciar o UE-V Agent usando o pacote de configuração do UE-V 2.

[Configurando o UE-V 2. x com o System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md)

## Administração do UE-V 2. x com o PowerShell e o WMI


O UE-V fornece cmdlets do Windows PowerShell, que podem ajudar os administradores a executar várias tarefas de UE-V.

[Administração do UE-V 2. x com o Windows PowerShell e o WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

## Configurando o centro de configurações de empresa para UE-V 2. x


Você pode configurar o centro de configurações da empresa que é instalado usando o UE-V Agent para definir como os usuários interagem com a UE-V.

[Configurando o centro de configurações de empresa para UE-V 2. x](configuring-the-company-settings-center-for-ue-v-2x-both-uevv2.md)

## Exemplos de definições de configuração para UE-V 2. x


Veja a seguir alguns exemplos de definições de configuração de UE-V:

-   **Caminho de armazenamento de configurações:** Especifica o local do compartilhamento de arquivos que armazena as configurações de UE-V.

-   **Caminho do catálogo de modelos de configurações:** Especifica o caminho da Convenção Universal de nomenclatura (UNC) que define o local que foi verificado em busca de novos modelos de local de configurações.

-   **Registre os modelos da Microsoft:** Especifica se os modelos padrão da Microsoft devem ser registrados durante a instalação.

-   **Método de sincronização:** Especifica se UE-V usa o provedor de sincronização ou "nenhum". O "SyncProvider" dá suporte a computadores desconectados da rede. "Nenhum" aplica-se quando o computador está sempre conectado à rede. Para obter mais informações sobre o método Sync, consulte [métodos de sincronização para UE-V 2. x](sync-methods-for-ue-v-2x-both-uevv2.md).

-   **Tempo limite de sincronização:** Especifica o número de milissegundos que o computador aguarda antes do tempo limite quando ele recupera as configurações de usuário do local de armazenamento de configurações.

-   **Habilitar Sincronização:** Especifica se a sincronização das configurações do UE-V está habilitada ou desabilitada.

-   **Tamanho máximo do pacote:** Especifica um tamanho de limite de arquivo de pacote de configurações em bytes em que o UE-V Agent informa um aviso.

-   **Não sincronizar as configurações do aplicativo Windows:** Especifica que o UE-V não deve sincronizar aplicativos do Windows.

-   **Habilitar/desabilitar a notificação de primeira utilização:** Especifica se o UE-V exibirá uma caixa de diálogo na primeira vez que o UE-V Agent for executado no computador de um usuário.

-   **Ícone habilitar/desabilitar bandeja:** Especifica se a UE-V exibirá um ícone na área de notificação e todas as notificações associadas a ele. O ícone fornece um link para o centro de configurações da empresa.

-   **Hiperlink de contato personalizado:** Define o caminho, o texto e a descrição para o hiperlink **entrar em contato** no centro de configurações da empresa.






## Tópicos relacionados


[Administração do UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

[Implantar os recursos necessários na UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md)

[Implantar o UE-V 2. x para aplicativos personalizados](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

 

 





