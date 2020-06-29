---
title: Atualização da MED-V 2.0
description: Atualização da MED-V 2.0
author: dansimp
ms.assetid: beea2f54-42d7-4a17-98e0-d243a8562265
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 62e8987ec511783422b8dd336dd4f3be2008c9b2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799331"
---
# <span data-ttu-id="005ab-103">Atualização da MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="005ab-103">Updating MED-V 2.0</span></span>


<span data-ttu-id="005ab-104">Ajude a proteger seu sistema aplicando as atualizações de segurança apropriadas para o Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="005ab-104">Help secure your system by applying the appropriate security updates for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="005ab-105">Atualização do MED-V</span><span class="sxs-lookup"><span data-stu-id="005ab-105">Updating MED-V</span></span>


<span data-ttu-id="005ab-106">Você pode atualizar o MED-V interativamente, pelo usuário final ou silenciosamente, usando um sistema de distribuição de software eletrônico.</span><span class="sxs-lookup"><span data-stu-id="005ab-106">You can update MED-V interactively, by the end user, or silently by using an electronic software distribution system.</span></span> <span data-ttu-id="005ab-107">A instalação do agente de host MED-V atualiza o host do MED-V Host Agent e, em seguida, atualiza o espaço de trabalho do MED-v, se necessário.</span><span class="sxs-lookup"><span data-stu-id="005ab-107">Installation of the MED-V Host Agent upgrades the MED-V Host Agent and then updates the MED-V workspace if required.</span></span> <span data-ttu-id="005ab-108">O agente de host do MED-V e o agente convidado mantêm-se sincronizados. Se os aplicativos estiverem sendo executados do espaço de trabalho do MED-V enquanto o agente de host do MED-V estiver sendo atualizado, será necessário reiniciar o computador host para concluir a atualização.</span><span class="sxs-lookup"><span data-stu-id="005ab-108">The MED-V Host Agent and Guest Agent keep in sync. If applications are running from the MED-V workspace while the MED-V Host Agent is being updated, a restart of the host computer is required to complete the update.</span></span> <span data-ttu-id="005ab-109">Se nenhum aplicativo estiver sendo executado, o MED-V será reiniciado automaticamente e a atualização será concluída sem a reinicialização do computador host.</span><span class="sxs-lookup"><span data-stu-id="005ab-109">If no applications are running, MED-V is restarted automatically and the upgrade is completed without a restart of the host computer.</span></span>

<span data-ttu-id="005ab-110">Se estiver atualizando o MED-V usando um sistema de distribuição de software eletrônico, você pode controlar o comportamento de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="005ab-110">If you are updating MED-V by using an electronic software distribution system, you can control the restart behavior.</span></span> <span data-ttu-id="005ab-111">Para fazer isso, omita a reinicialização digitando **reboot = "ReallySuppress"** no prompt de comando ao instalar MED-V\_HostAgent\_Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="005ab-111">To do this, suppress the restart by typing **REBOOT=”ReallySuppress”** at the command prompt when installing MED-V\_HostAgent\_Setup.exe.</span></span> <span data-ttu-id="005ab-112">Em seguida, configure o sistema de distribuição de software eletrônico para capturar o código de retorno do 3010 (que sinaliza que uma reinicialização é necessária) e executar o comportamento definir reinicialização.</span><span class="sxs-lookup"><span data-stu-id="005ab-112">Then, configure the electronic software distribution system to capture the 3010 return code (which signals that a restart is required) and perform the set restart behavior.</span></span>

## <span data-ttu-id="005ab-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="005ab-113">Related topics</span></span>


[<span data-ttu-id="005ab-114">Referência técnica da MED-V</span><span class="sxs-lookup"><span data-stu-id="005ab-114">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

 

 





