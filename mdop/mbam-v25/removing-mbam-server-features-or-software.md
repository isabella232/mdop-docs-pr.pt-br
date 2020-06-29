---
title: Removendo os recursos de servidor ou o software do MBAM
description: Removendo os recursos de servidor ou o software do MBAM
author: dansimp
ms.assetid: 5212ba3f-124d-43c5-824a-608e9a192e86
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e6e57c3d2a62a4e01242ade7a82a7bfa551da83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799580"
---
# <span data-ttu-id="046dd-103">Removendo os recursos de servidor ou o software do MBAM</span><span class="sxs-lookup"><span data-stu-id="046dd-103">Removing MBAM Server Features or Software</span></span>


<span data-ttu-id="046dd-104">Estas instruções explicam como remover software e recursos do Microsoft BitLocker Administration and Monitoring (MBAM).</span><span class="sxs-lookup"><span data-stu-id="046dd-104">These instructions explain how to remove software and features from Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="046dd-105">Se você remover os recursos do MBAM Server, apenas os recursos configurados serão removidos do servidor, e não do software do servidor do MBAM.</span><span class="sxs-lookup"><span data-stu-id="046dd-105">If you remove MBAM Server features, only the configured features are removed from the server, not the MBAM Server software.</span></span> <span data-ttu-id="046dd-106">Se você remover o software MBAM Server, o software e todos os recursos do MBAM Server que você configurou nesse servidor serão removidos.</span><span class="sxs-lookup"><span data-stu-id="046dd-106">If you remove the MBAM Server software, the software and any MBAM Server features that you configured on that server are removed.</span></span>

<span data-ttu-id="046dd-107">**Observação**  Para impedir a remoção acidental de dados, o MBAM não fornece nenhum mecanismo para remover os bancos de dados; Você deve fazer isso manualmente.</span><span class="sxs-lookup"><span data-stu-id="046dd-107">**Note** To prevent the accidental removal of data, MBAM provides no mechanism for removing the databases; you must do that manually.</span></span>

 

## <a href="" id="bkmk-removeserverfeatures"></a><span data-ttu-id="046dd-108">Removendo recursos do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="046dd-108">Removing MBAM Server features</span></span>


<span data-ttu-id="046dd-109">Você pode usar qualquer um dos seguintes métodos para remover os recursos do MBAM Server que você configurou:</span><span class="sxs-lookup"><span data-stu-id="046dd-109">You can use either of the following methods to remove MBAM Server features that you have configured:</span></span>

-   <span data-ttu-id="046dd-110">Assistente de configuração do servidor do MBAM</span><span class="sxs-lookup"><span data-stu-id="046dd-110">MBAM Server Configuration wizard</span></span>

-   <span data-ttu-id="046dd-111">Cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="046dd-111">Windows PowerShell cmdlets</span></span>

### <span data-ttu-id="046dd-112">Usar o assistente de configuração do servidor do MBAM para remover recursos</span><span class="sxs-lookup"><span data-stu-id="046dd-112">Using the MBAM Server Configuration wizard to remove features</span></span>

<span data-ttu-id="046dd-113">Siga estas instruções para usar o assistente de configuração do servidor do MBAM para remover os recursos de servidor MBAM configurados de um servidor.</span><span class="sxs-lookup"><span data-stu-id="046dd-113">Follow these instructions to use the MBAM Server Configuration wizard to remove configured MBAM Server features from a server.</span></span>

**<span data-ttu-id="046dd-114">Para remover os recursos do MBAM usando o assistente</span><span class="sxs-lookup"><span data-stu-id="046dd-114">To remove MBAM features by using the wizard</span></span>**

1.  <span data-ttu-id="046dd-115">No servidor em que você deseja remover recursos, selecione **configuração do servidor do MBAM** para abrir o assistente de configuração.</span><span class="sxs-lookup"><span data-stu-id="046dd-115">On the server where you want to remove features, select **MBAM Server Configuration** to open the configuration wizard.</span></span>

2.  <span data-ttu-id="046dd-116">Clique em **remover recursos**, selecione os recursos a serem removidos e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="046dd-116">Click **Remove Features**, select the features to remove, and then click **Next**.</span></span> <span data-ttu-id="046dd-117">Uma página de **Resumo** exibe os recursos que você selecionou para remoção.</span><span class="sxs-lookup"><span data-stu-id="046dd-117">A **Summary** page displays the features you selected for removal.</span></span>

3.  <span data-ttu-id="046dd-118">Clique em **remover** para começar a remover os recursos e, em seguida, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="046dd-118">Click **Remove** to start removing the features, and then click **Close**.</span></span>

### <span data-ttu-id="046dd-119">Usando o Windows PowerShell para remover recursos</span><span class="sxs-lookup"><span data-stu-id="046dd-119">Using Windows PowerShell to remove features</span></span>

<span data-ttu-id="046dd-120">Use as etapas a seguir como um guia geral para remover os recursos do MBAM Server usando cmdlets do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="046dd-120">Use the following steps as a general guide to remove MBAM Server features by using Windows PowerShell cmdlets.</span></span>

**<span data-ttu-id="046dd-121">Para remover os recursos do MBAM usando o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="046dd-121">To remove MBAM features by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="046dd-122">Antes de remover qualquer recurso, consulte [configurando recursos do MBAM 2,5 Server usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) para examinar os pré-requisitos para usar o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="046dd-122">Before removing any features, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="046dd-123">Use os seguintes cmdlets para remover os recursos do MBAM Server:</span><span class="sxs-lookup"><span data-stu-id="046dd-123">Use the following cmdlets to remove MBAM Server features:</span></span>

    -   <span data-ttu-id="046dd-124">Disable-MbamReport</span><span class="sxs-lookup"><span data-stu-id="046dd-124">Disable-MbamReport</span></span>

    -   <span data-ttu-id="046dd-125">Disable-MbamWebApplication</span><span class="sxs-lookup"><span data-stu-id="046dd-125">Disable-MbamWebApplication</span></span>

    -   <span data-ttu-id="046dd-126">Disable-MbamCMIntegration</span><span class="sxs-lookup"><span data-stu-id="046dd-126">Disable-MbamCMIntegration</span></span>

    <span data-ttu-id="046dd-127">Para obter ajuda com os cmdlets do Windows PowerShell, digite cmdlet **Get-Help** &lt; *cmdlet* &gt; ou consulte a [automação do Microsoft Desktop Optimization Pack with Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=393498) para os cmdlets do Windows PowerShell MBAM.</span><span class="sxs-lookup"><span data-stu-id="046dd-127">To get help with Windows PowerShell cmdlets, type **Get-Help** &lt;*cmdlet*&gt; or see the [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=393498) page for the MBAM Windows PowerShell cmdlets.</span></span>

## <span data-ttu-id="046dd-128">Removendo o software MBAM Server</span><span class="sxs-lookup"><span data-stu-id="046dd-128">Removing MBAM Server software</span></span>


<span data-ttu-id="046dd-129">Use as etapas a seguir para remover o software do servidor MBAM e todos os recursos do MBAM Server que você configurou nesse servidor.</span><span class="sxs-lookup"><span data-stu-id="046dd-129">Use the following steps to remove the MBAM Server software and any MBAM Server features that you configured on that server.</span></span>

**<span data-ttu-id="046dd-130">Para remover o software do servidor MBAM</span><span class="sxs-lookup"><span data-stu-id="046dd-130">To remove the MBAM Server software</span></span>**

1.  <span data-ttu-id="046dd-131">No servidor em que você deseja desinstalar o software MBAM Server, execute **MBAMserversetup.exe** para iniciar o assistente de configuração de monitoramento e administração do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="046dd-131">On the server where you want to uninstall the MBAM Server software, run **MBAMserversetup.exe** to start the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

2.  <span data-ttu-id="046dd-132">Selecione **desinstalar**e siga os prompts restantes para concluir o processo de desinstalação do software MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="046dd-132">Select **Uninstall**, and follow the remaining prompts to complete the process of uninstalling the MBAM Server software.</span></span>



## <span data-ttu-id="046dd-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="046dd-133">Related topics</span></span>


[<span data-ttu-id="046dd-134">Implantando o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="046dd-134">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

 

 

## <span data-ttu-id="046dd-135">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="046dd-135">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="046dd-136">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="046dd-136">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="046dd-137">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="046dd-137">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



