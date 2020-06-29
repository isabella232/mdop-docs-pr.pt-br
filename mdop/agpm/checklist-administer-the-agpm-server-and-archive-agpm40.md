---
title: Lista de verificação Administre o servidor do AGPM e o arquivamento
description: Lista de verificação Administre o servidor do AGPM e o arquivamento
author: dansimp
ms.assetid: d9c60203-90c2-48a7-9318-197e0ec5038b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f0e464dafa68b9d93c5a1051c986a0efde4702c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797462"
---
# <span data-ttu-id="5d93b-103">Lista de verificação: Administrar o servidor e o arquivo morto do AGPM</span><span class="sxs-lookup"><span data-stu-id="5d93b-103">Checklist: Administer the AGPM Server and Archive</span></span>


<span data-ttu-id="5d93b-104">No gerenciamento avançado de política de grupo (AGPM), o Serviço AGPM e o arquivo são gerenciados por administradores do AGPM (controle total).</span><span class="sxs-lookup"><span data-stu-id="5d93b-104">In Advanced Group Policy Management (AGPM), both the AGPM Service and the archive are managed by AGPM Administrators (Full Control).</span></span> <span data-ttu-id="5d93b-105">Veja a seguir as tarefas típicas de um administrador do AGPM.</span><span class="sxs-lookup"><span data-stu-id="5d93b-105">The following are typical tasks for an AGPM Administrator.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5d93b-106">Tarefa frequente</span><span class="sxs-lookup"><span data-stu-id="5d93b-106">Frequent Task</span></span></th>
<th align="left"><span data-ttu-id="5d93b-107">Referência</span><span class="sxs-lookup"><span data-stu-id="5d93b-107">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5d93b-108">Acesse o acesso a objetos de política de grupo (GPOs) no arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="5d93b-108">Delegate access to Group Policy Objects (GPOs) in the archive.</span></span></p></td>
<td align="left"><p><a href="delegate-domain-level-access-to-the-archive-agpm40.md" data-raw-source="[Delegate Domain-Level Access to the Archive](delegate-domain-level-access-to-the-archive-agpm40.md)"><span data-ttu-id="5d93b-109">Delegar acesso no nível do domínio ao arquivo morto</span><span class="sxs-lookup"><span data-stu-id="5d93b-109">Delegate Domain-Level Access to the Archive</span></span></a></p>
<p><a href="delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md" data-raw-source="[Delegate Access to an Individual GPO in the Archive](delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md)"><span data-ttu-id="5d93b-110">Delegar acesso a um GPO individual no arquivo morto</span><span class="sxs-lookup"><span data-stu-id="5d93b-110">Delegate Access to an Individual GPO in the Archive</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5d93b-111">Faça backup do arquivo morto para habilitar a recuperação de desastres.</span><span class="sxs-lookup"><span data-stu-id="5d93b-111">Back up the archive to enable disaster recovery.</span></span></p></td>
<td align="left"><p><a href="back-up-the-archive-agpm40.md" data-raw-source="[Back Up the Archive](back-up-the-archive-agpm40.md)"><span data-ttu-id="5d93b-112">Fazer backup do arquivo morto</span><span class="sxs-lookup"><span data-stu-id="5d93b-112">Back Up the Archive</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5d93b-113">Tarefa não frequente</span><span class="sxs-lookup"><span data-stu-id="5d93b-113">Infrequent Task</span></span></th>
<th align="left"><span data-ttu-id="5d93b-114">Referência</span><span class="sxs-lookup"><span data-stu-id="5d93b-114">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5d93b-115">Restaure o arquivo a partir de um backup para recuperar-se de um desastre.</span><span class="sxs-lookup"><span data-stu-id="5d93b-115">Restore the archive from a backup to recover from a disaster.</span></span></p></td>
<td align="left"><p><a href="restore-the-archive-from-a-backup-agpm40.md" data-raw-source="[Restore the Archive from a Backup](restore-the-archive-from-a-backup-agpm40.md)"><span data-ttu-id="5d93b-116">Restaurar o arquivo morto de um backup</span><span class="sxs-lookup"><span data-stu-id="5d93b-116">Restore the Archive from a Backup</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5d93b-117">Mova o serviço do AGPM, o arquivo ou ambos para um servidor diferente.</span><span class="sxs-lookup"><span data-stu-id="5d93b-117">Move the AGPM Service, the archive, or both to a different server.</span></span></p></td>
<td align="left"><p><a href="move-the-agpm-server-and-the-archive-agpm40.md" data-raw-source="[Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive-agpm40.md)"><span data-ttu-id="5d93b-118">Mover o servidor e o arquivo morto do AGPM</span><span class="sxs-lookup"><span data-stu-id="5d93b-118">Move the AGPM Server and the Archive</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5d93b-119">Altere o caminho de arquivo morto, a conta de serviço do AGPM ou a porta que o serviço do AGPM escuta.</span><span class="sxs-lookup"><span data-stu-id="5d93b-119">Change the archive path, the AGPM Service Account, or the port on which the AGPM Service listens.</span></span></p></td>
<td align="left"><p><a href="modify-the-agpm-service-agpm40.md" data-raw-source="[Modify the AGPM Service](modify-the-agpm-service-agpm40.md)"><span data-ttu-id="5d93b-120">Modificar o serviço AGPM</span><span class="sxs-lookup"><span data-stu-id="5d93b-120">Modify the AGPM Service</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5d93b-121">Solucionar problemas comuns com o servidor do AGPM.</span><span class="sxs-lookup"><span data-stu-id="5d93b-121">Troubleshoot common problems with the AGPM Server.</span></span></p></td>
<td align="left"><p><a href="troubleshooting-agpm-agpm40.md" data-raw-source="[Troubleshooting AGPM](troubleshooting-agpm-agpm40.md)"><span data-ttu-id="5d93b-122">Solução de problemas do AGPM</span><span class="sxs-lookup"><span data-stu-id="5d93b-122">Troubleshooting AGPM</span></span></a></p>
<p><a href="configure-logging-and-tracing-agpm40.md" data-raw-source="[Configure Logging and Tracing](configure-logging-and-tracing-agpm40.md)"><span data-ttu-id="5d93b-123">Configurar log e rastreamento</span><span class="sxs-lookup"><span data-stu-id="5d93b-123">Configure Logging and Tracing</span></span></a></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="5d93b-124">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="5d93b-124">Additional references</span></span>

-   [<span data-ttu-id="5d93b-125">Gerenciamento Avançado de Política de Grupo 4.0</span><span class="sxs-lookup"><span data-stu-id="5d93b-125">Advanced Group Policy Management 4.0</span></span>](advanced-group-policy-management-40.md)

 

 





