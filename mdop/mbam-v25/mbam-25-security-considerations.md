---
title: Considerações sobre segurança do MBAM 2.5
description: Considerações sobre segurança do MBAM 2.5
author: dansimp
ms.assetid: f6613c63-b32b-45fb-a6e8-673d6dae7d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: 86a756ab6f983fa1f22de6835b5993e1215d1dbe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799952"
---
# <span data-ttu-id="c2ab7-103">Considerações sobre segurança do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c2ab7-103">MBAM 2.5 Security Considerations</span></span>


<span data-ttu-id="c2ab7-104">Este tópico contém as seguintes informações sobre como proteger a administração e o monitoramento do Microsoft BitLocker (MBAM):</span><span class="sxs-lookup"><span data-stu-id="c2ab7-104">This topic contains the following information about how to secure Microsoft BitLocker Administration and Monitoring (MBAM):</span></span>

-   [<span data-ttu-id="c2ab7-105">Configurar o MBAM para fazer a caução do TPM e armazenar senhas do OwnerAuth</span><span class="sxs-lookup"><span data-stu-id="c2ab7-105">Configure MBAM to escrow the TPM and store OwnerAuth passwords</span></span>](#bkmk-tpm)

-   [<span data-ttu-id="c2ab7-106">Configurar o MBAM para desbloquear automaticamente o TPM após um bloqueio</span><span class="sxs-lookup"><span data-stu-id="c2ab7-106">Configure MBAM to automatically unlock the TPM after a lockout</span></span>](#bkmk-autounlock)

-   [<span data-ttu-id="c2ab7-107">Conexões seguras com o SQL Server</span><span class="sxs-lookup"><span data-stu-id="c2ab7-107">Secure connections to SQL Server</span></span>](#bkmk-secure-databases)

-   [<span data-ttu-id="c2ab7-108">Criar contas e grupos</span><span class="sxs-lookup"><span data-stu-id="c2ab7-108">Create accounts and groups</span></span>](#bkmk-accts-groups)

-   [<span data-ttu-id="c2ab7-109">Usar arquivos de log do MBAM</span><span class="sxs-lookup"><span data-stu-id="c2ab7-109">Use MBAM log files</span></span>](#bkmk-logfiles)

-   [<span data-ttu-id="c2ab7-110">Analisar considerações do TDE de banco de dados MBAM</span><span class="sxs-lookup"><span data-stu-id="c2ab7-110">Review MBAM database TDE considerations</span></span>](#bkmk-tde)

-   [<span data-ttu-id="c2ab7-111">Entender as considerações gerais de segurança</span><span class="sxs-lookup"><span data-stu-id="c2ab7-111">Understand general security considerations</span></span>](#bkmk-general-security)

## <a href="" id="bkmk-tpm"></a><span data-ttu-id="c2ab7-112">Configurar o MBAM para fazer a caução do TPM e armazenar senhas do OwnerAuth</span><span class="sxs-lookup"><span data-stu-id="c2ab7-112">Configure MBAM to escrow the TPM and store OwnerAuth passwords</span></span>

<span data-ttu-id="c2ab7-113">**Observação** Para o Windows 10, versão 1607 ou posterior, somente o Windows pode apropriar-se do TPM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-113">**Note** For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="c2ab7-114">Além disso, o Windows não mantém a senha de proprietário do TPM ao provisionar o TPM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-114">In addition, Windows will not retain the TPM owner password when provisioning the TPM.</span></span> <span data-ttu-id="c2ab7-115">Consulte a [senha de proprietário do TPM](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-115">See [TPM owner password](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) for further details.</span></span>

<span data-ttu-id="c2ab7-116">Dependendo da configuração, o Trusted Platform Module (TPM) será bloqueado em determinadas situações ─ como quando muitas senhas incorretas são inseridas ─ e podem permanecer bloqueadas por um período de tempo.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-116">Depending on its configuration, the Trusted Platform Module (TPM) will lock itself in certain situations ─ such as when too many incorrect passwords are entered ─ and can remain locked for a period of time.</span></span> <span data-ttu-id="c2ab7-117">Durante o bloqueio do TPM, o BitLocker não pode acessar as chaves de criptografia para executar operações de desbloqueio ou descriptografia, exigindo que o usuário insira sua chave de recuperação do BitLocker para acessar a unidade do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-117">During TPM lockout, BitLocker cannot access the encryption keys to perform unlock or decryption operations, requiring the user to enter their BitLocker recovery key to access the operating system drive.</span></span> <span data-ttu-id="c2ab7-118">Para redefinir o bloqueio de TPM, você deve fornecer a senha de OwnerAuth do TPM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-118">To reset TPM lockout, you must provide the TPM OwnerAuth password.</span></span>

<span data-ttu-id="c2ab7-119">MBAM pode armazenar a senha do OwnerAuth do TPM no banco de dados do MBAM se ele possuir o TPM ou se ele tiver a senha em caução.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-119">MBAM can store the TPM OwnerAuth password in the MBAM database if it owns the TPM or if it escrows the password.</span></span> <span data-ttu-id="c2ab7-120">As senhas do OwnerAuth podem ser facilmente acessadas no site de administração e monitoramento quando você deve se recuperar de um bloqueio de TPM, eliminando a necessidade de aguardar que o bloqueio seja resolvido por conta própria.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-120">OwnerAuth passwords are then easily accessible on the Administration and Monitoring Website when you must recover from a TPM lockout, eliminating the need to wait for the lockout to resolve on its own.</span></span>

### <span data-ttu-id="c2ab7-121">OwnerAuth TPM de caução no Windows 8 e em versões mais recentes</span><span class="sxs-lookup"><span data-stu-id="c2ab7-121">Escrowing TPM OwnerAuth in Windows 8 and higher</span></span>

<span data-ttu-id="c2ab7-122">**Observação** Para o Windows 10, versão 1607 ou posterior, somente o Windows pode apropriar-se do TPM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-122">**Note** For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="c2ab7-123">No addiiton, o Windows não mantém a senha de proprietário do TPM ao provisionar o TPM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-123">In addiiton, Windows will not retain the TPM owner password when provisioning the TPM.</span></span> <span data-ttu-id="c2ab7-124">Consulte a [senha de proprietário do TPM](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-124">See [TPM owner password](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) for further details.</span></span>

<span data-ttu-id="c2ab7-125">No Windows 8 ou superior, o MBAM não deve mais possuir o TPM para armazenar a senha do OwnerAuth, desde que o OwnerAuth esteja disponível no computador local.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-125">In Windows 8 or higher, MBAM no longer must own the TPM to store the OwnerAuth password, as long as the OwnerAuth is available on the local machine.</span></span>

<span data-ttu-id="c2ab7-126">Para habilitar o MBAM para caução e, em seguida, armazenar senhas de OwnerAuth do TPM, você deve definir essas configurações de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-126">To enable MBAM to escrow and then store TPM OwnerAuth passwords, you must configure these Group Policy settings.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2ab7-127">Configuração da política de grupo</span><span class="sxs-lookup"><span data-stu-id="c2ab7-127">Group Policy Setting</span></span></th>
<th align="left"><span data-ttu-id="c2ab7-128">Configuração</span><span class="sxs-lookup"><span data-stu-id="c2ab7-128">Configuration</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2ab7-129">Ativar o backup do TPM nos serviços de domínio do Active Directory</span><span class="sxs-lookup"><span data-stu-id="c2ab7-129">Turn on TPM backup to Active Directory Domain Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2ab7-130">Desabilitado ou não configurado</span><span class="sxs-lookup"><span data-stu-id="c2ab7-130">Disabled or Not Configured</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2ab7-131">Configurar o nível de informações de autorização de proprietário do TPM disponíveis para o sistema operacional</span><span class="sxs-lookup"><span data-stu-id="c2ab7-131">Configure the level of TPM owner authorization information available to the operating system</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2ab7-132">Delegado/nenhum ou não configurado</span><span class="sxs-lookup"><span data-stu-id="c2ab7-132">Delegated/None or Not Configured</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c2ab7-133">O local dessas configurações de política de grupo é o sistema de modelos administrativos de **configuração do computador** &gt; **Administrative Templates** &gt; **System** &gt; **serviços de módulo de plataforma confiável**.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-133">The location of these Group Policy settings is **Computer Configuration** &gt; **Administrative Templates** &gt; **System** &gt; **Trusted Platform Module Services**.</span></span>

<span data-ttu-id="c2ab7-134">**Observação**  O Windows remove o OwnerAuth localmente após o MBAM ter a caução com êxito com essas configurações.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-134">**Note** Windows removes the OwnerAuth locally after MBAM successfully escrows it with these settings.</span></span>

 

### <span data-ttu-id="c2ab7-135">OwnerAuth TPM de caução no Windows 7</span><span class="sxs-lookup"><span data-stu-id="c2ab7-135">Escrowing TPM OwnerAuth in Windows 7</span></span>

<span data-ttu-id="c2ab7-136">No Windows 7, MBAM deve possuir o TPM para fazer automaticamente a caução do TPM OwnerAuth informações no banco de dados do MBAM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-136">In Windows 7, MBAM must own the TPM to automatically escrow TPM OwnerAuth information in the MBAM database.</span></span> <span data-ttu-id="c2ab7-137">Se o MBAM não for proprietário do TPM, você deverá usar os cmdlets de importação de dados do Active Directory do MBAM (AD) para copiar OwnerAuth do TPM do Active Directory para o banco de dados do MBAM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-137">If MBAM does not own the TPM, you must use the MBAM Active Directory (AD) Data Import cmdlets to copy TPM OwnerAuth from Active Directory into the MBAM database.</span></span>

### <span data-ttu-id="c2ab7-138">Cmdlets de importação de dados do Active MBAM do Active Directory</span><span class="sxs-lookup"><span data-stu-id="c2ab7-138">MBAM Active Directory Data Import cmdlets</span></span>

<span data-ttu-id="c2ab7-139">Os cmdlets de importação de dados do Active Directory do MBAM permitem que você recupere pacotes de chave de recuperação e senhas do OwnerAuth armazenadas no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-139">The MBAM Active Directory Data Import cmdlets let you retrieve recovery key packages and OwnerAuth passwords that are stored in Active Directory.</span></span>

<span data-ttu-id="c2ab7-140">O MBAM 2,5 SP1 Server é fornecido com quatro cmdlets do PowerShell que preenchem bancos de dados do MBAM com as informações de recuperação de volume e de proprietário do TPM armazenadas no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-140">The MBAM 2.5 SP1 server ships with four PowerShell cmdlets that pre-populate MBAM databases with the Volume recovery and TPM owner information stored in Active Directory.</span></span>

<span data-ttu-id="c2ab7-141">Para pacotes e chaves de recuperação de volume:</span><span class="sxs-lookup"><span data-stu-id="c2ab7-141">For Volume Recovery keys and packages:</span></span>

-   <span data-ttu-id="c2ab7-142">Leitura-ADRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="c2ab7-142">Read-ADRecoveryInformation</span></span>

-   <span data-ttu-id="c2ab7-143">Write-MbamRecoveryInformation</span><span class="sxs-lookup"><span data-stu-id="c2ab7-143">Write-MbamRecoveryInformation</span></span>

<span data-ttu-id="c2ab7-144">Para obter informações de proprietário do TPM:</span><span class="sxs-lookup"><span data-stu-id="c2ab7-144">For TPM Owner Information:</span></span>

-   <span data-ttu-id="c2ab7-145">Leitura-ADTpmInformation</span><span class="sxs-lookup"><span data-stu-id="c2ab7-145">Read-ADTpmInformation</span></span>

-   <span data-ttu-id="c2ab7-146">Write-MbamTpmInformation</span><span class="sxs-lookup"><span data-stu-id="c2ab7-146">Write-MbamTpmInformation</span></span>

<span data-ttu-id="c2ab7-147">Para associar usuários a computadores:</span><span class="sxs-lookup"><span data-stu-id="c2ab7-147">For Associating Users to Computers:</span></span>

-   <span data-ttu-id="c2ab7-148">Write-MbamComputerUser</span><span class="sxs-lookup"><span data-stu-id="c2ab7-148">Write-MbamComputerUser</span></span>

<span data-ttu-id="c2ab7-149">Os cmdlets Read-AD \ \* lêem informações do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-149">The Read-AD\* cmdlets read information from Active Directory.</span></span> <span data-ttu-id="c2ab7-150">Os cmdlets Write-MBAM \ \* empurram os dados para os bancos de dados do MBAM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-150">The Write-Mbam\* cmdlets push the data into the MBAM databases.</span></span> <span data-ttu-id="c2ab7-151">Consulte [a referência de cmdlet para administração e monitoramento do Microsoft Bitlocker 2,5](https://technet.microsoft.com/library/dn459018.aspx) para obter informações detalhadas sobre esses cmdlets, incluindo sintaxe, parâmetros e exemplos.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-151">See [Cmdlet Reference for Microsoft Bitlocker Administration and Monitoring 2.5](https://technet.microsoft.com/library/dn459018.aspx) for detailed information about these cmdlets, including syntax, parameters, and examples.</span></span>

<span data-ttu-id="c2ab7-152">**Criar associações de usuário para computador:** Os cmdlets de importação de dados do Active Directory do MBAM coletam informações do Active Directory e inserem os dados no banco de dados do MBAM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-152">**Create user-to-computer associations:** The MBAM Active Directory Data Import cmdlets gather information from Active Directory and insert the data into MBAM database.</span></span> <span data-ttu-id="c2ab7-153">No entanto, eles não associam usuários a volumes.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-153">However, they do not associate users to volumes.</span></span> <span data-ttu-id="c2ab7-154">Você pode baixar o Add-ComputerUser.ps1 script do PowerShell para criar associações de usuário para computador, que permitem que os usuários obtenham acesso a um computador por meio do site de administração e monitoramento ou usando o portal de autoatendimento para recuperação.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-154">You can download the Add-ComputerUser.ps1 PowerShell script to create user-to-machine associations, which let users regain access to a computer through the Administration and Monitoring Website or by using the Self-Service Portal for recovery.</span></span> <span data-ttu-id="c2ab7-155">O script Add-ComputerUser.ps1 coleta dados do atributo **gerenciado por** no Active Directory (AD), o proprietário do objeto no AD ou de um arquivo CSV personalizado.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-155">The Add-ComputerUser.ps1 script gathers data from the **Managed By** attribute in Active Directory (AD), the object owner in AD, or from a custom CSV file.</span></span> <span data-ttu-id="c2ab7-156">Em seguida, o script adiciona os usuários descobertos ao objeto de pipeline de informações de recuperação, que deve ser passado para Write-MbamRecoveryInformation para inserir os dados no banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-156">The script then adds the discovered users to the recovery information pipeline object, which must be passed to Write-MbamRecoveryInformation to insert the data into the recovery database.</span></span>

<span data-ttu-id="c2ab7-157">Baixe o Add-ComputerUser.ps1 script do PowerShell no [centro de download da Microsoft](https://go.microsoft.com/fwlink/?LinkId=613122).</span><span class="sxs-lookup"><span data-stu-id="c2ab7-157">Download the Add-ComputerUser.ps1 PowerShell script from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?LinkId=613122).</span></span>

<span data-ttu-id="c2ab7-158">Você pode especificar **ajuda Add-ComputerUser.ps1** para obter ajuda para o script, incluindo exemplos de como usar os cmdlets e o script.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-158">You can specify **help Add-ComputerUser.ps1** to get help for the script, including examples of how to use the cmdlets and the script.</span></span>

<span data-ttu-id="c2ab7-159">Para criar associações entre computadores após a instalação do servidor do MBAM, use o cmdlet do PowerShell Write-MbamComputerUser.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-159">To create user-to-computer associations after you have installed the MBAM server, use the Write-MbamComputerUser PowerShell cmdlet.</span></span> <span data-ttu-id="c2ab7-160">Semelhante ao Add-ComputerUser.ps1 script do PowerShell, esse cmdlet permite que você especifique os usuários que podem usar o portal de autoatendimento para obter informações de OwnerAuth de TPM ou senhas de recuperação de volume do computador especificado.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-160">Similar to the Add-ComputerUser.ps1 PowerShell script, this cmdlet lets you specify users that can use the Self-Service Portal to get TPM OwnerAuth information or volume recovery passwords for the specified computer.</span></span>

<span data-ttu-id="c2ab7-161">**Observação**  O agente MBAM substituirá as associações de usuário para computador quando esse computador começar a se reportar até o servidor.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-161">**Note** The MBAM agent will override user-to-computer associations when that computer begins reporting up to the server.</span></span>

 

<span data-ttu-id="c2ab7-162">**Pré-requisitos:** Os cmdlets Read-AD \ \* podem recuperar informações do AD apenas se eles forem executados como uma conta de usuário altamente privilegiada, como um administrador de domínio, ou executar como uma conta em um grupo de segurança personalizado com acesso de leitura às informações (recomendado).</span><span class="sxs-lookup"><span data-stu-id="c2ab7-162">**Prerequisites:** The Read-AD\* cmdlets can retrieve information from AD only if they are either run as a highly privileged user account, such as a Domain Administrator, or run as an account in a custom security group granted read access to the information (recommended).</span></span>

<span data-ttu-id="c2ab7-163">[Guia de operações de criptografia de unidade de disco BitLocker: recuperar volumes criptografados com o AD DS](https://technet.microsoft.com/library/cc771778(WS.10).aspx) fornece detalhes sobre como criar um grupo de segurança personalizado (ou vários grupos) com acesso de leitura às informações do anúncio.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-163">[BitLocker Drive Encryption Operations Guide: Recovering Encrypted Volumes with AD DS](https://technet.microsoft.com/library/cc771778(WS.10).aspx) provides details about creating a custom security group (or multiple groups) with read access to the AD information.</span></span>

<span data-ttu-id="c2ab7-164">**Permissões de gravação do serviço Web de hardware e recuperação do MBAM:** Os cmdlets Write-MBAM \ \* aceitam a URL do serviço de recuperação e hardware do MBAM, usados para publicar as informações de recuperação ou TPM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-164">**MBAM Recovery and Hardware Web Service Write Permissions:** The Write-Mbam\* cmdlets accept the URL of the MBAM Recovery and Hardware Service, used to publish the recovery or TPM information.</span></span> <span data-ttu-id="c2ab7-165">Geralmente, apenas uma conta de serviço do computador do domínio pode se comunicar com o serviço de recuperação e hardware do MBAM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-165">Typically, only a domain computer service account can communicate with the MBAM Recovery and Hardware Service.</span></span> <span data-ttu-id="c2ab7-166">No MBAM 2,5 SP1, você pode configurar o serviço de recuperação e de hardware do MBAM com um grupo de segurança chamado DataMigrationAccessGroup cujos membros podem ignorar a verificação da conta do serviço de computador do domínio.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-166">In MBAM 2.5 SP1, you can configure the MBAM Recovery and Hardware Service with a security group called DataMigrationAccessGroup whose members are allowed to bypass the domain computer service account check.</span></span> <span data-ttu-id="c2ab7-167">Os cmdlets Write-MBAM \ \* devem ser executados como um usuário pertencente a esse grupo configurado.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-167">The Write-Mbam\* cmdlets must be run as a user belonging to this configured group.</span></span> <span data-ttu-id="c2ab7-168">(Se preferir, as credenciais de um usuário individual no grupo configurado podem ser especificadas usando o parâmetro – Credential nos cmdlets Write-MBAM \ \*.)</span><span class="sxs-lookup"><span data-stu-id="c2ab7-168">(Alternatively, the credentials of an individual user in the configured group can be specified by using the –Credential parameter in the Write-Mbam\* cmdlets.)</span></span>

<span data-ttu-id="c2ab7-169">Você pode configurar o serviço de recuperação e de hardware do MBAM com o nome desse grupo de segurança de uma destas maneiras:</span><span class="sxs-lookup"><span data-stu-id="c2ab7-169">You can configure the MBAM Recovery and Hardware Service with the name of this security group in one of these ways:</span></span>

-   <span data-ttu-id="c2ab7-170">Forneça o nome do grupo de segurança (ou individual) no parâmetro-DataMigrationAccessGroup do cmdlet Enable-MbamWebApplication – AgentService do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-170">Provide the name of the security group (or individual) in the -DataMigrationAccessGroup parameter of the Enable-MbamWebApplication –AgentService Powershell cmdlet.</span></span>

-   <span data-ttu-id="c2ab7-171">Configure o grupo após a instalação do serviço de hardware e recuperação do MBAM, editando o arquivo web.config &lt; na &gt; pasta \\Microsoft Solution\\Recovery de gerenciamento do BitLocker e Service\\.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-171">Configure the group after the MBAM Recovery and Hardware Service has been installed by editing the web.config file in the &lt;inetpub&gt;\\Microsoft Bitlocker Management Solution\\Recovery and Hardware Service\\ folder.</span></span>

    ```xml
    <add key="DataMigrationUsersGroupName" value="<groupName>|<empty>" />
    ```

    <span data-ttu-id="c2ab7-172">onde &lt; nome_do_grupo &gt; é substituído pelo domínio e o nome do grupo (ou o usuário individual) que será usado para permitir a migração de dados do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-172">where &lt;groupName&gt; is replaced with the domain and the group name (or the individual user) that will be used to allow data migration from Active Directory.</span></span>

-   <span data-ttu-id="c2ab7-173">Use o editor de configuração no Gerenciador do IIS para editar esse appSetting.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-173">Use the Configuration Editor in IIS Manager to edit this appSetting.</span></span>

<span data-ttu-id="c2ab7-174">No exemplo a seguir, o comando, quando executado como membro do grupo ADRecoveryInformation e do grupo usuários de migração de dados, extrai as informações de recuperação de volume de computadores na unidade organizacional WORKSTATIONs (OU) no domínio contoso.com e os grava no MBAM usando o serviço de recuperação e de hardware do MBAM em execução no servidor mbam.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-174">In the following example, the command, when run as a member of both the ADRecoveryInformation group and the Data Migration Users group, will pull the volume recovery information from computers in the WORKSTATIONS organizational unit (OU) in the contoso.com domain and write them to MBAM by using the MBAM Recovery and Hardware Service running on the mbam.contoso.com server.</span></span>

``` syntax
PS C:\> Read-ADRecoveryInformation -Server contoso.com -SearchBase "OU=WORKSTATIONS,DC=CONTOSO,DC=COM" | Write-MbamRecoveryInformation -RecoveryServiceEndPoint "https://mbam.contoso.com/MBAMRecoveryAndHardwareService/CoreService.svc"
```

<span data-ttu-id="c2ab7-175">\*\*Ler-os cmdlets de leitura \ \*\*\* aceitam o nome ou o endereço IP de um computador servidor host do Active Directory para consultar informações de recuperação ou TPM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-175">**Read-AD\* cmdlets** accept the name or IP address of an Active Directory hosting server machine to query for recovery or TPM information.</span></span> <span data-ttu-id="c2ab7-176">Recomendamos fornecer os nomes distintos dos contêineres de anúncios nos quais o objeto de computador reside como o valor do parâmetro SearchBase.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-176">We recommend providing the distinguished names of the AD containers in which the computer object resides as the value of the SearchBase parameter.</span></span> <span data-ttu-id="c2ab7-177">Se os computadores estiverem armazenados em várias UOs, os cmdlets poderão aceitar a entrada de pipeline para serem executados uma vez para cada contêiner.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-177">If computers are stored across several OUs, the cmdlets can accept pipeline input to run once for each container.</span></span> <span data-ttu-id="c2ab7-178">O nome diferenciado de um contêiner de anúncios terá uma aparência semelhante a OU = máquinas, CC = contoso, DC = com.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-178">The distinguished name of an AD container will look similar to OU=Machines,DC=contoso,DC=com.</span></span> <span data-ttu-id="c2ab7-179">Executar uma pesquisa direcionada para contêineres específicos oferece os seguintes benefícios:</span><span class="sxs-lookup"><span data-stu-id="c2ab7-179">Performing a search targeted to specific containers provides the following benefits:</span></span>

-   <span data-ttu-id="c2ab7-180">Reduz o risco de tempo limite enquanto consulta um grande conjunto de um conjunto de grandes objetos de computador.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-180">Reduces the risk of timeout while querying a large AD dataset for computer objects.</span></span>

-   <span data-ttu-id="c2ab7-181">Pode omitir UOs que contenham servidores Datacenter ou outras classes de computadores para as quais o backup pode não ser desejado ou necessário.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-181">Can omit OUs containing datacenter servers or other classes of computers for which the backup might not be desired or necessary.</span></span>

<span data-ttu-id="c2ab7-182">Outra opção é fornecer o sinalizador-recurse com ou sem o SearchBase opcional para pesquisar objetos de computador em todos os contêineres sob o SearchBase especificado ou o domínio inteiro, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-182">Another option is to provide the –Recurse flag with or without the optional SearchBase to search for computer objects across all containers under the specified SearchBase or the entire domain respectively.</span></span> <span data-ttu-id="c2ab7-183">Ao usar o sinalizador-recurse, você também pode usar o parâmetro-MaxPageSize para controlar a quantidade de memória local e remota necessária para atender a consulta.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-183">When you use the -Recurse flag, you can also use the -MaxPageSize parameter to control the amount of local and remote memory required to service the query.</span></span>

<span data-ttu-id="c2ab7-184">Esses cmdlets gravam nos objetos de pipeline do tipo PsObject.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-184">These cmdlets write to the pipeline objects of type PsObject.</span></span> <span data-ttu-id="c2ab7-185">Cada ocorrência de PsObject contém uma única chave de recuperação de volume ou uma cadeia de caracteres de proprietário TPM com seu nome de computador associado, carimbo de data/hora e outras informações necessárias para publicá-lo no repositório de dados MBAM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-185">Each PsObject instance contains a single volume recovery key or TPM owner string with its associated computer name, timestamp, and other information required to publish it to the MBAM data store.</span></span>

<span data-ttu-id="c2ab7-186">Os \*\*cmdlets Write-MBAM \ \*\*\* aceitam valores de parâmetro de informações de recuperação do pipeline por nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-186">**Write-Mbam\* cmdlets** accept recovery information parameter values from the pipeline by property name.</span></span> <span data-ttu-id="c2ab7-187">Isso permite que os cmdlets Write-MBAM \ \* aceitem a saída do pipeline dos cmdlets Read-AD \ \* (por exemplo, Read-ADRecoveryInformation – Server contoso.com-recurse | Write-MbamRecoveryInformation – RecoveryServiceEndpoint mbam.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="c2ab7-187">This allows the Write-Mbam\* cmdlets to accept the pipeline output of the Read-AD\* cmdlets (for example, Read-ADRecoveryInformation –Server contoso.com –Recurse | Write-MbamRecoveryInformation –RecoveryServiceEndpoint mbam.contoso.com).</span></span>

<span data-ttu-id="c2ab7-188">Os \*\*cmdlets Write-MBAM \ \*\*\* incluem parâmetros opcionais que fornecem opções para tolerância a falhas, registro em log detalhado e preferências para a WhatIf e confirmar.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-188">The **Write-Mbam\* cmdlets** include optional parameters that provide options for fault tolerance, verbose logging, and preferences for WhatIf and Confirm.</span></span>

<span data-ttu-id="c2ab7-189">Os \*\*cmdlets Write-MBAM \ \*\*\* também incluem um parâmetro de *tempo* opcional cujo valor é um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="c2ab7-189">The **Write-Mbam\* cmdlets** also include an optional *Time* parameter whose value is a **DateTime** object.</span></span> <span data-ttu-id="c2ab7-190">Esse objeto inclui um atributo *Kind* que pode ser definido como `Local` , `UTC` , ou `Unspecified` .</span><span class="sxs-lookup"><span data-stu-id="c2ab7-190">This object includes a *Kind* attribute that can be set to `Local`, `UTC`, or `Unspecified`.</span></span> <span data-ttu-id="c2ab7-191">Quando o parâmetro *tempo* é preenchido a partir de dados obtidos do Active Directory, o tempo é convertido em UTC e esse atributo *Kind* é definido automaticamente como `UTC` .</span><span class="sxs-lookup"><span data-stu-id="c2ab7-191">When the *Time* parameter is populated from data taken from the Active Directory, the time is converted to UTC and this *Kind* attribute is set automatically to `UTC`.</span></span> <span data-ttu-id="c2ab7-192">No entanto, ao preencher o parâmetro *time* usando outra fonte, como um arquivo de texto, você deve explicitamente definir o atributo *Kind* para o valor apropriado.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-192">However, when populating the *Time* parameter using another source, such as a text file, you must explicitly set the *Kind* attribute to its appropriate value.</span></span>

<span data-ttu-id="c2ab7-193">**Observação**  Os cmdlets Read-AD \ \* não têm a capacidade de descobrir as contas de usuário que representam os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-193">**Note** The Read-AD\* cmdlets do not have the ability to discover the user accounts that represent the computer users.</span></span> <span data-ttu-id="c2ab7-194">As associações de conta de usuário são necessárias para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c2ab7-194">User account associations are needed for the following:</span></span>

-   <span data-ttu-id="c2ab7-195">Os usuários recuperem senhas/pacotes de volume usando o portal de autoatendimento</span><span class="sxs-lookup"><span data-stu-id="c2ab7-195">Users to recover volume passwords/packages by using the Self-Service portal</span></span>

-   <span data-ttu-id="c2ab7-196">Usuários que não estão no grupo de segurança usuários da assistência técnica avançada do MBAM conforme definidos durante a instalação, recuperando em nome de outros usuários</span><span class="sxs-lookup"><span data-stu-id="c2ab7-196">Users who are not in the MBAM Advanced Helpdesk Users security group as defined during installation, recovering on behalf of other users</span></span>

 

## <a href="" id="bkmk-autounlock"></a><span data-ttu-id="c2ab7-197">Configurar o MBAM para desbloquear automaticamente o TPM após um bloqueio</span><span class="sxs-lookup"><span data-stu-id="c2ab7-197">Configure MBAM to automatically unlock the TPM after a lockout</span></span>


<span data-ttu-id="c2ab7-198">Você pode configurar o MBAM 2,5 SP1 para desbloquear automaticamente o TPM em caso de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-198">You can configure MBAM 2.5 SP1 to automatically unlock the TPM in case of a lockout.</span></span> <span data-ttu-id="c2ab7-199">Se a reinicialização automática do bloqueio do TPM estiver habilitada, o MBAM pode detectar que um usuário está bloqueado e obter a senha do OwnerAuth do banco de dados do MBAM para desbloquear automaticamente o TPM para o usuário.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-199">If TPM lockout auto reset is enabled, MBAM can detect that a user is locked out and then get the OwnerAuth password from the MBAM database to automatically unlock the TPM for the user.</span></span> <span data-ttu-id="c2ab7-200">A redefinição automática do bloqueio do TPM só estará disponível se a chave de recuperação do sistema operacional desse computador foi recuperada usando o portal de autoatendimento ou o site de administração e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-200">TPM lockout auto reset is only available if the OS recovery key for that computer was retrieved by using the Self Service Portal or the Administration and Monitoring Website.</span></span>

<span data-ttu-id="c2ab7-201">**Importante**  Para habilitar a redefinição automática do bloqueio do TPM, você deve configurar esse recurso tanto no lado do servidor quanto na política de grupo do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-201">**Important** To enable TPM lockout auto reset, you must configure this feature on both the server side and in Group Policy on the client side.</span></span>

 

-   <span data-ttu-id="c2ab7-202">Para habilitar a redefinição automática do bloqueio do TPM no lado do cliente, defina a configuração da política de grupo "configurar redefinição automática do bloqueio do TPM", localizada em modelos administrativos de **configuração do computador** &gt; **Administrative Templates** &gt; **componentes do Windows** &gt; **MBAM** &gt; **Gerenciamento de cliente**.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-202">To enable TPM lockout auto reset on the client side, configure the Group Policy setting "Configure TPM lockout auto reset" located at **Computer Configuration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM** &gt; **Client Management**.</span></span>

-   <span data-ttu-id="c2ab7-203">Para habilitar a redefinição automática do bloqueio do TPM no lado do servidor, você pode verificar "habilitar a redefinição automática do bloqueio do TPM" no assistente de configuração do servidor do MBAM durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-203">To enable TPM lockout auto reset on the server side, you can check "Enable TPM lockout auto reset" in the MBAM Server Configuration wizard during setup.</span></span>

    <span data-ttu-id="c2ab7-204">Você também pode habilitar a redefinição automática do bloqueio do TPM no PowerShell especificando a opção "-reinício automático do bloqueio do TPM" ao habilitar o componente Web do serviço de agente.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-204">You can also enable TPM lockout auto reset in PowerShell by specifying the "-TPM lockout auto reset" switch while enabling the agent service web component.</span></span>

<span data-ttu-id="c2ab7-205">Depois que um usuário inserir a chave de recuperação do BitLocker que obteve no portal de autoatendimento ou o site de administração e monitoramento, o agente do MBAM determinará se o TPM está bloqueado. Se estiver bloqueado, ele tentará recuperar o TPM OwnerAuth para o computador do banco de dados do MBAM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-205">After a user enters the BitLocker recovery key they obtained from the Self Service Portal or the Administration and Monitoring Website, the MBAM agent will determine if the TPM is locked out. If it is locked out, it will attempt to retrieve the TPM OwnerAuth for the computer from the MBAM database.</span></span> <span data-ttu-id="c2ab7-206">Se o TPM OwnerAuth for recuperado com êxito, ele será usado para desbloquear o TPM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-206">If the TPM OwnerAuth is successfully retrieved, it will be used to unlock the TPM.</span></span> <span data-ttu-id="c2ab7-207">Desbloquear o TPM torna o TPM totalmente funcional e o usuário não será forçado a inserir a senha de recuperação durante reinicializações subsequentes a partir de um bloqueio de TPM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-207">Unlocking the TPM makes the TPM fully functional and the user will not be forced to enter the recovery password during subsequent reboots from a TPM lockout.</span></span>

<span data-ttu-id="c2ab7-208">A redefinição automática do bloqueio do TPM está desabilitada por padrão.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-208">TPM lockout auto reset is disabled by default.</span></span>

<span data-ttu-id="c2ab7-209">**Observação**  A redefinição automática do bloqueio do TPM só tem suporte em computadores que executam o TPM versão 1,2.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-209">**Note** TPM lockout auto reset is only supported on computers running TPM version 1.2.</span></span> <span data-ttu-id="c2ab7-210">O TPM 2,0 fornece funcionalidade interna de redefinição automática de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-210">TPM 2.0 provides built-in lockout auto reset functionality.</span></span>

 

<span data-ttu-id="c2ab7-211">**O relatório de auditoria de recuperação** inclui eventos relacionados à redefinição automática do bloqueio do TPM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-211">**The Recovery Audit Report** includes events related to TPM lockout auto reset.</span></span> <span data-ttu-id="c2ab7-212">Se for feita uma solicitação do cliente MBAM para recuperar uma senha do OwnerAuth TPM, um evento será registrado para indicar a recuperação.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-212">If a request is made from the MBAM client to retrieve a TPM OwnerAuth password, an event is logged to indicate recovery.</span></span> <span data-ttu-id="c2ab7-213">As entradas de auditoria incluirão os seguintes eventos:</span><span class="sxs-lookup"><span data-stu-id="c2ab7-213">Audit entries will include the following events:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c2ab7-214">Entradas</span><span class="sxs-lookup"><span data-stu-id="c2ab7-214">Entry</span></span></th>
<th align="left"><span data-ttu-id="c2ab7-215">Valor</span><span class="sxs-lookup"><span data-stu-id="c2ab7-215">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2ab7-216">Fonte de solicitação de auditoria</span><span class="sxs-lookup"><span data-stu-id="c2ab7-216">Audit Request Source</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2ab7-217">Desbloquear TPM de agente</span><span class="sxs-lookup"><span data-stu-id="c2ab7-217">Agent TPM unlock</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c2ab7-218">Tipo de chave</span><span class="sxs-lookup"><span data-stu-id="c2ab7-218">Key Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2ab7-219">Hash de senha TPM</span><span class="sxs-lookup"><span data-stu-id="c2ab7-219">TPM Password Hash</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c2ab7-220">Descrição do motivo</span><span class="sxs-lookup"><span data-stu-id="c2ab7-220">Reason Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="c2ab7-221">Redefinição de TPM</span><span class="sxs-lookup"><span data-stu-id="c2ab7-221">TPM Reset</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-secure-databases"></a><span data-ttu-id="c2ab7-222">Conexões seguras com o SQL Server</span><span class="sxs-lookup"><span data-stu-id="c2ab7-222">Secure connections to SQL Server</span></span>


<span data-ttu-id="c2ab7-223">No MBAM, o SQL Server se comunica com o SQL Server Reporting Services e com os serviços Web para o site de administração e monitoramento e o portal de autoatendimento.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-223">In MBAM, SQL Server communicates with SQL Server Reporting Services and with the web services for the Administration and Monitoring Website and Self-Service Portal.</span></span> <span data-ttu-id="c2ab7-224">Recomendamos que você proteja a comunicação com o SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-224">We recommend that you secure the communication with SQL Server.</span></span> <span data-ttu-id="c2ab7-225">Para obter mais informações, consulte [criptografar conexões com o SQL Server](https://technet.microsoft.com/library/ms189067.aspx).</span><span class="sxs-lookup"><span data-stu-id="c2ab7-225">For more information, see [Encrypting Connections to SQL Server](https://technet.microsoft.com/library/ms189067.aspx).</span></span>

<span data-ttu-id="c2ab7-226">Para obter mais informações sobre como proteger os sites do MBAM, consulte [planejando como proteger os sites do MBAM](planning-how-to-secure-the-mbam-websites.md).</span><span class="sxs-lookup"><span data-stu-id="c2ab7-226">For more information about securing the MBAM websites, see [Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md).</span></span>

## <a href="" id="bkmk-accts-groups"></a><span data-ttu-id="c2ab7-227">Criar contas e grupos</span><span class="sxs-lookup"><span data-stu-id="c2ab7-227">Create accounts and groups</span></span>


<span data-ttu-id="c2ab7-228">A prática recomendada para gerenciar contas de usuário é criar grupos globais de domínio e adicionar contas de usuário a eles.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-228">The best practice for managing user accounts is to create domain global groups and add user accounts to them.</span></span> <span data-ttu-id="c2ab7-229">Para obter uma descrição das contas e dos grupos recomendados, consulte [planejando para MBAM 2,5 grupos e contas](planning-for-mbam-25-groups-and-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="c2ab7-229">For a description of the recommended accounts and groups, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md).</span></span>

## <a href="" id="bkmk-logfiles"></a><span data-ttu-id="c2ab7-230">Usar arquivos de log do MBAM</span><span class="sxs-lookup"><span data-stu-id="c2ab7-230">Use MBAM log files</span></span>


<span data-ttu-id="c2ab7-231">Esta seção descreve os arquivos de log do servidor MBAM e do cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-231">This section describes the MBAM Server and MBAM Client log files.</span></span>

**<span data-ttu-id="c2ab7-232">Arquivos de log de instalação do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="c2ab7-232">MBAM Server Setup log files</span></span>**

<span data-ttu-id="c2ab7-233">O arquivo **MBAMServerSetup.exe** gera os seguintes arquivos de log na pasta **% Temp%** do usuário durante a instalação do MBAM:</span><span class="sxs-lookup"><span data-stu-id="c2ab7-233">The **MBAMServerSetup.exe** file generates the following log files in the user’s **%temp%** folder during the MBAM installation:</span></span>

-   **<span data-ttu-id="c2ab7-234">Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 Numbers &gt; . log</span><span class="sxs-lookup"><span data-stu-id="c2ab7-234">Microsoft\_BitLocker\_Administration\_and\_Monitoring\_&lt;14 numbers&gt;.log</span></span>**

    <span data-ttu-id="c2ab7-235">Registra as ações executadas durante a configuração do MBAM e a configuração do recurso do servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-235">Logs the actions taken during the MBAM setup and the MBAM Server feature configuration.</span></span>

-   **<span data-ttu-id="c2ab7-236">Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 \ _numbers &gt;\_0\_MBAMServer.msi. log</span><span class="sxs-lookup"><span data-stu-id="c2ab7-236">Microsoft\_BitLocker\_Administration\_and\_Monitoring\_&lt;14\_numbers&gt;\_0\_MBAMServer.msi.log</span></span>**

    <span data-ttu-id="c2ab7-237">Registra a ação adicional tomada durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-237">Logs additional action taken during installation.</span></span>

**<span data-ttu-id="c2ab7-238">Arquivos de log de configuração do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="c2ab7-238">MBAM Server Configuration log files</span></span>**

-   **<span data-ttu-id="c2ab7-239">Logs de aplicativos e serviços/Microsoft Windows/MBAM-configuração</span><span class="sxs-lookup"><span data-stu-id="c2ab7-239">Applications and Services Logs/Microsoft Windows/MBAM-Setup</span></span>**

    <span data-ttu-id="c2ab7-240">Registra os erros que ocorrem quando você está usando cmdlets do Windows PowerShell ou o assistente de configuração do servidor do MBAM para configurar os recursos do MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-240">Logs the errors that occur when you are using Windows Powershell cmdlets or the MBAM Server Configuration wizard to configure the MBAM Server features.</span></span>

**<span data-ttu-id="c2ab7-241">Arquivos de log de configuração do cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="c2ab7-241">MBAM Client setup log files</span></span>**

-   **<span data-ttu-id="c2ab7-242">MSI &lt; cinco caracteres aleatórios &gt; . log</span><span class="sxs-lookup"><span data-stu-id="c2ab7-242">MSI&lt;five random characters&gt;.log</span></span>**

    <span data-ttu-id="c2ab7-243">Registra as ações executadas durante a instalação do cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-243">Logs the actions taken during the MBAM Client installation.</span></span>

**<span data-ttu-id="c2ab7-244">MBAM-arquivos de log da Web</span><span class="sxs-lookup"><span data-stu-id="c2ab7-244">MBAM-Web log files</span></span>**

-   <span data-ttu-id="c2ab7-245">Mostra a atividade nos serviços e portais da Web.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-245">Shows activity from the web portals and services.</span></span>

## <a href="" id="bkmk-tde"></a><span data-ttu-id="c2ab7-246">Analisar considerações do TDE de banco de dados MBAM</span><span class="sxs-lookup"><span data-stu-id="c2ab7-246">Review MBAM database TDE considerations</span></span>


<span data-ttu-id="c2ab7-247">O recurso de criptografia transparente de dados (TDE) que está disponível no SQL Server é uma instalação opcional para as instâncias de banco de dados que hospedam os recursos de banco de dados do MBAM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-247">The transparent data encryption (TDE) feature that is available in SQL Server is an optional installation for the database instances that will host the MBAM database features.</span></span>

<span data-ttu-id="c2ab7-248">Com o TDE, você pode executar a criptografia em nível de banco de dados completa em tempo real.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-248">With TDE, you can perform real-time, full database-level encryption.</span></span> <span data-ttu-id="c2ab7-249">O TDE é a melhor opção para a criptografia em massa para atender aos padrões de segurança de dados corporativos ou conformidade normativa.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-249">TDE is the optimal choice for bulk encryption to meet regulatory compliance or corporate data security standards.</span></span> <span data-ttu-id="c2ab7-250">O TDE funciona no nível de arquivo, que é semelhante a dois recursos do Windows: o sistema de arquivos com criptografia (EFS) e a criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-250">TDE works at the file level, which is similar to two Windows features: the Encrypting File System (EFS) and BitLocker Drive Encryption.</span></span> <span data-ttu-id="c2ab7-251">Os dois recursos também criptografam dados no disco rígido.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-251">Both features also encrypt data on the hard drive.</span></span> <span data-ttu-id="c2ab7-252">O TDE não substitui a criptografia, o EFS ou o BitLocker no nível da célula.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-252">TDE does not replace cell-level encryption, EFS, or BitLocker.</span></span>

<span data-ttu-id="c2ab7-253">Quando o TDE está habilitado em um banco de dados, todos os backups são criptografados.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-253">When TDE is enabled on a database, all backups are encrypted.</span></span> <span data-ttu-id="c2ab7-254">Portanto, deve-se tomar cuidado especial para garantir que o certificado que foi usado para proteger a chave de criptografia do banco de dados tenha backup e seja mantido com o backup do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-254">Thus, special care must be taken to ensure that the certificate that was used to protect the database encryption key is backed up and maintained with the database backup.</span></span> <span data-ttu-id="c2ab7-255">Se esse certificado (ou certificados) for perdido, os dados serão ilegíveis.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-255">If this certificate (or certificates) is lost, the data will be unreadable.</span></span>

<span data-ttu-id="c2ab7-256">Faça backup do certificado com o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-256">Back up the certificate with the database.</span></span> <span data-ttu-id="c2ab7-257">Cada backup de certificado deve ter dois arquivos.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-257">Each certificate backup should have two files.</span></span> <span data-ttu-id="c2ab7-258">Esses dois arquivos devem ser arquivados.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-258">Both of these files should be archived.</span></span> <span data-ttu-id="c2ab7-259">Idealmente para segurança, o backup deve ser feito separadamente do arquivo de backup do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-259">Ideally for security, they should be backed up separately from the database backup file.</span></span> <span data-ttu-id="c2ab7-260">Você também pode considerar o uso do recurso EKM (gerenciamento de chaves extensível) (consulte gerenciamento extensível de chaves) para armazenamento e manutenção de chaves usadas para o TDE.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-260">You can alternatively consider using the extensible key management (EKM) feature (see Extensible Key Management) for storage and maintenance of keys that are used for TDE.</span></span>

<span data-ttu-id="c2ab7-261">Para obter um exemplo de como habilitar o TDE para instâncias de banco de dados do MBAM, consulte [noções básicas sobre criptografia de dados transparente (TDE)](https://technet.microsoft.com/library/bb934049.aspx).</span><span class="sxs-lookup"><span data-stu-id="c2ab7-261">For an example of how to enable TDE for MBAM database instances, see [Understanding Transparent Data Encryption (TDE)](https://technet.microsoft.com/library/bb934049.aspx).</span></span>

## <a href="" id="bkmk-general-security"></a><span data-ttu-id="c2ab7-262">Entender as considerações gerais de segurança</span><span class="sxs-lookup"><span data-stu-id="c2ab7-262">Understand general security considerations</span></span>


**<span data-ttu-id="c2ab7-263">Compreender os riscos de segurança.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-263">Understand the security risks.</span></span>** <span data-ttu-id="c2ab7-264">O risco mais sério quando você usa a administração e o monitoramento do Microsoft BitLocker é que sua funcionalidade pode ser comprometida por um usuário não autorizado que poderia reconfigurar a criptografia de unidade de disco BitLocker e obter dados de chave de criptografia BitLocker em clientes do MBAM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-264">The most serious risk when you use Microsoft BitLocker Administration and Monitoring is that its functionality could be compromised by an unauthorized user who could then reconfigure BitLocker Drive Encryption and gain BitLocker encryption key data on MBAM Clients.</span></span> <span data-ttu-id="c2ab7-265">No entanto, a perda de funcionalidade do MBAM por um curto período de tempo, devido a um ataque de negação de serviço, geralmente não tem um impacto catastrófico, ao contrário, por exemplo, perda de comunicação de emails ou de rede ou de energia.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-265">However, the loss of MBAM functionality for a short period of time, due to a denial-of-service attack, does not generally have a catastrophic impact, unlike, for example, losing e-mail or network communications, or power.</span></span>

<span data-ttu-id="c2ab7-266">**Proteja seus computadores fisicamente**.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-266">**Physically secure your computers**.</span></span> <span data-ttu-id="c2ab7-267">Não há segurança sem segurança física.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-267">There is no security without physical security.</span></span> <span data-ttu-id="c2ab7-268">Um invasor que obtém acesso físico a um servidor MBAM pode usá-lo para atacar toda a base de clientes.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-268">An attacker who gets physical access to an MBAM Server could potentially use it to attack the entire client base.</span></span> <span data-ttu-id="c2ab7-269">Todos os possíveis ataques físicos devem ser considerados de alto risco e diminuídos adequadamente.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-269">All potential physical attacks must be considered high risk and mitigated appropriately.</span></span> <span data-ttu-id="c2ab7-270">Os servidores MBAM devem ser armazenados em uma sala de servidor seguro com acesso controlado.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-270">MBAM Servers should be stored in a secure server room with controlled access.</span></span> <span data-ttu-id="c2ab7-271">Proteja esses computadores quando os administradores não estiverem fisicamente presentes fazendo com que o sistema operacional trave o computador ou usando um protetor de tela seguro.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-271">Secure these computers when administrators are not physically present by having the operating system lock the computer, or by using a secured screen saver.</span></span>

<span data-ttu-id="c2ab7-272">**Aplicar as atualizações de segurança mais recentes a todos os computadores**.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-272">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="c2ab7-273">Mantenha-se informado sobre novas atualizações para sistemas operacionais Windows, SQL Server e MBAM assinando o serviço de notificação de segurança no [TechCenter de segurança](https://go.microsoft.com/fwlink/?LinkId=28819).</span><span class="sxs-lookup"><span data-stu-id="c2ab7-273">Stay informed about new updates for Windows operating systems, SQL Server, and MBAM by subscribing to the Security Notification service at the [Security TechCenter](https://go.microsoft.com/fwlink/?LinkId=28819).</span></span>

<span data-ttu-id="c2ab7-274">**Use senhas fortes ou frases secretas**.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-274">**Use strong passwords or pass phrases**.</span></span> <span data-ttu-id="c2ab7-275">Sempre use senhas fortes com 15 caracteres ou mais para todas as contas de administrador do MBAM.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-275">Always use strong passwords with 15 or more characters for all MBAM administrator accounts.</span></span> <span data-ttu-id="c2ab7-276">Nunca use senhas em branco.</span><span class="sxs-lookup"><span data-stu-id="c2ab7-276">Never use blank passwords.</span></span> <span data-ttu-id="c2ab7-277">Para obter mais informações sobre os conceitos de senha, consulte [política de senha](https://technet.microsoft.com/library/hh994572.aspx).</span><span class="sxs-lookup"><span data-stu-id="c2ab7-277">For more information about password concepts, see [Password Policy](https://technet.microsoft.com/library/hh994572.aspx).</span></span>



## <span data-ttu-id="c2ab7-278">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2ab7-278">Related topics</span></span>


[<span data-ttu-id="c2ab7-279">Planejando a implantação do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="c2ab7-279">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

 
## <span data-ttu-id="c2ab7-280">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="c2ab7-280">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="c2ab7-281">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="c2ab7-281">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="c2ab7-282">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="c2ab7-282">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





