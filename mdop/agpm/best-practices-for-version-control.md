---
title: Práticas recomendadas para o controle de versão
description: Práticas recomendadas para o controle de versão
author: dansimp
ms.assetid: 89067f6a-f7ea-4dad-999d-118284cf6c5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ed91408faeb8968175976382f9dd97d45becddb5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797478"
---
# <span data-ttu-id="f8189-103">Práticas recomendadas para o controle de versão</span><span class="sxs-lookup"><span data-stu-id="f8189-103">Best Practices for Version Control</span></span>


<span data-ttu-id="f8189-104">O gerenciamento avançado de política de grupo (AGPM) da Microsoft fornece controle de versão para objetos de política de grupo (GPOs) da mesma forma que o Microsoft Visual SourceSafe® fornece controle de versão para código-fonte.</span><span class="sxs-lookup"><span data-stu-id="f8189-104">Microsoft Advanced Group Policy Management (AGPM) provides version control for Group Policy Objects (GPOs) much like Microsoft Visual SourceSafe® provides version control for source code.</span></span> <span data-ttu-id="f8189-105">Os desenvolvedores podem usar o Visual SourceSafe para gerenciar várias versões de cada arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="f8189-105">Developers can use Visual SourceSafe to manage multiple versions of each source file.</span></span> <span data-ttu-id="f8189-106">Os administradores de política de grupo podem usar o AGPM para fazer o mesmo para GPOs.</span><span class="sxs-lookup"><span data-stu-id="f8189-106">Group Policy administrators can use AGPM to do the same for GPOs.</span></span> <span data-ttu-id="f8189-107">Quando você usa o AGPM, os administradores de política de grupo devem estar cientes das práticas recomendadas que se aplicam a qualquer sistema de controle de versão:</span><span class="sxs-lookup"><span data-stu-id="f8189-107">When you use AGPM, Group Policy administrators should be aware of best practices that apply to any version control system:</span></span>

-   <span data-ttu-id="f8189-108">**Data e hora:** O AGPM carimba cada versão de um GPO com a data e a hora.</span><span class="sxs-lookup"><span data-stu-id="f8189-108">**Date and time:** AGPM stamps each version of a GPO with the date and time.</span></span> <span data-ttu-id="f8189-109">Para garantir que o histórico seja preciso, especialmente quando você edita GPOs em mais de um computador, verifique se cada computador sincroniza seu relógio com uma fonte de tempo autoritativa.</span><span class="sxs-lookup"><span data-stu-id="f8189-109">To ensure that history is accurate, especially when you edit GPOs on more than one computer, make sure that each computer synchronizes its clock with one authoritative time source.</span></span>

-   <span data-ttu-id="f8189-110">**Fazer check-in de GPOs quando terminar de editá-los:** É comum que os editores confiram os GPOs e esqueçam de verificá-los de volta ao arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="f8189-110">**Check in GPOs when you are finished editing them:** It is common for Editors to check out GPOs and forget to check them back into the archive.</span></span> <span data-ttu-id="f8189-111">No entanto, isso pode impedir que outros administradores de política de grupo alterem o GPO.</span><span class="sxs-lookup"><span data-stu-id="f8189-111">However, this can prevent other Group Policy administrators from changing the GPO.</span></span> <span data-ttu-id="f8189-112">Sempre verifique os GPOs novamente no AGPM imediatamente quando terminar de editar.</span><span class="sxs-lookup"><span data-stu-id="f8189-112">Always check GPOs back in to AGPM immediately when you are finished editing.</span></span>

-   <span data-ttu-id="f8189-113">**Salve as mudanças com frequência:** Ao editar um GPO, salve as alterações com frequência.</span><span class="sxs-lookup"><span data-stu-id="f8189-113">**Save changes frequently:** When you edit a GPO, save changes frequently.</span></span> <span data-ttu-id="f8189-114">A maioria dos editores verificam um GPO, fazem muitas alterações e, em seguida, verificamos o GPO no arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="f8189-114">Most Editors check out a GPO, make many changes, and then check the GPO into the archive.</span></span> <span data-ttu-id="f8189-115">Em vez disso, verifique o GPO em arquivar regularmente e, em seguida, dê uma olhada nele novamente.</span><span class="sxs-lookup"><span data-stu-id="f8189-115">Instead, check the GPO into the archive regularly, and then check it out again.</span></span> <span data-ttu-id="f8189-116">O detalhe pode ser tão pequeno quanto fazer check-in do GPO após alterar todas as configurações (não recomendado) ou fazer check-in do GPO depois de fazer grupos de alterações relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f8189-116">The detail can be as small as checking in the GPO after you change every setting (not recommended) or checking in the GPO after you make groups of related changes.</span></span> <span data-ttu-id="f8189-117">O resultado é um histórico melhor documentado para cada GPO que pode ajudar na solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="f8189-117">The result is a better-documented history for each GPO that can help when troubleshooting issues.</span></span>

-   <span data-ttu-id="f8189-118">**Implante GPOs com frequência:** Não deixe os GPOs novos e editados que ainda não foram implantados acumulados em números grandes no arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="f8189-118">**Deploy GPOs frequently:** Do not let new and edited GPOs that have not yet been deployed accumulate in large numbers in the archive.</span></span> <span data-ttu-id="f8189-119">Em vez disso, implante os GPOs novos e editados o mais rápido possível para que tenham um efeito mínimo sobre o ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="f8189-119">Instead, deploy new and edited GPOs as soon as possible so that they have a minimum effect on the production environment.</span></span> <span data-ttu-id="f8189-120">Implantar vários GPOs novos e editados ao mesmo tempo pode prejudicar o ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="f8189-120">Deploying many new and edited GPOs at one time can jeopardize the production environment.</span></span>

-   <span data-ttu-id="f8189-121">**Documentar a finalidade das alterações ao fazer check-in de GPOs:** Qualquer revisor pode comparar versões de um GPO para ver alterações específicas entre os dois.</span><span class="sxs-lookup"><span data-stu-id="f8189-121">**Document the purpose of changes when you check in GPOs:** Any Reviewer can compare versions of a GPO to see specific changes between the two.</span></span> <span data-ttu-id="f8189-122">A documentação dessas alterações específicas não agrega valor.</span><span class="sxs-lookup"><span data-stu-id="f8189-122">Documenting those specific changes adds no value.</span></span> <span data-ttu-id="f8189-123">Em vez disso, documente a intenção e a finalidade de uma alteração em vez de documentar o que os revisores podem ver exibindo relatórios de diferença.</span><span class="sxs-lookup"><span data-stu-id="f8189-123">Instead, document the intent and purpose of a change instead of documenting what Reviewers can see by viewing difference reports.</span></span> <span data-ttu-id="f8189-124">Comentários sobre a versão devem adicionar valor ao relatório de comparação e ajudar um revisor a entender por que o editor alterou o GPO.</span><span class="sxs-lookup"><span data-stu-id="f8189-124">Version comments should add value to the comparison report and help a Reviewer understand why the Editor changed the GPO.</span></span>

-   <span data-ttu-id="f8189-125">**Testar GPOs em um laboratório antes de implantá** -los: Implantar GPOs no ambiente de produção sem primeiro testá-los é arriscado.</span><span class="sxs-lookup"><span data-stu-id="f8189-125">**Test GPOs in a lab before you deploy:** Deploying GPOs to the production environment without first testing them is risky.</span></span> <span data-ttu-id="f8189-126">Em vez disso, teste os GPOs em um ambiente de laboratório vinculando-os a uma unidade organizacional que contém computadores de teste e usuários e verificando se eles funcionam corretamente.</span><span class="sxs-lookup"><span data-stu-id="f8189-126">Instead, test GPOs in a lab environment by linking them to an organizational unit that contains test computers and users, and then verifying that they function correctly.</span></span> <span data-ttu-id="f8189-127">Depois de verificar cada GPO no laboratório, implante o GPO no ambiente de produção.</span><span class="sxs-lookup"><span data-stu-id="f8189-127">After verifying each GPO in the lab, deploy the GPO to the production environment.</span></span>

### <span data-ttu-id="f8189-128">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="f8189-128">Additional references</span></span>

-   [<span data-ttu-id="f8189-129">Guia operacional do Gerenciamento Avançado de Política de Grupo 3.0 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="f8189-129">Operations Guide for Microsoft Advanced Group Policy Management 3.0</span></span>](operations-guide-for-microsoft-advanced-group-policy-management-30-agpm30ops.md)

 

 





