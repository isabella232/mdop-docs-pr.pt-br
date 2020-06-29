---
title: Página Sobre Aceleradores de Pacote
description: Página Sobre Aceleradores de Pacote
author: dansimp
ms.assetid: 9630cde0-e2c3-476f-8fa1-58b3c9f7d3f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 34fe55d910a7532f011b239ff5b8162aa9240f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797636"
---
# Página Sobre Aceleradores de Pacote


As informações a seguir fornecem informações de práticas recomendadas sobre como compartilhar aceleradores de pacote. Se você planeja compartilhar arquivos de aceleradores de pacote, informações como nomes de computador, informações da conta do usuário e informações sobre aplicativos incluídos nas transformações podem estar incluídas no arquivo aceleradores de pacote. Você deve examinar quaisquer configurações ou arquivos de configuração associados ao pacote de aplicativo virtual para garantir que os aplicativos não contenham informações pessoais. Esta página contém os elementos a seguir.

-   **Nome de usuário**. Ao fazer logon no computador executando o Microsoft App-V Sequencer, você deve usar uma conta de usuário genérica, como a conta de **administrador** interna. Você não deve usar uma conta com base em um nome de usuário existente.

-   **Nome do computador**. Especifique um nome geral, não identificado do computador que está executando o sequenciador.

-   **URL do servidor**. No console App-V Sequencer, na guia **implantação** , use as configurações padrão para as informações de configuração de URL do servidor.

-   **Aplicativos**. Se você não deseja compartilhar a lista de aplicativos que foram instalados no computador que executa o sequenciador quando você criou o acelerador de pacote, você deve excluir o arquivo **appv\_manifest.xml** . Esse arquivo está localizado no diretório raiz do pacote do pacote de aplicativo virtual.

## Tópicos relacionados


[Assistente para Criar Acelerador de Pacote (App-V 4.6 SP1)](create-package-accelerator-wizard--appv-46-sp1-.md)

[Sobre aceleradores de pacote do App-V (App-V 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md)

 

 





