---
title: Planejar Requisitos de Política de Grupo do MBAM 1.0
description: Planejar Requisitos de Política de Grupo do MBAM 1.0
author: dansimp
ms.assetid: 0fc9c509-7850-4a8e-bb82-b949025bcb02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5061748107dc1d00baa41188b8cf240ec187317
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795999"
---
# <span data-ttu-id="3bdb0-103">Planejar Requisitos de Política de Grupo do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="3bdb0-103">Planning for MBAM 1.0 Group Policy Requirements</span></span>


<span data-ttu-id="3bdb0-104">O gerenciamento de clientes de administração e monitoramento do Microsoft BitLocker (MBAM) exige a aplicação de configurações personalizadas de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-104">Microsoft BitLocker Administration and Monitoring (MBAM) Client management requires custom Group Policy settings to be applied.</span></span> <span data-ttu-id="3bdb0-105">Este tópico descreve as opções de política disponíveis para objeto de política de grupo (GPO) quando você usa o MBAM para gerenciar a criptografia de unidade de disco BitLocker na empresa.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-105">This topic describes the available policy options for Group Policy Object (GPO) when you use MBAM to manage BitLocker Drive Encryption in the enterprise.</span></span>

**<span data-ttu-id="3bdb0-106">Importante</span><span class="sxs-lookup"><span data-stu-id="3bdb0-106">Important</span></span>**  
<span data-ttu-id="3bdb0-107">O MBAM não usa as configurações padrão de GPO para criptografia de unidade de disco BitLocker do Windows.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-107">MBAM does not use the default GPO settings for Windows BitLocker drive encryption.</span></span> <span data-ttu-id="3bdb0-108">Se as configurações padrão estiverem habilitadas, elas poderão causar um comportamento conflitante.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-108">If the default settings are enabled, they can cause conflicting behavior.</span></span> <span data-ttu-id="3bdb0-109">Para permitir que o MBAM gerencie o BitLocker, você deve definir as configurações de política de GPO após a instalação do modelo de política de grupo do MBAM.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-109">To enable MBAM to manage BitLocker, you must define the GPO policy settings after you install the MBAM Group Policy Template.</span></span>



<span data-ttu-id="3bdb0-110">Depois de instalar o modelo de política de grupo do MBAM, você pode exibir e modificar as configurações de política de GPO de MBAM personalizadas disponíveis para permitir que o MBAM gerencie a criptografia do BitLocker corporativo.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-110">After you install the MBAM Group Policy template, you can view and modify the available custom MBAM GPO policy settings that enable MBAM to manage the enterprise BitLocker encryption.</span></span> <span data-ttu-id="3bdb0-111">O modelo de política de grupo MBAM deve ser instalado em um computador que seja capaz de executar o console de gerenciamento de política de grupo (GPMC) ou a tecnologia avançada do MDOP do gerenciamento de política de grupo (AGPM).</span><span class="sxs-lookup"><span data-stu-id="3bdb0-111">The MBAM Group Policy template must be installed on a computer that is capable of running the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) MDOP technology.</span></span> <span data-ttu-id="3bdb0-112">Em seguida, para editar o GPO aplicável, abra o GPMC ou o AGPM e navegue até o nó do GPO a seguir: modelos administrativos de **configuração de computador** \\ **Administrative Templates** \\ **componentes** \\ **do Windows MDOP MBAM (gerenciamento de BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-112">Next, to edit the applicable GPO, open the GPMC or AGPM, and then navigate to the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)**.</span></span>

<span data-ttu-id="3bdb0-113">O nó do GPO MBAM (gerenciamento do BitLocker) do MDOP contém quatro configurações de política global e quatro nós de configuração de GPO filho, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-113">The MDOP MBAM (BitLocker Management) GPO node contains four global policy settings and four child GPO setting nodes, respectively.</span></span> <span data-ttu-id="3bdb0-114">As quatro configurações de política global de GPO são: gerenciamento de cliente, unidade fixa, unidade do sistema operacional e unidade removível.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-114">The four GPO global policy settings are: Client Management, Fixed Drive, Operating System Drive, and Removable Drive.</span></span> <span data-ttu-id="3bdb0-115">As seções a seguir fornecem definições de política e configurações de política sugeridas para ajudá-lo a planejar os requisitos de configuração de política de GPO MBAM.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-115">The following sections provide policy definitions and suggested policy settings to help you plan for the MBAM GPO policy setting requirements.</span></span>

**<span data-ttu-id="3bdb0-116">Observação</span><span class="sxs-lookup"><span data-stu-id="3bdb0-116">Note</span></span>**  
<span data-ttu-id="3bdb0-117">Para obter mais informações sobre como definir as configurações mínimas de GPO sugeridas para permitir que o MBAM gerencie a criptografia do BitLocker, consulte [como editar configurações de GPO MBAM 1,0](how-to-edit-mbam-10-gpo-settings.md).</span><span class="sxs-lookup"><span data-stu-id="3bdb0-117">For more information about configuring the minimum suggested GPO settings to enable MBAM to manage BitLocker encryption, see [How to Edit MBAM 1.0 GPO Settings](how-to-edit-mbam-10-gpo-settings.md).</span></span>



## <span data-ttu-id="3bdb0-118">Definições de política global</span><span class="sxs-lookup"><span data-stu-id="3bdb0-118">Global policy definitions</span></span>


<span data-ttu-id="3bdb0-119">Esta seção descreve as definições de política global do MBAM, que podem ser encontradas no nó GPO a seguir: modelos administrativos de **configuração de computador** \\ **Administrative Templates** \\ **componentes** \\ **do Windows MDOP MBAM (gerenciamento de BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-119">This section describes the MBAM Global policy definitions, which can be found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3bdb0-120">Nome da política</span><span class="sxs-lookup"><span data-stu-id="3bdb0-120">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="3bdb0-121">Visão geral e configuração de política sugerida</span><span class="sxs-lookup"><span data-stu-id="3bdb0-121">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bdb0-122">Escolher método de criptografia de unidade e nível de codificação</span><span class="sxs-lookup"><span data-stu-id="3bdb0-122">Choose drive encryption method and cipher strength</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bdb0-123">Configuração sugerida: <strong> não configurada</span><span class="sxs-lookup"><span data-stu-id="3bdb0-123">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="3bdb0-124">Configure essa política para usar um método de criptografia específico e um nível de codificação.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-124">Configure this policy to use a specific encryption method and cipher strength.</span></span></p>
<p><span data-ttu-id="3bdb0-125">Quando essa política não está configurada, o BitLocker usa o método de criptografia padrão do AES 128-bit com difusor ou o método de criptografia especificado pelo script de instalação.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-125">When this policy is not configured, BitLocker uses the default encryption method of AES 128-bit with Diffuser or the encryption method specified by the setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bdb0-126">Impedir substituição de memória na reinicialização</span><span class="sxs-lookup"><span data-stu-id="3bdb0-126">Prevent memory overwrite on restart</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bdb0-127">Configuração sugerida: <strong> não configurada</span><span class="sxs-lookup"><span data-stu-id="3bdb0-127">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="3bdb0-128">Configure essa política para melhorar o desempenho de reinicialização sem substituir os segredos do BitLocker na memória na reinicialização.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-128">Configure this policy to improve restart performance without overwriting BitLocker secrets in memory on restart.</span></span></p>
<p><span data-ttu-id="3bdb0-129">Quando essa política não está configurada, os segredos do BitLocker são removidos da memória quando o computador é reiniciado.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-129">When this policy is not configured, BitLocker secrets are removed from memory when the computer restarts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bdb0-130">Validar regra de uso de certificado de cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="3bdb0-130">Validate smart card certificate usage rule</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bdb0-131">Configuração sugerida: <strong> não configurada</span><span class="sxs-lookup"><span data-stu-id="3bdb0-131">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="3bdb0-132">Configure essa política para usar a proteção do BitLocker baseada em certificados de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-132">Configure this policy to use smartcard certificate-based BitLocker protection.</span></span></p>
<p><span data-ttu-id="3bdb0-133">Quando essa política não está configurada, um identificador de objeto padrão 1.3.6.1.4.1.311.67.1.1 é usado para especificar um certificado.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-133">When this policy is not configured, a default object identifier 1.3.6.1.4.1.311.67.1.1 is used to specify a certificate.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bdb0-134">Fornecer os identificadores exclusivos para a sua organização</span><span class="sxs-lookup"><span data-stu-id="3bdb0-134">Provide the unique identifiers for your organization</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bdb0-135">Configuração sugerida: <strong> não configurada</span><span class="sxs-lookup"><span data-stu-id="3bdb0-135">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="3bdb0-136">Configure essa política para usar um agente de recuperação de dados baseado em certificado ou o leitor BitLocker To Go.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-136">Configure this policy to use a certificate-based data recovery agent or the BitLocker To Go reader.</span></span></p>
<p><span data-ttu-id="3bdb0-137">Quando essa política não está configurada, o <strong> campo de identificação </strong> não é usado.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-137">When this policy is not configured, the <strong>Identification</strong> field is not used.</span></span></p>
<p><span data-ttu-id="3bdb0-138">Se a sua empresa exigir medidas de segurança superiores, talvez você queira configurar <strong> o </strong> campo de identificação para garantir que todos os dispositivos USB tenham esse campo definido e que eles estejam alinhados com essa configuração de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-138">If your company requires higher security measurements, you may want to configure the <strong>Identification</strong> field to make sure that all USB devices have this field set and that they are aligned with this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="3bdb0-139">Definições da política de gerenciamento de cliente</span><span class="sxs-lookup"><span data-stu-id="3bdb0-139">Client Management policy definitions</span></span>


<span data-ttu-id="3bdb0-140">Esta seção descreve as definições da política de gerenciamento de cliente para MBAM, encontradas no nó GPO a seguir: modelos administrativos de **configuração de computador** \\ **Administrative Templates** \\ **componentes do Windows** \\ **MDOP MBAM (gerenciamento de BitLocker)**  \\  **Gerenciamento de cliente**.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-140">This section describes the Client Management policy definitions for MBAM, found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Client Management**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3bdb0-141">Nome da política</span><span class="sxs-lookup"><span data-stu-id="3bdb0-141">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="3bdb0-142">Visão geral e configurações de política sugeridas</span><span class="sxs-lookup"><span data-stu-id="3bdb0-142">Overview and Suggested Policy Settings</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bdb0-143">Configurar os serviços do MBAM</span><span class="sxs-lookup"><span data-stu-id="3bdb0-143">Configure MBAM Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bdb0-144">Configuração sugerida: <strong> habilitada</span><span class="sxs-lookup"><span data-stu-id="3bdb0-144">Suggested Configuration: <strong>Enabled</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="3bdb0-145">MBAM recuperação e ponto de extremidade do serviço de hardware </strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb0-145">MBAM Recovery and Hardware service endpoint</strong>.</span></span> <span data-ttu-id="3bdb0-146">Esta é a primeira configuração de política que você deve configurar para habilitar o gerenciamento de criptografia do BitLocker do cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-146">This is the first policy setting that you must configure to enable the MBAM Client BitLocker encryption management.</span></span> <span data-ttu-id="3bdb0-147">Para essa configuração, insira o local do ponto de extremidade semelhante ao exemplo a seguir: <strong> http:// </strong><em> &lt; MBAM administração e monitoramento nome &gt; </em><strong> do servidor de monitoramento: </strong><em> &lt; porta o serviço Web está associado a &gt; </em><strong> /MBAMRecoveryAndHardwareService/CoreService.svc </strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb0-147">For this setting, enter the endpoint location similar to the following example: <strong>http://</strong><em>&lt;MBAM Administration and Monitoring Server Name&gt;</em><strong>:</strong><em>&lt;port the web service is bound to&gt;</em><strong>/MBAMRecoveryAndHardwareService/CoreService.svc</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="3bdb0-148">Selecione as informações de recuperação do BitLocker a serem armazenadas </strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb0-148">Select BitLocker recovery information to store</strong>.</span></span> <span data-ttu-id="3bdb0-149">Essa configuração de política permite configurar o serviço de recuperação de chave para fazer backup das informações de recuperação do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-149">This policy setting lets you configure the key recovery service to back up the BitLocker recovery information.</span></span> <span data-ttu-id="3bdb0-150">Ele também permite configurar o serviço de relatório de status para coletar relatórios de conformidade e auditoria.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-150">It also lets you configure the status reporting service for collecting compliance and audit reports.</span></span> <span data-ttu-id="3bdb0-151">A política fornece um método administrativo de recuperação de dados criptografados pelo BitLocker para ajudar a evitar a perda de dados devido à falta de informações importantes.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-151">The policy provides an administrative method of recovering data encrypted by BitLocker to help prevent data loss due to the lack of key information.</span></span> <span data-ttu-id="3bdb0-152">O relatório de status e a atividade de recuperação de chave serão enviados automaticamente e silenciosamente para o local do servidor de relatório configurado.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-152">Status report and key recovery activity will automatically and silently be sent to the configured report server location.</span></span></p>
<p><span data-ttu-id="3bdb0-153">Se você não configurar ou se desabilitar essa configuração de política, as informações de recuperação de chave não serão salvas, e o relatório de status e a atividade de recuperação de chave não serão relatados ao servidor.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-153">If you do not configure or if you disable this policy setting, the key recovery information will not be saved, and status report and key recovery activity will not be reported to server.</span></span> <span data-ttu-id="3bdb0-154">Quando essa configuração estiver definida como <strong> senha de recuperação e pacote </strong> de chaves, a senha de recuperação e o pacote de chaves serão automaticamente e, em seguida, o backup será silenciosa para o local do servidor de recuperação de chave configurado.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-154">When this setting is set to <strong>Recovery Password and key package</strong>, the recovery password and key package will be automatically and silently backed up to the configured key recovery server location.</span></span></p></li>
<li><p><strong><span data-ttu-id="3bdb0-155">Digite a frequência de verificação do status do cliente em minutos </strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb0-155">Enter the client checking status frequency in minutes</strong>.</span></span> <span data-ttu-id="3bdb0-156">Essa configuração de política gerencia com que frequência o cliente verifica as políticas de proteção BitLocker e o status no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-156">This policy setting manages how frequently the client checks the BitLocker protection policies and the status on the client computer.</span></span> <span data-ttu-id="3bdb0-157">Essa política também gerencia com que frequência o status de conformidade do cliente é salvo no servidor.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-157">This policy also manages how frequently the client compliance status is saved to the server.</span></span> <span data-ttu-id="3bdb0-158">O cliente verifica as políticas de proteção BitLocker e o status no computador cliente e também faz backup da chave de recuperação do cliente na frequência configurada.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-158">The client checks the BitLocker protection policies and status on the client computer, and it also backs up the client recovery key at the configured frequency.</span></span></p>
<p><span data-ttu-id="3bdb0-159">Defina essa frequência com base na necessidade estabelecida pela sua empresa com a frequência para verificar o status de conformidade do computador e com que frequência fazer backup da chave de recuperação do cliente.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-159">Set this frequency based on the requirement established by your company on how frequently to check the compliance status of the computer, and how frequently to back up the client recovery key.</span></span></p></li>
<li><p><strong><span data-ttu-id="3bdb0-160">Ponto de extremidade do serviço de relatório de status do MBAM </strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb0-160">MBAM Status reporting service endpoint</strong>.</span></span> <span data-ttu-id="3bdb0-161">Esta é a segunda configuração de política que você deve configurar para habilitar o gerenciamento de criptografia do BitLocker do cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-161">This is the second policy setting that you must configure to enable MBAM Client BitLocker encryption management.</span></span> <span data-ttu-id="3bdb0-162">Para essa configuração, insira o local do ponto de extremidade usando o seguinte exemplo: <strong> http:// </strong><em> &lt; MBAM administração e monitoramento nome &gt; </em><strong> do servidor de monitoramento: </strong><em> &lt; porta o serviço Web está associado a &gt; </em><strong> /MBAMComplianceStatusService/StatusReportingService.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-162">For this setting, enter the endpoint location by using the following example: <strong>http://</strong><em>&lt;MBAM Administration and Monitoring Server Name&gt;</em><strong>:</strong><em>&lt;port the web service is bound to&gt;</em><strong>/MBAMComplianceStatusService/StatusReportingService.</span></span> <span data-ttu-id="3bdb0-163">svc </strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb0-163">svc</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bdb0-164">Permitir verificação de compatibilidade de hardware</span><span class="sxs-lookup"><span data-stu-id="3bdb0-164">Allow hardware compatibility checking</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bdb0-165">Configuração sugerida: <strong> habilitada</span><span class="sxs-lookup"><span data-stu-id="3bdb0-165">Suggested Configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="3bdb0-166">Essa configuração de política permite que você gerencie a verificação de compatibilidade de hardware antes de habilitar a proteção BitLocker em unidades de computadores cliente do MBAM.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-166">This policy setting lets you manage the verification of hardware compatibility before you enable BitLocker protection on drives of MBAM client computers.</span></span></p>
<p><span data-ttu-id="3bdb0-167">Você deve habilitar essa opção de política se a sua empresa tiver hardware de computador ou computadores mais antigos que não dão suporte ao Trusted Platform Module (TPM).</span><span class="sxs-lookup"><span data-stu-id="3bdb0-167">You should enable this policy option if your enterprise has older computer hardware or computers that do not support Trusted Platform Module (TPM).</span></span> <span data-ttu-id="3bdb0-168">Se qualquer um desses critérios for verdadeiro, habilite a verificação de compatibilidade de hardware para garantir que o MBAM seja aplicado somente a modelos de computador que dão suporte ao BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-168">If either of these criteria is true, enable the hardware compatibility verification to make sure that MBAM is applied only to computer models that support BitLocker.</span></span> <span data-ttu-id="3bdb0-169">Se todos os computadores de sua organização oferecerem suporte ao BitLocker, você não precisará implantar a compatibilidade de hardware e poderá definir essa política como <strong> não configurada </strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb0-169">If all computers in your organization support BitLocker, you do not have to deploy the Hardware Compatibility, and you can set this policy to <strong>Not Configured</strong>.</span></span></p>
<p><span data-ttu-id="3bdb0-170">Se você habilitar essa configuração de política, o modelo do computador será validado em relação à lista de compatibilidade de hardware uma vez a cada 24 horas, antes que a política habilite a proteção BitLocker em uma unidade de computador.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-170">If you enable this policy setting, the model of the computer is validated against the hardware compatibility list once every 24 hours, before the policy enables BitLocker protection on a computer drive.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3bdb0-171">Observação</span><span class="sxs-lookup"><span data-stu-id="3bdb0-171">Note</span></span></strong><br/><p><span data-ttu-id="3bdb0-172">Antes de habilitar essa configuração de política, verifique se você configurou a <strong> configuração de ponto de extremidade do serviço de hardware e recuperação do MBAM </strong> nas <strong> Opções de política configurar serviços MBAM </strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb0-172">Before enabling this policy setting, make sure that you have configured the <strong>MBAM Recovery and Hardware service endpoint</strong> setting in the <strong>Configure MBAM Services</strong> policy options.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="3bdb0-173">Se você desabilitar ou não definir essa configuração de política, o modelo do computador não será validado em relação à lista de compatibilidade de hardware.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-173">If you either disable or do not configure this policy setting, the computer model is not validated against the hardware compatibility list.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bdb0-174">Configurar a política de isenção de usuário</span><span class="sxs-lookup"><span data-stu-id="3bdb0-174">Configure user exemption policy</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bdb0-175">Configuração sugerida: <strong> não configurada</span><span class="sxs-lookup"><span data-stu-id="3bdb0-175">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="3bdb0-176">Essa configuração de política permite configurar um endereço de site, endereço de email ou número de telefone que instruirá o usuário a solicitar uma isenção da criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-176">This policy setting lets you configure a web site address, email address, or phone number that will instruct a user to request an exemption from BitLocker encryption.</span></span></p>
<p><span data-ttu-id="3bdb0-177">Se você habilitar essa configuração de política e fornecer um endereço de site, endereço de email ou número de telefone, os usuários verão uma caixa de diálogo com instruções sobre como solicitar uma isenção da proteção do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-177">If you enable this policy setting and provide a web site address, email address, or phone number, users will see a dialog with instructions on how to apply for an exemption from BitLocker protection.</span></span> <span data-ttu-id="3bdb0-178">Para obter mais informações sobre como habilitar as isenções de criptografia BitLocker para usuários, consulte <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)"> como gerenciar isenções de criptografia de usuário do usuário </a> .</span><span class="sxs-lookup"><span data-stu-id="3bdb0-178">For more information about how to enable BitLocker encryption exemptions for users, see <a href="how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md" data-raw-source="[How to Manage User BitLocker Encryption Exemptions](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)">How to Manage User BitLocker Encryption Exemptions</a>.</span></span></p>
<p><span data-ttu-id="3bdb0-179">Se você desabilitar ou não definir essa configuração de política, as instruções sobre como solicitar uma solicitação de isenção não serão apresentadas aos usuários.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-179">If you either disable or do not configure this policy setting, the instructions about how to apply for an exemption request will not be presented to users.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="3bdb0-180">Observação</span><span class="sxs-lookup"><span data-stu-id="3bdb0-180">Note</span></span></strong><br/><p><span data-ttu-id="3bdb0-181">Isenção de usuário é gerenciada por usuário, não por computador.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-181">User exemption is managed per user, not per computer.</span></span> <span data-ttu-id="3bdb0-182">Se vários usuários fizerem logon no mesmo computador e um usuário não estiver isento, o computador será criptografado.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-182">If multiple users log on to the same computer and one user is not exempt, the computer will be encrypted.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="3bdb0-183">Definições de política de unidade fixa</span><span class="sxs-lookup"><span data-stu-id="3bdb0-183">Fixed Drive policy definitions</span></span>


<span data-ttu-id="3bdb0-184">Esta seção descreve as definições de política de unidade fixa para MBAM, que podem ser encontradas no nó GPO a seguir: modelos administrativos de **configuração de computador** \\ **Administrative Templates** \\ **componentes** \\ **do Windows MDOP MBAM (gerenciamento de BitLocker)**  \\  **unidade fixa**.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-184">This section describes the Fixed Drive policy definitions for MBAM, which can be found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Fixed Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3bdb0-185">Nome da política</span><span class="sxs-lookup"><span data-stu-id="3bdb0-185">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="3bdb0-186">Visão geral e configuração de política sugerida</span><span class="sxs-lookup"><span data-stu-id="3bdb0-186">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bdb0-187">Configurações de criptografia de unidade de dados fixas</span><span class="sxs-lookup"><span data-stu-id="3bdb0-187">Fixed data drive encryption settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bdb0-188">Configuração sugerida: <strong> habilitada </strong> e marque a <strong> caixa de seleção Habilitar desbloqueio automático de unidade de dados fixa </strong> se o volume do sistema operacional precisar ser criptografado.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-188">Suggested Configuration: <strong>Enabled</strong>, and select the <strong>Enable auto-unlock fixed data drive</strong> check box if the operating system volume is required to be encrypted.</span></span></p>
<p><span data-ttu-id="3bdb0-189">Essa configuração de política permite que você gerencie se deseja ou não criptografar as unidades fixas.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-189">This policy setting lets you manage whether or not to encrypt the fixed drives.</span></span></p>
<p><span data-ttu-id="3bdb0-190">Quando você habilita essa política, não desabilite a <strong> política configurar o uso da senha para unidades de dados fixas </strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb0-190">When you enable this policy, do not disable the <strong>Configure use of password for fixed data drives</strong> policy.</span></span></p>
<p><span data-ttu-id="3bdb0-191">Se a <strong> caixa de seleção Habilitar desbloqueio automático de unidade de dados fixa </strong> estiver marcada, o volume do sistema operacional deve ser criptografado.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-191">If the <strong>Enable auto-unlock fixed data drive</strong> check box is selected, the operating system volume must be encrypted.</span></span></p>
<p><span data-ttu-id="3bdb0-192">Se você habilitar essa configuração de política, os usuários deverão colocar todas as unidades fixas em proteção BitLocker, que criptografará as unidades.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-192">If you enable this policy setting, users are required to put all fixed drives under BitLocker protection, which will encrypt the drives.</span></span></p>
<p><span data-ttu-id="3bdb0-193">Se você não configurar essa política ou se desabilitar essa política, os usuários não deverão colocar unidades fixas sob proteção BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-193">If you do not configure this policy or if you disable this policy, users are not required to put fixed drives under BitLocker protection.</span></span></p>
<p><span data-ttu-id="3bdb0-194">Se você desabilitar essa política, o agente de MBAM descriptografará todas as unidades fixas criptografadas.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-194">If you disable this policy, the MBAM agent decrypts any encrypted fixed drives.</span></span></p>
<p><span data-ttu-id="3bdb0-195">Se a criptografia do volume do sistema operacional não for necessária, desmarque a <strong> caixa de seleção Habilitar unidade de dados fixa de desbloqueio automático </strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb0-195">If encrypting the operating system volume is not required, clear the <strong>Enable auto-unlock fixed data drive</strong> check box.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bdb0-196">Negar permissão de "gravação" para unidades fixas que não estão protegidas por BitLocker</span><span class="sxs-lookup"><span data-stu-id="3bdb0-196">Deny “write” permission to fixed drives that are not protected by BitLocker</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bdb0-197">Configuração sugerida: <strong> não configurada</span><span class="sxs-lookup"><span data-stu-id="3bdb0-197">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="3bdb0-198">Essa configuração de política determina se a proteção do BitLocker é necessária para unidades fixas em um computador para que elas sejam graváveis.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-198">This policy setting determines if BitLocker protection is required for fixed drives on a computer so that they are writable.</span></span> <span data-ttu-id="3bdb0-199">Essa configuração de política é aplicada quando você ativa o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-199">This policy setting is applied when you turn on BitLocker.</span></span></p>
<p><span data-ttu-id="3bdb0-200">Quando a política não está configurada, todas as unidades fixas no computador são montadas com permissões de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-200">When the policy is not configured, all fixed drives on the computer are mounted with read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bdb0-201">Permitir o acesso a unidades fixas protegidas pelo BitLocker de versões anteriores do Windows</span><span class="sxs-lookup"><span data-stu-id="3bdb0-201">Allow access to BitLocker-protected fixed drives from earlier versions of Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bdb0-202">Configuração sugerida: <strong> não configurada</span><span class="sxs-lookup"><span data-stu-id="3bdb0-202">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="3bdb0-203">Habilite essa política para desbloquear e visualizar as unidades fixas que estão formatadas com o sistema de arquivos FAT (File Allocation Table) em computadores que executam o Windows Server 2008, o Windows Vista, o Windows XP com SP3 ou o Windows XP com SP2.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-203">Enable this policy to unlock and view the fixed drives that are formatted with the file allocation table (FAT) file system on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p>
<p><span data-ttu-id="3bdb0-204">Esses sistemas operacionais têm permissões somente leitura para unidades protegidas pelo BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-204">These operating systems have read-only permissions to BitLocker-protected drives.</span></span></p>
<p><span data-ttu-id="3bdb0-205">Quando a política está desabilitada, as unidades fixas formatadas com o sistema de arquivos FAT não podem ser desbloqueadas e seu conteúdo não pode ser visualizado em computadores que executam o Windows Server 2008, o Windows Vista, o Windows XP com SP3 ou o Windows XP com SP2.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-205">When the policy is disabled, fixed drives formatted with the FAT file system cannot be unlocked and their content cannot be viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bdb0-206">Configurar o uso da senha para unidades fixas</span><span class="sxs-lookup"><span data-stu-id="3bdb0-206">Configure use of password for fixed drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bdb0-207">Configuração sugerida: <strong> não configurada</span><span class="sxs-lookup"><span data-stu-id="3bdb0-207">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="3bdb0-208">Habilite essa política para configurar a proteção por senha em unidades fixas.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-208">Enable this policy to configure password protection on fixed drives.</span></span></p>
<p><span data-ttu-id="3bdb0-209">Quando a política não está configurada, as senhas são compatíveis com as configurações padrão, que não incluem requisitos de complexidade de senha e exigem apenas oito caracteres.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-209">When the policy is not configured, passwords will be supported with the default settings, which do not include password complexity requirements and require only eight characters.</span></span></p>
<p><span data-ttu-id="3bdb0-210">Para maior segurança, habilite essa política e selecione <strong> exigir senha para unidade de dados fixo </strong> , selecione <strong> exigir complexidade de senha </strong> e defina o <strong> comprimento mínimo da senha </strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb0-210">For higher security, enable this policy and select <strong>Require password for fixed data drive</strong>, select <strong>Require password complexity</strong>, and set the desired <strong>minimum password length</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bdb0-211">Escolher como as unidades fixas protegidas pelo BitLocker podem ser recuperadas</span><span class="sxs-lookup"><span data-stu-id="3bdb0-211">Choose how BitLocker-protected fixed drives can be recovered</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bdb0-212">Configuração sugerida: <strong> não configurada</span><span class="sxs-lookup"><span data-stu-id="3bdb0-212">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="3bdb0-213">Configure essa política para habilitar o agente de recuperação de dados BitLocker ou para salvar as informações de recuperação do BitLocker nos serviços de domínio Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="3bdb0-213">Configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="3bdb0-214">Quando essa política não está configurada, o agente de recuperação de dados BitLocker é permitido e não é feito o backup das informações de recuperação para o AD DS.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-214">When this policy is not configured, the BitLocker data recovery agent is allowed, and recovery information is not backed up to AD DS.</span></span> <span data-ttu-id="3bdb0-215">O MBAM não exige o backup das informações de recuperação para o AD DS.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-215">MBAM does not require the recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="3bdb0-216">Definições de política de unidade do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="3bdb0-216">Operating System Drive policy definitions</span></span>


<span data-ttu-id="3bdb0-217">Esta seção descreve as definições de política de unidade do sistema operacional para MBAM, encontradas no seguinte nó de GPO: modelos administrativos de **configuração de computador** \\ **Administrative Templates** \\ **componentes do Windows** \\ **MDOP MBAM (gerenciamento de BitLocker)**  \\  **unidade do sistema operacional**.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-217">This section describes the Operating System Drive policy definitions for MBAM, found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Operating System Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3bdb0-218">Nome da política</span><span class="sxs-lookup"><span data-stu-id="3bdb0-218">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="3bdb0-219">Visão geral e configuração de política sugerida</span><span class="sxs-lookup"><span data-stu-id="3bdb0-219">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bdb0-220">Configurações de criptografia de unidade do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="3bdb0-220">Operating system drive encryption settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bdb0-221">Configuração sugerida: <strong> habilitada</span><span class="sxs-lookup"><span data-stu-id="3bdb0-221">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="3bdb0-222">Essa configuração de política determina se a unidade do sistema operacional será criptografada.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-222">This policy setting determines if the operating system drive will be encrypted.</span></span></p>
<p><span data-ttu-id="3bdb0-223">Configure esta política para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3bdb0-223">Configure this policy to do the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="3bdb0-224">Impor a proteção BitLocker para a unidade do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-224">Enforce BitLocker protection for the operating system drive.</span></span></p></li>
<li><p><span data-ttu-id="3bdb0-225">Configurar o uso do PIN para usar um PIN do Trusted Platform Module (TPM) para proteção do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-225">Configure PIN usage to use a Trusted Platform Module (TPM) PIN for operating system protection.</span></span></p></li>
<li><p><span data-ttu-id="3bdb0-226">Configure PINs de inicialização avançados para permitir caracteres como letras maiúsculas e minúsculas e números.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-226">Configure enhanced startup PINs to permit characters such as uppercase and lowercase letters, and numbers.</span></span> <span data-ttu-id="3bdb0-227">O MBAM não dá suporte ao uso de símbolos e espaços para PINs avançados, mesmo que o BitLocker dê suporte a símbolos e espaços.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-227">MBAM does not support the use of symbols and spaces for enhanced PINs, even though BitLocker supports symbols and spaces.</span></span></p></li>
</ul>
<p><span data-ttu-id="3bdb0-228">Se você habilitar essa configuração de política, os usuários deverão proteger a unidade do sistema operacional usando o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-228">If you enable this policy setting, users are required to secure the operating system drive by using BitLocker.</span></span></p>
<p><span data-ttu-id="3bdb0-229">Se você não configurar ou se desabilitar a configuração, os usuários não serão obrigados a proteger a unidade do sistema operacional usando o BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-229">If you do not configure or if you disable the setting, users are not required to secure the operating system drive by using BitLocker.</span></span></p>
<p><span data-ttu-id="3bdb0-230">Se você desabilitar essa política, o agente de MBAM descriptografará o volume do sistema operacional, se estiver criptografado.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-230">If you disable this policy, the MBAM agent decrypts the operating system volume if it is encrypted.</span></span></p>
<p><span data-ttu-id="3bdb0-231">Quando habilitada, essa configuração de política requer que os usuários protejam o sistema operacional usando a proteção do BitLocker, e a unidade é criptografada.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-231">When it is enabled, this policy setting requires users to secure the operating system by using BitLocker protection, and the drive is encrypted.</span></span> <span data-ttu-id="3bdb0-232">Com base em seus requisitos de criptografia, você pode selecionar o método de proteção para a unidade do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-232">Based on your encryption requirements, you may select the method of protection for the operating system drive.</span></span></p>
<p><span data-ttu-id="3bdb0-233">Para obter requisitos de segurança mais altos, use TPM + PIN, permitir pinos aprimorados e definir o comprimento mínimo do PIN como oito caracteres.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-233">For higher security requirements, use TPM + PIN, allow enhanced PINs, and set the minimum PIN length to eight characters.</span></span></p>
<p><span data-ttu-id="3bdb0-234">Quando essa política é habilitada com o protetor TPM + PIN, você pode considerar a desabilitação das seguintes políticas em <strong> configurações de suspensão do gerenciamento de energia do sistema </strong>  /  <strong> </strong>  /  <strong> </strong> :</span><span class="sxs-lookup"><span data-stu-id="3bdb0-234">When this policy is enabled with the TPM + PIN protector, you can consider disabling the following policies under <strong>System</strong> / <strong>Power Management</strong> / <strong>Sleep Settings</strong>:</span></span></p>
<ul>
<li><p><span data-ttu-id="3bdb0-235">Permitir Estados de espera (S1-S3) quando em repouso (conectado)</span><span class="sxs-lookup"><span data-stu-id="3bdb0-235">Allow Standby States (S1-S3) When Sleeping (Plugged In)</span></span></p></li>
<li><p><span data-ttu-id="3bdb0-236">Permitir Estados de espera (S1-S3) quando em repouso (bateria)</span><span class="sxs-lookup"><span data-stu-id="3bdb0-236">Allow Standby States (S1-S3) When Sleeping (On Battery)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bdb0-237">Configurar o perfil de validação da plataforma TPM</span><span class="sxs-lookup"><span data-stu-id="3bdb0-237">Configure TPM platform validation profile</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bdb0-238">Configuração sugerida: <strong> não configurada</span><span class="sxs-lookup"><span data-stu-id="3bdb0-238">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="3bdb0-239">Essa configuração de política permite configurar como o hardware de segurança TPM em um computador protege a chave de criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-239">This policy setting lets you configure how the TPM security hardware on a computer secures the BitLocker encryption key.</span></span> <span data-ttu-id="3bdb0-240">Essa configuração de política não se aplicará se o computador não tiver um TPM compatível ou se o BitLocker já tiver habilitado a proteção TPM.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-240">This policy setting does not apply if the computer does not have a compatible TPM or if BitLocker already has TPM protection enabled.</span></span></p>
<p><span data-ttu-id="3bdb0-241">Quando essa política não está configurada, o TPM usa o perfil de validação de plataforma padrão ou o perfil de validação de plataforma especificado pelo script de instalação.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-241">When this policy is not configured, the TPM uses the default platform validation profile or the platform validation profile specified by the setup script.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bdb0-242">Escolher como recuperar unidades do sistema operacional protegidas pelo BitLocker</span><span class="sxs-lookup"><span data-stu-id="3bdb0-242">Choose how to recover BitLocker-protected operating system drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bdb0-243">Configuração sugerida: <strong> não configurada</span><span class="sxs-lookup"><span data-stu-id="3bdb0-243">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="3bdb0-244">Configure essa política para habilitar o agente de recuperação de dados BitLocker ou para salvar as informações de recuperação do BitLocker nos serviços de domínio Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="3bdb0-244">Configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="3bdb0-245">Quando essa política não está configurada, o agente de recuperação de dados é permitido, e não é feito o backup das informações de recuperação para o AD DS.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-245">When this policy is not configured, the data recovery agent is allowed, and the recovery information is not backed up to AD DS.</span></span></p>
<p><span data-ttu-id="3bdb0-246">A operação MBAM não exige o backup das informações de recuperação para o AD DS.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-246">MBAM operation does not require the recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="3bdb0-247">Definições de política de unidade removível</span><span class="sxs-lookup"><span data-stu-id="3bdb0-247">Removable Drive policy definitions</span></span>


<span data-ttu-id="3bdb0-248">Esta seção descreve as definições de política de unidade removível para MBAM, encontradas no seguinte nó de GPO: modelos administrativos de **configuração de computador** \\ **Administrative Templates** \\ **componentes do Windows** \\ **MDOP MBAM (gerenciamento de BitLocker)**  \\  **unidade removível**.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-248">This section describes the Removable Drive Policy definitions for MBAM, found at the following GPO node: **Computer Configuration**\\**Administrative Templates**\\**Windows Components**\\**MDOP MBAM (BitLocker Management)** \\ **Removable Drive**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3bdb0-249">Nome da política</span><span class="sxs-lookup"><span data-stu-id="3bdb0-249">Policy Name</span></span></th>
<th align="left"><span data-ttu-id="3bdb0-250">Visão geral e configuração de política sugerida</span><span class="sxs-lookup"><span data-stu-id="3bdb0-250">Overview and Suggested Policy Setting</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bdb0-251">Controlar o uso do BitLocker em unidades removíveis</span><span class="sxs-lookup"><span data-stu-id="3bdb0-251">Control the use of BitLocker on removable drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bdb0-252">Configuração sugerida: <strong> habilitada</span><span class="sxs-lookup"><span data-stu-id="3bdb0-252">Suggested configuration: <strong>Enabled</span></span></strong></p>
<p><span data-ttu-id="3bdb0-253">Esta política controla o uso do BitLocker em unidades de dados removíveis.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-253">This policy controls the use of BitLocker on removable data drives.</span></span></p>
<p><span data-ttu-id="3bdb0-254">Habilite a <strong> opção permitir que os usuários apliquem a proteção BitLocker em unidades de dados removíveis </strong> , para permitir que os usuários executem o assistente de configuração do BitLocker em uma unidade de dados removível.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-254">Enable the <strong>Allow users to apply BitLocker protection on removable data drives</strong> option, to allow users to run the BitLocker setup wizard on a removable data drive.</span></span></p>
<p><span data-ttu-id="3bdb0-255">Habilite a <strong> opção permitir que os usuários suspendem e descriptografem o BitLocker em unidades de dados removíveis </strong> para permitir que os usuários removam a criptografia de unidade de disco BitLocker da unidade ou para suspender a criptografia enquanto a manutenção é realizada.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-255">Enable the <strong>Allow users to suspend and decrypt BitLocker on removable data drives</strong> option to allow users to remove BitLocker drive encryption from the drive or to suspend the encryption while maintenance is performed.</span></span></p>
<p><span data-ttu-id="3bdb0-256">Quando essa política está habilitada e a <strong> opção permitir que os usuários apliquem a proteção BitLocker em unidades de dados removíveis </strong> , o cliente MBAM salva as informações de recuperação sobre unidades removíveis no servidor de recuperação de chave do MBAM e permite que os usuários recuperem a unidade se a senha for perdida.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-256">When this policy is enabled and the <strong>Allow users to apply BitLocker protection on removable data drives</strong> option is selected, the MBAM Client saves the recovery information about removable drives to the MBAM key recovery server, and it allows users to recover the drive if the password is lost.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bdb0-257">Negar permissões de "gravação" para unidades removíveis que não estão protegidas pelo BitLocker</span><span class="sxs-lookup"><span data-stu-id="3bdb0-257">Deny the “write” permissions to removable drives that are not protected by BitLocker</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bdb0-258">Configuração sugerida: <strong> não configurada</span><span class="sxs-lookup"><span data-stu-id="3bdb0-258">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="3bdb0-259">Habilite essa política para permitir permissões somente gravação para unidades protegidas pelo BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-259">Enable this policy to allow write-only permissions to BitLocker protected drives.</span></span></p>
<p><span data-ttu-id="3bdb0-260">Quando essa política está habilitada, todas as unidades de dados removíveis no computador exigem criptografia para que as permissões de gravação sejam permitidas.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-260">When this policy is enabled, all removable data drives on the computer require encryption before write permissions are allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bdb0-261">Permitir o acesso a unidades removíveis protegidas pelo BitLocker de versões anteriores do Windows</span><span class="sxs-lookup"><span data-stu-id="3bdb0-261">Allow access to BitLocker-protected removable drives from earlier versions of Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bdb0-262">Configuração sugerida: <strong> não configurada</span><span class="sxs-lookup"><span data-stu-id="3bdb0-262">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="3bdb0-263">Habilite essa política para desbloquear e exibir as unidades fixas formatadas com o sistema de arquivos (FAT) em computadores que executam o Windows Server 2008, o Windows Vista, o Windows XP com SP3 ou o Windows XP com SP2.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-263">Enable this policy to unlock and view the fixed drives that are formatted with the (FAT) file system on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p>
<p><span data-ttu-id="3bdb0-264">Esses sistemas operacionais têm permissões somente leitura para unidades protegidas pelo BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-264">These operating systems have read-only permissions to BitLocker-protected drives.</span></span></p>
<p><span data-ttu-id="3bdb0-265">Quando a política está desabilitada, as unidades removíveis formatadas com o sistema de arquivos FAT não podem ser desbloqueadas e seu conteúdo não pode ser visualizado em computadores que executam o Windows Server 2008, o Windows Vista, o Windows XP com SP3 ou o Windows XP com SP2.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-265">When the policy is disabled, removable drives formatted with the FAT file system cannot be unlocked and their content cannot be viewed on computers that are running Windows Server 2008, Windows Vista, Windows XP with SP3, or Windows XP with SP2.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bdb0-266">Configurar o uso da senha para unidades de dados removíveis</span><span class="sxs-lookup"><span data-stu-id="3bdb0-266">Configure the use of password for removable data drives</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bdb0-267">Configuração sugerida: <strong> não configurada</span><span class="sxs-lookup"><span data-stu-id="3bdb0-267">Suggested configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="3bdb0-268">Habilite essa política para configurar a proteção por senha em unidades de dados removíveis.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-268">Enable this policy to configure password protection on removable data drives.</span></span></p>
<p><span data-ttu-id="3bdb0-269">Quando essa política não está configurada, há suporte para senhas com as configurações padrão, que não incluem requisitos de complexidade de senha e exigem apenas oito caracteres.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-269">When this policy is not configured, passwords are supported with the default settings, which do not include password complexity requirements and require only eight characters.</span></span></p>
<p><span data-ttu-id="3bdb0-270">Para aumentar a segurança, você pode habilitar essa política e selecionar <strong> exigir senha para unidade de dados removível </strong> , selecionar <strong> exigir complexidade de senha </strong> e, em seguida, definir o <strong> comprimento mínimo de senha preferencial </strong> .</span><span class="sxs-lookup"><span data-stu-id="3bdb0-270">For increased security, you can enable this policy and select <strong>Require password for removable data drive</strong>, select <strong>Require password complexity</strong>, and then set the preferred <strong>minimum password length</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bdb0-271">Escolher como as unidades removíveis protegidas pelo BitLocker podem ser recuperadas</span><span class="sxs-lookup"><span data-stu-id="3bdb0-271">Choose how BitLocker-protected removable drives can be recovered</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bdb0-272">Configuração sugerida: <strong> não configurada</span><span class="sxs-lookup"><span data-stu-id="3bdb0-272">Suggested Configuration: <strong>Not Configured</span></span></strong></p>
<p><span data-ttu-id="3bdb0-273">Você pode configurar esta política para habilitar o agente de recuperação de dados BitLocker ou salvar as informações de recuperação do BitLocker nos serviços de domínio Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="3bdb0-273">You can configure this policy to enable the BitLocker data recovery agent or to save BitLocker recovery information to Active Directory Domain Services (AD DS).</span></span></p>
<p><span data-ttu-id="3bdb0-274">Quando a política é definida como <strong> não configurada </strong> , o agente de recuperação de dados é permitido e não é feito o backup das informações de recuperação no AD DS.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-274">When the policy is set to <strong>Not Configured</strong>, the data recovery agent is allowed and recovery information is not backed up to AD DS.</span></span></p>
<p><span data-ttu-id="3bdb0-275">A operação MBAM não exige o backup das informações de recuperação para o AD DS.</span><span class="sxs-lookup"><span data-stu-id="3bdb0-275">MBAM operation does not require the recovery information to be backed up to AD DS.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="3bdb0-276">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3bdb0-276">Related topics</span></span>


[<span data-ttu-id="3bdb0-277">Preparando seu ambiente para o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="3bdb0-277">Preparing your Environment for MBAM 1.0</span></span>](preparing-your-environment-for-mbam-10.md)









