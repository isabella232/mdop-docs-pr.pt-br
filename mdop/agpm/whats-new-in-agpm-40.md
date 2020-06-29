---
title: Novidades no AGPM 4.0
description: Novidades no AGPM 4.0
author: dansimp
ms.assetid: 31775f7f-a59c-4e64-a875-0adc9f5bc835
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 82b4445a7d22fb7c1ef4f42d896f11908a22f2f5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797658"
---
# <span data-ttu-id="3ce51-103">Novidades no AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="3ce51-103">What's New in AGPM 4.0</span></span>


<span data-ttu-id="3ce51-104">O gerenciamento avançado de política de grupo (AGPM) 4.0 da Microsoft oferece novos recursos que permitem pesquisar objetos de política de grupo (GPOs), filtrar a lista de GPOs exibidos, exportar e importar um GPO para uma floresta diferente e instalar o AGPM em computadores que executam o Windows e o Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="3ce51-104">Microsoft Advanced Group Policy Management (AGPM)4.0 includes new features that let you search for Group Policy Objects (GPOs), filter the list of GPOs displayed, export and import a GPO to a different forest, and install AGPM on computers running Windows7 and Windows Server2008R2.</span></span>

## <span data-ttu-id="3ce51-105">Pesquisar e filtrar GPOs</span><span class="sxs-lookup"><span data-stu-id="3ce51-105">Search and filter GPOs</span></span>


<span data-ttu-id="3ce51-106">No AGPM 4,0, você pode pesquisar a lista de GPOs em busca de atributos específicos para filtrar a lista de GPOs exibida.</span><span class="sxs-lookup"><span data-stu-id="3ce51-106">In AGPM 4.0, you can search the list of GPOs for specific attributes to filter the list of GPOs displayed.</span></span> <span data-ttu-id="3ce51-107">Por exemplo, você pode pesquisar GPOs com um nome, estado ou comentário específico.</span><span class="sxs-lookup"><span data-stu-id="3ce51-107">For example, you can search for GPOs with a particular name, state, or comment.</span></span> <span data-ttu-id="3ce51-108">Você também pode pesquisar os GPOs que foram alterados pela última vez por um determinado administrador de política de grupo ou em uma data específica.</span><span class="sxs-lookup"><span data-stu-id="3ce51-108">You can also search for GPOs that were last changed by a particular Group Policy administrator or on a particular date.</span></span>

<span data-ttu-id="3ce51-109">Você pode criar uma cadeia de pesquisa complexa usando o *atributo Format GPO 1: Pesquisar texto 1 atributo do GPO 2: Pesquisar texto 2..*., onde um atributo GPO é qualquer título de coluna na lista de GPOs do AGPM.</span><span class="sxs-lookup"><span data-stu-id="3ce51-109">You can create a complex search string by using the format *GPO attribute 1: search text 1 GPO attribute 2: search text 2…*, where a GPO attribute is any column heading in the list of GPOs in AGPM.</span></span> <span data-ttu-id="3ce51-110">Por exemplo, para pesquisar todos os GPOs com nomes, incluindo o texto "MyGPO" que está com check-in e alterados pela última vez pela Editor03 do usuário, você deve digitar o seguinte na caixa de pesquisa: **nome: MyGPO Estado:\*\*\*\*check-in\*\*\*\*alterado por: Editor03**.</span><span class="sxs-lookup"><span data-stu-id="3ce51-110">For example, to search for all GPOs with names including the text "MyGPO" that are checked in and were last changed by the user Editor03, you would type the following in the Search box: **name: MyGPO state:\*\*\*\*checked in\*\*\*\*changed by: Editor03**.</span></span> <span data-ttu-id="3ce51-111">A pesquisa retorna correspondências parciais para que você possa inserir parte de um nome de GPO ou nome de usuário e exibir uma lista de todos os GPOs que incluem esse texto no nome.</span><span class="sxs-lookup"><span data-stu-id="3ce51-111">The search returns partial matches so that you can enter part of a GPO name or user name and view a list of all GPOs that include that text in their name.</span></span>

<span data-ttu-id="3ce51-112">Além disso, você pode usar os mesmos termos especiais disponíveis ao pesquisar no Windows para pesquisar os GPOs alterados em uma data específica ou em um intervalo de datas.</span><span class="sxs-lookup"><span data-stu-id="3ce51-112">Additionally, you can use the same special terms available when you search in Windows to search for GPOs changed on a specific date or range of dates.</span></span> <span data-ttu-id="3ce51-113">Por exemplo, **alterar Data:\*\*\*\*lastmonth** ou **alterar Data:\*\*\*\*thisweek**.</span><span class="sxs-lookup"><span data-stu-id="3ce51-113">For example, **change date:\*\*\*\*lastmonth** or **change date:\*\*\*\*thisweek**.</span></span>

## <span data-ttu-id="3ce51-114">Exportar e importar GPOs para florestas diferentes</span><span class="sxs-lookup"><span data-stu-id="3ce51-114">Export and import GPOs to different forests</span></span>


<span data-ttu-id="3ce51-115">Usando o AGPM 4,0, você pode copiar um GPO controlado de um domínio em uma floresta para um domínio em uma segunda floresta.</span><span class="sxs-lookup"><span data-stu-id="3ce51-115">Using AGPM 4.0, you can copy a controlled GPO from a domain in one forest to a domain in a second forest.</span></span> <span data-ttu-id="3ce51-116">Por exemplo, você pode exportar um GPO de um domínio em uma floresta para um arquivo CAB usando o AGPM, copiar esse arquivo CAB para uma unidade USB, conectar a unidade USB a um computador em um domínio em uma segunda floresta e importar o GPO para o AGPM em um domínio na segunda floresta.</span><span class="sxs-lookup"><span data-stu-id="3ce51-116">For example, you can export a GPO from a domain in one forest to a CAB file by using AGPM, copy that CAB file to a USB drive, plug the USB drive into a computer in a domain in a second forest, and import the GPO into AGPM in a domain in the second forest.</span></span> <span data-ttu-id="3ce51-117">Você pode importar o GPO como um novo GPO controlado ou importá-lo para substituir as configurações de um GPO existente que está com check-out.</span><span class="sxs-lookup"><span data-stu-id="3ce51-117">You can either import the GPO as a new controlled GPO, or import it to replace the settings of an existing GPO that is checked out.</span></span>

## <span data-ttu-id="3ce51-118">Suporte para Windows Server 2008 R2 e Windows 7</span><span class="sxs-lookup"><span data-stu-id="3ce51-118">Support for Windows Server 2008 R2 and Windows 7</span></span>


<span data-ttu-id="3ce51-119">O AGPM 4,0 tem suporte para Windows Server2008R2 e Windows e ainda oferece suporte ao Windows Server2008 e WindowsVista® com Service Pack1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="3ce51-119">AGPM 4.0 supports Windows Server2008R2 and Windows7, yet still supports Windows Server2008 and WindowsVista® with Service Pack1 (SP1).</span></span> <span data-ttu-id="3ce51-120">No entanto, há limitações em um ambiente misto que inclui os sistemas operacionais mais recentes e mais antigos, conforme indicado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3ce51-120">However, there are limitations in a mixed environment that includes both the newer and older operating systems, as indicated in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3ce51-121">Sistema operacional no qual o servidor do AGPM 4,0 é executado</span><span class="sxs-lookup"><span data-stu-id="3ce51-121">Operating system on which AGPM Server 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="3ce51-122">Sistema operacional no qual o cliente do AGPM 4,0 é executado</span><span class="sxs-lookup"><span data-stu-id="3ce51-122">Operating system on which AGPM Client 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="3ce51-123">Status do suporte do AGPM 4,0</span><span class="sxs-lookup"><span data-stu-id="3ce51-123">Status of AGPM 4.0 support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ce51-124">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="3ce51-124">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ce51-125">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="3ce51-125">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ce51-126">Com suporte</span><span class="sxs-lookup"><span data-stu-id="3ce51-126">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ce51-127">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="3ce51-127">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ce51-128">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="3ce51-128">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ce51-129">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server2008R2 ou no Windows7</span><span class="sxs-lookup"><span data-stu-id="3ce51-129">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3ce51-130">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="3ce51-130">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ce51-131">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="3ce51-131">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ce51-132">Sem Suporte</span><span class="sxs-lookup"><span data-stu-id="3ce51-132">Unsupported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3ce51-133">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="3ce51-133">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ce51-134">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="3ce51-134">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="3ce51-135">Com suporte, mas não pode reportar ou editar configurações de política ou itens de preferência que existem somente no Windows Server2008R2 ou no Windows7</span><span class="sxs-lookup"><span data-stu-id="3ce51-135">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 





