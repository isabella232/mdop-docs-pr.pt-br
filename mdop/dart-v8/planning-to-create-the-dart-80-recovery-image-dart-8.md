---
title: Planejamento para criar a imagem de recuperação do DaRT 8.0
description: Planejamento para criar a imagem de recuperação do DaRT 8.0
author: dansimp
ms.assetid: cfd0e1e2-c379-4460-b545-3f7be9f33583
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1d1dc7dc5b3776638523a282d9216b80d4ce9ce1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799546"
---
# <span data-ttu-id="3bd94-103">Planejamento para criar a imagem de recuperação do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="3bd94-103">Planning to Create the DaRT 8.0 Recovery Image</span></span>


<span data-ttu-id="3bd94-104">Use as informações desta seção quando estiver planejando criar a imagem de recuperação do Microsoft (Microsoft Diagnostics and Recovery Toolset) 8,0.</span><span class="sxs-lookup"><span data-stu-id="3bd94-104">Use the information in this section when you are planning to create the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 recovery image.</span></span>

## <span data-ttu-id="3bd94-105">Planejando criar a imagem de recuperação do DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="3bd94-105">Planning to create the DaRT 8.0 recovery image</span></span>


<span data-ttu-id="3bd94-106">Ao criar a imagem de recuperação do DaRT, você precisa decidir quais ferramentas incluir na imagem.</span><span class="sxs-lookup"><span data-stu-id="3bd94-106">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="3bd94-107">Para tomar a decisão, considere que os usuários finais podem ter acesso a essas ferramentas.</span><span class="sxs-lookup"><span data-stu-id="3bd94-107">To make the decision, consider that end users may have access to those tools.</span></span> <span data-ttu-id="3bd94-108">Se os engenheiros de suporte adotarem a mídia de recuperação de imagem para os computadores dos usuários finais para diagnosticar problemas, talvez você queira instalar todas as ferramentas na imagem de recuperação.</span><span class="sxs-lookup"><span data-stu-id="3bd94-108">If support engineers will take the recovery image media to end users’ computers to diagnose issues, you may want to install all of the tools on the recovery image.</span></span> <span data-ttu-id="3bd94-109">Se você planeja diagnosticar os computadores dos usuários finais remotamente, talvez queira desativar algumas das ferramentas, como apagamento de disco e editor do registro, e, em seguida, habilitar outras ferramentas, incluindo conexão remota.</span><span class="sxs-lookup"><span data-stu-id="3bd94-109">If you plan to diagnose end user’s computers remotely, you may want to disable some of the tools, such as Disk Wipe and Registry Editor, and then enable other tools, including Remote Connection.</span></span>

<span data-ttu-id="3bd94-110">Ao criar a imagem de recuperação do DaRT, você também especifica se deseja incluir drivers ou arquivos adicionais.</span><span class="sxs-lookup"><span data-stu-id="3bd94-110">When you create the DaRT recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="3bd94-111">Determine os locais de drivers ou arquivos adicionais que você deseja incluir na imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="3bd94-111">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

<span data-ttu-id="3bd94-112">Para obter mais informações sobre as ferramentas do DaRT, consulte [visão geral das ferramentas no DaRT 8,0](overview-of-the-tools-in-dart-80-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="3bd94-112">For more information about the DaRT tools, see [Overview of the Tools in DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md).</span></span> <span data-ttu-id="3bd94-113">Para obter mais informações sobre como criar uma imagem de recuperação segura, consulte [considerações de segurança para o DaRT 8,0](security-considerations-for-dart-80--dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="3bd94-113">For more information about how to help create a secure recovery image, see [Security Considerations for DaRT 8.0](security-considerations-for-dart-80--dart-8.md).</span></span>

## <span data-ttu-id="3bd94-114">Pré-requisitos para a imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="3bd94-114">Prerequisites for the recovery image</span></span>


<span data-ttu-id="3bd94-115">Os seguintes itens são necessários ou recomendados para criar a imagem de recuperação do DaRT:</span><span class="sxs-lookup"><span data-stu-id="3bd94-115">The following items are required or recommended for creating the DaRT recovery image:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3bd94-116">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="3bd94-116">Prerequisite</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="3bd94-117">Detalhes</span><span class="sxs-lookup"><span data-stu-id="3bd94-117">Details</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bd94-118">Arquivos de origem do Windows 8</span><span class="sxs-lookup"><span data-stu-id="3bd94-118">Windows 8 source files</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bd94-119">Obrigatório para criar a imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="3bd94-119">Required to create the DaRT recovery image.</span></span> <span data-ttu-id="3bd94-120">Fornecer o caminho de um DVD do Windows 8 ou dos arquivos de origem do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3bd94-120">Provide the path of a Windows 8 DVD or of Windows 8 source files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bd94-121">Ferramentas de depuração do Windows para a sua plataforma</span><span class="sxs-lookup"><span data-stu-id="3bd94-121">Windows Debugging Tools for your platform</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bd94-122">Obrigatório ao executar o <strong> Crash Analyzer </strong> para determinar a causa de uma falha no computador.</span><span class="sxs-lookup"><span data-stu-id="3bd94-122">Required when you run the <strong>Crash Analyzer</strong> to determine the cause of a computer failure.</span></span> <span data-ttu-id="3bd94-123">Recomendamos que você especifique o caminho das ferramentas de depuração do Windows no momento em que cria a imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="3bd94-123">We recommend that you specify the path of the Windows Debugging Tools at the time that you create the DaRT recovery image.</span></span> <span data-ttu-id="3bd94-124">Você pode baixar as ferramentas de depuração do Windows aqui: <a href="https://go.microsoft.com/fwlink/?LinkId=99934" data-raw-source="[Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934)"> baixar e instalar as ferramentas de depuração para Windows </a> .</span><span class="sxs-lookup"><span data-stu-id="3bd94-124">You can download the Windows Debugging Tools here: <a href="https://go.microsoft.com/fwlink/?LinkId=99934" data-raw-source="[Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934)">Download and Install Debugging Tools for Windows</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bd94-125">Opcional: <strong> definições do defender </strong></span><span class="sxs-lookup"><span data-stu-id="3bd94-125">Optional: <strong>Defender</strong> definitions</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bd94-126">As definições mais recentes para o <strong> defender </strong> são necessárias ao executar o <strong> defender </strong> .</span><span class="sxs-lookup"><span data-stu-id="3bd94-126">The latest definitions for <strong>Defender</strong> are required when you run <strong>Defender</strong>.</span></span> <span data-ttu-id="3bd94-127">Embora você possa baixar as definições ao executar o <strong> defender </strong> , recomendamos baixar as definições mais recentes no momento em que cria a imagem de recuperação do DART para que você ainda possa executar a ferramenta com as definições mais recentes mesmo que o computador com problema não tenha conectividade de rede.</span><span class="sxs-lookup"><span data-stu-id="3bd94-127">Although you can download the definitions when you run <strong>Defender</strong>, we recommend that you download the latest definitions at the time you create the DaRT recovery image so that you can still run the tool with the latest definitions even if the problem computer does not have network connectivity.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bd94-128">Opcional: Arquivos de símbolos do Windows para uso com o <strong> Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="3bd94-128">Optional: Windows symbols files for use with <strong>Crash Analyzer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3bd94-129">Geralmente, as informações de depuração são armazenadas em um arquivo de símbolo separado do programa.</span><span class="sxs-lookup"><span data-stu-id="3bd94-129">Typically, debugging information is stored in a symbol file that is separate from the program.</span></span> <span data-ttu-id="3bd94-130">Você deve ter acesso às informações de símbolo ao depurar um aplicativo que parou de responder, por exemplo, se ele parou de funcionar.</span><span class="sxs-lookup"><span data-stu-id="3bd94-130">You must have access to the symbol information when you debug an application that has stopped responding, for example, if it stopped working.</span></span> <span data-ttu-id="3bd94-131">Para obter mais informações, consulte <a href="diagnosing-system-failures-with-crash-analyzer--dart-8.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)"> diagnosticar falhas do sistema com o Crash Analyzer </a> .</span><span class="sxs-lookup"><span data-stu-id="3bd94-131">For more information, see <a href="diagnosing-system-failures-with-crash-analyzer--dart-8.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)">Diagnosing System Failures with Crash Analyzer</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="3bd94-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3bd94-132">Related topics</span></span>


[<span data-ttu-id="3bd94-133">Planejamento da implantação do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="3bd94-133">Planning to Deploy DaRT 8.0</span></span>](planning-to-deploy-dart-80-dart-8.md)

 

 





