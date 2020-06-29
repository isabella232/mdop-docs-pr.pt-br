---
title: Como definir a marca do Portal de Autoatendimento
description: Como definir a marca do Portal de Autoatendimento
author: dansimp
ms.assetid: 3ef9e951-7c42-4f7f-b131-3765d39b3207
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe4f4efc5852042671711ba5780cc78055957ba8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799614"
---
# Como definir a marca do Portal de Autoatendimento


Depois de instalar o portal de autoatendimento do Microsoft BitLocker Administration and Monitoring (MBAM), você pode marcar o portal de autoatendimento com o nome da sua empresa, a URL do suporte técnico e o texto "aviso". Você também pode alterar a configuração de tempo limite da sessão para fazer com que a sessão do usuário final expire após um período de inatividade especificado.

**Para definir o tempo limite da sessão e a identidade visual do portal de autoatendimento**

1.  Para definir o período de tempo limite da sessão do usuário final, inicie o **Gerenciador dos serviços de informações da Internet**ou execute **inetmgr.exe**.

2.  Navegue até **sites** &gt; **Administração e monitoramento do Microsoft BitLocker** &gt; **SelfService** &gt; **ASP.net** &gt; **estado de sessão**e altere o valor de **tempo limite** em **configurações de cookie** para o número de minutos após o qual a sessão do portal de autoatendimento do usuário final vencerá. O padrão é 5. Para desabilitar a configuração de modo que não haja tempo limite, defina o valor como **0**.

3.  Para definir os itens de identidade visual para o portal de autoatendimento, inicie o **Gerenciador dos serviços de informações da Internet**ou execute **inetmgr.exe**.

4.  Navegue até **sites** &gt; **Administração e monitoramento do Microsoft BitLocker** &gt; **SelfService** &gt; **configurações do aplicativo**.

5.  Na coluna **nome** , selecione o item que você deseja alterar e altere o valor padrão para refletir o nome que você deseja usar. A tabela a seguir lista os valores que você pode definir.

    **Tenha**  
    Não altere o valor na coluna Name (CompanyName \ *), pois isso fará com que o portal de autoatendimento pare de funcionar.



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Default Value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CompanyName*</p></td>
<td align="left"><p>Contoso IT</p></td>
</tr>
<tr class="even">
<td align="left"><p>HelpdeskText*</p></td>
<td align="left"><p>Contact Help Desk or IT Department</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HelpdeskUrl*</p></td>
<td align="left"><p>Http://www.microsoft.com</p></td>
</tr>
<tr class="even">
<td align="left"><p>jQueryPath</p></td>
<td align="left"><p>//ajax.aspnetcdn.com/ajax/jQuery/jquery-1.7.2.min.js</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MicrosoftAjaxPath</p></td>
<td align="left"><p>//ajax.aspnetcdn.com/ajax/3.5/MicrosoftAjax.js</p></td>
</tr>
<tr class="even">
<td align="left"><p>MicrosoftMvcAjaxPath</p></td>
<td align="left"><p>//ajax.aspnetcdn.com/ajax/mvc/2.0/MicrosoftMvcValidation.js</p></td>
</tr>
<tr class="odd">
<td align="left"><p>NoticeTextPath</p></td>
<td align="left"><p>Notice.txt</p>
<div class="alert">
<strong>Note</strong>  
<p>You can edit the Notice text either by using the IIS Manager or by opening and changing the Notice.txt file in the installation directory.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>
~~~



## Tópicos relacionados


[Implantação da infraestrutura de servidor do MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









