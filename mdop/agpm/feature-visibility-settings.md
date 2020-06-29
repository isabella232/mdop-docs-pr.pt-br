---
title: Configurações de visibilidade do recurso
description: Configurações de visibilidade do recurso
author: dansimp
ms.assetid: 9db2ba03-fb75-4f95-9138-ec89b9fc8d01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26f19895d0a9163885779688ba7d89f6d16f2a17
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797799"
---
# <span data-ttu-id="26b89-103">Configurações de visibilidade do recurso</span><span class="sxs-lookup"><span data-stu-id="26b89-103">Feature Visibility Settings</span></span>


<span data-ttu-id="26b89-104">As configurações de modelo administrativo para gerenciamento avançado de política de grupo (AGPM) permitem que você configure centralmente a visibilidade do nó de **controle de alterações** e a guia **histórico** para administradores de política de grupo para os quais um objeto de política de grupo (GPO) com essas configurações é aplicado.</span><span class="sxs-lookup"><span data-stu-id="26b89-104">The Administrative template settings for Advanced Group Policy Management (AGPM) enable you to centrally configure the visibility of the **Change Control** node and **History** tab for Group Policy administrators to whom a Group Policy object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="26b89-105">As configurações a seguir estão disponíveis em snap-ins do Configuration\\Administrative Templates\\Windows Components\\Microsoft console de gerenciamento \ \ restritos/permitidos Snap-ins\\Extension no **Editor de objeto de política de grupo** durante a edição de um GPO no GPMC (console de gerenciamento de política de grupo).</span><span class="sxs-lookup"><span data-stu-id="26b89-105">The following settings are available under User Configuration\\Administrative Templates\\Windows Components\\Microsoft Management Console\\Restricted/Permitted Snap-ins\\Extension Snap-ins in the **Group Policy Object Editor** when editing a GPO in the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="26b89-106">Se esse caminho não estiver visível, clique com o botão direito do mouse em **modelos administrativos**e adicione o modelo AGPM. admx ou AGPM. adm.</span><span class="sxs-lookup"><span data-stu-id="26b89-106">If this path is not visible, right-click **Administrative Templates**, and add the agpm.admx or agpm.adm template.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="26b89-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="26b89-107">Setting</span></span></th>
<th align="left"><span data-ttu-id="26b89-108">Efeito</span><span class="sxs-lookup"><span data-stu-id="26b89-108">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="26b89-109">Controle de alterações do AGPM</span><span class="sxs-lookup"><span data-stu-id="26b89-109">AGPM Change Control</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="26b89-110">Se habilitada ou não configurada, o <strong> nó de controle de alterações </strong> fica visível no GPMC.</span><span class="sxs-lookup"><span data-stu-id="26b89-110">If enabled or not configured, the <strong>Change Control</strong> node is visible in the GPMC.</span></span></p>
<p><span data-ttu-id="26b89-111">Se desabilitado, o <strong> nó de controle de alterações </strong> não fica visível no GPMC.</span><span class="sxs-lookup"><span data-stu-id="26b89-111">If disabled, the <strong>Change Control</strong> node is not visible in the GPMC.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="26b89-112">Extensão do link do AGPM</span><span class="sxs-lookup"><span data-stu-id="26b89-112">AGPM Link Extension</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="26b89-113">Se habilitada ou não configurada, uma <strong> </strong> guia histórico será exibida no GPMC para cada GPO vinculado.</span><span class="sxs-lookup"><span data-stu-id="26b89-113">If enabled or not configured, a <strong>History</strong> tab appears in the GPMC for each linked GPO.</span></span></p>
<p><span data-ttu-id="26b89-114">Se desabilitado, <strong> a </strong> guia histórico não fica visível para GPOs vinculados.</span><span class="sxs-lookup"><span data-stu-id="26b89-114">If disabled, the <strong>History</strong> tab is not visible for linked GPOs.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="26b89-115">Extensão do GPO do AGPM</span><span class="sxs-lookup"><span data-stu-id="26b89-115">AGPM GPO Extension</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="26b89-116">Se habilitada ou não configurada, uma <strong> </strong> guia histórico será exibida no GPMC para cada GPO.</span><span class="sxs-lookup"><span data-stu-id="26b89-116">If enabled or not configured, a <strong>History</strong> tab appears in the GPMC for each GPO.</span></span></p>
<p><span data-ttu-id="26b89-117">Se desabilitado, <strong> a </strong> guia histórico não fica visível para GPOs.</span><span class="sxs-lookup"><span data-stu-id="26b89-117">If disabled, the <strong>History</strong> tab is not visible for GPOs.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="26b89-118">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="26b89-118">Additional references</span></span>

-   [<span data-ttu-id="26b89-119">Configurações de Modelo Administrativo</span><span class="sxs-lookup"><span data-stu-id="26b89-119">Administrative Template Settings</span></span>](administrative-template-settings.md)

 

 





