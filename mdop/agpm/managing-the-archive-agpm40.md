---
title: Gerenciamento do arquivo morto
description: Gerenciamento do arquivo morto
author: dansimp
ms.assetid: b11a3d71-74ea-4dd7-b243-6f2880b7af2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 682d720b4095dbfa6a7cc4d868109f57c4f54641
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797749"
---
# <span data-ttu-id="a2147-103">Gerenciamento do arquivo morto</span><span class="sxs-lookup"><span data-stu-id="a2147-103">Managing the Archive</span></span>


<span data-ttu-id="a2147-104">No gerenciamento avançado de política de grupo (AGPM), como administrador do AGPM (controle total), você pode gerenciar o acesso ao arquivo morto e ter a opção de limitar o número de versões de cada objeto de política de grupo (GPO) armazenados no arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="a2147-104">In Advanced Group Policy Management (AGPM), as an AGPM Administrator (Full Control), you manage access to the archive and have the option to limit the number of versions of each Group Policy Object (GPO) stored in the archive.</span></span> <span data-ttu-id="a2147-105">Você pode delegar o acesso a GPOs no arquivo no nível do domínio ou no nível do GPO.</span><span class="sxs-lookup"><span data-stu-id="a2147-105">You can delegate access to GPOs in the archive at the domain level or GPO level.</span></span> <span data-ttu-id="a2147-106">Além disso, é possível fazer backup do arquivo para que você possa recuperá-lo se ocorrer um desastre.</span><span class="sxs-lookup"><span data-stu-id="a2147-106">Additionally, you can back up the archive so that you may be able to recover it if a disaster occurs.</span></span>

<span data-ttu-id="a2147-107">Como administrador do AGPM, você pode exportar um GPO para um arquivo, copiar o arquivo para outra floresta e, em seguida, importar o GPO para um domínio nessa floresta.</span><span class="sxs-lookup"><span data-stu-id="a2147-107">As an AGPM Administrator, you can export a GPO to a file, copy the file to another forest, and then import the GPO into a domain in that forest.</span></span> <span data-ttu-id="a2147-108">Ao contrário de um editor, você pode importar configurações de política de um backup de GPO diretamente para um novo GPO controlado ao criá-lo.</span><span class="sxs-lookup"><span data-stu-id="a2147-108">Unlike an Editor, you can import policy settings from a GPO backup directly into a new controlled GPO when you create it.</span></span> <span data-ttu-id="a2147-109">Para obter informações sobre como exportar um GPO, consulte [exportar um GPO para um arquivo](export-a-gpo-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="a2147-109">For information about how to export a GPO, see [Export a GPO to a File](export-a-gpo-to-a-file.md).</span></span>

-   [<span data-ttu-id="a2147-110">Delegar acesso no nível do domínio ao arquivo morto</span><span class="sxs-lookup"><span data-stu-id="a2147-110">Delegate Domain-Level Access to the Archive</span></span>](delegate-domain-level-access-to-the-archive-agpm40.md)

-   [<span data-ttu-id="a2147-111">Delegar acesso a um GPO individual no arquivo morto</span><span class="sxs-lookup"><span data-stu-id="a2147-111">Delegate Access to an Individual GPO in the Archive</span></span>](delegate-access-to-an-individual-gpo-in-the-archive-agpm40.md)

-   [<span data-ttu-id="a2147-112">Limitar as versões de GPO armazenadas</span><span class="sxs-lookup"><span data-stu-id="a2147-112">Limit the GPO Versions Stored</span></span>](limit-the-gpo-versions-stored-agpm40.md)

-   [<span data-ttu-id="a2147-113">Importar um GPO de um arquivo</span><span class="sxs-lookup"><span data-stu-id="a2147-113">Import a GPO from a File</span></span>](import-a-gpo-from-a-file-agpmadmin.md)

-   [<span data-ttu-id="a2147-114">Fazer backup do arquivo morto</span><span class="sxs-lookup"><span data-stu-id="a2147-114">Back Up the Archive</span></span>](back-up-the-archive-agpm40.md)

-   [<span data-ttu-id="a2147-115">Restaurar o arquivo morto de um backup</span><span class="sxs-lookup"><span data-stu-id="a2147-115">Restore the Archive from a Backup</span></span>](restore-the-archive-from-a-backup-agpm40.md)

### <span data-ttu-id="a2147-116">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="a2147-116">Additional references</span></span>

-   <span data-ttu-id="a2147-117">Para obter informações sobre como delegar o acesso a GPOs no ambiente de produção, consulte [delegar acesso ao ambiente de produção](delegate-access-to-the-production-environment-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="a2147-117">For information about how to delegate access to GPOs in the production environment, see [Delegate Access to the Production Environment](delegate-access-to-the-production-environment-agpm40.md).</span></span>

-   <span data-ttu-id="a2147-118">Para obter informações sobre como mover o arquivo morto, consulte [mover o servidor do AGPM e o arquivo morto](move-the-agpm-server-and-the-archive-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="a2147-118">For information about how to move the archive, see [Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive-agpm40.md).</span></span>

-   [<span data-ttu-id="a2147-119">Executar tarefas de administração de AGPM</span><span class="sxs-lookup"><span data-stu-id="a2147-119">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

 

 





