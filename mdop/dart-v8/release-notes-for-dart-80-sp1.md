---
title: Notas de versão do DaRT 8.0 SP1
description: Notas de versão do DaRT 8.0 SP1
author: dansimp
ms.assetid: fa7512d8-fb00-4c27-8f65-c15f3a8ff1cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a4c49d12fed07f507d2db4d56969d8e7b0559c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799539"
---
# <span data-ttu-id="b53b9-103">Notas de versão do DaRT 8.0 SP1</span><span class="sxs-lookup"><span data-stu-id="b53b9-103">Release Notes for DaRT 8.0 SP1</span></span>


**<span data-ttu-id="b53b9-104">Para pesquisar essas notas de versão, pressione CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="b53b9-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="b53b9-105">Leia estas notas de versão cuidadosamente antes de instalar o Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="b53b9-105">Read these release notes thoroughly before you install Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 Service Pack 1 (SP1).</span></span>

<span data-ttu-id="b53b9-106">Estas notas da versão contêm informações necessárias para instalar com êxito o diagnóstico e o conjunto de ferramentas de recuperação do 8,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="b53b9-106">These release notes contain information that is required to successfully install Diagnostics and Recovery Toolset 8.0 SP1.</span></span> <span data-ttu-id="b53b9-107">As notas de versão também contêm informações que não estão disponíveis na documentação do produto.</span><span class="sxs-lookup"><span data-stu-id="b53b9-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="b53b9-108">Se houver uma diferença entre essas notas de versão e outra documentação do DaRT, a alteração mais recente deve ser considerada autorizada.</span><span class="sxs-lookup"><span data-stu-id="b53b9-108">If there is a difference between these release notes and other DaRT documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="b53b9-109">Estas notas de versão substituem o conteúdo que está incluído neste produto.</span><span class="sxs-lookup"><span data-stu-id="b53b9-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="b53b9-110">Sobre a documentação do produto</span><span class="sxs-lookup"><span data-stu-id="b53b9-110">About the product documentation</span></span>


<span data-ttu-id="b53b9-111">Para obter informações sobre a documentação do DaRT, consulte a [Home Page do DART](https://go.microsoft.com/fwlink/?LinkID=252096) no Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="b53b9-111">For information about documentation for DaRT, see the [DaRT home page](https://go.microsoft.com/fwlink/?LinkID=252096) on Microsoft TechNet.</span></span>

## <span data-ttu-id="b53b9-112">Problemas conhecidos com o DaRT 8,0 SP1</span><span class="sxs-lookup"><span data-stu-id="b53b9-112">Known issues with DaRT 8.0 SP1</span></span>


### <span data-ttu-id="b53b9-113">A restauração do sistema falha quando você executa o locksmith ou o editor do registro</span><span class="sxs-lookup"><span data-stu-id="b53b9-113">System restore fails when you run Locksmith or Registry Editor</span></span>

<span data-ttu-id="b53b9-114">Se você executar o locksmith, o editor do registro e possivelmente outras ferramentas, a restauração do sistema falhará.</span><span class="sxs-lookup"><span data-stu-id="b53b9-114">If you run Locksmith, Registry Editor, and possibly other tools, System Restore fails.</span></span>

<span data-ttu-id="b53b9-115">**Solução alternativa:** Feche e reinicie o DaRT e, em seguida, inicie a restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="b53b9-115">**Workaround:** Close and restart DaRT and then start System Restore.</span></span>

### <span data-ttu-id="b53b9-116">A verificação do SFC falha ao ser executada após iniciar e fechar o locksmith ou o gerenciamento do computador</span><span class="sxs-lookup"><span data-stu-id="b53b9-116">SFC scan fails to run after you launch and close Locksmith or Computer Management</span></span>

<span data-ttu-id="b53b9-117">Se você iniciar e fechar as ferramentas de gerenciamento de locksmith ou computador, verificador de arquivos do sistema falha ao executar.</span><span class="sxs-lookup"><span data-stu-id="b53b9-117">If you start and then close the Locksmith or Computer Management tools, System File Checker fails to run.</span></span>

<span data-ttu-id="b53b9-118">**Solução alternativa:** Feche e reinicie o DaRT e, em seguida, inicie o SFC.</span><span class="sxs-lookup"><span data-stu-id="b53b9-118">**Workaround:** Close and restart DaRT and then start SFC.</span></span>

### <a href="" id="-------------dart-installer-does-not-fail-when-adk-has-not-been-installed"></a> <span data-ttu-id="b53b9-119">O instalador do DaRT não falha quando o ADK não foi instalado</span><span class="sxs-lookup"><span data-stu-id="b53b9-119">DaRT installer does not fail when ADK has not been installed</span></span>

<span data-ttu-id="b53b9-120">Se você instalar o DaRT 8,0 SP1 usando a linha de comando para executar o MSI, e o ADK não tiver sido instalado, a instalação do DaRT não terá êxito.</span><span class="sxs-lookup"><span data-stu-id="b53b9-120">If you install DaRT 8.0 SP1 by using the command line to run the MSI, and the ADK has not been installed, the DaRT installation should fail.</span></span> <span data-ttu-id="b53b9-121">Atualmente, o instalador do DaRT 8,0 SP1 instala todos os componentes, exceto a imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="b53b9-121">Currently, the DaRT 8.0 SP1 installer installs all components except the DaRT recovery image.</span></span>

<span data-ttu-id="b53b9-122">**Solução alternativa:** Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b53b9-122">**Workaround:** None.</span></span>

### <span data-ttu-id="b53b9-123">Não é possível iniciar o defender após a inicialização do locksmith, do RegEdit, do Crash Analyzer e do gerenciamento do computador</span><span class="sxs-lookup"><span data-stu-id="b53b9-123">Defender cannot be launched after Locksmith, RegEdit, Crash Analyzer, and Computer Management are launched</span></span>

<span data-ttu-id="b53b9-124">O defender não será iniciado se você já tiver iniciado o locksmith, o RegEdit, o Crash Analyzer e o gerenciamento do computador.</span><span class="sxs-lookup"><span data-stu-id="b53b9-124">Defender does not launch if you have already launched Locksmith, RegEdit, Crash Analyzer, and Computer Management.</span></span>

<span data-ttu-id="b53b9-125">**Solução alternativa:** Feche e reinicie o DaRT e inicie o defender.</span><span class="sxs-lookup"><span data-stu-id="b53b9-125">**Workaround:** Close and restart DaRT and then launch Defender.</span></span>

### <span data-ttu-id="b53b9-126">O defender pode estar lento para iniciar</span><span class="sxs-lookup"><span data-stu-id="b53b9-126">Defender may be slow to launch</span></span>

<span data-ttu-id="b53b9-127">O defender às vezes leva alguns minutos para ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="b53b9-127">Defender sometimes takes a few minutes to launch.</span></span> <span data-ttu-id="b53b9-128">A barra de progresso indica o status atual de carregamento.</span><span class="sxs-lookup"><span data-stu-id="b53b9-128">The progress bar indicates the current loading status.</span></span>

<span data-ttu-id="b53b9-129">**Solução alternativa:** Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b53b9-129">**Workaround:** None.</span></span>

## <span data-ttu-id="b53b9-130">Informações de direitos autorais da versão</span><span class="sxs-lookup"><span data-stu-id="b53b9-130">Release notes copyright information</span></span>


<span data-ttu-id="b53b9-131">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune e WindowsPowerShell são marcas comerciais do grupo de empresas da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b53b9-131">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="b53b9-132">Todas as outras marcas comerciais são propriedade de seus respectivos proprietários.</span><span class="sxs-lookup"><span data-stu-id="b53b9-132">All other trademarks are property of their respective owners.</span></span>



## <span data-ttu-id="b53b9-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b53b9-133">Related topics</span></span>


[<span data-ttu-id="b53b9-134">Sobre o DaRT 8.0 SP1</span><span class="sxs-lookup"><span data-stu-id="b53b9-134">About DaRT 8.0 SP1</span></span>](about-dart-80-sp1.md)

 

 





