---
title: Aplicação de hotfixes no MBAM 2.5 SP1
description: Aplicação de hotfixes no MBAM 2.5 SP1
ms.author: dansimp
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 8/30/2018
ms.openlocfilehash: ea564d93a3eec6a46ec7d4c1be0f794abba9c93e
ms.sourcegitcommit: 8ecbf818a6ff2ddafd80b93614c01256484737ad
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/14/2020
ms.locfileid: "11014985"
---
# <span data-ttu-id="bb90d-103">Aplicação de hotfixes no MBAM 2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="bb90d-103">Applying hotfixes on MBAM 2.5 SP1</span></span>
<span data-ttu-id="bb90d-104">Este tópico descreve o processo para aplicar os hotfixes do servidor de administração e monitoramento do Microsoft BitLocker (MBAM) Server 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="bb90d-104">This topic describes the process for applying the hotfixes for Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 SP1</span></span>

### <span data-ttu-id="bb90d-105">Antes de começar, baixe o hotfix mais recente do Microsoft BitLocker Administration and Monitoring (MBAM) Server 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="bb90d-105">Before you begin, download the latest hotfix of Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 SP1</span></span>
[<span data-ttu-id="bb90d-106">Desktop Optimization Pack</span><span class="sxs-lookup"><span data-stu-id="bb90d-106">Desktop Optimization Pack</span></span>](https://www.microsoft.com/download/details.aspx?id=57157)

> [!NOTE]
> <span data-ttu-id="bb90d-107">Para obter mais informações sobre as versões de hotfix, consulte o [gráfico de versão do MBAM](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart).</span><span class="sxs-lookup"><span data-stu-id="bb90d-107">For more information about the hotfix releases, see the [MBAM version chart](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart).</span></span>

#### <span data-ttu-id="bb90d-108">Etapas para atualizar o servidor MBAM para o ambiente MBAM existente</span><span class="sxs-lookup"><span data-stu-id="bb90d-108">Steps to update the MBAM Server for existing MBAM environment</span></span> 
1. <span data-ttu-id="bb90d-109">Remova o recurso do servidor do MBAM (faça isso abrindo a ferramenta de configuração do servidor do MBAM e selecionando remover recursos).</span><span class="sxs-lookup"><span data-stu-id="bb90d-109">Remove MBAM server feature (do this by opening the MBAM Server Configuration Tool, then selecting Remove Features).</span></span>
2. <span data-ttu-id="bb90d-110">Remover o MBAM do MDOP do painel de controle | Programas e recursos.</span><span class="sxs-lookup"><span data-stu-id="bb90d-110">Remove MDOP MBAM from Control Panel | Programs and Features.</span></span>
3. <span data-ttu-id="bb90d-111">Instale os componentes do servidor do MBAM 2,5 SP1 RTM.</span><span class="sxs-lookup"><span data-stu-id="bb90d-111">Install MBAM 2.5 SP1 RTM server components.</span></span>
4. <span data-ttu-id="bb90d-112">Instalar o pacote cumulativo de hotfix do MBAM 2,5 SP1 mais recente.</span><span class="sxs-lookup"><span data-stu-id="bb90d-112">Install lastest MBAM 2.5 SP1 hotfix rollup.</span></span>
5. <span data-ttu-id="bb90d-113">Configure os recursos do MBAM usando o configurador do MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="bb90d-113">Configure MBAM features using MBAM Server Configurator.</span></span>

#### <span data-ttu-id="bb90d-114">Etapas para instalar o novo hotfix do servidor do MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="bb90d-114">Steps to install the new MBAM 2.5 SP1 server hotfix</span></span>
<span data-ttu-id="bb90d-115">Consulte o documento para [instalação do novo servidor](deploying-the-mbam-25-server-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="bb90d-115">Refer to the document for [new server installation](deploying-the-mbam-25-server-infrastructure.md).</span></span>
