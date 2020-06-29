---
title: Criar um modelo
description: Criar um modelo
author: dansimp
ms.assetid: b38423af-7d24-437a-98bc-01f1ae891127
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd50dd41863e383b931b8563854a8bbd4ee196d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797852"
---
# <span data-ttu-id="5ddd4-103">Criar um modelo</span><span class="sxs-lookup"><span data-stu-id="5ddd4-103">Create a Template</span></span>


<span data-ttu-id="5ddd4-104">A criação de um modelo permite que você salve todas as configurações de uma versão específica de um objeto de política de grupo (GPO) para usar como ponto de partida para a criação de novos GPOs.</span><span class="sxs-lookup"><span data-stu-id="5ddd4-104">Creating a template enables you to save all of the settings of a particular version of a Group Policy Object (GPO) to use as a starting point for creating new GPOs.</span></span>

<span data-ttu-id="5ddd4-105">**Observação**  Um modelo é uma versão não editável e estática de um GPO para uso como um ponto de partida para a criação de GPOs novos e editáveis.</span><span class="sxs-lookup"><span data-stu-id="5ddd4-105">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="5ddd4-106">Uma conta de usuário com a função de editor ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="5ddd4-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="5ddd4-107">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="5ddd4-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="5ddd4-108">Para criar um modelo com base em um GPO existente</span><span class="sxs-lookup"><span data-stu-id="5ddd4-108">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="5ddd4-109">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="5ddd4-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="5ddd4-110">Na guia **conteúdo** do painel detalhes, clique na guia **controlado** ou não **controlado** para exibir os GPOs disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5ddd4-110">On the **Contents** tab in the details pane, click the **Controlled** or **Uncontrolled** tab to display available GPOs.</span></span>

3.  <span data-ttu-id="5ddd4-111">Clique com o botão direito do mouse no GPO do qual você deseja criar um modelo e, em seguida, clique em **salvar como modelo**.</span><span class="sxs-lookup"><span data-stu-id="5ddd4-111">Right-click the GPO from which you want to create a template, and then click **Save as Template**.</span></span>

4.  <span data-ttu-id="5ddd4-112">Digite um nome para o modelo e um comentário e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ddd4-112">Type a name for the template and a comment, and then click **OK**.</span></span>

5.  <span data-ttu-id="5ddd4-113">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="5ddd4-113">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="5ddd4-114">O novo modelo aparece na guia **modelos** .</span><span class="sxs-lookup"><span data-stu-id="5ddd4-114">The new template appears on the **Templates** tab.</span></span>

### <span data-ttu-id="5ddd4-115">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="5ddd4-115">Additional considerations</span></span>

-   <span data-ttu-id="5ddd4-116">Por padrão, você deve ser um editor ou um administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="5ddd4-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="5ddd4-117">Especificamente, você deve ter **conteúdo de lista** e criar permissões de **modelo** para o domínio.</span><span class="sxs-lookup"><span data-stu-id="5ddd4-117">Specifically, you must have **List Contents** and **Create Template** permissions for the domain.</span></span>

-   <span data-ttu-id="5ddd4-118">Renomear ou excluir um modelo não afeta os GPOs criados a partir desse modelo.</span><span class="sxs-lookup"><span data-stu-id="5ddd4-118">Renaming or deleting a template does not impact GPOs created from that template.</span></span>

-   <span data-ttu-id="5ddd4-119">Como não pode ser alterado, um modelo não tem um histórico.</span><span class="sxs-lookup"><span data-stu-id="5ddd4-119">Because it cannot be altered, a template does not have a history.</span></span>

### <span data-ttu-id="5ddd4-120">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="5ddd4-120">Additional references</span></span>

-   [<span data-ttu-id="5ddd4-121">Criação de um modelo e ajuste de um modelo padrão</span><span class="sxs-lookup"><span data-stu-id="5ddd4-121">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template-agpm40.md)

-   [<span data-ttu-id="5ddd4-122">Solicitar a criação de um novo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="5ddd4-122">Request the Creation of a New Controlled GPO</span></span>](request-the-creation-of-a-new-controlled-gpo-agpm40.md)

 

 





