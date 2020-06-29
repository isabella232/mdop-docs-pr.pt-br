---
title: Solução de problemas do Application Virtualization Sequencer
description: Solução de problemas do Application Virtualization Sequencer
author: dansimp
ms.assetid: 2712094b-a0bc-4643-aced-5415535f3fec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8b84f37217f29ff2c08a2254d7f54ce74348d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796686"
---
# <span data-ttu-id="f56c8-103">Solução de problemas do Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="f56c8-103">Troubleshooting Application Virtualization Sequencer Issues</span></span>


<span data-ttu-id="f56c8-104">Este tópico inclui informações que você pode usar para ajudar a solucionar problemas gerais no sequenciador do Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="f56c8-104">This topic includes information that you can use to help troubleshoot general issues on the Application Virtualization (App-V) Sequencer.</span></span>

## <span data-ttu-id="f56c8-105">A criação de um arquivo SFTD usando o sequenciador App-V aumenta o número da versão inesperadamente</span><span class="sxs-lookup"><span data-stu-id="f56c8-105">Creating an SFTD File by Using the App-V Sequencer Increases the Version Number Unexpectedly</span></span>


<span data-ttu-id="f56c8-106">Use a linha de comando para gerar um novo arquivo. SFT.</span><span class="sxs-lookup"><span data-stu-id="f56c8-106">Use the command line to generate a new .sft file.</span></span> <span data-ttu-id="f56c8-107">Para criar o arquivo. sft usando a linha de comando, digite o seguinte em um prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="f56c8-107">To create the .sft file by using the command line, enter the following at a command prompt:</span></span>

**<span data-ttu-id="f56c8-108">&lt;Nome do arquivo SFT base mkdiffpkg.exe nome do arquivo &gt; &lt; SFT do SFT&gt;</span><span class="sxs-lookup"><span data-stu-id="f56c8-108">mkdiffpkg.exe &lt;base SFT file name&gt; &lt;diff SFT file name&gt;</span></span>**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a><span data-ttu-id="f56c8-109">O nome do arquivo no arquivo OSD não está correto após a atualização do pacote</span><span class="sxs-lookup"><span data-stu-id="f56c8-109">File Name in OSD File Is Not Correct After Package Upgrade</span></span>


<span data-ttu-id="f56c8-110">Ao abrir um pacote para atualização, você deve especificar a unidade Q:\\ raiz como o local de saída do pacote.</span><span class="sxs-lookup"><span data-stu-id="f56c8-110">When you open a package for upgrade, you should specify the root Q:\\ drive as the output location for the package.</span></span> <span data-ttu-id="f56c8-111">Não especifique um nome de arquivo associado com o local de saída.</span><span class="sxs-lookup"><span data-stu-id="f56c8-111">Do not specify an associated file name with the output location.</span></span>

## <span data-ttu-id="f56c8-112">A instalação padrão do Microsoft Word2003 resulta em um erro quando transmitido para um cliente</span><span class="sxs-lookup"><span data-stu-id="f56c8-112">Microsoft Word2003 Default Install Results in an Error When Streamed to a Client</span></span>


<span data-ttu-id="f56c8-113">Quando você transmite o Microsoft Word2003 para um cliente, um erro é retornado, mas o Microsoft Word continua a ser executado.</span><span class="sxs-lookup"><span data-stu-id="f56c8-113">When you stream Microsoft Word2003 to a client, an error is returned, but Microsoft Word continues to run.</span></span>

**<span data-ttu-id="f56c8-114">Solução</span><span class="sxs-lookup"><span data-stu-id="f56c8-114">Solution</span></span>**

<span data-ttu-id="f56c8-115">Resequenciar o pacote de aplicativo virtual e selecionar **instalação completa**.</span><span class="sxs-lookup"><span data-stu-id="f56c8-115">Resequence the virtual application package and select **Full Install**.</span></span>

## <span data-ttu-id="f56c8-116">A atualização ativa não funciona quando você cria um pacote dependente</span><span class="sxs-lookup"><span data-stu-id="f56c8-116">Active Upgrade Does Not Work When You Create a Dependent Package</span></span>


<span data-ttu-id="f56c8-117">Quando você cria um pacote dependente usando a atualização ativa e adiciona novas entradas do registro, parece funcionar corretamente, mas as entradas do registro atualizadas não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f56c8-117">When you create a dependent package by using active upgrade and add new registry entries, it appears to function correctly, but the updated registry entries are not available.</span></span>

**<span data-ttu-id="f56c8-118">Solução</span><span class="sxs-lookup"><span data-stu-id="f56c8-118">Solution</span></span>**

<span data-ttu-id="f56c8-119">As configurações do registro são sempre armazenadas com a versão original do pacote, portanto, as atualizações para o pacote não parecerão estar disponíveis, a menos que você repare o pacote original.</span><span class="sxs-lookup"><span data-stu-id="f56c8-119">Registry settings are always stored with the original version of the package, so updates to the package will not appear to be available unless you repair the original package.</span></span>

## <span data-ttu-id="f56c8-120">Informações detalhadas não estão visíveis para documentos do Microsoft Office2007 usando a página Propriedades</span><span class="sxs-lookup"><span data-stu-id="f56c8-120">Detailed information is not visible for Microsoft Office2007 documents by using the properties page</span></span>


<span data-ttu-id="f56c8-121">Quando você tenta exibir informações detalhadas associadas a um documento do Microsoft Office2007 usando a página Propriedades, as informações detalhadas não ficam visíveis.</span><span class="sxs-lookup"><span data-stu-id="f56c8-121">When you try to view detailed information associated with a Microsoft Office2007 document by using the properties page, the detailed information is not visible.</span></span>

**<span data-ttu-id="f56c8-122">Solução</span><span class="sxs-lookup"><span data-stu-id="f56c8-122">Solution</span></span>**

<span data-ttu-id="f56c8-123">O App-V não oferece suporte às extensões Shell necessárias para essas páginas de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f56c8-123">App-V does not support the required shell extensions for these property pages.</span></span>

## <span data-ttu-id="f56c8-124">Algumas chaves do registro não são capturadas quando você sequencia aplicativos de 16 bits</span><span class="sxs-lookup"><span data-stu-id="f56c8-124">Some registry keys are not captured when you sequence 16-bit applications</span></span>


<span data-ttu-id="f56c8-125">No App-V 4,5, o gancho do registro foi movido do modo kernel para o modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="f56c8-125">In App-V 4.5, registry hooking has been moved from kernel mode to user mode.</span></span> <span data-ttu-id="f56c8-126">Se quiser sequenciar um aplicativo de 16 bits ou um aplicativo que usa um instalador de 16 bits, você deve primeiro configurar o computador do sequenciador para que o processo seja executado em sua própria cópia do computador de DOS virtual do Windows NT (NTVDM).</span><span class="sxs-lookup"><span data-stu-id="f56c8-126">If you want to sequence a 16-bit application or an application that uses a 16-bit installer, you must first configure the sequencer computer so that the process runs in its own copy of the Windows NT Virtual DOS Machine (NTVDM).</span></span>

**<span data-ttu-id="f56c8-127">Solução</span><span class="sxs-lookup"><span data-stu-id="f56c8-127">Solution</span></span>**

<span data-ttu-id="f56c8-128">Antes de sequenciar o aplicativo, defina o seguinte valor da chave do registro global REGSZ como "Sim" no computador de sequenciamento:</span><span class="sxs-lookup"><span data-stu-id="f56c8-128">Before you sequence the application, set the following global REGSZ registry key value to "yes" on the sequencing computer:</span></span>

<span data-ttu-id="f56c8-129">HKLM\\SYSTEM\\CurrentControlSet\\Control\\WOW\\DefaultSeparateVDM</span><span class="sxs-lookup"><span data-stu-id="f56c8-129">HKLM\\SYSTEM\\CurrentControlSet\\Control\\WOW\\DefaultSeparateVDM</span></span>

<span data-ttu-id="f56c8-130">Você deve reiniciar o computador para que ele tenha efeito.</span><span class="sxs-lookup"><span data-stu-id="f56c8-130">You must restart the computer before this takes effect.</span></span>

## <span data-ttu-id="f56c8-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f56c8-131">Related topics</span></span>


[<span data-ttu-id="f56c8-132">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="f56c8-132">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





