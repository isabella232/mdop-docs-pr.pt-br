---
title: Como implantar o App-V 4,6 e o cliente do App-V 5,0 no mesmo computador
description: Como implantar o App-V 4,6 e o cliente do App-V 5,0 no mesmo computador
ms.assetid: 5b7e27e4-4360-464c-b832-f1c7939e5485
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.date: 06/21/2016
ms.openlocfilehash: 38e77ce6ce6c0dba7c67f6c0dfa5c9e263e07e20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796435"
---
# <span data-ttu-id="57029-103">Como implantar o App-V 4,6 e o cliente do App-V 5,0 no mesmo computador</span><span class="sxs-lookup"><span data-stu-id="57029-103">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</span></span>

<span data-ttu-id="57029-104">**Observação:** O App-V 4,6 tem saído do suporte básico.</span><span class="sxs-lookup"><span data-stu-id="57029-104">**Note:** App-V 4.6 has exited Mainstream support.</span></span> <span data-ttu-id="57029-105">O seguinte pressupõe que o cliente App-V 4,6 SP3 já está instalado.</span><span class="sxs-lookup"><span data-stu-id="57029-105">The following assumes that the App-V 4.6 SP3 client is already installed.</span></span>

<span data-ttu-id="57029-106">Use as informações a seguir para instalar o cliente do App-V 5,0 (de preferência, com os service packs e hotfixes mais recentes) e o aplicativo App-V 4.6 SP3 no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="57029-106">Use the following information to install the App-V 5.0 client (preferably, with the latest Service Packs and hotfixes) and the App-V 4.6SP3 client on the same computer.</span></span> <span data-ttu-id="57029-107">Para obter as versões, os requisitos e outras informações de planejamento compatíveis, consulte [planejando a migração de uma versão anterior do App-V](planning-for-migrating-from-a-previous-version-of-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="57029-107">For supported versions, requirements, and other planning information, see [Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md).</span></span>

**<span data-ttu-id="57029-108">Para implantar o cliente do App-V 5,0 e o aplicativo do App-V 4,6 no mesmo computador</span><span class="sxs-lookup"><span data-stu-id="57029-108">To deploy the App-V 5.0 client and App-V 4.6 client on the same computer</span></span>**

1.  <span data-ttu-id="57029-109">Instale o cliente do App-V 5,0 SP3 no computador que está executando a versão do App-V 4,6 do cliente.</span><span class="sxs-lookup"><span data-stu-id="57029-109">Install the App-V 5.0 SP3 client on the computer that is running the App-V 4.6 version of the client.</span></span> <span data-ttu-id="57029-110">Para obter melhores resultados, recomendamos que você instale todas as atualizações disponíveis para o cliente App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="57029-110">For best results, we recommend that you install all available updates to the App-V 5.0 SP3 client.</span></span>

2.  <span data-ttu-id="57029-111">Converter ou resequenciar os pacotes gradualmente.</span><span class="sxs-lookup"><span data-stu-id="57029-111">Convert or re-sequence the packages gradually.</span></span>

    -   <span data-ttu-id="57029-112">Para converter os pacotes, use o conversor de pacotes do App-V 5,0 e converta os pacotes necessários para o formato de arquivo do App-V 5,0 (**. AppV**).</span><span class="sxs-lookup"><span data-stu-id="57029-112">To convert the packages, use the App-V 5.0 package converter and convert the required packages to the App-V 5.0 (**.appv**) file format.</span></span>

    -   <span data-ttu-id="57029-113">Para resequenciar os pacotes, considere usar a versão mais recente do sequenciador para obter os melhores resultados.</span><span class="sxs-lookup"><span data-stu-id="57029-113">To re-sequence the packages, consider using the latest version of the Sequencer for best results.</span></span>

    <span data-ttu-id="57029-114">Para obter mais informações sobre como publicar pacotes, consulte [como publicar um pacote usando o console de gerenciamento](how-to-publish-a-package-by-using-the-management-console-50.md).</span><span class="sxs-lookup"><span data-stu-id="57029-114">For more information about publishing packages, see [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md).</span></span>

3.  <span data-ttu-id="57029-115">Implantar pacotes nos computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="57029-115">Deploy packages to the client computers.</span></span>

4.  <span data-ttu-id="57029-116">Converta os pontos de extensão, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="57029-116">Convert extension points, as needed.</span></span> <span data-ttu-id="57029-117">Para obter mais informações, consulte os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="57029-117">For more information, see the following resources:</span></span>

    -   [<span data-ttu-id="57029-118">Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.0 convertido para todos os usuários em um computador específico</span><span class="sxs-lookup"><span data-stu-id="57029-118">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

    -   [<span data-ttu-id="57029-119">Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.0 para um usuário específico</span><span class="sxs-lookup"><span data-stu-id="57029-119">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

    -   [<span data-ttu-id="57029-120">Como converter um pacote criado em uma versão anterior do App-V</span><span class="sxs-lookup"><span data-stu-id="57029-120">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

5.  <span data-ttu-id="57029-121">Teste se seus pacotes do App-V 5,0 foram bem-sucedidos e, em seguida, remova os pacotes do 4,6.</span><span class="sxs-lookup"><span data-stu-id="57029-121">Test that your App-V 5.0 packages are successful, and then remove the 4.6 packages.</span></span> <span data-ttu-id="57029-122">Para verificar o estado do usuário dos seus computadores cliente, recomendamos que você use a [virtualização da experiência do usuário](https://technet.microsoft.com/library/dn458947.aspx) ou outra ferramenta de gerenciamento do ambiente do usuário.</span><span class="sxs-lookup"><span data-stu-id="57029-122">To check the user state of your client computers, we recommend that you use [User Experience Virtualization](https://technet.microsoft.com/library/dn458947.aspx) or another user environment management tool.</span></span>

    <span data-ttu-id="57029-123">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="57029-123">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="57029-124">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="57029-124">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="57029-125">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="57029-125">Got an App-V issue?</span></span>** <span data-ttu-id="57029-126">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="57029-126">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="57029-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="57029-127">Related topics</span></span>


[<span data-ttu-id="57029-128">Planejamento para a migração de uma versão anterior do App-V</span><span class="sxs-lookup"><span data-stu-id="57029-128">Planning for Migrating from a Previous Version of App-V</span></span>](planning-for-migrating-from-a-previous-version-of-app-v.md)

[<span data-ttu-id="57029-129">Implantação do sequenciador e do cliente App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="57029-129">Deploying the App-V 5.0 Sequencer and Client</span></span>](deploying-the-app-v-50-sequencer-and-client.md)

 

 





