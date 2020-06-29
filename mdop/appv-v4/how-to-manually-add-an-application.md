---
title: Como adicionar um aplicativo manualmente
description: Como adicionar um aplicativo manualmente
author: dansimp
ms.assetid: c635b07a-5c7f-4ab2-ba18-366457146cb9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 868939553fae6172ccca549ddc3f08aa76ee3c56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797057"
---
# Como adicionar um aplicativo manualmente


Ao adicionar um aplicativo ao servidor de gerenciamento do Application Virtualization, é recomendável importá-lo. Você pode adicionar um aplicativo manualmente, mas deve fornecer as informações exatas e detalhadas sobre o aplicativo chamado para nesta seção.

**Para adicionar manualmente um novo aplicativo**

1.  No painel esquerdo, clique com o botão direito do mouse no nó **aplicativos** e escolha **novo aplicativo**.

2.  No **Assistente novo aplicativo**, preencha a caixa de diálogo **informações gerais** :

    1.  **Nome do aplicativo**— digite o nome que você deseja que os usuários vejam.

    2.  **Versão**— digite a versão do aplicativo.

    3.  **Habilitado**– essa caixa deve ser selecionada para transmitir o aplicativo após criá-lo.

    4.  **Descrição**— digite uma descrição opcional para o uso administrativo.

    5.  **Caminho OSD**— procure a rede no arquivo Open Software DESCRIPTOR (OSD) do aplicativo. Esse arquivo deve estar em uma pasta de rede compartilhada.

    6.  **Caminho do ícone**— navegue até o arquivo ico do aplicativo.

    7.  **Grupo de licenças de aplicativos**— se você tiver configurado grupos de licenças, poderá atribuir o aplicativo a um selecionando-o na lista suspensa.

    8.  **Grupo de servidores**— se você tiver vários servidores de virtualização de aplicativos, poderá atribuir o aplicativo a um selecionando-o na lista pull-down.

3.  Clique em **Avançar**.

4.  Na caixa de diálogo **selecionar pacote** , selecione o pacote relacionado e clique em **Avançar**.

5.  Na tela **atalhos publicados** , marque as caixas dos locais em que você deseja que os atalhos do aplicativo apareçam nos computadores cliente e clique em **Avançar**.

6.  Na tela **associações de arquivo** , você pode adicionar novas associações de arquivo de tipo a esse aplicativo. Para fazer isso, clique em **Adicionar**, insira a extensão (sem um ponto precedente), insira uma descrição e clique em **OK**.

7.  Clique em **Avançar**.

8.  Na caixa de diálogo **permissões de acesso** , clique em **Adicionar**.

9.  Na caixa de diálogo **Adicionar/editar grupo de usuários** , navegue até o grupo usuário. Você também pode inserir o domínio e o grupo digitando as informações nos respectivos campos. Quando terminar, clique em **OK**. Você pode adicionar outros grupos com as mesmas páginas.

10. Clique em **Avançar**.

11. Na tela **Resumo** , você pode revisar as configurações de importação. Clique em **concluir** para adicionar o aplicativo, clique em **retornar** para alterar as informações ou clique em **Cancelar**.

## Tópicos relacionados


[Como gerenciar aplicativos no Server Management Console](how-to-manage-applications-in-the-server-management-console.md)

 

 





