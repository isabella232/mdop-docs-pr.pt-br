---
title: Como instalar o Modelo de Política de Grupo do MBAM 1.0
description: Como instalar o Modelo de Política de Grupo do MBAM 1.0
author: dansimp
ms.assetid: 451a50b0-939c-47ad-9248-a138deade550
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a055c84fb6b1645592b53d957daf157a6055880
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799652"
---
# <span data-ttu-id="55964-103">Como instalar o Modelo de Política de Grupo do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="55964-103">How to Install the MBAM 1.0 Group Policy Template</span></span>


<span data-ttu-id="55964-104">Além dos recursos relacionados ao servidor do Microsoft BitLocker Administration and Monitoring (MBAM), o aplicativo de configuração do servidor inclui um modelo de política de grupo do MBAM.</span><span class="sxs-lookup"><span data-stu-id="55964-104">In addition to the server-related features of Microsoft BitLocker Administration and Monitoring (MBAM), the server setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="55964-105">Você pode instalar esse modelo em qualquer computador que seja capaz de executar o console de gerenciamento de política de grupo (GPMC) ou o gerenciamento avançado de política de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="55964-105">You can install this template on any computer that is capable of running the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="55964-106">As etapas a seguir descrevem como instalar o modelo de política de grupo do MBAM.</span><span class="sxs-lookup"><span data-stu-id="55964-106">The following steps describe how to install the MBAM Group Policy template.</span></span>

<span data-ttu-id="55964-107">**Observação**  Certifique-se de usar a configuração de 32 bits em servidores de 32 bits e a configuração de 64 bits em servidores de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="55964-107">**Note** Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>

 

**<span data-ttu-id="55964-108">Para instalar o modelo de política de grupo do MBAM</span><span class="sxs-lookup"><span data-stu-id="55964-108">To install the MBAM Group Policy template</span></span>**

1.  <span data-ttu-id="55964-109">Iniciar o assistente de instalação do MBAM; em seguida, clique em **instalar** na página de boas-vindas.</span><span class="sxs-lookup"><span data-stu-id="55964-109">Start the MBAM installation wizard; then, click **Install** on the Welcome page.</span></span>

2.  <span data-ttu-id="55964-110">Leia e aceite os termos de licença para software Microsoft e, em seguida, clique em **Avançar** para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="55964-110">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

3.  <span data-ttu-id="55964-111">Por padrão, todos os recursos do MBAM são selecionados para instalação.</span><span class="sxs-lookup"><span data-stu-id="55964-111">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="55964-112">Desmarque todas as opções de recursos, exceto o **modelo de política**, e clique em **Avançar** para continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="55964-112">Clear all feature options except for **Policy Template**, and then click **Next** to continue the installation.</span></span>

    <span data-ttu-id="55964-113">**Observação**  O assistente de instalação verifica os pré-requisitos para a sua instalação e exibe os pré-requisitos que estão faltando.</span><span class="sxs-lookup"><span data-stu-id="55964-113">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="55964-114">Se todos os pré-requisitos forem atendidos, a instalação continuará.</span><span class="sxs-lookup"><span data-stu-id="55964-114">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="55964-115">Se um pré-requisito ausente for detectado, você deve resolver o pré-requisito ausente e clicar **novamente em verificar pré-requisitos**.</span><span class="sxs-lookup"><span data-stu-id="55964-115">If a missing prerequisite is detected, you must resolve the missing prerequisite and then click **Check prerequisites again**.</span></span> <span data-ttu-id="55964-116">Depois que todos os pré-requisitos forem atendidos, a instalação será retomada.</span><span class="sxs-lookup"><span data-stu-id="55964-116">Once all prerequisites are met, the installation will resume.</span></span>

     

4.  <span data-ttu-id="55964-117">Depois que o assistente de configuração do MBAM exibir as páginas de instalação dos recursos selecionados, clique em **concluir** para fechar a instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="55964-117">After the MBAM Setup wizard displays installation pages for the selected features, click **Finish** to close MBAM Setup.</span></span>

## <span data-ttu-id="55964-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="55964-118">Related topics</span></span>


[<span data-ttu-id="55964-119">Implantar Objetos de Política de Grupo no MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="55964-119">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)

 

 





