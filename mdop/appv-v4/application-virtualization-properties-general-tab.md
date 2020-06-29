---
title: Guia geral de propriedades da virtualização de aplicativos
description: Guia geral de propriedades da virtualização de aplicativos
author: dansimp
ms.assetid: be7449d9-171a-4a11-9382-83b7008ccbdd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ee00bfc7f70ee7b17da42aad61356540a7a0be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797575"
---
# <span data-ttu-id="d04b2-103">Propriedades do Application Virtualization: guia Geral</span><span class="sxs-lookup"><span data-stu-id="d04b2-103">Application Virtualization Properties: General Tab</span></span>


<span data-ttu-id="d04b2-104">Use a guia **geral** da caixa de diálogo **Propriedades do Application Virtualization** para modificar as configurações de log e locais de dados.</span><span class="sxs-lookup"><span data-stu-id="d04b2-104">Use the **General** tab of the **Application Virtualization Properties** dialog box to modify log settings and data locations.</span></span>

<span data-ttu-id="d04b2-105">Esta guia contém os elementos a seguir.</span><span class="sxs-lookup"><span data-stu-id="d04b2-105">This tab contains the following elements.</span></span>

<a href="" id="log-level"></a>**<span data-ttu-id="d04b2-106">Nível de log</span><span class="sxs-lookup"><span data-stu-id="d04b2-106">Log Level</span></span>**  
<span data-ttu-id="d04b2-107">Selecione o nível na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="d04b2-107">Select the level from the drop-down list.</span></span> <span data-ttu-id="d04b2-108">O nível padrão é **informações**.</span><span class="sxs-lookup"><span data-stu-id="d04b2-108">The default level is **Information**.</span></span>

<a href="" id="reset-log"></a>**<span data-ttu-id="d04b2-109">Redefinir log</span><span class="sxs-lookup"><span data-stu-id="d04b2-109">Reset Log</span></span>**  
<span data-ttu-id="d04b2-110">Clique neste botão para fazer backup do arquivo de log atual e iniciar imediatamente um novo arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="d04b2-110">Click this button to back up the current log file and immediately start a new log file.</span></span>

<a href="" id="location"></a>**<span data-ttu-id="d04b2-111">Localização</span><span class="sxs-lookup"><span data-stu-id="d04b2-111">Location</span></span>**  
<span data-ttu-id="d04b2-112">Digite ou navegue até o local onde você deseja salvar o arquivo de log sftlog.txt.</span><span class="sxs-lookup"><span data-stu-id="d04b2-112">Enter or browse to the location where you want to save the log file sftlog.txt.</span></span> <span data-ttu-id="d04b2-113">Os locais padrão são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="d04b2-113">The default locations are as follows:</span></span>

-   <span data-ttu-id="d04b2-114">Para WindowsXP, Windows Server2003-*C:\\Documents e Settings\\All Users\\Application cliente de virtualização do Data\\Microsoft\\Application*</span><span class="sxs-lookup"><span data-stu-id="d04b2-114">For WindowsXP, Windows Server2003—*C:\\Documents and Settings\\All Users\\Application Data\\Microsoft\\Application Virtualization Client*</span></span>

-   <span data-ttu-id="d04b2-115">Para Windows Vista, Windows 7, Windows Server2008 —*cliente de virtualização C:\\ProgramData\\Microsoft\\Application*</span><span class="sxs-lookup"><span data-stu-id="d04b2-115">For Windows Vista, Windows 7, Windows Server2008—*C:\\ProgramData\\Microsoft\\Application Virtualization Client*</span></span>

<a href="" id="system-log-level"></a>**<span data-ttu-id="d04b2-116">Nível de log do sistema</span><span class="sxs-lookup"><span data-stu-id="d04b2-116">System Log Level</span></span>**  
<span data-ttu-id="d04b2-117">Selecione o nível na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="d04b2-117">Select the level from the drop-down list.</span></span> <span data-ttu-id="d04b2-118">O nível padrão é **aviso**.</span><span class="sxs-lookup"><span data-stu-id="d04b2-118">The default level is **Warning**.</span></span>

<span data-ttu-id="d04b2-119">**Observação**  A configuração de **nível de log do sistema** controla o nível de mensagens enviadas ao log de eventos do sistema.</span><span class="sxs-lookup"><span data-stu-id="d04b2-119">**Note** The **System Log Level** setting controls the level of messages sent to the system event log.</span></span> <span data-ttu-id="d04b2-120">As mensagens registradas são idênticas às mensagens que são registradas no log de eventos do cliente, mas elas são armazenadas em um local diferente, que não tem as limitações de espaço do log de eventos do cliente.</span><span class="sxs-lookup"><span data-stu-id="d04b2-120">The logged messages are identical to the messages that get logged to the client event log, but they are stored in a different location that does not have the space limitations of the client event log.</span></span> <span data-ttu-id="d04b2-121">Como o log de eventos do sistema não tem limitações de espaço, ele é ideal para situações em que o registro em log detalhado é necessário.</span><span class="sxs-lookup"><span data-stu-id="d04b2-121">Because the system event log does not have space limitations, it is ideally suited for situations where verbose logging is necessary.</span></span>

 

<a href="" id="global-data-directory"></a>**<span data-ttu-id="d04b2-122">Diretório de dados globais</span><span class="sxs-lookup"><span data-stu-id="d04b2-122">Global Data Directory</span></span>**  
<span data-ttu-id="d04b2-123">Digite ou navegue até o local do diretório do arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="d04b2-123">Enter or browse to the location of the directory of the log file.</span></span> <span data-ttu-id="d04b2-124">Os locais padrão são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="d04b2-124">The default locations are as follows:</span></span>

-   <span data-ttu-id="d04b2-125">Para WindowsXP, Windows Server2003-*C:\\Documents e Settings\\All Users\\Application cliente de virtualização do Data\\Microsoft\\Application*</span><span class="sxs-lookup"><span data-stu-id="d04b2-125">For WindowsXP, Windows Server2003—*C:\\Documents and Settings\\All Users\\Application Data\\Microsoft\\Application Virtualization Client*</span></span>

-   <span data-ttu-id="d04b2-126">Para Windows Vista, Windows 7, Windows Server2008 —*cliente de virtualização C:\\ProgramData\\Microsoft\\Application*</span><span class="sxs-lookup"><span data-stu-id="d04b2-126">For Windows Vista, Windows 7, Windows Server2008—*C:\\ProgramData\\Microsoft\\Application Virtualization Client*</span></span>

<a href="" id="user-data-directory"></a>**<span data-ttu-id="d04b2-127">Diretório de dados do usuário</span><span class="sxs-lookup"><span data-stu-id="d04b2-127">User Data Directory</span></span>**  
<span data-ttu-id="d04b2-128">Digite ou navegue até o local do diretório onde os dados específicos do usuário estão armazenados.</span><span class="sxs-lookup"><span data-stu-id="d04b2-128">Enter or browse to the location of the directory where user-specific data is stored.</span></span> <span data-ttu-id="d04b2-129">O padrão é% APPDATA%.</span><span class="sxs-lookup"><span data-stu-id="d04b2-129">The default is %APPDATA%.</span></span> <span data-ttu-id="d04b2-130">Esse caminho deve ser uma variável de ambiente válida no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="d04b2-130">This path must be a valid environment variable on the client computer.</span></span>

## <span data-ttu-id="d04b2-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d04b2-131">Related topics</span></span>


[<span data-ttu-id="d04b2-132">Client Management Console: propriedades do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="d04b2-132">Client Management Console: Application Virtualization Properties</span></span>](client-management-console-application-virtualization-properties.md)

 

 





