---
title: Exibição e configuração de logs da MED-V
description: Exibição e configuração de logs da MED-V
author: dansimp
ms.assetid: a15537ce-981d-4f55-9c3c-e7fbf94b8fe5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7984cec072827136db9ea52a535c0ea44c6bc2c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799330"
---
# Exibição e configuração de logs da MED-V


Ao solucionar problemas e problemas do MED-V, talvez você ache útil ou necessário acessar os logs de eventos do MED-V. Você pode abrir o Visualizador de eventos para o computador host e para a máquina virtual convidada usando o kit de ferramentas de administração do MED-V. Você também pode usar o kit de ferramentas de administração do MED-V para definir o nível de log no qual os logs de eventos do MED-V relatam eventos do MED-V.

Para obter informações sobre como abrir o kit de ferramentas de administração do MED-V, consulte [solução de problemas do MED-v usando o kit de ferramentas de administração](troubleshooting-med-v-by-using-the-administration-toolkit.md).

## Exibir logs de eventos do MED-V


Na janela do **Kit de ferramentas de administração do MED-V** , clique em eventos do **host** para abrir o Visualizador de eventos para o computador host. Ou clique em **eventos de convidado** para abrir o Visualizador de eventos para a máquina virtual convidada.

O Visualizador de eventos abre e exibe os logs de eventos correspondentes que você pode usar para solucionar os problemas que podem ocorrer ao implantar ou gerenciar o MED-V. Por padrão, somente erros e avisos são exibidos. Para obter mais informações sobre IDs e mensagens específicas do evento, consulte [mensagens de log de eventos do MED-V](med-v-event-log-messages.md).

**Observação**  Os usuários finais só poderão salvar arquivos de log de eventos no convidado se tiverem permissões administrativas.

 

### Para abrir manualmente o Visualizador de eventos no computador host

1.  Clique em **Iniciar**, em **painel de controle**e em **Ferramentas administrativas**.

2.  Clique duas vezes em **Visualizador de eventos**e, em seguida, clique em **logs de aplicativos e serviços**.

3.  Clique duas vezes em **medv**.

## Configurando logs de eventos do MED-V


Você pode especificar o nível do log de eventos do MED-V selecionando o botão de opção correspondente no kit de ferramentas de administração do MED-V. Você pode decidir se o log de eventos inclui apenas erros, erros e avisos ou mensagens informativas e erros. O nível de log de eventos especificado é definido para o computador host e para a máquina virtual convidada.

Você também pode especificar o nível de log de eventos editando o valor do registro EventLogLevel. Para obter mais informações, consulte [Gerenciando as configurações do espaço de trabalho do MED-V](managing-med-v-workspace-configuration-settings.md).

**Observação**  O nível que você especifica na janela do **Kit de ferramentas de administração do MED-v** se aplica a futuros registros de eventos do MED-v. Se você definir o nível para capturar todos os erros, avisos e mensagens informativas, os logs de eventos serão preenchidos mais rapidamente e os eventos mais antigos serão removidos.

 

## Tópicos relacionados


[Reiniciar e redefinir um espaço de trabalho da MED-V](restarting-and-resetting-a-med-v-workspace.md)

[Exibição de configurações do espaço de trabalho da MED-V](viewing-med-v-workspace-configurations.md)

 

 





