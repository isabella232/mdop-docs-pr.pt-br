---
title: Como testar o redirecionamento da URL
description: Como testar o redirecionamento da URL
author: dansimp
ms.assetid: 38d80088-da1d-4098-b27e-76f9e78f81dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d964cf9d0114d3085d7e8952eebc82486b7b76cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799474"
---
# <span data-ttu-id="e6763-103">Como testar o redirecionamento da URL</span><span class="sxs-lookup"><span data-stu-id="e6763-103">How to Test URL Redirection</span></span>


<span data-ttu-id="e6763-104">Depois de concluir o teste da configuração inicial, você pode verificar se a funcionalidade de redirecionamento de URL está funcionando como esperado executando as seguintes tarefas.</span><span class="sxs-lookup"><span data-stu-id="e6763-104">After your test of first time setup finishes, you can verify that the URL redirection functionality is working as expected by performing the following tasks.</span></span>

<span data-ttu-id="e6763-105">**Importante**  O agente de host do MED-V deve estar em execução para que o redirecionamento de URL funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="e6763-105">**Important** The MED-V Host Agent must be running for URL redirection to function correctly.</span></span>

<a href="" id="bkmk-urlredir"></a>**<span data-ttu-id="e6763-106">Para testar o redirecionamento de URL</span><span class="sxs-lookup"><span data-stu-id="e6763-106">To test URL Redirection</span></span>**

1.  <span data-ttu-id="e6763-107">Abra um navegador do Internet Explorer no computador host e insira uma URL que você especificou para o redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="e6763-107">Open an Internet Explorer browser in the host computer and enter a URL that you specified for redirection.</span></span>

2.  <span data-ttu-id="e6763-108">Verifique se a página da Web está aberta no Internet Explorer na máquina virtual convidada.</span><span class="sxs-lookup"><span data-stu-id="e6763-108">Verify that the webpage is opened in Internet Explorer on the guest virtual machine.</span></span>

3.  <span data-ttu-id="e6763-109">Repita esse processo para cada URL que você deseja testar.</span><span class="sxs-lookup"><span data-stu-id="e6763-109">Repeat this process for each URL that you want to test.</span></span>

**<span data-ttu-id="e6763-110">Para testar se uma URL pode ser adicionada ou removida</span><span class="sxs-lookup"><span data-stu-id="e6763-110">To test that a URL can be added or removed</span></span>**

1.  <span data-ttu-id="e6763-111">Adicione ou remova uma URL do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="e6763-111">Add or remove a URL from the MED-V workspace.</span></span>

    <span data-ttu-id="e6763-112">Para obter informações sobre como adicionar e remover URLs para redirecionamento em um espaço de trabalho do MED-V, consulte [gerenciar o redirecionamento de URL do MED-v](manage-med-v-url-redirection.md).</span><span class="sxs-lookup"><span data-stu-id="e6763-112">For information about how to add and remove URLs for redirection on a MED-V workspace, see [Manage MED-V URL Redirection](manage-med-v-url-redirection.md).</span></span>

2.  <span data-ttu-id="e6763-113">Se você adicionou uma URL à lista de redirecionamento, repita as etapas em [para testar o redirecionamento de URL](#bkmk-urlredir) para verificar se a nova URL é redirecionada conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="e6763-113">If you added a URL to the redirection list, repeat the steps in [To Test URL Redirection](#bkmk-urlredir) to verify that the new URL redirects as intended.</span></span>

3.  <span data-ttu-id="e6763-114">Se você removeu uma URL da lista de redirecionamento, verifique se ela foi removida seguindo estas etapas:</span><span class="sxs-lookup"><span data-stu-id="e6763-114">If you removed a URL from the redirection list, verify that it is removed by following these steps:</span></span>

    1.  <span data-ttu-id="e6763-115">Abra um navegador do Internet Explorer no computador host e insira a URL que você removeu da lista de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="e6763-115">Open an Internet Explorer browser in the host computer and enter the URL that you removed from the redirection list.</span></span>

    2.  <span data-ttu-id="e6763-116">Verifique se a página da Web está aberta no Internet Explorer no computador host, em vez de na máquina virtual convidada.</span><span class="sxs-lookup"><span data-stu-id="e6763-116">Verify that the webpage is opened in Internet Explorer on the host computer instead of on the guest virtual machine.</span></span>

        <span data-ttu-id="e6763-117">**Observação**  Pode levar alguns segundos para que as alterações de redirecionamento de URL sejam realizadas.</span><span class="sxs-lookup"><span data-stu-id="e6763-117">**Note** It can take several seconds for the URL redirection changes to take place.</span></span>

<span data-ttu-id="e6763-118">**Observação**  Se você tiver problemas ao verificar suas configurações de redirecionamento de URL, consulte [solução de problemas de operações](operations-troubleshooting-medv2.md).</span><span class="sxs-lookup"><span data-stu-id="e6763-118">**Note** If you encounter any problems when verifying your URL redirection settings, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

<span data-ttu-id="e6763-119">Depois de concluir o teste do redirecionamento de URL no seu espaço de trabalho do MED-V, você pode testar outras configurações para verificar se elas funcionam conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="e6763-119">After you have completed testing URL redirection in your MED-V workspace, you can test other configurations to verify that they function as intended.</span></span>

<span data-ttu-id="e6763-120">Depois de concluir o teste do pacote do espaço de trabalho do MED-V e ter confirmado que ele está funcionando conforme o esperado, você pode implantar o espaço de trabalho do MED-V na sua empresa.</span><span class="sxs-lookup"><span data-stu-id="e6763-120">After you have completed testing your MED-V workspace package and have verified that it is functioning as intended, you can deploy the MED-V workspace to your enterprise.</span></span>

## <span data-ttu-id="e6763-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e6763-121">Related topics</span></span>

[<span data-ttu-id="e6763-122">Como testar a publicação de aplicativos</span><span class="sxs-lookup"><span data-stu-id="e6763-122">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="e6763-123">Como verificar as configurações da primeira instalação</span><span class="sxs-lookup"><span data-stu-id="e6763-123">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

[<span data-ttu-id="e6763-124">Como implantar o pacote de espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="e6763-124">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)

 

 





