---
title: Planejamento da implantação do DaRT 7.0
description: Planejamento da implantação do DaRT 7.0
author: dansimp
ms.assetid: 05e97cdb-a8c2-46e4-9c75-a7d12fe26fe8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 09725e994a95f4f93ae655402e7577e137e33f18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797901"
---
# <span data-ttu-id="b3f17-103">Planejamento da implantação do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="b3f17-103">Planning to Deploy DaRT 7.0</span></span>


<span data-ttu-id="b3f17-104">Há várias configurações e pré-requisitos de implantação diferentes que devem ser consideradas antes de criar seu plano de implantação.</span><span class="sxs-lookup"><span data-stu-id="b3f17-104">There are a number of different deployment configurations and prerequisites that you must consider before you create your deployment plan.</span></span> <span data-ttu-id="b3f17-105">Esta seção inclui informações que podem ajudá-lo a obter as informações que você precisa ter para formular um plano de implantação que melhor atenda às suas necessidades de negócios.</span><span class="sxs-lookup"><span data-stu-id="b3f17-105">This section includes information that can help you gather the information that you must have to formulate a deployment plan that best meets your business requirements.</span></span>

<span data-ttu-id="b3f17-106">Considere o seguinte ao planejar a instalação do Microsoft diagnóstico e do conjunto de ferramentas de recuperação (DaRT) 7:</span><span class="sxs-lookup"><span data-stu-id="b3f17-106">Consider the following when you plan your Microsoft Diagnostics and Recovery Toolset (DaRT)7 installation:</span></span>

-   <span data-ttu-id="b3f17-107">Ao instalar o DaRT, você pode instalar toda a funcionalidade em um computador administrador de ti no qual executará todas as tarefas associadas à execução do DaRT.</span><span class="sxs-lookup"><span data-stu-id="b3f17-107">When you install DaRT, you can either install all functionality on an IT administrator computer where you will perform all the tasks associated with running DaRT.</span></span> <span data-ttu-id="b3f17-108">Ou você pode instalar apenas a funcionalidade DaRT que cria a imagem de recuperação no computador do administrador de ti.</span><span class="sxs-lookup"><span data-stu-id="b3f17-108">Or you can install only the DaRT functionality that creates the recovery image on the IT administrator computer.</span></span> <span data-ttu-id="b3f17-109">Em seguida, instale a funcionalidade usada para executar o DaRT, como o **Visualizador de conexão remota do DART** e o **Crash Analyzer**, no computador do agente da assistência técnica.</span><span class="sxs-lookup"><span data-stu-id="b3f17-109">Then, install the functionality used to run DaRT, such as the **DaRT Remote Connection Viewer** and **Crash Analyzer**, on a helpdesk agent computer.</span></span>

-   <span data-ttu-id="b3f17-110">Para poder executar o DaRT remotamente, certifique-se de que o computador do agente de helpdesk e todos os computadores que você pode estar Solucionando remotamente estejam na mesma rede.</span><span class="sxs-lookup"><span data-stu-id="b3f17-110">To be able to run DaRT remotely, make sure that the helpdesk agent computer and all computers that you might be troubleshooting remotely are on the same network.</span></span>

-   <span data-ttu-id="b3f17-111">Antes de implantar o DaRT na produção, você pode primeiro construir um ambiente de laboratório para testes.</span><span class="sxs-lookup"><span data-stu-id="b3f17-111">Before you roll out DaRT into production, you can first build a lab environment for testing.</span></span> <span data-ttu-id="b3f17-112">Um laboratório de teste deve incluir no mínimo dois computadores, um para atuar como administrador de ti/agente de helpdesk e outro para atuar como um computador de usuário final.</span><span class="sxs-lookup"><span data-stu-id="b3f17-112">A test lab should include a minimum of two computers, one to act as the IT administrator/helpdesk agent computer and one to act as an end-user computer.</span></span> <span data-ttu-id="b3f17-113">Ou você pode usar três computadores em seu laboratório se quiser separar as responsabilidades do administrador de ti daquelas do agente da assistência técnica.</span><span class="sxs-lookup"><span data-stu-id="b3f17-113">Or, you can use three computers in your lab if you want to separate the IT administrator responsibilities from those of the helpdesk agent.</span></span>

## <span data-ttu-id="b3f17-114">Examine as configurações com suporte</span><span class="sxs-lookup"><span data-stu-id="b3f17-114">Review the supported configurations</span></span>


<span data-ttu-id="b3f17-115">Você deve revisar as informações de configuração do Microsoft Diagnostics and Recovery Toolset (DaRT) 7 para confirmar que os computadores selecionados para a instalação de cliente ou de recurso atendem aos requisitos mínimos de hardware e sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b3f17-115">You should review the Microsoft Diagnostics and Recovery Toolset (DaRT)7 Supported Configurations information to confirm that the computers you have selected for client or feature installation meet the minimum hardware and operating system requirements.</span></span>

[<span data-ttu-id="b3f17-116">Configurações compatíveis do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="b3f17-116">DaRT 7.0 Supported Configurations</span></span>](dart-70-supported-configurations-dart-7.md)

## <span data-ttu-id="b3f17-117">Plano para a criação da imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="b3f17-117">Plan for creating the DaRT recovery image</span></span>


<span data-ttu-id="b3f17-118">Ao criar a imagem de recuperação do DaRT, você precisa decidir quais ferramentas incluir na imagem.</span><span class="sxs-lookup"><span data-stu-id="b3f17-118">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="b3f17-119">Quando você fizer essa decisão, lembre-se de que os usuários finais podem ter acesso às vezes a várias ferramentas DaRT.</span><span class="sxs-lookup"><span data-stu-id="b3f17-119">When you make that decision, remember that end users might have access occasionally to the various DaRT tools.</span></span> <span data-ttu-id="b3f17-120">Quando você criar a imagem de recuperação, também será possível especificar se deseja incluir drivers ou arquivos adicionais.</span><span class="sxs-lookup"><span data-stu-id="b3f17-120">When you create the recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="b3f17-121">Determine os locais de drivers ou arquivos adicionais que você deseja incluir na imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="b3f17-121">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

<span data-ttu-id="b3f17-122">Você deve estar ciente dos pré-requisitos e outras recomendações de planejamento adicionais para criar a imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="b3f17-122">You should be aware of the prerequisites and other additional planning recommendations for creating the DaRT recovery image.</span></span>

[<span data-ttu-id="b3f17-123">Planejamento para criar a imagem de recuperação do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="b3f17-123">Planning to Create the DaRT 7.0 Recovery Image</span></span>](planning-to-create-the-dart-70-recovery-image.md)

## <span data-ttu-id="b3f17-124">Plano para salvar e implantar a imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="b3f17-124">Plan for saving and deploying the DaRT recovery image</span></span>


<span data-ttu-id="b3f17-125">Vários métodos podem ser usados para salvar e implantar a imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="b3f17-125">Several methods can be used to save and deploy the DaRT recovery image.</span></span> <span data-ttu-id="b3f17-126">Ao determinar o método que você vai usar, considere as vantagens e desvantagens de cada um.</span><span class="sxs-lookup"><span data-stu-id="b3f17-126">When you are determining the method that you will use, consider the advantages and disadvantages of each.</span></span> <span data-ttu-id="b3f17-127">Além disso, considere como você deseja usar o DaRT na sua empresa.</span><span class="sxs-lookup"><span data-stu-id="b3f17-127">Also, consider how you want to use DaRT in your enterprise.</span></span>

<span data-ttu-id="b3f17-128">**Observação**  Talvez você queira usar mais de um método em sua organização.</span><span class="sxs-lookup"><span data-stu-id="b3f17-128">**Note** You might want to use more than one method in your organization.</span></span> <span data-ttu-id="b3f17-129">Por exemplo, você pode inicializar o DaRT a partir de uma partição remota para a maioria das situações e ter uma unidade flash USB disponível para o caso de o computador do usuário final não conseguir se conectar à rede.</span><span class="sxs-lookup"><span data-stu-id="b3f17-129">For example, you can boot into DaRT from a remote partition for most situations and have a USB flash drive available in case the end-user computer cannot connect to the network.</span></span>

 

[<span data-ttu-id="b3f17-130">Planejar como salvar e implantar a imagem de recuperação do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="b3f17-130">Planning How to Save and Deploy the DaRT 7.0 Recovery Image</span></span>](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md)

## <span data-ttu-id="b3f17-131">Outros recursos para planejar a implantação do DaRT</span><span class="sxs-lookup"><span data-stu-id="b3f17-131">Other resources for Planning to Deploy DaRT</span></span>


[<span data-ttu-id="b3f17-132">Planejamento para o DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="b3f17-132">Planning for DaRT 7.0</span></span>](planning-for-dart-70-new-ia.md)

 

 





