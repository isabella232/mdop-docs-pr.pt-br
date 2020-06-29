---
title: Relatório de Utilização do Sistema
description: Relatório de Utilização do Sistema
author: dansimp
ms.assetid: 4d490d15-2d1f-4f2c-99bb-0685447c0672
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe7ff547d969c63ace234104c3e6b7146da2c113
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796688"
---
# <span data-ttu-id="a8db6-103">Relatório de Utilização do Sistema</span><span class="sxs-lookup"><span data-stu-id="a8db6-103">System Utilization Report</span></span>


<span data-ttu-id="a8db6-104">Use o relatório de utilização do sistema para representar graficamente o uso total diário do sistema.</span><span class="sxs-lookup"><span data-stu-id="a8db6-104">Use the System Utilization Report to graph the total daily system usage.</span></span> <span data-ttu-id="a8db6-105">Você pode usar esse relatório para determinar a carga em seu sistema de virtualização de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a8db6-105">You can use this report to determine the load on your Application Virtualization System.</span></span>

<span data-ttu-id="a8db6-106">Esse relatório controla o uso ao longo do tempo durante o período do relatório para o servidor especificado ou para o grupo de servidores.</span><span class="sxs-lookup"><span data-stu-id="a8db6-106">This report tracks the usage over time during the reporting period for the specified server or for the server group.</span></span>

<span data-ttu-id="a8db6-107">O relatório de utilização do sistema também apresenta graficamente o seguinte uso do sistema:</span><span class="sxs-lookup"><span data-stu-id="a8db6-107">The System Utilization Report also graphs the following system usage:</span></span>

-   <span data-ttu-id="a8db6-108">Uso por dia da semana</span><span class="sxs-lookup"><span data-stu-id="a8db6-108">Usage by day of the week</span></span>

-   <span data-ttu-id="a8db6-109">Uso por hora do dia</span><span class="sxs-lookup"><span data-stu-id="a8db6-109">Usage by hour of the day</span></span>

<span data-ttu-id="a8db6-110">O relatório de utilização do sistema também inclui um resumo do uso total do sistema para usuários específicos e contagens totais de sessão.</span><span class="sxs-lookup"><span data-stu-id="a8db6-110">The System Utilization Report also includes a summary of the total system usage for specific users and total session counts.</span></span>

<span data-ttu-id="a8db6-111">Quando você cria um relatório, especifica os parâmetros que são usados para coletar os dados quando o relatório é executado.</span><span class="sxs-lookup"><span data-stu-id="a8db6-111">When you create a report, you specify the parameters that are used for collecting the data when the report is run.</span></span>

<span data-ttu-id="a8db6-112">Os relatórios não são executados automaticamente; Você deve executá-los explicitamente para gerar dados de saída.</span><span class="sxs-lookup"><span data-stu-id="a8db6-112">Reports are not run automatically; you must run them explicitly to generate output data.</span></span> <span data-ttu-id="a8db6-113">O período de tempo que leva para executar esse relatório é determinado pela quantidade de dados coletados no repositório de dados.</span><span class="sxs-lookup"><span data-stu-id="a8db6-113">The length of time it takes to run this report is determined by the amount of data collected in the data store.</span></span>

<span data-ttu-id="a8db6-114">Depois que você executa um relatório e a saída é exibida no console de gerenciamento do servidor do Application Virtualization, você pode exportar o relatório para os seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="a8db6-114">After you run a report and the output is displayed in the Application Virtualization Server Management Console, you can export the report into the following formats:</span></span>

-   <span data-ttu-id="a8db6-115">Adobe Acrobat (PDF)</span><span class="sxs-lookup"><span data-stu-id="a8db6-115">Adobe Acrobat (PDF)</span></span>

-   <span data-ttu-id="a8db6-116">Microsoft Office Excel</span><span class="sxs-lookup"><span data-stu-id="a8db6-116">Microsoft Office Excel</span></span>

<span data-ttu-id="a8db6-117">**Observação**  O nome do servidor App-V informado dos clientes deve fazer parte do grupo de servidores padrão para que o relatório de utilização do sistema mostre dados.</span><span class="sxs-lookup"><span data-stu-id="a8db6-117">**Note** The App-V server name reported from the clients must be part of the Default Server Group in order for the System Utilization report to show data.</span></span> <span data-ttu-id="a8db6-118">Por exemplo, se você estiver usando vários servidores com um NLB (balanceador de carga de rede), será necessário adicionar o nome do cluster NLB ao grupo servidor padrão.</span><span class="sxs-lookup"><span data-stu-id="a8db6-118">For example, if you are using multiple servers with a Network Load Balancer (NLB), you must add the NLB cluster name to the Default Server Group.</span></span>

 

## <span data-ttu-id="a8db6-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a8db6-119">Related topics</span></span>


[<span data-ttu-id="a8db6-120">Como criar um relatório</span><span class="sxs-lookup"><span data-stu-id="a8db6-120">How to Create a Report</span></span>](how-to-create-a-reportserver.md)

[<span data-ttu-id="a8db6-121">Como excluir um relatório</span><span class="sxs-lookup"><span data-stu-id="a8db6-121">How to Delete a Report</span></span>](how-to-delete-a-reportserver.md)

[<span data-ttu-id="a8db6-122">Como exportar um relatório</span><span class="sxs-lookup"><span data-stu-id="a8db6-122">How to Export a Report</span></span>](how-to-export-a-reportserver.md)

[<span data-ttu-id="a8db6-123">Como imprimir um relatório</span><span class="sxs-lookup"><span data-stu-id="a8db6-123">How to Print a Report</span></span>](how-to-print-a-reportserver.md)

[<span data-ttu-id="a8db6-124">Como executar um relatório</span><span class="sxs-lookup"><span data-stu-id="a8db6-124">How to Run a Report</span></span>](how-to-run-a-reportserver.md)

 

 





