---
title: Como adicionar ou atualizar pacotes usando o Console de Gerenciamento
description: Como adicionar ou atualizar pacotes usando o Console de Gerenciamento
author: dansimp
ms.assetid: 62417b63-06b2-437c-8584-523e1dea97c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4ac458a5e33b83e19d72fee39cf837aa6bd57bc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796511"
---
# Como adicionar ou atualizar pacotes usando o Console de Gerenciamento


Você pode o procedimento a seguir para adicionar ou atualizar um pacote para o console de gerenciamento do App-V 5,1. Para atualizar um pacote que já existe no console de gerenciamento, use as etapas a seguir e importe o pacote atualizado usando o mesmo **nome**do pacote.

**Para adicionar um pacote ao console de gerenciamento**

1.  Clique na guia **pacotes** no painel de navegação da exibição do console de gerenciamento.

    O console exibe a lista de pacotes que foram adicionados ao servidor juntamente com as informações de status sobre cada pacote. Quando um pacote é selecionado, informações detalhadas sobre o pacote são exibidas no painel **pacotes** .

    Clique na caixa de listagem suspensa **desagrupada** e especifique como os pacotes devem ser exibidos no console. Você também pode clicar no cabeçalho da coluna associada para classificar os pacotes.

2.  Para especificar o pacote que você deseja adicionar, clique em **Adicionar ou atualizar pacotes**.

3.  Digite o caminho completo para o pacote que você deseja adicionar. Use o formato de caminho UNC ou HTTP, por exemplo, **\\\\servername\\sharename\\foldername\\packagename.AppV** ou **http://server.1234/file.appv** , e clique em **Adicionar**.

    **Importante**  Você deve selecionar um pacote com a extensão de nome de arquivo **. AppV** .

     

4.  A página exibe a mensagem de status **adicionando &lt; PackageName &gt; **. Clique em **importar status** para verificar o status de um pacote importado.

    Clique em **OK** para adicionar o pacote e feche a página **Adicionar pacote** . Se houve um erro durante a importação, clique em **detalhes** na página **importação de pacote** para obter mais informações. O pacote recém-adicionado agora está disponível no painel **pacotes** .

5.  Clique em **fechar** para fechar a página **Adicionar ou atualizar pacotes** .

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Operações para o App-V 5.1](operations-for-app-v-51.md)

 

 





