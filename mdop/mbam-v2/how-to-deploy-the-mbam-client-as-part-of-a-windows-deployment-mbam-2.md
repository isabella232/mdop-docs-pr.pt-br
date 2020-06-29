---
title: Como implantar o cliente do MBAM como parte de uma implantação do Windows
description: Como implantar o cliente do MBAM como parte de uma implantação do Windows
author: dansimp
ms.assetid: 67387de7-8b02-4412-9850-3b8d8e5c18af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d75e5748167d2d4866f98e9d3611584067ecd418
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799509"
---
# <span data-ttu-id="62e72-103">Como implantar o cliente do MBAM como parte de uma implantação do Windows</span><span class="sxs-lookup"><span data-stu-id="62e72-103">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>


<span data-ttu-id="62e72-104">O cliente Microsoft BitLocker Administration and Monitoring (MBAM) permite que os administradores imponham e monitorem a criptografia de unidade de disco BitLocker em computadores da empresa.</span><span class="sxs-lookup"><span data-stu-id="62e72-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="62e72-105">Se computadores que têm um chip TPM (Trusted Platform Module), o cliente BitLocker pode ser integrado a uma organização habilitando o gerenciamento e a criptografia de BitLocker em computadores cliente como parte do processo de implantação e implantação de imagens do Windows.</span><span class="sxs-lookup"><span data-stu-id="62e72-105">If computers that have a Trusted Platform Module (TPM) chip, the BitLocker client can be integrated into an organization by enabling BitLocker management and encryption on client computers as part of the imaging and Windows deployment process.</span></span>

**<span data-ttu-id="62e72-106">Observação</span><span class="sxs-lookup"><span data-stu-id="62e72-106">Note</span></span>**  
<span data-ttu-id="62e72-107">Para verificar os requisitos do sistema do cliente de administração e administração do Microsoft BitLocker, consulte [configurações compatíveis do MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="62e72-107">To review the Microsoft BitLocker Administration and Monitoring Client system requirements, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>



<span data-ttu-id="62e72-108">A criptografia de computadores cliente com o BitLocker durante o estágio inicial da criação de imagens de uma implantação do Windows pode reduzir a sobrecarga administrativa necessária para implementar o MBAM em uma organização.</span><span class="sxs-lookup"><span data-stu-id="62e72-108">Encrypting client computers with BitLocker during the initial imaging stage of a Windows deployment can lower the administrative overhead necessary for implementing MBAM in an organization.</span></span> <span data-ttu-id="62e72-109">Ele também garante que todos os computadores implantados já tenham o BitLocker em execução e estejam configurados corretamente.</span><span class="sxs-lookup"><span data-stu-id="62e72-109">It also ensures that every computer that is deployed already has BitLocker running and is configured correctly.</span></span>

**<span data-ttu-id="62e72-110">Observação</span><span class="sxs-lookup"><span data-stu-id="62e72-110">Note</span></span>**  
<span data-ttu-id="62e72-111">O procedimento neste tópico descreve como modificar o registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="62e72-111">The procedure in this topic describes modifying the Windows registry.</span></span> <span data-ttu-id="62e72-112">Usar o editor do registro incorretamente pode causar sérios problemas que podem exigir a reinstalação do Windows.</span><span class="sxs-lookup"><span data-stu-id="62e72-112">Using Registry Editor incorrectly can cause serious problems that may require you to reinstall Windows.</span></span> <span data-ttu-id="62e72-113">A Microsoft não pode garantir que os problemas resultantes do uso incorreto do editor do registro possam ser resolvidos.</span><span class="sxs-lookup"><span data-stu-id="62e72-113">Microsoft cannot guarantee that problems resulting from the incorrect use of Registry Editor can be solved.</span></span> <span data-ttu-id="62e72-114">Use o editor do registro por sua conta e risco.</span><span class="sxs-lookup"><span data-stu-id="62e72-114">Use Registry Editor at your own risk.</span></span>



**<span data-ttu-id="62e72-115">Para criptografar um computador como parte da implantação do Windows</span><span class="sxs-lookup"><span data-stu-id="62e72-115">To encrypt a computer as part of Windows deployment</span></span>**

1.  <span data-ttu-id="62e72-116">Se sua organização planeja usar o protetor TPM (Trusted Platform Module) ou as opções de protetor TPM + PIN no BitLocker, você deve ativar o chip TPM antes da implantação inicial do MBAM.</span><span class="sxs-lookup"><span data-stu-id="62e72-116">If your organization is planning to use the Trusted Platform Module (TPM) protector or the TPM + PIN protector options in BitLocker, you must activate the TPM chip before the initial deployment of MBAM.</span></span> <span data-ttu-id="62e72-117">Ao ativar o chip TPM, você evita uma reinicialização mais tarde no processo e garante que os chips do TPM sejam configurados corretamente de acordo com os requisitos da sua organização.</span><span class="sxs-lookup"><span data-stu-id="62e72-117">When you activate the TPM chip, you avoid a reboot later in the process, and you ensure that the TPM chips are correctly configured according to the requirements of your organization.</span></span> <span data-ttu-id="62e72-118">Você deve ativar o chip TPM manualmente no BIOS do computador.</span><span class="sxs-lookup"><span data-stu-id="62e72-118">You must activate the TPM chip manually in the BIOS of the computer.</span></span>

    **<span data-ttu-id="62e72-119">Observação</span><span class="sxs-lookup"><span data-stu-id="62e72-119">Note</span></span>**  
    <span data-ttu-id="62e72-120">Alguns fornecedores fornecem ferramentas para ativar e ativar o chip TPM no BIOS de dentro do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="62e72-120">Some vendors provide tools to turn on and activate the TPM chip in the BIOS from within the operating system.</span></span> <span data-ttu-id="62e72-121">Consulte a documentação do fabricante para obter mais detalhes sobre como configurar o chip TPM.</span><span class="sxs-lookup"><span data-stu-id="62e72-121">Refer to the manufacturer documentation for more details about how to configure the TPM chip.</span></span>



2.  <span data-ttu-id="62e72-122">Instale o agente cliente de administração e administração do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="62e72-122">Install the Microsoft BitLocker Administration and Monitoring client agent.</span></span>

3.  <span data-ttu-id="62e72-123">Ingressar no computador em um domínio (recomendado).</span><span class="sxs-lookup"><span data-stu-id="62e72-123">Join the computer to a domain (recommended).</span></span>

    -   <span data-ttu-id="62e72-124">Se o computador não estiver associado ao domínio, a senha de recuperação não será armazenada no serviço de recuperação de chave MBAM.</span><span class="sxs-lookup"><span data-stu-id="62e72-124">If the computer is not joined to the domain, the recovery password is not stored in the MBAM Key Recovery service.</span></span> <span data-ttu-id="62e72-125">Por padrão, o MBAM não permite que a criptografia ocorra, a menos que a chave de recuperação possa ser armazenada.</span><span class="sxs-lookup"><span data-stu-id="62e72-125">By default, MBAM does not allow encryption to occur unless the recovery key can be stored.</span></span>

    -   <span data-ttu-id="62e72-126">Se um computador for iniciado no modo de recuperação antes que a chave de recuperação seja armazenada no servidor do MBAM, o computador precisará ser renovado.</span><span class="sxs-lookup"><span data-stu-id="62e72-126">If a computer starts in recovery mode before the recovery key is stored on the MBAM Server, the computer has to be reimaged.</span></span> <span data-ttu-id="62e72-127">Nenhum método de recuperação está disponível.</span><span class="sxs-lookup"><span data-stu-id="62e72-127">No recovery method is available.</span></span>

4.  <span data-ttu-id="62e72-128">Execute o prompt de comando como administrador, interrompa o serviço do MBAM e, em seguida, defina o serviço como **manual** ou por **demanda**e, em seguida, comece digitando os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="62e72-128">Run the command prompt as an administrator, stop the MBAM service, and then set the service to **manual** or **on demand**, and then start by typing the following commands:</span></span>

    **<span data-ttu-id="62e72-129">net stop mbamagent</span><span class="sxs-lookup"><span data-stu-id="62e72-129">net stop mbamagent</span></span>**

    **<span data-ttu-id="62e72-130">SC config mbamagent Start = Demand</span><span class="sxs-lookup"><span data-stu-id="62e72-130">sc config mbamagent start= demand</span></span>**

5.  <span data-ttu-id="62e72-131">Defina as configurações do registro para o agente MBAM para ignorar a política de grupo e executar o TPM para **apenas a criptografia do sistema operacional** executando o **regedit**e, em seguida, importando o modelo de chave do registro de c:\\Arquivos de Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span><span class="sxs-lookup"><span data-stu-id="62e72-131">Set the registry settings for the MBAM agent to ignore Group Policy and run the TPM for **operating system only encryption** by running **Regedit**, and then importing the registry key template from C:\\Program Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.</span></span>

6.  <span data-ttu-id="62e72-132">Em regedit, vá para HKLM\\SOFTWARE\\Microsoft\\MBAM e defina as configurações listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="62e72-132">In regedit, go to HKLM\\SOFTWARE\\Microsoft\\MBAM, and configure the settings that are listed in the following table.</span></span>

    <span data-ttu-id="62e72-133">Entrada do registro</span><span class="sxs-lookup"><span data-stu-id="62e72-133">Registry entry</span></span>

    <span data-ttu-id="62e72-134">Definições de configuração</span><span class="sxs-lookup"><span data-stu-id="62e72-134">Configuration settings</span></span>

    <span data-ttu-id="62e72-135">Deploymenttime</span><span class="sxs-lookup"><span data-stu-id="62e72-135">DeploymentTime</span></span>

    <span data-ttu-id="62e72-136">0 = DESATIVADO</span><span class="sxs-lookup"><span data-stu-id="62e72-136">0 = OFF</span></span>

    <span data-ttu-id="62e72-137">1 = usar configurações de política de tempo de implantação (padrão)</span><span class="sxs-lookup"><span data-stu-id="62e72-137">1 = Use deployment time policy settings (default)</span></span>

    <span data-ttu-id="62e72-138">UseKeyRecoveryService</span><span class="sxs-lookup"><span data-stu-id="62e72-138">UseKeyRecoveryService</span></span>

    <span data-ttu-id="62e72-139">0 = não usar a caução de chave (as próximas duas entradas do registro não são necessárias nesse caso)</span><span class="sxs-lookup"><span data-stu-id="62e72-139">0 = Do not use key escrow ( the next two registry entries are not required in this case)</span></span>

    <span data-ttu-id="62e72-140">1 = usar a caução chave no sistema de recuperação de chave (padrão)</span><span class="sxs-lookup"><span data-stu-id="62e72-140">1 = Use key escrow in Key Recovery system (default)</span></span>

    <span data-ttu-id="62e72-141">Recomendado: o computador deve ser capaz de se comunicar com o serviço de recuperação de chave.</span><span class="sxs-lookup"><span data-stu-id="62e72-141">Recommended: The computer must be able to communicate with the Key Recovery service.</span></span> <span data-ttu-id="62e72-142">Verifique se o computador pode se comunicar com o serviço antes de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="62e72-142">Verify that the computer can communicate with the service before you proceed.</span></span>

    <span data-ttu-id="62e72-143">Keyrecoveryoptions</span><span class="sxs-lookup"><span data-stu-id="62e72-143">KeyRecoveryOptions</span></span>

    <span data-ttu-id="62e72-144">0 = carregar apenas a chave de recuperação</span><span class="sxs-lookup"><span data-stu-id="62e72-144">0 = Uploads Recovery Key Only</span></span>

    <span data-ttu-id="62e72-145">1 = carregar chave de recuperação e pacote de recuperação de chave (padrão)</span><span class="sxs-lookup"><span data-stu-id="62e72-145">1 = Uploads Recovery Key and Key Recovery Package (default)</span></span>

    <span data-ttu-id="62e72-146">KeyRecoveryServiceEndPoint</span><span class="sxs-lookup"><span data-stu-id="62e72-146">KeyRecoveryServiceEndPoint</span></span>

    <span data-ttu-id="62e72-147">Defina esse valor como a URL para o servidor Web de recuperação de chave, por exemplo, http://de &lt; nome de computador &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.</span><span class="sxs-lookup"><span data-stu-id="62e72-147">Set this value to the URL for the Key Recovery web server, for example, http://&lt;computer name&gt;/MBAMRecoveryAndHardwareService/CoreService.svc.</span></span>



~~~
**Note**  
MBAM policy or registry values can be set here to override previously set values.
~~~



7. <span data-ttu-id="62e72-148">O agente MBAM reinicia o sistema durante a implantação do cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="62e72-148">The MBAM agent restarts the system during MBAM client deployment.</span></span> <span data-ttu-id="62e72-149">Quando estiver pronto para esta reinicialização, execute o seguinte comando em um prompt de comando como administrador:</span><span class="sxs-lookup"><span data-stu-id="62e72-149">When you are ready for this reboot, run the following command at a command prompt as an administrator:</span></span>

   **<span data-ttu-id="62e72-150">net start mbamagent</span><span class="sxs-lookup"><span data-stu-id="62e72-150">net start mbamagent</span></span>**

8. <span data-ttu-id="62e72-151">Quando o computador for reiniciado e o BIOS solicitar que você aceite uma alteração no TPM, aceite a alteração.</span><span class="sxs-lookup"><span data-stu-id="62e72-151">When the computers restarts, and the BIOS prompts you to accept a TPM change, accept the change.</span></span>

9. <span data-ttu-id="62e72-152">Durante o processo de criação de imagens do sistema operacional cliente Windows, quando você estiver pronto para iniciar a criptografia, reinicie o serviço do agente do MBAM e defina iniciar como **automático** executando um prompt de comando como administrador e digitando os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="62e72-152">During the Windows client operating system imaging process, when you are ready to start encryption, restart the MBAM agent service, and set start to **automatic** by running a command prompt as an administrator and typing the following commands:</span></span>

   **<span data-ttu-id="62e72-153">SC config mbamagent Start = auto</span><span class="sxs-lookup"><span data-stu-id="62e72-153">sc config mbamagent start= auto</span></span>**

   **<span data-ttu-id="62e72-154">net start mbamagent</span><span class="sxs-lookup"><span data-stu-id="62e72-154">net start mbamagent</span></span>**

10. <span data-ttu-id="62e72-155">Remova os valores do registro bypass executando regedit e indo para a entrada do registro HKLM\\SOFTWARE\\Microsoft.</span><span class="sxs-lookup"><span data-stu-id="62e72-155">Remove the bypass registry values by running Regedit and going to the HKLM\\SOFTWARE\\Microsoft registry entry.</span></span> <span data-ttu-id="62e72-156">Para excluir o nó **MBAM** , clique com o botão direito do mouse no nó e clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="62e72-156">To delete the **MBAM** node, right-click the node and click **Delete**.</span></span>

## <span data-ttu-id="62e72-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="62e72-157">Related topics</span></span>


[<span data-ttu-id="62e72-158">Implantando o Cliente do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="62e72-158">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)









