---
title: Solução de problemas do Gerenciamento Avançado de Política de Grupo
description: Solução de problemas do Gerenciamento Avançado de Política de Grupo
author: dansimp
ms.assetid: f58849cf-6c5b-44d8-b356-0ed7a5b24cee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c22b9a0983b26252ee0d9c8d99b63cd4ab5dc2b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797288"
---
# Solução de problemas do Gerenciamento Avançado de Política de Grupo


Esta seção lista alguns problemas comuns que você pode encontrar ao usar o gerenciamento avançado de política de grupo (AGPM) para gerenciar objetos de política de grupo (GPOs).

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

### <a href="" id="bkmk-access-an-archive"></a>Não consigo acessar um arquivo morto

-   **Causa**: você não selecionou o servidor e a porta corretos para o arquivo morto.

-   **Solução**:

    -   Se você for um administrador do AGPM: consulte [Configurar a conexão do servidor do AGPM](configure-the-agpm-server-connection.md).

    -   Se você não for um administrador do AGPM: solicite detalhes de conexão para o servidor do AGPM de um administrador do AGPM. Consulte [Configurar a conexão do servidor do AGPM](configure-the-agpm-server-connection-reviewer.md).

-   **Causa**: o serviço de gerenciamento de política de grupo avançado não está em execução.

-   **Solução**:

    -   Se você for um administrador do AGPM: Inicie o serviço do AGPM. Para obter mais informações, consulte [Iniciar e interromper o serviço do AGPM](start-and-stop-the-agpm-service.md).

    -   Se você não for um administrador do AGPM: entre em contato com um administrador do AGPM para obter assistência.

### <a href="" id="bkmk-state-varies"></a>O estado do GPO varia de acordo com os diferentes administradores de política de grupo

-   **Causa**: os administradores de política de grupo diferentes selecionaram servidores de AGPM diferentes para o mesmo arquivo morto.

-   **Solução**:

    -   Se você for um administrador do AGPM: consulte [Configurar a conexão do servidor do AGPM](configure-the-agpm-server-connection.md).

    -   Se você não for um administrador do AGPM: solicite detalhes de conexão para o servidor do AGPM de um administrador do AGPM. Consulte [Configurar a conexão do servidor do AGPM](configure-the-agpm-server-connection-reviewer.md).

### <a href="" id="bkmk-modify-archive-location"></a>Não consigo modificar a conexão do servidor do AGPM

-   **Causa**: se as configurações na guia **servidor do AGPM** não estiverem disponíveis, o servidor do AGPM foi configurado centralmente usando um modelo administrativo.

-   **Solução**:

    -   Se você for um administrador do AGPM: se as configurações na guia **servidor de AGPM** não estiverem disponíveis, consulte [Configurar a conexão do servidor do AGPM](configure-the-agpm-server-connection.md).

    -   Se você não for um administrador do AGPM: se as configurações na guia **servidor do AGPM** não estiverem disponíveis, você não precisará modificar o servidor do AGPM.

### <a href="" id="bkmk-perform-task"></a>Não consigo alterar o modelo padrão ou exibir, criar, editar, renomear, implantar ou excluir GPOs

-   **Causa**: você não recebeu uma função com as permissões necessárias para executar a tarefa ou tarefas.

-   **Solução**:

    -   Se você for um administrador do AGPM: consulte [delegar](delegate-domain-level-access.md) acesso a nível de domínio e [acesso de representante a um GPO individual](delegate-access-to-an-individual-gpo.md). As permissões do AGPM serão em cascata do domínio para todos os GPOs no arquivo morto. Como novos administradores de política de grupo são adicionados no nível do domínio, suas permissões devem ser definidas para aplicar-se a **esse objeto e a objetos aninhados**. Para obter detalhes sobre quais funções podem executar uma tarefa e quais permissões são necessárias para executar uma tarefa, consulte a ajuda da tarefa.

    -   Se você não for um administrador do AGPM e precisar de funções ou permissões adicionais: entre em contato com um administrador do AGPM para obter assistência. Observe que, se você for um editor, você pode iniciar o processo de criação de um GPO, implantação de um GPO ou exclusão de um GPO do ambiente de produção, mas um Aprovador ou administrador do AGPM deve aprovar sua solicitação.

### <a href="" id="bkmk-use-particular-name"></a>Não consigo usar um nome de GPO específico

-   **Causa**: o nome do GPO já está em uso ou você não tem permissão para listar o GPO.

-   **Solução**:

    -   Se o nome do GPO aparecer na guia **controlado**, não **controlado**ou **pendente** , escolha outro nome. Se um GPO que foi implantado for renomeado mas ainda não reimplantado, ele será exibido em seu nome antigo no ambiente de produção – portanto, o nome antigo ainda estará em uso. Reimplante o GPO para atualizar seu nome no ambiente de produção e libere o nome para ser usado por outro GPO.

    -   Se o nome do GPO não aparecer na guia **controlado**, não **controlado**ou **pendente** , talvez você não tenha permissão para listar o GPO. Para solicitar permissão, entre em contato com um administrador do AGPM.

### <a href="" id="bkmk-email"></a>Não estou recebendo notificações por email do AGPM

-   **Causa**: um servidor de email SMTP e um endereço de email válidos não foram fornecidos, ou nenhuma ação foi tomada e gera uma notificação por email.

-   **Solução**:

    -   Se você for um administrador do AGPM: para notificações por email sobre ações pendentes a serem enviadas pelo AGPM, um administrador do AGPM deve fornecer um servidor de email SMTP válido e endereços de email para aprovadores na guia de **delegação de domínio** . Para obter mais informações, consulte [Configurar notificação por email](configure-e-mail-notification.md).

    -   As notificações por email são geradas apenas quando um editor, um revisor ou outro administrador de política de grupo que não tem a permissão necessária para criar, implantar ou excluir um GPO envia uma solicitação para que uma dessas ações ocorra. Não há nenhuma notificação automática de aprovação ou rejeição de uma solicitação.

### <a href="" id="bkmk-port"></a>Não consigo usar a porta 4600 para o serviço do AGPM

-   **Causa**: por padrão, a porta na qual o serviço do AGPM escuta é a porta 4600.

-   **Solução**: se a porta 4600 não estiver disponível para o serviço do AGPM, modifique cada arquivo de índice do arquivo para usar outra porta e, em seguida, atualize o servidor do AGPM para todos os administradores de política de grupo. Para obter mais informações, consulte [Modificar a porta na qual o serviço do AGPM escuta](modify-the-port-on-which-the-agpm-service-listens.md).

### <a href="" id="bkmk-not-start"></a>O serviço do AGPM não será iniciado

-   **Causa**: você modificou as configurações do serviço do AGPM no sistema operacional em **Ferramentas administrativas** e **Serviços**.

-   **Solução**: modifique as configurações para **gerenciamento avançado de política de grupo da Microsoft-servidor** em **Adicionar ou remover programas**. Para obter mais informações, consulte [Modificar a conta do serviço do AGPM](modify-the-agpm-service-account.md).

### <a href="" id="bkmk-software-installation"></a>A instalação do software de política de grupo falha ao instalar o software

-   **Causa**: o AGPM preserva a integridade dos pacotes de instalação do software de política de grupo. Embora os GPOs sejam editados offline, os links entre pacotes e as informações de cliente armazenadas em cache são preservados. Isso ocorre por design.

-   **Solução**: ao editar um GPO offline com o AGPM, configure qualquer atualização de instalação de software de política de grupo de um pacote em outro GPO para fazer referência ao GPO implantado e não à cópia com check-out. O editor deve ter permissão de **leitura** para o GPO implantado.

 

 





