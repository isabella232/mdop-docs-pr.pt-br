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
ms.openlocfilehash: b09ea8161b6801c62552f1c0d0ef8455dc111e2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797457"
---
# <span data-ttu-id="7d9be-103">Como escolher qual versão do AGPM a ser instalada</span><span class="sxs-lookup"><span data-stu-id="7d9be-103">Choosing Which Version of AGPM to Install</span></span>


<span data-ttu-id="7d9be-104">Cada lançamento do gerenciamento de política de grupo (AGPM) do MicrosoftAdvanced oferece suporte a versões específicas do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="7d9be-104">Each release of MicrosoftAdvanced Group Policy Management (AGPM) supports specific versions of the Windows operating system.</span></span> <span data-ttu-id="7d9be-105">É altamente recomendável que você execute o cliente do AGPM e o servidor do AGPM na mesma linha de sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="7d9be-105">We strongly recommend that you run the AGPM Client and AGPM Server on the same line of operating systems.</span></span> <span data-ttu-id="7d9be-106">Por exemplo, Windows 10 com Windows Server 2016, Windows 8.1 com Windows Server2012 R2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="7d9be-106">For example, Windows 10 with Windows Server 2016, Windows8.1 with Windows Server2012 R2, and so on.</span></span>

<span data-ttu-id="7d9be-107">Recomendamos que você instale o servidor do AGPM na versão mais recente do sistema operacional do domínio.</span><span class="sxs-lookup"><span data-stu-id="7d9be-107">We recommend that you install the AGPM Server on the most recent version of the operating system in the domain.</span></span> <span data-ttu-id="7d9be-108">O AGPM usa o GPMC (console de gerenciamento de política de grupo) para fazer backup e restaurar objetos de política de grupo (GPOs).</span><span class="sxs-lookup"><span data-stu-id="7d9be-108">AGPM uses the Group Policy Management Console (GPMC) to back up and restore Group Policy Objects (GPOs).</span></span> <span data-ttu-id="7d9be-109">Como as versões mais recentes do GPMC fornecem configurações de política adicionais que não estão disponíveis em versões anteriores, você pode gerenciar mais configurações de política usando a versão mais recente do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7d9be-109">Because newer versions of the GPMC provide additional policy settings that are not available in earlier versions, you can manage more policy settings by using the most recent version of the operating system.</span></span>

<span data-ttu-id="7d9be-110">Todas as versões do AGPM podem gerenciar apenas as configurações de política que foram introduzidas na mesma versão ou em uma versão anterior do sistema operacional em que o AGPM está em execução.</span><span class="sxs-lookup"><span data-stu-id="7d9be-110">All versions of AGPM can manage only the policy settings that were introduced in the same version or an earlier version of the operating system on which AGPM is running.</span></span> <span data-ttu-id="7d9be-111">Por exemplo, se você instalar o AGPM 4.0 SP2 no Windows Server 2012, poderá gerenciar as configurações de política que foram introduzidas no Windows Server 2012 ou anterior, mas não poderá gerenciar as configurações de política que foram introduzidas mais tarde, no Windows 8.1 ou no Windows Server2012 R2.</span><span class="sxs-lookup"><span data-stu-id="7d9be-111">For example, if you install AGPM4.0 SP2 on Windows Server 2012, you can manage policy settings that were introduced in Windows Server 2012 or earlier, but you cannot manage policy settings that were introduced later, in Windows8.1 or Windows Server2012 R2.</span></span>

<span data-ttu-id="7d9be-112">Se a versão do GPMC em seu servidor do AGPM for mais antiga do que a versão nos computadores que os administradores usam para gerenciar a política de grupo, o servidor do AGPM não poderá armazenar nenhuma configuração de política que não esteja disponível na versão anterior do GPMC.</span><span class="sxs-lookup"><span data-stu-id="7d9be-112">If the version of the GPMC on your AGPM Server is older than the version on the computers that administrators use to manage Group Policy, the AGPM Server will be unable to store any policy settings that are not available in the older version of the GPMC.</span></span> <span data-ttu-id="7d9be-113">Consulte a planilha de configurações de Política de Grupo incluídas no Windows na [Referência de configurações de Política de Grupo para Windows e Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span><span class="sxs-lookup"><span data-stu-id="7d9be-113">For a spreadsheet of Group Policy settings included in Windows, see [Group Policy Settings Reference for Windows and Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span></span>

## <span data-ttu-id="7d9be-114">AGPM 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="7d9be-114">AGPM4.0 SP3</span></span>


<span data-ttu-id="7d9be-115">Se você estiver usando computadores que executam o Windows 10 para gerenciar GPOs, deverá usar o AGPM 4,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="7d9be-115">If you are using computers that are running Windows 10 to manage GPOs, you must use AGPM 4.0 SP3.</span></span> <span data-ttu-id="7d9be-116">Não é possível instalar versões anteriores do AGPM em computadores que executam o sistema operacional Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7d9be-116">You cannot install earlier versions of AGPM on computers that are running the Windows 10 operating system.</span></span>

<span data-ttu-id="7d9be-117">A tabela 1 lista os sistemas operacionais nos quais você pode instalar o AGPM 4.0 SP3 e as configurações de política que você pode gerenciar usando o AGPM 4.0 SP3.</span><span class="sxs-lookup"><span data-stu-id="7d9be-117">Table 1 lists the operating systems on which you can install AGPM4.0 SP3, and the policy settings that you can manage by using AGPM4.0 SP3.</span></span>

**<span data-ttu-id="7d9be-118">Tabela 1: sistemas operacionais compatíveis com o AGPM 4,0 SP3 e configurações de política</span><span class="sxs-lookup"><span data-stu-id="7d9be-118">Table 1: AGPM 4.0 SP3 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="7d9be-119">Configurações com suporte para o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="7d9be-119">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="7d9be-120">Configurações com suporte para o cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="7d9be-120">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="7d9be-121">Suporte do AGPM</span><span class="sxs-lookup"><span data-stu-id="7d9be-121">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d9be-122">Windows Server 2016 ou Windows 10</span><span class="sxs-lookup"><span data-stu-id="7d9be-122">Windows Server 2016 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-123">Windows Server 2016 ou Windows 10</span><span class="sxs-lookup"><span data-stu-id="7d9be-123">Windows Server 2016 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-124">Com suporte</span><span class="sxs-lookup"><span data-stu-id="7d9be-124">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d9be-125">Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="7d9be-125">Windows Server2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-126">Windows 10</span><span class="sxs-lookup"><span data-stu-id="7d9be-126">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-127">Compatível com as advertências descritas em <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)"> KB 4015786</span><span class="sxs-lookup"><span data-stu-id="7d9be-127">Supported with the caveats outlined in <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)">KB 4015786</span></span></a>
</p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d9be-128">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7d9be-128">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-129">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7d9be-129">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="7d9be-130">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d9be-131">Windows Server2012 R2, Windows Server 2012 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7d9be-131">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-132">Windows Server 2012 ou Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="7d9be-132">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-133">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7d9be-133">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d9be-134">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="7d9be-134">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-135">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="7d9be-135">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-136">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7d9be-136">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d9be-137">Windows Server 2012, Windows Server2008R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="7d9be-137">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-138">Windows Server2008 ou WindowsVista com Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="7d9be-138">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-139">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server2012 R2, no Windows Server 2012, no Windows Server2008R2, no Windows 8.1 ou no Windows7</span><span class="sxs-lookup"><span data-stu-id="7d9be-139">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d9be-140">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="7d9be-140">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-141">Windows Server 2012, Windows Server2008R2, Windows 8 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="7d9be-141">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-142">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="7d9be-142">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d9be-143">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="7d9be-143">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-144">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="7d9be-144">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-145">Com suporte, mas não pode relatar ou editar configurações de política ou itens de preferência que existem somente no Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7d9be-145">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="7d9be-146">AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="7d9be-146">AGPM4.0 SP2</span></span>


<span data-ttu-id="7d9be-147">Se estiver usando computadores que executam o Windows Server2012 R2 ou o Windows 8.1 para gerenciar GPOs, você deve usar o AGPM 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="7d9be-147">If you are using computers that are running Windows Server2012 R2 or Windows8.1 to manage GPOs, you must use AGPM4.0 SP2.</span></span> <span data-ttu-id="7d9be-148">Não é possível instalar versões anteriores do AGPM em computadores que executam esses sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="7d9be-148">You cannot install earlier versions of AGPM on computers that are running those operating systems.</span></span>

<span data-ttu-id="7d9be-149">A tabela 1 lista os sistemas operacionais nos quais você pode instalar o AGPM 4.0 SP2 e as configurações de política que você pode gerenciar usando o AGPM 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="7d9be-149">Table 1 lists the operating systems on which you can install AGPM4.0 SP2, and the policy settings that you can manage by using AGPM4.0 SP2.</span></span>

**<span data-ttu-id="7d9be-150">Tabela 2: sistemas operacionais com suporte do AGPM 4.0 SP2 e configurações de política</span><span class="sxs-lookup"><span data-stu-id="7d9be-150">Table 2: AGPM4.0 SP2 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="7d9be-151">Configurações com suporte para o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="7d9be-151">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="7d9be-152">Configurações com suporte para o cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="7d9be-152">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="7d9be-153">Suporte do AGPM</span><span class="sxs-lookup"><span data-stu-id="7d9be-153">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d9be-154">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7d9be-154">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-155">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7d9be-155">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-156">Com suporte</span><span class="sxs-lookup"><span data-stu-id="7d9be-156">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d9be-157">Windows Server2012 R2, Windows Server 2012 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7d9be-157">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-158">Windows Server 2012 ou Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="7d9be-158">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-159">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7d9be-159">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d9be-160">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="7d9be-160">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-161">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="7d9be-161">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-162">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7d9be-162">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d9be-163">Windows Server 2012, Windows Server2008R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="7d9be-163">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-164">Windows Server2008 ou WindowsVista com Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="7d9be-164">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-165">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server2012 R2, no Windows Server 2012, no Windows Server2008R2, no Windows 8.1 ou no Windows7</span><span class="sxs-lookup"><span data-stu-id="7d9be-165">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d9be-166">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="7d9be-166">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-167">Windows Server 2012, Windows Server2008R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="7d9be-167">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-168">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="7d9be-168">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d9be-169">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="7d9be-169">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-170">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="7d9be-170">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-171">Com suporte, mas não pode relatar ou editar configurações de política ou itens de preferência que existem somente no Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7d9be-171">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="7d9be-172">AGPM 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="7d9be-172">AGPM4.0 SP1</span></span>


<span data-ttu-id="7d9be-173">A tabela 2 lista os sistemas operacionais nos quais você pode instalar o AGPM 4,0 SP1 e as configurações de política que você pode gerenciar usando o AGPM 4.0 SP1.</span><span class="sxs-lookup"><span data-stu-id="7d9be-173">Table 2 lists the operating systems on which you can install AGPM 4.0 SP1, and the policy settings that you can manage by using AGPM4.0 SP1.</span></span>

**<span data-ttu-id="7d9be-174">Tabela 3: sistemas operacionais com suporte do AGPM 4.0 SP1 e configurações de política</span><span class="sxs-lookup"><span data-stu-id="7d9be-174">Table 3: AGPM4.0 SP1 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="7d9be-175">Configurações com suporte para o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="7d9be-175">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="7d9be-176">Configurações com suporte para o cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="7d9be-176">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="7d9be-177">Suporte do AGPM</span><span class="sxs-lookup"><span data-stu-id="7d9be-177">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d9be-178">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7d9be-178">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-179">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7d9be-179">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-180">Com suporte</span><span class="sxs-lookup"><span data-stu-id="7d9be-180">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d9be-181">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="7d9be-181">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-182">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="7d9be-182">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-183">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="7d9be-183">Supported, but cannot edit policy settings or preference items that exist only in Windows 8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d9be-184">Windows Server 2012, Windows Server2008R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="7d9be-184">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-185">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="7d9be-185">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-186">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server2008R2 ou no Windows7</span><span class="sxs-lookup"><span data-stu-id="7d9be-186">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d9be-187">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="7d9be-187">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-188">Windows Server 2012, Windows Server2008R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="7d9be-188">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-189">Com suporte</span><span class="sxs-lookup"><span data-stu-id="7d9be-189">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d9be-190">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="7d9be-190">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-191">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="7d9be-191">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-192">Com suporte, mas não pode reportar ou editar configurações de política ou itens de preferência que existem somente no Windows Server2008R2 ou no Windows7</span><span class="sxs-lookup"><span data-stu-id="7d9be-192">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="7d9be-193">AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="7d9be-193">AGPM4.0</span></span>


<span data-ttu-id="7d9be-194">A tabela 3 lista os sistemas operacionais nos quais você pode instalar o AGPM 4,0 e as configurações de política que você pode gerenciar usando o AGPM 4.0.</span><span class="sxs-lookup"><span data-stu-id="7d9be-194">Table 3 lists the operating systems on which you can install AGPM 4.0, and the policy settings that you can manage by using AGPM4.0.</span></span>

**<span data-ttu-id="7d9be-195">Tabela 4: sistemas operacionais com suporte do AGPM 4.0 e configurações de política</span><span class="sxs-lookup"><span data-stu-id="7d9be-195">Table 4: AGPM4.0 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7d9be-196">Sistemas operacionais com suporte para o servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="7d9be-196">Supported operating systems for the AGPM Server</span></span></th>
<th align="left"><span data-ttu-id="7d9be-197">Sistemas operacionais com suporte para o cliente do AGPM</span><span class="sxs-lookup"><span data-stu-id="7d9be-197">Supported operating systems for the AGPM Client</span></span></th>
<th align="left"><span data-ttu-id="7d9be-198">Suporte do AGPM</span><span class="sxs-lookup"><span data-stu-id="7d9be-198">AGPM Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d9be-199">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="7d9be-199">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-200">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="7d9be-200">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-201">Com suporte</span><span class="sxs-lookup"><span data-stu-id="7d9be-201">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d9be-202">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="7d9be-202">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-203">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="7d9be-203">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-204">Com suporte, mas não é possível editar configurações de política ou itens de preferência que existem somente no Windows Server2008R2 ou no Windows7</span><span class="sxs-lookup"><span data-stu-id="7d9be-204">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d9be-205">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="7d9be-205">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-206">Windows Server2008R2 ou Windows7</span><span class="sxs-lookup"><span data-stu-id="7d9be-206">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-207">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="7d9be-207">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d9be-208">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="7d9be-208">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-209">Windows Server2008 ou Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="7d9be-209">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-210">Com suporte, mas não pode reportar ou editar configurações de política ou itens de preferência que existem somente no Windows Server2008R2 ou no Windows7</span><span class="sxs-lookup"><span data-stu-id="7d9be-210">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="7d9be-211">Versões do AGPM que precedem o AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="7d9be-211">Versions of AGPM that precede AGPM4.0</span></span>


<span data-ttu-id="7d9be-212">A tabela 4 lista os sistemas operacionais em que você pode instalar as versões do AGPM que precedem o AGPM 4.0.</span><span class="sxs-lookup"><span data-stu-id="7d9be-212">Table 4 lists the operating systems on which you can install the versions of AGPM that precede AGPM4.0.</span></span> <span data-ttu-id="7d9be-213">Se um sistema operacional não estiver listado, não será possível instalar o AGPM nesse sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7d9be-213">If an operating system is not listed, you cannot install AGPM on that operating system.</span></span>

**<span data-ttu-id="7d9be-214">Tabela 5: sistemas operacionais com suporte para versões do AGPM que precedem o AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="7d9be-214">Table 5: Supported operating systems for versions of AGPM that precede AGPM4.0</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7d9be-215">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="7d9be-215">Operating system</span></span></th>
<th align="left"><span data-ttu-id="7d9be-216">Versão do AGPM que pode ser instalada</span><span class="sxs-lookup"><span data-stu-id="7d9be-216">Version of AGPM that can be installed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d9be-217">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="7d9be-217">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-218">3,0</span><span class="sxs-lookup"><span data-stu-id="7d9be-218">3.0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d9be-219">Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="7d9be-219">Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-220">3,0</span><span class="sxs-lookup"><span data-stu-id="7d9be-220">3.0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7d9be-221">WindowsVista sem Service Pack instalado (32 bits)</span><span class="sxs-lookup"><span data-stu-id="7d9be-221">WindowsVista with no service pack installed (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-222">2,5</span><span class="sxs-lookup"><span data-stu-id="7d9be-222">2.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7d9be-223">Windows Server2003 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="7d9be-223">Windows Server2003 (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="7d9be-224">2,5</span><span class="sxs-lookup"><span data-stu-id="7d9be-224">2.5</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="7d9be-225">Como obter tecnologias do MDOP</span><span class="sxs-lookup"><span data-stu-id="7d9be-225">How to Get MDOP Technologies</span></span>


<span data-ttu-id="7d9be-226">O AGPM 4,0 SP2 faz parte do Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="7d9be-226">AGPM 4.0 SP2 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="7d9be-227">O MDOP faz parte do Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="7d9be-227">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="7d9be-228">Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte [como obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="7d9be-228">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="7d9be-229">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d9be-229">Related topics</span></span>


[<span data-ttu-id="7d9be-230">Gerenciamento Avançado de Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="7d9be-230">Advanced Group Policy Management</span></span>](index.md)

 

 





