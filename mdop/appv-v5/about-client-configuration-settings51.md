---
title: Sobre as configurações do cliente
description: Sobre as configurações do cliente
author: dansimp
ms.assetid: 18bb307a-7eda-4dd6-a83e-6afaefd99470
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fb547eedf63bf165b1e8f5fd024839b3c2af3e4c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796626"
---
# Sobre as configurações do cliente


O cliente Microsoft Application Virtualization (App-V) 5,1 armazena sua configuração no registro. Você pode coletar algumas informações úteis sobre o cliente se compreender o formato dos dados no registro. Você também pode configurar várias ações do cliente alterando as entradas do registro. Este tópico lista as configurações de cliente do App-V 5,1 e explica seus usos. Você pode usar o PowerShell para modificar as configurações de configuração do cliente. Para obter mais informações sobre como usar o PowerShell e o App-V 5,1 [, consulte Administrando o app-v 5,1 usando o PowerShell](administering-app-v-51-by-using-powershell.md).

## <a href="" id="---------app-v-5-1-client-configuration-settings"></a> Configurações de cliente do App-V 5,1


A tabela a seguir exibe informações sobre as definições de configuração do cliente do App-V 5,1:

|Nome da configuração | Sinalizador de configuração | Descrição | Opções de configuração | Valor da chave do registro | Chaves e valores de estado de política desabilitados |
|-------------|------------|-------------|-----------------|--------------------|--------------------------------------|
| PackageInstallationRoot | PACKAGEINSTALLATIONROOT | Especifica o diretório onde todos os novos aplicativos e atualizações serão instalados. | String | Streaming\PackageInstallationRoot | Valor da política não gravado (igual a não configurado) |
| PackageSourceRoot | PACKAGESOURCEROOT | Substitui o local de origem para baixar o conteúdo do pacote. | String | Streaming\PackageSourceRoot | Valor da política não gravado (igual a não configurado) |
| AllowHighCostLaunch | Não está disponível. |Esta configuração controla se os aplicativos virtualizados são iniciados em máquinas Windows 10 conectadas por meio de uma conexão de rede limitada (por exemplo, 4G). | Verdadeiro (habilitado); Falso (estado desabilitado) | Streaming\AllowHighCostLaunch | 0 |
| ReestablishmentRetries | Não está disponível. | Especifica o número de vezes para tentar uma sessão descartada novamente. | Inteiro (0-99) | Streaming\ReestablishmentRetries | Valor da política não gravado (igual a não configurado) |
| ReestablishmentInterval | Não está disponível. | Especifica o número de segundos entre tentativas para restabelecer uma sessão interrompida. | Inteiro (0-3600) | Streaming\ReestablishmentInterval | Valor da política não gravado (igual a não configurado) |
| LocalProvider | Não está disponível. | Especifica o CLSID para uma implementação compatível da interface IAppvPackageLocationProvider. | String | Streaming\LocationProvider | Valor da política não gravado (igual a não configurado) |
| CertFilterForClientSsl | Não está disponível. | Especifica o caminho para um certificado válido no repositório de certificados. | String | Streaming\CertFilterForClientSsl | Valor da política não gravado (igual a não configurado) |
| VerifyCertificateRevocationList | Não está disponível. | Verifica o status da revogação do certificado do servidor antes do fluxo usando HTTPS. | Verdadeiro (habilitado); Falso (estado desabilitado) | Streaming\VerifyCertificateRevocationList | 0 |
| SharedContentStoreMode | SHAREDCONTENTSTOREMODE | Especifica que o conteúdo do pacote em fluxo não será salvo no disco rígido local. | Verdadeiro (habilitado); Falso (estado desabilitado) | Streaming\SharedContentStoreMode | 0 |
| Nome<br>**Observação** Esta configuração não pode ser modificada usando o cmdLet **set-AppvclientConfiguration** . Você deve usar o cmdlet **set-AppvPublishingServer** . | PUBLISHINGSERVERNAME | Exibe o nome do servidor de publicação. | String | Publishing\Servers\ {serverID} \ FriendlyName | Valor da política não gravado (igual a não configurado) |
| URL<br>**Observação** Esta configuração não pode ser modificada usando o cmdLet **set-AppvclientConfiguration** . Você deve usar o cmdlet **set-AppvPublishingServer** . | PUBLISHINGSERVERURL | Exibe a URL do Publishing Server. | String | Publishing\Servers\ {serverID} \ URL | Valor da política não gravado (igual a não configurado) |
| GlobalRefreshEnabled<br>**Observação** Esta configuração não pode ser modificada usando o cmdLet **set-AppvclientConfiguration** . Você deve usar o cmdlet **set-AppvPublishingServer** . | GLOBALREFRESHENABLED | Habilita a atualização de publicação global (booliano) | Verdadeiro (habilitado); Falso (estado desabilitado) | Publishing\Servers\ {serverID} \ GlobalEnabled | False |
| GlobalRefreshOnLogon<br>**Observação** Esta configuração não pode ser modificada usando o cmdLet **set-AppvclientConfiguration** . Você deve usar o cmdlet **set-AppvPublishingServer** . | GLOBALREFRESHONLOGON | Dispara uma atualização de publicação global ao fazer logon. Booliana | Verdadeiro (habilitado); Falso (estado desabilitado) | Publishing\Servers\ {serverID} \ GlobalLogonRefresh | False |
| GlobalRefreshInterval<br>**Observação** Esta configuração não pode ser modificada usando o cmdLet **set-AppvclientConfiguration** . Você deve usar o cmdlet **set-AppvPublishingServer** . | GLOBALREFRESHINTERVAL | Especifica o intervalo de atualização de publicação usando GlobalRefreshIntervalUnit. Para desabilitar a atualização do pacote, selecione 0. | Inteiro (0-744) | Publishing\Servers\ {serverID} \ GlobalPeriodicRefreshInterval | 0 |
| GlobalRefreshIntervalUnit <br>**Observação** Esta configuração não pode ser modificada usando o cmdLet **set-AppvclientConfiguration** . Você deve usar o cmdlet **set-AppvPublishingServer** . | GLOBALREFRESHINTERVALUNI | Especifica a unidade de intervalo (hora 0-23, dia 0-31). | 0 para hora, 1 para dia | Publishing\Servers\ {serverID} \ GlobalPeriodicRefreshIntervalUnit | um |
| UserRefreshEnabled<br>**Observação** Esta configuração não pode ser modificada usando o cmdLet **set-AppvclientConfiguration** . Você deve usar o cmdlet **set-AppvPublishingServer** . | USERREFRESHENABLED | Habilita a atualização da publicação do usuário (booliano) | Verdadeiro (habilitado); Falso (estado desabilitado) | Publishing\Servers\ {serverID} \ UserEnabled | False |
| UserRefreshOnLogon<br>**Observação** Esta configuração não pode ser modificada usando o cmdLet **set-AppvclientConfiguration** . Você deve usar o cmdlet **set-AppvPublishingServer** . | USERREFRESHONLOGON | Dispara uma atualização de publicação do usuário ONLOGON. Booliana<br>Contagem de palavras (com espaços): 60 | Verdadeiro (habilitado); Falso (estado desabilitado) | Publishing\Servers\ {serverID} \ UserLogonRefresh | False |
| UserRefreshInterval<br>**Observação** Esta configuração não pode ser modificada usando o cmdLet **set-AppvclientConfiguration** . Você deve usar o cmdlet **set-AppvPublishingServer** . | USERREFRESHINTERVAL | Especifica o intervalo de atualização de publicação usando UserRefreshIntervalUnit. Para desabilitar a atualização do pacote, selecione 0. | Contagem de palavras (com espaços): 85<br>Integer (0-744 horas) | Publishing\Servers\ {serverID} \ UserPeriodicRefreshInterval | 0 |
| UserRefreshIntervalUnit<br>**Observação** Esta configuração não pode ser modificada usando o cmdLet **set-AppvclientConfiguration** . Você deve usar o cmdlet **set-AppvPublishingServer** . | USERREFRESHINTERVALUNIT | Especifica a unidade de intervalo (hora 0-23, dia 0-31). | 0 para hora, 1 para dia | Publishing\Servers\ {serverID} \ UserPeriodicRefreshIntervalUnit | um |
| Migrationmode | MIGRATIONmode | O modo de migração permite que o cliente App-V modifique atalhos e FTA de pacotes criados usando uma versão anterior do App-V. | Verdadeiro (estado habilitado); Falso (estado desabilitado) | Coexistence\MigrationMode | |
| CEIPOPTIN | CEIPOPTIN | Permite que o computador executando o cliente App-V 5,1 colete e retorne determinadas informações de uso para que possamos melhorar ainda mais o aplicativo. | 0 para desabilitado; 1 para habilitado | SOFTWARE/Microsoft/AppV/CEIP/CEIPEnable | 0 | 
| EnablePackageScripts | ENABLEPACKAGESCRIPTS | Habilita scripts definidos no manifesto do pacote de arquivos de configuração que devem ser executados. | Verdadeiro (habilitado); Falso (estado desabilitado) | \Scripting\EnablePackageScripts | | 
| RoamingFileExclusions | ROAMINGFILEEXCLUSIONS | Especifica os caminhos de arquivo relativos a% USERPROFILE% que não fazem roaming com um perfil de usuário. Exemplo de uso:/ROAMINGFILEEXCLUSIONS = ' área de trabalho; minhas imagens ' | | | |
| RoamingRegistryExclusions | ROAMINGREGISTRYEXCLUSIONS | Especifica os caminhos do registro que não fazem roaming com um perfil de usuário. Exemplo de uso:/ROAMINGREGISTRYEXCLUSIONS = software\\classes; software\\clients | String | Integration\RoamingRegistryExclusions | Valor da política não gravado (igual a não configurado) |
| IntegrationRootUser | Não está disponível. | Especifica o local para criar links simbólicos associados à versão atual de um pacote publicado por usuário. todas as extensões de aplicativo virtual, por exemplo, atalhos e associações de tipo de arquivo, apontarão para esse caminho. Se você não especificar um caminho, os links simbólicos não serão usados quando você publicar o pacote. Por exemplo:%localappdata%\Microsoft\AppV\Client\Integration.| String | Integration\IntegrationRootUser | Valor da política não gravado (igual a não configurado) |
|IntegrationRootGlobal | Não está disponível.| Especifica o local para criar links simbólicos associados à versão atual de um pacote publicado globalmente. todas as extensões de aplicativo virtual, por exemplo, atalhos e associações de tipo de arquivo, apontarão para esse caminho. Se você não especificar um caminho, os links simbólicos não serão usados quando você publicar o pacote. Por exemplo:%allusersprofile%\Microsoft\AppV\Client\Integration | String | Integration\IntegrationRootGlobal | Valor da política não gravado (igual a não configurado) |
| VirtualizableExtensions | Não está disponível. | Uma lista delineada por vírgulas de extensões de nome de arquivo que podem ser usadas para determinar se um aplicativo instalado localmente pode ser executado no ambiente virtual.<br>Quando os atalhos, FTAs e outros pontos de extensão forem criados durante a publicação, o App-V irá comparar a extensão de nome de arquivo com a lista se o aplicativo associado ao ponto de extensão for instalado localmente. Se a extensão for localizada, o parâmetro de linha de comando **RunVirtual** será adicionado, e o aplicativo será executado virtualmente.<br>Para obter mais informações sobre o parâmetro **RunVirtual** , consulte [executando um aplicativo instalado localmente dentro de um ambiente virtual com aplicativos virtualizados](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications51.md). | String | Integration\VirtualizableExtensions | Valor da política não escrito |
| ReportingEnabled | Não está disponível. | Permite que o cliente retorne informações para um servidor de relatórios. | Verdadeiro (habilitado); Falso (estado desabilitado) | Reporting\EnableReporting | False |
| ReportingServerURL | Não está disponível. | Especifica o local no servidor de relatório onde as informações do cliente são salvas. | String | Reporting\ReportingServer | Valor da política não gravado (igual a não configurado) |
| ReportingDataCacheLimit | Não está disponível. | Especifica o tamanho máximo em megabytes (MB) do cache XML para armazenar informações de relatório. O tamanho se aplica ao cache na memória. Quando o limite for atingido, o arquivo de log será revertido. Definido entre 0 e 1024. | Inteiro [0-1024] | Reporting\DataCacheLimit | Valor da política não gravado (igual a não configurado) |
| ReportingDataBlockSize| Não está disponível. | Especifica o tamanho máximo em bytes a ser transmitido para o servidor para relatar solicitações de carregamento. Isso pode ajudar a evitar falhas de transmissão permanente quando o log atingir um tamanho significativo. Definido entre 1024 e ilimitado. | Inteiro [1024-ilimitado] | Reporting\DataBlockSize | Valor da política não gravado (igual a não configurado) |
| ReportingStartTime | Não está disponível. | Especifica o tempo de início do cliente para enviar dados ao servidor de relatórios. Você deve especificar um inteiro válido entre 0-23 correspondente à hora do dia. Por padrão, o **ReportingStartTime** começará no dia atual em 10 P. M ou 22.<br>**Observação** Você deve definir essa configuração para um horário em que os computadores que executam o cliente App-V 5,1 têm menos probabilidade de ficar offline. | Inteiro (0 – 23) | Relatórios \ StartTime | Valor da política não gravado (igual a não configurado) |
| ReportingInterval | Não está disponível. | Especifica o intervalo de repetição que o cliente usará para reenviar dados ao servidor de relatórios. | Inteiro | Reporting\RetryInterval | Valor da política não gravado (igual a não configurado) |
| ReportingRandomDelay | Não está disponível. | Especifica o atraso máximo (em minutos) dos dados a serem enviados para o servidor de relatórios. Quando a tarefa agendada for iniciada, o cliente gerará um atraso aleatório entre 0 e **ReportingRandomDelay** e esperará a duração especificada antes de enviar os dados. Isso pode ajudar a evitar colisões no servidor. | Inteiro [0-ReportingRandomDelay] | Reporting\RandomDelay | Valor da política não gravado (igual a não configurado) |
| EnableDynamicVirtualization<br>**Importante** Essa configuração está disponível somente com o App-V 5,0 SP2 ou posterior. | Não está disponível. | Habilita as extensões do shell com suporte, os objetos auxiliares do navegador e os controles ActiveX para serem virtualizados e executados com aplicativos virtuais. | 1 (habilitado), 0 (desabilitado) | HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Virtualization | |
| EnablePublishingRefreshUI<br>**Importante** Essa configuração está disponível somente com o App-V 5,0 SP2. | Não está disponível. | Habilita a barra de progresso de atualização de publicação do computador que executa o cliente App-V 5,1. | 1 (habilitado), 0 (desabilitado) | HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Publishing | |
| HideUI<br>**Importante**  Essa configuração está disponível somente com o App-V 5,0 SP2.| Não está disponível. | Oculta a barra de progresso de atualização de publicação. | 1 (habilitado), 0 (desabilitado) | | |
| ProcessesUsingVirtualComponents | Não está disponível. | Especifica uma lista de caminhos de processo (que podem conter caracteres curinga), que são candidatos ao uso de virtualização dinâmica (extensões do shell com suporte, objetos auxiliares do navegador e controles ActiveX). Somente os processos cujo caminho completo corresponde a um desses itens podem usar a virtualização dinâmica. | String | Virtualization\ProcessesUsingVirtualComponents | Cadeia de caracteres vazia. |






## Tópicos relacionados


[Implantação do sequenciador e do cliente App-V 5.1](deploying-the-app-v-51-sequencer-and-client.md)

[Como modificar a configuração do cliente App-V 5.1 usando o modelo ADMX e a Política de Grupo](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md)

[Como implantar o cliente do App-V](how-to-deploy-the-app-v-client-51gb18030.md)

 

 





