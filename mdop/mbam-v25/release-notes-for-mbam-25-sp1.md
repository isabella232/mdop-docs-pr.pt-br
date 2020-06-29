---
title: Notas de versão do MBAM 2.5 SP1
description: Notas de versão do MBAM 2.5 SP1
author: dansimp
ms.assetid: 3ac424c8-c490-4d62-aba4-1b462c02e962
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/06/2017
ms.openlocfilehash: 837892897aeca341433de54aca1228c0faeee124
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799582"
---
# <span data-ttu-id="5d2b7-103">Notas de versão do MBAM 2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="5d2b7-103">Release Notes for MBAM 2.5 SP1</span></span>


<span data-ttu-id="5d2b7-104">Para pesquisar essas notas de versão, pressione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="5d2b7-105">Leia estas notas de versão cuidadosamente antes de instalar o Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1.</span></span> <span data-ttu-id="5d2b7-106">Estas notas da versão contêm informações necessárias para instalar com êxito o MBAM e podem conter informações que não estão disponíveis na documentação do produto.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-106">These release notes contain information that is required to successfully install MBAM and can contain information that is not available in the product documentation.</span></span> <span data-ttu-id="5d2b7-107">Se estas notas de versão forem diferentes das outras documentações do MBAM 2,5 SP1, considere as últimas alterações a serem autoritativas.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-107">If these release notes differ from other MBAM 2.5 SP1 documentation, consider the latest change to be authoritative.</span></span> <span data-ttu-id="5d2b7-108">Estas notas de versão substituem o conteúdo que está incluído neste produto.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-5-sp1-known-issues"></a> <span data-ttu-id="5d2b7-109">Problemas conhecidos do MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="5d2b7-109">MBAM 2.5 SP1 known issues</span></span>


<span data-ttu-id="5d2b7-110">Esta seção contém notas de versão do MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-110">This section contains release notes for MBAM 2.5 SP1.</span></span>

### <a href="" id="powershell-read-ad--cmdlets-do-not-provide-feedback-if-user-does-not-have-sufficient-rights"></a><span data-ttu-id="5d2b7-111">Os cmdlets Read-AD \* do PowerShell não fornecem comentários se o usuário não tem direitos suficientes</span><span class="sxs-lookup"><span data-stu-id="5d2b7-111">PowerShell Read-AD\* cmdlets do not provide feedback if user does not have sufficient rights</span></span>

<span data-ttu-id="5d2b7-112">Se um usuário tentar usar os cmdlets Read-AD \ \* do PowerShell para o servidor do MBAM não tiver direitos de usuário para ler as informações de recuperação do Active Directory ou ler as informações do TPM, os cmdlets não fornecerão ao usuário qualquer erro ou aviso.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-112">If a user trying to use the PowerShell Read-AD\* cmdlets for the MBAM Server does not have user rights to read the Active Directory recovery information or to read the TPM information, the cmdlets will not provide the user with any error or warning.</span></span>

<span data-ttu-id="5d2b7-113">**Solução alternativa:** Use os cmdlets Read-AD \* do PowerShell se você tiver os direitos de usuário necessários.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-113">**Workaround:** Only use the PowerShell Read-AD\* cmdlets if you have the required user rights.</span></span>

### <span data-ttu-id="5d2b7-114">Os cmdlets de migração do MBAM Active Directory (AD) não recuperam informações de recuperação de volume</span><span class="sxs-lookup"><span data-stu-id="5d2b7-114">MBAM Active Directory (AD) Migration cmdlets do not retrieve volume recovery information</span></span>

<span data-ttu-id="5d2b7-115">MBAM cmdlets de migração do Active Directory (AD) falham ao recuperar informações de recuperação de volume para computadores em unidades organizacionais (UOs) se o caractere de barra (/) for parte do nome da UO.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-115">MBAM Active Directory (AD) Migration cmdlets fail to retrieve volume recovery information for computers in organizational units (OUs) if the forward slash character (/) is part of the OU name.</span></span> <span data-ttu-id="5d2b7-116">Recebimentos de anúncio repetidos falharão com um erro de encerramento de pipeline quando esse erro for encontrado.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-116">Repeated AD pulls will fail with a pipeline terminating error when this error is encountered.</span></span>

<span data-ttu-id="5d2b7-117">**Detalhes técnicos:** Você verá esse erro ao executar o comando:</span><span class="sxs-lookup"><span data-stu-id="5d2b7-117">**Technical Details:** You will see this error when running the command:</span></span>

``` syntax
Read-ADRecoveryInformation : Unknown error (0x80005000)
At line:1 char:1
+ Read-ADRecoveryInformation -Server "…" -SearchBase " ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: (:) [Read-ADRecoveryInformation], COMException
    + FullyQualifiedErrorId : System.Runtime.InteropServices.COMException,Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADRecoveryInformationCommand
```

<span data-ttu-id="5d2b7-118">Além disso, o rastreamento de pilha de exceção `Error[0].Exception.StackTrace` terá a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="5d2b7-118">In addition, the Exception stack trace `Error[0].Exception.StackTrace` will look like this:</span></span>

``` syntax
   at System.DirectoryServices.DirectoryEntry.Bind(Boolean throwIfFail)
   at System.DirectoryServices.DirectoryEntry.Bind()
   at System.DirectoryServices.DirectoryEntry.get_AdsObject()
   at System.DirectoryServices.PropertyValueCollection.PopulateList()
   at System.DirectoryServices.PropertyValueCollection..ctor(DirectoryEntry entry, String propertyName)
   at System.DirectoryServices.PropertyCollection.get_Item(String propertyName)
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.VerifySettingsConnectivity()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.ExecuteRead()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADInformationBase.ProcessRecord()
   at System.Management.Automation.CommandProcessor.ProcessRecord()
```

<span data-ttu-id="5d2b7-119">**Solução alternativa:** Execute uma destas tarefas para resolver essa situação:</span><span class="sxs-lookup"><span data-stu-id="5d2b7-119">**Workaround:** Perform one of these tasks to resolve this situation:</span></span>

-   <span data-ttu-id="5d2b7-120">Renomeie a UO para remover o caractere de barra e, em seguida, execute o script.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-120">Rename the OU to remove the forward slash character and then run the script.</span></span>

-   <span data-ttu-id="5d2b7-121">Para excluir qualquer UO problemática do processo de backup, localize uma lista de UOs cujos nomes não contenham o caractere de barra.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-121">To exclude any problematic OU from the backup process, find a list of OUs whose names do not contain the forward slash character.</span></span> <span data-ttu-id="5d2b7-122">Execute o script nessas UOs, uma OU por vez.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-122">Run the script on these OUs, one OU at a time.</span></span>

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> <span data-ttu-id="5d2b7-123">O MBAM não criptografa um volume e informa um erro se você definir um protetor TPM + PIN em um dispositivo tablet</span><span class="sxs-lookup"><span data-stu-id="5d2b7-123">MBAM fails to encrypt a volume and reports an error if you set a TPM + PIN protector on a tablet device</span></span>

<span data-ttu-id="5d2b7-124">Se os usuários finais tentarem definir um protetor TPM + PIN em um dispositivo tablet, o MBAM não criptografará, e ele reportará um erro.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-124">If end users try to set a TPM + PIN protector on a tablet device, MBAM fails to encrypt, and it reports an error.</span></span> <span data-ttu-id="5d2b7-125">Esse problema ocorre porque os dispositivos Tablet não têm um teclado de ambiente de pré-inicialização.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-125">This issue occurs because tablet devices do not have a pre-boot environment keyboard.</span></span>

<span data-ttu-id="5d2b7-126">**Solução alternativa:** Habilite o **uso da autenticação do BitLocker exigindo a entrada do teclado de pré-inicialização na configuração da política de grupo do tablets** .</span><span class="sxs-lookup"><span data-stu-id="5d2b7-126">**Workaround:** Enable the **Enable use of BitLocker authentication requiring preboot keyboard input on tablets** Group Policy setting.</span></span> <span data-ttu-id="5d2b7-127">Essa configuração é uma configuração de política de grupo do BitLocker e não está disponível nos modelos de política de grupo do MBAM.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-127">This setting is a BitLocker Group Policy setting and is not available in the MBAM Group Policy Templates.</span></span>

### <span data-ttu-id="5d2b7-128">O nome UPN do usuário é necessário para todas as contas de serviço</span><span class="sxs-lookup"><span data-stu-id="5d2b7-128">User principal name is required for all service accounts</span></span>

<span data-ttu-id="5d2b7-129">Um nome UPN deve ser definido para todas as contas de serviço no MBAM.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-129">A user principal name (UPN) must be set for all service accounts in MBAM.</span></span> <span data-ttu-id="5d2b7-130">Se você não conseguir criar um UPN para uma conta, uma mensagem de erro aparecerá durante o processo de configuração para indicar que o usuário ou grupo não foi encontrado no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-130">If you fail to create a UPN for an account, an error message appears during the configuration process to indicate that the user or group could not be found in Active Directory.</span></span>

<span data-ttu-id="5d2b7-131">**Solução alternativa:** Adicione o UPN à conta de serviço.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-131">**Workaround:** Add the UPN to the service account.</span></span>

### <span data-ttu-id="5d2b7-132">O portal de autoatendimento e o site de administração e monitoramento não abrem após a atualização do IIS para o .NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="5d2b7-132">Self-Service Portal and the Administration and Monitoring Website do not open after you upgrade IIS to .NET Framework 4.5</span></span>

<span data-ttu-id="5d2b7-133">Quando você atualiza os serviços de informações da Internet (IIS) para o Microsoft .NET Framework 4,5, o portal de autoatendimento e o site de administração e monitoramento não abrem.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-133">When you upgrade Internet Information Services (IIS) to the Microsoft .NET Framework 4.5, the Self-Service Portal and the Administration and Monitoring Website do not open.</span></span>

<span data-ttu-id="5d2b7-134">**Solução alternativa:** Veja a mensagem de erro do artigo [depois de instalar o .NET Framework 4,0: "não foi possível carregar o tipo ' System. ServiceModel. Activation. HttpModule '](https://go.microsoft.com/fwlink/?LinkId=393568).</span><span class="sxs-lookup"><span data-stu-id="5d2b7-134">**Workaround:** See the article [Error message after you install the .NET Framework 4.0: "Could not load type 'System.ServiceModel.Activation.HttpModule'](https://go.microsoft.com/fwlink/?LinkId=393568).</span></span>

### <span data-ttu-id="5d2b7-135">Site de administração e monitoramento exibe uma mensagem de erro "não é possível encontrar o relatório" quando os relatórios não estão configurados</span><span class="sxs-lookup"><span data-stu-id="5d2b7-135">Administration and Monitoring Website displays a "Report cannot be found" error message when Reports are not configured</span></span>

<span data-ttu-id="5d2b7-136">Se você configurar o site de administração e monitoramento e, em seguida, tentar exibir um relatório sem configurar o recurso relatórios primeiro, uma mensagem de erro indicará que o relatório não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-136">If you configure the Administration and Monitoring Website and then try to view a report without configuring the Reports feature first, an error message indicates that the report cannot be found.</span></span>

<span data-ttu-id="5d2b7-137">**Solução alternativa:** Configure o recurso relatórios antes de configurar os aplicativos Web.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-137">**Workaround:** Configure the Reports feature before you configure the web applications.</span></span>

### <span data-ttu-id="5d2b7-138">Relatórios no site de administração e monitoramento exibirão um aviso se a SSL não estiver configurada no SSRS</span><span class="sxs-lookup"><span data-stu-id="5d2b7-138">Reports in the Administration and Monitoring Website display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="5d2b7-139">Se o SSRS (SQL Server Reporting Services) não tiver sido configurado para usar SSL (Secure Socket Layer), a URL do recurso de relatórios será definida como HTTP em vez de HTTPS quando você configurar o servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-139">If SQL Server Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the Reports feature will be set to HTTP instead of to HTTPS when you configure the MBAM Server.</span></span> <span data-ttu-id="5d2b7-140">Se, em seguida, você abrir o site de administração e monitoramento e selecionar um relatório, a seguinte mensagem de erro será exibida: "somente conteúdo seguro é exibido".</span><span class="sxs-lookup"><span data-stu-id="5d2b7-140">If you then open the Administration and Monitoring Website and select a report, the following error message appears: "Only Secure Content is Displayed."</span></span>

<span data-ttu-id="5d2b7-141">**Solução alternativa:** Para mostrar o relatório, clique em **mostrar todo o conteúdo**.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-141">**Workaround:** To show the report, click **Show All Content**.</span></span> <span data-ttu-id="5d2b7-142">Para corrigir esse problema, vá para o computador do MBAM em que o SQL Server Reporting Services está instalado, execute o **Gerenciador de configuração do Reporting Services**e clique em **URL do serviço Web**.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-142">To correct this issue, go to the MBAM computer where SQL Server Reporting Services is installed, run **Reporting Services Configuration Manager**, and then click **Web Service URL**.</span></span> <span data-ttu-id="5d2b7-143">Selecione o certificado SSL apropriado para o servidor, insira a porta SSL apropriada (a porta padrão é 443) e, em seguida, clique em **aplicar**.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-143">Select the appropriate SSL certificate for the server, enter the appropriate SSL port (the default port is 443), and then click **Apply**.</span></span>

### <span data-ttu-id="5d2b7-144">Clicar em "retornar" no relatório de Resumo de conformidade do BitLocker pode gerar um erro</span><span class="sxs-lookup"><span data-stu-id="5d2b7-144">Clicking "Back" in the BitLocker Compliance Summary report might throw an error</span></span>

<span data-ttu-id="5d2b7-145">Se você fizer buscas detalhadas em um relatório de Resumo de conformidade do BitLocker e, em seguida, clicar no link **retomar** no relatório SSRS, um erro poderá ser acionado.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-145">If you drill down into a BitLocker Compliance Summary report, and then click the **Back** link in the SSRS report, an error might be thrown.</span></span>

<span data-ttu-id="5d2b7-146">**Solução alternativa:** Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-146">**Workaround:** None.</span></span>

### <span data-ttu-id="5d2b7-147">O nível de codificação é exibido incorretamente no relatório de conformidade do computador BitLocker</span><span class="sxs-lookup"><span data-stu-id="5d2b7-147">Cipher strength displays incorrectly on the BitLocker Computer Compliance report</span></span>

<span data-ttu-id="5d2b7-148">Se você não definir um nível de codificação específico no objeto **escolher método de criptografia de unidade e nível de codificação de codificação** , o relatório de conformidade do computador BitLocker na topologia de integração do Configuration Manager sempre exibirá "desconhecido" para o nível de codificação, mesmo quando a força de codificação usar o padrão de criptografia de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-148">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the BitLocker Computer Compliance report in the Configuration Manager Integration topology always displays "unknown" for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="5d2b7-149">O relatório exibe a intensidade de codificação correta se você definir um nível de codificação específico no objeto de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-149">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="5d2b7-150">**Solução alternativa:** Defina sempre um nível de codificação específico no objeto **escolher o método de criptografia de unidade e** o objeto de política de grupo de força de codificação.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-150">**Workaround:** Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="5d2b7-151">A distribuição do status de conformidade por tipo de drive exibe dados antigos após a atualização dos itens de configuração</span><span class="sxs-lookup"><span data-stu-id="5d2b7-151">Compliance Status Distribution By Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="5d2b7-152">Depois de atualizar os itens de configuração do MBAM no SystemCenter2012 ConfigurationManager, o gráfico de distribuição de status de distribuição por tipo de unidade no painel de conformidade do BitLocker Enterprise mostra os dados que se baseiam em informações de versões antigas dos itens de configuração.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-152">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="5d2b7-153">**Solução alternativa:** Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-153">**Workaround:** None.</span></span> <span data-ttu-id="5d2b7-154">Não há suporte para modificação dos itens de configuração do MBAM, e o relatório pode não aparecer como esperado.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-154">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="5d2b7-155">A configuração de segurança reforçada pode fazer com que os relatórios exibam uma mensagem de erro incorretamente</span><span class="sxs-lookup"><span data-stu-id="5d2b7-155">Enhanced Security Configuration might cause reports to display an error message incorrectly</span></span>

<span data-ttu-id="5d2b7-156">Se a configuração de segurança reforçada (ESC) do Internet Explorer estiver ativada, uma mensagem de erro "acesso negado" poderá aparecer quando você tentar exibir relatórios no servidor do MBAM.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-156">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an "Access Denied" error message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="5d2b7-157">Por padrão, a tecla ESC está ativada para proteger o servidor, diminuindo a exposição do servidor a possíveis ataques que podem ocorrer por meio de conteúdo da Web e scripts de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-157">By default, ESC is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="5d2b7-158">**Solução alternativa:** Se a mensagem de erro "acesso negado" for exibida quando você tentar exibir relatórios no servidor do MBAM, você pode definir um objeto de política de grupo ou alterar o padrão manualmente na sua imagem para desativar a configuração de segurança reforçada.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-158">**Workaround:** If the "Access Denied" error message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="5d2b7-159">Você também pode exibir os relatórios de outro computador em que a ESC não está habilitado.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-159">You can also alternatively view the reports from another computer on which ESC is not enabled.</span></span>

### <span data-ttu-id="5d2b7-160">Suporte para algoritmo de criptografia do XTS-AES para o BitLocker</span><span class="sxs-lookup"><span data-stu-id="5d2b7-160">Support for Bitlocker XTS-AES encryption algorithm</span></span>
<span data-ttu-id="5d2b7-161">Suporte adicionado ao BitLocker para o algoritmo de criptografia XTS-AES no Windows 10, versão 1511.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-161">Bitlocker added support for the XTS-AES encryption algorithm in Windows 10, version 1511.</span></span> <span data-ttu-id="5d2b7-162">Com o HF02, o MBAM adicionou suporte ao cliente para esta opção BitLocker e no HF04, o suporte do lado do servidor foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-162">With HF02, MBAM added client support for this Bitlocker option and in HF04, the server-side support was added.</span></span> <span data-ttu-id="5d2b7-163">No entanto, há uma limitação conhecida:</span><span class="sxs-lookup"><span data-stu-id="5d2b7-163">However, there is one known limitation:</span></span>

* <span data-ttu-id="5d2b7-164">Os clientes devem usar o mesmo nível de criptografia para o sistema operacional e volumes de dados na mesma máquina.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-164">Customers must use the same encryption strength for OS and data volumes on the same machine.</span></span>
<span data-ttu-id="5d2b7-165">Se forem usados diferentes níveis de criptografia, o MBAM informará a máquina como **não compatível**.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-165">If different encryption strengths are used, MBAM will report the machine as **non-compliant**.</span></span>

### <span data-ttu-id="5d2b7-166">O portal de autoatendimento adiciona automaticamente "-" na entrada de ID da chave</span><span class="sxs-lookup"><span data-stu-id="5d2b7-166">Self-Service Portal automatically adds "-" on Key ID entry</span></span>
<span data-ttu-id="5d2b7-167">A partir de HF02, o portal de autoatendimento do MBAM adiciona automaticamente o "-" na entrada de ID da chave.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-167">As of HF02, the MBAM Self-Service Portal automatically adds the '-' on Key ID entry.</span></span>  
<span data-ttu-id="5d2b7-168">**Observação:** O servidor deve ser reconfigurado para que o JavaScript entre em vigor.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-168">**Note:** The Server has to be reconfigured for the Javascript to take effect.</span></span>

### <span data-ttu-id="5d2b7-169">Os relatórios do MBAM 2,5 SP1 não funcionam e são renderizados corretamente</span><span class="sxs-lookup"><span data-stu-id="5d2b7-169">MBAM 2.5 Sp1 Reports does not work / render properly</span></span>
<span data-ttu-id="5d2b7-170">A página relatórios não é renderizada corretamente quando o SSRS está hospedado na edição do SQL Server 2016.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-170">Reports Page does not render properly when SSRS is hosted on SQL Server 2016 edition.</span></span> 
<span data-ttu-id="5d2b7-171">Por exemplo – navegar para o helpdesk – clicar em relatórios – (a parte realçada tem "x" nele) abordando isso ainda mais com o Fiddler – ela se parecerá quando clicarmos nos relatórios – ele chama a página SSRS com o formato de renderização HTML 4,0.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-171">For example – Browsing to Helpdesk – Clicking on Reports – ( Highlighted portion have “x” on it ) Digging this further with Fiddler – it does look like once we click on Reports – it calls the SSRS page with HTML 4.0 rendering format.</span></span>

<span data-ttu-id="5d2b7-172">**Solução alternativa:** Olhando para o código mestre site. e observou que o modo X-UA foi ditado como IE8.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-172">**Workaround:** Looking at the site.master code and noticed the X-UA mode was dictated as IE8.</span></span> <span data-ttu-id="5d2b7-173">À medida que o IE8 está ultrapassando o fim da vida útil, o cliente está usando o IE11.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-173">As IE8 is WAY past the end of life, and customer is using IE11.</span></span> <span data-ttu-id="5d2b7-174">Atualize a configuração para o código abaixo.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-174">Update the setting to the below code.</span></span> <span data-ttu-id="5d2b7-175">Isso permite que o site utilize tecnologias de renderização IE11</span><span class="sxs-lookup"><span data-stu-id="5d2b7-175">This allows the site to utilize IE11 rendering technologies</span></span>

    <meta http-equiv="X-UA-Compatible" content="IE=Edge" />

<span data-ttu-id="5d2b7-176">A configuração original é:</span><span class="sxs-lookup"><span data-stu-id="5d2b7-176">Original setting is:</span></span> 

    <meta http-equiv="X-UA-Compatible" content="IE=8" />


<span data-ttu-id="5d2b7-177">Esse é o motivo pelo qual o problema não era visto com outros navegadores, como o Chrome, o Firefox, etc.</span><span class="sxs-lookup"><span data-stu-id="5d2b7-177">This is the reason why the issue was not seen with other browsers like Chrome, Firefox etc.</span></span>



## <span data-ttu-id="5d2b7-178">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5d2b7-178">Related topics</span></span>


[<span data-ttu-id="5d2b7-179">Sobre o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="5d2b7-179">About MBAM 2.5</span></span>](about-mbam-25.md)

 

## <span data-ttu-id="5d2b7-180">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="5d2b7-180">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="5d2b7-181">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="5d2b7-181">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="5d2b7-182">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="5d2b7-182">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





