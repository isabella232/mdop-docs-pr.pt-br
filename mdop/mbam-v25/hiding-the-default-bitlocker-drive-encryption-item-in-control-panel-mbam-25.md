---
title: Ocultando o item de Criptografia de Unidade de Disco BitLocker padrão no Painel de Controle
description: Ocultando o item de Criptografia de Unidade de Disco BitLocker padrão no Painel de Controle
author: dansimp
ms.assetid: 6e2a9a02-a809-43a1-80a3-1b03c7192c89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af395928ca8934bfea4eeb848bbd4ee377987293
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799204"
---
# <span data-ttu-id="339b0-103">Ocultando o item de Criptografia de Unidade de Disco BitLocker padrão no Painel de Controle</span><span class="sxs-lookup"><span data-stu-id="339b0-103">Hiding the Default BitLocker Drive Encryption Item in Control Panel</span></span>


<span data-ttu-id="339b0-104">Este tópico descreve como ocultar o item do painel de controle de **criptografia de unidade de disco BitLocker** , que é exibido por padrão no painel de controle como parte do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="339b0-104">This topic describes how to hide the **BitLocker Drive Encryption** Control Panel item, which appears by default on Control Panel as part of the Windows operating system.</span></span>

<span data-ttu-id="339b0-105">**Observação**  O Microsoft BitLocker Administration and Monitoring (MBAM) cria um item de painel de controle adicional personalizado, chamado **Opções de criptografia do BitLocker**, que permite que os usuários finais gerenciem o PIN e a senha, ativem o BitLocker para uma unidade e marquem a criptografia.</span><span class="sxs-lookup"><span data-stu-id="339b0-105">**Note** Microsoft BitLocker Administration and Monitoring (MBAM) creates an additional, custom Control Panel item, called **BitLocker Encryption Options**, which enables end users to manage their PIN and password, turn on BitLocker for a drive, and check encryption.</span></span>

 

<span data-ttu-id="339b0-106">Consulte [compreendendo as opções de criptografia BitLocker e os itens de criptografia de unidade de disco BitLocker no painel de controle](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md) para ler sobre:</span><span class="sxs-lookup"><span data-stu-id="339b0-106">See [Understanding the BitLocker Encryption Options and BitLocker Drive Encryption Items in Control Panel](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md) to read about:</span></span>

-   <span data-ttu-id="339b0-107">Diferenças entre o MBAM e os itens padrão do painel de controle</span><span class="sxs-lookup"><span data-stu-id="339b0-107">Differences between the MBAM and the default Control Panel items</span></span>

-   <span data-ttu-id="339b0-108">Menu de atalho **gerenciar o BitLocker** que aparece quando você clica com o botão direito do mouse em uma unidade no Windows Explorer</span><span class="sxs-lookup"><span data-stu-id="339b0-108">**Manage BitLocker** shortcut menu that appears when you right-click a drive in Windows Explorer</span></span>

<span data-ttu-id="339b0-109">**Importante**  Não altere as configurações de política de grupo no nó **criptografia de unidade de disco BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="339b0-109">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node.</span></span> <span data-ttu-id="339b0-110">Se fizer isso, o MBAM não funcionará corretamente.</span><span class="sxs-lookup"><span data-stu-id="339b0-110">If you do, MBAM will not work correctly.</span></span> <span data-ttu-id="339b0-111">Ao definir as configurações de política de grupo no nó **MDOP MBAM (gerenciamento de BitLocker)** , o MBAM configura automaticamente as configurações de **criptografia de unidade de disco BitLocker** para você.</span><span class="sxs-lookup"><span data-stu-id="339b0-111">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>

 

**<span data-ttu-id="339b0-112">Para ocultar o item de criptografia de unidade de disco BitLocker padrão no painel de controle</span><span class="sxs-lookup"><span data-stu-id="339b0-112">To hide the default BitLocker Drive Encryption item in Control Panel</span></span>**

1.  <span data-ttu-id="339b0-113">No console de gerenciamento de política de grupo (GPMC) ou no gerenciamento avançado de política de grupo, navegue até políticas de **configuração do usuário** &gt; **Policies** &gt; painel de controle de **modelos administrativos** &gt; **Control Panel**.</span><span class="sxs-lookup"><span data-stu-id="339b0-113">In the Group Policy Management Console (GPMC) or in Advanced Group Policy Management, browse to **User configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Control Panel**.</span></span>

2.  <span data-ttu-id="339b0-114">No painel **detalhes** , clique duas vezes em **ocultar itens do painel de controle especificado**e, em seguida, clique em **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="339b0-114">In the **Details** pane, double-click **Hide specified Control Panel items**, and then click **Enabled**.</span></span>

3.  <span data-ttu-id="339b0-115">Clique em **Mostrar**, clique em **Adicionar**e, em seguida, digite **Microsoft. BitLockerDriveEncryption**.</span><span class="sxs-lookup"><span data-stu-id="339b0-115">Click **Show**, click **Add**, and then type **Microsoft.BitLockerDriveEncryption**.</span></span>



## <span data-ttu-id="339b0-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="339b0-116">Related topics</span></span>


[<span data-ttu-id="339b0-117">Noções básicas sobre as opções de criptografia BitLocker e itens de Criptografia de Unidade de Disco BitLocker no Painel de Controle</span><span class="sxs-lookup"><span data-stu-id="339b0-117">Understanding the BitLocker Encryption Options and BitLocker Drive Encryption Items in Control Panel</span></span>](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md)

[<span data-ttu-id="339b0-118">Implantando objetos de Política de Grupo do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="339b0-118">Deploying MBAM 2.5 Group Policy Objects</span></span>](deploying-mbam-25-group-policy-objects.md)

 

## <span data-ttu-id="339b0-119">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="339b0-119">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="339b0-120">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="339b0-120">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="339b0-121">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="339b0-121">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





