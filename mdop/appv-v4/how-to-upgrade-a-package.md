---
title: Como fazer upgrade de um pacote
description: Como fazer upgrade de um pacote
author: dansimp
ms.assetid: 831c7556-6f6c-4b3a-aefb-26889094dc1a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a9b3eca2c996337d79e551784818a421f495316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796938"
---
# Como fazer upgrade de um pacote


O processo para uma atualização automática é o mesmo para adicionar uma versão do pacote no console de gerenciamento do servidor do Application Virtualization. Uma atualização automática é realizada quando você resequencia o aplicativo em um pacote existente. Em seguida, você pode adicionar essa nova versão aos seus servidores para transmissão.

Quando você atualiza um pacote com uma nova versão, pode deixar a versão existente no lugar ou excluí-la e deixar apenas a mais recente. Talvez você queira deixar a versão antiga em vigor para a compatibilidade com documentos herdados ou para poder testar a nova versão antes de disponibilizá-la para todos os usuários.

**Para atualizar um pacote automaticamente**

1.  Copie o novo arquivo SFT para a pasta de conteúdo do servidor do Application Virtualization.

    **Observação**  Se a resequenciagem não adicionou recursos que alteraram os arquivos Open Software Descriptor (OSD), Icon (ICO) ou Sequencer Project (SPRJ), você não precisará copiá-los. Você pode incluir esses arquivos se desejar que todos esses arquivos exibam a mesma data.

     

2.  No painel esquerdo do console de gerenciamento do servidor do Application Virtualization, expanda **pacotes**.

3.  Clique com o botão direito do mouse no pacote que você deseja atualizar e selecione **Adicionar versão**.

4.  Na caixa de diálogo **Adicionar versão do pacote** , procure ou digite o nome do caminho completo da nova versão do aplicativo no **caminho completo do campo arquivo** . Deve ser um arquivo SFT.

5.  Clique em **Avançar**.

6.  A caixa de diálogo **Resumo** mostra o local do arquivo e solicita que você copie o arquivo, caso ainda não tenha feito isso. Clique em **concluir** depois de verificar as informações.

    A nova versão agora está completa e pronta para transmitir.

## Tópicos relacionados


[Como gerenciar pacotes no Server Management Console](how-to-manage-packages-in-the-server-management-console.md)

 

 





