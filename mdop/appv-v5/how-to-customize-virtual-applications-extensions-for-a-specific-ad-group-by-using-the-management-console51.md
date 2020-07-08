---
title: Como personalizar extensões de aplicativos virtuais para um grupo do AD específico usando o Console de Gerenciamento
description: Como personalizar extensões de aplicativos virtuais para um grupo do AD específico usando o Console de Gerenciamento
author: dansimp
ms.assetid: dd71df05-512f-4eb4-a55f-e5b93601323d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bf086da3fbb6938a4fc602af5ab63adb1621532
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796454"
---
# Como personalizar extensões de aplicativos virtuais para um grupo do AD específico usando o Console de Gerenciamento


Use o procedimento a seguir para personalizar as extensões de aplicativo virtual para um grupo do Active Directory (AD).

**Para personalizar extensões de aplicativos virtuais para um grupo de anúncios**

1.  Para exibir o pacote que você deseja configurar, abra o console de gerenciamento do App-V 5,1. Para exibir a configuração atribuída a um determinado grupo de usuários, selecione o pacote e clique com o botão direito do mouse no nome do pacote e selecione **Editar acesso ao Active Directory**. Ou, se preferir, selecione o pacote e clique em **Editar** no painel **acesso ao anúncio** .

2.  Para personalizar um grupo do AD, você pode encontrar o grupo na lista de **entidades do anúncio com o Access**. Em seguida, usando a caixa suspensa no painel de **configuração atribuído** , selecione **personalizado**e clique em **Editar**.

3.  Para desabilitar todas as extensões para um determinado aplicativo, desmarque **habilitar**.

    Para adicionar um novo atalho para o aplicativo selecionado, clique com o botão direito do mouse no aplicativo no painel **atalhos** e selecione **Adicionar novo atalho**. Para remover um atalho, clique com o botão direito do mouse no aplicativo no painel **atalhos** e selecione **remover atalho**. Para editar um atalho existente, clique com o botão direito do mouse no aplicativo e selecione **Editar atalho**.

4.  Para exibir outras extensões de aplicativo, clique em **avançado**e em **Exportar configuração**. Digite um nome de arquivo e clique em **salvar**. Você pode exibir todas as extensões de aplicativo associadas ao pacote usando o arquivo de configuração.

5.  Para editar extensões de aplicativo adicionais, modifique o arquivo de configuração e clique em **importar e substitua essa configuração**. Selecione o arquivo modificado e clique em **abrir**. Na caixa de diálogo, clique em **substituir** para concluir o processo.

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Operações para o App-V 5.1](operations-for-app-v-51.md)

 

 





