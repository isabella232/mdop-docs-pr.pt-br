---
title: Como configurar o Portal de Autoatendimento quando os computadores cliente não puderem acessar a Rede de Distribuição de Conteúdo da Microsoft
description: Como configurar o Portal de Autoatendimento quando os computadores cliente não puderem acessar a Rede de Distribuição de Conteúdo da Microsoft
author: dansimp
ms.assetid: 90ee76db-9876-41b5-994a-118556d5ed3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ffce3dd023cb6ff9bd5cdb13ea789b348661de24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799483"
---
# <span data-ttu-id="464ea-103">Como configurar o Portal de Autoatendimento quando os computadores cliente não puderem acessar a Rede de Distribuição de Conteúdo da Microsoft</span><span class="sxs-lookup"><span data-stu-id="464ea-103">How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network</span></span>


<span data-ttu-id="464ea-104">Siga estas instruções se os computadores cliente da sua organização não tiverem acesso à rede de distribuição de conteúdo (CDN) do Microsoft Ajax.</span><span class="sxs-lookup"><span data-stu-id="464ea-104">Follow these instructions if the client computers in your organization do not have access to the Microsoft Ajax Content Delivery Network (CDN).</span></span>

**<span data-ttu-id="464ea-105">Por que você precisa configurar isto:</span><span class="sxs-lookup"><span data-stu-id="464ea-105">Why you need to configure this:</span></span>**

<span data-ttu-id="464ea-106">Seus computadores cliente precisam ter acesso à CDN, que fornece ao portal de autoatendimento o acesso necessário a certos arquivos JavaScript.</span><span class="sxs-lookup"><span data-stu-id="464ea-106">Your client computers need access to the CDN, which gives the Self-Service Portal the required access to certain JavaScript files.</span></span> <span data-ttu-id="464ea-107">Se você não configurar o portal de autoatendimento quando os computadores cliente não puderem acessar a CDN, somente o nome da empresa e a conta sob a qual o usuário final será efetuado será exibido.</span><span class="sxs-lookup"><span data-stu-id="464ea-107">If you don’t configure the Self-Service Portal when client computers cannot access CDN, only the company name and the account under which the end user logs in will be displayed.</span></span> <span data-ttu-id="464ea-108">Nenhuma mensagem de erro será mostrada.</span><span class="sxs-lookup"><span data-stu-id="464ea-108">No error message will be shown.</span></span>

<span data-ttu-id="464ea-109">**Observação**  No MBAM 2,5 SP1, os arquivos JavaScript são incluídos no produto, e você não precisa seguir as instruções nesta seção para configurar o SSP para dar suporte a clientes que não podem acessar a Internet.</span><span class="sxs-lookup"><span data-stu-id="464ea-109">**Note** In MBAM 2.5 SP1, the JavaScript files are included in the product, and you do not need to follow the instructions in this section to configure the SSP to support clients that cannot access the internet.</span></span>

 

**<span data-ttu-id="464ea-110">Como configurar o portal de autoatendimento quando os computadores cliente não puderem acessar a CDN</span><span class="sxs-lookup"><span data-stu-id="464ea-110">How to configure the Self-Service Portal when client computers cannot access the CDN</span></span>**

1. <span data-ttu-id="464ea-111">Baixe os seguintes arquivos JavaScript da CDN:</span><span class="sxs-lookup"><span data-stu-id="464ea-111">Download the following JavaScript files from the CDN:</span></span>

   -   [<span data-ttu-id="464ea-112">jQuery-1.10.2.min.js</span><span class="sxs-lookup"><span data-stu-id="464ea-112">jQuery-1.10.2.min.js</span></span>](https://go.microsoft.com/fwlink/?LinkID=390515)

   -   [<span data-ttu-id="464ea-113">jQuery.validate.min.js</span><span class="sxs-lookup"><span data-stu-id="464ea-113">jQuery.validate.min.js</span></span>](https://go.microsoft.com/fwlink/?LinkID=390516)

   -   [<span data-ttu-id="464ea-114">jQuery.validate.unobtrusive.min.js</span><span class="sxs-lookup"><span data-stu-id="464ea-114">jQuery.validate.unobtrusive.min.js</span></span>](https://go.microsoft.com/fwlink/?LinkID=390517)

2. <span data-ttu-id="464ea-115">Copie os arquivos JavaScript para o diretório **scripts** do portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="464ea-115">Copy the JavaScript files to the **Scripts** directory of the Self-Service Portal.</span></span> <span data-ttu-id="464ea-116">Esse diretório está localizado no <em> &lt; MBAM Self-Service &gt; \\ </em> Website\\Scripts. Self-Service Directory</span><span class="sxs-lookup"><span data-stu-id="464ea-116">This directory is located in <em>&lt;MBAM Self-Service Install Directory&gt;\\</em>Self Service Website\\Scripts.</span></span>

3. <span data-ttu-id="464ea-117">Abra o Gerenciador dos serviços de informações da Internet (IIS).</span><span class="sxs-lookup"><span data-stu-id="464ea-117">Open Internet Information Services (IIS) Manager.</span></span>

4. <span data-ttu-id="464ea-118">Expanda **sites** &gt; **Administração e monitoramento do Microsoft BitLocker**e realce **SelfService**.</span><span class="sxs-lookup"><span data-stu-id="464ea-118">Expand **Sites** &gt; **Microsoft BitLocker Administration and Monitoring**, and highlight **SelfService**.</span></span>

   **<span data-ttu-id="464ea-119">Observação</span><span class="sxs-lookup"><span data-stu-id="464ea-119">Note</span></span>**  
   <span data-ttu-id="464ea-120">*SelfService* é o nome do diretório virtual padrão.</span><span class="sxs-lookup"><span data-stu-id="464ea-120">*SelfService* is the default virtual directory name.</span></span> <span data-ttu-id="464ea-121">Se você escolheu um nome diferente para esse diretório durante a configuração, lembre-se de substituir *SelfService* nessas instruções pelo nome escolhido.</span><span class="sxs-lookup"><span data-stu-id="464ea-121">If you chose a different name for this directory during the configuration, remember to replace *SelfService* in these instructions with the name you chose.</span></span>

     

5. <span data-ttu-id="464ea-122">No painel do meio, clique duas vezes em **configurações do aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="464ea-122">In the middle pane, double-click **Application Settings**.</span></span>

6. <span data-ttu-id="464ea-123">Para cada item na lista a seguir, edite as configurações do aplicativo para referenciar o novo local substituindo/ &lt; *diretório virtual* &gt; /com/SelfService/(ou qualquer nome que você tenha escolhido durante a configuração).</span><span class="sxs-lookup"><span data-stu-id="464ea-123">For each item in the following list, edit the application settings to reference the new location by replacing /&lt;*virtual directory*&gt;/ with /SelfService/ (or whatever name you chose during configuration).</span></span> <span data-ttu-id="464ea-124">Por exemplo, o caminho do diretório virtual será semelhante a jQuery-1.10.2.min.js/selfservice/Scripts/.</span><span class="sxs-lookup"><span data-stu-id="464ea-124">For example, the virtual directory path will be similar to /selfservice/Scripts/ jQuery-1.10.2.min.js.</span></span>

   -   <span data-ttu-id="464ea-125">jQueryPath:/ &lt; *diretório virtual* &gt; /scripts/jQuery-1.10.2.min.js</span><span class="sxs-lookup"><span data-stu-id="464ea-125">jQueryPath: /&lt;*virtual directory*&gt;/Scripts/jQuery-1.10.2.min.js</span></span>

   -   <span data-ttu-id="464ea-126">jQueryValidatePath:/ &lt; *diretório virtual* &gt; /scripts/jQuery.validate.min.js</span><span class="sxs-lookup"><span data-stu-id="464ea-126">jQueryValidatePath: /&lt;*virtual directory*&gt;/Scripts/jQuery.validate.min.js</span></span>

   -   <span data-ttu-id="464ea-127">jQueryValidateUnobtrusivePath:/ &lt; *diretório virtual* &gt; /scripts/jQuery.validate.unobtrusive.min.js</span><span class="sxs-lookup"><span data-stu-id="464ea-127">jQueryValidateUnobtrusivePath: /&lt;*virtual directory*&gt;/Scripts/jQuery.validate.unobtrusive.min.js</span></span>



## <span data-ttu-id="464ea-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="464ea-128">Related topics</span></span>


[<span data-ttu-id="464ea-129">Como configurar os aplicativos Web do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="464ea-129">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

 

## <span data-ttu-id="464ea-130">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="464ea-130">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="464ea-131">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="464ea-131">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="464ea-132">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="464ea-132">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





