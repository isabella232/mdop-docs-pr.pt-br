---
title: Como criar e testar uma imagem do MED-V
description: Como criar e testar uma imagem do MED-V
author: dansimp
ms.assetid: 40e4aba6-12cb-4794-967d-2c09dc20d808
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f7989871a695b09c987124ab02c0143082148f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799993"
---
# Como criar e testar uma imagem do MED-V


O administrador do MED-V cria uma imagem do MED-V para que possa ser carregada, associada a um espaço de trabalho do MED-V e, em seguida, distribuída para o cliente pela Web, adicionada a um pacote do MED-V ou baixada para o cliente usando um sistema de terceiros. É recomendável primeiro criar uma imagem de teste e testá-la no cliente MED-V antes de implantá-la.

Ao criar uma imagem do MED-V, ela passa pelos seguintes estágios:

1.  **Imagem de teste local**— uma imagem básica que pode ser testada localmente.

2.  **Imagem empacotada local**– após a imagem ser testada, a imagem é compactada como era antes do teste. Nenhuma alteração feita durante o teste está incluída na imagem empacotada.

3.  **Imagem empacotada no servidor**— a imagem empacotada é carregada no servidor.

## Como criar uma imagem de teste do MED-V


**Para criar uma nova imagem de teste do MED-V**

1.  Clique no botão gerenciamento de **imagens** .

    O módulo **imagens** é exibido.

    -   O módulo **imagens** consiste nos seguintes painéis:

        -   **Imagens de teste locais**— imagens descompactadas locais.

        -   **Imagens compactadas locais**– todas as imagens compactadas no computador local.

        -   **Imagens compactadas no servidor**— todas as imagens que foram empacotadas e carregadas no servidor.

    -   Nas **imagens compactadas locais** e **imagens compactadas nos** painéis do servidor, a versão mais recente de cada imagem é exibida como o nó pai. Clique no nó pai para ver todas as outras versões existentes da imagem.

2.  No painel **imagens de teste locais** , clique em **novo**.

3.  Na caixa de diálogo **testar criação de imagem** , selecione a imagem da máquina virtual que você deseja configurar como uma imagem de teste do MED-V seguindo um destes procedimentos:

    -   No campo **base** do arquivo de imagem, digite o caminho completo do diretório em que a imagem do Microsoft Virtual PC preparado para o MED-V está localizada.

    -   Clique em **procurar** para navegar até o diretório onde a imagem do Microsoft Virtual PC preparado para o MED-V está localizada.

4.  No campo **nome da imagem** , digite ou selecione o nome desejado.

    **Observação**  Os seguintes caracteres não podem ser incluídos no nome da imagem: espaço " &lt; &gt; | \\ / : \* ?

     

5.  Clique em **OK**.

    Uma nova imagem de teste do MED-V é criada no computador host com as propriedades definidas na tabela a seguir.

    Para obter mais informações sobre como configurar a imagem do espaço de trabalho do MED-V, consulte [Configurando políticas do espaço de trabalho do MED-v](configuring-med-v-workspace-policies.md).

**Propriedades de imagens de teste locais**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriedade</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nome da imagem</p></td>
<td align="left"><p>O nome da imagem de teste conforme definido quando o administrador criou a imagem.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Caminho da imagem</p></td>
<td align="left"><p>O caminho local da imagem de teste.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Criado</p></td>
<td align="left"><p>A data em que a imagem de teste foi criada.</p></td>
</tr>
</tbody>
</table>

 

## Como testar uma imagem do MED-V do cliente MED-V


Após a criação de uma imagem de teste do MED-V, use o procedimento a seguir para testar a imagem localmente.

**Para testar uma imagem do MED-V**

1.  Clique no botão gerenciamento de **políticas** .

2.  No módulo de **política** , atribua a imagem de teste do MED-v a um espaço de trabalho do MED-v fazendo o seguinte:

    1.  Clique na guia **máquina virtual** .

    2.  No campo de **imagem atribuído** , selecione a imagem de teste do MED-V que você criou. Se a sua imagem de teste não estiver na lista, clique em **Atualizar**.

    3.  Na barra de ferramentas, clique em **salvar alterações**.

3.  Configure qualquer outra configuração de espaço de trabalho do MED-V para ser testada. Para obter mais informações, consulte [Configurando políticas do espaço de trabalho do MED-V](configuring-med-v-workspace-policies.md).

4.  Inicie o cliente MED-V.

5.  Na caixa de confirmação **confirmar teste em execução** , clique em **usar imagem de teste**.

6.  Testar a imagem de teste do espaço de trabalho do MED-V.

    Para obter informações sobre como iniciar e executar o cliente MED-V, consulte [operações do cliente med-v](med-v-client-operations.md).

**Observação**  Ao testar uma imagem, não abra o VPC e faça alterações na imagem.

 

**Observação**  Ao testar uma imagem, nenhuma alteração é salva na imagem entre as sessões; em vez disso, eles são salvos em um arquivo separado temporário. Isso é para garantir que, quando a imagem é empacotada e executada no ambiente de produção, seja a imagem original e limpa.

 

## Tópicos relacionados


[Criando uma imagem do Virtual PC para o MED-V](creating-a-virtual-pc-image-for-med-v.md)

[Criando um espaço de trabalho do MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

[Configurando políticas de espaço de trabalho do MED-V](configuring-med-v-workspace-policies.md)

[Operações do cliente MED-V](med-v-client-operations.md)

 

 





