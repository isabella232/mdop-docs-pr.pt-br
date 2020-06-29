---
title: Como definir a identidade visual e o tempo limite de sessão do Portal de Autoatendimento
description: Como definir a identidade visual e o tempo limite de sessão do Portal de Autoatendimento
author: dansimp
ms.assetid: 031eedfc-fade-4d2f-8771-b329e1d38c0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e222880b2d5557ef15cd7a4efd6421b9972541f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796023"
---
# Como definir a identidade visual e o tempo limite de sessão do Portal de Autoatendimento


Depois de configurar o portal de autoatendimento, você pode marcar o nome da sua empresa, a URL do suporte técnico e o texto "aviso". Você também pode alterar a configuração de tempo limite de sessão para fazer com que a sessão do usuário final expire após um período de inatividade especificado.

**Observação**  
Você também pode marcar o portal de autoatendimento usando o cmdlet **Enable-MbamWebApplication** do Windows PowerShell ou o assistente de configuração do servidor do MBAM. Para obter instruções sobre como usar o assistente, confira [como configurar os aplicativos Web do MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).



**Observação**  
Nas instruções a seguir, *SelfService* é o nome do diretório virtual padrão do portal de autoatendimento. Você pode ter usado um nome diferente ao configurar o portal de autoatendimento.



**Para definir o tempo limite da sessão e a identidade visual do portal de autoatendimento**

1.  Para definir o período de tempo limite da sessão do usuário final, inicie o **Gerenciador dos serviços de informações da Internet**ou execute **inetmgr.exe**.

2.  Navegue até **sites** &gt; **Administração e monitoramento do Microsoft BitLocker** &gt; **SelfService** &gt; **ASP.net** &gt; **estado de sessão**e altere o valor de **tempo limite** em **configurações de cookie** para o número de minutos após o qual a sessão do portal de autoatendimento do usuário final expira. O valor padrão é **5**. Para desabilitar a configuração de modo que não haja tempo limite, defina o valor como **0**.

3.  Para definir os itens de identidade visual do portal de autoatendimento, inicie o **Gerenciador dos serviços de informações da Internet** ou execute **inetmgr.exe**.

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
<th align="left">Default value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ClientValidationEnabled</p></td>
<td align="left"><p>true</p></td>
</tr>
<tr class="even">
<td align="left"><p>CompanyName</p></td>
<td align="left"><p>Contoso IT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DisplayNotice</p></td>
<td align="left"><p>true</p></td>
</tr>
<tr class="even">
<td align="left"><p>HelpdeskText</p></td>
<td align="left"><p>Contact Helpdesk or IT Department</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HelpdeskUrl</p></td>
<td align="left"><p>#</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, the HelpdeskUrl default value is empty.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>jQueryPath</p></td>
<td align="left"><p>[//go.microsoft.com/fwlink/?LinkID=390515](//go.microsoft.com/fwlink/?LinkID=390515)</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, this has been changed to a local JavaScript file shipped with the product, located at ~/Scripts/jquery-1.10.2.min.js</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>jQueryValidatePath</p></td>
<td align="left"><p>[//go.microsoft.com/fwlink/?LinkID=390516](//go.microsoft.com/fwlink/?LinkID=390516)</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, this has been changed to a local JavaScript file shipped with the product, located at ~/Scripts/jquery.validate.min.js</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>jQueryValidateUnobtrusivePath</p></td>
<td align="left"><p>[//go.microsoft.com/fwlink/?LinkID=390517](//go.microsoft.com/fwlink/?LinkID=390517)</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, this has been changed to a local JavaScript file shipped with the product, located at ~/Scripts/jquery.validate.unobtrusive.min.js</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>NoticeTextPath</p></td>
<td align="left"><p>Notice.txt</p>
<div class="alert">
<strong>Note</strong>  
<p>You can edit the notice text either by using the Internet Information Services (IIS) Manager or by opening and changing the Notice.txt file in the installation directory.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>UnobtrusiveJavaScriptEnabled</p></td>
<td align="left"><p>true</p></td>
</tr>
</tbody>
</table>
~~~





## Tópicos relacionados


[Personalizando o Portal de Autoatendimento para sua organização](customizing-the-self-service-portal-for-your-organization.md)



## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





