---
title: Notas de versão do MBAM 2.5
description: Notas de versão do MBAM 2.5
author: dansimp
ms.assetid: fcaf03e6-5e39-4771-af3c-a3cd468f3961
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4bcc17d6295b14a7f3276146d5630b869b94b7f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799581"
---
# <span data-ttu-id="ed07e-103">Notas de versão do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ed07e-103">Release Notes for MBAM 2.5</span></span>


<span data-ttu-id="ed07e-104">Para pesquisar essas notas de versão, pressione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="ed07e-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="ed07e-105">Leia estas notas de versão cuidadosamente antes de instalar o Microsoft BitLocker Administration and Monitoring (MBAM) 2,5.</span><span class="sxs-lookup"><span data-stu-id="ed07e-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM) 2.5.</span></span> <span data-ttu-id="ed07e-106">Estas notas da versão contêm informações necessárias para instalar com êxito o MBAM e podem conter informações que não estão disponíveis na documentação do produto.</span><span class="sxs-lookup"><span data-stu-id="ed07e-106">These release notes contain information that is required to successfully install MBAM and can contain information that is not available in the product documentation.</span></span> <span data-ttu-id="ed07e-107">Se estas notas de versão forem diferentes de outras documentações do MBAM 2,5, considere as alterações mais recentes a serem autoritativas.</span><span class="sxs-lookup"><span data-stu-id="ed07e-107">If these release notes differ from other MBAM 2.5 documentation, consider the latest change to be authoritative.</span></span> <span data-ttu-id="ed07e-108">Estas notas de versão substituem o conteúdo que está incluído neste produto.</span><span class="sxs-lookup"><span data-stu-id="ed07e-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-5-known-issues"></a> <span data-ttu-id="ed07e-109">MBAM 2,5 problemas conhecidos</span><span class="sxs-lookup"><span data-stu-id="ed07e-109">MBAM 2.5 known issues</span></span>


<span data-ttu-id="ed07e-110">Esta seção contém notas de versão do MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="ed07e-110">This section contains release notes for MBAM 2.5.</span></span>

### <span data-ttu-id="ed07e-111">Navegador da Web executado de forma não intencional como administrador</span><span class="sxs-lookup"><span data-stu-id="ed07e-111">Web browser unintentionally run as administrator</span></span>

<span data-ttu-id="ed07e-112">Os links de ajuda na ferramenta de configuração do MBAM Server podem fazer com que as janelas do navegador sejam abertas com direitos de administrador.</span><span class="sxs-lookup"><span data-stu-id="ed07e-112">Help links in the MBAM Server Configuration tool can cause browser windows to open with administrator rights.</span></span>

<span data-ttu-id="ed07e-113">**Solução alternativa:** Habilitar a configuração de segurança reforçada do Internet Explorer (IESC) ou fechar o navegador da Web antes de navegar para outros sites.</span><span class="sxs-lookup"><span data-stu-id="ed07e-113">**Workaround:** Enable Internet Explorer Enhanced Security Configuration (IESC) or close your web browser before navigating to other sites.</span></span>

<span data-ttu-id="ed07e-114">**Observação**  Isso foi corrigido no MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="ed07e-114">**Note** This is fixed in MBAM 2.5 SP1.</span></span>

 

### <a href="" id="-------------mbam-reports-as-noncompliant-a-client-encrypted-with-aes-256-bit-encryption-keys-and-diffuser"></a> <span data-ttu-id="ed07e-115">MBAM relatórios como não compatíveis um cliente criptografado com chaves de criptografia AES de 256 bits e difusor</span><span class="sxs-lookup"><span data-stu-id="ed07e-115">MBAM reports as noncompliant a client encrypted with AES 256-bit encryption keys and Diffuser</span></span>

<span data-ttu-id="ed07e-116">Se um computador tiver o cliente do MBAM 2,5 instalado e for criptografado usando o AES de 256 bits com força de codificação do difusor, o cliente MBAM será relatado como não compatível nos relatórios de conformidade do MBAM.</span><span class="sxs-lookup"><span data-stu-id="ed07e-116">If a computer has the MBAM 2.5 client installed and is encrypted by using the AES 256-bit with Diffuser cipher strength, the MBAM client is reported as noncompliant in the MBAM compliance reports.</span></span>

<span data-ttu-id="ed07e-117">**Solução alternativa:** Instale o hotfix em [KB2975636](https://go.microsoft.com/fwlink/?LinkId=511972).</span><span class="sxs-lookup"><span data-stu-id="ed07e-117">**Workaround:** Install the hotfix at [KB2975636](https://go.microsoft.com/fwlink/?LinkId=511972).</span></span>

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> <span data-ttu-id="ed07e-118">O MBAM não criptografa um volume e informa um erro se você definir um protetor TPM + PIN em um dispositivo tablet</span><span class="sxs-lookup"><span data-stu-id="ed07e-118">MBAM fails to encrypt a volume and reports an error if you set a TPM + PIN protector on a tablet device</span></span>

<span data-ttu-id="ed07e-119">Se os usuários finais tentarem definir um protetor TPM + PIN em um dispositivo tablet, o MBAM não criptografará, e ele reportará um erro.</span><span class="sxs-lookup"><span data-stu-id="ed07e-119">If end users try to set a TPM + PIN protector on a tablet device, MBAM fails to encrypt, and it reports an error.</span></span> <span data-ttu-id="ed07e-120">Esse problema ocorre porque os dispositivos Tablet não têm um teclado de ambiente de pré-inicialização.</span><span class="sxs-lookup"><span data-stu-id="ed07e-120">This issue occurs because tablet devices do not have a pre-boot environment keyboard.</span></span>

<span data-ttu-id="ed07e-121">**Solução alternativa:** Habilite o **uso da autenticação do BitLocker exigindo a entrada do teclado de pré-inicialização na configuração da política de grupo do tablets** .</span><span class="sxs-lookup"><span data-stu-id="ed07e-121">**Workaround:** Enable the **Enable use of BitLocker authentication requiring preboot keyboard input on tablets** Group Policy setting.</span></span> <span data-ttu-id="ed07e-122">Essa configuração é uma configuração de política de grupo do BitLocker e não está disponível nos modelos de política de grupo do MBAM.</span><span class="sxs-lookup"><span data-stu-id="ed07e-122">This setting is a BitLocker Group Policy setting and is not available in the MBAM Group Policy Templates.</span></span>

### <span data-ttu-id="ed07e-123">O nome UPN do usuário é necessário para todas as contas de serviço</span><span class="sxs-lookup"><span data-stu-id="ed07e-123">User principal name is required for all service accounts</span></span>

<span data-ttu-id="ed07e-124">Um nome UPN deve ser definido para todas as contas de serviço no MBAM.</span><span class="sxs-lookup"><span data-stu-id="ed07e-124">A user principal name (UPN) must be set for all service accounts in MBAM.</span></span> <span data-ttu-id="ed07e-125">Se você não conseguir criar um UPN para uma conta, uma mensagem de erro aparecerá durante o processo de configuração para indicar que o usuário ou grupo não foi encontrado no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ed07e-125">If you fail to create a UPN for an account, an error message appears during the configuration process to indicate that the user or group could not be found in Active Directory.</span></span>

<span data-ttu-id="ed07e-126">**Solução alternativa:** Adicione o UPN à conta de serviço.</span><span class="sxs-lookup"><span data-stu-id="ed07e-126">**Workaround:** Add the UPN to the service account.</span></span>

### <span data-ttu-id="ed07e-127">O portal de autoatendimento requer configuração adicional se os computadores cliente não puderem acessar a rede de distribuição de conteúdo do Microsoft Ajax</span><span class="sxs-lookup"><span data-stu-id="ed07e-127">Self-Service Portal requires additional configuration if client computers cannot access Microsoft Ajax Content Delivery Network</span></span>

<span data-ttu-id="ed07e-128">Se seus computadores cliente não tiverem acesso à rede de distribuição de conteúdo (CDN) do Microsoft Ajax, que fornece ao portal de autoatendimento o acesso necessário a certos arquivos JavaScript, você deve configurar o portal de autoatendimento para fazer referência aos arquivos JavaScript a partir de uma fonte acessível.</span><span class="sxs-lookup"><span data-stu-id="ed07e-128">If your client computers do not have access to the Microsoft Ajax Content Delivery Network (CDN), which gives the Self-Service Portal the access that it requires to certain JavaScript files, you must configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span> <span data-ttu-id="ed07e-129">Se você não configurar o portal de autoatendimento quando os computadores cliente não puderem acessar a CDN, somente o nome da empresa e a conta na qual você fez logon será exibido.</span><span class="sxs-lookup"><span data-stu-id="ed07e-129">If you don’t configure the Self-Service Portal when client computers cannot access CDN, only the company name and the account under which you logged on is displayed.</span></span> <span data-ttu-id="ed07e-130">Nenhuma mensagem de erro será exibida.</span><span class="sxs-lookup"><span data-stu-id="ed07e-130">No error message appears.</span></span>

<span data-ttu-id="ed07e-131">**Solução alternativa:** Instale o MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="ed07e-131">**Workaround:** Install MBAM 2.5 SP1.</span></span> <span data-ttu-id="ed07e-132">ou configure o portal de autoatendimento seguindo estas instruções: [como configurar o portal de autoatendimento quando os computadores cliente não conseguem acessar a rede de distribuição de conteúdo da Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span><span class="sxs-lookup"><span data-stu-id="ed07e-132">or configure the Self-Service Portal by following these instructions: [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span></span>

### <span data-ttu-id="ed07e-133">O portal de autoatendimento e o site de administração e monitoramento não abrem após a atualização do IIS para o .NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="ed07e-133">Self-Service Portal and the Administration and Monitoring Website do not open after you upgrade IIS to .NET Framework 4.5</span></span>

<span data-ttu-id="ed07e-134">Quando você atualiza os serviços de informações da Internet (IIS) para o Microsoft .NET Framework 4,5, o portal de autoatendimento e o site de administração e monitoramento não abrem.</span><span class="sxs-lookup"><span data-stu-id="ed07e-134">When you upgrade Internet Information Services (IIS) to the Microsoft .NET Framework 4.5, the Self-Service Portal and the Administration and Monitoring Website do not open.</span></span>

<span data-ttu-id="ed07e-135">**Solução alternativa:** Veja a mensagem de erro do artigo [depois de instalar o .NET Framework 4,0: "não foi possível carregar o tipo ' System. ServiceModel. Activation. HttpModule '](https://go.microsoft.com/fwlink/?LinkId=393568).</span><span class="sxs-lookup"><span data-stu-id="ed07e-135">**Workaround:** See the article [Error message after you install the .NET Framework 4.0: "Could not load type 'System.ServiceModel.Activation.HttpModule'](https://go.microsoft.com/fwlink/?LinkId=393568).</span></span>

### <span data-ttu-id="ed07e-136">Site de administração e monitoramento exibe uma mensagem de erro "não é possível encontrar o relatório" quando os relatórios não estão configurados</span><span class="sxs-lookup"><span data-stu-id="ed07e-136">Administration and Monitoring Website displays a "Report cannot be found" error message when Reports are not configured</span></span>

<span data-ttu-id="ed07e-137">Se você configurar o site de administração e monitoramento e, em seguida, tentar exibir um relatório sem configurar o recurso relatórios primeiro, uma mensagem de erro indicará que o relatório não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="ed07e-137">If you configure the Administration and Monitoring Website and then try to view a report without configuring the Reports feature first, an error message indicates that the report cannot be found.</span></span>

<span data-ttu-id="ed07e-138">**Solução alternativa:** Configure o recurso relatórios antes de configurar os aplicativos Web.</span><span class="sxs-lookup"><span data-stu-id="ed07e-138">**Workaround:** Configure the Reports feature before you configure the web applications.</span></span>

### <span data-ttu-id="ed07e-139">Relatórios no site de administração e monitoramento exibirão um aviso se a SSL não estiver configurada no SSRS</span><span class="sxs-lookup"><span data-stu-id="ed07e-139">Reports in the Administration and Monitoring Website display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="ed07e-140">Se o SSRS (SQL Server Reporting Services) não tiver sido configurado para usar SSL (Secure Socket Layer), a URL do recurso de relatórios será definida como HTTP em vez de HTTPS quando você configurar o servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="ed07e-140">If SQL Server Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the Reports feature will be set to HTTP instead of to HTTPS when you configure the MBAM Server.</span></span> <span data-ttu-id="ed07e-141">Se, em seguida, você abrir o site de administração e monitoramento e selecionar um relatório, a seguinte mensagem de erro será exibida: "somente conteúdo seguro é exibido".</span><span class="sxs-lookup"><span data-stu-id="ed07e-141">If you then open the Administration and Monitoring Website and select a report, the following error message appears: "Only Secure Content is Displayed."</span></span>

<span data-ttu-id="ed07e-142">**Solução alternativa:** Para mostrar o relatório, clique em **mostrar todo o conteúdo**.</span><span class="sxs-lookup"><span data-stu-id="ed07e-142">**Workaround:** To show the report, click **Show All Content**.</span></span> <span data-ttu-id="ed07e-143">Para corrigir esse problema, vá para o computador do MBAM em que o SQL Server Reporting Services está instalado, execute o **Gerenciador de configuração do Reporting Services**e clique em **URL do serviço Web**.</span><span class="sxs-lookup"><span data-stu-id="ed07e-143">To correct this issue, go to the MBAM computer where SQL Server Reporting Services is installed, run **Reporting Services Configuration Manager**, and then click **Web Service URL**.</span></span> <span data-ttu-id="ed07e-144">Selecione o certificado SSL apropriado para o servidor, insira a porta SSL apropriada (a porta padrão é 443) e, em seguida, clique em **aplicar**.</span><span class="sxs-lookup"><span data-stu-id="ed07e-144">Select the appropriate SSL certificate for the server, enter the appropriate SSL port (the default port is 443), and then click **Apply**.</span></span>

### <span data-ttu-id="ed07e-145">Clicar em "retornar" no relatório de Resumo de conformidade do BitLocker pode gerar um erro</span><span class="sxs-lookup"><span data-stu-id="ed07e-145">Clicking "Back" in the BitLocker Compliance Summary report might throw an error</span></span>

<span data-ttu-id="ed07e-146">Se você fizer buscas detalhadas em um relatório de Resumo de conformidade do BitLocker e, em seguida, clicar no link **retomar** no relatório SSRS, um erro poderá ser acionado.</span><span class="sxs-lookup"><span data-stu-id="ed07e-146">If you drill down into a BitLocker Compliance Summary report, and then click the **Back** link in the SSRS report, an error might be thrown.</span></span>

<span data-ttu-id="ed07e-147">**Solução alternativa:** Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed07e-147">**Workaround:** None.</span></span>

### <span data-ttu-id="ed07e-148">O espaço usado apenas a criptografia não funciona corretamente</span><span class="sxs-lookup"><span data-stu-id="ed07e-148">Used Space Only Encryption does not work correctly</span></span>

<span data-ttu-id="ed07e-149">Se você criptografar um computador pela primeira vez após a instalação do cliente do MBAM e tiver configurado uma configuração de política de grupo para implementar a criptografia somente espaço usado, o MBAM criptografará erroneamente o disco inteiro, em vez de criptografar somente o espaço usado pelo disco.</span><span class="sxs-lookup"><span data-stu-id="ed07e-149">If you encrypt a computer for the first time after you install the MBAM Client, and you have configured a Group Policy setting to implement Used Space Only encryption, MBAM erroneously encrypts the entire disk instead of encrypting only the disk’s used space.</span></span> <span data-ttu-id="ed07e-150">Se um computador já está criptografado com espaço usado apenas quando você instala o cliente MBAM e configurou a mesma configuração de política de grupo, MBAM informa que a unidade está criptografada corretamente e não tenta criptografar novamente a unidade.</span><span class="sxs-lookup"><span data-stu-id="ed07e-150">If a computer is already encrypted with Used Space Only when you install the MBAM Client, and you have configured the same Group Policy setting, MBAM reports that the drive is encrypted correctly, and does not try to re-encrypt the drive.</span></span>

<span data-ttu-id="ed07e-151">**Solução alternativa:** Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed07e-151">**Workaround:** None.</span></span>

### <span data-ttu-id="ed07e-152">O nível de codificação é exibido incorretamente no relatório de conformidade do computador BitLocker</span><span class="sxs-lookup"><span data-stu-id="ed07e-152">Cipher strength displays incorrectly on the BitLocker Computer Compliance report</span></span>

<span data-ttu-id="ed07e-153">Se você não definir um nível de codificação específico no objeto **escolher método de criptografia de unidade e nível de codificação de codificação** , o relatório de conformidade do computador BitLocker na topologia de integração do Configuration Manager sempre exibirá "desconhecido" para o nível de codificação, mesmo quando a força de codificação usar o padrão de criptografia de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="ed07e-153">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the BitLocker Computer Compliance report in the Configuration Manager Integration topology always displays "unknown" for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="ed07e-154">O relatório exibe a intensidade de codificação correta se você definir um nível de codificação específico no objeto de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="ed07e-154">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="ed07e-155">**Solução alternativa:** Defina sempre um nível de codificação específico no objeto **escolher o método de criptografia de unidade e** o objeto de política de grupo de força de codificação.</span><span class="sxs-lookup"><span data-stu-id="ed07e-155">**Workaround:** Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="ed07e-156">A distribuição do status de conformidade por tipo de drive exibe dados antigos após a atualização dos itens de configuração</span><span class="sxs-lookup"><span data-stu-id="ed07e-156">Compliance Status Distribution by Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="ed07e-157">Depois de atualizar os itens de configuração do MBAM no SystemCenter2012 ConfigurationManager, o gráfico de distribuição de status de distribuição por tipo de unidade no painel de conformidade do BitLocker Enterprise mostra os dados que se baseiam em informações de versões antigas dos itens de configuração.</span><span class="sxs-lookup"><span data-stu-id="ed07e-157">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="ed07e-158">**Solução alternativa:** Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed07e-158">**Workaround:** None.</span></span> <span data-ttu-id="ed07e-159">Não há suporte para modificação dos itens de configuração do MBAM, e o relatório pode não aparecer como esperado.</span><span class="sxs-lookup"><span data-stu-id="ed07e-159">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="ed07e-160">A configuração de segurança reforçada pode fazer com que os relatórios exibam uma mensagem de erro incorretamente</span><span class="sxs-lookup"><span data-stu-id="ed07e-160">Enhanced Security Configuration might cause reports to display an error message incorrectly</span></span>

<span data-ttu-id="ed07e-161">Se a configuração de segurança reforçada (ESC) do Internet Explorer estiver ativada, uma mensagem de erro "acesso negado" poderá aparecer quando você tentar exibir relatórios no servidor do MBAM.</span><span class="sxs-lookup"><span data-stu-id="ed07e-161">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an "Access Denied" error message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="ed07e-162">Por padrão, a tecla ESC está ativada para proteger o servidor, diminuindo a exposição do servidor a possíveis ataques que podem ocorrer por meio de conteúdo da Web e scripts de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ed07e-162">By default, ESC is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="ed07e-163">**Solução alternativa:** Se a mensagem de erro "acesso negado" for exibida quando você tentar exibir relatórios no servidor do MBAM, você pode definir um objeto de política de grupo ou alterar o padrão manualmente na sua imagem para desativar a configuração de segurança reforçada.</span><span class="sxs-lookup"><span data-stu-id="ed07e-163">**Workaround:** If the "Access Denied" error message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="ed07e-164">Você também pode exibir os relatórios de outro computador em que a ESC não está habilitado.</span><span class="sxs-lookup"><span data-stu-id="ed07e-164">You can also alternatively view the reports from another computer on which ESC is not enabled.</span></span>

## <a href="" id="hotfixes-and-knowledge-base-articles-for-mbam-2-5-"></a><span data-ttu-id="ed07e-165">Hotfixes e artigos da base de dados de conhecimento da MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="ed07e-165">Hotfixes and Knowledge Base articles for MBAM 2.5</span></span>


<span data-ttu-id="ed07e-166">Esta tabela lista os hotfixes e artigos da KB para o MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="ed07e-166">This table lists the hotfixes and KB articles for MBAM 2.5.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="ed07e-167">Artigo do KB</span><span class="sxs-lookup"><span data-stu-id="ed07e-167">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="ed07e-168">Title</span><span class="sxs-lookup"><span data-stu-id="ed07e-168">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="ed07e-169">Link</span><span class="sxs-lookup"><span data-stu-id="ed07e-169">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed07e-170">2975636</span><span class="sxs-lookup"><span data-stu-id="ed07e-170">2975636</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed07e-171">Pacote de hotfix 1 para administração e monitoramento do Microsoft BitLocker 2,5</span><span class="sxs-lookup"><span data-stu-id="ed07e-171">Hotfix Package 1 for Microsoft BitLocker Administration and Monitoring 2.5</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975636/EN-US" data-raw-source="[support.microsoft.com/kb/2975636/EN-US](https://support.microsoft.com/kb/2975636/EN-US)"><span data-ttu-id="ed07e-172">support.microsoft.com/kb/2975636/EN-US</span><span class="sxs-lookup"><span data-stu-id="ed07e-172">support.microsoft.com/kb/2975636/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ed07e-173">3015477</span><span class="sxs-lookup"><span data-stu-id="ed07e-173">3015477</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed07e-174">Pacote de hotfix 2 para administração e monitoramento de BitLocker 2,5</span><span class="sxs-lookup"><span data-stu-id="ed07e-174">Hotfix Package 2 for BitLocker Administration and Monitoring 2.5</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3015477" data-raw-source="[support.microsoft.com/kb/3015477](https://support.microsoft.com/kb/3015477)"><span data-ttu-id="ed07e-175">support.microsoft.com/kb/3015477</span><span class="sxs-lookup"><span data-stu-id="ed07e-175">support.microsoft.com/kb/3015477</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed07e-176">3011022</span><span class="sxs-lookup"><span data-stu-id="ed07e-176">3011022</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed07e-177">A instalação do MBAM 2,5 ou o relatório do Configuration Manager falha se o nome da instância do SSRS contiver um sublinhado</span><span class="sxs-lookup"><span data-stu-id="ed07e-177">MBAM 2.5 installation or Configuration Manager reporting fails if the name of SSRS instance contains an underscore</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3011022/EN-US" data-raw-source="[support.microsoft.com/kb/3011022/EN-US](https://support.microsoft.com/kb/3011022/EN-US)"><span data-ttu-id="ed07e-178">support.microsoft.com/kb/3011022/EN-US</span><span class="sxs-lookup"><span data-stu-id="ed07e-178">support.microsoft.com/kb/3011022/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ed07e-179">2756402</span><span class="sxs-lookup"><span data-stu-id="ed07e-179">2756402</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed07e-180">O cliente MBAM falharia com a ID de evento 4 e o código de erro 0x8004100E na descrição do evento</span><span class="sxs-lookup"><span data-stu-id="ed07e-180">MBAM client would fail with Event ID 4 and error code 0x8004100E in the Event description</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)"><span data-ttu-id="ed07e-181">support.microsoft.com/kb/2756402/EN-US</span><span class="sxs-lookup"><span data-stu-id="ed07e-181">support.microsoft.com/kb/2756402/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed07e-182">2639518</span><span class="sxs-lookup"><span data-stu-id="ed07e-182">2639518</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed07e-183">Erro ao abrir relatórios corporativos ou de conformidade de computador no MBAM</span><span class="sxs-lookup"><span data-stu-id="ed07e-183">Error opening Enterprise or Computer Compliance Reports in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)"><span data-ttu-id="ed07e-184">support.microsoft.com/kb/2639518/EN-US</span><span class="sxs-lookup"><span data-stu-id="ed07e-184">support.microsoft.com/kb/2639518/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ed07e-185">2870842</span><span class="sxs-lookup"><span data-stu-id="ed07e-185">2870842</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed07e-186">A instalação do MBAM 2,0 falha durante o cenário de integração do Configuration Manager com o SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed07e-186">MBAM 2.0 Setup fails during Configuration Manager Integration Scenario with SQL Server 2008</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)"><span data-ttu-id="ed07e-187">support.microsoft.com/kb/2870842/EN-US</span><span class="sxs-lookup"><span data-stu-id="ed07e-187">support.microsoft.com/kb/2870842/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ed07e-188">2975472</span><span class="sxs-lookup"><span data-stu-id="ed07e-188">2975472</span></span></p></td>
<td align="left"><p><span data-ttu-id="ed07e-189">Deadlocks SQL quando muitos clientes MBAM se conectam ao banco de dados de recuperação do MBAM</span><span class="sxs-lookup"><span data-stu-id="ed07e-189">SQL deadlocks when many MBAM clients connect to the MBAM recovery database</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975472/EN-US" data-raw-source="[support.microsoft.com/kb/2975472/EN-US](https://support.microsoft.com/kb/2975472/EN-US)"><span data-ttu-id="ed07e-190">support.microsoft.com/kb/2975472/EN-US</span><span class="sxs-lookup"><span data-stu-id="ed07e-190">support.microsoft.com/kb/2975472/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="ed07e-191">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ed07e-191">Related topics</span></span>


[<span data-ttu-id="ed07e-192">Sobre o MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ed07e-192">About MBAM 2.5</span></span>](about-mbam-25.md)

 

## <span data-ttu-id="ed07e-193">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="ed07e-193">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="ed07e-194">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="ed07e-194">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="ed07e-195">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="ed07e-195">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





