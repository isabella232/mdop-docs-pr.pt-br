---
title: Pesquisar e filtrar a lista de GPOs
description: Pesquisar e filtrar a lista de GPOs
author: dansimp
ms.assetid: 1bc58a38-033c-4aed-9eb4-c239827f5501
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5646a51a37a4ca9195fb9ef858e8c5920ca7738a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797690"
---
# <span data-ttu-id="7ff7e-103">Pesquisar e filtrar a lista de GPOs</span><span class="sxs-lookup"><span data-stu-id="7ff7e-103">Search and Filter the List of GPOs</span></span>


<span data-ttu-id="7ff7e-104">No gerenciamento avançado de política de grupo (AGPM), você pode pesquisar a lista de objetos de política de grupo (GPOs) e seus atributos para filtrar a lista de GPOs exibida.</span><span class="sxs-lookup"><span data-stu-id="7ff7e-104">In Advanced Group Policy Management (AGPM), you can search the list of Group Policy Objects (GPOs) and their attributes to filter the list of GPOs displayed.</span></span> <span data-ttu-id="7ff7e-105">Por exemplo, você pode pesquisar GPOs com um nome, estado ou comentário específico.</span><span class="sxs-lookup"><span data-stu-id="7ff7e-105">For example, you can search for GPOs with a particular name, state, or comment.</span></span> <span data-ttu-id="7ff7e-106">Você também pode pesquisar os GPOs que foram alterados pela última vez por um determinado administrador de política de grupo ou em uma data específica.</span><span class="sxs-lookup"><span data-stu-id="7ff7e-106">You can also search for GPOs that were last changed by a particular Group Policy administrator or on a particular date.</span></span>

## <span data-ttu-id="7ff7e-107">Executar uma pesquisa complexa</span><span class="sxs-lookup"><span data-stu-id="7ff7e-107">Performing a complex search</span></span>


<span data-ttu-id="7ff7e-108">Você pode realizar uma pesquisa complexa usando o atributo Format *GPO 1: Pesquisar Cadeia de caracteres 1 do atributo GPO 2: Pesquisar Cadeia de caracteres 2... cadeias de caracteres de pesquisa de todas as colunas*.</span><span class="sxs-lookup"><span data-stu-id="7ff7e-108">You can perform a complex search by using the format *GPO attribute 1: search string 1 GPO attribute 2: search string 2…all-column search strings*.</span></span> <span data-ttu-id="7ff7e-109">A pesquisa não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7ff7e-109">The search is not case-sensitive.</span></span>

-   <span data-ttu-id="7ff7e-110">**Atributo GPO:** Qualquer título de coluna na lista de GPOs em AGPM diferente da **versão do computador** ou da **versão do usuário**.</span><span class="sxs-lookup"><span data-stu-id="7ff7e-110">**GPO attribute:** Any column heading in the list of GPOs in AGPM other than **Computer Version** or **User Version**.</span></span> <span data-ttu-id="7ff7e-111">Os atributos de GPO incluem o nome do GPO, o estado, o usuário que alterou mais recentemente o GPO, a data e a hora em que o GPO foi alterado mais recentemente, comentário, status do GPO e filtro WMI aplicado ao GPO.</span><span class="sxs-lookup"><span data-stu-id="7ff7e-111">GPO attributes include the GPO name, state, user who most recently changed the GPO, date and time when the GPO was most recently changed, comment, GPO status, and WMI filter applied to the GPO.</span></span>

-   <span data-ttu-id="7ff7e-112">**Cadeia de pesquisa:** Texto a ser pesquisado na coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="7ff7e-112">**Search string:** Text for which to search in the specified column.</span></span> <span data-ttu-id="7ff7e-113">Se uma cadeia de caracteres incluir espaços, você deve colocar a cadeia de caracteres entre aspas.</span><span class="sxs-lookup"><span data-stu-id="7ff7e-113">If a string includes spaces, you must enclose the string with quotation marks.</span></span>

-   <span data-ttu-id="7ff7e-114">**Cadeias de caracteres de pesquisa de todas as colunas:** Texto no qual Pesquisar em todas as colunas da lista de GPOs em AGPM diferente da **versão do computador** e da **versão do usuário**.</span><span class="sxs-lookup"><span data-stu-id="7ff7e-114">**All-column search strings:** Text for which to search in all columns in the list of GPOs in AGPM other than **Computer Version** and **User Version**.</span></span> <span data-ttu-id="7ff7e-115">Você pode incluir várias cadeias de caracteres separadas por espaços.</span><span class="sxs-lookup"><span data-stu-id="7ff7e-115">You can include multiple strings separated by spaces.</span></span> <span data-ttu-id="7ff7e-116">Se uma cadeia de caracteres incluir espaços, você deve colocar a cadeia de caracteres entre aspas.</span><span class="sxs-lookup"><span data-stu-id="7ff7e-116">If a string includes spaces, you must enclose the string with quotation marks.</span></span>

<span data-ttu-id="7ff7e-117">Cada par de atributos de objeto de objeto e de cadeia de caracteres de pesquisa e cada cadeia de caracteres de pesquisa de todas as colunas são combinados usando uma operação e lógica.</span><span class="sxs-lookup"><span data-stu-id="7ff7e-117">Each GPO attribute and search string pair and each all-column search string are combined by using a logical AND operation.</span></span> <span data-ttu-id="7ff7e-118">O resultado é uma lista de todos os GPOs para os quais cada atributo especificado inclui a cadeia de caracteres de pesquisa especificada e para a qual todas as cadeias de caracteres de pesquisa de todas as colunas aparecem em pelo menos uma coluna.</span><span class="sxs-lookup"><span data-stu-id="7ff7e-118">The result is a list of all GPOs for which each specified attribute includes the specified search string and for which any all-column search strings appear in at least one column.</span></span> <span data-ttu-id="7ff7e-119">A pesquisa retorna quaisquer correspondências parciais para cadeias de caracteres para que você possa inserir parte de um nome de GPO ou nome de usuário e exibir uma lista de todos os GPOs que incluam esse texto no nome.</span><span class="sxs-lookup"><span data-stu-id="7ff7e-119">The search returns any partial matches for strings so that you can enter part of a GPO name or user name and view a list of all GPOs that include that text in their name.</span></span>

<span data-ttu-id="7ff7e-120">Veja a seguir exemplos de pesquisas:</span><span class="sxs-lookup"><span data-stu-id="7ff7e-120">The following are examples of searches:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7ff7e-121">Descrição do resultado da pesquisa</span><span class="sxs-lookup"><span data-stu-id="7ff7e-121">Description of search result</span></span></th>
<th align="left"><span data-ttu-id="7ff7e-122">Consulta de pesquisa</span><span class="sxs-lookup"><span data-stu-id="7ff7e-122">Search query</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ff7e-123">Todos os GPOs com nomes que incluem a <strong> segurança de texto </strong> e a <strong> América do Norte </strong> .</span><span class="sxs-lookup"><span data-stu-id="7ff7e-123">All GPOs with names that include the text <strong>security</strong> and <strong>North America</strong>.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="7ff7e-124">Nome: </strong><strong> nome de segurança </strong><strong> : </strong> &quot; <strong> América do Norte</strong>&quot;</span><span class="sxs-lookup"><span data-stu-id="7ff7e-124">name:</strong><strong>security</strong><strong>name:</strong>&quot;<strong>North America</strong>&quot;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ff7e-125">Todos os GPOs com check-out.</span><span class="sxs-lookup"><span data-stu-id="7ff7e-125">All checked out GPOs.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="7ff7e-126">Estado: </strong> &quot; <strong> com check-out</strong>&quot;</span><span class="sxs-lookup"><span data-stu-id="7ff7e-126">state:</strong>&quot;<strong>checked out</strong>&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ff7e-127">Todos os GPOs alterados mais recentemente pelo usuário chamado <strong> administrador </strong> e alterados recentemente no mês anterior.</span><span class="sxs-lookup"><span data-stu-id="7ff7e-127">All GPOs most recently changed by the user named <strong>Administrator</strong> and most recently changed within the previous month.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="7ff7e-128">alterado por: </strong><strong> data de alteração do administrador </strong><strong> : </strong><strong> lastmonth</span><span class="sxs-lookup"><span data-stu-id="7ff7e-128">changed by:</strong><strong>Administrator</strong><strong>change date:</strong><strong>lastmonth</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ff7e-129">Todos os GPOs nos quais o <strong> Firewall do Word </strong> está incluído no comentário mais recente e no qual a palavra <strong> segurança é </strong> exibida em qualquer coluna.</span><span class="sxs-lookup"><span data-stu-id="7ff7e-129">All GPOs in which the word <strong>firewall</strong> is included in the most recent comment and in which the word <strong>security</strong> appears in any column.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="7ff7e-130">Comentário: </strong><strong> segurança do firewall </strong><strong></span><span class="sxs-lookup"><span data-stu-id="7ff7e-130">comment:</strong><strong>firewall</strong><strong>security</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ff7e-131">Todos os GPOs que têm um status de <strong> todas as configurações desabilitadas </strong> .</span><span class="sxs-lookup"><span data-stu-id="7ff7e-131">All GPOs that have a status of <strong>All Settings Disabled</strong>.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="7ff7e-132">status do GPO: </strong><strong> todos</span><span class="sxs-lookup"><span data-stu-id="7ff7e-132">gpo status:</strong><strong>all</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7ff7e-133">Todos os GPOs que têm um filtro WMI chamado <strong> meu filtro WMI </strong> foram aplicados e que têm um status de <strong> configuração do usuário desabilitado </strong> .</span><span class="sxs-lookup"><span data-stu-id="7ff7e-133">All GPOs that have a WMI filter named <strong>My WMI Filter</strong> applied and that have a status of <strong>User Configuration Settings Disabled</strong>.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="7ff7e-134">filtro WMI: </strong> &quot; <strong> status do GPO do meu filtro WMI </strong> &quot; <strong> : </strong><strong> usuário</span><span class="sxs-lookup"><span data-stu-id="7ff7e-134">wmi filter:</strong>&quot;<strong>My WMI Filter</strong>&quot;<strong>gpo status:</strong><strong>user</span></span></strong></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="7ff7e-135">Especificando datas</span><span class="sxs-lookup"><span data-stu-id="7ff7e-135">Specifying dates</span></span>


<span data-ttu-id="7ff7e-136">Você pode pesquisar os GPOs alterados em uma data específica, em um horário específico ou durante um período de tempo usando os mesmos termos especiais disponíveis quando você pesquisa no Windows.</span><span class="sxs-lookup"><span data-stu-id="7ff7e-136">You can search for GPOs changed on a specific date, at a specific time, or during a span of time by using the same special terms available when you search in Windows.</span></span> <span data-ttu-id="7ff7e-137">Ao inserir uma data ou hora específica, você deve usar o formato usado na coluna **alterar Data** .</span><span class="sxs-lookup"><span data-stu-id="7ff7e-137">If entering a specific date or time, you must use the format that is used in the **Change Date** column.</span></span> <span data-ttu-id="7ff7e-138">Veja a seguir exemplos de pesquisas da coluna **data de alteração** :</span><span class="sxs-lookup"><span data-stu-id="7ff7e-138">The following are examples of searches of the **Change Date** column:</span></span>

-   <span data-ttu-id="7ff7e-139">**alterar Data:\*\*\*\*10/10/2009**</span><span class="sxs-lookup"><span data-stu-id="7ff7e-139">**change date:\*\*\*\*10/10/2009**</span></span>

-   <span data-ttu-id="7ff7e-140">**alterar Data:\*\*\*\*10/10/2009 9:00:00 am**</span><span class="sxs-lookup"><span data-stu-id="7ff7e-140">**change date:\*\*\*\*10/10/2009 9:00:00 AM**</span></span>

-   <span data-ttu-id="7ff7e-141">**alterar Data:\*\*\*\*thisweek**</span><span class="sxs-lookup"><span data-stu-id="7ff7e-141">**change date:\*\*\*\*thisweek**</span></span>

<span data-ttu-id="7ff7e-142">Você pode usar os seguintes termos especiais, que não diferenciam maiúsculas de minúsculas, quando você pesquisa a coluna **alterar Data** :</span><span class="sxs-lookup"><span data-stu-id="7ff7e-142">You can use the following special terms, which are not case-sensitive, when you search the **Change Date** column:</span></span>

-   **<span data-ttu-id="7ff7e-143">Hoje</span><span class="sxs-lookup"><span data-stu-id="7ff7e-143">Today</span></span>**

-   **<span data-ttu-id="7ff7e-144">Ontem</span><span class="sxs-lookup"><span data-stu-id="7ff7e-144">Yesterday</span></span>**

-   **<span data-ttu-id="7ff7e-145">ThisWeek</span><span class="sxs-lookup"><span data-stu-id="7ff7e-145">ThisWeek</span></span>**

-   **<span data-ttu-id="7ff7e-146">LastWeek</span><span class="sxs-lookup"><span data-stu-id="7ff7e-146">LastWeek</span></span>**

-   **<span data-ttu-id="7ff7e-147">ThisMonth</span><span class="sxs-lookup"><span data-stu-id="7ff7e-147">ThisMonth</span></span>**

-   **<span data-ttu-id="7ff7e-148">LastMonth</span><span class="sxs-lookup"><span data-stu-id="7ff7e-148">LastMonth</span></span>**

-   **<span data-ttu-id="7ff7e-149">TwoMonths</span><span class="sxs-lookup"><span data-stu-id="7ff7e-149">TwoMonths</span></span>**

-   **<span data-ttu-id="7ff7e-150">ThreeMonths</span><span class="sxs-lookup"><span data-stu-id="7ff7e-150">ThreeMonths</span></span>**

-   **<span data-ttu-id="7ff7e-151">ThisYear</span><span class="sxs-lookup"><span data-stu-id="7ff7e-151">ThisYear</span></span>**

-   **<span data-ttu-id="7ff7e-152">LastYear</span><span class="sxs-lookup"><span data-stu-id="7ff7e-152">LastYear</span></span>**

### <span data-ttu-id="7ff7e-153">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="7ff7e-153">Additional considerations</span></span>

-   <span data-ttu-id="7ff7e-154">Por padrão, você deve ser um revisor, um editor, um Aprovador ou um administrador do AGPM (controle total) para executar esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="7ff7e-154">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="7ff7e-155">Especificamente, você deve ter permissão de **listar conteúdo** para o domínio.</span><span class="sxs-lookup"><span data-stu-id="7ff7e-155">Specifically, you must have **List Contents** permission for the domain.</span></span>

-   <span data-ttu-id="7ff7e-156">Para obter mais informações sobre atributos de GPO, consulte [recursos da guia conteúdo](contents-tab-features-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="7ff7e-156">For more information about GPO attributes, see [Contents Tab Features](contents-tab-features-agpm40.md).</span></span>

### <span data-ttu-id="7ff7e-157">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="7ff7e-157">Additional references</span></span>

-   [<span data-ttu-id="7ff7e-158">Gerenciamento Avançado de Política de Grupo 4.0</span><span class="sxs-lookup"><span data-stu-id="7ff7e-158">Advanced Group Policy Management 4.0</span></span>](advanced-group-policy-management-40.md)

 

 





