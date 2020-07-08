---
title: Como permitir que apenas administradores publiquem pacotes usando ESD
description: Como permitir que apenas administradores publiquem pacotes usando ESD
author: dansimp
ms.assetid: bbc9fda2-fc09-4d72-8d9a-e83d2fcfe234
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22de7f62f540ceff274862c3f16b1f89d9459093
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796413"
---
# Como permitir que apenas administradores publiquem pacotes usando ESD


A partir do App-V 5,0 SP3, você pode configurar o cliente App-V para que somente administradores (não usuários finais) possam publicar ou cancelar a publicação de pacotes. Em versões anteriores do App-V, você não pode impedir que os usuários finais executem essas tarefas.

**Para habilitar apenas os administradores a publicar ou cancelar a publicação de pacotes**

1.  Navegue até o seguinte nó de objeto de política de Grupo:

    **Configuração &gt; do computador Política &gt; modelos administrativos &gt; do &gt; App-V &gt; Publishing**.

2.  Habilite a configuração de política **exigir publicação como administrador** .

    Para usar opcionalmente o PowerShell para definir esse item, consulte [como gerenciar pacotes do App-V 5,1 em execução em um computador autônomo usando o PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

 

 





