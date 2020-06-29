---
title: Como alterar o tamanho do cache do FileSystem
description: Como alterar o tamanho do cache do FileSystem
author: dansimp
ms.assetid: 6ed17ba3-293b-4482-b3fa-31e5f606dad6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63c98d53ccb31e8eb64bc70d3d79b2198c506e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797238"
---
# Como alterar o tamanho do cache do FileSystem


Você pode alterar o tamanho do cache do sistema de arquivos usando a linha de comando. Essa ação requer uma redefinição completa do cache e requer direitos administrativos.

**Para alterar o tamanho do cache do sistema de arquivos**

1.  Defina o seguinte valor do registro como 0 (zero):

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State

2.  Defina o valor do registro a seguir para o tamanho máximo do cache, em MB, que é necessário para manter os pacotes — por exemplo, 8192 MB:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\FileSize

3.  Reinicie o computador.

## Tópicos relacionados


[Como definir as configurações de Registro do cliente do App-V usando a linha de comando](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





