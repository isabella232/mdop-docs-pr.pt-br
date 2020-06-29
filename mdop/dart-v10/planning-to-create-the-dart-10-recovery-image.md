---
title: Planejamento para criar a imagem de recuperação do DaRT 10
description: Planejamento para criar a imagem de recuperação do DaRT 10
author: dansimp
ms.assetid: a0087d93-b88f-454b-81b2-3c7ce3718023
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 44cf052eaffd19645885618da9104e5b0a50cfd5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799180"
---
# <span data-ttu-id="86c99-103">Planejamento para criar a imagem de recuperação do DaRT 10</span><span class="sxs-lookup"><span data-stu-id="86c99-103">Planning to Create the DaRT 10 Recovery Image</span></span>


<span data-ttu-id="86c99-104">Use as informações desta seção quando estiver planejando criar uma imagem de recuperação do Microsoft DaRT (Microsoft Diagnostics and Recovery Toolset) 10.</span><span class="sxs-lookup"><span data-stu-id="86c99-104">Use the information in this section when you are planning to create the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image.</span></span>

## <span data-ttu-id="86c99-105">Planejando criar a imagem de recuperação do DaRT 10</span><span class="sxs-lookup"><span data-stu-id="86c99-105">Planning to create the DaRT 10 recovery image</span></span>


<span data-ttu-id="86c99-106">Ao criar a imagem de recuperação do DaRT, você precisa decidir quais ferramentas incluir na imagem.</span><span class="sxs-lookup"><span data-stu-id="86c99-106">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="86c99-107">Para tomar a decisão, considere que os usuários finais podem ter acesso a essas ferramentas.</span><span class="sxs-lookup"><span data-stu-id="86c99-107">To make the decision, consider that end users may have access to those tools.</span></span> <span data-ttu-id="86c99-108">Se os engenheiros de suporte adotarem a mídia de recuperação de imagem para os computadores dos usuários finais para diagnosticar problemas, talvez você queira instalar todas as ferramentas na imagem de recuperação.</span><span class="sxs-lookup"><span data-stu-id="86c99-108">If support engineers will take the recovery image media to end users’ computers to diagnose issues, you may want to install all of the tools on the recovery image.</span></span> <span data-ttu-id="86c99-109">Se você planeja diagnosticar os computadores dos usuários finais remotamente, talvez queira desativar algumas das ferramentas, como apagamento de disco e editor do registro, e, em seguida, habilitar outras ferramentas, incluindo conexão remota.</span><span class="sxs-lookup"><span data-stu-id="86c99-109">If you plan to diagnose end user’s computers remotely, you may want to disable some of the tools, such as Disk Wipe and Registry Editor, and then enable other tools, including Remote Connection.</span></span>

<span data-ttu-id="86c99-110">Ao criar a imagem de recuperação do DaRT, você também especifica se deseja incluir drivers ou arquivos adicionais.</span><span class="sxs-lookup"><span data-stu-id="86c99-110">When you create the DaRT recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="86c99-111">Determine os locais de drivers ou arquivos adicionais que você deseja incluir na imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="86c99-111">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

<span data-ttu-id="86c99-112">Para obter mais informações sobre as ferramentas do DaRT, consulte [visão geral das ferramentas no DART 10](overview-of-the-tools-in-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="86c99-112">For more information about the DaRT tools, see [Overview of the Tools in DaRT 10](overview-of-the-tools-in-dart-10.md).</span></span> <span data-ttu-id="86c99-113">Para obter mais informações sobre como criar uma imagem de recuperação segura, consulte [considerações de segurança para o DART 10](security-considerations-for-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="86c99-113">For more information about how to help create a secure recovery image, see [Security Considerations for DaRT 10](security-considerations-for-dart-10.md).</span></span>

## <span data-ttu-id="86c99-114">Pré-requisitos para a imagem de recuperação</span><span class="sxs-lookup"><span data-stu-id="86c99-114">Prerequisites for the recovery image</span></span>


<span data-ttu-id="86c99-115">Os seguintes itens são necessários ou recomendados para criar a imagem de recuperação do DaRT:</span><span class="sxs-lookup"><span data-stu-id="86c99-115">The following items are required or recommended for creating the DaRT recovery image:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="86c99-116">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="86c99-116">Prerequisite</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="86c99-117">Detalhes</span><span class="sxs-lookup"><span data-stu-id="86c99-117">Details</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86c99-118">Arquivos de origem do Windows 10</span><span class="sxs-lookup"><span data-stu-id="86c99-118">Windows 10 source files</span></span></p></td>
<td align="left"><p><span data-ttu-id="86c99-119">Obrigatório para criar a imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="86c99-119">Required to create the DaRT recovery image.</span></span> <span data-ttu-id="86c99-120">Forneça o caminho de um DVD do Windows 10 ou de arquivos de origem do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="86c99-120">Provide the path of a Windows 10 DVD or of Windows 10 source files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86c99-121">Ferramentas de depuração do Windows para a sua plataforma</span><span class="sxs-lookup"><span data-stu-id="86c99-121">Windows Debugging Tools for your platform</span></span></p></td>
<td align="left"><p><span data-ttu-id="86c99-122">Obrigatório ao executar o <strong> Crash Analyzer </strong> para determinar a causa de uma falha no computador.</span><span class="sxs-lookup"><span data-stu-id="86c99-122">Required when you run the <strong>Crash Analyzer</strong> to determine the cause of a computer failure.</span></span> <span data-ttu-id="86c99-123">Recomendamos que você especifique o caminho das ferramentas de depuração do Windows no momento em que cria a imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="86c99-123">We recommend that you specify the path of the Windows Debugging Tools at the time that you create the DaRT recovery image.</span></span> <span data-ttu-id="86c99-124">Você pode baixar as ferramentas de depuração do Windows aqui: <a href="https://docs.microsoft.com/windows-hardware/drivers/debugger/" data-raw-source="[Download and Install Debugging Tools for Windows](https://docs.microsoft.com/windows-hardware/drivers/debugger/)"> baixar e instalar as ferramentas de depuração para Windows </a> .</span><span class="sxs-lookup"><span data-stu-id="86c99-124">You can download the Windows Debugging Tools here: <a href="https://docs.microsoft.com/windows-hardware/drivers/debugger/" data-raw-source="[Download and Install Debugging Tools for Windows](https://docs.microsoft.com/windows-hardware/drivers/debugger/)">Download and Install Debugging Tools for Windows</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86c99-125">Opcional: Arquivos de símbolos do Windows para uso com o <strong> Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="86c99-125">Optional: Windows symbols files for use with <strong>Crash Analyzer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="86c99-126">Geralmente, as informações de depuração são armazenadas em um arquivo de símbolo separado do programa.</span><span class="sxs-lookup"><span data-stu-id="86c99-126">Typically, debugging information is stored in a symbol file that is separate from the program.</span></span> <span data-ttu-id="86c99-127">Você deve ter acesso às informações de símbolo ao depurar um aplicativo que parou de responder, por exemplo, se ele parou de funcionar.</span><span class="sxs-lookup"><span data-stu-id="86c99-127">You must have access to the symbol information when you debug an application that has stopped responding, for example, if it stopped working.</span></span> <span data-ttu-id="86c99-128">Para obter mais informações, consulte <a href="diagnosing-system-failures-with-crash-analyzer-dart-10.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md)"> diagnosticar falhas do sistema com o Crash Analyzer </a> .</span><span class="sxs-lookup"><span data-stu-id="86c99-128">For more information, see <a href="diagnosing-system-failures-with-crash-analyzer-dart-10.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md)">Diagnosing System Failures with Crash Analyzer</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="86c99-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="86c99-129">Related topics</span></span>

[<span data-ttu-id="86c99-130">Planejamento da implantação do DaRT 10</span><span class="sxs-lookup"><span data-stu-id="86c99-130">Planning to Deploy DaRT 10</span></span>](planning-to-deploy-dart-10.md)

 

 




