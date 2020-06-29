---
title: Sobre pacotes do Application Virtualization
description: Sobre pacotes do Application Virtualization
author: dansimp
ms.assetid: 69bd35c1-7af3-43db-931b-3074780aa926
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cfe6df90881ea4179fa8cd224609ca6d28ff5f61
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797654"
---
# <span data-ttu-id="c0590-103">Sobre pacotes do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="c0590-103">About Application Virtualization Packages</span></span>


<span data-ttu-id="c0590-104">Na virtualização do aplicativo, um *pacote* é a saída do processo de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="c0590-104">In Application Virtualization, a *package* is the output of the sequencing process.</span></span> <span data-ttu-id="c0590-105">Use pacotes ao implantar aplicativos em seus servidores pela primeira vez e quando atualizar aplicativos com uma nova versão.</span><span class="sxs-lookup"><span data-stu-id="c0590-105">You use packages when you first deploy applications on your servers and when you upgrade applications with a new version.</span></span> <span data-ttu-id="c0590-106">Os pacotes permitem que você controle as versões do aplicativo virtual em seus servidores de gerenciamento do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="c0590-106">Packages enable you to control virtual application versions on your Application Virtualization Management Servers.</span></span> <span data-ttu-id="c0590-107">Um único pacote pode conter um ou mais aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c0590-107">A single package can contain one or more applications.</span></span> <span data-ttu-id="c0590-108">Cada pacote de aplicativo contém um conjunto de arquivos como uma unidade autônoma.</span><span class="sxs-lookup"><span data-stu-id="c0590-108">Each application package contains a set of files as a self-contained unit.</span></span>

## <span data-ttu-id="c0590-109">Gerenciando pacotes</span><span class="sxs-lookup"><span data-stu-id="c0590-109">Managing Packages</span></span>


<span data-ttu-id="c0590-110">Depois que o sequenciador cria um pacote de um ou mais aplicativos como parte de seu processo, você pode copiar os arquivos gerados do sequenciador para um servidor de gerenciamento do Application Virtualization e disponibilizá-los para streaming.</span><span class="sxs-lookup"><span data-stu-id="c0590-110">After the Sequencer creates a package of one or more applications as part of its process, you can copy the Sequencer-generated files to a Application Virtualization Management Server and make them available for streaming.</span></span>

<span data-ttu-id="c0590-111">Os pacotes disponíveis aparecem no contêiner **pacotes** no painel esquerdo do console de gerenciamento do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="c0590-111">Available packages appear under the **Packages** container in the left pane of the Application Virtualization Management Console.</span></span> <span data-ttu-id="c0590-112">Quando você importa um aplicativo com um arquivo de projeto de sequenciador (SPRJ) ou um arquivo Open Software Descriptor (OSD), uma entrada relacionada aparece no contêiner **pacotes** .</span><span class="sxs-lookup"><span data-stu-id="c0590-112">When you import an application with a Sequencer Project (SPRJ) file or an Open Software Descriptor (OSD) file, a related entry appears in the **Packages** container.</span></span> <span data-ttu-id="c0590-113">No console de gerenciamento de servidor do Application Virtualization, você pode implantar, atualizar ou excluir pacotes e versões deles.</span><span class="sxs-lookup"><span data-stu-id="c0590-113">From the Application Virtualization Server Management Console, you can then deploy, upgrade, or delete packages and versions of them.</span></span>

<span data-ttu-id="c0590-114">Cada aplicativo virtual tem um pacote associado.</span><span class="sxs-lookup"><span data-stu-id="c0590-114">Each virtual application has an associated package.</span></span> <span data-ttu-id="c0590-115">Este pacote inclui os seguintes arquivos:</span><span class="sxs-lookup"><span data-stu-id="c0590-115">This package includes the following files:</span></span>

-   <span data-ttu-id="c0590-116">SFT — o arquivo que transmite o aplicativo aos clientes.</span><span class="sxs-lookup"><span data-stu-id="c0590-116">SFT—The file that streams the application to clients.</span></span>

-   <span data-ttu-id="c0590-117">OSD — o arquivo Open Software Descriptor contém as informações necessárias para localizar e iniciar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c0590-117">OSD—The Open Software Descriptor file contains the information needed to find and launch the application.</span></span>

-   <span data-ttu-id="c0590-118">ICO — o arquivo de ícone que representa visualmente o aplicativo em interfaces do usuário e atalhos.</span><span class="sxs-lookup"><span data-stu-id="c0590-118">ICO—The icon file that visually represents the application in user interfaces and shortcuts.</span></span>

-   <span data-ttu-id="c0590-119">SPRJ — o arquivo de projeto do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="c0590-119">SPRJ—The Sequencer Project file.</span></span>

<span data-ttu-id="c0590-120">Quando você importa o arquivo SPRJ, todos os aplicativos sequenciados estão disponíveis para implantação, por padrão, mas os aplicativos não estão habilitados para streaming.</span><span class="sxs-lookup"><span data-stu-id="c0590-120">When you import the SPRJ file, all sequenced applications are available for deployment, by default, but the applications are not enabled for streaming.</span></span> <span data-ttu-id="c0590-121">Você pode optar por transmitir todos ou alguns dos aplicativos no pacote.</span><span class="sxs-lookup"><span data-stu-id="c0590-121">You can choose to stream all or some of the applications in the package.</span></span> <span data-ttu-id="c0590-122">Por exemplo, se você tiver sequenciado e importado o Microsoft Office, poderá optar por não implantar alguns aplicativos, como o assistente para salvar minhas configurações.</span><span class="sxs-lookup"><span data-stu-id="c0590-122">For example, if you sequenced and imported Microsoft Office, you can choose not to deploy some applications, such as the Save My Settings Wizard.</span></span> <span data-ttu-id="c0590-123">Nesse caso, clique com o botão direito do mouse em cada aplicativo que você deseja implantar, escolha **Propriedades**e verifique se a caixa **habilitado** está desmarcada (em branco).</span><span class="sxs-lookup"><span data-stu-id="c0590-123">In this case, right-click each application you want to deploy, choose **Properties**, and make sure that the **Enabled** box is cleared (blank).</span></span> <span data-ttu-id="c0590-124">Somente os aplicativos com a caixa **habilitado** selecionada serão transmitidos para os computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="c0590-124">Only the applications with the **Enabled** box selected will stream to client computers.</span></span>

<span data-ttu-id="c0590-125">Depois de resequenciar um pacote e produzir um novo arquivo SFT para streaming, você pode atualizar o pacote antigo com rapidez e facilidade por meio do console de gerenciamento do servidor do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="c0590-125">After you resequence a package and produce a new SFT file for streaming, you can upgrade the old package quickly and easily through the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="c0590-126">O único cenário operacional que requer o uso do nó **pacotes** é quando você introduz uma nova versão (arquivo SFT) para o pacote.</span><span class="sxs-lookup"><span data-stu-id="c0590-126">The only operational scenario that requires you to use the **Packages** node is when you introduce a new version (SFT file) for the package.</span></span> <span data-ttu-id="c0590-127">Sempre que você importa aplicativos, atribui acesso e licenças para aplicativos e assim por diante, o sistema do Application Virtualization acompanha essas informações no nível do pacote.</span><span class="sxs-lookup"><span data-stu-id="c0590-127">Whenever you import applications, assign access and licenses to applications, and so on, the Application Virtualization System tracks this information at the package level.</span></span> <span data-ttu-id="c0590-128">Isso significa que, quando você autoriza um usuário a usar um aplicativo, está fornecendo permissão ao usuário para executar qualquer aplicativo no mesmo pacote.</span><span class="sxs-lookup"><span data-stu-id="c0590-128">This means that when you authorize a user to use an application, you are giving the user permission to run any application in the same package.</span></span>

### <span data-ttu-id="c0590-129">Versão do pacote</span><span class="sxs-lookup"><span data-stu-id="c0590-129">Package Version</span></span>

<span data-ttu-id="c0590-130">Uma versão do pacote é representada por um arquivo SFT específico.</span><span class="sxs-lookup"><span data-stu-id="c0590-130">A package version is represented by a specific SFT file.</span></span> <span data-ttu-id="c0590-131">Quando você atualiza um pacote (aplica uma atualização a um aplicativo ou adiciona um aplicativo a um pacote), você gera um novo arquivo SFT.</span><span class="sxs-lookup"><span data-stu-id="c0590-131">When you upgrade a package (apply an update to an application or add an application to a package), you generate a new SFT file.</span></span> <span data-ttu-id="c0590-132">Toda vez que você cria um novo arquivo SFT, você está criando uma nova versão de pacote.</span><span class="sxs-lookup"><span data-stu-id="c0590-132">Each time you create a new SFT file, you are creating a new package version.</span></span>

<span data-ttu-id="c0590-133">Quando você importa aplicativos por meio do console de gerenciamento do servidor do Application Virtualization, o software cria automaticamente um pacote e uma versão do pacote, se eles ainda não existirem.</span><span class="sxs-lookup"><span data-stu-id="c0590-133">When you import applications through the Application Virtualization Server Management Console, the software automatically creates a package and a package version if they do not already exist.</span></span>

## <span data-ttu-id="c0590-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0590-134">Related topics</span></span>


[<span data-ttu-id="c0590-135">Sobre aplicativos do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="c0590-135">About Application Virtualization Applications</span></span>](about-application-virtualization-applications.md)

[<span data-ttu-id="c0590-136">Sobre o Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="c0590-136">About the Application Virtualization Server Management Console</span></span>](about-the-application-virtualization-server-management-console.md)

[<span data-ttu-id="c0590-137">Como gerenciar pacotes no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="c0590-137">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





