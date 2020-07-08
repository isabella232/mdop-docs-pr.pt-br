---
title: Logs de eventos do servidor
description: Logs de eventos do servidor
author: dansimp
ms.assetid: 04e724d2-28cc-4fa8-86a1-0d4ab0234b11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 269e9b4bc2644fae4dc5796652c7587bb0ef6076
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799261"
---
# Logs de eventos do servidor


As tabelas nesta seção fornecem informações sobre os IDs de evento de log do servidor do MBAM.

## Configuração


A tabela a seguir contém mensagens e informações de solução de problemas para IDs de evento que podem ocorrer no servidor MBAM durante a configuração.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ID do evento</th>
<th align="left">Origem</th>
<th align="left">Símbolo de evento</th>
<th align="left">Mensagem</th>
<th align="left">Solução de problemas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>103</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/operacional</p></td>
<td align="left"><p>VssRegistrationException</p></td>
<td align="left"><p>Uma exceção foi gerada durante o registro do VSS.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>104</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/operacional</p></td>
<td align="left"><p>VssDeregistrationException</p></td>
<td align="left"><p>Uma exceção foi gerada durante o cancelamento de registro do VSS.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>300</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>CmdletError</p></td>
<td align="left"><p>Falha ao remover a pasta.</p></td>
<td align="left"><p>Indica que ocorreu um erro de encerramento ao executar uma tarefa. Inspecione outras mensagens de evento no log para diagnosticar ainda mais a configuração do MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>301</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>cmdletUnexpectedError</p></td>
<td align="left"><p>Erro de cmdlet inesperado.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>302</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>CmdletWarning</p></td>
<td align="left"><p>Aviso de cmdlet.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>303</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/operacional</p></td>
<td align="left"><p>CmdletInformation</p></td>
<td align="left"><p>Informações do cmdlet.</p></td>
<td align="left"><p>Somente informativo; sem necessidade de solução de problemas. O evento indica que uma tarefa está ocorrendo pelos cmdlets como enabling\disabling um recurso ou cancelando uma operação.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>400</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>ConfiguratorError</p></td>
<td align="left"><p>Erro do Configurador.</p></td>
<td align="left"><p>Indica que ocorreu um erro ao iniciar o configurador MBAM. Certifique-se de que o usuário tenha privilégios adequados para iniciar o configurador do MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>401</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>ConfiguratorUnexpectedError</p></td>
<td align="left"><p>Erro de configurador inesperado.</p></td>
<td align="left"><p>Indica que ocorreu um erro de encerramento ao executar uma tarefa do Configurador MBAM. A mensagem de erro conterá mais detalhes sobre o erro. Inspecione outras mensagens de erro no log de eventos para diagnosticar ainda mais a configuração do MBAM. Os erros conhecidos incluem:</p>
<ul>
<li><p>Falha ao recuperar ou validar um certificado selecionado pelo usuário</p></li>
<li><p>Falha ao analisar a URL dos relatórios</p></li>
<li><p>Falha ao abrir logs de eventos para o usuário</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>402</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>ConfiguratorWarning</p></td>
<td align="left"><p>Aviso do Configurador.</p></td>
<td align="left"><p>Indica que uma tarefa do MBAM configurador não está concluída como esperado, mas não foi completamente reprovada. As tarefas conhecidas incluem o certificado ausente na loja do LocalMachine\My que foi configurada no recurso de aplicativo Web ou um tempo limite para uma tarefa pendente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>410</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/operacional</p></td>
<td align="left"><p>ConfiguratorInformation</p></td>
<td align="left"><p>Informações do Configurador.</p></td>
<td align="left"><p>Somente informativo; sem necessidade de solução de problemas. O evento indica que uma tarefa está sendo invocada pelo configurador MBAM. As tarefas conhecidas incluem:</p>
<ul>
<li><p>Iniciando o configurador</p></li>
<li><p>Verificando pré-requisitos de software para um recurso do MBAM</p></li>
<li><p>Validando parâmetros para um recurso do MBAM</p></li>
<li><p>Enabling\disabling\committing um recurso MBAM</p></li>
<li><p>Gerando um script do PowerShell a partir do Configurador</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>500</p></td>
<td align="left"><p>Microsoft_Windows_MBAM_Server_Admin</p></td>
<td align="left"><p>WebProviderUnexpectedError</p></td>
<td align="left"><p>Erro inesperado do provedor do aplicativo Web.</p></td>
<td align="left"><p>Indica que ocorreu um erro ao habilitar e configurar um site da Web do MBAM ou serviço Web no IIS. Os erros conhecidos incluem:</p>
<ul>
<li><p>Falha ao localizar a pasta raiz WWW do IIS</p></li>
<li><p>Falha ao acessar a configuração do IIS no web.config devido a arquivos malformados ou configurações ausentes</p></li>
<li><p>Falha ao criar ou remover um aplicativo Web</p></li>
<li><p>Violação de acesso do IIS</p></li>
</ul>
<p>Esse erro também será registrado se MBAM não conseguir acessar o Active Directory (AD) para validar contas de usuário. Verifique se o IIS está instalado, corretamente configurado e se o serviço IIS está em execução. Verifique se todas as verificações de pré-requisitos do software MBAM foram aprovadas. Verifique se o usuário tem as permissões corretas para criar aplicativos Web na instância do IIS. Verifique se o usuário tem acesso para ler objetos de conta de usuário no AD.</p></td>
</tr>
<tr class="even">
<td align="left"><p>501</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>WebProviderError</p></td>
<td align="left"><p>Erro inesperado do provedor do aplicativo Web.</p></td>
<td align="left"><p>Indica que ocorreu um erro ao habilitar, desabilitar ou configurar um site ou serviço da Web do MBAM no IIS. Os erros conhecidos incluem:</p>
<ul>
<li><p>Falha ao ler informações de associação básicas ou WSHttp do IIS</p></li>
<li><p>Seção identidade ausente ou entrada DNS na seção identidade nos arquivos de configuração do IIS</p></li>
<li><p>Falha ao abrir a chave do registro HKLM\SOFTWARE\Microsoft\InetStp</p></li>
<li><p>Falha ao ler o valor PathWWWRoot da chave do registro HKLM\SOFTWARE\Microsoft\InetStp</p></li>
<li><p>O usuário está tentando especificar um nome de diretório virtual com um nome reservado para MBAM</p></li>
</ul>
<p>Verifique se o IIS está instalado e configurado corretamente. Verifique se a chave do registro HKLM\SOFTWARE\Microsoft\InetStp: PathWWWRoot existe e está acessível. Verifique se as informações de associação no IIS não estão corrompidas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>502</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>WebProviderWarning</p></td>
<td align="left"><p>Aviso de provedor de aplicativo Web.</p></td>
<td align="left"><p>Indica que ocorreu um erro de não encerramento ao habilitar um site ou serviço da Web do MBAM. Os erros conhecidos incluem:</p>
<ul>
<li><p>Falha ao acessar o AD para validar o SPN (nome da entidade de serviço) na conta do pool de aplicativos</p></li>
<li><p>Falha ao validar o SPN porque ele está atribuído a várias contas no AD</p></li>
<li><p>Falha ao registrar um SPN na conta do pool de aplicativos no AD</p></li>
<li><p>O SPN está registrado em uma conta diferente do pool de aplicativos no AD</p></li>
<li><p>Falha ao remover o SPN da conta do pool de aplicativos no anúncio durante uma operação de reversão</p></li>
<li><p>Falha ao verificar se o grupo de IIS_IUSRS recebeu o privilégio de logon como um lote no servidor IIS</p></li>
</ul>
<p>A mensagem do evento conterá mais informações sobre o erro específico. Verifique se o anúncio pode ser acessado do servidor em que a instalação do MBAM está sendo executada. Verifique se o usuário que está executando a instalação do MBAM tem permissões de leitura na conta do pool de aplicativos no AD. Se um SPN já estiver registrado na conta do pool de aplicativos no AD, certifique-se de que ele não esteja registrado em outras contas.</p></td>
</tr>
<tr class="even">
<td align="left"><p>503</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/operacional</p></td>
<td align="left"><p>WebProviderInformation</p></td>
<td align="left"><p>Informações do provedor de aplicativos Web. Descritivo</p></td>
<td align="left"><p>Somente informativo; sem necessidade de solução de problemas. O evento indica que uma tarefa está sendo invocada pela configuração do MBAM. As tarefas conhecidas incluem obter a configuração do IIS, como informações de associação e site raiz, e configurar o SPN (nome da entidade de serviço).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>600</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>SetupUnexpectedError</p></td>
<td align="left"><p>Erro de configuração inesperado.</p></td>
<td align="left"><p>Indica que ocorreu um erro de encerramento ao enabling\disabling ou configuração de um recurso do MBAM. Os erros conhecidos incluem:</p>
<ul>
<li><p>Falha ao reverter uma tarefa após um erro</p></li>
<li><p>Falha ao ler do registro</p></li>
<li><p>Falha ao criar ou excluir uma pasta no sistema de arquivos</p></li>
<li><p>Falha ao ler informações sobre a versão do SQL</p></li>
<li><p>Falha ao registrar o gravador VSS no SQL</p></li>
</ul>
<p>A mensagem do evento conterá mais informações sobre o erro específico. Verifique se todas as verificações de pré-requisitos do software MBAM foram aprovadas. Verifique se o caminho do registro MBAM, se existe, HKEY_LOCAL_MACHINE servidor \SOFTWARE\Microsoft\MBAM e todas as subchaves são legíveis. Verifique se o anúncio pode ser acessado do servidor em que a instalação do MBAM está sendo executada. Verifique se o usuário que está executando a instalação do MBAM tem permissões de leitura no AD.</p>
<p>Para um registro bem-sucedido do gravador do VSS, verifique se uma versão com suporte do SQL está instalada e se uma instância está acessível para o usuário que está executando a configuração do MBAM. Se você desabilitar um recurso do MBAM ou desinstalar o MBAM, verifique se todos os arquivos, como arquivos de log e arquivos de web.config estão fechados, para que o MBAM possa remover seus sites e serviços da Web.</p></td>
</tr>
<tr class="even">
<td align="left"><p>601</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>SetupError</p></td>
<td align="left"><p>Erro de instalação.</p></td>
<td align="left"><p>Indica que ocorreu um erro de encerramento ao enabling\disabling ou configuração de um recurso do MBAM. Os erros conhecidos incluem:</p>
<ul>
<li><p>Falha ao ler a configuração do MBAM no IIS</p></li>
<li><p>Seção appSettings corrompida na configuração do IIS ou configurações mal configuradas</p></li>
<li><p>Falha ao validar o nome do host</p></li>
<li><p>Falha ao ler informações sobre a versão do SQL</p></li>
<li><p>Falha ao registrar o gravador VSS no SQL</p></li>
</ul>
<p>A mensagem do evento conterá mais informações sobre o erro específico. Verifique se o IIS está instalado e configurado corretamente. Verifique se todas as verificações de pré-requisitos do software MBAM foram aprovadas. Para um registro bem-sucedido do gravador do VSS, verifique se uma versão com suporte do SQL está instalada e se uma instância está acessível para o usuário que está executando a configuração do MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>602</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>SetupWarning</p></td>
<td align="left"><p>Aviso de instalação.</p></td>
<td align="left"><p>Indica que ocorreu um erro de não encerramento durante a enabling\disabling ou a configuração de um recurso MBAM, como a integração do Configuration Manager (CM) ou o aplicativo Web MBAM. Os erros conhecidos incluem: falha ao excluir relatórios do MBAM do ponto de função SRS no CM e falha ao resolver um nome de host do controlador de domínio. A mensagem do evento conterá mais informações sobre o erro específico.</p>
<p>Verifique se o anúncio pode ser acessado do servidor em que a instalação do MBAM está sendo executada. Verifique se o usuário que está executando a configuração do MBAM removeu permissões na instância do SSRS que está configurada como um ponto de função do SRS em CM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>603</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/operacional</p></td>
<td align="left"><p>SetupInformation</p></td>
<td align="left"><p>Informações de configuração.</p></td>
<td align="left"><p>Somente informativo; sem necessidade de solução de problemas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>605</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>WebProviderSoftwareCheckFailure</p></td>
<td align="left"><p>O aplicativo Web não pode ser habilitado porque uma ou mais dependências de software não estão sendo atendidas.</p></td>
<td align="left"><p>Durante a instalação do Web site/serviço Web do MBAM, a instalação do MBAM verifica se os pré-requisitos necessários estão corretos. Esta mensagem indica que o MBAM falhou ao instalar o Web site/serviço Web solicitado, pois o pré-requisito necessário está ausente. Consulte mensagens de erro anteriores a essa mensagem para obter mais informações sobre pré-requisitos ausentes.</p></td>
</tr>
<tr class="even">
<td align="left"><p>606</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>SetupParameterValidationFailure</p></td>
<td align="left"><p>O parâmetro necessário para habilitar o recurso do servidor não foi especificado ou não passou na validação.</p></td>
<td align="left"><p>Indica que o parâmetro necessário para configurar um recurso MBAM não foi especificado ou não passou na validação.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>607</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>SetupParameterValidationFailureWithError</p></td>
<td align="left"><p>Erro encontrado ao tentar validar o parâmetro especificado necessário para habilitar o recurso do servidor.</p></td>
<td align="left"><p>Indica que um erro foi encontrado ao tentar validar o parâmetro especificado necessário para habilitar o recurso do servidor.</p></td>
</tr>
<tr class="even">
<td align="left"><p>700</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>DbProviderUnexpectedError</p></td>
<td align="left"><p>Erro inesperado do provedor do BD.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>701</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>DbProviderError</p></td>
<td align="left"><p>Erro do provedor do BD.</p></td>
<td align="left"><p>A mensagem contida na seção EventDetails deve fornecer mais informações sobre o erro real. Estas são algumas das áreas a serem verificadas:</p>
<ul>
<li><p>A instalação do MBAM falhou ao se conectar ao banco de dados usando as informações de conexão fornecidas. Verifique os detalhes da cadeia de conexão fornecidos à instalação do MBAM.</p></li>
<li><p>A instalação do MBAM não pôde se conectar ao banco de dados fornecido usando as credenciais de conta de domínio fornecidas. Verifique se o nome de usuário e a senha da conta de domínio são válidos.</p></li>
<li><p>A instalação do MBAM não pôde se conectar ao banco de dados fornecido usando as credenciais de conta de domínio fornecidas. Verifique se a conta de domínio fornecida tem permissões necessárias no lugar para se conectar ao banco de dados do MBAM.</p></li>
<li><p>MBAM PAC do DAC não será bem-sucedida se uma versão mais recente do banco de dados do MBAM já estiver instalada. Verifique se uma nova versão do bancos de dados do MBAM não existe no SQL Server fornecido.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>702</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>DbProviderWarning</p></td>
<td align="left"><p>Aviso do provedor de BD.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>703</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/operacional</p></td>
<td align="left"><p>DbProviderInformation</p></td>
<td align="left"><p>Informações do provedor do banco de dados.</p></td>
<td align="left"><p>Somente informativo; sem necessidade de solução de problemas.</p></td>
</tr>
<tr class="even">
<td align="left"><p>704</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>DbProviderDacError</p></td>
<td align="left"><p>Ocorreu um erro ao implantar o aplicativo da camada de dados.</p></td>
<td align="left"><p>O MBAM empacota seus bancos de dados como aplicativos da camada de dados e tenta registrá-los usando Microsoft. SqlServer. DAC. DacServices. A mensagem de erro no contexto é reportada pelo serviço DAC. O evento deve conter informações detalhadas sobre o que causou. Leia as informações na mensagem de erro para solucionar e corrigir o problema.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>705</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>DbProviderDacWarning</p></td>
<td align="left"><p>Ocorreu um aviso ao implantar o aplicativo da camada de dados.</p></td>
<td align="left"><p>MBAM compacta seus bancos de dados como aplicativo da camada de dados e tenta registrá-los usando Microsoft. SqlServer. DAC. DacServices. A mensagem de aviso em contexto é reportada pelo serviço DAC. O evento deve conter informações detalhadas sobre o que causou. Leia as informações na mensagem de aviso para solucionar e corrigir o problema.</p></td>
</tr>
<tr class="even">
<td align="left"><p>706</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/operacional</p></td>
<td align="left"><p>DbProviderDacInformation</p></td>
<td align="left"><p>Uma mensagem foi gerada durante a implantação do aplicativo da camada de dados.</p></td>
<td align="left"><p>Somente informativo; sem necessidade de solução de problemas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>800</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>ReportProviderUnexpectedError</p></td>
<td align="left"><p>Erro inesperado do provedor de relatório.</p></td>
<td align="left"><p>Erro inesperado do provedor de relatório. Descritivo {exceptionDetails} Estes são alguns dos possíveis detalhes da exceção:</p>
<p><strong>Ocorreu um erro ao obter o nome do &#39; do diretório {directoryName} &#39;</strong></p>
<p><strong>Ocorreu uma exceção ao obter arquivos para o diretório &#39; {directoryName} &#39;</strong></p>
<p><strong>Ocorreu uma exceção ao enumerar os diretórios no diretório &#39; {directoryName} &#39;</strong></p>
<p><strong>Ocorreu uma exceção ao ler todos os bytes para o arquivo &#39; {fileName} &#39;</strong></p>
<p>Durante a instalação do MBAM, o programa de instalação do MBAM descompacta todos os arquivos de relatório para o caminho de instalação especificado. Como parte da instalação do relatório, o módulo de instalação tenta acessar os arquivos de relatório descompactados no caminho de instalação e se comunica com o SQL Reporting Services para publicar os arquivos de relatório. Os erros acima ocorrem quando o MBAM não pode acessar os arquivos/pastas no caminho de instalação descompactado. Estas são algumas dicas para solucionar esse problema:</p>
<ul>
<li><p>Verifique se o MBAM está instalado.</p></li>
<li><p>Verifique se a RegKey HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM Server\InstallationPath está presente e acessível para o usuário que está executando.</p></li>
<li><p>Verifique se o caminho para os arquivos de relatório em MBAM InstallationPath não excede 248 caracteres.</p></li>
<li><p>Verifique se a pasta de instalação do MBAM ou os arquivos contidos no caminho de instalação do MBAM não foram modificados desde a instalação.</p></li>
<li><p>Verifique se o usuário que está executando a instalação está autorizado a ler de/gravar na pasta de instalação do MBAM.</p></li>
</ul>
<p><strong>Falha na conectividade do Reporting Services. {exceptionDetails}</strong></p>
<p>Durante a instalação dos relatórios do MBAM, os módulos tentam se comunicar com os serviços Web do SSRS para criar pastas e publicar relatórios. A mensagem acima indica que o MBAM não pôde localizar ou se comunicar com os serviços Web do SSRS. Estas são algumas dicas para solucionar esse problema:</p>
<ul>
<li><p>Verifique se o SSRS está instalado no computador especificado.</p></li>
<li><p>Usar o console do SSRS Verifique se o SSRS está habilitado e em execução.</p></li>
<li><p>Verifique se o usuário que está executando a instalação está autorizado a acessar o SSRS.</p></li>
</ul>
<p><strong>Falha ao remover os relatórios do MBAM que usam a URL da instância do Reporting Services &#39; {SSRSInstanceUrl} &#39;. Certifique-se de que a instância do SSRS necessária para os relatórios do MBAM esteja em execução e configurada corretamente.</strong></p>
<p>Quando a instalação do MBAM falha ou quando o usuário desabilita recursos de relatórios do MBAM, o módulo de instalação remove relatórios SSRS. A mensagem acima indica que o MBAM falhou ao remover relatórios SSRS. Estas são algumas dicas para solucionar esse problema:</p>
<ul>
<li><p>Verifique se o SSRS está instalado no computador especificado.</p></li>
<li><p>Usar o console do SSRS Verifique se o SSRS está habilitado e em execução.</p></li>
<li><p>Verifique se o usuário que está executando a instalação está autorizado a acessar o SSRS.</p></li>
</ul>
<p><strong>Ocorreu um erro ao publicar os relatórios. {exceptionDetails}.</strong></p>
<p>Durante a instalação dos relatórios do MBAM, os módulos tentam se comunicar com os serviços Web do SSRS para criar pastas e publicar relatórios. A mensagem acima indica que o serviço Web do SSRS relatou e exceção ao publicar relatórios. Estas são algumas dicas para solucionar esse problema:</p>
<ul>
<li><p>Usar o console do SSRS Verifique se o SSRS está habilitado e em execução.</p></li>
<li><p>Verifique se o usuário que está executando a instalação está autorizado a acessar/publicar relatórios no SSRS.</p></li>
</ul>
<p><strong>Uma política para o nome de usuário do grupo &#39; {userName} &#39; já existe. Caso não esteja correto, revise manualmente o serviço de relatório para políticas duplicadas ou inválidas.</strong></p>
<p>Após a publicação de relatórios do MBAM, a instalação do MBAM tenta criar um MBAM relatar funções aos usuários (se ele ainda não existir) e define a política de usuário correspondente. O erro acima indica que o serviço Web SSRS emitiu uma exceção ao configurar a política de função de usuário de relatório. Siga as instruções na mensagem do evento e consulte &quot; <a href="https://www.microsoft.com/technet/support/ee/transform.aspx?ProdName=SQL+Server+Reporting+Services&amp;ProdVer=8.00&amp;EvtID=rsInvalidPolicyDefinition&amp;EvtSrc=Microsoft.ReportingServices.Diagnostics.ErrorStrings.resources.Strings&amp;LCID=1033&amp;quot" data-raw-source="https://www.microsoft.com/technet/support/ee/transform.aspx?ProdName=SQL+Server+Reporting+Services&amp;amp;ProdVer=8.00&amp;amp;EvtID=rsInvalidPolicyDefinition&amp;amp;EvtSrc=Microsoft.ReportingServices.Diagnostics.ErrorStrings.resources.Strings&amp;amp;LCID=1033&amp;quot"> https://www.microsoft.com/technet/support/ee/transform.aspx?ProdName=SQL+Server+Reporting+Services&amp ; ProdVer = 8 &amp; EvtID = rsInvalidPolicyDefinition &amp; EvtSrc = Microsoft. ReportingServices. Diagnostics. ErrorStrings. Resources. Strings &amp; LCID = 1033&quot </a> ; para obter mais ajuda.</p>
<p><strong>Ocorreu um erro ao validar o acesso ao SSRS {exceptionDetails}.</strong></p>
<p>Como parte da verificação de pré-requisitos, a configuração do MBAM verifica se o usuário tem permissões necessárias para acessar/criar pasta em SSRS. A mensagem de erro indica que ocorreu uma exceção ao verificar o acesso ao SSRS. Consulte os detalhes da exceção para obter dicas de depuração.</p>
<p><strong>Ocorreu um erro de SOAP ao verificar a URL do SSRS. {exceptionDetails}</strong></p>
<p><strong>Ocorreu um erro na Web ao verificar a URL do SSRS. {exceptionDetails}</strong></p>
<p><strong>Ocorreu um erro http/https ao verificar a URL do SSRS. {exceptionDetails}</strong></p>
<p><strong>Ocorreu um erro ao verificar a URL do SSRS. {exceptionDetails}</strong></p>
<p>Como parte da verificação de pré-requisitos, a configuração do MBAM recupera URLs associadas à instância do SSRS fornecida e tenta se comunicar com o serviço Web do SSRS. A mensagem de erro acima indica que o serviço Web SSRS na URL fornecida emitiu uma exceção, consulte os detalhes da exceção para obter mais informações. Estas são algumas dicas para resolver problemas de comunicação do SSRS.</p>
<ul>
<li><p>Verifique se o SSRS está instalado no computador especificado.</p></li>
<li><p>Usar o console do SSRS Verifique se o SSRS está habilitado e em execução.</p></li>
<li><p>Verifique se o usuário que está executando a instalação está autorizado a acessar o SSRS.</p></li>
</ul>
<p><strong>Ocorreu um erro ao recuperar a versão do SSRS. {exceptionDetails}</strong></p>
<p>Como parte da verificação de pré-requisitos, a configuração MBAM consulta o WMI para recuperar o número de versão associado à instância SSRS fornecida. A mensagem de erro acima indica que ocorreu uma exceção ao consultar o WMI. Consulte exceptionDetails para obter mais informações. Estas são algumas verificações que você pode executar:</p>
<ul>
<li><p>Verifique se o SSRS com o nome da instância especificado está instalado no computador especificado.</p></li>
<li><p>Usar o console do SSRS Verifique se o SSRS está habilitado e em execução.</p></li>
<li><p>Verifique se o usuário que está executando a instalação está autorizado a consultar classe SSRS em namespace WMI.</p></li>
</ul>
<p><strong>O usuário atual não está autorizado a acessar o namespace WMI &#39; {ssrsWMINamespace} &#39;.</strong></p>
<p><strong>Ocorreu um erro ao enumerar o namespace &#39; {ssrsWMINamespace} &#39;. O servidor de RPC para o provedor de WMI SSRS no host local não foi encontrado.</strong></p>
<p><strong>Ocorreu um erro ao enumerar o namespace &#39; {ssrsNamespace} &#39;. Não é possível localizar uma instância do SSRS no host local.</strong></p>
<p><strong>Ocorreu um erro ao acessar o WMI. O servidor de RPC para a instância &#39; {ssrsInstance} &#39; não foi encontrado.</strong></p>
<p><strong>Ocorreu um erro ao acessar o WMI. O nome da instância &#39; {ssrsInstanceName} &#39; não está correto.</strong></p>
<p><strong>Ocorreu um erro ao acessar o WMI. Não é possível encontrar a instância &#39; {ssrsInstanceName} &#39; no host local.</strong></p>
<p>Como parte da verificação de pré-requisitos, a configuração MBAM consulta o WMI para recuperar o namespace WMI associado à instância fornecida. A mensagem de erro acima indica que e exceção ocorreu ao consultar a WMI. Consulte exceptionDetails para obter mais informações. Estas são algumas verificações que você pode executar:</p>
<ul>
<li><p>Verifique se o SSRS com o nome da instância especificado está instalado no computador especificado.</p></li>
<li><p>Usar o console do SSRS Verifique se o SSRS está habilitado e em execução.</p></li>
<li><p>Verifique se o usuário que está executando a instalação está autorizado a acessar/consultar a classe SSRS em namespace WMI.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>801</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>ReportProviderError</p></td>
<td align="left"><p>Erro inesperado do provedor de relatório.</p></td>
<td align="left"><p>Devido ao nome da instância do SQL Server Reporting Services, o MBAM tenta encontrar o namespace WMI correspondente à instância de relatório e se conecta a ele. Esse erro ocorre se o MBAM encontrar uma exceção quando o MBAM procura ou tenta se conectar ao namespace WMI do SSRS. Leia as informações nas mensagens de erro registradas no canal de instalação do MBAM antes desta mensagem para obter mais detalhes. Veja algumas coisas que você pode verificar:</p>
<ul>
<li><p>Verifique se o SSRS com o nome de instância fornecido está ativo e em execução</p></li>
<li><p>Verifique se a conta de usuário que executa a instalação do MBAM tem as permissões necessárias para consultar/conectar-se ao namespace WMI do SSRS</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>802</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>ReportProviderWarning</p></td>
<td align="left"><p>Aviso do provedor de relatório.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>803</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/operacional</p></td>
<td align="left"><p>ReportProviderInformation</p></td>
<td align="left"><p>Relatar informações do provedor.</p></td>
<td align="left"><p>Somente informativo; sem necessidade de solução de problemas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>900</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>CMProviderUnexpectedError</p></td>
<td align="left"><p>Erro inesperado do provedor CM.</p></td>
<td align="left"><p>Indica que ocorreu um erro de encerramento ao enabling\disabling ou configuração do recurso de integração do Configuration Manager (CM) no MBAM. Os erros conhecidos incluem:</p>
<ul>
<li><p>Falha ao se conectar ao servidor de site CM pelo provedor de SMS</p></li>
<li><p>Falha ao ler do registro</p></li>
<li><p>Falha ao criar ou excluir uma pasta no sistema de arquivos</p></li>
<li><p>Falha ao localizar a instalação do console do Configuration Manager no computador local</p></li>
<li><p>Falha ao recuperar informações para a instância do SSRS configurada como um ponto de função do SRS no CM</p></li>
</ul>
<p>A mensagem do evento conterá mais informações sobre o erro específico. Verifique se todas as verificações de pré-requisitos do software MBAM foram aprovadas. Verifique se o caminho do registro MBAM, se existe, HKEY_LOCAL_MACHINE servidor \SOFTWARE\Microsoft\MBAM e todas as subchaves são legíveis. Verifique se o MBAM está sendo integrado com uma versão com suporte do Configuration Manager. Verifique se o console do Configuration Manager está instalado no computador em que a configuração do MBAM está sendo invocada e se o console pode ser usado para conexão com o servidor de site de destino CM. Verifique se uma instância válida do SSRS está configurada como um ponto de função do SRS em CM e se o usuário que está executando a configuração MBAM tem permissões read\write na instância do SSRS.</p></td>
</tr>
<tr class="even">
<td align="left"><p>901</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/admin</p></td>
<td align="left"><p>CMProviderError</p></td>
<td align="left"><p>Erro inesperado do provedor CM.</p></td>
<td align="left"><p>Indica que ocorreu um erro de encerramento ao enabling\disabling ou configuração do recurso de integração do Configuration Manager (CM) no MBAM. Os erros conhecidos incluem:</p>
<ul>
<li><p>Falha ao se conectar ao servidor de site CM pelo provedor de SMS</p></li>
<li><p>Falha ao ler do registro</p></li>
<li><p>Falha ao criar ou excluir uma pasta no sistema de arquivos</p></li>
<li><p>Falha ao localizar a instalação do console do Configuration Manager no computador local</p></li>
<li><p>pasta do ConfigMgr ausente no SSRS como a pasta raiz dos relatórios de ponto de função SRS</p></li>
<li><p>fonte de dados compartilhada do ConfigMgr ausente no SSRS</p></li>
<li><p>Falha ao implantar relatórios SSRS na instância do SSRS configurada como um ponto de função do SRS no CM</p></li>
<li><p>Falha ao criar itens de configuração e linhas de base em CM</p></li>
</ul>
<p>A mensagem do evento conterá mais informações sobre o erro específico. Verifique se todas as verificações de pré-requisitos do software MBAM foram aprovadas. Verifique se o caminho do registro MBAM, se existe, HKEY_LOCAL_MACHINE servidor \SOFTWARE\Microsoft\MBAM e todas as subchaves são legíveis. Verifique se o MBAM está sendo integrado com uma versão com suporte do Configuration Manager. Verifique se o console do Configuration Manager está instalado no computador em que a configuração do MBAM está sendo invocada e se o console pode ser usado para conexão com o servidor de site de destino CM. Verifique se o usuário tem as permissões read\write necessárias para criar itens de configuração, linhas de base e coleções em CM. Verifique se uma instância válida do SSRS está configurada como um ponto de função do SRS em CM e se o usuário que está executando a configuração MBAM tem permissões read\write na instância do SSRS.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>902</p></td>
<td align="left"><p>Microsoft_Windows_MBAM_Server_Admin</p></td>
<td align="left"><p>CMProviderWarning</p></td>
<td align="left"><p>Aviso do provedor CM.</p></td>
<td align="left"><p>Indica que ocorreu um erro de não encerramento ao habilitar o recurso de integração do Configuration Manager (CM). Os erros conhecidos incluem: falha ao confirmar regras de coleta no conjunto de computadores com suporte MBAM em CM e outros erros relacionados a redes e SSRS.</p>
<p>A mensagem do evento conterá mais informações sobre o erro específico. Algumas operações que causaram esse aviso são desativadas após o aviso. Se, após várias tentativas, o erro persistir, MBAM poderá terminar com um erro real. Inspecione outras mensagens de evento no log para diagnosticar ainda mais a configuração do MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>903</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-servidor/operacional</p></td>
<td align="left"><p>CMProviderInformation</p></td>
<td align="left"><p>Informações do provedor CM.</p></td>
<td align="left"><p>Somente informativo; sem necessidade de solução de problemas.</p></td>
</tr>
</tbody>
</table>

 

## Operação


A tabela a seguir contém mensagens e informações de solução de problemas para IDs de evento que podem ocorrer enquanto o MBAM está em execução.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ID do evento</th>
<th align="left">Origem</th>
<th align="left">Símbolo de evento</th>
<th align="left">Mensagem</th>
<th align="left">Solução de problemas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>um</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/administrador</p></td>
<td align="left"><p>WebAppSpnError</p></td>
<td align="left"><p>Aplicativo: {SiteName} {VirtualDirectory} não contém os seguintes nomes principais de serviço (SPNs): {ListOfSpns} registre os SPNs necessários na conta: {ExecutionAccount}.</p></td>
<td align="left"><p>Para que a autenticação integrada do Windows seja bem-sucedida, os SPNs necessários devem estar vigentes. Esta mensagem indica que o SPN necessário para o aplicativo MBAM não foi configurado corretamente. Os detalhes contidos nesse evento devem fornecer mais informações.</p>
<p>Consulte "nome da entidade de serviço (SPN)" nos <a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md#bkmk-prereqsams" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md#bkmk-prereqsams)"> pré-requisitos do servidor do MBAM 2,5 para topologias autônomas e </a> de integração do Configuration Manager para obter mais informações.</p></td>
</tr>
<tr class="even">
<td align="left"><p>4</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/operacional</p></td>
<td align="left"><p>PerformanceCounterError</p></td>
<td align="left"><p>Ocorreu um erro ao recuperar um contador de desempenho.</p>
<p>Mensagem: {EventMessage} Category: {CategoryOfPerformanceCounter} contador de desempenho: {NameOfPerformanceCounter} instância: {nome da instância de categoria do contador de desempenho} exceção: {ExceptionThrown}</p>
<p>A mensagem de rastreamento conterá a mensagem de exceção real, algumas delas são explicadas aqui:</p>
<p><strong>ArgumentNullException </strong> : essa exceção será lançada se a categoria, o contador ou a instância do contador de desempenho solicitado for inválido.</p>
<p><strong>System. InvalidOperationException </strong> : CategoryName é uma cadeia de caracteres vazia ( &quot; &quot; ).-ou-CounterName é uma cadeia de caracteres vazia ( &quot; &quot; ).</p>
<p>-ou-a configuração de permissão de leitura/gravação solicitada é inválida para este contador.</p>
<p>-ou-a categoria especificada não existe (se readOnly for verdadeiro).</p>
<p>-ou-a categoria especificada não é uma categoria personalizada do .NET Framework (se readOnly for falso).</p>
<p>-ou-a categoria especificada está marcada como de várias instâncias e requer que o contador de desempenho seja criado com um nome de instância.</p>
<p>-ou-instanceName tem mais de 127 caracteres.</p>
<p>-ou-NomeDaCategoria e counterName foram traduzidos em diferentes idiomas.</p>
<p><strong>System. ComponentModel. Win32exception </strong> : ocorreu um erro ao acessar uma API do sistema.</p>
<p><strong>System. PlatformNotSupportedException </strong> : a plataforma é windows 98 ou Windows Millennium Edition (me), que não dá suporte a contadores de desempenho.</p>
<p><strong>System. UnauthorizedAccessException </strong> : o código que está em execução sem privilégios administrativos tentou ler um contador de desempenho.</p></td>
<td align="left"><p>A mensagem contida no evento fornecerá mais detalhes sobre a exceção que foi lançada. Se um System. UnauthorizedAccessException foi lançado, verifique se a conta de execução do MBAM (pool de aplicativos) tem acesso a APIs de contador de desempenho.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>100</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/administrador</p></td>
<td align="left"><p>AdminServiceRecoveryDbError</p></td>
<td align="left"><p><strong>GetMachineUsers </strong> : ocorreu um erro ao obter as informações do usuário a partir do banco de dados. Mensagem: {Message}-ou-</p>
<p><strong>GetRecoveryKey </strong> : ocorreu um erro ao obter a chave de recuperação do banco de dados. Mensagem: {Message}-ou-</p>
<p><strong>GetRecoveryKey </strong> : ocorreu um erro ao obter as informações do usuário a partir do banco de dados. Mensagem: {Message}-ou-</p>
<p><strong>GetRecoveryKeyIds </strong> : ocorreu um erro ao obter as IDs da chave de recuperação do banco de dados. Mensagem: {Message}-ou-</p>
<p><strong>GetTpmHashForUser </strong> : ocorreu um erro ao obter dados de hash TPM do banco de dados de recuperação. Mensagem: {Message}-ou-</p>
<p><strong>GetTpmHashForUser </strong> : ocorreu um erro ao obter dados de hash TPM do banco de dados de recuperação. Mensagem: {Message}-ou-</p>
<p><strong>QueryDriveRecoveryData </strong> : ocorreu um erro ao obter dados de recuperação de unidade do banco de dados. Mensagem: {Message}-ou-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : ocorreu um erro ao obter as IDs da chave de recuperação do banco de dados. Mensagem: {Message}-ou-</p>
<p><strong>QueryVolumeUsers </strong> : ocorreu um erro ao obter as informações do usuário a partir do banco de dados.</p></td>
<td align="left"><p>Essa mensagem é registrada sempre que há uma exceção durante a comunicação com o banco de dados de recuperação do MBAM. Leia as informações contidas no rastreamento para obter detalhes específicos sobre a exceção.</p>
<p>Para obter as etapas de solução de problemas detalhadas, consulte o artigo do TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> como solucionar problemas de conexão com o mecanismo de banco de dados do SQL Server </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>101</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/administrador</p></td>
<td align="left"><p>AdminServiceComplianceDbError</p></td>
<td align="left"><p><strong>GetRecoveryKey </strong> : ocorreu um erro ao registrar um evento de auditoria no banco de dados de conformidade. Mensagem: {Message}-ou-</p>
<p><strong>GetRecoveryKeyIds </strong> : ocorreu um erro ao registrar um evento de auditoria no banco de dados de conformidade. Mensagem: {Message}-ou-</p>
<p><strong>GetTpmHashForUser </strong> : ocorreu um erro ao registrar um evento de auditoria no banco de dados de conformidade. Mensagem: {Message}-ou-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : ocorreu um erro ao registrar um evento de auditoria no banco de dados de conformidade. Mensagem: {Message}-ou-</p>
<p><strong>QueryDriveRecoveryData </strong> : ocorreu um erro ao registrar um evento de auditoria no banco de dados de conformidade. Mensagem: {Message}</p></td>
<td align="left"><p>Essa mensagem é registrada sempre que há uma exceção ao comunicar o banco de dados de conformidade do MBAM. Leia as informações contidas no rastreamento para obter detalhes específicos sobre a exceção.</p>
<p>Para obter as etapas de solução de problemas detalhadas, consulte o artigo do TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> como solucionar problemas de conexão com o mecanismo de banco de dados do SQL Server </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>102</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/administrador</p></td>
<td align="left"><p>AgentServiceRecoveryDbError</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Esta mensagem indica uma exceção quando o serviço de agente MBAM tenta se comunicar com o banco de dados de recuperação. Leia a mensagem contida no evento para obter informações específicas sobre a exceção.</p>
<p>Consulte o artigo do TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> como solucionar problemas de conexão com o mecanismo de banco de dados do SQL Server </a> para verificar se a conta do pool de aplicativos do MBAM tem as permissões necessárias para se conectar ou executar no banco de dados de recuperação do MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>103</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/administrador</p></td>
<td align="left"><p>AgentServiceError</p></td>
<td align="left"><p>Não é possível detectar uma conta de computador cliente ou uma conta de usuário de migração de dados. - ou -</p>
<p>A verificação da conta falhou para a identificação de chamadas.</p></td>
<td align="left"><p>Sempre que uma chamada é feita nos &quot; &quot; &quot; &quot; métodos da Web PostKeyRecoveryInfo, IsRecoveryKeyResetRequired, &quot; CommitRecoveryKeyRest &quot; ou &quot; GetTpmHash &quot; nos serviços de agente do MBAM, ele recupera o contexto do chamador para obter credenciais de chamadas. Se o contexto do chamador for nulo ou ficar vazio, o serviço do agente MBAM registrará &quot; não é possível detectar a conta de computador cliente ou a conta de usuário da migração de dados.&quot;</p>
<p>A verificação da conta da mensagem &quot; falhou para a identificação de chamadas &quot; será registrada se o método da Web estiver esperando que o chamador seja uma conta de computador e o chamador não seja uma conta de computador, ou se o método da Web estiver, exceto se o autor for uma conta de usuário, e o chamador não for uma conta de usuário ou membro da conta do grupo de migração de dados.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>104</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/administrador</p></td>
<td align="left"><p>StatusServiceComplianceDbConfigError</p></td>
<td align="left"><p>&quot;A cadeia de conexão do banco de dados de conformidade no registro está vazia.&quot;</p></td>
<td align="left"><p>Essa mensagem é registrada sempre que a cadeia de conexão do BD de conformidade é inválida.</p>
<p>Verifique o valor na chave do registro HKLM\Software\Microsoft\MBAM Server\Web\ComplianceDBConnectionString</p></td>
</tr>
<tr class="even">
<td align="left"><p>105</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/administrador</p></td>
<td align="left"><p>StatusServiceComplianceDbError</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Esse erro indica que os sites/serviços Web do MBAM não puderam se conectar ao banco de dados do MBAMCompliance.</p>
<p>Consulte o artigo do TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> como solucionar problemas de conexão com o mecanismo de banco de dados do SQL Server </a> para verificar se a conta do pool de aplicativos do IIS pode se conectar ao banco de dados de conformidade do MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>106</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/administrador</p></td>
<td align="left"><p>HelpdeskError</p></td>
<td align="left"><p>A solicitação para URL {URL} causou um erro interno. - ou -</p>
<p>Ocorreu um erro ao obter informações de contexto de execução. Não é possível verificar o registro SPN (nome da entidade de serviço). - ou -</p>
<p>Ocorreu um erro ao verificar o registro SPN (nome da entidade de serviço).</p></td>
<td align="left"><p>Indica que uma exceção não tratada foi gerada no aplicativo helpdesk. Examine as entradas do log no canal operacional do administrador do MBAM para encontrar a exceção específica. or</p>
<p>Durante a operação de carregamento do website da assistência técnica inicial, uma verificação de SPN é realizada. Para verificar o SPN, a assistência técnica requer as informações da conta de execução, o SiteName do IIS e o ApplicationVirtualPath correspondente ao website da assistência técnica. Essa mensagem de erro é registrada quando uma ou mais delas são inválidas ou ausentes. or</p>
<p>Essa mensagem indica que uma exceção de segurança é lançada ao executar a verificação de SPN. Consulte a exceção contida na seção detalhes do evento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>107</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/administrador</p></td>
<td align="left"><p>SelfServicePortalError</p></td>
<td align="left"><p>Ocorreu um erro ao obter a chave de recuperação para um usuário. EventDetails: {ExceptionMessage}-ou-</p>
<p>Ocorreu um erro ao obter informações de contexto de execução. Não é possível verificar o registro SPN (nome da entidade de serviço). EventDetails: User: {username Identity} Application: {SiteName\ApplicationVirtualPath}-ou-</p>
<p>Ocorreu um erro ao verificar o registro SPN (nome da entidade de serviço). EventDetails:{ExceptionMessage}</p></td>
<td align="left"><p>Indica que uma exceção inesperada foi gerada quando uma solicitação foi feita para recuperar a chave de recuperação. Consulte a mensagem de exceção contida na seção detalhes do evento. Se o rastreamento estiver habilitado no helpdesk do MBAM, consulte rastrear dados para obter mensagens de exceção detalhadas. or</p>
<p>Durante uma operação de carregamento inicial, o SSP (portal de autoatendimento) recupera as informações da conta de execução, do IIS SiteName e do ApplicationVirtualPath correspondente ao site de autoatendimento para verificar o SPN. Essa mensagem de erro é registrada quando um ou mais desses são inválidos. or</p>
<p>Esta mensagem indica que uma exceção de segurança foi gerada ao executar a verificação de SPN. Consulte a exceção contida na seção detalhes do evento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>108</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/administrador</p></td>
<td align="left"><p>DomainControllerError</p></td>
<td align="left"><p>Ocorreu um erro ao resolver o nome de domínio {DomainName}, ocorreu uma falha na alocação de memória. - ou -</p>
<p>Não foi possível invocar o método DsGetDcName. EventDetails:{ExceptionMessage}</p></td>
<td align="left"><p>Para resolver o nome de domínio, o MBAM aproveita a &quot; API DsGetDcName do &quot; Windows. Essa mensagem é registrada quando &quot; DsGetDcName &quot; retorna &quot; ERROR_NOT_ENOUGH_MEMORY &quot; indicando uma falha de alocação de memória. or</p>
<p>Esta mensagem indica que &quot; o &quot; método de API DsGetDcName não está disponível no sistema de hospedagem.</p></td>
</tr>
<tr class="even">
<td align="left"><p>109</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/administrador</p></td>
<td align="left"><p>WebAppRecoveryDbError</p></td>
<td align="left"><p>Ocorreu um erro ao ler a configuração do banco de dados de recuperação. A cadeia de conexão para o banco de dados de recuperação não está configurada. Mensagem: {Message}-ou-</p>
<p><strong>DoesUserHaveMatchingRecoveryKey </strong> : ocorreu um erro ao obter IDs de chave de recuperação para um usuário. Mensagem: {Message}-ou-</p>
<p><strong>QueryDriveRecoveryData </strong> : ocorreu um erro ao obter dados de recuperação de unidade. Mensagem: {Message}-ou-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : ocorreu um erro ao obter IDs de chave de recuperação para um usuário. Mensagem: {Message}-ou-</p>
<p>Ocorreu um erro ao obter hash de senha de TPM do banco de dados de recuperação. EventDetails:{ExceptionMessage}</p></td>
<td align="left"><p>Esta mensagem indica que as informações da cadeia de conexão do banco de dados de recuperação em &quot; HKLM\Software\Microsoft\MBAM Server\Web\RecoveryDBConnectionString &quot; são inválidas. Verifique o valor de chave do registro fornecido. or</p>
<p>Se qualquer uma das mensagens restantes for registrada, consulte as etapas de solução de problemas listadas no artigo do TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> como solucionar problemas de conexão com o mecanismo de banco de dados do SQL Server </a> para verificar se uma conexão pode ser feita ao banco de dados de recuperação do MBAM a partir do servidor do IIS usando credenciais do pool de aplicativos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>110</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/administrador</p></td>
<td align="left"><p>WebAppComplianceDbError</p></td>
<td align="left"><p>Ocorreu um erro ao ler a configuração do banco de dados de conformidade. A cadeia de conexão para o banco de dados de conformidade não está configurada. - ou -</p>
<p><strong>GetRecoveryKeyForCurrentUser </strong> : ocorreu um erro ao registrar um evento de auditoria no banco de dados de conformidade. Mensagem: {Message}-ou-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : ocorreu um erro ao registrar um evento de auditoria no banco de dados de conformidade. Mensagem: {Message}-ou-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : ocorreu um erro ao registrar um evento de auditoria no banco de dados de conformidade. Mensagem: {Message}</p></td>
<td align="left"><p>Esta mensagem indica que as informações da cadeia de conexão do BD de conformidade em &quot; HKLM\Software\Microsoft\MBAM Server\Web\ComplianceDBConnectionString &quot; são inválidas. Verifique o valor correspondente à chave do registro acima. or</p>
<p>Se qualquer uma das mensagens restantes for registrada, consulte as etapas de solução de problemas listadas no artigo do TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> como solucionar problemas de conexão com o mecanismo de banco de dados do SQL Server </a> para verificar se uma conexão pode ser feita ao banco de dados de conformidade do MBAM a partir do servidor do IIS usando as credenciais do pool de aplicativos.</p></td>
</tr>
<tr class="even">
<td align="left"><p>111</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/administrador</p></td>
<td align="left"><p>WebAppDbError</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Esses erros indicam uma das duas condições a seguir</p>
<ul>
<li><p>Os sites/WebServices da MBAM não puderam se conectar ao banco de dados do MBAMCompliance ou do MBAMRecovery</p></li>
<li><p>Conta de execução de sites/WebServices da MBAM (conta do pool de aplicativos) não pôde executar o procedimento armazenado do GetVersion no banco de dados do MBAMCompliance ou MBAMRecovery</p></li>
</ul>
<p>A mensagem contida no evento irá fornecer mais detalhes sobre a exceção.</p>
<p>Consulte as etapas de solução de problemas listadas no artigo do TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> como solucionar problemas de conexão com o mecanismo de banco de dados do SQL Server </a> para verificar se a conta de execução do MBAM (conta do pool de aplicativos) pode se conectar ao banco de dados de conformidade/recuperação do MBAM e tem permissões para executar o procedimento armazenado do GetVersion.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>112</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/administrador</p></td>
<td align="left"><p>WebAppError</p></td>
<td align="left"><p>Ocorreu um erro ao verificar o registro SPN (nome da entidade de serviço). EventDetails:{ExceptionMessage}</p></td>
<td align="left"><p>Para executar a verificação de SPN, o MBAM consulta o Active Directory para recuperar uma lista de SPNs mapeado conta de execução. O MBAM também consulta o &quot;ApplicationHost.config&quot; para obter associações de site do MBAM. Essa mensagem de erro indica que o MBAM não pôde se comunicar com o Active Directory ou não pôde carregar o arquivo applicationHost.config.</p>
<p>Verifique se a conta de execução (conta do pool de aplicativos) tem permissões para consultar o anúncio ou o arquivo de ApplicationHost.config. Verifique também as entradas de associação de site no arquivo ApplicationHost.config.</p></td>
</tr>
<tr class="even">
<td align="left"><p>200</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/operacional</p></td>
<td align="left"><p>HelpDeskInformation</p></td>
<td align="left"><p>O aplicativo de site de administração foi encontrado com êxito e conectado a uma versão com suporte do banco de dados de recuperação. - ou -</p>
<p>O aplicativo de site de administração foi encontrado com êxito e conectado a uma versão do banco de dados de conformidade com suporte.</p></td>
<td align="left"><p>Indica a conexão com êxito com o banco de dados de recuperação/conformidade do website da assistência técnica da MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>201</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/operacional</p></td>
<td align="left"><p>SelfServicePortalInformation</p></td>
<td align="left"><p>O aplicativo do portal de autoatendimento foi encontrado e conectado com êxito a uma versão do banco de dados de recuperação com suporte. - ou -</p>
<p>O aplicativo do portal de autoatendimento foi encontrado e conectado com êxito a uma versão do banco de dados de conformidade com suporte.</p></td>
<td align="left"><p>Indica a conexão com êxito com o banco de dados de recuperação/conformidade do portal de autoatendimento do MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>202</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/operacional</p></td>
<td align="left"><p>WebAppInformation</p></td>
<td align="left"><p>O aplicativo tem seus SPNs registrados corretamente.</p></td>
<td align="left"><p>Indica que os SPNs necessários para o site da assistência técnica MBAM estão registrados corretamente na conta em execução.</p></td>
</tr>
</tbody>
</table>

 


## Tópicos relacionados


[Referência técnica do MBAM 2.5](technical-reference-for-mbam-25.md)

[Logs de eventos do cliente](client-event-logs.md)

 
## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





