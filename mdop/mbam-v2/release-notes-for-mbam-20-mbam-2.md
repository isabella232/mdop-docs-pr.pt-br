---
title: Notas de Versão do MBAM 2.0
description: Notas de Versão do MBAM 2.0
author: dansimp
ms.assetid: c3f16cf3-94f2-47ac-b3a4-3dc505c6a8dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2d5d3c7d539cf2828d28c1844321bc34ab7736ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799702"
---
# <span data-ttu-id="0f7eb-103">Notas de Versão do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="0f7eb-103">Release Notes for MBAM 2.0</span></span>


<span data-ttu-id="0f7eb-104">Para pesquisar essas notas de versão, pressione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="0f7eb-105">Leia estas notas de versão cuidadosamente antes de instalar o Microsoft BitLockerAdministration e Monitoring (MBAM) 2.0.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-105">Read these release notes thoroughly before you install Microsoft BitLockerAdministration and Monitoring(MBAM)2.0.</span></span> <span data-ttu-id="0f7eb-106">Estas notas da versão contêm informações que são necessárias para instalar o BitLockerAdministration e o Monitoring 2.0 com êxito e contêm informações que não estão disponíveis na documentação do produto.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-106">These release notes contain information that is required to successfully install BitLockerAdministration and Monitoring2.0 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="0f7eb-107">Se houver uma diferença entre essas notas de versão e outras documentações do MBAM 2.0, a alteração mais recente deve ser considerada autorizada.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-107">If there is a difference between these release notes and other MBAM2.0 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="0f7eb-108">Estas notas de versão substituem o conteúdo que está incluído neste produto.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-0-known-issues"></a> <span data-ttu-id="0f7eb-109">Problemas conhecidos do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="0f7eb-109">MBAM2.0 Known Issues</span></span>


<span data-ttu-id="0f7eb-110">Esta seção contém notas de versão do MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-110">This section contains release notes for MBAM2.0.</span></span>

### <span data-ttu-id="0f7eb-111">Campo nome do computador pode não aparecer nos relatórios de conformidade do computador BitLocker e conformidade corporativa do BitLocker ao executar o MBAM com o Microsoft System Center Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="0f7eb-111">Computer Name field may not appear in the BitLocker Computer Compliance and BitLocker Enterprise Compliance Details reports when you run MBAM with Microsoft System Center Configuration Manager 2007</span></span>

<span data-ttu-id="0f7eb-112">O campo nome do computador pode estar em branco nos relatórios de conformidade do computador BitLocker e conformidade corporativa do BitLocker quando você usa o MBAM com o Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-112">The Computer Name field may be blank in the BitLocker Computer Compliance and BitLocker Enterprise Compliance Details reports when you use MBAM with Configuration Manager 2007.</span></span>

<span data-ttu-id="0f7eb-113">SOLUÇÃO alternativa: nenhum.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-113">WORKAROUND: None.</span></span>

### <span data-ttu-id="0f7eb-114">O relatório de conformidade empresarial falha ao atualizar após a atualização da infraestrutura autônoma do MBAM Server</span><span class="sxs-lookup"><span data-stu-id="0f7eb-114">Enterprise Compliance Report fails to update after you upgrade the Stand-alone MBAM server infrastructure</span></span>

<span data-ttu-id="0f7eb-115">Se você estiver usando a topologia autônoma do MBAM e atualizar a infraestrutura do servidor da versão 1,0 para o 2,0, o relatório de conformidade empresarial falha ao atualizar.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-115">If you are using the MBAM Stand-alone topology, and you upgrade the server infrastructure from version 1.0 to 2.0, the Enterprise Compliance Report fails to update.</span></span>

<span data-ttu-id="0f7eb-116">SOLUÇÃO alternativa: após a atualização, execute o seguinte script no banco de dados de conformidade e auditoria:</span><span class="sxs-lookup"><span data-stu-id="0f7eb-116">WORKAROUND: After the upgrade, run the following script on the Compliance and Audit Database:</span></span>

```sql
-- =============================================
-- Script Template
-- =============================================

DECLARE @DatabaseName nvarchar(255);
SET @DatabaseName = DB_NAME()

USE msdb;

DECLARE @JobID BINARY(16)
SELECT @JobID = job_id
FROM msdb.dbo.sysjobs
WHERE (name = N'CreateCache')

if (@JobID IS NOT NULL)
BEGIN
    EXEC dbo.sp_delete_job
         @job_name = N'CreateCache';
END

EXEC dbo.sp_add_job
    @job_name = N'CreateCache',
    @enabled = 1;

EXEC dbo.sp_add_jobstep
     @job_name = N'CreateCache',
     @step_name = N'Copy Data',
     @subsystem = N'TSQL',
     @command = N'EXEC [ComplianceCore].UpdateCache',
     @database_name = @DatabaseName,
     @retry_attempts = 5,
     @retry_interval = 5;


EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule1am',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 010000,
     @active_end_time = 020000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule1am';

EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule7am',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 070000,
     @active_end_time = 080000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule7am';

EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule1pm',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 130000,
     @active_end_time = 140000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule1pm';

EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule7pm',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 190000,
     @active_end_time = 200000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule7pm';

EXEC dbo.sp_add_jobserver
     @job_name = N'CreateCache';
```

### <span data-ttu-id="0f7eb-117">Os relatórios no portal de suporte técnico exibirão um aviso se a SSL não estiver configurada no SSRS</span><span class="sxs-lookup"><span data-stu-id="0f7eb-117">Reports in the Help Desk Portal display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="0f7eb-118">Se o SSRS (SQL Server Reporting Services) não tiver sido configurado para usar SSL (Secure Socket Layer), a URL dos relatórios será definida como HTTP em vez de HTTPS quando você instalar o servidor MBAM.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-118">If SQL Server Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server.</span></span> <span data-ttu-id="0f7eb-119">Se, em seguida, você navegar até o portal de suporte técnico e selecionar um relatório, a seguinte mensagem será exibida: "somente conteúdo seguro é exibido".</span><span class="sxs-lookup"><span data-stu-id="0f7eb-119">If you then browse to the Help Desk Portal and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span>

<span data-ttu-id="0f7eb-120">SOLUÇÃO alternativa: para mostrar o relatório, clique em **mostrar todo o conteúdo**.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-120">WORKAROUND: To show the report, click **Show All Content**.</span></span> <span data-ttu-id="0f7eb-121">Para solucionar esse problema, vá para o computador do MBAM em que o SQL Server Reporting Services está instalado, execute o **Gerenciador de configuração do Reporting Services**e clique em **URL do serviço Web**.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-121">To address this issue, go to the MBAM computer where SQL Server Reporting Services is installed, run **Reporting Services Configuration Manager**, and then click **Web Service URL**.</span></span> <span data-ttu-id="0f7eb-122">Selecione o certificado SSL apropriado para o servidor, insira a porta SSL apropriada (a porta padrão é 443) e, em seguida, clique em **aplicar**.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-122">Select the appropriate SSL certificate for the server, enter the appropriate SSL port (the default port is 443), and then click **Apply**.</span></span>

### <span data-ttu-id="0f7eb-123">Não há suporte para instâncias não padrão do banco de dados do Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="0f7eb-123">Non-default instances of the Configuration Manager database are not supported</span></span>

<span data-ttu-id="0f7eb-124">MBAM procura apenas a instância padrão do banco de dados do Configuration Manager no Configuration Manager 2007 e SystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-124">MBAM looks only for the default instance of the Configuration Manager database in Configuration Manager 2007 and SystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="0f7eb-125">Se você usar uma instância não padrão, não será possível instalar o MBAM.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-125">If you use a non-default instance, you cannot install MBAM.</span></span>

<span data-ttu-id="0f7eb-126">SOLUÇÃO alternativa: nenhum.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-126">WORKAROUND: None.</span></span>

### <a href="" id="clicking--back--in-the-compliance-summary-report-might-throw-an-error"></a><span data-ttu-id="0f7eb-127">Clicar em "retornar" no relatório de Resumo de conformidade pode gerar um erro</span><span class="sxs-lookup"><span data-stu-id="0f7eb-127">Clicking “Back” in the Compliance Summary report might throw an error</span></span>

<span data-ttu-id="0f7eb-128">Se você fizer buscas detalhadas em um relatório de Resumo de conformidade e, em seguida, clicar no link **retomar** no relatório SSRS, um erro poderá ser acionado.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-128">If you drill down into a Compliance Summary report, and then click the **Back** link in the SSRS report, an error might be thrown.</span></span>

<span data-ttu-id="0f7eb-129">SOLUÇÃO alternativa: nenhum.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-129">WORKAROUND: None.</span></span>

### <span data-ttu-id="0f7eb-130">O espaço usado apenas a criptografia não funciona corretamente</span><span class="sxs-lookup"><span data-stu-id="0f7eb-130">Used Space Only Encryption does not work correctly</span></span>

<span data-ttu-id="0f7eb-131">Se você criptografar um computador pela primeira vez após a instalação do cliente do MBAM e tiver definido um objeto de política de grupo para implementar a criptografia somente espaço usado, o MBAM criptografará erroneamente o disco inteiro, em vez de criptografar somente o espaço usado pelo disco.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-131">If you encrypt a computer for the first time after you install the MBAM Client, and you have set a Group Policy Object to implement Used Space Only encryption, MBAM erroneously encrypts the entire disk instead of encrypting only the disk’s used space.</span></span> <span data-ttu-id="0f7eb-132">Se um computador já estiver criptografado quando você instalar o cliente do MBAM e tiver definido o mesmo objeto de política de grupo, a criptografia funcionará corretamente e criptografará apenas o espaço em disco usado no computador.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-132">If a computer is already encrypted when you install the MBAM Client, and you have set the same Group Policy Object, the encryption works correctly and encrypts only the used disk space on your computer.</span></span>

<span data-ttu-id="0f7eb-133">SOLUÇÃO alternativa: nenhum.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-133">WORKAROUND: None.</span></span>

### <span data-ttu-id="0f7eb-134">O nível de codificação é exibido incorretamente no relatório de conformidade do computador</span><span class="sxs-lookup"><span data-stu-id="0f7eb-134">Cipher strength displays incorrectly on the Computer Compliance report</span></span>

<span data-ttu-id="0f7eb-135">Se você não definir um nível de codificação específico no objeto **escolher método de criptografia de unidade e nível de codificação** , o relatório de conformidade do computador na topologia de integração do Configuration Manager sempre exibirá "desconhecido" para o nível de codificação, mesmo quando a força de codificação usar o padrão de criptografia de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-135">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the Computer Compliance report in the Configuration Manager Integration topology always displays “unknown” for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="0f7eb-136">O relatório exibe a intensidade de codificação correta se você definir um nível de codificação específico no objeto de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-136">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="0f7eb-137">SOLUÇÃO alternativa: Defina sempre um nível de codificação específico no objeto **escolher método de criptografia de unidade e nível de codificação** .</span><span class="sxs-lookup"><span data-stu-id="0f7eb-137">WORKAROUND: Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="0f7eb-138">A distribuição do status de conformidade por tipo de drive exibe dados antigos após a atualização dos itens de configuração</span><span class="sxs-lookup"><span data-stu-id="0f7eb-138">Compliance Status Distribution By Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="0f7eb-139">Depois de atualizar os itens de configuração do MBAM no SystemCenter2012 ConfigurationManager, o gráfico de distribuição de status de distribuição por tipo de unidade no painel de conformidade do BitLocker Enterprise mostra os dados que se baseiam em informações de versões antigas dos itens de configuração.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-139">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="0f7eb-140">SOLUÇÃO alternativa: nenhum.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-140">WORKAROUND: None.</span></span> <span data-ttu-id="0f7eb-141">Não há suporte para modificação dos itens de configuração do MBAM, e o relatório pode não aparecer como esperado.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-141">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="0f7eb-142">A configuração de segurança reforçada pode fazer com que os relatórios sejam exibidos incorretamente</span><span class="sxs-lookup"><span data-stu-id="0f7eb-142">Enhanced Security Configuration may cause reports to display incorrectly</span></span>

<span data-ttu-id="0f7eb-143">Se a configuração de segurança reforçada (ESC) do Internet Explorer estiver ativada, uma mensagem de "acesso negado" poderá aparecer quando você tentar exibir relatórios no servidor do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-143">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an “Access Denied” message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="0f7eb-144">Por padrão, a tecla ESC está ativada para proteger o servidor, diminuindo a exposição do servidor a possíveis ataques que podem ocorrer por meio de conteúdo da Web e scripts de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-144">By default, ESC is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="0f7eb-145">SOLUÇÃO alternativa: se a mensagem "acesso negado" for exibida quando você tentar exibir relatórios no servidor do MBAM, você pode definir um objeto de política de grupo ou alterar o padrão manualmente na sua imagem para desativar a configuração de segurança reforçada.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-145">WORKAROUND: If the “Access Denied” message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="0f7eb-146">Você também pode exibir os relatórios de outro computador em que a ESC não está habilitado.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-146">You can also alternatively view the reports from another computer on which ESC is not enabled.</span></span>

### <span data-ttu-id="0f7eb-147">A instalação do MBAM Server falha quando você atualiza do SQL Server 2008 para o SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="0f7eb-147">MBAM Server installation fails when you upgrade from SQL Server 2008 to SQL Server 2012</span></span>

<span data-ttu-id="0f7eb-148">Se você atualizar do SQL Server 2008 para o SQL Server 2012 e, em seguida, tentar instalar o banco de dados de conformidade e auditoria ou o banco de dados de recuperação, a instalação falha e é revertida.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-148">If you upgrade from SQL Server 2008 to SQL Server 2012, and then try to install the Compliance and Audit Database or the Recovery Database, the installation fails and rolls back.</span></span> <span data-ttu-id="0f7eb-149">A falha ocorre porque o arquivo de SQLCMD.exe necessário foi removido durante a atualização do SQL e não pode ser encontrado pelo instalador do MBAM.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-149">The failure occurs because the required SQLCMD.exe file was removed during the SQL upgrade and cannot be found by the MBAM installer.</span></span> <span data-ttu-id="0f7eb-150">As linhas do arquivo de log MSI podem parecer semelhantes às seguintes:</span><span class="sxs-lookup"><span data-stu-id="0f7eb-150">The MSI log file lines may look similar to the following:</span></span>

<span data-ttu-id="0f7eb-151">RunDbInstallScript de recuperação banco de de recuperação: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript de recuperação de banco de arquivos: dbInstance-xxxxxx\\I01RunDbInstallScript recuperação banco de arquivos do BD: SQLscript-C:\\Arquivos Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript recuperação DB CA: dbName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript recuperação _Recovery BD CA: MBAM-defaultDataPath I01\\MSSQL\\DATA\\RunDbInstallScript de banco de defaultLogPath de recuperação:-K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\RunDbInstallScript recuperação do banco de scriptLogPath de recuperação:-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\Arquivos Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFilename = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript recuperação de banco de dados do: Iniciando para executar o banco de dados de recuperação instalar scriptRunDbInstallScript recuperação de banco de dados do banco de dados: sqlcmd o arquivo de log está localizado na C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript recuperação banco de dados exceção: instalar a ação personalizada do banco de dados de recuperação exceção de saída de linha de comando: o sistema não</span><span class="sxs-lookup"><span data-stu-id="0f7eb-151">RunDbInstallScript Recovery Db CA: BinDir - E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery Db CA: dbInstance - xxxxxx\\I01RunDbInstallScript Recovery Db CA: sqlScript- C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery Db CA: dbName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultFileName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultDataPath- F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\RunDbInstallScript Recovery Db CA: defaultLogPath- K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\RunDbInstallScript Recovery Db CA: scriptLogPath - C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e -E -S xxxxxxx\\I01 -i "C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql" -v DatabaseName="MBAM\_Recovery\_and\_Hardware" DefaultFileName="MBAM\_Recovery\_and\_Hardware" DefaultDataPath="F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\" DefaultLogPath="K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\" -o "C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log"RunDbInstallScript Recovery Db CA:Starting to run the Recovery database install scriptRunDbInstallScript Recovery Db CA: Sqlcmd log file is located in C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript Recovery Db CA Exception: Install Recovery database Custom Action command line output Exception: The system cannot find the file specified</span></span>

<span data-ttu-id="0f7eb-152">O Windows Installer do Windows Server está codificado para localizar o caminho do SQLCMD.exe examinando o valor da cadeia de caracteres de caminho no registro em HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-152">The MBAM Server Windows Installer is hardcoded to find the SQLCMD.exe path by looking in the Path string value in the registry under HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup.</span></span> <span data-ttu-id="0f7eb-153">A chave ainda está presente durante a migração do SQL Server 2008 para o SQL Server 2012, mas o caminho referenciado pelo valor de dados não contém o arquivo SQLCMD.exe, porque o processo de atualização do SQL removeu o arquivo.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-153">The key is still present during the migration from SQL Server 2008 to SQL Server 2012, but the path that is referenced by the data value does not contain the SQLCMD.exe file, because the SQL upgrade process removed the file.</span></span>

<span data-ttu-id="0f7eb-154">SOLUÇÃO alternativa: renomeie temporariamente o valor da cadeia de caracteres de caminho HKLM\\Software\\Microsoft\\Microsoft do SQL Server\\100\\Tools\\ClientSetup para o **caminho \ _old**e execute novamente o Windows Installer do MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-154">WORKAROUND: Temporarily rename the HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup Path string value to **Path\_old**, and then re-run the MBAM Server Windows Installer.</span></span> <span data-ttu-id="0f7eb-155">Quando a instalação for concluída com êxito e criar os bancos de dados no SQL Server 2012, renomeie o **caminho \ _old** valor para **caminho**.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-155">When the installation completes successfully and creates the databases in SQL Server 2012, rename the **Path\_old** value to **Path**.</span></span>

## <span data-ttu-id="0f7eb-156">Hotfixes e artigos da base de dados de conhecimento da MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="0f7eb-156">Hotfixes and Knowledge Base articles for MBAM2.0</span></span>


<span data-ttu-id="0f7eb-157">Esta seção contém hotfixes e artigos da KB para o MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="0f7eb-157">This section contains hotfixes and KB articles for MBAM2.0.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="0f7eb-158">Artigo do KB</span><span class="sxs-lookup"><span data-stu-id="0f7eb-158">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="0f7eb-159">Title</span><span class="sxs-lookup"><span data-stu-id="0f7eb-159">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="0f7eb-160">Link</span><span class="sxs-lookup"><span data-stu-id="0f7eb-160">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0f7eb-161">2831166</span><span class="sxs-lookup"><span data-stu-id="0f7eb-161">2831166</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f7eb-162">A instalação do Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 falha com os &quot; objetos cm do System Center já instalados&quot;</span><span class="sxs-lookup"><span data-stu-id="0f7eb-162">Installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 fails with &quot;System Center CM Objects Already Installed&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)"><span data-ttu-id="0f7eb-163">support.microsoft.com/kb/2831166/EN-US</span><span class="sxs-lookup"><span data-stu-id="0f7eb-163">support.microsoft.com/kb/2831166/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0f7eb-164">2870849</span><span class="sxs-lookup"><span data-stu-id="0f7eb-164">2870849</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f7eb-165">Os usuários não podem recuperar a chave de recuperação do BitLocker usando o portal de autoatendimento do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="0f7eb-165">Users cannot retrieve BitLocker Recovery key using MBAM2.0 Self Service Portal</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)"><span data-ttu-id="0f7eb-166">support.microsoft.com/kb/2870849/EN-US</span><span class="sxs-lookup"><span data-stu-id="0f7eb-166">support.microsoft.com/kb/2870849/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0f7eb-167">2756402</span><span class="sxs-lookup"><span data-stu-id="0f7eb-167">2756402</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f7eb-168">O cliente MBAM falharia com a ID de evento 4 e o código de erro 0x8004100E na descrição do evento</span><span class="sxs-lookup"><span data-stu-id="0f7eb-168">MBAM client would fail with Event ID 4 and error code 0x8004100E in the Event description</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)"><span data-ttu-id="0f7eb-169">support.microsoft.com/kb/2756402/EN-US</span><span class="sxs-lookup"><span data-stu-id="0f7eb-169">support.microsoft.com/kb/2756402/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0f7eb-170">2620287</span><span class="sxs-lookup"><span data-stu-id="0f7eb-170">2620287</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f7eb-171">Mensagem de erro "erro de servidor no aplicativo"/Reports "" quando você clica na guia relatórios do MBAM</span><span class="sxs-lookup"><span data-stu-id="0f7eb-171">Error Message “Server Error in ‘/Reports’ Application” When You Click Reports Tab in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)"><span data-ttu-id="0f7eb-172">support.microsoft.com/kb/2620287/EN-US</span><span class="sxs-lookup"><span data-stu-id="0f7eb-172">support.microsoft.com/kb/2620287/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0f7eb-173">2639518</span><span class="sxs-lookup"><span data-stu-id="0f7eb-173">2639518</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f7eb-174">Erro ao abrir relatórios corporativos ou de conformidade de computador no MBAM</span><span class="sxs-lookup"><span data-stu-id="0f7eb-174">Error opening Enterprise or Computer Compliance Reports in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)"><span data-ttu-id="0f7eb-175">support.microsoft.com/kb/2639518/EN-US</span><span class="sxs-lookup"><span data-stu-id="0f7eb-175">support.microsoft.com/kb/2639518/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0f7eb-176">2620269</span><span class="sxs-lookup"><span data-stu-id="0f7eb-176">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f7eb-177">MBAM relatório corporativo não está sendo atualizado</span><span class="sxs-lookup"><span data-stu-id="0f7eb-177">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="0f7eb-178">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="0f7eb-178">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0f7eb-179">2712461</span><span class="sxs-lookup"><span data-stu-id="0f7eb-179">2712461</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f7eb-180">Não há suporte para a instalação do MBAM em um controlador de domínio</span><span class="sxs-lookup"><span data-stu-id="0f7eb-180">Installing MBAM on a Domain Controller is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)"><span data-ttu-id="0f7eb-181">support.microsoft.com/kb/2712461/EN-US</span><span class="sxs-lookup"><span data-stu-id="0f7eb-181">support.microsoft.com/kb/2712461/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0f7eb-182">2876732</span><span class="sxs-lookup"><span data-stu-id="0f7eb-182">2876732</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f7eb-183">Você recebe o código de erro 0x80071a90 durante a configuração de integração do Gerenciador de configurações ou autônomas do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="0f7eb-183">You receive error code 0x80071a90 during Standalone or Configuration Manager Integration setup of MBAM2.0</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)"><span data-ttu-id="0f7eb-184">support.microsoft.com/kb/2876732/EN-US</span><span class="sxs-lookup"><span data-stu-id="0f7eb-184">support.microsoft.com/kb/2876732/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0f7eb-185">2754259</span><span class="sxs-lookup"><span data-stu-id="0f7eb-185">2754259</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f7eb-186">MBAM e comunicações de rede seguras</span><span class="sxs-lookup"><span data-stu-id="0f7eb-186">MBAM and Secure Network Communication</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)"><span data-ttu-id="0f7eb-187">support.microsoft.com/kb/2754259/EN-US</span><span class="sxs-lookup"><span data-stu-id="0f7eb-187">support.microsoft.com/kb/2754259/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0f7eb-188">2870842</span><span class="sxs-lookup"><span data-stu-id="0f7eb-188">2870842</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f7eb-189">A instalação do MBAM 2.0 falha durante o cenário de integração do Configuration Manager com o SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f7eb-189">MBAM2.0 Setup fails during Configuration Manager Integration Scenario with SQL Server 2008</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)"><span data-ttu-id="0f7eb-190">support.microsoft.com/kb/2870842/EN-US</span><span class="sxs-lookup"><span data-stu-id="0f7eb-190">support.microsoft.com/kb/2870842/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0f7eb-191">2668533</span><span class="sxs-lookup"><span data-stu-id="0f7eb-191">2668533</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f7eb-192">A instalação do MBAM falha se o SSRS do SQL não estiver configurado corretamente</span><span class="sxs-lookup"><span data-stu-id="0f7eb-192">MBAM Setup fails if SQL SSRS is not configured properly</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)"><span data-ttu-id="0f7eb-193">support.microsoft.com/kb/2668533/EN-US</span><span class="sxs-lookup"><span data-stu-id="0f7eb-193">support.microsoft.com/kb/2668533/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0f7eb-194">2870847</span><span class="sxs-lookup"><span data-stu-id="0f7eb-194">2870847</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f7eb-195">Falha na instalação do MBAM 2,0 com o &quot; erro na recuperação de configurações de função de servidor do Configuration Manager para&#39; função de ponto do &#39;Reporting Services&quot;</span><span class="sxs-lookup"><span data-stu-id="0f7eb-195">MBAM 2.0 Setup fails with &quot;Error retrieving Configuration Manager Server role settings for &#39;Reporting Services Point&#39; role&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)"><span data-ttu-id="0f7eb-196">support.microsoft.com/kb/2870847/EN-US</span><span class="sxs-lookup"><span data-stu-id="0f7eb-196">support.microsoft.com/kb/2870847/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0f7eb-197">2870839</span><span class="sxs-lookup"><span data-stu-id="0f7eb-197">2870839</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f7eb-198">Os relatórios do MBAM 2.0 Enterprise não são atualizados na topologia autônoma do MBAM 2.0 devido à falha de CreateCache do trabalho do SQL</span><span class="sxs-lookup"><span data-stu-id="0f7eb-198">MBAM2.0 Enterprise Reports are not refreshed in MBAM2.0 Standalone topology due to SQL job CreateCache failure</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)"><span data-ttu-id="0f7eb-199">support.microsoft.com/kb/2870839/EN-US</span><span class="sxs-lookup"><span data-stu-id="0f7eb-199">support.microsoft.com/kb/2870839/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0f7eb-200">2620269</span><span class="sxs-lookup"><span data-stu-id="0f7eb-200">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f7eb-201">MBAM relatório corporativo não está sendo atualizado</span><span class="sxs-lookup"><span data-stu-id="0f7eb-201">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="0f7eb-202">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="0f7eb-202">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0f7eb-203">2935997</span><span class="sxs-lookup"><span data-stu-id="0f7eb-203">2935997</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f7eb-204">Os relatórios de conformidade de computadores com suporte MBAM inclui incorretamente produtos sem suporte</span><span class="sxs-lookup"><span data-stu-id="0f7eb-204">MBAM Supported Computers compliance reporting incorrectly includes unsupported products</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)"><span data-ttu-id="0f7eb-205">support.microsoft.com/kb/2935997/EN-US</span><span class="sxs-lookup"><span data-stu-id="0f7eb-205">support.microsoft.com/kb/2935997/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0f7eb-206">2612822</span><span class="sxs-lookup"><span data-stu-id="0f7eb-206">2612822</span></span></p></td>
<td align="left"><p><span data-ttu-id="0f7eb-207">O registro do computador foi rejeitado no MBAM</span><span class="sxs-lookup"><span data-stu-id="0f7eb-207">Computer Record is Rejected in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)"><span data-ttu-id="0f7eb-208">support.microsoft.com/kb/2612822/EN-US</span><span class="sxs-lookup"><span data-stu-id="0f7eb-208">support.microsoft.com/kb/2612822/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="0f7eb-209">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f7eb-209">Related topics</span></span>


[<span data-ttu-id="0f7eb-210">Sobre o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="0f7eb-210">About MBAM 2.0</span></span>](about-mbam-20-mbam-2.md)

 

 





