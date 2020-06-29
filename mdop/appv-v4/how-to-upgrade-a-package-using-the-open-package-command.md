---
title: Como fazer upgrade de um pacote usando o comando Abrir Pacote
description: Como fazer upgrade de um pacote usando o comando Abrir Pacote
author: dansimp
ms.assetid: 67c10440-de8a-4547-a34b-f83206d0cc3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cca438fe90373e8f934d1d790246544cdf46fa18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796941"
---
# Como fazer upgrade de um pacote usando o comando Abrir Pacote


Use o comando abrir pacote para atualizar ou aplicar uma atualização a um pacote de aplicativo sequenciado. Quando você atualiza um pacote de aplicativo virtual existente usando a linha de comando, a versão original do arquivo. sft é excluída. Você deve fazer backup do arquivo. sft associado antes de atualizar o pacote usando a linha de comando.

**Para atualizar um pacote usando o comando abrir pacote**

1.  Para abrir o pacote que será atualizado, no console do Application Virtualization (App-V) **, clique em** **Abrir pacote para atualização**. Na caixa de diálogo **abrir** , selecione o pacote que será atualizado.

2.  Para iniciar o assistente de **sequenciamento** , selecione **ferramentas**, **Assistente de sequenciamento**. Concluir o assistente que aplica as alterações de configuração, para salvar o novo aplicativo sequenciado, selecione **arquivo**, **salvar**.

3.  Para acrescentar o número da versão ao nome do pacote, no console do sequenciador, selecione **ferramentas**, **Opções**. Selecione **acrescentar versão do pacote ao nome do arquivo**. Clique em **OK**.

    **Importante**  Atualizar o nome do arquivo com a versão do pacote é essencial para concluir a atualização com êxito.

     

## Tópicos relacionados


[Como gerenciar aplicativos virtuais usando a linha de comando](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





