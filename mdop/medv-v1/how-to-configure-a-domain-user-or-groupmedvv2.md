---
title: Como configurar um usuário ou grupo de domínio
description: Como configurar um usuário ou grupo de domínio
author: dansimp
ms.assetid: 055aba81-a9c9-4b98-969d-775e603becf3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c51da13808df657c1341572767c24860d9d5e8b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800024"
---
# Como configurar um usuário ou grupo de domínio


As configurações de implantação permitem controlar quais usuários ou grupos podem acessar o espaço de trabalho do MED-V, bem como quanto tempo o espaço de trabalho do MED-V pode ser utilizado e se ele pode ser usado offline. Você também pode configurar regras adicionais para controlar o acesso entre o espaço de trabalho do MED-V e o host.

Todas as permissões do espaço de trabalho do MED-V são configuradas no módulo de **política** , na guia **implantação** .

Para permitir que os usuários utilizem o espaço de trabalho do MED-V, você deve primeiro adicionar usuários ou grupos do domínio às permissões do espaço de trabalho do MED-V. Em seguida, você pode definir permissões para cada usuário ou grupo.

## Como adicionar um usuário ou grupo de domínio


**Para adicionar um usuário ou grupo de domínio**

1.  Na janela **usuários/grupos** , clique em **Adicionar.**

2.  Na caixa de diálogo **Inserir nomes de usuário ou grupo** , selecione usuários de domínio ou grupos seguindo um destes procedimentos:

    -   No campo **Inserir nomes de usuário ou grupo** , digite um usuário ou grupo que exista no domínio ou como um usuário ou grupo local no computador. Em seguida, clique em **verificar nomes** para resolvê-lo para o nome completo existente.

    -   Clique em **Localizar** para abrir a caixa de diálogo **Selecionar usuários ou grupos** padrão. Em seguida, selecione usuários ou grupos do domínio.

3.  Clique em **OK**.

    Os usuários do domínio ou grupos são adicionados.

    **Observação**  
    Os usuários de domínios confiáveis devem ser adicionados manualmente.



~~~
**Warning**  
Do not run the management application from a computer that is part of a domain that is not trusted by the domain the server is installed on.
~~~



## Como remover um usuário ou grupo de domínio


**Para remover um usuário ou grupo de domínio**

1.  Na janela **usuários/grupos** , selecione um usuário ou grupo.

2.  Clique em **remover**.

    O usuário ou grupo é excluído.

## Como definir permissões para um usuário ou um grupo


**Para definir permissões para um usuário ou um grupo**

1.  Clique no usuário ou grupo para o qual você está configurando as permissões.

2.  Configure as propriedades do espaço de trabalho do MED-V conforme descrito na tabela a seguir.

3.  No menu **política** , selecione **confirmar**.

**Propriedades de implantação do espaço de trabalho**

Descrição da propriedade *geral*

Habilitar espaço de trabalho para &lt; usuário ou grupo&gt;

Marque esta caixa de seleção para habilitar o espaço de trabalho do MED-V para este usuário ou grupo.

O espaço de trabalho vence nesta data

Marque esta caixa de seleção para atribuir uma data de expiração para as permissões definidas para este usuário ou grupo.

Quando selecionada, a caixa data é habilitada. Defina a data e as permissões vencerão no final da data especificada.

O trabalho offline está restrito a

Marque esta caixa de seleção para atribuir um período de tempo no qual a política deve ser atualizada para este usuário ou grupo. Quando selecionada, a caixa período de tempo é habilitada. Defina o número de dias ou horas e, no final do período de tempo especificado, o usuário ou grupo não poderá se conectar se a política não for atualizada.

Opções de exclusão do espaço de trabalho

Clique para definir as opções de exclusão do espaço de trabalho do MED-V. Para obter mais informações, consulte [como definir as opções de exclusão do espaço de trabalho do MED-V](how-to-set-med-v-workspace-deletion-options.md).

*Transferência de dados*

Área de transferência de suporte entre host e espaço de trabalho

Marque esta caixa de seleção para habilitar a cópia e a colagem entre o host e o espaço de trabalho do MED-V.

Suporte para transferência de arquivos entre o host e o espaço de trabalho

Marque esta caixa de seleção para habilitar a transferência de arquivos entre o host e o espaço de trabalho do MED-V. Selecione uma das seguintes opções na caixa **transferência de arquivo** :

-   **Ambos**— permitem transferir arquivos entre o host e o espaço de trabalho do MED-V.

-   **Host para espaço de trabalho**— habilite a transferência de arquivos do host para o espaço de trabalho do MED-V.

-   **Espaço de trabalho para o host**— habilite a transferência de arquivos do espaço de trabalho do MED-V para o host.

**Observação**  
Se um usuário sem permissões tentar transferir arquivos, será exibida uma janela solicitando que ele Insira as credenciais de um usuário com permissões para executar a transferência de arquivo.



**Importante**  
Para dar suporte à transferência de arquivos no Windows XP SP3, você deve desativar a sincronização de arquivos offline editando o registro da seguinte maneira:

`REG ADD HKLM\software\microsoft\windows\currentversion\netcache /V Enabled /T REG_DWORD /F /D 0`



Avançado

Clique para definir as opções avançadas de transferência de arquivo. Para obter mais informações, consulte [como definir opções avançadas de transferência de arquivo](how-to-set-advanced-file-transfer-options.md).

*Controle de dispositivo*

Habilitar a impressão em impressoras conectadas ao host

Marque esta caixa de seleção para permitir que os usuários imprimam a partir do espaço de trabalho do MED-V usando a impressora host.

**Observação**  
A impressão é realizada pelas impressoras definidas no host.



Habilitar o acesso ao CD/DVD

Marque esta caixa de seleção para permitir o acesso a uma unidade de CD ou DVD deste espaço de trabalho do MED-V.



**Várias associações**

1.  Se o usuário fizer parte de um grupo e as permissões forem aplicadas ao usuário e ao grupo do qual elas fazem parte, todas as permissões serão aplicadas.

2.  Se o usuário for membro de dois grupos diferentes, as permissões menos restritivas serão aplicadas.

## Tópicos relacionados


[Usando a interface de usuário do Console de Gerenciamento do MED-V](using-the-med-v-management-console-user-interface.md)

[Criando um espaço de trabalho do MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

[Como definir opções de exclusão de espaços de trabalho do MED-V](how-to-set-med-v-workspace-deletion-options.md)

[Como definir opções avançadas de transferência de arquivos](how-to-set-advanced-file-transfer-options.md)









