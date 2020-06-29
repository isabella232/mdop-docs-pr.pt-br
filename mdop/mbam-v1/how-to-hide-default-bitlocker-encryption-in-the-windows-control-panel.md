---
title: Como ocultar a criptografia BitLocker padrão no Painel de Controle do Windows
description: Como ocultar a criptografia BitLocker padrão no Painel de Controle do Windows
author: dansimp
ms.assetid: c8503743-220c-497c-9785-e2feeca484d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67a61763e556f8c3b93825220dbbd61a14b7d6f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799486"
---
# <span data-ttu-id="8f579-103">Como ocultar a criptografia BitLocker padrão no Painel de Controle do Windows</span><span class="sxs-lookup"><span data-stu-id="8f579-103">How to Hide Default BitLocker Encryption in The Windows Control Panel</span></span>


<span data-ttu-id="8f579-104">O monitoramento e administração do Microsoft BitLocker (MBAM) oferece um painel de controle personalizado para computadores cliente MBAM nomeados como opções de criptografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8f579-104">Microsoft BitLocker Administration and Monitoring (MBAM) offers a customized control panel for MBAM client computers that is named called BitLocker Encryption Options.</span></span> <span data-ttu-id="8f579-105">Este painel de controle personalizado pode substituir o painel de controle padrão do Windows BitLocker chamado de criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8f579-105">This customized control panel can replace the default Windows BitLocker control panel that is named BitLocker Drive Encryption.</span></span> <span data-ttu-id="8f579-106">O painel de controle opções de criptografia do BitLocker, localizado em sistema e segurança, no painel de controle do Windows, permite que os usuários gerenciem seu PIN e senhas, desbloqueiem unidades e ocultem a interface que permite que os administradores descriptografem uma unidade ou suspendam ou retomem a criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8f579-106">The BitLocker Encryption Options control panel, located under System and Security in the Windows control panel, enables users to manage their PIN and passwords, unlock drives, and hides the interface that allows administrators to decrypt a drive or to suspend or resume BitLocker encryption.</span></span>

**<span data-ttu-id="8f579-107">Para ocultar a criptografia do BitLocker padrão no painel de controle do Windows</span><span class="sxs-lookup"><span data-stu-id="8f579-107">To hide default BitLocker Encryption in the Windows Control Panel</span></span>**

1.  <span data-ttu-id="8f579-108">Navegue até **configuração do usuário** usando o GPMC (console de gerenciamento de política de grupo), o gerenciamento avançado de política de grupo (AGPM) ou o editor de política de grupo local no computador de políticas de grupo do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8f579-108">Browse to **User configuration** by using the Group Policy Management Console (GPMC), the Advanced Group Policy Management (AGPM), or the Local Group Policy Editor on the BitLocker Group Policies computer.</span></span>

2.  <span data-ttu-id="8f579-109">Clique em **políticas**, selecione **modelos administrativos**e, em seguida, clique em **painel de controle**.</span><span class="sxs-lookup"><span data-stu-id="8f579-109">Click **Policies**, select **Administrative Templates**, and then click **Control Panel**.</span></span>

3.  <span data-ttu-id="8f579-110">No painel **detalhes** , clique duas vezes em **ocultar itens do painel de controle especificado**e selecione **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="8f579-110">In the **Details** pane, double-click **Hide specified Control Panel items**, and then select **Enabled**.</span></span>

4.  <span data-ttu-id="8f579-111">Clique em **Mostrar**, **clique em Adicionar...** e digite Microsoft. BitLockerDriveEncryption.</span><span class="sxs-lookup"><span data-stu-id="8f579-111">Click **Show**, **click Add…**, and then type Microsoft.BitLockerDriveEncryption.</span></span> <span data-ttu-id="8f579-112">Essa política oculta a ferramenta de gerenciamento do Windows BitLocker padrão do painel de controle do Windows e permite ao usuário abrir a ferramenta de opções de criptografia do BitLocker MBAM atualizada a partir do painel de controle do Windows.</span><span class="sxs-lookup"><span data-stu-id="8f579-112">This policy hides the default Windows BitLocker Management tool from the Windows Control Panel and allows the user to open the updated MBAM BitLocker Encryption Options tool from the Windows Control Panel.</span></span>

## <span data-ttu-id="8f579-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8f579-113">Related topics</span></span>


[<span data-ttu-id="8f579-114">Implantar Objetos de Política de Grupo no MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="8f579-114">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)

 

 





