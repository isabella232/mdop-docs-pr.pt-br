---
title: Como testar o redirecionamento da URL
description: Como testar o redirecionamento da URL
author: dansimp
ms.assetid: 38d80088-da1d-4098-b27e-76f9e78f81dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d964cf9d0114d3085d7e8952eebc82486b7b76cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799474"
---
# Como testar o redirecionamento da URL


Depois de concluir o teste da configuração inicial, você pode verificar se a funcionalidade de redirecionamento de URL está funcionando como esperado executando as seguintes tarefas.

**Importante**  O agente de host do MED-V deve estar em execução para que o redirecionamento de URL funcione corretamente.

<a href="" id="bkmk-urlredir"></a>**Para testar o redirecionamento de URL**

1.  Abra um navegador do Internet Explorer no computador host e insira uma URL que você especificou para o redirecionamento.

2.  Verifique se a página da Web está aberta no Internet Explorer na máquina virtual convidada.

3.  Repita esse processo para cada URL que você deseja testar.

**Para testar se uma URL pode ser adicionada ou removida**

1.  Adicione ou remova uma URL do espaço de trabalho do MED-V.

    Para obter informações sobre como adicionar e remover URLs para redirecionamento em um espaço de trabalho do MED-V, consulte [gerenciar o redirecionamento de URL do MED-v](manage-med-v-url-redirection.md).

2.  Se você adicionou uma URL à lista de redirecionamento, repita as etapas em [para testar o redirecionamento de URL](#bkmk-urlredir) para verificar se a nova URL é redirecionada conforme o esperado.

3.  Se você removeu uma URL da lista de redirecionamento, verifique se ela foi removida seguindo estas etapas:

    1.  Abra um navegador do Internet Explorer no computador host e insira a URL que você removeu da lista de redirecionamento.

    2.  Verifique se a página da Web está aberta no Internet Explorer no computador host, em vez de na máquina virtual convidada.

        **Observação**  Pode levar alguns segundos para que as alterações de redirecionamento de URL sejam realizadas.

**Observação**  Se você tiver problemas ao verificar suas configurações de redirecionamento de URL, consulte [solução de problemas de operações](operations-troubleshooting-medv2.md).

Depois de concluir o teste do redirecionamento de URL no seu espaço de trabalho do MED-V, você pode testar outras configurações para verificar se elas funcionam conforme o esperado.

Depois de concluir o teste do pacote do espaço de trabalho do MED-V e ter confirmado que ele está funcionando conforme o esperado, você pode implantar o espaço de trabalho do MED-V na sua empresa.

## Tópicos relacionados

[Como testar a publicação de aplicativos](how-to-test-application-publishing.md)

[Como verificar as configurações da primeira instalação](how-to-verify-first-time-setup-settings.md)

[Como implantar o pacote de espaço de trabalho da MED-V](deploying-the-med-v-workspace-package.md)

 

 





