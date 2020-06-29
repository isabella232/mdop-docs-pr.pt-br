---
title: Sobre o MBAM 2.5
description: Sobre o MBAM 2.5
author: dansimp
ms.assetid: 1ce218ec-4d2e-4a75-8d1a-68d737a8f3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d4c9ff0bc5ee3f7dc51a56cc428081a7c3783694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799427"
---
# <span data-ttu-id="0a885-103">Sobre o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="0a885-103">About MBAM 2.5</span></span>


<span data-ttu-id="0a885-104">O monitoramento e a administração do Microsoft BitLocker (MBAM) 2,5 fornecem uma interface administrativa simplificada para a criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0a885-104">Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 provides a simplified administrative interface for BitLocker Drive Encryption.</span></span> <span data-ttu-id="0a885-105">O BitLocker oferece proteção aprimorada contra roubo de dados ou exposição de dados para computadores perdidos ou roubados.</span><span class="sxs-lookup"><span data-stu-id="0a885-105">BitLocker offers enhanced protection against data theft or data exposure for computers that are lost or stolen.</span></span> <span data-ttu-id="0a885-106">O BitLocker criptografa todos os dados armazenados nos volumes e unidades de sistema operacional Windows e nas unidades de dados configurados.</span><span class="sxs-lookup"><span data-stu-id="0a885-106">BitLocker encrypts all data that is stored on the Windows operating system volumes and drives and configured data drives.</span></span>

## <span data-ttu-id="0a885-107">Visão geral do MBAM</span><span class="sxs-lookup"><span data-stu-id="0a885-107">Overview of MBAM</span></span>


<span data-ttu-id="0a885-108">O MBAM 2,5 tem os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="0a885-108">MBAM 2.5 has the following features:</span></span>

-   <span data-ttu-id="0a885-109">Permite que os administradores automatizem o processo de criptografar volumes em computadores cliente em toda a empresa.</span><span class="sxs-lookup"><span data-stu-id="0a885-109">Enables administrators to automate the process of encrypting volumes on client computers across the enterprise.</span></span>

-   <span data-ttu-id="0a885-110">Permite que os agentes de segurança determinem rapidamente o estado de conformidade de computadores individuais ou até mesmo da empresa em si.</span><span class="sxs-lookup"><span data-stu-id="0a885-110">Enables security officers to quickly determine the compliance state of individual computers or even of the enterprise itself.</span></span>

-   <span data-ttu-id="0a885-111">Fornece gerenciamento centralizado de relatório e de hardware com o Microsoft System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0a885-111">Provides centralized reporting and hardware management with Microsoft System Center Configuration Manager.</span></span>

-   <span data-ttu-id="0a885-112">Reduz a carga de trabalho no suporte técnico para ajudar os usuários finais com o PIN do BitLocker e solicitações de chave de recuperação.</span><span class="sxs-lookup"><span data-stu-id="0a885-112">Reduces the workload on the Help Desk to assist end users with BitLocker PIN and recovery key requests.</span></span>

-   <span data-ttu-id="0a885-113">Permite aos usuários finais recuperar dispositivos criptografados de forma independente, usando o Portal de Autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="0a885-113">Enables end users to recover encrypted devices independently by using the Self-Service Portal.</span></span>

-   <span data-ttu-id="0a885-114">Permite que os gerentes de segurança auditem facilmente o acesso para recuperar informações importantes.</span><span class="sxs-lookup"><span data-stu-id="0a885-114">Enables security officers to easily audit access to recover key information.</span></span>

-   <span data-ttu-id="0a885-115">Permite que os usuários do Windows Enterprise continuem a trabalhar em qualquer lugar com a garantia de que seus dados corporativos estão protegidos.</span><span class="sxs-lookup"><span data-stu-id="0a885-115">Empowers Windows Enterprise users to continue working anywhere with the assurance that their corporate data is protected.</span></span>

<span data-ttu-id="0a885-116">O MBAM impõe as opções de política de criptografia BitLocker definidas para a sua empresa, monitora a conformidade dos computadores cliente com essas políticas e relata sobre o status de criptografia dos computadores da empresa e do indivíduo.</span><span class="sxs-lookup"><span data-stu-id="0a885-116">MBAM enforces the BitLocker encryption policy options that you set for your enterprise, monitors the compliance of client computers with those policies, and reports on the encryption status of the enterprise’s and individual’s computers.</span></span> <span data-ttu-id="0a885-117">Além disso, o MBAM permite que você acesse as informações da chave de recuperação quando os usuários esquecem o PIN ou a senha, ou quando os registros de inicialização ou do BIOS são alterados.</span><span class="sxs-lookup"><span data-stu-id="0a885-117">In addition, MBAM lets you access the recovery key information when users forget their PIN or password, or when their BIOS or boot records change.</span></span>

<span data-ttu-id="0a885-118">Os seguintes grupos podem estar interessados em usar o MBAM para gerenciar o BitLocker:</span><span class="sxs-lookup"><span data-stu-id="0a885-118">The following groups might be interested in using MBAM to manage BitLocker:</span></span>

-   <span data-ttu-id="0a885-119">Administradores, profissionais de segurança de ti e responsáveis pela conformidade responsáveis por garantir que os dados confidenciais não sejam divulgados sem autorização</span><span class="sxs-lookup"><span data-stu-id="0a885-119">Administrators, IT security professionals, and compliance officers who are responsible for ensuring that confidential data is not disclosed without authorization</span></span>

-   <span data-ttu-id="0a885-120">Administradores que são responsáveis por segurança de computador em escritórios remotos ou filiais</span><span class="sxs-lookup"><span data-stu-id="0a885-120">Administrators who are responsible for computer security in remote or branch offices</span></span>

-   <span data-ttu-id="0a885-121">Administradores responsáveis pelos computadores cliente que executam o Windows</span><span class="sxs-lookup"><span data-stu-id="0a885-121">Administrators who are responsible for client computers that are running Windows</span></span>

<span data-ttu-id="0a885-122">**Observação**  O BitLocker não é explicado em detalhes nesta documentação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0a885-122">**Note** BitLocker is not explained in detail in this MBAM documentation.</span></span> <span data-ttu-id="0a885-123">Para obter mais informações, consulte [visão geral da criptografia de unidade BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span><span class="sxs-lookup"><span data-stu-id="0a885-123">For more information, see [BitLocker Drive Encryption Overview](https://go.microsoft.com/fwlink/p/?LinkId=225013).</span></span>

 

## <a href="" id="what-s-new-in-mbam-2-5"></a><span data-ttu-id="0a885-124">O que há de novo no MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="0a885-124">What’s new in MBAM 2.5</span></span>


<span data-ttu-id="0a885-125">Esta seção descreve os novos recursos do MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="0a885-125">This section describes the new features in MBAM 2.5.</span></span>

### <span data-ttu-id="0a885-126">Suporte para o Microsoft SQL Server 2014</span><span class="sxs-lookup"><span data-stu-id="0a885-126">Support for Microsoft SQL Server 2014</span></span>

<span data-ttu-id="0a885-127">O MBAM adiciona suporte ao Microsoft SQL Server 2014, além do mesmo software com suporte em versões anteriores do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0a885-127">MBAM adds support for Microsoft SQL Server 2014, in addition to the same software that is supported in earlier versions of MBAM.</span></span>

### <a href="" id="-------------mbam-group-policy-templates-downloaded-separately"></a> <span data-ttu-id="0a885-128">MBAM de modelos de política de grupo baixados separadamente</span><span class="sxs-lookup"><span data-stu-id="0a885-128">MBAM Group Policy Templates downloaded separately</span></span>

<span data-ttu-id="0a885-129">Os modelos de política de grupo do MBAM devem ser baixados separadamente da instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0a885-129">The MBAM Group Policy Templates must be downloaded separately from the MBAM installation.</span></span> <span data-ttu-id="0a885-130">Em versões anteriores do MBAM, o instalador do MBAM incluiu um modelo de política de MBAM, que continha os objetos de política de grupo (GPOs) necessários do MBAM que definem as configurações de implementação do MBAM para a criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0a885-130">In previous versions of MBAM, the MBAM installer included an MBAM Policy Template, which contained the required MBAM-specific Group Policy Objects (GPOs) that define MBAM implementation settings for BitLocker Drive Encryption.</span></span> <span data-ttu-id="0a885-131">Esses GPOs foram removidos do instalador do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0a885-131">These GPOs have been removed from the MBAM installer.</span></span> <span data-ttu-id="0a885-132">Agora, você pode baixar os GPOs em [como obter modelos de política de grupo do MDOP (. admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) e copiá-los para um servidor ou uma estação de trabalho antes de iniciar a instalação do cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0a885-132">You now download the GPOs from [How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941) and copy them to a server or workstation before you begin the MBAM Client installation.</span></span> <span data-ttu-id="0a885-133">Você pode copiar os modelos de política de grupo para qualquer servidor ou estação de trabalho que esteja executando uma versão com suporte do Windows Server ou sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="0a885-133">You can copy the Group Policy Templates to any server or workstation that is running a supported version of the Windows Server or Windows operating system.</span></span>

<span data-ttu-id="0a885-134">**Importante**  Não altere as configurações de política de grupo no nó de **criptografia de unidade de disco BitLocker** , ou o MBAM não funcionará corretamente.</span><span class="sxs-lookup"><span data-stu-id="0a885-134">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node, or MBAM will not work correctly.</span></span> <span data-ttu-id="0a885-135">Ao definir as configurações de política de grupo no nó **MDOP MBAM (gerenciamento de BitLocker)** , o MBAM configura automaticamente as configurações de criptografia de unidade de disco BitLocker para você.</span><span class="sxs-lookup"><span data-stu-id="0a885-135">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the BitLocker Drive Encryption settings for you.</span></span>

 

<span data-ttu-id="0a885-136">Os arquivos de modelo que você precisa copiar para um servidor ou estação de trabalho são:</span><span class="sxs-lookup"><span data-stu-id="0a885-136">The template files that you need to copy to a server or workstation are:</span></span>

-   <span data-ttu-id="0a885-137">BitLockerManagement. adml</span><span class="sxs-lookup"><span data-stu-id="0a885-137">BitLockerManagement.adml</span></span>

-   <span data-ttu-id="0a885-138">BitLockerManagement. admx</span><span class="sxs-lookup"><span data-stu-id="0a885-138">BitLockerManagement.admx</span></span>

-   <span data-ttu-id="0a885-139">BitLockerUserManagement. adml</span><span class="sxs-lookup"><span data-stu-id="0a885-139">BitLockerUserManagement.adml</span></span>

-   <span data-ttu-id="0a885-140">BitLockerUserManagement. admx</span><span class="sxs-lookup"><span data-stu-id="0a885-140">BitLockerUserManagement.admx</span></span>

<span data-ttu-id="0a885-141">Copie os arquivos de modelo para o local mais adequado às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="0a885-141">Copy the template files to the location that best meets your needs.</span></span> <span data-ttu-id="0a885-142">Para os arquivos específicos do idioma, que devem ser copiados para uma pasta específica do idioma, o console de gerenciamento de política de grupo é necessário para exibir os arquivos.</span><span class="sxs-lookup"><span data-stu-id="0a885-142">For the language-specific files, which must be copied to a language-specific folder, the Group Policy Management Console is required to view the files.</span></span>

- <span data-ttu-id="0a885-143">Para instalar os arquivos de modelo localmente em um servidor ou uma estação de trabalho, copie os arquivos para um dos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a885-143">To install the template files locally on a server or workstation, copy the files to one of the following locations.</span></span>

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left"><span data-ttu-id="0a885-144">Tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="0a885-144">File type</span></span></th>
  <th align="left"><span data-ttu-id="0a885-145">Local do arquivo</span><span class="sxs-lookup"><span data-stu-id="0a885-145">File location</span></span></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p><span data-ttu-id="0a885-146">idioma neutro (. admx)</span><span class="sxs-lookup"><span data-stu-id="0a885-146">language neutral (.admx)</span></span></p></td>
  <td align="left"><p><em><span data-ttu-id="0a885-147">% SystemRoot% </em> \policyDefinitions</span><span class="sxs-lookup"><span data-stu-id="0a885-147">%systemroot%</em>\policyDefinitions</span></span></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="0a885-148">específico do idioma (. adml)</span><span class="sxs-lookup"><span data-stu-id="0a885-148">language specific (.adml)</span></span></p></td>
  <td align="left"><p><em><span data-ttu-id="0a885-149">% SystemRoot% </em> \policyDefinitions [ <em> MUIculture </em> ] (por exemplo, o arquivo específico do idioma inglês dos EUA será armazenado em <em> % systemroot% &lt; /em &gt; policyDefinitions\en-US)</span><span class="sxs-lookup"><span data-stu-id="0a885-149">%systemroot%</em>\policyDefinitions[<em>MUIculture</em>] (for example, the U.S. English language specific file will be stored in <em>%systemroot%&lt;/em&gt;policyDefinitions\en-us)</span></span></p></td>
  </tr>
  </tbody>
  </table>

     

- <span data-ttu-id="0a885-150">Para disponibilizar os modelos para todos os administradores de política de grupo em um domínio, copie os arquivos para um dos locais a seguir em um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="0a885-150">To make the templates available to all Group Policy administrators in a domain, copy the files to one of the following locations on a domain controller.</span></span>

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left"><span data-ttu-id="0a885-151">Tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="0a885-151">File type</span></span></th>
  <th align="left"><span data-ttu-id="0a885-152">Local do arquivo do controlador de domínio</span><span class="sxs-lookup"><span data-stu-id="0a885-152">Domain controller file location</span></span></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p><span data-ttu-id="0a885-153">Idioma neutro (. admx)</span><span class="sxs-lookup"><span data-stu-id="0a885-153">Language neutral (.admx)</span></span></p></td>
  <td align="left"><p><em><span data-ttu-id="0a885-154">% SystemRoot% </em> sysvol\domain\policies\PolicyDefinitions</span><span class="sxs-lookup"><span data-stu-id="0a885-154">%systemroot%</em>sysvol\domain\policies\PolicyDefinitions</span></span></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="0a885-155">Específico do idioma (. adml)</span><span class="sxs-lookup"><span data-stu-id="0a885-155">Language specific (.adml)</span></span></p></td>
  <td align="left"><p><em><span data-ttu-id="0a885-156">% SystemRoot% </em> \sysvol\domain\policies\PolicyDefinitions [ <em> MUIculture </em> ] (por exemplo, o arquivo específico do idioma inglês dos EUA será armazenado em <em> % systemroot% </em> \sysvol\domain\policies\PolicyDefinitions\en-US)</span><span class="sxs-lookup"><span data-stu-id="0a885-156">%systemroot%</em>\sysvol\domain\policies\PolicyDefinitions[<em>MUIculture</em>] (for example, the U.S. English language-specific file will be stored in <em>%systemroot%</em>\sysvol\domain\policies\PolicyDefinitions\en-us)</span></span></p></td>
  </tr>
  </tbody>
  </table>

     

<span data-ttu-id="0a885-157">Para obter mais informações sobre arquivos de modelo, consulte o [guia passo a passo sobre como gerenciar arquivos ADMX de política de grupo](https://go.microsoft.com/fwlink/?LinkId=392818).</span><span class="sxs-lookup"><span data-stu-id="0a885-157">For more information about template files, see [Managing Group Policy ADMX Files Step-by-Step Guide](https://go.microsoft.com/fwlink/?LinkId=392818).</span></span>

### <span data-ttu-id="0a885-158">Capacidade de impor políticas de criptografia no sistema operacional e unidades de dados fixas</span><span class="sxs-lookup"><span data-stu-id="0a885-158">Ability to enforce encryption policies on operating system and fixed data drives</span></span>

<span data-ttu-id="0a885-159">O MBAM 2.5 permite que você aplique políticas de criptografia no sistema operacional e unidades de dados fixas para computadores em sua organização e limite o número de dias que os usuários finais podem solicitar um adiamento da necessidade de atender às políticas de criptografia do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0a885-159">MBAM2.5 enables you to enforce encryption policies on operating system and fixed data drives for computers in your organization and limit the number of days that end users can request a postponement of the requirement to comply with MBAM encryption policies.</span></span>

<span data-ttu-id="0a885-160">Para permitir que você configure a aplicação de políticas de criptografia, uma nova configuração de política de grupo, chamada de política de aplicação de criptografia, foi adicionada para unidades do sistema operacional e unidades de dados fixas.</span><span class="sxs-lookup"><span data-stu-id="0a885-160">To enable you to configure encryption policy enforcement, a new Group Policy setting, called Encryption Policy Enforcement Settings, has been added for operating system drives and fixed data drives.</span></span> <span data-ttu-id="0a885-161">Essa política é descrita na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a885-161">This policy is described in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0a885-162">Configuração da Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="0a885-162">Group Policy setting</span></span></th>
<th align="left"><span data-ttu-id="0a885-163">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a885-163">Description</span></span></th>
<th align="left"><span data-ttu-id="0a885-164">Nó de política de grupo usado para definir essa configuração</span><span class="sxs-lookup"><span data-stu-id="0a885-164">Group Policy node used to configure this setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0a885-165">Configurações de imposição de política de criptografia (unidade do sistema operacional)</span><span class="sxs-lookup"><span data-stu-id="0a885-165">Encryption Policy Enforcement Settings (Operating System Drive)</span></span></p></td>
<td align="left"><p><span data-ttu-id="0a885-166">Para essa configuração, use a opção <strong> Configurar o número de dias do período de cortesia não compatível para unidades do sistema operacional </strong> para configurar um período de cortesia.</span><span class="sxs-lookup"><span data-stu-id="0a885-166">For this setting, use the option <strong>Configure the number of noncompliance grace period days for operating system drives</strong> to configure a grace period.</span></span></p>
<p><span data-ttu-id="0a885-167">O período de carência especifica o número de dias pelos quais os usuários finais podem adiar a conformidade com as políticas do MBAM para a unidade do sistema operacional após a primeira detecção da unidade como não compatível.</span><span class="sxs-lookup"><span data-stu-id="0a885-167">The grace period specifies the number of days that end users can postpone compliance with MBAM policies for their operating system drive after the drive is first detected as noncompliant.</span></span></p>
<p><span data-ttu-id="0a885-168">Depois que o período de cortesia configurado expirar, os usuários não poderão adiar a ação necessária ou solicitar uma isenção a ele.</span><span class="sxs-lookup"><span data-stu-id="0a885-168">After the configured grace period expires, users cannot postpone the required action or request an exemption from it.</span></span></p>
<p><span data-ttu-id="0a885-169">Se a interação do usuário for necessária (por exemplo, se você estiver usando o TPM (Trusted Platform Module) + PIN ou usando um protetor de senha, será exibida uma caixa de diálogo e os usuários não poderão fechá-lo até fornecer as informações necessárias.</span><span class="sxs-lookup"><span data-stu-id="0a885-169">If user interaction is required (for example, if you are using the Trusted Platform Module (TPM) + PIN or using a password protector), a dialog box appears, and users cannot close it until they provide the required information.</span></span> <span data-ttu-id="0a885-170">Se o protetor for somente TPM, a criptografia começará imediatamente em segundo plano sem a entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="0a885-170">If the protector is TPM only, encryption begins immediately in the background without user input.</span></span></p>
<p><span data-ttu-id="0a885-171">Os usuários não podem solicitar isenções por meio do assistente de criptografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0a885-171">Users cannot request exemptions through the BitLocker encryption wizard.</span></span> <span data-ttu-id="0a885-172">Em vez disso, eles devem entrar em contato com o suporte técnico ou usar qualquer processo que sua organização usa para solicitações de isenção.</span><span class="sxs-lookup"><span data-stu-id="0a885-172">Instead, they must contact their Help Desk or use whatever process their organization uses for exemption requests.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0a885-173">Políticas de configuração do computador &gt; &gt; modelos administrativos &gt; componentes &gt; do Windows MDOP MBAM (gerenciamento de BitLocker) &gt; unidade do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="0a885-173">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; Windows Components &gt; MDOP MBAM (BitLocker Management) &gt; Operating System Drive</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0a885-174">Configurações de imposição de política de criptografia (unidades de dados fixas)</span><span class="sxs-lookup"><span data-stu-id="0a885-174">Encryption Policy Enforcement Settings (Fixed Data Drives)</span></span></p></td>
<td align="left"><p><span data-ttu-id="0a885-175">Para essa configuração, use a opção <strong> Configurar o número de dias do período de cortesia não compatível para unidades fixas </strong> para configurar um período de cortesia.</span><span class="sxs-lookup"><span data-stu-id="0a885-175">For this setting, use the option <strong>Configure the number of noncompliance grace period days for fixed drives</strong> to configure a grace period.</span></span></p>
<p><span data-ttu-id="0a885-176">O período de carência especifica o número de dias pelos quais os usuários finais podem adiar a conformidade com as políticas MBAM para a unidade fixa após a primeira detecção da unidade como não compatível.</span><span class="sxs-lookup"><span data-stu-id="0a885-176">The grace period specifies the number of days that end users can postpone compliance with MBAM policies for their fixed drive after the drive is first detected as noncompliant.</span></span></p>
<p><span data-ttu-id="0a885-177">O período de cortesia começa quando a unidade fixa é determinada como não compatível.</span><span class="sxs-lookup"><span data-stu-id="0a885-177">The grace period begins when the fixed drive is determined to be noncompliant.</span></span> <span data-ttu-id="0a885-178">Se você estiver usando o desbloqueio automático, a política não será imposta até que a unidade do sistema operacional seja compatível.</span><span class="sxs-lookup"><span data-stu-id="0a885-178">If you are using auto-unlock, the policy will not be enforced until the operating system drive is compliant.</span></span> <span data-ttu-id="0a885-179">No entanto, se você não estiver usando o desbloqueio automático, a criptografia da unidade de dados fixa pode começar antes que a unidade do sistema operacional seja totalmente criptografada.</span><span class="sxs-lookup"><span data-stu-id="0a885-179">However, if you are not using auto-unlock, encryption of the fixed data drive can begin before the operating system drive is fully encrypted.</span></span></p>
<p><span data-ttu-id="0a885-180">Depois que o período de cortesia configurado expirar, os usuários não poderão adiar a ação necessária ou solicitar uma isenção a ele.</span><span class="sxs-lookup"><span data-stu-id="0a885-180">After the configured grace period expires, users cannot postpone the required action or request an exemption from it.</span></span> <span data-ttu-id="0a885-181">Se a interação do usuário for necessária, uma caixa de diálogo será exibida e os usuários não poderão fechá-la até fornecer as informações necessárias.</span><span class="sxs-lookup"><span data-stu-id="0a885-181">If user interaction is required, a dialog box appears and users cannot close it until they provide the required information.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0a885-182">Políticas de configuração do computador &gt; &gt; modelos administrativos &gt; componentes &gt; do Windows MDOP MBAM (gerenciamento de BitLocker) &gt; unidade fixa</span><span class="sxs-lookup"><span data-stu-id="0a885-182">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; Windows Components &gt; MDOP MBAM (BitLocker Management) &gt; Fixed Drive</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="0a885-183">Capacidade de fornecer uma URL no assistente de criptografia de unidade BitLocker para apontar para sua política de segurança</span><span class="sxs-lookup"><span data-stu-id="0a885-183">Ability to provide a URL in the BitLocker Drive Encryption wizard to point to your security policy</span></span>

<span data-ttu-id="0a885-184">Uma nova configuração de política de grupo, **forneça a URL para o link de política de segurança**, permite que você configure uma URL que será apresentada aos usuários finais como um link chamado **política de segurança da empresa**.</span><span class="sxs-lookup"><span data-stu-id="0a885-184">A new Group Policy setting, **Provide the URL for the Security Policy link**, enables you to configure a URL that will be presented to end users as a link called **Company Security Policy**.</span></span> <span data-ttu-id="0a885-185">Esse link será exibido quando o MBAM solicitar que os usuários criptografem um volume.</span><span class="sxs-lookup"><span data-stu-id="0a885-185">This link will appear when MBAM prompts users to encrypt a volume.</span></span>

<span data-ttu-id="0a885-186">Se você habilitar essa configuração de política, poderá configurar a URL para o link de **política de segurança da empresa** .</span><span class="sxs-lookup"><span data-stu-id="0a885-186">If you enable this policy setting, you can configure the URL for the **Company Security Policy** link.</span></span> <span data-ttu-id="0a885-187">Se você desabilitar ou não definir essa configuração de política, o link **política de segurança da empresa** não será exibido para os usuários.</span><span class="sxs-lookup"><span data-stu-id="0a885-187">If you disable or do not configure this policy setting, the **Company Security Policy** link is not displayed to users.</span></span>

<span data-ttu-id="0a885-188">A nova configuração de política de grupo está localizada no seguinte nó de GPO: modelos administrativos de políticas de **configuração de computador** &gt; **Policies** &gt; **Administrative Templates** &gt; **componentes do Windows** &gt; **MDOP MBAM (gerenciamento de BitLocker) &gt; Gerenciamento de cliente**.</span><span class="sxs-lookup"><span data-stu-id="0a885-188">The new Group Policy setting is located in the following GPO node: **Computer Configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management) &gt; Client Management**.</span></span>

### <span data-ttu-id="0a885-189">Suporte para chaves de recuperação compatíveis com FIPS</span><span class="sxs-lookup"><span data-stu-id="0a885-189">Support for FIPS-compliant recovery keys</span></span>

<span data-ttu-id="0a885-190">O MBAM 2.5 é compatível com as chaves de recuperação do BitLocker compatíveis com o padrão FIPS (Federal Information Processing Standard) em dispositivos que executam o sistema operacional Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="0a885-190">MBAM2.5 supports Federal Information Processing Standard (FIPS)-compliant BitLocker recovery keys on devices that are running the Windows8.1 operating system.</span></span> <span data-ttu-id="0a885-191">A chave de recuperação não é compatível com FIPS nas versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="0a885-191">The recovery key was not FIPS compliant in earlier versions of Windows.</span></span> <span data-ttu-id="0a885-192">Esse aperfeiçoamento aprimora o processo de recuperação de unidade em organizações que exigem conformidade com FIPS porque permite que os usuários finais usem o portal de autoatendimento ou o site de administração e monitoramento (Help Desk) para recuperar suas unidades se eles esquecerem do PIN ou da senha ou ficarão bloqueados em seus computadores.</span><span class="sxs-lookup"><span data-stu-id="0a885-192">This enhancement improves the drive recovery process in organizations that require FIPS compliance because it enables end users to use the Self-Service Portal or Administration and Monitoring Website (Help Desk) to recover their drives if they forget their PIN or password or get locked out of their computers.</span></span> <span data-ttu-id="0a885-193">O novo recurso de conformidade com FIPS não se estende a protetores de senha.</span><span class="sxs-lookup"><span data-stu-id="0a885-193">The new FIPS compliance feature does not extend to password protectors.</span></span>

<span data-ttu-id="0a885-194">Para habilitar a conformidade com FIPS em sua organização, você deve configurar as configurações de política de grupo do padrão FIPS (padrão de processamento de informações federais).</span><span class="sxs-lookup"><span data-stu-id="0a885-194">To enable FIPS compliance in your organization, you must configure the Federal Information Processing Standard (FIPS) Group Policy settings.</span></span> <span data-ttu-id="0a885-195">Para obter instruções de configuração, consulte [configurações de política de grupo BitLocker](https://go.microsoft.com/fwlink/?LinkId=393560).</span><span class="sxs-lookup"><span data-stu-id="0a885-195">For configuration instructions, see [BitLocker Group Policy Settings](https://go.microsoft.com/fwlink/?LinkId=393560).</span></span>

<span data-ttu-id="0a885-196">Para computadores cliente que executam os sistemas operacionais Windows8 ou Windows7 sem o [hotfix do BitLocker instalado](https://support.microsoft.com/kb/3015477), os administradores de ti continuarão usando o protetor de Data Recovery Agents (Dra) em ambientes compatíveis com FIPS.</span><span class="sxs-lookup"><span data-stu-id="0a885-196">For client computers that are running the Windows8 or Windows7 operating systems without the [installed BitLocker hotfix](https://support.microsoft.com/kb/3015477), IT administrators will continue to use the Data Recovery Agents (DRA) protector in FIPS-compliant environments.</span></span> <span data-ttu-id="0a885-197">Para obter informações sobre DRA, consulte [usando agentes de recuperação de dados com o BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).</span><span class="sxs-lookup"><span data-stu-id="0a885-197">For information about DRA, see [Using Data Recovery Agents with BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).</span></span>

<span data-ttu-id="0a885-198">Consulte [pacote de hotfix 2 para administração e monitoramento do bitlocker 2,5](https://support.microsoft.com/kb/3015477) para baixar e instalar o hotfix do BitLocker para computadores com o Windows 7 e o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0a885-198">See [Hotfix Package 2 for BitLocker Administration and Monitoring 2.5](https://support.microsoft.com/kb/3015477) to download and install the BitLocker hotfix for Windows 7 and Windows 8 computers.</span></span>

### <span data-ttu-id="0a885-199">Suporte para implantações de alta disponibilidade</span><span class="sxs-lookup"><span data-stu-id="0a885-199">Support for high availability deployments</span></span>

<span data-ttu-id="0a885-200">O MBAM é compatível com os seguintes cenários de alta disponibilidade, além das topologias padrão de integração de dois servidores e do Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="0a885-200">MBAM supports the following high-availability scenarios in addition to the standard two-server and Configuration Manager Integration topologies:</span></span>

-   <span data-ttu-id="0a885-201">Grupos de disponibilidade do SQL Server AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="0a885-201">SQL Server AlwaysOn availability groups</span></span>

-   <span data-ttu-id="0a885-202">Clustering do SQL Server</span><span class="sxs-lookup"><span data-stu-id="0a885-202">SQL Server clustering</span></span>

-   <span data-ttu-id="0a885-203">Balanceamento de carga de rede (NLB)</span><span class="sxs-lookup"><span data-stu-id="0a885-203">Network load balancing (NLB)</span></span>

-   <span data-ttu-id="0a885-204">Espelhamento do SQL Server</span><span class="sxs-lookup"><span data-stu-id="0a885-204">SQL Server mirroring</span></span>

-   <span data-ttu-id="0a885-205">Backup do Volume Shadow Copy Service (VSS)</span><span class="sxs-lookup"><span data-stu-id="0a885-205">Volume Shadow Copy Service (VSS) Backup</span></span>

<span data-ttu-id="0a885-206">Para obter mais informações sobre esses recursos, confira [planejando a alta disponibilidade do MBAM 2,5](planning-for-mbam-25-high-availability.md).</span><span class="sxs-lookup"><span data-stu-id="0a885-206">For more information about these features, see [Planning for MBAM 2.5 High Availability](planning-for-mbam-25-high-availability.md).</span></span>

### <a href="" id="management-of-roles-for-administration-and-monitoring-website-changed-"></a><span data-ttu-id="0a885-207">Gerenciamento de funções para administração e monitoramento do site alterado</span><span class="sxs-lookup"><span data-stu-id="0a885-207">Management of roles for Administration and Monitoring Website changed</span></span>

<span data-ttu-id="0a885-208">No MBAM 2.5, você deve criar grupos de segurança nos serviços de domínio Active Directory (ADDS) para gerenciar as funções que fornecem direitos de acesso ao site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="0a885-208">In MBAM2.5, you must create security groups in Active Directory Domain Services (ADDS) to manage the roles that provide access rights to the Administration and Monitoring Website.</span></span> <span data-ttu-id="0a885-209">As funções permitem que os usuários de grupos de segurança específicos realizem tarefas diferentes no site, como a exibição de relatórios ou a ajuda de usuários finais a recuperarem unidades criptografadas.</span><span class="sxs-lookup"><span data-stu-id="0a885-209">Roles enable users who are in specific security groups to perform different tasks in the website such as viewing reports or helping end users recover encrypted drives.</span></span> <span data-ttu-id="0a885-210">Em versões anteriores do MBAM, as funções eram gerenciadas por meio de grupos locais.</span><span class="sxs-lookup"><span data-stu-id="0a885-210">In previous versions of MBAM, roles were managed by using local groups.</span></span>

<span data-ttu-id="0a885-211">No MBAM 2.5, o termo "funções" substitui o termo "funções de administrador", que foi usado em versões anteriores do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0a885-211">In MBAM2.5, the term “roles” replaces the term “administrator roles,” which was used in earlier versions of MBAM.</span></span> <span data-ttu-id="0a885-212">Além disso, no MBAM 2.5, a função "administradores de sistema do MBAM" foi removida.</span><span class="sxs-lookup"><span data-stu-id="0a885-212">In addition, in MBAM2.5 the “MBAM System Administrators” role has been removed.</span></span>

<span data-ttu-id="0a885-213">A tabela a seguir lista os grupos de segurança que você deve criar no AD DS.</span><span class="sxs-lookup"><span data-stu-id="0a885-213">The following table lists the security groups that you must create in AD DS.</span></span> <span data-ttu-id="0a885-214">Você pode usar qualquer nome para os grupos de segurança.</span><span class="sxs-lookup"><span data-stu-id="0a885-214">You can use any name for the security groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0a885-215">Função</span><span class="sxs-lookup"><span data-stu-id="0a885-215">Role</span></span></th>
<th align="left"><span data-ttu-id="0a885-216">Direitos de acesso para esta função no site de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="0a885-216">Access rights for this role on the Administration and Monitoring Website</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0a885-217">Usuários da assistência técnica MBAM</span><span class="sxs-lookup"><span data-stu-id="0a885-217">MBAM Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0a885-218">Fornece acesso às áreas gerenciar TPM e recuperação de unidade do site de administração e monitoramento do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0a885-218">Provides access to the Manage TPM and Drive Recovery areas of the MBAM Administration and Monitoring Website.</span></span> <span data-ttu-id="0a885-219">Os usuários que têm acesso a essas áreas devem preencher todos os campos quando usarem qualquer uma das áreas.</span><span class="sxs-lookup"><span data-stu-id="0a885-219">Users who have access to these areas must fill in all fields when they use either area.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0a885-220">Usuários do relatório MBAM</span><span class="sxs-lookup"><span data-stu-id="0a885-220">MBAM Report Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0a885-221">Fornece acesso aos relatórios no site Administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="0a885-221">Provides access to the Reports in the Administration and Monitoring Website.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0a885-222">Usuários avançados da assistência técnica MBAM</span><span class="sxs-lookup"><span data-stu-id="0a885-222">MBAM Advanced Helpdesk Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0a885-223">Fornece acesso a todas as áreas no site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="0a885-223">Provides access to all areas in the Administration and Monitoring Website.</span></span> <span data-ttu-id="0a885-224">Os usuários neste grupo precisam inserir apenas a chave de recuperação, e não o domínio do usuário final e o nome de usuário, ao ajudar os usuários finais a recuperarem suas unidades.</span><span class="sxs-lookup"><span data-stu-id="0a885-224">Users in this group have to enter only the recovery key, not the end user’s domain and user name, when helping end users recover their drives.</span></span> <span data-ttu-id="0a885-225">Se um usuário for membro do grupo usuários da assistência técnica do MBAM e do grupo usuários avançados da assistência técnica do MBAM, o MBAM permissões do grupo usuários da assistência avançada do MBAM substituirá as permissões do grupo usuários da assistência técnica do.</span><span class="sxs-lookup"><span data-stu-id="0a885-225">If a user is a member of the MBAM Helpdesk Users group and the MBAM Advanced Helpdesk Users group, the MBAM Advanced Helpdesk Users group permissions override the MBAM Helpdesk Users group permissions.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="0a885-226">Depois de criar os grupos de segurança em Adicionar, atribua usuários e/ou grupos ao grupo de segurança apropriado para habilitar o nível de acesso correspondente ao site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="0a885-226">After you create the security groups in ADDS, assign users and/or groups to the appropriate security group to enable the corresponding level of access to the Administration and Monitoring Website.</span></span> <span data-ttu-id="0a885-227">Para habilitar as pessoas com cada função para acessar o site de administração e monitoramento, você também deve especificar cada grupo de segurança quando estiver configurando o site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="0a885-227">To enable individuals with each role to access the Administration and Monitoring Website, you must also specify each security group when you are configuring the Administration and Monitoring Website.</span></span>

### <span data-ttu-id="0a885-228">Cmdlets do Windows PowerShell para configurar os recursos do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="0a885-228">Windows PowerShell cmdlets for configuring MBAM Server features</span></span>

<span data-ttu-id="0a885-229">Os cmdlets do Windows PowerShell para MBAM 2.5 permitem que você configure e gerencie os recursos do servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="0a885-229">Windows PowerShell cmdlets for MBAM2.5 enable you to configure and manage the MBAM Server features.</span></span> <span data-ttu-id="0a885-230">Cada recurso tem um cmdlet do Windows PowerShell correspondente que você pode usar para habilitar ou desabilitar recursos ou para obter informações sobre o recurso.</span><span class="sxs-lookup"><span data-stu-id="0a885-230">Each feature has a corresponding Windows PowerShell cmdlet that you can use to enable or disable features, or to get information about the feature.</span></span>

<span data-ttu-id="0a885-231">Para pré-requisitos e pré-requisitos para usar o Windows PowerShell, consulte [configurando recursos do MBAM 2,5 Server usando o Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="0a885-231">For prerequisites and prerequisites for using Windows PowerShell, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span></span>

**<span data-ttu-id="0a885-232">Para carregar a ajuda do MBAM 2,5 para cmdlets do Windows PowerShell após instalar o software do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="0a885-232">To load the MBAM 2.5 Help for Windows PowerShell cmdlets after installing the MBAM Server software</span></span>**

1.  <span data-ttu-id="0a885-233">Abra o Windows PowerShell ou o ambiente de script integrado do Windows PowerShell (ISE).</span><span class="sxs-lookup"><span data-stu-id="0a885-233">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="0a885-234">Digite **Update-Help – módulo Microsoft. MBAM**.</span><span class="sxs-lookup"><span data-stu-id="0a885-234">Type **Update-Help –Module Microsoft.MBAM**.</span></span>

<span data-ttu-id="0a885-235">A ajuda do Windows PowerShell para MBAM está disponível nos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="0a885-235">Windows PowerShell Help for MBAM is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0a885-236">Formato de ajuda do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0a885-236">Windows PowerShell Help format</span></span></th>
<th align="left"><span data-ttu-id="0a885-237">Mais informações</span><span class="sxs-lookup"><span data-stu-id="0a885-237">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0a885-238">Em um prompt de comando do Windows PowerShell, digite <strong> </strong> &lt; <em> cmdlet Get-Help</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="0a885-238">At a Windows PowerShell command prompt, type <strong>Get-Help</strong> &lt;<em>cmdlet</em>&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="0a885-239">Para carregar os cmdlets do Windows PowerShell mais recentes, siga as instruções na seção anterior sobre como carregar a ajuda do Windows PowerShell para MBAM.</span><span class="sxs-lookup"><span data-stu-id="0a885-239">To upload the latest Windows PowerShell cmdlets, follow the instructions in the previous section on how to load Windows PowerShell Help for MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0a885-240">No TechNet como páginas da Web</span><span class="sxs-lookup"><span data-stu-id="0a885-240">On TechNet as webpages</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0a885-241">No centro de download como um arquivo. docx do Word</span><span class="sxs-lookup"><span data-stu-id="0a885-241">On the Download Center as a Word .docx file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0a885-242">No centro de download como um arquivo. pdf</span><span class="sxs-lookup"><span data-stu-id="0a885-242">On the Download Center as a .pdf file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="0a885-243">Suporte para PINs de somente ASCII e aprimorados e capacidade para evitar caracteres sequenciais e de repetição</span><span class="sxs-lookup"><span data-stu-id="0a885-243">Support for ASCII-only and enhanced PINs and ability to prevent sequential and repeating characters</span></span>

**<span data-ttu-id="0a885-244">Permitir PINs avançados para a configuração da política de grupo de inicialização</span><span class="sxs-lookup"><span data-stu-id="0a885-244">Allow enhanced PINs for startup Group Policy setting</span></span>**

<span data-ttu-id="0a885-245">A configuração de política de grupo, **permitir pinos aprimorados para inicialização**, permite que você configure se os Pins de inicialização avançados serão usados com o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0a885-245">The Group Policy setting, **Allow enhanced PINs for startup**, enables you to configure whether enhanced startup PINs are used with BitLocker.</span></span> <span data-ttu-id="0a885-246">PINs de inicialização avançados permitem que os usuários insiram teclas em um teclado completo, incluindo letras maiúsculas e minúsculas, símbolos, números e espaços.</span><span class="sxs-lookup"><span data-stu-id="0a885-246">Enhanced startup PINs permit users to enter any keys on a full keyboard, including uppercase and lowercase letters, symbols, numbers, and spaces.</span></span> <span data-ttu-id="0a885-247">Se você habilitar essa configuração de política, todos os novos PINs de inicialização do BitLocker definidos serão PINs aprimorados.</span><span class="sxs-lookup"><span data-stu-id="0a885-247">If you enable this policy setting, all new BitLocker startup PINs that are set will be enhanced PINs.</span></span> <span data-ttu-id="0a885-248">Se você desabilitar ou não definir essa configuração de política, PINs avançados não poderão ser usados.</span><span class="sxs-lookup"><span data-stu-id="0a885-248">If you disable or do not configure this policy setting, enhanced PINs cannot be used.</span></span>

<span data-ttu-id="0a885-249">Nem todos os computadores dão suporte à entrada de pinos aprimorados no ambiente de execução antes da inicialização (PXE).</span><span class="sxs-lookup"><span data-stu-id="0a885-249">Not all computers support the entry of enhanced PINs in the Pre-Boot Execution Environment (PXE).</span></span> <span data-ttu-id="0a885-250">Antes de habilitar essa configuração de política de grupo para sua organização, execute uma verificação do sistema durante o processo de configuração do BitLocker para garantir que o BIOS do computador seja compatível com o uso do teclado completo no PXE.</span><span class="sxs-lookup"><span data-stu-id="0a885-250">Before you enable this Group Policy setting for your organization, run a system check during the BitLocker setup process to ensure that the computer’s BIOS supports the use of the full keyboard in PXE.</span></span> <span data-ttu-id="0a885-251">Para obter mais informações, consulte [planejando os requisitos da política de grupo do MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0a885-251">For more information, see [Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md).</span></span>

**<span data-ttu-id="0a885-252">Caixa de seleção exigir pinos somente ASCII</span><span class="sxs-lookup"><span data-stu-id="0a885-252">Require ASCII-only PINs check box</span></span>**

<span data-ttu-id="0a885-253">A configuração **permitir pinos aprimorados para a política de grupo de inicialização** também contém a caixa de seleção **exigir Pins somente ASCII** .</span><span class="sxs-lookup"><span data-stu-id="0a885-253">The **Allow enhanced PINs for startup** Group Policy setting also contains a **Require ASCII-only PINs** check box.</span></span> <span data-ttu-id="0a885-254">Se os computadores de sua organização não tiverem suporte para o uso do teclado completo em PXE, você poderá habilitar a caixa de seleção **permitir pinos aprimorados para** a configuração de política de grupo e, em seguida, marcar a caixa de seleção **exigir Pins somente ASCII** para exigir que os Pins aprimorados usem apenas caracteres ASCII imprimíveis.</span><span class="sxs-lookup"><span data-stu-id="0a885-254">If the computers in your organization do not support the use of the full keyboard in PXE, you can enable the **Allow enhanced PINs for startup** Group Policy setting, and then select the **Require ASCII-only PINs** check box to require that enhanced PINs use only printable ASCII characters.</span></span>

**<span data-ttu-id="0a885-255">Uso imposto de caracteres não sequenciais e não repetitivos</span><span class="sxs-lookup"><span data-stu-id="0a885-255">Enforced use of nonsequential and nonrepeating characters</span></span>**

<span data-ttu-id="0a885-256">O MBAM 2.5 impede que os usuários finais criem PINs que consistem em números de repetição (como 1111) ou números sequenciais (como o 1234).</span><span class="sxs-lookup"><span data-stu-id="0a885-256">MBAM2.5 prevents end users from creating PINs that consist of repeating numbers (such as 1111) or sequential numbers (such as 1234).</span></span> <span data-ttu-id="0a885-257">Se os usuários finais tentarem inserir uma senha que contenha três ou mais números de repetição ou sequencial, o assistente de criptografia de unidade de disco BitLocker exibirá uma mensagem de erro e impedirá que os usuários insiram um PIN com os caracteres proibidos.</span><span class="sxs-lookup"><span data-stu-id="0a885-257">If end users try to enter a password that contains three or more repeating or sequential numbers, the Bitlocker Drive Encryption wizard displays an error message and prevents users from entering a PIN with the prohibited characters.</span></span>

### <span data-ttu-id="0a885-258">Adição de certificado DRA ao relatório de conformidade do computador BitLocker</span><span class="sxs-lookup"><span data-stu-id="0a885-258">Addition of DRA Certificate to BitLocker Computer Compliance report</span></span>

<span data-ttu-id="0a885-259">Um novo tipo de protetor, o certificado de agente de recuperação de dados (DRA), foi adicionado ao relatório de conformidade do computador BitLocker no Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0a885-259">A new protector type, the Data Recovery Agent (DRA) Certificate, has been added to the BitLocker Computer Compliance Report in Configuration Manager.</span></span> <span data-ttu-id="0a885-260">Esse tipo de protetor aplica-se às unidades do sistema operacional, e ele aparece na seção **volume (s) do computador** na coluna **tipos de protetor** .</span><span class="sxs-lookup"><span data-stu-id="0a885-260">This protector type applies to operating system drives, and it appears in the **Computer Volume(s)** section in the **Protector Types** column.</span></span>

### <span data-ttu-id="0a885-261">Suporte para implantações de suporte de várias florestas</span><span class="sxs-lookup"><span data-stu-id="0a885-261">Support for multi-forest support deployments</span></span>

<span data-ttu-id="0a885-262">O MBAM 2,5 oferece suporte aos seguintes tipos de implantação de várias florestas:</span><span class="sxs-lookup"><span data-stu-id="0a885-262">MBAM 2.5 supports the following types of multi-forest deployments:</span></span>

-   <span data-ttu-id="0a885-263">Floresta única com um único domínio</span><span class="sxs-lookup"><span data-stu-id="0a885-263">Single forest with single domain</span></span>

-   <span data-ttu-id="0a885-264">Floresta única com uma única árvore e vários domínios</span><span class="sxs-lookup"><span data-stu-id="0a885-264">Single forest with a single tree and multiple domains</span></span>

-   <span data-ttu-id="0a885-265">Floresta única com vários namespaces de árvores e disjunção</span><span class="sxs-lookup"><span data-stu-id="0a885-265">Single forest with multiple trees and disjoint namespaces</span></span>

-   <span data-ttu-id="0a885-266">Várias florestas em uma topologia de floresta central</span><span class="sxs-lookup"><span data-stu-id="0a885-266">Multiple forests in a central forest topology</span></span>

-   <span data-ttu-id="0a885-267">Várias florestas em uma topologia de floresta de recursos</span><span class="sxs-lookup"><span data-stu-id="0a885-267">Multiple forests in a resource forest topology</span></span>

<span data-ttu-id="0a885-268">Não há suporte para migração de floresta (indo de simples para vários, múltiplo para único, recurso para toda a floresta etc.) ou atualização ou downgrade.</span><span class="sxs-lookup"><span data-stu-id="0a885-268">There is no support for forest migration (going from single to multiple, multiple to single, resource to across the forest, etc.), or upgrade or downgrade.</span></span>

<span data-ttu-id="0a885-269">Os pré-requisitos para a implantação do MBAM em implantações de várias florestas são:</span><span class="sxs-lookup"><span data-stu-id="0a885-269">The prerequisites for deploying MBAM in multi-forest deployments are:</span></span>

-   <span data-ttu-id="0a885-270">A floresta deve estar em execução em versões compatíveis do Windows Server.</span><span class="sxs-lookup"><span data-stu-id="0a885-270">Forest must be running on supported versions of Windows Server.</span></span>

-   <span data-ttu-id="0a885-271">Uma relação de confiança bidirecional ou unidirecional é necessária.</span><span class="sxs-lookup"><span data-stu-id="0a885-271">A two-way or one-way trust is required.</span></span> <span data-ttu-id="0a885-272">As relações de confiança unidirecionais exigem que o domínio do servidor confie no domínio do cliente.</span><span class="sxs-lookup"><span data-stu-id="0a885-272">One-way trusts require that the server’s domain trusts the client’s domain.</span></span> <span data-ttu-id="0a885-273">Em outras palavras, o domínio do servidor é apontado no domínio do cliente.</span><span class="sxs-lookup"><span data-stu-id="0a885-273">In other words, the server’s domain is pointed at the client’s domain.</span></span>

### <span data-ttu-id="0a885-274">Suporte do cliente MBAM para discos rígidos criptografados</span><span class="sxs-lookup"><span data-stu-id="0a885-274">MBAM Client support for Encrypted Hard Drives</span></span>

<span data-ttu-id="0a885-275">O MBAM dá suporte ao BitLocker em discos rígidos criptografados que atendem aos requisitos de especificação do TCG para o Opal e com os padrões IEEE 1667.</span><span class="sxs-lookup"><span data-stu-id="0a885-275">MBAM supports BitLocker on Encrypted Hard Drives that meet TCG specification requirements for Opal as well as IEEE 1667 standards.</span></span> <span data-ttu-id="0a885-276">Quando o BitLocker estiver habilitado nesses dispositivos, ele irá gerar chaves e executar funções de gerenciamento na unidade criptografada.</span><span class="sxs-lookup"><span data-stu-id="0a885-276">When BitLocker is enabled on these devices, it will generate keys and perform management functions on the encrypted drive.</span></span> <span data-ttu-id="0a885-277">Para obter mais informações, consulte [unidade de disco rígido criptografado](https://technet.microsoft.com/library/hh831627.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0a885-277">See [Encrypted Hard Drive](https://technet.microsoft.com/library/hh831627.aspx) for more information.</span></span>

## <span data-ttu-id="0a885-278">Como obter tecnologias do MDOP</span><span class="sxs-lookup"><span data-stu-id="0a885-278">How to Get MDOP Technologies</span></span>


<span data-ttu-id="0a885-279">O MBAM é parte do Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="0a885-279">MBAM is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="0a885-280">O MDOP faz parte do programa Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="0a885-280">MDOP is part of the Microsoft Software Assurance program.</span></span> <span data-ttu-id="0a885-281">Para obter mais informações sobre o programa Microsoft Software Assurance e como adquirir o MDOP, consulte [como faço para obter o MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="0a885-281">For more information about the Microsoft Software Assurance program and how to acquire the MDOP, see [How Do I Get MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <a href="" id="---------mbam-2-5-release-notes"></a> <span data-ttu-id="0a885-282">Notas de versão do MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="0a885-282">MBAM 2.5 Release Notes</span></span>


<span data-ttu-id="0a885-283">Para obter mais informações e últimas notícias que não estão incluídas nesta documentação, confira [notas de versão do MBAM 2,5](release-notes-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="0a885-283">For more information and late-breaking news that is not included in this documentation, see [Release Notes for MBAM 2.5](release-notes-for-mbam-25.md).</span></span>

## <span data-ttu-id="0a885-284">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="0a885-284">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="0a885-285">Envie seus comentários [aqui](https://support.microsoft.com/help/4021566/windows-10-send-feedback-to-microsoft-with-feedback-hub).</span><span class="sxs-lookup"><span data-stu-id="0a885-285">Send your feedback [here](https://support.microsoft.com/help/4021566/windows-10-send-feedback-to-microsoft-with-feedback-hub).</span></span> 
- <span data-ttu-id="0a885-286">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="0a885-286">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

## <span data-ttu-id="0a885-287">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0a885-287">Related topics</span></span>


[<span data-ttu-id="0a885-288">Microsoft BitLocker Administration and Monitoring 2.5</span><span class="sxs-lookup"><span data-stu-id="0a885-288">Microsoft BitLocker Administration and Monitoring 2.5</span></span>](index.md)

[<span data-ttu-id="0a885-289">Introdução ao MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="0a885-289">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

 

 





