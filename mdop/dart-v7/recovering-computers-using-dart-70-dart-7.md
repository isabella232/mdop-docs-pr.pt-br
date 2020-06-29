---
title: Recuperar computadores usando o DaRT 7.0
description: Recuperar computadores usando o DaRT 7.0
author: dansimp
ms.assetid: bcded7ca-237b-4971-ac34-4394b05cbc50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 44dd48146155294bd8013b4b5a9bf23ffb3e8316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799138"
---
# <span data-ttu-id="d632a-103">Recuperar computadores usando o DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="d632a-103">Recovering Computers Using DaRT 7.0</span></span>


<span data-ttu-id="d632a-104">Há dois métodos disponíveis para recuperar computadores usando o Microsoft Diagnostics e o conjunto de ferramentas de recuperação (DaRT) 7.</span><span class="sxs-lookup"><span data-stu-id="d632a-104">There are two methods available to recover computers using Microsoft Diagnostics and Recovery Toolset (DaRT)7.</span></span> <span data-ttu-id="d632a-105">Você pode executar a imagem de recuperação do DaRT7 localmente ou usar o recurso conexão remota disponível no DaRT7 para recuperar um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="d632a-105">You can either run the DaRT7 recovery image locally or use The Remote Connection feature available in DaRT7 to recover a remote computer.</span></span> <span data-ttu-id="d632a-106">Os dois métodos são descritos com mais detalhes nesta seção.</span><span class="sxs-lookup"><span data-stu-id="d632a-106">Both methods are described in more detail in this section.</span></span>

## <span data-ttu-id="d632a-107">Recuperar computadores locais usando a imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="d632a-107">Recover Local Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="d632a-108">Para recuperar um computador local usando o DaRT7, você deve estar fisicamente presente no computador do usuário final que está apresentando problemas que exijam o DaRT.</span><span class="sxs-lookup"><span data-stu-id="d632a-108">To recover a local computer by using DaRT7, you must be physically present at the end-user computer that is experiencing problems that require DaRT.</span></span>

<span data-ttu-id="d632a-109">Você tem vários métodos diferentes para escolher para inicializar o DaRT, dependendo de como você implanta a imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="d632a-109">You have several different methods to choose from to boot into DaRT, depending on how you deploy the DaRT recovery image.</span></span>

-   <span data-ttu-id="d632a-110">Insira um CD, DVD ou unidade flash USB para a imagem de recuperação do DaRT no computador com problema e use-o para inicializar no computador.</span><span class="sxs-lookup"><span data-stu-id="d632a-110">Insert a DaRT recovery image CD, DVD, or USB flash drive into the problem computer and use it to boot into the computer.</span></span>

-   <span data-ttu-id="d632a-111">Inicialize no DaRT a partir de uma partição de recuperação no computador problemático.</span><span class="sxs-lookup"><span data-stu-id="d632a-111">Boot into DaRT from a recovery partition on the problem computer.</span></span>

-   <span data-ttu-id="d632a-112">Inicialize no DaRT a partir de uma partição remota na rede.</span><span class="sxs-lookup"><span data-stu-id="d632a-112">Boot into DaRT from a remote partition on the network.</span></span>

<span data-ttu-id="d632a-113">Para obter informações sobre as vantagens e desvantagens de cada método, consulte [planejar como salvar e implantar a imagem de recuperação do DaRT 7,0](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="d632a-113">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 7.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span></span>

<span data-ttu-id="d632a-114">Seja qual for o método que você usa para inicializar o DaRT, você deve habilitar o dispositivo de inicialização no BIOS para as opções de inicialização ou as opções que você deseja disponibilizar para o usuário final.</span><span class="sxs-lookup"><span data-stu-id="d632a-114">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

<span data-ttu-id="d632a-115">**Observação**  A configuração do BIOS é exclusiva, dependendo do tipo de unidade de disco rígido, adaptadores de rede e outros tipos de hardware usados em sua organização.</span><span class="sxs-lookup"><span data-stu-id="d632a-115">**Note** Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>

 

[<span data-ttu-id="d632a-116">Como recuperar computadores locais usando a imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="d632a-116">How to Recover Local Computers Using the DaRT Recovery Image</span></span>](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md)

## <span data-ttu-id="d632a-117">Recuperar computadores remotos usando a imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="d632a-117">Recover Remote Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="d632a-118">O recurso conexão remota no DaRT permite que um administrador de ti execute as ferramentas do DaRT remotamente em um computador de usuário final.</span><span class="sxs-lookup"><span data-stu-id="d632a-118">The Remote Connection feature in DaRT lets an IT administrator run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="d632a-119">Depois que determinadas informações forem fornecidas pelo usuário final (ou por um profissional de assistência técnica em funcionamento no computador do usuário final), o administrador de ti ou o agente de helpdesk poderá assumir o controle do computador do usuário final e executar as ferramentas do DaRT necessárias remotamente.</span><span class="sxs-lookup"><span data-stu-id="d632a-119">After certain information is provided by the end user (or by a helpdesk professional working on the end-user computer), the IT administrator or helpdesk agent can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

<span data-ttu-id="d632a-120">**Importante**  Os dois computadores que estabelecem uma conexão remota devem fazer parte da mesma rede.</span><span class="sxs-lookup"><span data-stu-id="d632a-120">**Important** The two computers establishing a remote connection must be part of the same network.</span></span>

 

<span data-ttu-id="d632a-121">A janela **diagnóstico e recuperação do conjunto de ferramentas de recuperação** inclui a opção para executar o DART em um computador de usuário final remotamente a partir de um computador administrador.</span><span class="sxs-lookup"><span data-stu-id="d632a-121">The **Diagnostics and Recovery Toolset** window includes the option to run DaRT on an end-user computer remotely from an administrator computer.</span></span> <span data-ttu-id="d632a-122">O usuário final abre as ferramentas DaRT no computador problemático e inicia a sessão remota clicando em **conexão remota**.</span><span class="sxs-lookup"><span data-stu-id="d632a-122">The end user opens the DaRT tools on the problem computer and starts the remote session by clicking **Remote Connection**.</span></span>

<span data-ttu-id="d632a-123">O recurso conexão remota no computador do usuário final cria as seguintes informações de conexão: um número de tíquete, uma porta e uma lista de todos os endereços IP disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d632a-123">The Remote Connection feature on the end-user computer creates the following connection information: a ticket number, a port, and a list of all available IP addresses.</span></span> <span data-ttu-id="d632a-124">O número do bilhete e a porta são gerados aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="d632a-124">The ticket number and port are generated randomly.</span></span>

<span data-ttu-id="d632a-125">O administrador de ti ou o agente de assistência técnica insere essas informações no **Visualizador de conexão remota do DART** para estabelecer a conexão de serviços de terminal com o computador do usuário final.</span><span class="sxs-lookup"><span data-stu-id="d632a-125">The IT administrator or helpdesk agent enters this information into the **DaRT Remote Connection Viewer** to establish the terminal services connection to the end-user computer.</span></span> <span data-ttu-id="d632a-126">A conexão de serviços de terminal que é estabelecida permite que um administrador de ti interaja remotamente com as ferramentas do DaRT no computador do usuário final.</span><span class="sxs-lookup"><span data-stu-id="d632a-126">The terminal services connection that is established lets an IT administrator remotely interact with the DaRT tools on the end-user computer.</span></span> <span data-ttu-id="d632a-127">Em seguida, o computador do usuário final processa as informações de conexão, compartilha sua tela e responde às instruções do computador do administrador de ti.</span><span class="sxs-lookup"><span data-stu-id="d632a-127">The end-user computer then processes the connection information, shares its screen, and responds to instructions from the IT administrator computer.</span></span>

[<span data-ttu-id="d632a-128">Como recuperar computadores remotos usando a imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="d632a-128">How to Recover Remote Computers Using the DaRT Recovery Image</span></span>](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md)

## <span data-ttu-id="d632a-129">Outros recursos para recuperar computadores usando o DaRT7</span><span class="sxs-lookup"><span data-stu-id="d632a-129">Other resources for recovering computers using DaRT7</span></span>


[<span data-ttu-id="d632a-130">Operações do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="d632a-130">Operations for DaRT 7.0</span></span>](operations-for-dart-70-new-ia.md)

 

 





