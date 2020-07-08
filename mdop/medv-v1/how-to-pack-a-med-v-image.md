---
title: Como empacotar uma imagem do MED-V
description: Como empacotar uma imagem do MED-V
author: dansimp
ms.assetid: e1ce2307-0f1b-4bf8-b146-e4012dc138d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a330b8feca922239691bed083767c3acc57105d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799520"
---
# Como empacotar uma imagem do MED-V


Uma imagem do MED-V deve ser empacotada antes de poder ser adicionada a um pacote de implantação ou carregada no servidor.

**Para criar uma imagem do MED-V compactada**

1.  Clique no botão gerenciamento de **imagens** .

2.  No módulo **imagens** , no painel **imagens compactadas locais** , clique em **novo**.

3.  Na caixa de diálogo **criação de imagem empacotada** , selecione a imagem da máquina virtual seguindo um destes procedimentos:

    -   No campo **base do arquivo de imagem** , digite o caminho completo do diretório em que a imagem do Microsoft Virtual PC preparado para o MED-V está localizada.

    -   Clique em **procurar** para navegar até o diretório onde a imagem do Microsoft Virtual PC preparado para o MED-V está localizada.

4.  Especifique o nome da nova imagem seguindo um destes procedimentos:

    -   No campo **nome da imagem** , digite o nome desejado.

        **Observação**  
        Os seguintes caracteres não podem ser incluídos no nome da imagem: espaço " &lt; &gt; | \\ / : \* ?



~~~
    A new packed image will be created.

-   From the drop-down list, select an existing name.

    A new version of the existing image will be created.
~~~

5. Clique em **OK**.

   Uma nova imagem empacotada do MED-V é criada em seu computador host com as propriedades definidas na tabela a seguir.

**Observação**  
Nas **imagens compactadas locais** e **imagens compactadas nos** painéis do servidor, a versão mais recente de cada imagem é exibida como o nó pai. Clique no nó pai para ver todas as outras versões existentes da imagem.



**Propriedades de imagens compactadas locais**

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
<td align="left"><p>O nome da imagem empacotada conforme definido quando o administrador criou a imagem.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versão</p></td>
<td align="left"><p>A versão da imagem exibida.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Todas as versões anteriores são mantidas, a menos que sejam excluídas.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Tamanho do arquivo (compactado)</p></td>
<td align="left"><p>O tamanho compactado físico da imagem.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tamanho da imagem (não compactado)</p></td>
<td align="left"><p>O tamanho físico não compactado da imagem.</p></td>
</tr>
</tbody>
</table>



## Tópicos relacionados


[Como instalar o cliente MED-V e o Console de Gerenciamento do MED-V](how-to-install-med-v-client-and-med-v-management-console.md)

[Usando a interface de usuário do Console de Gerenciamento do MED-V](using-the-med-v-management-console-user-interface.md)

[Criando uma imagem do Virtual PC para o MED-V](creating-a-virtual-pc-image-for-med-v.md)









