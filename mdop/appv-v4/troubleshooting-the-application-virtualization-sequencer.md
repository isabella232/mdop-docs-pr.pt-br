---
title: Solução de problemas do Application Virtualization Sequencer
description: Solução de problemas do Application Virtualization Sequencer
author: dansimp
ms.assetid: 12ea8367-0b84-44e1-a885-e0539486556b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60c47b853c74d90afc21e9ca172c0eec2a2c7a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796674"
---
# <span data-ttu-id="19c83-103">Solução de problemas do Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="19c83-103">Troubleshooting the Application Virtualization Sequencer</span></span>


<span data-ttu-id="19c83-104">Este tópico inclui informações que você pode usar para ajudar a solucionar problemas gerais no sequenciador do Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="19c83-104">This topic includes information that you can use to help troubleshoot general issues on the Application Virtualization (App-V) Sequencer.</span></span>

## <span data-ttu-id="19c83-105">A criação de um arquivo SFTD usando o sequenciador App-V aumenta o número da versão inesperadamente</span><span class="sxs-lookup"><span data-stu-id="19c83-105">Creating an SFTD File by Using the App-V Sequencer Increases the Version Number Unexpectedly</span></span>


<span data-ttu-id="19c83-106">O número de versão associado a um arquivo SFTD aumenta inesperadamente.</span><span class="sxs-lookup"><span data-stu-id="19c83-106">The version number associated with an SFTD file increases unexpectedly.</span></span>

**<span data-ttu-id="19c83-107">Solução</span><span class="sxs-lookup"><span data-stu-id="19c83-107">Solution</span></span>**

<span data-ttu-id="19c83-108">Use a linha de comando para gerar um novo arquivo. SFT.</span><span class="sxs-lookup"><span data-stu-id="19c83-108">Use the command line to generate a new .sft file.</span></span> <span data-ttu-id="19c83-109">Para criar o arquivo. sft usando a linha de comando, digite o seguinte em um prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="19c83-109">To create the .sft file by using the command line, enter the following at a command prompt:</span></span>

**<span data-ttu-id="19c83-110">&lt;Nome do arquivo SFT base mkdiffpkg.exe nome do arquivo &gt; &lt; SFT do SFT&gt;</span><span class="sxs-lookup"><span data-stu-id="19c83-110">mkdiffpkg.exe &lt;base SFT file name&gt; &lt;diff SFT file name&gt;</span></span>**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a><span data-ttu-id="19c83-111">O nome do arquivo no arquivo OSD não está correto após a atualização do pacote</span><span class="sxs-lookup"><span data-stu-id="19c83-111">File Name in OSD File Is Not Correct After Package Upgrade</span></span>


<span data-ttu-id="19c83-112">Depois de atualizar um pacote existente, o nome do arquivo não está correto.</span><span class="sxs-lookup"><span data-stu-id="19c83-112">After you upgrade an existing package, the file name is not correct.</span></span>

**<span data-ttu-id="19c83-113">Solução</span><span class="sxs-lookup"><span data-stu-id="19c83-113">Solution</span></span>**

<span data-ttu-id="19c83-114">Ao abrir um pacote para atualização, você deve especificar a unidade Q:\\ raiz como o local de saída do pacote.</span><span class="sxs-lookup"><span data-stu-id="19c83-114">When you open a package for upgrade, you should specify the root Q:\\ drive as the output location for the package.</span></span> <span data-ttu-id="19c83-115">Não especifique um nome de arquivo associado com o local de saída.</span><span class="sxs-lookup"><span data-stu-id="19c83-115">Do not specify an associated file name with the output location.</span></span>

## <span data-ttu-id="19c83-116">A instalação padrão do Microsoft Word2003 resulta em um erro quando transmitido para um cliente</span><span class="sxs-lookup"><span data-stu-id="19c83-116">Microsoft Word2003 Default Install Results in an Error When Streamed to a Client</span></span>


<span data-ttu-id="19c83-117">Quando você transmite o Microsoft Word2003 para um cliente, um erro é retornado, mas o Microsoft Word continua a ser executado.</span><span class="sxs-lookup"><span data-stu-id="19c83-117">When you stream Microsoft Word2003 to a client, an error is returned but Microsoft Word continues to run.</span></span>

**<span data-ttu-id="19c83-118">Solução</span><span class="sxs-lookup"><span data-stu-id="19c83-118">Solution</span></span>**

<span data-ttu-id="19c83-119">Resequenciar o pacote de aplicativo virtual e selecionar **instalação completa**.</span><span class="sxs-lookup"><span data-stu-id="19c83-119">Resequence the virtual application package, and select **Full Install**.</span></span>

## <span data-ttu-id="19c83-120">A atualização do pacote não funciona quando você cria um pacote dependente</span><span class="sxs-lookup"><span data-stu-id="19c83-120">Package Upgrade Does Not Work When You Create a Dependent Package</span></span>


<span data-ttu-id="19c83-121">Quando você cria um pacote dependente usando a atualização de pacote e adiciona novas entradas do registro, parece funcionar corretamente, mas as entradas do registro atualizadas não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="19c83-121">When you create a dependent package by using package upgrade and add new registry entries, it appears to function correctly but the updated registry entries are not available.</span></span>

**<span data-ttu-id="19c83-122">Solução</span><span class="sxs-lookup"><span data-stu-id="19c83-122">Solution</span></span>**

<span data-ttu-id="19c83-123">As configurações do registro são sempre armazenadas com a versão original do pacote, portanto, as atualizações para o pacote não parecerão estar disponíveis, a menos que você repare o pacote original.</span><span class="sxs-lookup"><span data-stu-id="19c83-123">Registry settings are always stored with the original version of the package, so updates to the package will not appear to be available unless you repair the original package.</span></span>

## <span data-ttu-id="19c83-124">Erro ao tentar sequenciar. NET 2.0</span><span class="sxs-lookup"><span data-stu-id="19c83-124">Error When Trying to Sequence .NET2.0</span></span>


<span data-ttu-id="19c83-125">Quando você sequenciar um pacote que exija. NET 2.0, você recebe um erro.</span><span class="sxs-lookup"><span data-stu-id="19c83-125">When you sequence a package that requires .NET2.0, you get an error.</span></span>

**<span data-ttu-id="19c83-126">Solução</span><span class="sxs-lookup"><span data-stu-id="19c83-126">Solution</span></span>**

<span data-ttu-id="19c83-127">Sequenciando pacotes que exigem. Não há suporte para NET 2.0.</span><span class="sxs-lookup"><span data-stu-id="19c83-127">Sequencing packages that require .NET2.0 is not supported.</span></span>

## <span data-ttu-id="19c83-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="19c83-128">Related topics</span></span>


[<span data-ttu-id="19c83-129">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="19c83-129">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





