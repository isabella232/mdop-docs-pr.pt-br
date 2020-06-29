---
title: Como gerenciar opções de criptografia BitLocker do Cliente do MBAM utilizando o Painel de Controle
description: Como gerenciar opções de criptografia BitLocker do Cliente do MBAM utilizando o Painel de Controle
author: dansimp
ms.assetid: e2ff153e-5770-4a12-b79d-cda998b8a8ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a42901ac9d8a1a3527712f4cf342b5c0ca9ffdfd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799606"
---
# <span data-ttu-id="ec2eb-103">Como gerenciar opções de criptografia BitLocker do Cliente do MBAM utilizando o Painel de Controle</span><span class="sxs-lookup"><span data-stu-id="ec2eb-103">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>


<span data-ttu-id="ec2eb-104">Um aplicativo do painel de controle de administração e monitoramento do Microsoft BitLocker (MBAM), chamado de opções de criptografia do BitLocker, estará disponível em **sistema e segurança** quando o cliente de administração e monitoramento do Microsoft BitLocker estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-104">A Microsoft BitLocker Administration and Monitoring (MBAM) control panel application, called BitLocker Encryption Options, will be available under **System and Security** when the Microsoft BitLocker Administration and Monitoring Client is installed.</span></span> <span data-ttu-id="ec2eb-105">Este painel de controle do MBAM personalizado é um painel de controle adicional.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-105">This custom MBAM control panel is an additional control panel.</span></span> <span data-ttu-id="ec2eb-106">Ele não substitui o painel de controle padrão do Windows BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-106">It does not replace the default Windows BitLocker control panel.</span></span> <span data-ttu-id="ec2eb-107">O painel de controle do MBAM pode ser usado para desbloquear unidades fixas e removíveis criptografadas e também gerenciar seu PIN ou senha.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-107">The MBAM control panel can be used to unlock encrypted fixed and removable drives, and also manage your PIN or password.</span></span> <span data-ttu-id="ec2eb-108">Para obter mais informações sobre como habilitar o painel de controle do MBAM, consulte [como ocultar a criptografia do BitLocker padrão no painel de controle do Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="ec2eb-108">For more information about enabling the MBAM control panel, see [How to Hide Default BitLocker Encryption in the Windows Control Panel](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md).</span></span>

**<span data-ttu-id="ec2eb-109">Para usar o painel de controle do cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="ec2eb-109">To use the MBAM Client Control Panel</span></span>**

1.  <span data-ttu-id="ec2eb-110">Para abrir as opções de criptografia do BitLocker, clique em **Iniciar** e, em seguida, selecione **painel de controle**.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-110">To open BitLocker Encryption Options, click **Start** and then select **Control Panel**.</span></span> <span data-ttu-id="ec2eb-111">Quando o **painel de controle** for aberto, selecione **sistema e segurança**.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-111">When **Control Panel** opens, select **System and Security**.</span></span>

2.  <span data-ttu-id="ec2eb-112">Clique duas vezes em **Opções de criptografia do BitLocker** para abrir o painel de controle MBAM personalizado.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-112">Double-click **BitLocker Encryption Options** to open the customized MBAM control panel.</span></span> <span data-ttu-id="ec2eb-113">Você verá uma lista de todas as unidades de disco rígido no computador e seu status de criptografia, além de uma opção para gerenciar seu PIN ou senhas.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-113">You will see a list of all the hard disk drives on the computer and their encryption status, in addition to an option to manage your PIN or passwords.</span></span>

    <span data-ttu-id="ec2eb-114">A lista de unidades de disco rígido no computador pode ser usada para verificar o status de criptografia, desbloquear uma unidade ou solicitar uma isenção de proteção do BitLocker se as políticas de isenção de usuário e computador tiverem sido implantadas.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-114">The list of hard disk drives on the computer can be used to verify encryption status, unlock a drive, or request an exemption for BitLocker protection if the User and Computer Exemption policies have been deployed.</span></span>

    <span data-ttu-id="ec2eb-115">O painel de controle opções de criptografia do BitLocker também permite que os usuários que não são administradores gerenciem seu PIN ou senhas.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-115">The BitLocker Encryption Options control panel also allows for non-administrator users to manage their PIN or passwords.</span></span> <span data-ttu-id="ec2eb-116">Ao selecionar **gerenciar PIN**, os usuários são solicitados a digitar um PIN atual e um novo PIN (além de confirmar o novo PIN).</span><span class="sxs-lookup"><span data-stu-id="ec2eb-116">By selecting **Manage PIN**, users are prompted to enter both a current PIN and a new PIN (in addition to confirming the new PIN).</span></span> <span data-ttu-id="ec2eb-117">Selecionar **Atualizar PIN** irá redefinir o pino para o novo que os usuários selecionaram.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-117">Selecting **Update PIN** will reset the PIN to the new one that the users selected.</span></span>

    <span data-ttu-id="ec2eb-118">Para gerenciar sua senha, selecione **desbloquear unidade** e insira sua senha atual.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-118">To manage your password, select **Unlock drive** and enter your current password.</span></span> <span data-ttu-id="ec2eb-119">Assim que a unidade for desbloqueada, selecione **Redefinir senha** para alterar sua senha atual.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-119">As soon as the drive is unlocked, select **Reset Password** to change your current password.</span></span>

## <span data-ttu-id="ec2eb-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec2eb-120">Related topics</span></span>


[<span data-ttu-id="ec2eb-121">Administrando os Recursos do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="ec2eb-121">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)

 

 





