---
title: Solução de problemas de instalação do MBAM 2.5
description: Apresentando como solucionar problemas de instalação do MBAM 2,5.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: ed56a87496e09601c44028b7f948eda39143e8c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796106"
---
# <span data-ttu-id="18e86-103">Solução de problemas de instalação do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="18e86-103">Troubleshooting MBAM 2.5 installation problems</span></span>

<span data-ttu-id="18e86-104">Este artigo apresenta como solucionar problemas de instalação do Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 em uma configuração autônoma.</span><span class="sxs-lookup"><span data-stu-id="18e86-104">This article introduces how to troubleshoot Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 installation issues in a standalone configuration.</span></span>

## <span data-ttu-id="18e86-105">Fazendo referência a arquivos de log do MBAM para solução de problemas</span><span class="sxs-lookup"><span data-stu-id="18e86-105">Referring MBAM log files for troubleshooting</span></span>

<span data-ttu-id="18e86-106">O MBAM inclui log para instalação do servidor, instalação do cliente e eventos.</span><span class="sxs-lookup"><span data-stu-id="18e86-106">MBAM includes logging for server installation, client installation, and events.</span></span> <span data-ttu-id="18e86-107">Este registro em log deve ser consultado para solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="18e86-107">This logging should be referred to for troubleshooting.</span></span> 
 
### <span data-ttu-id="18e86-108">Arquivos de log de instalação do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="18e86-108">MBAM server installation log files</span></span>

<span data-ttu-id="18e86-109">MBAMServerSetup.exe gera os seguintes arquivos de log na pasta% Temp% do usuário durante a instalação do MBAM:</span><span class="sxs-lookup"><span data-stu-id="18e86-109">MBAMServerSetup.exe generates the following log files in the user’s %temp% folder during MBAM installation:</span></span><br /> **<span data-ttu-id="18e86-110">Microsoft_BitLocker_Administration_and_Monitoring_<14 números>. log</span><span class="sxs-lookup"><span data-stu-id="18e86-110">Microsoft_BitLocker_Administration_and_Monitoring_<14 numbers>.log</span></span>**

<span data-ttu-id="18e86-111">MBAMServerSetup.exe registra as ações que foram feitas durante a instalação do MBAM e o recurso MBAM Server Feature:</span><span class="sxs-lookup"><span data-stu-id="18e86-111">MBAMServerSetup.exe logs the actions that were taken during MBAM setup and MBAM server feature installation:</span></span><br /> **<span data-ttu-id="18e86-112">Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers # C1_0_MBAMServer.msi. log</span><span class="sxs-lookup"><span data-stu-id="18e86-112">Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers>_0_MBAMServer.msi.log</span></span>**

<span data-ttu-id="18e86-113">MBAMServerSetup.exe registra ações adicionais que foram executadas durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="18e86-113">MBAMServerSetup.exe logs additional actions that were taken during installation.</span></span>

### <span data-ttu-id="18e86-114">Arquivo de log de instalação do cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="18e86-114">MBAM client installation log file</span></span>

<span data-ttu-id="18e86-115">A instalação do cliente é gravada no seguinte arquivo de log na pasta% temp% (ou em um local personalizado, dependendo de como o cliente foi instalado):</span><span class="sxs-lookup"><span data-stu-id="18e86-115">The client installation is recorded in the following log file in the %temp% folder (or a custom location, depending on how the client was installed):</span></span> <br />**<span data-ttu-id="18e86-116">MSI \<five random characters\> . log</span><span class="sxs-lookup"><span data-stu-id="18e86-116">MSI\<five random characters\>.log</span></span>**

<span data-ttu-id="18e86-117">Esse log contém as ações que são executadas durante a instalação do cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="18e86-117">This log contains the actions that are taken during MBAM client installation.</span></span>
 
### <span data-ttu-id="18e86-118">Canal de log de eventos do cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="18e86-118">MBAM client event-logging channel</span></span>

<span data-ttu-id="18e86-119">O MBAM tem canais de log de eventos separados.</span><span class="sxs-lookup"><span data-stu-id="18e86-119">MBAM has separate event-logging channels.</span></span> <span data-ttu-id="18e86-120">Os arquivos de log do administrador, analítico e operacional estão localizados no Visualizador de eventos, em **logs de aplicativos e serviços**  >  **Microsoft**  >  **Windows**  >  **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="18e86-120">The Admin, Analytical, and Operational log files are located in Event Viewer, under **Application and Services Logs** > **Microsoft** > **Windows** > **MBAM**.</span></span>

<span data-ttu-id="18e86-121">A tabela a seguir fornece uma breve descrição de cada log de eventos.</span><span class="sxs-lookup"><span data-stu-id="18e86-121">The following table provides a brief description of each event log.</span></span>
 
|<span data-ttu-id="18e86-122">Log de eventos</span><span class="sxs-lookup"><span data-stu-id="18e86-122">Event log</span></span>| <span data-ttu-id="18e86-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="18e86-123">Description</span></span>|
|----------|-------|
|<span data-ttu-id="18e86-124">Microsoft-Windows-MBAM/administrador</span><span class="sxs-lookup"><span data-stu-id="18e86-124">Microsoft-Windows-MBAM/Admin</span></span>|  <span data-ttu-id="18e86-125">Contém mensagens de erro</span><span class="sxs-lookup"><span data-stu-id="18e86-125">Contains error messages</span></span>|
|<span data-ttu-id="18e86-126">Microsoft-Windows-MBAM/analítica</span><span class="sxs-lookup"><span data-stu-id="18e86-126">Microsoft-Windows-MBAM/Analytic</span></span>|   <span data-ttu-id="18e86-127">Contém informações de registro avançado</span><span class="sxs-lookup"><span data-stu-id="18e86-127">Contains advanced logging information</span></span>|
|<span data-ttu-id="18e86-128">Microsoft-Windows-MBAM/operacional</span><span class="sxs-lookup"><span data-stu-id="18e86-128">Microsoft-Windows-MBAM/Operational</span></span>|    <span data-ttu-id="18e86-129">Contém mensagens de êxito</span><span class="sxs-lookup"><span data-stu-id="18e86-129">Contains success messages</span></span>|

### <span data-ttu-id="18e86-130">Canal de log de eventos do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="18e86-130">MBAM server event-logging channel</span></span>

<span data-ttu-id="18e86-131">Os arquivos de log estão localizados em Visualizador de eventos, em **logs de aplicativos e serviços**  >  **Microsoft**  >  **Windows**  >  **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="18e86-131">The log files are located in Event Viewer, under **Application and Services Logs** > **Microsoft** > **Windows** > **MBAM**.</span></span> <span data-ttu-id="18e86-132">A tabela a seguir inclui logs de eventos do servidor que foram introduzidos no MBAM 2,5:</span><span class="sxs-lookup"><span data-stu-id="18e86-132">The following table includes server event logs that were introduced in MBAM 2.5:</span></span>

|<span data-ttu-id="18e86-133">Log de eventos</span><span class="sxs-lookup"><span data-stu-id="18e86-133">Event log</span></span>| <span data-ttu-id="18e86-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="18e86-134">Description</span></span>|
|--------|-------------|
|<span data-ttu-id="18e86-135">Microsoft-Windows-MBAM/administrador</span><span class="sxs-lookup"><span data-stu-id="18e86-135">Microsoft-Windows-MBAM/Admin</span></span>|  <span data-ttu-id="18e86-136">Contém mensagens de erro</span><span class="sxs-lookup"><span data-stu-id="18e86-136">Contains error messages</span></span>|
|<span data-ttu-id="18e86-137">Microsoft-Windows-MBAM/analítica</span><span class="sxs-lookup"><span data-stu-id="18e86-137">Microsoft-Windows-MBAM/Analytic</span></span>|   <span data-ttu-id="18e86-138">Contém informações de registro avançado</span><span class="sxs-lookup"><span data-stu-id="18e86-138">Contains advanced logging information</span></span>|
|<span data-ttu-id="18e86-139">Microsoft-Windows-MBAM/operacional</span><span class="sxs-lookup"><span data-stu-id="18e86-139">Microsoft-Windows-MBAM/Operational</span></span>|    <span data-ttu-id="18e86-140">Contém mensagens de êxito</span><span class="sxs-lookup"><span data-stu-id="18e86-140">Contains success messages</span></span>|

### <span data-ttu-id="18e86-141">Logs de serviços Web do MBAM</span><span class="sxs-lookup"><span data-stu-id="18e86-141">MBAM web service logs</span></span>

<span data-ttu-id="18e86-142">Cada log de serviço Web do MBAM grava as informações de registro em um arquivo SVCLOG.</span><span class="sxs-lookup"><span data-stu-id="18e86-142">Each MBAM web service log writes logging information to an SVCLOG file.</span></span> <span data-ttu-id="18e86-143">Por padrão, cada serviço Web grava o arquivo de rastreamento em uma pasta que usa seu nome na pasta C:\inetpub\Microsoft BitLocker Management Solution\Logs.</span><span class="sxs-lookup"><span data-stu-id="18e86-143">By default, each web service writes the trace file under a folder that uses its name in the C:\inetpub\Microsoft BitLocker Management Solution\Logs folder.</span></span>

<span data-ttu-id="18e86-144">Você pode usar a ferramenta Visualizador de rastreamento de serviço (parte do Microsoft Visual Studio) para analisar os rastreamentos do svclog.</span><span class="sxs-lookup"><span data-stu-id="18e86-144">You can use the service trace viewer tool (part of Microsoft Visual Studio) to review the svclog traces.</span></span>

## <span data-ttu-id="18e86-145">Solução de problemas de criptografia e emissão de relatórios</span><span class="sxs-lookup"><span data-stu-id="18e86-145">Troubleshooting encryption and reporting issues</span></span>

<span data-ttu-id="18e86-146">Esta seção contém informações de solução de problemas para funcionalidade do servidor, funcionalidade do cliente, configurações e problemas conhecidos:</span><span class="sxs-lookup"><span data-stu-id="18e86-146">This section contains troubleshooting information for server functionality, client functionality, configuration settings, and known issues:</span></span>
 
### <span data-ttu-id="18e86-147">Instalação do cliente do MBAM, configurações da política de grupo</span><span class="sxs-lookup"><span data-stu-id="18e86-147">MBAM client installation, Group Policy settings</span></span>

<span data-ttu-id="18e86-148">Determine se o agente do MBAM está instalado no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="18e86-148">Determine whether the MBAM agent is installed on the client computer.</span></span> <span data-ttu-id="18e86-149">Quando o MBAM é instalado, ele cria um serviço denominado serviço de cliente de gerenciamento BitLocker.</span><span class="sxs-lookup"><span data-stu-id="18e86-149">When MBAM is installed, it creates a service that is named BitLocker Management Client Service.</span></span> <span data-ttu-id="18e86-150">Este serviço é configurado para iniciar automaticamente.</span><span class="sxs-lookup"><span data-stu-id="18e86-150">This service is configured to start automatically.</span></span> <span data-ttu-id="18e86-151">Determine se o serviço está em execução.</span><span class="sxs-lookup"><span data-stu-id="18e86-151">Determine whether the service is running.</span></span>

<span data-ttu-id="18e86-152">Verifique se as configurações de política de grupo do MBAM são aplicadas no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="18e86-152">Make sure that MBAM Group Policy settings are applied on the client computer.</span></span> <span data-ttu-id="18e86-153">A seguinte subchave do registro será criada se as configurações de política de grupo tiverem sido aplicadas no computador cliente: **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**</span><span class="sxs-lookup"><span data-stu-id="18e86-153">The following registry subkey is created if the Group Policy settings were applied on the client computer: **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**</span></span>

<span data-ttu-id="18e86-154">Verifique se essa chave existe e se está preenchida usando valores por configurações de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="18e86-154">Verify that this key exists and is populated by using values per Group Policy settings.</span></span>

### <span data-ttu-id="18e86-155">Agente MBAM no período de atraso inicial</span><span class="sxs-lookup"><span data-stu-id="18e86-155">MBAM Agent in the initial delay period</span></span>

<span data-ttu-id="18e86-156">O cliente MBAM não inicia a operação imediatamente após a instalação.</span><span class="sxs-lookup"><span data-stu-id="18e86-156">The MBAM client doesn't start the operation immediately after installation.</span></span> <span data-ttu-id="18e86-157">Há um atraso inicial aleatório de 1 – 18 minutos antes de o agente MBAM iniciar a operação.</span><span class="sxs-lookup"><span data-stu-id="18e86-157">There is an initial random delay of 1–18 minutes before the MBAM Agent starts its operation.</span></span> <span data-ttu-id="18e86-158">Além do atraso inicial, há um atraso de pelo menos 90 minutos.</span><span class="sxs-lookup"><span data-stu-id="18e86-158">In addition to the initial delay, there is a delay of at least 90 minutes.</span></span> <span data-ttu-id="18e86-159">(O atraso depende das configurações de política de grupo que estão definidas para a frequência de verificação do status do cliente.) Portanto, o atraso total antes da operação de início do cliente é a demora de *inicialização aleatória*atraso da  +  *frequência de verificação do cliente*.</span><span class="sxs-lookup"><span data-stu-id="18e86-159">(The delay depends on the Group Policy settings that are configured for the frequency of checking the client status.) Therefore, the total delay before a client starts operation is *random startup delay* + *client checking frequency delay*.</span></span>

<span data-ttu-id="18e86-160">Se os logs de eventos de administração e operacionais estiverem em branco, o cliente ainda não iniciou a operação e estará no período de atraso mencionado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="18e86-160">If the Operational and Admin event logs are blank, the client has not started the operation yet and is in the delay period that was mentioned earlier.</span></span> <span data-ttu-id="18e86-161">Se você quiser ignorar o atraso, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="18e86-161">If you want to bypass the delay, follow these steps:</span></span>
 
1. <span data-ttu-id="18e86-162">Parar o serviço de serviço de cliente de gerenciamento BitLocker.</span><span class="sxs-lookup"><span data-stu-id="18e86-162">Stop the BitLocker Management Client Service service.</span></span>

2. <span data-ttu-id="18e86-163">Na subchave do registro do **HKEY_LOCAL_MACHINE \software\microsoft\mbam** , crie o valor do registro **NoStartupDelay** , defina seu tipo como **REG_DWORD**e, em seguida, defina seu valor como **1**.</span><span class="sxs-lookup"><span data-stu-id="18e86-163">Under the **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM** registry subkey, create the **NoStartupDelay** registry value, set its type to **REG_DWORD**, and then set its value to **1**.</span></span>

3. <span data-ttu-id="18e86-164">Em **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**, defina os valores **ClientWakeupFrequency** e **StatusReportingFrequency** como **1**.</span><span class="sxs-lookup"><span data-stu-id="18e86-164">Under **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**, set the **ClientWakeupFrequency** and **StatusReportingFrequency** values to **1**.</span></span> <span data-ttu-id="18e86-165">Esses valores retornarão às configurações originais depois que as atualizações de política de grupo estiverem no computador.</span><span class="sxs-lookup"><span data-stu-id="18e86-165">These values will revert to their original settings after Group Policy updates are on the computer.</span></span>

4. <span data-ttu-id="18e86-166">Inicie o serviço de serviço de cliente de gerenciamento BitLocker.</span><span class="sxs-lookup"><span data-stu-id="18e86-166">Start the BitLocker Management Client Service service.</span></span>

<span data-ttu-id="18e86-167">Depois que o serviço for iniciado, se você fizer logon localmente no computador e não houver erros, você deve receber uma solicitação para criptografar o computador dentro de um minuto.</span><span class="sxs-lookup"><span data-stu-id="18e86-167">After the service starts, if you log in locally on the computer and there are no errors, you should receive a request to encrypt the computer within one minute.</span></span> <span data-ttu-id="18e86-168">Se você não receber uma solicitação, analise os logs de administração do MBAM para obter as entradas de erro.</span><span class="sxs-lookup"><span data-stu-id="18e86-168">If you do not receive a request, you should review the MBAM Admin logs for any error entries.</span></span>

### <span data-ttu-id="18e86-169">O computador não tem um dispositivo TPM ou o dispositivo TPM não está habilitado no BIOS</span><span class="sxs-lookup"><span data-stu-id="18e86-169">Computer does not have a TPM device, or the TPM device is not enabled in the BIOS</span></span>

<span data-ttu-id="18e86-170">Examine o log de eventos de administrador do MBAM.</span><span class="sxs-lookup"><span data-stu-id="18e86-170">Review the MBAM Admin event log.</span></span> <span data-ttu-id="18e86-171">Você verá uma entrada de evento semelhante à seguinte no log de eventos de administração do MBAM:</span><span class="sxs-lookup"><span data-stu-id="18e86-171">You will see an event entry that resembles the following in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 12:31:10 PM
    Event ID:      9
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    The TPM hardware is missing.
    TPM is needed to encrypt the operating system drive with any TPM protector.

<span data-ttu-id="18e86-172">Abra o gerenciamento TPM (TPM. msc) e verifique se o computador tem um dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="18e86-172">Open TPM Management (tpm.msc), and check whether the computer has a TPM device.</span></span> <span data-ttu-id="18e86-173">Se o TPM. msc não mostrar um dispositivo, abra o Gerenciador de dispositivos (devmgmt. msc) e verifique se há um módulo de plataforma confiável em dispositivos de segurança.</span><span class="sxs-lookup"><span data-stu-id="18e86-173">If tpm.msc does not show a device, open Device Manager (devmgmt.msc), and check for a Trusted Platform Module under Security Devices.</span></span> <span data-ttu-id="18e86-174">Se você não vir um dispositivo de módulo de plataforma confiável, isso pode ser verdade por um dos seguintes motivos:</span><span class="sxs-lookup"><span data-stu-id="18e86-174">If you do not see a Trusted Platform Module device, this might be true for one of the following reasons:</span></span>

* <span data-ttu-id="18e86-175">Seu sistema não tem um dispositivo TPM/segurança (Trusted Platform Module).</span><span class="sxs-lookup"><span data-stu-id="18e86-175">Your system doesn't have a Trusted Platform Module (TPM/Security) device.</span></span>

* <span data-ttu-id="18e86-176">O dispositivo TPM está desabilitado no BIOS.</span><span class="sxs-lookup"><span data-stu-id="18e86-176">The TPM device is disabled in the BIOS.</span></span>

* <span data-ttu-id="18e86-177">O dispositivo TPM está habilitado no BIOS, mas o gerenciamento do dispositivo TPM da configuração do sistema operacional está desabilitado no BIOS.</span><span class="sxs-lookup"><span data-stu-id="18e86-177">TPM Device is enabled in the BIOS, but management of the TPM device from the operating system setting is disabled in the BIOS.</span></span>

* <span data-ttu-id="18e86-178">Você não está usando um driver da Microsoft para o dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="18e86-178">You aren't using a Microsoft driver for the TPM device.</span></span> <span data-ttu-id="18e86-179">Examine os dispositivos listados no Gerenciador de dispositivos para identificar o driver de dispositivo TPM da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="18e86-179">Review the devices that are listed in device manager to identify the Microsoft TPM device driver.</span></span>

<span data-ttu-id="18e86-180">Se o dispositivo TPM não estiver usando o driver C:\Windows\System32\tpm.sys, você deverá atualizar o driver selecionando o arquivo C:\Windows\Inf\tpm.inf.</span><span class="sxs-lookup"><span data-stu-id="18e86-180">If the TPM device is not using the C:\Windows\System32\tpm.sys driver, you should update the driver by selecting the C:\Windows\Inf\tpm.inf file.</span></span>

### <span data-ttu-id="18e86-181">O computador não tem uma partição de sistema válida</span><span class="sxs-lookup"><span data-stu-id="18e86-181">Computer does not have a valid SYSTEM partition</span></span>

<span data-ttu-id="18e86-182">Examine o log de eventos de administrador do MBAM.</span><span class="sxs-lookup"><span data-stu-id="18e86-182">Review the MBAM Admin event log.</span></span> <span data-ttu-id="18e86-183">Você verá uma entrada de evento semelhante à seguinte no log de eventos de administração do MBAM:</span><span class="sxs-lookup"><span data-stu-id="18e86-183">You will see an event entry that resembles the following in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:37 AM
    Event ID:      8
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTESTVM.xtremelabs.com
    Description:
    The system volume is missing.
    SystemVolume is needed to encrypt the operating system drive.

<span data-ttu-id="18e86-184">O BitLocker exige uma partição de sistema para habilitar a criptografia ([criptografia de unidade de disco BitLocker no Windows 7: perguntas frequentes](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).</span><span class="sxs-lookup"><span data-stu-id="18e86-184">BitLocker requires a SYSTEM partition to enable encryption ([BitLocker Drive Encryption in Windows 7: Frequently Asked Questions](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).</span></span>

<span data-ttu-id="18e86-185">O MBAM não cria a partição do sistema automaticamente.</span><span class="sxs-lookup"><span data-stu-id="18e86-185">MBAM doesn't create the system partition automatically.</span></span> <span data-ttu-id="18e86-186">Você pode usar o utilitário de preparação de unidade BitLocker (bdehdcfg.exe) para criar a partição do sistema e mover os arquivos de inicialização necessários.</span><span class="sxs-lookup"><span data-stu-id="18e86-186">You can use the BitLocker drive preparation utility (bdehdcfg.exe) to create the system partition and move the required startup files.</span></span>

<span data-ttu-id="18e86-187">Por exemplo, você pode usar o comando **% windir% \system32\bdeHdCfg.exe-Target default-size 300 – Quiet** para preparar a unidade silenciosamente antes de implantar o MBAM para criptografar as unidades.</span><span class="sxs-lookup"><span data-stu-id="18e86-187">For example, you can use the command **%windir%\system32\bdeHdCfg.exe -target default -size 300 –quiet** to prepare the drive silently before you deploy MBAM to encrypt the drives.</span></span> <span data-ttu-id="18e86-188">Isso requer uma reinicialização.</span><span class="sxs-lookup"><span data-stu-id="18e86-188">This requires a restart.</span></span> <span data-ttu-id="18e86-189">Você também pode criar um script para a ação caso isso seja necessário.</span><span class="sxs-lookup"><span data-stu-id="18e86-189">You can also script the action if this is required.</span></span> <span data-ttu-id="18e86-190">O documento a seguir descreve a ferramenta de preparação de unidade de disco BitLocker:</span><span class="sxs-lookup"><span data-stu-id="18e86-190">The following document describes the BitLocker Drive Preparation Tool:</span></span>

[<span data-ttu-id="18e86-191">Descrição da ferramenta de preparação de unidade de disco BitLocker</span><span class="sxs-lookup"><span data-stu-id="18e86-191">Description of the BitLocker Drive Preparation Tool</span></span>](https://support.microsoft.com/help/933246)

### <span data-ttu-id="18e86-192">As unidades não estão formatadas para ter um sistema de arquivos compatível</span><span class="sxs-lookup"><span data-stu-id="18e86-192">Drives are not formatted to have a compatible file system</span></span>

<span data-ttu-id="18e86-193">Consulte o [artigo do TechNet para requisitos do sistema de arquivos para o BitLocker](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements).</span><span class="sxs-lookup"><span data-stu-id="18e86-193">See the [TechNet article for file system requirements for BitLocker](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements).</span></span>

### <span data-ttu-id="18e86-194">Conflito de política de grupo</span><span class="sxs-lookup"><span data-stu-id="18e86-194">Group Policy conflict</span></span>

<span data-ttu-id="18e86-195">Você verá uma entrada de evento semelhante à seguinte no log de eventos de administração do MBAM:</span><span class="sxs-lookup"><span data-stu-id="18e86-195">You will see an event entry that resembles the following in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/25/2013 9:27:58 PM
    Event ID:      22
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Detected Fixed Data Drive volume encryption policies conflict.
    Check BitLocker and MBAM policies related to FDD drive protectors.

<span data-ttu-id="18e86-196">Verifique as configurações da política de grupo para garantir que você não tenha uma configuração conflitante entre as configurações da política de grupo do MBAM.</span><span class="sxs-lookup"><span data-stu-id="18e86-196">Verify your Group Policy settings to make sure that you do not have a conflicting setting among the MBAM Group Policy settings.</span></span>

<span data-ttu-id="18e86-197">Você deve configurar a política de grupo usando o modelo de MBAM do MDOP e não o modelo de criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="18e86-197">You should configure Group Policy by using the MDOP MBAM template and not the BitLocker Drive Encryption template.</span></span>

<span data-ttu-id="18e86-198">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="18e86-198">For example:</span></span>

<span data-ttu-id="18e86-199">Em configurações de criptografia de unidade de sistema operacional, você selecionou TPM como protetor e também **permite pinos aprimorados para inicialização**.</span><span class="sxs-lookup"><span data-stu-id="18e86-199">Under Operating system drive encryption settings, you selected TPM as the protector, and you also selected **Allow enhanced PINs for startup**.</span></span> <span data-ttu-id="18e86-200">Essas são configurações conflitantes porque a proteção somente TPM não requer um PIN.</span><span class="sxs-lookup"><span data-stu-id="18e86-200">These are conflicting settings because TPM-only protection doesn't require a PIN.</span></span> <span data-ttu-id="18e86-201">Portanto, você deve desabilitar a configuração de pinos aprimorados.</span><span class="sxs-lookup"><span data-stu-id="18e86-201">Therefore, you should disable the enhanced PINs setting.</span></span>

### <span data-ttu-id="18e86-202">O usuário pode ter solicitado uma isenção</span><span class="sxs-lookup"><span data-stu-id="18e86-202">User may have requested an exemption</span></span>

<span data-ttu-id="18e86-203">Se você ativou a configuração do Computador\modelos Administrativos\Componentes do Components\MDOP MBAM (gerenciamento de BitLocker) \Client Management\Configure política de grupo da política de isenção de usuário, os usuários terão a opção de solicitar uma isenção.</span><span class="sxs-lookup"><span data-stu-id="18e86-203">If you enabled the Computer Configuration\Administrative Templates\Windows Components\MDOP MBAM (BitLocker Management)\Client Management\Configure user exemption policy Group Policy setting, users will be offered the option to request an exemption.</span></span>

<span data-ttu-id="18e86-204">Por padrão, se o usuário solicitar uma isenção, a isenção será válida por 7 dias e o usuário não receberá prompts para criptografar durante esse período.</span><span class="sxs-lookup"><span data-stu-id="18e86-204">By default, if the user requests an exemption, the exemption will be valid for 7 days, and the user will not receive prompts to encrypt during this period.</span></span> <span data-ttu-id="18e86-205">(O valor padrão pode ser aumentado ou diminuído durante a configuração da política.) Quando o período de isenção termina, o usuário é solicitado a criptografar.</span><span class="sxs-lookup"><span data-stu-id="18e86-205">(The default value can be increased or decreased during policy configuration.) After the exemption period is over, the user is prompted to encrypt.</span></span>

<span data-ttu-id="18e86-206">Você verá a seguinte entrada no log de eventos de administrador do MBAM quando um computador estiver em isenção de usuário:</span><span class="sxs-lookup"><span data-stu-id="18e86-206">You will see the following entry in the MBAM Admin event log when a computer is under user exemption:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 3:06:40 PM
    Event ID:      13
    Task Category: None
    Level:         Warning
    Keywords:      
    User:          SYSTEM
    Computer:      MBAMCLIENT.contoso.com
    Description:
    The user is exempt from encryption.

<span data-ttu-id="18e86-207">Se você quiser substituir manualmente a isenção do usuário de um computador, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="18e86-207">If you want to manually override user exemption for a computer, follow these steps:</span></span>
 
1. <span data-ttu-id="18e86-208">Defina o valor AllowUserExemption como **0** na seguinte subchave do registro:</span><span class="sxs-lookup"><span data-stu-id="18e86-208">Set the AllowUserExemption value to **0** under the following registry subkey:</span></span> <br />
**<span data-ttu-id="18e86-209">HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span><span class="sxs-lookup"><span data-stu-id="18e86-209">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span></span>**

2. <span data-ttu-id="18e86-210">Exclua todos os valores do registro na seguinte subchave do registro, exceto para **AgentVersion**, **EncodedComputerName**e **instalado**:</span><span class="sxs-lookup"><span data-stu-id="18e86-210">Delete all the registry values under the following registry subkey except for **AgentVersion**, **EncodedComputerName**, and **Installed**:</span></span><br />
**<span data-ttu-id="18e86-211">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM</span><span class="sxs-lookup"><span data-stu-id="18e86-211">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM</span></span>**

    <span data-ttu-id="18e86-212">**Observação** Você deve reiniciar o agente MBAM para que as alterações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="18e86-212">**Note** You must restart the MBAM agent for the changes to take effect.</span></span>

<span data-ttu-id="18e86-213">Lembre-se de que depois de aplicar a política de grupo ao computador, esses valores podem reverter às configurações originais.</span><span class="sxs-lookup"><span data-stu-id="18e86-213">Be aware that after you apply Group Policy to the computer, these values may revert to their original settings.</span></span>

### <span data-ttu-id="18e86-214">Problema do WMI</span><span class="sxs-lookup"><span data-stu-id="18e86-214">WMI issue</span></span>

<span data-ttu-id="18e86-215">MBAM usa métodos da classe win32_encryptablevolume para gerenciar o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="18e86-215">MBAM uses methods of the win32_encryptablevolume class to manage BitLocker.</span></span> <span data-ttu-id="18e86-216">Se esse módulo estiver cancelado ou corrompido, o cliente MBAM não funcionará corretamente, e você verá a seguinte entrada de evento no log de eventos de administração do MBAM:</span><span class="sxs-lookup"><span data-stu-id="18e86-216">If this module is unregistered or corrupted, the MBAM client will not operate correctly, and you will see the following event entry in the MBAM Admin event log:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/27/2013 11:18:51 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTEST.xtremelabs.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x80041016 
    Details:
    NULL

<span data-ttu-id="18e86-217">Além disso, você pode observar que as políticas de recuperação e de hardware não se aplicam com o código de erro 0x8007007E.</span><span class="sxs-lookup"><span data-stu-id="18e86-217">Additionally, you may notice that the Recovery and Hardware policies do not apply with Error Code 0x8007007e.</span></span> <span data-ttu-id="18e86-218">Isso é convertido em "o módulo especificado não foi encontrado".</span><span class="sxs-lookup"><span data-stu-id="18e86-218">This translates to "The specified module could not be found."</span></span>

<span data-ttu-id="18e86-219">Para resolver esse problema, você deve registrar novamente a classe **Win32_EncryptableVolume** usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="18e86-219">To resolve this issue, you should reregister the **win32_encryptablevolume** class by using the following command:</span></span>

```cmd
mofcomp c:\Windows\System32\wbem\win32_encryptablevolume.mof
```

## <span data-ttu-id="18e86-220">Solução de problemas de comunicação do agente MBAM</span><span class="sxs-lookup"><span data-stu-id="18e86-220">Troubleshooting MBAM Agent communication issues</span></span>

<span data-ttu-id="18e86-221">Esta seção contém informações de solução de problemas para os seguintes problemas relacionados à comunicação do agente do MBAM:</span><span class="sxs-lookup"><span data-stu-id="18e86-221">This section contains troubleshooting information for the following issues that are related to MBAM agent communication:</span></span>

### <span data-ttu-id="18e86-222">URL do serviço de MBAM incorreta</span><span class="sxs-lookup"><span data-stu-id="18e86-222">Incorrect MBAM service URL</span></span>

<span data-ttu-id="18e86-223">Se o valor do serviço de status de conformidade do MBAM ou do serviço de recuperação e de hardware estiver incorreto, você verá uma entrada de evento semelhante à seguinte no log de eventos de administração do MBAM no computador cliente:</span><span class="sxs-lookup"><span data-stu-id="18e86-223">If the value of MBAM Compliance Status Service or Recovery and Hardware Service is incorrect, you'll see an event entry that resembles the following in the MBAM Admin event log on the client computer:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:36 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:33 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

<span data-ttu-id="18e86-224">Verifique os valores de **KeyRecoveryServiceEndPoint** e **StatusReportingServiceEndpoint** sob a seguinte subchave do registro no computador cliente:</span><span class="sxs-lookup"><span data-stu-id="18e86-224">Verify the values of **KeyRecoveryServiceEndPoint** and **StatusReportingServiceEndpoint** under the following registry subkey on the client computer:</span></span> <br />
**<span data-ttu-id="18e86-225">HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span><span class="sxs-lookup"><span data-stu-id="18e86-225">HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement</span></span>**

<span data-ttu-id="18e86-226">Por padrão, a URL para o KeyRecoveryServiceEndPoint (recuperação do MBAM e o ponto de extremidade do serviço de hardware) está no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="18e86-226">By default, the URL for KeyRecoveryServiceEndPoint (MBAM Recovery and Hardware service endpoint) is in the following format:</span></span> <br />
**<span data-ttu-id="18e86-227">http:// \<servername\> : \<port\> /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="18e86-227">http://\<servername\>:\<port\>/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>**

<span data-ttu-id="18e86-228">Por padrão, a URL para o ponto de extremidade do serviço de relatório de status do StatusReportingServiceEndpoint (MBAM status) está no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="18e86-228">By default, the URL for StatusReportingServiceEndpoint (MBAM Status reporting service endpoint) is in the following format:</span></span><br />
**<span data-ttu-id="18e86-229">http:// \<servername\> : \<port\> /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="18e86-229">http://\<servername\>:\<port\>/MBAMComplianceStatusService/StatusReportingService.svc</span></span>**

> [!Note]
> <span data-ttu-id="18e86-230">Não deve haver espaços na URL.</span><span class="sxs-lookup"><span data-stu-id="18e86-230">There should be no spaces in the URL.</span></span>

<span data-ttu-id="18e86-231">Se a URL do serviço estiver incorreta, você deverá corrigir a URL do serviço na seguinte configuração de política de Grupo:</span><span class="sxs-lookup"><span data-stu-id="18e86-231">If the service URL is incorrect, you should correct the service URL in the following Group Policy setting:</span></span>

<span data-ttu-id="18e86-232">**Configuração**  >  do computador **Regras**  >  de **Modelos administrativos**  >  **Componentes**  >  do Windows **MDOP MBAM (gerenciamento de BitLocker)**  >  **Gerenciamento**  >  de cliente **Configurar os serviços do MBAM**</span><span class="sxs-lookup"><span data-stu-id="18e86-232">**Computer configuration** > **Policies** > **Administrative Templates** > **Windows Components** > **MDOP MBAM (BitLocker Management)** > **Client Management** > **Configure MBAM Services**</span></span>

### <span data-ttu-id="18e86-233">Problema de conectividade que afeta o servidor de administração do MBAM</span><span class="sxs-lookup"><span data-stu-id="18e86-233">Connectivity issue that affects the MBAM administration server</span></span>

<span data-ttu-id="18e86-234">O agente MBAM não poderá postar atualizações para o banco de dados se houver problemas de conectividade entre o agente cliente e o servidor de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="18e86-234">The MBAM agent will be unable to post any updates to the database if connectivity issues exist between the client agent and the MBAM administration server.</span></span> <span data-ttu-id="18e86-235">Nesse caso, você observará entradas de falha de conectividade no log de eventos de administrador do MBAM no computador cliente:</span><span class="sxs-lookup"><span data-stu-id="18e86-235">In this case, you will notice connectivity failure entries in the MBAM Admin event log on the client computer:</span></span>

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 18:21:22
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.
 
    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 23:06:48
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0006 
    Details:
    The operation did not complete within the time allotted.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          02-09-2013 02:02:04
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.

<span data-ttu-id="18e86-236">Verificações básicas:</span><span class="sxs-lookup"><span data-stu-id="18e86-236">Basic checks:</span></span>

* <span data-ttu-id="18e86-237">Verifique a conectividade básica fazendo ping no servidor de administração do MBAM por nome e IP.</span><span class="sxs-lookup"><span data-stu-id="18e86-237">Verify basic connectivity by pinging the MBAM administration server by name and IP.</span></span> <span data-ttu-id="18e86-238">Verifique se você pode se conectar ao site de administração do MBAM ou à porta de serviço usando o Telnet ou o Portqry.</span><span class="sxs-lookup"><span data-stu-id="18e86-238">Check whether you can connect to the MBAM administration website or service port by using telnet or portqry.</span></span>

* <span data-ttu-id="18e86-239">Verifique se o serviço IIS está em execução no servidor de administração e monitoramento do MBAM e se o serviço Web do MBAM está ouvindo na mesma porta que está configurada no computador cliente do MBAM ( `netstat –ano | find "portnumber"` ).</span><span class="sxs-lookup"><span data-stu-id="18e86-239">Verify that the IIS service is running on the MBAM administration and monitoring server and that the MBAM web service is listening on the same port that is configured on the MBAM client computer (`netstat –ano | find "portnumber"`).</span></span>

* <span data-ttu-id="18e86-240">Verifique se o número da porta que está configurado para o site do MBAM está usando o Gerenciador do IIS (inetmgr).</span><span class="sxs-lookup"><span data-stu-id="18e86-240">Verify that the port number that is configured for the MBAM website is using IIS Manager (inetmgr).</span></span> <span data-ttu-id="18e86-241">Certifique-se de que o número da porta seja igual ao número da porta na qual o cliente está ouvindo.</span><span class="sxs-lookup"><span data-stu-id="18e86-241">Make sure that the port number is the same as the port number on which the client is listening.</span></span> <span data-ttu-id="18e86-242">Certifique-se de que o número da porta não seja compartilhado por outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="18e86-242">Make sure that the port number is not shared by another application.</span></span> <span data-ttu-id="18e86-243">Por exemplo, outro aplicativo no servidor não deve estar usando a mesma porta.</span><span class="sxs-lookup"><span data-stu-id="18e86-243">For example, another application on the server should not be using the same port.</span></span>

* <span data-ttu-id="18e86-244">Se houver um firewall, certifique-se de que a porta esteja aberta no firewall ou servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="18e86-244">If there is a firewall, make sure that the port is open in the firewall or proxy server.</span></span>

* <span data-ttu-id="18e86-245">Se a comunicação entre o cliente e o servidor for segura, certifique-se de que você esteja usando um certificado SSL válido.</span><span class="sxs-lookup"><span data-stu-id="18e86-245">If the communication between client and server is secure, make sure that you are using a valid SSL certificate.</span></span>

* <span data-ttu-id="18e86-246">Verifique a conectividade de rede entre o servidor Web e o servidor de banco de dados para o qual os dados são enviados para inserção.</span><span class="sxs-lookup"><span data-stu-id="18e86-246">Verify network connectivity between the web server and the database server to which the data is sent for insertion.</span></span> <span data-ttu-id="18e86-247">Você pode verificar a conectividade do banco de dados do servidor Web para o servidor de banco de dados usando o administrador de fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="18e86-247">You can check database connectivity from the web server to the database server by using ODBC Data Source Administrator.</span></span> <span data-ttu-id="18e86-248">As informações detalhadas de solução de problemas de conexão do SQL Server estão disponíveis em [como solucionar problemas de conexão com o mecanismo de banco de dados do SQL Server](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).</span><span class="sxs-lookup"><span data-stu-id="18e86-248">Detailed SQL Server connection troubleshooting information is available in [How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).</span></span>

#### <span data-ttu-id="18e86-249">Solução de problemas do problema de conectividade</span><span class="sxs-lookup"><span data-stu-id="18e86-249">Troubleshooting the connectivity issue</span></span>

<span data-ttu-id="18e86-250">Verifique se a URL do serviço que está configurada no cliente está correta.</span><span class="sxs-lookup"><span data-stu-id="18e86-250">Make sure that the service URL that is configured on the client is correct.</span></span> <span data-ttu-id="18e86-251">Copie o valor da URL para KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**) a partir do registro e abra-o no Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="18e86-251">Copy the value of the URL for KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**) from the registry, and open it in Internet Explorer.</span></span>

<span data-ttu-id="18e86-252">Da mesma forma, copie o valor da URL para StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**) e abra-o no Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="18e86-252">Similarly, copy the value of the URL for StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**), and open it in Internet Explorer.</span></span>

> [!Note]
> <span data-ttu-id="18e86-253">Se não conseguir navegar até a URL do computador cliente, você deve testar a conectividade de rede básica do cliente para o servidor que está executando o IIS.</span><span class="sxs-lookup"><span data-stu-id="18e86-253">If you cannot browse to the URL from the client computer, you should test basic network connectivity from the client to the server that is running IIS.</span></span> <span data-ttu-id="18e86-254">Veja os pontos 1, 2, 3 e 4 na seção anterior.</span><span class="sxs-lookup"><span data-stu-id="18e86-254">See points 1, 2, 3, and 4 in the previous section.</span></span>

<span data-ttu-id="18e86-255">Além disso, examine os logs do aplicativo no servidor de administração e monitoramento em busca de erros.</span><span class="sxs-lookup"><span data-stu-id="18e86-255">Additionally, review the Application logs on the administration and monitoring server for any errors.</span></span>

<span data-ttu-id="18e86-256">Você pode fazer um rastreamento de rede simultânea entre o cliente e o servidor e examinar o rastreamento para determinar a causa da falha de conexão entre o agente cliente e o servidor de administração do MBAM.</span><span class="sxs-lookup"><span data-stu-id="18e86-256">You can make a concurrent network trace between the client and the server, and review the trace to determine the cause of connection failure between the client agent and the MBAM administration server.</span></span>

> [!Note]
> <span data-ttu-id="18e86-257">Se você puder navegar para as URLs de serviço do computador cliente e houver entradas de erro de conectividade nos logs de eventos de administrador do MBAM, isso pode ser devido a uma falha de conectividade entre o servidor de administração e o servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="18e86-257">If you can browse to the service URLs from the client computer and there are connectivity error entries in the MBAM admin event logs, this might be because of a connectivity failure between the administration server and the database server.</span></span>

<span data-ttu-id="18e86-258">Se você conseguir navegar para as duas URLs de serviço e houver conectividade entre o cliente e o servidor que está em execução, o IIS está funcionando.</span><span class="sxs-lookup"><span data-stu-id="18e86-258">If you can successfully browse to both service URLs, and there is connectivity between the client and the server that is running, IIS is working.</span></span> <span data-ttu-id="18e86-259">No entanto, pode haver um problema em comunicação entre o servidor que está executando o IIS e o servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="18e86-259">However, there may be a problem in communication between the server that is running IIS and the database server.</span></span>

<span data-ttu-id="18e86-260">Os serviços do MBAM podem não conseguir se conectar ao servidor de banco de dados devido a um problema de rede ou uma configuração de cadeia de conexão de banco de dados incorreta.</span><span class="sxs-lookup"><span data-stu-id="18e86-260">The MBAM services may be unable to connect to the database server because of a network issue or an incorrect database connection string setting.</span></span> <span data-ttu-id="18e86-261">Examine os logs do aplicativo no servidor de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="18e86-261">Review the Application logs on the administration and monitoring server.</span></span> <span data-ttu-id="18e86-262">Você pode ver erros de entrada ou avisos do 2.0.50727.0 de origem ASP.NET que se assemelham à seguinte entrada de log:</span><span class="sxs-lookup"><span data-stu-id="18e86-262">You might see errors entries or warnings from source ASP.NET 2.0.50727.0 that resemble the following log entry:</span></span>

    Log Name:      Application
    Source:        ASP.NET 2.0.50727.0
    Date:          7/11/2013 6:16:34 PM
    Event ID:      1310
    Task Category: Web Event
    Level:         Warning
    Keywords:      Classic
    User:          N/A
    Computer:      MBAM2-Admin.contoso.com
    Description:
    Event code: 100001
    Event message: SQL error occurred
    Event time: 7/11/2013 6:16:34 PM
    Event time (UTC): 7/11/2013 12:46:34 PM
    Event ID: 6615fb8eb9d54e778b933d5bb7ca91ed
    Event sequence: 2
    Event occurrence: 1
    Event detail code: 0 
    Application information:
        Application domain: /LM/W3SVC/2/ROOT/MBAMAdministrationService-1-130180202570338699
        Trust level: Full
        Application Virtual Path: /MBAMAdministrationService
        Application Path: C:\inetpub\Microsoft BitLocker Management Solution\Administration Service\
        Machine name: MBAM2-ADMIN 
    
    Process information:
        Process ID: 1940
        Process name: w3wp.exe
        Account name: NT AUTHORITY\NETWORK SERVICE 
    
    Exception information:
        Exception type: SqlException
        Exception message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server) 
    
    Request information:
        Request URL: 
        Request path: 
        User host address: 
        User: 
        Is authenticated: False
        Authentication Type: 
        Thread account name: NT AUTHORITY\NETWORK SERVICE 
    
    Thread information:
        Thread ID: 7
        Thread account name: NT AUTHORITY\NETWORK SERVICE
        Is impersonating: False
        Stack trace:    at System.Data.SqlClient.SqlInternalConnection.OnError(SqlException exception, Boolean breakConnection)
       at System.Data.SqlClient.TdsParser.ThrowExceptionAndWarning(TdsParserStateObject stateObj)
       at System.Data.SqlClient.TdsParser.Connect(ServerInfo serverInfo, SqlInternalConnectionTds connHandler, Boolean ignoreSniOpenTimeout, Int64 timerExpire, Boolean encrypt, Boolean trustServerCert, Boolean integratedSecurity, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.AttemptOneLogin(ServerInfo serverInfo, String newPassword, Boolean ignoreSniOpenTimeout, Int64 timerExpire, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.LoginNoFailover(String host, String newPassword, Boolean redirectedUserInstance, SqlConnection owningObject, SqlConnectionString connectionOptions, Int64 timerStart)
       at System.Data.SqlClient.SqlInternalConnectionTds.OpenLoginEnlist(SqlConnection owningObject, SqlConnectionString connectionOptions, String newPassword, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlInternalConnectionTds..ctor(DbConnectionPoolIdentity identity, SqlConnectionString connectionOptions, Object providerInfo, String newPassword, SqlConnection owningObject, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlConnectionFactory.CreateConnection(DbConnectionOptions options, Object poolGroupProviderInfo, DbConnectionPool pool, DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionFactory.CreatePooledConnection(DbConnection owningConnection, DbConnectionPool pool, DbConnectionOptions options)
       at System.Data.ProviderBase.DbConnectionPool.CreateObject(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.UserCreateRequest(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.GetConnection(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionFactory.GetConnection(DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionClosed.OpenConnection(DbConnection outerConnection, DbConnectionFactory connectionFactory)
       at System.Data.SqlClient.SqlConnection.Open()
       at System.Data.Linq.SqlClient.SqlConnectionManager.UseConnection(IConnectionUser user)
       at System.Data.Linq.SqlClient.SqlProvider.get_IsSqlCe()
       at System.Data.Linq.SqlClient.SqlProvider.InitializeProviderMode()
       at System.Data.Linq.SqlClient.SqlProvider.System.Data.Linq.Provider.IProvider.Execute(Expression query)
       at System.Data.Linq.DataContext.ExecuteMethodCall(Object instance, MethodInfo methodInfo, Object[] parameters)
       at Microsoft.Mbam.Server.ServiceCommon.KeyRecoveryModelDataContext.GetRecoveryKeyIds(String partialRecoveryKeyId, String reason)
       at Microsoft.Mbam.ApplicationSupportService.AdministrationService.GetRecoveryKeyIds(String partialRecoveryKeyId, String reasonCode)
    
    Custom event details:
        Application: MBAMAdministrationService
        Sql Server:
        Database: MBAM Recovery and Hardware
        Database: MBAM Compliance Status
        Sql ErrorCode: 5
        Error Message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)

#### <span data-ttu-id="18e86-263">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="18e86-263">Possible causes</span></span>

##### <span data-ttu-id="18e86-264">Causa 1</span><span class="sxs-lookup"><span data-stu-id="18e86-264">Cause 1</span></span>

<span data-ttu-id="18e86-265">O administrador pode ter especificado um nome de instância de banco de dados/nome de banco de dados inválido durante a instalação dos componentes de servidor de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="18e86-265">The administrator may have specified an invalid database instance name/database name during installation of administration and monitoring server components.</span></span>

<span data-ttu-id="18e86-266">Você pode verificar e corrigir as cadeias de conexão de banco de dados usando o console de gerenciamento do IIS.</span><span class="sxs-lookup"><span data-stu-id="18e86-266">You can verify and correct the database connection strings by using the IIS Management console.</span></span> <span data-ttu-id="18e86-267">Para fazer isso, abra o Gerenciador do IIS e navegue até Administração e monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="18e86-267">To do this, open IIS Manager, and browse to Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="18e86-268">Para cada serviço listado no lado esquerdo, siga estas etapas para alterar as cadeias de conexão do banco de dados:</span><span class="sxs-lookup"><span data-stu-id="18e86-268">For each service that is listed on the left side, follow these steps to change the database connection strings:</span></span>

1. <span data-ttu-id="18e86-269">No **modo de exibição recursos**, selecione duas **cadeias de conexão**.</span><span class="sxs-lookup"><span data-stu-id="18e86-269">In **Features View**, double-select **Connection Strings**.</span></span>

2. <span data-ttu-id="18e86-270">Na página **cadeias de conexão** , selecione a cadeia de conexão que você deseja alterar.</span><span class="sxs-lookup"><span data-stu-id="18e86-270">On the **Connection Strings** page, select the connection string that you want to change.</span></span>

3. <span data-ttu-id="18e86-271">No painel **ações** , selecione **Editar**.</span><span class="sxs-lookup"><span data-stu-id="18e86-271">In the **Actions** pane, select **Edit**.</span></span>

4. <span data-ttu-id="18e86-272">Na caixa de diálogo **Editar Cadeia de conexão** , altere as propriedades que você deseja alterar e, em seguida, selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="18e86-272">In the **Edit Connection String** dialog box, change the properties that you want to change, and then select **OK**.</span></span>

##### <span data-ttu-id="18e86-273">Causa 2</span><span class="sxs-lookup"><span data-stu-id="18e86-273">Cause 2</span></span>

<span data-ttu-id="18e86-274">Porta do SQL Server bloqueada no firewall.</span><span class="sxs-lookup"><span data-stu-id="18e86-274">SQL Server port blocked in firewall.</span></span> <span data-ttu-id="18e86-275">Verifique o número da porta para a qual o SQL Server está configurado para escuta e certifique-se de que a porta esteja aberta no firewall entre o servidor de administração e o servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="18e86-275">Verify the port number to which SQL Server is configured to listen, and make sure that the port is open in the firewall between the administration server and database server.</span></span>

##### <span data-ttu-id="18e86-276">Causa 3</span><span class="sxs-lookup"><span data-stu-id="18e86-276">Cause 3</span></span>

<span data-ttu-id="18e86-277">Associações TCP/IP do SQL Server incorretas.</span><span class="sxs-lookup"><span data-stu-id="18e86-277">Incorrect SQL server TCP/IP bindings.</span></span> <span data-ttu-id="18e86-278">Verifique as associações de TCP/IP do SQL no Gerenciador de configuração do SQL Server no servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="18e86-278">Verify SQL TCP/IP bindings in SQL Server Configuration Manager on the database server.</span></span> <span data-ttu-id="18e86-279">MBAM requer que os protocolos TCP/IP e pipes nomeados estejam habilitados para se conectar ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="18e86-279">MBAM requires that the TCP/IP and Named Pipes protocols are enabled to connect to the database.</span></span>

##### <span data-ttu-id="18e86-280">Causa 4</span><span class="sxs-lookup"><span data-stu-id="18e86-280">Cause 4</span></span>

<span data-ttu-id="18e86-281">A conta NT Authority\Network Service ou a conta de computador do servidor de administração do MBAM não tem as permissões necessárias para se conectar ao banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="18e86-281">The NT Authority\Network Service account or the MBAM Administration Server’s computer account doesn't have the required permissions to connect to the SQL database.</span></span>

<span data-ttu-id="18e86-282">Durante a instalação dos componentes de banco de dados no servidor de banco de dados, o instalador cria dois grupos locais: MBAM conformidade auditando o acesso ao banco de dados e recuperação do MBAM e acesso ao banco de dados de hardware.</span><span class="sxs-lookup"><span data-stu-id="18e86-282">During the installation of database components on the database server, the installer creates two local groups: MBAM Compliance Auditing DB Access and MBAM Recovery and Hardware DB Access.</span></span>

<span data-ttu-id="18e86-283">A conta NT Authority\Network Service, a conta de computador do servidor de administração do MBAM e o usuário que instala os componentes do banco de dados são automaticamente adicionados a esses grupos.</span><span class="sxs-lookup"><span data-stu-id="18e86-283">The NT Authority\Network Service account, the MBAM administration server’s computer account, and the user who installs the database components are automatically added to these groups.</span></span>

<span data-ttu-id="18e86-284">Esses grupos recebem as permissões necessárias no banco de dados durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="18e86-284">These groups are granted the required permissions on the database during the installation.</span></span> <span data-ttu-id="18e86-285">Todos os usuários que fazem parte deste grupo recebem automaticamente as permissões necessárias no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="18e86-285">All users who are part of this group automatically receive the required permissions on the database.</span></span>

<span data-ttu-id="18e86-286">O serviço Web pode não se conectar ao servidor de banco de dados devido a um problema de permissões se uma ou mais das seguintes condições forem verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="18e86-286">The web service may not connect to the database server because of a permissions issue if one or more of the following conditions are true:</span></span>

* <span data-ttu-id="18e86-287">Os grupos mencionados anteriormente são removidos dos grupos locais do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="18e86-287">The groups that were mentioned earlier are removed from the local groups on the database server.</span></span>

* <span data-ttu-id="18e86-288">A conta NT Authority\Network Service e a conta do computador do servidor de administração do MBAM não são membros desses grupos.</span><span class="sxs-lookup"><span data-stu-id="18e86-288">The NT Authority\Network Service account and the MBAM administration server’s computer account are not members of these groups.</span></span>

* <span data-ttu-id="18e86-289">Esses grupos não têm as permissões necessárias no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="18e86-289">These groups do not have the required permissions on the database.</span></span>

<span data-ttu-id="18e86-290">Você notará erros relacionados a permissões nos logs do aplicativo na administração do MBAM e no servidor de monitoramento se qualquer uma das condições anteriores forem verdadeiras.</span><span class="sxs-lookup"><span data-stu-id="18e86-290">You will notice permissions-related errors in the Application logs on the MBAM administration and monitoring server if any of the previous conditions are true.</span></span> <span data-ttu-id="18e86-291">Nesse caso, você deve adicionar manualmente a conta NT Authority\Network Service e a conta de computador do servidor de administração do MBAM e conceder a elas uma função pública em todo o servidor no servidor de banco de dados SQL que está usando o SQL Server Management Studio ( https://msdn.microsoft.com/library/aa337562.aspx) .</span><span class="sxs-lookup"><span data-stu-id="18e86-291">In that case, you should manually add the NT Authority\Network Service account and MBAM administration server’s computer account and grant them a server-wide public role on the SQL database server that is using SQL Server Management Studio (https://msdn.microsoft.com/library/aa337562.aspx).</span></span>

#### <span data-ttu-id="18e86-292">Examine os logs do serviço Web</span><span class="sxs-lookup"><span data-stu-id="18e86-292">Review the web service logs</span></span>

<span data-ttu-id="18e86-293">Se nenhum evento for registrado nos logs do aplicativo no servidor de administração do MBAM, é hora de analisar os logs do serviço Web (. svclog) do serviço Web MBAM hospedado no servidor de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="18e86-293">If no events are logged in the Application logs on the MBAM administration server, it’s time to review the web service logs (.svclog) of the MBAM web service that is hosted on the MBAM administration and monitoring server.</span></span> <span data-ttu-id="18e86-294">Você precisará usar a ferramenta Visualizador de rastreamento de serviço (SvcTraceViewer.exe) https://msdn.microsoft.com/library/ms732023.aspx para exibir o arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="18e86-294">You will have to use the Service Trace Viewer Tool (SvcTraceViewer.exe) https://msdn.microsoft.com/library/ms732023.aspx to view the log file.</span></span>

<span data-ttu-id="18e86-295">Você deve investigar principalmente os logs de rastreamento de serviço do RecoveryandHardwareService e do ComplianceStatusService.</span><span class="sxs-lookup"><span data-stu-id="18e86-295">You should primarily investigate the service trace logs of RecoveryandHardwareService and ComplianceStatusService.</span></span> <span data-ttu-id="18e86-296">Por padrão, os logs do serviço Web estão localizados na pasta Solution\Logs C:\inetpub\Microsoft de gerenciamento do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="18e86-296">By default, web service logs are located in the C:\inetpub\Microsoft BitLocker Management Solution\Logs folder.</span></span> <span data-ttu-id="18e86-297">Nesse caso, cada serviço grava o arquivo. svclog em sua própria pasta.</span><span class="sxs-lookup"><span data-stu-id="18e86-297">There, each service writes its .svclog file under its own folder.</span></span>

<span data-ttu-id="18e86-298">Examine a atividade no log de rastreamento do serviço em busca de erros ou entradas de aviso.</span><span class="sxs-lookup"><span data-stu-id="18e86-298">Review the activity in the service trace log for any error or warning entries.</span></span> <span data-ttu-id="18e86-299">Por padrão, as entradas de erro são realçadas em vermelho.</span><span class="sxs-lookup"><span data-stu-id="18e86-299">By default, error entries are highlighted in red.</span></span> <span data-ttu-id="18e86-300">Selecione a descrição do erro no painel direito do Visualizador de rastreamento para ver informações detalhadas sobre a entrada de erro.</span><span class="sxs-lookup"><span data-stu-id="18e86-300">Select the error description on the right pane of the trace viewer to view detailed information about the error entry.</span></span> <span data-ttu-id="18e86-301">Veja a seguir um exemplo de entrada de erro do log de rastreamento:</span><span class="sxs-lookup"><span data-stu-id="18e86-301">The following is a sample error entry from the trace log:</span></span>

    <E2ETraceEvent xmlns="http://schemas.microsoft.com/2004/06/E2ETraceEvent">
    <System xmlns="http://schemas.microsoft.com/2004/06/windows/eventlog/system">
    <EventID>15183</EventID>
    <Type>3</Type>
    <SubType Name="Error">0</SubType>
    <Level>2</Level>
    <TimeCreated SystemTime="2013-07-05T14:48:06.2821550Z" />
    <Source Name="Microsoft.Mbam.CoreService" />
    <Correlation ActivityID="{00000000-0000-0000-0000-000000000000}" />
    <Execution ProcessName="w3wp" ProcessID="4332" ThreadID="11" />
    <Channel />
    <Computer>XXXXXXXXXXX</Computer>
    </System>
    <ApplicationData>AddUpdateVolume: While executing sql transaction for add volume to store exception occurred Key Recovery Data Store processing error: Violation of UNIQUE KEY constraint 'UniqueRecoveryKeyId'. Cannot insert duplicate key in object 'RecoveryAndHardwareCore.Keys'. The duplicate key value is (8637036e-b379-4798-bd9e-5a0b36296de3).
    </ApplicationData>
    </E2ETraceEvent>

## <span data-ttu-id="18e86-302">Reinstalação ou reconfiguração da infraestrutura do MBAM</span><span class="sxs-lookup"><span data-stu-id="18e86-302">Re-installation or reconfiguration of MBAM infrastructure</span></span>

<span data-ttu-id="18e86-303">Para reinstalar ou reconfigurar a infraestrutura do MBAM, você deve conhecer os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="18e86-303">To re-install or reconfigure MBAM infrastructure, you must know the following things:</span></span>

* <span data-ttu-id="18e86-304">Conta do pool de aplicativos</span><span class="sxs-lookup"><span data-stu-id="18e86-304">Application Pool account</span></span>

* <span data-ttu-id="18e86-305">Grupos do MBAM (assistência técnica, avançado, grupo de usuários de relatório)</span><span class="sxs-lookup"><span data-stu-id="18e86-305">MBAM Groups (Helpdesk, Advanced, Report Users Group)</span></span>

* <span data-ttu-id="18e86-306">URL de relatórios do MBAM</span><span class="sxs-lookup"><span data-stu-id="18e86-306">MBAM Reports URL</span></span>

* <span data-ttu-id="18e86-307">Nome do SQL Server e nomes de bancos de dados</span><span class="sxs-lookup"><span data-stu-id="18e86-307">SQL Server name and database names</span></span>

* <span data-ttu-id="18e86-308">MBAM ReadWrite e ReadOnly</span><span class="sxs-lookup"><span data-stu-id="18e86-308">MBAM ReadWrite and ReadOnly Accounts</span></span>

### <span data-ttu-id="18e86-309">Conta do pool de aplicativos</span><span class="sxs-lookup"><span data-stu-id="18e86-309">Application Pool account</span></span>

<span data-ttu-id="18e86-310">Para localizar a conta do pool de aplicativos, faça logon no servidor Web MBAM, abra o **Gerenciador dos serviços de informações da Internet (IIS)** e selecione **pools de aplicativos**:</span><span class="sxs-lookup"><span data-stu-id="18e86-310">To find the Application Pool account, log on to the MBAM Web Server, open **Internet Information Services (IIS) Manager**, and then select **Application Pools**:</span></span>

![pools de aplicativos](images/troubleshooting-MBAM-installation-1.png)

<span data-ttu-id="18e86-312">O SPN (nome da entidade de serviço) deve ser definido nesta conta.</span><span class="sxs-lookup"><span data-stu-id="18e86-312">The Service Principal Name (SPN) must be set in this account.</span></span> <span data-ttu-id="18e86-313">Essa configuração é muito importante para a funcionalidade do MBAM.</span><span class="sxs-lookup"><span data-stu-id="18e86-313">This setting is very important to the functionality of MBAM.</span></span>

### <span data-ttu-id="18e86-314">Grupos do MBAM (assistência técnica, avançado, grupo de usuários relatórios e URL de relatórios)</span><span class="sxs-lookup"><span data-stu-id="18e86-314">MBAM Groups (Helpdesk, Advanced, Report Users Group and Reports URL)</span></span>

![Grupos do MBAM](images/troubleshooting-MBAM-installation-2.png)

<span data-ttu-id="18e86-316">Isso fornece informações como grupo de helpdesk, grupo avançado de assistência técnica, grupo de usuários de relatório e URL de relatórios do MBAM.</span><span class="sxs-lookup"><span data-stu-id="18e86-316">This provides information such as Helpdesk Group, Advanced Helpdesk Group, Report Users group, and MBAM Reports URL.</span></span> <span data-ttu-id="18e86-317">A URL de relatórios do MBAM deve ser fornecida na configuração do MBAM e deve ser lida como: http (s)://servername/ReportServer.</span><span class="sxs-lookup"><span data-stu-id="18e86-317">The MBAM Reports URL must be provided in the MBAM setup and should read as: http(s)://servername/ReportServer.</span></span>

### <span data-ttu-id="18e86-318">Nome do SQL Server e nomes de banco de dados (DB)</span><span class="sxs-lookup"><span data-stu-id="18e86-318">SQL Server name and database (DB) names</span></span>

<span data-ttu-id="18e86-319">Para localizar os nomes e instâncias do SQL Server que hospedam os bancos de MBAM, faça logon no servidor Web do MBAM (IIS) e navegue até a subchave do registro do folowing:</span><span class="sxs-lookup"><span data-stu-id="18e86-319">To find the SQL Server names and instances hosting the MBAM DBs, log on to the MBAM Web (IIS) server and browse to the folowing registry subkey:</span></span>

**<span data-ttu-id="18e86-320">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM Server\Web</span><span class="sxs-lookup"><span data-stu-id="18e86-320">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web</span></span>**

![Regedit](images/troubleshooting-MBAM-installation-3.png)

<span data-ttu-id="18e86-322">As partes realçadas são cadeias de conexão.</span><span class="sxs-lookup"><span data-stu-id="18e86-322">The highlighted portions are connection strings.</span></span> <span data-ttu-id="18e86-323">Eles devem ter o nome do SQL Server, os nomes de banco de dados e as instâncias (se nomeados).</span><span class="sxs-lookup"><span data-stu-id="18e86-323">These should have the SQL Server name, database names, and instances (if named).</span></span>

### <span data-ttu-id="18e86-324">MBAM ReadWrite e ReadOnly</span><span class="sxs-lookup"><span data-stu-id="18e86-324">MBAM ReadWrite and ReadOnly accounts</span></span>

<span data-ttu-id="18e86-325">Essas informações estarão no banco de dados do SQL Server, para a qual já encontramos o nome do servidor Web.</span><span class="sxs-lookup"><span data-stu-id="18e86-325">This information will be in the SQL Server database, for which we already found the name from the web server.</span></span>

#### <span data-ttu-id="18e86-326">Conta ReadWrite</span><span class="sxs-lookup"><span data-stu-id="18e86-326">ReadWrite account</span></span>

1. <span data-ttu-id="18e86-327">Conecte-se ao SQL Management Studio.</span><span class="sxs-lookup"><span data-stu-id="18e86-327">Log in to the SQL Management Studio.</span></span>

2. <span data-ttu-id="18e86-328">Clique com o botão direito do mouse em **MBAM recuperação e hardware**, selecione **Propriedades**e, em seguida, selecione **permissões**.</span><span class="sxs-lookup"><span data-stu-id="18e86-328">Right-click **MBAM Recovery and Hardware**, select **Properties**, and then select **Permissions**.</span></span>

<span data-ttu-id="18e86-329">Por exemplo, o nome da conta do laboratório é **MBAMWrite**.</span><span class="sxs-lookup"><span data-stu-id="18e86-329">For example, The the lab account name is **MBAMWrite**.</span></span> <span data-ttu-id="18e86-330">As contas pool de aplicativos e ReadWrite são definidas para serem iguais.</span><span class="sxs-lookup"><span data-stu-id="18e86-330">The Application Pool and ReadWrite accounts are set to be the same.</span></span>

![SQL DB](images/troubleshooting-MBAM-installation-4.png)

![Propriedades de banco de BD](images/troubleshooting-MBAM-installation-5.png)

<span data-ttu-id="18e86-333">Navegue até **segurança** e, em seguida, **logins** no SQL Management Studio.</span><span class="sxs-lookup"><span data-stu-id="18e86-333">Browse to **Security** and then **Logins** in SQL Management Studio.</span></span> <span data-ttu-id="18e86-334">Navegue até a conta mostrada na captura de tela anterior.</span><span class="sxs-lookup"><span data-stu-id="18e86-334">Browse to the account shown in the previous screenshot.</span></span>

![Segurança do SQL](images/troubleshooting-MBAM-installation-6.png)

<span data-ttu-id="18e86-336">Clique com o botão direito do mouse nas contas, vá para **Propriedades mapeamento de usuários**e localize o banco de dados de recuperação e hardware do MBAM:</span><span class="sxs-lookup"><span data-stu-id="18e86-336">Right-click the accounts, go to **Properties User Mapping**, and locate the MBAM Recovery and Hardware database:</span></span>

![Mapeamento de usuários](images/troubleshooting-MBAM-installation-7.png)

#### <span data-ttu-id="18e86-338">Conta somente leitura</span><span class="sxs-lookup"><span data-stu-id="18e86-338">ReadOnly account</span></span>

<span data-ttu-id="18e86-339">Abra o Gerenciador de configuração do SQL Server Reporting Services no servidor SSRS.</span><span class="sxs-lookup"><span data-stu-id="18e86-339">Open SQL Server Reporting Services Configuration Manager on the SSRS Server.</span></span> <span data-ttu-id="18e86-340">Selecione a **URL do Gerenciador de relatórios**e, em seguida, navegue pelas **URLs**:</span><span class="sxs-lookup"><span data-stu-id="18e86-340">Select **Report Manager URL**, and then browse the **URLs**:</span></span>

![Gerenciador de relatórios](images/troubleshooting-MBAM-installation-8.png)

<span data-ttu-id="18e86-342">Selecione **Administração e monitoramento do Microsoft BitLocker**:</span><span class="sxs-lookup"><span data-stu-id="18e86-342">Select **Microsoft Bitlocker Administration and Monitoring**:</span></span>

![Administração e monitoramento do BitLocker](images/troubleshooting-MBAM-installation-9.png)

<span data-ttu-id="18e86-344">Selecione **MaltaDatasource**:</span><span class="sxs-lookup"><span data-stu-id="18e86-344">Select **MaltaDatasource**:</span></span>

![Bancos](images/troubleshooting-MBAM-installation-10.png)

![MaltaDatasource](images/troubleshooting-MBAM-installation-11.png)

<span data-ttu-id="18e86-347">MaltaDataSource deve ter o nome da conta ReadOnly e deve ser usado na instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="18e86-347">MaltaDataSource should have the ReadOnly Account name and should be used in MBAM setup.</span></span>

## <span data-ttu-id="18e86-348">Referência</span><span class="sxs-lookup"><span data-stu-id="18e86-348">Reference</span></span>

<span data-ttu-id="18e86-349">Para obter mais informações, consulte os seguintes artigos:</span><span class="sxs-lookup"><span data-stu-id="18e86-349">For more information, see the following articles:</span></span>

[<span data-ttu-id="18e86-350">Implantando o MBAM 2,5 em uma configuração autônoma</span><span class="sxs-lookup"><span data-stu-id="18e86-350">Deploying MBAM 2.5 in a standalone configuration</span></span>](https://support.microsoft.com/help/3046555)

[<span data-ttu-id="18e86-351">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="18e86-351">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/)
