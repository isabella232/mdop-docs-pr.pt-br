---
title: Como ocultar a criptografia BitLocker padrão no Painel de Controle do Windows
description: Como ocultar a criptografia BitLocker padrão no Painel de Controle do Windows
author: dansimp
ms.assetid: 6674aa51-2b5d-4e4a-8b43-2cc18d008285
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eda8fafbd7b3ebf414520354eba6def2e97f6237
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799401"
---
# <span data-ttu-id="40aea-103">Como ocultar a criptografia BitLocker padrão no Painel de Controle do Windows</span><span class="sxs-lookup"><span data-stu-id="40aea-103">How to Hide Default BitLocker Encryption in the Windows Control Panel</span></span>


<span data-ttu-id="40aea-104">O monitoramento e administração do Microsoft BitLocker (MBAM) oferece um painel de controle personalizado para os computadores cliente de administração e monitoramento do Microsoft BitLocker, chamados opções de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="40aea-104">Microsoft BitLocker Administration and Monitoring (MBAM) offers a customized control panel for Microsoft BitLocker Administration and Monitoring client computers, called BitLocker Encryption Options.</span></span> <span data-ttu-id="40aea-105">Este painel de controle personalizado pode substituir o painel de controle padrão do Windows BitLocker, que é chamado de criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="40aea-105">This customized control panel can replace the default Windows BitLocker control panel, which is called BitLocker Drive Encryption.</span></span> <span data-ttu-id="40aea-106">O painel de controle personalizado, que está no painel de controle, em sistema e segurança, permite que os usuários gerenciem seu PIN e senhas e desbloqueiem unidades e ocultam a interface que permite que os administradores descriptografem uma unidade ou suspendam ou retomem a criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="40aea-106">The customized control panel, which is in Control Panel under System and Security, enables users to manage their PIN and passwords and to unlock drives, and hides the interface that enables administrators to decrypt a drive or to suspend or resume BitLocker drive encryption.</span></span>

**<span data-ttu-id="40aea-107">Para ocultar a criptografia de unidade de disco BitLocker padrão no painel de controle do Windows</span><span class="sxs-lookup"><span data-stu-id="40aea-107">To hide default BitLocker drive encryption in Windows Control Panel</span></span>**

1.  <span data-ttu-id="40aea-108">No GPMC (console de gerenciamento de política de grupo), no gerenciamento avançado de política de grupo (AGPM) ou no editor de política de grupo local no computador de políticas de grupo do BitLocker, navegue até **configuração do usuário**.</span><span class="sxs-lookup"><span data-stu-id="40aea-108">In the Group Policy Management Console (GPMC), the Advanced Group Policy Management (AGPM), or the Local Group Policy Editor on the BitLocker Group Policies computer, browse to **User configuration**.</span></span>

2.  <span data-ttu-id="40aea-109">Em seguida, clique em **políticas**, selecione **modelos administrativos**e, em seguida, clique em **painel de controle**.</span><span class="sxs-lookup"><span data-stu-id="40aea-109">Next, click **Policies**, select **Administrative Templates**, and then click **Control Panel**.</span></span>

3.  <span data-ttu-id="40aea-110">Clique duas vezes em **ocultar itens do painel de controle especificado** no painel **detalhes** e selecione **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="40aea-110">Double-click **Hide specified Control Panel items** in the **Details** pane, and then select **Enabled**.</span></span>

4.  <span data-ttu-id="40aea-111">Clique em **Mostrar**, clique em **Adicionar**e, em seguida, digite **Microsoft. BitLockerDriveEncryption**.</span><span class="sxs-lookup"><span data-stu-id="40aea-111">Click **Show**, click **Add**, and then type **Microsoft.BitLockerDriveEncryption**.</span></span> <span data-ttu-id="40aea-112">Essa política oculta a ferramenta de gerenciamento do Windows BitLocker padrão no painel de controle do Windows e, no painel de controle, permite ao usuário abrir a ferramenta de opções de criptografia do BitLocker MBAM atualizada em sistema e segurança.</span><span class="sxs-lookup"><span data-stu-id="40aea-112">This policy hides the default Windows BitLocker Management tool from the Windows Control Panel and, in Control Panel, lets the user open the updated MBAM BitLocker Encryption Options tool under System and Security.</span></span>

## <span data-ttu-id="40aea-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="40aea-113">Related topics</span></span>


[<span data-ttu-id="40aea-114">Implantar Objetos de Política de Grupo no MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="40aea-114">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





