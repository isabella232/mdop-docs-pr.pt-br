---
title: Como aplicar configurações gerais a um espaço de trabalho do MED-V
description: Como aplicar configurações gerais a um espaço de trabalho do MED-V
author: dansimp
ms.assetid: 6152dced-e301-4fa2-bfa0-aecf3c23f23a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 176564ae1d22b27a24625d988f46c9746b291748
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799892"
---
# Como aplicar configurações gerais a um espaço de trabalho do MED-V


As configurações gerais permitem que você defina a experiência do usuário básica ao trabalhar com um espaço de trabalho do MED-V, definindo se o espaço de trabalho do MED-V aparecerá em integração sem falhas ou em modo de área de trabalho completo. Integração perfeita inclui aplicativos herdados na área de trabalho do host para que eles apareçam como se estivessem instalados diretamente no host. Área de trabalho completa apresenta a área de trabalho do sistema operacional do espaço de trabalho do MED-V em uma janela separada no host.

Todas as configurações gerais são configuradas no módulo de **política** , na guia **geral** .

**Para aplicar as configurações gerais a um espaço de trabalho do MED-V**

1.  Clique no espaço de trabalho do MED-V para configurar.

2.  Configure as propriedades gerais conforme descrito na tabela a seguir.

3.  No menu **política** , selecione **confirmar**.

**Propriedades gerais do espaço de trabalho**

Propriedades do *espaço de trabalho* descrição da propriedade

Nome

O nome do espaço de trabalho do MED-V.

**Aviso**  Não renomeie um espaço de trabalho do MED-V existente enquanto ele estiver em execução em um computador cliente.

 

Descrição

Descrição do espaço de trabalho do MED-V, que pode incluir o conteúdo ou o status do espaço de trabalho do MED-V e qualquer outra informação útil.

**Observação**  A descrição é para uso do administrador e não tem impacto sobre a política.

 

Informações de contato de suporte

As informações de contato para suporte técnico. As informações inseridas serão exibidas na tela informações de contato de suporte que podem ser acessadas na área de notificação do cliente MED-V.

*UI do espaço de trabalho*

Integração perfeita

Selecione esta opção para os ícones do espaço de trabalho do Windows, da barra de tarefas e da área de notificação para integrar-se perfeitamente à área de trabalho do host.

Desenhar um quadro em volta de cada janela do espaço de trabalho

Ao usar a integração direta, selecione esta opção para criar uma borda colorida em torno de todos os aplicativos executados no espaço de trabalho do MED-V e um plano de fundo colorido para todos os ícones de botão da barra de tarefas. No campo **cor do quadro** , selecione a cor.

Área de trabalho completa

Selecione essa opção para exibir o espaço de trabalho do MED-V como toda a área de trabalho, sem integração com o host.

*Verificação de host*

Linha de comando

Digite uma linha de comando para executar no host antes de iniciar o espaço de trabalho do MED-V.

Não iniciar o espaço de trabalho se a verificação falhar (o código de saída não é ' 0 ')

Marque esta caixa de seleção se você estiver usando uma linha de comando e deseja iniciar o espaço de trabalho do MED-V somente se o script for concluído com êxito.

 

Uma linha de comando pode ser executada no host antes de iniciar o espaço de trabalho do MED-V.

**Para executar uma linha de comando antes de iniciar um espaço de trabalho do MED-V**

1.  No campo **linha de comando** , insira uma linha de comando.

2.  Para iniciar o espaço de trabalho do MED-V somente se a linha de comando tiver sido bem-sucedida, marque a caixa de seleção não **iniciar o espaço de trabalho se a verificação falhar** .

## Tópicos relacionados


[Usando a interface de usuário do Console de Gerenciamento do MED-V](using-the-med-v-management-console-user-interface.md)

[Criando um espaço de trabalho do MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

 

 





