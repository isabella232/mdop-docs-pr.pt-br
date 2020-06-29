---
title: Configurações de conexão do servidor do AGPM
description: Configurações de conexão do servidor do AGPM
author: dansimp
ms.assetid: cc67f122-6309-4820-92c2-f6a27d897123
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 55bd5c04f573a421674068bea6fc9c6adcd29a12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796098"
---
# <span data-ttu-id="f23f6-103">Configurações de conexão do servidor do AGPM</span><span class="sxs-lookup"><span data-stu-id="f23f6-103">AGPM Server Connection Settings</span></span>


<span data-ttu-id="f23f6-104">Você pode usar as configurações de modelo administrativo para o gerenciamento avançado de política de grupo (AGPM) para configurar de forma centralizada as conexões do servidor do AGPM para administradores de política de grupo para os quais um objeto de política de grupo (GPO) com essas configurações é aplicado.</span><span class="sxs-lookup"><span data-stu-id="f23f6-104">You can use Administrative template settings for Advanced Group Policy Management (AGPM) to centrally configure AGPM Server connections for Group Policy administrators to whom a Group Policy Object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="f23f6-105">As configurações a seguir estão disponíveis em User Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM ao editar um GPO.</span><span class="sxs-lookup"><span data-stu-id="f23f6-105">The following settings are available under User Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM when editing a GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f23f6-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="f23f6-106">Setting</span></span></th>
<th align="left"><span data-ttu-id="f23f6-107">Efeito</span><span class="sxs-lookup"><span data-stu-id="f23f6-107">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f23f6-108">AGPM: especificar o servidor do AGPM padrão (todos os domínios)</span><span class="sxs-lookup"><span data-stu-id="f23f6-108">AGPM: Specify default AGPM Server (all domains)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f23f6-109">Essa configuração de política permite especificar um servidor do AGPM padrão para todos os domínios.</span><span class="sxs-lookup"><span data-stu-id="f23f6-109">This policy setting allows you to specify a default AGPM Server for all domains.</span></span> <span data-ttu-id="f23f6-110">Isso é usado somente pelos clientes do AGPM e restringe os administradores de política de grupo a se conectarem a outro arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="f23f6-110">This is used only by AGPM Clients, and restricts Group Policy administrators from connecting to another archive.</span></span> <span data-ttu-id="f23f6-111">Você pode substituir esse padrão para domínios individuais usando a <strong> configuração do AGPM: especificar servidores de AGPM </strong> .</span><span class="sxs-lookup"><span data-stu-id="f23f6-111">You can override this default for individual domains using the <strong>AGPM: Specify AGPM Servers</strong> setting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f23f6-112">AGPM: especificar servidores de AGPM</span><span class="sxs-lookup"><span data-stu-id="f23f6-112">AGPM: Specify AGPM Servers</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f23f6-113">Essa configuração de política permite especificar os servidores do AGPM para domínios individuais.</span><span class="sxs-lookup"><span data-stu-id="f23f6-113">This policy setting allows you to specify the AGPM Servers for individual domains.</span></span> <span data-ttu-id="f23f6-114">Isso é usado somente pelos clientes do AGPM e restringe os administradores de política de grupo a se conectarem a um arquivo morto diferente para o domínio especificado.</span><span class="sxs-lookup"><span data-stu-id="f23f6-114">This is used only by AGPM Clients, and restricts Group Policy administrators from connecting to a different archive for the specified domain.</span></span> <span data-ttu-id="f23f6-115">Para especificar um servidor do AGPM padrão, use o <strong> AGPM: especificar o servidor do AGPM padrão (todos os domínios) </strong> e usar essa configuração de política para substituir o padrão por domínio.</span><span class="sxs-lookup"><span data-stu-id="f23f6-115">To specify a default AGPM Server, use the <strong>AGPM: Specify default AGPM Server (all domains)</strong> setting and use this policy setting to override the default on a per domain basis.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f23f6-116">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="f23f6-116">Additional references</span></span>

-   [<span data-ttu-id="f23f6-117">Pasta Modelos Administrativos</span><span class="sxs-lookup"><span data-stu-id="f23f6-117">Administrative Templates Folder</span></span>](administrative-templates-folder-agpm40.md)

-   [<span data-ttu-id="f23f6-118">Executar tarefas de administração de AGPM</span><span class="sxs-lookup"><span data-stu-id="f23f6-118">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

 

 





