---
title: Como configurar o cliente para receber atualizações de pacotes e grupos de conexão do servidor de publicação
description: Como configurar o cliente para receber atualizações de pacotes e grupos de conexão do servidor de publicação
author: dansimp
ms.assetid: f5dfd96d-4b63-468c-8d93-9dfdf47c28fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e9df1f8b324430449d8d1dd3624d9f1157968a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796487"
---
# Como configurar o cliente para receber atualizações de pacotes e grupos de conexão do servidor de publicação


Implantar pacotes e grupos de conexão usando o servidor de publicação App-V 5,0 é útil porque oferece gerenciamento de ponto único e alta escalabilidade.

Use as etapas a seguir para configurar o cliente App-V 5,0 para receber atualizações do servidor de publicação.

**Observação**  Para os procedimentos a seguir, o servidor de gerenciamento foi instalado em um computador chamado **MyMgmtSrv**, e o servidor de publicação foi instalado em um computador chamado **MyPubSrv**.

 

**Para configurar o cliente do App-V 5,0 para receber atualizações do servidor de publicação**

1.  Implante os servidores de gerenciamento do App-V 5,0 e de publicação e adicione os pacotes e os grupos de conexão necessários. Para obter mais informações sobre como adicionar pacotes e grupos de conexão, consulte [como adicionar ou atualizar pacotes usando o console de gerenciamento](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) e [como criar um grupo de conexão](how-to-create-a-connection-group.md).

2.  Para abrir o console de gerenciamento, clique no link a seguir, abra um navegador e digite o seguinte: http://MyMgmtSrv/AppvManagement/Console.html em um navegador da Web e importe, publique e entitle todos os pacotes e grupos de conexão que serão necessários para um conjunto específico de usuários.

3.  No computador que executa o cliente App-V 5,0, abra um prompt de comando elevado do PowerShell, execute o seguinte comando:

    **Add-AppvPublishingServer-Name ABC-URL http://MyPubSrv/AppvPublishing**

    Esse comando irá configurar o servidor de publicação especificado. Você deve ver uma saída semelhante à seguinte:

    ID: 1

    SetByGroupPolicy: false

    Nome: ABC

    URL: http://MyPubSrv/AppvPublishing

    GlobalRefreshEnabled: false

    GlobalRefreshOnLogon: false

    GlobalRefreshInterval: 0

    GlobalRefreshIntervalUnit: dia

    UserRefreshEnabled: true

    UserRefreshOnLogon: true

    UserRefreshInterval: 0

    UserRefreshIntervalUnit: dia

    A ID retornada – nesse caso 1

4.  No computador que executa o cliente App-V 5,0, abra um prompt de comando do PowerShell e digite o seguinte comando:

    **Sync-AppvPublishingServer-serverID 1**

    O comando consultará o servidor de publicação para os pacotes e grupos de conexão que precisam ser adicionados ou removidos para esse cliente específico com base nos direitos dos pacotes e grupos de conexão conforme configurados no servidor de gerenciamento.

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Operações para o App-V 5.0](operations-for-app-v-50.md)

 

 





