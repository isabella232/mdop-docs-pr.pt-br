---
title: Como escolher qual versão do AGPM a ser instalada
description: Como escolher qual versão do AGPM a ser instalada
author: dansimp
ms.assetid: 31357d2a-bc23-4e15-93f4-0beda8ab7a7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/05/2017
ms.openlocfilehash: f8a69fb323d9f47c5b906ac3abc6ec59376ee6f7
ms.sourcegitcommit: 0a7dee11289780336d9c24ebbf27c5c1ffee441c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/04/2020
ms.locfileid: "10905598"
---
# <span data-ttu-id="0023a-103">Como escolher qual versão do AGPM a ser instalada</span><span class="sxs-lookup"><span data-stu-id="0023a-103">Choosing Which Version of AGPM to Install</span></span>


<span data-ttu-id="0023a-104">Cada lançamento do gerenciamento de política de grupo (AGPM) do MicrosoftAdvanced oferece suporte a versões específicas do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="0023a-104">Each release of MicrosoftAdvanced Group Policy Management (AGPM) supports specific versions of the Windows operating system.</span></span> <span data-ttu-id="0023a-105">É altamente recomendável que você execute o cliente do AGPM e o servidor do AGPM na mesma linha de sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="0023a-105">We strongly recommend that you run the AGPM Client and AGPM Server on the same line of operating systems.</span></span> <span data-ttu-id="0023a-106">Por exemplo, Windows 10 com Windows Server 2016, Windows 8.1 com Windows Server2012 R2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="0023a-106">For example, Windows 10 with Windows Server 2016, Windows8.1 with Windows Server2012 R2, and so on.</span></span>

<span data-ttu-id="0023a-107">Recomendamos que você instale o servidor do AGPM na versão mais recente do sistema operacional do domínio.</span><span class="sxs-lookup"><span data-stu-id="0023a-107">We recommend that you install the AGPM Server on the most recent version of the operating system in the domain.</span></span> <span data-ttu-id="0023a-108">O AGPM usa o GPMC (console de gerenciamento de política de grupo) para fazer backup e restaurar objetos de política de grupo (GPOs).</span><span class="sxs-lookup"><span data-stu-id="0023a-108">AGPM uses the Group Policy Management Console (GPMC) to back up and restore Group Policy Objects (GPOs).</span></span> <span data-ttu-id="0023a-109">Como as versões mais recentes do GPMC fornecem configurações de política adicionais que não estão disponíveis em versões anteriores, você pode gerenciar mais configurações de política usando a versão mais recente do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0023a-109">Because newer versions of the GPMC provide additional policy settings that are not available in earlier versions, you can manage more policy settings by using the most recent version of the operating system.</span></span>

<span data-ttu-id="0023a-110">Todas as versões do AGPM podem gerenciar apenas as configurações de política que foram introduzidas na mesma versão ou em uma versão anterior do sistema operacional em que o AGPM está em execução.</span><span class="sxs-lookup"><span data-stu-id="0023a-110">All versions of AGPM can manage only the policy settings that were introduced in the same version or an earlier version of the operating system on which AGPM is running.</span></span> <span data-ttu-id="0023a-111">Por exemplo, se você instalar o AGPM 4.0 SP2 no Windows Server 2012, poderá gerenciar as configurações de política que foram introduzidas no Windows Server 2012 ou anterior, mas não poderá gerenciar as configurações de política que foram introduzidas mais tarde, no Windows 8.1 ou no Windows Server2012 R2.</span><span class="sxs-lookup"><span data-stu-id="0023a-111">For example, if you install AGPM4.0 SP2 on Windows Server 2012, you can manage policy settings that were introduced in Windows Server 2012 or earlier, but you cannot manage policy settings that were introduced later, in Windows8.1 or Windows Server2012 R2.</span></span>

<span data-ttu-id="0023a-112">Se a versão do GPMC em seu servidor do AGPM for mais antiga do que a versão nos computadores que os administradores usam para gerenciar a política de grupo, o servidor do AGPM não poderá armazenar nenhuma configuração de política que não esteja disponível na versão anterior do GPMC.</span><span class="sxs-lookup"><span data-stu-id="0023a-112">If the version of the GPMC on your AGPM Server is older than the version on the computers that administrators use to manage Group Policy, the AGPM Server will be unable to store any policy settings that are not available in the older version of the GPMC.</span></span> <span data-ttu-id="0023a-113">Consulte a planilha de configurações de Política de Grupo incluídas no Windows na [Referência de configurações de Política de Grupo para Windows e Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span><span class="sxs-lookup"><span data-stu-id="0023a-113">For a spreadsheet of Group Policy settings included in Windows, see [Group Policy Settings Reference for Windows and Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span></span>

## <span data-ttu-id="0023a-114">AGPM 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="0023a-114">AGPM4.0 SP3</span></span>


<span data-ttu-id="0023a-115">Se você estiver usando computadores que executam o Windows 10 para gerenciar GPOs, deverá usar o AGPM 4,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="0023a-115">If you are using computers that are running Windows 10 to manage GPOs, you must use AGPM 4.0 SP3.</span></span> <span data-ttu-id="0023a-116">Não é possível instalar versões anteriores do AGPM em computadores que executam o sistema operacional Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0023a-116">You cannot install earlier versions of AGPM on computers that are running the Windows 10 operating system.</span></span>

<span data-ttu-id="0023a-117">A tabela 1 lista os sistemas operacionais nos quais você pode instalar o AGPM 4.0 SP3 e as configurações de política que você pode gerenciar usando o AGPM 4.0 SP3.</span><span class="sxs-lookup"><span data-stu-id="0023a-117">Table 1 lists the operating systems on which you can install AGPM4.0 SP3, and the policy settings that you can manage by using AGPM4.0 SP3.</span></span>

**<span data-ttu-id="0023a-118">Tabela 1: sistemas operacionais compatíveis com o AGPM 4,0 SP3 e configurações de política</span><span class="sxs-lookup"><span data-stu-id="0023a-118">Table 1: AGPM 4.0 SP3 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="0023a-119">Configurações com suporte para o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="0023a-119">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="0023a-120">Configurações com suporte para o cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="0023a-120">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="0023a-121">Suporte do AGPM</span><span class="sxs-lookup"><span data-stu-id="0023a-121">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0023a-122">Windows Server 2019 ou Windows 10</span><span class="sxs-lookup"><span data-stu-id="0023a-122">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-123">Windows Server 2019 ou Windows 10</span><span class="sxs-lookup"><span data-stu-id="0023a-123">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-124">Com suporte</span><span class="sxs-lookup"><span data-stu-id="0023a-124">Supported</span></span></p></td>
</tr>
 <tr class="even">
<td align="left"><p><span data-ttu-id="0023a-125">Windows Server 2019 ou Windows 10</span><span class="sxs-lookup"><span data-stu-id="0023a-125">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-126">Windows Server 2019 ou Windows 10</span><span class="sxs-lookup"><span data-stu-id="0023a-126">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-127">Com suporte</span><span class="sxs-lookup"><span data-stu-id="0023a-127">Supported</span></span></p></td>
</tr>
<tr class="edd">
<td align="left"><p><span data-ttu-id="0023a-128">Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="0023a-128">Windows Server2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-129">Windows 10</span><span class="sxs-lookup"><span data-stu-id="0023a-129">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-130">Compatível com as advertências descritas em <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)"> KB 4015786</span><span class="sxs-lookup"><span data-stu-id="0023a-130">Supported with the caveats outlined in <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)">KB 4015786</span></span></a>
</p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0023a-131">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0023a-131">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-132">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0023a-132">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-133">Com suporte</span><span class="sxs-lookup"><span data-stu-id="0023a-133">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0023a-134">Windows Server2012 R2, Windows Server 2012 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0023a-134">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-135">Windows Server 2012 ou Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="0023a-135">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-136">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0023a-136">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0023a-137">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="0023a-137">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-138">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="0023a-138">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-139">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0023a-139">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0023a-140">Windows Server 2012, Windows Server2008R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="0023a-140">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-141">Windows Server2008 ou WindowsVista com Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="0023a-141">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-142">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server2012 R2, no Windows Server 2012, no Windows Server2008R2, no Windows 8.1 ou no Windows7</span><span class="sxs-lookup"><span data-stu-id="0023a-142">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0023a-143">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="0023a-143">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-144">Windows Server 2012, Windows Server2008R2, Windows 8 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="0023a-144">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-145">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="0023a-145">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0023a-146">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="0023a-146">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-147">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="0023a-147">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-148">Com suporte, mas não pode relatar ou editar configurações de política ou itens de preferência que existem somente no Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0023a-148">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="0023a-149">AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="0023a-149">AGPM4.0 SP2</span></span>


<span data-ttu-id="0023a-150">Se estiver usando computadores que executam o Windows Server2012 R2 ou o Windows 8.1 para gerenciar GPOs, você deve usar o AGPM 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="0023a-150">If you are using computers that are running Windows Server2012 R2 or Windows8.1 to manage GPOs, you must use AGPM4.0 SP2.</span></span> <span data-ttu-id="0023a-151">Não é possível instalar versões anteriores do AGPM em computadores que executam esses sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="0023a-151">You cannot install earlier versions of AGPM on computers that are running those operating systems.</span></span>

<span data-ttu-id="0023a-152">A tabela 1 lista os sistemas operacionais nos quais você pode instalar o AGPM 4.0 SP2 e as configurações de política que você pode gerenciar usando o AGPM 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="0023a-152">Table 1 lists the operating systems on which you can install AGPM4.0 SP2, and the policy settings that you can manage by using AGPM4.0 SP2.</span></span>

**<span data-ttu-id="0023a-153">Tabela 2: sistemas operacionais com suporte do AGPM 4.0 SP2 e configurações de política</span><span class="sxs-lookup"><span data-stu-id="0023a-153">Table 2: AGPM4.0 SP2 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="0023a-154">Configurações com suporte para o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="0023a-154">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="0023a-155">Configurações com suporte para o cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="0023a-155">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="0023a-156">Suporte do AGPM</span><span class="sxs-lookup"><span data-stu-id="0023a-156">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0023a-157">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0023a-157">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-158">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0023a-158">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-159">Com suporte</span><span class="sxs-lookup"><span data-stu-id="0023a-159">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0023a-160">Windows Server2012 R2, Windows Server 2012 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0023a-160">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-161">Windows Server 2012 ou Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="0023a-161">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-162">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0023a-162">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0023a-163">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="0023a-163">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-164">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="0023a-164">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-165">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0023a-165">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0023a-166">Windows Server 2012, Windows Server2008R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="0023a-166">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-167">Windows Server2008 ou WindowsVista com Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="0023a-167">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-168">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server2012 R2, no Windows Server 2012, no Windows Server2008R2, no Windows 8.1 ou no Windows7</span><span class="sxs-lookup"><span data-stu-id="0023a-168">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0023a-169">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="0023a-169">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-170">Windows Server 2012, Windows Server2008R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="0023a-170">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-171">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="0023a-171">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0023a-172">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="0023a-172">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-173">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="0023a-173">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-174">Com suporte, mas não pode relatar ou editar configurações de política ou itens de preferência que existem somente no Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0023a-174">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="0023a-175">AGPM 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="0023a-175">AGPM4.0 SP1</span></span>


<span data-ttu-id="0023a-176">A tabela 2 lista os sistemas operacionais nos quais você pode instalar o AGPM 4,0 SP1 e as configurações de política que você pode gerenciar usando o AGPM 4.0 SP1.</span><span class="sxs-lookup"><span data-stu-id="0023a-176">Table 2 lists the operating systems on which you can install AGPM 4.0 SP1, and the policy settings that you can manage by using AGPM4.0 SP1.</span></span>

**<span data-ttu-id="0023a-177">Tabela 3: sistemas operacionais com suporte do AGPM 4.0 SP1 e configurações de política</span><span class="sxs-lookup"><span data-stu-id="0023a-177">Table 3: AGPM4.0 SP1 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="0023a-178">Configurações com suporte para o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="0023a-178">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="0023a-179">Configurações com suporte para o cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="0023a-179">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="0023a-180">Suporte do AGPM</span><span class="sxs-lookup"><span data-stu-id="0023a-180">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0023a-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0023a-181">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-182">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0023a-182">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-183">Com suporte</span><span class="sxs-lookup"><span data-stu-id="0023a-183">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0023a-184">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="0023a-184">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-185">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="0023a-185">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-186">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="0023a-186">Supported, but cannot edit policy settings or preference items that exist only in Windows 8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0023a-187">Windows Server 2012, Windows Server2008R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="0023a-187">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-188">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="0023a-188">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-189">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server2008R2 ou no Windows7</span><span class="sxs-lookup"><span data-stu-id="0023a-189">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0023a-190">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="0023a-190">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-191">Windows Server 2012, Windows Server2008R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="0023a-191">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-192">Com suporte</span><span class="sxs-lookup"><span data-stu-id="0023a-192">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0023a-193">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="0023a-193">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-194">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="0023a-194">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-195">Com suporte, mas não pode reportar ou editar configurações de política ou itens de preferência que existem somente no Windows Server2008R2 ou no Windows7</span><span class="sxs-lookup"><span data-stu-id="0023a-195">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="0023a-196">AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="0023a-196">AGPM4.0</span></span>


<span data-ttu-id="0023a-197">A tabela 3 lista os sistemas operacionais nos quais você pode instalar o AGPM 4,0 e as configurações de política que você pode gerenciar usando o AGPM 4.0.</span><span class="sxs-lookup"><span data-stu-id="0023a-197">Table 3 lists the operating systems on which you can install AGPM 4.0, and the policy settings that you can manage by using AGPM4.0.</span></span>

**<span data-ttu-id="0023a-198">Tabela 4: sistemas operacionais com suporte do AGPM 4.0 e configurações de política</span><span class="sxs-lookup"><span data-stu-id="0023a-198">Table 4: AGPM4.0 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0023a-199">Sistemas operacionais com suporte para o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="0023a-199">Supported operating systems for the AGPM Server</span></span></th>
<th align="left"><span data-ttu-id="0023a-200">Sistemas operacionais com suporte para o cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="0023a-200">Supported operating systems for the AGPM Client</span></span></th>
<th align="left"><span data-ttu-id="0023a-201">Suporte do AGPM</span><span class="sxs-lookup"><span data-stu-id="0023a-201">AGPM Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0023a-202">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="0023a-202">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-203">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="0023a-203">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-204">Com suporte</span><span class="sxs-lookup"><span data-stu-id="0023a-204">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0023a-205">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="0023a-205">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-206">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="0023a-206">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-207">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server2008R2 ou no Windows7</span><span class="sxs-lookup"><span data-stu-id="0023a-207">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0023a-208">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="0023a-208">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-209">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="0023a-209">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-210">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="0023a-210">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0023a-211">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="0023a-211">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-212">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="0023a-212">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-213">Com suporte, mas não pode reportar ou editar configurações de política ou itens de preferência que existem somente no Windows Server2008R2 ou no Windows7</span><span class="sxs-lookup"><span data-stu-id="0023a-213">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="0023a-214">Versões do AGPM que precedem o AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="0023a-214">Versions of AGPM that precede AGPM4.0</span></span>


<span data-ttu-id="0023a-215">A tabela 4 lista os sistemas operacionais em que você pode instalar as versões do AGPM que precedem o AGPM 4.0.</span><span class="sxs-lookup"><span data-stu-id="0023a-215">Table 4 lists the operating systems on which you can install the versions of AGPM that precede AGPM4.0.</span></span> <span data-ttu-id="0023a-216">Se um sistema operacional não estiver listado, não será possível instalar o AGPM nesse sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0023a-216">If an operating system is not listed, you cannot install AGPM on that operating system.</span></span>

**<span data-ttu-id="0023a-217">Tabela 5: sistemas operacionais com suporte para versões do AGPM que precedem o AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="0023a-217">Table 5: Supported operating systems for versions of AGPM that precede AGPM4.0</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0023a-218">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="0023a-218">Operating system</span></span></th>
<th align="left"><span data-ttu-id="0023a-219">Versão do AGPM que pode ser instalada</span><span class="sxs-lookup"><span data-stu-id="0023a-219">Version of AGPM that can be installed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0023a-220">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="0023a-220">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-221">3,0</span><span class="sxs-lookup"><span data-stu-id="0023a-221">3.0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0023a-222">Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="0023a-222">Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-223">3,0</span><span class="sxs-lookup"><span data-stu-id="0023a-223">3.0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0023a-224">WindowsVista sem Service Pack instalado (32 bits)</span><span class="sxs-lookup"><span data-stu-id="0023a-224">WindowsVista with no service pack installed (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-225">2,5</span><span class="sxs-lookup"><span data-stu-id="0023a-225">2.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0023a-226">Windows Server2003 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="0023a-226">Windows Server2003 (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="0023a-227">2,5</span><span class="sxs-lookup"><span data-stu-id="0023a-227">2.5</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="0023a-228">Como obter tecnologias do MDOP</span><span class="sxs-lookup"><span data-stu-id="0023a-228">How to Get MDOP Technologies</span></span>


<span data-ttu-id="0023a-229">O AGPM 4,0 SP2 faz parte do Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="0023a-229">AGPM 4.0 SP2 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="0023a-230">O MDOP faz parte do Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="0023a-230">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="0023a-231">Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte [como obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="0023a-231">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="0023a-232">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0023a-232">Related topics</span></span>


[<span data-ttu-id="0023a-233">Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="0023a-233">Advanced Group Policy Management</span></span>](index.md)

 

 





