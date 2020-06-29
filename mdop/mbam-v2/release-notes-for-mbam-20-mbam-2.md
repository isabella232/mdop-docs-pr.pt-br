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
# Notas de Versão do MBAM 2.0


Para pesquisar essas notas de versão, pressione Ctrl + F.

Leia estas notas de versão cuidadosamente antes de instalar o Microsoft BitLockerAdministration e Monitoring (MBAM) 2.0. Estas notas da versão contêm informações que são necessárias para instalar o BitLockerAdministration e o Monitoring 2.0 com êxito e contêm informações que não estão disponíveis na documentação do produto. Se houver uma diferença entre essas notas de versão e outras documentações do MBAM 2.0, a alteração mais recente deve ser considerada autorizada. Estas notas de versão substituem o conteúdo que está incluído neste produto.

## <a href="" id="---------mbam-2-0-known-issues"></a> Problemas conhecidos do MBAM 2.0


Esta seção contém notas de versão do MBAM 2.0.

### Campo nome do computador pode não aparecer nos relatórios de conformidade do computador BitLocker e conformidade corporativa do BitLocker ao executar o MBAM com o Microsoft System Center Configuration Manager 2007

O campo nome do computador pode estar em branco nos relatórios de conformidade do computador BitLocker e conformidade corporativa do BitLocker quando você usa o MBAM com o Configuration Manager 2007.

SOLUÇÃO alternativa: nenhum.

### O relatório de conformidade empresarial falha ao atualizar após a atualização da infraestrutura autônoma do MBAM Server

Se você estiver usando a topologia autônoma do MBAM e atualizar a infraestrutura do servidor da versão 1,0 para o 2,0, o relatório de conformidade empresarial falha ao atualizar.

SOLUÇÃO alternativa: após a atualização, execute o seguinte script no banco de dados de conformidade e auditoria:

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

### Os relatórios no portal de suporte técnico exibirão um aviso se a SSL não estiver configurada no SSRS

Se o SSRS (SQL Server Reporting Services) não tiver sido configurado para usar SSL (Secure Socket Layer), a URL dos relatórios será definida como HTTP em vez de HTTPS quando você instalar o servidor MBAM. Se, em seguida, você navegar até o portal de suporte técnico e selecionar um relatório, a seguinte mensagem será exibida: "somente conteúdo seguro é exibido".

SOLUÇÃO alternativa: para mostrar o relatório, clique em **mostrar todo o conteúdo**. Para solucionar esse problema, vá para o computador do MBAM em que o SQL Server Reporting Services está instalado, execute o **Gerenciador de configuração do Reporting Services**e clique em **URL do serviço Web**. Selecione o certificado SSL apropriado para o servidor, insira a porta SSL apropriada (a porta padrão é 443) e, em seguida, clique em **aplicar**.

### Não há suporte para instâncias não padrão do banco de dados do Configuration Manager

MBAM procura apenas a instância padrão do banco de dados do Configuration Manager no Configuration Manager 2007 e SystemCenter2012 ConfigurationManager. Se você usar uma instância não padrão, não será possível instalar o MBAM.

SOLUÇÃO alternativa: nenhum.

### <a href="" id="clicking--back--in-the-compliance-summary-report-might-throw-an-error"></a>Clicar em "retornar" no relatório de Resumo de conformidade pode gerar um erro

Se você fizer buscas detalhadas em um relatório de Resumo de conformidade e, em seguida, clicar no link **retomar** no relatório SSRS, um erro poderá ser acionado.

SOLUÇÃO alternativa: nenhum.

### O espaço usado apenas a criptografia não funciona corretamente

Se você criptografar um computador pela primeira vez após a instalação do cliente do MBAM e tiver definido um objeto de política de grupo para implementar a criptografia somente espaço usado, o MBAM criptografará erroneamente o disco inteiro, em vez de criptografar somente o espaço usado pelo disco. Se um computador já estiver criptografado quando você instalar o cliente do MBAM e tiver definido o mesmo objeto de política de grupo, a criptografia funcionará corretamente e criptografará apenas o espaço em disco usado no computador.

SOLUÇÃO alternativa: nenhum.

### O nível de codificação é exibido incorretamente no relatório de conformidade do computador

Se você não definir um nível de codificação específico no objeto **escolher método de criptografia de unidade e nível de codificação** , o relatório de conformidade do computador na topologia de integração do Configuration Manager sempre exibirá "desconhecido" para o nível de codificação, mesmo quando a força de codificação usar o padrão de criptografia de 128 bits. O relatório exibe a intensidade de codificação correta se você definir um nível de codificação específico no objeto de política de grupo.

SOLUÇÃO alternativa: Defina sempre um nível de codificação específico no objeto **escolher método de criptografia de unidade e nível de codificação** .

### A distribuição do status de conformidade por tipo de drive exibe dados antigos após a atualização dos itens de configuração

Depois de atualizar os itens de configuração do MBAM no SystemCenter2012 ConfigurationManager, o gráfico de distribuição de status de distribuição por tipo de unidade no painel de conformidade do BitLocker Enterprise mostra os dados que se baseiam em informações de versões antigas dos itens de configuração.

SOLUÇÃO alternativa: nenhum. Não há suporte para modificação dos itens de configuração do MBAM, e o relatório pode não aparecer como esperado.

### A configuração de segurança reforçada pode fazer com que os relatórios sejam exibidos incorretamente

Se a configuração de segurança reforçada (ESC) do Internet Explorer estiver ativada, uma mensagem de "acesso negado" poderá aparecer quando você tentar exibir relatórios no servidor do MBAM. Por padrão, a tecla ESC está ativada para proteger o servidor, diminuindo a exposição do servidor a possíveis ataques que podem ocorrer por meio de conteúdo da Web e scripts de aplicativo.

SOLUÇÃO alternativa: se a mensagem "acesso negado" for exibida quando você tentar exibir relatórios no servidor do MBAM, você pode definir um objeto de política de grupo ou alterar o padrão manualmente na sua imagem para desativar a configuração de segurança reforçada. Você também pode exibir os relatórios de outro computador em que a ESC não está habilitado.

### A instalação do MBAM Server falha quando você atualiza do SQL Server 2008 para o SQL Server 2012

Se você atualizar do SQL Server 2008 para o SQL Server 2012 e, em seguida, tentar instalar o banco de dados de conformidade e auditoria ou o banco de dados de recuperação, a instalação falha e é revertida. A falha ocorre porque o arquivo de SQLCMD.exe necessário foi removido durante a atualização do SQL e não pode ser encontrado pelo instalador do MBAM. As linhas do arquivo de log MSI podem parecer semelhantes às seguintes:

RunDbInstallScript de recuperação banco de de recuperação: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript de recuperação de banco de arquivos: dbInstance-xxxxxx\\I01RunDbInstallScript recuperação banco de arquivos do BD: SQLscript-C:\\Arquivos Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript recuperação DB CA: dbName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript recuperação _Recovery BD CA: MBAM-defaultDataPath I01\\MSSQL\\DATA\\RunDbInstallScript de banco de defaultLogPath de recuperação:-K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\RunDbInstallScript recuperação do banco de scriptLogPath de recuperação:-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\Arquivos Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFilename = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript recuperação de banco de dados do: Iniciando para executar o banco de dados de recuperação instalar scriptRunDbInstallScript recuperação de banco de dados do banco de dados: sqlcmd o arquivo de log está localizado na C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript recuperação banco de dados exceção: instalar a ação personalizada do banco de dados de recuperação exceção de saída de linha de comando: o sistema não

O Windows Installer do Windows Server está codificado para localizar o caminho do SQLCMD.exe examinando o valor da cadeia de caracteres de caminho no registro em HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup. A chave ainda está presente durante a migração do SQL Server 2008 para o SQL Server 2012, mas o caminho referenciado pelo valor de dados não contém o arquivo SQLCMD.exe, porque o processo de atualização do SQL removeu o arquivo.

SOLUÇÃO alternativa: renomeie temporariamente o valor da cadeia de caracteres de caminho HKLM\\Software\\Microsoft\\Microsoft do SQL Server\\100\\Tools\\ClientSetup para o **caminho \ _old**e execute novamente o Windows Installer do MBAM Server. Quando a instalação for concluída com êxito e criar os bancos de dados no SQL Server 2012, renomeie o **caminho \ _old** valor para **caminho**.

## Hotfixes e artigos da base de dados de conhecimento da MBAM 2.0


Esta seção contém hotfixes e artigos da KB para o MBAM 2.0.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Artigo do KB</strong></th>
<th align="left">Title</th>
<th align="left"><strong>Link</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>2831166</p></td>
<td align="left"><p>A instalação do Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 falha com os &quot; objetos cm do System Center já instalados&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)">support.microsoft.com/kb/2831166/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870849</p></td>
<td align="left"><p>Os usuários não podem recuperar a chave de recuperação do BitLocker usando o portal de autoatendimento do MBAM 2.0</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)">support.microsoft.com/kb/2870849/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2756402</p></td>
<td align="left"><p>O cliente MBAM falharia com a ID de evento 4 e o código de erro 0x8004100E na descrição do evento</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)">support.microsoft.com/kb/2756402/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620287</p></td>
<td align="left"><p>Mensagem de erro "erro de servidor no aplicativo"/Reports "" quando você clica na guia relatórios do MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)">support.microsoft.com/kb/2620287/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2639518</p></td>
<td align="left"><p>Erro ao abrir relatórios corporativos ou de conformidade de computador no MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)">support.microsoft.com/kb/2639518/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>MBAM relatório corporativo não está sendo atualizado</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2712461</p></td>
<td align="left"><p>Não há suporte para a instalação do MBAM em um controlador de domínio</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)">support.microsoft.com/kb/2712461/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2876732</p></td>
<td align="left"><p>Você recebe o código de erro 0x80071a90 durante a configuração de integração do Gerenciador de configurações ou autônomas do MBAM 2.0</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)">support.microsoft.com/kb/2876732/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2754259</p></td>
<td align="left"><p>MBAM e comunicações de rede seguras</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)">support.microsoft.com/kb/2754259/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870842</p></td>
<td align="left"><p>A instalação do MBAM 2.0 falha durante o cenário de integração do Configuration Manager com o SQL Server 2008</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)">support.microsoft.com/kb/2870842/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2668533</p></td>
<td align="left"><p>A instalação do MBAM falha se o SSRS do SQL não estiver configurado corretamente</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)">support.microsoft.com/kb/2668533/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870847</p></td>
<td align="left"><p>Falha na instalação do MBAM 2,0 com o &quot; erro na recuperação de configurações de função de servidor do Configuration Manager para&#39; função de ponto do &#39;Reporting Services&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)">support.microsoft.com/kb/2870847/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2870839</p></td>
<td align="left"><p>Os relatórios do MBAM 2.0 Enterprise não são atualizados na topologia autônoma do MBAM 2.0 devido à falha de CreateCache do trabalho do SQL</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)">support.microsoft.com/kb/2870839/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>MBAM relatório corporativo não está sendo atualizado</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2935997</p></td>
<td align="left"><p>Os relatórios de conformidade de computadores com suporte MBAM inclui incorretamente produtos sem suporte</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)">support.microsoft.com/kb/2935997/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2612822</p></td>
<td align="left"><p>O registro do computador foi rejeitado no MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)">support.microsoft.com/kb/2612822/EN-US</a></p></td>
</tr>
</tbody>
</table>

 

## Tópicos relacionados


[Sobre o MBAM 2.0](about-mbam-20-mbam-2.md)

 

 





