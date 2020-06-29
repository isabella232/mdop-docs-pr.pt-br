---
title: Como alterar os níveis de relatório de log e redefinir arquivos de log
description: Como alterar os níveis de relatório de log e redefinir arquivos de log
author: dansimp
ms.assetid: 9561d6fb-b35c-491b-a355-000064583194
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7307dee0030d9c03a8107d9d0ceef2086a94df07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797247"
---
# Como alterar os níveis de relatório de log e redefinir arquivos de log


Você pode usar o procedimento a seguir para alterar o nível de relatório de log do nó **virtualização de aplicativos** no console de gerenciamento do Application Virtualization. Quando o arquivo de log atinge o tamanho máximo (o padrão é 256 MB), uma redefinição é forçada quando ocorre a próxima gravação do log. Uma redefinição faz com que um novo arquivo de log seja criado, e o arquivo antigo é renomeado como um backup.

**Para alterar o nível de relatório de log**

1.  Clique com o botão direito do mouse no nó do **Application Virtualization** e selecione **Propriedades** no menu pop-up.

2.  Na guia **geral** da caixa de diálogo **Propriedades** , na lista suspensa **nível de log** , selecione o nível de log desejado.

    **Observação**  Se você escolher **Verbose** como o nível de log, os arquivos de log aumentarão muito rapidamente. Isso pode inibir o desempenho do cliente, portanto a prática recomendada é usar esse nível de log somente para diagnosticar problemas específicos.

     

3.  Na guia **geral** da caixa de diálogo **Propriedades** , na lista suspensa **nível de log do sistema** , selecione o nível de log desejado.

    **Observação**  A configuração de **nível de log do sistema** controla o nível de mensagens enviadas ao log de eventos do sistema. As mensagens registradas são idênticas às mensagens que são registradas no log de eventos do cliente, mas são armazenadas em um local diferente.

     

4.  Clique em **OK** ou **aplicar** para alterar a configuração.

**Para redefinir o arquivo de log**

1.  Clique com o botão direito do mouse no nó do **Application Virtualization** e selecione **Propriedades** no menu pop-up.

2.  Na guia **geral** da caixa de diálogo **Propriedades** , clique em **Redefinir log** para fazer backup do arquivo de log atual e iniciar imediatamente um novo arquivo de log. Os arquivos de log de backup são armazenados na mesma pasta.

3.  Clique em **OK** ou **aplicar** para alterar a configuração.

## Tópicos relacionados


[Como configurar o Application Virtualization Client Management Console](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

[Permissões de acesso de usuário no Application Virtualization Client](user-access-permissions-in-application-virtualization-client.md)

 

 





