---
title: Como fazer upgrade dos componentes de servidores e do sistema
description: Como fazer upgrade dos componentes de servidores e do sistema
author: dansimp
ms.assetid: 7d8374fe-5897-452e-923e-556a854b2024
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 61f8742a2f5e3c17083a77b839dfbee85ea00e24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796922"
---
# Como fazer upgrade dos componentes de servidores e do sistema


Use o procedimento a seguir para atualizar componentes de software instalados em todos os computadores do sistema do Application Virtualization. Os serviços do sistema do Application Virtualization serão reiniciados automaticamente em cada computador após a atualização.

**Observação**  
-   O processo de atualização interrompe todos os serviços do sistema do Application Virtualization, tirando o sistema de fora do serviço. As sessões de usuário devem ser desligadas antes do início do processo de atualização, e você deve parar todos os serviços de servidor de virtualização de aplicativos no seu ambiente.

-   Se você tiver mais de um servidor que está compartilhando o acesso ao banco de dados do Application Virtualization, todos esses servidores deverão ser colocados offline enquanto o banco de dados estiver sendo atualizado. Você deve seguir as práticas comerciais normais para a atualização do banco de dados, mas é altamente recomendável que você teste a atualização do banco de dados usando uma cópia de backup do banco de dados primeiro em um servidor de teste. Em seguida, você deve selecionar um dos servidores para a primeira atualização, o que fará a atualização do esquema de banco de dados. Depois que o banco de dados de produção for atualizado com êxito, você poderá atualizar os outros servidores.

-   Você pode atualizar para o Microsoft Application Virtualization (App-V) 4.5 somente a partir do Microsoft Application Virtualization (App-V) 4.1 ou 4.1 SP1. O App-V 4.0 e versões anteriores devem ser desinstalados ou atualizados para o 4.1 ou 4.1 SP1 antes da atualização para o App-V 4.5.

 

**Para atualizar componentes de software em computadores sistema do Application Virtualization**

1.  Navegue até o local do programa de instalação na rede, execute este programa da rede ou copie o diretório dele para o computador de destino e, em seguida, clique duas vezes no arquivo Setup.exe.

2.  Na página de **boas-vindas** do assistente de instalação, clique em **Avançar**.

3.  Na página **contrato de licença** , leia o contrato de licença, marque aceito **os termos do contrato de licença**e clique em **Avançar**.

4.  Quando a página **software instalado** abrir e exibir uma lista dos componentes de sistema instalados do aplicativo Virtualization e a versão de cada componente, clique em **Avançar**.

5.  Na página **aviso de perda de sessão** , leia a mensagem exibida e clique em **Avançar**.

6.  Na página **conectar-se ao banco de dados de configuração** , examine o conteúdo na página e clique em **Avançar**.

7.  Se a página de **atualização de banco de dados necessária** for exibida, será necessária uma atualização de banco de dados. Insira as credenciais administrativas do banco de dados e clique em **Avançar**. Se essa página não for exibida, pule para a etapa 9.

8.  Na página **banco de dados de configuração de backup** , marque as caixas apropriadas para executar o backup e exportá-las para um local existente e clique em **Avançar**.

    **Importante**  Se você quiser ser capaz de reverter para a versão anterior no caso de uma falha de atualização, verifique se você verificou a caixa **executar um backup do banco de dados de configuração** ou perderá os dados de configuração.

    Quando desejar restaurar um banco de dados com o VSS, primeiro você deve parar o serviço App-V Server no servidor de gerenciamento. Isso deve ser feito em todos os servidores de gerenciamento se houver mais de um servidor conectado ao mesmo banco de dados.

     

9.  Na primeira página de **validação do pacote** , leia o conteúdo e clique em **Avançar**.

10. Na segunda página de **validação do pacote** , você tem a opção de exibir os detalhes da validação do pacote em uma janela do bloco de notas. Para ver os detalhes, clique em **detalhes**; caso contrário, clique em **Avançar**.

11. Na página **pronto para atualizar o programa** , clique em **Avançar**.

12. Na página **Assistente de instalação concluído** , clique em **concluir**.

13. Repita as etapas de 1 a 12 em todos os outros computadores em que você instalou o console de gerenciamento do Application Virtualization ou o componente do software do servidor do Application Virtualization.

    Após a atualização do repositório de dados, você pode retomar a operação normal. (O repositório de dados é atualizado quando você atualiza qualquer servidor ou o serviço Web de gerenciamento do App-V.)

## Tópicos relacionados


[Considerações de atualização e implantação do Application Virtualization](application-virtualization-deployment-and-upgrade-considerations.md)

 

 





