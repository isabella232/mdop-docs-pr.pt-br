---
title: Como excluir todos os aplicativos virtuais usando a linha de comando
description: Como excluir todos os aplicativos virtuais usando a linha de comando
author: dansimp
ms.assetid: bfe13b5c-825a-4eb1-a979-6c4b8d8b2a9c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 55c809df31fa5c19f2f1a56c143d492b092156c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797145"
---
# Como excluir todos os aplicativos virtuais usando a linha de comando


Você pode usar o procedimento a seguir para excluir todos os aplicativos virtuais de um computador específico.

**Observação**  Quando todos os aplicativos são excluídos de um pacote, o cliente do Application Virtualization (App-V) também exclui o pacote.

 

**Para excluir todos os aplicativos**

-   Execute o comando a seguir para excluir todos os aplicativos da conta de usuário sob a qual o comando é executado. Se você executar o comando com a opção/GLOBAL opcional, usando uma conta com direitos administrativos, todos os aplicativos serão excluídos para todos os usuários.

    `SFTMIME DELETE OBJ:APP [/GLOBAL]`

    **Observação**  Quando todos os aplicativos são excluídos de um pacote, o cliente do Application Virtualization (App-V) também exclui o pacote.

     

## Tópicos relacionados


[Como adicionar um pacote usando a linha de comando](how-to-add-a-package-by-using-the-command-line.md)

[Como remover um pacote usando a linha de comando](how-to-remove-a-package-by-using-the-command-line.md)

 

 





