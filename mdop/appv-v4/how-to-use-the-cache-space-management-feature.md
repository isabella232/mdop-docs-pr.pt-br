---
title: Como Usar o Recurso de Gerenciamento de Espaço do Cache
description: Como Usar o Recurso de Gerenciamento de Espaço do Cache
author: dansimp
ms.assetid: 60965660-c015-46a8-88ac-54cbc050fe33
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fcb9cc4bc076e1acf52fb1c03797384c45b82f7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796919"
---
# <span data-ttu-id="20882-103">Como Usar o Recurso de Gerenciamento de Espaço do Cache</span><span class="sxs-lookup"><span data-stu-id="20882-103">How to Use the Cache Space Management Feature</span></span>


<span data-ttu-id="20882-104">O recurso de gerenciamento de espaço de cache do sistema de arquivos usa um algoritmo menos usado recentemente (LRU) e é habilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="20882-104">The FileSystem cache space management feature uses a Least Recently Used (LRU) algorithm and is enabled by default.</span></span> <span data-ttu-id="20882-105">Se o espaço necessário para um novo pacote ultrapassar o espaço livre disponível no cache, o cliente do Application Virtualization (App-V) usará esse recurso para determinar quais pacotes existentes podem ser excluídos do cache para liberar espaço para o novo pacote.</span><span class="sxs-lookup"><span data-stu-id="20882-105">If the space that is required for a new package would exceed the available free space in the cache, the Application Virtualization (App-V) Client uses this feature to determine which, if any, existing packages it can delete from the cache to make room for the new package.</span></span> <span data-ttu-id="20882-106">O cliente exclui o pacote com a data mais recente acessada se for anterior ao valor especificado no valor do registro MinPkgAge.</span><span class="sxs-lookup"><span data-stu-id="20882-106">The client deletes the package with the oldest last-accessed date if it is older than the value specified in the MinPkgAge registry value.</span></span> <span data-ttu-id="20882-107">O uso do recurso de gerenciamento de espaço de cache do sistema de arquivos também pode ajudar a evitar problemas de espaço em cache baixo.</span><span class="sxs-lookup"><span data-stu-id="20882-107">Use of the FileSystem cache space management feature can also help to avoid low cache space problems.</span></span>

<span data-ttu-id="20882-108">Mais de um pacote é excluído, se necessário.</span><span class="sxs-lookup"><span data-stu-id="20882-108">More than one package is deleted if necessary.</span></span> <span data-ttu-id="20882-109">Os pacotes que estiverem bloqueados não serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="20882-109">Packages that are locked are not deleted.</span></span>

<span data-ttu-id="20882-110">**Observação**  Para garantir que o cache tem espaço suficiente alocado para todos os pacotes que podem ser implantados, use a configuração **usar o limite de espaço em disco livre** ao configurar o cliente para que o cache possa crescer conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="20882-110">**Note** To ensure that the cache has sufficient space allocated for all packages that might be deployed, use the **Use free disk space threshold** setting when you configure the client so that the cache can grow as needed.</span></span> <span data-ttu-id="20882-111">Ou, se preferir, determine com antecedência quanto espaço em disco será necessário para o cache do App-V e, no momento da instalação, defina o tamanho do cache de acordo.</span><span class="sxs-lookup"><span data-stu-id="20882-111">Alternatively, determine in advance how much disk space will be needed for the App-V cache, and at installation time, set the cache size accordingly.</span></span>

 

<span data-ttu-id="20882-112">O recurso de gerenciamento de espaço em cache é controlado pelo valor do registro UnloadLeastRecentlyUsed.</span><span class="sxs-lookup"><span data-stu-id="20882-112">The cache space management feature is controlled by the UnloadLeastRecentlyUsed registry value.</span></span> <span data-ttu-id="20882-113">Um valor 1 habilita o recurso, e o valor 0 (zero) o desabilita.</span><span class="sxs-lookup"><span data-stu-id="20882-113">A value of 1 enables the feature, and a value of 0 (zero) disables it.</span></span>

**<span data-ttu-id="20882-114">Para habilitar ou desabilitar o recurso de gerenciamento de espaço do cache</span><span class="sxs-lookup"><span data-stu-id="20882-114">To enable or disable the cache space management feature</span></span>**

-   <span data-ttu-id="20882-115">Defina o valor de registro a seguir como 1 para habilitar o algoritmo LRU.</span><span class="sxs-lookup"><span data-stu-id="20882-115">Set the following registry value to 1 to enable the LRU algorithm.</span></span> <span data-ttu-id="20882-116">Defina-o como 0 (zero) para desabilitar o recurso.</span><span class="sxs-lookup"><span data-stu-id="20882-116">Set it to 0 (zero) to disable the feature.</span></span>

    <span data-ttu-id="20882-117">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\UnloadLeastRecentlyUsed</span><span class="sxs-lookup"><span data-stu-id="20882-117">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\UnloadLeastRecentlyUsed</span></span>

**<span data-ttu-id="20882-118">Para controlar quais pacotes podem ser descartados</span><span class="sxs-lookup"><span data-stu-id="20882-118">To control which packages can be discarded</span></span>**

-   <span data-ttu-id="20882-119">Para determinar quando o pacote pode ser selecionado para descartar, defina o valor do registro a seguir para igual ao número mínimo de dias que você deseja que decorra desde o último pacote ter sido acessado.</span><span class="sxs-lookup"><span data-stu-id="20882-119">To determine when the package can be selected for discard, set the following registry value to equal the minimum number of days you want to elapse since the package was last accessed.</span></span> <span data-ttu-id="20882-120">Os pacotes que foram usados mais recentemente não são descartados.</span><span class="sxs-lookup"><span data-stu-id="20882-120">Packages that have been used more recently are not discarded.</span></span>

    <span data-ttu-id="20882-121">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\MinPkgAge</span><span class="sxs-lookup"><span data-stu-id="20882-121">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\MinPkgAge</span></span>

    <span data-ttu-id="20882-122">**Cuidado**  O valor máximo para esta chave do registro é 0x00011111.</span><span class="sxs-lookup"><span data-stu-id="20882-122">**Caution** The maximum value for this registry key is 0x00011111.</span></span> <span data-ttu-id="20882-123">Valores maiores impedirão a operação correta do recurso de gerenciamento de espaço em cache.</span><span class="sxs-lookup"><span data-stu-id="20882-123">Larger values will prevent the correct operation of the cache space management feature.</span></span>

     

## <span data-ttu-id="20882-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="20882-124">Related topics</span></span>


[<span data-ttu-id="20882-125">Como definir as configurações de Registro do cliente do App-V usando a linha de comando</span><span class="sxs-lookup"><span data-stu-id="20882-125">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





