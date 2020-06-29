---
title: Recuperar computadores usando o DaRT 8.0
description: Recuperar computadores usando o DaRT 8.0
author: dansimp
ms.assetid: 0caeb7d9-c1e6-4f32-bc27-157b91630989
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39bab02488252b53deb971d35bc6872c0a2df73b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799558"
---
# <span data-ttu-id="124b6-103">Recuperar computadores usando o DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="124b6-103">Recovering Computers Using DaRT 8.0</span></span>


<span data-ttu-id="124b6-104">Após implantar a imagem de recuperação do Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0, você pode usar o DaRT 8,0 para recuperar computadores.</span><span class="sxs-lookup"><span data-stu-id="124b6-104">After deploying the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 recovery image, you can use DaRT 8.0 to recover computers.</span></span> <span data-ttu-id="124b6-105">As informações nesta seção descrevem as tarefas de recuperação que você pode executar.</span><span class="sxs-lookup"><span data-stu-id="124b6-105">The information in this section describes the recovery tasks that you can perform.</span></span>

<span data-ttu-id="124b6-106">Você tem vários métodos diferentes para escolher para inicializar o DaRT, dependendo de como você implanta a imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="124b6-106">You have several different methods to choose from to boot into DaRT, depending on how you deploy the DaRT recovery image.</span></span>

-   <span data-ttu-id="124b6-107">Insira um CD, DVD ou unidade flash USB para a imagem de recuperação do DaRT no computador com problema e use-o para inicializar no computador.</span><span class="sxs-lookup"><span data-stu-id="124b6-107">Insert a DaRT recovery image CD, DVD, or USB flash drive into the problem computer and use it to boot into the computer.</span></span>

-   <span data-ttu-id="124b6-108">Inicialize no DaRT a partir de uma partição de recuperação no computador problemático.</span><span class="sxs-lookup"><span data-stu-id="124b6-108">Boot into DaRT from a recovery partition on the problem computer.</span></span>

-   <span data-ttu-id="124b6-109">Inicialize no DaRT a partir de uma partição remota na rede.</span><span class="sxs-lookup"><span data-stu-id="124b6-109">Boot into DaRT from a remote partition on the network.</span></span>

<span data-ttu-id="124b6-110">Para obter informações sobre as vantagens e desvantagens de cada método, consulte [planejar como salvar e implantar a imagem de recuperação do DaRT 8,0](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="124b6-110">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 8.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="124b6-111">Seja qual for o método que você usa para inicializar o DaRT, você deve habilitar o dispositivo de inicialização no BIOS para as opções de inicialização ou as opções que você deseja disponibilizar para o usuário final.</span><span class="sxs-lookup"><span data-stu-id="124b6-111">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

<span data-ttu-id="124b6-112">**Observação**  A configuração do BIOS é exclusiva, dependendo do tipo de unidade de disco rígido, adaptadores de rede e outros tipos de hardware usados em sua organização.</span><span class="sxs-lookup"><span data-stu-id="124b6-112">**Note** Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>

 

## <span data-ttu-id="124b6-113">Recuperar um computador local usando a imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="124b6-113">Recover a local computer by using the DaRT recovery image</span></span>


<span data-ttu-id="124b6-114">Para recuperar um computador local usando o DaRT, você deve estar fisicamente presente no computador do usuário final que está tendo problemas que exijam o DaRT.</span><span class="sxs-lookup"><span data-stu-id="124b6-114">To recover a local computer by using DaRT, you must be physically present at the end-user computer that is experiencing problems that require DaRT.</span></span>

[<span data-ttu-id="124b6-115">Como recuperar computadores locais usando a imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="124b6-115">How to Recover Local Computers by Using the DaRT Recovery Image</span></span>](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-8.md)

## <span data-ttu-id="124b6-116">Recuperar um computador remoto usando a imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="124b6-116">Recover a remote computer by using the DaRT recovery image</span></span>


<span data-ttu-id="124b6-117">O recurso conexão remota no DaRT permite que um administrador de ti execute as ferramentas do DaRT remotamente em um computador de usuário final.</span><span class="sxs-lookup"><span data-stu-id="124b6-117">The Remote Connection feature in DaRT lets an IT administrator run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="124b6-118">Depois que determinadas informações são fornecidas pelo usuário final (ou por um profissional de suporte técnico trabalhando no computador do usuário final), o administrador de ti ou o trabalhador de suporte técnico pode assumir o controle do computador do usuário final e executar as ferramentas do DaRT necessárias remotamente.</span><span class="sxs-lookup"><span data-stu-id="124b6-118">After certain information is provided by the end user (or by a help desk professional working on the end-user computer), the IT administrator or help desk worker can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

<span data-ttu-id="124b6-119">**Importante**  Os dois computadores que estabelecem uma conexão remota devem fazer parte da mesma rede.</span><span class="sxs-lookup"><span data-stu-id="124b6-119">**Important** The two computers establishing a remote connection must be part of the same network.</span></span>

 

<span data-ttu-id="124b6-120">A janela **diagnóstico e recuperação do conjunto de ferramentas de recuperação** inclui a opção para executar o DART em um computador de usuário final remotamente a partir de um computador administrador.</span><span class="sxs-lookup"><span data-stu-id="124b6-120">The **Diagnostics and Recovery Toolset** window includes the option to run DaRT on an end-user computer remotely from an administrator computer.</span></span> <span data-ttu-id="124b6-121">O usuário final abre as ferramentas DaRT no computador problemático e inicia a sessão remota clicando em **conexão remota**.</span><span class="sxs-lookup"><span data-stu-id="124b6-121">The end user opens the DaRT tools on the problem computer and starts the remote session by clicking **Remote Connection**.</span></span>

<span data-ttu-id="124b6-122">O recurso conexão remota no computador do usuário final cria as seguintes informações de conexão: um número de tíquete, uma porta e uma lista de todos os endereços IP disponíveis.</span><span class="sxs-lookup"><span data-stu-id="124b6-122">The Remote Connection feature on the end-user computer creates the following connection information: a ticket number, a port, and a list of all available IP addresses.</span></span> <span data-ttu-id="124b6-123">O número do bilhete e a porta são gerados aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="124b6-123">The ticket number and port are generated randomly.</span></span>

<span data-ttu-id="124b6-124">O administrador de ti ou o trabalho de suporte técnico insere essas informações no **Visualizador de conexão remota do DART** para estabelecer a conexão de serviços de terminal com o computador do usuário final.</span><span class="sxs-lookup"><span data-stu-id="124b6-124">The IT administrator or help desk worker enters this information into the **DaRT Remote Connection Viewer** to establish the terminal services connection to the end-user computer.</span></span> <span data-ttu-id="124b6-125">A conexão de serviços de terminal que é estabelecida permite que um administrador de ti interaja remotamente com as ferramentas do DaRT no computador do usuário final.</span><span class="sxs-lookup"><span data-stu-id="124b6-125">The terminal services connection that is established lets an IT administrator remotely interact with the DaRT tools on the end-user computer.</span></span> <span data-ttu-id="124b6-126">Em seguida, o computador do usuário final processa as informações de conexão, compartilha sua tela e responde às instruções do computador do administrador de ti.</span><span class="sxs-lookup"><span data-stu-id="124b6-126">The end-user computer then processes the connection information, shares its screen, and responds to instructions from the IT administrator computer.</span></span>

[<span data-ttu-id="124b6-127">Como recuperar computadores remotos usando a imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="124b6-127">How to Recover Remote Computers by Using the DaRT Recovery Image</span></span>](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-8.md)

## <span data-ttu-id="124b6-128">Outros recursos para recuperar computadores usando o DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="124b6-128">Other resources for recovering computers using DaRT 8.0</span></span>


[<span data-ttu-id="124b6-129">Operações do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="124b6-129">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

 

 





