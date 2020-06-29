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
# <span data-ttu-id="53031-103">Como definir a identidade visual e o tempo limite de sessão do Portal de Autoatendimento</span><span class="sxs-lookup"><span data-stu-id="53031-103">How to Set the Self-Service Portal Branding and Session Time-out</span></span>


<span data-ttu-id="53031-104">Depois de configurar o portal de autoatendimento, você pode marcar o nome da sua empresa, a URL do suporte técnico e o texto "aviso".</span><span class="sxs-lookup"><span data-stu-id="53031-104">After you configure the Self-Service Portal, you can brand it with your company name, Help Desk URL, and "notice" text.</span></span> <span data-ttu-id="53031-105">Você também pode alterar a configuração de tempo limite de sessão para fazer com que a sessão do usuário final expire após um período de inatividade especificado.</span><span class="sxs-lookup"><span data-stu-id="53031-105">You can also change the Session Time-out setting to make the end user’s session expire after a specified period of inactivity.</span></span>

**<span data-ttu-id="53031-106">Observação</span><span class="sxs-lookup"><span data-stu-id="53031-106">Note</span></span>**  
<span data-ttu-id="53031-107">Você também pode marcar o portal de autoatendimento usando o cmdlet **Enable-MbamWebApplication** do Windows PowerShell ou o assistente de configuração do servidor do MBAM.</span><span class="sxs-lookup"><span data-stu-id="53031-107">You can also brand the Self-Service Portal by using the **Enable-MbamWebApplication** Windows PowerShell cmdlet or the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="53031-108">Para obter instruções sobre como usar o assistente, confira [como configurar os aplicativos Web do MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="53031-108">For instructions on using the wizard, see [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>



**<span data-ttu-id="53031-109">Observação</span><span class="sxs-lookup"><span data-stu-id="53031-109">Note</span></span>**  
<span data-ttu-id="53031-110">Nas instruções a seguir, *SelfService* é o nome do diretório virtual padrão do portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="53031-110">In the following instructions, *SelfService* is the default virtual directory name for the Self-Service Portal.</span></span> <span data-ttu-id="53031-111">Você pode ter usado um nome diferente ao configurar o portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="53031-111">You might have used a different name when you configured the Self-Service Portal.</span></span>



**<span data-ttu-id="53031-112">Para definir o tempo limite da sessão e a identidade visual do portal de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="53031-112">To set the session time-out and branding for the Self-Service Portal</span></span>**

1.  <span data-ttu-id="53031-113">Para definir o período de tempo limite da sessão do usuário final, inicie o **Gerenciador dos serviços de informações da Internet**ou execute **inetmgr.exe**.</span><span class="sxs-lookup"><span data-stu-id="53031-113">To set the time-out period for the end user’s session, start the **Internet Information Services Manager**, or run **inetmgr.exe**.</span></span>

2.  <span data-ttu-id="53031-114">Navegue até **sites** &gt; **Administração e monitoramento do Microsoft BitLocker** &gt; **SelfService** &gt; **ASP.net** &gt; **estado de sessão**e altere o valor de **tempo limite** em **configurações de cookie** para o número de minutos após o qual a sessão do portal de autoatendimento do usuário final expira.</span><span class="sxs-lookup"><span data-stu-id="53031-114">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **ASP.NET** &gt; **Session State**, and change the **Time-out** value under **Cookie Settings** to the number of minutes after which the end user’s Self-Service Portal session expires.</span></span> <span data-ttu-id="53031-115">O valor padrão é **5**.</span><span class="sxs-lookup"><span data-stu-id="53031-115">The default value is **5**.</span></span> <span data-ttu-id="53031-116">Para desabilitar a configuração de modo que não haja tempo limite, defina o valor como **0**.</span><span class="sxs-lookup"><span data-stu-id="53031-116">To disable the setting so that there is no time-out, set the value to **0**.</span></span>

3.  <span data-ttu-id="53031-117">Para definir os itens de identidade visual do portal de autoatendimento, inicie o **Gerenciador dos serviços de informações da Internet** ou execute **inetmgr.exe**.</span><span class="sxs-lookup"><span data-stu-id="53031-117">To set the branding items for the Self-Service Portal, start the **Internet Information Services Manager** or run **inetmgr.exe**.</span></span>

4.  <span data-ttu-id="53031-118">Navegue até **sites** &gt; **Administração e monitoramento do Microsoft BitLocker** &gt; **SelfService** &gt; **configurações do aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="53031-118">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

5.  <span data-ttu-id="53031-119">Na coluna **nome** , selecione o item que você deseja alterar e altere o valor padrão para refletir o nome que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="53031-119">In the **Name** column, select the item that you want to change, and change the default value to reflect the name that you want to use.</span></span> <span data-ttu-id="53031-120">A tabela a seguir lista os valores que você pode definir.</span><span class="sxs-lookup"><span data-stu-id="53031-120">The following table lists the values that you can set.</span></span>

    **<span data-ttu-id="53031-121">Tenha</span><span class="sxs-lookup"><span data-stu-id="53031-121">Caution</span></span>**  
    <span data-ttu-id="53031-122">Não altere o valor na coluna Name (CompanyName \ \*), pois isso fará com que o portal de autoatendimento pare de funcionar.</span><span class="sxs-lookup"><span data-stu-id="53031-122">Do not change the value in the Name column (CompanyName\*), as it will cause Self-Service Portal to stop working.</span></span>



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





## <span data-ttu-id="53031-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="53031-123">Related topics</span></span>


[<span data-ttu-id="53031-124">Personalizando o Portal de Autoatendimento para sua organização</span><span class="sxs-lookup"><span data-stu-id="53031-124">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)



## <span data-ttu-id="53031-125">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="53031-125">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="53031-126">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="53031-126">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="53031-127">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="53031-127">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





