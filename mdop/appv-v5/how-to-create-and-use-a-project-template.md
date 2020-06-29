---
title: Como criar e usar um modelo de projeto
description: Como criar e usar um modelo de projeto
author: dansimp
ms.assetid: 2063f0b3-47a1-4090-bf99-0f26b107331c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e7640b9dc1e7baec194315400ee5672dfa83f394
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796455"
---
# Como criar e usar um modelo de projeto


Você pode usar um modelo de projeto App-V 5,0 para salvar as configurações comumente aplicadas associadas a um pacote de aplicativo virtual existente. Essas configurações podem ser aplicadas quando você cria novos pacotes de aplicativos virtuais em seu ambiente. Usar um modelo de projeto pode simplificar o processo de criação de pacotes de aplicativos virtuais.

**Observação**  Você pode, em geral, aplicar um modelo de projeto App-V 5,0 durante uma atualização de pacote. Por exemplo, se você tiver sequenciado um aplicativo com uma lista de exclusão personalizada, é recomendável que um modelo associado seja criado e salvo para uso posterior durante a atualização do aplicativo sequenciado.

Os modelos de projeto do App-V 5,0 diferem dos aceleradores de aplicativos do App-V 5,0 porque o App-V 5,0 Application Accelerators são específicos do aplicativo e os modelos de projeto do App-V 5,0 podem ser aplicados a vários aplicativos.

Use os procedimentos a seguir para criar e aplicar um novo modelo.

**Para criar um modelo de projeto**

1.  Para iniciar o sequenciador do App-V 5,0, no computador que está executando o sequenciador, clique em **Iniciar**  /  **todos os programas**Microsoft  /  **Application**Virtualization  /  **Sequencer Virtualization**.

**Observação**  Se o pacote de aplicativo virtual estiver aberto no console do App-V 5,0 Sequencer, pule para a etapa 3 deste procedimento.

2. Para abrir o pacote de aplicativo virtual existente que contém as configurações que você deseja salvar com o modelo de projeto App-V 5,0, clique em **arquivo**  /  **abrir**e, em seguida, clique em **Editar pacote**. Na página **selecionar pacote** , clique em **procurar** e localize o pacote de aplicativo virtual que você deseja abrir. Clique em **Editar**.

3. No console do sequenciador do App-V 5,0, para salvar o arquivo de modelo, clique em **arquivo**  /  **salvar como modelo**. Depois de revisar as configurações que serão salvas com o novo modelo, clique em **OK**. Especifique um nome que será associado ao novo modelo de projeto do App-V 5,0. Clique em salvar.
   O novo modelo de projeto do App-V 5,0 é salvo no diretório especificado na etapa 3 deste procedimento.

**Para aplicar um modelo de projeto**

**Importante**  Não há suporte para a criação de um pacote de aplicativo virtual usando um modelo de projeto em conjunto com um acelerador de pacote.

1.  Para iniciar o sequenciador do App-V 5,0, no computador que está executando o sequenciador, clique em **Iniciar**  /  **todos os programas**Microsoft  /  **Application**Virtualization  /  **Sequencer Virtualization**.

2.  Para criar ou atualizar um novo pacote de aplicativo virtual usando um modelo de projeto App-V 5,0, clique em **arquivo**  /  **novo do modelo**.

3.  Para selecionar o modelo de projeto que você deseja usar, navegue até o diretório onde o modelo de projeto foi salvo, selecione o modelo de projeto e clique em **abrir**.

    Crie o novo pacote de aplicativo virtual. As configurações salvas com o modelo especificado serão aplicadas ao novo pacote de aplicativo virtual que você está criando.

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Operações para o App-V 5.0](operations-for-app-v-50.md)









