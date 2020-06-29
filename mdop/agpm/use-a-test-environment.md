---
title: Usar um ambiente de teste
description: Usar um ambiente de teste
author: dansimp
ms.assetid: b8d7b3ee-030a-4b5b-8223-4a3276fd47a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2299fb6eaf7c75f6841056f67a05fe025ea19bb7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797284"
---
# <span data-ttu-id="f1ad3-103">Usar um ambiente de teste</span><span class="sxs-lookup"><span data-stu-id="f1ad3-103">Use a Test Environment</span></span>


<span data-ttu-id="f1ad3-104">Se você usar uma UO (unidade organizacional de teste) para testar objetos de política de grupo (GPOs) antes da implantação para o ambiente de produção, você deve ter as permissões necessárias para acessar a OU de teste.</span><span class="sxs-lookup"><span data-stu-id="f1ad3-104">If you use a testing organizational unit (OU) to test Group Policy objects (GPOs) before deployment to the production environment, you must have the necessary permissions to access the test OU.</span></span> <span data-ttu-id="f1ad3-105">O uso de uma OU de teste é opcional.</span><span class="sxs-lookup"><span data-stu-id="f1ad3-105">The use of a test OU is optional.</span></span>

**<span data-ttu-id="f1ad3-106">Para usar uma OU de teste</span><span class="sxs-lookup"><span data-stu-id="f1ad3-106">To use a test OU</span></span>**

1.  <span data-ttu-id="f1ad3-107">Enquanto o GPO tiver sido verificado para edição, no console de **Gerenciamento de política de grupo**, clique em **objetos de política de grupo** na floresta e no domínio em que você está gerenciando GPOs.</span><span class="sxs-lookup"><span data-stu-id="f1ad3-107">While you have the GPO checked out for editing, in the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you are managing GPOs.</span></span>

2.  <span data-ttu-id="f1ad3-108">Clique na cópia checked-out do GPO a ser testado.</span><span class="sxs-lookup"><span data-stu-id="f1ad3-108">Click the checked out copy of the GPO to be tested.</span></span> <span data-ttu-id="f1ad3-109">O nome será precedido de **\ [AGPM \]**.</span><span class="sxs-lookup"><span data-stu-id="f1ad3-109">The name will be preceded with **\[AGPM\]**.</span></span> <span data-ttu-id="f1ad3-110">(Se não estiver listado, clique em **ação**e em **Atualizar**.</span><span class="sxs-lookup"><span data-stu-id="f1ad3-110">(If it is not listed, click **Action**, then **Refresh**.</span></span> <span data-ttu-id="f1ad3-111">Classifique os nomes em ordem alfabética, e **\ [AGPM \]** os GPOs geralmente aparecem na parte superior da lista.)</span><span class="sxs-lookup"><span data-stu-id="f1ad3-111">Sort the names alphabetically, and **\[AGPM\]** GPOs will typically appear at the top of the list.)</span></span>

3.  <span data-ttu-id="f1ad3-112">Arraste e solte o GPO na OU Test OU.</span><span class="sxs-lookup"><span data-stu-id="f1ad3-112">Drag and drop the GPO to the test OU.</span></span>

4.  <span data-ttu-id="f1ad3-113">Clique em **OK** na caixa de diálogo para perguntar se deseja criar um link para o GPO na OU Test ou.</span><span class="sxs-lookup"><span data-stu-id="f1ad3-113">Click **OK** in the dialog box asking whether to create a link to the GPO in the test OU.</span></span>

### <span data-ttu-id="f1ad3-114">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="f1ad3-114">Additional considerations</span></span>

-   <span data-ttu-id="f1ad3-115">Quando o teste estiver concluído, fazer check-in do GPO excluirá automaticamente o link para a cópia checked-out do GPO.</span><span class="sxs-lookup"><span data-stu-id="f1ad3-115">When testing is complete, checking in the GPO automatically deletes the link to the checked-out copy of the GPO.</span></span>

### <span data-ttu-id="f1ad3-116">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="f1ad3-116">Additional references</span></span>

-   [<span data-ttu-id="f1ad3-117">Editando um GPO</span><span class="sxs-lookup"><span data-stu-id="f1ad3-117">Editing a GPO</span></span>](editing-a-gpo.md)

 

 





