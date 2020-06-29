---
title: Elementos de arquivo OSD
description: Elementos de arquivo OSD
author: dansimp
ms.assetid: 8211b562-7549-4331-8321-144f52574e99
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8e3ebcf53ff39ecd2ef7ad0feec0bbbcae199db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796859"
---
# <span data-ttu-id="8903e-103">Elementos de arquivo OSD</span><span class="sxs-lookup"><span data-stu-id="8903e-103">OSD File Elements</span></span>


<span data-ttu-id="8903e-104">O diretório de instalação do sequenciador contém um arquivo de esquema XML, **Softricity. xsd**, que define a estrutura válida de um arquivo de descritor de software aberto (OSD).</span><span class="sxs-lookup"><span data-stu-id="8903e-104">The Sequencer installation directory contains an XML schema file, **Softricity.xsd**, which defines the valid structure of an Open Software Descriptor (OSD) file.</span></span> <span data-ttu-id="8903e-105">Veja a seguir alguns dos elementos OSD usados com mais frequência.</span><span class="sxs-lookup"><span data-stu-id="8903e-105">Following are some of the more frequently used OSD elements.</span></span>

<a href="" id="softpkg"></a><span data-ttu-id="8903e-106">SOFTPKG</span><span class="sxs-lookup"><span data-stu-id="8903e-106">SOFTPKG</span></span>  
<span data-ttu-id="8903e-107">O elemento raiz do arquivo OSD que contém todos os elementos que definem o pacote do software.</span><span class="sxs-lookup"><span data-stu-id="8903e-107">The root element of the OSD file containing all elements defining the software package.</span></span>

<a href="" id="codebase"></a><span data-ttu-id="8903e-108">CÓDIGO</span><span class="sxs-lookup"><span data-stu-id="8903e-108">CODEBASE</span></span>  
<span data-ttu-id="8903e-109">Informações sobre o arquivo. SFT para este pacote, incluindo os atributos HREF, FILENAME e GUID.</span><span class="sxs-lookup"><span data-stu-id="8903e-109">Information about the .sft file for this package, including the HREF, FILENAME, and GUID attributes.</span></span> <span data-ttu-id="8903e-110">Você pode editar o atributo HREF se alterar o ponto de distribuição desse pacote específico.</span><span class="sxs-lookup"><span data-stu-id="8903e-110">You can edit the HREF attribute if you change the distribution point of this particular package.</span></span>

<a href="" id="os"></a><span data-ttu-id="8903e-111">SO</span><span class="sxs-lookup"><span data-stu-id="8903e-111">OS</span></span>  
<span data-ttu-id="8903e-112">Define em quais sistemas operacionais esse aplicativo pode ser executado com base em valores definidos inicialmente no assistente de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="8903e-112">Defines on what operating systems this application can run based on values that are initially set in the Sequencing Wizard.</span></span> <span data-ttu-id="8903e-113">Esse valor pode conter apenas os valores definidos em **Softricity. xsd**.</span><span class="sxs-lookup"><span data-stu-id="8903e-113">This value can contain only the values defined in **Softricity.xsd**.</span></span>

<a href="" id="local-interaction-allowed"></a><span data-ttu-id="8903e-114">LOCAL \ _INTERACTION \ _ALLOWED</span><span class="sxs-lookup"><span data-stu-id="8903e-114">LOCAL\_INTERACTION\_ALLOWED</span></span>  
<span data-ttu-id="8903e-115">Definido como verdadeiro, permite a criação de objetos nomeados (eventos, exclusões mútuas, semáforos, mapeamentos de arquivos e processadores de aplicativos no namespace global, em vez de serem isolados dentro de um ambiente virtual específico, o que permite que os aplicativos virtuais interajam com os aplicativos do sistema operacional do host.</span><span class="sxs-lookup"><span data-stu-id="8903e-115">Set to TRUE, this enables creation of named objects (events, mutexes, semaphores, file mappings, and mailslots) and COM objects in the global namespace rather than isolated inside a particular virtual environment, which allows virtual applications to interact with the host operating system's applications.</span></span>

<span data-ttu-id="8903e-116">Exemplo: &lt; implementação do SOFTPKG &gt; &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="8903e-116">Example:&lt;SOFTPKG&gt;&lt;IMPLEMENTATION&gt;</span></span>

<span data-ttu-id="8903e-117">&lt;políticas de VIRTUALENV &gt; &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="8903e-117">&lt;VIRTUALENV&gt;&lt;POLICIES&gt;</span></span>

<span data-ttu-id="8903e-118">&lt;LOCAL \ _INTERACTION \ _ALLOWED &gt; verdadeiro</span><span class="sxs-lookup"><span data-stu-id="8903e-118">&lt;LOCAL\_INTERACTION\_ALLOWED&gt;TRUE</span></span>

<span data-ttu-id="8903e-119">&lt;/LOCAL\ _INTERACTION \ _ALLOWED&gt;</span><span class="sxs-lookup"><span data-stu-id="8903e-119">&lt;/LOCAL\_INTERACTION\_ALLOWED&gt;</span></span>

<span data-ttu-id="8903e-120">&lt;/POLICIES &gt; &lt; /VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="8903e-120">&lt;/POLICIES&gt;&lt;/VIRTUALENV&gt;</span></span>

<span data-ttu-id="8903e-121">&lt;/IMPLEMENTATION &gt; &lt; /SOFTPKG&gt;</span><span class="sxs-lookup"><span data-stu-id="8903e-121">&lt;/IMPLEMENTATION&gt;&lt;/SOFTPKG&gt;</span></span>

<a href="" id="dependencies"></a><span data-ttu-id="8903e-122">RELAÇÃO</span><span class="sxs-lookup"><span data-stu-id="8903e-122">DEPENDENCIES</span></span>  
<span data-ttu-id="8903e-123">Define a composição do pacote dinâmico (dependências em outros pacotes) usando uma marca CODEBASE de outro pacote.</span><span class="sxs-lookup"><span data-stu-id="8903e-123">Defines Dynamic Suite Composition (dependencies on other packages) by using a CODEBASE tag from another package.</span></span>

<span data-ttu-id="8903e-124">Exemplo: &lt; dependências &gt; &lt; codebase href = "RTSPS://Server/Package.SFT" GUID = "7579F4DF-2461-4219-BD43-494E1FDC69E3" SYSGUARDFILE = "pkg. 1 \ \ osguard. CP" Size = "6572748" Mandatory = "false"/ &gt; &lt; /Dependencies&gt;</span><span class="sxs-lookup"><span data-stu-id="8903e-124">Example:&lt;DEPENDENCIES&gt;&lt;CODEBASE HREF="rtsps://server/package.sft" GUID="7579F4DF-2461-4219-BD43-494E1FDC69E3" SYSGUARDFILE="pkg.1\\osguard.cp" SIZE="6572748" MANDATORY="FALSE"/&gt;&lt;/DEPENDENCIES&gt;</span></span>

<a href="" id="package-name"></a><span data-ttu-id="8903e-125">NOME DO PACOTE</span><span class="sxs-lookup"><span data-stu-id="8903e-125">PACKAGE NAME</span></span>  
<span data-ttu-id="8903e-126">Um nome comum para o pacote inserido na página **informações do pacote** do assistente de sequenciamento, que permite que você especifique um único nome usado para um aplicativo sequenciado contendo vários aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8903e-126">A common name for the package entered into the Sequencing Wizard **Package Information** page, which enables you to specify a single name used for a sequenced application containing multiple applications.</span></span>

<a href="" id="title"></a><span data-ttu-id="8903e-127">LHE</span><span class="sxs-lookup"><span data-stu-id="8903e-127">TITLE</span></span>  
<span data-ttu-id="8903e-128">Nome descritivo opcional do aplicativo que você está sequenciando.</span><span class="sxs-lookup"><span data-stu-id="8903e-128">Optional descriptive name of the application you are sequencing.</span></span>

<a href="" id="abstract"></a><span data-ttu-id="8903e-129">ABSTRAIR</span><span class="sxs-lookup"><span data-stu-id="8903e-129">ABSTRACT</span></span>  
<span data-ttu-id="8903e-130">Descrição resumida do pacote de software inserido no campo **comentários** na página **informações do pacote** do assistente de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="8903e-130">Short description of the software package entered in the **Comments** field in the Sequencing Wizard **Package Information** page.</span></span> <span data-ttu-id="8903e-131">Uma prática recomendada é especificar informações como o sistema operacional e o nível de Service Pack da estação de trabalho do sequenciador, a versão do sequenciador e o nome do engenheiro de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="8903e-131">A best practice is to specify information such as the operating system and service-pack level of the Sequencer workstation, Sequencer version, and the sequencing engineer’s name.</span></span>

<a href="" id="script"></a><span data-ttu-id="8903e-132">SOBRESCRITO</span><span class="sxs-lookup"><span data-stu-id="8903e-132">SCRIPT</span></span>  
<span data-ttu-id="8903e-133">Define eventos com script específicos para ocorrer durante a inicialização, o desligamento ou o streaming.</span><span class="sxs-lookup"><span data-stu-id="8903e-133">Defines specific scripted events to occur during startup, shutdown, or streaming.</span></span>

<a href="" id="mgmt-shortcutlist"></a><span data-ttu-id="8903e-134">GERENCIAMENTO \ _SHORTCUTLIST</span><span class="sxs-lookup"><span data-stu-id="8903e-134">MGMT\_SHORTCUTLIST</span></span>  
<span data-ttu-id="8903e-135">Lista de todos os atalhos definidos no assistente.</span><span class="sxs-lookup"><span data-stu-id="8903e-135">List of all shortcuts defined in the wizard.</span></span>

<a href="" id="mgmt-fileassociations"></a><span data-ttu-id="8903e-136">GERENCIAMENTO \ _FILEASSOCIATIONS</span><span class="sxs-lookup"><span data-stu-id="8903e-136">MGMT\_FILEASSOCIATIONS</span></span>  
<span data-ttu-id="8903e-137">Lista de tipos de arquivo especificados no assistente.</span><span class="sxs-lookup"><span data-stu-id="8903e-137">List of the file types specified in the wizard.</span></span>

## <span data-ttu-id="8903e-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8903e-138">Related topics</span></span>


[<span data-ttu-id="8903e-139">Sobre a guia OSD</span><span class="sxs-lookup"><span data-stu-id="8903e-139">About the OSD Tab</span></span>](about-the-osd-tab.md)

 

 





