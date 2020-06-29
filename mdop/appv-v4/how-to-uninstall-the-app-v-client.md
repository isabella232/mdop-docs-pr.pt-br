---
title: Como desinstalar o cliente do App-V
description: Como desinstalar o cliente do App-V
author: dansimp
ms.assetid: 07591270-9651-4bb5-a5b3-e0fc009bd9e2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: acb3f53b42027ff2c1b84fd2ab2bdde3c52f96de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796942"
---
# <span data-ttu-id="fc2a7-103">Como desinstalar o cliente do App-V</span><span class="sxs-lookup"><span data-stu-id="fc2a7-103">How to Uninstall the App-V Client</span></span>


<span data-ttu-id="fc2a7-104">Use o procedimento a seguir para desinstalar o cliente Application Virtualization do computador.</span><span class="sxs-lookup"><span data-stu-id="fc2a7-104">Use the following procedure to uninstall the Application Virtualization Client from the computer.</span></span>

**<span data-ttu-id="fc2a7-105">Para desinstalar o cliente de desktop do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="fc2a7-105">To uninstall the Application Virtualization Desktop Client</span></span>**

1.  <span data-ttu-id="fc2a7-106">No painel de controle, clique duas vezes em **Adicionar ou remover programas** (ou, no Windows Vista, **programas e recursos**) e, em seguida, clique duas vezes em **cliente da área de trabalho do Microsoft Application Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="fc2a7-106">In Control Panel, double-click **Add or Remove Programs** (or in Windows Vista, **Programs and Features**), and then double-click **Microsoft Application Virtualization Desktop Client**.</span></span>

2.  <span data-ttu-id="fc2a7-107">Na caixa de diálogo exibida, clique em **Sim** para continuar com o processo de desinstalação.</span><span class="sxs-lookup"><span data-stu-id="fc2a7-107">In the dialog box that appears, click **Yes** to continue with the uninstall process.</span></span>

    <span data-ttu-id="fc2a7-108">**Importante**  O processo de desinstalação não pode ser cancelado ou interrompido.</span><span class="sxs-lookup"><span data-stu-id="fc2a7-108">**Important** The uninstall process cannot be canceled or interrupted.</span></span>

     

3.  <span data-ttu-id="fc2a7-109">Quando uma mensagem informando que o aplicativo da bandeja do cliente Microsoft Application Virtualization deve ser fechada antes de continuar aparecer, clique com o botão direito do mouse no ícone do App-V na área de notificação e selecione **sair** para fechar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc2a7-109">When a message stating that the Microsoft Application Virtualization Client Tray application must be closed before continuing appears, right-click the App-V icon in the notification area and select **Exit** to close the application.</span></span> <span data-ttu-id="fc2a7-110">Em seguida, clique em **repetir** para continuar com o processo de desinstalação.</span><span class="sxs-lookup"><span data-stu-id="fc2a7-110">Then click **Retry** to continue with the uninstall process.</span></span>

    <span data-ttu-id="fc2a7-111">**Importante**  Você pode ver uma mensagem informando que um ou mais aplicativos virtuais estão em uso.</span><span class="sxs-lookup"><span data-stu-id="fc2a7-111">**Important** You might see a message stating that one or more virtual applications are in use.</span></span> <span data-ttu-id="fc2a7-112">Feche todos os aplicativos abertos e salve os dados antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="fc2a7-112">Close any open applications and save your data before you continue.</span></span> <span data-ttu-id="fc2a7-113">Em seguida, clique em **OK** para continuar com o processo de desinstalação.</span><span class="sxs-lookup"><span data-stu-id="fc2a7-113">Then click **OK** to continue with the uninstall process.</span></span>

     

4.  <span data-ttu-id="fc2a7-114">Uma barra de progresso mostra o tempo restante.</span><span class="sxs-lookup"><span data-stu-id="fc2a7-114">A progress bar shows the time remaining.</span></span> <span data-ttu-id="fc2a7-115">Quando esta etapa terminar, você deverá reiniciar o computador para que todos os drivers associados possam ser interrompidos para concluir o processo de desinstalação.</span><span class="sxs-lookup"><span data-stu-id="fc2a7-115">When this step finishes, you must restart the computer so that all associated drivers can be stopped to complete the uninstall process.</span></span>

    <span data-ttu-id="fc2a7-116">**Observação**  As seguintes chaves do registro permanecem após o processo de desinstalação ser concluído:</span><span class="sxs-lookup"><span data-stu-id="fc2a7-116">**Note** The following registry keys remain after the uninstall process is complete:</span></span>

    -   <span data-ttu-id="fc2a7-117">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid</span><span class="sxs-lookup"><span data-stu-id="fc2a7-117">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid</span></span>

    -   <span data-ttu-id="fc2a7-118">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5</span><span class="sxs-lookup"><span data-stu-id="fc2a7-118">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5</span></span>

    -   <span data-ttu-id="fc2a7-119">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard "cliente" = DWORD: 00000000</span><span class="sxs-lookup"><span data-stu-id="fc2a7-119">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard"Client"=dword:00000000</span></span>

    -   <span data-ttu-id="fc2a7-120">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey</span><span class="sxs-lookup"><span data-stu-id="fc2a7-120">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey</span></span>

     

## <span data-ttu-id="fc2a7-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc2a7-121">Related topics</span></span>


[<span data-ttu-id="fc2a7-122">Como instalar o cliente usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="fc2a7-122">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

[<span data-ttu-id="fc2a7-123">Como instalar manualmente o Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="fc2a7-123">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="fc2a7-124">Como publicar um aplicativo virtual no cliente</span><span class="sxs-lookup"><span data-stu-id="fc2a7-124">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

 

 





