---
title: Como instalar o Modelo de Política de Grupo do MBAM 2.0
description: Como instalar o Modelo de Política de Grupo do MBAM 2.0
author: dansimp
ms.assetid: bc193232-d060-4285-842e-d194a74dd3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6420fc4d499de05ed740b038b40aff6a9cd8a05f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799835"
---
# <span data-ttu-id="2e599-103">Como instalar o Modelo de Política de Grupo do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="2e599-103">How to Install the MBAM 2.0 Group Policy Template</span></span>


<span data-ttu-id="2e599-104">Além dos recursos do Microsoft BitLocker Administration and Monitoring (MBAM) relacionados ao servidor, o aplicativo de configuração do servidor inclui um modelo de política de grupo de administração e monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2e599-104">In addition to the server-related Microsoft BitLocker Administration and Monitoring (MBAM) features, the server setup application includes an Microsoft BitLocker Administration and Monitoring Group Policy template.</span></span> <span data-ttu-id="2e599-105">Este modelo pode ser instalado em qualquer computador capaz de executar o GPMC (console de gerenciamento de política de grupo) ou no AGPM (gerenciamento avançado de política de grupo).</span><span class="sxs-lookup"><span data-stu-id="2e599-105">This template can be installed on any computer capable of running the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="2e599-106">As etapas a seguir descrevem como instalar o modelo de política de grupo do MBAM.</span><span class="sxs-lookup"><span data-stu-id="2e599-106">The following steps describe how to install the MBAM Group Policy template.</span></span>

<span data-ttu-id="2e599-107">**Observação**  Certifique-se de usar a configuração de 32 bits em servidores de 32 bits e a configuração de 64 bits em servidores de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="2e599-107">**Note** Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>

 

**<span data-ttu-id="2e599-108">Para instalar o modelo de política de grupo do MBAM</span><span class="sxs-lookup"><span data-stu-id="2e599-108">To install the MBAM Group Policy template</span></span>**

1.  <span data-ttu-id="2e599-109">No servidor em que você deseja instalar o MBAM, execute **MBAMSetup.exe** para iniciar o assistente de instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="2e599-109">On the server where you want to install MBAM, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="2e599-110">Na página de **boas-vindas** , selecione o **programa de aperfeiçoamento da experiência do usuário**e clique em **Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="2e599-110">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="2e599-111">Leia e aceite os termos de licença para software Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="2e599-111">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="2e599-112">Por padrão, todos os recursos de administração e monitoramento do Microsoft BitLocker são selecionados para instalação.</span><span class="sxs-lookup"><span data-stu-id="2e599-112">By default, all Microsoft BitLocker Administration and Monitoring features are selected for installation.</span></span> <span data-ttu-id="2e599-113">Desmarque todas as opções de recursos, exceto o **modelo de política**, e clique em **Avançar** para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="2e599-113">Clear all feature options except for **Policy Template**, and then click **Next** to continue the installation.</span></span>

    <span data-ttu-id="2e599-114">**Observação**  O assistente de instalação verifica os pré-requisitos para a sua instalação e exibe os pré-requisitos que estão faltando.</span><span class="sxs-lookup"><span data-stu-id="2e599-114">**Note** The installation wizard checks the prerequisites for your installation and displays prerequisites that are missing.</span></span> <span data-ttu-id="2e599-115">Se todos os pré-requisitos forem atendidos, a instalação continuará.</span><span class="sxs-lookup"><span data-stu-id="2e599-115">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="2e599-116">Se um pré-requisito ausente for detectado, você precisará resolver os pré-requisitos ausentes e, em seguida, clique em **verificar pré-requisitos novamente**.</span><span class="sxs-lookup"><span data-stu-id="2e599-116">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="2e599-117">Depois que todos os pré-requisitos forem atendidos, a instalação será retomada.</span><span class="sxs-lookup"><span data-stu-id="2e599-117">Once all prerequisites are met, the installation will resume.</span></span>

     

5.  <span data-ttu-id="2e599-118">Para ver as etapas específicas sobre como e onde instalar os modelos, consulte [como baixar e implantar modelos de política de grupo do MDOP (. admx)](https://technet.microsoft.com/library/dn659707.aspx).</span><span class="sxs-lookup"><span data-stu-id="2e599-118">For specific steps about how and where to install the templates, see [How to Download and Deploy MDOP Group Policy (.admx) Templates](https://technet.microsoft.com/library/dn659707.aspx).</span></span>

6.  <span data-ttu-id="2e599-119">Depois que o assistente de configuração de administração e administração do Microsoft BitLocker exibir páginas de instalação dos recursos selecionados, clique em **concluir** para fechar a instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="2e599-119">After the Microsoft BitLocker Administration and Monitoring Setup wizard displays installation pages for the selected features, click **Finish** to close MBAM Setup.</span></span>

## <span data-ttu-id="2e599-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2e599-120">Related topics</span></span>


[<span data-ttu-id="2e599-121">Implantar Objetos de Política de Grupo no MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="2e599-121">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





