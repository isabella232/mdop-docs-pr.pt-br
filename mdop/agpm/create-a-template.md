---
title: Criar um modelo
description: Criar um modelo
author: dansimp
ms.assetid: 6992bd55-4a4f-401f-9815-c468bac598ef
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9ad57204170fc3f49b01b571d82b00e1faf62de0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797851"
---
# <span data-ttu-id="3f269-103">Criar um modelo</span><span class="sxs-lookup"><span data-stu-id="3f269-103">Create a Template</span></span>


<span data-ttu-id="3f269-104">A criação de um modelo permite que você salve todas as configurações de uma versão específica de um objeto de política de grupo (GPO) para usar como ponto de partida para a criação de novos GPOs.</span><span class="sxs-lookup"><span data-stu-id="3f269-104">Creating a template enables you to save all of the settings of a particular version of a Group Policy object (GPO) to use as a starting point for creating new GPOs.</span></span>

<span data-ttu-id="3f269-105">**Observação**  Um modelo é uma versão não editável e estática de um GPO para uso como um ponto de partida para a criação de GPOs novos e editáveis.</span><span class="sxs-lookup"><span data-stu-id="3f269-105">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="3f269-106">Uma conta de usuário com a função de editor ou administrador do AGPM (controle total) ou permissões necessárias no gerenciamento avançado de política de grupo é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="3f269-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="3f269-107">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="3f269-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="3f269-108">Para criar um modelo com base em um GPO existente</span><span class="sxs-lookup"><span data-stu-id="3f269-108">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="3f269-109">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="3f269-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="3f269-110">Na guia **conteúdo** do painel detalhes, clique na guia **controlado** ou não **controlado** para exibir os GPOs disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3f269-110">On the **Contents** tab in the details pane, click the **Controlled** or **Uncontrolled** tab to display available GPOs.</span></span>

3.  <span data-ttu-id="3f269-111">Clique com o botão direito do mouse no GPO do qual você deseja criar um modelo e, em seguida, clique em **salvar como modelo**.</span><span class="sxs-lookup"><span data-stu-id="3f269-111">Right-click the GPO from which you want to create a template, then click **Save as Template**.</span></span>

4.  <span data-ttu-id="3f269-112">Digite um nome para o modelo e um comentário e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="3f269-112">Type a name for the template and a comment, then click **OK**.</span></span>

5.  <span data-ttu-id="3f269-113">Quando a janela de **progresso** indicar que o progresso geral foi concluído, clique em **fechar**.</span><span class="sxs-lookup"><span data-stu-id="3f269-113">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="3f269-114">O novo modelo aparece na guia **modelos** .</span><span class="sxs-lookup"><span data-stu-id="3f269-114">The new template appears on the **Templates** tab.</span></span>

### <span data-ttu-id="3f269-115">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="3f269-115">Additional considerations</span></span>

-   <span data-ttu-id="3f269-116">Por padrão, você deve ser um editor ou um administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="3f269-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="3f269-117">Especificamente, você deve ter **conteúdo de lista** e criar permissões de **modelo** para o domínio.</span><span class="sxs-lookup"><span data-stu-id="3f269-117">Specifically, you must have **List Contents** and **Create Template** permissions for the domain.</span></span>

-   <span data-ttu-id="3f269-118">Renomear ou excluir um modelo não afeta os GPOs criados a partir desse modelo.</span><span class="sxs-lookup"><span data-stu-id="3f269-118">Renaming or deleting a template does not impact GPOs created from that template.</span></span>

-   <span data-ttu-id="3f269-119">Como não pode ser alterado, um modelo não tem um histórico.</span><span class="sxs-lookup"><span data-stu-id="3f269-119">Because it cannot be altered, a template does not have a history.</span></span>

### <span data-ttu-id="3f269-120">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="3f269-120">Additional references</span></span>

-   [<span data-ttu-id="3f269-121">Criação de um modelo e ajuste de um modelo padrão</span><span class="sxs-lookup"><span data-stu-id="3f269-121">Creating a Template and Setting a Default Template</span></span>](creating-a-template-and-setting-a-default-template.md)

-   [<span data-ttu-id="3f269-122">Solicitar a criação de um novo GPO controlado</span><span class="sxs-lookup"><span data-stu-id="3f269-122">Request the Creation of a New Controlled GPO</span></span>](request-the-creation-of-a-new-controlled-gpo.md)

 

 





