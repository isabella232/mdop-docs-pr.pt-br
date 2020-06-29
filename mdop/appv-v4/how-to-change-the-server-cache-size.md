---
title: Como alterar o tamanho do cache do servidor
description: Como alterar o tamanho do cache do servidor
author: dansimp
ms.assetid: 24e63744-21c3-458e-b137-9592f4fe785c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92e56a8a28f7a00d71805b497f9e404cca65919d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797243"
---
# Como alterar o tamanho do cache do servidor


Você pode usar o procedimento a seguir para alterar o tamanho do cache de qualquer servidor diretamente do console de gerenciamento do servidor do Application Virtualization.

**Observação**  Embora você possa alterar o tamanho do cache, a menos que sua configuração exija especificamente que você altere o tamanho, é recomendável deixar o tamanho do cache definido para os valores padrão.

 

**Para alterar o tamanho do cache do servidor**

1.  Clique no nó **Server groups** no painel esquerdo para expandir a lista de grupos de servidores.

2.  No painel de **resultados** , clique duas vezes no grupo de servidores desejado para exibir a lista de servidores do grupo.

3.  No painel de **resultados** , clique com o botão direito do mouse no servidor desejado e selecione **Propriedades**.

4.  Selecione a guia **avançado** .

5.  Insira um valor no campo de **alocação máxima de memória** para o cache do servidor e insira um valor para o nível de aviso de limite no campo aviso de **alocação de memória** .

6.  Insira um valor no campo **tamanho máximo do bloco** . Esse número deve ser maior ou igual ao tamanho máximo do bloco do maior pacote que será transmitido do servidor.

7.  Clique em **OK**.

## Tópicos relacionados


[Como alterar a porta do servidor](how-to-change-the-server-port.md)

[Como gerenciar servidores no Server Management Console](how-to-manage-servers-in-the-server-management-console.md)

 

 





