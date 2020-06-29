---
title: Gerenciar impressoras em uma área de trabalho da MED-V
description: Gerenciar impressoras em uma área de trabalho da MED-V
author: dansimp
ms.assetid: ba0a65ad-444f-4d18-95eb-8b9fa1a3ffba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bc7a62075c95e8816a425eff89ffb992f1185d04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799808"
---
# <span data-ttu-id="9f505-103">Gerenciar impressoras em uma área de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="9f505-103">Managing Printers on a MED-V Workspace</span></span>


<span data-ttu-id="9f505-104">Na virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0, o redirecionamento de impressoras fornece aos usuários finais uma experiência de impressão consistente entre a máquina virtual do MED-V e o computador host.</span><span class="sxs-lookup"><span data-stu-id="9f505-104">In Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, printer redirection provides end users with a consistent printing experience between the MED-V virtual machine and the host computer.</span></span>

<span data-ttu-id="9f505-105">Este tópico fornece informações sobre como gerenciar a impressão em um espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="9f505-105">This topic provides information about how to manage printing in a MED-V workspace.</span></span>

## <span data-ttu-id="9f505-106">Gerenciando impressoras em espaços de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="9f505-106">Managing Printers in MED-V Workspaces</span></span>


<span data-ttu-id="9f505-107">Na maioria dos casos, o MED-V manipula o redirecionamento da impressora automaticamente.</span><span class="sxs-lookup"><span data-stu-id="9f505-107">In most cases, MED-V handles printer redirection automatically.</span></span> <span data-ttu-id="9f505-108">Após o término da primeira vez, o MED-V identifica todas as impressoras de rede instaladas no host, recupera os drivers correspondentes do servidor de impressão de rede e, se encontrado, instala os drivers relevantes no espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="9f505-108">After first time setup finishes, MED-V identifies all network printers installed on the host, retrieves the corresponding drivers from the network print server, and if found, installs the relevant drivers in the MED-V workspace.</span></span> <span data-ttu-id="9f505-109">Depois que todos os drivers forem encontrados e instalados, o MED-V reinicializará o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="9f505-109">After all drivers are found and installed, MED-V reboots the MED-V workspace.</span></span> <span data-ttu-id="9f505-110">Somente após a reinicialização do espaço de trabalho do MED-V, as impressoras do host estão presentes e estão disponíveis no convidado, em alguns minutos.</span><span class="sxs-lookup"><span data-stu-id="9f505-110">Only after the MED-V workspace restarts, the host printers are present and available on the guest, typically in a few minutes.</span></span>

<span data-ttu-id="9f505-111">**Observação**  Se os aplicativos estiverem sendo executados no espaço de trabalho do MED-V, o usuário final será solicitado a permitir que o reinício continue ou adie-o até mais tarde.</span><span class="sxs-lookup"><span data-stu-id="9f505-111">**Note** If applications are running on the MED-V workspace, the end user is prompted to let the restart continue or postpone it until later.</span></span> <span data-ttu-id="9f505-112">Se nenhum aplicativo estiver sendo executado, a reinicialização será automática e não será exibida para o usuário final.</span><span class="sxs-lookup"><span data-stu-id="9f505-112">If no applications are running, the restart is automatic and not shown to the end user.</span></span>

 

<span data-ttu-id="9f505-113">Sempre que o MED-V é reiniciado, ele verifica se há novas impressoras instaladas no host e, se encontradas, recupera os drivers correspondentes do servidor de impressão de rede e os instala no convidado.</span><span class="sxs-lookup"><span data-stu-id="9f505-113">Every time MED-V is re-started, it checks whether any new printers are installed on the host and, if found, retrieves the corresponding drivers from the network print server and installs them on the guest.</span></span> <span data-ttu-id="9f505-114">Em seguida, o MED-V reinicia o espaço de trabalho do MED-V da mesma forma que quando a configuração foi concluída pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="9f505-114">MED-V then restarts the MED-V workspace just as when first time setup was completed.</span></span>

<span data-ttu-id="9f505-115">**Importante**  Após a instalação dos drivers relevantes no convidado, as impressoras só se tornam visíveis no convidado após a reinicialização.</span><span class="sxs-lookup"><span data-stu-id="9f505-115">**Important** After the relevant drivers are installed on the guest, the printers only become visible on the guest after the restart occurs.</span></span>

 

<span data-ttu-id="9f505-116">Se, a qualquer momento, não for possível localizar ou instalar um driver, ele deve ser instalado manualmente no convidado para que a impressora de rede esteja disponível para o usuário final.</span><span class="sxs-lookup"><span data-stu-id="9f505-116">If at any time a driver cannot be located or installed, it must be manually installed on the guest for the network printer to be available to the end user.</span></span>

<span data-ttu-id="9f505-117">A lista a seguir oferece algumas orientações adicionais:</span><span class="sxs-lookup"><span data-stu-id="9f505-117">The following list offers some additional guidance:</span></span>

<span data-ttu-id="9f505-118">O **MED-V gerencia apenas impressoras de rede**.</span><span class="sxs-lookup"><span data-stu-id="9f505-118">**MED-V only manages network printers**.</span></span> <span data-ttu-id="9f505-119">Os drivers para impressoras instaladas localmente no host não são instalados automaticamente no convidado.</span><span class="sxs-lookup"><span data-stu-id="9f505-119">Drivers for printers that are installed locally on the host are not automatically installed on the guest.</span></span>

<span data-ttu-id="9f505-120">**O MED-V instala somente drivers de impressora, se encontrados no servidor de impressão**.</span><span class="sxs-lookup"><span data-stu-id="9f505-120">**MED-V only installs printer drivers if found on the print server**.</span></span> <span data-ttu-id="9f505-121">Se não for encontrado, os drivers da impressora deverão ser instalados manualmente.</span><span class="sxs-lookup"><span data-stu-id="9f505-121">If not found, printer drivers must be manually installed.</span></span>

<span data-ttu-id="9f505-122">**As impressoras instaladas manualmente no convidado não estão acessíveis para o host**.</span><span class="sxs-lookup"><span data-stu-id="9f505-122">**Printers manually installed on the guest are not accessible to the host**.</span></span> <span data-ttu-id="9f505-123">Por padrão, o MED-V aceita apenas o redirecionamento de impressoras do convidado para o host.</span><span class="sxs-lookup"><span data-stu-id="9f505-123">By default, MED-V only supports printer redirection from the guest to the host.</span></span>

<span data-ttu-id="9f505-124">**Aviso**  Se uma impressora é instalada manualmente no convidado e a mesma impressora é instalada posteriormente no host, o resultado é que a impressora é instalada duas vezes no convidado.</span><span class="sxs-lookup"><span data-stu-id="9f505-124">**Warning** If a printer is manually installed on the guest, and the same printer is later installed on the host, the result is that the printer is installed two times in the guest.</span></span> <span data-ttu-id="9f505-125">Para evitar essa situação, uma prática recomendada do MED-V é gerenciar o redirecionamento de impressora apenas de uma maneira: desabilite o redirecionamento e instale as impressoras manualmente no convidado ou habilite o redirecionamento e não instale impressoras manualmente no convidado.</span><span class="sxs-lookup"><span data-stu-id="9f505-125">To avoid this situation, a MED-V best practice is to manage printer redirection in one manner only: either disable redirection and install printers manually on the guest, or enable redirection and do not install printers manually on the guest.</span></span>

 

## <span data-ttu-id="9f505-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9f505-126">Related topics</span></span>


[<span data-ttu-id="9f505-127">Gerenciar configurações de espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="9f505-127">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





