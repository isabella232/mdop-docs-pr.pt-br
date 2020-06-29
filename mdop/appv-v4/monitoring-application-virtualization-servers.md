---
title: Monitorando Application Virtualization Servers
description: Monitorando Application Virtualization Servers
author: dansimp
ms.assetid: d84355ae-4fe4-41d9-ac3a-3eaa32d9a61f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a53c0c37ca609c701727a7f4e18019a9f20110ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796866"
---
# <span data-ttu-id="87f65-103">Monitorando Application Virtualization Servers</span><span class="sxs-lookup"><span data-stu-id="87f65-103">Monitoring Application Virtualization Servers</span></span>


<span data-ttu-id="87f65-104">Para simplificar o gerenciamento do servidor do Application Virtualization (App-V), você pode usar o pacote de gerenciamento do Manager2007 de operações do System Center.</span><span class="sxs-lookup"><span data-stu-id="87f65-104">To simplify Application Virtualization (App-V) Server management, you can use the System Center Operations Manager2007 Management Pack.</span></span> <span data-ttu-id="87f65-105">Este pacote de gerenciamento oferece suporte somente a servidores do Application Virtualization (App-V) 4,5; Ele não é compatível com versões anteriores do servidor.</span><span class="sxs-lookup"><span data-stu-id="87f65-105">This Management Pack supports only Application Virtualization (App-V) 4.5 servers; it does not support previous server versions.</span></span> <span data-ttu-id="87f65-106">O pacote de gerenciamento maximiza a disponibilidade do App-V Server para manipular solicitações do cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="87f65-106">The Management Pack maximizes App-V Server availability for handling App-V Client requests.</span></span>

## <span data-ttu-id="87f65-107">Indicadores de status</span><span class="sxs-lookup"><span data-stu-id="87f65-107">Status Indicators</span></span>


<span data-ttu-id="87f65-108">Os indicadores de status de integridade do App-V Server são codificados por cor.</span><span class="sxs-lookup"><span data-stu-id="87f65-108">The App-V Server health status indicators are color-coded.</span></span> <span data-ttu-id="87f65-109">As cores representam os seguintes valores de status:</span><span class="sxs-lookup"><span data-stu-id="87f65-109">The colors represent the following status values:</span></span>

-   <span data-ttu-id="87f65-110">Sem cor indica que o servidor está em execução sem erros não recuperáveis.</span><span class="sxs-lookup"><span data-stu-id="87f65-110">No color indicates that the server is running without non-recoverable errors.</span></span>

-   <span data-ttu-id="87f65-111">Amarelo indica que um dos componentes não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="87f65-111">Yellow indicates that one of the components is not functioning correctly.</span></span> <span data-ttu-id="87f65-112">A funcionalidade geral do servidor está degradada, mas o servidor ainda está disponível.</span><span class="sxs-lookup"><span data-stu-id="87f65-112">The overall functionality of the server is degraded, but the server is still available.</span></span>

-   <span data-ttu-id="87f65-113">Vermelho indica que o servidor não está disponível e que não pode fornecer serviços essenciais nem comunicar-se com dependências de serviço externo.</span><span class="sxs-lookup"><span data-stu-id="87f65-113">Red indicates that the server is not available and that it cannot provide key services or communicate with external service dependencies.</span></span>

## <span data-ttu-id="87f65-114">Critérios de monitoramento</span><span class="sxs-lookup"><span data-stu-id="87f65-114">Monitoring Criteria</span></span>


<span data-ttu-id="87f65-115">O pacote de gerenciamento monitora os seguintes aspectos da integridade do servidor:</span><span class="sxs-lookup"><span data-stu-id="87f65-115">The Management Pack monitors the following aspects of server health:</span></span>

-   <span data-ttu-id="87f65-116">Status do servidor — monitora eventos do servidor para confirmar se o servidor está fornecendo seus serviços esperados.</span><span class="sxs-lookup"><span data-stu-id="87f65-116">Server Status—monitors server events to validate that the server is providing its expected services.</span></span>

-   <span data-ttu-id="87f65-117">Acesso ao repositório de dados — controla a capacidade de um ou mais dos servidores de gerenciamento do App-V acessar e se comunicar com o repositório de dados do App-V.</span><span class="sxs-lookup"><span data-stu-id="87f65-117">Data Store Access—tracks the ability of one or more of the App-V Management Servers to access and communicate with the App-V data store.</span></span>

-   <span data-ttu-id="87f65-118">Acesso a dados de conteúdo — monitora o acesso ao diretório \\Content, que pode ser um diretório local ou um compartilhamento de rede e a capacidade de ler os arquivos solicitados.</span><span class="sxs-lookup"><span data-stu-id="87f65-118">Content Data Access—monitors access to the \\Content directory, which might be a local directory or a network share, and the ability to read the requested files.</span></span>

-   <span data-ttu-id="87f65-119">Segurança — relata erros com o certificado do servidor App-V e comunicações seguras.</span><span class="sxs-lookup"><span data-stu-id="87f65-119">Security—reports errors with the App-V Server’s certificate and secure communications.</span></span>

-   <span data-ttu-id="87f65-120">Tratamento de solicitação do cliente — monitora a capacidade de um ou mais dos servidores do App-V manipular e responder corretamente a solicitações do cliente.</span><span class="sxs-lookup"><span data-stu-id="87f65-120">Client Request Handling—monitors the ability of one or more of the App-V Servers to handle and correctly respond to client requests.</span></span> <span data-ttu-id="87f65-121">Essas solicitações incluem a publicação de itens como solicitações de configuração, solicitações de carregamento de pacote e solicitações fora de sequência.</span><span class="sxs-lookup"><span data-stu-id="87f65-121">These requests include publishing such items as configuration requests, package load requests, and out of sequence requests.</span></span>

-   <span data-ttu-id="87f65-122">Configuração do servidor — verifica as configurações do App-V Server.</span><span class="sxs-lookup"><span data-stu-id="87f65-122">Server Configuration—checks the configuration settings of the App-V Server.</span></span> <span data-ttu-id="87f65-123">Essas configurações incluem as configurações no registro e no repositório de dados App-V.</span><span class="sxs-lookup"><span data-stu-id="87f65-123">These configuration settings include the settings in the registry and in the App-V data store.</span></span>

## <span data-ttu-id="87f65-124">Diferenças do servidor</span><span class="sxs-lookup"><span data-stu-id="87f65-124">Server Differences</span></span>


<span data-ttu-id="87f65-125">As principais diferenças entre o servidor de gerenciamento do App-V e do App-V Streaming Server são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="87f65-125">The main differences between the App-V Management Server and the App-V Streaming Server are as follows:</span></span>

-   <span data-ttu-id="87f65-126">Os servidores de gerenciamento do App-V podem oferecer serviços de publicação, streaming, gerenciamento e relatórios.</span><span class="sxs-lookup"><span data-stu-id="87f65-126">App-V Management Servers can provide publishing, streaming, management, and reporting services.</span></span> <span data-ttu-id="87f65-127">Portanto, o pacote de gerenciamento pode gerenciar mais aspectos do servidor de gerenciamento do App-V do que ele pode gerenciar no servidor de streaming do App-V, que fornece apenas streaming de pacote.</span><span class="sxs-lookup"><span data-stu-id="87f65-127">Therefore, the Management Pack can manage more aspects of the App-V Management Server than it can manage on the App-V Streaming Server, which provides only package streaming.</span></span>

-   <span data-ttu-id="87f65-128">O servidor de streaming App-V não tem um repositório de dados App-V, portanto, o acesso ao repositório de dados não é monitorado.</span><span class="sxs-lookup"><span data-stu-id="87f65-128">The App-V Streaming Server does not have an App-V data store, so data store access is not monitored.</span></span> <span data-ttu-id="87f65-129">As informações de configuração do servidor de streaming App-V são gerenciadas no registro.</span><span class="sxs-lookup"><span data-stu-id="87f65-129">The configuration information for the App-V Streaming Server is managed in the registry.</span></span>

-   <span data-ttu-id="87f65-130">O servidor de streaming do App-V não usa a interface do console de gerenciamento do App-V Server; Use outras ferramentas para gerenciar a configuração.</span><span class="sxs-lookup"><span data-stu-id="87f65-130">The App-V Streaming Server does not use the App-V Server Management Console interface; use other tools to manage the configuration.</span></span>

## <span data-ttu-id="87f65-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87f65-131">Related topics</span></span>


[<span data-ttu-id="87f65-132">Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="87f65-132">Application Virtualization Server</span></span>](application-virtualization-server.md)

 

 





