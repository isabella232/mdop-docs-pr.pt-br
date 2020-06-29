---
title: Como configurar as propriedades de padrão de nomes do computador VM
description: Como configurar as propriedades de padrão de nomes do computador VM
author: dansimp
ms.assetid: ddf79ace-8cc3-4ee6-be5a-5940b4df5c36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa171712b6624b73fb5e0756aaf56277baa4c8cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800000"
---
# Como configurar as propriedades de padrão de nomes do computador VM


Um padrão de nome de computador de máquina virtual pode ser atribuído para os espaços de trabalho reversível e para os espaços de trabalho do MED-V persistentes.

-   Reversível — os administradores podem atribuir um nome exclusivo a cada instância reversível do espaço de trabalho do MED-V para diferenciar entre vários computadores usando o mesmo espaço de trabalho do MED-V.

-   Persistente – em um espaço de trabalho do MED-V persistente, os administradores podem definir um computador para ser renomeado durante um script de instalação.

## Como atribuir um padrão de nome de computador de máquina virtual a um espaço de trabalho do MED-V reversível


**Para atribuir um padrão de nome de computador de máquina virtual a um espaço de trabalho do MED-V reversível**

1.  Clique no espaço de trabalho do MED-V reversível para configurar.

2.  Na seção **configuração de VM reversível** , marque a caixa de seleção **renomear a VM com base no padrão de nome do computador** .

3.  Na seção **máquina de nome do computador VM** , digite o padrão a ser usado para nomear imagens da máquina virtual, usando as seguintes opções:

    -   **Constante**— Insira um texto livre que será constante em todos os computadores usando o espaço de trabalho do MED-V.

    -   **Variável**— Insira uma variável clicando em **Inserir variável**e selecione uma das seguintes opções:

        -   **Nome de usuário**

        -   **Nome do domínio**

        -   **Nome do host**

        -   **Nome do espaço de trabalho**

        -   **Nome da máquina virtual**

        A variável selecionada será específica do computador usando o espaço de trabalho do MED-V. Por exemplo, se o **nome do domínio** for selecionado, o nome exclusivo de cada computador incluirá o nome de domínio do computador.

    -   **Caracteres aleatórios**— insira "\ #" para cada caractere aleatório a ser incluído no padrão. Cada computador que usa o espaço de trabalho do MED-V terá um sufixo do comprimento especificado, que é gerado aleatoriamente.

    **Observação**  
    O nome do computador tem um limite de 15 caracteres. Se o padrão exceder o limite, ele será truncado.



4.  No menu **política** , selecione **confirmar**.

    **Observação**  
    Um padrão de nome de computador VM reversível pode ser atribuído somente quando você **renomeia a VM com base nos padrões de nome de computador** (na seção **configuração de VM reversível** ) está marcada.



~~~
**Note**  
A unique computer name can be assigned only if it is configured prior to MED-V workspace setup. Changing the name will not affect MED-V workspaces that were already set up.
~~~



## Como atribuir um padrão de nome de computador virtual a um espaço de trabalho do MED-V persistente


**Para atribuir um padrão de nome de computador de máquina virtual a um espaço de trabalho do MED-V persistente**

1.  Clique no espaço de trabalho persistente do MED-V para configurar.

2.  Na seção **configuração de VM persistente** , clique em **Editor de script**.

3.  Na caixa de diálogo **ações de script** , clique em **Adicionar**e, no submenu, clique em **renomear computador**.

4.  Clique em **OK** para fechar a caixa de diálogo **ações de script** .

5.  Na guia **configuração da VM** , na seção **padrão de nome do computador VM** , digite o padrão a ser usado para renomear o computador, usando o seguinte:

    -   **Constante**— Insira um texto livre que será incluído no nome do computador.

    -   **Variável**— Insira uma variável clicando em **Inserir variável**e selecione uma das seguintes opções:

        -   **Nome de usuário**

        -   **Nome do domínio**

        -   **Nome do host**

        -   **Nome do espaço de trabalho**

        -   **Nome da máquina virtual**

        A variável selecionada será específica para o computador que está sendo renomeado. Por exemplo, se o **nome do domínio** estiver selecionado, o nome do computador incluirá o nome de domínio do computador.

    -   **Caracteres aleatórios**— insira "\ #" para cada caractere aleatório a ser incluído no padrão. O computador terá um sufixo do comprimento especificado, que é gerado aleatoriamente.

    **Observação**  
    O nome do computador tem um limite de 15 caracteres. Se o padrão exceder o limite, ele será truncado.



6.  No menu **política** , selecione **confirmar**.

    **Observação**  
    O computador será renomeado somente se for definido como uma ação na caixa de diálogo **ações de script** . Para obter informações detalhadas, consulte [como configurar ações de script](how-to-set-up-script-actions.md).



## Tópicos relacionados


[Usando a interface de usuário do Console de Gerenciamento do MED-V](using-the-med-v-management-console-user-interface.md)

[Criando um espaço de trabalho do MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

[Como configurar ações de script](how-to-set-up-script-actions.md)

[Exemplos de configurações de máquina virtual](examples-of-virtual-machine-configurationsv2.md)









