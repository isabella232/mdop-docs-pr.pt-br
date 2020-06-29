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
# Notas de versão do MBAM 2.0 SP1


Para pesquisar essas notas de versão, pressione Ctrl + F.

Leia estas notas de versão cuidadosamente antes de instalar o Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 Service Pack 1 (SP1). Estas notas da versão contêm informações necessárias para instalar com êxito a administração do BitLocker e o monitoramento do 2,0 SP1, e eles contêm informações que não estão disponíveis na documentação do produto. Se houver uma diferença entre essas notas de versão e outras documentações do MBAM 2,0 SP1, a alteração mais recente deve ser considerada autorizada. Estas notas de versão substituem o conteúdo que está incluído neste produto.

## <a href="" id="---------mbam-2-0-sp1-known-issues"></a> Problemas conhecidos do MBAM 2,0 SP1


Esta seção contém problemas conhecidos para o MBAM 2,0 SP1.

### A atualização do MBAM com a topologia integrada do Configuration Manager para o MBAM 2,0 SP1 requer a remoção manual de objetos do Configuration Manager

Se você estiver usando o MBAM com o Configuration Manager e quiser atualizar para o MBAM 2,0 SP1, será necessário remover manualmente todos os objetos do Configuration Manager que foram instalados no Configuration Manager como parte da instalação do MBAM. Os objetos que você deve remover manualmente são os relatórios do MBAM, a coleção MBAM Computers supported e a linha de base de configuração de proteção BitLocker e seus itens de configuração associados.

**Solução alternativa**: atualize os objetos do Configuration Manager completando as seguintes etapas:

1.  Faça backup dos dados de conformidade existentes para um arquivo externo, conforme descrito nas etapas a seguir.

    **Observação**  Todos os dados de conformidade do BitLocker existentes serão excluídos quando você excluir a linha de base existente no Configuration Manager. Os dados serão regenerados ao longo do tempo, mas é recomendável que você salve uma cópia dos dados em caso de precisar dos dados de conformidade para um computador específico antes que os dados de conformidade sejam gerados novamente.

     

    1.  Para salvar os dados de conformidade do BitLocker do histórico, abra o relatório de **detalhes de conformidade corporativa do BitLocker** .

    2.  Clique no ícone **salvar** no relatório e selecione **Excel**.

        O relatório salvo conterá dados como o nome do computador, o nome do domínio, o status de conformidade, isenção, usuários do dispositivo, detalhes do status de conformidade e data/hora do último contato. Algumas informações, como informações detalhadas sobre o volume e nível de criptografia, não são salvas.

2.  Desinstale o **MBAM** do servidor usando o instalador do **MBAM** .

3.  Exclua manualmente os seguintes objetos do Configuration Manager:

    -   Conjunto de computadores com suporte MBAM

    -   Linha de base de proteção BitLocker

    -   Item de configuração de proteção de unidade de sistema operacional BitLocker

    -   Item de configuração proteção de unidades de dados fixas do BitLocker

4.  Exclua manualmente a pasta de relatórios do MBAM no site do SQL Server Reporting Services do Configuration Manager. Para fazer isso:

    1.  Use o Internet Explorer para navegar até o ponto do Reporting Services, por exemplo, http:// &lt; yourcmserver &gt; /reports.

    2.  Clique no link de código de site apropriado do Configuration Manager.

    3.  Exclua a pasta MBAM.

5.  Use o instalador do MBAM Server para reinstalar os objetos de integração do Configuration Manager. Os computadores cliente começarão a carregar dados de conformidade do BitLocker novamente ao longo do tempo.

### O botão enviar no portal de autoatendimento não funciona no Internet Explorer10

Quando você usa o Internet Explorer10 para acessar o site de administração e monitoramento, o botão **Enviar** no website não funciona.

**Solução alternativa**: no servidor em que você instalou o site de administração e monitoramento, instale o [hotfix para ASP.net arquivos de definição do navegador](https://go.microsoft.com/fwlink/?LinkId=317798).

### Não há suporte para nomes de domínio internacionais

MBAM 2,0 SP1 não é compatível com nomes de domínio internacionais.

**Solução alternativa**: nenhum.

### Relatórios no site de administração e monitoramento exibirão um aviso se a SSL não estiver configurada no SSRS

Se o SSRS Reporting Services (SSRS) não tiver sido configurado para usar SSL (Secure Socket Layer), a URL dos relatórios será definida como HTTP em vez de HTTPS quando você instalar o servidor MBAM. Se, em seguida, você navegar até o site de administração e monitoramento e selecionar um relatório, a seguinte mensagem será exibida: "somente conteúdo seguro é exibido".

**Solução alternativa**: para corrigir esse problema, configure o SSL no **Gerenciador de configuração do Reporting Services** no servidor do MBAM em que o SqlServer Reporting Services está instalado. Desinstale e reinstale o site do servidor de administração e monitoração.

### Clicar em retornar no relatório de Resumo de conformidade pode criar um erro

Se você fizer buscas detalhadas em um relatório de Resumo de conformidade e, em seguida, clicar no link **retomar** no relatório SSRS, pode ocorrer um erro.

**Solução alternativa**: nenhum.

### O espaço usado apenas a criptografia não funciona corretamente

Se você criptografar um computador pela primeira vez após a instalação do cliente do MBAM e tiver definido um objeto de política de grupo para implementar a criptografia somente espaço usado, o MBAM criptografará erroneamente o disco inteiro, em vez de criptografar somente o espaço usado pelo disco. Se um computador já estiver criptografado com a criptografia somente espaço usado antes de instalar o cliente do MBAM, e você tiver definido o mesmo objeto de política de grupo de criptografia somente espaço usado, o MBAM reconhece a configuração e relata a criptografia corretamente nos relatórios de conformidade.

**Solução alternativa**: nenhum.

### O nível de codificação é exibido incorretamente no relatório de conformidade do computador

Se você não definir um nível de codificação específico no **método escolher o método de criptografia de unidade e** o objeto de política de grupo de força de codificação, o relatório de conformidade do computador na topologia integrada do Configuration Manager sempre exibirá **desconhecido** para o nível de codificação, mesmo quando a força de codificação usar o padrão de criptografia de 128 bits. O relatório exibe a intensidade de codificação correta se você definir um nível de codificação específico no objeto de política de grupo.

**Solução alternativa**: Defina sempre um nível de codificação específico no objeto **escolher método de criptografia de unidade e nível de codificação** .

### A distribuição do status de conformidade por tipo de drive exibe dados antigos após a atualização dos itens de configuração

Depois de atualizar os itens de configuração do MBAM no SystemCenter2012 ConfigurationManager, o gráfico de distribuição de status de distribuição por tipo de unidade no painel de conformidade do BitLocker Enterprise mostra os dados que se baseiam em informações de versões antigas dos itens de configuração.

**Solução alternativa**: nenhum. Não há suporte para modificação dos itens de configuração do MBAM, e o relatório pode não aparecer como esperado.

### A configuração de segurança reforçada pode fazer com que os relatórios sejam exibidos incorretamente

Se a configuração de segurança reforçada (ESC) do Internet Explorer estiver ativada, uma mensagem de **acesso negado** poderá ser exibida quando você tentar exibir relatórios no servidor do MBAM. Por padrão, a configuração de segurança reforçada está ativada para proteger o servidor, diminuindo a exposição do servidor a possíveis ataques que podem ocorrer por meio de conteúdo da Web e scripts de aplicativo.

**Solução alternativa**: se a mensagem de **acesso negado** for exibida quando você tentar exibir relatórios no servidor do MBAM, você pode definir um objeto de política de grupo ou alterar o padrão manualmente na sua imagem para desativar a configuração de segurança reforçada. Você também pode exibir os relatórios de outro computador em que a configuração de segurança reforçada não está habilitada.

### <a href="" id="-------------mbam-server-installation-fails-when-you-upgrade-from-sql-server-2008-to-sql-server-2012"></a> A instalação do MBAM Server falha quando você atualiza do SQLServer2008 para o SQLServer2012

Se você atualizar de SQLServer2008 para SQLServer2012 e, em seguida, tentar instalar o banco de dados de conformidade e auditoria ou o banco de dados de recuperação, a instalação falha e é revertida. A falha ocorre porque o arquivo de SQLCMD.exe necessário foi removido durante a atualização do SQLServer e não pode ser encontrado pelo instalador do MBAM. As linhas do arquivo de log MSI podem parecer semelhantes às seguintes:

RunDbInstallScript de recuperação banco de de recuperação: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript de recuperação de banco de arquivos: dbInstance-xxxxxx\\I01RunDbInstallScript recuperação banco de arquivos do BD: SQLscript-C:\\Arquivos Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript recuperação DB CA: dbName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript recuperação _Recovery BD CA: MBAM-defaultDataPath I01\\MSSQL\\DATA\\RunDbInstallScript de banco de defaultLogPath de recuperação:-K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\RunDbInstallScript recuperação do banco de scriptLogPath de recuperação:-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\Arquivos Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFilename = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript recuperação de banco de dados do: Iniciando para executar o banco de dados de recuperação instalar scriptRunDbInstallScript recuperação de banco de dados do banco de dados: sqlcmd o arquivo de log está localizado na C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript recuperação banco de dados exceção: instalar a ação personalizada do banco de dados de recuperação exceção de saída de linha de comando: o sistema não

O Windows Installer do Windows Server está codificado para localizar o caminho do SQLCMD.exe examinando o valor da cadeia de caracteres de caminho no registro em HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup. A chave ainda está presente durante a migração de SQLServer2008 para SQLServer2012, mas o caminho referenciado pelo valor de dados não contém o arquivo SQLCMD.exe, porque o processo sqlupgrade removeu o arquivo.

**Solução alternativa**: renomeie temporariamente o valor da cadeia de caracteres de caminho HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup para o **caminho \ _old**e execute o Windows Installer no servidor MBAM novamente. Quando a instalação for concluída com êxito e criar os bancos de dados no SQLServer2012, renomeie o **caminho \ _old** para **caminho**.

## Hotfixes e artigos da base de dados de conhecimento para MBAM 2,0 SP1


Esta seção contém hotfixes e artigos da KB para o MBAM 2,0 SP1.

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


[Sobre o MBAM 2.0 SP1](about-mbam-20-sp1.md)

 

 





