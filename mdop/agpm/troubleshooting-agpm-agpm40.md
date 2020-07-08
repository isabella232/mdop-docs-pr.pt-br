---
title: Solução de problemas do AGPM
description: Solução de problemas do AGPM
author: dansimp
ms.assetid: bedcd817-beb2-47bf-aebd-e3923c4fd06f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b44612cb9e3737a8d8f3109f76b0c9325d183383
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797668"
---
# Solução de problemas do AGPM


Esta seção lista alguns problemas comuns que você pode encontrar ao usar o gerenciamento avançado de política de grupo (AGPM) para gerenciar objetos de política de grupo (GPOs). Para diagnosticar problemas não listados aqui, pode ser útil para um administrador do AGPM (controle total) para usar o log e o rastreamento. Para obter mais informações, consulte [configurar log e rastreamento](configure-logging-and-tracing-agpm40.md).

**Observação**  
-   Para obter informações sobre como reverter para uma versão anterior de um GPO se houver problemas, confira [reverter para uma versão anterior de um GPO](roll-back-to-an-earlier-version-of-a-gpo-agpm40.md).

-   Para obter informações sobre como recuperar de um desastre restaurando o arquivo completo de um backup, consulte [restaurar o arquivo de um backup](restore-the-archive-from-a-backup-agpm40.md).

 

## Quais são os problemas que você está tendo?


-   [Não consigo acessar um arquivo morto](#bkmk-access-an-archive)

-   [O estado do GPO varia de acordo com os diferentes administradores de política de grupo](#bkmk-state-varies)

-   [Não consigo modificar a conexão do servidor do AGPM](#bkmk-modify-archive-location)

-   [Não consigo alterar o modelo padrão ou exibir, criar, editar, renomear, implantar ou excluir GPOs](#bkmk-perform-task)

-   [Não consigo usar um nome de GPO específico](#bkmk-use-particular-name)

-   [Não estou recebendo notificações por email do AGPM](#bkmk-email)

-   [Não consigo usar a porta 4600 para o serviço do AGPM](#bkmk-port)

-   [O serviço do AGPM não será iniciado](#bkmk-not-start)

-   [A instalação do software de política de grupo falha ao instalar o software](#bkmk-software-installation)

-   [Ocorreu um erro ao restaurar o arquivo morto para um novo servidor do AGPM](#bkmk-error-on-restore)

### <a href="" id="bkmk-access-an-archive"></a>Não consigo acessar um arquivo morto

-   **Causa**: você não selecionou o servidor e a porta corretos para o arquivo morto.

-   **Solução**:

    -   Se você for um administrador do AGPM: consulte [Configurar conexões do servidor do AGPM](configure-agpm-server-connections-agpm40.md).

    -   Se você não for um administrador do AGPM: solicite detalhes de conexão para o servidor do AGPM de um administrador do AGPM. Consulte [Configurar uma conexão com o servidor do AGPM](configure-an-agpm-server-connection-agpm40.md).

-   **Causa**: o serviço do AGPM não está em execução.

-   **Solução**:

    -   Se você for um administrador do AGPM: Inicie o serviço do AGPM. Para obter mais informações, consulte [Iniciar e interromper o serviço do AGPM](start-and-stop-the-agpm-service-agpm40.md).

    -   Se você não for um administrador do AGPM: entre em contato com um administrador do AGPM para obter assistência.

### <a href="" id="bkmk-state-varies"></a>O estado do GPO varia de acordo com os diferentes administradores de política de grupo

-   **Causa**: os administradores de política de grupo diferentes selecionaram servidores de AGPM diferentes para o mesmo arquivo morto.

-   **Solução**:

    -   Se você for um administrador do AGPM: consulte [Configurar conexões do servidor do AGPM](configure-agpm-server-connections-agpm40.md).

    -   Se você não for um administrador do AGPM: solicite detalhes de conexão para o servidor do AGPM de um administrador do AGPM. Consulte [Configurar uma conexão com o servidor do AGPM](configure-an-agpm-server-connection-agpm40.md).

### <a href="" id="bkmk-modify-archive-location"></a>Não consigo modificar a conexão do servidor do AGPM

-   **Causa**: se as configurações na guia **servidor do AGPM** não estiverem disponíveis, o servidor do AGPM foi configurado centralmente usando um modelo administrativo.

-   **Solução**:

    -   Se você for um administrador do AGPM: se as configurações na guia **servidor do AGPM** não estiverem disponíveis, consulte [Configurar conexões do servidor do AGPM](configure-agpm-server-connections-agpm40.md).

    -   Se você não for um administrador do AGPM: se as configurações na guia **servidor do AGPM** não estiverem disponíveis, você não precisará modificar o servidor do AGPM.

### <a href="" id="bkmk-perform-task"></a>Não consigo alterar o modelo padrão ou exibir, criar, editar, renomear, implantar ou excluir GPOs

-   **Causa**: você não recebeu uma função com as permissões necessárias para executar a tarefa ou tarefas.

-   **Solução**:

    -   Se você for um administrador do AGPM: consulte [delegar acesso ao nível do domínio ao arquivo morto](delegate-domain-level-access-to-the-archive-agpm40.md) e [delegar o acesso a um GPO individual no arquivo morto](delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md). As permissões do AGPM serão em cascata do domínio para todos os GPOs no arquivo morto. Para obter detalhes sobre quais funções podem executar uma tarefa e quais permissões são necessárias para executar uma tarefa, consulte a ajuda da tarefa.

    -   Se você não for um administrador do AGPM e precisar de funções ou permissões adicionais: entre em contato com um administrador do AGPM para obter assistência. Lembre-se de que, se você for um editor, poderá iniciar o processo de criação de um GPO, implantação de um GPO ou exclusão de um GPO do ambiente de produção do domínio, mas um Aprovador ou administrador do AGPM deve aprovar sua solicitação.

### <a href="" id="bkmk-use-particular-name"></a>Não consigo usar um nome de GPO específico

-   **Causa**: o nome do GPO já está em uso ou você não tem permissão para listar o GPO.

-   **Solução**:

    -   Se o nome do GPO aparecer na guia **controlado**, não **controlado**ou **pendente** , escolha outro nome. Se um GPO implantado for renomeado mas ainda não reimplantado, ele será exibido em seu nome antigo no ambiente de produção do domínio. Portanto, o nome antigo ainda está sendo usado. Reimplante o GPO para atualizar seu nome no ambiente de produção e libere o nome para ser usado por outro GPO.

    -   Se o nome do GPO não aparecer na guia **controlado**, não **controlado**ou **pendente** , talvez você não tenha permissão para listar o GPO. Para solicitar permissão, entre em contato com um administrador do AGPM.

### <a href="" id="bkmk-email"></a>Não estou recebendo notificações por email do AGPM

-   **Causa**: um servidor de email SMTP e um endereço de email válidos não foram fornecidos, ou nenhuma ação foi tomada e gera uma notificação por email.

-   **Solução**:

    -   Se você for um administrador do AGPM: para notificações por email sobre ações pendentes a serem enviadas pelo AGPM, um administrador do AGPM deve fornecer um servidor de email SMTP válido e endereços de email para aprovadores na guia de **delegação de domínio** . Para obter mais informações, consulte [Configurar notificação por email](configure-e-mail-notification-agpm40.md).

    -   As notificações por email são geradas apenas quando um editor, um revisor ou outro administrador de política de grupo que não tem a permissão necessária para criar, implantar ou excluir um GPO envia uma solicitação para que uma dessas ações ocorra. Não há nenhuma notificação automática de aprovação ou rejeição de uma solicitação.

### <a href="" id="bkmk-port"></a>Não consigo usar a porta 4600 para o serviço do AGPM

-   **Causa**: por padrão, a porta na qual o serviço do AGPM escuta é a porta 4600.

-   **Solução**: se a porta 4600 não estiver disponível para o serviço do AGPM, modifique a configuração de porta no servidor do AGPM para usar outra porta e, em seguida, atualize a porta na conexão do servidor do AGPM para clientes do AGPM. Para obter mais informações, consulte [Modificar o serviço do AGPM](modify-the-agpm-service-agpm40.md).

### <a href="" id="bkmk-not-start"></a>O serviço do AGPM não será iniciado

-   **Causa**: você modificou as configurações do serviço do AGPM no sistema operacional em **Ferramentas administrativas** e **Serviços**.

-   **Solução**: modifique as configurações para **gerenciamento avançado de política de grupo da Microsoft-servidor** em **programas e recursos** no painel de controle. Para obter mais informações, consulte [Modificar o serviço do AGPM](modify-the-agpm-service-agpm40.md).

### <a href="" id="bkmk-software-installation"></a>A instalação do software de política de grupo falha ao instalar o software

-   **Causa**: o AGPM preserva a integridade dos pacotes de instalação do software de política de grupo. Embora os GPOs sejam editados offline, os links entre pacotes além das informações de cliente armazenadas em cache são preservados. Isso ocorre por design.

-   **Solução**: ao editar um GPO offline com o AGPM, configure qualquer atualização de instalação de software de política de grupo de um pacote em outro GPO para fazer referência ao GPO implantado, e não à cópia com check-out. O editor deve ter permissão de **leitura** para o GPO implantado.

### <a href="" id="bkmk-error-on-restore"></a>Ocorreu um erro ao restaurar o arquivo morto para um novo servidor do AGPM

-   **Causa**: por motivos de segurança, a criptografia que protege a senha inserida na guia de **delegação de domínio** faz com que a senha falhe se o arquivo morto for movido para outro computador.

-   **Solução**: Digite novamente e confirme a senha na guia de **delegação de domínio** . Para obter mais informações, consulte [Configurar notificação por email](configure-e-mail-notification-agpm40.md).

 

 





