---
title: Como adicionar um pacote
description: Como adicionar um pacote
author: dansimp
ms.assetid: 5407fdbe-e658-44f6-a9b8-a566b81dedce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c580d7d131017c52e278adda0208ffcb2e86ccf2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797917"
---
# Como adicionar um pacote


Você pode adicionar um pacote do console de gerenciamento do servidor do Application Virtualization das seguintes maneiras:

-   Importar um aplicativo, que cria o pacote automaticamente no processo.

-   Adicione um pacote manualmente.

É recomendável importar aplicativos em vez de adicioná-los manualmente. Para obter mais informações sobre como importar aplicativos, consulte [como importar um aplicativo](how-to-import-an-applicationserver.md).

**Para adicionar um pacote manualmente**

1.  No console de gerenciamento do servidor do Application Virtualization, clique com o botão direito do mouse no nó **pacotes** no painel esquerdo e escolha **novo pacote**.

2.  Na caixa de diálogo **novo pacote** , digite um nome no campo **nome do pacote** .

3.  Procure ou digite um nome de caminho no campo **caminho completo do arquivo de pacote** . Deve ser um arquivo SFT.

    **Observação**  Se você navegar até o arquivo SFT, substitua o caminho local (como C:\\Arquivos de Files\\User\ _Apps \\Virtual\ _App \ _Server \\Content) pelo nome de host estático ou endereço IP do servidor. Usar a variável *% SFT \ _SOFTGRIDSERVER%* exige configuração do computador por cliente.

    Nas caixas de diálogo que fazem referência a servidores de aplicativos virtuais, você deve usar um local de rede, como o nome de host estático ou o endereço IP do servidor, que os usuários possam acessar. O arquivo Open Software Descriptor (OSD) do aplicativo pode substituir a variável de espaço reservado *% SFT \ _SOFTGRIDSERER%* com o nome de host estático ou o endereço IP do servidor estático. Se você deixar a variável de espaço reservado, será necessário definir essa variável em cada computador cliente que acessará esse servidor. Defina uma variável de usuário ou sistema em cada computador para SFT \ _SOFTGRIDSERVER. O valor da variável deve ser o nome de host estático ou o endereço IP do servidor. Se você definir uma variável, saia da sessão do cliente, desconecte-se do Microsoft Windows e, em seguida, reinicie a sessão em cada computador que tenha uma sessão em execução e o conjunto de variáveis.

     

4.  Clique em **Avançar**.

5.  A caixa de diálogo **Resumo** mostra o local do arquivo e solicita que você copie o arquivo para o local, caso ainda não tenha feito isso. Clique em **concluir** depois de verificar as informações.

    **Observação**  Se você estiver gerenciando aplicativos em um servidor remoto, na caixa de diálogo seguinte, digite apenas o caminho do arquivo relativo à raiz de conteúdo do servidor.

     

## Tópicos relacionados


[Como importar um aplicativo](how-to-import-an-applicationserver.md)

[Como gerenciar pacotes no Server Management Console](how-to-manage-packages-in-the-server-management-console.md)

 

 





