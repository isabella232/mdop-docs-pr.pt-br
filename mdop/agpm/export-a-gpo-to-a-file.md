---
title: Exportar um GPO para um arquivo
description: Exportar um GPO para um arquivo
author: dansimp
ms.assetid: 0d01b1f7-a6a4-4d0d-9aa7-2d6f1ae93d9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4622930cb0e5b439649cc0445ae2b3d02d7d3224
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797808"
---
# <span data-ttu-id="d092e-103">Exportar um GPO para um arquivo</span><span class="sxs-lookup"><span data-stu-id="d092e-103">Export a GPO to a File</span></span>


<span data-ttu-id="d092e-104">Você pode exportar um GPO (objeto de política de grupo) controlado para um arquivo CAB para poder copiá-lo para um domínio em outra floresta e importar o GPO para o gerenciamento avançado de política de grupo (AGPM) nesse domínio.</span><span class="sxs-lookup"><span data-stu-id="d092e-104">You can export a controlled Group Policy Object (GPO) to a CAB file so that you can copy it to a domain in another forest and import the GPO into Advanced Group Policy Management (AGPM) in that domain.</span></span> <span data-ttu-id="d092e-105">Para obter informações sobre como importar configurações de GPO para um GPO novo ou existente, consulte [importar um GPO de um arquivo](import-a-gpo-from-a-file-ed.md).</span><span class="sxs-lookup"><span data-stu-id="d092e-105">For information about how to import GPO settings into a new or existing GPO, see [Import a GPO from a File](import-a-gpo-from-a-file-ed.md).</span></span>

<span data-ttu-id="d092e-106">Uma conta de usuário com a função de editor ou administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="d092e-106">A user account with the Editor or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span><span data-ttu-id="d092e-107">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="d092e-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="d092e-108">Para exportar um GPO para um arquivo</span><span class="sxs-lookup"><span data-stu-id="d092e-108">To export a GPO to a file</span></span>**

1.  <span data-ttu-id="d092e-109">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="d092e-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="d092e-110">Na guia **conteúdo** , clique na guia **controlado** para exibir os GPOs controlados.</span><span class="sxs-lookup"><span data-stu-id="d092e-110">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="d092e-111">Clique com o botão direito do mouse no GPO e, em seguida, clique em **exportar para**.</span><span class="sxs-lookup"><span data-stu-id="d092e-111">Right-click the GPO, and then click **Export to**.</span></span>

4.  <span data-ttu-id="d092e-112">Insira um nome de arquivo para o arquivo para o qual você deseja exportar o GPO e, em seguida, clique em **Exportar**.</span><span class="sxs-lookup"><span data-stu-id="d092e-112">Enter a file name for the file to which you want to export the GPO, and then click **Export**.</span></span> <span data-ttu-id="d092e-113">Se o arquivo não existir, ele será criado.</span><span class="sxs-lookup"><span data-stu-id="d092e-113">If the file does not exist, it is created.</span></span> <span data-ttu-id="d092e-114">Se ele já existir, será substituído.</span><span class="sxs-lookup"><span data-stu-id="d092e-114">If it already exists, it is replaced.</span></span>

### <span data-ttu-id="d092e-115">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="d092e-115">Additional considerations</span></span>

-   <span data-ttu-id="d092e-116">Por padrão, você deve ser um editor ou um administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="d092e-116">By default, you must be an Editor or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="d092e-117">Especificamente, você deve ter **conteúdo da lista**, **ler configurações**e **Exportar** permissões de GPO para o GPO.</span><span class="sxs-lookup"><span data-stu-id="d092e-117">Specifically, you must have **List Contents**, **Read Settings**, and **Export GPO** permissions for the GPO.</span></span>

### <span data-ttu-id="d092e-118">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="d092e-118">Additional references</span></span>

-   [<span data-ttu-id="d092e-119">Como usar um ambiente de teste</span><span class="sxs-lookup"><span data-stu-id="d092e-119">Using a Test Environment</span></span>](using-a-test-environment.md)

 

 





