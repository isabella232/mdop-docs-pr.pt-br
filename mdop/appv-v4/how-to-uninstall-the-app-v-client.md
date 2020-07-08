---
title: Como desinstalar o cliente do App-V
description: Como desinstalar o cliente do App-V
author: dansimp
ms.assetid: 07591270-9651-4bb5-a5b3-e0fc009bd9e2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: acb3f53b42027ff2c1b84fd2ab2bdde3c52f96de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796942"
---
# Como desinstalar o cliente do App-V


Use o procedimento a seguir para desinstalar o cliente Application Virtualization do computador.

**Para desinstalar o cliente de desktop do Application Virtualization**

1.  No painel de controle, clique duas vezes em **Adicionar ou remover programas** (ou, no Windows Vista, **programas e recursos**) e, em seguida, clique duas vezes em **cliente da área de trabalho do Microsoft Application Virtualization**.

2.  Na caixa de diálogo exibida, clique em **Sim** para continuar com o processo de desinstalação.

    **Importante**  O processo de desinstalação não pode ser cancelado ou interrompido.

     

3.  Quando uma mensagem informando que o aplicativo da bandeja do cliente Microsoft Application Virtualization deve ser fechada antes de continuar aparecer, clique com o botão direito do mouse no ícone do App-V na área de notificação e selecione **sair** para fechar o aplicativo. Em seguida, clique em **repetir** para continuar com o processo de desinstalação.

    **Importante**  Você pode ver uma mensagem informando que um ou mais aplicativos virtuais estão em uso. Feche todos os aplicativos abertos e salve os dados antes de continuar. Em seguida, clique em **OK** para continuar com o processo de desinstalação.

     

4.  Uma barra de progresso mostra o tempo restante. Quando esta etapa terminar, você deverá reiniciar o computador para que todos os drivers associados possam ser interrompidos para concluir o processo de desinstalação.

    **Observação**  As seguintes chaves do registro permanecem após o processo de desinstalação ser concluído:

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard "cliente" = DWORD: 00000000

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey

     

## Tópicos relacionados


[Como instalar o cliente usando a linha de comando](how-to-install-the-client-by-using-the-command-line-new.md)

[Como instalar manualmente o Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)

[Como publicar um aplicativo virtual no cliente](how-to-publish-a-virtual-application-on-the-client.md)

 

 





