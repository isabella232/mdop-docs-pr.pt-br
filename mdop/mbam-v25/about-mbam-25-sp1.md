---
title: Sobre o MBAM 2.5 SP1
description: Sobre o MBAM 2.5 SP1
author: dansimp
ms.assetid: 6f12e605-44e6-4646-9c20-aee89c8ff0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 41e47e1561629c00d30b45ad2dcd94f37753af5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799341"
---
# <span data-ttu-id="47f51-103">Sobre o MBAM 2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="47f51-103">About MBAM 2.5 SP1</span></span>


<span data-ttu-id="47f51-104">O MBAM 2,5 SP1 fornece uma interface administrativa simplificada para a criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="47f51-104">MBAM 2.5 SP1 provides a simplified administrative interface for BitLocker Drive Encryption.</span></span> <span data-ttu-id="47f51-105">O BitLocker oferece proteção aprimorada contra roubo de dados ou exposição de dados para computadores perdidos ou roubados.</span><span class="sxs-lookup"><span data-stu-id="47f51-105">BitLocker offers enhanced protection against data theft or data exposure for computers that are lost or stolen.</span></span> <span data-ttu-id="47f51-106">O BitLocker criptografa todos os dados armazenados no sistema operacional Windows e nas unidades de dados configuradas.</span><span class="sxs-lookup"><span data-stu-id="47f51-106">BitLocker encrypts all data that is stored on the Windows operating system and drives and configured data drives.</span></span>

## <span data-ttu-id="47f51-107">Visão geral do MBAM</span><span class="sxs-lookup"><span data-stu-id="47f51-107">Overview of MBAM</span></span>


<span data-ttu-id="47f51-108">O MBAM 2,5 SP1 tem os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="47f51-108">MBAM 2.5 SP1 has the following features:</span></span>

-   <span data-ttu-id="47f51-109">Permite que os administradores automatizem o processo de criptografar volumes em computadores cliente em toda a empresa.</span><span class="sxs-lookup"><span data-stu-id="47f51-109">Enables administrators to automate the process of encrypting volumes on client computers across the enterprise.</span></span>

-   <span data-ttu-id="47f51-110">Permite que os agentes de segurança determinem rapidamente o estado de conformidade de computadores individuais ou até mesmo da empresa em si.</span><span class="sxs-lookup"><span data-stu-id="47f51-110">Enables security officers to quickly determine the compliance state of individual computers or even of the enterprise itself.</span></span>

-   <span data-ttu-id="47f51-111">Fornece gerenciamento centralizado de relatório e de hardware com o Microsoft System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="47f51-111">Provides centralized reporting and hardware management with Microsoft System Center Configuration Manager.</span></span>

-   <span data-ttu-id="47f51-112">Reduz a carga de trabalho no suporte técnico para ajudar os usuários finais com o PIN do BitLocker e solicitações de chave de recuperação.</span><span class="sxs-lookup"><span data-stu-id="47f51-112">Reduces the workload on the Help Desk to assist end users with BitLocker PIN and recovery key requests.</span></span>

-   <span data-ttu-id="47f51-113">Permite aos usuários finais recuperar dispositivos criptografados de forma independente, usando o Portal de Autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="47f51-113">Enables end users to recover encrypted devices independently by using the Self-Service Portal.</span></span>

-   <span data-ttu-id="47f51-114">Permite que os gerentes de segurança auditem facilmente o acesso para recuperar informações importantes.</span><span class="sxs-lookup"><span data-stu-id="47f51-114">Enables security officers to easily audit access to recover key information.</span></span>

-   <span data-ttu-id="47f51-115">Permite que os usuários do Windows Enterprise continuem a trabalhar em qualquer lugar com a garantia de que seus dados corporativos estão protegidos.</span><span class="sxs-lookup"><span data-stu-id="47f51-115">Empowers Windows Enterprise users to continue working anywhere with the assurance that their corporate data is protected.</span></span>

<span data-ttu-id="47f51-116">O MBAM impõe as opções de política de criptografia BitLocker definidas para a sua empresa, monitora a conformidade dos computadores cliente com essas políticas e relata sobre o status de criptografia dos computadores da empresa e do indivíduo.</span><span class="sxs-lookup"><span data-stu-id="47f51-116">MBAM enforces the BitLocker encryption policy options that you set for your enterprise, monitors the compliance of client computers with those policies, and reports on the encryption status of the enterprise’s and individual’s computers.</span></span> <span data-ttu-id="47f51-117">Além disso, o MBAM permite que você acesse as informações da chave de recuperação quando os usuários esquecem o PIN ou a senha, ou quando os registros de inicialização ou do BIOS são alterados.</span><span class="sxs-lookup"><span data-stu-id="47f51-117">In addition, MBAM lets you access the recovery key information when users forget their PIN or password, or when their BIOS or boot records change.</span></span>

<span data-ttu-id="47f51-118">Os seguintes grupos podem estar interessados em usar o MBAM para gerenciar o BitLocker:</span><span class="sxs-lookup"><span data-stu-id="47f51-118">The following groups might be interested in using MBAM to manage BitLocker:</span></span>

-   <span data-ttu-id="47f51-119">Administradores, profissionais de segurança de ti e responsáveis pela conformidade responsáveis por garantir que os dados confidenciais não sejam divulgados sem autorização</span><span class="sxs-lookup"><span data-stu-id="47f51-119">Administrators, IT security professionals, and compliance officers who are responsible for ensuring that confidential data is not disclosed without authorization</span></span>

-   <span data-ttu-id="47f51-120">Administradores que são responsáveis por segurança de computador em escritórios remotos ou filiais</span><span class="sxs-lookup"><span data-stu-id="47f51-120">Administrators who are responsible for computer security in remote or branch offices</span></span>

-   <span data-ttu-id="47f51-121">Administradores responsáveis pelos computadores cliente que executam o Windows</span><span class="sxs-lookup"><span data-stu-id="47f51-121">Administrators who are responsible for client computers that are running Windows</span></span>

<span data-ttu-id="47f51-122">**Observação**  O BitLocker não é explicado em detalhes nesta documentação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="47f51-122">**Note** BitLocker is not explained in detail in this MBAM documentation.</span></span> <span data-ttu-id="47f51-123">Para obter mais informações, consulte [visão geral da criptografia de unidade BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span><span class="sxs-lookup"><span data-stu-id="47f51-123">For more information, see [BitLocker Drive Encryption Overview](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span></span>

 

## <a href="" id="what-s-new-in-mbam-2-5-sp1"></a><span data-ttu-id="47f51-124">O que há de novo no MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="47f51-124">What’s new in MBAM 2.5 SP1</span></span>


<span data-ttu-id="47f51-125">Esta seção descreve os novos recursos do MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="47f51-125">This section describes the new features in MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="47f51-126">Idiomas recém-instalados para o cliente MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="47f51-126">Newly Supported Languages for the MBAM 2.5 SP1 Client</span></span>

<span data-ttu-id="47f51-127">Os seguintes idiomas adicionais agora são compatíveis com o MBAM 2,5 SP1 somente para o cliente MBAM, incluindo o portal de autoatendimento:</span><span class="sxs-lookup"><span data-stu-id="47f51-127">The following additional languages are now supported in MBAM 2.5 SP1 for the MBAM Client only, including the Self-Service Portal:</span></span>

<span data-ttu-id="47f51-128">Tcheco (República Tcheca) CS-CZ</span><span class="sxs-lookup"><span data-stu-id="47f51-128">Czech (Czech Republic) cs-CZ</span></span>

<span data-ttu-id="47f51-129">Dinamarquês (Dinamarca) da-DK</span><span class="sxs-lookup"><span data-stu-id="47f51-129">Danish (Denmark) da-DK</span></span>

<span data-ttu-id="47f51-130">Holandês (Holanda) nl-NL</span><span class="sxs-lookup"><span data-stu-id="47f51-130">Dutch (Netherlands) nl-NL</span></span>

<span data-ttu-id="47f51-131">Finlandês (Finlândia) fi-FI</span><span class="sxs-lookup"><span data-stu-id="47f51-131">Finnish (Finland) fi-FI</span></span>

<span data-ttu-id="47f51-132">Grego (Grécia) El-GA</span><span class="sxs-lookup"><span data-stu-id="47f51-132">Greek (Greece) el-GR</span></span>

<span data-ttu-id="47f51-133">Húngaro (Hungria) hu-HU</span><span class="sxs-lookup"><span data-stu-id="47f51-133">Hungarian (Hungary) hu-HU</span></span>

<span data-ttu-id="47f51-134">Norueguês, Bokmål (Noruega) NB-não</span><span class="sxs-lookup"><span data-stu-id="47f51-134">Norwegian, Bokmål (Norway) nb-NO</span></span>

<span data-ttu-id="47f51-135">Polonês (Polônia) pl-PL</span><span class="sxs-lookup"><span data-stu-id="47f51-135">Polish (Poland) pl-PL</span></span>

<span data-ttu-id="47f51-136">Português (Portugal) pt-PT</span><span class="sxs-lookup"><span data-stu-id="47f51-136">Portuguese (Portugal) pt-PT</span></span>

<span data-ttu-id="47f51-137">Eslovaco (Eslováquia) SK-SK</span><span class="sxs-lookup"><span data-stu-id="47f51-137">Slovak (Slovakia) sk-SK</span></span>

<span data-ttu-id="47f51-138">Esloveno (Eslovênia) SL-SI</span><span class="sxs-lookup"><span data-stu-id="47f51-138">Slovenian (Slovenia) sl-SI</span></span>

<span data-ttu-id="47f51-139">Sueco (Suécia) VA-SE</span><span class="sxs-lookup"><span data-stu-id="47f51-139">Swedish (Sweden) sv-SE</span></span>

<span data-ttu-id="47f51-140">Turco (Turquia) TR-TR</span><span class="sxs-lookup"><span data-stu-id="47f51-140">Turkish (Turkey) tr-TR</span></span>

<span data-ttu-id="47f51-141">Para obter uma lista de todos os idiomas compatíveis com o cliente e o servidor no MBAM 2,5 e o MBAM 2,5 SP1, consulte [configurações compatíveis do MBAM 2,5](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="47f51-141">For a list of all languages supported for client and server in MBAM 2.5 and MBAM 2.5 SP1, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

### <span data-ttu-id="47f51-142">Suporte para Windows 10</span><span class="sxs-lookup"><span data-stu-id="47f51-142">Support for Windows 10</span></span>

<span data-ttu-id="47f51-143">O MBAM 2,5 SP1 adiciona suporte para o Windows 10 e o Windows Server 2016, além do mesmo software com suporte em versões anteriores do MBAM.</span><span class="sxs-lookup"><span data-stu-id="47f51-143">MBAM 2.5 SP1 adds support for Windows 10 and Windows Server 2016, in addition to the same software that is supported in earlier versions of MBAM.</span></span>

<span data-ttu-id="47f51-144">O Windows 10 tem suporte no MBAM 2,5 e no MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="47f51-144">Windows 10 is supported in both MBAM 2.5 and MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="47f51-145">Suporte para Microsoft SQL Server 2014 SP1</span><span class="sxs-lookup"><span data-stu-id="47f51-145">Support for Microsoft SQL Server 2014 SP1</span></span>

<span data-ttu-id="47f51-146">O MBAM 2,5 SP1 adiciona suporte para o Microsoft SQL Server 2014 SP1, além do mesmo software com suporte em versões anteriores do MBAM.</span><span class="sxs-lookup"><span data-stu-id="47f51-146">MBAM 2.5 SP1 adds support for Microsoft SQL Server 2014 SP1, in addition to the same software that is supported in earlier versions of MBAM.</span></span>

### <span data-ttu-id="47f51-147">O MBAM não é mais fornecido com um MSI separado</span><span class="sxs-lookup"><span data-stu-id="47f51-147">MBAM no longer ships with separate MSI</span></span>

<span data-ttu-id="47f51-148">A partir do MBAM 2,5 SP1, um MSI separado não está mais incluído no produto MBAM.</span><span class="sxs-lookup"><span data-stu-id="47f51-148">Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="47f51-149">No entanto, você pode extrair o MSI do arquivo executável (. exe) que está incluído no produto.</span><span class="sxs-lookup"><span data-stu-id="47f51-149">However, you can extract the MSI from the executable file (.exe) that is included with the product.</span></span>

### <span data-ttu-id="47f51-150">MBAM pode caução OwnerAuth senhas sem possuir o TPM</span><span class="sxs-lookup"><span data-stu-id="47f51-150">MBAM can escrow OwnerAuth passwords without owning the TPM</span></span>

<span data-ttu-id="47f51-151">Anteriormente, se MBAM não possuía o TPM, o OwnerAuth TPM não pôde ser recontado para o banco de dados do MBAM.</span><span class="sxs-lookup"><span data-stu-id="47f51-151">Previously, if MBAM did not own the TPM, the TPM OwnerAuth could not be escrowed to the MBAM database.</span></span> <span data-ttu-id="47f51-152">Para configurar o MBAM para possuir o TPM e armazenar as senhas, você precisava desabilitar o provisionamento automático do TPM e limpar o TPM no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="47f51-152">To configure MBAM to own the TPM and to store the passwords, you had to disable TPM auto-provisioning and clear the TPM on the client computer.</span></span>

<span data-ttu-id="47f51-153">No Windows 8 e versões posteriores, o MBAM 2,5 SP1 agora pode caução nas senhas do OwnerAuth sem ter o TPM.</span><span class="sxs-lookup"><span data-stu-id="47f51-153">In Windows 8 and higher, MBAM 2.5 SP1 can now escrow the OwnerAuth passwords without owning the TPM.</span></span> <span data-ttu-id="47f51-154">Durante a inicialização do serviço, as consultas MBAM para ver se o TPM já tem proprietário e, em caso afirmativo, ele solicita as senhas do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="47f51-154">During service startup, MBAM queries to see if the TPM is already owned and if so, it requests the passwords from the operating system.</span></span> <span data-ttu-id="47f51-155">As senhas são então em caução para o banco de dados do MBAM.</span><span class="sxs-lookup"><span data-stu-id="47f51-155">The passwords are then escrowed to the MBAM database.</span></span> <span data-ttu-id="47f51-156">Além disso, a política de grupo deve ser definida para impedir que o OwnerAuth seja excluído localmente.</span><span class="sxs-lookup"><span data-stu-id="47f51-156">In addition, Group Policy must be set to prevent the OwnerAuth from being deleted locally.</span></span>

<span data-ttu-id="47f51-157">No Windows 7, MBAM deve possuir o TPM para fazer automaticamente a caução do TPM OwnerAuth informações no banco de dados do MBAM.</span><span class="sxs-lookup"><span data-stu-id="47f51-157">In Windows 7, MBAM must own the TPM to automatically escrow TPM OwnerAuth information in the MBAM database.</span></span> <span data-ttu-id="47f51-158">Se o MBAM não tiver o backup do TPM e do Active Directory (AD) do TPM configurado por meio da política de grupo, você deverá usar os **cmdlets de importação de dados do Active Directory do MBAM (AD)** para copiar os OWNERAUTH do TPM do AD para o banco de dados do MBAM.</span><span class="sxs-lookup"><span data-stu-id="47f51-158">If MBAM does not own the TPM and Active Directory (AD) backup of the TPM is configured through Group Policy, you must use the **MBAM Active Directory (AD) Data Import cmdlets** to copy TPM OwnerAuth from AD into the MBAM database.</span></span> <span data-ttu-id="47f51-159">Estes são cinco novos cmdlets do PowerShell que preenchem bancos de dados do MBAM com as informações de recuperação de volume e de proprietário do TPM armazenadas no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="47f51-159">These are five new PowerShell cmdlets that pre-populate MBAM databases with the Volume recovery and TPM owner information stored in Active Directory.</span></span>

<span data-ttu-id="47f51-160">Para obter mais informações, consulte [MBAM 2,5 considerações de segurança](mbam-25-security-considerations.md#bkmk-tpm).</span><span class="sxs-lookup"><span data-stu-id="47f51-160">For more information, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm).</span></span>

### <span data-ttu-id="47f51-161">O MBAM pode desbloquear automaticamente o TPM após um bloqueio</span><span class="sxs-lookup"><span data-stu-id="47f51-161">MBAM can automatically unlock the TPM after a lockout</span></span>

<span data-ttu-id="47f51-162">Em computadores que executam o TPM 1,2, agora você pode configurar o MBAM para desbloquear automaticamente o TPM em caso de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="47f51-162">On computers running TPM 1.2, you can now configure MBAM to automatically unlock the TPM in case of a lockout.</span></span> <span data-ttu-id="47f51-163">Se o recurso de redefinição automática do bloqueio do TPM estiver habilitado, o MBAM pode detectar que um usuário está bloqueado e obter a senha do OwnerAuth do banco de dados do MBAM para desbloquear automaticamente o TPM para o usuário.</span><span class="sxs-lookup"><span data-stu-id="47f51-163">If the TPM lockout auto reset feature is enabled, MBAM can detect that a user is locked out and then get the OwnerAuth password from the MBAM database to automatically unlock the TPM for the user.</span></span>

<span data-ttu-id="47f51-164">Esse recurso deve ser habilitado no lado do servidor e na política de grupo no lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="47f51-164">This feature must be enabled on both the server side and in Group Policy on the client side.</span></span> <span data-ttu-id="47f51-165">Para obter mais informações, consulte [MBAM 2,5 considerações de segurança](mbam-25-security-considerations.md#bkmk-autounlock).</span><span class="sxs-lookup"><span data-stu-id="47f51-165">For more information, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-autounlock).</span></span>

### <span data-ttu-id="47f51-166">Suporte para protetores de senha numérica do BitLocker compatíveis com FIPS</span><span class="sxs-lookup"><span data-stu-id="47f51-166">Support for FIPS-compliant BitLocker numerical password protectors</span></span>

<span data-ttu-id="47f51-167">No MBAM 2.5, foi adicionada para as chaves de recuperação do BitLocker compatíveis com o padrão FIPS (Federal Information Processing Standard) em dispositivos que executam o sistema operacional Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="47f51-167">In MBAM2.5, support was added for Federal Information Processing Standard (FIPS)-compliant BitLocker recovery keys on devices running the Windows 8.1 operating system.</span></span> <span data-ttu-id="47f51-168">No entanto, o Windows não implementou as chaves de recuperação compatíveis com FIPS no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="47f51-168">However, Windows did not implement FIPS-compliant recovery keys in Windows 7.</span></span> <span data-ttu-id="47f51-169">Portanto, os dispositivos Windows 7 e Windows 8 ainda exigem um protetor de agente de recuperação de dados (DRA) para recuperação.</span><span class="sxs-lookup"><span data-stu-id="47f51-169">Therefore, Windows 7 and Windows 8 devices still required a Data Recovery Agent (DRA) protector for recovery.</span></span>

<span data-ttu-id="47f51-170">A equipe do Windows tem chaves de recuperação compatíveis com FIPS com um hotfix e o MBAM 2,5 SP1 também adicionou suporte para elas.</span><span class="sxs-lookup"><span data-stu-id="47f51-170">The Windows team has backported FIPS-compliant recovery keys with a hotfix, and MBAM 2.5 SP1 has added support for them as well.</span></span>

<span data-ttu-id="47f51-171">**Observação**  Os computadores cliente que executam o sistema operacional Windows8 ainda exigem um protetor de DRA, pois o hotfix não era reportado para esse sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="47f51-171">**Note** Client computers that are running the Windows8 operating system still require a DRA protector since the hotfix was not backported to that OS.</span></span> <span data-ttu-id="47f51-172">Consulte [pacote de hotfix 2 para administração e monitoramento do bitlocker 2,5](https://support.microsoft.com/kb/3015477) para baixar e instalar o hotfix do BitLocker para computadores com o Windows 7 e o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="47f51-172">See [Hotfix Package 2 for BitLocker Administration and Monitoring 2.5](https://support.microsoft.com/kb/3015477) to download and install the BitLocker hotfix for Windows 7 and Windows 8 computers.</span></span> <span data-ttu-id="47f51-173">Para obter informações sobre DRA, consulte [usando agentes de recuperação de dados com o BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).</span><span class="sxs-lookup"><span data-stu-id="47f51-173">For information about DRA, see [Using Data Recovery Agents with BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).</span></span>

 

<span data-ttu-id="47f51-174">Para habilitar a conformidade com FIPS em sua organização, você deve configurar as configurações de política de grupo do padrão FIPS (padrão de processamento de informações federais).</span><span class="sxs-lookup"><span data-stu-id="47f51-174">To enable FIPS compliance in your organization, you must configure the Federal Information Processing Standard (FIPS) Group Policy settings.</span></span> <span data-ttu-id="47f51-175">Para obter instruções de configuração, consulte [configurações de política de grupo BitLocker](https://go.microsoft.com/fwlink/?LinkId=393560).</span><span class="sxs-lookup"><span data-stu-id="47f51-175">For configuration instructions, see [BitLocker Group Policy Settings](https://go.microsoft.com/fwlink/?LinkId=393560).</span></span>

### <span data-ttu-id="47f51-176">Personalizar mensagem de recuperação antes da inicialização e URL com a nova configuração de política de grupo</span><span class="sxs-lookup"><span data-stu-id="47f51-176">Customize pre-boot recovery message and URL with new Group Policy setting</span></span>

<span data-ttu-id="47f51-177">Uma nova configuração de política de grupo, **Configurar a URL e a mensagem de recuperação antes da inicialização**, permite que você configure uma mensagem de recuperação personalizada ou ESPECIFIQUE uma URL que, em seguida, será exibida na tela pré-inicialização de recuperação do BitLocker quando a unidade do sistema operacional estiver bloqueada.</span><span class="sxs-lookup"><span data-stu-id="47f51-177">A new Group Policy setting, **Configure pre-boot recovery message and URL**, lets you configure a custom recovery message or specify a URL that is then displayed on the pre-boot BitLocker recovery screen when the OS drive is locked.</span></span> <span data-ttu-id="47f51-178">Essa configuração só está disponível em computadores cliente que executam o Windows 10.</span><span class="sxs-lookup"><span data-stu-id="47f51-178">This setting is only available on client computers running Windows 10.</span></span>

<span data-ttu-id="47f51-179">Se você habilitar essa configuração de política, poderá selecionar uma destas opções para a mensagem de recuperação antes da inicialização:</span><span class="sxs-lookup"><span data-stu-id="47f51-179">If you enable this policy setting, you can you can select one of these options for the pre-boot recovery message:</span></span>

-   <span data-ttu-id="47f51-180">**Usar mensagem de recuperação personalizada**: Selecione esta opção para incluir uma mensagem personalizada na tela pré-inicialização de recuperação do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="47f51-180">**Use custom recovery message**: Select this option to include a custom message in the pre-boot BitLocker recovery screen.</span></span>

-   <span data-ttu-id="47f51-181">**Usar a URL de recuperação personalizada**: Selecione esta opção para substituir a URL padrão que é exibida na tela pré-inicializar do BitLocker Recovery.</span><span class="sxs-lookup"><span data-stu-id="47f51-181">**Use custom recovery URL**: Select this option to replace the default URL that is displayed in the pre-boot BitLocker recovery screen.</span></span>

-   <span data-ttu-id="47f51-182">**Usar a mensagem e a URL de recuperação padrão**: Selecione esta opção para exibir a mensagem e a URL de recuperação do BitLocker padrão na tela pré-inicialização de recuperação do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="47f51-182">**Use default recovery message and URL**: Select this option to display the default BitLocker recovery message and URL in the pre-boot BitLocker recovery screen.</span></span> <span data-ttu-id="47f51-183">Se você configurou anteriormente uma mensagem ou URL de recuperação personalizada e quer reverter para a mensagem padrão, você deve habilitar essa política e selecionar essa opção.</span><span class="sxs-lookup"><span data-stu-id="47f51-183">If you previously configured a custom recovery message or URL and want to revert to the default message, you must enable this policy and select this option.</span></span>

<span data-ttu-id="47f51-184">A nova configuração de política de grupo está localizada no seguinte nó de GPO: modelos administrativos de políticas de **configuração de computador** &gt; **Policies** &gt; **Administrative Templates** &gt; **componentes do Windows** &gt; **MDOP MBAM (gerenciamento de BitLocker)** &gt; **unidade de sistema operacional**.</span><span class="sxs-lookup"><span data-stu-id="47f51-184">The new Group Policy setting is located in the following GPO node: **Computer Configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)** &gt; **Operating System Drive**.</span></span> <span data-ttu-id="47f51-185">Para obter mais informações, consulte [planejando os requisitos da política de grupo do MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="47f51-185">For more information, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>

### <span data-ttu-id="47f51-186">MBAM adicionou suporte para criptografia de espaço usado</span><span class="sxs-lookup"><span data-stu-id="47f51-186">MBAM added support for Used Space Encryption</span></span>

<span data-ttu-id="47f51-187">No MBAM 2,5 SP1, se você habilitar a criptografia de espaço usado via política de grupo do BitLocker, o cliente MBAM honrará-a.</span><span class="sxs-lookup"><span data-stu-id="47f51-187">In MBAM 2.5 SP1, if you enable Used Space Encryption via BitLocker Group Policy, the MBAM Client honors it.</span></span>

<span data-ttu-id="47f51-188">Essa configuração de política de grupo é chamada **impor tipo de criptografia de unidade em unidades do sistema operacional** e está localizada no nó do GPO a seguir: modelos administrativos de **configuração de computador** &gt; **Administrative Templates** &gt; **componentes do Windows componentes** do &gt; **BitLocker Drive Encryption** &gt; **sistema operacional**da criptografia de unidade de disco rígido</span><span class="sxs-lookup"><span data-stu-id="47f51-188">This Group Policy setting is called **Enforce drive encryption type on operating system drives** and is located in the following GPO node: **Computer Configuration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **BitLocker Drive Encryption** &gt; **Operating System Drives**.</span></span> <span data-ttu-id="47f51-189">Se você habilitar essa política e selecionar o tipo de criptografia como **apenas criptografia de espaço usado**, o MBAM honrará a política e o BitLocker somente criptografará o espaço em disco usado no volume.</span><span class="sxs-lookup"><span data-stu-id="47f51-189">If you enable this policy and select the encryption type as **Used Space Only encryption**, MBAM will honor the policy and BitLocker will only encrypt disk space that is used on the volume.</span></span>

<span data-ttu-id="47f51-190">Para obter mais informações, consulte [planejando os requisitos da política de grupo do MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="47f51-190">For more information, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>

### <span data-ttu-id="47f51-191">Suporte do cliente MBAM para discos rígidos criptografados</span><span class="sxs-lookup"><span data-stu-id="47f51-191">MBAM Client support for Encrypted Hard Drives</span></span>

<span data-ttu-id="47f51-192">O MBAM dá suporte ao BitLocker em discos rígidos criptografados que atendem aos requisitos de especificação do TCG para o Opal e com os padrões IEEE 1667.</span><span class="sxs-lookup"><span data-stu-id="47f51-192">MBAM supports BitLocker on Encrypted Hard Drives that meet TCG specification requirements for Opal as well as IEEE 1667 standards.</span></span> <span data-ttu-id="47f51-193">Quando o BitLocker estiver habilitado nesses dispositivos, ele irá gerar chaves e executar funções de gerenciamento na unidade criptografada.</span><span class="sxs-lookup"><span data-stu-id="47f51-193">When BitLocker is enabled on these devices, it will generate keys and perform management functions on the encrypted drive.</span></span> <span data-ttu-id="47f51-194">Para obter mais informações, consulte [unidade de disco rígido criptografado](https://technet.microsoft.com/library/hh831627.aspx) .</span><span class="sxs-lookup"><span data-stu-id="47f51-194">See [Encrypted Hard Drive](https://technet.microsoft.com/library/hh831627.aspx) for more information.</span></span>

### <span data-ttu-id="47f51-195">A configuração de delegação não é mais necessária ao registrar SPNs</span><span class="sxs-lookup"><span data-stu-id="47f51-195">Delegation configuration no longer required when registering SPNs</span></span>

<span data-ttu-id="47f51-196">A necessidade de configurar a delegação restrita para SPNs que você se registra para a conta do pool de aplicativos não é mais necessária no MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="47f51-196">The requirement to configure constrained delegation for SPNs that you register for the application pool account is no longer necessary in MBAM 2.5 SP1.</span></span> <span data-ttu-id="47f51-197">No entanto, ainda é um requisito para o MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="47f51-197">However, it is still a requirement for MBAM 2.5.</span></span>

### <span data-ttu-id="47f51-198">Habilitar o BitLocker usando o MBAM como parte de uma implantação do Windows</span><span class="sxs-lookup"><span data-stu-id="47f51-198">Enable BitLocker using MBAM as Part of a Windows Deployment</span></span>

<span data-ttu-id="47f51-199">No MBAM 2,5 SP1, você pode usar um script do PowerShell para configurar a criptografia de unidade de disco BitLocker e as chaves de recuperação de caução para o servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="47f51-199">In MBAM 2.5 SP1, you can use a PowerShell script to configure BitLocker drive encryption and escrow recovery keys to the MBAM Server.</span></span>

<span data-ttu-id="47f51-200">Para obter mais informações, consulte [como habilitar o BitLocker usando o MBAM como parte de uma implantação do Windows](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)</span><span class="sxs-lookup"><span data-stu-id="47f51-200">For more information, see [How to Enable BitLocker by Using MBAM as Part of a Windows Deployment](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)</span></span>

### <span data-ttu-id="47f51-201">O portal de autoatendimento pode ser personalizado usando o PowerShell ou o assistente para personalização do SSP</span><span class="sxs-lookup"><span data-stu-id="47f51-201">Self-Service Portal can be customized by using either PowerShell or the SSP customization wizard</span></span>

<span data-ttu-id="47f51-202">A partir do MBAM 2,5 SP1, o portal de autoatendimento pode ser configurado usando o assistente para personalização e usando o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="47f51-202">As of MBAM 2.5 SP1, the Self-Service Portal can be configured by using the customization wizard as well as by using PowerShell.</span></span> <span data-ttu-id="47f51-203">Veja [como configurar os aplicativos Web do MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="47f51-203">See [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>

### <span data-ttu-id="47f51-204">O navegador da Web não é mais intencionalmente executado como administrador</span><span class="sxs-lookup"><span data-stu-id="47f51-204">Web browser no longer unintentionally runs as administrator</span></span>

<span data-ttu-id="47f51-205">Um problema no MBAM 2,5 causou links de ajuda na ferramenta de configuração do servidor para fazer com que as janelas do navegador sejam abertas com direitos de administrador.</span><span class="sxs-lookup"><span data-stu-id="47f51-205">An issue in MBAM 2.5 caused help links in the Server Configuration tool to cause browser windows to open with administrator rights.</span></span> <span data-ttu-id="47f51-206">Este problema foi corrigido no MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="47f51-206">This issue is fixed in MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="47f51-207">Não precisa mais fazer o download dos arquivos JavaScript para configurar o portal de autoatendimento quando a CDN estiver inacessível</span><span class="sxs-lookup"><span data-stu-id="47f51-207">No longer need to download the JavaScript files to configure the Self-Service Portal when the CDN is inaccessible</span></span>

<span data-ttu-id="47f51-208">No MBAM 2,5 e anterior, os arquivos jQuery usados para a configuração do portal de autoatendimento precisavam ser baixados da CDN antecipadamente se os clientes que acessarem o portal de autoatendimento não tivessem acesso à Internet.</span><span class="sxs-lookup"><span data-stu-id="47f51-208">In MBAM 2.5 and earlier, the jQuery files used for configuration of the Self-Service Portal had to be downloaded from the CDN in advance if clients accessing the Self-Service Portal did not have internet access.</span></span> <span data-ttu-id="47f51-209">No MBAM 2,5 SP1, todos os arquivos JavaScript são incluídos no produto, portanto o download é desnecessário.</span><span class="sxs-lookup"><span data-stu-id="47f51-209">In MBAM 2.5 SP1, all JavaScript files are included in the product, so downloading them is unnecessary.</span></span>

### <span data-ttu-id="47f51-210">Os relatórios podem ser abertos no construtor de Relatórios 3,0</span><span class="sxs-lookup"><span data-stu-id="47f51-210">Reports can be opened in Report Builder 3.0</span></span>

<span data-ttu-id="47f51-211">No MBAM 2,5 SP1, os relatórios foram atualizados para o esquema mais recente de linguagem de definição de relatório, permitindo que os usuários abram e personalizem os relatórios no construtor de Relatórios 3,0 e salve-os imediatamente sem danificar o arquivo de relatório.</span><span class="sxs-lookup"><span data-stu-id="47f51-211">In MBAM 2.5 SP1, the reports have been updated to the latest report definition language schema, allowing users to open and customize the reports in Report Builder 3.0 and save them immediately without corrupting the report file.</span></span>

### <span data-ttu-id="47f51-212">Novos cmdlets do PowerShell</span><span class="sxs-lookup"><span data-stu-id="47f51-212">New PowerShell cmdlets</span></span>

<span data-ttu-id="47f51-213">Os novos cmdlets do PowerShell para MBAM 2,5 SP1 permitem que você configure e gerencie diferentes recursos do MBAM, incluindo bancos de dados, relatórios e aplicativos Web.</span><span class="sxs-lookup"><span data-stu-id="47f51-213">New PowerShell cmdlets for MBAM 2.5 SP1 enable you to configure and manage different MBAM features, including databases, reports, and web applications.</span></span> <span data-ttu-id="47f51-214">Cada recurso tem um cmdlet do PowerShell correspondente que você pode usar para habilitar ou desabilitar recursos ou para obter informações sobre o recurso.</span><span class="sxs-lookup"><span data-stu-id="47f51-214">Each feature has a corresponding PowerShell cmdlet that you can use to enable or disable features, or to get information about the feature.</span></span>

<span data-ttu-id="47f51-215">Os seguintes cmdlets foram implementados para o MBAM 2,5 SP1:</span><span class="sxs-lookup"><span data-stu-id="47f51-215">The following cmdlets have been implemented for MBAM 2.5 SP1:</span></span>

-   <span data-ttu-id="47f51-216">Write-MbamTpmInformation</span><span class="sxs-lookup"><span data-stu-id="47f51-216">Write-MbamTpmInformation</span></span>

-   <span data-ttu-id="47f51-217">Write-MbamRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="47f51-217">Write-MbamRecoveryInformation</span></span>

-   <span data-ttu-id="47f51-218">Leitura-ADTpmInformation</span><span class="sxs-lookup"><span data-stu-id="47f51-218">Read-ADTpmInformation</span></span>

-   <span data-ttu-id="47f51-219">Leitura-ADRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="47f51-219">Read-ADRecoveryInformation</span></span>

-   <span data-ttu-id="47f51-220">Write-MbamComputerUser</span><span class="sxs-lookup"><span data-stu-id="47f51-220">Write-MbamComputerUser</span></span>

<span data-ttu-id="47f51-221">Os parâmetros a seguir foram implementados nos cmdlets Enable-MbamWebApplication e Test-MbamWebApplication para MBAM 2,5 SP1:</span><span class="sxs-lookup"><span data-stu-id="47f51-221">The following parameters have been implemented in the Enable-MbamWebApplication and Test-MbamWebApplication cmdlets for MBAM 2.5 SP1:</span></span>

-   <span data-ttu-id="47f51-222">DataMigrationAccessGroup</span><span class="sxs-lookup"><span data-stu-id="47f51-222">DataMigrationAccessGroup</span></span>

-   <span data-ttu-id="47f51-223">TpmAutoUnlock</span><span class="sxs-lookup"><span data-stu-id="47f51-223">TpmAutoUnlock</span></span>

<span data-ttu-id="47f51-224">Para obter informações sobre os cmdlets, consulte [considerações de segurança do MBAM 2,5](mbam-25-security-considerations.md) e [ajuda do cmdlet de administração e monitoramento do Microsoft BitLocker](https://technet.microsoft.com/library/dn720418.aspx).</span><span class="sxs-lookup"><span data-stu-id="47f51-224">For information about the cmdlets, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md) and [Microsoft Bitlocker Administration and Monitoring Cmdlet Help](https://technet.microsoft.com/library/dn720418.aspx).</span></span>

### <span data-ttu-id="47f51-225">O MBAM Agent detecta o modo de apresentação</span><span class="sxs-lookup"><span data-stu-id="47f51-225">MBAM agent detects presentation mode</span></span>

<span data-ttu-id="47f51-226">O agente MBAM pode detectar quando o computador está no modo de apresentação e evitar invocar a interface do usuário do MBAM nesse momento.</span><span class="sxs-lookup"><span data-stu-id="47f51-226">The MBAM agent can detect when the computer is in presentation mode and avoid invoking the MBAM UI at that time.</span></span>

### <span data-ttu-id="47f51-227">O serviço de agente MBAM agora está configurado para usar o início atrasado</span><span class="sxs-lookup"><span data-stu-id="47f51-227">MBAM agent service now configured to use delayed start</span></span>

<span data-ttu-id="47f51-228">Após a instalação, o serviço definirá o serviço do MBAM Agent para usar o início atrasado, reduzindo a quantidade de tempo necessária para iniciar o Windows.</span><span class="sxs-lookup"><span data-stu-id="47f51-228">After installation, the service will now set the MBAM agent service to use delayed start, decreasing the amount of time it takes to start Windows.</span></span>

### <span data-ttu-id="47f51-229">Volumes de dados fixos bloqueados agora se reportam como em conformidade</span><span class="sxs-lookup"><span data-stu-id="47f51-229">Locked Fixed Data volumes now report as Compliant</span></span>

<span data-ttu-id="47f51-230">A lógica de cálculo de conformidade dos volumes de "dados fixos bloqueados" foi alterada para relatar os volumes como "compatível", mas com um estado de protetor e estado de criptografia de "desconhecido" e com um detalhe de status de conformidade de "volume está bloqueado".</span><span class="sxs-lookup"><span data-stu-id="47f51-230">The compliance calculation logic for "Locked Fixed Data" volumes has been changed to report the volumes as "Compliant," but with a Protector State and Encryption State of "Unknown" and with a Compliance Status Detail of "Volume is locked".</span></span> <span data-ttu-id="47f51-231">Anteriormente, os volumes bloqueados eram relatados como "não conforme", um estado de protetor de "criptografado", um estado de criptografia de "desconhecido" e um detalhe de status de conformidade de "um erro desconhecido".</span><span class="sxs-lookup"><span data-stu-id="47f51-231">Previously, locked volumes were reported as “Non-Compliant”, a Protector State of "Encrypted", an Encryption State of "Unknown", and a Compliance Status Detail of "An unknown error".</span></span>


## <span data-ttu-id="47f51-232">Como obter tecnologias do MDOP</span><span class="sxs-lookup"><span data-stu-id="47f51-232">How to Get MDOP Technologies</span></span>


<span data-ttu-id="47f51-233">O MBAM é parte do Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="47f51-233">MBAM is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="47f51-234">O MDOP faz parte do programa Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="47f51-234">MDOP is part of the Microsoft Software Assurance program.</span></span> <span data-ttu-id="47f51-235">Para obter mais informações sobre o programa Microsoft Software Assurance e como adquirir o MDOP, consulte [como faço para obter o MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="47f51-235">For more information about the Microsoft Software Assurance program and how to acquire the MDOP, see [How Do I Get MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="47f51-236">Notas de versão do MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="47f51-236">MBAM 2.5 SP1 Release Notes</span></span>


<span data-ttu-id="47f51-237">Para obter mais informações e últimas notícias que não estão incluídas nesta documentação, confira [notas de versão do MBAM 2,5 SP1](release-notes-for-mbam-25-sp1.md).</span><span class="sxs-lookup"><span data-stu-id="47f51-237">For more information and late-breaking news that is not included in this documentation, see [Release Notes for MBAM 2.5 SP1](release-notes-for-mbam-25-sp1.md).</span></span>

## <span data-ttu-id="47f51-238">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="47f51-238">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="47f51-239">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="47f51-239">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="47f51-240">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="47f51-240">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

## <span data-ttu-id="47f51-241">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="47f51-241">Related topics</span></span>


[<span data-ttu-id="47f51-242">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="47f51-242">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](index.md)

[<span data-ttu-id="47f51-243">Introdução ao MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="47f51-243">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

 

 





