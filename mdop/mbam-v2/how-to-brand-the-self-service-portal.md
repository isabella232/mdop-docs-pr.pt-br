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
# <span data-ttu-id="54036-103">Como definir a marca do Portal de Autoatendimento</span><span class="sxs-lookup"><span data-stu-id="54036-103">How to Brand the Self-Service Portal</span></span>


<span data-ttu-id="54036-104">Depois de instalar o portal de autoatendimento do Microsoft BitLocker Administration and Monitoring (MBAM), você pode marcar o portal de autoatendimento com o nome da sua empresa, a URL do suporte técnico e o texto "aviso".</span><span class="sxs-lookup"><span data-stu-id="54036-104">After you install the Microsoft BitLocker Administration and Monitoring (MBAM) Self-Service Portal, you can brand the Self-Service Portal with your company name, Help Desk URL, and “notice” text.</span></span> <span data-ttu-id="54036-105">Você também pode alterar a configuração de tempo limite da sessão para fazer com que a sessão do usuário final expire após um período de inatividade especificado.</span><span class="sxs-lookup"><span data-stu-id="54036-105">You can also change the Session Timeout setting to make the end user’s session expire after a specified period of inactivity.</span></span>

**<span data-ttu-id="54036-106">Para definir o tempo limite da sessão e a identidade visual do portal de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="54036-106">To set the session time-out and branding for the Self-Service Portal</span></span>**

1.  <span data-ttu-id="54036-107">Para definir o período de tempo limite da sessão do usuário final, inicie o **Gerenciador dos serviços de informações da Internet**ou execute **inetmgr.exe**.</span><span class="sxs-lookup"><span data-stu-id="54036-107">To set the time-out period for the end user’s session, start the **Internet Information Services Manager**, or run **inetmgr.exe**.</span></span>

2.  <span data-ttu-id="54036-108">Navegue até **sites** &gt; **Administração e monitoramento do Microsoft BitLocker** &gt; **SelfService** &gt; **ASP.net** &gt; **estado de sessão**e altere o valor de **tempo limite** em **configurações de cookie** para o número de minutos após o qual a sessão do portal de autoatendimento do usuário final vencerá.</span><span class="sxs-lookup"><span data-stu-id="54036-108">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **ASP.NET** &gt; **Session State**, and change the **Time-out** value under **Cookie Settings** to the number of minutes after which the end user’s Self-Service Portal session will expire.</span></span> <span data-ttu-id="54036-109">O padrão é 5.</span><span class="sxs-lookup"><span data-stu-id="54036-109">The default is 5.</span></span> <span data-ttu-id="54036-110">Para desabilitar a configuração de modo que não haja tempo limite, defina o valor como **0**.</span><span class="sxs-lookup"><span data-stu-id="54036-110">To disable the setting so that there is no time-out, set the value to **0**.</span></span>

3.  <span data-ttu-id="54036-111">Para definir os itens de identidade visual para o portal de autoatendimento, inicie o **Gerenciador dos serviços de informações da Internet**ou execute **inetmgr.exe**.</span><span class="sxs-lookup"><span data-stu-id="54036-111">To set the branding items for the Self-Service Portal, start the **Internet Information Services Manager**, or run **inetmgr.exe**.</span></span>

4.  <span data-ttu-id="54036-112">Navegue até **sites** &gt; **Administração e monitoramento do Microsoft BitLocker** &gt; **SelfService** &gt; **configurações do aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="54036-112">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

5.  <span data-ttu-id="54036-113">Na coluna **nome** , selecione o item que você deseja alterar e altere o valor padrão para refletir o nome que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="54036-113">From the **Name** column, select the item that you want to change, and change the default value to reflect the name that you want to use.</span></span> <span data-ttu-id="54036-114">A tabela a seguir lista os valores que você pode definir.</span><span class="sxs-lookup"><span data-stu-id="54036-114">The following table lists the values that you can set.</span></span>

    **<span data-ttu-id="54036-115">Tenha</span><span class="sxs-lookup"><span data-stu-id="54036-115">Caution</span></span>**  
    <span data-ttu-id="54036-116">Não altere o valor na coluna Name (CompanyName \ \*), pois isso fará com que o portal de autoatendimento pare de funcionar.</span><span class="sxs-lookup"><span data-stu-id="54036-116">Do not change the value in the Name column (CompanyName\*), as it will cause the Self-Service Portal to stop working.</span></span>



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



## <span data-ttu-id="54036-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="54036-117">Related topics</span></span>


[<span data-ttu-id="54036-118">Implantação da infraestrutura de servidor do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="54036-118">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









