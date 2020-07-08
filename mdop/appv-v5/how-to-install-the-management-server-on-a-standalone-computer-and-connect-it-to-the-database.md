---
title: Como instalar o servidor de gerenciamento em um computador autônomo e conectá-lo ao banco de dados
description: Como instalar o servidor de gerenciamento em um computador autônomo e conectá-lo ao banco de dados
author: dansimp
ms.assetid: 95281287-cb56-4117-befd-854268ea147c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 86f384e88b85101855287bb428e75376f7974219
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796397"
---
# Como instalar o servidor de gerenciamento em um computador autônomo e conectá-lo ao banco de dados


Use o procedimento a seguir para instalar o servidor de gerenciamento em um computador autônomo e conectá-lo ao banco de dados.

**Para instalar o servidor de gerenciamento em um computador autônomo e conectá-lo ao banco de dados**

1.  Copie os arquivos de instalação do App-V 5,0 Server para o computador no qual você deseja instalá-lo. Para iniciar a instalação do App-V 5,0 Server, clique com o botão direito do mouse e execute **appv\_server\_setup.exe** como administrador. Clique em **Instalar**.

2.  Na página de **introdução** , examine e aceite os termos de licença e clique em **Avançar**.

3.  Na página **usar o Microsoft Update para ajudar a manter seu computador seguro e atualizado** , para habilitar as atualizações da Microsoft, selecione **usar o Microsoft Update quando eu verificar se há atualizações (recomendado).** Para desabilitar o Microsoft Updates, selecione **não quero usar o Microsoft Update**. Clique em **Avançar**.

4.  Na página **seleção de recursos** , marque a caixa de seleção **servidor de gerenciamento** e clique em **Avançar**.

5.  Na página **local de instalação** , aceite o local padrão e clique em **Avançar**.

6.  Na página **configurar banco de dados de gerenciamento existente** , selecione **usar um SQL Server remoto**e digite o nome do computador que executa o Microsoft SQL SQL, por exemplo, **SqlServerMachine**.

    **Observação**  
    Se o Microsoft SQL Server estiver implantado no mesmo servidor, selecione **usar SQL Server local**.



~~~
For the SQL Server Instance, select **Use the default instance**. If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.

Specify the **SQL Server Database name** that this management server will use, for example **AppvManagement**.
~~~

7. Na página **configurar configuração do servidor de gerenciamento** , especifique o grupo de anúncios ou a conta que será conectada ao console de gerenciamento para fins administrativos, por exemplo, **MyDomain\\MyUser** ou **MyDomain\\AdminGroup**. A conta ou o grupo do AD especificado será habilitado para gerenciar o servidor por meio do console de gerenciamento. Você pode adicionar mais usuários ou grupos usando o console de gerenciamento após a instalação

   Especifique o **nome do site** que você deseja usar para o serviço de gerenciamento. Aceite o padrão se você não tiver um nome personalizado. Para a **Associação de portabilidade**, especifique um número de porta exclusivo a ser usado, por exemplo, **12345**.

8. Clique em **Instalar**.

9. Para confirmar se a configuração foi concluída com êxito, abra um navegador da Web e digite a seguinte URL: http://managementserver:portnumber/Console.html se a instalação tiver sido bem-sucedida, você verá o **console de gerenciamento do Silverlight** aparecerá sem mensagens de erro ou avisos sendo exibidos.

   **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Implantação do App-V 5.0](deploying-app-v-50.md)









