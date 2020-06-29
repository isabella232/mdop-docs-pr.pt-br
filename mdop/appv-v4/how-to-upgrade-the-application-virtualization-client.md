---
title: Como fazer upgrade do Application Virtualization Client
description: Como fazer upgrade do Application Virtualization Client
author: dansimp
ms.assetid: 2a75d8b5-da88-456c-85bb-f5bd3d470f7f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b9748fbdba7c8d2777a06c93295e4582be784dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796928"
---
# Como fazer upgrade do Application Virtualization Client


Você pode usar os procedimentos a seguir para atualizar o cliente de área de trabalho do Application Virtualization (App-V) ou o cliente App-V para serviços de área de trabalho remota (antes serviços de terminal). Você atualiza o cliente instalando uma nova versão sobre a versão anterior instalada anteriormente. Quando você atualiza os clientes, o software do instalador preserva e migra automaticamente as configurações do usuário para aplicativos virtuais. É necessário ter direitos administrativos para executar o programa de instalação.

**Observação**  Durante a atualização para versões do Application Virtualization (App-V) 4.5 ou versões posteriores, as permissões para a chave do Registro HKCU são alteradas. Por isso, os usuários perderão as configurações de usuário que foram definidas anteriormente, como as configurações de modo desconectado do usuário definidas pelo usuário. Se o usuário não estiver ativamente importando a configuração do comportamento da interface de usuário do cliente por meio de um bloqueio de permissão, o usuário poderá redefinir essas preferências após uma atualização de publicação.

 

**Importante**  Ao atualizar para a versão 4.6 ou uma versão posterior do cliente App-V, você deve usar o instalador correto para o sistema operacional do computador, 32 bits ou 64 bits. A instalação não será bem-sucedida e uma mensagem de erro será exibida se você usar o instalador errado.

 

**Para atualizar o cliente da área de trabalho do Application Virtualization**

1.  Desligar todos os aplicativos virtuais, clique com o botão direito do mouse no ícone do cliente da área de trabalho do App-V exibido na área de notificação da área de trabalho do Windows e selecione **sair** para desligar o cliente existente.

2.  Depois de obter o arquivo morto correto do instalador e salvá-lo no seu computador, clique duas vezes nele para expandir o arquivo morto.

3.  Navegue até localizar o arquivo setup.exe e clique duas vezes setup.exe para iniciar a instalação.

4.  O assistente verifica o sistema para garantir que todos os softwares de pré-requisito estejam instalados e solicitará que você instale qualquer um dos seguintes, se ausente:

    -   Pacote redistribuível do Microsoft VisualC + + 2005SP1 (x86)

    -   Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)

    -   Relatório de erros do aplicativo Microsoft

    **Observação**  Para a versão 4.6 ou superior, o assistente também instalará o seguinte pré-requisito de software:

    -   Pacote redistribuível do Microsoft VisualC + + 2008SP1 (x86)

     

5.  Clique em **Instalar**. O progresso da instalação é exibido, e o status muda de **pendente** para **instalação**. O status de instalação muda para **bem-sucedida** à medida que cada etapa é concluída com êxito.

6.  Quando a caixa de diálogo de **cliente da área de trabalho do Application Virtualization** for exibida e exibir uma mensagem informando que uma versão mais antiga do cliente foi encontrada no computador, clique em **Avançar** para atualizar para a nova versão.

7.  Quando a tela **contrato de licença** for exibida, leia o contrato de licença e, se você concordar, clique em **aceito os termos do contrato de licença**e, em seguida, clique em **Avançar**.

8.  Quando o Assistente InstallShield exibir a tela de diálogo **pronto para atualizar o programa** , clique em **Atualizar** para iniciar a atualização. A tela seguinte indica que o cliente está sendo instalado.

    **Aviso**  Se você não tiver desligado o programa cliente na etapa 1, talvez veja um aviso **arquivos em uso** exibido. Se isso acontecer, clique com o botão direito do mouse no ícone do cliente App-V exibido na área de notificação da área de trabalho e selecione **sair** para desligar o cliente existente. Em seguida, clique em **repetir** para continuar.

     

9.  Quando a instalação for concluída com êxito, você será solicitado a reiniciar o computador. Você precisa reiniciar o computador para concluir a instalação.

    **Cuidado**  Se a atualização falhar por algum motivo, será preciso reiniciar o computador antes de tentar a atualização novamente.

     

**Para atualizar o cliente do Application Virtualization usando a linha de comando**

1.  Se estiver atualizando o cliente App-V usando o programa setup.msi, certifique-se de que todos os softwares de pré-requisito necessários foram instalados.

    **Importante**  
    -   Para a versão 4.6 e posterior do cliente App-V, o programa setup.msi verifica o sistema e irá falhar com uma mensagem de erro indicando que a instalação não pode continuar se o software de pré-requisito não estiver instalado.

    -   Para o App-V versão 4.6, os parâmetros de linha de comando não podem ser usados durante uma atualização e serão ignorados.

     

2.  O exemplo de linha de comando a seguir usa o arquivo setup.msi para atualizar o cliente App-V. Você precisará usar o programa de instalação do cliente correto, dependendo se estiver atualizando o cliente da área de trabalho do App-V ou o cliente App-V para serviços de área de trabalho remota (anteriormente serviços de terminal).

    **msiexec.exe/i "setup.msi"**

    **Importante**  As aspas são necessárias somente quando o valor contém um espaço. Para a consistência, todas as instâncias no exemplo anterior são mostradas como tendo aspas.

     

**Para atualizar o cliente do Application Virtualization para serviços de área de trabalho remota**

1.  Siga as políticas padrão da sua organização para instalar ou atualizar aplicativos no servidor host da sessão da área de trabalho remota (host RDSession). Se o sistema fizer parte de um farm, remova o host RDSession do farm de servidores.

2.  Para atualizar o cliente App-V para serviços de área de trabalho remota (anteriormente conhecido como serviços de terminal), você deve usar a linha de comando porque não é possível atualizar o cliente manualmente no host RDSession.

    **Observação**  Na versão 4,6 e posterior da App-V, além de usar a linha de comando para atualizar o cliente, você também pode usar uma sessão de área de trabalho remota. Nenhum parâmetro especial é necessário para iniciar a sessão da área de trabalho remota.

     

3.  Após concluir a atualização do cliente para serviços de área de trabalho remota, reinicie e conecte-se ao host RDSession.

4.  Após a reinicialização do sistema, adicione o servidor ao farm de servidores.

    **Cuidado**  Se a atualização falhar por algum motivo, será preciso reiniciar o computador antes de tentar a atualização novamente.

     

## Tópicos relacionados


[Considerações de atualização e implantação do Application Virtualization](application-virtualization-deployment-and-upgrade-considerations.md)

 

 





