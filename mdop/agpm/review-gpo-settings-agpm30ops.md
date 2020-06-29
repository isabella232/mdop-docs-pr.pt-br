---
title: Analisar configurações do GPO
description: Analisar configurações do GPO
author: dansimp
ms.assetid: bed956d0-082e-4fa9-bf1e-572d0d3d02ec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 23d18eb5a41b4246964b79f687eb9fa44b98b730
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797305"
---
# <span data-ttu-id="dcf60-103">Analisar configurações do GPO</span><span class="sxs-lookup"><span data-stu-id="dcf60-103">Review GPO Settings</span></span>


<span data-ttu-id="dcf60-104">Você pode gerar relatórios baseados em HTML e baseados em XML para revisar as configurações dentro de qualquer versão de um objeto de política de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="dcf60-104">You can generate HTML-based and XML-based reports for reviewing settings within any version of a Group Policy Object (GPO).</span></span>

<span data-ttu-id="dcf60-105">Uma conta de usuário com a função revisor, editor, Aprovador ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="dcf60-105">A user account with the Reviewer, Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM)is required to complete this procedure.</span></span> <span data-ttu-id="dcf60-106">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="dcf60-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="dcf60-107">Para revisar as configurações em qualquer versão de um GPO</span><span class="sxs-lookup"><span data-stu-id="dcf60-107">To review settings in any version of a GPO</span></span>**

1.  <span data-ttu-id="dcf60-108">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="dcf60-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="dcf60-109">Na guia **conteúdo** do painel detalhes, clique em uma guia para exibir os GPOs.</span><span class="sxs-lookup"><span data-stu-id="dcf60-109">On the **Contents** tab in the details pane, click a tab to display GPOs.</span></span>

3.  <span data-ttu-id="dcf60-110">Clique duas vezes no GPO para exibir seu histórico.</span><span class="sxs-lookup"><span data-stu-id="dcf60-110">Double-click the GPO to display its history.</span></span>

4.  <span data-ttu-id="dcf60-111">Clique com o botão direito do mouse na versão do GPO para a qual revisar as configurações, clique em **configurações**e, em seguida, clique em **relatório HTML** ou em **relatório XML** para exibir um resumo das configurações do GPO.</span><span class="sxs-lookup"><span data-stu-id="dcf60-111">Right-click the GPO version for which to review the settings, click **Settings**, and then click **HTML Report** or **XML Report** to display a summary of the GPO's settings.</span></span>

### <span data-ttu-id="dcf60-112">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="dcf60-112">Additional considerations</span></span>

-   <span data-ttu-id="dcf60-113">Por padrão, você deve ser um revisor, um editor, um Aprovador ou um administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="dcf60-113">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="dcf60-114">Especificamente, você deve ter permissões de **lista de conteúdo** e **ler configurações** para o GPO.</span><span class="sxs-lookup"><span data-stu-id="dcf60-114">Specifically, you must have **List Contents** and **Read Settings** permissions for the GPO.</span></span> <span data-ttu-id="dcf60-115">Além disso, para exibir a lista de GPOs, você deve ter permissão de **lista de conteúdo** para o domínio.</span><span class="sxs-lookup"><span data-stu-id="dcf60-115">Also, to display the list of GPOs, you must have **List Contents** permission for the domain.</span></span>

### <span data-ttu-id="dcf60-116">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="dcf60-116">Additional references</span></span>

-   [<span data-ttu-id="dcf60-117">Execução de tarefas do revisor</span><span class="sxs-lookup"><span data-stu-id="dcf60-117">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

 

 





