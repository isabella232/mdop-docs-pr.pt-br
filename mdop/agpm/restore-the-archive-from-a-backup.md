---
title: Restaurar o arquivo morto de um backup
description: Restaurar o arquivo morto de um backup
author: dansimp
ms.assetid: 49666337-d72c-4e44-99e4-9eb59b2355a9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b00d2e5e612e2ac43f965e4adf6175e2fd159007
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797310"
---
# <span data-ttu-id="e136b-103">Restaurar o arquivo morto de um backup</span><span class="sxs-lookup"><span data-stu-id="e136b-103">Restore the Archive from a Backup</span></span>


<span data-ttu-id="e136b-104">Se ocorrer um desastre e o arquivo para o gerenciamento avançado de política de grupo (AGPM) estiver danificado ou destruído, um administrador do AGPM (controle total) pode restaurar o arquivo de uma cópia de backup preparada antecipadamente e, em seguida, importar do ambiente de produção qualquer objeto de política de grupo (GPOs) que não esteja no arquivo morto</span><span class="sxs-lookup"><span data-stu-id="e136b-104">If a disaster occurs and the archive for Advanced Group Policy Management (AGPM) is damaged or destroyed, an AGPM Administrator (Full Control) can restore the archive from a backup copy prepared in advance and then import from the production environment any Group Policy Objects (GPOs) that are not in the archive or for which the version in production is more current than that in the archive.</span></span> <span data-ttu-id="e136b-105">Para obter informações sobre como restaurar um backup de arquivo morto para um servidor diferente, consulte [mover o servidor do AGPM e o arquivo morto](move-the-agpm-server-and-the-archive.md).</span><span class="sxs-lookup"><span data-stu-id="e136b-105">For information about how to restore an archive backup to a different server, see [Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive.md).</span></span>

<span data-ttu-id="e136b-106">Uma conta de usuário que tenha acesso ao servidor do AGPM (o computador no qual o serviço do AGPM está instalado) e à pasta que contém o arquivo morto será necessária para concluir esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="e136b-106">A user account that has access to the AGPM Server (the computer on which the AGPM Service is installed) and to the folder that contains the archive is required to complete this procedure.</span></span>

**<span data-ttu-id="e136b-107">Para restaurar o arquivo de um backup</span><span class="sxs-lookup"><span data-stu-id="e136b-107">To restore the archive from a backup</span></span>**

1.  <span data-ttu-id="e136b-108">Interrompa o serviço do AGPM.</span><span class="sxs-lookup"><span data-stu-id="e136b-108">Stop the AGPM Service.</span></span> <span data-ttu-id="e136b-109">Para obter mais informações, consulte [Iniciar e interromper o serviço do AGPM](start-and-stop-the-agpm-service-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="e136b-109">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm30ops.md).</span></span>

2.  <span data-ttu-id="e136b-110">Remova o arquivo morto existente.</span><span class="sxs-lookup"><span data-stu-id="e136b-110">Remove the existing archive.</span></span> <span data-ttu-id="e136b-111">Por padrão, a pasta arquivo morto é%ProgramData%\\Microsoft\\AGPM, no entanto, o administrador do AGPM que instalou o gerenciamento avançado de política de grupo da Microsoft – o servidor pode ter entrado um local diferente durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="e136b-111">By default, the archive folder is %ProgramData%\\Microsoft\\AGPM, however the AGPM Administrator who installed Microsoft Advanced Group Policy Management - Server may have entered a different location during setup.</span></span>

3.  <span data-ttu-id="e136b-112">Recrie a pasta arquivo morto Configurando o caminho do arquivo, a conta do serviço do AGPM, o proprietário do arquivo e a porta de escuta.</span><span class="sxs-lookup"><span data-stu-id="e136b-112">Re-create the archive folder by configuring the archive path, AGPM Service Account, Archive Owner, and listening port.</span></span> <span data-ttu-id="e136b-113">Não é necessário usar os mesmos valores usados durante a instalação original.</span><span class="sxs-lookup"><span data-stu-id="e136b-113">Using the same values as used during the original installation is not necessary.</span></span> <span data-ttu-id="e136b-114">Para obter mais informações, consulte [Modificar o serviço do AGPM](modify-the-agpm-service-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="e136b-114">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm30ops.md).</span></span>

4.  <span data-ttu-id="e136b-115">Copie o conteúdo do arquivo morto backup para a pasta de arquivo morto, copiando as subpastas e arquivos para garantir que cada subpasta e arquivo herdem as permissões da pasta arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="e136b-115">Copy the contents of the archive backup to the archive folder, copying the subfolders and files to make sure that each subfolder and file inherits the permissions of the archive folder.</span></span> <span data-ttu-id="e136b-116">Tome cuidado para não substituir a pasta de arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="e136b-116">Be careful not to overwrite the archive folder.</span></span>

5.  <span data-ttu-id="e136b-117">Se você não tiver certeza sobre se um GPO no backup do arquivo morto é mais recente do que a cópia daquele GPO na produção, gere um relatório de diferença e compare as configurações.</span><span class="sxs-lookup"><span data-stu-id="e136b-117">If you not sure about whether a GPO in the archive backup is more current than the copy of that GPO in production, generate a difference report and compare their settings.</span></span> <span data-ttu-id="e136b-118">Para obter mais informações, consulte [identificar diferenças entre GPOs, versões de GPO ou modelos](identify-differences-between-gpos-gpo-versions-or-templates-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="e136b-118">For more information, see [Identify Differences Between GPOs, GPO Versions, or Templates](identify-differences-between-gpos-gpo-versions-or-templates-agpm30ops.md).</span></span>

6.  <span data-ttu-id="e136b-119">Reinicie o serviço do AGPM.</span><span class="sxs-lookup"><span data-stu-id="e136b-119">Restart the AGPM Service.</span></span> <span data-ttu-id="e136b-120">Para obter mais informações, consulte [Iniciar e interromper o serviço do AGPM](start-and-stop-the-agpm-service-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="e136b-120">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm30ops.md).</span></span>

### <span data-ttu-id="e136b-121">Referências adicionais</span><span class="sxs-lookup"><span data-stu-id="e136b-121">Additional references</span></span>

-   [<span data-ttu-id="e136b-122">Fazer backup do arquivo morto</span><span class="sxs-lookup"><span data-stu-id="e136b-122">Back Up the Archive</span></span>](back-up-the-archive.md)

-   [<span data-ttu-id="e136b-123">Mover o servidor e o arquivo morto do AGPM</span><span class="sxs-lookup"><span data-stu-id="e136b-123">Move the AGPM Server and the Archive</span></span>](move-the-agpm-server-and-the-archive.md)

-   [<span data-ttu-id="e136b-124">Gerenciamento do arquivo morto</span><span class="sxs-lookup"><span data-stu-id="e136b-124">Managing the Archive</span></span>](managing-the-archive.md)

 

 





