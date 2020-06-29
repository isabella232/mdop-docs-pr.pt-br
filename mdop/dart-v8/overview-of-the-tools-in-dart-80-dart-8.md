---
title: Visão geral das ferramentas do DaRT 8.0
description: Visão geral das ferramentas do DaRT 8.0
author: dansimp
ms.assetid: 1766c82e-c099-47d4-b186-4689b026a7e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 10/03/2016
ms.openlocfilehash: a058f6018888f446782aa8f3a18ee89570840c2a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799508"
---
# <span data-ttu-id="188a9-103">Visão geral das ferramentas do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="188a9-103">Overview of the Tools in DaRT 8.0</span></span>


<span data-ttu-id="188a9-104">Na janela **diagnóstico e recuperação do conjunto** de ferramentas de diagnóstico e recuperação do Microsoft (DaRT) 8,0, você pode iniciar qualquer uma das ferramentas individuais que você inclui quando cria a imagem de recuperação do DART 8,0.</span><span class="sxs-lookup"><span data-stu-id="188a9-104">From the **Diagnostics and Recovery Toolset** window in Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0, you can start any of the individual tools that you include when you create the DaRT 8.0 recovery image.</span></span> <span data-ttu-id="188a9-105">Para obter informações sobre como acessar a janela **diagnóstico e conjunto de ferramentas de recuperação** , consulte [como recuperar computadores locais usando a imagem de recuperação do DART](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="188a9-105">For information about how to access the **Diagnostics and Recovery Toolset** window, see [How to Recover Local Computers by Using the DaRT Recovery Image](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="188a9-106">Se ele estiver disponível, você pode usar o **Assistente de soluções** na janela **diagnóstico e recuperação de conjunto de ferramentas** para selecionar a ferramenta que melhor atende a seu problema específico, com base em uma breve entrevista que o assistente fornece.</span><span class="sxs-lookup"><span data-stu-id="188a9-106">If it is available, you can use the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to select the tool that best addresses your particular issue, based on a brief interview that the wizard provides.</span></span>

## <span data-ttu-id="188a9-107">Explorando as ferramentas do DaRT</span><span class="sxs-lookup"><span data-stu-id="188a9-107">Exploring the DaRT tools</span></span>


<span data-ttu-id="188a9-108">Uma descrição das ferramentas do DaRT 8,0 é a seguinte.</span><span class="sxs-lookup"><span data-stu-id="188a9-108">A description of the DaRT 8.0 tools follows.</span></span>

### <span data-ttu-id="188a9-109">Gerenciamento do computador</span><span class="sxs-lookup"><span data-stu-id="188a9-109">Computer Management</span></span>

<span data-ttu-id="188a9-110">**Gerenciamento de computador** é uma coleção de ferramentas administrativas do Windows que ajudam você a solucionar um problema de computador.</span><span class="sxs-lookup"><span data-stu-id="188a9-110">**Computer Management** is a collection of Windows administrative tools that help you troubleshoot a problem computer.</span></span> <span data-ttu-id="188a9-111">Você pode usar as ferramentas de **Gerenciamento do computador** no DART para ver as informações do sistema e os logs de eventos, gerenciar discos, listar Autoruns e gerenciar serviços e drivers.</span><span class="sxs-lookup"><span data-stu-id="188a9-111">You can use the **Computer Management** tools in DaRT to view system information and event logs, manage disks, list autoruns, and manage services and drivers.</span></span> <span data-ttu-id="188a9-112">O console de **Gerenciamento do computador** é personalizado para ajudar você a diagnosticar e reparar problemas que possam impedir a inicialização do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="188a9-112">The **Computer Management** console is customized to help you diagnose and repair problems that might be preventing the Windows operating system from starting.</span></span>

<span data-ttu-id="188a9-113">**Observação**  Não há suporte para a recuperação de discos dinâmicos com o DaRT.</span><span class="sxs-lookup"><span data-stu-id="188a9-113">**Note** The recovery of dynamic disks with DaRT is not supported.</span></span>

 

### <span data-ttu-id="188a9-114">Crash Analyzer</span><span class="sxs-lookup"><span data-stu-id="188a9-114">Crash Analyzer</span></span>

<span data-ttu-id="188a9-115">Use o **Assistente do Crash Analyzer** para determinar rapidamente a causa de uma falha no computador analisando o arquivo de despejo de memória no sistema operacional do Windows que você está reparando.</span><span class="sxs-lookup"><span data-stu-id="188a9-115">Use the **Crash Analyzer Wizard** to quickly determine the cause of a computer failure by analyzing the memory dump file on the Windows operating system that you are repairing.</span></span> <span data-ttu-id="188a9-116">O **Crash Analyzer** examina o arquivo de despejo de memória para o driver que causou a falha do computador.</span><span class="sxs-lookup"><span data-stu-id="188a9-116">**Crash Analyzer** examines the memory dump file for the driver that caused a computer to fail.</span></span> <span data-ttu-id="188a9-117">Em seguida, você pode desabilitar o driver de dispositivo com problema usando o nó **serviços e drivers** na ferramenta de **Gerenciamento do computador** .</span><span class="sxs-lookup"><span data-stu-id="188a9-117">You can then disable the problem device driver by using the **Services and Drivers** node in the **Computer Management** tool.</span></span>

<span data-ttu-id="188a9-118">O **Assistente do Crash Analyzer** requer as ferramentas de depuração para Windows e arquivos de símbolo para o sistema operacional que você está reparando.</span><span class="sxs-lookup"><span data-stu-id="188a9-118">The **Crash Analyzer Wizard** requires the Debugging Tools for Windows and symbol files for the operating system that you are repairing.</span></span> <span data-ttu-id="188a9-119">Você pode incluir ambos os requisitos ao criar a imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="188a9-119">You can include both requirements when you create the DaRT recovery image.</span></span> <span data-ttu-id="188a9-120">Se não estiverem incluídos na imagem de recuperação e você não tiver acesso a elas no computador que está reparando, você pode copiar o arquivo de despejo de memória para outro computador e usar a versão autônoma do **Crash Analyzer** para diagnosticar o problema.</span><span class="sxs-lookup"><span data-stu-id="188a9-120">If they are not included on the recovery image and you do not have access to them on the computer that you are repairing, you can copy the memory dump file to another computer and use the stand-alone version of **Crash Analyzer** to diagnose the problem.</span></span>

<span data-ttu-id="188a9-121">Executar o **Crash Analyzer** é uma boa ideia, mesmo que você planeje a nova imagem do computador.</span><span class="sxs-lookup"><span data-stu-id="188a9-121">Running **Crash Analyzer** is a good idea even if you plan to reimage the computer.</span></span> <span data-ttu-id="188a9-122">A imagem pode ter um driver defeituoso que está causando problemas em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="188a9-122">The image could have a defective driver that is causing problems in your environment.</span></span> <span data-ttu-id="188a9-123">Ao executar o **Crash Analyzer**, você pode identificar os drivers dos problemas e melhorar a estabilidade da imagem.</span><span class="sxs-lookup"><span data-stu-id="188a9-123">By running **Crash Analyzer**, you can identify problem drivers and improve the image stability.</span></span>

<span data-ttu-id="188a9-124">Para obter mais informações sobre o **Crash Analyzer**, consulte [Diagnosticando falhas do sistema com o Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="188a9-124">For more information about **Crash Analyzer**, see [Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md).</span></span>

### <span data-ttu-id="188a9-125">Defender</span><span class="sxs-lookup"><span data-stu-id="188a9-125">Defender</span></span>

<span data-ttu-id="188a9-126">**Importante**  Ambientes com o DaRT defender implantados devem, em vez disso, usar a imagem de proteção do Microsoft defender offline (WDO) para detecção de malware.</span><span class="sxs-lookup"><span data-stu-id="188a9-126">**Important** Environments with the DaRT Defender deployed should instead use the Microsoft Defender Offline (WDO) protection image for malware detection.</span></span> <span data-ttu-id="188a9-127">Por causa de como a ferramenta defender se integra ao DaRT, todas as implantações de versão do DaRT com suporte não podem aplicar essas atualizações Antimalware às imagens DaRT.</span><span class="sxs-lookup"><span data-stu-id="188a9-127">Because of how the Defender tool integrates into DaRT, all supported DaRT version deployments cannot apply these anti-malware updates to their DaRT images.</span></span> <span data-ttu-id="188a9-128">Para obter mais informações, consulte [os usuários do Microsoft Diagnostics and Recovery Toolset (DART) devem usar o Microsoft defender offline (WDO) para detecção de malware-->](use-windows-defender-offline-wdo-for-malware-protection-not-dart.md).</span><span class="sxs-lookup"><span data-stu-id="188a9-128">For more information, see  [Microsoft Diagnostics and Recovery Toolset (DaRT) users should use Microsoft Defender Offline (WDO) for malware detection-->](use-windows-defender-offline-wdo-for-malware-protection-not-dart.md).</span></span>

 

<span data-ttu-id="188a9-129">O **defender** pode ajudar a detectar malware e software indesejado e avisá-lo sobre riscos de segurança.</span><span class="sxs-lookup"><span data-stu-id="188a9-129">**Defender** can help detect malware and unwanted software and warn you of security risks.</span></span> <span data-ttu-id="188a9-130">Você pode usar essa ferramenta para examinar um computador e remover malware mesmo quando o sistema operacional do Windows instalado não está em execução.</span><span class="sxs-lookup"><span data-stu-id="188a9-130">You can use this tool to scan a computer for and remove malware even when the installed Windows operating system is not running.</span></span> <span data-ttu-id="188a9-131">Quando o **defender** detecta software mal-intencionado ou indesejado, ele solicita a remoção, a quarentena ou a permissão para cada item.</span><span class="sxs-lookup"><span data-stu-id="188a9-131">When **Defender** detects malicious or unwanted software, it prompts you to remove, quarantine, or allow for each item.</span></span>

<span data-ttu-id="188a9-132">Malware que usa rootkits podem se mascarar do sistema operacional em execução.</span><span class="sxs-lookup"><span data-stu-id="188a9-132">Malware that uses rootkits can mask itself from the running operating system.</span></span> <span data-ttu-id="188a9-133">Se um vírus ou spyware habilitado para rootkit estiver em um computador, a maioria das ferramentas de digitalização e remoção em tempo real não poderá mais vê-la ou removê-la.</span><span class="sxs-lookup"><span data-stu-id="188a9-133">If a rootkit-enabled virus or spyware is in a computer, most real-time scanning and removal tools can no longer see it or remove it.</span></span> <span data-ttu-id="188a9-134">Como você inicializa o computador com problema no DaRT e o sistema operacional instalado está offline, você pode detectar o rootkit sem ser capaz de se mascarar.</span><span class="sxs-lookup"><span data-stu-id="188a9-134">Because you boot the problem computer into DaRT and the installed operating system is offline, you can detect the rootkit without it being able to mask itself.</span></span>

### <span data-ttu-id="188a9-135">Disk Commander</span><span class="sxs-lookup"><span data-stu-id="188a9-135">Disk Commander</span></span>

<span data-ttu-id="188a9-136">O **Disk Commander** permite recuperar e reparar partições de disco ou volumes usando um dos seguintes processos de recuperação:</span><span class="sxs-lookup"><span data-stu-id="188a9-136">**Disk Commander** lets you recover and repair disk partitions or volumes by using one of the following recovery processes:</span></span>

-   <span data-ttu-id="188a9-137">Restaurar o registro mestre de inicialização (MBR)</span><span class="sxs-lookup"><span data-stu-id="188a9-137">Restore the master boot record (MBR)</span></span>

-   <span data-ttu-id="188a9-138">Recuperar um ou mais volumes perdidos</span><span class="sxs-lookup"><span data-stu-id="188a9-138">Recover one or more lost volumes</span></span>

-   <span data-ttu-id="188a9-139">Restaurar tabelas de partição do backup do **Disk Commander**</span><span class="sxs-lookup"><span data-stu-id="188a9-139">Restore partition tables from **Disk Commander** backup</span></span>

-   <span data-ttu-id="188a9-140">Salvar tabelas de partição no backup do **Disk Commander**</span><span class="sxs-lookup"><span data-stu-id="188a9-140">Save partition tables to **Disk Commander** backup</span></span>

<span data-ttu-id="188a9-141">**Aviso**  Recomendamos que você faça backup de um disco antes de usar o **Disk Commander** para repará-lo.</span><span class="sxs-lookup"><span data-stu-id="188a9-141">**Warning** We recommend that you back up a disk before you use **Disk Commander** to repair it.</span></span> <span data-ttu-id="188a9-142">Usando o **Disk Commander**, você pode danificar volumes e torná-los inacessíveis.</span><span class="sxs-lookup"><span data-stu-id="188a9-142">By using **Disk Commander**, you can potentially damage volumes and make them inaccessible.</span></span> <span data-ttu-id="188a9-143">Além disso, as alterações em um volume podem afetar outros volumes porque volumes em um disco compartilham uma tabela de partição.</span><span class="sxs-lookup"><span data-stu-id="188a9-143">Additionally, changes to one volume can affect other volumes because volumes on a disk share a partition table.</span></span>

 

<span data-ttu-id="188a9-144">**Observação**  Não há suporte para a recuperação de discos dinâmicos com o DaRT.</span><span class="sxs-lookup"><span data-stu-id="188a9-144">**Note** The recovery of dynamic disks with DaRT is not supported.</span></span>

 

### <span data-ttu-id="188a9-145">Apagamento de disco</span><span class="sxs-lookup"><span data-stu-id="188a9-145">Disk Wipe</span></span>

<span data-ttu-id="188a9-146">Você pode usar **apagamento de disco** para excluir todos os dados de um disco ou volume, até mesmo os dados que são deixados para trás após a reformatação de uma unidade de disco rígido.</span><span class="sxs-lookup"><span data-stu-id="188a9-146">You can use **Disk Wipe** to delete all data from a disk or volume, even the data that is left behind after you reformat a hard disk drive.</span></span> <span data-ttu-id="188a9-147">O **apagamento de disco** permite que você selecione entre uma substituição de passagem única ou uma substituição de quatro passagens, que atende aos padrões atuais do departamento de defesa dos EUA.</span><span class="sxs-lookup"><span data-stu-id="188a9-147">**Disk Wipe** lets you select from either a single-pass overwrite or a four-pass overwrite, which meets current U.S. Department of Defense standards.</span></span>

<span data-ttu-id="188a9-148">**Aviso**  Após limpar um disco ou volume, você não pode recuperar os dados.</span><span class="sxs-lookup"><span data-stu-id="188a9-148">**Warning** After wiping a disk or volume, you cannot recover the data.</span></span> <span data-ttu-id="188a9-149">Verifique o tamanho e o rótulo de um volume antes de apagá-lo.</span><span class="sxs-lookup"><span data-stu-id="188a9-149">Verify the size and label of a volume before erasing it.</span></span>

 

### <span data-ttu-id="188a9-150">Explorador</span><span class="sxs-lookup"><span data-stu-id="188a9-150">Explorer</span></span>

<span data-ttu-id="188a9-151">A ferramenta do **Explorer** permite que você navegue no sistema de arquivos do computador e em compartilhamentos de rede para que você possa remover dados importantes que o usuário armazenou na unidade local antes de tentar reparar ou refazer a imagem do computador.</span><span class="sxs-lookup"><span data-stu-id="188a9-151">The **Explorer** tool lets you browse the computer’s file system and network shares so that you can remove important data that the user stored on the local drive before you try to repair or reimage the computer.</span></span> <span data-ttu-id="188a9-152">E, como você pode mapear letras de unidade para compartilhamentos de rede, é fácil copiar e mover arquivos do computador para a rede para que ele possa ser restaurado ou da rede para o computador.</span><span class="sxs-lookup"><span data-stu-id="188a9-152">And because you can map drive letters to network shares, you can easily copy and move files from the computer to the network for safekeeping or from the network to the computer to restore them.</span></span>

### <span data-ttu-id="188a9-153">Restauração de arquivos</span><span class="sxs-lookup"><span data-stu-id="188a9-153">File Restore</span></span>

<span data-ttu-id="188a9-154">A **restauração de arquivos** permite que você tente restaurar arquivos que foram excluídos acidentalmente ou que eram muito grandes para caber na lixeira.</span><span class="sxs-lookup"><span data-stu-id="188a9-154">**File Restore** lets you try to restore files that were accidentally deleted or that were too big to fit in the Recycle Bin.</span></span> <span data-ttu-id="188a9-155">A **restauração de arquivos** não está limitada a volumes de disco regulares, mas pode localizar e restaurar arquivos em volumes perdidos ou em volumes criptografados pelo BitLocker.</span><span class="sxs-lookup"><span data-stu-id="188a9-155">**File Restore** is not limited to regular disk volumes, but can find and restore files on lost volumes or on volumes that are encrypted by BitLocker.</span></span>

<span data-ttu-id="188a9-156">**Observação**  Não há suporte para a recuperação de discos dinâmicos com o DaRT.</span><span class="sxs-lookup"><span data-stu-id="188a9-156">**Note** The recovery of dynamic disks with DaRT is not supported.</span></span>

 

### <span data-ttu-id="188a9-157">Pesquisa de arquivos</span><span class="sxs-lookup"><span data-stu-id="188a9-157">File Search</span></span>

<span data-ttu-id="188a9-158">Antes de recriar uma cópia de um computador, recuperar arquivos do disco rígido local é importante, especialmente quando o usuário pode não ter feito backup ou armazenado os arquivos em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="188a9-158">Before reimaging a computer, recovering files from the local hard disk is important, especially when the user might not have backed up or stored the files elsewhere.</span></span>

<span data-ttu-id="188a9-159">A ferramenta de **pesquisa** abre uma janela de **pesquisa de arquivos** que você pode usar para localizar documentos quando você não conhece o caminho do arquivo ou para Pesquisar tipos gerais de arquivos em todos os discos rígidos locais.</span><span class="sxs-lookup"><span data-stu-id="188a9-159">The **Search** tool opens a **File Search** window that you can use to find documents when you do not know the file path or to search for general kinds of files across all local hard disks.</span></span> <span data-ttu-id="188a9-160">Você pode procurar padrões de nome de arquivo específicos em caminhos específicos.</span><span class="sxs-lookup"><span data-stu-id="188a9-160">You can search for specific file-name patterns in specific paths.</span></span> <span data-ttu-id="188a9-161">Você também pode limitar os resultados a um intervalo de datas ou intervalo de tamanho.</span><span class="sxs-lookup"><span data-stu-id="188a9-161">You can also limit results to a date range or size range.</span></span>

### <span data-ttu-id="188a9-162">Desinstalação de hotfix</span><span class="sxs-lookup"><span data-stu-id="188a9-162">Hotfix Uninstall</span></span>

<span data-ttu-id="188a9-163">O **Assistente de desinstalação de hotfix** permite que você remova hotfixes ou Service Packs do sistema operacional Windows no computador que está reparando.</span><span class="sxs-lookup"><span data-stu-id="188a9-163">The **Hotfix Uninstall Wizard** lets you remove hotfixes or service packs from the Windows operating system on the computer that you are repairing.</span></span> <span data-ttu-id="188a9-164">Use essa ferramenta quando um hotfix ou Service Pack for suspeito para impedir que o sistema operacional seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="188a9-164">Use this tool when a hotfix or service pack is suspected in preventing the operating system from starting.</span></span>

<span data-ttu-id="188a9-165">Recomendamos que você desinstale apenas um hotfix de cada vez, mesmo que a ferramenta permita que você desinstale mais de um.</span><span class="sxs-lookup"><span data-stu-id="188a9-165">We recommend that you uninstall only one hotfix at a time, even though the tool lets you uninstall more than one.</span></span>

<span data-ttu-id="188a9-166">**Importante**  Os programas que foram instalados ou atualizados após a instalação de um hotfix podem não funcionar corretamente após a desinstalação de um hotfix.</span><span class="sxs-lookup"><span data-stu-id="188a9-166">**Important** Programs that were installed or updated after a hotfix was installed might not work correctly after you uninstall a hotfix.</span></span>

 

### <span data-ttu-id="188a9-167">Locksmith</span><span class="sxs-lookup"><span data-stu-id="188a9-167">Locksmith</span></span>

<span data-ttu-id="188a9-168">O **Assistente locksmith** permite definir ou alterar a senha de qualquer conta local no sistema operacional Windows que você está analisando ou reparando.</span><span class="sxs-lookup"><span data-stu-id="188a9-168">The **Locksmith Wizard** lets you set or change the password for any local account on the Windows operating system that you are analyzing or repairing.</span></span> <span data-ttu-id="188a9-169">Você não precisa saber a senha atual.</span><span class="sxs-lookup"><span data-stu-id="188a9-169">You do not have to know the current password.</span></span> <span data-ttu-id="188a9-170">No entanto, a senha definida deve ser compatível com os requisitos definidos por um objeto de política de grupo local.</span><span class="sxs-lookup"><span data-stu-id="188a9-170">However, the password that you set must comply with any requirements that are defined by a local Group Policy Object.</span></span> <span data-ttu-id="188a9-171">Isso inclui o tamanho e a complexidade da senha.</span><span class="sxs-lookup"><span data-stu-id="188a9-171">This includes password length and complexity.</span></span>

<span data-ttu-id="188a9-172">Você pode usar **locksmith** quando a senha de uma conta local, como a conta de administrador local, for desconhecida.</span><span class="sxs-lookup"><span data-stu-id="188a9-172">You can use **Locksmith** when the password for a local account, such as the local Administrator account, is unknown.</span></span> <span data-ttu-id="188a9-173">Você não pode usar **locksmith** para definir senhas para contas de domínio.</span><span class="sxs-lookup"><span data-stu-id="188a9-173">You cannot use **Locksmith** to set passwords for domain accounts.</span></span>

### <span data-ttu-id="188a9-174">Editor do registro</span><span class="sxs-lookup"><span data-stu-id="188a9-174">Registry Editor</span></span>

<span data-ttu-id="188a9-175">Você pode usar o **Editor do registro** para acessar e alterar o registro do sistema operacional Windows que você está analisando ou reparando.</span><span class="sxs-lookup"><span data-stu-id="188a9-175">You can use **Registry Editor** to access and change the registry of the Windows operating system that you are analyzing or repairing.</span></span> <span data-ttu-id="188a9-176">Isso inclui a adição, a remoção e a edição de chaves e valores e a importação de arquivos do registro (. reg).</span><span class="sxs-lookup"><span data-stu-id="188a9-176">This includes adding, removing, and editing keys and values, and importing registry (.reg) files.</span></span>

<span data-ttu-id="188a9-177">**Aviso**  Sérios problemas podem ocorrer se você alterar o registro incorretamente usando o **Editor do registro**.</span><span class="sxs-lookup"><span data-stu-id="188a9-177">**Warning** Serious problems can occur if you change the registry incorrectly by using **Registry Editor**.</span></span> <span data-ttu-id="188a9-178">Esses problemas podem exigir a reinstalação do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="188a9-178">These problems might require you to reinstall the operating system.</span></span> <span data-ttu-id="188a9-179">Antes de fazer alterações no registro, você deve fazer backup de todos os dados importantes do computador.</span><span class="sxs-lookup"><span data-stu-id="188a9-179">Before you make changes to the registry, you should back up any valued data on the computer.</span></span> <span data-ttu-id="188a9-180">Altere o registro por sua conta e risco.</span><span class="sxs-lookup"><span data-stu-id="188a9-180">Change the registry at your own risk.</span></span>

 

### <span data-ttu-id="188a9-181">Verificação de SFC</span><span class="sxs-lookup"><span data-stu-id="188a9-181">SFC Scan</span></span>

<span data-ttu-id="188a9-182">A ferramenta de **verificação Sfc** inicia o **Assistente de reparo de arquivos do sistema** e permite reparar arquivos do sistema que impedem o início do sistema operacional Windows instalado.</span><span class="sxs-lookup"><span data-stu-id="188a9-182">The **SFC Scan** tool starts the **System File Repair Wizard** and lets you repair system files that are preventing the installed Windows operating system from starting.</span></span> <span data-ttu-id="188a9-183">O **Assistente de reparo de arquivos do sistema** pode reparar automaticamente os arquivos de sistema corrompidos ou ausentes, ou pode notificá-lo antes que ele realize qualquer reparo.</span><span class="sxs-lookup"><span data-stu-id="188a9-183">The **System File Repair Wizard** can automatically repair system files that are corrupted or missing, or it can prompt you before it performs any repairs.</span></span>

### <span data-ttu-id="188a9-184">Assistente de solução</span><span class="sxs-lookup"><span data-stu-id="188a9-184">Solution Wizard</span></span>

<span data-ttu-id="188a9-185">O **Assistente de solução** apresenta uma série de perguntas e, em seguida, recomenda a melhor ferramenta para a situação, com base nas suas respostas.</span><span class="sxs-lookup"><span data-stu-id="188a9-185">The **Solution Wizard** presents a series of questions and then recommends the best tool for the situation, based on your answers.</span></span> <span data-ttu-id="188a9-186">Este assistente ajuda você a determinar qual ferramenta usar quando você não estiver familiarizado com as ferramentas do DaRT.</span><span class="sxs-lookup"><span data-stu-id="188a9-186">This wizard helps you determine which tool to use when you are not familiar with the tools in DaRT.</span></span>

### <span data-ttu-id="188a9-187">Configuração de TCP/IP</span><span class="sxs-lookup"><span data-stu-id="188a9-187">TCP/IP Config</span></span>

<span data-ttu-id="188a9-188">Quando você inicializa um computador com problema no DaRT, ele é definido para obter automaticamente a sua configuração de TCP/IP (endereço IP e servidor DNS) do protocolo DHCP (protocolo de configuração dinâmica de hosts).</span><span class="sxs-lookup"><span data-stu-id="188a9-188">When you boot a problem computer into DaRT, it is set to automatically obtain its TCP/IP configuration (IP address and DNS server) from Dynamic Host Configuration Protocol (DHCP).</span></span> <span data-ttu-id="188a9-189">Se o DHCP estiver indisponível, você poderá configurar manualmente o TCP/IP usando a ferramenta de **configuração TCP/IP** .</span><span class="sxs-lookup"><span data-stu-id="188a9-189">If DHCP is unavailable, you can manually configure TCP/IP by using the **TCP/IP Config** tool.</span></span> <span data-ttu-id="188a9-190">Primeiro, selecione um adaptador de rede e, em seguida, configure o endereço IP e o servidor DNS para esse adaptador.</span><span class="sxs-lookup"><span data-stu-id="188a9-190">You first select a network adapter, and then configure the IP address and DNS server for that adapter.</span></span>

## <span data-ttu-id="188a9-191">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="188a9-191">Related topics</span></span>


[<span data-ttu-id="188a9-192">Introdução ao DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="188a9-192">Getting Started with DaRT 8.0</span></span>](getting-started-with-dart-80-dart-8.md)

 

 





