---
title: Como redefinir o cache do FileSystem
description: Como redefinir o cache do FileSystem
author: dansimp
ms.assetid: 7777259d-8c21-4c06-9384-9599b69f9828
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 680634d98f8aac048af605c62029a0ee6b20af03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796980"
---
# Como redefinir o cache do FileSystem


A redefinição do cache do sistema de arquivos não é algo que geralmente deve ser necessária. No entanto, se precisar redefinir completamente o cache do sistema de arquivos, talvez para fins de solução de problemas, você pode usar o procedimento a seguir. São necessários direitos administrativos para executar esta ação.

**Para redefinir o cache do sistema de arquivos**

1.  Defina o seguinte valor do registro como 0 (zero):

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State

2.  Reinicie o computador.

## Tópicos relacionados


[Como definir as configurações de Registro do cliente do App-V usando a linha de comando](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





