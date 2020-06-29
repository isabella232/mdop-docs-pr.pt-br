---
title: Definir um modelo padrão
description: Definir um modelo padrão
author: dansimp
ms.assetid: 07208b6b-cb3a-4f6c-9c84-36d4dc1486d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51a13c2c57e38adca883a6eb962d8c5eae4316db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797684"
---
# <span data-ttu-id="75877-103">Definir um modelo padrão</span><span class="sxs-lookup"><span data-stu-id="75877-103">Set a Default Template</span></span>


<span data-ttu-id="75877-104">Como um editor, você pode especificar quais dos modelos disponíveis serão o modelo padrão sugerido para todos os administradores de política de grupo criando novos objetos de política de grupo (GPOs).</span><span class="sxs-lookup"><span data-stu-id="75877-104">As an Editor, you can specify which of the available templates will be the default template suggested for all Group Policy administrators creating new Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="75877-105">**Observação**  Um modelo é uma versão não editável e estática de um GPO para uso como um ponto de partida para a criação de GPOs novos e editáveis.</span><span class="sxs-lookup"><span data-stu-id="75877-105">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="75877-106">Uma conta de usuário com a função de editor ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="75877-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="75877-107">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="75877-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="75877-108">Para definir o modelo padrão a ser usado ao criar novos GPOs</span><span class="sxs-lookup"><span data-stu-id="75877-108">To set the default template for use when creating new GPOs</span></span>**

1.  <span data-ttu-id="75877-109">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="75877-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="75877-110">Na guia **conteúdo** do painel detalhes, clique na guia **modelos** para exibir os modelos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="75877-110">On the **Contents** tab in the details pane, click the **Templates** tab to display available templates.</span></span>

3.  <span data-ttu-id="75877-111">Clique com o botão direito do mouse no modelo que deseja definir como padrão e, em seguida, clique em **definir como padrão**.</span><span class="sxs-lookup"><span data-stu-id="75877-111">Right-click the template that you want to set as the default, and then click **Set as Default**.</span></span>

4.  <span data-ttu-id="75877-112">Clique em **Sim** para confirmar.</span><span class="sxs-lookup"><span data-stu-id="75877-112">Click **Yes** to confirm.</span></span>

5.  <span data-ttu-id="75877-113">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="75877-113">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="75877-114">O modelo padrão tem um ícone azul e o estado é identificado como **modelo (padrão)** na guia **modelos** .</span><span class="sxs-lookup"><span data-stu-id="75877-114">The default template has a blue icon and the state is identified as **Template (default)** on the **Templates** tab.</span></span>

### <span data-ttu-id="75877-115">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="75877-115">Additional considerations</span></span>

-   <span data-ttu-id="75877-116">Por padrão, você deve ser um editor ou um administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="75877-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="75877-117">Especificamente, você deve ter **conteúdo de lista** e criar permissões de **modelo** para o domínio.</span><span class="sxs-lookup"><span data-stu-id="75877-117">Specifically, you must have **List Contents** and **Create Template** permissions for the domain.</span></span>

-   <span data-ttu-id="75877-118">Depois de definir um modelo como padrão, esse modelo será o primeiro selecionado na caixa de diálogo **novo GPO controlado** quando os administradores de política de grupo criarem novos GPOs.</span><span class="sxs-lookup"><span data-stu-id="75877-118">After you set a template as the default, that template will be the one initially selected in the **New Controlled GPO** dialog box when Group Policy administrators create new GPOs.</span></span> <span data-ttu-id="75877-119">No entanto, eles terão a opção de selecionar qualquer outro modelo de GPO, incluindo \*\* &lt; GPO &gt; vazio\*\*, que não inclui configurações.</span><span class="sxs-lookup"><span data-stu-id="75877-119">However, they will have the option to select any other GPO template, including **&lt;Empty GPO&gt;**, which does not include any settings.</span></span>

-   <span data-ttu-id="75877-120">Renomear ou excluir um modelo não afeta os GPOs criados a partir desse modelo.</span><span class="sxs-lookup"><span data-stu-id="75877-120">Renaming or deleting a template does not impact GPOs created from that template.</span></span>

-   <span data-ttu-id="75877-121">Como não pode ser alterado, um modelo não tem um histórico.</span><span class="sxs-lookup"><span data-stu-id="75877-121">Because it cannot be altered, a template does not have a history.</span></span>

### <span data-ttu-id="75877-122">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="75877-122">Additional references</span></span>

-   [<span data-ttu-id="75877-123">Criação de um modelo e ajuste de um modelo padrão</span><span class="sxs-lookup"><span data-stu-id="75877-123">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template-agpm40.md)

-   [<span data-ttu-id="75877-124">Solicitar a criação de um novo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="75877-124">Request the Creation of a New Controlled GPO</span></span>](request-the-creation-of-a-new-controlled-gpo-agpm40.md)

 

 





