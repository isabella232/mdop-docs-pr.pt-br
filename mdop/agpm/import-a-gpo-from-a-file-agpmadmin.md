---
title: Importar um GPO de um arquivo
description: Importar um GPO de um arquivo
author: dansimp
ms.assetid: 2cbcda72-4de3-47ad-aaf8-4fc7341d5a00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 04819dacac8df73f0a61cace0dab8b9fa79b7307
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797788"
---
# <span data-ttu-id="ea2b3-103">Importar um GPO de um arquivo</span><span class="sxs-lookup"><span data-stu-id="ea2b3-103">Import a GPO from a File</span></span>


<span data-ttu-id="ea2b3-104">No gerenciamento avançado de política de grupo (AGPM), se você for um administrador do AGPM (controle total) e exportou um objeto de política de grupo (GPO) para um arquivo CAB, poderá importar as configurações de política desse GPO para um novo GPO ou um GPO existente em um domínio em outra floresta.</span><span class="sxs-lookup"><span data-stu-id="ea2b3-104">In Advanced Group Policy Management (AGPM), if you are an AGPM Administrator (Full Control) and you have exported a Group Policy Object (GPO) to a CAB file, you can import the policy settings from that GPO into a new GPO or an existing GPO in a domain in another forest.</span></span> <span data-ttu-id="ea2b3-105">Para obter informações sobre como exportar configurações de GPO para um arquivo CAB, consulte [exportar um GPO para um arquivo](export-a-gpo-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="ea2b3-105">For information about exporting GPO settings to a CAB file, see [Export a GPO to a File](export-a-gpo-to-a-file.md).</span></span>

<span data-ttu-id="ea2b3-106">Uma conta de usuário com a função de administrador do AGPM ou as permissões necessárias no AGPM é necessária para importar as configurações de política para um novo GPO controlado.</span><span class="sxs-lookup"><span data-stu-id="ea2b3-106">A user account with the AGPM Administrator role or the necessary permissions in AGPM is required to import policy settings into a new controlled GPO.</span></span> <span data-ttu-id="ea2b3-107">Uma conta de usuário com a função de administrador ou administrador do AGPM ou permissões necessárias no AGPM é necessária para importar configurações de política para um GPO existente.</span><span class="sxs-lookup"><span data-stu-id="ea2b3-107">A user account with the Editor or AGPM Administrator role or necessary permissions in AGPM is required to import policy settings into an existing GPO.</span></span> <span data-ttu-id="ea2b3-108">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="ea2b3-108">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="ea2b3-109">Importando configurações de política de um arquivo</span><span class="sxs-lookup"><span data-stu-id="ea2b3-109">Importing policy settings from a file</span></span>


<span data-ttu-id="ea2b3-110">Ao importar configurações de política de um arquivo, você pode importá-las para um novo GPO ou um GPO existente.</span><span class="sxs-lookup"><span data-stu-id="ea2b3-110">When you import policy settings from a file, you can import them into a new GPO or an existing GPO.</span></span> <span data-ttu-id="ea2b3-111">No entanto, se você importar configurações de política para um GPO existente, todas as configurações de política dentro dela serão substituídas.</span><span class="sxs-lookup"><span data-stu-id="ea2b3-111">However, if you import policy settings into an existing GPO, all policy settings within it are replaced.</span></span>

-   [<span data-ttu-id="ea2b3-112">Importar configurações de política para um novo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="ea2b3-112">Import policy settings into a new controlled GPO</span></span>](#bkmk-new)

-   [<span data-ttu-id="ea2b3-113">Importar configurações de política para um GPO existente</span><span class="sxs-lookup"><span data-stu-id="ea2b3-113">Import policy settings into an existing GPO</span></span>](#bkmk-existing)

### <a href="" id="bkmk-new"></a>

**<span data-ttu-id="ea2b3-114">Para importar configurações de política para um novo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="ea2b3-114">To import policy settings into a new controlled GPO</span></span>**

1.  <span data-ttu-id="ea2b3-115">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** no domínio ao qual você deseja importar as configurações de política.</span><span class="sxs-lookup"><span data-stu-id="ea2b3-115">In the **Group Policy Management Console** tree, click **Change Control** in the domain to which you want to import policy settings.</span></span>

2.  <span data-ttu-id="ea2b3-116">Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="ea2b3-116">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="ea2b3-117">Crie um novo GPO controlado.</span><span class="sxs-lookup"><span data-stu-id="ea2b3-117">Create a new controlled GPO.</span></span> <span data-ttu-id="ea2b3-118">Na caixa de diálogo **novo GPO controlado** , clique em **importar** e, em seguida, clique em **Iniciar assistente**.</span><span class="sxs-lookup"><span data-stu-id="ea2b3-118">In the **New Controlled GPO** dialog box, click **Import** and then click **Launch Wizard**.</span></span> <span data-ttu-id="ea2b3-119">Para obter mais informações sobre como criar um GPO, consulte [criar um novo GPO controlado](create-a-new-controlled-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="ea2b3-119">For more information about how to create a GPO, see [Create a New Controlled GPO](create-a-new-controlled-gpo-agpm40.md).</span></span>

4.  <span data-ttu-id="ea2b3-120">Siga as instruções no **Assistente de importação de configurações** para selecionar um backup de GPO, importar configurações de política dele para o novo GPO e inserir um comentário para a faixa de auditoria do novo GPO.</span><span class="sxs-lookup"><span data-stu-id="ea2b3-120">Follow the instructions in the **Import Settings Wizard** to select a GPO backup, import policy settings from it for the new GPO, and enter a comment for the audit trail of the new GPO.</span></span>

### <a href="" id="bkmk-existing"></a>

**<span data-ttu-id="ea2b3-121">Para importar configurações de política para um GPO existente</span><span class="sxs-lookup"><span data-stu-id="ea2b3-121">To import policy settings into an existing GPO</span></span>**

1.  <span data-ttu-id="ea2b3-122">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** no domínio ao qual você deseja importar as configurações de política.</span><span class="sxs-lookup"><span data-stu-id="ea2b3-122">In the **Group Policy Management Console** tree, click **Change Control** in the domain to which you want to import policy settings.</span></span>

2.  <span data-ttu-id="ea2b3-123">Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="ea2b3-123">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="ea2b3-124">Verifique o GPO de destino para o qual você deseja importar as configurações de política.</span><span class="sxs-lookup"><span data-stu-id="ea2b3-124">Check out the destination GPO to which you want to import policy settings.</span></span>

4.  <span data-ttu-id="ea2b3-125">Clique com o botão direito do mouse no GPO de destino, aponte para **importar de**e clique em **arquivo**.</span><span class="sxs-lookup"><span data-stu-id="ea2b3-125">Right-click the destination GPO, point to **Import from**, and then click **File**.</span></span>

5.  <span data-ttu-id="ea2b3-126">Siga as instruções no **Assistente de importação de configurações** para selecionar um backup de GPO, importar suas configurações de política para substituir as do GPO de destino e inserir um comentário para a faixa de auditoria do GPO de destino.</span><span class="sxs-lookup"><span data-stu-id="ea2b3-126">Follow the instructions in the **Import Settings Wizard** to select a GPO backup, import its policy settings to replace those in the destination GPO, and enter a comment for the audit trail of the destination GPO.</span></span> <span data-ttu-id="ea2b3-127">Por padrão, o GPO de destino é verificado quando o assistente é concluído.</span><span class="sxs-lookup"><span data-stu-id="ea2b3-127">By default, the destination GPO is checked in when the wizard is finished.</span></span>

### <span data-ttu-id="ea2b3-128">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="ea2b3-128">Additional considerations</span></span>

-   <span data-ttu-id="ea2b3-129">Para importar configurações de política para um novo GPO controlado, você deve ter o **conteúdo da lista**, **importar GPO**e criar permissões de **GPO** para o domínio.</span><span class="sxs-lookup"><span data-stu-id="ea2b3-129">To import policy settings to a new controlled GPO, you must have **List Contents**, **Import GPO**, and **Create GPO** permissions for the domain.</span></span> <span data-ttu-id="ea2b3-130">Por padrão, você deve ser um administrador do AGPM para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="ea2b3-130">By default, you must be an AGPM Administrator to perform this procedure.</span></span>

-   <span data-ttu-id="ea2b3-131">Para importar configurações de política para um GPO existente, você deve ter a **lista de conteúdo**, **Editar configurações**e importar permissões de **GPO** para o domínio, e o GPO deve ser verificado por você.</span><span class="sxs-lookup"><span data-stu-id="ea2b3-131">To import policy settings to an existing GPO, you must have **List Contents**, **Edit Settings**, and **Import GPO** permissions for the domain, and the GPO must be checked out by you.</span></span> <span data-ttu-id="ea2b3-132">Por padrão, você deve ser um editor ou um administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="ea2b3-132">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span>

### <span data-ttu-id="ea2b3-133">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="ea2b3-133">Additional references</span></span>

-   [<span data-ttu-id="ea2b3-134">Gerenciamento do arquivo morto</span><span class="sxs-lookup"><span data-stu-id="ea2b3-134">Managing the Archive</span></span>](managing-the-archive-agpm40.md)

 

 





