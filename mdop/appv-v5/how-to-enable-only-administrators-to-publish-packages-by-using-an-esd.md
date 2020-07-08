---
title: Como permitir que apenas administradores publiquem pacotes usando ESD
description: Como permitir que apenas administradores publiquem pacotes usando ESD
author: dansimp
ms.assetid: 03367b26-83d5-4299-ad52-b9177b9cf9a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 341e86ca806c5acc736c78cf8072aab6fb4286df
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796417"
---
# Como permitir que apenas administradores publiquem pacotes usando ESD


A partir do App-V 5,0 SP3, você pode configurar o cliente App-V para que somente administradores (não usuários finais) possam publicar ou cancelar a publicação de pacotes. Em versões anteriores do App-V, você não pode impedir que os usuários finais executem essas tarefas.

**Para habilitar apenas os administradores a publicar ou cancelar a publicação de pacotes**

1.  Navegue até o seguinte nó de objeto de política de Grupo:

    **Configuração &gt; do computador Política &gt; modelos administrativos &gt; do &gt; App-V &gt; Publishing**.

2.  Habilite a configuração de política **exigir publicação como administrador** .

    Para usar opcionalmente o PowerShell para definir esse item, consulte [como gerenciar pacotes do App-V 5,0 em execução em um computador autônomo usando o PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

 

 





