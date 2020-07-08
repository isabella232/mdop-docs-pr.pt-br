---
title: Como instalar o cliente MED-V
description: Como instalar o cliente MED-V
author: dansimp
ms.assetid: bfac6de7-d96d-4b3e-bd8b-183e051e53c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2e4468b15c0c196bf605b1b5d129ab38678ec74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800023"
---
# Como instalar o cliente MED-V


Em um cenário baseado em pacote de implantação, a instalação do cliente do MED-V está incluída no pacote de implantação e instalada diretamente do pacote.

**Importante**  
Ao usar um pacote de implantação que não inclua uma imagem, certifique-se de que a imagem seja carregada na Web ou por push para a pasta de pré-teste antes de instalar o pacote de implantação.



**Para instalar um pacote de implantação**

1.  Siga um destes procedimentos:

    -   Baixe o pacote do MED-V na Web.

    -   Insira o DVD ou USB de implantação na unidade host.

2.  Se o MED-V não iniciar automaticamente, clique duas vezes MED-VAutoInstaller.exe.

    Uma caixa de diálogo é exibida listando os componentes que já estão instalados e os que estão sendo instalados no momento.

    **Observação**  
    Se houver uma versão do Microsoft Virtual PC sem suporte no computador host, será exibida uma mensagem informando que você deseja desinstalar a versão existente e executar o instalador novamente.



~~~
**Note**  
If an older version of the MED-V client exists, it will prompt you asking whether you want to upgrade.



Depending on the components that have been installed, you might need to reboot. If rebooting is necessary, a message appears notifying you that you must reboot.
~~~

3. Se necessário, reinicie o computador.

   Quando a instalação estiver concluída, o MED-V será iniciado e será exibida uma mensagem informando que a instalação foi concluída.

4. Conecte-se ao MED-V usando o nome de usuário e a senha a seguir:

   -   Digite o nome de domínio e o nome de usuário seguidos da senha do usuário do domínio que tem permissão para funcionar com o MED-V.

       Exemplo: "domínio \ _name \\user\ _name", "senha"

## Tópicos relacionados


[Como configurar um pacote de implantação](how-to-configure-a-deployment-package.md)

[Como carregar uma imagem do MED-V no servidor](how-to-upload-a-med-v-image-to-the-server.md)

[Referência de linha de comando para instalação do cliente](client-installation-command-line-reference.md)









