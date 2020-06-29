---
title: Como configurar ou desabilitar o tamanho de banco de dados
description: Como configurar ou desabilitar o tamanho de banco de dados
author: dansimp
ms.assetid: 4abaf349-132d-4186-8873-a0e515593b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cbb041920e2680d51b01926f144eba595fe28d05
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796950"
---
# <span data-ttu-id="26a6f-103">Como configurar ou desabilitar o tamanho de banco de dados</span><span class="sxs-lookup"><span data-stu-id="26a6f-103">How to Set Up or Disable Database Size</span></span>


<span data-ttu-id="26a6f-104">Você pode usar os procedimentos a seguir no console de gerenciamento do servidor do Application Virtualization para especificar o tamanho (em MB) do uso do sistema do Application Virtualization que você deseja armazenar no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="26a6f-104">You can use the following procedures in the Application Virtualization Server Management Console to specify the size (in MB) of Application Virtualization System usage that you want to store in the database.</span></span>

<span data-ttu-id="26a6f-105">Quando o tamanho dos dados armazenados alcança 95% (a marca-d ' água alta) do limite especificado, o sistema excluirá 10% dos dados de uso, deixando 85% dos dados.</span><span class="sxs-lookup"><span data-stu-id="26a6f-105">When the size of the stored data reaches 95% (the high watermark) of the specified limit, the system will delete 10% of the usage data, leaving 85% of the data.</span></span> <span data-ttu-id="26a6f-106">Os dados de uso do pacote e do aplicativo serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="26a6f-106">Package and application usage data will be deleted.</span></span> <span data-ttu-id="26a6f-107">Quando o banco de dados cresce grande o suficiente e se aproxima da marca d' água alta, uma mensagem de aviso é enviada ao log do SQL Server para informar que esse limite foi atingido.</span><span class="sxs-lookup"><span data-stu-id="26a6f-107">When the database grows large enough and approaches the high watermark, a warning message is sent to the SQL Server log to inform you that this limit has been reached.</span></span> <span data-ttu-id="26a6f-108">Esse aviso é necessário porque a ação de limpeza pode afetar a saída dos relatórios.</span><span class="sxs-lookup"><span data-stu-id="26a6f-108">This warning is necessary because the cleanup action can affect the output of the reports.</span></span> <span data-ttu-id="26a6f-109">Ele também ajudará você a decidir se precisa aumentar o tamanho máximo do banco de dados, reduzir o número de meses de dados de uso a serem mantidos ou desativar o nível de log.</span><span class="sxs-lookup"><span data-stu-id="26a6f-109">It will also help you decide whether you need to increase the maximum database size, reduce the number of months of usage data to be kept, or turn down the logging level.</span></span>

<span data-ttu-id="26a6f-110">**Observação**  As opções **sem limite de tamanho** e **manter todas as** opções de uso são fornecidas para que você possa desabilitar o relatório de uso e a limpeza do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="26a6f-110">**Note** The **No Size Limit** and **Keep All Usage** options are provided so that you can disable usage reporting and database cleanup.</span></span> <span data-ttu-id="26a6f-111">Selecionar esses itens limpará também o log de transação do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="26a6f-111">Selecting these items will clean up the database transaction log as well.</span></span> <span data-ttu-id="26a6f-112">(Todas as transações confirmadas do Microsoft SQL Server serão removidas do log de banco de dados.)</span><span class="sxs-lookup"><span data-stu-id="26a6f-112">(All committed Microsoft SQL Server transactions will be removed from the database log.)</span></span>

 

**<span data-ttu-id="26a6f-113">Para configurar o tamanho do banco de dados</span><span class="sxs-lookup"><span data-stu-id="26a6f-113">To set up database size</span></span>**

1.  <span data-ttu-id="26a6f-114">Clique com o botão direito do mouse no nó do sistema de virtualização do aplicativo no painel esquerdo e selecione **Opções do sistema**.</span><span class="sxs-lookup"><span data-stu-id="26a6f-114">Right-click the Application Virtualization System node in the left pane, and select **System Options**.</span></span>

2.  <span data-ttu-id="26a6f-115">Selecione a guia **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="26a6f-115">Select the **Database** tab.</span></span>

3.  <span data-ttu-id="26a6f-116">Selecione o botão de opção **tamanho máximo do banco de dados (MB)** ou **limite de tamanho** .</span><span class="sxs-lookup"><span data-stu-id="26a6f-116">Select the **Maximum Database Size (MB)** or **No Size Limit** radio button.</span></span>

4.  <span data-ttu-id="26a6f-117">Se você optar por especificar um tamanho de banco de dados, as práticas recomendadas recomendam que você insira um número entre 512 e 4096 MB.</span><span class="sxs-lookup"><span data-stu-id="26a6f-117">If you choose to specify a database size, best practices recommend that you enter a number between 512 and 4096 MB.</span></span> <span data-ttu-id="26a6f-118">O tamanho padrão é de 1024 MB e, se você precisar aumentar o tamanho do banco de dados, o valor máximo que você pode inserir é 2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="26a6f-118">The default size is 1024 MB and if you need to increase the database size, the maximum value you can enter is 2,147,483,647.</span></span> <span data-ttu-id="26a6f-119">Se você selecionar **sem limite de tamanho**, o banco de dados será aumentado até atingir o limite de tamanho do disco.</span><span class="sxs-lookup"><span data-stu-id="26a6f-119">If you select **No Size Limit**, the database will grow until it reaches the disk size limit.</span></span>

5.  <span data-ttu-id="26a6f-120">Clique em **aplicar** ou em **OK**.</span><span class="sxs-lookup"><span data-stu-id="26a6f-120">Click **Apply** or **OK**.</span></span>

**<span data-ttu-id="26a6f-121">Para desabilitar os limites de tamanho do banco de dados</span><span class="sxs-lookup"><span data-stu-id="26a6f-121">To disable database size limits</span></span>**

1.  <span data-ttu-id="26a6f-122">Clique com o botão direito do mouse no nó do sistema do Application Virtualization no painel **escopo** e selecione **Opções do sistema**.</span><span class="sxs-lookup"><span data-stu-id="26a6f-122">Right-click the Application Virtualization System node in the **Scope** pane, and select **System Options**.</span></span>

2.  <span data-ttu-id="26a6f-123">Selecione a guia **banco de dados** .</span><span class="sxs-lookup"><span data-stu-id="26a6f-123">Select the **Database** tab.</span></span>

3.  <span data-ttu-id="26a6f-124">Selecione os botões de opção **sem limite de tamanho** e **manter todos os usos** .</span><span class="sxs-lookup"><span data-stu-id="26a6f-124">Select the **No Size Limit** and **Keep All Usage** radio buttons.</span></span>

4.  <span data-ttu-id="26a6f-125">Clique em **aplicar** ou em **OK**.</span><span class="sxs-lookup"><span data-stu-id="26a6f-125">Click **Apply** or **OK**.</span></span>

## <span data-ttu-id="26a6f-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="26a6f-126">Related topics</span></span>


[<span data-ttu-id="26a6f-127">Como personalizar um Application Virtualization System no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="26a6f-127">How to Customize an Application Virtualization System in the Server Management Console</span></span>](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[<span data-ttu-id="26a6f-128">Como configurar ou desabilitar os relatórios de uso</span><span class="sxs-lookup"><span data-stu-id="26a6f-128">How to Set Up or Disable Usage Reporting</span></span>](how-to-set-up-or-disable-usage-reporting.md)

 

 





