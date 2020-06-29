---
title: Como implantar o App-V 4,6 e o cliente do App-V 5,1 no mesmo computador
description: Como implantar o App-V 4,6 e o cliente do App-V 5,1 no mesmo computador
ms.assetid: 498d50c7-f13d-4fbb-8ea1-b959ade26fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 354db96223e623a7cd0416cb49ad67eb4d8f7162
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796433"
---
# <span data-ttu-id="9bd5a-103">Como implantar o App-V 4,6 e o cliente do App-V 5,1 no mesmo computador</span><span class="sxs-lookup"><span data-stu-id="9bd5a-103">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</span></span>

<span data-ttu-id="9bd5a-104">**Observação:** O App-V 4,6 tem saído do suporte básico.</span><span class="sxs-lookup"><span data-stu-id="9bd5a-104">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="9bd5a-105">Use as seguintes informações para instalar o cliente do Microsoft Application Virtualization (App-V) 5,1 (preferencialmente, com os service packs e hotfixes mais recentes) e o cliente App-V 4.6 SP2 ou o App-V 4.6 S3 Client no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="9bd5a-105">Use the following information to install the Microsoft Application Virtualization (App-V) 5.1 client (preferably, with the latest Service Packs and hotfixes) and the App-V 4.6SP2 client or the App-V 4.6S3 client on the same computer.</span></span> <span data-ttu-id="9bd5a-106">Para obter as versões, os requisitos e outras informações de planejamento compatíveis, consulte [planejando a migração de uma versão anterior do App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md).</span><span class="sxs-lookup"><span data-stu-id="9bd5a-106">For supported versions, requirements, and other planning information, see [Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md).</span></span>

**<span data-ttu-id="9bd5a-107">Para implantar o cliente do App-V 5,1 e o aplicativo do App-V 4,6 no mesmo computador</span><span class="sxs-lookup"><span data-stu-id="9bd5a-107">To deploy the App-V 5.1 client and App-V 4.6 client on the same computer</span></span>**

1.  <span data-ttu-id="9bd5a-108">Instale a versão a seguir do cliente App-V no computador que está executando o App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="9bd5a-108">Install the following version of the App-V client on the computer that is running App-V 4.6.</span></span>

    -   [<span data-ttu-id="9bd5a-109">Microsoft Application Virtualization 4,6 Service Pack 3</span><span class="sxs-lookup"><span data-stu-id="9bd5a-109">Microsoft Application Virtualization 4.6 Service Pack 3</span></span>](https://www.microsoft.com/download/details.aspx?id=41187)

2.  <span data-ttu-id="9bd5a-110">Instale o cliente App-V 5,1 no computador que está executando a versão App-V 4,6 SP3 do cliente.</span><span class="sxs-lookup"><span data-stu-id="9bd5a-110">Install the App-V 5.1 client on the computer that is running the App-V 4.6 SP3 version of the client.</span></span> <span data-ttu-id="9bd5a-111">Para obter melhores resultados, recomendamos que você instale todas as atualizações disponíveis para o cliente do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="9bd5a-111">For best results, we recommend that you install all available updates to the App-V 5.1 client.</span></span>

3.  <span data-ttu-id="9bd5a-112">Converter ou resequenciar os pacotes gradualmente.</span><span class="sxs-lookup"><span data-stu-id="9bd5a-112">Convert or re-sequence the packages gradually.</span></span>

    -   <span data-ttu-id="9bd5a-113">Para converter os pacotes, use o conversor de pacotes do App-V 5,1 e converta os pacotes necessários para o formato de arquivo do App-V 5,1 (**. AppV**).</span><span class="sxs-lookup"><span data-stu-id="9bd5a-113">To convert the packages, use the App-V 5.1 package converter and convert the required packages to the App-V 5.1 (**.appv**) file format.</span></span>

    -   <span data-ttu-id="9bd5a-114">Para resequenciar os pacotes, considere usar a versão mais recente do sequenciador para obter os melhores resultados.</span><span class="sxs-lookup"><span data-stu-id="9bd5a-114">To re-sequence the packages, consider using the latest version of the Sequencer for best results.</span></span>

    <span data-ttu-id="9bd5a-115">Para obter mais informações sobre como publicar pacotes, consulte [como publicar um pacote usando o console de gerenciamento](how-to-publish-a-package-by-using-the-management-console-51.md).</span><span class="sxs-lookup"><span data-stu-id="9bd5a-115">For more information about publishing packages, see [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-51.md).</span></span>

4.  <span data-ttu-id="9bd5a-116">Implantar pacotes nos computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="9bd5a-116">Deploy packages to the client computers.</span></span>

5.  <span data-ttu-id="9bd5a-117">Converta os pontos de extensão, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="9bd5a-117">Convert extension points, as needed.</span></span> <span data-ttu-id="9bd5a-118">Para obter mais informações, consulte os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="9bd5a-118">For more information, see the following resources:</span></span>

    -   [<span data-ttu-id="9bd5a-119">Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.1 convertido para todos os usuários em um computador específico</span><span class="sxs-lookup"><span data-stu-id="9bd5a-119">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

    -   [<span data-ttu-id="9bd5a-120">Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.1 para um usuário específico</span><span class="sxs-lookup"><span data-stu-id="9bd5a-120">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

    -   [<span data-ttu-id="9bd5a-121">Como converter um pacote criado em uma versão anterior do App-V</span><span class="sxs-lookup"><span data-stu-id="9bd5a-121">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

6.  <span data-ttu-id="9bd5a-122">Teste se seus pacotes do App-V 5,1 foram bem-sucedidos e, em seguida, remova os pacotes do 4,6.</span><span class="sxs-lookup"><span data-stu-id="9bd5a-122">Test that your App-V 5.1 packages are successful, and then remove the 4.6 packages.</span></span> <span data-ttu-id="9bd5a-123">Para verificar o estado do usuário dos seus computadores cliente, recomendamos que você use a [virtualização da experiência do usuário](https://technet.microsoft.com/library/dn458947.aspx) ou outra ferramenta de gerenciamento do ambiente do usuário.</span><span class="sxs-lookup"><span data-stu-id="9bd5a-123">To check the user state of your client computers, we recommend that you use [User Experience Virtualization](https://technet.microsoft.com/library/dn458947.aspx) or another user environment management tool.</span></span>

    <span data-ttu-id="9bd5a-124">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="9bd5a-124">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="9bd5a-125">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="9bd5a-125">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="9bd5a-126">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="9bd5a-126">Got an App-V issue?</span></span>** <span data-ttu-id="9bd5a-127">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="9bd5a-127">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="9bd5a-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9bd5a-128">Related topics</span></span>


[<span data-ttu-id="9bd5a-129">Planejamento para a migração de uma versão anterior do App-V</span><span class="sxs-lookup"><span data-stu-id="9bd5a-129">Planning for Migrating from a Previous Version of App-V</span></span>](planning-for-migrating-from-a-previous-version-of-app-v51.md)

[<span data-ttu-id="9bd5a-130">Implantação do sequenciador e do cliente App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="9bd5a-130">Deploying the App-V 5.1 Sequencer and Client</span></span>](deploying-the-app-v-51-sequencer-and-client.md)

 

 





