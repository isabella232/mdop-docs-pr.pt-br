---
title: Como aplicar configurações de máquina virtual a um espaço de trabalho do MED-V
description: Como aplicar configurações de máquina virtual a um espaço de trabalho do MED-V
author: dansimp
ms.assetid: b50d0dfb-8d61-4543-9607-a29bbb1ed45f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9662bb8202285d51971eeea8beaef938b98ed6b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799779"
---
# Como aplicar configurações de máquina virtual a um espaço de trabalho do MED-V


Todos os espaços de trabalho do MED-V devem ter uma imagem do Microsoft Virtual PC associada a ele. As configurações da máquina virtual permitem atribuir uma imagem do Virtual PC e definir outras propriedades da máquina virtual.

Todas as configurações da máquina virtual são configuradas no módulo de **política** , na guia **configurações de máquina virtual** .

**Para aplicar as configurações da máquina virtual a um espaço de trabalho do MED-V**

1.  Clique no espaço de trabalho do MED-V para configurar.

2.  Configure as propriedades da máquina virtual conforme descrito na tabela a seguir.

3.  No menu **política** , selecione **confirmar**.

**Propriedades da máquina virtual**

Descrição da propriedade *configurações da máquina virtual*

Imagem atribuída

A imagem real do Microsoft Virtual PC atribuída ao espaço de trabalho do MED-V. O menu fornece uma lista de todas as imagens disponíveis do Virtual PC. Os seguintes tipos de imagem estão na lista de imagens **ativas** :

-   **Imagens de teste locais**— imagens no computador local que ainda não foram compactadas. Esses nomes de imagens são seguidos pela palavra "Test" entre parênteses (teste) e só para fins de teste.

-   **Imagens compactadas locais**— imagens compactadas no computador local. Essas imagens são seguidas pela palavra "local" entre parênteses (local) e não podem ser baixadas pelos clientes até que o administrador os carregue para o servidor.

    Uma imagem local pode ser selecionada se você estiver criando um pacote que será distribuído para o cliente via mídia removível (como USB ou DVD).

-   **Imagens compactadas no servidor**— imagens que estão no servidor e estão disponíveis para download por clientes. Clique em atualizar para atualizar a lista imagens.

    **Observação**  Cada imagem do espaço de trabalho do MED-V só pode ser usada por um usuário do Windows.

     

O espaço de trabalho é persistente

Marque esta caixa de seleção para configurar o espaço de trabalho do MED-V como persistente. Em um espaço de trabalho do MED-V persistente, quando o espaço de trabalho do MED-V é interrompido, as alterações e inclusões no espaço de trabalho do MED-v são salvas no espaço de trabalho do MED-v.

Para um espaço de trabalho do MED-V de domínio, essa opção deve ser selecionada.

**Observação**  Essa configuração não deve ser alterada após a implantação de um espaço de trabalho do MED-V para os usuários.

 

Desligar a VM ao interromper o espaço de trabalho

Marque esta caixa de seleção para desligar a máquina virtual ao parar o espaço de trabalho do MED-V. Se essa caixa de seleção estiver desmarcada, na conclusão de cada sessão, a máquina virtual não será desligada, mas, em vez disso, usará um instantâneo da máquina virtual. Durante a inicialização de uma nova sessão, o Windows é iniciado a partir do instantâneo (ou seja, o Windows não é reiniciado e não é necessário fazer logon).

**Observação**  Essa propriedade será habilitada somente se o **espaço de trabalho for persistente** estiver selecionado.

 

Logon no Windows na VM usando credenciais do MED-V (SSO)

Marque esta caixa de seleção para entrar no Windows na máquina virtual usando as credenciais do MED-V inseridas ao fazer logon no cliente MED-V.

**Observação**  Essa propriedade é habilitada somente quando o **espaço de trabalho é persistente** é selecionado.

 

O espaço de trabalho é reversível

Marque esta caixa de seleção para configurar o espaço de trabalho do MED-V como reversível. Em um espaço de trabalho do MED-V reversível, na conclusão de cada sessão (ou seja, quando o usuário pára o espaço de trabalho do MED-V), o espaço de trabalho do MED-V é revertido para o estado original que estava durante a implantação. Nenhuma alteração ou acréscimo feita pelo usuário é salva no espaço de trabalho do MED-V entre as sessões.

**Observação**  Essa configuração não deve ser alterada após a implantação de um espaço de trabalho do MED-V para os usuários.

 

Sincronizar o fuso horário do espaço de trabalho com o host

Marque esta caixa de seleção para sincronizar o fuso horário no espaço de trabalho do MED-V com o host.

A sincronização funciona de forma diferente, dependendo se o espaço de trabalho do MED-V é persistente ou reversível, da seguinte maneira:

-   Em um espaço de trabalho do MED-V persistente, o fuso horário primeiro tenta sincronizar com o servidor. Se isso falhar, ele será sincronizado com o host.

-   Em um espaço de trabalho do MED-V reversível, o fuso horário é sincronizado com o host.

*Configurações de bloqueio*

Bloquear o espaço de trabalho no evento de hibernação/espera do host

Marque esta caixa de seleção para bloquear automaticamente o espaço de trabalho do MED-V quando o computador host entrar no modo de espera ou hibernação.

Bloquear o espaço de trabalho após

Marque esta caixa de seleção para bloquear o espaço de trabalho do MED-V quando o espaço de trabalho do MED-V estiver ocioso por um período de tempo especificado. Quando selecionada, a caixa número está habilitada. Digite o número de minutos de tempo ocioso antes de bloquear o espaço de trabalho do MED-V.

**Observação**  O tempo ocioso refere-se aos aplicativos do espaço de trabalho do MED-V (não aos aplicativos host).

 

*Configurações de atualização de imagem*

Manter somente

Marque esta caixa de seleção para limitar o número de versões de imagem antigas a serem mantidas.

Quando selecionada, a caixa número está habilitada. Digite o número de versões antigas a serem mantidas.

Sugerir atualização quando uma nova versão estiver disponível

Marque esta caixa de seleção para sugerir (mas não forçar) uma atualização quando uma nova versão da imagem estiver disponível.

Os clientes devem usar a transferência de corte ao baixar imagens para este espaço de trabalho

Marque esta caixa de seleção para habilitar a transferência de corte (para obter mais informações, consulte [tecnologia de transferência de corte do MED-V](med-v-trim-transfer-technology-medvv2.md)) ao baixar imagens associadas a este espaço de trabalho do MED-v. Se essa caixa de seleção estiver desmarcada, a imagem inteira será baixada.

**Observação**  A transferência de corte exige o índice da unidade de disco rígido, o que pode demorar um tempo considerável. É recomendável usar a transferência de corte ao indexar o disco rígido é mais eficiente do que baixar a nova versão da imagem, por exemplo, ao baixar uma versão de imagem semelhante à existente.

 

 

## Tópicos relacionados


[Criando uma imagem do MED-V](creating-a-med-v-image.md)

[Usando a interface de usuário do Console de Gerenciamento do MED-V](using-the-med-v-management-console-user-interface.md)

[Criando um espaço de trabalho do MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

 

 





