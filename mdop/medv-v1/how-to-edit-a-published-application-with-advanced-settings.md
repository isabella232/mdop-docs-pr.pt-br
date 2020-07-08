---
title: Como editar um aplicativo publicado com configurações avançadas
description: Como editar um aplicativo publicado com configurações avançadas
author: dansimp
ms.assetid: 06a79049-9ce9-490f-aad7-fd4fdf185590
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 843aebb38f54959f209e742b398e3979acac3334
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799984"
---
# Como editar um aplicativo publicado com configurações avançadas


Após a adição e a configuração de um aplicativo publicado, o aplicativo publicado pode ser editado e configurações avançadas adicionais podem ser configuradas.

**Para editar um aplicativo publicado com configurações avançadas**

1.  No painel **aplicativos** , adicione e configure um aplicativo publicado.

2.  Selecione o aplicativo publicado a ser editado.

3.  Clique em **Editar**.

4.  Na caixa de diálogo **aplicativo publicado** , configure os parâmetros conforme descrito na tabela a seguir.

5.  Clique em **OK**.

6.  No menu **política** , selecione **confirmar**.

**Editando propriedades do aplicativo publicado**

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
<td align="left"><p>Nome de exibição</p></td>
<td align="left"><p>O nome do atalho no menu Iniciar do usuário&#39;s do Windows.</p>
<div class="alert">
<strong>Observação</strong><br/><p>O nome para exibição <strong> não diferencia </strong> maiúsculas de minúsculas.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Descrição</p></td>
<td align="left"><p>Uma descrição do menu publicado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Iniciar em</p></td>
<td align="left"><p>O diretório a partir do qual o aplicativo será iniciado.</p>
<div class="alert">
<strong>Observação</strong><br/><p>O caminho não precisa incluir aspas.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Linha de comando</p></td>
<td align="left"><p>O comando com o qual executar o aplicativo no espaço de trabalho do MED-V.</p>
<p>O caminho completo é necessário, e os parâmetros podem ser passados para o aplicativo de maneira semelhante, como em qualquer outro comando do Windows.</p>
<p>Em uma configuração de domínio, geralmente existe uma unidade compartilhada no servidor em que todos os computadores do domínio mapeiam. O diretório deve ser mapeado aqui e, se for uma pasta que exija autenticação do usuário, a <strong> caixa de seleção usar credenciais do MED-V para executar este aplicativo </strong> deve estar marcada.</p>
<p>Em um espaço de trabalho do MED-V reversível, você pode mapear uma unidade de rede com a sintaxe MapNetworkDrive: &quot; <em> &lt; &gt; &lt; caminho da unidade MapNetworkDrive &gt; </em> &quot; , por exemplo, &quot; <em> MapNetworkDrive t: \tux\data </em> &quot; .</p>
<p>Por exemplo, para publicar o Windows Explorer, use a seguinte sintaxe: &quot; <em> c: &amp; quot; ou &quot; c:\Windows </em> &quot; .</p>
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
<td align="left"><p>Adicionar um atalho no menu Iniciar do Windows host</p></td>
<td align="left"><p>Marque esta caixa de seleção para criar um atalho para o aplicativo no menu Iniciar do usuário&#39;s do Windows.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Iniciar este aplicativo quando o espaço de trabalho for iniciado</p></td>
<td align="left"><p>Marque esta caixa de seleção para executar o aplicativo automaticamente quando o espaço de trabalho do MED-V for iniciado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usar credenciais do MED-V para executar este aplicativo</p></td>
<td align="left"><p>Marque esta caixa de seleção para autenticar aplicativos que solicitam um nome de usuário e senha usando as credenciais do MED-V em vez das credenciais definidas para o aplicativo.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Ao usar o SSO, a linha de comando deve ser <strong>C:\Windows\Explorer.exe &quot; caminho da pasta &quot; </strong> . Quando não estiver usando o SSO, a linha de comando deve ser o &quot; <strong> caminho da pasta </strong> &quot; .</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Tópicos relacionados


[Como configurar aplicativos publicados](how-to-configure-published-applicationsmedvv2.md)









