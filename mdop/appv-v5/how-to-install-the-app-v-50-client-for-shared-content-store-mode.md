---
title: Como instalar o cliente App-V 5.0 para o modo de repositório de conteúdo compartilhado
description: Como instalar o cliente App-V 5.0 para o modo de repositório de conteúdo compartilhado
author: dansimp
ms.assetid: 88f09e6f-19e7-48ea-965a-907052d1a02f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 704ea6c1e4b1ba4670a4e52d754b8e6e5a9fb8f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796404"
---
# Como instalar o cliente App-V 5.0 para o modo de repositório de conteúdo compartilhado


Use o procedimento a seguir para instalar o cliente do Microsoft Application Virtualization (App-V) 5,0 para que ele use o modo SCS (Shared Content Store) do App-V 5,0. Você deve certificar-se de que todos os pré-requisitos necessários estejam instalados no computador para o qual você planeja instalar. Use o link a seguir para os [pré-requisitos do App-V 5,0](app-v-50-prerequisites.md).

**Observação**  Antes de executar este procedimento, se necessário, desinstale qualquer versão existente do cliente App-V 5,0.

 

Para obter mais informações sobre o modo SCS, consulte [repositório de conteúdo compartilhado no Microsoft App-V 5,0 – por trás dos bastidores](https://go.microsoft.com/fwlink/?LinkId=316879) ( https://go.microsoft.com/fwlink/?LinkId=316879) .

**Instalar e configurar o cliente do App-V 5,0 para o modo SCS**

1.  Copie os arquivos de instalação do cliente do App-V 5,0 para o computador em que ele será instalado. Abra uma linha de comando e do diretório em que os arquivos de instalação são salvos digite uma das opções a seguir, dependendo da versão do cliente que você está instalando:

    -   Para instalar a versão RDS do tipo de cliente App-V 5,0: **appv\_client\_setup\_rds.exe/SHAREDCONTENTSTOREMODE = 1/q**

    -   Para instalar a versão padrão do tipo de cliente App-V 5,0: **appv\_client\_setup.exe/SHAREDCONTENTSTOREMODE = 1/q**

        **Importante**  Você deve executar uma instalação silenciosa ou haverá falha na instalação.

         

2.  Depois de concluir a instalação, você pode implantar pacotes no computador que está executando o cliente e todo o conteúdo do pacote será transmitido na rede.

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Implantação do sequenciador e do cliente App-V 5.0](deploying-the-app-v-50-sequencer-and-client.md)

 

 





