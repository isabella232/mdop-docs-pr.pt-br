---
title: Página de opções avançadas do assistente de sequenciamento do Application Virtualization
description: Página de opções avançadas do assistente de sequenciamento do Application Virtualization
author: dansimp
ms.assetid: 2c4c5d95-d55e-463d-a851-8486f6a724f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 716fa27852f1cadfebec31a267ce1b9b581b8ff7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797557"
---
# <span data-ttu-id="0f7b2-103">Página de opções avançadas do assistente de sequenciamento do Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="0f7b2-103">Application Virtualization Sequencing Wizard Advanced Options Page</span></span>


<span data-ttu-id="0f7b2-104">Use a página de **Opções avançadas** do assistente de sequenciamento do Application Virtualization (App-V) para especificar opções avançadas para o aplicativo a ser instalado.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-104">Use the **Advanced Options** page of the Application Virtualization (App-V) Sequencing Wizard to specify advanced options for the application to be installed.</span></span> <span data-ttu-id="0f7b2-105">A página contém os elementos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-105">The page contains the elements described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0f7b2-106">Nome</span><span class="sxs-lookup"><span data-stu-id="0f7b2-106">Name</span></span></th>
<th align="left"><span data-ttu-id="0f7b2-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f7b2-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0f7b2-108">Tamanho do bloco</span><span class="sxs-lookup"><span data-stu-id="0f7b2-108">Block Size</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0f7b2-109">Use para especificar o tamanho dos blocos dos quais o arquivo SFT será dividido quando transmitido em uma rede.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-109">Use to specify the size of blocks that the SFT file will be divided into when streamed across a network.</span></span> <span data-ttu-id="0f7b2-110">Todos os blocos são iguais ao tamanho especificado; no entanto, o último bloco pode ser menor do que o especificado.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-110">All blocks equal the specified size; however, the last block might be smaller than specified.</span></span> <span data-ttu-id="0f7b2-111">Selecione um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="0f7b2-111">Select one of the following values:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="0f7b2-112">4 KB</span><span class="sxs-lookup"><span data-stu-id="0f7b2-112">4 KB</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="0f7b2-113">16 KB</span><span class="sxs-lookup"><span data-stu-id="0f7b2-113">16 KB</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="0f7b2-114">32 KB</span><span class="sxs-lookup"><span data-stu-id="0f7b2-114">32 KB</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="0f7b2-115">64 KB</span><span class="sxs-lookup"><span data-stu-id="0f7b2-115">64 KB</span></span></strong></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="0f7b2-116">Observação</span><span class="sxs-lookup"><span data-stu-id="0f7b2-116">Note</span></span></strong><br/><p><span data-ttu-id="0f7b2-117">Quando você selecionar um tamanho de bloco, considere o tamanho do arquivo SFT e a largura de banda da rede.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-117">When you select a block size, consider the size of the SFT file and your network bandwidth.</span></span> <span data-ttu-id="0f7b2-118">Um arquivo com um tamanho de bloco menor leva mais tempo para transmitir pela rede, mas tem menos largura de banda e consome menos largura de banda.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-118">A file with a smaller block size takes longer to stream over the network but is less bandwidth-intensive.</span></span> <span data-ttu-id="0f7b2-119">Arquivos com tamanhos de blocos maiores podem ser usados com mais rapidez, mas usam mais largura de banda de rede.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-119">Files with larger block sizes might stream faster, but they use more network bandwidth.</span></span> <span data-ttu-id="0f7b2-120">Por meio da experimentação, você pode descobrir o tamanho de bloco ideal para aplicativos de streaming na sua rede.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-120">Through experimentation, you can discover the optimum block size for streaming applications on your network.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0f7b2-121">Habilitar o Microsoft Update durante o monitoramento</span><span class="sxs-lookup"><span data-stu-id="0f7b2-121">Enable Microsoft Update During Monitoring</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0f7b2-122">Permite a instalação de atualizações da Microsoft durante o assistente de sequenciamento&#39;fase de monitoramento de s.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-122">Enables installation of Microsoft Updates during the Sequencing Wizard&#39;s monitoring phase.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0f7b2-123">Alterar a base das DLLs</span><span class="sxs-lookup"><span data-stu-id="0f7b2-123">Rebase DLLs</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0f7b2-124">Permite o remapeamento de bibliotecas de vínculo dinâmico compatíveis para um espaço contíguo na RAM, economizando memória e melhorando o desempenho.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-124">Enables remapping of supported dynamic-link libraries to a contiguous space in RAM, saving memory and improving performance.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0f7b2-125">Voltar</span><span class="sxs-lookup"><span data-stu-id="0f7b2-125">Back</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0f7b2-126">Acessa o assistente de sequenciamento&#39;a página anterior.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-126">Accesses the Sequencing Wizard&#39;s previous page.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0f7b2-127">Próxima</span><span class="sxs-lookup"><span data-stu-id="0f7b2-127">Next</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0f7b2-128">Acessa o assistente de sequenciamento&#39;s próxima página.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-128">Accesses the Sequencing Wizard&#39;s next page.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0f7b2-129">Cancelar</span><span class="sxs-lookup"><span data-stu-id="0f7b2-129">Cancel</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0f7b2-130">Finaliza a operação do assistente de sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-130">Terminates operation of the Sequencing Wizard.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="0f7b2-131">\ [Valor do token do modelo \]</span><span class="sxs-lookup"><span data-stu-id="0f7b2-131">\[Template Token Value\]</span></span>

<span data-ttu-id="0f7b2-132">Use a página de **Opções avançadas** do assistente de sequenciamento do App-V para especificar opções avançadas para o aplicativo que você está sequenciando.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-132">Use the **Advanced Options** page of the App-V Sequencing Wizard to specify advanced options for the application you are sequencing.</span></span> <span data-ttu-id="0f7b2-133">Esta página contém os elementos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-133">This page contains the elements described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0f7b2-134">Nome</span><span class="sxs-lookup"><span data-stu-id="0f7b2-134">Name</span></span></th>
<th align="left"><span data-ttu-id="0f7b2-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f7b2-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0f7b2-136">Permitir que o Microsoft Update seja executado durante o monitoramento</span><span class="sxs-lookup"><span data-stu-id="0f7b2-136">Allow Microsoft Update to run during monitoring</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0f7b2-137">Especifica se as atualizações de software serão aplicadas ao aplicativo durante a fase de monitoramento do sequenciamento do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-137">Specifies whether software updates will be applied to the application during the monitoring phase of application sequencing.</span></span> <span data-ttu-id="0f7b2-138">Esta opção será útil se as atualizações forem necessárias para concluir a instalação do aplicativo com êxito.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-138">This option is helpful if updates are required to successfully complete the application installation.</span></span> <span data-ttu-id="0f7b2-139">Essa opção não é selecionada por padrão.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-139">This option is not selected by default.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0f7b2-140">Alterar a base das DLLs</span><span class="sxs-lookup"><span data-stu-id="0f7b2-140">Rebase Dlls</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0f7b2-141">Permite o remapeamento de bibliotecas de vínculo dinâmico compatíveis para um espaço contíguo na RAM.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-141">Enables remapping of supported dynamic-link libraries to a contiguous space in RAM.</span></span> <span data-ttu-id="0f7b2-142">Selecionar essa opção pode ajudar a gerenciar a memória e melhorar o desempenho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-142">Selecting this option can help manage memory and improve application performance.</span></span> <span data-ttu-id="0f7b2-143">Essa opção não é selecionada por padrão.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-143">This option is not selected by default.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0f7b2-144">Voltar</span><span class="sxs-lookup"><span data-stu-id="0f7b2-144">Back</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0f7b2-145">Vai para a página anterior do assistente.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-145">Goes to the previous page of the wizard.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="0f7b2-146">Próxima</span><span class="sxs-lookup"><span data-stu-id="0f7b2-146">Next</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0f7b2-147">Vai para a próxima página do assistente.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-147">Goes to the next page of the wizard.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="0f7b2-148">Cancelar</span><span class="sxs-lookup"><span data-stu-id="0f7b2-148">Cancel</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="0f7b2-149">Descarta as configurações e sai do assistente.</span><span class="sxs-lookup"><span data-stu-id="0f7b2-149">Discards the settings and exits the wizard.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="0f7b2-150">\ [Valor do token do modelo \]</span><span class="sxs-lookup"><span data-stu-id="0f7b2-150">\[Template Token Value\]</span></span>

## <span data-ttu-id="0f7b2-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f7b2-151">Related topics</span></span>


[<span data-ttu-id="0f7b2-152">Assistente de Sequenciamento</span><span class="sxs-lookup"><span data-stu-id="0f7b2-152">Sequencing Wizard</span></span>](sequencing-wizard.md)









