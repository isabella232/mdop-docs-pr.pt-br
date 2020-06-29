---
title: Como instalar o cliente MED-V e o Console de Gerenciamento do MED-V
description: Como instalar o cliente MED-V e o Console de Gerenciamento do MED-V
author: dansimp
ms.assetid: 8a5f3010-3a50-487e-99d8-e352e5cb51c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 24a486cc7cf5534171f80b08dc93742e03cd4a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799981"
---
# Como instalar o cliente MED-V e o Console de Gerenciamento do MED-V


Os seguintes componentes do MED-V estão incluídos no pacote Client. msi:

-   Cliente MED-V — o software MED-V que deve ser instalado em computadores cliente para executar os espaços de trabalho do MED-V.

-   Console de gerenciamento do MED-V – a ferramenta administrativa que os administradores podem usar para criar e manter imagens, espaços de trabalho do MED-V e políticas.

O console de gerenciamento do MED-V e o cliente MED-V são instalados do pacote MED-V Client. msi. No entanto, o cliente MED-V pode ser instalado independentemente sem o console de gerenciamento do MED-V, desmarcando a caixa de seleção **instalar o aplicativo de gerenciamento do MED-v** durante a instalação.

**Observação**  
O cliente do MED-V e o console de gerenciamento do MED-V só podem ser instalados em computadores com Windows 7, Windows Vista e Windows XP. Eles não podem ser instalados em produtos de servidor.



**Observação**  
Não instale o cliente MED-V usando o comando **runas** do Windows.



**Para instalar o cliente MED-V**

1.  Faça logon como usuário com direitos de administrador local no computador local.

2.  Execute o pacote MED-V. msi.

    O pacote MED-V. msi é chamado *MED-V\_x.msi*, em que *x* é o número da versão.

    Por exemplo, *MED-V\_1.0.65.msi*.

3.  Quando a tela de **boas-vindas do Assistente InstallShield** for exibida, clique em **Avançar**.

4.  Na tela **contrato de licença** , leia o contrato de licença, clique em **aceito os termos do contrato de licença**e clique em **Avançar**.

    A tela de **pasta de destino** será exibida, com a pasta de instalação padrão exibida.

    A pasta de instalação padrão é o diretório onde o sistema operacional está instalado.

    -   Para alterar a pasta em que o MED-V deve ser instalado, clique em **alterar**e navegue até uma pasta existente.

5.  Clique em **Avançar**.

6.  Na tela de **configurações do MED-v** , configure a instalação do MED-v da seguinte maneira:

    -   Marque a caixa de seleção **instalar o aplicativo de gerenciamento do MED-V** para incluir o componente de gerenciamento na instalação.

        **Observação**  
        Os administradores de virtualização de área de trabalho corporativa devem instalar o aplicativo de gerenciamento do MED-V. Este aplicativo é necessário para configurar imagens da área de trabalho e espaços de trabalho do MED-V.



~~~
-   Select the **Load MED-V when Windows starts** check box to start MED-V automatically on startup.

-   Select the **Add a MED-V shortcut to my desktop** check box to create a MED-V shortcut on your desktop.

-   In the **Server address** field, type the server address.

-   In the **Server port** field, type the server's port.

-   Select the **Server requires encrypted connections (https)** check box to work with https.

-   The default virtual machine images folder is displayed. The default installation folder is *%systemdrive%\\MED-V Images\\*. To change the folder where MED-V should be installed, click **Change**, and browse to an existing folder.
~~~

7. Clique em **Avançar**.

8. Na tela **pronto para instalar o programa** , clique em **instalar**.

   A instalação do cliente do MED-V é iniciada. Isso pode levar alguns minutos, e a tela pode não exibir texto. Durante a instalação, várias telas de progresso são exibidas. Se aparecer uma mensagem, siga as instruções fornecidas.

   Após a instalação bem-sucedida, a tela **Assistente InstallShield concluído** é exibida.

9. Clique em **concluir** para fechar o assistente.

## Tópicos relacionados


[Configurações com suporte](supported-configurationsmedv-orientation.md)

[Listas de verificação para instalação e atualização](installation-and-upgrade-checklists.md)









