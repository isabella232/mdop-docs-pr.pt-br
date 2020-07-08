---
title: Como testar a publicação de aplicativos
description: Como testar a publicação de aplicativos
author: dansimp
ms.assetid: 17ba2e12-50a0-4f41-8300-f61f09db9f6c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 8dffb4f79ac89c7d419b27640f4f05364bd69e5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799967"
---
# Como testar a publicação de aplicativos


Depois de concluir o teste da configuração inicial, você pode verificar se a funcionalidade de publicação do aplicativo está funcionando como esperado executando as seguintes tarefas.

<a href="" id="bkmk-apppub"></a>**Para testar a publicação do aplicativo**

1.  Verifique se os aplicativos que você especificou para publicação estão visíveis.

    Clique em **Iniciar** e em **todos os programas** e procure os aplicativos especificados.

    Em alguns casos, você pode ter o mesmo aplicativo instalado duas vezes, uma vez no computador host e uma vez no convidado. Se um aplicativo publicado com o mesmo nome for publicado no mesmo local no menu **Iniciar** host, ele será diferenciado do atalho do aplicativo host adicionando o nome da máquina virtual ao nome do atalho. Por exemplo, para uma máquina virtual chamada "MEDVHost1", um aplicativo host pode ser "bloco de notas" e um aplicativo publicado pode ser "notepad (MEDVHost1)".

2.  Verifique se os aplicativos funcionam conforme o esperado.

    No computador host, inicie os aplicativos publicados e verifique se eles abrem no Windows XP SP3 no convidado. O aplicativo deve aparecer em uma janela no estilo do Windows XP na área de trabalho do computador host.

3.  Se aplicável, verifique se o redirecionamento do documento funciona conforme o esperado.

    Se um aplicativo publicado no convidado precisa abrir uma pasta na unidade do sistema host, verifique se ela pode abrir a pasta especificada.

    **Importante**  Como o Windows Virtual PC não dá suporte à criação de um compartilhamento de uma pasta que já esteja compartilhada, o redirecionamento não ocorre para documentos que se abrem em uma pasta compartilhada, como uma pasta meus documentos localizada na rede. Para obter mais informações, consulte [solução de problemas de operações](operations-troubleshooting-medv2.md).

Depois de verificar que os aplicativos publicados estão instalados e funcionando corretamente, você pode testar se os aplicativos podem ser adicionados ou removidos do espaço de trabalho do MED-V.

**Para testar se um aplicativo pode ser adicionado ou removido**

1.  Adicionar ou remover um aplicativo do espaço de trabalho do MED-V.

    Para obter informações sobre como adicionar e remover aplicativos de um espaço de trabalho do MED-V, consulte [Gerenciando aplicativos implantados em espaços de trabalho do MED-v](managing-applications-deployed-to-med-v-workspaces.md).

2.  Se você adicionou um aplicativo, repita as etapas em [para testar a publicação do aplicativo](#bkmk-apppub) para verificar se o novo aplicativo funciona conforme o esperado.

3.  Se você removeu um aplicativo, clique em **Iniciar** , em **todos os programas** e verifique se qualquer aplicativo removido não está mais listado.

**Observação**  Se você encontrar problemas ao verificar as configurações da publicação do aplicativo, consulte [solução de problemas de operações](operations-troubleshooting-medv2.md).

Depois de concluir o teste da publicação do aplicativo, você pode testar outras configurações do espaço de trabalho do MED-V para verificar se elas funcionam conforme o esperado.

Depois de concluir o teste do pacote do espaço de trabalho do MED-V e ter confirmado que ele está funcionando conforme o esperado, você pode implantar o espaço de trabalho do MED-V na sua empresa.

## Tópicos relacionados

[Como testar o redirecionamento da URL](how-to-test-url-redirection.md)

[Como verificar as configurações da primeira instalação](how-to-verify-first-time-setup-settings.md)

[Como implantar o pacote de espaço de trabalho da MED-V](deploying-the-med-v-workspace-package.md)

 

 





