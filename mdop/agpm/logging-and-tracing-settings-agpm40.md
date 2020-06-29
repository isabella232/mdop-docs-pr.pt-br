---
title: Configurações de registro em log e rastreamento
description: Configurações de registro em log e rastreamento
author: dansimp
ms.assetid: 66d03306-80d8-4132-bf71-2827157b1fc9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c58da00e7030c5e4cb3e4d5c4e5bbffa0c754233
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797757"
---
# <span data-ttu-id="d6685-103">Configurações de registro em log e rastreamento</span><span class="sxs-lookup"><span data-stu-id="d6685-103">Logging and Tracing Settings</span></span>


<span data-ttu-id="d6685-104">As configurações de modelo administrativo para gerenciamento avançado de política de grupo (AGPM) permitem que você configure centralmente as opções de log e rastreamento para servidores de AGPM e clientes para os quais um objeto de política de grupo (GPO) com essas configurações é aplicado.</span><span class="sxs-lookup"><span data-stu-id="d6685-104">The Administrative template settings for Advanced Group Policy Management (AGPM) enable you to centrally configure logging and tracing options for AGPM Servers and clients to which a Group Policy Object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="d6685-105">A configuração a seguir está disponível em Computer Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM ao editar um GPO.</span><span class="sxs-lookup"><span data-stu-id="d6685-105">The following setting is available under Computer Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM when editing a GPO.</span></span>

<span data-ttu-id="d6685-106">**Rastrear locais de arquivos**:</span><span class="sxs-lookup"><span data-stu-id="d6685-106">**Trace file locations**:</span></span>

-   <span data-ttu-id="d6685-107">Cliente:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="d6685-107">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

-   <span data-ttu-id="d6685-108">Servidor:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="d6685-108">Server: %ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d6685-109">Configuração</span><span class="sxs-lookup"><span data-stu-id="d6685-109">Setting</span></span></th>
<th align="left"><span data-ttu-id="d6685-110">Efeito</span><span class="sxs-lookup"><span data-stu-id="d6685-110">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="d6685-111">AGPM: configurar o log</span><span class="sxs-lookup"><span data-stu-id="d6685-111">AGPM: Configure logging</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="d6685-112">Essa configuração de política permite ativar e configurar o registro em log para AGPM.</span><span class="sxs-lookup"><span data-stu-id="d6685-112">This policy setting allows you to turn on and configure logging for AGPM.</span></span> <span data-ttu-id="d6685-113">Essa configuração afeta os componentes cliente e servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="d6685-113">This setting affects both client and server components of AGPM.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="d6685-114">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="d6685-114">Additional references</span></span>

-   [<span data-ttu-id="d6685-115">Pasta Modelos Administrativos</span><span class="sxs-lookup"><span data-stu-id="d6685-115">Administrative Templates Folder</span></span>](administrative-templates-folder-agpm40.md)

 

 





