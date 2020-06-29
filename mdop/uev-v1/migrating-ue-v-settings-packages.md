---
title: Migrando pacotes de configurações do UE-V
description: Migrando pacotes de configurações do UE-V
author: dansimp
ms.assetid: 93d99254-3e17-4e96-92ad-87059d8554a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0087f334e916c06e7611d2671d0b50e7d1dd916
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799226"
---
# <span data-ttu-id="35036-103">Migrando pacotes de configurações do UE-V</span><span class="sxs-lookup"><span data-stu-id="35036-103">Migrating UE-V Settings Packages</span></span>


<span data-ttu-id="35036-104">No ciclo de vida de uma implantação do Microsoft User Experience Virtualization (UE-V), talvez seja necessário realocar os pacotes de configurações do usuário ao migrar para um novo servidor ou para fins de backup.</span><span class="sxs-lookup"><span data-stu-id="35036-104">In the lifecycle of a Microsoft User Experience Virtualization (UE-V) deployment, you might need to relocate the user settings packages either when migrating to a new server or for backup purposes.</span></span> <span data-ttu-id="35036-105">A migração de pacotes de configurações pode ser necessária nos seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="35036-105">Migration of settings packages might be needed in the following scenarios:</span></span>

-   <span data-ttu-id="35036-106">Atualização do hardware do servidor existente para um servidor mais moderno.</span><span class="sxs-lookup"><span data-stu-id="35036-106">Upgrade of existing server hardware to a more modern server.</span></span>

-   <span data-ttu-id="35036-107">Migração de um local de armazenamento de configurações compartilhar de um laboratório para um servidor de produção.</span><span class="sxs-lookup"><span data-stu-id="35036-107">Migration of a settings storage location share from a lab to a production server.</span></span>

<span data-ttu-id="35036-108">Basta copiar os arquivos e as pastas não preservará as permissões e as configurações de segurança.</span><span class="sxs-lookup"><span data-stu-id="35036-108">Simply copying the files and folders will not preserve the security settings and permissions.</span></span> <span data-ttu-id="35036-109">As etapas descritas a seguir copiarão corretamente os arquivos de pacote de configurações com suas permissões de NTFS para um novo compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="35036-109">The following described steps will properly copy the settings package files with their NTFS permissions to a new share.</span></span>

**<span data-ttu-id="35036-110">Como preservar pacotes de configurações do UE-V ao migrar para um novo servidor</span><span class="sxs-lookup"><span data-stu-id="35036-110">How to preserve UE-V settings packages when migrating to a new server</span></span>**

1.  <span data-ttu-id="35036-111">Em um novo local em um servidor diferente, crie uma nova pasta; por exemplo, MySettings.</span><span class="sxs-lookup"><span data-stu-id="35036-111">In a new location on a different server, create a new folder; for example, MySettings.</span></span>

2.  <span data-ttu-id="35036-112">Desabilite o compartilhamento para o compartilhamento de pasta antiga no servidor antigo.</span><span class="sxs-lookup"><span data-stu-id="35036-112">Disable sharing for the old folder share on the old server.</span></span>

3.  <span data-ttu-id="35036-113">Mova os pacotes de configurações existentes para o novo servidor com Robocopy na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="35036-113">Move the existing settings packages to the new server with Robocopy from the command line.</span></span> <span data-ttu-id="35036-114">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="35036-114">For example:</span></span>

    ``` syntax
    c:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    <span data-ttu-id="35036-115">**Observação**  Para monitorar o progresso da cópia, abra MySettings.txt com um leitor de arquivo de log, como Trace32.</span><span class="sxs-lookup"><span data-stu-id="35036-115">**Note** To monitor the copy progress, open MySettings.txt with a log file reader such as Trace32.</span></span>

     

4.  <span data-ttu-id="35036-116">Conceda permissões no nível do compartilhamento para o novo compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="35036-116">Grant share-level permissions to the new share.</span></span> <span data-ttu-id="35036-117">Deixe as permissões de NTFS como foram definidas pelo Robocopy.</span><span class="sxs-lookup"><span data-stu-id="35036-117">Leave the NTFS permissions as they were set by Robocopy.</span></span>

    <span data-ttu-id="35036-118">Em computadores que executam o UE-V Agent, atualize a configuração SettingsStoragePath para o caminho UNC do novo compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="35036-118">On computers that run the UE-V agent, update the SettingsStoragePath configuration setting to the UNC path of the new share.</span></span>

## <span data-ttu-id="35036-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="35036-119">Related topics</span></span>


[<span data-ttu-id="35036-120">Administração da UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="35036-120">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="35036-121">Operações para a UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="35036-121">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





