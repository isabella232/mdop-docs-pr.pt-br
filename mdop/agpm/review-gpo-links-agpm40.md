---
title: Analisar links do GPO
description: Analisar links do GPO
author: dansimp
ms.assetid: 3aaba9da-f0aa-466f-bd1c-49f11d00ea54
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3884a6f3852986cf02e499af59bb56fcaf404ef8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797307"
---
# <span data-ttu-id="1fbc8-103">Analisar links do GPO</span><span class="sxs-lookup"><span data-stu-id="1fbc8-103">Review GPO Links</span></span>


<span data-ttu-id="1fbc8-104">Você pode exibir um diagrama que mostra onde um objeto de política de grupo (GPO) ou GPOs selecionados estão vinculados a unidades organizacionais.</span><span class="sxs-lookup"><span data-stu-id="1fbc8-104">You can display a diagram showing where a Group Policy Object (GPO) or GPOs that you select are linked to organizational units.</span></span> <span data-ttu-id="1fbc8-105">Os diagramas de link de GPO são atualizados toda vez que o GPO é controlado, importado ou verificado.</span><span class="sxs-lookup"><span data-stu-id="1fbc8-105">GPO link diagrams are updated each time the GPO is controlled, imported, or checked in.</span></span>

<span data-ttu-id="1fbc8-106">Uma conta de usuário com a função revisor, editor, Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="1fbc8-106">A user account with the Reviewer, Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM)is required to complete this procedure.</span></span> <span data-ttu-id="1fbc8-107">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="1fbc8-107">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="1fbc8-108">Revisão de links de GPO</span><span class="sxs-lookup"><span data-stu-id="1fbc8-108">Reviewing GPO links</span></span>


-   [<span data-ttu-id="1fbc8-109">Para um ou mais GPOs</span><span class="sxs-lookup"><span data-stu-id="1fbc8-109">For one or more GPOs</span></span>](#bkmk-gpos)

-   [<span data-ttu-id="1fbc8-110">Para uma ou mais versões de um GPO</span><span class="sxs-lookup"><span data-stu-id="1fbc8-110">For one or more versions of a GPO</span></span>](#bkmk-gpo-versions)

### <a href="" id="bkmk-gpos"></a>

**<span data-ttu-id="1fbc8-111">Para exibir links de GPO para um ou mais GPOs</span><span class="sxs-lookup"><span data-stu-id="1fbc8-111">To display GPO links for one or more GPOs</span></span>**

1.  <span data-ttu-id="1fbc8-112">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="1fbc8-112">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="1fbc8-113">Na guia **conteúdo** do painel detalhes, clique na guia **controlado**, **pendente**ou **Lixeira** para exibir os GPOs.</span><span class="sxs-lookup"><span data-stu-id="1fbc8-113">On the **Contents** tab in the details pane, click the **Controlled**, **Pending**, or **Recycle Bin** tab to display GPOs.</span></span>

3.  <span data-ttu-id="1fbc8-114">Selecione um ou mais GPOs para os quais exibir links, clique com o botão direito do mouse em um GPO selecionado, clique em **configurações**e, em seguida, clique em **vínculos de GPO** para exibir um diagrama de domínios e unidades organizacionais com links para o (s) GPO (s) selecionado (s).</span><span class="sxs-lookup"><span data-stu-id="1fbc8-114">Select one or more GPOs for which to display links, right-click a selected GPO, click **Settings**, and then click **GPO Links** to display a diagram of domains and organizational units with links to the selected GPO(s).</span></span>

### <a href="" id="bkmk-gpo-versions"></a>

**<span data-ttu-id="1fbc8-115">Para exibir links de GPO para uma ou mais versões de um GPO</span><span class="sxs-lookup"><span data-stu-id="1fbc8-115">To display GPO links for one or more versions of a GPO</span></span>**

1.  <span data-ttu-id="1fbc8-116">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="1fbc8-116">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="1fbc8-117">Na guia **conteúdo** do painel detalhes, clique na guia de **Lixeira** ou **controlado** para exibir os GPOs.</span><span class="sxs-lookup"><span data-stu-id="1fbc8-117">On the **Contents** tab in the details pane, click the **Controlled** or **Recycle Bin** tab to display GPOs.</span></span>

3.  <span data-ttu-id="1fbc8-118">Clique duas vezes no GPO para exibir seu histórico.</span><span class="sxs-lookup"><span data-stu-id="1fbc8-118">Double-click the GPO to display its history.</span></span>

4.  <span data-ttu-id="1fbc8-119">Clique com o botão direito do mouse na versão do GPO para a qual revisar as configurações, clique em **configurações**e, em seguida, clique em **relatório HTML** ou em **relatório XML** para exibir um resumo das configurações do GPO.</span><span class="sxs-lookup"><span data-stu-id="1fbc8-119">Right-click the GPO version for which to review the settings, click **Settings**, and then click **HTML Report** or **XML Report** to display a summary of the GPO's settings.</span></span>

### <span data-ttu-id="1fbc8-120">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="1fbc8-120">Additional considerations</span></span>

-   <span data-ttu-id="1fbc8-121">Por padrão, você deve ser um revisor, um editor, um Aprovador ou um administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="1fbc8-121">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="1fbc8-122">Especificamente, você deve ter permissões de **lista de conteúdo** e **ler configurações** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="1fbc8-122">Specifically, you must have **List Contents** and **Read Settings** permissions for the GPO.</span></span> <span data-ttu-id="1fbc8-123">Além disso, para exibir a lista de GPOs, você deve ter permissão de **lista de conteúdo** para o domínio.</span><span class="sxs-lookup"><span data-stu-id="1fbc8-123">Also, to display the list of GPOs, you must have **List Contents** permission for the domain.</span></span>

### <span data-ttu-id="1fbc8-124">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="1fbc8-124">Additional references</span></span>

-   [<span data-ttu-id="1fbc8-125">Execução de tarefas do revisor</span><span class="sxs-lookup"><span data-stu-id="1fbc8-125">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 





