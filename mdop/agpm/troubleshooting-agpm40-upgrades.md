---
title: Solução de problemas de atualizações do AGPM
description: Solução de problemas de atualizações do AGPM
author: dansimp
ms.assetid: 1abbf0c1-fd32-46a8-a3ba-c005f066523d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2089eac51803dca60da51f61ebdb112fbf0bda08
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797287"
---
# <span data-ttu-id="3b78f-103">Solução de problemas de atualizações do AGPM</span><span class="sxs-lookup"><span data-stu-id="3b78f-103">Troubleshooting AGPM Upgrades</span></span>

<span data-ttu-id="3b78f-104">Esta seção lista alguns problemas comuns que você pode encontrar ao atualizar seu servidor de gerenciamento de política de grupo (AGPM) avançado para uma versão mais recente (por exemplo, AGPM 4,0 para AGPM 4,3).</span><span class="sxs-lookup"><span data-stu-id="3b78f-104">This section lists common issues that you may encounter when you upgrade your Advanced Group Policy Management (AGPM) server to a newer version (e.g. AGPM 4.0 to AGPM 4.3).</span></span> <span data-ttu-id="3b78f-105">Para diagnosticar problemas não listados aqui, talvez seja útil exibir o [AGPM de solução de problemas](troubleshooting-agpm-agpm40.md) ou um administrador do AGPM (controle total) para usar o log e o rastreamento.</span><span class="sxs-lookup"><span data-stu-id="3b78f-105">To diagnose issues not listed here, it may be helpful to view the [Troubleshooting AGPM](troubleshooting-agpm-agpm40.md) or for an AGPM Administrator (Full Control) to use logging and tracing.</span></span> <span data-ttu-id="3b78f-106">Para obter mais informações, consulte [configurar log e rastreamento](configure-logging-and-tracing-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="3b78f-106">For more information, see [Configure Logging and Tracing](configure-logging-and-tracing-agpm40.md).</span></span>

## <span data-ttu-id="3b78f-107">Quais são os problemas que você está tendo?</span><span class="sxs-lookup"><span data-stu-id="3b78f-107">What problems are you having?</span></span>

-   [<span data-ttu-id="3b78f-108">Falha ao gerar um relatório de diferença de GPO HTML (código de erro 80004003)</span><span class="sxs-lookup"><span data-stu-id="3b78f-108">Failed to generate a HTML GPO difference report (Error code 80004003)</span></span>](#bkmk-error-80004003)

### <a href="" id="bkmk-error-80004003"></a><span data-ttu-id="3b78f-109">Falha ao gerar um relatório de diferença de GPO HTML (código de erro 80004003)</span><span class="sxs-lookup"><span data-stu-id="3b78f-109">Failed to generate a HTML GPO difference report (Error code 80004003)</span></span>

-   <span data-ttu-id="3b78f-110">**Causa**: você instalou o pacote de atualização do AGPM com uma conta incorreta.</span><span class="sxs-lookup"><span data-stu-id="3b78f-110">**Cause**: You have installed the AGPM upgrade package with an incorrect account.</span></span>

-   <span data-ttu-id="3b78f-111">**Solução**: você precisará ser um administrador do AGPM para corrigir esse problema.</span><span class="sxs-lookup"><span data-stu-id="3b78f-111">**Solution**: You will need to be an AGPM administrator in order to fix this issue.</span></span>
    
    -   <span data-ttu-id="3b78f-112">Verifique se você conhece o nome de usuário & senha de sua **conta de serviço do AGPM**.</span><span class="sxs-lookup"><span data-stu-id="3b78f-112">Ensure you know the username & password of your **AGPM service account**.</span></span>

    -   <span data-ttu-id="3b78f-113">Faça logon no seu servidor do AGPM de forma interativa como sua conta de serviço do AGPM.</span><span class="sxs-lookup"><span data-stu-id="3b78f-113">Log onto your AGPM server interactively as your AGPM service account.</span></span>
        
        -   <span data-ttu-id="3b78f-114">Isso é extremamente importante, pois a instalação falhará se você usar uma conta diferente.</span><span class="sxs-lookup"><span data-stu-id="3b78f-114">This is critically important, as the install will fail if you use a different account.</span></span>

    -   <span data-ttu-id="3b78f-115">Desligue o serviço do AGPM.</span><span class="sxs-lookup"><span data-stu-id="3b78f-115">Shutdown the AGPM service.</span></span>
    
    -   <span data-ttu-id="3b78f-116">Instale o hotfix necessário.</span><span class="sxs-lookup"><span data-stu-id="3b78f-116">Install the required hotfix.</span></span>
    
    -   <span data-ttu-id="3b78f-117">Conecte-se ao AGPM usando um cliente do AGPM para testar se seus relatórios de diferença estão funcionando agora.</span><span class="sxs-lookup"><span data-stu-id="3b78f-117">Connect to AGPM using an AGPM client to test that your difference reports are now functioning.</span></span>
    
## <span data-ttu-id="3b78f-118">Instalar o pacote de hotfix 1 para o gerenciamento avançado de política de grupo da Microsoft 4,0 SP3</span><span class="sxs-lookup"><span data-stu-id="3b78f-118">Install Hotfix Package 1 for Microsoft Advanced Group Policy Management 4.0 SP3</span></span>
    
<span data-ttu-id="3b78f-119">**Problema corrigido neste hotfix: o**AGPM não pode gerar relatórios de diferença quando controla ou gerencia novos objetos de política de grupo (GPOs).</span><span class="sxs-lookup"><span data-stu-id="3b78f-119">**Issue fixed in this hotfix**: AGPM can't generate difference reports when it controls or manages new Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="3b78f-120">**Como obter esta atualização**: Instale a versão mais recente do Microsoft Desktop Optimization Pack ([versão de serviço de março de 2017](https://www.microsoft.com/download/details.aspx?id=54967)).</span><span class="sxs-lookup"><span data-stu-id="3b78f-120">**How to get this update**: Install the latest version of Microsoft Desktop Optimization Pack ([March 2017 Servicing Release](https://www.microsoft.com/download/details.aspx?id=54967)).</span></span> <span data-ttu-id="3b78f-121">Consulte [KB 4014009](https://support.microsoft.com/help/4014009/) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="3b78f-121">See [KB 4014009](https://support.microsoft.com/help/4014009/) for more information.</span></span>

<span data-ttu-id="3b78f-122">Mais especificamente, você pode optar por baixar somente o primeiro arquivo, `AGPM4.0SP1_Server_X64_KB4014009.exe` a partir da lista apresentada após pressionar o botão baixar.</span><span class="sxs-lookup"><span data-stu-id="3b78f-122">More specifically, you can choose to download only the first file, `AGPM4.0SP1_Server_X64_KB4014009.exe`, from the list presented after pressing the download button.</span></span>
      
<span data-ttu-id="3b78f-123">O link download para o pacote Microsoft Desktop Optimization Pack (versão de manutenção de março de 2017) pode ser encontrado [aqui](https://www.microsoft.com/download/details.aspx?id=54967).</span><span class="sxs-lookup"><span data-stu-id="3b78f-123">The download link to the Microsoft Desktop Optimization Pack (March 2017 Servicing Release) can be found [here](https://www.microsoft.com/download/details.aspx?id=54967).</span></span>
      
      
## <span data-ttu-id="3b78f-124">Link de referência</span><span class="sxs-lookup"><span data-stu-id="3b78f-124">Reference link</span></span>
https://support.microsoft.com/help/3127165/hotfix-package-1-for-microsoft-advanced-group-policy-management-4-0-sp
      
