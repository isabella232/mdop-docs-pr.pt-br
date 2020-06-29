---
title: Importar um GPO de produção
description: Importar um GPO de produção
author: dansimp
ms.assetid: ad90f13e-e73c-400f-b86f-c12f2e75d19d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c78cba0f69bf282fb720051fc1c074b41ec0a6c4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797774"
---
# <span data-ttu-id="45038-103">Importar um GPO de produção</span><span class="sxs-lookup"><span data-stu-id="45038-103">Import a GPO from Production</span></span>


<span data-ttu-id="45038-104">Se forem feitas alterações em um objeto de política de grupo (GPO) controlado fora do gerenciamento avançado de política de grupo (AGPM), você poderá importar uma cópia do GPO do ambiente de produção e salvá-la no arquivo para colocar o arquivo morto e o ambiente de produção em um estado consistente.</span><span class="sxs-lookup"><span data-stu-id="45038-104">If changes are made to a controlled Group Policy Object (GPO) outside of Advanced Group Policy Management (AGPM), you can import a copy of the GPO from the production environment and save it to the archive to bring the archive and the production environment to a consistent state.</span></span> <span data-ttu-id="45038-105">Para importar um GPO não controlado, controle o GPO.</span><span class="sxs-lookup"><span data-stu-id="45038-105">(To import an uncontrolled GPO, control the GPO.</span></span> <span data-ttu-id="45038-106">Consulte [controlar um GPO não controlado](control-an-uncontrolled-gpo-agpm30ops.md).)</span><span class="sxs-lookup"><span data-stu-id="45038-106">See [Control an Uncontrolled GPO](control-an-uncontrolled-gpo-agpm30ops.md).)</span></span>

<span data-ttu-id="45038-107">Uma conta de usuário com a função de editor, Aprovador ou administrador do AGPM (controle total) ou permissões necessárias inexigidamente é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="45038-107">A user account with the Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions inAGPM is required to complete this procedure.</span></span> <span data-ttu-id="45038-108">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="45038-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="45038-109">Para importar um GPO do ambiente de produção</span><span class="sxs-lookup"><span data-stu-id="45038-109">To import a GPO from the production environment</span></span>**

1.  <span data-ttu-id="45038-110">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="45038-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="45038-111">Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="45038-111">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="45038-112">Clique com o botão direito do mouse no GPO e, em seguida, clique em **importar da produção**.</span><span class="sxs-lookup"><span data-stu-id="45038-112">Right-click the GPO, and then click **Import from Production**.</span></span>

4.  <span data-ttu-id="45038-113">Digite um comentário para a faixa de auditoria do GPO e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="45038-113">Type a comment for the audit trail of the GPO, and then click **OK**.</span></span>

### <span data-ttu-id="45038-114">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="45038-114">Additional considerations</span></span>

-   <span data-ttu-id="45038-115">Por padrão, você deve ser um editor, Aprovador ou administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="45038-115">By default, you must be an Editor, Approver, or AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="45038-116">Especificamente, você deve ter **conteúdo da lista** e **Editar as configurações**, **implantar o GPO**ou excluir permissões de **GPO** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="45038-116">Specifically, you must have **List Contents** and either **Edit Settings**, **Deploy GPO**, or **Delete GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="45038-117">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="45038-117">Additional references</span></span>

-   [<span data-ttu-id="45038-118">Criação, controle ou importação de um GPO</span><span class="sxs-lookup"><span data-stu-id="45038-118">Creating, Controlling, or Importing a GPO</span></span>](creating-controlling-or-importing-a-gpo-editor-agpm30ops.md)

 

 





