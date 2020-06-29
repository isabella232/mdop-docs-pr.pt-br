---
title: Como mover os sites do MBAM 2.5
description: Como mover os sites do MBAM 2.5
author: dansimp
ms.assetid: 71af9a54-c27b-408f-9d75-37c0d02e730e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa5bd8156810b3dccc1588b4dfd4cadd96fd22fb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799734"
---
# <span data-ttu-id="8cbc2-103">Como mover os sites do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8cbc2-103">How to Move the MBAM 2.5 Websites</span></span>


<span data-ttu-id="8cbc2-104">Use estes procedimentos para mover os seguintes sites do MBAM de um computador para outro, ou seja, para mover os seguintes recursos do servidor a para o servidor B:</span><span class="sxs-lookup"><span data-stu-id="8cbc2-104">Use these procedures to move the following MBAM websites from one computer to another, that is, to move the following features from Server A to Server B:</span></span>

-   <span data-ttu-id="8cbc2-105">Site de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="8cbc2-105">Administration and Monitoring Website</span></span>

-   <span data-ttu-id="8cbc2-106">Portal de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="8cbc2-106">Self-Service Portal</span></span>

<span data-ttu-id="8cbc2-107">**Importante**  Durante a configuração dos dois websites, você deve fornecer a mesma cadeia de conexão, a URL de relatórios, as contas de grupo e a conta de domínio do pool de aplicativos de serviço Web como aquelas que você está usando no momento.</span><span class="sxs-lookup"><span data-stu-id="8cbc2-107">**Important** During the configuration of both websites, you must provide the same connection string, Reports URL, group accounts, and web service application pool domain account as the ones that you are currently using.</span></span> <span data-ttu-id="8cbc2-108">Se você não usar os mesmos valores, não será possível acessar alguns dos servidores.</span><span class="sxs-lookup"><span data-stu-id="8cbc2-108">If you don’t use the same values, you cannot access some of the servers.</span></span> <span data-ttu-id="8cbc2-109">Para obter os valores atuais, use o cmdlet **Get-MbamWebApplication** do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8cbc2-109">To get the current values, use the **Get-MbamWebApplication** Windows PowerShell cmdlet.</span></span>

 

**<span data-ttu-id="8cbc2-110">Para mover o site de administração e monitoramento para outro servidor</span><span class="sxs-lookup"><span data-stu-id="8cbc2-110">To move the Administration and Monitoring Website to another server</span></span>**

1.  <span data-ttu-id="8cbc2-111">No servidor B, instale o software do servidor MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="8cbc2-111">On Server B, install the MBAM 2.5 Server software.</span></span> <span data-ttu-id="8cbc2-112">Para obter instruções, confira [instalar o software de servidor MBAM 2,5](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="8cbc2-112">For instructions, see [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span>

2.  <span data-ttu-id="8cbc2-113">No servidor B, inicie o assistente de configuração do servidor do MBAM, clique em **Adicionar novos recursos**e selecione apenas o recurso de **site Administração e monitoramento** .</span><span class="sxs-lookup"><span data-stu-id="8cbc2-113">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Administration and Monitoring Website** feature.</span></span>

    <span data-ttu-id="8cbc2-114">Você também pode usar o cmdlet **Enable-MbamWebApplication** do Windows PowerShell para configurar o site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="8cbc2-114">Alternatively, you can use the **Enable-MbamWebApplication** Windows PowerShell cmdlet to configure the Administration and Monitoring Website.</span></span>

    <span data-ttu-id="8cbc2-115">Para obter instruções sobre como configurar o site de administração e monitoramento, consulte [como configurar os aplicativos Web do MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="8cbc2-115">For instructions on how to configure the Administration and Monitoring Website, see [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>

**<span data-ttu-id="8cbc2-116">Para mover o portal de autoatendimento para outro servidor</span><span class="sxs-lookup"><span data-stu-id="8cbc2-116">To move the Self-Service Portal to another server</span></span>**

1.  <span data-ttu-id="8cbc2-117">No servidor B, instale o software do servidor MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="8cbc2-117">On Server B, install the MBAM 2.5 Server software.</span></span> <span data-ttu-id="8cbc2-118">Para obter instruções, confira [instalar o software de servidor MBAM 2,5](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="8cbc2-118">For instructions, see [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span>

2.  <span data-ttu-id="8cbc2-119">No servidor B, inicie o assistente de configuração do servidor do MBAM, clique em **Adicionar novos recursos**e selecione apenas o recurso do **portal de autoatendimento** .</span><span class="sxs-lookup"><span data-stu-id="8cbc2-119">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Self-Service Portal** feature.</span></span>

    <span data-ttu-id="8cbc2-120">Você também pode usar o cmdlet **Enable-MbamWebApplication** do Windows PowerShell para configurar o portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="8cbc2-120">Alternatively, you can use the **Enable-MbamWebApplication** Windows PowerShell cmdlet to configure the Self-Service Portal.</span></span>

    <span data-ttu-id="8cbc2-121">Para obter instruções sobre como configurar o site de administração e monitoramento, consulte [como configurar os aplicativos Web do MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="8cbc2-121">For instructions on how to configure the Administration and Monitoring Website, see [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>

3.  <span data-ttu-id="8cbc2-122">Se os computadores cliente da sua organização não tiverem acesso à rede de entrega de conteúdo da Microsoft, também será necessário mover os arquivos JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8cbc2-122">If the client computers in your organization do not have access to the Microsoft Content Delivery Network, you also have to move the JavaScript files.</span></span> <span data-ttu-id="8cbc2-123">Veja [como configurar o portal de autoatendimento quando os computadores cliente não puderem acessar a rede de entrega de conteúdo da Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8cbc2-123">See [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md) for more information.</span></span>

4.  <span data-ttu-id="8cbc2-124">Personalize o portal de autoatendimento da sua organização.</span><span class="sxs-lookup"><span data-stu-id="8cbc2-124">Customize the Self-Service Portal for your organization.</span></span> <span data-ttu-id="8cbc2-125">Use as instruções em [Personalizando o portal de autoatendimento da sua organização](customizing-the-self-service-portal-for-your-organization.md) para analisar suas personalizações atuais e para definir configurações personalizadas no portal de autoservidor no servidor B.</span><span class="sxs-lookup"><span data-stu-id="8cbc2-125">Use the instructions in [Customizing the Self-Service Portal for Your Organization](customizing-the-self-service-portal-for-your-organization.md) to review your current customizations and to configure custom settings on the Self-Server Portal on Server B.</span></span>



## <span data-ttu-id="8cbc2-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8cbc2-126">Related topics</span></span>


[<span data-ttu-id="8cbc2-127">Como configurar os aplicativos Web do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8cbc2-127">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

[<span data-ttu-id="8cbc2-128">Configurando recursos de servidor do MBAM 2.5 usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8cbc2-128">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[<span data-ttu-id="8cbc2-129">Movendo os recursos do MBAM 2.5 para outro servidor</span><span class="sxs-lookup"><span data-stu-id="8cbc2-129">Moving MBAM 2.5 Features to Another Server</span></span>](moving-mbam-25-features-to-another-server.md)

 

## <span data-ttu-id="8cbc2-130">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="8cbc2-130">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8cbc2-131">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="8cbc2-131">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8cbc2-132">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8cbc2-132">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





