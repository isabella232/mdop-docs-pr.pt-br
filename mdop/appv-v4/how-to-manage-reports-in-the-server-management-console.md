---
title: Como gerenciar relatórios no Server Management Console
description: Como gerenciar relatórios no Server Management Console
author: dansimp
ms.assetid: 28d99620-6339-43f6-9288-4aa958607c59
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3d70734be04df380e6ce3f4ee8de126503e482e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797066"
---
# <span data-ttu-id="23c86-103">Como gerenciar relatórios no Server Management Console</span><span class="sxs-lookup"><span data-stu-id="23c86-103">How to Manage Reports in the Server Management Console</span></span>


<span data-ttu-id="23c86-104">Para gerenciar com eficiência o sistema de virtualização de aplicativos, você pode usar o console de gerenciamento do servidor do Application Virtualization para gerar uma variedade de relatórios que fornecem informações sobre o sistema.</span><span class="sxs-lookup"><span data-stu-id="23c86-104">To effectively manage the Application Virtualization System, you can use the Application Virtualization Server Management Console to generate a variety of reports that provide information about the system.</span></span> <span data-ttu-id="23c86-105">Essas informações incluem informações de uso diária para um aplicativo específico ou todos os aplicativos e o rastreamento de erros do sistema.</span><span class="sxs-lookup"><span data-stu-id="23c86-105">This information includes daily usage information for a specific application or all applications, and system error tracking.</span></span>

**<span data-ttu-id="23c86-106">Observação</span><span class="sxs-lookup"><span data-stu-id="23c86-106">Note</span></span>**  
-   <span data-ttu-id="23c86-107">Durante a instalação, o script de instalação instala apenas a versão do idioma inglês do Visualizador de relatórios.</span><span class="sxs-lookup"><span data-stu-id="23c86-107">During installation, the installation script installs only the English language version of report viewer.</span></span> <span data-ttu-id="23c86-108">Para que o Visualizador de relatórios exiba as informações corretas em outros idiomas, é necessário instalar um pacote de idiomas do seguinte local: <https://go.microsoft.com/fwlink/?LinkId=131645> .</span><span class="sxs-lookup"><span data-stu-id="23c86-108">For the report viewer to display the correct information in other languages, it is necessary to install a language pack from the following location: <https://go.microsoft.com/fwlink/?LinkId=131645>.</span></span>

-   <span data-ttu-id="23c86-109">Quando você adiciona ou edita um aplicativo no console de gerenciamento do servidor, deve certificar-se de que os nomes e versões dos aplicativos correspondem exatamente aos dos arquivos OSD.</span><span class="sxs-lookup"><span data-stu-id="23c86-109">When you add or edit an application in the Server Management Console, you must make sure that the application names and versions exactly match those in the OSD files.</span></span> <span data-ttu-id="23c86-110">O recurso de relatório usa os campos de dados nomes e versões dos aplicativos quando identifica os dados de uso do aplicativo nos quais relatar.</span><span class="sxs-lookup"><span data-stu-id="23c86-110">The reporting feature uses the application names and versions data fields when it identifies application usage data on which to report.</span></span> <span data-ttu-id="23c86-111">Se os campos de dados não corresponderem, os registros de uso serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="23c86-111">If the data fields do not match, the usage records will be skipped.</span></span>

 

## <span data-ttu-id="23c86-112">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="23c86-112">In This Section</span></span>


<a href="" id="application-virtualization-report-types"></a>[<span data-ttu-id="23c86-113">Tipos de relatórios do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="23c86-113">Application Virtualization Report Types</span></span>](application-virtualization-report-types.md)  
<span data-ttu-id="23c86-114">Contém informações sobre os tipos de relatórios disponíveis.</span><span class="sxs-lookup"><span data-stu-id="23c86-114">Contains information about the available report types.</span></span>

<a href="" id="how-to-create-a-report"></a>[<span data-ttu-id="23c86-115">Como criar um relatório</span><span class="sxs-lookup"><span data-stu-id="23c86-115">How to Create a Report</span></span>](how-to-create-a-reportserver.md)  
<span data-ttu-id="23c86-116">Fornece um processo passo a passo para a criação de um relatório.</span><span class="sxs-lookup"><span data-stu-id="23c86-116">Provides a step-by-step process for creating a report.</span></span>

<a href="" id="how-to-run-a-report"></a>[<span data-ttu-id="23c86-117">Como executar um relatório</span><span class="sxs-lookup"><span data-stu-id="23c86-117">How to Run a Report</span></span>](how-to-run-a-reportserver.md)  
<span data-ttu-id="23c86-118">Fornece um processo passo a passo para executar um relatório.</span><span class="sxs-lookup"><span data-stu-id="23c86-118">Provides a step-by-step process for running a report.</span></span>

<a href="" id="how-to-print-a-report"></a>[<span data-ttu-id="23c86-119">Como imprimir um relatório</span><span class="sxs-lookup"><span data-stu-id="23c86-119">How to Print a Report</span></span>](how-to-print-a-reportserver.md)  
<span data-ttu-id="23c86-120">Fornece um processo passo a passo para imprimir um relatório.</span><span class="sxs-lookup"><span data-stu-id="23c86-120">Provides a step-by-step process for printing a report.</span></span>

<a href="" id="how-to-export-a-report"></a>[<span data-ttu-id="23c86-121">Como exportar um relatório</span><span class="sxs-lookup"><span data-stu-id="23c86-121">How to Export a Report</span></span>](how-to-export-a-reportserver.md)  
<span data-ttu-id="23c86-122">Fornece um processo passo a passo para exportar um relatório.</span><span class="sxs-lookup"><span data-stu-id="23c86-122">Provides a step-by-step process for exporting a report.</span></span>

<a href="" id="how-to-delete-a-report"></a>[<span data-ttu-id="23c86-123">Como excluir um relatório</span><span class="sxs-lookup"><span data-stu-id="23c86-123">How to Delete a Report</span></span>](how-to-delete-a-reportserver.md)  
<span data-ttu-id="23c86-124">Fornece um processo passo a passo para excluir um relatório.</span><span class="sxs-lookup"><span data-stu-id="23c86-124">Provides a step-by-step process for deleting a report.</span></span>

## <span data-ttu-id="23c86-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="23c86-125">Related topics</span></span>


[<span data-ttu-id="23c86-126">Relatório de Utilização de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="23c86-126">Application Utilization Report</span></span>](application-utilization-reportserver.md)

[<span data-ttu-id="23c86-127">Como realizar tarefas administrativas no Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="23c86-127">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

[<span data-ttu-id="23c86-128">Relatório de Auditoria de Software</span><span class="sxs-lookup"><span data-stu-id="23c86-128">Software Audit Report</span></span>](software-audit-reportserver.md)

[<span data-ttu-id="23c86-129">Relatório de Erros do Sistema</span><span class="sxs-lookup"><span data-stu-id="23c86-129">System Error Report</span></span>](system-error-reportserver.md)

[<span data-ttu-id="23c86-130">Relatório de Utilização do Sistema</span><span class="sxs-lookup"><span data-stu-id="23c86-130">System Utilization Report</span></span>](system-utilization-reportserver.md)

 

 





