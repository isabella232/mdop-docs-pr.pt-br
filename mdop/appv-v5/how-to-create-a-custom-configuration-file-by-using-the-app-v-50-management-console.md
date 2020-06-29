---
title: Como criar um arquivo de configuração personalizada usando o Console de Gerenciamento do App-V 5.0
description: Como criar um arquivo de configuração personalizada usando o Console de Gerenciamento do App-V 5.0
author: dansimp
ms.assetid: 0d1f6768-be30-4682-8eeb-aa95918b24c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d54e68caa380025b2ff6f3ea79d30f275b589b30
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796472"
---
# Como criar um arquivo de configuração personalizada usando o Console de Gerenciamento do App-V 5.0


Você pode usar uma configuração dinâmica para personalizar um pacote App-V 5,0 para um usuário específico. No entanto, você deve primeiro criar o arquivo de configuração dinâmica do usuário (. xml) ou o arquivo de configuração de implantação dinâmica antes de poder usar os arquivos. A criação do arquivo é uma operação manual avançada. Para obter informações gerais sobre arquivos de configuração de usuários dinâmicos, consulte [sobre a configuração dinâmica do App-V 5,0](about-app-v-50-dynamic-configuration.md).

Use o procedimento a seguir para criar um arquivo de configuração de usuário dinâmico usando o console de gerenciamento do App-V 5,0.

**Para criar um arquivo de configuração de usuário dinâmico**

1.  Clique com o botão direito do mouse no nome do pacote que você deseja exibir e selecione **Editar acesso ao Active Directory** para exibir a configuração atribuída a um determinado grupo de usuários. Ou, se preferir, selecione o pacote e clique em **Editar**.

2.  Usando a lista de **entidades do anúncio com o Access**, selecione o grupo do anúncio que você deseja personalizar. Selecione **personalizado** na lista suspensa, se ainda não estiver selecionado. Um link chamado **Editar** será exibido.

3.  Clique em **Editar**. A configuração do usuário dinâmico atribuído ao grupo do anúncio será exibida.

4.  Clique em **avançado**e, em seguida, clique em **Exportar configuração**. Digite um nome de arquivo e clique em **salvar**. Agora, você pode editar o arquivo para configurar um pacote para um usuário.

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Operações para o App-V 5.0](operations-for-app-v-50.md)

 

 





