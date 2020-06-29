---
title: Testar um GPO em uma unidade organizacional separada
description: Testar um GPO em uma unidade organizacional separada
author: dansimp
ms.assetid: 9a9e6d22-74e6-41d8-ac2f-12a1b76ad5a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 509721fdd775c8669399549f6dcc29cb9ebaea2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797289"
---
# <span data-ttu-id="ece8a-103">Testar um GPO em uma unidade organizacional separada</span><span class="sxs-lookup"><span data-stu-id="ece8a-103">Test a GPO in a Separate Organizational Unit</span></span>


<span data-ttu-id="ece8a-104">Se você usar uma unidade organizacional de teste (OU) para testar objetos de política de grupo (GPOs) no mesmo domínio antes da implantação para o ambiente de produção, você deve ter as permissões necessárias para acessar a OU de teste.</span><span class="sxs-lookup"><span data-stu-id="ece8a-104">If you use a testing organizational unit (OU) to test Group Policy Objects (GPOs) within the same domain before deployment to the production environment, you must have the necessary permissions to access the test OU.</span></span> <span data-ttu-id="ece8a-105">Usar uma OU de teste é opcional.</span><span class="sxs-lookup"><span data-stu-id="ece8a-105">Using a test OU is optional.</span></span>

**<span data-ttu-id="ece8a-106">Para usar uma OU de teste</span><span class="sxs-lookup"><span data-stu-id="ece8a-106">To use a test OU</span></span>**

1.  <span data-ttu-id="ece8a-107">Embora você tenha feito o check-out do GPO para edição, no **console de gerenciamento de política de grupo**, clique em objetos de política de **grupo** na floresta e no domínio em que você está gerenciando GPOs.</span><span class="sxs-lookup"><span data-stu-id="ece8a-107">Although you have the GPO checked out for editing, in the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you are managing GPOs.</span></span>

2.  <span data-ttu-id="ece8a-108">Clique na cópia checked-out do GPO a ser testado.</span><span class="sxs-lookup"><span data-stu-id="ece8a-108">Click the checked out copy of the GPO to be tested.</span></span> <span data-ttu-id="ece8a-109">O nome será precedido por **\ [AGPM \]**.</span><span class="sxs-lookup"><span data-stu-id="ece8a-109">The name will be preceded by **\[AGPM\]**.</span></span> <span data-ttu-id="ece8a-110">(Se não estiver listado, clique em **ação**e em **Atualizar**.</span><span class="sxs-lookup"><span data-stu-id="ece8a-110">(If it is not listed, click **Action**, then **Refresh**.</span></span> <span data-ttu-id="ece8a-111">Classifique os nomes em ordem alfabética, e **\ [AGPM \]** os GPOs geralmente aparecem na parte superior da lista.)</span><span class="sxs-lookup"><span data-stu-id="ece8a-111">Sort the names alphabetically, and **\[AGPM\]** GPOs will typically appear at the top of the list.)</span></span>

3.  <span data-ttu-id="ece8a-112">Arraste o GPO para a OU Test.</span><span class="sxs-lookup"><span data-stu-id="ece8a-112">Drag the GPO to the test OU.</span></span>

4.  <span data-ttu-id="ece8a-113">Clique em **OK** na caixa de diálogo que pergunta se deve criar um link para o GPO na OU Test ou.</span><span class="sxs-lookup"><span data-stu-id="ece8a-113">Click **OK** in the dialog box that asks whether to create a link to the GPO in the test OU.</span></span>

### <span data-ttu-id="ece8a-114">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="ece8a-114">Additional considerations</span></span>

-   <span data-ttu-id="ece8a-115">Quando o teste estiver concluído, fazer check-in do GPO excluirá automaticamente o link para a cópia checked-out do GPO.</span><span class="sxs-lookup"><span data-stu-id="ece8a-115">When testing is complete, checking in the GPO automatically deletes the link to the checked-out copy of the GPO.</span></span>

### <span data-ttu-id="ece8a-116">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="ece8a-116">Additional references</span></span>

-   [<span data-ttu-id="ece8a-117">Como usar um ambiente de teste</span><span class="sxs-lookup"><span data-stu-id="ece8a-117">Using a Test Environment</span></span>](using-a-test-environment.md)

 

 





