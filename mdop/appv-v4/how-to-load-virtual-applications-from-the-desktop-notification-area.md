---
title: Como carregar aplicativos virtuais desde a Área de Notificação da Área de Trabalho
description: Como carregar aplicativos virtuais desde a Área de Notificação da Área de Trabalho
author: dansimp
ms.assetid: f52758eb-8b81-4b3c-9bc3-adcf7c00c238
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d7004f9e0031dfeeedc8b6a916e2f3488f1d31e1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797081"
---
# <span data-ttu-id="6d8a5-103">Como carregar aplicativos virtuais desde a Área de Notificação da Área de Trabalho</span><span class="sxs-lookup"><span data-stu-id="6d8a5-103">How to Load Virtual Applications from the Desktop Notification Area</span></span>


<span data-ttu-id="6d8a5-104">Se você for um usuário móvel, talvez queira carregar completamente seus aplicativos no cache para usá-los durante a operação desconectada ou o modo offline.</span><span class="sxs-lookup"><span data-stu-id="6d8a5-104">If you are a mobile user, you might want to fully load your applications in the cache to use them during disconnected operation or offline mode.</span></span> <span data-ttu-id="6d8a5-105">Para transmitir aplicativos do servidor do Application Virtualization (App-V) ou do Application Virtualization (App-V) Streaming Server, você deve estar conectado a um servidor para carregar aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6d8a5-105">To stream applications from the Application Virtualization (App-V) Server or the Application Virtualization (App-V) Streaming Server, you must be connected to a server to load applications.</span></span> <span data-ttu-id="6d8a5-106">Se você não estiver conectado ao servidor quando tentar carregar aplicativos, seu sistema gerará uma mensagem de erro adequada.</span><span class="sxs-lookup"><span data-stu-id="6d8a5-106">If you are not connected to the server when you attempt to load applications, your system will generate an appropriate error message.</span></span> <span data-ttu-id="6d8a5-107">Você também pode transmitir aplicativos para o cliente a partir de um arquivo ou disco.</span><span class="sxs-lookup"><span data-stu-id="6d8a5-107">You can also stream applications to the client from a file or disk.</span></span>

<span data-ttu-id="6d8a5-108">Os aplicativos são carregados um aplicativo de cada vez.</span><span class="sxs-lookup"><span data-stu-id="6d8a5-108">The applications are loaded one application at a time.</span></span> <span data-ttu-id="6d8a5-109">A barra de progresso mostra o nome do aplicativo, a porcentagem do aplicativo carregado e o número de aplicativos já processados em comparação ao número total dos aplicativos em fila.</span><span class="sxs-lookup"><span data-stu-id="6d8a5-109">The progress bar shows you the application name, the percentage of application loaded, and the number of applications already processed compared to the total number of the applications queued.</span></span> <span data-ttu-id="6d8a5-110">Você pode ignorar qualquer aplicativo em andamento antes que ele seja 100% carregado.</span><span class="sxs-lookup"><span data-stu-id="6d8a5-110">You can skip any application in progress before it is 100% loaded.</span></span> <span data-ttu-id="6d8a5-111">Você também pode ignorar o carregamento de todos os aplicativos restantes.</span><span class="sxs-lookup"><span data-stu-id="6d8a5-111">You can skip the loading of all remaining applications as well.</span></span>

<span data-ttu-id="6d8a5-112">**Observação**  Se o sistema encontrar um erro ao carregar um aplicativo, ele informa o erro para você.</span><span class="sxs-lookup"><span data-stu-id="6d8a5-112">**Note** If your system encounters an error while loading an application, it reports the error to you.</span></span> <span data-ttu-id="6d8a5-113">Você deve descartar a caixa de diálogo de erro antes que ela carregue o próximo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6d8a5-113">You must dismiss the error dialog before it will load the next application.</span></span>

 

**<span data-ttu-id="6d8a5-114">Para carregar todos os aplicativos</span><span class="sxs-lookup"><span data-stu-id="6d8a5-114">To load all applications</span></span>**

1.  <span data-ttu-id="6d8a5-115">Clique com o botão direito do mouse no ícone do sistema do Application Virtualization na área de notificação.</span><span class="sxs-lookup"><span data-stu-id="6d8a5-115">Right-click the Application Virtualization System icon in the notification area.</span></span>

2.  <span data-ttu-id="6d8a5-116">Selecione **carregar aplicativos** no menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="6d8a5-116">Select **Load Applications** from the pop-up menu.</span></span>

**<span data-ttu-id="6d8a5-117">Para ignorar aplicativos</span><span class="sxs-lookup"><span data-stu-id="6d8a5-117">To skip applications</span></span>**

1.  <span data-ttu-id="6d8a5-118">Clique na barra de progresso para exibir a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6d8a5-118">Click the progress bar to display the dialog box.</span></span>

2.  <span data-ttu-id="6d8a5-119">Selecione um dos seguintes botões para obter os resultados desejados:</span><span class="sxs-lookup"><span data-stu-id="6d8a5-119">Select one of the following buttons to achieve the desired results:</span></span>

    1.  <span data-ttu-id="6d8a5-120">**Ignorar**— para ignorar o aplicativo que está carregando.</span><span class="sxs-lookup"><span data-stu-id="6d8a5-120">**Skip**—To skip the currently loading application.</span></span>

    2.  <span data-ttu-id="6d8a5-121">**Ignorar tudo**— para ignorar todos os aplicativos restantes.</span><span class="sxs-lookup"><span data-stu-id="6d8a5-121">**Skip All**—To skip all remaining applications.</span></span>

    3.  <span data-ttu-id="6d8a5-122">**Continuar**— para cancelar a caixa de diálogo e continuar carregando aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6d8a5-122">**Continue**—To cancel the dialog box and continue loading applications.</span></span>

## <span data-ttu-id="6d8a5-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6d8a5-123">Related topics</span></span>


[<span data-ttu-id="6d8a5-124">Como usar a Área de Notificação da Área de Trabalho para o Application Virtualization Client Management</span><span class="sxs-lookup"><span data-stu-id="6d8a5-124">How to Use the Desktop Notification Area for Application Virtualization Client Management</span></span>](how-to-use-the-desktop-notification-area-for-application-virtualization-client-management.md)

 

 





