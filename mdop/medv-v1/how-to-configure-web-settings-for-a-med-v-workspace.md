---
title: Como definir as configurações da Web de um espaço de trabalho do MED-V
description: Como definir as configurações da Web de um espaço de trabalho do MED-V
author: dansimp
ms.assetid: 9a6cd28f-7e4f-468f-830a-7b1d9abd3af3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 770d3fa9a03c9754db86ca348390d0b916de6d5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799998"
---
# Como definir as configurações da Web de um espaço de trabalho do MED-V


Os sites que só podem ser exibidos em versões mais antigas do Internet Explorer e que não existem no sistema operacional do host podem ser exibidos em versões mais antigas do Internet Explorer dentro do espaço de trabalho do MED-V. O usuário não precisa abrir um navegador no espaço de trabalho do MED-V para exibir os sites da Web especificados. O usuário pode abrir um navegador no host e ser redirecionado automaticamente para o espaço de trabalho do MED-V e vice-versa.

Os procedimentos a seguir descrevem como você pode definir uma lista de regras de navegação na Web para um espaço de trabalho do MED-V. Todos os sites incluídos nas regras podem ser pesquisados no espaço de trabalho do MED-V ou no host, conforme definido pelo administrador. Todos os sites não definidos dentro das regras são acessados a partir do ambiente em que foram solicitados. No entanto, você também pode configurá-los como um grupo, para ser navegado no espaço de trabalho do MED-V ou no host.

**Observação**  
As configurações da Web são aplicadas apenas ao Internet Explorer e a outros navegadores.



Todas as configurações da Web são definidas no módulo de **política** , na guia **Web** .

## Como definir configurações da Web para o espaço de trabalho do MED-V


**Para definir configurações da Web para o espaço de trabalho do MED-V**

1.  Clique no espaço de trabalho do MED-V para ser configurado.

2.  Marque a caixa **de seleção procurar na lista de URLs definidas na tabela a seguir** para redirecionar o usuário para um navegador dentro do espaço de trabalho ou host do MED-V, quando o usuário navegar para uma URL que está em conformidade com as regras da Web especificadas.

3.  Clique em uma das seguintes opções:

    -   **No espaço de trabalho**— Redirecione para um navegador no espaço de trabalho do MED-V.

    -   **No host**— Redirecione para um navegador no host.

4.  Marque a caixa de seleção **procurar todas as outras URLs** para redirecionar todas as URLs excluídas das regras da Web para o host ou o espaço de trabalho do MED-V.

5.  Clique em uma das seguintes opções:

    -   **No espaço de trabalho**, redirecione todas as outras URLs para um navegador no espaço de trabalho do MED-V.

    -   **No host**— redirecione todas as outras URLs para um navegador no host.

6.  No menu **política** , selecione **confirmar**.

## Como adicionar uma regra da Web


**Para adicionar uma regra da Web**

1.  Marque a caixa **de seleção procurar na lista de URLs definida na tabela a seguir** para habilitar as regras de navegação na Web.

2.  Clique em **Adicionar**.

    Uma nova regra da Web é adicionada.

3.  Configure as propriedades da regra da Web conforme descrito na tabela a seguir.

4.  No menu **política** , selecione **confirmar**.

**Propriedades da Web do espaço de trabalho do MED-V**

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
<td align="left"><p>Tipo</p></td>
<td align="left"><ul>
<li><p><strong>Sufixo do domínio </strong> – o acesso a qualquer endereço de host que termina com o sufixo especificado na <strong> </strong> propriedade valor e é definido de acordo com a opção definida na <strong> navegação na Web </strong> .</p></li>
<li><p><strong>Prefixo </strong> de IP – acesso a qualquer endereço IP completo ou parcial no intervalo do prefixo especificado na <strong> </strong> propriedade valor e é definido de acordo com a opção definida na navegação na <strong> Web </strong> .</p></li>
<li><p><strong>Todos os endereços locais </strong> – acesso a todos os endereços sem um &#39;. &#39; e é definido de acordo com a opção definida na <strong> navegação na Web </strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Valor</p></td>
<td align="left"><ul>
<li><p>Se <strong> sufixo </strong> do domínio for selecionado na <strong> </strong> propriedade tipo, insira um sufixo de domínio.</p>
<div class="alert">
<strong>Observação</strong><br/><ul>
<li><p>Não insira &quot; * &quot; antes do sufixo.</p></li>
<li><p>Sufixos de domínio também dão suporte a aliases.</p></li>
</ul>
</div>
<div>

</div></li>
<li><p>Se prefixo IP estiver selecionado na <strong> propriedade tipo </strong> , insira um endereço IP completo ou parcial.</p></li>
</ul></td>
</tr>
</tbody>
</table>



## Como excluir uma regra da Web


**Para excluir uma regra da Web**

1.  No painel **da Web** , selecione a regra da Web a ser excluída.

2.  Clique em **remover**.

    A regra da Web é excluída.

## Tópicos relacionados


[Usando a interface de usuário do Console de Gerenciamento do MED-V](using-the-med-v-management-console-user-interface.md)

[Criando um espaço de trabalho do MED-V](creating-a-med-v-workspacemedv-10-sp1.md)









