---
title: Guia Servidor do AGPM
description: Guia Servidor do AGPM
author: dansimp
ms.assetid: fb3b0265-53ed-4bf6-88a4-c409f5f1bed4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 335cad07691f914884583636cef01be8dbaa0266
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797495"
---
# Guia Servidor do AGPM


A guia **servidor do AGPM** no painel de **controle alterar** permite que você selecione um servidor do AGPM inserindo um nome de computador e uma porta totalmente qualificados e para excluir versões mais antigas dos objetos de política de grupo (GPOs) do arquivo para conservar o espaço em disco no servidor do AGPM.

## Especificando o servidor do AGPM


O servidor do AGPM selecionado determina qual arquivo é exibido para você na guia **conteúdo** e para qual local as configurações de **delegação de domínio** são aplicadas. A porta padrão do AGPM (gerenciamento avançado de política de grupo) é a porta 4600.

Se a conexão do servidor de AGPM estiver configurada de forma centralizada usando as configurações de modelo administrativo, as opções nesta guia para configurar a conexão não estarão disponíveis. Para obter mais informações, consulte [Configurar conexões do servidor de AGPM](configure-agpm-server-connections-agpm30ops.md).

## Excluindo versões antigas do GPO


Por padrão, todas as versões de cada GPO controlado são mantidas no arquivo morto. No entanto, você pode configurar o serviço do AGPM para limitar o número de versões retidas para cada GPO e excluir automaticamente a versão mais antiga quando esse limite for excedido. Somente as versões de GPO exibidas na guia **versões exclusivas** da janela do **histórico** contam para o limite.

**Observação**  O número máximo de versões exclusivas a serem armazenadas para cada GPO não inclui a versão atual, portanto, digitar 0 retém somente a versão atual. O limite não deve ser maior do que as versões do 999.

Quando uma versão do GPO é excluída, um registro dessa versão permanece no histórico do GPO, mas a própria versão do GPO é excluída do arquivamento. Você pode impedir que uma versão do GPO seja excluída marcando-a no histórico como indispensável.

 

### Referências adicionais

-   [Interface do usuário: Gerenciamento Avançado de Política de Grupo](user-interface-advanced-group-policy-management-agpm30ops.md)

-   [Executar tarefas de administração de AGPM](performing-agpm-administrator-tasks-agpm30ops.md)

-   [Execução de tarefas do revisor](performing-reviewer-tasks-agpm30ops.md)

 

 





