---
title: Como configurar aplicativos publicados
description: Como configurar aplicativos publicados
author: dansimp
ms.assetid: 43a59ff7-5d4e-49dc-84e5-1082bc4dd8f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cb5736382f03e818ef10aa814a8e61044ca2b73a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799447"
---
# Como configurar aplicativos publicados


Os aplicativos que não são compatíveis com o sistema operacional do host podem ser executados dentro do espaço de trabalho do MED-V e iniciados a partir do espaço de trabalho do MED-V da mesma forma que são iniciados a partir da área de trabalho, a partir do menu iniciar ou de um atalho de host local. Os aplicativos selecionados e definidos são chamados de aplicativos publicados. Os procedimentos desta seção descrevem como adicionar e remover aplicativos publicados.

Um aplicativo pode ser publicado de uma das seguintes maneiras:

-   Como um aplicativo — selecione um aplicativo específico digitando na linha de comando para o aplicativo. Somente o aplicativo selecionado é publicado.

-   Como um menu — selecione uma pasta que contenha vários aplicativos. Todos os aplicativos da pasta são publicados e exibidos como um menu.

## <a href="" id="bkmk-addingapublishedapplication"></a>Como adicionar um aplicativo publicado a um espaço de trabalho do MED-V


**Para adicionar um aplicativo ao espaço de trabalho do MED-V**

1.  Clique no espaço de trabalho do MED-V para configurar.

2.  No painel **aplicativos** , na seção **aplicativos publicados** , clique em **Adicionar** para adicionar um novo aplicativo.

3.  Configure as propriedades do aplicativo conforme descrito na tabela a seguir.

4.  No menu **política** , selecione **confirmar**.

    **Observação**  
    Se você estiver definindo o Internet Explorer como um aplicativo publicado para garantir que o redirecionamento da Web funcione corretamente, certifique-se de que todos os parâmetros não estejam entre parênteses.



**Propriedades do aplicativo publicado**

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
<td align="left"><p>Habilitado</p></td>
<td align="left"><p>Marque esta caixa de seleção para habilitar o aplicativo publicado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome de exibição</p></td>
<td align="left"><p>O nome do atalho no menu Iniciar do usuário&#39;s do Windows.</p>
<div class="alert">
<strong>Observação</strong><br/><p>O nome para exibição <strong> não diferencia </strong> maiúsculas de minúsculas.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Descrição</p></td>
<td align="left"><p>Uma descrição do aplicativo publicado, que aparece como uma dica de ferramenta quando o usuário&#39;s passa o mouse sobre o atalho.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Linha de comando</p></td>
<td align="left"><p>O comando usado para executar o aplicativo no espaço de trabalho do MED-V. O caminho completo é necessário, e os parâmetros podem ser passados para o aplicativo de maneira semelhante, como em qualquer outro comando do Windows.</p>
<p>Em um espaço de trabalho do MED-V reversível, você pode mapear uma unidade de rede com a sintaxe MapNetworkDrive: &quot; <em> &lt; &gt; &lt; caminho da unidade MapNetworkDrive &gt; </em> &quot; , por exemplo, &quot; <em> MapNetworkDrive t: \tux\date </em> &quot; .</p>
<p>Por exemplo, para publicar o Windows Explorer, use a seguinte sintaxe: &quot; <em> c: &lt; /em &gt; &quot; ou &quot; <em> c:\Windows </em> .&quot;</p>
<div class="alert">
<strong>Observação</strong><br/><p>Para ter uma resolução de nomes, você precisa executar um dos seguintes procedimentos:</p>
</div>
<div>

</div>
<ul>
<li><p>Configurar o DNS na imagem base do espaço de trabalho do MED-V base.</p></li>
<li><p>Verifique se a resolução DNS está definida no host e configure-a para usar o DNS do host.</p></li>
<li><p>Use o IP para definir a unidade de rede.</p></li>
</ul>
<div class="alert">
<strong>Observação</strong><br/><p>Se o caminho incluir espaços, o caminho inteiro deve estar entre aspas.</p>
</div>
<div>

</div>
<div class="alert">
<strong>Observação</strong><br/><p>O caminho não deve terminar com uma barra invertida ().</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Menu Iniciar</p></td>
<td align="left"><p>Marque esta caixa de seleção para criar um atalho para o aplicativo no menu Iniciar do usuário&#39;s do Windows.</p></td>
</tr>
</tbody>
</table>



Todos os aplicativos publicados aparecem como atalhos no menu **Iniciar** do Windows (**Iniciar &gt; todos os programas do &gt; MED-V para aplicativos**).

## Como remover um aplicativo publicado de um espaço de trabalho do MED-V


**Para remover um aplicativo do espaço de trabalho do MED-V**

1.  Clique em um espaço de trabalho do MED-V.

2.  No painel **aplicativos** , na seção **aplicativos publicados** , selecione um aplicativo para remover.

3.  Clique em **remover**.

    O aplicativo é removido da lista de aplicativos publicados.

4.  No menu **política** , selecione **confirmar**.

## Como adicionar um menu publicado a um espaço de trabalho do MED-V


**Para adicionar um menu publicado ao espaço de trabalho do MED-V**

1.  Clique no espaço de trabalho do MED-V para configurar.

2.  No painel **aplicativos** , na seção **menus publicados** , clique em **Adicionar** para adicionar um novo menu.

3.  Configure as propriedades do menu conforme descrito na tabela a seguir.

4.  No menu **política** , selecione **confirmar**.

**Propriedades do menu publicado**

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
<td align="left"><p>Habilitado</p></td>
<td align="left"><p>Marque esta caixa de seleção para habilitar o menu publicado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome de exibição</p></td>
<td align="left"><p>O nome do atalho no menu Iniciar do usuário&#39;s do Windows.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Descrição</p></td>
<td align="left"><p>A descrição, que aparece como uma dica de ferramenta quando o usuário&#39;s passa o mouse sobre o atalho.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Pasta no espaço de trabalho</p></td>
<td align="left"><p>Selecione a pasta a ser publicada como um menu que contém todos os aplicativos dentro dela.</p>
<p>O texto exibido é um caminho relativo da pasta programas.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Se deixado em branco, todos os programas no host serão publicados como um menu.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



Todos os menus publicados aparecem como atalhos no menu **Iniciar** do Windows (**Iniciar &gt; todos os programas do &gt; MED-V para aplicativos**). Você pode alterar o nome do atalho no campo **pasta de atalhos do menu iniciar** .

**Observação**  
Ao configurar dois espaços de trabalho do MED-V, é recomendável configurar um nome diferente para a pasta atalhos do menu iniciar.



## Como remover um menu publicado de um espaço de trabalho do MED-V


**Para remover um menu publicado de um espaço de trabalho do MED-V**

1.  Clique em um espaço de trabalho do MED-V.

2.  No painel **aplicativos** , na seção **menus publicados** , selecione um menu a ser removido.

3.  Clique em **remover**.

    O menu é removido da lista de menus publicados.

4.  No menu **política** , selecione **confirmar**.

## Executar um aplicativo publicado a partir de uma linha de comando no cliente


O administrador pode executar aplicativos publicados de qualquer local, como um atalho da área de trabalho, usando o seguinte comando:

``` syntax
"<Install path>\Manager\KidaroCommands.exe" /run "<published application name>" "<MED-V workspace name>"
```

**Observação**  
O espaço de trabalho do MED-V no qual o aplicativo publicado está definido deve estar em execução.



## Tópicos relacionados


[Como editar um aplicativo publicado com configurações avançadas](how-to-edit-a-published-application-with-advanced-settings.md)

[Usando a interface de usuário do Console de Gerenciamento do MED-V](using-the-med-v-management-console-user-interface.md)

[Criando um espaço de trabalho do MED-V](creating-a-med-v-workspacemedv-10-sp1.md)









