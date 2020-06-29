---
title: Notas de versão do MBAM 2.0 SP1
description: Notas de versão do MBAM 2.0 SP1
author: dansimp
ms.assetid: b39002ba-33c6-45ec-9d1b-464327b60f5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 54a77fc7a493b36217ae2cdc875226b25fdc6e7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799701"
---
# <span data-ttu-id="21cc1-103">Notas de versão do MBAM 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="21cc1-103">Release Notes for MBAM 2.0 SP1</span></span>


<span data-ttu-id="21cc1-104">Para pesquisar essas notas de versão, pressione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="21cc1-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="21cc1-105">Leia estas notas de versão cuidadosamente antes de instalar o Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="21cc1-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1).</span></span> <span data-ttu-id="21cc1-106">Estas notas da versão contêm informações necessárias para instalar com êxito a administração do BitLocker e o monitoramento do 2,0 SP1, e eles contêm informações que não estão disponíveis na documentação do produto.</span><span class="sxs-lookup"><span data-stu-id="21cc1-106">These release notes contain information that is required to successfully install BitLocker Administration and Monitoring 2.0 SP1, and they contain information that is not available in the product documentation.</span></span> <span data-ttu-id="21cc1-107">Se houver uma diferença entre essas notas de versão e outras documentações do MBAM 2,0 SP1, a alteração mais recente deve ser considerada autorizada.</span><span class="sxs-lookup"><span data-stu-id="21cc1-107">If there is a difference between these release notes and other MBAM 2.0 SP1 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="21cc1-108">Estas notas de versão substituem o conteúdo que está incluído neste produto.</span><span class="sxs-lookup"><span data-stu-id="21cc1-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-0-sp1-known-issues"></a> <span data-ttu-id="21cc1-109">Problemas conhecidos do MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="21cc1-109">MBAM 2.0 SP1 known issues</span></span>


<span data-ttu-id="21cc1-110">Esta seção contém problemas conhecidos para o MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="21cc1-110">This section contains known issues for MBAM 2.0 SP1.</span></span>

### <span data-ttu-id="21cc1-111">A atualização do MBAM com a topologia integrada do Configuration Manager para o MBAM 2,0 SP1 requer a remoção manual de objetos do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="21cc1-111">Upgrade of MBAM with Configuration Manager Integrated topology to MBAM 2.0 SP1 requires manual removal of Configuration Manager objects</span></span>

<span data-ttu-id="21cc1-112">Se você estiver usando o MBAM com o Configuration Manager e quiser atualizar para o MBAM 2,0 SP1, será necessário remover manualmente todos os objetos do Configuration Manager que foram instalados no Configuration Manager como parte da instalação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="21cc1-112">If you are using MBAM with Configuration Manager, and you want to upgrade to MBAM 2.0 SP1, you must manually remove all of the Configuration Manager objects that were installed into Configuration Manager as a part of the MBAM installation.</span></span> <span data-ttu-id="21cc1-113">Os objetos que você deve remover manualmente são os relatórios do MBAM, a coleção MBAM Computers supported e a linha de base de configuração de proteção BitLocker e seus itens de configuração associados.</span><span class="sxs-lookup"><span data-stu-id="21cc1-113">The objects that you must manually remove are the MBAM reports, MBAM Supported Computers collection, and the BitLocker Protection Configuration Baseline and its associated configuration items.</span></span>

<span data-ttu-id="21cc1-114">**Solução alternativa**: atualize os objetos do Configuration Manager completando as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="21cc1-114">**Workaround**: Upgrade the Configuration Manager objects by completing the following steps:</span></span>

1.  <span data-ttu-id="21cc1-115">Faça backup dos dados de conformidade existentes para um arquivo externo, conforme descrito nas etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="21cc1-115">Back up existing compliance data to an external file, as described in the following steps.</span></span>

    <span data-ttu-id="21cc1-116">**Observação**  Todos os dados de conformidade do BitLocker existentes serão excluídos quando você excluir a linha de base existente no Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="21cc1-116">**Note** All existing BitLocker compliance data will be deleted when you delete the existing baseline in Configuration Manager.</span></span> <span data-ttu-id="21cc1-117">Os dados serão regenerados ao longo do tempo, mas é recomendável que você salve uma cópia dos dados em caso de precisar dos dados de conformidade para um computador específico antes que os dados de conformidade sejam gerados novamente.</span><span class="sxs-lookup"><span data-stu-id="21cc1-117">The data will be regenerated over time, but it is recommended that you save a copy of the data in case you need the compliance data for a particular computer before the compliance data has been regenerated.</span></span>

     

    1.  <span data-ttu-id="21cc1-118">Para salvar os dados de conformidade do BitLocker do histórico, abra o relatório de **detalhes de conformidade corporativa do BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="21cc1-118">To save historical BitLocker compliance data, open the **BitLocker Enterprise Compliance Details** Report.</span></span>

    2.  <span data-ttu-id="21cc1-119">Clique no ícone **salvar** no relatório e selecione **Excel**.</span><span class="sxs-lookup"><span data-stu-id="21cc1-119">Click the **Save** icon in the report and select **Excel**.</span></span>

        <span data-ttu-id="21cc1-120">O relatório salvo conterá dados como o nome do computador, o nome do domínio, o status de conformidade, isenção, usuários do dispositivo, detalhes do status de conformidade e data/hora do último contato.</span><span class="sxs-lookup"><span data-stu-id="21cc1-120">The saved report will contain data such as the computer name, domain name, compliance status, exemption, device users, compliance status details, and last contact date/time.</span></span> <span data-ttu-id="21cc1-121">Algumas informações, como informações detalhadas sobre o volume e nível de criptografia, não são salvas.</span><span class="sxs-lookup"><span data-stu-id="21cc1-121">Some information, such as detailed volume information and encryption strength, are not saved.</span></span>

2.  <span data-ttu-id="21cc1-122">Desinstale o **MBAM** do servidor usando o instalador do **MBAM** .</span><span class="sxs-lookup"><span data-stu-id="21cc1-122">Uninstall **MBAM** from the server by using the **MBAM** installer.</span></span>

3.  <span data-ttu-id="21cc1-123">Exclua manualmente os seguintes objetos do Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="21cc1-123">Manually delete the following objects from Configuration Manager:</span></span>

    -   <span data-ttu-id="21cc1-124">Conjunto de computadores com suporte MBAM</span><span class="sxs-lookup"><span data-stu-id="21cc1-124">MBAM Supported Computers collection</span></span>

    -   <span data-ttu-id="21cc1-125">Linha de base de proteção BitLocker</span><span class="sxs-lookup"><span data-stu-id="21cc1-125">BitLocker Protection baseline</span></span>

    -   <span data-ttu-id="21cc1-126">Item de configuração de proteção de unidade de sistema operacional BitLocker</span><span class="sxs-lookup"><span data-stu-id="21cc1-126">BitLocker Operating System Drive Protection configuration item</span></span>

    -   <span data-ttu-id="21cc1-127">Item de configuração proteção de unidades de dados fixas do BitLocker</span><span class="sxs-lookup"><span data-stu-id="21cc1-127">BitLocker Fixed Data Drives Protection configuration item</span></span>

4.  <span data-ttu-id="21cc1-128">Exclua manualmente a pasta de relatórios do MBAM no site do SQL Server Reporting Services do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="21cc1-128">Manually delete the MBAM Reports folder in the Configuration Manager SQL Server Reporting Services site.</span></span> <span data-ttu-id="21cc1-129">Para fazer isso:</span><span class="sxs-lookup"><span data-stu-id="21cc1-129">To do this:</span></span>

    1.  <span data-ttu-id="21cc1-130">Use o Internet Explorer para navegar até o ponto do Reporting Services, por exemplo, http:// &lt; yourcmserver &gt; /reports.</span><span class="sxs-lookup"><span data-stu-id="21cc1-130">Use Internet Explorer to browse to the reporting services point, for example, http://&lt;yourcmserver&gt;/reports.</span></span>

    2.  <span data-ttu-id="21cc1-131">Clique no link de código de site apropriado do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="21cc1-131">Click the appropriate Configuration Manager site code link.</span></span>

    3.  <span data-ttu-id="21cc1-132">Exclua a pasta MBAM.</span><span class="sxs-lookup"><span data-stu-id="21cc1-132">Delete the MBAM folder.</span></span>

5.  <span data-ttu-id="21cc1-133">Use o instalador do MBAM Server para reinstalar os objetos de integração do Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="21cc1-133">Use the MBAM Server installer to reinstall the Configuration Manager Integration objects.</span></span> <span data-ttu-id="21cc1-134">Os computadores cliente começarão a carregar dados de conformidade do BitLocker novamente ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="21cc1-134">The client computers will begin to upload BitLocker compliance data again over time.</span></span>

### <span data-ttu-id="21cc1-135">O botão enviar no portal de autoatendimento não funciona no Internet Explorer10</span><span class="sxs-lookup"><span data-stu-id="21cc1-135">Submit button on Self-Service Portal does not work in Internet Explorer10</span></span>

<span data-ttu-id="21cc1-136">Quando você usa o Internet Explorer10 para acessar o site de administração e monitoramento, o botão **Enviar** no website não funciona.</span><span class="sxs-lookup"><span data-stu-id="21cc1-136">When you use Internet Explorer10 to access the Administration and Monitoring Website, the **Submit** button on the website does not work.</span></span>

<span data-ttu-id="21cc1-137">**Solução alternativa**: no servidor em que você instalou o site de administração e monitoramento, instale o [hotfix para ASP.net arquivos de definição do navegador](https://go.microsoft.com/fwlink/?LinkId=317798).</span><span class="sxs-lookup"><span data-stu-id="21cc1-137">**Workaround**: On the server where you installed the Administration and Monitoring Website, install [Hotfix for ASP.NET browser definition files](https://go.microsoft.com/fwlink/?LinkId=317798).</span></span>

### <span data-ttu-id="21cc1-138">Não há suporte para nomes de domínio internacionais</span><span class="sxs-lookup"><span data-stu-id="21cc1-138">International domain names are not supported</span></span>

<span data-ttu-id="21cc1-139">MBAM 2,0 SP1 não é compatível com nomes de domínio internacionais.</span><span class="sxs-lookup"><span data-stu-id="21cc1-139">MBAM 2.0 SP1 does not support international domain names.</span></span>

<span data-ttu-id="21cc1-140">**Solução alternativa**: nenhum.</span><span class="sxs-lookup"><span data-stu-id="21cc1-140">**Workaround**: None.</span></span>

### <span data-ttu-id="21cc1-141">Relatórios no site de administração e monitoramento exibirão um aviso se a SSL não estiver configurada no SSRS</span><span class="sxs-lookup"><span data-stu-id="21cc1-141">Reports in the Administration and Monitoring website display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="21cc1-142">Se o SSRS Reporting Services (SSRS) não tiver sido configurado para usar SSL (Secure Socket Layer), a URL dos relatórios será definida como HTTP em vez de HTTPS quando você instalar o servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="21cc1-142">If SQLServer Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server.</span></span> <span data-ttu-id="21cc1-143">Se, em seguida, você navegar até o site de administração e monitoramento e selecionar um relatório, a seguinte mensagem será exibida: "somente conteúdo seguro é exibido".</span><span class="sxs-lookup"><span data-stu-id="21cc1-143">If you then browse to the Administration and Monitoring website and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span>

<span data-ttu-id="21cc1-144">**Solução alternativa**: para corrigir esse problema, configure o SSL no **Gerenciador de configuração do Reporting Services** no servidor do MBAM em que o SqlServer Reporting Services está instalado.</span><span class="sxs-lookup"><span data-stu-id="21cc1-144">**Workaround**: To correct this issue, configure SSL in **Reporting Services Configuration Manager** on the MBAM server where SQLServer Reporting Services is installed.</span></span> <span data-ttu-id="21cc1-145">Desinstale e reinstale o site do servidor de administração e monitoração.</span><span class="sxs-lookup"><span data-stu-id="21cc1-145">Uninstall and then reinstall the Administration and Monitoring Server website.</span></span>

### <span data-ttu-id="21cc1-146">Clicar em retornar no relatório de Resumo de conformidade pode criar um erro</span><span class="sxs-lookup"><span data-stu-id="21cc1-146">Clicking Back in the Compliance Summary report might create an error</span></span>

<span data-ttu-id="21cc1-147">Se você fizer buscas detalhadas em um relatório de Resumo de conformidade e, em seguida, clicar no link **retomar** no relatório SSRS, pode ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="21cc1-147">If you drill down into a Compliance Summary report, and then click the **Back** link in the SSRS report, an error might occur.</span></span>

<span data-ttu-id="21cc1-148">**Solução alternativa**: nenhum.</span><span class="sxs-lookup"><span data-stu-id="21cc1-148">**Workaround**: None.</span></span>

### <span data-ttu-id="21cc1-149">O espaço usado apenas a criptografia não funciona corretamente</span><span class="sxs-lookup"><span data-stu-id="21cc1-149">Used Space Only Encryption does not work correctly</span></span>

<span data-ttu-id="21cc1-150">Se você criptografar um computador pela primeira vez após a instalação do cliente do MBAM e tiver definido um objeto de política de grupo para implementar a criptografia somente espaço usado, o MBAM criptografará erroneamente o disco inteiro, em vez de criptografar somente o espaço usado pelo disco.</span><span class="sxs-lookup"><span data-stu-id="21cc1-150">If you encrypt a computer for the first time after you install the MBAM Client, and you have set a Group Policy Object to implement Used Space Only Encryption, MBAM erroneously encrypts the entire disk instead of encrypting only the disk’s used space.</span></span> <span data-ttu-id="21cc1-151">Se um computador já estiver criptografado com a criptografia somente espaço usado antes de instalar o cliente do MBAM, e você tiver definido o mesmo objeto de política de grupo de criptografia somente espaço usado, o MBAM reconhece a configuração e relata a criptografia corretamente nos relatórios de conformidade.</span><span class="sxs-lookup"><span data-stu-id="21cc1-151">If a computer is already encrypted with Used Space Only Encryption before you install the MBAM Client, and you have set the same Used Space Only Encryption Group Policy Object, MBAM recognizes the setting and reports the encryption correctly in the compliance reports.</span></span>

<span data-ttu-id="21cc1-152">**Solução alternativa**: nenhum.</span><span class="sxs-lookup"><span data-stu-id="21cc1-152">**Workaround**: None.</span></span>

### <span data-ttu-id="21cc1-153">O nível de codificação é exibido incorretamente no relatório de conformidade do computador</span><span class="sxs-lookup"><span data-stu-id="21cc1-153">Cipher strength displays incorrectly in the Computer Compliance report</span></span>

<span data-ttu-id="21cc1-154">Se você não definir um nível de codificação específico no **método escolher o método de criptografia de unidade e** o objeto de política de grupo de força de codificação, o relatório de conformidade do computador na topologia integrada do Configuration Manager sempre exibirá **desconhecido** para o nível de codificação, mesmo quando a força de codificação usar o padrão de criptografia de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="21cc1-154">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the Computer Compliance report in the Configuration Manager integrated topology always displays **Unknown** for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="21cc1-155">O relatório exibe a intensidade de codificação correta se você definir um nível de codificação específico no objeto de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="21cc1-155">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="21cc1-156">**Solução alternativa**: Defina sempre um nível de codificação específico no objeto **escolher método de criptografia de unidade e nível de codificação** .</span><span class="sxs-lookup"><span data-stu-id="21cc1-156">**Workaround**: Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="21cc1-157">A distribuição do status de conformidade por tipo de drive exibe dados antigos após a atualização dos itens de configuração</span><span class="sxs-lookup"><span data-stu-id="21cc1-157">Compliance Status Distribution By Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="21cc1-158">Depois de atualizar os itens de configuração do MBAM no SystemCenter2012 ConfigurationManager, o gráfico de distribuição de status de distribuição por tipo de unidade no painel de conformidade do BitLocker Enterprise mostra os dados que se baseiam em informações de versões antigas dos itens de configuração.</span><span class="sxs-lookup"><span data-stu-id="21cc1-158">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="21cc1-159">**Solução alternativa**: nenhum.</span><span class="sxs-lookup"><span data-stu-id="21cc1-159">**Workaround**: None.</span></span> <span data-ttu-id="21cc1-160">Não há suporte para modificação dos itens de configuração do MBAM, e o relatório pode não aparecer como esperado.</span><span class="sxs-lookup"><span data-stu-id="21cc1-160">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="21cc1-161">A configuração de segurança reforçada pode fazer com que os relatórios sejam exibidos incorretamente</span><span class="sxs-lookup"><span data-stu-id="21cc1-161">Enhanced Security Configuration may cause reports to display incorrectly</span></span>

<span data-ttu-id="21cc1-162">Se a configuração de segurança reforçada (ESC) do Internet Explorer estiver ativada, uma mensagem de **acesso negado** poderá ser exibida quando você tentar exibir relatórios no servidor do MBAM.</span><span class="sxs-lookup"><span data-stu-id="21cc1-162">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an **Access Denied** message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="21cc1-163">Por padrão, a configuração de segurança reforçada está ativada para proteger o servidor, diminuindo a exposição do servidor a possíveis ataques que podem ocorrer por meio de conteúdo da Web e scripts de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="21cc1-163">By default, Enhanced Security Configuration is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="21cc1-164">**Solução alternativa**: se a mensagem de **acesso negado** for exibida quando você tentar exibir relatórios no servidor do MBAM, você pode definir um objeto de política de grupo ou alterar o padrão manualmente na sua imagem para desativar a configuração de segurança reforçada.</span><span class="sxs-lookup"><span data-stu-id="21cc1-164">**Workaround**: If the **Access Denied** message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="21cc1-165">Você também pode exibir os relatórios de outro computador em que a configuração de segurança reforçada não está habilitada.</span><span class="sxs-lookup"><span data-stu-id="21cc1-165">You can also alternatively view the reports from another computer on which Enhanced Security Configuration is not enabled.</span></span>

### <a href="" id="-------------mbam-server-installation-fails-when-you-upgrade-from-sql-server-2008-to-sql-server-2012"></a> <span data-ttu-id="21cc1-166">A instalação do MBAM Server falha quando você atualiza do SQLServer2008 para o SQLServer2012</span><span class="sxs-lookup"><span data-stu-id="21cc1-166">MBAM Server installation fails when you upgrade from SQLServer2008 to SQLServer2012</span></span>

<span data-ttu-id="21cc1-167">Se você atualizar de SQLServer2008 para SQLServer2012 e, em seguida, tentar instalar o banco de dados de conformidade e auditoria ou o banco de dados de recuperação, a instalação falha e é revertida.</span><span class="sxs-lookup"><span data-stu-id="21cc1-167">If you upgrade from SQLServer2008 to SQLServer2012, and then try to install the Compliance and Audit Database or the Recovery Database, the installation fails and rolls back.</span></span> <span data-ttu-id="21cc1-168">A falha ocorre porque o arquivo de SQLCMD.exe necessário foi removido durante a atualização do SQLServer e não pode ser encontrado pelo instalador do MBAM.</span><span class="sxs-lookup"><span data-stu-id="21cc1-168">The failure occurs because the required SQLCMD.exe file was removed during the SQLServer upgrade, and it cannot be found by the MBAM installer.</span></span> <span data-ttu-id="21cc1-169">As linhas do arquivo de log MSI podem parecer semelhantes às seguintes:</span><span class="sxs-lookup"><span data-stu-id="21cc1-169">The MSI log file lines may look similar to the following:</span></span>

<span data-ttu-id="21cc1-170">RunDbInstallScript de recuperação banco de de recuperação: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript de recuperação de banco de arquivos: dbInstance-xxxxxx\\I01RunDbInstallScript recuperação banco de arquivos do BD: SQLscript-C:\\Arquivos Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript recuperação DB CA: dbName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript recuperação _Recovery BD CA: MBAM-defaultDataPath I01\\MSSQL\\DATA\\RunDbInstallScript de banco de defaultLogPath de recuperação:-K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\RunDbInstallScript recuperação do banco de scriptLogPath de recuperação:-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\Arquivos Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFilename = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript recuperação de banco de dados do: Iniciando para executar o banco de dados de recuperação instalar scriptRunDbInstallScript recuperação de banco de dados do banco de dados: sqlcmd o arquivo de log está localizado na C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript recuperação banco de dados exceção: instalar a ação personalizada do banco de dados de recuperação exceção de saída de linha de comando: o sistema não</span><span class="sxs-lookup"><span data-stu-id="21cc1-170">RunDbInstallScript Recovery Db CA: BinDir - E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery Db CA: dbInstance - xxxxxx\\I01RunDbInstallScript Recovery Db CA: sqlScript- C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery Db CA: dbName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultFileName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultDataPath- F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\RunDbInstallScript Recovery Db CA: defaultLogPath- K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\RunDbInstallScript Recovery Db CA: scriptLogPath - C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e -E -S xxxxxxx\\I01 -i "C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql" -v DatabaseName="MBAM\_Recovery\_and\_Hardware" DefaultFileName="MBAM\_Recovery\_and\_Hardware" DefaultDataPath="F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\" DefaultLogPath="K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\" -o "C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log"RunDbInstallScript Recovery Db CA:Starting to run the Recovery database install scriptRunDbInstallScript Recovery Db CA: Sqlcmd log file is located in C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript Recovery Db CA Exception: Install Recovery database Custom Action command line output Exception: The system cannot find the file specified</span></span>

<span data-ttu-id="21cc1-171">O Windows Installer do Windows Server está codificado para localizar o caminho do SQLCMD.exe examinando o valor da cadeia de caracteres de caminho no registro em HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup.</span><span class="sxs-lookup"><span data-stu-id="21cc1-171">The MBAM Server Windows Installer is hardcoded to find the SQLCMD.exe path by looking in the Path string value in the registry under HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup.</span></span> <span data-ttu-id="21cc1-172">A chave ainda está presente durante a migração de SQLServer2008 para SQLServer2012, mas o caminho referenciado pelo valor de dados não contém o arquivo SQLCMD.exe, porque o processo sqlupgrade removeu o arquivo.</span><span class="sxs-lookup"><span data-stu-id="21cc1-172">The key is still present during the migration from SQLServer2008 to SQLServer2012, but the path that is referenced by the data value does not contain the SQLCMD.exe file, because the SQLupgrade process removed the file.</span></span>

<span data-ttu-id="21cc1-173">**Solução alternativa**: renomeie temporariamente o valor da cadeia de caracteres de caminho HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup para o **caminho \ _old**e execute o Windows Installer no servidor MBAM novamente.</span><span class="sxs-lookup"><span data-stu-id="21cc1-173">**Workaround**: Temporarily rename the HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup path string value to **Path\_old**, and then run Windows Installer on the MBAM Server again.</span></span> <span data-ttu-id="21cc1-174">Quando a instalação for concluída com êxito e criar os bancos de dados no SQLServer2012, renomeie o **caminho \ _old** para **caminho**.</span><span class="sxs-lookup"><span data-stu-id="21cc1-174">When the installation completes successfully and creates the databases in SQLServer2012, rename **Path\_old** to **Path**.</span></span>

## <span data-ttu-id="21cc1-175">Hotfixes e artigos da base de dados de conhecimento para MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="21cc1-175">Hotfixes and Knowledge Base articles for MBAM 2.0 SP1</span></span>


<span data-ttu-id="21cc1-176">Esta seção contém hotfixes e artigos da KB para o MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="21cc1-176">This section contains hotfixes and KB articles for MBAM 2.0 SP1.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="21cc1-177">Artigo do KB</span><span class="sxs-lookup"><span data-stu-id="21cc1-177">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="21cc1-178">Title</span><span class="sxs-lookup"><span data-stu-id="21cc1-178">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="21cc1-179">Link</span><span class="sxs-lookup"><span data-stu-id="21cc1-179">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21cc1-180">2831166</span><span class="sxs-lookup"><span data-stu-id="21cc1-180">2831166</span></span></p></td>
<td align="left"><p><span data-ttu-id="21cc1-181">A instalação do Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 falha com os &quot; objetos cm do System Center já instalados&quot;</span><span class="sxs-lookup"><span data-stu-id="21cc1-181">Installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 fails with &quot;System Center CM Objects Already Installed&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)"><span data-ttu-id="21cc1-182">support.microsoft.com/kb/2831166/EN-US</span><span class="sxs-lookup"><span data-stu-id="21cc1-182">support.microsoft.com/kb/2831166/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21cc1-183">2870849</span><span class="sxs-lookup"><span data-stu-id="21cc1-183">2870849</span></span></p></td>
<td align="left"><p><span data-ttu-id="21cc1-184">Os usuários não podem recuperar a chave de recuperação do BitLocker usando o portal de autoatendimento do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="21cc1-184">Users cannot retrieve BitLocker Recovery key using MBAM2.0 Self Service Portal</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)"><span data-ttu-id="21cc1-185">support.microsoft.com/kb/2870849/EN-US</span><span class="sxs-lookup"><span data-stu-id="21cc1-185">support.microsoft.com/kb/2870849/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21cc1-186">2756402</span><span class="sxs-lookup"><span data-stu-id="21cc1-186">2756402</span></span></p></td>
<td align="left"><p><span data-ttu-id="21cc1-187">O cliente MBAM falharia com a ID de evento 4 e o código de erro 0x8004100E na descrição do evento</span><span class="sxs-lookup"><span data-stu-id="21cc1-187">MBAM client would fail with Event ID 4 and error code 0x8004100E in the Event description</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)"><span data-ttu-id="21cc1-188">support.microsoft.com/kb/2756402/EN-US</span><span class="sxs-lookup"><span data-stu-id="21cc1-188">support.microsoft.com/kb/2756402/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21cc1-189">2620287</span><span class="sxs-lookup"><span data-stu-id="21cc1-189">2620287</span></span></p></td>
<td align="left"><p><span data-ttu-id="21cc1-190">Mensagem de erro "erro de servidor no aplicativo"/Reports "" quando você clica na guia relatórios do MBAM</span><span class="sxs-lookup"><span data-stu-id="21cc1-190">Error Message “Server Error in ‘/Reports’ Application” When You Click Reports Tab in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)"><span data-ttu-id="21cc1-191">support.microsoft.com/kb/2620287/EN-US</span><span class="sxs-lookup"><span data-stu-id="21cc1-191">support.microsoft.com/kb/2620287/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21cc1-192">2639518</span><span class="sxs-lookup"><span data-stu-id="21cc1-192">2639518</span></span></p></td>
<td align="left"><p><span data-ttu-id="21cc1-193">Erro ao abrir relatórios corporativos ou de conformidade de computador no MBAM</span><span class="sxs-lookup"><span data-stu-id="21cc1-193">Error opening Enterprise or Computer Compliance Reports in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)"><span data-ttu-id="21cc1-194">support.microsoft.com/kb/2639518/EN-US</span><span class="sxs-lookup"><span data-stu-id="21cc1-194">support.microsoft.com/kb/2639518/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21cc1-195">2620269</span><span class="sxs-lookup"><span data-stu-id="21cc1-195">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="21cc1-196">MBAM relatório corporativo não está sendo atualizado</span><span class="sxs-lookup"><span data-stu-id="21cc1-196">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="21cc1-197">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="21cc1-197">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21cc1-198">2712461</span><span class="sxs-lookup"><span data-stu-id="21cc1-198">2712461</span></span></p></td>
<td align="left"><p><span data-ttu-id="21cc1-199">Não há suporte para a instalação do MBAM em um controlador de domínio</span><span class="sxs-lookup"><span data-stu-id="21cc1-199">Installing MBAM on a Domain Controller is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)"><span data-ttu-id="21cc1-200">support.microsoft.com/kb/2712461/EN-US</span><span class="sxs-lookup"><span data-stu-id="21cc1-200">support.microsoft.com/kb/2712461/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21cc1-201">2876732</span><span class="sxs-lookup"><span data-stu-id="21cc1-201">2876732</span></span></p></td>
<td align="left"><p><span data-ttu-id="21cc1-202">Você recebe o código de erro 0x80071a90 durante a configuração de integração do Gerenciador de configurações ou autônomas do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="21cc1-202">You receive error code 0x80071a90 during Standalone or Configuration Manager Integration setup of MBAM2.0</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)"><span data-ttu-id="21cc1-203">support.microsoft.com/kb/2876732/EN-US</span><span class="sxs-lookup"><span data-stu-id="21cc1-203">support.microsoft.com/kb/2876732/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21cc1-204">2754259</span><span class="sxs-lookup"><span data-stu-id="21cc1-204">2754259</span></span></p></td>
<td align="left"><p><span data-ttu-id="21cc1-205">MBAM e comunicações de rede seguras</span><span class="sxs-lookup"><span data-stu-id="21cc1-205">MBAM and Secure Network Communication</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)"><span data-ttu-id="21cc1-206">support.microsoft.com/kb/2754259/EN-US</span><span class="sxs-lookup"><span data-stu-id="21cc1-206">support.microsoft.com/kb/2754259/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21cc1-207">2870842</span><span class="sxs-lookup"><span data-stu-id="21cc1-207">2870842</span></span></p></td>
<td align="left"><p><span data-ttu-id="21cc1-208">A instalação do MBAM 2.0 falha durante o cenário de integração do Configuration Manager com o SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="21cc1-208">MBAM2.0 Setup fails during Configuration Manager Integration Scenario with SQL Server 2008</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)"><span data-ttu-id="21cc1-209">support.microsoft.com/kb/2870842/EN-US</span><span class="sxs-lookup"><span data-stu-id="21cc1-209">support.microsoft.com/kb/2870842/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21cc1-210">2668533</span><span class="sxs-lookup"><span data-stu-id="21cc1-210">2668533</span></span></p></td>
<td align="left"><p><span data-ttu-id="21cc1-211">A instalação do MBAM falha se o SSRS do SQL não estiver configurado corretamente</span><span class="sxs-lookup"><span data-stu-id="21cc1-211">MBAM Setup fails if SQL SSRS is not configured properly</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)"><span data-ttu-id="21cc1-212">support.microsoft.com/kb/2668533/EN-US</span><span class="sxs-lookup"><span data-stu-id="21cc1-212">support.microsoft.com/kb/2668533/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21cc1-213">2870847</span><span class="sxs-lookup"><span data-stu-id="21cc1-213">2870847</span></span></p></td>
<td align="left"><p><span data-ttu-id="21cc1-214">Falha na instalação do MBAM 2,0 com o &quot; erro na recuperação de configurações de função de servidor do Configuration Manager para&#39; função de ponto do &#39;Reporting Services&quot;</span><span class="sxs-lookup"><span data-stu-id="21cc1-214">MBAM 2.0 Setup fails with &quot;Error retrieving Configuration Manager Server role settings for &#39;Reporting Services Point&#39; role&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)"><span data-ttu-id="21cc1-215">support.microsoft.com/kb/2870847/EN-US</span><span class="sxs-lookup"><span data-stu-id="21cc1-215">support.microsoft.com/kb/2870847/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21cc1-216">2870839</span><span class="sxs-lookup"><span data-stu-id="21cc1-216">2870839</span></span></p></td>
<td align="left"><p><span data-ttu-id="21cc1-217">Os relatórios do MBAM 2.0 Enterprise não são atualizados na topologia autônoma do MBAM 2.0 devido à falha de CreateCache do trabalho do SQL</span><span class="sxs-lookup"><span data-stu-id="21cc1-217">MBAM2.0 Enterprise Reports are not refreshed in MBAM2.0 Standalone topology due to SQL job CreateCache failure</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)"><span data-ttu-id="21cc1-218">support.microsoft.com/kb/2870839/EN-US</span><span class="sxs-lookup"><span data-stu-id="21cc1-218">support.microsoft.com/kb/2870839/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21cc1-219">2620269</span><span class="sxs-lookup"><span data-stu-id="21cc1-219">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="21cc1-220">MBAM relatório corporativo não está sendo atualizado</span><span class="sxs-lookup"><span data-stu-id="21cc1-220">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="21cc1-221">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="21cc1-221">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="21cc1-222">2935997</span><span class="sxs-lookup"><span data-stu-id="21cc1-222">2935997</span></span></p></td>
<td align="left"><p><span data-ttu-id="21cc1-223">Os relatórios de conformidade de computadores com suporte MBAM inclui incorretamente produtos sem suporte</span><span class="sxs-lookup"><span data-stu-id="21cc1-223">MBAM Supported Computers compliance reporting incorrectly includes unsupported products</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)"><span data-ttu-id="21cc1-224">support.microsoft.com/kb/2935997/EN-US</span><span class="sxs-lookup"><span data-stu-id="21cc1-224">support.microsoft.com/kb/2935997/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="21cc1-225">2612822</span><span class="sxs-lookup"><span data-stu-id="21cc1-225">2612822</span></span></p></td>
<td align="left"><p><span data-ttu-id="21cc1-226">O registro do computador foi rejeitado no MBAM</span><span class="sxs-lookup"><span data-stu-id="21cc1-226">Computer Record is Rejected in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)"><span data-ttu-id="21cc1-227">support.microsoft.com/kb/2612822/EN-US</span><span class="sxs-lookup"><span data-stu-id="21cc1-227">support.microsoft.com/kb/2612822/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="21cc1-228">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="21cc1-228">Related topics</span></span>


[<span data-ttu-id="21cc1-229">Sobre o MBAM 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="21cc1-229">About MBAM 2.0 SP1</span></span>](about-mbam-20-sp1.md)

 

 





