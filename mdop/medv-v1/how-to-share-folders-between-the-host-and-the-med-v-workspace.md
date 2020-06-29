---
title: Como compartilhar pastas entre o host e o espaço de trabalho do MED-V
description: Como compartilhar pastas entre o host e o espaço de trabalho do MED-V
author: dansimp
ms.assetid: 3cb295f2-c07e-4ee6-aa3c-ce4c8c45c191
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 87f315c9894cd38834413d2549e652a36c5cc16d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799735"
---
# <span data-ttu-id="53b68-103">Como compartilhar pastas entre o host e o espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="53b68-103">How to Share Folders Between the Host and the MED-V Workspace</span></span>


<span data-ttu-id="53b68-104">Você pode compartilhar pastas entre o host e o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="53b68-104">You can share folders between the host and the MED-V workspace.</span></span> <span data-ttu-id="53b68-105">As pastas compartilhadas podem ser armazenadas no seguinte:</span><span class="sxs-lookup"><span data-stu-id="53b68-105">The shared folders can be stored on the following:</span></span>

-   <span data-ttu-id="53b68-106">Um computador externo na rede</span><span class="sxs-lookup"><span data-stu-id="53b68-106">An external computer on the network</span></span>

-   <span data-ttu-id="53b68-107">O computador host</span><span class="sxs-lookup"><span data-stu-id="53b68-107">The host computer</span></span>

<span data-ttu-id="53b68-108">Os procedimentos a seguir demonstram como compartilhar pastas entre o host e o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="53b68-108">The following procedures demonstrate how to share folders between the host and the MED-V workspace.</span></span>

**<span data-ttu-id="53b68-109">Para compartilhar pastas localizadas na rede</span><span class="sxs-lookup"><span data-stu-id="53b68-109">To share folders located on the network</span></span>**

1.  <span data-ttu-id="53b68-110">Configure o MED-V no modo de área de trabalho completo.</span><span class="sxs-lookup"><span data-stu-id="53b68-110">Configure MED-V in full desktop mode.</span></span>

2.  <span data-ttu-id="53b68-111">No gerenciamento do MED-V, na guia rede, clique em **usar um endereço IP diferente do host (ponte)**.</span><span class="sxs-lookup"><span data-stu-id="53b68-111">In MED-V management, on the Network tab, click **Use different IP address than host (Bridge)**.</span></span>

3.  <span data-ttu-id="53b68-112">Faça o seguinte no computador host:</span><span class="sxs-lookup"><span data-stu-id="53b68-112">Do the following on the host computer:</span></span>

    1.  <span data-ttu-id="53b68-113">No painel de controle, clique em **Exibir o status e as tarefas da rede**e defina **descoberta de rede** como **ativada**.</span><span class="sxs-lookup"><span data-stu-id="53b68-113">In Control Panel, click **View network status and tasks**, and set **Network discovery** to **On**.</span></span>

    2.  <span data-ttu-id="53b68-114">No menu Iniciar, clique com o botão direito do mouse em **computador**e clique em **Mapear unidade de rede**.</span><span class="sxs-lookup"><span data-stu-id="53b68-114">On the Start menu, right-click **Computer**, and click **Map network drive**.</span></span>

    3.  <span data-ttu-id="53b68-115">Na caixa de diálogo **Mapear unidade de rede** , no campo **unidade** , selecione uma unidade.</span><span class="sxs-lookup"><span data-stu-id="53b68-115">In the **Map Network Drive** dialog box, in the **Drive** field, select a drive.</span></span>

        <span data-ttu-id="53b68-116">**Observação**  Verifique se a mesma letra de unidade não está em uso em ambos os computadores.</span><span class="sxs-lookup"><span data-stu-id="53b68-116">**Note** Ensure that the same drive letter is not in use on both computers.</span></span>

         

    4.  <span data-ttu-id="53b68-117">Clique em **Procurar**.</span><span class="sxs-lookup"><span data-stu-id="53b68-117">Click **Browse**.</span></span>

    5.  <span data-ttu-id="53b68-118">Na caixa de diálogo **Procurar pasta** , navegue até a unidade compartilhada e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="53b68-118">In the **Browse For Folder** dialog box, browse to the shared drive, and click **OK**.</span></span>

    6.  <span data-ttu-id="53b68-119">Clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="53b68-119">Click **Finish**.</span></span>

4.  <span data-ttu-id="53b68-120">Repita a etapa 3 no espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="53b68-120">Repeat step 3 in the MED-V workspace.</span></span> <span data-ttu-id="53b68-121">Aponte para a mesma unidade do computador host.</span><span class="sxs-lookup"><span data-stu-id="53b68-121">Point to the same drive as on the host computer.</span></span>

**<span data-ttu-id="53b68-122">Para compartilhar pastas localizadas no host</span><span class="sxs-lookup"><span data-stu-id="53b68-122">To share folders located on the host</span></span>**

1.  <span data-ttu-id="53b68-123">Configure a pasta a ser compartilhada com as permissões apropriadas.</span><span class="sxs-lookup"><span data-stu-id="53b68-123">Configure the folder to be shared with the appropriate permissions.</span></span>

2.  <span data-ttu-id="53b68-124">No espaço de trabalho do MED-V, vá para **meus locais de rede** e localize a pasta compartilhada.</span><span class="sxs-lookup"><span data-stu-id="53b68-124">From the MED-V workspace, go to **My network places** and locate the shared folder.</span></span>

3.  <span data-ttu-id="53b68-125">No espaço de trabalho do MED-V, localize a pasta compartilhada.</span><span class="sxs-lookup"><span data-stu-id="53b68-125">From the MED-V workspace, locate the shared folder.</span></span>

<span data-ttu-id="53b68-126">**Observação**  Certifique-se de que os computadores do espaço de trabalho do host e do espaço de trabalho do MED-V estejam no mesmo domínio ou grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="53b68-126">**Note** Ensure that both the host and MED-V workspace computers are in the same domain or workgroup.</span></span>

 

 

 





