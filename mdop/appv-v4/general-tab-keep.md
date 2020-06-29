---
title: Guia Geral
description: Guia Geral
author: dansimp
ms.assetid: aeefae39-60cd-4ad4-9575-c07d7e2b1e59
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 327635422030b713aeadbc5de0007685b69e1c2e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797932"
---
# <span data-ttu-id="7735b-103">Guia Geral</span><span class="sxs-lookup"><span data-stu-id="7735b-103">General Tab</span></span>


<span data-ttu-id="7735b-104">Use a guia **geral** para configurar as opções do sequenciador do Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="7735b-104">Use the **General** tab to configure options for Microsoft Application Virtualization (App-V) Sequencer.</span></span>

<a href="" id="scratch-directory"></a>**<span data-ttu-id="7735b-105">Diretório de rascunho</span><span class="sxs-lookup"><span data-stu-id="7735b-105">Scratch Directory</span></span>**  
<span data-ttu-id="7735b-106">Especifica o caminho para o local em que o sequenciador salvará temporariamente os arquivos gerados durante o sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="7735b-106">Specifies the path to the location where the Sequencer will temporarily save files generated during sequencing.</span></span> <span data-ttu-id="7735b-107">O caminho padrão é C:\\ProgramFiles\\Microsoft Application Virtualization Sequencer\\Scratch.</span><span class="sxs-lookup"><span data-stu-id="7735b-107">The default path is C:\\ProgramFiles\\Microsoft Application Virtualization Sequencer\\Scratch.</span></span> <span data-ttu-id="7735b-108">Para especificar um novo caminho, clique em **procurar**.</span><span class="sxs-lookup"><span data-stu-id="7735b-108">To specify a new path, click **Browse**.</span></span>

<a href="" id="log-directory"></a>**<span data-ttu-id="7735b-109">Diretório de log</span><span class="sxs-lookup"><span data-stu-id="7735b-109">Log Directory</span></span>**  
<span data-ttu-id="7735b-110">Especifica o caminho para o diretório onde o sequenciador salvará os arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="7735b-110">Specifies the path to the directory where the Sequencer will save log files.</span></span> <span data-ttu-id="7735b-111">O caminho padrão é C:\\ProgramFiles\\Microsoft Application Virtualization Sequencer\\Logs.</span><span class="sxs-lookup"><span data-stu-id="7735b-111">The default path is C:\\ProgramFiles\\Microsoft Application Virtualization Sequencer\\Logs.</span></span> <span data-ttu-id="7735b-112">Para especificar um novo caminho, clique em **procurar**</span><span class="sxs-lookup"><span data-stu-id="7735b-112">To specify a new path, click **Browse**</span></span>

<a href="" id="allow-use-of-msi-installer"></a>**<span data-ttu-id="7735b-113">Permitir o uso do instalador MSI</span><span class="sxs-lookup"><span data-stu-id="7735b-113">Allow Use of MSI Installer</span></span>**  
<span data-ttu-id="7735b-114">Selecione esta opção para permitir a interação entre o sequenciador e o instalador do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7735b-114">Select this option to allow interaction between the Sequencer and the application installer.</span></span> <span data-ttu-id="7735b-115">Essa opção é selecionada por padrão.</span><span class="sxs-lookup"><span data-stu-id="7735b-115">This option is selected by default.</span></span>

<a href="" id="allow-virtualization-of-events"></a>**<span data-ttu-id="7735b-116">Permitir a virtualização de eventos</span><span class="sxs-lookup"><span data-stu-id="7735b-116">Allow Virtualization of Events</span></span>**  
<span data-ttu-id="7735b-117">Selecione esta opção para permitir que atividades de sistema operacional de baixo nível do aplicativo sejam virtualizadas quando um pacote de aplicativo sequenciado for executado em clientes de área de trabalho do App-V.</span><span class="sxs-lookup"><span data-stu-id="7735b-117">Select this option to allow low-level operating system activities of the application to be virtualized when a sequenced application package is run on App-V Desktop Clients.</span></span> <span data-ttu-id="7735b-118">Essa opção é selecionada por padrão.</span><span class="sxs-lookup"><span data-stu-id="7735b-118">This option is selected by default.</span></span>

<a href="" id="allow-virtualization-of-services"></a>**<span data-ttu-id="7735b-119">Permitir a virtualização de serviços</span><span class="sxs-lookup"><span data-stu-id="7735b-119">Allow Virtualization of Services</span></span>**  
<span data-ttu-id="7735b-120">Selecione esta opção para permitir que os serviços exigidos pelo aplicativo sejam virtualizados quando o aplicativo for executado em clientes de área de trabalho do App-V.</span><span class="sxs-lookup"><span data-stu-id="7735b-120">Select this option to allow services required by the application to be virtualized when the application is run on App-V Desktop Clients.</span></span> <span data-ttu-id="7735b-121">Essa opção é selecionada por padrão.</span><span class="sxs-lookup"><span data-stu-id="7735b-121">This option is selected by default.</span></span>

<a href="" id="append-package-version-to-filename"></a>**<span data-ttu-id="7735b-122">Acrescentar versão do pacote ao nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="7735b-122">Append Package Version to Filename</span></span>**  
<span data-ttu-id="7735b-123">Selecione esta opção para acrescentar automaticamente o número de versão do pacote do aplicativo sequenciado ao nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="7735b-123">Select this option to automatically append the sequenced application package version number to the file name.</span></span> <span data-ttu-id="7735b-124">Essa opção é selecionada por padrão.</span><span class="sxs-lookup"><span data-stu-id="7735b-124">This option is selected by default.</span></span>

<a href="" id="ok"></a>**<span data-ttu-id="7735b-125">OK</span><span class="sxs-lookup"><span data-stu-id="7735b-125">OK</span></span>**  
<span data-ttu-id="7735b-126">Salva as alterações e fecha a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7735b-126">Saves changes and closes the dialog box.</span></span>

<a href="" id="cancel"></a>**<span data-ttu-id="7735b-127">Cancelar</span><span class="sxs-lookup"><span data-stu-id="7735b-127">Cancel</span></span>**  
<span data-ttu-id="7735b-128">Sai da caixa de diálogo sem salvar as alterações.</span><span class="sxs-lookup"><span data-stu-id="7735b-128">Exits the dialog box without saving any changes.</span></span>

<a href="" id="apply"></a>**<span data-ttu-id="7735b-129">Aplicar</span><span class="sxs-lookup"><span data-stu-id="7735b-129">Apply</span></span>**  
<span data-ttu-id="7735b-130">Salva as alterações e permanece na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7735b-130">Saves the changes and remains in the dialog box.</span></span>

## <span data-ttu-id="7735b-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7735b-131">Related topics</span></span>


[<span data-ttu-id="7735b-132">Caixa de diálogo Opções do Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="7735b-132">Application Virtualization Sequencer Options Dialog Box</span></span>](application-virtualization-sequencer-options-dialog-box.md)

 

 





