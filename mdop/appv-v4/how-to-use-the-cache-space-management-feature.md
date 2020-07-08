---
title: Como Usar o Recurso de Gerenciamento de Espaço do Cache
description: Como Usar o Recurso de Gerenciamento de Espaço do Cache
author: dansimp
ms.assetid: 60965660-c015-46a8-88ac-54cbc050fe33
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fcb9cc4bc076e1acf52fb1c03797384c45b82f7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796919"
---
# Como Usar o Recurso de Gerenciamento de Espaço do Cache


O recurso de gerenciamento de espaço de cache do sistema de arquivos usa um algoritmo menos usado recentemente (LRU) e é habilitado por padrão. Se o espaço necessário para um novo pacote ultrapassar o espaço livre disponível no cache, o cliente do Application Virtualization (App-V) usará esse recurso para determinar quais pacotes existentes podem ser excluídos do cache para liberar espaço para o novo pacote. O cliente exclui o pacote com a data mais recente acessada se for anterior ao valor especificado no valor do registro MinPkgAge. O uso do recurso de gerenciamento de espaço de cache do sistema de arquivos também pode ajudar a evitar problemas de espaço em cache baixo.

Mais de um pacote é excluído, se necessário. Os pacotes que estiverem bloqueados não serão excluídos.

**Observação**  Para garantir que o cache tem espaço suficiente alocado para todos os pacotes que podem ser implantados, use a configuração **usar o limite de espaço em disco livre** ao configurar o cliente para que o cache possa crescer conforme necessário. Ou, se preferir, determine com antecedência quanto espaço em disco será necessário para o cache do App-V e, no momento da instalação, defina o tamanho do cache de acordo.

 

O recurso de gerenciamento de espaço em cache é controlado pelo valor do registro UnloadLeastRecentlyUsed. Um valor 1 habilita o recurso, e o valor 0 (zero) o desabilita.

**Para habilitar ou desabilitar o recurso de gerenciamento de espaço do cache**

-   Defina o valor de registro a seguir como 1 para habilitar o algoritmo LRU. Defina-o como 0 (zero) para desabilitar o recurso.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\UnloadLeastRecentlyUsed

**Para controlar quais pacotes podem ser descartados**

-   Para determinar quando o pacote pode ser selecionado para descartar, defina o valor do registro a seguir para igual ao número mínimo de dias que você deseja que decorra desde o último pacote ter sido acessado. Os pacotes que foram usados mais recentemente não são descartados.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\MinPkgAge

    **Cuidado**  O valor máximo para esta chave do registro é 0x00011111. Valores maiores impedirão a operação correta do recurso de gerenciamento de espaço em cache.

     

## Tópicos relacionados


[Como definir as configurações de Registro do cliente do App-V usando a linha de comando](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





