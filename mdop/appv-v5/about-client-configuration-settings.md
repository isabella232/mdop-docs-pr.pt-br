---
title: Sobre as configurações do cliente
description: Sobre as configurações do cliente
author: dansimp
ms.assetid: cc7ae28c-b2ac-4f68-b992-5ccdbd5316a4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 289f5b35ac223d488152ff7ee1f42b1cf50341df
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796625"
---
# Sobre as configurações do cliente


O cliente Microsoft Application Virtualization (App-V) 5,0 armazena sua configuração no registro. Você pode coletar algumas informações úteis sobre o cliente se compreender o formato dos dados no registro. Você também pode configurar várias ações do cliente alterando as entradas do registro. Este tópico lista as configurações de cliente do App-V 5,0 e explica seus usos. Você pode usar o PowerShell para modificar as configurações de configuração do cliente. Para obter mais informações sobre como usar o PowerShell e o App-V 5,0 [, consulte Administrando o app-v usando o PowerShell](administering-app-v-by-using-powershell.md).

## <a href="" id="---------app-v-5-0-client-configuration-settings"></a> Configurações de cliente do App-V 5,0


A tabela a seguir exibe informações sobre as definições de configuração do cliente do App-V 5,0:

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da configuração</th>
<th align="left">Sinalizador de configuração</th>
<th align="left">Descrição</th>
<th align="left">Opções de configuração</th>
<th align="left">Valor da chave do registro</th>
<th align="left">Chaves e valores de estado de política desabilitados</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>PackageInstallationRoot</p></td>
<td align="left"><p>PACKAGEINSTALLATIONROOT</p></td>
<td align="left"><p>Especifica o diretório onde todos os novos aplicativos e atualizações serão instalados.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Streaming\PackageInstallationRoot</p></td>
<td align="left"><p>Valor da política não gravado (igual a não configurado)</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageSourceRoot</p></td>
<td align="left"><p>PACKAGESOURCEROOT</p></td>
<td align="left"><p>Substitui o local de origem para baixar o conteúdo do pacote.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Streaming\PackageSourceRoot</p></td>
<td align="left"><p>Valor da política não gravado (igual a não configurado)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AllowHighCostLaunch</p></td>
<td align="left"><p>Não está disponível.</p></td>
<td align="left"><p>Esta configuração controla se os aplicativos virtualizados são iniciados em máquinas Windows 8 conectadas por meio de uma conexão de rede limitada (por exemplo, 4G).</p></td>
<td align="left"><p>Verdadeiro (habilitado); Falso (estado desabilitado)</p></td>
<td align="left"><p>Streaming\AllowHighCostLaunch</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReestablishmentRetries</p></td>
<td align="left"><p>Não está disponível.</p></td>
<td align="left"><p>Especifica o número de vezes para tentar uma sessão descartada novamente.</p></td>
<td align="left"><p>Inteiro (0-99)</p></td>
<td align="left"><p>Streaming\ReestablishmentRetries</p></td>
<td align="left"><p>Valor da política não gravado (igual a não configurado)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReestablishmentInterval</p></td>
<td align="left"><p>Não está disponível.</p></td>
<td align="left"><p>Especifica o número de segundos entre tentativas para restabelecer uma sessão interrompida.</p></td>
<td align="left"><p>Inteiro (0-3600)</p></td>
<td align="left"><p>Streaming\ReestablishmentInterval</p></td>
<td align="left"><p>Valor da política não gravado (igual a não configurado)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Carregar</p></td>
<td align="left"><p>CARREGAR</p></td>
<td align="left"><p>Especifica como novos pacotes devem ser carregados automaticamente pelo App-V em um computador específico.</p></td>
<td align="left"><p>(0x0) nenhum; (0x1) usado anteriormente; (0x2) todos</p></td>
<td align="left"><p>Streaming\AutoLoad</p></td>
<td align="left"><p>Valor da política não gravado (igual a não configurado)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalProvider</p></td>
<td align="left"><p>Não está disponível.</p></td>
<td align="left"><p>Especifica o CLSID para uma implementação compatível da interface IAppvPackageLocationProvider.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Streaming\LocationProvider</p></td>
<td align="left"><p>Valor da política não gravado (igual a não configurado)</p></td>
</tr>
<tr class="even">
<td align="left"><p>CertFilterForClientSsl</p></td>
<td align="left"><p>Não está disponível.</p></td>
<td align="left"><p>Especifica o caminho para um certificado válido no repositório de certificados.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Streaming\CertFilterForClientSsl</p></td>
<td align="left"><p>Valor da política não gravado (igual a não configurado)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>VerifyCertificateRevocationList</p></td>
<td align="left"><p>Não está disponível.</p></td>
<td align="left"><p>Verifica o status da revogação do certificado do servidor antes do fluxo usando HTTPS.</p></td>
<td align="left"><p>Verdadeiro (habilitado); Falso (estado desabilitado)</p></td>
<td align="left"><p>Streaming\VerifyCertificateRevocationList</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="even">
<td align="left"><p>SharedContentStoreMode</p></td>
<td align="left"><p>SHAREDCONTENTSTOREMODE</p></td>
<td align="left"><p>Especifica que o conteúdo do pacote em fluxo não será salvo no disco rígido local.</p></td>
<td align="left"><p>Verdadeiro (habilitado); Falso (estado desabilitado)</p></td>
<td align="left"><p>Streaming\SharedContentStoreMode</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome</p>
<div class="alert">
<strong>Observação</strong><br/><p>Esta configuração não pode ser modificada usando o <strong> cmdLet Set-AppvclientConfiguration </strong> . Você deve usar o <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>PUBLISHINGSERVERNAME</p></td>
<td align="left"><p>Exibe o nome do servidor de publicação.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Publishing\Servers {serverID} \ FriendlyName</p></td>
<td align="left"><p>Valor da política não gravado (igual a não configurado)</p></td>
</tr>
<tr class="even">
<td align="left"><p>URL</p>
<div class="alert">
<strong>Observação</strong><br/><p>Esta configuração não pode ser modificada usando o <strong> cmdLet Set-AppvclientConfiguration </strong> . Você deve usar o <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>PUBLISHINGSERVERURL</p></td>
<td align="left"><p>Exibe a URL do Publishing Server.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Publishing\Servers {serverID} \ URL</p></td>
<td align="left"><p>Valor da política não gravado (igual a não configurado)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GlobalRefreshEnabled</p>
<div class="alert">
<strong>Observação</strong><br/><p>Esta configuração não pode ser modificada usando o <strong> cmdLet Set-AppvclientConfiguration </strong> . Você deve usar o <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHENABLED</p></td>
<td align="left"><p>Habilita a atualização de publicação global (booliano)</p></td>
<td align="left"><p>Verdadeiro (habilitado); Falso (estado desabilitado)</p></td>
<td align="left"><p>Publishing\Servers {serverID} \ GlobalEnabled</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalRefreshOnLogon</p>
<div class="alert">
<strong>Observação</strong><br/><p>Esta configuração não pode ser modificada usando o <strong> cmdLet Set-AppvclientConfiguration </strong> . Você deve usar o <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHONLOGON</p></td>
<td align="left"><p>Dispara uma atualização de publicação global ao fazer logon. Booliana</p></td>
<td align="left"><p>Verdadeiro (habilitado); Falso (estado desabilitado)</p></td>
<td align="left"><p>Publishing\Servers {serverID} \ GlobalLogonRefresh</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GlobalRefreshInterval</p>
<div class="alert">
<strong>Observação</strong><br/><p>Esta configuração não pode ser modificada usando o <strong> cmdLet Set-AppvclientConfiguration </strong> . Você deve usar o <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHINTERVAL  </p></td>
<td align="left"><p>Especifica o intervalo de atualização de publicação usando GlobalRefreshIntervalUnit. Para desabilitar a atualização do pacote, selecione 0.</p></td>
<td align="left"><p>Inteiro (0-744</p></td>
<td align="left"><p>Publishing\Servers {serverID} \ GlobalPeriodicRefreshInterval</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalRefreshIntervalUnit</p>
<div class="alert">
<strong>Observação</strong><br/><p>Esta configuração não pode ser modificada usando o <strong> cmdLet Set-AppvclientConfiguration </strong> . Você deve usar o <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHINTERVALUNI</p></td>
<td align="left"><p>Especifica a unidade de intervalo (hora 0-23, dia 0-31). </p></td>
<td align="left"><p>0 para hora, 1 para dia</p></td>
<td align="left"><p>Publishing\Servers {serverID} \ GlobalPeriodicRefreshIntervalUnit</p></td>
<td align="left"><p>um</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UserRefreshEnabled</p>
<div class="alert">
<strong>Observação</strong><br/><p>Esta configuração não pode ser modificada usando o <strong> cmdLet Set-AppvclientConfiguration </strong> . Você deve usar o <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHENABLED </p></td>
<td align="left"><p>Habilita a atualização da publicação do usuário (booliano)</p></td>
<td align="left"><p>Verdadeiro (habilitado); Falso (estado desabilitado)</p></td>
<td align="left"><p>Publishing\Servers {serverID} \ UserEnabled</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>UserRefreshOnLogon</p>
<div class="alert">
<strong>Observação</strong><br/><p>Esta configuração não pode ser modificada usando o <strong> cmdLet Set-AppvclientConfiguration </strong> . Você deve usar o <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHONLOGON</p></td>
<td align="left"><p>Dispara uma atualização de publicação do usuário ONLOGON. Booliana</p>
<p>Contagem de palavras (com espaços): 60</p></td>
<td align="left"><p>Verdadeiro (habilitado); Falso (estado desabilitado)</p></td>
<td align="left"><p>Publishing\Servers {serverID} \ UserLogonRefresh</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UserRefreshInterval</p>
<div class="alert">
<strong>Observação</strong><br/><p>Esta configuração não pode ser modificada usando o <strong> cmdLet Set-AppvclientConfiguration </strong> . Você deve usar o <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHINTERVAL     </p></td>
<td align="left"><p>Especifica o intervalo de atualização de publicação usando UserRefreshIntervalUnit. Para desabilitar a atualização do pacote, selecione 0.</p>
<p>Contagem de palavras (com espaços): 85</p></td>
<td align="left"><p>Integer (0-744 horas)</p></td>
<td align="left"><p>Publishing\Servers {serverID} \ UserPeriodicRefreshInterval</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="even">
<td align="left"><p>UserRefreshIntervalUnit</p>
<div class="alert">
<strong>Observação</strong><br/><p>Esta configuração não pode ser modificada usando o <strong> cmdLet Set-AppvclientConfiguration </strong> . Você deve usar o <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHINTERVALUNIT  </p></td>
<td align="left"><p>Especifica a unidade de intervalo (hora 0-23, dia 0-31). </p></td>
<td align="left"><p>0 para hora, 1 para dia</p></td>
<td align="left"><p>Publishing\Servers {serverID} \ UserPeriodicRefreshIntervalUnit</p></td>
<td align="left"><p>um</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Migrationmode</p></td>
<td align="left"><p>MIGRATIONmode</p></td>
<td align="left"><p>O modo de migração permite que o cliente App-V modifique atalhos e FTA de pacotes criados usando uma versão anterior do App-V.</p></td>
<td align="left"><p>Verdadeiro (estado habilitado); Falso (estado desabilitado)</p></td>
<td align="left"><p>Coexistence\MigrationMode</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>CEIPOPTIN</p></td>
<td align="left"><p>CEIPOPTIN</p></td>
<td align="left"><p>Permite que o computador executando o cliente App-V 5,0 colete e retorne determinadas informações de uso para que possamos melhorar ainda mais o aplicativo.</p></td>
<td align="left"><p>0 para desabilitado; 1 para habilitado</p></td>
<td align="left"><p>SOFTWARE/Microsoft/AppV/CEIP/CEIPEnable</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="odd">
<td align="left"><p>EnablePackageScripts</p></td>
<td align="left"><p>ENABLEPACKAGESCRIPTS</p></td>
<td align="left"><p>Habilita scripts definidos no manifesto do pacote de arquivos de configuração que devem ser executados.</p></td>
<td align="left"><p>Verdadeiro (habilitado); Falso (estado desabilitado)</p></td>
<td align="left"><p>\Scripting\EnablePackageScripts</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>RoamingFileExclusions</p></td>
<td align="left"><p>ROAMINGFILEEXCLUSIONS</p></td>
<td align="left"><p>Especifica os caminhos de arquivo relativos a% USERPROFILE% que não fazem roaming com um perfil de usuário&#39;s. Exemplo de uso:/ROAMINGFILEEXCLUSIONS =&#39;área de trabalho; minhas imagens&#39;</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>RoamingRegistryExclusions</p></td>
<td align="left"><p>ROAMINGREGISTRYEXCLUSIONS</p></td>
<td align="left"><p>Especifica os caminhos do registro que não fazem roaming com um perfil de usuário. Exemplo de uso:/ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Integration\RoamingRegistryExclusions</p></td>
<td align="left"><p>Valor da política não gravado (igual a não configurado)</p></td>
</tr>
<tr class="even">
<td align="left"><p>IntegrationRootUser</p></td>
<td align="left"><p>Não está disponível.</p></td>
<td align="left"><p>Especifica o local para criar links simbólicos associados à versão atual de um pacote publicado por usuário. todas as extensões de aplicativo virtual, por exemplo, atalhos e associações de tipo de arquivo, apontarão para esse caminho. Se você não especificar um caminho, os links simbólicos não serão usados quando você publicar o pacote. Por exemplo:%localappdata%\Microsoft\AppV\Client\Integration.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Integration\IntegrationRootUser</p></td>
<td align="left"><p>Valor da política não gravado (igual a não configurado)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IntegrationRootGlobal</p></td>
<td align="left"><p>Não está disponível.</p></td>
<td align="left"><p>Especifica o local para criar links simbólicos associados à versão atual de um pacote publicado globalmente. todas as extensões de aplicativo virtual, por exemplo, atalhos e associações de tipo de arquivo, apontarão para esse caminho. Se você não especificar um caminho, os links simbólicos não serão usados quando você publicar o pacote. Por exemplo:%allusersprofile%\Microsoft\AppV\Client\Integration</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Integration\IntegrationRootGlobal</p></td>
<td align="left"><p>Valor da política não gravado (igual a não configurado)</p></td>
</tr>
<tr class="even">
<td align="left"><p>VirtualizableExtensions</p></td>
<td align="left"><p>Não está disponível.</p></td>
<td align="left"><p>Uma lista delineada por vírgulas de extensões de nome de arquivo que podem ser usadas para determinar se um aplicativo instalado localmente pode ser executado no ambiente virtual.</p>
<p>Quando os atalhos, FTAs e outros pontos de extensão forem criados durante a publicação, o App-V irá comparar a extensão de nome de arquivo com a lista se o aplicativo associado ao ponto de extensão for instalado localmente. Se a extensão for localizada, o <strong> </strong> parâmetro de linha de comando RunVirtual será adicionado, e o aplicativo será executado virtualmente.</p>
<p>Para obter mais informações sobre <strong> o </strong> parâmetro RunVirtual, consulte <a href="running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md" data-raw-source="[Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)"> executando um aplicativo instalado localmente dentro de um ambiente virtual com aplicativos virtualizados </a> .</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Integration\VirtualizableExtensions</p></td>
<td align="left"><p>Valor da política não escrito</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingEnabled</p></td>
<td align="left"><p>Não está disponível.</p></td>
<td align="left"><p>Permite que o cliente retorne informações para um servidor de relatórios.</p></td>
<td align="left"><p>Verdadeiro (habilitado); Falso (estado desabilitado)</p></td>
<td align="left"><p>Reporting\EnableReporting</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReportingServerURL</p></td>
<td align="left"><p>Não está disponível.</p></td>
<td align="left"><p>Especifica o local no servidor de relatório onde as informações do cliente são salvas.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Reporting\ReportingServer</p></td>
<td align="left"><p>Valor da política não gravado (igual a não configurado)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingDataCacheLimit</p></td>
<td align="left"><p>Não está disponível.</p></td>
<td align="left"><p>Especifica o tamanho máximo em megabytes (MB) do cache XML para armazenar informações de relatório. O tamanho se aplica ao cache na memória. Quando o limite for atingido, o arquivo de log será revertido. Definido entre 0 e 1024.</p></td>
<td align="left"><p>Inteiro [0-1024]</p></td>
<td align="left"><p>Reporting\DataCacheLimit</p></td>
<td align="left"><p>Valor da política não gravado (igual a não configurado)</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReportingDataBlockSize</p></td>
<td align="left"><p>Não está disponível.</p></td>
<td align="left"><p>Especifica o tamanho máximo em bytes a ser transmitido para o servidor para relatar solicitações de carregamento. Isso pode ajudar a evitar falhas de transmissão permanente quando o log atingir um tamanho significativo. Definido entre 1024 e ilimitado.</p></td>
<td align="left"><p>Inteiro [1024-ilimitado]</p></td>
<td align="left"><p>Reporting\DataBlockSize</p></td>
<td align="left"><p>Valor da política não gravado (igual a não configurado)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingStartTime</p></td>
<td align="left"><p>Não está disponível.</p></td>
<td align="left"><p>Especifica o tempo de início do cliente para enviar dados ao servidor de relatórios. Você deve especificar um inteiro válido entre 0-23 correspondente à hora do dia. Por padrão, o <strong> ReportingStartTime </strong> começará no dia atual em 10 P. M ou 22.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Você deve definir essa configuração para um horário em que os computadores que executam o cliente App-V 5,0 têm menos probabilidade de ficar offline.</p>
</div>
<div>

</div></td>
<td align="left"><p>Inteiro (0 – 23)</p></td>
<td align="left"><p>Relatórios \ StartTime</p></td>
<td align="left"><p>Valor da política não gravado (igual a não configurado)</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReportingInterval</p></td>
<td align="left"><p>Não está disponível.</p></td>
<td align="left"><p>Especifica o intervalo de repetição que o cliente usará para reenviar dados ao servidor de relatórios.</p></td>
<td align="left"><p>Inteiro</p></td>
<td align="left"><p>Reporting\RetryInterval</p></td>
<td align="left"><p>Valor da política não gravado (igual a não configurado)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingRandomDelay</p></td>
<td align="left"><p>Não está disponível.</p></td>
<td align="left"><p>Especifica o atraso máximo (em minutos) dos dados a serem enviados para o servidor de relatórios. Quando a tarefa agendada for iniciada, o cliente gerará um atraso aleatório entre 0 e <strong> ReportingRandomDelay </strong> e esperará a duração especificada antes de enviar os dados. Isso pode ajudar a evitar colisões no servidor.</p></td>
<td align="left"><p>Inteiro [0-ReportingRandomDelay]</p></td>
<td align="left"><p>Reporting\RandomDelay</p></td>
<td align="left"><p>Valor da política não gravado (igual a não configurado)</p></td>
</tr>
<tr class="even">
<td align="left"><p>EnableDynamicVirtualization</p>
<div class="alert">
<strong>Importante</strong><br/><p>Essa configuração está disponível somente com o App-V 5,0 SP2 ou posterior.</p>
</div>
<div>

</div></td>
<td align="left"><p>Não está disponível.</p></td>
<td align="left"><p>Habilita as extensões do shell com suporte, os objetos auxiliares do navegador e os controles ActiveX para serem virtualizados e executados com aplicativos virtuais.</p></td>
<td align="left"><p>1 (habilitado), 0 (desabilitado)</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Virtualization</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>EnablePublishingRefreshUI</p>
<div class="alert">
<strong>Importante</strong><br/><p>Essa configuração está disponível somente com o App-V 5,0 SP2.</p>
</div>
<div>

</div></td>
<td align="left"><p>Não está disponível.</p></td>
<td align="left"><p>Habilita a barra de progresso de atualização de publicação do computador que executa o cliente App-V 5,0.</p></td>
<td align="left"><p>1 (habilitado), 0 (desabilitado)</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Publishing</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>HideUI</p>
<div class="alert">
<strong>Importante</strong><br/><p>Essa configuração está disponível somente com o App-V 5,0 SP2.</p>
</div>
<div>

</div></td>
<td align="left"><p>Não está disponível.</p></td>
<td align="left"><p>Oculta a barra de progresso de atualização de publicação.</p></td>
<td align="left"><p>1 (habilitado), 0 (desabilitado)</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>ProcessesUsingVirtualComponents</p></td>
<td align="left"><p>Não está disponível.</p></td>
<td align="left"><p>Especifica uma lista de caminhos de processo (que podem conter caracteres curinga), que são candidatos ao uso de virtualização dinâmica (extensões do shell com suporte, objetos auxiliares do navegador e controles ActiveX). Somente os processos cujo caminho completo corresponde a um desses itens podem usar a virtualização dinâmica.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Virtualization\ProcessesUsingVirtualComponents</p></td>
<td align="left"><p>Cadeia de caracteres vazia.</p></td>
</tr>
</tbody>
</table>








## Tópicos relacionados


[Implantação do sequenciador e do cliente App-V 5.0](deploying-the-app-v-50-sequencer-and-client.md)

[Como modificar a configuração do cliente App-V 5.0 usando o modelo ADMX e a Política de Grupo](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

[Como implantar o cliente do App-V](how-to-deploy-the-app-v-client-gb18030.md)









