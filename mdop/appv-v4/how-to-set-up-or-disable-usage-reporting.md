---
title: Como configurar ou desabilitar os relatórios de uso
description: Como configurar ou desabilitar os relatórios de uso
author: dansimp
ms.assetid: 8587003a-128d-4b5d-ac70-5b9eddddd3dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f8f6c44d4060581f1ebe435875bc2f105cb93d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796947"
---
# <span data-ttu-id="35a14-103">Como configurar ou desabilitar os relatórios de uso</span><span class="sxs-lookup"><span data-stu-id="35a14-103">How to Set Up or Disable Usage Reporting</span></span>


<span data-ttu-id="35a14-104">Você pode usar os procedimentos a seguir no console de gerenciamento do servidor do Application Virtualization para especificar a duração (em meses) das informações de uso do sistema do Application Virtualization que você deseja armazenar no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="35a14-104">You can use the following procedures in the Application Virtualization Server Management Console to specify the duration (in months) of Application Virtualization System usage information you want to store in the database.</span></span>

<span data-ttu-id="35a14-105">**Observação**  Para armazenar informações de uso, você deve marcar a caixa de seleção **registrar informações de uso** na guia **pipeline do provedor** . Para exibir essa guia, clique com o botão direito do mouse na política do provedor no painel **resultados das políticas do provedor** e selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="35a14-105">**Note** To store usage information, you must select the **Log Usage Information** check box on the **Provider Pipeline** tab. To display this tab, right-click the provider policy in the **Provider Policies Results** pane and select **Properties**.</span></span>

 

**<span data-ttu-id="35a14-106">Para configurar o relatório de uso</span><span class="sxs-lookup"><span data-stu-id="35a14-106">To set up usage reporting</span></span>**

1.  <span data-ttu-id="35a14-107">Clique com o botão direito do mouse no nó do sistema de virtualização do aplicativo no painel esquerdo e selecione **Opções do sistema**.</span><span class="sxs-lookup"><span data-stu-id="35a14-107">Right-click the Application Virtualization System node in the left pane, and select **System Options**.</span></span>

2.  <span data-ttu-id="35a14-108">Selecione a guia **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="35a14-108">Select the **Database** tab.</span></span>

3.  <span data-ttu-id="35a14-109">Marque a caixa de seleção **manter uso de (meses)** ou **manter todos os usos** .</span><span class="sxs-lookup"><span data-stu-id="35a14-109">Select the **Keep Usage For (Months)** or **Keep All Usage** radio button.</span></span>

4.  <span data-ttu-id="35a14-110">Se você optar por especificar a duração do uso em meses, insira um número entre 1 e 120 (o valor padrão é de 6 meses).</span><span class="sxs-lookup"><span data-stu-id="35a14-110">If you choose to specify usage duration in months, enter a number from 1 to 120 (default value is 6 months).</span></span> <span data-ttu-id="35a14-111">Se você selecionar **manter todo o uso**, o banco de dados será ampliado até atingir o limite de tamanho especificado.</span><span class="sxs-lookup"><span data-stu-id="35a14-111">If you select **Keep All Usage**, the database will grow until it reaches the specified size limit.</span></span>

5.  <span data-ttu-id="35a14-112">Clique em **aplicar** ou em **OK**.</span><span class="sxs-lookup"><span data-stu-id="35a14-112">Click **Apply** or **OK**.</span></span>

**<span data-ttu-id="35a14-113">Para desabilitar o relatório de uso</span><span class="sxs-lookup"><span data-stu-id="35a14-113">To disable usage reporting</span></span>**

1.  <span data-ttu-id="35a14-114">Clique no nó **políticas de provedor** .</span><span class="sxs-lookup"><span data-stu-id="35a14-114">Click the **Provider Policies** node.</span></span>

2.  <span data-ttu-id="35a14-115">Clique com o botão direito do mouse em **política do provedor** e selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="35a14-115">Right-click **Provider Policy** and select **Properties**.</span></span>

3.  <span data-ttu-id="35a14-116">Selecione a guia **pipeline do provedor** .</span><span class="sxs-lookup"><span data-stu-id="35a14-116">Select the **Provider Pipeline** tab.</span></span>

4.  <span data-ttu-id="35a14-117">Desmarque a caixa de seleção **registrar informações de uso** .</span><span class="sxs-lookup"><span data-stu-id="35a14-117">Clear the **Log Usage Information** check box.</span></span>

5.  <span data-ttu-id="35a14-118">Clique em **aplicar** ou em **OK**.</span><span class="sxs-lookup"><span data-stu-id="35a14-118">Click **Apply** or **OK**.</span></span>

## <span data-ttu-id="35a14-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="35a14-119">Related topics</span></span>


[<span data-ttu-id="35a14-120">Como personalizar um Application Virtualization System no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="35a14-120">How to Customize an Application Virtualization System in the Server Management Console</span></span>](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[<span data-ttu-id="35a14-121">Como configurar ou desabilitar o tamanho de banco de dados</span><span class="sxs-lookup"><span data-stu-id="35a14-121">How to Set Up or Disable Database Size</span></span>](how-to-set-up-or-disable-database-size.md)

 

 





