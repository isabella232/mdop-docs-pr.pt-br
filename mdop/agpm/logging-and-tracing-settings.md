---
title: Configurações de registro em log e rastreamento
description: Configurações de registro em log e rastreamento
author: dansimp
ms.assetid: db6b43c7-fdde-4d11-b5ab-a81346e56940
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bef0f8367647aad688c2aec7586ecdaae2e22143
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797755"
---
# <span data-ttu-id="e8f01-103">Configurações de registro em log e rastreamento</span><span class="sxs-lookup"><span data-stu-id="e8f01-103">Logging and Tracing Settings</span></span>


<span data-ttu-id="e8f01-104">As configurações de modelo administrativo para gerenciamento avançado de política de grupo (AGPM) permitem que você configure centralmente as opções de log e rastreamento para servidores de AGPM e clientes para os quais um objeto de política de grupo (GPO) com essas configurações é aplicado.</span><span class="sxs-lookup"><span data-stu-id="e8f01-104">The Administrative Template settings for Advanced Group Policy Management (AGPM) enable you to centrally configure logging and tracing options for AGPM Servers and clients to which a Group Policy object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="e8f01-105">A configuração a seguir está disponível em Computer Configuration\\Administrative Templates\\Windows Components\\AGPM no **Editor de objeto de política de grupo** durante a edição de um GPO no GPMC (console de gerenciamento de política de grupo).</span><span class="sxs-lookup"><span data-stu-id="e8f01-105">The following setting is available under Computer Configuration\\Administrative Templates\\Windows Components\\AGPM in the **Group Policy Object Editor** when editing a GPO in the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="e8f01-106">Se esse caminho não estiver visível, clique com o botão direito do mouse em **modelos administrativos**e adicione o modelo AGPM. admx ou AGPM. adm.</span><span class="sxs-lookup"><span data-stu-id="e8f01-106">If this path is not visible, right-click **Administrative Templates**, and add the agpm.admx or agpm.adm template.</span></span>

<span data-ttu-id="e8f01-107">**Rastrear locais de arquivos**:</span><span class="sxs-lookup"><span data-stu-id="e8f01-107">**Trace file locations**:</span></span>

-   <span data-ttu-id="e8f01-108">Cliente:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="e8f01-108">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

-   <span data-ttu-id="e8f01-109">Servidor:%CommonAppData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="e8f01-109">Server: %CommonAppData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e8f01-110">Configuração</span><span class="sxs-lookup"><span data-stu-id="e8f01-110">Setting</span></span></th>
<th align="left"><span data-ttu-id="e8f01-111">Efeito</span><span class="sxs-lookup"><span data-stu-id="e8f01-111">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e8f01-112">Log do AGPM</span><span class="sxs-lookup"><span data-stu-id="e8f01-112">AGPM Logging</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e8f01-113">Se habilitada, essa configuração define se o rastreamento está ativado e o nível de detalhes.</span><span class="sxs-lookup"><span data-stu-id="e8f01-113">If enabled, this setting configures whether tracing is turned on and the level of detail.</span></span> <span data-ttu-id="e8f01-114">Essa configuração afeta os componentes cliente e servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="e8f01-114">This setting affects both client and server components of AGPM.</span></span></p>
<p><span data-ttu-id="e8f01-115">Se desabilitada ou não configurada, essa configuração não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="e8f01-115">If disabled or not configured, this setting has no effect.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="e8f01-116">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="e8f01-116">Additional references</span></span>

-   [<span data-ttu-id="e8f01-117">Configurações de Modelo Administrativo</span><span class="sxs-lookup"><span data-stu-id="e8f01-117">Administrative Template Settings</span></span>](administrative-template-settings.md)

 

 





