---
title: Como gerenciar opções de criptografia BitLocker do Cliente do MBAM utilizando o Painel de Controle
description: Como gerenciar opções de criptografia BitLocker do Cliente do MBAM utilizando o Painel de Controle
author: dansimp
ms.assetid: c08077e1-5529-468f-9370-c3b33fc258f3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 271147d0e5581f6ce49fe0b46aa83dae6ae4556b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796129"
---
# <span data-ttu-id="9aeb6-103">Como gerenciar opções de criptografia BitLocker do Cliente do MBAM utilizando o Painel de Controle</span><span class="sxs-lookup"><span data-stu-id="9aeb6-103">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>


<span data-ttu-id="9aeb6-104">Um aplicativo do painel de controle de administração e monitoramento do Microsoft BitLocker (MBAM), chamado de opções de criptografia do BitLocker, estará disponível em **sistema e segurança** quando o cliente MBAM estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="9aeb6-104">A Microsoft BitLocker Administration and Monitoring (MBAM) control panel application, called BitLocker Encryption Options, will be available under **System and Security** when the MBAM Client is installed.</span></span> <span data-ttu-id="9aeb6-105">Este painel de controle MBAM personalizado substitui o painel de controle padrão do Windows BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9aeb6-105">This customized MBAM control panel replaces the default Windows BitLocker control panel.</span></span> <span data-ttu-id="9aeb6-106">O painel de controle do MBAM permite desbloquear unidades criptografadas (fixas e removíveis) e também ajuda você a gerenciar seu PIN ou senha.</span><span class="sxs-lookup"><span data-stu-id="9aeb6-106">The MBAM control panel enables you to unlock encrypted drives (fixed and removable), and also helps you manage your PIN or password.</span></span> <span data-ttu-id="9aeb6-107">Para obter mais informações sobre como habilitar o painel de controle do MBAM, consulte [como ocultar a criptografia do BitLocker padrão no painel de controle do Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md).</span><span class="sxs-lookup"><span data-stu-id="9aeb6-107">For more information about enabling the MBAM control panel, see [How to Hide Default BitLocker Encryption in The Windows Control Panel](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md).</span></span>

<span data-ttu-id="9aeb6-108">**Observação**  Para o cliente BitLocker, o administrador e os arquivos de log operacional estão localizados no Visualizador de eventos, em **logs de aplicativos e serviços**  /  **Microsoft**  /  **Windows**  /  **BitLockerManagement**.</span><span class="sxs-lookup"><span data-stu-id="9aeb6-108">**Note** For the BitLocker client, the Admin and Operational log files are located in Event Viewer, under **Application and Services Logs** / **Microsoft** / **Windows** / **BitLockerManagement**.</span></span>

 

**<span data-ttu-id="9aeb6-109">Para usar o painel de controle do cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="9aeb6-109">To use the MBAM Client Control Panel</span></span>**

1.  <span data-ttu-id="9aeb6-110">Para abrir as opções de criptografia do BitLocker, clique em **Iniciar**e, em seguida, selecione **painel de controle**.</span><span class="sxs-lookup"><span data-stu-id="9aeb6-110">To open BitLocker Encryption Options, click **Start**, and then select **Control Panel**.</span></span> <span data-ttu-id="9aeb6-111">Quando o **painel de controle** for aberto, selecione **sistema e segurança**.</span><span class="sxs-lookup"><span data-stu-id="9aeb6-111">When **Control Panel** opens, select **System and Security**.</span></span>

2.  <span data-ttu-id="9aeb6-112">Clique duas vezes em **Opções de criptografia do BitLocker** para abrir o painel de controle MBAM personalizado.</span><span class="sxs-lookup"><span data-stu-id="9aeb6-112">Double-click **BitLocker Encryption Options** to open the customized MBAM control panel.</span></span> <span data-ttu-id="9aeb6-113">Você verá uma lista de todas as unidades de disco rígido no computador e seu status de criptografia.</span><span class="sxs-lookup"><span data-stu-id="9aeb6-113">You will see a list of all the hard disk drives on the computer and their encryption status.</span></span> <span data-ttu-id="9aeb6-114">Você também poderá ver uma opção para gerenciar seu PIN ou senhas.</span><span class="sxs-lookup"><span data-stu-id="9aeb6-114">You will also see an option to manage your PIN or passwords.</span></span>

3.  <span data-ttu-id="9aeb6-115">Use a lista de unidades de disco rígido no computador para verificar o status de criptografia, desbloquear uma unidade ou solicitar uma isenção de proteção do BitLocker se as políticas de isenção de usuário e computador tiverem sido implantadas.</span><span class="sxs-lookup"><span data-stu-id="9aeb6-115">Use the list of hard disk drives on the computer to verify the encryption status, unlock a drive, or request an exemption for BitLocker protection if the User and Computer Exemption policies have been deployed.</span></span>

4.  <span data-ttu-id="9aeb6-116">Usuários que não são administradores podem usar o painel de controle opções de criptografia BitLocker para gerenciar PINs ou senhas.</span><span class="sxs-lookup"><span data-stu-id="9aeb6-116">Non-administrators can use the BitLocker Encryption Options control panel to manage PINs or passwords.</span></span> <span data-ttu-id="9aeb6-117">Um usuário pode selecionar **gerenciar PIN** e, em seguida, inserir um PIN atual e um novo PIN.</span><span class="sxs-lookup"><span data-stu-id="9aeb6-117">A user can select **Manage PIN,** and then enter both a current PIN and a new PIN.</span></span> <span data-ttu-id="9aeb6-118">Os usuários também podem confirmar o novo PIN.</span><span class="sxs-lookup"><span data-stu-id="9aeb6-118">Users can also confirm their new PIN.</span></span> <span data-ttu-id="9aeb6-119">A função **Atualizar PIN** irá redefinir o pino para o novo que o usuário selecionar.</span><span class="sxs-lookup"><span data-stu-id="9aeb6-119">The **Update PIN** function will reset the PIN to the new one that the user selects.</span></span>

5.  <span data-ttu-id="9aeb6-120">Para gerenciar sua senha, selecione **desbloquear unidade** e insira sua senha atual.</span><span class="sxs-lookup"><span data-stu-id="9aeb6-120">To manage your password, select **Unlock drive** and enter your current password.</span></span> <span data-ttu-id="9aeb6-121">Assim que a unidade for desbloqueada, selecione **Redefinir senha** para alterar sua senha atual.</span><span class="sxs-lookup"><span data-stu-id="9aeb6-121">As soon as the drive is unlocked, select **Reset Password** to change your current password.</span></span>

## <span data-ttu-id="9aeb6-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9aeb6-122">Related topics</span></span>


[<span data-ttu-id="9aeb6-123">Administrando os Recursos do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="9aeb6-123">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





