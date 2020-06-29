---
title: Como usar um ambiente de teste
description: Como usar um ambiente de teste
author: dansimp
ms.assetid: fc5fcc7c-1ac8-483a-a6bd-2279ae2ee3fb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fc3ad91747c755efe0576cc62473848094b72ed1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797272"
---
# <span data-ttu-id="f5cc0-103">Como usar um ambiente de teste</span><span class="sxs-lookup"><span data-stu-id="f5cc0-103">Using a Test Environment</span></span>


<span data-ttu-id="f5cc0-104">Antes de solicitar que um objeto de política de grupo (GPO) seja implantado no ambiente de produção, você deve testar o GPO em um ambiente de laboratório.</span><span class="sxs-lookup"><span data-stu-id="f5cc0-104">Before you request that a Group Policy Object (GPO) be deployed to the production environment, you should test the GPO in a lab environment.</span></span> <span data-ttu-id="f5cc0-105">Se você desenvolver o GPO em um domínio em uma floresta de teste, poderá exportar o GPO para um arquivo e importá-lo para um domínio na floresta de produção.</span><span class="sxs-lookup"><span data-stu-id="f5cc0-105">If you develop the GPO in a domain in a test forest, you can export the GPO to a file and import the file to a domain in the production forest.</span></span> <span data-ttu-id="f5cc0-106">Em seguida, você pode testar o GPO vinculando-o a uma unidade organizacional (OU) que contém computadores de teste e usuários.</span><span class="sxs-lookup"><span data-stu-id="f5cc0-106">You can then test the GPO by linking it to an organizational unit (OU) that contains test computers and users.</span></span>

-   [<span data-ttu-id="f5cc0-107">Exportar um GPO para um arquivo</span><span class="sxs-lookup"><span data-stu-id="f5cc0-107">Export a GPO to a File</span></span>](export-a-gpo-to-a-file.md)

-   [<span data-ttu-id="f5cc0-108">Importar um GPO de um arquivo</span><span class="sxs-lookup"><span data-stu-id="f5cc0-108">Import a GPO from a File</span></span>](import-a-gpo-from-a-file-ed.md)

-   [<span data-ttu-id="f5cc0-109">Testar um GPO em uma unidade organizacional separada</span><span class="sxs-lookup"><span data-stu-id="f5cc0-109">Test a GPO in a Separate Organizational Unit</span></span>](test-a-gpo-in-a-separate-organizational-unit-agpm40.md)

<span data-ttu-id="f5cc0-110">**Observação**  Você também pode importar um GPO do ambiente de produção do domínio.</span><span class="sxs-lookup"><span data-stu-id="f5cc0-110">**Note** You can also import a GPO from the production environment of the domain.</span></span> <span data-ttu-id="f5cc0-111">Para obter mais informações, consulte [importar um GPO da produção](import-a-gpo-from-production-agpm40-ed.md).</span><span class="sxs-lookup"><span data-stu-id="f5cc0-111">For more information, see [Import a GPO from Production](import-a-gpo-from-production-agpm40-ed.md).</span></span>

 

 

 





