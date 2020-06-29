---
title: Limitar as versões de GPO armazenadas
description: Limitar as versões de GPO armazenadas
author: dansimp
ms.assetid: da14edc5-0c36-4c54-b122-861c86b99eb1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 20a3ae60cc330c27cbd19e943ba7f071d4ec60b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797762"
---
# <span data-ttu-id="e96e1-103">Limitar as versões de GPO armazenadas</span><span class="sxs-lookup"><span data-stu-id="e96e1-103">Limit the GPO Versions Stored</span></span>


<span data-ttu-id="e96e1-104">Por padrão, todas as versões de cada objeto de política de grupo controlado (GPO) são mantidas no arquivo morto no servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="e96e1-104">By default, all versions of every controlled Group Policy Object (GPO) are retained in the archive on the AGPM Server.</span></span> <span data-ttu-id="e96e1-105">No entanto, você pode limitar o número de versões retidas para cada GPO e excluir versões mais antigas quando esse limite for excedido.</span><span class="sxs-lookup"><span data-stu-id="e96e1-105">However, you can limit the number of versions retained for each GPO and delete older versions when that limit is exceeded.</span></span> <span data-ttu-id="e96e1-106">Quando as versões do GPO são excluídas, um registro da versão permanece no histórico do GPO, mas a própria versão do GPO é excluída do arquivamento.</span><span class="sxs-lookup"><span data-stu-id="e96e1-106">When GPO versions are deleted, a record of the version remains in the history of the GPO, but the GPO version itself is deleted from the archive.</span></span>

<span data-ttu-id="e96e1-107">Uma conta de usuário com a função de administrador do AGPM (controle total) ou permissões necessárias no AGPM (gerenciamento avançado de política de grupo) é necessária para concluir este procedimento.</span><span class="sxs-lookup"><span data-stu-id="e96e1-107">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="e96e1-108">Examine os detalhes em "considerações adicionais" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="e96e1-108">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="e96e1-109">Para limitar o número de versões de GPO armazenadas</span><span class="sxs-lookup"><span data-stu-id="e96e1-109">To limit the number of GPO versions stored</span></span>**

1.  <span data-ttu-id="e96e1-110">Na árvore do **console de gerenciamento de política de grupo** , clique em **alterar controle** na floresta e no domínio dos quais você deseja gerenciar GPOs.</span><span class="sxs-lookup"><span data-stu-id="e96e1-110">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="e96e1-111">No painel detalhes, clique na guia **servidor do AGPM** .</span><span class="sxs-lookup"><span data-stu-id="e96e1-111">In the details pane, click the **AGPM Server** tab.</span></span>

3.  <span data-ttu-id="e96e1-112">Marque a caixa de seleção **Excluir versões antigas de cada GPO da lista de arquivos** e digite o número máximo de versões de GPO a serem armazenadas para cada GPO, não incluindo a versão atual.</span><span class="sxs-lookup"><span data-stu-id="e96e1-112">Select the **Delete old versions of each GPO from the archive** check box, and type the maximum number of GPO versions to store for each GPO, not including the current version.</span></span> <span data-ttu-id="e96e1-113">Para reter apenas a versão atual, digite 0.</span><span class="sxs-lookup"><span data-stu-id="e96e1-113">To retain only the current version, enter 0.</span></span> <span data-ttu-id="e96e1-114">O máximo não deve ser maior do que 999.</span><span class="sxs-lookup"><span data-stu-id="e96e1-114">The maximum must be no greater than 999.</span></span>

    <span data-ttu-id="e96e1-115">**Importante**  Somente as versões de GPO exibidas na guia **versões exclusivas** da janela do **histórico** contam para o limite.</span><span class="sxs-lookup"><span data-stu-id="e96e1-115">**Important** Only GPO versions displayed on the **Unique Versions** tab of the **History** window count toward the limit.</span></span>

     

4.  <span data-ttu-id="e96e1-116">Clique no botão **aplicar** .</span><span class="sxs-lookup"><span data-stu-id="e96e1-116">Click the **Apply** button.</span></span>

### <span data-ttu-id="e96e1-117">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="e96e1-117">Additional considerations</span></span>

-   <span data-ttu-id="e96e1-118">Por padrão, você deve ser um administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="e96e1-118">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="e96e1-119">Especificamente, você deve ter permissões de **lista de conteúdo** e **Opções de modificação** para o domínio.</span><span class="sxs-lookup"><span data-stu-id="e96e1-119">Specifically, you must have **List Contents** and **Modify Options** permissions for the domain.</span></span>

-   <span data-ttu-id="e96e1-120">Você pode impedir que uma versão do GPO seja excluída marcando-a no histórico como não qualificado para exclusão.</span><span class="sxs-lookup"><span data-stu-id="e96e1-120">You can prevent a GPO version from being deleted by marking it in the history as ineligible for deletion.</span></span> <span data-ttu-id="e96e1-121">Para fazer isso, clique com o botão direito do mouse na versão no histórico do GPO e clique em não **excluir**.</span><span class="sxs-lookup"><span data-stu-id="e96e1-121">To do so, right-click the version in the history of the GPO and click **Do Not Delete**.</span></span>

### <span data-ttu-id="e96e1-122">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="e96e1-122">Additional references</span></span>

-   [<span data-ttu-id="e96e1-123">Gerenciamento do arquivo morto</span><span class="sxs-lookup"><span data-stu-id="e96e1-123">Managing the Archive</span></span>](managing-the-archive.md)

 

 





