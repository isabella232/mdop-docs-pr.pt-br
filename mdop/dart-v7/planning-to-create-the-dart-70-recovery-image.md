---
title: Planejamento para criar a imagem de recuperação do DaRT 7.0
description: Planejamento para criar a imagem de recuperação do DaRT 7.0
author: dansimp
ms.assetid: e5d49bee-ae4e-467b-9976-c1203f6355f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c370d2a69ec8ccea217696045e64e9a0ae724815
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797904"
---
# <span data-ttu-id="e041f-103">Planejamento para criar a imagem de recuperação do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="e041f-103">Planning to Create the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="e041f-104">Use as informações desta seção quando planejar a criação da imagem de recuperação do Microsoft diagnóstico e do conjunto de ferramentas de recuperação (DaRT) 7.</span><span class="sxs-lookup"><span data-stu-id="e041f-104">Use the information in this section when you plan for creating the Microsoft Diagnostics and Recovery Toolset (DaRT)7 recovery image.</span></span>

## <span data-ttu-id="e041f-105">Planejando criar a imagem de recuperação do DaRT 7</span><span class="sxs-lookup"><span data-stu-id="e041f-105">Planning to Create the DaRT 7 Recovery Image</span></span>


<span data-ttu-id="e041f-106">Ao criar a imagem de recuperação do DaRT, você precisa decidir quais ferramentas incluir na imagem.</span><span class="sxs-lookup"><span data-stu-id="e041f-106">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="e041f-107">Quando você fizer essa decisão, lembre-se de que os usuários finais podem ter acesso às vezes a várias ferramentas DaRT.</span><span class="sxs-lookup"><span data-stu-id="e041f-107">When you make that decision, remember that end users might have access occasionally to the various DaRT tools.</span></span> <span data-ttu-id="e041f-108">Para obter mais informações sobre as ferramentas do DaRT, consulte [visão geral das ferramentas no DaRT 7,0](overview-of-the-tools-in-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="e041f-108">For more information about the DaRT tools, see [Overview of the Tools in DaRT 7.0](overview-of-the-tools-in-dart-70-new-ia.md).</span></span> <span data-ttu-id="e041f-109">Para obter mais informações sobre como criar uma imagem de recuperação segura, consulte [considerações de segurança para o DaRT 7,0](security-considerations-for-dart-70-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="e041f-109">For more information about how to help create a secure recovery image, see [Security Considerations for DaRT 7.0](security-considerations-for-dart-70-dart-7.md).</span></span>

<span data-ttu-id="e041f-110">Ao criar a imagem de recuperação do DaRT, você também especifica se deseja incluir drivers ou arquivos adicionais.</span><span class="sxs-lookup"><span data-stu-id="e041f-110">When you create the DaRT recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="e041f-111">Determine os locais de drivers ou arquivos adicionais que você deseja incluir na imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="e041f-111">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

## <span data-ttu-id="e041f-112">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="e041f-112">Prerequisites</span></span>


<span data-ttu-id="e041f-113">Os seguintes itens são necessários ou recomendados para criar a imagem de recuperação do DaRT:</span><span class="sxs-lookup"><span data-stu-id="e041f-113">The following items are required or recommended for creating the DaRT recovery image:</span></span>

-   <span data-ttu-id="e041f-114">Arquivos de origem do Windows 7</span><span class="sxs-lookup"><span data-stu-id="e041f-114">Windows 7 source files</span></span>

    <span data-ttu-id="e041f-115">Você deve fornecer o caminho de um DVD do Windows 7 ou dos arquivos de origem do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e041f-115">You must provide the path of a Windows 7 DVD or of Windows 7 source files.</span></span> <span data-ttu-id="e041f-116">Os arquivos de origem do Windows 7 são necessários para criar a imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="e041f-116">Windows 7 source files are required to create the DaRT recovery image.</span></span>

-   <span data-ttu-id="e041f-117">Ferramentas de depuração do Windows para a sua plataforma</span><span class="sxs-lookup"><span data-stu-id="e041f-117">Windows Debugging Tools for your platform</span></span>

    <span data-ttu-id="e041f-118">As ferramentas de depuração do Windows são necessárias ao executar o **Crash Analyzer** para determinar a causa da falha do computador.</span><span class="sxs-lookup"><span data-stu-id="e041f-118">Windows Debugging Tools are required when you run **Crash Analyzer** to determine the cause of a computer crash.</span></span> <span data-ttu-id="e041f-119">Recomendamos que você especifique o caminho das ferramentas de depuração do Windows no momento em que cria a imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="e041f-119">We recommend that you specify the path of the Windows Debugging Tools at the time that you create the DaRT recovery image.</span></span> <span data-ttu-id="e041f-120">Se for necessário, você pode baixar as ferramentas de depuração do Windows aqui: [baixar e instalar as ferramentas de depuração para Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span><span class="sxs-lookup"><span data-stu-id="e041f-120">If it is necessary, you can download the Windows Debugging Tools here: [Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span></span>

-   <span data-ttu-id="e041f-121">Opcional: definições de **limpeza de sistema autônomo**</span><span class="sxs-lookup"><span data-stu-id="e041f-121">Optional: **Standalone System Sweeper** definitions</span></span>

    <span data-ttu-id="e041f-122">As definições mais recentes para o **standalone System Sweeper** são necessárias ao executar essa ferramenta.</span><span class="sxs-lookup"><span data-stu-id="e041f-122">The latest definitions for the **Standalone System Sweeper** are required when you run this tool.</span></span> <span data-ttu-id="e041f-123">Embora você possa baixar as definições ao executar o **standalone System Sweeper**, recomendamos que baixe as definições mais recentes no momento em que cria a imagem de recuperação do DART.</span><span class="sxs-lookup"><span data-stu-id="e041f-123">Although you can download the definitions when you run **Standalone System Sweeper**, we recommend that you download the latest definitions at the time you create the DaRT recovery image.</span></span> <span data-ttu-id="e041f-124">Dessa forma, você ainda pode executar a ferramenta com as definições mais recentes mesmo que o computador com problema não tenha conectividade de rede.</span><span class="sxs-lookup"><span data-stu-id="e041f-124">In this manner, you can still run the tool with the latest definitions even if the problem computer does not have network connectivity.</span></span>

-   <span data-ttu-id="e041f-125">Opcional: Arquivos de símbolos do Windows para uso com o **Crash Analyzer**</span><span class="sxs-lookup"><span data-stu-id="e041f-125">Optional: Windows symbols files for use with **Crash Analyzer**</span></span>

    <span data-ttu-id="e041f-126">Geralmente, as informações de depuração são armazenadas em um arquivo de símbolo separado do executável.</span><span class="sxs-lookup"><span data-stu-id="e041f-126">Typically, debugging information is stored in a symbol file that is separate from the executable.</span></span> <span data-ttu-id="e041f-127">Você deve ter acesso às informações de símbolo ao depurar um aplicativo que parou de responder, por exemplo, se ele travou.</span><span class="sxs-lookup"><span data-stu-id="e041f-127">You must have access to the symbol information when you debug an application that has stopped responding, for example if it crashed.</span></span> <span data-ttu-id="e041f-128">Para obter mais informações, consulte [diagnosticar falhas do sistema com o Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="e041f-128">For more information, see [Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-7.md).</span></span>

## <span data-ttu-id="e041f-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e041f-129">Related topics</span></span>


[<span data-ttu-id="e041f-130">Planejamento da implantação do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="e041f-130">Planning to Deploy DaRT 7.0</span></span>](planning-to-deploy-dart-70.md)

 

 





