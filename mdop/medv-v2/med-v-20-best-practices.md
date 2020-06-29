---
title: Práticas recomendadas da MED-V 2.0
description: Práticas recomendadas da MED-V 2.0
author: dansimp
ms.assetid: 47ba2dd1-6c6e-4d6e-8e18-b42291f8e02a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7b664d33b403b821ce6bc9c045d937380ab4f91b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799807"
---
# <span data-ttu-id="45a65-103">Práticas recomendadas da MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="45a65-103">MED-V 2.0 Best Practices</span></span>


<span data-ttu-id="45a65-104">Quando estiver planejando, implantando e gerenciando o MED-V na sua empresa, você poderá encontrar as recomendações de práticas recomendadas para ser útil.</span><span class="sxs-lookup"><span data-stu-id="45a65-104">When you are planning, deploying, and managing MED-V in your enterprise, you may find the best practice recommendations to be useful.</span></span>

### <span data-ttu-id="45a65-105">Configurar a primeira vez a instalação para ser executada de forma autônoma</span><span class="sxs-lookup"><span data-stu-id="45a65-105">Configure first time setup to run unattended</span></span>

<span data-ttu-id="45a65-106">Embora você possa especificar as configurações de sua preferência, uma prática recomendada do MED-V é criar o arquivo Sysprep. inf para que a configuração inicial possa ser executada no modo **autônomo** .</span><span class="sxs-lookup"><span data-stu-id="45a65-106">Although you can specify any settings that you prefer, a MED-V best practice is that you create the Sysprep.inf file so that first time setup can be run in **Unattended** mode.</span></span> <span data-ttu-id="45a65-107">Isso exige que você forneça todas as informações de configurações necessárias ao continuar usando o assistente do **Gerenciador de instalação** .</span><span class="sxs-lookup"><span data-stu-id="45a65-107">This requires you to provide all the required settings information as you continue through the **Setup Manager** wizard.</span></span> <span data-ttu-id="45a65-108">Para obter mais informações sobre como configurar a imagem do MED-V, consulte [Configurando uma imagem do Windows Virtual PC para med-v](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="45a65-108">For more information about how to configure the MED-V image, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

### <span data-ttu-id="45a65-109">Desabilitar pontos de restauração na máquina virtual</span><span class="sxs-lookup"><span data-stu-id="45a65-109">Disable restore points on the virtual machine</span></span>

<span data-ttu-id="45a65-110">Antes de criar o pacote do espaço de trabalho do MED-V, recomendamos que você desabilite os pontos de restauração na máquina virtual para impedir que o disco diferencial aumente não associado.</span><span class="sxs-lookup"><span data-stu-id="45a65-110">Before you create the MED-V workspace package, we recommend that you disable restore points on the virtual machine to prevent the differencing disk from growing unbounded.</span></span> <span data-ttu-id="45a65-111">Para obter mais informações, consulte [como desativar e ativar a restauração do sistema no Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) ( https://go.microsoft.com/fwlink/?LinkId=195927) .</span><span class="sxs-lookup"><span data-stu-id="45a65-111">For more information, see [How to turn off and turn on System Restore in Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) (https://go.microsoft.com/fwlink/?LinkId=195927).</span></span>

### <span data-ttu-id="45a65-112">Configurar a imagem do MED-V para usar perfis locais</span><span class="sxs-lookup"><span data-stu-id="45a65-112">Configure MED-V image to use local profiles</span></span>

<span data-ttu-id="45a65-113">Recomendamos que você aplique apenas as políticas que fazem sentido em um ambiente de compatibilidade do aplicativo para Windows XP.</span><span class="sxs-lookup"><span data-stu-id="45a65-113">We recommend that you apply only those policies that make sense in an application compatibility environment for Windows XP.</span></span> <span data-ttu-id="45a65-114">Por exemplo, as políticas de personalização da área de trabalho geralmente não precisam ser aplicadas e devem ser desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="45a65-114">For example, desktop customization policies do not typically have to be applied and should be disabled.</span></span> <span data-ttu-id="45a65-115">Para obter mais informações sobre como permitir somente perfis locais, consulte [configurações de política de grupo para perfis de usuário móvel](https://go.microsoft.com/fwlink/?LinkId=205072) ( https://go.microsoft.com/fwlink/?LinkId=205072) .</span><span class="sxs-lookup"><span data-stu-id="45a65-115">For more information about how to allow only local profiles, see [Group Policy Settings for Roaming User Profiles](https://go.microsoft.com/fwlink/?LinkId=205072) (https://go.microsoft.com/fwlink/?LinkId=205072).</span></span>

### <span data-ttu-id="45a65-116">Configurar uma atualização de desempenho da política de grupo</span><span class="sxs-lookup"><span data-stu-id="45a65-116">Configure a Group Policy performance update</span></span>

<span data-ttu-id="45a65-117">Por padrão, a política de grupo é baixada para um computador, um byte de cada vez.</span><span class="sxs-lookup"><span data-stu-id="45a65-117">By default, Group Policy is downloaded to a computer one byte at a time.</span></span> <span data-ttu-id="45a65-118">Isso causa atrasos quando o MED-V está sendo associado ao domínio.</span><span class="sxs-lookup"><span data-stu-id="45a65-118">This causes delays when MED-V is being joined to the domain.</span></span> <span data-ttu-id="45a65-119">Para aumentar o desempenho da política de grupo, recomendamos que você defina o seguinte valor da chave do registro para o registro:</span><span class="sxs-lookup"><span data-stu-id="45a65-119">To increase the performance of Group Policy, we recommend that you set the following registry key value to the registry:</span></span>

<span data-ttu-id="45a65-120">Subchave do registro: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span><span class="sxs-lookup"><span data-stu-id="45a65-120">Registry subkey: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span></span>

<span data-ttu-id="45a65-121">Entrada: BufferPolicyReads</span><span class="sxs-lookup"><span data-stu-id="45a65-121">Entry: BufferPolicyReads</span></span>

<span data-ttu-id="45a65-122">Tipo: DWORD</span><span class="sxs-lookup"><span data-stu-id="45a65-122">Type: DWORD</span></span>

<span data-ttu-id="45a65-123">Valor: 1</span><span class="sxs-lookup"><span data-stu-id="45a65-123">Value: 1</span></span>

### <span data-ttu-id="45a65-124">Distribuir aviso legal por meio da política de grupo em vez de na imagem do MED-V</span><span class="sxs-lookup"><span data-stu-id="45a65-124">Distribute legal notice through Group Policy instead of in the MED-V image</span></span>

<span data-ttu-id="45a65-125">Se você quiser que os usuários finais vejam um contrato de nível de serviço (SLA) antes de acessarem o MED-V, recomendamos que você aplique o SLA por meio da política de grupo para que o SLA seja exibido para o usuário final após a primeira vez que a instalação for concluída.</span><span class="sxs-lookup"><span data-stu-id="45a65-125">If you want end users to see a service level agreement (SLA) before they access MED-V, we recommend that you enforce the SLA through Group Policy later so that the SLA is displayed to the end user after the first time setup is finished.</span></span>

<span data-ttu-id="45a65-126">**Cuidado**  Embora seja possível executar a primeira prática durante a configuração no modo **autônomo** , se você decidir definir a política local ou a entrada do registro para incluir um SLA na sua imagem (disco rígido virtual), também deverá especificar a primeira vez que a configuração da instalação será executada no modo **assistido** ou que a configuração da primeira vez poderá falhar.</span><span class="sxs-lookup"><span data-stu-id="45a65-126">**Caution** Even though a best practice is to run first time setup in **Unattended** mode, if you decide to set the local policy or registry entry to include an SLA in your image (virtual hard disk), you must also specify that first time setup is run in **Attended** mode, or first time setup can fail.</span></span>

 

### <span data-ttu-id="45a65-127">Compactar o disco rígido virtual</span><span class="sxs-lookup"><span data-stu-id="45a65-127">Compact the virtual hard disk</span></span>

<span data-ttu-id="45a65-128">Recomendamos que você compacte seu disco rígido virtual para recuperar espaço em disco vazio e reduzir o tamanho do disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="45a65-128">We recommend that you compact your virtual hard disk to reclaim empty disk space and reduce the size of the virtual hard disk.</span></span> <span data-ttu-id="45a65-129">Para obter mais informações sobre como compactar seu disco rígido virtual, consulte [compactando o disco rígido virtual do MED-V](compacting-the-med-v-virtual-hard-disk.md).</span><span class="sxs-lookup"><span data-stu-id="45a65-129">For more information about how to compact your virtual hard disk, see [Compacting the MED-V Virtual Hard Disk](compacting-the-med-v-virtual-hard-disk.md).</span></span>

### <span data-ttu-id="45a65-130">Configurar a máquina virtual para reiniciar em uma falha de tela azul</span><span class="sxs-lookup"><span data-stu-id="45a65-130">Configure virtual machine to restart on blue screen crash</span></span>

<span data-ttu-id="45a65-131">Recomendamos que você configure a máquina virtual do espaço de trabalho do MED-V para reiniciar automaticamente quando encontrar uma falha de tela azul.</span><span class="sxs-lookup"><span data-stu-id="45a65-131">We recommend that you configure the MED-V workspace virtual machine to automatically restart when it encounters a blue screen crash.</span></span> <span data-ttu-id="45a65-132">Para definir essa configuração no convidado, defina o valor de reinicialização na chave hKey \ _LOCAL \ _MACHINE \\system\\currentcontrolset\\control\\crashcontrol como "1".</span><span class="sxs-lookup"><span data-stu-id="45a65-132">To configure this setting in the guest, set the AutoReboot value in the HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\CrashControl key to “1”.</span></span>

<span data-ttu-id="45a65-133">Você também pode definir essa configuração clicando em **Iniciar**, em **painel de controle**e, em seguida, em **sistema**.</span><span class="sxs-lookup"><span data-stu-id="45a65-133">You can also configure this setting by clicking **Start**, clicking **Control Panel**, and then clicking **System**.</span></span> <span data-ttu-id="45a65-134">Em seguida, na área **inicialização e recuperação** da guia **avançado** , clique em **configurações**.</span><span class="sxs-lookup"><span data-stu-id="45a65-134">Then, in the **Startup and Recovery** area of the **Advanced** tab, click **Settings**.</span></span> <span data-ttu-id="45a65-135">Marque a caixa de seleção **reinicialização automática** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="45a65-135">Select the **Automatically restart** check box and click **OK**.</span></span>

### <span data-ttu-id="45a65-136">Fazer backup da imagem do MED-V antes de lacra-la</span><span class="sxs-lookup"><span data-stu-id="45a65-136">Back up MED-V image before sealing it</span></span>

<span data-ttu-id="45a65-137">Recomendamos que você crie uma cópia de backup da imagem do MED-V antes de lacra-la.</span><span class="sxs-lookup"><span data-stu-id="45a65-137">We recommend that you create a backup copy of the MED-V image before you seal it.</span></span> <span data-ttu-id="45a65-138">Para obter mais informações sobre como lacrar sua imagem do MED-V, consulte [Configurando uma imagem do Windows Virtual PC para med-v](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="45a65-138">For more information about sealing your MED-V image, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

### <span data-ttu-id="45a65-139">Instalar o Windows Virtual PC por último ao instalar a partir de um arquivo em lote</span><span class="sxs-lookup"><span data-stu-id="45a65-139">Install Windows Virtual PC last when installing from a batch file</span></span>

<span data-ttu-id="45a65-140">Ao instalar os componentes do MED-V usando um arquivo em lotes, especifique que o Windows Virtual PC e o hotfix do Windows Virtual PC são instalados após o agente do host do MED-V e os arquivos de pacote do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="45a65-140">When you install the MED-V components by using a batch file, specify that Windows Virtual PC and the Windows Virtual PC hotfix are installed after the MED-V Host Agent and the MED-V workspace package files.</span></span> <span data-ttu-id="45a65-141">Isso garante que o Windows Update não causará interferência com o processo de instalação exigindo uma reinicialização.</span><span class="sxs-lookup"><span data-stu-id="45a65-141">This ensures that Windows Update will not cause any interference with the installation process by requiring a restart.</span></span>

### <span data-ttu-id="45a65-142">Instalar o espaço de trabalho do MED-V na pasta local</span><span class="sxs-lookup"><span data-stu-id="45a65-142">Install MED-V workspace from local folder</span></span>

<span data-ttu-id="45a65-143">Devido a problemas que podem ocorrer ao instalar o MED-V a partir de um local de rede, recomendamos que você copie os arquivos de configuração do espaço de trabalho do MED-V localmente e, em seguida, execute setup.exe.</span><span class="sxs-lookup"><span data-stu-id="45a65-143">Because of problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.</span></span>

### <a href="" id="manage-printer-redirection-in-one-manner-only-"></a><span data-ttu-id="45a65-144">Gerenciar o redirecionamento de impressoras somente de uma maneira</span><span class="sxs-lookup"><span data-stu-id="45a65-144">Manage printer redirection in one manner only</span></span>

<span data-ttu-id="45a65-145">Se uma impressora é instalada manualmente na máquina virtual de convidado do MED-V, e a mesma impressora é instalada posteriormente no computador host, o resultado é que ela é instalada duas vezes no convidado.</span><span class="sxs-lookup"><span data-stu-id="45a65-145">If a printer is manually installed on the MED-V guest virtual machine, and the same printer is later installed on the host computer, the result is that it is installed two times in the guest.</span></span> <span data-ttu-id="45a65-146">Para evitar essa situação, recomendamos que você gerencie o redirecionamento de impressora apenas de uma maneira: desabilite o redirecionamento e instale as impressoras manualmente no convidado ou habilite o redirecionamento e não instale impressoras manualmente no convidado.</span><span class="sxs-lookup"><span data-stu-id="45a65-146">To avoid this situation, we recommend as MED-V best practice that you manage printer redirection in one manner only: either disable redirection and install printers manually on the guest, or enable redirection and do not install printers manually on the guest.</span></span>

### <a href="" id="configure-settings-for-med-v-guest-patching-"></a><span data-ttu-id="45a65-147">Definir configurações para patch de convidado do MED-V</span><span class="sxs-lookup"><span data-stu-id="45a65-147">Configure settings for MED-V guest patching</span></span>

<span data-ttu-id="45a65-148">Você pode controlar quando e por quanto tempo a máquina virtual do MED-V pode receber atualizações automáticas definindo os valores de configuração relevantes no registro.</span><span class="sxs-lookup"><span data-stu-id="45a65-148">You can control when and for how long the MED-V virtual machine awakens to receive automatic updates by defining the relevant configuration values in the registry.</span></span> <span data-ttu-id="45a65-149">Uma prática recomendada do MED-V é definir seu intervalo de ativação para corresponder ao tempo em que você agendou atualizações regulares para máquinas virtuais do MED-V.</span><span class="sxs-lookup"><span data-stu-id="45a65-149">A MED-V best practice is to set your wake-up interval to match the time when you have scheduled regular updates for MED-V virtual machines.</span></span> <span data-ttu-id="45a65-150">Além disso, recomendamos que você defina essas configurações para se parecer com o comportamento do computador host.</span><span class="sxs-lookup"><span data-stu-id="45a65-150">In addition, we recommend that you configure these settings to resemble the host computer’s behavior.</span></span>

<span data-ttu-id="45a65-151">Para obter mais informações sobre como definir as configurações para o patch de convidado do MED-V, consulte [gerenciando atualizações automáticas para espaços de trabalho do MED-v](managing-automatic-updates-for-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="45a65-151">For more information about how to configure settings for MED-V guest patching, see [Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md).</span></span>

### <span data-ttu-id="45a65-152">Configurar antivírus/software de backup</span><span class="sxs-lookup"><span data-stu-id="45a65-152">Configure antivirus/backup software</span></span>

<span data-ttu-id="45a65-153">Para impedir que as atividades de antivírus afetem o desempenho da área de trabalho virtual, recomendamos que, quando possível, você exclua os seguintes tipos de arquivo de máquina virtual de qualquer processo de antivírus ou backup em execução no computador host do MED-V:</span><span class="sxs-lookup"><span data-stu-id="45a65-153">To prevent antivirus activity from affecting the performance of the virtual desktop, we recommend that when you can, you exclude the following virtual machine file types from any antivirus or backup process that is running on the MED-V host computer:</span></span>

-   <span data-ttu-id="45a65-154">\*. VMC</span><span class="sxs-lookup"><span data-stu-id="45a65-154">\*.VMC</span></span>

-   <span data-ttu-id="45a65-155">\*. VUD</span><span class="sxs-lookup"><span data-stu-id="45a65-155">\*.VUD</span></span>

-   <span data-ttu-id="45a65-156">\*. VSV</span><span class="sxs-lookup"><span data-stu-id="45a65-156">\*.VSV</span></span>

-   <span data-ttu-id="45a65-157">\*. Wim</span><span class="sxs-lookup"><span data-stu-id="45a65-157">\*.VHD</span></span>

## <span data-ttu-id="45a65-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="45a65-158">Related topics</span></span>


[<span data-ttu-id="45a65-159">Segurança e proteção para a MED-V</span><span class="sxs-lookup"><span data-stu-id="45a65-159">Security and Protection for MED-V</span></span>](security-and-protection-for-med-v.md)

 

 





