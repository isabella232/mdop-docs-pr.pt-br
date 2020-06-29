---
title: Migrando pacotes de configurações do UE-V 2. x
description: Migrando pacotes de configurações do UE-V 2. x
author: dansimp
ms.assetid: f79381f4-e142-405c-b728-5c048502aa70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0aa1f1c36594d69de40306dfa70a4a0cf5c86dbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799688"
---
# <span data-ttu-id="1b76f-103">Migrando pacotes de configurações do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="1b76f-103">Migrating UE-V 2.x Settings Packages</span></span>


<span data-ttu-id="1b76f-104">No ciclo de vida de uma implantação do Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 ou 2,1 SP1, talvez seja necessário realocar os pacotes de configurações do usuário quando migrar para um novo servidor ou quando executar backups.</span><span class="sxs-lookup"><span data-stu-id="1b76f-104">In the lifecycle of a Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 deployment, you might have to relocate the user settings packages either when you migrate to a new server or when you perform backups.</span></span> <span data-ttu-id="1b76f-105">Os pacotes de configurações podem precisar ser migrados nos seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="1b76f-105">Settings packages might have to be migrated in the following scenarios:</span></span>

-   <span data-ttu-id="1b76f-106">Atualização do hardware do servidor existente para um servidor mais moderno.</span><span class="sxs-lookup"><span data-stu-id="1b76f-106">Upgrade of existing server hardware to a more modern server.</span></span>

-   <span data-ttu-id="1b76f-107">Migração de um local de armazenamento de configurações compartilhar de um servidor de teste para um servidor de produção.</span><span class="sxs-lookup"><span data-stu-id="1b76f-107">Migration of a settings storage location share from a test server to a production server.</span></span>

<span data-ttu-id="1b76f-108">Simplesmente copiar os arquivos e pastas não preserva as permissões e as configurações de segurança.</span><span class="sxs-lookup"><span data-stu-id="1b76f-108">Simply copying the files and folders does not preserve the security settings and permissions.</span></span> <span data-ttu-id="1b76f-109">As etapas a seguir descrevem como copiar corretamente o pacote de configurações juntamente com as permissões do sistema de arquivos NTFS para um novo compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="1b76f-109">The following steps describe how to correctly copy the settings package along with their NTFS file system permissions to a new share.</span></span>

**<span data-ttu-id="1b76f-110">Para preservar pacotes de configurações do UE-V 2 ao migrar para um novo servidor</span><span class="sxs-lookup"><span data-stu-id="1b76f-110">To preserve UE-V 2 settings packages when you migrate to a new server</span></span>**

1.  <span data-ttu-id="1b76f-111">Em um novo local em um servidor diferente, crie uma nova pasta, por exemplo, MySettings.</span><span class="sxs-lookup"><span data-stu-id="1b76f-111">In a new location on a different server, create a new folder, for example, MySettings.</span></span>

2.  <span data-ttu-id="1b76f-112">Desabilite o compartilhamento para o compartilhamento de pasta antiga no servidor antigo.</span><span class="sxs-lookup"><span data-stu-id="1b76f-112">Disable sharing for the old folder share on the old server.</span></span>

3.  <span data-ttu-id="1b76f-113">Para copiar os pacotes de configurações existentes para o novo servidor com Robocopy</span><span class="sxs-lookup"><span data-stu-id="1b76f-113">To copy the existing settings packages to the new server with Robocopy</span></span>

    ``` syntax
    C:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    <span data-ttu-id="1b76f-114">**Observação**  Para monitorar o progresso da cópia, abra MySettings.txt com um visualizador de log, como Trace32.</span><span class="sxs-lookup"><span data-stu-id="1b76f-114">**Note** To monitor the copy progress, open MySettings.txt with a log viewer such as Trace32.</span></span>

     

4.  <span data-ttu-id="1b76f-115">Conceda permissões no nível do compartilhamento para o novo compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="1b76f-115">Grant share-level permissions to the new share.</span></span> <span data-ttu-id="1b76f-116">Deixe as permissões do sistema de arquivos NTFS como foram definidas pelo Robocopy.</span><span class="sxs-lookup"><span data-stu-id="1b76f-116">Leave the NTFS file system permissions as they were set by Robocopy.</span></span>

    <span data-ttu-id="1b76f-117">Em computadores que executam o UE-V Agent, atualize a configuração **SettingsStoragePath** para o caminho da Convenção Universal de nomenclatura (UNC) do novo compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="1b76f-117">On computers that run the UE-V Agent, update the **SettingsStoragePath** configuration setting to the Universal Naming Convention (UNC) path of the new share.</span></span>

    <span data-ttu-id="1b76f-118">**Tem uma sugestão para UE-V**?</span><span class="sxs-lookup"><span data-stu-id="1b76f-118">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="1b76f-119">Adicione ou vote em sugestões [aqui](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span><span class="sxs-lookup"><span data-stu-id="1b76f-119">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="1b76f-120">**Tem um problema de UE-V**?</span><span class="sxs-lookup"><span data-stu-id="1b76f-120">**Got a UE-V issue**?</span></span> <span data-ttu-id="1b76f-121">Use o [Fórum do TechNet para UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span><span class="sxs-lookup"><span data-stu-id="1b76f-121">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <span data-ttu-id="1b76f-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b76f-122">Related topics</span></span>


[<span data-ttu-id="1b76f-123">Administração do UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="1b76f-123">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

 

 





