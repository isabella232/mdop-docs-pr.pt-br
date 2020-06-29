---
title: Como configurar permissões de usuário
description: Como configurar permissões de usuário
author: dansimp
ms.assetid: 54e69f46-b028-4ad1-9b80-f06ef5c8f559
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3c2581a9f9dddcbc63682d356c777a24222dd62f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797184"
---
# Como configurar permissões de usuário


Você pode habilitar e desabilitar algumas ações para usuários que não têm direitos administrativos editando os valores de chave na chave do registro **Permissions** (HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\permissions). Essa chave é projetada principalmente para ajudar a impedir que os usuários façam erros em vez de fornecer qualquer segurança especial, pois os usuários com direitos administrativos podem editar qualquer um desses valores de chave. Os procedimentos a seguir são exemplos de como alterar os valores de chave. Para obter mais informações sobre as chaves e os valores do cliente do Application Virtualization (App-V), consulte <https://go.microsoft.com/fwlink/?LinkId=121528> .

**Para alterar permissões de usuário**

1.  Para permitir que os usuários escolham executar o cliente no modo offline, defina o valor da chave a seguir como 1:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ToggleOfflineMode

2.  Para permitir que os usuários visualizem todos os aplicativos por meio da interface do usuário, defina o valor da chave a seguir como 1. Definir o valor como 0 (zero) permite que os usuários vejam apenas os aplicativos que estão disponíveis para eles.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ViewAllApplications

## Tópicos relacionados


[Como definir as configurações de Registro do cliente do App-V usando a linha de comando](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

[Permissões de acesso de usuário no Application Virtualization Client](user-access-permissions-in-application-virtualization-client.md)

 

 





