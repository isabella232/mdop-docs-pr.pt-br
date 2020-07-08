---
title: Como adicionar uma versão de pacote
description: Como adicionar uma versão de pacote
author: dansimp
ms.assetid: dbb829c1-e5cb-4a2f-bc17-9a9bb50c671c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a60252e8b43af61ad548df30a93d8fbc9bae0cb7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797918"
---
# Como adicionar uma versão de pacote


No console de gerenciamento do servidor do Application Virtualization, ao resequenciar um pacote, você pode usar o procedimento a seguir para adicionar a nova versão aos seus servidores para transmissão.

**Observação**  Quando você atualiza um pacote com uma nova versão, pode deixar a versão existente no lugar ou excluí-la e deixar apenas a mais recente. Talvez você queira deixar a versão antiga em vigor para a compatibilidade com documentos herdados ou para poder testar a nova versão antes de disponibilizá-la para todos os usuários.

 

**Para adicionar uma versão de pacote**

1.  Copie o novo arquivo SFT para a pasta de conteúdo do servidor do aplicativo. Se o resequenciamento não adicionar alterações aos arquivos Open Software Descriptor (OSD), Icon (ICO) ou Sequencer Project (SPRJ), você não precisará copiá-los. Você pode incluir esses arquivos se desejar que todos os arquivos exibam a mesma data.

2.  No painel esquerdo do console de gerenciamento do servidor do Application Virtualization, expanda o nó **pacotes** .

3.  Clique com o botão direito do mouse no pacote que você deseja atualizar e escolha **Adicionar versão**.

4.  Na caixa de diálogo **Adicionar versão do pacote** , procure ou digite o nome do caminho para o novo arquivo do aplicativo no campo **caminho completo do arquivo de pacote** . Deve ser um arquivo SFT.

5.  Clique em **Avançar**.

6.  A caixa de diálogo **Resumo** mostra o local do arquivo e solicita que você copie o arquivo, caso ainda não tenha feito isso. Clique em **concluir** depois de verificar as informações.

    A nova versão agora está completa e pronta para transmitir.

## Tópicos relacionados


[Como excluir um pacote](how-to-delete-a-packageserver.md)

[Como gerenciar pacotes no Server Management Console](how-to-manage-packages-in-the-server-management-console.md)

 

 





