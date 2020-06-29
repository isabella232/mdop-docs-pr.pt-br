---
title: Como implantar o cliente do MBAM como parte de uma implantação do Windows
description: Como implantar o cliente do MBAM como parte de uma implantação do Windows
author: dansimp
ms.assetid: 8704bf33-535d-41da-b9b2-45b60754367e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a63311bcc93d84472ceff5c80c9222fefd5445c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799567"
---
# <span data-ttu-id="aaac2-103">Como implantar o cliente do MBAM como parte de uma implantação do Windows</span><span class="sxs-lookup"><span data-stu-id="aaac2-103">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>


<span data-ttu-id="aaac2-104">O cliente Microsoft BitLocker Administration and Monitoring (MBAM) permite que os administradores imponham e monitorem a criptografia de unidade de disco BitLocker em computadores da empresa.</span><span class="sxs-lookup"><span data-stu-id="aaac2-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="aaac2-105">O cliente BitLocker pode ser integrado a uma organização habilitando o gerenciamento e a criptografia de BitLocker em computadores cliente durante o processo de criação de imagens do computador e implantação do Windows.</span><span class="sxs-lookup"><span data-stu-id="aaac2-105">The BitLocker Client can be integrated into an organization by enabling BitLocker management and encryption on client computers during the computer imaging and Windows deployment process.</span></span>

**<span data-ttu-id="aaac2-106">Observação</span><span class="sxs-lookup"><span data-stu-id="aaac2-106">Note</span></span>**  
<span data-ttu-id="aaac2-107">Para verificar os requisitos do sistema do cliente do MBAM, consulte [configurações compatíveis do MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="aaac2-107">To review the MBAM Client system requirements, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>



<span data-ttu-id="aaac2-108">A criptografia de computadores cliente com o BitLocker durante o estágio inicial da imagem de uma implantação do Windows pode reduzir a sobrecarga administrativa da implementação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="aaac2-108">Encryption of client computers with BitLocker during the initial imaging stage of a Windows deployment can lower the administrative overhead for MBAM implementation.</span></span> <span data-ttu-id="aaac2-109">Essa abordagem também garante que todos os computadores implantados já tenham o BitLocker em execução e estejam configurados corretamente.</span><span class="sxs-lookup"><span data-stu-id="aaac2-109">This approach also ensures that every computer that is deployed already has BitLocker running and is configured correctly.</span></span>

**<span data-ttu-id="aaac2-110">Aviso</span><span class="sxs-lookup"><span data-stu-id="aaac2-110">Warning</span></span>**  
<span data-ttu-id="aaac2-111">Este tópico descreve como alterar o registro do Windows usando o editor do registro.</span><span class="sxs-lookup"><span data-stu-id="aaac2-111">This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="aaac2-112">Se você alterar o registro do Windows incorretamente, poderá causar sérios problemas que talvez exijam a reinstalação do Windows.</span><span class="sxs-lookup"><span data-stu-id="aaac2-112">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="aaac2-113">Você deve fazer uma cópia de backup dos arquivos do registro (System. dat e User. dat) antes de alterar o registro.</span><span class="sxs-lookup"><span data-stu-id="aaac2-113">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="aaac2-114">A Microsoft não pode garantir que os problemas que podem ocorrer quando você alterar o registro possam ser resolvidos.</span><span class="sxs-lookup"><span data-stu-id="aaac2-114">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="aaac2-115">Altere o registro por sua conta e risco.</span><span class="sxs-lookup"><span data-stu-id="aaac2-115">Change the registry at your own risk.</span></span>



**<span data-ttu-id="aaac2-116">Para criptografar um computador como parte da implantação do Windows</span><span class="sxs-lookup"><span data-stu-id="aaac2-116">To encrypt a computer as part of Windows deployment</span></span>**

1.  <span data-ttu-id="aaac2-117">Se sua organização planeja usar o protetor TPM (Trusted Platform Module) ou as opções de protetor TPM + PIN no BitLocker, você deve ativar o chip TPM antes da implantação inicial do MBAM.</span><span class="sxs-lookup"><span data-stu-id="aaac2-117">If your organization plans to use the Trusted Platform Module (TPM) protector or the TPM + PIN protector options in BitLocker, you must activate the TPM chip before the initial deployment of MBAM.</span></span> <span data-ttu-id="aaac2-118">Ao ativar o chip TPM, você evita uma reinicialização mais tarde no processo e garante que os chips do TPM sejam configurados corretamente de acordo com os requisitos da sua organização.</span><span class="sxs-lookup"><span data-stu-id="aaac2-118">When you activate the TPM chip, you avoid a reboot later in the process, and you ensure that the TPM chips are correctly configured according to the requirements of your organization.</span></span> <span data-ttu-id="aaac2-119">Você deve ativar o chip TPM manualmente na BIOS do computador.</span><span class="sxs-lookup"><span data-stu-id="aaac2-119">You must activate the TPM chip manually in the computer's BIOS.</span></span> <span data-ttu-id="aaac2-120">Consulte a documentação do fabricante para obter mais detalhes sobre como configurar o chip TPM.</span><span class="sxs-lookup"><span data-stu-id="aaac2-120">Refer to the manufacturer documentation for more details about how to configure the TPM chip.</span></span>

2.  <span data-ttu-id="aaac2-121">Instale o agente do cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="aaac2-121">Install the MBAM client agent.</span></span>

3.  <span data-ttu-id="aaac2-122">Recomendamos que você ingresse no computador em um domínio...</span><span class="sxs-lookup"><span data-stu-id="aaac2-122">We recommend that you join the computer to a domain...</span></span>

    -   <span data-ttu-id="aaac2-123">Se o computador não estiver associado a um domínio, a senha de recuperação não será armazenada no serviço de recuperação de chave MBAM.</span><span class="sxs-lookup"><span data-stu-id="aaac2-123">If the computer is not joined to a domain, the recovery password is not stored in the MBAM Key Recovery service.</span></span> <span data-ttu-id="aaac2-124">Por padrão, o MBAM não permite que a criptografia ocorra, a menos que a chave de recuperação possa ser armazenada.</span><span class="sxs-lookup"><span data-stu-id="aaac2-124">By default, MBAM does not allow encryption to occur unless the recovery key can be stored.</span></span>

    -   <span data-ttu-id="aaac2-125">Se um computador for iniciado no modo de recuperação antes que a chave de recuperação seja armazenada no servidor do MBAM, o computador precisará ser renovado.</span><span class="sxs-lookup"><span data-stu-id="aaac2-125">If a computer starts in recovery mode before the recovery key is stored on the MBAM server, the computer has to be reimaged.</span></span> <span data-ttu-id="aaac2-126">Nenhum método de recuperação está disponível.</span><span class="sxs-lookup"><span data-stu-id="aaac2-126">No recovery method is available.</span></span>

4.  <span data-ttu-id="aaac2-127">Abra um prompt de comando como administrador, interrompa o serviço do MBAM e, em seguida, defina o serviço como **manual** ou por **demanda**.</span><span class="sxs-lookup"><span data-stu-id="aaac2-127">Open a command prompt as an administrator, stop the MBAM service, and then set the service to **manual** or **on demand**.</span></span> <span data-ttu-id="aaac2-128">Em seguida, execute os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="aaac2-128">Then, run the following commands:</span></span>

    **<span data-ttu-id="aaac2-129">net stop mbamagent</span><span class="sxs-lookup"><span data-stu-id="aaac2-129">net stop mbamagent</span></span>**

    **<span data-ttu-id="aaac2-130">SC config mbamagent Start = Demand</span><span class="sxs-lookup"><span data-stu-id="aaac2-130">sc config mbamagent start= demand</span></span>**

5.  <span data-ttu-id="aaac2-131">Defina as configurações do registro para que o agente MBAM ignore a política de grupo e execute o TPM para que o **sistema operacional somente** execute a criptografia para fazer isso, execute o **regedit**e, em seguida, importe o modelo de chave do registro de c:\\Arquivos de Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span><span class="sxs-lookup"><span data-stu-id="aaac2-131">Set the registry settings for the MBAM agent to ignore Group Policy and run the TPM for **operating system only encryption** To do this, run **regedit**, and then import the registry key template from C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span></span>

6.  <span data-ttu-id="aaac2-132">Em regedit, vá para HKLM\\SOFTWARE\\Microsoft\\MBAM e defina as configurações listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="aaac2-132">In regedit, go to HKLM\\SOFTWARE\\Microsoft\\MBAM and configure the settings that are listed in the following table.</span></span>

    <span data-ttu-id="aaac2-133">Entrada do registro</span><span class="sxs-lookup"><span data-stu-id="aaac2-133">Registry entry</span></span>

    <span data-ttu-id="aaac2-134">Definições de configuração</span><span class="sxs-lookup"><span data-stu-id="aaac2-134">Configuration settings</span></span>

    <span data-ttu-id="aaac2-135">Deploymenttime</span><span class="sxs-lookup"><span data-stu-id="aaac2-135">DeploymentTime</span></span>

    <span data-ttu-id="aaac2-136">0 = DESATIVADO</span><span class="sxs-lookup"><span data-stu-id="aaac2-136">0 = OFF</span></span>

    <span data-ttu-id="aaac2-137">1 = usar configurações de política de tempo de implantação (padrão)</span><span class="sxs-lookup"><span data-stu-id="aaac2-137">1 = Use deployment time policy settings (default)</span></span>

    <span data-ttu-id="aaac2-138">UseKeyRecoveryService</span><span class="sxs-lookup"><span data-stu-id="aaac2-138">UseKeyRecoveryService</span></span>

    <span data-ttu-id="aaac2-139">0 = não usar a caução de chave (as próximas duas entradas do registro não são necessárias nesse caso).</span><span class="sxs-lookup"><span data-stu-id="aaac2-139">0 = Do not use key escrow (The next two registry entries are not required in this case.)</span></span>

    <span data-ttu-id="aaac2-140">1 = usar a caução chave no sistema de recuperação de chave (padrão)</span><span class="sxs-lookup"><span data-stu-id="aaac2-140">1 = Use key escrow in Key Recovery system (default)</span></span>

    <span data-ttu-id="aaac2-141">Recomendado: o computador deve ser capaz de se comunicar com o serviço de recuperação de chave.</span><span class="sxs-lookup"><span data-stu-id="aaac2-141">Recommended: The computer must be able to communicate with the Key Recovery service.</span></span> <span data-ttu-id="aaac2-142">Verifique se o computador pode se comunicar com o serviço antes de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="aaac2-142">Verify that the computer can communicate with the service before you proceed.</span></span>

    <span data-ttu-id="aaac2-143">Keyrecoveryoptions</span><span class="sxs-lookup"><span data-stu-id="aaac2-143">KeyRecoveryOptions</span></span>

    <span data-ttu-id="aaac2-144">0 = somente chave de recuperação para carregar</span><span class="sxs-lookup"><span data-stu-id="aaac2-144">0 = Upload Recovery Key Only</span></span>

    <span data-ttu-id="aaac2-145">1 = carregar chave de recuperação e pacote de recuperação de chave (padrão)</span><span class="sxs-lookup"><span data-stu-id="aaac2-145">1 = Upload Recovery Key and Key Recovery Package (default)</span></span>

    <span data-ttu-id="aaac2-146">KeyRecoveryServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="aaac2-146">KeyRecoveryServiceEndPoint</span></span>

    <span data-ttu-id="aaac2-147">Defina esse valor como a URL para o servidor Web de recuperação de chave.</span><span class="sxs-lookup"><span data-stu-id="aaac2-147">Set this value to the URL for the Key Recovery web server.</span></span>

    <span data-ttu-id="aaac2-148">Exemplo: http://de &lt; nome do computador &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.</span><span class="sxs-lookup"><span data-stu-id="aaac2-148">Example: http://&lt;computer name&gt;/MBAMRecoveryAndHardwareService/CoreService.svc.</span></span>



~~~
**Note**  
MBAM policy or registry values can be set here to override the previously set values.
~~~



7. <span data-ttu-id="aaac2-149">O agente MBAM reinicia o sistema durante a implantação do cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="aaac2-149">The MBAM agent restarts the system during MBAM client deployment.</span></span> <span data-ttu-id="aaac2-150">Quando estiver pronto para esta reinicialização, execute o seguinte comando em um prompt de comando como administrador:</span><span class="sxs-lookup"><span data-stu-id="aaac2-150">When you are ready for this reboot, run the following command at a command prompt as an administrator:</span></span>

   **<span data-ttu-id="aaac2-151">net start mbamagent</span><span class="sxs-lookup"><span data-stu-id="aaac2-151">net start mbamagent</span></span>**

8. <span data-ttu-id="aaac2-152">Quando o computador for reiniciado e o BIOS solicitar que você aceite uma alteração no TPM, aceite a alteração.</span><span class="sxs-lookup"><span data-stu-id="aaac2-152">When the computers restarts and the BIOS prompts you to accept a TPM change, accept the change.</span></span>

9. <span data-ttu-id="aaac2-153">Durante o processo de criação de imagens do sistema operacional cliente Windows, quando você estiver pronto para iniciar a criptografia, reinicie o serviço do agente MBAM.</span><span class="sxs-lookup"><span data-stu-id="aaac2-153">During the Windows client operating system imaging process, when you are ready to start encryption, restart the MBAM agent service.</span></span> <span data-ttu-id="aaac2-154">Em seguida, para definir start to **Automatic**, abra um prompt de comando como administrador e execute os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="aaac2-154">Then, to set start to **automatic**, open a command prompt as an administrator and run the following commands:</span></span>

   **<span data-ttu-id="aaac2-155">SC config mbamagent Start = auto</span><span class="sxs-lookup"><span data-stu-id="aaac2-155">sc config mbamagent start= auto</span></span>**

   **<span data-ttu-id="aaac2-156">net start mbamagent</span><span class="sxs-lookup"><span data-stu-id="aaac2-156">net start mbamagent</span></span>**

10. <span data-ttu-id="aaac2-157">Remova os valores do registro de bypass.</span><span class="sxs-lookup"><span data-stu-id="aaac2-157">Remove the bypass registry values.</span></span> <span data-ttu-id="aaac2-158">Para fazer isso, execute regedit, navegue até a entrada do registro HKLM\\SOFTWARE\\Microsoft, clique com o botão direito do mouse no nó **MBAM** e, em seguida, clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="aaac2-158">To do this, run regedit, browse to the HKLM\\SOFTWARE\\Microsoft registry entry, right-click the **MBAM** node, and then click **Delete**.</span></span>

## <span data-ttu-id="aaac2-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aaac2-159">Related topics</span></span>


[<span data-ttu-id="aaac2-160">Implantando o Cliente do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="aaac2-160">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)









