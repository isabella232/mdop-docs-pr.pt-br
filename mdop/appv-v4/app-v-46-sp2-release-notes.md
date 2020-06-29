---
title: Notas de versão do App-V 4.6 SP2
description: Notas de versão do App-V 4.6 SP2
author: dansimp
ms.assetid: abb536f0-e187-4c5b-952a-f837abd10ad2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cf36a6361e6f49c2b868c6752e1b2eb379cc9a31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799053"
---
# <span data-ttu-id="952e6-103">Notas de versão do App-V 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="952e6-103">App-V 4.6 SP2 Release Notes</span></span>


**<span data-ttu-id="952e6-104">Para pesquisar essas notas de versão, pressione CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="952e6-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="952e6-105">Leia estas notas de versão cuidadosamente antes de instalar o Microsoft Application Virtualization (App-V) 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="952e6-105">Read these release notes thoroughly before you install Microsoft Application Virtualization (App-V)4.6 SP2.</span></span>

<span data-ttu-id="952e6-106">Estas notas da versão contêm informações necessárias para instalar com êxito o Application Virtualization 4,6 SP2.</span><span class="sxs-lookup"><span data-stu-id="952e6-106">These release notes contain information that is required to successfully install Application Virtualization 4.6 SP2.</span></span> <span data-ttu-id="952e6-107">As notas de versão também contêm informações que não estão disponíveis na documentação do produto.</span><span class="sxs-lookup"><span data-stu-id="952e6-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="952e6-108">Se houver uma diferença entre essas notas de versão e outras documentações do App-V 4.6 SP2, a alteração mais recente deve ser considerada autorizada.</span><span class="sxs-lookup"><span data-stu-id="952e6-108">If there is a difference between these release notes and other App-V4.6SP2 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="952e6-109">Estas notas de versão substituem o conteúdo que está incluído neste produto.</span><span class="sxs-lookup"><span data-stu-id="952e6-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="952e6-110">Sobre a documentação do produto</span><span class="sxs-lookup"><span data-stu-id="952e6-110">About the Product Documentation</span></span>


<span data-ttu-id="952e6-111">Para obter mais informações sobre a documentação do App-V, consulte a página de [virtualização de aplicativos](https://go.microsoft.com/fwlink/?LinkID=232982) no Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="952e6-111">For more information about documentation for App-V, see the [Application Virtualization](https://go.microsoft.com/fwlink/?LinkID=232982) page on Microsoft TechNet.</span></span>

## <span data-ttu-id="952e6-112">Fornecendo comentários</span><span class="sxs-lookup"><span data-stu-id="952e6-112">Providing feedback</span></span>


<span data-ttu-id="952e6-113">Estamos interessados em seus comentários sobre o App-V 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="952e6-113">We are interested in your feedback on App-V4.6SP2.</span></span> <span data-ttu-id="952e6-114">Você pode enviar seus comentários para o <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="952e6-114">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="952e6-115">**Observação**  Este endereço de e-mail não é um canal de suporte, mas seus comentários nos ajudarão a planejar mudanças futuras para nossa documentação e versões de produtos.</span><span class="sxs-lookup"><span data-stu-id="952e6-115">**Note** This email address is not a support channel, but your feedback will help us to plan future changes for our documentation and product releases.</span></span>

 

<span data-ttu-id="952e6-116">Para obter as informações mais recentes sobre o MDOP e recursos de aprendizagem adicionais, consulte a página [experiência de informações do MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="952e6-116">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="952e6-117">Para obter mais informações sobre novas atualizações ou fornecer comentários, siga-nos no [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="952e6-117">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <a href="" id="known-issues-with-app-v-4-6-sp2-"></a><span data-ttu-id="952e6-118">Problemas conhecidos com o App-V 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="952e6-118">Known Issues with App-V4.6SP2</span></span>


### <span data-ttu-id="952e6-119">O suporte curto a nomes de arquivo está desabilitado para unidades físicas não pertencentes ao sistema durante a sequência</span><span class="sxs-lookup"><span data-stu-id="952e6-119">Short file name support is disabled for non-system physical drives when you sequence</span></span>

<span data-ttu-id="952e6-120">Quando você sequencia no Windows 8 ou no Windows Server 2012, o suporte para nomes de arquivo curtos (8,3) é desabilitado por padrão para unidades físicas que não sejam do sistema.</span><span class="sxs-lookup"><span data-stu-id="952e6-120">When you sequence on Windows 8 or Windows Server 2012, support for short file names (8.3) is disabled by default for non-system physical drives.</span></span>

<span data-ttu-id="952e6-121">A unidade física subjacente associada ao diretório de aplicativos virtual primário (por exemplo, "Q:\\appname") na estação de sequenciamento deve fornecer suporte a curto (8,3) para o aplicativo do App-V 4.6 SP2 gerar nomes de arquivo curtos ao criar pacotes de aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="952e6-121">The underlying physical drive associated with the primary virtual application directory (for example, “Q:\\appname”) on the sequencing station must provide short file name (8.3) support in order for the App-V4.6SP2 Sequencer to generate short file names when creating virtual application packages.</span></span> <span data-ttu-id="952e6-122">O suporte ao nome do arquivo curto (8,3) é desabilitado por padrão para unidades físicas que não são do sistema no Windows 8 ou no Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="952e6-122">Short file name (8.3) support is disabled by default for non-system physical drives on Windows 8 or Windows Server 2012.</span></span>

<span data-ttu-id="952e6-123">**Solução alternativa:** Habilite o suporte a curto File Name (8,3) em unidades físicas não pertencentes ao sistema.</span><span class="sxs-lookup"><span data-stu-id="952e6-123">**Workaround:** Enable short file name (8.3) support on non-system physical drives.</span></span> <span data-ttu-id="952e6-124">Você pode usar o comando a seguir para habilitar o suporte curto a nomes de arquivo no Windows 8 ou no Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="952e6-124">You can use the following command to enable short file name support on Windows 8 or Windows Server 2012.</span></span>

``` syntax
fsutil 8dot3name set <virtual drive letter>:
```

<span data-ttu-id="952e6-125">Por exemplo, use o seguinte comando se a letra da unidade for "p:":</span><span class="sxs-lookup"><span data-stu-id="952e6-125">For example, use the following command if the drive letter is “Q:”:</span></span>

``` syntax
fsutil 8dot3name set Q: 0
```

<span data-ttu-id="952e6-126">**Observação**  Você não precisa alterar essa configuração no cliente App-V porque o sistema de arquivos App-V manipula corretamente caminhos curtos no Windows 8 ou no Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="952e6-126">**Note** You do not need to change this setting on the App-V client because the App-V file system properly handles short paths on Windows 8 or Windows Server 2012.</span></span>

 

### <a href="" id="-------------app-v-does-not-override-the-default-handler-for-file-type-or-protocol-associations-on-windows-8"></a> <span data-ttu-id="952e6-127">O App-V não substitui o manipulador padrão do tipo de arquivo ou associações de protocolo no Windows 8</span><span class="sxs-lookup"><span data-stu-id="952e6-127">App-V does not override the default handler for file type or protocol associations on Windows 8</span></span>

<span data-ttu-id="952e6-128">Se você selecionar um aplicativo padrão usando **programas padrão** no **painel de controle** no Windows 8, o App-V não substituirá as associações de tipo de arquivo associadas a esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="952e6-128">If you select a default application by using **Default Programs** in **Control Panel** on Windows 8, App-V will not override the associated file type associations for that application.</span></span>

<span data-ttu-id="952e6-129">**Solução alternativa:** Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="952e6-129">**Workaround:** None.</span></span>

### <span data-ttu-id="952e6-130">O Outlook 2010 virtualizado não é oferecido como uma opção para links do mailto clicáveis no Windows 8</span><span class="sxs-lookup"><span data-stu-id="952e6-130">Virtualized Outlook 2010 is not offered as an option for mailto clickable links on Windows 8</span></span>

<span data-ttu-id="952e6-131">A extensão do mailto para Shell não oferece o Outlook 2010 virtualizado no Windows 8.</span><span class="sxs-lookup"><span data-stu-id="952e6-131">The mailto shell extension does not offer virtualized Outlook 2010 on Windows 8.</span></span> <span data-ttu-id="952e6-132">Por exemplo, se você clicar em um link mailto: do Outlook virtualizado do Outlook 2010 que está em execução no Windows 8, uma nova janela de email não será criada.</span><span class="sxs-lookup"><span data-stu-id="952e6-132">For example, if you click a mailto: link from virtualized Outlook 2010 that is running on Windows 8, a new email window is not created.</span></span> <span data-ttu-id="952e6-133">Esta opção funciona corretamente no Windows 7 e em versões anteriores do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="952e6-133">This option works correctly on Windows 7 and earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="952e6-134">**Solução alternativa:** Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="952e6-134">**Workaround:** None.</span></span>

### <a href="" id="-------------application-virtualization-4-6-sp2-update-is-not-offered-on-all-locales-that-use-microsoft-update"></a> <span data-ttu-id="952e6-135">A atualização do Application Virtualization 4,6 SP2 não é oferecida em todas as localidades que usam o Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="952e6-135">Application Virtualization 4.6 SP2 update is not offered on all locales that use Microsoft Update</span></span>

<span data-ttu-id="952e6-136">Quando você usa o Microsoft Update, a atualização do App-V 4.6 SP2 não está disponível para as seguintes localidades de idioma:</span><span class="sxs-lookup"><span data-stu-id="952e6-136">When you use Microsoft Update, the update for App-V4.6SP2 is not available for the following language locales:</span></span>

-   <span data-ttu-id="952e6-137">Cazaque</span><span class="sxs-lookup"><span data-stu-id="952e6-137">Kazakh</span></span>

-   <span data-ttu-id="952e6-138">Híndi</span><span class="sxs-lookup"><span data-stu-id="952e6-138">Hindi</span></span>

-   <span data-ttu-id="952e6-139">Sérvio-cirílico</span><span class="sxs-lookup"><span data-stu-id="952e6-139">Serbian-Cyrillic</span></span>

<span data-ttu-id="952e6-140">**Solução alternativa:** Se você estiver usando o Microsoft Windows Server Update Services (WSUS), use a versão em inglês da atualização ou baixe a atualização do catálogo do Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="952e6-140">**Workaround:** If you are using Microsoft Windows Server Update Services (WSUS), use the English version of the update or download the update from the Microsoft Update Catalog.</span></span>

## <span data-ttu-id="952e6-141">Informações de direitos autorais da versão</span><span class="sxs-lookup"><span data-stu-id="952e6-141">Release Notes Copyright Information</span></span>


<span data-ttu-id="952e6-142">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune e WindowsPowerShell são marcas comerciais do grupo de empresas da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="952e6-142">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="952e6-143">Todas as outras marcas comerciais são propriedade de seus respectivos proprietários.</span><span class="sxs-lookup"><span data-stu-id="952e6-143">All other trademarks are property of their respective owners.</span></span>



## <span data-ttu-id="952e6-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="952e6-144">Related topics</span></span>


[<span data-ttu-id="952e6-145">Sobre o Microsoft Application Virtualization 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="952e6-145">About Microsoft Application Virtualization 4.6 SP2</span></span>](about-microsoft-application-virtualization-46-sp2.md)

 

 





